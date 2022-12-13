<a name="---"></a><!---
---
Demo: Title: 'Microsoft Defender für Cloud-Apps' Module: 'Lernpfad: Beschreiben der Funktionen von Microsoft-Sicherheitslösungen; Modul 4: Beschreiben der Bedrohungsschutzfunktionen von Microsoft 365; Lerneinheit 5: Beschreiben von Microsoft Defender für Cloud-Apps'
---
--->

# <a name="demo-microsoft-defender-for-cloud-apps"></a>Demo: Microsoft Defender für Cloud-Apps

Diese Demo ist den folgenden Learn-Inhalten zugeordnet:

- Lernpfad: Beschreiben der Funktionen von Microsoft-Sicherheitslösungen
- Modul: Beschreiben der Bedrohungsschutzfunktionen von Microsoft 365
- Lerneinheit: Beschreiben von Microsoft Defender für Cloud-Apps

## <a name="demo-scenario"></a>Demoszenario

In dieser Demo zeigen Sie die Funktionen von Microsoft Defender for Cloud-Apps.  Sie führen die Lernenden durch die Informationen, die im Cloud Discovery-Dashboard verfügbar sind, den Cloud App-Katalog, die Möglichkeiten zur Untersuchung der Ergebnisse mit dem Aktivitätsprotokoll und Dateien sowie die Möglichkeiten zur Kontrolle der Auswirkungen auf Ihr Unternehmen mithilfe von Richtlinien.  Hinweis: Eine Organisation muss über eine Lizenz verfügen, um Microsoft Defender for Cloud-Apps verwenden zu können, einen benutzerbasierten Abonnementdienst.  

### <a name="demo-part-1-explore-cloud-discovery"></a>Teil 1 der Demo: Erkunden von Cloud Discovery

1. Öffnen Sie Microsoft Edge. Geben Sie **admin.microsoft.com** in die Adressleiste ein.  Sie sollten bereits als Administrator angemeldet sein.  Falls nicht, melden Sie sich mit Ihren Administratoranmeldeinformationen an.

1. Wählen Sie im linken Navigationsbereich von Microsoft 365 Admin Center **Alle anzeigen** aus.  Äußern Sie sich zum Punkt, dass der Zugriff auf die unterschiedlichen Microsoft 365 Admin Centers von hier aus möglich ist.

1. Wählen Sie **Sicherheit** unter „Admin Center“ aus.  Die Startseite des Microsoft 365 Defender-Portals wird auf einer neuen Browserseite geöffnet.  

1. Wenn Sie das Microsoft 365 Defender-Portal das erste Mal besuchen, wird möglicherweise ein Popupfenster für eine Schnelleinführung angezeigt.  Schließen Sie es.

1. Wählen Sie im linken Navigationsbereich **Cloud-Apps** aus, um die Liste zu erweitern, und wählen Sie dann **Cloud Discovery** aus. Dadurch gelangen Sie zur Dashboardansicht.  Beachten Sie die im Dashboard verfügbaren Informationen. In der Dashboardansicht können Sie oben auf der Seite verschiedene Registerkarten auswählen.  Sehen Sie oben auf der Seite die einzelnen Registerkarten durch.
    
1. Wählen Sie **Ermittelte Apps** aus. Das Fenster „Ermittelte Apps“ enthält eine ausführliche Ansicht der ermittelten Apps, einschließlich der Risikobewertung, des Datenverkehrs, der Anzahl der Benutzer und mehr. 
    1. Wählen Sie für ein beliebiges Element in der Liste die **Auslassungspunkte** in der Spalte der Aktion der Tabelle aus.  Beachten Sie die verschiedenen Optionen, die verfügbar sind, einschließlich der Funktion, mit der eine Apps als sanktioniert oder nicht sanktioniert markiert werden kann.  Wählen Sie die Auslassungspunkte erneut aus, um das Aktionsfeld zu schließen.
    1. Durch die Auswahl eines bestimmten Zeilenelements wird für die bestimmte App eine Detailseite geöffnet.  Wählen Sie ein Element in der Liste aus.  Wählen Sie für das ausgewählte Element die Registerkarte **Cloud-App-Nutzung** aus, um ausführlichere Informationen wie **Nutzung**, **Benutzer**, **IP-Adressen** und **Warnungen** anzuzeigen. Wenn Sie mit dem Untersuchen der Detailseite fertig sind, kehren Sie zur Seite „Ermittelte Apps“ zurück, indem Sie oben auf der Seite **Cloud Discovery** auswählen.  Wenn Sie „Cloud Discovery“ im linken Navigationsbereich auswählen, gelangen Sie zurück zur Dashboardansicht.
    1. Wählen Sie oben auf der Seite die Registerkarte **IP-Adressen** aus. Dort finden Sie Daten wie die Anzahl der Transaktionen, das Datenverkehrsvolumen und die Uploadvolumen nach IP-Adresse.  Beachten Sie, dass Sie auch nach einer bestimmten IP-Adresse filtern oder die Daten zur weitergehenden Analyse exportieren können.
    1. Wählen Sie oben auf der Seite die Option **Benutzer** aus.  Dies ist derselbe Informationstyp, der bei der Auswahl von IP-Adressen bereitgestellt wird. Diese Angaben werden jedoch für einzelne Benutzer aufgelistet.  Auch hier filtern Sie nach einem bestimmten Benutzer und exportieren die Daten zur weitergehenden Analyse.

