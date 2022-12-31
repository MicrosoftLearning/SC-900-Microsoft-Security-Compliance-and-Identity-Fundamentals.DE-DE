<a name="---"></a><!---
---
Lab: Title: 'Erkunden des Insider-Risikomanagements in Microsoft Purview' Learning Path/Module/Unit: 'Lernpfad: Beschreiben der Funktionen der Microsoft-Compliancelösungen; Modul 4: Beschreiben der Microsoft Purview-Funktionen für den Umgang mit Insider-Risiken; Lerneinheit 2: Beschreiben des Insider-Risikomanagements'
---
--->

# <a name="lab-explore-insider-risk-management-in-microsoft-purview"></a>Lab: Erkunden des Insider-Risikomanagements in Microsoft Purview

Dieses Lab ist den folgenden Learn-Inhalten zugeordnet:

- Lernpfad: Beschreiben der Funktionen der Microsoft-Compliancelösungen
- Modul: Beschreiben der Microsoft Purview-Funktionen für den Umgang mit Insider-Risiken
- Lerneinheit: Beschreiben des Insider-Risikomanagements

## <a name="lab-scenario"></a>Labszenario

In diesem Lab gehen Sie den Einstellungsprozess einer Insider-Risikorichtlinie und die grundlegenden Voraussetzungen zum Konfigurieren und Verwenden von Insider-Risikomanagementrichtlinien durch.  Hinweis: Dieses Lab umfasst Informationen zum Einrichten des Insider-Risikomanagements und zu den Optionen für das Erstellen einer Richtlinie.  In diesem Lab ist keine Aufgabe zum Auslösen der Richtlinie enthalten, da die Anzahl der Ereignisse, die zum Auslösen einer Richtlinie erforderlich sind, und die erforderliche Zeit den Rahmen dieser Übung überschreiten.

**Geschätzte Dauer**: 45-60 Minuten

### <a name="task-1"></a>Aufgabe 1

Bei dieser Aufgabe aktivieren Sie als globaler Administrator Berechtigungen für das Insider-Risikomanagement.  Insbesondere fügen Sie dabei der Rollengruppe „Insider-Risikomanagement“ Benutzer hinzu, um sicherzustellen, dass die vorgesehenen Benutzer auf die Funktion „Insider-Risikomanagement“ zugreifen und diese verwenden können.  Es kann bis zu 30 Minuten dauern, bis die Rollengruppenberechtigungen auf die Benutzer in der gesamten Organisation angewendet werden.

1. Öffnen Sie Microsoft Edge. Geben Sie **admin.microsoft.com** in die Adressleiste ein.

1. Melden Sie sich mit Ihren Administratoranmeldeinformationen an.
    1. Geben Sie **admin@WWLxZZZZZZ.onmicrosoft.com** (ZZZZZZ ist hierbei die eindeutige Mandanten-ID, die von Ihrem Lab-Hostinganbieter bereitgestellt wurde) in das Fenster „Anmelden“ ein, und wählen Sie dann **Weiter** aus.

    1. Geben Sie das Administratorkennwort ein, das von Ihrem Lab-Hostinganbieter bereitgestellt werden sollte. Wählen Sie **Anmelden**.
    1. Wählen Sie **Ja** aus, wenn Sie gefragt werden, ob Sie angemeldet bleiben möchten. Dadurch gelangen Sie zur Seite „Microsoft 365 Admin Center“.

1. Wählen Sie im linken Navigationsbereich von Microsoft 365 Admin Center **Alle anzeigen** aus.

1. Wählen Sie unter „Admin Center“ die Option **Compliance** aus.  Die Startseite des Microsoft Purview-Complianceportals wird auf einer neuen Browserseite geöffnet.  

1. Wählen Sie im linken Navigationsbereich des Microsoft Purview-Complianceportals **Berechtigungen** aus.

1. Wählen Sie auf der Seite „Berechtigungen und Rollen“ unter „Microsoft Purview-Lösungen“ die Option **Rollen** aus.

1. Geben Sie **Insider-Risiko** in die Suchleiste ein. Wählen Sie dann das Suchsymbol (Vergrößerungsglas) aus.  Beachten Sie die zahlreichen Rollen, die angezeigt werden.  Diese weisen jeweils unterschiedliche Zugriffsebenen auf.  Wählen Sie **Insider-Risikomanagement** aus, und überprüfen Sie die Beschreibung.  Scrollen Sie nach unten, bis Mitglieder angezeigt werden, und beachten Sie, dass „MOD Administrator“ und „Megan Bowen“ aufgeführt werden. Klicken Sie unten im Fenster auf **Schließen**.

