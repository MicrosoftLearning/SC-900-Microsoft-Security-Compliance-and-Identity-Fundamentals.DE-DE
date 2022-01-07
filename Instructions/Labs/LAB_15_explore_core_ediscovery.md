---
lab:
    title: 'Erkunden des Core eDiscovery-Workflows'
    module: 'Modul 4, Lektion 4: Beschreiben der Funktionen der Microsoft-Compliancelösungen: Beschreiben der eDiscovery- und Überwachungsfunktionen in Microsoft 365'
---


# Lab: Erkunden des Core eDiscovery-Workflows

## Labszenario
In diesem Lab gehen Sie die zum Einrichten von Core eDiscovery erforderlichen Schritte und den Core eDiscovery-Workflow durch. Dazu erstellen Sie eine eDiscovery-Aufbewahrung und Suchabfrage und exportieren die Suchergebnisse anschließend.  Hinweis:  Für die Lizenzierung von Core eDiscovery sind das entsprechende Organisationsabonnement und die benutzerbezogene Lizenzierung erforderlich. Wenn Sie nicht sicher sind, welche Lizenzen Core eDiscovery abdecken, rufen Sie „Erste Schritte mit Core eDiscovery“ auf.


**Geschätzte Dauer**: 20–25 Minuten

#### Aufgabe 1:  Benutzer benötigen die entsprechenden Berechtigungen, um auf Core eDiscovery zugreifen oder als Mitglied zu einem Core eDiscovery-Fall hinzugefügt werden zu können. Bei dieser Aufgabe fügen Sie als globaler Administrator bestimmte Benutzer als Mitglieder der Rollgengruppe "eDiscovery-Manager" hinzu.

 Öffnen Sie Microsoft Edge. Geben Sie **admin.microsoft.com** in die Adressleiste ein.

1. Melden Sie sich mit Ihren Administratoranmeldeinformationen an.
    1. Geben Sie **admin@WWLxZZZZZZ.onmicrosoft.com** (ZZZZZZ ist hierbei die eindeutige Mandanten-ID, die von Ihrem Labhostinganbieter bereitgestellt wurde) in das Fenster „Anmelden“ ein, und wählen Sie dann **Weiter** aus.
    
    1. Geben Sie das Administratorkennwort ein, das Sie vom Labhostinganbieter erhalten haben sollten. Wählen Sie **Anmelden** aus.
    1. Wählen Sie **Ja** aus, wenn Sie gefragt werden, ob Sie angemeldet bleiben möchten. Dadurch gelangen Sie zur Seite „Microsoft 365 Admin Center“.

1. Wählen Sie im linken Navigationsbereich von Microsoft 365 Admin Center **Alle anzeigen** aus.

1. Wählen Sie **Sicherheit** unter „Admin Center“ aus.  Die Startseite des Microsoft 365 Defender-Portals wird auf einer neuen Browserseite geöffnet.  

1. Wählen Sie im linken Navigationsbereich des Microsoft 365 Defender-Portals die Option **Berechtigungen und Rollen** aus.  Es kann sein, dass Sie nach unten scrollen müssen, damit diese Option angezeigt wird.

1. Wählen Sie auf der Seite „Berechtigungen und Rollen“ unter **Rollen für E-Mail und Zusammenarbeit** die Option **Rollen** aus.

1. Geben Sie **eDiscovery** in die Suchleiste ein. Wählen Sie dann das Suchsymbol (Lupe) aus.  Wählen Sie **eDiscovery-Manager** aus.

1. Beachten Sie im Fenster, das geöffnet wird, die zwei Untergruppen: „eDiscovery-Manager“ und „eDiscovery-Administrator“.  Lesen Sie die jeweilige Beschreibung.  In diesem Lab fügen wir der Untergruppe „eDiscovery-Administrator“ Mitglieder hinzu. Wählen Sie **Bearbeiten** neben „eDiscovery-Administrator“ aus.  Als allgemein bewährte Methode empfiehlt es sich, Benutzern die niedrigste Berechtigung zuzuweisen, die für ihre Rolle erforderlich ist.

1. Wählen Sie die Registerkarte **eDiscovery-Administrator auswählen** und dann **eDiscovery-Administrator auswählen** aus, um dieser Rollengruppe Mitglieder hinzuzufügen.

1. Wählen Sie oben auf der Seite **+ hinzufügen** aus.

1. Wählen Sie in der Liste der Namen die Einträge **MOD-Administrator** und **Megan Bowen** aus. Wählen Sie dann unten auf der Seite die Option **Hinzufügen** und **Fertig** aus.

1. Überprüfen Sie, ob die hinzugefügten Mitglieder richtig sind, und wählen Sie dann **Speichern** aus.

1. Wählen Sie unten im Fenster „eDiscovery“ die Option **Schließen** aus.

1. Lassen Sie diese Browserregisterkarte geöffnet, da Sie in einer nachfolgenden Aufgabe dorthin zurückkehren werden.

