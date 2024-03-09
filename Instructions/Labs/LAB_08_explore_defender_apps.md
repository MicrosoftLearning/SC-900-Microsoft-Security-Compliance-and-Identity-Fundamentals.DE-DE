---
lab:
  title: Erkunden von Microsoft Defender for Cloud Apps
  module: Describe the threat protection capabilities of Microsoft 365
---

# Lab: Erkunden von Microsoft Defender für Cloud-Apps

Dieses Lab ist den folgenden Learn-Inhalten zugeordnet:

- Lernpfad: Beschreiben der Funktionen von Microsoft-Sicherheitslösungen
- Modul: Beschreiben der Bedrohungsschutzfunktionen von Microsoft 365
- Lerneinheit: Beschreiben von Microsoft Defender für Cloud-Apps

## Labszenario

In diesem Lab erkunden Sie die Funktionen von Microsoft Defender for Cloud-Apps.  Sie durchlaufen die Informationen, die auf dem Cloud Discovery-Dashboard verfügbar sind, den Cloud-App-Katalog, die verfügbaren Funktionen zur Untersuchung der Ergebnisse und die Möglichkeiten zur Steuerung der Auswirkungen auf Ihr Unternehmen durch Richtlinien. Hinweis: Eine Organisation muss über eine Lizenz verfügen, um Microsoft Defender for Cloud-Apps verwenden zu können, einen benutzerbasierten Abonnementdienst.

**Geschätzte Dauer**: 15 bis 20 Minuten

### Aufgabe 1: Erkunden von Cloud Discovery

Erkunden Sie Cloud Discovery.

1. Öffnen Sie Microsoft Edge. Geben Sie **admin.microsoft.com** in die Adressleiste ein.

1. Melden Sie sich mit Ihren Administratoranmeldeinformationen für den Microsoft 365-Mandanten an.
    1. Geben Sie **admin@WWLxZZZZZZ.onmicrosoft.com** (ZZZZZZ ist hierbei die eindeutige Mandanten-ID, die von Ihrem Lab-Hostinganbieter bereitgestellt wurde) in das Fenster „Anmelden“ ein, und wählen Sie dann **Weiter** aus.
    1. Geben Sie das Administratorkennwort ein, das von Ihrem Lab-Hostinganbieter bereitgestellt werden sollte. Wählen Sie **Anmelden**.
    1. Wählen Sie **Ja** aus, wenn Sie gefragt werden, ob Sie angemeldet bleiben möchten. Dadurch gelangen Sie zur Seite „Microsoft 365 Admin Center“.

1. Wählen Sie im linken Navigationsbereich von Microsoft 365 Admin Center **Alle anzeigen** aus.

1. Wählen Sie **Sicherheit** unter „Admin Center“ aus.  Die Startseite des Microsoft 365 Defender-Portals wird auf einer neuen Browserseite geöffnet.  

1. Wenn Sie das Microsoft 365 Defender-Portal das erste Mal besuchen, wird möglicherweise ein Popupfenster für eine Schnelleinführung angezeigt.  Schließen Sie es.

1. Wählen Sie im linken Navigationsbereich **Cloud-Apps** aus, um die Liste zu erweitern, und wählen Sie dann **Cloud Discovery** aus. Dadurch gelangen Sie zur Dashboardansicht.  Beachten Sie die im Dashboard verfügbaren Informationen. In der Dashboardansicht können Sie oben auf der Seite verschiedene Registerkarten auswählen.  

