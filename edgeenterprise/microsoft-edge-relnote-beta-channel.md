---
title: Anmerkungen zu dieser Version von Microsoft Edge für Beta-Kanal
ms.author: aguta
author: dan-wesley
manager: srugh
ms.date: 11/03/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Anmerkungen zu dieser Version von Microsoft Edge für Beta-Kanal
ms.openlocfilehash: bcc2ecf91c6d90443de26b5bff1c744d7582aa18
ms.sourcegitcommit: 4ec03873a85f065d9bfa6203cfe6c3e938f79bc5
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2021
ms.locfileid: "12155102"
---
# <a name="release-notes-for-microsoft-edge-beta-channel"></a>Versionshinweise für Microsoft Edge Beta-Kanal

Diese Versionshinweise enthalten Informationen zu neuen Funktionen und nicht sicherheitsrelevanten Updates, die im Microsoft Edge Beta-Kanal enthalten sind. Archivierte Versionen dieser Versionshinweise sind [hier](microsoft-edge-relnote-archive-beta-channel.md) verfügbar.

> [!NOTE]
> Die Microsoft Edge-Webplattform entwickelt sich ständig weiter, um Benutzerfreundlichkeit, Sicherheit und Datenschutz zu verbessern. Weitere Informationen finden Sie unter [Kommende Änderungen in Microsoft Edge mit Auswirkungen auf die Websitekompatibilität](/microsoft-edge/web-platform/site-impacting-changes).

## <a name="version-96010548-november-1"></a>Version 96.0.1054.8: 1. November

### <a name="feature-updates"></a>Funktionsupdates

- **Starten Sie progressive Web App (PWA) direkt über Protokolllinks.** Installed PWAs handle links that use a specific protocol for a more integrated experience.

- **Erfahren Sie, wie Sie mathematische Probleme mit Math Solver lösen.** Wir freuen uns, Ihnen mitteilen zu können, dass Sie Math Solver in Microsoft Edge verwenden können, um Hilfe bei einer Vielzahl mathematischer Konzepte zu erhalten. Diese Konzepte reichen von elementaren arithmetischen und quadratischen Formeln bis hin zu Trigonometrie und Berechnung. Mit Math Solver können Sie ein Bild eines handschriftlichen oder gedruckten mathematischen Problems erstellen und dann eine sofortige Lösung mit schrittweisen Anweisungen bereitstellen, mit denen Sie lernen können, wie Sie die Lösung ohne Hilfe erreichen. Math Solver verfügt auch über eine mathematische Tastatur, mit der Sie mathematische Probleme einfach eingeben können. Mit dieser Tastatur müssen Sie keine herkömmliche Tastatur durchsuchen, um die benötigten mathematischen Zeichen zu finden. Nach der Lösung Ihres Problems bietet Math Solver Optionen zum weiteren Lernen mit Quizfragen, Arbeitsblättern und Videolernprogrammen.

- **Verbesserungen beim Scrollen für PDF-Dokumente.** Wir verbessern die Bildlaufleistung, um eine reibungslosere Bildlauferfahrung in PDF-Dokumenten zu ermöglichen. Während des Bildlaufs werden keine weißen Balken angezeigt.

- **Freihandformhervorhebung auf PDFs.** Die PDF-Anzeige- und Markupoberfläche wird durch die Hinzufügung von Freihandformmarkern verbessert. Sie können Abschnitte in PDFs, auf die Sie keinen Zugriff haben, und gescannte Dokumente hervorheben.

- **Control-Flow Enforcement Technology (CET).**  Microsoft Edge unterstützt einen noch sichereren Browsermodus, der hardwareabhängigen Steuerungsfluss für Browserprozesse verwendet. Der Steuerungsfluss wird auf dieser unterstützten Hardware bereitgestellt: Intel 11. Generation. oder AMD Cer 3. You can disable CET by configuring Image File Execution Options (IFEO) using group policy.

