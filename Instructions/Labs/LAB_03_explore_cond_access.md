<!---
---
Lab: Lernpfad: Beschreiben der Funktionen von Microsoft Entra; Modul: Beschreiben der Zugriffsverwaltungsfunktionen von Microsoft Entra ID; Lerneinheit: Erklären des bedingten Zugriffs
---
--->

# Lab: Bedingter Zugriff mit Microsoft Entra

Dieses Lab ist den folgenden Learn-Inhalten zugeordnet:

- Lernpfad: Beschreiben der Funktionen von Microsoft Entra
- Modul: Beschreiben der Funktionen für die Zugriffsverwaltung in Microsoft Entra ID
- Lerneinheit: Beschreiben des bedingten Zugriffs

## Labszenario

In diesem Lab erkunden Sie MFA beim bedingten Zugriff aus Perspektive eines Administrators und eines Benutzers.  Als Administrator erstellen Sie eine Richtlinie, die Benutzer*innen beim Zugriff auf eine cloudbasierte Microsoft Admin Portale zwingt, Multi-Faktor-Authentifizierung zu durchlaufen.  Aus Benutzerperspektive sehen Sie, wie sich die Richtlinie für bedingten Zugriff auswirkt, einschließlich des Prozesses zum Registrieren für MFA.

**Geschätzte Dauer**: 30 Minuten

### Aufgabe 1

Bei dieser Aufgabe setzen Sie als Administrator das Kennwort für den Benutzer Debra Berger zurück.  Dieser Schritt ist erforderlich, damit Sie sich anfangs als der Benutzer in nachfolgenden Aufgaben anmelden können.

1. Öffnen Sie Microsoft Edge.  Geben Sie **https://entra.microsoft.com** in die Adressleiste ein und melden Sie sich mit Ihren Administratoranmeldeinformationen an.
    1. Geben Sie **admin@WWLxZZZZZZ.onmicrosoft.com** (ZZZZZZ ist hierbei die eindeutige Mandanten-ID, die von Ihrem Lab-Hostinganbieter bereitgestellt wurde) in das Anmeldefenster ein, und wählen Sie dann **Weiter** aus.
    1. Geben Sie das Administratorkennwort ein, das von Ihrem Lab-Hostinganbieter bereitgestellt werden sollte. Wählen Sie **Anmelden**.
    1. Wählen Sie **Ja** aus, wenn Sie gefragt werden, ob Sie angemeldet bleiben möchten.

1. Erweitern Sie im linken Navigationsbereich **Identität**, erweitern Sie **Benutzer**, und wählen Sie dann **Alle Benutzer** aus.

1. Wählen Sie in der Benutzerliste den Eintrag **Debra Berger** aus.

1. Wählen Sie oben auf der Seite **Kennwort zurücksetzen** aus. Da Sie sich noch nicht als Debra Berger angemeldet haben, kennen Sie ihr Kennwort nicht. Daher müssen Sie das Kennwort zurücksetzen.

1. Wenn das Kennwortzurücksetzungsfenster geöffnet wird, wählen Sie **Kennwort zurücksetzen** aus.  WICHTIG: Notieren Sie das neue Kennwort. Sie benötigen es in einer nachfolgenden Aufgabe, um sich als der Benutzer anmelden zu können.

1. Schließen Sie das Fenster zum Zurücksetzen des Kennworts, indem Sie das **X** in der oberen rechten Ecke der Seite auswählen, und schließen Sie dann das Fenster „Debra Berger“, indem Sie das **X** in der oberen rechten Ecke der Seite auswählen.

1. Wählen Sie im linken Navigationsbereich die Option **Startseite** aus, um zum Microsoft Entra Admin Center zurückzukehren.

1. Lassen Sie dieses Fenster geöffnet.

### Aufgabe 2

Bei dieser Aufgabe durchlaufen Sie den Prozess zum Erstellen einer Richtlinie für bedingten Zugriff in Azure AD.

1. Öffnen Sie die Browserregisterkarte zur Startseite des Microsoft Entra Admin Centers.   Wenn Sie diese Browserregisterkarte zuvor geschlossen haben, öffnen Sie Microsoft Edge, und geben Sie **https://entra.microsoft.com** in die Adressleiste ein. Melden Sie sich dann mit Ihren Microsoft 365 Administratoranmeldeinformationen, die Sie von Ihrem ALH erhalten haben, an.

1. Erweitern Sie im linken Navigationsbereich **Schutz** und wählen Sie dann **Bedingter Zugriff** aus.

1. Die Übersichtsseite für bedingten Zugriff wird angezeigt.  Hier sehen Sie Kacheln mit der Richtlinienzusammenfassung und allgemeinen Warnungen.  Wählen Sie im linken Navigationsbereich **Richtlinien** aus.

1. Wählen Sie im linken Navigationsbereich **Richtlinien** aus. Alle vorhandenen Richtlinien für bedingten Zugriff werden hier aufgelistet. Wählen Sie **+ Neue Richtlinie** aus.

1. Geben Sie **MFA-Testrichtlinie** in das Feld „Name“ ein.

1. Wählen Sie **0 Benutzer und Gruppen ausgewählt** unter Benutzer aus.