1. Ein wichtiger Punkt ist, dass die auf der Seite Cloud Discovery und den zugehörigen Registerkarten bereitgestellten Informationen entweder auf Momentaufnahmeberichten von Datenverkehrsprotokollen beruhen, die Sie manuell von Ihren Firewalls und Proxys hochladen, oder auf fortlaufenden Berichten, die alle Protokolle analysieren, die aus Ihrem Netzwerk mit Cloud App Security weitergeleitet werden.  Wählen Sie in der oberen rechten Ecke der Seite **Aktionen** aus, um zu erfahren, wo dies eingerichtet wird.
    1. Wählen Sie die erste Option **Momentaufnahmebericht zu Cloud Discovery erstellen** und dann **Weiter** aus. Hier tragen Sie die erforderlichen Details ein und laden Datenverkehrsprotokolle hoch, um einen Bericht zu generieren und hochzuladen.  Wählen Sie **Beenden** aus, und wählen Sie erneut **Beenden** aus, wenn Sie gefragt werden, ob Sie sicher sind.  Die für Ihren Lab-Mandanten angezeigten Daten stammen aus einem Momentaufnahmebericht. Sie können diese Informationen oben im Cloud Discovery-Fenster anzeigen.
    1. Wählen Sie zum Anzeigen der Option für fortlaufende Berichte **Aktionen** in der oberen rechten Ecke der Seite aus, und wählen Sie im Dropdown den Eintrag **Automatischen Upload konfigurieren** aus.  Es sind keine Datenquellen verbunden. Hier würden Sie jedoch eine Datenquelle hinzufügen. Wählen Sie **Datenquelle hinzufügen** und dann den Dropdownpfeil im Feld **Appliance auswählen** aus, um die Appliancetypen anzuzeigen, die Sie als Datenquelle verbinden können.  Wählen Sie **Abbrechen** aus, um den Vorgang zu beenden.
    1. Wählen Sie im linken Navigationsbereich **Cloud Discovery** aus, um zur Seite „Cloud Discovery“ zurückzukehren.

