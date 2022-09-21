---
ms.openlocfilehash: 5d7767e0187f043004b0c9d17e7cd1d1915613cc
ms.sourcegitcommit: 15658ca1c7bae8a4dbaa33ab6f897070bde521b9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/12/2022
ms.locfileid: "147892160"
---
<a name="---"></a><!---
---
Lab: 'Lernpfad: Beschreiben der Funktionen von Azure Active Directory (Azure AD), Teil von Microsoft Entra; Modul: Beschreiben der Zugriffsverwaltungsfunktionen von Azure AD; Lerneinheit: Erklären des bedingten Zugriffs in Azure AD'
---
--->

# <a name="lab-explore-access-management-in-azure-ad-with-conditional"></a>Lab: Erkunden der Zugriffsverwaltung in Azure AD mit bedingtem Zugriff

Dieses Lab ist den folgenden Learn-Inhalten zugeordnet:

- Lernpfad: Beschreiben der Funktionen von Azure Active Directory (Azure AD), Teil von Microsoft Entra
- Modul: Beschreiben der Zugriffsverwaltungsfunktionen von Azure AD
- Lerneinheit: Beschreiben des bedingten Zugriffs in Azure AD

## <a name="lab-scenario"></a>Labszenario

In diesem Lab erkunden Sie die MFA beim bedingten Zugriff aus Perspektive eines Administrators und eines Benutzers.  Als Administrator erstellen Sie eine Richtlinie, die den Benutzer beim Zugriff auf eine cloudbasierte Microsoft Azure-Verwaltungsanwendung zwingt, die mehrstufige Authentifizierung zu durchlaufen.  Aus Benutzerperspektive sehen Sie, wie sich die Richtlinie für bedingten Zugriff auswirkt, einschließlich des Prozesses zum Registrieren für die MFA.

**Geschätzte Dauer**: 10–15 Minuten

### <a name="task-1"></a>Aufgabe 1

Bei dieser Aufgabe setzen Sie als Administrator das Kennwort für den Benutzer Debra Berger zurück.  Dieser Schritt ist erforderlich, damit Sie sich anfangs als der Benutzer in nachfolgenden Aufgaben anmelden können.

1. Öffnen Sie Microsoft Edge.  Geben Sie **portal.azure.com** in die Adressleiste ein.

2. Melden Sie sich mit Ihren Administratoranmeldeinformationen an.
    1. Geben Sie **admin@WWLxZZZZZZ.onmicrosoft.com** (ZZZZZZ ist hierbei die eindeutige Mandanten-ID, die von Ihrem Labhostinganbieter bereitgestellt wurde) in das Fenster „Anmelden“ ein, und wählen Sie dann **Weiter** aus.
    1. Geben Sie das Administratorkennwort ein, das Sie vom Labhostinganbieter erhalten haben sollten. Wählen Sie **Anmelden**.
    1. Wählen Sie **Ja** aus, wenn Sie gefragt werden, ob Sie angemeldet bleiben möchten.

3. Wählen Sie in der oberen linken Ecke des Bildschirms neben dem Text „Microsoft Azure“ das Symbol „Portalmenü anzeigen“ (die drei horizontalen Linien werden auch als Hamburgersymbol bezeichnet) und dann im linken Navigationsbereich unter „Favoriten“ Azure Active Directory aus. Wenn die Option nicht unter „Favoriten“ aufgeführt ist, geben Sie Azure Active Directory im Suchfeld ein. Wählen Sie anschließend aus der Ergebnisliste **Azure Active Directory** aus.

4. Wählen Sie im linken Navigationsbereich **Benutzer** aus.

5. Wählen Sie in der Benutzerliste den Eintrag **Debra Berger** aus.

6. Wählen Sie oben auf der Seite **Kennwort zurücksetzen** aus. Da Sie sich noch nicht als Debra Berger angemeldet haben, kennen Sie ihr Kennwort nicht. Daher müssen Sie das Kennwort zurücksetzen.

