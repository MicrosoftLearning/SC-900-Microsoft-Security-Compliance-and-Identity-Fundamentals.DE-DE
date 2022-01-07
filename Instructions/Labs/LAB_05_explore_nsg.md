---
lab:
    title: 'Erkunden von Azure-Netzwerksicherheitsgruppen (Network Security Groups, NSGs)'
    module: 'Modul 3, Lektion 1: Beschreiben der Funktionen der Microsoft-Sicherheitslösungen: Beschreiben der allgemeinen Sicherheitsfunktionen in Azure'
---


# Lab: Erkunden von Azure-Netzwerksicherheitsgruppen (Network Security Groups, NSGs)

## Labszenario
In diesem Lab erkunden Sie die Funktion von Netzwerksicherheitsgruppen in Azure.  Dazu erstellen Sie die VM ohne jegliche Netzwerksicherheitsgruppe (Network Security Group, NSG).  Ohne NSGs zum Filtern von Datenverkehr stehen alle Ports in der VM dem öffentlichen Internet ungeschützt offen.  Anschließend durchlaufen Sie den Prozess zum Erstellen einer NSG und zum Zuweisen der Schnittstelle der VM zu dieser NSG.  Nach der Konfiguration testen Sie mithilfe der standardmäßigen NSG-Regeln und auch der von Ihnen erstellten Regeln die Verbindung mit der VM.
  

**Geschätzte Dauer**: 15–20 Minuten

#### Aufgabe 1:  Bei dieser Aufgabe erstellen Sie einen virtuellen Computer unter Windows 10.    
1.	Öffnen Sie Microsoft Edge.  Geben Sie **portal.azure.com** in die Adressleiste ein.

1. Melden Sie sich mit Ihren Administratoranmeldeinformationen an.
    1. Geben Sie **admin@WWLxZZZZZZ.onmicrosoft.com** (ZZZZZZ ist hierbei die eindeutige Mandanten-ID, die von Ihrem Labhostinganbieter bereitgestellt wurde) in das Fenster „Anmelden“ ein, und wählen Sie dann **Weiter** aus.

    1. Geben Sie das Administratorkennwort ein, das Sie vom Labhostinganbieter erhalten haben sollten. Wählen Sie **Anmelden** aus.
    1. Wählen Sie **Ja** aus, wenn Sie gefragt werden, ob Sie angemeldet bleiben möchten.
1. Wählen Sie in der oberen linken Ecke des Bildschirms neben dem Text „Microsoft Azure“ das Symbol „Portalmenü anzeigen“ (die drei horizontalen Linien werden auch als Hamburgersymbol bezeichnet) und dann **Alle Dienste** aus.  
1. Wählen Sie im Hauptfenster unter „Empfohlen“ die Option „Virtuelle Computer“ aus.  Wenn „Virtuelle Computer“ nicht aufgelistet wird, geben Sie den entsprechenden Text in die Suchleiste ein, und treffen Sie dann die Auswahl aus den Suchergebnissen.
1. Wählen Sie oben links auf der Seite **+ Erstellen** und dann **+ Virtueller Computer** aus.
1. Tragen Sie auf der Registerkarte „Grundlagen“ die folgenden Informationen (übernehmen Sie für nicht aufgeführte Elemente die Standardeinstellungen) ein:
    1. Abonnement: Bestätigen Sie, dass die Standardeinstellung „Azure Pass-Förderung“ lautet.

    1. Ressourcengruppe:  Wählen Sie **Neue erstellen** aus. Geben Sie dann in das Feld „Name“ den Text **LabsSC900** ein, und wählen Sie dann **OK** aus.
    1. Name des virtuellen Computers:  Geben Sie **SC900-WinVM** ein.
    1. Image:  Wählen Sie im Dropdown **Windows 10 Pro, Version 20H2 – Gen 1** aus.
    1. Größe:  Wählen Sie im Dropdown **Alle Größen anzeigen** und dann **B2s** aus. Klicken Sie anschließend unten auf der Seite auf **Auswählen**.
    1. Benutzername:  Geben Sie **AzureUser** ein.
    1. Kennwort:  Geben Sie **SC900AzureLabs** ein.
    1. Öffentliche Inbound-Ports:  Wählen Sie **Keine** aus.
    1. Lizenzierung:  Wählen Sie **Ich bestätige, dass ich eine berechtigte Windows 10-Lizenz mit der Berechtigung zum Hosten mehrerer Mandanten besitze** aus, sodass im Feld ein Häkchen angezeigt wird.
    1. Wählen Sie **Weiter: Datenträger** aus. 
