---
title: Versionshinweise von Microsoft Edge für Stable Channel
ms.author: leahtu
author: dan-wesley
manager: srugh
ms.date: 10/22/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Versionshinweise von Microsoft Edge für Stable Channel
ms.openlocfilehash: e416f04adfdd96f7d14cb662ce2a1fd052951d26
ms.sourcegitcommit: f0966278011219cbab4590487a8b34cb76a73232
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/22/2021
ms.locfileid: "12107450"
---
# <a name="release-notes-for-microsoft-edge-stable-channel"></a>Versionshinweise für Microsoft Edge Stable Channel

Diese Versionshinweise enthalten Informationen zu neuen Funktionen und nicht sicherheitsrelevanten Updates, die im Microsoft Edge Stable Channel enthalten sind.

- Alle Sicherheitsupdates werden [hier](microsoft-edge-relnotes-security.md) aufgelistet.
- Archivierte Versionshinweise für Microsoft Edge Stable Channel finden Sie [hier.](microsoft-edge-relnote-archive-stable-channel.md)

 Informationen zu Microsoft Edge-Kanälen finden Sie in der [Übersicht über die Microsoft Edge-Kanäle](microsoft-edge-channels.md).

> [!NOTE]
> Für den Stable Channel erfolgt das Rollout von Updates progressiv über einen oder mehrere Tage. Weitere Informationen hierzu finden Sie unter [Progressive Rollouts für Microsoft Edge-Updates](microsoft-edge-update-progressive-rollout.md).
>
> Die Microsoft Edge-Webplattform entwickelt sich ständig weiter, um Benutzerfreundlichkeit, Sicherheit und Datenschutz zu verbessern. Weitere Informationen finden Sie unter [Kommende Änderungen in Microsoft Edge mit Auswirkungen auf die Websitekompatibilität](/microsoft-edge/web-platform/site-impacting-changes).

## <a name="version-950102030-october-21"></a>Version95.0.1020.30: 21.Oktober