#### Aufgabe 2:  Bei dieser Aufgabe erstellen Sie als ein eDiscovery-Administrator (der MOD-Administrator ist ein eDiscovery-Administrator) einen Fall, um mit der Verwendung von Core eDiscovery zu beginnen.

1. Öffnen Sie in Ihrem Browser die Registerkarte „Microsoft 365 Admin Center“.

1. Wählen Sie im linken Navigationsbereich unter „Admin Center“ die Option **Compliance** aus.

1. Sie befinden sich nun in Microsoft 365 Compliance Center. Wählen Sie im linken Navigationsbereich **Alle anzeigen** aus.

1. Wählen Sie im linken Navigationsbereich unter „Lösungen“ die Optionen **eDiscovery** und **Core** aus.

1. Wählen Sie oben auf der Seite „Core eDiscovery“ die Option **+ Fall erstellen** aus.

1. Geben Sie in das Fenster „Neuer Fall“ den Fallnamen **SC900-Testfall** ein. Wählen Sie dann unten auf der Seite **Speichern** aus.

1. Der Fall sollte nun in der Liste angezeigt werden. 

1. Da Sie den Fall erstellt haben und über eDiscovery-Administrator-Berechtigungen verfügen, können Sie ihn bearbeiten.  

1. Lassen Sie diese Browserregisterkarte geöffnet, da Sie sie in der nachfolgenden Aufgabe verwenden werden.

#### Aufgabe 3:  Nun können Sie den von Ihnen erstellten Core eDiscovery-Fall bearbeiten.  Bei dieser Aufgabe erstellen Sie eine eDiscovery-Aufbewahrung für den von Ihnen soeben erstellten Fall.  Insbesondere erstellen Sie dabei eine Aufbewahrung für das Exchange-Postfach von Adele Vance.

1. Öffnen Sie in Ihrem Browser die Registerkarte „Core eDiscovery“.

1. Wählen Sie auf der Seite „Core eDiscovery“ den Fall **SC900-Testfall** aus, den Sie auf der vorherigen Registerkarte erstellt haben. 

1. Wählen Sie auf der Startseite des Falls die Registerkarte **Aufbewahrung** und dann **+ Erstellen** aus.

1. Geben Sie im Feld „Name“ den Text **Testaufbewahrung** ein, und wählen Sie dann „Weiter“ aus.

1. Wählen Sie auf der Seite „Speicherorte auswählen“ den neben „Exchange-E-Mail“ befindlichen Umschalter aus, um den Status auf **Ein** festzulegen, wählen Sie **Benutzer, Gruppen oder Teams auswählen** aus.  Geben Sie **Adele** in das Suchfeld ein, und drücken Sie dann die EINGABETASTE auf Ihrer Tastatur. Wählen Sie in den Suchergebnissen den Eintrag **Adele Vance** aus. Wählen Sie dann „Auswählen“ und **Fertig** aus.

1. Wählen Sie auf der Seite „Speicherorte auswählen“ die Option **Weiter** aus.  Aus Zweckmäßigkeitsgründen sind im Lab bei dieser Aufbewahrung keine anderen Speicherorte enthalten.

1. Auf der Seite „Abfragebedingungen“ können Sie eine Aufbewahrung erstellen, die auf bestimmten erfüllten Schlüsselwörtern oder Bedingungen basiert. Wählen Sie **+ Bedingungen** aus, um die verfügbaren Optionen anzuzeigen.  Klicken Sie dann auf **Weiter**. Sind keine Bedingungen vorhanden, behält die Aufbewahrung alle Inhalte am angegebenen Speicherort bei.

1. Überprüfen Sie Ihre Einstellungen, und wählen Sie **Senden** aus. Es kann eine Minute dauern. Wählen Sie dann **Fertig** aus.  „Testaufbewahrung“ sollte in der Liste angezeigt werden.  Wenn es nicht sofort angezeigt wird, wählen Sie **Aktualisieren** aus.

1. Lassen Sie diese Browserregisterkarte geöffnet, da Sie sie in der nachfolgenden Aufgabe verwenden werden.

#### Aufgabe 4:  Erstellen Sie bei vorhandener Aufbewahrung eine Suchabfrage.  Nach Abschluss Ihrer Suche exportieren und laden Sie die Ergebnisse zur künftigen Untersuchung herunter.   Hinweis:  Die einem Core eDiscovery-Fall zugeordneten Suchen werden auf der Seite „Inhaltssuche“ in Microsoft 365 Compliance Center nicht aufgelistet. Diese Suchen werden lediglich auf der Seite „Suchen“ des zugeordneten Core eDiscovery-Falls aufgelistet.

1. Öffnen Sie in Ihrem Browser die Registerkarte „SC900-Testfall“.

1. Wählen Sie auf der Seite „Aufbewahrung“ des Falls die Option **Suchen** aus.

1. Wählen Sie auf der Seite „Suche“ die Option **+ Neue Suche** aus.

1. Geben Sie in das Feld „Name“ den Text **Testaufbewahrung – Vertriebssuche** ein. Wählen Sie dann unten auf der Seite **Weiter** aus.

