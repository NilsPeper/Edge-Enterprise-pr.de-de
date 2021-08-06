---
title: Archivierte Versionshinweise für Microsoft Edge Beta-Kanal
ms.author: aguta
author: AndreaLBarr
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Archivierte Versionshinweise für Microsoft Edge Beta-Kanal
ms.openlocfilehash: 60ef45f2b0db38233e06faa6aa3104ac1f9930c66b342cf9eb8d53f936c52256
ms.sourcegitcommit: d44c0997ffe40d67421312ed96e7766da947eaa0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "11727618"
---
# <a name="archived-release-notes-for-microsoft-edge-beta-channel"></a>Archivierte Versionshinweise für Microsoft Edge Beta-Kanal

Diese Versionshinweise enthalten Informationen zu neuen Funktionen und nicht sicherheitsrelevanten Updates, die im Microsoft Edge Beta-Kanal enthalten sind. Informationen zu Microsoft Edge-Kanälen finden Sie in der [Übersicht über die Microsoft Edge-Kanäle](microsoft-edge-channels.md). Alle Sicherheitsupdates werden [hier](microsoft-edge-relnotes-security.md) aufgelistet.
## <a name="version-89077418-february-3"></a>Version 89.0.774.18: 3. Februar

### <a name="feature-updates"></a>Funktionsupdates

