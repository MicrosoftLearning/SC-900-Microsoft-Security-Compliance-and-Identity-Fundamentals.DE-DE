<!---
---
Demo: Titel: „Microsoft Defender for Cloud“ Lernpfad/Modul/Lerneinheit: „Lernpfad: Beschreiben der Funktionen von Microsoft-Sicherheitslösungen; Modul 2: Beschreiben der Sicherheitsverwaltungsfunktionen von Azure; Lerneinheit 3: Beschreiben von Cloud Security Posture Management“
---
--->

# Demo: Microsoft Defender für Cloud

Diese Demo ist den folgenden Learn-Inhalten zugeordnet:

- Lernpfad: Beschreiben der Funktionen von Microsoft-Sicherheitslösungen
- Modul: Beschreiben der Sicherheitsverwaltungsfunktionen von Azure
- Lerneinheit: Beschreiben von Cloud Security Posture Management

## Vorführungsszenario

In dieser Demo stellen Sie Microsoft Defender for Cloud vor und zeigen, wie der Sicherheitsstatus einer Organisation damit verbessert werden kann.  HINWEIS: Das Azure-Abonnement, das vom Authorized Lab Hoster (AH) verwaltet wird, schränkt möglicherweise einige Zugriffsmöglichkeiten ein führt zu Verzögerungen, die länger als normal sind.

### Teil 1 der Demo

In dieser Demoaufgabe durchlaufen Sie auf hoher Ebene einige der Funktionen von Microsoft Defender for Cloud.

1. Öffnen Sie in der Browser-Registerkarte **Home-Microsoft Azure**.  Falls Sie die Registerkarte geschlossen haben, öffnen Sie eine Browserseite, und geben Sie **https://portal.azure.com** in die Adressleiste ein. Melden Sie sich mit den Azure-Anmeldeinformationen an, die vom autorisierten Labhoster (ALH) bereitgestellt werden.  Sie befinden sich nun auf der Homepage der Azure-Dienste.

1. Geben Sie **Microsoft Defender for Cloud** in die blaue Suchleiste ein, und wählen Sie dann in der Ergebnisliste **Microsoft Defender for Cloud** aus.

1. Wenn Sie Microsoft Defender for Cloud zum ersten Mal mit Ihrem Abonnement aufrufen, werden Sie möglicherweise zur Seite „Erste Schritte“ geleitet und zur Durchführung eines Upgrades aufgefordert.  Scrollen Sie auf der Seite nach unten, und klicken Sie auf **Überspringen**.  Sie gelangen auf die Übersichtsseite. Beachten Sie in der Übersicht von Microsoft Defender für Cloud die auf der Seite verfügbaren Informationen.  Oben auf der Seite finden Sie Informationen wie die Anzahl der Azure-Abonnements, die Anzahl der bewerteten Ressourcen, die Anzahl der aktiven Empfehlungen und alle Sicherheitswarnungen.  In der Mitte der Seite befinden sich Karten für den Sicherheitsstatus, die Einhaltung gesetzlicher Bestimmungen, Insights und mehr.  Für alle Abonnements sind standardmäßig grundlegende CSPM-Features aktiviert. Dadurch wird eine Sicherheitsbewertung bereitgestellt.  
    1. Der Wert der Sicherheitsbewertung wird jedoch als 0 % angezeigt, da Azure eine Verzögerung von bis zu 24 Stunden aufweisen kann, bis eine anfängliche Bewertung angezeigt wird.  
    1. Wichtig ist auch, dass Defender for Cloud eine Multicloudlösung ist, die nicht nur mit Azure, sondern auch mit AWS und Google Cloud Platform Ihren Sicherheitsstatus verbessern kann.

1. Als Erstes sollten Sie zeigen, dass Microsoft Defender for Cloud Microsoft Cloud Security Benchmark als Standardrichtlinieninitiative verwendet.  Wählen Sie im linken Navigationsbereich **Umgebungseinstellungen** aus Wählen Sie im Hauptfenster die Option **Alle erweitern** aus.  In der erweiterten Ansicht wird Ihr Abonnement als blauer Text angezeigt.  Wählen Sie das Abonnement **MOC Subscription--lodXXXXXX** aus.

