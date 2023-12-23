<!---
---
Lab: Title: 'Erkunden des Insider-Risikomanagements in Microsoft Purview' Learning Path/Module/Unit: 'Lernpfad: Beschreiben der Funktionen der Microsoft-Compliancelösungen; Modul 4: Beschreiben der Microsoft Purview-Funktionen für den Umgang mit Insider-Risiken; Lerneinheit 2: Beschreiben des Insider-Risikomanagements'
---
--->

# Lab: Erkunden des Insider-Risikomanagements in Microsoft Purview

Dieses Lab ist den folgenden Learn-Inhalten zugeordnet:

- Lernpfad: Beschreiben der Funktionen der Microsoft-Compliancelösungen
- Modul: Beschreiben der Microsoft Purview-Funktionen für den Umgang mit Insider-Risiken
- Lerneinheit: Beschreiben des Insider-Risikomanagements

## Labszenario

In diesem Lab gehen Sie den Einstellungsprozess einer Insider-Risikorichtlinie und die grundlegenden Voraussetzungen zum Konfigurieren und Verwenden von Insider-Risikomanagementrichtlinien durch.  Hinweis: Dieses Lab umfasst Informationen zum Einrichten des Insider-Risikomanagements und zu den Optionen für das Erstellen einer Richtlinie.  In diesem Lab ist keine Aufgabe zum Auslösen der Richtlinie enthalten, da die Anzahl der Ereignisse, die zum Auslösen einer Richtlinie erforderlich sind, und die erforderliche Zeit den Rahmen dieser Übung überschreiten.

**Geschätzte Dauer**: 45 bis 60 Minuten

### Aufgabe 1

Bei dieser Aufgabe aktivieren Sie als globale*r Administrator*in Berechtigungen für das Insider-Risikomanagement.  Insbesondere fügen Sie dabei der Rollengruppe „Insider-Risikomanagement“ Benutzer hinzu, um sicherzustellen, dass die vorgesehenen Benutzer auf die Funktion „Insider-Risikomanagement“ zugreifen und diese verwenden können.  Es kann bis zu 30 Minuten dauern, bis die Rollengruppenberechtigungen für Benutzer in der gesamten Organisation gelten.

1. Öffnen Sie die Browserregisterkarte für die Startseite von Microsoft Purview.  Wenn Sie die Registerkarte zuvor geschlossen haben, öffnen Sie eine neue Browserregisterkarte, und geben Sie **https://admin.microsoft.com** ein. Melden Sie sich mit den Administratoranmeldeinformationen für den Microsoft 365-Mandanten an, der vom autorisierten Labhoster (ALH) bereitgestellt wird. Wählen Sie im linken Navigationsbereich von Microsoft 365 Admin Center **Alle anzeigen** und dann **Compliance** aus.  Die Startseite des Microsoft Purview-Complianceportals wird auf einer neuen Browserseite geöffnet.  

1. Erweitern Sie im linken Navigationsbereich **Rollen & Bereiche**, und wählen Sie dann **Berechtigungen** aus.

1. Wählen Sie unter Microsoft Purview-Lösungen die Option **Rollen** aus.

1. Geben Sie im Suchfeld **Insider-Risiko** ein, und drücken Sie dann die ENTER auf der Tastatur.  Beachten Sie die zahlreichen Rollen, die angezeigt werden.  Jeder dieser Elemente weist unterschiedliche Zugriffsebenen auf.  Wählen Sie **Insider-Risikomanagement** aus, und überprüfen Sie die Beschreibung.  Scrollen Sie nach unten, bis Mitglieder angezeigt werden, und beachten Sie, dass „MOD Administrator“ und „Megan Bowen“ aufgeführt werden. Schließen Sie das Fenster, indem Sie in der oberen rechten Ecke des Bildschirms das **X** auswählen.

1. Wählen Sie im linken Navigationsbereich die **Startseite** aus, um zur Microsoft Purview-Complianceportalseite zurückzukehren.

1. Lassen Sie diese Browserregisterkarte geöffnet, da Sie in einer nachfolgenden Aufgabe zu ihr zurückkehren werden.

