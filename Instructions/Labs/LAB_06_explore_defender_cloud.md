---
lab:
  title: Erkunden von Microsoft Defender für Cloud
  module: Describe the security management capabilities of Azure
---

# Lab: Erkunden von Microsoft Defender für Cloud

Dieses Lab ist den folgenden Learn-Inhalten zugeordnet:

- Lernpfad: Beschreiben der Funktionen von Microsoft-Sicherheitslösungen
- Modul: Beschreiben der Sicherheitsverwaltungsfunktionen von Azure
- Lerneinheit: Beschreiben von Cloud Security Posture Management

## Labszenario

In diesem Lab erkunden Sie Microsoft Defender for Cloud.  HINWEIS: Das Azure-Abonnement, das vom Authorized Lab Hoster (ALH) bereitgestellt wird, schränkt möglicherweise den Zugriff ein und kann zu Verzögerungen führen, die länger als normal sind.

**Geschätzte Dauer**: 30 Minuten

### Aufgabe 1

In dieser Aufgabe durchlaufen Sie auf hoher Ebene einige der Funktionen von Microsoft Defender for Cloud.

1. Sie sollten sich auf der Startseite für Azure-Dienste befinden.  Wenn Sie den Browser zuvor geschlossen haben, öffnen Sie Microsoft Edge. Geben Sie **portal.azure.com** in die Adressleiste ein, und melden Sie sich mit Ihren Administratoranmeldeinformationen an.

1. Geben Sie **Microsoft Defender for Cloud** in die blaue Suchleiste ein, und wählen Sie dann in der Ergebnisliste **Microsoft Defender for Cloud** aus.

1. Wenn Sie Microsoft Defender for Cloud zum ersten Mal mit Ihrem Abonnement aufrufen, werden Sie möglicherweise zur Seite „Erste Schritte“ geleitet und zur Durchführung eines Upgrades aufgefordert.  Scrollen Sie zum unteren Rand der Seite, und wählen **Sie Später erinnern** (oder **Überspringen**) aus.  Sie gelangen auf die Übersichtsseite.

1. Beachten Sie auf der Seite „Übersicht“ von Microsoft Defender for Cloud die auf der Seite verfügbaren Informationen (wenn Sie 0 bewertete Ressourcen und aktive Empfehlungen sehen, aktualisieren Sie die Browserseite, dies kann einige Minuten dauern).  Oben auf der Seite finden Sie Informationen wie die Anzahl der Azure-Abonnements, die Anzahl der bewerteten Ressourcen, die Anzahl der aktiven Empfehlungen und alle Sicherheitswarnungen.  In der Mitte der Seite befinden sich Karten für den Sicherheitsstatus, die Einhaltung gesetzlicher Bestimmungen, Insights und mehr.  Hinweis: Die Microsoft Defender for Cloud-Standardrichtlinieninitiative, die normalerweise vom Administrator zugewiesen werden müsste, wurde bereits im Rahmen der Einrichtung des Azure-Abonnements zugewiesen. Die Sicherheitsbewertung wird jedoch als 0 % angezeigt, da Azure eine Verzögerung von bis zu 24 Stunden aufweisen kann, bis eine anfängliche Bewertung angezeigt wird.

1. Wählen Sie oben auf der Seite die Option **Bewertete Ressourcen** aus. 
    1. Dadurch gelangen Sie zur Seite **Bestand**, auf der die aktuellen Ressourcen aufgeführt werden. Wählen Sie die VM-Ressource **sc900-winwm** aus. Diese Ressource ist der VM zugeordnet, die Sie im vorherigen Lab verwendet haben.
    1. Auf der Seite „Ressourcenintegrität“ finden Sie eine Liste mit Empfehlungen.  Wählen Sie in der verfügbaren Liste Elemente aus, die den Status **fehlerhaft** aufweisen.
    1. Beachten Sie die ausführliche Beschreibung.  Wählen Sie den Dropdownpfeil neben den Wartungsschritten aus. Beachten Sie, wie Wartungsanweisungen (oder Links zu Anweisungen) zusammen mit der Option zum Ergreifen von Maßnahmen bereitgestellt werden.  Beenden Sie das Fenster, ohne Maßnahmen zu ergreifen.
    1. Kehren Sie zur Übersichtsseite für Microsoft Defender for Cloud zurück, indem Sie **Microsoft Defender for Cloud | Übersicht** oben auf der Seite über „Ressourcenintegrität“ auswählen.

