---
title: Lokale Websiteliste für den Internet Explorer-Modus (IE)
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 03/24/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Erfahren Sie, wie Sie lokale Websitelisten und einfachen Zugriff auf den IE-Modus aktivieren.
ms.openlocfilehash: 85aa6baa1abaa1a59f4e9cf9f2414f54ccf70cbb
ms.sourcegitcommit: dd8cdbd35726c795ddce917e549ddf17ee7f5290
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/11/2022
ms.locfileid: "12473637"
---
# <a name="configure-local-site-list-for-internet-explorer-ie-mode"></a>Konfigurieren der lokalen Websiteliste für den Internet Explorer-Modus (IE)

>[!Note]
> Die Internet Explorer 11-Desktopanwendung wird eingestellt und wird am 15. Juni 2022 nicht mehr unterstützt (eine Liste der Bereiche finden Sie in den häufig gestellten [Fragen zur Einstellung der Internet Explorer 11-Desktop-App](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549)). Dieselben IE11-Apps und -Websites, die Sie heute verwenden, können in Microsoft Edge im Internet Explorer-Modus geöffnet werden. Weitere Informationen finden Sie unter [Die Zukunft von Internet Explorer auf Windows 10 befindet sich in Microsoft Edge](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/).

In diesem Artikel wird erläutert, wie Sie den einfachen Zugriff auf den Internet Explorer-Modus (IE-Modus) konfigurieren und die Verwendung lokaler Websitelisten in Ihrer Organisation zulassen.

> [!NOTE]
> Dieser Artikel bezieht sich auf Microsoft Edge Version 92 oder höher.

## <a name="prerequisites"></a>Voraussetzungen