### Aufgabe 2 (HINWEIS: ÜBERSPRINGEN Sie Aufgabe 2, falls Sie die Aufgabe „Lab einrichten“ zum Aktivieren des Überwachungsprotokolls absolviert haben.)

Es empfiehlt sich, diese Funktion zu aktivieren, da Microsoft 365 Überwachungsprotokolle für Benutzererkenntnisse und -aktivitäten in Richtlinien und Analyseerkenntnissen verwendet. Bei dieser Aufgabe aktivieren Sie die Funktion „Überwachungsprotokollsuche“. Hinweis: Es kann einige Stunden dauern, nachdem Sie die Audit-Protokoll-Suche eingeschaltet haben, bis Sie bei der Suche im Audit-Protokoll Ergebnisse zurückgeben können.  Obwohl es mehrere Stunden dauern kann, bis Sie das Überwachungsprotokoll durchsuchen können, wirkt sich dies nicht auf die Möglichkeit aus, andere Aufgaben in diesem Lab auszuführen.

1. Wählen Sie die Browserregisterkarte mit der Bezeichnung **Startseite – Microsoft 365 Compliance** aus.  Wenn Sie diese Browserregisterkarte zuvor geschlossen haben, öffnen Sie Microsoft Edge, und geben Sie **compliance.microsoft.com** in die Adressleiste ein. Melden Sie sich dann mit Ihren Administratoranmeldeinformationen an.

1. Wählen Sie im linken Navigationsbereich **Audit** aus.

1. Stellen Sie sicher, dass die Registerkarte **Neue Suche** ausgewählt (unterstrichen) ist.

1. Sobald Sie auf der Seite "Überwachung" landen, warten Sie 2-3 Minuten.  Wenn Überwachung NICHT aktiviert ist, wird oben auf der Seite ein blauer Balken mit der Meldung „Aufzeichnung von Benutzer- und Administratoraktivitäten starten“ angezeigt.  Wählen Sie **Aufzeichnung von Benutzer- und Administratoraktivitäten starten** aus.  Sobald die Überwachung aktiviert ist, wird die blaue Leiste ausgeblendet.  Wird der blaue Balken nicht angezeigt, ist Überwachung bereits aktiviert, und keine weitere Aktion ist erforderlich.

1. Wählen Sie im linken Navigationsbereich die **Startseite** aus, um zur Startseite des Microsoft Purview-Complianceportals zurückzukehren.

1. Lassen Sie diese Browserregisterkarte geöffnet, da Sie sie in der nächsten Aufgabe verwenden werden.

### Aufgabe 3

Bei dieser Aufgabe gehen Sie die Einstellungen der Insider-Risikomanagement-Lösung durch.  Insider-Risikomanagementeinstellungen gelten für alle Insider-Risikomanagementrichtlinien, unabhängig von der Vorlage, die Sie beim Erstellen einer Richtlinie auswählen.

1. Sie sollten sich auf der Startseite des Microsoft Purview-Complianceportals befinden. Wenn nicht, wählen Sie die Browserregisterkarte  **Home - Microsoft 365 Compliance** aus.

1. Wählen Sie im linken Navigationsbereich unter "Lösungen" die Option "**Insider-Risikomanagement** aus.