1. Sie befinden sich nun auf der Registerkarte „Datenträger“ für die VM-Konfiguration.  Übernehmen Sie alle Standardeinstellungen, und wählen Sie **Weiter: Netzwerk >** aus.
1. Sie befinden sich nun auf der Registerkarte „Netzwerk“ für die VM-Konfiguration.  Tragen Sie die folgenden Informationen (übernehmen Sie für nicht aufgeführte Elemente die Standardeinstellungen) ein:
    1. NIC-Netzwerksicherheitsgruppe:  Wählen Sie **Keine** aus.

    1. Wählen Sie **Weiter:  Verwaltung >** aus.
1. Sie befinden sich nun auf der Registerkarte „Verwaltung“ für die VM-Konfiguration.  Übernehmen Sie alle Standardeinstellungen, und wählen Sie **Weiter: Erweitert >** aus.
1. Sie befinden sich nun auf der Registerkarte „Erweitert“ für die VM-Konfiguration.  Übernehmen Sie alle Standardeinstellungen, und wählen Sie **Weiter: Tags >** aus.
1. Sie befinden sich nun auf der Registerkarte „Tags“ für die VM-Konfiguration.  Übernehmen Sie alle Standardeinstellungen, und wählen Sie **Weiter: Bewerten + erstellen >** aus.
1. Überprüfen Sie die Konfiguration für Ihre VM.  Hinweise: Diese VM verfügt über eine öffentliche IP-Adresse, weist aber keine NIC-Netzwerksicherheitsgruppe auf.  Aus Sicherheitsperspektive ist die VM ungeschützt.  Darum kümmern wir uns in einer nachfolgenden Aufgabe. Wählen Sie „Erstellen“ aus.  Der Abschluss der VM-Bereitstellung kann mehrere Minuten dauern.
1. Notieren Sie den Namen der Netzwerkschnittstelle **sc900-winvmXXX** (das XXX ist spezifisch für die Netzwerkschnittstelle Ihrer VM).
1. Wählen Sie nach Abschluss der VM-Bereitstellung die Option **Zu Ressource wechseln** aus.
1. Sie befinden sich nun auf der Seite „SC900-WinVM“.  Notieren Sie die öffentliche IP-Adresse. 
1. Wählen Sie oben auf der Seite **Verbinden** aus. Wählen Sie anschließend im Dropdown **RDP** aus.
1. Stellen Sie sicher, dass die IP-Adresse auf „Öffentliche IP-Adresse“ festgelegt ist, übernehmen Sie die Standardportnummer, und wählen Sie **RDP-Datei herunterladen** aus. 
1. Öffnen Sie die heruntergeladene-Datei, und wählen Sie **Verbinden** aus. 
1. Sie werden aufgefordert, Ihre Anmeldeinformationen einzugeben.  Geben Sie **AzureUser** als Benutzernamen ein.  Geben Sie **SC900AzureLabs** als Kennwort ein. 
1. Ein Remotedesktop-Verbindungsfenster wird geöffnet und gibt „Die Identität des Remotecomputers kann nicht überprüft werden.  Möchten Sie die Verbindung dennoch herstellen?“ an.  Wählen Sie **Ja** aus.
1. Sie sind nun mit Ihrer erstellten Windows-VM verbunden. Befolgen Sie die Aufforderungen, um die Windows-Einrichtung abzuschließen. Obwohl Sie die Verbindung mit der VM über RDP und einen allgemein genutzten RDP-Port hergestellt haben, sind bei dieser VM alle Ports geöffnet, wobei der Datenverkehr durch nichts gefiltert wird. 
1. Schließen Sie die Remotedesktopverbindung. Wählen Sie dazu oben zentral auf der Seite, wo die IP-Adresse angezeigt wird, das **X** aus.  Ein Popupfenster gibt „Die Remotesitzung wird getrennt“ an. Wählen Sie **OK** aus.
1. Sie befinden sich nun wieder im Azure-Portal auf der Seite „SC900-WinVM“.  Lassen Sie die Browserregisterkarte für die nächste Aufgabe geöffnet.

