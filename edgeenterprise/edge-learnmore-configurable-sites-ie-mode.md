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
# <span data-ttu-id="f3c54-103">Informationen über konfigurierbare Websites im IE-Modus</span><span class="sxs-lookup"><span data-stu-id="f3c54-103">Learn about Configurable sites in IE mode</span></span>

<span data-ttu-id="f3c54-104">In diesem Artikel wird das Feature "konfigurierbare Websites" der Enterprise Mode Site List erläutert, wenn Sie den IE-Modus in Microsoft Edge verwenden.</span><span class="sxs-lookup"><span data-stu-id="f3c54-104">This article explains the Configurable sites feature of the Enterprise Mode Site List when using IE mode in Microsoft Edge.</span></span>

## <span data-ttu-id="f3c54-105">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="f3c54-105">Prerequisites</span></span>

- <span data-ttu-id="f3c54-106">Windows-Updates</span><span class="sxs-lookup"><span data-stu-id="f3c54-106">Windows updates</span></span>

  - <span data-ttu-id="f3c54-107">Windows 10, Version 1909, Windows Server, Version 1909 – KB4550945 oder höher</span><span class="sxs-lookup"><span data-stu-id="f3c54-107">Windows 10 version 1909, Windows server version 1909 – KB4550945  or higher</span></span>
  - <span data-ttu-id="f3c54-108">Windows 10, Version 1903, Windows Server, Version 1903 – KB4550945 oder höher</span><span class="sxs-lookup"><span data-stu-id="f3c54-108">Windows 10 version 1903, Windows server version 1903 – KB4550945  or higher</span></span>
  - <span data-ttu-id="f3c54-109">Windows 10, Version 1809, Windows Server, Version 1809, und Windows Server 2019 – KB4550969 oder höher</span><span class="sxs-lookup"><span data-stu-id="f3c54-109">Windows 10 version 1809, Windows Server version 1809, and Windows Server 2019 - KB4550969 or higher</span></span>
  - <span data-ttu-id="f3c54-110">Windows 10, Version 1803 – KB4550944 oder höher</span><span class="sxs-lookup"><span data-stu-id="f3c54-110">Windows 10 version 1803 – KB4550944 or higher</span></span>
  - <span data-ttu-id="f3c54-111">Windows 10, Version 1607, Windows Server 2016 – KB4556826 oder höher</span><span class="sxs-lookup"><span data-stu-id="f3c54-111">Windows 10 version 1607, Windows Server 2016 - KB4556826 or higher</span></span>
  - <span data-ttu-id="f3c54-112">Windows 10, Anfangsversion, Juli 2015 – KB4550947 oder höher</span><span class="sxs-lookup"><span data-stu-id="f3c54-112">Windows 10 initial version, July 2015 - KB4550947 or higher</span></span>
  - <span data-ttu-id="f3c54-113">Windows 8.1 – KB4556798 oder höher</span><span class="sxs-lookup"><span data-stu-id="f3c54-113">Windows 8.1 – KB4556798 or higher</span></span>

