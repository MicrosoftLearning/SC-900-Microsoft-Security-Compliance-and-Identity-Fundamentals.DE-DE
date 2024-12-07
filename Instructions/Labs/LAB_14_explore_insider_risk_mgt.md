---
lab:
  title: "Erkunden des Insider-Risikomanagements in Microsoft\_Purview"
  module: Describe the data security solutions of Microsoft Purview
---

# Lab: Erkunden des Insider-Risikomanagements in Microsoft Purview

Dieses Lab ist den folgenden Learn-Inhalten zugeordnet:

- Lernpfad: Beschreiben der Funktionen von Microsoft Priva und Microsoft Purview
- Modul: Beschreiben der Datensicherheitslösungen von Microsoft Purview
- Lerneinheit: Beschreiben des Insider-Risikomanagements in Microsoft Purview

## Labszenario

In diesem Lab gehen Sie den Einstellungsprozess einer Insider-Risikorichtlinie und die grundlegenden Voraussetzungen zum Konfigurieren und Verwenden von Insider-Risikomanagementrichtlinien durch.  Hinweis: Dieses Lab umfasst Informationen zum Einrichten des Insider-Risikomanagements und zu den Optionen für das Erstellen einer Richtlinie.  In diesem Lab ist keine Aufgabe zum Auslösen der Richtlinie enthalten, da die Anzahl der Ereignisse, die zum Auslösen einer Richtlinie erforderlich sind, und die erforderliche Zeit den Rahmen dieser Übung überschreiten.

**Geschätzte Dauer**: 60 Minuten

### Aufgabe 1

Bei dieser Aufgabe aktivieren Sie als globale(r) Administrator*in Berechtigungen für das Insider-Risikomanagement.  Insbesondere fügen Sie dabei der Rollengruppe „Insider-Risikomanagement“ Benutzer hinzu, um sicherzustellen, dass die vorgesehenen Benutzer auf die Funktion „Insider-Risikomanagement“ zugreifen und diese verwenden können.  Es kann bis zu 30 Minuten dauern, bis die Rollengruppenberechtigungen für Benutzer*innen in der gesamten Organisation gelten.

1. Öffnen Sie die Browserregisterkarte für die Startseite von Microsoft Purview.  Wenn Sie die Registerkarte zuvor geschlossen haben, öffnen Sie eine neue Browserregisterkarte, und geben Sie **https://admin.microsoft.com** ein. Melden Sie sich mit den Administratoranmeldeinformationen für den Microsoft 365-Mandanten an, der vom autorisierten Labhoster (ALH) bereitgestellt wird. 

1. Wählen Sie im linken Navigationsbereich von Microsoft 365 Admin Center **Alle anzeigen** und dann **Compliance** aus.  Die Startseite des Microsoft Purview-Portals wird auf einer neuen Browserseite geöffnet.  

1. Wählen Sie im linken Navigationsbereich **Einstellungen**, erweitern Sie **Rollen und Bereiche** und wählen Sie dann **Rollengruppen**.

1. Geben Sie in das Suchfeld oben rechts auf der Seite **Insider-Risiko** ein und fahren Sie mit der Eingabetaste auf Ihrer Tastatur fort.  Beachten Sie die zahlreichen Rollen, die angezeigt werden.  Jedes dieser Elemente weist unterschiedliche Zugriffsebenen auf.  Wählen Sie **Insider-Risikomanagement** aus, und überprüfen Sie die Beschreibung.  Scrollen Sie nach unten, bis Mitglieder angezeigt werden, und beachten Sie, dass „MOD Administrator“ und „Megan Bowen“ aufgeführt werden. Schließen Sie das Fenster, indem Sie in der oberen rechten Ecke des Bildschirms das **X** auswählen.

1. Wählen Sie im linken Navigationsbereich **Startseite** aus, um zur Microsoft Purview-Portalseite zurückzukehren.

1. Lassen Sie diese Browserregisterkarte geöffnet, da Sie in einer nachfolgenden Aufgabe zu ihr zurückkehren werden.

### Aufgabe 2

Bei dieser Aufgabe gehen Sie die Einstellungen der Insider-Risikomanagement-Lösung durch.  Einstellungen für das Insider-Risikomanagement gelten für alle Richtlinien zum Insider-Risikomanagement, unabhängig von der Vorlage, die Sie beim Erstellen einer Richtlinie auswählen.

