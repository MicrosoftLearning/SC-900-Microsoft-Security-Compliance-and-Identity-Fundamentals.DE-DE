<a name="---"></a><!---
---
Lab: Title: 'Erkunden des eDiscovery (Standard)-Workflows' Learning Path/Module/Unit: 'Lernpfad: Beschreiben der Funktionen der Microsoft-Compliancelösungen; Modul 5: eDiscovery-Funktionen und Überwachungsfunktionen von Microsoft Purview; Lerneinheit 2: Beschreiben der eDiscovery-Lösungen in Microsoft 365'
---
--->

# <a name="lab-explore-the-ediscovery-standard-workflow"></a>Lab: Erkunden des eDiscovery (Standard)-Workflows

Dieses Lab ist den folgenden Learn-Inhalten zugeordnet:

- Lernpfad: Beschreiben der Funktionen der Microsoft-Compliancelösungen
- Modul: eDiscovery-Funktionen und Überwachungsfunktionen von Microsoft Purview
- Lerneinheit: Beschreiben der eDiscovery-Lösungen in Microsoft 365

## <a name="lab-scenario"></a>Labszenario

In diesem Lab gehen Sie die Schritte durch, die zum Festlegen von eDiscovery erforderlich sind, darunter Einrichten von Rollenberechtigungen, Erstellen eines eDiscovery-Falls, Erstellen einer eDiscovery-Aufbewahrung und Erstellen einer Suchabfrage.  Hinweis:  Für die Lizenzierung von eDiscovery (Standard) sind das entsprechende Organisationsabonnement und die benutzerbezogene Lizenzierung erforderlich. Wenn Sie nicht sicher sind, welche Lizenzen eDiscovery (Standard) unterstützen, besuchen Sie [Erste Schritte mit eDiscovery (Standard) in Microsoft Purview](https://docs.microsoft.com/microsoft-365/compliance/get-started-core-ediscovery?view=o365-worldwide).

**Geschätzte Dauer**: 25-30 Minuten

### <a name="task-1"></a>Aufgabe 1

Für den Zugriff auf eDiscovery (Standard) oder das Hinzufügen als Mitglied eines eDiscovery-Falls müssen einem Benutzer die entsprechenden Berechtigungen zugewiesen werden. Bei dieser Aufgabe fügen Sie als globaler Administrator bestimmte Benutzer als Mitglieder der Rollgengruppe "eDiscovery-Manager" hinzu.

 Öffnen Sie Microsoft Edge. Geben Sie **admin.microsoft.com** in die Adressleiste ein.

1. Melden Sie sich mit Ihren Administratoranmeldeinformationen an.
    1. Geben Sie **admin@WWLxZZZZZZ.onmicrosoft.com** (ZZZZZZ ist hierbei die eindeutige Mandanten-ID, die von Ihrem Lab-Hostinganbieter bereitgestellt wurde) in das Fenster „Anmelden“ ein, und wählen Sie dann **Weiter** aus.

    1. Geben Sie das Administratorkennwort ein, das von Ihrem Lab-Hostinganbieter bereitgestellt werden sollte. Wählen Sie **Anmelden**.
    1. Wählen Sie **Ja** aus, wenn Sie gefragt werden, ob Sie angemeldet bleiben möchten. Dadurch gelangen Sie zur Seite „Microsoft 365 Admin Center“.

1. Wählen Sie im linken Navigationsbereich von Microsoft 365 Admin Center **Alle anzeigen** aus.

1. Wählen Sie unter „Admin Center“ die Option **Compliance** aus.  Die Startseite des Microsoft Purview-Complianceportals wird auf einer neuen Browserseite geöffnet.  

1. Wählen Sie im linken Navigationsbereich **Berechtigungen** aus.

1. Wählen Sie auf der Seite „Berechtigungen und Rollen“ unter „Microsoft Purview-Lösungen“ die Option **Rollen** aus.

1. Geben Sie **eDiscovery** in das Suchfeld ein, und wählen Sie dann das Suchsymbol (Lupe) aus.  Wählen Sie **eDiscovery-Manager** aus.

1. Beachten Sie im Fenster, das geöffnet wird, die zwei Untergruppen: „eDiscovery-Manager“ und „eDiscovery-Administrator“.  Lesen Sie die jeweilige Beschreibung.  In diesem Lab fügen wir der Untergruppe „eDiscovery-Administrator“ Mitglieder hinzu. Wählen Sie **Bearbeiten** neben „eDiscovery-Administrator“ aus.  Als allgemein bewährte Methode empfiehlt es sich, Benutzern die niedrigste Berechtigung zuzuweisen, die für ihre Rolle erforderlich ist.

1. Wählen Sie die Registerkarte **eDiscovery-Administrator auswählen** und dann **eDiscovery-Administrator auswählen** aus, um dieser Rollengruppe Mitglieder hinzuzufügen.

1. Wählen Sie oben auf der Seite **+ hinzufügen** aus.

1. Wählen Sie in der Liste der Namen die Einträge **MOD-Administrator** und **Megan Bowen** aus. Wählen Sie dann unten auf der Seite die Option **Hinzufügen** und **Fertig** aus.

1. Überprüfen Sie, ob die hinzugefügten Mitglieder richtig sind, und wählen Sie dann **Speichern** aus.

1. Wählen Sie unten im Fenster „eDiscovery“ die Option **Schließen** aus.

1. Lassen Sie diese Browserregisterkarte geöffnet, da Sie sie in der nächsten Aufgabe verwenden werden.

### <a name="task-2"></a>Aufgabe 2

Bei dieser Aufgabe erstellen Sie als ein eDiscovery-Administrator (der MOD-Administrator ist ein eDiscovery-Administrator) einen Fall, um mit der Verwendung von eDiscovery (Standard) zu beginnen.

1. Sie sollten sich immer noch auf der Seite „Rollen“ im Complianceportal befinden. Wenn Sie die Browserregisterkarte aus der vorherigen Aufgabe geschlossen haben, öffnen Sie eine neue, und geben Sie **compliance.microsoft.com** ein.

1. Wählen Sie im linken Navigationsbereich unter „Lösungen“ die Optionen **eDiscovery** und dann **Standard** aus.

1. Wählen Sie oben auf der Seite „eDiscovery (Standard)“ die Option **+ Fall erstellen** aus.

1. Geben Sie in das Fenster „Neuer Fall“ den Fallnamen **SC900-Testfall** ein. Wählen Sie dann unten auf der Seite **Speichern** aus.

1. Der Fall sollte nun in der Liste angezeigt werden.

1. Da Sie den Fall erstellt haben und über eDiscovery-Administrator-Berechtigungen verfügen, können Sie ihn bearbeiten.  

1. Lassen Sie diese Browserregisterkarte geöffnet, da Sie sie in der nachfolgenden Aufgabe verwenden werden.

### <a name="task-3"></a>Aufgabe 3

Nun können Sie den von Ihnen erstellten eDiscovery-Fall (Standardfall) bearbeiten.  Bei dieser Aufgabe erstellen Sie eine eDiscovery-Aufbewahrung für den von Ihnen erstellten Fall.  Insbesondere erstellen Sie dabei eine Aufbewahrung für das Exchange-Postfach von Adele Vance.

1. Öffnen Sie in Ihrem Browser die Registerkarte „eDiscovery (Standard)“.

1. Wählen Sie auf der Seite „eDiscovery (Standard)“ den Fall **SC900-Testfall** aus, den Sie auf der vorherigen Registerkarte erstellt haben.

1. Wählen Sie auf der Startseite des Falls die Registerkarte **Aufbewahrung** und dann **+ Erstellen** aus.

1. Geben Sie im Feld „Name“ den Text **Testaufbewahrung** ein, und wählen Sie dann **Weiter** aus.

1. Wählen Sie auf der Seite „Speicherorte auswählen“ die Umschaltfläche neben **Exchange-Postfächer** aus, um den Status auf **Ein** festzulegen.  

1. Wählen Sie nun **Benutzer, Gruppen oder Teams auswählen** aus.  Geben Sie **Adele** in das Suchfeld ein, und drücken Sie dann die EINGABETASTE auf Ihrer Tastatur. Wählen Sie in den Suchergebnissen **Adele Vance** und dann **Fertig** aus.

1. Wählen Sie auf der Seite „Speicherorte auswählen“ die Option **Weiter** aus.  Aus Zweckmäßigkeitsgründen sind im Lab bei dieser Aufbewahrung keine anderen Speicherorte enthalten.

1. Auf der Seite „Abfragebedingungen“ können Sie eine Aufbewahrung erstellen, die auf bestimmten erfüllten Schlüsselwörtern oder Bedingungen basiert. Wählen Sie **+ Bedingung hinzufügen** aus, um die verfügbaren Optionen anzuzeigen.  Wählen Sie **Weiter** aus. Sind keine Bedingungen vorhanden, behält die Aufbewahrung alle Inhalte am angegebenen Speicherort bei.

1. Überprüfen Sie Ihre Einstellungen, und wählen Sie **Senden** aus. Es kann eine Minute dauern. Wählen Sie dann **Fertig** aus.  „Testaufbewahrung“ sollte in der Liste angezeigt werden.  Wenn es nicht sofort angezeigt wird, wählen Sie **Aktualisieren** aus.

1. Lassen Sie diese Browserregisterkarte geöffnet, da Sie sie in der nachfolgenden Aufgabe verwenden werden.

### <a name="task-4"></a>Aufgabe 4

Erstellen Sie bei vorhandener Aufbewahrung eine Suchabfrage.  Sobald Ihre Suche abgeschlossen ist, unterstützt der eDiscovery-Vorgang Aktionen, z. B. das Exportieren und Herunterladen der Ergebnisse für zukünftige Untersuchungen.   Hinweis:  Die einem eDiscovery (Standard)-Fall zugeordneten Suchen werden auf der Seite „Inhaltssuche“ im Microsoft Purview-Complianceportal nicht aufgelistet. Diese Suchen werden lediglich auf der Seite „Suchen“ des zugeordneten eDiscovery (Standard)-Falls aufgelistet.

1. Öffnen Sie in Ihrem Browser die Registerkarte „SC900-Testfall“.

1. Wählen Sie auf der Seite „SC900-Testfall“ die Option **Suchen** aus.

1. Wählen Sie auf der Seite „Suche“ die Option **+ Neue Suche** aus.

1. Geben Sie in das Feld „Name“ den Text **Testaufbewahrung – Vertriebssuche** ein. Wählen Sie dann unten auf der Seite **Weiter** aus.

1. Wählen Sie auf der Seite „Speicherorte auswählen“ die Option **Speicherorte unter Aufbewahrung** aus, und deaktivieren Sie **App-Inhalt für lokale Benutzer hinzufügen**, da keine lokalen Benutzer in Ihrer Laborumgebung vorhanden sind. Wählen Sie dann **Weiter** aus.

1. Auf der Seite „Abfragebedingungen“ können Sie eine Suche erstellen, die auf bestimmten erfüllten Schlüsselwörtern oder Bedingungen basiert. Geben Sie in das Feld „Schlüsselwort“ den Text **Vertrieb** ein, und wählen Sie **Weiter** aus.

1. Überprüfen Sie Ihre Einstellungen, und wählen Sie **Senden** aus. Es kann eine Minute dauern. Wählen Sie dann **Fertig** aus.  Das Suchelement sollte in der Liste angezeigt werden.  Wenn es nicht sofort angezeigt wird, wählen Sie **Aktualisieren** aus.

1. Wählen Sie im Fenster „Suchen“ die von Ihnen soeben erstellte Suche **Testaufbewahrung – Vertriebssuche** aus.  Es wird ein Fenster geöffnet, in dem die Registerkarte „Zusammenfassung“ ausgewählt ist.  Nach Abschluss der Suche gibt der Status an, dass sie beendet ist.  Es wird die Registerkarte „Suchstatistik“ angezeigt (wenn die Registerkarte „Suchstatistik“ nicht angezeigt wird, kann es sein, dass die Suche noch ausgeführt wird und ihr Abschluss möglicherweise noch einige Minuten dauert).  Wählen Sie die Registerkarte **Suchstatistik** und das Dropdown neben „Inhaltssuche“ aus.  Zudem können Sie weitere Informationen für „Bedingungsbericht“ und „Top-Orte“ anzeigen.  

1. Wählen Sie unten auf der Seite **Aktionen** aus.  Beachten Sie die verfügbaren Optionen, die Exportoptionen enthalten (die Exportoptionen können nicht innerhalb der Lab-Plattform ausgewählt werden, die vom autorisierten Lab-Hoster bereitgestellt wird, sind aber in einer Produktionsumgebung verfügbar und gelten als Teil des Standardworkflows). Klicken Sie auf **Schließen**.

1. Schließen Sie alle geöffneten Browserregisterkarten.

### <a name="review"></a>Überprüfung

In diesem Lab haben Sie die ersten Schritte für eDiscovery (Standard) ausgeführt, darunter das Einrichten von Rollenberechtigungen für eDiscovery und das Erstellen eines eDiscovery-Falls.  Mit dem erstellten Fall haben Sie Elemente des eDiscovery Workflows (Standardworkflow) durchlaufen, indem Sie eine eDiscovery-Aufbewahrung und eine Suchanfrage erstellt haben.
