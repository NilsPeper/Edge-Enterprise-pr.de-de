---
title: Zulassungsliste für Microsoft Edge-Endpunkte
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 11/25/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Zulassungsliste für Microsoft Edge-Endpunkte
ms.openlocfilehash: b8f793edcc23798199fe5de1bfae912a63468464
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/24/2021
ms.locfileid: "11448199"
---
# <a name="allow-list-for-microsoft-edge-endpoints"></a><span data-ttu-id="8be75-103">Zulassungsliste für Microsoft Edge-Endpunkte</span><span class="sxs-lookup"><span data-stu-id="8be75-103">Allow list for Microsoft Edge endpoints</span></span>

<span data-ttu-id="8be75-104">Microsoft Edge erfordert zur Unterstützung der zugehörigen Features eine Internetverbindung.</span><span class="sxs-lookup"><span data-stu-id="8be75-104">Microsoft Edge requires connectivity to the Internet to support its features.</span></span> <span data-ttu-id="8be75-105">In diesem Artikel werden die Domänen-URLs aufgeführt, die Sie der Zulassungsliste hinzufügen müssen, um die Kommunikation über Firewalls und andere Sicherheitsmechanismen sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="8be75-105">This article identifies the domain URLs that you need to add to the Allow list to ensure communications through firewalls and other security mechanisms.</span></span>

> [!NOTE]
> <span data-ttu-id="8be75-106">Dieser Artikel bezieht sich auf Microsoft Edge Version 77 oder neuer.</span><span class="sxs-lookup"><span data-stu-id="8be75-106">This applies  to Microsoft Edge version 77 or later.</span></span>

## <a name="domain-urls-to-allow"></a><span data-ttu-id="8be75-107">Domänen-URLs für Zulassungsliste</span><span class="sxs-lookup"><span data-stu-id="8be75-107">Domain URLs to allow</span></span>

<span data-ttu-id="8be75-108">Lassen Sie die folgenden Domänen-URLs für Microsoft Edge zu.</span><span class="sxs-lookup"><span data-stu-id="8be75-108">Allow the following domain URLs for Microsoft Edge.</span></span>

### <a name="update-service"></a><span data-ttu-id="8be75-109">Updatedienst</span><span class="sxs-lookup"><span data-stu-id="8be75-109">Update Service</span></span>

<span data-ttu-id="8be75-110">Der Dienst, der Microsoft Edge verwendet, um nach neuen Updates zu suchen.</span><span class="sxs-lookup"><span data-stu-id="8be75-110">The service that Microsoft Edge uses to check for new updates.</span></span>

- `https://msedge.api.cdp.microsoft.com`

### <a name="experimentation-and-configuration-service"></a><span data-ttu-id="8be75-111">Experimentier- und Konfigurationsservice</span><span class="sxs-lookup"><span data-stu-id="8be75-111">Experimentation and Configuration service</span></span>

- `https://config.edge.skype.com`

### <a name="download-locations-for-microsoft-edge"></a><span data-ttu-id="8be75-112">Speicherorte für den Download von Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="8be75-112">Download locations for Microsoft Edge</span></span>

<span data-ttu-id="8be75-113">Speicherorte, von denen Microsoft Edge während einer Erstinstallation oder bei einem Update heruntergeladen werden kann.</span><span class="sxs-lookup"><span data-stu-id="8be75-113">Locations Microsoft Edge can be downloaded from during an initial install or when an update is available.</span></span> <span data-ttu-id="8be75-114">Der Downloadort wird vom Update Dienst festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8be75-114">The download location is determined by the Update Service.</span></span>

#### <a name="http"></a><span data-ttu-id="8be75-115">HTTP</span><span class="sxs-lookup"><span data-stu-id="8be75-115">HTTP</span></span>

- `http://msedge.f.tlu.dl.delivery.mp.microsoft.com`
- `http://msedge.f.dl.delivery.mp.microsoft.com`
- `http://msedge.b.tlu.dl.delivery.mp.microsoft.com`
- `http://msedge.b.dl.delivery.mp.microsoft.com`

