<!---
---
Demo: Titel: „Erkunden des eDiscovery-Workflows“ Lernpfad/Modul/Lerneinheit: „Lernpfad: Beschreiben der Funktionen von Microsoft Priva und Microsoft Purview; Modul 3: Beschreiben der Daten-Compliance-Lösungen von Microsoft Purview; Einheit 2: Beschreiben von eDiscovery“
---
--->

# Demo: Erkunden von eDiscovery (Standard)

Diese Demo ist den folgenden Learn-Inhalten zugeordnet:

- Lernpfad: Beschreiben der Funktionen von Microsoft Priva und Microsoft Purview
- Modul: Beschreiben der Daten-Compliance-Lösungen von Microsoft Purview
- Lerneinheit: Beschreiben von eDiscovery

## Vorführungsszenario

In dieser Demo gehen Sie die Schritte durch, die zum Einrichten von eDiscovery erforderlich sind, darunter Einrichten von Rollenberechtigungen, Erstellen eines eDiscovery-Falls, Erstellen einer eDiscovery-Aufbewahrung und Erstellen einer Suchabfrage.  HINWEIS: Im Microsoft Purview-Portal werden Updates für die Benutzeroberfläche schrittweise eingeführt. Einige Lab-/Demomandanten zeigen möglicherweise noch nicht die neueste Benutzeroberfläche an, sodass alle Lab-Schritte mithilfe der klassischen eDiscovery-Benutzeroberfläche angezeigt werden.

### Teil 1 der Demo

Um auf eDiscovery zuzugreifen oder als Mitglied eines eDiscovery-Falls hinzugefügt zu werden, müssen benutzenden Personen die entsprechenden Berechtigungen zugewiesen werden. In diesem Teil der Demo durchlaufen Sie als globale*r Administrator*in den Prozess zum Hinzufügen bestimmter Benutzer*innen als Mitglieder der Rollengruppe „eDiscovery-Manager“.

1. Öffnen Sie die Browser-Registerkarte für **Microsoft Purview**. Wenn Sie die Anwendung zuvor geschlossen haben, öffnen Sie eine Browserregisterkarte, und geben Sie **https://purview.microsoft.com** in der Adressleiste ein und wählen Sie dann die Option **Erste Schritte** aus.  
1. Wählen Sie im linken Navigationsbereich **Einstellungen** aus.
1. Wählen Sie in dem sich öffnenden Navigationsbereich **Rollen und Bereiche**, um die Option zu erweitern, und wählen Sie dann **Rollengruppen**.
1. Suchen Sie im Suchfeld auf der rechten Seite des Bildschirms nach dem Begriff **eDiscovery**.  Wählen Sie **eDiscovery-Manager** aus.
    1. Wählen Sie **Bearbeiten** aus.
    1. Wählen Sie **Benutzer auswählen** aus.
    1. Suchen Sie nach „MOD-Administrator“, wählen Sie das Feld neben **MOD-Administrator** aus, und wählen Sie dann unten auf der Seite die Schaltfläche **Auswählen** aus.
    1. Wählen Sie **Weiter**, dann **Speichern** und schließlich **Fertig**.

1. Halten Sie diese Browser-Registerkarte offen.

### Teil 2 der Demo

Hier erstellen Sie als eDiscovery-Admin (MOD-Admin ist eine bzw. ein Discovery-Admin) einen Fall, um mit der Verwendung von eDiscovery zu beginnen.

1. Sie sollten sich auf der Startseite des Microsoft Purview-Portals befinden.

1. Erweitern Sie im linken Navigationsbereich unter „Lösungen“ die Option **eDiscovery** und wählen Sie dann **Fälle** aus.

1. Wählen Sie auf der Seite „Fälle“ die Option **Fall erstellen** aus.

1. Geben Sie im Fenster „Neuer Fall“ den Fallnamen **SC900 Test Case** ein, und wählen Sie dann **Erstellen** aus.

1. Der Fall sollte jetzt in der Liste angezeigt werden.

1. Als Ersteller des Falls und weil Sie über eDiscovery-Administratorrechte verfügen, können Sie damit beginnen.  

1. Lassen Sie diese Browserregisterkarte geöffnet, da Sie sie in der nachfolgenden Aufgabe verwenden werden.

### Teil 3 der Demo

