---
lab:
  title: Erkunden von Azure-Netzwerksicherheitsgruppen (Network Security Groups, NSGs)
  module: 'Module 3 Lesson 1: Describe the capabilities of Microsoft security solutions: Describe basic security capabilities in Azure.'
ms.openlocfilehash: 47f71fdf1587a240803bb508a902ce098253793d
ms.sourcegitcommit: 07d6d5b9df44c747453e21a65bca524afbaf85ae
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2022
ms.locfileid: "147695292"
---
# <a name="lab-explore-azure-network-security-groups-nsgs"></a>Lab: Erkunden von Azure-Netzwerksicherheitsgruppen (Network Security Groups, NSGs)

## <a name="lab-scenario"></a>Labszenario

In diesem Lab erkunden Sie die Funktion von Netzwerksicherheitsgruppen in Azure.  Das werden Sie durch das Erstellen der VM ohne jegliche Netzwerksicherheitsgruppe (NSG) tun. Anschließend durchlaufen Sie den Prozess zum Erstellen einer NSG und zum Zuweisen der Schnittstelle der VM zu dieser NSG.  Nach der Konfiguration werden Sie die Standardregeln für eingehende und ausgehende Regeln beobachten und neue Regeln erstellen.
  
**Geschätzte Dauer**: 15 bis 20 Minuten

### <a name="task-1"></a>Aufgabe 1

Bei dieser Aufgabe erstellen Sie einen virtuellen Computer unter Windows 10.

1. Öffnen Sie Microsoft Edge.  Geben Sie **portal.azure.com** in die Adressleiste ein.

1. Melden Sie sich mit Ihren Administratoranmeldeinformationen an.
    1. Geben Sie **admin@WWLxZZZZZZ.onmicrosoft.com** (ZZZZZZ ist hierbei die eindeutige Mandanten-ID, die von Ihrem Labhostinganbieter bereitgestellt wurde) in das Fenster „Anmelden“ ein, und wählen Sie dann **Weiter** aus.

    1. Geben Sie das Administratorkennwort ein, das Sie vom Labhostinganbieter erhalten haben sollten. Wählen Sie **Anmelden**.
    1. Wählen Sie **Ja** aus, wenn Sie gefragt werden, ob Sie angemeldet bleiben möchten.
1. Wählen Sie in der oberen linken Ecke des Bildschirms neben dem Text „Microsoft Azure“ das Symbol „Portalmenü anzeigen“ (die drei horizontalen Linien werden auch als Hamburgersymbol bezeichnet) und dann **Alle Dienste** aus.  
1. Wählen Sie im Hauptfenster unter „Empfohlen“ die Option „Virtuelle Computer“ aus.  Wenn „Virtuelle Computer“ nicht aufgelistet wird, geben Sie den entsprechenden Text in die Suchleiste ein, und treffen Sie dann die Auswahl aus den Suchergebnissen.
1. Wählen Sie oben links auf der Seite **+Erstellen** und dann **+Virtueller Azure-Computer** aus.
1. Tragen Sie auf der Registerkarte „Grundlagen“ die folgenden Informationen (übernehmen Sie für nicht aufgeführte Elemente die Standardeinstellungen) ein:
    1. Abonnement: Bestätigen Sie, dass die Standardeinstellung „Azure Pass-Förderung“ lautet.

    1. Ressourcengruppe: Wählen Sie **Neu erstellen** aus. Geben Sie dann **LabsSC900-RG** in das Feld „Name“ ein, und wählen Sie **OK** aus.
    1. Name des virtuellen Computers: Geben Sie **SC900-WinVM** ein.
    1. Region: Wenn das Regionsfeld nicht vorab ausgefüllt ist, wählen Sie die Region aus, die Ihrem Standort am nächsten ist.
    1. Bild: Wählen Sie im Dropdownmenü **Windows 10 Pro, Version 21H2 – Gen 2** aus.
    1. Größe: Wählen Sie im Dropdownmenü **Alle Größen anzeigen** und dann **B2s** aus. Klicken Sie anschließend unten auf der Seite auf **Auswählen**.
    1. Benutzername:  Geben Sie den gewünschten Benutzernamen ein.  Notieren Sie sich diesen, da Sie ihn für den Zugriff auf den virtuellen Computer benötigen.
    1. Kennwort:  Geben Sie ein Kennwort Ihrer Wahl ein.  Notieren Sie sich dieses, da Sie es für den Zugriff auf den virtuellen Computer benötigen.
    1. Öffentliche eingehende Ports: Verlassen Sie die Standardeinstellung, **Ausgewählte Ports zulassen**.
    1. Eingehende Ports auswählen: Verlassen Sie die Standardeinstellung, **RDP 3389**.
    1. Lizenz: Wählen Sie **Ich bestätige, dass ich über eine berechtigte Windows 10-Lizenz mit Rechten für mehrinstanzenfähiges Hosting verfüge** aus, sodass im Kontrollkästchen ein Häkchen angezeigt wird.
    1. Klicken Sie auf **Weiter: Datenträger**.
