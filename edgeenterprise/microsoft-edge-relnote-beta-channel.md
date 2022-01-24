---
title: Anmerkungen zu dieser Version von Microsoft Edge für Beta-Kanal
ms.author: aguta
author: dan-wesley
manager: srugh
ms.date: 01/07/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Anmerkungen zu dieser Version von Microsoft Edge für Beta-Kanal
ms.openlocfilehash: ddb745c206dc392dc1dbb46a0522db9648ba624e
ms.sourcegitcommit: e7f3098d8b7d91cae20b5778a71a87daababc312
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2022
ms.locfileid: "12297713"
---
# <a name="release-notes-for-microsoft-edge-beta-channel"></a>Versionshinweise für Microsoft Edge Beta-Kanal

Diese Versionshinweise enthalten Informationen zu neuen Funktionen und nicht sicherheitsrelevanten Updates, die im Microsoft Edge Beta-Kanal enthalten sind. Archivierte Versionen dieser Versionshinweise sind in [den archivierten Versionshinweisen für Microsoft Edge Beta Channel](./microsoft-edge-relnote-archive-beta-channel.md)verfügbar.

> [!NOTE]
> Die Microsoft Edge-Webplattform entwickelt sich ständig weiter, um Benutzerfreundlichkeit, Sicherheit und Datenschutz zu verbessern. Weitere Informationen finden Sie unter [Kommende Änderungen in Microsoft Edge mit Auswirkungen auf die Websitekompatibilität](/microsoft-edge/web-platform/site-impacting-changes).

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

## <a name="version-970107221-december-1"></a>Version 97.0.1072.21: 1. Dezember

### <a name="feature-updates"></a>Funktionsupdate

- **Verwenden Sie das aktuelle Profil, um sich bei Websites anzumelden, wenn mehrere Geschäfts-, Schul- oder Unikonten auf einem Gerät angemeldet sind.** Wenn mehrere Geschäfts-, Schul- oder Unikonten auf einem Gerät angemeldet sind, werden Benutzer aufgefordert, ein Konto aus der Kontoauswahl auszuwählen, um ihre Besuche auf Websites fortzusetzen. In dieser Version werden Benutzer aufgefordert, Microsoft Edge die automatische Anmeldung bei den Websites mit dem Geschäfts-, Schul- und Unikonto zu erlauben, das beim aktuellen Profil angemeldet ist. Benutzer können dieses Feature in **Einstellungen/Profileinstellungen**aktivieren und deaktivieren.

- **Fügen Sie Unterstützung für Microsoft Endpoint Data Loss Prevention (DLP) unter macOS hinzu.** Die Erzwingung von Microsoft Endpoint DLP-Richtlinien ist nativ unter macOS verfügbar.

- **Öffnen Sie digital signierte PDF-Dateien.**  Digitale Signaturen werden umfassend verwendet, um die Echtheit eines Dokuments zu überprüfen und Änderungen an diesem Dokument vorzunehmen. Benutzer können die Signaturen für PDF-Dateien direkt im Browser überprüfen, ohne dass Add-Ins erforderlich sind.

