---
lab:
  title: Erkunden von Vertraulichkeitsbezeichnungen in Microsoft 365
  module: 'Module 4 Lesson 3: Describe the capabilities of Microsoft compliance solutions: Describe information protection and governance capabilities of Microsoft 365'
ms.openlocfilehash: ab8d44cf92697deb200bf968a1865d328025984b
ms.sourcegitcommit: c14538b208890797642cfe5c35abf6bea45364bf
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/15/2022
ms.locfileid: "142614445"
---
# <a name="lab-explore-sensitivity-labels-in-microsoft-365"></a>Lab: Erkunden von Vertraulichkeitsbezeichnungen in Microsoft 365

## <a name="lab-scenario"></a>Labszenario
In diesem Lab erkunden Sie die Funktionen von Vertraulichkeitsbezeichnungen.  Sie gehen die Einstellungen für vorhandene, bereits erstellte Vertraulichkeitsbezeichnungen und für die entsprechende Richtlinie zum Veröffentlichen der Bezeichnung durch.   Anschließend erfahren Sie, wie eine Bezeichnung angewendet wird, und welche Auswirkung diese Bezeichnung aus Perspektive eines Benutzers hat.


**Geschätzte Dauer**: 20 bis 25 Minuten

#### <a name="task-1-in-this-task-you-will-gain-an-understanding-of-what-sensitivity-labels-can-do-by-going-through-the-settings-for-an-existing-sensitivity-label-that-have-been-created-and-the-corresponding-policy-to-publish-the-label"></a>Aufgabe 1: In dieser Aufgabe erfahren Sie, wozu Vertraulichkeitsbezeichnungen dienen, indem Sie die Einstellungen für eine bereits erstellte Vertraulichkeitsbezeichnung und für die entsprechende Richtlinie zum Veröffentlichen der Bezeichnung durchgehen.

1. Öffnen Sie Microsoft Edge. Geben Sie **admin.microsoft.com** in die Adressleiste ein.

1. Melden Sie sich mit Ihren Administratoranmeldeinformationen an.
    1. Geben Sie **admin@WWLxZZZZZZ.onmicrosoft.com** (ZZZZZZ ist hierbei die eindeutige Mandanten-ID, die von Ihrem Labhostinganbieter bereitgestellt wurde) in das Fenster „Anmelden“ ein, und wählen Sie dann **Weiter** aus.
    
    1. Geben Sie das Administratorkennwort ein, das Sie vom Labhostinganbieter erhalten haben sollten. Wählen Sie **Anmelden**.
    1. Wählen Sie **Ja** aus, wenn Sie gefragt werden, ob Sie angemeldet bleiben möchten. Dadurch gelangen Sie zur Seite „Microsoft 365 Admin Center“.

1. Wählen Sie im linken Navigationsbereich von Microsoft 365 Admin Center **Alle anzeigen** aus.

1. Wählen Sie unter „Admin Center“ die Option **Compliance** aus.  Die Startseite des Microsoft 365 Compliance Center wird auf einer neuen Browserseite geöffnet.  

1. Wählen Sie im linken Navigationsbereich **Information Protection** unter „Lösungen“ aus.

1. Wählen Sie oben auf der Seite die Registerkarte **Bezeichnungen** aus.

1. Daraufhin wird ein gelbes Informationsfeld mit dem folgenden Hinweis angezeigt: „Ihre Organisation hat die Möglichkeit zum Verarbeiten von Inhalten in Office-Online-Dateien, für die verschlüsselte Vertraulichkeitsbezeichnungen verwendet wurden und die in SharePoint oder auf OneDrive gespeichert sind, nicht aktiviert“.  Wählen Sie „Jetzt aktivieren“ aus.  Nachdem Sie diese Aktion vorgenommen haben, kann es eine Verzögerung geben, bis die Einstellung vom System übernommen wurde.


1. Beachten Sie in der Mitte der Seite, dass bereits Bezeichnungen erstellt wurden.  Wählen Sie **Vertraulich – Finanzen** aus.  Ein Fenster wird geöffnet, das Informationen über diese Bezeichnung bereitstellt.  Beachten Sie, wie diese Bezeichnung festgelegt ist, um die Verschlüsselung und Inhaltsmarkierung zu unterstützen.  Wählen Sie oben auf der Seite „Bezeichnung bearbeiten“ aus, um einige der grundlegenden Konfigurationseinstellungen anzuzeigen.

1. Bei der Konfiguration werden zunächst ein Name und eine Beschreibung für Ihre Bezeichnung angegeben.  Nehmen Sie keine Änderungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.