1. Wählen Sie im linken Navigationsbereich die **Startseite** aus, um zur Microsoft Purview-Complianceportalseite zurückzukehren.

1. Lassen Sie diese Browserregisterkarte geöffnet, da Sie in einer nachfolgenden Aufgabe zu ihr zurückkehren werden.

### <a name="task-2-skip-if-you-did-the-setup-lab-task-to-enable-the-audit-log"></a>Aufgabe 2 (ÜBERSPRINGEN Sie sie, falls Sie die Aufgabe „Lab einrichten“ zum Aktivieren des Überwachungsprotokolls absolviert haben)

Das Insider-Risikomanagement verwendet Microsoft 365-Überwachungsprotokolle für Benutzererkenntnisse und -aktivitäten in Richtlinien und Analyseerkenntnisse. Bei dieser Aufgabe aktivieren Sie die Funktion „Überwachungsprotokollsuche“. Hinweis:  Nach der Aktivierung der Überwachungsprotokollsuche kann es mehrere Stunden dauern, bis beim Durchsuchen des Überwachungsprotokolls Ergebnisse zurückgegeben werden.  Obwohl es mehrere Stunden dauern kann, bis Sie das Überwachungsprotokoll durchsuchen können, wirkt sich dies nicht auf die Fähigkeit aus, andere Aufgabe in diesem Lab abzuschließen.

1. Wählen Sie die Browserregisterkarte mit der Bezeichnung **Startseite – Microsoft 365 Compliance** aus.  Wenn Sie diese Browserregisterkarte zuvor geschlossen haben, öffnen Sie Microsoft Edge, und geben Sie **compliance.microsoft.com** in die Adressleiste ein. Melden Sie sich dann mit Ihren Administratoranmeldeinformationen an.

1. Wählen Sie im linken Navigationsbereich unter „Lösungen“ die Option **Überwachen** aus.

1. Stellen Sie sicher, dass die Registerkarte **Suche** ausgewählt (unterstrichen) ist.

1. Warten Sie zwei bis drei Minuten, nachdem Sie zur Seite „Überwachen“ gelangt sind.  Wenn Überwachung NICHT aktiviert ist, wird oben auf der Seite ein blauer Balken mit der Meldung „Aufzeichnung von Benutzer- und Administratoraktivitäten starten“ angezeigt.  Wählen Sie **Aufzeichnung von Benutzer- und Administratoraktivitäten starten** aus.  Sobald die Überwachung aktiviert ist, wird der blaue Balken nicht mehr angezeigt.  Wird der blaue Balken nicht angezeigt, ist Überwachung bereits aktiviert, und keine weitere Aktion ist erforderlich.

1. Wählen Sie im linken Navigationsbereich die **Startseite** aus, um zur Startseite des Microsoft Purview-Complianceportals zurückzukehren.

1. Lassen Sie diese Browserregisterkarte geöffnet, da Sie sie in der nächsten Aufgabe verwenden werden.

### <a name="task-3"></a>Aufgabe 3

Bei dieser Aufgabe gehen Sie die Einstellungen der Insider-Risikomanagement-Lösung durch.  Die Einstellungen für das Insider-Risikomanagement gelten für alle Richtlinien für das Insider-Risikomanagement, unabhängig davon, welche Vorlage Sie beim Erstellen einer Richtlinie auswählen.

1. Sie sollten sich auf der Startseite des Microsoft Purview-Complianceportals befinden. Falls nicht, öffnen Sie die Browserregisterkarte **Startseite – Microsoft 365 Compliance**.

1. Wählen Sie im linken Navigationsbereich unter „Lösungen“ die Option **Insider-Risikomanagement** aus.

