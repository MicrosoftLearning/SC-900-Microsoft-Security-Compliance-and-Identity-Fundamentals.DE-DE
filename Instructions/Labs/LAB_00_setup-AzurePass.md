<a name="---"></a><!---
---
Lab: Title: 'Setup'
---
--->

# <a name="lab-setup"></a>Lab: Setup

## <a name="lab-scenario"></a>Labszenario

Dieses Setuplab besteht aus zwei separaten Aufgaben.  Die erste Aufgabe wird angewendet und nur empfohlen, wenn in Ihrer Laborumgebung die Verwendung eines Azure Pass-Angebots integriert ist. Die zweite Aufgabe konzentriert sich auf die Aktivierung des Microsoft-Überwachungsprotokolls.

**Geschätzte Dauer**: 5–10 Minuten



### <a name="setup-part-1---redeem-azure-pass"></a>Teil 1 der Einrichtung – Einlösen des Azure Pass

Diese Aufgabe wird angewendet und nur empfohlen, wenn die von Ihnen verwendete Laborumgebung ein Azure Pass-Angebot enthält. In dieser Aufgabe lösen Sie Ihr Azure Pass-Angebot unter Verwendung der gleichen Anmeldeinformationen ein, die Sie auch für den Microsoft 365-Mandanten verwenden.  So können Sie nahtloser zwischen Microsoft 365 und Azure wechseln.

1. Falls Browserfenster geöffnet sind, wird empfohlen, alle Browser zu schließen.

1. Klicken Sie mit der rechten Maustaste auf das Microsoft Edge-Symbol, und wählen Sie **Neues InPrivate-Fenster** aus, um eine neue InPrivate-Browsersitzung zu öffnen.

1. Geben Sie **www.microsoftazurepass.com** in die Adressleiste ein.  

1. Wählen Sie die Schaltfläche **Start** aus, um zu beginnen.

    1. Geben Sie die E-Mail-Adresse **admin@WWLxZZZZZZ.onmicrosoft.com** (ZZZZZZ ist hierbei die eindeutige Mandanten-ID, die von Ihrem Labhostinganbieter bereitgestellt wurde) in das Fenster „Anmelden“ ein, und wählen Sie dann **Weiter** aus.
    1. Geben Sie das Administratorkennwort ein, das Sie vom Labhostinganbieter erhalten haben sollten. Wählen Sie **Anmelden**.  Wählen Sie **Ja** aus, wenn Sie gefragt werden, ob Sie angemeldet bleiben möchten.
    1. Wählen Sie **Microsoft-Konto bestätigen** aus, falls die richtige E-Mail-Adresse aufgelistet ist.
    1. Geben Sie im Feld „Angebotscode“ Ihren Angebotscode ein, und klicken Sie auf **Angebotscode beanspruchen**.  
    1. Übernehmen Sie auf der Seite „Ihr Profil“ alle Standardinformationen, wählen Sie **Ich stimme dem Abonnentenvertrag, den Angaben zum Angebot und den Datenschutzbestimmungen zu** und dann **Registrieren** aus.
    1. Wenn ein Umfragefenster geöffnet wird, können Sie es durch Klicken auf das **X** schließen oder die Fragen beantworten und dann **Senden** auswählen.

1. Die Aktivierung Ihres Kontos kann ein paar Minuten dauern.  Nach der Aktivierung werden Sie zur Homepage des Azure-Portals umgeleitet. Das Fenster „Willkommen bei Microsoft Azure“ wird geöffnet. Wählen Sie **Vielleicht später** aus. Möglicherweise wird das Popupfenster „Cloudworkloads mit personalisierten Empfehlungen optimieren“ angezeigt. Wählen Sie in diesem Fall in der oberen rechten Ecke des Fensters **X** aus.

1. Lassen Sie die Browserregisterkarte für die Homepage des Azure-Portals geöffnet. In der nächsten Demo navigieren Sie zu ihr zurück.

