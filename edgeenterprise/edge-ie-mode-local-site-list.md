---
title: Lokale Websiteliste für den IE-Modus
ms.author: shisub
author: AndreaLBarr
manager: srugh
ms.date: 09/13/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Erfahren Sie, wie Sie lokale Websitelisten und einfachen Zugriff auf den IE-Modus aktivieren
ms.openlocfilehash: 8130a835cd803f5cdeb50f825ccee895f35f62e3
ms.sourcegitcommit: c3d63d913eb15e7dbeb9f45b5f28fc841b46bce1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/15/2021
ms.locfileid: "12016564"
---
## <a name="local-site-list-for-ie-mode"></a>Lokale Websiteliste für den IE-Modus

>[!Note]
> Die Internet Explorer 11-Desktopanwendung wird eingestellt und wird ab dem 15. Juni 2022 nicht mehr unterstützt (eine Liste der in diesem Bereich enthaltenen Elemente [finden Sie in den FAQ](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549)). Dieselben IE11-Apps und -Websites, die Sie heute verwenden, können in Microsoft Edge im Internet Explorer-Modus geöffnet werden. [Weitere Informationen finden Sie hier](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/).

In diesem Artikel wird erläutert, wie Sie den einfachen Zugriff auf den Internet Explorer-Modus (IE-Modus) konfigurieren und die Verwendung lokaler Websitelisten in Ihrer Organisation zulassen.

> [!NOTE]
> Dieser Artikel bezieht sich auf Microsoft Edge Version 92 oder höher.

### <a name="prerequisites"></a>Voraussetzungen

1. Windows-Updates

