---
Demo:
    title: 'Bedingter Zugriff in Azure Active Directory'
    module: 'Modul 2, Lektion 3: Beschreiben der Funktionen von Identitäts- und Zugriffsverwaltungslösungen von Microsoft: Erkunden der Zugriffsverwaltungsfunktionen von Azure AD'
---


# Demo: Bedingter Zugriff in Azure Active Directory

### Demoszenario
In dieser Demo gehen Sie die verschiedenen Optionen durch, die für eine Richtlinie für bedingten Zugriff verfügbar sind.

1. Navigieren Sie zu der in Ihrem Browser geöffneten Registerkarte **Contoso – Microsoft Azure**. Falls Sie die Registerkarte geschlossen haben, öffnen Sie eine Browserseite. Geben Sie „portal.azure.com“ in die Adressleiste ein, und wählen Sie „Azure Active Directory“ aus. Sie sollten beim Azure-Portal als Administrator angemeldet sein. Falls nicht, melden Sie sich wieder an.

1. Wählen Sie im linken Navigationsbereich **Sicherheit** aus.

1. Wählen Sie im linken Navigationsbereich **Bedingter Zugriff** aus.

1. Der Bildschirm „Richtlinien für bedingten Zugriff“ wird angezeigt. Alle vorhandenen Richtlinien für bedingten Zugriff werden hier aufgelistet. Wählen Sie zum Anzeigen der Einstellungen für den bedingten Zugriff **+ Neue Richtlinie** aus.

1. Geben Sie im Feld **Name** einfachen einen Namen für die Richtlinie ein.

1. Beachten Sie, dass Ihnen unter **Zuweisungen** verschiedene Optionen zur Verfügung stehen.  Da es sich bei Richtlinien für bedingten Zugriff um Wenn-/Dann-Anweisungen handelt, sind die Einstellungen für die Zuweisungen wie „Wenn“-Anweisungen.
    1. **Benutzer und Gruppen** - Bewegen Sie den Mauszeiger über das Informationssymbol neben „Benutzer und Gruppen“. Heben Sie dann hervor, dass dies der Ort ist, an dem Sie die Benutzer und Gruppen im Verzeichnis festlegen, wofür die Richtlinie gilt. Wählen Sie **0 Benutzer und Gruppen ausgewählt**.  Nun wird die Option zum Aufnehmen oder Ausschließen von Benutzern oder Gruppen angezeigt. Wählen Sie die für die Registerkarte **Aufnehmen** verfügbaren Einstellungen aus, und heben Sie sie hervor. Wählen Sie dann die für die Registerkarte **Ausschließen** verfügbaren Einstellungen aus, und sprechen Sie darüber.
    1. **Cloud-Apps oder -aktionen** - Bewegen Sie den Mauszeiger über das Informationssymbol neben dem Text „Cloud-Apps oder -aktionen“, und heben Sie hervor, dass Sie darüber die für die Richtlinie für bedingten Zugriff verwendeten Anwendungen oder für die durch den Benutzer ausgeführten Aktionen festlegen.  Wählen Sie **Keine Cloud-Apps oder -aktionen ausgewählt** aus.
        1. Wählen Sie den Dropdownpfeil im darunterliegenden Feld **Wählen Sie aus, worauf diese Richtlinie angewendet werden soll** aus, und beachten Sie die Optionen.  Übernehmen Sie die Standardeinstellung „Cloud-Apps“.
        1. Wählen Sie die für die Registerkarte „Einschließen“ verfügbaren Einstellungen aus, und heben Sie sie hervor. Wählen Sie unter der Registerkarte **Einschließen** die Option **Apps auswählen** aus.  Beachten Sie das Fenster, das geöffnet wird, in dem Sie aus einer Liste von Anwendungen auswählen können.  Treffen Sie keine Auswahl. Schließen Sie dieses Fenster, indem Sie in der oberen rechten Ecke des Fensters das **X** auswählen. Wechseln Sie zurück, indem Sie **Keine** auswählen, um den Fehler zu entfernen.
        1. Wählen Sie dann die für die Registerkarte **Ausschließen** verfügbaren Einstellungen aus, und sprechen Sie darüber.  Hier können Sie wiederum bestimmte Apps auswählen, die ausgeschlossen werden sollen.
    1. **Bedingungen** - Bewegen Sie den Mauszeiger über das Informationssymbol neben dem Text „Bedingungen“, und heben Sie hervor, dass dies festgelegt ist, wenn die Richtlinie angewendet wird. Wählen Sie **0 Bedingungen ausgewählt** aus. Sprechen Sie über die verschiedenen aufgelisteten „Signale“.   Wählen Sie ein paar der Optionen aus. Wählen Sie dazu zunächst das Informationssymbol, um zu definieren, was es ist. Wählen Sie dann **Nicht konfiguriert** für das bestimmte Element aus, um die verschiedenen Optionen anzuzeigen.
        1. **Benutzerrisiko** - Benutzerrisiko steht für die Wahrscheinlichkeit der Kompromittierung einer bestimmten Identität oder eines bestimmten Kontos. Diese Risiken werden offline mithilfe der internen und externen Threat Intelligence-Quellen von Microsoft berechnet.
        1. **Anmelderisiko** - Ein Anmelderisiko stellt die Wahrscheinlichkeit dar, dass eine bestimmte Authentifizierungsanforderung vom Identitätsbesitzer nicht autorisiert wurde. Zu Beispielen zählen die Anmeldung über eine anonyme IP-Adresse oder ein ungewöhnlicher Ortswechsel usw.
        1. **Geräteplattform** - Plattform, über die sich der Benutzer anmeldet, zum Beispiel „iOS“.
        1. **Standort** - Standort (wird mithilfe des IP-Adressbereichs bestimmt), über den sich der Benutzer anmeldet.
        1. **Client-Apps** - Software, die der Benutzer verwendet, um auf die Cloud-App zuzugreifen, zum Beispiel „Browser“.

