<a name="---"></a><!---
---
Demo: Title: 'Microsoft Sentinel' Learning Path/Module/Title: 'Lernpfad: Beschreiben der Funktionen von Microsoft-Sicherheitslösungen; Modul 3: Beschreiben der Sicherheitsfunktionen von Microsoft Sentinel; Lerneinheit 3: Erklären des integrierten Bedrohungsmanagements von Microsoft Sentinel'
---
--->

# <a name="demo-microsoft-sentinel"></a>Demo: Microsoft Sentinel

Diese Demo ist den folgenden Learn-Inhalten zugeordnet:

- Lernpfad: Beschreiben der Funktionen von Microsoft-Sicherheitslösungen
- Modul: Beschreiben der Sicherheitsfunktionen von Microsoft Sentinel
- Lerneinheit: Erklären des integrierten Bedrohungsmanagements von Microsoft Sentinel

## <a name="demo-scenario"></a>Demoszenario

In dieser Demo durchlaufen Sie den Prozess der Erstellung einer Microsoft Sentinel-Instanz.  Zudem richten Sie die Berechtigungen ein, um den Zugriff auf die Ressourcen sicherzustellen, die zur Unterstützung von Microsoft Sentinel bereitgestellt werden.  Sobald diese grundlegende Einrichtung abgeschlossen ist, führen Sie die Schritte zum Verbinden von Microsoft Sentinel mit Ihren Datenquellen aus und wählen eine Arbeitsmappe aus, um Ihre Daten zu überwachen und zu visualisieren.  Abschließend sehen Sie sich einige weitere verfügbare Optionen an, z. B. die integrierte Analyse, die Sie bei verdächtigen Aktivitäten benachrichtigt, die Automatisierungsfunktion und vieles mehr.

### <a name="pre-demo-setup--create-a-microsoft-sentinel-instance"></a>Einrichtung vor der Demo: Erstellen einer Microsoft Sentinel-Instanz

1. Öffnen Sie die Browserregisterkarte **Startseite – Microsoft Azure**.  Falls Sie die Registerkarte geschlossen haben, öffnen Sie eine Browserseite. Geben Sie „portal.azure.com“ in die Adressleiste ein, und melden Sie sich erneut an.

1. Geben Sie in das Suchfeld, das sich auf dem blauen Balken oben auf der Seite neben dem Text „Microsoft Azure“ befindet, den Text **Microsoft Sentinel** ein, und wählen Sie dann **Microsoft Sentinel** in den Suchergebnissen aus.

1. Wählen Sie auf der Seite „Microsoft Sentinel“ die Option **Microsoft Sentinel erstellen** aus.

1. Wählen Sie auf der Seite zum Hinzufügen von Microsoft Sentinel zu einem Arbeitsbereich die Option **Neuen Arbeitsbereich erstellen** aus.

1. Geben Sie auf der Registerkarte „Grundlagen“ von „Log Analytics-Arbeitsbereich erstellen“ Folgendes ein:
    1. Abonnement: Übernehmen Sie die Standardeinstellung.
    1. Ressourcengruppe: Wählen Sie **Neu erstellen** aus, geben Sie dann den Namen **SC900-Sentinel-RG** ein, und wählen Sie **OK** aus.
    1. Name: **SC900-LogAnalytics-workspace**.
    1. Region: **East US** (Sie können eine andere Standardregion basierend auf Ihrem Standort auswählen)
    1. Wählen Sie **Überprüfen und erstellen** aus (es werden keine Tags konfiguriert).
    1. Überprüfen Sie Ihre eingegebenen Informationen, und wählen Sie dann **Erstellen** aus.
    1. Es kann eine oder zwei Minuten dauern, bis der Arbeitsbereich aufgelistet wird. Wenn er weiterhin nicht angezeigt wird, wählen Sie **Aktualisieren** und dann **Hinzufügen** aus.

1. Nachdem der neue Arbeitsbereich hinzugefügt wurde, wird die Seite „Microsoft Sentinel | News und Leitfäden“ angezeigt, die angibt, dass die kostenlose Microsoft Sentinel-Testversion aktiviert ist.  Klicken Sie auf **OK**.  Beachten Sie die drei auf der Seite „Erste Schritte“ aufgelisteten Schritte.

1. Lassen Sie diese Seite geöffnet, da Sie sie in der nächsten Aufgabe verwenden werden.

