---
Demo:
  title: Vertraulichkeitsbezeichnungen in Microsoft Purview
  module: 'Module 4 Lesson 3: Describe the capabilities of Microsoft compliance solutions: Describe information protection and data lifecycle management of Microsoft Purview'
ms.openlocfilehash: 9dbcb385f5f4545942ecd38fe5fc0ad17e2934a3
ms.sourcegitcommit: a69acc26ed3a09cea4a3af95719a6edc7fe2814d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/29/2022
ms.locfileid: "146649956"
---
# <a name="demo-sensitivity-labels-in-microsoft-purview"></a>Demo: Vertraulichkeitsbezeichnungen in Microsoft Purview

## <a name="demo-scenario"></a>Demoszenario

In dieser Demo zeigen Sie die Funktionen der Vertraulichkeitsbezeichnungen.  Sie gehen die Einstellungen für vorhandene, bereits erstellte Vertraulichkeitsbezeichnungen und für die entsprechende Richtlinie zum Veröffentlichen der Bezeichnung durch.   Anschließend erfahren Sie, wie eine Bezeichnung angewendet wird, und welche Auswirkung diese Bezeichnung aus Perspektive eines Benutzers hat.  **HINWEIS:** Wenn Sie Word zum ersten Mal online mit Ihrem Microsoft 365-Mandanten verwenden, kann es bis zu 15 Minuten dauern, bis die Option „Vertraulichkeit“ im Menüband angezeigt wird.  Referent*innen sollten den Demoteil 2 noch vor Kursbeginn ausführen, damit noch genügend Zeit bleibt, bis die Option angezeigt wird.

### <a name="demo-part-1"></a>Teil 1 der Demo

In dieser Demo zeigen Sie die Einstellungen für eine vorhandene Vertraulichkeitsbezeichnung und die entsprechende Richtlinie zum Veröffentlichen der Bezeichnung.

1. Öffnen Sie Microsoft Edge. Geben Sie **admin.microsoft.com** in die Adressleiste ein.

1. Melden Sie sich mit Ihren Administratoranmeldeinformationen an.
    1. Geben Sie **admin@WWLxZZZZZZ.onmicrosoft.com** (ZZZZZZ ist hierbei die eindeutige Mandanten-ID, die von Ihrem Labhostinganbieter bereitgestellt wurde) in das Fenster „Anmelden“ ein, und wählen Sie dann **Weiter** aus.
    1. Geben Sie das Administratorkennwort ein, das Sie vom Labhostinganbieter erhalten haben sollten. Wählen Sie **Anmelden**.
    1. Wählen Sie **Ja** aus, wenn Sie gefragt werden, ob Sie angemeldet bleiben möchten. Dadurch gelangen Sie zur Seite „Microsoft 365 Admin Center“.

1. Wählen Sie im linken Navigationsbereich von Microsoft 365 Admin Center **Alle anzeigen** aus.

1. Wählen Sie unter „Admin Center“ die Option **Compliance** aus.  Die Startseite des Microsoft Purview-Complianceportals wird auf einer neuen Browserseite geöffnet.  

1. Wählen Sie im linken Navigationsbereich des Microsoft Purview-Complianceportals **Alle anzeigen** aus.

1. Wählen Sie im linken Navigationsbereich **Information Protection** unter „Lösungen“ aus.

1. Im gelben Informationsfeld werden Sie darauf hingewiesen, dass Ihre Organisation die Option zum Verarbeiten von Inhalten in Office-Onlinedateien, für die verschlüsselte Vertraulichkeitsbezeichnungen verwendet wurden und die in OneDrive oder SharePoint gespeichert sind, nicht aktiviert hat.  Wählen Sie **Jetzt aktivieren** aus.  Nachdem Sie diese Aktion vorgenommen haben, kann es eine Verzögerung geben, bis die Einstellung vom System übernommen wurde.

1. Überprüfen Sie, ob die oben auf der Seite befindliche Registerkarte **Bezeichnungen** ausgewählt (unterstrichen) ist.

