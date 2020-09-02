---
title: Microsoft Edge und konfigurierbare Websites im IE-Modus
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 05/28/2020
audience: ITPro
ms.topic: procedural
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Edge und konfigurierbare Websites im IE-Modus
ms.openlocfilehash: a846d71d63a4f837041acc9b601f704999bb826a
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/31/2020
ms.locfileid: "10980038"
---
# Informationen über konfigurierbare Websites im IE-Modus

In diesem Artikel wird das Feature "konfigurierbare Websites" der Enterprise Mode Site List erläutert, wenn Sie den IE-Modus in Microsoft Edge verwenden.

## Voraussetzungen

- Windows-Updates

  - Windows10, Version1909, Windows Server, Version1909– KB4550945 oder höher
  - Windows10, Version1903, Windows Server, Version1903– KB4550945 oder höher
  - Windows10, Version1809, Windows Server, Version1809, und Windows Server2019– KB4550969 oder höher
  - Windows10, Version1803– KB4550944 oder höher
  - Windows10, Version1607, Windows Server2016– KB4556826 oder höher
  - Windows10, Anfangsversion, Juli2015– KB4550947 oder höher
  - Windows8.1– KB4556798 oder höher

- Microsoft Edge, Version83 oder höher
- [IE-Modus](https://aka.ms/iemodeonedge) konfiguriert mit Enterprise Mode Site List

## Übersicht

Das Konfigurieren von Websites, die den IE-Modus in der Enterprise Mode Site List benötigen, eignet sich gut für die meisten Umgebungen mit älteren Anwendungen. In einigen Fällen ist dieser Ansatz nicht der beste, um eine Teilmenge von-Websites so zu konfigurieren, dass sie im IE-Modus geöffnet werden, ohne eine gesamte Domäne im IE-Modus zu rendern. Dies trifft beispielsweise zu, wenn Ihre Umgebung sowohl moderne als auch ältere Anwendungen enthält, die auf einem einzigen Server ausgeführt werden, und Sie die Flexibilität haben möchten, nur die älteren Anwendungen im IE-, die verbleibenden aber im Microsoft Edge-Modus auszuführen.

Die Lösung besteht darin, das Feature "konfigurierbare Websites" der Enterprise Mode Site List zu verwenden. Wenn das Feature aktiviert ist, erlaubt Microsoft Edge Websites mit dem Tag „konfigurierbar“ an der IE-Modus-Engine-Bestimmung teilzunehmen.

## Funktionsweise konfigurierbarer Websites

### Automatischer Umstieg von der Microsoft Edge-Engine auf die IE-Modus-Engine

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
2. Eine konfigurierbare Website sendet möglicherweise eine Umleitungsantwort (z.B. HTTP 302) mit dem HTTP-Antwortheader "`X-InternetExplorerMode: 1`", um anzufordern, dass Microsoft Edge die Website im IE-Modus lädt.
3. Das Ziel der Umleitung (d.h. der Wert des Antwortheaders **Standort**) muss auch eine **konfigurierbare** oder **neutrale** Website sein. Andernfalls wird der Antwortheader für den IE-Modus ignoriert. Es wird erwartet, dass das Ziel der Umleitung in der Regel mit der ursprünglichen URL übereinstimmt. Dies muss jedoch nicht immer der Fall sein.

   > [!NOTE]
   > Die Umleitungsantwort unterliegt einer Zwischenspeicherung entsprechend dem üblichen HTTP-Zwischenspeicherungsverhalten von Microsoft Edge für Umleitungen.

### Zurückkehren vom IE-Modus-Modul zum Microsoft Edge-Modul

Wenn Sie das Feature „konfigurierbare Websites“ in Microsoft Edge aktivieren, wird automatisch das folgende Verhalten auf den Registerkarten im IE-Modus aktiviert:

1. Wenn Sie eine Anforderung an eine konfigurierbare Website stellen, senden die Registerkarten im IE-Modus den gleichen Anforderungsheader "`X-InternetExplorerModeConfigurable: 1`" wie die Microsoft Edge-Registerkarten.
2. Eine konfigurierbare Website sendet möglicherweise eine Umleitungsantwort (z.B. HTTP 302) mit dem HTTP-Antwortheader "`X-InternetExplorerMode: 0`", um anzufordern, dass die Navigation zum Microsoft Edge-Modus zurückwechselt.
3. Das Ziel der Umleitung (d.h. der Wert des Antwortheaders **Standort**) muss auch eine **konfigurierbare** oder **neutrale** Website sein. Andernfalls wird der Antwortheader für den IE-Modus ignoriert. Es wird erwartet, dass das Ziel der Umleitung in der Regel mit der ursprünglichen URL übereinstimmt. Dies muss jedoch nicht immer der Fall sein.

   > [!NOTE]
   > Die Umleitungsantwort unterliegt einer Zwischenspeicherung entsprechend dem üblichen HTTP-Zwischenspeicherungsverhalten von Microsoft Edge für Umleitungen.

> [!TIP]
> Beide Browsermodule senden den gleichen Anforderungsheader „`X-InternetExplorerModeConfigurable: 1`“ an konfigurierbare Websites. Sie sollten den Anforderungsheader „User-Agent“ verwenden, um zwischen den Anforderungen des Microsoft Edge-Modus und des IE-Modus zu unterscheiden. Auf diese Weise vermeiden Sie eine Umleitung, wenn die Website bereits im richtigen Modul geladen wird.

## Weitere Informationen

- [Informationen zum IE-Modus](https://docs.microsoft.com/deployedge/edge-ie-mode)
- [Weitere Informationen zum Unternehmensmodus](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [Angebotsseite für Microsoft Edge für Unternehmen](https://aka.ms/EdgeEnterprise)