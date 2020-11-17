---
title: Dokumentation für die Microsoft Edge Browserrichtlinie
ms.author: stmoody
author: dan-wesley
manager: tahills
ms.date: 11/13/2020
audience: ITPro
ms.topic: reference
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
ms.custom: ''
description: Windows- und Mac-Dokumentation für alle vom Microsoft Edge Browser unterstützten Richtlinien
ms.openlocfilehash: e191d9487a0e6c0d72f2f4b47d6b6c413449cb71
ms.sourcegitcommit: 2b6808a4d1878fd2da886f9c6c56f592c6b200e1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/13/2020
ms.locfileid: "11168800"
---
# Microsoft Edge-Richtlinien

Die neueste Version von Microsoft Edge umfasst die folgenden Richtlinien. Sie können diese Richtlinien verwenden, um zu konfigurieren, wie Microsoft Edge in Ihrer Organisation ausgeführt wird.

Informationen zu einer zusätzlichen Richtlinie, mit der Sie steuern können, wie und wann Microsoft Edge aktualisiert wird, finden Sie unter [Microsoft Edge Updaterichtlinien-Referenz](microsoft-edge-update-policies.md).

Sie können das [Microsoft Security Compliance Toolkit](https://www.microsoft.com/download/details.aspx?id=55319) für die empfohlenen grundlegenden Sicherheitskonfigurations-Einstellungen für Microsoft Edge herunterladen. Weitere Informationen finden Sie unter [Microsoft Sicherheitsbaselines-Blog](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/bg-p/Microsoft-Security-Baselines).

> [!NOTE]
> Dieser Artikel bezieht sich auf Microsoft Edge Version 77 oder neuer.

## Verfügbare Richtlinien

In dieser Tabelle sind sämtliche, in dieser Version von Microsoft Edge verfügbaren Browser-bezogenen Gruppenrichtlinien aufgeführt. Über die Links in der folgenden Tabelle erhalten Sie weitere Einzelheiten zu bestimmten Richtlinien.

|||
|-|-|
|[Application Guard-Einstellungen](#application-guard-settings)|[Cast](#cast)|
|[Einstellungen für den Inhalt](#content-settings)|[Standardmäßiger Suchdienstanbieter](#default-search-provider)|
|[Extensions](#extensions)|[HTTP-Authentifizierung](#http-authentication)|
|[Einstellungen für den Kioskmodus](#kiosk-mode-settings)|[Systemeigenes Messaging](#native-messaging)|
|[Kennwort-Manager und Schutz](#password-manager-and-protection)|[Leistung](#performance)|
|[Drucken](#printing)|[Proxyserver](#proxy-server)|
|[SmartScreen-Einstellungen](#smartscreen-settings)|[Start, Startseite und neue Registerkarte](#startup-home-page-and-new-tab-page)|
|[Sonstiges](#additional)|

### [*Application Guard-Einstellungen*](#application-guard-settings-policies)

|Richtlinienname|Beschriftung|
|-|-|
|[ApplicationGuardContainerProxy](#applicationguardcontainerproxy)|Application Guard-Containerproxy|
### [*Cast*](#cast-policies)

|Richtlinienname|Beschriftung|
|-|-|
|[EnableMediaRouter](#enablemediarouter)|Google Cast aktivieren|
|[ShowCastIconInToolbar](#showcasticonintoolbar)|Anzeigen des Cast-Symbols in der Symbolleiste|
### [*Einstellungen für den Inhalt*](#content-settings-policies)

|Richtlinienname|Beschriftung|
|-|-|
|[AutoSelectCertificateForUrls](#autoselectcertificateforurls)|Automatisches Auswählen von Clientzertifikaten für diese Websites|
|[CookiesAllowedForUrls](#cookiesallowedforurls)|Erlauben von Cookies auf bestimmten Websites|
|[CookiesBlockedForUrls](#cookiesblockedforurls)|Blockieren von Cookies auf bestimmten Websites|
|[CookiesSessionOnlyForUrls](#cookiessessiononlyforurls)|Einschränken von Cookies von bestimmten Websites auf die aktuelle Sitzung|
|[DefaultCookiesSetting](#defaultcookiessetting)|Configure cookies|
|[DefaultFileSystemReadGuardSetting](#defaultfilesystemreadguardsetting)|Steuern der Verwendung der Datei-System-API für den Lesezugriff|
|[DefaultFileSystemWriteGuardSetting](#defaultfilesystemwriteguardsetting)|Steuern der Verwendung der Datei-System-API für den Schreibzugriff|
|[DefaultGeolocationSetting](#defaultgeolocationsetting)|Standardeinstellung für Geolocation|
|[DefaultImagesSetting](#defaultimagessetting)|Standardeinstellung für Bilder|
|[DefaultInsecureContentSetting](#defaultinsecurecontentsetting)|Verwendung von unsicheren Inhaltsausnahmen steuern|
|[DefaultJavaScriptSetting](#defaultjavascriptsetting)|Standardeinstellung für JavaScript|
|[DefaultNotificationsSetting](#defaultnotificationssetting)|Standardeinstellung für Benachrichtigungen|
|[DefaultPluginsSetting](#defaultpluginssetting)|Standardeinstellung für Adobe Flash|
|[DefaultPopupsSetting](#defaultpopupssetting)|Standardeinstellung für Popupfenster|
|[DefaultWebBluetoothGuardSetting](#defaultwebbluetoothguardsetting)|Steuern der Verwendung der Web-Bluetooth-API|
|[DefaultWebUsbGuardSetting](#defaultwebusbguardsetting)|Steuern der Verwendung der WebUSB-API|
|[FileSystemReadAskForUrls](#filesystemreadaskforurls)|Lesezugriff über die Datei-System-API auf diesen Websites zulassen|
|[FileSystemReadBlockedForUrls](#filesystemreadblockedforurls)|Lesezugriff über die Datei-System-API auf diesen Websites blockieren|
|[FileSystemWriteAskForUrls](#filesystemwriteaskforurls)|Schreibzugriff auf Dateien und Verzeichnisse auf diesen Websites zulassen|
|[FileSystemWriteBlockedForUrls](#filesystemwriteblockedforurls)|Schreibzugriff auf Dateien und Verzeichnisse auf diesen Websites blockieren|
|[ImagesAllowedForUrls](#imagesallowedforurls)|Zulassen von Bildern auf diesen Websites|
|[ImagesBlockedForUrls](#imagesblockedforurls)|Blockieren von Bildern auf bestimmten Websites|
|[InsecureContentAllowedForUrls](#insecurecontentallowedforurls)|Zulassen von unsicheren Inhalten auf bestimmten Websites|
|[InsecureContentBlockedForUrls](#insecurecontentblockedforurls)|Blockieren von unsicheren Inhalten auf bestimmten Websites|
|[JavaScriptAllowedForUrls](#javascriptallowedforurls)|JavaScript auf bestimmten Websites zulassen|
|[JavaScriptBlockedForUrls](#javascriptblockedforurls)|JavaScript auf bestimmten Websites blockieren|
|[LegacySameSiteCookieBehaviorEnabled](#legacysamesitecookiebehaviorenabled)|Standardeinstellung für das Verhalten von Legacy-SameSite-Cookies aktivieren|
|[LegacySameSiteCookieBehaviorEnabledForDomainList](#legacysamesitecookiebehaviorenabledfordomainlist)|Zurückkehren zum alten SameSite-Verhalten für Cookies auf bestimmten Websites|
|[NotificationsAllowedForUrls](#notificationsallowedforurls)|Zulassen von Benachrichtigungen bei bestimmten Websites|
|[NotificationsBlockedForUrls](#notificationsblockedforurls)|Blockieren von Benachrichtigungen für bestimmte Websites|
|[PluginsAllowedForUrls](#pluginsallowedforurls)|Zulassen des Adobe Flash-Plug-Ins auf bestimmten Websites|
|[PluginsBlockedForUrls](#pluginsblockedforurls)|Blockieren des Adobe Flash-Plug-Ins auf bestimmten Websites|
|[PopupsAllowedForUrls](#popupsallowedforurls)|Popupfenster auf bestimmten Websites zulassen|
|[PopupsBlockedForUrls](#popupsblockedforurls)|Popupfenster auf bestimmten Websites blockieren|
|[RegisteredProtocolHandlers](#registeredprotocolhandlers)|Registrieren von Protokollhandlern|
|[SpotlightExperiencesAndRecommendationsEnabled](#spotlightexperiencesandrecommendationsenabled)|Wählen Sie aus, ob Benutzer personalisierte Hintergrundbilder und Text, Vorschläge, Benachrichtigungen
und Tipps für Microsoft-Dienste erhalten können.|
|[WebUsbAllowDevicesForUrls](#webusballowdevicesforurls)|Bestimmten Websites die Herstellung einer Verbindung zu bestimmten USB-Geräten gewähren.|
|[WebUsbAskForUrls](#webusbaskforurls)|Erlauben von WebUSB auf bestimmten Websites|
|[WebUsbBlockedForUrls](#webusbblockedforurls)|Blockieren von WebUSB auf bestimmten Websites|
### [*Standardmäßiger Suchdienstanbieter*](#default-search-provider-policies)

|Richtlinienname|Beschriftung|
|-|-|
|[DefaultSearchProviderEnabled](#defaultsearchproviderenabled)|Standardmäßigen Suchdienstanbieter aktivieren|
|[DefaultSearchProviderEncodings](#defaultsearchproviderencodings)|Verschlüsselung standardmäßiger Suchdienstanbieter|
|[DefaultSearchProviderImageURL](#defaultsearchproviderimageurl)|Spezifiziert das Feature „Suche nach Bild“ für den standardmäßigen Suchanbieter|
|[DefaultSearchProviderImageURLPostParams](#defaultsearchproviderimageurlpostparams)|Parameter für eine Bild-URL, die POST verwendet|
|[DefaultSearchProviderKeyword](#defaultsearchproviderkeyword)|Schlüsselwort standardmäßiger Suchdienstanbieter|
|[DefaultSearchProviderName](#defaultsearchprovidername)|Name des standardmäßigen Suchdienstanbieters|
|[DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl)|Such-URL des standardmäßigen Suchdienstanbieters|
|[DefaultSearchProviderSuggestURL](#defaultsearchprovidersuggesturl)|URL des standardmäßigen Suchdienstanbieters für Vorschläge|
|[NewTabPageSearchBox](#newtabpagesearchbox)|Konfigurieren das neuen Suchfeld für die Registerkartenoberfläche |
### [*Extensions*](#extensions-policies)

|Richtlinienname|Beschriftung|
|-|-|
|[ExtensionAllowedTypes](#extensionallowedtypes)|Konfigurieren von zulässigen Erweiterungstypen|
|[ExtensionInstallAllowlist](#extensioninstallallowlist)|Zulassen, dass bestimmte Erweiterungen installiert werden|
|[ExtensionInstallBlocklist](#extensioninstallblocklist)|Steuern, welche Erweiterungen nicht installiert werden können|
|[ExtensionInstallForcelist](#extensioninstallforcelist)|Steuern, welche Erweiterungen im Hintergrund installiert werden|
|[ExtensionInstallSources](#extensioninstallsources)|Konfigurieren von Erweiterungen und Installationsquellen für Benutzerskripts|
|[ExtensionSettings](#extensionsettings)|Konfigurieren der Erweiterungsverwaltungseinstellungen|
### [*HTTP-Authentifizierung*](#http-authentication-policies)

|Richtlinienname|Beschriftung|
|-|-|
|[AllowCrossOriginAuthPrompt](#allowcrossoriginauthprompt)|Zulassen ursprungsübergreifender HTTP-Authentifizierungsaufforderungen|
|[AuthNegotiateDelegateAllowlist](#authnegotiatedelegateallowlist)|Gibt eine Liste der Server an, an die Microsoft Edge Benutzeranmeldeinformationen delegieren kann|
|[AuthSchemes](#authschemes)|Unterstützte Authentifizierungsschemas|
|[AuthServerAllowlist](#authserverallowlist)|Konfigurieren der Liste der zulässigen Authentifizierungsserver|
|[DisableAuthNegotiateCnameLookup](#disableauthnegotiatecnamelookup)|Deaktivieren des CNAME-Lookup beim Verhandeln der Kerberos-Authentifizierung|
|[EnableAuthNegotiatePort](#enableauthnegotiateport)|Einschließen eines nicht standardmäßigen Ports in Kerberos-SPN|
|[NtlmV2Enabled](#ntlmv2enabled)|Steuern, ob die NTLMv2-Authentifizierung aktiviert ist|
### [*Einstellungen für den Kioskmodus*](#kiosk-mode-settings-policies)

|Richtlinienname|Beschriftung|
|-|-|
|[KioskAddressBarEditingEnabled](#kioskaddressbareditingenabled)|Konfigurieren der Adressleistenbearbeitung für die öffentliche Browsernutzung im Kioskmodus.|
|[KioskDeleteDownloadsOnExit](#kioskdeletedownloadsonexit)|Löschen von Dateien, die während einer Kiosk-Sitzung heruntergeladen wurden, wenn Microsoft Edge geschlossen wird|
### [*Systemeigenes Messaging*](#native-messaging-policies)

|Richtlinienname|Beschriftung|
|-|-|
|[NativeMessagingAllowlist](#nativemessagingallowlist)|Steuern, welche systemeigenen Messaging-Hosts Benutzer verwenden können|
|[NativeMessagingBlocklist](#nativemessagingblocklist)|Konfigurieren der systemeigenen Nachrichten-Sperrliste|
|[NativeMessagingUserLevelHosts](#nativemessaginguserlevelhosts)|Zulassen systemeigener Messaging-Hosts auf Benutzerebene (ohne Administratorberechtigungen installiert)|
### [*Kennwort-Manager und Schutz*](#password-manager-and-protection-policies)

|Richtlinienname|Beschriftung|
|-|-|
|[PasswordManagerEnabled](#passwordmanagerenabled)|Aktivieren des Speicherung von Kennwörtern im Kennwort-Manager|
|[PasswordMonitorAllowed](#passwordmonitorallowed)|Zulassen, dass Benutzer benachrichtigt werden, wenn Ihre Kennwörter als unsicher eingestuft werden|
|[PasswordProtectionChangePasswordURL](#passwordprotectionchangepasswordurl)|Konfigurieren der URL für das Ändern eines Kennworts|
|[PasswordProtectionLoginURLs](#passwordprotectionloginurls)|Konfigurieren Sie die Liste der Unternehmens-Login-URLs, bei denen der Kennwortschutzdienst gesalzene Hashes eines Kennworts sammeln soll|
|[PasswordProtectionWarningTrigger](#passwordprotectionwarningtrigger)|Auslösung der Warnung zum Kennwortschutz konfigurieren|
|[PasswordRevealEnabled](#passwordrevealenabled)|Schaltfläche „Kennwort anzeigen“ aktivieren|
### [*Leistung*](#performance-policies)

|Richtlinienname|Beschriftung|
|-|-|
|[StartupBoostEnabled](#startupboostenabled)|Startbeschleunigung aktivieren|
### [*Drucken*](#printing-policies)

|Richtlinienname|Beschriftung|
|-|-|
|[DefaultPrinterSelection](#defaultprinterselection)|Regeln zur Auswahl des Standarddruckers|
|[PrintHeaderFooter](#printheaderfooter)|Drucken von Kopf- und Fußzeilen|
|[PrintPreviewUseSystemDefaultPrinter](#printpreviewusesystemdefaultprinter)|Standarddrucker des Systems als Standarddrucker festlegen|
|[PrintingEnabled](#printingenabled)|Drucken aktivieren|
|[PrintingPaperSizeDefault](#printingpapersizedefault)|Standardmäßiges Seitenformat für den Druck|
|[UseSystemPrintDialog](#usesystemprintdialog)|Drucken über das System-Dialogfeld „Drucken“|
### [*Proxyserver*](#proxy-server-policies)

|Richtlinienname|Beschriftung|
|-|-|
|[ProxyBypassList](#proxybypasslist)|Proxy-Umgehungsregeln konfigurieren (veraltet)|
|[ProxyMode](#proxymode)|Proxyservereinstellungen konfigurieren (veraltet)|
|[ProxyPacUrl](#proxypacurl)|Proxy-.pac-Datei-URL festlegen (veraltet)|
|[ProxyServer](#proxyserver)|Adresse oder URL von Proxyservern konfigurieren (veraltet)|
|[ProxySettings](#proxysettings)|Proxyeinstellungen|
### [*SmartScreen-Einstellungen*](#smartscreen-settings-policies)

|Richtlinienname|Beschriftung|
|-|-|
|[PreventSmartScreenPromptOverride](#preventsmartscreenpromptoverride)|Umgehung der Microsoft Defender SmartScreen-Aufforderungen für Websites verhindern|
|[PreventSmartScreenPromptOverrideForFiles](#preventsmartscreenpromptoverrideforfiles)|Verhindern der Umgehung von Microsoft Defender-SmartScreen-Warnungen zu Downloads|
|[SmartScreenAllowListDomains](#smartscreenallowlistdomains)|Konfigurieren der Liste der Domänen, für die Microsoft Defender-SmartScreen keine Warnungen auslöst|
|[SmartScreenEnabled](#smartscreenenabled)|Konfigurieren des Microsoft Defender SmartScreen|
|[SmartScreenForTrustedDownloadsEnabled](#smartscreenfortrusteddownloadsenabled)|Erzwingen der Microsoft Defender-SmartScreen-Überprüfung für Downloads aus vertrauenswürdigen Quellen|
|[SmartScreenPuaEnabled](#smartscreenpuaenabled)|Konfigurieren von Microsoft Defender SmartScreen, sodass potenziell unerwünschte Apps blockiert werden|
### [*Start&comma; Startseite und neue Registerkarte*](#startup-home-page-and-new-tab-page-policies)

|Richtlinienname|Beschriftung|
|-|-|
|[HomepageIsNewTabPage](#homepageisnewtabpage)|Festlegen einer neuen Registerkarte als Startseite|
|[HomepageLocation](#homepagelocation)|Konfigurieren der Startseiten-URL|
|[NewTabPageAllowedBackgroundTypes](#newtabpageallowedbackgroundtypes)|Konfigurieren der für das neue Registerkartenseiten-Layout zulässigen Hintergrundtypen|
|[NewTabPageCompanyLogo](#newtabpagecompanylogo)|Firmenlogo für „Neuer Tab“-Seite festlegen (veraltet)|
|[NewTabPageHideDefaultTopSites](#newtabpagehidedefaulttopsites)|Ausblenden der standardmäßigen Top-Websites auf der neuen Registerkartenseite|
|[NewTabPageLocation](#newtabpagelocation)|Konfigurieren der URL der neuen Registerkartenseite|
|[NewTabPageManagedQuickLinks](#newtabpagemanagedquicklinks)|Festlegen der Quicklinks auf der neuen Registerkartenseite|
|[NewTabPagePrerenderEnabled](#newtabpageprerenderenabled)|Aktivieren des Vorabladens der neuen Registerkarte für schnellere Darstellung|
|[NewTabPageSetFeedType](#newtabpagesetfeedtype)|Konfigurieren der neuen Registerkartenoberfläche für Microsoft Edge (veraltet)|
|[RestoreOnStartup](#restoreonstartup)|Auszuführende Aktion beim Start|
|[RestoreOnStartupURLs](#restoreonstartupurls)|Websites, die beim Start des Browsers geöffnet werden sollen|
|[ShowHomeButton](#showhomebutton)|Schaltfläche „Start“ auf der Symbolleiste anzeigen|
### [*Sonstiges*](#additional-policies)

|Richtlinienname|Beschriftung|
|-|-|
|[AddressBarMicrosoftSearchInBingProviderEnabled](#addressbarmicrosoftsearchinbingproviderenabled)|Aktivieren von Microsoft Search in Bing-Vorschlägen in der Adressleiste|
|[AdsSettingForIntrusiveAdsSites](#adssettingforintrusiveadssites)|Anzeigeneinstellung für Websites mit aufdringlichen Anzeigen|
|[AllowDeletingBrowserHistory](#allowdeletingbrowserhistory)|Löschen des Browser- und Downloadverlaufs aktivieren|
|[AllowFileSelectionDialogs](#allowfileselectiondialogs)|Dialogfelder „Dateiauswahl“ zulassen|
|[AllowPopupsDuringPageUnload](#allowpopupsduringpageunload)|Ermöglicht es einer Seite, Popups während ihrer Entladung anzuzeigen|
|[AllowSurfGame](#allowsurfgame)|Surfspiel zulassen|
|[AllowSyncXHRInPageDismissal](#allowsyncxhrinpagedismissal)|Seiten das Senden synchroner XHR-Anforderungen während der Seitenschließung ermöglichen (veraltet)|
|[AllowTokenBindingForUrls](#allowtokenbindingforurls)|Konfigurieren Sie die Liste der Websites, für die Microsoft Edge versucht, eine Tokenbindung einzurichten.|
|[AllowTrackingForUrls](#allowtrackingforurls)|Konfigurieren der Ausnahmen für die Nachverfolgungs-Vorbeugung für bestimmte Websites|
|[AlternateErrorPagesEnabled](#alternateerrorpagesenabled)|Ähnliche Seiten vorschlagen, wenn eine Webseite nicht gefunden werden kann|
|[AlwaysOpenPdfExternally](#alwaysopenpdfexternally)|PDF-Dateien immer extern öffnen|
|[AmbientAuthenticationInPrivateModesEnabled](#ambientauthenticationinprivatemodesenabled)|Aktivieren der Umgebungsauthentifizierung für InPrivate- und Gastprofile|
|[AppCacheForceEnabled](#appcacheforceenabled)|Ermöglicht das erneute Aktivieren des AppCache-Features, auch wenn es standardmäßig deaktiviert ist|
|[ApplicationLocaleValue](#applicationlocalevalue)|Festlegen des Anwendungsgebietsschemas|
|[AudioCaptureAllowed](#audiocaptureallowed)|Audio-Aufnahme zulassen oder blockieren|
|[AudioCaptureAllowedUrls](#audiocaptureallowedurls)|Websites, die auf Audio-Aufnahmegeräte zugreifen können, ohne eine Berechtigung anfordern zu müssen|
|[AudioSandboxEnabled](#audiosandboxenabled)|Audio-Sandkasten ausführen lassen|
|[AutoImportAtFirstRun](#autoimportatfirstrun)|Automatisches Importieren der Daten und Einstellungen eines anderen Browsers bei der ersten Ausführung|
|[AutoLaunchProtocolsFromOrigins](#autolaunchprotocolsfromorigins)|Eine Liste der Protokolle definieren, mit denen eine externe Anwendung von den aufgeführten Ursprüngen aus gestartet werden kann, ohne den Benutzer aufzufordern|
|[AutoOpenAllowedForURLs](#autoopenallowedforurls)|URLs, auf die AutoOpenFileTypes angewendet werden können|
|[AutoOpenFileTypes](#autoopenfiletypes)|Liste der Dateitypen, die beim Download automatisch geöffnet werden sollen|
|[AutofillAddressEnabled](#autofilladdressenabled)|Automatisches Ausfüllen von Adressen zulassen|
|[AutofillCreditCardEnabled](#autofillcreditcardenabled)|AutoFill für Kreditkartendaten aktivieren|
|[AutoplayAllowed](#autoplayallowed)|Zulassen der automatischen Wiedergabe von Medien für Websites|
|[BackgroundModeEnabled](#backgroundmodeenabled)|Ausführung von Hintergrund-Apps zulassen, nachdem Microsoft Edge geschlossen wurde|
|[BackgroundTemplateListUpdatesEnabled](#backgroundtemplatelistupdatesenabled)|Aktiviert Hintergrundaktualisierungen der Liste verfügbarer Vorlagen für Kollektionen und andere Features, die Vorlagen verwenden|
|[BingAdsSuppression](#bingadssuppression)|Blockieren aller Anzeigen in Bing-Suchergebnissen|
|[BlockThirdPartyCookies](#blockthirdpartycookies)|Blockieren der Cookies von Drittanbietern|
|[BrowserAddProfileEnabled](#browseraddprofileenabled)|Aktivieren der Profilerstellung im Flyout „Identität“ oder auf der Seite „Einstellungen“|
|[BrowserGuestModeEnabled](#browserguestmodeenabled)|Gastmodus aktivieren|
|[BrowserNetworkTimeQueriesEnabled](#browsernetworktimequeriesenabled)|Abfragen an einen Browser Netzwerk-Zeitdienst zulassen|
|[BrowserSignin](#browsersignin)|Browser-Anmeldungseinstellungen|
|[BuiltInDnsClientEnabled](#builtindnsclientenabled)|Verwenden des integrierten DNS-Clients|
|[BuiltinCertificateVerifierEnabled](#builtincertificateverifierenabled)|Bestimmt, ob die integrierte Zertifikatprüfung zum Überprüfen von Serverzertifikaten verwendet wird (veraltet)|
|[CertificateTransparencyEnforcementDisabledForCas](#certificatetransparencyenforcementdisabledforcas)|Deaktivieren der Erzwingung der Zertifikattransparenz für eine Liste mit subjectPublicKeyInfo-Hashwerten|
|[CertificateTransparencyEnforcementDisabledForLegacyCas](#certificatetransparencyenforcementdisabledforlegacycas)|Deaktivieren der Erzwingung der Zertifikattransparenz für eine Liste mit Legacy-Zertifizierungsstellen|
|[CertificateTransparencyEnforcementDisabledForUrls](#certificatetransparencyenforcementdisabledforurls)|Deaktivieren der Erzwingung der Zertifikattransparenz für bestimmte URLs|
|[ClearBrowsingDataOnExit](#clearbrowsingdataonexit)|Löschen der Browsingdaten beim Schließen von Microsoft Edge|
|[ClearCachedImagesAndFilesOnExit](#clearcachedimagesandfilesonexit)|Löschen von zwischengespeicherten Bildern und Dateien, wenn Microsoft Edge geschlossen wird|
|[ClickOnceEnabled](#clickonceenabled)|Benutzern das Öffnen von Dateien mithilfe des ClickOnce-Protokolls gestatten|
|[CollectionsServicesAndExportsBlockList](#collectionsservicesandexportsblocklist)|Blockieren des Zugriffs auf eine bestimmte Liste von Diensten und Exportieren von Zielen in Sammlungen|
|[CommandLineFlagSecurityWarningsEnabled](#commandlineflagsecuritywarningsenabled)|Aktivieren von Sicherheitswarnungen für Befehlszeilen Kennzeichnungen|
|[ComponentUpdatesEnabled](#componentupdatesenabled)|Aktivieren von Komponentenupdates in Microsoft Edge|
|[ConfigureDoNotTrack](#configuredonottrack)|DNT konfigurieren|
|[ConfigureFriendlyURLFormat](#configurefriendlyurlformat)|Konfigurieren des Standardformats für das Einfügen von URLs, die aus MicrosoftEdge kopiert wurden, und zum Ermitteln, ob Benutzern weitere Formate zur Verfügung stehen|
|[ConfigureOnPremisesAccountAutoSignIn](#configureonpremisesaccountautosignin)|Konfiguration der automatischen Anmeldung mit einem Active Directory-Domänenkonto, wenn kein Azure AD-Domänenkonto vorhanden ist|
|[ConfigureOnlineTextToSpeech](#configureonlinetexttospeech)|Konfiguration von Text-zu-Sprache Online|
|[ConfigureShare](#configureshare)|Konfiguration der Freigabeoberfläche|
|[CustomHelpLink](#customhelplink)|Benutzerdefinierten „Hilfe“-Link konfigurieren|
|[DNSInterceptionChecksEnabled](#dnsinterceptionchecksenabled)|DNS-Interception-Prüfungen aktiviert|
|[DefaultBrowserSettingEnabled](#defaultbrowsersettingenabled)|Festlegen von Microsoft Edge als Standardbrowser|
|[DefaultSearchProviderContextMenuAccessAllowed](#defaultsearchprovidercontextmenuaccessallowed)|Zugriff auf das Kontextmenü des Standardsuchanbieters zulassen|
|[DefaultSensorsSetting](#defaultsensorssetting)|Standardeinstellung für Sensoren|
|[DefaultSerialGuardSetting](#defaultserialguardsetting)|Steuerung der Verwendung der Serial-API|
|[DelayNavigationsForInitialSiteListDownload](#delaynavigationsforinitialsitelistdownload)|Voraussetzen, dass die Enterprise Mode Site List vor der Registerkartennavigation verfügbar ist|
|[DeleteDataOnMigration](#deletedataonmigration)|Löschen alter Browserdaten bei der Migration|
|[DeveloperToolsAvailability](#developertoolsavailability)|Steuern, wo Entwicklertools verwendet werden können|
|[DiagnosticData](#diagnosticdata)|Senden erforderlicher und optionaler Diagnosedaten zur Browsernutzung|
|[DirectInvokeEnabled](#directinvokeenabled)|Benutzern das Öffnen von Dateien mithilfe des DirectInvoke-Protokolls gestatten|
|[Disable3DAPIs](#disable3dapis)|Deaktivieren der Unterstützung für 3D-Grafik-APIs|
|[DisableScreenshots](#disablescreenshots)|Deaktivieren der Anfertigung von Screenshots|
|[DiskCacheDir](#diskcachedir)|Festlegen des Datenträgercache Verzeichnisses|
|[DiskCacheSize](#diskcachesize)|Festlegen der Datenträgercachegröße, in Bytes|
|[DnsOverHttpsMode](#dnsoverhttpsmode)|Steuern des Modus von „DNS-over-HTTPS“|
|[DnsOverHttpsTemplates](#dnsoverhttpstemplates)|Geben Sie die URI-Vorlage des gewünschten DNS-over-HTTPS-Resolvers an|
|[Download Directory](#downloaddirectory)|Downloadverzeichnis festlegen|
|[DownloadRestrictions](#downloadrestrictions)|Downloadbeschränkungen zulassen|
|[EdgeCollectionsEnabled](#edgecollectionsenabled)|Aktivieren des Features „Sammlungen“|
|[EdgeShoppingAssistantEnabled](#edgeshoppingassistantenabled)|Einkaufen in Microsoft Edge aktiviert|
|[EditFavoritesEnabled](#editfavoritesenabled)|Ermöglicht Benutzern das Bearbeiten von Favoriten|
|[EnableDeprecatedWebPlatformFeatures](#enabledeprecatedwebplatformfeatures)|Re-enable deprecated web platform features for a limited time (obsolete)|
|[EnableDomainActionsDownload](#enabledomainactionsdownload)|Herunterladen aktivieren von Domänenaktionen von Microsoft (veraltet)|
|[EnableOnlineRevocationChecks](#enableonlinerevocationchecks)|Aktivieren von Online-OCSP-/CRL-Prüfungen|
|[EnableSha1ForLocalAnchors](#enablesha1forlocalanchors)|Zulassen von Zertifikaten, die mit SHA-1 signiert wurden, wenn sie von lokalen Vertrauensankern ausgegeben wurden (veraltet).|
|[EnterpriseHardwarePlatformAPIEnabled](#enterprisehardwareplatformapienabled)|Zulassen der Verwendung der Enterprise-Hardware Plattform-API für verwaltete Erweiterungen|
|[EnterpriseModeSiteListManagerAllowed](#enterprisemodesitelistmanagerallowed)|Zugriff auf das Enterprise Mode Site List Manager-Tool ulassen|
|[ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](#exemptdomainfiletypepairsfromfiletypedownloadwarnings)|Herunterladen deaktivieren von Warnungen basierend auf Dateierweiterungen für bestimmte Dateitypen in Domänen|
|[ExperimentationAndConfigurationServiceControl](#experimentationandconfigurationservicecontrol)|Steuern der Kommunikation mit dem Experimentier- und Konfigurationsservice|
|[ExternalProtocolDialogShowAlwaysOpenCheckbox](#externalprotocoldialogshowalwaysopencheckbox)|Anzeigen eines „immer öffnen“-Kontrollkästchens im externen Protokoll-Dialog|
|[FamilySafetySettingsEnabled](#familysafetysettingsenabled)|Zulassen, dass Benutzer Family Safety konfigurieren|
|[FavoritesBarEnabled](#favoritesbarenabled)|Aktivieren der Favoritenleiste|
|[ForceBingSafeSearch](#forcebingsafesearch)|Erzwingen von Bing SafeSearch|
|[ForceCertificatePromptsOnMultipleMatches](#forcecertificatepromptsonmultiplematches)|Konfigurieren, ob Microsoft Edge automatisch ein Zertifikat auswählen soll, wenn mehrere Zertifikat-Übereinstimmungen für eine Website vorhanden sind, die mit „AutoSelectCertificateForUrls“ konfiguriert ist|
|[ForceEphemeralProfiles](#forceephemeralprofiles)|Verwendung von kurzlebigen Profilen zulassen|
|[ForceGoogleSafeSearch](#forcegooglesafesearch)|Google SafeSearch erzwingen|
|[ForceLegacyDefaultReferrerPolicy](#forcelegacydefaultreferrerpolicy)|Verwenden Sie die standardmäßige Verweiserrichtlinie „kein Verweiser beim Downgrade“ (veraltet)|
|[ForceNetworkInProcess](#forcenetworkinprocess)|Erzwingen der Ausführung des Netzwerkcodes im Browserprozess (veraltet)|
|[ForceSync](#forcesync)|Synchronisierung von Browserdaten erzwingen und Zustimmungsaufforderung für die Synchronisierung nicht anzeigen|
|[ForceYouTubeRestrict](#forceyoutuberestrict)|Erzwingen des minimal eingeschränkten Modus für YouTube|
|[FullscreenAllowed](#fullscreenallowed)|Vollbild-Modus zulassen|
|[GloballyScopeHTTPAuthCacheEnabled](#globallyscopehttpauthcacheenabled)|Aktivieren von globalem HTTP-Authentifizierungscache|
|[GoToIntranetSiteForSingleWordEntryInAddressBar](#gotointranetsiteforsinglewordentryinaddressbar)|Erzwingen der direkten Intranet-Websitenavigation anstelle der Suche nach Einzelwort-Einträgen in der Adressleiste|
|[HSTSPolicyBypassList](#hstspolicybypasslist)|Konfigurieren der Liste der Namen, die die HSTS-Richtlinienüberprüfung umgehen|
|[HardwareAccelerationModeEnabled](#hardwareaccelerationmodeenabled)|Verwenden der Hardwarebeschleunigung, falls verfügbar|
|[HideFirstRunExperience](#hidefirstrunexperience)|Unterdrücken der ersten Ausführungsumgebung und des Begrüßungsbildschirms|
|[HideInternetExplorerRedirectUXForIncompatibleSitesEnabled](#hideinternetexplorerredirectuxforincompatiblesitesenabled)|Ausblenden des einmaligen Dialogfelds „Umleitung“ und des Banners auf Microsoft Edge|
|[ImportAutofillFormData](#importautofillformdata)|Import von AutoFill-Formulardaten zulassen|
|[ImportBrowserSettings](#importbrowsersettings)|Import von Browsereinstellungen zulassen|
|[ImportCookies](#importcookies)|Lassen Sie den Import von Cookies zu|
|[ImportExtensions](#importextensions)|Lassen Sie den Import von Erweiterungen zu|
|[ImportFavorites](#importfavorites)|Import von Favoriten zulassen|
|[ImportHistory](#importhistory)|Import des Browserverlaufs zulassen|
|[ImportHomepage](#importhomepage)|Import von Startseiteneinstellungen zulassen|
|[ImportOpenTabs](#importopentabs)|Import von Offenen Registerkarten zulassen|
|[ImportPaymentInfo](#importpaymentinfo)|Import von Zahlungsinformationen zulassen|
|[ImportSavedPasswords](#importsavedpasswords)|Import von gespeicherten Kennwörtern zulassen|
|[ImportSearchEngine](#importsearchengine)|Import von Suchmaschinen-Einstellungen zulassen|
|[ImportShortcuts](#importshortcuts)|Lassen Sie den Import von Verknüpfungen zu|
|[InPrivateModeAvailability](#inprivatemodeavailability)|Konfigurieren der InPrivate-Modus-Verfügbarkeit|
|[InsecureFormsWarningsEnabled](#insecureformswarningsenabled)|Aktivieren von Warnungen für unsichere Formulare|
|[IntensiveWakeUpThrottlingEnabled](#intensivewakeupthrottlingenabled)|Regulierung des IntensiveWakeUpThrottlingEnabled-Features|
|[InternetExplorerIntegrationEnhancedHangDetection](#internetexplorerintegrationenhancedhangdetection)|Konfigurieren der Ermittlung von Anwendungsstillständen für Internet Explorer-Modus|
|[InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel)|Konfigurieren der Internet Explorer-Integration|
|[InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist)|Enterprise Mode Site List konfigurieren|
|[InternetExplorerIntegrationSiteRedirect](#internetexplorerintegrationsiteredirect)|Angeben, wie sich „seiteninterne“ Navigationen zu nicht konfigurierten Websites verhalten, wenn sie von Seiten im Internet Explorer-Modus gestartet werden|
|[InternetExplorerIntegrationTestingAllowed](#internetexplorerintegrationtestingallowed)|Internet Explorer-Modus-Tests zulassen|
|[IsolateOrigins](#isolateorigins)|Aktivieren der Website-Isolation für bestimmte Ursprünge|
|[LocalProvidersEnabled](#localprovidersenabled)|Vorschläge von lokalen Anbietern zulassen|
|[ManagedFavorites](#managedfavorites)|Favoriten konfigurieren|
|[ManagedSearchEngines](#managedsearchengines)|Verwalten von Suchmaschinen|
|[MaxConnectionsPerProxy](#maxconnectionsperproxy)|Maximale Anzahl gleichzeitiger Verbindungen mit dem Proxyserver|
|[MediaRouterCastAllowAllIPs](#mediaroutercastallowallips)|Zulassen, dass Google Cast eine Verbindung mit den Cast-Geräten aller IP-Adressen herstellt|
|[MetricsReportingEnabled](#metricsreportingenabled)|Aktivieren der Berichterstellung für Nutzung und Absturz (veraltet).|
|[NativeWindowOcclusionEnabled](#nativewindowocclusionenabled)|Native Window Occlusion aktivieren|
|[NavigationDelayForInitialSiteListDownloadTimeout](#navigationdelayforinitialsitelistdownloadtimeout)|Festlegen eines Zeitlimits für die Verzögerung der Registerkartennavigation für die Enterprise Mode Site List|
|[NetworkPredictionOptions](#networkpredictionoptions)|Aktivieren der Netzwerkvorhersage|
|[NonRemovableProfileEnabled](#nonremovableprofileenabled)|Konfigurieren, ob ein Benutzer immer ein Standardprofil hat, das automatisch mit seinem Geschäfts- oder Schulkonto angemeldet ist|
|[OverrideSecurityRestrictionsOnInsecureOrigin](#overridesecurityrestrictionsoninsecureorigin)|Steuern, wo Sicherheitseinschränkungen bei unsicheren Ursprüngen angewendet werden|
|[PaymentMethodQueryEnabled](#paymentmethodqueryenabled)|Websites erlauben, nach verfügbaren Zahlungsmethoden zu fragen|
|[PersonalizationReportingEnabled](#personalizationreportingenabled)|Die Personalisierung von Werbung, der Suche und von Nachrichten ermöglichen, indem der Browserverlauf an Microsoft gesendet wird|
|[PinningWizardAllowed](#pinningwizardallowed)|Assistent „an Taskleiste anheften“ zulassen|
|[ProactiveAuthEnabled](#proactiveauthenabled)|Proaktive Authentifizierung aktivieren|
|[PromotionalTabsEnabled](#promotionaltabsenabled)|Aktivieren von Promotion-Inhalten auf der gesamten Registerkarte|
|[PromptForDownloadLocation](#promptfordownloadlocation)|Fragen, wo heruntergeladene Dateien gespeichert werden sollen|
|[QuicAllowed](#quicallowed)|QUIC-Protokoll zulassen|
|[RedirectSitesFromInternetExplorerPreventBHOInstall](#redirectsitesfrominternetexplorerpreventbhoinstall)|Verhindern der Installation des BHO zum Umleiten von inkompatiblen Websites von Internet Explorer zu Microsoft Edge|
|[RedirectSitesFromInternetExplorerRedirectMode](#redirectsitesfrominternetexplorerredirectmode)|Umleiten von inkompatiblen Websites von Internet Explorer zu MicrosoftEdge|
|[RelaunchNotification](#relaunchnotification)|Einen Benutzer informieren, dass für ausstehende Updates ein Browser-Neustart empfohlen oder erforderlich ist|
|[RelaunchNotificationPeriod](#relaunchnotificationperiod)|Festlegen des Zeitraums für Aktualisierungsbenachrichtigungen|
|[RendererCodeIntegrityEnabled](#renderercodeintegrityenabled)|Aktivieren der Codeintegrität des Renderers|
|[RequireOnlineRevocationChecksForLocalAnchors](#requireonlinerevocationchecksforlocalanchors)|Angeben, ob Online-OCSP-/-CRL-Prüfungen für lokale Vertrauensanker erforderlich sind|
|[ResolveNavigationErrorsUseWebService](#resolvenavigationerrorsusewebservice)|Aktivieren der Auflösung von Navigationsfehlern mithilfe eines Webdiensts|
|[RestrictSigninToPattern](#restrictsignintopattern)|Einschränken, welche Konten als primäre Microsoft Edge-Konten verwendet werden können|
|[RoamingProfileLocation](#roamingprofilelocation)|Festlegen des Server gespeicherten Profilverzeichnisses|
|[RoamingProfileSupportEnabled](#roamingprofilesupportenabled)|Aktivieren der Verwendung von Roaming-Kopien für Microsoft Edge-Profildaten|
|[RunAllFlashInAllowMode](#runallflashinallowmode)|Erweitern der Einstellung für Adobe Flash-Inhalte auf alle Inhalte|
|[SSLErrorOverrideAllowed](#sslerroroverrideallowed)|Zulassen, dass Benutzer die HTTPS-Warnungsseite überschreiten können|
|[SSLVersionMin](#sslversionmin)|Mindestens aktivierte TLS-Version|
|[SaveCookiesOnExit](#savecookiesonexit)|Speichern von Cookies, wenn Microsoft Edge geschlossen wird|
|[SavingBrowserHistoryDisabled](#savingbrowserhistorydisabled)|Speichern des Browserverlaufs deaktivieren|
|[ScreenCaptureAllowed](#screencaptureallowed)|Bildschirmaufnahme zulassen oder verweigern|
|[ScrollToTextFragmentEnabled](#scrolltotextfragmentenabled)|Aktivieren des Scrollens zu Text, der in URL-Fragmenten angegeben ist|
|[SearchSuggestEnabled](#searchsuggestenabled)|Suchvorschläge zulassen|
|[SecurityKeyPermitAttestation](#securitykeypermitattestation)|Websites oder Domänen, für die keine Berechtigung zur Verwendung der direkten Sicherheitsschlüssel-Bestätigung erforderlich ist|
|[SendIntranetToInternetExplorer](#sendintranettointernetexplorer)|Senden aller Intranet-Seiten an Internet Explorer|
|[SendSiteInfoToImproveServices](#sendsiteinfotoimproveservices)|Senden von Siteinformationen, um die Microsoft-Dienste zu verbessern (veraltet).|
|[SensorsAllowedForUrls](#sensorsallowedforurls)|Zugriff auf Sensoren auf bestimmten Websites zulassen|
|[SensorsBlockedForUrls](#sensorsblockedforurls)|Zugriff auf Sensoren auf bestimmten Websites blockieren|
|[SerialAskForUrls](#serialaskforurls)|Die Serial-API auf bestimmten Websites zulassen|
|[SerialBlockedForUrls](#serialblockedforurls)|Die Serial-API auf bestimmten Websites blockieren|
|[ShowOfficeShortcutInFavoritesBar](#showofficeshortcutinfavoritesbar)|Microsoft Office-Verknüpfung auf der Favoritenleiste anzeigen (veraltet)|
|[SignedHTTPExchangeEnabled](#signedhttpexchangeenabled)|Unterstützung für Signed HTTP Exchange (SXG) aktivieren|
|[SitePerProcess](#siteperprocess)|Aktivieren der Website-Isolation für alle Websites|
|[SpeechRecognitionEnabled](#speechrecognitionenabled)|Configure Speech Recognition|
|[SpellcheckEnabled](#spellcheckenabled)|Rechtschreibprüfung aktivieren|
|[SpellcheckLanguage](#spellchecklanguage)|Aktivieren spezifischer Sprachen für die Rechtschreibprüfung|
|[SpellcheckLanguageBlocklist](#spellchecklanguageblocklist)|Deaktivierung der Rechtschreibprüfungssprachen erzwingen|
|[StricterMixedContentTreatmentEnabled](#strictermixedcontenttreatmentenabled)|Aktivieren der strikteren Behandlung von gemischten Inhalten (veraltet)|
|[SuppressUnsupportedOSWarning](#suppressunsupportedoswarning)|Unterdrücken der Warnung in Bezug auf nicht unterstützte Betriebssysteme|
|[SyncDisabled](#syncdisabled)|Deaktivieren der Synchronisierung von Daten mit Microsoft Sync Services|
|[SyncTypesListDisabled](#synctypeslistdisabled)|Konfigurieren Sie die Liste der Typen, die von der Synchronisierung ausgeschlossen werden|
|[TLS13HardeningForLocalAnchorsEnabled](#tls13hardeningforlocalanchorsenabled)|Aktivieren eines TLS 1.3-Sicherheitsfeatures für lokale Vertrauensanker (veraltet)|
|[TLSCipherSuiteDenyList](#tlsciphersuitedenylist)|Angeben der zu deaktivierenden TLS-Verschlüsselungssammlungen|
|[TabFreezingEnabled](#tabfreezingenabled)|Einfrieren von Hintergrundregisterkarten zulassen|
|[TaskManagerEndProcessEnabled](#taskmanagerendprocessenabled)|Beenden von Prozessen im Task-Manager des Browsers zulassen|
|[TotalMemoryLimitMb](#totalmemorylimitmb)|Festlegen der Speicherbegrenzung in Megabyte, die eine einzelne Microsoft Edge-Instanz verwenden kann|
|[TrackingPrevention](#trackingprevention)|Blockieren der Nachverfolgung der Browsing-Aktivitäten des Benutzers|
|[TranslateEnabled](#translateenabled)|Übersetzungen aktivieren|
|[URLAllowlist](#urlallowlist)|Definieren einer Liste zulässiger URLs|
|[URLBlocklist](#urlblocklist)|Blockieren des Zugriffs auf eine Liste von URLs|
|[UserAgentClientHintsEnabled](#useragentclienthintsenabled)|Aktivieren des Features User-Agent Client Hints (veraltet)|
|[UserDataDir](#userdatadir)|Festlegen des Benutzerdatenverzeichnisses|
|[UserDataSnapshotRetentionLimit](#userdatasnapshotretentionlimit)|Schränkt die Anzahl der Benutzerdaten-Momentaufnahmen ein, die zur Verwendung für Notfall-Rollbacks aufbewahrt werden.|
|[UserFeedbackAllowed](#userfeedbackallowed)|Benutzerfeedback zulassen|
|[VideoCaptureAllowed](#videocaptureallowed)|Video-Aufnahme zulassen oder blockieren|
|[VideoCaptureAllowedUrls](#videocaptureallowedurls)|Websites, die auf Video-Aufnahmegeräte zugreifen können, ohne eine Berechtigung anfordern zu müssen|
|[WPADQuickCheckEnabled](#wpadquickcheckenabled)|WPAD-Optimierung einrichten|
|[WebAppInstallForceList](#webappinstallforcelist)|Konfigurieren der Liste der erzwungen installierten Web-Apps|
|[WebCaptureEnabled](#webcaptureenabled)|Aktivieren des Features „Websammlung“ in MicrosoftEdge.|
|[WebComponentsV0Enabled](#webcomponentsv0enabled)|Erneut aktivieren der Web Components v0 API bis M84 (veraltet)|
|[WebDriverOverridesIncompatiblePolicies](#webdriveroverridesincompatiblepolicies)|Zulassen, dass WebDriver inkompatible Richtlinien außer Kraft setzt (veraltet)|
|[WebRtcLocalIpsAllowedUrls](#webrtclocalipsallowedurls)|Verwaltung der Gefährdung lokaler IP-Adressen durch WebRTC|
|[WebRtcLocalhostIpHandling](#webrtclocalhostiphandling)|Einschränken der Gefährdung lokaler IP-Adresse durch WebRTC|
|[WebRtcUdpPortRange](#webrtcudpportrange)|Einschränken des von WebRTC verwendeten lokalen Bereichs an UDP-Ports|
|[WebWidgetAllowed](#webwidgetallowed)|Webwidget aktivieren|
|[WebWidgetIsEnabledOnStartup](#webwidgetisenabledonstartup)|Web-Widget beim Windows-Start zulassen|
|[WinHttpProxyResolverEnabled](#winhttpproxyresolverenabled)|Verwenden von Windows-Proxy Konfliktlöser (verworfen)|




  ## Richtlinien für Application Guard-Einstellungen

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### ApplicationGuardContainerProxy

  #### Application Guard-Containerproxy

  
  
  #### Unterstützte Versionen:

  - Unter Windows seit 84 oder später

  #### Beschreibung

  Konfiguriert die Proxyeinstellungen für Microsoft Edge Application Guard.
Wenn Sie diese Richtlinie aktivieren, ignoriert Microsoft Edge Application Guard andere Quellen von Proxykonfigurationen.

Wenn Sie diese Richtlinie nicht konfigurieren, verwendet der Microsoft Edge Application Guard die Proxykonfiguration des Hosts.

Diese Richtlinie hat keinen Einfluss auf die Proxykonfiguration von Microsoft Edge außerhalb von Application Guard (auf dem Host).

Im Feld „ProxyMode“ können Sie den vom Microsoft Edge Application Guard verwendeten Proxyserver angeben.

Das Feld ProxyPacUrl ist eine URL zu einer Proxy-.pac-Datei.

Das ProxyServer-Feld ist eine URL für den Proxy Server.

Wenn Sie den Wert „direct“ als „ProxyMode“ auswählen, werden alle anderen Felder ignoriert.

Wenn Sie den Wert "auto_detect" als "ProxyMode" auswählen, werden alle anderen Felder ignoriert.

Wenn Sie den Wert „fixed_servers“ als „ProxyMode“ auswählen, wird das Feld „ProxyServer“ verwendet.

Wenn Sie den Wert „pac_script“ als „ProxyMode“ auswählen, wird das Feld „ProxyPacUrl“ verwendet.

Weitere Informationen zum Identifizieren des Datenverkehrs in Application Guard über den Dual-Proxy finden Sie unter[https://go.microsoft.com/fwlink/?linkid=2134653](https://go.microsoft.com/fwlink/?linkid=2134653).

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Dictionary

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - Eindeutiger GP-Name: ApplicationGuardContainerProxy
  - GP-Name: Application Guard-Containerproxy
  - GP-Pfad (Pflicht): administrative Vorlagen/Microsoft Edge/Application Guard-Einstellungen
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: ApplicationGuardContainerProxy
  - Werttyp: REG_SZ

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\ApplicationGuardContainerProxy = {
  "ProxyMode": "direct", 
  "ProxyPacUrl": "https://internal.site/example.pac", 
  "ProxyServer": "123.123.123.123:8080"
}
```

  ##### Kompakter Beispielwert:

  ```
  SOFTWARE\Policies\Microsoft\Edge\ApplicationGuardContainerProxy = {"ProxyMode": "direct", "ProxyPacUrl": "https://internal.site/example.pac", "ProxyServer": "123.123.123.123:8080"}
  ```
  

  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ## Cast-Richtlinien

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### EnableMediaRouter

  #### Google Cast aktivieren

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Aktivieren Sie diese Richtlinie, um Google Cast zu aktivieren. Benutzer können es über das App-Menü, Seitenkontextmenüs, Media-Steuerelemente auf Cast-fähigen Websites und (sofern angezeigt) den Eintrag „Cast“ in der Symbolleiste starten.

Deaktivieren Sie diese Richtlinie, um Google Cast zu deaktivieren.

Standardmäßig ist Google Cast aktiviert.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: EnableMediaRouter
  - GP-Name: Google Cast aktivieren
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Cast
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: EnableMediaRouter
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: EnableMediaRouter
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### ShowCastIconInToolbar

  #### Anzeigen des Cast-Symbols in der Symbolleiste

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Legen Sie diese Richtlinie auf "true" fest, um das Cast-Symbol auf der Symbolleiste oder im Überlaufmenü anzuzeigen. Benutzer können sie nicht entfernen.

Falls Sie diese Richtlinie nicht konfigurieren oder falls Sie sie deaktivieren, können Benutzer das Symbol über das Kontextmenü anheften oder entfernen.

Falls Sie die Richtlinie [EnableMediaRouter](#enablemediarouter) auch auf „Falsch“ festgelegt haben, wird diese Richtlinie ignoriert und das Symbol auf der Symbolleiste wird nicht angezeigt.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: ShowCastIconInToolbar
  - GP-Name: Anzeigen des Cast-Symbols in der Symbolleiste
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Cast
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: ShowCastIconInToolbar
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000000
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: ShowCastIconInToolbar
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ## Richtlinien für Inhaltseinstellungen

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### AutoSelectCertificateForUrls

  #### Automatisches Auswählen von Clientzertifikaten für diese Websites

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Wenn Sie die Richtlinie festlegen, können Sie eine Liste von URL-Mustern erstellen, die Websites angeben, für die Microsoft Edge ein Clientzertifikat automatisch auswählen kann. Der Wert ist ein Array aus in Zeichenfolgen konvertierten JSON-Wörterbüchern, die jeweils die folgende Form aufweisen: { "pattern": "$URL_PATTERN", "filter" : $FILTER }, wobei "$URL _PATTERN" ein Inhaltseinstellungsmuster ist. "$FILTER" schränkt die Clientzertifikate ein, aus denen der Browser automatisch auswählen kann. Unabhängig vom Filter werden nur Zertifikate ausgewählt, die die Zertifikatanforderungen des Servers erfüllen.

Beispiele für die Verwendung des Abschnitts "$FILTER":

* Wenn "$FILTER" beispielsweise auf { "ISSUER": { "CN": "$ISSUER_CN" } } festgelegt ist, werden nur Clientzertifikate ausgewählt, die von einem Zertifikat mit dem CommonName "$ISSUER_CN" ausgegeben wurden.

* Wenn "$Filter" sowohl den Abschnitt "ISSUER" als auch den Abschnitt "SUBJECT" enthält, werden nur Clientzertifikate ausgewählt, die beide Bedingungen erfüllen.

* Wenn "$Filter" einen Abschnitt "SUBJECT" mit dem Wert "O" enthält, muss für ein Zertifikat mindestens eine Organisation mit dem angegebenen Wert übereinstimmen, damit es ausgewählt werden kann.

* Wenn "$Filter" einen Abschnitt "SUBJECT" mit einem "OU"-Wert enthält, muss für ein Zertifikat mindestens eine Organisationseinheit mit dem angegebenen Wert übereinstimmen, damit es ausgewählt werden kann.

* Wenn "$Filter" auf {} festgelegt ist, wird die Auswahl der Clientzertifikate nicht weiter eingeschränkt. Beachten Sie, dass vom Webserver eingerichtete Filter weiterhin gelten.

Wenn Sie die Richtlinie nicht einrichten, ist die automatische Auswahl für keine Seite möglich.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Liste von Zeichenfolgen

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: AutoSelectCertificateForUrls
  - GP-Name: Automatisches Auswählen von Clientzertifikaten für diese Websites
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Content settings
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge\AutoSelectCertificateForUrls
  - Pfad (Empfohlen): n.a.
  - Wertname: 1, 2, 3, ...
  - Werttyp: REG_SZ-Liste

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\AutoSelectCertificateForUrls\1 = "{\"pattern\":\"https://www.contoso.com\",\"filter\":{\"ISSUER\":{\"CN\":\"certificate issuer name\", \"L\": \"certificate issuer location\", \"O\": \"certificate issuer org\", \"OU\": \"certificate issuer org unit\"}, \"SUBJECT\":{\"CN\":\"certificate subject name\", \"L\": \"certificate subject location\", \"O\": \"certificate subject org\", \"OU\": \"certificate subject org unit\"}}}"

```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: AutoSelectCertificateForUrls
  - Beispielwert:
``` xml
<array>
  <string>{"pattern":"https://www.contoso.com","filter":{"ISSUER":{"CN":"certificate issuer name", "L": "certificate issuer location", "O": "certificate issuer org", "OU": "certificate issuer org unit"}, "SUBJECT":{"CN":"certificate subject name", "L": "certificate subject location", "O": "certificate subject org", "OU": "certificate subject org unit"}}}</string>
</array>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### CookiesAllowedForUrls

  #### Erlauben von Cookies auf bestimmten Websites

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Sie können eine Liste an Websites, basierend auf URL-Mustern, definieren, die Cookies festlegen dürfen.

Falls Sie diese Richtlinie nicht konfigurieren, wird der globale Standardwert aus der [DefaultCookiesSetting](#defaultcookiessetting)-Richtlinie (sofern festgelegt) oder die persönliche Konfiguration des Benutzers für alle Websites verwendet.

Weitere Informationen hierzu finden Sie unter [CookiesBlockedForUrls](#cookiesblockedforurls) und [CookiesSessionOnlyForUrls](#cookiessessiononlyforurls) Richtlinien.

Beachten Sie, dass für diese drei Richtlinien keine Konflikt verursachenden URL-Muster festgelegt werden dürfen:

- [CookiesBlockedForUrls](#cookiesblockedforurls)

- CookiesAllowedForUrls

- [CookiesSessionOnlyForUrls](#cookiessessiononlyforurls)

Konfigurieren Sie die [SaveCookiesOnExit](#savecookiesonexit)-Richtlinie, um das Löschen von Cookies beim Beenden zu verhindern.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Liste von Zeichenfolgen

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: CookiesAllowedForUrls
  - GP-Name: Erlauben von Cookies auf bestimmten Websites
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Content settings
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge\CookiesAllowedForUrls
  - Pfad (Empfohlen): n.a.
  - Wertname: 1, 2, 3, ...
  - Werttyp: REG_SZ-Liste

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\CookiesAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\CookiesAllowedForUrls\2 = "[*.]contoso.edu"

```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: CookiesAllowedForUrls
  - Beispielwert:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### CookiesBlockedForUrls

  #### Blockieren von Cookies auf bestimmten Websites

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Sie können eine Liste an Websites, basierend auf URL-Mustern, definieren, die keine Cookies setzen dürfen.

Falls Sie diese Richtlinie nicht konfigurieren, wird der globale Standardwert aus der [DefaultCookiesSetting](#defaultcookiessetting)-Richtlinie (sofern festgelegt) oder die persönliche Konfiguration des Benutzers für alle Websites verwendet.

Weitere Informationen hierzu finden Sie unter [CookiesAllowedForUrls](#cookiesallowedforurls) und [CookiesSessionOnlyForUrls](#cookiessessiononlyforurls) Richtlinien.

Beachten Sie, dass für diese drei Richtlinien keine Konflikt verursachenden URL-Muster festgelegt werden dürfen:

- CookiesBlockedForUrls

- [CookiesAllowedForUrls](#cookiesallowedforurls)

- [CookiesSessionOnlyForUrls](#cookiessessiononlyforurls)

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Liste von Zeichenfolgen

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: CookiesBlockedForUrls
  - GP-Name: Blockieren von Cookies auf bestimmten Websites
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Content settings
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge\CookiesBlockedForUrls
  - Pfad (Empfohlen): n.a.
  - Wertname: 1, 2, 3, ...
  - Werttyp: REG_SZ-Liste

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\CookiesBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\CookiesBlockedForUrls\2 = "[*.]contoso.edu"

```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: CookiesBlockedForUrls
  - Beispielwert:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### CookiesSessionOnlyForUrls

  #### Einschränken von Cookies von bestimmten Websites auf die aktuelle Sitzung

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Von Websites, die einem von Ihnen definierten URL-Muster entsprechen, erstellte Cookies werden beim Ende der Sitzung gelöscht (wenn das Fenster geschlossen wird).

Cookies, die von Websites erstellt wurden, die nicht dem Muster entsprechen, werden durch die [DefaultCookiesSetting](#defaultcookiessetting) Richtlinie (sofern festgelegt) oder durch die persönliche Konfiguration des Benutzers gesteuert. Dies ist auch das Standardverhalten, wenn Sie diese Richtlinie nicht konfigurieren.

Wenn Microsoft Edge im Hintergrundmodus ausgeführt wird, wird die Sitzung möglicherweise nicht geschlossen, wenn das letzte Fenster geschlossen wird, was bedeutet, dass die Cookies beim Schließen des Fensters nicht gelöscht werden. Informationen zur Konfiguration dessen, was geschieht, wenn Microsoft Edge im Hintergrundmodus ausgeführt wird, finden Sie in der [BackgroundModeEnabled](#backgroundmodeenabled)-Richtlinie.

Sie können auch die [CookiesAllowedForUrls](#cookiesallowedforurls) und [CookiesBlockedForUrls](#cookiesblockedforurls) Richtlinien verwenden, um zu steuern, welche Websites Cookies erstellen können.

Beachten Sie, dass für diese drei Richtlinien keine Konflikt verursachenden URL-Muster festgelegt werden dürfen:

- [CookiesBlockedForUrls](#cookiesblockedforurls)

- [CookiesAllowedForUrls](#cookiesallowedforurls)

- CookiesSessionOnlyForUrls

Wenn Sie die [RestoreOnStartup](#restoreonstartup) Richtlinie so festlegen, dass URLs aus vorherigen Sitzungen wiederhergestellt werden, wird diese Richtlinie ignoriert, und Cookies werden für diese Websites dauerhaft gespeichert.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Liste von Zeichenfolgen

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: CookiesSessionOnlyForUrls
  - GP-Name: Einschränken von Cookies von bestimmten Websites auf die aktuelle Sitzung
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Content settings
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge\CookiesSessionOnlyForUrls
  - Pfad (Empfohlen): n.a.
  - Wertname: 1, 2, 3, ...
  - Werttyp: REG_SZ-Liste

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\CookiesSessionOnlyForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\CookiesSessionOnlyForUrls\2 = "[*.]contoso.edu"

```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: CookiesSessionOnlyForUrls
  - Beispielwert:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### DefaultCookiesSetting

  #### Configure cookies

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Steuern, ob Websites auf dem Gerät des Benutzers Cookies erstellen können. Diese Richtlinie arbeitet mit absoluten Werten – Sie können zulassen, dass alle Websites Cookies erstellen können, oder dass keine Websites Cookies erstellen können. Sie können diese Richtlinie nicht verwenden, um Cookies nur von bestimmten Websites zuzulassen.

Setzen Sie die Richtlinie auf „SessionOnly“, um Cookies beim Beenden der Sitzung zu löschen. Wenn Microsoft Edge im Hintergrundmodus ausgeführt wird, wird die Sitzung möglicherweise nicht geschlossen, wenn das letzte Fenster geschlossen wird, was bedeutet, dass die Cookies beim Schließen des Fensters nicht gelöscht werden. Informationen zur Konfiguration dessen, was geschieht, wenn Microsoft Edge im Hintergrundmodus ausgeführt wird, finden Sie in der [BackgroundModeEnabled](#backgroundmodeenabled)-Richtlinie.

Wenn Sie diese Richtlinie nicht konfigurieren, wird die Standardeinstellung „AllowCookies“ verwendet. Die Benutzer können diese Einstellung in den Microsoft Edge-Einstellungen ändern. (Wenn Sie nicht möchten, dass die Benutzer diese Einstellung ändern können, legen Sie die Richtlinie fest.)

Zuordnung von Richtlinienoptionen:

* AllowCookies (1) = alle Websites können Cookies erstellen

* BlockCookies (2) = keine Website kann Cookies erstellen

* SessionOnly (4) = Cookies für die Dauer der Sitzung beibehalten, mit Ausnahme derjenigen, die in [SaveCookiesOnExit](#savecookiesonexit) aufgeführt sind

Verwenden Sie die vorstehenden Informationen, wenn Sie diese Richtlinie konfigurieren.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Ganze Zahl

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: DefaultCookiesSetting
  - GP-Name: Konfigurieren von Cookies
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Content settings
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: DefaultCookiesSetting
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: DefaultCookiesSetting
  - Beispielwert:
``` xml
<integer>1</integer>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### DefaultFileSystemReadGuardSetting

  #### Steuern der Verwendung der Datei-System-API für den Lesezugriff

  
  
  #### Unterstützte Versionen:

  - Unter Windows und macOS ab 86 oder höher

  #### Beschreibung

  Wenn Sie diese Richtlinie auf "3" festlegen, können Websites Lesezugriff auf das Dateisystem des Hostbetriebssystems mithilfe der Datei-System-API anfordern. Wenn Sie diese Richtlinie auf "2" festlegen, wird der Zugriff verweigert.

Wenn Sie diese Richtlinie nicht festlegen, können Websites Zugriff anfordern. Diese Einstellung kann von Benutzern geändert werden.

Zuordnung von Richtlinienoptionen:

* BlockFileSystemRead (2) = nicht zulassen, dass eine Website Lesezugriff auf Dateien und Verzeichnisse über die Datei System-API anfordert

* AskFileSystemRead (3) = nicht zulassen, dass eine Website vom Benutzer Lesezugriff auf Dateien und Verzeichnisse über die Datei-System-API anfordert

Verwenden Sie die vorstehenden Informationen, wenn Sie diese Richtlinie konfigurieren.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Ganze Zahl

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - Eindeutiger GP-Name: DefaultFileSystemReadGuardSetting
  - GP-Name: Steuern der Verwendung der Datei-System-API für den Lesezugriff
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Content settings
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: DefaultFileSystemReadGuardSetting
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000002
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: DefaultFileSystemReadGuardSetting
  - Beispielwert:
``` xml
<integer>2</integer>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### DefaultFileSystemWriteGuardSetting

  #### Steuern der Verwendung der Datei-System-API für den Schreibzugriff

  
  
  #### Unterstützte Versionen:

  - Unter Windows und macOS ab 86 oder höher

  #### Beschreibung

  Wenn Sie diese Richtlinie auf "3" festlegen, können Websites Schreibzugriff auf das Dateisystem des Hostbetriebssystems mithilfe der Datei-System-API anfordern. Wenn Sie diese Richtlinie auf "2" festlegen, wird der Zugriff verweigert.

Wenn Sie diese Richtlinie nicht festlegen, können Websites Zugriff anfordern. Diese Einstellung kann von Benutzern geändert werden.

Zuordnung von Richtlinienoptionen:

* BlockFileSystemWrite (2) = nicht zulassen, dass Websites Schreibzugriff auf Dateien und Verzeichnisse anfordern

* AskFileSystemWrite (3) = zulassen, dass Websites vom Benutzer Schreibzugriff auf Dateien und Verzeichnisse anfordern

Verwenden Sie die vorstehenden Informationen, wenn Sie diese Richtlinie konfigurieren.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Ganze Zahl

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - Eindeutiger GP-Name: DefaultFileSystemWriteGuardSetting
  - GP-Name: Steuern der Verwendung der Datei-System-API für den Schreibzugriff
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Content settings
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: DefaultFileSystemWriteGuardSetting
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000002
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: DefaultFileSystemWriteGuardSetting
  - Beispielwert:
``` xml
<integer>2</integer>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### DefaultGeolocationSetting

  #### Standardeinstellung für Geolocation

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Legen Sie fest, ob Websites den Aufenthaltsort der Benutzer nachverfolgen können. Sie können die Standortbestimmung standardmäßig zulassen („AllowGeolocation“), sie standardmäßig verweigern („BlockGeolocation“) oder den Benutzer jedes Mal Fragen, wenn eine Website seinen Standort anfordert („AskGeolocation“).

Falls Sie diese Richtlinie nicht konfigurieren, wird „AskGeolocation“ verwendet, und der Benutzer kann dies ändern.

Zuordnung von Richtlinienoptionen:

* AllowGeolocation (1) = zulassen, dass Websites den Standort der Benutzer nachverfolgen

* BlockGeolocation (2) = nicht zulassen, dass Websites den Standort der Benutzer nachverfolgen

* AskGeolocation (3) = immer fragen, wenn eine Website den Standort der Benutzer nachverfolgen möchte

Verwenden Sie die vorstehenden Informationen, wenn Sie diese Richtlinie konfigurieren.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Ganze Zahl

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: DefaultGeolocationSetting
  - GP-Name: Standardeinstellung für Geolocation
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Content settings
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: DefaultGeolocationSetting
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: DefaultGeolocationSetting
  - Beispielwert:
``` xml
<integer>1</integer>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### DefaultImagesSetting

  #### Standardeinstellung für Bilder

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Legen Sie fest, ob Websites Bilder anzeigen können. Sie können Bilder auf allen Websites zulassen („AllowImages“) oder auf allen Websites blockieren („BlockImages“).

Wenn Sie diese Richtlinie nicht konfigurieren, sind Bilder standardmäßig zulässig und der Benutzer kann diese Einstellung ändern.

Zuordnung von Richtlinienoptionen:

* AllowImages (1) = zulassen, dass alle Websites alle Bilder anzeigen

* BlockImages (2) = nicht zulassen, dass Websites Bilder anzeigen

Verwenden Sie die vorstehenden Informationen, wenn Sie diese Richtlinie konfigurieren.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Ganze Zahl

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: DefaultImagesSetting
  - GP-Name: Standardeinstellung für Bilder
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Content settings
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: DefaultImagesSetting
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: DefaultImagesSetting
  - Beispielwert:
``` xml
<integer>1</integer>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### DefaultInsecureContentSetting

  #### Verwendung von unsicheren Inhaltsausnahmen steuern

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 80 oder höher

  #### Beschreibung

  Sie können festlegen, ob Benutzer Ausnahmen hinzufügen können, um gemischten Inhalt für bestimmte Websites zuzulassen.

Diese Richtlinie kann für bestimmte URL-Muster überschrieben werden, indem die Richtlinien [InsecureContentAllowedForUrls](#insecurecontentallowedforurls) und [InsecureContentBlockedForUrls](#insecurecontentblockedforurls) verwendet werden.

Wenn diese Richtlinie nicht festgelegt ist, können Benutzer Ausnahmen hinzufügen, um blockierbare Mischinhalte zuzulassen und automatische Upgrades für optional blockierbare Mischinhalte zu deaktivieren.

Zuordnung von Richtlinienoptionen:

* BlockInsecureContent (2) = nicht zulassen, dass eine Website gemischten Inhalt lädt

* AllowExceptionsInsecureContent (3) = Benutzern erlauben, Ausnahmen hinzuzufügen, um Mischinhalte zuzulassen

Verwenden Sie die vorstehenden Informationen, wenn Sie diese Richtlinie konfigurieren.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Ganze Zahl

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: DefaultInsecureContentSetting
  - GP-Name: Verwendung von unsicheren Inhaltsausnahmen steuern
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Content settings
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: DefaultInsecureContentSetting
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000002
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: DefaultInsecureContentSetting
  - Beispielwert:
``` xml
<integer>2</integer>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### DefaultJavaScriptSetting

  #### Standardeinstellung für JavaScript

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Legen Sie fest, ob Websites JavaScript ausführen können. Sie können es für alle Websites erlauben („AllowJavaScript“) oder für alle Websites blockieren („BlockJavaScript“).

Wenn Sie diese Richtlinie nicht konfigurieren, können alle Websites JavaScript standardmäßig ausführen und der Benutzer kann diese Einstellung ändern.

Zuordnung von Richtlinienoptionen:

* AllowJavaScript (1) = zulassen, dass alle Websites JavaScript ausführen

* BlockJavaScript (2) = nicht zulassen, dass Websites JavaScript ausführen

Verwenden Sie die vorstehenden Informationen, wenn Sie diese Richtlinie konfigurieren.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Ganze Zahl

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: DefaultJavaScriptSetting
  - GP-Name: Standardeinstellung für JavaScript
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Content settings
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: DefaultJavaScriptSetting
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: DefaultJavaScriptSetting
  - Beispielwert:
``` xml
<integer>1</integer>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### DefaultNotificationsSetting

  #### Standardeinstellung für Benachrichtigungen

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Legen Sie fest, ob Websites Desktopbenachrichtigungen anzeigen können. Sie können diese standardmäßig zulassen („AllowNotifications“), sie standardmäßig ablehnen („BlockNotifications“) oder den Benutzer jedes Mal Fragen, wenn eine Website eine Benachrichtigung anzeigen möchte („AskNotifications“).

Wenn Sie diese Richtlinie nicht konfigurieren, sind Benachrichtigungen standardmäßig zulässig und der Benutzer kann diese Einstellung ändern.

Zuordnung von Richtlinienoptionen:

* AllowNotifications (1) = zulassen, dass Websites Desktopbenachrichtigungen anzeigen

* BlockNotifications (2) = nicht zulassen, dass Websites Desktopbenachrichtigungen anzeigen

* AskNotifications (3) = jedes Mal fragen, wenn eine Website Desktopbenachrichtigungen anzeigen möchte

Verwenden Sie die vorstehenden Informationen, wenn Sie diese Richtlinie konfigurieren.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Ganze Zahl

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: DefaultNotificationsSetting
  - GP-Name: Standardeinstellung für Benachrichtigungen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Content settings
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: DefaultNotificationsSetting
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000002
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: DefaultNotificationsSetting
  - Beispielwert:
``` xml
<integer>2</integer>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### DefaultPluginsSetting

  #### Standardeinstellung für Adobe Flash

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  [PluginsAllowedForUrls](#pluginsallowedforurls) und [PluginsBlockedForUrls](#pluginsblockedforurls) werden zuerst überprüft, dann diese Richtlinie. Die Optionen lauten "ClickToPlay" und "BlockPlugins". Wenn Sie diese Richtlinie auf "BlockPlugins" festlegen, wird dieses Plugin für alle Websites abgelehnt. Mit "ClickToPlay" kann das Flash-Plugin ausgeführt werden, die Benutzer klicken aber auf den Platzhalter, um es zu starten.

Wenn Sie diese Richtlinie nicht konfigurieren, können Benutzer diese Einstellung manuell ändern.

Hinweis: Die automatische Wiedergabe gilt nur für Domänen, die in der Richtlinie [PluginsAllowedForUrls](#pluginsallowedforurls) explizit aufgelistet sind. Wenn Sie die automatische Wiedergabe für alle Websites aktivieren möchten, fügen Sie "http://*" und "https://*" zur Liste der zulässigen URLs hinzu.

Zuordnung von Richtlinienoptionen:

* BlockPlugins (2) = Blockieren des Adobe Flash-Plug-Ins

* ClickToPlay (3) = zum Abspielen klicken

Verwenden Sie die vorstehenden Informationen, wenn Sie diese Richtlinie konfigurieren.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Ganze Zahl

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: DefaultPluginsSetting
  - GP-Name: Standardeinstellung für Adobe Flash
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Content settings
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: DefaultPluginsSetting
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000002
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: DefaultPluginsSetting
  - Beispielwert:
``` xml
<integer>2</integer>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### DefaultPopupsSetting

  #### Standardeinstellung für Popupfenster

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Legen Sie fest, ob Websites Popupfenster anzeigen können. Sie können sie auf allen Websites zulassen („AllowPopups“) oder sie auf allen Websites blockieren („BlockPopups“).

Falls Sie diese Richtlinie nicht konfigurieren, werden Popupfenster standardmäßig blockiert und der Benutzer kann diese Einstellung ändern.

Zuordnung von Richtlinienoptionen:

* AllowPopups (1) = zulassen, dass alle Websites Popupfenster anzeigen

* BlockPopups (2) = nicht zulassen, dass Websites Popups anzeigen

Verwenden Sie die vorstehenden Informationen, wenn Sie diese Richtlinie konfigurieren.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Ganze Zahl

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: DefaultPopupsSetting
  - GP-Name: Standardeinstellung für Popupfenster
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Content settings
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: DefaultPopupsSetting
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: DefaultPopupsSetting
  - Beispielwert:
``` xml
<integer>1</integer>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### DefaultWebBluetoothGuardSetting

  #### Steuern der Verwendung der Web-Bluetooth-API

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Steuern, ob Websites auf in der Nähe befindliche Bluetooth-Geräte zugreifen können. Sie können den Zugriff vollständig blockieren oder es für die Website erforderlich machen, den Benutzer jedes Mal zu fragen, wenn sie auf ein Bluetooth-Gerät zugreifen möchte.

Wenn Sie diese Richtlinie nicht konfigurieren, wird der Standardwert („AskWebBluetooth“, d. h. die Benutzer werden jedes Mal gefragt) verwendet, und die Benutzer können ihn ändern.

Zuordnung von Richtlinienoptionen:

* BlockWebBluetooth (2) = nicht zulassen, dass eine Website Zugriff auf Bluetooth-Geräte über die Web-Bluetooth-API anfordert

* AskWebBluetooth (3) = zulassen, dass Websites den Benutzer um Zugriff auf ein in der Nähe befindliches Bluetooth-Gerät bitten

Verwenden Sie die vorstehenden Informationen, wenn Sie diese Richtlinie konfigurieren.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Ganze Zahl

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: DefaultWebBluetoothGuardSetting
  - GP-Name: Steuern der Verwendung der Web-Bluetooth-API
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Content settings
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: DefaultWebBluetoothGuardSetting
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000002
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: DefaultWebBluetoothGuardSetting
  - Beispielwert:
``` xml
<integer>2</integer>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### DefaultWebUsbGuardSetting

  #### Steuern der Verwendung der WebUSB-API

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Legen Sie fest, ob Websites auf angeschlossene USB-Geräte zugreifen können. Sie können den Zugriff vollständig blockieren oder den Benutzer jedes Mal fragen, wenn eine Website auf angeschlossene USB-Geräte zugreifen möchte.

Sie können diese Richtlinie für bestimmte URL-Muster außer Kraft setzen, indem Sie die [WebUsbAskForUrls](#webusbaskforurls) und [WebUsbBlockedForUrls](#webusbblockedforurls) Richtlinien verwenden.

Wenn Sie diese Richtlinie nicht konfigurieren, können Websites Benutzer standardmäßig fragen, ob sie auf verbundene USB-Geräte zugreifen können („AskWebUsb“) und die Benutzer können diese Einstellung ändern.

Zuordnung von Richtlinienoptionen:

* BlockWebUsb (2) = nicht zulassen, dass Websites Zugriff auf USB-Geräte über die WebUSB-API anfordern

* AskWebUsb (3) = zulassen, dass Websites den Benutzer um Zugriff auf ein verbundenes USB-Gerät bitten

Verwenden Sie die vorstehenden Informationen, wenn Sie diese Richtlinie konfigurieren.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Ganze Zahl

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: DefaultWebUsbGuardSetting
  - GP-Name: Steuern der Verwendung der WebUSB-API
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Content settings
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: DefaultWebUsbGuardSetting
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000002
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: DefaultWebUsbGuardSetting
  - Beispielwert:
``` xml
<integer>2</integer>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### FileSystemReadAskForUrls

  #### Lesezugriff über die Datei-System-API auf diesen Websites zulassen

  
  
  #### Unterstützte Versionen:

  - Unter Windows und macOS ab 86 oder höher

  #### Beschreibung

  Beim Festlegen der Richtlinie können Sie die URL-Muster auflisten, mit denen angegeben wird, welche Websites vom Benutzer Lesezugriff auf Dateien oder Verzeichnisse im Dateisystem des Hostbetriebssystems über die Dateisystem-API anfordern dürfen.

Wenn Sie die Richtlinie nicht festlegen, bedeutet dies, dass [DefaultFileSystemReadGuardSetting](#defaultfilesystemreadguardsetting) für alle Websites gilt, sofern diese festgelegt ist. Ist dies nicht der Fall, werden die persönlichen Einstellungen der Benutzer übernommen.

URL-Muster dürfen nicht mit [FileSystemReadBlockedForUrls](#filesystemreadblockedforurls) in Konflikt stehen. Keine der Richtlinien hat Vorrang, wenn eine URL mit beiden übereinstimmt.

Ausführliche Informationen zu gültigen URL-Mustern finden Sie unter https://cloud.google.com/docs/chrome-enterprise/policies/url-patterns.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Liste von Zeichenfolgen

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - Eindeutiger GP-Name: FileSystemReadAskForUrls
  - GP-Name: Lesezugriff über die Datei-System-API auf diesen Websites zulassen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Content settings
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge\FileSystemReadAskForUrls
  - Pfad (Empfohlen): n.a.
  - Wertname: 1, 2, 3, ...
  - Werttyp: REG_SZ-Liste

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\FileSystemReadAskForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\FileSystemReadAskForUrls\2 = "[*.]example.edu"

```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: FileSystemReadAskForUrls
  - Beispielwert:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### FileSystemReadBlockedForUrls

  #### Lesezugriff über die Datei-System-API auf diesen Websites blockieren

  
  
  #### Unterstützte Versionen:

  - Unter Windows und macOS ab 86 oder höher

  #### Beschreibung

  Beim Festlegen der Richtlinie können Sie die URL-Muster auflisten, mit denen angegeben wird, welche Websites vom Benutzer keinen Lesezugriff auf Dateien oder Verzeichnisse im Dateisystem des Hostbetriebssystems über die Dateisystem-API anfordern dürfen.

Wenn Sie die Richtlinie nicht festlegen, gilt [DefaultFileSystemReadGuardSetting](#defaultfilesystemreadguardsetting) für alle Websites, sofern diese festgelegt ist. Ist dies nicht der Fall, werden die persönlichen Einstellungen der Benutzer übernommen.

URL-Muster dürfen nicht mit [FileSystemReadAskForUrls](#filesystemreadaskforurls) in Konflikt stehen. Keine der Richtlinien hat Vorrang, wenn eine URL mit beiden übereinstimmt.

Ausführliche Informationen zu gültigen URL-Mustern finden Sie unter https://cloud.google.com/docs/chrome-enterprise/policies/url-patterns.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Liste von Zeichenfolgen

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - Eindeutiger GP-Name: FileSystemReadBlockedForUrls
  - GP-Name: Lesezugriff über die Datei-System-API auf diesen Websites blockieren
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Content settings
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge\FileSystemReadBlockedForUrls
  - Pfad (Empfohlen): n.a.
  - Wertname: 1, 2, 3, ...
  - Werttyp: REG_SZ-Liste

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\FileSystemReadBlockedForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\FileSystemReadBlockedForUrls\2 = "[*.]example.edu"

```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: FileSystemReadBlockedForUrls
  - Beispielwert:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### FileSystemWriteAskForUrls

  #### Schreibzugriff auf Dateien und Verzeichnisse auf diesen Websites zulassen

  
  
  #### Unterstützte Versionen:

  - Unter Windows und macOS ab 86 oder höher

  #### Beschreibung

  Beim Festlegen der Richtlinie können Sie die URL-Muster auflisten, mit denen angegeben wird, welche Websites vom Benutzer Schreibzugriff auf Dateien oder Verzeichnisse im Dateisystem des Hostbetriebssystems anfordern dürfen.

Wenn Sie die Richtlinie nicht festlegen, gilt [DefaultFileSystemWriteGuardSetting](#defaultfilesystemwriteguardsetting) für alle Websites, sofern diese festgelegt ist. Ist dies nicht der Fall, werden die persönlichen Einstellungen der Benutzer übernommen.

URL-Muster dürfen nicht mit [FileSystemWriteBlockedForUrls](#filesystemwriteblockedforurls) in Konflikt stehen. Keine der Richtlinien hat Vorrang, wenn eine URL mit beiden übereinstimmt.

Ausführliche Informationen zu gültigen URL-Mustern finden Sie unter https://cloud.google.com/docs/chrome-enterprise/policies/url-patterns.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Liste von Zeichenfolgen

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - Eindeutiger GP-Name: FileSystemWriteAskForUrls
  - GP-Name: Schreibzugriff auf Dateien und Verzeichnisse auf diesen Websites zulassen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Content settings
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteAskForUrls
  - Pfad (Empfohlen): n.a.
  - Wertname: 1, 2, 3, ...
  - Werttyp: REG_SZ-Liste

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteAskForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteAskForUrls\2 = "[*.]example.edu"

```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: FileSystemWriteAskForUrls
  - Beispielwert:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### FileSystemWriteBlockedForUrls

  #### Schreibzugriff auf Dateien und Verzeichnisse auf diesen Websites blockieren

  
  
  #### Unterstützte Versionen:

  - Unter Windows und macOS ab 86 oder höher

  #### Beschreibung

  Beim Festlegen der Richtlinie können Sie die URL-Muster auflisten, mit denen angegeben wird, welche Websites vom Benutzer keinen Schreibzugriff auf Dateien oder Verzeichnisse im Dateisystem des Hostbetriebssystems anfordern dürfen.

Wenn Sie die Richtlinie nicht festlegen, gilt [DefaultFileSystemWriteGuardSetting](#defaultfilesystemwriteguardsetting) für alle Websites, sofern diese festgelegt ist. Ist dies nicht der Fall, werden die persönlichen Einstellungen der Benutzer übernommen.

URL-Muster dürfen nicht mit [FileSystemWriteAskForUrls](#filesystemwriteaskforurls) in Konflikt stehen. Keine der Richtlinien hat Vorrang, wenn eine URL mit beiden übereinstimmt.

Ausführliche Informationen zu gültigen URL-Mustern finden Sie unter https://cloud.google.com/docs/chrome-enterprise/policies/url-patterns.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Liste von Zeichenfolgen

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - Eindeutiger GP-Name: FileSystemWriteBlockedForUrls
  - GP-Name: Schreibzugriff auf Dateien und Verzeichnisse auf diesen Websites blockieren
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Content settings
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteBlockedForUrls
  - Pfad (Empfohlen): n.a.
  - Wertname: 1, 2, 3, ...
  - Werttyp: REG_SZ-Liste

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteBlockedForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteBlockedForUrls\2 = "[*.]example.edu"

```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: FileSystemWriteBlockedForUrls
  - Beispielwert:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### ImagesAllowedForUrls

  #### Zulassen von Bildern auf diesen Websites

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Sie können eine Liste an Websites, basierend auf URL-Mustern, definieren, die Bilder anzeigen dürfen.

Falls Sie diese Richtlinie nicht konfigurieren, wird für alle Websites der globale Standardwert aus der [DefaultImagesSetting](#defaultimagessetting)-Richtlinie (sofern festgelegt) oder die persönliche Konfiguration des Benutzers verwendet.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Liste von Zeichenfolgen

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: ImagesAllowedForUrls
  - GP-Name: Zulassen von Bildern auf diesen Websites
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Content settings
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge\ImagesAllowedForUrls
  - Pfad (Empfohlen): n.a.
  - Wertname: 1, 2, 3, ...
  - Werttyp: REG_SZ-Liste

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\ImagesAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\ImagesAllowedForUrls\2 = "[*.]contoso.edu"

```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: ImagesAllowedForUrls
  - Beispielwert:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### ImagesBlockedForUrls

  #### Blockieren von Bildern auf bestimmten Websites

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Sie können eine Liste an Websites, basierend auf URL-Mustern, definieren, die keine Bilder anzeigen dürfen.

Falls Sie diese Richtlinie nicht konfigurieren, wird der globale Standardwert aus der [DefaultImagesSetting](#defaultimagessetting)-Richtlinie (sofern festgelegt) oder die persönliche Konfiguration des Benutzers für alle Websites verwendet.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Liste von Zeichenfolgen

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: ImagesBlockedForUrls
  - GP-Name: Blockieren von Bildern auf bestimmten Websites
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Content settings
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge\ImagesBlockedForUrls
  - Pfad (Empfohlen): n.a.
  - Wertname: 1, 2, 3, ...
  - Werttyp: REG_SZ-Liste

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\ImagesBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\ImagesBlockedForUrls\2 = "[*.]contoso.edu"

```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: ImagesBlockedForUrls
  - Beispielwert:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### InsecureContentAllowedForUrls

  #### Zulassen von unsicheren Inhalten auf bestimmten Websites

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 80 oder höher

  #### Beschreibung

  Erstellen Sie eine Liste von URL-Mustern, um Websites festzulegen, die unsicheren gemischten Inhalt anzeigen können (also HTTP-Inhalte auf HTTPS-Websites).

Wenn Sie diese Richtlinie nicht konfigurieren, werden blockierbare Mischinhalte blockiert und optional können blockierbare Mischinhalte auch aktualisiert werden. Benutzer können jedoch Ausnahmen festlegen, um unsichere Mischinhalte auf bestimmten Websites zuzulassen.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Liste von Zeichenfolgen

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: InsecureContentAllowedForUrls
  - GP-Name: Zulassen von unsicheren Inhalten auf bestimmten Websites
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Content settings
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge\InsecureContentAllowedForUrls
  - Pfad (Empfohlen): n.a.
  - Wertname: 1, 2, 3, ...
  - Werttyp: REG_SZ-Liste

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\InsecureContentAllowedForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\InsecureContentAllowedForUrls\2 = "[*.]example.edu"

```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: InsecureContentAllowedForUrls
  - Beispielwert:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### InsecureContentBlockedForUrls

  #### Blockieren von unsicheren Inhalten auf bestimmten Websites

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 80 oder höher

  #### Beschreibung

  Erstellen Sie eine Liste von URL-Mustern, um Websites festzulegen, die keine blockierbaren (d h. aktiven) gemischten Inhalte (also HTTP-Inhalte auf HTTPS-Websites) anzeigen dürfen und für die optional blockierbare Mischinhalte aktualisiert werden.

Wenn Sie diese Richtlinie nicht konfigurieren, werden blockierbare Mischinhalte blockiert und optional können blockierbare Mischinhalte auch aktualisiert werden. Benutzer können jedoch Ausnahmen festlegen, um unsichere Mischinhalte auf bestimmten Websites zuzulassen.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Liste von Zeichenfolgen

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: InsecureContentBlockedForUrls
  - GP-Name: Blockieren von unsicheren Inhalten auf bestimmten Websites
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Content settings
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge\InsecureContentBlockedForUrls
  - Pfad (Empfohlen): n.a.
  - Wertname: 1, 2, 3, ...
  - Werttyp: REG_SZ-Liste

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\InsecureContentBlockedForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\InsecureContentBlockedForUrls\2 = "[*.]example.edu"

```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: InsecureContentBlockedForUrls
  - Beispielwert:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### JavaScriptAllowedForUrls

  #### JavaScript auf bestimmten Websites zulassen

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Sie können eine Liste an Websites, basierend auf URL-Mustern, definieren, die JavaScript ausführen dürfen.

Falls Sie diese Richtlinie nicht konfigurieren, wird der globale Standardwert aus der [DefaultJavaScriptSetting](#defaultjavascriptsetting)-Richtlinie (sofern festgelegt) oder die persönliche Konfiguration des Benutzers für alle Websites verwendet.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Liste von Zeichenfolgen

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: JavaScriptAllowedForUrls
  - GP-Name: JavaScript auf bestimmten Websites zulassen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Content settings
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge\JavaScriptAllowedForUrls
  - Pfad (Empfohlen): n.a.
  - Wertname: 1, 2, 3, ...
  - Werttyp: REG_SZ-Liste

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\JavaScriptAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\JavaScriptAllowedForUrls\2 = "[*.]contoso.edu"

```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: JavaScriptAllowedForUrls
  - Beispielwert:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### JavaScriptBlockedForUrls

  #### JavaScript auf bestimmten Websites blockieren

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Sie können eine Liste an Websites, basierend auf URL-Mustern, definieren, die JavaScript nicht ausführen dürfen.

Falls Sie diese Richtlinie nicht konfigurieren, wird der globale Standardwert aus der [DefaultJavaScriptSetting](#defaultjavascriptsetting)-Richtlinie (sofern festgelegt) oder die persönliche Konfiguration des Benutzers für alle Websites verwendet.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Liste von Zeichenfolgen

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: JavaScriptBlockedForUrls
  - GP-Name: JavaScript auf bestimmten Websites blockieren
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Content settings
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge\JavaScriptBlockedForUrls
  - Pfad (Empfohlen): n.a.
  - Wertname: 1, 2, 3, ...
  - Werttyp: REG_SZ-Liste

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\JavaScriptBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\JavaScriptBlockedForUrls\2 = "[*.]contoso.edu"

```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: JavaScriptBlockedForUrls
  - Beispielwert:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### LegacySameSiteCookieBehaviorEnabled

  #### Standardeinstellung für das Verhalten von Legacy-SameSite-Cookies aktivieren

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 80 oder höher

  #### Beschreibung

  Hiermit können Sie alle Cookies auf das alte SameSite-Verhalten zurücksetzen. Durch das Zurückkehren zum alten Verhalten werden Cookies, die kein SameSite-Attribut angeben, so behandelt, als wären sie "SameSite = None", und die Anforderung an "SameSite = None"-Cookies, das "Secure"-Attribut zu übermitteln, wird entfernt. Darüber hinaus wird der Schemavergleich beim Überprüfen, ob zwei Websites der gleichen Seite angehören, übersprungen.

Wenn Sie diese Richtlinie nicht festlegen, ist das standardmäßige SameSite-Verhalten für Cookies von anderen Konfigurationsquellen für das "SameSite-by-default"-Feature, das "Cookies-without-SameSite-must-be-secure"-Feature und das "Schemeful Same-Site"-Feature abhängig. Diese Funktionen können auch durch eine Feldprüfung oder durch das "same-site-by-default-cookies"-Flag, das "cookies-without-same-site-must-be-secure"-Flag oder das "schemeful-same-site"-Flag unter edge://flags konfiguriert werden.

Zuordnung von Richtlinienoptionen:

* DefaultToLegacySameSiteCookieBehavior (1) = wiederherstellen des Legacy-SameSite-Verhaltens für Cookies auf bestimmten Websites

* DefaultToSameSiteByDefaultCookieBehavior (2) = verwenden von standardmäßigem SameSite-Verhalten für Cookies auf allen Websites

Verwenden Sie die vorstehenden Informationen, wenn Sie diese Richtlinie konfigurieren.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Ganze Zahl

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: LegacySameSiteCookieBehaviorEnabled
  - GP-Name: Standardeinstellung für das Verhalten von Legacy-SameSite-Cookies aktivieren
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Content settings
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: LegacySameSiteCookieBehaviorEnabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: LegacySameSiteCookieBehaviorEnabled
  - Beispielwert:
``` xml
<integer>1</integer>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### LegacySameSiteCookieBehaviorEnabledForDomainList

  #### Zurückkehren zum alten SameSite-Verhalten für Cookies auf bestimmten Websites

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 80 oder höher

  #### Beschreibung

  Cookies, die für Domänen mit den angegebenen Mustern gesetzt wurden, werden auf das alte SameSite-Verhalten zurückfallen.

Durch das Zurückkehren zum alten Verhalten werden Cookies, die kein SameSite-Attribut angeben, so behandelt, als wären sie "SameSite = None", und die Anforderung an "SameSite = None"-Cookies, das "Secure"-Attribut zu übermitteln, wird entfernt. Darüber hinaus wird der Schemavergleich beim Überprüfen, ob zwei Websites der gleichen Seite angehören, übersprungen.

Wenn Sie diese Richtlinie nicht festlegen, wird der globale Standardwert verwendet. Der globale Standardwert wird auch für Cookies in Domänen verwendet, die nicht unter die von Ihnen angegebenen Muster fallen.

Der globale Standardwert kann mit der Richtlinie [LegacySameSiteCookieBehaviorEnabled](#legacysamesitecookiebehaviorenabled) konfiguriert werden. Wenn [LegacySameSiteCookieBehaviorEnabled](#legacysamesitecookiebehaviorenabled) nicht eingestellt wird, greift der globale Standardwert auf andere Konfigurationsquellen zurück.

Beachten Sie, dass die von Ihnen in dieser Richtlinie aufgelisteten Muster als Domänen und nicht als URLs behandelt werden, daher sollten Sie kein(en) Schema oder Port angeben.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Liste von Zeichenfolgen

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: LegacySameSiteCookieBehaviorEnabledForDomainList
  - GP-Name: Zurückkehren zum alten SameSite-Verhalten für Cookies auf bestimmten Websites
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Content settings
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge\LegacySameSiteCookieBehaviorEnabledForDomainList
  - Pfad (Empfohlen): n.a.
  - Wertname: 1, 2, 3, ...
  - Werttyp: REG_SZ-Liste

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\LegacySameSiteCookieBehaviorEnabledForDomainList\1 = "www.example.com"
SOFTWARE\Policies\Microsoft\Edge\LegacySameSiteCookieBehaviorEnabledForDomainList\2 = "[*.]example.edu"

```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: LegacySameSiteCookieBehaviorEnabledForDomainList
  - Beispielwert:
``` xml
<array>
  <string>www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### NotificationsAllowedForUrls

  #### Zulassen von Benachrichtigungen bei bestimmten Websites

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Ermöglicht Ihnen, eine Liste von URL-Mustern zu erstellen, um Websites anzugeben, die Benachrichtigungen anzeigen dürfen.

Wenn Sie diese Richtlinie nicht festlegen, wird für alle Websites der globale Standardwert verwendet. Dieser Standardwert stammt aus der Richtlinie [DefaultNotificationsSetting](#defaultnotificationssetting), sofern diese festgelegt ist, oder aus der persönlichen Konfiguration des Benutzers. Ausführliche Informationen zu gültigen URL-Mustern finden Sie unter [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Liste von Zeichenfolgen

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: NotificationsAllowedForUrls
  - GP-Name: Zulassen von Benachrichtigungen bei bestimmten Websites
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Content settings
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge\NotificationsAllowedForUrls
  - Pfad (Empfohlen): n.a.
  - Wertname: 1, 2, 3, ...
  - Werttyp: REG_SZ-Liste

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\NotificationsAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\NotificationsAllowedForUrls\2 = "[*.]contoso.edu"

```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: NotificationsAllowedForUrls
  - Beispielwert:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### NotificationsBlockedForUrls

  #### Blockieren von Benachrichtigungen für bestimmte Websites

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Ermöglicht Ihnen, eine Liste von URL-Mustern zu erstellen, um Sites anzugeben, die keine Benachrichtigungen anzeigen dürfen.

Wenn Sie diese Richtlinie nicht festlegen, wird für alle Websites der globale Standardwert verwendet. Dieser Standardwert stammt aus der Richtlinie [DefaultNotificationsSetting](#defaultnotificationssetting), sofern diese festgelegt ist, oder aus der persönlichen Konfiguration des Benutzers. Ausführliche Informationen zu gültigen URL-Mustern finden Sie unter [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Liste von Zeichenfolgen

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: NotificationsBlockedForUrls
  - GP-Name: Blockieren von Benachrichtigungen für bestimmte Websites
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Content settings
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge\NotificationsBlockedForUrls
  - Pfad (Empfohlen): n.a.
  - Wertname: 1, 2, 3, ...
  - Werttyp: REG_SZ-Liste

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\NotificationsBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\NotificationsBlockedForUrls\2 = "[*.]contoso.edu"

```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: NotificationsBlockedForUrls
  - Beispielwert:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### PluginsAllowedForUrls

  #### Zulassen des Adobe Flash-Plug-Ins auf bestimmten Websites

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Sie können eine Liste an Websites, basierend auf URL-Mustern, definieren, die das Adobe Flash-Plug-In ausführen dürfen.

Falls Sie diese Richtlinie nicht konfigurieren, wird der globale Standardwert aus der [DefaultPluginsSetting](#defaultpluginssetting)-Richtlinie (sofern festgelegt) oder die persönliche Konfiguration des Benutzers für alle Websites verwendet.

Ausführliche Informationen zu gültigen URL-Mustern finden Sie unter [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322). Ab M85 werden jedoch Muster mit „*“-und „[*.]“-Platzhaltern für diese Richtlinie nicht mehr unterstützt.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Liste von Zeichenfolgen

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: PluginsAllowedForUrls
  - GP-Name: Zulassen des Adobe Flash-Plug-Ins auf bestimmten Websites
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Content settings
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge\PluginsAllowedForUrls
  - Pfad (Empfohlen): n.a.
  - Wertname: 1, 2, 3, ...
  - Werttyp: REG_SZ-Liste

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\PluginsAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\PluginsAllowedForUrls\2 = "http://contoso.edu:8080"

```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: PluginsAllowedForUrls
  - Beispielwert:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>http://contoso.edu:8080</string>
</array>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### PluginsBlockedForUrls

  #### Blockieren des Adobe Flash-Plug-Ins auf bestimmten Websites

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Sie können eine Liste an Websites, basierend auf URL-Mustern, definieren, die das Adobe Flash-Plug-In nicht ausführen dürfen.

Falls Sie diese Richtlinie nicht konfigurieren, wird der globale Standardwert aus der [DefaultPluginsSetting](#defaultpluginssetting)-Richtlinie (sofern festgelegt) oder die persönliche Konfiguration des Benutzers für alle Websites verwendet.

Ausführliche Informationen zu gültigen URL-Mustern finden Sie unter [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322). Ab M85 werden jedoch Muster mit „*“-und „[*.]“-Platzhaltern für diese Richtlinie nicht mehr unterstützt.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Liste von Zeichenfolgen

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: PluginsBlockedForUrls
  - GP-Name: Blockieren des Adobe Flash-Plug-Ins auf bestimmten Websites
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Content settings
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge\PluginsBlockedForUrls
  - Pfad (Empfohlen): n.a.
  - Wertname: 1, 2, 3, ...
  - Werttyp: REG_SZ-Liste

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\PluginsBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\PluginsBlockedForUrls\2 = "http://contoso.edu:8080"

```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: PluginsBlockedForUrls
  - Beispielwert:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>http://contoso.edu:8080</string>
</array>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### PopupsAllowedForUrls

  #### Popupfenster auf bestimmten Websites zulassen

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Sie können eine Liste an Websites, basierend auf URL-Mustern, definieren, die Popup-Fenster öffnen dürfen.

Falls Sie diese Richtlinie nicht konfigurieren, wird der globale Standardwert aus der [DefaultPopupsSetting](#defaultpopupssetting)-Richtlinie (sofern festgelegt) oder die persönliche Konfiguration des Benutzers für alle Websites verwendet.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Liste von Zeichenfolgen

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: PopupsAllowedForUrls
  - GP-Name: Popupfenster auf bestimmten Websites zulassen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Content settings
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge\PopupsAllowedForUrls
  - Pfad (Empfohlen): n.a.
  - Wertname: 1, 2, 3, ...
  - Werttyp: REG_SZ-Liste

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\PopupsAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\PopupsAllowedForUrls\2 = "[*.]contoso.edu"

```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: PopupsAllowedForUrls
  - Beispielwert:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### PopupsBlockedForUrls

  #### Popupfenster auf bestimmten Websites blockieren

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Sie können eine Liste an Websites, basierend auf URL-Mustern, definieren, die keine Popup-Fenster öffnen dürfen.

Falls Sie diese Richtlinie nicht konfigurieren, wird der globale Standardwert aus der [DefaultPopupsSetting](#defaultpopupssetting)-Richtlinie (sofern festgelegt) oder die persönliche Konfiguration des Benutzers für alle Websites verwendet.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Liste von Zeichenfolgen

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: PopupsBlockedForUrls
  - GP-Name: Popupfenster auf bestimmten Websites blockieren
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Content settings
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge\PopupsBlockedForUrls
  - Pfad (Empfohlen): n.a.
  - Wertname: 1, 2, 3, ...
  - Werttyp: REG_SZ-Liste

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\PopupsBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\PopupsBlockedForUrls\2 = "[*.]contoso.edu"

```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: PopupsBlockedForUrls
  - Beispielwert:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### RegisteredProtocolHandlers

  #### Registrieren von Protokollhandlern

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Legen Sie diese Richtlinie (nur empfohlen) fest, um eine Liste von Protokollhandlern zu registrieren. Diese Liste wird mit denen vom Benutzer registrierten zusammengeführt, und beide stehen zur Nutzung zur Verfügung.

So registrieren Sie einen Protokollhandler:

- Legen Sie die Protocol-Eigenschaft auf das Schema fest (z.B. „mailto“)
- Setzen Sie die URL-Eigenschaft auf die URL-Eigenschaft der Anwendung, die das im Feld „Protokoll“ angegebene Schema verarbeitet. Das Muster kann einen „%s“ enthalten, der durch die verarbeitete URL ersetzt wird.

Benutzer können einen durch diese Richtlinie registrierten Protokollhandler nicht entfernen. Sie können jedoch einen neuen Standard-Protokollhandler installieren, um die vorhandenen Protokollhandler zu überschreiben.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Nein
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Dictionary

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: RegisteredProtocolHandlers
  - GP-Name: Registrieren von Protokollhandlern
  - GP-Pfad (verpflichtend): N/A
  - GP Pfad (Empfohlen): Administrative Templates/Microsoft Edge – Standardeinstellungen (Benutzer können diese außer Kraft setzen)/Inhaltseinstellungen
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): N/A
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Wertname: RegisteredProtocolHandlers
  - Werttyp: REG_SZ

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\RegisteredProtocolHandlers = [
  {
    "default": true, 
    "protocol": "mailto", 
    "url": "https://mail.contoso.com/mail/?extsrc=mailto&url=%s"
  }
]
```

  ##### Kompakter Beispielwert:

  ```
  SOFTWARE\Policies\Microsoft\Edge\RegisteredProtocolHandlers = [{"default": true, "protocol": "mailto", "url": "https://mail.contoso.com/mail/?extsrc=mailto&url=%s"}]
  ```
  

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: RegisteredProtocolHandlers
  - Beispielwert:
``` xml
<key>RegisteredProtocolHandlers</key>
<array>
  <dict>
    <key>default</key>
    <true/>
    <key>protocol</key>
    <string>mailto</string>
    <key>url</key>
    <string>https://mail.contoso.com/mail/?extsrc=mailto&url=%s</string>
  </dict>
</array>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### SpotlightExperiencesAndRecommendationsEnabled

  #### Wählen Sie aus, ob Benutzer personalisierte Hintergrundbilder und Text, Vorschläge, Benachrichtigungen
und Tipps für Microsoft-Dienste erhalten können.

  
  
  #### Unterstützte Versionen:

  - Unter Windows 86 oder später

  #### Beschreibung

  Wählen Sie aus, ob Benutzer personalisierte Hintergrundbilder und Text, Vorschläge, Benachrichtigungen und Tipps für Microsoft-Dienste erhalten können.

Wenn Sie diese Einstellung aktivieren oder nicht konfigurieren, sind Blickpunkt-Erlebnisse und -Empfehlungen aktiviert.

Wenn Sie diese Einstellung deaktivieren, sind Blickpunkt-Erlebnisse und -Empfehlungen deaktiviert.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - Eindeutiger GP-Name: SpotlightExperiencesAndRecommendationsEnabled
  - GP-Name: Wählen Sie aus, ob Benutzer personalisierte Hintergrundbilder und Text, Vorschläge, Benachrichtigungen und Tipps für Microsoft-Dienste erhalten können.
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Content settings
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: SpotlightExperiencesAndRecommendationsEnabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### WebUsbAllowDevicesForUrls

  #### Bestimmten Websites die Herstellung einer Verbindung zu bestimmten USB-Geräten gewähren.

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Ermöglicht es Ihnen, eine Liste von URLs festzulegen, die festlegt, welche Websites automatisch die Berechtigung für den Zugriff auf ein USB-Gerät mit den angegebenen Lieferanten- und Produkt-IDs erhalten. Jedes Element in der Liste muss sowohl Geräte als auch URLs enthalten, damit die Richtlinie gültig ist. Jedes Element in „Geräte“ kann ein Feld "Lieferanten-ID" und "Produkt-ID" enthalten. Jede weggelassene ID wird als Platzhalter mit einer Ausnahme behandelt, und diese Ausnahme besteht darin, dass keine Produkt-ID angegeben werden kann, ohne dass auch eine Lieferanten-ID angegeben wird. Andernfalls ist die Richtlinie ungültig und wird ignoriert.

Beim USB-Berechtigungsmodell wird die URL der anfordernden Website ("anfordernde URL") und die URL der Frame-Website der obersten Ebene ("Einbettende URL") verwendet, um der anfordernden URL die Berechtigung für den Zugriff auf das USB-Gerät zu erteilen. Die anfordernde URL unterscheidet sich möglicherweise von der Einbettenden URL, wenn die anfordernde Website in einen iframe geladen wird. Daher kann das Feld "URLs" bis zu zwei URL-Zeichenfolgen enthalten, die durch ein Komma getrennt sind, um die anfordernde von der einbettenden URL zu unterscheiden. Wenn nur eine URL angegeben ist, wird der Zugriff auf die entsprechenden USB-Geräte gewährt, wenn die URL der anfordernden Website dieser URL unabhängig vom Einbettungsstatus entspricht. Die URLs in "URLs" müssen gültige URLs sein, andernfalls wird die Richtlinie ignoriert.

Falls diese Richtlinie nicht festgelegt wurde, wird für alle Websites der globale Standardwert aus der [DefaultWebUsbGuardSetting](#defaultwebusbguardsetting)-Richtlinie (sofern festgelegt) oder andernfalls die persönliche Konfiguration des Benutzers verwendet.

URL-Muster in dieser Richtlinie sollten keine Konflikte mit denen verursachen, die in [WebUsbBlockedForUrls](#webusbblockedforurls) konfiguriert sind. Wenn ein Konflikt vorliegt, hat diese Richtlinie Vorrang vor [WebUsbBlockedForUrls](#webusbblockedforurls) und [WebUsbAskForUrls](#webusbaskforurls).

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Dictionary

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: WebUsbAllowDevicesForUrls
  - GP-Name: Bestimmten Websites die Herstellung einer Verbindung zu bestimmten USB-Geräten gewähren
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Content settings
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: WebUsbAllowDevicesForUrls
  - Werttyp: REG_SZ

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\WebUsbAllowDevicesForUrls = [
  {
    "devices": [
      {
        "product_id": 5678, 
        "vendor_id": 1234
      }
    ], 
    "urls": [
      "https://contoso.com", 
      "https://fabrikam.com"
    ]
  }
]
```

  ##### Kompakter Beispielwert:

  ```
  SOFTWARE\Policies\Microsoft\Edge\WebUsbAllowDevicesForUrls = [{"devices": [{"product_id": 5678, "vendor_id": 1234}], "urls": ["https://contoso.com", "https://fabrikam.com"]}]
  ```
  

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: WebUsbAllowDevicesForUrls
  - Beispielwert:
``` xml
<key>WebUsbAllowDevicesForUrls</key>
<array>
  <dict>
    <key>devices</key>
    <array>
      <dict>
        <key>product_id</key>
        <integer>5678</integer>
        <key>vendor_id</key>
        <integer>1234</integer>
      </dict>
    </array>
    <key>urls</key>
    <array>
      <string>https://contoso.com</string>
      <string>https://fabrikam.com</string>
    </array>
  </dict>
</array>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### WebUsbAskForUrls

  #### Erlauben von WebUSB auf bestimmten Websites

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Definieren Sie eine Liste der-Websites, die auf URL-Mustern basiert, die den Benutzer um Zugriff auf ein USB-Gerät bitten können.

Falls Sie diese Richtlinie nicht konfigurieren, wird der globale Standardwert aus der [DefaultWebUsbGuardSetting](#defaultwebusbguardsetting)-Richtlinie (sofern festgelegt) oder die persönliche Konfiguration des Benutzers für alle Websites verwendet.

Die in dieser Richtlinie definierten URL-Muster dürfen nicht mit den in der [WebUsbBlockedForUrls](#webusbblockedforurls) Richtlinie konfigurierten Konflikten in Konflikt stehen. Sie können eine URL nicht sowohl zulassen als auch blockieren. Ausführliche Informationen zu gültigen URL-Mustern finden Sie unter [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Liste von Zeichenfolgen

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: WebUsbAskForUrls
  - GP-Name: Erlauben von WebUSB auf bestimmten Websites
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Content settings
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge\WebUsbAskForUrls
  - Pfad (Empfohlen): n.a.
  - Wertname: 1, 2, 3, ...
  - Werttyp: REG_SZ-Liste

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\WebUsbAskForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\WebUsbAskForUrls\2 = "[*.]contoso.edu"

```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: WebUsbAskForUrls
  - Beispielwert:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### WebUsbBlockedForUrls

  #### Blockieren von WebUSB auf bestimmten Websites

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Definieren Sie eine Liste der-Websites, die auf URL-Mustern basiert, die den Benutzer nicht um Zugriff auf ein USB-Gerät bitten können.

Falls Sie diese Richtlinie nicht konfigurieren, wird der globale Standardwert aus der [DefaultWebUsbGuardSetting](#defaultwebusbguardsetting)-Richtlinie (sofern festgelegt) oder die persönliche Konfiguration des Benutzers für alle Websites verwendet.

URL-Muster in dieser Richtlinie dürfen nicht mit denen in Konflikt stehen, die in der [WebUsbAskForUrls](#webusbaskforurls) Richtlinie konfiguriert sind. Sie können eine URL nicht sowohl zulassen als auch blockieren.  Ausführliche Informationen zu gültigen URL-Mustern finden Sie unter [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Liste von Zeichenfolgen

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: WebUsbBlockedForUrls
  - GP-Name: Blockieren von WebUSB auf bestimmten Websites
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Content settings
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge\WebUsbBlockedForUrls
  - Pfad (Empfohlen): n.a.
  - Wertname: 1, 2, 3, ...
  - Werttyp: REG_SZ-Liste

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\WebUsbBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\WebUsbBlockedForUrls\2 = "[*.]contoso.edu"

```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: WebUsbBlockedForUrls
  - Beispielwert:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ## Richtlinien des standardmäßigen Suchdienstanbieters

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### DefaultSearchProviderEnabled

  #### Standardmäßigen Suchdienstanbieter aktivieren

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Ermöglicht die Verwendung eines Standardsuchanbieters.

Wenn Sie diese Richtlinie aktivieren, kann ein Benutzer nach einem Begriff suchen, indem er ihn in die Adressleiste tippt (sofern es sich nicht um eine URL handelt).

Sie können den zu verwendenden Standard-Suchanbieter angeben, indem Sie die restlichen Standard-Suchrichtlinien aktivieren. Wenn diese leer (nicht konfiguriert) bleiben oder nicht ordnungsgemäß konfiguriert sind, kann der Benutzer den Standardanbieter auswählen.

Wenn Sie diese Richtlinie deaktivieren, kann der Benutzer nicht über die Adressleiste suchen.

Wenn Sie diese Richtlinie aktivieren oder deaktivieren, können die Benutzer sie nicht ändern oder außer Kraft setzen.

Wenn Sie diese Richtlinie nicht konfigurieren, ist der standardmäßige Suchanbieter aktiviert, und der Benutzer kann den standardmäßigen Suchanbieter auswählen und die Suchanbieterliste festlegen.

Diese Richtlinie ist nur für Windows-Instanzen verfügbar, die mit einer Microsoft Active Directory-Domäne verknüpft sind, Windows 10 Pro- oder Enterprise-Instanzen, die für die Geräteverwaltung registriert sind, oder MacOS-Instanzen, die über MDM verwaltet oder über MCX einer Domäne beigetreten sind.

Beginnend mit Microsoft Edge 84 können Sie diese Richtlinie als empfohlene Richtlinie festlegen.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: DefaultSearchProviderEnabled
  - GP-Name: Standardmäßigen Suchdienstanbieter aktivieren
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Default search provider
  - GP Pfad (Empfohlen): Administrative Vorlagen/Microsoft Edge – Standardeinstellungen (Benutzer können diese außer Kraft setzen)/Standardsuchanbieter
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Wertname: DefaultSearchProviderEnabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: DefaultSearchProviderEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### DefaultSearchProviderEncodings

  #### Verschlüsselung standardmäßiger Suchdienstanbieter

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Geben Sie die vom Suchanbieter unterstützten Zeichencodierungen an. Codierungen sind Codepagenamen wie UTF-8, GB2312 und ISO-8859-1. Sie werden in der bereitgestellten Reihenfolge ausprobiert.

Diese Richtlinie ist optional. Wenn dies nicht konfiguriert ist, wird standardmäßig UTF-8 verwendet.

Diese Richtlinie wird nur angewendet, wenn Sie die Richtlinien [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) und [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl) aktivieren.

Beginnend mit Microsoft Edge 84 können Sie diese Richtlinie als empfohlene Richtlinie festlegen. Wenn der Benutzer bereits einen standardmäßigen Suchanbieter festgelegt hat, wird der von dieser empfohlenen Richtlinie konfigurierte Standardsuchanbieter nicht zur Liste der Suchanbieter hinzugefügt, aus denen der Benutzer auswählen kann. Wenn dies das gewünschte Verhalten ist, verwenden Sie die[ManagedSearchEngines](#managedsearchengines) Richtlinie.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Liste von Zeichenfolgen

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: DefaultSearchProviderEncodings
  - GP-Name: Verschlüsselung standardmäßiger Suchdienstanbieter
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Default search provider
  - GP Pfad (Empfohlen): Administrative Vorlagen/Microsoft Edge – Standardeinstellungen (Benutzer können diese außer Kraft setzen)/Standardsuchanbieter
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Recommended\RestoreOnStartupURLs
  - Wertname: 1, 2, 3, ...
  - Werttyp: REG_SZ-Liste

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings\1 = "UTF-8"
SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings\2 = "UTF-16"
SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings\3 = "GB2312"
SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings\4 = "ISO-8859-1"

```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: DefaultSearchProviderEncodings
  - Beispielwert:
``` xml
<array>
  <string>UTF-8</string>
  <string>UTF-16</string>
  <string>GB2312</string>
  <string>ISO-8859-1</string>
</array>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### DefaultSearchProviderImageURL

  #### Spezifiziert das Feature „Suche nach Bild“ für den standardmäßigen Suchanbieter

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Gibt die URL für die Suchmaschine an, die für die die Bildsuche verwendet wird. Suchanforderungen werden mithilfe der GET-Methode gesendet.

Diese Richtlinie ist optional. Wenn Sie sie nicht konfigurieren, ist die Bildsuche nicht verfügbar.

Legen Sie Bings Bildsuch-URL folgendermaßen fest: '{bing:baseURL}images/detail/search?iss=sbiupload&FORM=ANCMS1#enterInsights'.

Legen Sie Googles Bildsuch-URL folgendermaßen fest: '{google:baseURL}searchbyimage/upload'.

Sehen Sie in der [DefaultSearchProviderImageURLPostParams](#defaultsearchproviderimageurlpostparams) Richtlinie nach, um die Konfiguration der Bildsuche abzuschließen.

Diese Richtlinie wird nur angewendet, wenn Sie die Richtlinien [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) und [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl) aktivieren.

Beginnend mit Microsoft Edge 84 können Sie diese Richtlinie als empfohlene Richtlinie festlegen. Wenn der Benutzer bereits einen standardmäßigen Suchanbieter festgelegt hat, wird der von dieser empfohlenen Richtlinie konfigurierte Standardsuchanbieter nicht zur Liste der Suchanbieter hinzugefügt, aus denen der Benutzer auswählen kann. Wenn dies das gewünschte Verhalten ist, verwenden Sie die[ManagedSearchEngines](#managedsearchengines) Richtlinie.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Zeichenfolge

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: DefaultSearchProviderImageURL
  - GP-Name: Spezifiziert das Feature „Suche nach Bild“ für den standardmäßigen Suchanbieter
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Default search provider
  - GP Pfad (Empfohlen): Administrative Vorlagen/Microsoft Edge – Standardeinstellungen (Benutzer können diese außer Kraft setzen)/Standardsuchanbieter
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Wertname: DefaultSearchProviderImageURL
  - Werttyp: REG_SZ

  ##### Beispielwert:

```
"https://search.contoso.com/searchbyimage/upload"
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: DefaultSearchProviderImageURL
  - Beispielwert:
``` xml
<string>https://search.contoso.com/searchbyimage/upload</string>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### DefaultSearchProviderImageURLPostParams

  #### Parameter für eine Bild-URL, die POST verwendet

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Wenn Sie diese Richtlinie aktivieren, werden die Parameter angegeben, die verwendet werden, wenn eine Bildsuche, die POST verwendet, ausgeführt wird. Die Richtlinie besteht aus durch Trennzeichen getrennten Namen/Wert-Paaren. Wenn ein Wert ein Vorlagenparameter ist, z.B. {Bildminiaturansicht} im vorangehenden Beispiel, wird er durch eine reale Miniaturbilddatei ersetzt. Diese Richtlinie wird nur angewendet, wenn Sie die Richtlinien [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) und [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl) aktivieren.

Legen Sie die POST-Parameter für Bings Bildsuch-URL folgendermaßen fest: 'imageBin={google:imageThumbnailBase64}'.

Legen Sie die POST-Parameter für Googles Bildsuch-URL folgendermaßen fest: 'encoded_image={google:imageThumbnail},image_url={google:imageURL},sbisrc={google:imageSearchSource},original_width={google:imageOriginalWidth},original_height={google:imageOriginalHeight}'.

Wenn Sie diese Richtlinie nicht festlegen, werden die Anforderungen für die Bildsuche mithilfe der GET-Methode gesendet.

Beginnend mit Microsoft Edge 84 können Sie diese Richtlinie als empfohlene Richtlinie festlegen. Wenn der Benutzer bereits einen standardmäßigen Suchanbieter festgelegt hat, wird der von dieser empfohlenen Richtlinie konfigurierte Standardsuchanbieter nicht zur Liste der Suchanbieter hinzugefügt, aus denen der Benutzer auswählen kann. Wenn dies das gewünschte Verhalten ist, verwenden Sie die[ManagedSearchEngines](#managedsearchengines) Richtlinie.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Zeichenfolge

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: DefaultSearchProviderImageURLPostParams
  - GP-Name: Parameter für eine Bild-URL, die POST verwendet
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Default search provider
  - GP Pfad (Empfohlen): Administrative Vorlagen/Microsoft Edge – Standardeinstellungen (Benutzer können diese außer Kraft setzen)/Standardsuchanbieter
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Wertname: DefaultSearchProviderImageURLPostParams
  - Werttyp: REG_SZ

  ##### Beispielwert:

```
"content={imageThumbnail},url={imageURL},sbisrc={SearchSource}"
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: DefaultSearchProviderImageURLPostParams
  - Beispielwert:
``` xml
<string>content={imageThumbnail},url={imageURL},sbisrc={SearchSource}</string>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### DefaultSearchProviderKeyword

  #### Schlüsselwort standardmäßiger Suchdienstanbieter

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Gibt das Schlüsselwort an, das in der Adressleiste als Abkürzung verwendet wird, um die Suche mit diesem Anbieter auszulösen.

Diese Richtlinie ist optional. Wenn Sie sie nicht konfigurieren, wird der Suchanbieter durch kein Schlüsselwort aktiviert.

Diese Richtlinie wird nur angewendet, wenn Sie die Richtlinien [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) und [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl) aktivieren.

Beginnend mit Microsoft Edge 84 können Sie diese Richtlinie als empfohlene Richtlinie festlegen. Wenn der Benutzer bereits einen standardmäßigen Suchanbieter festgelegt hat, wird der von dieser empfohlenen Richtlinie konfigurierte Standardsuchanbieter nicht zur Liste der Suchanbieter hinzugefügt, aus denen der Benutzer auswählen kann. Wenn dies das gewünschte Verhalten ist, verwenden Sie die[ManagedSearchEngines](#managedsearchengines) Richtlinie.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Zeichenfolge

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: DefaultSearchProviderKeyword
  - GP-Name: Schlüsselwort standardmäßiger Suchdienstanbieter
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Default search provider
  - GP Pfad (Empfohlen): Administrative Vorlagen/Microsoft Edge – Standardeinstellungen (Benutzer können diese außer Kraft setzen)/Standardsuchanbieter
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Wertname: DefaultSearchProviderKeyword
  - Werttyp: REG_SZ

  ##### Beispielwert:

```
"mis"
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: DefaultSearchProviderKeyword
  - Beispielwert:
``` xml
<string>mis</string>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### DefaultSearchProviderName

  #### Name des standardmäßigen Suchdienstanbieters

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Gibt den Namen des Standardsuchanbieters an.

Wenn Sie diese Richtlinie aktivieren, legen Sie den Namen des standardmäßigen Such-Dienstanbieters fest.

Wenn Sie diese Richtlinie nicht aktivieren oder Sie leer lassen, wird der in der Such-URL angegebene Hostname verwendet.

"DefaultSearchProviderName" sollte auf einen vom Unternehmen genehmigten, verschlüsselten Suchanbieter festgelegt sein, der dem verschlüsselten Suchanbieter in DTBC-0008 entspricht. Diese Richtlinie wird nur angewendet, wenn Sie die Richtlinien [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) und [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl) aktivieren.

Beginnend mit Microsoft Edge 84 können Sie diese Richtlinie als empfohlene Richtlinie festlegen. Wenn der Benutzer bereits einen standardmäßigen Suchanbieter festgelegt hat, wird der von dieser empfohlenen Richtlinie konfigurierte Standardsuchanbieter nicht zur Liste der Suchanbieter hinzugefügt, aus denen der Benutzer auswählen kann. Wenn dies das gewünschte Verhalten ist, verwenden Sie die[ManagedSearchEngines](#managedsearchengines) Richtlinie.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Zeichenfolge

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: DefaultSearchProviderName
  - GP-Name: Name des standardmäßigen Suchdienstanbieters
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Default search provider
  - GP Pfad (Empfohlen): Administrative Vorlagen/Microsoft Edge – Standardeinstellungen (Benutzer können diese außer Kraft setzen)/Standardsuchanbieter
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Wertname: DefaultSearchProviderName
  - Werttyp: REG_SZ

  ##### Beispielwert:

```
"My Intranet Search"
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: DefaultSearchProviderName
  - Beispielwert:
``` xml
<string>My Intranet Search</string>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### DefaultSearchProviderSearchURL

  #### Such-URL des standardmäßigen Suchdienstanbieters

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Gibt die URL für die Suchmaschine an, die für die Standardsuche verwendet wird. Die URL enthält die Zeichenfolge "{searchTerms}", die zum Zeitpunkt der Abfrage durch die vom Benutzer gesuchten Ausdrücke ersetzt wird.

Legen Sie die Bing-Such-URL wie folgt fest:

'{bing:baseURL}search?q={searchTerms}'.

Legen Sie die Google-Such-URL wie folgt fest:: '{google:baseURL}search?q={searchTerms}&{google:RLZ}{google:originalQueryForSuggestion}{google:assistedQueryStats}{google:searchFieldtrialParameter}{google:searchClient}{google:sourceId}ie={inputEncoding}'.

Diese Richtlinie ist erforderlich, wenn Sie die Richtlinie [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) aktivieren. Wenn Sie diese letztgenannte Richtlinie nicht aktivieren, wird diese Richtlinie ignoriert.

Beginnend mit Microsoft Edge 84 können Sie diese Richtlinie als empfohlene Richtlinie festlegen. Wenn der Benutzer bereits einen standardmäßigen Suchanbieter festgelegt hat, wird der von dieser empfohlenen Richtlinie konfigurierte Standardsuchanbieter nicht zur Liste der Suchanbieter hinzugefügt, aus denen der Benutzer auswählen kann. Wenn dies das gewünschte Verhalten ist, verwenden Sie die[ManagedSearchEngines](#managedsearchengines) Richtlinie.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Zeichenfolge

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: DefaultSearchProviderSearchURL
  - GP-Name: Such-URL des standardmäßigen Suchdienstanbieters
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Default search provider
  - GP Pfad (Empfohlen): Administrative Vorlagen/Microsoft Edge – Standardeinstellungen (Benutzer können diese außer Kraft setzen)/Standardsuchanbieter
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Wertname: DefaultSearchProviderSearchURL
  - Werttyp: REG_SZ

  ##### Beispielwert:

```
"https://search.contoso.com/search?q={searchTerms}"
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: DefaultSearchProviderSearchURL
  - Beispielwert:
``` xml
<string>https://search.contoso.com/search?q={searchTerms}</string>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### DefaultSearchProviderSuggestURL

  #### URL des standardmäßigen Suchdienstanbieters für Vorschläge

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Gibt die URL für die Suchmaschine an, durch die Suchvorschläge bereitgestellt werden. Die URL enthält die Zeichenfolge "{searchTerms}", die zum Zeitpunkt der Abfrage durch den vom Benutzer bisher eingegebenen Text ersetzt wird.

Diese Richtlinie ist optional. Wenn Sie sie nicht konfigurieren, werden Benutzern keine Suchvorschläge angezeigt. Sie sehen Vorschläge aus dem Browserverlauf und den Favoriten.

Bings Vorschlags-URL kann folgendermaßen angegeben werden:

'{bing:baseURL}qbox?query={searchTerms}'.

Googles Vorschlags-URL kann folgendermaßen angegeben werden: '{google:baseURL}complete/search?output=chrome&q={searchTerms}'.

Diese Richtlinie wird nur angewendet, wenn Sie die Richtlinien [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) und [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl) aktivieren.

Beginnend mit Microsoft Edge 84 können Sie diese Richtlinie als empfohlene Richtlinie festlegen. Wenn der Benutzer bereits einen standardmäßigen Suchanbieter festgelegt hat, wird der von dieser empfohlenen Richtlinie konfigurierte Standardsuchanbieter nicht zur Liste der Suchanbieter hinzugefügt, aus denen der Benutzer auswählen kann. Wenn dies das gewünschte Verhalten ist, verwenden Sie die[ManagedSearchEngines](#managedsearchengines) Richtlinie.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Zeichenfolge

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: DefaultSearchProviderSuggestURL
  - GP-Name: URL des standardmäßigen Suchdienstanbieters für Vorschläge
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Default search provider
  - GP Pfad (Empfohlen): Administrative Vorlagen/Microsoft Edge – Standardeinstellungen (Benutzer können diese außer Kraft setzen)/Standardsuchanbieter
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Wertname: DefaultSearchProviderSuggestURL
  - Werttyp: REG_SZ

  ##### Beispielwert:

```
"https://search.contoso.com/suggest?q={searchTerms}"
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: DefaultSearchProviderSuggestURL
  - Beispielwert:
``` xml
<string>https://search.contoso.com/suggest?q={searchTerms}</string>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### NewTabPageSearchBox

  #### Konfigurieren das neuen Suchfeld für die Registerkartenoberfläche 

  
  
  #### Unterstützte Versionen:

  - Auf Windows und MacOS ab 85 oder später

  #### Beschreibung

  Sie können das neue Suchfeld für die Registerkartenseite so konfigurieren, dass "Suchfeld (empfohlen)" oder "Adressleiste" zum Suchen auf neuen Registerkarten verwendet wird. Diese Richtlinie funktioniert nur, wenn Sie die Suchfunktion auf einen anderen Wert als Bing festlegen, indem Sie die beiden folgenden Richtlinien festlegen: [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) und [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl).

 Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren und:

- Wenn die Standardsuchmaschine der Adressleiste Bing ist, verwendet die Registerkarte "neu" das Suchfeld, um auf neuen Registerkarten zu suchen.
- Wenn die Standardsuchmaschine der Adressleiste nicht Bing ist, wird den Benutzern bei der Suche auf neuen Registerkarten eine weitere Option ("Adressleiste") angezeigt.


Wenn Sie diese Richtlinie aktivieren und folgende Einstellungen festlegen:

- "Suchfeld (empfohlen)" ("Bing"), die Registerkarte "neu" verwendet das Suchfeld, um auf neuen Registerkarten zu suchen.
- "Adressleiste" ("Umleitung"), das neue Suchfeld der Registerkarte verwendet die Adressleiste, um auf neuen Registerkarten zu suchen.

Zuordnung von Richtlinienoptionen:

* Bing (Bing) = Suchfeld (empfohlen)

* Redirect (Umleitung) = Adressleiste

Verwenden Sie die vorstehenden Informationen, wenn Sie diese Richtlinie konfigurieren.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Zeichenfolge

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - Eindeutiger Name des GP: NewTabPageSearchBox
  - GP-Name: Konfigurieren des neuen Suchfelds für die Registerkartenoberfläche
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Default search provider
  - GP Pfad (Empfohlen): Administrative Vorlagen/Microsoft Edge – Standardeinstellungen (Benutzer können diese außer Kraft setzen)/Standardsuchanbieter
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Value Name: NewTabPageSearchBox
  - Werttyp: REG_SZ

  ##### Beispielwert:

```
"bing"
```

  #### Mac – Informationen und Einstellungen
  
  - Name des Einstellungsschlüssels: NewTabPageSearchBox
  - Beispielwert:
``` xml
<string>bing</string>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ## Erweiterungsrichtlinien

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### ExtensionAllowedTypes

  #### Konfigurieren von zulässigen Erweiterungstypen

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Durch Festlegen der Richtlinie wird gesteuert, welche Apps und Erweiterungen in Microsoft Edge installiert werden können, mit welchen Hosts Sie interagieren können und es wird der Zugriff auf die Laufzeit eingeschränkt.

Wenn Sie diese Richtlinie nicht festlegen, gibt es keine Einschränkungen für zulässige Erweiterungen und App-Typen.

Erweiterungen und Apps, die einen Typ aufweisen, der nicht in der Liste enthalten ist, werden nicht installiert. Jeder Wert sollte eine der folgenden Zeichenfolgen sein:

* „extension“

* „theme“

* „user_script“

* „hosted_app“

Weitere Informationen zu diesen Typen finden Sie in der Dokumentation zu Microsoft Edge-Erweiterungen.

Hinweis: Diese Richtlinie wirkt sich auch auf Erweiterungen und Apps aus, deren Installation mithilfe von [ExtensionInstallForcelist](#extensioninstallforcelist) erzwungen werden soll.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Liste von Zeichenfolgen

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: ExtensionAllowedTypes
  - GP-Name: Konfigurieren von zulässigen Erweiterungstypen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Extensions
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge\ExtensionAllowedTypes
  - Pfad (Empfohlen): n.a.
  - Wertname: 1, 2, 3, ...
  - Werttyp: REG_SZ-Liste

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\ExtensionAllowedTypes\1 = "hosted_app"

```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: ExtensionAllowedTypes
  - Beispielwert:
``` xml
<array>
  <string>hosted_app</string>
</array>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### ExtensionInstallAllowlist

  #### Zulassen, dass bestimmte Erweiterungen installiert werden

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Standardmäßig sind alle Erweiterungen zulässig. Wenn Sie jedoch alle Erweiterungen blockieren, indem Sie die Richtlinie "ExtensionInstallBlockList" auf "*" festlegen, können Benutzer nur die in dieser Richtlinie definierten Erweiterungen installieren.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Liste von Zeichenfolgen

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: ExtensionInstallAllowlist
  - GP-Name: Zulassen, dass bestimmte Erweiterungen installiert werden
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Extensions
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallAllowlist
  - Pfad (Empfohlen): n.a.
  - Wertname: 1, 2, 3, ...
  - Werttyp: REG_SZ-Liste

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallAllowlist\1 = "extension_id1"
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallAllowlist\2 = "extension_id2"

```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: ExtensionInstallAllowlist
  - Beispielwert:
``` xml
<array>
  <string>extension_id1</string>
  <string>extension_id2</string>
</array>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### ExtensionInstallBlocklist

  #### Steuern, welche Erweiterungen nicht installiert werden können

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Listet bestimmte Erweiterungen auf, die Benutzer in Microsoft Edge NICHT installieren können. Wenn Sie diese Richtlinie bereitstellen, werden alle Erweiterungen in dieser Liste, die zuvor installiert wurden, deaktiviert, und der Benutzer ist nicht in der Lage, sie zu aktivieren. Wenn Sie ein Element aus der Liste der blockierten Erweiterungen entfernen, wird diese Erweiterung überall, wo sie zuvor installiert war, automatisch wieder aktiviert.

Verwenden Sie "*", um alle Erweiterungen zu blockieren, die nicht explizit in der Zulassungsliste aufgelistet sind.

Wenn Sie diese Richtlinie nicht konfigurieren, können Benutzer beliebige Erweiterungen in Microsoft Edge installieren.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Liste von Zeichenfolgen

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: ExtensionInstallBlocklist
  - GP-Name: Steuern, welche Erweiterungen nicht installiert werden können
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Extensions
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallBlocklist
  - Pfad (Empfohlen): n.a.
  - Wertname: 1, 2, 3, ...
  - Werttyp: REG_SZ-Liste

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallBlocklist\1 = "extension_id1"
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallBlocklist\2 = "extension_id2"

```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: ExtensionInstallBlocklist
  - Beispielwert:
``` xml
<array>
  <string>extension_id1</string>
  <string>extension_id2</string>
</array>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### ExtensionInstallForcelist

  #### Steuern, welche Erweiterungen im Hintergrund installiert werden

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Legen Sie diese Richtlinie fest, um eine Liste der Apps und Erweiterungen anzugeben, die ohne Benutzerinteraktion im Hintergrund installiert werden. Benutzer können diese Einstellung nicht deinstallieren oder deaktivieren. Berechtigungen werden implizit gewährt, einschließlich der Erweiterungs-APIs enterprise.deviceAttributes und enterprise.platformKeys. Hinweis: Diese beiden APIs sind für Apps und Erweiterungen, deren Installation nicht erzwungen wird, nicht verfügbar.

Wenn Sie diese Richtlinie nicht festlegen, werden keine Apps oder Erweiterungen automatisch installiert, und Benutzer können jede beliebige App in Microsoft Edge deinstallieren.

Diese Richtlinie ersetzt die [ExtensionInstallBlocklist](#extensioninstallblocklist)-Richtlinie. Wenn eine App oder Erweiterung, deren Installation zuvor erzwungen wurde, aus dieser Liste entfernt wird, wird Sie von Microsoft Edge automatisch deinstalliert.

Auf Microsoft Windows-Instanzen kann die Installation von Apps und Erweiterungen von außerhalb der Microsoft Edge Add-ons-Website nur dann erzwungen werden, wenn die Instanz mit einer Microsoft Active Directory-Domäne verbunden ist und Windows 10 Pro ausgeführt wird.

Auf macOS-Instanzen kann die Installation von Apps und Erweiterungen von außerhalb der Microsoft Edge-Add-ons-Website nur dann erzwungen werden, wenn die Instanz über MDM verwaltet oder über MCX mit einer Domäne verbunden wird.

Der Quellcode einer beliebigen Erweiterung kann von Benutzern mit Entwicklertools geändert werden, wodurch die Erweiterung möglicherweise nicht mehr funktionsfähig ist. Wenn dies ein Problem darstellt, konfigurieren Sie die DeveloperToolsDisabled-Richtlinie.

Jedes Listenelement der Richtlinie ist eine Zeichenfolge, die eine Erweiterungs-ID und optional eine durch ein Semikolon (;) abgetrennte „Update“-URL enthält. Die Erweiterungs-ID ist die Zeichenfolge mit 32 Buchstaben, die beispielsweise auf edge://extensions im Entwicklermodus gefunden wird. Wenn angegeben, sollte die „Update“-URL auf ein Update-Manifest-XML-Dokument ( [https://go.microsoft.com/fwlink/?linkid=2095043](https://go.microsoft.com/fwlink/?linkid=2095043) ) verweisen. Standardmäßig wird die Update-URL der Microsoft Edge-Add-ons-Website verwendet. Die in dieser Richtlinie gesetzte „Update“-URL wird nur für die Erstinstallation verwendet; bei nachfolgenden Aktualisierungen der Erweiterung wird die Update-URL im Manifest der Erweiterung verwendet.

Hinweis: Diese Richtlinie gilt nicht für den InPrivate-Modus. Informieren Sie sich über Hosting-Erweiterungen (https://docs.microsoft.com/microsoft-edge/extensions-chromium/enterprise/hosting-and-updating).

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Liste von Zeichenfolgen

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: ExtensionInstallForcelist
  - GP-Name: Steuern, welche Erweiterungen im Hintergrund installiert werden
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Extensions
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallForcelist
  - Pfad (Empfohlen): n.a.
  - Wertname: 1, 2, 3, ...
  - Werttyp: REG_SZ-Liste

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallForcelist\1 = "gbchcmhmhahfdphkhkmpfmihenigjmpp;https://edge.microsoft.com/extensionwebstorebase/v1/crx"
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallForcelist\2 = "abcdefghijklmnopabcdefghijklmnop"

```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: ExtensionInstallForcelist
  - Beispielwert:
``` xml
<array>
  <string>gbchcmhmhahfdphkhkmpfmihenigjmpp;https://edge.microsoft.com/extensionwebstorebase/v1/crx</string>
  <string>abcdefghijklmnopabcdefghijklmnop</string>
</array>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### ExtensionInstallSources

  #### Konfigurieren von Erweiterungen und Installationsquellen für Benutzerskripts

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  URLs definieren, von denen Erweiterungen und Designs installiert werden können.

URLs definieren, von denen Erweiterungen und Designs direkt installiert werden können, ohne dass die Pakete per Drag & Drop auf die Seite edge://extensions gezogen werden müssen.

Jedes Element in dieser Liste ist ein Übereinstimmungsmuster im Erweiterungs-Stil (siehe [https://go.microsoft.com/fwlink/?linkid=2095039](https://go.microsoft.com/fwlink/?linkid=2095039)). Benutzer können Elemente ganz einfach von einer beliebigen URL aus installieren, die einem Element in dieser Liste entspricht. Sowohl der Speicherort der Datei "*.crx" als auch die Seite, von der der Download ausgeführt wird (mit anderen Worten, der Referrer), muss von diesen Mustern her zulässig sein. Hosten Sie die Dateien nicht an einem Ort, für den eine Authentifizierung erforderlich ist.

Die Richtlinie [ExtensionInstallBlocklist](#extensioninstallblocklist) hat Vorrang vor dieser Richtlinie. Erweiterungen, die sich in der Blockier-Liste befinden, werden nicht installiert, auch wenn sie von einer-Website in dieser Liste stammen.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Liste von Zeichenfolgen

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: ExtensionInstallSources
  - GP-Name: Konfigurieren von Erweiterungen und Installationsquellen für Benutzerskripts
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Extensions
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallSources
  - Pfad (Empfohlen): n.a.
  - Wertname: 1, 2, 3, ...
  - Werttyp: REG_SZ-Liste

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallSources\1 = "https://corp.contoso.com/*"

```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: ExtensionInstallSources
  - Beispielwert:
``` xml
<array>
  <string>https://corp.contoso.com/*</string>
</array>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### ExtensionSettings

  #### Konfigurieren der Erweiterungsverwaltungseinstellungen

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Konfiguriert Erweiterungsverwaltungseinstellungen für Microsoft Edge.

Diese Richtlinie steuert mehrere Einstellungen, einschließlich der Einstellungen, die von allen vorhandenen Erweiterungs-bezogenen Richtlinien gesteuert werden. Diese Richtlinie setzt alle Legacy-Richtlinien außer Kraft, wenn beide festgelegt sind.

Mit dieser Richtlinie wird eine Erweiterungs-ID oder eine Update-URL ihrer jeweiligen Konfiguration zugeordnet. Bei einer Erweiterungs-ID wird die Konfiguration nur auf die angegebene Erweiterung angewendet. Legen Sie eine Standardkonfiguration für die spezielle ID "*" fest, damit diese auf alle Erweiterungen angewendet wird, die in dieser Richtlinie nicht ausdrücklich aufgelistet sind. Bei einer Update-URL wird die Konfiguration auf alle Erweiterungen angewendet, die die genaue Aktualisierungs-URL aufweisen, die im Manifest dieser Erweiterung angegeben ist, wie unter [https://go.microsoft.com/fwlink/?linkid=2095043](https://go.microsoft.com/fwlink/?linkid=2095043)beschrieben.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Dictionary

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: ExtensionSettings
  - GP-Name: Konfigurieren der Erweiterungsverwaltungseinstellungen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Extensions
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: ExtensionSettings
  - Werttyp: REG_SZ

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\ExtensionSettings = {
  "*": {
    "allowed_types": [
      "hosted_app"
    ], 
    "blocked_install_message": "Custom error message.", 
    "blocked_permissions": [
      "downloads", 
      "bookmarks"
    ], 
    "install_sources": [
      "https://company-intranet/apps"
    ], 
    "installation_mode": "blocked", 
    "runtime_allowed_hosts": [
      "*://good.contoso.com"
    ], 
    "runtime_blocked_hosts": [
      "*://*.contoso.com"
    ]
  }, 
  "abcdefghijklmnopabcdefghijklmnop": {
    "blocked_permissions": [
      "history"
    ], 
    "installation_mode": "allowed", 
    "minimum_version_required": "1.0.1"
  }, 
  "bcdefghijklmnopabcdefghijklmnopa": {
    "allowed_permissions": [
      "downloads"
    ], 
    "installation_mode": "force_installed", 
    "runtime_allowed_hosts": [
      "*://good.contoso.com"
    ], 
    "runtime_blocked_hosts": [
      "*://*.contoso.com"
    ], 
    "update_url": "https://contoso.com/update_url"
  }, 
  "cdefghijklmnopabcdefghijklmnopab": {
    "blocked_install_message": "Custom error message.", 
    "installation_mode": "blocked"
  }, 
  "defghijklmnopabcdefghijklmnopabc,efghijklmnopabcdefghijklmnopabcd": {
    "blocked_install_message": "Custom error message.", 
    "installation_mode": "blocked"
  }, 
  "fghijklmnopabcdefghijklmnopabcde": {
    "blocked_install_message": "Custom removal message.", 
    "installation_mode": "removed"
  }, 
  "update_url:https://www.contoso.com/update.xml": {
    "allowed_permissions": [
      "downloads"
    ], 
    "blocked_permissions": [
      "wallpaper"
    ], 
    "installation_mode": "allowed"
  }
}
```

  ##### Kompakter Beispielwert:

  ```
  SOFTWARE\Policies\Microsoft\Edge\ExtensionSettings = {"*": {"allowed_types": ["hosted_app"], "blocked_install_message": "Custom error message.", "blocked_permissions": ["downloads", "bookmarks"], "install_sources": ["https://company-intranet/apps"], "installation_mode": "blocked", "runtime_allowed_hosts": ["*://good.contoso.com"], "runtime_blocked_hosts": ["*://*.contoso.com"]}, "abcdefghijklmnopabcdefghijklmnop": {"blocked_permissions": ["history"], "installation_mode": "allowed", "minimum_version_required": "1.0.1"}, "bcdefghijklmnopabcdefghijklmnopa": {"allowed_permissions": ["downloads"], "installation_mode": "force_installed", "runtime_allowed_hosts": ["*://good.contoso.com"], "runtime_blocked_hosts": ["*://*.contoso.com"], "update_url": "https://contoso.com/update_url"}, "cdefghijklmnopabcdefghijklmnopab": {"blocked_install_message": "Custom error message.", "installation_mode": "blocked"}, "defghijklmnopabcdefghijklmnopabc,efghijklmnopabcdefghijklmnopabcd": {"blocked_install_message": "Custom error message.", "installation_mode": "blocked"}, "fghijklmnopabcdefghijklmnopabcde": {"blocked_install_message": "Custom removal message.", "installation_mode": "removed"}, "update_url:https://www.contoso.com/update.xml": {"allowed_permissions": ["downloads"], "blocked_permissions": ["wallpaper"], "installation_mode": "allowed"}}
  ```
  

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: ExtensionSettings
  - Beispielwert:
``` xml
<key>ExtensionSettings</key>
<dict>
  <key>*</key>
  <dict>
    <key>allowed_types</key>
    <array>
      <string>hosted_app</string>
    </array>
    <key>blocked_install_message</key>
    <string>Custom error message.</string>
    <key>blocked_permissions</key>
    <array>
      <string>downloads</string>
      <string>bookmarks</string>
    </array>
    <key>install_sources</key>
    <array>
      <string>https://company-intranet/apps</string>
    </array>
    <key>installation_mode</key>
    <string>blocked</string>
    <key>runtime_allowed_hosts</key>
    <array>
      <string>*://good.contoso.com</string>
    </array>
    <key>runtime_blocked_hosts</key>
    <array>
      <string>*://*.contoso.com</string>
    </array>
  </dict>
  <key>abcdefghijklmnopabcdefghijklmnop</key>
  <dict>
    <key>blocked_permissions</key>
    <array>
      <string>history</string>
    </array>
    <key>installation_mode</key>
    <string>allowed</string>
    <key>minimum_version_required</key>
    <string>1.0.1</string>
  </dict>
  <key>bcdefghijklmnopabcdefghijklmnopa</key>
  <dict>
    <key>allowed_permissions</key>
    <array>
      <string>downloads</string>
    </array>
    <key>installation_mode</key>
    <string>force_installed</string>
    <key>runtime_allowed_hosts</key>
    <array>
      <string>*://good.contoso.com</string>
    </array>
    <key>runtime_blocked_hosts</key>
    <array>
      <string>*://*.contoso.com</string>
    </array>
    <key>update_url</key>
    <string>https://contoso.com/update_url</string>
  </dict>
  <key>cdefghijklmnopabcdefghijklmnopab</key>
  <dict>
    <key>blocked_install_message</key>
    <string>Custom error message.</string>
    <key>installation_mode</key>
    <string>blocked</string>
  </dict>
  <key>defghijklmnopabcdefghijklmnopabc,efghijklmnopabcdefghijklmnopabcd</key>
  <dict>
    <key>blocked_install_message</key>
    <string>Custom error message.</string>
    <key>installation_mode</key>
    <string>blocked</string>
  </dict>
  <key>fghijklmnopabcdefghijklmnopabcde</key>
  <dict>
    <key>blocked_install_message</key>
    <string>Custom removal message.</string>
    <key>installation_mode</key>
    <string>removed</string>
  </dict>
  <key>update_url:https://www.contoso.com/update.xml</key>
  <dict>
    <key>allowed_permissions</key>
    <array>
      <string>downloads</string>
    </array>
    <key>blocked_permissions</key>
    <array>
      <string>wallpaper</string>
    </array>
    <key>installation_mode</key>
    <string>allowed</string>
  </dict>
</dict>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ## HTTP-Authentifizierungsrichtlinien

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### AllowCrossOriginAuthPrompt

  #### Zulassen ursprungsübergreifender HTTP-Authentifizierungsaufforderungen

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Controls whether third-party images on a page can show an authentication prompt.

Normalerweise ist dies als Phishing-Abwehr deaktiviert. Wenn Sie diese Richtlinie nicht konfigurieren, ist sie deaktiviert, und Bilder von Drittanbietern können keine Authentifizierungsaufforderung anzeigen.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: AllowCrossOriginAuthPrompt
  - GP-Name: Zulassen ursprungsübergreifender HTTP-Authentifizierungsaufforderungen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/HTTP authentication
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: AllowCrossOriginAuthPrompt
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000000
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: AllowCrossOriginAuthPrompt
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### AuthNegotiateDelegateAllowlist

  #### Gibt eine Liste der Server an, an die Microsoft Edge Benutzeranmeldeinformationen delegieren kann

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Konfiguriert die Liste der Server an, an die Microsoft Edge delegieren kann.

Trennen Sie mehrere Servernamen durch Kommas. Platzhalter (*) sind zulässig.

Wenn Sie diese Richtlinie nicht konfigurieren, delegiert Microsoft Edge keine Benutzeranmeldeinformationen, auch wenn ein Server als Intranet erkannt wird.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Zeichenfolge

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: AuthNegotiateDelegateAllowlist
  - GP-Name: Gibt eine Liste der Server an, an die Microsoft Edge Benutzeranmeldeinformationen delegieren kann
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/HTTP authentication
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: AuthNegotiateDelegateAllowlist
  - Werttyp: REG_SZ

  ##### Beispielwert:

```
"contoso.com"
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: AuthNegotiateDelegateAllowlist
  - Beispielwert:
``` xml
<string>contoso.com</string>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### AuthSchemes

  #### Unterstützte Authentifizierungsschemas

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Gibt an, welche HTTP-Authentifizierungsschemas unterstützt werden.

Sie können die Richtlinie mit diesen Werten konfigurieren: "basic", "digest", "NTLM" und "negotiate". Trennen Sie mehrere Werte durch Kommata.

Wenn Sie diese Richtlinie nicht konfigurieren, werden alle vier Schemas verwendet.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Zeichenfolge

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: AuthSchemes
  - GP-Name: Unterstützte Authentifizierungsschemas
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/HTTP authentication
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: AuthSchemes
  - Werttyp: REG_SZ

  ##### Beispielwert:

```
"basic,digest,ntlm,negotiate"
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: AuthSchemes
  - Beispielwert:
``` xml
<string>basic,digest,ntlm,negotiate</string>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### AuthServerAllowlist

  #### Konfigurieren der Liste der zulässigen Authentifizierungsserver

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Gibt an, welche Server für die integrierte Authentifizierung aktiviert werden sollen. Die integrierte Authentifizierung ist nur verfügbar, wenn Microsoft Edge eine Authentifizierungsabfrage von einem Proxy oder von einem Server in dieser Liste empfängt.

Trennen Sie mehrere Servernamen durch Kommas. Platzhalter (*) sind zulässig.

Wenn Sie diese Richtlinie nicht konfigurieren, versucht Microsoft Edge zu erkennen, ob sich ein Server im Intranet befindet. Nur dann reagiert es auf IWA-Anforderungen. Wenn sich der Server im Internet befindet, werden IWA-Anfragen dieses Servers von Microsoft Edge ignoriert.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Zeichenfolge

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: AuthServerAllowlist
  - GP-Name: Konfigurieren der Liste der zulässigen Authentifizierungsserver
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/HTTP authentication
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: AuthServerAllowlist
  - Werttyp: REG_SZ

  ##### Beispielwert:

```
"*contoso.com,contoso.com"
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: AuthServerAllowlist
  - Beispielwert:
``` xml
<string>*contoso.com,contoso.com</string>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### DisableAuthNegotiateCnameLookup

  #### Deaktivieren des CNAME-Lookup beim Verhandeln der Kerberos-Authentifizierung

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Bestimmt, ob der generierte Kerberos-SPN auf dem kanonischen DNS-Namen (CNAME) oder auf dem ursprünglich eingegebenen Namen basiert.

Wenn Sie diese Richtlinie aktivieren, wird das CNAME-Lookup übersprungen, und der Servername (wie eingegeben) wird verwendet.

Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, wird der kanonische Name des Servers verwendet.  Dies wird durch CNAME-Lookup bestimmt.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: DisableAuthNegotiateCnameLookup
  - GP-Name: Deaktivieren des CNAME-Lookup beim Verhandeln der Kerberos-Authentifizierung
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/HTTP authentication
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: DisableAuthNegotiateCnameLookup
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000000
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: DisableAuthNegotiateCnameLookup
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### EnableAuthNegotiatePort

  #### Einschließen eines nicht standardmäßigen Ports in Kerberos-SPN

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Gibt an, ob der generierte Kerberos-SPN einen nicht-standardmäßigen Port enthalten soll.

Wenn Sie diese Richtlinie aktivieren und ein Benutzer einen nicht-standardmäßigen Port (einen Port außer "80" oder "443") in einer URL einschließt, ist dieser Port Bestandteil des generierten Kerberos-SPN.

Wenn Sie diese Richtlinie nicht konfigurieren oder deaktivieren, enthält der generierte Kerberos-SPN in keinem Fall einen Port.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: EnableAuthNegotiatePort
  - GP-Name: Einschließen eines nicht standardmäßigen Ports in Kerberos-SPN
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/HTTP authentication
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: EnableAuthNegotiatePort
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000000
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: EnableAuthNegotiatePort
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### NtlmV2Enabled

  #### Steuern, ob die NTLMv2-Authentifizierung aktiviert ist

  
  
  #### Unterstützte Versionen:

  - Auf macOS ab 77 oder höher

  #### Beschreibung

  Steuert, ob NTLMv2 aktiviert ist.

Alle neueren Versionen von Samba und Windows-Servern unterstützen NTLMv2. Sie sollten NTLMv2 nur deaktivieren, um Probleme mit der Abwärtskompatibilität zu beheben, da dadurch die Sicherheit der Authentifizierung verringert wird.

Wenn Sie diese Richtlinie nicht konfigurieren, ist NTLMv2 standardmäßig aktiviert.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: NtlmV2Enabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ## Richtlinien für Einstellungen für den Kioskmodus

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### KioskAddressBarEditingEnabled

  #### Konfigurieren der Adressleistenbearbeitung für die öffentliche Browsernutzung im Kioskmodus.

  
  
  #### Unterstützte Versionen:

  - On Windows and macOS since 87 or later

  #### Beschreibung

  Diese Richtlinie gilt nur für den Microsoft Edge-Kioskmodus, während die öffentliche Browseroberfläche verwendet wird.

Wenn Sie diese Richtlinie aktivieren, können Benutzer die URL in der Adressleiste nicht ändern.

Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, können die Benutzer die URL in der Adressleiste ändern.

Ausführliche Informationen zum Konfigurieren des Kioskmodus finden Sie unter [https://go.microsoft.com/fwlink/?linkid=2137578](https://go.microsoft.com/fwlink/?linkid=2137578).

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - Eindeutiger GP-Name: KioskAddressBarEditingEnabled
  - GP-Name: Konfigurieren der Adressleistenbearbeitung für die öffentliche Browsernutzung im Kioskmodus.
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Kiosk Mode settings
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: KioskAddressBarEditingEnabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: KioskAddressBarEditingEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### KioskDeleteDownloadsOnExit

  #### Löschen von Dateien, die während einer Kiosk-Sitzung heruntergeladen wurden, wenn Microsoft Edge geschlossen wird

  
  
  #### Unterstützte Versionen:

  - Unter Windows seit 87 oder später

  #### Beschreibung

  Diese Richtlinie bezieht sich nur auf Microsoft Edge-Kioskmodus.

Wenn Sie diese Richtlinie aktivieren, werden Dateien, die während einer Kiosk-Sitzung heruntergeladen wurden, beim Schließen von Microsoft Edge jedes Mal gelöscht.

Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, werden Dateien, die während einer Kiosk-Sitzung heruntergeladen wurden, beim Schließen von Microsoft Edge nicht gelöscht.

Ausführliche Informationen zum Konfigurieren des Kioskmodus finden Sie unter [https://go.microsoft.com/fwlink/?linkid=2137578](https://go.microsoft.com/fwlink/?linkid=2137578).

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - Eindeutiger GP-Name: KioskDeleteDownloadsOnExit
  - GP-Name: Löschen von Dateien, die während einer Kiosk-Sitzung heruntergeladen wurden, wenn Microsoft Edge geschlossen wird
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Kiosk Mode settings
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: KioskDeleteDownloadsOnExit
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ## Richtlinien zum systemeigenen Messaging

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### NativeMessagingAllowlist

  #### Steuern, welche systemeigenen Messaging-Hosts Benutzer verwenden können

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Listen Sie bestimmte systemeigene Messaginghosts auf, die Benutzer in Microsoft Edge verwenden können.

Standardmäßig sind alle systemeigenen Messaginghosts zulässig. Wenn Sie die [NativeMessagingBlocklist](#nativemessagingblocklist) Richtlinie auf * festlegen, werden alle systemeigenen Messaginghosts blockiert, und es werden nur die hier aufgeführten systemeigenen Messaginghosts geladen.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Liste von Zeichenfolgen

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: NativeMessagingAllowlist
  - GP-Name: Steuern, welche systemeigenen Messaging-Hosts Benutzer verwenden können
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Native Messaging
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge\NativeMessagingAllowlist
  - Pfad (Empfohlen): n.a.
  - Wertname: 1, 2, 3, ...
  - Werttyp: REG_SZ-Liste

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\NativeMessagingAllowlist\1 = "com.native.messaging.host.name1"
SOFTWARE\Policies\Microsoft\Edge\NativeMessagingAllowlist\2 = "com.native.messaging.host.name2"

```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: NativeMessagingAllowlist
  - Beispielwert:
``` xml
<array>
  <string>com.native.messaging.host.name1</string>
  <string>com.native.messaging.host.name2</string>
</array>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### NativeMessagingBlocklist

  #### Konfigurieren der systemeigenen Nachrichten-Sperrliste

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Gibt an, welche systemeigenen Messaginghosts nicht verwendet werden sollten.

Verwenden Sie "*", um alle systemeigenen Messaginghosts zu blockieren, es sei denn, sie werden in der Zulassungsliste explizit aufgelistet.

Wenn Sie diese Richtlinie nicht konfigurieren, lädt Microsoft Edge alle installierten, systemeigenen Messaginghosts.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Liste von Zeichenfolgen

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: NativeMessagingBlocklist
  - GP-Name: Konfigurieren der systemeigenen Nachrichten-Sperrliste
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Native Messaging
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge\NativeMessagingBlocklist
  - Pfad (Empfohlen): n.a.
  - Wertname: 1, 2, 3, ...
  - Werttyp: REG_SZ-Liste

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\NativeMessagingBlocklist\1 = "com.native.messaging.host.name1"
SOFTWARE\Policies\Microsoft\Edge\NativeMessagingBlocklist\2 = "com.native.messaging.host.name2"

```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: NativeMessagingBlocklist
  - Beispielwert:
``` xml
<array>
  <string>com.native.messaging.host.name1</string>
  <string>com.native.messaging.host.name2</string>
</array>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### NativeMessagingUserLevelHosts

  #### Zulassen systemeigener Messaging-Hosts auf Benutzerebene (ohne Administratorberechtigungen installiert)

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Ermöglicht die Installation von systemeigenen Messaginghosts auf Benutzerebene.

Wenn Sie diese Richtlinie deaktivieren, verwendet Microsoft Edge nur auf Systemebene installierte, systemeigene Messaginghosts.

Als Standard, falls Sie diese Richtlinie nicht konfigurieren, gestattet Microsoft Edge die Nutzung von systemeigenen Messaginghosts auf Benutzerebene.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: NativeMessagingUserLevelHosts
  - GP-Name: Zulassen systemeigener Messaging-Hosts auf Benutzerebene (ohne Administratorberechtigungen installiert)
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Native Messaging
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: NativeMessagingUserLevelHosts
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000000
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: NativeMessagingUserLevelHosts
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ## Kennwortmanager- und Schutz-Richtlinien

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### PasswordManagerEnabled

  #### Aktivieren des Speicherung von Kennwörtern im Kennwort-Manager

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Aktivieren, dass Microsoft Edge Benutzerkennwörter speichert.

Wenn Sie diese Richtlinie aktivieren, können die Benutzer ihre Kennwörter in Microsoft Edge speichern. Wenn Sie eine Website das nächste Mal besuchen, gibt Microsoft Edge das Kennwort automatisch ein.

Wenn Sie diese Richtlinie deaktivieren, können die Benutzer keine neuen Kennwörter speichern, sie können aber weiterhin bisher gespeicherte Kennwörter verwenden.

Wenn Sie diese Richtlinie aktivieren oder deaktivieren, können die Benutzer sie in Microsoft Edge nicht ändern oder außer Kraft setzen. Wenn Sie sie nicht konfigurieren, können Benutzer Kennwörter speichern und diese Funktion deaktivieren.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: PasswordManagerEnabled
  - GP-Name: Aktivieren des Speicherung von Kennwörtern im Kennwort-Manager
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Password manager and protection
  - GP Pfad (Empfohlen): Administrative Templates/Microsoft Edge – Standardeinstellungen (Benutzer können diese außer Kraft setzen)/Password manager and protection
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Wertname: PasswordManagerEnabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: PasswordManagerEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### PasswordMonitorAllowed

  #### Zulassen, dass Benutzer benachrichtigt werden, wenn Ihre Kennwörter als unsicher eingestuft werden

  
  
  #### Unterstützte Versionen:

  - Auf Windows seit 85 oder später

  #### Beschreibung

  Zulassen, dass Microsoft Edge Benutzerkennwörter überwacht.

Wenn Sie diese Richtlinie aktivieren und ein Benutzer dem Aktivieren der Richtlinie zustimmt, wird der Benutzer benachrichtigt, wenn eines der in Microsoft Edge gespeicherten Kennwörter als unsicher eingestuft wird. In Microsoft Edge wird eine Warnung angezeigt, und diese Informationen sind auch in den Einstellungen > Kennwörter > Kennwort-Monitor verfügbar.

Wenn Sie diese Richtlinie deaktivieren, werden die Benutzer nicht um Erlaubnis gebeten, dieses Feature zu aktivieren. Ihre Kennwörter werden nicht gescannt, und Sie werden auch nicht benachrichtigt.

Wenn Sie die Richtlinie aktivieren oder nicht konfigurieren, können die Benutzer dieses Feature aktivieren oder deaktivieren.

Wenn Sie mehr darüber erfahren möchten, wie Microsoft Edge unsichere Kennwörter findet, lesen Sie [https://go.microsoft.com/fwlink/?linkid=2133833](https://go.microsoft.com/fwlink/?linkid=2133833)

Zusätzliche Anleitung:

Diese Richtlinie kann sowohl als empfohlen als auch als obligatorisch festgelegt werden, jedoch mit einer wichtigen Legende.

Obligatorische Aktivierung: vorausgesetzt, dass die Zustimmung des einzelnen Benutzers eine Voraussetzung für die Aktivierung dieses Features für einen bestimmten Benutzer ist, gibt es für diese Richtlinie keine Einstellung "erforderlich". Wenn die Richtlinie auf "obligatorisch" aktiviert ist, ändert sich die Benutzeroberfläche in "Einstellungen" nicht, und die folgende Fehlermeldung wird in edge://policy angezeigt.

Beispiel Fehlerstatusmeldung: "dieser Richtlinienwert wird ignoriert, da für die Kennwortüberwachung das Einverständnis des jeweiligen Benutzers erforderlich ist. Sie können die Benutzer in Ihrer Organisation bitten, zu Einstellungen > Profil > Kennwort zu wechseln, und das Feature aktivieren."

Empfohlene Aktivierung: Wenn für die Richtlinie die Option „Empfohlen“ aktiviert festgelegt ist, verbleiben die Benutzeroberfläche in Einstellungen im Status "aus", aber es wird ein Aktenkoffersymbol angezeigt, bei dem diese Beschreibung beim Hovern angezeigt wird: "Ihre Organisation empfiehlt einen bestimmten Wert für diese Einstellung, und Sie haben einen anderen Wert gewählt"

Obligatorisch und Empfohlen deaktiviert: beide Zustände funktionieren in der normalen Weise, wobei die normalen Beschriftungen Benutzern angezeigt werden.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - Eindeutiger Name des GP: PasswordMonitorAllowed
  - GP-Name: erlauben Sie Benutzern, benachrichtigt zu werden, wenn Ihre Kennwörter als unsicher eingestuft werden.
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Password manager and protection
  - GP Pfad (Empfohlen): Administrative Templates/Microsoft Edge – Standardeinstellungen (Benutzer können diese außer Kraft setzen)/Password manager and protection
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Wertname: PasswordMonitorAllowed
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### PasswordProtectionChangePasswordURL

  #### Konfigurieren der URL für das Ändern eines Kennworts

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Konfiguriert die Kennwort-Ändern-URL (nur HTTP- und HTTPS-Schemata).

Der Kennwortschutzdienst leitet Benutzer an diese URL weiter, um ihr Kennwort zu ändern, nachdem ihnen eine Warnung im Browser angezeigt wurde.

Wenn Sie diese Richtlinie aktivieren, sendet der Kennwortschutzdienst Benutzer an diese URL, um ihr Kennwort zu ändern.

Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, leitet der Kennwortschutzdienst Benutzer nicht zu einer Kennwort-Ändern-URL um.

Diese Richtlinie ist nur für Windows-Instanzen verfügbar, die mit einer Microsoft Active Directory-Domäne verknüpft sind, Windows 10 Pro- oder Enterprise-Instanzen, die für die Geräteverwaltung registriert sind, oder MacOS-Instanzen, die über MDM verwaltet oder über MCX einer Domäne beigetreten sind.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Zeichenfolge

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: PasswordProtectionChangePasswordURL
  - GP-Name: Konfigurieren der URL für das Ändern eines Kennworts
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Password manager and protection
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: PasswordProtectionChangePasswordURL
  - Werttyp: REG_SZ

  ##### Beispielwert:

```
"https://contoso.com/change_password.html"
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: PasswordProtectionChangePasswordURL
  - Beispielwert:
``` xml
<string>https://contoso.com/change_password.html</string>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### PasswordProtectionLoginURLs

  #### Konfigurieren Sie die Liste der Unternehmens-Login-URLs, bei denen der Kennwortschutzdienst gesalzene Hashes eines Kennworts sammeln soll

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Konfigurieren Sie die Liste der Unternehmensanmelde-URLs (nur HTTP- und HTTPS-Schemata), bei denen Microsoft Edge die gesalzenen Hashes von Kennwörtern sammeln und für die Erkennung der Kennwortwiederverwendung verwenden soll.

Wenn Sie diese Richtlinie aktivieren, erfasst der Kennwortschutzdienst Fingerabdrücke von Kennwörtern auf den definierten URLs.

Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, werden keine Kennwort-Fingerabdrücke erfasst.

Diese Richtlinie ist nur für Windows-Instanzen verfügbar, die mit einer Microsoft Active Directory-Domäne verknüpft sind, Windows 10 Pro- oder Enterprise-Instanzen, die für die Geräteverwaltung registriert sind, oder MacOS-Instanzen, die über MDM verwaltet oder über MCX einer Domäne beigetreten sind.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Liste von Zeichenfolgen

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: PasswordProtectionLoginURLs
  - GP-Name: Konfigurieren Sie die Liste der Unternehmensanmelde-URLs, bei denen der Kennwortschutzdienst gesalzene Hashes eines Kennworts sammeln soll
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Password manager and protection
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge\PasswordProtectionLoginURLs
  - Pfad (Empfohlen): n.a.
  - Wertname: 1, 2, 3, ...
  - Werttyp: REG_SZ-Liste

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\PasswordProtectionLoginURLs\1 = "https://contoso.com/login.html"
SOFTWARE\Policies\Microsoft\Edge\PasswordProtectionLoginURLs\2 = "https://login.contoso.com"

```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: PasswordProtectionLoginURLs
  - Beispielwert:
``` xml
<array>
  <string>https://contoso.com/login.html</string>
  <string>https://login.contoso.com</string>
</array>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### PasswordProtectionWarningTrigger

  #### Auslösung der Warnung zum Kennwortschutz konfigurieren

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Ermöglicht es Ihnen, zu steuern, wann Kennwortschutz-Warnungen ausgelöst werden. Kennwortschutz benachrichtigt Benutzer, wenn diese Ihre geschützten Kennwörter auf potenziell verdächtigen Websites wiederverwenden.

Sie können die Richtlinien [PasswordProtectionLoginURLs](#passwordprotectionloginurls) und [PasswordProtectionChangePasswordURL](#passwordprotectionchangepasswordurl) verwenden, um zu konfigurieren, welche Kennwörter geschützt werden sollen.

Ausnahmen: Kennwörter für die in [PasswordProtectionLoginURLs](#passwordprotectionloginurls) und [PasswordProtectionChangePasswordURL](#passwordprotectionchangepasswordurl) aufgeführten Websites sowie für die in [SmartScreenAllowListDomains](#smartscreenallowlistdomains) aufgeführten Websites lösen keine Warnung durch den Kennwortschutz aus.

Auf „PasswordProtectionWarningOff“ setzen, um keine Kennwortschutzwarnungen anzuzeigen.

Auf „PasswordProtectionWarningOnPasswordReuse“ setzen, um Kennwortschutzwarnungen anzuzeigen, wenn der Benutzer sein geschütztes Kennwort auf einer Website wiederverwendet, die nicht auf einer Erlaubnisliste steht.

Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, wird dieser Warnhinweis nicht angezeigt.

Zuordnung von Richtlinienoptionen:

* PasswordProtectionWarningOff (0) = Kennwortschutzwarnung ist deaktiviert

* PasswordProtectionWarningOnPasswordReuse (1) = Kennwortschutzwarnung wird durch Wiederverwendung von Kennwörtern ausgelöst

Verwenden Sie die vorstehenden Informationen, wenn Sie diese Richtlinie konfigurieren.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Ganze Zahl

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: PasswordProtectionWarningTrigger
  - GP-Name: Auslösung der Warnung zum Kennwortschutz konfigurieren
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Password manager and protection
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: PasswordProtectionWarningTrigger
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: PasswordProtectionWarningTrigger
  - Beispielwert:
``` xml
<integer>1</integer>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### PasswordRevealEnabled

  #### Schaltfläche „Kennwort anzeigen“ aktivieren

  
  
  #### Unterstützte Versionen:

  - On Windows and macOS since 87 or later

  #### Beschreibung

  Ermöglicht es Ihnen, die Standardanzeige der Browser-Schaltfläche "Kennwort anzeigen" für Kennworteingabefelder auf Websites zu konfigurieren.

Wenn Sie diese Richtlinie aktivieren oder nicht konfigurieren, werden die Benutzereinstellungen des Browsers die Schaltfläche „Kennwort anzeigen“ standardmäßig anzeigen.

Wenn Sie diese Richtlinie deaktivieren, werden die Benutzereinstellungen des Browsers die Schaltfläche „Kennwort anzeigen“ nicht anzeigen.

Für die Barrierefreiheit können Benutzer die Browsereinstellung gegenüber der Standardrichtlinie ändern.

Diese Richtlinie hat nur Einfluss auf die Browser-Schaltfläche „Kennwort anzeigen“. Sie wirkt sich nicht auf benutzerdefinierte Anzeigeschaltflächen in Websites aus.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Nein
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - Eindeutiger GP-Name: PasswordRevealEnabled
  - GP-Name: Schaltfläche „Kennwort anzeigen“ aktivieren
  - GP-Pfad (verpflichtend): N/A
  - GP Pfad (Empfohlen): Administrative Templates/Microsoft Edge – Standardeinstellungen (Benutzer können diese außer Kraft setzen)/Password manager and protection
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): N/A
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Wertname: PasswordRevealEnabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: PasswordRevealEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ## Leistungsrichtlinien

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### StartupBoostEnabled

  #### Startbeschleunigung aktivieren

  
  
  #### Unterstützte Versionen:

  - Unter Windows ab Version 88 oder höher

  #### Beschreibung

  Microsoft Edge-Prozesse können bei der Betriebssystem-Anmeldung starten und nach dem Schließen des letzten Browserfensters im Hintergrund neu starten.

Wenn Microsoft Edge im Hintergrundmodus ausgeführt wird, wird der Browser u. U. nicht geschlossen, wenn das letzte Fenster geschlossen wird, und nach dem Schließen des Fensters nicht im Hintergrund neu gestartet. Informationen dazu, was nach dem Konfigurieren von Microsoft Edge für den Hintergrundmodus geschieht, finden Sie in der [BackgroundModeEnabled](#backgroundmodeenabled)-Richtlinie.

Wenn Sie diese Richtlinie aktivieren, ist die Startbeschleunigung aktiviert.

Wenn Sie diese Richtlinie deaktivieren, ist die Startbeschleunigung deaktiviert.

Wenn Sie diese Richtlinie nicht konfigurieren, ist die Startbeschleunigung möglicherweise anfänglich aktiviert oder deaktiviert. Der Benutzer kann das Verhalten unter edge://settings/system konfigurieren.

Weitere Informationen zur Startbeschleunigung finden Sie unter [https://go.microsoft.com/fwlink/?linkid=2147018](https://go.microsoft.com/fwlink/?linkid=2147018).

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - Eindeutiger GP-Name: StartupBoostEnabled
  - GP-Name: Startbeschleunigung aktivieren
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Performance
  - GP Pfad (Empfohlen): Administrative Templates/Microsoft Edge – Standardeinstellungen (Benutzer können diese außer Kraft setzen)/Performance
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Wertname: StartupBoostEnabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ## Richtlinien zum Drucken

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### DefaultPrinterSelection

  #### Regeln zur Auswahl des Standarddruckers

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Setzt die Auswahlregeln für Standarddrucker für Microsoft Edge außer Kraft. Diese Richtlinie bestimmt die Regeln für die Auswahl des Standarddruckers in Microsoft Edge, was passiert, wenn ein Benutzer zum ersten Mal versucht, eine Seite zu drucken.

Wenn diese Richtlinie festgelegt ist, versucht Microsoft Edge, einen Drucker zu finden, der allen angegebenen Attributen entspricht, und verwendet ihn als Standarddrucker. Wenn mehrere Drucker vorhanden sind, die die Kriterien erfüllen, wird der erste übereinstimmende Drucker verwendet.

Wenn Sie diese Richtlinie nicht konfigurieren oder keine übereinstimmenden Drucker innerhalb des Timeouts gefunden werden, ist der Drucker standardmäßig der integrierte PDF-Drucker oder kein Drucker, wenn der PDF-Drucker nicht verfügbar ist.

Der Wert wird als JSON-Objekt analysiert und ist mit dem folgenden Schema konform: { "type": "object", "properties": { "idPattern": { "description": "Regular expression to match printer id.", "type": "string" }, "namePattern": { "description": "Regular expression to match printer display name.", "type": "string" } } }

Wenn ein Feld ausgelassen wird, bedeutet dies, dass alle Werte übereinstimmen. Wenn Sie beispielsweise "Konnektivität" nicht angeben, beginnt die Druckansicht, alle Arten von lokalen Druckern zu erkennen. Muster regulärer Ausdrücke müssen der JavaScript-RegExp-Syntax entsprechen, und bei Übereinstimmungen wird die Groß-/Kleinschreibung beachtet.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Zeichenfolge

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: DefaultPrinterSelection
  - GP-Name: Regeln zur Auswahl des Standarddruckers
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Printing
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: DefaultPrinterSelection
  - Werttyp: REG_SZ

  ##### Beispielwert:

```
"{ \"idPattern\": \".*public\", \"namePattern\": \".*Color\" }"
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: DefaultPrinterSelection
  - Beispielwert:
``` xml
<string>{ "idPattern": ".*public", "namePattern": ".*Color" }</string>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### PrintHeaderFooter

  #### Drucken von Kopf- und Fußzeilen

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Erzwingen Sie im Dialogfeld "Drucken" die Option "Kopf- und Fußzeilen".

Wenn Sie diese Richtlinie nicht konfigurieren, können die Benutzer entscheiden, ob sie Kopf- und Fußzeilen drucken möchten.

Wenn Sie diese Richtlinie deaktivieren, können Benutzer keine Kopf- und Fußzeilen drucken.

Wenn Sie diese Richtlinie aktivieren, drucken Benutzer immer Kopf- und Fußzeilen.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: PrintHeaderFooter
  - GP-Name: Drucken von Kopf- und Fußzeilen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Printing
  - GP Pfad (Empfohlen): Administrative Templates/Microsoft Edge – Standardeinstellungen (Benutzer können diese außer Kraft setzen)/Printing
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Wertname: PrintHeaderFooter
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000000
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: PrintHeaderFooter
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### PrintPreviewUseSystemDefaultPrinter

  #### Standarddrucker des Systems als Standarddrucker festlegen

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Teilt Microsoft Edge mit, den Standarddrucker des Systems als Standardoption für die Seitenansicht anstelle des zuletzt verwendeten Druckers zu verwenden.

Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, verwendet die Seitenansicht den zuletzt verwendeten Drucker als Standardziel.

Wenn Sie diese Richtlinie aktivieren, verwendet die Seitenansicht den Standarddrucker des Betriebssystems als Standardziel.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: PrintPreviewUseSystemDefaultPrinter
  - GP-Name: Standarddrucker des Systems als Standarddrucker festlegen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Printing
  - GP Pfad (Empfohlen): Administrative Templates/Microsoft Edge – Standardeinstellungen (Benutzer können diese außer Kraft setzen)/Printing
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Wertname: PrintPreviewUseSystemDefaultPrinter
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000000
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: PrintPreviewUseSystemDefaultPrinter
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### PrintingEnabled

  #### Drucken aktivieren

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Aktiviert das Drucken in Microsoft Edge und hindert Benutzer daran, diese Einstellung zu ändern.

Wenn Sie diese Richtlinie aktivieren oder nicht konfigurieren, können Benutzer drucken.

Wenn Sie diese Richtlinie deaktivieren, können Benutzer nicht aus Microsoft Edge drucken. Das Drucken ist im Menü "Schraubenschlüssel", "Erweiterungen", "JavaScript-Anwendungen" usw. deaktiviert. Benutzer können weiterhin über Plug-Ins drucken, die Microsoft Edge beim Drucken umgehen. So gibt es beispielsweise bei bestimmten Adobe Flash-Anwendungen die Option Drucken im Kontextmenü, die von dieser Richtlinie nicht abgedeckt wird.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: PrintingEnabled
  - GP-Name: Drucken aktivieren
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Printing
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: PrintingEnabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: PrintingEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### PrintingPaperSizeDefault

  #### Standardmäßiges Seitenformat für den Druck

  
  
  #### Unterstützte Versionen:

  - Unter Windows und macOS ab 86 oder höher

  #### Beschreibung

  Außerkraftsetzung des standardmäßigen Seitenformats für den Druck.

Der Name sollte eines der aufgeführten Formate oder "Benutzerdefiniert" enthalten, wenn das erforderliche Papierformat nicht in der Liste enthalten ist. Wenn der Wert "Benutzerdefiniert" angegeben wird, sollte die Eigenschaft "custom_size" angegeben werden. Sie beschreibt die gewünschte Höhe und Breite in Mikrometer. Andernfalls sollte die "custom_size"-Eigenschaft nicht angegeben werden. Richtlinien, die diese Regeln verletzen, werden ignoriert.

Wenn das Seitenformat auf dem vom Benutzer ausgewählten Drucker nicht verfügbar ist, wird diese Richtlinie ignoriert.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Dictionary

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - Eindeutiger GP-Name: PrintingPaperSizeDefault
  - GP-Name: Standardmäßiges Seitenformat für den Druck
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Printing
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: PrintingPaperSizeDefault
  - Werttyp: REG_SZ

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\PrintingPaperSizeDefault = {
  "custom_size": {
    "height": 297000, 
    "width": 210000
  }, 
  "name": "custom"
}
```

  ##### Kompakter Beispielwert:

  ```
  SOFTWARE\Policies\Microsoft\Edge\PrintingPaperSizeDefault = {"custom_size": {"height": 297000, "width": 210000}, "name": "custom"}
  ```
  

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: PrintingPaperSizeDefault
  - Beispielwert:
``` xml
<key>PrintingPaperSizeDefault</key>
<dict>
  <key>custom_size</key>
  <dict>
    <key>height</key>
    <integer>297000</integer>
    <key>width</key>
    <integer>210000</integer>
  </dict>
  <key>name</key>
  <string>custom</string>
</dict>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### UseSystemPrintDialog

  #### Drucken über das System-Dialogfeld „Drucken“

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Zeigt das System-Dialogfeld "Drucken" anstelle der Seitenansicht.

Wenn Sie diese Richtlinie aktivieren, öffnet Microsoft Edge das System-Dialogfeld „Drucken“ anstatt der integrierten Seitenansicht, wenn ein Benutzer eine Seite druckt.

Wenn Sie diese Richtlinie nicht konfigurieren oder deaktivieren, wird mit den Druckbefehlen der Bildschirm "Microsoft Edge-Druckvorschau" aufgerufen.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: UseSystemPrintDialog
  - GP-Name: Drucken über das System-Dialogfeld „Drucken“
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Printing
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: UseSystemPrintDialog
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000000
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: UseSystemPrintDialog
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ## Proxyserver-Richtlinien

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### ProxyBypassList

  #### Proxy-Umgehungsregeln konfigurieren (veraltet)

  >VERALTET: Diese Richtlinie ist veraltet. Sie wird zurzeit unterstützt, aber in einer zukünftigen Version als veraltet behandelt.
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Diese Richtlinie ist veraltet. Verwenden Sie stattdessen [ProxySettings](#proxysettings). Funktioniert nicht in Microsoft Edge Version 91.

Gibt eine Liste von Hosts an, für die Microsoft Edge jeden Proxy umgeht.

Diese Richtlinie wird nur angewendet, wenn die Richtlinie für [ProxySettings](#proxysettings) nicht angegeben ist und Sie in der Richtlinie [ProxyMode](#proxymode) „fixed_servers“ ausgewählt haben. Wenn Sie irgend einen anderen Modus zum Konfigurieren von Proxy-Richtlinien ausgewählt haben, sollten Sie diese Richtlinie nicht aktivieren oder konfigurieren.

Wenn Sie diese Richtlinie aktivieren, können Sie eine Liste mit Hosts erstellen, für die Microsoft Edge keinen Proxy verwendet.

Wenn Sie diese Richtlinie nicht konfigurieren, wird keine Liste mit Hosts erstellt, für die Microsoft Edge einen Proxy umgeht. Lassen Sie diese Richtlinie unkonfiguriert, wenn Sie eine andere Methode zum Festlegen von Proxy-Richtlinien festgelegt haben.

Ausführlichere Beispiele finden Sie unter [https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936).

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Zeichenfolge

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: ProxyBypassList
  - GP-Name: Proxy-Umgehungsregeln konfigurieren (veraltet)
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Proxy server
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: ProxyBypassList
  - Werttyp: REG_SZ

  ##### Beispielwert:

```
"https://www.contoso.com, https://www.fabrikam.com"
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: ProxyBypassList
  - Beispielwert:
``` xml
<string>https://www.contoso.com, https://www.fabrikam.com</string>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### ProxyMode

  #### Proxyservereinstellungen konfigurieren (veraltet)

  >VERALTET: Diese Richtlinie ist veraltet. Sie wird zurzeit unterstützt, aber in einer zukünftigen Version als veraltet behandelt.
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Diese Richtlinie ist veraltet. Verwenden Sie stattdessen [ProxySettings](#proxysettings). Funktioniert nicht in Microsoft Edge Version 91.

Wenn Sie diese Richtlinie aktivieren, können Sie den von Microsoft Edge verwendeten Proxyserver angeben, und Benutzer können die Proxyeinstellungen nicht ändern. Microsoft Edge ignoriert alle Proxy-bezogenen Optionen, die über die Befehlszeile angegeben werden. Diese Richtlinie wird nur angewendet, wenn die Richtlinie für [ProxySettings](#proxysettings) nicht angegeben wurde.

Wenn Sie eine der folgenden Optionen auswählen, werden andere Optionen ignoriert:
  * direct = nie einen Proxy Server verwenden und immer eine direkte Verbindung herstellen
  * system = System-Proxyeinstellungen verwenden
  * auto_detect = Proxyserver automatisch bestimmen

Bei Auswahl folgender Optionen:
  * fixed_servers = festgelegte Proxyserver verwenden. Sie können weitere Optionen mit [Proxyserver](#proxyserver) und [ProxyBypassList](#proxybypasslist) angeben.
  * pac_script = .pac-Proxyskript verwenden. Verwenden Sie [ProxyPacUrl](#proxypacurl), um die URL zu einer Proxy-.pac-Datei anzugeben.

Ausführliche Beispiele finden Sie unter [https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936).

Wenn Sie diese Richtlinie nicht konfigurieren, können die Benutzer ihre eigenen Proxyeinstellungen auswählen.

Zuordnung von Richtlinienoptionen:

* ProxyDisabled (direct) = niemals einen Proxy verwenden

* ProxyAutoDetect (auto_detect) = automatisches Erkennen von Proxyeinstellungen

* ProxyPacScript (pac_script) = verwenden eines PAC-Proxyskripts

* ProxyFixedServers (fixed_servers) = verwenden von festen Proxyservern

* ProxyUseSystem (System) = System Proxyeinstellungen verwenden

Verwenden Sie die vorstehenden Informationen, wenn Sie diese Richtlinie konfigurieren.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Zeichenfolge

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - Eindeutiger Name der GP: ProxyMode
  - GP-Name: Proxyservereinstellungen konfigurieren (veraltet)
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Proxy server
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Name des Wertes: ProxyMode
  - Werttyp: REG_SZ

  ##### Beispielwert:

```
"direct"
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: ProxyMode
  - Beispielwert:
``` xml
<string>direct</string>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### ProxyPacUrl

  #### Proxy-.pac-Datei-URL festlegen (veraltet)

  >VERALTET: Diese Richtlinie ist veraltet. Sie wird zurzeit unterstützt, aber in einer zukünftigen Version als veraltet behandelt.
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Diese Richtlinie ist veraltet. Verwenden Sie stattdessen [ProxySettings](#proxysettings). Funktioniert nicht in Microsoft Edge Version 91.

Legt die URL für eine Proxy-Autokonfigurationsdatei (PAC-Datei) fest.

Diese Richtlinie wird nur angewendet, wenn die Richtlinie für [ProxySettings](#proxysettings) nicht angegeben ist und Sie in der Richtlinie [ProxyMode](#proxymode) „pac_script“ ausgewählt haben. Wenn Sie irgend einen anderen Modus zum Konfigurieren von Proxy-Richtlinien ausgewählt haben, sollten Sie diese Richtlinie nicht aktivieren oder konfigurieren.

Wenn Sie diese Richtlinie aktivieren, können Sie die URL für eine PAC-Datei angeben, die definiert, wie der Browser automatisch den richtigen Proxyserver auswählt, um eine bestimmte Website abzurufen.

Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, wird keine PAC-Datei angegeben. Lassen Sie diese Richtlinie unkonfiguriert, wenn Sie eine andere Methode zum Festlegen von Proxy-Richtlinien festgelegt haben.

Ausführliche Beispiele finden Sie unter [https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936).

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Zeichenfolge

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - Eindeutiger Name der GP: ProxyPacUrl
  - GP-Name: Proxy-.pac-Datei-URL festlegen (veraltet)
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Proxy server
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Name des Wertes: ProxyPacUrl
  - Werttyp: REG_SZ

  ##### Beispielwert:

```
"https://internal.contoso.com/example.pac"
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: ProxyPacUrl
  - Beispielwert:
``` xml
<string>https://internal.contoso.com/example.pac</string>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### ProxyServer

  #### Adresse oder URL von Proxyservern konfigurieren (veraltet)

  >VERALTET: Diese Richtlinie ist veraltet. Sie wird zurzeit unterstützt, aber in einer zukünftigen Version als veraltet behandelt.
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Diese Richtlinie ist veraltet. Verwenden Sie stattdessen [ProxySettings](#proxysettings). Funktioniert nicht in Microsoft Edge Version 91.

Gibt die URL des Proxyservers an.

Diese Richtlinie wird nur angewendet, wenn die Richtlinie für [ProxySettings](#proxysettings) nicht angegeben ist und Sie in der Richtlinie [ProxyMode](#proxymode) „fixed_servers“ ausgewählt haben. Wenn Sie irgend einen anderen Modus zum Konfigurieren von Proxy-Richtlinien ausgewählt haben, sollten Sie diese Richtlinie nicht aktivieren oder konfigurieren.

Wenn Sie diese Richtlinie aktivieren, wird der durch diese Richtlinie konfigurierte Proxy Server für alle URLs verwendet.

Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, können die Benutzer ihre eigenen Proxyeinstellungen auswählen, während sie sich in diesem Proxymodus befinden. Lassen Sie diese Richtlinie unkonfiguriert, wenn Sie eine andere Methode zum Festlegen von Proxy-Richtlinien festgelegt haben.

Weitere Optionen und detaillierte Beispiele finden Sie unter [https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936).

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Zeichenfolge

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - Eindeutiger Name der GP: ProxyServer
  - GP-Name: Adresse oder URL von Proxyservern konfigurieren (veraltet)
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Proxy server
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Name des Wertes: ProxyServer
  - Werttyp: REG_SZ

  ##### Beispielwert:

```
"123.123.123.123:8080"
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: ProxyServer
  - Beispielwert:
``` xml
<string>123.123.123.123:8080</string>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### ProxySettings

  #### Proxyeinstellungen

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Konfiguriert die Proxyeinstellungen für Microsoft Edge.

Wenn Sie diese Richtlinie aktivieren, ignoriert Microsoft Edge alle Proxy-bezogenen Optionen, die von der Befehlszeile aus angegeben wurden.

Wenn Sie diese Richtlinie nicht konfigurieren, können die Benutzer ihre eigenen Proxyeinstellungen auswählen.

Mit dieser Richtlinie werden die folgenden einzelnen Richtlinien außer Kraft gesetzt:

[ProxyMode](#proxymode)
[ProxyPacUrl](#proxypacurl)
[ProxyServer](#proxyserver)
[ProxyBypassList](#proxybypasslist)

Beim Festlegen der [ProxySettings](#proxysettings)-Richtlinie sind die folgenden Felder zulässig:
  * „ProxyMode“, über das Sie den von Microsoft Edge verwendeten Proxyserver angeben können. Dies verhindert, dass Benutzer Proxyeinstellungen ändern.
  * „ProxyPacUrl“, eine URL zu einer Proxy-.pac-Datei
  * „ProxyServer“, eine URL für den Proxy Server
  * „ProxyBypassList“, eine Liste von Proxy-Hosts, die von Microsoft Edge umgangen werden

Bei Auswahl der folgenden Werte für „ProxyMode“:
  * direct: Es wird kein Proxy verwendet, und alle anderen Felder werden ignoriert.
  * system: Es wird der Proxy des Systems verwendet, und alle anderen Felder werden ignoriert.
  * auto_detect: Alle anderen Felder werden ignoriert.
  * fixed_server: Es werden die Felder "Proxyserver" und "ProxyBypassList" verwendet.
  * pac_script: Es werden die Felder "ProxyPacUrl" und "ProxyBypassList" verwendet.

Ausführlichere Beispiele finden Sie unter [https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936).

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Dictionary

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: ProxySettings
  - GP-Name: Konfigurieren von Proxyeinstellungen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Proxy server
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: ProxySettings
  - Werttyp: REG_SZ

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\ProxySettings = {
  "ProxyBypassList": "https://www.example1.com,https://www.example2.com,https://internalsite/", 
  "ProxyMode": "direct", 
  "ProxyPacUrl": "https://internal.site/example.pac", 
  "ProxyServer": "123.123.123.123:8080"
}
```

  ##### Kompakter Beispielwert:

  ```
  SOFTWARE\Policies\Microsoft\Edge\ProxySettings = {"ProxyBypassList": "https://www.example1.com,https://www.example2.com,https://internalsite/", "ProxyMode": "direct", "ProxyPacUrl": "https://internal.site/example.pac", "ProxyServer": "123.123.123.123:8080"}
  ```
  

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: ProxySettings
  - Beispielwert:
``` xml
<key>ProxySettings</key>
<dict>
  <key>ProxyBypassList</key>
  <string>https://www.example1.com,https://www.example2.com,https://internalsite/</string>
  <key>ProxyMode</key>
  <string>direct</string>
  <key>ProxyPacUrl</key>
  <string>https://internal.site/example.pac</string>
  <key>ProxyServer</key>
  <string>123.123.123.123:8080</string>
</dict>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ## SmartScreen-Einstellungs-Richtlinien

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### PreventSmartScreenPromptOverride

  #### Umgehung der Microsoft Defender SmartScreen-Aufforderungen für Websites verhindern

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Mit dieser Richtlinieneinstellung können Sie festlegen, ob Benutzer die Microsoft Defender SmartScreen-Warnungen zu möglicherweise schädlichen Websites übergehen dürfen.

Wenn Sie diese Einstellung aktivieren, können Benutzer Microsoft Defender SmartScreen-Warnungen nicht ignorieren, und sie werden am Aufrufen der Website gehindert.

Wenn Sie diese Einstellung deaktivieren oder nicht konfigurieren, können Benutzer Microsoft Defender SmartScreen-Warnungen ignorieren und die Website aufrufen.

Diese Richtlinie ist nur für Windows-Instanzen verfügbar, die mit einer Microsoft Active Directory-Domäne verknüpft sind, Windows 10 Pro- oder Enterprise-Instanzen, die für die Geräteverwaltung registriert sind, oder MacOS-Instanzen, die über MDM verwaltet oder über MCX einer Domäne beigetreten sind.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: PreventSmartScreenPromptOverride
  - GP-Name: Umgehung der Microsoft Defender SmartScreen-Aufforderungen für Websites verhindern
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/SmartScreen settings
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: PreventSmartScreenPromptOverride
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: PreventSmartScreenPromptOverride
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### PreventSmartScreenPromptOverrideForFiles

  #### Verhindern der Umgehung von Microsoft Defender-SmartScreen-Warnungen zu Downloads

  
  
  #### Unterstützte Versionen:

  - Auf Windows ab 77 oder höher
  - Auf macOS ab 79 oder höher

  #### Beschreibung

  Mit dieser Richtlinie können Sie ermitteln, ob Benutzer die SmartScreen-Warnungen von Microsoft Defender über nicht überprüfte Downloads außer Kraft setzen können.

Wenn Sie diese Richtlinie aktivieren, können die Benutzer in Ihrer Organisation die Microsoft Defender-SmartScreen-Warnungen nicht ignorieren und sie werden daran gehindert, die nicht überprüften Downloads abzuschließen.

Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, können Benutzer Microsoft Defender-SmartScreen-Warnungen ignorieren und nicht überprüfte Downloads abschließen.

Diese Richtlinie ist nur für Windows-Instanzen verfügbar, die mit einer Microsoft Active Directory-Domäne verknüpft sind, Windows 10 Pro- oder Enterprise-Instanzen, die für die Geräteverwaltung registriert sind, oder MacOS-Instanzen, die über MDM verwaltet oder über MCX einer Domäne beigetreten sind.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: PreventSmartScreenPromptOverrideForFiles
  - GP-Name: Verhindern der Umgehung von Microsoft Defender-SmartScreen-Warnungen zu Downloads
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/SmartScreen settings
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: PreventSmartScreenPromptOverrideForFiles
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: PreventSmartScreenPromptOverrideForFiles
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### SmartScreenAllowListDomains

  #### Konfigurieren der Liste der Domänen, für die Microsoft Defender-SmartScreen keine Warnungen auslöst

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Konfigurieren der Liste der für Microsoft Defender SmartScreen vertrauenswürdigen Domänen. Dies bedeutet: Microsoft Defender SmartScreen überprüft nicht auf potenziell bösartige Ressourcen wie Phishingsoftware und andere Malware, wenn die Quell-URLs einer hier aufgeführten Domäne entspricht.
Der Microsoft Defender SmartScreen-Download Schutzdienst überprüft die auf diesen Domänen gehosteten Downloads nicht.

Wenn Sie diese Richtlinie aktivieren, vertraut Microsoft Defender SmartScreen diesen Domänen.
Wenn Sie diese Richtlinie deaktivieren oder nicht festlegen, wird der standardmäßige Microsoft Defender-SmartScreen-Schutz auf alle Ressourcen angewendet.

Diese Richtlinie ist nur für Windows-Instanzen verfügbar, die mit einer Microsoft Active Directory-Domäne verknüpft sind, Windows 10 Pro- oder Enterprise-Instanzen, die für die Geräteverwaltung registriert sind, oder MacOS-Instanzen, die über MDM verwaltet oder über MCX einer Domäne beigetreten sind.
Beachten Sie auch, dass diese Richtlinie nicht zutrifft, wenn Ihre Organisation Microsoft Defender Advanced Threat Protection aktiviert hat. Sie müssen stattdessen Ihre Zulassungs- und Sperrlisten im Microsoft Defender Security Center konfigurieren.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Liste von Zeichenfolgen

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: SmartScreenAllowListDomains
  - GP-Name: Konfigurieren der Liste der Domänen, für die Microsoft Defender-SmartScreen keine Warnungen auslöst
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/SmartScreen settings
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge\SmartScreenAllowListDomains
  - Pfad (Empfohlen): n.a.
  - Wertname: 1, 2, 3, ...
  - Werttyp: REG_SZ-Liste

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\SmartScreenAllowListDomains\1 = "mydomain.com"
SOFTWARE\Policies\Microsoft\Edge\SmartScreenAllowListDomains\2 = "myuniversity.edu"

```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: SmartScreenAllowListDomains
  - Beispielwert:
``` xml
<array>
  <string>mydomain.com</string>
  <string>myuniversity.edu</string>
</array>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### SmartScreenEnabled

  #### Konfigurieren des Microsoft Defender SmartScreen

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Mit dieser Richtlinieneinstellung können Sie konfigurieren, ob Microsoft Defender SmartScreen aktiviert werden soll. Microsoft Defender SmartScreen sendet Warnmeldungen, um zum Schutz Ihrer Benutzer vor potenziellen Betrugsversuchen durch Phishing oder Schadsoftware beizutragen. Microsoft Defender SmartScreen ist standardmäßig aktiviert.

Wenn Sie diese Einstellung aktivieren, wird Microsoft Defender SmartScreen aktiviert.

Wenn Sie diese Einstellung deaktivieren, ist Microsoft Defender SmartScreen deaktiviert.

Wenn Sie diese Einstellung nicht konfigurieren, können Benutzer entscheiden, ob sie Microsoft Defender SmartScreen verwenden möchten.

Diese Richtlinie ist nur für Windows-Instanzen verfügbar, die mit einer Microsoft Active Directory-Domäne verknüpft sind, Windows 10 Pro- oder Enterprise-Instanzen, die für die Geräteverwaltung registriert sind, oder MacOS-Instanzen, die über MDM verwaltet oder über MCX einer Domäne beigetreten sind.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: SmartScreenEnabled
  - GP-Name: Konfigurieren des Microsoft Defender SmartScreen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/SmartScreen settings
  - GP Pfad (Empfohlen): Administrative Templates/Microsoft Edge – Standardeinstellungen (Benutzer können diese außer Kraft setzen)/SmartScreen settings
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Wertname: SmartScreenEnabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: SmartScreenEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### SmartScreenForTrustedDownloadsEnabled

  #### Erzwingen der Microsoft Defender-SmartScreen-Überprüfung für Downloads aus vertrauenswürdigen Quellen

  
  
  #### Unterstützte Versionen:

  - Auf Windows ab 78 oder höher

  #### Beschreibung

  Diese Richtlinieneinstellung ermöglicht es Ihnen, zu konfigurieren, ob Microsoft Defender-SmartScreen den Ruf des Downloads mittels einer vertrauenswürdigen Quelle überprüft.

Wenn Sie diese Einstellung aktivieren oder nicht konfigurieren, überprüft Microsoft Defender SmartScreen den Ruf des Downloads unabhängig von der Quelle.

Wenn Sie diese Einstellung deaktivieren, überprüft Microsoft Defender SmartScreen beim Herunterladen aus einer vertrauenswürdigen Quelle den Ruf des Downloads nicht.

Diese Richtlinie gilt nur für Windows-Instanzen, die mit einer Microsoft Active Directory-Domäne verknüpft sind, Windows 10 Pro- oder Enterprise-Instanzen, die für die Geräteverwaltung registriert sind.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: SmartScreenForTrustedDownloadsEnabled
  - GP-Name: Erzwingen der Microsoft Defender-SmartScreen-Überprüfung für Downloads aus vertrauenswürdigen Quellen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/SmartScreen settings
  - GP Pfad (Empfohlen): Administrative Templates/Microsoft Edge – Standardeinstellungen (Benutzer können diese außer Kraft setzen)/SmartScreen settings
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Wertname: SmartScreenForTrustedDownloadsEnabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000000
```

  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### SmartScreenPuaEnabled

  #### Konfigurieren von Microsoft Defender SmartScreen, sodass potenziell unerwünschte Apps blockiert werden

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 80 oder höher

  #### Beschreibung

  Mit dieser Richtlinieneinstellung können Sie konfigurieren, ob die Blockierung potenziell unerwünschter Apps mit Microsoft Defender SmartScreen aktiviert werden soll. Die Funktion zum Blockieren potenziell unerwünschter Apps mit Microsoft Defender SmartScreen bietet Warnmeldungen, die beim Schutz von Benutzern vor Adware, Coin Minern, Bundleware und anderen Apps mit schlechtem Ruf helfen, die von Websites gehostet werden. Die Funktion zum Blockieren potenziell unerwünschter Apps mit Microsoft Defender SmartScreen ist standardmäßig deaktiviert.

Wenn Sie diese Einstellung aktivieren, wird die Funktion zum Blockieren potenziell unerwünschter Apps mit Microsoft Defender SmartScreen aktiviert.

Wenn Sie diese Einstellung deaktivieren, wird die Funktion zum Blockieren potenziell unerwünschter Apps mit Microsoft Defender SmartScreen deaktiviert.

Wenn Sie diese Einstellung nicht konfigurieren, können Benutzer entscheiden, ob sie die Funktion zum Blockieren potenziell unerwünschter Apps mit Microsoft Defender SmartScreen verwenden möchten.

Diese Richtlinie ist nur für Windows-Instanzen verfügbar, die mit einer Microsoft Active Directory-Domäne verknüpft sind, Windows 10 Pro- oder Enterprise-Instanzen, die für die Geräteverwaltung registriert sind, oder MacOS-Instanzen, die über MDM verwaltet oder über MCX einer Domäne beigetreten sind.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: SmartScreenPuaEnabled
  - GP-Name: Konfigurieren von Microsoft Defender SmartScreen, sodass potenziell unerwünschte Apps blockiert werden
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/SmartScreen settings
  - GP Pfad (Empfohlen): Administrative Templates/Microsoft Edge – Standardeinstellungen (Benutzer können diese außer Kraft setzen)/SmartScreen settings
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Wertname: SmartScreenPuaEnabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: SmartScreenPuaEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ## Richtlinien für Start&comma; Homepage und neue Registerkarten

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### HomepageIsNewTabPage

  #### Festlegen einer neuen Registerkarte als Startseite

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Konfiguriert die Standardstartseite in Microsoft Edge. Sie können die Startseite auf eine URL festlegen, die Sie angeben, oder auf eine neue Registerkartenseite.

Wenn Sie diese Richtlinie aktivieren, wird die neue Registerkartenseite immer als Homepage verwendet, und der Speicherort der Homepage wird ignoriert.

Wenn Sie diese Richtlinie deaktivieren, kann die Startseite des Benutzers nicht die neue Registerkartenseite sein, es sei denn, die URL ist auf "edge://newtab" festgelegt.

Wenn nicht konfiguriert, können Benutzer wählen, ob es sich bei der neuen Registerkartenseite um ihre Startseite handelt.

Diese Richtlinie ist nur für Windows-Instanzen verfügbar, die mit einer Microsoft Active Directory-Domäne verknüpft sind, Windows 10 Pro- oder Enterprise-Instanzen, die für die Geräteverwaltung registriert sind, oder MacOS-Instanzen, die über MDM verwaltet oder über MCX einer Domäne beigetreten sind.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: HomepageIsNewTabPage
  - GP-Name: Festlegen einer neuen Registerkarte als Startseite
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Startup, home page and new tab page
  - GP Pfad (Empfohlen): Administrative Templates/Microsoft Edge – Standardeinstellungen (Benutzer können diese außer Kraft setzen)/Startup, home page and new tab page
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Wertname: HomepageIsNewTabPage
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: HomepageIsNewTabPage
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### HomepageLocation

  #### Konfigurieren der Startseiten-URL

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Konfiguriert die Standardstartseiten-URL in Microsoft Edge.

Die Startseite ist die Seite, die von der Schaltfläche "Start" geöffnet wird. Die beim Start geöffneten Seiten werden von den Richtlinien [RestoreOnStartup](#restoreonstartup) gesteuert.

Sie können hier entweder eine URL festlegen oder festlegen, dass die Startseite die neue Registerkartenseite öffnet. Wenn Sie auswählen, dass die neue Registerkartenseite geöffnet werden soll, wird diese Richtlinie nicht wirksam.

Wenn Sie diese Richtlinie aktivieren, können die Benutzer ihre Startseiten-URL zwar nicht ändern, aber sie können die neue Registerkartenseite als Startseite verwenden.

Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, können Benutzer eine eigene Startseite auswählen, sofern die [HomepageIsNewTabPage](#homepageisnewtabpage) Richtlinie nicht aktiviert ist.

Diese Richtlinie ist nur für Windows-Instanzen verfügbar, die mit einer Microsoft Active Directory-Domäne verknüpft sind, Windows 10 Pro- oder Enterprise-Instanzen, die für die Geräteverwaltung registriert sind, oder MacOS-Instanzen, die über MDM verwaltet oder über MCX einer Domäne beigetreten sind.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Zeichenfolge

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: HomepageLocation
  - GP-Name: Konfigurieren der Startseiten-URL
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Startup, home page and new tab page
  - GP Pfad (Empfohlen): Administrative Templates/Microsoft Edge – Standardeinstellungen (Benutzer können diese außer Kraft setzen)/Startup, home page and new tab page
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Wertname: HomepageLocation
  - Werttyp: REG_SZ

  ##### Beispielwert:

```
"https://www.contoso.com"
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: HomepageLocation
  - Beispielwert:
``` xml
<string>https://www.contoso.com</string>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### NewTabPageAllowedBackgroundTypes

  #### Konfigurieren der für das neue Registerkartenseiten-Layout zulässigen Hintergrundtypen

  
  
  #### Unterstützte Versionen:

  - Unter Windows und macOS ab 86 oder höher

  #### Beschreibung

  Sie können festlegen, welche Arten von Hintergrundbildern im neuen Registerkartenseiten-Layout in Microsoft Edge zulässig sind.

Wenn Sie diese Richtlinie nicht konfigurieren, werden alle Hintergrundbildtypen auf der neuen Registerkarte aktiviert.

Zuordnung von Richtlinienoptionen:

* DisableImageOfTheDay (1) = Deaktivieren des täglichen Hintergrundbildtyps

* DisableCustomImage (2) = Deaktivieren des benutzerdefinierten täglichen Hintergrundbildtyps

* DisableAll (3) = Deaktivieren aller Hintergrundbildtypen

Verwenden Sie die vorstehenden Informationen, wenn Sie diese Richtlinie konfigurieren.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Ganze Zahl

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - Eindeutiger GP-Name: NewTabPageAllowedBackgroundTypes
  - GP-Name: Konfigurieren der zulässigen Hintergrundtypen für das neue Registerkartenseiten-Layout
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Startup, home page and new tab page
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: NewTabPageAllowedBackgroundTypes
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000002
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: NewTabPageAllowedBackgroundTypes
  - Beispielwert:
``` xml
<integer>2</integer>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### NewTabPageCompanyLogo

  #### Firmenlogo für „Neuer Tab“-Seite festlegen (veraltet)

  
  >VERALTET: Diese Richtlinie ist veraltet und funktioniert nach Microsoft Edge 85 nicht mehr.
  #### Unterstützte Versionen:

  - Unter Windows und macOS ab 79 bis 85

  #### Beschreibung

  Diese Richtlinie hat aufgrund veränderter betrieblicher Anforderungen nicht erwartungsgemäß funktioniert. Deshalb ist sie veraltet und sollte nicht verwendet werden.

Gibt das Firmenlogo an, das auf der neuen Registerkartenseite in Microsoft Edge verwendet werden soll.

Die Richtlinie sollte als Zeichenfolge konfiguriert werden, die das Logo/die Logos im JSON-Format ausdrückt. Beispiel: { "default_logo": { "url": "https://www.contoso.com/logo.png", "hash": "cd0aa9856147b6c5b4ff2b7dfee5da20aa38253099ef1b4a64aced233c9afe29" }, "light_logo": { "url": "https://www.contoso.com/light_logo.png", "Hash": "517d286edb416bb2625ccfcba9de78296e90da8e32330d4c9c8275c4c1c33737" } }

Sie konfigurieren diese Richtlinie, indem Sie die URL angeben, aus der Microsoft Edge das Logo und dessen Kryptografie-Hash (SHA-256) herunterladen kann, mit dem die Integrität des Downloads überprüft wird. Das Logo muss im PNG- oder SVG-Format vorliegen, und die Dateigröße darf 16 MB nicht überschreiten. Das Logo wird heruntergeladen und zwischengespeichert, und es wird immer dann erneut heruntergeladen, wenn sich die URL oder der Hashwert ändert. Die URL muss ohne Authentifizierung erreichbar sein.

Das "default_logo" ist erforderlich und wird verwendet, wenn kein Hintergrundbild verfügbar ist. Wenn "light_logo" angeboten wird, wird dies verwendet, wenn die neue Registerkartenseite des Benutzers ein Hintergrundbild aufweist. Wir empfehlen ein horizontales Logo mit einem transparenten Hintergrund, das linksbündig und vertikal mittig ausgerichtet ist. Das Logo sollte eine Mindesthöhe von 32 Pixeln und ein Seitenverhältnis von 1:1 bis 4:1 aufweisen. Das "default_logo" sollte einen guten Kontrast gegen einen weißen/schwarzen Hintergrund aufweisen, während das "light_logo" einen guten Kontrast zu einem Hintergrundbild aufweisen sollte.

Wenn Sie diese Richtlinie aktivieren, downloadet Microsoft Edge das angegebene Logo bzw. die Logos und zeigt sie auf der neuen Registerkartenseite. Benutzer können die Logos nicht umgehen oder ausblenden.

Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, zeigt Microsoft Edge auf der neuen Registerkartenseite kein Firmenlogo oder ein Microsoft-Logo an.

Hilfe zur Ermittlung des SHA-256-Hashs finden Sie unter https://docs.microsoft.com/powershell/module/microsoft.powershell.utility/get-filehash.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Dictionary

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: NewTabPageCompanyLogo
  - GP-Name: Firmenlogo für „Neuer Tab“-Seite festlegen (veraltet)
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Startup, home page and new tab page
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: NewTabPageCompanyLogo
  - Werttyp: REG_SZ

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\NewTabPageCompanyLogo = {
  "default_logo": {
    "hash": "cd0aa9856147b6c5b4ff2b7dfee5da20aa38253099ef1b4a64aced233c9afe29", 
    "url": "https://www.contoso.com/logo.png"
  }, 
  "light_logo": {
    "hash": "517d286edb416bb2625ccfcba9de78296e90da8e32330d4c9c8275c4c1c33737", 
    "url": "https://www.contoso.com/light_logo.png"
  }
}
```

  ##### Kompakter Beispielwert:

  ```
  SOFTWARE\Policies\Microsoft\Edge\NewTabPageCompanyLogo = {"default_logo": {"hash": "cd0aa9856147b6c5b4ff2b7dfee5da20aa38253099ef1b4a64aced233c9afe29", "url": "https://www.contoso.com/logo.png"}, "light_logo": {"hash": "517d286edb416bb2625ccfcba9de78296e90da8e32330d4c9c8275c4c1c33737", "url": "https://www.contoso.com/light_logo.png"}}
  ```
  

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: NewTabPageCompanyLogo
  - Beispielwert:
``` xml
<key>NewTabPageCompanyLogo</key>
<dict>
  <key>default_logo</key>
  <dict>
    <key>hash</key>
    <string>cd0aa9856147b6c5b4ff2b7dfee5da20aa38253099ef1b4a64aced233c9afe29</string>
    <key>url</key>
    <string>https://www.contoso.com/logo.png</string>
  </dict>
  <key>light_logo</key>
  <dict>
    <key>hash</key>
    <string>517d286edb416bb2625ccfcba9de78296e90da8e32330d4c9c8275c4c1c33737</string>
    <key>url</key>
    <string>https://www.contoso.com/light_logo.png</string>
  </dict>
</dict>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### NewTabPageHideDefaultTopSites

  #### Ausblenden der standardmäßigen Top-Websites auf der neuen Registerkartenseite

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Ausblenden der standardmäßigen Top-Websites auf der neuen Registerkartenseite in Microsoft Edge.

Wenn Sie diese Richtlinie auf "wahr" festlegen, werden die Kacheln der standardmäßigen Top-Websites ausgeblendet.

Wenn Sie diese Richtlinie auf "falsch" festlegen oder sie nicht konfigurieren, bleiben die Kacheln für die standardmäßigen Top-Websites sichtbar.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: NewTabPageHideDefaultTopSites
  - GP-Name: Ausblenden der standardmäßigen Top-Websites auf der neuen Registerkartenseite
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Startup, home page and new tab page
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: NewTabPageHideDefaultTopSites
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: NewTabPageHideDefaultTopSites
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### NewTabPageLocation

  #### Konfigurieren der URL der neuen Registerkartenseite

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Konfiguriert die Standard-URL für die neue Registerkartenseite.

Diese Richtlinie bestimmt die Seite, die beim Erstellen neuer Registerkarten (einschließlich beim Öffnen neuer Fenster) geöffnet wird. Er wirkt sich auch auf die Startseite aus, wenn diese auf die neue Registerkartenseite festgelegt ist.

Diese Richtlinie bestimmt nicht, welche Seite beim Start geöffnet wird. Dies wird durch die Richtlinie [RestoreOnStartup](#restoreonstartup) gesteuert. Es wirkt sich auch nicht auf die Startseite aus, wenn diese auf die neue Registerkartenseite festgelegt ist.

Wenn Sie diese Richtlinie nicht konfigurieren, wird die standardmäßige neue Registerkartenseite verwendet.

Wenn Sie diese Richtlinie *und* die Richtlinie [NewTabPageSetFeedType](#newtabpagesetfeedtype) konfigurieren, hat diese Richtlinie Vorrang.

Wenn eine ungültige URL bereitgestellt wird, werden neue Registerkarten about://blank öffnen.

Diese Richtlinie ist nur für Windows-Instanzen verfügbar, die mit einer Microsoft Active Directory-Domäne verknüpft sind, Windows 10 Pro- oder Enterprise-Instanzen, die für die Geräteverwaltung registriert sind, oder MacOS-Instanzen, die über MDM verwaltet oder über MCX einer Domäne beigetreten sind.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Zeichenfolge

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: NewTabPageLocation
  - GP-Name: Konfigurieren der URL der neuen Registerkartenseite
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Startup, home page and new tab page
  - GP Pfad (Empfohlen): Administrative Templates/Microsoft Edge – Standardeinstellungen (Benutzer können diese außer Kraft setzen)/Startup, home page and new tab page
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Wertname: NewTabPageLocation
  - Werttyp: REG_SZ

  ##### Beispielwert:

```
"https://www.fabrikam.com"
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: NewTabPageLocation
  - Beispielwert:
``` xml
<string>https://www.fabrikam.com</string>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### NewTabPageManagedQuickLinks

  #### Festlegen der Quicklinks auf der neuen Registerkartenseite

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 79 oder höher

  #### Beschreibung

  Standardmäßig zeigt Microsoft Edge Quicklinks auf der neuen Registerkartenseite, die aus vom Benutzer hinzugefügten Verknüpfungen und Top-Websites aus dem Browserverlauf bestehen. Mit dieser Richtlinie können Sie bis zu drei Kacheln auf der neuen Registerkartenseite konfigurieren, die als JSON-Objekt ausgedrückt werden:

[ { "url": "https://www.contoso.com", "title": "Contoso Portal", "pinned": true/false }, ... ]

Das Feld "url" ist erforderlich. "title" und "pinned" sind optional. Wenn "title" nicht angegeben ist, wird die URL als Standardtitel verwendet. Wenn "pinned" nicht angegeben ist, lautet der Standardwert falsch.

Microsoft Edge zeigt diese in der genannten Reihenfolge, von links nach rechts, an, wobei alle angepinnten Kacheln vor nicht-angepinnten Kacheln angezeigt werden.

Wenn die Richtlinie als verpflichtend festgelegt ist, wird das Feld "pinned" ignoriert, und alle Kacheln werden angeheftet. Die Kacheln können nicht vom Benutzer gelöscht werden und werden immer am Anfang der Liste der Quicklinks angezeigt.

Wenn die Richtlinie wie empfohlen festgelegt ist, bleiben angeheftete Kacheln in der Liste, aber der Benutzer kann sie bearbeiten und löschen. Quicklink-Kacheln, die nicht angepinnt sind, verhalten sich wie standardmäßige Top-Websites und werden in der Liste nicht mehr angezeigt, wenn andere Websites häufiger besucht werden. Wenn nicht angepinnte Links über diese Richtlinie auf ein vorhandenes Browserprofil angewendet werden, werden die Links möglicherweise überhaupt nicht angezeigt, je nachdem, wie häufig sie im Vergleich zum Browserverlauf des Benutzers besucht wurden.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Dictionary

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: NewTabPageManagedQuickLinks
  - GP-Name: Festlegen der Quicklinks auf der neuen Registerkartenseite
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Startup, home page and new tab page
  - GP Pfad (Empfohlen): Administrative Templates/Microsoft Edge – Standardeinstellungen (Benutzer können diese außer Kraft setzen)/Startup, home page and new tab page
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Wertname: NewTabPageManagedQuickLinks
  - Werttyp: REG_SZ

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\NewTabPageManagedQuickLinks = [
  {
    "pinned": true, 
    "title": "Contoso Portal", 
    "url": "https://contoso.com"
  }, 
  {
    "title": "Fabrikam", 
    "url": "https://fabrikam.com"
  }
]
```

  ##### Kompakter Beispielwert:

  ```
  SOFTWARE\Policies\Microsoft\Edge\NewTabPageManagedQuickLinks = [{"pinned": true, "title": "Contoso Portal", "url": "https://contoso.com"}, {"title": "Fabrikam", "url": "https://fabrikam.com"}]
  ```
  

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: NewTabPageManagedQuickLinks
  - Beispielwert:
``` xml
<key>NewTabPageManagedQuickLinks</key>
<array>
  <dict>
    <key>pinned</key>
    <true/>
    <key>title</key>
    <string>Contoso Portal</string>
    <key>url</key>
    <string>https://contoso.com</string>
  </dict>
  <dict>
    <key>title</key>
    <string>Fabrikam</string>
    <key>url</key>
    <string>https://fabrikam.com</string>
  </dict>
</array>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### NewTabPagePrerenderEnabled

  #### Aktivieren des Vorabladens der neuen Registerkarte für schnellere Darstellung

  
  
  #### Unterstützte Versionen:

  - Auf Windows und MacOS ab 85 oder später

  #### Beschreibung

  Wenn Sie diese Richtlinie konfigurieren, ist das Vorladen der neuen Registerkarte aktiviert, und die Benutzer können diese Einstellung nicht ändern. Wenn Sie diese Richtlinie nicht konfigurieren, ist das Vorladen aktiviert, und ein Benutzer kann diese Einstellung ändern.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - Eindeutiger Name des GP: NewTabPagePrerenderEnabled
  - GP-Name: Aktivieren des Vorabladens der neuen Registerkarte für schnellere Darstellung
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Startup, home page and new tab page
  - GP Pfad (Empfohlen): Administrative Templates/Microsoft Edge – Standardeinstellungen (Benutzer können diese außer Kraft setzen)/Startup, home page and new tab page
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Wertname: NewTabPagePrerenderEnabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Name des Einstellungsschlüssels: NewTabPagePrerenderEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### NewTabPageSetFeedType

  #### Konfigurieren der neuen Registerkartenoberfläche für Microsoft Edge (veraltet)

  >VERALTET: Diese Richtlinie ist veraltet. Sie wird zurzeit unterstützt, aber in einer zukünftigen Version als veraltet behandelt.
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 79 oder höher

  #### Beschreibung

  Diese Richtlinie wird nicht mehr unterstützt, da die neue Version der Registerkartenseite „Unternehmen“ die Auswahl zwischen verschiedenen Inhaltstypen nicht mehr erfordert. Stattdessen können die dem Benutzer angezeigten Inhalte über das Microsoft 365 Admin Center gesteuert werden. Um zum Microsoft 365 Admin Center zu gelangen, melden Sie sich bei https://admin.microsoft.com mit Ihrem Administratorkonto an. Diese Richtlinie wird nach der Microsoft Edge-Version 90 inaktiv gesetzt.

Ermöglicht es Ihnen, entweder die Microsoft News oder den Office 365-Feed für die neue Registerkartenseite auszuwählen.

Wenn Sie diese Richtlinie auf „Microsoft News“ setzen, wird den Benutzern auf der neuen Registerkartenseite der "Microsoft-Newsfeeds" angezeigt.

Wenn Sie diese Richtlinie auf „Office“ setzen, wird den Benutzern mit einer Azure Active Directory-Browser-Anmeldung auf der neuen Registerkartenseite das Office 365-Feed angezeigt.

Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren:

- Benutzern mit einer Azure Active Directory-Browser-Anmeldung wird auf der neuen Registerkartenseite der "Office 365-Feed" sowie die neue standardmäßige Feed-Umgebung angeboten.

- Benutzer ohne Azure Active Directory-Browser-Anmeldung sehen die standardmäßige Oberfläche der neuen Registerkartenseite.

Wenn Sie diese Richtlinie *und* die Richtlinie [NewTabPageLocation](#newtabpagelocation) konfigurieren, hat die [NewTabPageLocation](#newtabpagelocation) Richtlinie Vorrang.

Standardeinstellung: Deaktiviert oder nicht konfiguriert.

Zuordnung von Richtlinienoptionen:

* Microsoft News (0) = Microsoft-Newsfeed

* Office (1) = Office 365-Feed

Verwenden Sie die vorstehenden Informationen, wenn Sie diese Richtlinie konfigurieren.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Ganze Zahl

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: NewTabPageSetFeedType
  - GP-Name: Konfigurieren der neuen Registerkartenoberfläche für Microsoft Edge
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Startup, home page and new tab page
  - GP Pfad (Empfohlen): Administrative Templates/Microsoft Edge – Standardeinstellungen (Benutzer können diese außer Kraft setzen)/Startup, home page and new tab page
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Wertname: NewTabPageSetFeedType
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000000
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: NewTabPageSetFeedType
  - Beispielwert:
``` xml
<integer>0</integer>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### RestoreOnStartup

  #### Auszuführende Aktion beim Start

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Legen Sie fest, wie sich Microsoft Edge beim Start verhält.

Wenn Sie möchten, dass beim Start immer eine neue Registerkarte geöffnet wird, wählen Sie „RestoreOnStartupIsNewTabPage“ aus.

Wenn Sie URLs wieder öffnen möchten, die beim letzten Schließen von Microsoft Edge geöffnet waren, wählen Sie „RestoreOnStartupIsLastSession“ aus. Die Browsersitzung wird unverändert wiederhergestellt. Beachten Sie, dass mit dieser Option einige Einstellungen deaktiviert werden, die auf Sitzungen angewiesen sind oder beim Beenden Aktionen ausführen (z.B. Löschen des Browserverlaufs beim Beenden oder nur-sitzungsbasierte Cookies).

Wenn Sie eine bestimmte Gruppe von URLs öffnen möchten, wählen Sie „RestoreOnStartupIsURLs“ aus.

Diese Einstellung zu deaktivieren hat den gleichen Effekt wie sie nicht zu konfigurieren. Benutzer können sie in Microsoft Edge ändern.

Diese Richtlinie ist nur für Windows-Instanzen verfügbar, die mit einer Microsoft Active Directory-Domäne verknüpft sind, Windows 10 Pro- oder Enterprise-Instanzen, die für die Geräteverwaltung registriert sind, oder MacOS-Instanzen, die über MDM verwaltet oder über MCX einer Domäne beigetreten sind.

Zuordnung von Richtlinienoptionen:

* RestoreOnStartupIsNewTabPage (5) = neue Registerkarte öffnen

* RestoreOnStartupIsLastSession (1) = die letzte Sitzung wiederherstellen

* RestoreOnStartupIsURLs (4) = eine Liste von URLs öffnen

Verwenden Sie die vorstehenden Informationen, wenn Sie diese Richtlinie konfigurieren.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Ganze Zahl

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: RestoreOnStartup
  - GP-Name: Auszuführende Aktion beim Start
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Startup, home page and new tab page
  - GP Pfad (Empfohlen): Administrative Templates/Microsoft Edge – Standardeinstellungen (Benutzer können diese außer Kraft setzen)/Startup, home page and new tab page
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Wertname: RestoreOnStartup
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000004
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: RestoreOnStartup
  - Beispielwert:
``` xml
<integer>4</integer>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### RestoreOnStartupURLs

  #### Websites, die beim Start des Browsers geöffnet werden sollen

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Sie können eine Liste mit Websites angeben, die beim Start des Browsers automatisch geöffnet werden sollen. Wenn Sie diese Richtlinie nicht konfigurieren, wird beim Start keine Website geöffnet.

Diese Richtlinie funktioniert nur, wenn Sie auch die [RestoreOnStartup](#restoreonstartup) Richtlinie so festlegen, dass eine Liste von URLs geöffnet wird (4).

Diese Richtlinie ist nur für Windows-Instanzen verfügbar, die mit einer Microsoft Active Directory-Domäne verknüpft sind, Windows 10 Pro- oder Enterprise-Instanzen, die für die Geräteverwaltung registriert sind, oder MacOS-Instanzen, die über MDM verwaltet oder über MCX einer Domäne beigetreten sind.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Liste von Zeichenfolgen

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: RestoreOnStartupURLs
  - GP-Name: Websites, die beim Start des Browsers geöffnet werden sollen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Startup, home page and new tab page
  - GP Pfad (Empfohlen): Administrative Templates/Microsoft Edge – Standardeinstellungen (Benutzer können diese außer Kraft setzen)/Startup, home page and new tab page
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge\RestoreOnStartupURLs
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Recommended\RestoreOnStartupURLs
  - Wertname: 1, 2, 3, ...
  - Werttyp: REG_SZ-Liste

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\RestoreOnStartupURLs\1 = "https://contoso.com"
SOFTWARE\Policies\Microsoft\Edge\RestoreOnStartupURLs\2 = "https://www.fabrikam.com"

```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: RestoreOnStartupURLs
  - Beispielwert:
``` xml
<array>
  <string>https://contoso.com</string>
  <string>https://www.fabrikam.com</string>
</array>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### ShowHomeButton

  #### Schaltfläche „Start“ auf der Symbolleiste anzeigen

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Zeigt die Schaltfläche "Start" auf der Microsoft Edge-Symbolleiste.

Aktivieren Sie diese Richtlinie, um immer die Schaltfläche "Start" anzuzeigen. Deaktivieren Sie diese Option, um die Schaltfläche niemals anzuzeigen.

Wenn Sie die Richtlinie nicht konfigurieren, können die Benutzer auswählen, ob die Schaltfläche Start angezeigt werden soll.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: ShowHomeButton
  - GP-Name: Schaltfläche „Start“ auf der Symbolleiste anzeigen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/Startup, home page and new tab page
  - GP Pfad (Empfohlen): Administrative Templates/Microsoft Edge – Standardeinstellungen (Benutzer können diese außer Kraft setzen)/Startup, home page and new tab page
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Wertname: ShowHomeButton
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: ShowHomeButton
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ## Weitere Richtlinien

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### AddressBarMicrosoftSearchInBingProviderEnabled

  #### Aktivieren von Microsoft Search in Bing-Vorschlägen in der Adressleiste

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 81 oder höher

  #### Beschreibung

  Aktiviert die Anzeige der relevanten Microsoft-Suche in Bing-Vorschläge in der Vorschlagsliste der Adressleiste, wenn der Benutzer eine Suchzeichenfolge in der Adressleiste eingibt. Wenn Sie diese Richtlinie aktivieren oder nicht konfigurieren, können Benutzer Ergebnisse anzeigen, die von Microsoft Suche in Bing in der Vorschlagsliste der Microsoft Edge-Adressleiste angezeigt werden. Um die Microsoft-Suche in Bing-Resultate anzuzeigen, muss der Benutzer mit seinem Azure AD-Konto für diese Organisation bei Microsoft Edge angemeldet sein.
Wenn Sie diese Richtlinie deaktivieren, können die Benutzer interne Ergebnisse in der Vorschlagsliste der Microsoft Edge-Adressleiste nicht anzeigen.
Wenn Sie die Richtlinien für einen standardmäßigen Suchanbieter ([DefaultSearchProviderEnabled](#defaultsearchproviderenabled), [DefaultSearchProviderName](#defaultsearchprovidername) und [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl)) aktiviert haben und der angegebene Suchanbieter nicht Bing ist, gilt diese Richtlinie nicht, und es gibt in der Vorschlagsliste der Adressleiste keine Microsoft-Suche in Bing-Vorschläge.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: AddressBarMicrosoftSearchInBingProviderEnabled
  - GP-Name: Aktivieren von Microsoft Search in Bing-Vorschlägen in der Adressleiste
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: AddressBarMicrosoftSearchInBingProviderEnabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: AddressBarMicrosoftSearchInBingProviderEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### AdsSettingForIntrusiveAdsSites

  #### Anzeigeneinstellung für Websites mit aufdringlichen Anzeigen

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 78 oder höher

  #### Beschreibung

  Steuert, ob Werbung auf Websites mit aufdringlichen Anzeigen blockiert wird.

Zuordnung von Richtlinienoptionen:

* AllowAds (1) = Werbung auf allen Websites zulassen

* BlockAds (2) = Werbung auf Websites mit aufdringlichen Anzeigen blockieren. (Standardwert)

Verwenden Sie die vorstehenden Informationen, wenn Sie diese Richtlinie konfigurieren.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Ganze Zahl

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: AdsSettingForIntrusiveAdsSites
  - GP-Name: Anzeigeneinstellung für Websites mit aufdringlichen Anzeigen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: AdsSettingForIntrusiveAdsSites
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: AdsSettingForIntrusiveAdsSites
  - Beispielwert:
``` xml
<integer>1</integer>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### AllowDeletingBrowserHistory

  #### Löschen des Browser- und Downloadverlaufs aktivieren

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Hiermit können Sie den Browserverlauf und den Downloadverlauf löschen und verhindern, dass Benutzer diese Einstellung ändern.

Beachten Sie, dass auch bei Abschaltung dieser Richtlinie nicht sichergestellt ist, dass der Browser- und Downloadverlauf unbedingt aufbewahrt wird: Benutzer können die Verlaufsdatenbankdateien direkt bearbeiten oder löschen und der Browser selbst kann (basierend auf dem Ablaufzeitraum) Verlaufselemente jederzeit löschen oder archivieren.

Wenn Sie diese Richtlinie aktivieren oder nicht konfigurieren, können Benutzer den Browser- und Downloadverlauf löschen.

Wenn Sie diese Richtlinie deaktivieren, können Benutzer den Browser- und Downloadverlauf nicht löschen, und die Verlaufssynchronisierung ist deaktiviert.

Wenn Sie diese Richtlinie aktivieren, aktivieren Sie die Richtlinie [ClearBrowsingDataOnExit](#clearbrowsingdataonexit) nicht, da sich beide auf das Löschen von Daten auswirken. Wenn Sie beide Optionen aktivieren, hat die [ClearBrowsingDataOnExit](#clearbrowsingdataonexit)-Richtlinie Vorrang und löscht alle Daten, wenn Microsoft Edge geschlossen wird – unabhängig davon, wie diese Richtlinie konfiguriert ist.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: AllowDeletingBrowserHistory
  - GP-Name: Löschen des Browser- und Downloadverlaufs aktivieren
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: AllowDeletingBrowserHistory
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: AllowDeletingBrowserHistory
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### AllowFileSelectionDialogs

  #### Dialogfelder „Dateiauswahl“ zulassen

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Ermöglichen Sie den Zugriff auf lokale Dateien, indem Sie Dateiauswahl-Dialogfelder in Microsoft Edge anzeigen lassen.

Wenn Sie diese Richtlinie aktivieren oder nicht konfigurieren, können Benutzer die Dateiauswahl Dialogfelder normal öffnen.

Wenn Sie diese Richtlinie deaktivieren und der Benutzer eine Aktion ausführt, durch die ein Dateiauswahl-Dialogfeld ausgelöst wird (z.B. beim Importieren von Favoriten, beim Hochladen von Dateien oder beim Speichern von Links), wird stattdessen eine Nachricht angezeigt, und es wird so verfahren, als hätte der Benutzer im Dateiauswahl-Dialogfeld auf „Abbrechen“ geklickt.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: AllowFileSelectionDialogs
  - GP-Name: Dialogfelder „Dateiauswahl“ zulassen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: AllowFileSelectionDialogs
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: AllowFileSelectionDialogs
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### AllowPopupsDuringPageUnload

  #### Ermöglicht es einer Seite, Popups während ihrer Entladung anzuzeigen

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 78 oder höher

  #### Beschreibung

  Diese Richtlinie ermöglicht es einem Administrator anzugeben, dass eine Seite während der Entladung Popups anzeigen kann.

Wenn die Richtlinie auf "aktiviert" festgelegt ist, können Seiten Popups anzeigen, während sie entladen werden.

Wenn die Richtlinie deaktiviert oder nicht eingerichtet ist, dürfen Seiten keine Popups anzeigen, während sie entladen werden. Dies ist gemäß Spezifikation: (https://html.spec.whatwg.org/#apis-for-creating-and-navigating-browsing-contexts-by-name).

Diese Richtlinie wird künftig entfernt.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: AllowPopupsDuringPageUnload
  - GP-Name: Ermöglicht es einer Seite, Popups während ihrer Entladung anzuzeigen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: AllowPopupsDuringPageUnload
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000000
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: AllowPopupsDuringPageUnload
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### AllowSurfGame

  #### Surfspiel zulassen

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 83 oder höher

  #### Beschreibung

  Wenn Sie diese Richtlinie deaktivieren, können die Benutzer das Surfspiel nicht spielen, wenn das Gerät offline ist oder wenn der Benutzer zu edge://surf navigiert.

Wenn Sie diese Richtlinie aktivieren oder nicht konfigurieren, können Benutzer das Surfspiel spielen.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: AllowSurfGame
  - GP-Name: Surfspiel zulassen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: AllowSurfGame
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000000
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: AllowSurfGame
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### AllowSyncXHRInPageDismissal

  #### Seiten das Senden synchroner XHR-Anforderungen während der Seitenschließung ermöglichen (veraltet)

  >VERALTET: Diese Richtlinie ist veraltet. Sie wird zurzeit unterstützt, aber in einer zukünftigen Version als veraltet behandelt.
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 79 oder höher

  #### Beschreibung

  Diese Richtlinie wird nicht mehr unterstützt, weil sie nur als kurzfristiger Mechanismus vorgesehen ist, um Unternehmen mehr Zeit zum Aktualisieren ihrer Webinhalte zu verschaffen, falls diese mit der Änderung inkompatibel sind, um synchrone XHR-Anforderungen während der Seitenschließung abzulehnen. Es wird in Microsoft Edge ab Version 88 nicht mehr funktionieren.

Mit dieser Richtlinie können Sie festlegen, dass während der Schließung einer Seite synchrone XHR-Anforderungen gesendet werden können.

Wenn Sie diese Richtlinie aktivieren, können Seiten synchrone XHR-Anforderungen während der Seitenschließung senden.

Wenn Sie diese Richtlinie deaktivieren oder diese Richtlinie nicht konfigurieren, dürfen Seiten während der Seitenschließung keine synchronen XHR-Anforderungen senden.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: AllowSyncXHRInPageDismissal
  - GP-Name: Seiten das Senden synchroner XHR-Anforderungen während der Seitenschließung ermöglichen (veraltet)
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: AllowSyncXHRInPageDismissal
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000000
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: AllowSyncXHRInPageDismissal
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### AllowTokenBindingForUrls

  #### Konfigurieren Sie die Liste der Websites, für die Microsoft Edge versucht, eine Tokenbindung einzurichten.

  
  
  #### Unterstützte Versionen:

  - Auf Windows ab 83 oder höher

  #### Beschreibung

  Konfigurieren Sie die Liste der URL-Muster für Websites, bei denen der Browser versucht, das Token Binding-Protokoll auszuführen.
Bei den Domänen in dieser Liste sendet der Browser das Token Binding-ClientHello im TLS-Handshake (siehe https://tools.ietf.org/html/rfc8472).
Wenn der Server mit einer gültigen ServerHello-Antwort antwortet, erstellt und sendet der Browser Token-Binding-Meldungen bei nachfolgenden HTTPS-Anforderungen. Weitere Informationen finden Sie unter https://tools.ietf.org/html/rfc8471.

Wenn diese Liste leer ist, wird die Tokenbindung deaktiviert.

Diese Richtlinie steht nur auf Windows 10-Geräten zur Verfügung, die den Modus für virtuelle Sicherheit aufweisen.

Ab Microsoft Edge 86 unterstützt diese Richtlinie keine dynamische Aktualisierung mehr.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Liste von Zeichenfolgen

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: AllowTokenBindingForUrls
  - GP-Name: Konfigurieren Sie die Liste der Websites, für die Microsoft Edge versucht, eine Tokenbindung einzurichten.
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge\AllowTokenBindingForUrls
  - Pfad (Empfohlen): n.a.
  - Wertname: 1, 2, 3, ...
  - Werttyp: REG_SZ-Liste

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\AllowTokenBindingForUrls\1 = "mydomain.com"
SOFTWARE\Policies\Microsoft\Edge\AllowTokenBindingForUrls\2 = "[*.]mydomain2.com"
SOFTWARE\Policies\Microsoft\Edge\AllowTokenBindingForUrls\3 = "[*.].mydomain2.com"

```

  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### AllowTrackingForUrls

  #### Konfigurieren der Ausnahmen für die Nachverfolgungs-Vorbeugung für bestimmte Websites

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 78 oder höher

  #### Beschreibung

  Konfigurieren Sie die Liste der URL-Muster, die vom Nachverfolgungsschutz ausgeschlossen sind.

Wenn Sie diese Richtlinie konfigurieren, wird die Liste der konfigurierten URL-Muster vom Nachverfolgungsschutz ausgeschlossen.

Falls Sie diese Richtlinie nicht konfigurieren, wird der globale Standardwert aus der „Blockieren der Nachverfolgung der Webbrowsing-Aktivitäten des Benutzers“-Richtlinie (sofern festgelegt) oder die persönliche Konfiguration des Benutzers für alle Websites verwendet.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Liste von Zeichenfolgen

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: AllowTrackingForUrls
  - GP-Name: Konfigurieren der Ausnahmen für die Nachverfolgungs-Vorbeugung für bestimmte Websites
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge\AllowTrackingForUrls
  - Pfad (Empfohlen): n.a.
  - Wertname: 1, 2, 3, ...
  - Werttyp: REG_SZ-Liste

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\AllowTrackingForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\AllowTrackingForUrls\2 = "[*.]contoso.edu"

```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: AllowTrackingForUrls
  - Beispielwert:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### AlternateErrorPagesEnabled

  #### Ähnliche Seiten vorschlagen, wenn eine Webseite nicht gefunden werden kann

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 80 oder höher

  #### Beschreibung

  Microsoft Edge kann eine Verbindung mit einem Webdienst herstellen, um URL- und Suchvorschläge zu Verbindungsproblemen wie DNS-Fehlern zu generieren.

Wenn Sie diese Richtlinie aktivieren, wird ein Webdienst verwendet, um URL- und Suchvorschläge zu Netzwerkfehlern zu generieren.

Wenn Sie diese Richtlinie deaktivieren, werden keine Abfragen an den Webdienst gesendet und es wird eine Standardfehlerseite angezeigt.

Wenn Sie diese Richtlinie nicht konfigurieren, respektiert Microsoft Edge die Benutzereinstellungen, die unter Dienste unter Edge://Settings/Privacy festgelegt sind.
Insbesondere gibt es ein Auswahlfeld namens **ähnliche Seiten vorschlagen, wenn eine Webseite nicht gefunden werden kann**, das der Benutzer ein- oder ausschalten kann. Beachten Sie, dass wenn Sie diese Richtlinie aktiviert haben (AlternateErrorPagesEnabled), die Einstellung „ähnliche Seiten vorschlagen, wenn eine Webseite nicht gefunden werden kann“ eingeschaltet ist, doch der Benutzer kann die Einstellung nicht mithilfe des Auswahlfeldes ändern. Wenn Sie diese Richtlinie deaktivieren, wird die Einstellung „ähnliche Seiten vorschlagen, wenn eine Webseite nicht gefunden werden kann“ deaktiviert, und der Benutzer kann die Einstellung nicht mithilfe der Umschaltfläche ändern.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: AlternateErrorPagesEnabled
  - GP-Name: Ähnliche Seiten vorschlagen, wenn eine Webseite nicht gefunden werden kann
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): Administrative Templates/Microsoft Edge – Standardeinstellungen (Benutzer können diese außer Kraft setzen)/
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Wertname: AlternateErrorPagesEnabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: AlternateErrorPagesEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### AlwaysOpenPdfExternally

  #### PDF-Dateien immer extern öffnen

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Deaktiviert den internen PDF-Viewer in Microsoft Edge.

Wenn Sie diese Richtlinie aktivieren, behandelt Microsoft Edge PDF-Dateien als Downloads und ermöglicht es Benutzern, diese mit der Standardanwendung zu öffnen.

Wenn Sie diese Richtlinie nicht konfigurieren oder nicht aktivieren, öffnet Microsoft Edge PDF-Dateien (es sei denn, der Benutzer deaktiviert dies).

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: AlwaysOpenPdfExternally
  - GP-Name: PDF-Dateien immer extern öffnen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: AlwaysOpenPdfExternally
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: AlwaysOpenPdfExternally
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### AmbientAuthenticationInPrivateModesEnabled

  #### Aktivieren der Umgebungsauthentifizierung für InPrivate- und Gastprofile

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 81 oder höher

  #### Beschreibung

  Konfigurieren Sie diese Richtlinie, um die Umgebungsauthentifizierung für InPrivate- und Gastprofile in Microsoft Edge zuzulassen oder abzulehnen.

Die Umgebungsauthentifizierung ist eine HTTP-Authentifizierung mit Standardanmeldeinformationen, wenn explizite Anmeldeinformationen nicht über NTLM/Kerberos/Negotiate Challenge/Antwortschemen bereitgestellt werden.

Wenn Sie die Richtlinie auf „RegularOnly“ festlegen, wird die Ambient-Authentifizierung nur für reguläre Sitzungen zugelassen. InPrivate- und Gastsitzungen dürfen keine Ambient-Authentifizierung durchführen.

Wenn Sie die Richtlinie auf „InPrivateAndRegular“ festlegen, wird die Ambient-Authentifizierung für InPrivate und reguläre Sitzungen zugelassen. Gastsitzungen dürfen keine Ambient-Authentifizierung durchführen.

Wenn Sie die Richtlinie auf „GuestAndRegular“ festlegen, ist die Ambient-Authentifizierung für Gast- und normale Sitzungen zugelassen. InPrivate-Sitzungen dürfen keine Ambient-Authentifizierung durchführen.

Wenn Sie die Richtlinie auf „All“ festlegen, wird die Umgebungsauthentifizierung für alle Sitzungen zugelassen.

Beachten Sie, dass die Ambient-Authentifizierung in normalen Profilen immer zulässig ist.

Wenn die Richtlinie in der Microsoft Edge-Version 81 und neuer nicht festgelegt ist, wird die Ambient-Authentifizierung nur in regulären Sitzungen aktiviert.

Zuordnung von Richtlinienoptionen:

* RegularOnly (0) = Ambient-Authentifizierung nur in regulären Sitzungen aktivieren

* InPrivateAndRegular (1) = Aktivieren der Ambient-Authentifizierung für InPrivate- und reguläre Sitzungen

* GuestAndRegular (2) = Aktivieren der Ambient-Authentifizierung für Gast- und reguläre Sitzungen

* All (3) = Aktivieren der Ambient-Authentifizierung für reguläre, InPrivate- und Gastsitzungen

Verwenden Sie die vorstehenden Informationen, wenn Sie diese Richtlinie konfigurieren.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Ganze Zahl

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: AmbientAuthenticationInPrivateModesEnabled
  - GP-Name: Aktivieren der Umgebungsauthentifizierung für InPrivate- und Gastprofile
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: AmbientAuthenticationInPrivateModesEnabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000000
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: AmbientAuthenticationInPrivateModesEnabled
  - Beispielwert:
``` xml
<integer>0</integer>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### AppCacheForceEnabled

  #### Ermöglicht das erneute Aktivieren des AppCache-Features, auch wenn es standardmäßig deaktiviert ist

  
  
  #### Unterstützte Versionen:

  - Auf Windows und MacOS ab 84 oder höher

  #### Beschreibung

  Wenn Sie diese Richtlinie auf "wahr" festlegen, ist die AppCache aktiviert, auch wenn AppCache in Microsoft Edge standardmäßig nicht verfügbar ist.

Wenn Sie diese Richtlinie auf "falsch" festlegen oder nicht festlegen, folgt AppCache den Standardwerten von Microsoft Edge.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - Eindeutiger Name des GP: AppCacheForceEnabled
  - GP-Name: Ermöglicht das erneute Aktivieren des AppCache-Features, auch wenn es standardmäßig deaktiviert ist
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: AppCacheForceEnabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000000
```

  #### Mac – Informationen und Einstellungen
  
  - Name des Einstellungsschlüssels: AppCacheForceEnabled
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### ApplicationLocaleValue

  #### Festlegen des Anwendungsgebietsschemas

  
  
  #### Unterstützte Versionen:

  - Auf Windows ab 77 oder höher

  #### Beschreibung

  Konfiguriert das App-Gebietsschema in Microsoft Edge und hindert Benutzer daran, das Gebietsschema zu ändern.

Wenn Sie diese Richtlinie aktivieren, verwendet Microsoft Edge das angegebene Gebietsschema. Wenn das konfigurierte Gebietsschema nicht unterstützt wird, wird stattdessen "en-US" verwendet.

Wenn Sie diese Einstellung deaktivieren oder nicht konfigurieren, verwendet Microsoft Edge entweder das vom Benutzer angegebene bevorzugte Gebietsschema (sofern konfiguriert) oder das Fallback-Gebietsschema "en-US".

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Zeichenfolge

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP unique name: ApplicationLocaleValue
  - GP-Name: Festlegen des Anwendungsgebietsschemas
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): Administrative Templates/Microsoft Edge – Standardeinstellungen (Benutzer können diese außer Kraft setzen)/
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Wertname: ApplicationLocaleValue
  - Werttyp: REG_SZ

  ##### Beispielwert:

```
"en"
```

  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### AudioCaptureAllowed

  #### Audio-Aufnahme zulassen oder blockieren

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Ermöglicht es Ihnen, festzulegen, ob ein Benutzer aufgefordert wird, einer Website Zugriff auf sein Audioaufnahmegerät einzuräumen. Diese Richtlinie gilt für alle URLs außer denen, die in der Liste [AudioCaptureAllowedUrls](#audiocaptureallowedurls) konfiguriert sind.

Wenn Sie diese Richtlinie aktivieren oder nicht konfigurieren (die Standardeinstellung), wird der Benutzer für den Zugriff auf Audioaufzeichnungsgeräte aufgefordert, außer bei den URLs in der Liste [AudioCaptureAllowedUrls](#audiocaptureallowedurls). Diesen aufgelisteten URLs wird ohne Aufforderung an den Benutzer der Zugriff gewährt.

Wenn Sie diese Richtlinie deaktivieren, wird der Benutzer nicht aufgefordert, und die Audioaufzeichnung kann nur für die in [AudioCaptureAllowedUrls](#audiocaptureallowedurls) konfigurierten URLs aufgerufen werden.

Diese Richtlinie wirkt sich auf alle Arten von Audio-Eingabegeräten aus, nicht nur auf das integrierte Mikrofon.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: AudioCaptureAllowed
  - GP-Name: Audio-Aufnahme zulassen oder blockieren
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: AudioCaptureAllowed
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000000
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: AudioCaptureAllowed
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### AudioCaptureAllowedUrls

  #### Websites, die auf Audio-Aufnahmegeräte zugreifen können, ohne eine Berechtigung anfordern zu müssen

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Sie können auf der Grundlage von URL-Mustern Websites angeben, die Audioaufnahmegeräte verwenden können, ohne den Benutzer um Erlaubnis zu bitten. Muster in dieser Liste werden mit dem Sicherheitsursprung der anfordernden URL abgeglichen. Wenn eine Übereinstimmung vorliegt, wird automatisch der Zugriff auf die Audioaufnahmegeräte gewährt.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Liste von Zeichenfolgen

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: AudioCaptureAllowedUrls
  - GP-Name: Websites, die auf Audio-Aufnahmegeräte zugreifen können, ohne eine Berechtigung anfordern zu müssen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge\AudioCaptureAllowedUrls
  - Pfad (Empfohlen): n.a.
  - Wertname: 1, 2, 3, ...
  - Werttyp: REG_SZ-Liste

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\AudioCaptureAllowedUrls\1 = "https://www.contoso.com/"
SOFTWARE\Policies\Microsoft\Edge\AudioCaptureAllowedUrls\2 = "https://[*.]contoso.edu/"

```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: AudioCaptureAllowedUrls
  - Beispielwert:
``` xml
<array>
  <string>https://www.contoso.com/</string>
  <string>https://[*.]contoso.edu/</string>
</array>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### AudioSandboxEnabled

  #### Audio-Sandkasten ausführen lassen

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 81 oder höher

  #### Beschreibung

  Diese Richtlinie steuert die Audioprozess-Sandbox.

Wenn Sie diese Richtlinie aktivieren, wird der Audiovorgang in der Sandbox ausgeführt.

Wenn Sie diese Richtlinie deaktivieren, wird der Audiovorgang nicht in der Sandbox ausgeführt, und das WebRTC-Audioverarbeitungsmodul wird im Rendererprozess ausgeführt.
Damit bleiben die Benutzer offen für Sicherheitsrisiken, die mit der Ausführung des Audio-Subsystems außerhalb einer Sandbox verbunden sind.

Wenn Sie diese Richtlinie nicht konfigurieren, wird die Standardkonfiguration für die Audio-Sandbox verwendet, die je nach Plattform unterschiedlich sein kann.

Diese Richtlinie soll Unternehmen Flexibilität beim Deaktivieren der Audio-Sandbox bieten, wenn sie Sicherheitssoftware-Setups verwenden, welche die Sandbox behindert.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: AudioSandboxEnabled
  - GP-Name: Audio-Sandkasten ausführen lassen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: AudioSandboxEnabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: AudioSandboxEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### AutoImportAtFirstRun

  #### Automatisches Importieren der Daten und Einstellungen eines anderen Browsers bei der ersten Ausführung

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Wenn Sie diese Richtlinie aktivieren, werden alle unterstützten Datentypen und Einstellungen aus dem angegebenen Browser bei der ersten Ausführung automatisch und im Hintergrund importiert. In der Benutzererfahrung zur ersten Ausführung wird der Import-Abschnitt ebenfalls übersprungen.

Die Browserdaten aus Microsoft Edge Legacy werden bei der ersten Ausführung unabhängig vom Wert dieser Richtlinie immer automatisch migriert.

Wenn diese Richtlinie auf „FromDefaultBrowser“ eingestellt ist, werden die Datentypen importiert, die dem Standardbrowser auf dem verwalteten Gerät entsprechen.

Wenn der als Wert dieser Richtlinie angegebene Browser nicht auf dem verwalteten Gerät vorhanden ist, wird der Import durch Microsoft Edge einfach übersprungen, ohne dass eine Benachrichtigung an den Benutzer erfolgt.

Wenn Sie diese Richtlinie auf „DisabledAutoImport“ festgelegt haben, wird der Import-Abschnitt der Benutzererfahrung zur ersten Ausführung vollständig übersprungen, und Microsoft Edge importiert keine Browserdaten und -Einstellungen automatisch.

Wenn diese Richtlinie auf den Wert „FromInternetExplorer“ eingestellt ist, werden die folgenden Datentypen aus Internet Explorer importiert:
1. Favoriten oder Lesezeichen
2. Gespeicherte Kennwörter
3. Suchmaschinen
4. Browserverlauf
5. Startseite

Wenn diese Richtlinie auf den Wert „FromGoogleChrome“ festgelegt ist, werden die folgenden Datentypen aus Google Chrome importiert:
1. Favoriten
2. Gespeicherte Kennwörter
3. Adressen und weiteres
4. Zahlungsinformationen
5. Browserverlauf
6. Einstellungen
7. Angepinnte und geöffnete Registerkarten
8. Extensions
9. Cookies

Hinweis: Weitere Informationen dazu, was aus Google Chrome importiert wird, finden Sie unter [https://go.microsoft.com/fwlink/?linkid=2120835](https://go.microsoft.com/fwlink/?linkid=2120835)

Wenn diese Richtlinie auf den Wert „FromSafari“ eingestellt ist, werden Benutzerdaten nicht mehr in Microsoft Edge importiert. Dies ist aufgrund der Funktionsweise von Full Disk Access auf Mac.
Auf MacOS Mojave und höher ist es nicht mehr möglich, Safari-Daten automatisch und unbeaufsichtigt in Microsoft Edge zu importieren.

Beginnend mit Microsoft Edge Version 83 werden die folgenden Datentypen aus Mozilla Firefox importiert, wenn diese Richtlinie auf den Wert „FromMozillaFirefox“ gesetzt ist:
1. Favoriten oder Lesezeichen
2. Gespeicherte Kennwörter
3. Adressen und weiteres
4. Browserverlauf

Wenn Sie verhindern möchten, dass bestimmte Datentypen auf verwalteten Geräten importiert werden, können Sie diese Richtlinie mit anderen Richtlinien wie [ImportAutofillFormData](#importautofillformdata), [ImportBrowserSettings](#importbrowsersettings), [ImportFavorites](#importfavorites) usw. verwenden.

Zuordnung von Richtlinienoptionen:

* FromDefaultBrowser (0) = importiert automatisch alle unterstützten Datentypen und Einstellungen aus dem Standardbrowser

* FromDefaultBrowser (1) = importiert automatisch alle unterstützten Datentypen und Einstellungen aus dem Internet Explorer

* FromGoogleChrome (2) = importiert automatisch alle unterstützten Datentypen und Einstellungen von Google Chrome

* FromSafari (3) = importiert automatisch alle unterstützten Datentypen und Einstellungen aus Safari

* DisabledAutoImport (4) = deaktiviert den automatischen Import und überspringt den Import-Abschnitt der Benutzererfahrung zur ersten Ausführung

* FromMozillaFirefox (5) = importiert automatisch alle unterstützten Datentypen und Einstellungen aus Mozilla Firefox

Verwenden Sie die vorstehenden Informationen, wenn Sie diese Richtlinie konfigurieren.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Ganze Zahl

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: AutoImportAtFirstRun
  - GP-Name: Automatisches Importieren der Daten und Einstellungen eines anderen Browsers bei der ersten Ausführung
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: AutoImportAtFirstRun
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000002
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: AutoImportAtFirstRun
  - Beispielwert:
``` xml
<integer>2</integer>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### AutoLaunchProtocolsFromOrigins

  #### Eine Liste der Protokolle definieren, mit denen eine externe Anwendung von den aufgeführten Ursprüngen aus gestartet werden kann, ohne den Benutzer aufzufordern

  
  
  #### Unterstützte Versionen:

  - Auf Windows und MacOS ab 85 oder später

  #### Beschreibung

  Ermöglicht es Ihnen, eine Liste der Protokolle und für jedes Protokoll eine zugeordnete Liste zulässiger Ursprungsmuster festzulegen, die eine externe Anwendung starten können, ohne den Benutzer aufzufordern. Das nachgestellte Trennzeichen sollte nicht einbezogen werden, wenn das Protokoll aufgelistet wird. Listen Sie beispielsweise "Skype" anstelle von "Skype:" oder "Skype://" auf.

Wenn Sie diese Richtlinie konfigurieren, ist es nur zulässig, ein Protokoll zu starten, ohne dass eine externe Anwendung durch Richtlinie angefordert wird wenn:

- das Protokoll aufgelistet ist

- der Ursprung der Website, die versucht, das Protokoll zu starten, einem der Ursprungsmuster entspricht in der allowed_origins Liste dieses Protokolls.

Wenn eine der Bedingungen falsch ist, wird die Eingabeaufforderung für den externen Protokollstart nicht durch Richtlinien ausgelassen.

Wenn Sie diese Richtlinie nicht konfigurieren, können keine Protokolle ohne Eingabeaufforderung gestartet werden. Benutzer können die Eingabeaufforderungen auf Protokoll-/Website Basis deaktivieren, es sei denn, die Richtlinie [ExternalProtocolDialogShowAlwaysOpenCheckbox](#externalprotocoldialogshowalwaysopencheckbox) ist deaktiviert. Diese Richtlinie wirkt sich nicht auf die von Benutzern festgelegten Ausnahmen pro Protokoll/Website aus.

Bei den Mustern für den Ursprung entsprechen dieselben Formate wie für die [URLBlocklist-](#urlblocklist) Richtlinie, die bei[https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)dokumentiert sind.

Allerdings können die Ursprungs Übereinstimmungsmuster für diese Richtlinie keine "/Path"-oder "@Query"-Elemente enthalten. Jedes Muster, das das Element "/Path" oder "@Query" enthält, wird ignoriert.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Dictionary

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - Eindeutiger Name des GP: AutoLaunchProtocolsFromOrigins
  - GP-Name: Eine Liste der Protokolle definieren, mit denen eine externe Anwendung von den aufgeführten Ursprüngen aus gestartet werden kann, ohne den Benutzer aufzufordern
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: AutoLaunchProtocolsFromOrigins
  - Werttyp: REG_SZ

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\AutoLaunchProtocolsFromOrigins = [
  {
    "allowed_origins": [
      "example.com", 
      "http://www.example.com:8080"
    ], 
    "protocol": "spotify"
  }, 
  {
    "allowed_origins": [
      "https://example.com", 
      "https://.mail.example.com"
    ], 
    "protocol": "teams"
  }, 
  {
    "allowed_origins": [
      "*"
    ], 
    "protocol": "outlook"
  }
]
```

  ##### Kompakter Beispielwert:

  ```
  SOFTWARE\Policies\Microsoft\Edge\AutoLaunchProtocolsFromOrigins = [{"allowed_origins": ["example.com", "http://www.example.com:8080"], "protocol": "spotify"}, {"allowed_origins": ["https://example.com", "https://.mail.example.com"], "protocol": "teams"}, {"allowed_origins": ["*"], "protocol": "outlook"}]
  ```
  

  #### Mac – Informationen und Einstellungen
  
  - Name des Einstellungsschlüssels: AutoLaunchProtocolsFromOrigins
  - Beispielwert:
``` xml
<key>AutoLaunchProtocolsFromOrigins</key>
<array>
  <dict>
    <key>allowed_origins</key>
    <array>
      <string>example.com</string>
      <string>http://www.example.com:8080</string>
    </array>
    <key>protocol</key>
    <string>spotify</string>
  </dict>
  <dict>
    <key>allowed_origins</key>
    <array>
      <string>https://example.com</string>
      <string>https://.mail.example.com</string>
    </array>
    <key>protocol</key>
    <string>teams</string>
  </dict>
  <dict>
    <key>allowed_origins</key>
    <array>
      <string>*</string>
    </array>
    <key>protocol</key>
    <string>outlook</string>
  </dict>
</array>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### AutoOpenAllowedForURLs

  #### URLs, auf die AutoOpenFileTypes angewendet werden können

  
  
  #### Unterstützte Versionen:

  - Auf Windows und MacOS ab 85 oder später

  #### Beschreibung

  Eine Liste der URLs, auf die [AutoOpenFileTypes-](#autoopenfiletypes) angewendet werden sollen. Diese Richtlinie hat keine Auswirkungen auf automatisch geöffnete Werte, die von Benutzern über das Download-Feld festgelegt werden... > Menüeintrag "Dateien dieser Art immer öffnen".

Wenn Sie URLs in dieser Richtlinie festlegen, werden Dateien nur nach Richtlinie automatisch geöffnet, wenn die URL Bestandteil dieses Satzes ist und der Dateityp in [AutoOpenFileTypes-](#autoopenfiletypes)aufgelistet wird. Wenn eine der beiden Voraussetzungen falsch ist, wird der Download nicht automatisch durch Richtlinie geöffnet.

Wenn Sie diese Richtlinie nicht festlegen, werden alle Downloads, bei denen der Dateityp in [AutoOpenFileTypes](#autoopenfiletypes) ist, automatisch geöffnet.

Ein URL-Muster muss gemäß [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)formatiert sein.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Liste von Zeichenfolgen

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - Eindeutiger Name des GP: AutoOpenAllowedForURLs
  - GP-Name: URLs, auf die AutoOpenFileTypes angewendet werden können
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Path (Mandatory): SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs
  - Pfad (Empfohlen): n.a.
  - Wertname: 1, 2, 3, ...
  - Werttyp: REG_SZ-Liste

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\1 = "example.com"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\2 = "https://ssl.server.com"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\3 = "hosting.com/good_path"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\4 = "https://server:8080/path"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\5 = ".exact.hostname.com"

```

  #### Mac – Informationen und Einstellungen
  
  - Name des Einstellungsschlüssels: AutoOpenAllowedForURLs
  - Beispielwert:
``` xml
<array>
  <string>example.com</string>
  <string>https://ssl.server.com</string>
  <string>hosting.com/good_path</string>
  <string>https://server:8080/path</string>
  <string>.exact.hostname.com</string>
</array>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### AutoOpenFileTypes

  #### Liste der Dateitypen, die beim Download automatisch geöffnet werden sollen

  
  
  #### Unterstützte Versionen:

  - Auf Windows und MacOS ab 85 oder später

  #### Beschreibung

  Mit dieser Richtlinie wird eine Liste der Dateitypen festgelegt, die beim Download automatisch geöffnet werden sollen. Hinweis: beim Auflisten des Dateityps sollte das führende Trennzeichen nicht einbezogen werden, also wird "txt" anstelle von ".txt" aufgelistet.

Standardmäßig werden diese Dateitypen automatisch für alle URLs geöffnet. Sie können die [AutoOpenAllowedForURLs](#autoopenallowedforurls) Richtlinie verwenden, um die URLs einzuschränken, für die diese Dateitypen automatisch geöffnet werden.

Dateien mit Typen, die automatisch geöffnet werden sollten, unterliegen weiterhin der aktivierten Microsoft Defender-SmartScreen-Überprüfung und werden nicht geöffnet, wenn diese Überprüfung fehlschlägt. 

Die Dateitypen, die ein Benutzer bereits für das automatische öffnen angegeben hat, werden beim Herunterladen weiterhin durchgeführt. Der Benutzer kann weiterhin weitere Dateitypen angeben, die automatisch geöffnet werden sollen.

Wenn Sie diese Richtlinie nicht festlegen, werden nur die Dateitypen, die ein Benutzer bereits für das automatische öffnen angegeben hat, beim Herunterladen verwendet.

Diese Richtlinie ist nur für Windows-Instanzen verfügbar, die mit einer Microsoft Active Directory-Domäne verknüpft sind, Windows 10 Pro- oder Enterprise-Instanzen, die für die Geräteverwaltung registriert sind, oder MacOS-Instanzen, die über MDM verwaltet oder über MCX einer Domäne beigetreten sind.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Liste von Zeichenfolgen

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - Eindeutiger Name des GP: AutoOpenFileTypes
  - GP-Name: Liste der Dateitypen, die beim Download automatisch geöffnet werden sollen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Path (Mandatory): SOFTWARE\Policies\Microsoft\Edge\AutoOpenFileTypes
  - Pfad (Empfohlen): n.a.
  - Wertname: 1, 2, 3, ...
  - Werttyp: REG_SZ-Liste

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\AutoOpenFileTypes\1 = "exe"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenFileTypes\2 = "txt"

```

  #### Mac – Informationen und Einstellungen
  
  - Name des Einstellungsschlüssels: AutoOpenFileTypes
  - Beispielwert:
``` xml
<array>
  <string>exe</string>
  <string>txt</string>
</array>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### AutofillAddressEnabled

  #### Automatisches Ausfüllen von Adressen zulassen

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Aktiviert das Feature "AutoFill" und ermöglicht es Benutzern, Adressinformationen in Webformularen mit zuvor gespeicherten Informationen automatisch zu vervollständigen.

Wenn Sie diese Richtlinie deaktivieren, werden Adressinformationen von AutoFill niemals vorgeschlagen oder ausgefüllt, und es werden auch keine weiteren Adressinformationen gespeichert, die der Benutzer während des Surfens im Internet möglicherweise senden kann.

Wenn Sie diese Richtlinie aktivieren oder nicht konfigurieren, können Benutzer AutoFill für Adressen über die Benutzeroberfläche steuern.

Beachten Sie, dass Sie, wenn Sie diese Richtlinie deaktivieren, auch alle Aktivitäten aller Webformulare beenden, außer Zahlungs- und Kennwort-Formularen. Es werden keine weiteren Einträge gespeichert, und Microsoft Edge schlägt keine vorherigen Einträge vor oder verwendet AutoFill.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: AutofillAddressEnabled
  - GP-Name: Automatisches Ausfüllen von Adressen zulassen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): Administrative Templates/Microsoft Edge – Standardeinstellungen (Benutzer können diese außer Kraft setzen)/
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Wertname: AutofillAddressEnabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000000
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: AutofillAddressEnabled
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### AutofillCreditCardEnabled

  #### AutoFill für Kreditkartendaten aktivieren

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Aktiviert das Feature "AutoFill" in Microsoft Edge und lässt Benutzer Kreditkarteninformationen in Webformularen mit zuvor gespeicherten Informationen automatisch vervollständigen.

Wenn Sie diese Richtlinie deaktivieren, werden Kreditkarteninformationen von AutoFill niemals vorgeschlagen oder ausgefüllt, und es werden auch keine weiteren Kreditkarteninformationen gespeichert, die Benutzer während des Surfens im Internet möglicherweise senden können.

Wenn Sie diese Richtlinie aktivieren oder nicht konfigurieren, können Benutzer AutoFill für Kreditkarten steuern.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: AutofillCreditCardEnabled
  - GP-Name: AutoFill für Kreditkartendaten aktivieren
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): Administrative Templates/Microsoft Edge – Standardeinstellungen (Benutzer können diese außer Kraft setzen)/
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Wertname: AutofillCreditCardEnabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000000
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: AutofillCreditCardEnabled
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### AutoplayAllowed

  #### Zulassen der automatischen Wiedergabe von Medien für Websites

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 78 oder höher

  #### Beschreibung

  Mit dieser Richtlinie wird die Medien AutoPlay-Richtlinie für Websites festgelegt.

Die Standardeinstellung "nicht konfiguriert" respektiert die aktuellen Einstellungen für die Wiedergabe von Medien und ermöglicht Benutzern, ihre Einstellungen für die automatische Wiedergabe zu konfigurieren.

Wenn Sie die Richtlinine auf "aktiviert" festlegen, wird die automatische Wiedergabe auf "zulassen" festgelegt.  Allen Websites ist die Wiedergabe von Medien gestattet. Benutzer können diese Richtlinie nicht außer Kraft setzen.

Wenn Sie die Richtlinine auf "deaktiviert" festlegen, wird die automatische Wiedergabe auf "blockieren" festgelegt.  Keiner Website ist die Wiedergabe von Medien gestattet. Benutzer können diese Richtlinie nicht außer Kraft setzen.

Eine Registerkarte muss geschlossen und erneut geöffnet werden, damit diese Richtlinie wirksam wird.


  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: AutoplayAllowed
  - GP-Name: Zulassen der automatischen Wiedergabe von Medien für Websites
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: AutoplayAllowed
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: AutoplayAllowed
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### BackgroundModeEnabled

  #### Ausführung von Hintergrund-Apps zulassen, nachdem Microsoft Edge geschlossen wurde

  
  
  #### Unterstützte Versionen:

  - Auf Windows ab 77 oder höher

  #### Beschreibung

  Microsoft Edge-Prozesse können bei der Betriebssystem-Anmeldung starten und nach dem Schließen des letzten Browserfensters weiterhin ausgeführt werden. In diesem Szenario bleiben Hintergrund-Apps und die aktuelle Browsersitzung aktiv, einschließlich aller Sitzungscookies. Bei einem geöffneten Hintergrundprozess wird ein Symbol in der Taskleiste angezeigt, und er kann immer von dort aus geschlossen werden.

Wenn Sie diese Richtlinie aktivieren, ist der Hintergrundmodus aktiviert.

Wenn Sie diese Richtlinie deaktivieren, ist der Hintergrundmodus deaktiviert.

Wenn Sie diese Richtlinie nicht konfigurieren, ist der Hintergrundmodus anfänglich deaktiviert, und der Benutzer kann dessen Verhalten in Edge://Settings/System konfigurieren.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: BackgroundModeEnabled
  - GP-Name: Ausführung von Hintergrund-Apps zulassen, nachdem Microsoft Edge geschlossen wurde
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): Administrative Templates/Microsoft Edge – Standardeinstellungen (Benutzer können diese außer Kraft setzen)/
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Wertname: BackgroundModeEnabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### BackgroundTemplateListUpdatesEnabled

  #### Aktiviert Hintergrundaktualisierungen der Liste verfügbarer Vorlagen für Kollektionen und andere Features, die Vorlagen verwenden

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 79 oder höher

  #### Beschreibung

  Aktiviert oder deaktiviert Hintergrundaktualisierungen der Liste verfügbarer Vorlagen für Kollektionen und andere Features, die Vorlagen verwenden.  Vorlagen werden verwendet, um umfangreiche Metadaten aus einer Webseite zu extrahieren, wenn die Seite in einer Sammlung gespeichert wird.

Wenn Sie diese Einstellung aktivieren oder die Einstellung nicht konfiguriert ist, wird die Liste der verfügbaren Vorlagen alle 24 Stunden im Hintergrund von einem Microsoft-Dienst heruntergeladen.

Wenn Sie diese Einstellung deaktivieren, wird die Liste der verfügbaren Vorlagen bei Bedarf heruntergeladen. Diese Art von Download kann zu kleinen Leistungseinbußen bei Sammlungen und anderen Features führen.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: BackgroundTemplateListUpdatesEnabled
  - GP-Name: Aktiviert Hintergrundaktualisierungen der Liste verfügbarer Vorlagen für Kollektionen und andere Features, die Vorlagen verwenden
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: BackgroundTemplateListUpdatesEnabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: BackgroundTemplateListUpdatesEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### BingAdsSuppression

  #### Blockieren aller Anzeigen in Bing-Suchergebnissen

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 83 oder höher

  #### Beschreibung

  Ermöglicht eine Suchumgebung ohne Werbung auf Bing.com

Wenn Sie diese Richtlinie aktivieren, kann ein Benutzer auf Bing.com suchen, ohne dass dabei Werbung angezeigt wird. Gleichzeitig wird die SafeSearch-Einstellung auf "Strikt" festgelegt und kann vom Benutzer nicht geändert werden.

Wenn Sie diese Richtlinie nicht konfigurieren, werden in den Suchergebnissen auf Bing.com Werbeanzeigen angezeigt. SafeSearch wird standardmäßig auf "moderat" festgelegt und kann vom Benutzer geändert werden.

Diese Richtlinie steht nur für K-12-SKUs zur Verfügung, die von Microsoft als EDU-Mandanten anerkannt werden.

Wenn Sie weitere Informationen zu dieser Richtlinie erhalten möchten oder die folgenden Szenarien auf Sie zutreffen, lesen Sie bitte [https://go.microsoft.com/fwlink/?linkid=2119711](https://go.microsoft.com/fwlink/?linkid=2119711):

* Sie verfügen über einen EDU-Mandanten, aber die Richtlinie funktioniert nicht.

* Ihre IP-Adresse wurde für das werbefreie Sucherlebnis auf eine Whitelist gesetzt.

* Bei Microsoft Edge Legacy hatten Sie bereits die werbefreie Suchumgebung und möchten ein Upgrade auf die neue Version von Microsoft Edge durchführen.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: BingAdsSuppression
  - GP-Name: Blockieren aller Anzeigen in Bing-Suchergebnissen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: BingAdsSuppression
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: BingAdsSuppression
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### BlockThirdPartyCookies

  #### Blockieren der Cookies von Drittanbietern

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Blockieren von Cookies, die von Webseitenelementen stammen, die nicht zu der Domäne gehören, die sich in der Adressleiste befindet.

Wenn Sie diese Richtlinie aktivieren, können Webseitenelemente, die sich nicht in der Domäne befinden, die sich in der Adressleiste befindet, keine Cookies setzen.

Wenn Sie diese Richtlinie deaktivieren, können Webseitenelemente aus anderen Domänen als in der Adressleiste Cookies setzen.

Wenn Sie diese Richtlinie nicht konfigurieren, werden Cookies von Drittanbietern aktiviert, aber die Benutzer können diese Einstellung ändern.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: BlockThirdPartyCookies
  - GP-Name: Blockieren der Cookies von Drittanbietern
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): Administrative Templates/Microsoft Edge – Standardeinstellungen (Benutzer können diese außer Kraft setzen)/
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Wertname: BlockThirdPartyCookies
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000000
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: BlockThirdPartyCookies
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### BrowserAddProfileEnabled

  #### Aktivieren der Profilerstellung im Flyout „Identität“ oder auf der Seite „Einstellungen“

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Ermöglicht es Benutzern, neue Profile zu erstellen, indem Sie die Option **Profil hinzufügen** verwenden.
Wenn Sie diese Richtlinie aktivieren oder nicht konfigurieren, ermöglicht Microsoft Edge Benutzern, **Profil hinzufügen** im Identitäts-Flyoutmenü oder auf der Seite „Einstellungen“ zu verwenden, um neue Profile zu erstellen.

Wenn Sie diese Richtlinie deaktivieren, können Benutzer im Identitäts-Flyoutmenü oder auf der Seite "Einstellungen" keine neuen Profile hinzufügen.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: BrowserAddProfileEnabled
  - GP-Name: Aktivieren der Profilerstellung im Flyout „Identität“ oder auf der Seite „Einstellungen“
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: BrowserAddProfileEnabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: BrowserAddProfileEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### BrowserGuestModeEnabled

  #### Gastmodus aktivieren

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Aktiviert die Option, Gastprofile in Microsoft Edge zuzulassen. In einem Gastprofil importiert der Browser keine Browserdaten aus vorhandenen Profilen und löscht die Browserdaten, wenn alle Gastprofile geschlossen werden.

Wenn Sie diese Richtlinie aktivieren oder nicht konfigurieren, ermöglicht Microsoft Edge das Browsen in Gastprofilen.

Wenn Sie diese Richtlinie deaktivieren, lässt Microsoft Edge keine Benutzer in Gastprofilen browsen.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: BrowserGuestModeEnabled
  - GP-Name: Gastmodus aktivieren
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: BrowserGuestModeEnabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: BrowserGuestModeEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### BrowserNetworkTimeQueriesEnabled

  #### Abfragen an einen Browser Netzwerk-Zeitdienst zulassen

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Verhindert, dass Microsoft Edge gelegentlich Abfragen an einen Browser-Netzwerkzeitdienst sendet, um einen genauen Zeitstempel abzurufen.

Wenn Sie diese Richtlinie deaktivieren, unterlässt Microsoft Edge das Senden von Abfragen an einen Browser-Netzwerkzeitdienst.

Wenn Sie diese Richtlinie aktivieren oder nicht konfigurieren, sendet Microsoft Edge gelegentlich Abfragen an einen Browser-Netzwerkzeitdienst.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: BrowserNetworkTimeQueriesEnabled
  - GP-Name: Abfragen an einen Browser Netzwerk-Zeitdienst zulassen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: BrowserNetworkTimeQueriesEnabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: BrowserNetworkTimeQueriesEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### BrowserSignin

  #### Browser-Anmeldungseinstellungen

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Geben Sie an, ob sich ein Benutzer mit seinem Konto bei Microsoft Edge anmelden kann und kontobezogene Dienste wie Synchronisierung und einmaliges Anmelden verwenden kann. Wenn Sie die Verfügbarkeit der Synchronisierung steuern möchten, verwenden Sie stattdessen die [SyncDisabled](#syncdisabled)-Richtlinie.

Wenn Sie diese Richtlinie auf „Deaktivieren“ festlegen, stellen Sie sicher, dass Sie auch die Richtlinie[NonRemovableProfileEnabled](#nonremovableprofileenabled) auf „Deaktiviert“ setzen, da [NonRemovableProfileEnabled](#nonremovableprofileenabled) die Erstellung eines automatisch angemeldeten Browser-Profils deaktiviert. Wenn beide Richtlinien festgelegt sind, verwendet Microsoft Edge die Richtlinie "Browser-Anmeldung deaktivieren" und verhält sich, als ob [NonRemovableProfileEnabled](#nonremovableprofileenabled) auf deaktiviert festgelegt ist.

Wenn Sie diese Richtlinie auf „Aktivieren“ setzen, können sich die Benutzer im Browser anmelden. Das Anmelden beim Browser bedeutet nicht, dass die Synchronisierung standardmäßig aktiviert ist. Der Benutzer muss diesem Feature separat zustimmen.

Wenn Sie diese Richtlinie auf „Erzwingen“ setzen, müssen sich die Benutzer in einem Profil anmelden, um den Browser benutzen zu können. Auf diese Weise kann der Benutzer standardmäßig auswählen, ob er die Synchronisierung mit seinem Konto veranlassen möchte, es sei denn, die Synchronisierung wird vom Domänenadministrator oder mit der [SyncDisabled](#syncdisabled) Richtlinie deaktiviert. Der Standardwert für [BrowserGuestModeEnabled](#browserguestmodeenabled)-Richtlinie ist auf falsch festgelegt.

Wenn Sie diese Richtlinie nicht konfigurieren, können die Benutzer entscheiden, ob Sie die Browser-Anmeldeoption aktivieren und diese so verwenden, wie es für sie geeignet ist.

Zuordnung von Richtlinienoptionen:

* Disable (0) = Browser-Anmeldung deaktivieren

* Enable (1) = Browser-Anmeldung aktivieren

* Force (2) = erzwingen, dass Benutzer sich anmelden, um den Browser zu verwenden

Verwenden Sie die vorstehenden Informationen, wenn Sie diese Richtlinie konfigurieren.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Ganze Zahl

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: BrowserSignin
  - GP-Name: Browser-Anmeldungseinstellungen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: BrowserSignin
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000002
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: BrowserSignin
  - Beispielwert:
``` xml
<integer>2</integer>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### BuiltInDnsClientEnabled

  #### Verwenden des integrierten DNS-Clients

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Steuert, ob der integrierte DNS-Client verwendet werden soll.

Dies wirkt sich nicht darauf aus, welche DNS-Server verwendet werden, sondern nur auf den Softwarestapel, der für die Kommunikation verwendet wird. Wenn das Betriebssystem beispielsweise so konfiguriert ist, dass es einen Enterprise-DNS-Server verwendet, wird dieser Server auch vom integrierten DNS-Client verwendet. Es kann jedoch vorkommen, dass der integrierte DNS-Client Server auf unterschiedliche Weise ansprechen wird, da modernere DNS-bezogene Protokolle wie DNS-over-TLS verwendet werden können.

Wenn Sie diese Richtlinie aktivieren, wird der integrierte DNS-Client verwendet (sofern verfügbar).

Wenn Sie diese Richtlinie deaktivieren, wird der Client nie verwendet.

Wenn Sie diese Richtlinie nicht konfigurieren, ist der integrierte DNS-Client auf MacOS standardmäßig aktiviert, und die Benutzer können die Verwendung des integrierten DNS-Clients ändern, indem Sie die Edge://Flags bearbeiten oder eine Befehlszeilenkennzeichnung angeben.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: BuiltInDnsClientEnabled
  - GP-Name: Verwenden des integrierten DNS-Clients
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: BuiltInDnsClientEnabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: BuiltInDnsClientEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### BuiltinCertificateVerifierEnabled

  #### Bestimmt, ob die integrierte Zertifikatprüfung zum Überprüfen von Serverzertifikaten verwendet wird (veraltet)

  >VERALTET: Diese Richtlinie ist veraltet. Sie wird zurzeit unterstützt, aber in einer zukünftigen Version als veraltet behandelt.
  
  #### Unterstützte Versionen:

  - Auf macOS ab 83 oder höher

  #### Beschreibung

  Diese Richtlinie ist veraltet, da sie nur als kurzfristiger Mechanismus dienen soll, um Unternehmen mehr Zeit zu geben, ihre Umgebungen zu aktualisieren und Probleme zu melden, wenn sich herausstellt, dass sie mit der integrierten Zertifikatsprüfung nicht kompatibel sind.

Dies wird in der Microsoft Edge für Mac OS X-Version 87 nicht funktionieren, wenn die Entfernung der Unterstützung für die Legacy Zertifikatprüfung aus Microsoft Edge für Mac OS X geplant ist.


  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Boolesch

  

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: BuiltinCertificateVerifierEnabled
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### CertificateTransparencyEnforcementDisabledForCas

  #### Deaktivieren der Erzwingung der Zertifikattransparenz für eine Liste mit subjectPublicKeyInfo-Hashwerten

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Deaktiviert die Erzwingung der Zertifikattransparenz-Bedingungen für eine Liste mit subjectPublicKeyInfo-Hashwerten.

Mit dieser Richtlinie können Sie die Offenlegungsanforderungen für die Zertifikattransparenz für Zertifikatketten deaktivieren, die Zertifikate mit einem der angegebenen subjectPublicKeyInfo-Hashwerte enthalten. Auf diese Weise können Zertifikate, die andernfalls nicht vertrauenswürdig wären, da sie nicht ordnungsgemäß öffentlich offengelegt wurden, dennoch für Enterprise-Hosts verwendet werden.

Wenn Sie die Erzwingung der Zertifikattransparenz deaktivieren möchten, wenn diese Richtlinie festgelegt ist, muss eine der folgenden Bedingungen erfüllt sein:
1. Der Hash ist vom subjectPublicKeyInfo des Serverzertifikats.
2. Bei dem Hash handelt es sich um ein subjectPublicKeyInfo, das in einem Zertifizierungsstellenzertifikat in der Zertifikatkette angezeigt wird, das Zertifizierungsstellenzertifikat wird durch die X.509v3 nameConstraints-Erweiterung eingeschränkt, mindestens ein directoryName nameConstraints ist in permittedSubtrees vorhanden und der directoryName enthält ein organizationName-Attribut.
3. Bei dem Hash handelt es sich um ein subjectPublicKeyInfo, das in einem Zertifizierungsstellenzertifikat in der Zertifikatkette angezeigt wird, das Zertifizierungsstellenzertifikat verfügt über ein oder mehrere organizationName-Attribute im Zertifikatbetreff und das Serverzertifikat enthält die gleiche Anzahl von organizationName-Attributen, in der gleichen Reihenfolge und mit Byte-für-Byte identischen Werten.

Ein subjectPublicKeyInfo-Hashwert wird durch Verketten des Hashalgorithmusnamens, des "/"-Zeichens und der Base64-Kodierung des Hashwerts angegeben, der auf die DER-codierten subjectPublicKeyInfo des angegebenen Zertifikats angewendet wird. Diese Base64-Kodierung entspricht dem Format eines SPKI-Fingerabdrucks, wie in RFC 7469, Abschnitt 2.4 definiert. Nicht erkannte Hashalgorithmen werden ignoriert. Der einzige unterstützte Hashalgorithmus zu diesem Zeitpunkt ist „sha256“.

Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, wird jedes Zertifikat, für das eine Offenlegung mittels Zertifikattransparenz erforderlich ist als nicht vertrauenswürdig behandelt, falls es nicht entsprechend der Zertifikattransparenzrichtlinie offengelegt wurde.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Liste von Zeichenfolgen

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: CertificateTransparencyEnforcementDisabledForCas
  - GP-Name: Deaktivieren der Erzwingung der Zertifikattransparenz für eine Liste mit subjectPublicKeyInfo-Hashwerten
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForCas
  - Pfad (Empfohlen): n.a.
  - Wertname: 1, 2, 3, ...
  - Werttyp: REG_SZ-Liste

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForCas\1 = "sha256/AAAAAAAAAAAAAAAAAAAAAA=="
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForCas\2 = "sha256//////////////////////w=="

```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: CertificateTransparencyEnforcementDisabledForCas
  - Beispielwert:
``` xml
<array>
  <string>sha256/AAAAAAAAAAAAAAAAAAAAAA==</string>
  <string>sha256//////////////////////w==</string>
</array>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### CertificateTransparencyEnforcementDisabledForLegacyCas

  #### Deaktivieren der Erzwingung der Zertifikattransparenz für eine Liste mit Legacy-Zertifizierungsstellen

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Deaktiviert die Bedingung der Erzwingung der Zertifikattransparenz für eine Liste mit Legacy-Zertifizierungsstellen (CAs).

Mit dieser Richtlinie können Sie die Offenlegungsanforderungen für die Zertifikattransparenz für Zertifikatketten deaktivieren, die Zertifikate mit einem der angegebenen subjectPublicKeyInfo-Hashwerte enthalten. Auf diese Weise können Zertifikate, die andernfalls nicht vertrauenswürdig wären, da sie nicht ordnungsgemäß öffentlich offengelegt wurden, weiterhin für Enterprise-Hosts verwendet werden.

Damit die Erzwingung der Zertifikattransparenz deaktiviert wird, müssen Sie den Hashwert auf einen subjectPublicKeyInfo festlegen, der in einem Zertifizierungsstellenzertifikat angezeigt wird, das als Legacy-Zertifizierungsstelle anerkannt wird. Eine Legacy-Zertifizierungsstelle ist eine Zertifizierungsstelle, die standardmäßig von einem oder mehreren Betriebssystem als öffentlich vertrauenswürdig eingestuft wurde, die Microsoft Edge unterstützen.

Sie geben einen subjectPublicKeyInfo-Hashwert durch Verketten des Hashalgorithmusnamens, des "/"-Zeichens und der Base64-Kodierung des Hashwerts an, der auf die DER-codierten subjectPublicKeyInfo des angegebenen Zertifikats angewendet wird. Diese Base64-Kodierung entspricht dem Format eines SPKI-Fingerabdrucks, wie in RFC 7469, Abschnitt 2.4 definiert. Nicht erkannte Hashalgorithmen werden ignoriert. Der einzige unterstützte Hashalgorithmus zu diesem Zeitpunkt ist „sha256“.

Wenn Sie diese Richtlinie nicht konfigurieren, wird jedes Zertifikat, für das eine Offenlegung mittels Zertifikattransparenz erforderlich ist als nicht vertrauenswürdig behandelt, falls es nicht entsprechend der Zertifikattransparenzrichtlinie offengelegt wurde.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Liste von Zeichenfolgen

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: CertificateTransparencyEnforcementDisabledForLegacyCas
  - GP-Name: Deaktivieren der Erzwingung der Zertifikattransparenz für eine Liste mit Legacy-Zertifizierungsstellen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForLegacyCas
  - Pfad (Empfohlen): n.a.
  - Wertname: 1, 2, 3, ...
  - Werttyp: REG_SZ-Liste

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForLegacyCas\1 = "sha256/AAAAAAAAAAAAAAAAAAAAAA=="
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForLegacyCas\2 = "sha256//////////////////////w=="

```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: CertificateTransparencyEnforcementDisabledForLegacyCas
  - Beispielwert:
``` xml
<array>
  <string>sha256/AAAAAAAAAAAAAAAAAAAAAA==</string>
  <string>sha256//////////////////////w==</string>
</array>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### CertificateTransparencyEnforcementDisabledForUrls

  #### Deaktivieren der Erzwingung der Zertifikattransparenz für bestimmte URLs

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Deaktiviert die Erzwingung der Zertifikattransparenz für die aufgelisteten URLs.

Mit dieser Richtlinie können Sie Zertifikate für die Hostnamen in den angegebenen URLs nicht über die Zertifikattransparenz offenlegen. Auf diese Weise können Sie Zertifikate verwenden, die sonst nicht als vertrauenswürdig eingestuft würden, da sie nicht ordnungsgemäß öffentlich offen gelegt wurden, aber es erschwert das erkennen falsch ausgegebener Zertifikate für diese Hosts.

Erstellen Sie Ihr URL-Muster gemäß [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322). Da Zertifikate für einen angegebenen Hostnamen gültig sind, unabhängig vom Schema, Port oder Pfad, wird nur der Hostname der URLs berücksichtigt. Platzhalter-Hosts werden nicht unterstützt.

Wenn Sie diese Richtlinie nicht konfigurieren, wird jedes Zertifikat, das über die Zertifikattransparenz offengelegt werden sollte, als nicht vertrauenswürdig behandelt, wenn es nicht offengelegt wurde.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Liste von Zeichenfolgen

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: CertificateTransparencyEnforcementDisabledForUrls
  - GP-Name: Deaktivieren der Erzwingung der Zertifikattransparenz für bestimmte URLs
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForUrls
  - Pfad (Empfohlen): n.a.
  - Wertname: 1, 2, 3, ...
  - Werttyp: REG_SZ-Liste

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForUrls\1 = "contoso.com"
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForUrls\2 = ".contoso.com"

```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: CertificateTransparencyEnforcementDisabledForUrls
  - Beispielwert:
``` xml
<array>
  <string>contoso.com</string>
  <string>.contoso.com</string>
</array>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### ClearBrowsingDataOnExit

  #### Löschen der Browsingdaten beim Schließen von Microsoft Edge

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 78 oder höher

  #### Beschreibung

  Microsoft Edge löscht Browserdaten beim Schließen nicht standardmäßig. Browserdaten umfassen Informationen, die in Formulare eingegeben werden, Kennwörter und auch die besuchten Websites.

Wenn Sie diese Richtlinie aktivieren, werden alle Browserdaten jedes Mal gelöscht, wenn Microsoft Edge geschlossen wird. Beachten Sie, dass wenn Sie diese Richtlinie aktivieren, sie Vorrang vor Ihrer Konfiguration von [DefaultCookiesSetting](#defaultcookiessetting) hat.

Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, können Benutzer die Option zum Löschen von Browserdaten in den Einstellungen konfigurieren.

Wenn Sie diese Richtlinie aktivieren, konfigurieren Sie die [AllowDeletingBrowserHistory](#allowdeletingbrowserhistory) oder die [ClearCachedImagesAndFilesOnExit](#clearcachedimagesandfilesonexit) Richtlinie nicht, da diese sich alle mit dem Löschen von Browserdaten befassen. Wenn Sie die vorhergehenden Richtlinien und diese Richtlinie konfigurieren, werden alle Browserdaten gelöscht, wenn Microsoft Edge geschlossen wird – unabhängig davon, wie Sie [AllowDeletingBrowserHistory](#allowdeletingbrowserhistory) oder [ClearCachedImagesAndFilesOnExit](#clearcachedimagesandfilesonexit) konfiguriert haben.

Konfigurieren Sie die [SaveCookiesOnExit](#savecookiesonexit)-Richtlinie, um das Löschen von Cookies beim Beenden zu verhindern.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: ClearBrowsingDataOnExit
  - GP-Name: Löschen der Browsingdaten beim Schließen von Microsoft Edge
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): Administrative Templates/Microsoft Edge – Standardeinstellungen (Benutzer können diese außer Kraft setzen)/
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Wertname: ClearBrowsingDataOnExit
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: ClearBrowsingDataOnExit
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### ClearCachedImagesAndFilesOnExit

  #### Löschen von zwischengespeicherten Bildern und Dateien, wenn Microsoft Edge geschlossen wird

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 83 oder höher

  #### Beschreibung

  Microsoft Edge löscht Bilder und Dateien im Cache beim Schließen nicht standardmäßig.

Wenn Sie diese Richtlinie aktivieren, werden alle Bilder und Dateien im Cache jedes Mal gelöscht, wenn Microsoft Edge geschlossen wird.

Wenn Sie diese Richtlinie deaktivieren, können Benutzer die Option "Bilder und Dateien im Cache" in Edge://Settings/clearBrowsingDataOnClose nicht konfigurieren.

Wenn Sie diese Richtlinie nicht konfigurieren, können Benutzer auswählen, ob die zwischengespeicherten Bilder und Dateien beim Beenden gelöscht werden sollen.

Wenn Sie diese Richtlinie deaktivieren, aktivieren Sie die Richtlinie [ClearBrowsingDataOnExit](#clearbrowsingdataonexit) nicht, da sich beide auf das Löschen von Daten auswirken. Wenn Sie beide konfigurieren, hat die [ClearBrowsingDataOnExit](#clearbrowsingdataonexit)-Richtlinie Vorrang und löscht alle Daten, wenn Microsoft Edge geschlossen wird – unabhängig davon, wie [ClearCachedImagesAndFilesOnExit](#clearcachedimagesandfilesonexit) konfiguriert ist.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: ClearCachedImagesAndFilesOnExit
  - GP-Name: Löschen von zwischengespeicherten Bildern und Dateien, wenn Microsoft Edge geschlossen wird
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): Administrative Templates/Microsoft Edge – Standardeinstellungen (Benutzer können diese außer Kraft setzen)/
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Wertname: ClearCachedImagesAndFilesOnExit
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: ClearCachedImagesAndFilesOnExit
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### ClickOnceEnabled

  #### Benutzern das Öffnen von Dateien mithilfe des ClickOnce-Protokolls gestatten

  
  
  #### Unterstützte Versionen:

  - Auf Windows ab 78 oder höher

  #### Beschreibung

  Benutzern das Öffnen von Dateien mithilfe des ClickOnce-Protokolls gestatten. Mithilfe des ClickOnce-Protokolls können Websites fordern, dass der Browser Dateien aus einer bestimmten URL mit dem ClickOnce-Dateihandler auf dem Computer oder Gerät des Benutzers öffnet.

Wenn Sie diese Richtlinie aktivieren, können Benutzer Dateien mithilfe des ClickOnce-Protokolls öffnen. Diese Richtlinie setzt die ClickOnce-Einstellung des Benutzers auf der Seite Edge://Flags/ außer Kraft.

Wenn Sie diese Richtlinie deaktivieren, können Benutzer keine Dateien mithilfe des ClickOnce-Protokolls öffnen. Die Datei wird stattdessen vom Browser im Dateisystem gespeichert. Diese Richtlinie setzt die ClickOnce-Einstellung des Benutzers auf der Seite Edge://Flags/ außer Kraft.

Wenn Sie diese Richtlinie nicht konfigurieren, können Benutzer mit Microsoft Edge-Versionen vor Microsoft Edge 87 Dateien standardmäßig nicht mit dem ClickOnce-Protokoll öffnen. Benutzer haben jedoch die Möglichkeit, die Verwendung des ClickOnce-Protokolls auf der Seite edge://flags/ zu aktivieren. Benutzer mit Microsoft Edge Versionen 87 und höher können Dateien standardmäßig mit dem ClickOnce-Protokoll öffnen, haben aber auch die Möglichkeit, das ClickOnce-Protokoll über die Seite edge://flags/ zu deaktivieren.

Durch das Deaktivieren von ClickOnce wird ggf. verhindert, dass ClickOnce-Anwendungen (.application-Dateien) ordnungsgemäß gestartet werden.

Weitere Informationen zu ClickOnce finden Sie unter [https://go.microsoft.com/fwlink/?linkid=2103872](https://go.microsoft.com/fwlink/?linkid=2103872) und [https://go.microsoft.com/fwlink/?linkid=2099880](https://go.microsoft.com/fwlink/?linkid=2099880).

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: ClickOnceEnabled
  - GP-Name: Benutzern das Öffnen von Dateien mithilfe des ClickOnce-Protokolls gestatten
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: ClickOnceEnabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000000
```

  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### CollectionsServicesAndExportsBlockList

  #### Blockieren des Zugriffs auf eine bestimmte Liste von Diensten und Exportieren von Zielen in Sammlungen

  
  
  #### Unterstützte Versionen:

  - Unter Windows und macOS ab 86 oder höher

  #### Beschreibung

  Listen Sie bestimmte Dienste und Exportziele auf, auf die Benutzer in der Funktion „Sammlungen“ in Microsoft Edge nicht zugreifen können. Dazu gehören die Anzeige zusätzlicher Daten aus Bing und der Export von Sammlungen in Microsoft-Produkte oder zu externen Partnern.

Wenn Sie diese Richtlinie aktivieren, werden Dienste und Exportziele, die mit der angegebenen Liste übereinstimmen, blockiert.

Wenn Sie diese Richtlinie nicht konfigurieren, werden keine Beschränkungen für die zulässigen Dienstleistungen und Exportziele erzwungen.

Zuordnung von Richtlinienoptionen:

* pinterest_suggestions (pinterest_suggestions) = Pinterest-Vorschläge

* collections_share (collections_share) = Sammlungen freigeben

Verwenden Sie die vorstehenden Informationen, wenn Sie diese Richtlinie konfigurieren.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Liste von Zeichenfolgen

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - Eindeutiger GP-Name: CollectionsServicesAndExportsBlockList
  - GP-Name: Blockieren des Zugriffs auf eine bestimmte Liste von Diensten und Exportieren von Zielen in Sammlungen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (obligatorisch): SOFTWARE\Policies\Microsoft\Edge\CollectionsServicesAndExportsBlockList
  - Pfad (Empfohlen): n.a.
  - Wertname: 1, 2, 3, ...
  - Werttyp: REG_SZ-Liste

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\CollectionsServicesAndExportsBlockList\1 = "pinterest_suggestions"
SOFTWARE\Policies\Microsoft\Edge\CollectionsServicesAndExportsBlockList\2 = "collections_share"

```

  #### Mac – Informationen und Einstellungen
  
  - Name des Einstellungsschlüssels: CollectionsServicesAndExportsBlockList
  - Beispielwert:
``` xml
<array>
  <string>pinterest_suggestions</string>
  <string>collections_share</string>
</array>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### CommandLineFlagSecurityWarningsEnabled

  #### Aktivieren von Sicherheitswarnungen für Befehlszeilen Kennzeichnungen

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 78 oder höher

  #### Beschreibung

  Wenn diese Richtlinie deaktiviert ist, werden Sicherheitswarnungen beim Start von Microsoft Edge mit potenziell gefährlichen Befehlszeilenoptionen nicht angezeigt.

Wenn diese Option aktiviert oder nicht verwendet wird, werden Sicherheitswarnungen angezeigt, wenn diese Befehlszeilenoptionen zum Starten von Microsoft Edge verwendet werden.

So wird beispielsweise durch die Option --disable-gpu-sandbox die folgende Warnung erzeugt: Sie verwenden eine nicht unterstützte Befehlszeilenoption:--disable-gpu-sandbox. Dies birgt Stabilitäts- und Sicherheitsrisiken.

Diese Richtlinie ist nur für Windows-Instanzen verfügbar, die mit einer Microsoft Active Directory-Domäne verknüpft sind, Windows 10 Pro- oder Enterprise-Instanzen, die für die Geräteverwaltung registriert sind, oder MacOS-Instanzen, die über MDM verwaltet oder über MCX einer Domäne beigetreten sind.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: CommandLineFlagSecurityWarningsEnabled
  - GP-Name: Aktivieren von Sicherheitswarnungen für Befehlszeilen Kennzeichnungen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: CommandLineFlagSecurityWarningsEnabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: CommandLineFlagSecurityWarningsEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### ComponentUpdatesEnabled

  #### Aktivieren von Komponentenupdates in Microsoft Edge

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Wenn Sie diese Richtlinie aktivieren oder nicht konfigurieren, sind Komponentenupdates in Microsoft Edge aktiviert.

Wenn Sie diese Richtlinie deaktivieren oder auf falsch festlegen, werden die Komponentenupdates für alle Komponenten in Microsoft Edge deaktiviert.

Einige Komponenten sind jedoch von dieser Richtlinie ausgenommen. Dazu gehört jede Komponente, die keinen ausführbaren Code enthält, die das Browserverhalten nicht erheblich ändert oder die für die Sicherheit wichtig ist. Dies bedeutet, dass Updates, die als "sicherheitskritisch" eingestuft werden, weiterhin angewendet werden, auch wenn Sie diese Richtlinie deaktivieren.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: ComponentUpdatesEnabled
  - GP-Name: Aktivieren von Komponentenupdates in Microsoft Edge
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: ComponentUpdatesEnabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: ComponentUpdatesEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### ConfigureDoNotTrack

  #### DNT konfigurieren

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Legt fest, ob „Do Not Track“-Anforderungen an Websites gesendet werden sollen, die Nachverfolgungsinformationen anfordern. Do-Not-Track-Anforderungen lassen die Website, die Sie besuchen, wissen, dass Ihre Browseraktivitäten nicht nachverfolgt werden sollen. Microsoft Edge sendet standardmäßig keine Do-Not-Track-Anforderungen, aber die Benutzer können dieses Feature aktivieren, um sie zu senden.

Wenn Sie diese Richtlinie aktivieren, werden Do Not Track-Anforderungen (nicht verfolgen) immer an Websites gesendet, die Nachverfolgungsinformationen anfordern.

Wenn Sie diese Richtlinie deaktivieren, werden keine Anforderungen gesendet.

Wenn Sie die Richtlinie nicht konfigurieren, können die Benutzer auswählen, ob diese Anforderungen gesendet werden sollen.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: ConfigureDoNotTrack
  - GP-Name: DNT konfigurieren
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: ConfigureDoNotTrack
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000000
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: ConfigureDoNotTrack
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### ConfigureFriendlyURLFormat

  #### Konfigurieren des Standardformats für das Einfügen von URLs, die aus MicrosoftEdge kopiert wurden, und zum Ermitteln, ob Benutzern weitere Formate zur Verfügung stehen

  
  
  #### Unterstützte Versionen:

  - Unter Windows seit 87 oder später
  - Auf macOS ab 88 oder höher

  #### Beschreibung

  Wenn FriendlyURLs aktiviert ist, berechnet Microsoft Edge zusätzliche Darstellungen der URL und platziert Sie in der Zwischenablage.

Diese Richtlinie konfiguriert, welches Format beim Einfügen durch den Benutzers in externe Anwendungen oder innerhalb von Microsoft Edge ohne das Kontextmenüelement "Einfügen als" eingefügt wird.

Wenn diese Richtlinie konfiguriert ist, trifft sie eine Auswahl im Namen des Benutzers. Die Optionen in edge://settings/shareCopyPaste sind abgeblendet, und die Optionen im Kontextmenü "Einfügen als" stehen nicht zur Verfügung.

* Nicht konfiguriert = der Benutzer kann sein bevorzugtes Einfügeformat auswählen. Standardmäßig ist dies auf das benutzerfreundliche URL-Format festgelegt. Das Menü "Einfügen als" ist in Microsoft Edge verfügbar.

* 1 = In der Zwischenablage werden keine weiteren Formate gespeichert. Es wird in Microsoft Edge kein Kontextmenüelement "Einfügen als" vorhanden sein, und das einzige zum Einfügen verfügbare Format ist das Nur-Text-Format der URL. Das Feature für die benutzerfreundliche URL wird effektiv deaktiviert.

* 3 = Der Benutzer erhält eine benutzerfreundliche URL, wenn er in Oberflächen einfügt, die Rich-Text akzeptieren. Die Standard-URL steht weiterhin für Oberflächen zur Verfügung, die keinen Rich-Text akzeptieren. Das Menü "Einfügen als" wird in Microsoft Edge nicht verfügbar sein.

* 4 = (Zurzeit nicht verwendet)

Die umfangreicheren Formate werden in einigen Einfügezielen und / oder Websites möglicherweise nicht gut unterstützt. Wenn also diese Richtlinie konfiguriert werden soll, wird die Standard-URL-Option empfohlen.

Zuordnung von Richtlinienoptionen:

* PlainText (1) = die Standard-URL ohne zusätzliche Informationen wie z. B. den Titel der Seite. Dies ist die empfohlene Option, wenn diese Richtlinie konfiguriert wird. Weitere Informationen finden Sie in der Beschreibung.

* TitledHyperlink (3) = Betitelter Link: Ein Link, der auf die kopierte URL zeigt, dessen sichtbarer Text aber der Titel der Zielseite ist. Dies ist das benutzerfreundliche URL-Format.

* WebPreview (4) = in Kürze verfügbar. Wenn aktiviert, verhält es sich wie die „Standard-URL“.

Verwenden Sie die vorstehenden Informationen, wenn Sie diese Richtlinie konfigurieren.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Ganze Zahl

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - Eindeutiger GP-Name: ConfigureFriendlyURLFormat
  - GP-Name: Konfigurieren des Standardformats für das Einfügen von URLs, die aus MicrosoftEdge kopiert wurden, und zum Ermitteln, ob Benutzern weitere Formate zur Verfügung stehen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: ConfigureFriendlyURLFormat
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000003
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: ConfigureFriendlyURLFormat
  - Beispielwert:
``` xml
<integer>3</integer>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### ConfigureOnPremisesAccountAutoSignIn

  #### Konfiguration der automatischen Anmeldung mit einem Active Directory-Domänenkonto, wenn kein Azure AD-Domänenkonto vorhanden ist

  
  
  #### Unterstützte Versionen:

  - Auf Windows ab 81 oder höher

  #### Beschreibung

  Aktiviert die Verwendung von Active Directory-Konten für die automatische Anmeldung, wenn die Computer Ihrer Benutzer domänenverbunden sind und Ihre Umgebung nicht hybridverbunden ist. Wenn Sie möchten, dass Benutzer stattdessen automatisch mit ihren Azure Active Directory-Konten angemeldet werden, stellen Sie Ihre Umgebung bitte auf Azure AD-Anmeldung (Weitere Informationen finden Sie unter [https://go.microsoft.com/fwlink/?linkid=2118197](https://go.microsoft.com/fwlink/?linkid=2118197)) oder Hybridverbindung (Weitere Informationen finden Sie unter [https://go.microsoft.com/fwlink/?linkid=2118365](https://go.microsoft.com/fwlink/?linkid=2118365) Weitere Informationen) um.

Wenn Sie die [BrowserSignin](#browsersignin) Richtlinie auf deaktiviert konfiguriert haben, wird diese Richtlinie nicht wirksam.

Wenn Sie diese Richtlinie aktivieren und auf „SignInAndMakeDomainAccountNonRemovable“ setzen, meldet Microsoft Edge Benutzer automatisch an, die sich auf einem domänenverbundenen Computer befinden und ihr Active Directory-Konto verwenden.

Wenn Sie diese Richtlinie auf „Disabled“ setzen oder sie nicht festlegen, meldet Microsoft Edge nicht automatisch Benutzer an, die sich auf einem domänenverbundenen Computer mit Active Directory-Konto befinden.

Zuordnung von Richtlinienoptionen:

* Disabled (0) = deaktiviert

* SignInAndMakeDomainAccountNonRemovable (1) = anmelden und Domain-Konto auf „nicht entfernbar“ setzen

Verwenden Sie die vorstehenden Informationen, wenn Sie diese Richtlinie konfigurieren.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Ganze Zahl

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: ConfigureOnPremisesAccountAutoSignIn
  - GP-Name: Konfiguration der automatischen Anmeldung mit einem Active Directory-Domänenkonto, wenn kein Azure AD-Domänenkonto vorhanden ist
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: ConfigureOnPremisesAccountAutoSignIn
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000000
```

  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### ConfigureOnlineTextToSpeech

  #### Konfiguration von Text-zu-Sprache Online

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Legen Sie fest, ob der Browser die Sprachfonts von „Online Text zu Sprache“, Teil von Azure Cognitive Services, verwenden kann. Diese Sprachfonts besitzen eine höhere Qualität als die vorinstallierten System-Sprachfonts.

Wenn Sie diese Richtlinie aktivieren oder nicht konfigurieren, können webbasierte Anwendungen, die die SpeechSynthesis-API nutzen, Online Text-zu-Sprache Sprachfonts verwenden.

Wenn Sie diese Richtlinie deaktivieren, sind die Sprachfonts nicht verfügbar.

Hier finden Sie weitere Informationen zu diesem Feature: SpeechSynthesis-API: [https://go.microsoft.com/fwlink/?linkid=2110038](https://go.microsoft.com/fwlink/?linkid=2110038) Cognitive Services: [https://go.microsoft.com/fwlink/?linkid=2110141](https://go.microsoft.com/fwlink/?linkid=2110141)

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: ConfigureOnlineTextToSpeech
  - GP-Name: Konfiguration von Text-zu-Sprache Online
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: ConfigureOnlineTextToSpeech
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: ConfigureOnlineTextToSpeech
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### ConfigureShare

  #### Konfiguration der Freigabeoberfläche

  
  
  #### Unterstützte Versionen:

  - Auf Windows ab 83 oder höher

  #### Beschreibung

  Wenn Sie diese Richtlinie auf „ShareAllowed“ setzen, können die Benutzer über das Menü „Einstellungen und mehr“ in Microsoft Edge auf die Windows 10-Freigabeumgebung zugreifen, um an andere Apps im System zu freizugeben.

Wenn Sie diese Richtlinie auf „ShareDisallowed“ setzen, können die Benutzer nicht mehr auf die Windows 10-Freigabeumgebung zugreifen. Wenn sich die Schaltfläche "Freigeben" auf der Symbolleiste befindet, wird sie ebenfalls ausgeblendet.

Zuordnung von Richtlinienoptionen:

* ShareAllowed (0) = Verwendung der Freigabeoberfläche zulassen

* ShareDisallowed (1) = Verwendung der Freigabeoberfläche nicht zulassen

Verwenden Sie die vorstehenden Informationen, wenn Sie diese Richtlinie konfigurieren.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Ganze Zahl

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: ConfigureShare
  - GP-Name: Konfiguration der Freigabeoberfläche
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: ConfigureShare
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### CustomHelpLink

  #### Benutzerdefinierten „Hilfe“-Link konfigurieren

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 79 oder höher

  #### Beschreibung

  Angeben eines Links für das Menü "Hilfe" oder "F1".

Wenn Sie diese Richtlinie aktivieren, kann ein Administrator einen Link für das Menü "Hilfe" oder die Taste "F1" angeben.

Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, wird der Standardlink für das Menü "Hilfe" oder "F1" verwendet.

Diese Richtlinie ist nur für Windows-Instanzen verfügbar, die mit einer Microsoft Active Directory-Domäne verknüpft sind, Windows 10 Pro- oder Enterprise-Instanzen, die für die Geräteverwaltung registriert sind, oder MacOS-Instanzen, die über MDM verwaltet oder über MCX einer Domäne beigetreten sind.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Zeichenfolge

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: CustomHelpLink
  - GP-Name: Benutzerdefinierten „Hilfe“-Link konfigurieren
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: CustomHelpLink
  - Werttyp: REG_SZ

  ##### Beispielwert:

```
"https://go.microsoft.com/fwlink/?linkid=2080734"
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: CustomHelpLink
  - Beispielwert:
``` xml
<string>https://go.microsoft.com/fwlink/?linkid=2080734</string>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### DNSInterceptionChecksEnabled

  #### DNS-Interception-Prüfungen aktiviert

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 80 oder höher

  #### Beschreibung

  Diese Richtlinie konfiguriert einen lokalen Schalter, der verwendet werden kann, um DNS-Interception-Prüfungen zu deaktivieren. Bei diesen Prüfungen wird versucht, zu ermitteln, ob sich der Browser hinter einem Proxy befindet, der unbekannte Hostnamen umleitet.

Diese Erkennung ist in einer Unternehmensumgebung, in der die Netzwerkkonfiguration bekannt ist, möglicherweise nicht erforderlich. Er kann deaktiviert werden, um zusätzlichen DNS- und HTTP-Datenverkehr beim Start und bei jeder Änderung der DNS-Konfiguration zu vermeiden.

Wenn Sie diese Richtlinie aktivieren oder nicht festlegen, werden die DNS-Abfangprüfungen durchgeführt.

Wenn Sie diese Richtlinie deaktivieren, werden DNS-Abfangprüfungen nicht ausgeführt.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: DNSInterceptionChecksEnabled
  - GP-Name: DNS-Interception-Prüfungen aktiviert
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: DNSInterceptionChecksEnabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: DNSInterceptionChecksEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### DefaultBrowserSettingEnabled

  #### Festlegen von Microsoft Edge als Standardbrowser

  
  
  #### Unterstützte Versionen:

  - Auf Windows 7 und macOS ab 77 oder höher

  #### Beschreibung

  Wenn Sie diese Richtlinie auf "wahr" festlegen, überprüft Microsoft Edge beim Start immer, ob es als Standardbrowser eingestellt ist und registriert sich, wenn möglich, automatisch.

Wenn Sie diese Richtlinie auf "falsch" festlegen, wird Microsoft Edge gestoppt, je nachdem, ob es sich um die standardmäßige Einstellung handelt.

Wenn Sie diese Richtlinie nicht festlegen, können die Benutzer von Microsoft Edge steuern, ob es sich um die Standardeinstellung handelt und, falls nicht, ob Benutzer Benachrichtigungen angezeigt werden sollen.

Hinweis für Windows-Administratoren: Diese Richtlinie funktioniert nur für PCs unter Windows 7. In späteren Versionen von Windows müssen Sie eine "Standard-Anwendungszuordnungen"-Datei bereitstellen, die Microsoft Edge als Handler für die HTTPS- und HTTP-Protokolle (und optional das FTP-Protokoll und Dateiformate wie .html, htm, .pdf, .svg, .webp) festlegt. Weitere Informationen finden Sie unter [https://go.microsoft.com/fwlink/?linkid=2094932](https://go.microsoft.com/fwlink/?linkid=2094932).

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: DefaultBrowserSettingEnabled
  - GP-Name: Festlegen von Microsoft Edge als Standardbrowser
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: DefaultBrowserSettingEnabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: DefaultBrowserSettingEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### DefaultSearchProviderContextMenuAccessAllowed

  #### Zugriff auf das Kontextmenü des Standardsuchanbieters zulassen

  
  
  #### Unterstützte Versionen:

  - Auf Windows und MacOS ab 85 oder später

  #### Beschreibung

  Aktiviert die Verwendung eines standardmäßigen Suchdienstanbieters im Kontextmenü.

Wenn Sie diese Richtlinie auf „Disabled“ setzen, sind der Eintrag im Suchkontextmenü, der sich auf Ihren standardmäßigen Suchdienstanbieter stützt und die Suche in der Seitenleiste sind nicht verfügbar.

Wenn diese Richtlinie auf „Enabled“ gesetzt oder nicht eingestellt ist, ist das Element des Kontextmenüs für den standardmäßigen Suchdienstanbieter und die Suche in der Seitenleiste verfügbar.

Der Wert für die Richtlinie wird nur dann angewendet, wenn die Richtlinie „[DefaultSearchProviderEnabled](#defaultsearchproviderenabled)“ aktiviert ist und ist ansonsten nicht anwendbar.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - Eindeutiger PGP-Name: DefaultSearchProviderContextMenuAccessAllowed
  - GP-Name: Dem standardmäßigen Suchdienstanbieter Zugriff auf die Kontextmenüsuche gewähren
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: DefaultSearchProviderContextMenuAccessAllowed
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Name des Einstellungsschlüssels: DefaultSearchProviderContextMenuAccessAllowed
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### DefaultSensorsSetting

  #### Standardeinstellung für Sensoren

  
  
  #### Unterstützte Versionen:

  - Unter Windows und macOS ab 86 oder höher

  #### Beschreibung

  Legen Sie fest, ob Websites auf Sensoren wie Bewegungs- und Lichtsensoren zugreifen und diese verwenden dürfen. Sie können den Zugriff auf Sensoren für Websites vollständig zulassen oder blockieren.

Wenn Sie die Richtlinie auf "1" festlegen, können Websites auf Sensoren zugreifen und diese verwenden. Wenn Sie die Richtlinie auf "2" festlegen, wird der Zugriff auf Sensoren verweigert.

Sie können diese Richtlinie für bestimmte URL-Muster außer Kraft setzen, indem Sie die [SensorsAllowedForUrls](#sensorsallowedforurls)- und [SensorsBlockedForUrls](#sensorsblockedforurls)-Richtlinien verwenden.

Wenn Sie diese Richtlinie nicht konfigurieren, können Websites auf Sensoren zugreifen und diese verwenden, und der Benutzer kann diese Einstellung ändern. Hierbei handelt es sich um die globale Standardeinstellung für [SensorsAllowedForUrls](#sensorsallowedforurls) und [SensorsBlockedForUrls](#sensorsblockedforurls).

Zuordnung von Richtlinienoptionen:

* AllowSensors (1) = Websites dürfen auf Sensoren zugreifen

* BlockSensors (2) = Websites dürfen nicht auf Sensoren zugreifen

Verwenden Sie die vorstehenden Informationen, wenn Sie diese Richtlinie konfigurieren.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Ganze Zahl

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - Eindeutiger GP-Name: DefaultSensorsSetting
  - GP-Name: Standardeinstellung für Sensoren
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: DefaultSensorsSetting
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000002
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: DefaultSensorsSetting
  - Beispielwert:
``` xml
<integer>2</integer>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### DefaultSerialGuardSetting

  #### Steuerung der Verwendung der Serial-API

  
  
  #### Unterstützte Versionen:

  - Unter Windows und macOS ab 86 oder höher

  #### Beschreibung

  Legen Sie fest, ob Websites auf serielle Anschlüsse zugreifen dürfen. Sie können den Zugriff vollständig blockieren oder festlegen, dass der Benutzer jedes Mal gefragt wird, wenn eine Website auf einen seriellen Anschluss zugreifen möchte.

Wenn Sie die Richtlinie auf "3" festlegen, können Websites Zugriff auf serielle Anschlüsse anfordern. Wenn Sie die Richtlinie auf "2" festlegen, wird der Zugriff auf serielle Anschlüsse verweigert.

Sie können diese Richtlinie für bestimmte URL-Muster außer Kraft setzen, indem Sie die [SerialAskForUrls](#serialaskforurls)- und [SerialBlockedForUrls](#serialblockedforurls)-Richtlinien verwenden.

Wenn Sie diese Richtlinie nicht konfigurieren, können Websites Benutzer standardmäßig fragen, ob sie auf serielle Anschlüsse zugreifen können, und die Benutzer können diese Einstellung ändern.

Zuordnung von Richtlinienoptionen:

* BlockSerial (2) = nicht zulassen, dass eine Website Zugriff auf serielle Anschlüsse über die Serial API anfordert

* AskSerial (3) = Websites gestatten, Benutzerberechtigungen für den Zugriff auf einen seriellen Anschluss anzufordern

Verwenden Sie die vorstehenden Informationen, wenn Sie diese Richtlinie konfigurieren.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Ganze Zahl

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - Eindeutiger GP-Name: DefaultSerialGuardSetting
  - GP-Name: Steuern der Verwendung der Serial-API
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: DefaultSerialGuardSetting
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000002
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: DefaultSerialGuardSetting
  - Beispielwert:
``` xml
<integer>2</integer>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### DelayNavigationsForInitialSiteListDownload

  #### Voraussetzen, dass die Enterprise Mode Site List vor der Registerkartennavigation verfügbar ist

  
  
  #### Unterstützte Versionen:

  - Unter Windows seit 84 oder später

  #### Beschreibung

  Sie können angeben, ob die Microsoft Edge-Registerkarten warten, bis der Browser die anfängliche Enterprise Mode Site List heruntergeladen hat. Diese Einstellung ist für das Szenario vorgesehen, in dem die Browser Startseite im Internet Explorer-Modus geladen werden soll, und es ist wichtig, dass dies im Browser zuerst ausgeführt wird, nachdem der IE-Modus aktiviert ist. Wenn dieses Szenario nicht vorhanden ist, empfiehlt es sich, diese Einstellung nicht zu aktivieren, da sich dies negativ auf die Leistung des Ladens der Startseite auswirken kann. Die Einstellung gilt nur, wenn Microsoft Edge nicht über eine im Cache des Enterprise Mode Site List verfügt, z. b. auf dem Browser erst ausgeführt wird, nachdem der IE-Modus aktiviert ist.

Diese Einstellung funktioniert in Verbindung mit: [InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) auf „IEMode“ und der Richtlinie „[InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist)“, wenn die Liste mindestens einen Eintrag hat.

Das Timeout-Verhalten dieser Richtlinie kann mit der Richtlinie für [NavigationDelayForInitialSiteListDownloadTimeout-](#navigationdelayforinitialsitelistdownloadtimeout) konfiguriert werden.

Wenn Sie diese Richtlinie auf „All“ setzen und Microsoft Edge nicht über eine zwischengespeicherte Version der Enterprise Mode Site List verfügt, verzögern Registerkarten die Navigation, bis der Browser die Seitenliste heruntergeladen hat. Websites, die so konfiguriert sind, dass Sie über die Siteliste im Internet Explorer-Modus geöffnet werden, werden im Internet Explorer-Modus geladen, auch während der anfänglichen Navigation im Browser. Websites, die möglicherweise nicht so konfiguriert werden, dass sie in Internet Explorer geöffnet werden, z.B. jegliche Websites mit einem anderen Schema als http:, https:, file: oder ftp: zögern nicht beim Navigieren und laden sofort im Edge-Modus.

Wenn Sie diese Richtlinie auf „None“ setzen oder sie nicht konfigurieren und Microsoft Edge nicht über eine zwischengespeicherte Version der Enterprise Mode Site List verfügt, navigieren die Registerkarten sofort und warten nicht darauf, dass der Browser die Enterprise Mode Site List heruntergeladen hat. Websites, die so konfiguriert sind, dass sie über die Siteliste im Internet Explorer-Modus geöffnet werden, werden im Microsoft Edge-Modus geöffnet, bis der Browser den Download der Enterprise Mode Site List abgeschlossen hat.

Zuordnung von Richtlinienoptionen:

* None (0) = keine

* All (1) = alle geeigneten Navigationselemente

Verwenden Sie die vorstehenden Informationen, wenn Sie diese Richtlinie konfigurieren.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Ganze Zahl

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - Eindeutiger Name des GP: DelayNavigationsForInitialSiteListDownloadvigationsForInitialSiteListDownload
  - GP-Name: Voraussetzen, dass die Enterprise Mode Site List vor der Registerkartennavigation verfügbar ist
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: DelayNavigationsForInitialSiteListDownload
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### DeleteDataOnMigration

  #### Löschen alter Browserdaten bei der Migration

  
  
  #### Unterstützte Versionen:

  - Auf Windows ab 83 oder höher

  #### Beschreibung

  Diese Richtlinie bestimmt, ob Benutzerdaten aus Microsoft Edge Legacy nach der Migration zur Microsoft Edge-Version 81 oder höher gelöscht werden.

Wenn Sie diese Richtlinie auf "aktiviert" festlegen, werden alle Browserdaten aus Microsoft Edge Legacy nach der Migration zur Microsoft Edge-Version 81 oder höher gelöscht. Diese Richtlinie muss festgelegt werden, bevor Sie zu Microsoft Edge Version 81 oder höher migrieren, um sich auf die vorhandenen Browserdaten auszuwirken.

Wenn Sie diese Richtlinie auf "deaktiviert" festlegen oder die Richtlinie nicht konfiguriert ist, werden die Benutzerdaten nach der Migration zur Microsoft Edge-Version 83 oder höher nicht gelöscht.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: DeleteDataOnMigration
  - GP-Name: Löschen alter Browserdaten bei der Migration
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: DeleteDataOnMigration
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000000
```

  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### DeveloperToolsAvailability

  #### Steuern, wo Entwicklertools verwendet werden können

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Steuert, wo Entwicklertools verwendet werden können.

Wenn Sie diese Richtlinie auf „DeveloperToolsDisallowedForForceInstalledExtensions“ setzen, können die Benutzer auf die Entwicklertools und die JavaScript-Konsole im Allgemeinen zugreifen, aber nicht im Rahmen von Erweiterungen, die von der Unternehmensrichtlinie installiert werden.

Wenn Sie diese Richtlinie auf „DeveloperToolsAllowed“ setzen, können die Benutzer grundsätzlich auf die Entwicklertools und die JavaScript-Konsole zugreifen, einschließlich der von Unternehmensrichtlinien installierten Erweiterungen.

Wenn Sie diese Richtlinie auf „DeveloperToolsDisallowed“ setzen, können die Benutzer nicht auf die Entwicklertools zugreifen oder die Elemente von Websiten prüfen. Die Tastenkombinationen und Menü- oder Kontextmenüeinträge, die die Entwicklertools oder die JavaScript-Konsole öffnen, sind deaktiviert.

Zuordnung von Richtlinienoptionen:

* DeveloperToolsDisallowedForForceInstalledExtensions (0) = Blockieren der Entwicklertools für Erweiterungen, die von der Enterprise-Richtlinie installiert wurden, in anderen Kontexten zulassen

* DeveloperToolsAllowed (1) = Entwicklertools zulassen

* DeveloperToolsAllowed (2) = Entwicklertools nicht zulassen

Verwenden Sie die vorstehenden Informationen, wenn Sie diese Richtlinie konfigurieren.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Ganze Zahl

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: DeveloperToolsAvailability
  - GP-Name: Steuern, wo Entwicklertools verwendet werden können
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: DeveloperToolsAvailability
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000002
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: DeveloperToolsAvailability
  - Beispielwert:
``` xml
<integer>2</integer>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### DiagnosticData

  #### Senden erforderlicher und optionaler Diagnosedaten zur Browsernutzung

  
  
  #### Unterstützte Versionen:

  - Unter Windows 7 und MacOS ab 86 oder höher

  #### Beschreibung

  Diese Richtlinie steuert das Senden der erforderlichen und optionalen Diagnosedaten zur Browsernutzung an Microsoft.

Erforderliche Diagnosedaten werden gesammelt, um Microsoft Edge sicher, aktuell und erwartungsgemäß zu halten.

Zu den optionalen Diagnosedaten gehören Daten zur Verwendung des Browsers, von Ihnen besuchte Websites und Absturzberichte an Microsoft zur Verbesserung von Produkten und Diensten.

Diese Richtlinie wird auf Windows 10-Geräten nicht unterstützt. Um diese Datenerfassung unter Windows 10 zu steuern, müssen IT-Administratoren die Windows-Diagnosedaten-Gruppenrichtlinie verwenden. Diese Richtlinie lautet je nach Windows-Version entweder "Telemetrie zulassen" oder "Diagnosedaten zulassen". Weitere Informationen zur Windows 10-Diagnosedatenerfassung:[https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569)

Verwenden Sie eine der folgenden Einstellungen, um diese Richtlinie zu konfigurieren:

'Aus' deaktiviert die erforderliche und optionale Diagnosedatenerfassung. Diese Option wird nicht empfohlen.

'RequiredData' sendet die erforderlichen Diagnosedaten, deaktiviert jedoch die optionale Diagnosedatenerfassung. Microsoft Edge sendet die erforderlichen Diagnosedaten, um Microsoft Edge sicher, aktuell und erwartungsgemäß zu halten.

'OptionalData' sendet optionale Diagnosedaten, einschließlich Daten zur Browsernutzung, besuchten Websites und Absturzberichten, die zur Produkt- und Serviceverbesserung an Microsoft gesendet werden.

Unter Windows 7/macOS steuert diese Richtlinie das Senden der erforderlichen und optionalen Daten an Microsoft.

Wenn Sie diese Richtlinie nicht konfigurieren oder deaktivieren, verwendet Microsoft Edge standardmäßig die Einstellungen des Benutzers.

Zuordnung von Richtlinienoptionen:

* Aus (0) = Aus (Nicht empfohlen)

* RequiredData (1) = Erforderliche Daten

* OptionalData (2) = Optionale Daten

Verwenden Sie die vorstehenden Informationen, wenn Sie diese Richtlinie konfigurieren.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Ganze Zahl

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - Eindeutiger Name der GP: DiagnosticData
  - GP-Name: Senden Sie die erforderlichen und optionalen Diagnosedaten zur Browsernutzung
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: DiagnosticData
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000002
```

  #### Mac – Informationen und Einstellungen
  
  - Name des Einstellungsschlüssels: DiagnosticData
  - Beispielwert:
``` xml
<integer>2</integer>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### DirectInvokeEnabled

  #### Benutzern das Öffnen von Dateien mithilfe des DirectInvoke-Protokolls gestatten

  
  
  #### Unterstützte Versionen:

  - Auf Windows ab 78 oder höher

  #### Beschreibung

  Benutzern das Öffnen von Dateien mithilfe des DirectInvoke-Protokolls gestatten. Mithilfe des DirectInvoke-Protokolls können Websites fordern, dass der Browser Dateien aus einer bestimmten URL mit einem bestimmten Dateihandler auf dem Computer oder Gerät des Benutzers öffnet.

Wenn Sie diese Richtlinie aktivieren oder nicht konfigurieren, können Benutzer Dateien mit dem DirectInvoke-Protokoll öffnen.

Wenn Sie diese Richtlinie deaktivieren, können Benutzer keine Dateien mithilfe des DirectInvoke-Protokolls öffnen. Die Datei wird stattdessen im Dateisystem gespeichert.

Hinweis: durch das Deaktivieren von DirectInvoke können bestimmte Microsoft SharePoint Online-Features nicht erwartungsgemäß funktionieren.

Weitere Informationen zu DirectInvoke finden Sie unter [https://go.microsoft.com/fwlink/?linkid=2103872](https://go.microsoft.com/fwlink/?linkid=2103872) und [https://go.microsoft.com/fwlink/?linkid=2099871](https://go.microsoft.com/fwlink/?linkid=2099871).

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: DirectInvokeEnabled
  - GP-Name: Benutzern das Öffnen von Dateien mithilfe des DirectInvoke-Protokolls gestatten
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: DirectInvokeEnabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000000
```

  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### Disable3DAPIs

  #### Deaktivieren der Unterstützung für 3D-Grafik-APIs

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Verhindern, dass Webseiten auf die GPU (Grafikkarte/ -prozessor) zugreifen. Speziell können Webseiten nicht auf die WebGL-API zugreifen und Plug-Ins können die Pepper 3D-API nicht verwenden.

Wenn Sie diese Richtlinie nicht konfigurieren oder deaktivieren, ist es möglich, dass Webseiten mithilfe der WebGL-API und Plug-ins die Pepper 3D-API verwenden können. Microsoft Edge kann in der Standardeinstellung weiterhin Befehlszeilenargumente zur Verwendung dieser APIs erforderlich machen.

Wenn die [HardwareAccelerationModeEnabled](#hardwareaccelerationmodeenabled)-Richtlinie auf falsch festgelegt ist, wird die Einstellung für die "Disable3DAPIs"-Richtlinie ignoriert – das entspricht der Einstellung von "Disable3DAPIs" auf "true".

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: Disable3DAPIs
  - GP-Name: Deaktivieren der Unterstützung für 3D-Grafik-APIs
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: Disable3DAPIs
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000000
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: Disable3DAPIs
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### DisableScreenshots

  #### Deaktivieren der Anfertigung von Screenshots

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Steuert, ob Benutzer Screenshots der Browserseite erstellen können.

Wenn diese Option aktiviert ist, können Benutzer keine Screenshots mithilfe von Tastenkombinationen oder Erweiterungs-APIs erstellen.

Wenn diese Richtlinie deaktiviert oder nicht konfiguriert wird, können die Benutzer Screenshots erstellen.

Bitte beachten Sie, dass diese Richtlinie sich auf Screenshots auswirkt, die im Browser selbst aufgenommen werden. Auch wenn Sie diese Richtlinie aktivieren, können die Benutzer möglicherweise weiterhin Screenshots erstellen, wenn sie dazu eine Methode außerhalb des Browsers verwenden (wie die Verwendung eines Betriebssystem-Features oder einer anderen Anwendung).

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: DisableScreenshots
  - GP-Name: Deaktivieren der Anfertigung von Screenshots
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: DisableScreenshots
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: DisableScreenshots
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### DiskCacheDir

  #### Festlegen des Datenträgercache Verzeichnisses

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Konfiguriert das Verzeichnis, das zum Speichern zwischengespeicherter Dateien verwendet werden soll.

Wenn Sie diese Richtlinie aktivieren, verwendet Microsoft Edge das bereitgestellte Verzeichnis unabhängig davon, ob der Benutzer das Flag "--disk-cache-dir" festgelegt hat. Zum Vermeiden von Datenverlust oder anderen unerwarteten Fehlern konfigurieren Sie diese Richtlinie nicht auf das Stammverzeichnis eines Volumes oder auf ein Verzeichnis, das für andere Zwecke verwendet wird, da Microsoft Edge dessen Inhalte verwaltet.

Eine Liste der Variablen, die Sie beim Angeben von Verzeichnissen und Pfaden verwenden können, finden Sie unter [https://go.microsoft.com/fwlink/?linkid=2095041](https://go.microsoft.com/fwlink/?linkid=2095041).

Wenn Sie diese Richtlinie nicht konfigurieren, wird das standardmäßige Cacheverzeichnis verwendet, und die Benutzer können diese Standardeinstellung außer Kraft setzen, indem Sie das Befehlszeilenkennzeichen "--disk-cache-dir" verwenden.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Zeichenfolge

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: DiskCacheDir
  - GP-Name: Festlegen des Datenträgercache Verzeichnisses
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: DiskCacheDir
  - Werttyp: REG_SZ

  ##### Beispielwert:

```
"${user_home}/Edge_cache"
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: DiskCacheDir
  - Beispielwert:
``` xml
<string>${user_home}/Edge_cache</string>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### DiskCacheSize

  #### Festlegen der Datenträgercachegröße, in Bytes

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Konfiguriert die Cachegröße (in Bytes), die zum Speichern von Dateien auf dem Datenträger verwendet wird.

Wenn Sie diese Richtlinie aktivieren, verwendet Microsoft Edge die bereitgestellte Cachegröße unabhängig davon, ob der Benutzer das Flag "--disk-cache-size" festgelegt hat. Der Wert, der in dieser Richtlinie angegeben ist, ist keine feste Grenze, sondern ein Vorschlag für das Cachingsystem. Ein Wert geringer als einige Megabytes ist zu klein und wird auf ein vertretbares Minimum gerundet.

Wenn Sie den Wert dieser Richtlinie auf "0" festlegen, wird die Standardcachegröße verwendet, und die Benutzer können diese nicht ändern.

Wenn Sie diese Richtlinie nicht konfigurieren, wird die Standardgröße verwendet, aber die Benutzer können sie mit dem Flag "--disk-cache-size" außer Kraft setzen.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Ganze Zahl

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: DiskCacheSize
  - GP-Name: Festlegen der Datenträgercachegröße, in Bytes
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: DiskCacheSize
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x06400000
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: DiskCacheSize
  - Beispielwert:
``` xml
<integer>104857600</integer>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### DnsOverHttpsMode

  #### Steuern des Modus von „DNS-over-HTTPS“

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 83 oder höher

  #### Beschreibung

  Steuern des Modus des „DNS-over-HTTPS“-Resolvers. Beachten Sie, dass mit dieser Richtlinie nur der Standardmodus für jede Abfrage festgelegt wird. Der Modus kann für spezielle Arten von Abfragen überschrieben werden, z.B. Anforderungen zum Auflösen eines DNS-over-HTTPS-Server-Hostnamens.

Der Modus "Aus" deaktiviert DNS-over-HTTPS.

Der Modus "automatisch" sendet DNS-over-HTTPS-Abfragen erst, wenn ein DNS-over-HTTPS-Server verfügbar ist, und er kann beim Auftreten eines Fehlers auf das Senden von unsicheren Abfragen zurückgreifen.

Der Modus "sicher" sendet nur DNS-over-HTTPS-Abfragen kann im Fehlerfall nicht auflösen.

Wenn Sie diese Richtlinie nicht konfigurieren, sendet der Browser möglicherweise DNS-über-HTTPS-Anforderungen an einen Resolver, der dem konfigurierten Systemresolver des Benutzers zugeordnet ist.

Zuordnung von Richtlinienoptionen:

* Off (Aus) = DNS-over-HTTPS deaktivieren

* Automatic (Automatisch) = DNS-over-HTTPS mit unsicheren Abfragen aktivieren

* Secure (Sicher) = DNS-over-HTTPS ohne unsichere Abfragen aktivieren

Verwenden Sie die vorstehenden Informationen, wenn Sie diese Richtlinie konfigurieren.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Zeichenfolge

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: DnsOverHttpsMode
  - GP-Name: Steuern des Modus von „DNS-over-HTTPS“
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: DnsOverHttpsMode
  - Werttyp: REG_SZ

  ##### Beispielwert:

```
"off"
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: DnsOverHttpsMode
  - Beispielwert:
``` xml
<string>off</string>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### DnsOverHttpsTemplates

  #### Geben Sie die URI-Vorlage des gewünschten DNS-over-HTTPS-Resolvers an

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 83 oder höher

  #### Beschreibung

  Die URI-Vorlage des gewünschten DNS-over-HTTPS-Resolvers. Wenn Sie mehrere DNS-über-HTTPS-Resolver angeben möchten, trennen Sie die entsprechenden URI-Vorlagen durch Leerzeichen.

Wenn Sie [DnsOverHttpsMode](#dnsoverhttpsmode) auf "sicher" festlegen, muss diese Richtlinie festgelegt und darf nicht leer sein.

Wenn Sie [DnsOverHttpsMode](#dnsoverhttpsmode) auf "automatisch" festlegen und diese Richtlinie festgelegt ist, werden die angegebenen URI-Vorlagen verwendet. Wenn Sie diese Richtlinie nicht festlegen, werden hartcodierte Zuordnungen verwendet, um zu versuchen, den aktuelle DNS-Resolver des Benutzers auf einen DoH-Resolver zu aktualisieren, der vom gleichen Anbieter betrieben wird.

Wenn die URI-Vorlage eine DNS-Variable enthält, verwenden Anforderungen an den Resolver GET, andernfalls verwenden sie POST.

Falsch formatierte Vorlagen werden ignoriert.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Zeichenfolge

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: DnsOverHttpsTemplates
  - GP-Name: Geben Sie die URI-Vorlage des gewünschten DNS-over-HTTPS-Resolvers an
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: DnsOverHttpsTemplates
  - Werttyp: REG_SZ

  ##### Beispielwert:

```
"https://dns.example.net/dns-query{?dns}"
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: DnsOverHttpsTemplates
  - Beispielwert:
``` xml
<string>https://dns.example.net/dns-query{?dns}</string>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### Download Directory

  #### Downloadverzeichnis festlegen

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Konfiguriert das Verzeichnis, das zum Speichern heruntergeladener Dateien verwendet werden soll.

Wenn Sie diese Richtlinie aktivieren, verwendet Microsoft Edge das bereitgestellte Verzeichnis unabhängig davon, ob der Benutzer eines festgelegt hat oder gewählt hat, jedes Mal nach einem Downloadort gefragt zu werden. Eine Liste der Variablen, die verwendet werden können, finden Sie unter [https://go.microsoft.com/fwlink/?linkid=2095041](https://go.microsoft.com/fwlink/?linkid=2095041).

Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, wird das standardmäßige Downloadverzeichnis verwendet und der Benutzer kann es ändern.

Wenn Sie einen ungültigen Pfad festlegen, wird Microsoft Edge auf das standardmäßige Downloadverzeichnis des Benutzers zurückgreifen.

Wenn der Ordner, der vom Pfad angegeben wird, nicht vorhanden ist, wird beim Herunterladen eine Eingabeaufforderung angezeigt, in der der Benutzer gefragt wird, wo der Download gespeichert werden soll.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Zeichenfolge

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: DownloadDirectory
  - GP-Name: Downloadverzeichnis festlegen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): Administrative Templates/Microsoft Edge – Standardeinstellungen (Benutzer können diese außer Kraft setzen)/
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Wertname: DownloadDirectory
  - Werttyp: REG_SZ

  ##### Beispielwert:

```
"\n      Linux-based OSes (including Mac): /home/${user_name}/Downloads\n      Windows: C:\\Users\\${user_name}\\Downloads"
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: DownloadDirectory
  - Beispielwert:
``` xml
<string>
      Linux-based OSes (including Mac): /home/${user_name}/Downloads
      Windows: C:\Users\${user_name}\Downloads</string>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### DownloadRestrictions

  #### Downloadbeschränkungen zulassen

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Konfiguriert die Art der Downloads, die von Microsoft Edge vollständig blockiert werden, ohne dass die Benutzer die Sicherheitsentscheidung außer Kraft setzen können.

Legen Sie die Einstellung auf „BlockDangerousDownloads“ fest, damit alle Downloads mit Ausnahme derer zulässig sind, die eine Microsoft Defender SmartScreen-Warnung erhalten.

Legen Sie die Einstellung auf „BlockPotentiallyDangerousDownloads“ fest, damit alle Downloads mit Ausnahme derer zulässig sind, die eine Microsoft Defender SmartScreen-Warnung für „potenziell gefährliche oder unerwünschte Downloads“ erhalten.

Legen Sie die Einstellung auf „'BlockAllDownloads“ fest, um alle Downloads zu blockieren.

Wenn Sie diese Richtlinie nicht konfigurieren oder die Option „DefaultDownloadSecurity“ festlegen, durchlaufen die Downloads die üblichen Sicherheitseinschränkungen, die auf den Analyseergebnissen von Microsoft Defender SmartScreen basieren.

Beachten Sie, dass diese Einschränkungen für Downloads aus Webseiteninhalten sowie für die Kontextmenü-Option „Download Link...“ gelten. Diese Einschränkungen gelten nicht für das Speichern oder Herunterladen der aktuell angezeigten Seite oder für die Option "als PDF speichern" aus den Druckoptionen.

Unter [https://go.microsoft.com/fwlink/?linkid=2094934](https://go.microsoft.com/fwlink/?linkid=2094934) finden Sie weitere Informationen zu Microsoft Defender SmartScreen.

Zuordnung von Richtlinienoptionen:

* DefaultDownloadSecurity (0) = Keine speziellen Beschränkungen

* BlockDangerousDownloads (1) = Gefährliche Downloads blockieren

* BlockPotentiallyDangerousDownloads (2) = Blockieren potenziell gefährlicher oder unerwünschter Downloads

* BlockAllDownloads (3) = Alle Downloads blockieren

Verwenden Sie die vorstehenden Informationen, wenn Sie diese Richtlinie konfigurieren.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Ganze Zahl

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: DownloadRestrictions
  - GP-Name: Downloadbeschränkungen zulassen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): Administrative Templates/Microsoft Edge – Standardeinstellungen (Benutzer können diese außer Kraft setzen)/
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Wertname: DownloadRestrictions
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000002
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: DownloadRestrictions
  - Beispielwert:
``` xml
<integer>2</integer>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### EdgeCollectionsEnabled

  #### Aktivieren des Features „Sammlungen“

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 78 oder höher

  #### Beschreibung

  Ermöglicht es Benutzern, auf das Sammlungs-Feature zuzugreifen, wodurch sie Inhalte effizienter und mit Office-Integration sammeln, organisieren, freigeben und exportieren können.

Wenn Sie diese Richtlinie aktivieren oder nicht konfigurieren, können Benutzer auf das Feature Sammlungen in Microsoft Edge zugreifen und es verwenden.

Wenn Sie diese Richtlinie deaktivieren, können Benutzer nicht auf Sammlungen in Microsoft Edge zugreifen und diese verwenden.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: EdgeCollectionsEnabled
  - GP-Name: Aktivieren des Features „Sammlungen“
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: EdgeCollectionsEnabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: EdgeCollectionsEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### EdgeShoppingAssistantEnabled

  #### Einkaufen in Microsoft Edge aktiviert

  
  
  #### Unterstützte Versionen:

  - On Windows and macOS since 87 or later

  #### Beschreibung

  Diese Richtlinie ermöglicht Benutzern, die Preise eines Produkts zu vergleichen, das Sie gerade betrachten, Gutscheine von der Website zu erhalten, auf der Sie sich befinden oder während des Auftragsabschlusses automatisch Coupons anzuwenden.

Wenn Sie diese Richtlinie aktivieren oder nicht konfigurieren, werden Einkaufsfeatures wie Preisvergleich und Coupons automatisch für Einzelhandelsdomänen angewendet. Coupons für den aktuellen Händler und die Preise von anderen Händlern werden auf einem Server abgeholt.

Wenn Sie diese Richtlinie deaktivieren, werden Einkaufsfeatures wie Preisvergleich und Coupons für Einzelhandelsdomänen nicht automatisch gefunden.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - Eindeutiger GP-Name: EdgeShoppingAssistantEnabled
  - GP-Name: Einkaufen in Microsoft Edge aktiviert
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): Administrative Templates/Microsoft Edge – Standardeinstellungen (Benutzer können diese außer Kraft setzen)/
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Wertname: EdgeShoppingAssistantEnabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: EdgeShoppingAssistantEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### EditFavoritesEnabled

  #### Ermöglicht Benutzern das Bearbeiten von Favoriten

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Aktivieren Sie diese Richtlinie, damit Benutzer Favoriten hinzufügen, entfernen und ändern können. Dies ist das Standardverhalten, wenn Sie die Richtlinie nicht konfigurieren.

Deaktivieren Sie diese Richtlinie, um zu verhindern, dass Benutzer Favoriten hinzufügen, entfernen oder ändern. Sie können die vorhandenen Favoriten weiterhin verwenden.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: EditFavoritesEnabled
  - GP-Name: Ermöglicht Benutzern das Bearbeiten von Favoriten
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: EditFavoritesEnabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000000
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: EditFavoritesEnabled
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### EnableDeprecatedWebPlatformFeatures

  #### Re-enable deprecated web platform features for a limited time (obsolete)

  
  >OBSOLETE: This policy is obsolete and doesn't work after Microsoft Edge 86.
  #### Unterstützte Versionen:

  - On Windows and macOS since 77, until 86

  #### Beschreibung

  This policy is obsolete because dedicated web platform policies are now used to manage individual web platform feature deprecations.

Geben Sie eine Liste von veralteten Webplattform-Features an, um diese vorübergehend wieder zu aktivieren.

Diese Richtlinie lässt Sie veraltete Webplattform-Features für einen begrenzten Zeitraum wieder aktivieren. Features werden durch eine Kennzeichnungs-Zeichenfolge identifiziert.

Wenn Sie diese Richtlinie nicht konfigurieren, wenn die Liste leer ist oder wenn ein Feature keiner der unterstützten Kennzeichnungs-Zeichenfolgen entspricht, bleiben alle veralteten Webplattform-Features deaktiviert.

Während die Richtlinie selbst auf den oben genannten Plattformen unterstützt wird, ist das von ihr aktivierte Feature möglicherweise nicht auf allen diesen Plattformen verfügbar. Nicht alle nicht mehr unterstützten Web-Plattformfeatures können erneut aktiviert werden. Nur die nachstehend aufgeführten Features können erneut aktiviert werden, und zwar nur für einen begrenzten Zeitraum, der sich je nach Feature unterscheidet. Sie können den Zweck der Änderungen am Webplattform-Feature in https://bit.ly/blinkintents erfahren.

Das allgemeine Format der Kennzeichnungszeichenfolge lautet [NameDesNichtMehrUnterstütztenFeatures] _EffectiveUntil[JJJJMMTT].

Zuordnung von Richtlinienoptionen:

* ExampleDeprecatedFeature (ExampleDeprecatedFeature_EffectiveUntil20080902) = ExampleDeprecatedFeature-API bis 02.09.2008 aktivieren

Verwenden Sie die vorstehenden Informationen, wenn Sie diese Richtlinie konfigurieren.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Liste von Zeichenfolgen

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: EnableDeprecatedWebPlatformFeatures
  - GP name: Re-enable deprecated web platform features for a limited time (obsolete)
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge\EnableDeprecatedWebPlatformFeatures
  - Pfad (Empfohlen): n.a.
  - Wertname: 1, 2, 3, ...
  - Werttyp: REG_SZ-Liste

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\EnableDeprecatedWebPlatformFeatures\1 = "ExampleDeprecatedFeature_EffectiveUntil20080902"

```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: EnableDeprecatedWebPlatformFeatures
  - Beispielwert:
``` xml
<array>
  <string>ExampleDeprecatedFeature_EffectiveUntil20080902</string>
</array>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### EnableDomainActionsDownload

  #### Herunterladen aktivieren von Domänenaktionen von Microsoft (veraltet)

  
  >VERALTET: Diese Richtlinie ist veraltet und funktioniert nach der Microsoft Edge-Version 84 nicht mehr.
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77, bis 84

  #### Beschreibung

  Diese Richtlinie funktioniert nicht, da in Konflikt stehende Zustände vermieden werden sollten. Diese Richtlinie wurde zum Aktivieren/Deaktivieren des Downloads der Liste der Domänenaktionen verwendet, hat jedoch nicht immer den gewünschten Status erreicht. Der Experimentier- und Konfigurationsservice, der den Download verarbeitet, verfügt über eine eigene Richtlinie, um zu konfigurieren, was aus dem Dienst heruntergeladen wird. Verwenden Sie stattdessen die [ExperimentationAndConfigurationServiceControl-](#experimentationandconfigurationservicecontrol)Richtlinie.

In Microsoft Edge stellen Domänenaktionen eine Reihe von Kompatibilitätsfeatures dar, die dazu beitragen, dass der Browser im Internet ordnungsgemäß funktioniert.

Eine Liste der Aktionen, die für bestimmte Domänen ausgeführt werden können, wird von Microsoft aus Kompatibilitätsgründen beibehalten. So kann beispielsweise der Browser die Zeichenfolge des Benutzeragenten auf einer Website außer Kraft setzen, wenn diese Website aufgrund der neuen Zeichenfolge des Benutzeragenten auf Microsoft Edge unterbrochen wurde. Jede dieser Aktionen soll temporär sein, während Microsoft versucht, das Problem mit dem Websitebesitzer zu beheben.

Wenn der Browser gestartet wird und danach in periodischen Abständen, kontaktiert der Browser den Experimentier- und Konfigurationsservice, der die aktuellste Liste der durchzuführenden Kompatibilitätsaktionen enthält. Diese Liste wird lokal gespeichert, nachdem sie zum ersten Mal abgerufen wurde, damit nachfolgende Anforderungen nur dann aktualisiert werden, wenn sich die Kopie des Servers geändert hat.

Wenn Sie diese Richtlinie aktivieren, wird die Liste der Domänenaktionen weiterhin aus dem Experimentier- und Konfigurationsservice heruntergeladen.

Wenn Sie diese Richtlinie deaktivieren, wird die Liste der Domänenaktionen nicht mehr aus dem Experimentier- und Konfigurationsservice heruntergeladen.

Wenn Sie diese Richtlinie nicht konfigurieren, wird die Liste der Domänenaktionen weiterhin aus dem Experimentier- und Konfigurationsservice heruntergeladen.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: EnableDomainActionsDownload
  - GP-Name: Herunterladen von Domänenaktionen von Microsoft aktivieren (veraltet)
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: EnableDomainActionsDownload
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: EnableDomainActionsDownload
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### EnableOnlineRevocationChecks

  #### Aktivieren von Online-OCSP-/CRL-Prüfungen

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Online-Sperrprüfungen bieten keinen wesentlichen Sicherheitsvorteil und sind standardmäßig deaktiviert.

Wenn Sie diese Richtlinie aktivieren, führt Microsoft Edge Soft-Fail-Online-OCSP-/CRL-Prüfungen durch. "Soft Fail" bedeutet: Wenn der Sperrserver nicht erreicht werden kann, wird das Zertifikat als gültig betrachtet.

Wenn Sie die Richtlinie deaktivieren oder nicht konfigurieren, führt Microsoft Edge keine Online-Sperrüberprüfungen aus.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: EnableOnlineRevocationChecks
  - GP-Name: Aktivieren von Online-OCSP-/CRL-Prüfungen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: EnableOnlineRevocationChecks
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000000
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: EnableOnlineRevocationChecks
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### EnableSha1ForLocalAnchors

  #### Zulassen von Zertifikaten, die mit SHA-1 signiert wurden, wenn sie von lokalen Vertrauensankern ausgegeben wurden (veraltet).

  >VERALTET: Diese Richtlinie ist veraltet. Sie wird zurzeit unterstützt, aber in einer zukünftigen Version als veraltet behandelt.
  
  #### Unterstützte Versionen:

  - Auf Windows und MacOS ab 85 oder später

  #### Beschreibung

  Wenn diese Einstellung aktiviert ist, lässt Microsoft Edge Verbindungen zu, die durch SHA-1-signierte Zertifikate gesichert sind, solange das Zertifikat mit einem lokal installierten Stammzertifikat verknüpft und ansonsten gültig ist.

Beachten Sie, dass diese Richtlinie davon abhängt, ob der Verifizierungsstapel des Betriebssystems (OS) SHA-1-Signaturen zulässt. Wenn ein Update des Betriebssystems die Handhabung von SHA-1-Zertifikaten durch das Betriebssystem ändert, hat diese Richtlinie möglicherweise keine Wirkung mehr.  Außerdem ist diese Richtlinie als vorübergehende Problemumgehung vorgesehen, um den Unternehmen mehr Zeit geben, sich vom SHA-1 umzuorientieren. Diese Richtlinie wird mit der Veröffentlichung von Microsoft Edge 92 Mitte 2021 entfernt werden.

Wenn Sie diese Richtlinie nicht festlegen, auf „false“ setzen oder das SHA-1-Zertifikat mit einem öffentlich vertrauenswürdigen Stammzertifikat verknüpfen, lässt Microsoft Edge keine von SHA-1 signierten Zertifikate zu.

Diese Richtlinie ist nur für Windows-Instanzen verfügbar, die mit einer Microsoft Active Directory-Domäne verknüpft sind, Windows 10 Pro- oder Enterprise-Instanzen, die für die Geräteverwaltung registriert sind, oder MacOS-Instanzen, die über MDM verwaltet oder über MCX einer Domäne beigetreten sind.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - Eindeutiger GP-Name: EnableSha1ForLocalAnchors
  - GP-Name: Zulassen von Zertifikaten, die mit SHA-1 signiert wurden, wenn sie von lokalen Vertrauensankern ausgegeben wurden (veraltet)
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: EnableSha1ForLocalAnchors
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000000
```

  #### Mac – Informationen und Einstellungen
  
  - Name des Einstellungsschlüssels: EnableSha1ForLocalAnchors
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### EnterpriseHardwarePlatformAPIEnabled

  #### Zulassen der Verwendung der Enterprise-Hardware Plattform-API für verwaltete Erweiterungen

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 78 oder höher

  #### Beschreibung

  Wenn diese Richtlinie auf "aktiviert" festgelegt ist, können mit der Enterprise-Richtlinie installierte Erweiterungen die API der Enterprise-Hardware Plattform verwenden.
Wenn diese Richtlinie auf „deaktiviert“ festgelegt oder nicht festgelegt ist, dürfen keine Erweiterungen die API für die Enterprise-Hardware Plattform verwenden.
Diese Richtlinie gilt auch für Komponentenerweiterungen.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: EnterpriseHardwarePlatformAPIEnabled
  - GP-Name: Zulassen der Verwendung der Enterprise-Hardware Plattform-API für verwaltete Erweiterungen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: EnterpriseHardwarePlatformAPIEnabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: EnterpriseHardwarePlatformAPIEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### EnterpriseModeSiteListManagerAllowed

  #### Zugriff auf das Enterprise Mode Site List Manager-Tool ulassen

  
  
  #### Unterstützte Versionen:

  - Unter Windows 86 oder später

  #### Beschreibung

  Hier können Sie einstellen, ob der Enterprise Mode Site List Manager für Benutzer zur Verfügung steht.

Wenn Sie diese Richtlinie aktivieren, können Benutzer die Navigationsschaltfläche Enterprise Mode Site List Manager auf der Seite edge://compat sehen, zum Tool navigieren und es verwenden.

Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, sehen die Benutzer die Navigationsschaltfläche Enterprise Mode Site List Manager nicht und können sie nicht verwenden.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - Eindeutiger GP-Name: EnterpriseModeSiteListManagerAllowed
  - GP-Name: Zugriff auf das Tool Enterprise Mode Site List Manager zulassen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: EnterpriseModeSiteListManagerAllowed
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000000
```

  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### ExemptDomainFileTypePairsFromFileTypeDownloadWarnings

  #### Herunterladen deaktivieren von Warnungen basierend auf Dateierweiterungen für bestimmte Dateitypen in Domänen

  
  
  #### Unterstützte Versionen:

  - Auf Windows und MacOS ab 85 oder später

  #### Beschreibung

  Sie können diese Richtlinie aktivieren, um ein Lexikon mit Dateityperweiterungen mit einer entsprechenden Liste von Domänen erstellen, die Download-Warnungen ausschließt, basierend auf Dateierweiterungen für bestimmte Dateitypen. Auf diese Weise können Unternehmensadministratoren Download-Warnungen für Dateien blockieren, basierend auf Dateierweiterungen, die einer aufgeführten Domäne zugeordnet sind. Wenn z. b. die Erweiterung "JNLP" mit "website1.com" verknüpft ist, wird den Benutzern beim Herunterladen von "JNLP"-Dateien aus "website1.com" keine Warnung angezeigt, es wird jedoch eine Download-Warnung angezeigt, wenn Sie "JNLP"-Dateien aus "website2.com" herunterladen.

Dateien mit Dateityperweiterungen, die für Domänen angegeben sind, die durch diese Richtlinie gekennzeichnet sind, unterliegen weiterhin Sicherheitswarnungen, die nicht auf Dateityp basieren, wie z. b. Download Warnungen mit gemischten Inhalten und SmartScreen-Warnungen von Microsoft Defender.

Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, zeigen Dateitypen die Download-Warnungen auslösen, basierende auf Dateierweiterungen für den Benutzer an.

Wenn Sie diese Richtlinie aktivieren:

* Das URL-Muster sollte gemäß [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)formatiert sein.
* Die eingegebene Dateierweiterung muss sich im kleingeschriebenen ASCII-Format befinden. Das führende Trennzeichen sollte nicht einbezogen werden, wenn die Dateinamenerweiterung aufgelistet wird. Deshalb sollte die Liste "JNLP" anstelle von ". jnlp" verwendet werden.

Beispiel:

Der folgende Beispielwert würde Download-Warnungen für Dateien basierend auf Dateierweiterungen bei den SWF-, exe-und JNLP-Erweiterungen für *. contoso.com-Domänen verhindern. Dies würde dem Benutzer eine Download-Warnung zeigen basierend auf Dateityperweiterung auf jegliche Domänen von Exe-und JNLP-Dateien, nicht jedoch für SWF-Dateien.

[ { "file_extension": "jnlp", "domains": ["contoso.com"] }, { "file_extension": "exe", "domains": ["contoso.com"] }, { "file_extension": "swf", "domains": ["*"] } ]

Beachten Sie, dass, während im vorstehenden Beispiel die Unterdrückung von Download-Warnungen basierend auf Dateityperweiterung für "SWF"-Dateien für alle Domänen dargestellt wird, die Anwendung einer Unterdrückung derartiger Warnungen für alle Domänen für alle gefährlichen Dateierweiterungen aufgrund von Sicherheitsbedenken nicht empfohlen wird. In diesem Beispiel wird nur gezeigt, dass es möglich ist.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Liste von Zeichenfolgen

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - Eindeutiger Name des GP: ExemptDomainFileTypePairsFromFileTypeDownloadWarnings
  - GP-Name: Herunterladen deaktivieren von Warnungen basierend auf Dateierweiterungen für bestimmte Dateitypen in Domänen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Path (Mandatory): SOFTWARE\Policies\Microsoft\Edge\ExemptDomainFileTypePairsFromFileTypeDownloadWarnings
  - Pfad (Empfohlen): n.a.
  - Wertname: 1, 2, 3, ...
  - Werttyp: REG_SZ-Liste

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\ExemptDomainFileTypePairsFromFileTypeDownloadWarnings\1 = {"domains": ["https://contoso.com", "contoso2.com"], "file_extension": "jnlp"}
SOFTWARE\Policies\Microsoft\Edge\ExemptDomainFileTypePairsFromFileTypeDownloadWarnings\2 = {"domains": ["*"], "file_extension": "swf"}

```

  #### Mac – Informationen und Einstellungen
  
  - Name des Einstellungsschlüssels: ExemptDomainFileTypePairsFromFileTypeDownloadWarnings
  - Beispielwert:
``` xml
<array>
  <string>{'domains': ['https://contoso.com', 'contoso2.com'], 'file_extension': 'jnlp'}</string>
  <string>{'domains': ['*'], 'file_extension': 'swf'}</string>
</array>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### ExperimentationAndConfigurationServiceControl

  #### Steuern der Kommunikation mit dem Experimentier- und Konfigurationsservice

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  In Microsoft Edge wird der Experimentier- und Konfigurationsservice verwendet, um Experimentier- und Konfigurationsnutzlasten bereitzustellen.

Die Experimentier-Nutzlast besteht aus einer Liste von Funktionen in Frühstadien der Entwicklung, die Microsoft zu Test- und Feedbackzwecken aktiviert.

Die Konfigurationsnutzlast besteht aus einer Liste von Einstellungen, die Microsoft an Microsoft Edge bereitstellen möchte, um die Benutzererfahrung zu optimieren. So kann beispielsweise die Konfigurationsnutzlast angeben, wie oft Microsoft Edge Anforderungen an den Experimentier- und Konfigurationsservice sendet, um die neueste Nutzlast abzurufen.

Zusätzlich kann die Konfigurationsnutzlast auch eine Liste der Aktionen enthalten, die aus Kompatibilitätsgründen für bestimmte Domänen ausgeführt werden sollen. So kann beispielsweise der Browser die Zeichenfolge des Benutzeragenten auf einer Website außer Kraft setzen, wenn diese Website aufgrund der neuen Zeichenfolge des Benutzeragenten auf Microsoft Edge unterbrochen wurde. Jede dieser Aktionen soll temporär sein, während Microsoft versucht, das Problem mit dem Websitebesitzer zu beheben.

Wenn Sie diese Richtlinie auf „FullMode“ setzen, wird die vollständige Nutzlast aus dem Experimentier- und Konfigurationsservice heruntergeladen. Dies umfasst sowohl die Test- als auch die Konfigurationsnutzlast.

Wenn Sie diese Richtlinie auf „ConfigurationsOnlyMode“ setzen, wird nur die Konfigurationsnutzlast bereitgestellt.

Wenn Sie diese Richtlinie auf „RestrictedMode“ setzen, wird die Kommunikation mit dem Experimentier- und Konfigurationsservice vollständig gestoppt.

Wenn Sie diese Richtlinie nicht konfigurieren, ist das Verhalten auf einem verwalteten Gerät auf Stable- und Beta-Kanälen identisch mit dem Modus „ConfigurationsOnlyMode“.

Wenn Sie diese Richtlinie nicht konfigurieren, ist das Verhalten auf einem nicht verwalteten Gerät das gleiche wie beim „FullMode“.

Zuordnung von Richtlinienoptionen:

* FullMode (2) = Abrufen von Konfigurationen und Experimenten

* ConfigurationsOnlyMode (1) = Nur Konfigurationen abrufen

* RestrictedMode (0) = Kommunikation mit dem Experimentier- und Konfigurationsservice deaktivieren

Verwenden Sie die vorstehenden Informationen, wenn Sie diese Richtlinie konfigurieren.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Ganze Zahl

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: ExperimentationAndConfigurationServiceControl
  - GP-Name: Steuern der Kommunikation mit dem Experimentier- und Konfigurationsservice
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: ExperimentationAndConfigurationServiceControl
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000002
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: ExperimentationAndConfigurationServiceControl
  - Beispielwert:
``` xml
<integer>2</integer>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### ExternalProtocolDialogShowAlwaysOpenCheckbox

  #### Anzeigen eines „immer öffnen“-Kontrollkästchens im externen Protokoll-Dialog

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 79 oder höher

  #### Beschreibung

  Mit dieser Richtlinie wird gesteuert, ob das Kontrollkästchen "diese Website kann immer Links dieser Art öffnen" auf Bestätigungsmeldungen zum Start externer Protokolle angezeigt wird. Diese Richtlinie gilt nur für https://-Links.

Wenn Sie diese Richtlinie aktivieren, kann der Benutzer bei der Anzeige einer externen Protokollbestätigungsaufforderung "Immer zulassen" markieren, um alle zukünftigen Bestätigungsaufforderungen für das Protokoll auf dieser Site zu überspringen.

Wenn Sie diese Richtlinie deaktivieren, wird das Kontrollkästchen "Immer zulassen" nicht angezeigt. Der Benutzer wird jedes Mal, wenn ein externes Protokoll aufgerufen wird, zur Bestätigung aufgefordert.

Wird diese Richtlinie nicht konfiguriert, wurde vor dem Microsoft Edge 83 das Kontrollkästchen „Immer zulassen“ nicht angezeigt. Der Benutzer wird jedes Mal, wenn ein externes Protokoll aufgerufen wird, zur Bestätigung aufgefordert.

Wenn Sie diese Richtlinie unter Microsoft Edge 83 nicht konfigurieren, wird die Sichtbarkeit des Kontrollkästchens durch das Flag „Einstellungen für Protokollstartaufforderung beibehalten“ in „edge://flags“ gesteuert.

Wenn Sie ab Microsoft Edge 84 diese Richtlinie nicht konfigurieren, kann der Benutzer bei der Anzeige einer externen Protokollbestätigungsaufforderung „Immer zulassen“ markieren, um alle zukünftigen Bestätigungsaufforderungen für das Protokoll auf dieser Site zu überspringen.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: ExternalProtocolDialogShowAlwaysOpenCheckbox
  - GP-Name: Anzeigen eines „immer offen“-Kontrollkästchens im externen Protokoll-Dialog
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: ExternalProtocolDialogShowAlwaysOpenCheckbox
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: ExternalProtocolDialogShowAlwaysOpenCheckbox
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### FamilySafetySettingsEnabled

  #### Zulassen, dass Benutzer Family Safety konfigurieren

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 83 oder höher

  #### Beschreibung

  Mit dieser Richtlinie wird die Family Safety-Seite in Einstellungen deaktiviert und vollständig ausgeblendet. Auch die Navigation zu edge://settings/familysafety wird blockiert. Auf der Seite Family Safety wird beschrieben, welche Features für Familiengruppen verfügbar sind und wie Sie einer Familiengruppe beitreten. Hier erfahren Sie mehr über Family Safety: ([https://go.microsoft.com/fwlink/?linkid=2098432](https://go.microsoft.com/fwlink/?linkid=2098432)).

Wenn Sie diese Richtlinie aktivieren oder nicht konfigurieren, wird die Seite Family Safety angezeigt.

Wenn Sie diese Richtlinie deaktivieren, wird die Seite Family Safety nicht angezeigt.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: FamilySafetySettingsEnabled
  - GP-Name: Zulassen, dass Benutzer Family Safety konfigurieren
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: FamilySafetySettingsEnabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: FamilySafetySettingsEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### FavoritesBarEnabled

  #### Aktivieren der Favoritenleiste

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Aktiviert oder deaktiviert die Favoritenleiste.

Wenn Sie diese Richtlinie aktivieren, wird den Benutzern die Favoritenleiste angezeigt.

Wenn Sie diese Richtlinie deaktivieren, wird den Benutzern die Favoritenleiste nicht angezeigt.

Wenn diese Richtlinie nicht konfiguriert ist, kann der Benutzer entscheiden, die Favoritenleiste zu verwenden oder nicht.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: FavoritesBarEnabled
  - GP-Name: Aktivieren der Favoritenleiste
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): Administrative Templates/Microsoft Edge – Standardeinstellungen (Benutzer können diese außer Kraft setzen)/
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Wertname: FavoritesBarEnabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: FavoritesBarEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### ForceBingSafeSearch

  #### Erzwingen von Bing SafeSearch

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Stellt sicher, dass Abfragen in der Bing-Websuche mit dem festgelegten SafeSearch-Wert ausgeführt werden. Benutzer können diese Einstellung nicht ändern.

Wenn Sie diese Richtlinie auf „BingSafeSearchNoRestrictionsMode“ konfigurieren, greift SafeSearch in der Bing-Suche auf den Bing.com-Wert zurück.

Wenn Sie diese Richtlinie auf „BingSafeSearchModerateMode“ konfigurieren, wird die moderate Einstellung in SafeSearch verwendet. Die moderate Einstellung filtert Videos und Bilder für Erwachsene aus, nicht aber Text aus den Suchergebnissen.

Wenn Sie diese Richtlinie auf „BingSafeSearchStrictMode“ konfigurieren, wird die strikte Einstellung in SafeSearch verwendet. Die strikte Einstellung filtert Text, Bilder und Videos für Erwachsene aus.

Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, wird SafeSearch in Bing Search nicht erzwungen, und die Benutzer können den gewünschten Wert auf Bing.com festlegen.

Zuordnung von Richtlinienoptionen:

* BingSafeSearchNoRestrictionsMode (0) = Keine Suchbeschränkungen in Bing konfigurieren

* BingSafeSearchModerateMode (1) = Moderate Suchbeschränkungen in Bing konfigurieren

* BingSafeSearchStrictMode (2) = Strikte Suchbeschränkungen in Bing konfigurieren

Verwenden Sie die vorstehenden Informationen, wenn Sie diese Richtlinie konfigurieren.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Ganze Zahl

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: ForceBingSafeSearch
  - GP-Name: Erzwingen von Bing SafeSearch
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: ForceBingSafeSearch
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000000
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: ForceBingSafeSearch
  - Beispielwert:
``` xml
<integer>0</integer>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### ForceCertificatePromptsOnMultipleMatches

  #### Konfigurieren, ob Microsoft Edge automatisch ein Zertifikat auswählen soll, wenn mehrere Zertifikat-Übereinstimmungen für eine Website vorhanden sind, die mit „AutoSelectCertificateForUrls“ konfiguriert ist

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 81 oder höher

  #### Beschreibung

  Legt fest, ob Benutzer zum Auswählen eines Zertifikats aufgefordert werden, wenn mehrere Zertifikate verfügbar sind und eine Website mit [AutoSelectCertificateForUrls](#autoselectcertificateforurls) konfiguriert ist. Wenn Sie [AutoSelectCertificateForUrls](#autoselectcertificateforurls) für eine Website nicht konfigurieren, wird der Benutzer immer aufgefordert, ein Zertifikat auszuwählen.

Wenn Sie diese Richtlinie auf "wahr" festlegen, fordert Microsoft Edge den Benutzer auf, ein Zertifikat für Websites aus der Liste auszuwählen, die durch [AutoSelectCertificateForUrls](#autoselectcertificateforurls) definiert wird, falls mehr als ein Zertifikat vorhanden ist.

Wenn Sie diese Richtlinie auf "false" festlegen oder Sie nicht konfigurieren, wählt Microsoft Edge automatisch ein Zertifikat aus, auch wenn mehrere Übereinstimmungen für ein Zertifikat vorhanden sind. Der Benutzer wird nicht aufgefordert, ein Zertifikat für Websites aus der Liste auszuwählen, die in [AutoSelectCertificateForUrls](#autoselectcertificateforurls) definiert ist.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: ForceCertificatePromptsOnMultipleMatches
  - GP-Name: Konfigurieren, ob Microsoft Edge automatisch ein Zertifikat auswählen soll, wenn mehrere Zertifikat-Übereinstimmungen für eine Website vorhanden sind, die mit „AutoSelectCertificateForUrls“ konfiguriert ist
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: ForceCertificatePromptsOnMultipleMatches
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: ForceCertificatePromptsOnMultipleMatches
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### ForceEphemeralProfiles

  #### Verwendung von kurzlebigen Profilen zulassen

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Steuert, ob Benutzerprofile in den kurzlebigen Modus verlagert werden. Beim Start einer Sitzung wird ein kurzlebiges Profil erstellt, beim Ende der Sitzung gelöscht und dem ursprünglichen Profil des Benutzers zugeordnet.

Wenn Sie diese Richtlinie aktivieren, werden Profile im kurzlebigen Modus ausgeführt. Auf diese Weise können Benutzer auf ihren eigenen Geräten arbeiten, ohne die Browserdaten auf diesen Geräten zu speichern. Wenn Sie diese Richtlinie als Betriebssystemrichtlinie (z.B. mithilfe von Gruppenrichtlinienobjekten unter Windows) aktivieren, gilt sie für alle Profile im System.

Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, erhalten die Benutzer beim Anmelden beim Browser ihre regulären Profile.

Im kurzlebigen Modus werden Profildaten nur für die Dauer der Benutzersitzung auf dem Datenträger gespeichert. Features wie Browserverlauf, Erweiterungen und deren Daten, Webdaten wie Cookies und Webdatenbanken werden nach dem Schließen des Browsers nicht gespeichert. Damit wird nicht verhindert, dass Benutzer Daten manuell auf den Datenträger herunterladen oder Seiten speichern oder drucken können. Wenn der Benutzer die Synchronisierung aktiviert hat, werden alle Daten in ihren Synchronisierungskonten, wie bei normalen Profilen, beibehalten. Benutzer können auch InPrivate-Browsen im kurzlebigen Modus verwenden, sofern Sie dies nicht explizit deaktivieren.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: ForceEphemeralProfiles
  - GP-Name: Verwendung von kurzlebigen Profilen zulassen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: ForceEphemeralProfiles
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: ForceEphemeralProfiles
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### ForceGoogleSafeSearch

  #### Google SafeSearch erzwingen

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Erzwingt, dass Abfragen in der Google-Websuche mit der SafeSearch-Einstellung „Aktiv“ durchgeführt werden und hindert Benutzer daran, diese Einstellung zu ändern.

Wenn Sie diese Richtlinie aktivieren, ist SafeSearch in der Google-Suche immer aktiv.

Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, wird SafeSearch in der Google-Suche nicht erzwungen.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: ForceGoogleSafeSearch
  - GP-Name: Google SafeSearch erzwingen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: ForceGoogleSafeSearch
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000000
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: ForceGoogleSafeSearch
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### ForceLegacyDefaultReferrerPolicy

  #### Verwenden Sie die standardmäßige Verweiserrichtlinie „kein Verweiser beim Downgrade“ (veraltet)

  >VERALTET: Diese Richtlinie ist veraltet. Sie wird zurzeit unterstützt, aber in einer zukünftigen Version als veraltet behandelt.
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 81 oder höher

  #### Beschreibung

  Diese Richtlinie ist veraltet, weil sie nur als kurzfristiger Mechanismus vorgesehen ist, um Unternehmen mehr Zeit zum Aktualisieren ihrer Webinhalte zu verschaffen, falls diese mit der aktuellen Standard-Referrer-Richtlinie inkompatibel sind. Es wird in Microsoft Edge ab Version 88 nicht mehr funktionieren.

Die standardmäßige Referrer-Richtlinie von Microsoft Edge wird vom aktuellen Wert von "no-referrer-when-downgrade" auf den sichereren „strict-origin-when-cross-origin“ durch ein schrittweises Rollout gestärkt.

Vor dem Rollout hat diese Unternehmensrichtlinie keine Wirkung. Nach dem Rollout, wenn diese Unternehmensrichtlinie aktiviert ist, wird die standardmäßige Referrer-Richtlinie von Microsoft Edge auf den alten Wert "no-referrer-when-downgrade" festgelegt.

Diese Unternehmensrichtlinie ist standardmäßig deaktiviert.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: ForceLegacyDefaultReferrerPolicy
  - GP-Name: Verwenden Sie die standardmäßige Verweiserrichtlinie „kein Verweiser beim Downgrade“ (verworfen)
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: ForceLegacyDefaultReferrerPolicy
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000000
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: ForceLegacyDefaultReferrerPolicy
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### ForceNetworkInProcess

  #### Erzwingen der Ausführung des Netzwerkcodes im Browserprozess (veraltet)

  
  >VERALTET: Diese Richtlinie ist veraltet und funktioniert nach Microsoft Edge 83 nicht mehr.
  #### Unterstützte Versionen:

  - Auf Windows seit 78, bis 83

  #### Beschreibung

  Diese Richtlinie funktioniert nicht, da es sich nur um einen kurzfristigen Mechanismus handeln sollte, um Unternehmen mehr Zeit für die Migration zu Software von Drittanbietern zu geben, die nicht vom einbinden von Netzwerk-APIs abhängig ist. Proxyserver werden über LSPs und Win32-API-Patching empfohlen.

Diese Richtlinie erzwingt das Ausführen von Netzwerkcode im Browserprozess.

Diese Richtlinie ist standardmäßig deaktiviert. Wenn sie aktiviert ist, sind Benutzer Sicherheitsproblemen ausgesetzt, wenn der Netzwerkvorgang in der Sandbox ausgeführt wird.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: ForceNetworkInProcess
  - GP-Name: Erzwingen des Ausführens von Netzwerkcode im Browserprozess (veraltet)
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: ForceNetworkInProcess
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000000
```

  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### ForceSync

  #### Synchronisierung von Browserdaten erzwingen und Zustimmungsaufforderung für die Synchronisierung nicht anzeigen

  
  
  #### Unterstützte Versionen:

  - Unter Windows und macOS ab 86 oder höher

  #### Beschreibung

  Erzwingt die Datensynchronisierung in Microsoft Edge. Diese Richtlinie hindert den Benutzer außerdem daran, die Synchronisierung zu deaktivieren.

Wenn Sie diese Richtlinie nicht konfigurieren, können die Benutzer die Synchronisierung aktivieren oder deaktivieren. Wenn Sie diese Richtlinie aktivieren, können die Benutzer die Synchronisierung nicht deaktivieren.

Damit diese Richtlinie ordnungsgemäß funktioniert, darf die [BrowserSignin](#browsersignin)-Richtlinie nicht konfiguriert oder aktiviert sein. Wenn [BrowserSignin](#browsersignin) auf "Deaktiviert" festgelegt ist, ist [ForceSync](#forcesync) nicht wirksam.

[SyncDisabled](#syncdisabled) darf nicht konfiguriert sein oder muss auf "False" festgelegt sein. Wenn sie auf "True" festgelegt ist, ist [ForceSync](#forcesync) nicht wirksam.

0 = Synchronisierung nicht automatisch starten und Zustimmungsaufforderung für die Synchronisierung anzeigen (Standardeinstellung) 1 = Aktivierung der Synchronisierung für Azure AD-/Azure AD-herabgesetztes Benutzerprofil erzwingen und Zustimmungsaufforderung für die Synchronisierung nicht anzeigen

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - Eindeutiger GP-Name: ForceSync
  - GP-Name: Synchronisierung von Browserdaten erzwingen und Zustimmungsaufforderung für die Synchronisierung nicht anzeigen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: ForceSync
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: ForceSync
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### ForceYouTubeRestrict

  #### Erzwingen des minimal eingeschränkten Modus für YouTube

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Erzwingt einen minimalen eingeschränkten Modus auf YouTube und hindert Benutzer daran, einen weniger eingeschränkten Modus zu wählen.

Auf „strikt“ setzen, um den Modus „strikt einschränkt“ auf YouTube zu erzwingen.

Auf „moderat“ setzen, um den Benutzer zu zwingen, auf YouTube nur den Modus „moderat eingeschränkt“ und „strikt eingeschränkt“ Modus zu verwenden. Der Benutzer kann den eingeschränkten Modus nicht deaktivieren.

Setzen Sie diese Richtlinie auf „Aus“ oder konfigurieren Sie sie nicht, so dass der eingeschränkte Modus auf YouTube nicht erzwungen wird. Externe Richtlinien, z.B. YouTube-Richtlinien, können den eingeschränkten Modus dennoch durchsetzen.

Zuordnung von Richtlinienoptionen:

* Off (0) = Den eingeschränkten Modus auf YouTube nicht erzwingen

* Moderate (1) = Mindestens den moderat eingeschränkten Modus auf YouTube erzwingen

* Strict (2) = Erzwingen des strikt eingeschränkten Modus auf YouTube

Verwenden Sie die vorstehenden Informationen, wenn Sie diese Richtlinie konfigurieren.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Ganze Zahl

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: ForceYouTubeRestrict
  - GP-Name: Erzwingen des Minimum-beschränkten Modus für YouTube
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: ForceYouTubeRestrict
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000000
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: ForceYouTubeRestrict
  - Beispielwert:
``` xml
<integer>0</integer>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### FullscreenAllowed

  #### Vollbild-Modus zulassen

  
  
  #### Unterstützte Versionen:

  - Auf Windows ab 77 oder höher

  #### Beschreibung

  Festlegen der Verfügbarkeit des Vollbildmodus – die gesamte Microsoft Edge-Benutzeroberfläche ist ausgeblendet, und nur Webinhalte werden angezeigt.

Wenn Sie diese Richtlinie aktivieren oder nicht konfigurieren, können der Benutzer, Apps und Erweiterungen mit den entsprechenden Berechtigungen in den Vollbildmodus wechseln.

Wenn Sie diese Richtlinie deaktivieren, können Benutzer, Apps und Erweiterungen nicht in den Vollbildmodus wechseln.

Das Öffnen von Microsoft Edge im Kioskmodus mithilfe der Befehlszeile ist nicht verfügbar, wenn der Vollbildmodus deaktiviert ist.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: FullscreenAllowed
  - GP-Name: Vollbild-Modus zulassen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: FullscreenAllowed
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### GloballyScopeHTTPAuthCacheEnabled

  #### Aktivieren von globalem HTTP-Authentifizierungscache

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 81 oder höher

  #### Beschreibung

  Diese Richtlinie konfiguriert einen einzelnen globalen Cache pro Profil mit Anmeldeinformationen für die HTTP-Serverauthentifizierung.

Wenn Sie diese Richtlinie deaktivieren oder nicht festlegen, verwendet der Browser das Standardverhalten der websiteübergreifenden Authentifizierung, die ab Version 80 die Festlegung der HTTP-Serverauthentifizierungs-Anmeldeinformationen nach Top-Level-Websites ist. Wenn also zwei Websites Ressourcen aus derselben authentifizierenden Domäne verwenden, müssen die Anmeldeinformationen im Kontext beider Websites unabhängig voneinander bereitgestellt werden. Zwischengespeicherte Proxyanmeldeinformationen werden für alle Websites wiederverwendet.

Wenn Sie diese Richtlinie aktivieren, werden die im Kontext einer Website eingegebenen HTTP-Authentifizierungs-Anmeldeinformationen automatisch im Kontext einer anderen Website verwendet.

Wenn Sie diese Richtlinie aktivieren, bleiben Websites für einige Arten von Cross-Site-Attacken offen, und Benutzer können auch ohne Cookies über mehrere Websites nachverfolgt werden, und zwar durch Hinzufügen von Einträgen im HTTP-Authentifizierungscache mithilfe von in URLs eingebetteten Anmeldeinformationen.

Diese Richtlinie dient dazu, Unternehmen je nach Legacy-Verhalten die Möglichkeit zu geben, ihre Anmeldeverfahren zu aktualisieren, und wird künftig entfernt.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: GloballyScopeHTTPAuthCacheEnabled
  - GP-Name: Aktivieren von globalem HTTP-Authentifizierungscache
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: GloballyScopeHTTPAuthCacheEnabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000000
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: GloballyScopeHTTPAuthCacheEnabled
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### GoToIntranetSiteForSingleWordEntryInAddressBar

  #### Erzwingen der direkten Intranet-Websitenavigation anstelle der Suche nach Einzelwort-Einträgen in der Adressleiste

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 78 oder höher

  #### Beschreibung

  Wenn Sie diese Richtlinie aktivieren, wird in der Vorschlagsliste der Adressleiste das erste Ergebnis zu Intranet-Websites navigieren, wenn der in der Adressleiste eingegebene Text nur ein einzelnes Wort ohne Interpunktion ist.

Wenn Sie ein einzelnes Wort ohne Interpunktionszeichen eingeben, wird die Navigation zu einer Intranetsite durchgeführt, die mit dem eingegebenen Text übereinstimmt.

Wenn Sie diese Richtlinie aktivieren, wird in der Vorschlagsliste der Adressleiste das zweite Ergebnis eine exakt diesem Begriff entsprechende Internetsuche auslösen, wenn der in der Adressleiste eingegebene Text nur ein einzelnes Wort ohne Interpunktion ist. Der standardmäßige Suchanbieter wird verwendet, es sei denn, es ist zusätzlich eine Richtlinie zur Verhinderung der Websuche aktiviert.

Die Aktivierung dieser Richtlinie hat zwei Auswirkungen:

Die Navigation zu Websites als Reaktion auf Einzelwortabfragen, die normalerweise ein Verlaufselement erzeugen würden, wird nicht mehr ausgeführt. Stattdessen versucht der Browser zu internen Websites zu navigieren, die im Intranet einer Organisation möglicherweise nicht vorhanden sind. Dies führt zu einem 404-Fehler.

Beliebte Einzelwort-Suchbegriffe benötigen eine manuelle Auswahl von Suchvorschlägen, um die Suche richtig durchführen zu können.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: GoToIntranetSiteForSingleWordEntryInAddressBar
  - GP-Name: Erzwingen der direkten Intranet-Websitenavigation anstelle der Suche nach Einzelwort-Einträgen in der Adressleiste
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: GoToIntranetSiteForSingleWordEntryInAddressBar
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000000
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: GoToIntranetSiteForSingleWordEntryInAddressBar
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### HSTSPolicyBypassList

  #### Konfigurieren der Liste der Namen, die die HSTS-Richtlinienüberprüfung umgehen

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 79 oder höher

  #### Beschreibung

  Hostnamen, die in dieser Liste angegeben sind, sind von der HSTS-Richtlinienüberprüfung ausgenommen, die möglicherweise Anfragen von "http://" auf "https://" hochstuft. In dieser Richtlinie sind nur Einzelbezeichnungs-Hostnamen zulässig. Hostnamen müssen kanonisch sein. Jeder IDN muss in sein A-Label-Format konvertiert werden, und alle ASCII-Zeichen müssen in Kleinbuchstaben vorliegen. Diese Richtlinie gilt nur für die explizit angegebenen Hostnamen. Er gilt nicht für Unterdomänen der Namen in der Liste.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Liste von Zeichenfolgen

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: HSTSPolicyBypassList
  - GP-Name: Konfigurieren der Liste der Namen, die die HSTS-Richtlinienüberprüfung umgehen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge\HSTSPolicyBypassList
  - Pfad (Empfohlen): n.a.
  - Wertname: 1, 2, 3, ...
  - Werttyp: REG_SZ-Liste

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\HSTSPolicyBypassList\1 = "meet"

```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: HSTSPolicyBypassList
  - Beispielwert:
``` xml
<array>
  <string>meet</string>
</array>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### HardwareAccelerationModeEnabled

  #### Verwenden der Hardwarebeschleunigung, falls verfügbar

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Legt die Verwendung der Hardwarebeschleunigung fest, falls diese verfügbar ist. Wenn Sie diese Richtlinie aktivieren oder nicht konfigurieren, wird die Hardwarebeschleunigung aktiviert, sofern kein GPU-Feature explizit blockiert wird.

Wenn Sie diese Richtlinie deaktivieren, ist die Hardwarebeschleunigung deaktiviert.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: HardwareAccelerationModeEnabled
  - GP-Name: Verwenden der Hardwarebeschleunigung, falls verfügbar
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: HardwareAccelerationModeEnabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: HardwareAccelerationModeEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### HideFirstRunExperience

  #### Unterdrücken der ersten Ausführungsumgebung und des Begrüßungsbildschirms

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 80 oder höher

  #### Beschreibung

  Wenn Sie diese Richtlinie aktivieren, werden die Erstausführungsumgebung und der Begrüßungsbildschirm Benutzern nicht angezeigt, wenn sie Microsoft Edge zum ersten Mal ausführen.

Bei den Konfigurationsoptionen, die in der Erstausführungsumgebung dargestellt werden, wird im Browser standardmäßig Folgendes gewählt:

– Auf der neuen Registerkartenseite ist der Feedtyp auf "MSN News" und Layout auf „Inspirational“ festgelegt.

– Der Benutzer wird weiterhin automatisch bei Microsoft Edge angemeldet, wenn es sich bei dem Windows-Konto um den Azure AD- oder MSA-Typ handelt.

- Die Synchronisierung wird nicht standardmäßig aktiviert sein, und die Benutzer werden aufgefordert, auszuwählen, ob beim Starten des Browsers synchronisiert werden soll. Sie können die Richtlinie [ForceSync](#forcesync) oder [SyncDisabled](#syncdisabled) verwenden, um die Synchronisierung und den Zustimmungsdialog für die Synchronisierung zu konfigurieren.

Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, werden die Erstausführungsumgebung und der Begrüßungsbildschirm angezeigt.

Hinweis: die spezifischen Konfigurationsoptionen, die dem Benutzer in der Erstausführungsumgebung angezeigt werden, können auch mit anderen spezifischen Richtlinien verwaltet werden. Sie können die HideFirstRunExperience-Richtlinie in Kombination mit diesen Richtlinien verwenden, um eine bestimmte Browseroberfläche auf Ihren verwalteten Geräten zu konfigurieren. Einige dieser anderen Richtlinien sind:

-[AutoImportAtFirstRun](#autoimportatfirstrun)

-[NewTabPageLocation](#newtabpagelocation)

-[NewTabPageSetFeedType](#newtabpagesetfeedtype)

-[ForceSync](#forcesync)

-[SyncDisabled](#syncdisabled)

-[BrowserSignin](#browsersignin)

-[NonRemovableProfileEnabled](#nonremovableprofileenabled)

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: HideFirstRunExperience
  - GP-Name: Unterdrücken der ersten Ausführungsumgebung und des Begrüßungsbildschirms
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: HideFirstRunExperience
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: HideFirstRunExperience
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### HideInternetExplorerRedirectUXForIncompatibleSitesEnabled

  #### Ausblenden des einmaligen Dialogfelds „Umleitung“ und des Banners auf Microsoft Edge

  
  
  #### Unterstützte Versionen:

  - Unter Windows seit 87 oder später

  #### Beschreibung

  Mit dieser Richtlinie können Sie das einmalige Dialogfeld „Umleitung“ und das Banner deaktivieren. Wenn diese Richtlinie aktiviert ist, wird den Benutzern weder das einmalige Dialogfeld „Umleitung“ noch das Banner angezeigt.
Die Benutzer werden weiterhin an Microsoft Edge umgeleitet, wenn Sie in Internet Explorer auf eine inkompatible Website stoßen, aber Ihre Browserdaten werden nicht importiert.

- Wenn Sie diese Richtlinie aktivieren, wird den Benutzern das Dialogfeld einmalige Dialogfeld „Umleitung“ und das Banner nicht angezeigt. Die Browserdaten der Benutzer werden nicht importiert, wenn eine Umleitung stattfindet.

- Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, wird das Dialogfeld „Einmalige Umleitung“ bei der ersten Umleitung angezeigt, und das persistente Umleitungsbanner wird Benutzern für Sitzungen angezeigt, die mit einer Umleitung beginnen. Die Browserdaten der Benutzer werden jedes Mal importiert, wenn der Benutzer auf eine solche Umleitung stößt (nur wenn der Benutzer dies im einmaligen Dialog akzeptiert hat).


  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - Eindeutiger GP-Name: HideInternetExplorerRedirectUXForIncompatibleSitesEnabled
  - GP-Name: Ausblenden des einmaligen Dialogfelds „Umleitung“ und des Banners auf Microsoft Edge
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: HideInternetExplorerRedirectUXForIncompatibleSitesEnabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### ImportAutofillFormData

  #### Import von AutoFill-Formulardaten zulassen

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Ermöglicht Benutzern das Importieren von AutoFill-Daten aus einem anderen Browser in Microsoft Edge.

Wenn Sie diese Richtlinie aktivieren, wird die Option zum manuellen Importieren von AutoFill-Daten automatisch ausgewählt.

Wenn Sie diese Richtlinie deaktivieren, werden die AutoFill-Formulardaten nicht bei der ersten Ausführung importiert und die Benutzer können die Daten nicht manuell importieren.

Wenn Sie diese Richtlinie nicht konfigurieren, werden die AutoFill-Daten bei der ersten Ausführung importiert, und die Benutzer können auswählen, ob diese Daten während späteren Browsersitzungen manuell importiert werden sollen.

Sie können diese Richtlinie als Empfehlung festlegen. Dies bedeutet, dass Microsoft Edge die AutoFill-Daten bei der ersten Ausführung importiert, aber die Benutzer können während des manuellen Imports die Option **AutoFill-Daten** aktivieren oder deaktivieren.

**Hinweis**: Diese Richtlinie verwaltet zurzeit den Import aus den Browsern Google Chrome (unter Windows 7, 8 und 10 sowie unter macOS) und Mozilla Firefox (unter Windows 7, 8 und 10 sowie unter macOS).

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: ImportAutofillFormData
  - GP-Name: Import von AutoFill-Formulardaten zulassen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): Administrative Templates/Microsoft Edge – Standardeinstellungen (Benutzer können diese außer Kraft setzen)/
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Wertname: ImportAutofillFormData
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: ImportAutofillFormData
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### ImportBrowserSettings

  #### Import von Browsereinstellungen zulassen

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 78 oder höher

  #### Beschreibung

  Ermöglicht Benutzern das Importieren von Browsereinstellungen aus einem anderen Browser in Microsoft Edge.

Wenn Sie diese Richtlinie aktivieren, wird das Kontrollkästchen **Browsereinstellungen** im Dialogfeld **Import von Browserdaten** aktiviert.

Wenn Sie diese Richtlinie deaktivieren, werden die Browsereinstellungen nicht bei der ersten Ausführung importiert und die Benutzer können sie nicht manuell importieren.

Wenn Sie diese Richtlinie nicht konfigurieren, werden die Browsereinstellungen bei der ersten Ausführung importiert, und die Benutzer können auswählen, ob sie während späteren Browsersitzungen manuell importiert werden sollen.

Sie können diese Richtlinie auch als Empfehlung festlegen. Dies bedeutet, dass Microsoft Edge die Einstellungen bei der ersten Ausführung importiert, aber die Benutzer können während des manuellen Imports die Option **Browsereinstellungen** aktivieren oder deaktivieren.

**Hinweis**: Diese Richtlinie verwaltet zurzeit das Importieren aus Google Chrome (unter Windows 7, 8 und 10 sowie unter macOS).

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: ImportBrowserSettings
  - GP-Name: Import von Browsereinstellungen zulassen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): Administrative Templates/Microsoft Edge – Standardeinstellungen (Benutzer können diese außer Kraft setzen)/
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Wertname: ImportBrowserSettings
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: ImportBrowserSettings
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### ImportCookies

  #### Lassen Sie den Import von Cookies zu

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 81 oder höher

  #### Beschreibung

  Ermöglicht Benutzern das Importieren von Cookies aus einem anderen Browser in Microsoft Edge.

Wenn Sie diese Richtlinie deaktivieren, werden Cookies bei der ersten Ausführung nicht importiert.

Wenn Sie diese Richtlinie nicht konfigurieren, werden Cookies bei der ersten Ausführung importiert.

Sie können diese Richtlinie auch als Empfehlung festlegen. Dies bedeutet, dass Microsoft Edge Cookies bei der ersten Ausführung importiert.

**Hinweis**: Diese Richtlinie verwaltet zurzeit das Importieren aus Google Chrome (unter Windows 7, 8 und 10 sowie unter macOS).

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: ImportCookies
  - GP-Name: Import von Cookies zulassen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): Administrative Templates/Microsoft Edge – Standardeinstellungen (Benutzer können diese außer Kraft setzen)/
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Wertname: ImportCookies
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: ImportCookies
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### ImportExtensions

  #### Lassen Sie den Import von Erweiterungen zu

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 81 oder höher

  #### Beschreibung

  Ermöglicht Benutzern das Importieren von Browsererweiterungen aus einem anderen Browser in Microsoft Edge.

Wenn Sie diese Richtlinie aktivieren, wird das Kontrollkästchen **Browsererweiterungen** im Dialogfeld **Import von Browserdaten** aktiviert.

Wenn Sie diese Richtlinie deaktivieren, werden die Browsererweiterungen nicht bei der ersten Ausführung importiert und die Benutzer können sie nicht manuell importieren.

Wenn Sie diese Richtlinie nicht konfigurieren, werden die Browsererweiterungen bei der ersten Ausführung importiert, und die Benutzer können auswählen, ob sie während späteren Browsersitzungen manuell importiert werden sollen.

Sie können diese Richtlinie auch als Empfehlung festlegen. Dies bedeutet, dass Microsoft Edge die Erweiterungen bei der ersten Ausführung importiert, aber die Benutzer können während des manuellen Imports die Option **Favoriten** aktivieren oder deaktivieren.

**Hinweis**: Diese Richtlinie unterstützt zurzeit lediglich das Importieren aus Google Chrome (unter Windows 7, 8 und 10 sowie unter macOS).

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: ImportExtensions
  - GP-Name: Import von Erweiterungen zulassen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): Administrative Templates/Microsoft Edge – Standardeinstellungen (Benutzer können diese außer Kraft setzen)/
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Wertname: ImportExtensions
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: ImportExtensions
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### ImportFavorites

  #### Import von Favoriten zulassen

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Ermöglicht Benutzern das Importieren von Favoriten aus einem anderen Browser in Microsoft Edge.

Wenn Sie diese Richtlinie aktivieren, wird das Kontrollkästchen **Favoriten** im Dialogfeld **Import von Browserdaten** aktiviert.

Wenn Sie diese Richtlinie deaktivieren, werden die Favoriten nicht bei der ersten Ausführung importiert und die Benutzer können sie nicht manuell importieren.

Wenn Sie diese Richtlinie nicht konfigurieren, werden die Favoriten bei der ersten Ausführung importiert, und die Benutzer können auswählen, ob sie während späteren Browsersitzungen manuell importiert werden sollen.

Sie können diese Richtlinie auch als Empfehlung festlegen. Dies bedeutet, dass Microsoft Edge die Favoriten bei der ersten Ausführung importiert, aber die Benutzer können während des manuellen Imports die Option **Favoriten** aktivieren oder deaktivieren.

**Hinweis**: Diese Richtlinie verwaltet zurzeit den Import aus Internet Explorer (unter Windows 7, 8 und 10), Google Chrome (unter Windows 7, 8 und 10 und unter macOS), Mozilla Firefox (unter Windows 7, 8 und 10 sowie unter macOS) und Apple Safari-Browsern (unter macOS).

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: ImportFavorites
  - GP-Name: Import von Favoriten zulassen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): Administrative Templates/Microsoft Edge – Standardeinstellungen (Benutzer können diese außer Kraft setzen)/
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Wertname: ImportFavorites
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: ImportFavorites
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### ImportHistory

  #### Import des Browserverlaufs zulassen

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Ermöglicht Benutzern das Importieren des Browserverlaufs aus einem anderen Browser in Microsoft Edge.

Wenn Sie diese Richtlinie aktivieren, wird das Kontrollkästchen **Browserverlauf** im Dialogfeld **Import von Browserdaten** aktiviert.

Wenn Sie diese Richtlinie deaktivieren, wird der Browserverlauf nicht bei der ersten Ausführung importiert und die Benutzer können die Daten nicht manuell importieren.

Wenn Sie diese Richtlinie nicht konfigurieren, wird der Browserverlauf bei der ersten Ausführung importiert, und die Benutzer können auswählen, ob er während späteren Browsersitzungen manuell importiert werden soll.

Sie können diese Richtlinie auch als Empfehlung festlegen. Dies bedeutet, dass Microsoft Edge den Browserverlauf bei der ersten Ausführung importiert, aber die Benutzer können während des manuellen Imports die Option **Browserverlauf** aktivieren oder deaktivieren.

**Hinweis**: Diese Richtlinie verwaltet zurzeit den Import aus Internet Explorer (unter Windows 7, 8 und 10), Google Chrome (unter Windows 7, 8 und 10 und unter macOS), Mozilla Firefox (unter Windows 7, 8 und 10 sowie unter macOS) und Apple Safari-Browsern (macOS).

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: ImportHistory
  - GP-Name: Import des Browserverlaufs zulassen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): Administrative Templates/Microsoft Edge – Standardeinstellungen (Benutzer können diese außer Kraft setzen)/
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Wertname: ImportHistory
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: ImportHistory
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### ImportHomepage

  #### Import von Startseiteneinstellungen zulassen

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Ermöglicht Benutzern das Importieren von Startseiteneinstellungen aus einem anderen Browser in Microsoft Edge.

Wenn Sie diese Richtlinie aktivieren, wird die Option zum manuellen Importieren von Startseiteneinstellungen automatisch ausgewählt.

Wenn Sie diese Richtlinie deaktivieren, werden die Startseiteneinstellungen nicht bei der ersten Ausführung importiert und die Benutzer können die Daten nicht manuell importieren.

Wenn Sie diese Richtlinie nicht konfigurieren, werden die Startseiteneinstellungen bei der ersten Ausführung importiert, und die Benutzer können auswählen, ob diese Daten während späteren Browsersitzungen manuell importiert werden sollen.

Sie können diese Richtlinie als Empfehlung festlegen. Dies bedeutet, dass Microsoft Edge die Startseiteneinstellungen bei der ersten Ausführung importiert, aber die Benutzer können während des manuellen Imports die Option **Startseite** aktivieren oder deaktivieren.

**Hinweis**: Diese Richtlinie verwaltet zurzeit den Import aus Internet Explorer (unter Windows 7, 8 und 10).

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: ImportHomepage
  - GP-Name: Import von Startseiteneinstellungen zulassen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: ImportHomepage
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: ImportHomepage
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### ImportOpenTabs

  #### Import von Offenen Registerkarten zulassen

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 79 oder höher

  #### Beschreibung

  Ermöglicht Benutzern das Importieren von offenen und angehefteten Tabs aus einem anderen Browser in Microsoft Edge.

Wenn Sie diese Richtlinie aktivieren, wird das Kontrollkästchen **Offene Tabs** im Dialogfeld **Import von Browserdaten** aktiviert.

Wenn Sie diese Richtlinie deaktivieren, werden die offenen Tabs nicht bei der ersten Ausführung importiert und die Benutzer können sie nicht manuell importieren.

Wenn Sie diese Richtlinie nicht konfigurieren, werden die offenen Tabs bei der ersten Ausführung importiert, und die Benutzer können auswählen, ob sie während späteren Browsersitzungen manuell importiert werden sollen.

Sie können diese Richtlinie auch als Empfehlung festlegen. Dies bedeutet, dass Microsoft Edge die offenen Tabs bei der ersten Ausführung importiert, aber die Benutzer können während des manuellen Imports die Option **Offene Tabs** aktivieren oder deaktivieren.

**Hinweis**: Diese Richtlinie unterstützt zurzeit lediglich das Importieren aus Google Chrome (unter Windows 7, 8 und 10 sowie unter macOS).

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: ImportOpenTabs
  - GP-Name: Import von Offenen Registerkarten zulassen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): Administrative Templates/Microsoft Edge – Standardeinstellungen (Benutzer können diese außer Kraft setzen)/
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Wertname: ImportOpenTabs
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: ImportOpenTabs
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### ImportPaymentInfo

  #### Import von Zahlungsinformationen zulassen

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Ermöglicht Benutzern das Importieren von Zahlungsinformationen aus einem anderen Browser in Microsoft Edge.

Wenn Sie diese Richtlinie aktivieren, wird das Kontrollkästchen **Zahlungsinformationen** im Dialogfeld **Import von Browserdaten** aktiviert.

Wenn Sie diese Richtlinie deaktivieren, werden die Zahlungsinformationen nicht bei der ersten Ausführung importiert und die Benutzer können die Daten nicht manuell importieren.

Wenn Sie diese Richtlinie nicht konfigurieren, werden Zahlungsinformationen bei der ersten Ausführung importiert, und die Benutzer können auswählen, ob diese während späteren Browsersitzungen manuell importiert werden sollen.

Sie können diese Richtlinie auch als Empfehlung festlegen. Dies bedeutet, dass Microsoft Edge die Zahlungsinformationen bei der ersten Ausführung importiert, aber die Benutzer können während des manuellen Imports die Option **Zahlungsinformationen** aktivieren oder deaktivieren.

**Hinweis**: Diese Richtlinie verwaltet zurzeit das Importieren aus Google Chrome (unter Windows 7, 8 und 10 sowie unter macOS).

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: ImportPaymentInfo
  - GP-Name: Import von Zahlungsinformationen zulassen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): Administrative Templates/Microsoft Edge – Standardeinstellungen (Benutzer können diese außer Kraft setzen)/
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Wertname: ImportPaymentInfo
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: ImportPaymentInfo
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### ImportSavedPasswords

  #### Import von gespeicherten Kennwörtern zulassen

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Ermöglicht Benutzern das Importieren von gespeicherten Passwörtern aus einem anderen Browser in Microsoft Edge.

Wenn Sie diese Richtlinie aktivieren, wird die Option zum manuellen Importieren von gespeicherten Passwörtern automatisch ausgewählt.

Wenn Sie diese Richtlinie deaktivieren, werden die gespeicherten Passwörter nicht bei der ersten Ausführung importiert und die Benutzer können sie nicht manuell importieren.

Wenn Sie diese Richtlinie nicht konfigurieren, werden die gespeicherten Passwörter bei der ersten Ausführung importiert, und die Benutzer können auswählen, ob sie während späteren Browsersitzungen manuell importiert werden sollen.

Sie können diese Richtlinie als Empfehlung festlegen. Dies bedeutet, dass Microsoft Edge die gespeicherten Passwörter bei der ersten Ausführung importiert, aber die Benutzer können während des manuellen Imports die Option **gespeicherten Passwörter** aktivieren oder deaktivieren.

**Hinweis**: Diese Richtlinie verwaltet zurzeit den Import aus Internet Explorer (unter Windows 7, 8 und 10), Google Chrome (unter Windows 7, 8 und 10 und unter macOS) und Mozilla Firefox (unter Windows 7, 8 und 10 sowie unter macOS).

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: ImportSavedPasswords
  - GP-Name: Import von gespeicherten Kennwörtern zulassen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): Administrative Templates/Microsoft Edge – Standardeinstellungen (Benutzer können diese außer Kraft setzen)/
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Wertname: ImportSavedPasswords
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: ImportSavedPasswords
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### ImportSearchEngine

  #### Import von Suchmaschinen-Einstellungen zulassen

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Ermöglicht Benutzern das Importieren von Suchmaschineneinstellungen aus einem anderen Browser in Microsoft Edge.

Wenn Sie diese Richtlinie aktivieren, wird die Option zum manuellen Importieren von Suchmaschineneinstellungen automatisch ausgewählt.

Wenn Sie diese Richtlinie deaktivieren, werden die Suchmaschineneinstellungen nicht bei der ersten Ausführung importiert und die Benutzer können sie nicht manuell importieren.

Wenn Sie diese Richtlinie nicht konfigurieren, werden die Suchmaschineneinstellungen bei der ersten Ausführung importiert, und die Benutzer können auswählen, ob diese Daten während späteren Browsersitzungen manuell importiert werden sollen.

Sie können diese Richtlinie als Empfehlung festlegen. Dies bedeutet, dass Microsoft Edge die Suchmaschineneinstellungen bei der ersten Ausführung importiert, aber die Benutzer können während des manuellen Imports die Option **Suchmaschineneinstellungen** aktivieren oder deaktivieren.

**Hinweis**: Diese Richtlinie verwaltet zurzeit den Import aus Internet Explorer (unter Windows 7, 8 und 10).

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: ImportSearchEngine
  - GP-Name: Import von Suchmaschinen-Einstellungen zulassen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): Administrative Templates/Microsoft Edge – Standardeinstellungen (Benutzer können diese außer Kraft setzen)/
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Wertname: ImportSearchEngine
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: ImportSearchEngine
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### ImportShortcuts

  #### Lassen Sie den Import von Verknüpfungen zu

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 81 oder höher

  #### Beschreibung

  Ermöglicht Benutzern das Importieren von Verknüpfungen aus einem anderen Browser in Microsoft Edge.

Wenn Sie diese Richtlinie deaktivieren, werden Verknüpfungen bei der ersten Ausführung nicht importiert.

Wenn Sie diese Richtlinie nicht konfigurieren, werden Verknüpfungen bei der ersten Ausführung importiert.

Sie können diese Richtlinie auch als Empfehlung festlegen. Dies bedeutet, dass Microsoft Edge Verknüpfungen bei der ersten Ausführung importiert.

**Hinweis**: Diese Richtlinie verwaltet zurzeit das Importieren aus Google Chrome (unter Windows 7, 8 und 10 sowie unter macOS).

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: ImportShortcuts
  - GP-Name: Import von Verknüpfungen zulassen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): Administrative Templates/Microsoft Edge – Standardeinstellungen (Benutzer können diese außer Kraft setzen)/
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Wertname: ImportShortcuts
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: ImportShortcuts
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### InPrivateModeAvailability

  #### Konfigurieren der InPrivate-Modus-Verfügbarkeit

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Gibt an, ob der Benutzer Seiten im InPrivate-Modus in Microsoft Edge öffnen kann.

Wenn Sie diese Richtlinie nicht konfigurieren oder auf „Enabled“ setzen, können Benutzer Seiten im InPrivate-Modus öffnen.

Setzen Sie diese Richtlinie auf „Disabled“, um Benutzer an der Verwendung des InPrivate-Modus zu hindern.

Setzen Sie diese Richtlinie auf „Forced“, um den InPrivate-Modus immer zu verwenden.

Zuordnung von Richtlinienoptionen:

* Enabled (0) = InPrivate-Modus verfügbar

* Disabled (1) = InPrivate-Modus deaktiviert

* Forced (2) = InPrivate-Modus erzwingen

Verwenden Sie die vorstehenden Informationen, wenn Sie diese Richtlinie konfigurieren.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Ganze Zahl

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: InPrivateModeAvailability
  - GP-Name: Konfigurieren der InPrivate-Modus-Verfügbarkeit
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: InPrivateModeAvailability
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: InPrivateModeAvailability
  - Beispielwert:
``` xml
<integer>1</integer>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### InsecureFormsWarningsEnabled

  #### Aktivieren von Warnungen für unsichere Formulare

  
  
  #### Unterstützte Versionen:

  - Unter Windows und macOS ab 86 oder höher

  #### Beschreibung

  Mit dieser Richtlinie wird der Umgang mit unsicheren Formulare (Formulare, die über HTTP übermittelt werden) gesteuert, die in sichere (HTTPS) Websites im Browser eingebettet sind.
Wenn Sie diese Richtlinie aktivieren oder nicht festlegen, wird eine ganzseitige Warnung angezeigt, wenn ein unsicheres Formular gesendet wird. Außerdem wird neben den Formularfeldern, in denen der Fokus liegt, eine Warnmeldung angezeigt, und das automatische Ausfüllen wird für diese Formulare deaktiviert.
Wenn Sie diese Richtlinie deaktivieren, werden für unsichere Formulare keine Warnungen angezeigt, und das automatische Ausfüllen funktioniert normal.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - Eindeutiger GP-Name: InsecureFormsWarningsEnabled
  - GP-Name: Warnungen für unsichere Formulare aktivieren
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: InsecureFormsWarningsEnabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: InsecureFormsWarningsEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### IntensiveWakeUpThrottlingEnabled

  #### Regulierung des IntensiveWakeUpThrottlingEnabled-Features

  
  
  #### Unterstützte Versionen:

  - Auf Windows und MacOS ab 85 oder später

  #### Beschreibung

  Wenn aktiviert, bewirkt das IntensiveWakeUpThrottling-Feature, dass Javascript-Zeitgeber in Registerkarten im Hintergrund aggressiv gedrosselt und zusammengefügt werden, mit einer Laufzeit von nicht mehr als einmal pro Minute, nachdem eine Seite in den Hintergrund verschoben wurde für 5 Minuten oder mehr. 

Dies ist eine Webstandard-Richtlinienkonforme-Feature, könnte aber zu einem Bruch der Funktionalität auf manchen Websites führen, indem bestimme Ausführungen bis zu einer Minute verzögert werden. Jedoch wird der CPU und die Batterie erheblich gespart, wenn es aktiviert ist.  Weitere Informationen finden Sie unter https://bit.ly/30b1XR4.

Wenn Sie diese Richtlinie aktivieren, wird das Feature zwangsaktiviert, und die Benutzer können diese Einstellung nicht außer Kraft setzen.
Wenn Sie diese Richtlinie aktivieren, wird das Feature zwangsdeaktiviert, und die Benutzer können diese Einstellung nicht außer Kraft setzen.
Wenn Sie diese Richtlinie nicht konfigurieren, wird das Feature durch seine eigene interne Logik gesteuert. Benutzer können diese Einstellung manuell konfigurieren.

Beachten Sie, dass die Richtlinie pro Renderer angewendet wird, wobei der aktuellste Wert der Richtlinieneinstellung beim Start eines Renderer-Prozesses gilt. Der vollständige Neustart ist erforderlich, um sicherzustellen, dass alle geladenen Registerkarten eine einheitliche Richtlinieneinstellung erhalten. Es ist harmlos, dass Prozesse mit unterschiedlichen Werten dieser Richtlinie ausgeführt werden.


  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - Eindeutiger Name des GP: IntensiveWakeUpThrottlingEnabled
  - GP-Name: Steuern des IntensiveWakeUpThrottling-Features
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: IntensiveWakeUpThrottlingEnabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Name des Einstellungsschlüssels: IntensiveWakeUpThrottlingEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### InternetExplorerIntegrationEnhancedHangDetection

  #### Konfigurieren der Ermittlung von Anwendungsstillständen für Internet Explorer-Modus

  
  
  #### Unterstützte Versionen:

  - Unter Windows seit 84 oder später

  #### Beschreibung

  Die verbesserte Ermittlung von Anwendungsstillständen ist ein differenzierterer Ansatz zum Erkennen von Webseiten die nicht reagieren im Internet Explorer-Modus, im Gegensatz zu dem, welches der eigenständige Internet Explorer benutzt. Wenn ein Anwendungsstillstand einer Webseite erkannt wird, wendet der Browser eine Abschwächung an, um zu verhindern, dass der Rest des Browsers hängen bleibt.

Diese Einstellung ermöglicht es Ihnen, die Verwendung von Enhanced Hang Detection für den Fall zu konfigurieren, dass Sie mit einer ihrer Websites nicht kompatible Probleme haben. Es wird empfohlen, diese Richtlinie nur zu deaktivieren, wenn Benachrichtigungen wie "(Website) reagiert nicht" im Internet Explorer-Modus, aber nicht in eigenständigem Internet Explorer angezeigt wird.

Diese Einstellung funktioniert in Verbindung mit: [InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) auf „IEMode“ und der Richtlinie „[InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist)“, wenn die Liste mindestens einen Eintrag hat.

Wenn Sie diese Richtlinie auf „Enabled“ setzen oder Sie nicht konfigurieren, verwenden Websites im Internet Explorer die erweiterte Anwendungsstillstand-Erkennung.

Wenn Sie diese Richtlinie auf „Disabled“ setzen, ist die Option „erweiterte Anwendungsstillstand-Erkennung“ deaktiviert, und die Benutzer erhalten die normale Anwendungsstillstand-Erkennung des Internet Explorers.

Weitere Informationen zum Internet Explorer-Modus finden Sie unter [https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210)

Zuordnung von Richtlinienoptionen:

* Disabled (0) = Erweiterte Anwendungsstillstand-Erkennung deaktiviert

* Enabled (1) = Erweiterte Anwendungsstillstand-Erkennung aktiviert

Verwenden Sie die vorstehenden Informationen, wenn Sie diese Richtlinie konfigurieren.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Ganze Zahl

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - Eindeutiger Name des GP: InternetExplorerIntegrationEnhancedHangDetection
  - GP-Name: Konfigurieren der erweiterten Anwendungsstillstand-Erkennung für Internet Explorer-Modus
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: InternetExplorerIntegrationEnhancedHangDetection
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### InternetExplorerIntegrationLevel

  #### Konfigurieren der Internet Explorer-Integration

  
  
  #### Unterstützte Versionen:

  - Auf Windows ab 77 oder höher

  #### Beschreibung

  Informationen zum Konfigurieren der optimalen Benutzeroberfläche für den Internet Explorer-Modus finden Sie unter [https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210)

Zuordnung von Richtlinienoptionen:

* None (0) = keine

* IEMode (1) = Internet Explorer-Modus

* NeedIE (2) = Benötigt Internet Explorer 11

Verwenden Sie die vorstehenden Informationen, wenn Sie diese Richtlinie konfigurieren.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Ganze Zahl

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: InternetExplorerIntegrationLevel
  - GP-Name: Konfigurieren der Internet Explorer-Integration
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: InternetExplorerIntegrationLevel
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### InternetExplorerIntegrationSiteList

  #### Enterprise Mode Site List konfigurieren

  
  
  #### Unterstützte Versionen:

  - Auf Windows ab 78 oder höher

  #### Beschreibung

  Informationen zum Konfigurieren der optimalen Benutzeroberfläche für den Internet Explorer-Modus finden Sie unter [https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210)

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Zeichenfolge

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: InternetExplorerIntegrationSiteList
  - GP-Name: Enterprise Mode Site List konfigurieren
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: InternetExplorerIntegrationSiteList
  - Werttyp: REG_SZ

  ##### Beispielwert:

```
"https://internal.contoso.com/sitelist.xml"
```

  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### InternetExplorerIntegrationSiteRedirect

  #### Angeben, wie sich „seiteninterne“ Navigationen zu nicht konfigurierten Websites verhalten, wenn sie von Seiten im Internet Explorer-Modus gestartet werden

  
  
  #### Unterstützte Versionen:

  - Auf Windows ab 81 oder höher

  #### Beschreibung

  Eine „seiteninterne“ Navigation wird über einen Link, ein Skript oder ein Formular auf der aktuellen Seite gestartet. Es kann sich auch um eine serverseitige Umleitung eines früheren Versuchs der „seiteninternen“ Navigation handeln. Umgekehrt kann ein Benutzer eine nicht „seiteninterne“ Navigation, die von der aktuellen Seite unabhängig ist, auf verschiedene Weise mithilfe der Browsersteuerelemente starten. Zum Beispiel über die Adressleiste, die Zurück-Schaltfläche oder einen Favoritenlink.

Mit dieser Einstellung können Sie festlegen, ob Navigationen, die von im Internet Explorer-Modus geladenen Seiten zu nicht konfigurierten Websites führen (die nicht in der Liste der Unternehmens Modus-Websites konfiguriert sind), zurück zu Microsoft Edge wechseln oder im Internet Explorer-Modus verbleiben.

Diese Einstellung funktioniert in Verbindung mit: [InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) auf „IEMode“ und der Richtlinie „[InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist)“, wenn die Liste mindestens einen Eintrag hat.

Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, werden nur die im Internet Explorer-Modus konfigurierten Websites in diesem Modus geöffnet. Alle Websites, die nicht zum Öffnen im Internet Explorer-Modus konfiguriert sind, werden zurück zu Microsoft Edge umgeleitet.

Wenn Sie diese Richtlinie auf „Default“ setzen, werden nur Seiten, die im Internet Explorer-Modus konfigurierten sind, geöffnet. Alle Websites, die nicht zum Öffnen im Internet Explorer-Modus konfiguriert sind, werden zurück zu Microsoft Edge umgeleitet.

Wenn Sie diese Richtlinie auf „AutomaticNavigationsOnly“ setzen, erhalten Sie die Standardeinstellung, mit Ausnahme, dass alle automatischen Navigationselemente (wie z.B. 302-Umleitungen) zu nicht-konfigurierten Webseiten im Internet Explorer-Modus beibehalten werden.

Wenn Sie diese Richtlinie auf „AllInPageNavigations“ setzen, werden alle Navigationen von Seiten zu nicht-konfigurierten Seiten, die im IE-Modus geladen wurden im Internet Explorer-Modus beibehalten (am wenigsten empfohlen).

Weitere Informationen zum Internet Explorer-Modus finden Sie unter [https://go.microsoft.com/fwlink/?linkid=2105106](https://go.microsoft.com/fwlink/?linkid=2105106)

Zuordnung von Richtlinienoptionen:

* Default (0) = Standard

* AutomaticNavigationsOnly (1) = Nur automatische Navigationen im Internet Explorer-Modus beibehalten

* AllInPageNavigations (2) = Alle seiteninternen Navigationen im Internet Explorer-Modus beibehalten

Verwenden Sie die vorstehenden Informationen, wenn Sie diese Richtlinie konfigurieren.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Ganze Zahl

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: InternetExplorerIntegrationSiteRedirect
  - GP-Name: Angeben, wie sich „seiteninterne“ Navigationen zu nicht konfigurierten Websites verhalten, wenn sie von Seiten im Internet Explorer-Modus gestartet werden
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: InternetExplorerIntegrationSiteRedirect
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000000
```

  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### InternetExplorerIntegrationTestingAllowed

  #### Internet Explorer-Modus-Tests zulassen

  
  
  #### Unterstützte Versionen:

  - Unter Windows 86 oder später

  #### Beschreibung

  Diese Richtlinie ermöglicht Benutzern das Testen von Anwendungen im Internet Explorer-Modus durch Öffnen eines IE-Modus-Tabs in Microsoft Edge.

Dies ist über das Menü "Weitere Tools" durch Auswahl der Option "Websites im Internet Explorer-Modus öffnen" möglich.

Darüber hinaus können Benutzer ihre Anwendungen in einem modernen Browser testen, ohne Anwendungen aus der Websiteliste zu entfernen, indem sie die Option "Websites im Edge-Modus öffnen" verwenden.

Diese Einstellung funktioniert in Verbindung mit: [InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) auf „IEMode“ und der Richtlinie „[InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist)“, wenn die Liste mindestens einen Eintrag hat.

Wenn Sie diese Richtlinie aktivieren, wird die Option "Websites im Internet Explorer-Modus öffnen" unter "Weitere Tools" angezeigt. Benutzer können ihre Websites im Internet Explorer-Modus in diesem Tab anzeigen. Die Option "Websites im Edge-Modus öffnen" wird auch unter "Weitere Tools" angezeigt, um das Testen von Websites in einem modernen Browser zu ermöglichen, ohne sie aus der Websiteliste zu entfernen.

Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, werden die Optionen "Im Internet Explorer-Modus öffnen" und "Im Edge-Modus öffnen" nicht im Menü "Weitere Tools" angezeigt. Benutzer können diese Optionen jedoch mit dem --ie-mode-test-Flag konfigurieren.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - Eindeutiger GP-Name: InternetExplorerIntegrationTestingAllowed
  - GP-Name: Internet Explorer-Modus-Tests zulassen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: InternetExplorerIntegrationTestingAllowed
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000000
```

  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### IsolateOrigins

  #### Aktivieren der Website-Isolation für bestimmte Ursprünge

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Legt Ursprünge fest, die in Ihrem eigenen Prozess isoliert ausgeführt werden sollen.

Diese Richtlinie isoliert außerdem die von Unterdomänen benannten Ursprünge. so wird beispielsweisedurch die Angabe von https://contoso.com/ https://foo.contoso.com/ als Bestandteil der https://contoso.com/-Website isoliert.

Wenn die Richtlinie aktiviert ist, wird jeder der in einer durch Trennzeichen getrennten Liste benannten Ursprünge in einem eigenen Prozess ausgeführt.

Wenn Sie diese Richtlinie deaktivieren, werden die Funktionen "IsolateOrigins" und "SitePerProcess" deaktiviert. Benutzer können die Richtlinie für "IsolateOrigins" weiterhin manuell über Befehlszeilenkennzeichnungen aktivieren.

Wenn Sie diese Richtlinie nicht konfigurieren, können Benutzer diese Einstellung ändern.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Zeichenfolge

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: IsolateOrigins
  - GP-Name: Aktivieren der Website-Isolation für bestimmte Ursprünge
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: IsolateOrigins
  - Werttyp: REG_SZ

  ##### Beispielwert:

```
"https://contoso.com/,https://fabrikam.com/"
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: IsolateOrigins
  - Beispielwert:
``` xml
<string>https://contoso.com/,https://fabrikam.com/</string>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### LocalProvidersEnabled

  #### Vorschläge von lokalen Anbietern zulassen

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 83 oder höher

  #### Beschreibung

  Lässt Vorschläge von Vorschlagsanbietern auf dem Gerät (lokale Anbieter), z.B. "Favoriten" und "Browserverlauf", in der Adressleiste von Microsoft Edge und der Liste der automatischen Vorschläge, zu.

Wenn Sie diese Richtlinie aktivieren, werden Vorschläge von lokalen Anbietern verwendet.

Wenn Sie diese Richtlinie deaktivieren, werden keine Vorschläge von lokalen Anbietern verwendet. Vorschläge für lokalen Verlauf und lokale Favoriten werden nicht angezeigt.

Wenn Sie diese Richtlinie nicht konfigurieren, sind Vorschläge von lokalen Anbietern zulässig, aber der Benutzer kann dies mithilfe der Umschaltfläche in "Einstellungen" ändern.

Beachten Sie, dass einige Features möglicherweise nicht verfügbar sind, wenn eine Richtlinie zum Deaktivieren dieses Features angewendet wurde. So sind beispielsweise die Vorschläge zum Durchsuchen des Verlaufs nicht verfügbar, wenn Sie die Richtlinie [SavingBrowserHistoryDisabled](#savingbrowserhistorydisabled) aktivieren.

Zur Anwendung dieser Richtlinie ist ein Browser-Neustart erforderlich.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: LocalProvidersEnabled
  - GP-Name: Vorschläge von lokalen Anbietern zulassen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): Administrative Templates/Microsoft Edge – Standardeinstellungen (Benutzer können diese außer Kraft setzen)/
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Wertname: LocalProvidersEnabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000000
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: LocalProvidersEnabled
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### ManagedFavorites

  #### Favoriten konfigurieren

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Konfiguriert eine Liste der verwalteten Favoriten.

Die Richtlinie erstellt eine Liste von Favoriten. Jeder Favorit enthält die Schlüssel "Name" und "URL", die den Namen des Favoriten und dessen Ziel enthalten. Sie können einen Unterordner konfigurieren, indem Sie einen Favoriten ohne einen "URL"-Schlüssel, aber mit einem weiteren "Children"-Schlüssel definieren, der eine Liste der oben definierten Favoriten enthält (von denen einige möglicherweise wieder Ordner sind). Microsoft Edge ändert unvollständige URLs so, als ob Sie über die Adressleiste übermittelt wurden. so wird beispielsweise "microsoft.com" zu "https://microsoft.com/".

Diese Favoriten werden in einem Ordner abgelegt, der vom Benutzer nicht geändert werden kann (aber der Benutzer kann festlegen, ihn auf der Favoritenleiste auszublenden). Standardmäßig lautet der Ordnername "verwaltete Favoriten". Sie können ihn aber auch ändern, indem Sie zur Favoritenliste ein Wörterbuch mit dem Schlüssel "toplevel_name" mit dem gewünschten Ordnernamen als Wert hinzufügen.

Verwaltete Favoriten werden nicht mit dem Benutzerkonto synchronisiert und können nicht durch Erweiterungen geändert werden.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Dictionary

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: ManagedFavorites
  - GP-Name: Favoriten konfigurieren
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: ManagedFavorites
  - Werttyp: REG_SZ

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\ManagedFavorites = [
  {
    "toplevel_name": "My managed favorites folder"
  }, 
  {
    "name": "Microsoft", 
    "url": "microsoft.com"
  }, 
  {
    "name": "Bing", 
    "url": "bing.com"
  }, 
  {
    "children": [
      {
        "name": "Microsoft Edge Insiders", 
        "url": "www.microsoftedgeinsider.com"
      }, 
      {
        "name": "Microsoft Edge", 
        "url": "www.microsoft.com/windows/microsoft-edge"
      }
    ], 
    "name": "Microsoft Edge links"
  }
]
```

  ##### Kompakter Beispielwert:

  ```
  SOFTWARE\Policies\Microsoft\Edge\ManagedFavorites = [{"toplevel_name": "My managed favorites folder"}, {"name": "Microsoft", "url": "microsoft.com"}, {"name": "Bing", "url": "bing.com"}, {"children": [{"name": "Microsoft Edge Insiders", "url": "www.microsoftedgeinsider.com"}, {"name": "Microsoft Edge", "url": "www.microsoft.com/windows/microsoft-edge"}], "name": "Microsoft Edge links"}]
  ```
  

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: ManagedFavorites
  - Beispielwert:
``` xml
<key>ManagedFavorites</key>
<array>
  <dict>
    <key>toplevel_name</key>
    <string>My managed favorites folder</string>
  </dict>
  <dict>
    <key>name</key>
    <string>Microsoft</string>
    <key>url</key>
    <string>microsoft.com</string>
  </dict>
  <dict>
    <key>name</key>
    <string>Bing</string>
    <key>url</key>
    <string>bing.com</string>
  </dict>
  <dict>
    <key>children</key>
    <array>
      <dict>
        <key>name</key>
        <string>Microsoft Edge Insiders</string>
        <key>url</key>
        <string>www.microsoftedgeinsider.com</string>
      </dict>
      <dict>
        <key>name</key>
        <string>Microsoft Edge</string>
        <key>url</key>
        <string>www.microsoft.com/windows/microsoft-edge</string>
      </dict>
    </array>
    <key>name</key>
    <string>Microsoft Edge links</string>
  </dict>
</array>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### ManagedSearchEngines

  #### Verwalten von Suchmaschinen

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Sie können Sie eine Liste mit bis zu 10 Suchmaschinen konfigurieren, von denen eine als Standardsuchmaschine gekennzeichnet sein muss.
Sie müssen die Codierung nicht angeben. Beginnend mit Microsoft Edge 80 sind die suggest_url-und image_search_url-Parameter optional. Der optionale Parameter image_search_post_params (besteht aus durch Trennzeichen getrennten Namen/Wert-Paaren), ist ab Microsoft Edge 80 verfügbar.

Beginnend mit Microsoft Edge 83 können Sie Suchmaschinen-Ermittlungen mit dem optionalen Parameter allow_search_engine_discovery aktivieren. Dieser Parameter muss das erste Element in der Liste sein. Wenn allow_search_engine_discovery nicht angegeben ist, wird die Suchmaschinen-Ermittlung standardmäßig deaktiviert. Beginnend mit Microsoft Edge 84 können Sie diese Richtlinie als empfohlene Richtlinie festlegen, um die Ermittlung des Suchanbieters zu ermöglichen. Sie müssen den optionalen Parameter allow_search_engine_discovery nicht hinzufügen.

Wenn Sie diese Richtlinie aktivieren, können Benutzer in der Liste keine Suchmaschinen hinzufügen, entfernen oder ändern. Benutzer können ihre Standardsuchmaschine auf eine beliebige Suchmaschine in der Liste festlegen.

Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, können Benutzer die Suchmaschinenliste nach Belieben ändern.

Wenn die Richtlinie [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl) festgelegt ist, wird diese Richtlinie (ManagedSearchEngines) ignoriert. Der Benutzer muss seinen Browser neu starten, um die Anwendung dieser Richtlinie abzuschließen.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Dictionary

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: ManagedSearchEngines
  - GP-Name: Verwalten von Suchmaschinen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): Administrative Templates/Microsoft Edge – Standardeinstellungen (Benutzer können diese außer Kraft setzen)/
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Wertname: ManagedSearchEngines
  - Werttyp: REG_SZ

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\ManagedSearchEngines = [
  {
    "allow_search_engine_discovery": true
  }, 
  {
    "is_default": true, 
    "keyword": "example1.com", 
    "name": "Example1", 
    "search_url": "https://www.example1.com/search?q={searchTerms}", 
    "suggest_url": "https://www.example1.com/qbox?query={searchTerms}"
  }, 
  {
    "image_search_post_params": "content={imageThumbnail},url={imageURL},sbisrc={SearchSource}", 
    "image_search_url": "https://www.example2.com/images/detail/search?iss=sbiupload", 
    "keyword": "example2.com", 
    "name": "Example2", 
    "search_url": "https://www.example2.com/search?q={searchTerms}", 
    "suggest_url": "https://www.example2.com/qbox?query={searchTerms}"
  }, 
  {
    "encoding": "UTF-8", 
    "image_search_url": "https://www.example3.com/images/detail/search?iss=sbiupload", 
    "keyword": "example3.com", 
    "name": "Example3", 
    "search_url": "https://www.example3.com/search?q={searchTerms}", 
    "suggest_url": "https://www.example3.com/qbox?query={searchTerms}"
  }, 
  {
    "keyword": "example4.com", 
    "name": "Example4", 
    "search_url": "https://www.example4.com/search?q={searchTerms}"
  }
]
```

  ##### Kompakter Beispielwert:

  ```
  SOFTWARE\Policies\Microsoft\Edge\ManagedSearchEngines = [{"allow_search_engine_discovery": true}, {"is_default": true, "keyword": "example1.com", "name": "Example1", "search_url": "https://www.example1.com/search?q={searchTerms}", "suggest_url": "https://www.example1.com/qbox?query={searchTerms}"}, {"image_search_post_params": "content={imageThumbnail},url={imageURL},sbisrc={SearchSource}", "image_search_url": "https://www.example2.com/images/detail/search?iss=sbiupload", "keyword": "example2.com", "name": "Example2", "search_url": "https://www.example2.com/search?q={searchTerms}", "suggest_url": "https://www.example2.com/qbox?query={searchTerms}"}, {"encoding": "UTF-8", "image_search_url": "https://www.example3.com/images/detail/search?iss=sbiupload", "keyword": "example3.com", "name": "Example3", "search_url": "https://www.example3.com/search?q={searchTerms}", "suggest_url": "https://www.example3.com/qbox?query={searchTerms}"}, {"keyword": "example4.com", "name": "Example4", "search_url": "https://www.example4.com/search?q={searchTerms}"}]
  ```
  

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: ManagedSearchEngines
  - Beispielwert:
``` xml
<key>ManagedSearchEngines</key>
<array>
  <dict>
    <key>allow_search_engine_discovery</key>
    <true/>
  </dict>
  <dict>
    <key>is_default</key>
    <true/>
    <key>keyword</key>
    <string>example1.com</string>
    <key>name</key>
    <string>Example1</string>
    <key>search_url</key>
    <string>https://www.example1.com/search?q={searchTerms}</string>
    <key>suggest_url</key>
    <string>https://www.example1.com/qbox?query={searchTerms}</string>
  </dict>
  <dict>
    <key>image_search_post_params</key>
    <string>content={imageThumbnail},url={imageURL},sbisrc={SearchSource}</string>
    <key>image_search_url</key>
    <string>https://www.example2.com/images/detail/search?iss=sbiupload</string>
    <key>keyword</key>
    <string>example2.com</string>
    <key>name</key>
    <string>Example2</string>
    <key>search_url</key>
    <string>https://www.example2.com/search?q={searchTerms}</string>
    <key>suggest_url</key>
    <string>https://www.example2.com/qbox?query={searchTerms}</string>
  </dict>
  <dict>
    <key>encoding</key>
    <string>UTF-8</string>
    <key>image_search_url</key>
    <string>https://www.example3.com/images/detail/search?iss=sbiupload</string>
    <key>keyword</key>
    <string>example3.com</string>
    <key>name</key>
    <string>Example3</string>
    <key>search_url</key>
    <string>https://www.example3.com/search?q={searchTerms}</string>
    <key>suggest_url</key>
    <string>https://www.example3.com/qbox?query={searchTerms}</string>
  </dict>
  <dict>
    <key>keyword</key>
    <string>example4.com</string>
    <key>name</key>
    <string>Example4</string>
    <key>search_url</key>
    <string>https://www.example4.com/search?q={searchTerms}</string>
  </dict>
</array>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### MaxConnectionsPerProxy

  #### Maximale Anzahl gleichzeitiger Verbindungen mit dem Proxyserver

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Gibt die maximale Anzahl gleichzeitiger Verbindungen mit dem Proxyserver an.

Einige Proxyserver können eine hohe Anzahl gleichzeitiger Verbindungen pro Client nicht verarbeiten. Dies können Sie lösen, indem Sie diese Richtlinie auf einen niedrigeren Wert festlegen.

Der Wert dieser Richtlinie sollte kleiner als 100 und höher als 6 sein. Der Standardwert lautet %%amp;quot;32%%amp;quot;.

Einige Web-Apps sind bekannt dafür, viele Verbindungen mit hängenden GETs zu blockieren – das Senken der maximalen Anzahl von Verbindungen unter 32 kann dazu führen, dass die Netzwerkaktivität des Browsers hängenbleibt, wenn zu viele dieser Arten von Webanwendungen geöffnet sind.

Wenn Sie diese Richtlinie nicht konfigurieren, wird der Standardwert (32) verwendet.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Ganze Zahl

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: MaxConnectionsPerProxy
  - GP-Name: Maximale Anzahl gleichzeitiger Verbindungen mit dem Proxyserver
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: MaxConnectionsPerProxy
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000020
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: MaxConnectionsPerProxy
  - Beispielwert:
``` xml
<integer>32</integer>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### MediaRouterCastAllowAllIPs

  #### Zulassen, dass Google Cast eine Verbindung mit den Cast-Geräten aller IP-Adressen herstellt

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Aktivieren Sie diese Richtlinie, damit Google Cast eine Verbindung mit Cast-Geräten auf allen IP-Adressen herstellt – nicht nur zu privaten RFC1918/RFC4193-Adressen.

Deaktivieren Sie diese Richtlinie, um Google Cast auf private RFC1918/RFC4193-Adressen zu beschränken.

Wenn Sie diese Richtlinie nicht konfigurieren, stellt Google Cast nur Verbindungen zu Cast-Geräten unter RFC1918/RFC4193-Adressen her, es sei denn, Sie aktivieren das Feature CastAllowAllIPs.

Wenn die Richtlinie [EnableMediaRouter](#enablemediarouter) deaktiviert ist, hat diese Richtlinie keine Wirkung.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: MediaRouterCastAllowAllIPs
  - GP-Name: Zulassen, dass Google Cast eine Verbindung mit den Cast-Geräten aller IP-Adressen herstellt
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: MediaRouterCastAllowAllIPs
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000000
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: MediaRouterCastAllowAllIPs
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### MetricsReportingEnabled

  #### Aktivieren der Berichterstellung für Nutzung und Absturz (veraltet).

  >VERALTET: Diese Richtlinie ist veraltet. Sie wird zurzeit unterstützt, aber in einer zukünftigen Version als veraltet behandelt.
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Diese Einstellung ist veraltet. Es wird derzeit unterstützt, wird jedoch in Microsoft Edge 89 veraltet sein. Diese Richtlinie wird durch die neue Richtlinie ersetzt: [DiagnosticData](#diagnosticdata) für Windows 7, Windows 8 und macOS. Diese Richtlinie wird durch "Telemetrie unter Win 10 zulassen" ([https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569)) ersetzt.

Diese Richtlinie ermöglicht die Erstellung von Berichten zu Nutzungs- und Absturzdaten über Microsoft Edge an Microsoft.

Aktivieren Sie diese Richtlinie, um Berichte zu Nutzungs- und Absturzdaten an Microsoft zu senden. Deaktivieren Sie diese Richtlinie, wenn Sie die Daten nicht an Microsoft senden möchten. In beiden Fällen können Benutzer die Einstellung weder ändern noch außer Kraft setzen.

Wenn Sie diese Richtlinie unter Windows 10 nicht konfigurieren, verwendet Microsoft Edge standardmäßig die Windows-Diagnosedateneinstellung. Wenn diese Richtlinie aktiviert ist, sendet Microsoft Edge nur dann Nutzungsdaten, wenn die Einstellung für Windows-Diagnosedaten auf Erweitert oder Vollständig festgelegt ist. Wenn diese Richtlinie deaktiviert ist, werden von Microsoft Edge keine Nutzungsdaten gesendet. Absturzdaten werden basierend auf der Einstellung für Windows-Diagnosedaten gesendet. Weitere Informationen zu den Einstellungen für Windows-Diagnosedaten finden Sie unter [https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569)

Unter Windows 7, Windows 8 und macOS steuert diese Richtlinie das Senden von Nutzungs- und Absturzdaten. Wenn Sie diese Richtlinie nicht konfigurieren, verwendet Microsoft Edge standardmäßig die Präferenz des Benutzers.

Um diese Richtlinie zu aktivieren, muss [SendSiteInfoToImproveServices](#sendsiteinfotoimproveservices) auf Aktiviert gesetzt sein. Wenn [MetricsReportingEnabled](#metricsreportingenabled) oder [SendSiteInfoToImproveServices](#sendsiteinfotoimproveservices) nicht konfiguriert oder deaktiviert ist, werden diese Daten nicht an Microsoft gesendet.

Diese Richtlinie ist nur für Windows-Instanzen verfügbar, die mit einer Microsoft Active Directory-Domäne verknüpft sind, Windows 10 Pro- oder Enterprise-Instanzen, die für die Geräteverwaltung registriert sind, oder MacOS-Instanzen, die über MDM verwaltet oder über MCX einer Domäne beigetreten sind.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: MetricsReportingEnabled
  - GP-Name: Aktivieren der Berichterstellung für Nutzung und Absturz (veraltet).
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: MetricsReportingEnabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: MetricsReportingEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### NativeWindowOcclusionEnabled

  #### Native Window Occlusion aktivieren

  
  
  #### Unterstützte Versionen:

  - Unter Windows seit 84 oder später

  #### Beschreibung

  Aktiviert Native Window Occlusion in Microsoft Edge.

Wenn Sie diese Einstellung aktivieren, wird Microsoft Edge zum Verringern der benötigten CPU-Leistung und des Stromverbrauchs erkennen, ob ein Fenster von anderen Fenstern überlagert wird, und das Zeichnen der überdeckten Pixel wird unterbrochen.

Wenn Sie diese Einstellung deaktivieren, wird Microsoft Edge nicht erkennen, wenn ein Fenster von anderen Fenstern überdeckt wird.

Wenn diese Richtlinie nicht festgelegt wurde, wird die Erkennung der Fensterüberlagerung aktiviert.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: NativeWindowOcclusionEnabled
  - GP-Name: Native Window Occlusion aktivieren
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: NativeWindowOcclusionEnabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### NavigationDelayForInitialSiteListDownloadTimeout

  #### Festlegen eines Zeitlimits für die Verzögerung der Registerkartennavigation für die Enterprise Mode Site List

  
  
  #### Unterstützte Versionen:

  - Unter Windows seit 84 oder später

  #### Beschreibung

  Ermöglicht es Ihnen, einen Zeitlimit (in Sekunden) für Microsoft Edge-Registerkarten festzulegen, die auf die Navigation warten, bis der Browser die ursprüngliche Standortliste im Enterprise-Modus heruntergeladen hat.

Diese Einstellung funktioniert in Verbindung mit: [InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) auf „IEMode“ und der Richtlinie „[InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist)“, wenn die Liste mindestens einen Eintrag hat und [DelayNavigationsForInitialSiteListDownload](#delaynavigationsforinitialsitelistdownload) auf „All eligible navigations“ (1) gesetzt ist.

Die Registerkarten warten nicht länger als dieses Zeitlimit, um die Enterprise Mode Site List herunterzuladen. Wenn der Browser die Enterprise Mode Site List nach Ablauf des Zeitlimits nicht heruntergeladen hat, werden die Microsoft Edge-Registerkarten trotzdem weiter navigiert. Der Wert des Zeitlimits sollte nicht größer als 20 Sekunden und nicht weniger als 1 Sekunde sein.

Wenn Sie für das Zeitlimit in dieser Richtlinie einen höheren als den Standardwert von 2 Sekunden festlegen, wird dem Benutzer eine Informationsleiste nach 2 Sekunden angezeigt. Die Informationsleiste enthält eine Schaltfläche, mit der der Benutzer auf den Abschluss des Downloads des Enterprise Mode Site List verzichten kann.

Wenn Sie diese Richtlinie nicht konfigurieren, wird das Standardzeitlimit von 2 Sekunden verwendet. Dieser Standardwert wird künftig geändert.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Ganze Zahl

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - Eindeutiger Name des GP: NavigationDelayForInitialSiteListDownloadTimeout
  - GP-Name: Festlegen eines Zeitlimits für die Verzögerung der Registerkartennavigation für die Enterprise Mode Site List
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: NavigationDelayForInitialSiteListDownloadTimeout
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x0000000a
```

  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### NetworkPredictionOptions

  #### Aktivieren der Netzwerkvorhersage

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Aktiviert Netzwerkvorhersage und hindert Benutzer daran, diese Einstellung zu ändern.

Hiermit werden DNS-Prefetch-Vorgänge, die TCP-und SSL-Vorverbindung sowie die Vordarstellung von Webseiten gesteuert.

Wenn Sie diese Richtlinie nicht konfigurieren, ist die Netzwerkvorhersage aktiviert, aber der Benutzer kann dies ändern.

Zuordnung von Richtlinienoptionen:

* NetworkPredictionAlways (0) = Vorhersagen von Netzwerkaktionen für alle Netzwerkverbindungen

* NetworkPredictionWifiOnly (1) = Nicht unterstützt. Wenn dieser Wert verwendet wird, wird er so behandelt, als ob „Predict network actions on any network connection“ (0) eingestellt wurde.

* NetworkPredictionNever (2) = Keine Vorhersagen von Netzwerkaktionen auf irgendeiner Netzwerkverbindung

Verwenden Sie die vorstehenden Informationen, wenn Sie diese Richtlinie konfigurieren.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Ganze Zahl

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: NetworkPredictionOptions
  - GP-Name: Aktivieren der Netzwerkvorhersage
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): Administrative Templates/Microsoft Edge – Standardeinstellungen (Benutzer können diese außer Kraft setzen)/
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Wertname: NetworkPredictionOptions
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000002
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: NetworkPredictionOptions
  - Beispielwert:
``` xml
<integer>2</integer>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### NonRemovableProfileEnabled

  #### Konfigurieren, ob ein Benutzer immer ein Standardprofil hat, das automatisch mit seinem Geschäfts- oder Schulkonto angemeldet ist

  
  
  #### Unterstützte Versionen:

  - Auf Windows ab 78 oder höher

  #### Beschreibung

  Mit dieser Richtlinie wird festgelegt, ob ein Benutzer das Microsoft Edge-Profil, das automatisch mit dem Geschäfts- oder Schulkonto eines Benutzers angemeldet ist, entfernen kann.

Wenn Sie diese Richtlinie aktivieren, wird ein nicht entfernbares Profil mit dem Geschäfts- oder Schulkonto des Benutzers unter Windows erstellt. Dieses Profil lässt sich nicht abmelden oder entfernen.

Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, kann das Profil, das automatisch mit dem Geschäfts- oder Schulkonto eines Benutzers in Windows angemeldet wird, vom Benutzer abgemeldet oder entfernt werden.

Wenn Sie die Browseranmeldung konfigurieren möchten, verwenden Sie die Richtlinie [BrowserSignin](#browsersignin).

Diese Richtlinie gilt nur für Windows-Instanzen, die mit einer Microsoft Active Directory-Domäne verknüpft sind, Windows 10 Pro- oder Enterprise-Instanzen, die für die Geräteverwaltung registriert sind.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: NonRemovableProfileEnabled
  - GP-Name: Konfigurieren, ob ein Benutzer immer ein Standardprofil hat, das automatisch mit seinem Geschäfts- oder Schulkonto angemeldet ist
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: NonRemovableProfileEnabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### OverrideSecurityRestrictionsOnInsecureOrigin

  #### Steuern, wo Sicherheitseinschränkungen bei unsicheren Ursprüngen angewendet werden

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Gibt eine Liste von Ursprüngen (URLs) oder Hostname-Mustern (z. b. "*.contoso.com") an, für die Sicherheitseinschränkungen bei unsicheren Ursprüngen nicht zutreffen.

Mit dieser Richtlinie können Sie die zulässigen Ursprünge für Legacy-Anwendungen angeben, die TLS nicht bereitstellen können, oder keinen Stagingserver für interne Webentwicklungen einrichten, sodass Entwickler Features testen können, die sichere Kontexte erfordern, ohne dass TLS auf dem Stagingserver bereitgestellt werden muss. Durch diese Richtlinie wird außerdem verhindert, dass der Ursprung in der Omnibox als "nicht sicher" gekennzeichnet wird.

Das Festlegen einer Liste von URLs in dieser Richtlinie hat dieselbe Wirkung wie das Festlegen der Befehlszeilenkennzeichnung "--unsafely-treat-insecure-origin-as-secure" auf eine durch Trennzeichen getrennte Liste gleicher URLs. Wenn Sie diese Richtlinie aktivieren, wird die Befehlszeilenkennzeichnung außer Kraft gesetzt.

Weitere Informationen zu sicheren Kontexten finden Sie unter https://www.w3.org/TR/secure-contexts/.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Liste von Zeichenfolgen

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: OverrideSecurityRestrictionsOnInsecureOrigin
  - GP-Name: Steuern, wo Sicherheitseinschränkungen bei unsicheren Ursprüngen angewendet werden
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge\OverrideSecurityRestrictionsOnInsecureOrigin
  - Pfad (Empfohlen): n.a.
  - Wertname: 1, 2, 3, ...
  - Werttyp: REG_SZ-Liste

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\OverrideSecurityRestrictionsOnInsecureOrigin\1 = "http://testserver.contoso.com/"
SOFTWARE\Policies\Microsoft\Edge\OverrideSecurityRestrictionsOnInsecureOrigin\2 = "*.contoso.com"

```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: OverrideSecurityRestrictionsOnInsecureOrigin
  - Beispielwert:
``` xml
<array>
  <string>http://testserver.contoso.com/</string>
  <string>*.contoso.com</string>
</array>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### PaymentMethodQueryEnabled

  #### Websites erlauben, nach verfügbaren Zahlungsmethoden zu fragen

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 80 oder höher

  #### Beschreibung

  Hiermit können Sie festlegen, ob Websites überprüfen können, ob der Benutzer Zahlungsmethoden gespeichert hat.

Wenn Sie diese Richtlinie deaktivieren, werden Websites, welche die PaymentRequest.canMakePayment oder PaymentRequest.hasEnrolledInstrument-API verwenden, informiert, dass keine Zahlungsmethoden verfügbar sind.

Wenn Sie diese Richtlinie aktivieren oder diese Richtlinie nicht festlegen, können Websites überprüfen, ob der Benutzer Zahlungsmethoden gespeichert hat.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: PaymentMethodQueryEnabled
  - GP-Name: Websites erlauben, nach verfügbaren Zahlungsmethoden zu fragen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: PaymentMethodQueryEnabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: PaymentMethodQueryEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### PersonalizationReportingEnabled

  #### Die Personalisierung von Werbung, der Suche und von Nachrichten ermöglichen, indem der Browserverlauf an Microsoft gesendet wird

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 80 oder höher

  #### Beschreibung

  Diese Richtlinie hindert Microsoft am Sammeln des Microsoft Edge-Browserverlaufs eines Benutzers zum Personalisieren von Werbung, Suche, Nachrichten und anderen Microsoft-Diensten.

Diese Einstellung ist nur für Benutzer mit einem Microsoft-Konto verfügbar. Diese Einstellung ist für Kinder- oder Enterprise-Konten nicht verfügbar.

Wenn Sie diese Richtlinie deaktivieren, können die Benutzer die Einstellung nicht ändern oder außer Kraft setzen. Wenn diese Richtlinie aktiviert oder nicht konfiguriert ist, wird von Microsoft Edge standardmäßig die Benutzereinstellung verwendet.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: PersonalizationReportingEnabled
  - GP-Name: Die Personalisierung von Werbung, der Suche und von Nachrichten ermöglichen, indem der Browserverlauf an Microsoft gesendet wird
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: PersonalizationReportingEnabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: PersonalizationReportingEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### PinningWizardAllowed

  #### Assistent „an Taskleiste anheften“ zulassen

  
  
  #### Unterstützte Versionen:

  - Auf Windows ab 80 oder höher

  #### Beschreibung

  Microsoft Edge verwendet den Assistenten "an Taskleiste anheften", damit Benutzer vorgeschlagene Websites an die Taskleiste anheften können. Das Feature "an Taskleiste anheften" ist standardmäßig aktiviert und für den Benutzer im Menü "Einstellungen und mehr" zugänglich.

Wenn Sie diese Richtlinie aktivieren oder nicht konfigurieren, können die Benutzer im Menü Einstellungen und mehr den Assistenten zum Anheften an die Taskleiste aufrufen. Der Assistent kann auch über einen Protokollstart aufgerufen werden.

Wenn Sie diese Richtlinie deaktivieren, ist der Assistent "an Taskleiste anheften" im Menü deaktiviert und kann nicht über einen Protokollstart aufgerufen werden.

Benutzereinstellungen zum Aktivieren oder Deaktivieren des Assistenten zum Anheften an die Taskleiste stehen nicht zur Verfügung.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: PinningWizardAllowed
  - GP-Name: Assistent „an Taskleiste anheften“ zulassen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: PinningWizardAllowed
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000000
```

  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### ProactiveAuthEnabled

  #### Proaktive Authentifizierung aktivieren

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Sie können konfigurieren, ob die proaktive Authentifizierung aktiviert werden soll.

Wenn Sie diese Richtlinie aktivieren, versucht Microsoft Edge, den angemeldeten Benutzer mit Microsoft-Diensten proaktiv zu authentifizieren. In regelmäßigen Abständen überprüft Microsoft Edge mit einem Onlinedienst nach einem aktualisierten Manifest, das die Konfiguration enthält, die vorgibt, wie dies zu tun ist.

Wenn Sie diese Richtlinie deaktivieren, versucht Microsoft Edge nicht, den angemeldeten Benutzer mit Microsoft-Diensten proaktiv zu authentifizieren. Microsoft Edge sucht nicht mehr bei einem Onlinedienst nach einem aktualisierten Manifest, das die entsprechende Konfiguration enthält.

Wenn Sie diese Richtlinie nicht konfigurieren, ist die proaktive Authentifizierung aktiviert.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: ProactiveAuthEnabled
  - GP-Name: Proaktive Authentifizierung aktivieren
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: ProactiveAuthEnabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: ProactiveAuthEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### PromotionalTabsEnabled

  #### Aktivieren von Promotion-Inhalten auf der gesamten Registerkarte

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Steuern der vollflächigen Präsentation von Promotions- oder Lehrinhalten auf Registerkarten. Mit dieser Einstellung wird die Präsentation von Willkommensseiten gesteuert, die Benutzern bei der Anmeldung bei Microsoft Edge helfen, den Standardbrowser auswählen lassen oder die über Produktfunktionen informieren.

Wenn Sie diese Richtlinie aktivieren (auf „true“ festlegen) oder nicht konfigurieren, kann Microsoft Edge vollflächige Registerkarteninhalte für Benutzer anzeigen, um Produktinformationen bereitzustellen.

Wenn Sie diese Richtlinie deaktivieren (auf "false" festlegen), kann Microsoft Edge Benutzern keine vollflächigen Registerkarteninhalte anzeigen.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: PromotionalTabsEnabled
  - GP-Name: Aktivieren von Promotion-Inhalten auf der gesamten Registerkarte
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: PromotionalTabsEnabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000000
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: PromotionalTabsEnabled
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### PromptForDownloadLocation

  #### Fragen, wo heruntergeladene Dateien gespeichert werden sollen

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Legen Sie fest, ob gefragt werden soll, wo eine Datei gespeichert werden soll, bevor diese heruntergeladen wird.

Wenn Sie diese Richtlinie aktivieren, wird der Benutzer gefragt, wo jede Datei vor dem herunterladen gespeichert werden soll. Wenn Sie sie nicht konfigurieren, werden die Dateien automatisch am Standardspeicherort gespeichert, ohne dass Sie den Benutzer fragen müssen.

Wenn Sie diese Richtlinie nicht konfigurieren, können Benutzer diese Einstellung ändern.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: PromptForDownloadLocation
  - GP-Name: Fragen, wo heruntergeladene Dateien gespeichert werden sollen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: PromptForDownloadLocation
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000000
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: PromptForDownloadLocation
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### QuicAllowed

  #### QUIC-Protokoll zulassen

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Ermöglicht die Verwendung des QUIC-Protokolls in Microsoft Edge.

Wenn Sie diese Richtlinie aktivieren oder nicht konfigurieren, ist das QUIC-Protokoll zulässig.

Wenn Sie diese Richtlinie deaktivieren, wird das QUIC-Protokoll blockiert.

QUIC ist ein Tranportschicht-Netzwerkprotokoll, das die Leistung von Webanwendungen, die aktuell TCP verwenden, verbessern kann.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: QuicAllowed
  - GP-Name: QUIC-Protokoll zulassen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: QuicAllowed
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: QuicAllowed
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### RedirectSitesFromInternetExplorerPreventBHOInstall

  #### Verhindern der Installation des BHO zum Umleiten von inkompatiblen Websites von Internet Explorer zu Microsoft Edge

  
  
  #### Unterstützte Versionen:

  - Unter Windows seit 87 oder später

  #### Beschreibung

  Diese Einstellung ermöglicht Ihnen festzulegen, ob die Installation des Browser Helper Object (BHO) blockiert werden soll, mit dem inkompatible Websites von Internet Explorer nach Microsoft Edge umgeleitet werden können, wenn für Websites ein moderner Browser erforderlich ist.

Wenn Sie diese Richtlinie aktivieren, wird das BHO nicht installiert. Wenn es bereits installiert ist, wird es beim nächsten Microsoft Edge-Update deinstalliert.

Wenn diese Richtlinie nicht konfiguriert oder deaktiviert ist, wird das BHO installiert.

Das BHO ist erforderlich, damit eine Umleitung für inkompatible Websites gemacht wird, ob aber die Umleitung stattfindet oder nicht, wird auch durch [RedirectSitesFromInternetExplorerRedirectMode](#redirectsitesfrominternetexplorerredirectmode) gesteuert.

Weitere Informationen zu dieser Richtlinie finden Sie unter [https://go.microsoft.com/fwlink/?linkid=2141715](https://go.microsoft.com/fwlink/?linkid=2141715)

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - Eindeutiger GP-Name: RedirectSitesFromInternetExplorerPreventBHOInstall
  - GP-Name: Verhindern der Installation des BHO zum Umleiten von inkompatiblen Websites von Internet Explorer zu Microsoft Edge
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: RedirectSitesFromInternetExplorerPreventBHOInstall
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### RedirectSitesFromInternetExplorerRedirectMode

  #### Umleiten von inkompatiblen Websites von Internet Explorer zu MicrosoftEdge

  
  
  #### Unterstützte Versionen:

  - Unter Windows seit 87 oder später

  #### Beschreibung

  Mit dieser Einstellung können Sie angeben, ob Internet Explorer Navigationsanforderungen für Websites, die einen modernen Browser benötigen, zu Microsoft Edge umleitet.

Wenn Sie diese Richtlinie nicht konfigurieren oder auf „Websiteliste“ festlegen, leitet Internet Explorer ab M87 inkompatible Websites, die einen modernen Browser benötigen, zu Microsoft Edge um.

Wenn eine Website von Internet Explorer zu Microsoft Edge umgeleitet wird, wird die Internet Explorer-Registerkarte, auf der die Website geladen wurde, geschlossen, wenn Sie keine vorherigen Inhalte hatte. Andernfalls wird die Registerkarte zu einer Microsoft-Hilfeseite weitergeleitet, die erklärt, warum die Website an Microsoft Edge umgeleitet wurde.

Wenn Microsoft Edge zum Laden einer Website aus dem Internet Explorer gestartet wird, wird dem Benutzer eine Informationsleiste angezeigt, in der erklärt wird, dass die Website in einem modernen Browser am besten funktioniert.

Wenn Sie diese Richtlinie deaktivieren, leitet Internet Explorer keinen Datenverkehr zu Microsoft Edge um.

Weitere Informationen zu dieser Richtlinie finden Sie unter [https://go.microsoft.com/fwlink/?linkid=2141715](https://go.microsoft.com/fwlink/?linkid=2141715)

Zuordnung von Richtlinienoptionen:

* Disable (0) = Deaktivieren

* Sitelist (1) = Websites basierend auf der Liste inkompatibler Websiteliste umleiten

Verwenden Sie die vorstehenden Informationen, wenn Sie diese Richtlinie konfigurieren.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Ganze Zahl

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - Eindeutiger GP-Name: RedirectSitesFromInternetExplorerRedirectMode
  - GP-Name: Umleiten von inkompatiblen Websites aus Internet Explorer zu MicrosoftEdge
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): Administrative Templates/Microsoft Edge – Standardeinstellungen (Benutzer können diese außer Kraft setzen)/
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Wertname: RedirectSitesFromInternetExplorerRedirectMode
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### RelaunchNotification

  #### Einen Benutzer informieren, dass für ausstehende Updates ein Browser-Neustart empfohlen oder erforderlich ist

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Informiert die Benutzer, dass sie Microsoft Edge neu starten müssen, um eine ausstehende Aktualisierung anzuwenden.

Wenn Sie diese Richtlinie nicht konfigurieren, fügt Microsoft Edge ein Neustartsymbol ganz rechts in der oberen Menüleiste hinzu, um die Benutzer aufzufordern, den Browser neu zu starten, um die Aktualisierung anzuwenden.

Wenn Sie diese Richtlinie aktivieren und auf „Recommended“ setzen, werden Benutzer durch eine wiederkehrende Warnung darauf hingewiesen, dass ein Neustart empfohlen wird. Benutzer können diese Warnung schließen und den Neustart zurückstellen.

Wenn Sie die Richtlinie auf „Required“ setzen, werden Benutzer durch eine wiederkehrende Warnung darauf hingewiesen, dass der Browser automatisch neu gestartet wird, sobald eine Benachrichtigungsfrist verstrichen ist. Der Standardzeitraum beträgt sieben Tage. Sie können diesen Zeitraum mit der Richtlinie [RelaunchNotificationPeriod](#relaunchnotificationperiod) konfigurieren.

Die Sitzung des Benutzers wird beim Neustart des Browsers wiederhergestellt.

Zuordnung von Richtlinienoptionen:

* Recommended (1) = Empfohlen – Zeigt dem Benutzer durch eine wiederkehrende Warnung an, dass ein Neustart empfohlen wird

* Required (2) = Erforderlich – Zeigt dem Benutzer durch eine wiederkehrende Warnung an, dass ein Neustart erforderlich ist

Verwenden Sie die vorstehenden Informationen, wenn Sie diese Richtlinie konfigurieren.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Ganze Zahl

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: RelaunchNotification
  - GP-Name: Einen Benutzer informieren, dass für ausstehende Updates ein Browser-Neustart empfohlen oder erforderlich ist
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: RelaunchNotification
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: RelaunchNotification
  - Beispielwert:
``` xml
<integer>1</integer>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### RelaunchNotificationPeriod

  #### Festlegen des Zeitraums für Aktualisierungsbenachrichtigungen

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Hiermit können Sie den Zeitraum in Millisekunden festlegen, in dem Benutzer benachrichtigt werden, dass Microsoft Edge neu gestartet werden muss, um ein ausstehendes Update anzuwenden.

Über diesen Zeitraum wird der Benutzer wiederholt informiert, dass eine Aktualisierung erforderlich ist. In Microsoft Edge ändert sich das App-Menü, um anzuzeigen, dass ein Neustart erforderlich ist, sobald ein Drittel des Benachrichtigungszeitraums abgelaufen ist. Diese Benachrichtigung ändert die Farbe, sobald zwei Drittel des Benachrichtigungszeitraums abgelaufen sind, und erneut, wenn der vollständige Benachrichtigungszeitraum abgelaufen ist. Die zusätzlichen Benachrichtigungen, die durch die Richtlinie [RelaunchNotification](#relaunchnotification) aktiviert sind, folgen diesem Zeitplan.

Wenn diese Option nicht festgelegt ist, wird der Standardzeitraum von 604800000 Millisekunden (eine Woche) verwendet.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Ganze Zahl

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: RelaunchNotificationPeriod
  - GP-Name: Festlegen des Zeitraums für Aktualisierungsbenachrichtigungen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: RelaunchNotificationPeriod
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x240c8400
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: RelaunchNotificationPeriod
  - Beispielwert:
``` xml
<integer>604800000</integer>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### RendererCodeIntegrityEnabled

  #### Aktivieren der Codeintegrität des Renderers

  
  
  #### Unterstützte Versionen:

  - Auf Windows ab 78 oder höher

  #### Beschreibung

  Wenn diese Richtlinie aktiviert oder nicht festgelegt ist, ist die Renderer-Code-Integrität aktiviert. Diese Richtlinie sollte nur deaktiviert werden, wenn Kompatibilitätsprobleme mit Software von Drittanbietern auftreten, die innerhalb der Renderer-Prozesse von Microsoft Edge ausgeführt werden müssen.

Das Deaktivieren dieser Richtlinie wirkt sich negativ auf die Sicherheit und Stabilität von Microsoft Edge aus, da unbekannte und potenziell böswilliger Code innerhalb der Renderer-Prozesse von Microsoft Edge geladen werden kann.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: RendererCodeIntegrityEnabled
  - GP-Name: Aktivieren der Codeintegrität des Renderers
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: RendererCodeIntegrityEnabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000000
```

  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### RequireOnlineRevocationChecksForLocalAnchors

  #### Angeben, ob Online-OCSP-/-CRL-Prüfungen für lokale Vertrauensanker erforderlich sind

  
  
  #### Unterstützte Versionen:

  - Auf Windows ab 77 oder höher

  #### Beschreibung

  Legt fest, ob Online-Sperrprüfungen (OCSP/CRL-Prüfungen) erforderlich sind. Wenn Microsoft Edge keine Widerrufsstatusinformationen erhalten kann, werden diese Zertifikate als widerrufen behandelt ("hard-fail").

Wenn Sie diese Richtlinie aktivieren, führt Microsoft Edge immer eine Sperrüberprüfung für Serverzertifikate durch, die erfolgreich überprüft wurden und durch lokal installierte CA-Zertifikate signiert sind.

Wenn Sie diese Richtlinie nicht konfigurieren oder deaktivieren, verwendet Microsoft Edge die vorhandenen Einstellungen für die Online-Sperrprüfung.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: RequireOnlineRevocationChecksForLocalAnchors
  - GP-Name: Angeben, ob Online-OCSP-/-CRL-Prüfungen für lokale Vertrauensanker erforderlich sind
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: RequireOnlineRevocationChecksForLocalAnchors
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000000
```

  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### ResolveNavigationErrorsUseWebService

  #### Aktivieren der Auflösung von Navigationsfehlern mithilfe eines Webdiensts

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Ermöglichen Sie Microsoft Edge den Aufbau einer datenlosen Verbindung mit einem Webdienst, um die Netzwerkkonnektivität in Fällen wie Hotel- und Airport-WLANs zu sondieren.

Wenn Sie diese Richtlinie aktivieren, wird ein Webdienst für Netzwerkverbindungstests verwendet.

Wenn Sie diese Richtlinie deaktivieren, verwendet Microsoft Edge systemeigene APIs, um zu versuchen, Netzwerkkonnektivitäts- und Navigationsprobleme zu lösen.

**Hinweis**: außer unter Windows 8 und neueren Versionen von Windows verwendet Microsoft Edge *immer* systemeigene APIs, um Verbindungsprobleme zu lösen.

Wenn Sie diese Richtlinie nicht konfigurieren, respektiert Microsoft Edge die Benutzereinstellungen, die unter Dienste unter Edge://Settings/Privacy festgelegt sind.
Insbesondere gibt es ein Wahlfeld **Verwenden eines Webdiensts zum Beheben von Navigationsfehlern**, das der Benutzer ein- oder ausschalten kann. Wenn Sie diese Richtlinie (ResolveNavigationErrorsUseWebService) aktiviert haben, sollten Sie wissen, dass die Einstellung **Verwenden eines Webdiensts zum Beheben von Navigationsfehlern** aktiviert ist, der Benutzer die Einstellung jedoch nicht mithilfe der Umschaltfläche ändern kann. Wenn Sie diese Richtlinie deaktiviert haben, ist die Einstellung **Verwenden eines Webdiensts zum Beheben von Navigationsfehlern** deaktiviert und der Benutzer kann die Einstellung nicht mithilfe der Umschaltfläche ändern.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: ResolveNavigationErrorsUseWebService
  - GP-Name: Aktivieren der Auflösung von Navigationsfehlern mithilfe eines Webdiensts
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): Administrative Templates/Microsoft Edge – Standardeinstellungen (Benutzer können diese außer Kraft setzen)/
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Wertname: ResolveNavigationErrorsUseWebService
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: ResolveNavigationErrorsUseWebService
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### RestrictSigninToPattern

  #### Einschränken, welche Konten als primäre Microsoft Edge-Konten verwendet werden können

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Bestimmt, welche Konten als primäre Browserkonten in Microsoft Edge (das Konto, das während des Synchronisierungs-Zustimmungs-Stroms ausgewählt wurde) festgelegt werden können.

Wenn ein Benutzer versucht, ein primäres Browserkonto mit einem Benutzernamen zu konfigurieren, der diesem Muster nicht entspricht, wird dies blockiert und erhält die entsprechende Fehlermeldung. Sie können diese Richtlinie so konfigurieren, dass mehrere Konten mit einem regulären Ausdruck im Perl-Stil für das Muster übereinstimmen. Beachten Sie, dass bei Musterübereinstimmungen die Groß-/Kleinschreibung beachtet wird. Weitere Informationen über die Regeln für reguläre Ausdrücke, die verwendet werden, finden Sie unter https://go.microsoft.com/fwlink/p/?linkid=2133903.

Wenn Sie diese Richtlinie nicht konfigurieren oder sie leer lassen, können Benutzer jedes Konto als primäres Browserkonto in Microsoft Edge festlegen.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Zeichenfolge

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: RestrictSigninToPattern
  - GP-Name: Einschränken, welche Konten als primäre Microsoft Edge-Konten verwendet werden können
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: RestrictSigninToPattern
  - Werttyp: REG_SZ

  ##### Beispielwert:

```
".*@contoso.com"
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: RestrictSigninToPattern
  - Beispielwert:
``` xml
<string>.*@contoso.com</string>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### RoamingProfileLocation

  #### Festlegen des Server gespeicherten Profilverzeichnisses

  
  
  #### Unterstützte Versionen:

  - Auf Windows seit 85 oder später

  #### Beschreibung

  Konfiguriert das Verzeichnis zum Aufbewahren der Server gespeicherten Kopie der Profile.

Wenn Sie diese Richtlinie aktivieren, verwendet Microsoft Edge das bereitgestellte Verzeichnis, um eine Server gespeicherte Kopie der Profile zu sichern, sofern Sie die Richtlinie [RoamingProfileSupportEnabled](#roamingprofilesupportenabled) aktiviert haben. Wenn Sie die Richtlinie [RoamingProfileSupportEnabled](#roamingprofilesupportenabled) deaktivieren oder nicht konfigurieren, wird der in dieser Richtlinie gespeicherte Wert nicht verwendet.

Eine Liste der Variablen, die Sie verwenden können, finden Sie unter [https://go.microsoft.com/fwlink/?linkid=2095041](https://go.microsoft.com/fwlink/?linkid=2095041).

Wenn Sie diese Richtlinie nicht konfigurieren, wird der Standardpfad für den Server gespeicherten Profile verwendet.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Zeichenfolge

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - Eindeutiger Name des GP: RoamingProfileLocation
  - GP-Name: Festlegen des Server gespeicherten Profilverzeichnisses
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: RoamingProfileLocation
  - Werttyp: REG_SZ

  ##### Beispielwert:

```
"${roaming_app_data}\\edge-profile"
```

  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### RoamingProfileSupportEnabled

  #### Aktivieren der Verwendung von Roaming-Kopien für Microsoft Edge-Profildaten

  
  
  #### Unterstützte Versionen:

  - Auf Windows seit 85 oder später

  #### Beschreibung

  Aktivieren Sie diese Richtlinie, um Server gespeicherte Profile unter Windows zu verwenden. Die in Microsoft Edge-Profile (Favoriten und Einstellungen) gespeicherten Einstellungen werden auch in einer Datei gespeichert, die im Server gespeicherten Benutzerprofilordner gespeichert ist (oder der vom Administrator durch die [RoamingProfileLocation-](#roamingprofilelocation) Richtlinie angegebenen Position).

Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, werden nur die normalen lokalen Profile verwendet.

Die Richtlinie [SyncDisabled](#syncdisabled) deaktiviert die gesamte Datensynchronisierung, wobei die Richtlinie außer Kraft gesetzt wird.

Weitere Informationen zur Verwendung von Server gespeicherten Benutzerprofilen finden Sie unter https://docs.microsoft.com/windows-server/storage/folder-redirection/deploy-roaming-user-profiles.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - Eindeutiger Name des GP: RoamingProfileSupportEnabled
  - GP-Name: Aktivieren der Verwendung von Roaming-Kopien für Microsoft Edge-Profildaten
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: RoamingProfileSupportEnabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### RunAllFlashInAllowMode

  #### Erweitern der Einstellung für Adobe Flash-Inhalte auf alle Inhalte

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Wenn Sie diese Richtlinie aktivieren, werden alle in Websites, die so eingerichtet sind, dass sie Adobe Flash in den Inhaltseinstellungen zulassen – entweder vom Benutzer oder von einer Unternehmensrichtlinie – eingebetteten Adobe Flash-Inhalte ausgeführt. Dies umfasst Inhalte aus anderen Ursprüngen und/oder kleine Inhalte.

Wenn Sie steuern möchten, welche Websites Adobe Flash ausführen können, lesen Sie die Spezifikationen in den [DefaultPluginsSetting](#defaultpluginssetting), [PluginsAllowedForUrls](#pluginsallowedforurls) und [PluginsBlockedForUrls](#pluginsblockedforurls)-Richtlinien.

Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, werden Adobe Flash-Inhalte von anderen Ursprüngen (von Websites, die nicht in den drei erwähnten Richtlinien angegeben sind) oder kleine Inhalte möglicherweise blockiert.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: RunAllFlashInAllowMode
  - GP-Name: Erweitern der Einstellung für Adobe Flash-Inhalte auf alle Inhalte
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: RunAllFlashInAllowMode
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: RunAllFlashInAllowMode
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### SSLErrorOverrideAllowed

  #### Zulassen, dass Benutzer die HTTPS-Warnungsseite überschreiten können

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Microsoft Edge zeigt eine Warnseite an, wenn Benutzer Websites besuchen, die SSL-Fehler aufweisen.

Wenn Sie diese Richtlinie aktivieren oder nicht konfigurieren (Standardeinstellung), können die Benutzer diese Warnseiten durch Klicken schließen.

Wenn Sie diese Richtlinie deaktivieren, werden die Benutzer daran gehindert, jegliche Warnseiten durch Klicken zu schließen.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: SSLErrorOverrideAllowed
  - GP-Name: Zulassen, dass Benutzer die HTTPS-Warnungsseite überschreiten können
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: SSLErrorOverrideAllowed
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: SSLErrorOverrideAllowed
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### SSLVersionMin

  #### Mindestens aktivierte TLS-Version

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Sets the minimum supported version of TLS. Wenn Sie diese Richtlinie nicht konfigurieren, zeigt Microsoft Edge einen Fehler für TLS 1.0 und TLS 1.1 an, der Benutzer kann ihn jedoch umgehen.

Wenn Sie diese Richtlinie festlegen, verwendet Microsoft Edge keine SSL/TLS-Versionen, die niedriger als die angegebene Version sind. Jeder nicht erkannte Wert wird ignoriert.

Zuordnung von Richtlinienoptionen:

* TLSv1 (tls1) = TLS 1.0

* TLSv1.1 (tls1.1) = TLS 1.1

* TLSv1.2 (tls1.2) = TLS 1.2

Verwenden Sie die vorstehenden Informationen, wenn Sie diese Richtlinie konfigurieren.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Zeichenfolge

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: SSLVersionMin
  - GP-Name: Mindestens aktivierte TLS-Version
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: SSLVersionMin
  - Werttyp: REG_SZ

  ##### Beispielwert:

```
"tls1"
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: SSLVersionMin
  - Beispielwert:
``` xml
<string>tls1</string>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### SaveCookiesOnExit

  #### Speichern von Cookies, wenn Microsoft Edge geschlossen wird

  
  
  #### Unterstützte Versionen:

  - Unter Windows und macOS ab 86 oder höher

  #### Beschreibung

  Wenn diese Richtlinie aktiviert ist, werden die angegebenen Cookies beim Schließen des Browsers nicht gelöscht werden. Diese Richtlinie ist nur wirksam, wenn:
- Der Umschalter "Cookies und andere Site-Daten" unter "Einstellungen"/"Datenschutz und Dienste"/"Browserdaten beim Schließen löschen" konfiguriert wurde, oder
- Die Richtlinie [ClearBrowsingDataOnExit](#clearbrowsingdataonexit) ist aktiviert oder
- Die Richtlinie [DefaultCookiesSetting](#defaultcookiessetting) auf "Cookies für die Dauer der Sitzung beibehalten" festgelegt ist.

Sie können basierend auf URL-Mustern eine Liste von Websites definieren, deren Cookies über Sitzungen hinweg beibehalten werden.

Hinweis: Benutzer können die Cookie-Site-Liste weiterhin bearbeiten, um URLs hinzuzufügen oder zu entfernen. Sie können jedoch keine URLs entfernen, die von einem Administrator hinzugefügt wurden.

Wenn Sie diese Richtlinie aktivieren, wird die Liste der Cookies beim Schließen des Browsers nicht gelöscht.

Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, wird die persönliche Konfiguration des Benutzers verwendet.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Liste von Zeichenfolgen

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - Eindeutiger Name der GP: SaveCookiesOnExit
  - GP-Name: Speichern Sie Cookies, wenn Microsoft Edge geschlossen wird
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (obligatorisch): SOFTWARE\Policies\Microsoft\Edge\SaveCookiesOnExit
  - Pfad (Empfohlen): n.a.
  - Wertname: 1, 2, 3, ...
  - Werttyp: REG_SZ-Liste

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\SaveCookiesOnExit\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SaveCookiesOnExit\2 = "[*.]contoso.edu"

```

  #### Mac – Informationen und Einstellungen
  
  - Name des Einstellungsschlüssels: SaveCookiesOnExit
  - Beispielwert:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### SavingBrowserHistoryDisabled

  #### Speichern des Browserverlaufs deaktivieren

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Deaktiviert den Browserverlauf und hindert Benutzer daran, diese Einstellung zu ändern.

Wenn Sie diese Richtlinie aktivieren, wird der Browserverlauf nicht gespeichert. Dadurch wird auch die Synchronisierung von Registerkarten deaktiviert.

Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, wird der Browserverlauf gespeichert.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: SavingBrowserHistoryDisabled
  - Speichern des Browserverlaufs deaktivieren
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: SavingBrowserHistoryDisabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: SavingBrowserHistoryDisabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### ScreenCaptureAllowed

  #### Bildschirmaufnahme zulassen oder verweigern

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 83 oder höher

  #### Beschreibung

  Wenn Sie diese Richtlinie aktivieren oder diese Richtlinie nicht konfigurieren, kann eine Webseite Bildschirmfreigabe-APIs (z.B. getDisplayMedia() oder die API für die Desktopaufnahme-Erweiterung) für eine Bildschirmaufnahme verwenden.
Wenn Sie diese Richtlinie deaktivieren, treten beim Aufrufen von Screen-Share-APIs Fehler auf. Wenn Sie beispielsweise eine webbasierte Onlinebesprechung verwenden, funktioniert die Video- oder Bildschirmfreigabe nicht.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: ScreenCaptureAllowed
  - GP-Name: Bildschirmaufnahme zulassen oder verweigern
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: ScreenCaptureAllowed
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000000
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: ScreenCaptureAllowed
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### ScrollToTextFragmentEnabled

  #### Aktivieren des Scrollens zu Text, der in URL-Fragmenten angegeben ist

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 83 oder höher

  #### Beschreibung

  Mithilfe dieses Features können Links- und Adressleisten-URL-Navigationen auf einen bestimmten Text auf einer Webseite abzielen, der nach dem Laden der Webseite durch Scrollen erreicht wird.

Wenn Sie diese Richtlinie aktivieren oder nicht konfigurieren, wird der Webseiten-Bildlauf zu bestimmten Textfragmenten über eine URL aktiviert.

Wenn Sie diese Richtlinie deaktivieren, wird der Webseiten-Bildlauf zu bestimmten Textfragmenten über eine URL deaktiviert.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: ScrollToTextFragmentEnabled
  - GP-Name: Aktivieren des Scrollens zu Text, der in URL-Fragmenten angegeben ist
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: ScrollToTextFragmentEnabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000000
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: ScrollToTextFragmentEnabled
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### SearchSuggestEnabled

  #### Suchvorschläge zulassen

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Aktiviert Websuche-Vorschläge in der Adressleiste von Microsoft Edge und der Liste "Auto-Vorschläge" und hindert Benutzer daran, diese Richtlinie zu ändern.

Wenn Sie diese Richtlinie aktivieren, werden Vorschläge für Websuchen verwendet.

Wenn Sie diese Richtlinie deaktivieren, werden Vorschläge für die Websuche nie verwendet, doch werden die Vorschläge für den lokalen Verlauf und lokale Favoriten weiterhin angezeigt. Wenn Sie diese Richtlinie deaktivieren, werden weder die eingegebenen Zeichen noch die besuchten URLs zur Telemetrie an Microsoft hinzugefügt.

Wenn diese Richtlinie nicht festgelegt wurde, sind Suchvorschläge aktiviert, aber der Benutzer kann dies ändern.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: SearchSuggestEnabled
  - GP-Name: Suchvorschläge zulassen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): Administrative Templates/Microsoft Edge – Standardeinstellungen (Benutzer können diese außer Kraft setzen)/
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Wertname: SearchSuggestEnabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: SearchSuggestEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### SecurityKeyPermitAttestation

  #### Websites oder Domänen, für die keine Berechtigung zur Verwendung der direkten Sicherheitsschlüssel-Bestätigung erforderlich ist

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Gibt Websites und Domänen an, für die keine explizite Benutzerberechtigung erforderlich ist, wenn Nachweiszertifikate von Sicherheitsschlüsseln angefordert werden. Darüber hinaus wird ein Signal an den Sicherheitsschlüssel gesendet, das angibt, dass die individuelle Bestätigung verwendet werden kann. Ohne dies werden die Benutzer jedes Mal angefragt, wenn eine Website den Nachweis über Sicherheitsschlüssel anfordert.

Websites (wie https://contoso.com/some/path) stimmen nur als U2F appIDs überein. Domänen (z.B. contoso.com) stimmen nur als webauthn-RP-IDs überein. Wenn Sie sowohl U2F als auch webauthn-APIs für eine bestimmte Website abdecken möchten, müssen Sie sowohl die appID URL als auch die Domäne angeben.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Liste von Zeichenfolgen

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: SecurityKeyPermitAttestation
  - GP-Name: Websites oder Domänen, für die keine Berechtigung zur Verwendung der direkten Sicherheitsschlüssel-Bestätigung erforderlich ist
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge\SecurityKeyPermitAttestation
  - Pfad (Empfohlen): n.a.
  - Wertname: 1, 2, 3, ...
  - Werttyp: REG_SZ-Liste

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\SecurityKeyPermitAttestation\1 = "https://contoso.com"

```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: SecurityKeyPermitAttestation
  - Beispielwert:
``` xml
<array>
  <string>https://contoso.com</string>
</array>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### SendIntranetToInternetExplorer

  #### Senden aller Intranet-Seiten an Internet Explorer

  
  
  #### Unterstützte Versionen:

  - Auf Windows ab 77 oder höher

  #### Beschreibung

  Informationen zum Konfigurieren der optimalen Benutzeroberfläche für den Internet Explorer-Modus finden Sie unter [https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210)

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: SendIntranetToInternetExplorer
  - GP-Name: Senden aller Intranet-Seiten an Internet Explorer
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: SendIntranetToInternetExplorer
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### SendSiteInfoToImproveServices

  #### Senden von Siteinformationen, um die Microsoft-Dienste zu verbessern (veraltet).

  >VERALTET: Diese Richtlinie ist veraltet. Sie wird zurzeit unterstützt, aber in einer zukünftigen Version als veraltet behandelt.
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Diese Einstellung ist veraltet. Es wird derzeit unterstützt, wird jedoch in Microsoft Edge 89 veraltet sein. Diese Richtlinie wird durch die neue Richtlinie ersetzt: [DiagnosticData](#diagnosticdata) für Windows 7, Windows 8 und macOS. Diese Richtlinie wird durch "Telemetrie unter Win 10 zulassen" ([https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569)) ersetzt.

Diese Richtlinie ermöglicht das Senden von Informationen über die in Microsoft Edge besuchten Websites an Microsoft, um Dienste wie die Suche zu verbessern.

Aktivieren Sie diese Richtlinie, um Infos zu den Websites, die in Microsoft Edge besucht wurden, an Microsoft zu senden. Deaktivieren Sie diese Richtlinie, um keine Infos zu den Websites, die in Microsoft Edge besucht wurden, an Microsoft zu senden. In beiden Fällen können Benutzer die Einstellung weder ändern noch außer Kraft setzen.

Wenn Sie diese Richtlinie unter Windows 10 nicht konfigurieren, verwendet Microsoft Edge standardmäßig die Windows-Diagnosedateneinstellung. Wenn diese Richtlinie aktiviert ist, sendet Microsoft Edge nur Informationen zu Websites, die in Microsoft Edge besucht wurden, wenn die Windows-Diagnosedaten Einstellung auf "voll" festgelegt ist. Wenn diese Richtlinie deaktiviert ist, werden von Microsoft Edge keine Informationen zu besuchten Websites gesendet. Weitere Informationen zu den Einstellungen für Windows-Diagnosedaten finden Sie unter: [https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569)

Unter Windows 7, Windows 8 und MacOS steuert diese Richtlinie das Senden von Informationen zu besuchten Websites. Wenn Sie diese Richtlinie nicht konfigurieren, verwendet Microsoft Edge standardmäßig die Präferenz des Benutzers.

Um diese Richtlinie zu aktivieren, muss [MetricsReportingEnabled](#metricsreportingenabled) auf Aktiviert gesetzt sein. Wenn [SendSiteInfoToImproveServices](#sendsiteinfotoimproveservices) oder [MetricsReportingEnabled](#metricsreportingenabled) nicht konfiguriert oder deaktiviert ist, werden diese Daten nicht an Microsoft gesendet.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: SendSiteInfoToImproveServices
  - GP-Name: Senden von Site-Informationen, um die Microsoft-Dienste zu verbessern (veraltet).
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: SendSiteInfoToImproveServices
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000000
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: SendSiteInfoToImproveServices
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### SensorsAllowedForUrls

  #### Zugriff auf Sensoren auf bestimmten Websites zulassen

  
  
  #### Unterstützte Versionen:

  - Unter Windows und macOS ab 86 oder höher

  #### Beschreibung

  Definieren Sie eine auf URL-Mustern basierende Liste von Websites, die auf Sensoren wie Bewegungs- und Lichtsensoren zugreifen und diese verwenden dürfen.

Wenn Sie diese Richtlinie nicht konfigurieren, wird der globale Standardwert aus der [DefaultSensorsSetting](#defaultsensorssetting)-Richtlinie (sofern festgelegt) oder die persönliche Konfiguration des Benutzers für alle Websites verwendet.

Bei URL-Mustern, die dieser Richtlinie nicht entsprechen, wird die folgende Prioritätsreihenfolge verwendet: die [SensorsBlockedForUrls](#sensorsblockedforurls)-Richtlinie (wenn es eine Übereinstimmung gibt), die [DefaultSensorsSetting](#defaultsensorssetting)-Richtlinie (sofern festgelegt) oder die persönlichen Einstellungen des Benutzers.

Die in dieser Richtlinie definierten URL-Muster dürfen nicht mit jenen in der [SensorsBlockedForUrls](#sensorsblockedforurls)-Richtlinie angegebenen in Konflikt stehen. Sie können eine URL nicht sowohl zulassen als auch blockieren.

Ausführliche Informationen zu gültigen URL-Mustern finden Sie unter [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Liste von Zeichenfolgen

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - Eindeutiger GP-Name: SensorsAllowedForUrls
  - GP-Name: Zugriff auf Sensoren auf bestimmten Websites zulassen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge\SensorsAllowedForUrls
  - Pfad (Empfohlen): n.a.
  - Wertname: 1, 2, 3, ...
  - Werttyp: REG_SZ-Liste

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\SensorsAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SensorsAllowedForUrls\2 = "[*.]contoso.edu"

```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: SensorsAllowedForUrls
  - Beispielwert:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### SensorsBlockedForUrls

  #### Zugriff auf Sensoren auf bestimmten Websites blockieren

  
  
  #### Unterstützte Versionen:

  - Unter Windows und macOS ab 86 oder höher

  #### Beschreibung

  Definieren Sie eine auf URL-Mustern basierende Liste von Websites, die nicht auf Sensoren wie Bewegungs- und Lichtsensoren zugreifen dürfen.

Wenn Sie diese Richtlinie nicht konfigurieren, wird der globale Standardwert aus der [DefaultSensorsSetting](#defaultsensorssetting)-Richtlinie (sofern festgelegt) oder die persönliche Konfiguration des Benutzers für alle Websites verwendet.

Bei URL-Mustern, die dieser Richtlinie nicht entsprechen, wird die folgende Prioritätsreihenfolge verwendet: die [SensorsAllowedForUrls](#sensorsallowedforurls)-Richtlinie (wenn es eine Übereinstimmung gibt), die [DefaultSensorsSetting](#defaultsensorssetting)-Richtlinie (sofern festgelegt) oder die persönlichen Einstellungen des Benutzers.

Die in dieser Richtlinie definierten URL-Muster dürfen nicht mit jenen in der [SensorsAllowedForUrls](#sensorsallowedforurls)-Richtlinie angegebenen in Konflikt stehen. Sie können eine URL nicht sowohl zulassen als auch blockieren.

Ausführliche Informationen zu gültigen URL-Mustern finden Sie unter [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Liste von Zeichenfolgen

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - Eindeutiger GP-Name: SensorsBlockedForUrls
  - GP-Name: Zugriff auf Sensoren auf bestimmten Websites blockieren
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge\SensorsBlockedForUrls
  - Pfad (Empfohlen): n.a.
  - Wertname: 1, 2, 3, ...
  - Werttyp: REG_SZ-Liste

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\SensorsBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SensorsBlockedForUrls\2 = "[*.]contoso.edu"

```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: SensorsBlockedForUrls
  - Beispielwert:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### SerialAskForUrls

  #### Die Serial-API auf bestimmten Websites zulassen

  
  
  #### Unterstützte Versionen:

  - Unter Windows und macOS ab 86 oder höher

  #### Beschreibung

  Definieren Sie eine auf URL-Mustern basierende Liste von Websites, die vom Benutzer Zugriff auf einen seriellen Anschluss anfordern dürfen.

Falls Sie diese Richtlinie nicht konfigurieren, wird der globale Standardwert aus der [DefaultSerialGuardSetting](#defaultserialguardsetting)-Richtlinie (sofern festgelegt) oder die persönliche Konfiguration des Benutzers für alle Websites verwendet.

Bei URL-Mustern, die dieser Richtlinie nicht entsprechen, wird die folgende Prioritätsreihenfolge verwendet: die [SerialBlockedForUrls](#serialblockedforurls)-Richtlinie (wenn es eine Übereinstimmung gibt), die [DefaultSerialGuardSetting](#defaultserialguardsetting)-Richtlinie (sofern festgelegt) oder die persönlichen Einstellungen des Benutzers.

Die in dieser Richtlinie definierten URL-Muster dürfen nicht mit jenen in der [SerialBlockedForUrls](#serialblockedforurls)-Richtlinie angegebenen in Konflikt stehen. Sie können eine URL nicht sowohl zulassen als auch blockieren.

Ausführliche Informationen zu gültigen URL-Mustern finden Sie unter [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Liste von Zeichenfolgen

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - Eindeutiger GP-Name: SerialAskForUrls
  - GP-Name: Die Serial-API auf bestimmten Websites zulassen.
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfade (verpflichtend): SOFTWARE\Policies\Microsoft\Edge\SerialAskForUrls
  - Pfad (Empfohlen): n.a.
  - Wertname: 1, 2, 3, ...
  - Werttyp: REG_SZ-Liste

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\SerialAskForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SerialAskForUrls\2 = "[*.]contoso.edu"

```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: SerialAskForUrls
  - Beispielwert:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### SerialBlockedForUrls

  #### Die Serial-API auf bestimmten Websites blockieren

  
  
  #### Unterstützte Versionen:

  - Unter Windows und macOS ab 86 oder höher

  #### Beschreibung

  Definieren Sie eine auf URL-Mustern basierende Liste von Websites, die vom Benutzer keinen Zugriff auf einen seriellen Anschluss anfordern dürfen.

Falls Sie diese Richtlinie nicht konfigurieren, wird der globale Standardwert aus der [DefaultSerialGuardSetting](#defaultserialguardsetting)-Richtlinie (sofern festgelegt) oder die persönliche Konfiguration des Benutzers für alle Websites verwendet.

Bei URL-Mustern, die dieser Richtlinie nicht entsprechen, wird die folgende Prioritätsreihenfolge verwendet: die [SerialAskForUrls](#serialaskforurls)-Richtlinie (wenn es eine Übereinstimmung gibt), die [DefaultSerialGuardSetting](#defaultserialguardsetting)-Richtlinie (sofern festgelegt) oder die persönlichen Einstellungen des Benutzers.

Die URL-Muster in dieser Richtlinie dürfen nicht mit jenen in der [SerialAskForUrls](#serialaskforurls)-Richtlinie angegebenen in Konflikt stehen. Sie können eine URL nicht sowohl zulassen als auch blockieren.

Ausführliche Informationen zu gültigen URL-Mustern finden Sie unter [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Liste von Zeichenfolgen

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - Eindeutiger GP-Name: SerialBlockedForUrls
  - GP-Name: Die Serial-API auf bestimmten Websites blockieren
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge\SerialBlockedForUrls
  - Pfad (Empfohlen): n.a.
  - Wertname: 1, 2, 3, ...
  - Werttyp: REG_SZ-Liste

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\SerialBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SerialBlockedForUrls\2 = "[*.]contoso.edu"

```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: SerialBlockedForUrls
  - Beispielwert:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### ShowOfficeShortcutInFavoritesBar

  #### Microsoft Office-Verknüpfung auf der Favoritenleiste anzeigen (veraltet)

  >VERALTET: Diese Richtlinie ist veraltet. Sie wird zurzeit unterstützt, aber in einer zukünftigen Version als veraltet behandelt.
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Diese Richtlinie hat aufgrund veränderter betrieblicher Anforderungen nicht erwartungsgemäß funktioniert. Therefore it's deprecated and should not be used.

Gibt an, ob eine Verknüpfung mit Office.com in die Favoritenleiste einbezogen werden soll. For users signed into Microsoft Edge the shortcut takes users to their Microsoft Office apps and docs. If you enable or don't configure this policy, users can choose whether to see the shortcut by changing the toggle in the favorites bar context menu.
Wenn Sie diese Richtlinie deaktivieren, wird die Verknüpfung nicht angezeigt.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: ShowOfficeShortcutInFavoritesBar
  - GP-Name: Microsoft Office-Verknüpfung auf der Favoritenleiste anzeigen (veraltet)
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: ShowOfficeShortcutInFavoritesBar
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000000
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: ShowOfficeShortcutInFavoritesBar
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### SignedHTTPExchangeEnabled

  #### Unterstützung für Signed HTTP Exchange (SXG) aktivieren

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 78 oder höher

  #### Beschreibung

  Unterstützung für Signed HTTP Exchange (SXG) aktivieren.

Wenn diese Richtlinie nicht festgelegt oder aktiviert ist, akzeptiert Microsoft Edge Webinhalte, die als signierter HTTP-Austausch angeboten werden.

Wenn diese Richtlinie auf deaktiviert festgelegt ist, können signierte HTTP-Austausche nicht geladen werden.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: SignedHTTPExchangeEnabled
  - GP-Name: Unterstützung für Signed HTTP Exchange (SXG) aktivieren
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: SignedHTTPExchangeEnabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: SignedHTTPExchangeEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### SitePerProcess

  #### Aktivieren der Website-Isolation für alle Websites

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Die "SitePerProcess"-Richtlinie kann verwendet werden, um zu verhindern, dass Benutzer das Standardverhalten für das Isolieren aller Websites deaktivieren. Beachten Sie, dass Sie auch die [IsolateOrigins](#isolateorigins)-Richtlinie verwenden können, um zusätzliche, feiner definierte Ursprünge zu isolieren.

Wenn Sie diese Richtlinie aktivieren, können die Benutzer das Standardverhalten nicht deaktivieren, in dem jede Website in Ihrem eigenen Prozess ausgeführt wird.

Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, können Benutzer die Website-Isolation deaktivieren.  (z.B. mithilfe des Eintrags "Website-Isolation deaktivieren" in edge://flags.) Wenn Sie die Richtlinie deaktivieren oder die Richtlinie nicht konfigurieren, wird die Website-Isolation nicht deaktiviert.


  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: SitePerProcess
  - GP-Name: Aktivieren der Website-Isolation für alle Websites
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: SitePerProcess
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: SitePerProcess
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### SpeechRecognitionEnabled

  #### Configure Speech Recognition

  
  
  #### Unterstützte Versionen:

  - On Windows and macOS since 87 or later

  #### Beschreibung

  Set whether websites can use the W3C Web Speech API to recognize speech from the user. The Microsoft Edge implementation of the Web Speech API uses Azure Cognitive Services, so voice data will leave the machine.

If you enable or don't configure this policy, web-based applications that use the Web Speech API can use Speech Recognition.

If you disable this policy, Speech Recognition is not available through the Web Speech API.

Read more about this feature here: SpeechRecognition API: [https://go.microsoft.com/fwlink/?linkid=2143388](https://go.microsoft.com/fwlink/?linkid=2143388) Cognitive Services: [https://go.microsoft.com/fwlink/?linkid=2143680](https://go.microsoft.com/fwlink/?linkid=2143680)

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP unique name: SpeechRecognitionEnabled
  - GP name: Configure Speech Recognition
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Value Name: SpeechRecognitionEnabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Preference Key Name: SpeechRecognitionEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### SpellcheckEnabled

  #### Rechtschreibprüfung aktivieren

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Wenn Sie diese Richtlinie aktivieren oder nicht konfigurieren, kann der Benutzer die Rechtschreibprüfung verwenden.

Wenn Sie diese Richtlinie deaktivieren, kann der Benutzer keine Rechtsschreibprüfung verwenden, und die [SpellcheckLanguage](#spellchecklanguage) und [SpellcheckLanguageBlocklist](#spellchecklanguageblocklist) Richtlinien sind ebenfalls deaktiviert.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: SpellcheckEnabled
  - GP-Name: Rechtschreibprüfung aktivieren
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: SpellcheckEnabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000000
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: SpellcheckEnabled
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### SpellcheckLanguage

  #### Aktivieren spezifischer Sprachen für die Rechtschreibprüfung

  
  
  #### Unterstützte Versionen:

  - Auf Windows ab 77 oder höher

  #### Beschreibung

  Aktiviert unterschiedliche Sprachen für die Rechtschreibprüfung. Jede von Ihnen festgelegte Sprache, die nicht erkannt wird, wird ignoriert.

Wenn Sie diese Richtlinie aktivieren, ist die Rechtschreibprüfung für die angegebenen Sprachen sowie alle Sprachen, die der Benutzer aktiviert hat, aktiviert.

Wenn Sie diese Richtlinie nicht konfigurieren oder deaktivieren, gibt es keine Änderungen an den Einstellungen für die Rechtschreibprüfung des Benutzers.

Wenn die Richtlinie [SpellcheckEnabled](#spellcheckenabled) deaktiviert ist, hat diese Richtlinie keine Wirkung.

Wenn eine Sprache sowohl in der "SpellcheckLanguage" als auch in der [SpellcheckLanguageBlocklist](#spellchecklanguageblocklist) Richtlinie enthalten ist, ist die Sprache für die Rechtschreibprüfung aktiviert.

Die unterstützten Sprachen sind: af, bg, ca, cs, cy, da, de, el, en-AU, en-CA, en-GB, en-US, es, es-419, es-AR, es-ES, es-MX, es-US, et, fa, fo, fr, he, hi, hr, hu, id, it, ko, lt, lv, nb, nl, pl, pt-BR, pt-PT, ro, ru, sh, sk, sl, sq, sr, sv, ta, tg, tr, uk, vi.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Liste von Zeichenfolgen

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: SpellcheckLanguage
  - GP-Name: Aktivieren spezifischer Sprachen für die Rechtschreibprüfung
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguage
  - Pfad (Empfohlen): n.a.
  - Wertname: 1, 2, 3, ...
  - Werttyp: REG_SZ-Liste

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguage\1 = "fr"
SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguage\2 = "es"

```

  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### SpellcheckLanguageBlocklist

  #### Deaktivierung der Rechtschreibprüfungssprachen erzwingen

  
  
  #### Unterstützte Versionen:

  - Auf Windows ab 78 oder höher

  #### Beschreibung

  Deaktivierung der Rechtschreibprüfung für Sprachen erzwingen. Nicht erkannte Sprachen in dieser Liste werden ignoriert.

Wenn Sie diese Richtlinie aktivieren, wird die Rechtschreibprüfung für die angegebenen Sprachen deaktiviert. Benutzer können die Rechtschreibprüfung für Sprachen, die nicht in der Liste enthalten sind, weiterhin aktivieren oder deaktivieren.

Wenn Sie diese Richtlinie nicht festlegen oder deaktivieren, gibt es keine Änderungen an den Einstellungen für die Rechtschreibprüfung des Benutzers.

Wenn die Richtlinie [SpellcheckEnabled](#spellcheckenabled) deaktiviert ist, hat diese Richtlinie keine Wirkung.

Wenn eine Sprache sowohl in der [SpellcheckLanguage](#spellchecklanguage) als auch in der „SpellcheckLanguageBlocklist“ Richtlinie enthalten ist, ist die Sprache für die Rechtschreibprüfung aktiviert.

Die derzeit unterstützten Sprachen sind: af, bg, ca, cs, da, de, el, en-AU, en-CA, en-GB, en-US, es, es-419, es-AR, es-ES, es-MX, es-US, et, fa, fo, fr, he, hi, hr, hu, id, it, ko, lt, lv, nb, nl, pl, pt-BR, pt-PT, ro, ru, sh, sk, sl, sq, sr, sv, ta, tg, tr, uk, vi.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Liste von Zeichenfolgen

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: SpellcheckLanguageBlocklist
  - GP-Name: Deaktivierung der Rechtschreibprüfungssprachen erzwingen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguageBlocklist
  - Pfad (Empfohlen): n.a.
  - Wertname: 1, 2, 3, ...
  - Werttyp: REG_SZ-Liste

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguageBlocklist\1 = "fr"
SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguageBlocklist\2 = "es"

```

  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### StricterMixedContentTreatmentEnabled

  #### Aktivieren der strikteren Behandlung von gemischten Inhalten (veraltet)

  >VERALTET: Diese Richtlinie ist veraltet. Sie wird zurzeit unterstützt, aber in einer zukünftigen Version als veraltet behandelt.
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 81 oder höher

  #### Beschreibung

  Diese Richtlinie ist veraltet, weil sie nur als kurzfristiger Mechanismus vorgesehen ist, um Unternehmen mehr Zeit zum Aktualisieren ihrer Webinhalte zu verschaffen, falls diese mit strikterer Behandlung von Mischinhalten inkompatibel sind. Es wird in Microsoft Edge ab Version 85 nicht funktionieren.

Mit dieser Richtlinie wird die Behandlung gemischter Inhalte (HTTP-Inhalt auf HTTPS-Websites) im Browser gesteuert.

Wenn Sie diese Richtlinie auf "wahr" eingestellt oder nicht festgelegt wird, werden gemischte Audio- und Videoinhalte automatisch auf HTTPS aktualisiert (d.h. die URL wird als HTTPS neu geschrieben, ohne dass eine Ausweichaktion ausgeführt wird, wenn die Ressource nicht über HTTPS verfügbar ist), und die Warnung "nicht sicher" wird in der URL-Leiste für gemischten Bildinhalt angezeigt.

Wenn Sie die Richtlinie auf "false" festlegen, werden die automatischen Upgrades für Audio und Video deaktiviert, und es werden keine Warnungen für Bilder angezeigt.

Diese Richtlinie wirkt sich nicht auf andere Typen von gemischten Inhalten außer Audio, Video und Bildern aus.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: StricterMixedContentTreatmentEnabled
  - GP-Name: Aktivieren der strikteren Behandlung von gemischten Inhalten (veraltet)
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: StricterMixedContentTreatmentEnabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: StricterMixedContentTreatmentEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### SuppressUnsupportedOSWarning

  #### Unterdrücken der Warnung in Bezug auf nicht unterstützte Betriebssysteme

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Unterdrückt die Warnung, die angezeigt wird, wenn Microsoft Edge auf einem Computer oder Betriebssystem ausgeführt wird, das nicht mehr unterstützt wird.

Wenn diese Richtlinie falsch oder nicht festgelegt ist, werden die Warnungen auf solchen nicht unterstützten Computern oder Betriebssystemen angezeigt.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: SuppressUnsupportedOSWarning
  - GP-Name: Unterdrücken der Warnung in Bezug auf nicht unterstützte Betriebssysteme
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: SuppressUnsupportedOSWarning
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: SuppressUnsupportedOSWarning
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### SyncDisabled

  #### Deaktivieren der Synchronisierung von Daten mit Microsoft Sync Services

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Deaktiviert die Datensynchronisierung in Microsoft Edge. Durch diese Richtlinie wird außerdem verhindert, dass die Synchronisierungs Bestätigungsaufforderung angezeigt wird.

Wenn Sie diese Richtlinie nicht festlegen oder sie nicht wie empfohlen anwenden, können die Benutzer die Synchronisierung aktivieren oder deaktivieren. Wenn Sie diese Richtlinie als zwingend erforderlich anwenden, können die Benutzer die Synchronisierung nicht aktivieren.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: SyncDisabled
  - GP-Name: Deaktivieren der Synchronisierung von Daten mit Microsoft Sync Services
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): Administrative Templates/Microsoft Edge – Standardeinstellungen (Benutzer können diese außer Kraft setzen)/
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Wertname: SyncDisabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: SyncDisabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### SyncTypesListDisabled

  #### Konfigurieren Sie die Liste der Typen, die von der Synchronisierung ausgeschlossen werden

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 83 oder höher

  #### Beschreibung

  Wenn Sie diese Richtlinie aktivieren, werden alle angegebenen Datentypen aus der Synchronisierung ausgeschlossen. Diese Richtlinie kann verwendet werden, um die Datenypen einzuschränken, die in den Microsoft Edge-Synchronisierungsdienst hochgeladen werden.

Sie können einen der folgenden Datentypen für diese Richtlinie angeben: "Favoriten", "Einstellungen", "Kennwörter", "Adressen und mehr", "Erweiterungen", "Verlauf", "openTabs" und "Sammlungen". Beachten Sie, dass bei diesen Datentypnamen die Groß-/Kleinschreibung beachtet wird.

Benutzer sind nicht dazu in der Lage, die Deaktivierung von Datentypen außer Kraft zu setzen.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Liste von Zeichenfolgen

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: SyncTypesListDisabled
  - GP-Name: Konfigurieren Sie die Liste der Typen, die von der Synchronisierung ausgeschlossen werden
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge\SyncTypesListDisabled
  - Pfad (Empfohlen): n.a.
  - Wertname: 1, 2, 3, ...
  - Werttyp: REG_SZ-Liste

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\SyncTypesListDisabled\1 = "favorites"

```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: SyncTypesListDisabled
  - Beispielwert:
``` xml
<array>
  <string>favorites</string>
</array>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### TLS13HardeningForLocalAnchorsEnabled

  #### Aktivieren eines TLS 1.3-Sicherheitsfeatures für lokale Vertrauensanker (veraltet)

  
  >VERALTET: Diese Richtlinie ist veraltet und funktioniert nach Microsoft Edge 85 nicht mehr.
  #### Unterstützte Versionen:

  - Unter Windows und MacOS ab 81 bis 85

  #### Beschreibung

  Diese Richtlinie funktioniert nicht, da sie nur als kurzfristiger Mechanismus gedacht war, um Unternehmen mehr Zeit für das Upgrade betroffener Proxys zu geben.

Diese Richtlinie steuert ein Sicherheitsfeature in TLS 1.3, das Verbindungen vor Downgrade-Attacken schützt. Es ist abwärtskompatibel und wirkt sich nicht auf Verbindungen mit konformen TLS 1.2-Servern oder -Proxies aus. Ältere Versionen einiger TLS-abfangender Proxies weisen allerdings einen Implementierungsfehler auf, der dazu führt, dass diese inkompatibel sind.

Wenn Sie diese Richtlinie aktivieren oder nicht festlegen, aktiviert Microsoft Edge diese Sicherheitsfunktionen für alle Verbindungen.

Wenn Sie diese Richtlinie deaktivieren, deaktiviert Microsoft Edge diese Sicherheitsmaßnahmen für Verbindungen, die mit lokal installierten CA-Zertifikaten authentifiziert sind. Diese Schutzfunktionen sind für Verbindungen, die mit öffentlich vertrauenswürdigen CA-Zertifikaten authentifiziert sind, immer aktiviert.

Diese Richtlinie kann verwendet werden, um auf betroffene Proxys zu testen und diese zu aktualisieren. Bei betroffenen Proxies wird erwartet, dass Verbindungen mit dem Fehlercode ERR_TLS13_DOWNGRADE_DETECTED fehlschlagen.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: TLS13HardeningForLocalAnchorsEnabled
  - GP-Name: Aktivieren der TLS 1.3-Sicherheitsfunktion für lokale Vertrauensanker (veraltet).
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: TLS13HardeningForLocalAnchorsEnabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: TLS13HardeningForLocalAnchorsEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### TLSCipherSuiteDenyList

  #### Angeben der zu deaktivierenden TLS-Verschlüsselungssammlungen

  
  
  #### Unterstützte Versionen:

  - Auf Windows und MacOS ab 85 oder später

  #### Beschreibung

  Konfigurieren Sie die Liste der Verschlüsselungssammlungen, die für TLS-Verbindungen deaktiviert sind.

Wenn Sie diese Richtlinie konfigurieren, wird die Liste der konfigurierten Verschlüsselungssammlungen beim Einrichten von TLS-Verbindungen nicht verwendet.

Wenn Sie diese Richtlinie nicht konfigurieren, wählt der Browser aus, welche TLS-Verschlüsselungssammlungen verwendet werden sollen.

Verschlüsselungssammlungen-Werte, die deaktiviert werden sollen, werden als 16-Bit-Hexadezimalwerte angegeben. Die Werte werden von der IANA-Registrierung (Internet Assigned Numbers Authority) zugewiesen.

Die TLS 1,3 Cipher Suite TLS_AES_128_GCM_SHA256 (0x1301) ist für TLS 1,3 erforderlich und kann nicht durch diese Richtlinie deaktiviert werden.

Diese Richtlinie hat keine Auswirkungen auf QUIC-basierte Verbindungen. QUIC kann über die [QuicAllowed](#quicallowed)-Richtlinie deaktiviert werden.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Liste von Zeichenfolgen

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - Eindeutiger Name des GP: TLSCipherSuiteDenyList
  - GP-Name: Angeben der zu deaktivierenden TLS-Verschlüsselungssammlungen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Path (Mandatory): SOFTWARE\Policies\Microsoft\Edge\TLSCipherSuiteDenyList
  - Pfad (Empfohlen): n.a.
  - Wertname: 1, 2, 3, ...
  - Werttyp: REG_SZ-Liste

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\TLSCipherSuiteDenyList\1 = "0x1303"
SOFTWARE\Policies\Microsoft\Edge\TLSCipherSuiteDenyList\2 = "0xcca8"
SOFTWARE\Policies\Microsoft\Edge\TLSCipherSuiteDenyList\3 = "0xcca9"

```

  #### Mac – Informationen und Einstellungen
  
  - Name des Einstellungsschlüssels: TLSCipherSuiteDenyList
  - Beispielwert:
``` xml
<array>
  <string>0x1303</string>
  <string>0xcca8</string>
  <string>0xcca9</string>
</array>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### TabFreezingEnabled

  #### Einfrieren von Hintergrundregisterkarten zulassen

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 79 oder höher

  #### Beschreibung

  Steuert, ob Microsoft Edge Registerkarten einfrieren kann, die sich für mindestens 5 Minuten im Hintergrund befinden.

Das Einfrieren von Registerkarten reduziert die CPU-, Akku- und Speichernutzung. Microsoft Edge verwendet Heuristiken, um zu verhindern, dass Registerkarten mit nützlichen Arbeiten im Hintergrund fixiert werden, z.B. solche, die Benachrichtigungen anzeigen, Sound abspielen und Video streamen.

Wenn Sie diese Richtlinie aktivieren oder nicht konfigurieren, werden Registerkarten, die für mindestens 5 Minuten im Hintergrund waren, möglicherweise eingefroren.

Wenn Sie diese Richtlinie deaktivieren, werden keine Registerkarten eingefroren.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: TabFreezingEnabled
  - GP-Name: Einfrieren von Hintergrundregisterkarten zulassen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: TabFreezingEnabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000000
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: TabFreezingEnabled
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### TaskManagerEndProcessEnabled

  #### Beenden von Prozessen im Task-Manager des Browsers zulassen

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Wenn Sie diese Richtlinie aktivieren oder nicht konfigurieren, können Benutzer Prozesse im Browser-Task-Manager beenden. Wenn Sie sie deaktivieren, können Benutzer keine Prozesse beenden, und die Schaltfläche "Prozess beenden" ist im Task-Manager des Browsers deaktiviert.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: TaskManagerEndProcessEnabled
  - GP-Name: Beenden von Prozessen im Task-Manager des Browsers zulassen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: TaskManagerEndProcessEnabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: TaskManagerEndProcessEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### TotalMemoryLimitMb

  #### Festlegen der Speicherbegrenzung in Megabyte, die eine einzelne Microsoft Edge-Instanz verwenden kann

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 80 oder höher

  #### Beschreibung

  Konfiguriert die Größe des Arbeitsspeichers, den eine einzelne Microsoft-Edge-Instanz verwenden kann, bevor Registerkarten verworfen werden, um Speicherplatz zu sparen. Der von der Registerkarte verwendete Speicherplatz wird freigegeben, und die Registerkarte muss bei Aufruf neu geladen werden.

Wenn Sie diese Richtlinie aktivieren, beginnt der Browser mit dem Verwerfen von Registerkarten, um Speicherplatz zu sparen, sobald die Beschränkung überschritten wurde. Es gibt jedoch keine Garantie dafür, dass der Browser immer unter dem Limit ausgeführt wird. Jeder Wert unter 1024 wird auf 1024 aufgerundet.

Wenn Sie diese Richtlinie nicht festlegen, versucht der Browser nur dann, Speicher zu sparen, wenn er erkannt hat, dass die Größe des physikalischen Speichers auf dem Computer niedrig ist.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Ganze Zahl

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: TotalMemoryLimitMb
  - GP-Name: Festlegen der Speicherbegrenzung in Megabyte, die eine einzelne Microsoft Edge-Instanz verwenden kann.
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: TotalMemoryLimitMb
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000800
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: TotalMemoryLimitMb
  - Beispielwert:
``` xml
<integer>2048</integer>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### TrackingPrevention

  #### Blockieren der Nachverfolgung der Browsing-Aktivitäten des Benutzers

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 78 oder höher

  #### Beschreibung

  Legt fest, ob blockiert werden soll, dass Websites die Browsing-Aktivitäten der Benutzer nachverfolgen.

Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, können die Benutzer selbst den Umfang der Nachverfolgungsverhinderung festlegen.

Zuordnung von Richtlinienoptionen:

* TrackingPreventionOff (0) = Aus (keine Nachverfolgungsverhinderung )

* TrackingPreventionBasic (1) = Basis (Blockierung schädlicher Tracker, Inhalte und Anzeigen werden personalisiert)

* TrackingPreventionBalanced (2) = Ausgeglichen (blockiert schädliche Tracker und Tracker von Websites, die der Benutzer nicht besucht hat; Inhalt und Anzeigen werden weniger personalisiert)

* TrackingPreventionStrict (3) = Strikt (blockiert schädliche Tracker und die Mehrzahl der Tracker aller Websites. Inhalte und Anzeigen werden nur minimal personalisiert. Möglicherweise funktionieren einige Teile von Websites nicht)

Verwenden Sie die vorstehenden Informationen, wenn Sie diese Richtlinie konfigurieren.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Ganze Zahl

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: TrackingPrevention
  - GP-Name: Blockieren der Nachverfolgung der Browsing-Aktivitäten des Benutzers
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: TrackingPrevention
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000002
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: TrackingPrevention
  - Beispielwert:
``` xml
<integer>2</integer>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### TranslateEnabled

  #### Übersetzungen aktivieren

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Aktiviert den integrierten Microsoft-Übersetzungsdienst in Microsoft Edge.

Wenn Sie diese Richtlinie aktivieren, bietet Microsoft Edge Übersetzungsfunktionen für den Benutzer, indem ggf. ein integriertes Flyout „Übersetzen“ angezeigt wird, und im Kontextmenü die Option „Übersetzen“ auftaucht.

Deaktivieren Sie diese Richtlinie, um alle integrierten Übersetzungsfunktionen zu deaktivieren.

Wenn Sie die Richtlinie nicht konfigurieren, können die Benutzer auswählen, ob die Übersetzungsfunktionen verwendet werden sollen.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: TranslateEnabled
  - GP-Name: Übersetzungen aktivieren
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): Administrative Templates/Microsoft Edge – Standardeinstellungen (Benutzer können diese außer Kraft setzen)/
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Wertname: TranslateEnabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: TranslateEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### URLAllowlist

  #### Definieren einer Liste zulässiger URLs

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Das Aktivieren der Richtlinie ermöglicht den Zugriff auf die aufgelisteten URLs, als Ausnahmen zur [URLBlocklist](#urlblocklist).

Formatieren Sie das URL-Muster gemäß [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

Mithilfe dieser Richtlinie können Sie Ausnahmen für restriktive Sperrlisten formulieren. Sie können z.B. "*" in die Sperrliste einschließen, um alle Anforderungen zu blockieren, und dann diese Richtlinie verwenden, um den Zugriff auf eine beschränkte Liste von URLs zuzulassen. Mithilfe dieser Richtlinie können Sie Ausnahmen für bestimmte Schemas, Unterdomänen anderer Domänen, Ports oder bestimmte Pfade einrichten.

Der spezifischste Filter bestimmt, ob eine URL blockiert oder zulässig ist. Die Zulassungsliste hat Vorrang vor der Sperrliste.

Diese Richtlinie ist auf 1.000 Einträge beschränkt, weitere Einträge werden ignoriert.

Diese Richtlinie ermöglicht es dem Browser auch, automatisch externe Anwendungen aufzurufen, die als Protokollhandler für Protokolle wie "tel:" oder "ssh:" registriert sind.

Wenn Sie diese Richtlinie nicht konfigurieren, gibt es keine Ausnahmen zur Sperrliste in der Richtlinie [URLBlocklist](#urlblocklist).

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Liste von Zeichenfolgen

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: URLAllowlist
  - GP-Name: Definieren einer Liste zulässiger URLs
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge\URLAllowlist
  - Pfad (Empfohlen): n.a.
  - Wertname: 1, 2, 3, ...
  - Werttyp: REG_SZ-Liste

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\1 = "contoso.com"
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\2 = "https://ssl.server.com"
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\3 = "hosting.com/good_path"
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\4 = "https://server:8080/path"
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\5 = ".exact.hostname.com"

```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: URLAllowlist
  - Beispielwert:
``` xml
<array>
  <string>contoso.com</string>
  <string>https://ssl.server.com</string>
  <string>hosting.com/good_path</string>
  <string>https://server:8080/path</string>
  <string>.exact.hostname.com</string>
</array>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### URLBlocklist

  #### Blockieren des Zugriffs auf eine Liste von URLs

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Sie können eine Liste an Websites, basierend auf URL-Mustern, definieren, die blockiert werden (Ihre Benutzer können sie nicht aufrufen).

Formatieren Sie das URL-Muster gemäß [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

Sie können in der Richtlinie [URLAllowlist](#urlallowlist) Ausnahmen festlegen. Diese Richtlinien sind auf 1.000-Einträge beschränkt, weitere Einträge werden ignoriert.

Beachten Sie, dass das Blockieren interner "edge://*"-URLs nicht empfohlen wird. Dies kann zu unerwarteten Fehlern führen.

Durch diese Richtlinie wird nicht verhindert, dass die Seite über JavaScript dynamisch aktualisiert wird. Wenn Sie beispielsweise "contoso.com/abc" blockieren, können Benutzer möglicherweise weiterhin "contoso.com" besuchen und auf einen Link klicken, um "contoso.com/ABC" zu besuchen, solange die Seite nicht aktualisiert wird.

Wenn Sie diese Richtlinie nicht konfigurieren, sind keine URLs blockiert.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Liste von Zeichenfolgen

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: URLBlocklist
  - GP-Name: Blockieren des Zugriffs auf eine Liste von URLs
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge\URLBlocklist
  - Pfad (Empfohlen): n.a.
  - Wertname: 1, 2, 3, ...
  - Werttyp: REG_SZ-Liste

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\URLBlocklist\1 = "contoso.com"
SOFTWARE\Policies\Microsoft\Edge\URLBlocklist\2 = "https://ssl.server.com"
SOFTWARE\Policies\Microsoft\Edge\URLBlocklist\3 = "hosting.com/bad_path"
SOFTWARE\Policies\Microsoft\Edge\URLBlocklist\4 = "https://server:8080/path"
SOFTWARE\Policies\Microsoft\Edge\URLBlocklist\5 = ".exact.hostname.com"
SOFTWARE\Policies\Microsoft\Edge\URLBlocklist\6 = "file://*"
SOFTWARE\Policies\Microsoft\Edge\URLBlocklist\7 = "custom_scheme:*"
SOFTWARE\Policies\Microsoft\Edge\URLBlocklist\8 = "*"

```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: URLBlocklist
  - Beispielwert:
``` xml
<array>
  <string>contoso.com</string>
  <string>https://ssl.server.com</string>
  <string>hosting.com/bad_path</string>
  <string>https://server:8080/path</string>
  <string>.exact.hostname.com</string>
  <string>file://*</string>
  <string>custom_scheme:*</string>
  <string>*</string>
</array>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### UserAgentClientHintsEnabled

  #### Aktivieren des Features User-Agent Client Hints (veraltet)

  >VERALTET: Diese Richtlinie ist veraltet. Sie wird zurzeit unterstützt, aber in einer zukünftigen Version als veraltet behandelt.
  
  #### Unterstützte Versionen:

  - Unter Windows und macOS ab 86 oder höher

  #### Beschreibung

  Diese Richtlinie ist veraltet, da sie nur als kurzfristiger Mechanismus gedacht ist, um Unternehmen mehr Zeit für die Aktualisierung ihrer Webinhalte zu geben, wenn sich herausstellt, dass sie nicht mit der User-Agent Client Hint-Funktion kompatibel sind. Es wird in Microsoft Edge ab Version 89 nicht funktionieren.

Wenn diese Funktion aktiviert ist, sendet die Funktion User-Agent Client Hints granulare Anforderungsheader, die Informationen über den Browser des Benutzers (z.B. die Browserversion) und die Umgebung (z.B, die Systemarchitektur) bereitstellen.

Die ist eine zusätzliche Funktion. Die neuen Header können einige Websites unterbrechen, die die Zeichen einschränken, die Anfragen enthalten können.

Wenn Sie diese Richtlinie aktivieren oder nicht konfigurieren, ist die Funktion User-Agent Client Hints aktiviert. Wenn Sie diese Richtlinie deaktivieren, ist diese Funktion nicht verfügbar.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - Eindeutiger GP-Name: UserAgentClientHintsEnabled
  - GP-Name: Aktivieren der Funktion User-Agent Client Hints (veraltet).
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: UserAgentClientHintsEnabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Name des Einstellungsschlüssels: UserAgentClientHintsEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### UserDataDir

  #### Festlegen des Benutzerdatenverzeichnisses

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Legen Sie fest, welches Verzeichnis zum Speichern von Benutzerdaten verwendet werden soll.

Wenn Sie diese Richtlinie aktivieren, verwendet Microsoft Edge unabhängig davon, ob der Benutzer das Befehlszeilenkennzeichen "--user-data-dir" festgelegt hat, das angegebene Verzeichnis.

Wenn Sie diese Richtlinie nicht aktivieren, wird der Standardprofilpfad verwendet, aber der Benutzer kann ihn mithilfe des Kennzeichens "--user-data-dir" außer Kraft setzen. Benutzer finden das Verzeichnis für das Profil unter edge://version/ unter Profilpfad.

Zum Vermeiden von Datenverlust oder anderen Fehlern konfigurieren Sie diese Richtlinie nicht auf das Stammverzeichnis eines Volumes oder auf ein Verzeichnis, das für andere Zwecke verwendet wird, da Microsoft Edge dessen Inhalte verwaltet.

Eine Liste der Variablen, die verwendet werden können, finden Sie unter [https://go.microsoft.com/fwlink/?linkid=2095041](https://go.microsoft.com/fwlink/?linkid=2095041).

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Zeichenfolge

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: UserDataDir
  - GP-Name: Festlegen des Benutzerdatenverzeichnisses
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: UserDataDir
  - Werttyp: REG_SZ

  ##### Beispielwert:

```
"${users}/${user_name}/Edge"
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: UserDataDir
  - Beispielwert:
``` xml
<string>${users}/${user_name}/Edge</string>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### UserDataSnapshotRetentionLimit

  #### Schränkt die Anzahl der Benutzerdaten-Momentaufnahmen ein, die zur Verwendung für Notfall-Rollbacks aufbewahrt werden.

  
  
  #### Unterstützte Versionen:

  - Unter Windows 86 oder später

  #### Beschreibung

  Nach jedem größeren Versionsupdate erstellt Microsoft Edge eine Momentaufnahme von Teilen der Browserdaten des Benutzers, die für einen etwaigen späteren Notfall verwendet werden können, der ein vorübergehendes Versions-Rollback erfordert. Wenn ein vorübergehendes Rollback zu einer Version durchgeführt wird, für die ein Benutzer über eine entsprechende Momentaufnahme verfügt, werden die Daten in der Momentaufnahme wiederhergestellt. Auf diese Weise werden Benutzereinstellungen wie Textmarken und Daten für das automatische Ausfüllen beibehalten.

Wenn Sie diese Richtlinie nicht festlegen, wird der Standardwert von 3 Momentaufnahmen verwendet.

Wenn Sie diese Richtlinie festlegen, werden alte Momentaufnahmen nach Bedarf gelöscht, um dem von Ihnen festgelegten Wert zu entsprechen. Wenn Sie diese Richtlinie auf "0" festlegen, werden keine Momentaufnahmen erstellt.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Ganze Zahl

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - Eindeutiger GP-Name: UserDataSnapshotRetentionLimit
  - GP-Name: Schränkt die Anzahl der Benutzerdaten-Momentaufnahmen ein, die zur Verwendung für Notfall-Rollbacks aufbewahrt werden.
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: UserDataSnapshotRetentionLimit
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000003
```

  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### UserFeedbackAllowed

  #### Benutzerfeedback zulassen

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Microsoft Edge verwendet das Edge-Feedback-Feature (standardmäßig aktiviert), um Benutzern das Senden von Feedback, Vorschlägen oder Kundenumfragen und das Melden von Problemen mit dem Browser zu ermöglichen. Außerdem können Benutzer das Microsoft Edge Feedback-Feature standardmäßig nicht deaktivieren (abschalten).

Wenn Sie diese Richtlinie aktivieren oder nicht konfigurieren, können Benutzer Microsoft Edge Feedback aufrufen.

Wenn Sie diese Richtlinie deaktivieren, können die Benutzer Microsoft Edge Feedback nicht aufrufen.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: UserFeedbackAllowed
  - GP-Name: Benutzerfeedback zulassen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: UserFeedbackAllowed
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: UserFeedbackAllowed
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### VideoCaptureAllowed

  #### Video-Aufnahme zulassen oder blockieren

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Steuert, ob Websites Video aufzeichnen können.

Falls diese Richtlinie aktiviert oder nicht konfiguriert (Standardeinstellung) ist, wird der Benutzer von allen Websites um Erlaubnis zum Zugriff auf die Videoaufzeichnung gebeten, mit Ausnahme derjenigen, die in der Richtlinienliste [VideoCaptureAllowedUrls](#videocaptureallowedurls) konfiguriert sind und denen der Zugriff gewährt wird, ohne dass der Benutzer gefragt wird.

Wenn Sie diese Richtlinie deaktivieren, wird der Benutzer nicht gefragt, und die Videoaufzeichnung ist nur für URLs verfügbar, die in der Richtlinie [VideoCaptureAllowedUrls](#videocaptureallowedurls) konfiguriert sind.

Diese Richtlinie wirkt sich auf alle Arten von Video-Eingaben aus, nicht nur auf die integrierte Kamera.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: VideoCaptureAllowed
  - GP-Name: Video-Aufnahme zulassen oder blockieren
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: VideoCaptureAllowed
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000000
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: VideoCaptureAllowed
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### VideoCaptureAllowedUrls

  #### Websites, die auf Video-Aufnahmegeräte zugreifen können, ohne eine Berechtigung anfordern zu müssen

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Sie können auf der Grundlage von URL-Mustern Websites angeben, die Videoaufnahmegeräte verwenden können, ohne den Benutzer um Erlaubnis zu bitten. Muster in dieser Liste werden mit dem Sicherheitsursprung der anfordernden URL abgeglichen. Wenn eine Übereinstimmung vorliegt, wird automatisch der Zugriff auf die Videoaufnahmegeräte gewährt.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Liste von Zeichenfolgen

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: VideoCaptureAllowedUrls
  - GP-Name: Websites, die auf Video-Aufnahmegeräte zugreifen können, ohne eine Berechtigung anfordern zu müssen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge\VideoCaptureAllowedUrls
  - Pfad (Empfohlen): n.a.
  - Wertname: 1, 2, 3, ...
  - Werttyp: REG_SZ-Liste

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\VideoCaptureAllowedUrls\1 = "https://www.contoso.com/"
SOFTWARE\Policies\Microsoft\Edge\VideoCaptureAllowedUrls\2 = "https://[*.]contoso.edu/"

```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: VideoCaptureAllowedUrls
  - Beispielwert:
``` xml
<array>
  <string>https://www.contoso.com/</string>
  <string>https://[*.]contoso.edu/</string>
</array>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### WPADQuickCheckEnabled

  #### WPAD-Optimierung einrichten

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Ermöglicht es Ihnen, die WPAD-Optimierung (Web Proxy Auto-Discovery) in Microsoft Edge zu deaktivieren.

Wenn Sie diese Richtlinie deaktivieren, wird die WPAD-Optimierung deaktiviert, wodurch der Browser bei DNS-basierten WPAD-Servern länger wartet.

Wenn Sie die Richtlinie aktivieren oder nicht konfigurieren, ist die WPAD-Optimierung aktiviert.

Unabhängig davon, ob und wie diese Richtlinie aktiviert ist, kann die WPAD-Optimierungseinstellung nicht von Benutzern geändert werden.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: WPADQuickCheckEnabled
  - GP-Name: WPAD-Optimierung einrichten
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: WPADQuickCheckEnabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: WPADQuickCheckEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### WebAppInstallForceList

  #### Konfigurieren der Liste der erzwungen installierten Web-Apps

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 80 oder höher

  #### Beschreibung

  Konfigurieren Sie diese Richtlinie, um eine Liste von Webanwendungen anzugeben, die im Hintergrund installieren, ohne dass Benutzerinteraktionen vorgenommen werden, und die Benutzer nicht deinstallieren oder deaktivieren können.

Bei jedem Listenelement der Richtlinie handelt es sich um ein Objekt mit einem verpflichtenden Element: "url" (die URL der zu installierenden Web-App), und zwei optionalen Mitgliedern: "default_launch_container" (gibt den Fenstermodus an, in dem die Web App geöffnet wird – ein neuer Tab ist die Standardeinstellung) und "create_desktop_shortcut" ("true", wenn Desktopverknüpfungen für Linux und Windows erstellt werden sollen).

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Dictionary

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: WebAppInstallForceList
  - GP-Name: Konfigurieren der Liste der erzwungen installierten Web-Apps
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: WebAppInstallForceList
  - Werttyp: REG_SZ

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\WebAppInstallForceList = [
  {
    "create_desktop_shortcut": true, 
    "default_launch_container": "window", 
    "url": "https://www.contoso.com/maps"
  }, 
  {
    "default_launch_container": "tab", 
    "url": "https://app.contoso.edu"
  }
]
```

  ##### Kompakter Beispielwert:

  ```
  SOFTWARE\Policies\Microsoft\Edge\WebAppInstallForceList = [{"create_desktop_shortcut": true, "default_launch_container": "window", "url": "https://www.contoso.com/maps"}, {"default_launch_container": "tab", "url": "https://app.contoso.edu"}]
  ```
  

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: WebAppInstallForceList
  - Beispielwert:
``` xml
<key>WebAppInstallForceList</key>
<array>
  <dict>
    <key>create_desktop_shortcut</key>
    <true/>
    <key>default_launch_container</key>
    <string>window</string>
    <key>url</key>
    <string>https://www.contoso.com/maps</string>
  </dict>
  <dict>
    <key>default_launch_container</key>
    <string>tab</string>
    <key>url</key>
    <string>https://app.contoso.edu</string>
  </dict>
</array>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### WebCaptureEnabled

  #### Aktivieren des Features „Websammlung“ in MicrosoftEdge.

  
  
  #### Unterstützte Versionen:

  - On Windows and macOS since 87 or later

  #### Beschreibung

  Aktiviert das Feature „Websammlung“ in Microsoft Edge, das Benutzern das Erfassen von Webinhalten und das Kommentieren der Sammlung mithilfe von Freihandtools ermöglicht.
Wenn Sie diese Richtlinie aktivieren oder nicht konfigurieren, wird die Option „Websammlung“ im Kontextmenü, im Menü „Einstellungen“ und in weiteren Menüs angezeigt, oder mithilfe der Tastenkombination STRG+UMSCHALT+S.
Wenn Sie diese Richtlinie deaktivieren, können Benutzer nicht auf das Feature „Websammlungen“ in Microsoft Edge zugreifen.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - Eindeutiger GP-Name: WebCaptureEnabled
  - GP-Name: Aktivieren des Features „Websammlung“ in MicrosoftEdge
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: WebCaptureEnabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: WebCaptureEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### WebComponentsV0Enabled

  #### Erneut aktivieren der Web Components v0 API bis M84 (veraltet)

  
  >VERALTET: Diese Richtlinie ist veraltet und funktioniert nach der Microsoft Edge-Version 84 nicht mehr.
  #### Unterstützte Versionen:

  - Auf Windows und MacOS ab 80, bis 84

  #### Beschreibung

  Diese Richtlinie funktioniert nicht, da diese Richtlinie erlaubte, die Features wahlweise erneut zu aktivieren bis Microsoft Edge-Version 85. Die Webkomponenten v0 APIs (Shadow DOM v0, Custom Elements v0 und HTML Imports) wurden in 2018 verworfen und sind standardmäßig ab M80 deaktiviert.

Wenn Sie diese Richtlinie auf „wahr“ festlegen, werden die Funktionen der Webkomponenten v0 für alle Websites aktiviert.

Wenn Sie diese Richtlinie auf "falsch" festlegen oder diese Richtlinie nicht festlegen, werden die Funktionen der Webkomponenten v0 standardmäßig deaktiviert, beginnend mit M80.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: WebComponentsV0Enabled
  - GP-Name: Erneute Aktivierung der Web Components v0-API bis M84 (veraltet)
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: WebComponentsV0Enabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: WebComponentsV0Enabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### WebDriverOverridesIncompatiblePolicies

  #### Zulassen, dass WebDriver inkompatible Richtlinien außer Kraft setzt (veraltet)

  >VERALTET: Diese Richtlinie ist veraltet. Sie wird zurzeit unterstützt, aber in einer zukünftigen Version als veraltet behandelt.
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77, bis 84

  #### Beschreibung

  Diese Richtlinie funktioniert nicht, da WebDriver nun mit allen vorhandenen Richtlinien kompatibel ist.

Diese Richtlinie ermöglicht es Benutzern der WebDriver-Funktion, Richtlinien außer Kraft zu setzen, die sich auf seinen Betrieb auswirken könnten.

Diese Richtlinie deaktiviert aktuell die Richtlinien [SitePerProcess](#siteperprocess) und [IsolateOrigins](#isolateorigins).

Wenn die Richtlinie aktiviert ist, kann WebDriver inkompatible Richtlinien außer Kraft setzen.
Wenn die Richtlinie deaktiviert oder nicht konfiguriert ist, ist es WebDriver nicht gestattet, inkompatible Richtlinien außer Kraft zu setzen.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: WebDriverOverridesIncompatiblePolicies
  - GP-Name: Zulassen, dass WebDriver inkompatible Richtlinien außer Kraft setzt (veraltet)
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: WebDriverOverridesIncompatiblePolicies
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: WebDriverOverridesIncompatiblePolicies
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### WebRtcLocalIpsAllowedUrls

  #### Verwaltung der Gefährdung lokaler IP-Adressen durch WebRTC

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 80 oder höher

  #### Beschreibung

  Gibt eine Liste der Ursprünge (URLs) oder Hostnamen-Muster (wie "*contoso.com*") an, für die die lokale IP-Adresse von WebRTC verfügbar gemacht werden soll.

Wenn Sie diese Richtlinie aktivieren und eine Liste von Ursprüngen (URLs) oder Hostnamen-Mustern festlegen, wird beim Aktivieren von edge://flags/#enable-webrtc-hide-local-ips-with-mdns die lokale IP-Adresse von WebRTC für Fälle verfügbar gemacht, die den Mustern in der Liste entsprechen.

Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren und edge://flags/#enable-webrtc-hide-local-ips-with-mdns aktiviert ist, werden in WebRTC keine lokalen IP-Adressen verfügbar gemacht. Die lokale IP-Adresse wird mit einem mDNS-Hostnamen verborgen.

Wenn Sie diese Richtlinie aktivieren, deaktivieren oder nicht konfigurieren und edge://flags/#enable-webrtc-hide-local-ips-with-mdns deaktiviert ist, werden in WebRTC lokale IP-Adressen verfügbar gemacht.

Bitte beachten Sie, dass diese Richtlinie den Schutz lokaler IP-Adressen, der für Administratoren ggf. erforderlich ist, schwächt.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Liste von Zeichenfolgen

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: WebRtcLocalIpsAllowedUrls
  - GP-Name: Verwaltung der Gefährdung lokaler IP-Adressen durch WebRTC
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge\WebRtcLocalIpsAllowedUrls
  - Pfad (Empfohlen): n.a.
  - Wertname: 1, 2, 3, ...
  - Werttyp: REG_SZ-Liste

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\WebRtcLocalIpsAllowedUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\WebRtcLocalIpsAllowedUrls\2 = "*contoso.com*"

```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: WebRtcLocalIpsAllowedUrls
  - Beispielwert:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>*contoso.com*</string>
</array>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### WebRtcLocalhostIpHandling

  #### Einschränken der Gefährdung lokaler IP-Adresse durch WebRTC

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Hiermit können Sie festlegen, ob WebRTC die lokale IP-Adresse des Benutzers verfügbar macht.

Wenn Sie diese Richtlinie auf „AllowAllInterfaces“ oder „AllowPublicAndPrivateInterfaces“ setzen, zeigt WebRTC die lokale IP-Adresse an.

Wenn Sie diese Richtlinie auf „AllowPublicInterfaceOnly“ oder „DisableNonProxiedUdp“ setzen, zeigt WebRTC die lokale IP-Adresse nicht an.

Wenn Sie diese Richtlinie nicht festlegen oder wenn Sie sie deaktivieren, macht WebRTC die lokale IP-Adresse verfügbar.

Zuordnung von Richtlinienoptionen:

* AllowAllInterfaces (Standard) = alle Schnittstellen zulassen. Dies zeigt die lokale IP-Adresse an.

* AllowPublicAndPrivateInterfaces (default_public_and_private_interfaces) = Öffentliche und private Schnittstellen über die HTTP-Standardroute zulassen. Dies zeigt die lokale IP-Adresse an.

* AllowPublicInterfaceOnly (standard_public_interface_only) = Öffentliche Schnittstelle über HTTP-Standardroute zulassen. Dadurch wird die lokale IP-Adresse nicht offengelegt

* DisableNonProxiedUp (disable_non_proxied_udp) = TCP verwenden, es sei denn, der Proxy-Server unterstützt UDP. Dadurch wird die lokale IP-Adresse nicht offengelegt

Verwenden Sie die vorstehenden Informationen, wenn Sie diese Richtlinie konfigurieren.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Zeichenfolge

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: WebRtcLocalhostIpHandling
  - GP-Name: Einschränken der Gefährdung lokaler IP-Adresse durch WebRTC
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: WebRtcLocalhostIpHandling
  - Werttyp: REG_SZ

  ##### Beispielwert:

```
"default"
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: WebRtcLocalhostIpHandling
  - Beispielwert:
``` xml
<string>default</string>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### WebRtcUdpPortRange

  #### Einschränken des von WebRTC verwendeten lokalen Bereichs an UDP-Ports

  
  
  #### Unterstützte Versionen:

  - Auf Windows und macOS ab 77 oder höher

  #### Beschreibung

  Schränkt den von WebRTC verwendeten UDP-Portbereich auf ein angegebenes Port-Intervall (Endpunkte eingeschlossen) ein.

Wenn Sie diese Richtlinie konfigurieren, geben Sie den Bereich lokaler UDP-Ports an, den WebRTC verwenden kann.

Wenn Sie diese Richtlinie nicht konfigurieren oder wenn Sie sie auf eine leere Zeichenfolge oder einen ungültigen Port-Bereich festlegen, kann WebRTC jeden verfügbaren lokalen UDP-Port verwenden.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Zeichenfolge

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: WebRtcUdpPortRange
  - GP-Name: Einschränken des von WebRTC verwendeten lokalen Bereichs an UDP-Ports
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: WebRtcUdpPortRange
  - Werttyp: REG_SZ

  ##### Beispielwert:

```
"10000-11999"
```

  #### Mac – Informationen und Einstellungen
  
  - Einstellung Schlüsselname: WebRtcUdpPortRange
  - Beispielwert:
``` xml
<string>10000-11999</string>
```
  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### WebWidgetAllowed

  #### Webwidget aktivieren

  
  
  #### Unterstützte Versionen:

  - Unter Windows ab Version 88 oder höher

  #### Beschreibung

  Aktiviert das Webwidget. Wenn diese Option aktiviert ist, können Benutzer das Widget verwenden, um im Internet vom Desktop aus oder über eine Anwendung zu suchen. Das Widget bietet ein Suchfeld, im dem Webvorschläge angezeigt werden, und öffnet alle Websuchen in Microsoft Edge. Im Suchfeld werden Vorschläge für die Suche (auf Bing gestützt) und für URLs angezeigt. Das Widget umfasst außerdem Feed-Kacheln, die angeklickt werden können, um weitere Informationen auf msn.com in einem neuen Tab oder im Fenster des Microsoft Edge-Browsers anzuzeigen. Die Feed-Kacheln könnten Werbeanzeigen enthalten. Das Widget kann über die Microsoft Edge-Einstellungen oder über das Menü "Weitere Tools" in Microsoft Edge gestartet werden.

Wenn Sie diese Richtlinie aktivieren oder nicht konfigurieren, ist das Web-Widget automatisch für alle Profile aktiviert.
In den Microsoft Edge-Einstellungen wird die Option zum Starten des Widgets angezeigt.
In den Microsoft Edge-Einstellungen wird das Menüelement zum Ausführen des Widgets beim Windows-Start (automatischer Start) angezeigt.
Wenn die Richtlinie [WebWidgetIsEnabledOnStartup](#webwidgetisenabledonstartup) aktiviert ist, ist die Option zum Aktivieren des Widgets beim Start auf „Ein“ gesetzt.
Wenn die Richtlinie [WebWidgetIsEnabledOnStartup-](#webwidgetisenabledonstartup) deaktiviert oder nicht konfiguriert ist, ist die Option zum Aktivieren des Widgets beim Start auf „Aus“ gesetzt.
Benutzer sehen das Menüelement, um das Widget über das Microsoft Edge-Menü "Weitere Tools" zu starten. Benutzer können das Widget über das Menü "Weitere Tools" starten.
Das Widget kann durch die Option "Beenden" in der Statusleiste oder durch Schließen des Widgets über die Taskleiste deaktiviert werden. Wenn die Autostart-Option ausgewählt wurde, wird das Widget beim Neustart des Systems neu gestartet.

Wenn Sie diese Richtlinie deaktivieren, wird das Web-Widget für alle Profile deaktiviert.
Die Option zum Starten des Widgets über die Microsoft Edge-Einstellungen wird deaktiviert.
Die Option zum Starten des Widget beim Windows-Start (automatischer Start) wird deaktiviert.
Die Option zum Starten des Widgets über das Microsoft Edge-Menü "Weitere Tools" wird deaktiviert.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - Eindeutiger GP-Name: WebWidgetAllowed
  - GP-Name: Webwidget aktivieren
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: WebWidgetAllowed
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### WebWidgetIsEnabledOnStartup

  #### Web-Widget beim Windows-Start zulassen

  
  
  #### Unterstützte Versionen:

  - Unter Windows ab Version 88 oder höher

  #### Beschreibung

  Gestattet dem Web-Widget beim Start von Windows zu starten.

Ist diese Option aktiviert, wird das Web-Widget standardmäßig beim Windows-Start ausgeführt.
Wenn das Widget über die Richtlinie [WebWidgetAllowed](#webwidgetallowed) deaktiviert wurde, startet diese Richtlinie das Widget nicht beim Windows-Start.

Wenn Sie diese Richtlinie deaktivieren, wird das Web-Widget beim Windows-Start für keines der Profile automatisch gestartet.
Die Option zum Starten des Widgets beim Windows-Start wird deaktiviert und in den Microsoft Edge-Einstellungen auf „Aus“ gesetzt.

Wenn Sie diese Richtlinie nicht konfigurieren, wird das Web-Widget beim Windows-Start für keines der Profile automatisch gestartet.
Die Option zum Starten des Widgets beim Windows-Start wird in den Microsoft Edge-Einstellungen auf „Aus“ gesetzt.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - Eindeutiger GP-Name: WebWidgetIsEnabledOnStartup
  - GP-Name: Web-Widget beim Windows-Start zulassen
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: WebWidgetIsEnabledOnStartup
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  

  [Zurück zum Anfang](#microsoft-edge---policies)

  ### WinHttpProxyResolverEnabled

  #### Verwenden von Windows-Proxy Konfliktlöser (verworfen)

  >VERALTET: Diese Richtlinie ist veraltet. Sie wird zurzeit unterstützt, aber in einer zukünftigen Version als veraltet behandelt.
  
  #### Unterstützte Versionen:

  - Unter Windows seit 84 oder später

  #### Beschreibung

  Diese Richtlinie wird nicht mehr unterstützt, da sie von einem ähnlichen Feature in einer zukünftigen Version abgelöst wird. Erfahren Sie mehr unter https://crbug.com/1032820.

Verwenden Sie Windows, um Proxys für alle Browser-Netzwerke zu beheben, anstelle des in Microsoft Edge integrierten Proxy-Konfliktlösers. Der Windows Proxy-Konfliktlöser ermöglicht Windows Proxy-Features wie DirectAccess/NRPT.

Diese Richtlinie umfasst die von https://crbug.com/644030beschriebenen Probleme. Es bewirkt, dass PAC-Dateien von Windows-Code abgerufen und ausgeführt werden, einschließlich PAC-Dateien, die über die [ProxyPacUrl-](#proxypacurl) Richtlinie festgelegt wurden. Da Netzwerk-Abrufe für die PAC-Datei über Windows statt mit Microsoft Edge-Code stattfinden, gelten Netzwerkrichtlinien wie [DnsOverHttpsMode](#dnsoverhttpsmode) nicht für Netzwerk-Abrufe für eine PAC-Datei.

Wenn Sie diese Richtlinie aktivieren, wird der Windows Proxy-Konfliktlöser verwendet.

Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, wird der Microsoft Edge Proxy-Konfliktlöser verwendet.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein – erfordert Browser-Neustart

  #### Datentyp:

  - Boolesch

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - Eindeutiger Name des GP: WinHttpProxyResolverEnabled
  - GP-Name: Verwenden von Windows-Proxy Konfliktlöser (verworfen)
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/
  - GP Pfad (Empfohlen): n.a.
  - GP ADMX Dateiname: MSEdge.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): n.a.
  - Wertname: WinHttpProxyResolverEnabled
  - Werttyp: REG_DWORD

  ##### Beispielwert:

```
0x00000001
```

  

  [Zurück zum Anfang](#microsoft-edge---policies)


## Weitere Informationen

- [Konfigurieren von Microsoft Edge](configure-microsoft-edge.md)
- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)
- [Microsoft Sicherheitsbaselines-Blog](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/bg-p/Microsoft-Security-Baselines)