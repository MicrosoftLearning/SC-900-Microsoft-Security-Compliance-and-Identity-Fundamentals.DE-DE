---
lab:
  title: Microsoft Entra-Self-Service-Kennwortzurücksetzung
  module: Describe the authentication capabilities of Microsoft Entra ID
---

<!---
---
Lab: Titel: Erkunden der Azure AD-Authentifizierung mit Self-Service-Kennwortzurücksetzung' Lernpfad/Modul/Lerneinheit: Lernpfad: Beschreiben der Funktionen von Azure Active Directory (Azure AD), Teil von Microsoft Entra; Modul 2: Beschreiben der Authentifizierungsfunktionen von Azure AD; Lerneinheit 4: Beschreiben der Self-Service für Kennwort
---
--->

# Lab: Microsoft Entra Self-Service-Kennwortzurücksetzung (SSPR)

Dieses Lab ist den folgenden Learn-Inhalten zugeordnet:

- Lernpfad: Beschreiben der Funktionen von Microsoft Entra
- Modul: Beschreibung der Authentifizierungsfunktionen von Microsoft Entra ID
- Lerneinheit: Beschreiben der Self-Service-Kennwortzurücksetzung

## Labszenario

In diesem Lab durchlaufen Sie als Administrator den Prozess des Hinzufügens eines Benutzers zur SSPR-Sicherheitsgruppe, die bereits in Ihrem Microsoft 365-Mandanten eingerichtet ist. Bei aktivierter SSPR übernehmen Sie anschließend die Rolle eines Benutzers und durchlaufen den Prozess der Registrierung für SSPR und auch zur Zurücksetzung Ihres Kennworts.  Schließlich können Sie als Administrator*in Auditprotokolle sowie Nutzungsdaten u. Erkenntnisse zu SSPR anzeigen.

**Geschätzte Dauer**: 30 Minuten

### Aufgabe 1

In dieser Aufgabe durchlaufen Sie als Administrator einige der verfügbaren Konfigurationseinstellungen für SSPR.

1. Schließen Sie den Microsoft Edge-Browser. Geben Sie **https://entra.microsoft.com** in der Adressleiste ein und melden Sie sich mit den Administratoranmeldeinformationen für Microsoft 365 an, die von Ihrem autorisierten Labhoster (ALH) bereitgestellt wurden.
    1. Geben Sie **admin@WWLxZZZZZZ.onmicrosoft.com** (ZZZZZZ ist hierbei die eindeutige Mandanten-ID, die von Ihrem Lab-Hostinganbieter bereitgestellt wurde) in das Anmeldefenster ein, und wählen Sie dann **Weiter** aus.
    1. Geben Sie das Administratorkennwort ein, das von Ihrem Lab-Hostinganbieter bereitgestellt werden sollte. Wählen Sie **Anmelden**.
    1. Je nach Ihrem Lab-Hoster und abhängig davon, ob Sie sich zum ersten Mal beim Mandanten anmelden, werden Sie möglicherweise aufgefordert, den MFA-Registrierungsprozess abzuschließen. Wenn ja, befolgen Sie die Anweisungen auf dem Bildschirm, um MFA einzurichten.
    1. Sobald Sie angemeldet sind, werden Sie zur Seite „Microsoft 365 Admin Center“ weitergeleitet.

1. Erweitern Sie im linken Navigationsbereich die Option für **Schutz**, und wählen Sie dann **Kennwortzurücksetzung** aus.  

1. Es werden die Eigenschaften für die Self-Service-Kennwortzurücksetzung angezeigt. Wählen Sie das Informationssymbol neben dem Symbol aus, in dem die **Self-Services-Kennwortzurücksetzung aktiviert** ist, um die Beschreibung anzuzeigen. Stellen Sie sicher, dass **Ausgewählt** blau hervorgehoben ist. Bewegen Sie den Mauszeiger über das Informationssymbol neben dem Text **Gruppe auswählen** und beachten Sie die angezeigte Meldung „Definiert die Gruppe von Benutzern, die ihre eigenen Kennwörter zurücksetzen können“. Sie müssen Benutzer*innen in die Gruppe einschließen, sie können keine einzelnen Benutzer auswählen. Beachten Sie, dass bereits eine Gruppe aufgeführt ist: SSPRSecurityGroupUsers (diese Gruppe war als Teil Ihres Microsoft 365-Mandanten vorkonfiguriert). Beachten Sie schließlich das blaue Informationsfeld: „Diese Einstellungen gelten nur für Endbenutzer*innen in Ihrer Organisation. Administrator*innen können die Self-Service-Kennwortzurücksetzung immer durchführen. Sie müssen zum Zurücksetzen ihres Kennworts zwei Authentifizierungsmethoden anwenden.“