- **Der Kiosk-Modus ermöglicht zusätzliche Sperrfunktionen**. Ab Microsoft Edge Version 89 haben wir zusätzliche Sperrfunktionen im Kioskmodus hinzugefügt, damit Kunden ihre Arbeit produktiver und sicherer erledigen können. [Mehr dazu](microsoft-edge-configure-kiosk-mode.md#kiosk-mode-supported-features).

- **Das Site List Manager-Tool im Enterprise-Modus ist im Browser über die Seite *edge://compat* verfügbar**. Mit diesem Tool können Sie XML-Site-Listen für den Internet Explorer-Modus unter Microsoft Edge erstellen, bearbeiten und exportieren. Sie können den Zugriff auf dieses Tool nach Bedarf über Gruppenrichtlinien aktivieren. [Mehr dazu](./edge-ie-mode-site-list-manager.md).

- **Verbessern der Browserleistung mit ruhenden Registerkarten**. Das Ruhen von Registerkarten verbessert die Browserleistung, indem inaktive Registerkarten in den Ruhezustand versetzt werden, um Systemressourcen wie Speicher und CPU freizugeben, sodass aktive Registerkarten oder andere Anwendungen sie verwenden können. Benutzer können verhindern, dass Websites in den Ruhezustand versetzt werden, und die Zeitspanne konfigurieren, in der eine inaktive Registerkarte in den Ruhezustand versetzt wird. Um die Benutzer in ihrem Fluss zu halten, gibt es auch [Heuristiken](https://techcommunity.microsoft.com/t5/articles/sleeping-tabs-faq/m-p/1705434), die verhindern, dass bestimmte Websites in den Ruhezustand versetzt werden, z. B. Intranetsites. Diese Funktion kann mit Gruppenrichtlinien verwaltet werden.

  > [!NOTE]
  > „Verbessern der Browserleistung mit ruhenden Registerkarten“ ist ein Update für die Versionshinweise vom 3. Februar für Hauptversion 89.0.774.18.

- **Setzen Sie Ihre Microsoft Edge-Synchronisierungsdaten in der Cloud manuell zurück**. Wir bieten eine Möglichkeit, Ihre Microsoft Edge-Synchronisierungsdaten aus dem Produkt heraus zurückzusetzen. Auf diese Weise wird sichergestellt, dass Ihre Daten aus den Microsoft-Diensten gelöscht werden und bestimmte Produktprobleme behoben werden, für die zuvor ein Support-Ticket erforderlich war.

- **Verbesserungen bei der Textauswahl in PDF-Dokumenten**. Benutzer erhalten eine reibungslosere und konsistentere Textauswahl für PDF-Dokumente, die ab Version 89 in Microsoft Edge geöffnet werden.

- **Das Feld für das Geburtsdatum wird jetzt beim automatischen Ausfüllen unterstützt**. Heute hilft Ihnen Microsoft Edge, Zeit und Mühe beim Ausfüllen von Formularen und beim Erstellen von Online-Konten zu sparen, indem Sie Ihre Daten wie Adressen, Namen, Telefonnummern usw. automatisch ausfüllen. Ab Microsoft Edge Version 89 bieten wir Unterstützung für ein anderes Feld, das Sie gespeichert und automatisch ausgefüllt haben können – das Geburtsdatum. Sie können diese Informationen jederzeit in Ihren Profileinstellungen anzeigen, bearbeiten und löschen.

- **Unterstützung für die Suche in natürlicher Sprache in der Adressleiste, auf der Verlaufssuchseite und im Verlaufshub**. Ab Microsoft Edge Version 89 wird das Auffinden eines Artikels/einer Website durch die Suche in natürlicher Sprache in der Adressleiste, auf der Verlaufsseite und im Verlaufshub einfacher. Benutzer können zusätzlich zu Titeln/URL-Keyword-Übereinstimmungen nach zuvor angesehenem Seiteninhalt/Beschreibung/Timing (z. B. "Kuchenrezept der letzten Woche") suchen. Diese Funktion ist auf eine zufällig ausgewählte Gruppe von Benutzern beschränkt, die das Experimentieren aktiviert haben. Diese Benutzer geben dem Feature-Team Feedback.

### <a name="policy-updates"></a>Richtlinienupdates

#### <a name="new-policies"></a>Neue Richtlinien

- [BrowsingDataLifetime](./microsoft-edge-policies.md#browsingdatalifetime) – Durchsuchen der Einstellungen für die Lebensdauer von Daten
- [MAMEnabled](./microsoft-edge-policies.md#mamenabled) – Mobile App Management aktiviert
- [DefinePreferredLanguages](./microsoft-edge-policies.md#definepreferredlanguages) – Definiert eine geordnete Liste der bevorzugten Sprachen, in denen Websites angezeigt werden sollen, wenn die Website die Sprache unterstützt
- [ShowRecommendationsEnabled](./microsoft-edge-policies.md#showrecommendationsenabled) – Zulassen von Empfehlungen und Werbebenachrichtigungen von Microsoft Edge
- [PrintingAllowedBackgroundGraphicsModes](./microsoft-edge-policies.md#printingallowedbackgroundgraphicsmodes) – Einschränken des Druckmodus für Hintergrundgrafiken
- [PrintingBackgroundGraphicsDefault](./microsoft-edge-policies.md#printingbackgroundgraphicsdefault)– Standard-Druckmodus für Hintergrundgrafiken
- [SmartActionsBlockList](./microsoft-edge-policies.md#smartactionsblocklist)– Blockieren der intelligenten Aktionen für eine Liste von Diensten

#### <a name="obsoleted-policies"></a>Veraltete Richtlinie

- [ForceLegacyDefaultReferrerPolicy](./microsoft-edge-policies.md#forcelegacydefaultreferrerpolicy): Verwenden Sie die standardmäßige Verweiserrichtlinie „kein Verweiser beim Downgrade“
- [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) – Aktivieren Sie die Berichterstellung für Nutzung und Absturz
- [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices)|Senden von Site-Informationen, um die Microsoft-Dienste zu verbessern
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

- **Kioskmodus-Option zum Beenden der Sitzung**. Die Schaltfläche „Sitzung beenden“ ist jetzt im öffentlichen Browsing im Kioskmodus verfügbar. Diese Funktion stellt sicher, dass Browserdaten und -einstellungen gelöscht werden, wenn Microsoft Edge geschlossen wird. Weitere Informationen zu den Funktionen und der Roadmap des Kioskmodus finden Sie unter [Konfigurieren des Microsoft Edge-Kioskmodus](./microsoft-edge-configure-kiosk-mode.md).

- **Sicherheit und Datenschutz:**

  - Benachrichtigungen werden generiert, wenn das Kennwort eines Benutzers in einem Onlineleck gefunden wird. Benutzerkennwörter werden gegen ein Verzeichnis bekannter Anmeldeinformationen überprüft und geben dem Benutzer eine Warnung zurück, wenn eine Übereinstimmung gefunden wird. Um die Sicherheit und den Datenschutz zu gewährleisten, werden Benutzerkennwörter gehashed und verschlüsselt, wenn Sie mit der Datenbank der durchgesickerten Anmeldeinformationen abgeglichen werden.
  - Aktualisieren Sie gemischte Inhalte automatisch. Über HTTPS gelieferte sichere Seiten können Referenzbilder enthalten, die über nicht sicheres HTTP bereitgestellt werden. Um den Datenschutz und die Sicherheit in Microsoft Edge 88 zu verbessern, werden diese Bilder stattdessen über HTTPS abgerufen. Wenn das Bild nicht über HTTPS verfügbar ist, wird es nicht geladen.
  - Anzeigen von Site-Berechtigungen nach Site und nach letzten Aktivitäten. Ab Microsoft Edge 88 können Benutzer Site-Berechtigungen einfacher verwalten. Sie können Berechtigungen nach Website und nicht nur nach Berechtigungstyp anzeigen. Darüber hinaus haben wir einen Abschnitt mit den letzten Aktivitäten hinzugefügt, in dem ein Benutzer alle letzten Änderungen an seinen Websiteberechtigungen anzeigt.
  - Verbesserte Steuerelemente für Browser-Cookies. Ab Microsoft Edge 88 können Benutzer Cookies von Drittanbietern löschen, ohne dass dies Auswirkungen auf Cookies von Drittanbietern hat. Benutzer können ihre Cookies auch nach Erst- oder Drittanbietern filtern und nach Name, Anzahl der Cookies und der Menge der gespeicherten und zuletzt geänderten Daten sortieren.

- **Leistung:**

  - Verbessern Sie die Browserleistung mit Sleeping Tabs. Das Ruhen von Registerkarten verbessert die Browserleistung, indem inaktive Registerkarten in den Ruhezustand versetzt werden, um Systemressourcen wie Speicher und CPU freizugeben, sodass aktive Registerkarten oder andere Anwendungen sie verwenden können. Benutzer können verhindern, dass Websites in den Ruhezustand versetzt werden, und die Zeitspanne konfigurieren, in der eine inaktive Registerkarte in den Ruhezustand versetzt wird. Um die Benutzer in ihrem Fluss zu halten, gibt es auch Heuristiken, die verhindern, dass bestimmte Websites in den Ruhezustand versetzt werden, z. B. Intranetsites. Hinweis: Diese Funktion ist auf eine zufällig ausgewählte Gruppe von Benutzern beschränkt, die das Experimentieren aktiviert haben. Wir planen, das Feature „ruhende Registerkarten“ mit der Version 89 von Microsoft Edge standardmäßig zu aktivieren. Diese Funktion kann mit Gruppenrichtlinien verwaltet werden.
  - Verbessern Sie die Startgeschwindigkeit von Microsoft Edge mit dem Start-Boost. Um die Startgeschwindigkeit von Microsoft Edge zu verbessern, haben wir eine Funktion namens Startup-Boost entwickelt. Durch den Startup-Boost wird der Start von Microsoft Edge beschleunigt, da Microsoft Edge im Hintergrund ausgeführt werden kann. Hinweis: Diese Funktion ist auf eine zufällig ausgewählte Gruppe von Benutzern beschränkt, die das Experimentieren aktiviert haben. Diese Benutzer geben dem Feature-Team Feedback.

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

- [BlockExternalExtensions](./microsoft-edge-policies.md#blockexternalextensions) – Blockieren Sie die Installation externer Erweiterungen.
- [InternetExplorerIntegrationLocalFileAllowed](./microsoft-edge-policies.md#internetexplorerintegrationlocalfileallowed) – Ermöglichen Sie das Starten lokaler Dateien im Internet Explorer-Modus.
- [InternetExplorerIntegrationLocalFileExtensionAllowList](./microsoft-edge-policies.md#internetexplorerintegrationlocalfileextensionallowlist) – Öffnen Sie lokale Dateien im Internet Explorer-Modus.
- [InternetExplorerIntegrationLocalFileShowContextMenu](./microsoft-edge-policies.md#internetexplorerintegrationlocalfileshowcontextmenu) – Leiten Sie das Kontextmenü an, einen Link im Internet Explorer-Modus zu öffnen.
- [IntranetRedirectBehavior](./microsoft-edge-policies.md#intranetredirectbehavior) – Intranet-Umleitungsverhalten.
- [PrinterTypeDenyList](./microsoft-edge-policies.md#printertypedenylist) – Deaktivieren Sie die Druckertypen in der Verweigerungsliste.
- [ShowMicrosoftRewards](./microsoft-edge-policies.md#showmicrosoftrewards) – Zeigen Sie Microsoft Rewards-Erfahrungen an.
- [SleepingTabsEnabled](./microsoft-edge-policies.md#sleepingtabsenabled) – Konfigurieren Sie Sleeping Tabs.
- [SleepingTabsTimeout](./microsoft-edge-policies.md#sleepingtabstimeout) – Legen Sie das Zeitlimit für die Inaktivität der Hintergrundregisterkarte für Sleeping Tabs fest.
- [SleepingTabsBlockedForUrls](./microsoft-edge-policies.md#sleepingtabsblockedforurls) – Blockieren Sie Sleeping Tabs auf bestimmten Websites.
- [StartupBoostEnabled](./microsoft-edge-policies.md#startupboostenabled) – Aktivieren Sie die Startup-Boost.
- [UpdatePolicyOverride](./microsoft-edge-policies.md#updatepolicyoverride) – Gibt an, wie Microsoft Edge Update verfügbare Updates von Microsoft Edge verarbeitet. 
- [VerticalTabsAllowed](./microsoft-edge-policies.md#verticaltabsallowed) – Konfiguriert die Verfügbarkeit eines vertikalen Layouts für Registerkarten an der Seite des Browsers.
- [WebRtcAllowLegacyTLSProtocols](./microsoft-edge-policies.md#webrtcallowlegacytlsprotocols) – Ermöglichen Sie ein älteres TLS/DTLS-Downgrade in WebRTC.

#### <a name="deprecated-policies"></a>Veraltete Richtlinien

Die folgenden Richtlinien sind veraltet.

- [ProactiveAuthEnabled](./microsoft-edge-policies.md#proactiveauthenabled) – Aktivieren Sie die proaktive Authentifizierung.
- [ProxyBypassList](./microsoft-edge-policies.md#proxybypasslist) – Konfigurieren Sie die Proxy-Umgehungsregeln.
- [ProxyMode](./microsoft-edge-policies.md#proxymode) – Konfigurieren Sie die Proxy-Server-Einstellungen.
- [ProxyPacUrl](./microsoft-edge-policies.md#proxypacurl) – Legen Sie die URL der Proxy .pac-Datei fest.
- [Proxyserver](./microsoft-edge-policies.md#proxyserver) – Konfigurieren Sie die Adresse oder URL des Proxyservers.
- [WebDriverOverridesIncompatiblePolicies](./microsoft-edge-policies.md#webdriveroverridesincompatiblepolicies) – Erlauben Sie WebDriver, inkompatible Richtlinien zu überschreiben.

#### <a name="obsoleted-policies"></a>Veraltete Richtlinie

Die folgenden Richtlinien sind veraltet.

- [DefaultPluginsSetting](./microsoft-edge-policies.md#defaultpluginssetting) – Standardeinstellung für Adobe Flash.
- [PluginsAllowedForUrls](./microsoft-edge-policies.md#pluginsallowedforurls) – Lassen Sie das Adobe Flash-Plug-In auf bestimmten Websites zu.
- [PluginsBlockedForUrls](./microsoft-edge-policies.md#pluginsblockedforurls) – Blockieren Sie das Adobe Flash-Plug-in auf bestimmten Websites.
- [RunAllFlashInAllowMode](./microsoft-edge-policies.md#runallflashinallowmode) – Erweitern der Adobe Flash-Inhaltseinstellung auf alle Inhalte.

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

## <a name="version-87066418-october-26"></a>Version 87.0.664.18: 26. Oktober

Verschiedene Bugs und Leistungsprobleme wurden behoben.

<!-- begin major 87 -->
## <a name="version-87066412-october-20"></a>Version 87.0.664.12: 20. Oktober

### <a name="feature-updates"></a>Funktionsupdates

- **Datenschutzfeatures des Kioskmodus aktiviert**. Ab Microsoft Edge, Version 87, werden Kioskmodus-Features aktiviert, die Unternehmen im Zusammenhang mit dem Datenschutz für Benutzerdaten helfen. Diese Features ermöglichen es beispielsweise, dass die Benutzerdaten beim Beenden gelöscht werden, dass heruntergeladene Dateien gelöscht werden und dass die konfigurierte Startumgebung nach einer festgelegten Leerlaufzeitspanne zurückgesetzt wird. Informieren Sie sich genauer zum [Konfigurieren des Microsoft Edge-Kioskmodus](./microsoft-edge-configure-kiosk-mode.md).
- **ClickOnce-Bereitstellung standardmäßig aktiviert**. ClickOnce ist in Microsoft Edge 87 standardmäßig aktiviert, wodurch die Hindernisse für Unternehmen reduziert werden, die Software bereitstellen und mit dem Browserverhalten der Vorgängerversion von Microsoft Edge besser übereinstimmen möchten. Ab Microsoft Edge 87 gibt der Status „Nicht konfiguriert“ der Richtlinie „ClickOnceEnabled“ den neuen standardmäßigen ClickOnce-Status „Aktiviert“ (im Vergleich zum vorherigen Standardstatus „Deaktiviert“) wieder.
- **Auf der Enterprise-Seite „Neue Registerkarte” (New Tab Page, NTP) wird Produktivität in anpassbare, arbeitsrelevante Feedinhalte integriert**. Im Enterprise-NTP-Bereich werden die Office 365-Produktivitätsseite, die wir den mit ihrem Geschäfts-, Schul-oder Unikonto angemeldeten Benutzern bieten, mit personalisierten, arbeitsrelevanten Unternehmens- und Branchenfeeds zusammengeführt, die auf einer einzigen Seite organisiert sind. Benutzer können die vertrauten Office 365-Inhalte und Microsoft Search for Business erkennen, das von Bing unterstützt wird. Darüber hinaus können sie mühelos zu einem anpassbaren „Mein Feed“ mit Inhalten und Modulen, die für den Benutzer, sein Unternehmen oder seine Branche relevant sind, sowie zu einer Auswahl weiterer Feeds wechseln, die von der Organisation zur Verfügung gestellt wurde. [Weitere Informationen](/microsoft-365/admin/manage/manage-industry-news?preserve-view=true&view=o365-worldwide).

- **Datenschutz und Sicherheit:**

  - Unterstützung von TLS-Tokenbindung für mit Richtlinien konfigurierte Websites. Die TLS-Tokenbindung hilft bei der Verhinderung von Angriffen zum Diebstahl von Token, um sicherzustellen, dass Cookies nur auf dem Gerät wiederverwendet werden können, auf dem sie ursprünglich festgelegt wurden. Die Verwendung der TLS-Tokenbindung erfordert es, dass die Richtlinie [AllowTokenBindingForUrls](./microsoft-edge-policies.md#allowtokenbindingforurls) festgelegt wurde und dass die aufgeführten Websites dieses Feature unterstützen.

- **Tastaturunterstützung für Textmarker in PDF-Dateien**. Benutzer können jeden beliebigen Text in einer PDF-Datei mithilfe ihrer Tastatur hervorheben.

- **Drucken:**

  - Wählen Sie die Seite aus, die beim beidseitigen Drucken gedreht werden soll. Benutzer können auswählen, ob ein Blatt beim beidseitigen Drucken auf die lange Seite (Querformat) oder die kurze Seite (Hochformat) gedreht werden soll.
  - Wählen Sie den Druckmodus „Rasterung“ für das Unternehmen aus. Steuern Sie, wie Microsoft Edge auf einem Nicht-PostScript-Drucker unter Windows druckt. Manchmal müssen Druckaufträge bei Nicht-PostScript-Druckern gerastert werden, damit korrekt gedruckt wird. Die Druckoptionen sind „Full" (Vollständig) und „Fast“ (Schnell).

### <a name="policy-updates"></a>Richtlinienupdates

#### <a name="new-policies"></a>Neue Richtlinien

Es wurden zehn neue Richtlinien hinzugefügt. Laden Sie die aktualisierten administrativen Vorlagen von der [Microsoft Edge Enterprise Angebotsseite](https://www.microsoft.com/edge/business/download) herunter. Die folgenden neuen Richtlinien wurden hinzugefügt.

- [ConfigureFriendlyURLFormat](./microsoft-edge-policies.md#configurefriendlyurlformat) – Zum Konfigurieren des Standardformats für das Einfügen von URLs, die aus Microsoft Edge kopiert wurden, und zum Ermitteln, ob Benutzern weitere Formate zur Verfügung stehen.
- [EdgeShoppingAssistantEnabled](./microsoft-edge-policies.md#edgeshoppingassistantenabled) – Shopping in Microsoft Edge aktiviert.
- [HideInternetExplorerRedirectUXForIncompatibleSitesEnabled](./microsoft-edge-policies.md#hideinternetexplorerredirectuxforincompatiblesitesenabled) – Zum Ausblenden des Dialogfelds für einmalige Umleitung und des Banners in Microsoft Edge.
- [KioskAddressBarEditingEnabled](./microsoft-edge-policies.md#kioskaddressbareditingenabled) – Zum Konfigurieren der Adressleistenbearbeitung für Benutzerfreundlichkeit beim öffentlichen Surfen im Kioskmodus.
- [KioskDeleteDownloadsOnExit](./microsoft-edge-policies.md#kioskdeletedownloadsonexit) – Zum Löschen von Dateien, die während einer Kiosksitzung heruntergeladen wurden, wenn Microsoft Edge geschlossen wird.
- [PasswordRevealEnabled](./microsoft-edge-policies.md#passwordrevealenabled) – Zum Aktivieren der Schaltfläche für Kennwortanzeige.
- [RedirectSitesFromInternetExplorerPreventBHOInstall](./microsoft-edge-policies.md#redirectsitesfrominternetexplorerpreventbhoinstall) – Zum Verhindern, dass das BHO (Browserhilfsobjekt) installiert wird, um inkompatible Websites von Internet Explorer zu Microsoft Edge umzuleiten.
- [RedirectSitesFromInternetExplorerRedirectMode](./microsoft-edge-policies.md#redirectsitesfrominternetexplorerredirectmode) – Zum Umleiten inkompatibler Websites von Internet Explorer zu Microsoft Edge.
- [SpeechRecognitionEnabled](./microsoft-edge-policies.md#speechrecognitionenabled) – Zum Konfigurieren der Spracherkennung.
- [WebCaptureEnabled](./microsoft-edge-policies.md#webcaptureenabled) – Zum Aktivieren des Features „Weberfassung“ in Microsoft Edge.

#### <a name="deprecated-policy"></a>Veraltete Richtlinie

[NewTabPageSetFeedType](./microsoft-edge-policies.md#newtabpagesetfeedtype) – Zum Konfigurieren der Microsoft Edge-Oberfläche für neue Registerkartenseiten.

#### <a name="obsoleted-policy"></a>Veraltete Richtlinie

[EnableDeprecatedWebPlatformFeatures](./microsoft-edge-policies.md#enabledeprecatedwebplatformfeatures) – Zum erneuten Aktivieren von veralteten Features für Webplattformen für einen begrenzten Zeitraum.

<!-- end major 87 -->

## <a name="version-86062243-october-16"></a>Version 86.0.622.43: 16. Oktober

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-86062236-october-7"></a>Version 86.0.622.36: 7. Oktober

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-86062231-october-1"></a>Version 86.0.622.31: 1. Oktober

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-86062228-september-28"></a>Version 86.0.622.28: 28. September

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-86062215-september-14"></a>Version 86.0.622.15: 14. September

Verschiedene Bugs und Leistungsprobleme wurden behoben.
<!-- major 86 -->
## <a name="version-86062211-september-9"></a>Version 86.0.622.11: 9. September

### <a name="feature-updates"></a>Funktionsupdates

* **Internet Explorer-Modus:**

   * Ermöglichen Sie Benutzern, die Microsoft Edge-Benutzeroberfläche zum Testen von Websites im Internet Explorer-Modus zu verwenden. Beginnend mit der Microsoft Edge-Version 86 können Administratoren eine Benutzeroberflächenoption für Ihre Benutzer aktivieren, um eine Registerkarte im Internet Explorer-Modus zu Testzwecken oder als Notlösung zu laden, bis Websites zur XML-Websiteliste hinzugefügt werden.

* **Löschen von Downloads von der Festplatte mithilfe des Download-Managers.** Benutzer sind jetzt in der Lage, die heruntergeladenen Dateien von Ihrer Festplatte zu löschen, ohne den Browser verlassen zu müssen. Die neue Funktion zum Löschen von Downloads befindet sich im Kontextmenü des Downloadverzeichnisses oder der Downloadseite.

* **Zurücksetzen zur vorherigen Microsoft Edge-Version.** Mit der Rollback-Funktion können Administratoren auf eine Ihnen bekannte gute Version von Microsoft Edge zurückgreifen, wenn ein Problem in der neuesten Version von Microsoft Edge auftritt.
[Weitere Informationen](edge-learnmore-rollback.md).

* **Erzwingen der standardmäßigen Aktivierung der Synchronisierung im gesamten Unternehmen.**  Administratoren können die Synchronisierung für Azure Active Directory-Konten (Azure AD) standardmäßig mit der [ForceSync](./microsoft-edge-policies.md#forcesync)-Richtlinie aktivieren.

* **PDF-Updates:**

  * Inhaltsverzeichnis für PDF-Dokumente. Ab Version 86 hat Microsoft Edge Unterstützung für das Inhaltsverzeichnis hinzugefügt, das es Benutzern ermöglicht, einfach durch PDF-Dokumente zu navigieren.
  * Zugriff auf alle PDF-Funktionalitäten auf Bildschirmen mit kleinem Formfaktor. Zugriff auf alle Funktionen des Microsoft Edge PDF-Readers auf Geräten mit kleinen Bildschirmgrößen.
  * Stiftunterstützung für Textmarker in PDF-Dateien. Mit diesem Update können Benutzer mit ihrem digitalen Stift Text in PDF-Dateien direkt markieren, so wie sie es auch mit einem physischen Textmarker und Papier tun würden.
  * Verbessertes Scrollen im PDF-Format. Das Scrollen durch lange PDF-Dokumente kann jetzt ohne Ruckeln erlebt werden.

* **Automatischer Profilwechsel unter Windows 7, 8 und 8.1.** Der zurzeit in Microsoft Edge unter Windows 10 verfügbare automatische Profilwechsel wird auf Vorgängerversionen (Windows 7, 8 und 8.1) erweitert. Weitere Informationen finden Sie im Blogbeitrag [Automatischer Profilwechsel](https://blogs.windows.com/msedgedev/2020/04/30/automatic-profile-switching/).

* **Benutzer sehen Vorschläge zur automatischen Vervollständigung, wenn sie mit der Eingabe einer Suchanfrage auf der Microsoft Edge Add-ons-Website beginnen.** Die automatische Vervollständigung hilft Benutzern, Ihre Suchabfrage schnell zu vervollständigen, ohne die gesamte Zeichenfolge eingeben zu müssen. Dies ist hilfreich, da sich die Benutzer keine korrekten Schreibweisen merken müssen, und Sie können aus den verfügbaren Optionen auswählen, die angezeigt werden.

* **Entfernen der Cache-API für HTML5-Anwendungen.**  Beginnend mit der Microsoft Edge-Version 86, wird die veraltete Anwendungs-Cache-API, die die Offline-Nutzung von Webseiten ermöglicht, von Microsoft Edge entfernt. Webentwickler sollten sich die [WebDev-Dokumentation](https://web.dev/appcache-removal/) ansehen, um Informationen zum Ersetzen der Anwendungs-Cache-API durch Service Worker zu erhalten.  Wichtig: Sie können einen [AppCache OriginTrial-Token](https://developers.chrome.com/origintrials/#/view_trial/1776670052997660673) anfordern, der es Websites ermöglicht, die veraltete Anwendungs-Cache-API weiterhin bis zur Microsoft Edge-Version 90 zu verwenden.

* **Sicherheit:**

  * Unterstützung für sicheres DNS (DNS-over-HTTPS).  Ab der Microsoft Edge-Version 86 stehen Einstellungen zum Steuern des sicheren DNS auf nicht verwalteten Geräten zur Verfügung. Diese Einstellungen sind für Benutzer auf verwalteten Geräten nicht zugänglich, aber IT-Administratoren können sicheres DNS aktivieren oder deaktivieren, indem Sie die Gruppenrichtlinie [dnsoverhttpsmode](./microsoft-edge-policies.md#dnsoverhttpsmode) verwenden.


* **Hinzufügen eines benutzerdefiniertes Bildes zur Seite „Neue Registerkarte“ (New Tab Page, NTP) mithilfe einer Gruppenrichtlinie.** Beginnend mit der Microsoft Edge-Version 86 bietet die NTP die Möglichkeit, das Standardbild durch ein benutzerdefiniertes Bild zu ersetzen. Die Möglichkeit, die Eigenschaften dieses Bilds zu verwalten, wird auch von der Gruppenrichtlinie unterstützt.

* **Anpassen von benutzerdefinierten Tastenkombinationen an VS Code.** Microsoft Edge DevTools unterstützt jetzt die Anpassung von Tastenkombinationen in DevTools mit Ihrem Editor/Ihrer IDE. (In Microsoft Edge 84 wurde die Möglichkeit hinzugefügt, DevTools-Tastenkombinationen mit VS Code abzugleichen).

* **Ersetzen der Richtlinien [MetricsReportingEnabled]( /DeployEdge/microsoft-edge-policies#metricsreportingenabled) und [SendSiteInformationToImproveServices]( /DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices) für Vorgängerversionen von Windows und macOS.** Diese Richtlinien sind in der Microsoft Edge-Version 86 veraltet und werden in der Microsoft Edge-Version 89 überholt sein.<br>
Diese Richtlinien werden ersetzt durch [Telemetrie zulassen](/windows/privacy/configure-windows-diagnostic-data-in-your-organization) unter Windows 10 sowie die neue [DiagnosticData](./microsoft-edge-policies.md#diagnosticdata)-Richtlinie für alle anderen Plattformen. Dadurch können Benutzer die Diagnosedaten verwalten, die an Microsoft für Windows 7, 8, 8.1 und macOS gesendet werden.

* **"SameSite=Lax" für Cookies (Standard)**. Zur Verbesserung der Websicherheit und des Datenschutzes verwenden Cookies jetzt standardmäßig die [SameSite = Lax](https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie/SameSite)-Behandlung. Dies bedeutet, dass Cookies nur in einem Erstanbieterkontext gesendet werden und bei an Dritte gesendeten Anforderungen weggelassen werden. Diese Änderung kann Auswirkungen auf die Kompatibilität von Websites haben, die Cookies von Drittanbietern benötigen, damit Ressourcen die korrekt funktionieren. Um solche Cookies zuzulassen, können Webentwickler Cookies markieren, die aus Drittanbieterkontext gesetzt und an Drittanbieterkontext gesendet werden sollen, indem sie beim Setzen des Cookies explizit die Attribute `SameSite=none` und `Secure` hinzufügen. Unternehmen, die bestimmte Sites von dieser Änderung ausnehmen möchten, können dies mit der Richtlinie [LegacySameSiteCookieBehaviorEnabledForDomainList](./microsoft-edge-policies.md#legacysamesitecookiebehaviorenabledfordomainlist) tun oder die Änderung für alle Sites mit der Richtlinie [LegacySameSiteCookieBehaviorEnabled](./microsoft-edge-policies.md#legacysamesitecookiebehaviorenabled) ablehnen.

### <a name="policy-updates"></a>Richtlinienupdates

#### <a name="new-policies"></a>Neue Richtlinien

Es wurden neunzehn neue Richtlinien hinzugefügt. Laden Sie die aktualisierten administrativen Vorlagen von der [Microsoft Edge Enterprise Angebotsseite](https://aka.ms/EdgeEnterprise) herunter. Die folgenden neuen Richtlinien wurden hinzugefügt.

- [CollectionsServicesAndExportsBlockList](./microsoft-edge-policies.md#collectionsservicesandexportsblocklist): Blockieren des Zugriffs auf eine bestimmte Liste von Diensten und Exportieren von Zielen in Sammlungen.
- [DefaultSensorsSetting](./microsoft-edge-policies.md#defaultsensorssetting): Standardeinstellung für Sensoren.
- [DefaultSerialGuardSetting](./microsoft-edge-policies.md#defaultserialguardsetting): Steuerung der Verwendung der Serial-API.
- [DiagnosticData](./microsoft-edge-policies.md#diagnosticdata): Senden der erforderlichen und optionalen Diagnosedaten zur Browsernutzung.
- [EnterpriseModeSiteListManagerAllowed](./microsoft-edge-policies.md#enterprisemodesitelistmanagerallowed): Zugriff auf das Tool Enterprise Mode Site List Manager zulassen.
- [ForceSync](./microsoft-edge-policies.md#forcesync): Synchronisierung von Browserdaten erzwingen und Zustimmungsaufforderung für die Synchronisierung nicht anzeigen.
- [InsecureFormsWarningsEnabled](./microsoft-edge-policies.md#insecureformswarningsenabled): Aktivieren von Warnungen für unsichere Formulare.
- [InternetExplorerIntegrationTestingAllowed](./microsoft-edge-policies.md#internetexplorerintegrationtestingallowed): Internet Explorer-Modus-Tests zulassen.
- [SpotlightExperiencesAndRecommendationsEnabled](./microsoft-edge-policies.md#spotlightexperiencesandrecommendationsenabled): Wählen Sie aus, ob Benutzer personalisierte Hintergrundbilder und Text, Vorschläge, Benachrichtigungen und Tipps für Microsoft-Dienste erhalten können.
- [NewTabPageAllowedBackgroundTypes](./microsoft-edge-policies.md#newtabpageallowedbackgroundtypes): Konfigurieren der zulässigen Hintergrundtypen für das neue Registerkartenseiten-Layout.
- [SaveCookiesOnExit](./microsoft-edge-policies.md#savecookiesonexit): Speichern Sie Cookies, wenn Microsoft Edge geschlossen wird.
- [SensorsAllowedForUrls](./microsoft-edge-policies.md#sensorsallowedforurls): Zugriff auf Sensoren auf bestimmten Websites zulassen.
- [SensorsBlockedForUrls](./microsoft-edge-policies.md#sensorsblockedforurls): Zugriff auf Sensoren auf bestimmten Websites blockieren.
- [SerialAskForUrls](./microsoft-edge-policies.md#serialaskforurls): Die Serial-API auf bestimmten Websites zulassen.
- [SerialBlockedForUrls](./microsoft-edge-policies.md#serialblockedforurls): Die Serial-API auf bestimmten Websites blockieren.
- [URLBlocklist](./microsoft-edge-policies.md#urlblocklist): Blockieren des Zugriffs auf eine Liste von URLs.
- [URLAllowlist](./microsoft-edge-policies.md#urlallowlist): Definieren einer Liste zulässiger URLs.
- [UserAgentClientHintsEnabled](./microsoft-edge-policies.md#useragentclienthintsenabled): Aktivieren der Funktion User-Agent Client Hints.
- [UserDataSnapshotRetentionLimit](./microsoft-edge-policies.md#userdatasnapshotretentionlimit): Schränkt die Anzahl der Benutzerdaten-Momentaufnahmen ein, die zur Verwendung für Notfall-Rollbacks aufbewahrt werden.

#### <a name="deprecated-policies"></a>Veraltete Richtlinien

- [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled): Aktivieren der Berichterstellung für Nutzungs- und Absturzdaten.
- [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices): Senden von Siteinformationen, um Microsoft-Dienste zu verbessern.

#### <a name="obsoleted-policy"></a>Veraltete Richtlinie

[TLS13HardeningForLocalAnchorsEnabled](./microsoft-edge-policies.md#tls13hardeningforlocalanchorsenabled): Aktivieren Sie das TLS 1.3-Sicherheitsfeature für lokale Vertrauensanker.

#### <a name="policy-caption-changed"></a>Richtlinienüberschrift geändert

[NativeWindowOcclusionEnabled](./microsoft-edge-policies.md#nativewindowocclusionenabled): Native Window Occlusion aktivieren.

#### <a name="policy-description-changed"></a>Richtlinienbeschreibung geändert

- [AdsSettingForIntrusiveAdsSites](./microsoft-edge-policies.md#adssettingforintrusiveadssites)
- [AllowTokenBindingForUrls](./microsoft-edge-policies.md#allowtokenbindingforurls)
- [AmbientAuthenticationInPrivateModesEnabled](./microsoft-edge-policies.md#ambientauthenticationinprivatemodesenabled)
- [ApplicationGuardContainerProxy](./microsoft-edge-policies.md#applicationguardcontainerproxy)
- [AutoImportAtFirstRun](./microsoft-edge-policies.md#autoimportatfirstrun)
- [AutoOpenFileTypes](./microsoft-edge-policies.md#autoopenfiletypes)
- [BrowserSignin](./microsoft-edge-policies.md#browsersignin)
- [ClearBrowsingDataOnExit](./microsoft-edge-policies.md#clearbrowsingdataonexit) 
- [ClickOnceEnabled](./microsoft-edge-policies.md#clickonceenabled)
- [CommandLineFlagSecurityWarningsEnabled](./microsoft-edge-policies.md#commandlineflagsecuritywarningsenabled)
- [ConfigureOnPremisesAccountAutoSignIn](./microsoft-edge-policies.md#configureonpremisesaccountautosignin)
- [ConfigureShare](./microsoft-edge-policies.md#configureshare)
- [CookiesAllowedForUrls](./microsoft-edge-policies.md#cookiesallowedforurls)
- [CustomHelpLink](./microsoft-edge-policies.md#customhelplink)
- [DefaultCookiesSetting](./microsoft-edge-policies.md#defaultcookiessetting)
- [DefaultGeolocationSetting](./microsoft-edge-policies.md#defaultgeolocationsetting)
- [DefaultImagesSetting](./microsoft-edge-policies.md#defaultimagessetting)
- [DefaultInsecureContentSetting](./microsoft-edge-policies.md#defaultinsecurecontentsetting)
- [DefaultJavaScriptSetting](./microsoft-edge-policies.md#defaultjavascriptsetting)
- [DefaultNotificationsSetting](./microsoft-edge-policies.md#defaultnotificationssetting)
- [DefaultPluginsSetting](./microsoft-edge-policies.md#defaultpluginssetting)
- [DefaultPopupsSetting](./microsoft-edge-policies.md#defaultpopupssetting)
- [DefaultSearchProviderEnabled](./microsoft-edge-policies.md#defaultsearchproviderenabled)
- [DefaultWebBluetoothGuardSetting](./microsoft-edge-policies.md#defaultwebbluetoothguardsetting)
- [DefaultWebUsbGuardSetting](./microsoft-edge-policies.md#defaultwebusbguardsetting)
- [DelayNavigationsForInitialSiteListDownload](./microsoft-edge-policies.md#delaynavigationsforinitialsitelistdownload)
- [DeveloperToolsAvailability](./microsoft-edge-policies.md#developertoolsavailability)
- [EnableSha1ForLocalAnchors](./microsoft-edge-policies.md#enablesha1forlocalanchors)
- [DownloadRestrictions](./microsoft-edge-policies.md#downloadrestrictions)
- [EnableDeprecatedWebPlatformFeatures](./microsoft-edge-policies.md#enabledeprecatedwebplatformfeatures)
- [WinHttpProxyResolverEnabled](./microsoft-edge-policies.md#winhttpproxyresolverenabled)
- [ExperimentationAndConfigurationServiceControl](./microsoft-edge-policies.md#experimentationandconfigurationservicecontrol)
- [ExternalProtocolDialogShowAlwaysOpenCheckbox](./microsoft-edge-policies.md#externalprotocoldialogshowalwaysopencheckbox)
- [ExtensionInstallForcelist](./microsoft-edge-policies.md#extensioninstallforcelist)
- [ForceBingSafeSearch](./microsoft-edge-policies.md#forcebingsafesearch)
- [ForceYouTubeRestrict](./microsoft-edge-policies.md#forceyoutuberestrict)
- [HomepageIsNewTabPage](./microsoft-edge-policies.md#homepageisnewtabpage)
- [HomepageLocation](./microsoft-edge-policies.md#homepagelocation)
- [InPrivateModeAvailability](./microsoft-edge-policies.md#inprivatemodeavailability)
- [InternetExplorerIntegrationEnhancedHangDetection](./microsoft-edge-policies.md#internetexplorerintegrationenhancedhangdetection)
- [InternetExplorerIntegrationLevel](./microsoft-edge-policies.md#internetexplorerintegrationlevel)
- [InternetExplorerIntegrationSiteRedirect](./microsoft-edge-policies.md#internetexplorerintegrationsiteredirect)
- [LegacySameSiteCookieBehaviorEnabled](./microsoft-edge-policies.md#legacysamesitecookiebehaviorenabled)
- [NativeWindowOcclusionEnabled](./microsoft-edge-policies.md#nativewindowocclusionenabled)
- [NavigationDelayForInitialSiteListDownloadTimeout](./microsoft-edge-policies.md#navigationdelayforinitialsitelistdownloadtimeout)
- [NetworkPredictionOptions](./microsoft-edge-policies.md#networkpredictionoptions)
- [NewTabPageLocation](./microsoft-edge-policies.md#newtabpagelocation)
- [NewTabPageSearchBox](./microsoft-edge-policies.md#newtabpagesearchbox)
- [NewTabPageSetFeedType](./microsoft-edge-policies.md#newtabpagesetfeedtype)
- [NonRemovableProfileEnabled](./microsoft-edge-policies.md#nonremovableprofileenabled)
- [PasswordProtectionWarningTrigger](./microsoft-edge-policies.md#passwordprotectionwarningtrigger)
- [PasswordProtectionLoginURLs](./microsoft-edge-policies.md#passwordprotectionloginurls)
- [PasswordProtectionChangePasswordURL](./microsoft-edge-policies.md#passwordprotectionchangepasswordurl)
- [PluginsAllowedForUrls](./microsoft-edge-policies.md#pluginsallowedforurls)
- [PluginsBlockedForUrls](./microsoft-edge-policies.md#pluginsblockedforurls)
- [PreventSmartScreenPromptOverride](./microsoft-edge-policies.md#preventsmartscreenpromptoverride)
- [PreventSmartScreenPromptOverrideForFiles](./microsoft-edge-policies.md#preventsmartscreenpromptoverrideforfiles)
- [ProxyMode](./microsoft-edge-policies.md#proxymode)
- [RegisteredProtocolHandlers](./microsoft-edge-policies.md#registeredprotocolhandlers)
- [RelaunchNotification](./microsoft-edge-policies.md#relaunchnotification)
- [RestoreOnStartup](./microsoft-edge-policies.md#restoreonstartup)
- [RestoreOnStartupURLs](./microsoft-edge-policies.md#restoreonstartupurls)
- [RestrictSigninToPattern](./microsoft-edge-policies.md#restrictsignintopattern)
- [SSLVersionMin](./microsoft-edge-policies.md#sslversionmin)
- [SmartScreenAllowListDomains](./microsoft-edge-policies.md#smartscreenallowlistdomains)
- [SmartScreenEnabled](./microsoft-edge-policies.md#smartscreenenabled)
- [SmartScreenForTrustedDownloadsEnabled](./microsoft-edge-policies.md#smartscreenfortrusteddownloadsenabled)
- [SmartScreenPuaEnabled](./microsoft-edge-policies.md#smartscreenpuaenabled)
- [SyncTypesListDisabled](./microsoft-edge-policies.md#synctypeslistdisabled)
- [TrackingPrevention](./microsoft-edge-policies.md#trackingprevention)
- [WebRtcLocalhostIpHandling](./microsoft-edge-policies.md#webrtclocalhostiphandling)

<!-- end 86 -->

## <a name="version-85056441-august-25"></a>Version 85.0.564.41: August 25

Verschiedene Bugs und Leistungsprobleme wurden behoben.

## <a name="version-85056440-august-21"></a>Version 85.0.564.40: 21. August

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-85056436-august-17"></a>Version 85.0.564.36: 17. August

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-85056430-august-10"></a>Version 85.0.564.30: 10. August

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-85056423-august-3"></a>Version 85.0.564.23: 3. August

Verschiedene Bugs und Leistungsprobleme wurden behoben.
<!-- major 85 -->
## <a name="version-85056418-july-28"></a>Version 85.0.564.18: 28. Juli

### <a name="feature-updates"></a>Funktionsupdates

- **Lokale Synchronisierung von Favoriten und Einstellungen**. Jetzt können Sie Browser-Favoriten und -Einstellungen zwischen Active Directory-Profilen in Ihrer eigenen Umgebung synchronisieren, ohne dass eine Cloud-Synchronisierung erforderlich ist.

- **Unterstützung von Microsoft Edge-Gruppenrichtlinien zum Starten vertrauenswürdiger Website und App-Combos ohne Bestätigungsaufforderung.** Unterstützung von Gruppenrichtlinien hinzugefügt, mit denen Administratoren Website + App-Combos hinzufügen können, die vertrauenswürdig sind und deshalb ohne Bestätigungsaufforderung gestartet werden können. Dadurch wird die Möglichkeit für Administratoren hinzugefügt, vertrauenswürdige Protokoll-/Herkunftskombinationen (z. B. Microsoft 365-Apps) für ihre Endbenutzer zu konfigurieren, um die Bestätigungsaufforderung zu unterdrücken, wenn sie zu einer URL navigieren, die ein App-Protokoll enthält.

- **PDF-Textmarker-Tool**. Dieses Tool kann zur Symbolleiste für PDFs hinzugefügt werden, um wichtigen Text auf einfache Weise hervorzuheben.

- **Die Storage Access-API ist jetzt verfügbar**. Die Storage Access-API ermöglicht den Zugriff auf Erstanbieter-Speicher in einem Drittanbieter-Kontext, wenn ein Benutzer die Absicht bekundet hat, Speicher zuzulassen, der andernfalls durch die aktuelle Konfiguration des Browsers blockiert würde. Weitere Informationen finden Sie unter [Storage Access-API](https://www.chromestatus.com/feature/5612590694662144).

- **"An OneNote senden" ist für Microsoft Edge-Sammlungen verfügbar**. Alle freuen sich, in Sammlungen gesammelte Informationen an OneNote senden zu können, wo sie sie an ein größeres Projekt anfügen und mit anderen zusammenarbeiten können. Noch wichtiger ist, dass Sie in Microsoft Edge 85 Inhalte an *Office für Mac-*-Produkte (Word, Excel und OneNote) für Microsoft-Konto und Azure Active Directory senden können.

- **DevTools-Updates**. Ausführliche Informationen zu den folgenden Updates finden Sie unter [Neuerungen in DevTools (Microsoft Edge 85)](/microsoft-edge/devtools-guide-chromium/whats-new/2020/06/devtools).

   - Microsoft Edge DevTools unterstützt Surface Duo-Emulation. Die Microsoft Edge-DevTools können das Surface Duo emulieren, sodass Sie testen können, wie Ihre Webinhalte auf Dual-Screen-Geräten aussehen werden. Um dieses Experiment in DevTools zu aktivieren, drücken Sie STRG+UMSCHALT+M unter Windows oder CMD+UMSCHALT+M unter macOS, und wählen Sie dann Surface Duo aus der Dropdownliste der Geräte aus.
   - Mit Microsoft Edge DevTools können Sie Tastenkombinationen mit VS Code abgleichen. Microsoft Edge DevTools unterstützt die Anpassung von Tastenkombinationen in DevTools an Ihren Editor/Ihre IDE. In Microsoft Edge 85 wurde die Möglichkeit hinzugefügt, DevTools-Tastenkombinationen mit VS Code abzugleichen. Diese Änderung wird zur Produktivität in VS Code und DevTools beitragen.

### <a name="policy-updates"></a>Richtlinienupdates

#### <a name="new-policies"></a>Neue Richtlinien

Es wurden dreizehn neue Richtlinien hinzugefügt. Laden Sie die aktualisierten administrativen Vorlagen von der [Microsoft Edge Enterprise Angebotsseite](https://aka.ms/EdgeEnterprise) herunter. Die folgenden neuen Richtlinien wurden hinzugefügt.

- [AutoLaunchProtocolsFromOrigins](./microsoft-edge-policies.md#autolaunchprotocolsfromorigins): Eine Liste der Protokolle definieren, mit denen eine externe Anwendung von den aufgeführten Ursprüngen aus ohne Aufforderung an den Benutzer gestartet werden kann.
- [AutoOpenAllowedForURLs](./microsoft-edge-policies.md#autoopenallowedforurls): URLs, auf die AutoOpenFileTypes angewendet werden kann.
- [AutoOpenFileTypes](./microsoft-edge-policies.md#autoopenfiletypes): Liste der Dateitypen, die beim Download automatisch geöffnet werden sollen.
- [DefaultSearchProviderContextMenuAccessAllowed](./microsoft-edge-policies.md#defaultsearchprovidercontextmenuaccessallowed): Suchzugriff auf Kontextmenü des standardmäßigen Suchdienstanbieters zulassen.
- [EnableSha1ForLocalAnchors](./microsoft-edge-policies.md#enablesha1forlocalanchors): Zulassen von Zertifikaten, die mit SHA-1 signiert wurden, wenn sie von lokalen Vertrauensankern ausgegeben wurden.
- [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](./microsoft-edge-policies.md#exemptdomainfiletypepairsfromfiletypedownloadwarnings): Deaktivieren von auf Dateierweiterungen basierenden Download-Warnungen für bestimmte Dateitypen in Domänen.
- [IntensiveWakeUpThrottlingEnabled](./microsoft-edge-policies.md#intensivewakeupthrottlingenabled): Steuern des IntensiveWakeUpThrottling-Features.
- [NewTabPagePrerenderEnabled](./microsoft-edge-policies.md#newtabpageprerenderenabled): Aktivieren des Vorabladens der „Neuer Tab“-Seite für schnellere Darstellung.
- [NewTabPageSearchBox](./microsoft-edge-policies.md#newtabpagesearchbox): Konfigurieren der Suchfeldfunktion der „Neuer Tab“-Seite.
- [PasswordMonitorAllowed](./microsoft-edge-policies.md#passwordmonitorallowed): Benutzern ermöglichen, benachrichtigt zu werden, wenn ihre Kennwörter als unsicher eingestuft wurden.
- [RoamingProfileSupportEnabled](./microsoft-edge-policies.md#roamingprofilesupportenabled): Aktivieren der Verwendung von Roaming-Kopien für Microsoft Edge-Profildaten.
- [RoamingProfileLocation](./microsoft-edge-policies.md#roamingprofilelocation): Festlegen des Verzeichnisses für servergespeicherte Profile.
- [TLSCipherSuiteDenyList](./microsoft-edge-policies.md#tlsciphersuitedenylist): Angeben der zu deaktivierenden TLS-Verschlüsselungssammlungen.

#### <a name="obsoleted-policies"></a>Veraltete Richtlinie

- [EnableDomainActionsDownload](./microsoft-edge-policies.md#enabledomainactionsdownload): Herunterladen von Domänenaktionen von Microsoft aktivieren.
- [WebComponentsV0Enabled](./microsoft-edge-policies.md#webcomponentsv0enabled) – Erneutes Aktivieren der Web Components v0-API bis M84.
- [WebDriverOverridesIncompatiblePolicies](./microsoft-edge-policies.md#webdriveroverridesincompatiblepolicies): Zulassen, dass WebDriver inkompatible Richtlinien außer Kraft setzt.

<!--- END ---->

## <a name="version-84052235-july-9"></a>Version 84.0.522.35: 9. Juli

Verschiedene Bugs und Leistungsprobleme wurden behoben.

## <a name="version-84052228-june-26"></a>Version 84.0.522.28: 26. Juni

Verschiedene Bugs und Leistungsprobleme wurden behoben.

## <a name="version-84052226-june-24"></a>Version 84.0.522.26: 24. Juni

Verschiedene Bugs und Leistungsprobleme wurden behoben.

## <a name="version-84052220-june-15"></a>Version 84.0.522.20: 15. Juni

Verschiedene Bugs und Leistungsprobleme wurden behoben.

## <a name="version-84052215-june-8"></a>Version 84.0.522.15: 8. Juni

Verschiedene Bugs und Leistungsprobleme wurden behoben.

## <a name="version-84052211-june-2"></a>Version 84.0.522.11: 2. Juni

### <a name="feature-updates"></a>Funktionsupdates

- Diese Version von Microsoft Edge bietet verbesserte Downloadzeiten für Websitelisten im Internet Explorer-Modus.  Wir haben die Downloadverzögerung für die Websiteliste im Internet Explorer-Modus auf 0 Sekunden verringert (von einer ursprünglichen Wartezeit von 60 Sekunden), wenn keine zwischengespeicherte Websiteliste vorhanden ist. Wir haben auch die Unterstützung von Gruppenrichtlinien für Fälle hinzugefügt, in denen Startseitennavigationen im Internet Explorer-Modus verzögert werden müssen, bis die Websiteliste heruntergeladen wurde. Weitere Informationen hierzu finden Sie in der [DelayNavigationsForInitialSiteListDownload](./microsoft-edge-policies.md#delaynavigationsforinitialsitelistdownload)-Richtlinie.

- Microsoft Edge ermöglicht es Benutzern nun, sich beim Browser anzumelden, wenn er unter Windows 10 „als Administrator ausgeführt“ wird. Dies hilft Kunden, die Microsoft Edge auf Windows Server oder in Remotedesktop- und Sandbox-Szenarien auszuführen.

- Microsoft Edge bietet nun vollständige Mausunterstützung im Vollbildmodus. Jetzt können Sie mit der Maus auf Registerkarten, die Adressleiste und andere Elemente zugreifen, ohne den Vollbildmodus zu verlassen.

- Verbesserung für Onlinekäufe. Sie können benutzerdefinierte Spitznamen zu gespeicherten Debit- oder Kreditkarten hinzufügen. Jetzt können Sie zwischen Ihren Kreditkarten unterscheiden, wenn Sie Onlinekäufe tätigen. Wenn Sie Ihren Debit- oder Kreditkarten Spitznamen zuordnen, können Sie leichter die richtige Karte wählen, wenn Sie zur Auswahl der Zahlungsmethode die Funktion zum automatischen Ausfüllen verwenden.

- TLS/1.0 und TLS/1.1 sind standardmäßig deaktiviert. Um betroffene Websites leichter zu erkennen, können Sie die Kennzeichnung *edge://flags/#display-legacy-tls-warnings* so festlegen, dass Microsoft Edge beim Laden von Seiten, die veraltete TLS-Protokolle erfordern, eine nicht blockierende "Nicht sicher"-Benachrichtigung anzeigt. Die [SSLVersionMin](./microsoft-edge-policies.md#sslversionmin)-Richtlinie ermöglicht die erneute Aktivierung von TLS/1.0 und TLS/1.1. Diese Richtlinie bleibt mindestens bis zur Microsoft Edge-Version 88 verfügbar. Weitere Informationen finden Sie unter [Websitekompatibilität – Auswirkungen von Änderungen an Microsoft Edge](/microsoft-edge/web-platform/site-impacting-changes).

- Verbesserungen an "Sammlungen":

  - Es wurde eine Notizfunktion hinzugefügt, mit der Sie einem Element in einer Sammlung eine Notiz oder einen Kommentar hinzufügen können. Notizen werden gruppiert und bleiben an einen Eintrag angefügt, auch wenn Sie die Elemente in einer Sammlung sortieren. Klicken Sie zum Testen des neuen Features mit der rechten Maustaste auf ein Element, und wählen Sie "Notiz hinzufügen" aus.
  - Die Hintergrundfarbe von Notizen in Sammlungen kann geändert werden. Sie können Farbcodierung verwenden, um Informationen zu organisieren und Ihre Produktivität zu steigern.
  - Es gibt deutliche Verbesserungen bei der Leistung, dank derer Sie Ihre Sammlungen schneller als in früheren Versionen von Microsoft Edge nach Excel exportieren können.

- Zusätzliche Unterstützung von Microsoft Edge-APIs:

  - Die Storage Access-API. Diese API ermöglicht den Zugriff auf Erstanbieter-Speicher in einem Drittanbieter-Kontext, wenn ein Benutzer die Absicht bekundet, Speicher zuzulassen, der andernfalls durch die aktuelle Konfiguration des Browsers blockiert würde.

    Da der Datenschutz für die Benutzer immer wichtiger wird, wird die Forderung strengerer Browser-Standardeinstellungen und Opt-in-Einstellungen für Benutzer wie das Blockieren des Zugriffs auf Drittanbieter-Speicher immer verbreiteter. Diese Einstellungen tragen dazu bei, den Datenschutz zu verbessern und den unbefugten Zugriff durch unbekannte oder nicht vertrauenswürdige Parteien zu verhindern. Sie können jedoch auch unerwünschte Nebeneffekte haben wie z. B. das Blockieren des Zugriffs auf Inhalte, die der Benutzer anzeigen möchte (z. B. soziale Medien und eingebettete Medieninhalte).

  - Die Native File System-API ermöglicht es Ihnen, Websiteberechtigungen zum Bearbeiten von Dateien oder Ordnern zu erteilen.

- PDF-Verbesserungen:

  - "Laut vorlesen" für PDF ermöglicht Benutzern das Anhören von PDF-Inhalten, während sie andere wichtige Aufgaben ausführen. Außerdem hilft die Funktion audiovisuell Lernenden beim Lesen von Inhalten, wodurch das Lernen erleichtert wird.
  - Die Funktion zum Bearbeiten von PDF-Dateien wurde verbessert. Jetzt können Sie eine an einer PDF-Datei vorgenommene Bearbeitung direkt in der Datei speichern, anstatt dass jedes Mal, wenn Sie das PDF bearbeiten, eine Kopie erstellt wird.

- Microsoft Edge ermöglicht jetzt die Übersetzung im plastischen Reader. Wenn ein Benutzer eine Seite im plastischen Reader öffnet, kann er auswählen, ob sie in seine gewünschte Sprache übersetzt werden soll.

- DevTools unterstützt die Anpassung von Tastenkombinationen an Ihren Editor/Ihre IDE, einschließlich VS Code.

### <a name="policy-updates"></a>Richtlinienupdates

#### <a name="new-policies"></a>Neue Richtlinien

Es wurden fünf neue Richtlinien hinzugefügt. Laden Sie die aktualisierten administrativen Vorlagen von der [Microsoft Edge Enterprise Angebotsseite](https://aka.ms/EdgeEnterprise) herunter. Die folgenden neuen Richtlinien wurden hinzugefügt.

- [AppCacheForceEnabled](./microsoft-edge-policies.md#appcacheforceenabled) – Ermöglicht die Wiederaktivierung des AppCache-Features, auch wenn es standardmäßig deaktiviert ist.
- [ApplicationGuardContainerProxy](./microsoft-edge-policies.md#applicationguardcontainerproxy) – Application Guard-Containerproxy.
- [DelayNavigationsForInitialSiteListDownload](./microsoft-edge-policies.md#delaynavigationsforinitialsitelistdownload) – Voraussetzen, dass die Enterprise Mode Site List vor der Registerkartennavigation verfügbar ist.
- [NativeWindowOcclusionEnabled](./microsoft-edge-policies.md#nativewindowocclusionenabled) – Aktivieren des Ausblendens nativer Fenster.
- [NavigationDelayForInitialSiteListDownloadTimeout](./microsoft-edge-policies.md#navigationdelayforinitialsitelistdownloadtimeout): Festlegen eines Zeitlimits für die Verzögerung der Tabnavigation für die Websiteliste für den Unternehmensmodus.

#### <a name="deprecated-policies"></a>Veraltete Richtlinien

- [AllowSyncXHRInPageDismissal](./microsoft-edge-policies.md#allowsyncxhrinpagedismissal): Seiten das Senden synchroner XHR-Anforderungen während der Seitenschließung ermöglichen.
- [BuiltinCertificateVerifierEnabled](./microsoft-edge-policies.md#builtincertificateverifierenabled) – Bestimmt, ob die integrierte Zertifikatprüfung zum Überprüfen von Serverzertifikaten verwendet wird.
- [StricterMixedContentTreatmentEnabled](./microsoft-edge-policies.md#strictermixedcontenttreatmentenabled): Aktivieren Sie die striktere Behandlung gemischter Inhalte.

#### <a name="obsoleted-policy"></a>Veraltete Richtlinie

[ForceNetworkInProcess](./microsoft-edge-policies.md#forcenetworkinprocess) – Erzwingen des Ausführens von Netzwerkcode im Browserprozess.

<!-- end 84 -->

## <a name="version-83047844-june-1"></a>Version 83.0.478.44: 1. Juni

Verschiedene Bugs und Leistungsprobleme wurden behoben.

## <a name="version-83047837-may-20"></a>Version 83.0.478.37: 20. Mai

Verschiedene Bugs und Leistungsprobleme wurden behoben.

## <a name="version-83047833-may-15"></a>Version 83.0.478.33: 15. Mai

Verschiedene Bugs und Leistungsprobleme wurden behoben.

## <a name="version-83047828-may-7"></a>Version 83.0.478.28: 7. Mai

Verschiedene Bugs und Leistungsprobleme wurden behoben.

## <a name="version-83047825-may-4"></a>Version 83.0.478.25: 4. Mai

Verschiedene Bugs und Leistungsprobleme wurden behoben.

## <a name="version-83047818-april-27"></a>Version 83.0.478.18: 27. April

Verschiedene Bugs und Leistungsprobleme wurden behoben.

## <a name="version-83047813-april-22"></a>Version 83.0.478.13: 22. April

### <a name="feature-updates"></a>Funktionsupdates

- Verbesserungen an Microsoft Defender SmartScreen: mehrere Verbesserungen am Microsoft Defender SmartScreen-Dienst vorgenommen, z. B. verbesserter Schutz vor bösartigen Websites, die beim Laden umgeleitet werden, und Blockierung von Frames der obersten Ebene, wodurch bösartige Websites vollständig durch die Microsoft Defender SmartScreen-Sicherheitsseite ersetzt werden. Die allgemeine Blockierung von Frames verhindert, dass Audio und andere Medien der bösartigen Website wiedergegeben werden, was die Benutzererfahrung verbessert und weniger verwirrend macht.

- In Reaktion auf Benutzerfeedback können Benutzer nun bestimmte Cookies vom automatischen Löschen beim Schließen des Browsers ausschließen. Diese Option ist hilfreich, wenn es eine Website gibt, von der Benutzer nicht abgemeldet werden möchten, aber dennoch alle anderen Cookies beim Schließen des Browsers gelöscht werden sollen. Um dieses Feature zu verwenden, wechseln Sie zu *edge://settings/clearBrowsingDataOnClose*, und aktivieren Sie die Option "Cookies und andere Website-Daten".

- Der automatische Profilwechsel steht nun zur Verfügung, damit Sie Ihre Arbeitsinhalte einfacher auf alle Profile übertragen können. Wenn Sie arbeitsbedingt mehrere Profile verwenden, können Sie diese im Auge behalten, indem Sie zu einer Website navigieren, die eine Authentifizierung von Ihrem Geschäfts-, Uni- oder Schulkonto erfordert, während Sie in Ihrem persönlichen Profil angemeldet sind. Wenn eine Änderung erkannt wird, erhalten Sie eine Aufforderung, zu Ihrem geschäftlichen Profil zu wechseln, um auf diese Website zuzugreifen, ohne sich dafür anmelden zu müssen. Wenn Sie das geschäftliche Profil auswählen, zu dem Sie wechseln möchten, wird die Website darin geöffnet. Diese Profilwechselfunktion hilft Ihnen, Ihre Arbeits- und persönlichen Daten getrennt zu halten und müheloser zu Ihren Arbeitsinhalten zu gelangen. Wenn Sie nicht zum Wechsel zwischen Profilen aufgefordert werden möchten, können Sie einfach die Option "Nicht mehr danach fragen" auswählen.

- Verbesserungen bei den Sammlungen:
  - Sie können mit Drag & Drop ein Element zu einer Sammlung hinzufügen, ohne die Sammlung zu öffnen. Beim Ziehen und Ablegen können Sie auch einen Speicherort in der Sammlungsliste auswählen, an dem Sie das Element ablegen möchten.
  - Sie können einer Sammlung mehrere Elemente gleichzeitig hinzufügen, anstatt sie einzeln hinzuzufügen. Wenn Sie mehrere Elemente hinzufügen möchten, wählen Sie die Elemente aus, und ziehen Sie sie dann in die gewünschte Sammlung. Sie können die Elemente auch markieren, mit der rechten Maustaste klicken und dann die Sammlung auswählen, in die die Elemente eingefügt werden sollen.

- Sie können alle Tabs in einem Edge-Fenster einer neuen Sammlung hinzufügen, ohne sie einzeln hinzuzufügen. Um alle Registerkarten hinzuzufügen, klicken Sie mit der rechten Maustaste auf eine beliebige Registerkarte, und wählen Sie "Alle Registerkarten zu neuer Sammlung hinzufügen" aus.

- Erweiterungssynchronisierung ist jetzt verfügbar. Jetzt können Sie Ihre Erweiterungen auf allen Ihren Geräten synchronisieren! Erweiterungen aus den Microsoft und Chrome Stores werden mit Microsoft Edge synchronisiert. Um dieses Feature zu verwenden, klicken Sie auf die Auslassungspunkte (**...**) auf der Menüleiste, und wählen Sie **Einstellungen** aus. Klicken Sie unter Ihrem Profil auf **Synchronisierung**, um die Synchronisierungsoptionen anzuzeigen. Verwenden Sie unter **Profile/Synchronisierung** die Option zum Aktivieren von Erweiterungen. Zum Deaktivieren der Synchronisierung von Erweiterungen können Sie die [SyncTypesListDisabled](./microsoft-edge-policies.md#synctypeslistdisabled)-Gruppenrichtlinie verwenden.

- Die Meldung auf der Seite "Downloads verwalten" zu unsicheren Downloads, die blockiert wurden, wurde verbessert.

- Verbesserungen für den plastischen Reader:
  - Unterstützung für Adverbien in der Wortarten-Oberfläche im plastischen Reader wurde hinzugefügt. Wenn Sie einen Artikel im plastischen Reader lesen, öffnen Sie die Grammatiktools, und aktivieren Sie "Adverbien" in "Wortarten", um alle Adverbien auf der Seite hervorzuheben.
  - Die Möglichkeit, Inhalte auf einer Webseite auszuwählen und im plastischen Reader zu öffnen, wurde hinzugefügt. Diese Funktion ermöglicht es Benutzern, den plastischen Reader und alle Lerntools (z. B. "Zeilenfokus" und "Laut vorlesen") auf allen Websites zu verwenden.

- Link Doctor bietet den Benutzern eine Host-Korrektur und Suchabfrage, wenn sie sich bei der Eingabe einer URL vertippen. Zum Beispiel: <br>
Ein Benutzer gibt "powerbi" fälschlicherweise als "powerbbi".com ein. Der Link Doctor schlägt "powerbi".com als Korrektur vor und erstellt einen Link zur Suche nach "powerbbi", falls der Benutzer nach etwas anderem sucht.

- Lassen Sie zu, dass Benutzer ihre Entscheidung, ein externes Protokoll für eine bestimmte Site zu starten, speichern. Benutzer können die [ExternalProtocolDialogShowAlwaysOpenCheckbox](/DeployEdge/microsoft-edge-policies#externalprotocoldialogshowalwaysopencheckbox)-Richtlinie konfigurieren, um dieses Feature zu aktivieren oder zu deaktivieren.

- Benutzer können Microsoft Edge direkt in den Microsoft Edge-**Einstellungen** als Standardbrowser festlegen. Diese Funktion erleichtert es den Benutzern, ihren Standardbrowser im Kontext des Browsers selbst zu ändern, anstatt die Einstellungen des Betriebssystems durchsuchen zu müssen. Um dieses Feature zu nutzen, gehen Sie zu *edge://settings/defaultBrowser*, und klicken Sie auf **Als Standardbrowser festlegen**.

- Mehrere DevTools-Updates, einschließlich neuer Unterstützung für Remote-Debugging, Verbesserungen der Benutzeroberfläche und mehr. Weitere Informationen finden Sie unter [Neuigkeiten in DevTools (Microsoft Edge 83)](/microsoft-edge/devtools-guide-chromium/whats-new/2020/03/devtools).

### <a name="policy-updates"></a>Richtlinienupdates

#### <a name="new-policies"></a>Neue Richtlinien

Es wurden 15 neue Richtlinien hinzugefügt. Laden Sie die aktualisierten administrativen Vorlagen von der [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise) herunter. Die folgenden neuen Richtlinien wurden hinzugefügt.

- [AllowSurfGame](./microsoft-edge-policies.md#allowsurfgame) – Surfspiel zulassen.
- [AllowTokenBindingForUrls](./microsoft-edge-policies.md#allowtokenbindingforurls) – Konfigurieren Sie die Liste der Websites, für die Microsoft Edge versucht, eine Tokenverbindung einzurichten.
- [BingAdsSuppression](./microsoft-edge-policies.md#bingadssuppression) – Blockieren Sie alle Anzeigen in Bing-Suchergebnissen.
- [BuiltinCertificateVerifierEnabled](./microsoft-edge-policies.md#builtincertificateverifierenabled) – Bestimmt, ob die integrierte Zertifikatprüfung zum Überprüfen von Serverzertifikaten verwendet wird.
- [ClearCachedImagesAndFilesOnExit](./microsoft-edge-policies.md#clearcachedimagesandfilesonexit) – Löschen von zwischengespeicherten Bildern und Dateien, wenn Microsoft Edge geschlossen wird.
- [ConfigureShare](./microsoft-edge-policies.md#configureshare) – Konfigurieren Sie die Freigabe-Oberfläche.
- [DeleteDataOnMigration](./microsoft-edge-policies.md#deletedataonmigration) – Löschen alter Browserdaten bei der Migration.
- [DnsOverHttpsMode](./microsoft-edge-policies.md#dnsoverhttpsmode) – Steuert den Modus "DNS-over-HTTPS".
- [DnsOverHttpsTemplates](./microsoft-edge-policies.md#dnsoverhttpstemplates) – Geben Sie die URI-Vorlage des gewünschten DNS-over-HTTPS-Resolvers an.
- [FamilySafetySettingsEnabled](./microsoft-edge-policies.md#familysafetysettingsenabled) – Benutzern das Konfigurieren von Family Safety gestatten.
- [LocalProvidersEnabled](./microsoft-edge-policies.md#localprovidersenabled) – Vorschläge von lokalen Anbietern zulassen.
- [ScrollToTextFragmentEnabled](./microsoft-edge-policies.md#scrolltotextfragmentenabled) – Aktivieren des Scrollens zu Text, der in URL-Fragmenten angegeben ist.
- [ScreenCaptureAllowed](./microsoft-edge-policies.md#screencaptureallowed) – Zulassen oder Verweigern von Bildschirmaufnahmen.
- [SyncTypesListDisabled](./microsoft-edge-policies.md#synctypeslistdisabled) – Konfigurieren Sie die Liste der Typen, die von der Synchronisierung ausgeschlossen werden.
- [NativeWindowOcclusionEnabled](./microsoft-edge-policies.md#nativewindowocclusionenabled) – Aktivieren des Ausblendens nativer Fenster.

#### <a name="deprecated-policy"></a>Veraltete Richtlinie

Die folgende Richtlinie greift in dieser Version weiterhin. Sie veraltet in einer zukünftigen Version.

[EnableDomainActionsDownload](./microsoft-edge-policies.md#enabledomainactionsdownload) – Herunterladen von Domänenaktionen von Microsoft aktivieren

<!--  end 83 -->

## <a name="version-81041660-april-20"></a>Version 81.0.416.60: 20. April

Verschiedene Bugs und Leistungsprobleme wurden behoben.

## <a name="version-81041658-april-17"></a>Version 81.0.416.58: 17. April

Sicherheitsupdates.

## <a name="version-81041650-april-10"></a>Version 81.0.416.50: 10. April

Verschiedene Bugs und Leistungsprobleme wurden behoben.

## <a name="version-81041645-april-3"></a>Version 81.0.416.45: 3. April

Verschiedene Bugs und Leistungsprobleme wurden behoben.

## <a name="version-81041641-march-30"></a>Version 81.0.416.41: 30. März

Verschiedene Bugs und Leistungsprobleme wurden behoben.

## <a name="version-81041634-march-17"></a>Version 81.0.416.34: 17. März

Verschiedene Bugs und Leistungsprobleme wurden behoben.

## <a name="version-81041631-march-12"></a>Version 81.0.416.31: 12. März

Verschiedene Bugs und Leistungsprobleme wurden behoben.

## <a name="version-81041628-march-9"></a>Version 81.0.416.28: 9. März

Verschiedene Bugs und Leistungsprobleme wurden behoben.

## <a name="version-81041620-february-28"></a>Version 81.0.416.20: 28. Februar

Verschiedene Bugs und Leistungsprobleme wurden behoben.

## <a name="version-81041612-february-20"></a>Version 81.0.416.12: 20. Februar

### <a name="feature-updates"></a>Funktionsupdates

- Sammlungen ist jetzt verfügbar. Sie können beginnen, indem Sie auf das Symbol "Sammlungen" neben der Adressleiste klicken. Durch diese Aktion wird der Bereich "Sammlungen" geöffnet, in dem Sie Sammlungen erstellen, bearbeiten und anzeigen können. Wir haben Sammlungen basierend auf dem, was Sie im Web tun, gestaltet. Wenn Sie Shopper, Reisender, Lehrer oder Schüler bzw. Studierender sind, können Sammlungen hilfreich sein. [Weitere Informationen](https://blogs.windows.com/msedgedev/2019/12/09/improvements-collections-sync-microsoft-edge/#LuDPRDUDCgdgdOVt.97).

- Lassen Sie die Entfernung (Ausblenden aus der Symbolleiste) der Schaltfläche „Sammlungen“ aus der Microsoft Edge-Symbolleiste aus Konsistenzgründen zu.

- Die automatische Anmeldung bei lokalen Active Directory-Konten wird nur für Organisationen angestrebt, die diese Funktion aktivieren. Wenn Benutzer bereits mit einem lokalen AD-Konto angemeldet waren, können Sie sich nun abmelden. Jetzt werden Benutzer mit dem primären Konto ihres Betriebssystems nur automatisch angemeldet, wenn es sich um ein Microsoft-Konto oder ein Azure Active Directory-Konto handelt. Administratoren können mithilfe der ConfigureOnPremisesAccountAutoSignIn-Richtlinie die automatische Anmeldung mit einem lokalen AD-Konto aktivieren.

- Application Guard. Unterstützung von Erweiterungen ist jetzt im Container verfügbar.

- Eine Nachricht wurde hinzugefügt, um die Benutzer zu informieren, dass Internet Explorer nicht installiert ist, wenn sie zu einer Seite navigieren, die für das Öffnen im Internet Explorer-Modus konfiguriert ist.

- Das Tool für die 3D-Ansicht in Microsoft Edge DevTools wurde mit einem neuen Feature aktualisiert, das das Debuggen von Z-Index-Stapelkontext unterstützt. In der 3D-Ansicht wird die DOM(Dokumentobjektmodell)-Tiefe mithilfe von Farbe und Stapelung dargestellt, und mit der Z-Index-Ansicht können Sie die verschiedenen Stapelkontexte Ihrer Seite isolieren. [Weitere Informationen](https://blogs.windows.com/msedgedev/2020/01/23/debug-z-index-3d-view-edge-devtools/).

- Die F12-Dev-Tools wurden in zehn neue Sprachen lokalisiert, sodass sie mit der im restlichen Browser verwendeten Sprache übereinstimmen. [Weitere Informationen](https://blogs.windows.com/msedgedev/2020/02/04/localizing-edge-devtools/).

- Unterstützung für Dolby Vision-Wiedergabe hinzugefügt. Bei dem für Dolby Vision aktivierten Windows 10 Build 17134 (Update vom April 2018) können Dolby Vision-Inhalte von Websites angezeigt werden. Hier erfahren Sie, wie Sie Dolby Vision-Inhalte von [Netflix](https://help.netflix.com/en/node/42384) aktivieren.

- Microsoft Edge kann nun doppelte Favoriten erkennen und entfernen sowie Ordner mit demselben Namen zusammenführen. Für den Zugriff auf das Tool klicken Sie in der Symbolleiste des Browsers auf den Stern, und wählen Sie "Doppelte Favoriten entfernen" aus.  Sie können Änderungen bestätigen, und alle Updates Ihrer Favoriten werden auf allen Geräten synchronisiert.

- Wir haben von Benutzern gehört, dass es schwierig sein kann, ein normales Browserfenster in dunklem Design von einem InPrivate-Fenster zu unterscheiden, da beide Fensterrahmen dunkel sind. Die neue einfarbige, blaue InPrivate-Pille in der oberen rechten Ecke versichert den Benutzern, dass sie InPrivate browsen.

- Öffnen Sie externe Links im richtigen Browserprofil. Wählen Sie ein Standardprofil für Links aus externen Apps aus, um sie aus *edge://settings/multiProfileSettings* zu öffnen.

- Es wurde eine Warnung hinzugefügt, mit der Benutzer benachrichtigt werden, die sich bei einem Browserprofil mit einem Konto angemeldet haben, nachdem sie mit einem anderen Konto angemeldet waren. Auf diese Weise können Sie unbeabsichtigte Datenzusammenführung verhindern.

- Wenn Sie in Ihrem Microsoft-Konto Zahlungskarten gespeichert haben, können Sie diese in Microsoft Edge beim Ausfüllen von Zahlungsformularen verwenden. Die Karten in Ihrem Microsoft-Konto werden auf Desktopgeräten synchronisiert, und die vollständigen Details werden nach zweistufiger Authentifizierung (CVC-Code und Microsoft-Identität) für die Website freigegeben. Zur weiteren Vereinfachung können Sie während der Authentifizierung auswählen, dass eine Kopie der Karte auf dem Gerät gesichert werden soll.

- Der Zeilenfokus ist für Benutzer vorgesehen, die sich beim Lesen auf einen begrenzten Teil des Inhalts konzentrieren möchten. Benutzer können den Fokus auf jeweils 1, 3 oder 5 Zeilen gleichzeitig richten und den Rest der Seite abdunkeln, um ohne Ablenkung zu lesen. Benutzer können mit den Fingern oder Pfeiltasten scrollen, und der Fokus wird dementsprechend verschoben.

- Windows Speller ist nun auf den Windows-Plattformen 8.1 und höher in Microsoft Edge integriert. Diese Integration bietet eine bessere Sprachunterstützung, mit Zugriff auf weitere Sprachwörterbücher sowie der Möglichkeit zur Verwendung von Windows-Benutzerwörterbüchern. Es sind keine weiteren Aktionen von den Benutzern erforderlich, wenn eine Sprache in den Betriebssystem-Spracheinstellungen hinzugefügt wurde und in den Microsoft Edge-Einstellungen die Umschaltfläche für die Rechtschreibprüfung aktiviert ist.

- Wenn PDF-Dokumente mit Microsoft Edge geöffnet werden, können die Benutzer jetzt Stellen hervorheben, Farben ändern und Hervorhebungen löschen. Dies hilft bei späteren Verweisen auf wichtige Teile des Dokuments und bei der Zusammenarbeit.

- Beim Laden langer PDF-Dokumente, die für das Web optimiert wurden, werden die vom Benutzer angezeigten Seiten schneller geladen, während der Rest des Dokuments parallel geladen wird.

- Jetzt ist es einfacher, den Plastischen Reader für eine Website zu starten, indem Sie einfach die Taste F9 drücken.

- Jetzt ist es einfacher, mit einer Tastenkombination (STRG+UMSCHALT+U) „Laut vorlesen“ zu starten.

### <a name="policy-updates"></a>Richtlinienupdates

#### <a name="new-policies"></a>Neue Richtlinien

Es wurden 12 neue Richtlinien hinzugefügt. Laden Sie die aktualisierten administrativen Vorlagen von der [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise) herunter. Die folgenden neuen Richtlinien wurden hinzugefügt.

- [AmbientAuthenticationInPrivateModesEnabled](./microsoft-edge-policies.md#ambientauthenticationinprivatemodesenabled): Aktivieren Sie die Umgebungsauthentifizierung für InPrivate- und Gastprofile. 
- [AudioSandboxEnabled](./microsoft-edge-policies.md#audiosandboxenabled): Lassen Sie die Audio-Sandbox ausführen.
- [ForceLegacyDefaultReferrerPolicy](./microsoft-edge-policies.md#forcelegacydefaultreferrerpolicy): Verwenden Sie die standardmäßige Verweiserrichtlinie „kein Verweiser beim Downgrade“.
- [GloballyScopeHTTPAuthCacheEnabled](./microsoft-edge-policies.md#globallyscopehttpauthcacheenabled): Aktivieren Sie den Cache für HTTP-Authentifizierung mit globaler Reichweite.
- [ImportExtensions](./microsoft-edge-policies.md#importextensions): Lassen Sie den Import von Erweiterungen zu.
- [ImportCookies](./microsoft-edge-policies.md#importcookies): Lassen Sie den Import von Cookies zu.
- [ImportShortcuts](./microsoft-edge-policies.md#importshortcuts): Lassen Sie den Import von Verknüpfungen zu.
- [InternetExplorerIntegrationSiteRedirect](./microsoft-edge-policies.md#internetexplorerintegrationsiteredirect): Geben Sie an, wie sich „seiteninterne“ Navigationen zu nicht konfigurierten Websites verhalten, wenn sie von Seiten im Internet Explorer-Modus gestartet werden.
- [OmniboxMSBProviderEnabled](./microsoft-edge-policies.md): Aktivieren Sie Microsoft Search for Business-Anbieter in Omnibox.
- [StricterMixedContentTreatmentEnabled](./microsoft-edge-policies.md#strictermixedcontenttreatmentenabled): Aktivieren Sie die striktere Behandlung gemischter Inhalte.
- [TLS13HardeningForLocalAnchorsEnabled](./microsoft-edge-policies.md#tls13hardeningforlocalanchorsenabled): Aktivieren Sie das TLS 1.3-Sicherheitsfeature für lokale Vertrauensanker.
- [ConfigureOnPremisesAccountAutoSignIn](./microsoft-edge-policies.md#configureonpremisesaccountautosignin): Konfigurieren Sie die automatische Anmeldung mit einem Active Directory-Domänenkonto, wenn kein Azure AD-Domänenkonto vorhanden ist.

#### <a name="deprecated-policies"></a>Veraltete Richtlinien

Die folgenden Richtlinien greifen in dieser Version weiterhin. Sie veralten in einer zukünftigen Version.

- [WebComponentsV0Enabled](./microsoft-edge-policies.md#webcomponentsv0enabled): Aktivieren Sie die Web Components v0-API bis M84 erneut.
- [WebDriverOverridesIncompatiblePolicies](./microsoft-edge-policies.md#webdriveroverridesincompatiblepolicies): Lassen Sie zu, dass WebDriver inkompatible Richtlinien außer Kraft setzt.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)