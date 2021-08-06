---
title: Microsoft Edge und konfigurierbare Websites im IE-Modus
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Microsoft Edge und konfigurierbare Websites im IE-Modus
ms.openlocfilehash: 4f9a2b3f1d45b11f3ec299343cd57a89ecb0356179e6884064333d4b8f12e6cc
ms.sourcegitcommit: d44c0997ffe40d67421312ed96e7766da947eaa0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "11724308"
---
# <a name="learn-about-configurable-sites-in-ie-mode"></a>Informationen über konfigurierbare Websites im IE-Modus

In diesem Artikel wird das Feature "konfigurierbare Websites" der Enterprise Mode Site List erläutert, wenn Sie den IE-Modus in Microsoft Edge verwenden.

## <a name="prerequisites"></a>Voraussetzungen

- Windows-Updates

  - Windows 10, Version 1909, Windows Server, Version 1909 – KB4550945 oder höher
  - Windows 10, Version 1903, Windows Server, Version 1903 – KB4550945 oder höher
  - Windows 10, Version 1809, Windows Server, Version 1809, und Windows Server 2019 – KB4550969 oder höher
  - Windows 10, Version 1803 – KB4550944 oder höher
  - Windows 10, Version 1607, Windows Server 2016 – KB4556826 oder höher
  - Windows 10, Anfangsversion, Juli 2015 – KB4550947 oder höher
  - Windows 8.1 – KB4556798 oder höher

- Microsoft Edge, Version 83 oder höher
- [IE-Modus](./edge-ie-mode.md) konfiguriert mit Enterprise Mode Site List

## <a name="overview"></a>Übersicht

Das Konfigurieren von Websites, die den IE-Modus in der Enterprise Mode Site List benötigen, eignet sich gut für die meisten Umgebungen mit älteren Anwendungen. In einigen Fällen ist dieser Ansatz nicht der beste, um eine Teilmenge von-Websites so zu konfigurieren, dass sie im IE-Modus geöffnet werden, ohne eine gesamte Domäne im IE-Modus zu rendern. Dies trifft beispielsweise zu, wenn Ihre Umgebung sowohl moderne als auch ältere Anwendungen enthält, die auf einem einzigen Server ausgeführt werden, und Sie die Flexibilität haben möchten, nur die älteren Anwendungen im IE-, die verbleibenden aber im Microsoft Edge-Modus auszuführen.

Die Lösung besteht darin, das Feature "konfigurierbare Websites" der Enterprise Mode Site List zu verwenden. Wenn das Feature aktiviert ist, erlaubt Microsoft Edge Websites mit dem Tag „konfigurierbar“ an der IE-Modus-Engine-Bestimmung teilzunehmen.

## <a name="how-configurable-sites-works"></a>Funktionsweise konfigurierbarer Websites

### <a name="automatic-switching-from-the-microsoft-edge-engine-to-the-ie-mode-engine"></a>Automatischer Umstieg von der Microsoft Edge-Engine auf die IE-Modus-Engine

Um das Feature "konfigurierbare Websites" verwenden zu können, benötigen Sie mindestens eine Website in der Enterprise Mode Site List, um die Option "`<open-in>Configurable</open-in>`" zu nutzen.

Beispiel:

```
<site-list version="1">
  <site url="app.com">
    <open-in>Configurable</open-in>
  </site>
</site-list>
```

Wenn das Feature "konfigurierbare Websites" aktiviert ist, tritt das folgende Verhalten auf:

1. Wenn Sie eine Anforderung an eine konfigurierbare Website stellen, sendet Microsoft Edge den HTTP-Anforderungsheader "`X-InternetExplorerModeConfigurable: 1`".
2. Eine konfigurierbare Website sendet möglicherweise eine Umleitungsantwort (z. B. HTTP 302) mit dem HTTP-Antwortheader "`X-InternetExplorerMode: 1`", um anzufordern, dass Microsoft Edge die Website im IE-Modus lädt.
3. Das Ziel der Umleitung (d. h. der Wert des Antwortheaders **Standort**) muss auch eine **konfigurierbare** oder **neutrale** Website sein. Andernfalls wird der Antwortheader für den IE-Modus ignoriert. Es wird erwartet, dass das Ziel der Umleitung in der Regel mit der ursprünglichen URL übereinstimmt. Dies muss jedoch nicht immer der Fall sein.

   > [!NOTE]
   > Die Umleitungsantwort unterliegt einer Zwischenspeicherung entsprechend dem üblichen HTTP-Zwischenspeicherungsverhalten von Microsoft Edge für Umleitungen.

### <a name="switching-back-from-ie-mode-engine-to-microsoft-edge-engine"></a>Zurückkehren vom IE-Modus-Modul zum Microsoft Edge-Modul

Wenn Sie das Feature „konfigurierbare Websites“ in Microsoft Edge aktivieren, wird automatisch das folgende Verhalten auf den Registerkarten im IE-Modus aktiviert:

1. Wenn Sie eine Anforderung an eine konfigurierbare Website stellen, senden die Registerkarten im IE-Modus den gleichen Anforderungsheader "`X-InternetExplorerModeConfigurable: 1`" wie die Microsoft Edge-Registerkarten.
2. Eine konfigurierbare Website sendet möglicherweise eine Umleitungsantwort (z. B. HTTP 302) mit dem HTTP-Antwortheader "`X-InternetExplorerMode: 0`", um anzufordern, dass die Navigation zum Microsoft Edge-Modus zurückwechselt.
3. Das Ziel der Umleitung (d. h. der Wert des Antwortheaders **Standort**) muss auch eine **konfigurierbare** oder **neutrale** Website sein. Andernfalls wird der Antwortheader für den IE-Modus ignoriert. Es wird erwartet, dass das Ziel der Umleitung in der Regel mit der ursprünglichen URL übereinstimmt. Dies muss jedoch nicht immer der Fall sein.

   > [!NOTE]
   > Die Umleitungsantwort unterliegt einer Zwischenspeicherung entsprechend dem üblichen HTTP-Zwischenspeicherungsverhalten von Microsoft Edge für Umleitungen.

> [!TIP]
> Beide Browsermodule senden den gleichen Anforderungsheader „`X-InternetExplorerModeConfigurable: 1`“ an konfigurierbare Websites. Sie sollten den Anforderungsheader „User-Agent“ verwenden, um zwischen den Anforderungen des Microsoft Edge-Modus und des IE-Modus zu unterscheiden. Auf diese Weise vermeiden Sie eine Umleitung, wenn die Website bereits im richtigen Modul geladen wird.

## <a name="see-also"></a>Weitere Informationen

- [Informationen zum IE-Modus](./edge-ie-mode.md)
- [Weitere Informationen zum Unternehmensmodus](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [Angebotsseite für Microsoft Edge für Unternehmen](https://aka.ms/EdgeEnterprise)