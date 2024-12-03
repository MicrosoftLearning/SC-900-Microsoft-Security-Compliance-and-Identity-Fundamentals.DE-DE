---
lab:
  title: Bedingter Microsoft Entra-Zugriff
  module: Describe the access management capabilities of Microsoft Entra
---

# Lab: Bedingter Zugriff mit Microsoft Entra

Dieses Lab ist den folgenden Learn-Inhalten zugeordnet:

- Lernpfad: Beschreiben der Funktionen von Microsoft Entra
- Modul: Beschreiben der Access Management-Funktionen von Microsoft Entra
- Lerneinheit: Beschreiben des bedingten Zugriffs

## Labszenario

In diesem Lab erkunden Sie MFA beim bedingten Zugriff aus Perspektive eines Administrators und eines Benutzers.  Als Administrator*in erstellen Sie eine Richtlinie, die Benutzer*innen beim Zugriff auf ein Microsoft Admin-Portal zwingt, Multi-Faktor-Authentifizierung zu durchlaufen.  Aus Benutzerperspektive sehen Sie, wie sich die Richtlinie für bedingten Zugriff auswirkt, einschließlich des Prozesses zum Registrieren für MFA.

**Geschätzte Dauer**: 30 Minuten

### Aufgabe 1

Bei dieser Aufgabe setzen Sie als Administrator das Kennwort für den Benutzer Debra Berger zurück.  Dieser Schritt ist erforderlich, damit Sie sich anfangs als der Benutzer in nachfolgenden Aufgaben anmelden können.

1. Öffnen Sie Microsoft Edge.  Geben Sie **https://entra.microsoft.com** in die Adressleiste ein und melden Sie sich mit Ihren Administratoranmeldeinformationen an.
    1. Geben Sie **admin@WWLxZZZZZZ.onmicrosoft.com** (ZZZZZZ ist hierbei die eindeutige Mandanten-ID, die von Ihrem Lab-Hostinganbieter bereitgestellt wurde) in das Anmeldefenster ein, und wählen Sie dann **Weiter** aus.
    1. Geben Sie das Administratorkennwort ein, das von Ihrem Lab-Hostinganbieter bereitgestellt werden sollte. Wählen Sie **Anmelden**.
    1. Je nach Ihrem Lab-Hoster und abhängig davon, ob Sie sich zum ersten Mal beim Mandanten anmelden, werden Sie möglicherweise aufgefordert, den MFA-Registrierungsprozess abzuschließen. Wenn ja, befolgen Sie die Anweisungen auf dem Bildschirm, um MFA einzurichten.
    1. Sobald Sie angemeldet sind, werden Sie zur Seite „Microsoft 365 Admin Center“ weitergeleitet.

1. Erweitern Sie im linken Navigationsbereich **Identität**, erweitern Sie **Benutzer**, und wählen Sie dann **Alle Benutzer** aus.

1. Wählen Sie in der Benutzerliste den Eintrag **Debra Berger** aus.

1. Wählen Sie oben auf der Seite **Kennwort zurücksetzen** aus. Da Sie sich noch nicht als Debra Berger angemeldet haben, kennen Sie ihr Kennwort nicht. Daher müssen Sie das Kennwort zurücksetzen.

1. Wenn das Kennwortzurücksetzungsfenster geöffnet wird, wählen Sie **Kennwort zurücksetzen** aus.  WICHTIG: Notieren Sie das neue Kennwort. Sie benötigen es in einer nachfolgenden Aufgabe, um sich als der Benutzer anmelden zu können.

1. Schließen Sie das Fenster zum Zurücksetzen des Kennworts, indem Sie das **X** in der oberen rechten Ecke der Seite auswählen, und schließen Sie dann das Fenster „Debra Berger“, indem Sie das **X** in der oberen rechten Ecke der Seite auswählen.

1. Wählen Sie im linken Navigationsbereich die Option **Startseite** aus, um zum Microsoft Entra Admin Center zurückzukehren.

1. Lassen Sie dieses Fenster geöffnet.

### Aufgabe 2

Bei dieser Aufgabe durchlaufen Sie den Prozess zum Erstellen einer Richtlinie für bedingten Zugriff in Microsoft Entra ID.