Stable Channel-Sicherheitsupdates sind [hier](/deployedge/microsoft-edge-relnotes-security#october-21-2021) aufgeführt.

### <a name="feature-updates"></a>Funktionsupdates

- **Support für „Im Datei-Explorer anzeigen“ für Microsoft Office SharePoint Online-Bibliotheken in Microsoft Edge.**  Jetzt können Sie die Funktion „Im Datei-Explorer anzeigen“ in modernen Microsoft Office SharePoint Online-Dokumentbibliotheken aktivieren. Damit diese Erfahrung für Ihre Benutzer sichtbar und funktionsfähig ist, müssen Sie die Microsoft Edge-Richtlinie [Konfigurieren des Features „Im Datei-Explorer anzeigen“ für Microsoft Office SharePoint Online-Seiten in Microsoft Edge](/deployedge/microsoft-edge-policies#configureviewinfileexplorer) aktivieren und Ihre Microsoft Office SharePoint Online-Mandantenkonfiguration aktualisieren. Weitere Informationen: [Anzeigen von Microsoft Office SharePoint Online-Dateien mit dem Datei-Explorer in Microsoft Edge](/SharePoint/sharepoint-view-in-edge).

- **Datei-URL-Links für Intranetzonen werden im Windows-Datei-Explorer geöffnet.**  Sie können zulassen, dass Datei-URL-Links zu Intranetzonen-Dateien, die von Intranetzonen-HTTPS-Websites stammen, den Windows-Datei-Explorer für diese Datei oder dieses Verzeichnis öffnen. Sie können diese Erfahrung mithilfe der Richtlinie [IntranetFileLinksEnabled](/deployedge/microsoft-edge-policies#intranetfilelinksenabled) aktivieren.

- **Verbesserungen an der Downloaderfahrung.** Die Unterstützung für das Herunterladen der Benutzererfahrung wurde auf progressive Webanwendungen (PWAs) und WebView erweitert. Wir beginnen auch mit der Unterstützung von Drag & Drop zum Datei-Explorer und zum Desktop.

- **Machen Sie dort weiter, wo Sie in PDF-Dokumenten aufgehört haben.**  Sie können jetzt den Lesevorgang dort fortsetzen, wo Sie Ihr PDF-Dokument zuletzt geschlossen haben.

- **Der Effizienzmodus verlängert die Akkulaufzeit, wenn Ihr Laptop in den Stromsparmodus wechselt.**  Der Effizienzmodus wird aktiv, wenn Ihr Laptop in Stromsparmodus wechselt, um dem Browser die Verwaltung der Ressourcennutzung zur Verlängerung der Akkulaufzeit Ihres Computers zu ermöglichen. Sie haben vier Optionen, wenn der Effizienzmodus aktiv wird: „Nicht eingesteckt und niedriger Akkustand“, „Nicht eingesteckt“, „Immer“ und „Nie“. Hinweis: Hierbei handelt es sich um ein Feature für den kontrollierten Rollout. Wenn Sie dieses Feature nicht sehen, schauen Sie in Kürze wieder vorbei, während wir mit dem Rollout fortfahren.

- **Freiformtextfelder, die PDF-Dokumenten hinzugefügt werden.** Wir unterstützen jetzt das Hinzufügen von Freiformtextfeldern zu PDF-Dokumenten. Sie können diese Felder verwenden, um Formulare auszufüllen und sichtbare Notizen hinzuzufügen.

- **Die Unterstützung für Zitate wurde „Sammlungen“ hinzugefügt.**  Wir haben die Erfahrung „Sammlungen“ verbessert, insbesondere für Schüler/Studenten und Forscher. „Sammlungen“ unterstützt jetzt Zitate und Leselisten.

- **Aktualisieren Sie Ihre Kennwörter schneller und mit weniger Klicks.** Der Browser führt Sie jetzt direkt zur Seite „Kennwort ändern“ für eine bestimmte Website. Durch diese Aktion sparen Sie Zeit und Klicks, da Sie nicht mehr manuell zur Seite navigieren müssen. Nachdem Sie sich auf dieser Seite befinden, füllt der Browser ihr vorhandenes Kennwort ebenfalls automatisch aus und schlägt ein starkes, eindeutiges neues Kennwort vor.  Hinweis: Dieses Feature ist derzeit nur auf einer begrenzten Anzahl von Websites verfügbar.

- **Automatische Kontoerstellung.** Wir bieten jetzt zusätzlichen Support auf Registrierungsseiten, indem wir Ihnen das Erstellen eines Onlinekontos mit nur einem Klick ermöglichen. Wählen Sie dazu die Dropdownliste „Vorschlag“ aus, wenn Sie im Registrierungsformular auf ein beliebiges Formularfeld klicken. Auf diese Weise werden nicht nur Informationen angezeigt, die für das Registrierungsformular relevant sind, sondern auch ein Vorschlag für ein starkes neues Kennwort. Nach der Auswahl werden alle relevanten Informationen in den entsprechenden Feldern aufgefüllt, und das vorgeschlagene Kennwort wird bei der Übermittlung an die Website automatisch gespeichert. Hinweis: Dieses Feature ist derzeit nur auf einer begrenzten Anzahl von Websites verfügbar.

### <a name="policy-updates"></a>Richtlinienupdates

#### <a name="new-policies"></a>Neue Richtlinien

- [BrowserLegacyExtensionPointsBlockingEnabled](/DeployEdge/microsoft-edge-policies#browserlegacyextensionpointsblockingenabled) Blockierung von Legacy-Browsererweiterungspunkten aktivieren
- [CrossOriginWebAssemblyModuleSharingEnabled](/DeployEdge/microsoft-edge-policies#crossoriginwebassemblymodulesharingenabled) Gibt an, ob WebAssembly-Module ursprungsübergreifend gesendet werden können.
- [DisplayCapturePermissionsPolicyEnabled](/DeployEdge/microsoft-edge-policies#displaycapturepermissionspolicyenabled) Gibt an, ob die Berechtigungsrichtlinie für die Anzeigeerfassung aktiviert oder übersprungen wird.
- [InternetExplorerIntegrationWindowOpenHeightAdjustment](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationwindowopenheightadjustment) Konfigurieren der Pixelanpassung zwischen window.open-Höhen, die von Seiten im IE-Modus stammen, im Vergleich zu Seiten im Microsoft Edge-Modus.
- [InternetExplorerIntegrationWindowOpenWidthAdjustment](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationwindowopenwidthadjustment) Konfigurieren der Pixelanpassung zwischen window.open-Breiten, die von Seiten im IE-Modus stammen, im Vergleich zu Seiten im Microsoft Edge-Modus.
- [IntranetFileLinksEnabled](/DeployEdge/microsoft-edge-policies#intranetfilelinksenabled) Zulassen, dass Datei-URL-Links von Intranetzonen von Microsoft Edge im Windows-Datei-Explorer geöffnet werden
- [NewSmartScreenLibraryEnabled](/DeployEdge/microsoft-edge-policies#newsmartscreenlibraryenabled) Neue SmartScreen-Bibliothek aktivieren
- [ShadowStackCrashRollbackBehavior](/DeployEdge/microsoft-edge-policies#shadowstackcrashrollbackbehavior) Konfigurieren des ShadowStack-Absturzrollbackverhaltens
- [VisualSearchEnabled](/DeployEdge/microsoft-edge-policies#visualsearchenabled) Visuelle Suche aktiviert

#### <a name="obsoleted-policies"></a>Abgeschaffte Richtlinien

- [InternetExplorerIntegrationTestingAllowed](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationtestingallowed): Zulassen von Internet Explorer-Modustests
- [LegacySameSiteCookieBehaviorEnabled](/DeployEdge/microsoft-edge-policies#legacysamesitecookiebehaviorenabled) Aktivieren der Standardeinstellung für das Verhalten von Legacy-SameSite-Cookies


## <a name="version-94099250-october-14"></a>Version94.0.992.50: 14.Oktober

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-94099247-october-11"></a>Version94.0.992.47: 11.Oktober

Sicherheitsupdates im Stabilen Kanal sind [hier](/deployedge/microsoft-edge-relnotes-security#october-11-2021) aufgeführt.

## <a name="version-94099238-october-1"></a>Version 94.0.992.38: 1. Oktober

> [!Important]
> Dieses Update enthält einen Fix für [CVE-2021-37975](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-37975) und [CVE-2021-37976](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-37976), die vom Chromium-Team als Exploit gemeldet wurden. Weitere Informationen finden Sie im [Leitfaden für Sicherheitsupdates](https://msrc.microsoft.com/update-guide)

Sicherheitsupdates im Stabilen Kanal sind [hier](/deployedge/microsoft-edge-relnotes-security#october-01-2021) aufgeführt.

## <a name="version-94099237-september-30"></a>Version 94.0.992.37: 30. September

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-94099231-september-24"></a>Version 94.0.992.31: 24. September

> [!Important]
> Dieses Update enthält einen Fix für [CVE-2021-37973](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-37973), der vom Chromium-Team als Exploit gemeldet wurde. Weitere Informationen finden Sie im [Leitfaden zu Sicherheitsupdates](https://msrc.microsoft.com/update-guide).

Sicherheitsupdates im Stabilen Kanal sind [hier](/deployedge/microsoft-edge-relnotes-security#september-24-2021) aufgeführt.

### <a name="feature-updates"></a>Funktionsupdate

- **Der Wechsel zu einem vierwöchigen Rhythmus der Updates für Microsoft Edge ist abgeschlossen.**  Wir haben einen neuen 4-wöchigen Veröffentlichungszyklus für Hauptversionen eingeführt. Weitere Informationen finden Sie hier: https://blogs.windows.com/msedgedev/2021/03/12/new-release-cycles-microsoft-edge-extended-stable/

- **Neue Option „Stabil (Erweitert)“ wird angeboten.**  Wir bieten unseren verwalteten Enterprise-Kunden eine neue Option „Stabil (Erweitert)“ an. Die Option „Stabil (Erweitert)“ bleibt bei geraden Revisionsnummern und wird alle 8 Wochen aktualisiert. Es wird ein zweiwöchentliches Sicherheitsupdate geben.  Weitere Informationen finden Sie hier: https://blogs.windows.com/msedgedev/2021/07/15/opt-in-extended-stable-release-cycle/

- **Verbesserungen des Standardverhaltens beim Öffnen von MHTML-Dateien.**  MHTML-Dateien werden weiterhin im IE-Modus geöffnet, wenn der IE-Modus aktiviert ist, es sei denn, die MHTML-Datei wurde aus Microsoft Edge heraus gespeichert (mit den Optionen „Speichern unter“ oder „Seite speichern unter“ in Microsoft Edge). Wenn die Datei aus Microsoft Edge heraus gespeichert wurde, wird sie nun in Microsoft Edge geöffnet.  Diese Änderung behebt ein Renderingproblem, das beim Öffnen einer MHTML-Datei im IE-Modus festgestellt wurde, wenn diese aus Microsoft Edge heraus gespeichert wurde.

- **Beschränken Sie private Netzwerkanforderungen auf sichere Kontexte.** Der Zugriff auf Ressourcen in lokalen Netzwerken (Intranet) von Seiten im Internet erfordert, dass diese Seiten über HTTPS bereitgestellt werden. Diese Änderung erfolgt im Chromium-Projekt, auf dem Microsoft Edge basiert. Weitere Informationen finden Sie im [Chrome-Plattformstatuseintrag](https://chromestatus.com/feature/5436853517811712). Zur Unterstützung von Szenarien, in denen die Kompatibilität mit nicht sicheren Seiten beibehalten werden muss, stehen zwei Kompatibilitätsrichtlinien zur Verfügung: [InsecurePrivateNetworkRequestAllowed](/deployedge/microsoft-edge-policies#insecureprivatenetworkrequestsallowed) und [InsecurePrivateNetworkRequestAllowedForUrls](/deployedge/microsoft-edge-policies#insecureprivatenetworkrequestsallowedforurls).

- **Blockieren Sie Downloads gemischter Inhalte.** Sichere Seiten laden nur Dateien herunter, die auf anderen sicheren Seiten gehostet werden, und auf nicht sicheren Seiten (nicht HTTPS) gehostete Downloads werden blockiert, wenn sie von einer sicheren Seite aus initiiert wurden. Diese Änderung erfolgt im Chromium-Projekt, auf dem Microsoft Edge basiert. Für weitere Informationen navigieren Sie zum [Google Security-Blogeintrag](https://security.googleblog.com/2020/02/protecting-users-from-insecure_6.html).

- **Aktivieren Sie die implizite Anmeldung für lokale Konten.** Durch Aktivieren der Richtlinie [OnlyOnPremisesImplicitSigninEnabled](/deployedge/microsoft-edge-policies#onlyonpremisesimplicitsigninenabled) werden nur lokale Konten für die implizite Anmeldung aktiviert.  Microsoft Edge wird keine implizite Anmeldung bei MSA- oder AAD-Konten versuchen. Das Upgrade von lokalen Konten auf AAD-Konten wird ebenfalls beendet.

- **Neue Seite für Barrierefreiheitseinstellungen.**  Wir haben Einstellungen im Zusammenhang mit Barrierefreiheit auf einer einzigen Seite zusammengefasst. Sie finden die neue Seite „edge://settings/accessibility „ unter der Liste mit den Haupteinstellungen. Hier finden Sie Einstellungen, um die Webseite zu vergrößern, eine Gliederung mit hoher Sichtbarkeit um den Fokusbereich anzuzeigen, sowie andere Einstellungen, die Ihnen helfen, Ihre Webbrowsingerfahrung zu verbessern. In zukünftigen Versionen von Microsoft Edge werden wir weitere neue Einstellungen hinzufügen.

***Neue Richtlinien***

- [ApplicationGuardPassiveModeEnabled](/DeployEdge/microsoft-edge-policies#applicationguardpassivemodeenabled) Application Guard-Websitelistenkonfiguration ignorieren und Edge normal nutzen
- [OnlyOnPremisesImplicitSigninEnabled](/DeployEdge/microsoft-edge-policies#onlyonpremisesimplicitsigninenabled) Nur lokale Konten, die für die implizite Anmeldung aktiviert sind
- [WebRtcRespectOsRoutingTableEnabled](/DeployEdge/microsoft-edge-policies#webrtcrespectosroutingtableenabled) Unterstützung für Windows-BS-Routingtabellenregeln beim Herstellen von Peer-to-Peer-Verbindungen über WebRTC aktivieren

***Veraltete Richtlinie***

- [UserAgentClientHintsEnabled](/DeployEdge/microsoft-edge-policies#useragentclienthintsenabled): Die Funktion „User-Agent Client Hints“ aktivieren

## <a name="version-93096152-september-16"></a>Version 93.0.961.52: 16. September

>[!Important]
>Dieses Update enthält einen Fix für [CVE-2021-30633,](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-30632) der vom Chromium-Team als Exploit gemeldet wurde. Weitere Informationen finden Sie im [Leitfaden zu Sicherheitsupdates](https://msrc.microsoft.com/update-guide).

Stable Channel-Sicherheitsupdates sind [hier](/deployedge/microsoft-edge-relnotes-security#september-16-2021) aufgeführt.

## <a name="version-93096147-september-11"></a>Version 93.0.961.47: 11. September

> [!Important]
> Dieses Update enthält einen Fix für [CVE-2021-30632](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-30632), für das laut dem Chromium-Team ein Exploit im Umlauf ist. Weitere Informationen finden Sie im [Leitfaden zu Sicherheitsupdates](https://msrc.microsoft.com/update-guide).

Stable Channel-Sicherheitsupdates sind [hier](/deployedge/microsoft-edge-relnotes-security#september-11-2021) aufgeführt.

## <a name="version-93096144-september-9"></a>Version 93.0.961.44: 9. September

Stable Channel-Sicherheitsupdates sind [hier](/deployedge/microsoft-edge-relnotes-security#september-09-2021) aufgeführt.

## <a name="version-93096138-september-2"></a>Version 93.0.961.38: 2. September

Stable Channel-Sicherheitsupdates sind [hier](/deployedge/microsoft-edge-relnotes-security#september-02-2021) aufgeführt.

### <a name="feature-updates"></a>Funktionsupdates

- **Voreinstellungen in Microsoft Edge.**  Microsoft Edge unterstützt jetzt eine begrenzte Anzahl von Voreinstellungen (ehemals Mastereinstellungen). IT-Administratoren können diese Einstellungen standardmäßig bereitstellen, bevor der Browser zum ersten Mal von seinen Benutzern ausgeführt wird. Weitere Informationen finden Sie hier: [Konfigurieren sie Microsoft Edge mithilfe der Einstellungen für die Voreinstellungen für die erste Ausführung.](/deployedge/initial-preferences-support-on-microsoft-edge-browser)

- **Der IE-Modus auf Microsoft Edge unterstützt das "no-merge" Verhalten.**  Wenn ein Endbenutzer ein neues Browserfenster von einer IE-Modusanwendung aus startet, befindet es sich in einer separaten Sitzung, ähnlich dem "no-merge" Verhalten in IE11. Sie müssen Ihre Websiteliste anpassen, um Websites zu konfigurieren, die die Sitzungsfreigabe als "no-merge" verhindern müssen. Im Hintergrund wird für jedes Fenster von Microsoft Edge beim ersten Aufrufen einer IE-Modusregisterkarte in diesem Fenster, wenn es sich um eine der vorgesehenen "no-merge"-Websites handelt, dieses Fenster in eine andere "no-merge" IE-Sitzung von allen anderen Microsoft Edge-Fenstern gesperrt, mindestens bis die letzte Registerkarte für den IE-Modus in diesem Fenster geschlossen wird. Dies folgt dem vorherigen Verhalten, bei dem Benutzer IE ohne Zusammenführung starten und auch Microsoft Edge ohne Zusammenführung über andere Mechanismen starten konnten.  Weitere Informationen finden Sie hier: [Problembehandlung im IE-Modus und häufig gestellte Fragen | Microsoft-Dokumentation](/deployedge/edge-ie-mode-faq#does-ie-mode-on-microsoft-edge-support-the--nomerge--option-that-was-supported-in-internet-explorer-11-)

- **Neue Richtlinie zum Beenden der impliziten Anmeldung.**  Mit der [ImplicitSignInEnabled](/deployedge/microsoft-edge-policies#implicitsigninenabled)-Richtlinie können Systemadministratoren die implizite Anmeldung bei Microsoft Edge Browsern deaktivieren.

- **Richtlinien zum Umgehen von ClickOnce- und DirectInvoke-Eingabeaufforderungen.** Wir haben unsere Richtlinien aktualisiert, um die Umgehung von ClickOnce-Eingabeaufforderungen und der DirectInvoke-App für angegebene Dateitypen aus angegebenen Domänen zu ermöglichen. Dazu müssen Sie folgende Schritte ausführen:

  - Aktivieren von [ClickOnceEnabled](/deployedge/microsoft-edge-policies#clickonceenabled) oder [DirectInvokeEnabled](/deployedge/microsoft-edge-policies#directinvokeenabled)
  - Aktivieren Sie die [AutoOpenFileTypes](/deployedge/microsoft-edge-policies#autoopenfiletypes)-Richtlinie und legen Sie die Liste der spezifischen Dateitypen fest, für die ClickOnce und DirectInvoke deaktiviert werden sollen.
  - Aktivieren Sie die [AutoOpenAllowedForURLs](/deployedge/microsoft-edge-policies#autoopenallowedforurls)-Richtlinie und legen Sie die Liste bestimmter Domänen fest, für die ClickOnce und DirectInvoke deaktiviert werden.

  Hinweis: AutoOpenAllowedForURLs ist eine Supporterrichtlinie für AutoOpenFileTypes. Wenn AutoOpenAllowedForURLs nicht festgelegt und AutoOpenFileTypes festgelegt ist, werden die aufgelisteten Dateitypen automatisch über alle URLs geöffnet.

- **Registerkartengruppen.**  Wir aktivieren die Registerkartengruppierung, die die Möglichkeit bietet, Registerkarten in benutzerdefinierte Gruppen zu kategorisieren, und Ihnen dabei hilft, Registerkarten effektiver in mehreren Arbeitsstreams zu finden, zwischen ihnen zu wechseln und sie zu verwalten.  

- **Blenden Sie die Titelleiste aus, während Sie vertikale Registerkarten verwenden.**  Holen Sie sich die zusätzlichen Pixel zurück, indem Sie die Titelleiste des Browsers ausblenden, während Sie sich auf vertikalen Registerkarten befinden. Jetzt können Sie zu edge://settings/appearance wechseln und unter dem Abschnitt Symbolleiste anpassen die Option auswählen, um die Titelleiste im modus "Vertikale Registerkarte" auszublenden.

- **Videobild in Bild (PiP) auf der Symbolleiste mit dem Mauszeiger.**  Wenn Sie auf ein unterstütztes Video zeigen, wird eine Symbolleiste angezeigt, mit der Sie dieses Video in einem PiP-Fenster anzeigen können.  Hinweis: Dies ist derzeit für Microsoft Edge Benutzer unter macOS verfügbar.  

- **Entfernen von 3DES in TLS. Die Unterstützung für die TLS_RSA_WITH_3DES_EDE_CBC_SHA Verschlüsselungssammlung wird entfernt.** Diese Änderung erfolgt im Chromium-Projekt, auf dem Microsoft Edge basiert. Weitere Informationen finden Sie im [Chrome-Plattformstatuseintrag](https://chromestatus.com/feature/6678134168485888). Darüber hinaus steht in Microsoft Edge Version 93 die [TripleDESEnabled](/deployedge/microsoft-edge-policies#tripledesenabled)-Richtlinie zur Unterstützung von Szenarien zur Verfügung, die die Kompatibilität mit veralteten Servern beibehalten müssen. Diese Kompatibilitätsrichtlinie wird veraltet und funktioniert nicht mehr in Microsoft Edge Version 95. Stellen Sie sicher, dass Sie betroffene Server vorher aktualisieren.

***Neue Richtlinien***

- [AutoplayAllowlist](/DeployEdge/microsoft-edge-policies#autoplayallowlist) Zulassen der automatischen Medienwiedergabe auf bestimmten Websites
- [CECPQ2Enabled](/DeployEdge/microsoft-edge-policies#cecpq2enabled) CECPQ2 Post Quantum Key Agreement für TLS aktiviert
- [ConfigureViewInFileExplorer](/DeployEdge/microsoft-edge-policies#configureviewinfileexplorer) Konfigurieren des Features „Im Datei-Explorer anzeigen“ für SharePoint-Seiten in Microsoft Edge
- [DefaultJavaScriptJitSetting](/DeployEdge/microsoft-edge-policies#defaultjavascriptjitsetting) Steuern der Verwendung von JavaScript-JIT
- [ShowPDFDefaultRecommendationsEnabled](/DeployEdge/microsoft-edge-policies#showpdfdefaultrecommendationsenabled) Zulassen von Benachrichtigungen zum Festlegen von Microsoft Edge als standardmäßigen PDF-Reader
- [FeatureFlagOverridesControl](/DeployEdge/microsoft-edge-policies#featureflagoverridescontrol) Konfigurieren der Möglichkeit von Benutzern, Featurekennzeichnungen außer Kraft zu setzen
- [ImplicitSignInEnabled](/DeployEdge/microsoft-edge-policies#implicitsigninenabled) Aktivieren der impliziten Anmeldung
- [InternetExplorerIntegrationCloudSiteList](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationcloudsitelist) Konfigurieren der Unternehmensmodus-Cloudwebsiteliste
- [InternetExplorerIntegrationSiteListRefreshInterval](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationsitelistrefreshinterval) Konfigurieren, wie häufig die Unternehmensmodus-Cloudwebsiteliste aktualisiert wird
- [JavaScriptJitAllowedForSites](/DeployEdge/microsoft-edge-policies#javascriptjitallowedforsites) Zulassen, dass JavaScript JIT auf diesen Websites verwendet
- [JavaScriptJitBlockedForSites](/DeployEdge/microsoft-edge-policies#javascriptjitblockedforsites) Blockieren der Verwendung von JIT in JavaScript auf diesen Websites
- [LocalBrowserDataShareEnabled](/DeployEdge/microsoft-edge-policies#localbrowserdatashareenabled) Zulassen, dass Windows lokale Microsoft Edge-Browserdaten durchsucht
- [MAUEnabled](/DeployEdge/microsoft-edge-policies#mauenabled) Microsoft AutoUpdate immer als Updater für Microsoft Edge verwenden
- [MSAWebSiteSSOUsingThisProfileAllowed](/DeployEdge/microsoft-edge-policies#msawebsitessousingthisprofileallowed) Anmelden für Microsoft-Websites mit diesem Profil zulassen
- [OneAuthAuthenticationEnforced](/DeployEdge/microsoft-edge-policies#oneauthauthenticationenforced) Erzwungener OneAuth-Authentifizierungsablauf für die Anmeldung
- [PasswordGeneratorEnabled](/DeployEdge/microsoft-edge-policies#passwordgeneratorenabled) Zulassen, dass Benutzer einen Vorschlag für sichere Kennwörter erhalten, wenn sie ein Konto online erstellen
- [PrimaryPasswordSetting](/DeployEdge/microsoft-edge-policies#primarypasswordsetting) Konfiguriert eine Einstellung, die Benutzer auffordert, ihr Gerätekennwort einzugeben bei Verwendung des automatischen Ausfüllens von Kennwörtern
- [PrintingWebpageLayout](/DeployEdge/microsoft-edge-policies#printingwebpagelayout) Legt das Layout für das Drucken fest
- [RemoteDebuggingAllowed](/DeployEdge/microsoft-edge-policies#remotedebuggingallowed) Zulassen des Remotedebuggings
- [RelaunchWindow](/DeployEdge/microsoft-edge-policies#relaunchwindow) Festlegen des Zeitintervalls für den Neustart
- [TravelAssistanceEnabled](/DeployEdge/microsoft-edge-policies#travelassistanceenabled) Aktivieren der Reiseunterstützung
- [TripleDESEnabled](/DeployEdge/microsoft-edge-policies#tripledesenabled) Aktivieren von 3DES-Verschlüsselungssammlungen in TLS
- [WAMAuthBelowWin10RS3Enabled](/DeployEdge/microsoft-edge-policies#wamauthbelowwin10rs3enabled) WAM für die Authentifizierung unter Windows 10 WAMAuthBelowWin10RS3Enabled aktiviert

***Veraltete Richtlinie***

- [LegacySameSiteCookieBehaviorEnabled](/DeployEdge/microsoft-edge-policies#legacysamesitecookiebehaviorenabled) Aktivieren der Standardeinstellung für das Verhalten von Legacy-SameSite-Cookies

***Veraltete Richtlinie***

- [NewTabPageSetFeedType](/DeployEdge/microsoft-edge-policies#newtabpagesetfeedtype) Konfigurieren der Microsoft Edge-Oberfläche für neue Registerkartenseiten

***Zusätzliche Änderung***

- [ConfigureShare](/DeployEdge/microsoft-edge-policies#configureshare) Hinzufügen der Mac-Plattformunterstützung
- [PasswordMonitorAllowed](/DeployEdge/microsoft-edge-policies#passwordmonitorallowed) Hinzufügen der Mac-Plattformunterstützung

## <a name="version-92090284-august-26"></a>Version 92.0.902.84: 26. August

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-92090278-august-19"></a>Version 92.0.902.78: 19. August

Stable Channel-Sicherheitsupdates sind [hier](/deployedge/microsoft-edge-relnotes-security#august-19-2021) aufgeführt.

## <a name="version-92090273-august-12"></a>Version 92.0.902.73: 12. August

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-92090267-august-5"></a>Version 92.0.902.67: 5. August

Stable Channel-Sicherheitsupdates sind [hier](/deployedge/microsoft-edge-relnotes-security#august-05-2021) aufgeführt.

## <a name="version-92090262-july-29"></a>Version 92.0.902.62: 29. Juli

Verschiedene Fehler und Leistungsprobleme wurden behoben.

### <a name="modified-policy"></a>Geänderte Richtlinie

- AutoplayAllowed – Die Einstellung auf „Disabled“ setzt die automatische Medienwiedergabe jetzt auf „Limit“

## <a name="version-92090255-july-22"></a>Version 92.0.902.55: 22. Juli

Stable Channel-Sicherheitsupdates sind [hier](/deployedge/microsoft-edge-relnotes-security#july-22-2021) aufgeführt.

### <a name="feature-updates"></a>Funktionsupdates

**Benutzer können auf Internet Explorer-Modus auf Microsoft Edge problemlos wechseln**. Ab Microsoft Edge Version 92 können Benutzer eine Website im Internet Explorer-Modus auf Microsoft Edge neu laden, anstatt sich auf die eigenständige IE 11-Anwendung zu verlassen, während sie auf die Konfiguration einer Website in der Websiteliste für den Enterprise-Modus warten. Benutzer werden aufgefordert, die Website ihrer lokalen Websiteliste hinzuzufügen, sodass die Navigation zu derselben Seite in Microsoft Edge für die nächsten 30 Tage automatisch im IE-Modus gerendert wird. Mit der [InternetExplorerIntegrationReloadInIEModeAllowed](/deployedge/microsoft-edge-policies#internetexplorerintegrationreloadiniemodeallowed)-Richtlinie können Sie diese Umgebung konfigurieren und den Zugriff auf die Einstiegspunkte des IE-Modus sowie die Möglichkeit zum Hinzufügen von Websites zur lokalen Websiteliste zulassen. Mit der [InternetExplorerIntegrationLocalSiteListExpirationDays](/deployedge/microsoft-edge-policies#internetexplorerintegrationlocalsitelistexpirationdays)-Richtlinie können Sie die Anzahl der Tage anpassen, die Websites in der lokalen Websiteliste gespeichert werden sollen. Beachten Sie, dass KB5003698 oder höher für Windows 10, Version 1909, erforderlich ist; oder KB5003690 oder höher für Windows 10, Version 2004, Windows 10, Version 20H2 oder Windows 10, Version 21H1, für die End-to-End-Erfahrung erforderlich ist. Weitere Informationen finden Sie unter [Lokale Websiteliste für den IE-Modus.](/deployedge/edge-ie-mode-local-site-list)

**MHTML-Dateien werden standardmäßig im Internet Explorer-Modus geöffnet**. Ab Microsoft Edge Version 92 Stable werden MHTML-Dateitypen automatisch im Internet Explorer-Modus auf Microsoft Edge anstelle der Internet Explorer-Anwendung (IE11) geöffnet. Dies wird am häufigsten beim Versuch beobachtet, Outlook-E-Mails in einem Browser anzuzeigen. Diese Änderung tritt nur auf, wenn IE11 der Standardhandler für diesen Dateityp ist. Wenn Sie dies lieber ändern möchten, können Sie dies vor der Installation des Stable Version 92-Updates mithilfe [dieser Anleitung](/docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration) tun.

**Die Warnung „Entwicklermoduserweiterungen deaktivieren“ kann zwei Wochen lang geschlossen werden.** Ab Microsoft Edge Version 92 können Sie die Warnung „Entwicklermoduserweiterungen deaktivieren“ 2 Wochen lang erneut anzeigen, indem Sie die Option im Dropdownmenü des Warnungsdialogfelds auswählen.

**Verwalten Sie Ihre Erweiterungen direkt über die Symbolleiste**. Mit dem Menü "Ganz neue Erweiterungen" auf der Symbolleiste können Sie Erweiterungen einfach ausblenden/anheften. Die Quicklinks zum Verwalten von Erweiterungen und zum Suchen neuer Erweiterungen erleichtern Ihnen das Auffinden neuer Erweiterungen und das Verwalten Ihrer vorhandenen Erweiterungen.

**Der Standardwert für die automatische Wiedergabe wird auf „Beschränken“ festgelegt**.  Um Ihnen zu helfen, online konzentriert zu bleiben, haben wir ab Microsoft Edge Version 92 die Standardeinstellung für die automatische Wiedergabe von Medien von "Zulassen" zu "Beschränkt" geändert.

**Zahlungsmethoden werden jetzt geräteübergreifend synchronisiert**. Ab Microsoft Edge Version 92 haben Sie die Möglichkeit, Ihre Zahlungsinformationen zwischen Geräten, auf denen Sie angemeldet sind, zu synchronisieren. Bitte beachten Sie: Hierbei handelt es sich um ein gesteuertes Feature-Rollout. Sollte das Feature nicht angezeigt werden, sehen Sie bitte in Kürze wieder nach, da das Rollout noch läuft.
Dieses Feature ist derzeit nur in den USA und nur für MSA-Benutzer (nicht AAD) verfügbar.

**Verbesserungen am Rendering von Schriftarten**. Das Rendering von Text wurde verbessert, um die Deutlichkeit zu verbessern und die Unschärfe zu verringern. Bitte beachten Sie: Hierbei handelt es sich um ein gesteuertes Feature-Rollout. Sollte das Feature nicht angezeigt werden, sehen Sie bitte in Kürze wieder nach, da das Rollout noch läuft.

**Schaltflächenfeatures der Symbolleiste wie Favoriten und Sammlungen "merken“ sich, dass der Benutzer sie an die Seite des Fensters angeheftet hat.** Wenn der Benutzer eine Symbolleistenschaltfläche anheftet, ist jetzt standardmäßig aktiviert, dass sie so lange im angehefteten Zustand geöffnet wird, bis er die Anheftung wieder aufhebt.

**Benutzer können jetzt die Option "Einmaliges Anmelden für Geschäfts-, Schul- oder Uniwebsites mit diesem Profil zulassen" über Gruppenrichtlinien verwalten.**  Die Option "Einmaliges Anmelden für Geschäfts-, Uni- oder Schulwebsites mit diesem Profil zulassen" ermöglicht Nicht-AAD-Profilen die Verwendung von einmaligem Anmelden für Geschäfts-, Uni- oder Schulwebsites mit den auf dem Computer vorhandenen Geschäfts-, Uni- oder Schulanmeldeinformationen. Diese Option wird Endbenutzern als Umschalter unter Einstellungen -> Profile -> Profileinstellungen nur für Nicht-AAD-Profile angezeigt.  Mithilfe der [AADWebSiteSSOUsingThisProfileEnabled](/deployedge/microsoft-edge-policies#aadwebsitessousingthisprofileenabled)-Richtlinie können Sie das Verhalten konfigurieren.  

**Kennwortintegrität**: Es ist wichtig, sichere, eindeutige Kennwörter für verschiedene Konten zu verwenden, um online sicher zu bleiben. Dies ist jedoch einfacher gesagt als getan, und die meisten Benutzer weisen schlechte Kennwortgewohnheiten auf wie die Verwendung schwacher Kennwörter, die leicht erraten werden können, oder die Verwendung der selben sicheren Kennwörter für alle Konten.

Mit dieser neuesten Version von Microsoft Edge wird Ihre Aufgabe, sichere und eindeutige Kennwörter zu verwenden, etwas einfacher! Microsoft Edge informiert Sie nun darüber, ob gespeicherte Kennwörter sicher genug sind, und gibt außerdem an, ob sie auf mehreren Websites verwendet wurden, was Ihnen hilft, online sicherer zu bleiben. Die Informationen zum Status Ihrer Kennwörter finden Sie in der Liste der gespeicherten Kennwörter auf der Seite edge://settings/passwords.
  
**Datenschutz für Ihre gespeicherten Kennwörter hinzugefügt**: Wenn Sie ein Gerät verwenden, das auch von anderen Personen benutzt wird, oder Ihr Computer aus irgendeinem Grund entsperrt geblieben ist, können Sie sich jetzt für eine zweite Überprüfung mit Ihrem Gerätekennwort entscheiden, um zu verhindern, dass andere Zugriff auf Ihre Websitekennwörter erhalten. Einfach!

**Outlook Erweiterung**:  Bleiben Sie über Microsoft Outlook-Posteingang, Kalender, Aufgaben und mehr auf dem Laufenden, ohne ein neues Browserfenster öffnen zu müssen.  Sie können die neue Outlook-Erweiterung hier beziehen: [Microsoft Outlook – Microsoft Edge-Add-Ons](https://microsoftedge.microsoft.com/addons/detail/microsoft-outlook/kkpalkknhlklpbflpcpkepmmbnmfailf?hl=en-US)

**In Übereinstimmung mit dem Chromium-Open-Source-Projekt aktualisiert Microsoft Edge die Art und Weise, wie Tabellen auf Webseiten gerendert werden.** Diese Änderung behebt bekannte Probleme und bringt Microsoft Edge näher an die angegebene Art und Weise, wie Tabellen im Web/in anderen Browsern gerendert werden sollen. Es wird empfohlen, dass Sie wichtige Workflows in Ihrer Umgebung auf unerwartete Probleme testen. Eine vollständige Erläuterung finden Sie [hier.](https://docs.google.com/document/d/16PFD1GtMI9Zgwu0jtPaKZJ75Q2wyZ9EZnVbBacOfiNA/edit)

### <a name="new-policies"></a>Neue Richtlinien

- [AADWebSiteSSOUsingThisProfileEnabled](/DeployEdge/microsoft-edge-policies#aadwebsitessousingthisprofileenabled): Einmaliges Anmelden mit diesem Profil für Arbeits-, Schul- oder Uniwebsites aktiviert
- [AutomaticHttpsDefault](/DeployEdge/microsoft-edge-policies#automatichttpsdefault): Automatisches HTTPS konfigurieren
- [HeadlessModeEnabled](/DeployEdge/microsoft-edge-policies#headlessmodeenabled): Steuern der Verwendung des Headless-Modus
- [InsecurePrivateNetworkRequestsAllowed](/DeployEdge/microsoft-edge-policies#insecureprivatenetworkrequestsallowed) Gibt an, ob unsichere Websites Anforderungen an privatere Netzwerkendpunkte stellen dürfen.
- [InsecurePrivateNetworkRequestsAllowedForUrls](/DeployEdge/microsoft-edge-policies#insecureprivatenetworkrequestsallowedforurls): Zulassen, dass die aufgeführten Websites Anforderungen an privatere Netzwerkendpunkte aus unsicheren Kontexten stellen
- [InternetExplorerIntegrationLocalSiteListExpirationDays](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationlocalsitelistexpirationdays): Angeben der Anzahl der Tage, die eine Website in der lokalen Websiteliste für den IE-Modus verbleibt
- [InternetExplorerIntegrationReloadInIEModeAllowed](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationreloadiniemodeallowed): Zulassen, dass nicht konfigurierte Websites im Internet Explorer-Modus neu geladen werden
- [SharedArrayBufferUnrestrictedAccessAllowed](/DeployEdge/microsoft-edge-policies#sharedarraybufferunrestrictedaccessallowed): Gibt an, ob SharedArrayBuffers in einem nicht ursprungsübergreifenden isolierten Kontext verwendet werden können.

### <a name="deprecated-policy"></a>Veraltete Richtlinie

- [InternetExplorerIntegrationTestingAllowed](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationtestingallowed): Zulassen von Internet Explorer-Modustests

### <a name="obsoleted-policy"></a>Veraltete Richtlinie

- [EnableSha1ForLocalAnchors](/DeployEdge/microsoft-edge-policies#enablesha1forlocalanchors): Zulassen von Zertifikaten, die mit SHA-1 signiert wurden, wenn sie von lokalen Vertrauensanker ausgestellt wurden.

## <a name="version-91086471-july-19"></a>Version 91.0.864.71: 19. Juli

> [!Important]
>Dieses Update enthält einen Fix für [CVE-2021-30563,](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-30563) der vom Chromium-Team als Exploit gemeldet wurde. Weitere Informationen finden Sie im [Leitfaden zu Sicherheitsupdates](https://msrc.microsoft.com/update-guide/vulnerability/ADV200002).

Stable Channel-Sicherheitsupdates sind [hier](/deployedge/microsoft-edge-relnotes-security#july-19-2021) aufgeführt.

## <a name="version-91086467-july-8"></a>Version 91.0.864.67: 8. Juli

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-91086464-july-2"></a>Version 91.0.864.64: 2. Juli

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-91086459-june-24"></a>Version 91.0.864.59: 24. Juni

Sicherheitsupdates im Stabilen Kanal sind [hier](/deployedge/microsoft-edge-relnotes-security#june-24-2021) aufgeführt.

## <a name="version-91086454-june-18"></a>Version 91.0.864.54: 18. Juni

> [!Important]
> Dieses Update enthält einen Fix für [CVE-2021-30554,](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-30554) der vom Chromium-Team als Exploit gemeldet wurde. Weitere Informationen finden Sie im [Leitfaden zu Sicherheitsupdates](https://msrc.microsoft.com/update-guide/vulnerability/ADV200002).

Sicherheitsupdates im Stabilen Kanal sind [hier](/deployedge/microsoft-edge-relnotes-security#june-18-2021) aufgeführt.

## <a name="version-91086448-june-11"></a>Version 91.0.864.48: 11. Juni

> [!Important]
>Dieses Update enthält einen Fix für [CVE-2021-30551,](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-30551) der vom Chromium-Team als Exploit gemeldet wurde. Weitere Informationen finden Sie im [Leitfaden zu Sicherheitsupdates](https://msrc.microsoft.com/update-guide/vulnerability/ADV200002).

Sicherheitsupdates im Stabilen Kanal sind [hier](/deployedge/microsoft-edge-relnotes-security#june-11-2021) aufgeführt.

## <a name="version-91086441-june-3"></a>Version 91.0.864.41: 3. Juni

Sicherheitsupdates im Stabilen Kanal sind [hier](/deployedge/microsoft-edge-relnotes-security#june-3-2021) aufgeführt.

## <a name="version-91086437-may-27"></a>Version 91.0.864.37: 27. Mai

Sicherheitsupdates im Stabilen Kanal sind [hier](/deployedge/microsoft-edge-relnotes-security#may-27-2021) aufgeführt.

### <a name="feature-updates"></a>Funktionsupdates

- **Identifizieren Sie den Netzwerkdatenverkehr von Microsoft Defender Application Guard-Containern auf Proxyebene**. Ab Microsoft Edge Version 91 gibt es integrierte Unterstützung zum Markieren von Netzwerkdatenverkehr von Application Guard-Containern, sodass Unternehmen diese identifizieren und bestimmte Richtlinien anwenden können.

- **Unterstützungsoption, um die Synchronisierung von Favoriten vom Host mit dem Microsoft Edge Application Guard-Container zuzulassen**. Ab Microsoft Edge Version 91 haben Benutzer die Möglichkeit, Application Guard so zu konfigurieren, dass ihre Favoriten vom Host mit dem Container synchronisiert werden. Dadurch wird sichergestellt, dass auch neue Favoriten im Container angezeigt werden.

- **Ab Microsoft Edge Version 91 wird der Download von Typen, die Ihrem Computer schaden könnten, vom Browser automatisch unterbrochen, wenn diese Downloads ohne Benutzerinteraktion gestartet werden und von der Überprüfung der SmartScreen-Anwendungszuverlässigkeit nicht unterstützt werden.** Benutzer können den Download überschreiben und fortsetzen, indem sie mit der rechten Maustaste auf das Downloadelement klicken und „Beibehalten“ auswählen. Unternehmensadministratoren können dieses Verhalten deaktivieren, indem sie die folgende Richtlinie konfigurieren:
  - [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](/deployedge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings.md): Deaktivieren von auf Dateierweiterungen basierenden Download-Warnungen für bestimmte Dateitypen in Domänen.

    Weitere Informationen finden Sie unter [Unterbrechung von Microsoft Edge-Sicherheitsdownloads](microsoft-edge-security-downloads-interruptions.md).

- **Unterstützung für Spracherkennungs-APIs**. Ab Microsoft Edge Version 91 wird die API-Unterstützung für Spracherkennungsbefehle auf Google.com und ähnlichen Websites hinzugefügt. Diese Funktion ist auf eine zufällig ausgewählte Gruppe von Benutzern beschränkt, die das Experimentieren aktiviert haben. Diese Benutzer geben dem Feature-Team Feedback.

- **Personalisieren Sie Ihren Browser mit neuen Designfarben.**. Personalisieren Sie Ihr Microsoft Edge mit einer der 14 neuen Designfarben auf der Seite „Einstellungen“ > „Darstellung“. Sie können auch benutzerdefinierte Designs von der Microsoft Edge-Add-On-Website installieren. [Weitere Informationen](https://techcommunity.microsoft.com/t5/articles/make-microsoft-edge-your-own-with-themes/m-p/2083165)

### <a name="policy-updates"></a>Richtlinienupdates

#### <a name="new-policies"></a>Neue Richtlinien

Sechs neue Richtlinien wurden hinzugefügt. Laden Sie die aktualisierten administrativen Vorlagen von der [Microsoft Edge Enterprise-Angebotsseite](https://www.microsoft.com/edge/business/download) herunter. Die folgenden neuen Richtlinien wurden hinzugefügt:

- [ApplicationGuardTrafficIdentificationEnabled](/DeployEdge/microsoft-edge-policies#applicationguardtrafficidentificationenabled) – Application Guard-Netzwerkdatenverkehrsidentifikation
- [ExplicitlyAllowedNetworkPorts](/DeployEdge/microsoft-edge-policies#explicitlyallowednetworkports) – Explizit zugelassene Netzwerkports
- [ImportStartupPageSettings](/DeployEdge/microsoft-edge-policies#importstartuppagesettings) – Import von Startseiteneinstellungen zulassen
- [MathSolverEnabled](/DeployEdge/microsoft-edge-policies#mathsolverenabled) – Benutzer können ein mathematisches Problem mit einer schrittweisen Erläuterung in Microsoft Edge lösen
- [NewTabPageContentEnabled](/DeployEdge/microsoft-edge-policies#newtabpagecontentenabled) – Microsoft News-Inhalt auf der neuen Registerkartenseite zulassen
- [NewTabPageQuickLinksEnabled](/DeployEdge/microsoft-edge-policies#newtabpagequicklinksenabled) – Quicklinks auf der neuen Registerkartenseite zulassen

#### <a name="obsoleted-policy"></a>Veraltete Richtlinie

- [ProactiveAuthEnabled](./microsoft-edge-policies.md#proactiveauthenabled) – Proaktive Authentifizierung aktivieren
<!-- end major 91 -->

<!-- Archive from 89.0.774.45: March 4 to 90.0.818.66: May 20 ->
<!-- Archive from 86.0.622.43: October 15 to beta 88.0.705.81: February 25  ->
<!-- Archive from 86.0.622.38-october-9 to beta 86.0.62.215-september-14  ->
<!-- Archived to version 84.0.522.40: July 16 -->

## <a name="see-also"></a>Weitere Informationen

- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)
