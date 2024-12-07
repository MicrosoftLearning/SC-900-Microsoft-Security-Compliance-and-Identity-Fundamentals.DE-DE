---
lab:
  title: Erkunden der Microsoft Entra ID-Benutzereinstellungen
  module: Describe the function and identity types of Microsoft Entra ID
---

# Lab: Erkunden der Microsoft Entra ID-Benutzereinstellungen

Dieses Lab ist den folgenden Learn-Inhalten zugeordnet:

- Lernpfad: Beschreiben der Funktionen von Microsoft Entra.
- Modul: Beschreibung der Funktion und Identitätstypen von Microsoft Entra ID.
- Lerneinheit: Beschreiben der Identitätstypen.

## Labszenario

In diesem Lab greifen Sie auf Microsoft Entra ID (zuvor als Azure Active Directory bezeichnet) zu.  Außerdem erstellen Sie einen Benutzer, konfigurieren die verschiedenen Einstellungen und fügen dabei auch Lizenzen hinzu.  

**Geschätzte Dauer**: 30 Minuten

### Aufgabe 1

Mit einem Abonnement von Microsoft 365 verwenden Sie bereits die Microsoft Entra ID.  In dieser Aufgabe erfahren Sie, wie Sie einen neuen Benutzer in Microsoft Entra ID erstellen und einige Dienste erkunden, die auf Benutzerebene verwaltet werden können.

1. Schließen Sie den Microsoft Edge-Browser. Geben Sie in der Adressleiste **`https://admin.microsoft.com`** ein und melden Sie sich mit den Microsoft 365-Anmeldedaten an, die Sie von Ihrem autorisierten Lab-Hoster (ALH) erhalten haben.
    1. Geben Sie **admin@WWLxZZZZZZ.onmicrosoft.com** (ZZZZZZ ist hierbei die eindeutige Mandanten-ID, die von Ihrem Lab-Hostinganbieter bereitgestellt wurde) in das Anmeldefenster ein, und wählen Sie dann **Weiter** aus.
    1. Geben Sie das Administratorkennwort ein, das von Ihrem Lab-Hostinganbieter bereitgestellt werden sollte. Wählen Sie **Anmelden**.
    1. Je nach Ihrem Lab-Hoster und abhängig davon, ob Sie sich zum ersten Mal beim Mandanten anmelden, werden Sie möglicherweise aufgefordert, den MFA-Registrierungsprozess abzuschließen. Wenn ja, befolgen Sie die Anweisungen auf dem Bildschirm, um MFA einzurichten.
    1. Sobald Sie angemeldet sind, werden Sie zur Seite „Microsoft 365 Admin Center“ weitergeleitet.

1. Wählen sie im Admin Center **Identität** aus (möglicherweise müssen Sie **Alle anzeigen** auswählen und dann nach unten scrollen).  Die Übersichtsseite des Microsoft Entra Admin Centers wird auf einer neuen Browserseite geöffnet.

1. Erweitern Sie im linken Navigationsbereich **Benutzer** und wählen Sie dann **Alle Benutzer** aus. Beachten Sie, dass für Ihren Mandanten bereits Benutzer*innen konfiguriert sind.

1. Wählen Sie oben auf der Seite **+ Neuer Benutzer** aus, und wählen Sie dann im Dropdownfeld **Neuen Benutzer erstellen** aus.

1. Sie befinden sich jetzt auf der Registerkarte **Grundlagen** der Seite „Neue Benutzer erstellen“. Füllen Sie die Felder wie folgt aus:
    1. Benutzerprinzipalname: **sara**.

    1. E-Mail-Kontoname: Lassen Sie die Standardeinstellung, die auf den Benutzerprinzipalnamen festgelegt ist.

    1. Anzeigename: **Sara Perez**.

    1. Kennwort: Deaktivieren Sie das Kontrollkästchen, das besagt, dass das Kennwort automatisch generiert wird, und geben Sie ein temporäres Kennwort ein, das den Kennwortanforderungen entspricht, und notieren Sie es, da Sie es für die Ausführung der nachfolgende Aufgabe benötigen.

    1. Konto aktiviert: Lassen Sie das Häkchen stehen, um sicherzustellen, dass das Konto aktiviert ist.

    1. Klicken Sie unten auf der Seite auf **Weiter: Eigenschaften**.