#### Aufgabe 2:  Erstellen Sie eine Netzwerksicherheitsgruppe, und weisen Sie dieser NSG die Netzwerkschnittstelle der VM zu.

1. Öffnen Sie in Ihrem Browser die Registerkarte „SC900-WinVM – Microsoft Azure“.

1. Wählen Sie in der oberen linken Ecke der Seite neben dem Text „Microsoft Azure“ das Symbol „Portalmenü anzeigen“ (die drei horizontalen Linien werden auch als Hamburgersymbol bezeichnet) und dann **Alle Dienste** aus.
1. Geben Sie in das Feld „Dienste filtern“ neben „Alle Dienste“ den Text **Netzwerksicherheitsgruppen** ein. Wählen Sie dann **Netzwerksicherheitsgruppen** (ohne „Netzwerksicherheitsgruppen – klassisch“ auszuwählen) aus den Ergebnissen aus.
1. Wählen Sie oben auf der Seite „Netzwerksicherheitsgruppen“ die Option **+ Erstellen** aus.
1. Geben Sie auf der Registerkarte „Grundlagen“ der Seite „Netzwerksicherheitsgruppe erstellen“ die folgenden Einstellungen an:
    1. Abonnement:  Azure Pass-Förderung

    1. Ressourcengruppe:  **LabsSC900**
    1. Name:  **NSG-SC900**
    1. Region:  Übernehmen Sie den Standardwert **(US) East US**.
    1. Wählen Sie **Bewerten + erstellen** und dann **Erstellen** aus.
1. Klicken Sie nach Abschluss der Bereitstellung auf **Zu Ressource wechseln**.
1. Beachten Sie die standardmäßigen Eingangs- und Ausgangsregeln in der NSG.  Obwohl die NSG erstellt wurde und keine Standardregeln zum Filtern des Datenverkehrs vorhanden sind, wurde der NSG keine Schnittstelle zugeordnet. Entsprechend ist die VM weiterhin anfällig, da alle zugehörigen Ports für das öffentliche Internet zugänglich sind.
1. Wählen Sie auf der Seite „NSG-SC900“ im linken Navigationsbereich unter „Einstellungen“ die Option **Netzwerkschnittstellen** aus.
1. Wählen Sie oberhalb des Suchfelds die Option **+ Zuordnen** aus.
1. Wählen Sie **sc900-winvmXXX** (das XXX ist spezifisch für die Netzwerkschnittstelle Ihrer VM) auf der Seite „Netzwerkschnittstelle zuordnen“ aus.  Während die Schnittstelle zugeordnet wird, wird in der oberen rechten Ecke des Bildschirms ein Benachrichtigungsfeld angezeigt.
1. Sobald der NSG die Schnittstelle zugeordnet ist, wird sie in der Liste angezeigt.
1. Wenn die Schnittstelle der VMs der Netzwerksicherheitsgruppe und den NSG-Standardregeln zugeordnet ist, ist es nicht möglich, eine Verbindung mit der VM herzustellen.  
1. Wählen Sie in der oberen linken Ecke der Seite **Alle Dienste** aus. Wählen Sie dann unter „Empfohlen“ die Option **Virtuelle Computer** aus.
1. Wählen Sie **SC900-WinVM** auf der Seite „Virtuelle Computer“ aus.
1. Wählen Sie oben auf der Seite **SC900-WinVM** die Option **Verbinden** und dann **RDP** aus.
1. Stellen Sie sicher, dass die IP-Adresse auf „Öffentliche IP-Adresse“ festgelegt ist, übernehmen Sie die Standardportnummer, und wählen Sie **RDP-Datei herunterladen** aus.
1. Öffnen Sie die heruntergeladene-Datei, und wählen Sie **Verbinden** aus.
1. Nachdem ein paar Sekunden lang versucht wurde, eine Verbindung herzustellen, wird in der Fehlermeldung angezeigt, dass der Remotedesktop keine Verbindung mit dem Remotecomputer herstellen kann.  Wählen Sie **OK** aus.

