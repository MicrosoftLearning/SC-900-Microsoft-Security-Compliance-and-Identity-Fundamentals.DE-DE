<!---
---
Lab: Titel: Erkunden con Microsoft Entra ID Benutzereinstellungen Lernpfad/Modul/Lerneinheit: Lernpfad: Beschreiben der Funktionen von Microsoft Entra; Modul 1: Beschreiben der Funktions- und Identitätstypen von Microsoft Entra ID; Lerneinheit 3: Beschreiben der Microsoft Entra Identitätstypen
---
--->

# Lab: Erkunden von Microsoft Entra ID

Dieses Lab ist den folgenden Learn-Inhalten zugeordnet:

- Lernpfad: Beschreiben der Funktionen von Microsoft Entra.
- Modul: Beschreibung der Funktion und Identitätstypen von Microsoft Entra ID.
- Lerneinheit: Beschreiben der Identitätstypen.

## Labszenario

In diesem Lab greifen Sie auf die Microsoft Entra-ID (zuvor als Azure Active Directory bezeichnet) zu.  Außerdem erstellen Sie einen Benutzer, konfigurieren die verschiedenen Einstellungen und fügen dabei auch Lizenzen hinzu.  

**Geschätzte Dauer**: 10 bis 15 Minuten

### Aufgabe 1

Als Abonnent von Microsoft 365 verwenden Sie bereits Microsoft Entra-ID (zuvor als Azure AD bezeichnet).  In dieser Aufgabe erfahren Sie, wie Sie einen neuen Benutzer in der Microsoft Entra-ID erstellen und einige Dienste erkunden, die auf Benutzerebene verwaltet werden können.

