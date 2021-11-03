---
title: Anmerkungen zu dieser Version von Microsoft Edge für Beta-Kanal
ms.author: aguta
author: dan-wesley
manager: srugh
ms.date: 11/01/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Anmerkungen zu dieser Version von Microsoft Edge für Beta-Kanal
ms.openlocfilehash: 57ea92fde42d4ad4c63f238c3b30fa218ee5b360
ms.sourcegitcommit: 42f01cad0bf15224222b2aeadb48f03d46c35723
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2021
ms.locfileid: "12154517"
---
# <a name="release-notes-for-microsoft-edge-beta-channel"></a>Versionshinweise für Microsoft Edge Beta-Kanal

Diese Versionshinweise enthalten Informationen zu neuen Funktionen und nicht sicherheitsrelevanten Updates, die im Microsoft Edge Beta-Kanal enthalten sind. Archivierte Versionen dieser Versionshinweise sind [hier](microsoft-edge-relnote-archive-beta-channel.md) verfügbar.

> [!NOTE]
> Die Microsoft Edge-Webplattform entwickelt sich ständig weiter, um Benutzerfreundlichkeit, Sicherheit und Datenschutz zu verbessern. Weitere Informationen finden Sie unter [Kommende Änderungen in Microsoft Edge mit Auswirkungen auf die Websitekompatibilität](/microsoft-edge/web-platform/site-impacting-changes).

## <a name="version-96010548-november-1"></a>Version 96.0.1054.8: 1. November

### <a name="feature-updates"></a>Funktionsupdates

- **Starten Sie progressive Web App (PWA) direkt über Protokolllinks.** Installed PWAs handle links that use a specific protocol for a more integrated experience.

- **Erfahren Sie, wie Sie mathematische Probleme mit Math Solver lösen.** Wir freuen uns, Ihnen mitteilen zu können, dass Sie Math Solver in Microsoft Edge verwenden können, um Hilfe bei einer Vielzahl mathematischer Konzepte zu erhalten. Diese Konzepte reichen von elementaren arithmetischen und quadratischen Formeln bis hin zu Trigonometrie und Berechnung. Mit Math Solver können Sie ein Bild eines handschriftlichen oder gedruckten mathematischen Problems erstellen und dann eine sofortige Lösung mit schrittweisen Anweisungen bereitstellen, die Ihnen helfen, zu erfahren, wie Sie die Lösung ohne Hilfe erreichen. Math Solver verfügt auch über eine mathematische Tastatur, mit der Sie mathematische Probleme einfach eingeben können. Mit dieser Tastatur müssen Sie keine herkömmliche Tastatur durchsuchen, um die benötigten mathematischen Zeichen zu finden. Nach der Lösung Ihres Problems bietet Math Solver Optionen zum weiteren Lernen mit Quizfragen, Arbeitsblättern und Videolernprogrammen.

- **Verbesserungen beim Scrollen für PDF-Dokumente.** Wir verbessern die Bildlaufleistung, um eine reibungslosere Bildlauferfahrung in PDF-Dokumenten bereitzustellen. Während des Bildlaufs werden keine weißen Balken angezeigt.

- **Freihandformhervorhebung auf PDFs.** Die PDF-Anzeige- und Markupoberfläche wird durch die Hinzufügung von Freihandformmarkern verbessert. Sie können Abschnitte in PDFs, auf die Sie keinen Zugriff haben, und gescannte Dokumente hervorheben.

- **Control-Flow Enforcement Technology (CET).**  Microsoft Edge unterstützt einen noch sichereren Browsermodus, der hardwareabhängigen Steuerungsfluss für Browserprozesse verwendet. Der Steuerungsfluss wird auf dieser unterstützten Hardware bereitgestellt: Intel 11. Generation. oder AMD Cer 3. You can disable CET by configuring Image File Execution Options (IFEO) using group policy.

