---
lab:
  title: Erkunden von Microsoft Sentinel
  module: 'Module 3 Lesson 3: Describe the capabilities of Microsoft security solutions: Describe security capabilities of Microsoft Sentinel'
ms.openlocfilehash: 72d9f0c32e7c8f48b9c6fdb3468a000a9006b6ba
ms.sourcegitcommit: 57e11f5a455d10c8ae3c95bb8a9487b10af3d315
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/22/2022
ms.locfileid: "146542578"
---
# <a name="lab-explore-microsoft-sentinel"></a>Lab: Erkunden von Microsoft Sentinel

## <a name="lab-scenario"></a>Labszenario

In diesem Lab gehen Sie den Prozess der Erstellung einer Microsoft Sentinel-Instanz durch.  Zudem richten Sie die Berechtigungen ein, um den Zugriff auf die Ressourcen sicherzustellen, die zur Unterstützung von Microsoft Sentinel bereitgestellt werden.  Nachdem die grundlegende Einrichtung abgeschlossen ist, führen Sie die Schritte aus, die erforderlich sind, um Microsoft Sentinel mit Ihren Datenquellen zu verbinden und eine Arbeitsmappe einzurichten. Außerdem sehen Sie sich einige wichtigen Funktionen in Microsoft Sentinel an.  

**Geschätzte Dauer**: 45-60 Minuten

### <a name="task-1"></a>Aufgabe 1

Erstellen einer Microsoft Sentinel-Instanz

1. Öffnen Sie die Browserregisterkarte **Startseite – Microsoft Azure**.  Falls Sie die Registerkarte geschlossen haben, öffnen Sie eine Browserseite. Geben Sie „portal.azure.com“ in die Adressleiste ein, und melden Sie sich erneut an.

1. Geben Sie in das Suchfeld, das sich auf dem blauen Balken oben auf der Seite neben dem Text „Microsoft Azure“ befindet, den Text **Microsoft Sentinel** ein, und wählen Sie dann **Microsoft Sentinel** in den Suchergebnissen aus.

1. Wählen Sie auf der Seite „Microsoft Sentinel“ die Option **Microsoft Sentinel erstellen** aus.

1. Wählen Sie auf der Seite zum Hinzufügen von Microsoft Sentinel zu einem Arbeitsbereich die Option **Neuen Arbeitsbereich erstellen** aus.

1. Geben Sie auf der Registerkarte „Grundlagen“ von „Log Analytics-Arbeitsbereich erstellen“ Folgendes ein:
    1. Abonnement:  **Azure Pass – Sponsorship**
    1. Ressourcengruppe: Wählen Sie **Neu erstellen** aus, geben Sie dann den Namen **SC900-Sentinel-RG** ein, und wählen Sie **OK** aus.
    1. Name: **SC900-LogAnalytics-workspace**.
    1. Region: **East US** (Sie können eine andere Standardregion basierend auf Ihrem Standort auswählen)
    1. Klicken Sie auf **Weiter: Tags >**

1. Für „Tags“ können Sie dies leer lassen. Wählen Sie dann **Bewerten + erstellen** aus.

1. Überprüfen Sie Ihre eingegebenen Informationen, und wählen Sie dann **Erstellen** aus.

1. Es kann eine oder zwei Minuten dauern, bis der Arbeitsbereich aufgelistet wird. Wenn er weiterhin nicht angezeigt wird, wählen Sie **Aktualisieren** und dann **Hinzufügen** aus.

1. Nachdem der neue Arbeitsbereich hinzugefügt wurde, wird die Seite „Microsoft Sentinel | Neuigkeiten und Leitfäden“ angezeigt.  Beachten Sie die drei auf der Seite „Erste Schritte“ aufgelisteten Schritte.

1. Lassen Sie diese Seite geöffnet, da Sie sie in der nächsten Aufgabe verwenden werden.

### <a name="task-2"></a>Aufgabe 2

Nachdem Sie die Microsoft Sentinel-Instanz erstellt haben, möchten Sie sicherstellen, dass Sie über den erforderlichen Zugriff auf die Ressourcen verfügen, die zum Unterstützen von Microsoft Sentinel bereitgestellt werden.

1. Geben Sie in das Suchfeld, das sich auf dem blauen Balken oben auf der Seite neben dem Text „Microsoft Azure“ befindet, den Text **Ressourcengruppen** ein, und wählen Sie dann **Ressourcengruppen** aus den Suchergebnissen aus. Durch das Zuweisen der Rolle auf der Ressourcengruppenebene wird sichergestellt, dass die Rolle für alle Ressourcen gilt, die zum Unterstützen von Microsoft Sentinel bereitgestellt werden.