7. Wenn das Kennwortzurücksetzungsfenster geöffnet wird, wählen Sie **Kennwort zurücksetzen** aus.  WICHTIG: Notieren Sie das neue Kennwort. Sie benötigen es in einer nachfolgenden Aufgabe, um sich als der Benutzer anmelden zu können.

8. Schließen Sie das Kennwortzurücksetzungsfenster. Wählen Sie dazu in der oberen rechten Ecke der Seite das **X** aus.

9. Schließen Sie das Fenster „Benutzer“. Wählen Sie dazu in der oberen rechten Ecke der Seite das **X** aus.

10. Lassen Sie dieses Fenster geöffnet.

### <a name="task-2"></a>Aufgabe 2

Bei dieser Aufgabe gehen Sie den Prozess zum Erstellen einer Richtlinie für bedingten Zugriff Azure AD durch.

1. Öffnen Sie die Browserregisterkarte mit der Bezeichnung „Contoso – Microsoft Azure“.   Wenn Sie die Browserregisterkarte geschlossen haben, öffnen Sie Microsoft Edge, und geben Sie in die Adressleiste „portal.azure.com“ ein. Melden Sie sich mit Ihren Administratoranmeldeinformationen an, und wählen Sie dann „Azure Active Directory“ aus.  

2. Wählen Sie im linken Navigationsbereich **Sicherheit** aus.

3. Wählen Sie im linken Navigationsbereich **Bedingter Zugriff** aus.

4. Der Bildschirm „Richtlinien für bedingten Zugriff“ wird angezeigt. Alle vorhandenen Richtlinien für bedingten Zugriff werden hier aufgelistet. Wählen Sie **Neue Richtlinie** aus.

5. Geben Sie **MFA-Testrichtlinie** in das Feld „Name“ ein.

6. Wählen Sie **0 Benutzer und Gruppen ausgewählt** unter „Benutzer und Gruppen“ aus.

7. Nun wird die Option zum Aufnehmen oder Ausschließen von Benutzern oder Gruppen angezeigt.  Stellen Sie sicher, dass **Einschließen** ausgewählt (unterstrichen) ist.

8. Wählen Sie die Option **Benutzer und Gruppen auswählen** und **Benutzer und Gruppen** aus.  Das Fenster „Benutzer und Gruppen auswählen“ wird geöffnet.  

9. Geben Sie **Debra** in die Suchleiste ein.  Wählen Sie unterhalb der Suchleiste den Eintrag **Debra Berger** aus, und klicken Sie dann unten auf der Seite auf die Schaltfläche **Auswählen**.  Beachten Sie, dass eine gängige Methode darin besteht, Benutzern in einer Gruppe die Richtlinie zuzuweisen.  Der Einfachheit halber weisen wir in diesem Lab einem bestimmten Benutzer die Richtlinie zu.

10. Wählen Sie **Keine Cloud-Apps oder -aktionen ausgewählt** unter „Cloud-Apps oder -aktionen“ aus.

11. Nun wird die Option zum Einschließen oder Ausschließen von Cloud-Apps oder Benutzeraktionen angezeigt.  Stellen Sie sicher, dass **Cloud-Apps** hervorgehoben und **Einschließen** ausgewählt (unterstrichen) ist. Wählen Sie dann **Apps auswählen** aus.  Das Fenster zum Auswählen von Cloud-Apps wird geöffnet.

12. Geben Sie **Azure** in die Suchleiste ein.  Wählen Sie aus den unterhalb des Suchfelds angezeigten Suchergebnissen den Eintrag **Microsoft Azure-Verwaltung** aus. Klicken Sie dann unten auf der Seite auf **Auswählen**.  Beachten Sie die Warnung.  

13. Wählen Sie **0 Bedingungen ausgewählt** unter „Bedingungen“ aus.  Beachten Sie die unterschiedlichen Optionen, die von Ihnen konfiguriert werden können.  Durch die Richtlinie können Sie den Benutzerzugriff auf Basis von Signalen von Bedingungen steuern. Dazu zählen beispielsweise das Risiko, die Geräteplattform, der Standort, die Client-Apps oder der Gerätezustand.  So können Sie beispielsweise eine Bedingung für die Richtlinie aufnehmen, die mit Ausnahme von ausgewählten oder vertrauenswürdigen Standorten, wie etwa das Netzwerk Ihres Hauptsitzes, für jeden Standort gilt.  Legen Sie für diese Richtlinie keine Bedingung fest.