1. Schließen Sie den Microsoft Edge-Browser. Geben Sie in der Adressleits **[admin.microsoft.com](https://admin.microsoft.com)** ein und melden Sie sich mit den Administratoranmeldeinformationen für Microsoft 365 an, die von Ihrem autorisierten Labhoster (ALH) bereitgestellt wurden.
    1. Geben Sie **admin@WWLxZZZZZZ.onmicrosoft.com** (ZZZZZZ ist hierbei die eindeutige Mandanten-ID, die von Ihrem Lab-Hostinganbieter bereitgestellt wurde) in das Anmeldefenster ein, und wählen Sie dann **Weiter** aus.
    1. Geben Sie das Administratorkennwort ein, das von Ihrem Lab-Hostinganbieter bereitgestellt werden sollte. Wählen Sie **Anmelden**.
    1. Wählen Sie **Ja** aus, wenn Sie gefragt werden, ob Sie angemeldet bleiben möchten.

1. Wählen sie im Admin Center **Identität**aus (möglicherweise müssen Sie **Alle anzeigen** auswählen und dann nach unten scrollen).  Die Übersichtsseite des Microsoft Entra Admin Centers wird auf einer neuen Browserseite geöffnet. Hier sehen Sie grundlegende Informationen zu Ihrem Contoso-Mandanten. Wenn Sie im Hauptfenster nach unten scrollen, werden auch Informationen zu Warnungen, meinem Feed, Feature-Highlights und mehr angezeigt.

1. Erweitern Sie im linken Navigationsbereich **Benutzer** und wählen Sie dann **Alle Benutzer** aus. Beachten Sie, dass bereits Benutzer*innen für Ihren Mandanten konfiguriert sind.

1. Wählen Sie oben auf der Seite **+ Neuer Benutzer** aus, und wählen Sie dann im Dropdownfeld **Neuen Benutzer erstellen** aus.

1. Sie befinden sich jetzt auf der Registerkarte **Grundlagen** der Seite "Neue Benutzer erstellen". Füllen Sie die Felder wie folgt auf:
    1. Benutzerprinzipalname: **sara**.

    1. E-Mail-Spitzname: Lassen Sie die Standardeinstellung, die auf den Benutzerprinzipalnamen festgelegt ist.

    1. Anzeigename: **Sara Perez**.

    1. Kennwort: Deaktivieren Sie das Kontrollkästchen, in dem das Kennwort automatisch generiert wird, und geben Sie ein temporäres Kennwort ein, das den Kennwortanforderungen entspricht, und notieren Sie es, da Sie die nachfolgende Aufgabe ausführen müssen.

    1. Konto aktiviert: Lassen Sie das Häkchen, um sicherzustellen, dass das Konto aktiviert ist.

    1. Wählen Sie unten auf der Seite die Option **Weiter: Eigenschaften** aus.

1. Hier konfigurieren Sie einige der Felder auf der Registerkarte **Eigenschaften**.

    1. Vorname: Sara

    1. Nachname: Perez

    1. Benutzertypen: Behalten Sie die Standardeinstellung  **Mitglied**bei, beachten Sie jedoch, dass Sie in der Dropdownliste die Option zum Auswählen von Gast haben.

    1. Nutzungsort: Wählen Sie das Land/die Region aus, in dem Sie sich befinden.  Beachten Sie, dass Sie zum Feld "Verwendungsort" einen Bildlauf nach unten auf der Seite ausführen müssen, da es sich um das letzte Feld auf der Seite handelt.  **HINWEIS**: Wenn Sie dies nicht tun, können Sie in einem nachfolgenden Schritt keine Lizenz zuweisen.

    1. Wählen Sie **Weiter: Zuweisungen** aus.

1. Sie befinden sich jetzt auf der Registerkarte **Zuweisungen **auf der Sie eine Gruppenzuweisung hinzufügen und die verfügbaren Optionen zum Hinzufügen einer Rolle anzeigen.

    1. Wählen Sie **Gruppe hinzufügen** aus.

    1. Das Fenster, das geöffnet wird, zeigt alle verfügbaren Gruppen an.  

    1. HInweis auf die Liste aller verfügbaren Gruppen  Wählen Sie aus der Liste **Vorgänge** aus.  Wählen Sie unten auf der Seite die Schaltfläche **Auswählen** aus.  Es kann einige Sekunden dauern, aber die Vorgangsgruppe sollte auf der Zuweisungsseite angezeigt werden.

    1. Wählen Sie oben auf der Seite die Option **Rolle hinzufügen** aus.  Ein Fenster wird geöffnet, in dem alle verfügbaren Verzeichnisrollen angezeigt werden.  Zeigen Sie die verfügbaren Optionen an, fügen Sie jedoch keine neuen Rollen hinzu.  Schließen Sie dieses Fenster mithilfe des **X** oben rechts auf der Seite mit den Verzeichnisrollen.
    1. Klicken Sie im unteren Seitenbereich auf **Überprüfen und erstellen**. Es wird eine Zusammenfassung der Einstellungen angezeigt.  Wählen Sie am unteren Rand der Seite **Erstellen** aus.

1. Sie werden zur Seite „Benutzer“ zurückgeleitet.  Nach ein paar Sekunden wird Sara Perez aufgelistet.  Möglicherweise müssen Sie oben auf der Seite das Symbol **Aktualisieren** auswählen.

1. Wählen Sie in der Benutzerliste den soeben erstellten Benutzer (**Sara Perez**) aus.  Die Seite **Übersicht** wird angezeigt.

1. Im linken Navigationsbereich werden die verschiedenen Optionen angezeigt, die für Benutzer*innen konfiguriert werden können. Zeigen Sie die verfügbaren Optionen an.

1. Wählen Sie im linken Navigationsbereich **Lizenzen** aus.  Beachten Sie, dass für diese Person keine Lizenzzuweisungen gefunden wurden.  HINWEIS: Lizenzen können nur zugewiesen werden, wenn ein Verwendungsstandort konfiguriert wurde. Wenn Sie den Verwendungsstandort nicht festgelegt haben, fahren Sie mit diesem Schritt in der vorherigen Aufgabe fort.

    1. Wenn Sie eine Lizenz hinzufügen möchten, wählen Sie am oberen Rand des Hauptfensters **+ Aufgaben** aus.

    1. Wählen Sie unter „Lizenzen auswählen“ **Office 365 E3** und **Windows 10/11 Enterprise E3** aus. Wählen Sie anschließend unten im Bildschirm die Schaltfläche **Speichern** aus. Es sollte nun eine Benachrichtigung in der oberen rechten Ecke des Bildschirms anzeigen, dass die Lizenzzuweisungen erfolgreich waren.

    1. Wählen Sie oben rechts auf dem Bildschirm das **X** aus, um das Fenster „Lizenzzuweisungen“ zu schließen.

    1. Wählen Sie oben auf der Seite das **Symbol „Aktualisieren“** aus, um die Lizenzzuweisungen zu bestätigen.

1. Kehren Sie zum Microsoft Entra Admin Center zurück, indem Sie **Start** aus dem linken Navigationsbereich bzw. auf der oberen linken Seite des Bildschirms (dem Breadcrumb) auswählen, oberhalb von „Sara Perez | Lizenzen“.

1. Sie haben nun eine*n Benutzer*in in Microsoft Entra ID erstellt und konfiguriert.

1. Melden Sie sich von allen geöffneten Browserregisterkarten ab. Melden Sie sich ab. Wählen Sie dazu das in der oberen rechten Ecke des Bildschirms neben der E-Mail-Adresse befindliche Benutzersymbol und dann **Abmelden** aus. Schließen Sie alle Browserfenster.

### Aufgabe 2

Bei dieser Aufgabe melden Sie sich erstmals als Sara Perez an.

1. Öffnen Sie Microsoft Edge.

2. Geben Sie in der Adressleiste **https://login.microsoft.com** ein.

3. Melden Sie sich als **sara@WWLxZZZZZ.onmicrosoft.com** an (ZZZZZZ ist hierbei die eindeutige Mandanten-ID, die von Ihrem ALH (Authorized Lab Hoster) bereitgestellt wurde)
4. Geben Sie das temporäre Kennwort ein, das Sie bei der vorherigen Aufgabe festgelegt haben.

5. Sie werden nun aufgefordert, Ihr Kennwort zu aktualisieren. Geben Sie im Feld „Aktuelles Kennwort“ das temporäre Kennwort aus der vorherigen Aufgabe ein.

6. Geben Sie im Feld „Neues Kennwort“ ein neues Kennwort ein, bestätigen Sie es, und wählen Sie dann **Anmelden** aus.  Notieren Sie sich Ihr neues Kennwort – Sie benötigen es für die nachfolgende Labübung in SSPR.

7. Sie sollten nun bei Microsoft 365 angemeldet sein.

8. Melden Sie sich ab, indem Sie das Symbol in der oberen rechten Ecke des Microsoft 365-Fensters auswählen, das als Kreis mit den Buchstaben SP (neben dem Fragezeichensymbol) angezeigt wird, und dann **Abmelden** auswählen. Schließen Sie dann den Browser.

### Überprüfung

In diesem Lab haben Sie begonnen, sich mit Azure AD vertraut zu machen. Da Abonnent*innen von Microsoft 365 automatisch Azure AD verwenden, haben Sie festgestellt, dass Sie entweder über das Microsoft 365-Verwaltungsportal oder über das Azure-Portal auf Azure AD-Features und -Dienste zugreifen können.  Auf beide Arten gelangen Sie an denselben Ort.  Außerdem haben Sie den Prozess der Erstellung eines neuen Benutzers durchlaufen und die verschiedenen konfigurierbaren Einstellungen kennengelernt. Dazu zählen Gruppen, denen der Benutzer zugewiesen werden kann, die Verfügbarkeit von Rollen und die Zuweisung von Benutzerlizenzen.
