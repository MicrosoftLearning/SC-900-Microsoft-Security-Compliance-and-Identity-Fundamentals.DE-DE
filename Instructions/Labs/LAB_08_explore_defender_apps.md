---
lab:
  title: 'Erkunden von Microsoft Defender für Cloud-Apps '
  module: 'Module 3 Lesson 4: Describe the capabilities of Microsoft security solutions: Describe threat protection with Microsoft 365 Defender'
ms.openlocfilehash: c6b9e816596c74199123b21a9fcb07a5d33a725c
ms.sourcegitcommit: a69acc26ed3a09cea4a3af95719a6edc7fe2814d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/29/2022
ms.locfileid: "146650064"
---
# <a name="lab-explore-microsoft-defender-for-cloud-apps"></a>Lab: Erkunden von Microsoft Defender für Cloud-Apps

## <a name="lab-scenario"></a>Labszenario

In diesem Lab erkunden Sie die Funktionen von Microsoft Defender für Cloud-Apps.  Sie gehen die im Cloud Discovery-Dashboard verfügbaren Informationen und die verfügbaren Funktionen zum Untersuchen von Ergebnissen und zum Steuern der Auswirkung auf Ihre Organisation durch Richtlinien durch.  Hinweis:  Eine Organisation muss über eine Lizenz verfügen, um Microsoft Defender für Cloud-Apps verwenden zu können, wobei es sich um einen benutzerbasierten Abonnementdienst handelt.

**Geschätzte Dauer**: 15 bis 20 Minuten

### <a name="task-1"></a>Aufgabe 1

Erkunden Sie Cloud Discovery.

1. Öffnen Sie Microsoft Edge. Geben Sie **admin.microsoft.com** in die Adressleiste ein.

1. Melden Sie sich mit Ihren Administratoranmeldeinformationen an.
    1. Geben Sie **admin@WWLxZZZZZZ.onmicrosoft.com** (ZZZZZZ ist hierbei die eindeutige Mandanten-ID, die von Ihrem Labhostinganbieter bereitgestellt wurde) in das Fenster „Anmelden“ ein, und wählen Sie dann **Weiter** aus.
    1. Geben Sie das Administratorkennwort ein, das Sie vom Labhostinganbieter erhalten haben sollten. Wählen Sie **Anmelden**.
    1. Wählen Sie **Ja** aus, wenn Sie gefragt werden, ob Sie angemeldet bleiben möchten. Dadurch gelangen Sie zur Seite „Microsoft 365 Admin Center“.

1. Wählen Sie im linken Navigationsbereich von Microsoft 365 Admin Center **Alle anzeigen** aus.

1. Wählen Sie **Sicherheit** unter „Admin Center“ aus.  Die Startseite des Microsoft 365 Defender-Portals wird auf einer neuen Browserseite geöffnet.  

1. Wählen Sie unten im linken Navigationsbereich der Seite „Microsoft 365 Defender“ die Option **Weitere Ressourcen** aus.

1. Wählen Sie auf der Karte **Microsoft Defender für Cloud-Apps** die Option **Öffnen** aus.  Das Cloud App Security-Dashboard wird auf einer neuen Browserseite geöffnet.  Beachten Sie die verfügbaren Informationskarten.  Es kann sein, dass auf den Karten keine Informationen angezeigt werden, da es sich hierbei um eine vorkonfigurierte Labmandantenumgebung handelt, die nicht aktiv verwendet wurde.  

