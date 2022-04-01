---
lab:
  title: Erkunden des Microsoft 365 Defender-Portals
  module: 'Module 3 Lesson 5: Describe the capabilities of Microsoft security solutions: Describe security management capabilities of Microsoft 365'
ms.openlocfilehash: f123071ebcb702532c3c7c8eb76c72d6c4d41047
ms.sourcegitcommit: a341c2fc38e9b37dafb792d82e3c948f7ba4a099
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/14/2022
ms.locfileid: "137893990"
---
# <a name="lab-explore-the-microsoft-365-defender-portal"></a>Lab: Erkunden des Microsoft 365 Defender-Portals

## <a name="lab-scenario"></a>Labszenario
In diesem Lab erkunden Sie das Microsoft 365 Defender-Portal, indem Sie den auf der Landing Page angezeigten Inhalt durchgehen. Außerdem erkunden Sie die Optionen im Navigationsbereich, die einen schnellen Zugriff auf die Funktionen bieten, die Bestandteil der Lösung für Extended Detection and Response (XDR) von Microsoft sind: Microsoft Defender für Endpunkt und Microsoft Defender für Office 365 (E-Mail und Zusammenarbeit).  Als Letztes erkunden Sie zudem, wie Organisationen mithilfe der Microsoft-Sicherheitsbewertung ihre Sicherheitsstatus verbessern können.


**Geschätzte Dauer**: 10–15 Minuten

#### <a name="task-1--explore-the-microsoft-365-defender-landing-page"></a>Aufgabe 1:  Erkunden der Landing Page von Microsoft 365 Defender

1. Öffnen Sie Microsoft Edge. Geben Sie **admin.microsoft.com** in die Adressleiste ein.

1. Melden Sie sich mit Ihren Administratoranmeldeinformationen an.
    1. Geben Sie **admin@WWLxZZZZZZ.onmicrosoft.com** (ZZZZZZ ist hierbei die eindeutige Mandanten-ID, die von Ihrem Labhostinganbieter bereitgestellt wurde) in das Fenster „Anmelden“ ein, und wählen Sie dann **Weiter** aus.
   
    1. Geben Sie das Administratorkennwort ein, das Sie vom Labhostinganbieter erhalten haben sollten. Wählen Sie **Anmelden**.
    1. Wählen Sie **Ja** aus, wenn Sie gefragt werden, ob Sie angemeldet bleiben möchten. Dadurch gelangen Sie zur Seite „Microsoft 365 Admin Center“.

1. Wählen Sie im linken Navigationsbereich von Microsoft 365 Admin Center **Sicherheit** aus.  Wenn die Option „Sicherheit“ nicht aufgeführt ist, wählen Sie **Alle anzeigen** und dann **Sicherheit** aus.  Die Startseite des Microsoft 365 Defender-Portals wird auf einer neuen Browserseite geöffnet.  

1. Wenn Sie das Microsoft 365 Defender-Portal das erste Mal besuchen, wird möglicherweise ein Popupfenster für eine Schnelleinführung angezeigt.  Sie sollten die Tour absolvieren.  Wählen Sie **Schnelleinführung absolvieren** aus.  Lesen Sie die in jedem Popupfenster angegebene Beschreibung, und wählen Sie **Weiter** aus. Setzen Sie die Tour bis zum Ende fort. Wählen Sie dann **Fertig** aus.

1. Der linke Navigationsbereich enthält Links zu bzw. bietet Zugriff auf Informationen, die Teil der Extended Detection and Response-Lösung von Microsoft (XDR-Lösung) sind. Dazu zählen Incidents und Warnungen, Hunting, Action Center, Bedrohungsanalysen, sicherer Speicher und vieles mehr.  Zudem ermöglicht er den Schnellzugriff auf Microsoft Defender für Endpunkt (die unter „Endpunkte“ aufgelisteten Links) und auf Defender für Office 365 (die unter „E-Mail und Zusammenarbeit“ aufgelisteten Links).  Erkunden Sie diese Optionen, indem Sie einige der Links auswählen.   Wählen Sie im linken Navigationsbereich die Option **Startseite** aus, um zur Startseite des Microsoft 365 Defender-Portals zurückzukehren.  Hinweis: Auf diesen Registerkarten sind möglicherweise nicht viele Informationen aufgelistet, da keine Geräte angefügt sind und dafür möglicherweise keine aktiven Bedrohungen oder Warnungen vorhanden sind.

1. Auf der Startseite des Microsoft 365 Defender-Portals werden viele der allgemeinen Karten angezeigt, die von Sicherheitsteams benötigt werden. Die Zusammenstellung von Karten und Daten hängt von der Benutzerrolle ab. Scrollen Sie durch die Seite, um den Standardsatz der Karten für Ihre Rolle als globaler Administrator anzuzeigen.

1. Sie können anpassen, welche Karten angezeigt werden.  Wählen Sie **+ Karten hinzufügen** aus. Ein Fenster wird geöffnet. Darin wird angegeben, dass Sie bereits über alle Karten auf Ihrer Startseite verfügen.  Schließen Sie das Fenster, indem Sie in der oberen rechten Ecke des Fensters auf das **X** klicken.

1. Durch Auswahl der Auslassungspunkte im oberen rechten Bereich einer beliebigen Karte werden weitere Aktionen bereitgestellt, die vorgenommen werden können.  

1. Sie können die Karten auch verschieben. Bewegen Sie den Mauszeiger über die Titelleiste einer beliebigen Karte. Sobald ein kreuzförmiger Cursor angezeigt wird, wählen Sie die Karte aus, und verschieben Sie sie an die gewünschte Position.