1. **Zugriffssteuerungen**: So wie Richtlinien für bedingten Zugriff analog zu Wenn/Dann-Anweisungen sind, sind Zugriffssteuerungen analog zur „Dann“-Anweisung.
    1. **Erteilen** - Bewegen Sie den Mauszeiger über das Informationssymbol neben „Erteilen“, um die Beschreibung anzuzeigen.  Wählen Sie **0 Steuerelemente ausgewählt** aus, um die verschiedenen Optionen anzuzeigen.  Sprechen Sie über einige davon.  Heben Sie insbesondere die unter „Zugriff gewähren“ befindliche Option **Mehrstufige Authentifizierung anfordern** hervor, und erläutern Sie, wie sie verwendet werden kann, um sehr genau zu steuern, wann die MFA erforderlich ist.   Heben Sie zudem hervor, dass Sie mehrere Steuerelemente und alle oder bloß ein paar der ausgewählten Steuerelemente als erforderlich festlegen können.
    1. **Sitzung** - Bewegen Sie den Mauszeiger über das Informationssymbol neben dem Text „Sitzung“, um die Beschreibung anzuzeigen.  Heben Sie hervor, dass „Sitzungssteuerelemente“ für eingeschränkte Interaktionsmöglichkeiten innerhalb einer Cloud-App sorgt.  Beispielsweise kann der Benutzer auf die Cloud-App zugreifen, aber Inhalte weder herunterladen noch drucken.  Dies ist ein komplexeres Thema. Halten Sie es daher einfach.

1. Nach der Konfiguration einer Richtlinie können Sie eine Richtlinie aktivieren. Wählen Sie dazu **An** aus, und klicken Sie auf die Schaltfläche **Erstellen**, um eine Richtlinie zu erstellen.

1. Wählen Sie in der oberen rechten Ecke der Seite das **X** aus, um die Richtlinie zu schließen. Wählen Sie dann oben auf der Seite auf dem blauen Balken „Microsoft Azure“ aus, um zur Startseite des Azure-Portals zurückzukehren.

1. Lassen Sie diese Browserseite für die nächste Demo geöffnet.

### Überprüfung

In dieser Demo sind Sie die verschiedenen Optionen durchgegangen, die für eine Richtlinie für bedingten Zugriff verfügbar sind.
