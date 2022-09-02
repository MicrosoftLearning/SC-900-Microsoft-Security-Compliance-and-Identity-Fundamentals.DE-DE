---
Demo:
  title: Azure-Netzwerksicherheitsgruppen (Network Security Groups, NSGs)
  module: 'Module 3 Lesson 1: Describe the capabilities of Microsoft security solutions: Describe basic security capabilities in Azure.'
ms.openlocfilehash: 34a08ed5a6edd845087e4ed4b5d94d4f06bc8f89
ms.sourcegitcommit: 07d6d5b9df44c747453e21a65bca524afbaf85ae
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2022
ms.locfileid: "147695304"
---
# <a name="demo-azure-network-security-groups-nsgs"></a>Demo: Azure-Netzwerksicherheitsgruppen (Network Security Groups, NSGs)

## <a name="demo-scenario"></a>Demoszenario

In dieser Demo zeigen Sie die Funktionalität einer Netzwerksicherheitsgruppe (NSG) in Azure.  Dazu erstellen Sie im Rahmen der Einrichtung vor der Demo zunächst einen virtuellen Computer (Virtual Machine, VM) ohne NSG. Zudem erstellen Sie eine NSG ohne zugehörige Schnittstelle oder Subnetz.  Im Rahmen der Demo zeigen Sie die standardmäßigen Ein- und Ausgangsregeln für die NSG. Anschließend durchlaufen Sie den Prozess zum Zuweisen der Schnittstelle der VM zur NSG.  Nach der Konfiguration testen Sie mithilfe der standardmäßigen NSG-Regeln und auch der von Ihnen erstellten Regeln die Verbindung mit der VM.
  
### <a name="pre-demo-setup-part-1"></a>Einrichtung vor der Demo – Teil 1

 Kursleitern sollten dies **VOR** der Kurszeit ausführen, da das Erstellen einer VM mehrere Minuten dauern kann. Im Rahmen dieser Einrichtung erstellen Sie einen virtuellen Computer unter Windows 10.

1. Öffnen Sie die Registerkarte **Startseite – Microsoft Azure** in Ihrem Browser.  Falls Sie die Registerkarte geschlossen haben, öffnen Sie eine Browserseite. Geben Sie „portal.azure.com“ in die Adressleiste ein, und melden Sie sich erneut an.

1. Geben Sie in das Suchfeld, das sich auf dem blauen Balken oben auf der Seite neben dem Text „Microsoft Azure“ befindet, den Text **Virtuelle Computer** ein, und wählen Sie dann **Virtuelle Computer** aus den Suchergebnissen aus.  

1. Wählen Sie oben links auf der Seite **+Hinzufügen** und dann **+Virtueller Computer** aus.

1. Tragen Sie auf der Registerkarte „Grundlagen“ die folgenden Informationen (übernehmen Sie für nicht aufgeführte Elemente die Standardeinstellungen) ein:
    1. **Abonnement**: Bestätigen Sie, dass die Standardeinstellung „Azure Pass-Förderung“ lautet.
    1. **Ressourcengruppe**: Wählen Sie **Neue erstellen** aus. Geben Sie dann **LabsSC900-RG** in das Feld „Name“ ein, und wählen Sie **OK** aus.
    1. **Name des virtuellen Computers**: Geben Sie **SC900-WinVM** ein.
    1. **Region**: Übernehmen Sie den Standardwert.
    1. **Verfügbarkeitsoptionen**: Wählen Sie **Keine Infrastrukturredundanz erforderlich** aus.  HINWEIS: Es ist sehr wichtig, „Verfügbarkeitsoptionen“ auf „Keine Infrastrukturredundanz erforderlich“ festzulegen. Andernfalls funktioniert die Demo nicht wie gewünscht.  Wenn eine Verfügbarkeitsoption vorhanden ist, ist eine NSG erforderlich, wobei wir die VM mit Absicht ohne eine NSG erstellen.
    1. **Bild**: Wählen Sie im Dropdownmenü **Windows 10 Pro, Version 21H2 – Gen 2** aus.
    1. **Größe**: Wählen Sie im Dropdownmenü **Alle Größen anzeigen** und dann **B2s** aus. Klicken Sie anschließend unten auf der Seite auf **Auswählen**.
    1. **Benutzername**:  Geben Sie den gewünschten Benutzernamen ein.  Notieren Sie sich diesen, da Sie ihn für den Zugriff auf den virtuellen Computer benötigen.
    1. **Kennwort:**  Geben Sie ein Kennwort Ihrer Wahl ein.  Notieren Sie sich dieses, da Sie es für den Zugriff auf den virtuellen Computer benötigen.
    1. **Öffentliche eingehende Ports**: Verlassen Sie die Standardeinstellung, **Ausgewählte Ports zulassen**.
    1. **Eingehende Ports auswählen**: Verlassen Sie die Standardeinstellung, **RDP 3389**
    1. **Lizenz**: Wählen Sie **Ich bestätige, dass ich über eine berechtigte Windows 10-Lizenz mit Rechten für mehrinstanzenfähiges Hosting verfüge** aus, sodass im Kontrollkästchen ein Häkchen angezeigt wird.
    1. Klicken Sie auf **Weiter: Datenträger**.

