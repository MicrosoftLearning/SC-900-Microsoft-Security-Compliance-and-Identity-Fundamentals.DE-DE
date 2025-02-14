---
lab:
  title: Erkunden des Microsoft Defender-Portals
  module: Describe the threat protection capabilities of Microsoft XDR
---

# Lab: Erkunden des Microsoft Defender-Portals

Dieses Lab ist den folgenden Learn-Inhalten zugeordnet:

- Lernpfad: Beschreiben der Funktionen von Microsoft-Sicherheitslösungen
- Modul: Beschreiben Sie die Funktionen von Microsoft Defender XDR zum Bedrohungsschutz
- Einheit: Beschreiben Sie das Microsoft Defender Portal

## Labszenario

In diesem Lab erkunden Sie das Microsoft Defender-Portal, indem Sie die auf der Startseite angezeigten Inhalte durchgehen. Außerdem erkunden Sie die Optionen im Navigationsbereich, die einen schnellen Zugriff auf die Funktionen bieten, die Bestandteil der Lösung für Extended Detection and Response (XDR) von Microsoft sind: Microsoft Defender for Endpoint und Microsoft Defender für Office 365 (E-Mail und Zusammenarbeit).  Als Letztes erkunden Sie zudem, wie Organisationen mithilfe der Microsoft-Sicherheitsbewertung ihre Sicherheitsstatus verbessern können.

**Geschätzte Dauer**: 30 Minuten

### Aufgabe 1

Erkunden Sie die Microsoft Defender Landing Page.

1. Öffnen Sie Microsoft Edge. Geben Sie **admin.microsoft.com** in die Adressleiste ein.

1. Melden Sie sich mit Ihren Administratoranmeldeinformationen an.
    1. Geben Sie **admin@WWLxZZZZZZ.onmicrosoft.com** (ZZZZZZ ist hierbei die eindeutige Mandanten-ID, die von Ihrem Lab-Hostinganbieter bereitgestellt wurde) in das Anmeldefenster ein, und wählen Sie dann **Weiter** aus.
    1. Geben Sie das Administratorkennwort ein, das von Ihrem Lab-Hostinganbieter bereitgestellt wird. Wählen Sie **Anmelden**.
    1. Je nach Ihrem Lab-Hoster und abhängig davon, ob Sie sich zum ersten Mal beim Mandanten anmelden, werden Sie möglicherweise aufgefordert, den MFA-Registrierungsprozess abzuschließen. Wenn ja, befolgen Sie die Anweisungen auf dem Bildschirm, um MFA einzurichten.
    1. Sobald Sie angemeldet sind, werden Sie zur Seite „Microsoft 365 Admin Center“ weitergeleitet.

1. Wählen Sie im linken Navigationsbereich des Microsoft 365 Admin Centers **Sicherheit** aus.  Wenn die Option „Sicherheit“ nicht aufgeführt ist, wählen Sie **Alle anzeigen** und dann **Sicherheit** aus.  Eine neue Browserseite öffnet sich mit der Willkommensseite des Microsoft Defender-Portals.  

1. Wenn Sie das Microsoft 365 Defender-Portal das erste Mal besuchen, wird möglicherweise ein Popupfenster für eine Schnelleinführung angezeigt.  Sie können die kurze Tour machen oder das Fenster schließen.

1. Die Startseite des Microsoft Defender-Portals zeigt viele der gängigen Karten, die Sicherheitsteams benötigen. Die Zusammenstellung von Karten und Daten hängt von der Rolle des/der Benutzer*in ab. Scrollen Sie durch die Seite, um den Standardsatz von Karten für Ihre Rolle als globale(r) Administrator*in anzuzeigen.

1. Die angezeigten Karten können an Ihre Präferenz angepasst werden.  Klicken Sie auf **+ Karten hinzufügen**. Es wird ein Fenster geöffnet, in dem alle Karten angezeigt werden, die zur Startseite hinzugefügt werden können.  Möglicherweise haben Sie bereits alle Karten angezeigt. In diesem Fall sehen Sie den Hinweis "Sie haben bereits alle Karten auf Ihrer Startseite". Schließen Sie das Fenster, indem Sie in der oberen rechten Ecke des Fensters auf das **X** klicken.

1. Wenn Sie die Auslassungspunkte oben rechts auf einer Karte auswählen, können Sie die Karte von der Startseite entfernen.  

1. Sie können die Karten auch verschieben. Bewegen Sie den Mauszeiger über die Titelleiste einer beliebigen Karte. Sobald ein kreuzförmiger Cursor angezeigt wird, wählen Sie die Karte aus, und verschieben Sie sie an die gewünschte Position.  

1. Einige Karten verfügen über Schaltflächen unten auf der Karte, die auswählbar sind. Der Titel einiger Karten dient als Link zur Seite für dieses Thema.  Wenn Sie beispielsweise den Titel der Microsoft Secure Score-Karte auswählen, werden Sie zur Microsoft Secure Score-Seite weitergeleitet.  In einem späteren Abschnitt dieses Labs erfahren Sie mehr über den Microsoft Secure Score.

1. Schließen Sie dieses Browserfenster nicht.

### Aufgabe 2

