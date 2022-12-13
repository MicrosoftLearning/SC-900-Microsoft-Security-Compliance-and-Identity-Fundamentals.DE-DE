<a name="---"></a><!---
---
Demo: Title: 'Erkunden von Azure AD-Benutzereinstellungen' Learning Path/Module/Unit: 'Lernpfad: Beschreiben der Funktionen von Azure Active Directory (Azure AD), Teil von Microsoft Entra; Module 1: Beschreiben der grundlegenden Dienste und Identitätstypen von Azure AD; Lerneinheit 4: Beschreiben der Identitätstypen in Azure AD'
---
--->

# <a name="demo-azure-ad-user-settings"></a>Demo: Azure AD-Benutzereinstellungen

Diese Demo ist den folgenden Learn-Inhalten zugeordnet:

- Lernpfad: Beschreiben der Funktionen von Azure Active Directory (Azure AD), Teil von Microsoft Entra
- Modul: Beschreiben der grundlegenden Dienste und Identitätstypen von Azure AD
- Lerneinheit: Beschreiben der Identitätstypen in Azure AD

## <a name="demo-scenario"></a>Demoszenario

In dieser Demo greifen Sie auf Azure Active Directory zu und gehen die verschiedenen Einstellungen für einen vorhandenen Benutzer durch.  Hinweis an den Referenten:  In dieser Demo wird über den Microsoft 365-Mandanten auf Azure AD zugegriffen. Alternativ können Sie Kursteilnehmern zeigen, wie über das Azure-Portal auf Azure AD zugegriffen werden kann. Die Absicht dahinter ist, dass gezeigt werden soll, dass Microsoft 365 über das Microsoft 365-Portal auch Zugriff auf Azure AD bietet.

1. Öffnen Sie Microsoft Edge.

1. Geben Sie **admin.microsoft.com** in die Adressleiste ein, um auf Microsoft 365 Admin Center zuzugreifen.

1. Melden Sie sich mit Ihren Administratoranmeldeinformationen an.
    1. Geben Sie **admin@WWLxZZZZZZ.onmicrosoft.com** (ZZZZZZ ist hierbei die eindeutige Mandanten-ID, die von Ihrem Lab-Hostinganbieter bereitgestellt wurde) in das Anmeldefenster ein, und wählen Sie dann **Weiter** aus.
    1. Geben Sie das Administratorkennwort ein, das von Ihrem Lab-Hostinganbieter bereitgestellt werden sollte. Wählen Sie **Anmelden**.
    1. Wählen Sie **Ja** aus, wenn Sie gefragt werden, ob Sie angemeldet bleiben möchten.

1. Wählen Sie im linken Navigationsbereich von Microsoft 365 Admin Center **Alle anzeigen** aus.

1. Wählen Sie unter „Admin Center“ den Eintrag **Azure Active Directory** aus (möglicherweise müssen Sie dazu nach unten scrollen).  Die Seite „Mein Dashboard“ des Azure Active Directory Admin Center wird auf einer neuen Browserseite geöffnet. In den Hauptfenstern des Dashboards werden verschiedene Kacheln angezeigt, darunter die Kachel „Organisationsidentität“ (Contoso, der Mandant und die Azure AD-Edition), eine Kachel für Benutzer und Gruppen und mehr.

1. Wählen Sie im linken Navigationsbereich **Benutzer** aus. Beachten Sie, dass bereits Benutzer für Ihren Mandanten konfiguriert sind.

1. Wählen Sie aus der Liste der Benutzer **Adele Vance** aus.

1. Beachten Sie, dass im linken Navigationsbereich die Option **Profil** ausgewählt ist.  Zeigen Sie die Informationen auf der Profilseite bzw. erläutern Sie diese.

1. Wählen Sie im linken Navigationsbereich **Zugewiesene Rollen** aus.  Diesem Benutzer sind keine Administratorrollen zugewiesen.  Wählen Sie oben auf der Seite **+ Zuweisungen hinzufügen** aus, um zu sehen, welche Arten von Administratorrollen verfügbar sind.  Fügen Sie keine Zuweisungen hinzu. Schließen Sie die Seite einfach mit dem **X** rechts oben auf der Seite.

