---
lab:
  title: Erkunden von Microsoft Defender für Cloud
  module: 'Module 3 Lesson 2: Describe the capabilities of Microsoft security solutions: Describe security management capabilities of Azure'
ms.openlocfilehash: 208e11a7e82497fbb900b4fa024fb6fb367d458e
ms.sourcegitcommit: a341c2fc38e9b37dafb792d82e3c948f7ba4a099
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/14/2022
ms.locfileid: "137893991"
---
# <a name="lab-explore-microsoft-defender-for-cloud"></a>Lab: Erkunden von Microsoft Defender für Cloud

## <a name="lab-scenario"></a>Labszenario
In diesem Lab erkunden Sie Defender für Cloud und erfahren, wie Sie mithilfe der Azure-Sicherheitsbewertung den Sicherheitsstatus Ihrer Organisation verbessern können.

**Geschätzte Dauer**: 30 Minuten

#### <a name="task-1-in-this-task-you-will-take-a-brief-tour-of-microsoft-defender-for-cloud"></a>Aufgabe 1: In dieser Aufgabe erhalten Sie einen kurzen Überblick über Microsoft Defender für Cloud.
1.  Öffnen Sie Microsoft Edge. Geben Sie **portal.azure.com** in die Adressleiste ein.

1. Melden Sie sich mit Ihren Administratoranmeldeinformationen an.
    1. Geben Sie **admin@WWLxZZZZZZ.onmicrosoft.com** (ZZZZZZ ist hierbei die eindeutige Mandanten-ID, die von Ihrem Labhostinganbieter bereitgestellt wurde) in das Fenster „Anmelden“ ein, und wählen Sie dann **Weiter** aus.
    1. Geben Sie das Administratorkennwort ein, das Sie vom Labhostinganbieter erhalten haben sollten. Wählen Sie **Anmelden**.
    1. Wählen Sie **Ja** aus, wenn Sie gefragt werden, ob Sie angemeldet bleiben möchten.

1. Wählen Sie in der oberen linken Ecke des Bildschirms neben dem Text „Microsoft Azure“ das Symbol „Portalmenü anzeigen“ (die drei horizontalen Linien werden auch als Hamburgersymbol bezeichnet) und dann im linken Navigationsbereich unter „Favoriten“ **Microsoft Defender für Cloud** aus.  Wenn die Option unter „Favoriten“ nicht aufgeführt ist, geben Sie im Suchfeld **Microsoft Defender für Cloud** ein, und wählen Sie dann in der Ergebnisliste **Microsoft Defender für Cloud** aus.

1. Beachten Sie die Informationen, die auf der Übersichtsseite von Microsoft Defender für Cloud verfügbar sind.  

1. Möglicherweise wird oben auf der Seite ein blaues Informationsfeld angezeigt, das darauf hinweist, dass Sie möglicherweise nicht alle Informationen sehen.  Wählen Sie **Hier klicken** aus.
    1. Weisen Sie sich selbst die erforderliche Roll zu, um sicherzustellen, dass Sie über die mandantenweite Sichtbarkeit verfügen.  Wählen Sie **Sicherheitsadministrator** aus. Wählen Sie dann unten auf der Seite **Zugriff anfordern** aus.
    1. Wahrscheinlich wird die Meldung „Stammverwaltungsgruppe ist nicht vorhanden“ angezeigt.  Laut Beschreibung wird die Gruppe vom System für Sie erstellt.  Die Durchführung kann bis zu 15 Minuten dauern (in der Regel aber schneller).  Sobald der Zugriff erteilt wurde, wählen Sie in der oberen linken Ecke der Seite oberhalb von „Berechtigungen abrufen“ die Option **Microsoft Defender für Cloud** aus, und aktualisieren Sie dann die Microsoft Defender für Cloud-Übersichtsseite.

1. Oben auf der Seite finden Sie Informationen wie die Anzahl der Azure-Abonnements, die Anzahl der bewerteten Ressourcen, die Anzahl der aktiven Empfehlungen und alle Sicherheitswarnungen.  In der Mitte der Seite befinden sich Karten für die Sicherheitsbewertung, die Einhaltung gesetzlicher Bestimmungen, Insights und mehr.  

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

1. Wählen Sie auf der Hauptseite **Einhaltung gesetzlicher Bestimmungen** aus. Auf der Seite „Einhaltung gesetzlicher Bestimmungen“ finden Sie eine Liste mit Compliancekontrollen.  Unter jeder Kontrolle befinden sich eine Reihe von Bewertungen, die auf dem Azure-Sicherheitsvergleichstest basieren. Dieser liefert Empfehlungen dazu, wie Sie Ihre Cloudlösungen auf Azure schützen können.
    1. Wählen Sie **IM. Identitätsverwaltung** und dann **IM.6 Verwenden stärkerer Authentifizierungssteuerungen für den gesamten Azure Active Directory-basierten Zugriff** aus.  In der Liste werden Aktionen zur Verbesserung der Compliancesituation aufgeführt, für die der Kunde verantwortlich ist.
    1. Wählen Sie das **X** oben rechts auf dem Bildschirm aus, um die Seite zu schließen und zur Übersichtsseite von Microsoft Defender für Cloud zurückzukehren. 
    1. Lassen Sie die Übersichtsseite von Microsoft Defender für Cloud geöffnet. Sie wird in der nächsten Aufgabe verwendet.