1. Beachten Sie auf der Seitenmitte die drei bereits erstellten Bezeichnungen.  Wählen Sie **Vertraulich – Finanzen** aus.  Ein Fenster wird geöffnet, das Informationen über diese Bezeichnung bereitstellt.  Beachten Sie, wie diese Bezeichnung festgelegt ist, um die Verschlüsselung und Inhaltsmarkierung zu unterstützen.  Wählen Sie oben auf der Seite **Bezeichnung bearbeiten** aus, um einige der grundlegenden Konfigurationseinstellungen anzuzeigen.

    1. Bei der Konfiguration werden zunächst ein Name und eine Beschreibung für Ihre Bezeichnung angegeben.  Nehmen Sie keine Änderungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.

    1. Beachten Sie den Bereich für diese Bezeichnung.  Der Bereich ist auf Dateien und E-Mails festgelegt, wofür Sie die Verschlüsselungs- und Inhaltsmarkierungseinstellungen konfigurieren können, um mit einer Bezeichnung versehene E-Mails und Office-Dateien zu schützen.  Nehmen Sie keine Änderungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.

    1. Für den ausgewählten Bereich für Dateien und E-Mails können Sie den Inhalt so konfigurieren, dass er verschlüsselt bzw. markiert wird.  Beachten Sie, wie die Schutzeinstellungen für Dateien und E-Mails für die Verschlüsselung und Markierung des Inhalts der Dateien festgelegt sind.  Überprüfen Sie die jeweilige Definition.  Nehmen Sie keine Änderungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.

    1. Im Fenster „Verschlüsselung“ wird die Konfiguration für die Verschlüsselungseinstellungen angezeigt.  Nehmen Sie keine Änderungen vor.  Überprüfen Sie das Informationsfeld unter „Verschlüsselungseinstellungen konfigurieren“, und überprüfen Sie die konfigurierten Einstellungen. Beachten Sie, dass der Benutzerzugriff auf den Inhalt auf „Läuft nie ab“ festgelegt ist.  Sie können auch bestimmten Benutzern und Gruppen Berechtigungen zuweisen, damit nur diese mit Inhalt interagieren können, auf den diese Bezeichnung angewendet ist.  Der Mandant wird unter „Benutzer und Gruppen“ definiert. Entsprechend können alle Benutzer in Ihrem Mandanten Inhalt mit dieser Bezeichnung anzeigen.  Die Finanzabteilung ist ebenfalls aufgelistet und verfügt über Mitautorberechtigungen.  Nehmen Sie keine Änderungen an den Einstellungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.

    1. Beachten Sie auf der Seite „Inhaltsmarkierung“ das oben auf der Seite befindliche Informationsfeld.  Inhaltsmarkierungen werden auf Dokumente angewendet. Es werden aber nur Kopf- und Fußzeilen auf E-Mail-Nachrichten angewendet. Wasserzeichen werden entsprechend nicht auf E-Mails angewendet.  Die dieser Bezeichnung zugeordnete Inhaltsmarkierung ist ein Wasserzeichen.  Nehmen Sie keine Änderungen an den Einstellungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.

    1. Sie befinden sich nun im Fenster „Automatisches Anwenden von Bezeichnungen für Dateien und E-Mails“.  Lesen Sie oben auf der Seite die Beschreibung zum Anwenden der automatischen Bezeichnung und das darunter befindliche Informationsfeld.  Beachten Sie außerdem, dass diese Bezeichnung für das automatische Anwenden von Bezeichnungen für bestimmte Bedingungen festgelegt ist. Nehmen Sie keine Änderungen an den Einstellungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.

    1. In diesem nächsten Fenster werden Schutzeinstellungen für Teams, Gruppen und Sites festgelegt, wofür diese Bezeichnung gilt. Wenn sie nicht aktiviert ist, wählen Sie unten auf der Seite die Option **Weiter** aus.

    1. Dieses nächste Fenster ist eine Previewfunktion zum automatischen Anwenden dieser Bezeichnung auf Azure-Datenbankspalten (wie etwa SQL, Synapse und mehr), die Typen vertraulicher Informationen enthalten, die von Ihnen ausgewählt werden.  Diese Funktionen sind nicht aktiviert. Wählen Sie unten auf der Seite die Option **Abbrechen** aus, um den Assistenten für die Bezeichnungskonfiguration zu schließen und um zur Seite „Information Protection“ zurückzukehren.

