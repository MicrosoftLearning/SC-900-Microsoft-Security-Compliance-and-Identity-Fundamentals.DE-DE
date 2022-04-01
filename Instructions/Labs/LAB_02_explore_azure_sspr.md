---
lab:
  title: Erkunden der Azure AD-Authentifizierung mit Self-Service-Kennwortzurücksetzung
  module: 'Module 2 Lesson 2: Describe the capabilities of Microsoft Identity and access management solutions: Describe the different authentication methods of Azure AD'
ms.openlocfilehash: 7a9ae15dda8636c3323afacc0f92fc630485cc64
ms.sourcegitcommit: a341c2fc38e9b37dafb792d82e3c948f7ba4a099
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/14/2022
ms.locfileid: "137894015"
---
# <a name="lab-explore-azure-ad-authentication-with-self-service-password-reset"></a>Lab: Erkunden der Azure AD-Authentifizierung mit Self-Service-Kennwortzurücksetzung

## <a name="lab-scenario"></a>Labszenario

In diesem Lab gehen Sie als Administrator den Prozess der Aktivierung der Self-Service-Kennwortzurücksetzung durch. Bei aktivierter SSPR übernehmen Sie anschließend die Rolle eines Benutzers und gehen den Prozess der Registrierung für die SSPR und auch zur Zurücksetzung Ihres Kennworts durch.  Schließlich können Sie als Administrator Überwachungsprotokolle sowie Nutzungsdaten und Erkenntnisse für die SSPR anzeigen.

**Geschätzte Dauer**: 15 bis 20 Minuten


#### <a name="task-1--in-this-task-you-as-the-admin-will-add-an-existing-user-adele-vance-into-the-ssprsecurityusers-group--also-you-will-also-need-to-do-a-reset-of-the-users-password-so-that-you-can-do-a-first-time-login-as-the-user-and-register-for-sspr"></a>Aufgabe 1:  Bei dieser Aufgabe fügen Sie als Administrator der Gruppe „SSPRSecurityUsers“ den vorhandenen Benutzer Adele Vance hinzu.  Zudem müssen Sie das Kennwort des Benutzers zurücksetzen, damit Sie eine Erstanmeldung als der Benutzer vornehmen und sich für die SSPR registrieren können.

1. Öffnen Sie Microsoft Edge.

2. Geben Sie **portal.azure.com** in die Adressleiste ein, und melden Sie sich mit Ihren Administratoranmeldeinformationen an.
    1. Geben Sie **admin@WWLxZZZZZZ.onmicrosoft.com** (ZZZZZZ ist hierbei die eindeutige Mandanten-ID, die von Ihrem Labhostinganbieter bereitgestellt wurde) in das Fenster „Anmelden“ ein, und wählen Sie dann **Weiter** aus.
    1. Geben Sie das Administratorkennwort ein, das Sie vom Labhostinganbieter erhalten haben sollten. Wählen Sie **Anmelden**.
    1. Wählen Sie **Ja** aus, wenn Sie gefragt werden, ob Sie angemeldet bleiben möchten.

3. Wählen Sie **Azure Active Directory** aus.  

4. Wählen Sie im linken Navigationsbereich **Gruppen** aus.

5. Eine Liste der vorhandenen Gruppen wird angezeigt. Geben Sie in das Feld „Gruppen durchsuchen“ den Text **SSPR** ein. Wählen Sie dann **SSPRSecurityGroupUsers** aus den Suchergebnissen aus.  Dadurch gelangen Sie zur Konfigurationsoption für diese Gruppe.

6. Wählen Sie im linken Navigationsbereich **Mitglieder** aus.

7. Wählen Sie oben auf der Seite **+ Mitglieder hinzufügen** aus.  

8. Geben Sie **Adele** in das Suchfeld ein.  Sobald der Benutzer **Adele Vance** unterhalb des Suchfelds angezeigt wird, wählen Sie ihn aus, indem Sie unten auf der Seite auf **Auswählen** klicken.

9. Schließen Sie das Fenster „SSPRSecurityUsers“. Wählen Sie dazu in der oberen rechten Ecke des Bildschirms das **X** aus.

10. Kehren Sie zur Active Directory-Seite zurück. Wählen Sie dazu in der oberen linken Ecke des Bildschirms oberhalb von „Gruppen“ den Eintrag **Contoso** aus, um zur Seite mit dem Azure Active Directory von Contoso zurückzukehren.

11. Wählen Sie im linken Navigationsbereich **Benutzer** aus.

12. Wählen Sie **Adele Vance** aus der Liste der Benutzer aus.

