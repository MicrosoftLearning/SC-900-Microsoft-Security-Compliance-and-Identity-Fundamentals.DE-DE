<!---
---
Demo: Title: 'Azure-Netzwerksicherheitsgruppen (Network Security Groups, NSGs)' Learning Path/Module/Unit: 'Lernpfad: Beschreiben der Funktionen von Microsoft-Sicherheitslösungen; Modul 1: Beschreiben der grundlegenden Sicherheitsfunktionen in Azure; Lerneinheit 6: Beschreiben von Azure-Netzwerksicherheitsgruppen'
---
--->

# Demo: Azure Network Security Groups (NSGs)

Diese Demo ist den folgenden Learn-Inhalten zugeordnet:

- Lernpfad: Beschreiben der Funktionen von Microsoft-Sicherheitslösungen
- Modul: Beschreiben der grundlegenden Sicherheitsfunktionen in Azure
- Lerneinheit: Beschreiben von Azure-Netzwerksicherheitsgruppen

## Vorführungsszenario

In dieser Demo untersuchen Sie die Funktion von Netzwerksicherheitsgruppen in Azure und wenden eine NSG auf eine vorab erstellte VM an. Zunächst zeigen Sie kurz Informationen zu der VM, die vom autorisierten Lab-Hoster (ALH) vorab erstellt wurde. Anschließend zeigen Sie mithilfe einer NSG, die im Rahmen der Einrichtung vor der Demo eingerichtet wurde, die wesentlichen Parameter einer NSG und die Standardregeln für eingehenden und ausgehenden Datenverkehr an. Sie weisen der NSG eine VM-Schnittstelle zu, erstellen eine neue RDP-Regel, um die Verbindung mit dem virtuellen Computer zuzulassen, und testen sie schließlich.

### Teil 1 der Demo

In diesem Teil zeigen Sie einige der Parameter an, die dem virtuellen Computer zugeordnet sind, der im Rahmen der Setupdemo erstellt wurde (DEMO_00_pre_demo_setup.md).

1. Öffnen Sie Microsoft Edge.  Geben Sie **https://portal.azure.com** in der Adressleiste ein und melden Sie sich mit den Administratoranmeldeinformationen für Microsoft 365 an, die von Ihrem autorisierten Labhoster (ALH) bereitgestellt wurden.  Sie befinden sich nun auf der Homepage der Azure-Dienste.

1. Geben Sie **virtuelle Computer** im blauen Suchfeld oben auf der Seite ein, und wählen Sie **Virtuelle Computer** aus den Ergebnissen aus.

1. Wählen Sie **SC900-WinVM** auf der Seite „Virtuelle Computer“ aus.  Dieser virtuelle Computer sollte im Rahmen des Setups vor der Demo erstellt worden sein.  Wenn er nicht aufgeführt ist, erstellen Sie ihn jetzt.

1. Sie befinden sich nun auf der Seite „SC900-WinVM“.  Beachten Sie einige der grundlegenden Informationen zur VM.

1. Wählen Sie im linken Navigationsbereich **Netzwerk** aus.  
    1. Die Standardansicht gilt für Regeln für eingehende Ports.  Beachten Sie, dass für die Netzwerkschnittstelle für diese VM keine Netzwerksicherheitsgruppen konfiguriert sind.  Das gleiche gilt, wenn Sie Regeln für ausgehende Ports auswählen.
    1. Wählen Sie neben „Netzwerkschnittstelle“ die Option **Effektive Sicherheitsregeln** aus.  Beachten Sie die Angabe „Der Netzwerkschnittstelle sind keine Netzwerksicherheitsgruppen oder Anwendungssicherheitsgruppen zugeordnet“.

1. Hinweis für Referenten: Wenn Sie versuchen würden, den Port Status auf der Verbindungsseite zu überprüfen, erhalten Sie die Meldung „Kann nicht überprüft werden“.  Dies bedeutet nicht unbedingt, dass die Ports nicht verfügbar sind.  Wie Sie beachten werden, wenn Sie dieselbe Aktion mit zugewiesener NSG ausführen, erhalten Sie „Nicht Zugänglich“, was angibt, dass der Datenverkehr auf diesem Port blockiert ist.


1. Lassen Sie diese Browserregisterkarte geöffnet.

### Teil 2 der Demo

In diesem Teil weisen Sie der NSG eine Schnittstelle zu. Sie sprechen über die Standardregeln für eingehenden und ausgehenden Datenverkehr, um zu zeigen, wie die Regeln funktionieren.  Weisen Sie als Teil der Vorbereitung der Demo die Netzwerkschnittstelle der VM dieser NSG zu, und erstellen Sie eine neue Regel für eingehenden RDP-Datenverkehr.

