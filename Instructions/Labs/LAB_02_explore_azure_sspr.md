<!---
---
Lab: Titel: Erkunden der Azure AD-Authentifizierung mit Self-Service-Kennwortzurücksetzung' Lernpfad/Modul/Lerneinheit: Lernpfad: Beschreiben der Funktionen von Azure Active Directory (Azure AD), Teil von Microsoft Entra; Modul 2: Beschreiben der Authentifizierungsfunktionen von Azure AD; Lerneinheit 4: Beschreiben der Self-Service für Kennwort
---
--->

# Lab: Microsoft Entra Self-Service-Kennwortzurücksetzung (SSPR)

Dieses Lab ist den folgenden Learn-Inhalten zugeordnet:

- Lernpfad: Beschreiben der Funktionen der Microsoft Entra
- Modul: Beschreibung der Authentifizierungsfunktionen von Microsoft Entra ID
- Lerneinheit: Beschreiben der Self-Service-Kennwortzurücksetzung

## Labszenario

In diesem Lab durchlaufen Sie als Administrator den Prozess des Hinzufügens eines Benutzers zur SSPR-Sicherheitsgruppe, die bereits in Ihrem Microsoft 365-Mandanten eingerichtet ist. Bei aktivierter SSPR übernehmen Sie anschließend die Rolle eines Benutzers und durchlaufen den Prozess der Registrierung für SSPR und auch zur Zurücksetzung Ihres Kennworts.  Schließlich können Sie als Administrator Überwachungsprotokolle sowie Nutzungsdaten und Erkenntnisse für die SSPR anzeigen.

**Geschätzte Dauer**: 15 bis 20 Minuten

### Aufgabe 1

In dieser Aufgabe durchlaufen Sie als Administrator einige der verfügbaren Konfigurationseinstellungen für SSPR.

1. Schließen Sie den Microsoft Edge-Browser. Geben Sie **https://entra.microsoft.com** in der Adressleiste ein und melden Sie sich mit den Administratoranmeldeinformationen für Microsoft 365 an, die von Ihrem autorisierten Labhoster (ALH) bereitgestellt wurden.
    1. Geben Sie **admin@WWLxZZZZZZ.onmicrosoft.com** (ZZZZZZ ist hierbei die eindeutige Mandanten-ID, die von Ihrem Lab-Hostinganbieter bereitgestellt wurde) in das Anmeldefenster ein, und wählen Sie dann **Weiter** aus.
    1. Geben Sie das Administratorkennwort ein, das von Ihrem Lab-Hostinganbieter bereitgestellt werden sollte. Wählen Sie **Anmelden**.
    1. Wählen Sie **Ja** aus, wenn Sie gefragt werden, ob Sie angemeldet bleiben möchten.

1. Erweitern Sie im linken Navigationsbereich die Option für **Schutz**, und wählen Sie dann **Kennwortzurücksetzung** aus.  

1. Die Eigenschaften für die Self-Service-Kennwortzurücksetzung werden angezeigt. Wählen Sie das Informationssymbol neben dem Symbol aus, in dem die **Self-Services-Kennwortzurücksetzung aktiviert** ist, um die Beschreibung anzuzeigen. Stellen Sie sicher, dass **Ausgewählt** blau hervorgehoben ist. Bewegen Sie den Mauszeiger über das Informationssymbol neben dem Text **Gruppe auswählen** und beachten Sie die angezeigte Meldung „Definiert die Gruppe von Benutzern, die ihre eigenen Kennwörter zurücksetzen können“. Sie müssen Benutzer in die Gruppe aufnehmen. Es ist nicht möglich, Benutzer einzeln auszuwählen. Beachten Sie, dass bereits eine Gruppe aufgeführt ist: SSPRSecurityGroupUsers (diese Gruppe war als Teil Ihres Microsoft 365-Mandanten vorkonfiguriert). Beachten Sie als Letztes das blaue Informationsfeld: „Diese Einstellungen gelten nur für Endbenutzer in Ihrer Organisation. Administratoren können die Self-Service-Kennwortzurücksetzung immer durchführen und müssen zum Zurücksetzen ihres Kennworts zwei Authentifizierungsmethoden verwenden.“

1. Wählen Sie im linken Navigationsbereich von „Kennwort zurücksetzen“ die Option **Authentifizierungsmethoden** aus.

1. Wählen Sie **1** in „Anzahl von Methoden, die zurückgesetzt werden müssen“ aus. Beachten Sie das Informationsfeld auf dem Bildschirm.

1. Beachten Sie die unterschiedlichen Methoden, die für Benutzer verfügbar sind.  **E-Mail** und **Mobiltelefon (nur SMS)** sollten bereits aktiviert sein. Falls nicht, aktivieren Sie sie.