1. Öffnen Sie die Browserregisterkarte zur Startseite des Microsoft Entra Admin Centers.   Wenn Sie diese Browserregisterkarte zuvor geschlossen haben, öffnen Sie Microsoft Edge, und geben Sie **`https://entra.microsoft.com`** in die Adressleiste ein. Melden Sie sich dann mit Ihren Microsoft 365 Administratoranmeldeinformationen, die Sie von Ihrem ALH erhalten haben, an.

1. Erweitern Sie im linken Navigationsbereich **Schutz** und wählen Sie dann **Bedingter Zugriff** aus.

1. Die Übersichtsseite für bedingten Zugriff wird angezeigt. Wenn Sie auf der Überblickseite landen, ist die Registerkarte **Erste Schritte** ausgewählt (unterstrichen). Wählen Sie die Registerkarte **Übersicht** aus. Hier sehen Sie Kacheln mit der Richtlinienzusammenfassung und allgemeinen Warnmeldungen.  Wählen Sie im linken Navigationsbereich **Richtlinien** aus.

1. Wählen Sie im linken Navigationsbereich **Richtlinien** aus. Alle vorhandenen Richtlinien für bedingten Zugriff werden hier aufgelistet. Wählen Sie **+ Neue Richtlinie** aus.

1. Geben Sie in das Feld Name **Admin-Portale blockieren** ein.

1. Wählen Sie **0 Benutzer und Gruppen ausgewählt** unter Benutzer aus.

1. Nun wird die Option zum Ein- oder Ausschließen von Benutzern oder Gruppen angezeigt.  Stellen Sie sicher, dass **Einschließen** ausgewählt (unterstrichen) ist.

1. Wählen Sie die Option **Benutzer und Gruppen auswählen** und **Benutzer und Gruppen** aus.  Das Fenster „Benutzer und Gruppen auswählen“ wird geöffnet.  

1. Geben Sie **Debra** in die Suchleiste ein.  Wählen Sie unterhalb der Suchleiste den Eintrag **Debra Berger** aus, und klicken Sie dann unten auf der Seite auf die Schaltfläche **Auswählen**.  Beachten Sie, dass eine gängige Methode darin besteht, Benutzern in einer Gruppe die Richtlinie zuzuweisen.  Der Einfachheit halber weisen wir in diesem Lab einem bestimmten Benutzer die Richtlinie zu.

1. Wählen Sie unter Zielressourcen die Option **Keine Zielressourcen ausgewählt** aus.

1. Wählen Sie im Feld darunter **Auswählen, wofür diese Richtlinie gilt** den Pfeil nach unten aus, und notieren Sie sich die verfügbaren Optionen.  Behalten Sie die Standardeinstellung **Cloud-Apps** bei.  Stellen Sie sicher, dass die Registerkarte **Einschließen** unterstrichen ist.  Wählen Sie erst **Apps auswählen** aus und dann unterhalb, wo **Auswählen** steht, **Keine**.  Das Fenster zum Auswählen von Cloud-Apps wird geöffnet.

1. Wählen Sie **Microsoft Admin Portals**, und drücken Sie dann auf **Auswählen** unten auf der Seite.  Beachten Sie die Warnung.  

1. Wählen Sie unter „Netzwerk“ die Option **Beliebiges Netzwerk oder Standort** aus.  Überprüfen Sie die Optionen, wählen Sie jedoch keine aus.

1. Wählen Sie **0 Bedingungen ausgewählt** unter „Bedingungen“ aus.  Beachten Sie die unterschiedlichen Optionen, die von Ihnen konfiguriert werden können.  Durch die Richtlinie können Sie den Benutzerzugriff auf Basis von Signalen von Bedingungen steuern, unter anderem: Benutzerrisiko, Anmelderisiko, Geräteplattform, Speicherort, Client-Apps oder Filtern nach Geräten.  Erkunden Sie diese konfigurierbaren Optionen, aber legen Sie keine Bedingungen fest.

1. Sie legen nun die Zugriffssteuerungen fest.  Wählen Sie **0 Steuerelemente ausgewählt** unter „Erteilen“ fest.

1. Das Fenster „Erteilen“ wird geöffnet.  Wählen Sie **Zugriff blockieren** aus. Klicken Sie unten auf der Seite auf **Auswählen**.

1. Wählen Sie unten auf der Seite unter „Richtlinie aktivieren“ die Option **Ein** aus, und klicken Sie dann auf die Schaltfläche **Erstellen**.

