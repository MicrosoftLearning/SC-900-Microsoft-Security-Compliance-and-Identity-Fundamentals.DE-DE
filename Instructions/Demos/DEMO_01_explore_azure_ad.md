<!---
---
Demo: Titel: Erkunden Microsoft Entra ID Benutzereinstellungen Lernpfad/Modul/Lerneinheit: Lernpfad: Beschreiben der Funktionen von Microsoft Entra; Modul 1: Beschreiben der Funktions- und Identitätstypen von Microsoft Entra ID; Lerneinheit 3: Beschreiben der Microsoft Entra Identitätstypen
---
--->

# Demo: Microsoft Entra ID-Benutzereinstellungen

Diese Demo ist den folgenden Learn-Inhalten zugeordnet:

- Lernpfad: Beschreiben der Funktionen von Microsoft Entra.
- Modul: Beschreibung der Funktion und Identitätstypen von Microsoft Entra ID.
- Lerneinheit: Beschreiben der Identitätstypen.

## Vorführungsszenario

In dieser Demo greifen Sie auf Microsoft Entra ID zu und gehen die verschiedenen Einstellungen für vorhandene Benutzer durch.

1. Öffnen Sie Microsoft Edge.

1. Geben Sie **admin.microsoft.com** in die Adressleiste ein, um auf Microsoft 365 Admin Center zuzugreifen.

1. Melden Sie sich mit Ihren Administratoranmeldeinformationen an.
    1. Geben Sie **admin@WWLxZZZZZZ.onmicrosoft.com** (ZZZZZZ ist hierbei die eindeutige Mandanten-ID, die von Ihrem Lab-Hostinganbieter bereitgestellt wurde) in das Anmeldefenster ein, und wählen Sie dann **Weiter** aus.
    1. Geben Sie das Administratorkennwort ein, das von Ihrem Lab-Hostinganbieter bereitgestellt werden sollte. Wählen Sie **Anmelden**.
    1. Wählen Sie **Ja** aus, wenn Sie gefragt werden, ob Sie angemeldet bleiben möchten.

1. Wählen Sie im linken Navigationsbereich von Microsoft 365 Admin Center **Alle anzeigen** aus.

