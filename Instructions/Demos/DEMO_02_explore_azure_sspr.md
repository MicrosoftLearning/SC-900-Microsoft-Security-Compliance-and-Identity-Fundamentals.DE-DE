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

## Demoszenario

In dieser Demo gehen Sie die verschiedenen Einstellungen für die Aktivierung der Self-Service-Kennwortzurücksetzung durch.

1. Kehren Sie zur geöffneten Browserregisterkarte mit dem Titel „Start – Microsoft Entra Admin Center“ zurück.  Wenn Sie diese Browserregisterkarte zuvor geschlossen haben, öffnen Sie Microsoft Edge, und melden Sie sich bei **[entra.microsoft.com](https://entra.microsoft.com)** mit Ihren Microsoft 365-Administratoranmeldeinformationen an.

1. Erweitern Sie im linken Navigationsbereich die Option **Schutz**, und wählen Sie dann **Kennwortzurücksetzung** aus.

1. Die Registerkarte „Eigenschaften“ ist hervorgehoben.  Beachten Sie im Fenster „Eigenschaften“, dass SSPR für keine, ausgewählte oder alle Benutzer aktiviert werden kann.
    1. Bewegen Sie den Cursor über das Informationssymbol neben dem Text „Self-services password reset enabled“, und erklären Sie, dass die Kennwortzurücksetzung durch Auswahl von „Selected“ auf eine bestimmte Gruppe von Benutzern eingeschränkt werden kann. Weitere Optionen sind „None“ oder „All“.
    1. Bewegen Sie den Cursor über das Informationssymbol neben dem Text „Select Group“, und erklären Sie, dass hier die Gruppe von Benutzern angegeben werden kann, die ihre eigenen Kennwörter zurücksetzen dürfen.   Sie müssen Benutzer in die Gruppe aufnehmen. Es ist nicht möglich, Benutzer einzeln auszuwählen.  Wenn Sie die Gruppe ändern, ersetzt die von Ihnen ausgewählte Gruppe zudem die derzeit aufgelistete Gruppe.  Sie sollten der SSPR-Gruppe daher Benutzer hinzufügen.
    1. Beachten Sie das hellblaue Informationsfeld, und weisen Sie Kursteilnehmer darauf hin: Diese Einstellungen gelten nur für Endbenutzer in Ihrer Organisation. Administratoren können die Self-Service-Kennwortzurücksetzung immer durchführen und müssen zum Zurücksetzen ihres Kennworts zwei Authentifizierungsverfahren verwenden.

1. Wählen Sie im linken Navigationsbereich von „Kennwort zurücksetzen“ die Option Authentifizierungsmethoden aus.
    1. Bewegen Sie den Cursor über das Informationssymbol neben dem Text „Anzahl von Methoden, die zurückgesetzt werden müssen“.  Erklären Sie, dass hiermit die Anzahl der alternativen Methoden der Identifizierung festgelegt wird, über die ein Benutzer in diesem Verzeichnis verfügen muss, um sein Kennwort zurückzusetzen.   Ändern Sie die Einstellung nicht.
    1. Betonen Sie die unterschiedlichen Methoden, die für Benutzer verfügbar sind, und weisen Sie auch darauf hin, dass SSPR Sicherheitsfragen unterstützt. Wählen Sie Sicherheitsfragen aus, um die Optionen zur Verwendung von Sicherheitsfragen zu zeigen. Nachdem Sie die Optionen erläutert haben, wählen Sie wieder Sicherheitsfragen aus, um das Häkchen zu entfernen.

1. Wählen Sie im linken Navigationsbereich von „Kennwort zurücksetzen“ die Option „Registrierung“ aus.
    1. Bewegen Sie den Cursor über das Informationssymbol neben dem Text „Registrierung von Benutzern bei der Anmeldung verlangen“.   Weisen Sie die Benutzer darauf hin.  
    1. Bewegen Sie den Cursor über das Informationssymbol neben dem Text „Anzahl der Tage, bevor Benutzer aufgefordert werden, ihre Authentifizierungsinformationen erneut zu bestätigen“.   Weisen Sie die Benutzer darauf hin.  

1. Wählen Sie im linken Navigationsbereich von „Kennwort zurücksetzen“ die Option „Benachrichtigungen“ aus.  Weisen Sie auf die zwei Einstellungen hin. Bewegen Sie den Mauszeiger über das Informationssymbol für die Beschreibung.

1. Beachten Sie, dass der Navigationsbereich „Kennwort zurücksetzen“ auch Optionen zum Anzeigen der Überwachungsprotokolle und von „Nutzung & Erkenntnisse“ umfasst.

1. Wählen Sie oben rechts auf der Seite das X aus. Daraufhin wird wieder die Hauptseite für den Contoso-Mandanten angezeigt.

1. Lassen Sie diese Browserseite für die nächste Demo geöffnet.

### Überprüfung

In dieser Demo haben Sie die Einstellungen für die Self-Service-Kennwortzurücksetzung gezeigt.