In diesem Teil des Labs werden einige der Optionen vorgestellt, die über das linke Navigationsfeld des Defender-Portals verfügbar sind.  Mit dem Microsoft Defender-Portal löst Microsoft die Zusage einer einheitlichen Security Operations Plattform ein. Das Microsoft Defender-Portal kombiniert Schutz, Erkennung, Untersuchung und Reaktion auf Bedrohungen in Ihrer gesamten Organisation und alle zugehörigen Komponenten an einem zentralen Ort.  

1. Erkunden Sie den linken Navigationsbereich nach Belieben.

1. Um zur Startseite des Microsoft Defender-Portals zurückzukehren, wählen Sie **Startseite** im linken Navigationsbereich aus.

### Aufgabe 3

Bei dieser Aufgabe erkunden Sie, wie Organisationen mithilfe der Microsoft-Sicherheitsbewertung ihre Sicherheitsstatus verbessern können.

1. Sie sollten sich immer noch im Microsoft Defender-Portal befinden. Erweitern Sie im linken Navigationsbereich **Exposure Management** und wählen Sie dann **Secure Score** aus.  Wenn „Exposure Management“ in Ihrem Mandanten nicht angezeigt wird, scrollen Sie auf der Startseite des Microsoft Defender-Portals nach unten, bis Sie die Karte für **Microsoft Secure Score** sehen. Wählen Sie den Titel der Karte aus (der Text wird blau, wenn Sie den Mauszeiger über den Titel der Karte bewegen).

1. Die Seite „Microsoft-Sicherheitsbewertung“ wird auf der Registerkarte „Übersicht“ geöffnet. Die Microsoft-Sicherheitsbewertung ist eine Messung des Sicherheitsstatus einer Organisation. Der Sicherheitsstatus Ihrer Organisation wird als Prozentsatz zusammen mit der Anzahl der Punkte angezeigt, die Sie von den insgesamt möglichen Punkten erreicht haben, und nach Kategorie aufgeschlüsselt. Wählen Sie **Einschließen** neben „Ihre Sicherheitsbewertung“ aus.  Ein kleines Fenster wird geöffnet, in dem Sie die erreichbare Bewertung, die geplante Bewertung und die aktuelle Lizenzbewertung in die Aufschlüsselung der Sicherheitsbewertung Ihrer Organisation einfügen können.  Wählen Sie erneut **Einschließen** aus, um das Fenster zu schließen.

1. Zudem enthält die Überblicksseite die wichtigsten Verbesserungsmaßnahmen, die Vergleichsbewertung, den Verlauf und zusätzliche Ressourcen.

1. Wählen Sie oben auf der Seite **Verbesserungsaktionen** aus.  Beachten Sie die in der Tabelle verfügbaren Informationen.  

1. Wählen Sie den ersten Punkt aus der Liste aus und überprüfen Sie die verfügbaren Informationen. Beachten Sie im Fenster, das geöffnet wird, die verfügbaren Statusoptionen. Wählen Sie die Registerkarte **Implementierung** aus, um Informationen zur Implementierung anzuzeigen. Klicken Sie oben rechts auf das **X**, um dieses Fenster zu schließen.

1. Wählen Sie oben auf der Seite die Registerkarte **Verlauf** aus.  Für jede aufgeführte Aktivität gibt es eine kurze Anweisung, die Kontext bereitstellt.  Wählen Sie ein Element aus der Verlaufstabelle aus.  Wählen Sie oben rechts auf der Detailseite unter „Verlauf“ ** X Ereignisse** aus (wobei X eine Zahl ist).  Das Fenster „Aktionsverlauf“ wird geöffnet und bietet weitere Informationen.  Klicken Sie auf **Schließen** unten auf der Seite und dann auf  **X** oben rechts auf der Detailseite, um zur Seite „Verlauf“ zurückzukehren.

1. Wählen Sie oben auf der Seite **Metriken und Trends** aus.  Beachten Sie die verfügbaren Informationen.  Klicken Sie rechts oben auf der Seite auf das **Kalendersymbol**.  Sie können die Ansicht auf einen benutzerdefinierten Datumsbereich einschränken.  Durch die Auswahl des **Filtersymbols** können Sie die Ansicht nach Identität und/oder Apps filtern.  Schließen Sie das Fenster und wählen Sie **Startseite** in der linken Navigationsleiste, um zur Startseite von Microsoft Defender zurückzukehren.

1. Schließen Sie alle geöffneten Browserregisterkarten.

### Überprüfung

In diesem Lab haben Sie das Microsoft Defender-Portal erkundet, indem Sie die auf der Landing Page angezeigten Inhalte durchgelesen haben. Sie haben die Optionen im Navigationsbereich erkundet, die einen schnellen Zugriff auf die Funktionalitäten bereitstellen, die Teil der XDR-Lösung (Extended Detection and Response) von Microsoft, Microsoft Defender für Endpunkte und Microsoft Defender für Office 365 (E-Mail und Zusammenarbeit) sind.  Als Letztes erkunden Sie zudem, wie Organisationen mithilfe der Microsoft-Sicherheitsbewertung ihren Sicherheitsstatus verbessern können.
