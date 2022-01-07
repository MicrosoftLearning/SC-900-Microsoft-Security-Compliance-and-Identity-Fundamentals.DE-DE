---
Demo:
    title: 'Microsoft Sentinel'
    module: 'Modul 3, Lektion 3: Beschreiben der Funktionen der Microsoft-Sicherheitslösungen: Beschreiben der Sicherheitsfunktionen von Microsoft Sentinel'
---


# Demo: Microsoft Sentinel 

### Demoszenario
In dieser Demo gehen Sie den Prozess des Erstellens einer Microsoft Sentinel-Instanz durch.  Außerdem richten Sie die Berechtigungen ein, um Zugriff auf die Ressourcen sicherzustellen, die zur Unterstützung von Microsoft Sentinel bereitgestellt werden.  Nachdem diese grundlegende Einrichtung abgeschlossen ist, durchlaufen Sie die Schritte zum Verbinden von Microsoft Sentinel mit Ihren Datenquellen und die Verwendung integrierter Analysen, damit Sie über alle verdächtigen Aktivitäten benachrichtigt werden. Schließlich erkunden Sie die Automatisierungsfunktion.  

#### Teil 1 der Demo:  Erstellen einer Microsoft Sentinel-Instanz

1. Öffnen Sie die Browserregisterkarte **Startseite – Microsoft Azure**.  Falls Sie die Registerkarte geschlossen haben, öffnen Sie eine Browserseite. Geben Sie „portal.azure.com“ in die Adressleiste ein, und melden Sie sich erneut an.

1. Geben Sie in das Suchfeld, das sich auf dem blauen Balken oben auf der Seite neben dem Text „Microsoft Azure“ befindet, den Text **Microsoft Sentinel** ein, und wählen Sie dann **Microsoft Sentinel** aus den Suchergebnissen aus.

1. Wählen Sie auf der Microsoft Sentinel-Seite die Option **Microsoft Sentinel erstellen** aus.

1. Wählen Sie unter „Microsoft Sentinel zu einer Arbeitsbereichsseite hinzufügen“ die Option **Neuen Arbeitsbereich erstellen** aus.

1. Geben Sie auf der Registerkarte „Grundlagen“ von „Log Analytics-Arbeitsbereich erstellen“ Folgendes ein:
    1. Abonnement:  **Azure Pass-Förderung**
    1. Ressourcengruppe: Wählen Sie **Neu erstellen** aus, geben Sie dann den Namen **SC900-Sentinel-RG** ein, und wählen Sie **OK** aus.
    1. Name: **SC900-LogAnalytics-workspace**.
    1. Region: **East US** (übernehmen Sie diesen Standardwert).
    1. Wählen Sie **Weiter: „Tarif >“ aus.**

1. Übernehmen Sie für „Tarif“ die Standardeinstellungen: **Nutzungsbasierte Bezahlung (Pro GB 2018)**. Wählen Sie dann **Weiter: Tags >** aus.

1. Für „Tags“ können Sie dies leer lassen. Wählen Sie dann **Bewerten + erstellen** aus.

1. Überprüfen Sie Ihre eingegebenen Informationen, und wählen Sie dann **Erstellen** aus.

1. Es kann eine oder zwei Minuten dauern, bis der Arbeitsbereich aufgelistet wird. Wenn er weiterhin nicht angezeigt wird, wählen Sie **Aktualisieren** und dann **Hinzufügen** aus.

1. Nachdem der neue Arbeitsbereich hinzugefügt wurde, wird die Microsoft Sentinel-Seite | mit Neuigkeiten und Leitfäden angezeigt.  Beachten Sie die drei auf der Seite „Erste Schritte“ aufgelisteten Schritte.

1. Lassen Sie diese Seite geöffnet, da Sie sie in der nächsten Aufgabe verwenden werden.

