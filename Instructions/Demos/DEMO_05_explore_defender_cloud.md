---
demo:
  title: 'Microsoft Defender für Cloud'
  module: 'Modul 2: Beschreiben der Sicherheitsverwaltungsfunktionen von Azure'
---

# <a name="demo-microsoft-defender-for-cloud"></a>Demo: Microsoft Defender für Cloud

Diese Demo ist den folgenden Learn-Inhalten zugeordnet:

- Lernpfad: Beschreiben der Funktionen von Microsoft-Sicherheitslösungen
- Modul: Beschreiben der Sicherheitsverwaltungsfunktionen von Azure
- Lerneinheit: Beschreiben von Microsoft Defender für Cloud

## <a name="demo-scenario"></a>Demoszenario

In dieser Demo stellen Sie Microsoft Defender for Cloud vor und zeigen, wie der Sicherheitsstatus einer Organisation damit verbessert werden kann.  HINWEIS: Das Azure-Abonnement, das vom Authorized Lab Hoster (AH) verwaltet wird, schränkt möglicherweise einige Zugriffsmöglichkeiten ein führt zu Verzögerungen, die länger als normal sind.

### <a name="demo-task-1"></a>Demoaufgabe 1

In dieser Demoaufgabe durchlaufen Sie auf hoher Ebene einige der Funktionen von Microsoft Defender for Cloud.

1. Öffnen Sie Microsoft Edge. Geben Sie **portal.azure.com** in die Adressleiste ein.
1. Melden Sie sich mit Ihren Administratoranmeldeinformationen an.
    1. Geben Sie im Anmeldefenster den Benutzernamen ein, der von Ihrem Lab-Hostanbieter bereitgestellt wird, und wählen Sie dann **Weiter** aus.
    1. Geben Sie das Administratorkennwort ein, das von Ihrem Lab-Hostinganbieter bereitgestellt werden sollte. Wählen Sie **Anmelden**.
    1. Wählen Sie **Ja** aus, wenn Sie gefragt werden, ob Sie angemeldet bleiben möchten.

1. Geben Sie **Microsoft Defender for Cloud** in die blaue Suchleiste ein, und wählen Sie dann in der Ergebnisliste **Microsoft Defender for Cloud** aus.

1. Wenn Sie Microsoft Defender for Cloud zum ersten Mal mit Ihrem Abonnement aufrufen, werden Sie möglicherweise zur Seite „Erste Schritte“ geleitet und zur Durchführung eines Upgrades aufgefordert.  Scrollen Sie auf der Seite nach unten, und klicken Sie auf **Überspringen**.  Sie gelangen auf die Übersichtsseite.

1. Beachten Sie in der Übersicht von Microsoft Defender für Cloud die auf der Seite verfügbaren Informationen.  Oben auf der Seite finden Sie Informationen wie die Anzahl der Azure-Abonnements, die Anzahl der bewerteten Ressourcen, die Anzahl der aktiven Empfehlungen und alle Sicherheitswarnungen.  In der Mitte der Seite befinden sich Karten für den Sicherheitsstatus, die Einhaltung gesetzlicher Bestimmungen, Insights und mehr.  Hinweis: Die Microsoft Defender for Cloud-Standardrichtlinieninitiative, die normalerweise vom Administrator zugewiesen werden müsste, wurde bereits im Rahmen der Einrichtung des Azure-Abonnements zugewiesen. Die Sicherheitsbewertung wird jedoch als 0 % angezeigt, da Azure eine Verzögerung von bis zu 24 Stunden aufweisen kann, bis eine anfängliche Bewertung angezeigt wird.

1. Wählen Sie oben auf der Seite die Option **Bewertete Ressourcen** aus.  (Beachten Sie, dass Sie genauso auf der Startseite von Microsoft Defender für Cloud im linken Navigationsbereich die Option „Inventar“ auswählen können.)
    1. Dadurch gelangen Sie zur Seite **Bestand**, auf der die aktuellen Ressourcen aufgeführt werden. Wählen Sie die VM-Ressource **sc900-winwm** aus. Diese Ressource ist der VM zugeordnet, die Sie im vorherigen Lab verwendet haben.
    1. Auf der Seite „Ressourcenintegrität“ finden Sie eine Liste mit Empfehlungen.  Wählen Sie in der verfügbaren Liste Elemente aus, die den Status **fehlerhaft** aufweisen.
    1. Beachten Sie die ausführliche Beschreibung.  Wählen Sie den Dropdownpfeil neben den Wartungsschritten aus. Beachten Sie, wie Wartungsanweisungen (oder Links zu Anweisungen) zusammen mit der Option zum Ergreifen von Maßnahmen bereitgestellt werden.  Beenden Sie das Fenster, ohne Maßnahmen zu ergreifen.
    1. Kehren Sie zur Übersichtsseite für Microsoft Defender for Cloud zurück, indem Sie **Microsoft Defender for Cloud | Übersicht** oben auf der Seite über „Ressourcenintegrität“ auswählen.

