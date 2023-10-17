<!---
---
Lab: Title: 'Erkunden von Azure-Netzwerksicherheitsgruppen (Network Security Groups, NSGs)' Learning Path/Module/Unit: 'Lernpfad: Beschreiben der Funktionen von Microsoft-Sicherheitslösungen; Modul 1: Beschreiben der grundlegenden Sicherheitsfunktionen in Azure; Lerneinheit 6: Beschreiben von Azure-Netzwerksicherheitsgruppen'
---
--->

# Lab: Erkunden von Azure-Netzwerksicherheitsgruppen (Network Security Groups, NSGs)

Dieses Lab ist den folgenden Learn-Inhalten zugeordnet:

- Lernpfad: Beschreiben der Funktionen von Microsoft-Sicherheitslösungen
- Modul: Beschreiben der grundlegenden Sicherheitsfunktionen in Azure
- Lerneinheit: Beschreiben von Azure-Netzwerksicherheitsgruppen

## Labszenario

In diesem Lab erkunden Sie die Funktion von Netzwerksicherheitsgruppen in Azure.  Dazu erstellen Sie eine Netzwerksicherheitsgruppe (NSG) und weisen die NSG der Schnittstelle einer bereits vorhandenen VM zu.  Nach der Konfiguration werden Sie die Standardeingangs- und -ausgangsregeln beobachten, neue Regeln erstellen und diese Regeln testen.  In diesem Lab wird die VM, die Sie mit der NSG verwenden, für Sie erstellt, sodass Sie zunächst einige der Informationen anzeigen, die dieser VM zugeordnet sind.
  
**Geschätzte Dauer**: 30-45 Minuten

### Aufgabe 1

In dieser Aufgabe zeigen Sie einige der Parameter an, die der VM zugeordnet sind, die für die Verwendung mit diesem Lab erstellt wurde.

1. Öffnen Sie Microsoft Edge.  Geben Sie in der Adressleiste **https://portal.azure.com** ein.

1. Melden Sie sich mit Ihren Administratoranmeldeinformationen an.
    1. Geben Sie im Anmeldefenster den Benutzernamen ein, der von Ihrem Lab-Hostingnbieter bereitgestellt wird, und wählen Sie dann **Weiter** aus.
    1. Geben Sie das Administratorkennwort ein, das von Ihrem Lab-Hostinganbieter bereitgestellt werden sollte. Wählen Sie **Anmelden**.
    1. Wählen Sie **Ja** aus, wenn Sie gefragt werden, ob Sie angemeldet bleiben möchten.

1. Wählen Sie oben auf der Seite unterhalb von „Azure-Dienste“ die Option **Virtual Machines** aus.  Wenn diese Option nicht aufgeführt wird, geben Sie in das Suchfeld, das sich auf dem blauen Balken oben auf der Seite neben dem Text „Microsoft Azure“ befindet, den Text **Virtual Machines** ein, und wählen Sie dann **Virtual Machines** aus den Suchergebnissen aus.

1. Wählen Sie **SC900-WinVM** auf der Seite „Virtuelle Computer“ aus.

1. Sie befinden sich nun auf der Seite „SC900-WinVM“.  Beachten Sie einige der grundlegenden Informationen zur VM.

1. Wählen Sie oben auf der Seite **Verbinden** aus.  Wählen Sie die Option **Zugriff überprüfen** aus, die unter der IP-Adresse aufgeführt ist.  Diese Überprüfung erfolgt mithilfe von Port 3389, dem Port für die RDP-Konnektivität.  Die Meldung „Kann nicht überprüft werden“ sollte angezeigt werden.  Klicken Sie im nativen RDP-Feld auf **Auswählen**.  Im sich daraufhin öffnenden Fenster sollte unter "1 Voraussetzungen für das Konfigurieren von nativem RDP" die Meldung „Azure muss einige Features konfigurieren, um eine Verbindung mit der VM herzustellen“ angezeigt werden.  In der nächsten Aufgabe richten Sie eine NSG ein, um die RDP-Verbindung explizit zuzulassen.


1. Wählen Sie im linken Navigationsbereich **Netzwerk** aus.  
    1. Die Standardansicht gilt für Regeln für eingehende Ports.  Beachten Sie, dass für die Netzwerkschnittstelle für diese VM keine Netzwerksicherheitsgruppen konfiguriert sind.  Das gleiche gilt, wenn Sie Regeln für ausgehende Ports auswählen.
    1. Wählen Sie neben „Netzwerkschnittstelle“ die Option **Effektive Sicherheitsregeln** aus.  Beachten Sie die Angabe „Der Netzwerkschnittstelle sind keine Netzwerksicherheitsgruppen oder Anwendungssicherheitsgruppen zugeordnet“.