1. Indem Sie den Titel einer Karte auswählen, erhalten Sie zusätzliche Informationen zu diesem Thema. Dies erkunden Sie bei der nächsten Aufgabe.  Lassen Sie das Browserfenster geöffnet.

#### <a name="task-2-in-this-task-you-will-explore-how-microsoft-secure-score-can-help-an-organization-improve-its-security-posture"></a>Aufgabe 2: Bei dieser Aufgabe erkunden Sie, wie Organisationen mithilfe der Microsoft-Sicherheitsbewertung ihre Sicherheitsstatus verbessern können.

1. Wählen Sie auf der Startseite des Microsoft 365 Defender-Portals auf der Titelleiste der Karte (der Text wird blau) die Option **Microsoft-Sicherheitsbewertung** aus.  Alternativ können Sie **Sicherheitsbewertung** im linken Navigationsbereich auswählen.

1. Die Registerkarte „Übersicht“ der Seite „Microsoft-Sicherheitsbewertung“ wird geöffnet.  Mithilfe der Microsoft-Sicherheitsbewertung wird der Sicherheitsstatus einer Organisation gemessen. Der Sicherheitsstatus Ihrer Organisation wird als Prozentsatz zusammen mit der Anzahl der Punkte angezeigt, die Sie von den insgesamt möglichen Punkten erreicht haben, und nach Kategorie aufgeschlüsselt. Wählen Sie **Einschließen** neben „Ihre Sicherheitsbewertung“ aus.  Ein kleines Fenster wird geöffnet, in dem Sie die erreichbare Bewertung, die geplante Bewertung und die aktuelle Lizenzbewertung in die Aufschlüsselung der Sicherheitsbewertung Ihrer Organisation einfügen können.  Wählen Sie erneut **Einschließen** aus, um das Fenster zu schließen.

1. Zudem enthält die Übersichtsseite die wichtigsten Verbesserungsaktionen, die Vergleichsbewertung, den Verlauf und zusätzliche Ressourcen.

1. Wählen Sie oben auf der Seite **Verbesserungsaktionen** aus.  Beachten Sie die in der Tabelle für jedes Element enthaltenen Informationen, etwa „Bewertungsauswirkung“ und „Erzielte Punkte“.  

1. Durch Auswahl eines Elements aus der Liste werden ausführliche Informationen bereitgestellt.  Wählen Sie **MFA für Administratorrollen anfordern** aus.  Wählen Sie **Status bearbeiten & Aktionsplan** aus.  Notieren Sie sich im geöffneten Fenster die verfügbaren Statusoptionen. Klicken Sie oben rechts auf das **X**, um dieses Fenster zu schließen.

1. Wählen Sie unten auf der Seite **In Microsoft Azure verwalten** aus.  Eine neue Browserregisterkarte wird geöffnet, und Sie gelangen direkt zur Seite „Richtlinie für bedingten Zugriff“.  Nach Abschluss der Lab-Übung „Bedingter Zugriff“ sollte die Richtlinie aufgelistet werden. Kehren Sie in Ihrem Browser zur Registerkarte „Microsoft-Sicherheitsbewertung“ zurück, um zur Seite „Verbesserungsaktion“ für „MFA für Administratorrollen anfordern“ zurückzukehren. Wählen Sie in der oberen rechten Ecke des Fensters das **X** aus, um dieses Fenster zu schließen und um zur Seite „Verbesserungsaktionen“ zurückzukehren.

1. Wählen Sie oben auf der Seite die Registerkarte **Verlauf** aus.  Für einige Aktivitäten werden möglicherweise negative Punkte angezeigt.  Wie im Aktivitätsfeld beschrieben, kann dies daran liegen, dass ein Element entfernt wurde, weil es nicht mehr relevant war.  Wählen Sie ein Element aus der Verlaufstabelle aus.  Eine detaillierte Seite für das ausgewählte Element wird geöffnet.  Erkunden Sie die verfügbaren Optionen.  Um die Detailseite zu verlassen und zur Seite „Verlauf“ zurückzukehren, wählen Sie das **X** oben rechts auf der Seite aus.

1. Wählen Sie oben auf der Seite **Metriken und Trends** aus.  Beachten Sie die verfügbaren Informationen.  Wählen Sie in der oberen rechten Ecke der Seite das **Kalendersymbol** aus.  Sie können die Ansicht auf einen benutzerdefinierten Datumsbereich eingrenzen.  Durch die Auswahl des **Filtersymbols** können Sie die Ansicht nach Identität, Geräte bzw. Apps filtern.  Schließen Sie das Fenster, und wählen Sie im linken Navigationsbereich die Option **Startseite** aus, um zur Startseite von Microsoft 365 Defender zurückzukehren.

1. Schließen Sie die Browserseite.

#### <a name="review"></a>Überprüfung
In diesem Lab haben Sie das Microsoft 365 Defender-Portal erkundet, indem Sie den auf der Landing Page angezeigten Inhalt durchgegangen sind. Außerdem haben Sie die Optionen im Navigationsbereich erkundet, die einen Schnellzugriff auf Funktionen ermöglichen, die Bestandteil der Microsoft-Lösung für Extended Detection and Response (XDR), von Microsoft Defender für Endpunkt und von Microsoft Defender für Office 365 (E-Mail und Zusammenarbeit) sind.  Als Letztes haben Sie erkundet, wie Organisationen mithilfe der Microsoft-Sicherheitsbewertung ihre Sicherheitsstatus verbessern können.
