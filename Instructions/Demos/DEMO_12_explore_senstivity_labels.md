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

In dieser Demo zeigen Sie die Funktionen von Vertraulichkeitsbezeichnungen.  Sie durchlaufen die Einstellungen für vorhandene, bereits erstellte Vertraulichkeitsbezeichnungen und für die entsprechende Richtlinie zum Veröffentlichen der Bezeichnung.   Anschließend erfahren Sie, wie eine Bezeichnung angewendet wird, und welche Auswirkung diese Bezeichnung aus der Perspektive eines Benutzers hat.

**HINWEIS:** Wenn Sie Word mit Ihrem Microsoft 365-Mandanten online verwenden, kann es bis zu 15 Minuten dauern, bis das Symbol „Vertraulichkeit“ im Menüband angezeigt wird. Es wird empfohlen, dass referierende Personen Word online öffnen (wie in Demoteil 3 dargestellt), bevor Sie die vollständige Demo starten, damit genügend Zeit für die Anzeige der Option verfügbar ist.

### Teil 1 der Demo (optional)

Wenn das die erste Instanz ist, in der Sie eine Microsoft Purview-Lösung demonstrieren, empfiehlt es sich, ein paar Minuten lang eine Einführung in das Microsoft Purview-Portal zu geben, bevor Sie Vertraulichkeitsbezeichnungen vorstellen.

1. Öffnen Sie Microsoft Edge, und geben Sie in der Adressleiste **https://purview.microsoft.com** ein. Melden Sie sich mit den Anmeldeinformationen an, die vom autorisierten Labhoster bereitgestellt werden, und wählen Sie dann **Erste Schritte** aus.  

1. Bevor Sie sich mit Vertraulichkeitsbezeichnungen befassen, nehmen Sie sich ein paar Minuten Zeit, um das Microsoft Purview-Portal zu erkunden.

1. Wählen Sie die Kachel **Alle Lösungen anzeigen** aus, um die Gruppierung für die Microsoft Purview-Lösungen anzuzeigen.

1. Im linken Navigationsbereich sehen Sie Optionen für Lösungen, Learn, Einstellungen und kürzlich ausgewählte Lösungen.
    1. **Lösungen** Dadurch wird ein neues Panel mit allen Lösungen und verwandten Portalen geöffnet.
    1. Unter **Learn** erfahren Sie, wie Sie Links zu Dokumenten, Videos und Blogs anzeigen können.
    1. **Einstellungen**. Erkunden Sie diese Optionen nach Belieben. Hier können Sie Rollen und Bereiche, Datenconnectoren und alle Lösungseinstellungen konfigurieren.

1. Wählen Sie im linken Navigationsbereich **Home** aus, um zur Homepage zurückzugelangen.

### Teil 2 der Demo

In dieser Demo zeigen Sie die Einstellungen für eine vorhandene Vertraulichkeitsbezeichnung und die entsprechende Richtlinie zum Veröffentlichen der Bezeichnung.

1. Sie sollten sich auf der Startseite des Microsoft Purview-Portals befinden.  Öffnen Sie andernfalls eine Browserregisterkarte in Microsoft Edge, geben Sie **`https://puriview.microsoft.com`** ein, und melden Sie sich mit den Anmeldeinformationen an, die vom autorisierten Labhoster bereitgestellt werden.

1. Wählen Sie auf der Startseite des neuen Microsoft Purview-Portals die Kachel **Alle Lösungen anzeigen** und dann die Kachel **Informationsschutz** aus. Wählen Sie alternativ im linken Navigationsbereich **Lösungen** und dann **Information Protection** aus.

1. Sie gelangen auf die Übersichtsseite. Wählen Sie im linken Navigationsbereich **Vertraulichkeitsbezeichnungen** aus. Wenn ein gelbes Banner angezeigt wird, bedeutet dies, dass Ihre Organisation die Funktion zur Verarbeitung von Inhalten in Office-Online-Dateien, die mit verschlüsselten Vertraulichkeitsbezeichnungen versehen und in OneDrive und SharePoint gespeichert sind, nicht aktiviert hat.  Wählen Sie **Jetzt aktivieren** aus

