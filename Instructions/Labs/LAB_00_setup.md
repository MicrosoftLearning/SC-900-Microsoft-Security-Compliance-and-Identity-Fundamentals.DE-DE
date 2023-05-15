---
lab:
  title: 'Setup'
  module: 'Setup'
---


# <a name="lab-setup"></a>Lab: Setup

## <a name="lab-scenario"></a>Labszenario

Bei diesem Setuplab geht es um die Aktivierung des Microsoft-Überwachungsprotokolls.

**Geschätzte Dauer**: 5–10 Minuten

### <a name="setup---enable-microsoft-365-audit-log"></a>Einrichtung – Aktivieren des Microsoft 365-Überwachungsprotokolls

In dieser Einrichtungsaufgabe aktivieren Sie die Überwachungsprotokollfunktion in Microsoft 365.  Obwohl das Überwachungsprotokoll laut Dokumentation standardmäßig aktiviert ist, trifft dies für die meisten Lab-Mandanten nicht zu, und es kann mehrere Stunden dauern, bis die Änderung wirksam wird.  Es empfiehlt sich, diese Funktion zu aktivieren, da Microsoft 365 Überwachungsprotokolle für Benutzererkenntnisse und -aktivitäten in Richtlinien und Analyseerkenntnisse verwendet.

1. Öffnen Sie Microsoft Edge. Geben Sie **admin.microsoft.com** in die Adressleiste ein.

1. Melden Sie sich mit Ihren Administratoranmeldeinformationen an.
    1. Geben Sie **admin@WWLxZZZZZZ.onmicrosoft.com** (ZZZZZZ ist hierbei die eindeutige Mandanten-ID, die von Ihrem Lab-Hostinganbieter bereitgestellt wurde) in das Anmeldefenster ein, und wählen Sie dann **Weiter** aus.
    1. Geben Sie das Administratorkennwort ein, das von Ihrem Lab-Hostinganbieter bereitgestellt werden sollte. Wählen Sie **Anmelden**.
    1. Wählen Sie **Ja** aus, wenn Sie gefragt werden, ob Sie angemeldet bleiben möchten. Dadurch gelangen Sie zur Seite „Microsoft 365 Admin Center“.

1. Wählen Sie im linken Navigationsbereich von Microsoft 365 Admin Center **Alle anzeigen** aus.

1. Wählen Sie unter „Admin Center“ die Option **Compliance** aus.  Die Startseite des Microsoft Purview-Complianceportals wird auf einer neuen Browserseite geöffnet.  

1. Wählen Sie im linken Navigationsbereich unter „Lösungen“ die Option **Überwachen** aus.  Hinweis: Auf die Überwachungsfunktion kann auch über die Homepage von Microsoft 365 Defender (zuvor als Microsoft 365 Security Center bezeichnet) zugegriffen werden.

1. Stellen Sie sicher, dass die Registerkarte **Neue Suche** ausgewählt (unterstrichen) ist.

1. Warten Sie zwei bis drei Minuten, nachdem Sie zur Seite „Überwachen“ gelangt sind.  Wenn die Überwachung NICHT aktiviert ist, wird oben auf der Seite ein blauer Balken mit der Meldung „Aufzeichnung von Benutzer- und Administratoraktivitäten starten“ angezeigt.  Wählen Sie **Aufzeichnung von Benutzer- und Administratoraktivitäten starten** aus.  Wenn Sie aufgefordert werden, zu bestätigen, dass die Organisationseinstellung aktualisiert werden müssen, wählen Sie **Ja** aus. Sobald die Überwachung aktiviert ist, wird der blaue Balken nicht mehr angezeigt.  Wird der blaue Balken nicht angezeigt, ist Überwachung bereits aktiviert, und keine weitere Aktion ist erforderlich.  Sie können die Aktivierung der Überwachung auch über PowerShell überprüfen. Dies wird im Rahmen dieses Kurses jedoch nicht behandelt.

1. Kehren Sie zur Homepage des Microsoft Purview-Complianceportals zurück, indem Sie im linken Navigationsbereich **Start** auswählen und sich bei Microsoft 365 abmelden. Melden Sie sich ab, indem Sie das Symbol in der oberen rechten Ecke des Microsoft 365-Fensters auswählen, das als Kreis mit den Buchstaben MA (neben dem Fragezeichensymbol) angezeigt wird, und dann **Abmelden** auswählen. Schließen Sie dann den Browser.

### <a name="review"></a>Überprüfung

In diesem Setup haben Sie die Überwachungsprotokollfunktion in Microsoft 365 aktiviert.
