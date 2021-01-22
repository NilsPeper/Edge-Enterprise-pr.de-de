---
title: Anmerkungen zu dieser Version von Microsoft Edge für Beta-Kanal
ms.author: aguta
author: dan-wesley
manager: srugh
ms.date: 01/20/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Anmerkungen zu dieser Version von Microsoft Edge für Beta-Kanal
ms.openlocfilehash: c1d0b7091655d5ca0893ea11cc0c2fc44bb516dd
ms.sourcegitcommit: a6c58b19976c194299be217c58b9a99b48756fd0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/21/2021
ms.locfileid: "11281004"
---
# Versionshinweise für Microsoft Edge Beta-Kanal

Diese Versionshinweise enthalten Informationen zu neuen Funktionen und nicht sicherheitsrelevanten Updates, die im Microsoft Edge Beta-Kanal enthalten sind. Archivierte Versionen dieser Versionshinweise sind [hier](microsoft-edge-relnote-archive-beta-channel.md) verfügbar.

## Version 88.0.705.49: 20. Januar

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## Version 88.0.705.45: 15. Januar

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## Version 88.0.705.41: 11. Januar

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## Version 88.0.705.29: 21. Dezember

Verschiedene Fehler und Leistungsprobleme wurden behoben.

<!-- begin major 88 -->
## Version 88.0.705.18: 9. Dezember

### Funktionsupdates