1. Wählen Sie **Ermittelte Apps** aus. Das Fenster „Ermittelte Apps“ enthält eine ausführliche Ansicht der ermittelten Apps, einschließlich der Risikobewertung, des Datenverkehrs, der Anzahl der Benutzer und mehr.
    1. Wählen Sie für ein beliebiges Element in der Liste die **Auslassungspunkte** (...) in der Tabellenspalte der Aktion aus.  Beachten Sie die verschiedenen Optionen, die verfügbar sind, einschließlich der Funktion, mit der eine Apps als sanktioniert oder nicht sanktioniert markiert werden kann.  Wählen Sie die **Auslassungspunkte** (...) erneut aus, um das Aktionsfeld zu schließen.
    1. Durch die Auswahl eines bestimmten Zeilenelements wird für die bestimmte App eine Detailseite geöffnet.  Wählen Sie ein Element aus der Liste aus, und überprüfen Sie die Informationen, die auf der Übersichtsseite verfügbar sind.  Wählen Sie für das ausgewählte Element die Registerkarte **Cloud-App-Nutzung** aus, um ausführlichere Informationen wie **Nutzung**, **Benutzer**, **IP-Adressen** und **Warnungen** anzuzeigen. Wenn Sie mit dem Untersuchen der Detailseite fertig sind, kehren Sie zur Seite „Ermittelte Apps“ zurück, indem Sie oben auf der Seite **Cloud Discovery** auswählen.  Wenn Sie „Cloud Discovery“ im linken Navigationsbereich auswählen, gelangen Sie zurück zur Dashboardansicht.
    1. Wählen Sie oben auf der Seite die Registerkarte **IP-Adressen** aus. Dort finden Sie Daten wie die Anzahl der Transaktionen, das Datenverkehrsvolumen und die Uploadvolumen nach IP-Adresse.  Beachten Sie, dass Sie auch nach einer bestimmten IP-Adresse filtern oder die Daten zur weitergehenden Analyse exportieren können.
    1. Wählen Sie oben auf der Seite die Option **Benutzer** aus.  Dies ist derselbe Informationstyp, der bei der Auswahl von IP-Adressen bereitgestellt wird. Diese Angaben werden jedoch für einzelne Benutzer aufgelistet.  Auch hier filtern Sie nach einem bestimmten Benutzer und exportieren die Daten zur weitergehenden Analyse.

1. Die auf der Seite „Cloud Discovery“ und den zugehörigen Registerkarten bereitgestellten Informationen beruhen entweder auf Momentaufnahmeberichten von Datenverkehrsprotokollen, die Sie manuell von Ihren Firewalls und Proxys hochladen, oder auf fortlaufenden Berichten, die alle Protokolle analysieren, die aus Ihrem Netzwerk mit Cloud App Security weitergeleitet werden.  Wählen Sie in der oberen rechten Ecke der Seite **Aktionen** aus, um zu erfahren, wo dies eingerichtet wird.
    1. Wählen Sie die erste Option **Momentaufnahmebericht zu Cloud Discovery erstellen** und dann **Weiter** aus. Hier tragen Sie die erforderlichen Details ein und laden Datenverkehrsprotokolle hoch, um einen Bericht zu generieren und hochzuladen.  Wählen Sie **Beenden** aus, und wählen Sie erneut **Beenden** aus, wenn Sie gefragt werden, ob Sie sicher sind.  Die für Ihren Lab-Mandanten angezeigten Daten stammen aus einem Momentaufnahmebericht. Sie können diese Informationen oben im Cloud Discovery-Fenster anzeigen.
    1. Wählen Sie zum Anzeigen der Option für fortlaufende Berichte **Aktionen** in der oberen rechten Ecke der Seite aus, und wählen Sie im Dropdown den Eintrag **Automatischen Upload konfigurieren** aus.  Es sind keine Datenquellen verbunden. Hier würden Sie jedoch eine Datenquelle hinzufügen. Wählen Sie **Datenquelle hinzufügen** und dann den Dropdownpfeil im Feld **Appliance auswählen** aus, um die Appliancetypen anzuzeigen, die Sie als Datenquelle verbinden können.  Wählen Sie **Abbrechen** aus, um den Vorgang zu beenden.
    1. Wählen Sie im linken Navigationsbereich **Cloud Discovery** aus, um zur Seite „Cloud Discovery“ zurückzukehren.

