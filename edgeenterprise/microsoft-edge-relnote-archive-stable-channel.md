---
title: Archivierte Versionshinweise für Microsoft Edge Stable Channel
ms.author: leahtu
author: dan-wesley
manager: srugh
ms.date: 03/31/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Archivierte Versionshinweise für Microsoft Edge Stable Channel
ms.openlocfilehash: d2c1d9de5d68b008190bbdcc24aee83c352978aa
ms.sourcegitcommit: dd8cdbd35726c795ddce917e549ddf17ee7f5290
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/11/2022
ms.locfileid: "12473597"
---
# <a name="archived-release-notes-for-microsoft-edge-stable-channel"></a>Archivierte Versionshinweise für Microsoft Edge Stable Channel

Diese Versionshinweise enthalten Informationen zu neuen Funktionen und nicht sicherheitsrelevanten Updates, die im Microsoft Edge Stable Channel enthalten sind. Alle Sicherheitsupdates werden [hier](microsoft-edge-relnotes-security.md) aufgelistet.

## <a name="version-970107255-january-6"></a>Version 97.0.1072.55: 6. Januar

Sicherheitsupdates im Stabilen Kanal sind [hier](/deployedge/microsoft-edge-relnotes-security#january-6-2022) aufgeführt.

### <a name="feature-updates"></a>Funktionsupdate

- **Verwenden Sie das aktuelle Profil, um sich bei Websites anzumelden, wenn mehrere Geschäfts-, Schul- oder Unikonten auf einem Gerät angemeldet sind.** Wenn mehrere Geschäfts-, Schul- oder Unikonten auf einem Gerät angemeldet sind, werden Benutzer aufgefordert, ein Konto aus der Kontoauswahl auszuwählen, um ihre Websitebesuche fortzusetzen. In diesem Release werden die Benutzer aufgefordert, Microsoft Edge das automatische Anmelden mit dem Geschäfts-, Schul- oder Unikonto bei Websites zu gestatten, bei dem das aktuelle Profil angemeldet ist. Benutzer können dieses Feature unter **Einstellungen** >  **Profileinstellungen** aktivieren und deaktivieren.

- **Fügen Sie Unterstützung für Microsoft Endpoint Data Loss Prevention (DLP, Verhinderung von Datenschutz am Endpunkt) unter macOS hinzu.** Die Erzwingung von Microsoft Endpoint DLP-Richtlinien ist nun nativ unter macOS verfügbar.

- **Automatisches HTTPS.** Benutzer können die Navigation von HTTP auf HTTPS für Domänen ändern, die wahrscheinlich dieses sicherere Protokoll unterstützen. Diese Unterstützung kann auch so konfiguriert werden, dass die Übermittlung über HTTPS für alle Domänen versucht wird. Hinweis: Hierbei handelt es sich um ein Feature für den kontrollierten Rollout. Wenn Sie dieses Feature nicht sehen, sehen Sie immer wieder nach, da wir mit dem Rollout fortfahren.

- **WebSQL in Drittanbieterkontexten blockieren.** Die Verwendung des veralteten WebSQL-Features wird von Drittanbieterframes blockiert. Die [WebSQLInThirdPartyContextEnabled](/deployedge/microsoft-edge-policies#websqlinthirdpartycontextenabled)-Richtlinie ist bis Microsoft Edge Version 101 als Opt-Out-Option verfügbar. Diese Änderung erfolgt im Chromium-Projekt, auf dem Microsoft Edge basiert. Weitere Informationen finden Sie in diesem [Chrome-Plattformstatuseintrag](https://chromestatus.com/feature/5684870116278272).

- **Zitate in Microsoft Edge.** Das Angeben von Quellen für Recherchen ist eine häufige Anforderung für Schüler/Studenten. Sie müssen viele Recherchereferenzen und Quellen verwalten, was keine einfachen Aufgaben ist. Sie müssen diese Zitate auch in die richtigen Zitatformate wie APA, MLA und Chicago übertragen. Dieses neue "Zitate"Feature in der Vorschau in Microsoft Edge ermöglicht es Schülern/Studenten, Zitate besser zu verwalten und zu erstellen, während sie online recherchieren. Wenn das "Zitate"-Feature in "Sammlungen" oder über **Einstellungen und mehr (ALT-F)** aktiviert ist, generiert Microsoft Edge automatisch Zitate, die Schüler später verwenden können, sodass sie sich auf ihre Recherchen konzentrieren können. Wenn sie fertig sind, können sie diese Zitate ganz einfach in ein endgültiges Dokument einfügen. Weitere Informationen finden Sie unter ["Zitate“-Feature in Microsoft Edge (Vorschau)](https://blogs.windows.com/msedgedev/2021/11/04/preview-citations-feature-edge/).

- **Ablaufsteuerungsschutz (Control Flow Guard, CFG)** Microsoft Edge wird beginnen, einen differenzierteren Schutz zu unterstützen, indem Sicherheitsrisiken aufgrund von Speicherbeschädigungen behoben und indirekte Aufrufe geschützt werden. CFG wird nur mit Windows 8 und höher unterstützt. Weitere Informationen finden Sie unter [Ablaufsteuerungsschutz](/windows/win32/secbp/control-flow-guard).
  
  > [!NOTE]
  > Dies ist eine von uns beständig weiterentwickelte Technologie. Teilen Sie uns Ihr Feedback mit, um den Support zu stärken.

### <a name="policy-updates"></a>Richtlinienupdates

#### <a name="new-policies"></a>Neue Richtlinien

- [AccessibilityImageLabelsEnabled](/DeployEdge/microsoft-edge-policies#accessibilityimagelabelsenabled): Abrufen von Bildbeschreibungen von Microsoft Enabled
- [CORSNonWildcardRequestHeadersSupport](/DeployEdge/microsoft-edge-policies#corsnonwildcardrequestheaderssupport): CORS-Unterstützung für Nicht-Platzhalter-Anforderungsheader aktiviert
- [EdgeDiscoverEnabled](/DeployEdge/microsoft-edge-policies#edgediscoverenabled): Das Feature „Entdecken“ in Microsoft Edge
- [EdgeEnhanceImagesEnabled](/DeployEdge/microsoft-edge-policies#edgeenhanceimagesenabled): Bilder verbessern aktiviert
- [InternetExplorerModeTabInEdgeModeAllowed](/DeployEdge/microsoft-edge-policies#internetexplorermodetabinedgemodeallowed): Zulassen des Öffnens von Websites in Microsoft Edge, die für den Internet Explorer-Modus konfiguriert sind
- [SameOriginTabCaptureAllowedByOrigins](/DeployEdge/microsoft-edge-policies#sameorigintabcaptureallowedbyorigins): Zulassen der Registerkartenerfassung „Gleicher Ursprung“ durch diese Ursprünge
- [ScreenCaptureAllowedByOrigins](/DeployEdge/microsoft-edge-policies#screencaptureallowedbyorigins): Zulassen der Desktop-, Fenster- und Registerkartenerfassung durch diese Ursprünge
- [SerialAllowAllPortsForUrls](/DeployEdge/microsoft-edge-policies#serialallowallportsforurls): Websites automatisch die Berechtigung erteilen, eine Verbindung zu allen seriellen Anschlüssen herzustellen
- [SerialAllowUsbDevicesForUrls](/DeployEdge/microsoft-edge-policies#serialallowusbdevicesforurls): Websites die Berechtigung zum Herstellen einer Verbindung mit seriellen USB-Geräten automatisch erteilen
- [SmartScreenDnsRequestsEnabled](/DeployEdge/microsoft-edge-policies#smartscreendnsrequestsenabled): Aktivieren von Microsoft Defender SmartScreen DNS-Anforderungen
- [TabCaptureAllowedByOrigins](/DeployEdge/microsoft-edge-policies#tabcaptureallowedbyorigins): Zulassen der Registerkartenerfassung durch diese Ursprünge
- [WebSQLInThirdPartyContextEnabled](/DeployEdge/microsoft-edge-policies#websqlinthirdpartycontextenabled): Erzwingen der erneuten Aktivierung von WebSQL in Drittanbieterkontexten
- [WindowCaptureAllowedByOrigins](/DeployEdge/microsoft-edge-policies#windowcaptureallowedbyorigins): Zulassen der Registerkarten- und Fenstererfassung durch diese Ursprünge

## <a name="version-960105462-december-17"></a>Version 96.0.1054.62: 17. Dezember

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-960105457-december-14"></a>Version 96.0.1054.57: 14. Dezember

> [!Important]
> Dieses Update enthält einen Fix für [CVE-2021-4102](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-4102), wovon laut Chromium-Team ein Exploit in Umlauf ist. Weitere Informationen finden Sie im [Leitfaden zu Sicherheitsupdates](https://msrc.microsoft.com/update-guide).

Stable Channel-Sicherheitsupdates sind [hier](/deployedge/microsoft-edge-relnotes-security#december-14-2021) aufgeführt.

## <a name="version-960105453-december-10"></a>Version 96.0.1054.53: 10. Dezember

Stable Channel-Sicherheitsupdates sind [hier](/deployedge/microsoft-edge-relnotes-security#december-10-2021) aufgeführt.

## <a name="version-960105443-december-2"></a>Version 96.0.1054.43: 2. Dezember

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-960105441-november-30"></a>Version 96.0.1054.41: 30. November

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-960105434-november-23"></a>Version 96.0.1054.34: vom 23. November

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-960105429-november-19"></a>Version 96.0.1054.29: 19. November

Stable Channel-Sicherheitsupdates sind [hier](/deployedge/microsoft-edge-relnotes-security#november-19-2021) aufgeführt.

### <a name="feature-updates"></a>Funktionsupdates

- **Verwaltung von Cloudwebsitelisten für den IE-Modus in der öffentlichen Vorschau.** Mit der Verwaltung von Cloudwebsitelisten können Sie Ihre Websitelisten für den IE-Modus in der Cloud verwalten, ohne dass eine lokale Infrastruktur zum Hosten der Websiteliste Ihrer Organisation erforderlich ist. Sie können mithilfe der Microsoft Edge Site Lists-Oberfläche im Microsoft 365 Admin Center auf das Feature "Verwaltung von Cloudwebsitelisten" zugreifen. Weitere Informationen finden Sie im Artikel [zur Verwaltung von Cloudwebsitelisten für den IE-Modus (Öffentliche Vorschau).](./edge-ie-mode-cloud-site-list-mgmt.md)
  
- **Verbesserte Übergabe zwischen dem IE-Modus und dem modernen Browser.** Ab dieser Version von Microsoft Edge enthält die Navigation zwischen Microsoft Edge und dem Internet Explorer-Modus Formulardaten und zusätzliche HTTP-Header. Referrer headers, post data, forms data, and request methods will be forwarded correctly across the two experiences. Sie können mithilfe der InternetExplorerIntegrationComplexNavDataTypes-Richtlinie angeben, welche Datentypen eingeschlossen werden sollen. Weitere Informationen finden Sie in diesen häufig gestellten Fragen: [Meine Anwendung erfordert die Übertragung von POST-Daten zwischen dem IE-Modus und Microsoft Edge. Wird dies unterstützt?](./edge-ie-mode-faq.md#my-application-requires-transferring-post-data-between-ie-mode-and-microsoft-edge-is-this-supported)

- **Aktualisieren Sie Microsoft Edge WebWiew2 mit WSUS.** IT-Administratoren, die Windows Server Update Services (WSUS) zum Aktualisieren von Microsoft Edge verwenden, können microsoft Edge WebView2 auch mit WSUS aktualisieren. Diese Funktion bietet Administratoren einen einfacheren Wartungsprozess für Offlinegeräte.

- **WSUS-Updates für Server.** WSUS- und Katalogupdates für Microsoft Edge-Kanäle (Stable, Beta und Dev) gelten jetzt für Windows Server-SKUs, auf denen Microsoft Edge installiert ist, einschließlich Windows Server 2022. Weitere Informationen zum Konfigurieren von WSUS-Updates für Microsoft Edge finden Sie unter [Aktualisieren von Microsoft Edge](https://docs.microsoft.com/mem/configmgr/apps/deploy-use/deploy-edge?bc=https://docs.microsoft.com/DeployEdge/breadcrumb/toc.json&toc=https://docs.microsoft.com/DeployEdge/toc.json#update-microsoft-edge).

- **Microsoft Edge AutoLaunch Protocols Component.** Microsoft Edge 96 führt die [Komponente](https://textslashplain.com/2019/07/16/updating-browsers-quickly-flags-respins-and-components/) "AutoLaunch-Protokolle" ein, die Listen von Schemaursprungswörterbüchern enthält, die automatisch zugelassen oder blockiert werden sollen. Dies schützt Kunden vor gefährlichen Schemas (z. B. einem Protokollhandler mit einem 0-Tage-Ereignis), während Aufforderungen zu bekannten sicheren Kopplungen vermieden werden (beispielsweise kann die Teams-Website die Teams Client-App öffnen). Wenn Microsoft Edge aus irgendeinem Grund keine anfälligen Protokollhandler blockieren und bekannte sichere Kopplungen zulassen soll, verwenden Sie den Umschalter in *edge://settings/content/applicationLinks*, oder legen Sie die Richtlinie ["AutoLaunchProtocolsComponentEnabled](/deployedge/microsoft-edge-policies#autolaunchprotocolscomponentenabled) " auf "False" fest.

- **Starten Sie Progressive Web App (PWA) direkt über Protokolllinks.** Lassen Sie installierte PWAs Links verarbeiten, die ein bestimmtes Protokoll für eine integriertere Erfahrung verwenden.

- **Office-Dateien schnell im Browser anzeigen.** Benutzer können jetzt Office-Dateien wie Dokumente, Kalkulationstabellen und Präsentationen anzeigen, die ihnen beim Browsen auf Microsoft Edge direkt im Browser angezeigt werden, ohne die Datei herunterladen und dann in einer anderen Anwendung öffnen zu müssen. Die Dateiöffnungsoberfläche für Office-Dateien, die auf OneDrive oder SharePoint gehostet werden, wird nicht geändert.
  
- **Freihandformhervorhebung auf PDF-Dateien.** Die PDF-Anzeige und markup-Erfahrung wird durch das Hinzufügen von Freihandform-Textmarkern verbessert. Sie können Abschnitte in PDF-Dateien hervorheben, auf die Sie keinen Zugriff haben, und gescannte Dokumente.

- **Hardware-erzwungener Stapelschutz.** Microsoft Edge unterstützt nun einen noch sichereren Browsermodus, der den hardwareabhängigen Steuerungsfluss für Browserprozesse auf unterstützter Hardware verwendet (Intel 11. Generation. oder AMD Zen 3). Hinweis: Da es sich um ein kontrolliertes Featurerollout handelt, stellen Sie möglicherweise nicht fest, dass dieses Feature auf allen Geräten aktiviert ist. Sie können den hardwaredurchsetzten Stapelschutz aktivieren oder deaktivieren, indem Sie die Bilddateiausführungsoptionen (IFEO) mithilfe von Gruppenrichtlinien bearbeiten.

- **Neues Warnungsdialogfeld für Typosquatting-Websites.** Der Browser zeigt eine Warnung auf einigen Websites mit URLs an, die anderen Websites sehr ähnlich aussehen. Diese Benutzeroberfläche verwendet clientseitige Heuristiken, um Benutzer vor Websites zu warnen, die beliebte Websites spoofieren könnten. Weitere Informationen finden Sie unter [Was ist Typosquatting?](https://support.microsoft.com/topic/what-is-typosquatting-54a18872-8459-4d47-b3e3-d84d9a362eb0).
  
- **Wörterbuch, das der Minisymbolleiste in Immersive Reader hinzugefügt wurde.**  Wir fügen der Minisymbolleiste Wörterbuchfunktionen hinzu, um Sie beim Lesen und Recherchieren zu unterstützen. In der Immersive Reader können Sie die Rechtschreibung und Definitionen von Wörtern schneller und einfacher nachschlagen.
  
- **Erfahren Sie, wie Sie mathematische Probleme mit Math Solver lösen.** Wir freuen uns, Ihnen mitteilen zu können, dass Sie Math Solver in Microsoft Edge verwenden können, um Hilfe bei einer Vielzahl von mathematischen Konzepten zu erhalten. Diese Konzepte reichen von elementaren arithmetischen und quadratischen Gleichungen bis hin zu Trigonometrie und Berechnung. Mit Math Solver können Sie ein Bild eines handschriftlichen oder gedruckten mathematischen Problems machen und dann eine sofortige Lösung mit schrittweisen Anleitungen bereitstellen, die Ihnen helfen, zu erfahren, wie Sie die Lösung ohne Hilfe erreichen können. Math Solver verfügt auch über eine mathematische Tastatur, mit der Sie mathematische Probleme einfach eingeben können. Diese Tastatur entfällt die Notwendigkeit, eine herkömmliche Tastatur zu durchsuchen, um die mathematischen Zeichen zu finden, die Sie benötigen. Nachdem Sie Ihr Problem gelöst haben, bietet Math Solver Optionen, um mit Quizfragen, Arbeitsblättern und Videolernprogrammen weiter zu lernen.

- **Split-Tunnel-VPN-Unterstützung für WebRTC.** Ermöglicht Unternehmenskunden den Vorteil des geteilten VPN-Tunnelings für Peer-to-Peer-Datenverkehr auf Microsoft Edge. Sie können dieses Feature mithilfe der [WebRtcRespectOsRoutingTableEnabled-Richtlinie](/deployedge/microsoft-edge-policies#webrtcrespectosroutingtableenabled) aktivieren.

### <a name="policy-updates"></a>Richtlinienupdates

#### <a name="new-policies"></a>Neue Richtlinien

- [ApplicationGuardUploadBlockingEnabled](/DeployEdge/microsoft-edge-policies#applicationguarduploadblockingenabled) – Verhindert das Hochladen von Dateien in Application Guard
- [AudioProcessHighPriorityEnabled](/DeployEdge/microsoft-edge-policies#audioprocesshighpriorityenabled) – Zulassen, dass der Audioprozess unter Windows mit einer Priorität ausgeführt wird, die über der Normalen liegt
- [AutoLaunchProtocolsComponentEnabled – AutoLaunch](/DeployEdge/microsoft-edge-policies#autolaunchprotocolscomponentenabled) Protocols Component Enabled
- [EfficiencyMode](/DeployEdge/microsoft-edge-policies#efficiencymode) – Konfigurieren, wann der Effizienzmodus aktiv werden soll
- [ForceSyncTypes](/DeployEdge/microsoft-edge-policies#forcesynctypes) – Konfigurieren der Liste der Typen, die für die Synchronisierung enthalten sind
- [InternetExplorerIntegrationComplexNavDataTypes](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationcomplexnavdatatypes) – Konfigurieren, ob Formulardaten und HTTP-Header gesendet werden, wenn der Internet Explorer-Modus betreten oder beendet wird
- [InternetExplorerModeToolbarButtonEnabled](/DeployEdge/microsoft-edge-policies#internetexplorermodetoolbarbuttonenabled) – Schaltfläche "Im Internet Explorer-Modus neu laden" auf der Symbolleiste anzeigen
- [PrintPostScriptMode](/DeployEdge/microsoft-edge-policies#printpostscriptmode) – PostScript-Druckmodus
- [PrintRasterizePdfDpi](/DeployEdge/microsoft-edge-policies#printrasterizepdfdpi) – PDF-DPI-Druckrasterung
- [RendererAppContainerEnabled](/DeployEdge/microsoft-edge-policies#rendererappcontainerenabled) – Renderer im App-Container aktivieren
- [SharedLinksEnabled](/DeployEdge/microsoft-edge-policies#sharedlinksenabled) – Links anzeigen, die von Microsoft 365 Apps im Verlauf freigegeben wurden
- [TyposquattingCheckerEnabled](/DeployEdge/microsoft-edge-policies#typosquattingcheckerenabled) – Konfigurieren von Edge-TyposquattingChecker

## <a name="version-950102053-november-12"></a>Version 95.0.1020.53: 12. November

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-950102044-november-4"></a>Version 95.0.1020.44: 4. November

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-94099258-october-30"></a>Version 94.0.992.58: 30. Oktober

Verschiedene Fehler und Leistungsprobleme für das Release „Stabil (Erweitert) wurden behoben.

## <a name="version-950102040-october-29"></a>Version 95.0.1020.40: 29. Oktober

> [!IMPORTANT]
> Dieses Update enthält einen Fix für [CVE-2021-38000](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-38000) und [CVE-2021-38003](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-38003), die vom Chromium-Team als Exploit gemeldet wurden. Weitere Informationen finden Sie im [Leitfaden für Sicherheitsupdates](https://msrc.microsoft.com/update-guide)

Sicherheitsupdates im Stabilen Kanal sind [hier](/deployedge/microsoft-edge-relnotes-security#october-29-2021) aufgeführt.

## <a name="version-950102038-october-28"></a>Version 95.0.1020.38: 28. Oktober

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-94099257-october-27"></a>Version 94.0.992.57: 27. Oktober

Verschiedene Fehler und Leistungsprobleme für das Release „Stabil (Erweitert) wurden behoben.

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

Stable Channel-Sicherheitsupdates sind [hier](/deployedge/microsoft-edge-relnotes-security#september-24-2021) aufgeführt.

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

**MHTML-Dateien werden standardmäßig im Internet Explorer-Modus geöffnet**. Ab Microsoft Edge Version 92 Stable werden MHTML-Dateitypen automatisch im Internet Explorer-Modus auf Microsoft Edge anstelle der Internet Explorer-Anwendung (IE11) geöffnet. Dies wird am häufigsten beim Versuch beobachtet, Outlook-E-Mails in einem Browser anzuzeigen. Diese Änderung tritt nur auf, wenn IE11 der Standardhandler für diesen Dateityp ist. Wenn Sie dies lieber ändern möchten, können Sie dies vor der Installation des Stable Version 92-Updates mithilfe [dieser Anleitung](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration) tun.

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
>Dieses Update enthält einen Fix für [CVE-2021-21224](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21224), der vom Chromium-Team als Exploit gemeldet wurde. Weitere Informationen finden Sie im [Leitfaden zu Sicherheitsupdates](https://msrc.microsoft.com/update-guide).

Sicherheitsupdates im Stabilen Kanal sind [hier](/deployedge/microsoft-edge-relnotes-security#april-16-2021) aufgeführt.

## <a name="version-90081839-april-15"></a>Version 90.0.818.39: 15. April ##

Sicherheitsupdates im Stabilen Kanal sind [hier](/deployedge/microsoft-edge-relnotes-security#april-15-2021) aufgeführt.

## <a name="feature-updates"></a>Funktionsupdates ##

-    **Einmaliges Anmelden (Single Sign On, SSO) ist jetzt für Azure Active Directory (Azure AD)-Konten und Microsoft-Konten (MSA) unter macOS verfügbar.** Ein bei Microsoft Edge unter macOS angemeldeter Benutzer wird nun automatisch bei Websites angemeldet, die so konfiguriert sind, dass eine einmalige Anmeldung mit Arbeits- und Microsoft-Konten möglich ist (z. B. bing.com, office.com, msn.com und outlook.com).

- **Kioskmodus.** Ab Microsoft Edge Version 90 wurden die Druckeinstellungen der Benutzeroberfläche gesperrt, und es werden nur noch die konfigurierten Drucker und „In PDF drucken“-Optionen zugelassen. Wir haben außerdem Verbesserungen am Kioskmodus für den zugewiesenen Zugriff für nur eine App vorgenommen, um das Starten anderer Anwendungen über den Browser einzuschränken. Weitere Informationen zu den Features des Kioskmodus finden Sie [hier](/deployedge/microsoft-edge-configure-kiosk-mode#kiosk-mode-supported-features).

- **Downloads unterbrechen** Ab Microsoft Edge Version 91 wird der Download von Typen, die Ihrem Computer schaden könnten, vom Browser automatisch unterbrochen, wenn diese Downloads ohne Benutzerinteraktion gestartet werden und von der SmartScreen-Anwendungszuverlässigkeitsüberprüfung nicht unterstützt werden. Benutzer können den Download überschreiben und fortsetzen, indem sie mit der rechten Maustaste auf das Downloadelement klicken und „Beibehalten“ auswählen.
Unternehmensadministratoren können dieses Verhalten mit einer der folgenden beiden Richtlinien deaktivieren:
- [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](/deployedge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings): Deaktivieren von auf Dateierweiterungen basierenden Download-Warnungen für bestimmte Dateitypen in Domänen. Weitere Informationen finden Sie unter [Unterbrechung von Microsoft Edge-Sicherheitsdownloads](/deployedge/microsoft-edge-security-downloads-interruptions)

- **Drucken**:

    - **Neuer Druckrasterungsmodus für Nicht-PostScript-Drucker.** Ab Microsoft Edge Version 90 können Administratoren mithilfe einer neuen Richtlinie den Druckrasterungsmodus für ihre Benutzer definieren. Diese Richtlinie steuert, wie Microsoft Edge unter Windows auf Nicht-PostScript-Druckern druckt. Manchmal müssen Druckaufträge bei Nicht-PostScript-Druckern gerastert werden, damit korrekt gedruckt wird. Die Druckoptionen sind „Full" (Vollständig) und „Fast“ (Schnell).
    
  - **Zusätzliche Optionen für die Seitenskalierung beim Drucken.** Benutzer können jetzt die Skalierung anpassen, während sie Webseiten und PDF-Dokumente mit zusätzlichen Optionen drucken. Die Option „An Seite anpassen" stellt sicher, dass die Webseite oder das Dokument in den Bereich passt, der im ausgewählten „Papierformat" zum Drucken verfügbar ist. Die Option "Tatsächliche Größe" stellt sicher, dass sich die Größe des zu druckenden Inhalts unabhängig von der ausgewählten "Papiergröße" nicht ändert.

-   **Produktivität:**

    -   **Vorschläge zum automatischen Ausfüllen werden um den Inhalt von Adressfeldern aus der Zwischenablage erweitert.** Der Inhalt der Zwischenablage wird analysiert, wenn Sie auf ein Profil-/Adressfeld (z. B. Telefon, E-Mail, Postleitzahl, Stadt, Bundesland usw.) klicken, um es als Vorschläge zum automatischen Ausfüllen anzuzeigen.

    -   **Benutzer können nach Vorschlägen zum automatischen Ausfüllen suchen, auch wenn ein Formular oder Feld nicht erkannt wird.** Wenn Sie Ihre Informationen heute in Microsoft Edge gespeichert haben, werden automatisch Vorschläge zum automatischen Ausfüllen angezeigt, mit denen Sie beim Ausfüllen von Formularen Zeit sparen können. In Fällen, in denen beim automatischen Ausfüllen ein Formular fehlt oder wenn Sie Daten in Formularen abrufen möchten, die normalerweise nicht automatisch ausgefüllt sind (z. B. temporäre Formulare), können Sie mithilfe des automatischen Ausfüllens nach Ihren Informationen suchen.

-   **Greifen Sie über ein Flyout in der Menüleiste auf Downloads zu.** Downloads werden in der oberen rechten Ecke mit allen aktiven Downloads an einem Ort angezeigt. Dieses Menü ist leicht zu schließen, sodass Benutzer ununterbrochen weiter surfen und den gesamten Download-Fortschritt direkt über die Symbolleiste überwachen können. [Weitere Informationen](https://techcommunity.microsoft.com/t5/articles/introducing-the-new-downloads-experience/m-p/2111551).

-   **Verbesserungen beim Rendern von Schriftarten.** Ab Microsoft Edge Version 90 haben wir das Rendern von Text verbessert, um die Klarheit zu verbessern und Unschärfe zu reduzieren. Ein Teil der Verbesserungen beim Rendern von Schriftarten wird in der Beta-Version 90 landen, ist jedoch standardmäßig deaktiviert.

- **Kindermodus.** Wir haben die Richtlinie so aktualisiert, dass bei Aktivierung der Richtlinie nicht nur die Familiensicherheit, sondern auch das Feature „Kindermodus“ deaktiviert wird. Weitere Informationen zum Kindermodus finden Sie [hier](https://go.microsoft.com/fwlink/?linkid=2146910)

## <a name="policy-updates"></a>Richtlinienupdates

## <a name="new-policies"></a>Neue Richtlinien

Acht neue Richtlinien wurden hinzugefügt. Laden Sie die aktualisierten administrativen Vorlagen von der [Microsoft Edge Enterprise-Angebotsseite](https://www.microsoft.com/edge/business/download) herunter. Die folgenden neuen Richtlinien wurden hinzugefügt:
-   [ApplicationGuardFavoritesSyncEnabled](/DeployEdge/microsoft-edge-policies#applicationguardfavoritessyncenabled) – Synchronisierung von Application Guard-Favoriten aktiviert
- [ApplicationGuardTrafficIdentificationEnabled](/DeployEdge/microsoft-edge-policies#applicationguardtrafficidentificationenabled) – Application Guard-Netzwerkdatenverkehrsidentifikation
- [ExplicitlyAllowedNetworkPorts](/DeployEdge/microsoft-edge-policies#explicitlyallowednetworkports) – Explizit zugelassene Netzwerkports
- [ImportStartupPageSettings](/DeployEdge/microsoft-edge-policies#importstartuppagesettings) – Import von Startseiteneinstellungen zulassen
- [MathSolverEnabled](/DeployEdge/microsoft-edge-policies#mathsolverenabled) – Benutzer können ein mathematisches Problem mit einer schrittweisen Erläuterung in Microsoft Edge lösen
- [NewTabPageContentEnabled](/DeployEdge/microsoft-edge-policies#newtabpagecontentenabled) – Microsoft News-Inhalt auf der neuen Registerkartenseite zulassen
- [NewTabPageQuickLinksEnabled](/DeployEdge/microsoft-edge-policies#newtabpagequicklinksenabled) – Quicklinks auf der neuen Registerkartenseite zulassen
-   [FetchKeepaliveDurationSecondsOnShutdown](/DeployEdge/microsoft-edge-policies#fetchkeepalivedurationsecondsonshutdown) – Keepalive-Dauer beim Herunterfahren abrufen
-   [ManagedConfigurationPerOrigin](/DeployEdge/microsoft-edge-policies#managedconfigurationperorigin) – Legt verwaltete Konfigurationswerte für Websites auf bestimmte Ursprünge fest
-   [PrintRasterizationMode](/DeployEdge/microsoft-edge-policies#printrasterizationmode) – Druckrasterungsmodus
-   [QuickViewOfficeFilesEnabled](/DeployEdge/microsoft-edge-policies#quickviewofficefilesenabled) : Verwalten der QuickView Office-Dateifunktion in Microsoft Edge
-   [SSLErrorOverrideAllowedForOrigins](/DeployEdge/microsoft-edge-policies#sslerroroverrideallowedfororigins) – Benutzer können von der HTTPS-Warnseite für bestimmte Ursprünge fortfahren
-   [WindowOcclusionEnabled](/DeployEdge/microsoft-edge-policies#windowocclusionenabled) – Fester-Okklusion aktivieren
-   [WindowsHelloForHTTPAuthEnabled](/DeployEdge/microsoft-edge-policies#windowshelloforhttpauthenabled) – Windows Hello für HTTP-Authentifizierung aktiviert

## <a name="deprecated-policies"></a>Veraltete Richtlinien

- [ProactiveAuthEnabled](/DeployEdge/microsoft-edge-policies#proactiveauthenabled) – Proaktive Authentifizierung aktivieren
-   [NativeWindowOcclusionEnabled](/DeployEdge/microsoft-edge-policies#nativewindowocclusionenabled) – Native Fenster-Okklusion aktivieren
-   [SSLVersionMin](/DeployEdge/microsoft-edge-policies#sslversionmin)– Mindestens aktivierte TLS-Version

## <a name="version-89077477-april-14"></a>Version 89.0.774.77: 14. April

> [!Important]
>Dieses Update enthält einen Fix für [CVE-2021-21206](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21206) und [CVE-2021-21220](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21220), der vom Chromium-Team als Exploit gemeldet wurde.  Weitere Informationen finden Sie im [Leitfaden für Sicherheitsupdates](https://msrc.microsoft.com/update-guide).

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

## <a name="version"></a>Version

> [!IMPORTANT]
> Dieses Update enthält [CVE-2021-21166,](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21166) für das laut Chromium-Team ein Exploit im Umlauf ist. Weitere Informationen finden Sie im [Leitfaden für Sicherheitsupdates](https://msrc.microsoft.com/update-guide).

Stabile Kanalsicherheitsupdates sind [hier aufgeführt.](./microsoft-edge-relnotes-security.md#march-4-2021)

### <a name="resolved-issues"></a>Gelöste Probleme

- **Aktualisierungen und Korrekturen von Taskleisten- und Startmenü-Verknüpfungen:**
  - Wenn Sie mit der rechten Maustaste auf die Microsoft Edge-Verknüpfung im Startmenü klicken, wird jetzt die Option zum Entfernen von Microsoft Edge aus der Taskleiste korrekt angezeigt, wenn es angeheftet ist.
  - Startlayouts, die eine [Taskleistenkonfiguration](/windows/configuration/configure-windows-10-taskbar) zum Anheften von Microsoft Edge an die Taskleiste enthalten, führen nicht mehr dazu, dass eine zweite Microsoft Edge-Verknüpfung an die Taskleiste angeheftet wird.
  - Unternehmen, die Windows-Roaming-Profile verwenden, sehen nicht mehr ein leeres weißes Symbol anstelle des Microsoft Edge-Symbols in der Taskleiste, wenn sich ihre Benutzer bei Windows anmelden.

### <a name="feature-updates"></a>Funktionsupdates

- **Der Kiosk-Modus ermöglicht zusätzliche Sperrfunktionen**. Ab Microsoft Edge Version 89 haben wir zusätzliche Sperrfunktionen im Kioskmodus hinzugefügt, damit Kunden ihre Arbeit produktiver und sicherer erledigen können. [Mehr dazu](microsoft-edge-configure-kiosk-mode.md#kiosk-mode-supported-features).

- **Das Site List Manager-Tool im Enterprise-Modus ist im Browser über die Seite *edge://compat* verfügbar**. Mit diesem Tool können Sie XML-Site-Listen für den Internet Explorer-Modus unter Microsoft Edge erstellen, bearbeiten und exportieren. Sie können den Zugriff auf dieses Tool nach Bedarf über Gruppenrichtlinien aktivieren. [Mehr dazu](./edge-ie-mode-site-list-manager.md).

- **Verbessern der Browserleistung mit ruhenden Registerkarten**. Das Ruhen von Registerkarten verbessert die Browserleistung, indem inaktive Registerkarten in den Ruhezustand versetzt werden, um Systemressourcen wie Speicher und CPU freizugeben, sodass aktive Registerkarten oder andere Anwendungen sie verwenden können. Benutzer können verhindern, dass Websites in den Ruhezustand versetzt werden, und die Zeitspanne konfigurieren, in der eine inaktive Registerkarte in den Ruhezustand versetzt wird. Um die Benutzer in ihrem Fluss zu halten, gibt es auch [Heuristiken](https://techcommunity.microsoft.com/t5/articles/sleeping-tabs-faq/m-p/1705434), die verhindern, dass bestimmte Websites in den Ruhezustand versetzt werden, z. B. Intranetsites. Diese Funktion kann mit Gruppenrichtlinien verwaltet werden.

- **Setzen Sie Ihre Microsoft Edge-Synchronisierungsdaten in der Cloud manuell zurück**. Wir bieten eine Möglichkeit, Ihre Microsoft Edge-Synchronisierungsdaten aus dem Produkt heraus zurückzusetzen. Auf diese Weise wird sichergestellt, dass Ihre Daten aus den Microsoft-Diensten gelöscht werden und bestimmte Produktprobleme behoben werden, für die zuvor ein Support-Ticket erforderlich war.

- **Intelligente Aktivierung von einmaligem Anmelden (Single Sign-On, SSO) für alle Windows Azure Active Directory (Azure AD)-Konten für Benutzer mit einem einzigen Microsoft Edge-Profil ohne Azure AD**.  Aktivieren Sie diese Einstellung automatisch für Benutzer, die von diesem Feature am meisten profitieren können. Wenn ein Benutzer nur über ein Microsoft Edge-Profil verfügt (und es sich nicht um Azure AD oder den Modus für Kinder handelt), wird die Einstellung automatisch aktiviert, sobald Microsoft Edge gestartet wird. Dieser automatische Umschalter wird auch automatisch deaktiviert, wenn sich ein Benutzer später mit einem Azure AD-Konto bei einem anderen Microsoft Edge-Profil anmeldet. Benutzer können ihre Einstellungen für dieses Feature unter **Einstellungen > Profile > Profileinstellungen > Einmaliges Anmelden für Geschäfts-, Schul- oder Uniwebsites mithilfe dieses Profils zulassen** manuell aktualisieren.

- **Verbesserungen bei der Textauswahl in PDF-Dokumenten**. Benutzer erhalten eine reibungslosere und konsistentere Textauswahl für PDF-Dokumente, die ab Version 89 in Microsoft Edge geöffnet werden.

- **Das Feld für das Geburtsdatum wird jetzt beim automatischen Ausfüllen unterstützt**. Heute hilft Ihnen Microsoft Edge, Zeit und Mühe beim Ausfüllen von Formularen und beim Erstellen von Online-Konten zu sparen, indem Sie Ihre Daten wie Adressen, Namen, Telefonnummern usw. automatisch ausfüllen. Ab Microsoft Edge Version 89 bieten wir Unterstützung für ein anderes Feld, das Sie gespeichert und automatisch ausgefüllt haben können – das Geburtsdatum. Sie können diese Informationen jederzeit in Ihren Profileinstellungen anzeigen, bearbeiten und löschen.

### <a name="policy-updates"></a>Richtlinienupdates

#### <a name="new-policies"></a>Neue Richtlinien

Es wurden sieben neue Richtlinien hinzugefügt. Laden Sie die aktualisierten administrativen Vorlagen von der [Microsoft Edge Enterprise-Angebotsseite](https://www.microsoft.com/edge/business/download) herunter. Die folgenden neuen Richtlinien wurden hinzugefügt.

- [BrowsingDataLifetime](./microsoft-edge-policies.md#browsingdatalifetime) – Durchsuchen der Einstellungen für die Lebensdauer von Daten
- [MAMEnabled](./microsoft-edge-policies.md#mamenabled) – Mobile App Management aktiviert
- [DefinePreferredLanguages](./microsoft-edge-policies.md#definepreferredlanguages) – Definiert eine geordnete Liste der bevorzugten Sprachen, in denen Websites angezeigt werden sollen, wenn die Website die Sprache unterstützt
- [ShowRecommendationsEnabled](./microsoft-edge-policies.md#showrecommendationsenabled) – Zulassen von Empfehlungen und Werbebenachrichtigungen von Microsoft Edge
- [PrintingAllowedBackgroundGraphicsModes](./microsoft-edge-policies.md#printingallowedbackgroundgraphicsmodes) – Einschränken des Druckmodus für Hintergrundgrafiken
- [PrintingBackgroundGraphicsDefault](./microsoft-edge-policies.md#printingbackgroundgraphicsdefault)– Standard-Druckmodus für Hintergrundgrafiken
- [SmartActionsBlockList](./microsoft-edge-policies.md#smartactionsblocklist)– Blockieren der intelligenten Aktionen für eine Liste von Diensten

#### <a name="obsoleted-policies"></a>Veraltete Richtlinie

Die folgenden Richtlinien sind veraltet.

- [ForceLegacyDefaultReferrerPolicy](./microsoft-edge-policies.md#forcelegacydefaultreferrerpolicy): Verwenden Sie die standardmäßige Verweiserrichtlinie „kein Verweiser beim Downgrade“
- [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) – Aktivieren Sie die Berichterstellung für Nutzung und Absturz
- [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices) – Senden von Site-Informationen, um die Microsoft-Dienste zu verbessern

<!-- end major 89 -->

## <a name="version-88070581-february-25"></a>Version 88.0.705.81: 25. Februar

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-88070574-february-17"></a>Version 88.0.705.74: 17. Februar

Stabile Kanalsicherheitsupdates sind [hier aufgeführt.](./microsoft-edge-relnotes-security.md#february-17-2021)

## <a name="version-88070568-february-11"></a>Version 88.0.705.68: 11. Februar

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-88070563-february-5"></a>Version 88.0.705.63: 5. Februar

> [!IMPORTANT]
> Dieses Update enthält [CVE-2021-21148,](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21148) für das laut Chromium-Team ein Exploit im Umlauf ist.

Stabile Kanalsicherheitsupdates sind [hier aufgeführt.](./microsoft-edge-relnotes-security.md#february-5-2021)

## <a name="version-88070562-february-4"></a>Version 88.0.705.62: 4. Februar

Stabile Kanalsicherheitsupdates sind [hier aufgeführt.](./microsoft-edge-relnotes-security.md#february-4-2021)

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-88070556-january-28"></a>Version 88.0.705.56: 28. Januar

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-88070553-january-26"></a>Version 88.0.705.53: 26. Januar

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-88070550-january-21"></a>Version 88.0.705.50: 21. Januar

Stabile Kanalsicherheitsupdates sind [hier aufgeführt.](./microsoft-edge-relnotes-security.md#january-21-2021)

<!--- begin major 88  --->
### <a name="feature-updates"></a>Funktionsupdates

- **Abschreibungen:**

  - Veraltete Unterstützung für das FTP-Protokoll. Die Unterstützung für das ältere FTP-Protokoll wurde von Microsoft Edge entfernt. Der Versuch, zu einer FTP-Verbindung zu navigieren, führt dazu, dass der Browser das Betriebssystem anweist, eine externe Anwendung zu öffnen, um die FTP-Verbindung zu verarbeiten. Alternativ können IT-Administratoren Microsoft Edge so konfigurieren, dass der IE-Modus für Sites verwendet wird, die auf dem FTP-Protokoll basieren.
  - Die Adobe Flash-Unterstützung wird entfernt. Ab Microsoft Edge Beta Version 88 werden die Adobe Flash-Funktionen und die Unterstützung entfernt. Weitere Informationen: [Update auf Adobe Flash Player Ende der Unterstützung – Microsoft Edge-Blog (windows.com)](https://blogs.windows.com/msedgedev/2020/09/04/update-adobe-flash-end-support/)

- **Authentifizierung:**

  - Einmaliges Anmelden (SSO, Single Sign On) ist jetzt für Azure Active Directory-Konten (Azure AD) und Microsoft-Konto (MSA) unter Windows auf niedrigerer Ebene verfügbar. Ein Benutzer, der bei Microsoft Edge unter Microsoft Windows auf niedrigerer Ebene (7, 8.1) angemeldet ist, wird jetzt automatisch bei Websites angemeldet, die so konfiguriert sind, dass sie eine einmalige Anmeldung mit Geschäfts- und Microsoft-Konten ermöglichen (z. B. bing.com, office.com, msn.com, outlook.com).<br>Hinweis: Ein Benutzer muss sich möglicherweise abmelden und dann erneut anmelden, wenn er sich in einer Version vor Microsoft Edge 88 bei Microsoft Edge angemeldet hat, um diese Funktion nutzen zu können.
  
  - Single Sign-On (SSO) auf Geschäftswebsites mit beliebigen Windows Azure Active Directory (Azure AD)-Konten auf dem System in Nicht-Azure AD-Microsoft Edge-Profilen. Dieses Feature kann für jedes Profil aktiviert werden, das nicht mit einem Geschäfts-/Schulkonto angemeldet ist und nicht Gast oder Privat ist und die Verwendung eines beliebigen angemeldeten Geschäfts-/Schulkontos auf dem Betriebssystem mit diesem Profil zulässt. Dieses Feature kann in **Einstellungen** > **Profile** > **Profileinstellungen** > **Single Sign-on für Geschäfts- und Schulwebsites mit diesem Profil erlauben** konfiguriert werden.
  
    > [!NOTE]
    > „Single Sign-On (SSO) für alle Windows-Konten, die das Microsoft Edge-Profil verwenden" ist eine Aktualisierung für die Versionshinweise vom 21. Januar.

- **Kioskmodus-Option zum Beenden der Sitzung**. Die Schaltfläche „Sitzung beenden“ ist jetzt im öffentlichen Browsing im Kioskmodus verfügbar. Diese Funktion stellt sicher, dass Browserdaten und -einstellungen gelöscht werden, wenn Microsoft Edge geschlossen wird. Weitere Informationen zu den Funktionen und der Roadmap des Kioskmodus finden Sie unter [Konfigurieren des Microsoft Edge-Kioskmodus](./microsoft-edge-configure-kiosk-mode.md).

- **Sicherheit und Datenschutz:**

  - Benachrichtigungen werden generiert, wenn das Kennwort eines Benutzers in einem Onlineleck gefunden wird. Benutzerkennwörter werden gegen ein Verzeichnis bekannter Anmeldeinformationen überprüft und geben dem Benutzer eine Warnung zurück, wenn eine Übereinstimmung gefunden wird. Um die Sicherheit und den Datenschutz zu gewährleisten, werden Benutzerkennwörter gehashed und verschlüsselt, wenn Sie mit der Datenbank der durchgesickerten Anmeldeinformationen abgeglichen werden.
  - Aktualisieren Sie gemischte Inhalte automatisch. Über HTTPS gelieferte sichere Seiten können Referenzbilder enthalten, die über nicht sicheres HTTP bereitgestellt werden. Um den Datenschutz und die Sicherheit in Microsoft Edge 88 zu verbessern, werden diese Bilder stattdessen über HTTPS abgerufen. Wenn das Bild nicht über HTTPS verfügbar ist, wird es nicht geladen.
  - Anzeigen von Site-Berechtigungen nach Site und nach letzten Aktivitäten. Ab Microsoft Edge 88 können Benutzer Site-Berechtigungen einfacher verwalten. Sie können Berechtigungen nach Website und nicht nur nach Berechtigungstyp anzeigen. Darüber hinaus haben wir einen Abschnitt mit den letzten Aktivitäten hinzugefügt, in dem ein Benutzer alle letzten Änderungen an seinen Websiteberechtigungen anzeigt.
  - Verbesserte Steuerelemente für Browser-Cookies. Ab Microsoft Edge 88 können Benutzer Cookies von Drittanbietern löschen, ohne dass dies Auswirkungen auf Cookies von Drittanbietern hat. Benutzer können ihre Cookies auch nach Erst- oder Drittanbietern filtern und nach Name, Anzahl der Cookies und der Menge der gespeicherten und zuletzt geänderten Daten sortieren.

- **Kennwörter:**

  - Kennwortgenerator. Microsoft Edge bietet einen integrierten Generator für starke Kennwörter an, den Sie beim Erstellen eines neuen Kontos oder beim Ändern eines vorhandenen Kennworts verwenden können. Suchen Sie einfach nach dem vom Browser vorgeschlagenen Kennwort-Dropdown im Kennwortfeld. Wenn diese Option ausgewählt ist, wird sie Kennwörter automatisch im Browser speichern und geräteübergreifend synchronisieren, damit Sie diese in Zukunft einfach verwenden können.
  - Kennwortüberwachung. Wenn eines Ihrer im Browser gespeicherten Kennwörter mit denen in der Liste der kompromittierten Anmeldeinformationen übereinstimmt, benachrichtigt Microsoft Edge Sie und fordert Sie auf, Ihr Kennwort zu aktualisieren. Die Kennwortüberwachung prüft in Ihrem Auftrag auf Übereinstimmungen und ist standardmäßig aktiviert.
  - Kennwort bearbeiten. Sie können ihre gespeicherten Kennwörter jetzt direkt in den Microsoft Edge-Einstellungen bearbeiten. Jedes Mal, wenn ein Kennwort außerhalb von Microsoft Edge aktualisiert wurde, können Sie das gespeicherte ältere Kennwort ganz einfach durch das neue ersetzen, indem Sie den gespeicherten Eintrag in den Einstellungen bearbeiten. 

- **Verbessern der Startgeschwindigkeit von Microsoft Edge mit der Startup-Boost**. Um die Startgeschwindigkeit von Microsoft Edge zu verbessern, haben wir eine Funktion namens Startup-Boost entwickelt. Durch den Startup-Boost wird der Start von Microsoft Edge beschleunigt, da Microsoft Edge im Hintergrund ausgeführt werden kann. Hinweis: Diese Funktion ist auf eine zufällig ausgewählte Gruppe von Benutzern beschränkt, die das Experimentieren aktiviert haben. Diese Benutzer geben dem Feature-Team Feedback.

- **Produktivität:**

  - Verbessern Sie die Produktivität und das Multitasking mit vertikalen Registerkarten. Wenn die Anzahl der horizontalen Registerkarten zunimmt, werden die Site-Titel abgeschnitten und die Steuerelemente der Registerkarten gehen verloren, wenn die einzelnen Registerkarten verkleinert werden. Dies unterbricht den Benutzerworkflow, da sie mehr Zeit damit verbringen, ihre Registerkarten zu finden, zu wechseln und zu verwalten, und weniger Zeit für die jeweilige Aufgabe. Mit vertikalen Registerkarten können Benutzer ihre Registerkarten zur Seite verschieben. Vertikal ausgerichtete Symbole und längere Site-Titel erleichtern das schnelle Scannen, Identifizieren und Wechseln zu der Registerkarte, die sie öffnen möchten.
  - Das Feld für das Geburtsdatum wird automatisch ausgefüllt. Microsoft Edge spart bereits Zeit und Mühe beim Ausfüllen von Formularen und beim Erstellen von Online-Konten, indem Benutzerdaten wie Adressen, Namen, Telefonnummern usw. automatisch ausgefüllt werden. Microsoft Edge unterstützt jetzt das Feld für das Geburtsdatum, das Benutzer speichern und automatisch ausfüllen können. Ein Benutzer kann diese Informationen jederzeit in seinen Profileinstellungen anzeigen, bearbeiten und löschen.
  - Verbesserungen an Vor kurzem im Verlauf geschlossen. „Vor kurzem geschlossen“ behält jetzt die letzten 25 Registerkarten und Fenster aus früheren Browsersitzungen und nicht nur aus der vorherigen Sitzung bei. Benutzer können in der neuen Verlaufserfahrung die Option „Zuletzt geschlossen“ auswählen, um alle geöffneten Registerkarten anzuzeigen.
  - Das Feature "Ihr Tag auf einen Blick" ist standardmäßig aktiviert. Beginnend mit Microsoft Edge Version 88 können Informationsdienste von intelligenten Produktivitätsfunktionen auf ihrer „Neue Registerkartenseite (NTP)“ profitieren. Microsoft Edge 87-Benutzern werden diese Erfahrungen innerhalb von zwei Wochen nach der Veröffentlichung von Microsoft Edge 88 auch erhalten. Wir bieten Benutzern, die mit Ihrem Geschäfts- oder Schulkonto angemeldet sind, personalisierte und relevante Inhalte an, die von ihrem M365 Graph unterstützt werden. Benutzer können Ihre "Ihr Tag auf einen Blick"-Module schnell durchsuchen, um Ihre Besprechungen und die aktuelle Arbeit zu überwachen sowie die Anwendungen, die Sie verwenden möchten, schnell zu starten.

- **Verlaufs- und geöffnete Registerkarten-Synchronisierung**. Die Verlaufssynchronisierung und Synchronisierung von geöffneten Registerkarten ist jetzt für Benutzer verfügbar. Das Aktivieren dieses Features hilft Benutzern dort weiterzumachen, wo Sie aufgehört haben, indem Sie ihren Browserverlauf und die geöffneten Registerkarten auf allen ihren Synchronisierungsgeräten zur Verfügung stellen. Wir haben die Synchronisierungs- und Browserverlaufsrichtlinien aktualisiert, sodass die Benutzer jetzt über Microsoft Edge geräteübergreifend verbunden und produktiv sind. [Mehr dazu](https://blogs.windows.com/windowsexperience/2021/01/21/this-year-lets-resolve-to-make-the-most-of-our-time-online-and-better-protect-ourselves-from-online-threats/).

- **PDF:**

  - PDF-Dokumentanzeige in der Buchansicht (zwei Seiten). Ab Microsoft Edge Version 88 können Benutzer PDF-Dokumente auf einer einzelnen Seite oder in der zweiseitigen Buchansicht anzeigen. Um die Ansicht zu ändern, klicken Sie in der Symbolleiste auf die Schaltfläche **Seitenansicht**.
  - Unterstützung für verankerte Textnotizen für PDF-Dateien. Ab Microsoft Edge Version 87 können Benutzer zu jedem Text in PDF-Dateien getippte Textnotizen hinzufügen.

- **Schriftarten:**

  - Browsersymbole werden auf das Fluent-Designsystem aktualisiert. Im Rahmen unserer fortgesetzten Arbeit an Fluent Design im Browser haben wir Änderungen vorgenommen, um die Symbole näher am neuen Microsoft-Symbolsystem auszurichten. Diese Änderungen wirken sich auf viele unserer High-Touch-Benutzeroberflächen aus, einschließlich Registerkarten, Adressleiste sowie Navigations- und Wegfindungssymbole in unseren verschiedenen Menüs.
  - Verbesserte Schriftwiedergabe. Die Textwiedergabe wurde verbessert, um die Übersichtlichkeit zu verbessern und Unschärfe zu verringern.

### <a name="policy-updates"></a>Richtlinienupdates

#### <a name="new-policies"></a>Neue Richtlinien

Achtzehn neue Richtlinien wurden hinzugefügt. Laden Sie die aktualisierten administrativen Vorlagen von der [Microsoft Edge Enterprise-Angebotsseite](https://www.microsoft.com/edge/business/download) herunter. Die folgenden neuen Richtlinien wurden hinzugefügt.

- [BasicAuthOverHttpEnabled](./microsoft-edge-policies.md#basicauthoverhttpenabled) – Lassen Sie die Standardauthentifizierung für HTTP zu.
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
- [TargetBlankImpliesNoOpener](./microsoft-edge-policies.md#targetblankimpliesnoopener) – Legen Sie "window.opener" nicht für Links fest, die auf _blank abzielen.
- [UpdatePolicyOverride](./microsoft-edge-policies.md#updatepolicyoverride) – Gibt an, wie Microsoft Edge Update verfügbare Updates von Microsoft Edge verarbeitet. 
- [VerticalTabsAllowed](./microsoft-edge-policies.md#verticaltabsallowed) – Konfiguriert die Verfügbarkeit eines vertikalen Layouts für Registerkarten an der Seite des Browsers.
- [WebRtcAllowLegacyTLSProtocols](./microsoft-edge-policies.md#webrtcallowlegacytlsprotocols) – Ermöglichen Sie ein älteres TLS/DTLS-Downgrade in WebRTC.
- [WebWidgetAllowed](./microsoft-edge-policies.md#webwidgetallowed) – Aktivieren Sie das Web-Widget.
- [WebWidgetIsEnabledOnStartup](./microsoft-edge-policies.md#webwidgetisenabledonstartup) – Lassen Sie das Web-Widget beim Start von Windows zu.

#### <a name="deprecated-policies"></a>Veraltete Richtlinien

- [ProactiveAuthEnabled](./microsoft-edge-policies.md#proactiveauthenabled) – Aktivieren Sie die proaktive Authentifizierung.
- [ProxyBypassList](./microsoft-edge-policies.md#proxybypasslist) – Konfigurieren Sie die Proxy-Umgehungsregeln.
- [ProxyMode](./microsoft-edge-policies.md#proxymode) – Konfigurieren Sie die Proxy-Server-Einstellungen.
- [ProxyPacUrl](./microsoft-edge-policies.md#proxypacurl) – Legen Sie die URL der Proxy .pac-Datei fest.
- [Proxyserver](./microsoft-edge-policies.md#proxyserver) – Konfigurieren Sie die Adresse oder URL des Proxyservers.
- [WebDriverOverridesIncompatiblePolicies](./microsoft-edge-policies.md#webdriveroverridesincompatiblepolicies) – Erlauben Sie WebDriver, inkompatible Richtlinien zu überschreiben.

### <a name="obsoleted-policies"></a>Abgeschaffte Richtlinien

- [AllowPopupsDuringPageUnload](./microsoft-edge-policies.md#allowpopupsduringpageunload) – Ermöglicht einer Seite das Anzeigen von Popups während der Entladung.
- [DefaultPluginsSetting](./microsoft-edge-policies.md#defaultpluginssetting) – Standardeinstellung für Adobe Flash.
- [PluginsAllowedForUrls](./microsoft-edge-policies.md#pluginsallowedforurls) – Lassen Sie das Adobe Flash-Plug-In auf bestimmten Websites zu.
- [PluginsBlockedForUrls](./microsoft-edge-policies.md#pluginsblockedforurls) – Blockieren Sie das Adobe Flash-Plug-in auf bestimmten Websites.
- [RunAllFlashInAllowMode](./microsoft-edge-policies.md#runallflashinallowmode) – Erweitern der Adobe Flash-Inhaltseinstellung auf alle Inhalte.
<!--- end major 88  --->
## <a name="version-87066475-january-7"></a>Version 87.0.664.75: 7. Januar

Stabile Kanalsicherheitsupdates sind [hier aufgeführt.](./microsoft-edge-relnotes-security.md#january-7-2021)

## <a name="version-87066466-december-17"></a>Version 87.0.664.66: 17. Dezember

Verschiedene Bugs und Leistungsprobleme wurden behoben.

## <a name="version-87066460-december-10"></a>Version 87.0.664.60: 10. Dezember

Verschiedene Bugs und Leistungsprobleme wurden behoben.

## <a name="version-87066457-december-7"></a>Version 87.0.664.57: 7. Dezember

Verschiedene Fehler und Leistungsprobleme wurden behoben. Stabile Kanalsicherheitsupdates sind [hier aufgeführt.](./microsoft-edge-relnotes-security.md#december-7-2020)

## <a name="version-87066455-december-3"></a>Version 87.0.664.55: 3. Dezember

Verschiedene Bugs und Leistungsprobleme wurden behoben. Das folgende Feature wurde mit diesem Release aktualisiert.

- **Shopping ist standardmäßig aktiviert**. Ab Microsoft Edge, Version 87, können Unternehmensbenutzer von Shopping-Features in Microsoft Edge profitieren. Mit den Shopping-Features hilft Microsoft Edge Benutzern, beim Onlineshopping Gutscheine und bessere Preise zu finden. (Die Coupon-Erfahrung wurde mit Stable Version 87.0.664.41 veröffentlicht). Die Preisvergleich-Erfahrung ist jetzt mit diesem Update verfügbar. Dieses Feature kann mithilfe der [EdgeShoppingAssistantEnabled](./microsoft-edge-policies.md#edgeshoppingassistantenabled)-Richtlinie konfiguriert werden. Schauen Sie sich unseren [Blog](https://blogs.windows.com/windowsexperience/2020/11/19/finish-up-that-holiday-shopping-with-new-features-from-microsoft-edge-and-bing/) an, und [erfahren Sie mehr](/microsoft-edge/privacy-whitepaper#shopping) über Microsoft Shopping.

## <a name="version-87066452-november-30"></a>Version 87.0.664.52: 30. November

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-87066447-november-23"></a>Version 87.0.664.47: vom 23. November

Verschiedene Fehler und Leistungsprobleme wurden behoben.

<!-- begin major 87 --->
## <a name="version-87066441-november-19"></a>Version 87.0.664.41: 19. November

Stabile Kanalsicherheitsupdates sind [hier aufgeführt.](./microsoft-edge-relnotes-security.md#november-19-2020)

### <a name="feature-updates"></a>Funktionsupdates

- **Automatisches Umleiten von inkompatiblen Websites aus Internet Explorer zu Microsoft Edge**. Ab dem Microsoft Edge 87 Stable-Update werden öffentliche Websites, die eine Inkompatibilitätsmeldung in Internet Explorer anzeigen, automatisch an Microsoft Edge umgeleitet. Weitere Informationen hierzu und zum Konfigurieren dieser Umgebung finden Sie unter [Umleiten von nicht kompatiblen Websites](./edge-learnmore-neededge.md).

- **Datenschutzfeatures des Kioskmodus aktiviert**. Ab Microsoft Edge, Version 87, werden Kioskmodus-Features aktiviert, die Unternehmen im Zusammenhang mit dem Datenschutz für Benutzerdaten helfen. Diese Features ermöglichen es beispielsweise, dass die Benutzerdaten beim Beenden gelöscht werden, dass heruntergeladene Dateien gelöscht werden und dass die konfigurierte Startumgebung nach einer festgelegten Leerlaufzeitspanne zurückgesetzt wird. Informieren Sie sich genauer zum [Konfigurieren des Microsoft Edge-Kioskmodus](./microsoft-edge-configure-kiosk-mode.md).

- **Shopping-Features standardmäßig aktiviert**. Ab Microsoft Edge, Version 87, können Unternehmensbenutzer auch von Shopping-Features in Microsoft Edge profitieren. Mit den Shopping-Features hilft Microsoft Edge Benutzern, beim Onlineshopping Gutscheine und bessere Preise zu finden. Die Couponumgebung ist mit diesem Update verfügbar, und der Preisvergleich wird in den bevorstehenden Updates für Microsoft Edge 87 veröffentlicht. Dieses Feature kann über die [EdgeShoppingAssistantEnabled](./microsoft-edge-policies.md#edgeshoppingassistantenabled)-Richtlinie konfiguriert werden. Schauen Sie sich unseren [Blog](https://blogs.windows.com/windowsexperience/2020/11/19/finish-up-that-holiday-shopping-with-new-features-from-microsoft-edge-and-bing/) an, und [erfahren Sie mehr](/microsoft-edge/privacy-whitepaper#shopping) über Microsoft Shopping.

- **ClickOnce-Bereitstellung standardmäßig aktiviert**. ClickOnce ist in Microsoft Edge 87 standardmäßig aktiviert, wodurch die Hindernisse für Unternehmen reduziert werden, die Software bereitstellen und mit dem Browserverhalten der Vorgängerversion von Microsoft Edge besser übereinstimmen möchten. Ab Microsoft Edge 87 gibt der Status „Nicht konfiguriert“ der Richtlinie „ClickOnceEnabled“ den neuen standardmäßigen ClickOnce-Status „Aktiviert“ (im Vergleich zum vorherigen Standardstatus „Deaktiviert“) wieder.

- **Auf der Enterprise-Seite „Neue Registerkarte” (New Tab Page, NTP) wird Produktivität in anpassbare, arbeitsrelevante Feedinhalte integriert**. Im Enterprise-NTP-Bereich werden die Office 365-Produktivitätsseite, die wir den mit ihrem Geschäfts-, Schul-oder Unikonto angemeldeten Benutzern bieten, mit personalisierten, arbeitsrelevanten Unternehmens- und Branchenfeeds zusammengeführt, die auf einer einzigen Seite organisiert sind. Benutzer können die vertrauten Office 365-Inhalte und Microsoft Search for Business erkennen, das von Bing unterstützt wird. Darüber hinaus können sie "Mein Feed" leicht anpassen, indem sie aus den verfügbaren Inhalten und Modulen für ihre Organisation die für sie relevantesten auswählen. IT-Administratoren können die Einstellungen für Newsfeeds für Ihre Organisation, einschließlich der ausgewählten Branche für die Microsoft Edge-Seite "Neue Registerkarte", über das Microsoft 365 Admin Center steuern. [Weitere Informationen](https://blogs.windows.com/msedgedev/2020/10/29/enterprise-new-tab-page-my-feed/)

- **Datenschutz und Sicherheit:**

  - Unterstützung von TLS-Tokenbindung für mit Richtlinien konfigurierte Websites. Die TLS-Tokenbindung hilft bei der Verhinderung von Angriffen zum Diebstahl von Token, um sicherzustellen, dass Cookies nur auf dem Gerät wiederverwendet werden können, auf dem sie ursprünglich festgelegt wurden. Die Verwendung der TLS-Tokenbindung erfordert es, dass die Richtlinie [AllowTokenBindingForUrls](./microsoft-edge-policies.md#allowtokenbindingforurls) festgelegt wurde und dass die aufgeführten Websites dieses Feature unterstützen.

- **Tastaturunterstützung für Textmarker in PDF-Dateien**. Benutzer können jeden beliebigen Text in einer PDF-Datei mithilfe ihrer Tastatur hervorheben.

- **Drucken:**

  - Wählen Sie die Seite aus, die beim beidseitigen Drucken gedreht werden soll. Benutzer können auswählen, ob ein Blatt beim beidseitigen Drucken auf die lange Seite (Querformat) oder die kurze Seite (Hochformat) gedreht werden soll.
  - Wählen Sie den Druckmodus „Rasterung“ für das Unternehmen aus. Steuern Sie, wie Microsoft Edge auf einem Nicht-PostScript-Drucker unter Windows druckt. Manchmal müssen Druckaufträge bei Nicht-PostScript-Druckern gerastert werden, damit korrekt gedruckt wird. Die Druckoptionen sind „Full" (Vollständig) und „Fast“ (Schnell).

### <a name="policy-updates"></a>Richtlinienupdates

#### <a name="new-policies"></a>Neue Richtlinien

Es wurden zehn neue Richtlinien hinzugefügt. Laden Sie die aktualisierten administrativen Vorlagen von der [Microsoft Edge Enterprise-Angebotsseite](https://www.microsoft.com/edge/business/download) herunter. Die folgenden neuen Richtlinien wurden hinzugefügt.

- [ConfigureFriendlyURLFormat](./microsoft-edge-policies.md#configurefriendlyurlformat) – Zum Konfigurieren des Standardformats für das Einfügen von URLs, die aus Microsoft Edge kopiert wurden, und zum Ermitteln, ob Benutzern weitere Formate zur Verfügung stehen.
- [EdgeShoppingAssistantEnabled](./microsoft-edge-policies.md#edgeshoppingassistantenabled) – Shopping in Microsoft Edge aktiviert.
- [HideInternetExplorerRedirectUXForIncompatibleSitesEnabled](./microsoft-edge-policies.md#hideinternetexplorerredirectuxforincompatiblesitesenabled) – Zum Ausblenden des Dialogfelds für einmalige Umleitung und des Banners in Microsoft Edge.
- [KioskAddressBarEditingEnabled](./microsoft-edge-policies.md#kioskaddressbareditingenabled) – Zum Konfigurieren der Adressleistenbearbeitung für Benutzerfreundlichkeit beim öffentlichen Surfen im Kioskmodus.
- [KioskDeleteDownloadsOnExit](./microsoft-edge-policies.md#kioskdeletedownloadsonexit) – Zum Löschen von während einer Kiosksitzung heruntergeladenen Dateien, wenn Microsoft Edge geschlossen wird.
- [PasswordRevealEnabled](./microsoft-edge-policies.md#passwordrevealenabled) – Zum Aktivieren der Schaltfläche für Kennwortanzeige.
- [RedirectSitesFromInternetExplorerPreventBHOInstall](./microsoft-edge-policies.md#redirectsitesfrominternetexplorerpreventbhoinstall) – Zum Verhindern, dass das Browserhilfsobjekt (BHO) installiert wird, um inkompatible Websites von Internet Explorer zu Microsoft Edge umzuleiten.
- [RedirectSitesFromInternetExplorerRedirectMode](./microsoft-edge-policies.md#redirectsitesfrominternetexplorerredirectmode) – Zum Umleiten inkompatibler Websites von Internet Explorer zu Microsoft Edge.
- [SpeechRecognitionEnabled](./microsoft-edge-policies.md#speechrecognitionenabled) – Zum Konfigurieren der Spracherkennung.
- [WebCaptureEnabled](./microsoft-edge-policies.md#webcaptureenabled) – Zum Aktivieren des Features "Weberfassung" in Microsoft Edge.

#### <a name="deprecated-policy"></a>Veraltete Richtlinie

[NewTabPageSetFeedType](./microsoft-edge-policies.md#newtabpagesetfeedtype) – Zum Konfigurieren der Microsoft Edge-Oberfläche für neue Registerkartenseiten.

#### <a name="obsoleted-policy"></a>Veraltete Richtlinie

[EnableDeprecatedWebPlatformFeatures](./microsoft-edge-policies.md#enabledeprecatedwebplatformfeatures) – Zum Reaktivieren veralteter Features für Webplattformen für einen begrenzten Zeitraum.

<!-- end major 87 -->

## <a name="version-86062269-november-13"></a>Version 86.0.622.69: 13. November

> [!IMPORTANT]
> Dieses Update enthält [CVE-2020-16013](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-16013) und [CVE-2020-16017](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-16017), wovon laut Chromium-Team ein Exploit im Umlauf ist.

Stabile Kanalsicherheitsupdates sind [hier aufgeführt.](./microsoft-edge-relnotes-security.md#november-13-2020)

## <a name="version-86062268-november-11"></a>Version 86.0.622.68: 11. November

Sicherheitsupdates für stabile Kanäle sind hier [aufgeführt.](./microsoft-edge-relnotes-security.md#november-11-2020)

## <a name="version-86062263-november-4"></a>Version 86.0.622.63: 4. November

> [!IMPORTANT]
> Dieses Update enthält [CVE-2020-16009](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-16009), wovon laut Chromium-Team ein Exploit im Umlauf ist.

Stabile Kanalsicherheitsupdates sind [hier aufgeführt.](./microsoft-edge-relnotes-security.md#november-4-2020)

## <a name="version-86062261-november-2"></a>Version 86.0.622.61: 2. November

Verschiedene Bugs und Leistungsprobleme wurden behoben.

## <a name="version-86062258-october-29"></a>Version 86.0.622.58: 29. Oktober

Verschiedene Bugs und Leistungsprobleme wurden behoben.

## <a name="version-86062256-october-27"></a>Version 86.0.622.56: 27. Oktober

Verschiedene Bugs und Leistungsprobleme wurden behoben.

## <a name="version-86062251-october-22"></a>Version 86.0.622.51: 22. Oktober

Sicherheitsupdates für stabile Kanäle sind hier [aufgeführt.](./microsoft-edge-relnotes-security.md#october-22-2020)

## <a name="version-86062248-october-20"></a>Version 86.0.622.48: 20. Oktober

Verschiedene Bugs und Leistungsprobleme wurden behoben.

## <a name="version-86062243-october-15"></a>Version 86.0.622.43: 15. Oktober

Verschiedene Bugs und Leistungsprobleme wurden behoben.

## <a name="version-86062238-october-9"></a>Version 86.0.622.38: 9. Oktober

Sicherheitsupdates werden [hier](./microsoft-edge-relnotes-security.md#october-9-2020) aufgelistet.

### <a name="feature-updates"></a>Funktionsupdates

* **Zurücksetzen zur vorherigen Microsoft Edge-Version.** Mit der Rollback-Funktion können Administratoren auf eine Ihnen bekannte gute Version von Microsoft Edge zurückgreifen, wenn ein Problem in der neuesten Version von Microsoft Edge auftritt. **Hinweis:** Stabile Version 86.0.622.38 ist die erste Version, auf die Sie zurücksetzen können, was bedeutet, dass stabile Version 87 die erste Version ist, von der eine Rücksetzung ausgeführt werden kann. [Weitere Informationen](edge-learnmore-rollback.md).

* **Erzwingen der standardmäßigen Aktivierung der Synchronisierung im gesamten Unternehmen.**  Administratoren können die Synchronisierung für Azure Active Directory-Konten (Azure AD) standardmäßig mit der [ForceSync](./microsoft-edge-policies.md#forcesync)-Richtlinie aktivieren.

* **Automatischer Profilwechsel unter Windows 7 und 8.1.** Der zurzeit in Microsoft Edge unter Windows 10 verfügbare automatische Profilwechsel wird auf Vorgängerversionen (Windows 7 und 8.1) erweitert. Weitere Informationen finden Sie im Blogbeitrag [Automatischer Profilwechsel](https://blogs.windows.com/msedgedev/2020/04/30/automatic-profile-switching/).

* **"SameSite=Lax" für Cookies (Standard)**. Zur Verbesserung der Websicherheit und des Datenschutzes verwenden Cookies jetzt standardmäßig die [SameSite = Lax](https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie/SameSite)-Behandlung. Dies bedeutet, dass Cookies nur in einem Erstanbieterkontext gesendet werden und bei an Dritte gesendeten Anforderungen weggelassen werden. Diese Änderung kann Auswirkungen auf die Kompatibilität von Websites haben, die Cookies von Drittanbietern benötigen, damit Ressourcen die korrekt funktionieren. Um solche Cookies zuzulassen, können Webentwickler Cookies markieren, die aus Drittanbieterkontext gesetzt und an Drittanbieterkontext gesendet werden sollen, indem sie beim Setzen des Cookies explizit die Attribute `SameSite=none` und `Secure` hinzufügen. Unternehmen, die bestimmte Sites von dieser Änderung ausnehmen möchten, können dies mit der Richtlinie [LegacySameSiteCookieBehaviorEnabledForDomainList](./microsoft-edge-policies.md#legacysamesitecookiebehaviorenabledfordomainlist) tun oder die Änderung für alle Sites mit der Richtlinie [LegacySameSiteCookieBehaviorEnabled](./microsoft-edge-policies.md#legacysamesitecookiebehaviorenabled) ablehnen.

* **Entfernen der Cache-API für HTML5-Anwendungen.**  Beginnend mit der Microsoft Edge-Version 86, wird die veraltete Anwendungs-Cache-API, die die Offline-Nutzung von Webseiten ermöglicht, von Microsoft Edge entfernt. Webentwickler sollten sich die [WebDev-Dokumentation](https://web.dev/appcache-removal/) ansehen, um Informationen zum Ersetzen der Anwendungs-Cache-API durch Service Worker zu erhalten.  Wichtig: Sie können einen [AppCache OriginTrial-Token](https://developers.chrome.com/origintrials/#/view_trial/1776670052997660673) anfordern, der es Websites ermöglicht, die veraltete Anwendungs-Cache-API weiterhin bis zur Microsoft Edge-Version 90 zu verwenden.

* **Datenschutz und Sicherheit:**

  * Ersetzen der Richtlinien [MetricsReportingEnabled](/DeployEdge/microsoft-edge-policies#metricsreportingenabled) und [SendSiteInformationToImproveServices](/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices) für Vorgängerversionen von Windows und macOS. Diese Richtlinien sind in der Microsoft Edge-Version 86 veraltet und werden in der Microsoft Edge-Version 89 überholt sein.<br>
Diese Richtlinien werden ersetzt durch [Telemetrie zulassen](/windows/privacy/configure-windows-diagnostic-data-in-your-organization) unter Windows 10 sowie die neue [DiagnosticData](./microsoft-edge-policies.md#diagnosticdata)-Richtlinie für alle anderen Plattformen. Dadurch können Benutzer die Diagnosedaten verwalten, die an Microsoft für Windows 7, 8, 8.1 und macOS gesendet werden.
  * Unterstützung für sicheres DNS (DNS-over-HTTPS).  Ab der Microsoft Edge-Version 86 stehen Einstellungen zum Steuern des sicheren DNS auf nicht verwalteten Geräten zur Verfügung. Diese Einstellungen sind für Benutzer auf verwalteten Geräten nicht zugänglich, aber IT-Administratoren können sicheres DNS aktivieren oder deaktivieren, indem Sie die Gruppenrichtlinie [dnsoverhttpsmode](./microsoft-edge-policies.md#dnsoverhttpsmode) verwenden.

* **Internet Explorer-Modus:** Ermöglichen Sie Benutzern, die Microsoft Edge-Benutzeroberfläche zum Testen von Websites im Internet Explorer-Modus zu verwenden. Beginnend mit der Microsoft Edge-Version 86 können Administratoren eine Benutzeroberflächenoption für Ihre Benutzer aktivieren, um eine Registerkarte im Internet Explorer-Modus zu Testzwecken oder als Notlösung zu laden, bis Websites zur XML-Websiteliste hinzugefügt werden.

* **PDF-Updates:**

  * Inhaltsverzeichnis für PDF-Dokumente. Ab Version 86 hat Microsoft Edge Unterstützung für das Inhaltsverzeichnis hinzugefügt, das es Benutzern ermöglicht, einfach durch PDF-Dokumente zu navigieren.
  * Zugriff auf alle PDF-Funktionalitäten auf Bildschirmen mit kleinem Formfaktor. Zugriff auf alle Funktionen des Microsoft Edge PDF-Readers auf Geräten mit kleinen Bildschirmgrößen.
  * Stiftunterstützung für Textmarker in PDF-Dateien. Mit diesem Update können Benutzer mit ihrem digitalen Stift Text in PDF-Dateien direkt markieren, so wie sie es auch mit einem physischen Textmarker und Papier tun würden.
  * Verbessertes Scrollen im PDF-Format. Das Scrollen durch lange PDF-Dokumente kann jetzt ohne Ruckeln erlebt werden.

* **Benutzer sehen Vorschläge zur automatischen Vervollständigung, wenn sie mit der Eingabe einer Suchanfrage auf der Microsoft Edge Add-ons-Website beginnen.** Die automatische Vervollständigung hilft Benutzern, Ihre Suchabfrage schnell zu vervollständigen, ohne die gesamte Zeichenfolge eingeben zu müssen. Dies ist hilfreich, da sich die Benutzer keine korrekten Schreibweisen merken müssen, und Sie können aus den verfügbaren Optionen auswählen, die angezeigt werden.

* **Hinzufügen eines benutzerdefiniertes Bildes zur Seite „Neue Registerkarte“ (New Tab Page, NTP) mithilfe einer Gruppenrichtlinie.** Beginnend mit der Microsoft Edge-Version 86 bietet die NTP die Möglichkeit, das Standardbild durch ein benutzerdefiniertes Bild zu ersetzen. Die Möglichkeit, die Eigenschaften dieses Bilds zu verwalten, wird auch von der Gruppenrichtlinie unterstützt.

* **Anpassen von benutzerdefinierten Tastenkombinationen an VS Code.** Microsoft Edge DevTools unterstützt jetzt die Anpassung von Tastenkombinationen in DevTools mit Ihrem Editor/Ihrer IDE. (In Microsoft Edge 84 wurde die Möglichkeit hinzugefügt, DevTools-Tastenkombinationen mit VS Code abzugleichen).

* **Löschen von Downloads von der Festplatte mithilfe des Download-Managers.** Benutzer sind jetzt in der Lage, die heruntergeladenen Dateien von Ihrer Festplatte zu löschen, ohne den Browser verlassen zu müssen. Die neue Funktion zum Löschen von Downloads befindet sich im Kontextmenü des Downloadverzeichnisses oder der Downloadseite.

### <a name="policy-updates"></a>Richtlinienupdates

#### <a name="new-policies"></a>Neue Richtlinien

Es wurden dreiundzwanzig neue Richtlinien hinzugefügt. Laden Sie die aktualisierten administrativen Vorlagen von der [Microsoft Edge Enterprise Angebotsseite](https://aka.ms/EdgeEnterprise) herunter. Die folgenden neuen Richtlinien wurden hinzugefügt.

- [CollectionsServicesAndExportsBlockList](./microsoft-edge-policies.md#collectionsservicesandexportsblocklist): Blockieren des Zugriffs auf eine bestimmte Liste von Diensten und Exportieren von Zielen in Sammlungen.
- [DefaultFileSystemReadGuardSetting](./microsoft-edge-policies.md#defaultfilesystemreadguardsetting) –⁠ Steuern der Verwendung der Dateisystem-API zum Lesen.
- [DefaultFileSystemWriteGuardSetting](./microsoft-edge-policies.md#defaultfilesystemwriteguardsetting) –⁠ Steuern der Verwendung der Dateisystem-API zum Schreiben.
- [DefaultSensorsSetting](./microsoft-edge-policies.md#defaultsensorssetting): Standardeinstellung für Sensoren.
- [DefaultSerialGuardSetting](./microsoft-edge-policies.md#defaultserialguardsetting): Steuerung der Verwendung der Serial-API.
- [DiagnosticData](./microsoft-edge-policies.md#diagnosticdata) –⁠ Senden der erforderlichen und optionalen Diagnosedaten zur Browsernutzung.
- [EnterpriseModeSiteListManagerAllowed](./microsoft-edge-policies.md#enterprisemodesitelistmanagerallowed): Zugriff auf das Tool Enterprise Mode Site List Manager zulassen.
- [FileSystemReadAskForUrls](./microsoft-edge-policies.md#filesystemreadaskforurls) –⁠ Lesezugriff über die Datei-System-API auf diesen Websites zulassen.
- [FileSystemReadBlockedForUrls](./microsoft-edge-policies.md#filesystemreadblockedforurls) –⁠ Lesezugriff über die Datei-System-API auf diesen Websites blockieren.
- [FileSystemWriteAskForUrls](./microsoft-edge-policies.md#filesystemwriteaskforurls) –⁠ Schreibzugriff auf Dateien und Verzeichnisse auf diesen Websites zulassen.
- [FileSystemWriteBlockedForUrls](./microsoft-edge-policies.md#filesystemwriteblockedforurls) –⁠ Schreibzugriff auf Dateien und Verzeichnisse auf diesen Websites blockieren.
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
- [UserAgentClientHintsEnabled](./microsoft-edge-policies.md#useragentclienthintsenabled): Aktivieren der Funktion User-Agent Client Hints.
- [UserDataSnapshotRetentionLimit](./microsoft-edge-policies.md#userdatasnapshotretentionlimit): Schränkt die Anzahl der Benutzerdaten-Momentaufnahmen ein, die zur Verwendung für Notfall-Rollbacks aufbewahrt werden.

#### <a name="deprecated-policies"></a>Veraltete Richtlinien

- [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled): Aktivieren der Berichterstellung für Nutzungs- und Absturzdaten.
- [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices): Senden von Siteinformationen, um Microsoft-Dienste zu verbessern.

#### <a name="obsoleted-policy"></a>Veraltete Richtlinie

[TLS13HardeningForLocalAnchorsEnabled](./microsoft-edge-policies.md#tls13hardeningforlocalanchorsenabled): Aktivieren Sie das TLS 1.3-Sicherheitsfeature für lokale Vertrauensanker.

## <a name="version-85056470-october-6"></a>Version 85.0.564.70: 6. Oktober

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-85056468-october-1"></a>Version 85.0.564.68: 1. Oktober

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-85056463-september-23"></a>Version 85.0.564.63: 23. September

Sicherheitsupdates werden [hier](./microsoft-edge-relnotes-security.md#september-23-2020) aufgelistet.

## <a name="version-85056451-september-9"></a>Version 85.0.564.51: 9. September

Sicherheitsupdates werden [hier](./microsoft-edge-relnotes-security.md#september-9-2020) aufgelistet.

## <a name="version-85056444-august-31"></a>Version 85.0.564.44: 31. August

Verschiedene Bugs und Leistungsprobleme wurden behoben.

<!-- 85.0.564.41: August 27 -->

## <a name="version-85056441-august-27"></a>Version 85.0.564.41: 27. August

Sicherheitsupdates werden [hier](./microsoft-edge-relnotes-security.md#august-27-2020) aufgelistet.

### <a name="feature-updates"></a>Funktionsupdates

- **Lokale Synchronisierung von Favoriten und Einstellungen**. Jetzt können Sie Browser-Favoriten und -Einstellungen zwischen Active Directory-Profilen in Ihrer eigenen Umgebung synchronisieren, ohne dass eine Cloud-Synchronisierung erforderlich ist.

- Unterstützung von **Microsoft Edge-Gruppenrichtlinien zum Starten vertrauenswürdiger Website und App-Combos ohne Bestätigungsaufforderung**. Unterstützung von Gruppenrichtlinien hinzugefügt, mit denen Administratoren Website + App-Combos hinzufügen können, die vertrauenswürdig sind und deshalb ohne Bestätigungsaufforderung gestartet werden können. Dadurch wird die Möglichkeit für Administratoren hinzugefügt, vertrauenswürdige Protokoll-/Herkunftskombinationen (z. B. Microsoft 365-Apps) für ihre Endbenutzer zu konfigurieren, um die Bestätigungsaufforderung zu unterdrücken, wenn sie zu einer URL navigieren, die ein App-Protokoll enthält.

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
- [EnableSha1ForLocalAnchors](./microsoft-edge-policies.md#enablesha1forlocalanchors): Zulassen von Zertifikaten, die mit SHA-1 signiert wurden, wenn sie von lokalen Vertrauensankern ausgegeben wurden. <!--- [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](./microsoft-edge-policies.md#exemptdomainfiletypepairsfromfiletypedownloadwarnings) - Disable download file type extension-based warnings for specified file types on domains. -->
- [IntensiveWakeUpThrottlingEnabled](./microsoft-edge-policies.md#intensivewakeupthrottlingenabled): Steuern des IntensiveWakeUpThrottling-Features.
- [NewTabPagePrerenderEnabled](./microsoft-edge-policies.md#newtabpageprerenderenabled): Aktivieren des Vorabladens der „Neuer Tab“-Seite für schnellere Darstellung.
- [NewTabPageSearchBox](./microsoft-edge-policies.md#newtabpagesearchbox): Konfigurieren der Suchfeldfunktion der „Neuer Tab“-Seite.
- [PasswordMonitorAllowed](./microsoft-edge-policies.md#passwordmonitorallowed): Benutzern ermöglichen, benachrichtigt zu werden, wenn ihre Kennwörter als unsicher eingestuft wurden.
- [RoamingProfileSupportEnabled](./microsoft-edge-policies.md#roamingprofilesupportenabled): Aktivieren der Verwendung von Roaming-Kopien für Microsoft Edge-Profildaten.
- [RoamingProfileLocation](./microsoft-edge-policies.md#roamingprofilelocation): Festlegen des Verzeichnisses für servergespeicherte Profile.
- [TLSCsipherSuiteDenyList](./microsoft-edge-policies.md#tlsciphersuitedenylist) – Geben Sie die zu deaktivierenden TLS-Chiffrier-Suites an.

#### <a name="obsoleted-policies"></a>Veraltete Richtlinie

- [EnableDomainActionsDownload](./microsoft-edge-policies.md#enabledomainactionsdownload): Herunterladen von Domänenaktionen von Microsoft aktivieren.
- [WebComponentsV0Enabled](./microsoft-edge-policies.md#webcomponentsv0enabled) – Erneutes Aktivieren der Web Components v0-API bis M84.
- [WebDriverOverridesIncompatiblePolicies](./microsoft-edge-policies.md#webdriveroverridesincompatiblepolicies): Zulassen, dass WebDriver inkompatible Richtlinien außer Kraft setzt.

## <a name="version-84052263-august-20"></a>Version 84.0.522.63: 20. August

Sicherheitsupdates befinden sich [hier](./microsoft-edge-relnotes-security.md#august-20-2020).

## <a name="version-84052261-august-17"></a>Version 84.0.522.61: 17. August

Verschiedene Bugs und Leistungsprobleme wurden behoben.

## <a name="version-84052259-august-11"></a>Version 84.0.522.59: 11. August

Sicherheitsupdates werden [hier](./microsoft-edge-relnotes-security.md#august-11-2020) aufgelistet.

## <a name="version-84052258-august-10"></a>Version 84.0.522.58: 10. August

Verschiedene Bugs und Leistungsprobleme wurden behoben.

## <a name="version-84052252-august-1"></a>Version 84.0.522.52: 1. August

Verschiedene Bugs und Leistungsprobleme wurden behoben.

## <a name="version-84052250-july-31"></a>Version 84.0.522.50: 31. Juli

Verschiedene Bugs und Leistungsprobleme wurden behoben.

## <a name="version-84052249-july-29"></a>Version 84.0.522.49: 29. Juli

Sicherheitsupdates werden [hier](./microsoft-edge-relnotes-security.md#july-29-2020) aufgelistet.

## <a name="version-84052248-july-28"></a>Version 84.0.522.48: 28. Juli

Verschiedene Bugs und Leistungsprobleme wurden behoben.

## <a name="version-84052244-july-23"></a>Version 84.0.522.44: 23. Juli

Verschiedene Bugs und Leistungsprobleme wurden behoben.

## <a name="version-84052240-july-16"></a>Version 84.0.522.40: 16. Juli

Sicherheitsupdates werden [hier](./microsoft-edge-relnotes-security.md#july-16-2020) aufgelistet.

### <a name="feature-updates"></a>Funktionsupdates

- Diese Version von Microsoft Edge bietet verbesserte Downloadzeiten für Websitelisten im Internet Explorer-Modus. Wir haben die Downloadverzögerung für die Websiteliste im Internet Explorer-Modus auf 0 Sekunden verringert (von einer ursprünglichen Wartezeit von 60 Sekunden), wenn keine zwischengespeicherte Websiteliste vorhanden ist. Wir haben auch die Unterstützung von Gruppenrichtlinien für Fälle hinzugefügt, in denen Startseitennavigationen im Internet Explorer-Modus verzögert werden müssen, bis die Websiteliste heruntergeladen wurde. Weitere Informationen hierzu finden Sie in der [DelayNavigationsForInitialSiteListDownload](./microsoft-edge-policies.md#delaynavigationsforinitialsitelistdownload)-Richtlinie.

- Microsoft Edge ermöglicht es Benutzern nun, sich beim Browser anzumelden, wenn er unter Windows 10 „als Administrator ausgeführt“ wird. Dies hilft Kunden, die Microsoft Edge auf Windows Server oder in Remotedesktop- und Sandbox-Szenarien auszuführen.

- Microsoft Edge bietet nun vollständige Mausunterstützung im Vollbildmodus. Jetzt können Sie mit der Maus auf Registerkarten, die Adressleiste und andere Elemente zugreifen, ohne den Vollbildmodus zu verlassen.

- Verbesserung für Onlinekäufe. Sie können benutzerdefinierte Spitznamen zu gespeicherten Debit- oder Kreditkarten hinzufügen. Jetzt können Sie zwischen Ihren Kreditkarten unterscheiden, wenn Sie Onlinekäufe tätigen. Wenn Sie Ihren Debit- oder Kreditkarten Spitznamen zuordnen, können Sie leichter die richtige Karte wählen, wenn Sie zur Auswahl der Zahlungsmethode die Funktion zum automatischen Ausfüllen verwenden.

- TLS/1.0 und TLS/1.1 sind standardmäßig deaktiviert.  Die [SSLVersionMin](./microsoft-edge-policies.md#sslversionmin)-Richtlinie ermöglicht die erneute Aktivierung von TLS/1.0 und TLS/1.1. Diese Richtlinie bleibt mindestens bis zur Microsoft Edge-Version 88 verfügbar. Weitere Informationen finden Sie unter [Websitekompatibilität – Auswirkungen von Änderungen an Microsoft Edge](/microsoft-edge/web-platform/site-impacting-changes).

- Verbesserungen an "Sammlungen":

  - Es wurde eine Notizfunktion hinzugefügt, mit der Sie einem Element in einer Sammlung eine Notiz oder einen Kommentar hinzufügen können. Notizen werden gruppiert und bleiben an einen Eintrag angefügt, auch wenn Sie die Elemente in einer Sammlung sortieren. Klicken Sie zum Testen des neuen Features mit der rechten Maustaste auf ein Element, und wählen Sie "Notiz hinzufügen" aus.
  - Die Hintergrundfarbe von Notizen in Sammlungen kann geändert werden. Sie können Farbcodierung verwenden, um Informationen zu organisieren und Ihre Produktivität zu steigern.
  - Es gibt deutliche Verbesserungen bei der Leistung, dank derer Sie Ihre Sammlungen schneller als in früheren Versionen von Microsoft Edge nach Excel exportieren können.

- Zusätzliche Unterstützung von Microsoft Edge-APIs:

  - Die Storage Access-API ist für den Test aktiviert. Dieses Feature ist für Privatbenutzer und Unternehmensbenutzer aktiviert, und die Richtlinie [ExperimentationAndConfigurationServiceControl](./microsoft-edge-policies.md#experimentationandconfigurationservicecontrol) ist auf "Vollständig" festgelegt. Dieses Feature wird standardmäßig für alle Benutzer in Microsoft Edge Version 85 des Stable-Kanals aktiviert.
  
    Da der Datenschutz für die Benutzer immer wichtiger wird, wird die Forderung strengerer Browser-Standardeinstellungen und Opt-in-Einstellungen für Benutzer wie das Blockieren des Zugriffs auf Drittanbieter-Speicher immer verbreiteter. Diese Einstellungen tragen dazu bei, den Datenschutz zu verbessern und den unbefugten Zugriff durch unbekannte oder nicht vertrauenswürdige Parteien zu verhindern. Sie können jedoch auch unerwünschte Nebeneffekte haben wie z. B. das Blockieren des Zugriffs auf Inhalte, die der Benutzer anzeigen möchte (z. B. soziale Medien und eingebettete Medieninhalte).

    Die Storage Access-API ermöglicht den Zugriff auf Erstanbieter-Speicher in einem Drittanbieter-Kontext, wenn ein Benutzer die Absicht bekundet, Speicher zuzulassen, der andernfalls durch die aktuelle Konfiguration des Browsers blockiert würde. Weitere Informationen finden Sie unter [Storage Access-API](https://www.chromestatus.com/feature/5612590694662144).

  - Die Native File System-API ermöglicht es Ihnen, Websiteberechtigungen zum Bearbeiten von Dateien oder Ordnern zu erteilen.

- PDF-Verbesserungen:

  - "Laut vorlesen" für PDF ermöglicht Benutzern das Anhören von PDF-Inhalten, während sie andere wichtige Aufgaben ausführen. Außerdem hilft die Funktion audiovisuell Lernenden beim Lesen von Inhalten, wodurch das Lernen erleichtert wird.
  - Die Funktion zum Bearbeiten von PDF-Dateien wurde verbessert. Jetzt können Sie eine an einer PDF-Datei vorgenommene Bearbeitung direkt in der Datei speichern, anstatt dass jedes Mal, wenn Sie das PDF bearbeiten, eine Kopie erstellt wird.

- Microsoft Edge ermöglicht jetzt die Übersetzung im plastischen Reader. Wenn ein Benutzer eine Seite im plastischen Reader öffnet, kann er auswählen, ob sie in seine gewünschte Sprache übersetzt werden soll.

- Mehrere DevTools-Updates, einschließlich der Unterstützung der Anpassung von Tastenkombinationen für die Übereinstimmung mit VS-Code und die Anzeige der DevTools mit hohem Kontrast.  Weitere Einzelheiten finden Sie unter [Neuigkeiten in DevTools (Microsoft Edge 84)](/microsoft-edge/devtools-guide-chromium/whats-new/2020/05/devtools).

### <a name="policy-updates"></a>Richtlinienupdates

#### <a name="new-policies"></a>Neue Richtlinien

Es wurden sieben neue Richtlinien hinzugefügt. Laden Sie die aktualisierten administrativen Vorlagen von der [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise) herunter. Die folgenden neuen Richtlinien wurden hinzugefügt.

- [AppCacheForceEnabled](./microsoft-edge-policies.md#appcacheforceenabled): Ermöglicht das Wiederaktivieren des AppCache-Features, auch wenn es standardmäßig deaktiviert ist.
- [ApplicationGuardContainerProxy](./microsoft-edge-policies.md#applicationguardcontainerproxy): Konfigurieren der Einstellungen für den Application Guard-Containerproxy.
- [DelayNavigationsForInitialSiteListDownload](./microsoft-edge-policies.md#delaynavigationsforinitialsitelistdownload): Festlegen, dass die Siteliste für den Unternehmensmodus vor der Tabnavigation verfügbar sein muss.
- [WinHttpProxyResolverEnabled](./microsoft-edge-policies.md#winhttpproxyresolverenabled): Verwenden des Windows-Proxy-Konfliktlösers.
- [InternetExplorerIntegrationEnhancedHangDetection](./microsoft-edge-policies.md#internetexplorerintegrationenhancedhangdetection): Konfigurieren der erweiterten Ermittlung von Anwendungsstillständen für den Internet Explorer-Modus.
- [NativeWindowOcclusionEnabled](./microsoft-edge-policies.md#nativewindowocclusionenabled): Zum Verringern des CPU-Leistungs- und Stromverbrauchs erkennt Microsoft Edge, ob ein Fenster von anderen Fenstern überlagert wird, und das Zeichnen der überdeckten Pixel wird unterbrochen.
- [NavigationDelayForInitialSiteListDownloadTimeout](./microsoft-edge-policies.md#navigationdelayforinitialsitelistdownloadtimeout): Festlegen eines Zeitlimits für die Verzögerung der Tabnavigation für die Websiteliste für den Unternehmensmodus.

#### <a name="deprecated-policies"></a>Veraltete Richtlinien

- [AllowSyncXHRInPageDismissal](./microsoft-edge-policies.md#allowsyncxhrinpagedismissal): Seiten das Senden synchroner XHR-Anforderungen während der Seitenschließung ermöglichen.
- [BuiltinCertificateVerifierEnabled](./microsoft-edge-policies.md#builtincertificateverifierenabled) – Bestimmt, ob die integrierte Zertifikatprüfung zum Überprüfen von Serverzertifikaten verwendet wird.
- [StricterMixedContentTreatmentEnabled](./microsoft-edge-policies.md#strictermixedcontenttreatmentenabled): Aktivieren Sie die striktere Behandlung gemischter Inhalte.

#### <a name="obsoleted-policy"></a>Veraltete Richtlinie

[ForceNetworkInProcess](./microsoft-edge-policies.md#forcenetworkinprocess): Erzwingen des Ausführens von Netzwerkcode im Browserprozess.

<!-- End 84 -->
## <a name="version-83047864-july-13"></a>Version 83.0.478.64: 13. Juli

Verschiedene Bugs und Leistungsprobleme wurden behoben.

## <a name="version-83047861-july-7"></a>Version 83.0.478.61: 7. Juli

Verschiedene Bugs und Leistungsprobleme wurden behoben.

## <a name="version-83047858-june-30"></a>Version 83.0.478.58: 30. Juni

Verschiedene Bugs und Leistungsprobleme wurden behoben.

## <a name="version-83047856-june-24"></a>Version 83.0.478.56: 24. Juni

Verschiedene Bugs und Leistungsprobleme wurden behoben.

Sicherheitsupdates werden [hier](./microsoft-edge-relnotes-security.md#june-24-2020) aufgelistet.

## <a name="version-83047854-june-17"></a>Version 83.0.478.54: 17. Juni

Sicherheitsupdates werden [hier](./microsoft-edge-relnotes-security.md#june-17-2020) aufgelistet.

## <a name="version-83047850-june-15"></a>Version 83.0.478.50: 15. Juni

Verschiedene Bugs und Leistungsprobleme wurden behoben.

## <a name="version-83047845-june-4"></a>Version 83.0.478.45: 4. Juni

Sicherheitsupdates werden [hier](./microsoft-edge-relnotes-security.md#june-4-2020) aufgelistet.

## <a name="version-83047844-june-1"></a>Version 83.0.478.44: 1. Juni

Verschiedene Bugs und Leistungsprobleme wurden behoben.

## <a name="version-83047837-may-21"></a>Version 83.0.478.37: 21. Mai

Sicherheitsupdates werden [hier](./microsoft-edge-relnotes-security.md#may-21-2020) aufgelistet.

### <a name="feature-updates"></a>Funktionsupdates

- Das Rollout von Microsoft Edge-Updates erfolgt nun schrittweise. In Zukunft werden Updates für Microsoft Edge für unsere Benutzer über einen Zeitraum von wenigen Tagen bereitgestellt. Auf diese Weise können mehr von ihnen vor versehentlichen fehlerhaften Updates geschützt werden, wodurch die Aktualisierung verbessert wird. Als Benutzer erhalten Sie weiterhin nahtlose automatische Updates. Wenn Ihre Organisation nicht für automatische Updates registriert ist, sind Sie von dieser Änderung nicht betroffen. Weitere Informationen hierzu finden Sie im Artikel [Progressive Rollouts](microsoft-edge-update-progressive-rollout.md).
- Verbesserungen an Microsoft Defender SmartScreen: mehrere Verbesserungen am Microsoft Defender SmartScreen-Dienst vorgenommen, z. B. verbesserter Schutz vor bösartigen Websites, die beim Laden umgeleitet werden, und Blockierung von Frames der obersten Ebene, wodurch bösartige Websites vollständig durch die Microsoft Defender SmartScreen-Sicherheitsseite ersetzt werden. Die allgemeine Blockierung von Frames verhindert, dass Audio und andere Medien der bösartigen Website wiedergegeben werden, was die Benutzererfahrung verbessert und weniger verwirrend macht.

- In Reaktion auf Benutzerfeedback können Benutzer nun bestimmte Cookies vom automatischen Löschen beim Schließen des Browsers ausschließen. Diese Option ist hilfreich, wenn es eine Website gibt, von der Benutzer nicht abgemeldet werden möchten, aber dennoch alle anderen Cookies beim Schließen des Browsers gelöscht werden sollen. Um dieses Feature zu verwenden, wechseln Sie zu *edge://settings/clearBrowsingDataOnClose*, und aktivieren Sie die Option "Cookies und andere Website-Daten".

- Der automatische Profilwechsel steht nun zur Verfügung, damit Sie Ihre Arbeitsinhalte einfacher auf alle Profile übertragen können. Wenn Sie arbeitsbedingt mehrere Profile verwenden, können Sie diese im Auge behalten, indem Sie zu einer Website navigieren, die eine Authentifizierung von Ihrem Geschäfts-, Uni- oder Schulkonto erfordert, während Sie in Ihrem persönlichen Profil angemeldet sind. Wenn dies erkannt wird, erhalten Sie eine Aufforderung, zu Ihrem geschäftlichen Profil zu wechseln, um auf diese Website zuzugreifen, ohne sich dafür anmelden zu müssen. Wenn Sie das geschäftliche Profil auswählen, zu dem Sie wechseln möchten, wird die Website einfach darin geöffnet. Diese Profilwechselfunktion hilft Ihnen, Ihre Arbeits- und persönlichen Daten getrennt zu halten und müheloser zu Ihren Arbeitsinhalten zu gelangen. Wenn Sie nicht zum Wechsel zwischen Profilen aufgefordert werden möchten, können Sie einfach die Option "Nicht mehr danach fragen" auswählen.

- Verbesserungen bei den Sammlungen:
  - Sie können mit Drag & Drop ein Element zu einer Sammlung hinzufügen, ohne die Sammlung zu öffnen. Beim Ziehen und Ablegen können Sie auch einen Speicherort in der Sammlungsliste auswählen, an dem Sie das Element ablegen möchten.
  - Sie können einer Sammlung mehrere Elemente gleichzeitig hinzufügen, anstatt sie einzeln hinzuzufügen. Wenn Sie mehrere Elemente hinzufügen möchten, wählen Sie die Elemente aus, und ziehen Sie sie dann in die gewünschte Sammlung. Sie können die Elemente auch markieren, mit der rechten Maustaste klicken und dann die Sammlung auswählen, in die die Elemente eingefügt werden sollen.

- Sie können alle Tabs in einem Edge-Fenster einer neuen Sammlung hinzufügen, ohne sie einzeln hinzuzufügen. Klicken Sie dazu mit der rechten Maustaste auf einen beliebigen Tab, und wählen Sie "Alle Tabs zu neuer Sammlung hinzufügen" aus.

- Erweiterungssynchronisierung ist jetzt verfügbar. Jetzt können Sie Ihre Erweiterungen auf allen Ihren Geräten synchronisieren! Erweiterungen aus den Microsoft und Chrome Stores werden mit Microsoft Edge synchronisiert. Um dieses Feature zu verwenden, klicken Sie auf die Auslassungspunkte (**...**) auf der Menüleiste, und wählen Sie **Einstellungen** aus. Klicken Sie unter Ihrem Profil auf **Synchronisierung**, um die Synchronisierungsoptionen anzuzeigen. Verwenden Sie unter **Profile/Synchronisierung** die Option zum Aktivieren von Erweiterungen. Zum Deaktivieren der Synchronisierung von Erweiterungen können Sie die [SyncTypesListDisabled](./microsoft-edge-policies.md#synctypeslistdisabled)-Gruppenrichtlinie verwenden.

- Die Meldung auf der Seite "Downloads verwalten" zu unsicheren Downloads, die blockiert wurden, wurde verbessert.

- Verbesserungen für den plastischen Reader:
  - Unterstützung für Adverbien in der Wortarten-Oberfläche im plastischen Reader wurde hinzugefügt. Wenn Sie einen Artikel im plastischen Reader lesen, öffnen Sie die Grammatiktools, und aktivieren Sie "Adverbien" in "Wortarten", um alle Adverbien auf der Seite hervorzuheben.
  - Die Möglichkeit, Inhalte auf einer Webseite auszuwählen und im plastischen Reader zu öffnen, wurde hinzugefügt. Diese Funktion ermöglicht es Benutzern, den plastischen Reader und alle Lerntools (z. B. "Zeilenfokus" und "Laut vorlesen") auf allen Websites zu verwenden.

- Link Doctor bietet den Benutzern eine Host-Korrektur und Suchabfrage, wenn sie sich bei der Eingabe einer URL vertippen. Zum Beispiel: <br>
Ein Benutzer gibt "powerbi" fälschlicherweise als "powerbbi".com ein. Der Link Doctor schlägt "powerbi".com als Korrektur vor und erstellt einen Link zur Suche nach "powerbbi", falls der Benutzer nach etwas anderem sucht.

- Lassen Sie zu, dass Benutzer ihre Entscheidung, ein externes Protokoll für eine bestimmte Site zu starten, speichern. Benutzer können die [ExternalProtocolDialogShowAlwaysOpenCheckbox](/DeployEdge/microsoft-edge-policies#externalprotocoldialogshowalwaysopencheckbox)-Richtlinie konfigurieren, um dieses Feature zu aktivieren oder zu deaktivieren.

- Benutzer können Microsoft Edge direkt in den Microsoft Edge-**Einstellungen** als Standardbrowser festlegen. Dies erleichtert es den Benutzern, ihren Standardbrowser im Kontext des Browsers selbst zu ändern, anstatt die Einstellungen des Betriebssystems durchsuchen zu müssen. Um dieses Feature zu nutzen, gehen Sie zu *edge://settings/defaultBrowser*, und klicken Sie auf **Als Standardbrowser festlegen**.

- Mehrere DevTools-Updates, einschließlich neuer Unterstützung für Remote-Debugging, Verbesserungen der Benutzeroberfläche und mehr. Weitere Einzelheiten finden Sie unter [Neuigkeiten in DevTools (Microsoft Edge 83)](/microsoft-edge/devtools-guide-chromium/whats-new/2020/03/devtools).

- Das Warnszenario für Microsoft Defender für Cloud-Apps ist jetzt verfügbar. Dies ermöglicht Administratoren das Einrichten von Warn, einer neuen Kategorie von Defender für Cloud-Apps-Blöcken, bei denen der Benutzer eine Defender für Cloud-Apps-Sperrseite überschreiben kann. MDATP E5-Blockierungen sind in Microsoft Edge in SmartScreen-Blockierungen nativ integriert und bieten eine nahtlose Benutzererfahrung. Diese Funktion ermöglicht die Anzeige eines ganzseitigen roten Blocks mit der Meldung "Diese Website wird von Ihrer Organisation blockiert" anstelle einer Popupbenachrichtigung.

- Synchrones XmlHttpRequest bei Seitenbeendigung nicht zulassen. Das Senden synchroner XmlHttpRequests während des Beendens einer Webseite wird entfernt. Durch diese Änderung wird die Leistung und Zuverlässigkeit des Browsers verbessert, sie wirkt sich jedoch möglicherweise auf Webanwendungen aus, die noch nicht aktualisiert wurden, um modernere Web-APIs wie sendBeacon und fetch zu verwenden. Die Gruppenrichtlinie zum Deaktivieren dieser Änderung und zum Zulassen von synchronem XHR während der Seitenbeendigung ist bis Microsoft Edge 88 verfügbar. Weitere Informationen finden Sie unter [Websitekompatibilität – Auswirkungen von Änderungen an Microsoft Edge](/microsoft-edge/web-platform/site-impacting-changes).

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

<!-- end 83 -->

## <a name="version-81041677-may-18"></a>Version 81.0.416.77: 18. Mai

Verschiedene Bugs und Leistungsprobleme wurden behoben.

## <a name="version-81041672-may-7"></a>Version 81.0.416.72: 07. Mai

Sicherheitsupdates werden [hier](./microsoft-edge-relnotes-security.md#may-7-2020) aufgelistet.

## <a name="version-81041668-april-29"></a>Version 81.0.416.68: 29. April

Sicherheitsupdates werden [hier](./microsoft-edge-relnotes-security.md#april-29-2020) aufgelistet.

## <a name="version-81041664-april-23"></a>Version 81.0.416.64: 23. April

Sicherheitsupdates werden [hier](./microsoft-edge-relnotes-security.md#april-23-2020) aufgelistet.

## <a name="version-81041658-april-17"></a>Version 81.0.416.58: 17. April

Sicherheitsupdates werden [hier](./microsoft-edge-relnotes-security.md#april-17-2020) aufgelistet.

## <a name="version-81041653-april-13"></a>Version 81.0.416.53: 13. April

Sicherheitsupdates werden [hier](./microsoft-edge-relnotes-security.md#april-13-2020) aufgelistet.

### <a name="feature-updates"></a>Funktionsupdates

- Unterstützung für Windows Information Protection (WIP) wurde hinzugefügt, der Unternehmen dabei hilft, vertrauliche Daten vor unbefugter Offenlegung zu schützen. [Weitere Informationen](./microsoft-edge-security-windows-information-protection.md)

- Sammlungen ist jetzt verfügbar. Um zu beginnen, klicken Sie auf das Symbol "Sammlungen" neben der Adressleiste. Durch diese Aktion wird der Bereich "Sammlungen" geöffnet, in dem Sie Sammlungen erstellen, bearbeiten und anzeigen können. Wir haben Sammlungen basierend auf dem, was Sie im Web tun, gestaltet. Wenn Sie Shopper, Reisender, Lehrer oder Schüler bzw. Studierender sind, können Sammlungen hilfreich sein. [Weitere Informationen](https://blogs.windows.com/msedgedev/2019/12/09/improvements-collections-sync-microsoft-edge/#LuDPRDUDCgdgdOVt.97).

- Lassen Sie die Entfernung (Ausblenden aus der Symbolleiste) der Schaltfläche „Sammlungen“ aus der Microsoft Edge-Symbolleiste aus Konsistenzgründen zu.

- Die automatische Anmeldung bei lokalen Active Directory-Konten wird nur für Organisationen angestrebt, die diese Funktion aktivieren.  Wenn Benutzer bereits mit einem lokalen AD-Konto angemeldet waren, können Sie sich abmelden. Benutzer werden mit dem primären Konto ihres Betriebssystems nur automatisch angemeldet, wenn es sich um ein Microsoft-Konto oder ein Azure Active Directory-Konto handelt. Administratoren können mithilfe der ConfigureOnPremisesAccountAutoSignIn-Richtlinie die automatische Anmeldung mit einem lokalen AD-Konto aktivieren.

- Application Guard. Unterstützung von Erweiterungen ist jetzt im Container verfügbar.

- Eine Nachricht wurde hinzugefügt, um die Benutzer zu informieren, dass Internet Explorer nicht installiert ist, wenn sie zu einer Seite navigieren, die für das Öffnen im Internet Explorer-Modus konfiguriert ist.

- Das Tool für die 3D-Ansicht in Microsoft Edge DevTools wurde mit einem neuen Feature aktualisiert, das das Debuggen von Z-Index-Stapelkontext unterstützt. In der 3D-Ansicht wird die DOM(Dokumentobjektmodell)-Tiefe mithilfe von Farbe und Stapelung dargestellt, und mit der Z-Index-Ansicht können Sie die verschiedenen Stapelkontexte Ihrer Seite isolieren. [Weitere Informationen](https://blogs.windows.com/msedgedev/2020/01/23/debug-z-index-3d-view-edge-devtools/).

- Die F12-Entwicklungstools wurden in zehn neue Sprachen lokalisiert, sodass sie mit der im restlichen Browser verwendeten Sprache übereinstimmen. [Weitere Informationen](https://blogs.windows.com/msedgedev/2020/02/04/localizing-edge-devtools/).

- Unterstützung für Dolby Vision-Wiedergabe hinzugefügt. Bei dem für Dolby Vision aktivierten Windows 10 Build 17134 (Update vom April 2018) können Dolby Vision-Inhalte von Websites angezeigt werden. Hier erfahren Sie, wie Sie Dolby Vision-Inhalte von [Netflix](https://help.netflix.com/en/node/42384) aktivieren.

- Microsoft Edge kann nun doppelte Favoriten erkennen und entfernen sowie Ordner mit demselben Namen zusammenführen. Für den Zugriff auf das Tool klicken Sie in der Symbolleiste des Browsers auf den Stern, und wählen Sie "Doppelte Favoriten entfernen" aus.  Sie können Änderungen bestätigen und alle Updates Ihrer Favoriten werden auf allen Geräten synchronisiert.

- Wir haben von Benutzern gehört, dass es schwierig sein kann, ein normales Browserfenster in dunklem Design von einem InPrivate-Fenster zu unterscheiden, da beide Fensterrahmen dunkel sind. Die neue einfarbige, blaue InPrivate-Pille in der oberen rechten Ecke versichert den Benutzern, dass sie InPrivate browsen.

- Öffnen Sie externe Links im richtigen Browserprofil. Wählen Sie ein Standardprofil für Links aus externen Apps aus, um sie aus *edge://settings/multiProfileSettings* zu öffnen.

- Es wurde eine Warnung hinzugefügt, mit der Benutzer benachrichtigt werden, die sich bei einem Browserprofil mit einem Konto anmelden, nachdem sie bereits mit einem anderen Konto angemeldet sind. Diese Warnung dient als Unterstützung, um unbeabsichtigte Datenzusammenführungen zu verhindern.

- Wenn Sie in Ihrem Microsoft-Konto Zahlungskarten gespeichert haben, können Sie diese in Microsoft Edge beim Ausfüllen von Zahlungsformularen verwenden. Die Karten in Ihrem Microsoft-Konto werden auf Desktopgeräten synchronisiert, und die vollständigen Details werden nach zweistufiger Authentifizierung (CVC-Code und Microsoft-Identität) für die Website freigegeben. Zur weiteren Vereinfachung können Sie während der Authentifizierung auswählen, dass eine Kopie der Karte auf dem Gerät gesichert werden soll.

- Der Zeilenfokus ist für Benutzer vorgesehen, die sich beim Lesen auf einen begrenzten Teil des Inhalts konzentrieren möchten. Benutzer können den Fokus auf jeweils 1, 3 oder 5 Zeilen gleichzeitig richten und den Rest der Seite abblenden, um ohne Ablenkung zu lesen. Benutzer können mit den Fingern oder Pfeiltasten scrollen, und der Fokus wird dementsprechend verschoben.

- Windows Speller ist nun auf den Windows-Plattformen 8.1 und höher in Microsoft Edge integriert. Diese Integration bietet eine bessere Sprachunterstützung, mit Zugriff auf weitere Sprachwörterbücher sowie der Möglichkeit zur Verwendung von Windows-Benutzerwörterbüchern. Es sind keine weiteren Aktionen von Seiten der Benutzer erforderlich, wenn eine Sprache in den Spracheinstellungen des Betriebssystems hinzugefügt wurde. Außerdem ist in den Microsoft Edge-Einstellungen eine Umschaltfläche für die Rechtschreibprüfung aktiviert.

- Wenn PDF-Dokumente mit Microsoft Edge geöffnet werden, können die Benutzer jetzt Stellen hervorheben, Farben ändern und Hervorhebungen löschen. Dieses Feature hilft bei späteren Verweisen auf wichtige Teile des Dokuments und bei der Zusammenarbeit.

- Beim Laden langer PDF-Dokumente, die für das Web optimiert wurden, werden die vom Benutzer angezeigten Seiten schneller geladen, während der Rest des Dokuments parallel geladen wird.

- Jetzt ist es einfacher, den Plastischen Reader für eine Website zu starten, indem Sie einfach die Taste F9 drücken.

- Jetzt ist es einfacher, mit einer Tastenkombination (STRG+UMSCHALT+U) „Laut vorlesen“ zu starten.

- Es wurde ein MSI-Befehlszeilenparameter hinzugefügt, mit dem Sie die Erstellung von Desktop Symbolen bei der Installation von Microsoft Edge unterdrücken können. Im folgenden Beispiel wird gezeigt, wie dieser neue Parameter verwendet wird: <br>
`MicrosoftEdgeEnterpriseX64.msi DONOTCREATEDESKTOPSHORTCUT=true`<br>
Es wird eine Gruppenrichtlinie geben, die diese Funktion in einer künftigen Version unterstützt.

### <a name="policy-updates"></a>Richtlinienupdates

#### <a name="new-policies"></a>Neue Richtlinien

Es wurden 11 neue Richtlinien hinzugefügt. Laden Sie die aktualisierten administrativen Vorlagen von der [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise) herunter. Die folgenden neuen Richtlinien wurden hinzugefügt.

- [AmbientAuthenticationInPrivateModesEnabled](./microsoft-edge-policies.md#ambientauthenticationinprivatemodesenabled): Aktivieren Sie die Umgebungsauthentifizierung für InPrivate- und Gastprofile. 
- [AudioSandboxEnabled](./microsoft-edge-policies.md#audiosandboxenabled): Lassen Sie die Audio-Sandbox ausführen.
- [ForceLegacyDefaultReferrerPolicy](./microsoft-edge-policies.md#forcelegacydefaultreferrerpolicy): Verwenden Sie die standardmäßige Verweiserrichtlinie „kein Verweiser beim Downgrade“.
- [GloballyScopeHTTPAuthCacheEnabled](./microsoft-edge-policies.md#globallyscopehttpauthcacheenabled): Aktivieren Sie den Cache für HTTP-Authentifizierung mit globaler Reichweite.
- [ImportExtensions](./microsoft-edge-policies.md#importextensions): Lassen Sie den Import von Erweiterungen zu.
- [ImportCookies](./microsoft-edge-policies.md#importcookies): Lassen Sie den Import von Cookies zu.
- [ImportShortcuts](./microsoft-edge-policies.md#importshortcuts): Lassen Sie den Import von Verknüpfungen zu.
- [InternetExplorerIntegrationSiteRedirect](./microsoft-edge-policies.md#internetexplorerintegrationsiteredirect): Geben Sie an, wie sich „seiteninterne“ Navigationen zu nicht konfigurierten Websites verhalten, wenn sie von Seiten im Internet Explorer-Modus gestartet werden.
- [StricterMixedContentTreatmentEnabled](./microsoft-edge-policies.md#strictermixedcontenttreatmentenabled): Aktivieren Sie die striktere Behandlung gemischter Inhalte.
- [TLS13HardeningForLocalAnchorsEnabled](./microsoft-edge-policies.md#tls13hardeningforlocalanchorsenabled): Aktivieren Sie das TLS 1.3-Sicherheitsfeature für lokale Vertrauensanker.
- [ConfigureOnPremisesAccountAutoSignIn](./microsoft-edge-policies.md#configureonpremisesaccountautosignin): Konfigurieren Sie die automatische Anmeldung mit einem Active Directory-Domänenkonto, wenn kein Azure AD-Domänenkonto vorhanden ist.

#### <a name="policy-name-and-caption-changes"></a>Richtlinienname und Titeländerungen

Die Richtlinie `OmniboxMSBProviderEnabled` wird in [AddressBarMicrosoftSearchInBingProviderEnabled](//DeployEdge/microsoft-edge-policies#addressbarmicrosoftsearchinbingproviderenabled) geändert. Der Titel der Richtlinie lautet „Microsoft Search in Bing-Vorschlägen in der Adressleiste aktivieren“.

#### <a name="deprecated-policies"></a>Veraltete Richtlinien

Die folgenden Richtlinien greifen in dieser Version weiterhin. Sie veralten in einer zukünftigen Version.

- [WebComponentsV0Enabled](./microsoft-edge-policies.md#webcomponentsv0enabled): Aktivieren Sie die Web Components v0-API bis M84 erneut.
- [WebDriverOverridesIncompatiblePolicies](./microsoft-edge-policies.md#webdriveroverridesincompatiblepolicies): Lassen Sie zu, dass WebDriver inkompatible Richtlinien außer Kraft setzt.

#### <a name="resolved-issues"></a>Gelöste Probleme

- Es wurde ein Problem behoben, das dazu geführt hat, dass durch den IE-Modus on Microsoft Edge selbst nach dem Herunterladen der Datei ein fortlaufendes Dialogfeld angezeigt wurde.
- Es wurde ein Problem behoben, bei dem Microsoft Edge Sitzungscookies abgelegt hat, selbst wenn eine Seite, die sich bereits im IE-Modus befand, das Öffnen einer neuen Registerkarte im IE-Modus- ausgelöst hat.

## <a name="version-800361111-april-7"></a>Version 80.0.361.111: 7. April

Verschiedene Bugs und Leistungsprobleme wurden behoben.

## <a name="version-800361109-april-1"></a>Version 80.0.361.109: 1. April

Sicherheitsupdates werden [hier](./microsoft-edge-relnotes-security.md#april-1-2020) aufgelistet.

## <a name="version-80036169-march-19"></a>Version 80.0.361.69: 19. März

Sicherheitsupdates werden [hier](./microsoft-edge-relnotes-security.md#march-19-2020) aufgelistet.

## <a name="version-80036166-march-4"></a>Version 80.0.361.66: 4. März

Sicherheitsupdates werden [hier](./microsoft-edge-relnotes-security.md#march-4-2020) aufgelistet.

## <a name="version-80036162-february-25"></a>Version 80.0.361.62: 25. Februar

Sicherheitsupdates werden [hier](./microsoft-edge-relnotes-security.md#february-25-2020) aufgelistet.

## <a name="version-80036157-february-20"></a>Version 80.0.361.57: 20. Februar

Sicherheitsupdates werden [hier](./microsoft-edge-relnotes-security.md#february-20-2020) aufgelistet.

## <a name="version-80036156-february-19"></a>Version 80.0.361.56: 19. Februar

Verschiedene Bugs und Leistungsprobleme wurden behoben.

## <a name="version-80036154-february-14"></a>Version 80.0.361.54: 14. Februar

### <a name="resolved-issues"></a>Gelöste Probleme

- Ein Problem wurde behoben, bei dem Kennwort, Zahlungen und Cookies nicht in Microsoft Edge importiert werden konnten.

## <a name="version-80036150-february-11"></a>Version 80.0.361.50: 11. Februar

Verschiedene Bugs wurden behoben und Leistungskorrekturen vorgenommen.

## <a name="version-80036148-february-7"></a>Version 80.0.361.48: 7. Februar

Sicherheitsupdates werden [hier](./microsoft-edge-relnotes-security.md#february-7-2020) aufgelistet.

### <a name="feature-updates"></a>Funktionsupdates

- SmartScreen-Schutz vor dem Herunterladen potenziell unerwünschter Apps wurde hinzugefügt. [Mehr erfahren](/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus)
- Unterstützung für Dolby Vision-Wiedergabe hinzugefügt.
- Nutzer von Windows Mixed Reality können jetzt 360°-Videos auf VR-Headsets anzeigen.
- Der Leseansicht wurde eine Option hinzugefügt, um den Textabstand zu vergrößern.
- Unterstützung für das Löschen von Links mit dem Surface Pen-Radierer hinzugefügt.
- Unterstützung für die Verwendung der Pfeiltasten und der Leertaste zum Zeichnen von Feedback-Screenshots im Editor-Modus hinzugefügt.
- Die Zuverlässigkeit von Screenshots wurde verbessert, sodass sie beim Senden von Feedback nicht mehr schwarz angezeigt werden.
- Unterstützung für dunkles Design zur lokalen neuen Registerkartenseite hinzugefügt, die angezeigt wird, wenn das Gerät nicht mit dem Internet verbunden ist.
- Es wurde die Möglichkeit hinzugefügt, Websites, die als Apps installiert sind, wiederherzustellen, wenn eine Browsersitzung nach einer Aktualisierung, einem Absturz und so weiter wiederhergestellt wird.
- Unterstützung für dunkle Themen zur PDF-Benutzeroberfläche hinzugefügt, wenn der Browser über Gruppenrichtlinien verwaltet wird.
- Adobe Flash auf Version 32.0.0.321 aktualisiert. [Mehr erfahren](https://helpx.adobe.com/flash-player/release-note/fp_32_air_32_release_notes.html)

### <a name="policy-updates"></a>Richtlinienupdates

#### <a name="new-policies"></a>Neue Richtlinien

Es wurden 16 neue Richtlinien hinzugefügt. Laden Sie die aktualisierten administrativen Vorlagen von der [Microsoft Edge Enterprise Angebotsseite](https://aka.ms/EdgeEnterprise) herunter. Die folgenden neuen Richtlinien wurden hinzugefügt.

- [AlternateErrorPagesEnabled](./microsoft-edge-policies.md#alternateerrorpagesenabled) – Schlagen Sie ähnliche Seiten vor, wenn eine Webseite nicht gefunden werden kann.
- [DefaultInsecureContentSetting](./microsoft-edge-policies.md#defaultinsecurecontentsetting) – Steuern Sie die Verwendung unsicherer Inhaltsausnahmen.
- [DNSInterceptionChecksEnabled](./microsoft-edge-policies.md#dnsinterceptionchecksenabled) – DNS-Abhörprüfungen aktiviert.
- [HideFirstRunExperience](./microsoft-edge-policies.md#hidefirstrunexperience) – Blenden Sie den Ersteinführungsbildschirm und den Begrüßungsbildschirm aus.
- [InsecureContentAllowedForUrls](./microsoft-edge-policies.md#insecurecontentallowedforurls) – Erlauben unsicheren Inhalts auf bestimmten Seiten.
- [InsecureContentBlockedForUrls](./microsoft-edge-policies.md#insecurecontentblockedforurls) – Blockieren Sie unsicheren Inhalt auf bestimmten Websites.
- [LegacySameSiteCookieBehaviorEnabled](./microsoft-edge-policies.md#legacysamesitecookiebehaviorenabled) – Standardeinstellung für das Verhalten von Legacy-SameSite-Cookies aktivieren.
- [LegacySameSiteCookieBehaviorEnabledForDomainList](./microsoft-edge-policies.md#legacysamesitecookiebehaviorenabledfordomainlist) – Wiederherstellen des Legacy-SameSite-Verhaltens für Cookies auf bestimmten Websites.
- [PaymentMethodQueryEnabled](./microsoft-edge-policies.md#paymentmethodqueryenabled) – Websites erlauben, nach verfügbaren Zahlungsmethoden zu fragen.
- [PersonalizationReportingEnabled](./microsoft-edge-policies.md#personalizationreportingenabled) – Die Personalisierung von Werbung, der Suche und von Nachrichten ermöglichen, indem der Browserverlauf an Microsoft gesendet wird.
- [PinningWizardAllowed](./microsoft-edge-policies.md#pinningwizardallowed) – PIN für Taskleisten-Assistenten zulassen.
- [SmartScreenPuaEnabled](./microsoft-edge-policies.md#smartscreenpuaenabled) – Konfigurieren von Microsoft Defender SmartScreen, sodass potenziell unerwünschte Apps blockiert werden.
- [TotalMemoryLimitMb](./microsoft-edge-policies.md#totalmemorylimitmb) – Festlegen der Speicherbegrenzung für Megabyte, die eine einzelne Microsoft Edge-Instanz verwenden kann.
- [WebAppInstallForceList](./microsoft-edge-policies.md#webappinstallforcelist) – Konfigurieren der Liste der erzwungen installierten Web-Apps.
- [WebComponentsV0Enabled](./microsoft-edge-policies.md#webcomponentsv0enabled) – Erneutes Aktivieren der Web Components v0-API bis M84.
- [WebRtcLocalIpsAllowedUrls](./microsoft-edge-policies.md#webrtclocalipsallowedurls) – Verwalten der Offenlegung lokaler IP-Adressen durch WebRTC.

#### <a name="deprecated-policies"></a>Veraltete Richtlinien

Die folgende Richtlinie wurde verworfen.

- [NewTabPageCompanyLogo](./microsoft-edge-policies.md#newtabpagecompanylogo) – Neues Firmenlogo auf der Registerkarte festlegen.

### <a name="resolved-issues"></a>Gelöste Probleme

- Es wurde ein Problem behoben, bei dem Audio in der Citrix-Umgebung nicht funktioniert hat.
- Es wurde ein Problem behoben, durch das Microsoft Edge und ältere Versionen von Microsoft Edge nebeneinander zu fehlerhaften älteren Verknüpfungen und Abstürzen führten.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)