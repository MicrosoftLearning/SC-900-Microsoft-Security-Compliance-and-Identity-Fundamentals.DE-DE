---
ms.openlocfilehash: 8e34065623722f1f249c4da363aa862e46e49b0b
ms.sourcegitcommit: 15658ca1c7bae8a4dbaa33ab6f897070bde521b9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/12/2022
ms.locfileid: "147892148"
---
<a name="---"></a><!---
---
Lab: Title: 'Erkunden von Azure Policy' Learning Path/Module/Unit: 'Lernpfad: Beschreiben der Funktionen der Microsoft-Compliancelösungen; Modul 6: Beschreiben der Ressourcengovernancefunktionen in Azure; Lerneinheit 2: Beschreiben von Azure Policy'
---
--->

# <a name="lab-explore-azure-policy"></a>Lab: Umgehen mit Azure Policy

Dieses Lab ist den folgenden Learn-Inhalten zugeordnet:

- Lernpfad: Beschreiben der Funktionen der Microsoft-Compliancelösungen
- Modul: Beschreiben der Ressourcengovernancefunktionen in Azure
- Lerneinheit: Beschreiben von Azure Policy

## <a name="lab-scenario"></a>Labszenario

Azure Policy hilft bei der Durchsetzung von Organisationsstandards und bei der Bewertung der Compliance nach Bedarf. Azure Policy wertet Ressourcen in Azure aus, indem die Eigenschaften dieser Ressourcen mit Geschäftsregeln verglichen werden. In diesem Lab erkunden Sie zunächst die Landing Page von Azure Policy. Nach der anfänglichen Erkundung der Azure Policy-Seite erstellen Sie eine Richtlinie und erfahren, wie sich diese Richtlinie auswirkt.

**Geschätzte Dauer**: 20 bis 25 Minuten

### <a name="task-1"></a>Aufgabe 1

Erkunden Sie kurz die Azure Policy-Seite.

1. Öffnen Sie Microsoft Edge. Geben Sie **portal.azure.com** in die Adressleiste ein.

1. Melden Sie sich mit Ihren Administratoranmeldeinformationen an.
    1. Geben Sie **admin@WWLxZZZZZZ.onmicrosoft.com** (ZZZZZZ ist hierbei die eindeutige Mandanten-ID, die von Ihrem Labhostinganbieter bereitgestellt wurde) in das Fenster „Anmelden“ ein, und wählen Sie dann **Weiter** aus.

    1. Geben Sie das Administratorkennwort ein, das Sie vom Labhostinganbieter erhalten haben sollten. Wählen Sie **Anmelden**.
    1. Wählen Sie **Ja** aus, wenn Sie gefragt werden, ob Sie angemeldet bleiben möchten.

1. Sie befinden sich nun im Azure-Portal.  Geben Sie in das Suchfeld, das sich auf dem blauen Balken oben auf der Seite neben dem Text „Microsoft Azure“ befindet, den Text **Richtlinie** ein, und wählen Sie dann **Richtlinie** aus den Suchergebnissen aus. Dadurch wird die Azure Policy-Homepage geöffnet, die eine Dashboard-Ansicht bereitstellt.  Der Geltungsbereich, für den Informationen angezeigt werden, richtet sich nach dem im Rahmen dieses Labs verwendeten Azure Pass.   Beachten Sie die im Dashboard verfügbaren Informationen.

1. Es gibt ein Element namens „ASC-Standard“ (ASC bezieht sich auf Azure Security Center das jetzt Microsoft Defender für Cloud genannt wird), dessen Gültigkeitsbereich Azure Pass – Sponsorship ist.   Wählen Sie **ASC-Standard** aus.

1. Oben auf der Seite unter „Essentials“ werden der Name, die Beschreibung und andere wesentliche Informationen angezeigt.  Lesen Sie die Beschreibung (bewegen Sie den Mauszeiger über die Beschreibung). HINWEIS: Das Beschreibungsfeld verweist auf Azure Security Center, das in Microsoft Defender für Cloud umbenannt wurde.