1. Wählen Sie im linken Navigationsbereich von „Kennwort zurücksetzen“ die Option **Registrierung** aus.  

1. Stellen Sie sicher, dass die Einstellung „Registrierung von Benutzern bei der Anmeldung verlangen?“ auf **Ja** festgelegt ist.  Übernehmen Sie für die Einstellung „Anzahl der Tage, bevor Benutzer aufgefordert werden, ihre Authentifizierungsinformationen erneut zu bestätigen“ die Standardeinstellung von 180.   Beachten Sie das Informationsfeld auf der Seite.

1. Wählen Sie im linken Navigationsbereich von „Kennwort zurücksetzen“ die Option **Benachrichtigungen** aus.  

1. Stellen Sie sicher, dass die Einstellung „Benutzer über Kennwortzurücksetzungen benachrichtigen“ auf **Ja** festgelegt ist.  Übernehmen Sie „Nein“ für die Einstellung „Alle Administratoren benachrichtigen, wenn andere Administratoren ihr Kennwort zurücksetzen“.

1. Beachten Sie, dass der Navigationsbereich „Kennwort zurücksetzen“ auch Optionen zum Anzeigen der Überwachungsprotokolle und von „Nutzung & Erkenntnisse“ umfasst.

1. Schließen Sie das Kennwortzurücksetzungsfenster. Wählen Sie dazu in der oberen rechten Ecke der Seite das **X** aus. Dadurch kehren Sie zum Microsoft Entra Admin Center zurück.

1. Lassen Sie das Microsoft Entra-Fenster geöffnet.

### Aufgabe 2

In dieser Aufgabe fügen Sie als Administrator den Benutzer, den Sie in der vorherigen Labübung erstellt haben, der SSPR-Sicherheitsgruppe hinzu.