1. Sie sich können sich direkt mit Apps verbinden, indem Sie App-Connectors einrichten, die Ihnen bessere Sichtbarkeit und Kontrolle über Ihre Cloud-Apps ermöglichen. Wählen Sie in der oberen rechten Ecke des Bildschirms **Aktionen** und dann **Cloud Discovery**-Einstellungen aus.  Wählen Sie auf der linken Seite des Bildschirms unter „Verbundene Apps“ die Option **App-Connectors** aus.  

    1. Wählen Sie auf der Seite „Verbundene Apps“ **Office 365** aus der Liste aus, um die verfügbaren detaillierten Informationen anzuzeigen, und wählen Sie dann die vertikalen Auslassungspunkte (⋮) auf der rechten Seite des Bildschirms aus. Wählen Sie dann **App-Connectoreinstellungen anzeigen** aus, um zur Seite „App-Connectors“ zurückzukehren. Wenn für Office 365 ein Verbindungsfehler angezeigt wird, liegt dies höchstwahrscheinlich daran, dass die Option für Überwachung nicht aktiviert ist.  Wenn die Überwachung aktiviert ist, wechseln Sie zu den vertikalen Auslassungspunkten (⋮) auf der rechten Seite des Zeilenelements, und wählen Sie dann **Einstellungen bearbeiten** aus.  Um die Verbindung erneut herzustellen, wählen Sie am unteren Rand der Seite **Office 365 verbinden** aus. Auf der Seite sollte nun angezeigt werden, dass Office 365 verbunden ist. Wählen Sie **Fertig** aus.  Der Status wird nun mit einem gelben Warnzeichen angezeigt, das angibt, dass kein aktueller Status vorhanden ist.  Es dauert einige Zeit, bis der Status aktualisiert wird, da sich der Zeitraum für die rückwirkende Überprüfung je nach App unterscheidet und für Lab-Mandanten möglicherweise längere Verzögerungen als üblich auftreten.

    1. Jetzt richten Sie einen neuen App-Connector ein. Wählen Sie **+ App verbinden** aus. Wählen Sie dann in der Dropdownliste den Eintrag **Microsoft Azure** aus.  Wählen Sie im Microsoft Azure-Popupfenster **Mit Microsoft Azure verbinden** und dann **Fertig** aus.  Sie sehen dann den Status verbunden (falls Sie ihn nicht sehen sollten, aktualisieren Sie Ihren Browser). Wählen Sie **Microsoft Azure** aus, um die detaillierten Informationen zum Überprüfen von Benutzern, Daten und Aktivitäten anzuzeigen.  Kehren Sie zum Cloud Discovery-Dashboard zurück, indem Sie im Navigationsbereich ganz links **Cloud Discovery** auswählen.

1. Lassen Sie diese Seite geöffnet, da Sie sie in der nächsten Aufgabe verwenden werden.

### Aufgabe 2: Erkunden des Cloud-App-Katalogs

Cloud Discovery analysiert Ihre Datenverkehrsprotokolle im Abgleich mit dem Cloud-App-Katalog von Microsoft Defender for Cloud-Apps, der mehr als 31.000 Cloud-Apps enthält. Die Apps werden nach über 80 Risikofaktoren bewertet, damit Sie laufende Einblicke in die Verwendung der Cloud, die Schatten-IT und die Risiken haben, die die Schatten-IT für Ihre Organisation darstellt.  In dieser Aufgabe untersuchen Sie die Funktionen des Cloud-App-Katalogs.

1. Wählen Sie im linken Navigationsbereich **Cloud-App-Katalog** aus.

1. Mithilfe des Cloud-App-Katalogs können Sie auswählen, welche App den Sicherheitsanforderungen Ihrer Organisation gerecht wird. Administratoren können grundlegende Filterung von Apps durchführen, wie oben auf der Seite gezeigt. Dazu gehört, ob die App sanktioniert bzw. unsanktioniert ist oder kein Tag, keine Risikobewertung, keinen Compliancerisikofaktor und keinen Sicherheitsrisikofaktor aufweist.  Wenn Sie beispielsweise nach dem Compliancerisikofaktor filtern, können Sie nach bestimmten Standards, Zertifizierungen und Compliancevorgaben suchen, die die App möglicherweise erfüllt. Dazu zählen beispielsweise HIPAA, ISO 27001, SOC 2 und PCI-DSS. Wählen Sie **Kompatibilitätsrisikofaktor** aus, um die verfügbaren Optionen anzuzeigen.  Sie können weiter nach Risikobewertung filtern, indem Sie die Schieberegler für die Risikobewertung oben auf der Seite verwenden. Wenn Sie den Regler verschoben haben, stellen Sie sicher, dass Sie ihn so festgelegt haben, dass der Bereich auf 0 bis 10 festgelegt ist.

1. Administratoren können auch nach Apps nach Kategorie suchen.  Geben Sie z. B. im Feld zum Suchen nach Kategorie **Soziales Netzwerk** ein, und wählen Sie dann **Soziales Netzwerk** aus.  Wählen Sie ein beliebiges Element aus der Liste aus, um eine detaillierte Ansicht zu erhalten.  Wenn Sie mit dem Mauszeiger auf Themen für eine bestimmte Kategorie zeigen, wird ein Informationssymbol angezeigt, das Sie auswählen können, um weitere Informationen zum jeweiligen Thema zu erhalten.

1. Lassen Sie diese Seite geöffnet, da Sie sie in der nächsten Aufgabe verwenden werden.

