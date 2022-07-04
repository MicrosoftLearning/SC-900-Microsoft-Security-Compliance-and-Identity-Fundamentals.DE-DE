---
Demo:
  title: Microsoft Defender für Cloud'
  module: 'Module 3 Lesson 2: Describe the capabilities of Microsoft security solutions: Describe security management capabilities of Azure'
ms.openlocfilehash: ff5145e967445c12dacd90ea50002fe0c3042efb
ms.sourcegitcommit: b8b861a8c884a56f094213e47a59be48ba898ca1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/29/2022
ms.locfileid: "146741902"
---
# <a name="demo-microsoft-defender-for-cloud"></a>Demo: Microsoft Defender für Cloud

## <a name="demo-scenario"></a>Demoszenario

In dieser Demo gehen Sie Microsoft Defender für Cloud durch und zeigen, wie der Sicherheitsstatus einer Organisation mit der Azure-Sicherheitsbewertung verbessert werden kann.  HINWEIS: Bei dieser exemplarischen Vorgehensweise wird davon ausgegangen, dass der Referent bzw. die Referentin über Berechtigungen auf Administratorebene für das Azure-Abonnement über Azure Pass verfügt.  Ein Azure-Abonnement, z. B. ein Cloudslice-Abonnement, das vom autorisierten Lab-Hoster verwaltet wird, beschränkt den Zugriff und die Funktionalität, sodass einige nachfolgenden Schritte möglicherweise nicht verfügbar sind oder keine Informationen anzeigen.

### <a name="demo-setup"></a>Demoeinrichtung

In dieser Setupaufgabe führen Sie einige grundlegende Einrichtungsschritte in Microsoft Defender für Cloud aus, um das Abonnement vorzubereiten und eine Standardrichtlinie zu aktivieren und zuzuweisen. Tun Sie dies, bevor Sie den Kurs halten. 

1. Öffnen Sie die Browserregisterkarte **Startseite – Microsoft Azure**.  Falls Sie die Registerkarte geschlossen haben, öffnen Sie eine Browserseite. Geben Sie „portal.azure.com“ in die Adressleiste ein, und melden Sie sich erneut an.

1. Geben Sie im Suchfeld in der blauen Leiste oben auf der Seite neben der Stelle, an der Microsoft Azure steht, **Microsoft Defender für Cloud** ein, und wählen Sie dann in den Suchergebnissen **Microsoft Defender für Cloud** aus.

1. Wenn Sie Microsoft Defender für Cloud zum ersten Mal mit Ihrem Abonnement aufrufen, werden Sie möglicherweise zur Seite „Erste Schritte“ geleitet und zur Durchführung eines Upgrades aufgefordert.  Scrollen Sie auf der Seite nach unten, und klicken Sie auf **Skip**.  Sie werden zur Übersicht weitergeleitet.
    1. Oben auf der Seite wird ein hellblaues Informationsfeld angezeigt, das angibt: „Getting things ready for your subscription. This may take a few minutes...“ (Ihr Abonnement wird vorbereitet. Dies kann einige Minuten dauern.).
    1. Sobald das Abonnement fertig ist, wird ein neues Informationsfeld angezeigt, das besagt: „One subscription doesn't have the default policy assigned. To review the the list of subscriptions, open the Security Policy page.“ (Einem Abonnement ist keine Standardrichtinie zugewiesen. Öffnen Sie die Seite „Sicherheitsrichtlinie“, um die Liste der Abonnements zu überprüfen.).  Wählen Sie den Pfeil nach rechts am Ende des Satzes aus.
        1. Sie befinden sich jetzt auf der Seite „Umgebungseinstellungen“. Wählen Sie **Azure Pass – Förderung** aus. 
        1. Wählen Sie im linken Navigationsbereich **Sicherheitsrichtlinie** aus.
        1. Wählen Sie auf der Hauptseite unter „Standardinitiative“ die Option **Richtlinie zuweisen** aus.
        1. Klicken Sie im unteren Seitenbereich auf **Überprüfen und erstellen**.
        1. Wählen Sie am unteren Rand der Seite **Erstellen** aus.
        1. Wählen Sie oben auf der Seite in der Breadcrumb-Leiste unter Microsoft Azure die Option **Microsoft Defender für Cloud** aus, um zur Übersicht zurückzukehren.

### <a name="demo-task"></a>Demoaufgabe

In dieser Demoaufgabe durchlaufen Sie ganz allgemein einige der Funktionen von Microsoft Defender für Cloud.

1. Oben auf der Seite der Microsoft Defender für Cloud-Übersicht finden Sie Informationen wie die Anzahl der Azure-Abonnements, die Anzahl der bewerteten Ressourcen, die Anzahl der aktiven Empfehlungen und alle Sicherheitswarnungen.  In der Mitte der Seite befinden sich Karten für die Sicherheitsbewertung, die Einhaltung gesetzlicher Bestimmungen, Insights und mehr.  