1. Wählen Sie im Admin Center den Eintrag **Identität** aus (möglicherweise müssen Sie dazu nach unten scrollen).  Die Übersichtsseite des Microsoft Entra Admin Centers wird auf einer neuen Browserseite geöffnet. Hier sehen Sie grundlegende Informationen zu Ihrem Contoso-Mandanten. Wenn Sie im Hauptfenster nach unten scrollen, werden auch Informationen zu Warnungen, meinem Feed, Feature-Highlights und mehr angezeigt.  
    1. Hinweis an Referenten/Kursleiter: Sie können auch direkt auf das Microsoft Entra Admin Center zugreifen, indem Sie zu **[entra.microsoft.com](https://entra.microsoft.com)** wechseln.

1. Erweitern Sie im linken Navigationsbereich **Benutzer** und wählen Sie dann **Alle Benutzer** aus.  Auf der Benutzerseite werden zusätzliche Navigationsoptionen und die Liste der Benutzer angezeigt. Beachten Sie, dass bereits Benutzer für Ihren Mandanten konfiguriert sind.

1. Wählen Sie aus der Liste der Benutzer*innen **Adele Vance** aus.

1. Beachten Sie, dass im linken Navigationsbereich die **Übersicht** hellgrau hervorgehoben ist.  Zeigen Sie die Informationen auf der Übersichtsseite bzw. erläutern Sie diese.  Wählen Sie oben auf der Seite die Registerkarte **Überwachung** aus, auf der Benutzeranmeldungen angezeigt werden (es wird keine Anmeldung angezeigt, es sei denn, Sie haben sich zuvor als Adele Vance angemeldet).  Wählen Sie dann **Eigenschaften** aus, um alle Eigenschaften für das Adele Vance-Benutzerobjekt anzuzeigen.

1. Wählen Sie im linken Navigationsbereich **Zugewiesene Rollen** aus.  Diesem Benutzer sind keine Administratorrollen zugewiesen.  Wählen Sie oben auf der Seite **+ Zuweisungen hinzufügen** aus, und erweitern Sie dann auf der Seite Zuweisungen hinzufügen das Feld Rollensuche unter Rolle auswählen, um eine Liste der verfügbaren Verwaltungsrollentypen anzuzeigen.  Fügen Sie keine weiteren hinzu, schließen Sie die Seite, indem Sie das **X** oben rechts anklicken.

1. Wählen Sie im linken Navigationsbereich **Gruppen** aus.  Sprechen Sie die Tatsache an, dass diese(r) Benutzer*in Mitglied in mehreren Gruppen ist.  Hier können Sie die Arten von Gruppen ansprechen.  Um diesen Benutzer anderen Gruppen hinzuzufügen, würden Sie **+ Mitgliedschaften hinzufügen** auswählen.  Fügen Sie keine neuen Gruppen hinzu. Erwähnen Sie nur, wie einfach es ist, einen Benutzer vorhandenen Gruppen hinzuzufügen. Schließen Sie das Gruppenfenster mit dem **X** rechts oben auf der Seite.

1. Wählen Sie im linken Navigationsbereich **Lizenzen** aus. Beachten Sie, dass diesem Benutzer Microsoft 365 E5-Lizenzen und eine EMS-Lizenz zugewiesen sind.  Wenn Sie eine Lizenz hinzufügen möchten, klicken Sie oben im Hauptfenster auf **+ Zuweisungen**.  Zeigen Sie die Lizenzen für diese(n) Benutzer*in an. Ändern Sie NICHTS.  Schließen Sie dieses Fenster mit dem **X** oben rechts auf der Seite.

1. Wählen Sie im linken Navigationsbereich **Geräte** aus.  Nichts wird angezeigt, aber Sie können davon ausgehen, dass, wenn diesem Benutzer Geräte zugewiesen wären, dies an dieser Stelle angezeigt würde.

1. Wählen Sie im linken Navigationsbereich **Azure-Rollenzuweisungen** aus.  Aufruf:
    1. Diese Registerkarte ist nicht identisch mit der für zugewiesene Rollen, die zuvor gezeigt wurde, da die zuvor gezeigte Registerkarte für die rollenbasierte Zugriffssteuerung in Microsoft Entra gedacht ist.
    1. Obwohl hier nichts aufgeführt ist, ist dies die Registerkarte, auf der Sie Rollenzuweisungen für Azure-Ressourcen anzeigen können, die Adele zugewiesen sind. Wenn Sie beispielsweise eine Azure-Ressourcengruppe erstellen und Adele eine bestimmte Rolle zuweisen, z. B. Besitzerin oder Mitwirkende für die Ressourcengruppe, würden Sie diese Rolle hier sehen. Dies ist Teil der rollenbasierten Zugriffssteuerung in Azure (Azure RBAC). Diese Rollenzuweisung wird im Rahmen dieser konkreten Ressource verwaltet.

1. Wählen Sie im linken Navigationsbereich **Authentifizierungsmethoden** aus.  Rufen Sie die Beschreibung auf, die besagt: „Hier können Sie die Telefonnummern und E-Mail-Adressen festlegen, die Benutzer*innen verwenden, um Multi-Faktor-Authentifizierung und Self-Service-Kennwortzurücksetzung durchzuführen und ihr Kennwort zurückzusetzen.“ Wenn für einen Benutzer SSPR konfiguriert ist oder dieser MFA verwenden muss und Sie als Administrator dieses Feld ausfüllen, ist der Benutzer bereits registriert und muss für SSPR oder MFA keine Registrierungsschritte mehr durchführen.  Normalerweise registrieren sich Benutzer selbst. Es kommt eher selten vor, dass der Administrator dies ausführen muss.

1. Klicken sie auf das **X** oben rechts auf der Seite. Dadurch kehren Sie zur Benutzerliste zurück.

1. Klicken sie auf das **X** oben rechts auf der Seite. Dadurch kehren Sie zur Hauptseite für das Microsoft Entra Admin Center zurück.

1. Lassen Sie diese Browserregisterkarte geöffnet, da Sie sie in der nächsten Aufgabe verwenden werden.

### Überprüfung

In dieser Demo haben Sie die Einstellungen eines vorhandenen Benutzers gezeigt. Dazu zählen Gruppen, denen der Benutzer zugewiesen werden kann, die Verfügbarkeit von Rollen und die Zuweisung von Benutzerlizenzen.
