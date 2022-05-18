---
lab:
  title: Erkunden des Insider-Risikomanagements in Microsoft Purview
  module: 'Module 4 Lesson 4: Describe the capabilities of Microsoft compliance solutions: Describe insider risk capabilities in Microsoft Purview'
ms.openlocfilehash: 8bd1f517bfbc4f71fec1ab65dca93b7b95458832
ms.sourcegitcommit: 25998048c2e354ea23d6f497205e8a062d34ac80
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2022
ms.locfileid: "144557541"
---
# <a name="lab-explore-insider-risk-management-in-microsoft-purview"></a>Lab: Erkunden des Insider-Risikomanagements in Microsoft Purview

## <a name="lab-scenario"></a>Labszenario

In diesem Lab gehen Sie den Einstellungsprozess einer Insider-Risikorichtlinie und die grundlegenden Voraussetzungen zum Konfigurieren und Verwenden von Insider-Risikomanagementrichtlinien durch.  Hinweis: Dieses Lab umfasst Informationen zum Einrichten des Insider-Risikomanagements und zu den Optionen für das Erstellen einer Richtlinie.  In diesem Lab ist keine Aufgabe zum Auslösen der Richtlinie enthalten, da die Anzahl der Ereignisse, die zum Auslösen einer Richtlinie erforderlich sind, außerhalb des Bereichs dieser Übung liegen.

**Geschätzte Dauer**: 25-30 Minuten

### <a name="task-1"></a>Aufgabe 1

Bei dieser Aufgabe aktivieren Sie als globaler Administrator Berechtigungen für das Insider-Risikomanagement.  Insbesondere fügen Sie dabei der Rollengruppe „Insider-Risikomanagement“ Benutzer hinzu, um sicherzustellen, dass die vorgesehenen Benutzer auf die Funktion „Insider-Risikomanagement“ zugreifen und diese verwenden können.  Es kann bis zu 30 Minuten dauern, bis die Rollengruppenberechtigungen auf die Benutzer in der gesamten Organisation angewendet werden.

1. Öffnen Sie Microsoft Edge. Geben Sie **admin.microsoft.com** in die Adressleiste ein.

1. Melden Sie sich mit Ihren Administratoranmeldeinformationen an.
    1. Geben Sie **admin@WWLxZZZZZZ.onmicrosoft.com** (ZZZZZZ ist hierbei die eindeutige Mandanten-ID, die von Ihrem Labhostinganbieter bereitgestellt wurde) in das Fenster „Anmelden“ ein, und wählen Sie dann **Weiter** aus.

    1. Geben Sie das Administratorkennwort ein, das Sie vom Labhostinganbieter erhalten haben sollten. Wählen Sie **Anmelden**.
    1. Wählen Sie **Ja** aus, wenn Sie gefragt werden, ob Sie angemeldet bleiben möchten. Dadurch gelangen Sie zur Seite „Microsoft 365 Admin Center“.

1. Wählen Sie im linken Navigationsbereich von Microsoft 365 Admin Center **Alle anzeigen** aus.

1. Wählen Sie unter „Admin Center“ die Option **Compliance** aus.  Die Startseite des Microsoft Purview-Complianceportals wird auf einer neuen Browserseite geöffnet.  

1. Wählen Sie im linken Navigationsbereich des Microsoft Purview-Complianceportals **Berechtigungen** aus.

1. Wählen Sie auf der Seite „Berechtigungen und Rollen“ unter „Complianceportal“ die Option **Rollen** aus.

1. Geben Sie **Insider-Risiko** in die Suchleiste ein. Wählen Sie dann das Suchsymbol (Vergrößerungsglas) aus.  Beachten Sie die zahlreichen Rollen, die angezeigt werden.  Diese weisen jeweils unterschiedliche Zugriffsebenen auf.  Wählen Sie **Insider-Risikomanagement** aus.

1. Wählen Sie im Fenster, das geöffnet wird, neben „Mitglieder“ die Option **Bearbeiten** aus.

1. Wählen Sie **Mitglieder auswählen** aus, um dieser Rollengruppe Mitglieder hinzuzufügen.

1. Wählen Sie oben auf der Seite **+ hinzufügen** aus.

1. Wählen Sie in der Liste der Namen die Einträge **MOD-Administrator** und **Megan Bowen** aus. Wählen Sie dann unten auf der Seite die Option **Hinzufügen** und **Fertig** aus.

1. Überprüfen Sie, ob die hinzugefügten Mitglieder richtig sind, und wählen Sie dann **Speichern** aus.

1. Wählen Sie unten im Fenster „Insider-Risikomanagement“ die Option **Schließen** aus.