1. Wählen Sie auf der Seite „Ressourcengruppen“ die von Ihnen mit Microsoft Sentinel erstellte Ressourcengruppe aus, nämlich **SC900-Sentinel-RG**.

1. Wählen Sie auf der Seite „SC900-Sentinel-RG“ im linken Navigationsbereich die Option **Zugriffssteuerung (IAM)** aus.

1. Wählen Sie auf der Seite „Zugriffssteuerung“ die Option **Meinen Zugriff anzeigen** aus.  Für den MOD-Administrator ist die aktuelle Rolle „Dienstadministrator“.  Damit erhalten Sie die notwendigen Berechtigungen. Sie müssen die für Sentinel spezifischen Rollen aber kennen.  Wählen Sie zum Schließen des Fensters für die MOD-Administratorzuweisungen das **X** aus, das sich in der oberen rechten Ecke des Fensters befindet.

    1. Wählen Sie auf der Seite „Zugriffssteuerung“ die Option **+ Hinzufügen** und dann **Rollenzuweisung hinzufügen** aus.

    1. Das Fenster „Rollenzuweisung hinzufügen“ wird geöffnet.  Geben Sie **Microsoft Sentinel** in das Suchfeld ein, um die vier Rollen anzuzeigen, die Microsoft Sentinel zugeordnet sind.
    1. Wählen Sie in einer der aufgeführten Rollen **Anzeigen** aus, um die Details dieser Rolle anzuzeigen.  Als bewährte Methode empfiehlt es sich, die niedrigste Berechtigung zuzuweisen, die für die Rolle erforderlich ist.  

    1. Schließen Sie das Fenster, indem Sie in der oberen rechten Ecke des Fensters das **X** auswählen.

1. Schließen Sie auf der Zugriffssteuerungsseite das Fenster, indem Sie in der oberen rechten Ecke des Fensters das **X** auswählen.

### <a name="task-3"></a>Aufgabe 3

Bei dieser Aufgabe gehen Sie den Prozess zum Herstellen der Verbindung zwischen Microsoft Sentinel und Ihrer Datenquelle durch, um mit dem Sammeln von Daten zu beginnen.

1. Geben Sie in das Suchfeld, das sich auf dem blauen Balken oben auf der Seite neben dem Text „Microsoft Azure“ befindet, den Text **Microsoft Sentinel** ein, und wählen Sie dann **Microsoft Sentinel** in den Suchergebnissen aus.

1. Wählen Sie auf der Seite „Microsoft Sentinel“ den von Ihnen mit der Microsoft Sentinel-Instanz erstellten Arbeitsbereich aus, nämlich **SC900-LogAnalytics-workspace**.

1. Der erste Schritt mit Microsoft Sentinel besteht darin, Daten sammeln zu können. Wählen Sie im linken Navigationsbereich die unter der Konfiguration aufgelistete Option **Datenconnectors** aus.

1. Scrollen Sie auf der Seite „Datenconnectors“ nach unten zum Hauptfenster, um die ausführliche Liste mit den verfügbaren Connectors anzuzeigen. Geben Sie auf der Seite „Datenconnectors“ **Office 365** in das Suchfeld ein, und wählen Sie dann **Office 365** aus der Liste aus.

1. Das Fenster mit dem Office 365-Connector wird geöffnet.  Wählen Sie **Connectorseite öffnen** aus.

1. Lesen Sie die Beschreibung des Office 365-Connectors auf der linken Seite.

1. Auf der Registerkarte „Anweisungen“ im Hauptfenster sind die Voraussetzungen für die Integration von Microsoft Sentinel in Office 365 angegeben. Hier sollte überall ein grünes Häkchen angezeigt werden.   Wählen Sie unter „Konfiguration“ die Optionen **Exchange** und **SharePoint** und dann „Änderungen anwenden“ aus.  Auf der linken Seite des Fensters wird der Status nahezu sofort als „Verbunden“ angezeigt.

1. Schließen Sie das Fenster, indem Sie das **X** in der oberen rechten Ecke des Fensters auswählen, um zur Seite „Datenconnectors“ zurückzukehren.