#### Aufgabe 3: Bei dieser Aufgabe erstellen Sie eine NSG-Regel, um eingehenden Datenverkehr über das RDP an Port 3389 zuzulassen.  Anschließend testen Sie diese Regel, indem Sie versuchen, über das RDP eine Verbindung mit der VM herzustellen. 

1. Öffnen Sie in Ihrem Browser die Registerkarte „SC900-WinVM – Microsoft Azure“.

1. Wählen Sie im linken Navigationsbereich unter „Einstellungen“ die Option **Netzwerk** aus.
1. Auf der ausgewählten Registerkarte „Regeln für eingehende Ports“ sehen Sie die Standardeingangsregeln. Sie können die Standardregeln nicht entfernen, aber Sie können sie außer Kraft setzen, indem Sie Regeln mit höheren Prioritäten erstellen. Wählen Sie rechts auf der Seite **Regel für eingehenden Port hinzufügen** aus:
1. Geben Sie auf der Seite „Eingangssicherheitsregel hinzufügen“ die folgenden Einstellungen an:
    1. Quelle:  **Any**

    1. Quellportbereiche: *
    1. Ziel:  **Any**
    1. Kundendienst:  **RDP**
    1. Aktion:  **Zulassen**
    1. Priorität:  **300**; Hinweis: Regeln mit niedrigeren Zahlen haben eine höhere Priorität und werden zuerst verarbeitet.
    1. Name:  **AllowRDP**
1. Wählen Sie **Hinzufügen** aus.
1. Nach der Bereitstellung der Regel wird sie in der Liste der Eingangsregeln angezeigt.
1. Stellen Sie nun sicher, dass Sie über das RDP eine Verbindung mit der VM herstellen können.  Wählen Sie im linken Navigationsbereich **Verbinden** aus.
1. Stellen Sie sicher, dass die IP-Adresse auf „Öffentliche IP-Adresse“ festgelegt ist, übernehmen Sie die Standardportnummer, und wählen Sie **RDP-Datei herunterladen** aus.
1. Öffnen Sie die heruntergeladene-Datei, und wählen Sie **Verbinden** aus.
1. Sie werden aufgefordert, Ihre Anmeldeinformationen einzugeben.  Geben Sie **AzureUser** als Benutzernamen ein.  Geben Sie **SC900AzureLabs** als Kennwort ein.
1. Ein Remotedesktop-Verbindungsfenster wird geöffnet und gibt „Die Identität des Remotecomputers kann nicht überprüft werden.  Möchten Sie die Verbindung dennoch herstellen?“ an.  Wählen Sie **Ja** aus.
1. Sie sind nun mit der VM verbunden. In diesem Fall konnten Sie eine Verbindung mit der VM herstellen, da die von Ihnen erstellte Regel für eingehenden Datenverkehr eingehenden Datenverkehr zur VM über das RDP zulässt.
1. Lassen Sie die VM geöffnet. Sie verwenden sie bei der nächsten Aufgabe.

#### Aufgabe 4:  Die Standardausgangsregeln für NSG lassen ausgehenden Internetdatenverkehr zu. Daher überprüfen Sie, ob Sie eine Verbindung mit dem Internet herstellen können.  Anschließend durchlaufen Sie den Prozess zum Erstellen einer benutzerdefinierten Ausgangsregel, um ausgehenden Internetdatenverkehr zu blockieren und diese Regel zu testen.

