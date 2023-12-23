<!---
---
Demo: Titel: Erkunden Microsoft Entra ID Benutzereinstellungen Lernpfad/Modul/Einheit: Lernpfad: Beschreiben der Funktionen von Microsoft Entra; Modul 2: Beschreiben der Authentifizierungsfunktionen von Microsoft Entra ID; Lerneinheit 3: Beschreiben der Authentifizierungsmethoden und Einheit 4: Beschreiben der mehrstufigen Authentifizierung
---
--->

# Authentifizierungsmethoden und MFA

Diese Demo ist den folgenden Learn-Inhalten zugeordnet:

- Lernpfad 2: Beschreiben der Funktionen von Microsoft Entra.
- Module: Beschreibung der Authentifizierungsfunktionen von Microsoft Entra ID.
- Lerneinheiten: Beschreiben von Authentifizierungsmethoden und Beschreiben der mehrstufigen Authentifizierung.

## Vorführungsszenario

In dieser Demo erkunden Sie die verschiedenen Einstellungen, die für die Authentifizierung in Microsoft Entra verfügbar sind.

1. Kehren Sie zur geöffneten Browserregisterkarte mit dem Titel „Home-Microsoft Entra Admin Center“ zurück.  Wenn Sie diese Browserregisterkarte zuvor geschlossen haben, öffnen Sie Microsoft Edge, und melden Sie sich bei **[entra.microsoft.com](https://entra.microsoft.com)** mit Ihren Microsoft 365-Administratoranmeldeinformationen an.

1. Erweitern Sie im linken Navigationsbereich **Schutz** und wählen Sie dann **Authentifizierungsmethoden** aus.

1. Wenn Sie Authentifizierungsmethoden auswählen, wird die Richtlinienseite angezeigt.  Hier sehen Sie die verfügbaren Authentifizierungsmethoden und ob sie aktiviert sind.  Wir gehen einige der dieser Methoden durch:  
    1. Wählen Sie **SMS** aus.  Lesen Sie die Beschreibung oben auf der Seite: „Diese Authentifizierungsmethode übermittelt einen einmaligen Code per SMS an das Telefon des Benutzers, und der Benutzer gibt diesen Code dann für die Anmeldung ein. SMS kann für Multi-Faktor-Authentifizierung und Self-Service-Kennwortzurücksetzung verwendet werden. Sie kann auch so konfiguriert werden, dass sie als erster Faktor verwendet werden kann.“
        1. Hier ist zu beachten, dass einige Authentifizierungsmethoden für MFA und/oder SSPR verwendet werden können.  Einige können nur als primäre Form der Authentifizierung verwendet werden, während andere nur als sekundäre Authentifizierungsform verwendet werden können.
        1. Um eine bestimmte Authentifizierungsmethode zu konfigurieren, müssen Sie sie aktivieren und dann festlegen, welche Benutzer und/oder Gruppen eingeschlossen werden sollen.  Sie können auch auswählen, welche Gruppen ausgeschlossen werden sollen.
        1. Nehmen Sie keine Änderungen an den Einstellungen vor.  Wählen Sie das **X** in der oberen rechten Ecke der Seite aus, um die SMS-Einstellungsseite zu schließen.  
    1. Sehen wir uns die Sprachanrufeinstellungen an.  Wählen Sie **Sprachanruf** aus. In der Beschreibung sehen Sie einen wichtigen Unterschied.  Der Sprachanruf kann nicht als Erste-Faktor-Authentifizierungsmethode verwendet werden.
    1. Wählen Sie nun **Microsoft Authenticator aus**.  Dies sind die wichtigsten Authentifizierungsmethoden.  
        1. Hier aktivieren Sie die Features und zielen darauf ab, wer eingeschlossen werden soll.  Sie können dies für alle Benutzer oder Gruppen tun. Nachdem Sie ermittelt haben, welche Benutzer/Gruppen eingeschlossen werden sollen, können Sie bestimmte Gruppen identifizieren, die ausgeschlossen werden sollen.  
        1. Auf der Registerkarte **Konfigurieren** können Sie auswählen, ob ein bestimmtes Feature von Microsoft verwaltet wird. Die Option, die Einstellung ist eine bequeme Möglichkeit für eine Organisation, Microsoft zu erlauben, eine Funktion standardmäßig zu aktivieren oder zu deaktivieren. Dies kann einer Organisation helfen, ihren Sicherheitsstatus zu verbessern.
        1. Nehmen Sie keine Änderungen an den Einstellungen vor. Schließen Sie dieses Fenster mit dem **X** oben rechts auf der Seite.
 
1. Sehen wir uns nun den Kennwortschutz an. Wählen Sie **Kennwortschutz aktivieren**.  Beachten Sie die verschiedenen verfügbaren Konfigurationsparameter.  
    1. Wählen Sie das Informationssymbol neben **Sperrschwellenwert** aus, um die Bedeutung dieses Parameters anzuzeigen.  Derzeit ist es auf 10 festgelegt, was bedeutet, dass es bis zu 10 fehlerhafte Anmeldungen geben kann, bevor das Konto gesperrt wird.  Wenn es Ihnen ein bisschen zu hoch erscheint, können Sie einen anderen Wert festlegen.
    1. Wählen Sie das Informationssymbol für jeden der verschiedenen Parameter aus, und sprechen Sie kurz darüber.  Sie sollten insbesondere die Liste der benutzerdefinierten gesperrten Kennwörter aufrufen.

1. Die Authentifizierungsstärke ist ein Steuerelement für bedingten Zugriff, mit dessen Hilfe Administratoren angeben können, welche Kombination von Authentifizierungsmethoden für den Zugriff auf eine Ressource verwendet werden kann. Dies wird unter Bedingter Zugriff angezeigt.

1. Wählen Sie im linken Navigationsbereich für Authentifizierungsmethoden die Option **Aktivität** aus.
    1. Die **Registrierung** wird mit einer blauen Unterstreichung angezeigt.  Hier können Sie die Registrierungsaktivität für verschiedene Authentifizierungsmethoden anzeigen.
    1. Wählen Sie **Verwendung** aus, um Nutzungsdetails anzuzeigen, und beachten Sie, dass Sie verschiedene Filter hinzufügen können.

1. In diesem Modul haben Sie auch über die mehrstufige Authentifizierung gesprochen. Sie werden MFA weiter in der Demo zum bedingten Zugriff behandeln, aber Sie sollten sich eine Minute Zeit nehmen, um einige grundlegende Einstellungen anzuzeigen.  Wählen Sie im Microsoft Entra Navigationsbereich des Admin Centers die Option **Mehrstufige Authentifizierung** aus.  Möglicherweise müssen Sie im linken Navigationsbereich im Abschnitt Schutz die Option **Mehr anzeigen** auswählen.
    1. Auf der Seite **Erste Schritte** wird gezeigt, dass sie am besten über bedingten Zugriff auf Benutzer angewendet werden kann. Es gibt jedoch einige spezifische Einstellungen, die Sie hier konfigurieren müssen.
    1. Wählen Sie **Kontosperrung** aus und rufen Sie die konfigurierbaren Sperrparameter auf.
    1. Wählen Sie **Benutzer blockieren/aufheben** aus, und erklären Sie, dass hier ein Administrator Benutzer manuell blockieren bzw. die Blockierung aufheben kann.  Beachten Sie, dass ein blockierter Benutzer 90 Tage blockiert bleibt, es sei denn, die Blockierung wird manuell aufgehoben.
    1. Wählen Sie **Betrugswarnung** aus.  Hiermit können Admins den Benutzern das Melden von Betrugsversuchen ermöglichen, wenn sie eine nicht von ihnen initialisierte Anforderung zur Überprüfung in zwei Schritten erhalten.
    1. Wählen Sie **Benachrichtigungen** aus.  Sie können Microsoft Entra ID so konfigurieren, dass E-Mail-Benachrichtigungen gesendet werden, wenn Benutzer Betrugswarnungen melden. Diese Benachrichtigungen werden in der Regel an Identitätsadministratoren gesendet, da die Anmeldeinformationen für das Benutzerkonto wahrscheinlich kompromittiert sind.
    1. Schließen Sie dieses Fenster mit dem **X** oben rechts auf der Seite.  Wiederholen Sie dann diesen Schritt, um zum Microsoft Entra Admin Center zurückzukehren.

1. Lassen Sie die Browserregisterkarte geöffnet, während Sie für die nächste Demo zum Microsoft Entra Admin Center zurückkehren.

### Überprüfung

In dieser Demo haben Sie die in Microsoft Entra verfügbaren Authentifizierungsmethoden gezeigt.  Sie zeigen auch einige der konfigurierbaren Parameter an, die der mehrstufigen Authentifizierung zugeordnet sind.