1. Sie befinden sich nun auf der Registerkarte „Datenträger“ für die VM-Konfiguration.  Übernehmen Sie alle Standardeinstellungen, und wählen Sie **Weiter: Netzwerk >** aus.
1. Sie befinden sich nun auf der Registerkarte „Netzwerk“ für die VM-Konfiguration.  Wählen Sie für die NIC-Netzwerksicherheitsgruppe die Option **Keine** aus. Belassen Sie für alle anderen Einstellungen die Standardwerte.
1. Wählen Sie unten auf der Seite **Weiter: Überprüfen + erstellen>** aus, nachdem die Überprüfung bestanden wurde, wählen Sie **Erstellen** aus. Der Abschluss der VM-Bereitstellung kann mehrere Minuten dauern.
1. Wählen Sie nach Abschluss der VM-Bereitstellung die Option **Zu Ressource wechseln** aus.
1. Sie befinden sich nun auf der Seite „SC900-WinVM“.
1. Wählen Sie oben auf der Seite **Verbinden** aus. Wählen Sie anschließend im Dropdown **RDP** aus.
1. Beachten Sie, dass die Portvoraussetzungen nicht erfüllt sind.  Damit die Voraussetzung erfüllt werden kann, muss eine eingehende Netzwerksicherheitsregel mit dem Zielport 3389, der von RDP verwendet wird, konfiguriert werden.  Dies werden Sie in der nächsten Aufgabe tun, wenn Sie eine Netzwerksicherheitsgruppe erstellen.
1. Lassen Sie diese Browserregisterkarte geöffnet.


### <a name="pre-demo-setup-part-2"></a>Einrichtung vor der Demo – Teil 2

Erstellen Sie eine Netzwerksicherheitsgruppe, OHNE dieser NSG die Netzwerkschnittstelle der VM zuzuweisen.  

1. Öffnen Sie in Ihrem Browser die Registerkarte „SC900-WinVM – Microsoft Azure“.

1. Geben Sie in das Suchfeld, das sich auf dem blauen Balken oben auf der Seite neben dem Text „Microsoft Azure“ befindet, den Text **Netzwerksicherheitsgruppe** ein, und wählen Sie dann **Netzwerksicherheitsgruppen** aus den Suchergebnissen aus.  Wählen Sie nicht „Netzwerksicherheitsgruppen – klassisch“ aus.

1. Wählen Sie oben auf der Seite „Netzwerksicherheitsgruppen“ die Option **+ Erstellen** aus.

1. Geben Sie auf der Registerkarte „Grundlagen“ der Seite „Netzwerksicherheitsgruppe erstellen“ die folgenden Einstellungen an:
    1. Abonnement:  Azure Pass-Förderung
    1. Ressourcengruppe:  **LabsSC900-RG**
    1. Name:  **NSG-SC900**
    1. Region: Übernehmen Sie den Standardwert
    1. Wählen Sie **Bewerten + erstellen** und dann **Erstellen** aus.

