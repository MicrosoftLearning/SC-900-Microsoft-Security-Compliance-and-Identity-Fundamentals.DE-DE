<a name="---"></a><!---
---
Lab: Title: 'Erkunden von Vertraulichkeitsbezeichnungen in Microsoft Purview' Learning Path/Module/Unit: 'Lernpfad: Beschreiben der Funktionen der Microsoft-Compliancelösungen; Modul 3: Beschreiben von Information Protection und Datenlebenszyklusverwaltung in Microsoft Purview; Lerneinheit 4: Beschreiben von Vertraulichkeitsbezeichnungen'
---
--->

# <a name="lab-explore-sensitivity-labels-in-microsoft-purview"></a>Lab: Erkunden von Vertraulichkeitsbezeichnungen in Microsoft Purview

Dieses Lab ist den folgenden Learn-Inhalten zugeordnet:

- Lernpfad: Beschreiben der Funktionen der Microsoft-Compliancelösungen
- Modul: Beschreiben von Information Protection und Datenlebenszyklusverwaltung in Microsoft Purview
- Lerneinheit: Beschreiben von Vertraulichkeitsbezeichnungen

## <a name="lab-scenario"></a>Labszenario

In diesem Lab erkunden Sie die Funktionen von Vertraulichkeitsbezeichnungen.  Sie durchlaufen die Einstellungen für vorhandene, bereits erstellte Vertraulichkeitsbezeichnungen und für die entsprechende Richtlinie zum Veröffentlichen der Bezeichnung.   Anschließend erfahren Sie, wie eine Bezeichnung angewendet wird, und welche Auswirkung diese Bezeichnung aus der Perspektive eines Benutzers hat.

**Geschätzte Dauer**: 20 bis 25 Minuten

### <a name="task-1"></a>Aufgabe 1

In dieser Aufgabe erfahren Sie, wozu Vertraulichkeitsbezeichnungen dienen, indem Sie die Einstellungen für eine bereits erstellte Vertraulichkeitsbezeichnung und für die entsprechende Richtlinie zum Veröffentlichen der Bezeichnung durchgehen.

1. Öffnen Sie Microsoft Edge. Geben Sie **admin.microsoft.com** in die Adressleiste ein.

1. Melden Sie sich mit Ihren Administratoranmeldeinformationen an.
    1. Geben Sie **admin@WWLxZZZZZZ.onmicrosoft.com** (ZZZZZZ ist hierbei die eindeutige Mandanten-ID, die von Ihrem Lab-Hostinganbieter bereitgestellt wurde) in das Anmeldefenster ein, und wählen Sie dann **Weiter** aus.

    1. Geben Sie das Administratorkennwort ein, das von Ihrem Lab-Hostinganbieter bereitgestellt werden sollte. Wählen Sie **Anmelden**.
    1. Wählen Sie **Ja** aus, wenn Sie gefragt werden, ob Sie angemeldet bleiben möchten. Dadurch gelangen Sie zur Seite „Microsoft 365 Admin Center“.

1. Wählen Sie im linken Navigationsbereich von Microsoft 365 Admin Center **Alle anzeigen** aus.

1. Wählen Sie unter „Admin Center“ die Option **Compliance** aus.  Die Startseite des Microsoft Purview-Complianceportals wird auf einer neuen Browserseite geöffnet.  

1. Wählen Sie im linken Navigationsbereich **Information Protection** unter „Lösungen“ aus.

1. Beachten Sie auf der Übersichtsseite, dass das gelbe Informationsfeld anzeigt, dass Ihre Organisation die Fähigkeit zur Verarbeitung von Inhalten in Office-Onlinedateien, die mit verschlüsselten Vertraulichkeitsbezeichnungen versehen und in OneDrive und SharePoint gespeichert sind, nicht aktiviert hat.  Wählen Sie **Jetzt aktivieren** aus.  Nachdem Sie diese Aktion vorgenommen haben, kann es eine Verzögerung geben, bis die Einstellung vom System übernommen wurde.  Lesen Sie auch die Informationen, die auf dieser Übersichtsseite verfügbar sind.

1. Wählen Sie oben auf der Seite die Registerkarte **Bezeichnungen** aus.

1. Beachten Sie in der Mitte der Seite, dass bereits Bezeichnungen erstellt wurden.  Wählen Sie **Vertraulich – Finanzen** aus.  Ein Fenster wird geöffnet, das Informationen über diese Bezeichnung bereitstellt.  Beachten Sie, wie diese Bezeichnung festgelegt ist, um die Verschlüsselung und Inhaltsmarkierung zu unterstützen.  Wählen Sie oben auf der Seite **Bezeichnung bearbeiten** aus, um einige der grundlegenden Konfigurationseinstellungen anzuzeigen.  Wenn Sie die verschiedenen Einstellungen durchgehen und anzeigen, nehmen Sie KEINE Änderungen vor.