#### Teil 2 der Demo:  Nachdem Sie die Microsoft Sentinel-Instanz erstellt haben, sollten Sie sicherstellen, dass Sie über den nötigen Zugriff auf die Ressourcen verfügen, die zur Unterstützung von Microsoft Sentinel bereitgestellt werden.  In dieser Aufgaben rufen Sie die Seite für die Zugriffssteuerung (IAM) für die Ressourcengruppe auf, die Sie mit der Instanz von Microsoft Sentinel erstellt haben, zeigen die verfügbaren Rollen an und weisen sich selbst (MOD-Administrator) die erforderliche Rolle zu. Durch Zuweisen der Rolle auf Ressourcengruppenebene wird sichergestellt, dass die Rolle auf alle Ressourcengruppen angewendet wird, die zur Unterstützung von Microsoft Sentinel bereitgestellt werden.

1. Geben Sie in das Suchfeld, das sich auf dem blauen Balken oben auf der Seite neben dem Text „Microsoft Azure“ befindet, den Text **Ressourcengruppen** ein, und wählen Sie dann **Ressourcengruppen** aus den Suchergebnissen aus.

1. Wählen Sie auf der Seite mit den Ressourcengruppen die Ressourcengruppe aus, die Sie mit Microsoft Sentinel erstellt haben, und zwar **SC900-Sentinel-RG**.

1. Wählen Sie auf der Seite „SC900-Sentinel-RG“ im linken Navigationsbereich die Option **Zugriffssteuerung (IAM)** aus.

1. Wählen Sie auf der Seite „Zugriffssteuerung“ die Option **Meinen Zugriff anzeigen** aus.  Beachten Sie, dass die aktuelle Rolle „Dienstadministrator“ lautet.  Wählen Sie zum Schließen des Fensters für die MOD-Administratorzuweisungen das **X** aus, das sich in der oberen rechten Ecke des Fensters befindet.

1. Wählen Sie auf der Seite „Zugriffssteuerung“ die Option **+ Hinzufügen** und dann **Rollenzuweisung hinzufügen** aus.

1. Das Fenster „Rollenzuweisung hinzufügen“ wird geöffnet.  Wählen Sie den Dropdownpfeil im Feld „Rolle auswählen“ aus, um die verfügbaren Rollen anzuzeigen. Geben Sie im Suchfeld zum Auswählen einer Rolle **Microsoft Sentinel** ein, um die vier Rollen im Zusammenhang mit Microsoft Sentinel anzuzeigen. Als bewährte Methode empfiehlt es sich, die niedrigste Berechtigung zuzuweisen, die für die Rolle erforderlich ist.  Geben Sie in diesem Lab der Einfachheit halber in das Suchfeld den Text **Besitzer** ein, und wählen Sie **Besitzer** aus den Suchergebnissen aus.  Überprüfen Sie als Referenz die Berechtigungen in Microsoft Sentinel:  https://docs.microsoft.com/de-de/azure/sentinel/roles

1. Wählen Sie in der angezeigten Liste der Benutzer den Eintrag **MOD-Administrator** aus.

1. Wählen Sie unten auf der Seite **Speichern** aus.

1. Wählen Sie auf der Seite „Zugriffssteuerung“ die Option **Meinen Zugriff anzeigen** aus, um zu bestätigen, dass die Rolle hinzugefügt wurde. Schließen Sie dann das Fenster, indem Sie in der oberen rechten Ecke des Fensters das **X** auswählen.

#### Teil 3 der Demo:  In diesem Teil der Demo durchlaufen Sie den Prozess des Verbindens von Microsoft Sentinel mit Ihrer Datenquelle, um mit der Erfassung von Daten zu beginnen.  Hinweis: Es kann einige Zeit in Anspruch nehmen, bis der verbundene Status eines Connectors angezeigt wird (~ 30 Minuten, je nach Mandant).

1. Geben Sie in das Suchfeld, das sich auf dem blauen Balken oben auf der Seite neben dem Text „Microsoft Azure“ befindet, den Text **Microsoft Sentinel** ein, und wählen Sie dann **Microsoft Sentinel** aus den Suchergebnissen aus.

1. Wählen Sie auf der Microsoft Sentinel-Seite den Arbeitsbereich aus, den Sie mit der Instanz von Microsoft Sentinel erstellt haben, und zwar **SC900-LogAnalytics-workspace**.

