---
title: Anmerkungen zu dieser Version von Microsoft Edge für Beta-Kanal
ms.author: leahtu
author: dan-wesley
manager: srugh
ms.date: 04/08/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Anmerkungen zu dieser Version von Microsoft Edge für Beta-Kanal
ms.openlocfilehash: 8c2fcd1a45d6d6417e10609dec3cf1c669576c92
ms.sourcegitcommit: dd8cdbd35726c795ddce917e549ddf17ee7f5290
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/11/2022
ms.locfileid: "12473561"
---
# <a name="release-notes-for-microsoft-edge-beta-channel"></a>Versionshinweise für Microsoft Edge Beta-Kanal

Diese Versionshinweise enthalten Informationen zu neuen Funktionen und nicht sicherheitsrelevanten Updates, die im Microsoft Edge Beta-Kanal enthalten sind. Archivierte Versionen dieser Versionshinweise sind in [den archivierten Versionshinweisen für den Betakanal von Microsoft Edge](./microsoft-edge-relnote-archive-beta-channel.md) verfügbar.

> [!NOTE]
> Die Microsoft Edge-Webplattform entwickelt sich ständig weiter, um Benutzerfreundlichkeit, Sicherheit und Datenschutz zu verbessern. Weitere Informationen finden Sie unter [Kommende Änderungen in Microsoft Edge mit Auswirkungen auf die Websitekompatibilität](/microsoft-edge/web-platform/site-impacting-changes).

## <a name="version-1010121010-april-8"></a>Version 101.0.1210.10: 8. April

### <a name="feature-updates"></a>Funktionsupdates

