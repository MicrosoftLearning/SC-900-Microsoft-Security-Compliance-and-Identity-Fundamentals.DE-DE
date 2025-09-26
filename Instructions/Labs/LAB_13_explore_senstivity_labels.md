---
lab:
  title: "Erkunden von Vertraulichkeitsbezeichnungen in Microsoft\_Purview"
  module: Describe the data security solutions of Microsoft Purview
---

# Lab: Erkunden von Vertraulichkeitsbezeichnungen in Microsoft Purview

Dieses Lab ist den folgenden Learn-Inhalten zugeordnet:

- Lernpfad: Beschreiben der Funktionen von Microsoft Priva und Microsoft Purview
- Modul: Beschreiben der Datensicherheitslösungen von Microsoft Purview
- Lerneinheit: Beschreiben von Vertraulichkeitsbezeichnungen und Richtlinien in Microsoft Purview Information Protection

## Labszenario

In diesem Lab erkunden Sie die Funktionen von Vertraulichkeitsbezeichnungen.  Sie durchlaufen die Einstellungen für vorhandene, bereits erstellte Vertraulichkeitsbezeichnungen und für die entsprechende Richtlinie zum Veröffentlichen der Bezeichnung. Anschließend erfahren Sie, wie eine Bezeichnung angewendet wird, und welche Auswirkung diese Bezeichnung aus der Perspektive eines Benutzers hat.

**Geschätzte Dauer**: 45 Minuten

### Aufgabe 1

In dieser Aufgabe erfahren Sie, wozu Vertraulichkeitsbezeichnungen dienen, indem Sie eine neue Bezeichnung erstellen und eine Richtlinie zur Veröffentlichung der Bezeichnung erstellen.

1. Öffnen Sie die Browserregisterkarte für die Startseite von Microsoft Purview.  Wenn Sie die Registerkarte zuvor geschlossen haben, öffnen Sie eine neue Browserregisterkarte, und geben Sie **`https://admin.microsoft.com`** ein. Melden Sie sich mit den Administratoranmeldeinformationen für den Microsoft 365-Mandanten an, der vom autorisierten Labhoster (ALH) bereitgestellt wird.

1. Wählen Sie im linken Navigationsbereich von Microsoft 365 Admin Center **Alle anzeigen** und dann **Microsoft Purview** aus.  Die Startseite des Microsoft Purview-Portals wird auf einer neuen Browserseite geöffnet.

1. Wählen Sie im linken Navigationsbereich **Lösungen** und dann **Information Protection** aus.  Sie befinden sich auf der Überblicksseite. Scrollen Sie nach unten, um die verfügbaren Informationen anzuzeigen.

1. Wählen Sie im linken Navigationsbereich **Vertraulichkeitsbezeichnungen** aus.
1. Sie sehen ein gelbes Banner, das darauf hinweist, dass Ihre Organisation die Funktion zur Verarbeitung von Inhalten in Office-Online-Dateien, die mit verschlüsselten Vertraulichkeitsbezeichnungen versehen und in OneDrive und SharePoint gespeichert sind, nicht aktiviert hat.  Wählen Sie **Jetzt aktivieren** aus.

1. Einige Bezeichnungen wurden in Ihrem Microsoft 365-Labmandanten vorkonfiguriert. Erweitern Sie die Bezeichnung **Höchst Vertraulich**, und wählen Sie dann **Alle Mitarbeiter** aus.  Ein Fenster wird geöffnet, das Informationen über diese Bezeichnung bereitstellt.  Beachten Sie die Einstellungen für diese Bezeichnung.  Wählen Sie **Bezeichnung bearbeiten** aus. Wenn diese Option nicht angezeigt wird, wählen Sie die Auslassungspunkte aus.
    1. Die Konfiguration beginnt mit der Bereitstellung grundlegender Details für die Bezeichnung.  Nehmen Sie keine Änderungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.
    1. Beachten Sie den Bereich für diese Bezeichnung. Nehmen Sie keine Änderungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.
    1. Auf diesem nächsten Bildschirm können Sie Schutzeinstellungen für die beschrifteten Elemente auswählen. Diese Bezeichnung steuert, wer auf gekennzeichnete Elemente zugreifen und diese anzeigen kann, und wendet auch die Inhaltskennzeichnung an.  Wählen Sie **Weiter** aus, um die Details anzuzeigen.
        1. Zugriffssteuerung: Überprüfen Sie die Einstellungen, ändern Sie jedoch nichts.  Wählen Sie **Weiter** aus.
        1. Inhaltskennzeichnung: Beachten Sie, dass die Bezeichnung eine Fußzeile anwendet.  Wählen Sie anschließend **Weiter** aus.
        1. Automatische Bezeichnungen für Dateien und E-Mails: Lesen Sie oben auf der Seite die Beschreibung zum Anwenden der automatischen Bezeichnung und das darunter befindliche Informationsfeld.  Beachten Sie außerdem, dass diese Bezeichnung als automatische Bezeichnung festgelegt ist, wenn Kreditkartennummern erkannt werden. Nehmen Sie keine Änderungen an den Einstellungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.
    1. Definieren von Schutzeinstellungen für Gruppen und Websites: Überprüfen Sie die Optionen für Schutzeinstellungen und automatisches Anwenden von Einstellungen.  In diesem Fenster wurde nichts konfiguriert.  Nehmen Sie keine Änderungen vor. Wählen Sie unten auf der Seite die Option **Weiter** aus.
    1. Überprüfen Sie Ihre Einstellungen, und schließen Sie Folgendes ab: Überprüfen Sie Ihre Einstellungen.  Da nichts geändert wurde, wählen Sie **Abbrechen** aus.

