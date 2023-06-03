<a name="---"></a><!---
---
Lab: Title: 'Erkunden von Azure Active Directory' Learning Path/Module/Unit: 'Lernpfad: Beschreiben der Funktionen von Azure Active Directory (Azure AD), Teil von Microsoft Entra; Module 1: Beschreiben der grundlegenden Dienste und Identitätstypen von Azure AD; Lerneinheit 4: Beschreiben der Identitätstypen in Azure AD'
---
--->

# <a name="lab-explore-azure-active-directory"></a>Lab: Erkunden von Azure Active Directory

Dieses Lab ist den folgenden Learn-Inhalten zugeordnet:

- Lernpfad: Beschreiben der Funktionen von Azure Active Directory (Azure AD), Teil von Microsoft Entra
- Modul: Beschreiben der grundlegenden Dienste und Identitätstypen von Azure AD
- Lerneinheit: Beschreiben der Identitätstypen in Azure AD

## <a name="lab-scenario"></a>Labszenario

In diesem Lab greifen Sie auf Azure Active Directory zu.  Außerdem erstellen Sie einen Benutzer, konfigurieren die verschiedenen Einstellungen und fügen dabei auch Lizenzen hinzu.  

**Geschätzte Dauer**: 10–15 Minuten

### <a name="task-1"></a>Aufgabe 1

Als Abonnent von Microsoft 365 verwenden Sie Azure AD bereits.  Bei dieser Aufgabe durchlaufen Sie den schrittweisen Prozess zum Zugreifen auf Azure AD über das Microsoft 365-Verwaltungsportal und das Azure-Portal.

1. Wählen Sie im Microsoft Edge-Browser die Registerkarte „Start – Microsoft 365 Admin Center“ aus.

1. Wenn Sie diese Browserregisterkarte zuvor geschlossen haben, führen Sie die folgenden Schritte aus:
    1. Geben Sie in der Adressleiste **admin.microsoft.com** ein, und melden Sie sich wie folgt mit Ihren Administratoranmeldeinformationen an:
    1. Geben Sie **admin@WWLxZZZZZZ.onmicrosoft.com** (ZZZZZZ ist hierbei die eindeutige Mandanten-ID, die von Ihrem Lab-Hostinganbieter bereitgestellt wurde) in das Anmeldefenster ein, und wählen Sie dann **Weiter** aus.
    1. Geben Sie das Administratorkennwort ein, das von Ihrem Lab-Hostinganbieter bereitgestellt werden sollte. Wählen Sie **Anmelden**.
    1. Wählen Sie **Ja** aus, wenn Sie gefragt werden, ob Sie angemeldet bleiben möchten.
    1. Wählen Sie im linken Navigationsbereich von Microsoft 365 Admin Center **Alle anzeigen** aus.

1. Wählen Sie unter „Admin Center“ den Eintrag **Azure Active Directory** aus (möglicherweise müssen Sie dazu nach unten scrollen).  Die Seite „Mein Dashboard“ des Azure Active Directory Admin Center wird auf einer neuen Browserseite geöffnet. In den Hauptfenstern des Dashboards werden verschiedene Kacheln angezeigt, darunter die Kachel „Organisationsidentität“ (Contoso, der Mandant und die Azure AD-Edition), eine Kachel für Benutzer und Gruppen und mehr.

1. Wählen Sie im linken Navigationsbereich unter „Favoriten“ die Option **Azure Active Directory** aus.  Im Hauptfenster wird ein weiterer Navigationsbereich angezeigt. In diesem werden alle in Azure AD verfügbaren Dienste aufgelistet. Rechts finden Sie Informationen zum Mandanten „Contoso“ und Links zu erstellbaren Identitätstypen sowie zu ausgewählten Diensten.  

1. Öffnen Sie nun ein neues Browserfenster, und geben Sie **portal.azure.com** in die Adressleiste ein.  Da Sie sich bereits als admin@WWLxZZZZZZ.onmicrosoft.com angemeldet und ursprünglich dieselben Anmeldeinformationen verwendet haben, um Ihren Azure Pass einzulösen, sollten Sie beim Zugriff auf das Azure-Portal als Administrator angemeldet sein.  Sie können dies überprüfen, indem Sie sich die in der oberen rechten der Seite angegebene E-Mail-Adresse ansehen und den Mauszeiger über das Benutzersymbol bewegen.

1. Auf der Landing Page des Azure-Portals werden Azure-Dienste angezeigt, darunter Azure Active Directory, VMs, Speicherkonten, Datenbanken und vieles mehr.  Wählen Sie **Weitere Dienste** und dann **Azure Active Directory** aus. Wenn die Anzeige nicht sofort erfolgt, können Sie Azure Active Directory in die blaue Suchleiste eingeben und dort auswählen.  

