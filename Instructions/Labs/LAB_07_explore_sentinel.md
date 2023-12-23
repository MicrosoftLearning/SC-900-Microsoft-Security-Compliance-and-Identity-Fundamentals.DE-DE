<!---
---
Lab: Title: Erkunden von Microsoft Sentinel Lernpfad/Modul/Titel: Lernpfad: Beschreiben der Funktionen von Microsoft-Sicherheitslösungen; Modul 3: Beschreiben der Sicherheitsfunktionen von Microsoft Sentinel; Lerneinheit 3: Erklären des integrierten Bedrohungsmanagements von Microsoft Sentinel
---
--->

# Lab: Erkunden von Microsoft Sentinel

Dieses Lab ist den folgenden Learn-Inhalten zugeordnet:

- Lernpfad: Beschreiben der Funktionen von Microsoft-Sicherheitslösungen
- Modul: Beschreiben der Sicherheitsfunktionen von Microsoft Sentinel
- Lerneinheit: Beschreiben von Bedrohungserkennungs- und Risikominderungsfunktionen in Microsoft Sentinel

## Labszenario

Sie durchlaufen den Prozess der Erstellung einer Microsoft Sentinel-Instanz.  Zudem richten Sie Berechtigungen ein, um Zugriff auf die Ressourcen sicherzustellen, die zur Unterstützung von Microsoft Sentinel bereitgestellt werden.  Nachdem die grundlegende Einrichtung abgeschlossen ist, führen Sie die Schritte aus, die erforderlich sind, um Microsoft Sentinel mit Ihren Datenquellen zu verbinden und eine Arbeitsmappe einzurichten. Außerdem sehen Sie sich einige wichtigen Funktionen in Microsoft Sentinel an.

**Geschätzte Dauer**: 45 bis 60 Minuten

### Aufgabe 1

Erstellen einer Microsoft Sentinel-Instanz

1. Sie sollten sich auf der Startseite für Azure-Dienste befinden.  Wenn Sie den Browser zuvor geschlossen haben, öffnen Sie Microsoft Edge. Geben Sie **portal.azure.com** in die Adressleiste ein, und melden Sie sich mit Ihren Administratoranmeldeinformationen an.

1. Geben Sie in das blaue Suchfeld oben auf der Seite **Microsoft Sentinel** ein, und wählen Sie dann **Microsoft Sentinel** in den Suchergebnissen aus.

1. Wählen Sie auf der Seite „Microsoft Sentinel“ die Option **Microsoft Sentinel erstellen** aus.

1. Wählen Sie auf der Seite zum Hinzufügen von Microsoft Sentinel zu einem Arbeitsbereich die Option **Neuen Arbeitsbereich erstellen** aus.

1. Geben Sie auf der Registerkarte "Grundlagen" des Arbeitsbereichs "Log Analytics erstellen" Folgendes ein:
    1. Abonnement: Behalten Sie den Standardwert bei. Dies ist das Azure-Abonnement, das vom autorisierten Lab-Hoster (ALH) bereitgestellt wird.
    1. Ressourcengruppe: Wählen Sie **SC900-Sentinel-RG** aus. Wenn diese Ressourcengruppe nicht aufgeführt ist, erstellen Sie sie, indem Sie **Neu erstellen** auswählen, **SC900-Sentinel-RG** eingeben und dann **OK** auswählen.
    1. Name: **SC900-LogAnalytics-workspace**.
    1. Region: **USA, Osten** (Sie können eine andere Standardregion basierend auf Ihrem Standort auswählen)
    1. Wählen Sie **Überprüfen und erstellen** aus (es werden keine Tags konfiguriert).
    1. Vergewissern Sie sich, dass Sie die richtigen Informationen eingegeben haben, und wählen Sie dann **Erstellen** aus.
    1. Es kann eine oder zwei Minuten dauern, bis der ne-Arbeitsbereich aufgelistet wird, wenn sie immer noch nicht angezeigt wird, wählen Sie **Aktualisieren**und dann** Hinzufügen** aus.

1. Nachdem der neue Arbeitsbereich hinzugefügt wurde, wird die Seite „Microsoft Sentinel | News und Leitfäden“ angezeigt, die angibt, dass die kostenlose Microsoft Sentinel-Testversion aktiviert ist.  Klickan Sie auf **OK**.  Beachten Sie die drei Schritte, die auf der Seite "Erste Schritte" aufgeführt sind.

