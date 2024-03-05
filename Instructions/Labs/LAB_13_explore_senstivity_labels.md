---
lab:
  title: "Erkunden von Vertraulichkeitsbezeichnungen in Microsoft\_Purview"
  module: Describe information protection and data lifecycle management in Microsoft Purview
---

# Lab: Erkunden von Vertraulichkeitsbezeichnungen in Microsoft Purview

Dieses Lab ist den folgenden Learn-Inhalten zugeordnet:

- Lernpfad: Beschreiben der Funktionen der Microsoft-Compliancelösungen
- Modul: Beschreiben von Information Protection und Datenlebenszyklusverwaltung in Microsoft Purview
- Lerneinheit: Beschreiben von Vertraulichkeitsbezeichnungen

## Labszenario

In diesem Lab erkunden Sie die Funktionen von Vertraulichkeitsbezeichnungen.  Sie durchlaufen die Einstellungen für vorhandene, bereits erstellte Vertraulichkeitsbezeichnungen und für die entsprechende Richtlinie zum Veröffentlichen der Bezeichnung.   Anschließend erfahren Sie, wie eine Bezeichnung angewendet wird, und welche Auswirkung diese Bezeichnung aus der Perspektive eines Benutzers hat.

**Geschätzte Dauer**: 20 bis 25 Minuten

### Aufgabe 1

In dieser Aufgabe erfahren Sie, wozu Vertraulichkeitsbezeichnungen dienen, indem Sie eine neue Bezeichnung erstellen und eine Richtlinie zur Veröffentlichung der Bezeichnung erstellen.

1. Öffnen Sie die Browserregisterkarte für die Startseite von Microsoft Purview.  Wenn Sie die Registerkarte zuvor geschlossen haben, öffnen Sie eine neue Browserregisterkarte, und geben Sie **https://admin.microsoft.com** ein. Melden Sie sich mit den Administratoranmeldeinformationen für den Microsoft 365-Mandanten an, der vom autorisierten Labhoster (ALH) bereitgestellt wird. Wählen Sie im linken Navigationsbereich von Microsoft 365 Admin Center **Alle anzeigen** und dann **Compliance** aus.  Die Startseite des Microsoft Purview-Complianceportals wird auf einer neuen Browserseite geöffnet.

1. Erweitern Sie im linken Navigationsbereich unter Lösungen den Eintrag **Informationsschutz** und wählen Sie dann **Übersicht** aus. Beachten Sie die Warnung oben auf der Seite, und scrollen Sie nach unten, um die verfügbaren Informationen anzuzeigen.
   1. Möglicherweise sehen Sie auf der Übersichtsseite ein gelbes Informationsfeld, das anzeigt, dass Ihre Organisation die Fähigkeit zur Verarbeitung von Inhalten in Office-Onlinedateien, die mit verschlüsselten Vertraulichkeitsbezeichnungen versehen und in OneDrive und SharePoint gespeichert sind, nicht aktiviert hat.  Wählen Sie **Jetzt aktivieren** aus.  Wenn dies passiert, kann es zu einer Verzögerung für die Weitergabe der Einstellung über das System kommen, und es müssen zusätzliche Schritte ausgeführt werden, um Teams, SharePoint-Websites und Microsoft 365-Gruppen zu schützen.

1. Wählen Sie im linken Navigationsbereich **Bezeichnungen** aus.
   1. Möglicherweise sehen Sie auf der Bezeichnungenseite ein gelbes Informationsfeld, das anzeigt, dass Ihre Organisation die Fähigkeit zur Verarbeitung von Inhalten in Office-Onlinedateien, die mit verschlüsselten Vertraulichkeitsbezeichnungen versehen und in OneDrive und SharePoint gespeichert sind, nicht aktiviert hat.  Wählen Sie **Jetzt aktivieren** aus.  Wenn dies passiert, kann es zu einer Verzögerung für die Weitergabe der Einstellung über das System kommen, und es müssen zusätzliche Schritte ausgeführt werden, um Teams, SharePoint-Websites und Microsoft 365-Gruppen zu schützen.