1. Wählen Sie im linken Navigationsbereich die **Startseite** aus, um zur des Microsoft Purview-Complianceportalseite zurückzukehren.

1. Lassen Sie diese Browserregisterkarte geöffnet, da Sie in einer nachfolgenden Aufgabe dorthin zurückkehren werden.

### <a name="task-2-skip-if-you-did-the-setup-lab-task-to-enable-the-audit-log"></a>Aufgabe 2 (ÜBERSPRINGEN Sie sie, falls Sie die Aufgabe „Lab einrichten“ zum Aktivieren des Überwachungsprotokolls absolviert haben)

Das Insider-Risikomanagement verwendet Microsoft 365-Überwachungsprotokolle für Benutzererkenntnisse und -aktivitäten in Richtlinien und Analyseerkenntnisse. Bei dieser Aufgabe aktivieren Sie die Funktion „Überwachungsprotokollsuche“. Hinweis:  Nach der Aktivierung der Überwachungsprotokollsuche kann es mehrere Stunden dauern, bis beim Durchsuchen des Überwachungsprotokolls Ergebnisse zurückgegeben werden.  Obwohl es mehrere Stunden dauern kann, bis Sie das Überwachungsprotokoll durchsuchen können, wirkt sich dies nicht auf die Fähigkeit aus, andere Aufgabe in diesem Lab abzuschließen.

1. Wählen Sie die Browserregisterkarte mit der Bezeichnung **Startseite – Microsoft 365 Compliance** aus.  Wenn Sie diese Browserregisterkarte zuvor geschlossen haben, öffnen Sie Microsoft Edge, und geben Sie **compliance.microsoft.com** in die Adressleiste ein. Melden Sie sich dann mit Ihren Administratoranmeldeinformationen an.

1. Wählen Sie im linken Navigationsbereich unter „Lösungen“ die Option **Überwachen** aus.

1. Stellen Sie sicher, dass die Registerkarte **Suche** ausgewählt (unterstrichen) ist.

1. Warten Sie zwei bis drei Minuten, nachdem Sie zur Seite „Überwachen“ gelangt sind.  Wenn die Überwachung NICHT aktiviert ist, wird oben auf der Seite ein blauer Balken mit der Meldung „Aufzeichnung von Benutzer- und Administratoraktivitäten starten“ angezeigt.  Wählen Sie **Aufzeichnung von Benutzer- und Administratoraktivitäten starten** aus.  Sobald die Überwachung aktiviert ist, wird der blaue Balken nicht mehr angezeigt.  Wird der blaue Balken nicht angezeigt, ist die Überwachung bereits aktiviert, und keine weitere Aktion ist erforderlich.

1. Wählen Sie im linken Navigationsbereich die **Startseite** aus, um zur Startseite des Microsoft Purview-Complianceportals zurückzukehren.

1. Lassen Sie diese Browserregisterkarte geöffnet, da Sie sie in der nächsten Aufgabe verwenden werden.

### <a name="task-3"></a>Aufgabe 3

Bei dieser Aufgabe gehen Sie die Einstellungen der Insider-Risikomanagement-Lösung durch.  Die Einstellungen für das Insider-Risikomanagement gelten für alle Richtlinien für das Insider-Risikomanagement, unabhängig davon, welche Vorlage Sie beim Erstellen einer Richtlinie auswählen.

1. Sie sollten sich auf der Startseite des Microsoft Purview-Complianceportals befinden. Falls nicht, öffnen Sie die Browserregisterkarte **Startseite – Microsoft 365 Compliance**.

1. Wählen Sie im linken Navigationsbereich unter „Lösungen“ die Option **Insider-Risikomanagement** aus.