1. Wählen Sie in der VM **Edge** aus, um den Browser zu öffnen.  
1. Geben Sie **https://www.bing.com** in die Adressleiste des Browsers ein, und bestätigen Sie, dass Sie eine Verbindung mit der Suchmaschine herstellen können.
1. Schließen Sie auf Ihrer VM den Browser. Lassen Sie die VM jedoch geöffnet, da Sie sie in den nachfolgenden Schritten verwenden.
1. Kehren Sie zum Azure-Portal zurück, und öffnen Sie im Browser die Registerkarte „SC900-WinVM – Microsoft Azure“.
1. Wählen Sie im linken Navigationsbereich unter „Einstellungen“ die Option **Netzwerk** aus.
1. Wählen Sie die Registerkarte **Regeln für ausgehende Ports** aus.  Die Standardausgangsregeln werden angezeigt.  Beachten Sie die Standardregel „AllowInternetOutBound“. Diese Regel lässt sämtlichen ausgehenden Internetdatenverkehr zu. Sie können die Standardregel nicht entfernen. Sie können sie jedoch überschreiben, indem Sie eine Regel mit höherer Priorität erstellen. Wählen Sie rechts auf der Seite **Regel für ausgehenden Port hinzufügen** aus:
1. Geben Sie auf der Seite „Ausgangssicherheitsregel hinzufügen“ die folgenden Einstellungen an:
    1. Quelle:  **Any**

    1. Quellportbereiche:  *
    1. Ziel:  **Diensttag**
    1. Zieldiensttag:  **Internet**
    1. Kundendienst:  **Benutzerdefiniert** (übernehmen Sie den Standardwert)
    1. Zielportbereiche:  * (setzen Sie ein Sternchen in das Feld „Zielportbereiche“).
    1. Protokoll: **Any**
    1. Aktion: **Verweigern**
    1. Priorität:  **4000**
    1. Name:  **DenyInternet**
1. Wählen Sie **Hinzufügen** aus.
1. Nach der Bereitstellung der Regel wird sie in der Liste der Ausgangsregeln angezeigt.  Obwohl sie in der Liste angezeigt wird, dauert es ein paar Minuten, bis sie wirksam wird (warten Sie ein paar Minuten, bevor Sie mit den nächsten Schritten fortfahren).  
1. Wechseln Sie zurück zu Ihrer VM zurück.
1. Öffnen Sie in Ihrer VM den Edge-Browser, und geben Sie **https://www.bing.com** ein.  Die Seite sollte nicht angezeigt werden.  Hinweis: Wenn Sie eine Verbindung mit dem Internet herstellen können und sichergestellt haben, dass alle Parameter für die Ausgangsregel ordnungsgemäß festgelegt wurden, liegt dies wahrscheinlich daran, dass es ein paar Minuten dauern kann, bis die Regel wirksam wird.  Schließen Sie den Browser, warten Sie ein paar Minuten, und versuchen Sie es erneut.
1. Schließen Sie die Remotedesktopverbindung. Wählen Sie dazu oben zentral auf der Seite, wo die IP-Adresse angezeigt wird, das **X** aus.  Ein Popupfenster gibt „Die Remotesitzung wird getrennt“ an. Wählen Sie **OK** aus.
1. Bei dieser Aufgabe haben Sie erfolgreich eine Ausgangsregel in Ihrer NSG konfiguriert, um ausgehenden Internetdatenverkehr zu blockieren.

#### Aufgabe 5:  WICHTIG: Bei dieser Aufgabe löschen Sie die Ressourcengruppe und alle darin enthaltenen Ressourcen.   Dies ist wichtig, um zusätzliche Gebühren zu vermeiden.

1. Öffnen Sie in Ihrem Browser die Registerkarte „SC900-WinVM – Microsoft Azure“.

1. Wählen Sie in der oberen linken Ecke der Seite **Alle Dienste** aus.
1. Geben Sie in das Feld „Dienste filtern“ neben „Alle Dienste“ den Text **Ressourcengruppen** ein, und wählen Sie dann **Ressourcengruppen** aus den Ergebnissen aus.
1. Wählen Sie **LabsSC900** aus.
1. Wählen Sie im oberen mittleren Bereich der LabsSC900-Seite die Option **Ressourcengruppe löschen** aus.
1. Geben Sie in das Fenster, das geöffnet wird, den Namen der Ressourcengruppe **LabsSC900** ein, um die Löschung der Ressourcengruppe und aller zugehöriger Ressourcen zu bestätigen. Wählen Sie dann unten auf der Seite **Löschen** aus.
1. Es kann ein paar Minuten dauern, bis alle Ressourcen und die Ressourcengruppe gelöscht sind.

#### Überprüfung

In diesem Lab sind Sie den Prozess zum Einstellen einer VM mit und ohne Netzwerksicherheitsgruppe (NSG) durchgegangen und haben die Auswirkung von NSG-Standardregeln gesehen.  Außerdem sind Sie den Prozess zum Erstellen einer NSG-Regel durchgegangen.