- **Neues Warndialogfeld für Tippfehler bei Websites.** Der Browser zeigt nun eine Warnung auf einigen Websites mit URLs an, die anderen Websites sehr ähnlich aussehen. Diese Benutzeroberfläche verwendet clientseitige Heuristiken, um Benutzer vor Websites zu warnen, die möglicherweise häufig verwendete Websites spoofen. Weitere Informationen finden Sie unter [What is typosquatting?](https://support.microsoft.com/topic/what-is-typosquatting-54a18872-8459-4d47-b3e3-d84d9a362eb0).

- **Verbesserte Übergabe zwischen dem IE-Modus und dem modernen Browser.**  Ab dieser Version von Microsoft Edge enthalten navigations zwischen Microsoft Edge und Internet Explorer-Modus Formulardaten und zusätzliche HTTP-Header. Referrer-Header, Post-Daten, Formulardaten und Anforderungsmethoden werden auf den beiden Oberflächen korrekt weitergeleitet. Mithilfe der [InternetExplorerIntegrationComplexNavDataTypes-Richtlinie](/deployedge/microsoft-edge-policies#internetexplorerintegrationcomplexnavdatatypes) können Sie angeben, welche Datentypen einbezogen werden sollen.

- **Cloud Site List Management für den IE-Modus in der öffentlichen Vorschau.**  Mit cloudbasierter Websitelistenverwaltung können Sie Ihre Websitelisten für den IE-Modus in der Cloud verwalten, ohne dass eine lokale Infrastruktur zum Hosten der Websiteliste Ihrer Organisation erforderlich ist. Sie können auf das Feature für die Verwaltung von Cloudwebsitelisten über die Microsoft Edge Websitelisten im Microsoft 365 Admin Center zugreifen. Weitere Informationen finden Sie im Artikel zur [Cloud-Websitelistenverwaltung für den IE-Modus (Public Preview).](./edge-ie-mode-cloud-site-list-mgmt.md)

- **Aktualisieren sie Microsoft Edge WebWiew2 mithilfe von WSUS.** IT-Administratoren, die WSUS zum Aktualisieren von Microsoft Edge verwenden, können auch Microsoft Edge WebView2 mithilfe von WSUS aktualisieren. Diese Funktion ermöglicht Administratoren einen einfacheren Wartungsprozess für Offlinegeräte.

- **WSUS-Updates für Server.** WSUS- und Katalogupdates für Microsoft Edge Kanäle (Stable, Beta, Dev) gelten jetzt für Windows Server-SKUs, die Microsoft Edge installiert haben, einschließlich Windows Server 2022. Weitere Informationen zum Konfigurieren von WSUS-Updates für Microsoft Edge finden Sie unter [Update Microsoft Edge](https://docs.microsoft.com/mem/configmgr/apps/deploy-use/deploy-edge?bc=https%3A%2F%2Fdocs.microsoft.com%2FDeployEdge%2Fbreadcrumb%2Ftoc.json&toc=https%3A%2F%2Fdocs.microsoft.com%2FDeployEdge%2Ftoc.json#update-microsoft-edge).

### <a name="policy-updates"></a>Richtlinienupdates

#### <a name="new-policies"></a>Neue Richtlinien

- [ApplicationGuardUploadBlockingEnabled](/DeployEdge/microsoft-edge-policies#applicationguarduploadblockingenabled) : Verhindert, dass Dateien in Application Guard hochgeladen werden.
- [AudioProcessHighPriorityEnabled](/DeployEdge/microsoft-edge-policies#audioprocesshighpriorityenabled) : Zulassen, dass der Audioprozess mit einer Priorität ausgeführt wird, die auf Windows über dem normalen Wert liegt.
- [AutoLaunchProtocolsComponentEnabled](/DeployEdge/microsoft-edge-policies#autolaunchprotocolscomponentenabled) – AutoLaunch-Protokollkomponente aktiviert.
- [EfficiencyMode](/DeployEdge/microsoft-edge-policies#efficiencymode) : Konfigurieren Sie, wann der Effizienzmodus aktiviert werden soll.
- [ForceSyncTypes](/DeployEdge/microsoft-edge-policies#forcesynctypes) : Konfigurieren Sie die Liste der Typen, die für die Synchronisierung enthalten sind.
- [InternetExplorerIntegrationComplexNavDataTypes](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationcomplexnavdatatypes) – Konfigurieren Sie, ob Formulardaten und HTTP-Header gesendet werden, wenn sie in den Internet Explorer-Modus wechseln oder ihn verlassen.
- [InternetExplorerModeToolbarButtonEnabled](/DeployEdge/microsoft-edge-policies#internetexplorermodetoolbarbuttonenabled) – Schaltfläche "Neuladen im Internet Explorer-Modus" auf der Symbolleiste anzeigen.
- [PrintPostScriptMode](/DeployEdge/microsoft-edge-policies#printpostscriptmode) – Drucken im PostScript Modus.
- [PrintRasterizePdfDpi](/DeployEdge/microsoft-edge-policies#printrasterizepdfdpi) – Drucken in PDF-DPI rasterisieren.
- [RendererAppContainerEnabled](/DeployEdge/microsoft-edge-policies#rendererappcontainerenabled) – Renderer im App-Container aktivieren.
- [SharedLinksEnabled](/DeployEdge/microsoft-edge-policies#sharedlinksenabled) : Anzeigen von Links, die von Microsoft 365 Apps im Verlauf freigegeben wurden.
- [TyposquattingCheckerEnabled](/DeployEdge/microsoft-edge-policies#typosquattingcheckerenabled) – Edge TyposquattingChecker konfigurieren.

<!-- end major 96 --->

## <a name="version-950102038-october-28"></a>Version 95.0.1020.38: 28. Oktober

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-950102020-october-11"></a>Version 95.0.1020.20: 11. Oktober

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-950102014-october-5"></a>Version 95.0.1020.14: 5. Oktober

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-95010209-september-28"></a>Version 95.0.1020.9: 28. September

### <a name="feature-updates"></a>Funktionsupdates

- **Support für „Im Datei-Explorer anzeigen“ für Microsoft Office SharePoint Online-Bibliotheken in Microsoft Edge.**  Jetzt können Sie die Funktion "Im Datei-Explorer anzeigen" für SharePoint Moderne Dokumentbibliotheken online aktivieren. Damit diese Erfahrung für Ihre Benutzer sichtbar und funktionsfähig ist, müssen Sie die Richtlinie Microsoft Edge ["Konfigurieren des Features "Ansicht im Datei-Explorer für SharePoint Seiten in Microsoft Edge"](/deployedge/microsoft-edge-policies#configureviewinfileexplorer) aktivieren und Ihre SharePoint Onlinemandantenkonfiguration aktualisieren. Weitere Informationen: [Anzeigen SharePoint Dateien mit dem Datei-Explorer in Microsoft Edge – SharePoint in Microsoft 365 | Microsoft Docs](/SharePoint/sharepoint-view-in-edge).

- **Datei-URL-Links für Intranetzonen werden im Windows-Datei-Explorer geöffnet.**  Sie können zulassen, dass Datei-URL-Links zu Intranetzonen-Dateien, die von Intranetzonen-HTTPS-Websites stammen, den Windows-Datei-Explorer für diese Datei oder dieses Verzeichnis öffnen. Sie können diese Erfahrung mithilfe der Richtlinie [IntranetFileLinksEnabled](/deployedge/microsoft-edge-policies#intranetfilelinksenabled) aktivieren.

- **Verbesserungen an der Downloaderfahrung.**  Die Unterstützung für die Downloadbenutzeroberfläche wird auf progressive Webanwendungen PWAs und WebView erweitert. Wir beginnen auch mit der Unterstützung von Drag & Drop zum Datei-Explorer und zum Desktop.

- **Machen Sie dort weiter, wo Sie in PDF-Dokumenten aufgehört haben.**  Sie können den Lesezugriff von dem Speicherort fortsetzen, an dem Sie das PDF-Dokument zuletzt geschlossen haben.

- **Der Effizienzmodus verlängert die Akkulaufzeit, wenn Ihr Laptop in den Stromsparmodus wechselt.**  Der Effizienzmodus wird aktiv, wenn Ihr Laptop in Stromsparmodus wechselt, um dem Browser die Verwaltung der Ressourcennutzung zur Verlängerung der Akkulaufzeit Ihres Computers zu ermöglichen. Sie haben vier Optionen für den Zeitpunkt, an dem der Effizienzmodus aktiv wird: Unplugged und low battery, Unplugged, Always und Never. Hinweis: Dies ist ein kontrolliertes Featurerollout. Auf Geräten mit Akku sollte das Feature aktiviert sein.

***Neue Richtlinien***

- [BrowserLegacyExtensionPointsBlockingEnabled](/DeployEdge/microsoft-edge-policies#browserlegacyextensionpointsblockingenabled) – Aktivieren des Blockierens von Browserversionserweiterungspunkten.
- [CrossOriginWebAssemblyModuleSharingEnabled](/DeployEdge/microsoft-edge-policies#crossoriginwebassemblymodulesharingenabled) – Gibt an, ob WebAssembly-Module ursprungsübergreifend gesendet werden können.
- [DisplayCapturePermissionsPolicyEnabled](/DeployEdge/microsoft-edge-policies#displaycapturepermissionspolicyenabled) – Gibt an, ob die Berechtigungsrichtlinie für die Anzeigeerfassung überprüft oder übersprungen wird.
- [InternetExplorerIntegrationWindowOpenHeightAdjustment](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationwindowopenheightadjustment) – Konfigurieren sie die Pixelanpassung zwischen window.open-Höhen, die von IE-Modusseiten im Vergleich zu Microsoft Edge-Modusseiten stammen.
- [InternetExplorerIntegrationWindowOpenWidthAdjustment](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationwindowopenheightadjustment) – Konfigurieren sie die Pixelanpassung zwischen window.open-Breiten, die von IE-Modusseiten bezogen werden, im Vergleich zu Microsoft Edge Modusseiten.
- [IntranetFileLinksEnabled](/DeployEdge/microsoft-edge-policies#intranetfilelinksenabled) : Zulassen, dass Intranetzone-Datei-URL-Links von Microsoft Edge im Windows Datei-Explorer geöffnet werden.
- [ShadowStackCrashRollbackBehavior](/DeployEdge/microsoft-edge-policies#shadowstackcrashrollbackbehavior) – Konfigurieren des ShadowStack-Absturzrollbackverhaltens.
- [VisualSearchEnabled](/DeployEdge/microsoft-edge-policies#visualsearchenabled) – Visuelle Suche aktivieren.

***Abgeschaffte Richtlinien***

- [InternetExplorerIntegrationTestingAllowed](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationtestingallowed): Internet Explorer-Modus-Tests zulassen.
- [LegacySameSiteCookieBehaviorEnabled](/DeployEdge/microsoft-edge-policies#legacysamesitecookiebehaviorenabled) – Standardeinstellung für das Verhalten von Legacy-SameSite-Cookies aktivieren.

## <a name="version-94099223-september-17"></a>Version 94.0.992.23: 17. September

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-94099219-september-13"></a>Version 94.0.992.19: 13. September

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-94099214-september-7"></a>Version 94.0.992.14: 7. September

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-9409929-september-2"></a>Version 94.0.992.9: 2. September

### <a name="feature-updates"></a>Funktionsupdates

- **Microsoft Edge zu einem vierwöchigen Rhythmus für Updates in Beta- und Stable-Kanälen wechseln.**  Wir werden einen neuen 4-wöchigen Veröffentlichungszyklus für Hauptversionen einführen. Weitere Informationen zur Entscheidung finden Sie hier: https://blogs.windows.com/msedgedev/2021/03/12/new-release-cycles-microsoft-edge-extended-stable/

- **Neue Option „Stabil (Erweitert)“ wird angeboten.**  Wir bieten unseren verwalteten Enterprise-Kunden eine neue Option „Stabil (Erweitert)“ an. Die Option „Stabil (Erweitert)“ bleibt bei geraden Revisionsnummern und wird alle 8 Wochen aktualisiert. Es wird ein zweiwöchentliches Sicherheitsupdate geben.  Weitere Informationen finden Sie hier: https://blogs.windows.com/msedgedev/2021/07/15/opt-in-extended-stable-release-cycle/

- **Verbesserungen des Standardverhaltens beim Öffnen von MHTML-Dateien.**  MHTML-Dateien werden weiterhin im IE-Modus geöffnet, wenn der IE-Modus aktiviert ist, es sei denn, die MHTML-Datei wurde aus Microsoft Edge heraus gespeichert (mit den Optionen „Speichern unter“ oder „Seite speichern unter“ in Microsoft Edge). Wenn die Datei aus Microsoft Edge heraus gespeichert wurde, wird sie nun in Microsoft Edge geöffnet.  Diese Änderung behebt ein Renderingproblem, das beim Öffnen einer MHTML-Datei im IE-Modus festgestellt wurde, wenn diese aus Microsoft Edge heraus gespeichert wurde.

- **Beschränken Sie private Netzwerkanforderungen auf sichere Kontexte.** Der Zugriff auf Ressourcen in lokalen Netzwerken (Intranet) von Seiten im Internet erfordert, dass diese Seiten über HTTPS bereitgestellt werden. Diese Änderung erfolgt im Chromium-Projekt, auf dem Microsoft Edge basiert. Weitere Informationen finden Sie im [Chrome-Plattformstatuseintrag](https://chromestatus.com/feature/5436853517811712). Zur Unterstützung von Szenarien, in denen die Kompatibilität mit nicht sicheren Seiten beibehalten werden muss, stehen zwei Kompatibilitätsrichtlinien zur Verfügung: [InsecurePrivateNetworkRequestAllowed](/deployedge/microsoft-edge-policies#insecureprivatenetworkrequestsallowed) und [InsecurePrivateNetworkRequestAllowedForUrls](/deployedge/microsoft-edge-policies#insecureprivatenetworkrequestsallowedforurls).

- **Blockieren Sie Downloads gemischter Inhalte.** Sichere Seiten laden nur Dateien herunter, die auf anderen sicheren Seiten gehostet werden, und auf nicht sicheren Seiten (nicht HTTPS) gehostete Downloads werden blockiert, wenn sie von einer sicheren Seite aus initiiert wurden. Diese Änderung erfolgt im Chromium-Projekt, auf dem Microsoft Edge basiert. Für weitere Informationen navigieren Sie zum [Google Security-Blogeintrag](https://security.googleblog.com/2020/02/protecting-users-from-insecure_6.html).

- **Aktivieren Sie die implizite Anmeldung für lokale Konten.**   Durch Aktivieren der Richtlinie OnlyOnPremisesImplicitSigninEnabled werden nur lokale Konten für die implizite Anmeldung aktiviert.  Microsoft Edge wird keine implizite Anmeldung bei MSA- oder AAD-Konten versuchen. Das Upgrade von lokalen Konten auf AAD-Konten wird ebenfalls beendet.

- **Freiformtextfelder, die PDF-Dokumenten hinzugefügt werden.**  Wir unterstützen jetzt das Hinzufügen von Freihandtextfeldern zu PDF-Dokumenten, mit denen Sie Formulare ausfüllen und sichtbare Notizen hinzufügen können.

- **Aktualisieren Sie Ihre Kennwörter ganz einfach.**  Der Browser führt Sie nun direkt zur Seite zum Ändern des Kennworts für eine bestimmte Website, wodurch Sie Zeit und Klicks sparen, indem Sie vermeiden, dass Sie manuell zu der Seite navigieren müssen. Sobald Sie sich auf dieser Seite befinden, füllt der Browser auch Ihr vorhandenes Kennwort automatisch aus und schlägt ein sicheres, eindeutiges neues Kennwort vor.  Bitte beachten Sie: Dieses Feature ist derzeit auf einer begrenzten Anzahl von Websites verfügbar.  

- **Neue Seite für Barrierefreiheitseinstellungen.** Wir haben Einstellungen im Zusammenhang mit Barrierefreiheit auf einer einzigen Seite zusammengefasst. Sie finden die neue Seite „edge://settings/accessibility „ unter der Liste mit den Haupteinstellungen. Hier finden Sie Einstellungen, um die Webseite zu vergrößern, eine Gliederung mit hoher Sichtbarkeit um den Fokusbereich anzuzeigen, sowie andere Einstellungen, die Ihnen helfen, Ihre Webbrowsingerfahrung zu verbessern. In zukünftigen Versionen von Microsoft Edge werden wir weitere neue Einstellungen hinzufügen.

***Neue Richtlinien***

- [ApplicationGuardPassiveModeEnabled](/DeployEdge/microsoft-edge-policies#applicationguardpassivemodeenabled) Application Guard-Websitelistenkonfiguration ignorieren und Edge normal nutzen
- [OnlyOnPremisesImplicitSigninEnabled](/DeployEdge/microsoft-edge-policies#onlyonpremisesimplicitsigninenabled) Nur lokale Konten, die für die implizite Anmeldung aktiviert sind
- [WebRtcRespectOsRoutingTableEnabled](/DeployEdge/microsoft-edge-policies#webrtcrespectosroutingtableenabled) Unterstützung für Windows-BS-Routingtabellenregeln beim Herstellen von Peer-to-Peer-Verbindungen über WebRTC aktivieren

***Veraltete Richtlinie***

- [UserAgentClientHintsEnabled](/DeployEdge/microsoft-edge-policies#useragentclienthintsenabled): Die Funktion „User-Agent Client Hints“ aktivieren

## <a name="version-93096133-august-27"></a>Version 93.0.961.33: 27. August

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-93096127-august-20"></a>Version 93.0.961.27: 20. August

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-93096124-august-18"></a>Version 93.0.961.24: 18. August

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-93096111-august-3"></a>Version 93.0.961.11: 3. August

### <a name="feature-updates"></a>Funktionsupdates

- **Voreinstellungen in Microsoft Edge.**  Ab Microsoft Edge Version 93 wird die Bereitstellung von Microsoft Edge in Ihrem Unternehmen durch die Hinzufügung der [anfänglichen Einstellungen](/deployedge/initial-preferences-support-on-microsoft-edge-browser)einfacher.

- **Der IE-Modus auf Microsoft Edge unterstützt das "no-merge" Verhalten.**  Ab Microsoft Edge Version 93 unterstützt der IE-Modus auf Microsoft Edge "No-Merge". Wenn ein neues Browserfenster von einer IE-Modusanwendung gestartet wird, befindet sich ein Endbenutzer in einer separaten Sitzung, ähnlich wie in IE11. Sie müssen Ihre Websiteliste anpassen, um Websites zu konfigurieren, die die Sitzungsfreigabe verhindern müssen. Im Hintergrund wird für jedes Fenster von Microsoft Edge beim ersten Aufrufen einer IE-Modusregisterkarte in diesem Fenster, wenn es sich um eine der vorgesehenen "no-merge"-Websites handelt, dieses Fenster in eine andere "no-merge" IE-Sitzung von allen anderen Microsoft Edge-Fenstern gesperrt, mindestens bis die letzte Registerkarte für den IE-Modus in diesem Fenster geschlossen wird. Weitere Informationen finden Sie [hier](/deployedge/edge-ie-mode-faq#does-ie-mode-on-microsoft-edge-support-the--no-merge--option-that-was-supported-in-internet-explorer-11-).

- **Registerkartengruppen.**  Die Möglichkeit, Registerkarten in benutzerdefinierte Gruppen zu kategorisieren, hilft Ihnen, Registerkarten in mehreren Arbeitsstreams effektiver zu finden, zu wechseln und zu verwalten. Um dies zu aktivieren, aktivieren wir die Registerkartengruppierung ab Microsoft Edge Version 93.

- **Blenden Sie die Titelleiste aus, während Sie vertikale Registerkarten verwenden.**  Holen Sie sich die zusätzlichen Pixel zurück, indem Sie die Titelleiste des Browsers ausblenden, während Sie sich auf vertikalen Registerkarten befinden. Ab Microsoft Edge Version 93 können Sie zu edge://settings/appearance wechseln, und wählen Sie unter dem Abschnitt Symbolleiste anpassen die Option aus, um die Titelleiste im vertikalen Registerkartenmodus auszublenden.

- **Videobild in Bild (PiP) auf der Symbolleiste mit dem Mauszeiger.**  Ab Microsoft Edge Version 93 wird es noch einfacher, in den Bild-Modus (PiP) zu wechseln. Wenn Sie auf ein unterstütztes Video zeigen, wird eine Symbolleiste angezeigt, mit der Sie dieses Video in einem PiP-Fenster anzeigen können.  Hinweis: Dies ist derzeit für Microsoft Edge Benutzer unter macOS verfügbar.  Schauen Sie sich kurz zurück, während wir unseren Rollout für Windows Benutzer fortsetzen.

- **Entfernen von 3DES in TLS.**  Ab Microsoft Edge Version 93 wird die Unterstützung für die TLS_RSA_WITH_3DES_EDE_CBC_SHA Verschlüsselungssuite entfernt. Diese Änderung erfolgt im Chromium-Projekt, auf dem Microsoft Edge basiert. Weitere Informationen finden Sie im [Chrome-Plattformstatuseintrag](https://chromestatus.com/feature/6678134168485888). Darüber hinaus steht in Microsoft Edge Version 93 die [TripleDESEnabled](/deployedge/microsoft-edge-policies#tripledesenabled)-Richtlinie zur Unterstützung von Szenarien zur Verfügung, die die Kompatibilität mit veralteten Servern beibehalten müssen. Diese Kompatibilitätsrichtlinie wird veraltet und funktioniert nicht mehr in Microsoft Edge Version 95. Stellen Sie sicher, dass Sie betroffene Server vorher aktualisieren.

- **Richtlinien zum Umgehen von ClickOnce- und DirectInvoke-Eingabeaufforderungen.**  Wir haben unsere Richtlinien aktualisiert, um die Umgehung von ClickOnce-Eingabeaufforderungen und der DirectInvoke-App für angegebene Dateitypen aus angegebenen Domänen zu ermöglichen. Dazu müssen Sie folgende Schritte ausführen:

  - Aktivieren von [ClickOnceEnabled](/deployedge/microsoft-edge-policies#clickonceenabled) oder [DirectInvokeEnabled](/deployedge/microsoft-edge-policies#directinvokeenabled)
  - Aktivieren Sie die [AutoOpenFileTypes](/deployedge/microsoft-edge-policies#autoopenfiletypes)-Richtlinie und legen Sie die Liste der spezifischen Dateitypen fest, für die ClickOnce und DirectInvoke deaktiviert werden sollen.
  - Aktivieren Sie die [AutoOpenAllowedForURLs-Richtlinie,](/deployedge/microsoft-edge-policies#autoopenallowedforurls) und legen Sie die Liste der bestimmten Domänen fest, für die ClickOnce und DirectInvoke deaktiviert wird

  Hinweis: AutoOpenAllowedForURLs ist eine Supporterrichtlinie für AutoOpenFileTypes. Wenn AutoOpenAllowedForURLs nicht festgelegt und AutoOpenFileTypes festgelegt ist, werden die aufgelisteten Dateitypen automatisch über alle URLs geöffnet.

### <a name="new-policies"></a>Neue Richtlinien

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

#### <a name="deprecated-policy"></a>Veraltete Richtlinie

- [LegacySameSiteCookieBehaviorEnabled](/DeployEdge/microsoft-edge-policies#legacysamesitecookiebehaviorenabled) Aktivieren der Standardeinstellung für das Verhalten von Legacy-SameSite-Cookies

#### <a name="obsoleted-policy"></a>Veraltete Richtlinie

- [NewTabPageSetFeedType](/DeployEdge/microsoft-edge-policies#newtabpagesetfeedtype) Konfigurieren der Microsoft Edge-Oberfläche für neue Registerkartenseiten

#### <a name="additional-change"></a>Zusätzliche Änderung

- [ConfigureShare](/DeployEdge/microsoft-edge-policies#configureshare) Hinzufügen der Mac-Plattformunterstützung

## <a name="version-93096118-august-10"></a>Version 93.0.961.18: 10. August

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-92090262-july-29"></a>Version 92.0.902.62: 29. Juli

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-92090255-july-21"></a>Version 92.0.902.55: 21. Juli

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-92090245-july-12"></a>Version 92.0.902.45: 12. Juli

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-92090240-july-6"></a>Version 92.0.902.40: 6. Juli

Verschiedene Fehler und Leistungsprobleme wurden behoben.

<!--Archive on Oct 27 From Version 92.0.902.22: June 21 to Version 89.0.774.23: February 8  -->
<!--- Archived from Version 87.0.664.18: October 26 to to version 89.0.774.18: February 3 ---->
<!--- Archived from Version 87.0.664.12: October 20 to to version 86.0.622.15: September 14 ---->
<!--- Archived to version 86.0.622.11: September 9 ---->
<!--- Archived to version 85.0.564.18: July 28 ---->

## <a name="see-also"></a>Weitere Informationen

- [Microsoft Edge Enterprise-Startseite](https://aka.ms/EdgeEnterprise)