1. Vor dem Einrichten einer Richtlinie müssen einige Einstellungen konfiguriert werden.  Wählen Sie auf der Seite „Insider-Risikomanagement“ in der oberen rechten Ecke der Seite das **Zahnradsymbol für die Einstellungen** aus, um auf „Einstellungen für Risiken durch Insider“ zuzugreifen.  
    1. Überprüfen Sie, ob Sie sich auf der Registerkarte **Datenschutz** befinden: Für Benutzer, die Aktivitäten ausführen, die Ihren Insiderrisikorichtlinien entsprechen, bestimmt diese Einstellung, ob ihre tatsächlichen Namen angezeigt oder anonymisierte Versionen verwendet werden sollen, um ihre Identitäten zu maskieren.  Wählen Sie **Keine anonymisierten Versionen von Benutzernamen anzeigen** und dann **Speichern** aus.

    1. Wählen Sie die Registerkarte **Richtlinienindikatoren** aus. Wenn eine Richtlinie ausgelöst wird, werden den ausgewählten Indikatoren zugeordnete Aktivitäten verwendet, um die Risikobewertung für den Benutzer zu bestimmen. Die hier ausgewählten Richtlinienindikatoren werden in Vorlagen für die Insider-Risikorichtlinie aufgenommen.  Scrollen Sie, um alle verfügbaren Indikatoren und die zugehörigen Informationen anzuzeigen. Wählen Sie unter **Office-Indikatoren** die Option **Alles auswählen** und dann **Speichern** aus.
    1. Wählen Sie die Registerkarte **Richtlinien-Zeitrahmen** aus. Die von Ihnen hier ausgewählten Zeitrahmen treten für einen Benutzer in Kraft, wenn er eine Übereinstimmung für eine Insider-Risikorichtlinie auslöst.   Im Fenster „Aktivierung“ wird festgelegt, wie lange Richtlinien aktiv Aktivitäten für Benutzer erkennen und ausgelöst werden, wenn ein Benutzer die erste Aktivität ausführt, die mit einer Richtlinie übereinstimmt. Mit „Bisherige Aktivitätserkennung“ wird festgelegt, wie weit eine Richtlinie zurückreichen soll, um Benutzeraktivitäten zu erkennen, und wird ausgelöst, wenn ein Benutzer die erste Aktivität ausführt, die mit einer Richtlinie übereinstimmt.  Lassen Sie die Standardwerte unverändert.  Wählen Sie die Registerkarte **Intelligente Erkennungen** aus.
    1. Wählen Sie die Registerkarte **Intelligente Erkennungen** aus. Überprüfen Sie die hier vorhandenen Optionen.  Beachten Sie die Domäneneinstellungen und wie sie mit den Indikatoren zusammenhängen.
    1. Erkunden Sie die anderen Elemente, die in den Einstellungen aufgeführt sind, und beachten Sie, dass sich viele in der Vorschau befinden.

1. Wählen Sie in der oberen linken Ecke der Seite oberhalb von „Einstellungen“ die Option **Insider-Risikomanagement** aus, um zur Übersicht über Insider-Risikomanagement zurückzukehren.

1. Lassen Sie diese Browserregisterkarte geöffnet, da Sie sie in der nächsten Aufgabe verwenden werden.

### <a name="task-4"></a>Aufgabe 4

Bei dieser Aufgabe gehen Sie die Erstellung einer Richtlinie durch.

1. Sie sollten sich auf der Seite „Insider-Risikomanagement“ befinden.  Falls Sie noch nicht dort sind, öffnen Sie die Browserregisterkarte mit der Bezeichnung **Insider-Risikomanagement – Microsoft 365 Compliance**.

