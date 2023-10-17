<!---
---
Demo: Title: „Vertraulichkeitsbezeichnungen in Microsoft Purview“ Lernpfad/Modul/Lerneinheit: „Lernpfad: Beschreiben der Funktionen der Microsoft-Compliancelösungen; Modul 3: Beschreiben der Funktionen von Microsoft Purview zum Schutz von Informationen, zur Datenlebenszyklusverwaltung und zur Datengovernance; Lerneinheit 4: Beschreiben von Vertraulichkeitsbezeichnungen“
---
--->

# Demo: Vertraulichkeitsbezeichnungen in Microsoft Purview

Diese Demo ist den folgenden Learn-Inhalten zugeordnet:

- Lernpfad: Beschreiben der Funktionen der Microsoft-Compliancelösungen
- Modul: Beschreiben der Funktionen von Microsoft Purview zum Schutz von Informationen, zur Datenlebenszyklusverwaltung und zur Datenverwaltung
- Lerneinheit: Beschreiben von Vertraulichkeitsbezeichnungen

## Demoszenario

In dieser Demo zeigen Sie die Funktionen der Vertraulichkeitsbezeichnungen.  Sie durchlaufen die Einstellungen für vorhandene, bereits erstellte Vertraulichkeitsbezeichnungen und für die entsprechende Richtlinie zum Veröffentlichen der Bezeichnung.   Anschließend erfahren Sie, wie eine Bezeichnung angewendet wird, und welche Auswirkung diese Bezeichnung aus der Perspektive eines Benutzers hat.  **HINWEIS:** Wenn Sie Word zum ersten Mal online mit Ihrem Microsoft 365-Mandanten verwenden, kann es bis zu 15 Minuten dauern, bis die Option „Vertraulichkeit“ im Menüband angezeigt wird.  Referent*innen sollten den Demoteil 2 noch vor Kursbeginn ausführen, damit noch genügend Zeit bleibt, bis die Option angezeigt wird.

### Teil 1 der Demo

In dieser Demo zeigen Sie die Einstellungen für eine vorhandene Vertraulichkeitsbezeichnung und die entsprechende Richtlinie zum Veröffentlichen der Bezeichnung.

1. Öffnen Sie die Browserregisterkarte für die Startseite von Microsoft Purview.  Wenn Sie die Registerkarte zuvor geschlossen haben, öffnen Sie eine neue Browserregisterkarte, und geben Sie **https://admin.microsoft.com** ein. Melden Sie sich mit den Administratoranmeldeinformationen für den Microsoft 365-Mandanten an, der vom autorisierten Labhoster (ALH) bereitgestellt wird. Wählen Sie im linken Navigationsbereich von Microsoft 365 Admin Center **Alle anzeigen** und dann **Compliance** aus.  Die Startseite des Microsoft Purview-Complianceportals wird auf einer neuen Browserseite geöffnet.  

1. Erweitern Sie im linken Navigationsbereich unter Lösungen den Eintrag **Informationsschutz** und wählen Sie dann **Übersicht** aus.  Die Übersichtsseite enthält Informationen zu den wichtigsten Vertraulichkeitsbezeichnungen, die auf Inhalte angewendet werden, zu den wichtigsten erkannten Aktivitäten, zu Speicherorten, an denen Vertraulichkeitsbezeichnungen angewendet werden, und vieles mehr.  
    1. Möglicherweise sehen Sie auf der Übersichtsseite ein gelbes Informationsfeld, das anzeigt, dass Ihre Organisation die Fähigkeit zur Verarbeitung von Inhalten in Office-Onlinedateien, die mit verschlüsselten Vertraulichkeitsbezeichnungen versehen und in OneDrive und SharePoint gespeichert sind, nicht aktiviert hat.  Wählen Sie **Jetzt aktivieren** aus.  Nachdem Sie diese Aktion vorgenommen haben, kann es eine Verzögerung geben, bis die Einstellung vom System übernommen wurde.

1. Wählen Sie im linken Navigationsbereich **Bezeichnungen** aus.