1. Der erste Schritt besteht darin, mit Microsoft Sentinel Daten zu sammeln. Wählen Sie im linken Navigationsbereich die unter der Konfiguration aufgelistete Option **Datenconnectors** aus.

1. Scrollen Sie auf der Seite „Datenconnectors“ nach unten zum Hauptfenster, um die ausführliche Liste mit den verfügbaren Connectors anzuzeigen. Geben Sie in das Suchfeld der Seite „Datenconnectors“ den Text **Azure** ein. Wählen Sie dann in der Liste den Eintrag **Azure Active Directory** aus.

1. Das Fenster „Azure Active Directory Connector“ wird geöffnet.  Wählen Sie **Connectorseite öffnen** aus.

1. Überprüfen Sie auf der Azure Active Directory Connector-Seite die Beschreibung, und beachten Sie den zugehörigen Inhalt, der Arbeitsmappe, Abfragen und Regelvorlagen für Analysen umfasst.  

1. Die Registerkarte „Anweisungen“ im Hauptfenster liefert die Voraussetzungen für die Integration von Microsoft Sentinel in Azure Active Directory.   Wählen Sie unter „Konfiguration“ die Option **Anmeldeprotokolle** und dann „Änderungen anwenden“ (es können mehrere Connectors ausgewählt werden) aus.  Hinweis: Es kann einige Zeit in Anspruch nehmen, bis der verbundene Status für den Connector angezeigt wird (~ 30 Minuten oder so).  Als Referenz:
    1. Überprüfen Sie die Berechtigungen in Microsoft Sentinel:  https://docs.microsoft.com/de-de/azure/sentinel/roles
    1. Herstellen einer Verbindung mit Azure Active Directory:  https://docs.microsoft.com/de-de/azure/sentinel/connect-azure-active-directory

1. Beachten Sie auf der Registerkarte „Nächste Schritte“ die Liste mit den empfohlenen Arbeitsmappen.   Wählen Sie unter „Empfohlene Arbeitsmappen“ die Option **Azure-Anmeldeprotokolle** (es können zusätzliche Arbeitsmappen ausgewählt werden) aus.

1. Wählen Sie auf der Seite „Arbeitsmappen“ auf der ausgewählten (unterstrichenen) Registerkarte „Vorlagen“ die Option **Azure-Anmeldeprotokolle** aus.

1. Überprüfen Sie im Fenster „Azure Active Directory-Anmeldeprotokolle“, das geöffnet wird, die Beschreibung, und wählen Sie **Vorlage anzeigen** aus.  Schließen Sie die Vorlage. Wählen Sie dazu in der oberen rechten Ecke des Bildschirms das **X** aus.  Wählen Sie unten auf der Seite **Speichern** aus. Wählen Sie dann **OK** aus, um die Arbeitsmappe am Standardspeicherort zu speichern.

1. Wählen Sie in der oberen linken Ecke der Seite „Arbeitsmappen“ oberhalb von „Arbeitsmappen“ die Option **Microsoft Sentinel** aus. Dadurch gelangen Sie zurück zur Seite mit den Microsoft Sentinel-Datenconnectors.

1. Oben auf der Seite „Datenconnectors“ sollte „1 verbunden“ angezeigt werden, um anzugeben, dass Sie nun mit Azure Active Directory verbunden sind.

1. Wählen Sie im linken Navigationsbereich **Arbeitsmappen** aus.

1. Wählen Sie auf der Seite „Arbeitsmappen“ die Registerkarte **Meine Arbeitsmappen** aus, die sich oberhalb des Suchfelds befindet.  Die von Ihnen soeben gespeicherte Arbeitsmappe wird aufgelistet und steht Ihnen zum Anzeigen und Überwachen Ihrer Daten zur Verfügung.  Nachfolgende Anmeldungen werden in der Arbeitsmappe angezeigt. Daher können Sie auswählen, dies anzuzeigen.

1. Lassen Sie diese Seite geöffnet, da Sie sie in der nächsten Aufgabe verwenden werden.