13. Wählen Sie oben auf der Seite **Kennwort zurücksetzen** aus. Da Sie sich nicht zuvor als Adele Vance angemeldet haben, müssen Sie das Kennwort zurücksetzen.

14. Wenn das Kennwortzurücksetzungsfenster geöffnet wird, wählen Sie **Kennwort zurücksetzen** aus.  WICHTIG: Notieren Sie das neue Kennwort. Sie benötigen es in einer nachfolgenden Aufgabe, um sich als der Benutzer anmelden zu können.

15. Schließen Sie das Kennwortzurücksetzungsfenster. Wählen Sie dazu in der oberen rechten Ecke der Seite das **X** aus.

16. Schließen Sie das Fenster „Adele Vance“. Wählen Sie dazu in der oberen rechten Ecke der Seite das **X** aus.

17. Schließen Sie das Fenster „Benutzer“. Wählen Sie dazu in der oberen rechten Ecke der Seite das **X** aus.

18. Lassen Sie das Fenster „Contoso-Übersicht“ geöffnet, da Sie es in der nachfolgenden Aufgabe verwenden werden.

#### <a name="task-2-in-this-task-you-as-the-admin-will-learn-how-to-configure-password-reset-for-users-including-configuration-of-the-types-of-authentication-methods-to-use"></a>Aufgabe 2: Bei dieser Aufgabe erfahren Sie als Administrator, wie die Kennwortzurücksetzung für Benutzer konfiguriert wird, einschließlich der Konfiguration der zu verwendenden Authentifizierungsmethodentypen.

1. Navigieren Sie zu der in Ihrem Browser geöffneten Registerkarte „Contoso – Microsoft Azure“. Falls Sie die Registerkarte geschlossen haben, öffnen Sie eine Browserseite. Geben Sie „portal.azure.com“ in die Adressleiste ein, und wählen Sie „Azure Active Directory“ aus.  Sie sollten beim Azure-Portal als Administrator angemeldet sein. Falls nicht, melden Sie sich wieder an.

2. Wählen Sie im linken Navigationsbereich **Kennwort zurücksetzen** aus.  

3. Die Eigenschaften für die Self-Service-Kennwortzurücksetzung werden angezeigt.  Stellen Sie sicher, dass **Self-Service-Kennwortzurücksetzung** für die Gruppe **ausgewählt** ist, wofür sie aufgelistet ist, nämlich **SSPRSecurityUsers**.  Bewegen Sie den Mauszeiger über das Informationssymbol neben dem Text „Gruppe auswählen“, und beachten Sie die angezeigte Meldung „Definiert die Gruppe von Benutzern, die ihre eigenen Kennwörter zurücksetzen können“. Sie müssen Benutzer in die Gruppe aufnehmen. Es ist nicht möglich, Benutzer einzeln auszuwählen.  Wenn Sie die Gruppe ändern, ersetzt die von Ihnen ausgewählte Gruppe zudem die derzeit aufgelistete Gruppe.  Sie sollten der SSPR-Gruppe Benutzer einfach hinzufügen.  Beachten Sie als Letztes das blaue Informationsfeld: „Diese Einstellungen gelten nur für Endbenutzer in Ihrer Organisation. Administratoren können die Self-Service-Kennwortzurücksetzung immer durchführen und müssen zum Zurücksetzen ihres Kennworts zwei Authentifizierungsmethoden verwenden.“

5. Wählen Sie im linken Navigationsbereich von „Kennwort zurücksetzen“ die Option **Authentifizierungsmethoden** aus.

6. Wählen Sie **1** in „Anzahl von Methoden, die zurückgesetzt werden müssen“ aus. Beachten Sie das Informationsfeld auf dem Bildschirm.

7. Beachten Sie die unterschiedlichen Methoden, die für Benutzer verfügbar sind.  **E-Mail** und **Mobiltelefon (nur SMS)** sollten bereits aktiviert sein. Falls nicht, aktivieren Sie sie.

8. Wählen Sie im linken Navigationsbereich von „Kennwort zurücksetzen“ die Option **Registrierung** aus.  

9. Stellen Sie sicher, dass die Einstellung „Registrierung von Benutzern bei der Anmeldung verlangen?“ auf **Ja** festgelegt ist.  Übernehmen Sie für die Einstellung „Anzahl der Tage, bevor Benutzer aufgefordert werden, ihre Authentifizierungsinformationen erneut zu bestätigen“ die Standardeinstellung von 180.   Beachten Sie das Informationsfeld auf der Seite.