1. Oben auf der Seite „Datenconnectors“ sollte „1 verbunden“ angezeigt werden, um anzugeben, dass Sie nun mit Office 365 verbunden sind. Wenn diese Angabe nicht angezeigt wird, wählen Sie **Aktualisieren** aus. Es kann einige Minuten dauern, bis diese Seite aktualisiert wird.

1. Lassen Sie diese Seite geöffnet, da Sie sie in der nächsten Aufgabe verwenden werden.

### <a name="task-4"></a>Aufgabe 4

In dieser Aufgabe durchlaufen Sie den Prozess der Einrichtung einer Arbeitsmappe für Office 365, um Ihre Daten zu visualisieren und zu überwachen.

1. Wählen Sie im linken Navigationsbereich **Arbeitsmappen** aus.

1. Geben Sie „Office 365“ in das Suchfeld ein, und wählen Sie dann **Office 365** aus.

1. Lesen Sie die Beschreibung in dem Fenster, das auf der rechten Seite des Bildschirms geöffnet wird, und wählen Sie dann unten auf dem Bildschirm **Speichern** und danach **OK** aus, um die Arbeitsmappe im Standardspeicherort zu speichern.  Wählen Sie jetzt **Gespeicherte Arbeitsmappe anzeigen** aus.

1. Die Seite „Office 365-Arbeitsmappen“ wird geöffnet.  Wählen Sie den Dropdownpfeil neben **Vorgänge: löschen** und dann **Alle** aus.  Wählen Sie jetzt den Dropdownpfeil neben **Benutzer: Abfrage ausstehend** und dann **Alle** aus.  Wählen Sie das **Symbol „Speichern“ (Datenträger)** aus. Schließen Sie das Fenster, indem Sie in der oberen rechten Ecke des Fensters das **X** auswählen. Es kann mehrere Minuten dauern, bis Daten in der Arbeitsmappe angezeigt werden, Sie werden also später wieder zu den Arbeitsmappen zurückkehren.

1. Wählen Sie in der oberen linken Ecke der Seite „Arbeitsmappe“ oberhalb des Texts „Arbeitsmappen“ die Option **Microsoft Sentinel** aus. Damit werden Sie zur Seite „Übersicht“ zurückgeleitet.

### <a name="task-5"></a>Aufgabe 5

In dieser Aufgabe sehen Sie sich einige der in Sentinel verfügbaren Optionen an.

1. Wählen Sie im linken Navigationsbereich **Hunting** aus.  Wählen Sie auf der Registerkarte **Abfragen**, die ausgewählt (unterstrichen) ist, eine beliebige Abfrage aus der Liste aus.  Beachten Sie nach der Auswahl der Abfrage die Informationen, die zu dieser Abfrage bereitgestellt werden, wie z. B. den Code für die Abfrage sowie die Option zum Ausführen der Abfrage und Anzeigen der Ergebnisse.  Wählen Sie nichts aus.

1. Wählen Sie im linken Navigationsbereich **MITRE ATT&CK** aus.  MITRE ATT&CK ist eine öffentlich zugängliche Wissensdatenbank mit Taktiken und Techniken, die häufig von Angreifern verwendet werden. Mit Microsoft Sentinel können Sie die Erkennungen anzeigen, die bereits in Ihrem Arbeitsbereich aktiv sind, sowie diejenigen, die Ihnen zur Konfiguration zur Verfügung stehen. So erhalten Sie einen Überblick über die Sicherheitsmaßnahmen in Ihrer Organisation, basierend auf den Taktiken und Techniken des MITRE ATT&CK®-Frameworks.  Wählen Sie eine beliebige Zelle aus der Matrix aus, und beachten Sie die Informationen auf der rechten Seite des Bildschirms.  

1. Wählen Sie im linken Navigationsbereich **Community** aus. Die Sicherheitsanalysten von Microsoft erstellen laufend neue Arbeitsmappen, Playbooks, Hunting-Abfragen usw., die in der Community veröffentlicht werden und Ihnen zur Verwendung in Ihrer Umgebung zur Verfügung stehen. Sie können Beispielinhalte aus dem privaten GitHub-Repository der Community herunterladen, um benutzerdefinierte Arbeitsmappen, Suchabfragen, Notebooks und Playbooks für Microsoft Sentinel zu erstellen.  Wählen Sie **Communityinhalt integrieren** aus.  Eine neue Registerkarte mit dem GitHub-Repository wird geöffnet. Von dort können Sie Inhalte herunterladen, um Ihre Szenarien zu aktivieren.  Kehren Sie in Ihrem Browser zur Azure-Registerkarte zurück.