1. Wählen Sie im oberen Bereich der Seite „Information Protection“ die Option **Bezeichnungsrichtlinien** aus.  Vertraulichkeitsbezeichnungen können aufgrund von Bezeichnungsrichtlinien veröffentlicht werden.  

1. Wählen Sie die Richtlinie **Vertraulich – Finanzen** aus.  Ein Fenster wird geöffnet, das Informationen über die Richtlinie bereitstellt.  Über diese Richtlinie werden Richtlinienbezeichnungen vom Typ „Vertraulich – Finanzen“ veröffentlicht und Daten geschützt, die Finanzdaten für Contoso enthalten.  Beachten Sie außerdem, wie diese Richtlinie für alle veröffentlicht wird.  

1. Wählen Sie oben im Fenster die **Richtlinie bearbeiten** aus.

    1. Lesen Sie die Beschreibung unter „Zu veröffentlichende Vertraulichkeitsbezeichnungen auswählen“.  Beachten Sie die aufgelistete Bezeichnung.  Nehmen Sie keine Änderungen an den Einstellungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.

    1. Lesen Sie die Beschreibung unter „Für Benutzer und Gruppen veröffentlichen“.  Beachten Sie, dass diese Bezeichnung für alle Benutzer verfügbar ist.  Nehmen Sie keine Änderungen an den Einstellungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.

    1. Überprüfen Sie die Richtlinieneinstellungen.  Nehmen Sie keine Änderungen an den Einstellungen vor.  Wählen Sie unten auf der Seite die Option **Weiter** aus.

    1. Über die letzte Konfigurationsoption wird der Name Ihrer Richtlinie festgelegt.  Nehmen Sie keine Änderungen an den Einstellungen vor.  Wählen Sie unten auf der Seite die Option **Abbrechen** aus, um die Richtlinienkonfiguration zu schließen und um zur Seite „Information Protection“ zurückzukehren.

1. Wählen Sie auf der Seite „Information Protection“ die Option „Automatisches Bezeichnen“ aus.  Beachten Sie, dass dort keine automatische Bezeichnungsrichtlinie konfiguriert ist.  Nehmen Sie keine Änderungen an den Einstellungen vor.  Wenn Sie sich fragen, weshalb hier keine Richtlinie vorhanden ist, obwohl die Bezeichnungskonfiguration so festgelegt ist, dass die Bezeichnungen auf Dateien und E-Mails automatisch angewendet werden, wechseln Sie zurück zu den Schritten, in denen Sie die Bezeichnungskonfigurationseinstellungen durchgegangen sind. Überprüfen Sie die Beschreibung und Informationsfelder, die „Automatisches Anwenden von Bezeichnungen für Dateien und E-Mails“ zugeordnet sind.  Hinweis:  Auf der Registerkarte „Automatisches Bezeichnen“ für die Vertraulichkeitsbezeichnung wird  „Sie müssen eine automatische Bezeichnungsrichtlinie erstellen, um diese Bezeichnung automatisch auf bereits (in SharePoint und OneDrive) gespeicherte Dateien oder auf bereits durch Exchange verarbeitete E-Mails anzuwenden“ angezeigt.

1. Wählen Sie im linken Navigationsbereich die Startseite aus, um zur Startseite des Microsoft Purview-Complianceportals zurückzukehren.

1. Lassen Sie diese Seite geöffnet, da Sie sie in der nächsten Aufgabe verwenden werden.

### <a name="demo-part-2"></a>Teil 2 der Demo

In diesem Schritt zeigen Sie den Prozess der Anwendung einer Bezeichnung aus Perspektive des Benutzers (in diesem Fall ist der Benutzer der Administrator) und sehen die durch die Bezeichnung generierte Inhaltsmarkierung an.

1. Wählen Sie auf der Startseite des Microsoft Purview-Complianceportals das **App-Startfeld-Symbol** aus, das sich neben dem Text „Contoso Electronics“ befindet. **Klicken Sie mit der rechten Maustaste auf das Word-Symbol**, und wählen Sie **In neuer Registerkarte öffnen** aus.  

