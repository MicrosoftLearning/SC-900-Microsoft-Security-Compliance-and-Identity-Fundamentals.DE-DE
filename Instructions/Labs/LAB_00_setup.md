<!---
---
Lab: Title: 'Setup'
---
--->

# Lab: Einrichtung

## WWL-Mandanten – Nutzungsbedingungen
Wenn Ihnen im Rahmen einer Präsenzschulung ein Mandant zugewiesen worden ist, steht dieser für Praxislabs innerhalb der Präsenzschulung zur Verfügung.

Mandanten sollten nicht für Zwecke außerhalb von Praxislabs freigegeben oder verwendet werden. Der in diesem Kurs verwendete Mandant ist ein Testmandant; er kann nach Abschluss des Kurses nicht verwendet oder erreicht werden und ist nicht für Erweiterungen geeignet.

Mandanten dürfen nicht in ein kostenpflichtiges Abonnement konvertiert werden. Die im Rahmen dieses Kurses erworbenen Mandanten verbleiben im Eigentum der Microsoft Corporation, und wir behalten uns das Recht vor, jederzeit auf Mandanten zuzugreifen und diese zurückzuziehen.

## Labszenario

Bei diesem Setuplab geht es um die Aktivierung des Microsoft-Überwachungsprotokolls.

**Geschätzte Dauer**: 5-10 Minuten

### Einrichtung – Aktivieren des Microsoft 365-Überwachungsprotokolls

In dieser Einrichtungsaufgabe aktivieren Sie die Überwachungsprotokollfunktion in Microsoft 365.  Obwohl das Überwachungsprotokoll laut Dokumentation standardmäßig aktiviert ist, trifft dies für die meisten Lab-Mandanten nicht zu, und es kann mehrere Stunden dauern, bis die Änderung wirksam wird.  Es empfiehlt sich, diese Funktion zu aktivieren, da Microsoft 365 Überwachungsprotokolle für Benutzererkenntnisse und -aktivitäten in Richtlinien und Analyseerkenntnissen verwendet.

1. Öffnen Sie Microsoft Edge. Geben Sie **admin.microsoft.com** in die Adressleiste ein.

1. Melden Sie sich mit Ihren Administratoranmeldeinformationen an.
    1. Geben Sie **admin@WWLxZZZZZZ.onmicrosoft.com** (ZZZZZZ ist hierbei die eindeutige Mandanten-ID, die von Ihrem Lab-Hostinganbieter bereitgestellt wurde) in das Anmeldefenster ein, und wählen Sie dann **Weiter** aus.
    1. Geben Sie das Administratorkennwort ein, das von Ihrem Lab-Hostinganbieter bereitgestellt werden sollte. Wählen Sie **Anmelden**.
    1. Wählen Sie **Ja** aus, wenn Sie gefragt werden, ob Sie angemeldet bleiben möchten. Dadurch gelangen Sie zur Seite „Microsoft 365 Admin Center“.

1. Wählen Sie im linken Navigationsbereich von Microsoft 365 Admin Center **Alle anzeigen** aus.

1. Wählen Sie unter „Admin Center“ die Option **Compliance** aus.  Die Startseite des Microsoft Purview-Complianceportals wird auf einer neuen Browserseite geöffnet.  

1. Wählen Sie im linken Navigationsbereich **Audit** aus.  Hinweis: Auf die Überwachungsfunktionalität kann auch über die Microsoft 365 Defender-Startseite zugegriffen werden (zuvor als Microsoft 365 Security Center bezeichnet).

1. Stellen Sie sicher, dass die Registerkarte **Neue Suche** ausgewählt (unterstrichen) ist.

1. Sobald Sie auf der Seite "Überwachung" landen, warten Sie 2-3 Minuten.  Wenn Überwachung NICHT aktiviert ist, wird oben auf der Seite ein blauer Balken mit der Meldung „Aufzeichnung von Benutzer- und Administratoraktivitäten starten“ angezeigt.  Wählen Sie **Aufzeichnung von Benutzer- und Administratoraktivitäten starten** aus.  Wenn Sie aufgefordert werden, zu bestätigen, dass die Organisationseinstellung aktualisiert werden müssen, wählen Sie **Ja** aus. Sobald die Überwachung aktiviert ist, wird die blaue Leiste ausgeblendet.  Wird der blaue Balken nicht angezeigt, ist Überwachung bereits aktiviert, und keine weitere Aktion ist erforderlich.  Eine weitere Möglichkeit, um zu überprüfen, ob die Überwachung aktiviert ist, liegt jedoch außerhalb des Umfangs dieses Kurses.

1. Kehren Sie zur Homepage des Microsoft Purview-Complianceportals zurück, indem Sie im linken Navigationsbereich **Start** auswählen und sich bei Microsoft 365 abmelden. Melden Sie sich ab, indem Sie das Symbol in der oberen rechten Ecke des Microsoft 365-Fensters auswählen, das als Kreis mit den Buchstaben MA (neben dem Fragezeichensymbol) angezeigt wird, und dann **Abmelden** auswählen. Schließen Sie dann den Browser.

### Überprüfung

In diesem Setup haben Sie die Überwachungsprotokollfunktion in Microsoft 365 aktiviert.