1. Bevor Sie mit dem Einrichten einer Richtlinie beginnen, gibt es einige Einstellungen, mit denen ein Administrator vertraut sein sollte und die nach Bedarf für seine Organisation konfiguriert werden. Wählen Sie auf der Seite „Insider-Risikomanagement“ das **Zahnradsymbol** in der oberen rechten Ecke des Fensters „Insider-Risikomanagement“ aus, um auf die Einstellungen für das Insider-Risiko zuzugreifen.  
    1. Überprüfen Sie, ob Sie sich auf der Registerkarte **Datenschutz** befinden: Für Benutzer, die Aktivitäten ausführen, die Ihren Insiderrisikorichtlinien entsprechen, bestimmt diese Einstellung, ob ihre tatsächlichen Namen angezeigt oder anonymisierte Versionen verwendet werden sollen, um ihre Identitäten zu maskieren.  Für diese exemplarische Vorgehensweise können Sie die Standardeinstellung beibehalten.
    1. Wählen Sie die Registerkarte **Richtlinienindikatoren** aus. Wenn eine Richtlinie ausgelöst wird, werden den ausgewählten Indikatoren zugeordnete Aktivitäten verwendet, um die Risikobewertung für den Benutzer zu bestimmen. Die hier ausgewählten Richtlinienindikatoren werden in Vorlagen für die Insider-Risikorichtlinie aufgenommen.  Scrollen Sie, um alle verfügbaren Indikatoren und die zugehörigen Informationen anzuzeigen. Wählen Sie unter **Office-Indikatoren** die Option **Alle auswählen** und dann unten auf der Seite **Speichern** aus (Sie müssen nach unten scrollen).
    1. Wählen Sie die Registerkarte **Richtlinien-Zeitrahmen** aus. Die von Ihnen hier ausgewählten Zeitrahmen treten für einen Benutzer in Kraft, wenn er eine Übereinstimmung für eine Insider-Risikorichtlinie auslöst.   Im Fenster „Aktivierung“ wird festgelegt, wie lange Richtlinien aktiv Aktivitäten für Benutzer erkennen und ausgelöst werden, wenn ein Benutzer die erste Aktivität ausführt, die mit einer Richtlinie übereinstimmt. Mit „Bisherige Aktivitätserkennung“ wird festgelegt, wie weit eine Richtlinie zurückreichen soll, um Benutzeraktivitäten zu erkennen, und wird ausgelöst, wenn ein Benutzer die erste Aktivität ausführt, die mit einer Richtlinie übereinstimmt.  Lassen Sie die Standardwerte unverändert.
    1. Wählen Sie die Registerkarte **Intelligente Erkennungen** aus. Überprüfen Sie die hier vorhandenen Optionen.  Beachten Sie die Domäneneinstellungen und wie sie mit den Indikatoren zusammenhängen.
    1. Erkunden Sie die anderen Elemente, die in den Einstellungen aufgeführt sind, und beachten Sie, dass sich viele in der Vorschau befinden.

1. Wählen Sie in der oberen linken Ecke der Seite oberhalb von „Einstellungen“ die Option **Insider-Risikomanagement** aus, um zur Übersicht über Insider-Risikomanagement zurückzukehren.

1. Lassen Sie diese Browserregisterkarte geöffnet, da Sie sie in der nächsten Aufgabe verwenden werden.

### <a name="task-4"></a>Aufgabe 4

In dieser Aufgabe gehen Sie die Einstellungen zum Erstellen einer Richtlinie durch.  Das Ziel besteht einfach darin, ein Gefühl für die verschiedenen Optionen und die Flexibilität zu erhalten, die mit der Erstellung einer Richtlinie verbunden sind.

1. Sie sollten sich auf der Seite „Insider-Risikomanagement“ befinden.  Falls Sie noch nicht dort sind, öffnen Sie die Browserregisterkarte mit der Bezeichnung **Insider-Risikomanagement – Microsoft 365 Compliance**.

