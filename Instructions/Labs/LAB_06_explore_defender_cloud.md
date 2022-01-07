---
lab:
    title: 'Erkunden von Microsoft Defender für Cloud'
    module: 'Modul 3, Lektion 2: Beschreiben der Funktionen der Microsoft-Sicherheitslösungen: Beschreiben der Sicherheitsverwaltungsfunktionen von Azure'
---

# Lab: Erkunden von Microsoft Defender für Cloud

## Labszenario
In diesem Lab durchlaufen Sie Microsoft Defender für Cloud und erfahren, wie die Azure-Sicherheitsbewertung verwendet werden kann, um die Sicherheitslage Ihrer Organisation zu verbessern.

**Geschätzte Dauer**: 30 Minuten

#### Aufgabe 1: In dieser Aufgabe erhalten Sie eine kurze Einführung in Microsoft Defender für Cloud.
1.	Öffnen Sie Microsoft Edge. Geben Sie **portal.azure.com** in die Adressleiste ein.

1. Melden Sie sich mit Ihren Administratoranmeldeinformationen an.
    1. Geben Sie **admin@WWLxZZZZZZ.onmicrosoft.com** (ZZZZZZ ist hierbei die eindeutige Mandanten-ID, die von Ihrem Labhostinganbieter bereitgestellt wurde) in das Fenster „Anmelden“ ein, und wählen Sie dann **Weiter** aus.
    1. Geben Sie das Administratorkennwort ein, das Sie vom Labhostinganbieter erhalten haben sollten. Wählen Sie **Anmelden** aus.
    1. Wählen Sie **Ja** aus, wenn Sie gefragt werden, ob Sie angemeldet bleiben möchten.

1. Wählen Sie in der oberen linken Ecke des Bildschirms neben dem Text „Microsoft Azure“ das Symbol „Portalmenü anzeigen“ (die drei horizontalen Linien werden auch als Hamburgersymbol bezeichnet) und wählen Sie dann aus dem linken Navigationsbereich unter „Favoriten“ die Option **Microsoft Defender für Cloud** aus.  Wenn diese Option nicht unter „Favoriten“ aufgeführt ist, geben Sie im Suchfeld **Microsoft Defender für Cloud** ein und wählen Sie aus der Ergebnisliste **Microsoft Defender für Cloud** aus.

1. Beachten Sie die auf der Übersichtsseite von Microsoft Defender für Cloud verfügbaren Informationen.  

1. Möglicherweise wird oben auf der Seite ein blaues Informationsfeld angezeigt, das darauf hinweist, dass Sie eventuell nicht alle Informationen sehen.  Wählen Sie **Hier klicken** aus.
    1. Weisen Sie sich selbst die erforderliche Roll zu, um sicherzustellen, dass Sie über die mandantenweite Sichtbarkeit verfügen.  Wählen Sie **Sicherheitsadministrator** aus. Wählen Sie dann unten auf der Seite **Zugriff anfordern** aus.
    1. Wahrscheinlich wird die Meldung „Stammverwaltungsgruppe ist nicht vorhanden“ angezeigt.  Laut Beschreibung wird die Gruppe vom System für Sie erstellt.  Dies kann bis zu 15 Minuten dauern (geht aber in der Regel schneller).  Nachdem der Zugriff gewährt wurde, wählen Sie in der linken oberen Ecke der Seite neben dem Text „Berechtigungen abrufen“ die Option **Microsoft Defender für Cloud** aus, und aktualisieren Sie dann die Übersichtsseite von Microsoft Defender für Cloud.

1. Oben auf der Seite finden Sie Informationen wie die Anzahl der Azure-Abonnements, die Anzahl der bewerteten Ressourcen, die Anzahl der aktiven Empfehlungen und alle Sicherheitswarnungen.  In der Mitte der Seite befinden sich Karten für die Sicherheitsbewertung, die Einhaltung gesetzlicher Bestimmungen, Insights, Azure Defender und mehr.  