1. Bevor Sie mit dem Einrichten einer Richtlinie beginnen, gibt es einige Einstellungen, mit denen ein Administrator vertraut sein sollte und die nach Bedarf für seine Organisation konfiguriert werden. Wählen Sie auf der Seite „Insider-Risikomanagement“ das **Zahnradsymbol** in der oberen rechten Ecke des Fensters „Insider-Risikomanagement“ aus, um auf die Einstellungen für das Insider-Risiko zuzugreifen.  
    1. Überprüfen Sie, ob Sie sich auf der Registerkarte **Datenschutz** befinden: Für Benutzer, die Aktivitäten ausführen, die Ihren Insiderrisikorichtlinien entsprechen, bestimmt diese Einstellung, ob ihre tatsächlichen Namen angezeigt oder anonymisierte Versionen verwendet werden sollen, um ihre Identitäten zu maskieren.  Für diese exemplarische Vorgehensweise können Sie die Standardeinstellung beibehalten.
    1. Wählen Sie die Registerkarte **Richtlinienindikatoren** aus. Sobald ein Richtlinie ausgelöstes Ereignis auftritt, werden Aktivitäten, die den ausgewählten Indikatoren zugeordnet sind, bei der Ermittlung der Risikobewertung für den Benutzer verwendet. Hier ausgewählte Richtlinienindikatoren sind die Vorlagen für Insider-Risikorichtlinien enthalten.  Scrollen Sie, um alle verfügbaren Indikatoren und alle zugehörigen Informationen anzuzeigen. Wählen Sie unter **Office-Indikatoren** die Option **Alle auswählen** und dann unten auf der Seite **Speichern** aus (Sie müssen nach unten scrollen).
    1. Wählen Sie die Registerkarte **Richtlinienzeitrahmen** aus. Die hier ausgewählten Zeitrahmen werden für eine*n Benutzer*in wirksam, wenn er eine Übereinstimmung für eine Insider-Risikorichtlinie auslöst.   Das Aktivierungsfenster bestimmt, wie lange Richtlinien Aktivitäten für Benutzer*innen aktiv erkennen und ausgelöst werden, wenn ein*e Benutzer*in die erste Aktivität ausführt, die einer Richtlinie entspricht. Die Erkennung früherer Aktivitäten bestimmt, wie weit eine Richtlinie zurückgeht, um Benutzeraktivitäten zu erkennen und ausgelöst wird, wenn ein*e Benutzer*in die erste Aktivität ausführt, die einer Richtlinie entspricht.  Lassen Sie die Standardwerte unverändert.
    1. Wählen Sie die Registerkarte **Intelligente Erkennungen** aus. Überprüfen Sie hier die Optionen.  Beachten Sie die Domänen-Einstellungen und ihre Beziehung zu den Indikatoren.
    1. Erkunden Sie die anderen Elemente, die in den Einstellungen aufgeführt sind, und beachten Sie, dass sich viele in der Vorschau befinden.

1. Um zur Übersicht über das Insider-Risikomanagement zurückzukehren, wählen Sie **Insider-Risikomanagement** in der oberen linken Ecke der Seite aus, oben, wo Einstellungen steht.

1. Lassen Sie diese Browserregisterkarte geöffnet, da Sie sie in der nächsten Aufgabe verwenden werden.

### Aufgabe 4

In dieser Aufgabe gehen Sie die Einstellungen zum Erstellen einer Richtlinie durch.  Das Ziel besteht einfach darin, ein Gefühl für die verschiedenen Optionen und die Flexibilität zu erhalten, die mit der Erstellung einer Richtlinie verbunden sind.

1. Sie sollten sich auf der Seite "Insider-Risikomanagement" befinden.  Falls noch nicht vorhanden, öffnen Sie die Registerkarte "Browser" mit der Bezeichnung **Insider-Risikomanagement – Microsoft 365 Compliance**.

