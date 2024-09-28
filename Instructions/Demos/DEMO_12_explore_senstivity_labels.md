<!---
---
Demo: Titel: „Vertraulichkeitsbezeichnungen in Microsoft Purview“ Lernpfad/Modul/Lerneinheit: „Lernpfad: Beschreiben der Funktionen von Microsoft Priva und Microsoft Purview; Modul 2: Beschreiben der Datensicherheitslösungen von Microsoft Purview; Lerneinheit 4: Beschreiben von Vertraulichkeitsbezeichnungen und Richtlinien in Microsoft Purview Information Protection“
---
--->

# Demo: Vertraulichkeitsbezeichnungen in Microsoft Purview

Diese Demo ist den folgenden Learn-Inhalten zugeordnet:

- Lernpfad: Beschreiben der Funktionen von Microsoft Priva und Microsoft Purview
- Modul: Beschreiben der Datensicherheitslösungen von Microsoft Purview
- Lerneinheit: Beschreiben von Vertraulichkeitsbezeichnungen und Richtlinien in Microsoft Purview Information Protection

## Vorführungsszenario

In dieser Demo zeigen Sie die Funktionen der Vertraulichkeitsbezeichnungen.  Sie durchlaufen die Einstellungen für vorhandene, bereits erstellte Vertraulichkeitsbezeichnungen und für die entsprechende Richtlinie zum Veröffentlichen der Bezeichnung.   Anschließend erfahren Sie, wie eine Bezeichnung angewendet wird, und welche Auswirkung diese Bezeichnung aus der Perspektive eines Benutzers hat.  **HINWEIS**: Wenn Sie Word zum ersten Mal online mit Ihrem Microsoft 365-Mandanten verwenden, kann es bis zu 15 Minuten dauern, bis die Option „Vertraulichkeit“ im Menüband angezeigt wird.  Referent*innen sollten den Demoteil 2 noch vor Kursbeginn ausführen, damit noch genügend Zeit bleibt, bis die Option angezeigt wird.

### Teil 1 der Demo

In dieser Demo zeigen Sie die Einstellungen für eine vorhandene Vertraulichkeitsbezeichnung und die entsprechende Richtlinie zum Veröffentlichen der Bezeichnung.

1. Öffnen Sie eine neue Microsoft Edge-Browserregisterkarte, und geben Sie in der Adressleiste **https://purview.microsoft.com** ein. Um auf das neue Microsoft Purview-Portal zuzugreifen, wählen Sie das Kontrollkästchen neben **Ich stimme den Bedingungen der Datenflussoffenlegung und den Datenschutzbestimmungen zu** und wählen Sie dann **Erste Schritte** aus.  

1. Wählen Sie auf der Startseite des neuen Microsoft Purview-Portals die Kachel **Alle Lösungen anzeigen** und dann die Kachel **Information Manager** aus. Wählen Sie alternativ im linken Navigationsbereich **Lösungen** und dann **Information Protection** aus.

1. Sie gelangen auf die Übersichtsseite. Wählen Sie im linken Navigationsbereich **Vertraulichkeitsbezeichnungen** aus.

1. Einige Bezeichnungen wurden in Ihrem Microsoft 365-Labmandanten vorkonfiguriert. Wählen Sie die Bezeichnung namens **Vertraulich-Finanzen** aus.  Ein Fenster wird geöffnet, das Informationen über diese Bezeichnung bereitstellt.  Beachten Sie die Einstellungen für diese Bezeichnung.  Wählen Sie oben auf der Seite die Option **Bezeichnung bearbeiten** aus (möglicherweise als Bleistiftsymbol angezeigt), um einige der grundlegenden Konfigurationseinstellungen anzuzeigen. Wenn diese Option nicht angezeigt wird, wählen Sie die Auslassungspunkte aus.
    1. Bei der Konfiguration werden zunächst ein Name und eine Beschreibung für Ihre Bezeichnung angegeben.  Nehmen Sie keine Änderungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.
    1. Beachten Sie den Bereich für diese Bezeichnung. Nehmen Sie keine Änderungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.
    1. Auf diesem nächsten Bildschirm können Sie Schutzeinstellungen für die beschrifteten Elemente auswählen. Beachten Sie, dass diese Bezeichnung konfiguriert ist, die Inhaltsmarkierung zu unterstützen. Nehmen Sie keine Änderungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.
        1. Beachten Sie auf der Seite „Inhaltsmarkierung“ das oben auf der Seite befindliche Informationsfeld.  Nehmen Sie keine Änderungen an den Einstellungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.
    1. Sie befinden sich nun im Fenster „Automatisches Anwenden von Bezeichnungen für Dateien und E-Mails“.  Lesen Sie oben auf der Seite die Beschreibung zum Anwenden der automatischen Bezeichnung und das darunter befindliche Informationsfeld.  Beachten Sie außerdem, dass diese Bezeichnung für das automatische Anwenden von Bezeichnungen für bestimmte Bedingungen festgelegt ist. Nehmen Sie keine Änderungen an den Einstellungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.
    1. In diesem Fenster werden Schutzeinstellungen für Teams, Gruppen und Websites festgelegt, für die diese Bezeichnung angewendet wird. Wenn sie nicht aktiviert ist, wählen Sie unten auf der Seite die Option **Weiter** aus.
    1. Dieses Fenster ist eine Previewfunktion zum automatischen Anwenden dieser Bezeichnung auf schematisierte Datenobjekte in Microsoft Purview Data Map (wie etwa SQL, Synapse und mehr), die Arten vertraulicher Informationen enthalten, die von Ihnen ausgewählt wurden.  Dieses Feature ist nicht aktiviert. Wählen Sie unten auf der Seite die Option **Abbrechen** aus, um den Assistenten für die Bezeichnungskonfiguration zu schließen und um zur Seite „Information Protection“ zurückzukehren.