1. Wählen Sie im linken Navigationsbereich **Empfehlungen** aus.  (Beachten Sie, dass dies dem Auswählen der aktiven Empfehlungen oben auf der Übersichtsseite von Microsoft Defender for Cloud entspricht).
    1. Stellen Sie sicher, dass die Registerkarte **Alle Empfehlungen** ausgewählt (unterstrichen) ist.  Beachten Sie die Dashboardansicht, in der aktive Empfehlungen nach Schweregrad, Ressourcenintegrität und mehr angezeigt werden.
    1. Beachten Sie, dass einige Elemente als fehlerhafte Ressourcen angezeigt werden (roter Balken auf der rechten Seite des Zeilenelements).  Wählen Sie in der Liste eine fehlerhafte Ressource aus.  Auf der daraufhin geöffneten Seite werden eine Beschreibung, Schritte zur Wartung und betroffene Ressourcen angezeigt. Schließen Sie diese Seite mit dem **X** oben rechts auf dem Bildschirm.
    1. Schließen Sie die Empfehlungsseite mit dem **X** oben rechts auf dem Bildschirm, um zur Übersichtsseite zurückzukehren.

1. Wählen Sie im linken Hauptnavigationsbereich die Option **Einhaltung gesetzlicher Bestimmungen** aus. Auf der Seite zur Einhaltung gesetzlicher Bestimmungen finden Sie eine Liste der Konformitätskontrollen, die auf dem Microsoft-Cloudsicherheits-Vergleichstest basieren (stellen Sie sicher, dass die Registerkarte „Microsoft-Cloudsicherheitsvergleichstest“ ausgewählt/unterstrichen ist). Unter jeder Steuerelementdomäne befindet sich eine Teilmenge von Steuerelementen, und für jedes Steuerelement gibt es mindestens eine Bewertung. Jede Bewertung enthält Informationen, darunter Beschreibung, Wartung und betroffene Ressourcen.
    1. Sehen wir uns einen der Steuerelement-Domänenbereiche an. Wählen Sie **NS. Netzwerksicherheit** aus (erweitern Sie diese Option). Eine Liste mit Steuerelementen im Zusammenhang mit Netzwerksicherheit wird angezeigt.
    1. Wählen Sie **NS-10. Microsoft Defender for DNS sollte aktiviert sein** aus. Beachten Sie die Liste der automatisierten Bewertungen (einschließlich automatisierter Bewertungen für AWS) und wie jedes Bewertungszeilenelement Informationen bereitstellt, darunter der Ressourcentyp, fehlerhafte Ressourcen und Compliancestationen. Wählen Sie die aufgeführten Bewertungen aus.  Hier werden Informationen angezeigt, darunter eine Beschreibung, Wiederherstellungsschritte und betroffene Ressourcen.
    1. Wählen Sie in der oberen rechten Ecke des Bildschirms das **X** aus, um die Seite zu schließen.
    1. Wählen Sie im linken Navigationsbereich **Übersicht** aus, um zur Übersichtsseite für Microsoft Defender for Cloud zurückzukehren.
    1. Lassen Sie die Übersichtsseite von Microsoft Defender for Cloud geöffnet. Sie wird in der nächsten Aufgabe verwendet.

### <a name="demo-task-2"></a>Demoaufgabe 2

Denken Sie daran, dass Microsoft Defender for Cloud in zwei Modi angeboten wird: ohne erweiterte Sicherheitsfeatures (kostenlos) und mit erweiterten Sicherheitsfeatures, die über die Microsoft Defender for Cloud-Pläne verfügbar sind. In dieser Aufgabe erfahren Sie, wie Sie die verschiedenen Microsoft Defender for Cloud-Pläne aktivieren/deaktivieren.

1. Wählen Sie auf der Übersichtsseite von Microsoft Defender für Cloud im linken Navigationsbereich **Umgebungseinstellungen** aus.
1. Wählen Sie das Feld **Alle erweitern** aus, und wählen Sie dann das Abonnement **MOC-Abonnement - lodXXXXXXXXXX** aus, das neben dem gelben Schlüsselsymbol aufgeführt wird.
1. Beachten Sie auf der Seite mit den Defender-Plänen, wie Sie alle Pläne aktivieren oder einzelne Defender-Pläne auswählen können. 
    1. Vergewissern Sie sich, dass der CSPM-Status auf **Ein** festgelegt ist. Wenn dies nicht der Fall ist, legen Sie ihn jetzt fest.  
    1. Aktivieren Sie den Plan für Server.  Wählen Sie für das Zeilenelement „Server“ die Option **Ein** und dann oben auf der Seite **Speichern** aus.
1. Schließen Sie alle geöffneten Browserregisterkarten.

## <a name="review"></a>Überprüfung

In dieser Demo sind Sie Microsoft Defender für Cloud durchgegangen und haben gezeigt, wie der Sicherheitsstatus einer Organisation mit der Azure-Sicherheitsbewertung verbessert werden kann.
