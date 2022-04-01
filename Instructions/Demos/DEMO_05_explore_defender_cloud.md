---
Demo:
  title: Microsoft Defender für Cloud'
  module: 'Module 3 Lesson 2: Describe the capabilities of Microsoft security solutions: Describe security management capabilities of Azure'
ms.openlocfilehash: 1548f7ff825d472eeb53697342abf8cd48ad084f
ms.sourcegitcommit: a341c2fc38e9b37dafb792d82e3c948f7ba4a099
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/14/2022
ms.locfileid: "137894102"
---
# <a name="demo-microsoft-defender-for-cloud"></a>Demo: Microsoft Defender für Cloud

### <a name="demo-scenario"></a>Demoszenario

In dieser Demo gehen Sie Microsoft Defender für Cloud durch und zeigen, wie der Sicherheitsstatus einer Organisation mit der Azure-Sicherheitsbewertung verbessert werden kann.

1. Öffnen Sie die Browserregisterkarte **Startseite – Microsoft Azure**.  Falls Sie die Registerkarte geschlossen haben, öffnen Sie eine Browserseite. Geben Sie „portal.azure.com“ in die Adressleiste ein, und melden Sie sich erneut an.

1. Geben Sie im Suchfeld in der blauen Leiste oben auf der Seite neben der Stelle, an der Microsoft Azure steht, **Microsoft Defender für Cloud** ein, und wählen Sie dann in den Suchergebnissen **Microsoft Defender für Cloud** aus.

1. Wenn Sie Microsoft Defender für Cloud zum ersten Mal mit Ihrem Abonnement aufrufen, werden Sie möglicherweise zur Seite „Erste Schritte“ geleitet und zur Durchführung eines Upgrades aufgefordert.  Scrollen Sie auf der Seite nach unten, und klicken Sie auf **Skip**.

1. Beachten Sie die Informationen, die auf der Übersichtsseite von Microsoft Defender für Cloud verfügbar sind.  Hinweis: Möglicherweise wird oben auf der Seite ein blaues Informationsfeld angezeigt, das darauf hinweist, dass Sie möglicherweise nicht alle Informationen sehen.  Wählen Sie es nicht aus (die Verarbeitung kann bis zu 15 Minuten dauern und ist für diese Demo nicht erforderlich).

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

1. Sie befinden sich wieder auf der Übersichtsseite von Microsoft Defender für Cloud.  Wählen Sie auf der Hauptseite **Sicherheitsbewertung** aus (genauso können Sie im linken Navigationsbereich „Sicherheitsbewertung“ auswählen).
    1. Dadurch wird das Sicherheitsbewertungs-Dashboard angezeigt.  Darüber hinaus werden verfügbare Verwaltungsgruppen und Abonnements aufgeführt.  Wählen Sie Ihr Azure-Abonnement – Azure Pass-Förderung aus.
    1. Dadurch wird die Empfehlungsseite angezeigt, die zuvor zu sehen war.
    1. Schließen Sie die Empfehlungsseite mit dem **X** oben rechts auf dem Bildschirm.
    1. Schließen Sie die Sicherheitsbewertungsseite mit dem **X** oben rechts auf dem Bildschirm, um zur Übersichtsseite zurückzukehren.

1. Sie befinden sich wieder auf der Übersichtsseite von Microsoft Defender für Cloud.  Wählen Sie auf der Hauptseite **Einhaltung gesetzlicher Bestimmungen** aus. (Beachten Sie, dass Sie genauso auf der Startseite von Microsoft Defender für Cloud im linken Navigationsbereich die Option „Empfehlungen“ auswählen können.)
    1. Auf der Seite „Einhaltung gesetzlicher Bestimmungen“ finden Sie eine Liste mit Compliancekontrollen.  Unter jeder Kontrolle befinden sich eine Reihe von Bewertungen, die auf dem Azure-Sicherheitsvergleichstest basieren. Dieser liefert Empfehlungen dazu, wie Sie Ihre Cloudlösungen auf Azure schützen können.
    1. Wählen Sie **IM. Identitätsverwaltung** und dann **IM.6 Verwenden stärkerer Authentifizierungssteuerungen für den gesamten Azure Active Directory-basierten Zugriff** aus.  In der Liste werden Aktionen zur Verbesserung der Compliancesituation aufgeführt, für die der Kunde verantwortlich ist.
    1. Wählen Sie das **X** oben rechts auf dem Bildschirm aus, um die Seite zu schließen und zur Seite für die Einhaltung gesetzlicher Bestimmungen zurückzukehren.
    1. Wählen Sie das **X** oben rechts auf dem Bildschirm aus, um zur Übersichtsseite zurückzukehren.

1. Kehren Sie zur Startseite des Azure-Portals zurück. Wählen Sie dazu links oben auf der Seite **Startseite** aus.  Lassen Sie diese Browserregisterkarte geöffnet, da Sie diese in einer späteren Demo benötigen.

## <a name="review"></a>Überprüfung

In dieser Demo sind Sie Microsoft Defender für Cloud durchgegangen und haben gezeigt, wie der Sicherheitsstatus einer Organisation mit der Azure-Sicherheitsbewertung verbessert werden kann.

