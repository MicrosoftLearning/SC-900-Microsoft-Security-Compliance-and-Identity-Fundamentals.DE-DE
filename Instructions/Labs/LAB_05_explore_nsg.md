<!---
---
Lab: Title: 'Erkunden von Azure-Netzwerksicherheitsgruppen (Network Security Groups, NSGs)' Learning Path/Module/Unit: 'Lernpfad: Beschreiben der Funktionen von Microsoft-Sicherheitslösungen; Modul 1: Beschreiben der grundlegenden Sicherheitsfunktionen in Azure; Lerneinheit 6: Beschreiben von Azure-Netzwerksicherheitsgruppen'
---
--->

# Lab: Erkunden von Azure-Netzwerksicherheitsgruppen (NSGs)

Dieses Lab ist den folgenden Learn-Inhalten zugeordnet:

- Lernpfad: Beschreiben der Funktionen von Microsoft-Sicherheitslösungen
- Modul: Beschreiben der grundlegenden Sicherheitsfunktionen in Azure
- Lerneinheit: Beschreiben von Azure-Netzwerksicherheitsgruppen

## Labszenario

In diesem Lab erkunden Sie die Funktion von Netzwerksicherheitsgruppen in Azure.  Dazu erstellen Sie eine Netzwerksicherheitsgruppe (NSG) und weisen die NSG der Schnittstelle einer bereits vorhandenen VM zu.  Nach der Konfiguration werden Sie die Standardeingangs- und -ausgangsregeln beobachten, neue Regeln erstellen und diese Regeln testen.  In diesem Lab wird die VM, die Sie mit der NSG verwenden, für Sie erstellt, sodass Sie zunächst einige der Informationen anzeigen, die dieser VM zugeordnet sind.
  
**Geschätzte Dauer**: 30 bis 45 Minuten

### Aufgabe 1

In dieser Aufgabe zeigen Sie einige der Parameter an, die der VM zugeordnet sind, die für die Verwendung mit diesem Lab erstellt wurde.

1. Öffnen Sie Microsoft Edge.  Geben Sie in der Adressleiste **https://portal.azure.com** ein.

1. Melden Sie sich mit Ihren Administratoranmeldeinformationen an.
    1. Geben Sie im Anmeldefenster den Benutzernamen ein, der von Ihrem Lab-Hostingnbieter bereitgestellt wird, und wählen Sie dann **Weiter** aus.
    1. Geben Sie das Administratorkennwort ein, das von Ihrem Lab-Hostinganbieter bereitgestellt werden sollte. Wählen Sie **Anmelden**.
    1. Wählen Sie **Ja** aus, wenn Sie gefragt werden, ob Sie angemeldet bleiben möchten.

1. Wählen Sie oben auf der Seite unterhalb von „Azure-Dienste“ die Option **Virtual Machines** aus.  Wenn diese Option nicht aufgeführt wird, geben Sie in das Suchfeld, das sich auf dem blauen Balken oben auf der Seite neben dem Text „Microsoft Azure“ befindet, den Text **Virtual Machines** ein, und wählen Sie dann **Virtual Machines** aus den Suchergebnissen aus.

1. Wählen Sie **SC900-WinVM** auf der Seite „Virtuelle Computer“ aus.

1. Sie befinden sich nun auf der Seite „SC900-WinVM“.  Beachten Sie einige der grundlegenden Informationen zur VM.

1. Wählen Sie im linken Navigationsbereich **Netzwerkeinstellungen** aus.  In den Abschnitten „Grundlagen“ des Hauptfensters wird die Netzwerkschnittstelle für die VM angezeigt.  Beachten Sie, dass neben der Netzwerksicherheitsgruppe nichts aufgeführt ist, da der Schnittstelle keine NSG zugewiesen ist.

1. Lassen Sie diese Registerkarte geöffnet.

### Aufgabe 2

In diesem Teil erstellen Sie eine Netzwerksicherheitsgruppe, weisen die Netzwerkschnittstelle der VM dieser NSG zu und erstellen eine neue Regel für eingehenden RDP-Datenverkehr.

1. Klicken Sie auf der geöffneten Azure-Registerkarte mit der rechten Maustaste oben auf der Seite auf den Link *Startseite*, und wählen Sie **Link in neuer Registerkarte öffnen** aus, um eine weitere Seite für **Azure-Dienste** zu öffnen.

1. Geben Sie in der blauen Suchleiste oben auf der Seite **Netzwerksicherheitsgruppen** ein. Wählen Sie aus den Ergebnissen **Netzwerksicherheitsgruppen** aus. Wählen Sie nicht *Netzwerksicherheitsgruppen (klassisch)* aus.