1. Lassen Sie diese Browserregisterkarte geöffnet.


### Aufgabe 2

In diesem Teil erstellen Sie eine Netzwerksicherheitsgruppe, weisen die Netzwerkschnittstelle der VM dieser NSG zu und erstellen eine neue Regel für eingehenden RDP-Datenverkehr.

1. Klicken Sie auf der geöffneten NSG-Registerkarte mit der rechten Maustaste oben auf der Seite auf den Link *Startsteite*, und wählen Sie **Link in neuer Registerkarte öffnen** aus, um eine weitere Seite für **Azure-Dienste** zu öffnen.

1. Geben Sie in der blauen Suchleiste oben auf der Seite **Netzwerksicherheitsgruppen** ein. Wählen Sie aus den Ergebnissen **Netzwerksicherheitsgruppen** aus. Wählen Sie nicht *Netzwerksicherheitsgruppen (klassisch)* aus.

1. Wählen Sie oben auf der Seite „Netzwerksicherheitsgruppen“ die Option **+ Erstellen** aus.

1. Geben Sie auf der Registerkarte „Grundlagen“ der Seite „Netzwerksicherheitsgruppe erstellen“ die folgenden Einstellungen an:
    1. Abonnement: Behalten Sie den Standardwert bei (dies ist das Azure-Abonnement, das vom autorisierten Lab-Hoster bereitgestellt wird).
    1. Ressourcengruppe:  **LabsSC900**
    1. Name:  **NSG-SC900**
    1. Region: Übernehmen Sie den Standardwert.
    1. Wählen Sie **Bewerten + erstellen** und dann **Erstellen** aus.

1. Klicken Sie nach Abschluss der Bereitstellung auf **Zu Ressource wechseln**.

1. Oben auf der darunterliegenden Seite unter „Zusammenfassung“ werden einige grundlegende Informationen zur von Ihnen erstellten NSG angezeigt.  Zwei Punkte sind zu beachten: Es gibt keine benutzerdefinierten Sicherheitsregeln und keine Subnetze oder Netzwerkschnittstellen, die dieser NSG zugeordnet sind.  Obwohl es keine benutzerdefinierten Sicherheitsregeln gibt, gibt es Standardregeln für eingehenden und ausgehenden Datenverkehr, die in jeder NSG enthalten sind, wie auf der Seite gezeigt.  Überprüfen Sie die Eingangs- und Ausgangsregeln. Die Standardregeln für eingehenden Datenverkehr verweigern den gesamten eingehenden Datenverkehr, der nicht aus einem virtuellen Netzwerk oder einem Azure-Lastenausgleich stammt.  Die Ausgangsregeln verweigern den gesamten ausgehenden Datenverkehr mit Ausnahme des Datenverkehrs zwischen virtuellen Netzwerken und des ausgehenden Datenverkehrs in das Internet.

1. Wählen Sie auf der Seite „NSG-SC900“ im linken Navigationsbereich unter „Einstellungen“ die Option **Netzwerkschnittstellen** aus.
    1. Wählen Sie **Zuordnen** aus.
    2. Wählen Sie im Feld für Netzwerkschnittstellenzuordnungen den **Abwärtspfeil**, dann **sc900-winvmXXX** und schließlich unten im Fenster **OK** aus. Sobald der NSG die Schnittstelle zugeordnet ist, wird sie in der Liste angezeigt.

1. Wählen Sie im linken Navigationsbereich **Eingehende Sicherheitsregeln** aus.

1. Die Standardregeln für eingehenden Datenverkehr verweigern den gesamten eingehenden Datenverkehr, der nicht von einem VNet oder einem Azure-Lastenausgleich stammt, sodass Sie eine Regel einrichten müssen, um eingehenden RDP-Datenverkehr (Datenverkehr an Port 3389) zuzulassen. Erinnern Sie sich, dass Sie die Standardregeln nicht entfernen, aber außer Kraft setzen können, indem Sie Regeln mit höheren Prioritäten erstellen.

1. Wählen Sie oben auf der Seite die Option **Hinzufügen** aus. Geben Sie auf der Seite „Eingehende Sicherheitsregel hinzufügen“ die folgenden Einstellungen an:
    1. Quelle:  **Alle**
    1. Quellportbereiche: **\***
    1. Ziel:  **Alle**
    1. Dienst:  **RDP**
    1. Aktion:  **Zulassen**
    1. Priorität: **1.000**. Regeln mit niedrigeren Zahlen besitzen höhere Priorität und werden zuerst verarbeitet.
    1. Name: Behalten Sie den Standardnamen bei, oder erstellen Sie Ihren eigenen beschreibenden Namen.
    1. Beachten Sie das Warnzeichen am unteren Rand der Seite.  Wir verwenden RDP nur zu Testzwecken und zur Veranschaulichung der Funktionalität der NSG.
    1. Wählen Sie **Hinzufügen** aus.

