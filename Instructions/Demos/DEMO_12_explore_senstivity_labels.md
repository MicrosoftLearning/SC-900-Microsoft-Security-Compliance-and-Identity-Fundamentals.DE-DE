<!---
---
Demo: Titel: 'Vertraulichkeitsbezeichnungen in Microsoft Purview' Learning Path/Module/Unit: 'Lernpfad: Beschreiben der Funktionen der Microsoft-Compliancelösungen; Modul 3: Beschreiben von Information Protection in Microsoft Purview; Lerneinheit 4: Beschreiben von Vertraulichkeitsbezeichnungen'
---
--->

# Demo: Vertraulichkeitsbezeichnungen in Microsoft Purview

Diese Demo ist den folgenden Learn-Inhalten zugeordnet:

- Lernpfad: Beschreiben der Funktionen der Microsoft-Compliancelösungen
- Modul: Beschreiben der Funktionen von Microsoft Purview zur Information Protection, zur Daten-Lebenszyklusverwaltung und zur Daten-Governance
- Lerneinheit: Beschreiben von Vertraulichkeitsbezeichnungen

## Vorführungsszenario

In dieser Demo zeigen Sie die Funktionen der Vertraulichkeitsbezeichnungen.  Sie durchlaufen die Einstellungen für vorhandene, bereits erstellte Vertraulichkeitsbezeichnungen und für die entsprechende Richtlinie zum Veröffentlichen der Bezeichnung.   Anschließend erfahren Sie, wie eine Bezeichnung angewendet wird, und welche Auswirkung diese Bezeichnung aus der Perspektive eines Benutzers hat.  **HINWEIS**: Wenn Sie Word zum ersten Mal online mit Ihrem Microsoft 365-Mandanten verwenden, kann es bis zu 15 Minuten dauern, bis die Option „Vertraulichkeit“ im Menüband angezeigt wird.  Referent*innen sollten den Demoteil 2 noch vor Kursbeginn ausführen, damit noch genügend Zeit bleibt, bis die Option angezeigt wird.

### Teil 1 der Demo

In dieser Demo zeigen Sie die Einstellungen für eine vorhandene Vertraulichkeitsbezeichnung und die entsprechende Richtlinie zum Veröffentlichen der Bezeichnung.

1. Öffnen Sie die Browserregisterkarte für die Startseite von Microsoft Purview.  Wenn Sie die Registerkarte zuvor geschlossen haben, öffnen Sie eine neue Browserregisterkarte, und geben Sie **https://admin.microsoft.com** ein. Melden Sie sich mit den Administratoranmeldeinformationen für den Microsoft 365-Mandanten an, der vom autorisierten Labhoster (ALH) bereitgestellt wird. Wählen Sie im linken Navigationsbereich von Microsoft 365 Admin Center **Alle anzeigen** und dann **Compliance** aus.  Die Startseite des Microsoft Purview-Complianceportals wird auf einer neuen Browserseite geöffnet.  

1. Erweitern Sie im linken Navigationsbereich unter Lösungen den Eintrag **Informationsschutz** und wählen Sie dann **Übersicht** aus.  Die Überblicksseite enthält Informationen zu den wichtigsten Vertraulichkeitsbezeichnungen, die auf Inhalte angewendet werden, die wichtigsten Aktivitäten erkannt wurden, Speicherorte, an denen Vertraulichkeitsbezeichnungen angewendet werden, und vieles mehr.  
    1. Möglicherweise sehen Sie auf der Überblicksseite ein gelbes Informationsfeld, das anzeigt, dass Ihre Organisation die Fähigkeit zur Verarbeitung von Inhalten in Office-Onlinedateien, die mit verschlüsselten Vertraulichkeitsbezeichnungen versehen und in OneDrive und SharePoint gespeichert sind, nicht aktiviert hat.  Wählen Sie **Jetzt aktivieren** aus.  Nachdem Sie diese Aktion vorgenommen haben, kann es eine Verzögerung geben, bis die Einstellung vom System übernommen wurde.

1. Wählen Sie im linken Navigationsbereich **Bezeichnungen** aus.