14. Sie legen nun die Zugriffssteuerungen fest.  Wählen Sie **0 Steuerelemente ausgewählt** unter „Erteilen“ fest.

15. Das Fenster „Erteilen“ wird geöffnet.  Stellen Sie sicher, dass **Zugriff gewähren** ausgewählt ist. Wählen Sie dann **Mehrstufige Authentifizierung anfordern** aus.  Übernehmen Sie unter dem Abschnitt „Für mehrere Steuerelemente“ die Standardeinstellung **Alle ausgewählten Steuerungen anfordern**.  Klicken Sie unten auf der Seite auf **Auswählen**.

16. Wählen Sie unten auf der Seite unter „Richtlinie aktivieren“ die Option **An** aus, und klicken Sie dann auf die Schaltfläche **Erstellen**.

17. Nach ein paar Sekunden sollte die Richtlinie für den MFA-Pilotversuch in der Liste der Richtlinien für bedingten Zugriff (wählen Sie bei Bedarf oben auf der Seite **Aktualisieren** aus) angezeigt werden.

18. Melden Sie sich von Azure ab, und schließen Sie die Browserfenster.

### <a name="task-3"></a>Aufgabe 3

Bei dieser Aufgabe sehen Sie aus Perspektive des Benutzers Debra Berger, wie sich die Richtlinie für bedingten Zugriff auswirkt. Zunächst melden Sie sich dazu bei einer Anwendung an, die in der Richtlinie für bedingten Zugriff nicht enthalten ist.  Anschließend wiederholen Sie den Prozess für eine Anwendung, die in der Richtlinie für bedingten Zugriff enthalten ist.  Beachten Sie, dass der Benutzer entsprechend der Richtlinie die MFA durchlaufen muss, wenn er auf eine Microsoft Azure-Verwaltungsanwendung zugreift.  Damit der Benutzer die MFA verwenden kann, muss er zunächst die für die MFA zu verwendende Authentifizierungsmethode registrieren, beispielsweise ein an ein Mobilgerät gesendeter Code oder eine Authenticator-Anwendung.