1. Beachten Sie, dass die im Dashboard bereitgestellten Informationen entsprechend dem ausgewählten Element aktualisiert werden: ASC-Standard. Dieser ASC-Standard ist die Definition der Azure Security Benchmark-Initiative.  Wie Sie bereits erfahren haben, ist eine Initiativendefinition eine Sammlung von Richtliniendefinitionen, die auf das Erreichen eines einzigen übergeordneten Ziels ausgerichtet sind. Informationen können nach Gruppe, Richtlinien, nicht konformen Ressourcen oder Ereignissen angezeigt werden.

1. Schließen Sie die ASC-Seite, und kehren Sie zur Startseite der Richtlinie zurück, indem Sie oben rechts im Fenster **X** auswählen.

1. Wählen Sie im linken Navigationsbereich **Erste Schritte** aus.  Hier können Sie die verschiedenen Optionen anzeigen, einschließlich der Option zum Durchsuchen integrierter Richtlinien und zum Zuweisen von Richtlinien im großen Stil. Außerdem können Sie benutzerdefinierte Richtliniendefinitionen für Ihre Umgebung erstellen, Richtlinienzuweisungen empfehlen und vieles mehr.

1. Wählen Sie im linken Navigationsbereich **Compliance** aus.  Analog zur Übersichtsseite können Sie hier den Compliancezustand der aufgelisteten Richtlinien und/oder Initiativen anzeigen.  Auf der Seite „Richtlinienkompatibilität“ können Sie zudem eine Richtlinie oder Initiative zuweisen (in der nächsten Aufgabe weisen Sie eine Richtlinie zu).

1. Wählen Sie im linken Navigationsbereich **Wartung** aus.  Diese Seite umfasst eine Liste der Richtlinien, die über nicht-konforme Ressourcen verfügen.  Durch Auswahl einer Richtlinie auf der Seite „Wartung“ können Sie die Erstellung einer Aufgabe auslösen, um die Richtlinie zu korrigieren.  

1. Wählen Sie im linken Navigationsbereich unter „Erstellung“ die Option **Zuweisungen** aus.  Hier können Sie die aktuellen Richtlinien- und/oder Initiativenzuweisungen anzeigen und Richtlinienzuweisungen oder -initiativen erstellen.  Bei der nächsten Aufgabe werden Sie darauf zurückkommen.  

1. Wählen Sie im linken Navigationsbereich **Definitionen** aus.  Wählen Sie auf dieser Seite **Computer mit unsicheren Einstellungen zur Kennwortsicherheit überwachen** aus.  Dies ist eine Initiativendefinition, die viele Richtlinien umfasst.  Wählen Sie **Windows-Computer überwachen, die kein maximales Kennwortalter von 70 Tagen verwenden** aus, um zu erfahren, wie eine Richtliniendefinition aussieht.  Wenn die Seite geöffnet wird, wird die tatsächliche Richtliniendefinition in der JSON-Struktur (Java Script Object Notation) angezeigt.   Wie anhand des Texts in Rot zu sehen, enthält die Richtliniendefinition Elemente, die den Anzeigenamen, die Beschreibung, Parameter, Richtlinienregeln und mehr definieren. NEHMEN SIE KEINE ÄNDERUNGEN VOR.  

1. Wählen Sie zum Schließen der Seite „Richtliniendefinition“ das **X** in der oberen rechten Ecke der Seite aus.

1. Wählen Sie zum Schließen der Seite „Initiativendefinition“ das **X** in der oberen rechten Ecke der Seite aus.

1. Lassen Sie diese Browserregisterkarte („Richtlinie – Microsoft Azure“) für die nächste Aufgabe geöffnet.

### <a name="task-2"></a>Aufgabe 2

In dieser Aufgabe erstellen Sie eine einfache Richtlinienzuweisung, um eine Markierung für Ressourcengruppen zu erfordern.

