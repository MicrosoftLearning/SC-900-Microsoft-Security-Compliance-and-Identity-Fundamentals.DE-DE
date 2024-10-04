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

Für den Zugriff auf eDiscovery (Standard) oder das Hinzufügen als Mitglied eines eDiscovery-Falls müssen einem Benutzer die entsprechenden Berechtigungen zugewiesen werden. In diesem Teil der Demo durchlaufen Sie als globale*r Administrator*in den Prozess zum Hinzufügen bestimmter Benutzer*innen als Mitglieder der Rollengruppe „eDiscovery-Manager“.

1. Öffnen Sie die Browser-Registerkarte für **Microsoft Purview**. Wenn Sie es zuvor geschlossen haben, öffnen Sie eine Browser-Registerkarte und geben Sie in der Adressleiste **https://purview.microsoft.com** ein. Um auf das neue Microsoft Purview-Portal zuzugreifen, markieren Sie das Kontrollkästchen neben **Ich stimme den Bedingungen der Datenflussoffenlegung und den Datenschutzbestimmungen zu**, und wählen Sie dann **Erste Schritte** aus.  
1. Wählen Sie im linken Navigationsbereich **Einstellungen** aus.
1. Wählen Sie in dem sich öffnenden Navigationsbereich **Rollen und Bereiche**, um die Option zu erweitern, und wählen Sie dann **Rollengruppen**.
1. Suchen Sie im Suchfeld auf der rechten Seite des Bildschirms nach dem Begriff **eDiscovery**.  Wählen Sie **eDiscovery-Manager** aus.
    1. Wählen Sie **Bearbeiten** aus.
    1. Wählen Sie **Benutzer auswählen** aus.
    1. Suchen Sie nach „MOD-Administrator“, wählen Sie das Feld neben **MOD-Administrator** aus, und wählen Sie dann unten auf der Seite die Schaltfläche **Auswählen** aus.
    1. Wählen Sie **Weiter**, dann **Speichern** und schließlich **Fertig**.

1. Halten Sie diese Browser-Registerkarte offen.

### Teil 2 der Demo

In diesem Teil werden Sie einen Fall anlegen, um mit der Nutzung von eDiscovery (Standard) zu beginnen.

1. Wählen Sie im linken Navigationsbereich **Lösungen**, wählen Sie **eDiscovery** und wählen Sie dann **Standardfälle**.

1. Wählen Sie oben auf der Seite „eDiscovery (Standard)“ die Option **+ Fall erstellen** aus.

1. Geben Sie im Fenster „Neuer Fall“ einen Fallnamen ein, **SC900 Testfall**, und klicken Sie dann unten auf der Seite auf **Speichern**.

1. Der Fall sollte jetzt in der Liste angezeigt werden.

1. Als Ersteller des Falls und weil Sie über eDiscovery-Administratorrechte verfügen, können Sie damit beginnen.  

1. Halten Sie diese Browser-Registerkarte offen.

### Teil 3 der Demo

Nun können Sie den von Ihnen erstellten eDiscovery-Fall (Standardfall) bearbeiten.  Hier erstellen Sie eine eDiscovery-Aufbewahrung für den von Ihnen erstellten Fall.  Insbesondere erstellen Sie dabei eine Aufbewahrung für das Exchange-Postfach von Adele Vance.

1. Wählen Sie auf der Seite „eDiscovery (Standard)“ den von Ihnen erstellten Fall **SC900-Testfall** aus.

1. Wählen Sie auf der Startseite des Falls die Registerkarte **Halten** und dann **Erstellen**aus.

1. Geben Sie im Feld „Name“ den Text **Testaufbewahrung** ein, und wählen Sie dann **Weiter** aus.

1. Wählen Sie auf der Seite „Speicherorte auswählen“ die Umschaltfläche neben **Exchange-Postfächer** aus, um den Status auf **Ein** festzulegen.  

1. Wählen Sie nun **Benutzer, Gruppen oder Teams auswählen** aus.  Geben Sie in das Suchfeld **Adele** ein, und drücken Sie dann die Eingabetaste auf der Tastatur. Wählen Sie in den Suchergebnissen **Adele Vance** und dann **Fertig** aus.

1. Wählen Sie auf der Seite "Speicherorte auswählen" **Weiter**aus.  Aus Zweckmäßigkeitsgründen sind in der Demo bei dieser Aufbewahrung keine anderen Speicherorte enthalten.