1. Wählen Sie im linken Navigationsbereich **Gruppen** aus.  Erwähnen Sie, dass dieser Benutzer ein Mitglied mehrerer Gruppen ist.  Hier können Sie die Arten von Gruppen erwähnen.  Um diesen Benutzer anderen Gruppen hinzuzufügen, würden Sie **+ Mitgliedschaften hinzufügen** auswählen.  Fügen Sie keine neuen Gruppen hinzu. Erwähnen Sie nur, wie einfach es ist, einen Benutzer vorhandenen Gruppen hinzuzufügen. Schließen Sie das Gruppenfenster mit dem **X** rechts oben auf der Seite.

1. Wählen Sie im linken Navigationsbereich **Lizenzen** aus. Beachten Sie, dass diesem Benutzer Microsoft 365 E5-Lizenzen und eine EMS-Lizenz zugewiesen sind.  Wählen Sie im oberen Bereich des Hauptfensters **+ Zuweisungen** aus, um eine Lizenz hinzuzufügen.  Zeigen Sie die Lizenzen für diesen Benutzer. Nehmen Sie KEINE Änderungen vor.  Schließen Sie dieses Fenster mit dem **X** oben rechts auf der Seite.

1. Wählen Sie im linken Navigationsbereich **Geräte** aus.  Es wird nichts angezeigt. Sie können aber erklären, dass hier Geräte angezeigt werden würden, wenn diesem Benutzer welche zugewiesen wären.

1. Wählen Sie im linken Navigationsbereich **Azure-Rollenzuweisungen** aus.  Erklären Sie Folgendes:
    1. Diese Registerkarte ist nicht identisch mit der für zugewiesene Rollen, die zuvor gezeigt wurde, da die zuvor gezeigte Registerkarte für die rollenbasierte Zugriffssteuerung in Azure Active Directory gedacht ist (betonen Sie Active Directory).
    1. Auf dieser Registerkarte können Sie Rollenzuweisungen anzeigen, die Benutzern für Azure-Ressourcen zugewiesen wurden. Wenn Sie z. B. eine Azure-Ressourcengruppe erstellen, weisen Sie Adele eine bestimmte Rollen zu, etwa die Rolle als Besitzerin oder Mitwirkende für die Ressourcengruppe. Diese Rolle würde hier aufgeführt werden. Dies ist Teil der rollenbasierten Zugriffssteuerung in Azure (Azure RBAC). Diese Rollenzuweisung wird im Rahmen dieser konkreten Ressource verwaltet.

1. Wählen Sie im linken Navigationsbereich **Authentifizierungsmethoden** aus.  Heben Sie die Beschreibung bevor: „Hier können Sie die Telefonnummern und E-Mail-Adressen angeben, die Benutzer für die mehrstufige Authentifizierung, die Self-Service-Kennwortzurücksetzung und zum Zurücksetzen des Kennworts eines Benutzers verwenden.“ Wenn für einen Benutzer SSPR konfiguriert ist oder dieser MFA verwenden muss und Sie als Administrator dieses Feld ausfüllen, ist der Benutzer bereits registriert und muss für SSPR oder MFA keine Registrierungsschritte mehr durchführen.  Normalerweise registrieren sich Benutzer selbst. Es kommt eher selten vor, dass der Administrator dies ausführen muss.

1. Wählen Sie im linken Navigationsbereich **Anmeldungen** aus.  Hier können Sie Anmeldeaktivitäten dieses Benutzers sehen.  Bei dieser Benutzerin wird möglicherweise nichts angezeigt, da sie sich noch nicht angemeldet hat.

1. Wählen Sie oben rechts auf der Seite das **X** aus. Daraufhin wird wieder die Benutzerliste angezeigt.  Bevor Sie die Benutzerliste schließen, können Sie hervorheben, dass oben auf der Seite MFA angezeigt wird.  Wählen Sie **Multi-Factor Authentication** aus.  Dadurch wird ein neues Browserfenster geöffnet.  Hier können Sie MFA für mehrere Benutzer auswählen.  Dies ist eine Möglichkeit, MFA für Benutzer zu aktivieren.  Wir werden näher auf MFA im Kontext von bedingtem Zugriff eingehen und aufzeigen, wie eine präzisere Steuerung von MFA möglich ist.  Schließen Sie die Browserregisterkarte für die mehrstufige Authentifizierung.

1. Wählen Sie oben rechts auf der Seite das **X** aus. Daraufhin wird wieder die Hauptseite für den Contoso-Mandanten angezeigt.

### <a name="review"></a>Überprüfung

In dieser Demo haben Sie die Einstellungen eines vorhandenen Benutzers gezeigt. Dazu zählen Gruppen, denen der Benutzer zugewiesen werden kann, die Verfügbarkeit von Rollen und die Zuweisung von Benutzerlizenzen.