1. Windows-Updates

   - Windows 11

   - Windows 10, Version 1909 [– KB5003974](https://support.microsoft.com/topic/kb5003974-servicing-stack-update-for-windows-10-version-1909-june-15-2021-0e65680e-2d21-4a31-b97a-e24c022aeccf) und [KB5003698](https://support.microsoft.com/topic/june-15-2021-kb5003698-os-build-18363-1645-preview-1ecf117e-1f89-40f9-a0a5-ed5766737620) oder höher

   - Windows 10, Version 2004; Windows 10, Version 20H2 und Windows 10, Version 21H [– KB5005260](https://support.microsoft.com/topic/kb5005260-servicing-stack-update-for-windows-10-version-2004-20h2-and-21h1-august-10-2021-ec4c5daa-2cec-4b06-be93-037f150fe3ba) und [KB5005101](https://support.microsoft.com/topic/september-1-2021-kb5005101-os-builds-19041-1202-19042-1202-and-19043-1202-preview-82a50f27-a56f-4212-96ce-1554e8058dc1) oder höher

2. Microsoft Edge Version 92 (92.0.902.55 oder höher)

> [!IMPORTANT]
> Dieses Feature für lokale Websitelisten wird derzeit unter Windows Server 2016 nicht unterstützt.

## <a name="overview"></a>Übersicht

Der IE-Modus wird von der Konfiguration der Websiteliste für den Unternehmensmodus unterstützt. Während Sie Websites in der Websiteliste identifizieren und konfigurieren, um den IE-Modus zu verwenden, müssen Ihre Benutzer nicht mehr warten oder auf die eigenständige IE11-Anwendung zurückgreifen.

Ab Microsoft Edge Version 92 ist der wiederholte Zugriff auf *nicht konfigurierte* Websites im IE-Modus einfacher. Benutzer können Websites im IE-Modus neu laden. Sie können diese Websites ihrer lokalen Websiteliste hinzufügen, um sie 30 Tage lang automatisch im IE-Modus zu rendern, während die Websiteliste der Organisation aktualisiert wird. Wenn [IE11](/deployedge/edge-ie-disable-ie11) in Ihrer Umgebung deaktiviert ist, sind Ihre Benutzer nicht mehr ausschließlich von der Websiteliste der Organisation abhängig.

Sie können diese Benutzeroberfläche über Gruppenrichtlinien für Ihre Organisation konfigurieren.

> [!NOTE]
> Eine *nicht konfigurierte* Website ist eine Website, die den IE-Modus erfordert, aber nicht für das Öffnen im IE-Modus in der Websiteliste für den Unternehmensmodus konfiguriert ist.

## <a name="enable-the-local-site-list-experience"></a>Aktivieren der lokalen Websitelistenoberfläche

Um die lokale Websitelistenumgebung zu aktivieren, können Benutzer zur URL *edge://settings/defaultBrowser* wechseln und zulassen, **dass Websites im Internet Explorer-Modus auf "Zulassen" neu geladen werden**.****

:::image type="content" source="media/Edge-hybrid-IE-mode/internet-explorer-compatibilitiy.png" alt-text="Internet Explorer-Kompatibilität":::

>[!Note]  
>
>1. Wenn Sie das Testen des IE-Modus über die *Richtlinie "InternetExplorerIntegrationTestingAllowed* " aktiviert haben, wird diese Einstellung angezeigt, sie wird jedoch abgeblendet, es sei denn, Sie aktivieren explizit die *Richtlinie "InternetExplorerIntegrationReloadInIEModeAllowed* ".
>
>2. Wenn **"Zulassen, dass Websites im Internet Explorer-Modus neu geladen werden** " auf **"Standard**" festgelegt ist, können Benutzer Websites möglicherweise im IE-Modus neu laden, wenn sie über eine vorhandene Internet Explorer 11-Verwendung verfügen.  

Wenn diese Einstellung aktiviert ist, können Benutzer eine Website im IE-Modus neu laden, indem sie **"Einstellungen" und mehr (das Ellipsensymbol ...) > "Im Internet Explorer-Modus erneut laden**" auswählen. Benutzer können auch **im Internet Explorer-Modus die Registerkarte "Neu laden"** auswählen, wenn sie mit der rechten Maustaste auf eine Registerkarte klicken oder **im neuen Internet Explorer-Modus die Option "Link öffnen"** auswählen, wenn sie mit der rechten Maustaste auf einen Link klicken.

:::image type="content" source="media/Edge-hybrid-IE-mode/reload-in-internet-exploror-mode-screenshot.png" alt-text="Erneutes Laden im Internet Explorer-Modus":::

Das Symbol " **Im Internet Explorer-Modus neu laden** " kann an die Symbolleiste angeheftet werden. Die Symbolleistenschaltfläche ermöglicht es Benutzern, einfach in den IE-Modus zu wechseln und zu beenden, und kann über die *edge://settings/appearance-URL* verwaltet werden.

:::image type="content" source="media/Edge-hybrid-IE-mode/reload-in-internet-exploror-mode-icon-screenshot.png" alt-text="Symbol &quot;Im Internet Explorer-Modus neu laden&quot;":::

>[!Note]
>Wenn sich der Benutzer auf einer Website befindet, die sich bereits in der Enterprise Mode Site List der Organisation befindet, sind Optionen zum Erneuten Laden im Internet Explorer-Modus (oder Beenden) sichtbar, aber abgeblendet.

Wenn die Option ausgewählt ist, wird die Website im IE-Modus neu geladen. Das Symbol für den IE-Modus ist links neben der Adressleiste sichtbar, und im Flyout wird eine Option angezeigt, mit der Benutzer beim nächsten Mal auf "Seite im Internet Explorer-Modus öffnen" umschalten können. Dadurch wird die bestimmte Seite hinzugefügt, auf der sich der Benutzer befindet, der lokalen Websiteliste und wird automatisch für die nächsten 30 Tage im IE-Modus geöffnet.

:::image type="content" source="media/Edge-hybrid-IE-mode/site-has-been-reloaded-in-ie-mode-screenshot.png" alt-text="Diese Seite ist im Internet Explorer-Modus geöffnet.":::

Nachdem eine Website im IE-Modus neu geladen wurde, verbleibt die Seitennavigation im IE-Modus (z. B. ein Link, ein Skript, ein Formular auf der Seite oder eine serverseitige Umleitung von einer anderen "seitenseitigen" Navigation).  

Im IE-Modus wird benutzern ein Banner angezeigt, das angibt, dass sie sich im IE-Modus befinden, die Option zum Verlassen des IE-Modus und zum Anheften des IE-Modussymbols an die Symbolleiste (sofern es noch nicht angeheftet ist).

:::image type="content" source="media/Edge-hybrid-IE-mode/ie-mode-banner-screenshot.png" alt-text="Banner für den IE-Modus":::

Benutzer können den IE-Modus über die Schaltfläche "Verlassen" im Banner, das angeheftete Symbol für den IE-Modus oder **Einstellungen und mehr (das Ellipsensymbol ...) > Internet Explorer-Modus beenden, andernfalls** wird Microsoft Edge automatisch aus dem IE-Modus beendet, wenn eine Nicht-Seitennavigation auftritt (z. B. mithilfe der Adressleiste, der Schaltfläche "Zurück",  oder einen Bevorzugten Link).

Einträge verbleiben für einen Standardzeitraum von 30 Tagen in der lokalen Websiteliste. Es wird empfohlen, Legacywebsites für Ihre Organisation in der Websiteliste für den Unternehmensmodus zu konfigurieren. Die lokale Websiteliste stellt sicher, dass Benutzer ihren Workflow fortsetzen können, ohne unterbrochen zu werden, während die Websiteliste der Organisation aktualisiert wird. Wenn Benutzer am 31. Tag zur Website navigieren, wird ein Banner angezeigt, das erklärt, dass die Website nicht mehr im IE-Modus geladen wird. Benutzer können sie wieder zur lokalen Websiteliste hinzufügen, wenn sie dies auswählen.

:::image type="content" source="media/Edge-hybrid-IE-mode/page-will-no-longer-load-in-ie-mode-screenshot.png" alt-text="Seite wird im IE-Modus nicht mehr geladen":::

## <a name="policies-to-configure-the-use-of-local-site-lists-for-ie-mode"></a>Richtlinien zum Konfigurieren der Verwendung lokaler Websitelisten für den IE-Modus

Zum Konfigurieren der lokalen Websitelistenumgebung in Microsoft Edge stehen zwei Gruppenrichtlinien zur Verfügung. Diese Richtlinien lauten:

### <a name="policy-internetexplorerintegrationreloadiniemodeallowed"></a>Richtlinie: InternetExplorerIntegrationReloadInIEModeAllowed

Diese Richtlinie entspricht der Microsoft Edge-Einstellung "Zulassen, dass Websites im Internet Explorer-Modus neu geladen werden". Sie können auf diese Einstellung zugreifen, indem Sie zur URL *edge://settings/defaultbrowser* wechseln.

- Wenn Sie diese Richtlinie aktivieren, können Benutzer eine Website im IE-Modus neu laden, indem sie **"Einstellungen" und mehr auswählen (das Symbol "Auslassungszeichen... > Im Internet Explorer-Modus neu laden**". Benutzer können auch **im Internet Explorer-Modus die Registerkarte "Neu laden"** auswählen, wenn sie mit der rechten Maustaste auf eine Registerkarte klicken, oder auf der **neuen Registerkarte "Internet Explorer-Modus" auf "Link öffnen"** klicken, wenn sie mit der rechten Maustaste auf einen Link klicken.
Benutzer können Microsoft Edge optional anweisen, zukünftig den IE-Modus für die Website zu verwenden. Diese Auswahl wird standardmäßig 30 Tage lang gespeichert und kann mithilfe der Richtlinie *"InternetExplorerIntegrationLocalSiteListExpirationDays*" verwaltet werden.

- Wenn Sie diese Richtlinie deaktivieren, können Benutzer eine nicht konfigurierte Website im IE-Modus nicht neu laden.

- Wenn Sie diese Richtlinie nicht konfigurieren, zeigen wir Benutzern abhängig von der aktuellen Nutzung von Internet Explorer 11 Optionen zum Erneutladen nicht konfigurierter Websites im IE-Modus an.

Beachten Sie, dass diese Richtlinie Vorrang vor der Konfiguration der [Richtlinie "InternetExplorerIntegrationTestingAllowed](/deployedge/microsoft-edge-policies#internetexplorerintegrationtestingallowed) " hat und diese Richtlinie deaktiviert wird.

### <a name="policy-internetexplorerintegrationlocalsitelistexpirationdays"></a>Richtlinie: InternetExplorerIntegrationLocalSiteListExpirationDays

Diese Richtlinie kann verwendet werden, um die Anzahl der Tage anzupassen, die eine Website in der lokalen Websiteliste für Benutzer verbleibt.  

- Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, wird ein Standardwert von 30 Tagen verwendet.

- Wenn Sie die Richtlinie aktivieren, müssen Sie einen Wert zwischen 0 und 90 Tagen eingeben, um die Website in der lokalen Websiteliste eines Benutzers zu speichern.

Diese Richtlinie hat keine Auswirkung, wenn Sie die *InternetExplorerIntegrationReloadInIEModeAllowed-Richtlinie* deaktiviert haben.

> [!NOTE]
> Die lokale Websiteliste wird derzeit nicht geräteübergreifend synchronisiert. Diese Verbesserung befindet sich derzeit in unserem Rückstand, und wir werden dieses Feature aktualisieren, sobald es verfügbar ist.

## <a name="see-also"></a>Siehe auch

- Internet Explorer 11 deaktivieren – [Internet Explorer 11 deaktivieren](/deployedge/edge-ie-disable-ie11)
- Konfigurieren von Richtlinien für den IE-Modus – [Konfigurieren von Richtlinien für den IE-Modus](/deployedge/edge-ie-mode-policies)
