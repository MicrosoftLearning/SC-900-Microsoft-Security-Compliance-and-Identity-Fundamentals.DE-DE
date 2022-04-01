---
lab:
  title: Erkunden von Microsoft Intune
  module: 'Module 3 Lesson 6: Describe the capabilities of Microsoft security solutions: Describe endpoint security with Microsoft Intune'
ms.openlocfilehash: 648343111d82426fe30e1ceeed4e91062649fbcd
ms.sourcegitcommit: a341c2fc38e9b37dafb792d82e3c948f7ba4a099
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/14/2022
ms.locfileid: "137893983"
---
# <a name="lab-explore-microsoft-intune"></a>Lab: Erkunden von Microsoft Intune

## <a name="lab-scenario"></a>Labszenario

In diesem Lab erkunden Sie Microsoft Intune in Microsoft Endpoint Manager. Hinweis: In dieser Lab-Instanz werden weder Endpunkte noch Geräte konfiguriert. In dieser exemplarischen Vorgehensweise werden daher keine tatsächlichen Endpunktinformationen gezeigt. Diese exemplarische Vorgehensweise dient dem Kursteilnehmer lediglich als Orientierung, welche Informationen wo verfügbar sind.  Eine ausführlichere exemplarische Vorgehensweise finden Sie im Video (<https://www.microsoft.com/en-us/videoplayer/embed/RE4LTIu>) in den zugehörigen Learn-Inhalten.

**Geschätzte Dauer**: 10–15 Minuten

#### <a name="task-in-this-task-you-will-explore-microsoft-intune-in-microsoft-endpoint-manager"></a>Aufgabe: In dieser Aufgabe erkunden Sie Microsoft Intune in Microsoft Endpoint Manager.

1. Öffnen Sie Microsoft Edge. Geben Sie **admin.microsoft.com** in die Adressleiste ein.

1. Melden Sie sich mit Ihren Administratoranmeldeinformationen an.
    1. Geben Sie **admin@WWLxZZZZZZ.onmicrosoft.com** (ZZZZZZ ist hierbei die eindeutige Mandanten-ID, die von Ihrem Labhostinganbieter bereitgestellt wurde) in das Fenster „Anmelden“ ein, und wählen Sie dann **Weiter** aus.
    
    1. Geben Sie das Administratorkennwort ein, das Sie vom Labhostinganbieter erhalten haben sollten. Wählen Sie **Anmelden**.
    1. Wählen Sie **Ja** aus, wenn Sie gefragt werden, ob Sie angemeldet bleiben möchten. Dadurch gelangen Sie zur Seite „Microsoft 365 Admin Center“.

1. Wählen Sie im linken Navigationsbereich von Microsoft 365 Admin Center **Alle anzeigen** und dann **Alle Admin Center** aus.

1. Wählen Sie auf der Seite „Alle Admin Center“ **Endpunkt-Manager** aus.  Das Microsoft Endpoint Manager Admin Center wird auf einer neuen Browserseite geöffnet.

1. Wählen Sie im linken Navigationsbereich **Dashboard** aus, um Gesamtdetails über die Geräte und Client-Apps im Intune-Mandanten anzuzeigen.

1. Wählen Sie im linken Navigationsbereich **Geräte** aus, um Details über die im Intune-Mandanten registrierten Geräte anzuzeigen. Der Bereich Devices – Overview (Geräte – Übersicht) verfügt über mehrere Registerkarten, mit denen Sie eine Zusammenfassung der folgenden Status und Warnmeldungen sehen können:
    1. **Registrierungsstatus:** Überprüfen Sie die Details über die mit Intune registrierten Geräte nach Plattform- und Registrierungsfehler.
    
    1. **Registrierungswarnungen:** Erfahren Sie weitere Details über nicht zugewiesene Geräte nach Plattform.
    1. **Compliance status:** (Konformitätsstatus) Überprüfen Sie basierend auf dem Gerät, der Richtlinie, der Einstellung, der Bedrohung und dem Schutz den Konformitätsstatus. Zusätzlich dazu finden Sie in diesem Bereich eine Liste mit Geräten ohne eine Konformitätsrichtlinie.
    1. **Konfigurationsstatus:** Überprüfen Sie den Konfigurationsstatus von Geräteprofilen als auch von der Gerätebereitstellung.
    1. **Softwareupdatestatus:** Sehen Sie ein Visual des Bereitstellungsstatus für alle Geräte und für alle Benutzer.

1. Wählen Sie im Bereich Devices – Overview (Geräte – Übersicht) **Bedingter Zugriff** aus, um Details zu den Zugriffsrichtlinien zu erhalten.

1. Wählen Sie im linken Navigationsbereich **Geräte** und dann **Konfigurationsprofile** aus, um Details über Geräteprofile in Intune anzuzeigen.

1. Wählen Sie im linken Navigationsbereich **Geräte** und dann **Alle Geräte** aus, um Details über die registrierten Geräte des Intune-Mandanten anzuzeigen.  Obwohl keine Geräte aufgelistet werden, enthält diese Tabelle wichtige Details zu Compliance, Betriebssystemversion und zum Datum des letzten Check-Ins.

1. Wählen Sie im Navigationsbereich **Apps** aus, um eine Übersicht über den App-Status zu erhalten. Es gibt zwei Registerkarten, auf denen eine Übersicht der folgenden Status angezeigt wird:
    1. **Installationsstatus:** Sehen Sie die häufigsten Installationsfehler nach Gerät und die Apps mit Installationsfehlern.
    1. **App-Schutzrichtlinienstatus:** Erhalten Sie Details zu zugewiesenen und gekennzeichneten Benutzern in App-Schutzrichtlinien.

1. Wählen Sie im Bereich Apps – Overview (Apps – Übersicht) **Alle Apps** aus, um die in Intune hinzugefügte App-Liste zu erhalten.

1. Wählen Sie im linken Navigationsbereich **Benutzer** aus, um Details über die von Ihnen in Intune eingeschlossenen Benutzer anzuzeigen. Bei diesen Benutzern handelt es sich um die Mitarbeiter Ihres Unternehmens Contoso.

1. Wählen Sie im linken Navigationsbereich **Gruppen** aus, um Details über die in Intune enthaltenen Azure Active Directory(Azure AD)-Gruppen anzuzeigen.

1. Wählen Sie im linken Navigationsbereich **Mandantenverwaltung** aus, um Details über den Intune-Mandanten anzuzeigen.

1. Wählen Sie im linken Navigationsbereich **Problembehandlung + Support** und dann **Problembehandlung** aus, um die Statusdetails eines bestimmten Benutzers zu überprüfen.

#### <a name="review"></a>Überprüfung

In diesem Lab haben Sie Microsoft Intune in Microsoft Endpoint Manager erkundet. Hinweis: In dieser Lab-Instanz werden weder Endpunkte noch Geräte konfiguriert. In dieser exemplarischen Vorgehensweise werden daher keine tatsächlichen Endpunktinformationen gezeigt. Diese exemplarische Vorgehensweise dient dem Kursteilnehmer lediglich als Orientierung, welche Informationen wo verfügbar sind.  Eine ausführlichere exemplarische Vorgehensweise finden Sie im Video (<https://www.microsoft.com/en-us/videoplayer/embed/RE4LTIu>) in den zugehörigen Learn-Inhalten.