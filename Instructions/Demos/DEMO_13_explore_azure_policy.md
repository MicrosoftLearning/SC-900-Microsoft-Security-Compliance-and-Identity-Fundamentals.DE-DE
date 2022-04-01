---
Demo:
  title: Azure Policy
  module: 'Module 4 Lesson 5: Describe the capabilities of Microsoft compliance solutions: Describe Azure Policy'
ms.openlocfilehash: 898e2d2ae228baf6acbffd7301fcbdf4a6a2dba5
ms.sourcegitcommit: a341c2fc38e9b37dafb792d82e3c948f7ba4a099
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/14/2022
ms.locfileid: "137894070"
---
# <a name="demo-azure-policy"></a>Demo: Azure Policy

### <a name="demo-scenario"></a>Demoszenario
In dieser Demo gehen Sie den Prozess der Einrichtung einer Azure-Richtlinie und die Auswirkungen dieser Richtlinie durch.

#### <a name="demo-part-1-create-a-policy-to-require-a-tag-on-a-resource-group-shows-steps-to-create-a-policy-from-a-template"></a>Teil 1 der Demo: Erstellen einer Richtlinie, um ein Tag für eine Ressourcengruppe zu erfordern (es werden die Schritte zur Erstellung einer Richtlinie aus einer Vorlage gezeigt)

1. Öffnen Sie Microsoft Edge. Geben Sie **portal.microsoft.com** in die Adressleiste ein.  Sie sollten bereits angemeldet sein. Falls nicht, melden Sie sich mit Ihren Administratoranmeldeinformationen an.

1. Geben Sie in das Suchfeld, das sich auf dem blauen Balken oben auf der Seite neben dem Text „Microsoft Azure“ befindet, den Text **Richtlinie** ein, und wählen Sie dann **Richtlinie** aus den Suchergebnissen aus.

1. Sie befinden sich nun auf der Seite „Richtlinie“. Beachten Sie die im Dashboard verfügbaren Informationen.

1. Wählen Sie im linken Navigationsbereich unter „Erstellung“ die Option **Zuweisungen** aus.  Sie sehen, dass bereits eine Richtlinienzuweisung vorhanden ist. Wählen Sie **ASC-Standard** aus.  Überprüfen Sie das Beschreibungsfeld. HINWEIS: Das Beschreibungsfeld verweist auf Azure Security Center, das in Microsoft Defender für Cloud umbenannt wurde.  Wählen Sie das **X** rechts oben auf der Seite aus, um zur Seite „Richtlinienzuweisungen“ zurückzukehren.

1. Wählen Sie oben auf der Seite **Richtlinie zuweisen** aus

1. Der Assistent zum Zuweisen von Richtlinien wird geöffnet, um den Administrator durch den Prozess zum Zuweisen einer Richtlinie zu führen.  Wählen Sie neben dem Feld „Richtliniendefinition“ die **Auslassungszeichen** aus.  Es wird eine Liste der verfügbaren Richtliniendefinitionen bereitgestellt.  

1. Geben Sie in der Suchleiste **Tag** ein.

1. Wählen Sie in den Suchergebnissen **Tag für Ressourcengruppen erforderlich** aus (möglicherweise müssen Sie nach unten scrollen), und klicken Sie dann auf **Auswählen**.  Hinweis: Durch diese Richtlinie soll verhindert werden, dass neue Ressourcengruppen erstellt werden, welche die Anforderung nicht erfüllen.  

1. Beachten Sie den standardmäßigen Zuweisungsnamen.  Übernehmen Sie den Namen unverändert, und wählen Sie unten auf der Seite **Weiter** aus.

1. Geben Sie im Feld „Name der Markierung“ den Text **Umgebung** ein (für Ressourcengruppen wird eine Umgebungsmarkierung verlangt), und wählen Sie dann **Weiter** aus.  

1. Lesen Sie auf der Registerkarte „Wartung“ die Beschreibung, aber ändern Sie die Einstellungen nicht. Wählen Sie **Weiter** aus.

1. Geben Sie in der Meldung über die Nichtkonformität den Text **Umgebungstag erforderlich** ein, und wählen Sie dann **Weiter** aus. Hinweis: Diese Meldung wird als Grund für Nichtkonformität für Ressourcengruppen angezeigt, die vor der Richtlinienzuweisung erstellt wurden und das Umgebungstag nicht aufweisen.  Für nach der Erstellung der Richtlinie erstellte Ressourcengruppen wird das Erstellen der Ressourcengruppen verweigert, sofern kein Umgebungstag vorliegt.