1. Einige Bezeichnungen wurden in Ihrem Microsoft 365-Labmandanten vorkonfiguriert. Erweitern Sie die Bezeichnung **Streng vertraulich** und wählen Sie dann **Alle Mitarbeitenden** aus.  Ein Fenster wird geöffnet, das Informationen über diese Bezeichnung bereitstellt.  Beachten Sie die Einstellungen für diese Bezeichnung.  Wählen Sie **Bezeichnung bearbeiten** aus. Wenn diese Option nicht angezeigt wird, wählen Sie die Auslassungspunkte aus.
    1. Die Konfiguration beginnt mit der Bereitstellung grundlegender Details für die Bezeichnung.  Nehmen Sie keine Änderungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.
    1. Beachten Sie den Bereich für diese Bezeichnung. Nehmen Sie keine Änderungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.
    1. Auf diesem nächsten Bildschirm können Sie Schutzeinstellungen für die beschrifteten Elemente auswählen. Diese Bezeichnung steuert, wer auf gekennzeichnete Elemente zugreifen und diese anzeigen kann, und wendet auch die Inhaltskennzeichnung an.  Wählen Sie **Weiter** aus, um die Details anzuzeigen.
        1. Zugriffssteuerung: Überprüfen Sie die Einstellungen, ändern Sie jedoch nichts.  Wählen Sie **Weiter** aus.
        1. Inhaltskennzeichnung: Beachten Sie, dass die Bezeichnung eine Fußzeile anwendet.  Wählen Sie anschließend **Weiter** aus.
        1. Automatische Bezeichnungen für Dateien und E-Mails: Lesen Sie oben auf der Seite die Beschreibung zum Anwenden der automatischen Bezeichnung und das darunter befindliche Informationsfeld.  Beachten Sie außerdem, dass diese Bezeichnung für die automatische Bezeichnung festgelegt ist, wenn Kreditkartennummern erkannt werden. Nehmen Sie keine Änderungen an den Einstellungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.
    1. Definieren von Schutzeinstellungen für Gruppen und Websites: Überprüfen Sie die Optionen für Schutzeinstellungen und automatisches Anwenden von Einstellungen.  In diesem Fenster wurde nichts konfiguriert.  Nehmen Sie keine Änderungen vor. Wählen Sie unten auf der Seite die Option **Weiter** aus.
    1. Überprüfen Sie Ihre Einstellungen und schließen Sie folgendes ab: Überprüfen Sie Ihre Einstellungen.  Da nichts geändert wurde, wählen Sie **Abbrechen** aus.

1. Erweitern Sie im linken Navigationsbereich **Richtlinien** und wählen Sie dann **Richtlinien zur Bezeichnungsveröffentlichung** aus.  Vertraulichkeitsbezeichnungen können aufgrund von Bezeichnungsrichtlinien veröffentlicht werden.  Der Microsoft 365-Mandant wurde zur Vereinfachung mit einigen Bezeichnungsrichtlinien konfiguriert. Wählen Sie die Richtlinie **Streng vertrauliche Richtlinie** aus.  Ein Fenster wird geöffnet, das Informationen über die Richtlinie bereitstellt. Wählen Sie oben im Fenster die **Richtlinie bearbeiten** aus.  Hier werden Sie durch die Einstellungen geführt, ohne etwas zu ändern.
    1. Wählen Sie zu veröffentlichende Vertraulichkeitsbezeichnungen aus:  Beachten Sie die aufgelisteten Bezeichnungen.  Nehmen Sie keine Änderungen an den Einstellungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.
    1. Zuweisen von Administratoreinheiten: Die Administratoreinheiten sind auf das vollständige Verzeichnis festgelegt. Ändern Sie keine der Einstellungen. Wählen Sie **Weiter** aus.  
    1. Veröffentlichen für Benutzende und Gruppen:  Beachten Sie, dass diese Bezeichnung für alle Benutzer verfügbar ist.  Nehmen Sie keine Änderungen an den Einstellungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.
    1. Richtlinieneinstellungen: Beachten Sie die verfügbaren Optionen. Nehmen Sie keine Änderungen an den Einstellungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.
    1. Standardeinstellungen für Dokumente: Nehmen Sie keine Änderungen an den Einstellungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.
    1. Standardeinstellungen für E-Mails: Überprüfen Sie die Optionen und beachten Sie, dass E-Mails eine Bezeichnung von einer Anlage mit höherer Priorität erben können, sofern dies konfiguriert ist. Wählen Sie **Weiter** aus.
    1. Standardeinstellungen für Besprechungen und Kalenderereignisse: Überprüfen Sie die Optionen und beachten Sie die Option zum Anwenden der Vererbung zwischen Teambesprechungen und Artefakten. Nehmen Sie keine Änderungen an den Einstellungen vor.  Wählen Sie **Weiter** aus.
    1. Standardeinstellungen für Fabric- und Power BI-Inhalte: Nehmen Sie keine Änderungen an den Einstellungen vor.  Wählen Sie **Weiter** aus.
    1. Benennen Ihrer Richtlinie: Da Sie die Richtlinie bearbeiten, ist das Namensfeld ausgegraut.  Klicken Sie auf **Weiter**.
    1. Überprüfen und Fertigstellen: Da nichts geändert wurde, wählen Sie **Abbrechen** aus.