1. Einige Bezeichnungen wurden in Ihrem Microsoft 365-Labmandanten vorkonfiguriert. Erweitern Sie die Bezeichnung namens **Streng Vertraulich**, indem Sie **>** und dann **Alle Mitarbeiter** auswählen.  Ein Fenster wird geöffnet, das Informationen über diese Bezeichnung bereitstellt.  Beachten Sie, wie diese Bezeichnung festgelegt ist, um die Verschlüsselung und Inhaltsmarkierung zu unterstützen.  Wählen Sie oben auf der Seite das **Stiftsymbol** aus, um einige der grundlegenden Konfigurationseinstellungen anzuzeigen. Wenn das Stiftsymbol nicht angezeigt wird, wählen Sie die Auslassungspunkte aus.
    1. Bei der Konfiguration werden zunächst ein Name und eine Beschreibung für Ihre Bezeichnung angegeben.  Nehmen Sie keine Änderungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.
    1. Beachten Sie den Bereich für diese Bezeichnung.  Der Bereich ist auf „Dateien & E-Mails“ festgelegt.  Nehmen Sie keine Änderungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.
    1. Auf diesem nächsten Bildschirm können Sie Schutzeinstellungen für die beschrifteten Elemente auswählen. Beachten Sie, dass diese Bezeichnung so konfiguriert ist, dass sie die Verschlüsselung und Inhaltskennzeichnung unterstützt. Nehmen Sie keine Änderungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.
        1. Im Fenster „Verschlüsselung“ wird die Konfiguration für die Verschlüsselungseinstellungen angezeigt. Überprüfen Sie die aktuellen Einstellungen, ändern Sie jedoch nichts. Beachten Sie, dass der Benutzerzugriff auf den Inhalt auf „Läuft nie ab“ festgelegt ist.  Sie können auch bestimmten Benutzern und Gruppen Berechtigungen zuweisen, damit nur diese mit Inhalt interagieren können, auf den diese Bezeichnung angewendet ist.  Der Mandant wird unter „Benutzer und Gruppen“ definiert. Entsprechend können alle Benutzer in Ihrem Mandanten Inhalt mit dieser Bezeichnung anzeigen.  Die Finanzabteilung ist ebenfalls aufgelistet und verfügt über Mitautorberechtigungen.  Nehmen Sie keine Änderungen an den Einstellungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.
        1. Beachten Sie auf der Seite „Inhaltsmarkierung“ das oben auf der Seite befindliche Informationsfeld.  Inhaltsmarkierungen werden auf Dokumente angewendet. Es werden aber nur Kopf- und Fußzeilen auf E-Mail-Nachrichten angewendet. Wasserzeichen werden entsprechend nicht auf E-Mails angewendet.  Die dieser Bezeichnung zugeordnete Inhaltsmarkierung ist ein Wasserzeichen.  Nehmen Sie keine Änderungen an den Einstellungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.
    1. Sie befinden sich nun im Fenster „Automatisches Anwenden von Bezeichnungen für Dateien und E-Mails“.  Lesen Sie oben auf der Seite die Beschreibung zum Anwenden der automatischen Bezeichnung und das darunter befindliche Informationsfeld.  Beachten Sie außerdem, dass diese Bezeichnung für das automatische Anwenden von Bezeichnungen für bestimmte Bedingungen festgelegt ist. Nehmen Sie keine Änderungen an den Einstellungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.
    1. In diesem nächsten Fenster werden Schutzeinstellungen für Teams, Gruppen und Sites festgelegt, wofür diese Bezeichnung gilt. Wenn sie nicht aktiviert ist, wählen Sie unten auf der Seite die Option **Weiter** aus.
    1. Dieses nächste Fenster ist eine Previewfunktion zum automatischen Anwenden dieser Bezeichnung auf schematisierte Datenobjekte in Microsoft Purview Data Map (wie etwa SQL, Synapse usw.), die Arten vertraulicher Informationen enthalten, die von Ihnen ausgewählt wurden.  Dieses Feature ist nicht aktiviert. Wählen Sie unten auf der Seite die Option **Abbrechen** aus, um den Assistenten für die Bezeichnungskonfiguration zu schließen und um zur Seite „Information Protection“ zurückzukehren.

1. Wählen Sie im linken Navigationsbereich **Bezeichnungsrichtlinien** aus.  Vertraulichkeitsbezeichnungen können aufgrund von Bezeichnungsrichtlinien veröffentlicht werden.  Der Microsoft 365-Mandant wurde zur Vereinfachung mit einigen Bezeichnungsrichtlinien konfiguriert.