#### Teil 4 der Demo (optional):  Bei diesem Teil der Demo gehen Sie den Prozess der Verwendung einer integrierten Regelvorlage für Analysen durch, um eine Regel zu erstellen, damit Sie bei verdächtigen Aktivitäten benachrichtigt werden.

1. Wählen Sie im linken Navigationsbereich **Analysen** aus.

1. Auf der Seite „Analysen“ werden aktive Regeln („Erweiterte Erkennung von mehrstufigen Angriffen“ ist standardmäßig aktiviert) angezeigt. Außerdem bietet sie Zugriff auf „Regelvorlagen“.  Wählen Sie die Registerkarte **Regelvorlagen** aus.  Beachten Sie die Liste der verfügbaren Vorlagen und die unterschiedlichen Arten zum Filtern der Liste.  Über die integrierten Analysebenachrichtigungen innerhalb des Microsoft Sentinel-Arbeitsbereichs werden Sie benachrichtigt, wenn etwas Verdächtiges auftritt.

1. Geben Sie **Azure-Portal** in die Suchleiste ein.  Wählen Sie **Fehlgeschlagene Anmeldeversuche beim Azure-Portal** aus.  

1. Lesen Sie im Fenster, das geöffnet wird, die Beschreibung, und überprüfen Sie die der Vorlage zugeordneten Informationen.  Wählen Sie unten auf der Seite **Regel erstellen** aus.
    1. Überprüfen Sie im Assistenten für Analyseregeln die Informationen, und wählen Sie **Weiter: Regellogik festlegen >** aus.
    1. Auf der Seite „Regellogik festlegen“ definieren Sie die Logik für Ihre neue Analyseregel. Die Vorlage umfasst bereits eine gewisse Logik und vordefinierte Einstellungen.  Scrollen Sie durch die Seite, um die verfügbaren Einstellungen anzuzeigen.  Übernehmen Sie die Standardwerte. Wählen Sie **Weiter: Incidenteinstellungen (Vorschau) >** aus.
    1. Mit den Vorfallseinstellungen können Microsoft Sentinel-Benachrichtigungen zusammen in einem Vorfall gruppiert werden, der näher betrachtet werden sollte. Sie können festlegen, ob die durch diese Analyseregel ausgelösten Warnungen Incidents generieren sollen.  Übernehmen Sie die Standardeinstellungen, und wählen Sie **Weiter: Automatisierte Antwort >** aus.
    1. Beachten Sie auf der Registerkarte „Automatisierte Antwort“, wie Sie ein Playbook zum Automatisieren der Antwort hinzufügen können.  Ebenso können Sie eine Incidentautomatisierungsregel erstellen.  Wählen Sie **+ Neu hinzufügen** unter der Option für die Incidentautomatisierung aus.  Es wird ein Fenster zum Erstellen einer neuen Automatisierungsregel geöffnet.  Alle Automatisierungsregeln, die Sie auf dieser Seite erstellen, werden von der ursprünglich ausgewählten Analyseregel ausgelöst, in diesem Fall Fehlgeschlagene Anmeldeversuche beim Azure-Portal.  Beachten Sie, dass Sie Bedingungen hinzufügen und Aktionen für die Regel festlegen können.   Wählen Sie **Abbrechen** aus, um das Fenster zu schließen.
    1. Wählen Sie **Weiter: Überprüfen >** aus, um alle Details basierend auf der ausgewählten Vorlage zu überprüfen, die der Regel zugeordnet sind. An diesem Punkt können Sie die Regel erstellen, indem Sie **Erstellen** auswählen. Alternativ können Sie in der oberen rechten Ecke der Seite das **X** auswählen, um den Vorgang zu beenden, ohne die Regel zu erstellen.

1. Lassen Sie diese Seite geöffnet, da Sie sie in der nächsten Aufgabe verwenden werden.

