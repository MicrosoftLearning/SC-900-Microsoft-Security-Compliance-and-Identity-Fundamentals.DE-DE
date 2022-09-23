---
ms.openlocfilehash: eeee584ece9bb3ec4edcba5fa2e76a13dd9459c4
ms.sourcegitcommit: 15658ca1c7bae8a4dbaa33ab6f897070bde521b9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/12/2022
ms.locfileid: "147892604"
---
<a name="---"></a><!---
---
Lab: Title: 'Erkunden von Microsoft Defender für Cloud' Learning Path/Module/Unit: 'Lernpfad: Beschreiben der Funktionen von Microsoft-Sicherheitslösungen; Modul 2: Beschreiben der Sicherheitsverwaltungsfunktionen von Azure; Lerneinheit 3: Beschreiben von Microsoft Defender für Cloud'
---
--->

# <a name="lab-explore-microsoft-defender-for-cloud"></a>Lab: Erkunden von Microsoft Defender für Cloud

Dieses Lab ist den folgenden Learn-Inhalten zugeordnet:

- Lernpfad: Beschreiben der Funktionen von Microsoft-Sicherheitslösungen
- Modul: Beschreiben der Sicherheitsverwaltungsfunktionen von Azure
- Lerneinheit: Beschreiben von Microsoft Defender für Cloud

## <a name="lab-scenario"></a>Labszenario

In diesem Lab erkunden Sie Defender für Cloud und erfahren, wie Sie mithilfe der Azure-Sicherheitsbewertung den Sicherheitsstatus Ihrer Organisation verbessern können.  HINWEIS: Bei dieser exemplarischen Vorgehensweise wird davon ausgegangen, dass der Referent bzw. die Referentin über Berechtigungen auf Administratorebene für das Azure-Abonnement über Azure Pass verfügt.  Ein Azure-Abonnement, z. B. ein Cloudslice-Abonnement, das vom autorisierten Lab-Hoster verwaltet wird, beschränkt den Zugriff und die Funktionalität, sodass einige nachfolgenden Schritte möglicherweise nicht verfügbar sind oder keine Informationen anzeigen.

**Geschätzte Dauer**: 30 Minuten

### <a name="setup"></a>Einrichten

In dieser Aufgabe führen Sie einige grundlegende Einrichtungsschritte in Microsoft Defender für Cloud aus, um das Abonnement vorzubereiten und eine Standardrichtlinie zu aktivieren und zuzuweisen.

1. Öffnen Sie Microsoft Edge. Geben Sie **portal.azure.com** in die Adressleiste ein.

1. Melden Sie sich mit Ihren Administratoranmeldeinformationen an.
    1. Geben Sie **admin@WWLxZZZZZZ.onmicrosoft.com** (ZZZZZZ ist hierbei die eindeutige Mandanten-ID, die von Ihrem Labhostinganbieter bereitgestellt wurde) in das Fenster „Anmelden“ ein, und wählen Sie dann **Weiter** aus.
    1. Geben Sie das Administratorkennwort ein, das Sie vom Labhostinganbieter erhalten haben sollten. Wählen Sie **Anmelden**.
    1. Wählen Sie **Ja** aus, wenn Sie gefragt werden, ob Sie angemeldet bleiben möchten.

1. Wählen Sie in der oberen linken Ecke des Bildschirms neben dem Text „Microsoft Azure“ das Symbol „Portalmenü anzeigen“ (die drei horizontalen Linien werden auch als Hamburgersymbol bezeichnet) und dann im linken Navigationsbereich unter „Favoriten“ **Microsoft Defender für Cloud** aus.  Wenn die Option unter „Favoriten“ nicht aufgeführt ist, geben Sie im Suchfeld **Microsoft Defender für Cloud** ein, und wählen Sie dann in der Ergebnisliste **Microsoft Defender für Cloud** aus.