1. Auf der Seite „Abfragebedingungen“ können Sie eine Aufbewahrung erstellen, die auf bestimmten erfüllten Schlüsselwörtern oder Bedingungen basiert. Wählen Sie **+ Bedingung hinzufügen** aus, um die verfügbaren Optionen anzuzeigen.  Wählen Sie **Weiter** aus. Ohne Bedingungen behält die Aufbewahrung alle Inhalte am angegebenen Speicherort bei.

1. Überprüfen Sie Ihre Einstellungen, und klicken Sie auf **Absenden** – es kann eine Minute dauern – und dann auf **Fertig**.  Die Test-Aufbewahrung sollte in der Liste angezeigt werden.  Wählen Sie **Aktualisieren** aus, falls die Richtlinie nicht sofort angezeigt wird.

1. Halten Sie diese Browser-Registerkarte offen.

### Teil 4 der Demo

Erstellen Sie bei vorhandener Aufbewahrung eine Suchabfrage.  Sobald Ihre Suche abgeschlossen ist, unterstützt der eDiscovery-Vorgang Aktionen, z. B. das Exportieren und Herunterladen der Ergebnisse für zukünftige Untersuchungen.   Hinweis: Die einem eDiscovery (Standard)-Fall zugeordneten Suchen werden auf der Seite „Inhaltssuche“ im Microsoft Purview-Compliance-Portal nicht aufgelistet. Diese Suchen werden lediglich auf der Seite „Suchen“ des zugeordneten eDiscovery (Standard)-Falls aufgelistet.

1. Wählen Sie auf der Seite „SC900-Testfall“ die Option **Suchen** aus.

1. Klicken Sie auf der Seite „Suchen“ auf **+ Neue Suche**.

1. Geben Sie im Feld „Name“ **Testaufbewahrung – Suche in Verkäufen** ein, und klicken Sie dann unten auf der Seite auf **Weiter**.

1. Wählen Sie auf der Seite „Speicherorte auswählen“ die Option **Gesperrte Speicherorte** aus und deaktivieren Sie **App-Inhalt für lokale Benutzer hinzufügen**, da keine lokalen Benutzenden in Ihrer Lab-Umgebung vorhanden sind. Klicken Sie dann auf **Weiter**.

1. Auf der Seite „Abfragebedingungen“ können Sie eine Suche basierend auf bestimmten Schlüsselwörtern oder Bedingungen erstellen, die erfüllt sind. Geben Sie im Feld Schlüsselwort **Vertrieb** ein und klicken Sie auf **Weiter**.

1. Überprüfen Sie Ihre Einstellungen, und klicken Sie auf **Absenden** – es kann eine Minute dauern – und dann auf **Fertig**.  Die Suche sollte in der Liste angezeigt werden.  Klicken Sie auf **Aktualisieren**, falls sie nicht sofort angezeigt wird.

1. Wählen Sie im Fenster „Suchen“ die von Ihnen soeben erstellte Suche **Testaufbewahrung – Vertriebssuche** aus.  Ein Fenster, das mit ausgewählter Registerkarte „Zusammenfassung“ geöffnet wird.  Nach Abschluss der Suche gibt der Status an, dass sie beendet ist.  Es wird die Registerkarte „Suchstatistik“ angezeigt (wenn die Registerkarte „Suchstatistik“ nicht angezeigt wird, kann es sein, dass die Suche noch ausgeführt wird und ihr Abschluss möglicherweise noch einige Minuten dauert).  Wählen Sie die Registerkarte **Suchstatistik** und den Dropdownpfeil neben „Inhalt suchen“ aus.  Sie können auch weitere Informationen für den Bericht "Bedingung" und "Top"-Speicherorte anzeigen.  

1. Wählen Sie am unteren Rand der Seite **Aktionen** aus.  Beachten Sie die verfügbaren Optionen, die Exportoptionen enthalten. Wählen Sie **Schließen** aus.

1. Schließen Sie alle geöffneten Browserregisterkarten.

### Überprüfung

In dieser Demo haben Sie die ersten Schritte für eDiscovery (Standard) ausgeführt, darunter das Einrichten von Rollenberechtigungen für eDiscovery und das Erstellen eines eDiscovery-Falls.  Mit dem erstellten Fall haben Sie Elemente des eDiscovery Workflows (Standardworkflow) durchlaufen, indem Sie eine eDiscovery-Aufbewahrung und eine Suchanfrage erstellt haben.