1. Wählen Sie im linken Navigationsbereich **Analysen** aus.  Wählen Sie das erste Element aus der Liste **Erweiterte Erkennung mehrstufiger Angriffe** aus.  Lesen Sie die ausführlichen Informationen.  Microsoft Sentinel verwendet Fusion, eine Korrelations-Engine, die auf skalierbaren Algorithmen des maschinellen Lernens basiert, um automatisch mehrstufige Angriffe (auch als erweiterte persistente Bedrohungen bezeichnet) zu erkennen, indem Kombinationen aus anomalem Verhalten und verdächtigen Aktivitäten identifiziert werden, die in verschiedenen Phasen der Kill Chain beobachtet werden. Auf der Grundlage dieser Entdeckungen generiert Microsoft Sentinel Incidents, die auf andere Weise nur schwer abgefangen werden können.

1. Wählen Sie im linken Navigationsbereich **Automation** aus.  Hier können Sie ganz einfach Automatisierungsregeln erstellen und in vorhandene Playbooks integrieren oder neue Playbooks erstellen.  Wählen Sie **+Erstellen** und dann **Automatisierungsregel** aus.  Beachten Sie das Fenster, das auf der rechten Seite des Bildschirms geöffnet wird, und die dort verfügbaren Optionen zum Erstellen von Bedingungen und Aktionen.  Wählen Sie unten auf der Bildschirm **Abbrechen** aus.

1. Wählen Sie im linken Navigationsbereich **Arbeitsmappen** aus. Wählen Sie auf der Seite „Arbeitsmappen“ die Registerkarte **Meine Arbeitsmappen** aus, die sich oberhalb des Suchfelds befindet.  Die von Ihnen zuvor gespeicherte Arbeitsmappe wird aufgelistet und steht Ihnen zum Anzeigen und Überwachen Ihrer Daten zur Verfügung.  Wählen Sie in dem Fenster, das auf der rechten Seite des Bildschirms geöffnet wird, **Office 365** und dann **Gespeicherte Arbeitsmappe anzeigen** aus.  Beachten Sie die Visualisierungen im Zusammenhang mit Ihren Office 365-Workloads.  

1. Schließen Sie das Fenster, indem Sie in der oberen rechten Ecke des Fensters das **X** auswählen.

1. Wählen Sie in der oberen linken Ecke des Fensters direkt unterhalb der blauen Leiste die Option **Startseite** aus, um zur Startseite des Azure-Portals zurückzukehren.

### <a name="task-6"></a>Aufgabe 6

Microsoft Sentinel wird auf Grundlage der Datenmenge abgerechnet, die zur Analyse in Microsoft Sentinel erfasst wurde. Obwohl die im Rahmen dieses Labs erfasste Datenmenge sehr gering ist, sollten Sie die Microsoft Sentinel-Ressourcengruppe löschen, nachdem Sie die Funktionen von Microsoft Sentinel erkundet haben.

1. Wählen Sie auf der Seite „Microsoft Sentinel“ in der oberen linken Ecke der Seite oberhalb des Texts „Microsoft Sentinel“ die Option **Alle Dienste** aus.

2. Geben Sie die Ressourcengruppen in das Feld „Dienste filtern“ ein. Wählen Sie dann in der bereitgestellten Liste den Eintrag **Ressourcengruppen** aus.

3. Wählen Sie auf der Seite „Ressourcengruppen“ die von Ihnen mit Microsoft Sentinel erstellte Ressourcengruppe aus, nämlich **SC900-ResourceGroup**.

4. Wählen Sie im oberen mittleren Bereich der Seite die Option **Ressourcengruppe löschen** aus.  Überprüfen Sie die Warnung.  Geben Sie den Namen der Ressourcengruppe **SC900-ResourceGroup** ein. Wählen Sie dann unten auf der Seite **Löschen** aus.  Es kann mehrere Minuten dauern, bis die Ressourcengruppe gelöscht ist.

5. Nachdem Sie die Löschung der Ressourcengruppe überprüft haben, schließen Sie die Browserseite.

### <a name="review"></a>Überprüfung

In dieser Demo haben Sie die Schritte zum Verbinden von Microsoft Sentinel mit Datenquellen ausgeführt, eine Arbeitsmappe eingerichtet und sich verschiedene in Microsoft Sentinel verfügbare Optionen angesehen.