1. Öffnen Sie die Registerkarte Browser für die Startseite des Microsoft Entra Admin Centers **[entra.microsoft.com](https://entra.microsoft.com)** . Erweitern Sie bei Bedarf **Identität**.

1. Erweitern Sie im linken Navigationsbereich unter "Identität" **Gruppen** und wählen Sie dann **Alle Gruppen** aus.

1. Eine Liste der vorhandenen Gruppen wird angezeigt. Geben Sie in das Feld „Gruppen durchsuchen“ den Text **SSPR** ein. Wählen Sie dann **SSPRSecurityGroupUsers** aus den Suchergebnissen aus.  Dadurch gelangen Sie zur Konfigurationsoption für diese Gruppe.

1. Wählen Sie im linken Navigationsbereich **Mitglieder** aus.

1. Wählen Sie oben auf der Seite **+ Mitglieder hinzufügen** aus.  

1. Geben Sie im Suchfeld den Namen **Sara Perez** ein.  Sobald der Benutzer **Sara Perez** unterhalb des Suchfelds angezeigt wird, wählen Sie ihn aus, indem Sie unten auf der Seite auf **Auswählen** klicken.  Sie werden zur Mitgliederseite zurückgeleitet.  Wählen Sie oben auf der Seite **Aktualisieren** aus. Sara Perez sollte nun als Mitglied in der SSPR-Sicherheitsgruppe aufgeführt werden.

1. Melden Sie sich von allen Browserregisterkarten ab. Klicken Sie dazu auf das Benutzersymbol neben der E-Mail-Adresse in der oberen rechten Ecke des Bildschirms. Schließen Sie dann alle Browserfenster.

### Aufgabe 3

Bei dieser Aufgabe durchlaufen Sie als der Benutzerin Sara Perez den Registrierungsprozess für die Self-Service-Kennwortzurücksetzung.  Für diese Aufgabe müssen Sie über Zugriff auf ein Mobilgerät, auf dem Sie SMS empfangen können, oder über ein persönliches E-Mail-Konto verfügen, auf das Sie zugreifen können.

1. Öffnen Sie Microsoft Edge, und geben Sie in der Adressleiste **https://login.microsoft.com** ein.

1. Melden Sie sich als Sara Perez an.

1. Ein Popupfenster wird angezeigt und gibt an, dass weitere Informationen erforderlich sind,  Denn als Mitglied der Gruppe „SSPRSecurityGroupUsers“ müssen sich die Gruppenmitglieder im Rahmen der Konfiguration registrieren, wenn sie sich anmelden.  Wählen Sie die Schaltfläche **Weiter** aus.  Hinweis:  Alternativ zur Registrierung durch die Benutzer können Administratoren die Authentifizierungsmethoden direkt konfigurieren, wenn sie einen Benutzer hinzufügen. Dazu müssen Administratoren die Telefonnummern und E-Mail-Adressen der Benutzer kennen und festlegen, um die Self-Service-Kennwortzurücksetzung auszuführen und um das Kennwort eines Benutzers zurückzusetzen.

1. Die Seite „Schützen Sie Ihr Konto“ wird geöffnet.  Das angezeigte Fenster ist für die Authentifizierungsmethode „Telefon“. Falls Sie nicht über ein Mobilgerät verfügen, das SMS empfangen kann, springen Sie zum nächsten Schritt.  Sie werden aufgefordert, eine Telefonnummer einzugeben. Stellen Sie sicher, dass die Option **Code per SMS an mich senden** aktiviert ist.   Geben Sie die Telefonnummer ein, über die Sie einen Code per SMS empfangen können, und wählen Sie die Schaltfläche **Weiter** aus.  Ein neues Fenster wird geöffnet, in dem angegeben wird, dass der Code an das von Ihnen eingegebene Telefon gesendet wurde.  Geben Sie den empfangenen Code ein, und wählen Sie **Weiter** aus. In einem Fenster, das geöffnet wird, werden „Erfolg“ und Ihre „Standardanmeldemethode“ angezeigt.  Wählen Sie **Fertig**aus.  
    1. Alternativ können Sie auch eine andere Methode festlegen, wie unten links im Fenster gezeigt.  Wenn Sie eine andere Methode einrichten möchten, wählen Sie **Ich möchte eine andere Methode einrichten** aus. In einem angezeigten Popupfenster werden Sie Folgendes gefragt: „Welche Methode möchten Sie verwenden?“  Wählen Sie in der Dropdownliste den Eintrag **E-Mail** als Ihre bevorzugte Methode aus. Wählen Sie dann die Schaltfläche **Bestätigen** aus.  Geben Sie die gewünschte E-Mail-Adresse ein, und wählen Sie dann **Weiter** aus.  Ein neues Fenster wird geöffnet, in dem angegeben wird, dass der Code an die von Ihnen eingegebene E-Mail-Adresse gesendet wurde.  Greifen Sie auf die von Ihnen eingegebene E-Mail-Adresse zu, um den Code abzurufen.  Geben Sie den empfangenen Code ein, und wählen Sie **Weiter** aus. In einem Fenster, das geöffnet wird, werden „Erfolg“ und Ihre „Standardanmeldemethode“ angezeigt.  Wählen Sie **Fertig**aus.

1. Sie können ihre Anmeldung jetzt abschließen. Wenn Sie feststellen, dass die Anmeldezeit abgelaufen ist, geben Sie das Kennwort einfach erneut ein.

1. Melden Sie sich von allen Browserregisterkarten ab. Klicken Sie dazu auf das Benutzersymbol neben der E-Mail-Adresse in der oberen rechten Ecke des Bildschirms. Schließen Sie dann alle Browserfenster.

### Aufgabe 4 (optional)

Bei dieser Aufgabe durchlaufen Sie als die Benutzerin Sara Perez den Prozess zum Zurücksetzen Ihres Kennworts

1. Öffnen Sie Microsoft Edge.

1. Geben Sie in der Adressleiste **https://login.microsoftonline.com** ein.

1. Melden Sie sich als Sara Perez an. Geben Sie dazu Ihre E-Mail-Adresse **sara@WWLxZZZZ.onmicrosoft.com** ein (ZZZZZZ ist hierbei die eindeutige Mandanten-ID, die von Ihrem Labhostinganbieter bereitgestellt wurde) und wählen Sie die Schaltfläche **Weiter** aus. Es kann sein, dass stattdessen das Konto auswählen Fenster geöffnet wird. Wählen Sie in diesem Fall das Konto für Sara Perez aus.

1. Wählen Sie **Ich habe mein Kennwort vergessen** im Fenster „Kennwort eingeben“ aus.

1. Das Fenster „Konto wieder aktivieren“ wird geöffnet.   Vergewissern Sie sich, dass die E-Mail-Adresse für Sara Perez, sara@WWLxZZZZ.onmicrosoft.com, im Feld für die E-Mail-Adresse oder den Benutzernamen angezeigt wird.  Falls nicht, geben Sie sie ein.  

1. Geben Sie in das leere Feld die im Bild angezeigten Zeichen oder die Wörter aus dem Audio ein. Wählen Sie nach der Eingabe **Weiter** aus.

1. Auf dem Bildschirm werden „Konto wieder aktivieren“ sowie „Überprüfungsschritt 1 > Neues Kennwort auswählen“ angezeigt. Übernehmen Sie die Standardeinstellung **Textnachricht an mein Mobiltelefon senden**.  Sie werden aufgefordert, Ihre Mobiltelefonnummer einzugeben.  Wählen Sie nach ihrer Eingabe die Schaltfläche **Textnachricht** aus.  Wenn Sie während der Registrierung „E-Mail“ ausgewählt haben, wird im Fenster „Konto wieder aktivieren“ die Meldung „Sie erhalten eine E-Mail mit einem Prüfcode unter Ihrer alternativen E-Mail-Adresse“ angezeigt.  Wählen Sie **E-Mail** aus.

1. Geben Sie den Prüfcode ein, und klicken Sie auf **Weiter**.

1. Auf dem nächsten Bildschirm werden Sie aufgefordert, das neue Kennwort einzugeben und das neue Kennwort zu bestätigen.  Geben Sie diese neuen Kennwörter ein, und wählen Sie die Schaltfläche **Fertig stellen** aus.

1. Auf dem Bildschirm wird eine Meldung angezeigt, dass Ihr Kennwort zurückgesetzt wurde.  Wählen Sie **Klicken Sie hier** aus, um sich mit Ihrem neuen Kennwort anzumelden.

1. Wählen Sie **sara@WWLxZZZZZZ.onmicrosoft.com** im Informationsfeld „Konto auswählen“ aus, geben Sie Ihr neues Kennwort ein, und wählen Sie dann die Schaltfläche **Anmelden** aus.  Wenn Sie gefragt werden, ob Sie angemeldet bleiben möchten, wählen Sie **Nein** aus.

1. Sie sollten sich nun im Office-Portal befinden.

1. Melden Sie sich ab. Wählen Sie dazu das in der oberen rechten Ecke des Bildschirms neben der E-Mail-Adresse befindliche Benutzersymbol und dann **Abmelden** aus. Schließen Sie dann alle Browserfenster.

### Aufgabe 5 (optional)

Bei dieser Aufgabe zeigen Sie als Administrator kurz die Überwachungsprotokolle und die der Kennwortzurücksetzung zugeordneten Daten vom Typ „Nutzung und Erkenntnisse“ an.

1. Öffnen Sie Microsoft Edge.

1. Geben Sie **https://entra.microsoft.com** in der Adressleiste ein und melden Sie sich mit den Administratoranmeldeinformationen für Microsoft 365 an, die von Ihrem autorisierten Labhoster (ALH) bereitgestellt wurden.

1. Sie sind im Microsoft Entra Admin Center.  Erweitern Sie im linken Navigationsbereich die Option für **Schutz**, und wählen Sie dann **Kennwortzurücksetzung** aus.

1. Wählen Sie im linken Navigationsbereich **Überwachungsprotokolle** aus.  Beachten Sie die verfügbaren Informationen und die verfügbaren Filter.  Beachten Sie zudem, dass Sie Protokolle herunterladen können.  

1. Wählen Sie **Herunterladen** aus.  Beachten Sie, dass Sie den Download als CSV- oder JSON-Datei formatieren können.  Schließen Sie das Fenster. Wählen Sie dazu in der oberen rechten Ecke des Bildschirms das **X** aus.

1. Wählen Sie im linken Navigationsbereich **Nutzung & Erkenntnisse** aus.

1. Beachten Sie die verfügbaren Informationen, die sich auf die Registrierung beziehen.  Beachten Sie, dass die Aktualisierung dieser Daten dauern kann, selbst nachdem Sie eine Aktualisierung vornehmen. Daher werden die Registrierungs- oder Nutzungsdaten aus der vorherigen Aufgabe möglicherweise nicht angezeigt.

1. Wählen Sie oben auf der Seite **Nutzung** aus, um „Self-Service-Kennwortzurücksetzungen und Kontoentsperrungen nach Methode“ anzuzeigen.  Beachten Sie, dass die Aktualisierung dieser Daten dauern kann, selbst nachdem Sie eine Aktualisierung vornehmen. Daher werden die Nutzungsdaten aus der vorherigen Aufgabe möglicherweise nicht angezeigt.

1. Schließen Sie die geöffneten Browserregisterkarten.

### Überprüfung

In diesem Lab sind Sie als Administrator den Prozess der Aktivierung der Self-Service-Kennwortzurücksetzung durchgegangen. Bei aktivierter SSPR übernehmen Sie anschließend die Rolle eines Benutzers, um den Prozess der Registrierung für SSPR und auch zur Zurücksetzung Ihres Kennworts zu durchlaufen.  Als Letztes haben Sie als Administrator erfahren, wo Sie auf die Überwachungsprotokolle und Daten vom Typ „Nutzung & Erkenntnisse“ für die SSPR zugreifen.
