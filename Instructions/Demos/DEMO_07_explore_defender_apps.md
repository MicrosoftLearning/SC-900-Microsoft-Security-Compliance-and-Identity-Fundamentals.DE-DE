---
ms.openlocfilehash: 2ea64f800931ec99ace8cd3ec349573a0931899e
ms.sourcegitcommit: 15658ca1c7bae8a4dbaa33ab6f897070bde521b9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/12/2022
ms.locfileid: "147892616"
---
<a name="---"></a><!---
---
Demo: Title: 'Microsoft Defender für Cloud-Apps' Module: 'Lernpfad: Beschreiben der Funktionen von Microsoft-Sicherheitslösungen; Modul 4: Beschreiben der Bedrohungsschutzfunktionen von Microsoft 365; Lerneinheit 5: Beschreiben von Microsoft Defender für Cloud-Apps'
---
--->

# <a name="demo-microsoft-defender-for-cloud-apps"></a>Demo: Microsoft Defender für Cloud-Apps

Diese Demo ist den folgenden Learn-Inhalten zugeordnet:

- Lernpfad: Beschreiben der Funktionen von Microsoft-Sicherheitslösungen
- Modul: Beschreiben der Bedrohungsschutzfunktionen von Microsoft 365
- Lerneinheit: Beschreiben von Microsoft Defender für Cloud-Apps

## <a name="demo-scenario"></a>Demoszenario

In dieser Demo zeigen Sie die Funktionen von Microsoft Defender für Cloud-Apps.  Sie führen den Kursteilnehmer durch die im Cloud Discovery-Dashboard verfügbaren Informationen und die verfügbaren Funktionen zum Untersuchen von Ergebnissen und zum Steuern der Auswirkung auf Ihre Organisation durch Richtlinien.  Hinweis:  Eine Organisation muss über eine Lizenz verfügen, um Microsoft Defender für Cloud-Apps verwenden zu können, wobei es sich um einen benutzerbasierten Abonnementdienst handelt.  

### <a name="demo-part-1-explore-cloud-discovery"></a>Teil 1 der Demo: Erkunden der Cloud Discovery

1. Öffnen Sie Microsoft Edge. Geben Sie **admin.microsoft.com** in die Adressleiste ein.  Sie sollten bereits als Administrator angemeldet sein.  Falls nicht, melden Sie sich mit Ihren Administratoranmeldeinformationen an.

1. Wählen Sie im linken Navigationsbereich von Microsoft 365 Admin Center **Alle anzeigen** aus.  Äußern Sie sich zum Punkt, dass der Zugriff auf die unterschiedlichen Microsoft 365 Admin Centers von hier aus möglich ist.

1. Wählen Sie **Sicherheit** unter „Admin Center“ aus.  Die Startseite des Microsoft 365 Defender-Portals wird auf einer neuen Browserseite geöffnet.  

1. Wenn Sie das Microsoft 365 Defender-Portal das erste Mal besuchen, wird möglicherweise ein Popupfenster für eine Schnelleinführung angezeigt.  Schließen Sie es.

1. Wählen Sie unten im linken Navigationsbereich der Seite „Microsoft 365 Defender“ die Option **Weitere Ressourcen** aus.

1. Wählen Sie auf der Karte **Microsoft Defender für Cloud-Apps** die Option **Öffnen** aus.  Das Cloud App Security-Dashboard wird auf einer neuen Browserseite geöffnet.  Beachten Sie die verfügbaren Informationskarten.  Es kann sein, dass auf den Karten keine Informationen angezeigt werden, da es sich hierbei um eine vorkonfigurierte Labmandantenumgebung handelt, die nicht aktiv verwendet wurde.  

