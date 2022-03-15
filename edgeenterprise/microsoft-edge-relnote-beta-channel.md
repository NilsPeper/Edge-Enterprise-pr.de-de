---
title: Anmerkungen zu dieser Version von Microsoft Edge für Beta-Kanal
ms.author: leahtu
author: dan-wesley
manager: srugh
ms.date: 03/14/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Anmerkungen zu dieser Version von Microsoft Edge für Beta-Kanal
ms.openlocfilehash: 8633a5f15fe737a64a0160de714c1c4e53541482
ms.sourcegitcommit: 556aca8dde42dd66364427f095e8e473b86651a0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2022
ms.locfileid: "12445709"
---
# <a name="release-notes-for-microsoft-edge-beta-channel"></a>Versionshinweise für Microsoft Edge Beta-Kanal

Diese Versionshinweise enthalten Informationen zu neuen Funktionen und nicht sicherheitsrelevanten Updates, die im Microsoft Edge Beta-Kanal enthalten sind. Archivierte Versionen dieser Versionshinweise sind in [den archivierten Versionshinweisen für Microsoft Edge Beta Channel](./microsoft-edge-relnote-archive-beta-channel.md) verfügbar.

> [!NOTE]
> Die Microsoft Edge-Webplattform entwickelt sich ständig weiter, um Benutzerfreundlichkeit, Sicherheit und Datenschutz zu verbessern. Weitere Informationen finden Sie unter [Kommende Änderungen in Microsoft Edge mit Auswirkungen auf die Websitekompatibilität](/microsoft-edge/web-platform/site-impacting-changes).

## <a name="version-990115039-march-10"></a>Version 99.0.1150.39: 10. März

### <a name="feature-updates"></a>Funktionsupdate