1. Mit Microsoft 365 Defender for Cloud-Apps können Sie direkt eine Verbindung mit Apps herstellen, indem Sie App-Connectors festlegen, die Ihnen eine bessere Sichtbarkeit und Kontrolle über Ihre Cloud-Apps ermöglichen.  Ein wichtiger Punkt, den Sie beachten sollten, ist die Dokumentation zu den Voraussetzungen für das Verbinden bestimmter App-Connectors. Wählen Sie in der oberen rechten Ecke des Bildschirms **Aktionen** und dann **Cloud Discovery-Einstellungen** aus.  Wählen Sie auf der linken Seite des Bildschirms unter „Verbundene Apps“ die Option **App-Connectors** aus.  
    1. Wählen Sie auf der Seite „Verbundene Apps“ in der Liste *Office 365** aus, um ausführliche Informationen anzuzeigen. Wenn für Office 365 ein Verbindungsfehler angezeigt wird, liegt dies höchstwahrscheinlich daran, dass die Option für Überwachung nicht aktiviert ist.  Wenn Überwachung aktiviert ist, wechseln Sie zu den vertikalen Auslassungspunkten auf der rechten Seite des Zeilenelements, und wählen Sie dann **Einstellungen bearbeiten** aus.  Um die Verbindung erneut herzustellen, wählen Sie am unteren Rand der Seite **Office 365 verbinden** aus. Auf der Seite sollte nun angezeigt werden, dass Office 365 verbunden ist. Wählen Sie **Fertig** aus.  Der Status wird nun mit einem gelben Warnzeichen angezeigt, das angibt, dass kein aktueller Status vorhanden ist.  Es dauert einige Zeit, bis der Status aktualisiert wird, da sich der Zeitraum für die rückwirkende Überprüfung je nach App unterscheidet und für Lab-Mandanten möglicherweise Verzögerungen auftreten, die länger als normale Verzögerungen sind (erwarten Sie nicht, dass sich der Status während der Demo ändert, da dies viele Stunden dauern kann).
    1. Jetzt richten Sie einen neuen App-Connector ein.  Wählen Sie **+ App verbinden** aus. Wählen Sie dann in der Dropdownliste den Eintrag **Microsoft Azure** aus.  Wählen Sie im Microsoft Azure-Popupfenster **Mit Microsoft Azure verbinden** und dann **Fertig** aus.  Sie sehen einen Status „Verbunden“ (wenn dieser nicht angezeigt wird, aktualisieren Sie den Browser) und Informationen zum Überprüfen von Benutzern, Daten und Aktivitäten.  Kehren Sie zum Cloud Discovery-Dashboard zurück, indem Sie im Navigationsbereich ganz links **Cloud Discovery** auswählen.

1. Lassen Sie diese Seite geöffnet, da Sie sie im nächsten Teil verwenden werden.

### <a name="demo-part-2---explore-the-cloud-app-catalog"></a>Teil 2 der Demo: Erkunden des Cloud-App-Katalogs

In diesem Teil der Demo zeigen Sie die Funktionen des Cloud-App-Katalogs. Cloud Discovery analysiert Ihre Datenverkehrsprotokolle im Abgleich mit dem Cloud-App-Katalog von Microsoft Defender for Cloud-Apps, der mehr als 31.000 Cloud-Apps enthält. Die Apps werden nach über 80 Risikofaktoren bewertet, damit Sie laufende Einblicke in die Verwendung der Cloud, die Schatten-IT und die Risiken haben, die die Schatten-IT für Ihre Organisation darstellt.  

1. Wählen Sie im linken Navigationsbereich **Cloud-App-Katalog** aus.

1. Mithilfe des Cloud-App-Katalogs können Sie auswählen, welche App den Sicherheitsanforderungen Ihrer Organisation gerecht wird. Administratoren können grundlegende Filterung von Apps durchführen, wie oben auf der Seite gezeigt. Dazu gehört, ob die App sanktioniert bzw. unsanktioniert ist oder kein Tag, keine Risikobewertung, keinen Compliancerisikofaktor und keinen Sicherheitsrisikofaktor aufweist.  Wenn Sie beispielsweise nach dem Compliancerisikofaktor filtern, können Sie nach bestimmten Standards, Zertifizierungen und Compliancevorgaben suchen, die die App möglicherweise erfüllt. Dazu zählen beispielsweise HIPAA, ISO 27001, SOC 2 und PCI-DSS. Wählen Sie **Kompatibilitätsrisikofaktor** aus, um die verfügbaren Optionen anzuzeigen.  Sie können weiter nach Risikobewertung filtern, indem Sie die Schieberegler für die Risikobewertung oben auf der Seite verwenden. Wenn Sie den Regler verschoben haben, stellen Sie sicher, dass Sie ihn so festgelegt haben, dass der Bereich auf 0 bis 10 festgelegt ist.

1. Administratoren können auch nach Apps nach Kategorie suchen.  Geben Sie z. B. im Feld zum Suchen nach Kategorie **Soziales Netzwerk** ein, und wählen Sie dann **Soziales Netzwerk** aus.  Wählen Sie **Yammer** aus, um eine detaillierte Ansicht anzuzeigen.  Wenn Sie mit dem Mauszeiger auf Themen für eine bestimmte Kategorie zeigen, wird ein Informationssymbol angezeigt, das Sie auswählen können, um weitere Informationen zum jeweiligen Thema zu erhalten.

1. Lassen Sie diese Seite geöffnet, da Sie sie in der nächsten Aufgabe verwenden werden.

