---
title: Versionshinweise von Microsoft Edge für Stable Channel
ms.author: leahtu
author: dan-wesley
manager: srugh
ms.date: 03/10/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Versionshinweise von Microsoft Edge für Stable Channel
ms.openlocfilehash: a7e11586c77b600253f25c2819a26e72e18f4b28
ms.sourcegitcommit: 556aca8dde42dd66364427f095e8e473b86651a0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2022
ms.locfileid: "12445639"
---
# <a name="release-notes-for-microsoft-edge-stable-channel"></a>Versionshinweise für Microsoft Edge Stable Channel

Diese Versionshinweise enthalten Informationen zu neuen Funktionen und nicht sicherheitsrelevanten Updates, die im Microsoft Edge Stable Channel enthalten sind.

- Alle Sicherheitsupdates sind unter [Versionshinweise für Microsoft Edge-Sicherheitsupdates](./microsoft-edge-relnotes-security.md) aufgeführt.
- Archivierte Versionshinweise für Microsoft Edge Stable Channel finden Sie unter [Archivierte Versionshinweise für Microsoft Edge Stable Channel](./microsoft-edge-relnote-archive-stable-channel.md).

 Informationen zu Microsoft Edge-Kanälen finden Sie in der [Übersicht über die Microsoft Edge-Kanäle](./microsoft-edge-channels.md).

> [!NOTE]
> Für den Stable Channel erfolgt das Rollout von Updates progressiv über einen oder mehrere Tage. Weitere Informationen hierzu finden Sie unter [Progressive Rollouts für Microsoft Edge-Updates](./microsoft-edge-update-progressive-rollout.md).
>
> Die Microsoft Edge-Webplattform entwickelt sich ständig weiter, um Benutzerfreundlichkeit, Sicherheit und Datenschutz zu verbessern. Weitere Informationen finden Sie unter [Kommende Änderungen in Microsoft Edge mit Auswirkungen auf die Websitekompatibilität](/microsoft-edge/web-platform/site-impacting-changes).

## <a name="version-990115039-march-10"></a>Version 99.0.1150.39: 10. März

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-980110876-march-9"></a>Version 98.0.1108.76: 9. März

Verschiedene Fehler und Leistungsprobleme für das Release „Stabil (Erweitert) wurden behoben.

## <a name="version-990115036-march-7"></a>Version 99.0.1150.36: 7. März

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-990115030-march-3"></a>Version 99.0.1150.30: 3. März