1. Wenn Sie Microsoft Defender für Cloud zum ersten Mal mit Ihrem Abonnement aufrufen, werden Sie möglicherweise zur Seite „Erste Schritte“ geleitet und zur Durchführung eines Upgrades aufgefordert.  Scrollen Sie auf der Seite nach unten, und klicken Sie auf **Skip**.  Sie werden zur Übersicht weitergeleitet.
    1. Oben auf der Seite wird ein hellblaues Informationsfeld angezeigt, das angibt: „Getting things ready for your subscription. This may take a few minutes...“ (Ihr Abonnement wird vorbereitet. Dies kann einige Minuten dauern.).
    1. Sobald das Abonnement fertig ist, wird möglicherweise ein neues Informationsfeld angezeigt, das besagt: „One subscription doesn't have the default policy assigned. To review the the list of subscriptions, open the Security Policy page.“ (Einem Abonnement ist keine Standardrichtinie zugewiesen. Öffnen Sie die Seite „Sicherheitsrichtlinie“, um die Liste der Abonnements zu überprüfen.).  Wählen Sie den Pfeil nach rechts am Ende des Satzes aus, oder wählen Sie **Umgebungseinstellungen** im linken Navigationsbereich aus.
        1. Sie befinden sich jetzt auf der Seite „Umgebungseinstellungen“. Wählen Sie **Azure Pass – Förderung** aus.  Hinweis:  Wenn Ihre Azure-Umgebung auf einem Azure-Abonnement basiert, das vom autorisierten Lab-Hoster verwaltet wird, wird auf diese Option statt auf Azure Pass verwiesen. Erweitern Sie die Option, indem Sie das „Größer als“-Zeichen auswählen, bis Sie alle Optionen sehen können und das Abonnement angezeigt wird.
        1. Wählen Sie im linken Navigationsbereich **Sicherheitsrichtlinie** aus.
        1. Wählen Sie auf der Hauptseite unter „Standardinitiative“ die Option **Richtlinie zuweisen** aus.
        1. Klicken Sie im unteren Seitenbereich auf **Überprüfen und erstellen**.
        1. Wählen Sie am unteren Rand der Seite **Erstellen** aus.  Dadurch wird der Vergleichstest für die Azure-Sicherheit (Azure Security Benchmark) als Standardrichtlinieninitiative zugewiesen.  Aktualisieren Sie den Bildschirm (es kann einige Minuten dauern, bis die Einstellung übernommen wird).
        1. Verlassen Sie die Seite „Umgebungseinstellungen“, indem Sie das **X** auswählen.  
        1. Wählen Sie auf der Seite „Azure-Dienste“ **Microsoft Defender für Cloud** aus, um zur Übersichtsseite zurückzukehren.

### <a name="task-1"></a>Aufgabe 1

In dieser Aufgabe durchlaufen Sie ganz allgemein einige der Funktionen von Microsoft Defender für Cloud.

1. Beachten Sie in der Übersicht von Microsoft Defender für Cloud die auf der Seite verfügbaren Informationen.  Oben auf der Seite finden Sie Informationen wie die Anzahl der Azure-Abonnements, die Anzahl der bewerteten Ressourcen, die Anzahl der aktiven Empfehlungen und alle Sicherheitswarnungen.  In der Mitte der Seite befinden sich Karten für die Sicherheitsbewertung, die Einhaltung gesetzlicher Bestimmungen, Insights und mehr.

1. Wählen Sie oben auf der Seite die Option **Bewertete Ressourcen** aus.  (Beachten Sie, dass Sie genauso auf der Startseite von Microsoft Defender für Cloud im linken Navigationsbereich die Option „Inventar“ auswählen können.)
    1. Dadurch gelangen Sie zur Seite **Inventar**, auf der Ihr Azure Pass-Abonnement angezeigt wird.  Wählen Sie **Azure Pass-Förderung** aus.
    1. Auf der Seite „Resource Health“ finden Sie eine Liste mit Empfehlungen.  Wählen Sie in der verfügbaren Liste die Option **Ihrem Abonnement sollte mehr als ein Besitzer zugewiesen sein** aus.
    1. Wählen Sie den Dropdownpfeil neben den Wartungsschritten aus. Beachten Sie, dass ausführliche Schritte zur Wartung sowie eine entsprechende Option für Gegenmaßnahmen angezeigt werden.  
    1. Wählen Sie in der oberen linken Ecke des Bildschirms **Microsoft Defender für Cloud** aus, um zur Übersichtsseite von Microsoft Defender für Cloud zurückzukehren.

