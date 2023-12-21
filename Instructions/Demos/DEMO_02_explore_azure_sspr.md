<!---
---
Demo: Titel: „Microsoft Entra-Self-Service-Kennwortzurücksetzung (SSPR)“ Lernpfad/Modul/Lerneinheit: „Lernpfad: Beschreiben der Funktionen von Microsoft Entra; Modul 2: Beschreiben der Authentifizierungsfunktionen von Microsoft Entra ID; Lerneinheit 4: Beschreiben der Self-Service-Kennwortzurücksetzung“
---
--->

# Demo: Microsoft Entra-Self-Service-Kennwortzurücksetzung (SSPR)

Diese Demo ist den folgenden Learn-Inhalten zugeordnet:

- Lernpfad: Beschreiben der Funktionen von Microsoft Entra
- Modul: Beschreibung der Authentifizierungsfunktionen von Microsoft Entra ID
- Lerneinheit: Beschreiben der Self-Service-Kennwortzurücksetzung

## Vorführungsszenario

In dieser Demo gehen Sie die verschiedenen Einstellungen für die Aktivierung der Self-Service-Kennwortzurücksetzung durch.

1. Kehren Sie zur geöffneten Browserregisterkarte mit dem Titel „Start – Microsoft Entra Admin Center“ zurück.  Wenn Sie diese Browserregisterkarte zuvor geschlossen haben, öffnen Sie Microsoft Edge, und melden Sie sich bei **[entra.microsoft.com](https://entra.microsoft.com)** mit Ihren Microsoft 365-Administratoranmeldeinformationen an.

1. Erweitern Sie im linken Navigationsbereich die Option **Schutz**, und wählen Sie dann **Kennwortzurücksetzung** aus.

1. Die Registerkarte "Eigenschaften" ist hervorgehoben.  Beachten Sie im Eigenschaftenfenster, dass SSPR für "Keine", "Auswählen" oder "Alle" aktiviert werden kann.
    1. Bewegen Sie den Mauszeiger über das Informationssymbol neben der Stelle, an der es heißt "Passwortrücksetzung für Self-Services aktiviert", und weisen Sie darauf hin, dass Sie "Ausgewählt" wählen können, um die Passwortrücksetzung auf eine begrenzte Gruppe von Benutzer*innen zu beschränken, im Gegensatz zur Auswahl von "Keine" oder "Alle".
    1. Bewegen Sie den Mauszeiger über das Informationssymbol neben der Stelle, an der "Gruppe auswählen" steht, und weisen Sie darauf hin, dass Sie hier die Gruppe von Benutzer*innen festlegen, die ihr eigenes Kennwort zurücksetzen dürfen.   Sie müssen Benutzer*innen in die Gruppe einschließen, sie können keine einzelnen Benutzer auswählen.  Wenn Sie die Gruppe ändern, ersetzt die Gruppe, die Sie auswählen, die Gruppe, die derzeit aufgeführt ist.  Sie sollten der SSPR-Gruppe daher Benutzer hinzufügen.
    1. Beachten Sie das hellblaue Informationsfeld und weisen Sie die Lernenden darauf hin - Diese Einstellungen gelten nur für Endbenutzer in Ihrem Unternehmen. Administratoren können die Self-Service-Kennwortzurücksetzung immer durchführen und müssen zum Zurücksetzen ihres Kennworts zwei Authentifizierungsverfahren verwenden.

1. Wählen Sie im linken Navigationsbereich für Kennwortzurücksetzung "Authentifizierungsmethoden" aus.
    1. Bewegen Sie den Mauszeiger über das Informationssymbol neben der Stelle, an der "Anzahl der zum Zurücksetzen erforderlichen Methoden" steht.  Beachten Sie, dass dadurch die Anzahl der alternativen Methoden der Identifizierung festgelegt wird, die ein Benutzer in diesem Directory benötigt, um sein Kennwort zurückzusetzen.   Ändern Sie die -Einstellung nicht.
    1. Nennen Sie die verschiedenen "Methoden, die den Benutzer*innen zur Verfügung stehen", und weisen Sie darauf hin, dass SSPR Sicherheitsfragen unterstützt. Wählen Sie Sicherheitsfragen aus, um die Optionen für die Verwendung von Sicherheitsfragen anzuzeigen. Nachdem Sie die Optionen erläutert haben, wählen Sie wieder Sicherheitsfragen aus, um das Häkchen zu entfernen.

1. Wählen Sie im linken Navigationsbereich der Kennwortzurücksetzung die Option "Registrierung" aus.
    1. Bewegen Sie den Mauszeiger über das Informationssymbol neben der Stelle, an der steht: "Benutzer*innen müssen sich bei der Anmeldung registrieren".   Weisen Sie die Benutzer*innen darauf hin.  
    1. Bewegen Sie den Cursor über das Informationssymbol neben dem Text „Anzahl der Tage, bevor Benutzer aufgefordert werden, ihre Authentifizierungsinformationen erneut zu bestätigen“.   Weisen Sie die Benutzer*innen darauf hin.  

1. Wählen Sie im linken Navigationsbereich der Kennwortzurücksetzung die Option "Benachrichtigungen" aus.  Rufen Sie die beiden Einstellungen auf - Zeigen Sie mit der Maus auf das Informationssymbol für die Beschreibung.

1. Beachten Sie, dass der Navigationsbereich "Kennwortzurücksetzung" auch Optionen zum Anzeigen von Überwachungsprotokollen und Verwendung & Erkenntnisse enthält.

1. Wählen Sie oben rechts auf der Seite das "X" aus. Dadurch gelangen Sie zur Seite Standard für den Contoso-Mandanten.

1. Lassen Sie diese Browserseite für die nachfolgende Demo geöffnet.

### Überprüfung

In dieser Demo gehen Sie die verschiedenen Einstellungen für die Aktivierung der Self-Service-Kennwortzurücksetzung durch.
