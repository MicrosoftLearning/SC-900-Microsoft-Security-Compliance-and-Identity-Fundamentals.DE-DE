---
lab:
  title: Erkunden von Privileged Identity Management
  module: Describe the identity protection and governance capabilities of Microsoft Entra
---

# Lab: Azure Privileged Identity Management

Dieses Lab ist den folgenden Learn-Inhalten zugeordnet:

- Lernpfad: Beschreiben der Funktionen von Microsoft Entra
- Modul: Beschreiben der Identitätsschutz- und Governancefunktionen von Microsoft Entra
- Lerneinheit: Beschreiben der Funktionen von Privileged Identity Management

## Labszenario

In diesem Lab erkunden Sie einige der grundlegenden Funktionen von Privileged Identity Management (PIM). PIM erfordert Microsoft Entra-ID P2-Lizenzierung.  In diesem Lab konfigurieren Sie als Administrator durch Privileged Identity Management (PIM) einen Ihrer Benutzer, Diego Siciliani, mit einer Microsoft Entra-Benutzeradministratorrolle.   Mit Benutzeradministratorrechten kann Diego Lizenzen zum Verwalten von Benutzern und Gruppen erstellen und vieles mehr.  Sowohl der Administrator als auch der Benutzer Diego müssen für die Microsoft Entra ID Premium P2-Lizenzierung konfiguriert sein.

**Geschätzte Dauer**: 60 Minuten

### Aufgabe 1

Bei dieser Aufgabe setzen Sie als Administrator*in das Kennwort für den Benutzer Diego Siciliani zurück. Dieser Schritt ist erforderlich, damit Sie sich anfangs als der Benutzer in nachfolgenden Aufgaben anmelden können.

1. Öffnen Sie Microsoft Edge.  Geben Sie in der Adressleiste **https://entra.microsoft.com** ein.

1. Melden Sie sich mit den Microsoft 365-Administratoranmeldeinformationen an, die von Ihrer ALH bereitgestellt werden.
    1. Geben Sie **admin@WWLxZZZZZZ.onmicrosoft.com** (ZZZZZZ ist hierbei die eindeutige Mandanten-ID, die von Ihrem Lab-Hostinganbieter bereitgestellt wurde) in das Anmeldefenster ein, und wählen Sie dann **Weiter** aus.
    1. Geben Sie das Administratorkennwort ein, das von Ihrem Lab-Hostinganbieter bereitgestellt werden sollte. Wählen Sie **Anmelden**.
    1. Je nach Ihrem Lab-Hoster und abhängig davon, ob Sie sich zum ersten Mal beim Mandanten anmelden, werden Sie möglicherweise aufgefordert, den MFA-Registrierungsprozess abzuschließen. Wenn ja, befolgen Sie die Anweisungen auf dem Bildschirm, um MFA einzurichten.
    1. Sobald Sie angemeldet sind, werden Sie zur Seite „Microsoft 365 Admin Center“ weitergeleitet.

1. Erweitern Sie im linken Navigationsbereich **Identität**, erweitern Sie **Benutzer**, und wählen Sie dann **Alle Benutzer** aus.

1. Wählen Sie **Diego Siciliani** aus der Liste der Benutzer'innen aus.

1. Wählen Sie oben auf der Seite **Kennwort zurücksetzen** aus. Da Sie sich noch nicht als Diego angemeldet haben, kennen Sie sein Kennwort nicht. Daher müssen Sie das Kennwort zurücksetzen.

1. Wenn das Kennwortzurücksetzungsfenster geöffnet wird, wählen Sie **Kennwort zurücksetzen** aus.  WICHTIG: Notieren Sie das neue Kennwort. Sie benötigen es in einer nachfolgenden Aufgabe, um sich als der Benutzer anmelden zu können.

1. Wählen Sie im linken Navigationsbereich die Option **Startseite** aus, um zur Startseite von Microsoft Entra Admin Center zurückzukehren.

1. Lassen Sie die Browserseite geöffnet, da Sie sie in der nachfolgenden Aufgabe benötigen.

### Aufgabe 2

Bei dieser Aufgabe weisen Sie als Admin in Privileged Identity Management Diego eine Microsoft Entra ID-Rolle zu.