- **Neues Warndialogfeld für Tippfehler bei Websites.** Der Browser zeigt nun eine Warnung auf einigen Websites mit URLs an, die anderen Websites sehr ähnlich aussehen. Diese Benutzeroberfläche verwendet clientseitige Heuristiken, um Benutzer vor Websites zu warnen, die möglicherweise häufig verwendete Websites spoofen. Weitere Informationen finden Sie unter [Was ist Tippfehler?](https://support.microsoft.com/topic/what-is-typosquatting-54a18872-8459-4d47-b3e3-d84d9a362eb0).

- **Verbesserte Übergabe zwischen dem IE-Modus und dem modernen Browser.**  Ab dieser Version von Microsoft Edge enthalten navigations zwischen Microsoft Edge und Internet Explorer-Modus Formulardaten und zusätzliche HTTP-Header. Referrer-Header, Post-Daten, Formulardaten und Anforderungsmethoden werden auf den beiden Oberflächen korrekt weitergeleitet. Mithilfe der [InternetExplorerIntegrationComplexNavDataTypes-Richtlinie](/deployedge/microsoft-edge-policies#internetexplorerintegrationcomplexnavdatatypes) können Sie angeben, welche Datentypen einbezogen werden sollen. Weitere Informationen finden Sie in den folgenden häufig gestellten Fragen: [Meine Anwendung erfordert die Übertragung von POST-Daten zwischen dem IE-Modus und Microsoft Edge.](./edge-ie-mode-faq.md#my-application-requires-transferring-post-data-between-ie-mode-and-microsoft-edge-is-this-supported)

- **Cloud Site List Management für den IE-Modus in der öffentlichen Vorschau.**  Mit cloudbasierter Websitelistenverwaltung können Sie Ihre Websitelisten für den IE-Modus in der Cloud verwalten, ohne dass eine lokale Infrastruktur zum Hosten der Websiteliste Ihrer Organisation erforderlich ist. Sie können im Microsoft 365 Admin Center auf das Feature "CloudWebsitelistenverwaltung" zugreifen, indem Sie Microsoft Edge Websitelisten verwenden. Weitere Informationen finden Sie im Artikel zur [Cloud-Websitelistenverwaltung für den IE-Modus (Public Preview).](./edge-ie-mode-cloud-site-list-mgmt.md)

- **Aktualisieren sie Microsoft Edge WebWiew2 mit WSUS.** IT-Administratoren, die WSUS zum Aktualisieren von Microsoft Edge verwenden, können auch Microsoft Edge WebView2 mit WSUS aktualisieren. Diese Funktion ermöglicht Administratoren einen einfacheren Wartungsprozess für Offlinegeräte.

- **WSUS-Updates für Server.** WSUS- und Katalogupdates für Microsoft Edge Kanäle (Stable, Beta, Dev) gelten jetzt für Windows Server-SKUs, die Microsoft Edge installiert haben, einschließlich Windows Server 2022. Weitere Informationen zum Konfigurieren von WSUS-Updates für Microsoft Edge finden Sie unter [Update Microsoft Edge](https://docs.microsoft.com/mem/configmgr/apps/deploy-use/deploy-edge?bc=https%3A%2F%2Fdocs.microsoft.com%2FDeployEdge%2Fbreadcrumb%2Ftoc.json&toc=https%3A%2F%2Fdocs.microsoft.com%2FDeployEdge%2Ftoc.json#update-microsoft-edge).

### <a name="policy-updates"></a>Richtlinienupdates

#### <a name="new-policies"></a>Neue Richtlinien

- [ApplicationGuardUploadBlockingEnabled](/DeployEdge/microsoft-edge-policies#applicationguarduploadblockingenabled) : Verhindert, dass Dateien in Application Guard hochgeladen werden.
- [AudioProcessHighPriorityEnabled](/DeployEdge/microsoft-edge-policies#audioprocesshighpriorityenabled) : Zulassen, dass der Audioprozess mit einer Priorität ausgeführt wird, die bei Windows über dem Normalen liegt.
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

- **Support für „Im Datei-Explorer anzeigen“ für Microsoft Office SharePoint Online-Bibliotheken in Microsoft Edge.**  Jetzt können Sie die Ansicht im Datei-Explorer-Funktion für SharePoint Online-Bibliothek für moderne Dokumente aktivieren. Damit diese Erfahrung für Ihre Benutzer sichtbar und funktionsfähig ist, müssen Sie die Richtlinie Microsoft Edge [Richtlinie "Konfigurieren der Ansicht im Datei-Explorer-Feature für SharePoint Seiten in Microsoft Edge"](/deployedge/microsoft-edge-policies#configureviewinfileexplorer) aktivieren und Ihre SharePoint Onlinemandantenkonfiguration aktualisieren. Weitere Informationen: [Anzeigen SharePoint Dateien mit dem Datei-Explorer in Microsoft Edge – SharePoint in Microsoft 365 | Microsoft Docs](/SharePoint/sharepoint-view-in-edge).

- **Datei-URL-Links für Intranetzonen werden im Windows-Datei-Explorer geöffnet.**  Sie können zulassen, dass Datei-URL-Links zu Intranetzonen-Dateien, die von Intranetzonen-HTTPS-Websites stammen, den Windows-Datei-Explorer für diese Datei oder dieses Verzeichnis öffnen. Sie können diese Erfahrung mithilfe der Richtlinie [IntranetFileLinksEnabled](/deployedge/microsoft-edge-policies#intranetfilelinksenabled) aktivieren.

- **Verbesserungen an der Downloaderfahrung.**  Die Unterstützung für die Downloadbenutzeroberfläche wird auf progressive Webanwendungen PWAs und WebView erweitert. Wir beginnen auch mit der Unterstützung von Drag & Drop zum Datei-Explorer und zum Desktop.

- **Machen Sie dort weiter, wo Sie in PDF-Dokumenten aufgehört haben.**  Sie können den Lesezugriff von dem Speicherort fortsetzen, an dem Sie das PDF-Dokument zuletzt geschlossen haben.

- **Der Effizienzmodus verlängert die Akkulaufzeit, wenn Ihr Laptop in den Stromsparmodus wechselt.**  Der Effizienzmodus wird aktiv, wenn Ihr Laptop in Stromsparmodus wechselt, um dem Browser die Verwaltung der Ressourcennutzung zur Verlängerung der Akkulaufzeit Ihres Computers zu ermöglichen. Sie haben vier Optionen für den Zeitpunkt, an dem der Effizienzmodus aktiv wird: Unplugged und low battery, Unplugged, Always und Never. Hinweis: Dies ist ein kontrolliertes Featurerollout. Auf Geräten mit Akku sollte das Feature aktiviert sein.

***Neue Richtlinien***

- [BrowserLegacyExtensionPointsBlockingEnabled](/DeployEdge/microsoft-edge-policies#browserlegacyextensionpointsblockingenabled) – Aktivieren des Blockierens von Browserversionserweiterungspunkten.
- [CrossOriginWebAssemblyModuleSharingEnabled](/DeployEdge/microsoft-edge-policies#crossoriginwebassemblymodulesharingenabled) – Gibt an, ob WebAssembly-Module ursprungsübergreifend gesendet werden können.
- [DisplayCapturePermissionsPolicyEnabled](/DeployEdge/microsoft-edge-policies#displaycapturepermissionspolicyenabled) – Gibt an, ob die Berechtigungsrichtlinie für die Anzeigeerfassung überprüft oder übersprungen wird.
- [InternetExplorerIntegrationWindowOpenHeightAdjustment](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationwindowopenheightadjustment) – Konfigurieren sie die Pixelanpassung zwischen window.open-Höhen, die von IE-Modusseiten bezogen werden, im Vergleich zu Microsoft Edge Modusseiten.
- [InternetExplorerIntegrationWindowOpenWidthAdjustment](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationwindowopenheightadjustment) – Konfigurieren Sie die Pixelanpassung zwischen window.open-Breiten, die von IE-Modusseiten bezogen werden, im Vergleich zu Microsoft Edge Modusseiten.
- [IntranetFileLinksEnabled](/DeployEdge/microsoft-edge-policies#intranetfilelinksenabled) : Zulassen, dass Intranetzone-Datei-URL-Links von Microsoft Edge in Windows Datei-Explorer geöffnet werden.
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

<!-- archive from Version 94.0.992.9: September 2 to Version 92.0.902.40: July 6 -->
<!--Archive on Oct 27 From Version 92.0.902.22: June 21 to Version 89.0.774.23: February 8  -->
<!--- Archived from Version 87.0.664.18: October 26 to to version 89.0.774.18: February 3 ---->
<!--- Archived from Version 87.0.664.12: October 20 to to version 86.0.622.15: September 14 ---->
<!--- Archived to version 86.0.622.11: September 9 ---->
<!--- Archived to version 85.0.564.18: July 28 ---->

## <a name="see-also"></a>Weitere Informationen

- [Microsoft Edge Enterprise-Startseite](https://aka.ms/EdgeEnterprise)