1. Wählen Sie nach Abschluss der Bereitstellung **Zu Ressource wechseln** aus, und stellen Sie sicher, dass alles in Ordnung ist.  Dort sollten 3 standardmäßige Eingangs-, 3 standardmäßige Ausgangsregeln, keine Subnetze und keine Schnittstellen vorhanden sein, die der NSG zugeordnet sind.  Wechseln Sie zurück zur **Startseite** des Azure-Portals.  

### <a name="demo"></a>Demo

Gehen Sie die Einstellungen für eine NSG durch.  In diesem Fall gehen Sie sie für eine vorhandene NSG (die von Ihnen oben bei der Einrichtung erstellte) durch, die bisher noch keiner VM-Schnittstelle zugewiesen wurde. Anschließend zeigen Sie den Prozess zum Verknüpfen einer Schnittstelle mit der NSG und den Prozess zum Erstellen von Eingangs- und Ausgangsregeln.

1. Öffnen Sie die Browserregisterkarte **Startseite – Microsoft Azure**.  Falls Sie die Registerkarte geschlossen haben, öffnen Sie eine Browserseite. Geben Sie „portal.azure.com“ in die Adressleiste ein, und melden Sie sich erneut an.

1. Geben Sie in das Suchfeld, das sich auf dem blauen Balken oben auf der Seite neben dem Text „Microsoft Azure“ befindet, den Text **Netzwerksicherheitsgruppe** ein, und wählen Sie dann **Netzwerksicherheitsgruppen** aus den Suchergebnissen aus.  Wählen Sie nicht „Netzwerksicherheitsgruppen – klassisch“ aus.

1. Wählen Sie auf der Seite „NSG“ die NSG **NSG-SC900** aus, die Sie bei der Einrichtung erstellt haben.

1. Die Registerkarte **Übersicht** im linken Navigationsbereich wird hervorgehoben.  Beachten Sie die standardmäßigen Eingangs- und Ausgangsregeln in der NSG. Obwohl die NSG erstellt wurde und keine Standardregeln zum Filtern des Datenverkehrs vorhanden sind, wurde der NSG keine Schnittstelle zugeordnet. Dies können Sie oben rechts auf der Seite nachvollziehen. Dort steht „Verknüpft mit: 0 Subnetzen, 0 Netzwerkschnittstellen“.  Damit eine NSG ihrer Aufgabe nachkommt, muss sie einem anderen Element zugewiesen sein.  In unserem Fall weisen wir sie der Netzwerkschnittstelle für die zuvor erstellte VM zu.

1. Wählen Sie auf der Seite „NSG-SC900“ im linken Navigationsbereich unter „Einstellungen“ die Option **Netzwerkschnittstellen** aus.

1. Wählen Sie oberhalb des Suchfelds **+ Zuordnen** aus. Wählen Sie dann im Dropdown **sc900-winvmXXX** (das XXX ist spezifisch für die Netzwerkschnittstelle Ihrer VM) und dann **OK** aus. Während die Schnittstelle zugeordnet wird, wird in der oberen rechten Ecke des Bildschirms ein Benachrichtigungsfeld angezeigt. Sobald der NSG die Schnittstelle zugeordnet ist, wird sie in der Liste angezeigt.

1. Wechseln Sie zurück zur Registerkarte **Übersicht**.  Beachten Sie, dass oben rechts auf der Seite „Verknüpft mit: 0 Subnetze, 1 Netzwerkschnittstelle“ angezeigt wird. Entsprechend ist der NSG nun die Schnittstelle zugewiesen. Heben Sie den Kursteilnehmern gegenüber auch die Standardregeln hervor. Bei Eingangsregeln ist nur Datenverkehr von anderen Azure Virtual Networks und Azure Load Balancer zulässig. Der gesamte andere eingehende Datenverkehr zur VM wird verweigert. Heben Sie zudem die Standardausgangsregeln hervor.  Es sind lediglich ausgehender Datenverkehr zu anderen VNETs und ausgehender Internetdatenverkehr zulässig.  Im Rahmen der Demo sollten Sie sich die Zeit nehmen und zeigen, dass eingehender Datenverkehr verweigert wird.
    1. Geben Sie oben auf der Seite in die Suchleiste den Text **Virtuelle Computer** ein, und wählen Sie den Eintrag aus.
    1. Wählen Sie **SC900-WinVM** auf der Seite „Virtuelle Computer“ aus.
    1. Wählen Sie oben auf der Seite „SC900-WinVM“ die Option **Verbinden** und dann **RDP** aus.
    1. Beachten Sie, dass die Portvoraussetzungen nicht erfüllt sind.  Damit die Voraussetzung erfüllt werden kann, muss eine eingehende Netzwerksicherheitsregel mit dem Zielport 3389, der von RDP verwendet wird, konfiguriert werden.  