1. Lassen Sie diese Seite geöffnet, da Sie sie in der nächsten Aufgabe verwenden werden.

### Aufgabe 2

Nachdem die Microsoft Sentinel-Instanz erstellt wurde, ist es wichtig, dass Benutzer, die für die Unterstützung Microsoft Sentinel verantwortlich sind, über die erforderlichen Berechtigungen verfügen.  Dies geschieht, indem dem angegebenen Benutzer die erforderlichen Rollenberechtigungen zugewiesen werden.  In dieser Aufgabe zeigen Sie die verfügbaren integrierten Microsoft Sentinel-Rollen an.

1. Geben Sie in das blaue Suchfeld **Ressourcengruppen** ein, und wählen Sie dann **Ressourcengruppen** aus den Suchergebnissen aus. 

1. Wählen Sie auf der Seite „Ressourcengruppen“ die von Ihnen mit Microsoft Sentinel erstellte Ressourcengruppe aus, nämlich **SC900-Sentinel-RG**.  Wenn Sie auf Ressourcengruppenebene arbeiten, wird sichergestellt, dass jede ausgewählte Rolle auf alle Ressourcen angewendet wird, die Teil der Microsoft Sentinel-Instanz sind, die in der vorherigen Aufgabe erstellt wurde.

1. Auf der SC900-Sentinel-RG Seite, wählen Sie **Access Control (IAM)** aus dem linken Navigationsbereich.

1. Wählen Sie auf der Seite Access Control **Mein Zuriff ansehen**.  Für das Azure-Abonnement, das Ihnen vom autorisierten Lab-Hoster bereitgestellt wird, wurde eine Rolle definiert, die Ihnen Zugriff zum Verwalten aller erforderlichen Ressourcen gewährt, wie in der Beschreibung gezeigt. Es ist jedoch wichtig, die verfügbaren Sentinel-spezifischen Rollen zu verstehen.  Schließen Sie das Zuweisungsfenster, indem Sie in der oberen rechten Ecke des Fensters das **X** auswählen.

1. Wählen Sie auf der Seite „Zugriffssteuerung“ die Registerkarte **Rollen** oben auf der Seite aus.
    1. Geben Sie **Microsoft Sentinel** in das Suchfeld ein, um die integrierten Rollen anzuzeigen, die Microsoft Sentinel zugeordnet sind.
    1. Wählen Sie in einer der aufgeführten Rollen **Anzeigen** aus, um die Details dieser Rolle anzuzeigen.  Als bewährte Methode sollten Sie die geringsten Berechtigungen zuweisen, die für die Rolle erforderlich sind.  
    1. Schließen Sie das Fenster. Wählen Sie dazu in der oberen rechten Ecke des Fensters das **X** aus.

1. Schließen Sie auf der Zugriffssteuerungsseite das Fenster, indem Sie in der oberen rechten Ecke des Fensters das **X** auswählen.

1. Wählen Sie in der oberen linken Ecke des Fensters direkt unterhalb der blauen Leiste, wo „Microsoft Azure“ angezeigt wird, die Option **Startseite** aus, um zur Startseite der Azure-Dienste zurückzukehren.

1. Lassen Sie die Azure-Registerkarte in Ihrem Browser geöffnet.

### Aufgabe 3

Der Zweck dieser Aufgabe besteht darin, Sie durch die Schritte zu führen, die beim Herstellen einer Verbindung mit einer Datenquelle erforderlich sind. Viele Datenconnectors können im Rahmen einer Microsoft Sentinel-Lösung bereitgestellt werden – zusammen mit zugehörigen Inhalten wie Analyseregeln, Workbooks und Playbooks. Der Microsoft Sentinel Content-Hub ist ein zentraler Ort zum Entdecken und Verwalten sofort einsatzbereiter (integrierter) Inhalte. In diesem Schritt verwenden Sie den Content-Hub, um die Microsoft Defender für Cloud-Lösung für Microsoft Sentinel bereitzustellen.  Mit dieser Lösung können Sie Sicherheitswarnungen erfassen, die in Microsoft Defender für Cloud gemeldet werden.

1. Wählen Sie auf der Startseite der Azure-Dienste die Option Microsoft Sentinel und dann die von Ihnen erstellte Instanz **SC900-LogAnalytics-Workspace** aus.

1. Wählen Sie im linken Navigationsbereich **Content-Hub** aus.

