---
lab:
  title: 'Beschreiben der Zugriffsverwaltungsfunktionen von Azure AD'
  module: 'Modul: Beschreiben der Zugriffsverwaltungsfunktionen von Azure AD'
---


# <a name="lab-explore-access-management-in-azure-ad-with-conditional-access"></a>Lab: Erkunden der Zugriffsverwaltung in Azure AD mit bedingtem Zugriff

Dieses Lab ist den folgenden Learn-Inhalten zugeordnet:

- Lernpfad: Beschreiben der Funktionen von Azure Active Directory (Azure AD), Teil von Microsoft Entra
- Modul: Beschreiben der Zugriffsverwaltungsfunktionen von Azure AD
- Lerneinheit: Beschreiben des bedingten Zugriffs in Azure AD

## <a name="lab-scenario"></a>Labszenario

In diesem Lab erkunden Sie MFA beim bedingten Zugriff aus Perspektive eines Administrators und eines Benutzers.  Als Administrator erstellen Sie eine Richtlinie, die Benutzer beim Zugriff auf eine cloudbasierte Microsoft Azure-Verwaltungsanwendung zwingt, Multi-Faktor-Authentifizierung zu durchlaufen.  Aus Benutzerperspektive sehen Sie, wie sich die Richtlinie für bedingten Zugriff auswirkt, einschließlich des Prozesses zum Registrieren für MFA.

**Geschätzte Dauer**: 30 Minuten

### <a name="task-1"></a>Aufgabe 1

Bei dieser Aufgabe setzen Sie als Administrator das Kennwort für den Benutzer Debra Berger zurück.  Dieser Schritt ist erforderlich, damit Sie sich anfangs als der Benutzer in nachfolgenden Aufgaben anmelden können.

1. Öffnen Sie Microsoft Edge.  Geben Sie **portal.azure.com** in die Adressleiste ein.

2. Melden Sie sich mit Ihren Administratoranmeldeinformationen an.
    1. Geben Sie **admin@WWLxZZZZZZ.onmicrosoft.com** (ZZZZZZ ist hierbei die eindeutige Mandanten-ID, die von Ihrem Lab-Hostinganbieter bereitgestellt wurde) in das Anmeldefenster ein, und wählen Sie dann **Weiter** aus.
    1. Geben Sie das Administratorkennwort ein, das von Ihrem Lab-Hostinganbieter bereitgestellt werden sollte. Wählen Sie **Anmelden**.
    1. Wählen Sie **Ja** aus, wenn Sie gefragt werden, ob Sie angemeldet bleiben möchten.

3. Wählen Sie in der oberen linken Ecke des Bildschirms neben dem Text „Microsoft Azure“ das Symbol „Portalmenü anzeigen“ (die drei horizontalen Linien werden auch als Hamburgersymbol bezeichnet) und dann im linken Navigationsbereich unter „Favoriten“ Azure Active Directory aus. Wenn die Option nicht unter „Favoriten“ aufgeführt ist, geben Sie Azure Active Directory im Suchfeld ein. Wählen Sie anschließend aus der Ergebnisliste **Azure Active Directory** aus.

4. Wählen Sie im linken Navigationsbereich **Benutzer** aus.

5. Wählen Sie in der Benutzerliste den Eintrag **Debra Berger** aus.

6. Wählen Sie oben auf der Seite **Kennwort zurücksetzen** aus. Da Sie sich noch nicht als Debra Berger angemeldet haben, kennen Sie ihr Kennwort nicht. Daher müssen Sie das Kennwort zurücksetzen.

7. Wenn das Kennwortzurücksetzungsfenster geöffnet wird, wählen Sie **Kennwort zurücksetzen** aus.  WICHTIG: Notieren Sie das neue Kennwort. Sie benötigen es in einer nachfolgenden Aufgabe, um sich als der Benutzer anmelden zu können.

8. Schließen Sie das Fenster zum Zurücksetzen des Kennworts, indem Sie das **X** in der oberen rechten Ecke der Seite auswählen, und schließen Sie dann das Fenster „Debra Berger“, indem Sie das **X** in der oberen rechten Ecke der Seite auswählen.