### <a name="setup-part-2---enable-microsoft-365-audit-log"></a>Teil 2 der Einrichtung – Aktivieren des Microsoft 365-Überwachungsprotokolls

In dieser Einrichtungsaufgabe aktivieren Sie die Überwachungsprotokollfunktion in Microsoft 365.  Obwohl das Überwachungsprotokoll laut Dokumentation standardmäßig aktiviert ist, trifft dies für die meisten Labmandanten nicht zu, und es kann mehrere Stunden dauern, bis die Änderung wirksam wird.  Es empfiehlt sich, diese Funktion zu aktivieren, da Microsoft 365 Überwachungsprotokolle für Benutzererkenntnisse und -aktivitäten in Richtlinien und Analyseerkenntnisse verwendet.

1. Öffnen Sie Microsoft Edge. Geben Sie **admin.microsoft.com** in die Adressleiste ein.

1. Melden Sie sich mit Ihren Administratoranmeldeinformationen an.
    1. Geben Sie **admin@WWLxZZZZZZ.onmicrosoft.com** (ZZZZZZ ist hierbei die eindeutige Mandanten-ID, die von Ihrem Labhostinganbieter bereitgestellt wurde) in das Fenster „Anmelden“ ein, und wählen Sie dann **Weiter** aus.
    1. Geben Sie das Administratorkennwort ein, das Sie vom Labhostinganbieter erhalten haben sollten. Wählen Sie **Anmelden**.
    1. Wählen Sie **Ja** aus, wenn Sie gefragt werden, ob Sie angemeldet bleiben möchten. Dadurch gelangen Sie zur Seite „Microsoft 365 Admin Center“.

1. Wählen Sie im linken Navigationsbereich von Microsoft 365 Admin Center **Alle anzeigen** aus.

1. Wählen Sie unter „Admin Center“ die Option **Compliance** aus.  Die Startseite des Microsoft 365 Compliance Center wird auf einer neuen Browserseite geöffnet.  

1. Wählen Sie im linken Navigationsbereich unter „Lösungen“ die Option **Überwachen** aus.  Hinweis: Auf die Überwachungsfunktion kann auch über die Homepage von Microsoft 365 Defender (zuvor als Microsoft 365 Security Center bezeichnet) zugegriffen werden.

1. Stellen Sie sicher, dass die Registerkarte **Suche** ausgewählt (unterstrichen) ist.

1. Warten Sie zwei bis drei Minuten, nachdem Sie zur Seite „Überwachen“ gelangt sind.  Wenn die Überwachung NICHT aktiviert ist, wird oben auf der Seite ein blauer Balken mit der Meldung „Aufzeichnung von Benutzer- und Administratoraktivitäten starten“ angezeigt.  Wählen Sie **Aufzeichnung von Benutzer- und Administratoraktivitäten starten** aus.  Wenn Sie aufgefordert werden, zu bestätigen, dass die Organisationseinstellung aktualisiert werden müssen, wählen Sie **Ja** aus. Sobald die Überwachung aktiviert ist, wird der blaue Balken nicht mehr angezeigt.  Wird der blaue Balken nicht angezeigt, ist die Überwachung bereits aktiviert, und keine weitere Aktion ist erforderlich.  Sie können die Aktivierung der Überwachung auch über PowerShell überprüfen. Dies wird im Rahmen dieses Kurses jedoch nicht behandelt.

1. Wählen Sie im linken Navigationsbereich **Start** aus, um zur Homepage des Microsoft 365 Compliance Center zurück zu gelangen.

### <a name="review"></a>Überprüfung

Bei dieser Einrichtung haben Sie Ihren Azure Pass unter Verwendung der gleichen Anmeldeinformationen eingelöst, die Sie auch für den Microsoft 365-Mandanten verwenden.  Außerdem haben Sie die Überwachungsprotokollfunktion in Microsoft 365 aktiviert.