1. Jetzt werden Sie eine neue Regel erstellen wollen, um eingehenden RDP-Datenverkehr zuzulassen.  Heben Sie hervor, dass Sie die vorhandenen Standardregeln nicht löschen können. Sie können lediglich neue mit einer höheren Priorität erstellen. Wählen Sie im linken Navigationsbereich unter „Einstellungen“ die Option **Netzwerk** aus.  Sie befinden sich auf der Netzwerktechnologieseite der VM.
1. Stellen Sie sicher, dass die Registerkarte **Regeln für eingehende Ports** ausgewählt (unterstrichen) ist und wählen Sie dann **Regel für eingehenden Port hinzufügen** zum Erstellen der Regel mit den folgenden Einstellungen, um eingehenden RDP-Datenverkehr zuzulassen:
    1. Quelle: **Alle**
    1. Quellportbereiche: **\***
    1. Ziel: **Beliebig**
    1. Dienst: **RDP**
    1. Aktion: **Zulassen**
    1. Priorität: **300**, Hinweis: Regeln mit niedrigeren Zahlen haben eine höhere Priorität und werden zuerst verarbeitet. Entsprechend muss die Priorität für diese neue Regel höher als die Priorität für die vorhandene Regel sein, die den gesamten eingehenden Datenverkehr verweigert.
    1. Name: **AllowRDP**
    1. Wählen Sie **Hinzufügen** aus.
    1. Nach der Bereitstellung der Regel wird sie in der Liste der Eingangsregeln angezeigt.

1. Wählen Sie nun die Registerkarte **Regeln für ausgehende Ports** aus, und überprüfen Sie die Standardregeln.  Wählen Sie oben auf der Seite **Regel für ausgehenden Port hinzufügen** aus, und nehmen Sie die verschiedenen Einstellungen vor.  Ich empfehle, die Regel zu erstellen – über die folgenden Einstellungen wird eine Regel zum Verweigern des ausgehenden Internetdatenverkehrs erstellt:
    1. Quelle: **Alle**
    1. Quellportbereiche: **\***
    1. Ziel: **Diensttag**
    1. Zieldiensttag: **Internet**
    1. Dienst: **Benutzerdefiniert** (übernehmen Sie den Standardwert)
    1. Zielportbereiche: **\*** (Sternchen im Feld für Zielportbereiche eingeben)
    1. Protokoll: **Alle**
    1. Aktion: **Deny**
    1. Priorität: **4000** (dies sollte hervorgehoben werden, da die Priorität höher sein muss als die Priorität für die vorhandene Regel, welche den ausgehenden Internetdatenverkehr zulässt)
    1. Name: **DenyInternet**
    1. Wählen Sie **Hinzufügen** aus.
    1. Nach der Bereitstellung der Regel wird sie in der Liste der Ausgangsregeln angezeigt.

1. Wechseln Sie nun zurück zu Ihrer VM, und testen Sie die Regeln.  Wählen Sie oben auf der Seite die Option **SC900-VM** aus.

