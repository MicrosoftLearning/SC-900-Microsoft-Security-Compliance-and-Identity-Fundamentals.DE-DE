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

Azure Policy hilft bei der Durchsetzung von Organisationsstandards und bei der Bewertung der Compliance nach Bedarf. Azure Policy wertet Ressourcen in Azure aus, indem die Eigenschaften dieser Ressourcen mit Geschäftsregeln verglichen werden. In diesem Lab erstellen Sie eine Richtlinie und sehen sich die Auswirkungen dieser Richtlinie an.  Außerdem erhalten Sie Informationen zu Compliance und Wartung, die auf der Richtlinienseite verfügbar sind.

**Geschätzte Dauer**: 15 bis 20 Minuten

### <a name="task-1"></a>Aufgabe 1

In dieser Aufgabe erstellen Sie eine einfache Richtlinienzuweisung, die ein Tag für eine Ressourcengruppe erfordert.
1.  Öffnen Sie Microsoft Edge. Geben Sie **portal.azure.com** in die Adressleiste ein.

1. Melden Sie sich mit Administratoranmeldeinformationen für Ihr Azure-Abonnement an (diese Administratoranmeldeinformationen unterscheiden sich von den Microsoft 365-Administratoranmeldeinformationen).
    1. Geben Sie **User1-XXXXXXXX@LODSPRODMSLEARNMCA.onmicrosoft.com** (XXXXXXXX ist hierbei die eindeutige Mandanten-ID, die von Ihrem Lab-Hostinganbieter bereitgestellt wurde) in das Anmeldefenster ein, und wählen Sie dann **Weiter** aus.

    1. Geben Sie das Administratorkennwort ein, das von Ihrem Lab-Hostinganbieter bereitgestellt wird. Wählen Sie **Anmelden**.
    1. Wählen Sie **Ja** aus, wenn Sie gefragt werden, ob Sie angemeldet bleiben möchten.

1. Sie befinden sich nun im Azure-Portal.  Geben Sie in das Suchfeld, das sich auf dem blauen Balken oben auf der Seite neben dem Text „Microsoft Azure“ befindet, den Text **Richtlinie** ein, und wählen Sie dann **Richtlinie** aus den Suchergebnissen aus. Dadurch wird die Azure Policy-Homepage geöffnet, die eine Dashboardansicht bereitstellt.  Der Bereich für die Dashboardansicht ist das Azure-Abonnement, das vom autorisierten Lab-Hoster (ALH) bereitgestellt wird. Es wird eine Richtlinie aufgeführt, die vom ALH für die Verwendung des Azure-Abonnements erstellt wurde.

1. Wählen Sie im linken Navigationsbereich unter „Erstellung“ die Option **Zuweisungen** aus.

1. Wählen Sie oben auf der Seite **Richtlinie zuweisen** aus Der Assistent zum Zuweisen von Richtlinien wird geöffnet, um den Administrator durch den Prozess des Zuweisens einer Richtlinie zu führen.

1. Sie beginnen auf der Registerkarte „Grundlagen“.
    1. Behalten Sie für den Bereich die Standardeinstellung bei. In diesem Fall ist der Bereich der Richtlinie das Azure-Abonnement, das vom autorisierten Lab-Hoster (ALH) bereitgestellt wird.
    1. Wählen Sie für die Richtliniendefinition die **Auslassungspunkte** aus.  Es wird eine Liste der verfügbaren Richtliniendefinitionen bereitgestellt.  Geben Sie in der Suchleiste **Tag erforderlich** ein. Wählen Sie in den Suchergebnissen **Tag für Ressourcengruppen erforderlich** aus (möglicherweise müssen Sie nach unten scrollen), und drücken Sie dann auf **Auswählen**.  Hinweis: Durch diese Richtlinie soll verhindert werden, dass neue Ressourcengruppen erstellt werden, welche die Anforderung nicht erfüllen.  
    1. Beachten Sie den standardmäßigen Zuweisungsnamen.  Behalten Sie den Namen unverändert bei.
    1. Stellen Sie sicher, dass die Richtlinienerzwingung auf **Aktiviert** festgelegt ist.

1. Wählen Sie **Weiter** und dann erneut **Weiter** aus, um zur Registerkarte „Parameter“ zu wechseln (Sie hätten direkt die Registerkarte „Parameter“ auch direkt auswählen können).