1. Wählen Sie im linken Navigationsbereich **Ermitteln** aus. Wählen Sie dann im Dropdown das Dashboard **Cloud Discovery** aus.  Das Dashboard enthält eine Übersicht der ermittelten Apps, App-Kategorien, Risikostufen und mehr.  

    1. Wählen Sie oben auf der Seite „Cloud Discovery“ die Registerkarte **Ermittelte Apps** aus.  Das Fenster „Ermittelte Apps“ enthält eine ausführliche Ansicht der ermittelten Apps, einschließlich der Risikobewertung, des Datenverkehrs, der Anzahl der Benutzer und mehr.

        1. Wählen Sie für ein beliebiges Element in der Liste die **Auslassungspunkte** in der Spalte der Aktion der Tabelle aus.  Beachten Sie die verschiedenen Optionen, die verfügbar sind, einschließlich der Funktion, mit der eine Apps als sanktioniert oder nicht sanktioniert markiert werden kann.  Wählen Sie die Auslassungspunkte erneut aus, um das Aktionsfeld zu schließen.

        1. Durch die Auswahl eines bestimmten Zeilenelements wird für die bestimmte App eine Detailseite geöffnet.  Wählen Sie ein Element in der Liste aus.  Gehen Sie für das ausgewählte Element jede Registerkarte durch, die sich oben auf der Detailseite befindet.  **Nutzung**, **Info, IP**, **Adressen**, **Benutzer** und **Benachrichtigungen**. Wenn Sie die Detailseite fertig erkundet haben, kehren Sie zu den ermittelten Apps zurück. Wählen Sie dazu im linken Navigationsbereich die Option **Ermittelte Apps** aus.

    1. Wählen Sie oben auf der Seite die Registerkarte **IP-Adressen** (dies entspricht der Auswahl der IP-Adressen über den linken Navigationsbereich) aus.  Hier finden Sie Daten, darunter die Anzahl der Transaktionen, das Aufkommen von Datenverkehr und Uploadmengen nach IP-Adressen.  Beachten Sie, dass Sie auch nach einer bestimmten IP-Adresse filtern oder die Daten zur weitergehenden Analyse exportieren können.

    1. Wählen Sie oben auf der Seite (oder über den linken Navigationsbereich) die Option **Benutzer** aus.  Dies ist derselbe Informationstyp, der bei der Auswahl von IP-Adressen bereitgestellt wird. Er wird jedoch für einzelne Benutzer aufgelistet.  Auch hier filtern Sie nach einem bestimmten Benutzer und exportieren die Daten zur weitergehenden Analyse.

1. Die auf diesen Registerkarten bereitgestellten Informationen basieren auf Momentaufnahmeberichten aus von Ihnen manuell aus Ihren Firewalls und Proxys hochgeladenen Datenverkehrsprotokollen oder aus fortlaufenden Berichten, die alle Protokolle analysieren, die aus Ihrem Netzwerk mithilfe von Cloud App Security weitergeleitet werden.  Wählen Sie in der oberen rechten Ecke der Seite die **Auslassungspunkte** aus, um zu erfahren, wo dies eingerichtet wird.

    1. Wählen Sie die erste Option **Momentaufnahmebericht zu Cloud Discovery erstellen** aus. Hier tragen Sie die erforderlichen Details ein und laden Datenverkehrsprotokolle hoch, um einen Bericht zu generieren und hochzuladen.  Klicken Sie auf **Abbrechen**.  Die für Ihren Labmandanten angezeigten Daten stammen aus einem Momentaufnahmebericht. Sie können diese Informationen in der oberen rechten Ecke des Bildschirms anzeigen.

    1. Wählen Sie zum Anzeigen der Option für fortlaufende Berichte die **Auslassungspunkte** in der oberen rechten Ecke der Seite aus, und wählen Sie im Dropdown den Eintrag **Automatischen Upload konfigurieren** aus.  Es sind keine Datenquellen verbunden. Hier würden Sie jedoch eine Datenquelle hinzufügen. Wählen Sie den Dropdownpfeil **Appliance auswählen** aus, um die Appliancetypen anzuzeigen, die als Datenquelle verbunden werden können.  Wählen Sie **Abbrechen** aus, um den Vorgang zu beenden.

1. Ein weiterer Punkt, auf den Sie hinweisen sollten, ist, dass Sie sich direkt mit Apps verbinden können, indem Sie App-Konnektoren einrichten, die Ihnen eine bessere Sichtbarkeit und Kontrolle über Ihre Cloud-Apps ermöglichen. Wählen Sie in der oberen linken Ecke des Bildschirms das **Zahnradsymbol für die Einstellungen** aus. Wählen Sie dann in der Dropdownliste den Eintrag **App-Connectors** aus.  

    1. Auf der Seite „Verbundene Apps“ sollte „Office 365“ in der Liste mit einem verbundenen Status angezeigt werden.  Wenn für Office 365 ein Verbindungsfehler angezeigt wird, liegt dies höchstwahrscheinlich daran, dass die Option für die Überwachung nicht aktiviert ist.

    1. Wählen Sie **+ App verbinden** aus. Wählen Sie dann in der Dropdownliste den Eintrag **Microsoft Azure** aus.  Wählen Sie im Microsoft Azure-Popupfenster **Mit Microsoft Azure verbinden** aus.  Sie sehen den Verbunden-Status und Informationen zum Scannen von Benutzern, Daten und Aktivitäten.  Klicken Sie auf die Schaltfläche **Schließen**.

