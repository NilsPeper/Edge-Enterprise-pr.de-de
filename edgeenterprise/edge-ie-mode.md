---
title: Was ist der Internet Explorer-Modus?
ms.author: kvice
author: dan-wesley
manager: laurawi
ms.date: 02/26/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Erfahren Sie, wie der Internet Explorer-Modus in Microsoft Edge Zugriff auf Websites bietet, die Internet Explorer 11 benötigen, sowie Zugriff auf moderne Websites.
ms.openlocfilehash: 5ca14c4d448b573dc7de6781ce86ee62281a48a4
ms.sourcegitcommit: 93851b83dc11422924646a04a9e0f60ff2554af7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "11470223"
---
# <a name="what-is-internet-explorer-ie-mode"></a>Was ist der Internet Explorer (IE)-Modus?

Wir haben den Internet Explorer (IE)-Modus in Microsoft Edge für Organisationen erstellt, die Internet Explorer 11 zur Abwärtskompatibilität mit vorhandenen Websites benötigen, aber auch einen modernen Browser benötigen. Dieses Feature erleichtert Organisationen die Verwendung eines Browsers, für Vorgänger-Web/-Apps oder für ein modernes Web/eine moderne App. Dieser Artikel enthält eine Einführung in die Verwendung von Microsoft Edge mit dem IE-Modus.

> [!NOTE]
> Dieser Artikel bezieht sich auf Microsoft Edge Version 77 oder höher.

## <a name="what-is-ie-mode"></a>Was ist der IE-Modus?

Der IE-Modus auf Microsoft Edge erleichtert es Ihnen, alle Websites Ihrer Organisation in einem einzigen Browser zu verwenden. Dabei wird das integrierte Chrom-Modul für moderne Websites und das Trident MSHTML-Modul aus Internet Explorer 11 (IE11) für ältere Websites verwendet.

Wenn eine Website im IE-Modus geladen wird, wird die IE-Logo-Anzeige auf der linken Seite der Navigationsleiste angezeigt. Sie können auf die IE-Logo-Anzeige klicken, um weitere Informationen anzuzeigen, wie hier dargestellt:

  ![IE-Logo-Anzeige](./media/ie-mode/ie-logo-indicator1.png)

Nur die Websites, die Sie speziell (über eine Richtlinie) konfigurieren, verwenden den IE-Modus. Alle anderen Websites werden als moderne Websites dargestellt. Damit eine Website den IE-Modus verwenden kann, müssen Sie folgende Aktionen ausführen:

- Listen Sie die Website in der in einer der folgenden Richtlinien definierten Enterprise Mode Site List-XML auf:
  - Microsoft Edge 78 oder höher, „Enterprise Mode-Siteliste konfigurieren”
  - Internet Explorer. „Die Websiteliste für den Unternehmensmodus-IE verwenden”
  > [!NOTE]
  > Es wird nur eine Enterprise Mode Site List verarbeitet. Die Microsoft Edge-Websitelistenrichtlinie hat Vorrang vor der Internet Explorer-Websitelistenrichtlinie.
- Alle Intranetwebsites, wenn die Gruppenrichtlinie **Alle Intranetwebsites an Internet Explorer senden** aktiviert ist (Microsoft Edge 77 oder höher)

### <a name="ie-mode-supports-the-following-internet-explorer-functionality"></a>Der IE-Modus unterstützt die folgenden Funktionen von Internet Explorer

- Alle Dokumentmodi und Unternehmensmodi
- ActiveX-Steuerelemente (wie Java oder Silverlight)
- Browserhilfsobjekte 
- Internet Explorer-Einstellungen und Gruppenrichtlinien, die sich auf die Sicherheitszoneneinstellungen und den geschützten Modus auswirken
- Die F12-Entwicklertools für IE, wenn der Start mit [IEChooser](/office/dev/add-ins/testing/debug-add-ins-using-f12-developer-tools-on-windows-10) erfolgt
- Microsoft Edge-Erweiterungen (Erweiterungen, die direkt mit dem IE-Seiteninhalt interagieren, werden nicht unterstützt.)

### <a name="ie-mode-doesnt-support-the-following-internet-explorer-functionality"></a>Der IE-Modus unterstützt die folgenden Funktionen von Internet Explorer nicht

- Internet Explorer-Symbolleisten
- Internet Explorer-Einstellungen und Gruppenrichtlinien, die sich auf das Navigationsmenü auswirken (z. B. Suchmaschinen und Startseiten)
- IE11 oder Entwicklungstools von Microsoft Edge F12

## <a name="prerequisites"></a>Voraussetzungen

Die folgenden Voraussetzungen gelten für die Verwendung von Microsoft Edge im IE-Modus.

> [!IMPORTANT]
> Installieren Sie die neuesten Updates für Windows und Microsoft Edge, um die bestmögliche Leistung zu erzielen. Wenn Sie dies nicht tun, wird der IE-Modus wahrscheinlich fehlschlagen.