1. Sie sollten sich auf der Startseite des Microsoft Purview-Portals befinden. Wenn nicht, wählen Sie die Browserregisterkarte  **Home – Microsoft 365 Compliance** aus.

1. Bevor Sie mit dem Einrichten einer Richtlinie beginnen, sollten Sie sich mit einigen Einstellungen vertraut machen und diese nach Bedarf für Ihr Unternehmen konfigurieren. Wählen Sie im linken Navigationsbereich **Einstellungen** und dann **Insider-Risikomanagement**.  Hier können Sie einige der verfügbaren Einstellungen erkunden.
    1. Wählen Sie **Datenschutz**: Für Benutzende, die Aktivitäten ausführen, die Ihren Richtlinien für Insider-Risiken entsprechen, wird mit dieser Einstellung festgelegt, ob ihre tatsächlichen Namen angezeigt werden oder ob anonymisierte Versionen verwendet werden, um ihre Identitäten zu verschleiern.  Für diese exemplarische Vorgehensweise können Sie die Standardeinstellung beibehalten.
    1. Wählen Sie **Richtlinienindikatoren aus**. Sobald ein Ereignis eintritt, das eine Richtlinie auslöst, werden die Aktivitäten, die mit den ausgewählten Indikatoren verknüpft sind, zur Ermittlung der Risikobewertung für den Benutzenden herangezogen. Die hier ausgewählten Richtlinienindikatoren sind in den Vorlagen für Richtlinien zum Insider-Risiko enthalten.  Scrollen Sie, um alle verfügbaren Indikatoren und alle zugehörigen Informationen anzuzeigen. 
    1. Wählen Sie **Richtlinien-Zeitrahmen**. Die von Ihnen hier ausgewählten Zeitrahmen treten für Benutzende in Kraft, wenn sie einen Treffer für eine Insider-Risikorichtlinie auslösen.   Das Aktivierungsfenster bestimmt, wie lange Richtlinien Aktivitäten für Benutzer*innen aktiv erkennen und ausgelöst werden, wenn ein(e) Benutzer*in die erste Aktivität ausführt, die zu einer Richtlinie passt. Die Erkennung früherer Aktivitäten bestimmt, wie weit eine Richtlinie zurückgeht, um Benutzeraktivitäten zu erkennen und ausgelöst wird, wenn ein(e) Benutzer*in die erste Aktivität ausführt, die zu einer Richtlinie passt.  Lassen Sie die Standardwerte unverändert.
    1. Wählen Sie **Intelligente Erkennungen**. Überprüfen Sie die Optionen hier.  Beachten Sie die Domänen-Einstellungen und ihre Beziehung zu den Indikatoren.
    1. Erkunden Sie die anderen Elemente, die in den Einstellungen aufgeführt sind, und beachten Sie, dass sich viele in der Vorschau befinden.

1. Wählen Sie im linken Navigationsbereich **Lösungen** und dann **Insider-Risikomanagement**.

1. Lassen Sie diese Browserregisterkarte geöffnet, da Sie sie in der nächsten Aufgabe verwenden werden.

### Aufgabe 3

In dieser Aufgabe gehen Sie die Einstellungen zum Erstellen einer Richtlinie durch.  Das Ziel besteht einfach darin, ein Gefühl für die verschiedenen Optionen und die Flexibilität zu erhalten, die mit der Erstellung einer Richtlinie verbunden sind.

1. Sie sollten sich auf der Übersichtsseite „Insider-Risikomanagement“ befinden.  Falls noch nicht vorhanden, wählen Sie im linken Navigationsbereich **Lösungen** und dann **Insider-Risikomanagement**.

