<!---
---
Lab: Erkunden des Privileged Identity Managements. Learning Path/Module/Unit: Lernpfad: Beschreiben der Funktionen von Microsoft Entra; Modul 4: Module: Beschreiben der Funktionen für Identitätsschutz und Governance von Microsoft Entra; Lerneinheit 4: Beschreiben der Funktionen von Privileged Identity Management
---
--->

# Lab: Azure Privileged Identity Management

Dieses Lab ist den folgenden Learn-Inhalten zugeordnet:

- Lernpfad: Beschreiben der Funktionen von Microsoft Entra
- Modul: Beschreiben der Identitätsschutz- und Governancefunktionen von Microsoft Entra
- Lerneinheit: Beschreiben der Funktionen von Privileged Identity Management

## Labszenario

In diesem Lab erkunden Sie einige der grundlegenden Funktionen von Privileged Identity Management (PIM). PIM erfordert Microsoft Entra-ID P2-Lizenzierung.  In diesem Lab konfigurieren Sie als Administrator durch Privileged Identity Management (PIM) einen Ihrer Benutzer, Diego Siciliani, mit einer Microsoft Entra-Benutzeradministratorrolle.   Mit den Benutzeradministratorberechtigungen kann Diego Benutzer und Gruppen erstellen, Lizenzen verwalten und mehr.  Sowohl der Administrator als auch der Benutzer Diego müssen für die Microsoft Entra ID Premium P2-Lizenzierung konfiguriert sein.

**Geschätzte Dauer**: 45-60 Minuten

### Aufgabe 1

Bei dieser Aufgabe setzen Sie als Administrator das Kennwort für den Benutzer Diego Siciliani zurück. Dieser Schritt ist erforderlich, damit Sie sich anfangs als der Benutzer in nachfolgenden Aufgaben anmelden können.

1. Öffnen Sie Microsoft Edge.  Geben Sie in der Adressleiste **https://entra.microsoft.com** ein.

1. Melden Sie sich mit den Microsoft 365-Administratoranmeldeinformationen an, die von Ihrer ALH bereitgestellt werden.
    1. Geben Sie **admin@WWLxZZZZZZ.onmicrosoft.com** (ZZZZZZ ist hierbei die eindeutige Mandanten-ID, die von Ihrem Lab-Hostinganbieter bereitgestellt wurde) in das Anmeldefenster ein, und wählen Sie dann **Weiter** aus.
    1. Geben Sie das Administratorkennwort ein, das von Ihrem Lab-Hostinganbieter bereitgestellt werden sollte. Wählen Sie **Anmelden**.
    1. Wählen Sie **Ja** aus, wenn Sie gefragt werden, ob Sie angemeldet bleiben möchten.

1. Erweitern Sie im linken Navigationsbereich **Identität**, erweitern Sie **Benutzer**, und wählen Sie dann **Alle Benutzer** aus.

1. Wählen Sie in der Benutzerliste den Eintrag **Diego Siciliani** aus.

1. Wählen Sie oben auf der Seite **Kennwort zurücksetzen** aus. Da Sie sich noch nicht als Diego angemeldet haben, kennen Sie sein Kennwort nicht. Daher müssen Sie das Kennwort zurücksetzen.

1. Wenn das Kennwortzurücksetzungsfenster geöffnet wird, wählen Sie **Kennwort zurücksetzen** aus.  WICHTIG: Notieren Sie das neue Kennwort. Sie benötigen es in einer nachfolgenden Aufgabe, um sich als der Benutzer anmelden zu können.

1. Wählen Sie im linken Navigationsbereich die Option **Startseite** aus, um zur Startseite von Microsoft Entra Admin Center zurückzukehren.

1. Lassen Sie die Browserseite geöffnet, da Sie sie in der nachfolgenden Aufgabe benötigen.

### Aufgabe 2

Bei dieser Aufgabe weisen Sie als Administrator in Privileged Identity Management Diego eine Azure AD-Rolle zu.

1. Öffnen Sie die Registerkarte Browser für die Startseite des Microsoft Entra Admin Centers.

