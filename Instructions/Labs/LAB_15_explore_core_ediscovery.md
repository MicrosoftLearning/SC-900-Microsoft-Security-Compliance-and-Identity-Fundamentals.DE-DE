---
lab:
  title: eDiscovery (Standard)-Workflow erkunden
  module: Describe the eDiscovery and audit capabilities of Microsoft Purview
---

# Lab: eDiscovery (Standard)-Workflow erkunden

Dieses Lab ist den folgenden Learn-Inhalten zugeordnet:

- Lernpfad: Beschreiben der Funktionen der Microsoft-Compliancelösungen
- Modul: eDiscovery-Funktionen und Überwachungsfunktionen von Microsoft Purview
- Lerneinheit: Beschreiben der eDiscovery-Lösungen in Microsoft Purview

## Labszenario

In diesem Lab gehen Sie die Schritte durch, die zum Festlegen von eDiscovery erforderlich sind, darunter Einrichten von Rollenberechtigungen, Erstellen eines eDiscovery-Falls, Erstellen einer eDiscovery-Aufbewahrung und Erstellen einer Suchabfrage.  Hinweis: Die Lizenzierung für eDiscovery (Standard) erfordert das entsprechende Organisationsabonnement und die Lizenzierung pro Benutzer. Wenn Sie nicht sicher sind, welche Lizenzen eDiscovery (Standard) unterstützen, besuchen Sie [Erste Schritte mit eDiscovery (Standard) in Microsoft Purview](https://docs.microsoft.com/microsoft-365/compliance/get-started-core-ediscovery?view=o365-worldwide).

**Geschätzte Dauer**: 45 Minuten

### Aufgabe 1

Für den Zugriff auf eDiscovery (Standard) oder das Hinzufügen als Mitglied eines eDiscovery-Falls müssen einem Benutzer die entsprechenden Berechtigungen zugewiesen werden. In dieser Aufgabe fügen Sie als globale(r) Administrator*in bestimmte Benutzer*innen als Mitglieder der Rollengruppe „eDiscovery-Manager“ hinzu.

1. Öffnen Sie die Browserregisterkarte für die Startseite von Microsoft Purview.  Wenn Sie die Registerkarte zuvor geschlossen haben, öffnen Sie eine neue Browserregisterkarte, und geben Sie **https://admin.microsoft.com** ein. Melden Sie sich mit den Administratoranmeldeinformationen für den Microsoft 365-Mandanten an, der vom autorisierten Labhoster (ALH) bereitgestellt wird. Wählen Sie im linken Navigationsbereich von Microsoft 365 Admin Center **Alle anzeigen** und dann **Compliance** aus.  Die Startseite des Microsoft Purview-Portals wird auf einer neuen Browserseite geöffnet.  

1. Wählen Sie im linken Navigationsbereich **Einstellungen**, erweitern Sie **Rollen und Bereiche** und wählen Sie dann **Rollengruppen**.

1. Geben Sie in das Suchfeld oben rechts auf der Seite **eDiscovery** ein und drücken Sie die Eingabetaste auf Ihrer Tastatur.  Wählen Sie **eDiscovery-Manager** aus.

1. Wählen Sie **Bearbeiten** aus. Für dieses Lab setzen Sie sich als MOD-Admin sowie als eDiscovery-Manager und -Admin ein.  In der Praxis würden Sie bestimmte Benutzende für bestimmte Rollen benennen.
    1. Auf der Seite „eDiscovery-Manager verwalten“ können Sie Benutzer*innen der Rolle „eDiscovery-Manager“ hinzufügen.
    1. Wählen Sie **Benutzer auswählen** aus. Suchen Sie nach und wählen Sie **MOD-Administrator**. Drücken Sie dann **Auswählen** am unteren Ende der Seite und wählen Sie **Weiter**.
    1. Wählen Sie auf der Seite „eDiscovery-Administrator verwalten“ die Option **Benutzer auswählen** aus. Suchen Sie nach **MOD-Administrator** und wählen Sie **Auswählen** unten auf der Seite. Wählen Sie dann **Weiter** und anschließend **Speichern**.
    1. Wählen Sie auf der Seite „Sie haben die Rollengruppe erfolgreich aktualisiert“ die Option **Fertig** aus.

1. Lassen Sie diese Browserregisterkarte geöffnet, da Sie sie in der nächsten Aufgabe verwenden werden.

### Aufgabe 2

Bei dieser Aufgabe erstellen Sie als ein eDiscovery-Administrator (der MOD-Administrator ist ein eDiscovery-Administrator) einen Fall, um mit der Verwendung von eDiscovery (Standard) zu beginnen.

1. Sie sollten sich immer noch auf der Seite „Rollen“ im Complianceportal befinden. Wenn Sie die Browserregisterkarte der vorherigen Aufgabe geschlossen haben, öffnen Sie eine neue Browserregisterkarte und geben Sie **compliance.microsoft.com** ein, um zum Microsoft Purview-Portal zu gelangen.

1. Erweitern Sie in der linken Navigationsleiste unter Lösungen **eDiscovery** und wählen Sie dann **Standardfälle**.

1. Wählen Sie oben auf der Seite „eDiscovery (Standard)“ die Option **+ Fall erstellen** aus.

1. Geben Sie im Fenster „Neuer Fall“ einen Fallnamen ein, **SC900 Testfall**, und klicken Sie dann unten auf der Seite auf **Speichern**.

1. Der Fall sollte jetzt in der Liste angezeigt werden.

1. Als Ersteller des Falls und weil Sie über eDiscovery-Administratorrechte verfügen, können Sie damit beginnen.  

1. Lassen Sie diese Browserregisterkarte geöffnet, da Sie sie in der nachfolgenden Aufgabe verwenden werden.

### Aufgabe 3

Nun können Sie den von Ihnen erstellten eDiscovery-Fall (Standardfall) bearbeiten.  Bei dieser Aufgabe erstellen Sie eine eDiscovery-Aufbewahrung für den von Ihnen erstellten Fall.  Insbesondere erstellen Sie dabei eine Aufbewahrung für das Exchange-Postfach von Adele Vance.

1. Öffnen Sie in Ihrem Browser die Registerkarte „eDiscovery (Standard)“.

1. Wählen Sie auf der Seite „eDiscovery (Standard)“ den Fall **SC900-Testfall** aus, den Sie auf der vorherigen Registerkarte erstellt haben.

1. Wählen Sie auf der Startseite des Falls die Registerkarte **Halten** und dann **+Erstellen** aus.

1. Geben Sie im Feld „Name“ den Text **Testaufbewahrung** ein, und wählen Sie dann **Weiter** aus.

1. Wählen Sie auf der Seite „Speicherorte auswählen“ die Umschaltfläche neben **Exchange-Postfächer** aus, um den Status auf **Ein** festzulegen.  

1. Wählen Sie nun **Benutzer, Gruppen oder Teams auswählen** aus.  Geben Sie in das Suchfeld **Adele** ein, und drücken Sie dann die Eingabetaste auf der Tastatur. Wählen Sie in den Suchergebnissen **Adele Vance** und dann **Fertig** aus.

1. Wählen Sie auf der Seite „Speicherorte auswählen **Weiter** aus.  Aus Zweckmäßigkeitsgründen für dieses Lab werden keine weiteren Speicherorte in diese Aufbewahrung eingeschlossen.

1. Auf der Seite „Abfragebedingungen“ können Sie eine Aufbewahrung erstellen, die auf bestimmten erfüllten Schlüsselwörtern oder Bedingungen basiert. Wählen Sie **+ Bedingung hinzufügen** aus, um die verfügbaren Optionen anzuzeigen.  Wählen Sie **Weiter** aus. Ohne Bedingungen behält die Aufbewahrung alle Inhalte am angegebenen Speicherort bei.

1. Überprüfen Sie Ihre Einstellungen, und klicken Sie auf **Absenden** – es kann eine Minute dauern – und dann auf **Fertig**.  Die Test-Aufbewahrung sollte in der Liste angezeigt werden.  Klicken Sie auf **Aktualisieren**, falls sie nicht sofort angezeigt wird.

1. Lassen Sie diese Browserregisterkarte geöffnet, da Sie sie in der nachfolgenden Aufgabe verwenden werden.

### Aufgabe 4

Erstellen Sie bei vorhandener Aufbewahrung eine Suchabfrage.  Sobald Ihre Suche abgeschlossen ist, unterstützt der eDiscovery-Vorgang Aktionen, z. B. das Exportieren und Herunterladen der Ergebnisse für zukünftige Untersuchungen.   Hinweis: Die einem eDiscovery (Standard)-Fall zugeordneten Suchen werden auf der Seite „Inhaltssuche“ im Microsoft Purview-Compliance-Portal nicht aufgelistet. Diese Suchen werden lediglich auf der Seite „Suchen“ des zugeordneten eDiscovery (Standard)-Falls aufgelistet.

1. Öffnen Sie in Ihrem Browser die Registerkarte „SC900-Testfall“.

1. Wählen Sie auf der Seite „SC900-Testfall“ die Option **Suchen** aus.

1. Klicken Sie auf der Seite „Suchen“ auf **+ Neue Suche**.

1. Geben Sie im Feld „Name“ **Testaufbewahrung – Suche in Verkäufen** ein, und klicken Sie dann unten auf der Seite auf **Weiter**.

1. Wählen Sie auf der Seite „Speicherorte auswählen“ die Option **Speicherorte unter Aufbewahrung** aus, und deaktivieren Sie **App-Inhalt für lokale Benutzer hinzufügen**, da keine lokalen Benutzer in Ihrer Laborumgebung vorhanden sind. Wählen Sie dann **Weiter** aus.

1. Auf der Seite „Abfragebedingungen“ können Sie eine Suche basierend auf bestimmten Schlüsselwörtern oder Bedingungen erstellen, die erfüllt sind. Geben Sie im Feld Schlüsselwort **Vertrieb** ein und klicken Sie auf **Weiter**.

1. Überprüfen Sie Ihre Einstellungen, und klicken Sie auf **Absenden** – es kann eine Minute dauern – und dann auf **Fertig**.  Die Suche sollte in der Liste angezeigt werden.  Klicken Sie auf **Aktualisieren**, falls sie nicht sofort angezeigt wird.

1. Wählen Sie im Fenster „Suchen“ die von Ihnen soeben erstellte Suche **Testaufbewahrung – Vertriebssuche** aus.  Ein Fenster, das mit ausgewählter Registerkarte „Zusammenfassung“ geöffnet wird.  Nach Abschluss der Suche gibt der Status an, dass sie beendet ist.  Es wird die Registerkarte „Suchstatistik“ angezeigt (wenn die Registerkarte „Suchstatistik“ nicht angezeigt wird, kann es sein, dass die Suche noch ausgeführt wird und ihr Abschluss möglicherweise noch einige Minuten dauert).  Wählen Sie die Registerkarte **Suchstatistik** aus und klicken Sie auf den Dropdownpfeil neben „Inhalt suchen“.  Sie können auch weitere Informationen für den Bericht „Bedingung“ und „Top“-Speicherorte anzeigen.  

1. Wählen Sie am unteren Rand der Seite **Aktionen** aus.  Beachten Sie die verfügbaren Optionen, die Exportoptionen enthalten (die Exportoptionen können nicht innerhalb der Lab-Plattform ausgewählt werden, die vom autorisierten Lab-Hoster bereitgestellt wird, sind aber in einer Produktionsumgebung verfügbar und gelten als Teil des Standardworkflows). Wählen Sie **Schließen** aus.

1. Melden Sie sich ab, und schließen Sie alle geöffneten Browserfenster.

### Überprüfung

In diesem Lab haben Sie die ersten Schritte für eDiscovery (Standard) ausgeführt, darunter das Einrichten von Rollenberechtigungen für eDiscovery und das Erstellen eines eDiscovery-Falls.  Mit dem erstellten Fall haben Sie Elemente des eDiscovery Workflows (Standardworkflow) durchlaufen, indem Sie eine eDiscovery-Aufbewahrung und eine Suchanfrage erstellt haben.