10. Wählen Sie im linken Navigationsbereich von „Kennwort zurücksetzen“ die Option **Benachrichtigungen** aus.  

11. Stellen Sie sicher, dass die Einstellung „Benutzer über Kennwortzurücksetzungen benachrichtigen“ auf **Ja** festgelegt ist.  Übernehmen Sie „Nein“ für die Einstellung „Alle Administratoren benachrichtigen, wenn andere Administratoren ihr Kennwort zurücksetzen“.

12. Beachten Sie, dass der Navigationsbereich „Kennwort zurücksetzen“ auch Optionen zum Anzeigen der Überwachungsprotokolle und von „Nutzung & Erkenntnisse“ umfasst.

13. **Melden Sie sich von allen Browserregisterkarten ab**. Klicken Sie dazu auf das Benutzersymbol neben der E-Mail-Adresse in der oberen rechten Ecke des Bildschirms. Schließen Sie dann alle Browserfenster.


#### <a name="task-3--in-this-task-you-as-user-adele-vance-will-go-through-the-registration-process-for-self-service-password-reset--this-task-requires-that-you-have-access-to-a-mobile-device-where-you-can-receive-text-messages-or-a-personal-email-account-that-you-can-access"></a>Aufgabe 3:  Bei dieser Aufgabe durchlaufen Sie als der Benutzer Adele Vance den Registrierungsprozess für die Self-Service-Kennwortzurücksetzung.  Für diese Aufgabe müssen Sie über Zugriff auf ein Mobilgerät, auf dem Sie SMS empfangen können, oder über ein persönliches E-Mail-Konto verfügen, auf das Sie zugreifen können.
 
1. Öffnen Sie Microsoft Edge.

2. Geben Sie **login.microsoftonline.com** in die Adressleiste ein.

3. Melden Sie sich als Adele Vance an.
    1. Geben Sie **AdedleV@WWLxZZZZZZ.onmicrosoft.com** (ZZZZZZ ist hierbei die eindeutige Mandanten-ID, die von Ihrem Labhostinganbieter bereitgestellt wurde) in das Fenster „Anmelden“ ein, und wählen Sie dann **Weiter** aus.
    1. Geben Sie das in der vorherigen Aufgabe notierte Kennwort ein. Wählen Sie **Anmelden**.
    1. Wählen Sie **Ja** aus, wenn Sie gefragt werden, ob Sie angemeldet bleiben möchten.

4. Da Sie sich erstmals als Adele Vance anmelden, werden Sie aufgefordert, Ihr Kennwort zurückzusetzen.  Geben Sie Ihr altes Kennwort ein.  Geben Sie **SC900-Lab** als neues Kennwort ein. Geben Sie **SC-900-Lab** in das Feld „Kennwort bestätigen“ ein.  Wählen Sie **Anmelden**.  Hinweis: Wir verwenden dieses Kennwort nur der Einfachheit halber für das Lab. Als bewährte Methode würden Sie in der Regel ein sichereres Kennwort eingeben.

5. Ein Popupfenster wird angezeigt und gibt an, dass weitere Informationen erforderlich sind,  Denn als Mitglied der Gruppe „SSPRSecurityUsers“ müssen sich die Gruppenmitglieder im Rahmen der Konfiguration registrieren, wenn sie sich anmelden.  Wählen Sie die Schaltfläche **Weiter** aus.  Hinweis:  Alternativ zur Registrierung durch die Benutzer können Administratoren die Authentifizierungsmethoden direkt konfigurieren, wenn sie einen Benutzer hinzufügen. Dazu müssen Administratoren die Telefonnummern und E-Mail-Adressen der Benutzer kennen und festlegen, um die Self-Service-Kennwortzurücksetzung auszuführen und um das Kennwort eines Benutzers zurückzusetzen.

6. Die Seite „Schützen Sie Ihr Konto“ wird geöffnet.  Das angezeigte Fenster ist für die Authentifizierungsmethode „Telefon“. Falls Sie nicht über ein Mobilgerät verfügen, das SMS empfangen kann, springen Sie zum nächsten Schritt.  Sie werden aufgefordert, eine Telefonnummer einzugeben. Stellen Sie sicher, dass die Option **Code per SMS an mich senden** aktiviert ist.   Geben Sie die Telefonnummer ein, über die Sie einen Code per SMS empfangen können, und wählen Sie die Schaltfläche **Weiter** aus.  Ein neues Fenster wird geöffnet, in dem angegeben wird, dass der Code soeben an das von Ihnen eingegebene Telefon gesendet wurde.  Geben Sie den empfangenen Code ein, und wählen Sie **Weiter** aus. In einem Fenster, das geöffnet wird, werden „Erfolg“ und Ihre „Standardanmeldemethode“ angezeigt.  Wählen Sie **Fertig** aus.  