1. Die Mindestsystemaktualisierungen für die Betriebssysteme, die in der nächsten Tabelle aufgelistet sind.

 | Betriebssystem | Version       | Updates |
 |------------------|---------------|---------|
 | Windows 10       | 1909 oder höher |         |
 | Windows 10       | 1903          | [KB4501375](https://support.microsoft.com/help/4501375/windows-10-update-kb4501375) oder höher |
 | Windows Server   | 1903          | [KB4501375](https://support.microsoft.com/help/4501375/windows-10-update-kb4501375) oder höher |
 | Windows 10       | 1809          | [KB4501371](https://support.microsoft.com/help/4501371/windows-10-update-kb4501371) oder höher |
 | Windows Server   | 1809          | [KB4501371](https://support.microsoft.com/help/4501371/windows-10-update-kb4501371) oder höher |
 | Windows Server   | 2019          | [KB4501371](https://support.microsoft.com/help/4501371/windows-10-update-kb4501371) oder höher |
 | Windows 10       | 1803          | [KB4512509](https://support.microsoft.com/help/4512509/windows-10-update-kb4512509) oder höher |
 | Windows 10       | 1709          | [KB4512494](https://support.microsoft.com/help/4512494/windows-10-update-kb4512494) oder höher |
 | Windows 10       | 1607          | [KB4516061](https://support.microsoft.com/help/4516061/windows-10-update-kb4516061) oder höher |
 | Windows Server   | 2016          | [KB4516061](https://support.microsoft.com/help/4516061/windows-10-update-kb4516061) oder höher |
 | Windows 10       | Erste Version, Juli 2015 | [KB4520011](https://support.microsoft.com/help/4520011/windows-10-update-kb4520011) oder höher |
 | Windows 8       | 8.1              | [KB4507463](https://support.microsoft.com/help/4507463/july-16-2019-kb4507463-os-build-preview-of-monthly-rollup) oder höher bzw. [KB4511872](https://support.microsoft.com/help/4511872/cumulative-security-update-for-internet-explorer) oder höher |
 | Windows Server   | 2012 R2       | [KB4507463](https://support.microsoft.com/help/4507463/july-16-2019-kb4507463-os-build-preview-of-monthly-rollup) oder höher bzw. [KB4511872](https://support.microsoft.com/help/4511872/cumulative-security-update-for-internet-explorer) oder höher |
 | Windows 8  | Eingebettet            | Installieren Sie [KB4492872](https://support.microsoft.com/help/4492872/update-for-internet-explorer-april-16-2019)zum Aktualisieren auf den Internet Explorer 11; installieren Sie danach [KB4507447](https://support.microsoft.com/help/4507447/windows-server-2012-update-kb4507447) oder höher bzw. [KB4511872](https://support.microsoft.com/help/4511872/cumulative-security-update-for-internet-explorer) oder höher |
 | Windows Server   | 2012           | Installieren Sie [KB4492872](https://support.microsoft.com/help/4492872/update-for-internet-explorer-april-16-2019)zum Aktualisieren auf den Internet Explorer 11; installieren Sie danach [KB4507447](https://support.microsoft.com/help/4507447/windows-server-2012-update-kb4507447) oder höher bzw. [KB4511872](https://support.microsoft.com/help/4511872/cumulative-security-update-for-internet-explorer) oder höher |
 | Windows 7        |  SP1**        | [KB4507437](https://support.microsoft.com/help/4507437/windows-7-update-kb4507437) oder höher bzw. [KB4511872](https://support.microsoft.com/help/4511872/cumulative-security-update-for-internet-explorer) oder höher |
 | Windows Server   |  2008 R2**    | [KB4507437](https://support.microsoft.com/help/4507437/windows-7-update-kb4507437) oder höher bzw. [KB4511872](https://support.microsoft.com/help/4511872/cumulative-security-update-for-internet-explorer) oder höher |
  > [!IMPORTANT]
  > ** Windows 7 und Windows Server 2008 R2 unterstützen Microsoft Edge weiterhin, nachdem der Support für diese Betriebssysteme abgelaufen ist. Damit der IE-Modus unter diesen Betriebssystemen unterstützt wird, müssen die Geräte über die [Erweiterten Sicherheitsupdates für Windows 7](https://support.microsoft.com/help/4527878/faq-about-extended-security-updates-for-windows-7)verfügen. Es wird empfohlen, so bald wie möglich ein Upgrade auf ein unterstütztes Betriebssystem durchzuführen, um geschützt zu bleiben. Der Support für Microsoft Edge mit den erweiterten Sicherheitsupdates sollte als eine vorübergehende Überbrückung bis zum Erreichen eines unterstützten Betriebssystemstatus betrachtet werden.

2. Die administrative Vorlage von Microsoft Edge. Weitere Informationen finden Sie unter [Konfigurieren von Microsoft Edge](./configure-microsoft-edge.md).
3. Aktivieren von Internet Explorer 11 in Windows-Features.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)
- [Weitere Informationen zum Unternehmensmodus](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)