1. Einige Bezeichnungen wurden in Ihrem Microsoft 365-Labmandanten vorkonfiguriert. Wählen Sie die Bezeichnung" **Vertraulich-Finanzen** aus.  Ein Fenster wird geöffnet, das Informationen über diese Bezeichnung bereitstellt.  Beachten Sie die Einstellungen für diese Bezeichnung.  Wählen Sie oben auf der Seite das **Stiftsymbol** aus, um einige der grundlegenden Konfigurationseinstellungen anzuzeigen. Wenn das Stiftsymbol nicht angezeigt wird, wählen Sie die Auslassungspunkte aus.
    1. Bei der Konfiguration werden zunächst ein Name und eine Beschreibung für Ihre Bezeichnung angegeben.  Nehmen Sie keine Änderungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.
    1. Beachten Sie den Bereich für diese Bezeichnung. Nehmen Sie keine Änderungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.
    1. Auf diesem nächsten Bildschirm können Sie Schutzeinstellungen für die beschrifteten Elemente auswählen. Beachten Sie, dass diese Bezeichnung konfiguriert ist, die Inhaltsmarkierung zu unterstützen. Nehmen Sie keine Änderungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.
        1. Beachten Sie auf der Seite „Inhaltsmarkierung“ das oben auf der Seite befindliche Informationsfeld.  Nehmen Sie keine Änderungen an den Einstellungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.
    1. Sie befinden sich nun im Fenster „Automatisches Anwenden von Bezeichnungen für Dateien und E-Mails“.  Lesen Sie oben auf der Seite die Beschreibung zum Anwenden der automatischen Bezeichnung und das darunter befindliche Informationsfeld.  Beachten Sie außerdem, dass diese Bezeichnung für das automatische Anwenden von Bezeichnungen für bestimmte Bedingungen festgelegt ist. Nehmen Sie keine Änderungen an den Einstellungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.
    1. In diesem Fenster werden Schutzeinstellungen für Gruppen und Sites festgelegt, für die diese Bezeichnung angewendet wird. Wenn sie nicht aktiviert ist, wählen Sie unten auf der Seite die Option **Weiter** aus.
    1. Dieses Fenster ist eine Previewfunktion zum automatischen Anwenden dieser Bezeichnung auf schematisierte Datenobjekte in Microsoft Purview Data Map (wie etwa SQL, Synapse und mehr), die Arten vertraulicher Informationen enthalten, die von Ihnen ausgewählt wurden.  Dieses Feature ist nicht aktiviert. Wählen Sie unten auf der Seite die Option **Abbrechen** aus, um den Assistenten für die Bezeichnungskonfiguration zu schließen und um zur Seite „Information Protection“ zurückzukehren.

1. Wählen Sie im linken Navigationsbereich **Bezeichnungsrichtlinien** aus.  Vertraulichkeitsbezeichnungen können aufgrund von Bezeichnungsrichtlinien veröffentlicht werden.  Der Microsoft 365-Mandant wurde zur Vereinfachung mit einigen Bezeichnungsrichtlinien konfiguriert.

1. Wählen Sie **Richtlinie zu vertraulichen Finanzen** aus.  Ein Fenster wird geöffnet, das Informationen über die Richtlinie bereitstellt. 

1. Wählen Sie oben im Fenster die **Richtlinie bearbeiten** aus.  Hier werden Sie durch die Einstellungen geführt, ohne etwas zu ändern.
    1. Lesen Sie die Beschreibung unter „Zu veröffentlichende Vertraulichkeitsbezeichnungen auswählen“.  Beachten Sie die aufgelistete Bezeichnung.  Nehmen Sie keine Änderungen an den Einstellungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.
    1. Lesen Sie die Beschreibung für die „Zuweisung von Administratoreinheiten“. Die Administratoreinheiten sind auf das vollständige Verzeichnis festgelegt. Ändern Sie keine der Einstellungen. Wählen Sie **Weiter** aus.  
    1. Schauen Sie sich die Beschreibung für die „Veröffentlichung für Benutzer und Gruppen“ an.  Beachten Sie, dass diese Bezeichnung für alle Benutzer verfügbar ist.  Nehmen Sie keine Änderungen an den Einstellungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.
    1. Überprüfen Sie die Richtlinieneinstellungen. Nehmen Sie keine Änderungen an den Einstellungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.
    1. Lesen Sie die Beschreibung unter „Standardbezeichnung auf Dokumente anwenden“. Nehmen Sie keine Änderungen an den Einstellungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.
    1. Lesen Sie die Beschreibungen für „Anwenden einer Standardbezeichnung auf E-Mails“ und „Bezeichnung von Anlagen erben“. Nehmen Sie keine Änderungen an den Einstellungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.
    1. Lesen Sie die Beschreibung für „Anwenden einer Standardbezeichnung auf Besprechungen und Kalenderereignisse“. Nehmen Sie keine Änderungen an den Einstellungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.
    1. Lesen Sie die Beschreibung unter „Standardbezeichnung auf Power BI-Inhalte anwenden“. Nehmen Sie keine Änderungen an den Einstellungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.
    1. Über die letzte Konfigurationsoption wird der Name Ihrer Richtlinie festgelegt.  Da Sie die Richtlinie bearbeiten, ist das Feld „Name“ abgeblendet. Wählen Sie unten auf der Seite **Weiter** aus.
    1. Überprüfen Sie die Richtlinieneinstellungen. Wählen Sie **Abbrechen** aus, um alle Änderungen zu verwerfen und zur Seite Bezeichnungsrichtlinien zurückzukehren.