#### Demo: Schritt 5 (optional):  Im vorherigen Schritt haben Sie eine Analyseregel erstellt, um gewarnt zu werden, wenn verdächtige Aktivitäten auftreten.  Dieser Assistent enthält die Option, um die Antwort basierend auf der bestimmten Regel für einen Incident zu automatisieren.  Sie können Automatisierungsregeln aber auch direkt über die Option für die Automatisierungskonfiguration erstellen.

1. Wählen Sie im linken Navigationsbereich **Automation** aus.  

1. Wählen Sie **+ Erstellen** aus. Beachten Sie im Dropdown, dass Sie entweder ein neues Playbook oder eine neue Regel hinzufügen können.  Wählen Sie **Neue Regel hinzufügen** aus.  
    1. Es wird ein Fenster zum Erstellen einer neuen Automatisierungsregel geöffnet.  Beachten Sie, dass Sie Bedingungen hinzufügen und Aktionen für die Regel festlegen können.  Der einzige Unterschied besteht darin, dass die erste Bedingung zum Zuordnen der Analyseregel(n) vorgesehen ist, auf die diese Automatisierungsregel angewendet werden soll(en).  Dies war in der vorherigen Aufgabe ausgegraut, da die Automatisierung für die bestimmte Regel konfiguriert wurde.  Wählen Sie **Abbrechen** aus, um das Fenster „Neue Automatisierungsregel erstellen“ zu schließen.

1. Lassen Sie diese Seite geöffnet, da Sie sie in der nächsten Aufgabe verwenden werden.

#### Schritt 6: Nachbereitung: Der Kursleiter soll diesen Schritt nach dem Kurs erledigen. Löschen Sie die Microsoft Sentinel-Ressourcengruppe.  Die Rechnung für Microsoft Sentinel wird auf Basis des Volumens erfasster Daten für die Analyse in Microsoft Sentinel ausgestellt. Die Menge erfasster Daten als Ergebnis dieses Labs ist zwar minimal, es wird aber empfohlen, dass Sie die Microsoft Sentinel-Ressourcengruppe löschen, wenn Sie mit dem Erkunden der Features von Funktionen von Microsoft Sentinel fertig sind.

1. Wählen Sie auf der Microsoft Sentinel-Seite in der oberen linken Ecke der Seite oberhalb von „Microsoft Sentinel“ die Option **Alle Dienste** aus.

1. Geben Sie die Ressourcengruppen in das Feld „Dienste filtern“ ein. Wählen Sie dann in der bereitgestellten Liste den Eintrag **Ressourcengruppen** aus.

1. Wählen Sie auf der Seite mit den Ressourcengruppen die Ressourcengruppe aus, die Sie mit Microsoft Sentinel erstellt haben, und zwar **SC900-Sentinel-RG**.

1. Wählen Sie im oberen mittleren Bereich der Seite die Option **Ressourcengruppe löschen** aus.  Überprüfen Sie die Warnung.  Geben Sie den Namen der Ressourcengruppe **SC900-Sentinel-RG** ein. Wählen Sie dann unten auf der Seite **Löschen** aus.  Es kann mehrere Minuten dauern, bis die Ressourcengruppe gelöscht ist.

1. Nachdem Sie die Löschung der Ressourcengruppe überprüft haben, schließen Sie die Browserseite. 

#### Überprüfung

In dieser Demo haben Sie den Prozess des Erstellens einer Microsoft Sentinel-Instanz gezeigt.  Sie haben gezeigt, wie die Berechtigungen eingerichtet werden, um Zugriff auf die Ressourcen sicherzustellen, die mit Ihrer Instanz von Microsoft Sentinel verknüpft sind.  Nachdem die Microsoft Sentinel-Instanz erstellt wurde, haben Sie die Schritte zum Verbinden von Microsoft Sentinel mit Datenquellen und die Verwendung integrierter Analyseregeln durchlaufen, damit Sie über alle verdächtigen Aktivitäten benachrichtigt werden. Als letzten Schritt haben Sie die Automatisierungsfunktion erkundet. Sie haben die Demo abgeschlossen, indem Sie die mit der Instanz von Microsoft Sentinel verknüpfte Ressourcengruppe, die Sie erstellt haben, gelöscht haben.