1. Sie befinden sich jetzt auf der Registerkarte „Parameter“. Geben Sie im Feld „Tagname“ die Angabe **Umgebung** ein, und wählen Sie dann **Weiter** aus.

1. Behalten Sie die Standardkorrektureinstellungen auf der Registerkarte „Wartung“ unverändert bei, und wählen Sie dann **Weiter** aus.

1. Sie befinden sich jetzt auf der Registerkarte „Nichtkonformitätsmeldungen“. Geben Sie im Feld „Nichtkonformitätsmeldung“ die Angabe **Umgebungstag ist erforderlich** ein, und wählen Sie dann **Weiter** aus. Hinweis: Diese Meldung wird als Grund für Nichtkonformität für Ressourcengruppen angezeigt, die vor der Richtlinienzuweisung erstellt wurden und das Umgebungstag nicht aufweisen.

1. Überprüfen Sie die Richtlinienzuweisung, und wählen Sie dann **Erstellen** aus.  Wählen Sie **Aktualisieren** aus, falls die Richtlinie nicht sofort angezeigt wird. Hinweis: Es kann bis zu 30 Minuten dauern, bis die Richtlinie wirksam wird. In der Regel geschieht dies aber viel schneller.

1. Wählen Sie zum Schließen der Seite „Richtlinienzuweisungen“ das **X** in der oberen rechten Ecke des Bildschirms aus.

1. Sie befinden sich nun auf der Homepage der Azure-Dienste.  Lassen Sie diese Seite geöffnet. Sie benötigen sie für die nächste Aufgabe.

### <a name="task-2"></a>Aufgabe 2

In dieser Aufgabe lernen Sie die Auswirkungen der Azure-Richtlinienzuweisung kennen, indem Sie versuchen, eine Ressourcengruppe in Azure zu erstellen, die kein Tag aufweist.

1. Öffnen Sie die Browserregisterkarte „Home – Microsoft Azure“.

1. Wählen Sie oben auf der Seite unterhalb von „Azure-Dienste“ die Option **Ressourcengruppen** aus.

1. Wählen Sie in der oberen linken Ecke der Seite **+ Erstellen** aus.

1. Lassen Sie auf der Registerkarte „Grundlagen“ des Dialogfelds „Ressourcengruppe erstellen“ das Feld „Abonnement“ unverändert.

1. Geben Sie in das Feld „Ressourcengruppe“ den Text **SC900-Labs** ein.

1. Übernehmen Sie den Standardwert der Einstellung „Region“, und klicken Sie auf **Weiter: Tags**.

1. Lassen Sie die Felder „Tagname“ und „Wert“ leer.  TRAGEN SIE NICHTS EIN, und wählen Sie dann **Überprüfen + erstellen** aus.

1. Es wird eine Meldung zur bestandenen Validierung angezeigt („Tagname“ und „Wert“ sind keine Pflichtfelder im Assistenten). Wählen Sie dann **Erstellen** aus.

1. Am oberen Bildschirmrand wird die Fehlermeldung „Fehler beim Erstellen der Ressourcengruppe“ angezeigt. Wählen Sie **Fehlerdetails anzeigen** aus. Die Bedingung, die Teil der Azure-Richtlinie ist, wurde nicht erfüllt. Daher wurde die Erstellung der Ressourcengruppe aufgrund von Nichtkonformität blockiert. Hinweis: Wenn die Fehlermeldung nicht angezeigt wird und die Ressourcengruppe erstellt wurde, ist die Richtlinie noch nicht wirksam.  Navigieren Sie zum Aufrufen der in der vorherigen Aufgabe erstellten Richtlinie zur Seite „Richtlinie“. Sobald die Richtlinie wirksam ist, werden Sie feststellen, dass die Ressource nicht konform ist.  Die Detailseite umfasst die Meldung über die Nichtkonformität.

1. Die Fehlerzusammenfassung zeigt den Fehlertyp „Die Ressource ‚SC900-Labs‘ wurde durch eine Richtlinie abgelehnt“.  Schließen Sie dieses Fenster. Wählen Sie dazu in der oberen linken Ecke des Bildschirms das **X** aus.

1. Wählen Sie im Fenster „Ressourcengruppe erstellen“ die Option  **Zurück** aus.