1. Testen Sie die Eingangsregel, indem Sie sicherstellen, dass Sie über das RDP eine Verbindung mit der VM herstellen können.
    1. Wählen Sie im linken Navigationsbereich **Verbinden** aus.
    1. Stellen Sie sicher, dass die IP-Adresse auf „Öffentliche IP-Adresse“ festgelegt ist, übernehmen Sie die Standardportnummer, und wählen Sie **RDP-Datei herunterladen** aus.
    1. **Öffnen** Sie die heruntergeladene-Datei, und wählen Sie **Verbinden** aus.
    1. Sie werden aufgefordert, Ihre Anmeldeinformationen einzugeben. Geben Sie den Benutzernamen und das Kennwort ein, die Sie beim Erstellen der VM verwendet haben.  Wenn Sie im Fenster, von dem Sie aufgefordert werden, Ihre Anmeldeinformationen einzugeben, eine PIN eingeben müssen, wählen Sie **Weitere Optionen** und dann **Anderes Konto verwenden** aus.
    1. Ein Remotedesktop-Verbindungsfenster wird geöffnet und gibt „Die Identität des Remotecomputers kann nicht überprüft werden. Möchten Sie die Verbindung dennoch herstellen?“ an. Wählen Sie **Ja** aus.
    1. Sie sind nun mit der VM verbunden. Verdeutlichen Sie dem bzw. der Kursteilnehmer*in, dass Sie in diesem Fall eine Verbindung mit der VM herstellen konnten, da die von Ihnen erstellte Regel für eingehenden Datenverkehr den eingehenden Datenverkehr zur VM über RDP zulässt.

1. Testen Sie nun die NSG-Regel für ausgehenden Datenverkehr.
    1. Öffnen Sie in der VM den Edge-Browser.
    1. Geben Sie **www.bing.com** ein. Die Seite sollte nicht angezeigt werden. Hinweis: Wenn Sie eine Verbindung mit dem Internet herstellen können und sichergestellt haben, dass alle Parameter für die Ausgangsregel ordnungsgemäß festgelegt wurden, liegt dies wahrscheinlich daran, dass es ein paar Minuten dauern kann, bis die Regel wirksam wird. Warten Sie einige Minuten, und versuchen Sie erneut.

1. Schließen Sie die Remotedesktopverbindung. Wählen Sie dazu oben zentral auf der Seite, wo die IP-Adresse angezeigt wird, das **X** aus. Ein Popupfenster gibt „Die Remotesitzung wird getrennt“ an. Klicken Sie auf **OK**.

1. Wechseln Sie zur Startseite des Azure-Portals zurück. Wählen Sie dazu oben auf der Seite auf dem blauen Balken **Microsoft Azure** aus.

### <a name="post-course-delivery-tear-down"></a>Löschen von Daten und Ressourcen nach Abschluss des Kurses

VMs sind eine Ressource, die in Rechnung gestellt wird. Obwohl die Kosten für die Ausführung der VMs in dieser Demo gering sind, wird empfohlen, bei Abschluss dieses Kurses die Ressourcengruppe zu löschen, die die VM sowie zugehörige Ressourcen enthält.

1. Öffnen Sie in Ihrem Browser die Registerkarte „SC900-WinVM – Microsoft Azure“.

1. Wählen Sie in der oberen linken Ecke der Seite **Alle Dienste** aus.

1. Geben Sie in das Feld „Dienste filtern“ neben „Alle Dienste“ den Text **Ressourcengruppen** ein, und wählen Sie dann **Ressourcengruppen** aus den Ergebnissen aus.

1. Wählen Sie **LabsSC900-RG** aus.

1. Wählen Sie im oberen mittleren Bereich der LabsSC900-RG-Seite die Option **Ressourcengruppe löschen** aus.

1. Geben Sie in das Fenster, das geöffnet wird, den Namen der Ressourcengruppe **LabsSC900-RG** ein, um die Löschung der Ressourcengruppe und aller zugehöriger Ressourcen zu bestätigen. Wählen Sie dann unten auf der Seite **Löschen** aus.

1. Es kann ein paar Minuten dauern, bis alle Ressourcen und die Ressourcengruppe gelöscht sind.

#### <a name="review"></a>Überprüfung

In dieser Demo haben Sie die Informationen und Einstellungen in Bezug auf eine NSG gezeigt, darunter den Prozess zum Zuordnen einer Schrittstelle zur einer NSG. Sie haben die standardmäßigen Eingangs- und Ausgangsregeln und schließlich die Schritte zum Erstellen einer neuen Regel gezeigt.