1. Öffnen Sie die Browserregisterkarte „Richtlinie – Microsoft Azure“.

1. Wählen Sie im linken Navigationsbereich unter „Erstellung“ die Option **Zuweisungen** aus.

1. Wählen Sie oben auf der Seite **Richtlinie zuweisen** aus

1. Der Assistent zum Zuweisen von Richtlinien wird geöffnet, um den Administrator durch den Prozess zum Zuweisen einer Richtlinie zu führen.  Wählen Sie neben dem Feld „Richtliniendefinition“ die **Auslassungszeichen** aus.  Es wird eine Liste der verfügbaren Richtliniendefinitionen bereitgestellt.  

1. Geben Sie in der Suchleiste **Tag** ein.

1. Wählen Sie in den Suchergebnissen **Tag für Ressourcengruppen erforderlich** aus (möglicherweise müssen Sie nach unten scrollen), und klicken Sie dann auf **Auswählen**.  Hinweis: Durch diese Richtlinie soll verhindert werden, dass neue Ressourcengruppen erstellt werden, welche die Anforderung nicht erfüllen.  

1. Beachten Sie den standardmäßigen Zuweisungsnamen.  Übernehmen Sie den Namen unverändert, und wählen Sie unten auf der Seite **Weiter** aus.

1. Geben Sie im Feld „Name der Markierung“ den Text **Umgebung** ein, und wählen Sie dann **Weiter** aus.

1. Behalten Sie die Standardkorrektureinstellungen unverändert bei, und wählen Sie dann **Weiter** aus.

1. Geben Sie in der Meldung über die Nichtkonformität den Text **Umgebungstag erforderlich** ein, und wählen Sie dann **Weiter** aus. Hinweis: Diese Meldung wird als Grund für Nichtkonformität für Ressourcengruppen angezeigt, die vor der Richtlinienzuweisung erstellt wurden und das Umgebungstag nicht aufweisen.  Für nach der Erstellung der Richtlinie erstellte Ressourcengruppen wird das Erstellen der Ressourcengruppen verweigert, sofern kein Umgebungstag vorliegt.

1. Überprüfen Sie die Richtlinienzuweisung, und wählen Sie dann „Erstellen“ aus.  Wählen Sie **Aktualisieren** aus, falls die Richtlinie nicht sofort angezeigt wird. Hinweis: Es kann bis zu 30 Minuten dauern, bis die Richtlinie wirksam wird.

1. Wählen Sie zum Schließen der Seite „Richtlinienzuweisungen“ das **X** in der oberen rechten Ecke des Bildschirms aus.

1. Sie befinden sich nun auf der Homepage der Azure-Dienste.  Lassen Sie diese Seite geöffnet. Sie benötigen sie für die nächste Aufgabe.

### <a name="task-3"></a>Aufgabe 3

In dieser Aufgabe sehen Sie die Auswirkung der Azure-Richtlinienzuweisung. Dazu erstellen Sie eine Ressourcengruppe in Azure, die kein Tag enthält. Anschließend aktualisieren Sie die Ressourcengruppe so, dass sie ein Tag enthält.  Hinweis: Es kann bis zu 30 Minuten dauern, bis die in der vorherigen Aufgabe erstellte Richtlinie wirksam wird. In der Regel geht dies aber schneller.

1. Öffnen Sie die Browserregisterkarte „Home – Microsoft Azure“.

1. Wählen Sie oben auf der Seite unterhalb von „Azure-Dienste“ die Option **Ressourcengruppen** aus.

1. Wählen Sie in der oberen linken Ecke der Seite **+ Erstellen** aus.

1. Lassen Sie auf der Registerkarte „Grundlagen“ des Dialogfelds „Ressourcengruppe erstellen“ das Feld „Abonnement“ unverändert. Es lautet „Azure Pass-Förderung“.

1. Geben Sie in das Feld „Ressourcengruppe“ den Text **SC900-Labs** ein.