1. Beachten Sie den Bereich für diese Bezeichnung.  Der Bereich ist auf Dateien und E-Mails festgelegt, wofür Sie die Verschlüsselungs- und Inhaltsmarkierungseinstellungen konfigurieren können, um mit einer Bezeichnung versehene E-Mails und Office-Dateien zu schützen.  Nehmen Sie keine Änderungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.

1. Für den ausgewählten Bereich für Dateien und E-Mails können Sie den Inhalt so konfigurieren, dass er verschlüsselt bzw. markiert wird.  Beachten Sie, wie die Schutzeinstellungen für Dateien und E-Mails für die Verschlüsselung und Markierung des Inhalts der Dateien festgelegt sind.  Überprüfen Sie die jeweilige Definition.  Nehmen Sie keine Änderungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.

1. Im Fenster „Verschlüsselung“ wird die Konfiguration für die Verschlüsselungseinstellungen angezeigt.  Nehmen Sie keine Änderungen vor.  Überprüfen Sie das Informationsfeld unter „Verschlüsselungseinstellungen konfigurieren“, und überprüfen Sie die konfigurierten Einstellungen. Beachten Sie, dass der Benutzerzugriff auf den Inhalt auf „Läuft nie ab“ festgelegt ist.  Sie können auch bestimmten Benutzern und Gruppen Berechtigungen zuweisen, damit nur diese mit Inhalt interagieren können, auf den diese Bezeichnung angewendet ist.  Der Mandant wird unter „Benutzer und Gruppen“ definiert. Entsprechend können alle Benutzer in Ihrem Mandanten Inhalt mit dieser Bezeichnung anzeigen.  Die Finanzabteilung ist ebenfalls aufgelistet und verfügt über Mitautorberechtigungen.  Nehmen Sie keine Änderungen an den Einstellungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.

1. Beachten Sie auf der Seite „Inhaltsmarkierung“ das oben auf der Seite befindliche Informationsfeld.  Inhaltsmarkierungen werden auf Dokumente angewendet. Es werden aber nur Kopf- und Fußzeilen auf E-Mail-Nachrichten angewendet. Wasserzeichen werden entsprechend nicht auf E-Mails angewendet.  Die dieser Bezeichnung zugeordnete Inhaltsmarkierung ist ein Wasserzeichen mit dem Namen STRENG VERTRAULICH.  Nehmen Sie keine Änderungen an den Einstellungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.

1. Sie befinden sich nun im Fenster „Automatisches Anwenden von Bezeichnungen für Dateien und E-Mails“.  Lesen Sie oben auf der Seite die Beschreibung zum Anwenden der automatischen Bezeichnung und das darunter befindliche Informationsfeld.  Beachten Sie außerdem, dass diese Bezeichnung für das automatische Anwenden von Bezeichnungen für bestimmte Bedingungen festgelegt ist. Nehmen Sie keine Änderungen an den Einstellungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.

1. In diesem nächsten Fenster werden Schutzeinstellungen für Teams, Gruppen und Sites festgelegt, wofür diese Bezeichnung gilt. Wenn sie nicht aktiviert ist, wählen Sie unten auf der Seite die Option **Weiter** aus. 

1. Dieses nächste Fenster ist eine Previewfunktion zum automatischen Anwenden dieser Bezeichnung auf Azure-Datenbankspalten (wie etwa SQL, Synapse und mehr), die Typen vertraulicher Informationen enthalten, die von Ihnen ausgewählt werden.  Diese Funktionen sind nicht aktiviert. Wählen Sie unten auf der Seite die Option **Abbrechen** aus, um den Assistenten für die Bezeichnungskonfiguration zu schließen und um zur Seite „Information Protection“ zurückzukehren. 

1. Wählen Sie im oberen Bereich der Seite „Information Protection“ die Option **Bezeichnungsrichtlinien** aus.  Vertraulichkeitsbezeichnungen können aufgrund von Bezeichnungsrichtlinien veröffentlicht werden.  

1. Wählen Sie die Richtlinie **Vertraulich – Finanzen** aus.  Ein Fenster wird geöffnet, das Informationen über die Richtlinie bereitstellt.  Über diese Richtlinie werden Richtlinienbezeichnungen vom Typ „Vertraulich – Finanzen“ veröffentlicht und Daten geschützt, die Finanzdaten für Contoso enthalten.  Beachten Sie außerdem, wie diese Richtlinie für alle veröffentlicht wird.  

1. Wählen Sie oben im Fenster die **Richtlinie bearbeiten** aus.