1. Erweitern Sie im linken Navigationsbereich unter „Identität“ den Eintrag **Identitätsgovernance**, und wählen Sie dann **Privileged Identity Management** aus.

1. Sie befinden sich nun im Fenster für den Schnellstart in Privileged Identity Management. Schauen Sie sich die Informationen auf der Seite Erste Schritte erneut an. Wählen Sie **Verwalten** aus.

1. Sie befinden sich nun auf der Seite für die Contoso-Rollen.  Geben Sie oben auf der Seite in die Suchleiste den Text **Benutzer** ein.  Wählen Sie **Benutzeradministrator** aus den Suchergebnissen aus.

1. Wählen Sie oben auf der Seite **+ Zuweisung hinzufügen** aus.

1. Stellen Sie auf der Seite „Zuweisungen hinzufügen“ sicher, dass **Mitgliedschaft** unterstrichen ist.  Hier konfigurieren Sie die Mitgliedschaftseinstellungen für die Benutzeradministratorrolle in PIM.

1. Übernehmen Sie für „Bereichstyp“ den festgelegten Standardwert „Verzeichnis“.  

1. Wählen Sie unter Mitglieder auswählen die Option **Keine Mitglieder ausgewählt** aus. Dadurch wird das Fenster „Mitglied auswählen“ geöffnet.

1. Geben Sie **Diego** in die Suchleiste ein.  Wählen Sie **Diego Siciliani** aus den Suchergebnissen aus. Klicken Sie dann unten auf der Seite auf **Auswählen**.  

1. Unter „Mitglieder auswählen“ werden „1 Mitglied ausgewählt“ und der Name und die E-Mail-Adresse des ausgewählten Mitglieds, Diego Siciliani, angezeigt. Wählen Sie unten auf der Seite „Zuweisungen hinzufügen“ die Option **Weiter** aus.  

1. Sie befinden sich nun auf der Seite „Einstellung“.  Übernehmen Sie für „Zuweisungstyp“ die Standardeinstellung „Berechtigt“.

1. Wenn das Kästchen „Permanent berechtigt“ aktiviert ist, deaktivieren Sie das Häkchen für **Permanent berechtigt**.

1. Übernehmen Sie in den Feldern vom Typ „Zuweisung beginnt“ die standardmäßigen Datums- und Uhrzeitwerte, also heute und die aktuelle Uhrzeit.

1. Ändern Sie in den Feldern vom Typ „Zuweisung endet“ das Datum in das heutige Datum (beachten Sie, dass die Standardeinstellung ein Jahr von heute entfernt liegt, daher müssen Sie das Jahr ändern). Legen Sie die Uhrzeit auf zwei Stunden von der aktuellen Uhrzeit entfernt fest. Nachdem Sie die Uhrzeit festgelegt haben, zu der die Zuweisung endet, drücken Sie die TABULATORTASTE auf Ihrer Tastatur, und wählen Sie unten auf der Seite **Zuweisen** aus.  

1. Dadurch gelangen Sie zum Fenster „Zuweisungen“ zurück.  Nach ein paar Sekunden sollte Diego Siciliani in der Tabelle „Benutzeradministrator“ zusammen mit den Details der Zuweisung aufgelistet werden. Wenn die Aktualisierung nach ein paar Sekunden nicht angezeigt wird, wählen Sie oben auf der Seite **Aktualisieren** aus.

1. Wählen Sie oben auf der Seite die Option **Einstellungen** aus.

1. Beachten Sie in „Details zur Rolleneinstellung“ für „Benutzeradministrator“ die unterschiedlichen Optionen.  Beachten Sie, dass die Einstellungen „Begründung für Aktivierung erforderlich“ und „Bei Aktivierung Azure-MFA anfordern“ auf „Ja“ festgelegt sind.  Sie sehen beide bei der nächsten Aufgabe, wenn Diego die Rolle aktiviert.  Beachten Sie auch, dass „Genehmigung zum Aktivieren erforderlich“ auf „Nein“ festgelegt ist.  Übernehmen Sie für alle anderen Einstellungen die Standardwerte.  Schließen Sie die Seite. Wählen Sie dazu in der oberen rechten Ecke des Bildschirms das **X** aus.