1. Öffnen Sie die Registerkarte Browser für die Startseite des Microsoft Entra Admin Centers.

1. Erweitern Sie im linken Navigationsbereich den Eintrag **ID Governance**, und wählen Sie dann **Privileged Identity Management** aus.

1. Sie befinden sich nun im Fenster für den Schnellstart in Privileged Identity Management. Schauen Sie sich die Informationen auf der Seite Erste Schritte erneut an. Wählen Sie im Hauptfenster unter dem Punkt „Zugriff verwalten“ die Option **Verwalten**.

1. Sie befinden sich nun auf der Seite für die Contoso-Rollen.  Geben Sie oben auf der Seite in der Suchleiste **Benutzer** ein.  Wählen Sie in den Suchergebnissen **iBenutzeradministrator*in** aus.

1. Wählen Sie oben auf der Seite **+ Zuweisung hinzufügen** aus.

1. Vergewissern Sie sich, dass auf der Seite „Zuweisungen hinzufügen“ **Mitgliedschaft** unterstrichen ist.  Hier konfigurieren Sie die Mitgliedschaftseinstellungen für die Benutzeradministratorrolle in PIM.

1. Lassen Sie den Bereichstyp auf den Standardwert „Verzeichnis“ festgelegt.  

1. Wählen Sie unter Mitglieder auswählen die Option **Keine Mitglieder ausgewählt** aus. Dadurch wird das Fenster „Mitglied auswählen“ geöffnet.

1. Geben Sie in der Suchleiste **Diego** ein.  Wählen Sie in den Suchergenissen **Diego Siciliani** aus, und klicken Sie dann am unteren Rand der Seite auf **Auswählen**.  

1. Unter „Mitglieder auswählen“ werden „1 Mitglied ausgewählt“ und der Name und die E-Mail-Adresse des ausgewählten Mitglieds, Diego Siciliani, angezeigt. Klicken Sie unten auf der Seite „Aufgabe hinzufügen“ auf **Weiter**.  

1. Sie befinden sich nun auf der Seite „Einstellung“.  Lassen Sie den Zuweisungstyp auf die Standardeinstellung „Berechtigt“ festgelegt.

1. Wenn das Kontrollkästchen „Dauerhaft berechtigt“ aktiviert ist, wählen Sie **Dauerhaft berechtigt** aus, um das Häkchen zu entfernen.

1. Behalten Sie in den Feldern „Zuweisungsbeginn“ das Standarddatum und die Standardzeit bei, d. h. den heutigen Tag und die aktuelle Uhrzeit.

1. Ändern Sie in den Feldern „Zuweisungsende“ das Datum in das heutige Datum (beachten Sie, dass die Standardeinstellung ein Jahr ab dem heutigen Tag ist, daher müssen Sie das Jahr ändern). Legen Sie die Zeit auf zwei Stunden ab der aktuellen Uhrzeit fest. Nachdem Sie das Zeitfeld für den Zeitpunkt festgelegt haben, zu dem die Aufgabe endet, drücken Sie die TAB-TASTE auf der Tastatur, und wählen Sie unten auf der Seite **Zuweisen** aus.  

1. Dadurch gelangen Sie zurück zum Fenster „Zuweisungen“.  Nach ein paar Sekunden sollte Diego Siciliani in der Tabelle „Benutzeradministrator“ zusammen mit den Details der Zuweisung aufgeführt werden. Wenn nach ein paar Sekunden die Liste immer noch nicht aktualisiert angezeigt wird, klicken Sie oben auf der Seite auf **Aktualisieren**.

1. Wählen Sie oben auf der Seite **Einstellungen** aus.

1. Beachten Sie in den Rolleneinstellungsdetails für Benutzeradministrator*innen die verschiedenen Optionen.  Beachten Sie, dass die Einstellung „Bei Aktivierung Rechtfertigung erforderlich machen“ auf „Ja“ und „Bei Aktivierung Azure MFA erforderlich machen“ ebenfalls auf „Ja“ gesetzt ist.  Sie sehen beide bei der nächsten Aufgabe, wenn Diego die Rolle aktiviert.  Beachten Sie auch, dass „Genehmigung zum Aktivieren erforderlich“ auf „Nein“ festgelegt ist.  Übernehmen Sie für alle anderen Einstellungen die Standardwerte.  Schließen Sie dieses Fenster mit dem **X** oben rechts auf der Seite des Bildschirms.