1. Erweitern Sie im linken Navigationsbereich **Richtlinien**, und wählen Sie dann **Veröffentlichungsrichtlinien bezeichnen** aus.  Vertraulichkeitsbezeichnungen können aufgrund von Bezeichnungsrichtlinien veröffentlicht werden.  Der Microsoft 365-Mandant wurde zur Vereinfachung mit einigen Bezeichnungsrichtlinien konfiguriert. Wählen Sie **Streng vertrauliche Richtlinie** aus.  Ein Fenster wird geöffnet, das Informationen über die Richtlinie bereitstellt. Wählen Sie oben im Fenster die **Richtlinie bearbeiten** aus.  Hier werden Sie durch die Einstellungen geführt, ohne etwas zu ändern.
    1. Wählen Sie zu veröffentlichende Vertraulichkeitsbezeichnungen aus:  Beachten Sie die aufgelisteten Bezeichnungen.  Nehmen Sie keine Änderungen an den Einstellungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.
    1. Zuweisen von Admineinheiten: Die Administratoreinheiten sind auf das vollständige Verzeichnis festgelegt. Ändern Sie keine der Einstellungen. Wählen Sie **Weiter** aus.  
    1. Veröffentlichen für Benutzende und Gruppen:  Beachten Sie, dass diese Bezeichnung für alle Benutzer verfügbar ist.  Nehmen Sie keine Änderungen an den Einstellungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.
    1. Richtlinieneinstellungen: Beachten Sie die verfügbaren Optionen. Nehmen Sie keine Änderungen an den Einstellungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.
    1. Standardeinstellungen für Dokumente: Nehmen Sie keine Änderungen an den Einstellungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.
    1. Standardeinstellungen für E-Mails: Überprüfen Sie die Optionen, und beachten Sie, dass E-Mails eine Bezeichnung von einer Anlage mit höherer Priorität erben können, sofern dies konfiguriert ist. Wählen Sie **Weiter** aus.
    1. Standardeinstellungen für Besprechungen und Kalenderereignisse: Überprüfen Sie die Optionen, und beachten Sie die Option zum Anwenden der Vererbung zwischen Teambesprechungen und Artefakten. Nehmen Sie keine Änderungen an den Einstellungen vor.  Wählen Sie **Weiter** aus.
    1. Standardeinstellungen für Fabric- und Power BI-Inhalte: Nehmen Sie keine Änderungen an den Einstellungen vor.  Wählen Sie **Weiter** aus.
    1. Benennen Ihrer Richtlinie: Da Sie die Richtlinie bearbeiten, ist das Namensfeld ausgegraut.  Klicken Sie auf **Weiter**.
    1. Überprüfen und Fertigstellen: Da nichts geändert wurde, wählen Sie **Abbrechen** aus.