- **Zitate in Microsoft Edge.** Das Angeben von Quellen für Die Forschung ist eine häufige Anforderung für Schüler/Studenten. Sie müssen viele Recherchereferenzen und Quellen verwalten, was keine einfachen Aufgaben ist. Sie müssen diese Zitate auch in richtige Zitatformate wie APA, MLA und Chicago übersetzen. Dieses neue Feature "Zitate" in Microsoft Edge (jetzt in der Vorschau) bietet Schülern eine bessere Möglichkeit, Zitate zu verwalten und zu generieren, während sie online recherchieren. Wenn Zitate in Sammlungen oder aus **Einstellungen und mehr (ALT-F)** aktiviert sind, generiert Microsoft Edge automatisch Zitate, die Schüler später verwenden können, damit sie sich auf ihre Forschung konzentrieren können. Wenn sie fertig sind, können sie diese Zitate ganz einfach zu einem endgültigen Lieferumfang kompilieren. Weitere Informationen finden Sie unter [Previewing Citations in Microsoft Edge](https://blogs.windows.com/msedgedev/2021/11/04/preview-citations-feature-edge/).

### <a name="policy-updates"></a>Richtlinienupdates

#### <a name="new-policies"></a>Neue Richtlinien

- [AccessibilityImageLabelsEnabled](/DeployEdge/microsoft-edge-policies#accessibilityimagelabelsenabled) – Abrufen von Bildbeschreibungen von Microsoft Enabled
- [CORSNonWildcardRequestHeadersSupport](/DeployEdge/microsoft-edge-policies#corsnonwildcardrequestheaderssupport) – Unterstützung für CORS-Anforderungsheader ohne Platzhalter aktiviert
- [EdgeDiscoverEnabled](/DeployEdge/microsoft-edge-policies#edgediscoverenabled) – Feature "Entdecken" in Microsoft Edge
- [EdgeEnhanceImagesEnabled](/DeployEdge/microsoft-edge-policies#edgeenhanceimagesenabled) – Verbessern von Bildern aktiviert
- [InternetExplorerModeTabInEdgeModeAllowed](/DeployEdge/microsoft-edge-policies#internetexplorermodetabinedgemodeallowed) – Zulassen, dass Websites, die für den Internet Explorer-Modus konfiguriert sind, in Microsoft Edge
- [SameOriginTabCaptureAllowedByOrigins](/DeployEdge/microsoft-edge-policies#sameorigintabcaptureallowedbyorigins) – Allow Same Origin Tab capture by these origins
- [ScreenCaptureAllowedByOrigins](/DeployEdge/microsoft-edge-policies#screencaptureallowedbyorigins) – Desktop-, Fenster- und Tab-Erfassung durch diese Ursprünge zulassen
- [SerialAllowAllPortsForUrls](/DeployEdge/microsoft-edge-policies#serialallowallportsforurls) – Websites automatisch die Berechtigung erteilen, alle seriellen Ports zu verbinden
- [SerialAllowUsbDevicesForUrls](/DeployEdge/microsoft-edge-policies#serialallowusbdevicesforurls) – Websites automatisch die Berechtigung erteilen, eine Verbindung mit seriellen USB-Geräten herzustellen
- [SmartScreenDnsRequestsEnabled](/DeployEdge/microsoft-edge-policies#smartscreendnsrequestsenabled) – Aktivieren Microsoft Defender SmartScreen DNS-Anforderungen
- [TabCaptureAllowedByOrigins](/DeployEdge/microsoft-edge-policies#tabcaptureallowedbyorigins) – Tab-Erfassung durch diese Ursprünge zulassen
- [WebSQLInThirdPartyContextEnabled](/DeployEdge/microsoft-edge-policies#websqlinthirdpartycontextenabled) – Erzwingen der erneuten Aktivierung von WebSQL in Drittanbieterkontexten
- [WindowCaptureAllowedByOrigins](/DeployEdge/microsoft-edge-policies#windowcaptureallowedbyorigins) – Zulassen der Erfassung von Fenstern und Registerkarten durch diese Ursprünge

## <a name="version-960105434-november-23"></a>Version 96.0.1054.34: 23. November

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-960105426-november-17"></a>Version 96.0.1054.26: 17. November

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-960105424-november-16"></a>Version 96.0.1054.24: 16. November

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-960105413-november-5"></a>Version 96.0.1054.13: 5. November

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-96010548-november-1"></a>Version 96.0.1054.8: 1. November

### <a name="feature-updates"></a>Funktionsupdates

- **Starten Sie progressive Web App (PWA) direkt über Protokolllinks.** Installed PWAs handle links that use a specific protocol for a more integrated experience.

- **Erfahren Sie, wie Sie mathematische Probleme mit Math Solver lösen.** Wir freuen uns, Ihnen mitteilen zu können, dass Sie Math Solver in Microsoft Edge verwenden können, um Hilfe bei einer Vielzahl mathematischer Konzepte zu erhalten. Diese Konzepte reichen von elementaren arithmetischen und quadratischen Formeln bis hin zu Trigonometrie und Berechnung. Mit Math Solver können Sie ein Bild eines handschriftlichen oder gedruckten mathematischen Problems erstellen und dann eine sofortige Lösung mit schrittweisen Anweisungen bereitstellen, mit denen Sie lernen können, wie Sie die Lösung ohne Hilfe erreichen. Math Solver verfügt auch über eine mathematische Tastatur, mit der Sie mathematische Probleme einfach eingeben können. Mit dieser Tastatur müssen Sie keine herkömmliche Tastatur durchsuchen, um die benötigten mathematischen Zeichen zu finden. Nach der Lösung Ihres Problems bietet Math Solver Optionen zum weiteren Lernen mit Quizfragen, Arbeitsblättern und Videolernprogrammen.

- **Freihandformhervorhebung auf PDFs.** Die PDF-Anzeige- und Markupoberfläche wird durch die Hinzufügung von Freihandformmarkern verbessert. Sie können Abschnitte in PDFs, auf die Sie keinen Zugriff haben, und gescannte Dokumente hervorheben.

- **Hardwareerzwingte Stack Protection.**  Microsoft Edge beginnen, einen noch sichereren Browsermodus zu unterstützen, der hardwareabhängigen Steuerungsfluss für Browserprozesse auf unterstützter Hardware (Intel 11. Generation) verwendet. oder AMD Zen 3). Hinweis: Da es sich um ein kontrolliertes Featurerollout handelt, bemerken Sie möglicherweise nicht, dass dieses Feature auf allen Geräten aktiviert ist. Sie können den hardwareerzwingten Stapelschutz aktivieren oder deaktivieren, indem Sie die Bilddateiausführungsoptionen (IFEO) mithilfe von Gruppenrichtlinien bearbeiten.

- **Neues Warndialogfeld für Tippfehler bei Websites.** Der Browser zeigt nun eine Warnung auf einigen Websites mit URLs an, die ähnlich wie andere Websites aussehen. Diese Benutzeroberfläche verwendet clientseitige Heuristiken, um Benutzer vor Websites zu warnen, die möglicherweise häufig verwendete Websites spoofen. Weitere Informationen finden Sie unter [Was ist Tippfehler?](https://support.microsoft.com/topic/what-is-typosquatting-54a18872-8459-4d47-b3e3-d84d9a362eb0).

- **Verbesserte Übergabe zwischen dem IE-Modus und dem modernen Browser.**  Ab dieser Version von Microsoft Edge enthalten navigations zwischen Microsoft Edge und Internet Explorer-Modus Formulardaten und zusätzliche HTTP-Header. Referrer-Header, Post-Daten, Formulardaten und Anforderungsmethoden werden auf den beiden Oberflächen korrekt weitergeleitet. Mithilfe der [InternetExplorerIntegrationComplexNavDataTypes-Richtlinie](/deployedge/microsoft-edge-policies#internetexplorerintegrationcomplexnavdatatypes) können Sie angeben, welche Datentypen einbezogen werden sollen. Weitere Informationen finden Sie in diesen häufig gestellten Fragen: [Meine Anwendung erfordert die Übertragung von POST-Daten zwischen dem IE-Modus und Microsoft Edge.](./edge-ie-mode-faq.md#my-application-requires-transferring-post-data-between-ie-mode-and-microsoft-edge-is-this-supported)

- **Cloud Site List Management für den IE-Modus in der öffentlichen Vorschau.**  Mit cloudbasierter Websitelistenverwaltung können Sie Ihre Websitelisten für den IE-Modus in der Cloud verwalten, ohne dass eine lokale Infrastruktur zum Hosten der Websiteliste Ihrer Organisation erforderlich ist. Sie können im Microsoft 365 Admin Center auf das Feature für die Verwaltung von Cloudwebsitelisten zugreifen, indem Sie die Benutzeroberfläche Microsoft Edge Websitelisten verwenden. Weitere Informationen finden Sie im Artikel zur [Cloud-Websitelistenverwaltung für den IE-Modus (Public Preview).](./edge-ie-mode-cloud-site-list-mgmt.md)

- **Aktualisieren Sie Microsoft Edge WebWiew2 mit WSUS.** IT-Administratoren, die WSUS zum Aktualisieren von Microsoft Edge verwenden, können auch Microsoft Edge WebView2 mithilfe von WSUS aktualisieren. Diese Funktion ermöglicht Administratoren einen einfacheren Wartungsprozess für Offlinegeräte.

- **WSUS-Updates für Server.** WSUS- und Katalogupdates für Microsoft Edge Kanäle (Stable, Beta, Dev) gelten jetzt für Windows Server-SKUs, die Microsoft Edge installiert haben, einschließlich Windows Server 2022. Weitere Informationen zum Konfigurieren von WSUS-Updates für Microsoft Edge finden Sie unter [Update Microsoft Edge.](https://docs.microsoft.com/mem/configmgr/apps/deploy-use/deploy-edge?bc=https%3A%2F%2Fdocs.microsoft.com%2FDeployEdge%2Fbreadcrumb%2Ftoc.json&toc=https%3A%2F%2Fdocs.microsoft.com%2FDeployEdge%2Ftoc.json#update-microsoft-edge)

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

<!-- archive from version 95.0.1020.9: September 28 to version 94.0.992.14: September 7 ---->
<!-- archive from Version 94.0.992.9: September 2 to Version 92.0.902.40: July 6 -->
<!--Archive on Oct 27 From Version 92.0.902.22: June 21 to Version 89.0.774.23: February 8  -->
<!--- Archived from Version 87.0.664.18: October 26 to to version 89.0.774.18: February 3 ---->
<!--- Archived from Version 87.0.664.12: October 20 to to version 86.0.622.15: September 14 ---->
<!--- Archived to version 86.0.622.11: September 9 ---->
<!--- Archived to version 85.0.564.18: July 28 ---->

## <a name="see-also"></a>Weitere Informationen

- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)