1. Wählen Sie auf der Seite „Information Protection“ die Option „Automatisches Bezeichnen“ aus. Schauen Sie sich die Beschreibung an. Achten Sie darauf, dass Sie Richtlinien für die automatische Anwendung von Bezeichnungen, um automatisch Vertraulichkeitsbezeichnungen auf E-Mail-Nachrichten oder OneDrive- und SharePoint-Dateien anzuwenden, die vertrauliche Informationen enthalten, erstellen. Wenn Richtlinien für die automatische Bezeichnung konfiguriert sind, wählen Sie eine aus, und überprüfen Sie die Richtlinieninformationen im Detailbereich.  Wenn keine Richtlinie aufgeführt ist, können Sie die Schritte zum Erstellen durchlaufen, sofern dies die Zeit zulässt.

1. Wählen Sie im linken Navigationsbereich die Startseite aus, um zur Startseite des Microsoft Purview-Complianceportals zurückzukehren.

1. Halten Sie diese Browser-Registerkarte offen.

### Teil 2 der Demo

In diesem Schritt zeigen Sie den Prozess der Anwendung einer Bezeichnung aus der Perspektive des Benutzers (in diesem Fall ist der Benutzer der Administrator).  Um die Auswirkungen des Anwendens der Bezeichnung anzuzeigen, wählen Sie die Bezeichnung „Confidential – Finance“ (Vertraulich – Finanzen) aus, da diese Bezeichnung ein Wasserzeichen anwendet.

1. Wählen Sie auf der Startseite des Microsoft Purview-Complianceportals das **App-Startfeld-Symbol** aus, das sich neben dem Text „Contoso Electronics“ befindet. Wählen Sie das **Word-Symbol** aus.  

1. Wählen Sie **Leeres Dokument** aus, und geben Sie dann auf der Seite etwas Text ein.  Wählen Sie oben auf der Seite auf dem blauen Balken den Abwärtspfeil aus, der sich neben „DokumentXX – gespeichert“ befindet, und geben Sie in das Feld „Dateiname“ den Text **Testbezeichnung** ein. Drücken Sie dann die **EINGABETASTE** auf Ihrer Tastatur.

1. Wählen Sie in der oberen Menüleiste das Symbol **Vertraulichkeitssymbol** (das Symbol rechts neben dem Mikrofonsymbol) aus. Wenn diese Option nicht sofort angezeigt wird, aktualisieren Sie die Seite. Wählen Sie in der Dropdownliste den Eintrag **Confidential – Finance** (Vertraulich – Finanzen) aus.   HINWEIS: Wenn die Option „Vertraulichkeit“ nicht sofort angezeigt wird, aktualisieren Sie die Seite. Da es sich hier um eine Mandantenumgebung in einem Lab handelt, ist die Verzögerung möglicherweise länger als üblich (10-15 Minuten).
1. 
1. Wählen Sie auf der oberen Menüleiste die Option **Ansicht** und dann die Ansicht **Lesebereich** aus.

1. Beachten Sie, dass das Dokument das Wasserzeichen enthält.  

1. Schließen Sie die in Ihrem Browser geöffneten Microsoft Word-Registerkarten, um Word zu schließen.

1. Lassen Sie die Microsoft Purview-Browserregisterkarte für die nächste Demo geöffnet.

### Überprüfung

In dieser Demo haben Sie die Einstellungen gezeigt, die für Vertraulichkeitsbezeichnungen und die Einstellungen für Richtlinien zum Veröffentlichen von Vertraulichkeitsbezeichnungen konfiguriert werden können. Außerdem haben Sie gezeigt, wie Sie eine Bezeichnung anwenden.
