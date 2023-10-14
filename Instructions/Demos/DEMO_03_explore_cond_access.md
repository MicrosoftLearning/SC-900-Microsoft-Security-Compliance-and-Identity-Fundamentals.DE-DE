<!---
---
Demo: Title: Bedingter Zugriff in Azure AD Learning Path/Module/Unit: Lernpfad: Beschreiben der Funktionen von Microsoft Entra; Modul 3: Beschreiben der Zugriffsverwaltungsfunktionen von Microsoft Entra ID; Lerneinheit 2: Erklären des bedingten Zugriffs
---
--->

# Demo: Bedingter Zugriff mit Microsoft Entra

Diese Demo ist den folgenden Learn-Inhalten zugeordnet:

- Lernpfad: Beschreiben der Funktionen von Microsoft Entra
- Modul: Beschreiben der Funktionen für die Zugriffsverwaltung in Microsoft Entra ID
- Lerneinheit: Beschreiben des bedingten Zugriffs

## Demoszenario

In dieser Demo gehen Sie die verschiedenen Optionen durch, die für eine Richtlinie für bedingten Zugriff verfügbar sind.

1. Kehren Sie zur geöffneten Browserregisterkarte mit dem Titel „Home-Microsoft Entra Admin Center“ zurück.  Wenn Sie diese Browserregisterkarte zuvor geschlossen haben, öffnen Sie Microsoft Edge, und melden Sie sich bei **[entra.microsoft.com](https://entra.microsoft.com)** mit Ihren Microsoft 365-Administratoranmeldeinformationen an.

1. Erweitern Sie im linken Navigationsbereich **Schutz** und wählen Sie dann **Bedingter Zugriff** aus.

1. Die Übersichtsseite für bedingten Zugriff wird angezeigt.  Hier sehen Sie Kacheln mit der Richtlinienzusammenfassung und allgemeinen Warnungen.  Wählen Sie im linken Navigationsbereich **Richtlinien** aus.

1. Der Bildschirm „Richtlinien für bedingten Zugriff“ wird angezeigt. Alle vorhandenen Richtlinien für bedingten Zugriff werden hier aufgelistet. Wählen Sie zum Anzeigen der Einstellungen für den bedingten Zugriff **+ Neue Richtlinie** aus.

1. Geben Sie im Feld **Name** einen Namen für die Richtlinie ein.

1. Beachten Sie, dass Ihnen unter **Zuweisungen** verschiedene Optionen zur Verfügung stehen.  Da es sich bei Richtlinien für bedingten Zugriff um Wenn-/Dann-Anweisungen handelt, sind die Einstellungen für die Zuweisungen wie „Wenn“-Anweisungen.
    1. **Benutzer**: Bewegen Sie den Mauszeiger über das Informationssymbol neben „Benutzer“. Erklären Sie dann, dass dies der Ort ist, an dem Sie die Identitäten, unter anderem Benutzer, Gruppen und Dienstprinzipale, im Verzeichnis festlegen, für welche die Richtlinie gelten soll. Wählen Sie **0 Benutzer und Gruppen ausgewählt**.  Nun wird die Option zum Ein- oder Ausschließen von Benutzern oder Gruppen angezeigt. Wählen Sie die für die Registerkarte **Aufnehmen** verfügbaren Einstellungen aus, und heben Sie sie hervor. Wählen Sie dann die für die Registerkarte **Ausschließen** verfügbaren Einstellungen aus, und sprechen Sie darüber.
    1. **Zielressourcen**: Wählen Sie **Zielressourcen** aus.  Hier können Sie den Zugriff basierend auf dem gesamten oder bestimmtem Netzwerkzugriffsdatenverkehr, Cloud-Apps oder Aktionen steuern.  Erweitern Sie das Feld unter dem Feld, in dem es heißt, wählen Sie aus, wofür diese Richtlinie gilt.  Hier können Sie auswählen, ob die Richtlinie für Cloud-Apps, Benutzeraktionen oder den Authentifizierungskontext gilt.  
        1. Wählen Sie **Cloud-Apps** aus, und wählen Sie dann auf der Registerkarte Einschließen die Option **Apps auswählen** aus, und wählen Sie dann darunter **Auswählen** und **Keine** aus. Ein Fenster wird geöffnet, um eine oder mehrere der Apps auszuwählen, für welche die Richtlinie gelten soll.
        1. Schließen Sie dieses Fenster, indem Sie in der oberen rechten Ecke des Fensters das **X** auswählen.
        1. Wenn die Zeit dies zulässt, können Sie die anderen Optionen (Benutzeraktionen und Authentifizierungskontext) durchlaufen, um die Konfigurationsoptionen für sie anzuzeigen.
    1. **Bedingungen**: Bewegen Sie den Mauszeiger über das Informationssymbol neben dem Text „Bedingungen“ und heben Sie hervor, dass dies festgelegt ist, wenn die Richtlinie angewendet wird. Beispiel: ‚Speicherort. Wählen Sie **0 Bedingungen ausgewählt** aus. Sprechen Sie über die verschiedenen aufgelisteten „Signale“.   Wählen Sie ein paar der Optionen aus. Wählen Sie dazu zunächst das Informationssymbol, um zu definieren, was es ist. Wählen Sie dann **Nicht konfiguriert** für das bestimmte Element aus, um die verschiedenen Optionen anzuzeigen.
        1. **Benutzerrisiko**: Benutzerrisiko steht für die Wahrscheinlichkeit der Kompromittierung einer bestimmten Identität oder eines bestimmten Kontos. Diese Risiken werden mit den internen und externen Threat Intelligence-Quellen von Microsoft in Echtzeit oder offline berechnet.
        1. **Anmelderisiko**: Ein Anmelderisiko stellt die Wahrscheinlichkeit dar, dass eine bestimmte Authentifizierungsanforderung vom Identitätsbesitzer nicht autorisiert wurde. Zu Beispielen zählen die Anmeldung über eine anonyme IP-Adresse oder ein ungewöhnlicher Ortswechsel usw.
        1. **Geräteplattform**: Plattform, über die sich der Benutzer anmeldet, zum Beispiel „iOS“.
        1. **Standort**: Standort (wird mithilfe des IP-Adressbereichs bestimmt), über den sich der Benutzer anmeldet.
        1. **Client-Apps**: Software, die der Benutzer verwendet, um auf die Cloud-App zuzugreifen, zum Beispiel „Browser“.
        1. **Filtern nach Geräten**: Beim Erstellen von Richtlinien für bedingten Zugriff können Administratoren bestimmte Geräte in ihrer Umgebung als Ziel angeben oder ausschließen. Der Administrator kann mithilfe von unterstützten Operatoren und Eigenschaften für Gerätefilter und den anderen verfügbaren Zuweisungsbedingungen in Ihren Richtlinien für bedingten Zugriff auf bestimmte Geräte abzielen.

1. **Zugriffssteuerungen**: So wie Richtlinien für bedingten Zugriff analog zu Wenn/Dann-Anweisungen sind, sind Zugriffssteuerungen analog zur „Dann“-Anweisung.
    1. **Erteilen**: Bewegen Sie den Mauszeiger über das Informationssymbol neben „Erteilen“, um die Beschreibung anzuzeigen.  Wählen Sie **0 Steuerelemente ausgewählt** aus, um die verschiedenen Optionen anzuzeigen.  Sprechen Sie über einige davon.  Heben Sie insbesondere die unter „Zugriff gewähren“ befindliche Option **Multi-Faktor-Authentifizierung anfordern** hervor, und erläutern Sie, wie sie verwendet werden kann, um sehr genau zu steuern, wann MFA erforderlich ist.   Heben Sie zudem hervor, dass Sie mehrere Steuerelemente und alle oder bloß ein paar der ausgewählten Steuerelemente als erforderlich festlegen können.
    1. **Sitzung**: Bewegen Sie den Mauszeiger über das Informationssymbol neben „Sitzung“, um die Beschreibung anzuzeigen.  Heben Sie hervor, dass „Sitzungssteuerelemente“ für eingeschränkte Interaktionsmöglichkeiten innerhalb einer Cloud-App sorgt.  Beispielsweise kann der Benutzer auf die Cloud-App zugreifen, aber Inhalte weder herunterladen noch drucken.  Dies ist ein komplexeres Thema. Halten Sie es daher einfach.

1. Nach der Konfiguration einer Richtlinie können Sie eine Richtlinie aktivieren. Wählen Sie dazu **An** aus, und klicken Sie auf die Schaltfläche **Erstellen**, um eine Richtlinie zu erstellen.

1. Wählen Sie das **X** in der oberen rechten Ecke der Seite aus, um die Richtlinie zu schließen.

1. Schließen Sie Ihre geöffneten Browserregisterkarten.

### Überprüfung

In dieser Demo sind Sie die verschiedenen Optionen durchgegangen, die für eine Richtlinie für bedingten Zugriff verfügbar sind.