9. Schließen Sie das Fenster „Benutzer“. Wählen Sie dazu in der oberen rechten Ecke der Seite das **X** aus.

10. Sie kehren jetzt wieder zur Seite **Contoso-| Übersicht** zurück.  Lassen Sie dieses Fenster geöffnet.

### <a name="task-2"></a>Aufgabe 2

Bei dieser Aufgabe durchlaufen Sie den Prozess zum Erstellen einer Richtlinie für bedingten Zugriff in Azure AD.

1. Öffnen Sie die Browserregisterkarte mit der Bezeichnung „Contoso – Microsoft Azure“.   Wenn Sie die Browserregisterkarte geschlossen haben, öffnen Sie Microsoft Edge, und geben Sie in die Adressleiste „portal.azure.com“ ein. Melden Sie sich mit Ihren Administratoranmeldeinformationen an, und wählen Sie dann „Azure Active Directory“ aus.  

2. Wählen Sie im linken Navigationsbereich **Sicherheit** aus.

3. Wählen Sie im linken Navigationsbereich **Bedingter Zugriff** aus.

4. Der Bildschirm „Richtlinien für bedingten Zugriff“ wird angezeigt. Alle vorhandenen Richtlinien für bedingten Zugriff werden hier aufgelistet. Wählen Sie **+ Neue Richtlinie** aus.

5. Geben Sie **MFA-Testrichtlinie** in das Feld „Name“ ein.

6. Wählen Sie unter „Benutzer- oder Workloadidentitäten“ die Option **0 Benutzer- oder Workloadidentitäten ausgewählt** aus.

7. Nun wird die Option zum Ein- oder Ausschließen von Benutzern oder Gruppen angezeigt.  Stellen Sie sicher, dass **Einschließen** ausgewählt (unterstrichen) ist.

8. Wählen Sie die Option **Benutzer und Gruppen auswählen** und **Benutzer und Gruppen** aus.  Das Fenster „Benutzer und Gruppen auswählen“ wird geöffnet.  

9. Geben Sie **Debra** in die Suchleiste ein.  Wählen Sie unterhalb der Suchleiste den Eintrag **Debra Berger** aus, und klicken Sie dann unten auf der Seite auf die Schaltfläche **Auswählen**.  Beachten Sie, dass eine gängige Methode darin besteht, Benutzern in einer Gruppe die Richtlinie zuzuweisen.  Der Einfachheit halber weisen wir in diesem Lab einem bestimmten Benutzer die Richtlinie zu.

10. Wählen Sie unter „Cloud-Apps oder Aktionen“ die Option **Keine Cloud-Apps, Aktionen oder authentifizierten Kontexte ausgewählt** aus.

11. Nun wird die Option zum Ein- oder Ausschließen von Cloud-Apps oder Benutzeraktionen angezeigt.  Stellen Sie sicher, dass **Cloud-Apps** im Feld „Auswählen, für was diese Richtlinie gilt“ aufgeführt wird.  Falls noch nicht aufgeführt, wählen Sie diese Option in der Dropdownliste aus. Stellen Sie sicher, dass **Einschließen** ausgewählt (unterstrichen) ist, wählen Sie dann **Apps auswählen** aus, und wählen Sie anschließend unter „Auswählen“ die Option **Keine** aus.  Das Fenster zum Auswählen von Cloud-Apps wird geöffnet.

12. Geben Sie **Azure** in die Suchleiste ein.  Wählen Sie aus den unterhalb des Suchfelds angezeigten Suchergebnissen den Eintrag **Microsoft Azure-Verwaltung** aus. Klicken Sie dann unten auf der Seite auf **Auswählen**.  Beachten Sie die Warnung.  