1. Wählen Sie in diesem Fall **Richtlinie für globale Vertraulichkeitsbezeichnungen** aus.  Ein Fenster wird geöffnet, das Informationen über die Richtlinie bereitstellt.  Beachten Sie die Beschreibung. Diese Bezeichnungsrichtlinie wurde als Standardrichtlinie für Vertraulichkeitsbezeichnungen für alle Benutzer und Gruppen eingerichtet. Diese Richtlinie dient zum Veröffentlichen der meisten Bezeichnungen, die für diesen Microsoft 365-Lab-Mandanten vorkonfiguriert wurden und auf der Registerkarte „Bezeichnungen“ aufgeführt werden.

1. Wählen Sie oben im Fenster die **Richtlinie bearbeiten** aus.
    1. Lesen Sie die Beschreibung unter „Zu veröffentlichende Vertraulichkeitsbezeichnungen auswählen“.  Beachten Sie die aufgeführten Bezeichnungen.  Nehmen Sie keine Änderungen an den Einstellungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.
    1. Die nächste Seite ist eine Vorschau für das Zuweisen von Administratoreinheiten. Wählen Sie **Weiter** aus.
    1. Lesen Sie die Beschreibung unter „Für Benutzer und Gruppen veröffentlichen“.  Beachten Sie, dass diese Bezeichnung für alle Benutzer verfügbar ist.  Nehmen Sie keine Änderungen an den Einstellungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.
    1. Überprüfen Sie die Richtlinieneinstellungen.  Wählen Sie unten auf der Seite die Option **Weiter** aus.
    1. Lesen Sie die Beschreibung unter „Standardbezeichnung auf Dokumente anwenden“. Nehmen Sie keine Änderungen an den Einstellungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.
    1. Lesen Sie die Beschreibung unter „Standardbezeichnung auf E-Mails anwenden“. Nehmen Sie keine Änderungen an den Einstellungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.
    1. Lesen Sie die Beschreibung unter „Standardeinstellungen für Besprechungen und Kalenderereignisse“. Nehmen Sie keine Änderungen an den Einstellungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.
    1. Lesen Sie die Beschreibung unter „Standardbezeichnung auf Power BI-Inhalt anwenden“. Nehmen Sie keine Änderungen an den Einstellungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.
    1. Über die letzte Konfigurationsoption wird der Name Ihrer Richtlinie festgelegt.  Da Sie die Richtlinie bearbeiten, ist das Feld „Name“ abgeblendet. Wählen Sie unten auf der Seite **Weiter** aus.
    1. Überprüfen Sie die Richtlinieneinstellungen. Da nichts geändert wurde, wählen Sie **Abbrechen** aus, um zur Seite „Bezeichnungsrichtlinien“ zurückzukehren.

1. Wählen Sie auf der Seite „Information Protection“ die Option „Automatisches Bezeichnen“ aus. Sehen Sie sich die Beschreibung an. Beachten Sie, dass Sie Richtlinien für die automatische Anwendung von Bezeichnungen erstellen, um automatisch Vertraulichkeitsbezeichnungen auf E-Mail-Nachrichten oder OneDrive- und SharePoint-Dateien anzuwenden, die vertrauliche Informationen enthalten. Wenn Richtlinien zur automatischen Bezeichnung konfiguriert sind, wählen Sie eine aus, und überprüfen Sie die Richtlinieninformationen im Detailbereich.  Wenn keine Richtlinie aufgeführt ist und Ihre Zeit es erlaubt, können Sie die Schritte zum Erstellen einer Richtlinie durchlaufen.

1. Wählen Sie im linken Navigationsbereich die Startseite aus, um zur Startseite des Microsoft Purview-Complianceportals zurückzukehren.

1. Lassen Sie diese Browserregisterkarte geöffnet.

### Teil 2 der Demo

In diesem Schritt zeigen Sie den Prozess der Anwendung einer Bezeichnung aus der Perspektive des Benutzers (in diesem Fall ist der Benutzer der Administrator).  Um die Auswirkungen des Anwendens der Bezeichnung anzuzeigen, wählen Sie die Bezeichnung „Confidential – Finance“ (Vertraulich – Finanzen) aus, da diese Bezeichnung ein Wasserzeichen anwendet.

1. Wählen Sie auf der Startseite des Microsoft Purview-Complianceportals das **App-Startfeld-Symbol** aus, das sich neben dem Text „Contoso Electronics“ befindet. Wählen Sie das **Word-Symbol** aus.  