Sobald ein Fall erstellt wurde, können Sie mit diesem arbeiten. Zu den verfügbaren Optionen zählen das Erstellen einer Suchabfrage, um nach Daten und Inhalten zu suchen, die für Ihren Fall relevant sind, das Anwenden einer Aufbewahrungsrichtlinie, das Erstellen eines Prüfdateisatzes und das Exportieren von Daten. In dieser Aufgabe werden Sie mehr zu einigen dieser Optionen erfahren. HINWEIS: Es wird empfohlen, vor der Übermittlung einen Such- und Prüfdateisatz zu erstellen, damit die Ergebnisse der Suche und des Prüfdateisatzes während der Demo sofort verfügbar sind, da das Abschließen dieser Aktionen mehrere Minuten dauern kann.  

1. Öffnen Sie in Ihrem Browser die Registerkarte „SC900-Testfall“.

1. Wählen Sie auf der Seite „SC900 Test Case“ die Option **Suche erstellen** aus.

1. Geben Sie im Feld „Name“ **SC900 case search** ein, und wählen Sie dann **Erstellen** aus.

1. Wählen Sie **Quellen hinzufügen** aus. Beachten Sie die Filteroptionen und Standardeinstellungen. Geben Sie **`Pradeep`** im Suchfeld ein und wählen Sie dann **Suchen** aus. Wählen Sie von den Suchergebnissen **Pradeep Gupta** und dann **Speichern und schließen** aus. Mit dem Bedingungsgenerator können Sie eine Suchabfrage basierend auf bestimmten Schlüsselwörtern oder erfüllten Bedingungen erstellen. Geben Sie **Sales** in das Schlüsselwortfeld ein. Von hier aus können Sie sich dazu entscheiden, die **Abfrage auszuführen** und zwar vom Fenster „Suchergebnisse auswählen“ aus. Für den Labormandanten ist nur die Statistikansicht der Suchergebnisse verfügbar. Beachten Sie, dass die Optionen nach den wichtigsten Indikatoren angeordnet werden sollen. Wählen Sie **Abfrage ausführen** aus.  Dieser Vorgang kann einige Minuten in Anspruch nehmen.

1. Wenn Abfrageergebnisse in Form von Statistiken zurückgegeben werden, können Sie die Ergebnisse exportieren.  Wählen Sie oben rechts am Bildschirm (neben „Zu Prüfdateisatz hinzufügen“) die Option **Exportieren** aus, um die verfügbaren Optionen anzuzeigen, und wählen Sie dann **Abbrechen**aus.

1. Sie können einem Prüfdateisatz Elemente zur weiteren Verarbeitung hinzufügen.  Wählen Sie **Zu Prüfdateisatz hinzufügen** aus. Geben Sie einen Namen für den neuen Prüfdateisatz ein (**`SC900-review-set`**), übernehmen Sie die Standardeinstellungen und wählen Sie dann **Zu Prüfdateisatz hinzufügen** aus. Dies kann einige Minuten dauern. Sobald die Ergebnisse des Prüfdateisatzes präsentiert wurden, können Sie sich die verschiedenen Optionen ansehen, darunter „Analyse“, „Abfrage“, „Aktionen“, „Dateien markieren“ und „Verwalten“.

1. Sie können auch Aufbewahrungsrichtlinien erstellen, um für Ihren Fall relevante Inhalte beizubehalten. Wählen Sie im Fenster „Prüfdateisatz“ die Registerkarte **Aufbewahrung** aus.  Dadurch gelangen Sie zum Fenster „Aufbewahrungsrichtlinien“. Wählen Sie **Neue Richtlinie**.  Geben Sie einen Namen für die Richtlinie ein (**`SC900-hold`**) und wählen Sie **Erstellen** aus.  Sie müssen wie bei der Suche Datenquellen für die Aufbewahrung hinzufügen. Sie können auch können Schlüsselwörter und Bedingungen hinzufügen, die in der Aufbewahrungsrichtlinie verwendet werden sollen. Wählen Sie anschließend **Aufbewahrung anwenden** aus.  Zu den Aktionen, die Sie für Aufbewahrungsrichtlinien ausführen können, zählen das Wiederholen, Deaktivieren und Löschen einer Aufbewahrungsrichtlinie.

1. Melden Sie sich ab, und schließen Sie alle geöffneten Browserfenster.

### Überprüfung

In dieser Demo haben Sie mehr über die ersten Schritte für die Verwendung von eDiscovery erfahren, darunter das Einrichten der Rollenberechtigungen für eDiscovery und das Erstellen eines eDiscovery-Falls.  Im Zuge des Falls haben Sie die Einstellungen zum Erstellen von Such- und Exportergebnissen, zum Hinzufügen zu einem Prüfdateisatz und zum Erstellen eines Aufbewahrungszeitraums näher kennengelernt.
