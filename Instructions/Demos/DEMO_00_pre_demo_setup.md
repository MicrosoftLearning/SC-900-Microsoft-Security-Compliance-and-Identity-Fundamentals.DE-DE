<!---
---
Pre-Demo Setup: Title: 'Einrichtung der Demo'
---
--->

## WWL-Mandanten – Nutzungsbedingungen

Wenn Ihnen im Rahmen einer Präsenzschulung ein Mandant zugewiesen worden ist, steht dieser für Praxislabs innerhalb der Präsenzschulung zur Verfügung.

Mandanten sollten nicht für Zwecke außerhalb von Praxislabs freigegeben oder verwendet werden. Der in diesem Kurs verwendete Mandant ist ein Testmandant; er kann nach Abschluss des Kurses nicht verwendet oder erreicht werden und ist nicht für Erweiterungen geeignet.

Mandanten dürfen nicht in ein kostenpflichtiges Abonnement konvertiert werden. Die im Rahmen dieses Kurses erworbenen Mandanten verbleiben im Eigentum der Microsoft Corporation, und wir behalten uns das Recht vor, jederzeit auf Mandanten zuzugreifen und diese zurückzuziehen.

## Setup vor der Demo des Microsoft 365-Mandanten

### Aktivieren der Überwachung von Microsoft 365-Überwachungsprotokollen und -Dateien

In dieser Einrichtungsaufgabe aktivieren Sie die Überwachungsprotokoll- und Dateiüberwachungsfunktionen in Microsoft 365.

1. Öffnen Sie Microsoft Edge. Geben Sie in der Adressleiste **https://admin.microsoft.com** ein.

1. Melden Sie sich mit den Administratoranmeldeinformationen für den Microsoft 365-Mandanten an, die von Ihrem autorisierten Labhoster (ALH) bereitgestellt werden.

1. Wählen Sie im linken Navigationsbereich von Microsoft 365 Admin Center **Alle anzeigen** aus.

1. Wählen Sie **Sicherheit** unter „Admin Center“ aus.  Die Startseite von Microsoft Defender wird auf einer neuen Browserseite geöffnet.  

1. Wählen Sie im linken Navigationsbereich des Microsoft Purview-Complianceportals **Alle anzeigen** aus.

1. Scrollen Sie im linken Navigationsbereich nach unten, und erweitern Sie **System**.  Wählen Sie in der erweiterten Liste **Überwachung** aus.  Hinweis: Auf die Überwachungsfunktionalität kann auch über das Microsoft Purview-Portal zugegriffen werden.

1. Sobald Sie auf der Seite „Überwachung“ sind, warten Sie 1–2 Minuten.  Wenn Überwachung NICHT aktiviert ist, wird oben auf der Seite ein blauer Balken mit der Meldung „Aufzeichnung von Benutzer- und Administratoraktivitäten starten“ angezeigt.  Wählen Sie **Aufzeichnung von Benutzer- und Administratoraktivitäten starten** aus.  Sobald die Durchführung von Audits aktiviert ist, wird die blaue Leiste ausgeblendet.

1. Wählen Sie im linken Navigationsbereich unter „System“ **Einstellungen** aus

1. Wählen Sie auf der Seite „Einstellungen“ die Option **Cloud-Apps** aus.   Scrollen Sie nach unten, und wählen Sie unter „Information Protection die Option **Dateien** aus.

1. Wenn noch nicht aktiviert, wählen Sie das Kontrollkästchen neben **Dateiüberwachung aktivieren** und dann **Speichern** aus.  

### Konfigurieren der Rolle „Complianceadministrator“

In dieser Einrichtungsaufgabe fügen Sie sich selbst als MOD-Admin zur Rollengruppe „Complianceadministrator“ hinzu.

1. Öffnen Sie eine neue Microsoft Edge-Browserregisterkarte, und geben Sie in der Adressleiste **https://purview.microsoft.com** ein. Um auf das neue Microsoft Purview-Portal zuzugreifen, wählen Sie das Kontrollkästchen neben **Ich stimme den Bedingungen der Datenflussoffenlegung und den Datenschutzbestimmungen zu** und wählen Sie dann **Erste Schritte** aus.  
1. Wählen Sie im linken Navigationsbereich **Einstellungen** aus.
1. Wählen Sie im daraufhin geöffneten Navigationsbereich **Rollen und Bereich** aus, um die Option zu erweitern, und wählen Sie dann **Rollengruppen** aus.
1. Suchen Sie im Suchfeld auf der rechten Seite des Bildschirms nach dem Begriff **Compliance**.  Wählen Sie **Complianceadministrator** aus.
    1. Wählen Sie **Bearbeiten** aus.
    1. Wählen Sie **Benutzer auswählen** aus.
    1. Suchen Sie nach „MOD-Administrator“, wählen Sie das Feld neben **MOD-Administrator** aus, und wählen Sie dann unten auf der Seite die Schaltfläche **Auswählen** aus.
    1. Wählen Sie **Weiter** und dann **Speichern** und schließlich **Fertig** aus.
