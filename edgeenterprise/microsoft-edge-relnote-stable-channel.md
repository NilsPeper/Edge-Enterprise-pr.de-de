---
title: Versionshinweise von Microsoft Edge für Stable Channel
ms.author: aguta
author: AndreaLBarr
manager: srugh
ms.date: 09/09/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Versionshinweise von Microsoft Edge für Stable Channel
ms.openlocfilehash: e13778ee9a93a4621ad77a00da1d85def3f97225
ms.sourcegitcommit: 6eefb7cb134f25a1e2d1f515a3a8600524a4b6e3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2021
ms.locfileid: "12017969"
---
# <a name="release-notes-for-microsoft-edge-stable-channel"></a>Versionshinweise für Microsoft Edge Stable Channel

Diese Versionshinweise enthalten Informationen zu neuen Funktionen und nicht sicherheitsrelevanten Updates, die im Microsoft Edge Stable Channel enthalten sind.

- Alle Sicherheitsupdates werden [hier](microsoft-edge-relnotes-security.md) aufgelistet.
- Archivierte Versionshinweise für Microsoft Edge Stable Channel finden Sie [hier.](microsoft-edge-relnote-archive-stable-channel.md)

 Informationen zu Microsoft Edge-Kanälen finden Sie in der [Übersicht über die Microsoft Edge-Kanäle](microsoft-edge-channels.md).

> [!NOTE]
> Für den Stable Channel erfolgt das Rollout von Updates progressiv über einen oder mehrere Tage. Weitere Informationen hierzu finden Sie unter [Progressive Rollouts für Microsoft Edge-Updates](microsoft-edge-update-progressive-rollout.md).
>
> Die Microsoft Edge-Webplattform entwickelt sich ständig weiter, um Benutzerfreundlichkeit, Sicherheit und Datenschutz zu verbessern. Weitere Informationen finden Sie unter [Änderungen mit Auswirkungen auf die Websitekompatibilität für Microsoft Edge](/microsoft-edge/web-platform/site-impacting-changes).

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