1. Hier konfigurieren Sie einige der Felder auf der Registerkarte **Eigenschaften**.

    1. Vorname: Sara

    1. Nachname: Perez

    1. Benutzertypen: Behalten Sie die Standardeinstellung  **Mitglied** bei, merken Sie jedoch an, dass man in der Dropdownliste die Option zum Auswählen von „Gast“ hat.

    1. Nutzungsort: Wählen Sie das Land/die Region aus, in dem Sie sich befinden.  Beachten Sie, dass Sie, um zum Feld „Nutzungsort“ zu gelangen, einen Bildlauf nach unten auf der Seite ausführen müssen, da es sich um das letzte Feld auf der Seite handelt.  **HINWEIS**: Wenn Sie dies nicht tun, können Sie in einem nachfolgenden Schritt keine Lizenz zuweisen.

    1. Wählen Sie **Weiter: Zuweisungen** aus.

1. Sie befinden sich jetzt auf der Registerkarte **Zuweisungen**, auf der Sie eine Gruppenzuweisung hinzufügen und die verfügbaren Optionen zum Hinzufügen einer Rolle anzeigen können.

    1. Wählen Sie **Gruppe hinzufügen** aus.

    1. Das Fenster, das geöffnet wird, zeigt alle verfügbaren Gruppen an.  

    1. Beachten Sie die Liste aller verfügbaren Gruppen.  Wählen Sie aus der Liste **Vorgänge** aus.  Klicken Sie unten auf der Seite auf die Schaltfläche **Auswählen**.  Es kann einige Sekunden dauern, aber die Vorgangsgruppe sollte auf der Zuweisungsseite angezeigt werden.

    1. Wählen Sie oben auf der Seite **+ Rolle hinzufügen**.  Ein Fenster wird geöffnet, in dem alle verfügbaren Verzeichnisrollen angezeigt werden.  Zeigen Sie die verfügbaren Optionen an, fügen Sie jedoch keine neuen Rollen hinzu.  Schließen Sie dieses Fenster mithilfe des **X** oben rechts auf der Seite mit den Verzeichnisrollen.
    1. Klicken Sie im unteren Seitenbereich auf **Überprüfen und erstellen**. Es wird eine Zusammenfassung der Einstellungen angezeigt.  Wählen Sie am unteren Rand der Seite **Erstellen** aus.

1. Sie werden zur Seite „Benutzer“ zurückgeleitet.  Nach ein paar Sekunden wird Sara Perez aufgelistet.  Möglicherweise müssen Sie oben auf der Seite auf das Symbol **Aktualisieren** klicken.

1. Wählen Sie in der Benutzerliste den soeben erstellten Benutzer (**Sara Perez**) aus.  Die Seite **Übersicht** wird angezeigt.

1. Im linken Navigationsbereich werden die verschiedenen Optionen angezeigt, die für Benutzer*innen konfiguriert werden können. Zeigen Sie die verfügbaren Optionen an.

1. Wählen Sie im linken Navigationsbereich **Lizenzen** aus.  Beachten Sie, dass für diesen Benutzer keine Lizenzzuweisungen gefunden wurden, und beachten Sie auch das Warnsymbol, das besagt: „Das Hinzufügen, Entfernen und erneute Verarbeiten von Lizenzzuweisungen ist nur im M365 Admin Center verfügbar.“  Das werden Sie in der nächsten Aufgabe tun.  HINWEIS: Lizenzen können nur zugewiesen werden, wenn ein Nutzungsort konfiguriert wurde. Wenn Sie den Verwendungsort nicht festgelegt haben, gehen Sie jetzt zu diesem Schritt zurück.

### Aufgabe 2

In dieser Aufgabe weisen Sie dem soeben erstellten Benutzenden mithilfe des Microsoft 365 Admin Centers eine Lizenz zu.

1. Öffnen Sie die Browser-Registerkarte **Home - Microsoft 365 Admin Center**.