- **Abschreibungen:**

  - Veraltete Unterstützung für das FTP-Protokoll. Die Unterstützung für das ältere FTP-Protokoll wurde von Microsoft Edge entfernt. Der Versuch, zu einer FTP-Verbindung zu navigieren, führt dazu, dass der Browser das Betriebssystem anweist, eine externe Anwendung zu öffnen, um die FTP-Verbindung zu verarbeiten. Alternativ können IT-Administratoren Microsoft Edge so konfigurieren, dass der IE-Modus für Sites verwendet wird, die auf dem FTP-Protokoll basieren.
  - Die Adobe Flash-Unterstützung wird entfernt. Ab Microsoft Edge Beta Version 88 werden die Adobe Flash-Funktionen und die Unterstützung entfernt. Weitere Informationen: [Update auf Adobe Flash Player Ende der Unterstützung – Microsoft Edge-Blog (windows.com)](https://blogs.windows.com/msedgedev/2020/09/04/update-adobe-flash-end-support/)

- **Authentifizierung:**

  - Einmaliges Anmelden (SSO, Single Sign On) ist jetzt für Azure Active Directory-Konten (Azure AD) und Microsoft Account (MSA) unter MacOS und Windows auf niedrigerer Ebene verfügbar. Ein Benutzer, der bei Microsoft Edge unter macOS oder Microsoft Windows (7, 8.1) auf niedrigerer Ebene angemeldet ist, wird jetzt automatisch bei Websites angemeldet, die so konfiguriert sind, dass sie eine einmalige Anmeldung mit Work- und Microsoft-Konten ermöglichen (z. B. bing.com, office.com, msn.com, outlook.com).<br>Hinweis: Ein Benutzer muss sich möglicherweise abmelden und dann erneut anmelden, wenn er sich in einer Version vor Microsoft Edge 88 bei Microsoft Edge angemeldet hat, um diese Funktion nutzen zu können.
  - Wechseln Sie Benutzer unter macOS automatisch zu ihrem Arbeitsprofil für Websites, die sich bei ihrem Arbeitskonto authentifizieren. Ab Microsoft Edge Version 88 bieten wir die Möglichkeit, unter Websites zu wechseln, die sich unter macOS mit dem Arbeitsprofil eines Benutzers authentifizieren.<br>Hinweis: Ein Benutzer muss sich möglicherweise abmelden und dann erneut anmelden, wenn er sich in einer Version vor Microsoft Edge 88 bei Microsoft Edge angemeldet hat, um diese Funktion nutzen zu können.

- Kioskmodus-Option zum Beenden der Sitzung. Die Schaltfläche "Sitzung beenden" ist jetzt im öffentlichen Browsing im Kioskmodus verfügbar. Diese Funktion stellt sicher, dass Browserdaten und -einstellungen gelöscht werden, wenn Microsoft Edge geschlossen wird. Weitere Informationen zu den Funktionen und der Roadmap des Kioskmodus finden Sie unter [Konfigurieren des Microsoft Edge-Kioskmodus](https://docs.microsoft.com/deployedge/microsoft-edge-configure-kiosk-mode).

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

### Richtlinienupdates

#### Neue Richtlinien

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

#### Veraltete Richtlinien

Die folgenden Richtlinien sind veraltet.

- [ProactiveAuthEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proactiveauthenabled) – Aktivieren Sie die proaktive Authentifizierung.
- [ProxyBypassList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxybypasslist) – Konfigurieren Sie die Proxy-Umgehungsregeln.
- [ProxyMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxymode) – Konfigurieren Sie die Proxy-Server-Einstellungen.
- [ProxyPacUrl](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxypacurl) – Legen Sie die URL der Proxy .pac-Datei fest.
- [Proxyserver](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxyserver) – Konfigurieren Sie die Adresse oder URL des Proxyservers.
- [WebDriverOverridesIncompatiblePolicies](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webdriveroverridesincompatiblepolicies) – Erlauben Sie WebDriver, inkompatible Richtlinien zu überschreiben.

#### Veraltete Richtlinie

Die folgenden Richtlinien sind veraltet.

- [DefaultPluginsSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultpluginssetting) – Standardeinstellung für Adobe Flash.
- [PluginsAllowedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#pluginsallowedforurls) – Lassen Sie das Adobe Flash-Plug-In auf bestimmten Websites zu.
- [PluginsBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#pluginsblockedforurls) – Blockieren Sie das Adobe Flash-Plug-in auf bestimmten Websites.
- [RunAllFlashInAllowMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#runallflashinallowmode) – Erweitern der Adobe Flash-Inhaltseinstellung auf alle Inhalte.

<!-- end major 88 -->

## Version 87.0.664.55: 3. Dezember

Verschiedene Bugs und Leistungsprobleme wurden behoben. Das folgende neue Feature wird in diesem Release unterstützt.

- **Benachrichtigungen werden generiert, wenn das Kennwort eines Benutzers in einem Onlineleck gefunden wird**. Benutzerkennwörter werden gegen ein Verzeichnis bekannter Anmeldeinformationen überprüft und geben dem Benutzer eine Warnung zurück, wenn eine Übereinstimmung gefunden wird. Um die Sicherheit und den Datenschutz zu gewährleisten, werden Benutzerkennwörter gehashed und verschlüsselt, wenn Sie mit der Datenbank der durchgesickerten Anmeldeinformationen abgeglichen werden.

## Version 87.0.664.52: 30. November

Verschiedene Bugs und Leistungsprobleme wurden behoben.

## Version 87.0.664.40: vom 18. November

Verschiedene Bugs und Leistungsprobleme wurden behoben.

## Version 87.0.664.36: 16. November

Verschiedene Bugs und Leistungsprobleme wurden behoben.

## Version 87.0.664.30: 9. November

Verschiedene Bugs und Leistungsprobleme wurden behoben.

## Version 87.0.664.24: 2. November

Verschiedene Bugs und Leistungsprobleme wurden behoben.

## Version 87.0.664.18: 26.Oktober

Verschiedene Bugs und Leistungsprobleme wurden behoben.

<!-- begin major 87 -->
## Version 87.0.664.12: 20.Oktober

### Funktionsupdates

- **Datenschutzfeatures des Kioskmodus aktiviert**. Ab MicrosoftEdge, Version87, werden Kioskmodus-Features aktiviert, die Unternehmen im Zusammenhang mit dem Datenschutz für Benutzerdaten helfen. Diese Features ermöglichen es beispielsweise, dass die Benutzerdaten beim Beenden gelöscht werden, dass heruntergeladene Dateien gelöscht werden und dass die konfigurierte Startumgebung nach einer festgelegten Leerlaufzeitspanne zurückgesetzt wird. Informieren Sie sich genauer zum [Konfigurieren des MicrosoftEdge-Kioskmodus](https://docs.microsoft.com/deployedge/microsoft-edge-configure-kiosk-mode).
- **ClickOnce-Bereitstellung standardmäßig aktiviert**. ClickOnce ist in MicrosoftEdge87 standardmäßig aktiviert, wodurch die Hindernisse für Unternehmen reduziert werden, die Software bereitstellen und mit dem Browserverhalten der Vorgängerversion von MicrosoftEdge besser übereinstimmen möchten. Ab MicrosoftEdge87 gibt der Status „Nicht konfiguriert“ der Richtlinie „ClickOnceEnabled“ den neuen standardmäßigen ClickOnce-Status „Aktiviert“ (im Vergleich zum vorherigen Standardstatus „Deaktiviert“) wieder.
- **Auf der Enterprise-Seite „Neue Registerkarte” (New Tab Page, NTP) wird Produktivität in anpassbare, arbeitsrelevante Feedinhalte integriert**. Im Enterprise-NTP-Bereich werden die Office365-Produktivitätsseite, die wir den mit ihrem Geschäfts-, Schul-oder Unikonto angemeldeten Benutzern bieten, mit personalisierten, arbeitsrelevanten Unternehmens- und Branchenfeeds zusammengeführt, die auf einer einzigen Seite organisiert sind. Benutzer können die vertrauten Office365-Inhalte und MicrosoftSearch for Business erkennen, das von Bing unterstützt wird. Darüber hinaus können sie mühelos zu einem anpassbaren „Mein Feed“ mit Inhalten und Modulen, die für den Benutzer, sein Unternehmen oder seine Branche relevant sind, sowie zu einer Auswahl weiterer Feeds wechseln, die von der Organisation zur Verfügung gestellt wurde. [Weitere Informationen](https://docs.microsoft.com/microsoft-365/admin/manage/manage-industry-news?view=o365-worldwide&preserve-view=true).

- **Datenschutz und Sicherheit:**

  - Unterstützung von TLS-Tokenbindung für mit Richtlinien konfigurierte Websites. Die TLS-Tokenbindung hilft bei der Verhinderung von Angriffen zum Diebstahl von Token, um sicherzustellen, dass Cookies nur auf dem Gerät wiederverwendet werden können, auf dem sie ursprünglich festgelegt wurden. Die Verwendung der TLS-Tokenbindung erfordert es, dass die Richtlinie [AllowTokenBindingForUrls](https://docs.microsoft.com/deployedge/microsoft-edge-policies#allowtokenbindingforurls) festgelegt wurde und dass die aufgeführten Websites dieses Feature unterstützen.

- **Tastaturunterstützung für Textmarker in PDF-Dateien**. Benutzer können jeden beliebigen Text in einer PDF-Datei mithilfe ihrer Tastatur hervorheben.

- **Drucken:**

  - Wählen Sie die Seite aus, die beim beidseitigen Drucken gedreht werden soll. Benutzer können auswählen, ob ein Blatt beim beidseitigen Drucken auf die lange Seite (Querformat) oder die kurze Seite (Hochformat) gedreht werden soll.
  - Wählen Sie den Druckmodus „Rasterung“ für das Unternehmen aus. Steuern Sie, wie MicrosoftEdge auf einem Nicht-PostScript-Drucker unter Windows druckt. Manchmal müssen Druckaufträge bei Nicht-PostScript-Druckern gerastert werden, damit korrekt gedruckt wird. Die Druckoptionen sind „Full" (Vollständig) und „Fast“ (Schnell).

### Richtlinienupdates

#### Neue Richtlinien

Es wurden zehn neue Richtlinien hinzugefügt. Laden Sie die aktualisierten administrativen Vorlagen von der [Microsoft Edge Enterprise Angebotsseite](https://www.microsoft.com/edge/business/download) herunter. Die folgenden neuen Richtlinien wurden hinzugefügt.

- [ConfigureFriendlyURLFormat](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configurefriendlyurlformat) – Zum Konfigurieren des Standardformats für das Einfügen von URLs, die aus MicrosoftEdge kopiert wurden, und zum Ermitteln, ob Benutzern weitere Formate zur Verfügung stehen.
- [EdgeShoppingAssistantEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#edgeshoppingassistantenabled) – Shopping in MicrosoftEdge aktiviert.
- [HideInternetExplorerRedirectUXForIncompatibleSitesEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#hideinternetexplorerredirectuxforincompatiblesitesenabled) – Zum Ausblenden des Dialogfelds für einmalige Umleitung und des Banners in MicrosoftEdge.
- [KioskAddressBarEditingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskaddressbareditingenabled) – Zum Konfigurieren der Adressleistenbearbeitung für Benutzerfreundlichkeit beim öffentlichen Surfen im Kioskmodus.
- [KioskDeleteDownloadsOnExit](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskdeletedownloadsonexit) – Zum Löschen von Dateien, die während einer Kiosksitzung heruntergeladen wurden, wenn MicrosoftEdge geschlossen wird.
- [PasswordRevealEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#passwordrevealenabled) – Zum Aktivieren der Schaltfläche für Kennwortanzeige.
- [RedirectSitesFromInternetExplorerPreventBHOInstall](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#redirectsitesfrominternetexplorerpreventbhoinstall) – Zum Verhindern, dass das BHO (Browserhilfsobjekt) installiert wird, um inkompatible Websites von Internet Explorer zu MicrosoftEdge umzuleiten.
- [RedirectSitesFromInternetExplorerRedirectMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#redirectsitesfrominternetexplorerredirectmode) – Zum Umleiten inkompatibler Websites von Internet Explorer zu MicrosoftEdge.
- [SpeechRecognitionEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#speechrecognitionenabled) – Zum Konfigurieren der Spracherkennung.
- [WebCaptureEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webcaptureenabled) – Zum Aktivieren des Features „Weberfassung“ in MicrosoftEdge.

#### Veraltete Richtlinie

[NewTabPageSetFeedType](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagesetfeedtype) – Zum Konfigurieren der MicrosoftEdge-Oberfläche für neue Registerkartenseiten.

#### Veraltete Richtlinie

[EnableDeprecatedWebPlatformFeatures](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enabledeprecatedwebplatformfeatures) – Zum erneuten Aktivieren von veralteten Features für Webplattformen für einen begrenzten Zeitraum.

<!-- end major 87 -->

## Version 86.0.622.43: 16.Oktober

Verschiedene Bugs und Leistungsprobleme wurden behoben.

## Version 86.0.622.36: 7.Oktober

Verschiedene Bugs und Leistungsprobleme wurden behoben.

## Version 86.0.622.31: 1.Oktober

Verschiedene Bugs und Leistungsprobleme wurden behoben.

## Version 86.0.622.28: 28. September

Verschiedene Bugs und Leistungsprobleme wurden behoben.

## Version 86.0.622.15: 14. September

Verschiedene Bugs und Leistungsprobleme wurden behoben.

## Version 86.0.622.11: 9. September

### Funktionsupdates

* **Internet Explorer-Modus:**

   * Ermöglichen Sie Benutzern, die Microsoft Edge-Benutzeroberfläche zum Testen von Websites im Internet Explorer-Modus zu verwenden. Beginnend mit der Microsoft Edge-Version 86 können Administratoren eine Benutzeroberflächenoption für Ihre Benutzer aktivieren, um eine Registerkarte im Internet Explorer-Modus zu Testzwecken oder als Notlösung zu laden, bis Websites zur XML-Websiteliste hinzugefügt werden.

* **Löschen von Downloads von der Festplatte mithilfe des Download-Managers.** Benutzer sind jetzt in der Lage, die heruntergeladenen Dateien von Ihrer Festplatte zu löschen, ohne den Browser verlassen zu müssen. Die neue Funktion zum Löschen von Downloads befindet sich im Kontextmenü des Downloadverzeichnisses oder der Downloadseite.

* **Zurücksetzen zur vorherigen Microsoft Edge-Version.** Mit der Rollback-Funktion können Administratoren auf eine Ihnen bekannte gute Version von Microsoft Edge zurückgreifen, wenn ein Problem in der neuesten Version von Microsoft Edge auftritt.
[Weitere Informationen](edge-learnmore-rollback.md).

* **Erzwingen der standardmäßigen Aktivierung der Synchronisierung im gesamten Unternehmen.**  Administratoren können die Synchronisierung für Azure Active Directory-Konten (Azure AD) standardmäßig mit der [ForceSync](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forcesync)-Richtlinie aktivieren.

* **PDF-Updates:**

  * Inhaltsverzeichnis für PDF-Dokumente. Ab Version 86 hat Microsoft Edge Unterstützung für das Inhaltsverzeichnis hinzugefügt, das es Benutzern ermöglicht, einfach durch PDF-Dokumente zu navigieren.
  * Zugriff auf alle PDF-Funktionalitäten auf Bildschirmen mit kleinem Formfaktor. Zugriff auf alle Funktionen des Microsoft Edge PDF-Readers auf Geräten mit kleinen Bildschirmgrößen.
  * Stiftunterstützung für Textmarker in PDF-Dateien. Mit diesem Update können Benutzer mit ihrem digitalen Stift Text in PDF-Dateien direkt markieren, so wie sie es auch mit einem physischen Textmarker und Papier tun würden.
  * Verbessertes Scrollen im PDF-Format. Das Scrollen durch lange PDF-Dokumente kann jetzt ohne Ruckeln erlebt werden.

* **Automatischer Profilwechsel unter Windows 7, 8 und 8.1.** Der zurzeit in Microsoft Edge unter Windows 10 verfügbare automatische Profilwechsel wird auf Vorgängerversionen (Windows 7, 8 und 8.1) erweitert. Weitere Informationen finden Sie im Blogbeitrag [Automatischer Profilwechsel](https://blogs.windows.com/msedgedev/2020/04/30/automatic-profile-switching/).

* **Benutzer sehen Vorschläge zur automatischen Vervollständigung, wenn sie mit der Eingabe einer Suchanfrage auf der Microsoft Edge Add-ons-Website beginnen.** Die automatische Vervollständigung hilft Benutzern, Ihre Suchabfrage schnell zu vervollständigen, ohne die gesamte Zeichenfolge eingeben zu müssen. Dies ist hilfreich, da sich die Benutzer keine korrekten Schreibweisen merken müssen, und Sie können aus den verfügbaren Optionen auswählen, die angezeigt werden.

* **Entfernen der Cache-API für HTML5-Anwendungen.**  Beginnend mit der Microsoft Edge-Version 86, wird die veraltete Anwendungs-Cache-API, die die Offline-Nutzung von Webseiten ermöglicht, von Microsoft Edge entfernt. Webentwickler sollten sich die [WebDev-Dokumentation](https://web.dev/appcache-removal/) ansehen, um Informationen zum Ersetzen der Anwendungs-Cache-API durch Service Worker zu erhalten.  Wichtig: Sie können einen [AppCache OriginTrial-Token](https://developers.chrome.com/origintrials/#/view_trial/1776670052997660673) anfordern, der es Websites ermöglicht, die veraltete Anwendungs-Cache-API weiterhin bis zur Microsoft Edge-Version 90 zu verwenden.

* **Sicherheit:**

  * Unterstützung für sicheres DNS (DNS-over-HTTPS).  Ab der Microsoft Edge-Version 86 stehen Einstellungen zum Steuern des sicheren DNS auf nicht verwalteten Geräten zur Verfügung. Diese Einstellungen sind für Benutzer auf verwalteten Geräten nicht zugänglich, aber IT-Administratoren können sicheres DNS aktivieren oder deaktivieren, indem Sie die Gruppenrichtlinie [dnsoverhttpsmode](https://docs.microsoft.com/deployedge/microsoft-edge-policies#dnsoverhttpsmode) verwenden.


* **Hinzufügen eines benutzerdefiniertes Bildes zur Seite „Neue Registerkarte“ (New Tab Page, NTP) mithilfe einer Gruppenrichtlinie.** Beginnend mit der Microsoft Edge-Version 86 bietet die NTP die Möglichkeit, das Standardbild durch ein benutzerdefiniertes Bild zu ersetzen. Die Möglichkeit, die Eigenschaften dieses Bilds zu verwalten, wird auch von der Gruppenrichtlinie unterstützt.

* **Anpassen von benutzerdefinierten Tastenkombinationen an VS Code.** Microsoft Edge DevTools unterstützt jetzt die Anpassung von Tastenkombinationen in DevTools mit Ihrem Editor/Ihrer IDE. (In Microsoft Edge 84 wurde die Möglichkeit hinzugefügt, DevTools-Tastenkombinationen mit VS Code abzugleichen).

* **Ersetzen der Richtlinien [MetricsReportingEnabled]( https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#metricsreportingenabled) und [SendSiteInformationToImproveServices]( https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices) für Vorgängerversionen von Windows und macOS.** Diese Richtlinien sind in der Microsoft Edge-Version 86 veraltet und werden in der Microsoft Edge-Version 89 überholt sein.<br>
Diese Richtlinien werden ersetzt durch [Telemetrie zulassen](https://go.microsoft.com/fwlink/?linkid=2099569) unter Windows 10 sowie die neue [DiagnosticData](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#diagnosticdata)-Richtlinie für alle anderen Plattformen. Dadurch können Benutzer die Diagnosedaten verwalten, die an Microsoft für Windows 7, 8, 8.1 und macOS gesendet werden.

* **"SameSite=Lax" für Cookies (Standard)**. Zur Verbesserung der Websicherheit und des Datenschutzes verwenden Cookies jetzt standardmäßig die [SameSite = Lax](https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie/SameSite)-Behandlung. Dies bedeutet, dass Cookies nur in einem Erstanbieterkontext gesendet werden und bei an Dritte gesendeten Anforderungen weggelassen werden. Diese Änderung kann Auswirkungen auf die Kompatibilität von Websites haben, die Cookies von Drittanbietern benötigen, damit Ressourcen die korrekt funktionieren. Um solche Cookies zuzulassen, können Webentwickler Cookies markieren, die aus Drittanbieterkontext gesetzt und an Drittanbieterkontext gesendet werden sollen, indem sie beim Setzen des Cookies explizit die Attribute `SameSite=none` und `Secure` hinzufügen. Unternehmen, die bestimmte Sites von dieser Änderung ausnehmen möchten, können dies mit der Richtlinie [LegacySameSiteCookieBehaviorEnabledForDomainList](https://docs.microsoft.com/deployedge/microsoft-edge-policies#legacysamesitecookiebehaviorenabledfordomainlist) tun oder die Änderung für alle Sites mit der Richtlinie [LegacySameSiteCookieBehaviorEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#legacysamesitecookiebehaviorenabled) ablehnen.

### Richtlinienupdates

#### Neue Richtlinien

Es wurden neunzehn neue Richtlinien hinzugefügt. Laden Sie die aktualisierten administrativen Vorlagen von der [Microsoft Edge Enterprise Angebotsseite](https://aka.ms/EdgeEnterprise) herunter. Die folgenden neuen Richtlinien wurden hinzugefügt.

- [CollectionsServicesAndExportsBlockList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#collectionsservicesandexportsblocklist): Blockieren des Zugriffs auf eine bestimmte Liste von Diensten und Exportieren von Zielen in Sammlungen.
- [DefaultSensorsSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultsensorssetting): Standardeinstellung für Sensoren.
- [DefaultSerialGuardSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultserialguardsetting): Steuerung der Verwendung der Serial-API.
- [DiagnosticData](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#diagnosticdata): Senden der erforderlichen und optionalen Diagnosedaten zur Browsernutzung.
- [EnterpriseModeSiteListManagerAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enterprisemodesitelistmanagerallowed): Zugriff auf das Tool Enterprise Mode Site List Manager zulassen.
- [ForceSync](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forcesync): Synchronisierung von Browserdaten erzwingen und Zustimmungsaufforderung für die Synchronisierung nicht anzeigen.
- [InsecureFormsWarningsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#insecureformswarningsenabled): Aktivieren von Warnungen für unsichere Formulare.
- [InternetExplorerIntegrationTestingAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationtestingallowed): Internet Explorer-Modus-Tests zulassen.
- [SpotlightExperiencesAndRecommendationsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#spotlightexperiencesandrecommendationsenabled): Wählen Sie aus, ob Benutzer personalisierte Hintergrundbilder und Text, Vorschläge, Benachrichtigungen und Tipps für Microsoft-Dienste erhalten können.
- [NewTabPageAllowedBackgroundTypes](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpageallowedbackgroundtypes): Konfigurieren der zulässigen Hintergrundtypen für das neue Registerkartenseiten-Layout.
- [SaveCookiesOnExit](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#savecookiesonexit): Speichern Sie Cookies, wenn Microsoft Edge geschlossen wird.
- [SensorsAllowedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sensorsallowedforurls): Zugriff auf Sensoren auf bestimmten Websites zulassen.
- [SensorsBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sensorsblockedforurls): Zugriff auf Sensoren auf bestimmten Websites blockieren.
- [SerialAskForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#serialaskforurls): Die Serial-API auf bestimmten Websites zulassen.
- [SerialBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#serialblockedforurls): Die Serial-API auf bestimmten Websites blockieren.
- [URLBlocklist](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#urlblocklist): Blockieren des Zugriffs auf eine Liste von URLs.
- [URLAllowlist](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#urlallowlist): Definieren einer Liste zulässiger URLs.
- [UserAgentClientHintsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#useragentclienthintsenabled): Aktivieren der Funktion User-Agent Client Hints.
- [UserDataSnapshotRetentionLimit](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#userdatasnapshotretentionlimit): Schränkt die Anzahl der Benutzerdaten-Momentaufnahmen ein, die zur Verwendung für Notfall-Rollbacks aufbewahrt werden.

#### Veraltete Richtlinien

- [MetricsReportingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#metricsreportingenabled): Aktivieren der Berichterstellung für Nutzungs- und Absturzdaten.
- [SendSiteInfoToImproveServices](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices): Senden von Siteinformationen, um Microsoft-Dienste zu verbessern.

#### Veraltete Richtlinie

[TLS13HardeningForLocalAnchorsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#tls13hardeningforlocalanchorsenabled): Aktivieren Sie das TLS 1.3-Sicherheitsfeature für lokale Vertrauensanker.

#### Richtlinienüberschrift geändert

[NativeWindowOcclusionEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#nativewindowocclusionenabled): Native Window Occlusion aktivieren.

#### Richtlinienbeschreibung geändert

- [AdsSettingForIntrusiveAdsSites](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#adssettingforintrusiveadssites)
- [AllowTokenBindingForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#allowtokenbindingforurls)
- [AmbientAuthenticationInPrivateModesEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#ambientauthenticationinprivatemodesenabled)
- [ApplicationGuardContainerProxy](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#applicationguardcontainerproxy)
- [AutoImportAtFirstRun](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#autoimportatfirstrun)
- [AutoOpenFileTypes](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#autoopenfiletypes)
- [BrowserSignin](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#browsersignin)
- [ClearBrowsingDataOnExit](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#clearbrowsingdataonexit) 
- [ClickOnceEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#clickonceenabled)
- [CommandLineFlagSecurityWarningsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#commandlineflagsecuritywarningsenabled)
- [ConfigureOnPremisesAccountAutoSignIn](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configureonpremisesaccountautosignin)
- [ConfigureShare](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configureshare)
- [CookiesAllowedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#cookiesallowedforurls)
- [CustomHelpLink](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#customhelplink)
- [DefaultCookiesSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultcookiessetting)
- [DefaultGeolocationSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultgeolocationsetting)
- [DefaultImagesSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultimagessetting)
- [DefaultInsecureContentSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultinsecurecontentsetting)
- [DefaultJavaScriptSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultjavascriptsetting)
- [DefaultNotificationsSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultnotificationssetting)
- [DefaultPluginsSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultpluginssetting)
- [DefaultPopupsSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultpopupssetting)
- [DefaultSearchProviderEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultsearchproviderenabled)
- [DefaultWebBluetoothGuardSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultwebbluetoothguardsetting)
- [DefaultWebUsbGuardSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultwebusbguardsetting)
- [DelayNavigationsForInitialSiteListDownload](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#delaynavigationsforinitialsitelistdownload)
- [DeveloperToolsAvailability](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#developertoolsavailability)
- [EnableSha1ForLocalAnchors](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enablesha1forlocalanchors)
- [DownloadRestrictions](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#downloadrestrictions)
- [EnableDeprecatedWebPlatformFeatures](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enabledeprecatedwebplatformfeatures)
- [WinHttpProxyResolverEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#winhttpproxyresolverenabled)
- [ExperimentationAndConfigurationServiceControl](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#experimentationandconfigurationservicecontrol)
- [ExternalProtocolDialogShowAlwaysOpenCheckbox](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#externalprotocoldialogshowalwaysopencheckbox)
- [ExtensionInstallForcelist](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#extensioninstallforcelist)
- [ForceBingSafeSearch](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forcebingsafesearch)
- [ForceYouTubeRestrict](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forceyoutuberestrict)
- [HomepageIsNewTabPage](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#homepageisnewtabpage)
- [HomepageLocation](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#homepagelocation)
- [InPrivateModeAvailability](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#inprivatemodeavailability)
- [InternetExplorerIntegrationEnhancedHangDetection](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationenhancedhangdetection)
- [InternetExplorerIntegrationLevel](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationlevel)
- [InternetExplorerIntegrationSiteRedirect](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationsiteredirect)
- [LegacySameSiteCookieBehaviorEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#legacysamesitecookiebehaviorenabled)
- [NativeWindowOcclusionEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#nativewindowocclusionenabled)
- [NavigationDelayForInitialSiteListDownloadTimeout](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#navigationdelayforinitialsitelistdownloadtimeout)
- [NetworkPredictionOptions](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#networkpredictionoptions)
- [NewTabPageLocation](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagelocation)
- [NewTabPageSearchBox](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagesearchbox)
- [NewTabPageSetFeedType](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagesetfeedtype)
- [NonRemovableProfileEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#nonremovableprofileenabled)
- [PasswordProtectionWarningTrigger](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#passwordprotectionwarningtrigger)
- [PasswordProtectionLoginURLs](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#passwordprotectionloginurls)
- [PasswordProtectionChangePasswordURL](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#passwordprotectionchangepasswordurl)
- [PluginsAllowedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#pluginsallowedforurls)
- [PluginsBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#pluginsblockedforurls)
- [PreventSmartScreenPromptOverride](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#preventsmartscreenpromptoverride)
- [PreventSmartScreenPromptOverrideForFiles](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#preventsmartscreenpromptoverrideforfiles)
- [ProxyMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxymode)
- [RegisteredProtocolHandlers](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#registeredprotocolhandlers)
- [RelaunchNotification](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#relaunchnotification)
- [RestoreOnStartup](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#restoreonstartup)
- [RestoreOnStartupURLs](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#restoreonstartupurls)
- [RestrictSigninToPattern](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#restrictsignintopattern)
- [SSLVersionMin](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sslversionmin)
- [SmartScreenAllowListDomains](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#smartscreenallowlistdomains)
- [SmartScreenEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#smartscreenenabled)
- [SmartScreenForTrustedDownloadsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#smartscreenfortrusteddownloadsenabled)
- [SmartScreenPuaEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#smartscreenpuaenabled)
- [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled)
- [TrackingPrevention](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#trackingprevention)
- [WebRtcLocalhostIpHandling](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webrtclocalhostiphandling)

<!-- end 86 -->

## Version 85.0.564.41: August 25

Verschiedene Bugs und Leistungsprobleme wurden behoben.

## Version 85.0.564.40: 21. August

Verschiedene Bugs und Leistungsprobleme wurden behoben.

## Version 85.0.564.36: 17. August

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## Version 85.0.564.30: 10. August

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## Version 85.0.564.23: 3. August

Verschiedene Fehler und Leistungsprobleme wurden behoben.

<!--- Archived to version 85.0.564.18: July 28 ---->

## Weitere Informationen

- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)
