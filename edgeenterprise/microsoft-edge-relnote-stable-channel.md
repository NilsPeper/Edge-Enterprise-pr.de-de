---
title: Versionshinweise von Microsoft Edge für Stable Channel
ms.author: leahtu
author: dan-wesley
manager: srugh
ms.date: 04/07/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Versionshinweise von Microsoft Edge für Stable Channel
ms.openlocfilehash: 0cf9c2d0ac7a60c03ad6c80d4186629d296a73c6
ms.sourcegitcommit: dd8cdbd35726c795ddce917e549ddf17ee7f5290
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/11/2022
ms.locfileid: "12473665"
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

## <a name="version-1000118536-april-7"></a>Version 100.0.1185.36: 7. April

Stable Channel-Sicherheitsupdates sind [hier](/deployedge/microsoft-edge-relnotes-security#april-7-2022) aufgeführt.

## <a name="version-1000118529-april-1"></a>Version 100.0.1185.29: 1. April

Sicherheitsupdates im Stabilen Kanal sind [hier](/deployedge/microsoft-edge-relnotes-security#april-1-2022) aufgeführt.

### <a name="feature-updates"></a>Funktionsupdates

- **Dreistellige Versionsnummer im User-Agent-String.** Microsoft Edge sendet nun eine dreistellige Versionsnummer, z. B. Edg/100, im User-Agent-Header. Dies kann Skripte oder serverseitige Analysen verwirren, die einen fehlerhaften Parser verwenden, um die Versionsnummer der User-Agent-Zeichenfolge zu ermitteln. Sie können die [ForceMajorVersionToMinorPositionInUserAgent-Richtlinie](/deployedge/microsoft-edge-policies#forcemajorversiontominorpositioninuseragent) verwenden, um zu steuern, ob die User-Agent Hauptversion der Zeichenfolge bei 99 fixiert werden soll. Außerdem ist das **Flag #force Hauptversion zu Nebenversion** in *edge://flags* verfügbar, um die Hauptversion in der Zeichenfolge User-Agent auf 99 zu fixieren.

- **Rationalisierung Microsoft 365 Anwendungsprotokollaktivierungen.** Microsoft 365 Anwendungsprotokollaktivierungen für vertrauenswürdige Microsoft-Cloudspeicherdienste starten jetzt bestimmte Microsoft 365 Anwendungen direkt, einschließlich SharePoint Unterdomänen und Microsoft OneDrive URLs. Sie können die Richtlinien ["AutoLaunchProtocolsComponentEnabled](/deployedge/microsoft-edge-policies#autolaunchprotocolscomponentenabled) " und ["AutoLaunchProtocolsFromOrigins](/deployedge/microsoft-edge-policies#autolaunchprotocolsfromorigins) " verwenden, um bei Bedarf die Aktivierungsaufforderungen des Anwendungsprotokolls zu aktivieren und andere Anwendungen und Dienste zu definieren, bei denen Warnungen aktiviert oder deaktiviert sind.

- **Hardware-erzwungener Stack-Schutz.** Microsoft Edge wird beginnen, einen differenzierteren Schutz zu unterstützen, indem Sicherheitsrisiken aufgrund von Speicherbeschädigungen behoben und indirekte Aufrufe geschützt werden. Hardwaredurchsetzter Stapelschutz wird nur von Windows 8 und höher unterstützt. Weitere Informationen finden Sie unter [Hardware-erzwungener Stapelschutz](https://techcommunity.microsoft.com/t5/windows-kernel-internals-blog/developer-guidance-for-hardware-enforced-stack-protection/ba-p/2163340). Dieses Featureverhalten kann mithilfe der [ShadowStackCrashRollbackBehavior-Richtlinie](/deployedge/microsoft-edge-policies#shadowstackcrashrollbackbehavior) gesteuert werden.

- **Vorschau von PDF-Dateien in Microsoft Outlook und Explorer.** Benutzer können eine PDF-Datei in einer einfachen und umfangreichen schreibgeschützten Vorschau anzeigen. Dieses Feature ist für Outlook Desktop-PDF-Anlagen oder für lokale PDF-Dateien mit Explorer verfügbar.

- **Öffnen Sie digital signierte PDF-Dateien.** Digitale Signaturen werden umfassend verwendet, um die Echtheit eines Dokuments und die in einem Dokument vorgenommenen Änderungen zu überprüfen. Sie können die [PDFSecureMode-Richtlinie](/deployedge/microsoft-edge-policies#pdfsecuremode) verwenden, um die Validierung digitaler Signaturen für PDF-Dateien direkt über den Browser zu aktivieren, ohne dass Add-Ins erforderlich sind.

### <a name="policy-updates"></a>Richtlinienupdates

#### <a name="new-policies"></a>Neue Richtlinien

- [Konfigurieren, ob ](/DeployEdge/microsoft-edge-policies#adstransparencyenabled)das Anzeigentransparenzfeature aktiviert ist
- [Verwendung der WebHID-API steuern](/DeployEdge/microsoft-edge-policies#defaultwebhidguardsetting)
- [Dialogfeld „Seiten wiederherstellen“ nach Browserabsturz](/DeployEdge/microsoft-edge-policies#hiderestoredialogenabled) ausblenden
- [Sicherer Modus und Überprüfung der ](/DeployEdge/microsoft-edge-policies#pdfsecuremode)zertifikatbasierten digitalen Signatur im nativen PDF-Reader
- [Fordert den Benutzer auf, ein ](/DeployEdge/microsoft-edge-policies#promptonmultiplematchingcertificates)Zertifikat auszuwählen, wenn mehrere Zertifikate übereinstimmen
- [WebHID-API auf ](/DeployEdge/microsoft-edge-policies#webhidaskforurls)diesen Websites zulassen
- [WebHID-API auf ](/DeployEdge/microsoft-edge-policies#webhidblockedforurls)diesen Websites blockieren

#### <a name="deprecated-policy"></a>Veraltete Richtlinie

- [Aktiviert Hintergrundaktualisierungen](/DeployEdge/microsoft-edge-policies#backgroundtemplatelistupdatesenabled) der Liste verfügbarer Vorlagen für Kollektionen und andere Features, die Vorlagen verwenden

#### <a name="obsoleted-policy"></a>Veraltete Richtlinie

- [AllowSyncXHRInPageDismissal](/DeployEdge/microsoft-edge-policies#allowsyncxhrinpagedismissal): Seiten das Senden synchroner XHR-Anforderungen während der Seitenschließung ermöglichen.

## <a name="version-980110892-march-26"></a>Version 98.0.1108.92: 26. März

Verschiedene Fehler und Leistungsprobleme für das Release „Stabil (Erweitert) wurden behoben.

## <a name="version-990115055-march-26"></a>Version 99.0.1150.55: 26. März

> [!Important]
> Dieses Update enthält einen Fix für[ CVE-2022-1096](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2022-1096), der vom Chromium-Team als Exploit in wild gemeldet wurde. Weitere Informationen finden Sie im [Leitfaden zu Sicherheitsupdates](https://msrc.microsoft.com/update-guide).

Stable Channel-Sicherheitsupdates sind [hier](/deployedge/microsoft-edge-relnotes-security#march-26-2022) aufgeführt.

## <a name="version-990115052-march-24"></a>Version 99.0.1150.52: 24. März

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-980110884-march-17"></a>Version 98.0.1108.84: 17. März

Verschiedene Fehler und Leistungsprobleme für das Release „Stabil (Erweitert) wurden behoben.

## <a name="version-990115046-march-17"></a>Version 99.0.1150.46: 17. März

Stable Channel-Sicherheitsupdates sind [hier](/deployedge/microsoft-edge-relnotes-security#march-17-2022) aufgeführt.

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

<!---- From Version 97.0.1072.55: January 6 to Version 96.0.1054.34: November 23 ---->
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