1. Damit ist das Setup für den Microsoft 365-Mandanten abgeschlossen, und Sie können die Browserregisterkarten schließen.

## Einrichtung des Azure-Abonnements vor der Demo

Für diese Einrichtung verwenden Sie die Azure-Umgebung, die getrennt vom bereitgestellten Microsoft 365-Mandanten ist. Melden Sie sich vom Microsoft 365-Mandanten ab und melden Sie sich mit den Azure-Anmeldeinformationen an.

### Virtueller Azure-Computer

Überprüfen Sie, ob bereits ein virtueller Computer erstellt wurde. Wenn nicht, richten Sie ihn jetzt ein. Sie verwenden den virtuellen Computer als Teil der NSG-Demo.

1. Öffnen Sie Microsoft Edge.  Geben Sie **https://portal.azure.com** in der Adressleiste ein und melden Sie sich mit den Administratoranmeldeinformationen für Microsoft 365 an, die von Ihrem autorisierten Labhoster (ALH) bereitgestellt wurden.  Sie befinden sich nun auf der Homepage der Azure-Dienste.

1. Geben Sie **virtuelle Computer** im blauen Suchfeld oben auf der Seite ein, und wählen Sie **Virtuelle Computer** aus den Ergebnissen aus.

1. Wenn bereits eine VM aufgeführt ist, überspringen Sie die folgenden Schritte, andernfalls müssen Sie eine erstellen.  Wählen Sie **Erstellen** und dann im Dropdownmenü die Option **Virtueller Azure-Computer** aus. Konfigurieren Sie die folgenden Parameter (wenn kein Parameter aufgeführt ist, behalten Sie den Standardwert bei).
    1. Ressourcengruppe: Wählen Sie **Neu erstellen** aus, geben Sie **LabsSC900** ein und klicken Sie dann **OK**.
    1. Name des virtuellen Computers: Geben Sie **SC900-WinVM** ein.
    1. Verfügbarkeitsoptionen: Wählen Sie **Keine Infrastrukturredundanz erforderlich** aus.
    1. Sicherheitstyp: Wählen Sie in der Dropdownliste **Standard** aus.
    1. Abbildung: Wählen Sie in der Dropdownliste **Windows 11 Pro, Version 22H2 – x64 Gen2** (oder ein beliebiges Windows 10- oder Windows 11-Image aus).
    1. Größe: Wählen Sie **Alle Größen anzeigen** und dann **Standard_B1s** dann unten auf der Seite **Auswählen** aus.
    1. Benutzername: Geben Sie **SC900-VM-User** ein
    1. Passwort: Geben Sie ein Passwort ein, und notieren Sie es. Sie benötigen es später!!!
    1. Passwort bestätigen: Geben Sie das Passwort erneut ein.
    1. Öffentliche Eingangsports: **Keine**.
    1. Lizensierung: Wähle Sie folgendes aus: „Ich bestätige, dass ich über eine berechtigte Windows 10/11-Lizenz mit Rechten für mehrinstanzenfähiges Hosting verfüge.“  Es sollte ein Häkchen angezeigt werden.
    1. Klicken Sie auf **Weiter: Datenträger**
    1. Betriebssystemdatenträgertyp: Wählen Sie in der Dropdownliste **SSD Standard** aus.
    1. Klicken Sie auf **Weiter: Netzwerk**
    1. NIC-Netzwerksicherheitsgruppe: Wählen Sie **Keine** aus.  Sie erstellen eine NSG im Rahmen der Demo, also nicht hier!
    1. Öffentliche IP-Adresse und NIC löschen, wenn der virtuelle Computer gelöscht wird: Aktivieren Sie das Kontrollkästchen, damit ein Häkchen angezeigt wird.
    1. Klicken Sie auf **Überprüfen + Erstellen** und nach der Überprüfung auf **Erstellen**.
    1. Nachdem die VM-Bereitstellung abgeschlossen ist, wählen Sie oben auf der Seite **Start** aus.

1. Lassen Sie die Registerkarte des Azure-Browsers geöffnet, um mit dem Setup vor der Demo fortzufahren.

### Netzwerksicherheitsgruppe

Überprüfen Sie, ob bereits eine NSG erstellt wurde. Wenn die NSG noch nicht erstellt wurde, richten Sie sie jetzt ein, ordnen Sie ihr jedoch keine Schnittstelle zu, und erstellen Sie keine Regeln. Diese Schritte werden im Rahmen der NSG-Demo ausgeführt.

1. Geben Sie in der blauen Suchleiste oben auf der Seite **Netzwerksicherheitsgruppen** ein. Wählen Sie in den Ergebnissen **Netzwerksicherheitsgruppen** (nicht „Klassische Netzwerksicherheitsgruppen“) aus.

