---
demo:
  title: 'Azure Policy'
  module: 'Modul 6: Beschreiben der Ressourcengovernancefunktionen in Azure'
---


# <a name="demo-azure-policy"></a>Demo: Azure Policy

Diese Demo ist den folgenden Learn-Inhalten zugeordnet:

- Lernpfad: Beschreiben der Funktionen der Microsoft-Compliancelösungen
- Modul: Beschreiben der Ressourcengovernancefunktionen in Azure
- Lerneinheit: Beschreiben von Azure Policy

## <a name="demo-scenario"></a>Demoszenario

In dieser Demo durchlaufen Sie den Prozess der Einrichtung einer Azure-Richtlinie und lernen die Auswirkungen dieser Richtlinie kennen.

### <a name="demo-part-1"></a>Teil 1 der Demo

Erstellen einer Richtlinie, um ein Tag für eine Ressourcengruppe zu erfordern (es werden die Schritte zur Erstellung einer Richtlinie aus einer Vorlage gezeigt)

1. Öffnen Sie Microsoft Edge. Geben Sie **portal.azure.com** in die Adressleiste ein.  Sie sollten bereits angemeldet sein. Falls nicht, melden Sie sich mit Ihren Administratoranmeldeinformationen an.

1. Geben Sie in das Suchfeld, das sich auf dem blauen Balken oben auf der Seite neben dem Text „Microsoft Azure“ befindet, den Text **Richtlinie** ein, und wählen Sie dann **Richtlinie** aus den Suchergebnissen aus.

1. Sie befinden sich nun in der Übersicht der Seite „Richtlinie“. Beachten Sie die im Dashboard verfügbaren Informationen.

1. Wählen Sie im linken Navigationsbereich unter „Erstellung“ die Option **Zuweisungen** aus.  Sie sehen, dass bereits eine Richtlinienzuweisung vorhanden ist. Wählen Sie **ASC-Standard** aus.  Überprüfen Sie das Beschreibungsfeld. HINWEIS: Das Beschreibungsfeld verweist auf Azure Security Center, das in Microsoft Defender for Cloud umbenannt wurde.  Wählen Sie das **X** rechts oben auf der Seite aus, um zur Seite „Richtlinienzuweisungen“ zurückzukehren.

1. Wählen Sie oben auf der Seite **Richtlinie zuweisen** aus Der Assistent zum Zuweisen von Richtlinien wird geöffnet, um den Administrator durch den Prozess zum Zuweisen einer Richtlinie zu führen.

1. Sie beginnen auf der Registerkarte „Grundlagen“.
    1. Behalten Sie für den Bereich die Standardeinstellung bei. In diesem Fall ist der Bereich der Richtlinie das Azure-Abonnement, das vom autorisierten Lab-Hoster (ALH) bereitgestellt wird.
    1. Wählen Sie für die Richtliniendefinition die **Auslassungspunkte** aus.  Es wird eine Liste der verfügbaren Richtliniendefinitionen bereitgestellt.  Geben Sie in der Suchleiste **Tag erforderlich** ein. Wählen Sie in den Suchergebnissen **Tag für Ressourcengruppen erforderlich** aus (möglicherweise müssen Sie nach unten scrollen), und klicken Sie dann auf **Auswählen**.  Hinweis: Durch diese Richtlinie soll verhindert werden, dass neue Ressourcengruppen erstellt werden, welche die Anforderung nicht erfüllen.  
    1. Beachten Sie den standardmäßigen Zuweisungsnamen.  Behalten Sie den Namen unverändert bei.
    1. Stellen Sie sicher, dass „Richtlinienerzwingung“ auf **Aktiviert** festgelegt ist, und wählen Sie dann **Weiter** aus.

1. Sie befinden sich jetzt auf der Registerkarte „Parameter“. Geben Sie im Feld „Tagname“ die Angabe **Umgebung** ein, und wählen Sie dann **Weiter** aus.

1. Behalten Sie die Standardkorrektureinstellungen auf der Registerkarte „Wartung“ unverändert bei, und wählen Sie dann **Weiter** aus.

1. Sie befinden sich jetzt auf der Registerkarte „Nichtkonformitätsmeldungen“. Geben Sie im Feld „Nichtkonformitätsmeldung“ die Angabe **Umgebungstag ist erforderlich** ein, und wählen Sie dann **Weiter** aus. Hinweis: Diese Meldung wird als Grund für Nichtkonformität für Ressourcengruppen angezeigt, die vor der Richtlinienzuweisung erstellt wurden und das Umgebungstag nicht aufweisen.  

1. Überprüfen Sie die Richtlinienzuweisung, und wählen Sie dann **Erstellen** aus.  Wählen Sie **Aktualisieren** aus, falls die Richtlinie nicht sofort angezeigt wird. Hinweis: Es kann bis zu 30 Minuten dauern, bis die Richtlinie wirksam wird. In der Regel geschieht dies aber viel schneller.