7. Überspringen Sie diesen Schritt, falls Sie SSPR mit Ihrer Mobiltelefonnummer konfigurieren konnten.  Alternativ können Sie eine andere Methode als angezeigt im unteren linken Bereich des Fensters einrichten.  Wenn Sie eine andere Methode einrichten möchten, wählen Sie **Ich möchte eine andere Methode einrichten** aus. In einem angezeigten Popupfenster werden Sie Folgendes gefragt: „Welche Methode möchten Sie verwenden?“  Wählen Sie im Dropdown den Eintrag **E-Mail** als Ihre bevorzugte Methode aus. Wählen Sie dann die Schaltfläche **Bestätigen** aus.  Geben Sie die gewünschte E-Mail-Adresse ein, und wählen Sie dann **Weiter** aus.  Ein neues Fenster wird geöffnet, in dem angegeben wird, dass der Code soeben an die von Ihnen eingegebene E-Mail-Adresse gesendet wurde.  Greifen Sie auf die von Ihnen eingegebene E-Mail-Adresse zu, um den Code abzurufen.  Geben Sie den empfangenen Code ein, und wählen Sie **Weiter** aus. In einem Fenster, das geöffnet wird, werden „Erfolg“ und Ihre „Standardanmeldemethode“ angezeigt.  Wählen Sie **Fertig** aus.

8. Sie können ihre Anmeldung jetzt abschließen.  Sie sollten sich jetzt auf der Landing Page des Azure-Portals befinden.  Wenn Sie feststellen, dass die Anmeldezeit abgelaufen ist, geben Sie das Kennwort „SC900-Lab“ einfach noch einmal ein.

9. Melden Sie sich vom Azure-Portal ab, und schließen Sie das Browserfenster. 

#### <a name="task-4-optional-in-this-task-you-as-user-adele-vance-will-go-through-the-process-of-resetting-your-password"></a>Aufgabe 4 (optional): Bei dieser Aufgabe durchlaufen Sie als der Benutzer Adele Vance den Prozess zum Zurücksetzen Ihres Kennworts.

1. Öffnen Sie Microsoft Edge.

2. Geben Sie login.microsoftonline.com in die Adressleiste ein.

3. Melden Sie sich als Adele Vance an. Geben Sie dazu Ihre E-Mail-Adresse **AdeleV@WWLxZZZZ.onmicrosoft.com** ein (ZZZZZZ ist hierbei die eindeutige Mandanten-ID, die von Ihrem Labhostinganbieter bereitgestellt wurde), und wählen Sie die Schaltfläche **Weiter** aus. Es kann sein, dass stattdessen das Fenster „Konto auswählen“ geöffnet wird. Wählen Sie in diesem Fall das Konto für Adele Vance aus.

4. Wählen Sie **Ich habe mein Kennwort vergessen** im Fenster „Kennwort eingeben“ aus. 

5. Das Fenster „Konto wieder aktivieren“ wird geöffnet.   Vergewissern Sie sich, dass die E-Mail-Adresse für Adele Vance, AdeleV@WWLxZZZZ.onmicrosoft.com, im Feld für die E-Mail-Adresse oder den Benutzernamen angezeigt wird.  Falls nicht, geben Sie sie ein.  

6. Geben Sie in das leere Feld die im Bild angezeigten Zeichen oder die Wörter aus dem Audio ein. Wählen Sie nach der Eingabe **Weiter** aus.

7. Auf dem Bildschirm werden „Konto wieder aktivieren“ sowie „Überprüfungsschritt 1 > Neues Kennwort auswählen“ angezeigt. Übernehmen Sie die Standardeinstellung **Textnachricht an mein Mobiltelefon senden**.  Sie werden aufgefordert, Ihre Mobiltelefonnummer einzugeben.  Wählen Sie nach ihrer Eingabe die Schaltfläche **Textnachricht** aus.  Wenn Sie während der Registrierung „E-Mail“ ausgewählt haben, wird im Fenster „Konto wieder aktivieren“ die Meldung „Sie erhalten eine E-Mail mit einem Prüfcode unter Ihrer alternativen E-Mail-Adresse“ angezeigt.  Wählen Sie **E-Mail** aus. 

8. Geben Sie den Prüfcode ein, und klicken Sie auf **Weiter**.

9. Auf dem nächsten Bildschirm werden Sie aufgefordert, das neue Kennwort einzugeben und das neue Kennwort zu bestätigen.  Geben Sie diese neuen Kennwörter ein, und wählen Sie die Schaltfläche **Fertig stellen** aus.