#### <a name="https"></a><span data-ttu-id="8be75-116">HTTPS</span><span class="sxs-lookup"><span data-stu-id="8be75-116">HTTPS</span></span>

- `https://msedge.sf.tlu.dl.delivery.mp.microsoft.com`
- `https://msedge.sf.dl.delivery.mp.microsoft.com`
- `https://msedge.sb.tlu.dl.delivery.mp.microsoft.com`
- `https://msedge.sb.dl.delivery.mp.microsoft.com`

  > [!TIP]
  > <span data-ttu-id="8be75-117">Zur Vereinfachung der Zulassungsliste für Downloadorte kann eine Wildcard verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="8be75-117">To simplify the allow list for download locations a wild card can be used:</span></span> `*.dl.delivery.mp.microsoft.com`

### <a name="download-locations-for-microsoft-edge-extensions"></a><span data-ttu-id="8be75-118">Speicherorte für den Download von Erweiterungen für Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="8be75-118">Download locations for Microsoft Edge Extensions</span></span>

<span data-ttu-id="8be75-119">Speicherorte, von denen Microsoft Edge-Erweiterungen während einer Erstinstallation oder bei einem Update heruntergeladen werden können.</span><span class="sxs-lookup"><span data-stu-id="8be75-119">Locations Microsoft Edge Extensions can be downloaded from during an initial install or when an update is available.</span></span> <span data-ttu-id="8be75-120">Der Downloadort wird vom Update Dienst festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8be75-120">The download location is determined by the Update Service.</span></span>

#### <a name="http"></a><span data-ttu-id="8be75-121">HTTP</span><span class="sxs-lookup"><span data-stu-id="8be75-121">HTTP</span></span>

- `http://msedgeextensions.f.tlu.dl.delivery.mp.microsoft.com`
- `http://msedgeextensions.f.dl.delivery.mp.microsoft.com`
- `http://msedgeextensions.b.tlu.dl.delivery.mp.microsoft.com`
- `http://msedgeextensions.b.dl.delivery.mp.microsoft.com`

#### <a name="https"></a><span data-ttu-id="8be75-122">HTTPS</span><span class="sxs-lookup"><span data-stu-id="8be75-122">HTTPS</span></span>

- `https://msedgeextensions.sf.tlu.dl.delivery.mp.microsoft.com`
- `https://msedgeextensions.sf.dl.delivery.mp.microsoft.com`
- `https://msedgeextensions.sb.tlu.dl.delivery.mp.microsoft.com`
- `https://msedgeextensions.sb.dl.delivery.mp.microsoft.com`

  > [!TIP]
  > <span data-ttu-id="8be75-123">Zur Vereinfachung der Zulassungsliste für Downloadorte kann eine Wildcard verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="8be75-123">To simplify the allow list for download locations a wild card can be used:</span></span> `*.dl.delivery.mp.microsoft.com`

### <a name="optionally-for-download-delivery-optimization"></a><span data-ttu-id="8be75-124">Optional für die Download-Übermittlungsoptimierung</span><span class="sxs-lookup"><span data-stu-id="8be75-124">Optionally for Download Delivery Optimization</span></span>

<span data-ttu-id="8be75-125">Weitere Informationen zur Übermittlungsoptimierung finden Sie unter [Übermittlungsoptimierung für Windows 10-Updates](/windows/deployment/update/waas-delivery-optimization).</span><span class="sxs-lookup"><span data-stu-id="8be75-125">For information about delivery optimization, see [Delivery Optimization for Windows 10 updates](/windows/deployment/update/waas-delivery-optimization).</span></span>

- <span data-ttu-id="8be75-126">Kommunikation Client-zu-Dienst: `*.do.dsp.mp.microsoft.com` : (HTTP Port 80, HTTPS Port 443)</span><span class="sxs-lookup"><span data-stu-id="8be75-126">Client to Service communication: `*.do.dsp.mp.microsoft.com` (HTTP Port 80, HTTPS Port 443)</span></span>
- <span data-ttu-id="8be75-127">Kommunikation Client-zu-Client: TCP-Port 7680 muss für eingehenden Datenverkehr geöffnet sein</span><span class="sxs-lookup"><span data-stu-id="8be75-127">Client to Client communication: TCP port 7680 should be open for inbound traffic</span></span>