1. Melden Sie sich ab. Wählen Sie dazu das in der oberen rechten Ecke des Bildschirms neben der E-Mail-Adresse befindliche Benutzersymbol und dann **Abmelden** aus. Schließen Sie dann alle Browserfenster.

### Aufgabe 3

Bei dieser Aufgabe melden Sie sich als Diego Siciliani im Microsoft Entra Admin Center an, um auf die Privileged Identity Management-Funktion von Microsoft Entra zuzugreifen, um Ihre Zuweisung als Benutzeradministrator zu aktivieren.  Sobald sie aktiviert ist, nehmen Sie einige Konfigurationsänderungen an einem vorhandenen Benutzer vor. Hinweis: Bei dieser Aufgabe benötigen Sie Sofortzugriff auf ein Mobilgerät, das SMS empfangen kann.

1. Öffnen Sie Microsoft Edge.  Geben Sie **Entra.microsoft.com** in die Adressleiste des Browsers ein.

1. Melden Sie sich als Diego Siciliani an.
    1. Geben Sie **DiegoS@WWLxZZZZZZ.onmicrosoft.com** (ZZZZZZ ist hierbei die eindeutige Mandanten-ID, die von Ihrem Lab-Hostinganbieter bereitgestellt wurde) in das Anmeldefenster ein, und wählen Sie dann **Weiter** aus.
    1. Geben Sie das temporäre Kennwort ein, das Sie bei der vorherigen Aufgabe notiert haben, und wählen Sie **Anmelden** aus.  Wählen Sie **Anmelden**.
    1. Da das von Ihnen eingegebene Kennwort nur ein temporäres Kennwort war, müssen Sie es jetzt aktualisieren. Geben Sie das aktuelle Kennwort ein, geben Sie ein neues Kennwort ein, und bestätigen Sie dann das neue Kennwort.  Notieren Sie sich dieses neue Kennwort, da Sie die Aufgabe abschließen müssen.
    1. Wählen Sie **Ja** aus, wenn Sie gefragt werden, ob Sie angemeldet bleiben möchten.