10. Auf dem Bildschirm wird in einer Meldung angezeigt, dass Ihr Kennwort zurückgesetzt wurde.  Wählen Sie **Klicken Sie hier** aus, um sich mit Ihrem neuen Kennwort anzumelden.

11. Wählen Sie **AdeleV@WWLxZZZZZZ.onmicrosoft.com** im Informationsfeld „Konto auswählen“ aus, geben Sie Ihr neues Kennwort ein, und wählen Sie dann die Schaltfläche **Anmelden** aus.  Wenn Sie gefragt werden, ob Sie angemeldet bleiben möchten, wählen Sie **Nein** aus.

12. Sie sollten sich nun im Azure-Portal befinden.

13. Melden Sie sich ab. Wählen Sie dazu das in der oberen rechten Ecke des Bildschirms neben der E-Mail-Adresse befindliche Benutzersymbol und dann **Abmelden** aus. Schließen Sie dann alle Browserfenster.

#### <a name="task-5-optional--in-this-task-you-as-the-administrator-will-briefly-view-the-audit-logs-and-the-usage--insights-data-associated-with-password-reset"></a>Aufgabe 5 (optional):  Bei dieser Aufgabe zeigen Sie als Administrator kurz die Überwachungsprotokolle und die der Kennwortzurücksetzung zugeordneten Daten vom Typ „Nutzung & Erkenntnisse“ an.

1. Öffnen Sie Microsoft Edge.

2. Geben Sie **portal.azure.com** in die Adressleiste ein. 

3. Melden Sie sich mit Ihren Administratoranmeldeinformationen an.
    1. Geben Sie **admin@WWLxZZZZZZ.onmicrosoft.com** (ZZZZZZ ist hierbei die eindeutige Mandanten-ID, die von Ihrem Labhostinganbieter bereitgestellt wurde) in das Fenster „Anmelden“ ein, und wählen Sie dann **Weiter** aus.
    1. Geben Sie das Administratorkennwort ein, das Sie vom Labhostinganbieter erhalten haben sollten. Wählen Sie **Anmelden**.
    1. Wählen Sie **Ja** aus, wenn Sie gefragt werden, ob Sie angemeldet bleiben möchten.

4. Wählen Sie **Azure Active Directory** aus.  

5. Wählen Sie im linken Navigationsbereich **Kennwort zurücksetzen** aus.

6. Wählen Sie im linken Navigationsbereich **Überwachungsprotokolle** aus.  Beachten Sie die verfügbaren Informationen und die verfügbaren Filter.  Beachten Sie zudem, dass Sie Protokolle herunterladen können.  

7. Wählen Sie **Herunterladen** aus.  Beachten Sie, dass Sie den Download als CSV- oder JSON-Datei formatieren können.  Schließen Sie das Fenster. Wählen Sie dazu in der oberen rechten Ecke des Bildschirms das **X** aus.

8. Wählen Sie im linken Navigationsbereich **Nutzung & Erkenntnisse** aus.

9. Beachten Sie die verfügbaren Informationen, die sich auf die Registrierung beziehen.  Beachten Sie, dass die Aktualisierung dieser Daten dauern kann, selbst nachdem Sie eine Aktualisierung vornehmen. Daher werden die Registrierungs- oder Nutzungsdaten aus der vorherigen Aufgabe möglicherweise nicht angezeigt.

10. Wählen Sie oben auf der Seite **Nutzung** aus, um „Self-Service-Kennwortzurücksetzungen und Kontoentsperrungen nach Methode“ anzuzeigen.  Beachten Sie, dass die Aktualisierung dieser Daten dauern kann, selbst nachdem Sie eine Aktualisierung vornehmen. Daher werden die Nutzungsdaten aus der vorherigen Aufgabe möglicherweise nicht angezeigt.

11. Schließen Sie die geöffneten Browserregisterkarten.


#### <a name="review"></a>Überprüfung
In diesem Lab sind Sie als Administrator den Prozess der Aktivierung der Self-Service-Kennwortzurücksetzung durchgegangen. Bei aktivierter SSPR haben Sie anschließend die Rolle eines Benutzers übernommen und sind den Prozess der Registrierung für die SSPR und auch zur Zurücksetzung Ihres Kennworts durchgegangen.  Als Letztes haben Sie als Administrator erfahren, wo Sie auf die Überwachungsprotokolle und Daten vom Typ „Nutzung & Erkenntnisse“ für die SSPR zugreifen.