### <a name="demo-part-3---explore-the-activity-log-and-files"></a>Teil 3 der Demo: Erkunden des Aktivitätsprotokolls und der -dateien

Erkunden Sie Möglichkeiten, die aufgezeichneten Aktivitäten mit dem Aktivitätsprotokoll und den -dateien zu untersuchen.

1. Wählen Sie im linken Navigationsbereich die Option **Dateien** aus, und erkunden Sie sie. Beachten Sie die Optionen zum Filtern von Daten nach App, Besitzer, Zugriffsebene, Dateityp und übereinstimmender Richtlinie. Beachten Sie auch die Option zum Erstellen einer neuen Richtlinie aus der Suche und dem Export der Daten.
    1. Wählen Sie **+Neue Richtlinie aus Suche** aus.  Beachten Sie, wie Sie eine Richtlinie anhand einer Vorlage erstellen, einen Schweregrad und die Kategorie der Richtlinie auswählen, Filter für die Richtlinie erstellen, Warnungen erstellen und sogar Warnungen an Power Automate senden können.  Wählen Sie **Abbrechen** aus, um das Fenster für die Richtlinienerstellung zu beenden, und wählen Sie dann **Seite verlassen** aus.

1. Wählen Sie im linken Navigationsbereich **Aktivitätsprotokoll** aus. Hier können Sie alle Aktivitäten im Zusammenhang mit Ihren verbundenen Apps anzeigen. Möglicherweise werden keine Daten aufgelistet, da es mehrere Stunden dauern kann, rückwirkende Überprüfungen durchzuführen, nachdem Überwachung aktiviert wurde, und für Lab-Mandanten möglicherweise Verzögerungen auftreten, die länger als normal sind. Beachten Sie die verfügbaren Filteroptionen und die Option zum Erstellen einer neuen Richtlinie aus der Suche.

1. Lassen Sie diese Seite geöffnet, da Sie sie in der nächsten Aufgabe verwenden werden.

### <a name="demo-part-4---explore-policies"></a>Teil 4 der Demo: Erkunden von Richtlinien

In diesem Teil zeigen Sie die Optionen, die für Richtlinien in Microsoft Defender for Cloud-Apps verfügbar sind.

1. Wählen Sie im linken Navigationsbereich **Richtlinien** und dann **Richtlinienverwaltung** aus.  Die aufgelisteten Richtlinien umfassen Informationen zur Anzahl der von der Richtlinie generierten Warnungen, zum Schweregrad usw. Durch Auswahl eines Elements werden ausführlichere Informationen zur Richtlinie angezeigt. Wählen Sie ein Element aus der Liste aus, beispielsweise **Riskante Anmeldung**.
    1. Beachten Sie, dass Sie auch eine Richtlinie erstellen können. Wählen Sie **+ Richtlinie erstellen** aus, um die Richtlinientypen anzuzeigen, die Sie erstellen können.  Wählen Sie **Aktivitätsrichtlinie** aus, um die verschiedenen Optionen anzuzeigen, die zum Erstellen der Richtlinie verfügbar sind.  Wählen Sie **Abbrechen** aus, um das Konfigurationsfenster zu schließen.
    1. Beachten Sie, dass Sie auch die Möglichkeit haben, Richtlinieninformationen zu exportieren.

1. Wählen Sie im linken Navigationsbereich **Richtlinienvorlagen** aus. Um eine Richtlinie aus einer der verfügbaren Vorlagen zu erstellen, wählen Sie **+** auf der linken Seite des Vorlagenzeilenelements aus.  Zeigen Sie die verschiedenen Konfigurationsoptionen für die Richtlinie an.  Wählen Sie **Abbrechen** aus, um die Seite zu schließen.

1. Schließen Sie das Browserfenster.

### <a name="review"></a>Überprüfung

In dieser Demo haben Sie die Funktionen von Microsoft Defender für Cloud-Apps angezeigt.  Sie haben die Informationen gezeigt, die im Cloud Discovery-Dashboard verfügbar sind, den Cloud App-Katalog, die Möglichkeiten zur Untersuchung der Ergebnisse mit dem Aktivitätsprotokoll und Dateien sowie die Möglichkeiten zur Kontrolle der Auswirkungen auf Ihr Unternehmen mithilfe von Richtlinien.