1. Nun wird die Azure Active Directory-Instanz für Ihren Microsoft 365-Mandanten „Contoso“ angezeigt.    Unabhängig davon, mit welchem Verfahren Sie auf Azure Active Directory-Dienste zugreifen (über das Microsoft 365-Verwaltungsportal oder das Azure-Portal), gelangen Sie stets zur selben Stelle: zum Azure Active Directory von Contoso, in dem Sie alle Azure AD-Dienste verwalten können.

1. Lassen Sie diese Browserseite für die nächste Aufgabe geöffnet.

### <a name="task-2"></a>Aufgabe 2

Bei dieser Aufgabe erfahren Sie, wie Sie in Azure Active Directory einen neuen Benutzer erstellen. Außerdem erkunden Sie einige der Dienste, die auf Benutzerebene verwaltet werden können.

1. Navigieren Sie zu der in Ihrem Browser geöffneten Registerkarte „Contoso – Microsoft Azure“. Falls Sie die Registerkarte geschlossen haben, öffnen Sie eine Browserseite. Geben Sie „portal.azure.com“ in die Adressleiste ein, und wählen Sie „Azure Active Directory“ aus.  Sie sollten beim Azure-Portal als Administrator angemeldet sein. Falls nicht, melden Sie sich wieder an.

1. Wählen Sie im linken Navigationsbereich **Benutzer** aus.  Beachten Sie, dass bereits Benutzer für Ihren Mandanten konfiguriert sind.

1. Wählen Sie oben auf der Seite **+ Neuer Benutzer** aus, und wählen Sie dann im Dropdownfeld **Neuen Benutzer erstellen** aus.

1. **Neuen Benutzer erstellen** sollte bereits ausgewählt sein. Wenn dies nicht der Fall ist, wählen Sie diese Option aus.

1. Füllen Sie die Felder für **Identität** wie folgt aus:

    1. Benutzername: **sara**

    1. Feld „Name“: **Sara Perez**.

    1. Vorname: **Sara**.

    1. Nachname: **Perez**.

1. Füllen Sie die Felder für **Kennwort** wie folgt aus:

    1. Wählen Sie die Option **Kennwort selbst erstellen** aus.

    1. Anfängliches Kennwort: **Naja8996**. Sara wird bei ihrer ersten Anmeldung aufgefordert, ihr Kennwort zu ändern.

1. Konfigurieren Sie **Gruppen und Rollen**.

    1. Wählen Sie neben „Gruppen“ **0 Gruppen ausgewählt** aus.  Dadurch werden die verfügbaren Gruppen angezeigt.  Beachten Sie die Liste der verfügbaren Gruppen.

    1. Wählen Sie **Vorgänge** aus. Möglicherweise müssen Sie nach unten scrollen. Klicken Sie dann auf **Auswählen**. Beachten Sie, dass der Text neben „Gruppen“ aktualisiert wurde und jetzt widerspiegelt, dass 1 Gruppe ausgewählt ist.  

    1. Wählen Sie neben „Rollen“ **Benutzer** aus. Die Liste der Verzeichnisrollen wird angezeigt.  Scrollen Sie nach unten, um die verschiedenen integrierten Rollen anzuzeigen, ändern Sie jedoch die Benutzerrolle nicht.  Schließen Sie dieses Fenster. Wählen Sie dazu in der oberen rechten Ecke der Seite das **X** aus.

1. Konfigurieren von **Einstellungen**

    1. Anmeldung blockieren:  **Nein** (übernehmen Sie die Standardeinstellung).

    1. Nutzungsstandort: Wählen Sie die Dropdownliste aus, und wählen Sie dann **USA** (scrollen Sie nach unten, um diese Option zu finden) oder das Land aus, in dem Sie sich befinden.  Der Nutzungsspeicherort muss konfiguriert werden, um Lizenzen zuweisen zu können.

1. Wählen Sie unten auf der Seite die Schaltfläche **Erstellen** aus.

1. Vergewissern Sie sich, dass der Benutzer in der Benutzerliste angezeigt wird (Namen werden in alphabetischer Reihenfolge aufgeführt). Möglicherweise müssen Sie die Browserseite aktualisieren.

1. Wählen Sie in der Benutzerliste den soeben erstellten Benutzer (**Sara Perez**) aus.  Die Profilseite wird geöffnet.

1. Im linken Navigationsbereich werden die verschiedenen Optionen angezeigt, die für den Benutzer konfiguriert werden können.  Wählen Sie **Gruppen** aus.  Hier werden zusätzliche Informationen über die Gruppe angezeigt.  Überprüfen Sie, ob die Gruppe „Vorgänge“ aufgelistet wird (es kann ein paar Minuten dauern, bis die Gruppenzuweisung angezeigt wird).  Hinweis: Obwohl wir beim Erstellen des Benutzers lediglich eine Gruppe zugewiesen haben, wird auch die Gruppe „Contoso“ angezeigt.  Dies liegt an einer vorkonfigurierten Richtlinie im Mandanten, die bewirkt, dass neue Benutzer automatisch der Gruppe „Contoso“ zugewiesen werden.