13. Wählen Sie **0 Bedingungen ausgewählt** unter „Bedingungen“ aus.  Beachten Sie die unterschiedlichen Optionen, die von Ihnen konfiguriert werden können.  Durch die Richtlinie können Sie den Benutzerzugriff auf Basis von Signalen von Bedingungen steuern. Dazu zählen beispielsweise das Risiko, die Geräteplattform, der Standort, die Client-Apps oder der Gerätezustand.  So können Sie beispielsweise eine Bedingung für die Richtlinie aufnehmen, die mit Ausnahme von ausgewählten oder vertrauenswürdigen Standorten, wie etwa das Netzwerk Ihres Hauptsitzes, für jeden Standort gilt.  Legen Sie für diese Richtlinie keine Bedingung fest.

14. Sie legen nun die Zugriffssteuerungen fest.  Wählen Sie **0 Steuerelemente ausgewählt** unter „Erteilen“ fest.

15. Das Fenster „Erteilen“ wird geöffnet.  Stellen Sie sicher, dass **Zugriff gewähren** ausgewählt ist. Wählen Sie dann **Multi-Faktor-Authentifizierung erfordern** aus. Scrollen Sie im rechten Fenster ein wenig nach unten, und behalten Sie im Abschnitt „Für mehrere Steuerelemente“ die Standardeinstellung **Alle ausgewählten Steuerelemente erfordern** bei.  Klicken Sie unten auf der Seite auf **Auswählen**.

16. Wählen Sie unten auf der Seite unter „Richtlinie aktivieren“ die Option **Ein** aus, und klicken Sie dann auf die Schaltfläche **Erstellen**.

17. Nach ein paar Sekunden sollte die Richtlinie für den MFA-Pilotversuch in der Liste der Richtlinien für bedingten Zugriff (wählen Sie bei Bedarf oben auf der Seite **Aktualisieren** aus) angezeigt werden.

18. Melden Sie sich von Azure ab, und schließen Sie die Browserfenster.

### <a name="task-3"></a>Aufgabe 3

Bei dieser Aufgabe sehen Sie aus Perspektive des Benutzers Debra Berger, wie sich die Richtlinie für bedingten Zugriff auswirkt. Zunächst melden Sie sich dazu bei einer Anwendung an, die nicht in der Richtlinie für bedingten Zugriff enthalten ist (das Microsoft 365-Portal unter login.microsoftonline.com).  Anschließend wiederholen Sie den Vorgang für eine Anwendung, die in der Richtlinie für bedingten Zugriff enthalten ist (das Azure-Portal unter portal.azure.com).  Beachten Sie, dass der Benutzer entsprechend der Richtlinie die MFA durchlaufen muss, wenn er auf eine Microsoft Azure-Verwaltungsanwendung zugreift.  Damit der Benutzer die MFA verwenden kann, muss er zunächst die für die MFA zu verwendende Authentifizierungsmethode registrieren, beispielsweise ein an ein Mobilgerät gesendeter Code oder eine Authenticator-Anwendung.

1. Öffnen Sie Microsoft Edge.  Geben Sie **login.microsoftonline.com** in die Adressleiste ein.
    1. Melden Sie sich als **DebraB@WWLxZZZZZZ.onmicrosoft.com** an (ZZZZZZ ist hierbei die eindeutige Mandanten-ID, die von Ihrem Labhostinganbieter bereitgestellt wurde). Wählen Sie anschließend **Weiter** aus.
    1. Geben Sie das in der vorherigen Aufgabe notierte Kennwort ein. Wählen Sie **Anmelden**.
    1. Da das Kennwort temporär ist, dass bereitgestellt wurde, als Sie das Kennwort als Administrator zurückgesetzt haben, müssen Sie Ihr Kennwort (kein Bestandteil der MFA-Richtlinie) aktualisieren. Geben Sie das aktuelle Kennwort ein, geben Sie für das neue Kennwort **SC900-Lab** ein, und geben Sie dann erneut **SC900** ein, um das Kennwort zu bestätigen.
    1. Wählen Sie **Ja** aus, wenn Sie gefragt werden, ob Sie angemeldet bleiben möchten.  Sie sollten erfolgreich bei Ihrem Microsoft 365-Konto angemeldet sein. Die MFA war für diese Anwendung nicht erforderlich, da sie nicht zur Richtlinie gehört.

