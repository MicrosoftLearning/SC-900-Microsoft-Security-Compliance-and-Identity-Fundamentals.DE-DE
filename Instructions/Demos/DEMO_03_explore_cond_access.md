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

## Vorführungsszenario

In dieser Demo gehen Sie die verschiedenen Optionen durch, die für eine Richtlinie für bedingten Zugriff verfügbar sind.

1. Kehren Sie zur geöffneten Browserregisterkarte mit dem Titel „Start – Microsoft Entra Admin Center“ zurück.  Wenn Sie diese Browserregisterkarte zuvor geschlossen haben, öffnen Sie Microsoft Edge, und melden Sie sich bei **[entra.microsoft.com](https://entra.microsoft.com)** mit Ihren Microsoft 365-Administratoranmeldeinformationen an.

1. Erweitern Sie im linken Navigationsbereich **Schutz** und wählen Sie dann **Bedingter Zugriff** aus.

1. Die Übersichtsseite für bedingten Zugriff wird angezeigt.  Hier sehen Sie Informationen zur Richtlinienzusammenfassung, Neuigkeiten und allgemeinen Warnungen.  Wählen Sie im linken Navigationsbereich des Fensters bedingter Zugriff die Option **Richtlinien** aus.

1. Der Bildschirm „Richtlinien für bedingten Zugriff“ wird angezeigt. Alle vorhandenen Richtlinien für bedingten Zugriff werden hier aufgelistet. Um die Einstellungen anzuzeigen, die mit bedingtem Zugriff verknüpft sind, klicken Sie auf **+ Neue Richtlinie**.

1. Geben Sie im Feld **Name** einen Namen für die Richtlinie ein.

1. Beachten Sie, dass Sie unter **Zuweisungen** mehrere Optionen haben.  Da Richtlinien für bedingten Zugriff wie if/then-Anweisungen aussehen, sind die Zuweisungseinstellungen wie die „if“-Anweisungen.
    1. **Benutzer**: Bewegen Sie den Mauszeiger über das Informationssymbol neben „Benutzer“. Erklären Sie dann, dass dies der Ort ist, an dem Sie die Identitäten, unter anderem Benutzer, Gruppen und Dienstprinzipale, im Verzeichnis festlegen, für welche die Richtlinie gelten soll. Wählen Sie **0 Benutzer*innen und Gruppen ausgewählt**.  Nun wird die Option zum Ein- oder Ausschließen von Benutzern oder Gruppen angezeigt. Wählen Sie die für die Registerkarte **Einschließen** verfügbaren Einstellungen aus, und benennen Sie sie, und sprechen Sie dann die Einstellungen an, die für die Registerkarte **Ausschließen** verfügbar sind.
    1. **Zielressourcen**: Wählen Sie **Zielressourcen** aus.  Hier können Sie den Zugriff basierend auf dem gesamten oder bestimmtem Netzwerkzugriffsdatenverkehr, Cloud-Apps oder Aktionen steuern.  Erweitern Sie das Feld unter dem Feld, in dem es heißt, wählen Sie aus, wofür diese Richtlinie gilt.  Hier können Sie auswählen, ob die Richtlinie für Cloud-Apps, Benutzeraktionen oder den Authentifizierungskontext gilt.  
        1. Wählen Sie **Cloud-Apps** aus, und wählen Sie dann auf der Registerkarte Einschließen die Option **Apps auswählen** aus, und wählen Sie dann darunter **Auswählen** und **Keine** aus. Ein Fenster wird geöffnet, um eine oder mehrere der Apps auszuwählen, für welche die Richtlinie gelten soll.
        1. Schließen Sie dieses Fenster, indem Sie in der oberen rechten Ecke des Fensters das **X** auswählen.
        1. Wenn die Zeit dies zulässt, können Sie die anderen Optionen (Benutzeraktionen und Authentifizierungskontext) durchlaufen, um die Konfigurationsoptionen für sie anzuzeigen.
    1. **Netzwerk** - zeigen Sie mit der Maus über das Informationssymbol neben der Stelle, an der "Netzwerk" steht.  Weisen Sie darauf hin, dass die Netzstandorte anhand des IP-Adressbereichs oder der GPS-Koordinaten bestimmt werden, von denen aus sich der Benutzende anmeldet.  Wählen Sie **Nicht konfiguriert** aus, um die verfügbaren Optionen zu ändern.
    1. **Bedingungen**: Bewegen Sie den Mauszeiger über das Informationssymbol neben dem Text „Bedingungen“ und heben Sie hervor, dass dies festgelegt ist, wenn die Richtlinie angewendet wird. Beispiel: ‚Speicherort. Wählen Sie **0 Bedingungen ausgewählt**. Sprechen Sie die verschiedenen aufgeführten „Signale“ an.   Wählen Sie einige der Optionen aus, indem Sie zuerst das Informationssymbol anklicken, um zu definieren, was es ist, und wählen Sie dann **Nicht konfiguriert** für das jeweilige Element aus, um die verschiedenen Optionen anzuzeigen.
        1. **Benutzerrisiko**: Benutzerrisiko steht für die Wahrscheinlichkeit der Kompromittierung einer bestimmten Identität oder eines bestimmten Kontos. Diese Risiken werden mit den internen und externen Threat Intelligence-Quellen von Microsoft in Echtzeit oder offline berechnet.
        1. **Anmelderisiko**: Ein Anmelderisiko stellt die Wahrscheinlichkeit dar, dass eine bestimmte Authentifizierungsanforderung vom Identitätsbesitzer nicht autorisiert wurde. Beispiele können die Anmeldung von einer anonymen IP-Adresse oder ungewöhnliche Ortswechsel usw. sein.
        1. **Insider-Risiko – Insider-Risiko** , das in adaptivem Schutz konfiguriert ist, bewertet das Risiko basierend auf den riskanten Datenaktivitäten eines Benutzenden.
        1. **Geräteplattform**: Plattform, über die sich der Benutzer anmeldet, Zum Beispiel: „iOS“.
        1. **Standort**: Standort (wird mithilfe des IP-Adressbereichs bestimmt), über den sich der Benutzer anmeldet.
        1. **Client-Apps**: Software, die der Benutzer verwendet, um auf die Cloud-App zuzugreifen, Beispiel: „Browser“
        1. **Filtern nach Geräten**: Beim Erstellen von Richtlinien für bedingten Zugriff können Administratoren bestimmte Geräte in ihrer Umgebung als Ziel angeben oder ausschließen. Der Administrator kann mithilfe von unterstützten Operatoren und Eigenschaften für Gerätefilter und den anderen verfügbaren Zuweisungsbedingungen in Ihren Richtlinien für bedingten Zugriff auf bestimmte Geräte abzielen.

1. **Zugriffssteuerungen** – zurück zu der Analogie, dass Richtlinien für bedingten Zugriff wie if/then-Anweisungen aussehen, sind die Zugriffssteuerungen mit der Anweisung „then“ vergleichbar.
    1. **Erteilen**: Bewegen Sie den Mauszeiger über das Informationssymbol neben „Erteilen“, um die Beschreibung anzuzeigen.  Wählen Sie **0 Steuerelemente ausgewählt**, um die verschiedenen Optionen anzuzeigen.  Sagen sie etwas über einige davon.  Heben Sie insbesondere die unter „Zugriff gewähren“ befindliche Option **Multi-Faktor-Authentifizierung anfordern** hervor, und erläutern Sie, wie sie verwendet werden kann, um sehr genau zu steuern, wann MFA erforderlich ist.   Erwähnen Sie auch, dass man mehrere Steuerelemente festlegen kann und alle oder nur eines der ausgewählten Steuerelemente benötigt.
    1. **Sitzung**: Bewegen Sie den Mauszeiger über das Informationssymbol neben „Sitzung“, um die Beschreibung anzuzeigen.  Erwähnen Sie, dass Sitzungssteuerelemente das Einschränken der Benutzeroberfläche innerhalb einer Cloud-App ermöglichen.  Beispielsweise kann der Benutzer auf die Cloud-App zugreifen, aber Inhalte weder herunterladen noch drucken.  Dies ist ein komplexeres Thema, also halten Sie es einfach.

1. Nachdem eine Richtlinie konfiguriert wurde, können Sie eine Richtlinie aktivieren, indem Sie **Ein** auswählen, dann klicken Sie auf die Schaltfläche **Erstellen**, um eine Richtlinie zu erstellen.

1. Wählen Sie das **X** in der oberen rechten Ecke der Seite aus, um die Richtlinie zu schließen.

1. Schließen Sie Ihre geöffneten Browserregisterkarten.

### Überprüfung

In dieser Demo sind Sie die verschiedenen Optionen durchgegangen, die für eine Richtlinie für bedingten Zugriff verfügbar sind.