- <span data-ttu-id="f3c54-114">Microsoft Edge, Version 83 oder höher</span><span class="sxs-lookup"><span data-stu-id="f3c54-114">Microsoft Edge version 83 or later</span></span>
- <span data-ttu-id="f3c54-115">[IE-Modus](https://aka.ms/iemodeonedge) konfiguriert mit Enterprise Mode Site List</span><span class="sxs-lookup"><span data-stu-id="f3c54-115">[IE mode](https://aka.ms/iemodeonedge) configured with Enterprise Mode Site List</span></span>

## <span data-ttu-id="f3c54-116">Übersicht</span><span class="sxs-lookup"><span data-stu-id="f3c54-116">Overview</span></span>

<span data-ttu-id="f3c54-117">Das Konfigurieren von Websites, die den IE-Modus in der Enterprise Mode Site List benötigen, eignet sich gut für die meisten Umgebungen mit älteren Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="f3c54-117">Configuring sites needing IE mode in the Enterprise Mode Site List will work well for most environments with legacy applications.</span></span> <span data-ttu-id="f3c54-118">In einigen Fällen ist dieser Ansatz nicht der beste, um eine Teilmenge von-Websites so zu konfigurieren, dass sie im IE-Modus geöffnet werden, ohne eine gesamte Domäne im IE-Modus zu rendern.</span><span class="sxs-lookup"><span data-stu-id="f3c54-118">However, in some cases this approach isn't the best to configure a subset of sites to open in IE mode without rendering an entire domain in IE mode.</span></span> <span data-ttu-id="f3c54-119">Dies trifft beispielsweise zu, wenn Ihre Umgebung sowohl moderne als auch ältere Anwendungen enthält, die auf einem einzigen Server ausgeführt werden, und Sie die Flexibilität haben möchten, nur die älteren Anwendungen im IE-, die verbleibenden aber im Microsoft Edge-Modus auszuführen.</span><span class="sxs-lookup"><span data-stu-id="f3c54-119">For example, when your environment contains both modern and legacy applications running on a single server and you would like the flexibility to render only the legacy applications in IE mode and the remaining applications to render in Microsoft Edge mode.</span></span>

<span data-ttu-id="f3c54-120">Die Lösung besteht darin, das Feature "konfigurierbare Websites" der Enterprise Mode Site List zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="f3c54-120">The solution is to use the Configurable sites feature of the Enterprise Mode Site List.</span></span> <span data-ttu-id="f3c54-121">Wenn das Feature aktiviert ist, erlaubt Microsoft Edge Websites mit dem Tag „konfigurierbar“ an der IE-Modus-Engine-Bestimmung teilzunehmen.</span><span class="sxs-lookup"><span data-stu-id="f3c54-121">When the feature is enabled, Microsoft Edge will allow sites with the "configurable" tag to participate in IE mode engine determination.</span></span>

## <span data-ttu-id="f3c54-122">Funktionsweise konfigurierbarer Websites</span><span class="sxs-lookup"><span data-stu-id="f3c54-122">How Configurable sites works</span></span>

### <span data-ttu-id="f3c54-123">Automatischer Umstieg von der Microsoft Edge-Engine auf die IE-Modus-Engine</span><span class="sxs-lookup"><span data-stu-id="f3c54-123">Automatic switching from the Microsoft Edge engine to the IE mode engine</span></span>

<span data-ttu-id="f3c54-124">Um das Feature "konfigurierbare Websites" verwenden zu können, benötigen Sie mindestens eine Website in der Enterprise Mode Site List, um die Option "`<open-in>Configurable</open-in>`" zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="f3c54-124">To use the Configurable sites feature, you'll need one or more sites in the Enterprise Mode Site List to have the `<open-in>Configurable</open-in>` option.</span></span>

<span data-ttu-id="f3c54-125">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="f3c54-125">Example:</span></span>

```
<site-list version="1">
  <site url="app.com">
    <open-in>Configurable</open-in>
  </site>
</site-list>
```

<span data-ttu-id="f3c54-126">Wenn das Feature "konfigurierbare Websites" aktiviert ist, tritt das folgende Verhalten auf:</span><span class="sxs-lookup"><span data-stu-id="f3c54-126">When the Configurable sites feature is enabled, the following behavior occurs:</span></span>

1. <span data-ttu-id="f3c54-127">Wenn Sie eine Anforderung an eine konfigurierbare Website stellen, sendet Microsoft Edge den HTTP-Anforderungsheader "`X-InternetExplorerModeConfigurable: 1`".</span><span class="sxs-lookup"><span data-stu-id="f3c54-127">When making a request to a Configurable site, Microsoft Edge will send the HTTP request header "`X-InternetExplorerModeConfigurable: 1`".</span></span>
2. <span data-ttu-id="f3c54-128">Eine konfigurierbare Website sendet möglicherweise eine Umleitungsantwort (z. B. HTTP 302) mit dem HTTP-Antwortheader "`X-InternetExplorerMode: 1`", um anzufordern, dass Microsoft Edge die Website im IE-Modus lädt.</span><span class="sxs-lookup"><span data-stu-id="f3c54-128">A Configurable site may send a redirect response (for example, HTTP 302) with the HTTP response header "`X-InternetExplorerMode: 1`" to request that Microsoft Edge loads the site in IE mode.</span></span>
3. <span data-ttu-id="f3c54-129">Das Ziel der Umleitung (d. h. der Wert des Antwortheaders **Standort**) muss auch eine **konfigurierbare** oder **neutrale** Website sein. Andernfalls wird der Antwortheader für den IE-Modus ignoriert.</span><span class="sxs-lookup"><span data-stu-id="f3c54-129">The target of the redirect (that is, the value of the **Location** response header) must also be a **Configurable** or **Neutral** site, otherwise the IE mode response header will be ignored.</span></span> <span data-ttu-id="f3c54-130">Es wird erwartet, dass das Ziel der Umleitung in der Regel mit der ursprünglichen URL übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="f3c54-130">It's expected that the target of the redirect will usually be the same as the original URL.</span></span> <span data-ttu-id="f3c54-131">Dies muss jedoch nicht immer der Fall sein.</span><span class="sxs-lookup"><span data-stu-id="f3c54-131">However, it doesn't have to be.</span></span>

   > [!NOTE]
   > <span data-ttu-id="f3c54-132">Die Umleitungsantwort unterliegt einer Zwischenspeicherung entsprechend dem üblichen HTTP-Zwischenspeicherungsverhalten von Microsoft Edge für Umleitungen.</span><span class="sxs-lookup"><span data-stu-id="f3c54-132">The redirect response is subject to caching according to Microsoft Edge's normal HTTP caching behavior for redirects.</span></span>

### <span data-ttu-id="f3c54-133">Zurückkehren vom IE-Modus-Modul zum Microsoft Edge-Modul</span><span class="sxs-lookup"><span data-stu-id="f3c54-133">Switching back from IE mode engine to Microsoft Edge engine</span></span>

<span data-ttu-id="f3c54-134">Wenn Sie das Feature „konfigurierbare Websites“ in Microsoft Edge aktivieren, wird automatisch das folgende Verhalten auf den Registerkarten im IE-Modus aktiviert:</span><span class="sxs-lookup"><span data-stu-id="f3c54-134">Enabling Configurable sites in Microsoft Edge automatically enables the following behaviors in IE mode tabs:</span></span>

1. <span data-ttu-id="f3c54-135">Wenn Sie eine Anforderung an eine konfigurierbare Website stellen, senden die Registerkarten im IE-Modus den gleichen Anforderungsheader "`X-InternetExplorerModeConfigurable: 1`" wie die Microsoft Edge-Registerkarten.</span><span class="sxs-lookup"><span data-stu-id="f3c54-135">When making a request to a Configurable site, IE mode tabs will send the HTTP request header "`X-InternetExplorerModeConfigurable: 1`", the same as Microsoft Edge tabs.</span></span>
2. <span data-ttu-id="f3c54-136">Eine konfigurierbare Website sendet möglicherweise eine Umleitungsantwort (z. B. HTTP 302) mit dem HTTP-Antwortheader "`X-InternetExplorerMode: 0`", um anzufordern, dass die Navigation zum Microsoft Edge-Modus zurückwechselt.</span><span class="sxs-lookup"><span data-stu-id="f3c54-136">A Configurable site might send a redirect response (for example, HTTP 302) with the HTTP response header "`X-InternetExplorerMode: 0`" to request that the navigation switch back to Microsoft Edge mode.</span></span>
3. <span data-ttu-id="f3c54-137">Das Ziel der Umleitung (d. h. der Wert des Antwortheaders **Standort**) muss auch eine **konfigurierbare** oder **neutrale** Website sein. Andernfalls wird der Antwortheader für den IE-Modus ignoriert.</span><span class="sxs-lookup"><span data-stu-id="f3c54-137">The target of the redirect (that is, the value of the **Location** response header) must also be a **Configurable** or **Neutral** site, otherwise the IE mode response header will be ignored.</span></span> <span data-ttu-id="f3c54-138">Es wird erwartet, dass das Ziel der Umleitung in der Regel mit der ursprünglichen URL übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="f3c54-138">It's expected that the target of the redirect will usually be the same as the original URL.</span></span> <span data-ttu-id="f3c54-139">Dies muss jedoch nicht immer der Fall sein.</span><span class="sxs-lookup"><span data-stu-id="f3c54-139">However, it doesn't have to be.</span></span>

   > [!NOTE]
   > <span data-ttu-id="f3c54-140">Die Umleitungsantwort unterliegt einer Zwischenspeicherung entsprechend dem üblichen HTTP-Zwischenspeicherungsverhalten von Microsoft Edge für Umleitungen.</span><span class="sxs-lookup"><span data-stu-id="f3c54-140">The redirect response is subject to caching according to Microsoft Edge's normal HTTP caching behavior for redirects.</span></span>

> [!TIP]
> <span data-ttu-id="f3c54-141">Beide Browsermodule senden den gleichen Anforderungsheader „`X-InternetExplorerModeConfigurable: 1`“ an konfigurierbare Websites.</span><span class="sxs-lookup"><span data-stu-id="f3c54-141">Both browser engines send the same "`X-InternetExplorerModeConfigurable: 1`" request header to Configurable sites.</span></span> <span data-ttu-id="f3c54-142">Sie sollten den Anforderungsheader „User-Agent“ verwenden, um zwischen den Anforderungen des Microsoft Edge-Modus und des IE-Modus zu unterscheiden. Auf diese Weise vermeiden Sie eine Umleitung, wenn die Website bereits im richtigen Modul geladen wird.</span><span class="sxs-lookup"><span data-stu-id="f3c54-142">You should use the User-Agent request header to distinguish between requests from Microsoft Edge mode vs. IE mode to avoid redirecting when the site is already loading in the correct engine.</span></span>

## <span data-ttu-id="f3c54-143">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f3c54-143">See also</span></span>

- [<span data-ttu-id="f3c54-144">Informationen zum IE-Modus</span><span class="sxs-lookup"><span data-stu-id="f3c54-144">About IE mode</span></span>](https://docs.microsoft.com/deployedge/edge-ie-mode)
- [<span data-ttu-id="f3c54-145">Weitere Informationen zum Unternehmensmodus</span><span class="sxs-lookup"><span data-stu-id="f3c54-145">Additional Enterprise Mode information</span></span>](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [<span data-ttu-id="f3c54-146">Angebotsseite für Microsoft Edge für Unternehmen</span><span class="sxs-lookup"><span data-stu-id="f3c54-146">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)