1. Wählen Sie oben auf der Seite die Option **Bewertete Ressourcen** aus.  (Beachten Sie, dass dies der Auswahl von „Bestand“ aus dem linken Navigationsbereich der Startseite von Microsoft Defender für Cloud entspricht.)
    1. Dadurch gelangen Sie zur Seite **Inventar**, auf der Ihr Azure Pass-Abonnement angezeigt wird.  Wählen Sie **Azure Pass-Förderung** aus.
    1. Auf der Seite „Resource Health“ finden Sie eine Liste mit Empfehlungen.  Wählen Sie in der verfügbaren Liste die Option **Ihrem Abonnement sollte mehr als ein Besitzer zugewiesen sein** aus.
    1. Wählen Sie den Dropdownpfeil neben den Wartungsschritten aus. Beachten Sie, dass ausführliche Schritte zur Wartung sowie eine entsprechende Option für Gegenmaßnahmen angezeigt werden.  
    1. Wählen Sie das **Microsoft Defender für Cloud** oben rechts auf dem Bildschirm aus, um zur Übersichtsseite von Microsoft Defender für Cloud zurückzukehren.

1. Wählen Sie oben auf der Seite die Option **Aktive Empfehlungen** aus.  (Beachten Sie, dass dies der Auswahl von „Empfehlungen“ aus dem linken Navigationsbereich der Startseite von Microsoft Defender für Cloud entspricht.)
    1. Auf der Empfehlungsseite wird Ihr Sicherheitsbewertungs-Dashboard angezeigt.
    1. Unter dem Sicherheitsbewertungs-Dashboard finden Sie eine Liste von Kontrollen. Jede Sicherheitskontrolle stellt ein Sicherheitsrisiko dar, das eingedämmt werden sollte, und enthält außerdem Angaben zur maximalen Bewertung, die mit dieser Kontrolle verbunden ist, zur aktuellen Bewertung, zur potenziellen Erhöhung der Bewertung und zum Integritätsstatus der Ressourcen.  
    1. Wählen Sie eine Steuerung aus, wie etwa **MFA aktivieren**.  Wählen Sie ein Unterelement aus, wie etwa **Für Konten mit Besitzerberechtigungen für Ihr Abonnement muss MFA aktiviert sein**.  Auf der daraufhin geöffneten Seite werden Ihnen eine Beschreibung, Schritte zur Wartung und betroffene Ressourcen angezeigt. Schließen Sie diese Seite mit dem **X** oben rechts auf dem Bildschirm.
    1. Schließen Sie die Empfehlungsseite mit dem **X** oben rechts auf dem Bildschirm, um zur Übersichtsseite zurückzukehren.

1. Wählen Sie auf der Hauptseite **Einhaltung gesetzlicher Bestimmungen** aus. Auf der Seite „Einhaltung gesetzlicher Bestimmungen“ finden Sie eine Liste mit Compliancekontrollen.  Unter jeder Kontrolle befinden sich eine Reihe von Bewertungen, die auf dem Azure-Sicherheitsvergleichstest basieren. Dieser liefert Empfehlungen dazu, wie Sie Ihre Cloudlösungen auf Azure schützen können.
    1. Wählen Sie **IM** aus. **Identitätsmanagement**, und wählen Sie dann **IM-6 Sichere Authentifizierungskontrollen verwenden** aus.  In der Liste werden Aktionen zur Verbesserung der Compliancesituation aufgeführt, für die der Kunde verantwortlich ist.
    1. Wählen Sie das **X** oben rechts auf dem Bildschirm aus, um die Seite zu schließen und zur Übersichtsseite von Microsoft Defender für Cloud zurückzukehren. 
    1. Lassen Sie Übersichtsseite von Microsoft Defender für Cloud geöffnet, da Sie sie in der nächsten Aufgabe verwenden werden.


#### Aufgabe 2: Bei dieser Aufgabe navigieren Sie zur Azure-Sicherheitsbewertung und erkunden Empfehlungen, die Ihre Sicherheitsbewertung verbessern können. 

