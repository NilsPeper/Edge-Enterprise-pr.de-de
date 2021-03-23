---
title: Anmerkungen zu dieser Version von Microsoft Edge für Beta-Kanal
ms.author: aguta
author: dan-wesley
manager: srugh
ms.date: 03/18/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Anmerkungen zu dieser Version von Microsoft Edge für Beta-Kanal
ms.openlocfilehash: 6b5e68d44daf3297a20d6e87169c800bc06b9011
ms.sourcegitcommit: 6a3787dead062e4a0860adbc570229974dcaee07
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "11442395"
---
# <a name="release-notes-for-microsoft-edge-beta-channel"></a>Versionshinweise für Microsoft Edge Beta-Kanal

Diese Versionshinweise enthalten Informationen zu neuen Funktionen und nicht sicherheitsrelevanten Updates, die im Microsoft Edge Beta-Kanal enthalten sind. Archivierte Versionen dieser Versionshinweise sind [hier](microsoft-edge-relnote-archive-beta-channel.md) verfügbar.

> [!NOTE]
> Wir haben die Versionshinweise zur Microsoft Edge Beta [Version 89.0.774.18 vom 3. Februar](#version-89077418-february-3) aktualisiert, um die neuen Features zu zeigen.

<!-- begin major 90 -->
## <a name="version-9008188-march-16"></a>Version 90.0.818.8: 16. März

### <a name="feature-updates"></a>Funktionsupdates

- **Einmaliges Anmelden (Single Sign On, SSO) ist jetzt für Azure Active Directory (Azure AD)-Konten und Microsoft-Konten (MSA) unter macOS verfügbar.** Ein bei Microsoft Edge unter macOS angemeldeter Benutzer wird nun automatisch bei Websites angemeldet, die so konfiguriert sind, dass eine einmalige Anmeldung mit Arbeits- und Microsoft-Konten möglich ist (z. B. bing.com, office.com, msn.com und outlook.com).

- **Drucken:**

  - **Neuer Druckrasterungsmodus für Nicht-PostScript-Drucker**. Ab Microsoft Edge Version 90 können Administratoren mithilfe einer neuen Richtlinie den Druckrasterungsmodus für ihre Benutzer definieren. Diese Richtlinie steuert, wie Microsoft Edge unter Windows auf Nicht-PostScript-Druckern druckt.  Manchmal müssen Druckaufträge bei Nicht-PostScript-Druckern gerastert werden, damit korrekt gedruckt wird. Die Druckoptionen sind „Full" (Vollständig) und „Fast“ (Schnell).

  - **Zusätzliche Optionen für die Seitenskalierung beim Drucken**. Benutzer können jetzt die Skalierung anpassen, während sie Webseiten und PDF-Dokumente mit zusätzlichen Optionen drucken. Die Option „An Seite anpassen" stellt sicher, dass die Webseite oder das Dokument in den Bereich passt, der im ausgewählten „Papierformat" zum Drucken verfügbar ist. Die Option "Tatsächliche Größe" stellt sicher, dass sich die Größe des zu druckenden Inhalts unabhängig von der ausgewählten "Papiergröße" nicht ändert.

- **Produktivität:**

  - **Vorschläge zum automatischen Ausfüllen werden um den Inhalt von Adressfeldern aus der Zwischenablage erweitert.** Der Inhalt der Zwischenablage wird analysiert, wenn Sie auf ein Profil-/Adressfeld (z. B. Telefon, E-Mail, Postleitzahl, Stadt, Bundesland usw.) klicken, um es als Vorschläge zum automatischen Ausfüllen anzuzeigen.

  - **Benutzer können nach Vorschlägen zum automatischen Ausfüllen suchen, auch wenn ein Formular oder Feld nicht erkannt wird**. Wenn Sie Ihre Informationen heute in Microsoft Edge gespeichert haben, werden automatisch Vorschläge zum automatischen Ausfüllen angezeigt, mit denen Sie beim Ausfüllen von Formularen Zeit sparen können. In Fällen, in denen beim automatischen Ausfüllen ein Formular fehlt oder wenn Sie Daten in Formularen abrufen möchten, die normalerweise nicht automatisch ausgefüllt sind (z. B. temporäre Formulare), können Sie mithilfe des automatischen Ausfüllens nach Ihren Informationen suchen.

- **Greifen Sie über ein Flyout in der Menüleiste auf Downloads zu**. Downloads werden in der oberen rechten Ecke mit allen aktiven Downloads an einem Ort angezeigt. Dieses Menü ist leicht zu schließen, sodass Benutzer ununterbrochen weiter surfen und den gesamten Download-Fortschritt direkt über die Symbolleiste überwachen können. [Mehr dazu](https://techcommunity.microsoft.com/t5/articles/introducing-the-new-downloads-experience/m-p/2111551).

- **Verbesserungen beim Rendern von Schriftarten**. Ab Microsoft Edge Version 90 haben wir das Rendern von Text verbessert, um die Klarheit zu verbessern und Unschärfe zu reduzieren. Ein Teil der Verbesserungen beim Rendern von Schriftarten wird in der Beta-Version 90 landen, ist jedoch standardmäßig deaktiviert.


### <a name="policy-updates"></a>Richtlinienupdates

#### <a name="new-policies"></a>Neue Richtlinien

Es wurden sieben neue Richtlinien hinzugefügt. Laden Sie die aktualisierten administrativen Vorlagen von der [Microsoft Edge Enterprise-Angebotsseite](https://www.microsoft.com/edge/business/download) herunter. Die folgenden neuen Richtlinien wurden hinzugefügt:

- [ApplicationGuardFavoritesSyncEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#applicationguardfavoritessyncenabled) – Synchronisierung von Application Guard-Favoriten aktiviert
- [ManagedConfigurationPerOrigin](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#managedconfigurationperorigin) – Legt verwaltete Konfigurationswerte für Websites auf bestimmte Ursprünge fest
- [PrintRasterizationMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#printrasterizationmode) – Druckrasterungsmodus
- [QuickViewOfficeFilesEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#quickviewofficefilesenabled) : Verwalten der QuickView Office-Dateifunktion in Microsoft Edge
- [SSLErrorOverrideAllowedForOrigins](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sslerroroverrideallowedfororigins) – Benutzer können von der HTTPS-Warnseite für bestimmte Ursprünge fortfahren
- [WindowOcclusionEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#windowocclusionenabled) – Fester-Okklusion aktivieren
- [WindowsHelloForHTTPAuthEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#windowshelloforhttpauthenabled) – Windows Hello für HTTP-Authentifizierung aktiviert

#### <a name="deprecated-policies"></a>Veraltete Richtlinien

- [NativeWindowOcclusionEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#nativewindowocclusionenabled) – Native Fenster-Okklusion aktivieren
- [SSLVersionMin](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sslversionmin)– Mindestens aktivierte TLS-Version
<!-- end major 90 -->

## <a name="version-89077454-march-13"></a>Version 89.0.774.54: 13. März

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-89077450-march-10"></a>Version 89.0.774.50: 10. März

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-89077448-march-8"></a>Version 89.0.774.48: 8. März

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-89077445-march-3"></a>Version 89.0.774.45: 3. März

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-89077439-february-26"></a>Version 89.0.774.39: 26. Februar

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-89077434-february-22"></a>Version 89.0.774.34: 22. Februar

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-89077427-february-12"></a>Version 89.0.774.27: 12. Februar

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-89077423-february-8"></a>Version 89.0.774.23: 8. Februar

Verschiedene Fehler und Leistungsprobleme wurden behoben.

<!-- begin major 89 -->
## <a name="version-89077418-february-3"></a>Version 89.0.774.18: 3. Februar

### <a name="feature-updates"></a>Funktionsupdates

- **Der Kiosk-Modus ermöglicht zusätzliche Sperrfunktionen**. Ab Microsoft Edge Version 89 haben wir zusätzliche Sperrfunktionen im Kioskmodus hinzugefügt, damit Kunden ihre Arbeit produktiver und sicherer erledigen können. [Mehr dazu](microsoft-edge-configure-kiosk-mode.md#kiosk-mode-supported-features).

- **Das Site List Manager-Tool im Enterprise-Modus ist im Browser über die Seite *edge://compat* verfügbar**. Mit diesem Tool können Sie XML-Site-Listen für den Internet Explorer-Modus unter Microsoft Edge erstellen, bearbeiten und exportieren. Sie können den Zugriff auf dieses Tool nach Bedarf über Gruppenrichtlinien aktivieren. [Mehr dazu](https://docs.microsoft.com/deployedge/edge-ie-mode-site-list-manager).

- **Verbessern der Browserleistung mit ruhenden Registerkarten**. Das Ruhen von Registerkarten verbessert die Browserleistung, indem inaktive Registerkarten in den Ruhezustand versetzt werden, um Systemressourcen wie Speicher und CPU freizugeben, sodass aktive Registerkarten oder andere Anwendungen sie verwenden können. Benutzer können verhindern, dass Websites in den Ruhezustand versetzt werden, und die Zeitspanne konfigurieren, in der eine inaktive Registerkarte in den Ruhezustand versetzt wird. Um die Benutzer in ihrem Fluss zu halten, gibt es auch [Heuristiken](https://techcommunity.microsoft.com/t5/articles/sleeping-tabs-faq/m-p/1705434), die verhindern, dass bestimmte Websites in den Ruhezustand versetzt werden, z.B. Intranetsites. Diese Funktion kann mit Gruppenrichtlinien verwaltet werden.

  > [!NOTE]
  > „Verbessern der Browserleistung mit ruhenden Registerkarten“ ist ein Update für die Versionshinweise vom 3. Februar für Hauptversion 89.0.774.18.

- **Setzen Sie Ihre Microsoft Edge-Synchronisierungsdaten in der Cloud manuell zurück**. Wir bieten eine Möglichkeit, Ihre Microsoft Edge-Synchronisierungsdaten aus dem Produkt heraus zurückzusetzen. Auf diese Weise wird sichergestellt, dass Ihre Daten aus den Microsoft-Diensten gelöscht werden und bestimmte Produktprobleme behoben werden, für die zuvor ein Support-Ticket erforderlich war.

- **Verbesserungen bei der Textauswahl in PDF-Dokumenten**. Benutzer erhalten eine reibungslosere und konsistentere Textauswahl für PDF-Dokumente, die ab Version 89 in Microsoft Edge geöffnet werden.

- **Das Feld für das Geburtsdatum wird jetzt beim automatischen Ausfüllen unterstützt**. Heute hilft Ihnen Microsoft Edge, Zeit und Mühe beim Ausfüllen von Formularen und beim Erstellen von Online-Konten zu sparen, indem Sie Ihre Daten wie Adressen, Namen, Telefonnummern usw. automatisch ausfüllen. Ab Microsoft Edge Version 89 bieten wir Unterstützung für ein anderes Feld, das Sie gespeichert und automatisch ausgefüllt haben können – das Geburtsdatum. Sie können diese Informationen jederzeit in Ihren Profileinstellungen anzeigen, bearbeiten und löschen.

- **Unterstützung für die Suche in natürlicher Sprache in der Adressleiste, auf der Verlaufssuchseite und im Verlaufshub**. Ab Microsoft Edge Version 89 wird das Auffinden eines Artikels/einer Website durch die Suche in natürlicher Sprache in der Adressleiste, auf der Verlaufsseite und im Verlaufshub einfacher. Benutzer können zusätzlich zu Titeln/URL-Keyword-Übereinstimmungen nach zuvor angesehenem Seiteninhalt/Beschreibung/Timing (z. B. "Kuchenrezept der letzten Woche") suchen. Diese Funktion ist auf eine zufällig ausgewählte Gruppe von Benutzern beschränkt, die das Experimentieren aktiviert haben. Diese Benutzer geben dem Feature-Team Feedback.

### <a name="policy-updates"></a>Richtlinienupdates

#### <a name="new-policies"></a>Neue Richtlinien

- [BrowsingDataLifetime](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#browsingdatalifetime) – Durchsuchen der Einstellungen für die Lebensdauer von Daten
- [MAMEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#mamenabled) – Mobile App Management aktiviert
- [DefinePreferredLanguages](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#definepreferredlanguages) – Definiert eine geordnete Liste der bevorzugten Sprachen, in denen Websites angezeigt werden sollen, wenn die Website die Sprache unterstützt
- [ShowRecommendationsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#showrecommendationsenabled) – Zulassen von Empfehlungen und Werbebenachrichtigungen von Microsoft Edge
- [PrintingAllowedBackgroundGraphicsModes](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#printingallowedbackgroundgraphicsmodes) – Einschränken des Druckmodus für Hintergrundgrafiken
- [PrintingBackgroundGraphicsDefault](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#printingbackgroundgraphicsdefault)– Standard-Druckmodus für Hintergrundgrafiken
- [SmartActionsBlockList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#smartactionsblocklist)– Blockieren der intelligenten Aktionen für eine Liste von Diensten

#### <a name="obsoleted-policies"></a>Veraltete Richtlinie

- [ForceLegacyDefaultReferrerPolicy](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forcelegacydefaultreferrerpolicy): Verwenden Sie die standardmäßige Verweiserrichtlinie „kein Verweiser beim Downgrade“
- [MetricsReportingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#metricsreportingenabled) – Aktivieren Sie die Berichterstellung für Nutzung und Absturz
- [SendSiteInfoToImproveServices](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices)|Senden von Site-Informationen, um die Microsoft-Dienste zu verbessern
<!-- end major 89 -->

## <a name="version-88070556-january-29"></a>Version 88.0.705.56: 29. Januar

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-88070549-january-20"></a>Version 88.0.705.49: 20. Januar

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-88070545-january-15"></a>Version 88.0.705.45: 15. Januar

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-88070541-january-11"></a>Version 88.0.705.41: 11. Januar

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-88070529-december-21"></a>Version 88.0.705.29: 21. Dezember

Verschiedene Fehler und Leistungsprobleme wurden behoben.

<!-- begin major 88 -->
## <a name="version-88070518-december-9"></a>Version 88.0.705.18: 9. Dezember

### <a name="feature-updates"></a>Funktionsupdates

- **Abschreibungen:**

  - Veraltete Unterstützung für das FTP-Protokoll. Die Unterstützung für das ältere FTP-Protokoll wurde von Microsoft Edge entfernt. Der Versuch, zu einer FTP-Verbindung zu navigieren, führt dazu, dass der Browser das Betriebssystem anweist, eine externe Anwendung zu öffnen, um die FTP-Verbindung zu verarbeiten. Alternativ können IT-Administratoren Microsoft Edge so konfigurieren, dass der IE-Modus für Sites verwendet wird, die auf dem FTP-Protokoll basieren.
  - Die Adobe Flash-Unterstützung wird entfernt. Ab Microsoft Edge Beta Version 88 werden die Adobe Flash-Funktionen und die Unterstützung entfernt. Weitere Informationen: [Update auf Adobe Flash Player Ende der Unterstützung – Microsoft Edge-Blog (windows.com)](https://blogs.windows.com/msedgedev/2020/09/04/update-adobe-flash-end-support/)

- **Authentifizierung:**

  - Einmaliges Anmelden (SSO, Single Sign On) ist jetzt für Azure Active Directory-Konten (Azure AD) und Microsoft Account (MSA) unter MacOS und Windows auf niedrigerer Ebene verfügbar. Ein Benutzer, der bei Microsoft Edge unter macOS oder Microsoft Windows (7, 8.1) auf niedrigerer Ebene angemeldet ist, wird jetzt automatisch bei Websites angemeldet, die so konfiguriert sind, dass sie eine einmalige Anmeldung mit Work- und Microsoft-Konten ermöglichen (z. B. bing.com, office.com, msn.com, outlook.com).<br>Hinweis: Ein Benutzer muss sich möglicherweise abmelden und dann erneut anmelden, wenn er sich in einer Version vor Microsoft Edge 88 bei Microsoft Edge angemeldet hat, um diese Funktion nutzen zu können.
  - Wechseln Sie Benutzer unter macOS automatisch zu ihrem Arbeitsprofil für Websites, die sich bei ihrem Arbeitskonto authentifizieren. Ab Microsoft Edge Version 88 bieten wir die Möglichkeit, unter Websites zu wechseln, die sich unter macOS mit dem Arbeitsprofil eines Benutzers authentifizieren.<br>Hinweis: Ein Benutzer muss sich möglicherweise abmelden und dann erneut anmelden, wenn er sich in einer Version vor Microsoft Edge 88 bei Microsoft Edge angemeldet hat, um diese Funktion nutzen zu können.

- **Kioskmodus-Option zum Beenden der Sitzung**. Die Schaltfläche „Sitzung beenden“ ist jetzt im öffentlichen Browsing im Kioskmodus verfügbar. Diese Funktion stellt sicher, dass Browserdaten und -einstellungen gelöscht werden, wenn Microsoft Edge geschlossen wird. Weitere Informationen zu den Funktionen und der Roadmap des Kioskmodus finden Sie unter [Konfigurieren des Microsoft Edge-Kioskmodus](https://docs.microsoft.com/deployedge/microsoft-edge-configure-kiosk-mode).

- **Sicherheit und Datenschutz:**

  - Benachrichtigungen werden generiert, wenn das Kennwort eines Benutzers in einem Onlineleck gefunden wird. Benutzerkennwörter werden gegen ein Verzeichnis bekannter Anmeldeinformationen überprüft und geben dem Benutzer eine Warnung zurück, wenn eine Übereinstimmung gefunden wird. Um die Sicherheit und den Datenschutz zu gewährleisten, werden Benutzerkennwörter gehashed und verschlüsselt, wenn Sie mit der Datenbank der durchgesickerten Anmeldeinformationen abgeglichen werden.
  - Aktualisieren Sie gemischte Inhalte automatisch. Über HTTPS gelieferte sichere Seiten können Referenzbilder enthalten, die über nicht sicheres HTTP bereitgestellt werden. Um den Datenschutz und die Sicherheit in Microsoft Edge 88 zu verbessern, werden diese Bilder stattdessen über HTTPS abgerufen. Wenn das Bild nicht über HTTPS verfügbar ist, wird es nicht geladen.
  - Anzeigen von Site-Berechtigungen nach Site und nach letzten Aktivitäten. Ab Microsoft Edge 88 können Benutzer Site-Berechtigungen einfacher verwalten. Sie können Berechtigungen nach Website und nicht nur nach Berechtigungstyp anzeigen. Darüber hinaus haben wir einen Abschnitt mit den letzten Aktivitäten hinzugefügt, in dem ein Benutzer alle letzten Änderungen an seinen Websiteberechtigungen anzeigt.
  - Verbesserte Steuerelemente für Browser-Cookies. Ab Microsoft Edge 88 können Benutzer Cookies von Drittanbietern löschen, ohne dass dies Auswirkungen auf Cookies von Drittanbietern hat. Benutzer können ihre Cookies auch nach Erst- oder Drittanbietern filtern und nach Name, Anzahl der Cookies und der Menge der gespeicherten und zuletzt geänderten Daten sortieren.

- **Leistung:**

  - Verbessern Sie die Browserleistung mit Sleeping Tabs. Das Ruhen von Registerkarten verbessert die Browserleistung, indem inaktive Registerkarten in den Ruhezustand versetzt werden, um Systemressourcen wie Speicher und CPU freizugeben, sodass aktive Registerkarten oder andere Anwendungen sie verwenden können. Benutzer können verhindern, dass Websites in den Ruhezustand versetzt werden, und die Zeitspanne konfigurieren, in der eine inaktive Registerkarte in den Ruhezustand versetzt wird. Um die Benutzer in ihrem Fluss zu halten, gibt es auch Heuristiken, die verhindern, dass bestimmte Websites in den Ruhezustand versetzt werden, z. B. Intranetsites. Hinweis: Diese Funktion ist auf eine zufällig ausgewählte Gruppe von Benutzern beschränkt, die das Experimentieren aktiviert haben. Wir planen, das Feature „ruhende Registerkarten“ mit der Version 89 von Microsoft Edge standardmäßig zu aktivieren. Diese Funktion kann mit Gruppenrichtlinien verwaltet werden.
  - Verbessern Sie die Startgeschwindigkeit von Microsoft Edge mit dem Start-Boost. Um die Startgeschwindigkeit von Microsoft Edge zu verbessern, haben wir eine Funktion namens Startup Boost entwickelt. Durch den Startschub wird der Start von Microsoft Edge beschleunigt, da Microsoft Edge im Hintergrund ausgeführt werden kann. Hinweis: Diese Funktion ist auf eine zufällig ausgewählte Gruppe von Benutzern beschränkt, die das Experimentieren aktiviert haben. Diese Benutzer geben dem Feature-Team Feedback.

- **Produktivität:**

  - Verbessern Sie die Produktivität und das Multitasking mit vertikalen Registerkarten. Wenn die Anzahl der horizontalen Registerkarten zunimmt, werden die Site-Titel abgeschnitten und die Steuerelemente der Registerkarten gehen verloren, wenn die einzelnen Registerkarten verkleinert werden. Dies unterbricht den Benutzerworkflow, da sie mehr Zeit damit verbringen, ihre Registerkarten zu finden, zu wechseln und zu verwalten, und weniger Zeit für die jeweilige Aufgabe. Mit vertikalen Registerkarten können Benutzer ihre Registerkarten zur Seite verschieben. Vertikal ausgerichtete Symbole und längere Site-Titel erleichtern das schnelle Scannen, Identifizieren und Wechseln zu der Registerkarte, die sie öffnen möchten.
  - Das Feld für das Geburtsdatum wird automatisch ausgefüllt. Microsoft Edge spart bereits Zeit und Mühe beim Ausfüllen von Formularen und beim Erstellen von Online-Konten, indem Benutzerdaten wie Adressen, Namen, Telefonnummern usw. automatisch ausgefüllt werden. Microsoft Edge unterstützt jetzt das Feld für das Geburtsdatum, das Benutzer speichern und automatisch ausfüllen können. Ein Benutzer kann diese Informationen jederzeit in seinen Profileinstellungen anzeigen, bearbeiten und löschen.
  - Verbesserungen an Vor kurzem im Verlauf geschlossen. „Vor kurzem geschlossen“ behält jetzt die letzten 25 Registerkarten und Fenster aus früheren Browsersitzungen und nicht nur aus der vorherigen Sitzung bei. Benutzer können in der neuen Verlaufserfahrung die Option „Zuletzt geschlossen“ auswählen, um alle geöffneten Registerkarten anzuzeigen.
  - Das Feature "Ihr Tag auf einen Blick" ist standardmäßig aktiviert. Beginnend mit Microsoft Edge Version 88 können Informationsdienste von intelligenten Produktivitätsfunktionen auf ihrer neuen Registerkarte (NTP) profitieren. Wir bieten Benutzern, die mit Ihrem Geschäfts-, Schul- oder Schulkonto angemeldet sind, personalisierte und relevante Inhalte an, die von Ihrem M365-Diagramm angetrieben werden. Benutzer können Ihre "Ihr Tag auf einen Blick"-Module schnell durchsuchen, um Ihre Besprechungen und die aktuelle Arbeit zu überwachen sowie die Anwendungen, die Sie verwenden möchten, schnell zu starten.

- **PDF:**

  - PDF-Dokumentanzeige in der Buchansicht (zwei Seiten). Ab Microsoft Edge Version 88 können Benutzer PDF-Dokumente auf einer einzelnen Seite oder in der zweiseitigen Buchansicht anzeigen. Um die Ansicht zu ändern, klicken Sie in der Symbolleiste auf die Schaltfläche **Seitenansicht**.
  - Unterstützung für verankerte Textnotizen für PDF-Dateien. Ab Microsoft Edge Version 87 können Benutzer zu jedem Text in PDF-Dateien getippte Textnotizen hinzufügen.
  - Reibungslosere Textauswahl in PDF-Dokumenten. Benutzer erhalten eine reibungslosere und konsistentere Textauswahl für alle in Microsoft Edge geöffneten PDF-Dokumente.
  - Zeigen Sie als PDF-Dateien gespeicherte Webseiten in der Download-Leiste an. Benutzer können jetzt die generierten PDF-Dateien anzeigen, indem sie "Als PDF speichern" als Druckerziel für Webseiten in der Download-Leiste festlegen.

- **Schriftarten:**

  - Browsersymbole werden auf das Fluent-Designsystem aktualisiert. Im Rahmen unserer fortgesetzten Arbeit an Fluent Design im Browser haben wir Änderungen vorgenommen, um die Symbole näher am neuen Microsoft-Symbolsystem auszurichten. Diese Änderungen wirken sich auf viele unserer High-Touch-Benutzeroberflächen aus, einschließlich Registerkarten, Adressleiste sowie Navigations- und Wegfindungssymbole in unseren verschiedenen Menüs.
  - Verbesserte Schriftwiedergabe. Die Textwiedergabe wurde verbessert, um die Übersichtlichkeit zu verbessern und Unschärfe zu verringern.

### <a name="policy-updates"></a>Richtlinienupdates

#### <a name="new-policies"></a>Neue Richtlinien

Sechzehn neue Richtlinien wurden hinzugefügt. Laden Sie die aktualisierten administrativen Vorlagen von der [Microsoft Edge Enterprise Angebotsseite](https://www.microsoft.com/edge/business/download) herunter. Die folgenden neuen Richtlinien wurden hinzugefügt.

- [BlockExternalExtensions](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#blockexternalextensions) – Blockieren Sie die Installation externer Erweiterungen.
- [InternetExplorerIntegrationLocalFileAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationlocalfileallowed) – Ermöglichen Sie das Starten lokaler Dateien im Internet Explorer-Modus.
- [InternetExplorerIntegrationLocalFileExtensionAllowList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationlocalfileextensionallowlist) – Öffnen Sie lokale Dateien im Internet Explorer-Modus.
- [InternetExplorerIntegrationLocalFileShowContextMenu](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationlocalfileshowcontextmenu) – Leiten Sie das Kontextmenü an, einen Link im Internet Explorer-Modus zu öffnen.
- [IntranetRedirectBehavior](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#intranetredirectbehavior) – Intranet-Umleitungsverhalten.
- [PrinterTypeDenyList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#printertypedenylist) – Deaktivieren Sie die Druckertypen in der Verweigerungsliste.
- [ShowMicrosoftRewards](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#showmicrosoftrewards) – Zeigen Sie Microsoft Rewards-Erfahrungen an.
- [SleepingTabsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sleepingtabsenabled) – Konfigurieren Sie Sleeping Tabs.
- [SleepingTabsTimeout](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sleepingtabstimeout) – Legen Sie das Zeitlimit für die Inaktivität der Hintergrundregisterkarte für Sleeping Tabs fest.
- [SleepingTabsBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sleepingtabsblockedforurls) – Blockieren Sie Sleeping Tabs auf bestimmten Websites.
- [StartupBoostEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#startupboostenabled) – Startbeschleunigung aktivieren.
- [UpdatePolicyOverride](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#updatepolicyoverride) – Gibt an, wie Microsoft Edge Update verfügbare Updates von Microsoft Edge verarbeitet. 
- [VerticalTabsAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#verticaltabsallowed) – Konfiguriert die Verfügbarkeit eines vertikalen Layouts für Registerkarten an der Seite des Browsers.
- [WebRtcAllowLegacyTLSProtocols](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webrtcallowlegacytlsprotocols) – Ermöglichen Sie ein älteres TLS/DTLS-Downgrade in WebRTC.

#### <a name="deprecated-policies"></a>Veraltete Richtlinien

Die folgenden Richtlinien sind veraltet.

- [ProactiveAuthEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proactiveauthenabled) – Aktivieren Sie die proaktive Authentifizierung.
- [ProxyBypassList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxybypasslist) – Konfigurieren Sie die Proxy-Umgehungsregeln.
- [ProxyMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxymode) – Konfigurieren Sie die Proxy-Server-Einstellungen.
- [ProxyPacUrl](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxypacurl) – Legen Sie die URL der Proxy .pac-Datei fest.
- [Proxyserver](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxyserver) – Konfigurieren Sie die Adresse oder URL des Proxyservers.
- [WebDriverOverridesIncompatiblePolicies](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webdriveroverridesincompatiblepolicies) – Erlauben Sie WebDriver, inkompatible Richtlinien zu überschreiben.

#### <a name="obsoleted-policies"></a>Veraltete Richtlinie

Die folgenden Richtlinien sind veraltet.

- [DefaultPluginsSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultpluginssetting) – Standardeinstellung für Adobe Flash.
- [PluginsAllowedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#pluginsallowedforurls) – Lassen Sie das Adobe Flash-Plug-In auf bestimmten Websites zu.
- [PluginsBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#pluginsblockedforurls) – Blockieren Sie das Adobe Flash-Plug-in auf bestimmten Websites.
- [RunAllFlashInAllowMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#runallflashinallowmode) – Erweitern der Adobe Flash-Inhaltseinstellung auf alle Inhalte.

<!-- end major 88 -->

## <a name="version-87066455-december-3"></a>Version 87.0.664.55: 3. Dezember

Verschiedene Bugs und Leistungsprobleme wurden behoben. Das folgende neue Feature wird in diesem Release unterstützt.

- **Benachrichtigungen werden generiert, wenn das Kennwort eines Benutzers in einem Onlineleck gefunden wird**. Benutzerkennwörter werden gegen ein Verzeichnis bekannter Anmeldeinformationen überprüft und geben dem Benutzer eine Warnung zurück, wenn eine Übereinstimmung gefunden wird. Um die Sicherheit und den Datenschutz zu gewährleisten, werden Benutzerkennwörter gehashed und verschlüsselt, wenn Sie mit der Datenbank der durchgesickerten Anmeldeinformationen abgeglichen werden.

## <a name="version-87066452-november-30"></a>Version 87.0.664.52: 30. November

Verschiedene Bugs und Leistungsprobleme wurden behoben.

## <a name="version-87066440-november-18"></a>Version 87.0.664.40: vom 18. November

Verschiedene Bugs und Leistungsprobleme wurden behoben.

## <a name="version-87066436-november-16"></a>Version 87.0.664.36: 16. November

Verschiedene Bugs und Leistungsprobleme wurden behoben.

## <a name="version-87066430-november-9"></a>Version 87.0.664.30: 9. November

Verschiedene Bugs und Leistungsprobleme wurden behoben.

## <a name="version-87066424-november-2"></a>Version 87.0.664.24: 2. November

Verschiedene Bugs und Leistungsprobleme wurden behoben.

## <a name="version-87066418-october-26"></a>Version 87.0.664.18: 26.Oktober

Verschiedene Bugs und Leistungsprobleme wurden behoben.

<!--- Archived from Version 87.0.664.12: October 20 to to version 86.0.622.15: September 14 ---->
<!--- Archived to version 86.0.622.11: September 9 ---->
<!--- Archived to version 85.0.564.18: July 28 ---->

## <a name="see-also"></a>Weitere Informationen

- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)