1. Wählen Sie in der Mitte der Seite die blaue Schaltfläche mit der Bezeichnung **Netzwerksicherheitsgruppe erstellen** aus.  Alternativ können Sie auf der Seite „Netzwerksicherheitsgruppen“ auch **+ Erstellen** auswählen.

1. Geben Sie auf der Registerkarte „Allgemein“ der Seite „Netzwerksicherheitsgruppe erstellen“ die folgenden Einstellungen an:
    1. Abonnement: Behalten Sie den Standardwert bei (dies ist das Azure-Abonnement, das vom autorisierten Lab-Hoster bereitgestellt wird).
    1. Ressourcengruppe:  **LabsSC900**
    1. Name:  **NSG-SC900**
    1. Region: Übernehmen Sie den Standardwert.
    1. Klicken Sie auf **Überprüfen + erstellen** und dann auf **Erstellen**.

1. Klicken Sie nach Abschluss der Bereitstellung auf **Zu Ressource wechseln**.

1. Die Übersichtsseite für die neu erstellte NSG sollte angezeigt werden.  Wählen Sie andernfalls im linken Navigationsbereich die Option **Übersicht** aus. Oben auf der darunterliegenden Seite unter „Zusammenfassung“ werden einige grundlegende Informationen zur von Ihnen erstellten NSG angezeigt.  Zwei Punkte sind zu beachten: Es gibt keine benutzerdefinierten Sicherheitsregeln und keine Subnetze oder Netzwerkschnittstellen, die dieser NSG zugeordnet sind.  Obwohl es keine benutzerdefinierten Sicherheitsregeln gibt, gibt es Standardregeln für eingehenden und ausgehenden Datenverkehr, die in jeder NSG enthalten sind, wie auf der Seite gezeigt.  Überprüfen Sie die Eingangs- und Ausgangsregeln. Die Standardregeln für eingehenden Datenverkehr verweigern den gesamten eingehenden Datenverkehr, der nicht aus einem virtuellen Netzwerk oder einem Azure-Lastenausgleich stammt.  Die Ausgangsregeln verweigern den gesamten ausgehenden Datenverkehr mit Ausnahme des Datenverkehrs zwischen virtuellen Netzwerken und des ausgehenden Datenverkehrs in das Internet.

1. Wählen Sie im linken Navigationsbereich auf der Seite „NSG-SC900“ unter „Einstellungen“ die Option **Netzwerkschnittstellen** aus.
    1. Wählen Sie **Zuordnen** aus.
    2. Wählen Sie im Feld für Netzwerkschnittstellenzuordnungen den **Abwärtspfeil**, dann **sc900-winvmXXX** und schließlich unten im Fenster **OK** aus. Sobald die Schnittstelle dem NSG zugeordnet ist, wird sie in der Liste angezeigt.  Die NSG wird jetzt der Netzwerkschnittstelle Ihrer VM zugewiesen.

1. Navigieren Sie im Browser zurück zur Registerkarte **SC900-WinWM – Microsoft Azure**.  Aktualisieren Sie die Seite. Neben „Netzwerksicherheitsgruppe“ sollte nun der Name der NSG angezeigt werden, die Sie gerade erstellt haben.  Wenn sie immer noch nicht angezeigt wird, warten Sie eine weitere Minute, und aktualisieren Sie die Seite dann erneut.

1. Wählen Sie im linken Navigationsbereich **Verbinden** aus. Wählen Sie im Hauptfenster neben der Portnummer 3389 die Option **Zugriff überprüfen** aus. Die Zugriffsüberprüfungsfunktion sendet Signale (Datenverkehr) an den standardmäßigen RDP-Port 3389 der VM, um zu überprüfen, ob darauf zugegriffen werden kann. Es kann eine Minute dauern, aber dann sollte „Nicht zugänglich“ angezeigt werden.  Dies ist zu erwarten, da die NSG-Regel „DenyAllInBound“ den gesamten eingehenden Datenverkehr an die VM verweigert.

1. Navigieren Sie im Browser zurück zur Registerkarte **NSG-SC900 – Microsoft Azure**.

1. Wählen Sie im linken Navigationsbereich **Eingehende Sicherheitsregeln** aus. Die Standardregeln für eingehenden Datenverkehr verweigern den gesamten eingehenden Datenverkehr, der nicht von einem VNet oder einem Azure-Lastenausgleich stammt, sodass Sie eine Regel einrichten müssen, um eingehenden RDP-Datenverkehr (Datenverkehr an Port 3389) zuzulassen. Erinnern Sie sich, dass Sie die Standardregeln nicht entfernen, aber außer Kraft setzen können, indem Sie Regeln mit höheren Prioritäten erstellen.