1. Wählen Sie auf der Übersichtsseite für das Insider-Risikomanagement die Registerkarte **Richtlinien** und dann **+ Erstellen** aus.  Konfigurieren Sie jede der folgenden Richtlinienregisterkarten.

    1. Richtlinienvorlage: Wählen Sie unter der Kategorie „Datenlecks“ die Option **Datenlecks** aus.  Lesen Sie die Details für diese Vorlage. Unter Voraussetzungen wird die DLP-Richtlinie mit einem Häkchen in einem grünen Kreis angezeigt, um anzugeben, dass die Voraussetzung erfüllt ist.  Es gibt eine DLP-Richtlinie, die für diesen Lab-Mandanten vorkonfiguriert wurde. Wählen Sie **Weiter** aus. 
    1. Name und Beschreibung: Geben Sie den Namen **SC900-InsiderRiskPolicy** ein, und wählen Sie dann **Weiter** aus.
    1. Benutzer*innen und Gruppen: Überprüfen Sie das Informationsfeld.  Behalten Sie die Standardeinstellung bei, **schließen Sie alle Benutzer*innen und Gruppen** ein.  Wählen Sie **Weiter** aus.
    1. Zu priorisierende Inhalte: Laut Beschreibung werden die Risikobewertungen für jede Aktivität erhöht, die Prioritätsinhalte enthält, was wiederum die Wahrscheinlichkeit erhöht, eine Warnung mit hohem Schweregrad zu generieren. Der Einfachheit halber wählen Sie **Ich möchte Inhalte jetzt nicht priorisieren** aus, und wählen Sie dann **Weiter** aus.
    1. Trigger: Das auslösende Ereignis bestimmt, wann eine Richtlinie beginnt, der Aktivität eines Benutzers Risikobewertungen zuzuweisen.  Sie können eine vorhandene DLP-Richtlinie auswählen oder ob der Benutzer eine Exfiltrationsaktivität ausführen soll. Wählen Sie **Benutzer entspricht einer DLP-Richtlinie** aus, und wählen Sie dann in der Dropdownliste **U.S. Financial Data** aus. Wählen Sie **Weiter** aus.
    1. Indikatoren: Beachten Sie, dass alle Office-Indikatoren, die Sie in der vorherigen Aufgabe ausgewählt haben, ausgewählt sind (Sie können dies erkennen, indem Sie die NACH-UNTEN-PFEILTASTE neben Office-Indikatoren auswählen), und wählen Sie dann **Weiter** aus.
    1. Behalten Sie auf der Seite „Erkennungsoptionen“ alle Standardeinstellungen bei, lesen Sie aber die Beschreibung, die den verschiedenen Optionen zugeordnet ist, und zeigen Sie auf das Informationssymbol, um ausführlichere Informationen zu einer bestimmten Einstellung zu erhalten.  Wählen Sie **Weiter** aus.
    1. Behalten Sie auf der Seite zum Entscheiden, ob Standard- oder Kundenindikator-Schwellenwerte verwendet werden sollen, die Standardeinstellung **Standardschwellenwerte** bei, und wählen Sie dann **Weiter** aus.
    1. Fertigstellen: Überprüfen Sie die Einstellungen und wählen Sie **Senden** aus.
    1. Überprüfen Sie die Beschreibung, was als Nächstes geschieht, und wählen Sie dann **Fertig** aus.

1. Sie befinden sich wieder auf der Registerkarte „Richtlinien“ der Seite „Insider-Risikomanagement“.  Die von Ihnen erstellte Richtlinie wird aufgelistet.  Wenn sie nicht angezeigt wird, wählen Sie das Symbol **Aktualisieren** aus.

1. Als Administrator können Sie sofort damit beginnen, Benutzern Risikobewertungen basierend auf Aktivitäten zuzuweisen, die von den von Ihnen ausgewählten Richtlinien erkannt wurden. Dadurch wird die Anforderung umgangen, dass zuerst ein auslösendes Ereignis (z. B. eine DLP-Richtlinienentsprechung) erkannt wird.  Ein Administrator wählt dazu das leere Quadrat neben dem Richtliniennamen aus, um die Richtlinie auszuwählen. Wählen Sie dann die oberhalb der Tabelle mit den Richtlinien angezeigte Option **Bewertungsaktivität für Benutzer starten** aus.  Ein neues Fenster wird geöffnet, in dem der Administrator die verfügbaren Felder mit Daten auffüllen muss. Lassen Sie die Felder leer, da Sie diese Option nicht konfigurieren. Wenn Sie weitere Informationen dazu erhalten möchten, warum ein Administrator so vorgehen möchte, wählen Sie **Warum sollte ich so vorgehen?** aus.  Schließen Sie das Fenster, indem Sie in der oberen rechten Ecke des Bildschirms das **X** auswählen.

1. Wählen Sie im linken Navigationsbereich die **Zielseite** aus, um zur Startseite des Microsoft Purview-Complianceportals zurückzukehren.

1. Lassen Sie die Browserregisterkarte geöffnet.

### Überprüfung

In diesem Lab gehen Sie den Einstellungsprozess einer Insider-Risikorichtlinie und die grundlegenden Voraussetzungen zum Konfigurieren und Verwenden von Insider-Risikomanagementrichtlinien durch.