1. Wählen Sie im linken Navigationsbereich **Ermitteln** aus. Wählen Sie dann im Dropdown das Dashboard **Cloud Discovery** aus.  Das Dashboard enthält eine Übersicht der ermittelten Apps, App-Kategorien, Risikostufen und mehr.  
    1. Wählen Sie oben auf der Seite „Cloud Discovery“ die Registerkarte **Ermittelte Apps** aus.  Das Fenster „Ermittelte Apps“ enthält eine ausführliche Ansicht der ermittelten Apps, einschließlich der Risikobewertung, des Datenverkehrs, der Anzahl der Benutzer und mehr.
        1. Wählen Sie für ein beliebiges Element in der Liste die **Auslassungspunkte** in der Spalte der Aktion der Tabelle aus.  Beachten Sie die verschiedenen Optionen, die verfügbar sind, einschließlich der Funktion, mit der eine Apps als sanktioniert oder nicht sanktioniert markiert werden kann.  Wählen Sie die Auslassungspunkte erneut aus, um das Aktionsfeld zu schließen.
        1. Durch die Auswahl eines bestimmten Zeilenelements wird für die bestimmte App eine Detailseite geöffnet.  Wählen Sie ein Element in der Liste aus.  Gehen Sie für das ausgewählte Element jede Registerkarte durch, die sich oben auf der Detailseite befindet.  **Nutzung**, **Info, IP**, **Adressen**, **Benutzer** und **Benachrichtigungen**. Wenn Sie die Detailseite fertig erkundet haben, kehren Sie zu den ermittelten Apps zurück. Wählen Sie dazu im linken Navigationsbereich die Option **Ermittelte Apps** aus.
    1. Wählen Sie oben auf der Seite die Registerkarte **IP-Adressen** (dies entspricht der Auswahl der IP-Adressen über den linken Navigationsbereich) aus.  Hier finden Sie Daten, darunter die Anzahl der Transaktionen, das Aufkommen von Datenverkehr und Uploadmengen nach IP-Adressen.  Beachten Sie, dass Sie auch nach einer bestimmten IP-Adresse filtern oder die Daten zur weitergehenden Analyse exportieren können.
    1. Wählen Sie oben auf der Seite (oder über den linken Navigationsbereich) die Option **Benutzer** aus.  Dies ist derselbe Informationstyp, der bei der Auswahl von IP-Adressen bereitgestellt wird. Er wird jedoch für einzelne Benutzer aufgelistet.  Auch hier filtern Sie nach einem bestimmten Benutzer und exportieren die Daten zur weitergehenden Analyse.

1. Die auf diesen Registerkarten bereitgestellten Informationen basieren auf Momentaufnahmeberichten aus von Ihnen manuell aus Ihren Firewalls und Proxys hochgeladenen Datenverkehrsprotokollen oder aus fortlaufenden Berichten, die alle Protokolle analysieren, die aus Ihrem Netzwerk mithilfe von Cloud App Security weitergeleitet werden.  Wählen Sie in der oberen rechten Ecke der Seite die vertikalen **Auslassungspunkte** aus, um zu erfahren, wo dies eingerichtet wird.
    1. Wählen Sie die erste Option **Momentaufnahmebericht zu Cloud Discovery erstellen** aus. Hier tragen Sie die erforderlichen Details ein und laden Datenverkehrsprotokolle hoch, um einen Bericht zu generieren und hochzuladen.  Wählen Sie **Beenden** aus.  Die für Ihren Labmandanten angezeigten Daten stammen aus einem Momentaufnahmebericht. Sie können diese Informationen in der oberen rechten Ecke des Bildschirms anzeigen.
    1. Wählen Sie zum Anzeigen der Option für fortlaufende Berichte die **Auslassungspunkte** in der oberen rechten Ecke der Seite aus, und wählen Sie im Dropdown den Eintrag **Automatischen Upload konfigurieren** aus.  Es sind keine Datenquellen verbunden. Hier würden Sie jedoch eine Datenquelle hinzufügen. Wählen Sie **Datenquelle hinzufügen** und dann im Fenster „Datenquelle hinzufügen“ den Dropdownpfeil im Feld „Quelle“ aus, um die Gerätetypen anzuzeigen, die Sie als Datenquelle verbinden können.  Wählen Sie **Abbrechen** aus, um den Vorgang zu beenden.

1. Ein weiterer Punkt, auf den Sie hinweisen sollten, ist, dass Sie sich direkt mit Apps verbinden können, indem Sie App-Konnektoren einrichten, die Ihnen eine bessere Sichtbarkeit und Kontrolle über Ihre Cloud-Apps ermöglichen. Wählen Sie in der oberen linken Ecke des Bildschirms das **Zahnradsymbol für die Einstellungen** aus. Wählen Sie dann in der Dropdownliste den Eintrag **App-Connectors** aus.  
    1. Auf der Seite „Verbundene Apps“ sollte „Office 365“ in der Liste mit einem verbundenen Status angezeigt werden.  Wenn für Office 365 ein Verbindungsfehler angezeigt wird, liegt dies höchstwahrscheinlich daran, dass die Option für die Überwachung nicht aktiviert ist.
    1. Wählen Sie **+ App verbinden** aus. Wählen Sie dann in der Dropdownliste den Eintrag **Microsoft Azure** aus.  Wählen Sie im Microsoft Azure-Popupfenster **Mit Microsoft Azure verbinden** aus.  Sie sehen den Verbunden-Status und Informationen zum Scannen von Benutzern, Daten und Aktivitäten.  Klicken Sie auf die Schaltfläche **Schließen**.