1. Sie befinden sich nun auf der Registerkarte „Datenträger“ für die VM-Konfiguration.  Übernehmen Sie alle Standardeinstellungen, und wählen Sie **Weiter: Netzwerk >** aus.
1. Sie befinden sich nun auf der Registerkarte „Netzwerk“ für die VM-Konfiguration.  Wählen Sie für die NIC-Netzwerksicherheitsgruppe die Option **Keine** aus. Belassen Sie für alle anderen Einstellungen die Standardwerte.  Hinweis: Der Zweck beim Auswählen von "None" in diesem Schritt besteht darin, die Schritte zum Erstellen einer Netzwerksicherheitsgruppe in der nachfolgenden Aufgabe von Grund auf zu durchlaufen.
1. Wählen Sie unten auf der Seite **Weiter: Überprüfen + erstellen>** aus, nachdem die Überprüfung bestanden wurde, wählen Sie **Erstellen** aus. Der Abschluss der VM-Bereitstellung kann mehrere Minuten dauern.
1. Wählen Sie nach Abschluss der VM-Bereitstellung die Option **Zu Ressource wechseln** aus.
1. Sie befinden sich nun auf der Seite „SC900-WinVM“.
1. Wählen Sie oben auf der Seite **Verbinden** aus. Wählen Sie anschließend im Dropdown **RDP** aus.
1. Beachten Sie, dass die Portvoraussetzungen nicht erfüllt sind.  Damit die Voraussetzung erfüllt werden kann, muss eine eingehende Netzwerksicherheitsregel mit dem Zielport 3389, der von RDP verwendet wird, konfiguriert werden.  Dies werden Sie in der nächsten Aufgabe tun, wenn Sie eine Netzwerksicherheitsgruppe erstellen.
1. Lassen Sie diese Browserregisterkarte geöffnet.

### <a name="task-2"></a>Aufgabe 2

Erstellen Sie eine Netzwerksicherheitsgruppe, weisen Sie die Netzwerkschnittstelle der VM dieser NSG zu, und erstellen Sie eine neue Regel für eingehenden RDP-Datenverkehr.

1. Öffnen Sie in Ihrem Browser die Registerkarte „SC900-WinVM – Microsoft Azure“.

1. Wählen Sie in der oberen linken Ecke der Seite neben dem Text „Microsoft Azure“ das Symbol „Portalmenü anzeigen“ (die drei horizontalen Linien werden auch als Hamburgersymbol bezeichnet) und dann **Alle Dienste** aus.
1. Geben Sie in das Feld „Dienste filtern“ neben „Alle Dienste“ den Text **Netzwerksicherheitsgruppen** ein. Wählen Sie dann **Netzwerksicherheitsgruppen** (ohne „Netzwerksicherheitsgruppen – klassisch“ auszuwählen) aus den Ergebnissen aus.
1. Wählen Sie oben auf der Seite „Netzwerksicherheitsgruppen“ die Option **+ Erstellen** aus.
1. Geben Sie auf der Registerkarte „Grundlagen“ der Seite „Netzwerksicherheitsgruppe erstellen“ die folgenden Einstellungen an:
    1. Abonnement:  Azure Pass-Förderung

    1. Ressourcengruppe:  **LabsSC900**
    1. Name:  **NSG-SC900**
    1. Region: Übernehmen Sie den Standardwert.
    1. Wählen Sie **Bewerten + erstellen** und dann **Erstellen** aus.