### <a name="sync"></a><span data-ttu-id="8be75-128">Sync</span><span class="sxs-lookup"><span data-stu-id="8be75-128">Sync</span></span>

<span data-ttu-id="8be75-129">Diese Endpunkte verwalten das Lesen und Schreiben von synchronisierten Daten, die Rechteverwaltung für sichere Daten und die Benachrichtigung des Browsers, wenn neue Synchronisierungsdaten verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="8be75-129">These endpoints manage the reading and writing of synced data, rights management for secure data, and notifying the browser when new sync data is available.</span></span>

- <span data-ttu-id="8be75-130">Edge-Synchronisierungsdienst-Endpunkte:</span><span class="sxs-lookup"><span data-stu-id="8be75-130">Edge sync service endpoints:</span></span>

  - `https://edge-enterprise.activity.windows.com`
  - `https://edge.activity.windows.com`

- <span data-ttu-id="8be75-131">Azure Information Protection-Endpunkte:</span><span class="sxs-lookup"><span data-stu-id="8be75-131">Azure Information Protection endpoints:</span></span>

  - `https://api.aadrm.com` <span data-ttu-id="8be75-132">(für die meisten Mandanten)</span><span class="sxs-lookup"><span data-stu-id="8be75-132">(for most tenants)</span></span>
  - `https://api.aadrm.de` <span data-ttu-id="8be75-133">(für Mandanten in Deutschland)</span><span class="sxs-lookup"><span data-stu-id="8be75-133">(for tenants in Germany)</span></span>
  - `https://api.aadrm.cn` <span data-ttu-id="8be75-134">(für Mandanten in China)</span><span class="sxs-lookup"><span data-stu-id="8be75-134">(for tenants in China)</span></span>

- [<span data-ttu-id="8be75-135">Windows-Benachrichtigungsdienst-Endpunkte</span><span class="sxs-lookup"><span data-stu-id="8be75-135">Windows Notification Service endpoints</span></span>](/windows/uwp/design/shell/tiles-and-notifications/firewall-allowlist-config)

## <a name="other-browser-support-services"></a><span data-ttu-id="8be75-136">Andere Dienste zur Browserunterstützung</span><span class="sxs-lookup"><span data-stu-id="8be75-136">Other browser support services</span></span>

<span data-ttu-id="8be75-137">Stellen Sie Metadaten für Browser Features bereit, z.B. Tracking-Schutz, Zertifikatsperrlisten und Updates für Browserkomponenten.</span><span class="sxs-lookup"><span data-stu-id="8be75-137">Provide metadata for browser features such as tracking protection, certificate revocation lists, and other browser component updates.</span></span> <span data-ttu-id="8be75-138">Stellen Sie herunterladbare Rechtschreibwörterbücher und Listen zur Blockierung von Werbung bereit.</span><span class="sxs-lookup"><span data-stu-id="8be75-138">Provide downloadable spellcheck dictionaries and ad-blocking block lists.</span></span> <span data-ttu-id="8be75-139">Stellen Sie Dienste bereit, um Browserfeatures wie Sammlungen, AutoFill und Erweiterungsspeicher zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="8be75-139">Provide services to support browser features such as collections, autofill, and extension store.</span></span>

- `http://edge.microsoft.com/`
- `https://edge.microsoft.com/`

## <a name="see-also"></a><span data-ttu-id="8be75-140">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8be75-140">See also</span></span>

- [<span data-ttu-id="8be75-141">Microsoft Edge Enterprise-Angebotsseite</span><span class="sxs-lookup"><span data-stu-id="8be75-141">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="8be75-142">Angebotsseite der Microsoft Edge-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="8be75-142">Microsoft Edge documentation landing page</span></span>](./index.yml)
- [<span data-ttu-id="8be75-143">Verwalten von Verbindungsendpunkten für Windows 10 Enterprise, Version 1903</span><span class="sxs-lookup"><span data-stu-id="8be75-143">Manage connection endpoints for Windows 10 Enterprise, version 1903</span></span>](/windows/privacy/manage-windows-1903-endpoints)