1. Wählen Sie auf der Übersichtsseite für das Insider-Risikomanagement die Registerkarte **Richtlinien** und dann **+ Erstellen** aus.  Konfigurieren Sie jede der folgenden Registerkarten für Richtlinien.

    1. Richtlinienvorlage: Wählen Sie unter der Kategorie „Datenlecks“ die Option **Datenlecks** aus.  Lesen Sie die Details für diese Vorlage. Unter Voraussetzungen wird die DLP-Richtlinie mit einem Häkchen in einem grünen Kreis angezeigt, um anzugeben, dass die Voraussetzung erfüllt ist.  Es gibt eine DLP-Richtlinie, die für diesen Lab-Mandanten vorkonfiguriert wurde. Wählen Sie **Weiter** aus. 
    1. Name und Beschreibung: Geben Sie den Namen **SC900-InsiderRiskPolicy** ein, und wählen Sie dann **Weiter** aus.
    1. Benutzer und Gruppen:  Lesen Sie das Informationsfeld.  Übernehmen Sie die Standardeinstellung **Alle Benutzer und Gruppen aufnehmen**.  Klicken Sie auf **Weiter**.
    1. Zu priorisierende Inhalte: Laut Beschreibung werden die Risikobewertungen für jede Aktivität erhöht, die Prioritätsinhalte enthält, was wiederum die Wahrscheinlichkeit erhöht, eine Warnung mit hohem Schweregrad zu generieren. Der Einfachheit halber wählen Sie **Ich möchte Inhalte jetzt nicht priorisieren** aus, und wählen Sie dann **Weiter** aus.
    1. Entscheiden Sie, ob nur Aktivitäten mit Prioritätsinhalt bewertet werden sollen: Belassen Sie die Standardeinstellung **Warnungen für alle Aktivitäten abrufen**, und wählen Sie dann **Weiter** aus.
    1. Trigger: Das auslösende Ereignis bestimmt, wann eine Richtlinie beginnt, der Aktivität eines Benutzers Risikobewertungen zuzuweisen.  Sie können eine vorhandene DLP-Richtlinie auswählen oder ob der Benutzer eine Exfiltrationsaktivität ausführen soll. Wählen Sie **Benutzer entspricht einer DLP-Richtlinie** aus, und wählen Sie dann in der Dropdownliste **U.S. Financial Data** aus. Wählen Sie **Weiter** aus.
    1. Indikatoren: Beachten Sie, dass alle Office-Indikatoren, die Sie in der vorherigen Aufgabe ausgewählt haben, ausgewählt sind (Sie können dies erkennen, indem Sie die NACH-UNTEN-PFEILTASTE neben Office-Indikatoren auswählen), und wählen Sie dann **Weiter** aus.
    1. Behalten Sie auf der Seite „Erkennungsoptionen“ alle Standardeinstellungen bei, lesen Sie aber die Beschreibung, die den verschiedenen Optionen zugeordnet ist, und zeigen Sie auf das Informationssymbol, um ausführlichere Informationen zu einer bestimmten Einstellung zu erhalten.  Wählen Sie **Weiter** aus.
    1. Behalten Sie auf der Seite zum Entscheiden, ob Standard- oder Kundenindikator-Schwellenwerte verwendet werden sollen, die Standardeinstellung **Standardschwellenwerte** bei, und wählen Sie dann **Weiter** aus.
    1. Fertigstellen: Überprüfen Sie die Einstellungen, wählen Sie **Senden** und dann **Fertig** aus.

1. Sie befinden sich wieder auf der Registerkarte „Richtlinien“ der Seite „Insider-Risikomanagement“.  Die von Ihnen erstellte Richtlinie wird aufgelistet.  Wenn sie nicht angezeigt wird, wählen Sie das Symbol **Aktualisieren** aus.

1. Als Administrator können Sie sofort damit beginnen, Benutzern Risikobewertungen basierend auf Aktivitäten zuzuweisen, die von den von Ihnen ausgewählten Richtlinien erkannt wurden. Dadurch wird die Anforderung umgangen, dass zuerst ein auslösendes Ereignis (z. B. eine DLP-Richtlinienentsprechung) erkannt wird.  Ein Administrator wählt dazu das leere Quadrat neben dem Richtliniennamen aus, um die Richtlinie auszuwählen. Wählen Sie dann die oberhalb der Tabelle mit den Richtlinien angezeigte Option **Bewertungsaktivität für Benutzer starten** aus.  Ein neues Fenster wird geöffnet, in dem der Administrator die verfügbaren Felder mit Daten auffüllen muss. Lassen Sie die Felder leer, da Sie diese Option nicht konfigurieren. Wenn Sie weitere Informationen dazu erhalten möchten, warum ein Administrator so vorgehen möchte, wählen Sie **Warum sollte ich so vorgehen?** aus.  Schließen Sie das Fenster, indem Sie in der oberen rechten Ecke des Bildschirms das **X** auswählen.

1. Schließen Sie alle geöffneten Browserregisterkarten.

### <a name="review"></a>Überprüfung

In diesem Lab sind Sie den Einstellungsprozess einer Insider-Risikorichtlinie und die grundlegenden Voraussetzungen zum Konfigurieren und Verwenden von Insider-Risikomanagementrichtlinien durchgegangen.