1. Einige Bezeichnungen wurden in Ihrem Microsoft 365-Labmandanten vorkonfiguriert. Wählen Sie die Bezeichnung namens **Vertraulich-Finanzen** aus.  Ein Fenster wird geöffnet, das Informationen über diese Bezeichnung bereitstellt.  Beachten Sie die Einstellungen für diese Bezeichnung.  Wählen Sie oben auf der Seite die Option **Bezeichnung bearbeiten** aus (möglicherweise als Bleistiftsymbol angezeigt), um einige der grundlegenden Konfigurationseinstellungen anzuzeigen. Wenn diese Option nicht angezeigt wird, wählen Sie die Auslassungspunkte aus.
    1. Bei der Konfiguration werden zunächst ein Name und eine Beschreibung für Ihre Bezeichnung angegeben.  Nehmen Sie keine Änderungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.
    1. Beachten Sie den Bereich für diese Bezeichnung. Nehmen Sie keine Änderungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.
    1. Auf diesem nächsten Bildschirm können Sie Schutzeinstellungen für die beschrifteten Elemente auswählen. Beachten Sie, dass diese Bezeichnung konfiguriert ist, die Inhaltsmarkierung zu unterstützen. Nehmen Sie keine Änderungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.
        1. Beachten Sie auf der Seite „Inhaltsmarkierung“ das oben auf der Seite befindliche Informationsfeld.  Nehmen Sie keine Änderungen an den Einstellungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.
    1. Sie befinden sich nun im Fenster „Automatisches Anwenden von Bezeichnungen für Dateien und E-Mails“.  Lesen Sie oben auf der Seite die Beschreibung zum Anwenden der automatischen Bezeichnung und das darunter befindliche Informationsfeld.  Beachten Sie außerdem, dass diese Bezeichnung für das automatische Anwenden von Bezeichnungen für bestimmte Bedingungen festgelegt ist. Nehmen Sie keine Änderungen an den Einstellungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.
    1. In diesem Fenster werden Schutzeinstellungen für Teams, Gruppen und Websites festgelegt, für die diese Bezeichnung angewendet wird. Wenn sie nicht aktiviert ist, wählen Sie unten auf der Seite die Option **Weiter** aus.
    1. Dieses Fenster ist eine Previewfunktion zum automatischen Anwenden dieser Bezeichnung auf schematisierte Datenobjekte in Microsoft Purview Data Map (wie etwa SQL, Synapse und mehr), die Arten vertraulicher Informationen enthalten, die von Ihnen ausgewählt wurden.  Dieses Feature ist nicht aktiviert. Wählen Sie unten auf der Seite die Option **Abbrechen** aus, um den Assistenten für die Bezeichnungskonfiguration zu schließen und um zur Seite „Information Protection“ zurückzukehren.

1. Wählen Sie im linken Navigationsbereich **Bezeichnungsrichtlinien** aus.  Vertraulichkeitsbezeichnungen können aufgrund von Bezeichnungsrichtlinien veröffentlicht werden.  Der Microsoft 365-Mandant wurde zur Vereinfachung mit einigen Bezeichnungsrichtlinien konfiguriert.

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

1. Wählen Sie im linken Navigationsbereich unter „Information Protection“ die Option „Automatische Bezeichnung“ aus. Schauen Sie sich die Beschreibung an. Achten Sie darauf, dass Sie Richtlinien für die automatische Anwendung von Bezeichnungen, um automatisch Vertraulichkeitsbezeichnungen auf E-Mail-Nachrichten oder OneDrive- und SharePoint-Dateien anzuwenden, die vertrauliche Informationen enthalten, erstellen. In unserem Mandanten wurden keine Richtlinien für automatische Bezeichnungen vorkonfiguriert. Um eine neue Richtlinie für automatische Bezeichnungen zu erstellen, wählen Sie **Richtlinie für automatische Bezeichnungen erstellen** aus.  Hier werden die Schritte zum Erstellen einer neuen Richtlinie beschrieben.
    1. Wählen Sie zunächst die Informationen aus, auf die diese Bezeichnung angewendet werden soll.  Beachten Sie die verfügbaren Optionen.  Wählen Sie **Medizin und Gesundheit** aus, und wählen Sie dann eine der verfügbaren Vorlagen aus.  Wählen Sie **Weiter** aus.
    1. Sie können Ihre Richtlinie für die automatische Bezeichnung benennen oder den Standardnamen verwenden.  Wählen Sie **Weiter** aus.
    1. Sie können die Administratoreinheiten zuweisen, für die diese Richtlinie gilt.  Lassen Sie die Standardeinstellung auf vollständiges Verzeichnis, und wählen Sie **Weiter** aus.
    1. Notieren Sie sich die verfügbaren Speicherorte, an denen Sie die Bezeichnung anwenden möchten.  Übernehmen Sie die Standardwerte, und klicken Sie auf **Weiter**.
    1. Sie können allgemeine oder erweiterte Regeln einrichten, die definieren, auf welchen Inhalt die Bezeichnung angewendet wird.  Lassen Sie die Standardeinstellung auf Allgemeine Regeln, und wählen Sie **Weiter** aus.
    1. Sie können Regeln für Inhalte an allen Speicherorten definieren.  Die Bezeichnung wird auf Inhalte angewendet, die den auf dieser Seite definierten Regeln entsprechen.  Für die ausgewählte Vorlage sollte eine Position angezeigt werden. Erweitern Sie sie, um die geltenden Bedingungen anzuzeigen.  Übernehmen Sie die Standardeinstellungen, und klicken Sie auf **Weiter**.
    1. Wählen Sie eine Bezeichnung aus, die automatisch angewendet werden soll, indem Sie auf **Bezeichnung auswählen** klicken.  Wählen Sie eine Bezeichnung und klicken Sie dann **Hinzufügen**. Wählen Sie **Weiter** aus.
    1. Für E-Mails können zusätzliche Einstellungen konfiguriert werden. Übernehmen Sie die Standardwerte, und klicken Sie auf **Weiter**.
    1. Sie können die Richtlinie jetzt oder später testen.  Wählen Sie **Richtlinie deaktiviert lassen** und dann **Weiter** aus.
    1. Überprüfen Sie die Einstellungen, und wählen Sie **Richtlinie erstellen** und dann **Fertig** aus.