- Windows 10, Version 1909 [– KB5003698](https://support.microsoft.com/topic/june-15-2021-kb5003698-os-build-18363-1645-preview-1ecf117e-1f89-40f9-a0a5-ed5766737620) oder höher  

- Windows 10, Version 2004; Windows 10, Version 20H2 und Windows 10, Version 21H1 – [KB5003690](https://support.microsoft.com/topic/june-21-2021-kb5003690-os-builds-19041-1081-19042-1081-and-19043-1081-preview-11a7581f-2a01-47d5-ba12-431709ee2248) oder höher

2. Microsoft Edge Version 92 (92.0.925.0 oder höher)

## <a name="overview"></a>Übersicht

Der IE-Modus wird von der Konfiguration der Enterprise Mode Site List unterstützt. Während Sie Websites in der Websiteliste für die Verwendung des IE-Modus identifizieren und konfigurieren, müssen Ihre Benutzer nicht mehr auf die eigenständige IE11-Anwendung warten oder darauf zurückgreifen.

Ab Microsoft Edge Version 92 ist der *wiederholte* Zugriff auf nicht konfigurierte IE-Moduswebsites einfacher. Benutzer können Websites im IE-Modus erneut laden. Sie können diese Websites ihrer lokalen Websiteliste hinzufügen, um sie für einen Zeitraum von 30 Tagen automatisch im IE-Modus zu rendern, während die Websiteliste der Organisation aktualisiert wird. Wenn [IE11](/deployedge/edge-ie-disable-ie11) in Ihrer Umgebung deaktiviert ist, sind Ihre Benutzer nicht mehr ausschließlich von der Websiteliste der Organisation abhängig.

Sie können diese Erfahrung über Gruppenrichtlinien für Ihre Organisation konfigurieren.

Hinweis: Eine *nicht konfigurierte* Website ist eine Website, die den IE-Modus erfordert, aber nicht für das Öffnen im IE-Modus in der Enterprise Mode Site List konfiguriert ist.

## <a name="local-site-list-experience"></a>Lokale Websitelistenoberfläche

Um die lokale Websitelistenumgebung zu aktivieren, können Benutzer die URL *edge://settings/defaultBrowser* aufrufen und festlegen, **dass Websites im Internet Explorer-Modus neu geladen werden** können, auf **"Zulassen".**

:::image type="content" source="media/Edge-hybrid-IE-mode/internet-explorer-compatibilitiy.png" alt-text="Internet Explorer-Kompatibilität":::

>[!Note]  
>
>1. Wenn Sie IE-Modustests über die *InternetExplorerIntegrationTestingAllowed-Richtlinie* aktiviert haben, wird diese Einstellung angezeigt, sie wird jedoch abgeblendet, es sei denn, Sie aktivieren explizit die *InternetExplorerIntegrationReloadInIEModeAllowed-Richtlinie.*
>
>2. Wenn **"Neuladen von Websites im Internet Explorer-Modus zulassen"** auf **"Standard"** festgelegt ist, können Benutzer möglicherweise Websites im IE-Modus neu laden, wenn sie über eine vorhandene Internet Explorer 11-Verwendung verfügen.  

Wenn diese Einstellung aktiviert ist, können Benutzer eine Website im IE-Modus erneut laden, indem **sie Einstellungen und mehr auswählen (das Ellipsensymbol ...) > im Internet Explorer-Modus neu laden.** Benutzer können auch **die Registerkarte "Neu laden" im Internet Explorer-Modus** auswählen, wenn sie mit der rechten Maustaste auf eine Registerkarte klicken, oder auf der **neuen Registerkarte "Internet Explorer-Modus öffnen"** klicken, wenn sie mit der rechten Maustaste auf einen Link klicken.

:::image type="content" source="media/Edge-hybrid-IE-mode/reload-in-internet-exploror-mode-screenshot.png" alt-text="Neuladen im Internet Explorer-Modus":::

Das Symbol für das **Erneute Laden im Internet Explorer-Modus** kann an die Symbolleiste angeheftet werden. Die Symbolleistenschaltfläche ermöglicht Benutzern den einfachen Zugriff auf den IE-Modus und kann über die *edge://settings/appearance-URL* verwaltet werden.

:::image type="content" source="media/Edge-hybrid-IE-mode/reload-in-internet-exploror-mode-icon-screenshot.png" alt-text="Neuladen im Internet Explorer-Modus-Symbol":::

>[!Note]
>Wenn sich der Benutzer auf einer Website befindet, die sich bereits in der Enterprise Mode Site List der Organisation befindet, sind optionen zum Neuladen (oder Beenden) des Internet Explorer-Modus sichtbar, aber abgeblendet.

Wenn die Option ausgewählt ist, wird die Website im IE-Modus neu geladen. Das Symbol für den IE-Modus ist links neben der Adressleiste sichtbar, und das Flyout zeigt eine Option an, mit der Benutzer beim nächsten Mal auf "Seite im Internet Explorer-Modus öffnen" umschalten können. Dadurch wird die spezifische Seite, auf der sich der Benutzer befindet, zur lokalen Websiteliste hinzugefügt und für die nächsten 30 Tage automatisch im IE-Modus geöffnet.

:::image type="content" source="media/Edge-hybrid-IE-mode/site-has-been-reloaded-in-ie-mode-screenshot.png" alt-text="Diese Seite ist im Internet Explorer-Modus geöffnet":::

Nachdem eine Website im "seiteninternen" IE-Modus neu geladen wurde, verbleiben die Navigationen im IE-Modus (z. B. ein Link, ein Skript oder ein Formular auf der Seite oder eine serverseitige Umleitung von einer anderen "seiteninternen" Navigation).  

Im IE-Modus wird Benutzern ein Banner angezeigt, das angibt, dass sie sich im IE-Modus befinden, die Option zum Verlassen des IE-Modus und zum Anheften des IE-Modussymbols an die Symbolleiste (wenn es nicht bereits angeheftet ist).

:::image type="content" source="media/Edge-hybrid-IE-mode/ie-mode-banner-screenshot.png" alt-text="Banner für den IE-Modus":::

Benutzer können den IE-Modus mithilfe der Schaltfläche "Verlassen" auf dem Banner, des angehefteten IE-Modussymbols oder **Einstellungen und mehr beenden (das Ellipsensymbol ...) > Internet Explorer-Modus beenden.** Andernfalls wird Microsoft Edge automatisch aus dem IE-Modus beendet, wenn eine Navigation stattfindet, die nicht "auf der Seite" ist (z. B. mithilfe der Adressleiste, der Zurück-Schaltfläche oder eines bevorzugten Links).

Einträge verbleiben für einen Standardzeitraum von 30 Tagen in der lokalen Websiteliste. Es wird empfohlen, ältere Websites für Ihre Organisation in der Websiteliste für den Enterprise modus zu konfigurieren. Die lokale Websiteliste stellt sicher, dass Benutzer ihren Workflow fortsetzen können, ohne unterbrochen zu werden, während die Websiteliste der Organisation aktualisiert wird. Wenn Benutzer an Tag 31 zu der Website navigieren, wird ein Banner angezeigt, in dem erläutert wird, dass die Website nicht mehr im IE-Modus geladen wird. Benutzer können es wieder der lokalen Websiteliste hinzufügen, wenn sie dies wünschen.

:::image type="content" source="media/Edge-hybrid-IE-mode/page-will-no-longer-load-in-ie-mode-screenshot.png" alt-text="Seite wird im IE-Modus nicht mehr geladen":::

## <a name="policies-to-configure-the-use-of-local-site-lists-for-ie-mode"></a>Richtlinien zum Konfigurieren der Verwendung lokaler Websitelisten für den IE-Modus

Zwei Gruppenrichtlinien stehen zur Verfügung, um die lokale Websitelistenoberfläche in Microsoft Edge zu konfigurieren. Diese Richtlinien lauten:

### *<a name="policy-internetexplorerintegrationreloadiniemodeallowed"></a>Richtlinie: InternetExplorerIntegrationReloadInIEModeAllowed*

Diese Richtlinie entspricht der Microsoft Edge Einstellung "Zulassen, dass Websites im Internet Explorer-Modus neu geladen werden". Sie können auf diese Einstellung zugreifen, indem Sie zur URL *edge://settings/defaultbrowser* wechseln.

- Wenn Sie diese Richtlinie aktivieren, können Benutzer eine Website im IE-Modus erneut laden, indem **sie Einstellungen und mehr auswählen (das Ellipsensymbol ... > Im Internet Explorer-Modus neu laden.** Benutzer können auch **die Registerkarte "Neu laden" im Internet Explorer-Modus** auswählen, wenn sie mit der rechten Maustaste auf eine Registerkarte klicken, oder wenn sie mit der rechten Maustaste auf einen Link klicken, wählen Sie **"Link im neuen Internet Explorer-Modus öffnen"** aus.
Benutzer können optional Microsoft Edge anweisen, den IE-Modus für die Website in Zukunft zu verwenden. Diese Auswahl wird für eine Standardeinstellung von 30 Tagen gespeichert und kann mithilfe der Richtlinie *InternetExplorerIntegrationLocalSiteListExpirationDays*verwaltet werden.

- Wenn Sie diese Richtlinie deaktivieren, können Benutzer eine nicht konfigurierte Website im IE-Modus nicht erneut laden.

- Wenn Sie diese Richtlinie nicht konfigurieren, zeigen wir Benutzern Optionen zum erneuten Laden nicht konfigurierter Websites im IE-Modus an, abhängig von der aktuellen Internet Explorer 11-Verwendung.

Beachten Sie, dass diese Richtlinie Vorrang vor der Konfiguration der [InternetExplorerIntegrationTestingAllowed-Richtlinie](/deployedge/microsoft-edge-policies#internetexplorerintegrationtestingallowed) hat und diese Richtlinie deaktiviert wird.

### *<a name="policy-internetexplorerintegrationlocalsitelistexpirationdays"></a>Richtlinie: InternetExplorerIntegrationLocalSiteListExpirationDays*

Diese Richtlinie kann verwendet werden, um die Anzahl der Tage anzupassen, die eine Website in der lokalen Websiteliste für Benutzer verbleibt.  

- Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, wird ein Standardwert von 30 Tagen verwendet.

- Wenn Sie die Richtlinie aktivieren, müssen Sie einen Wert zwischen 0 und 90 Tagen eingeben, um die Website in der lokalen Websiteliste eines Benutzers zu speichern.

Diese Richtlinie hat keine Auswirkung, wenn Sie die *InternetExplorerIntegrationReloadInIEModeAllowed-Richtlinie* deaktiviert haben.

**Hinweis:**

Die lokale Websiteliste wird derzeit nicht geräteübergreifend synchronisiert. Diese Verbesserung befindet sich derzeit in unserem Backlog, und wir werden aktualisieren, wenn diese verfügbar wird.

## <a name="see-also"></a>Siehe auch

Deaktivieren von Internet Explorer 11 – [Deaktivieren von Internet Explorer 11 | Microsoft-Dokumente](/deployedge/edge-ie-disable-ie11)

Konfigurieren von IE-Modusrichtlinien – [Konfigurieren von Richtlinien für den IE-Modus | Microsoft-Dokumente](/deployedge/edge-ie-mode-policies)