#### <a name="task-2-in-this-task-you-will-navigate-to-azure-secure-score-and-explore-recommendations-that-can-improve-your-secure-score"></a>Aufgabe 2: Bei dieser Aufgabe navigieren Sie zur Azure-Sicherheitsbewertung und erkunden Empfehlungen, die Ihre Sicherheitsbewertung verbessern können. 

1. Wählen Sie auf der Übersichtsseite von Microsoft Defender für Cloud die Karte **Sicherheitsbewertung** aus.
1. Wählen Sie **Azure Pass-Förderung** aus.  Beachten Sie Ihre Sicherheitsbewertung.
1. Wählen Sie auf der Seite „Empfehlungen“ die Option **Best Practices für die Sicherheit implementieren** aus, um die Liste zu erweitern. Beachten Sie, dass der Ressourcenintegritätsstatus rot angezeigt wird.
1. Wählen Sie das Element **Ihrem Abonnement muss mehr als ein Besitzer zugewiesen sein** aus, das den Ressourcenintegritätsstatus in Rot anzeigt. 
1. Stellen Sie sicher, dass unter **Betroffene Ressourcen** „Fehlerhafte Ressourcen“ ausgewählt bzw. unterstrichen ist, und wählen Sie dann das aufgeführte Azure-Abonnement aus.
1. Wählen Sie oben auf der Seite „Zugriffssteuerung (IAM)“ die Option **+ Hinzufügen** aus. Wählen Sie dann aus dem Dropdown den Eintrag **Rollenzuweisung hinzufügen** aus.
    1. Wählen Sie links auf der Seite **Besitzer** aus (dies sollte das erste aufgeführte Element sein), sodass die Zeile grau hervorgehoben ist, und wählen Sie dann unten auf der Seite **Weiter** aus.
    1. Wählen Sie neben „Mitglieder“ die Option **+ Mitglieder auswählen** aus. 
    1. Wählen Sie im Fenster „Mitglieder auswählen“, das auf der rechten Seite des Bildschirms geöffnet wird, **Alex Willber** aus, und klicken Sie dann unten auf der Seite auf **Auswählen**.  
    1. Überprüfen Sie auf der Seite „Rollenzuweisung hinzufügen“, ob Alex Willber als Mitglied aufgeführt ist, und wählen Sie dann **Weiter** sowie **Überprüfen + zuweisen** aus.
    1. Es kann bis zu 24 Stunden dauern, bis der Status aktualisiert wird. Danach wird auch Ihre Sicherheitsbewertung aktualisiert, da alle Elemente in der Gruppe „Zugriff und Berechtigungen verwalten“ erfüllt sind.
    1. Wählen Sie oben links auf der Seite an der Stelle, wo „Azure Pass“ steht, **Microsoft Defender für Cloud** aus, um zur Übersichtsseite von Microsoft Defender für Cloud zurückzukehren.
1. Lassen Sie diese Seite für die nachfolgende Aufgabe geöffnet.


#### <a name="task-3--recall-that-microsoft-defender-for-cloud-is-offered-in-two-modes-without-enhanced-security-features-free-and-with-enhanced-security-features-which-are-available-through-the-microsoft-defender-for-cloud-plans-in-this-task-you-discover-how-to-enabledisable-the-various-microsoft-defender-for-cloud-plans"></a>Aufgabe 3:  Denken Sie daran, dass Microsoft Defender für Cloud in zwei Modi angeboten wird: ohne erweiterte Sicherheitsfeatures (kostenlos) und mit erweiterten Sicherheitsfeatures, die über die Microsoft Defender für Cloud-Pläne verfügbar sind. In dieser Aufgabe erfahren Sie, wie Sie die verschiedenen Microsoft Defender für Cloud-Pläne aktivieren/deaktivieren.

1.  Wählen Sie auf der Übersichtsseite von Microsoft Defender für Cloud im linken Navigationsbereich **Umgebungseinstellungen** aus.
1. Wählen Sie das Größer-als-Zeichen **>** neben „Mandantenstammgruppe“ aus, um sie zu erweitern (wählen Sie „Mandantenstammgruppe“ nicht direkt aus, da Sie dann zu einer anderen Seite geleitet werden). Wählen Sie dann **Azure Pass – Sponsorship** aus.
1.  Beachten Sie auf der Seite mit den Defender-Plänen, wie Sie alle Pläne aktivieren oder einzelne Defender-Pläne auswählen können. Übernehmen Sie die Einstellungen unverändert (alle Pläne deaktiviert).
1.  Sie können nun die Browserregisterkarte schließen, um das Azure-Portal zu beenden.


#### <a name="review"></a>Überprüfung
In diesem Lab haben Sie Defender für Cloud erkundet und erfahren, wie Sie mithilfe der Azure-Sicherheitsbewertung den Sicherheitsstatus Ihrer Organisation verbessern können.