1. Übernehmen Sie den Standardwert der Einstellung „Region“, und klicken Sie auf **Weiter: Tags**.

1. Lassen Sie die Felder „Tagname“ und „Wert“ leer.  TRAGEN SIE NICHTS EIN, und wählen Sie dann **Überprüfen + erstellen** aus.

1. Es wird eine Meldung zur bestandenen Validierung angezeigt („Tagname“ und „Wert“ sind keine Pflichtfelder im Assistenten). Wählen Sie dann **Erstellen** aus.

1. Oben im Bildschirm wird die Fehlermeldung „Fehler beim Erstellen der Ressourcengruppe. Zeigen Sie die Fehlerdetails an“ angezeigt.  Wählen Sie **Fehlerdetails anzeigen** aus. Die Bedingung, die Teil der Azure-Richtlinie ist, wurde nicht erfüllt. Daher wurde die Erstellung der Ressourcengruppe aufgrund der Nichtkonformität blockiert.

    Hinweis: Wenn die Fehlermeldung nicht angezeigt wird und die Ressourcengruppe erstellt wurde, ist die Richtlinie noch nicht wirksam.  Navigieren Sie zum Aufrufen der in der vorherigen Aufgabe erstellten Richtlinie zur Seite „Richtlinie“. Sobald die Richtlinie wirksam ist, werden Sie feststellen, dass die Ressource nicht konform ist.  Die Detailseite umfasst die Meldung über die Nichtkonformität. Wenn ein Fehler zurückgegeben wird, zeigen Ihnen die folgenden Schritte, wie Sie die Bereitstellung korrigieren.

1. Die Fehlerzusammenfassung zeigt den Fehlertyp „Die Ressource ‚SC900-Labs‘ wurde durch eine Richtlinie abgelehnt“.  Schließen Sie dieses Fenster. Wählen Sie dazu in der oberen linken Ecke des Bildschirms das **X** aus.

1. Wählen Sie im Fenster „Ressourcengruppe erstellen“ die Option  **Zurück** aus.

1. Sie sind zurück auf der Seite mit den Tags für „Ressourcengruppe erstellen“.  Geben Sie in das Feld „Name“ den Text „Umgebung“ und in das Feld „Wert“ den Text **SC900-Labs** ein. Wählen Sie anschließend **Weiter: Überprüfen + erstellen >** aus.

1. Überprüfen Sie das Tag, und wählen Sie **Erstellen** aus.

1. Die Ressourcengruppe wird aufgelistet.  Da das Tag in der Ressourcengruppe bereitgestellt wurde, wurde die im Rahmen der Azure-Richtlinie enthaltene Bedingung erfüllt.  Die Ressourcengruppe ist mit der Richtlinie konform.

1. Entfernen Sie die Azure-Richtlinie, bevor Sie den Vorgang beenden.
    1. Wählen Sie in der oberen linken Ecke der Seite die Option „Start“ aus, um zur Azure-Homepage zurückzukehren.

    1. Wählen Sie unter „Azure-Dienste“ die Option „Azure Policy“ aus.
    1. In der Mitte der Seite wird eine Liste der Azure-Richtlinien-/-Initiativenzuweisungen angezeigt.  Wählen Sie die Auslassungspunkte für die Richtlinienzuweisung „Tag für Ressourcengruppen erforderlich“ und dann „Zuweisung löschen“ aus.
    1. Sie werden aufgefordert zu bestätigen, dass die Zuweisung gelöscht werden soll.  Wählen Sie Ja aus.

1. Schließen Sie alle geöffneten Browserregisterkarten.

### <a name="review"></a>Überprüfung

In diesem Lab haben Sie die Landing Page von Azure Policy kennengelernt. Nach der anfänglichen Erkundung der Azure Policy-Seite haben Sie den Prozess der Erstellung einer Richtlinie durchlaufen und konnten die Auswirkung dieser Richtlinie beobachten.