1. Öffnen Sie eine neue Browserregisterkarte für das Azure-Portal (portal.azure.com), und geben Sie in der blauen Suchleiste oben auf der Seite **Netzwerksicherheitsgruppen** ein. Wählen Sie in den Ergebnissen **Netzwerksicherheitsgruppen** (nicht „Klassische Netzwerksicherheitsgruppen“) aus.

1. Wählen Sie die NSG aus, die im Rahmen des Setups vor der Demo erstellt wurde. Wenn Sie sie zuvor noch nicht erstellt haben, tun Sie dies jetzt. Wählen Sie **Netzwerksicherheitsgruppe erstellen** aus, und geben Sie die folgenden Einstellungen an:
    1. Abonnement: Behalten Sie den Standardwert bei (dies ist das Azure-Abonnement, das vom autorisierten Lab-Hoster bereitgestellt wird).
    1. Ressourcengruppe: **LabsSC900** (dieselbe Ressourcengruppe, die von der VM verwendet wird).
    1. Name:  **NSG-SC900**
    1. Region: Übernehmen Sie den Standardwert.
    1. Klicken Sie auf**Überprüfen + erstellen** und dann auf **Erstellen**.
    1. Sobald die Bereitstellung abgeschlossen ist (dies geschieht sehr schnell), wählen Sie **Zu Ressource wechseln** aus.

1. Oben auf der darunterliegenden Seite unter „Zusammenfassung“ werden einige grundlegende Informationen zur von Ihnen erstellten NSG angezeigt.  Zwei Punkte sind zu beachten: Es gibt keine BENUTZERDEFINIERTEN Sicherheitsregeln und keine Subnetze oder Netzwerkschnittstellen, die dieser NSG zugeordnet sind.  Obwohl es keine benutzerdefinierten Sicherheitsregeln gibt, gibt es Standardregeln für eingehenden und ausgehenden Datenverkehr, die in jeder NSG enthalten sind, wie auf der Seite gezeigt.  Überprüfen Sie die Eingangs- und Ausgangsregeln. Die Standardregeln für eingehenden Datenverkehr verweigern den gesamten eingehenden Datenverkehr, der nicht aus einem virtuellen Netzwerk oder einem Azure-Lastenausgleich stammt.  Die Ausgangsregeln verweigern den gesamten ausgehenden Datenverkehr mit Ausnahme des Datenverkehrs zwischen virtuellen Netzwerken und des ausgehenden Datenverkehrs in das Internet.

1. Wählen Sie im linken Navigationsbereich auf der Seite „NSG-SC900“ unter „Einstellungen“ die Option **Netzwerkschnittstellen** aus.
    1. Wählen Sie **Zuordnen** aus.
    1. Wählen Sie im Feld zum Auswählen von Netzwerkschnittstellenzuordnungen den **Abwärtspfeil** aus, wählen Sie **sc900-winvmXXX** aus und dann unten im Fenster **OK**. Sobald die Schnittstelle dem NSG zugeordnet ist, wird sie in der Liste angezeigt.

1. Geben Sie den zu dem virtuellen Computer zurück, indem Sie die Browserregisterkarte für den virtuellen Computer auswählen.  Sie sollten sehen, dass jetzt eine NSG an die VM-Schnittstelle angefügt ist.  Die Tabelle mit eingehenden Portregeln wird angezeigt. Die Standardregeln für eingehenden Datenverkehr verweigern den gesamten eingehenden Datenverkehr, der nicht aus einem virtuellen Netzwerk oder einem Azure-Lastenausgleich stammt.  Um dies zu testen, überprüfen Sie den Status am RDP-Port 3389.
    1. Wählen Sie oben auf der Seite **Verbinden** und dann für Port 3389 (RDP) **Zugriff überprüfen** aus. Daraufhin wird „Nicht zugänglich“ angezeigt.  
    1. Obwohl Sie nur mit dem RDP-Port 3389 testen, wird der gesamte eingehende Netzwerkdatenverkehr, der nicht aus einem anderen virtuellen Netzwerk oder Lastenausgleich stammt, blockiert.  

1. Erstellen Sie jetzt eine Regel, um eingehenden Datenverkehr auf dem RDP-Port zuzulassen.  Wählen Sie im linken Navigationsbereich **Netzwerk** aus. Die Tabelle mit den Regeln für eingehende Ports sollte angezeigt werden (die Registerkarte für eingehende Portregeln ist unterstrichen).  Wählen Sie rechts auf der Seite **Regel für eingehenden Port hinzufügen** aus. Ein wichtiger Punkt auf den Sie hinweisen sollten ist, dass Sie die Standardregeln nicht entfernen, aber außer Kraft setzen können, indem Sie Regeln mit höheren Prioritäten erstellen. Geben Sie auf der Seite „Eingehende Sicherheitsregel hinzufügen“ die folgenden Einstellungen an:
    1. Quelle:  **Beliebig**
    1. Quellportbereiche: **\***
    1. Ziel: **Beliebig**
    1. Dienst:  **RDP**
    1. Aktion: **Zulassen**
    1. Priorität: **1000**. Hinweis: Regeln mit niedrigeren Zahlen haben eine höhere Priorität und werden zuerst verarbeitet.
    1. Name: Behalten Sie den Standardnamen bei, oder erstellen Sie Ihren eigenen beschreibenden Namen.
    1. Beachten Sie das Warnzeichen am unteren Rand der Seite.  Wir verwenden RDP nur zu Testzwecken und zur Veranschaulichung der Funktionalität der NSG.
    1. Wählen Sie **Hinzufügen** aus.