1. Bei der Konfiguration werden zunächst ein Name und eine Beschreibung für Ihre Bezeichnung angegeben.  Nehmen Sie keine Änderungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.

1. Beachten Sie den Bereich für diese Bezeichnung.  Der Bereich ist auf **Elemente** festgelegt.  Lesen Sie die Beschreibung, aber ändern Sie nichts.  Wählen Sie unten auf der Seite die Option **Weiter** aus.

1. Für den ausgewählten Bereich (Elemente) können Sie den Inhalt so konfigurieren, dass er verschlüsselt und/oder markiert wird.  Beachten Sie, wie die Schutzeinstellungen für Dateien und E-Mails für die Verschlüsselung und Markierung des Inhalts der Dateien festgelegt sind.  Überprüfen Sie die jeweilige Definition.  Nehmen Sie keine Änderungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.

1. Im Fenster „Verschlüsselung“ wird die Konfiguration für die Verschlüsselungseinstellungen angezeigt.  Nehmen Sie keine Änderungen vor.  Überprüfen Sie das Informationsfeld unter „Verschlüsselungseinstellungen konfigurieren“, und überprüfen Sie die konfigurierten Einstellungen. Beachten Sie, dass der Benutzerzugriff auf den Inhalt auf „Läuft nie ab“ festgelegt ist.  Sie können auch bestimmten Benutzern und Gruppen Berechtigungen zuweisen, damit nur diese mit Inhalt interagieren können, auf den diese Bezeichnung angewendet ist.  Der Mandant wird unter „Benutzer und Gruppen“ definiert. Entsprechend können alle Benutzer in Ihrem Mandanten Inhalt mit dieser Bezeichnung anzeigen.  Die Finanzabteilung ist ebenfalls aufgelistet und verfügt über Mitautorberechtigungen.  Nehmen Sie keine Änderungen an den Einstellungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.

1. Beachten Sie auf der Seite „Inhaltsmarkierung“ das oben auf der Seite befindliche Informationsfeld.  Inhaltsmarkierungen werden auf Dokumente angewendet. Es werden aber nur Kopf- und Fußzeilen auf E-Mail-Nachrichten angewendet. Wasserzeichen werden entsprechend nicht auf E-Mails angewendet.  Die dieser Bezeichnung zugeordnete Inhaltsmarkierung ist ein Wasserzeichen mit dem Namen STRENG VERTRAULICH.  Nehmen Sie keine Änderungen an den Einstellungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.

1. Sie befinden sich nun im Fenster „Automatisches Anwenden von Bezeichnungen für Dateien und E-Mails“.  Lesen Sie oben auf der Seite die Beschreibung zum Anwenden der automatischen Bezeichnung und das darunter befindliche Informationsfeld.  Beachten Sie außerdem, dass diese Bezeichnung für das automatische Anwenden von Bezeichnungen für bestimmte Bedingungen festgelegt ist. Nehmen Sie keine Änderungen an den Einstellungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.

1. In diesem nächsten Fenster werden Schutzeinstellungen für Gruppen und Sites festgelegt, für die diese Bezeichnung angewendet wird. Wenn sie nicht aktiviert ist, wählen Sie unten auf der Seite die Option **Weiter** aus.

1. Dieses nächste Fenster ist eine Vorschaufunktion für die automatische Bezeichnung für schematisierte Datenressourcen. Lesen Sie die Beschreibung.  Dieses Feature ist nicht aktiviert. Wählen Sie unten auf der Seite die Option **Abbrechen** aus, um den Assistenten für die Bezeichnungskonfiguration zu schließen und um zur Seite „Information Protection“ zurückzukehren.

1. Wählen Sie im oberen Bereich der Seite „Information Protection“ die Option **Bezeichnungsrichtlinien** aus.  Vertraulichkeitsbezeichnungen können aufgrund von Bezeichnungsrichtlinien veröffentlicht werden.  

1. Wählen Sie in diesem Fall **Richtlinie für globale Vertraulichkeitsbezeichnungen** aus.  Ein Fenster wird geöffnet, das Informationen über die Richtlinie bereitstellt.  Beachten Sie die Beschreibung. Dies ist die Standardrichtlinie für Vertraulichkeitsbezeichnungen für alle Benutzer und Gruppen. Diese Richtlinie dient zum Veröffentlichen der meisten Bezeichnungen, die für diesen Microsoft 365-Lab-Mandanten vorkonfiguriert wurden und auf der Registerkarte „Bezeichnungen“ aufgeführt werden.  

