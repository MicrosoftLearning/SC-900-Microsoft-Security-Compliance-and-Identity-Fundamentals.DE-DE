---
lab:
  title: Erkunden von eDiscovery
  module: Describe the data compliance solutions of Microsoft Purview
---

# Lab: Erkunden von eDiscovery

Dieses Lab ist den folgenden Learn-Inhalten zugeordnet:

- Lernpfad: Beschreiben der Funktionen von Microsoft Priva und Microsoft Purview
- Modul: Beschreiben der Daten-Compliance-Lösungen von Microsoft Purview
- Lerneinheit: Beschreiben von eDiscovery

## Labszenario

In diesem Lab gehen Sie die Schritte durch, die zum Festlegen von eDiscovery erforderlich sind, darunter Einrichten von Rollenberechtigungen, Erstellen eines eDiscovery-Falls, Erstellen einer eDiscovery-Aufbewahrung und Erstellen einer Suchabfrage.  Hinweis:  Für die Lizenzierung von eDiscovery sind das entsprechende Organisationsabonnement und die Lizenzierung pro benutzende Person erforderlich. Wenn Sie nicht sicher sind, welche Lizenzen eDiscovery unterstützen, lesen Sie [Erste Schritte mit eDiscovery in Microsoft Purview](https://docs.microsoft.com/microsoft-365/compliance/get-started-core-ediscovery?view=o365-worldwide).

**Geschätzte Dauer**: 45 Minuten

### Aufgabe 1

Um auf eDiscovery zuzugreifen oder als Mitglied eines eDiscovery-Falls hinzugefügt zu werden, müssen benutzenden Personen die entsprechenden Berechtigungen zugewiesen werden. In dieser Aufgabe fügen Sie als globale(r) Administrator*in bestimmte Benutzer*innen als Mitglieder der Rollengruppe „eDiscovery-Manager“ hinzu.

1. Sie sollten sich auf der Startseite des Microsoft Purview-Portals befinden.  Wenn Sie die Registerkarte zuvor geschlossen haben, öffnen Sie eine neue Browserregisterkarte, und geben Sie **https://purview.microsoft.com** ein.

1. Wählen Sie im linken Navigationsbereich **Einstellungen**, erweitern Sie **Rollen und Bereiche** und wählen Sie dann **Rollengruppen**.

1. Geben Sie in das Suchfeld oben rechts auf der Seite **eDiscovery** ein und drücken Sie die Eingabetaste auf Ihrer Tastatur.  Wählen Sie **eDiscovery-Manager** aus.

1. Wählen Sie **Bearbeiten** aus. Für diese Übung legen Sie sich als MOD-Admin als eDiscovery-Manager und -Admin fest.  In der Praxis würden Sie bestimmte Benutzende für bestimmte Rollen benennen.
    1. Auf der Seite „eDiscovery-Manager verwalten“ können Sie Benutzer*innen der Rolle „eDiscovery-Manager“ hinzufügen.
    1. Wählen Sie **Benutzer auswählen** aus. Suchen Sie nach und wählen Sie **MOD-Administrator**. Drücken Sie dann **Auswählen** am unteren Ende der Seite und wählen Sie **Weiter**.
    1. Wählen Sie auf der Seite „eDiscovery-Administrator verwalten“ die Option **Benutzer auswählen** aus. Suchen Sie nach **MOD-Administrator** und wählen Sie **Auswählen** unten auf der Seite. Wählen Sie dann **Weiter** und anschließend **Speichern**.
    1. Wählen Sie auf der Seite „Sie haben die Rollengruppe erfolgreich aktualisiert“ die Option **Fertig** aus.

1. Kehren Sie zur Startseite von Microsoft Purview zurück, indem Sie im linken Navigationsbereich **Startseite** auswählen.

1. Lassen Sie diese Browserregisterkarte geöffnet, da Sie sie in der nächsten Aufgabe verwenden werden.

### Aufgabe 2

In dieser Aufgabe erstellen Sie als für eDiscovery-Administration zuständige Person (die für MOD-Administration zuständige Person ist eine für eDiscovery-Administration zuständige Person) einen Fall, um mit der Verwendung von eDiscovery zu beginnen.

1. Sie sollten sich auf der Startseite des Microsoft Purview-Portals befinden.

1. Erweitern Sie im linken Navigationsbereich unter „Lösungen“ die Option **eDiscovery**, und wählen Sie dann **Fälle** aus.

1. Wählen Sie auf der Seite „Fälle“ den Text im linken Teil des blauen Felds aus, in dem **Fall erstellen** steht.  Wenn Sie den Abwärtspfeil auswählen, öffnen Sie das Fenster zum Erstellen einer Suche, und während der Erstellung wird ein Fall erstellt.
    1. Geben Sie im Fenster „Neuer Fall“ den Fallnamen **SC900 Test Case** ein, und wählen Sie dann **Erstellen** aus.
    1. Der Fall sollte jetzt in der Liste angezeigt werden.
    1. Als Ersteller des Falls und weil Sie über eDiscovery-Administratorrechte verfügen, können Sie damit beginnen.  
    1. Lassen Sie diese Browserregisterkarte geöffnet, da Sie sie in der nachfolgenden Aufgabe verwenden werden.

### Aufgabe 3

Sobald ein Fall erstellt wurde, können Sie damit arbeiten. Zu den verfügbaren Optionen zählen das Erstellen einer Suchabfrage, um nach Daten und Inhalten zu suchen, die für Ihren Fall relevant sind, das Anwenden einer Aufbewahrungsrichtlinie, das Erstellen eines Prüfdateisatzes und das Exportieren von Daten. In dieser Aufgabe werden Sie einige dieser Optionen erkunden.

1. Öffnen Sie in Ihrem Browser die Registerkarte „SC900-Testfall“.

1. Wählen Sie auf der Seite „SC900 Test Case“ die Option **Suche erstellen** aus.

1. Geben Sie im Feld „Name“ **SC900 case search** ein, und wählen Sie dann **Erstellen** aus.

1. Wählen Sie **Quellen hinzufügen** aus. Beachten Sie die Filteroptionen und Standardeinstellungen. Geben Sie **`Pradeep`** im Suchfeld ein, und wählen Sie dann **Suchen** aus. Wählen Sie in den Suchergebnissen **Pradeep Gupta** und dann **Speichern und schließen** aus. Mit dem Bedingungsgenerator können Sie eine Suchabfrage basierend auf bestimmten Schlüsselwörtern oder erfüllten Bedingungen erstellen. Geben Sie **Sales** in das Schlüsselwortfeld ein. Nun können Sie im Fenster „Suchergebnisse auswählen“ die Option **Abfrage auszuführen** auswählen. Für den Labmandanten ist nur die Statistikansicht der Suchergebnisse verfügbar. Beachten Sie, dass die Optionen nach den wichtigsten Indikatoren angeordnet werden sollen. Wählen Sie **Abfrage ausführen** aus.  Dieser Vorgang kann einige Minuten in Anspruch nehmen.

1. Wenn Abfrageergebnisse in Form von Statistiken zurückgegeben werden, können Sie die Ergebnisse exportieren.  Wählen Sie **Exportieren** aus, um die verfügbaren Optionen anzuzeigen, und wählen Sie dann **Abbrechen** aus.

1. Sie können einem Prüfdateisatz Elemente hinzufügen, um ihn weiter zu bearbeiten.  Wählen Sie **Zu Prüfdateisatz hinzufügen** aus. Geben Sie einen Namen für den neuen Prüfdateisatz ein (**`SC900-review-set`**), übernehmen Sie die Standardeinstellungen, und wählen Sie dann **Zu Prüfdateisatz hinzufügen** aus. Dies kann einige Minuten dauern. Sobald die Ergebnisse des Prüfdateisatzes präsentiert wurden, können Sie sich die verschiedenen Optionen ansehen, darunter „Analyse“, „Abfragen“, „Aktionen“, „Dateien markieren“ und „Verwalten“.

1. Sie können auch Aufbewahrungsrichtlinien erstellen, um Inhalte beizubehalten, die für Ihren Fall relevant sind. Wählen Sie im Fenster „Prüfdateisatz“ die Registerkarte **Halten** aus.  Dadurch gelangen Sie zum Fenster „Aufbewahrungsrichtlinien“. Wählen Sie **Neue Richtlinie**.  Geben Sie einen Namen für die Richtlinie ein (**`SC900-hold`**), und wählen Sie **Erstellen** aus.  Wie bei der Suche müssen Sie Datenquellen für die Aufbewahrung hinzufügen, und Sie können Schlüsselwörter und Bedingungen hinzufügen, die in der Aufbewahrungsrichtlinie verwendet werden sollen. Wählen Sie anschließend **Aufbewahrungspflicht anwenden** an.  Zu den Aktionen, die Sie für Aufbewahrungsrichtlinien ausführen können, zählen das Wiederholen, Deaktivieren und Löschen einer Aufbewahrungsrichtlinie.

1. Melden Sie sich ab, und schließen Sie alle geöffneten Browserfenster.

### Überprüfung

In diesem Lab haben Sie die ersten Schritte für die Verwendung von eDiscovery durchgeführt, darunter das Einrichten der Rollenberechtigungen für eDiscovery und das Erstellen eines eDiscovery-Falls.  Im Zuge des Falls haben Sie die Einstellungen zum Erstellen von Such- und Exportergebnissen, zum Hinzufügen zu einem Prüfdateisatz und zum Erstellen eines Aufbewahrungszeitraums näher kennengelernt.