1. Sobald die Regel bereitgestellt wurde, wird sie in der Liste der eingehenden Regeln angezeigt (Möglicherweise müssen Sie den Bildschirm aktualisieren).

### Teil 3 der Demo

Wenn die NSG Ihrer VM und der erstellten RDP-Regel zugeordnet wurde, zeigen Sie die Auswirkungen der NSG, indem Sie die RDP-Konnektivität mit der VM testen.

1. Öffnen Sie die Registerkarte SC900-WinVM – Microsoft Azure in Ihrem Browser. 

1. Wählen Sie im linken Navigationsbereich **Verbinden** aus.
    1. Sie können einfach **Zugriff überprüfen** auswählen.  Der Status sollte als „Zugänglich“ angezeigt werden. Wenn Sie Zeit haben, können Sie alternativ eine Verbindung mit dem virtuellen Computer herstellen, indem Sie unter Windows eine Instanz der Remotedesktopverbindung öffnen.  Mit dieser Option wird der virtuelle Computer geöffnet, wenn die Verbindung erfolgreich hergestellt wurde.  Im Folgenden sind die Schritte aufgeführt:
        1. Geben Sie in der Windows-Suchleiste **Remotedesktopverbindung** ein, und wählen Sie dann **Öffnen** aus.
        1. Geben Sie in das Feld neben **Computer** die öffentliche IP-Adresse Ihres virtuellen Computers ein.
        1. Nachdem Sie die IP-Adresse eingegeben haben, sollte der Benutzername unter dem Feld angezeigt werden, in dem Sie die IP-Adresse eingegeben haben. Wenn nicht, erweitern Sie **Optionen anzeigen** und geben Sie den Benutzernamen für Ihren virtuellen Computer ein, und wählen Sie dann **Verbinden** aus.
        1. Ein Fenster für die Remotedesktopverbindung wird geöffnet und meldet: Die Identität des Remotecomputers kann nicht überprüft werden. Möchten Sie trotzdem eine Verbindung herstellen? Wählen Sie **Ja** aus.
        1. Sie sind nun mit der VM verbunden. Verdeutlichen Sie dem bzw. der Kursteilnehmer*in, dass Sie in diesem Fall eine Verbindung mit der VM herstellen konnten, da die von Ihnen erstellte Regel für eingehenden Datenverkehr den eingehenden Datenverkehr zur VM über RDP zulässt.
        1. Minimieren Sie die VM, indem Sie den Unterstrich **_** auf der blauen Registerkarte auswählen, die die IP-Adresse der VM anzeigt. Sie gelangen so zurück zur Seite „SC900-WinVM | Verbinden“.

1. Wählen Sie im linken Navigationsbereich **Netzwerk** und dann im Hauptfenster die Option **Ausgehende Portregeln** aus.  Sprechen Sie über die Standardregeln für ausgehenden Datenverkehr. Die Standardregeln lassen ausgehenden VNET-Datenverkehr von jedem virtuellen Netzwerk zu jedem anderen virtuellen Netzwerk zu und lassen ausgehenden Internetdatenverkehr zu. Jeder andere Typ von ausgehendem Datenverkehr wird verweigert.  Sie können die Standardregel nicht entfernen, aber Sie können sie überschreiben, indem Sie eine Regel mit höherer Priorität auf die gleiche Weise erstellen, wie Sie eine Eingangsregel erstellt haben.

1. Wenn Sie genug Zeit haben und Sie ähnliche Schritte für ausgehenden Datenverkehr zeigen möchten, führen Sie den unten aufgeführten optionalen Demoteil vor.  Beenden Sie andernfalls die VM, aber lassen Sie die Registerkarte Azure in Ihrem Browser für die nächste Demo geöffnet.

### OPTIONAL: Teil 4 der Demo

In diesem Teil zeigen Sie die aktuellen NSG-Ausgangsregeln, die ausgehenden Internetdatenverkehr von der VM zulassen.  Anschließend erstellen Sie eine Regel zum Blockieren des ausgehenden Internetdatenverkehrs von der VM. Schließlich zeigen Sie die Auswirkungen der neu erstellten Regel an, indem Sie versuchen, von der VM aus auf das Internet zuzugreifen.