1. Nun wird die Option zum Ein- oder Ausschließen von Benutzern oder Gruppen angezeigt.  Stellen Sie sicher, dass **Einschließen** ausgewählt (unterstrichen) ist.

1. Wählen Sie die Option **Benutzer und Gruppen auswählen** und **Benutzer und Gruppen** aus.  Das Fenster „Benutzer und Gruppen auswählen“ wird geöffnet.  

1. Geben Sie **Debra** in die Suchleiste ein.  Wählen Sie unterhalb der Suchleiste den Eintrag **Debra Berger** aus, und klicken Sie dann unten auf der Seite auf die Schaltfläche **Auswählen**.  Beachten Sie, dass eine gängige Methode darin besteht, Benutzern in einer Gruppe die Richtlinie zuzuweisen.  Der Einfachheit halber weisen wir in diesem Lab einem bestimmten Benutzer die Richtlinie zu.

1. Wählen Sie unter Zielressourcen die Option **Keine Zielressourcen ausgewählt** aus.

1. Wählen Sie im Feld darunter **Auswählen, wofür diese Richtlinie gilt** den Pfeil nach unten aus, und notieren Sie sich die verfügbaren Optionen.  Behalten Sie die Standardeinstellung **Cloud-Apps** bei.  Stellen Sie sicher, dass die Registerkarte **Einschließen** unterstrichen ist.  Wählen Sie erst **Apps auswählen** aus und dann unterhalb, wo **Auswählen** steht, **Keine**.  Das Fenster zum Auswählen von Cloud-Apps wird geöffnet.

1. Geben Sie **Azure** in die Suchleiste ein.  Wählen Sie aus den unterhalb des Suchfelds angezeigten Suchergebnissen **Microsoft Ademin Portale** aus. Klicken Sie dann unten auf der Seite auf **Auswählen**.  Beachten Sie die Warnung.  

1. Wählen Sie **0 Bedingungen ausgewählt** unter „Bedingungen“ aus.  Beachten Sie die unterschiedlichen Optionen, die von Ihnen konfiguriert werden können.  Durch die Richtlinie können Sie den Benutzerzugriff auf Basis von Signalen von Bedingungen steuern, unter anderem: Benutzerrisiko, Anmelderisiko, Geräteplattform, Speicherort, Client-Apps oder Filtern nach Geräten.  Erkunden Sie diese konfigurierbaren Optionen, aber legen Sie keine Bedingungen fest.

1. Sie legen nun die Zugriffssteuerungen fest.  Wählen Sie **0 Steuerelemente ausgewählt** unter „Erteilen“ fest.

1. Das Fenster „Erteilen“ wird geöffnet.  Stellen Sie sicher, dass **Zugriff gewähren** ausgewählt ist. Wählen Sie dann **Multi-Faktor-Authentifizierung erfordern** aus. Scrollen Sie im rechten Fenster ein wenig nach unten, und behalten Sie im Abschnitt „Für mehrere Steuerelemente“ die Standardeinstellung **Alle ausgewählten Steuerelemente erfordern** bei.  Klicken Sie unten auf der Seite auf **Auswählen**.

1. Wählen Sie unten auf der Seite unter „Richtlinie aktivieren“ die Option **Ein** aus, und klicken Sie dann auf die Schaltfläche **Erstellen**.

1. Wählen Sie im linken Navigationsbereich **Richtlinien** aus. Die Richtlinie für den MFA-Pilotversuch sollte in der Liste der Richtlinien für bedingten Zugriff angezeigt werden (wählen Sie bei Bedarf oben auf der Seite **Aktualisieren** aus).

1. Melden Sie sich ab. Wählen Sie dazu das in der oberen rechten Ecke des Bildschirms neben der E-Mail-Adresse befindliche Benutzersymbol und dann **Abmelden** aus. Schließen Sie dann alle Browserfenster.

### Aufgabe 3