- **Verbesserungen bei der Verwaltung von Cloudwebsitelisten für den IE-Modus.** Identifizieren Sie Lücken in Ihrer Enterprise-Websiteliste, indem Sie die Berichterstattung über Websitefeedback mit den Richtlinien ["InternetExplorerIntegrationCloudUserSitesReporting](/deployedge/microsoft-edge-policies#internetexplorerintegrationcloudusersitesreporting) " und ["InternetExplorerIntegrationCloudNeutralSitesReporting](/deployedge/microsoft-edge-policies#internetexplorerintegrationcloudneutralsitesreporting) " konfigurieren. Sie können lokale Websitelisten-URLs von Benutzern und möglicherweise falsch konfigurierte neutrale Website-URLs im Microsoft Edge Websitelisten im Microsoft 365 Admin Center anzeigen. Weitere Informationen finden Sie unter [Anzeigen des Websitefeedbacks im Microsoft 365 Admin Center](/deployedge/edge-ie-mode-cloud-site-list-mgmt#view-site-feedback-on-the-microsoft-365-admin-center-1).  **Hinweis:** Dies ist ein kontrolliertes Featurerollout. Wenn dieses Feature nicht angezeigt wird, checken Sie zurück, während wir unseren Rollout fortsetzen.

## <a name="version-990115030-march-2"></a>Version 99.0.1150.30: 2. März

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-990115025-february-25"></a>Version 99.0.1150.25: 25. Februar

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-990115021-february-22"></a>Version 99.0.1150.21: 22. Februar

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-990115016-february-14"></a>Version 99.0.1150.16: 14. Februar

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-990115011-february-9"></a>Version 99.0.1150.11: 9. Februar

### <a name="feature-updates"></a>Funktionsupdate

- **Bevorstehende dreistellige Versionsnummer in der Benutzer-Agent-Zeichenfolge.** Ab Version 100 sendet Microsoft Edge eine dreistellige Versionsnummer im User-Agent Header, z. B. "Edg/100". Ab Microsoft Edge 97 können Websitebesitzer diese anstehende Agent-Zeichenfolge testen, indem sie das Experimentkennzeichen **#force-Major-Version-zu-100** in *edge://flags* aktivieren, um sicherzustellen, dass ihre User-Agent Analyselogik stabil ist und wie erwartet funktioniert.

- **Personalisieren Sie Multi-Profile-Umgebungen mit Profileinstellungen für Websites.** Benutzer können ihre Erfahrung mit mehreren Profilen personalisieren, indem sie eine angepasste Liste von Websites für den automatischen Profilwechsel in Microsoft Edge erstellen können.

- **Bidirektionale Cookiefreigabe für den IE-Modus.** Dieses Feature erweitert die bereits verfügbare Cookiefreigabefunktion und ermöglicht Benutzern das Synchronisieren bestimmter Sitzungscookies aus dem Internet Explorer/IE-Modus mit Microsoft Edge. Weitere Informationen finden Sie unter [Cookie-Freigabe zwischen Microsoft Edge und Internet Explorer](/deployedge/edge-ie-mode-add-guidance-cookieshare).

- **Navigieren Sie in PDF-Dokumenten mit Miniaturansichten der Seite.** Sie können nun mithilfe von Miniaturansichten, die die Seiten darstellen, durch Ihr PDF-Dokument navigieren. Diese Miniaturansichten werden im Bereich auf der linken Seite des PDF-Readers angezeigt.

- **Konfigurieren Sie die Liste der Domänen, für die die Benutzeroberfläche des Kennwort-Managers für "Speichern" und "Ausfüllen" deaktiviert wird.** Verwenden Sie die [PasswordManagerBlocklist-Richtlinie](/deployedge/microsoft-edge-policies#passwordmanagerblocklist), um die Liste der Domänen zu konfigurieren (nur HTTP/HTTPS-Schemas und Hostnamen), in denen Microsoft Edge den Kennwort-Manager deaktivieren sollten. Dies bedeutet, dass Save and Fill-Workflows deaktiviert werden, wodurch sichergestellt wird, dass Kennwörter für diese Websites nicht gespeichert oder automatisch in Webformulare gefüllt werden können.

- **Aktualisieren Sie Erweiterungen für den Microsoft Edge-Add-Ons-Speicher mithilfe von APIs (in der öffentlichen Vorschau).** Sie können diese APIs direkt in Ihre Buildpipeline integrieren und Paketupdates auf der Microsoft Edge Add-On-Website veröffentlichen. Weitere Informationen finden Sie unter [Verwenden der Microsoft Edge-Add-Ons-API (in der privaten Vorschau)](/microsoft-edge/extensions-chromium/publish/api/using-addons-api)

### <a name="policy-updates"></a>Richtlinienupdates

#### <a name="new-policies"></a>Neue Richtlinien

- [AllowGamesMenu](/DeployEdge/microsoft-edge-policies#allowgamesmenu) – Benutzern den Zugriff auf das Spielemenü gestatten
- [DoNotSilentlyBlockProtocolsFromOrigins](/DeployEdge/microsoft-edge-policies#donotsilentlyblockprotocolsfromorigins) – Definieren einer Liste von Protokollen, die nicht im Hintergrund durch den Anti-Flood-Schutz blockiert werden können
- [HubsSidebarEnabled](/DeployEdge/microsoft-edge-policies#hubssidebarenabled) – Hub-Randleiste anzeigen
- [InternetExplorerIntegrationCloudNeutralSitesReporting](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationcloudneutralsitesreporting) – Konfigurieren der Berichterstellung potenziell falsch konfigurierter neutraler Website-URLs für die M365 Admin Center Site Lists-App
- [InternetExplorerIntegrationCloudUserSitesReporting](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationcloudusersitesreporting) – Konfigurieren der Berichterstellung von Benutzerlisteneinträgen für den IE-Modus für die M365 Admin Center Site Lists-App
- [PasswordManagerBlocklist](/DeployEdge/microsoft-edge-policies#passwordmanagerblocklist) – Konfigurieren der Liste der Domänen, für die die Kennwort-Manager-Benutzeroberfläche (Speichern und Ausfüllen) deaktiviert wird
- [RelatedMatchesCloudServiceEnabled](/DeployEdge/microsoft-edge-policies#relatedmatchescloudserviceenabled) – Konfigurieren verwandter Übereinstimmungen in "Auf Seite suchen"
- [SignInCtaOnNtpEnabled](/DeployEdge/microsoft-edge-policies#signinctaonntpenabled) – Aktivieren des Dialogfelds "Click to action anmelden"
- [UserAgentReduction](/DeployEdge/microsoft-edge-policies#useragentreduction) – Aktivieren oder Deaktivieren der User-Agent-Reduzierung

## <a name="version-980110848-february-8"></a>Version 98.0.1108.48: 8. Februar

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-980110843-february-3"></a>Version 98.0.1108.43: 3. Februar

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-980110842-february-2"></a>Version 98.0.1108.42: 2. Februar

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-980110839-january-31"></a>Version 98.0.1108.39: 31. Januar

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-980110833-january-24"></a>Version 98.0.1108.33: 24. Januar

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-980110827-january-19"></a>Version 98.0.1108.27: 19. Januar

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-980110823-january-14"></a>Version 98.0.1108.23: 14. Januar

### <a name="feature-updates"></a>Funktionsupdate

- **Verbessern Sie Ihre Sicherheit im Web.** Ein Browsermodus in Microsoft Edge, in dem die Sicherheit Ihres Browsers Vorrang hat, wodurch Sie beim Surfen im Web eine zusätzliche Schutzebene erhalten. Administratoren können die folgenden Gruppenrichtlinien auf Endbenutzerdesktops (Windows, macOS und Linux) anwenden, um sich vor Zero Days zu schützen. Diese Richtlinien sorgen außerdem dafür, dass wichtige Websites und Branchenanwendungen weiterhin wie erwartet funktionieren. Dieses Feature ist ein großer Schritt nach vorn, da es uns ermöglicht, unvorhergesehene aktive Nulltage (basierend auf historischen Trends) zu minimieren. Wenn dieses Feature aktiviert ist, bietet es hardwareerzwingten Stack Protection, Arbitrary Code Guard (ACG) und Content Flow Guard (CFG), um Sicherheitsminderungen zu unterstützen, um die Sicherheit der Benutzer im Web zu erhöhen.
Gruppenrichtlinien:
  - [EnhanceSecurityMode](/DeployEdge/microsoft-edge-policies#enhancesecuritymode)
  - [EnhanceSecurityModeBypassListDomains](/DeployEdge/microsoft-edge-policies#enhancesecuritymodebypasslistdomains)
  - [EnhanceSecurityModeEnforceListDomains](/DeployEdge/microsoft-edge-policies#enhancesecuritymodeenforcelistdomains)

- **Benutzerdefiniertes primäres Kennwort.** Der Browser verfügt bereits über die Funktion, in der Benutzer einen Authentifizierungsschritt hinzufügen können, bevor gespeicherte Kennwörter automatisch in Webformularen ausgefüllt werden. Dadurch wird eine weitere Datenschutzebene hinzugefügt und verhindert, dass nicht autorisierte Benutzer gespeicherte Kennwörter zum Anmelden bei Websites verwenden. Ein benutzerdefiniertes primäres Kennwort ist eine Weiterentwicklung desselben Features, bei dem Benutzer jetzt eine benutzerdefinierte Zeichenfolge ihrer Wahl als primäres Kennwort verwenden können. Nachdem es aktiviert wurde, geben Benutzer dieses Kennwort ein, um sich selbst zu authentifizieren und ihre gespeicherten Kennwörter automatisch in Webformulare zu füllen.

- **Zu Microsoft Edge hinzugefügte Überlagerungs-Bildlaufleisten.** Wir haben unsere Bildlaufleisten mit einem überlagerten Design aktualisiert. Benutzer können dieses Feature in *edge://flags* aktivieren.

### <a name="policy-updates"></a>Richtlinienupdates

#### <a name="new-policies"></a>Neue Richtlinien

- [AddressBarEditingEnabled](/DeployEdge/microsoft-edge-policies#addressbareditingenabled) : Konfigurieren der Bearbeitung der Adressleiste.
- [EdgeFollowEnabled](/DeployEdge/microsoft-edge-policies#edgefollowenabled) : Aktivieren Sie den Follow-Dienst in Microsoft Edge.
- [EnhanceSecurityMode](/DeployEdge/microsoft-edge-policies#enhancesecuritymode) – Verbessern des Sicherheitsstatus in Microsoft Edge.
- [EnhanceSecurityModeBypassListDomains](/DeployEdge/microsoft-edge-policies#enhancesecuritymodebypasslistdomains) : Konfigurieren Sie die Liste der Domänen, für die der Sicherheitsmodus verbessert wird, nicht erzwungen wird.
- [EnhanceSecurityModeEnforceListDomains](/DeployEdge/microsoft-edge-policies#enhancesecuritymodeenforcelistdomains) : Konfigurieren Sie die Liste der Domänen, für die der Sicherheitsmodus verbessert wird, immer erzwungen wird.
- [InAppSupportEnabled](/DeployEdge/microsoft-edge-policies#inappsupportenabled) – In-App-Unterstützung aktiviert.
- [MicrosoftEdgeInsiderPromotionEnabled](/DeployEdge/microsoft-edge-policies#microsoftedgeinsiderpromotionenabled) – Microsoft Edge Insider Promotion aktiviert.
- [PrintStickySettings](/DeployEdge/microsoft-edge-policies#printstickysettings) – Druckvorschau-Sticky-Einstellungen.
- [SandboxExternalProtocolBlocked](/DeployEdge/microsoft-edge-policies#sandboxexternalprotocolblocked) – Microsoft Edge erlauben, Navigationen zu externen Protokollen in einem Sandkasten-iframe zu blockieren.
- [U2fSecurityKeyApiEnabled](/DeployEdge/microsoft-edge-policies#u2fsecuritykeyapienabled) – Verwendung der veralteten U2F-Sicherheitsschlüssel-API zulassen.

## <a name="version-970107254-january-5"></a>Version 97.0.1072.54: 5. Januar

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-970107252-january-3"></a>Version 97.0.1072.52: 3. Januar

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-970107241-december-20"></a>Version 97.0.1072.41: 20. Dezember

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-970107234-december-13"></a>Version 97.0.1072.34: 13. Dezember

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-970107228-december-8"></a>Version 97.0.1072.28: 8. Dezember

Verschiedene Fehler und Leistungsprobleme wurden behoben.

<!--- Version 97.0.1072.21: December 1 to Version 96.0.1054.13: November 5  --->
<!--- archive from Version 96.0.1054.8: November 1 to Version 95.0.1020.14: October 5  --->
<!-- archive from version 95.0.1020.9: September 28 to version 94.0.992.14: September 7 ---->
<!-- archive from Version 94.0.992.9: September 2 to Version 92.0.902.40: July 6 -->
<!--Archive on Oct 27 From Version 92.0.902.22: June 21 to Version 89.0.774.23: February 8  -->
<!--- Archived from Version 87.0.664.18: October 26 to to version 89.0.774.18: February 3 ---->
<!--- Archived from Version 87.0.664.12: October 20 to to version 86.0.622.15: September 14 ---->
<!--- Archived to version 86.0.622.11: September 9 ---->
<!--- Archived to version 85.0.564.18: July 28 ---->

## <a name="see-also"></a>Weitere Informationen

- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)