1. Nehmen Sie sich einen Moment Zeit, um nach unten zu scrollen, um die lange Liste der verfügbaren Lösungen und die Optionen zum Filtern der Liste anzuzeigen.  Für diese Aufgabe suchen Sie nach **Microsoft Defender für Cloud**.  Wählen Sie ihn in der Liste aus.  Lesen Sie im daraufhin geöffneten Seitenfenster die Beschreibung, und wählen Sie dann **Installieren** aus.  Diese Lösung umfasst einen Datenconnector und eine Analyseregel. Ihre Installation kann einige Minuten in Anspruch nehmen.  Wählen Sie **Verwalten** aus.

1. Aktivieren Sie das Kontrollkästchen neben der Microsoft Defender für Cloud.  Rechts auf der Seite wird ein Fenster geöffnet.  Wählen Sie **Connectorseite öffnen** aus.

1. Beachten Sie die Konfigurationsanweisungen.  Wählen Sie das Feld neben dem Namen des Abonnements und wählen Sie dann **Verbinden** aus.  Möglicherweise wird ein Pop-Up-Fenster angezeigt, das angibt, dass nur Abonnements, für die Sie über Berechtigungen für Sicherheitsleseberechtigte verfügen, mit dem Streaming von Microsoft Defender Cloudwarnungen beginnen.  Klickan Sie auf **OK**.  Der Status wird zu verbunden geändert.  Der Connector ist jetzt aktiviert, obwohl es einige Zeit dauern kann, bis der Connector auf der Seite Datenconnectors angezeigt wird.  

1. Zeigen Sie nun Informationen zur Analyseregel an.  Wählen Sie oben auf der Seite (im Breadcrumb) **Microsoft Defender für Cloud** aus. Deaktivieren Sie das Kontrollkästchen neben Microsoft Defender für Cloud, da Sie den Connector bereits konfiguriert haben (es kann einige Zeit dauern, bis das Warnungssymbol ausgeblendet ist). Aktivieren Sie das Kontrollkästchen neben **CoreBackUp Deletion Activity aus verwandten Sicherheitswarnungen**. Im daraufhin geöffneten Fenster werden Informationen zur Regel und zu deren Funktionsweise angezeigt.  
    1. Obwohl die Details der Regellogik den Rahmen der Grundlagen sprengen, gehen Sie die Schritte zum Konfigurieren der Regel durch, um den Typ der Informationen anzuzeigen, die als Teil der Regel konfiguriert werden können. Wählen Sie **Konfiguration** aus.
    1. Wählen Sie die Regel **Detect CoreBackUp Deletion Activity aus verwandten Sicherheitswarnungen** aus.
    1. Wählen Sie im Fenster, das rechts auf der Seite geöffnet wird, **Regel erstellen** aus.
    1. Gehen Sie die einzelnen Konfigurationsseiten kurz und auf hoher Ebene durch, wählen Sie dann **Überprüfen und Erstellen** und dann **Speichern** aus.

1. Kehren Sie zur Sentinel-Seite zurück, indem Sie **Microsoft Sentinel | Content-Hub** aus dem Breadcrumb oben auf der Seite über den Analytics-Regeln auswählen.

1. Lassen Sie diese Seite geöffnet, da Sie sie in der nächsten Aufgabe verwenden werden.


### Aufgabe 4

In dieser Aufgabe sehen Sie sich einige der in Sentinel verfügbaren Optionen an.

1. Wählen Sie im linken Navigationsbereich **Hunting** aus.  Wählen Sie oben auf der Seite die Registerkarte **Abfragen** aus. Lesen Sie die Beschreibung, was eine Huntingabfrage ist. Hunting-Abfragen können über den Content-Hub hinzugefügt werden. Alle zuvor installierten Abfragen werden hier aufgeführt. Wählen Sie **Zum Content-Hub wechseln** aus.  Der Content-Hub listet Inhalte auf, die Abfragen entweder als Teil einer Lösung oder als eigenständige Abfrage enthalten.  Führen Sie einen Bildlauf durch, um die verfügbaren Abschnitte anzuzeigen. Schließen Sie den Content-Hub. Wählen Sie dazu in der oberen rechten Ecke des Fensters das **X** aus.