1. Wählen Sie im linken Navigationsbereich **Richtlinien** und dann **Veröffentlichungsrichtlinien** aus.  Vertraulichkeitsbezeichnungen können aufgrund von Bezeichnungsrichtlinien veröffentlicht werden.  Der Microsoft 365-Mandant wurde zur Vereinfachung mit einigen Bezeichnungsrichtlinien konfiguriert.

1. Wählen Sie **Richtlinie zu vertraulichen Finanzen** aus.  Ein Fenster wird geöffnet, das Informationen über die Richtlinie bereitstellt. Wählen Sie oben im Fenster die **Richtlinie bearbeiten** aus.  Hier werden Sie durch die Einstellungen geführt, ohne etwas zu ändern.
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

1. Wählen Sie im linken Navigationsbereich unter „Information Protection“ die Option „Automatische Bezeichnung“ aus. Schauen Sie sich die Beschreibung an. Achten Sie darauf, dass Sie Richtlinien für die automatische Anwendung von Bezeichnungen, um automatisch Vertraulichkeitsbezeichnungen auf E-Mail-Nachrichten oder OneDrive- und SharePoint-Dateien anzuwenden, die vertrauliche Informationen enthalten, erstellen. Wenn Richtlinien für die automatische Bezeichnung konfiguriert sind, wählen Sie eine aus, und lesen Sie die Richtlinieninformationen im Detailbereich.  Wenn keine Richtlinie aufgeführt ist, können Sie die Schritte zum Erstellen durchlaufen, sofern dies die Zeit zulässt.

1. Wählen Sie im linken Navigationsbereich „Startseite“ aus, um zum Microsoft Purview-Portal zurückzugehen.

1. Halten Sie diese Browser-Registerkarte offen.

### Teil 2 der Demo

In diesem Schritt zeigen Sie den Prozess der Anwendung einer Bezeichnung aus der Perspektive des Benutzers (in diesem Fall ist der Benutzer der Administrator).  Um die Auswirkungen des Anwendens der Bezeichnung anzuzeigen, wählen Sie die Bezeichnung „Confidential – Finance“ (Vertraulich – Finanzen) aus, da diese Bezeichnung ein Wasserzeichen anwendet.

1. Wählen Sie auf der Startseite des Microsoft Purview-Complianceportals das **App-Startfeld-Symbol** aus, das sich neben dem Text „Microsoft Purview“ (über dem Startseitensymbol) befindet. Wählen Sie das **Word-Symbol** aus.  

1. Wählen Sie **Leeres Dokument** aus, und geben Sie dann auf der Seite etwas Text ein.  Wählen Sie oben auf der Seite auf dem blauen Balken den Abwärtspfeil aus, der sich neben „DokumentXX – gespeichert“ befindet, und geben Sie in das Feld „Dateiname“ den Text **Testbezeichnung** ein. Drücken Sie dann die **EINGABETASTE** auf Ihrer Tastatur.

1. Ganz rechts auf der oberen Menüleiste (auch als Menüband bezeichnet) befindet sich ein Pfeil nach unten. Wählen Sie ihn aus, und wählen Sie dann **Klassisches Menüband** aus.  Dies vereinfacht das Erkennen des Vertraulichkeitssymbols. Wählen Sie neben dem Mikrofonsymbol die Option **Vertraulichkeit** aus. Wählen Sie im Dropdownmenü den Eintrag **Confidential-Finance** (Vertraulich – Finanzen) aus.  

1. Wählen Sie auf der oberen Menüleiste die Option **Ansicht** und dann die Ansicht **Lesebereich** aus.

1. Beachten Sie, dass das Dokument das Wasserzeichen enthält.  

1. Schließen Sie die in Ihrem Browser geöffneten Microsoft Word-Registerkarten, um Word zu schließen.

1. Lassen Sie die Browserregisterkarte „Microsoft Purview“ für die nächste Demo geöffnet.

### Überprüfung

In dieser Demo haben Sie die Einstellungen gezeigt, die für Vertraulichkeitsbezeichnungen und die Einstellungen für Richtlinien zum Veröffentlichen von Vertraulichkeitsbezeichnungen konfiguriert werden können. Außerdem haben Sie gezeigt, wie man eine Bezeichnung anwendet.