### <a name="demo-part-2"></a>Teil 2 der Demo

Nachdem Sie die Microsoft Sentinel-Instanz erstellt haben, möchten Sie sicherstellen, dass Sie über den erforderlichen Zugriff auf die Ressourcen verfügen, die zum Unterstützen von Microsoft Sentinel bereitgestellt werden.  

1. Geben Sie in das Suchfeld, das sich auf dem blauen Balken oben auf der Seite neben dem Text „Microsoft Azure“ befindet, den Text **Ressourcengruppen** ein, und wählen Sie dann **Ressourcengruppen** aus den Suchergebnissen aus. Durch das Zuweisen der Rolle auf der Ressourcengruppenebene wird sichergestellt, dass die Rolle für alle Ressourcen gilt, die zum Unterstützen von Microsoft Sentinel bereitgestellt werden.

1. Wählen Sie auf der Seite „Ressourcengruppen“ die von Ihnen mit Microsoft Sentinel erstellte Ressourcengruppe aus, nämlich **SC900-Sentinel-RG**.

1. Wählen Sie auf der Seite „SC900-Sentinel-RG“ im linken Navigationsbereich die Option **Zugriffssteuerung (IAM)** aus.

1. Wählen Sie auf der Seite „Zugriffssteuerung“ die Option **Meinen Zugriff anzeigen** aus.  Für den MOD-Administrator ist die aktuelle Rolle „Dienstadministrator“.  Dadurch erhalten Sie die erforderlichen Berechtigungen, aber für Demozwecke sollten Sie die Sentinel-spezifischen Rollen anzeigen.  Wählen Sie zum Schließen des Fensters für die MOD-Administratorzuweisungen das **X** aus, das sich in der oberen rechten Ecke des Fensters befindet.

    1. Wählen Sie auf der Seite „Zugriffssteuerung“ die Option **+ Hinzufügen** und dann **Rollenzuweisung hinzufügen** aus.

    1. Das Fenster „Rollenzuweisung hinzufügen“ wird geöffnet.  Geben Sie **Microsoft Sentinel** in das Suchfeld ein, um die vier Rollen anzuzeigen, die Microsoft Sentinel zugeordnet sind.
    1. Wählen Sie in einer der aufgeführten Rollen **Anzeigen** aus, um die Details dieser Rolle anzuzeigen.  Als bewährte Methode empfiehlt es sich, die niedrigste Berechtigung zuzuweisen, die für die Rolle erforderlich ist.  

    1. Schließen Sie das Fenster. Wählen Sie dazu in der oberen rechten Ecke des Fensters das **X** aus.

1. Schließen Sie auf der Zugriffssteuerungsseite das Fenster, indem Sie in der oberen rechten Ecke des Fensters das **X** auswählen.

### <a name="demo-part-3"></a>Teil 3 der Demo

In diesem Teil der Demo zeigen Sie die Schritte zum Herstellen einer Verbindung mit einer Datenquelle.  Insbesondere stellen Sie eine Verbindung mit dem Microsoft Defender for Cloud-Datenconnector her.

1. Geben Sie in das Suchfeld, das sich auf dem blauen Balken oben auf der Seite neben dem Text „Microsoft Azure“ befindet, den Text **Microsoft Sentinel** ein, und wählen Sie dann **Microsoft Sentinel** in den Suchergebnissen aus.

1. Wählen Sie auf der Seite „Microsoft Sentinel“ den von Ihnen mit der Microsoft Sentinel-Instanz erstellten Arbeitsbereich aus, nämlich **SC900-LogAnalytics-workspace**.

1. Der erste Schritt mit Microsoft Sentinel besteht darin, Daten sammeln zu können. Wählen Sie im linken Navigationsbereich die unter der Konfiguration aufgelistete Option **Datenconnectors** aus.

1. Scrollen Sie auf der Seite „Datenconnectors“ nach unten zum Hauptfenster, um die ausführliche Liste mit den verfügbaren Connectors anzuzeigen. Geben Sie auf der Seite „Datenconnectors“ im Suchfeld **Microsoft Defender for Cloud** ein, und wählen Sie dann in der Liste **Microsoft Defender for Cloud** aus.

1. Das Fenster „Microsoft Defender for Cloud-Connector“ wird geöffnet. Überprüfen Sie die Beschreibung, und wählen Sie dann **Connectorseite öffnen** aus.

