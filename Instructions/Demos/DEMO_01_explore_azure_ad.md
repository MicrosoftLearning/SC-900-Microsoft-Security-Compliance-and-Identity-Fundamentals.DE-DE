---
Demo:
  title: Benutzereinstellungen von Azure Active Directory
  module: 'Module 2 Lesson 1: Describe the capabilities of Microsoft Identity and access management solutions: Explore the services and identity types of Azure AD'
ms.openlocfilehash: eb1ffc50ce90922dced58726c39879edfc74fb5b
ms.sourcegitcommit: 25998048c2e354ea23d6f497205e8a062d34ac80
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2022
ms.locfileid: "144557180"
---
# <a name="demo-azure-active-directory-user-settings"></a>Demo: Benutzereinstellungen von Azure Active Directory

## <a name="demo-scenario"></a>Demoszenario

In dieser Demo greifen Sie auf Azure Active Directory zu und gehen die verschiedenen Einstellungen für einen bestehenden Benutzer durch.

1. Navigieren Sie zu der in Ihrem Browser geöffneten Registerkarte **Startseite – Microsoft Azure**.  Wenn Sie die Registerkarte geschlossen haben, öffnen Sie Microsoft Edge, und geben Sie in die Adressleiste „portal.azure.com“ ein. Melden Sie sich mit den gleichen Anmeldeinformationen an, die Sie für Ihren Microsoft 365-Mandanten verwenden.

1. Auf der Landing Page des Azure-Portals werden Azure-Dienste angezeigt. Wählen Sie **Azure Active Directory** aus. Ist diese Option nicht unmittelbar sichtbar, geben Sie im Suchfeld neben „Microsoft Azure“ den Text „Azure Active Directory“ ein.  Außerdem sollten Sie zeigen, wie Sie Azure Active Directory über das Symbol zur Anzeige des Portalmenüs aufrufen (die drei horizontalen Linien in dem blauen Balken oben auf der Seite werden auch als Hamburgersymbol bezeichnet). Dieses befindet sich links neben dem Eintrag „Microsoft Azure“.

1. Wählen Sie im linken Navigationsbereich **Benutzer** aus. Beachten Sie, dass bereits Benutzer für Ihren Mandanten konfiguriert sind.

1. Wählen Sie aus der Liste der Benutzer **Adele Vance** aus.

1. Beachten Sie, dass im linken Navigationsbereich die Option **Profil** ausgewählt ist.  Zeigen Sie die Informationen auf der Profilseite bzw. erläutern Sie diese.

1. Wählen Sie im linken Navigationsbereich **Zugewiesene Rollen** aus.  Diesem Benutzer sind keine Administratorrollen zugewiesen.  Wählen Sie oben auf der Seite **+ Zuweisungen hinzufügen** aus, um zu sehen, welche Arten von Administratorrollen verfügbar sind.  Fügen Sie keine Zuweisungen hinzu. Schließen Sie die Seite einfach mit dem **X** rechts oben auf der Seite.

1. Wählen Sie im linken Navigationsbereich **Gruppen** aus.  Erwähnen Sie, dass dieser Benutzer ein Mitglied mehrerer Gruppen ist.  Hier können Sie die Arten von Gruppen erwähnen.  Um diesen Benutzer anderen Gruppen hinzuzufügen, würden Sie einfach **+ Mitgliedschaften hinzufügen** auswählen.  Fügen Sie keine neuen Gruppen hinzu. Erwähnen Sie nur, wie einfach es ist, einen Benutzer zu bestehenden Gruppen hinzuzufügen. Schließen Sie das Gruppenfenster mit dem **X** rechts oben auf der Seite.