1. Wählen Sie im linken Navigationsbereich **Empfehlungen** aus.  
    1. Stellen Sie sicher, dass die Registerkarte **Alle Empfehlungen** ausgewählt (unterstrichen) ist.  Beachten Sie die Dashboardansicht, in der aktive Empfehlungen nach Schweregrad, Ressourcenintegrität und mehr angezeigt werden.
    1. Wählen Sie ein Element aus der Liste aus.  Auf der Seite, die geöffnet wird, sehen Sie eine Beschreibung und zusätzliche Informationen, die möglicherweise Korrekturschritte, betroffene Ressourcen und vieles mehr enthalten. Schließen Sie diese Seite mit dem **X** oben rechts auf dem Bildschirm.

1. Wählen Sie im linken Hauptnavigationsbereich die Option **Einhaltung gesetzlicher Bestimmungen** aus.  **HINWEIS:** Wenn kein Abonnement angezeigt wird, für das die Konformität berechnet werden kann, liegt das daran, dass es zu einer Verzögerung von bis zu 24 Stunden kommen kann, bis Informationen angezeigt werden. Wechseln Sie zu Aufgabe 2.  Wenn Informationen angezeigt werden, fahren Sie mit den folgenden Schritten fort.
    1. Auf der Seite zur Einhaltung gesetzlicher Bestimmungen finden Sie eine Liste der Konformitätskontrollen, die auf dem Microsoft-Cloudsicherheits-Vergleichstest basieren (stellen Sie sicher, dass die Registerkarte „Microsoft-Cloudsicherheitsvergleichstest“ ausgewählt/unterstrichen ist). Unter jeder Steuerelementdomäne befindet sich eine Teilmenge von Steuerelementen, und für jedes Steuerelement gibt es mindestens eine Bewertung. Jede Bewertung enthält Informationen, darunter Beschreibung, Wartung und betroffene Ressourcen.
    1. Sehen wir uns einen der Steuerelement-Domänenbereiche an. Wählen Sie **NS. Netzwerksicherheit** aus (erweitern Sie diese Option). Eine Liste mit Steuerelementen im Zusammenhang mit Netzwerksicherheit wird angezeigt.
    1. Wählen Sie **NS-10. Sicherheit des Domain Name Systems (DNS) sicherstellen** aus. Beachten Sie die Liste der automatisierten Bewertungen (einschließlich automatisierter Bewertungen für AWS) und wie jedes Bewertungszeilenelement Informationen bereitstellt, darunter der Ressourcentyp, fehlerhafte Ressourcen und Compliancestationen. Wählen Sie die aufgeführten Bewertungen aus.  Hier werden Informationen angezeigt, darunter eine Beschreibung, Wiederherstellungsschritte und betroffene Ressourcen.
    1. Wählen Sie in der oberen rechten Ecke des Bildschirms das **X** aus, um die Seite zu schließen.
    1. Wählen Sie im linken Navigationsbereich **Übersicht** aus, um zur Übersichtsseite für Microsoft Defender for Cloud zurückzukehren.
    1. Lassen Sie die Übersichtsseite von Microsoft Defender for Cloud geöffnet. Sie wird in der nächsten Aufgabe verwendet.

### Aufgabe 2

Denken Sie daran, dass Microsoft Defender for Cloud in zwei Modi angeboten wird: ohne erweiterte Sicherheitsfeatures (kostenlos) und mit erweiterten Sicherheitsfeatures, die über die Microsoft Defender for Cloud-Pläne verfügbar sind. In dieser Aufgabe erfahren Sie, wie Sie die verschiedenen Microsoft Defender for Cloud-Pläne aktivieren/deaktivieren.

1. Wählen Sie auf der Übersichtsseite von Microsoft Defender für Cloud im linken Navigationsbereich **Umgebungseinstellungen** aus.
1. Wählen Sie das Feld **Alle erweitern** aus, und wählen Sie dann das Abonnement **MOC-Abonnement - lodXXXXXXXXXX** aus, das neben dem gelben Schlüsselsymbol aufgeführt wird.
1. Beachten Sie auf der Seite mit den Defender-Plänen, wie Sie alle Pläne aktivieren oder einzelne Defender-Pläne auswählen können. 
    1. Vergewissern Sie sich, dass der CSPM-Status auf **Ein** festgelegt ist. Wenn dies nicht der Fall ist, legen Sie ihn jetzt fest.  
    1. Aktivieren Sie den Plan für Server.  Wählen Sie für das Zeilenelement „Server“ die Option **Ein** und dann oben auf der Seite **Speichern** aus.
1. Wählen Sie in der oberen linken Ecke des Fensters direkt unterhalb der blauen Leiste, wo „Microsoft Azure“ angezeigt wird, die Option **Startseite** aus, um zur Startseite der Azure-Dienste zurückzukehren.
1. Lassen Sie die Azure-Registerkarte in Ihrem Browser geöffnet.

### Überprüfung

In diesem Lab erkunden Sie Microsoft Defender for Cloud.