1. Wählen Sie in der linken Navigationsleiste unter Benutzende die Option **Aktive Benutzende**.  Wählen Sie in der Liste der Benutzenden **Sara Perez**.  Es öffnet sich ein Fenster mit Informationen über die Benutzerin.  

    1. Wählen Sie die Registerkarte **Lizenzen und Apps**.
    1. Für jede der aufgeführten Lizenzen wird die Anzahl der verfügbaren Lizenzen angezeigt.  Da keine Microsoft 365 E5-Lizenzen verfügbar sind (sie wurden bereits anderen Benutzenden zugewiesen), weisen Sie die Lizenzen **Microsoft Power Apps Developer** und **Microsoft Power Automate Free** zu, indem Sie das Kontrollkästchen neben ihnen aktivieren.
    1. Klicken Sie auf **Save changes** (Änderungen speichern). Es sollte nun eine Benachrichtigung in der oberen rechten Ecke des Bildschirms angezeigt werden, dass die Lizenzzuweisungen erfolgreich waren.
    1. Schließen Sie die Seite, indem Sie auf das **X** in der oberen rechten Ecke der Seite klicken.

1. Kehren Sie zum Microsoft Entra Admin Center zurück, indem Sie **Start** aus dem linken Navigationsbereich bzw. auf der oberen linken Seite des Bildschirms (dem Breadcrumb) auswählen, oberhalb von „Sara Perez | Lizenzen“.

1. Sie haben dem Benutzenden erfolgreich Lizenzen zugewiesen.

1. Melden Sie sich von allen geöffneten Browserregisterkarten ab. Melden Sie sich ab. Klicken Sie dazu auf das in der oberen rechten Ecke des Bildschirms neben der E-Mail-Adresse befindliche Benutzersymbol und dann auf **Abmelden**. Schließen Sie alle Browserfenster.

### Aufgabe 3

Bei dieser Aufgabe melden Sie sich erstmals als Sara Perez an.

1. Öffnen Sie Microsoft Edge.

1. Geben Sie in der Adressleiste **https://login.microsoft.com** ein.

1. Melden Sie sich als **sara@WWLxZZZZZ.onmicrosoft.com** an (ZZZZZZ ist hierbei die eindeutige Mandanten-ID, die von Ihrem ALH (Authorized Lab Hoster) bereitgestellt wurde).
1. Geben Sie das temporäre Kennwort ein, das Sie bei der vorherigen Aufgabe festgelegt haben.

1. Sie werden nun aufgefordert, Ihr Kennwort zu ändern. Geben Sie im Feld „Aktuelles Kennwort“ das temporäre Kennwort aus der vorherigen Aufgabe ein.

1. Geben Sie im Feld „Neues Kennwort“ ein neues Kennwort ein, bestätigen Sie es, und klicken Sie dann auf **Anmelden**.  Notieren Sie sich Ihr neues Kennwort – Sie benötigen es für die nachfolgende Lab-Übung zu SSPR.

1. Da Sie sich zum ersten Mal als Sara Perez anmelden, werden Sie möglicherweise aufgefordert, MFA einzurichten. Folgen Sie den Anweisungen auf dem Bildschirm, um MFA einzurichten.

1. Sie sollten nun erfolgreich bei Saras Microsoft-Konto angemeldet sein.  Beachten Sie, dass die Lizenzierung von Sara, die Sie in der vorherigen Aufgabe zugewiesen haben, nur auf der Microsoft Power Automate-Gratislizenz und Power Apps für Entwickler beschränkt war und keine E5-Lizenzierung umfasste.

1. Melden Sie sich ab, indem Sie das Symbol in der oberen rechten Ecke des Microsoft 365-Fensters auswählen, das als Kreis mit den Buchstaben SP (neben dem Fragezeichensymbol) angezeigt wird, und dann **Abmelden** auswählen. Schließen Sie dann den Browser.

### Überprüfung

In diesem Lab haben Sie damit begonnen, Microsoft Entra ID zu erkunden. Da Abonnenten von Microsoft 365 automatisch auch Microsoft Entra ID verwenden, haben Sie festgestellt, dass Sie über das Microsoft 365-Verwaltungsportal oder das Azure-Portal auf Funktionen und Dienste von Microsoft Entra ID zugreifen können.  Auf beide Arten gelangen Sie an denselben Ort.  Außerdem haben Sie den Prozess der Erstellung eines neuen Benutzers durchlaufen und die verschiedenen konfigurierbaren Einstellungen kennengelernt. Dazu zählen Gruppen, denen der Benutzer zugewiesen werden kann, die Verfügbarkeit von Rollen und die Zuweisung von Benutzerlizenzen.