1. Sobald die Regel bereitgestellt wurde, wird sie in der Liste der eingehenden Regeln angezeigt (Möglicherweise müssen Sie den Bildschirm aktualisieren).

1. Lassen Sie diese Browserregisterkarte geöffnet.  

### Aufgabe 3

In dieser Aufgabe testen Sie die neu erstellte NSG-Eingangsregel, um sicherzustellen, dass Sie eine RDP-Verbindung (Remotedesktop) mit der VM herstellen können.  Sobald Sie die VM nutzen, überprüfen Sie die ausgehende Konnektivität mit dem Internet von der VM aus.

1. Öffnen Sie in Ihrem Browser die Registerkarte „SC900-WinVM – Microsoft Azure“. Wenn Sie die Browserregisterkarte zuvor geschlossen haben, öffnen Sie eine neue Browserregisterkarte, geben Sie **https://portal.azure.com** ein, und wählen Sie **VMs** aus. Wählen Sie dann den die VM **SC900-WinVM** aus.

1. Wählen Sie im linken Navigationsbereich **Verbinden** aus.

1. Wählen Sie **Zugriff überprüfen** aus. (Überprüfen Sie, ob der Port auf 3389 festgelegt ist.)  Der Status sollte als „Zugänglich“ angezeigt werden.

1. Stellen Sie nun eine direkte Verbindung mit der VM her, indem Sie im Feld „Native RDP“ auf **Auswählen** klicken.
   
    1. Wählen Sie im sich daraufhin öffnenden „Native RDP„-Fenster die Option **RDP-Datei herunterladen** aus.
    1. Wenn eine Downloadwarnung angezeigt wird, wählen Sie **Beibehalten** und dann im angezeigten Popupfenster **Datei öffnen** aus.
    1. Ein Fenster für die Remotedesktopverbindung wird geöffnet. Wählen Sie **Verbinden** aus.
    1. Anschließend werden Sie zur Eingabe Ihrer Anmeldeinformationen aufgefordert.  Geben Sie den Benutzernamen und das Kennwort für die VM ein (siehe Registerkarte „Ressourcen“ im Lab-Anweisungsbereich).
    1. Ein Fenster für die Remotedesktopverbindung wird geöffnet und meldet: *Die Identität des Remotecomputers kann nicht überprüft werden. Möchten Sie trotzdem eine Verbindung herstellen?*  Wählen Sie **Ja** aus.

1. Sie sind nun mit der VM verbunden. In diesem Fall konnten Sie eine Verbindung mit der VM herstellen, da die von Ihnen erstellte Regel für eingehenden Datenverkehr eingehenden Datenverkehr zur VM über das RDP zulässt.  Nach einigen Sekunden wird auf dem Willkommensbildschirm möglicherweise ein Fenster angezeigt, in dem Sie Datenschutzeinstellungen für Ihr Gerät auswählen können. Wählen Sie **Akzeptieren** aus.  Wenn das Fenster „Netzwerke“ angezeigt wird, wählen Sie **Nein** aus.

1. Testen Sie die ausgehende Konnektivität mit dem Internet über die in der RDP-Sitzung ausgeführten VM.
    1. Wählen Sie in der geöffneten VM **Microsoft Edge** aus, um den Browser zu öffnen.  Da Sie Microsoft Edge zum ersten Mal öffnen, wird möglicherweise ein Popupfenster angezeigt. Wählen Sie **Ohne Ihre Daten starten**, **Weiter ohne diese Daten** und dann **Bestätigen und Browsing starten** aus.
    1. Geben Sie **www.bing.com** in die Adressleiste des Browsers ein, und bestätigen Sie, dass Sie eine Verbindung mit der Suchmaschine herstellen können.
    1. Nachdem Sie bestätigt haben, dass Sie auf www.bing.com zugreifen können, schließen Sie das Browserfenster auf der VM, lassen Sie die VM jedoch aktiviert.

1. Minimieren Sie die VM, indem Sie den Unterstrich **_** auf der blauen Registerkarte auswählen, die die IP-Adresse der VM anzeigt. Sie gelangen so zurück zur Seite „SC900-WinVM \| Verbinden“.

1. Lassen Sie die Browserregisterkarte geöffnet, Sie verwenden sie in der nächsten Aufgabe.

### Aufgabe 4