Bei dieser Aufgabe sehen Sie aus Perspektive des Benutzers Debra Berger, wie sich die Richtlinie für bedingten Zugriff auswirkt. Zunächst melden Sie sich dazu bei einer Anwendung an, die nicht in der Richtlinie für bedingten Zugriff enthalten ist (das Microsoft 365-Portal unter https://login.microsoftonline.com) ).  Anschließend wiederholen Sie den Vorgang für eine Anwendung, die in der Richtlinie für bedingten Zugriff enthalten ist (das Azure-Portal unter https://portal.azure.com) ).  Denken Sie daran, dass die Richtlinie erfordert, dass der Benutzer MFA durchlaufen muss, wenn er auf eines der Microsoft Admin Portals zugreift, einschließlich des Azure-Portals.  Damit der Benutzer die MFA verwenden kann, muss er zunächst die für die MFA zu verwendende Authentifizierungsmethode registrieren, beispielsweise ein an ein Mobilgerät gesendeter Code oder eine Authenticator-Anwendung.

1. Öffnen Sie Microsoft Edge.  Geben Sie in der Adressleiste **https://login.microsoftonline.com** ein.
    1. Melden Sie sich als **DebraB@WWLxZZZZZZ.onmicrosoft.com** an (ZZZZZZ ist hierbei die eindeutige Mandanten-ID, die von Ihrem Labhostinganbieter bereitgestellt wurde). Wählen Sie anschließend **Weiter** aus.
    1. Geben Sie das in der vorherigen Aufgabe notierte Kennwort ein. Wählen Sie **Anmelden**.
    1. Da das Kennwort temporär ist, dass bereitgestellt wurde, als Sie das Kennwort als Administrator zurückgesetzt haben, müssen Sie Ihr Kennwort (kein Bestandteil der MFA-Richtlinie) aktualisieren. Geben Sie das aktuelle Kennwort ein, geben Sie dann ein neues Kennwort ein, und bestätigen Sie dann das neue Kennwort.  Notieren Sie sich das neue Kennwort, da Sie es zum Abschließen der Aufgabe benötigen.
    1. Wählen Sie **Ja** aus, wenn Sie gefragt werden, ob Sie angemeldet bleiben möchten.  Sie sollten erfolgreich bei Ihrem Microsoft 365-Konto angemeldet sein. Die MFA war für diese Anwendung nicht erforderlich, da sie nicht zur Richtlinie gehört.

1. Nun versuchen Sie, sich bei einer Anwendung anzumelden, welche die Kriterien für MFA erfüllt. Öffnen Sie eine neue Browserregisterkarte und geben Sie **https://portal.azure.com** ein.

1. In einem Fenster wird angezeigt, dass weitere Informationen erforderlich sind.  Wählen Sie **Weiter** aus.  Beachten Sie, dass dadurch der MFA-Registrierungsprozess initiiert wird, da Sie hiermit erstmals auf die Cloud-App zugreifen, die in der Richtlinie für bedingten Zugriff identifiziert wurde.  Dieser Registrierungsprozess ist nur einmal erforderlich.   Alternativ zur Registrierung durch den Benutzer kann der Administrator die zu verwendende Authentifizierungsmethode konfigurieren.

1. Im Fenster „Schützen Sie Ihr Konto“ können Sie die für die MFA zu verwendende Methode auswählen.  „Microsoft Authenticator“ ist eine Option davon. Der Zweckmäßigkeit halber wählen Sie in dieser Lab-Übung eine andere Methode aus.  Wählen Sie **Ich möchte eine andere Methode einrichten** aus.  Wählen Sie im Popupfenster „Andere Methode auswählen“ den **Dropdownpfeil** aus. Wählen Sie **Telefon** und dann **Bestätigen** aus.

1. Stellen Sie im Fenster, das geöffnet wird, sicher, dass Ihr Land ausgewählt ist. Geben Sie dann die gewünschte Mobiltelefonnummer ein.  Stellen Sie sicher, dass **Code per SMS an mich senden** ausgewählt ist. Klicken Sie dann auf **Weiter**.  Sie erhalten eine SMS auf Ihrem Telefon mit einem Code, den Sie eingeben müssen, wenn die Aufforderung zum Eingeben von Code angezeigt wird.  Geben Sie den erhaltenen Code ein, und klicken Sie dann auf **Weiter**.  Nach der Bestätigung wird Folgendes auf dem Bildschirm angezeigt: „Die SMS wurde verifiziert. Ihr Telefon wurde erfolgreich registriert.“  Klicken Sie auf **Weiter**. Klicken Sie danach auf **Fertig**.  Dadurch wird der einmalige Registrierungsprozess abgeschlossen.

1. Sie sollten nun auf das Azure-Portal zugreifen können.  Das Azure-Portal ist ein Microsoft Admin Portal und erfordert entsprechend der erstellten Richtlinie für bedingten Zugriff die mehrstufige Authentifizierung.  
    1. Wenn in einer Meldung angezeigt wird, dass bei Ihrer Anmeldung eine Zeitüberschreitung aufgetreten ist, geben Sie das Kennwort ein und wählen dann **Anmelden** aus.
    1. Es wird ein Fenster angezeigt, in dem Sie Ihre Identität verifizieren müssen.  Wählen Sie =X XXXXXXX aus, um einen Code auf Ihrem Mobiltelefon zu erhalten. Geben Sie den Code ein, und wählen Sie **Überprüfen** aus.
    1. Wenn Sie gefragt werden, ob Sie angemeldet bleiben möchten, wählen Sie **Nein** aus.

1. Melden Sie sich ab. Wählen Sie dazu das in der oberen rechten Ecke des Bildschirms neben der E-Mail-Adresse befindliche Benutzersymbol und dann „Abmelden“ aus. Schließen Sie dann alle Browserfenster.

### Überprüfung

In diesem Lab haben Sie den Prozess zum Einrichten einer Richtlinie für bedingten Zugriff durchlaufen, die Benutzer beim Zugriff auf die Cloudanwendung für das Microsoft Admin Portal zwingt, MFA zu durchlaufen.  Anschließend sind Sie den Registrierungsprozess für die MFA als ein Benutzer durchgegangen und haben die Auswirkung der Richtlinie für bedingten Zugriff gesehen, die Sie beim Zugriff auf das Azure-Portal zwang, die MFA zu verwenden.