1. Sie sind zurück auf der Seite „Tags“ für „Ressourcengruppe erstellen“.  Geben Sie in das Feld „Name“ den Text „Umgebung“ und in das Feld „Wert“ den Text **SC900-Labs** ein. Wählen Sie anschließend **Weiter: Überprüfen + erstellen >** aus.

1. Überprüfen Sie das Tag, und wählen Sie **Erstellen** aus.

1. Geben Sie in das Feld „Name“ den Namen **Umgebung** und in das Feld Wert **Labs** ein (dieser Wert kann beliebig sein, die Richtlinie verlangt lediglich einen Tagwert), und wählen Sie **Weiter: Überprüfen und erstellen** und dann **Erstellen** aus.

1. Die Ressourcengruppe wird aufgelistet.  

1. Wählen Sie **Start** auf der Adressleiste oben auf der Seite aus, um zur Azure-Homepage zurückzukehren.

1. Lassen Sie die Browserregisterkarte geöffnet, sie wird für die nächste Aufgabe benötigt.

### <a name="task-3-optional"></a>Aufgabe 3 (optional)

In dieser Aufgabe führen Sie die Schritte zum Warten einer nicht konformen Ressourcengruppe durch. HINWEIS: Bei dem für die Übung verwendeten Azure-Abonnement kommt es zu einer längeren als der normalen Verzögerung bei der Aktualisierung des Konformitätsstatus einer gewarteten Ressourcengruppe.

1. Wählen Sie auf der Azure-Homepage die Option **Richtlinie** aus. Dadurch wird die Azure Policy-Homepage geöffnet, die eine Dashboardansicht bereitstellt.  Der Bereich für die Dashboardansicht ist das Azure-Abonnement, das vom autorisierten Lab-Hoster bereitgestellt wird.  

1. Die Richtlinie sollte angezeigt werden, die Sie zuvor erstellt haben. Wählen Sie sie aus.

1. Oben auf der Seite unter „Essentials“ werden der Name, die Beschreibung und andere wesentliche Informationen angezeigt.  Beachten Sie, dass die Richtlinie als nicht konform angezeigt wird.  Wählen Sie die Richtlinie aus, um weitere Informationen dazu zu erhalten, warum die Richtlinie nicht konform ist. Hier sehen Sie, dass eine Ressource, die als „resourgegroup1“ aufgeführt wird, nicht konform ist.  Dies ist ein Beispiel für eine Ressourcengruppe, die vor der Erstellung der Richtlinie erstellt wurde. Wählen Sie **Details** aus, um weitere Informationen zu erhalten.  Hier sehen Sie die Konformitätsmeldung, dass ein Umgebungstag erforderlich ist.  Wählen Sie das **X** oben rechts aus, um das Fenster zu schließen.

1. Wählen Sie **resourcegroup1** aus, und wählen Sie dann oben auf der Seite **Ressource anzeigen** aus.
    1. Wählen Sie neben „Tags“ die Option **Bearbeiten** aus.
    1. Platzieren Sie den Mauszeiger im Feld „Tag“, und wählen Sie **Umgebung** aus.
    1. Platzieren Sie den Mauszeiger im Feld „Wert“, und wählen Sie **Labs** und dann **Speichern** aus.

1. Kehren Sie nun zur Richtlinienseite zurück.  Platzieren Sie den Mauszeiger auf dem blauen Suchfeld oben auf der Seite, und wählen Sie **Richtlinie** aus.

1. Wählen Sie im linken Navigationsbereich **Compliance** aus.  Analog zur Übersichtsseite können Sie hier den Compliancezustand der aufgelisteten Richtlinien und/oder Initiativen anzeigen.  HINWEIS: Obwohl Sie das Tag der Ressourcengruppe hinzugefügt haben, dauert es einige Zeit, bis der Status aktualisiert wird.  Für Azure-Abonnements, die für Lab-Zwecke verwendet werden, können Verzögerungen auftreten, die länger als normal sind. Wenn Sie warten möchten, bis der Konformitätsstatus für diese Ressource aktualisiert wurde, beenden Sie das Lab nicht. Je nach Lab-Umgebung kann die Aktualisierung eine Stunde oder länger dauern.  

### <a name="review"></a>Überprüfung

In diesem Lab haben Sie den Prozess zum Erstellen einer Azure-Richtlinienzuweisung durchlaufen und die Auswirkungen dieser Richtlinie erkennen können.