1. Wählen Sie auf der Übersichtsseite für das Insider-Risikomanagement die Registerkarte **Richtlinien** und dann **+ Erstellen** aus.  Konfigurieren Sie jede der folgenden Registerkarten für Richtlinien.

    1. Richtlinienvorlage:  Wählen Sie in der Liste der Kategorien den Eintrag **Datenlecks** und dann **Allgemeine Datenlecks** aus.  Beachten Sie, dass die Vorlagen in den Kategorien möglicherweise zusätzliche Voraussetzungen aufweisen.  Lesen Sie die Details für diese Vorlage, und wählen Sie dann **Weiter** aus.

    1. Name und Beschreibung: Geben Sie den Namen **SC900-InsiderRiskPolicy** ein, und wählen Sie dann **Weiter** aus.
    1. Benutzer und Gruppen:  Lesen Sie das Informationsfeld.  Übernehmen Sie die Standardeinstellung **Alle Benutzer und Gruppen aufnehmen**.  Klicken Sie auf **Weiter**.
    1. Zu priorisierender Inhalt: Lesen Sie die Beschreibung. Wählen Sie **Ich möchte SharePoint-Sites, Vertraulichkeitsbezeichnungen bzw. Typen vertraulicher Informationen als Prioritätsinhalt angeben** und dann **Weiter** aus.
        1. SharePoint-Site: Lassen Sie dies bei diesem Richtlinienbeispiel leer, und wählen Sie **Weiter** aus.
        1. Typen vertraulicher Informationen: Lassen Sie dies bei diesem Richtlinienbeispiel leer, und wählen Sie dann **Weiter** aus.
        1. Vertraulichkeitsbezeichnungen: Wählen Sie **Vertraulichkeitsbezeichnungen hinzufügen oder bearbeiten** aus.  Wählen Sie die aufgelisteten Bezeichnungen aus:  **Vertraulich – Finanzen** und **Sehr vertraulich\Projekt – Falcon**, wählen Sie **Hinzufügen** und dann **Weiter** aus.
    1. Auslösung: Überprüfen Sie die ausführlichen Informationen.  Die Richtlinie wird ausgelöst, wenn der Benutzer eine definierte Exfiltrationsaktivität (wählen Sie die Informationssymbole für den jeweiligen Gliederungspunkt aus, um ausführlichere Informationen zu erhalten) ausführt ODER eine Übereinstimmung mit einer vorhandenen Richtlinie zur Verhinderung von Datenverlust (DLP) vorliegt.  Wählen Sie **Benutzer führt Exfiltrationsaktivität aus** aus, da Sie im Rahmen dieser Übung keine DLP-Richtlinie konfiguriert haben.  Beachten Sie, dass die bei der vorherigen Aufgabe von Ihnen ausgewählten Richtlinienindikatoren aktiviert sind.   Beachten Sie, dass diese Indikatoren erst nach der Richtlinienauslösung aktiviert werden und dass die diesen Indikatoren zugeordneten Aktivitäten zum Berechnen einer Risikobewertung für den Benutzer verwendet werden. Klicken Sie auf **Weiter**.
    1. Indikatorschwellenwerte: Hier können Sie die standardmäßigen oder benutzerdefinierten Schwellenwerte für die Indikatoren angeben.  Beachten Sie, dass die Indikatoren erst nach dem Richtlinientrigger aktiviert werden. Daher wirken sich diese Richtlinien nicht darauf aus, wann die Richtlinie ausgelöst wird. Wählen Sie **Benutzerdefinierte Schwellenwerte angeben** aus. Durch Auswahl dieser Option können Sie die aktuellen Standardwerte anzeigen. Übernehmen Sie die Standardeinstellungen, und wählen Sie **Weiter** aus.  
    1. Indikatoren: Beachten Sie, dass alle Office-Indikatoren, die Sie in der vorherigen Aufgabe ausgewählt haben, ausgewählt sind.  Scrollen Sie durch die Seite, um andere verfügbare Richtlinienindikatoren und andere Elemente anzuzeigen, die automatisch ausgewählt werden.   Die Sequenzerkennung ist aktiviert.  Wenn eine Sequenz von Aktivitäten, wie definiert, erkannt wird, deutet dies auf ein größeres Risiko hin.  Bewegen Sie den Mauszeiger auf das Informationssymbol, um ausführliche Informationen zu erhalten.  Für diese Elemente müssen bestimmte Indikatoren ausgewählt und Geräte integriert werden.  Deaktivieren Sie der Einfachheit halber und deshalb, dass für diesen Mandanten keine Geräte integriert sind, die Option **Alles auswählen**.
    1. Fertigstellen: Überprüfen Sie die Einstellungen, wählen Sie **Senden** und dann **Fertig** aus.

1. Sie befinden sich wieder auf der Registerkarte „Richtlinien“ der Seite „Insider-Risikomanagement“.  Die von Ihnen soeben erstellte Richtlinie wird aufgelistet.  

1. Bei der von Ihnen soeben erstellten Richtlinie werden im Feld „Benutzer im Geltungsbereich“ Benutzer angezeigt, denen aktuell durch die Richtlinie Risikobewertungen zugewiesen sind.  Benutzern werden Risikobewertungen zugewiesen, wenn die Richtlinie ausgelöst wird. Daher wird der Wert „0“ angezeigt.  Ein Administrator kann eine Richtlinie konfigurieren, um bestimmten Benutzern basierend auf der von den von Ihnen ausgewählten Richtlinien erkannten Aktivität Risikobewertungen zuzuweisen UND welche die Anforderung umgeht, dass zunächst ein auslösendes Ereignis erkannt wird.  Wählen Sie dazu den leeren Kreis neben dem Richtliniennamen aus, um die Richtlinie auszuwählen. Wählen Sie dann die oberhalb der Tabelle mit den Richtlinien angezeigte Option **Bewertung starten** aus.  Füllen Sie jedes Feld aus, und wählen Sie dann **Bewertung der Aktivitäten starten** aus.  Es kann bis zu 24 Stunden dauern, bis die Benutzer auf der Registerkarte „Benutzer“ angezeigt werden. Danach können Sie die Benutzer auf dieser Registerkarte auswählen, um erkannte Aktivitäten zu überprüfen.  Klicken Sie unten im Fenster auf **Schließen**.

### <a name="review"></a>Überprüfung

In diesem Lab sind Sie den Einstellungsprozess einer Insider-Risikorichtlinie und die grundlegenden Voraussetzungen zum Konfigurieren und Verwenden von Insider-Risikomanagementrichtlinien durchgegangen.