1. Nun versuchen Sie, sich bei einer Anwendung anzumelden, welche die Kriterien für MFA erfüllt. Öffnen Sie im Browser eine neue Registerkarte, und geben Sie **portal.azure.com** ein.

1. In einem Fenster wird angezeigt, dass weitere Informationen erforderlich sind.  Wählen Sie **Weiter** aus.  Beachten Sie, dass dadurch der MFA-Registrierungsprozess initiiert wird, da Sie hiermit erstmals auf die Cloud-App zugreifen, die in der Richtlinie für bedingten Zugriff identifiziert wurde.  Dieser Registrierungsprozess ist nur einmal erforderlich.   Alternativ zur Registrierung durch den Benutzer kann der Administrator die zu verwendende Authentifizierungsmethode konfigurieren.

1. Im Fenster „Schützen Sie Ihr Konto“ können Sie die für die MFA zu verwendende Methode auswählen.  „Microsoft Authenticator“ ist eine Option davon. Der Zweckmäßigkeit halber wählen Sie in dieser Lab-Übung eine andere Methode aus.  Wählen Sie **Ich möchte eine andere Methode einrichten** aus.  Wählen Sie im Popupfenster „Andere Methode auswählen“ den **Dropdownpfeil** aus. Wählen Sie **Telefon** und dann **Bestätigen** aus.

1. Stellen Sie im Fenster, das geöffnet wird, sicher, dass Ihr Land ausgewählt ist. Geben Sie dann die gewünschte Mobiltelefonnummer ein.  Stellen Sie sicher, dass **Code per SMS an mich senden** ausgewählt ist. Klicken Sie dann auf **Weiter**.  Sie erhalten eine SMS auf Ihrem Telefon mit einem Code, den Sie eingeben müssen, wenn die Aufforderung zum Eingeben von Code angezeigt wird.  Geben Sie den erhaltenen Code ein, und klicken Sie dann auf **Weiter**.  Nach der Bestätigung wird Folgendes auf dem Bildschirm angezeigt: „Die SMS wurde verifiziert. Ihr Telefon wurde erfolgreich registriert.“  Klicken Sie auf **Weiter**. Klicken Sie danach auf **Fertig**.  Dadurch wird der einmalige Registrierungsprozess abgeschlossen.

1. Sie sollten nun auf das Azure-Portal zugreifen können.  Das Azure-Portal ist eine Microsoft Azure-Verwaltungsanwendung und erfordert entsprechend der erstellten Richtlinie für bedingten Zugriff die mehrstufige Authentifizierung.  
    1. Wenn in einer Meldung angezeigt wird, dass bei Ihrer Anmeldung eine Zeitüberschreitung aufgetreten ist, geben Sie das Kennwort **SC900-Lab** ein und wählen dann **Anmelden** aus. 
    1. Es wird ein Fenster angezeigt, in dem Sie Ihre Identität verifizieren müssen.  Wählen Sie =X XXXXXXX aus, um einen Code auf Ihrem Mobiltelefon zu erhalten. Geben Sie den Code ein, und wählen Sie **Überprüfen** aus.
    1. Wenn Sie gefragt werden, ob Sie angemeldet bleiben möchten, wählen Sie **Nein** aus.

1. Melden Sie sich ab. Wählen Sie dazu das in der oberen rechten Ecke des Bildschirms neben der E-Mail-Adresse befindliche Benutzersymbol und dann „Abmelden“ aus. Schließen Sie dann alle Browserfenster.

### <a name="review"></a>Überprüfung

In diesem Lab haben Sie den Prozess zum Einrichten einer Richtlinie für bedingten Zugriff durchlaufen, die Benutzer beim Zugriff auf die Cloudanwendung für die Microsoft Azure-Verwaltung zwingt, MFA zu durchlaufen.  Anschließend sind Sie den Registrierungsprozess für die MFA als ein Benutzer durchgegangen und haben die Auswirkung der Richtlinie für bedingten Zugriff gesehen, die Sie beim Zugriff auf das Azure-Portal zwang, die MFA zu verwenden.