1. Lesen Sie die Beschreibung unter „Zu veröffentlichende Vertraulichkeitsbezeichnungen auswählen“.  Beachten Sie die aufgelistete Bezeichnung.  Nehmen Sie keine Änderungen an den Einstellungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.

1. Lesen Sie die Beschreibung unter „Für Benutzer und Gruppen veröffentlichen“.  Beachten Sie, dass diese Bezeichnung für alle Benutzer verfügbar ist.  Nehmen Sie keine Änderungen an den Einstellungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.

1. Überprüfen Sie die Richtlinieneinstellungen.  Nehmen Sie keine Änderungen an den Einstellungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.
    1. Lesen Sie die Beschreibung unter „Standardbezeichnung auf Dokumente anwenden“.  Beachten Sie, dass es keine Standardbezeichnung gibt. Nehmen Sie keine Änderungen an den Einstellungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.
    1. Lesen Sie die Beschreibung unter „Standardbezeichnung auf E-Mails anwenden“.  Wählen Sie den Dropdownpfeil im Eingabefeld aus, um die verfügbaren Optionen anzuzeigen. Nehmen Sie keine Änderungen an den Einstellungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.
    1. Lesen Sie die Beschreibung unter „Standardbezeichnung auf Power BI-Inhalt anwenden“.  Beachten Sie, dass es keine Standardbezeichnung gibt. Nehmen Sie keine Änderungen an den Einstellungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.

1. Über die letzte Konfigurationsoption wird der Name Ihrer Richtlinie festgelegt.  Nehmen Sie keine Änderungen an den Einstellungen vor.  Wählen Sie unten auf der Seite die Option **Abbrechen** aus, um die Richtlinienkonfiguration zu schließen und um zur Seite „Information Protection“ zurückzukehren.

1. Wählen Sie auf der Seite „Information Protection“ die Option „Automatisches Bezeichnen“ aus.  Beachten Sie, dass dort keine automatische Bezeichnungsrichtlinie konfiguriert ist.  Nehmen Sie keine Änderungen an den Einstellungen vor.  Wenn Sie sich fragen, weshalb hier keine Richtlinie vorhanden ist, obwohl die Bezeichnungskonfiguration so festgelegt ist, dass die Bezeichnungen auf Dateien und E-Mails automatisch angewendet werden, wechseln Sie zurück zu den Schritten, in denen Sie die Bezeichnungskonfigurationseinstellungen durchgegangen sind. Überprüfen Sie die Beschreibung und Informationsfelder, die „Automatisches Anwenden von Bezeichnungen für Dateien und E-Mails“ zugeordnet sind.  Hinweis:  Auf der Registerkarte „Automatisches Bezeichnen“ für die Vertraulichkeitsbezeichnung wird  „Sie müssen eine automatische Bezeichnungsrichtlinie erstellen, um diese Bezeichnung automatisch auf bereits (in SharePoint und OneDrive) gespeicherte Dateien oder auf bereits durch Exchange verarbeitete E-Mails anzuwenden“ angezeigt.

1. Wählen Sie im linken Navigationsbereich die Option „Startseite“ aus, um zum Microsoft 365 Compliance Center zurückzukehren.

1. Lassen Sie diese Seite geöffnet, da Sie sie in der nächsten Aufgabe verwenden werden.


#### <a name="task-2--in-this-task-you-will-go-through-the-process-of-applying-a-label-from-the-perspective-of-the-user-in-this-case-the-user-is-the-admin-and-view-the-content-marking-that-is-generated-by-the-label"></a>Aufgabe 2:  In dieser Aufgabe durchlaufen Sie den Prozess der Anwendung einer Bezeichnung aus Perspektive des Benutzers (in diesem Fall ist der Benutzer der Administrator) und sehen die durch die Bezeichnung generierte Inhaltsmarkierung an.

1. Stellen Sie zunächst sicher, dass Office auf Ihrem virtuellen Labcomputer (VM) eingerichtet wurde.  Wählen Sie hierzu die Registerkarte **Microsoft 365 Admin Center** aus, die im Browser geöffnet ist.  Wenn Sie die Registerkarte zuvor geschlossen haben, öffnen Sie eine neue Browserregisterkarte, und geben Sie **admin.microsoft.com** ein.
    1. Wählen Sie im linken Navigationsbereich **Abrechnung** aus, um alle Optionen anzuzeigen. Wählen Sie dann **Ihre Produkte** aus.
    1. Wählen Sie auf der Seite „Ihre Produkte“ die Option **Microsoft 365 E5 Trial** aus.
    1. Wählen Sie auf der Seite „Microsoft 365 E5 Trial“ **Software herunterladen und installieren** aus, und befolgen Sie die Anweisungen auf der Seite.