1. Wählen Sie im linken Navigationsbereich für die Kennwortzurücksetzung **Authentifizierungsmethoden** aus.

1. Wählen Sie für „Anzahl von erforderlichen Methoden zum Zurücksetzen“ **1** aus. Beachten Sie das Informationsfeld auf dem Bildschirm.

1. Beachten Sie die verschiedenen Methoden, die Benutzer*innen zur Verfügung stehen.  **E-Mail** und **Mobiltelefon** sollten bereits markiert sein. Wenn nicht, wählen Sie sie aus.

1. Wählen Sie im linken Navigationsbereich der Kennwortzurücksetzung die Option **Registrierung** aus.  

1. Stellen Sie sicher, dass die Einstellung „Von Benutzern bei der Anmeldung Registrierung verlangen“ auf **Ja** festgelegt ist.  Übernehmen Sie für die Einstellung „Anzahl der Tage, bevor Benutzer aufgefordert werden, ihre Authentifizierungsinformationen erneut zu bestätigen“ die Standardeinstellung von **180**.   Beachten Sie das Informationsfeld auf der Seite.

1. Wählen Sie im linken Navigationsbereich der Kennwortzurücksetzung die Option **Benachrichtigungen** aus.  

1. Stellen Sie sicher, dass die Einstellung „Benutzer über Kennwortzurücksetzungen benachrichtigen“ auf **Ja** festgelegt ist.  Belassen Sie die Einstellung „Benachrichtigen aller Administratoren, wenn andere Administratoren ihr Kennwort zurücksetzen“ bei **Nein**.

1. Beachten Sie, dass der Navigationsbereich „Kennwortzurücksetzung“ auch Optionen zum Anzeigen von Auditprotokollen und Nutzung u. Erkenntnisse enthält.

1. Schließen Sie das Kennwortzurücksetzungsfenster. Wählen Sie dazu in der oberen rechten Ecke der Seite das **X** aus. Dadurch kehren Sie zum Microsoft Entra Admin Center zurück.

1. Lassen Sie das Microsoft Entra-Fenster geöffnet.

### Aufgabe 2

In dieser Aufgabe fügen Sie als Administrator den Benutzer, den Sie in der vorherigen Labübung erstellt haben, der SSPR-Sicherheitsgruppe hinzu.