1. Lassen Sie diese Seite geöffnet, da Sie sie in der nächsten Aufgabe verwenden werden.

### <a name="task-2"></a>Aufgabe 2

Finden Sie Möglichkeiten, wie Sie die aufgezeichneten Aktivitäten untersuchen können.

1. Wählen Sie im linken Navigationsbereich unter „Untersuchen“ die Option **Aktivitätsprotokoll** aus.  Hier erhalten Sie Sichtbarkeit in alle Aktivitäten im Zusammenhang mit Ihren verbundenen Apps.   Da der Office 365-Connector bereits verbunden ist, sollten einige Daten angezeigt werden. Nachdem Sie mithilfe des App-Connectors eine Verbindung zwischen Cloud App Security und einer App hergestellt haben, scannt Cloud App Security alle Aktivitäten, die durchgeführt wurden, wobei die rückwirkende Scanzeit je nach App abweicht, und wird anschließend ständig mit neuen Aktivitäten aktualisiert.  

1. Wählen Sie die Aktivitätsspalte für ein Element aus, um ausführlichere Informationen anzuzeigen. Wählen Sie ganz rechts neben dem ausgewählten Element die vertikalen **Auslassungszeichen** aus.  Beachten Sie die verschiedenen Optionen.  Wählen Sie die Aktivitätsspalte für das jeweilige Element aus, um die Detailansicht zu reduzieren.

1. Beachten Sie oben auf der Seite die Option, eine neue Richtlinie aus der Suche hinzuzufügen oder die Daten für weitere Analysen zu exportieren.  Wählen Sie **+Neue Richtlinie aus Suche** aus.  Beachten Sie, wie Sie eine Richtlinie anhand einer Vorlage erstellen, einen Schweregrad und die Kategorie der Richtlinie auswählen, Filter für die Richtlinie erstellen, Warnungen erstellen und sogar Warnungen an Power Automate senden können.  Wählen Sie **Abbrechen** aus, um das Fenster zur Richtlinienerstellung zu schließen.

1. Wählen Sie im linken Navigationsbereich die Option **Dateien** aus, und beachten Sie die Optionen zum Filtern von Daten, Erstellen einer Dateirichtlinie und Exportieren der Daten.  

1. Wählen Sie im linken Navigationsbereich die Option **Benutzer und Konten** aus, und erkunden Sie diese.  Beachten Sie die Optionen zum Filtern von Daten und Exportieren der Daten.

1. Wählen Sie im linken Navigationsbereich die Option **Sicherheitskonfiguration** aus. Diese Seite umfasst Sicherheitskonfigurationsbewertungen für Ihre Azure-, Amazon Web Services- (AWS) und Google Cloud Platform-Konten (GCP).

1. Lassen Sie diese Seite geöffnet, da Sie sie in der nächsten Aufgabe verwenden werden.

### <a name="task-3"></a>Aufgabe 3

In dieser Aufgabe erkunden Sie die Seiten mit den Richtlinien und Warnungen in Microsoft Defender für Cloud-Apps.

1. Wählen Sie im linken Navigationsbereich neben der Stelle, an der **Steuerung** steht, den Pfeil nach unten und dann **Richtlinien** aus.  Die aufgelisteten Richtlinien umfassen Informationen zur Anzahl der von der Richtlinie generierten Warnungen, zum Schweregrad usw. Wenn Sie ein Element in der Liste auswählen, z. B. **Risikoanmeldung**, können Sie die Richtlinie bearbeiten. Wählen Sie unten auf der Seite **Abbrechen** aus.

1. Wählen Sie im linken Navigationsbereich **Warnungen** aus.  Wenn Warnungen aufgelistet werden, wählen Sie ein Element aus der Liste der Warnungen aus. Gehen Sie die bereitgestellten Informationen durch.  Wählen Sie in der oberen rechten Seite des Fensters **Warnung schließen** aus, um die Optionen zum Schließen der Warnung anzuzeigen.  

1. Schließen Sie alle geöffneten Browserregisterkarten.

### <a name="review"></a>Überprüfung

In diesem Lab haben Sie die Funktionen von Microsoft Defender für Cloud-Apps erkundet.  Sie sind die im Cloud Discovery-Dashboard verfügbaren Informationen und die verfügbaren Funktionen zum Untersuchen von Ergebnissen und zum Steuern der Auswirkung auf Ihre Organisation durch Richtlinien durchgegangen.