1. Klicken Sie nach Abschluss der Bereitstellung auf **Zu Ressource wechseln**.
1. Beachten Sie die standardmäßigen Eingangs- und Ausgangsregeln in der NSG.  Obwohl die NSG erstellt wurde und keine Standardregeln zum Filtern des Datenverkehrs vorhanden sind, wurde der NSG keine Schnittstelle zugeordnet.
1. Wählen Sie auf der Seite „NSG-SC900“ im linken Navigationsbereich unter „Einstellungen“ die Option **Netzwerkschnittstellen** aus.
1. Wählen Sie oberhalb des Suchfelds die Option **+ Zuordnen** aus.
1. Auf der rechten Seite der Seite ist ein Feld zum Auswählen der Netzwerkschnittstelle, die der NSG zugeordnet werden soll. Wählen Sie den Dropdownpfeil aus, und wählen Sie dann **sc900-winvmXXX** aus (das XXX wird für die Netzwerkschnittstelle Ihrer VM spezifisch sein), und wählen Sie dann unten im Fenster **Ok** aus.
1. Sobald der NSG die Schnittstelle zugeordnet ist, wird sie in der Liste angezeigt.
1. Wählen Sie im linken Navigationsbereich **Eingehende Sicherheitsregeln** aus.
1. Die standardmäßigen eingehenden Regeln verweigern den gesamten eingehenden Datenverkehr, der nicht von einem Vnet oder einem Azure Load Balancer stammt, sodass Sie eine Regel einrichten müssen, eingehenden RDP-Datenverkehr (Datenverkehr auf Port 3389) zuzulassen. Erinnern Sie sich, dass Sie die Standardregeln nicht entfernen, aber außer Kraft setzen können, indem Sie Regeln mit höheren Prioritäten erstellen.
1. Wählen Sie oben auf der Seite die Option **Hinzufügen** aus:
1. Geben Sie auf der Seite „Eingehende Sicherheitsregel hinzufügen“ die folgenden Einstellungen an:
    1. Quelle:  **Alle**

    1. Quellportbereiche: **\***
    1. Ziel:  **Alle**
    1. Dienst:  **RDP**
    1. Aktion:  **Zulassen**
    1. Priorität:  **300**, Hinweis: Regeln mit niedrigeren Zahlen haben eine höhere Priorität und werden zuerst verarbeitet.
    1. Name:  **AllowRDP**
1. Wählen Sie **Hinzufügen** aus.
1. Sobald die Regel bereitgestellt wurde, wird sie in der Liste der eingehenden Regeln angezeigt (Möglicherweise müssen Sie den Bildschirm aktualisieren).
1. Stellen Sie nun sicher, dass Sie über das RDP eine Verbindung mit der VM herstellen können.  Wählen Sie das Suchfeld oben auf der Seite aus, neben dem Bereich, an dem Microsoft Azure steht, um die zuletzt verwendeten Dienste anzuzeigen.  Wählen Sie **Virtuelle Computer** aus.
1. Wählen Sie die VM **SC900-WinVM** aus.
1. Wählen Sie oben auf der Seite **Verbinden** aus. Wählen Sie anschließend im Dropdown **RDP** aus.
1. Stellen Sie sicher, dass die IP-Adresse auf „Öffentliche IP-Adresse“ festgelegt ist, übernehmen Sie die Standardportnummer, und wählen Sie **RDP-Datei herunterladen** aus.
1. Öffnen Sie die heruntergeladene-Datei, und wählen Sie **Verbinden** aus.
1. Sie werden aufgefordert, Ihre Anmeldeinformationen einzugeben.  Geben Sie den Benutzernamen und das Kennwort ein, die Sie beim Erstellen der VM verwendet haben.
1. Ein Remotedesktop-Verbindungsfenster wird geöffnet und gibt „Die Identität des Remotecomputers kann nicht überprüft werden.  Möchten Sie die Verbindung dennoch herstellen?“ an.  Wählen Sie **Ja** aus.
1. Sie sind nun mit der VM verbunden. In diesem Fall konnten Sie eine Verbindung mit der VM herstellen, da die von Ihnen erstellte Regel für eingehenden Datenverkehr eingehenden Datenverkehr zur VM über das RDP zulässt.
1. Lassen Sie die VM geöffnet. Sie werden sie bei der nächsten Aufgabe verwenden.

### <a name="task-3"></a>Aufgabe 3

Die Standardausgangsregeln für NSG lassen ausgehenden Internetdatenverkehr zu. Daher überprüfen Sie, ob Sie eine Verbindung mit dem Internet herstellen können.  Anschließend durchlaufen Sie den Prozess zum Erstellen einer benutzerdefinierten Ausgangsregel, um ausgehenden Internetdatenverkehr zu blockieren und diese Regel zu testen.