1. Lassen Sie diese Seite geöffnet, da Sie sie in der nächsten Aufgabe verwenden werden.

### <a name="demo-part-2"></a>Teil 2 der Demo

Finden Sie Möglichkeiten, wie Sie die aufgezeichneten Aktivitäten untersuchen können.

1. Wählen Sie im linken Navigationsbereich unter **Untersuchen** die Option **Aktivitätsprotokoll** aus.  Hier können Sie alle Aktivitäten im Zusammenhang mit Ihren verbundenen Apps anzeigen.   Da der Office 365-Connector bereits verbunden ist, sollten einige Daten angezeigt werden. Nachdem Sie mithilfe des App-Connectors eine Verbindung zwischen Cloud App Security und einer App hergestellt haben, scannt Cloud App Security alle Aktivitäten, die durchgeführt wurden, wobei die rückwirkende Scanzeit je nach App abweicht, und wird anschließend ständig mit neuen Aktivitäten aktualisiert.  

1. Wählen Sie ein Element aus, um detailliertere Informationen anzuzeigen. Beachten Sie oben auf der Seite die Option, eine neue Richtlinie aus der Suche hinzuzufügen oder die Daten für weitere Analysen zu exportieren.  Wählen Sie **+Neue Richtlinie aus Suche** aus.  Beachten Sie, wie Sie eine Richtlinie anhand einer Vorlage erstellen, einen Schweregrad und die Kategorie der Richtlinie auswählen, Filter für die Richtlinie erstellen, Warnungen erstellen und sogar Warnungen an Power Automate senden können.  Wählen Sie **Abbrechen** aus, um das Fenster zur Richtlinienerstellung zu schließen.

1. Wählen Sie im linken Navigationsbereich die Option **Dateien** aus, und beachten Sie die Optionen zum Filtern von Daten, Erstellen einer Dateirichtlinie und Exportieren der Daten.  Wählen Sie die Option **Benutzer und Konten** aus, und erkunden Sie diese.  Beachten Sie die Optionen zum Filtern von Daten und Exportieren der Daten.

1. Wählen Sie im linken Navigationsbereich die Option „Sicherheitskonfiguration“ aus. Diese Seite umfasst Sicherheitskonfigurationsbewertungen für Ihre Azure-, Amazon Web Services- (AWS) und Google Cloud Platform-Konten (GCP).

1. Lassen Sie diese Seite geöffnet, da Sie sie in der nächsten Aufgabe verwenden werden.

### <a name="demo-part-3"></a>Teil 3 der Demo

In dieser Aufgabe erkunden Sie die Seiten mit den Richtlinien und Warnungen in Microsoft Defender für Cloud-Apps.

1. Wählen Sie im linken Navigationsbereich unter „Steuerung“ die Option **Richtlinien** aus.  Die aufgelisteten Richtlinien umfassen Informationen zur Anzahl der von der Richtlinie generierten Warnungen, zum Schweregrad usw. Durch Auswahl eines Elements werden ausführlichere Informationen zur Richtlinie angezeigt. Wählen Sie ein Element aus der Liste aus, beispielsweise **Riskante Anmeldung**.  

1. Wählen Sie im linken Navigationsbereich **Warnungen** aus.  Wenn Warnungen aufgelistet werden, wählen Sie ein Element aus der Liste der Warnungen aus. Gehen Sie die bereitgestellten Informationen durch.  Wählen Sie in der oberen rechten Seite des Fensters **Warnung schließen** aus, um die Optionen zum Schließen der Warnung anzuzeigen.  

1. Schließen Sie das Browserfenster.

### <a name="review"></a>Überprüfung

In dieser Demo haben Sie die Funktionen von Microsoft Defender für Cloud-Apps angezeigt.  Sie haben die im Cloud Discovery-Dashboard verfügbaren Informationen und die verfügbaren Funktionen zum Untersuchen von Ergebnissen und zum Steuern der Auswirkung auf Ihre Organisation durch Richtlinien gezeigt.