1. Wählen Sie oben auf der Seite die Option **Hinzufügen** aus. Geben Sie auf der Seite „Eingehende Sicherheitsregel hinzufügen“ die folgenden Einstellungen an:
    1. Quelle:  **Beliebig**
    1. Quellportbereiche: **\***
    1. Ziel: **Beliebig**
    1. Dienst:  **RDP**
    1. Aktion: **Zulassen**
    1. Priorität: **1.000**. Regeln mit niedrigeren Zahlen besitzen höhere Priorität und werden zuerst verarbeitet.
    1. Name: Behalten Sie den Standardnamen bei, oder erstellen Sie Ihren eigenen beschreibenden Namen.
    1. Beachten Sie das Warnzeichen am unteren Rand der Seite.  Wir verwenden RDP nur zu Testzwecken und zur Veranschaulichung der Funktionalität der NSG.
    1. Wählen Sie **Hinzufügen** aus

1. Sobald die Regel bereitgestellt wurde, wird sie in der Liste der eingehenden Regeln angezeigt (Möglicherweise müssen Sie den Bildschirm aktualisieren).

1. Lassen Sie diese Browserregisterkarte geöffnet.  

### Aufgabe 3

In dieser Aufgabe testen Sie die neu erstellte NSG-Eingangsregel, um sicherzustellen, dass Sie eine RDP-Verbindung (Remotedesktop) mit der VM herstellen können.  Sobald Sie die VM nutzen, überprüfen Sie die ausgehende Konnektivität mit dem Internet von der VM aus.

1. Öffnen Sie die Registerkarte „SC900-WinVM – Microsoft Azure“ in Ihrem Browser.

1. Klicken Sie im linken Navigationsbereich auf **Verbinden**.

1. Wählen Sie **Zugriff überprüfen** aus. (Überprüfen Sie, ob der Port auf 3389 festgelegt ist.)  Der Status sollte als „Zugänglich“ angezeigt werden.

1. Stellen Sie nun eine direkte Verbindung mit der VM her, indem Sie im Feld „Native RDP“ auf **Auswählen** klicken.
   
    1. Wählen Sie im sich daraufhin öffnenden „Native RDP“-Fenster die Option **RDP-Datei herunterladen** aus.
    1. Wenn eine Downloadwarnung angezeigt wird, wählen Sie **Beibehalten** und dann im angezeigten Popupfenster **Datei öffnen** aus.
    1. Ein Fenster für die Remotedesktopverbindung wird geöffnet. Wählen Sie **Verbinden** aus.
    1. Anschließend werden Sie zur Eingabe Ihrer Anmeldeinformationen aufgefordert.  Geben Sie den Benutzernamen und das Kennwort für die VM ein (siehe Registerkarte „Ressourcen“ im Lab-Anweisungsbereich).
    1. Ein Fenster für die Remotedesktopverbindung wird geöffnet und meldet: *Die Identität des Remotecomputers kann nicht überprüft werden. Möchten Sie trotzdem eine Verbindung herstellen?*  Wählen Sie **Ja** aus.

1. Sie sind nun mit der VM verbunden. In diesem Fall konnten Sie eine Verbindung mit der VM herstellen, da die von Ihnen erstellte Regel für eingehenden Datenverkehr den eingehenden Datenverkehr zur VM über RDP zulässt.  Nach einigen Sekunden wird auf dem Willkommensbildschirm möglicherweise ein Fenster angezeigt, in dem Sie Datenschutzeinstellungen für Ihr Gerät auswählen können. Wählen Sie **Akzeptieren** aus.  Wenn das Fenster „Netzwerke“ angezeigt wird, wählen Sie **Nein** aus.

1. Testen Sie die ausgehende Konnektivität mit dem Internet über die in der RDP-Sitzung ausgeführten VM.
    1. Wählen Sie in der geöffneten VM **Microsoft Edge** aus, um den Browser zu öffnen.  Da Sie Microsoft Edge zum ersten Mal öffnen, wird möglicherweise ein Popupfenster angezeigt. Wählen Sie **Ohne Ihre Daten starten**, **Weiter ohne diese Daten** und dann **Bestätigen und Browsing starten** aus.
    1. Geben Sie **www.bing.com** in die Adressleiste des Browsers ein, und bestätigen Sie, dass Sie eine Verbindung mit der Suchmaschine herstellen können.
    1. Nachdem Sie bestätigt haben, dass Sie auf www.bing.com zugreifen können, schließen Sie das Browserfenster auf der VM, lassen Sie die VM jedoch aktiviert.

1. Minimieren Sie die VM, indem Sie den Unterstrich **_** auf der blauen Registerkarte auswählen, die die IP-Adresse der VM anzeigt. Sie gelangen so zurück zur Seite „SC900-WinVM \| Verbinden“.

1. Lassen Sie die Browserregisterkarte geöffnet, Sie verwenden sie in der nächsten Aufgabe.