1. Sie sollten erfolgreich im Microsoft Entra Admin Center angemeldet sein.
1. Erweitern Sie im linken Navigationsbereich den Eintrag **Identitätsgovernance**, und wählen Sie dann **Privileged Identity Management** aus.
1. Wählen Sie im linken Navigationsbereich **Meine Rollen** aus.  Jetzt werden Informationen zu Ihren berechtigten Zuweisungen angezeigt.  Sie sehen, dass Ihnen, Diego, die Rolle „Benutzeradministrator“ zugewiesen ist.  
1. Wählen Sie in der letzten Spalte der Tabelle mit der Bezeichnung „Aktion“ den Eintrag **Aktivieren** aus.
1. Ein angezeigtes Warnsymbol gibt an, dass eine zusätzliche Überprüfung erforderlich ist.  Wählen Sie **Zum Fortfahren klicken** aus.  Beachten Sie, dass für die PIM-Einstellungen der Rolle „Benutzeradministrator“ Multi-Faktor-Authentifizierung erforderlich ist.  Da die für die MFA (Authentifizierungsmethoden) zu verwendenden Kontaktinformationen von Diego zuvor nicht konfiguriert wurden, muss er seine Informationen obendrein registrieren, um die MFA verwenden zu können.  Obwohl er die MFA immer durchlaufen muss, während er sich als Benutzeradministrator anmeldet, ist der MFA-Registrierungsprozess während des Zuweisungszeitraums nur einmal erforderlich.
1. Sie werden benachrichtigt, dass weitere Informationen erforderlich sind. Wählen Sie **Weiter** aus.
1. Geben Sie Ihr Kennwort ein.
1. Wählen Sie unten links im Microsoft Authenticator-Fenster die Option **Ich möchte eine andere Methode einrichten** aus.
1. Sie werden aufgefordert, eine andere Methode auszuwählen.  Wählen Sie neben „Authenticator-App“ die NACH-UNTEN-TASTE aus.   Wählen Sie **Telefon** und dann **Bestätigen** aus.
1. Sie werden aufgefordert, die gewünschte Telefonnummer einzugeben. Stellen Sie sicher, dass das Land für die Landeskennzahl Ihrer Telefonnummer richtig ist.  Geben Sie Ihre Telefonnummer ein. Stellen Sie sicher, dass **Code per SMS an mich senden** ausgewählt ist, und wählen Sie dann **Weiter** aus.
1. Geben Sie den 6-stelligen Code ein, den Sie auf Ihrem Telefon empfangen haben, und wählen Sie **Weiter** aus.
1. Es wird eine Benachrichtigung angezeigt, dass Ihr Telefon erfolgreich registriert wurde. Wählen Sie **Weiter** und dann **Fertig** aus.
1. Sie werden gefragt, ob Sie angemeldet bleiben möchten.  Wählen Sie **Ja** aus.
1. Das Fenster „Benutzeradministrator aktivieren“ wird angezeigt.  Sie werden aufgefordert, einen Grund für die Aktivierung einzugeben.  Geben Sie in das angezeigte Feld den gewünschten Grund (maximal 500 Zeichen) ein, und wählen Sie dann **Aktivieren** aus.
1. Sie sehen den Status (drei Fortschrittsphasen), während die Aktivierung verarbeitet wird.
1. Nach Abschluss der Aktivierung gelangen Sie zur Seite „Meine Azure AD-Rollen“ zurück. Dort wird in einer Benachrichtigung angegeben, dass Sie eine Rolle aktiviert haben.  Wählen Sie **Klicken Sie hier** aus, um Ihre aktiven Rollen anzuzeigen.  Wenn Sie feststellen, dass sich die Endzeit von der ursprünglich von Ihnen konfigurierten Zeit unterscheidet, wählen Sie oben auf der Seite den Schlüssel zum Aktualisieren (die Aktualisierung kann ein paar Minuten dauern) aus.
1. Wählen Sie im linken Navigationsbereich **Start** aus, um zur Homepage des Microsoft Entra Admin Center zurück zu gelangen. 
1. Als Azure AD-Benutzeradministrator können Sie Benutzer und Gruppen erstellen, Lizenzen verwalten und mehr. Erweitern Sie im linken Navigationsbereich **Identität**, erweitern Sie **Benutzer** und wählen Sie dann **Alle Benutzer** aus.
1. Wählen Sie in der Benutzerliste den Eintrag **Bianca Pisani** aus.
1. Wählen Sie im linken Navigationsbereich **Lizenzen** aus.
1. Beachten Sie, dass Bianca keine Lizenzen zugewiesen sind.  Wählen Sie oben auf der Seite **+ Zuweisungen** aus.
1. Wählen Sie in der Liste „Lizenzen auswählen“ die Einträge **Office 365 E3** und **Windows 10 Enterprise E3** aus.
1. Wählen Sie unten auf der Seite **Speichern** aus.  Sie werden im oberen rechten Bereich der Seite kurz benachrichtigt, dass die Lizenzen erfolgreich zugewiesen wurden.
1. Schließen Sie die Seite mit den aktualisierten Lizenzzuweisungen. Wählen Sie dazu in der oberen rechten Ecke der Seite das **X** aus.
1. Melden Sie sich ab. Wählen Sie dazu das in der oberen rechten Ecke des Bildschirms neben der E-Mail-Adresse befindliche Benutzersymbol und dann **Abmelden** aus. Schließen Sie dann alle Browserfenster.
1. Die Zuweisungsdauer der Rolle Benutzeradministrator ist auf die konfigurierte Zeit beschränkt.

### Überprüfung

In diesem Lab haben Sie PIM erkundet.  Sie als Administrator haben konfiguriert, dass Diego für einen angegebenen Zeitraum über Benutzeradministratorberechtigungen verfügt.  Anschließend sind Sie als Diego den Prozess der Aktivierung der Benutzeradministratorberechtigungen und der Konfiguration der Benutzereinstellungen durchgegangen.  Beachten Sie, dass für PIM die Azure AD Premium P2-Lizenzierung erforderlich ist.