1. Melden Sie sich ab. Wählen Sie dazu das in der oberen rechten Ecke des Bildschirms neben der E-Mail-Adresse befindliche Benutzersymbol und dann **Abmelden** aus. Schließen Sie dann alle Browserfenster.

### Aufgabe 3

Bei dieser Aufgabe melden Sie sich als Diego Siciliani im Microsoft Entra Admin Center an, um auf die Privileged Identity Management-Funktion von Microsoft Entra zuzugreifen, um Ihre Zuweisung als Benutzeradministrator zu aktivieren.  Sobald sie aktiviert ist, nehmen Sie einige Konfigurationsänderungen an einem vorhandenen Benutzer vor. Hinweis: Für diese Aufgabe benötigen Sie Zugriff auf ein mobiles Gerät, das mit der Microsoft Authenticator-App verwendet werden kann.

1. Öffnen Sie Microsoft Edge.  Geben Sie **Entra.microsoft.com** in die Adressleiste des Browsers ein.

1. Melden Sie sich als Diego Siciliani an.
    1. Geben Sie **DiegoS@WWLxZZZZZZ.onmicrosoft.com** (ZZZZZZ ist hierbei die eindeutige Mandanten-ID, die von Ihrem Lab-Hostinganbieter bereitgestellt wurde) in das Anmeldefenster ein, und wählen Sie dann **Weiter** aus.
    1. Geben Sie das temporäre Kennwort ein, das Sie bei der vorherigen Aufgabe notiert haben, und wählen Sie **Anmelden** aus.  Wählen Sie **anmelden** aus.
    1. Da das von Ihnen eingegebene Kennwort nur ein temporäres Kennwort war, müssen Sie es jetzt aktualisieren. Geben Sie das aktuelle Kennwort ein, geben Sie ein neues Kennwort ein, und bestätigen Sie dann das neue Kennwort.  Notieren Sie sich dieses neue Kennwort, da Sie die Aufgabe abschließen müssen.
    1. Da Sie sich zum ersten Mal als Diego anmelden, werden Sie möglicherweise aufgefordert, MFA einzurichten. Folgen Sie den Anweisungen auf dem Bildschirm, um MFA einzurichten.
    1. Wählen Sie **Ja** aus, wenn Sie gefragt werden, ob Sie angemeldet bleiben möchten.

1. Sie sollten erfolgreich im Microsoft Entra Admin Center angemeldet sein.
1. Erweitern Sie im linken Navigationsbereich den Eintrag **ID Governance**, und wählen Sie dann **Privileged Identity Management** aus.
1. Wählen Sie im linken Navigationsbereich **Meine Rollen** aus.  Jetzt werden Informationen zu Ihren berechtigten Zuweisungen angezeigt.  Sie sehen, dass Ihnen, Diego, die Rolle „Benutzeradministrator“ zugewiesen ist.  
1. Wählen Sie in der letzten Spalte der Tabelle **Aktivieren** aus.
1. Ein angezeigtes Warnsymbol gibt an, dass eine zusätzliche Überprüfung erforderlich ist.  Klicken Sie auf **Klicken, um fortzufahren**.  Beachten Sie, dass für die PIM-Einstellungen der Rolle „Benutzeradministrator“ Multi-Faktor-Authentifizierung erforderlich ist.  Da Diegos Kontaktinformationen für die Verwendung mit MFA (Authentifizierungsmethoden) noch nicht konfiguriert wurden, muss er seine Informationen registrieren, um MFA verwenden zu können.  Obwohl er jedes Mal, wenn er sich als Benutzeradministrator anmeldet, eine MFA durchführen muss, ist der MFA-Registrierungsprozess innerhalb des Zuweisungszeitraums nur einmal erforderlich.
1. Das angezeigte Fenster und die folgenden Schritte gelten für die Microsoft Authenticator-App-Methode. .
    1. Wenn Sie die Microsoft Authenticator-App bereits auf Ihrem mobilen Gerät installiert haben, wählen Sie **Weiter**. Andernfalls wählen Sie **Jetzt herunterladen** und folgen Sie den Schritten.
    1. Sie beginnen mit dem Einrichten Ihres Kontos.  Wählen Sie **Weiter** aus.
    1. Wählen Sie auf Ihrem Mobilgerät in der Microsoft Authenticator-App die Option **+**, um ein Konto hinzuzufügen, und wählen Sie **Geschäfts- oder Schulkonto**.
    1. Wählen Sie die Option **QR-Code scannen**, und scannen Sie dann mit Ihrem mobilen Gerät den QR-Code auf dem Bildschirm Ihres PCs.
    1. Öffnen Sie die Microsoft Authenticator-App auf Ihrem mobilen Gerät und scannen Sie den QR-Code.
    1. Führen Sie die Schritte auf Ihrem PC und mobilen Gerät aus, und wählen Sie dann **Weiter** aus.
    1. Nachdem Sie Ihre Sicherheitsinformationen eingerichtet haben, wird ein Erfolgsfenster angezeigt.  Wählen Sie **Fertig** aus.