1. Lesen Sie auf der Seite „Microsoft Defender for Cloud-Connector“ die Beschreibung auf der linken Seite des Fensters.

1. Die Registerkarte „Anweisungen“ im Hauptfenster enthält die Voraussetzungen.  Überprüfen Sie die Anweisungen und Konfigurationsinformationen.
    Die Registerkarte „Anweisungen“ im Hauptfenster enthält die Voraussetzungen.  Überprüfen Sie die Anweisungen und Konfigurationsinformationen.
    1. Aktivieren Sie im Konfigurationsabschnitt das leere Kontrollkästchen neben dem aufgelisteten Abonnement (**MOC-Abonnement--lodXXXXXXXX**), damit ein Häkchen in einem blauen Feld angezeigt wird, und wählen Sie dann **Verbinden** aus (die Option „Verbinden“ wird über dem Suchfeld angezeigt).  Ein Fenster „Verbinden“ wird angezeigt. Wählen Sie **OK** aus.  In der Statusspalte sollte neben dem Abonnement der Status in „Verbunden“ aktualisiert werden.  Machen Sie sich keine Gedanken, wenn der Verbindungsstatus nicht im Fenster links auf der Seite angezeigt wird. Aktualisieren Sie den Browser NICHT.
    1. Scrollen Sie auf der Seite nach unten, und wählen Sie **Aktivieren** aus, um Incidents automatisch aus allen Warnungen zu erstellen, die im verbundenen Dienst generiert werden.
    1. Wählen Sie nun oben auf der Seite die Registerkarte **Nächste Schritte** aus, um empfohlene Arbeitsmappen für diesen Datenconnector anzuzeigen.  Microsoft Sentinel verfügt über integrierte Arbeitsmappenvorlagen, mit denen Sie schnell Einblicke in Ihre Daten gewinnen können, sobald Sie eine Verbindung mit einer Datenquelle herstellen.
    1. Wählen Sie **ASC-Compliance und -Schutz** aus (Hinweis: ASC oder Azure Security Center heißt jetzt Microsoft Defender for Cloud).  Dadurch wird die Seite „Arbeitsmappen“ geöffnet.  Lesen Sie die Beschreibung auf der rechten Seite des Bildschirms, und wählen Sie dann unten auf dem Bildschirm **Speichern** und danach **OK** aus, um die Arbeitsmappe im Standardspeicherort zu speichern.  Wählen Sie jetzt **Gespeicherte Arbeitsmappe anzeigen** aus.  
    1. Wählen Sie im Feld „Arbeitsbereich“ **SC900-LogAnalytics-workspace** aus.
    1. Wählen Sie oben auf der Seite „Arbeitsmappe“ die Option **Automatische Aktualisierung: Aus** aus, und wählen Sie dann **5 Minuten** und **Anwenden** aus.
    1. Wählen Sie oben auf der Seite „Arbeitsmappe“ das **Speichersymbol** aus.
    1. Wählen Sie in der oberen linken Ecke der Seite „Arbeitsmappe“ oberhalb des Texts „Arbeitsmappen“ die Option **Microsoft Sentinel** aus. Damit werden Sie zur Seite „Übersicht“ zurückgeleitet. Nun sollte die Zahl 1 über dem Status „Verbunden“ angezeigt werden, um einen aktiven Connector anzugeben (möglicherweise müssen Sie die Seite aktualisieren).

1. Lassen Sie diese Seite geöffnet, da Sie sie in der nächsten Aufgabe verwenden werden.

### <a name="demo-part-4"></a>Teil 4 der Demo

In diesem Teil der Demo zeigen Sie einige der Optionen, die in Sentinel verfügbar sind.

1. Wählen Sie im linken Navigationsbereich **Hunting** aus.  Wählen Sie auf der Registerkarte **Abfragen**, die ausgewählt (unterstrichen) ist, eine beliebige Abfrage aus der Liste aus.  Beachten Sie nach der Auswahl der Abfrage die Informationen, die zu dieser Abfrage bereitgestellt werden, z. B. den Code für die Abfrage sowie die Option zum Ausführen der Abfrage und Anzeigen der Ergebnisse.  Wählen Sie nichts aus.

