---
lab:
  title: Setup der Übungsumgebung
  module: Setup your Microsoft 365 lab tenant (not associated with a Learn module)
---

# Lab: Einrichtung der Microsoft 365-Mandantschaft

## WWL-Mandanten – Nutzungsbedingungen
Wenn Ihnen im Rahmen einer Präsenzschulung ein Mandant zugewiesen worden ist, steht dieser für Praxislabs innerhalb der Präsenzschulung zur Verfügung.

Mandanten sollten nicht für Zwecke außerhalb von Praxislabs freigegeben oder verwendet werden. Der in diesem Kurs verwendete Mandant ist ein Testmandant; er kann nach Abschluss des Kurses nicht verwendet oder erreicht werden und ist nicht für Erweiterungen geeignet.

Mandanten dürfen nicht in ein kostenpflichtiges Abonnement konvertiert werden. Die im Rahmen dieses Kurses erworbenen Mandanten verbleiben im Eigentum der Microsoft Corporation, und wir behalten uns das Recht vor, jederzeit auf Mandanten zuzugreifen und diese zurückzuziehen.

## Labszenario

Dieses Setup-Lab besteht aus der Aktivierung der Microsoft-Überwachungsprotokoll- und Dateiüberwachungsfunktionen im Microsoft 365-Mandanten.

**Geschätzte Dauer**: 5–10 Minuten

### Einrichtung - Aktivieren Sie die Überwachung von Microsoft 365-Auditprotokollen und Dateien

In dieser Einrichtungsaufgabe aktivieren Sie die Audit-Protokoll- und Dateiüberwachungsfunktionen in Microsoft 365.  

1. Öffnen Sie Microsoft Edge. Geben Sie in der Adressleiste **`https://admin.microsoft.com`** ein.

1. Melden Sie sich mit den Administratoranmeldeinformationen für den Microsoft 365-Mandanten an, die von Ihrem autorisierten Labhoster (ALH) bereitgestellt werden.

1. Wählen Sie im linken Navigationsbereich von Microsoft 365 Admin Center **Alle anzeigen** aus.

1. Wählen Sie **Sicherheit** unter „Admin Center“ aus.  Die Startseite von Microsoft Defender wird auf einer neuen Browserseite geöffnet.

1. Scrollen Sie im linken Navigationsbereich nach unten, und erweitern Sie **System**.  Wählen Sie in der erweiterten Liste **Überwachung** aus.  Hinweis: Auf die Überwachungsfunktionalität kann auch über das Microsoft Purview-Portal zugegriffen werden.

1. Sobald Sie auf der Seite „Überwachung“ sind, warten Sie 1–2 Minuten.  Wenn Überwachung NICHT aktiviert ist, wird oben auf der Seite ein blauer Balken mit der Meldung „Aufzeichnung von Benutzer- und Administratoraktivitäten starten“ angezeigt.  Wählen Sie **Aufzeichnung von Benutzer- und Administratoraktivitäten starten** aus.  Sobald die Durchführung von Audits aktiviert ist, wird die blaue Leiste ausgeblendet.  Wird der blaue Balken nicht angezeigt, ist Überwachung bereits aktiviert, und keine weitere Aktion ist erforderlich.

1. Wählen Sie im linken Navigationsbereich unter „System“ **Einstellungen** aus

1. Wählen Sie auf der Seite „Einstellungen“ die Option **Cloud-Apps** aus.   Scrollen Sie nach unten und wählen Sie dann unter **Information Protection** die Option **Files** aus.

1. Wenn noch nicht aktiviert, wählen Sie das Kontrollkästchen neben **Dateiüberwachung aktivieren** und dann **Speichern** aus.  

1. Dies schließt die Lab-Einrichtung auf dem Microsoft 365-Mandanten ab.

### Überprüfung

Bei dieser Einrichtung haben Sie die Audit-Protokoll- und Dateiüberwachungsfunktionen in Microsoft 365 aktiviert.