1. Wählen Sie **Erstellen einer Netzwerksicherheitsgruppe** aus. Geben Sie auf der Registerkarte „Allgemein“ der Seite „Netzwerksicherheitsgruppe erstellen“ die folgenden Einstellungen an:
    1. Abonnement: Behalten Sie den Standardwert bei (dies ist das Azure-Abonnement, das vom autorisierten Lab-Hoster bereitgestellt wird).
    1. Ressourcengruppe:  **LabsSC900**
    1. Name:  **NSG-SC900**
    1. Region: Übernehmen Sie den Standardwert.
    1. Klicken Sie auf **Überprüfen + erstellen** und dann auf **Erstellen**.
    1. Sobald die Bereitstellung abgeschlossen ist (dies geschieht sehr schnell), wählen Sie **Zu Ressource wechseln** aus.

### Microsoft Defender für Cloud

Hier geht es einfach darum, zum ersten Mal auf Microsoft Defender Cloud zuzugreifen. Dies ist wichtig, da es bis zu 24 Stunden dauern kann, bis Defender für Cloud eine erste Sicherheitsbewertung widerspiegelt.  

1. Öffnen Sie die Registerkarte Startseite-Microsoft Azure in Ihrem Browser.

1. Geben Sie **Microsoft Defender for Cloud** in die blaue Suchleiste ein, und wählen Sie dann in der Ergebnisliste **Microsoft Defender for Cloud** aus.

1. Wenn Sie Microsoft Defender for Cloud zum ersten Mal mit Ihrem Abonnement aufrufen, werden Sie möglicherweise zur Seite „Erste Schritte“ geleitet und zur Durchführung eines Upgrades aufgefordert.  Scrollen Sie auf der Seite nach unten, und klicken Sie auf **Überspringen**.  Sie gelangen auf die Übersichtsseite.

1. Alle Abonnements verfügen standardmäßig über eine grundlegende CSPM-Aktivierung, die eine Sicherheitsbewertung bereitstellt, aber es kann bis zu 24 Stunden dauern, bis Defender für Cloud eine anfängliche Sicherheitsbewertung widerspiegelt.

1. Wählen Sie im oberen Bereich der Seite die Option **Start** aus.

1. Lassen Sie die Browserregisterkarte geöffnet, um mit dem Setup vor der Demo fortzufahren.

### Microsoft Sentinel

Vergewissern Sie sich, dass bereits eine Instanz von Microsoft Sentinel erstellt worden ist. Wenn nicht, richten Sie sie jetzt ein, da Sie sie im Rahmen der exemplarischen Demo in Microsoft Sentinel benötigen.

1. Öffnen Sie die Registerkarte Startseite-Microsoft Azure in Ihrem Browser.

1. Geben Sie in das Suchfeld, das sich auf dem blauen Balken oben auf der Seite neben dem Text „Microsoft Azure“ befindet, den Text **Microsoft Sentinel** ein, und wählen Sie dann **Microsoft Sentinel** in den Suchergebnissen aus.

1. Wählen Sie auf der Seite „Microsoft Sentinel“ die Option **Microsoft Sentinel erstellen** aus.

1. Wählen Sie auf der Seite zum Hinzufügen von Microsoft Sentinel zu einem Arbeitsbereich die Option **Neuen Arbeitsbereich erstellen** aus.

1. Geben Sie auf der Registerkarte „Grundlagen“ des Arbeitsbereichs „Log Analytics erstellen“ Folgendes ein:
    1. Abonnement: Übernehmen Sie die Standardeinstellung.
    1. Ressourcengruppe: Wählen Sie **Neu erstellen** aus. Geben Sie dann **SC900-Sentinel RG** ein, und klicken Sie auf **OK**.
    1. Name: **SC900-LogAnalytics-workspace**.
    1. Region: **Ost US** (Sie können eine andere Standardregion basierend auf Ihrem Standort auswählen).
    1. Wählen Sie **Überprüfen und erstellen** aus (es werden keine Tags konfiguriert).
    1. Vergewissern Sie sich, dass Sie die richtigen Informationen eingegeben haben, und klicken Sie dann auf **Erstellen**.
    1. Es kann eine oder zwei Minuten dauern, bis der Arbeitsbereich aufgelistet wird. Wenn er dann immer noch nicht angezeigt wird, klicken Sie auf **Aktualisieren** und dann auf **Hinzufügen**.

1. Nachdem der neue Arbeitsbereich hinzugefügt wurde, wird die Seite „Microsoft Sentinel | News und Leitfäden“ angezeigt, die angibt, dass die kostenlose Microsoft Sentinel-Testversion aktiviert ist.  Klickan Sie auf **OK**.

### Überprüfung

In dieser Konfiguration haben Sie die Funktion für das Überwachungsprotokoll in Ihrem Microsoft 365-Mandanten aktiviert und außerdem überprüft, ob eine VM in Ihrer Azure-Umgebung vorkonfiguriert wurde. Außerdem haben Sie Ihre Defender für Cloud- und Microsoft Sentinel-Umgebung vorbereitet.