1. Wählen Sie im linken Navigationsbereich die **Startseite** aus, um zur Startseite des Microsoft Purview-Complianceportals zurückzukehren.

1. Lassen Sie diese Seite geöffnet, da Sie sie in der nächsten Aufgabe verwenden werden.

### Aufgabe 2

In dieser Aufgabe durchlaufen Sie den Prozess zum Anwenden einer Vertraulichkeitsbezeichnung auf ein Microsoft Word-Dokument und zeigen dann die Inhaltsmarkierung (Wasserzeichen) an, die von der Bezeichnung generiert wird. HINWEIS: Wenn Sie Microsoft Word online verwenden, kann es zu einer Verzögerung kommen, bevor die Option zum Auswählen von Vertraulichkeitsbezeichnungen im oberen Menüband angezeigt wird.  Es wird empfohlen, alle verbleibenden Labs abzuschließen und dann wieder zu dieser Aufgabe zurückzukehren.

1. Wählen Sie auf der Startseite des Microsoft Purview-Complianceportals das **App-Startfeld-Symbol** aus, das sich neben dem Text „Contoso Electronics“ befindet. Wählen Sie das **Word-Symbol** aus.  

1. Wählen Sie unter „Neu erstellen“ die Option **Leeres Dokument** aus, und geben Sie dann auf der Seite etwas Text ein.  Wählen Sie oben auf der Seite den Abwärtspfeil aus, der sich neben „DokumentXX – gespeichert“ befindet, und geben Sie in das Feld „Dateiname“ den Text **Testbezeichnung** ein. Drücken Sie dann die **EINGABETASTE** auf Ihrer Tastatur.

1. Ganz rechts auf der oberen Menüleiste (auch als Menüband bezeichnet) befindet sich ein Pfeil nach unten. Wählen Sie ihn aus, und wählen Sie dann **Klassisches Menüband** aus.  Dies vereinfacht das Erkennen des Vertraulichkeitssymbols. Wählen Sie neben dem Mikrofonsymbol die Option **Vertraulichkeit** aus. Wählen Sie im Dropdownmenü den Eintrag **Confidential-Finance** (Vertraulich – Finanzen) aus.  

1. Wählen Sie auf der oberen Menüleiste die Option **Ansicht** und dann die Ansicht **Lesebereich** aus.

1. Beachten Sie, dass das Dokument das Wasserzeichen „Vertrauliche FINANZDATEN“ enthält.  

1. Schließen Sie die Microsoft Word-Registerkarten, die in Ihrem Browser geöffnet sind, um Word zu beenden, aber lassen Sie die Browserregisterkarte mit der Microsoft Purview-Homepage geöffnet.

### Überprüfung

In diesem Lab erkunden Sie die Funktionen von Vertraulichkeitsbezeichnungen.  Sie gehen die Einstellungen für vorhandene, bereits erstellte Vertraulichkeitsbezeichnungen und für die entsprechende Richtlinie zum Veröffentlichen der Bezeichnung durch.   Anschließend erfahren Sie, wie Sie eine Bezeichnung anwenden.