1. Wählen Sie im linken Navigationsbereich **MITRE ATT&CK** aus.  MITRE ATT&CK ist eine öffentlich zugängliche Wissensdatenbank mit Taktiken und Techniken, die häufig von Angreifern verwendet werden. Mit Microsoft Sentinel können Sie die Erkennungen anzeigen, die bereits in Ihrem Arbeitsbereich aktiv sind, sowie diejenigen, die Ihnen zur Konfiguration zur Verfügung stehen. So erhalten Sie einen Überblick über die Sicherheitsmaßnahmen in Ihrer Organisation, basierend auf den Taktiken und Techniken des MITRE ATT&CK®-Frameworks.  Wählen Sie eine beliebige Zelle aus der Matrix aus, und beachten Sie die Informationen auf der rechten Seite des Bildschirms.  

1. Wählen Sie im linken Navigationsbereich **Community** aus. Die Sicherheitsanalysten von Microsoft erstellen laufend neue Arbeitsmappen, Playbooks, Hunting-Abfragen usw., die in der Community veröffentlicht werden und Ihnen zur Verwendung in Ihrer Umgebung zur Verfügung stehen. Sie können Beispielinhalte aus dem privaten GitHub-Repository der Community herunterladen, um benutzerdefinierte Arbeitsmappen, Suchabfragen, Notebooks und Playbooks für Microsoft Sentinel zu erstellen.  Wählen Sie **Communityinhalt integrieren** aus.  Eine neue Registerkarte mit dem GitHub-Repository wird geöffnet. Von dort können Sie Inhalte herunterladen, um Ihre Szenarien zu aktivieren.  Kehren Sie in Ihrem Browser zur Azure-Registerkarte zurück.

1. Wählen Sie im linken Navigationsbereich **Analysen** aus.  Wählen Sie das erste Element aus der Liste **Erweiterte Erkennung mehrstufiger Angriffe** aus.  Lesen Sie die ausführlichen Informationen.  Microsoft Sentinel verwendet Fusion, eine Korrelations-Engine, die auf skalierbaren Algorithmen des maschinellen Lernens basiert, um automatisch mehrstufige Angriffe (auch als erweiterte persistente Bedrohungen bezeichnet) zu erkennen, indem Kombinationen aus anomalem Verhalten und verdächtigen Aktivitäten identifiziert werden, die in verschiedenen Phasen der Kill Chain beobachtet werden. Auf der Grundlage dieser Entdeckungen generiert Microsoft Sentinel Incidents, die auf andere Weise nur schwer abgefangen werden können.

1. Wählen Sie im linken Navigationsbereich **Automation** aus.  Hier können Sie ganz einfach Automatisierungsregeln erstellen und in vorhandene Playbooks integrieren oder neue Playbooks erstellen.  Wählen Sie **+Erstellen** und dann **Automatisierungsregel** aus.  Beachten Sie das Fenster, das auf der rechten Seite des Bildschirms geöffnet wird, und die dort verfügbaren Optionen zum Erstellen von Bedingungen und Aktionen.  Wählen Sie unten auf der Bildschirm **Abbrechen** aus.

1. Wählen Sie im linken Navigationsbereich **Arbeitsmappen** aus. Wählen Sie auf der Seite „Arbeitsmappen“ die Registerkarte **Meine Arbeitsmappen** aus, die sich oberhalb des Suchfelds befindet.  Die von Ihnen zuvor gespeicherte Arbeitsmappe wird aufgelistet und steht Ihnen zum Anzeigen und Überwachen Ihrer Daten zur Verfügung.   HINWEIS: Im Azure-Abonnement findet keine wirkliche Aktivität statt, die in der Arbeitsmappe widergespiegelt werden könnte, und bei Azure-Lab-Abonnements kann es zu größeren als den üblichen Verzögerungen bei der Erfassung von Daten kommen, die in der Arbeitsmappe visualisiert werden können.

1. Schließen Sie das Fenster. Wählen Sie dazu in der oberen rechten Ecke des Fensters das **X** aus.

1. Wählen Sie in der oberen linken Ecke des Fensters direkt unterhalb der blauen Leiste die Option **Startseite** aus, um zur Startseite des Azure-Portals zurückzukehren.  

### <a name="review"></a>Überprüfung

In dieser Demo haben Sie die Schritte zum Verbinden von Microsoft Sentinel mit Datenquellen ausgeführt, eine Arbeitsmappe eingerichtet und sich verschiedene in Microsoft Sentinel verfügbare Optionen angesehen.