1. Wählen Sie im linken Navigationsbereich **MITRE ATT&CK** aus.  MITRE ATT&CK ist eine öffentlich zugängliche Wissensdatenbank mit Taktiken und Techniken, die häufig von Angreifern verwendet werden. Mit Microsoft Sentinel können Sie die Erkennungen anzeigen, die bereits in Ihrem Arbeitsbereich aktiv sind, sowie diejenigen, die Ihnen zur Konfiguration zur Verfügung stehen. So erhalten Sie einen Überblick über die Sicherheitsmaßnahmen in Ihrer Organisation, basierend auf den Taktiken und Techniken des MITRE ATT&CK®-Frameworks.  Wählen Sie eine beliebige Zelle aus der Matrix aus, und beachten Sie die Informationen auf der rechten Seite des Bildschirms. **Hinweis**: Möglicherweise müssen Sie auf der rechten Seite des Fensters " **<<** " auswählen, um den Informationsbereich anzuzeigen.

1. Wählen Sie im linken Navigationsbereich **Community** aus. Die Sicherheitsanalysten von Microsoft erstellen laufend neue Arbeitsmappen, Playbooks, Suchabfragen usw., die in der Community veröffentlicht werden und Ihnen zur Verwendung in Ihrer Umgebung zur Verfügung stehen. Wählen Sie auf der rechten Seite des Bildschirms **Communityinhalte integrieren** aus.  Eine neue Registerkarte mit dem GitHub-Repository wird geöffnet. Von dort können Sie Inhalte herunterladen, um Ihre Szenarien zu aktivieren. Scrollen Sie nach unten zum Abschnitt README.md, und lesen Sie die Beschreibung. Kehren Sie in Ihrem Browser zur Azure-Registerkarte zurück.

1. Wählen Sie im linken Navigationsbereich **Analysen** aus.  Es sollten zwei aktive Regeln vorhanden sein - eine, die standardmäßig verfügbar ist, und die Regel, die Sie in der vorherigen Aufgabe erstellt haben. Wählen Sie die Standardregel **Erweiterte mehrstufige Angriffserkennung** aus.  Lesen Sie die ausführlichen Informationen.  Microsoft Sentinel verwendet Fusion, eine Korrelations-Engine, die auf skalierbaren Algorithmen des maschinellen Lernens basiert, um automatisch mehrstufige Angriffe (auch als erweiterte persistente Bedrohungen bezeichnet) zu erkennen, indem Kombinationen aus anomalem Verhalten und verdächtigen Aktivitäten identifiziert werden, die in verschiedenen Phasen der Kill Chain beobachtet werden. Auf der Grundlage dieser Entdeckungen generiert Microsoft Sentinel Incidents, die auf andere Weise nur schwer abgefangen werden können. **Hinweis**: Möglicherweise müssen Sie auf der rechten Seite des Fensters " **<<** " auswählen, um den Informationsbereich anzuzeigen.

1. Wählen Sie im linken Navigationsbereich **Automation** aus.  Hier können Sie einfache Automatisierungsregeln erstellen und in vorhandene Playbooks integrieren oder neue Playbooks erstellen.  Wählen Sie **+Erstellen** und dann **Automatisierungsregel** aus.  Beachten Sie das Fenster, das auf der rechten Seite des Bildschirms geöffnet wird, und die dort verfügbaren Optionen zum Erstellen von Bedingungen und Aktionen.  Wählen Sie unten auf der Bildschirm **Abbrechen** aus.

1. Wählen Sie im linken Navigationsbereich **Arbeitsmappen** aus. Lesen Sie die Beschreibung eines Microsoft Sentinel-Workbooks.  Workbooks können über den Content-Hub hinzugefügt werden. Alle zuvor installierten Workbooks werden hier aufgeführt. Wählen Sie **Zum Content-Hub wechseln** aus.  Der Content-Hub listet Inhalte auf, die Arbeitsmappen entweder als Teil einer Lösung oder als eigenständige Arbeitsmappe enthalten. Führen Sie einen Bildlauf durch, um die verfügbaren Abschnitte anzuzeigen.

1. Schließen Sie das Fenster. Wählen Sie dazu in der oberen rechten Ecke des Fensters das **X** aus.

1. Wählen Sie in der oberen linken Ecke des Fensters direkt unterhalb der blauen Leiste die Option **Startseite** aus, um zur Startseite des Azure-Portals zurückzukehren.

1. Schließen Sie alle geöffneten Browserregisterkarten.

### Überprüfung

In dieser Demo haben Sie die Schritte zum Verbinden von Microsoft Sentinel mit Datenquellen ausgeführt, eine Arbeitsmappe eingerichtet und sich verschiedene in Microsoft Sentinel verfügbare Optionen angesehen.