Stable Channel-Sicherheitsupdates sind [hier](/deployedge/microsoft-edge-relnotes-security#march-3-2022) aufgeführt.

### <a name="feature-updates"></a>Funktionsupdates

- **Bevorstehende dreistellige Versionsnummer in der Zeichenfolge des Benutzer-Agenten.** Ab Version 100 sendet Microsoft Edge eine dreistellige Versionsnummer in der Kopfzeile des Benutzer-Agenten, z. B. "Edg/100". Ab Microsoft Edge 97 können Sitebesitzer diese in Kürze verfügbare Agent-Zeichenfolge testen, indem sie das Experimentkennzeichen **#force-major-version-to-100** unter *edge://flags* aktivieren, um sicherzustellen, dass ihre User-Agent Analyselogik stabil ist und wie erwartet funktioniert.

- **Personalisieren Sie die Nutzung mehrerer Profile mit Profileinstellungen für Sites** Zur Personalisierung der Nutzung mehrerer Profile können Benutzer eine benutzerdefinierte Liste von Sites für den automatischen Profilwechsel in Microsoft Edge erstellen.

- **Navigieren Sie in PDF-Dokumenten mit Miniaturansichten der Seiten** Sie können jetzt mithilfe von Miniaturansichten der einzelnen Seiten durch Ihr PDF-Dokument navigieren. Diese Miniaturansichten werden im Bereich auf der linken Seite des PDF-Readers angezeigt.

- **Konfigurieren Sie die Liste der Domänen, für die die Benutzeroberfläche des Kennwort-Managers für "Speichern" und "Ausfüllen" deaktiviert wird.** Konfigurieren Sie über die [PasswordManagerBlocklist](/deployedge/microsoft-edge-policies#passwordmanagerblocklist)-Richtlinie die Liste der Domänen (nur HTTP-/HTTPS-Schemas und Hostnamen), für die in Microsoft Edge der Kennwort-Manager deaktiviert werden soll. Dies bedeutet, dass Speichern- und Ausfüllen-Abläufe deaktiviert werden, wodurch sichergestellt wird, dass Kennwörter für diese Websites nicht gespeichert oder automatisch in Webformulare eingegeben werden können.

- **Benutzerdefiniertes primäres Kennwort.** Der Browser verfügt bereits über die Funktion, mit der Benutzer einen Authentifizierungsschritt hinzufügen können, bevor gespeicherte Kennwörter automatisch in Webformulare eingegeben werden. Hiermit wird eine weitere Datenschutzebene hinzugefügt und verhindert, dass nicht-autorisierte Benutzer gespeicherte Kennwörter zum Anmelden bei Websites verwenden. Ein benutzerdefiniertes primäres Kennwort ist eine Weiterentwicklung desselben Features. Die Benutzer können jetzt eine benutzerdefinierte Zeichenfolge ihrer Wahl als primäres Kennwort verwenden. Nachdem es aktiviert wurde, geben Benutzer dieses Kennwort ein, um sich selbst zu authentifizieren, bevor ihre gespeicherten Kennwörter automatisch in Webformulare eingegeben werden.

### <a name="policy-updates"></a>Richtlinienupdates

#### <a name="new-policies"></a>Neue Richtlinien

- [DoNotSilentlyBlockProtocolsFromOrigins](/DeployEdge/microsoft-edge-policies#donotsilentlyblockprotocolsfromorigins): Definieren einer Liste von Protokollen, die nicht im Hintergrund durch den Anti-Flood-Schutz blockiert werden können
- [ForceMajorVersionToMinorPositionInUserAgent](/DeployEdge/microsoft-edge-policies#forcemajorversiontominorpositioninuseragent): Aktivieren oder Deaktivieren des Einfrierens der Benutzer-Agent-Zeichenfolge in Hauptversion 99
- [HubsSidebarEnabled](/DeployEdge/microsoft-edge-policies#hubssidebarenabled): Hub-Seitenleiste anzeigen
- [InternetExplorerIntegrationCloudNeutralSitesReporting](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationcloudneutralsitesreporting): Konfigurieren der Berichterstellung für potenziell falsch konfigurierte neutrale Website-URLs an die M365 Admin Center-Websitelisten-App
- [InternetExplorerIntegrationCloudUserSitesReporting](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationcloudusersitesreporting): Konfigurieren der Berichterstellung von IE-Modus-Benutzerlisteneinträgen an die M365 Admin Center-Websitelisten-App
- [PasswordManagerBlocklist](/DeployEdge/microsoft-edge-policies#passwordmanagerblocklist): Konfigurieren der Liste der Domänen, für die die Kennwort-Manager-Benutzeroberfläche ("Speichern" und "Ausfüllen") deaktiviert werden soll
- [RelatedMatchesCloudServiceEnabled](/DeployEdge/microsoft-edge-policies#relatedmatchescloudserviceenabled): Konfigurieren verwandter Übereinstimmungen in "Auf Seite suchen"
- [SignInCtaOnNtpEnabled](/DeployEdge/microsoft-edge-policies#signinctaonntpenabled): Aktivieren des Dialogfelds "Zum Anmelden klicken"
- [UserAgentReduction](/DeployEdge/microsoft-edge-policies#useragentreduction): Aktivieren oder Deaktivieren der Benutzer-Agent-Reduzierung


## <a name="version-980110862-february-24"></a>Version 98.0.1108.62: 24. Februar

Verschiedene Fehler und Leistungsprobleme für das Release "Stabil" und "Stabil (Erweitert)"wurden behoben.

## <a name="version-980110856-february-17"></a>Version 98.0.1108.56:: 17. Februar

Verschiedene Fehler und Leistungsprobleme für das Release "Stabil" und "Stabil (Erweitert)"wurden behoben.

## <a name="version-980110855-february-16"></a>Version 98.0.1108.55: 16. Februar

> [!Important]
> Dieses Update enthält einen Fix für [CVE-2022-0609](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2022-0609), wovon laut Chromium-Team ein Exploit in Umlauf ist. Weitere Informationen finden Sie im [Leitfaden für Sicherheitsupdates](https://msrc.microsoft.com/update-guide).

Stable Channel-Sicherheitsupdates sind [hier](/deployedge/microsoft-edge-relnotes-security#february-16-2022) aufgeführt.

## <a name="version-980110850-february-10"></a>Version 98.0.1108.50: 10. Februar

Stable Channel-Sicherheitsupdates sind [hier](/deployedge/microsoft-edge-relnotes-security#february-10-2022) aufgeführt.

## <a name="version-980110843-february-3"></a>Version 98.0.1108.43: 3. Februar

Sicherheitsupdates im Stabilen Kanal sind [hier](/deployedge/microsoft-edge-relnotes-security#february-3-2022) aufgeführt.

### <a name="feature-updates"></a>Funktionsupdates

- **Verbessern Sie Ihre Sicherheit im Web.** Dies ist ein Browsermodus in Microsoft Edge, in dem die Sicherheit des Browsers Priorität hat und der Benutzern beim Surfen im Internet zusätzlichen Schutz bietet. Administratoren können Gruppenrichtlinien auf Endbenutzerdesktops (Windows, macOS und Linux) anwenden, um zum Schutz vor Exploits im Umlauf (auch als Zero-Days-Exploits bezeichnet) beizutragen. Die folgenden Gruppenrichtlinien unterstützen diesen Browsermodus:

  - [EnhanceSecurityMode](/deployedge/microsoft-edge-policies#enhancesecuritymode)
  - [EnhanceSecurityModeBypassListDomains](/deployedge/microsoft-edge-policies#enhancesecuritymodebypasslistdomains)
  - [EnhanceSecurityModeEnforceListDomains](/deployedge/microsoft-edge-policies#enhancesecuritymodeenforcelistdomains)

- **Bevorstehende dreistellige Versionsnummer in der Zeichenfolge des Benutzer-Agenten.** Ab Version 100 sendet Microsoft Edge eine dreistellige Versionsnummer im User-Agent Header, z. B. "Edg/**100**". Ab Microsoft Edge 97 können Sitebesitzer diese in Kürze verfügbare User-Agent-Zeichenfolge testen, indem sie das Experimentkennzeichen **#force-major-version-to-100** unter *edge://flags* aktivieren, um sicherzustellen, dass ihre User-Agent Analyselogik stabil ist und wie erwartet funktioniert.

- **Veraltete Plan-B-SDP-Semantik von WebRTC.** Mit dieser Änderung wird ein veralteter SDP-Dialekt (Session Description Protocol) namens "Plan B" nicht mehr unterstützt. Dieses SDP-Format wird durch "Unified Plan" ersetzt, ein spezifikationskonformes und browserübergreifendes SDP-Format. Weitere Informationen finden Sie im Chrome Platform Status-Eintrag [PSA: Plan B should throw in M96 Beta and Stable](https://chromestatus.com/feature/5823036655665152) und [PSA: Plan B throwing in Stable and Extended Deprecation Trial End Date](https://groups.google.com/g/discuss-webrtc/c/gEHrZyYKsfU). Das Anfordern einer [Testversion für RTCPeerConnection Plan B SDP-Semantik](https://developer.chrome.com/origintrials/#/view_trial/3892235977954951169) ermöglicht es Websites, die veraltete API bis Version 101 weiterhin zu verwenden.

- **Bildlaufleisten mit Überlagerung zu Microsoft Edge hinzugefügt** Wir haben unsere Bildlaufleisten mit einem Überlagerungs-Design aktualisiert. Benutzer können dieses Feature unter *edge://flags* aktivieren.

### <a name="policy-updates"></a>Richtlinienupdates

#### <a name="new-policies"></a>Neue Richtlinien

- [AddressBarEditingEnabled](/DeployEdge/microsoft-edge-policies#addressbareditingenabled): Konfigurieren der Bearbeitung der Adressleiste
- [AllowGamesMenu](/DeployEdge/microsoft-edge-policies#allowgamesmenu): Benutzern den Zugriff auf das Menü "Spiele" gestatten
- [EdgeFollowEnabled](/DeployEdge/microsoft-edge-policies#edgefollowenabled): Aktivieren des "Folgen"-Diensts in Microsoft Edge
- [EnhanceSecurityMode](/DeployEdge/microsoft-edge-policies#enhancesecuritymode): Verbessern des Sicherheitsstatus in Microsoft Edge
- [EnhanceSecurityModeBypassListDomains](/DeployEdge/microsoft-edge-policies#enhancesecuritymodebypasslistdomains): Konfigurieren der Liste der Domänen, für die der erweiterte Sicherheitsmodus nicht erzwungen wird
- [EnhanceSecurityModeEnforceListDomains](/DeployEdge/microsoft-edge-policies#enhancesecuritymodeenforcelistdomains): Konfigurieren der Liste der Domänen, für die der erweiterte Sicherheitsmodus immer erzwungen wird
- [InAppSupportEnabled](/DeployEdge/microsoft-edge-policies#inappsupportenabled): In-App-Unterstützung aktiviert
- [MicrosoftEdgeInsiderPromotionEnabled](/DeployEdge/microsoft-edge-policies#microsoftedgeinsiderpromotionenabled): Microsoft Edge Insider-Promotion aktiviert
- [PrintStickySettings](/DeployEdge/microsoft-edge-policies#printstickysettings): Druckvorschau-Einrastfunktionseintellungen
- [SandboxExternalProtocolBlocked](/DeployEdge/microsoft-edge-policies#sandboxexternalprotocolblocked): Zulassen, dass Microsoft Edge die Navigation zu externen Protokollen in einem Sandkasten-iFrame blockiert
- [U2fSecurityKeyApiEnabled](/DeployEdge/microsoft-edge-policies#u2fsecuritykeyapienabled): Verwendung der veralteten U2F-Sicherheitsschlüssel-API zulassen

## <a name="version-970107276-january-27"></a>Version 97.0.1072.76: 27. Januar

Verschiedene Fehler und Leistungsprobleme wurden behoben.

### <a name="feature-updates"></a>Funktionsupdate

- **Bevorstehende dreistellige Versionsnummer in der Zeichenfolge des Benutzer-Agenten.** Ab Version 100 sendet Microsoft Edge eine dreistellige Versionsnummer im User-Agent Header, z. B. "Edg/**100**". Ab Microsoft Edge 97 können Sitebesitzer diese in Kürze verfügbare User-Agent-Zeichenfolge testen, indem sie das Experimentkennzeichen **#force-major-version-to-100** unter *edge://flags* aktivieren, um sicherzustellen, dass ihre User-Agent Analyselogik stabil ist und wie erwartet funktioniert.

## <a name="version-960105475-january-21"></a>Version 96.0.1054.75: 21. Januar

Verschiedene Fehler und Leistungsprobleme für das Release „Stabil (Erweitert) wurden behoben.

## <a name="version-970107269-january-20"></a>Version 97.0.1072.69: 20. Januar

Sicherheitsupdates im Stabilen Kanal sind [hier](/deployedge/microsoft-edge-relnotes-security#january-20-2022) aufgeführt.

## <a name="version-970107262-january-13"></a>Version 97.0.1072.62: 13. Januar

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-960105472-january-6"></a>Version 96.0.1054.72: 6. Januar

Verschiedene Fehler und Leistungsprobleme für das Release „Stabil (Erweitert) wurden behoben.

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

<!---archive from Version 96.0.1054.29: November 19 to Version 94.0.992.57: October 27 --->
<!-- archive from Version 95.0.1020.30: October 21 to Version 94.0.992.37: September 30 -->
<!-- archive from Version 94.0.992.31: September 24 to Version 93.0.961.44: September 9  -->
<!--- Archive from Version 93.0.961.38: September 2 to Version 92.0.902.62: July 29 --->
<!-- Archive from Version 92.0.902.55: July 22 to Version 91.0.864.37: May 27 -->
<!-- Archive from 89.0.774.45: March 4 to 90.0.818.66: May 20 ->
<!-- Archive from 86.0.622.43: October 15 to beta 88.0.705.81: February 25  ->
<!-- Archive from 86.0.622.38-october-9 to beta 86.0.62.215-september-14  ->
<!-- Archived to version 84.0.522.40: July 16 -->

## <a name="see-also"></a>Weitere Informationen

- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)