1. Öffnen Sie den virtuellen Computer, den Sie im vorherigen Schritt minimiert haben. Hier können Sie ausgehende Internetkonnektivität mit dem Internet zeigen, die durch eine der Standardregeln für ausgehenden Datenverkehr aktiviert ist. Sobald der virtuelle Computer geöffnet wird und Sie sich als Benutzer angemeldet haben, wählen Sie **Microsoft Edge** aus, um den Browser zu öffnen.  Da Sie Microsoft Edge zum ersten Mal öffnen, wird möglicherweise ein Popupfenster angezeigt. Wählen Sie **Ohne Ihre Daten starten**, **Weiter ohne diese Daten** und dann **Bestätigen und Browsing starten** aus.
    1. Geben Sie **www.bing.com** in die Adressleiste des Browsers ein, und bestätigen Sie, dass Sie eine Verbindung mit der Suchmaschine herstellen können.
    1. Nachdem Sie bestätigt haben, dass Sie auf www.bing.com zugreifen können, schließen Sie das Browserfenster auf der VM, lassen Sie die VM jedoch aktiviert.

1. Minimieren Sie die VM, indem Sie den Unterstrich **_** auf der blauen Registerkarte auswählen, die die IP-Adresse der VM anzeigt. Sie gelangen so zurück zur Seite „SC900-WinVM | Verbinden“.  

1. Wählen Sie im linken Navigationsbereich **Netzwerk** aus.

1. Wählen Sie die Registerkarte **Regeln für ausgehende Ports** aus. Die Standardausgangsregeln werden angezeigt.  Beachten Sie die Standardregel "AllowInternetOutBound". Diese Regel lässt sämtlichen ausgehenden Internetdatenverkehr zu. Sie können die Standardregeln nicht entfernen, aber Sie können sie außer Kraft setzen, indem Sie Regeln mit höheren Prioritäten erstellen. Wählen Sie rechts auf der Seite **Regel für ausgehenden Port hinzufügen** aus.

1. Geben Sie auf der Seite „Ausgehende Sicherheitsregel hinzufügen“ die folgenden Einstellungen an:
    1. Quelle:  **Beliebig**
    1. Quellportbereiche: **\***
    1. Ziel:  **Diensttag**
    1. Zieldiensttag:  **Internet**
    1. Dienst:  **Benutzerdefiniert** (Standard beibehalten)
    1. Zielportbereiche:  * (Sternchen im Feld für Zielportbereiche eingeben)
    1. Protokoll **Beliebig**
    1. Aktion: **Deny**
    1. Priorität: **1.000**
    1. Name: Behalten Sie den Standardnamen bei, oder erstellen Sie Ihren eigenen beschreibenden Namen.
    1. Wählen Sie **Hinzufügen** aus.

1. Sobald die Regel bereitgestellt wurde, wird sie in der Liste der ausgehenden Regeln angezeigt.  Obwohl sie in der Liste angezeigt wird, dauert es einige Minuten, bis sie wirksam wird (warten Sie einige Minuten, bevor Sie mit den nächsten Schritten fortfahren).  

1. Kehren Sie zu Ihrer VM zurück (das Symbol für die VM sollte auf der Taskleiste unten auf der Seite angezeigt werden).

1. Öffnen Sie auf Ihrer VM den Microsoft Edge-Browser, und geben Sie **www.bing.com** ein. Diese Seite sollte nicht angezeigt werden.  Hinweis: Wenn Sie eine Verbindung mit dem Internet herstellen können und sichergestellt haben, dass alle Parameter für die Ausgangsregel ordnungsgemäß festgelegt wurden, liegt dies wahrscheinlich daran, dass es einige Minuten dauern kann, bis die Regel wirksam wird.  Schließen Sie den Browser, warten Sie einige Minuten, und versuchen Sie es erneut.  Hinweis: Für Azure-Abonnements in der Lab-Umgebung können Verzögerungen auftreten,die länger als normal sind.

1. Schließen Sie die Remotedesktopverbindung, indem Sie das **X** in der oberen Mitte der Seite auswählen, auf der die IP-Adresse angezeigt wird.  Ein Popupfenster wird anzeigt, das „Die Remotesitzung wird getrennt“ angibt. Klickan Sie auf **OK**.

1. Lassen Sie die Registerkarte Azure in Ihrem Browser für die nächste Azure-Demo geöffnet.

### Überprüfung

In dieser Demo haben Sie die Informationen und Einstellungen in Bezug auf eine NSG gezeigt, darunter den Prozess zum Zuordnen einer Schrittstelle zu einer NSG. Sie haben die standardmäßigen Eingangs- und Ausgangsregeln und schließlich die Schritte zum Erstellen einer neuen Regel gezeigt.