1. Wählen Sie oben im Fenster die **Richtlinie bearbeiten** aus.
    1. Lesen Sie die Beschreibung unter „Zu veröffentlichende Vertraulichkeitsbezeichnungen auswählen“.  Beachten Sie die aufgelistete Bezeichnung.  Nehmen Sie keine Änderungen an den Einstellungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.
    1. Lesen Sie die Beschreibung unter „Für Benutzer und Gruppen veröffentlichen“.  Beachten Sie, dass diese Bezeichnung für alle Benutzer verfügbar ist.  Nehmen Sie keine Änderungen an den Einstellungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.
    1. Überprüfen Sie die Richtlinieneinstellungen.  Wählen Sie die Option **Benutzer müssen eine Bezeichnung auf ihre E-Mails und Dokumente anwenden** aus. Überprüfen Sie die bereitgestellte Beschreibung. Wählen Sie unten auf der Seite die Option **Weiter** aus.
    1. Lesen Sie die Beschreibung unter „Standardbezeichnung auf Dokumente anwenden“. Wählen Sie im Feld „Standardbezeichnung“ den Abwärtspfeil aus, und wählen Sie dann **Allgemein/Alle Mitarbeiter (uneingeschränkt)** aus.  Wählen Sie unten auf der Seite die Option **Weiter** aus.
    1. Lesen Sie die Beschreibung unter „Standardbezeichnung auf E-Mails anwenden“. Nehmen Sie keine Änderungen an den Einstellungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.
    1. Lesen Sie die Beschreibung unter „Standardbezeichnung auf Power BI-Inhalt anwenden“. Nehmen Sie keine Änderungen an den Einstellungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.
    1. Über die letzte Konfigurationsoption wird der Name Ihrer Richtlinie festgelegt.  Da Sie die Richtlinie bearbeiten, ist das Feld „Name“ abgeblendet. Wählen Sie unten auf der Seite **Weiter** aus.
    1. Überprüfen Sie die Richtlinieneinstellungen, und wählen Sie **Übermitteln** und dann **Fertig** aus, um zur Seite „Informationsschutz“ zurückzukehren.

1. Wählen Sie auf der Seite „Information Protection“ die Option „Automatisches Bezeichnen“ aus.  Beachten Sie, dass dort keine automatische Bezeichnungsrichtlinie konfiguriert ist.  Nehmen Sie keine Änderungen an den Einstellungen vor.  Wenn Sie sich fragen, weshalb hier keine Richtlinie vorhanden ist, obwohl die Bezeichnungskonfiguration so festgelegt ist, dass die Bezeichnungen auf Dateien und E-Mails automatisch angewendet werden, kehren Sie zu den Schritten zurück, in denen Sie die Bezeichnungskonfigurationseinstellungen durchgegangen sind. Überprüfen Sie die Beschreibung und Informationsfelder, die „Automatisches Anwenden von Bezeichnungen für Dateien und E-Mails“ zugeordnet sind.  Hinweis:  Auf der Registerkarte „Automatisches Bezeichnen“ für die Vertraulichkeitsbezeichnung wird  „Sie müssen eine automatische Bezeichnungsrichtlinie erstellen, um diese Bezeichnung automatisch auf bereits (in SharePoint und OneDrive) gespeicherte Dateien oder auf bereits durch Exchange verarbeitete E-Mails anzuwenden“ angezeigt.

1. Wählen Sie im linken Navigationsbereich die Startseite aus, um zur Startseite des Microsoft Purview-Complianceportals zurückzukehren.

1. Lassen Sie diese Seite geöffnet, da Sie sie in der nächsten Aufgabe verwenden werden.

### <a name="task-2"></a>Aufgabe 2

In dieser Aufgabe durchlaufen Sie den Prozess der Anwendung einer Bezeichnung aus Perspektive des Benutzers (in diesem Fall ist der Benutzer der Administrator) und sehen die durch die Bezeichnung generierte Inhaltsmarkierung an.

1. Wählen Sie auf der Startseite des Microsoft Purview-Complianceportals das **App-Startfeld-Symbol** aus, das sich neben dem Text „Contoso Electronics“ befindet. Wählen Sie das **Word-Symbol** aus.  