1. Wählen Sie im linken Navigationsbereich **Sicherheitsrichtlinie** aus. Diese Option ist unter den Richtlinieneinstellungen aufgeführt. Wenn die Standardinitiative nicht zugewiesen ist, wählen Sie **Richtlinie zuweisen** aus.
    1. Beachten Sie, dass auf der Registerkarte „Grundlagen“ die Initiativendefinition „Microsoft Cloud Security Benchmark“ lautet.  Diese ist abgeblendet, da dies die Standardinitiative ist und wir hier nur die Zuweisung durchführen.
    1. Klicken Sie auf **Überprüfen + erstellen** und dann auf **Erstellen**. Wenn Sie möchten, können Sie durch die konfigurierbaren Parameter für die verschiedenen Registerkarten scrollen, bevor Sie die Option zum Überprüfen und Erstellen auswählen.
    1. Dies ist ein wichtiger Schritt, um sicherzustellen, dass Sie Sicherheitsempfehlungen basierend auf Microsoft Cloud Security Benchmark sehen können.  

1. Beachten Sie auch, dass es vorgefertigte Branchenstandards und gesetzliche Bestimmungen gibt, die Sie hinzufügen können. Wenn die aufgeführten Standards als veraltet angezeigt werden, wählen Sie **Weitere Standards hinzufügen** aus, um eine vollständige Liste anzuzeigen.  Wählen Sie einen aus der Liste aus, und fügen Sie ihn dann manuell hinzu, indem Sie **Überprüfen + erstellen** und dann **Erstellen** auswählen.  Sie sehen, dass er der Liste der Branchen- und Standardvorschriften hinzugefügt wird.

1. Wählen Sie **Übersicht** aus.  In der Mitte der Seite befinden sich Karten für den Sicherheitsstatus, die Einhaltung gesetzlicher Bestimmungen, Insights und mehr.  Für alle Abonnements sind grundlegende CSPM-Features aktiviert. Dadurch wird eine Sicherheitsbewertung bereitgestellt. Der Wert wird jedoch als 0 % angezeigt, da Azure eine Verzögerung von bis zu 24 Stunden aufweisen kann, bis eine anfängliche Bewertung angezeigt wird.  Obwohl der Wert der Sicherheitsbewertung derzeit 0 % lautet, weisen Sie darauf hin, dass Defender for Cloud eine Multicloudlösung ist, die nicht nur mit Azure, sondern auch mit AWS und Google Cloud Platform Ihren Sicherheitsstatus verbessern kann.

1. Wählen Sie oben auf der Seite die Option **Bewertete Ressourcen** aus.  (Beachten Sie, dass Sie genauso auf der Startseite von Microsoft Defender für Cloud im linken Navigationsbereich die Option „Inventar“ auswählen können.)
    1. Dadurch gelangen Sie zur Seite **Bestand**, auf der die aktuellen Ressourcen aufgeführt werden. Wählen Sie die VM-Ressource **sc900-winwm** aus. Diese Ressource ist der VM zugeordnet, die Sie im vorherigen Lab oder der vorherigen Demo verwendet haben.
    1. Auf der Seite „Ressourcenintegrität“ finden Sie eine Liste mit Empfehlungen.  Wählen Sie in der verfügbaren Liste Elemente aus, die den Status **fehlerhaft** aufweisen.
    1. Beachten Sie die ausführliche Beschreibung.  Wählen Sie den Dropdownpfeil neben den Wartungsschritten aus. Beachten Sie, wie Wartungsanweisungen (oder Links zu Anweisungen) zusammen mit der Option zum Ergreifen von Maßnahmen bereitgestellt werden.  Beenden Sie das Fenster, ohne Maßnahmen zu ergreifen.
    1. Kehren Sie zur Übersichtsseite für Microsoft Defender for Cloud zurück, indem Sie **Microsoft Defender for Cloud | Übersicht** oben auf der Seite über „Ressourcenintegrität“ auswählen.

1. Wählen Sie im linken Navigationsbereich **Empfehlungen** aus.  (Beachten Sie, dass dies dem Auswählen der aktiven Empfehlungen oben auf der Übersichtsseite von Microsoft Defender for Cloud entspricht).
    1. Stellen Sie sicher, dass die Registerkarte **Alle Empfehlungen** ausgewählt (unterstrichen) ist.  Beachten Sie die Dashboardansicht, in der aktive Empfehlungen nach Schweregrad, Ressourcenintegrität und mehr angezeigt werden.
    1. Beachten Sie, dass einige Elemente als fehlerhafte Ressourcen angezeigt werden (roter Balken auf der rechten Seite des Zeilenelements).  Wählen Sie in der Liste eine fehlerhafte Ressource aus.  Auf der daraufhin geöffneten Seite werden eine Beschreibung, Schritte zur Wartung und betroffene Ressourcen angezeigt. Schließen Sie diese Seite mit dem **X** oben rechts auf dem Bildschirm.
    1. Schließen Sie die Empfehlungsseite mit dem **X** oben rechts auf dem Bildschirm, um zur Übersichtsseite zurückzukehren.