### Aufgabe 4

In der vorherigen Aufgabe haben Sie bestätigt, dass Sie eine RDP-Verbindung mit der VM herstellen können. Sobald Sie mit der Verwendung der VM begonnen haben, haben Sie auch bestätigt, dass Sie eine ausgehende Verbindung mit dem Internet herstellen können.  Der ausgehende Internetdatenverkehr wurde zugelassen, weil die Standardausgangsregeln für die NSG ausgehenden Internetdatenverkehr zulassen.  In dieser Aufgabe durchlaufen Sie den Prozess zum Erstellen einer benutzerdefinierten Ausgangsregel, um ausgehenden Internetdatenverkehr zu blockieren und diese Regel zu testen.

1. Sie sollten sich auf der Seite „SC900-WinVM \| Verbinden“ befinden. Wählen Sie im linken Navigationsbereich **Netzwerk** aus. Wenn Sie die Browserregisterkarte zuvor geschlossen haben, wählen Sie oben auf der Seite die blaue Suchleiste aus, und wählen Sie „Virtuelle Computer“ und dann die VM **SC900-WinVM** aus. Wählen Sie anschließend **Netzwerk** aus.

1. Wählen Sie die Registerkarte **Regeln für ausgehende Ports** aus. Die Standardausgangsregeln werden angezeigt.  Beachten Sie die Standardregel „AllowInternetOutBound“. Diese Regel lässt sämtlichen ausgehenden Internetdatenverkehr zu. Sie können die Standardregeln nicht entfernen, aber Sie können sie außer Kraft setzen, indem Sie Regeln mit höheren Prioritäten erstellen. Wählen Sie rechts auf der Seite **Regel für ausgehenden Port hinzufügen** aus.

1. Geben Sie auf der Seite „Sicherheitsregel für ausgehenden Datenverkehr hinzufügen“ die folgenden Einstellungen an:
    1. Quelle:  **Beliebig**
    1. Quellportbereiche: **\***
    1. Ziel:  **Diensttag**
    1. Zieldiensttag:  **Internet**
    1. Dienst:  **Benutzerdefiniert** (Standard beibehalten)
    1. Zielportbereiche: **\*** (Sternchen im Feld für Zielportbereiche eingeben)
    1. Protokoll **Beliebig**
    1. Aktion: **Deny**
    1. Priorität: **1.000**
    1. Name: Behalten Sie den Standardnamen bei, oder erstellen Sie Ihren eigenen beschreibenden Namen.
    1. Wählen Sie **Hinzufügen** aus

1. Sobald die Regel bereitgestellt wurde, wird sie in der Liste der Regeln für ausgehenden Datenverkehr angezeigt.  Obwohl sie in der Liste angezeigt wird, dauert es einige Minuten, bis sie wirksam wird (warten Sie einige Minuten, bevor Sie mit den nächsten Schritten fortfahren).  


1. Kehren Sie zu Ihrer VM zurück (das RDP-Symbol für die VM sollte auf der Taskleiste unten auf der Seite angezeigt werden).

1. Öffnen Sie auf Ihrer VM den Microsoft Edge-Browser, und geben Sie **www.bing.com** ein. Diese Seite sollte nicht angezeigt werden. Wenn Sie eine Verbindung mit dem Internet herstellen können und sichergestellt haben, dass alle Parameter für die Ausgangsregel ordnungsgemäß festgelegt wurden, liegt dies wahrscheinlich daran, dass es einige Minuten dauern kann, bis die Regel wirksam wird.  Schließen Sie den Browser, warten Sie einige Minuten, und versuchen Sie es erneut. Für Azure-Abonnements in der Laborumgebung können Verzögerungen auftreten, die länger als normal sind.

1. Schließen Sie die Remotedesktopverbindung, indem Sie auf das **X** in der oberen Mitte der Seite klicken, auf der die IP-Adresse angezeigt wird.  Ein Popupfenster wird anzeigt, das „Die Remotesitzung wird getrennt“ angibt. Klickan Sie auf **OK**.

1. Wählen Sie in der oberen linken Ecke des Fensters direkt unterhalb der blauen Leiste, wo „Microsoft Azure“ angezeigt wird, die Option **Startseite** aus, um zur Startseite der Azure-Dienste zurückzukehren.

1. Lassen Sie die Azure-Registerkarte in Ihrem Browser geöffnet.

### Überprüfung

In diesem Lab haben Sie den Prozess zur Einrichtung einer Netzwerksicherheitsgruppe (NSG) durchlaufen, die NSG der Netzwerkschnittstelle einer VM zugeordnet und der NSG neue Regeln hinzugefügt, um eingehenden RDP-Datenverkehr zuzulassen und ausgehenden Internetdatenverkehr zu blockieren.