1. Wählen Sie im linken Navigationsbereich **Lizenzen** aus.  Beachten Sie, dass für diesen Benutzer keine Lizenzzuweisungen gefunden wurden.  

1. Wählen Sie im oberen Bereich des Hauptfensters **+ Zuweisungen** aus, um eine Lizenz hinzuzufügen.

1. Wählen Sie unter „Lizenzen auswählen“ **Office 365 E3** und **Windows 10/11 Enterprise E3** aus. Wählen Sie anschließend unten im Bildschirm die Schaltfläche **Speichern** aus. In der oberen rechten Ecke des Bildschirms sollte in einer Benachrichtigung angezeigt werden, dass die Lizenzzuweisungen erfolgreich waren.

1. Wählen Sie oben rechts im Bildschirm das **X** aus, um das Fenster „Lizenzzuweisungen“ zu schließen.

1. Wählen Sie oben auf der Seite das Symbol **Aktualisieren** aus, um die Lizenzzuweisungen zu bestätigen.

1. Kehren Sie zur Azure Active Directory-Seite mit der Contoso-Übersicht zurück. Wählen Sie dazu oben links im Bildschirm **Contoso** (den Breadcrumb) aus, oberhalb der Angabe „Sara Perez | Lizenzen“.

1. Sie haben erfolgreich einen Benutzer in Azure Active Directory erstellt und konfiguriert.

1. Melden Sie sich von allen geöffneten Browserregisterkarten ab.  Melden Sie sich im Azure-Portal ab, indem Sie das Benutzersymbol neben der E-Mail-Adresse in der oberen rechten Ecke des Bildschirms auswählen und dann **Abmelden** auswählen. In Microsoft 365 melden Sie sich ab, indem Sie das Symbol in der oberen rechten Ecke des Microsoft 365-Fensters auswählen, das als Kreis mit den Buchstaben SP dargestellt wird (neben dem Fragezeichensymbol), und dann **Abmelden** auswählen. Schließen Sie alle Browserfenster.

### <a name="task-3"></a>Aufgabe 3

Bei dieser Aufgabe melden Sie sich erstmals als Sara Perez an.

1. Öffnen Sie Microsoft Edge.

2. Geben Sie **login.microsoft.com** in die Adressleiste ein.

3. Melden Sie sich als **sara@WWLxZZZZZ.onmicrosoft.com** an (ZZZZZZ ist hierbei die eindeutige Mandanten-ID, die von Ihrem Labhostinganbieter bereitgestellt wurde).

4. Geben Sie das temporäre Kennwort **Naja8996** ein.

5. Nun werden Sie aufgefordert, Ihr Kennwort zu aktualisieren. Geben Sie **Naja8996** in das Feld „Aktuelles Kennwort“ ein.

6. Geben Sie **SC900-Lab** in das Feld „Neues Kennwort“ ein.  Geben Sie „SC900-Lab“ in das Feld „Kennwort bestätigen“ ein, und wählen Sie dann „Anmelden“ aus.  Hinweis: Als bewährte Methode sollte ein sichereres Kennwort verwendet werden. Dieses Kennwort wird aus Gründen der Zweckmäßigkeit und nur für dieses Lab gewählt.

7. Sie sollten nun erfolgreich bei Microsoft 365 angemeldet sein.

8. Melden Sie sich ab, indem Sie das Symbol in der oberen rechten Ecke des Microsoft 365-Fensters auswählen, das als Kreis mit den Buchstaben SP (neben dem Fragezeichensymbol) angezeigt wird, und dann **Abmelden** auswählen. Schließen Sie dann den Browser.

### <a name="review"></a>Überprüfung

In diesem Lab haben Sie Azure AD erstmals erkundet. Da Abonnenten von Microsoft 365 Azure AD automatisch verwenden, haben Sie festgestellt, dass Sie über das Microsoft 365-Verwaltungsportal oder das Azure-Portal auf Azure AD-Funktionen und -Dienste zugreifen können.  Dabei gelangen Sie an dieselbe Stelle, unabhängig von Ihrem bevorzugten Verfahren.  Außerdem haben Sie den Prozess der Erstellung eines neuen Benutzers durchlaufen und die verschiedenen konfigurierbaren Einstellungen kennengelernt. Dazu zählen Gruppen, denen der Benutzer zugewiesen werden kann, die Verfügbarkeit von Rollen und die Zuweisung von Benutzerlizenzen.