In der vorherigen Aufgabe haben Sie bestätigt, dass Sie eine RDP-Verbindung mit der VM herstellen können. Sobald Sie mit der Verwendung der VM begonnen haben, haben Sie auch bestätigt, dass Sie eine ausgehende Verbindung mit dem Internet herstellen können.  Der ausgehende Internetdatenverkehr wurde zugelassen, weil die Standardausgangsregeln für die NSG ausgehenden Internetdatenverkehr zulassen.  In dieser Aufgabe durchlaufen Sie den Prozess zum Erstellen einer benutzerdefinierten Ausgangsregel, um ausgehenden Internetdatenverkehr zu blockieren und diese Regel zu testen.

1. Sie sollten sich auf der Seite „SC900-WinVM \| Verbinden“ befinden. Wählen Sie im linken Navigationsbereich **Netzwerk** aus. Wenn Sie die Browserregisterkarte zuvor geschlossen haben, wählen Sie oben auf der Seite die blaue Suchleiste aus, und wählen Sie „Virtuelle Computer“ und dann die VM **SC900-WinVM** aus. Wählen Sie anschließend **Netzwerk** aus.

1. Wählen Sie die Registerkarte **Regeln für ausgehende Ports** aus. Die Standardausgangsregeln werden angezeigt.  Beachten Sie die Standardregel „AllowInternetOutBound“. Diese Regel lässt sämtlichen ausgehenden Internetdatenverkehr zu. Sie können die Standardregel nicht entfernen. Sie können sie jedoch überschreiben, indem Sie eine Regel mit höherer Priorität erstellen. Wählen Sie rechts auf der Seite **Regel für ausgehenden Port hinzufügen** aus:

1. Geben Sie auf der Seite „Ausgangssicherheitsregel hinzufügen“ die folgenden Einstellungen an:
    1. Quelle:  **Alle**
    1. Quellportbereiche: **\***
    1. Ziel:  **Diensttag**
    1. Zieldiensttag:  **Internet**
    1. Dienst:  **Benutzerdefiniert** (übernehmen Sie den Standardwert)
    1. Zielportbereiche: **\*** (Sternchen im Feld für Zielportbereiche eingeben)
    1. Protokoll: **Alle**
    1. Aktion: **Deny**
    1. Priorität: **1.000**
    1. Name: Behalten Sie den Standardnamen bei, oder erstellen Sie Ihren eigenen beschreibenden Namen.
    1. Wählen Sie **Hinzufügen** aus.

1. Nach der Bereitstellung der Regel wird sie in der Liste der Ausgangsregeln angezeigt.  Obwohl sie in der Liste angezeigt wird, dauert es ein paar Minuten, bis sie wirksam wird (warten Sie ein paar Minuten, bevor Sie mit den nächsten Schritten fortfahren).  


1. Kehren Sie zu Ihrer VM zurück (das RDP-Symbol für die VM sollte auf der Taskleiste unten auf der Seite angezeigt werden).

1. Öffnen Sie auf Ihrer VM den Microsoft Edge-Browser, und geben Sie **www.bing.com** ein. Die Seite sollte nicht angezeigt werden. Wenn Sie eine Verbindung mit dem Internet herstellen können und sichergestellt haben, dass alle Parameter für die Ausgangsregel ordnungsgemäß festgelegt wurden, liegt dies wahrscheinlich daran, dass es einige Minuten dauern kann, bis die Regel wirksam wird.  Schließen Sie den Browser, warten Sie ein paar Minuten, und versuchen Sie es erneut. Für Azure-Abonnements in der Lab-Umgebung können Verzögerungen auftreten,die länger als normal sind.


1. Schließen Sie die Remotedesktopverbindung. Wählen Sie dazu oben zentral auf der Seite, wo die IP-Adresse angezeigt wird, das **X** aus.  Ein Popupfenster wird anzeigt, das „Die Remotesitzung wird getrennt“ angibt. Klicken Sie auf **OK**.

1. Wählen Sie in der oberen linken Ecke des Fensters direkt unterhalb der blauen Leiste, wo “Microsoft Azure” angezeigt wird, die Option **Startseite** aus, um zur Startseite des Azure-Portals zurückzukehren.

1. Lassen Sie die Azure-Registerkarte in Ihrem Browser geöffnet.

### Überprüfung

In diesem Lab haben Sie den Prozess zur Einrichtung einer Netzwerksicherheitsgruppe (NSG) durchlaufen, die NSG der Netzwerkschnittstelle einer VM zugeordnet und der NSG neue Regeln hinzugefügt, um eingehenden RDP-Datenverkehr zuzulassen und ausgehenden Internetdatenverkehr zu blockieren.