1. Wählen Sie oben auf der Seite die Option **Aktive Empfehlungen** aus.  (Beachten Sie, dass Sie genauso auf der Startseite von Microsoft Defender für Cloud im linken Navigationsbereich die Option „Empfehlungen“ auswählen können.)
    1. Auf der Empfehlungsseite wird Ihr Sicherheitsbewertungs-Dashboard angezeigt.
    1. Unter dem Sicherheitsbewertungs-Dashboard finden Sie eine Liste von Kontrollen. Jede Sicherheitskontrolle stellt ein Sicherheitsrisiko dar, das eingedämmt werden sollte, und enthält außerdem Angaben zur maximalen Bewertung, die mit dieser Kontrolle verbunden ist, zur aktuellen Bewertung, zur potenziellen Erhöhung der Bewertung und zum Integritätsstatus der Ressourcen.  
    1. Wählen Sie eines der Steuerelemente aus, z. B. **Best Practices für die Sicherheit implementieren**.  Wählen Sie eines der Unterelemente aus, z. B. **Ihrem Abonnement muss mehr als ein Besitzer zugewiesen sein**.  Auf der daraufhin geöffneten Seite werden Ihnen eine Beschreibung, Schritte zur Wartung und betroffene Ressourcen angezeigt. Schließen Sie diese Seite mit dem **X** oben rechts auf dem Bildschirm.
    1. Schließen Sie die Empfehlungsseite mit dem **X** oben rechts auf dem Bildschirm, um zur Übersichtsseite zurückzukehren.

1. Wählen Sie auf der Hauptseite **Einhaltung gesetzlicher Bestimmungen** aus. Auf der Seite „Einhaltung gesetzlicher Bestimmungen“ finden Sie eine Liste mit Compliancekontrollen.  Unter jeder Kontrolle befinden sich eine Reihe von Bewertungen, die auf dem Azure-Sicherheitsvergleichstest basieren. Dieser liefert Empfehlungen dazu, wie Sie Ihre Cloudlösungen auf Azure schützen können.
    1. Wählen Sie **IM. Identitätsverwaltung** und dann **IM.6 Verwenden stärkerer Authentifizierungssteuerungen für den gesamten Azure Active Directory-basierten Zugriff** aus.  In der Liste werden Aktionen zur Verbesserung der Compliancesituation aufgeführt, für die der Kunde verantwortlich ist.
    1. Wählen Sie das **X** oben rechts auf dem Bildschirm aus, um die Seite zu schließen und zur Übersichtsseite von Microsoft Defender für Cloud zurückzukehren.
    1. Lassen Sie die Übersichtsseite von Microsoft Defender für Cloud geöffnet. Sie wird in der nächsten Aufgabe verwendet.

### <a name="task-2"></a>Aufgabe 2

Denken Sie daran, dass Microsoft Defender für Cloud in zwei Modi angeboten wird: ohne erweiterte Sicherheitsfeatures (kostenlos) und mit erweiterten Sicherheitsfeatures, die über die Microsoft Defender für Cloud-Pläne verfügbar sind. In dieser Aufgabe erfahren Sie, wie Sie die verschiedenen Microsoft Defender für Cloud-Pläne aktivieren/deaktivieren.

1. Wählen Sie auf der Übersichtsseite von Microsoft Defender für Cloud im linken Navigationsbereich **Umgebungseinstellungen** aus.
1. Wählen Sie das Größer-als-Zeichen **>** neben „Mandantenstammgruppe“ aus, um sie zu erweitern (wählen Sie „Mandantenstammgruppe“ nicht direkt aus, da Sie dann zu einer anderen Seite geleitet werden). Wählen Sie dann **Azure Pass – Sponsorship** aus.
1. Beachten Sie auf der Seite mit den Defender-Plänen, wie Sie alle Pläne aktivieren oder einzelne Defender-Pläne auswählen können. Übernehmen Sie die Einstellungen unverändert (alle Pläne deaktiviert).
1. Schließen Sie alle geöffneten Browserregisterkarten.

### <a name="review"></a>Überprüfung

In diesem Lab haben Sie Defender für Cloud erkundet und erfahren, wie Sie mithilfe der Azure-Sicherheitsbewertung den Sicherheitsstatus Ihrer Organisation verbessern können.