1. Wählen Sie zum Schließen der Seite „Richtlinienzuweisungen“ das **X** in der oberen rechten Ecke des Bildschirms aus.

1. Sie befinden sich nun auf der Homepage der Azure-Dienste.  Lassen Sie diese Seite geöffnet. Sie benötigen sie für die nächste Aufgabe.

### <a name="demo-part-2"></a>Teil 2 der Demo

In dieser Aufgabe lernen Sie die Auswirkungen der Azure-Richtlinienzuweisung kennen, indem Sie versuchen, eine Ressourcengruppe in Azure zu erstellen, die kein Tag aufweist.

1. Öffnen Sie die Browserregisterkarte „Home – Microsoft Azure“.

1. Wählen Sie oben auf der Seite unterhalb von „Azure-Dienste“ die Option **Ressourcengruppen** aus.

1. Wählen Sie in der oberen linken Ecke der Seite **+ Erstellen** aus.

1. Lassen Sie auf der Registerkarte „Grundlagen“ des Dialogfelds „Ressourcengruppe erstellen“ das Feld „Abonnement“ unverändert.

1. Geben Sie in das Feld „Ressourcengruppe“ den Text **SC900-Labs** ein.

1. Übernehmen Sie den Standardwert der Einstellung „Region“, und klicken Sie auf **Weiter: Tags**.

1. Lassen Sie die Felder „Tagname“ und „Wert“ leer.  TRAGEN SIE NICHTS EIN, und wählen Sie dann **Überprüfen + erstellen** aus.

1. Es wird eine Meldung angezeigt, die besagt, dass die Validierung bestanden wurde („Tagname“ und „Wert“ sind keine Pflichtfelder im Assistenten). Wählen Sie dann **Erstellen** aus.

1. Am oberen Bildschirmrand wird die Fehlermeldung „Fehler beim Erstellen der Ressourcengruppe“ angezeigt. Wählen Sie **Fehlerdetails anzeigen** aus. Die Bedingung, die Teil der Azure-Richtlinie ist, wurde nicht erfüllt. Daher wurde die Erstellung der Ressourcengruppe aufgrund von Nichtkonformität blockiert. Hinweis: Wenn die Fehlermeldung nicht angezeigt wird und die Ressourcengruppe erstellt wurde, ist die Richtlinie noch nicht wirksam.  Navigieren Sie zum Aufrufen der in der vorherigen Aufgabe erstellten Richtlinie zur Seite „Richtlinie“. Sobald die Richtlinie wirksam ist, werden Sie feststellen, dass die Ressource nicht konform ist.  Die Detailseite umfasst die Meldung über die Nichtkonformität.

1. Die Fehlerzusammenfassung zeigt den Fehlertyp „Die Ressource ‚SC900-Labs‘ wurde durch eine Richtlinie abgelehnt“.  Schließen Sie dieses Fenster. Wählen Sie dazu in der oberen linken Ecke des Bildschirms das **X** aus.

1. Wählen Sie im Fenster „Ressourcengruppe erstellen“ die Option  **Zurück** aus.

1. Sie sind zurück auf der Seite „Tags“ für „Ressourcengruppe erstellen“.  Geben Sie in das Feld „Name“ den Text „Umgebung“ und in das Feld „Wert“ den Text **SC900-Labs** ein. Wählen Sie anschließend **Weiter: Überprüfen + erstellen >** aus.

1. Überprüfen Sie das Tag, und wählen Sie **Erstellen** aus.

1. Geben Sie in das Feld „Name“ den Namen **Umgebung** und in das Feld Wert **Labs** ein (dieser Wert kann beliebig sein, die Richtlinie verlangt lediglich einen Tagwert), und wählen Sie **Weiter: Überprüfen und erstellen** und dann **Erstellen** aus.

1. Die Ressourcengruppe wird aufgelistet.  

1. Weisen Sie die Lernenden darauf hin, dass eine Ressourcengruppe, die vor der Richtlinie erstellt wurde, nun als nicht konform mit dieser Richtlinienzuweisung angezeigt wird und durch die Anwendung des Umgebungstags korrigiert werden muss.  Es gibt eine bereits vorhandene Ressourcengruppe mit der Bezeichnung ResourceGroup1, die nicht konform ist und korrigiert werden kann, aber die Zeit bis zur Aktualisierung des Status nach der Korrektur ist länger als normal für die Lab-Umgebung.

### <a name="review"></a>Überprüfung

In dieser Demo haben Sie den Prozess der Einrichtung einer Azure-Richtlinie und die Auswirkungen dieser Richtlinie gezeigt.