1. Sobald Sie den MFA-Registrierungsprozess abgeschlossen haben, kehren Sie zur PIM-Seite „Aktiver Benutzer-Administrator“ zurück.
1. Das Fenster „Benutzeradministrator aktivieren“ wird angezeigt.  Sie werden aufgefordert, einen Grund für die Aktivierung einzugeben.  Geben Sie in das angezeigte Feld einen beliebigen Grund ein (max. 500 Zeichen), und klicken Sie dann auf **Aktivieren**.
1. Sie sehen den Status (drei Fortschrittsphasen), während die Aktivierung verarbeitet wird.
1. Nach Abschluss der Aktivierung gelangen Sie zur Seite „Meine Rollen | Microsoft Entra ID“ zurück. Dort wird in einer Benachrichtigung angegeben, dass Sie eine Rolle aktiviert haben.  Klicken Sie auf **Hier klicken**, um Ihre aktiven Rollen anzuzeigen.  Wenn Sie feststellen, dass die Endzeit anders ist als die ursprünglich konfigurierte, klicken Sie oben auf der Seite auf das Aktualisierungssymbol (es kann einige Minuten dauern, bis die Aktualisierung erfolgt).
1. Wählen Sie im linken Navigationsbereich **Start** aus, um zur Homepage des Microsoft Entra Admin Center zurück zu gelangen. 
1. Als Microsoft Entra ID-Benutzeradmin können Sie Benutzerkonten und Gruppen erstellen, Lizenzen verwalten und mehr. Erweitern Sie in der linken Navigationsleiste **Identität** und wählen Sie **Benutzer**.
1. Wählen Sie in der Benutzerliste **Bianca Pisani** aus.
1. Wählen Sie im linken Navigationsbereich **Gruppen** aus.
1. Beachten Sie die Gruppen, denen Bianca bereits zugewiesen ist. Wählen Sie oben auf der Seite die Option **+ Mitgliedschaften** aus.
1. Wählen Sie aus der Liste der Gruppen **Mark 8-Projektteam**.
1. Wählen Sie unten auf der Seite **Auswählen**.
1. Auf der Seite „Gruppen“ stellen Sie fest, dass die Gruppe „Mark 8-Projektteam“ zur Liste hinzugefügt wurde (wenn Sie sie nicht sofort sehen, klicken Sie auf die Schaltfläche **Aktualisieren**).
1. Melden Sie sich ab. Wählen Sie dazu das in der oberen rechten Ecke des Bildschirms neben der E-Mail-Adresse befindliche Benutzersymbol und dann **Abmelden** aus. Schließen Sie dann alle Browserfenster.
1. Die Zuweisungsdauer der Rolle Benutzeradministrator ist auf die konfigurierte Zeit beschränkt.

### Überprüfung

In diesem Lab haben Sie PIM erkundet.  Als Administrator*in haben Sie Diego für eine bestimmte Zeitdauer mit Benutzeradministratorrechten konfiguriert.  Dann haben Sie als Diego den Prozess der Aktivierung der Admin-Rechte für Benutzende und die Aufnahme eines Benutzers bzw. einer Benutzerin für eine Gruppe durchlaufen.  Beachten Sie, dass für PIM die Microsoft Entra ID Premium P2-Lizenzierung erforderlich ist.