1. Öffnen Sie die Registerkarte Browser für die Startseite des Microsoft Entra Admin Centers **[entra.microsoft.com](https://entra.microsoft.com)** . Erweitern Sie bei Bedarf **Identität**.

1. Erweitern Sie im linken Navigationsbereich unter "Identität" **Gruppen** und wählen Sie dann **Alle Gruppen** aus.

1. Es wird eine Liste vorhandener Gruppen angezeigt. Geben Sie im Feld „Gruppen suchen“ **SSPR** ein, und wählen Sie dann in den Suchergebnissen **SSPRSecurityGroupUsers** aus.  Sie gelangen zu der Konfigurationsoption für diese Gruppe.

1. Wählen Sie im linken Navigationsbereich die Option **Mitglieder** aus.

1. Wählen Sie oben auf der Seite die Option **+ Mitglieder hinzufügen** aus.  

1. Geben Sie im Suchfeld den Namen **Sara Perez** ein.  Sobald der Benutzer **Sara Perez** unterhalb des Suchfelds angezeigt wird, wählen Sie ihn aus, indem Sie unten auf der Seite auf **Auswählen** klicken.  Sie werden zur Mitgliederseite zurückgeleitet.  Wählen Sie oben auf der Seite **Aktualisieren** aus. Sara Perez sollte nun als Mitglied in der SSPR-Sicherheitsgruppe aufgeführt werden.

1. Melden Sie sich von allen Browserregisterkarten ab, indem Sie auf das Benutzersymbol neben der E-Mail-Adresse in der oberen rechten Ecke des Bildschirms klicken. Schließen Sie dann alle Browserfenster.

### Aufgabe 3

Bei dieser Aufgabe durchlaufen Sie als der Benutzerin Sara Perez den Registrierungsprozess für die Self-Service-Kennwortzurücksetzung.

1. Öffnen Sie Microsoft Edge, und geben Sie in der Adressleiste **https://login.microsoft.com** ein.

1. Melden Sie sich als Sara Perez an. Für den Anmeldevorgang ist möglicherweise MFA erforderlich.

1. Ein Popup zeigt an, dass weitere Informationen erforderlich sind.  Denn als Mitglied der Gruppe „SSPRSecurityGroupUsers“ müssen sich die Gruppenmitglieder im Rahmen der Konfiguration registrieren, wenn sie sich anmelden.  Wählen Sie die Schaltfläche **Weiter** aus.  Hinweis: Eine Alternative dazu, dass Benutzer*innen die Registrierung selbst durchführen, ist, dass Administrator*innen die Authentifizierungsmethoden beim Hinzufügen von Benutzer*innen direkt konfigurieren. Dazu müssen Administratoren die Telefonnummern und E-Mail-Adressen der Benutzer kennen und festlegen, um die Self-Service-Kennwortzurücksetzung auszuführen und um das Kennwort eines Benutzers zurückzusetzen.

1. Die Seite „Ihr Konto schützen“ wird geöffnet.  Das angezeigte Fenster und die folgenden Schritte gelten für die Microsoft Authenticator-App-Methode. Wenn Sie stattdessen eine E-Mail verwenden möchten, wählen Sie **Ich möchte eine andere Methode einrichten** und folgen Sie den Schritten.
    1. Wenn Sie die Microsoft Authenticator-App bereits auf Ihrem mobilen Gerät installiert haben, wählen Sie **Weiter**. Andernfalls wählen Sie **Jetzt herunterladen** und folgen Sie den Schritten.
    1. Sie beginnen mit dem Einrichten Ihres Kontos.  Wählen Sie **Weiter** aus.
    1. Wählen Sie auf Ihrem Mobilgerät in der Microsoft Authenticator-App die Option **+**, um ein Konto hinzuzufügen, und wählen Sie **Geschäfts- oder Schulkonto**.
    1. Wählen Sie die Option **QR-Code scannen**, und scannen Sie dann mit Ihrem mobilen Gerät den QR-Code auf dem Bildschirm Ihres PCs.
    1. Führen Sie die Schritte auf Ihrem PC und mobilen Gerät aus, und wählen Sie dann **Weiter** aus.
    1. Nachdem Sie Ihre Sicherheitsinformationen eingerichtet haben, wird ein Erfolgsfenster angezeigt.  Wählen Sie **Fertig** aus.

1. Sie können ihre Anmeldung jetzt abschließen. Wenn Sie feststellen, dass die Anmeldezeit abgelaufen ist, geben Sie das Kennwort einfach erneut ein.

1. Melden Sie sich von allen Browserregisterkarten ab, indem Sie auf das Benutzersymbol neben der E-Mail-Adresse in der oberen rechten Ecke des Bildschirms klicken. Schließen Sie dann alle Browserfenster.

### Aufgabe 4 (optional)

Bei dieser Aufgabe durchlaufen Sie als die Benutzerin Sara Perez den Prozess zum Zurücksetzen Ihres Kennworts

1. Öffnen Sie Microsoft Edge.

1. Geben Sie in der Adressleiste **https://login.microsoft.com** ein.

1. Melden Sie sich als Sara Perez an. Geben Sie dazu Ihre E-Mail-Adresse **sara@WWLxZZZZ.onmicrosoft.com** ein (ZZZZZZ ist hierbei die eindeutige Mandanten-ID, die von Ihrem Labhostinganbieter bereitgestellt wurde) und wählen Sie die Schaltfläche **Weiter** aus. Es kann sein, dass stattdessen das Konto auswählen Fenster geöffnet wird. Wählen Sie in diesem Fall das Konto für Sara Perez aus.

1. Wählen Sie im Fenster „Kennwort eingeben“ die Option **Kennwort vergessen** aus.

1. Das Fenster „Konto wieder aktivieren“ wird geöffnet.   Vergewissern Sie sich, dass die E-Mail-Adresse für Sara Perez, sara@WWLxZZZZ.onmicrosoft.com, im Feld für die E-Mail-Adresse oder den Benutzernamen angezeigt wird.  Wenn nicht, geben Sie hinein.  

1. Geben Sie in das leere Feld die im Bild angezeigten Zeichen oder die Wörter aus dem Audio ein. Wählen Sie nach der Eingabe **Weiter** aus.

1. Auf dem Bildschirm wird „Konto wieder aktivieren“ und „Überprüfungsschritt 1 > Neues Kennwort auswählen“ angezeigt. Wählen Sie die Option **Benachrichtigung auf meiner Authenticator-App genehmigen** und wählen Sie dann **Benachrichtigung senden**.

1. Notieren Sie sich die Nummer auf Ihrem PC, und folgen Sie den Anweisungen, um die Anmeldung mithilfe der Microsoft Authenticator-App auf Ihrem mobilen Gerät zu genehmigen.

1. Auf dem nächsten Bildschirm werden Sie aufgefordert, das neue Kennwort einzugeben und das neue Kennwort zu bestätigen.  Geben Sie diese jetzt ein, und klicken Sie auf die Schaltfläche **Fertigstellen**.

1. Auf dem Bildschirm wird eine Meldung angezeigt, dass Ihr Kennwort zurückgesetzt wurde.  Klicken Sie auf **Hier klicken**, um sich mit Ihrem neuen Kennwort anzumelden.

1. Wählen Sie **sara@WWLxZZZZZZ.onmicrosoft.com** im Informationsfeld „Konto auswählen“ aus, geben Sie Ihr neues Kennwort ein, und wählen Sie dann die Schaltfläche **Anmelden** aus.  Wenn Sie gefragt werden, ob Sie angemeldet bleiben möchten, **Nein** aus.

1. Sie sollten jetzt beim Microsoft-Konto von Sara angemeldet sein.

1. Melden Sie sich ab. Klicken Sie dazu auf das in der oberen rechten Ecke des Bildschirms neben der E-Mail-Adresse befindliche Benutzersymbol und dann auf **Abmelden**. Schließen Sie dann alle Browserfenster.

### Aufgabe 5 (optional)

Bei dieser Aufgabe zeigen Sie als Administrator kurz die Überwachungsprotokolle und die der Kennwortzurücksetzung zugeordneten Daten vom Typ „Nutzung und Erkenntnisse“ an.

1. Öffnen Sie Microsoft Edge.

1. Geben Sie **https://entra.microsoft.com** in der Adressleiste ein und melden Sie sich mit den Administratoranmeldeinformationen für Microsoft 365 an, die von Ihrem autorisierten Labhoster (ALH) bereitgestellt wurden.

1. Sie sind im Microsoft Entra Admin Center.  Erweitern Sie im linken Navigationsbereich die Option für **Schutz**, und wählen Sie dann **Kennwortzurücksetzung** aus.

1. Wählen Sie im linken Navigationsbereich die Option **Auditprotokolle** aus.  Beachten Sie die verfügbaren Informationen und Filter.  Sie können auch Protokolle herunterladen.  

1. Wählen Sie **Herunterladen** aus.  Beachten Sie, dass Sie den Download als CSV oder JSON formatieren können.  Schließen Sie das Fenster. Klicken Sie dazu in der oberen rechten Ecke des Bildschirms auf das **X**.

1. Wählen Sie im linken Navigationsbereich die Option **Nutzung u. Erkenntnisse** aus.

1. Beachten Sie die verfügbaren Informationen zur Registrierung.  Beachten Sie, dass es einige Zeit dauern kann, bis diese Daten aktualisiert sind, auch wenn Sie eine Aktualisierung durchgeführt haben, sodass möglicherweise die Registrierungs- oder Nutzungsdaten aus der vorherigen Aufgabe noch nicht darin widergespiegelt werden.

1. Wählen Sie oben auf der Seite **Nutzung** aus, um die Anzahl der Self-Service-Kennwortzurücksetzungen und Kontoentsperrungen nach Methode anzuzeigen.  Beachten Sie, dass, auch wenn Sie eine Aktualisierung durchgeführt haben, es einige Zeit dauern kann, bis diese Daten aktualisiert sind, sodass sich möglicherweise die Nutzungsdaten aus der vorherigen Aufgabe noch nicht darin widerspiegeln.

1. Schließen Sie die geöffneten Browserregisterkarten.

### Überprüfung

In diesem Lab haben Sie als Administrator*in den Prozess zum Aktivieren der Self-Service-Kennwortzurücksetzung durchlaufen. Bei aktivierter SSPR übernehmen Sie anschließend die Rolle eines Benutzers, um den Prozess der Registrierung für SSPR und auch zur Zurücksetzung Ihres Kennworts zu durchlaufen.  Schließlich erfahren Sie als Administrator*in, wo Sie auf Auditprotokolle und Nutzungs- und Erkenntnis-Daten für SSPR zugreifen können.
