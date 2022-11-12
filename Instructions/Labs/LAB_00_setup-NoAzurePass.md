---
ms.openlocfilehash: 57c3c2d1e24acc7efaab97162e443a664dd76965
ms.sourcegitcommit: 804b98d288b1db2c11a5154b4ded954e87f5ae55
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/28/2022
ms.locfileid: "148119015"
---
<a name="---"></a><!---
---
Lab: Title: 'Setup'
---
--->

# <a name="lab-setup"></a>Lab: Setup

## <a name="lab-scenario"></a>Labszenario

Bei diesem Setuplab geht es um die Aktivierung des Microsoft-Überwachungsprotokolls.

**Geschätzte Dauer**: 5–10 Minuten

### <a name="setup---enable-microsoft-365-audit-log"></a>Einrichtung – Aktivieren des Microsoft 365-Überwachungsprotokolls

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

In diesem Setup haben Sie die Überwachungsprotokollfunktion in Microsoft 365 aktiviert.