1. Wählen Sie **Leeres Dokument** aus. Geben Sie dann etwas Text auf der Seite ein.  Wählen Sie oben auf der Seite auf dem blauen Balken den Abwärtspfeil aus, der sich neben „DokumentXX – gespeichert“ befindet, und geben Sie in das Feld „Dateiname“ den Text **Testbezeichnung** ein. Drücken Sie dann die **EINGABETASTE** auf Ihrer Tastatur.

1. Wählen Sie in der oberen Menüleiste das Symbol **Vertraulichkeitssymbol** (das Symbol rechts neben dem Mikrofonsymbol) aus. Wenn diese Option nicht sofort angezeigt wird, aktualisieren Sie die Seite. Wählen Sie in der Dropdownliste den Eintrag **Confidential – Finance** (Vertraulich – Finanzen) aus.   HINWEIS: Wenn die Option „Vertraulichkeit“ nicht sofort angezeigt wird, aktualisieren Sie die Seite. Da es sich hier um eine Mandantenumgebung in einem Lab handelt, ist die Verzögerung möglicherweise länger als üblich (10-15 Minuten).
1. 
1. Wählen Sie auf der oberen Menüleiste die Option **Ansicht** und dann die Ansicht **Lesebereich** aus.

1. Beachten Sie, dass das Dokument das Wasserzeichen enthält.  

1. Schließen Sie die in Ihrem Browser geöffneten Microsoft Word-Registerkarten, um Word zu schließen.

1. Lassen Sie die Microsoft Purview-Browserregisterkarte für die nächste Demo geöffnet.

### Teil 3 der Demo (optional)

Erinnern Sie sich an den ersten Teil der Demo, in dem die Bezeichnung „Confidential – Finance“ für Verschlüsselung eingerichtet wird. Gemäß den Berechtigungen, die mit dieser Bezeichnung konfiguriert wurden, verfügen Benutzer im Contoso-Mandanten über Viewerberechtigungen für alle Dokumente/E-Mails, auf die die Bezeichnung angewendet wurde.  In diesem Abschnitt senden Sie ein zuvor erstelltes Dokument, das die Bezeichnung „Confidential – Finance“ enthält, an eine E-Mail-Adresse, auf die Sie Zugriff besitzen (eine persönliche E-Mail-Adresse oder Ihre Microsoft E-Mail-Adresse), die NICHT Teil der Domäne WWLxZZZZ.OnMicrosoft.com ist.  

1. Wählen Sie auf der Startseite des Microsoft Purview-Complianceportals das **App-Startfeld-Symbol** aus, das sich neben dem Text „Contoso Electronics“ befindet. Wählen Sie das **Outlook-Symbol** aus.

1. Wählen Sie in der oberen linken Ecke des Bildschirms die Option **Neue E-Mail** aus.  Geben Sie eine E-Mail-Adresse ein, auf die Sie zugreifen können und die kein Bestandteil der Domäne „WWLxZZZZ.OnMicrosoft.com“ ist. Geben Sie dann **Test** in die Betreffzeile ein.

1. Wählen Sie im oberen Menüband das Büroklammersymbol und dann in der Dropdownliste unter den vorgeschlagenen Dateien das im vorherigen Schritt erstellte Dokument **Test-label** aus, um es an die E-Mail anzuhängen.

1. Drücken Sie **Senden**, um die E-Mail zu verschicken.

1. Überprüfen Sie das E-Mail-Konto, an das Sie das Dokument gesendet haben.  Beachten Sie, dass die E-Mail möglicherweise in Ihrem Junk-E-Mail-Ordner gelandet ist.  Die E-Mail wurde erfolgreich gesendet, aber wenn Sie versuchen, die angefügte Word-Datei zu öffnen, die ursprünglich mit der Bezeichnung „Confidential – Finance“ versehen wurde, wird eine Benachrichtigung angezeigt, dass Sie nicht über die Berechtigung zum Öffnen des Dokuments verfügen.

1. Schließen Sie Outlook.

1. Lassen Sie die Microsoft Purview-Browserregisterkarte für die nächste Demo geöffnet.


### Überprüfung

In dieser Demo haben Sie die Einstellungen kennengelernt, die für Vertraulichkeitsbezeichnungen konfiguriert werden können, sowie die Einstellungen für Richtlinien zum Veröffentlichen von Vertraulichkeitsbezeichnungen. Darüber hinaus haben Sie erfahren, wie eine Bezeichnung angewendet wird und welche Auswirkung sie aus Perspektive eines Benutzers hat.