- 
            [AutoplayAllowlist](/DeployEdge/microsoft-edge-policies#autoplayallowlist) Zulassen der automatischen Medienwiedergabe auf bestimmten Websites
- 
            [CECPQ2Enabled](/DeployEdge/microsoft-edge-policies#cecpq2enabled) CECPQ2 Post Quantum Key Agreement für TLS aktiviert
- 
            [ConfigureViewInFileExplorer](/DeployEdge/microsoft-edge-policies#configureviewinfileexplorer) Konfigurieren des Features „Im Datei-Explorer anzeigen“ für SharePoint-Seiten in Microsoft Edge
- 
            [DefaultJavaScriptJitSetting](/DeployEdge/microsoft-edge-policies#defaultjavascriptjitsetting) Steuern der Verwendung von JavaScript-JIT
- 
            [ShowPDFDefaultRecommendationsEnabled](/DeployEdge/microsoft-edge-policies#showpdfdefaultrecommendationsenabled) Zulassen von Benachrichtigungen zum Festlegen von Microsoft Edge als standardmäßigen PDF-Reader
- 
            [FeatureFlagOverridesControl](/DeployEdge/microsoft-edge-policies#featureflagoverridescontrol) Konfigurieren der Möglichkeit von Benutzern, Featurekennzeichnungen außer Kraft zu setzen
- 
            [ImplicitSignInEnabled](/DeployEdge/microsoft-edge-policies#implicitsigninenabled) Aktivieren der impliziten Anmeldung
- 
            [InternetExplorerIntegrationCloudSiteList](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationcloudsitelist) Konfigurieren der Unternehmensmodus-Cloudwebsiteliste
- 
            [InternetExplorerIntegrationSiteListRefreshInterval](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationsitelistrefreshinterval) Konfigurieren, wie häufig die Unternehmensmodus-Cloudwebsiteliste aktualisiert wird
- 
            [JavaScriptJitAllowedForSites](/DeployEdge/microsoft-edge-policies#javascriptjitallowedforsites) Zulassen, dass JavaScript JIT auf diesen Websites verwendet
- 
            [JavaScriptJitBlockedForSites](/DeployEdge/microsoft-edge-policies#javascriptjitblockedforsites) Blockieren der Verwendung von JIT in JavaScript auf diesen Websites
- 
            [LocalBrowserDataShareEnabled](/DeployEdge/microsoft-edge-policies#localbrowserdatashareenabled) Zulassen, dass Windows lokale Microsoft Edge-Browserdaten durchsucht
- 
            [MAUEnabled](/DeployEdge/microsoft-edge-policies#mauenabled) Microsoft AutoUpdate immer als Updater für Microsoft Edge verwenden
- 
            [MSAWebSiteSSOUsingThisProfileAllowed](/DeployEdge/microsoft-edge-policies#msawebsitessousingthisprofileallowed) Anmelden für Microsoft-Websites mit diesem Profil zulassen
- 
            [OneAuthAuthenticationEnforced](/DeployEdge/microsoft-edge-policies#oneauthauthenticationenforced) Erzwungener OneAuth-Authentifizierungsablauf für die Anmeldung
- 
            [PasswordGeneratorEnabled](/DeployEdge/microsoft-edge-policies#passwordgeneratorenabled) Zulassen, dass Benutzer einen Vorschlag für sichere Kennwörter erhalten, wenn sie ein Konto online erstellen
- 
            [PrimaryPasswordSetting](/DeployEdge/microsoft-edge-policies#primarypasswordsetting) Konfiguriert eine Einstellung, die Benutzer auffordert, ihr Gerätekennwort einzugeben bei Verwendung des automatischen Ausfüllens von Kennwörtern
- 
            [PrintingWebpageLayout](/DeployEdge/microsoft-edge-policies#printingwebpagelayout) Legt das Layout für das Drucken fest
- 
            [RemoteDebuggingAllowed](/DeployEdge/microsoft-edge-policies#remotedebuggingallowed) Zulassen des Remotedebuggings
- 
            [RelaunchWindow](/DeployEdge/microsoft-edge-policies#relaunchwindow) Festlegen des Zeitintervalls für den Neustart
- 
            [TravelAssistanceEnabled](/DeployEdge/microsoft-edge-policies#travelassistanceenabled) Aktivieren der Reiseunterstützung
- 
            [TripleDESEnabled](/DeployEdge/microsoft-edge-policies#tripledesenabled) Aktivieren von 3DES-Verschlüsselungssammlungen in TLS
- 
            [WAMAuthBelowWin10RS3Enabled](/DeployEdge/microsoft-edge-policies#wamauthbelowwin10rs3enabled) WAM für die Authentifizierung unter Windows 10 WAMAuthBelowWin10RS3Enabled aktiviert

***Veraltete Richtlinie***

- 
            [LegacySameSiteCookieBehaviorEnabled](/DeployEdge/microsoft-edge-policies#legacysamesitecookiebehaviorenabled) Aktivieren der Standardeinstellung für das Verhalten von Legacy-SameSite-Cookies

***Veraltete Richtlinie***

- 
            [NewTabPageSetFeedType](/DeployEdge/microsoft-edge-policies#newtabpagesetfeedtype) Konfigurieren der Microsoft Edge-Oberfläche für neue Registerkartenseiten

***Zusätzliche Änderung***

- 
            [ConfigureShare](/DeployEdge/microsoft-edge-policies#configureshare) Hinzufügen der Mac-Plattformunterstützung
- 
            [PasswordMonitorAllowed](/DeployEdge/microsoft-edge-policies#passwordmonitorallowed) Hinzufügen der Mac-Plattformunterstützung


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


            **MHTML-Dateien werden standardmäßig im Internet Explorer-Modus geöffnet**. Ab Microsoft Edge Version 92 Stable werden MHTML-Dateitypen automatisch im Internet Explorer-Modus auf Microsoft Edge anstelle der Internet Explorer-Anwendung (IE11) geöffnet. Dies wird am häufigsten beim Versuch beobachtet, Outlook-E-Mails in einem Browser anzuzeigen. Diese Änderung tritt nur auf, wenn IE11 der Standardhandler für diesen Dateityp ist. Wenn Sie dies lieber ändern möchten, können Sie dies vor der Installation des Stable Version 92-Updates mithilfe [dieser Anleitung](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration) tun.


            **Die Warnung „Entwicklermoduserweiterungen deaktivieren“ kann zwei Wochen lang geschlossen werden.** 
           Ab Microsoft Edge Version 92 können Sie die Warnung „Entwicklermoduserweiterungen deaktivieren“ 2 Wochen lang erneut anzeigen, indem Sie die Option im Dropdownmenü des Warnungsdialogfelds auswählen.


            **Verwalten Sie Ihre Erweiterungen direkt über die Symbolleiste**. Mit dem Menü "Ganz neue Erweiterungen" auf der Symbolleiste können Sie Erweiterungen einfach ausblenden/anheften. Die Quicklinks zum Verwalten von Erweiterungen und zum Suchen neuer Erweiterungen erleichtern Ihnen das Auffinden neuer Erweiterungen und das Verwalten Ihrer vorhandenen Erweiterungen.


            **Der Standardwert für die automatische Wiedergabe wird auf „Beschränken“ festgelegt**.  Um Ihnen zu helfen, online konzentriert zu bleiben, haben wir ab Microsoft Edge Version 92 die Standardeinstellung für die automatische Wiedergabe von Medien von "Zulassen" zu "Beschränkt" geändert.


            **Zahlungsmethoden werden jetzt geräteübergreifend synchronisiert**. Ab Microsoft Edge Version 92 haben Sie die Möglichkeit, Ihre Zahlungsinformationen zwischen Geräten, auf denen Sie angemeldet sind, zu synchronisieren. Bitte beachten Sie: Hierbei handelt es sich um ein gesteuertes Feature-Rollout. Sollte das Feature nicht angezeigt werden, sehen Sie bitte in Kürze wieder nach, da das Rollout noch läuft.
Dieses Feature ist derzeit nur in den USA und nur für MSA-Benutzer (nicht AAD) verfügbar.


            **Verbesserungen am Rendering von Schriftarten**. Das Rendering von Text wurde verbessert, um die Deutlichkeit zu verbessern und die Unschärfe zu verringern. Bitte beachten Sie: Hierbei handelt es sich um ein gesteuertes Feature-Rollout. Sollte das Feature nicht angezeigt werden, sehen Sie bitte in Kürze wieder nach, da das Rollout noch läuft.


            **Schaltflächenfeatures der Symbolleiste wie Favoriten und Sammlungen "merken“ sich, dass der Benutzer sie an die Seite des Fensters angeheftet hat.** 
           Wenn der Benutzer eine Symbolleistenschaltfläche anheftet, ist jetzt standardmäßig aktiviert, dass sie so lange im angehefteten Zustand geöffnet wird, bis er die Anheftung wieder aufhebt.


            **Benutzer können jetzt die Option "Einmaliges Anmelden für Geschäfts-, Schul- oder Uniwebsites mit diesem Profil zulassen" über Gruppenrichtlinien verwalten.** 
            Die Option "Einmaliges Anmelden für Geschäfts-, Uni- oder Schulwebsites mit diesem Profil zulassen" ermöglicht Nicht-AAD-Profilen die Verwendung von einmaligem Anmelden für Geschäfts-, Uni- oder Schulwebsites mit den auf dem Computer vorhandenen Geschäfts-, Uni- oder Schulanmeldeinformationen. Diese Option wird Endbenutzern als Umschalter unter Einstellungen -> Profile -> Profileinstellungen nur für Nicht-AAD-Profile angezeigt.  Mithilfe der [AADWebSiteSSOUsingThisProfileEnabled](/deployedge/microsoft-edge-policies#aadwebsitessousingthisprofileenabled)-Richtlinie können Sie das Verhalten konfigurieren.  


            **Kennwortintegrität**: Es ist wichtig, sichere, eindeutige Kennwörter für verschiedene Konten zu verwenden, um online sicher zu bleiben. Dies ist jedoch einfacher gesagt als getan, und die meisten Benutzer weisen schlechte Kennwortgewohnheiten auf wie die Verwendung schwacher Kennwörter, die leicht erraten werden können, oder die Verwendung der selben sicheren Kennwörter für alle Konten.

Mit dieser neuesten Version von Microsoft Edge wird Ihre Aufgabe, sichere und eindeutige Kennwörter zu verwenden, etwas einfacher! Microsoft Edge informiert Sie nun darüber, ob gespeicherte Kennwörter sicher genug sind, und gibt außerdem an, ob sie auf mehreren Websites verwendet wurden, was Ihnen hilft, online sicherer zu bleiben. Die Informationen zum Status Ihrer Kennwörter finden Sie in der Liste der gespeicherten Kennwörter auf der Seite edge://settings/passwords.
  

            **Datenschutz für Ihre gespeicherten Kennwörter hinzugefügt**: Wenn Sie ein Gerät verwenden, das auch von anderen Personen benutzt wird, oder Ihr Computer aus irgendeinem Grund entsperrt geblieben ist, können Sie sich jetzt für eine zweite Überprüfung mit Ihrem Gerätekennwort entscheiden, um zu verhindern, dass andere Zugriff auf Ihre Websitekennwörter erhalten. Einfach!


            **Outlook Erweiterung**:  Bleiben Sie über Microsoft Outlook-Posteingang, Kalender, Aufgaben und mehr auf dem Laufenden, ohne ein neues Browserfenster öffnen zu müssen.  Sie können die neue Outlook-Erweiterung hier beziehen: [Microsoft Outlook – Microsoft Edge-Add-Ons](https://microsoftedge.microsoft.com/addons/detail/microsoft-outlook/kkpalkknhlklpbflpcpkepmmbnmfailf?hl=en-US)


            **In Übereinstimmung mit dem Chromium-Open-Source-Projekt aktualisiert Microsoft Edge die Art und Weise, wie Tabellen auf Webseiten gerendert werden.** 
           Diese Änderung behebt bekannte Probleme und bringt Microsoft Edge näher an die angegebene Art und Weise, wie Tabellen im Web/in anderen Browsern gerendert werden sollen. Es wird empfohlen, dass Sie wichtige Workflows in Ihrer Umgebung auf unerwartete Probleme testen. Eine vollständige Erläuterung finden Sie [hier.](https://docs.google.com/document/d/16PFD1GtMI9Zgwu0jtPaKZJ75Q2wyZ9EZnVbBacOfiNA/edit)

### <a name="new-policies"></a>Neue Richtlinien

- 
            [AADWebSiteSSOUsingThisProfileEnabled](/DeployEdge/microsoft-edge-policies#aadwebsitessousingthisprofileenabled): Einmaliges Anmelden mit diesem Profil für Arbeits-, Schul- oder Uniwebsites aktiviert
- 
            [AutomaticHttpsDefault](/DeployEdge/microsoft-edge-policies#automatichttpsdefault): Automatisches HTTPS konfigurieren
- 
            [HeadlessModeEnabled](/DeployEdge/microsoft-edge-policies#headlessmodeenabled): Steuern der Verwendung des Headless-Modus
- 
            [InsecurePrivateNetworkRequestsAllowed](/DeployEdge/microsoft-edge-policies#insecureprivatenetworkrequestsallowed) Gibt an, ob unsichere Websites Anforderungen an privatere Netzwerkendpunkte stellen dürfen.
- 
            [InsecurePrivateNetworkRequestsAllowedForUrls](/DeployEdge/microsoft-edge-policies#insecureprivatenetworkrequestsallowedforurls): Zulassen, dass die aufgeführten Websites Anforderungen an privatere Netzwerkendpunkte aus unsicheren Kontexten stellen
- 
            [InternetExplorerIntegrationLocalSiteListExpirationDays](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationlocalsitelistexpirationdays): Angeben der Anzahl der Tage, die eine Website in der lokalen Websiteliste für den IE-Modus verbleibt
- 
            [InternetExplorerIntegrationReloadInIEModeAllowed](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationreloadiniemodeallowed): Zulassen, dass nicht konfigurierte Websites im Internet Explorer-Modus neu geladen werden
- 
            [SharedArrayBufferUnrestrictedAccessAllowed](/DeployEdge/microsoft-edge-policies#sharedarraybufferunrestrictedaccessallowed): Gibt an, ob SharedArrayBuffers in einem nicht ursprungsübergreifenden isolierten Kontext verwendet werden können.

### <a name="deprecated-policy"></a>Veraltete Richtlinie

- 
            [InternetExplorerIntegrationTestingAllowed](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationtestingallowed): Zulassen von Internet Explorer-Modustests

### <a name="obsoleted-policy"></a>Veraltete Richtlinie

- 
            [EnableSha1ForLocalAnchors](/DeployEdge/microsoft-edge-policies#enablesha1forlocalanchors): Zulassen von Zertifikaten, die mit SHA-1 signiert wurden, wenn sie von lokalen Vertrauensanker ausgestellt wurden.

## <a name="version-91086471-july-19"></a>Version 91.0.864.71: 19. Juli

> [!Important]
>Dieses Update enthält [CVE-2021-30563](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-30563), für das laut Chromium-Team ein Exploit im Umlauf ist. Weitere Informationen finden Sie im [Leitfaden zu Sicherheitsupdates](https://msrc.microsoft.com/update-guide/vulnerability/ADV200002).

Stable Channel-Sicherheitsupdates sind [hier](/deployedge/microsoft-edge-relnotes-security#july-19-2021) aufgeführt.

## <a name="version-91086467-july-8"></a>Version 91.0.864.67: 8. Juli

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-91086464-july-2"></a>Version 91.0.864.64: 2. Juli

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-91086459-june-24"></a>Version 91.0.864.59: 24. Juni

Sicherheitsupdates im Stabilen Kanal sind [hier](/deployedge/microsoft-edge-relnotes-security#june-24-2021) aufgeführt.

## <a name="version-91086454-june-18"></a>Version 91.0.864.54: 18. Juni

> [!Important]
> Dieses Update enthält [CVE-2021-30554](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-30554), für das laut Chromium-Team ein Exploit im Umlauf ist. Weitere Informationen finden Sie im [Leitfaden für Sicherheitsupdates](https://msrc.microsoft.com/update-guide/vulnerability/ADV200002).

Sicherheitsupdates im Stabilen Kanal sind [hier](/deployedge/microsoft-edge-relnotes-security#june-18-2021) aufgeführt.

## <a name="version-91086448-june-11"></a>Version 91.0.864.48: 11. Juni

> [!Important]
>Dieses Update enthält [CVE-2021-30551](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-30551), für das laut Chromium-Team ein Exploit im Umlauf ist. Weitere Informationen finden Sie im [Leitfaden für Sicherheitsupdates](https://msrc.microsoft.com/update-guide/vulnerability/ADV200002).

Sicherheitsupdates im Stabilen Kanal sind [hier](/deployedge/microsoft-edge-relnotes-security#june-11-2021) aufgeführt.

## <a name="version-91086441-june-3"></a>Version 91.0.864.41: 3. Juni

Sicherheitsupdates im Stabilen Kanal sind [hier](/deployedge/microsoft-edge-relnotes-security#june-3-2021) aufgeführt.

## <a name="version-91086437-may-27"></a>Version 91.0.864.37: 27. Mai

Sicherheitsupdates im Stabilen Kanal sind [hier](/deployedge/microsoft-edge-relnotes-security#may-27-2021) aufgeführt.

### <a name="feature-updates"></a>Funktionsupdates

- 
            **Identifizieren Sie den Netzwerkdatenverkehr von Microsoft Defender Application Guard-Containern auf Proxyebene**. Ab Microsoft Edge Version 91 gibt es integrierte Unterstützung zum Markieren von Netzwerkdatenverkehr von Application Guard-Containern, sodass Unternehmen diese identifizieren und bestimmte Richtlinien anwenden können.

- 
            **Unterstützungsoption, um die Synchronisierung von Favoriten vom Host mit dem Microsoft Edge Application Guard-Container zuzulassen**. Ab Microsoft Edge Version 91 haben Benutzer die Möglichkeit, Application Guard so zu konfigurieren, dass ihre Favoriten vom Host mit dem Container synchronisiert werden. Dadurch wird sichergestellt, dass auch neue Favoriten im Container angezeigt werden.

- 
            **Ab Microsoft Edge Version 91 wird der Download von Typen, die Ihrem Computer schaden könnten, vom Browser automatisch unterbrochen, wenn diese Downloads ohne Benutzerinteraktion gestartet werden und von der Überprüfung der SmartScreen-Anwendungszuverlässigkeit nicht unterstützt werden.** 
           Benutzer können den Download überschreiben und fortsetzen, indem sie mit der rechten Maustaste auf das Downloadelement klicken und „Beibehalten“ auswählen. Unternehmensadministratoren können dieses Verhalten deaktivieren, indem sie die folgende Richtlinie konfigurieren:
  - 
            [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](/deployedge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings.md): Deaktivieren von auf Dateierweiterungen basierenden Download-Warnungen für bestimmte Dateitypen in Domänen.

    Weitere Informationen finden Sie unter [Unterbrechung von Microsoft Edge-Sicherheitsdownloads](microsoft-edge-security-downloads-interruptions.md).

- 
            **Unterstützung für Spracherkennungs-APIs**. Ab Microsoft Edge Version 91 wird die API-Unterstützung für Spracherkennungsbefehle auf Google.com und ähnlichen Websites hinzugefügt. Diese Funktion ist auf eine zufällig ausgewählte Gruppe von Benutzern beschränkt, die das Experimentieren aktiviert haben. Diese Benutzer geben dem Feature-Team Feedback.

- 
            **Personalisieren Sie Ihren Browser mit neuen Designfarben.**. Personalisieren Sie Ihr Microsoft Edge mit einer der 14 neuen Designfarben auf der Seite „Einstellungen“ > „Darstellung“. Sie können auch benutzerdefinierte Designs von der Microsoft Edge-Add-On-Website installieren. [Weitere Informationen](https://techcommunity.microsoft.com/t5/articles/make-microsoft-edge-your-own-with-themes/m-p/2083165)

### <a name="policy-updates"></a>Richtlinienupdates

#### <a name="new-policies"></a>Neue Richtlinien

Sechs neue Richtlinien wurden hinzugefügt. Laden Sie die aktualisierten administrativen Vorlagen von der [Microsoft Edge Enterprise-Angebotsseite](https://www.microsoft.com/edge/business/download) herunter. Die folgenden neuen Richtlinien wurden hinzugefügt:

- 
            [ApplicationGuardTrafficIdentificationEnabled](/DeployEdge/microsoft-edge-policies#applicationguardtrafficidentificationenabled) – Application Guard-Netzwerkdatenverkehrsidentifikation
- 
            [ExplicitlyAllowedNetworkPorts](/DeployEdge/microsoft-edge-policies#explicitlyallowednetworkports) – Explizit zugelassene Netzwerkports
- 
            [ImportStartupPageSettings](/DeployEdge/microsoft-edge-policies#importstartuppagesettings) – Import von Startseiteneinstellungen zulassen
- 
            [MathSolverEnabled](/DeployEdge/microsoft-edge-policies#mathsolverenabled) – Benutzer können ein mathematisches Problem mit einer schrittweisen Erläuterung in Microsoft Edge lösen
- 
            [NewTabPageContentEnabled](/DeployEdge/microsoft-edge-policies#newtabpagecontentenabled) – Microsoft News-Inhalt auf der neuen Registerkartenseite zulassen
- 
            [NewTabPageQuickLinksEnabled](/DeployEdge/microsoft-edge-policies#newtabpagequicklinksenabled) – Quicklinks auf der neuen Registerkartenseite zulassen

#### <a name="obsoleted-policy"></a>Veraltete Richtlinie

- 
            [ProactiveAuthEnabled](./microsoft-edge-policies.md#proactiveauthenabled) – Proaktive Authentifizierung aktivieren
<!-- end major 91 -->

## <a name="version-90081866-may-20"></a>Version 90.0.818.66: 20. Mai

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-90081862-may-13"></a>Version 90.0.818.62: 13. Mai

Sicherheitsupdates im Stabilen Kanal sind [hier](/deployedge/microsoft-edge-relnotes-security#may-13-2021) aufgeführt.

## <a name="version-90081856-may-6"></a>Version 90.0.818.56: 6. Mai

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-90081851-april-29"></a>Version 90.0.818.51: 29. April

Sicherheitsupdates im Stabilen Kanal sind [hier](/deployedge/microsoft-edge-relnotes-security#april-29-2021) aufgeführt.

## <a name="version-90081849-april-26"></a>Version 90.0.818.49: 26. April

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-90081846-april-22"></a>Version 90.0.818.46: 22. April ##

Sicherheitsupdates im Stabilen Kanal sind [hier](/deployedge/microsoft-edge-relnotes-security#april-22-2021) aufgeführt.

## <a name="version-90081842-april-19"></a>Version 90.0.818.42: 19. April

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-90081841-april-16"></a>Version 90.0.818.41: 16. April ##

> [!Important]
>Dieses Update enthält [CVE-2021-21224](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21224), für das laut Chromium-Team ein Exploit im Umlauf ist. Weitere Informationen finden Sie im [Leitfaden für Sicherheitsupdates](https://msrc.microsoft.com/update-guide).

Sicherheitsupdates im Stabilen Kanal sind [hier](/deployedge/microsoft-edge-relnotes-security#april-16-2021) aufgeführt.

## <a name="version-90081839-april-15"></a>Version 90.0.818.39: 15. April ##

Sicherheitsupdates im Stabilen Kanal sind [hier](/deployedge/microsoft-edge-relnotes-security#april-15-2021) aufgeführt.

## <a name="feature-updates"></a>Funktionsupdates ##

-    **Einmaliges Anmelden (Single Sign On, SSO) ist jetzt für Azure Active Directory (Azure AD)-Konten und Microsoft-Konten (MSA) unter macOS verfügbar.** Ein bei Microsoft Edge unter macOS angemeldeter Benutzer wird nun automatisch bei Websites angemeldet, die so konfiguriert sind, dass eine einmalige Anmeldung mit Arbeits- und Microsoft-Konten möglich ist (z. B. bing.com, office.com, msn.com und outlook.com).

- **Kioskmodus.** Ab Microsoft Edge Version 90 wurden die Druckeinstellungen der Benutzeroberfläche gesperrt, und es werden nur noch die konfigurierten Drucker und „In PDF drucken“-Optionen zugelassen. Wir haben außerdem Verbesserungen am Kioskmodus für den zugewiesenen Zugriff für nur eine App vorgenommen, um das Starten anderer Anwendungen über den Browser einzuschränken. Weitere Informationen zu den Features des Kioskmodus finden Sie [hier](/deployedge/microsoft-edge-configure-kiosk-mode#kiosk-mode-supported-features).

- 
            **Downloads unterbrechen** Ab Microsoft Edge Version 91 wird der Download von Typen, die Ihrem Computer schaden könnten, vom Browser automatisch unterbrochen, wenn diese Downloads ohne Benutzerinteraktion gestartet werden und von der SmartScreen-Anwendungszuverlässigkeitsüberprüfung nicht unterstützt werden. Benutzer können den Download überschreiben und fortsetzen, indem sie mit der rechten Maustaste auf das Downloadelement klicken und „Beibehalten“ auswählen.
Unternehmensadministratoren können dieses Verhalten mit einer der folgenden beiden Richtlinien deaktivieren:
- 
            [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](/deployedge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings): Deaktivieren von auf Dateierweiterungen basierenden Download-Warnungen für bestimmte Dateitypen in Domänen. Weitere Informationen finden Sie unter [Unterbrechung von Microsoft Edge-Sicherheitsdownloads](/deployedge/microsoft-edge-security-downloads-interruptions)

- 
            **Drucken**:

    - **Neuer Druckrasterungsmodus für Nicht-PostScript-Drucker.** Ab Microsoft Edge Version 90 können Administratoren mithilfe einer neuen Richtlinie den Druckrasterungsmodus für ihre Benutzer definieren. Diese Richtlinie steuert, wie Microsoft Edge unter Windows auf Nicht-PostScript-Druckern druckt. Manchmal müssen Druckaufträge bei Nicht-PostScript-Druckern gerastert werden, damit korrekt gedruckt wird. Die Druckoptionen sind „Full" (Vollständig) und „Fast“ (Schnell).
    
  - **Zusätzliche Optionen für die Seitenskalierung beim Drucken.** Benutzer können jetzt die Skalierung anpassen, während sie Webseiten und PDF-Dokumente mit zusätzlichen Optionen drucken. Die Option „An Seite anpassen" stellt sicher, dass die Webseite oder das Dokument in den Bereich passt, der im ausgewählten „Papierformat" zum Drucken verfügbar ist. Die Option "Tatsächliche Größe" stellt sicher, dass sich die Größe des zu druckenden Inhalts unabhängig von der ausgewählten "Papiergröße" nicht ändert.

-   **Produktivität:**

    -   **Vorschläge zum automatischen Ausfüllen werden um den Inhalt von Adressfeldern aus der Zwischenablage erweitert.** Der Inhalt der Zwischenablage wird analysiert, wenn Sie auf ein Profil-/Adressfeld (z. B. Telefon, E-Mail, Postleitzahl, Stadt, Bundesland usw.) klicken, um es als Vorschläge zum automatischen Ausfüllen anzuzeigen.

    -   **Benutzer können nach Vorschlägen zum automatischen Ausfüllen suchen, auch wenn ein Formular oder Feld nicht erkannt wird.** Wenn Sie Ihre Informationen heute in Microsoft Edge gespeichert haben, werden automatisch Vorschläge zum automatischen Ausfüllen angezeigt, mit denen Sie beim Ausfüllen von Formularen Zeit sparen können. In Fällen, in denen beim automatischen Ausfüllen ein Formular fehlt oder wenn Sie Daten in Formularen abrufen möchten, die normalerweise nicht automatisch ausgefüllt sind (z. B. temporäre Formulare), können Sie mithilfe des automatischen Ausfüllens nach Ihren Informationen suchen.

-   **Greifen Sie über ein Flyout in der Menüleiste auf Downloads zu.** Downloads werden in der oberen rechten Ecke mit allen aktiven Downloads an einem Ort angezeigt. Dieses Menü ist leicht zu schließen, sodass Benutzer ununterbrochen weiter surfen und den gesamten Download-Fortschritt direkt über die Symbolleiste überwachen können. 
            [Weitere Informationen](https://techcommunity.microsoft.com/t5/articles/introducing-the-new-downloads-experience/m-p/2111551).

-   **Verbesserungen beim Rendern von Schriftarten.** Ab Microsoft Edge Version 90 haben wir das Rendern von Text verbessert, um die Klarheit zu verbessern und Unschärfe zu reduzieren. Ein Teil der Verbesserungen beim Rendern von Schriftarten wird in der Beta-Version 90 landen, ist jedoch standardmäßig deaktiviert.

- **Kindermodus.** Wir haben die Richtlinie so aktualisiert, dass bei Aktivierung der Richtlinie nicht nur die Familiensicherheit, sondern auch das Feature „Kindermodus“ deaktiviert wird. Weitere Informationen zum Kindermodus finden Sie [hier](https://go.microsoft.com/fwlink/?linkid=2146910)

## <a name="policy-updates"></a>Richtlinienupdates

## <a name="new-policies"></a>Neue Richtlinien

Acht neue Richtlinien wurden hinzugefügt. Laden Sie die aktualisierten administrativen Vorlagen von der [Microsoft Edge Enterprise-Angebotsseite](https://www.microsoft.com/edge/business/download) herunter. Die folgenden neuen Richtlinien wurden hinzugefügt:
-   
            [ApplicationGuardFavoritesSyncEnabled](/DeployEdge/microsoft-edge-policies#applicationguardfavoritessyncenabled) – Synchronisierung von Application Guard-Favoriten aktiviert
- 
            [ApplicationGuardTrafficIdentificationEnabled](/DeployEdge/microsoft-edge-policies#applicationguardtrafficidentificationenabled) – Application Guard-Netzwerkdatenverkehrsidentifikation
- 
            [ExplicitlyAllowedNetworkPorts](/DeployEdge/microsoft-edge-policies#explicitlyallowednetworkports) – Explizit zugelassene Netzwerkports
- 
            [ImportStartupPageSettings](/DeployEdge/microsoft-edge-policies#importstartuppagesettings) – Import von Startseiteneinstellungen zulassen
- 
            [MathSolverEnabled](/DeployEdge/microsoft-edge-policies#mathsolverenabled) – Benutzer können ein mathematisches Problem mit einer schrittweisen Erläuterung in Microsoft Edge lösen
- 
            [NewTabPageContentEnabled](/DeployEdge/microsoft-edge-policies#newtabpagecontentenabled) – Microsoft News-Inhalt auf der neuen Registerkartenseite zulassen
- 
            [NewTabPageQuickLinksEnabled](/DeployEdge/microsoft-edge-policies#newtabpagequicklinksenabled) – Quicklinks auf der neuen Registerkartenseite zulassen
-   
            [FetchKeepaliveDurationSecondsOnShutdown](/DeployEdge/microsoft-edge-policies#fetchkeepalivedurationsecondsonshutdown) – Keepalive-Dauer beim Herunterfahren abrufen
-   
            [ManagedConfigurationPerOrigin](/DeployEdge/microsoft-edge-policies#managedconfigurationperorigin) – Legt verwaltete Konfigurationswerte für Websites auf bestimmte Ursprünge fest
-   
            [PrintRasterizationMode](/DeployEdge/microsoft-edge-policies#printrasterizationmode) – Druckrasterungsmodus
-   
            [QuickViewOfficeFilesEnabled](/DeployEdge/microsoft-edge-policies#quickviewofficefilesenabled) : Verwalten der QuickView Office-Dateifunktion in Microsoft Edge
-   
            [SSLErrorOverrideAllowedForOrigins](/DeployEdge/microsoft-edge-policies#sslerroroverrideallowedfororigins) – Benutzer können von der HTTPS-Warnseite für bestimmte Ursprünge fortfahren
-   
            [WindowOcclusionEnabled](/DeployEdge/microsoft-edge-policies#windowocclusionenabled) – Fester-Okklusion aktivieren
-   
            [WindowsHelloForHTTPAuthEnabled](/DeployEdge/microsoft-edge-policies#windowshelloforhttpauthenabled) – Windows Hello für HTTP-Authentifizierung aktiviert

## <a name="deprecated-policies"></a>Veraltete Richtlinien

- 
            [ProactiveAuthEnabled](/DeployEdge/microsoft-edge-policies#proactiveauthenabled) – Proaktive Authentifizierung aktivieren
-   
            [NativeWindowOcclusionEnabled](/DeployEdge/microsoft-edge-policies#nativewindowocclusionenabled) – Native Fenster-Okklusion aktivieren
-   
            [SSLVersionMin](/DeployEdge/microsoft-edge-policies#sslversionmin)– Mindestens aktivierte TLS-Version

## <a name="version-89077477-april-14"></a>Version 89.0.774.77: 14. April

> [!Important]
>Dieses Update enthält [CVE-2021-21206](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21206) und [CVE-2021-21220](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21220), für das laut Chromium-Team ein Exploit im Umlauf ist.  Weitere Informationen finden Sie im [Leitfaden für Sicherheitsupdates](https://msrc.microsoft.com/update-guide).

Sicherheitsupdates im Stabilen Kanal sind [hier](/deployedge/microsoft-edge-relnotes-security#april-14-2021) aufgeführt.

## <a name="version-89077476-april-12"></a>Version 89.0.774.76: 12. April

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-89077475-april-8"></a>Version 89.0.774.75: 8. April

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-89077468-april-1"></a>Version 89.0.774.68 vom 1. April

Sicherheitsupdates im Stabilen Kanal sind [hier](./microsoft-edge-relnotes-security.md#april-1-2021) aufgeführt.

## <a name="version-89077463-march-25"></a>Version 89.0.774.63 vom 25. März

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-89077457-march-18"></a>Version 89.0.774.57: 18. März

Verschiedene Bugs und Leistungsprobleme wurden behoben.

## <a name="version-89077454-march-13"></a>Version 89.0.774.54: 13. März

> [!IMPORTANT]
> Dieses Update enthält [CVE-2021-21193,](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21193) für das laut Chromium-Team ein Exploit im Umlauf ist. Weitere Informationen finden Sie im [Leitfaden für Sicherheitsupdates](https://msrc.microsoft.com/update-guide).

Stabile Kanalsicherheitsupdates sind [hier aufgeführt.](./microsoft-edge-relnotes-security.md#march-13-2021)

## <a name="version-89077450-march-10"></a>Version 89.0.774.50: 10. März

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-89077448-march-8"></a>Version 89.0.774.48: 8. März

Verschiedene Fehler und Leistungsprobleme wurden behoben.

<!-- begin major 89 -->
## <a name="version-89077445-march-4"></a>Version 89.0.774.45: 4. März

> [!IMPORTANT]
> Dieses Update enthält [CVE-2021-21166,](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21166) für das laut Chromium-Team ein Exploit im Umlauf ist. Weitere Informationen finden Sie im [Leitfaden für Sicherheitsupdates](https://msrc.microsoft.com/update-guide).

Stabile Kanalsicherheitsupdates sind [hier aufgeführt.](./microsoft-edge-relnotes-security.md#march-4-2021)

### <a name="resolved-issues"></a>Gelöste Probleme

- **Aktualisierungen und Korrekturen von Taskleisten- und Startmenü-Verknüpfungen:**
  - Wenn Sie mit der rechten Maustaste auf die Microsoft Edge-Verknüpfung im Startmenü klicken, wird jetzt die Option zum Entfernen von Microsoft Edge aus der Taskleiste korrekt angezeigt, wenn es angeheftet ist.
  - Startlayouts, die eine [Taskleistenkonfiguration](/windows/configuration/configure-windows-10-taskbar) zum Anheften von Microsoft Edge an die Taskleiste enthalten, führen nicht mehr dazu, dass eine zweite Microsoft Edge-Verknüpfung an die Taskleiste angeheftet wird.
  - Unternehmen, die Windows-Roaming-Profile verwenden, sehen nicht mehr ein leeres weißes Symbol anstelle des Microsoft Edge-Symbols in der Taskleiste, wenn sich ihre Benutzer bei Windows anmelden.

### <a name="feature-updates"></a>Funktionsupdates

- 
            **Der Kiosk-Modus ermöglicht zusätzliche Sperrfunktionen**. Ab Microsoft Edge Version 89 haben wir zusätzliche Sperrfunktionen im Kioskmodus hinzugefügt, damit Kunden ihre Arbeit produktiver und sicherer erledigen können. 
            [Mehr dazu](microsoft-edge-configure-kiosk-mode.md#kiosk-mode-supported-features).

- 
            **Das Site List Manager-Tool im Enterprise-Modus ist im Browser über die Seite *edge://compat* verfügbar**. Mit diesem Tool können Sie XML-Site-Listen für den Internet Explorer-Modus unter Microsoft Edge erstellen, bearbeiten und exportieren. Sie können den Zugriff auf dieses Tool nach Bedarf über Gruppenrichtlinien aktivieren. 
            [Mehr dazu](./edge-ie-mode-site-list-manager.md).

- 
            **Verbessern der Browserleistung mit ruhenden Registerkarten**. Das Ruhen von Registerkarten verbessert die Browserleistung, indem inaktive Registerkarten in den Ruhezustand versetzt werden, um Systemressourcen wie Speicher und CPU freizugeben, sodass aktive Registerkarten oder andere Anwendungen sie verwenden können. Benutzer können verhindern, dass Websites in den Ruhezustand versetzt werden, und die Zeitspanne konfigurieren, in der eine inaktive Registerkarte in den Ruhezustand versetzt wird. Um die Benutzer in ihrem Fluss zu halten, gibt es auch [Heuristiken](https://techcommunity.microsoft.com/t5/articles/sleeping-tabs-faq/m-p/1705434), die verhindern, dass bestimmte Websites in den Ruhezustand versetzt werden, z. B. Intranetsites. Diese Funktion kann mit Gruppenrichtlinien verwaltet werden.

- 
            **Setzen Sie Ihre Microsoft Edge-Synchronisierungsdaten in der Cloud manuell zurück**. Wir bieten eine Möglichkeit, Ihre Microsoft Edge-Synchronisierungsdaten aus dem Produkt heraus zurückzusetzen. Auf diese Weise wird sichergestellt, dass Ihre Daten aus den Microsoft-Diensten gelöscht werden und bestimmte Produktprobleme behoben werden, für die zuvor ein Support-Ticket erforderlich war.

- 
            **Intelligente Aktivierung von einmaligem Anmelden (Single Sign-On, SSO) für alle Windows Azure Active Directory (Azure AD)-Konten für Benutzer mit einem einzigen Microsoft Edge-Profil ohne Azure AD**.  Aktivieren Sie diese Einstellung automatisch für Benutzer, die von diesem Feature am meisten profitieren können. Wenn ein Benutzer nur über ein Microsoft Edge-Profil verfügt (und es sich nicht um Azure AD oder den Modus für Kinder handelt), wird die Einstellung automatisch aktiviert, sobald Microsoft Edge gestartet wird. Dieser automatische Umschalter wird auch automatisch deaktiviert, wenn sich ein Benutzer später mit einem Azure AD-Konto bei einem anderen Microsoft Edge-Profil anmeldet. Benutzer können ihre Einstellungen für dieses Feature unter **Einstellungen > Profile > Profileinstellungen > Einmaliges Anmelden für Geschäfts-, Schul- oder Uniwebsites mithilfe dieses Profils zulassen** manuell aktualisieren.

- 
            **Verbesserungen bei der Textauswahl in PDF-Dokumenten**. Benutzer erhalten eine reibungslosere und konsistentere Textauswahl für PDF-Dokumente, die ab Version 89 in Microsoft Edge geöffnet werden.

- 
            **Das Feld für das Geburtsdatum wird jetzt beim automatischen Ausfüllen unterstützt**. Heute hilft Ihnen Microsoft Edge, Zeit und Mühe beim Ausfüllen von Formularen und beim Erstellen von Online-Konten zu sparen, indem Sie Ihre Daten wie Adressen, Namen, Telefonnummern usw. automatisch ausfüllen. Ab Microsoft Edge Version 89 bieten wir Unterstützung für ein anderes Feld, das Sie gespeichert und automatisch ausgefüllt haben können – das Geburtsdatum. Sie können diese Informationen jederzeit in Ihren Profileinstellungen anzeigen, bearbeiten und löschen.

### <a name="policy-updates"></a>Richtlinienupdates

#### <a name="new-policies"></a>Neue Richtlinien

Es wurden sieben neue Richtlinien hinzugefügt. Laden Sie die aktualisierten administrativen Vorlagen von der [Microsoft Edge Enterprise-Angebotsseite](https://www.microsoft.com/edge/business/download) herunter. Die folgenden neuen Richtlinien wurden hinzugefügt.

- 
            [BrowsingDataLifetime](./microsoft-edge-policies.md#browsingdatalifetime) – Durchsuchen der Einstellungen für die Lebensdauer von Daten
- 
            [MAMEnabled](./microsoft-edge-policies.md#mamenabled) – Mobile App Management aktiviert
- 
            [DefinePreferredLanguages](./microsoft-edge-policies.md#definepreferredlanguages) – Definiert eine geordnete Liste der bevorzugten Sprachen, in denen Websites angezeigt werden sollen, wenn die Website die Sprache unterstützt
- 
            [ShowRecommendationsEnabled](./microsoft-edge-policies.md#showrecommendationsenabled) – Zulassen von Empfehlungen und Werbebenachrichtigungen von Microsoft Edge
- 
            [PrintingAllowedBackgroundGraphicsModes](./microsoft-edge-policies.md#printingallowedbackgroundgraphicsmodes) – Einschränken des Druckmodus für Hintergrundgrafiken
- 
            [PrintingBackgroundGraphicsDefault](./microsoft-edge-policies.md#printingbackgroundgraphicsdefault)– Standard-Druckmodus für Hintergrundgrafiken
- 
            [SmartActionsBlockList](./microsoft-edge-policies.md#smartactionsblocklist)– Blockieren der intelligenten Aktionen für eine Liste von Diensten

#### <a name="obsoleted-policies"></a>Veraltete Richtlinie

Die folgenden Richtlinien sind veraltet.

- 
            [ForceLegacyDefaultReferrerPolicy](./microsoft-edge-policies.md#forcelegacydefaultreferrerpolicy): Verwenden Sie die standardmäßige Verweiserrichtlinie „kein Verweiser beim Downgrade“
- 
            [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) – Aktivieren Sie die Berichterstellung für Nutzung und Absturz
- 
            [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices) – Senden von Site-Informationen, um die Microsoft-Dienste zu verbessern
<!-- end major 89 -->

<!-- Archive from 86.0.622.43: October 15 to beta 88.0.705.81: February 25  ->
<!-- Archive from 86.0.622.38-october-9 to beta 86.0.62.215-september-14  ->
<!-- Archived to version 84.0.522.40: July 16 -->

## <a name="see-also"></a>Weitere Informationen

- [Microsoft Edge Enterprise-Startseite](https://aka.ms/EdgeEnterprise)