1. Wählen Sie im linken Navigationsbereich unter „Information Protection“ die Option **Richtlinien für die automatische Bezeichnung** aus. Schauen Sie sich die Beschreibung an. Achten Sie darauf, dass Sie Richtlinien für die automatische Anwendung von Bezeichnungen, um automatisch Vertraulichkeitsbezeichnungen auf E-Mail-Nachrichten oder OneDrive- und SharePoint-Dateien anzuwenden, die vertrauliche Informationen enthalten, erstellen. In unserem Mandanten wurden keine Richtlinien für automatische Bezeichnungen vorkonfiguriert. Um eine neue Richtlinie für automatische Bezeichnungen zu erstellen, wählen Sie **Richtlinie für automatische Bezeichnungen erstellen** aus.  Hier werden die Schritte zum Erstellen einer neuen Richtlinie beschrieben.
    1. Wählen Sie zunächst die Informationen aus, auf die diese Bezeichnung angewendet werden soll.  Beachten Sie die verfügbaren Optionen.  Wählen Sie **Medizin und Gesundheitswesen** und dann eine der verfügbaren Verordnungen aus, die als Vorlage dienen soll.  Wählen Sie **Weiter** aus.
    1. Sie können Ihre Richtlinie für die automatische Bezeichnung benennen oder den Standardnamen verwenden.  Wählen Sie **Weiter** aus.
    1. Als Nächstes wählen Sie eine Bezeichnung aus, die automatisch angewendet werden soll.  Wählen Sie **+ Bezeichnung auswählen**aus.  Wählen Sie eine Bezeichnung aus der Liste und dann **Hinzufügen** aus.
    1. Sie können die Administratoreinheiten zuweisen, für die diese Richtlinie gilt.  Lassen Sie die Standardeinstellung auf vollständiges Verzeichnis, und wählen Sie **Weiter** aus.
    1. Wählen Sie die Stellen aus, an denen Sie die Bezeichnung anwenden möchten.  Überprüfen Sie die bereitgestellten Informationen und die verfügbaren Stellen, die Sie auswählen können. Wählen Sie für diese Übung das Kontrollkästchen neben **Exchange-E-Mail** und dann **Weiter** aus.
    1. Sie können allgemeine oder erweiterte Regeln einrichten, die definieren, auf welchen Inhalt die Bezeichnung angewendet wird.  Lassen Sie die Standardeinstellung auf Allgemeine Regeln, und wählen Sie **Weiter** aus.
    1. Sie können Regeln für Inhalte an allen Speicherorten definieren.  Die Bezeichnung wird auf Inhalte angewendet, die den auf dieser Seite definierten Regeln entsprechen.  Für die ausgewählte Vorlage sollte eine Position angezeigt werden. Erweitern Sie sie, um die geltenden Bedingungen anzuzeigen.  Übernehmen Sie die Standardeinstellungen, und klicken Sie auf **Weiter**.
    1. Für E-Mails können zusätzliche Einstellungen konfiguriert werden. Übernehmen Sie die Standardwerte, und klicken Sie auf **Weiter**.
    1. Sie können die Richtlinie jetzt oder später testen.  Wählen Sie **Richtlinie deaktiviert lassen** und dann **Weiter** aus.
    1. Überprüfen Sie die Einstellungen. Im Rahmen dieser Übung können Sie die Erstellung der Richtlinie abbrechen. Wählen Sie **Abbrechen** aus.

1. Wählen Sie im linken Navigationsbereich **Startseite** aus, um zum Microsoft Purview-Portal zurückzukehren.

1. Lassen Sie diese Seite geöffnet, da Sie sie in der nächsten Aufgabe verwenden werden.

### Aufgabe 2

In dieser Aufgabe durchlaufen Sie den Prozess zum Anwenden einer Vertraulichkeitsbezeichnung auf ein Microsoft Word-Dokument und zeigen dann die Inhaltsmarkierung (Fußzeile) an, die von der Bezeichnung generiert wird. HINWEIS: Wenn Sie Microsoft Word online verwenden, kann es zu einer Verzögerung kommen, bevor die Option zum Auswählen von Vertraulichkeitsbezeichnungen im oberen Menüband angezeigt wird.  Es wird empfohlen, alle verbleibenden Labs abzuschließen und dann wieder zu dieser Aufgabe zurückzukehren.

1. Sie sollten sich immer noch auf der Startseite des Microsoft Purview Portals befinden. 
1. Wählen Sie im Microsoft Purview-Portal das Symbol **für den App Launcher** neben der Angabe „Microsoft Purview“ aus. Wählen Sie das **Word-Symbol** aus.  

1. Wählen Sie unter „Neu erstellen“ die Option **Leeres Dokument** aus, und geben Sie dann auf der Seite etwas Text ein.  Wählen Sie oben auf der Seite neben dem Word-Symbol die Option **Dokument** aus und benennen Sie die Datei in **Test-Label** um. Drücken Sie dann auf Ihrer Tastatur die **Eingabetaste**.

1. Ganz rechts auf der oberen Menüleiste (auch als Menüband bezeichnet) befindet sich ein Pfeil nach unten. Wählen Sie ihn aus, und wählen Sie dann **Klassisches Menüband** aus.  Dies vereinfacht das Erkennen des Vertraulichkeitssymbols. Wählen Sie neben dem Mikrofonsymbol die Option **Vertraulichkeit** aus. Wählen Sie im Dropdownmenü **Höchst Vertraulich** und dann **Alle Mitarbeiter** aus.  

1. Wählen Sie auf der oberen Menüleiste die Option **Ansicht** und dann die Ansicht **Lesebereich** aus.

1. Beachten Sie, dass das Dokument die Fußzeile „Als streng vertraulich klassifiziert“ enthält.  

1. Schließen Sie die Microsoft Word-Registerkarten, die in Ihrem Browser geöffnet sind, um Word zu beenden, aber lassen Sie die Browserregisterkarte mit der Microsoft Purview-Homepage geöffnet.

### Überprüfung

In diesem Lab haben Sie die Funktionen von Vertraulichkeitsbezeichnungen kennengelernt.  Sie haben die Einstellungen für eine vorhandene Vertraulichkeitsbezeichnung und die entsprechende Richtlinie zum Veröffentlichen der Bezeichnung kennengelernt.  Sie haben die Bezeichnung angewendet und, da die Bezeichnung Inhaltsmarkierungen enthält, konnten Sie diese Markierung in dem Dokument sehen, auf das Sie die Bezeichnung angewendet haben.