1. Wählen Sie im linken Hauptnavigationsbereich die Option **Einhaltung gesetzlicher Bestimmungen** aus.  **HINWEIS:** Wenn kein Abonnement angezeigt wird, für das die Konformität berechnet werden kann, liegt das daran, dass es zu einer Verzögerung von bis zu 24 Stunden kommen kann, bis Informationen angezeigt werden. Wechseln Sie zu Aufgabe 2.  Wenn Informationen angezeigt werden, fahren Sie mit den folgenden Schritten fort.
    1. Auf der Seite zur Einhaltung gesetzlicher Bestimmungen finden Sie eine Liste der Konformitätskontrollen, die auf dem Microsoft-Cloudsicherheits-Vergleichstest basieren (stellen Sie sicher, dass die Registerkarte „Microsoft-Cloudsicherheitsvergleichstest“ ausgewählt/unterstrichen ist). Unter jeder Steuerelementdomäne befindet sich eine Teilmenge von Steuerelementen, und für jedes Steuerelement gibt es mindestens eine Bewertung. Jede Bewertung enthält Informationen, darunter Beschreibung, Wartung und betroffene Ressourcen.
    1. Sehen wir uns einen der Steuerelement-Domänenbereiche an. Wählen Sie **NS. Netzwerksicherheit** aus (erweitern Sie diese Option). Eine Liste mit Steuerelementen im Zusammenhang mit Netzwerksicherheit wird angezeigt.
    1. Wählen Sie **NS-10. Microsoft Defender for DNS sollte aktiviert sein** aus. Beachten Sie die Liste der automatisierten Bewertungen (einschließlich automatisierter Bewertungen für AWS) und wie jedes Bewertungszeilenelement Informationen bereitstellt, darunter der Ressourcentyp, fehlerhafte Ressourcen und Compliancestationen. Wählen Sie die aufgeführten Bewertungen aus.  Hier werden Informationen angezeigt, darunter eine Beschreibung, Wiederherstellungsschritte und betroffene Ressourcen.
    1. Wählen Sie in der oberen rechten Ecke des Bildschirms das **X** aus, um die Seite zu schließen.
    1. Wählen Sie im linken Navigationsbereich **Übersicht** aus, um zur Übersichtsseite für Microsoft Defender for Cloud zurückzukehren.
    1. Lassen Sie die Übersichtsseite von Microsoft Defender for Cloud geöffnet. Sie wird in der nächsten Aufgabe verwendet.

### Teil 2 der Demo

Denken Sie daran, dass Microsoft Defender for Cloud in zwei Modi angeboten wird: ohne erweiterte Sicherheitsfeatures (kostenlos) und mit erweiterten Sicherheitsfeatures, die über die Microsoft Defender for Cloud-Pläne verfügbar sind. In dieser Aufgabe erfahren Sie, wie Sie die verschiedenen Microsoft Defender for Cloud-Pläne aktivieren/deaktivieren.

1. Wählen Sie auf der Übersichtsseite von Microsoft Defender für Cloud im linken Navigationsbereich **Umgebungseinstellungen** aus.
1. Wählen Sie das Feld **Alle erweitern** aus, und wählen Sie dann das Abonnement **MOC-Abonnement - lodXXXXXXXXXX** aus, das neben dem gelben Schlüsselsymbol aufgeführt wird.
1. Beachten Sie auf der Seite mit den Defender-Plänen, wie Sie alle Pläne aktivieren oder einzelne Defender-Pläne auswählen können. 
    1. Vergewissern Sie sich, dass der CSPM-Status auf **Ein** festgelegt ist. Wenn dies nicht der Fall ist, legen Sie ihn jetzt fest.  
    1. Aktivieren Sie den Plan für Server.  Wählen Sie für das Zeilenelement „Server“ die Option **Ein** und dann oben auf der Seite **Speichern** aus.
1. Lassen Sie die Azure-Registerkarte in Ihrem Browser für die nächste Azure-Demo geöffnet.

## Überprüfung

In dieser Demo sind Sie Microsoft Defender for Cloud ganz allgemein durchgegangen und haben gezeigt, wie der Sicherheitsstatus einer Organisation mit der Azure-Sicherheitsbewertung verbessert werden kann.