1. Wählen Sie unter „Neu erstellen“ die Option **Leeres Dokument** aus, und geben Sie dann auf der Seite etwas Text ein.  Wählen Sie oben auf der Seite den Abwärtspfeil aus, der sich neben „DokumentXX – gespeichert“ befindet, und geben Sie in das Feld „Dateiname“ den Text **Testbezeichnung** ein. Drücken Sie dann die **EINGABETASTE** auf Ihrer Tastatur.

1. Wählen Sie in der oberen Menüleiste das **Vertraulichkeitssymbol** aus – das Symbol rechts neben dem Mikrofonsymbol (je nach Bildschirmgröße müssen Sie möglicherweise die Auslassungspunkte und dann die Option „Vertraulichkeit“ auswählen). Wählen Sie in der Dropdownliste den Eintrag **Confidential – Finance** (Vertraulich – Finanzen) aus.  HINWEIS: Wenn die Option „Vertraulichkeit“ nicht sofort angezeigt wird, aktualisieren Sie die Seite. Da es sich hier um eine Mandantenumgebung in einem Lab handelt, ist die Verzögerung möglicherweise länger als üblich (10-15 Minuten).

1. Wählen Sie auf der oberen Menüleiste die Option **Ansicht** und dann die Ansicht **Lesebereich** aus.

1. Beachten Sie, dass das Dokument das Wasserzeichen enthält.  

1. Schließen Sie die in Ihrem Browser geöffneten Microsoft Word-Registerkarten, um Word zu schließen.

### <a name="task-3-optional"></a>Aufgabe 3 (optional)

Erinnern Sie sich an den ersten Teil der Demo, in dem die Bezeichnung „Confidential – Finance“ für Verschlüsselung eingerichtet wird. Gemäß den Berechtigungen, die mit dieser Bezeichnung konfiguriert wurden, verfügen Benutzer im Contoso-Mandanten über Viewerberechtigungen für alle Dokumente/E-Mails, auf die die Bezeichnung angewendet wurde.  In diesem Abschnitt senden Sie ein zuvor erstelltes Dokument, das die Bezeichnung „Confidential – Finance“ enthält, an eine E-Mail-Adresse, auf die Sie Zugriff besitzen (d. h. eine persönliche E-Mail-Adresse oder Ihre Microsoft E-Mail-Adresse), die NICHT Teil der Domäne WWLxZZZZ.OnMicrosoft.com ist.  

1. Wählen Sie auf der Startseite des Microsoft Purview-Complianceportals das **App-Startfeld-Symbol** aus, das sich neben dem Text „Contoso Electronics“ befindet. Wählen Sie das **Outlook-Symbol** aus.

1. Wählen Sie in der oberen linken Ecke des Bildschirms die Option **Neue E-Mail** aus.  Geben Sie eine E-Mail-Adresse ein, auf die Sie zugreifen können und die kein Bestandteil der Domäne „WWLxZZZZ.OnMicrosoft.com“ ist. Geben Sie dann **Test** in die Betreffzeile ein.

1. Wählen Sie **Anfügen** (das Büroklammersymbol) aus.

1. Wählen Sie **OneDrive** aus.

1. Stellen Sie sicher, dass die Registerkarte **Zuletzt verwendet** im linken Navigationsbereich ausgewählt ist.  Wählen Sie in der angezeigten Liste das von Ihnen erstellte Dokument aus, auf das Sie die Bezeichnung **Testbezeichnung** angewendet haben. Wählen Sie **Weiter** und dann **Als Kopie anfügen** aus.  Klicken Sie auf **Senden**.

1. Überprüfen Sie das E-Mail-Konto, an das Sie das Dokument gesendet haben.  Beachten Sie, dass die E-Mail möglicherweise in Ihrem Junk-E-Mail-Ordner gelandet ist.  Die E-Mail wurde erfolgreich gesendet, aber wenn Sie versuchen, die angefügte Word-Datei zu öffnen, die ursprünglich mit der Bezeichnung „Confidential – Finance“ versehen wurde, wird eine Benachrichtigung angezeigt, dass Sie nicht über die Berechtigung zum Öffnen des Dokuments verfügen.

1. Schließen Sie die geöffneten Browserregisterkarten.

### <a name="review"></a>Überprüfung

In diesem Lab erkunden Sie die Funktionen von Vertraulichkeitsbezeichnungen.  Sie gehen die Einstellungen für vorhandene, bereits erstellte Vertraulichkeitsbezeichnungen und für die entsprechende Richtlinie zum Veröffentlichen der Bezeichnung durch.   Anschließend erfahren Sie, wie eine Bezeichnung angewendet wird, und welche Auswirkung diese Bezeichnung aus der Perspektive eines Benutzers hat.