1. Wählen Sie im linken Navigationsbereich **Lizenzen** aus. Beachten Sie, dass diesem Benutzer Microsoft 365 E5-Lizenzen und eine EMS-Lizenz zugewiesen sind.  Wählen Sie im oberen Bereich des Hauptfensters **+ Zuweisungen** aus, um eine Lizenz hinzuzufügen.  Zeigen Sie die Lizenzen für diesen Benutzer. Nehmen Sie KEINE Änderungen vor.  Schließen Sie dieses Fenster mit dem **X** oben rechts auf der Seite.

1. Wählen Sie im linken Navigationsbereich **Geräte** aus.  Es wird nichts angezeigt. Sie können aber erklären, dass hier Geräte angezeigt werden würden, wenn diesem Benutzer welche zugewiesen wären.

1. Wählen Sie im linken Navigationsbereich **Azure-Rollenzuweisungen** aus.  Erklären Sie Folgendes:
    1. Diese Registerkarte ist nicht identisch mit der für zugewiesene Rollen, die zuvor gezeigt wurde, da die zuvor gezeigte Registerkarte für die rollenbasierte Zugriffssteuerung in Azure Active Directory gedacht ist (betonen Sie Active Directory).
    1. Auf dieser Registerkarte können Sie Rollenzuweisungen anzeigen, die Benutzern für Azure-Ressourcen zugewiesen wurden. Wenn Sie z. B. eine Azure-Ressourcengruppe erstellen, weisen Sie Adele eine bestimmte Rollen zu, etwa die Rolle als Besitzerin oder Mitwirkende für die Ressourcengruppe. Diese Rolle würde hier aufgeführt werden. Dies ist Teil der rollenbasierten Zugriffssteuerung in Azure (Azure RBAC). Diese Rollenzuweisung wird im Rahmen dieser konkreten Ressource verwaltet.

1. Wählen Sie im linken Navigationsbereich **Authentifizierungsmethoden** aus.  Heben Sie die Beschreibung bevor: „Hier können Sie die Telefonnummern und E-Mail-Adressen angeben, die Benutzer für die mehrstufige Authentifizierung, die Self-Service-Kennwortzurücksetzung und zum Zurücksetzen des Kennworts eines Benutzers verwenden.“ Wenn für einen Benutzer SSPR konfiguriert ist oder dieser MFA verwenden muss und Sie als Administrator dieses Feld ausfüllen, ist der Benutzer bereits registriert und muss für SSPR oder MFA keine Registrierungsschritte mehr durchführen.  Normalerweise registrieren sich Benutzer selbst. Es kommt eher selten vor, dass der Administrator dies tun muss.

1. Wählen Sie im linken Navigationsbereich **Anmeldungen** aus.  Hier können Sie Anmeldeaktivitäten dieses Benutzers sehen.  Bei dieser Benutzerin wird möglicherweise nichts angezeigt, da sie sich noch nicht angemeldet hat.

1. Wählen Sie oben rechts auf der Seite das **X** aus. Daraufhin wird wieder die Benutzerliste angezeigt.  Bevor Sie die Benutzerliste schließen, können Sie hervorheben, dass oben auf der Seite MFA angezeigt wird.  Wählen Sie **Multi-Factor Authentication** aus.  Dadurch wird ein neues Browserfenster geöffnet.  Hier können Sie MFA für mehrere Benutzer auswählen.  Dies ist eine Möglichkeit, MFA für Benutzer zu aktivieren.  Im Zusammenhang mit dem bedingten Zugriff, der eine detailliertere Steuerung von MFA erlaubt, werden wir noch näher auf MFA eingehen.  Schließen Sie die Browserregisterkarte für die mehrstufige Authentifizierung.

1. Wählen Sie oben rechts auf der Seite das **X** aus. Daraufhin wird wieder die Hauptseite für den Contoso-Mandanten angezeigt.

### <a name="review"></a>Überprüfung

In dieser Demo sind Sie die Einstellungen eines bestehenden Benutzers durchgegangen. Dazu zählen Gruppen, denen der Benutzer zugewiesen werden kann, die Verfügbarkeit von Rollen und die Zuweisung von Benutzerlizenzen.