1. Wählen Sie **+ Neues leeres Dokument** aus. Geben Sie dann etwas Text auf der Seite ein.  Wählen Sie oben auf der Seite auf dem blauen Balken den Pfeil nach unten aus, der sich neben „DokumentXX – gespeichert“ befindet, und geben Sie in das Feld „Dateiname“ den Text **Testbezeichnung** ein.

1. Wählen Sie auf der oberen Menüleiste die Option **Vertraulichkeit** aus. Wenn diese Option nicht sofort angezeigt wird, aktualisieren Sie die Seite. Wählen Sie im Dropdown den Eintrag **Vertraulich – Finanzen** aus.

1. Wählen Sie auf der oberen Menüleiste die Option **Ansicht** und dann die Ansicht **Lesebereich** aus.

1. Beachten Sie, dass das Dokument das Wasserzeichen enthält.  

1. Schließen Sie die in Ihrem Browser geöffneten Microsoft Word-Registerkarten, um Word zu schließen.

### <a name="demo-part-3-optional"></a>Teil 3 der Demo (optional)

Zusätzlich zur Inhaltsmarkierung wurde die Bezeichnungsschutzeinstellung für die Verschlüsselung festgelegt. Entsprechend den für diese Bezeichnung konfigurierten Berechtigungen können Mitglieder der Finanzgruppe Dokumente, auf die diese Bezeichnung angewendet ist, gemeinsam erstellen, und Benutzer im Contoso-Mandanten können sie (oder Dokumente/E-Mails, auf welche die Bezeichnung angewendet ist) anzeigen.  In diesem Abschnitt senden Sie dieses Dokument an eine E-Mail-Adresse, auf die Sie zugreifen können (d. h. eine persönliche E-Mail-Adresse oder Ihre Microsoft-E-Mail-Adresse), die jedoch NICHT Bestandteil der Domäne „WWLxZZZZ.OnMicrosoft.com“ ist. Anschließend erfahren Sie, was passiert, wenn Sie versuchen, die Anlage zu öffnen.  

1. Wählen Sie auf der Startseite des Microsoft Purview-Complianceportals das **App-Startfeld-Symbol** aus, das sich neben dem Text „Contoso Electronics“ befindet. **Klicken Sie mit der rechten Maustaste auf das Outlook-Symbol**, und wählen Sie **In neuer Registerkarte öffnen** aus.

1. Wählen Sie in der oberen linken Ecke des Bildschirms die Option **Neue Nachricht** aus.  Geben Sie eine E-Mail-Adresse ein, auf die Sie zugreifen können und die kein Bestandteil der Domäne „WWLxZZZZ.OnMicrosoft.com“ ist. Geben Sie dann **Test** in die Betreffzeile ein.

1. Wählen Sie **Anfügen** aus.

1. Wählen Sie **Cloudspeicherorte durchsuchen** aus.

1. Wählen Sie in der angezeigten Liste das von Ihnen erstellte Dokument aus, auf das Sie die Bezeichnung **Testbezeichnung** angewendet haben. Wählen Sie **Weiter** und dann **Als Kopie anfügen** aus.  Klicken Sie auf **Senden**.

1. Überprüfen Sie das E-Mail-Konto, an das Sie das Dokument gesendet haben.  Beachten Sie, dass die E-Mail möglicherweise in Ihrem Junk-E-Mail-Ordner gelandet ist.  Wenn Sie versuchen, die angefügte Word-Datei zu öffnen, werden Sie benachrichtigt, dass Sie nicht berechtigt sind, das Dokument zu öffnen.

1. Schließen Sie die geöffneten Browserregisterkarten.

### <a name="review"></a>Überprüfung

In dieser Demo haben Sie Vertraulichkeitsbezeichnungen gezeigt.  Sie haben die Einstellungen für vorhandene, bereits erstellte Vertraulichkeitsbezeichnungen und die entsprechende Richtlinie zum Veröffentlichen der Bezeichnung gezeigt. Anschließend haben Sie gezeigt, wie eine Bezeichnung angewendet wird und welche Auswirkung diese Bezeichnung aus Perspektive eines Benutzers hat.