1. Wählen Sie in der VM **Edge** aus, um den Browser zu öffnen.  
1. Geben Sie **www.bing.com** in die Adressleiste des Browsers ein, und bestätigen Sie, dass Sie eine Verbindung mit der Suchmaschine herstellen können.
1. Schließen Sie auf Ihrer VM den Browser. Lassen Sie die VM jedoch geöffnet, da Sie sie in den nachfolgenden Schritten verwenden.
1. Kehren Sie zum Azure-Portal zurück, und öffnen Sie im Browser die Registerkarte „SC900-WinVM – Microsoft Azure“.
1. Wählen Sie im linken Navigationsbereich unter „Einstellungen“ die Option **Netzwerk** aus.
1. Wählen Sie die Registerkarte **Regeln für ausgehende Ports** aus.  Die Standardausgangsregeln werden angezeigt.  Beachten Sie die Standardregel „AllowInternetOutBound“. Diese Regel lässt sämtlichen ausgehenden Internetdatenverkehr zu. Sie können die Standardregel nicht entfernen. Sie können sie jedoch überschreiben, indem Sie eine Regel mit höherer Priorität erstellen. Wählen Sie rechts auf der Seite **Regel für ausgehenden Port hinzufügen** aus:
1. Geben Sie auf der Seite „Ausgangssicherheitsregel hinzufügen“ die folgenden Einstellungen an:
    1. Quelle:  **Alle**

    1. Quellportbereiche: **\***
    1. Ziel:  **Diensttag**
    1. Zieldiensttag:  **Internet**
    1. Dienst:  **Benutzerdefiniert** (übernehmen Sie den Standardwert)
    1. Zielportbereiche:  * (Sternchen im Feld für Zielportbereiche eingeben)
    1. Protokoll: **Alle**
    1. Aktion: **Deny**
    1. Priorität:  **4000**
    1. Name:  **DenyInternet**
1. Wählen Sie **Hinzufügen** aus.
1. Nach der Bereitstellung der Regel wird sie in der Liste der Ausgangsregeln angezeigt.  Obwohl sie in der Liste angezeigt wird, dauert es ein paar Minuten, bis sie wirksam wird (warten Sie ein paar Minuten, bevor Sie mit den nächsten Schritten fortfahren).  
1. Wechseln Sie zurück zu Ihrer VM zurück.
1. Öffnen Sie in Ihrer VM den Edge-Browser, und geben Sie **www.bing.com** ein. Die Seite sollte nicht angezeigt werden.  Hinweis: Wenn Sie eine Verbindung mit dem Internet herstellen können und sichergestellt haben, dass alle Parameter für die Ausgangsregel ordnungsgemäß festgelegt wurden, liegt dies wahrscheinlich daran, dass es ein paar Minuten dauern kann, bis die Regel wirksam wird.  Schließen Sie den Browser, warten Sie ein paar Minuten, und versuchen Sie es erneut.
1. Schließen Sie die Remotedesktopverbindung. Wählen Sie dazu oben zentral auf der Seite, wo die IP-Adresse angezeigt wird, das **X** aus.  Ein Popupfenster gibt „Die Remotesitzung wird getrennt“ an. Klicken Sie auf **OK**.
1. Bei dieser Aufgabe haben Sie erfolgreich eine Ausgangsregel in Ihrer NSG konfiguriert, um ausgehenden Internetdatenverkehr zu blockieren.

### <a name="tear-down"></a>Nachbereitung

VMs sind eine Ressource, die in Rechnung gestellt wird. Obwohl die Kosten für die Ausführung der VMs in dieser Demo gering sind, wird empfohlen, bei Abschluss dieses Kurses die Ressourcengruppe zu löschen, die die VM sowie zugehörige Ressourcen enthält.

1. Öffnen Sie in Ihrem Browser die Registerkarte „SC900-WinVM – Microsoft Azure“.

1. Wählen Sie in der oberen linken Ecke der Seite **Alle Dienste** aus.
1. Geben Sie in das Feld „Dienste filtern“ neben „Alle Dienste“ den Text **Ressourcengruppen** ein, und wählen Sie dann **Ressourcengruppen** aus den Ergebnissen aus.
1. Wählen Sie **LabsSC900-RG** aus.
1. Wählen Sie im oberen mittleren Bereich der LabsSC900-Seite die Option **Ressourcengruppe löschen** aus.
1. Geben Sie in das Fenster, das geöffnet wird, den Namen der Ressourcengruppe **LabsSC900** ein, um die Löschung der Ressourcengruppe und aller zugehöriger Ressourcen zu bestätigen. Wählen Sie dann unten auf der Seite **Löschen** aus.
1. Es kann ein paar Minuten dauern, bis alle Ressourcen und die Ressourcengruppe gelöscht sind.
1. Schließen Sie alle geöffneten Browserregisterkarten.

### <a name="review"></a>Überprüfung

In diesem Lab haben Sie den Prozess zur Einrichtung einer Netzwerksicherheitsgruppe (NSG) durchlaufen, die NSG der Netzwerkschnittstelle eines virtuellen Computers zugeordnet und dem NSG neue Regeln hinzugefügt, um eingehenden RDP-Datenverkehr zuzulassen und ausgehenden Internetdatenverkehr zu blockieren.