1. Wählen Sie auf der Seite „Speicherorte auswählen“ den neben „Exchange-E-Mail“ befindlichen Umschalter aus, um den Status auf **Ein** festzulegen, wählen Sie **Benutzer, Gruppen oder Teams auswählen** aus.  Geben Sie **Adele** in das Suchfeld ein, und drücken Sie dann die EINGABETASTE auf Ihrer Tastatur. Wählen Sie in den Suchergebnissen den Eintrag **Adele Vance** aus. Wählen Sie **Fertig** und dann **Weiter** aus.  Bei dieser Suche sind keine anderen Speicherorte enthalten.

1. Auf der Seite „Abfragebedingungen“ können Sie eine Suche erstellen, die auf bestimmten erfüllten Schlüsselwörtern oder Bedingungen basiert. Geben Sie in das Feld „Schlüsselwort“ den Text **Vertrieb** ein, und wählen Sie **Weiter** aus.

1. Überprüfen Sie Ihre Einstellungen, und wählen Sie **Senden** aus. Es kann eine Minute dauern. Wählen Sie dann **Fertig** aus.  Das Suchelement sollte in der Liste angezeigt werden.  Wenn es nicht sofort angezeigt wird, wählen Sie **Aktualisieren** aus.

1. Wählen Sie im Fenster „Suchen“ die von Ihnen soeben erstellte Suche **Testaufbewahrung – Vertriebssuche** aus.  Es wird ein Fenster geöffnet, in dem die Registerkarte „Zusammenfassung“ ausgewählt ist.  Nach Abschluss der Suche gibt der Status an, dass sie abgeschlossen ist.  Es wird die Registerkarte „Suchstatistik“ angezeigt (falls die Registerkarte „Suchstatistik“ nicht angezeigt wird, kann es sein, dass die Suche noch ausgeführt wird und ihr Abschluss möglicherweise noch ein paar Minuten dauert).  Wählen Sie die Registerkarte **Suchstatistik** und das Dropdown neben „Inhaltssuche“ aus.  Zudem können Sie weitere Informationen für „Bedingungsbericht“ und „Top-Orte“ anzeigen.  

1. Wählen Sie unten auf der Seite **Aktionen** aus.  Beachten Sie die verfügbaren Optionen, und wählen Sie dann **Ergebnisse exportieren** aus.
    
    1. Übernehmen Sie im Fenster „Ergebnisse exportieren“ die Standardeinstellungen, und wählen Sie unten auf der Seite **Exportieren** aus. Sie gelangen automatisch zum Fenster „Testaufbewahrung – Vertriebssuche“ zurück. Wählen Sie unten auf der Seite **Schließen** aus.
    
    1. Wählen Sie oben auf der Seite „SC900-Testfall“ die Option **Exporte** aus.
    1. Wählen Sie **Testaufbewahrung – Vertriebssuche_Exportieren** aus.
    1. Im Fenster „Testaufbewahrung – Vertriebssuche_Exportieren“, das geöffnet wird, wird ein Exportschlüssel angezeigt. Wählen Sie **In Zwischenablage kopieren** aus.
    1. Wählen Sie oben im Fenster **Ergebnisse herunterladen** aus. Eine neue Browserseite wird geöffnet. Zudem werden Sie in einem angezeigten Popupfenster gefragt, ob Sie diese Datei öffnen möchten. Wählen Sie **Öffnen** aus.
    1. Beim ersten Herunterladen einer Inhaltssuche werden Sie aufgefordert, das eDiscovery-Exporttool von Microsoft Office 365 zu installieren.  Wählen Sie **Installieren** aus.
    1. Nach Abschluss der Installation wird das Fenster für das eDiscovery-Exporttool geöffnet.  Fügen Sie den in die Zwischenablage kopierten Exportschlüssel in das erste Feld ein (drücken Sie STRG+V auf Ihrer Tastatur, oder klicken Sie mit der rechten Maustaste, und wählen Sie „Einfügen“ aus).
    1. Wählen Sie im zweiten Feld den Speicherort aus, an dem die Exportdatei gespeichert werden soll, und wählen Sie dann **Start** aus.  Wählen Sie nach Abschluss des Downloadprozesses **Schließen** aus, und schließen Sie diese Browserregisterkarte.
    1. Sie befinden sich wieder im Fenster „Testaufbewahrung – Vertriebssuche_Exportieren“.  Wählen Sie **Schließen** aus.
    1. Überprüfen Sie den Downloadspeicherort, um sicherzustellen, dass der Download erfolgreich abgeschlossen wurde. 


#### Überprüfung

In diesem Lab sind Sie die ersten Schritte für Core eDiscovery durchgegangen, darunter das Einstellen von Rollenberechtigungen für eDiscovery und das Erstellen eines eDiscovery-Falls.  Nach dem Erstellen des Falls sind Sie den Core eDiscovery-Workflow durchgegangen. Dazu haben Sie eine eDiscovery-Aufbewahrung und Suchabfrage erstellt und anschließend die Suchergebnisse exportiert, um sie für die weitergehende Untersuchung zu verwenden.