1. Wählen Sie im linken Navigationsbereich **Richtlinien** aus. Die Richtlinie **Admin-Portale blockieren**, die Sie gerade erstellt haben, sollte in der Liste der Richtlinien für den bedingten Zugriff angezeigt werden (wählen Sie bei Bedarf das **Aktualisieren-Symbol** in der Befehlsleiste oben auf der Seite aus).

1. Melden Sie sich ab. Klicken Sie dazu auf das in der oberen rechten Ecke des Bildschirms neben der E-Mail-Adresse befindliche Benutzersymbol und dann auf **Abmelden**. Schließen Sie dann alle Browserfenster.

### Aufgabe 3

Bei dieser Aufgabe sehen Sie aus Perspektive des Benutzers Debra Berger, wie sich die Richtlinie für bedingten Zugriff auswirkt. Zunächst melden Sie sich dazu bei einer Anwendung an, die nicht in der Richtlinie für bedingten Zugriff enthalten ist (das Microsoft 365-Portal unter https://login.microsoftonline.com) ).  Anschließend wiederholen Sie den Vorgang für eine Anwendung, die in der Richtlinie für bedingten Zugriff enthalten ist (das Azure-Portal unter https://portal.azure.com) ).  Bitte beachten Sie, dass die Richtlinie den Zugriff auf alle Microsoft-Administrationsportale, einschließlich des Azure-Portals, blockiert.  HINWEIS: Aus Sicherheitsgründen müssen alle Benutzerkonten, die auf jedes Portal zugreifen, MFA verwenden.  Die MFA-Anforderung ist unabhängig von dieser Übung.

1. Öffnen Sie Microsoft Edge.  Geben Sie in der Adressleiste **https://login.microsoftonline.com** ein.
    1. Melden Sie sich als **DebraB@WWLxZZZZZZ.onmicrosoft.com** an (ZZZZZZ ist hierbei die eindeutige Mandanten-ID, die von Ihrem Labhostinganbieter bereitgestellt wurde). Wählen Sie anschließend **Weiter** aus.
    1. Geben Sie das in der vorherigen Aufgabe notierte Kennwort ein. Wählen Sie **Anmelden** aus.
    1. Da das Kennwort, das Sie als Admin beim Zurücksetzen des Kennworts erhalten, nur vorübergehend gültig ist, müssen Sie Ihr Kennwort aktualisieren. Geben Sie das aktuelle Kennwort ein, geben Sie dann ein neues Kennwort ein, und bestätigen Sie dann das neue Kennwort.  Notieren Sie sich das neue Kennwort, da Sie es zum Abschließen der Aufgabe benötigen.
    1. Da Sie sich zum ersten Mal als Debra Berger anmelden, werden Sie möglicherweise aufgefordert, MFA einzurichten. Folgen Sie den Anweisungen auf dem Bildschirm, um MFA einzurichten.
    1. Wählen Sie **Ja** aus, wenn Sie gefragt werden, ob Sie angemeldet bleiben möchten.  Sie sollten erfolgreich bei Ihrem Microsoft 365-Konto angemeldet sein.

1. Jetzt versuchen Sie, sich bei einer Anwendung anzumelden, die die Kriterien der Richtlinie für bedingten Zugriff erfüllt. Öffnen Sie eine neue Browser-Registerkarte und geben Sie **https://portal.azure.com** ein, welches das Admin-Portal für Azure ist.  Es erscheint ein Pop-up-Fenster mit der Meldung „Sie haben keinen Zugriff darauf“.  Dies ist ein Ergebnis der Richtlinie für bedingten Zugriff, die Ihren Zugriff auf alle Microsoft-Admin-Portale blockiert.

1. Melden Sie sich ab. Wählen Sie dazu das in der oberen rechten Ecke des Bildschirms neben der E-Mail-Adresse befindliche Benutzersymbol und dann „Abmelden“ aus. Schließen Sie dann alle Browserfenster.

### Überprüfung

In diesem Lab haben Sie eine Richtlinie für den bedingten Zugriff eingerichtet, die den Zugriff auf Microsoft-Admin-Portale für alle in der Richtlinie enthaltenen Benutzenden blockiert.  Als Benutzende haben Sie dann beim Zugriff auf das Azure-Portal die Auswirkungen der Richtlinie für bedingten Zugriff erlebt.