1. Wählen Sie im linken Navigationsbereich unter „Information Protection“ die Option „Automatische Bezeichnung“ aus. Schauen Sie sich die Beschreibung an. Achten Sie darauf, dass Sie Richtlinien für die automatische Anwendung von Bezeichnungen, um automatisch Vertraulichkeitsbezeichnungen auf E-Mail-Nachrichten oder OneDrive- und SharePoint-Dateien anzuwenden, die vertrauliche Informationen enthalten, erstellen. Wenn Richtlinien für die automatische Bezeichnung konfiguriert sind, wählen Sie eine aus, und lesen Sie die Richtlinieninformationen im Detailbereich.  Wenn keine Richtlinie aufgeführt ist, können Sie die Schritte zum Erstellen durchlaufen, sofern dies die Zeit zulässt.

1. Wählen Sie im linken Navigationsbereich „Startseite“ aus, um zum Microsoft Purview-Portal zurückzugehen.

1. Halten Sie diese Browser-Registerkarte offen.

### Teil 3 der Demo

In diesem Schritt durchlaufen Sie den Prozess zum Anwenden einer Vertraulichkeitsbezeichnung auf ein Microsoft Word-Dokument und zeigen dann die Inhaltskennzeichnung (Fußzeile) an, die von der Bezeichnung generiert wird. HINWEIS: Wenn Sie Microsoft Word online verwenden, kann es zu einer Verzögerung kommen, bevor die Option zum Auswählen von Vertraulichkeitsbezeichnungen im oberen Menüband angezeigt wird.  Es wird empfohlen, alle verbleibenden Labs abzuschließen und dann wieder zu dieser Aufgabe zurückzukehren.

1. Sie sollten sich immer noch auf der Startseite des Microsoft Purview Portals befinden. 
1. Wählen Sie im Microsoft Purview-Portal das Symbol **für den App Launcher** neben der Angabe „Microsoft Purview“ aus. Wählen Sie das **Word-Symbol** aus.  

1. Wählen Sie unter „Neu erstellen“ die Option **Leeres Dokument** aus, und geben Sie dann auf der Seite etwas Text ein.  Wählen Sie oben auf der Seite neben dem Word-Symbol die Option **Dokument** aus und benennen Sie die Datei in **Test-Label** um. Drücken Sie dann auf Ihrer Tastatur die **Eingabetaste**.

1. Ganz rechts auf der oberen Menüleiste (auch als Menüband bezeichnet) befindet sich ein Pfeil nach unten. Wählen Sie ihn aus, und wählen Sie dann **Klassisches Menüband** aus.  Dies vereinfacht das Erkennen des Vertraulichkeitssymbols. Wählen Sie neben dem Mikrofonsymbol die Option **Vertraulichkeit** aus. Wählen Sie im Dropdownmenü **Streng Vertraulich** und dann **Alle Mitarbeitenden** aus.  

1. Wählen Sie auf der oberen Menüleiste die Option **Ansicht** und dann die Ansicht **Lesebereich** aus.

1. Beachten Sie, dass das Dokument die Fußzeile „Klassifiziert als streng vertraulich“ enthält.  

1. Schließen Sie die Microsoft Word-Registerkarten, die in Ihrem Browser geöffnet sind, um Word zu beenden, aber lassen Sie die Browserregisterkarte mit der Microsoft Purview-Homepage geöffnet.

### Überprüfung

In dieser Demo haben Sie die Einstellungen gezeigt, die für Vertraulichkeitsbezeichnungen und die Einstellungen für Richtlinien zum Veröffentlichen von Vertraulichkeitsbezeichnungen konfiguriert werden können. Außerdem haben Sie gezeigt, wie man eine Bezeichnung anwendet.