1. Wählen Sie in der linken unteren Ecke des virtuellen Labcomputers das Windows-Symbol, **Word** und dann **Leeres Dokument** aus.  Dadurch wird ein neues Word-Dokument in der Desktopversion von Word geöffnet.

1. Wählen Sie auf der oberen Menüleiste **Sensitivität** aus. Wählen Sie im Dropdown den Eintrag **Vertraulich – Finanzen** aus.

1. Beachten Sie, dass das Dokument das Wasserzeichen enthält.  Das Wasserzeichen wird als kleiner, hellgrauer Text vertikal auf der Seite angezeigt. 

1. Speichern Sie die Word-Datei.

1. Schließen Sie die in Ihrem Browser geöffneten Microsoft Word-Registerkarten, um Word zu schließen.

#### <a name="task-3-optional-in-addition-to-content-marking-the-label-protection-setting-was-set-for-encryption-per-the-permissions-that-were-configured-with-this-label-members-of-the-finance-group-can-co-author-documents-with-this-label-applied-and-users-in-the-contoso-tenant-can-view--in-this-task-you-will-send-this-document-to-an-email-address-to-which-you-have-access-ie-a-personal-email-address-and-that-is-not-part-of-the-wwlxzzzzonmicrosoftcom-domain-and-see-what-happens-when-you-try-to-open-the-attachment"></a>Aufgabe 3 (optional): Zusätzlich zur Inhaltsmarkierung wurde die Bezeichnungsschutzeinstellung für die Verschlüsselung festgelegt. Entsprechend den für diese Bezeichnung konfigurierten Berechtigungen können Mitglieder der Finanzgruppe Dokumente, auf die diese Bezeichnung angewendet ist, gemeinsam erstellen, und Benutzer im Contoso-Mandanten können sie anzeigen.  In dieser Aufgabe senden Sie dieses Dokument an eine E-Mail-Adresse, auf die Sie zugreifen können (d. h. eine persönliche E-Mail-Adresse), die jedoch NICHT Bestandteil der Domäne „WWLxZZZZ.OnMicrosoft.com“ ist. Anschließend erfahren Sie, was passiert, wenn Sie versuchen, die Anlage zu öffnen.  

1. Wählen Sie auf der Startseite von Microsoft 365 Compliance Center das **App-Startfeld-Symbol** aus, das sich neben dem Text „Contoso Electronics“ befindet. **Klicken Sie mit der rechten Maustaste auf das Outlook-Symbol**, und wählen Sie **In neuer Registerkarte öffnen** aus.

1. Wählen Sie in der oberen linken Ecke des Bildschirms die Option **Neue Nachricht** aus.  Geben Sie eine E-Mail-Adresse ein, auf die Sie zugreifen können und die kein Bestandteil der Domäne „WWLxZZZZ.OnMicrosoft.com“ ist. Geben Sie dann **Test** in die Betreffzeile ein.

1. Wählen Sie **Anfügen** aus.

1. Wählen Sie **Cloudspeicherorte durchsuchen** aus.

1. Wählen Sie in der angezeigten Liste das von Ihnen erstellte Dokument aus, auf das Sie die Bezeichnung **Testbezeichnung** angewendet haben. Wählen Sie **Weiter** und dann **Als Kopie anfügen** aus.  Klicken Sie auf **Senden**.

1. Melden Sie sich im Webbrowser auf Ihrer Lab-VM mit dem E-Mail-Konto an, an das Sie das Dokument gesendet haben.  Beachten Sie, dass die E-Mail möglicherweise in Ihrem Junk-E-Mail-Ordner gelandet ist.  Wenn Sie versuchen, die angefügte Word-Datei zu öffnen, werden Sie benachrichtigt, dass Sie nicht berechtigt sind, das Dokument zu öffnen.

1. Schließen Sie die geöffneten Browserregisterkarten.


#### <a name="review"></a>Überprüfung
In diesem Lab erkunden Sie die Funktionen von Vertraulichkeitsbezeichnungen.  Sie gehen die Einstellungen für vorhandene, bereits erstellte Vertraulichkeitsbezeichnungen und für die entsprechende Richtlinie zum Veröffentlichen der Bezeichnung durch.   Anschließend erfahren Sie, wie eine Bezeichnung angewendet wird, und welche Auswirkung diese Bezeichnung aus Perspektive eines Benutzers hat.