1. Öffnen Sie Microsoft Edge.  Geben Sie **login.microsoftonline.com/** in die Adressleiste des Browsers ein.

1. Melden Sie sich als Debra Berger an.
    1. Geben Sie **DebraB@WWLxZZZZZZ.onmicrosoft.com** (ZZZZZZ ist hierbei die eindeutige Mandanten-ID, die von Ihrem Labhostinganbieter bereitgestellt wurde) in das Fenster „Anmelden“ ein, und wählen Sie dann **Weiter** aus.
    1. Geben Sie das in der vorherigen Aufgabe notierte Kennwort ein. Wählen Sie **Anmelden**.
    1. Da das Kennwort temporär ist, dass bereitgestellt wurde, als Sie das Kennwort als Administrator zurückgesetzt haben, müssen Sie Ihr Kennwort (kein Bestandteil der MFA) aktualisieren.  Geben Sie das aktuelle Kennwort ein. Geben Sie dann in die Felder „Neues Kennwort“ und „Kennwort bestätigen“ das Kennwort **SC900-Lab** ein.
    1. Wählen Sie **Ja** aus, wenn Sie gefragt werden, ob Sie angemeldet bleiben möchten.

1. Sie sollten erfolgreich bei Ihrem Microsoft 365-Konto angemeldet sein.  Die MFA war für diese Anwendung nicht erforderlich, da sie nicht zur Richtlinie gehört.

1. Nun versuchen Sie, sich bei einer Anwendung anzumelden, welche die Kriterien für die MFA erfüllt.  Öffnen Sie Microsoft Edge, und geben Sie **portal.azure.com** in die Adressleiste ein.

1. In einer Warnung wird angezeigt, dass weitere Informationen erforderlich sind.  Klicken Sie auf **Weiter**.  Beachten Sie, dass dadurch der MFA-Registrierungsprozess initiiert wird, da Sie hiermit erstmals auf die Cloud-App zugreifen, die in der Richtlinie für bedingten Zugriff identifiziert wurde.  Dieser Registrierungsprozess ist nur einmal erforderlich.   Alternativ zur Registrierung durch den Benutzer kann der Administrator die zu verwendende Authentifizierungsmethode konfigurieren.

1. Im Fenster „Schützen Sie Ihr Konto“ können Sie die für die MFA zu verwendende Methode auswählen.  „Microsoft Authenticator“ ist eine Option davon. Der Zweckmäßigkeit halber wählen Sie in dieser Lab-Übung eine andere Methode aus.  Wählen Sie **Ich möchte eine andere Methode einrichten** aus.  Wählen Sie im Popupfenster „Andere Methode auswählen“ den **Dropdownpfeil** aus. Wählen Sie **Telefon** und dann **Bestätigen** aus.

1. Stellen Sie im Fenster, das geöffnet wird, sicher, dass Ihr Land ausgewählt ist. Geben Sie dann die gewünschte Mobiltelefonnummer ein, und stellen Sie sicher, dass **Code per SMS an mich senden** ausgewählt ist. Klicken Sie dann auf **Weiter**.  Auf dem Bildschirm wird „Die SMS wurde verifiziert. Ihr Telefon wurde erfolgreich registriert“ angezeigt.  Klicken Sie auf **Weiter**. Klicken Sie danach auf **Fertig**.  Dadurch wird der einmalige Registrierungsprozess abgeschlossen.

1. Wahrscheinlich wird in einer Meldung angezeigt, dass bei Ihrer Anmeldung eine Zeitüberschreitung aufgetreten ist.  Geben Sie einfach das Kennwort **SC900-Lab** ein, und wählen Sie **Anmelden** aus.

1. Es wird ein Fenster angezeigt, in dem Sie aufgefordert werden, den an Ihr Telefon gesendeten Code einzugeben.  Geben Sie den Code ein, und wählen Sie **Next** (Weiter) aus.  Diese Erfahrung machen Sie entsprechend der MFA-Richtlinie als der Benutzer Gerhart jedes Mal, wenn Sie auf eine Cloudanwendung für die Microsoft Azure-Verwaltung zugreifen, wie etwa auf das Azure-Portal.

1. Es wird ein Fenster angezeigt, in dem Sie aufgefordert werden, den an Ihr Telefon gesendeten Code einzugeben.  Geben Sie den Code ein, und wählen Sie die Schaltfläche **Bestätigen** aus.  Wählen Sie **Nein** aus, wenn Sie gefragt werden, ob Sie angemeldet bleiben möchten.

1. Sie sollten nun auf das Azure-Portal zugreifen können.  Das Azure-Portal ist eine Microsoft Azure-Verwaltungsanwendung und erfordert entsprechend der erstellten Richtlinie für bedingten Zugriff die mehrstufige Authentifizierung.  

1. Melden Sie sich ab. Wählen Sie dazu das in der oberen rechten Ecke des Bildschirms neben der E-Mail-Adresse befindliche Benutzersymbol und dann Abmelden aus. Schließen Sie dann alle Browserfenster.

### <a name="review"></a>Überprüfung

In diesem Lab sind Sie den Prozess zum Einrichten einer Richtlinie für bedingten Zugriff durchgegangen, die Benutzer beim Zugriff auf die Cloudanwendung für die Microsoft Azure-Verwaltung zwingt, die MFA zu durchlaufen.  Anschließend sind Sie den Registrierungsprozess für die MFA als ein Benutzer durchgegangen und haben die Auswirkung der Richtlinie für bedingten Zugriff gesehen, die Sie beim Zugriff auf das Azure-Portal zwang, die MFA zu verwenden.