- **Möglichkeit zum Festlegen des Standardprofils.** [Mit der EdgeDefaultProfileEnabled-Richtlinie](/DeployEdge/microsoft-edge-policies#edgedefaultprofileenabled) können Sie ein Standardprofil festlegen, das beim Öffnen des Browsers anstelle des zuletzt verwendeten Profils verwendet werden soll. Diese Richtlinie gilt nicht, wenn der `--profile-directory` Parameter angegeben wurde.

- **Client Certificate Switcher.** Dieses Feature bietet Benutzern die Möglichkeit, das gespeicherte Zertifikat zu löschen und die Zertifikatauswahl erneut zu öffnen, wenn sie eine Website besuchen, die http-Zertifikatauthentifizierung erfordert. Dies kann ohne manuelles Beenden von Microsoft Edge erfolgen.

- **Starten Sie progressive Web-Apps (PWAs) über die Favoritenleiste.** Verbesserungen an der PWA-Startumgebung werden beginnend mit einem App-Symbol angezeigt, das der Symbolleiste hinzugefügt werden kann.

- **Verwalten Sie die Einstellung "Erweiterungen aus anderen Stores zulassen".** Verwenden Sie die [ControlDefaultStateOfAllowExtensionFromOtherStoresSettingEnabled-Richtlinie](/DeployEdge/microsoft-edge-policies#controldefaultstateofallowextensionfromotherstoressettingenabled) , um den Standardstatus der Einstellung "Erweiterungen aus anderen Speichern zulassen" zu steuern.

### <a name="policy-updates"></a>Richtlinienupdates

#### <a name="new-policies"></a>Neue Richtlinien

- [ConfigureKeyboardShortcuts](/DeployEdge/microsoft-edge-policies#configurekeyboardshortcuts) – Konfigurieren der Liste der Befehle zum Deaktivieren von Tastenkombinationen
- [ControlDefaultStateOfAllowExtensionFromOtherStoresSettingEnabled](/DeployEdge/microsoft-edge-policies#controldefaultstateofallowextensionfromotherstoressettingenabled) – Konfigurieren des Standardstatus von "Erweiterungen aus anderen Speichereinstellungen zulassen"
- [EdgeAssetDeliveryServiceEnabled](/DeployEdge/microsoft-edge-policies#edgeassetdeliveryserviceenabled) – Features das Herunterladen von Ressourcen aus dem Asset Delivery Service erlauben
- [EdgeDefaultProfileEnabled](/DeployEdge/microsoft-edge-policies#edgedefaultprofileenabled) – Standardprofileinstellung aktiviert
- [InternetExplorerModeEnableSavePageAs](/DeployEdge/microsoft-edge-policies#internetexplorermodeenablesavepageas) – Seite "Speichern" im Internet Explorer-Modus zulassen
- [KioskSwipeGesturesEnabled](/DeployEdge/microsoft-edge-policies#kioskswipegesturesenabled) – Wischgesten im Microsoft Edge-Kioskmodus aktiviert
- [MicrosoftOfficeMenuEnabled](/DeployEdge/microsoft-edge-policies#microsoftofficemenuenabled) – Benutzern den Zugriff auf das Menü "Microsoft Office" ermöglichen
- [SiteSafetyServicesEnabled](/DeployEdge/microsoft-edge-policies#sitesafetyservicesenabled) – Zulassen, dass Benutzer Websitesicherheitsdienste konfigurieren

#### <a name="deprecated-policy"></a>Veraltete Richtlinie

- [ForceCertificatePromptsOnMultipleMatches](/DeployEdge/microsoft-edge-policies#forcecertificatepromptsonmultiplematches) – Konfigurieren, ob Microsoft Edge automatisch ein Zertifikat auswählen soll, wenn mehrere Zertifikatübereinstimmungen für eine Mit "AutoSelectCertificateForUrls" konfigurierte Website vorhanden sind

#### <a name="obsoleted-policy"></a>Veraltete Richtlinie

- [WebSQLInThirdPartyContextEnabled](/DeployEdge/microsoft-edge-policies#websqlinthirdpartycontextenabled): Erzwingen der erneuten Aktivierung von WebSQL in Drittanbieterkontexten


## <a name="version-1000118527-march-31"></a>Version 100.0.1185.27: 31. März

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-1000118523-march-28"></a>Version 100.0.1185.23: 28. März

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-1000118517-march-23"></a>Version 100.0.1185.17: 23. März

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-1000118512-march-18"></a>Version 100.0.1185.12: 18. März

Verschiedene Fehler und Leistungsprobleme wurden behoben.

### <a name="feature-updates"></a>Funktionsupdate

- **Rationalisierung Microsoft 365 Anwendungsprotokollaktivierungen.** Microsoft 365 Anwendungsprotokollaktivierungen für vertrauenswürdige Microsoft-Cloudspeicherdienste starten jetzt bestimmte Microsoft 365 Anwendungen direkt, einschließlich SharePoint Unterdomänen und Microsoft OneDrive URLs. Sie können die Richtlinien ["AutoLaunchProtocolsComponentEnabled](/deployedge/microsoft-edge-policies#autolaunchprotocolscomponentenabled) " und ["AutoLaunchProtocolsFromOrigins](/deployedge/microsoft-edge-policies#autolaunchprotocolsfromorigins) " verwenden, um bei Bedarf die Aktivierungsaufforderungen des Anwendungsprotokolls zu aktivieren und andere Anwendungen und Dienste zu definieren, bei denen Warnungen aktiviert oder deaktiviert sind.

## <a name="version-1000118510-march-17"></a>Version 100.0.1185.10: 17. März

### <a name="feature-updates"></a>Funktionsupdates

- **Verbesserungen bei der Verwaltung von Cloudwebsitelisten für den IE-Modus.** Sie können die Sitzungscookiefreigabe zwischen Microsoft Edge und Internet Explorer für den IE-Modus in Ihrer Websiteliste im Microsoft 365 Admin Center konfigurieren. **Hinweis:** Dies ist ein kontrolliertes Featurerollout. Wenn dieses Feature nicht angezeigt wird, schauen Sie erneut nach, während wir unseren Rollout fortsetzen.

- **Vorschau von PDF-Dateien in Microsoft Outlook und Explorer.** Benutzer können eine PDF-Datei in einer einfachen und umfangreichen schreibgeschützten Vorschau anzeigen.  Verfügbar für Outlook Desktop-PDF-Anlagen oder für lokale PDF-Dateien mit Explorer.  

- **Installierte Web-App-Synchronisierung auf allen Desktopgeräten.** Websites oder progressive Web-Apps (PWAs), die als Anwendungen installiert wurden, werden auf allen Desktopgeräten synchronisiert, bei denen Sie sich angemeldet haben, und die Synchronisierung aktiviert. Sie werden als "Verfügbare Apps" angezeigt, die Sie installieren können. Eine App, die von einem Gerät entfernt wurde, synchronisiert die Entfernung auf allen Geräten.

### <a name="policy-updates"></a>Richtlinienupdates

#### <a name="new-policies"></a>Neue Richtlinien

- [AdsTransparencyEnabled](/DeployEdge/microsoft-edge-policies#adstransparencyenabled) – Konfigurieren, ob das Feature "Anzeigentransparenz" aktiviert ist
- [DefaultWebHidGuardSetting](/DeployEdge/microsoft-edge-policies#defaultwebhidguardsetting) – Steuern der Verwendung der WebHID-API
- [HideRestoreDialogEnabled](/DeployEdge/microsoft-edge-policies#hiderestoredialogenabled) – Dialogfeld zum Wiederherstellen von Seiten nach dem Browserabsturz ausblenden
- [PDFSecureMode](/DeployEdge/microsoft-edge-policies#pdfsecuremode) – Sicherer Modus und zertifikatbasierte Überprüfung digitaler Signaturen im nativen PDF-Reader
- [PromptOnMultipleMatchingCertificates](/DeployEdge/microsoft-edge-policies#promptonmultiplematchingcertificates) – Auffordern des Benutzers, ein Zertifikat auszuwählen, wenn mehrere Zertifikate übereinstimmen
- [WebHidAskForUrls](/DeployEdge/microsoft-edge-policies#webhidaskforurls) – Zulassen der WebHID-API auf diesen Websites
- [WebHidBlockedForUrls](/DeployEdge/microsoft-edge-policies#webhidblockedforurls) – Blockieren der WebHID-API auf diesen Websites

#### <a name="deprecated-policy"></a>Veraltete Richtlinie

- [BackgroundTemplateListUpdatesEnabled](/DeployEdge/microsoft-edge-policies#backgroundtemplatelistupdatesenabled) – Ermöglicht Hintergrundaktualisierungen der Liste der verfügbaren Vorlagen für Sammlungen und andere Features, die Vorlagen verwenden

#### <a name="obsoleted-policy"></a>Veraltete Richtlinie

- [AllowSyncXHRInPageDismissal](/DeployEdge/microsoft-edge-policies#allowsyncxhrinpagedismissal) – Zulassen, dass Seiten synchrone XHR-Anforderungen während der Seitenentlassung senden

## <a name="version-990115039-march-10"></a>Version 99.0.1150.39: 10. März

### <a name="feature-updates"></a>Funktionsupdates

- **Verbesserungen bei der Verwaltung von Cloudwebsitelisten für den IE-Modus.** Identifizieren Sie Lücken in Ihrer Unternehmenswebsiteliste, indem Sie die Berichterstattung über Websitefeedback mit den Richtlinien ["InternetExplorerIntegrationCloudUserSitesReporting](/deployedge/microsoft-edge-policies#internetexplorerintegrationcloudusersitesreporting) " und ["InternetExplorerIntegrationCloudNeutralSitesReporting"](/deployedge/microsoft-edge-policies#internetexplorerintegrationcloudneutralsitesreporting) konfigurieren. Sie können URLs für lokale Websitelisten von Benutzern und möglicherweise falsch konfigurierte neutrale Website-URLs in der Microsoft Edge-Websitelistenoberfläche im Microsoft 365 Admin Center anzeigen. Weitere Informationen finden Sie unter ["Websitefeedback anzeigen" im Microsoft 365 Admin Center](/deployedge/edge-ie-mode-cloud-site-list-mgmt#view-site-feedback-on-the-microsoft-365-admin-center-1).  **Hinweis:** Dies ist ein kontrolliertes Featurerollout. Wenn dieses Feature nicht angezeigt wird, schauen Sie wieder nach, während wir unseren Rollout fortsetzen.

## <a name="version-990115030-march-2"></a>Version 99.0.1150.30: 2. März

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-990115025-february-25"></a>Version 99.0.1150.25: 25. Februar

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-990115021-february-22"></a>Version 99.0.1150.21: 22. Februar

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-990115016-february-14"></a>Version 99.0.1150.16: 14. Februar

Verschiedene Fehler und Leistungsprobleme wurden behoben.

<!--- From Version 99.0.1150.11: February 9 to Version 98.0.1108.27: January 19 --->
<!-- archive from Version 98.0.1108.23: January 14 to Version 97.0.1072.28: December 8 -->
<!--- Version 97.0.1072.21: December 1 to Version 96.0.1054.13: November 5  --->
<!--- archive from Version 96.0.1054.8: November 1 to Version 95.0.1020.14: October 5  --->
<!-- archive from version 95.0.1020.9: September 28 to version 94.0.992.14: September 7 -->
<!-- archive from Version 94.0.992.9: September 2 to Version 92.0.902.40: July 6 -->
<!--Archive from Version 92.0.902.22: June 21 to Version 89.0.774.23: February 8  -->
<!-- Archive from Version 87.0.664.18: October 26 to to version 89.0.774.18: February 3 --->
<!-- Archive from Version 87.0.664.12: October 20 to version 86.0.622.15: September 14 -->
<!--- Archived to version 86.0.622.11: September 9 ---->
<!--- Archived to version 85.0.564.18: July 28 ---->

## <a name="see-also"></a>Weitere Informationen

- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)