### Aufgabe 3: Erkunden des Aktivitätsprotokolls und der -dateien

Erkunden Sie Möglichkeiten, die aufgezeichneten Aktivitäten mit dem Aktivitätsprotokoll und den -dateien zu untersuchen.

1. Wählen Sie im linken Navigationsbereich **Aktivitätsprotokoll** aus. Hier können Sie alle Aktivitäten im Zusammenhang mit Ihren verbundenen Apps anzeigen. Möglicherweise werden keine Daten aufgelistet, da es mehrere Stunden dauern kann, rückwirkende Überprüfungen durchzuführen, nachdem Überwachung aktiviert wurde, und für Lab-Mandanten möglicherweise Verzögerungen auftreten, die länger als normal sind. Beachten Sie die verfügbaren Filteroptionen und die Option zum Erstellen einer neuen Richtlinie aus der Suche.

1. Um den Datenschutz zu gewährleisten, erhalten Sie Einblick von Microsoft Defender for Cloud Apps in alle Dateien aus Ihren verbundenen Apps, z. B. alle in SharePoint und Salesforce gespeicherten Dateien. Wählen Sie im linken Navigationsbereich die Option **Dateien** aus, und erkunden Sie sie.
    1. Die Möglichkeit zum Überprüfen von Dateien muss im Rahmen der Informationsschutzeinstellungen von Microsoft 365 Cloud-Apps aktiviert werden.  Wählen Sie **Dateiüberwachung aktivieren** aus, und wählen Sie das Kontrollkästchen neben **Dateiüberwachung aktivieren** aus, und wählen Sie dann **Speichern** aus.  
    1. Kehren Sie zu Dateien zurück, indem Sie im linken Navigationsbereich unter Cloud-Apps die Option **Dateien** auswählen. Wie bereits erwähnt, kann es mehrere Tage dauern, bis Dateien angezeigt werden. Sobald die Dateiüberwachung aktiviert ist, sollten Sie beachten, dass Sie nach der Liste der Dateien Daten nach App, Besitzer, Zugriffsebene, Dateityp und übereinstimmender Richtlinie filtern können. Beachten Sie auch die Option zum Erstellen einer neuen Richtlinie aus der Suche und dem Export der Daten.

1. Lassen Sie diese Seite geöffnet, da Sie sie in der nächsten Aufgabe verwenden werden.

### Aufgabe 4: Erkunden von Richtlinien

In dieser Aufgabe erkunden Sie die Richtlinien in Microsoft Defender for Cloud-Apps.

1. Wählen Sie im linken Navigationsbereich **Richtlinien** und dann **Richtlinienverwaltung** aus.  Die aufgelisteten Richtlinien umfassen Informationen zur Anzahl der von der Richtlinie generierten Warnungen, zum Schweregrad usw. Durch Auswahl eines Elements werden ausführlichere Informationen zur Richtlinie angezeigt.
    1. Beachten Sie, dass Sie auch eine Richtlinie erstellen können. Wählen Sie **+ Richtlinie erstellen** aus, um die Richtlinientypen anzuzeigen, die Sie erstellen können.  Wählen Sie **Aktivitätsrichtlinie** aus, um die verschiedenen Optionen anzuzeigen, die zum Erstellen der Richtlinie verfügbar sind.  Wählen Sie **Abbrechen** aus, um das Konfigurationsfenster zu schließen.
    1. Beachten Sie, dass Sie auch die Möglichkeit haben, Richtlinieninformationen zu exportieren.

1. Wählen Sie im linken Navigationsbereich **Richtlinienvorlagen** aus. Um eine Richtlinie aus einer der verfügbaren Vorlagen zu erstellen, wählen Sie **+** auf der linken Seite des Vorlagenzeilenelements aus.  Zeigen Sie die verschiedenen Konfigurationsoptionen für die Richtlinie an.  Wählen Sie **Abbrechen** aus, um die Seite zu schließen.

1. Schließen Sie das Browserfenster.

### Überprüfung

In diesem Lab haben Sie die Funktionen von Microsoft Defender für Cloud-Apps erkundet.  Sie haben die Informationen durchlaufen, die auf dem Cloud Discovery-Dashboard verfügbar sind, den Cloud-App-Katalog, die verfügbaren Funktionen zur Untersuchung der Ergebnisse und die Möglichkeiten zur Steuerung der Auswirkungen auf Ihr Unternehmen durch Richtlinien.