1. Wählen Sie oben auf der Seite die Option **Bewertete Ressourcen** aus.  (Beachten Sie, dass Sie genauso auf der Startseite von Microsoft Defender für Cloud im linken Navigationsbereich die Option „Inventar“ auswählen können.)
    1. Dadurch gelangen Sie zur Seite **Inventar**, auf der Ihr Azure Pass-Abonnement angezeigt wird.  Wählen Sie **Azure Pass-Förderung** aus.
    1. Auf der Seite „Resource Health“ finden Sie eine Liste mit Empfehlungen.  Wählen Sie in der verfügbaren Liste die Option **Ihrem Abonnement sollte mehr als ein Besitzer zugewiesen sein** aus.
    1. Wählen Sie den Dropdownpfeil neben den Wartungsschritten aus. Beachten Sie, dass ausführliche Schritte zur Wartung sowie eine entsprechende Option für Gegenmaßnahmen angezeigt werden.  
    1. Wählen Sie in der oberen linken Ecke des Bildschirms **Microsoft Defender für Cloud** aus, um zur Übersichtsseite von Microsoft Defender für Cloud zurückzukehren.

1. Wählen Sie oben auf der Seite die Option **Aktive Empfehlungen** aus.  (Beachten Sie, dass Sie genauso auf der Startseite von Microsoft Defender für Cloud im linken Navigationsbereich die Option „Empfehlungen“ auswählen können.)
    1. Auf der Empfehlungsseite wird Ihr Sicherheitsbewertungs-Dashboard angezeigt.
    1. Unter dem Sicherheitsbewertungs-Dashboard finden Sie eine Liste von Kontrollen. Jede Sicherheitskontrolle stellt ein Sicherheitsrisiko dar, das eingedämmt werden sollte, und enthält außerdem Angaben zur maximalen Bewertung, die mit dieser Kontrolle verbunden ist, zur aktuellen Bewertung, zur potenziellen Erhöhung der Bewertung und zum Integritätsstatus der Ressourcen.  
    1. Wählen Sie eine Steuerung aus, wie etwa **MFA aktivieren**.  Wählen Sie ein Unterelement aus, wie etwa **Für Konten mit Besitzerberechtigungen für Ihr Abonnement muss MFA aktiviert sein**.  Auf der daraufhin geöffneten Seite werden Ihnen eine Beschreibung, Schritte zur Wartung und betroffene Ressourcen angezeigt. Schließen Sie diese Seite mit dem **X** oben rechts auf dem Bildschirm.
    1. Schließen Sie die Empfehlungsseite mit dem **X** oben rechts auf dem Bildschirm, um zur Übersichtsseite zurückzukehren.

1. Sie befinden sich wieder auf der Übersichtsseite von Microsoft Defender für Cloud.  Wählen Sie auf der Hauptseite **Einhaltung gesetzlicher Bestimmungen** aus. (Beachten Sie, dass Sie genauso auf der Startseite von Microsoft Defender für Cloud im linken Navigationsbereich die Option „Empfehlungen“ auswählen können.)
    1. Auf der Seite „Einhaltung gesetzlicher Bestimmungen“ finden Sie eine Liste mit Compliancekontrollen.  Unter jeder Kontrolle befinden sich eine Reihe von Bewertungen, die auf dem Azure-Sicherheitsvergleichstest basieren. Dieser liefert Empfehlungen dazu, wie Sie Ihre Cloudlösungen auf Azure schützen können.
    1. Wählen Sie **IM. Identitätsverwaltung** und dann **IM.6 Verwenden stärkerer Authentifizierungssteuerungen für den gesamten Azure Active Directory-basierten Zugriff** aus.  In der Liste werden Aktionen zur Verbesserung der Compliancesituation aufgeführt, für die der Kunde verantwortlich ist.
    1. Wählen Sie das **X** oben rechts auf dem Bildschirm aus, um die Seite zu schließen und zur Seite für die Einhaltung gesetzlicher Bestimmungen zurückzukehren.
    1. Wählen Sie das **X** oben rechts auf dem Bildschirm aus, um zur Übersichtsseite zurückzukehren.

1. Denken Sie daran, dass Microsoft Defender für Cloud in zwei Modi angeboten wird: ohne erweiterte Sicherheitsfeatures (kostenlos) und mit erweiterten Sicherheitsfeatures, die über die Microsoft Defender für Cloud-Pläne verfügbar sind. Hier erfahren Sie, wie Sie die verschiedenen Microsoft Defender für Cloud-Pläne aktivieren/deaktivieren.
    1. Wählen Sie auf der Übersichtsseite von Microsoft Defender für Cloud im linken Navigationsbereich **Umgebungseinstellungen** aus.
    1. Wählen Sie das Größer-als-Zeichen **>** neben „Mandantenstammgruppe“ aus, um sie zu erweitern (wählen Sie „Mandantenstammgruppe“ nicht direkt aus, da Sie dann zu einer anderen Seite geleitet werden). Wählen Sie dann **Azure Pass – Sponsorship** aus.
    1. Beachten Sie auf der Seite mit den Defender-Plänen, wie Sie alle Pläne aktivieren oder einzelne Defender-Pläne auswählen können. Übernehmen Sie die Einstellungen unverändert (alle Pläne deaktiviert).
    1. Wählen Sie das **X** oben rechts auf dem Bildschirm aus, um zu den Umgebungseinstellungen zurückzukehren.
    1. Wählen Sie das **X** oben rechts auf dem Bildschirm aus, um zur Übersichtsseite zurückzukehren.

1. Kehren Sie zur Startseite des Azure-Portals zurück. Wählen Sie dazu links oben auf der Seite **Startseite** aus.  Lassen Sie diese Browserregisterkarte geöffnet, da Sie diese in einer späteren Demo benötigen.

## <a name="review"></a>Überprüfung

In dieser Demo sind Sie Microsoft Defender für Cloud durchgegangen und haben gezeigt, wie der Sicherheitsstatus einer Organisation mit der Azure-Sicherheitsbewertung verbessert werden kann.