1. Wählen Sie auf der Übersichtsseite für das Insider-Risikomanagement die Registerkarte **Richtlinien** und dann **+ Erstellen** aus.  Konfigurieren Sie jede der folgenden Richtlinienregisterkarten.

    1. Richtlinienvorlage: Wählen Sie unter der Kategorie „Datenlecks“ die Option **Datenlecks** aus.  Lesen Sie die Details für diese Vorlage. Unter Voraussetzungen wird die DLP-Richtlinie mit einem Häkchen in einem grünen Kreis angezeigt, um anzugeben, dass die Voraussetzung erfüllt ist.  Es gibt eine DLP-Richtlinie, die für diesen Lab-Mandanten vorkonfiguriert wurde. Wählen Sie **Weiter** aus. 
    1. Name und Beschreibung: Geben Sie den Namen **SC900-InsiderRiskPolicy** ein, und wählen Sie dann **Weiter** aus.
    1. Benutzer*innen und Gruppen: Lesen Sie das Informationsfeld.  Behalten Sie die Standardeinstellung **Alle Benutzer*innen und Gruppen einschließen** bei.  Wählen Sie **Weiter** aus.
    1. Benutzende und Gruppen ausschließen (optional) (Vorschau): Hier können Sie auszuschließende Benutzende und Gruppen auflisten. Nehmen Sie keine Änderungen vor. Wählen Sie **Weiter** aus.
    1. Zu priorisierende Inhalte: Laut Beschreibung werden die Risikobewertungen für jede Aktivität erhöht, die Prioritätsinhalte enthält, was wiederum die Wahrscheinlichkeit erhöht, eine Warnung mit hohem Schweregrad zu generieren. Der Einfachheit halber wählen Sie **Ich möchte Inhalte jetzt nicht priorisieren** aus, und wählen Sie dann **Weiter** aus.
    1. Trigger: Das auslösende Ereignis bestimmt, wann eine Richtlinie beginnt, der Aktivität eines Benutzers Risikobewertungen zuzuweisen.  Sie können eine vorhandene DLP-Richtlinie auswählen oder ob der Benutzer eine Exfiltrationsaktivität ausführen soll. Wählen Sie **Benutzer entspricht einer DLP-Richtlinie** aus, und wählen Sie dann in der Dropdownliste **U.S. Financial Data** aus. Wählen Sie **Weiter** aus.
    1. Indikatoren: Beachten Sie die ausgewählten Indikatoren. Nehmen Sie keine Änderungen vor. Wählen Sie **Weiter** aus.
    1. Behalten Sie auf der Seite „Erkennungsoptionen“ alle Standardeinstellungen bei, lesen Sie aber die Beschreibung, die den verschiedenen Optionen zugeordnet ist, und zeigen Sie auf das Informationssymbol, um ausführlichere Informationen zu einer bestimmten Einstellung zu erhalten.  Wählen Sie **Weiter** aus.
    1. Behalten Sie auf der Seite, auf der Sie entscheiden können, ob Sie die Standard- oder kundenseitig festgelegte Indikatorschwellenwerte verwenden möchten, die Standardeinstellung **Standardschwellenwerte von Microsoft verwenden** bei, und wählen Sie dann **Weiter** aus.
    1. Fertigstellen: Überprüfen Sie die Einstellungen und wählen Sie **Senden** aus.
    1. Überprüfen Sie die Beschreibung, was als Nächstes geschieht, und wählen Sie dann **Fertig** aus.

1. Sie befinden sich wieder auf der Registerkarte „Richtlinien“ der Seite „Insider-Risikomanagement“.  Die von Ihnen erstellte Richtlinie wird aufgelistet.  Wenn sie nicht angezeigt wird, wählen Sie das Symbol **Aktualisieren** aus.

1. Als Administrator können Sie sofort damit beginnen, Benutzern Risikobewertungen basierend auf Aktivitäten zuzuweisen, die von den von Ihnen ausgewählten Richtlinien erkannt wurden. Dadurch wird die Anforderung umgangen, dass zuerst ein auslösendes Ereignis (z. B. eine DLP-Richtlinienentsprechung) erkannt wird.  Ein Administrator wählt dazu das leere Quadrat neben dem Richtliniennamen aus, um die Richtlinie auszuwählen. Wählen Sie dann die oberhalb der Tabelle mit den Richtlinien angezeigte Option **Bewertungsaktivität für Benutzer starten** aus.  Ein neues Fenster wird geöffnet, in dem der Administrator die verfügbaren Felder mit Daten auffüllen muss. Lassen Sie die Felder leer, da Sie diese Option nicht konfigurieren. Wenn Sie weitere Informationen dazu erhalten möchten, warum ein Administrator so vorgehen möchte, wählen Sie **Warum sollte ich so vorgehen?** aus.  Schließen Sie das Fenster, indem Sie in der oberen rechten Ecke des Bildschirms das **X** auswählen.

1. Wählen Sie im linken Navigationsbereich **Startseite**, um zur Startseite des Microsoft Purview Portals zurückzukehren.

1. Lassen Sie die Browserregisterkarte geöffnet.

### Überprüfung

In diesem Lab sind Sie den Einstellungsprozess einer Richtlinie zum Insider-Risiko und die grundlegenden Voraussetzungen zum Konfigurieren und Verwenden von Richtlinien zum Insider-Risikomanagement durchgegangen.