1. Überprüfen Sie die Richtlinienzuweisung, und wählen Sie dann „Erstellen“ aus.  Wählen Sie **Aktualisieren** aus, falls die Richtlinie nicht sofort angezeigt wird. Hinweis: Es kann bis zu 30 Minuten dauern, bis die Richtlinie wirksam wird.

1. Wählen Sie zum Schließen der Seite „Richtlinienzuweisungen“ das **X** in der oberen rechten Ecke des Bildschirms aus.

1. Sie befinden sich nun auf der Homepage der Azure-Dienste.  Lassen Sie diese Seite geöffnet. Sie benötigen sie für die nächste Aufgabe.

#### <a name="demo-part-2--show-the-impact-of-the-policy-by-creating-a-resource-group-without-a-tag-then-fix-it-to-have-a-tag"></a>Teil 2 der Demo:  Zeigen Sie die Auswirkungen der Richtlinie. Erstellen Sie dazu eine Ressourcengruppe ohne Markierung, und fügen Sie dieser dann eine Markierung hinzu.

1. Wählen Sie oben auf der Seite unterhalb von „Azure-Dienste“ die Option **Ressourcengruppen** aus. Wenn die Option nicht angezeigt wird, geben Sie in die Suchleiste „Ressourcengruppen“ ein, und wählen Sie den Eintrag dann aus.

1. Wählen Sie in der oberen linken Ecke der Seite **+ Erstellen** aus.

1. Lassen Sie auf der Registerkarte „Grundlagen“ des Dialogfelds „Ressourcengruppe erstellen“ das Feld „Abonnement“ unverändert. Es lautet „Azure Pass-Förderung“.

1. Geben Sie in das Feld „Ressourcengruppe“ den Text **SC900-Labs** ein.

1. Übernehmen Sie den Standardwert der Einstellung „Region“, und klicken Sie auf **Weiter: Tags**.

1. Lassen Sie die Felder „Tagname“ und „Wert“ leer.  TRAGEN SIE NICHTS EIN, und wählen Sie dann **Überprüfen + erstellen** aus.

1. Es wird eine Meldung zur bestandenen Validierung angezeigt („Tagname“ und „Wert“ sind keine Pflichtfelder im Assistenten). Wählen Sie dann **Erstellen** aus.

1. Oben im Bildschirm wird die Fehlermeldung „Fehler beim Erstellen der Ressourcengruppe. Zeigen Sie die Fehlerdetails an“ angezeigt.  Wählen Sie **Fehlerdetails anzeigen** aus. Die Bedingung, die Teil der Azure-Richtlinie ist, wurde nicht erfüllt. Daher wurde die Erstellung der Ressourcengruppe aufgrund der Nichtkonformität blockiert. Hinweis: Wenn die Fehlermeldung nicht angezeigt wird und die Ressourcengruppe erstellt wurde, ist die Richtlinie noch nicht wirksam.  Navigieren Sie zum Aufrufen der in der vorherigen Aufgabe erstellten Richtlinie zur Seite „Richtlinie“. Sobald die Richtlinie wirksam ist, werden Sie feststellen, dass die Ressource nicht konform ist.  Die Detailseite umfasst die Meldung über die Nichtkonformität.

1. Die Fehlerzusammenfassung zeigt den Fehlertyp „Die Ressource ‚SC900-Labs‘ wurde durch eine Richtlinie abgelehnt“.  Schließen Sie dieses Fenster. Wählen Sie dazu in der oberen linken Ecke des Bildschirms das **X** aus.

1. Wählen Sie im Fenster „Ressourcengruppe erstellen“ die Option **< Vorherige** aus.

1. Sie sind zurück auf der Seite mit den Tags für „Ressourcengruppe erstellen“.  Geben Sie in das Feld „Name“ den Text „Umgebung“ und in das Feld „Wert“ den Text **SC900-Labs** ein. Wählen Sie anschließend **Weiter: Überprüfen + erstellen >** aus.

1. Überprüfen Sie das Tag, und wählen Sie **Erstellen** aus.

1. Die Ressourcengruppe wird aufgelistet.  Da das Tag in der Ressourcengruppe bereitgestellt wurde, wurde die im Rahmen der Azure-Richtlinie enthaltene Bedingung erfüllt.  Die Ressourcengruppe ist mit der Richtlinie konform.

#### <a name="review"></a>Überprüfung

In dieser Demo haben Sie den Prozess der Einrichtung einer Azure-Richtlinie und die Auswirkungen dieser Richtlinie gezeigt.