1. Wählen Sie auf der Übersichtsseite von Microsoft Defender für Cloud die Karte **Sicherheitsbewertung** aus.
1. Wählen Sie **Azure Pass-Förderung** aus.  Beachten Sie Ihre Sicherheitsbewertung.
1. Wählen Sie auf der Empfehlungsseite die Option zum **Implementieren von Best Practices für Sicherheit** aus, um die Liste zu erweitern. Beachten Sie, dass der Ressourcenintegritätsstatus in Rot angezeigt wird.
1. Wählen Sie das Element **Ihrem Abonnement muss mehr als ein Besitzer zugewiesen sein** aus, das den Ressourcenintegritätsstatus in Rot anzeigt. 
1. Stellen Sie unter dem Text **Betroffene Ressourcen** sicher, dass fehlerhafte Ressourcen ausgewählt/unterstrichen sind, und wählen Sie dann das aufgeführte Azure-Abonnement aus.
1. Wählen Sie oben auf der Seite „Zugriffssteuerung (IAM)“ die Option **+ Hinzufügen** aus. Wählen Sie dann aus dem Dropdown den Eintrag **Rollenzuweisung hinzufügen** aus.
    1. Wählen Sie auf der linken Seite der Seite **Besitzer** aus (dies sollte das erste aufgeführte Elemente sein), damit die Zeile in grau hervorgehoben wird. Wählen Sie dann am unteren Rand der Seite **Weiter** aus.
    1. Wählen Sie neben dem Text „Mitglieder“ die Option **+ Mitglieder auswählen** aus. 
    1. Wählen Sie im Fenster „Mitglieder auswählen“, das auf der rechten Seite des Bildschirms geöffnet wird, **Alex Wilber** aus und klicken Sie am unteren Rand der Seite auf **Auswählen**.  
    1. Überprüfen Sie auf der Seite „Rollenzuweisung hinzufügen“, dass Alex Wilber als Mitglied aufgeführt ist. Wählen Sie dann **Weiter** gefolgt von **Überprüfen + Zuweisen**.
    1. Es kann bis zu 24 Stunden dauern, bis der Status aktualisiert wird. Danach wird auch Ihre Sicherheitsbewertung aktualisiert, da alle Elemente in der Gruppe „Zugriff und Berechtigungen verwalten“ erfüllt sind.
    1. Wählen Sie in der linken oberen Ecke des Seite über dem Text „Azure Pass“ die Option **Microsoft Defender für Cloud** aus, um zur Übersichtsseite von Microsoft Defender für Cloud zurückzukehren.
1. Lassen Sie diese Seite für die nachfolgende Aufgabe geöffnet.


#### Aufgabe 3:  Bedenken Sie, dass Microsoft Defender für Cloud in zwei Modi angeboten wird: ohne verbesserte Sicherheitsfunktionen (kostenlos) und mit verbesserten Sicherheitsfunktionen, die über die Microsoft Defender für Cloud-Pläne verfügbar sind. In dieser Aufgabe erfahren Sie, wie Sie die verschiedenen Pläne für Microsoft Defender für Cloud aktivieren/deaktivieren.

1.	Wählen Sie auf der Übersichtsseite von Microsoft Defender für Cloud die Option **Umgebungseinstellungen** im linken Navigationsbereich aus.
1. Wählen Sie das Größer-als-Zeichen **>** neben dem Text „Mandantenstammgruppe“ aus, um sie zu erweitern (wählen Sie die Mandantenstammgruppe nicht direkt aus, da Sie sonst zu einer anderen Seite geleitet werden). Wählen Sie dann **Azure Pass-Förderung** aus.
1.	Beachten Sie auf der Seite mit den Defender-Plänen, dass Sie alle Defender-Pläne aktivieren oder einzelne Pläne auswählen können. Lassen Sie die Einstellungen wie sie sind, sodass alle Pläne deaktiviert sind.
1.	Sie können nun die Browserregisterkarte schließen, um das Azure-Portal zu beenden.


#### Überprüfung
In diesem Lab haben Sie Microsoft Defender für Cloud erkundet und erfahren, wie die Azure-Sicherheitsbewertung verwendet werden kann, um die Sicherheitslage Ihrer Organisation zu verbessern.
