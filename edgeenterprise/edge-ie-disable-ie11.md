---
title: Deaktivieren von Internet Explorer 11
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 03/02/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Erfahren Sie, wie Sie Internet Explorer 11 deaktivieren und den Internet Explorer-Modus in Microsoft Edge verwenden können.
ms.openlocfilehash: 08d1fe48bfc4614710f4a341a285048194a64794
ms.sourcegitcommit: 928714329d0b11575494f557498f69a8417a3289
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "11385333"
---
# <a name="disable-internet-explorer-11"></a><span data-ttu-id="11e11-103">Deaktivieren von Internet Explorer 11</span><span class="sxs-lookup"><span data-stu-id="11e11-103">Disable Internet Explorer 11</span></span>

<span data-ttu-id="11e11-104">In diesem Artikel wird beschrieben, wie Sie Internet Explorer 11 als eigenständigen Browser in Ihrer Umgebung deaktivieren können.</span><span class="sxs-lookup"><span data-stu-id="11e11-104">This article describes how to disable Internet Explorer 11 as a standalone browser in your environment.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="11e11-105">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="11e11-105">Prerequisites</span></span>

<span data-ttu-id="11e11-106">Die folgenden Windows-Updates und Microsoft Edge-Software sind erforderlich:</span><span class="sxs-lookup"><span data-stu-id="11e11-106">The following Windows updates and Microsoft Edge software are required:</span></span>

- <span data-ttu-id="11e11-107">Windows-Updates</span><span class="sxs-lookup"><span data-stu-id="11e11-107">Windows updates</span></span>

  - <span data-ttu-id="11e11-108">Windows 10, Version 2004, Windows Server, Version 2004, Windows 10, Version 20H2: [KB4598291](https://support.microsoft.com/topic/february-2-2021-kb4598291-os-builds-19041-789-and-19042-789-preview-6a766199-a4f1-616e-1f5c-58bdc3ca5e3b) oder höher</span><span class="sxs-lookup"><span data-stu-id="11e11-108">Windows 10, version 2004, Windows Server version 2004, Windows 10, version 20H2: [KB4598291](https://support.microsoft.com/topic/february-2-2021-kb4598291-os-builds-19041-789-and-19042-789-preview-6a766199-a4f1-616e-1f5c-58bdc3ca5e3b) or later</span></span>
  - <span data-ttu-id="11e11-109">Windows 10, Version 1909, Windows Server, Version 1909: [KB4598298](https://support.microsoft.com/topic/january-21-2021-kb4598298-os-build-18363-1350-preview-02dfd9ba-91a2-1b82-dede-42f288c02511) oder höher</span><span class="sxs-lookup"><span data-stu-id="11e11-109">Windows 10 version 1909, Windows Server version 1909: [KB4598298](https://support.microsoft.com/topic/january-21-2021-kb4598298-os-build-18363-1350-preview-02dfd9ba-91a2-1b82-dede-42f288c02511) or later</span></span>
  - <span data-ttu-id="11e11-110">Windows 10, Version 1809, Windows Server, Version 1809 und Windows Server 2019: [KB4598296](https://support.microsoft.com/topic/january-21-2021-kb4598296-os-build-17763-1728-preview-4c0931ff-45b7-ff59-5e00-c03b5afb363d) oder höher</span><span class="sxs-lookup"><span data-stu-id="11e11-110">Windows 10 version 1809, Windows Server version 1809, and Windows Server 2019: [KB4598296](https://support.microsoft.com/topic/january-21-2021-kb4598296-os-build-17763-1728-preview-4c0931ff-45b7-ff59-5e00-c03b5afb363d) or later</span></span>
  - <span data-ttu-id="11e11-111">Windows 10, Version 1607, Windows Server 2016: [KB4601318](https://support.microsoft.com/topic/february-9-2021-kb4601318-os-build-14393-4225-c5e3de6c-e3e6-ffb5-6197-48b9ce16446e) oder höher</span><span class="sxs-lookup"><span data-stu-id="11e11-111">Windows 10, version 1607, Windows Server 2016: [KB4601318](https://support.microsoft.com/topic/february-9-2021-kb4601318-os-build-14393-4225-c5e3de6c-e3e6-ffb5-6197-48b9ce16446e) or later</span></span>
   - <span data-ttu-id="11e11-112">Windows 10-Erstversion (Juli 2015): [KB4601331](https://support.microsoft.com/office/february-9-2021%e2%80%94kb4601331-os-build-10240-18842-6227d078-fef3-8d67-27e0-1882e6cb79ff?ui=en-US&rs=en-US&ad=US) oder höher</span><span class="sxs-lookup"><span data-stu-id="11e11-112">Windows 10 initial version (July 2015): [KB4601331](https://support.microsoft.com/office/february-9-2021%e2%80%94kb4601331-os-build-10240-18842-6227d078-fef3-8d67-27e0-1882e6cb79ff?ui=en-US&rs=en-US&ad=US) or later</span></span>
  - <span data-ttu-id="11e11-113">Windows 8.1: [KB4601384](https://support.microsoft.com/topic/february-9-2021-kb4601384-monthly-rollup-16bdbb75-dd4b-2910-abc5-7891c9756b96) oder höher</span><span class="sxs-lookup"><span data-stu-id="11e11-113">Windows 8.1: [KB4601384](https://support.microsoft.com/topic/february-9-2021-kb4601384-monthly-rollup-16bdbb75-dd4b-2910-abc5-7891c9756b96) or later</span></span>
  - <span data-ttu-id="11e11-114">Windows Server 2012: [KB4601348](https://support.microsoft.com/topic/february-9-2021-kb4601348-monthly-rollup-2c338c0c-73d6-fb80-cc91-f1a86e80db0c) oder höher</span><span class="sxs-lookup"><span data-stu-id="11e11-114">Windows Server 2012: [KB4601348](https://support.microsoft.com/topic/february-9-2021-kb4601348-monthly-rollup-2c338c0c-73d6-fb80-cc91-f1a86e80db0c) or later</span></span>
  
- <span data-ttu-id="11e11-115">Microsoft Edge Stable Channel</span><span class="sxs-lookup"><span data-stu-id="11e11-115">Microsoft Edge Stable Channel</span></span>


## <a name="overview"></a><span data-ttu-id="11e11-116">Übersicht</span><span class="sxs-lookup"><span data-stu-id="11e11-116">Overview</span></span>

<span data-ttu-id="11e11-117">Organisationen, die Internet Explorer 11 (IE11) für Abwärtskompatibilität benötigen, bietet der Internet Explorer-Modus (IE-Modus) in Microsoft Edge eine nahtlose, für sich stehende Browserumgebung.</span><span class="sxs-lookup"><span data-stu-id="11e11-117">For organizations that require Internet Explorer 11 (IE11) for legacy compatibility, Internet Explorer mode (IE mode) on Microsoft Edge provides a seamless, single browser experience.</span></span> <span data-ttu-id="11e11-118">Benutzer können von Microsoft Edge aus auf ältere Anwendungen zugreifen, ohne zu IE11 zurückkehren zu müssen.</span><span class="sxs-lookup"><span data-stu-id="11e11-118">Users can access legacy applications from within Microsoft Edge without having to switch back to IE11.</span></span>

<span data-ttu-id="11e11-119">Nachdem Sie den IE-Modus konfiguriert haben, können Sie mithilfe von Gruppenrichtlinien IE11 als eigenständigen Browser in Ihrer Organisation deaktivieren, **ohne die Funktionalität des IE-Modus zu beeinträchtigen**.</span><span class="sxs-lookup"><span data-stu-id="11e11-119">After you configure IE mode, you can disable IE11 as a standalone browser **without affecting IE mode functionality** across your organization using group policy.</span></span>

> [!NOTE]
> <span data-ttu-id="11e11-120">Wenn Sie die eigenständige IE11-App für bestimmte Websites benötigen und der übrige Browsertraffic an Microsoft Edge weitergeleitet werden soll, können Sie die Richtlinie [Alle Websites, die nicht in der Websiteliste enthalten sind, an Microsoft Edge weiterleiten](https://docs.microsoft.com/deployedge/edge-ie-mode-policies#redirect-sites-from-ie-to-microsoft-edge) so konfigurieren, dass Websites von IE zu Microsoft Edge umgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="11e11-120">If you need the standalone IE11 app for specific sites, and want to redirect all other browser traffic to Microsoft Edge, you can configure the [Send all sites not included in the site list to Microsoft Edge](https://docs.microsoft.com/deployedge/edge-ie-mode-policies#redirect-sites-from-ie-to-microsoft-edge) policy to redirect sites from IE to Microsoft Edge.</span></span>

## <a name="user-experience-after-redirecting-traffic-to-microsoft-edge"></a><span data-ttu-id="11e11-121">Benutzererfahrung nach dem Umleiten von Traffic zu Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="11e11-121">User experience after redirecting traffic to Microsoft Edge</span></span>

<span data-ttu-id="11e11-122">Wenn Sie die Richtlinie **Internet Explorer 11 als eigenständigen Browser deaktivieren** aktivieren, werden alle IE11-Aktivitäten zu Microsoft Edge umgeleitet, und die Benutzererfahrung sieht folgendermaßen aus:</span><span class="sxs-lookup"><span data-stu-id="11e11-122">When you enable the **Disable Internet Explorer 11 as a standalone browser** policy, all IE11 activity is redirected to Microsoft Edge and users have the following experience:</span></span>

- <span data-ttu-id="11e11-123">Das IE11-Symbol wird aus dem Startmenü entfernt, bleibt auf der Taskleiste jedoch erhalten.</span><span class="sxs-lookup"><span data-stu-id="11e11-123">The IE11 icon on the Start Menu will be removed, but the one on the taskbar will remain.</span></span>
- <span data-ttu-id="11e11-124">Wenn Benutzer versuchen, Verknüpfungen oder Dateizuordnungen zu starten, die IE11 verwenden, werden sie umgeleitet, um dieselbe Datei/URL in Microsoft Edge zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="11e11-124">When users try to launch shortcuts or file associations that use IE11, they will be redirected to open the same file/URL in Microsoft Edge.</span></span>
- <span data-ttu-id="11e11-125">Wenn Benutzer versuchen, IE11 zu starten, indem sie die iexplore.exe-Binärdatei direkt aufrufen, wird stattdessen Microsoft Edge gestartet.</span><span class="sxs-lookup"><span data-stu-id="11e11-125">When users try to launch IE11 by directly invoking the iexplore.exe binary, Microsoft Edge will launch instead.</span></span>

<span data-ttu-id="11e11-126">Während des Festlegens der Richtlinie für diese Benutzererfahrung können Sie optional eine Umleitungsnachricht für jeden Benutzer anzeigen lassen, der versucht, IE11 zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="11e11-126">As part of setting the policy for this experience, you can optionally show a redirect message for each user who tries to launch IE11.</span></span> <span data-ttu-id="11e11-127">Für diese Meldung können Sie auswählen, ob sie "Immer" oder "Einmal pro Benutzer" angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="11e11-127">This message can be set to display "Always" or "Once per user".</span></span> <span data-ttu-id="11e11-128">Die im nächsten Screenshot dargestellte Umleitungsnachricht wird standardmäßig nie angezeigt.</span><span class="sxs-lookup"><span data-stu-id="11e11-128">By default, the redirect message shown in the next screenshot is never shown.</span></span>

:::image type="content" source="media/edge-ie-disable-ie11/disable-ie-redirect-msg.png" alt-text="Warnung beim Versuch, IE zu öffnen, wenn die Umleitung zu Microsoft Edge aktiv ist.":::

<span data-ttu-id="11e11-130">Wenn Ihre Websiteliste für den Unternehmensmodus Anwendungen enthält, die für das Öffnen in der IE11-App konfiguriert sind und Sie IE11 mit dieser Richtlinie deaktivieren, werden die Anwendungen in Microsoft Edge im IE-Modus geöffnet.</span><span class="sxs-lookup"><span data-stu-id="11e11-130">If your Enterprise Mode Site List contains applications that are configured to open in the IE11 app and you disable IE11 with this policy, they will open in IE mode on Microsoft Edge.</span></span>
> [!NOTE]
> <span data-ttu-id="11e11-131">Es gibt ein bekanntes Problem mit dem Benutzerablauf, das auftritt, wenn eine Website für das Öffnen in IE11 konfiguriert ist und die Richtlinie zum Deaktivieren von IE11 aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="11e11-131">There is a known issue with the user flow when a site is configured to open in IE11 and the disable IE11 policy is set.</span></span> <span data-ttu-id="11e11-132">Das Problem wird derzeit untersucht.</span><span class="sxs-lookup"><span data-stu-id="11e11-132">The issue being actively investigated.</span></span>

## <a name="disable-internet-explorer-11-as-a-standalone-browser"></a><span data-ttu-id="11e11-133">Deaktivieren von Internet Explorer 11 als eigenständiger Browser</span><span class="sxs-lookup"><span data-stu-id="11e11-133">Disable Internet Explorer 11 as a standalone browser</span></span>

<span data-ttu-id="11e11-134">Führen Sie die folgenden Schritte aus, um Internet Explorer 11 mithilfe von Gruppenrichtlinien zu deaktivieren:</span><span class="sxs-lookup"><span data-stu-id="11e11-134">To disable Internet Explorer 11 using group policy, follow these steps:</span></span>

1. <span data-ttu-id="11e11-135">Laden Sie die neueste [Microsoft Edge-Richtlinienvorlage ](https://www.microsoft.com/en-us/business/download)herunter, und installieren Sie sie.</span><span class="sxs-lookup"><span data-stu-id="11e11-135">Download and install the latest [Microsoft Edge Policy Template](https://www.microsoft.com/en-us/business/download).</span></span>
2. <span data-ttu-id="11e11-136">Öffnen Sie den Gruppenrichtlinien-Editor.</span><span class="sxs-lookup"><span data-stu-id="11e11-136">Open the Group Policy Editor.</span></span>
3. <span data-ttu-id="11e11-137">Wechseln Sie zu ***Computerkonfiguration/Administrative Vorlagen/Windows-Komponenten/Internet Explorer***.</span><span class="sxs-lookup"><span data-stu-id="11e11-137">Go to ***Computer Configuration/Administrative Templates/Windows Components/Internet Explorer***.</span></span> 
4. <span data-ttu-id="11e11-138">Doppelklicken Sie auf  \*\* Internet Explorer 11 als eigenständigen Browser deaktivieren\*\*.</span><span class="sxs-lookup"><span data-stu-id="11e11-138">Double-click **Disable Internet Explorer 11 as a standalone browser**.</span></span>
5. <span data-ttu-id="11e11-139">Wählen Sie  **Aktiviert** aus.</span><span class="sxs-lookup"><span data-stu-id="11e11-139">Select **Enabled**.</span></span>
6. <span data-ttu-id="11e11-140">Wählen Sie unter  **Optionen** einen der folgenden Einträge aus:</span><span class="sxs-lookup"><span data-stu-id="11e11-140">Under **Options**, pick one of the following values:</span></span>

   - <span data-ttu-id="11e11-141">**Nie** , wenn Benutzer nicht darüber benachrichtigt werden sollen, dass IE11 deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="11e11-141">**Never** if you don’t want to notify users that IE11 is disabled.</span></span>
   - <span data-ttu-id="11e11-142">**Immer** , wenn Benutzer jedes Mal benachrichtigt werden sollen, wenn sie von IE11 umgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="11e11-142">**Always** if you want to notify users every time they're redirected from IE11.</span></span>
   - <span data-ttu-id="11e11-143">**Einmal pro Benutzer**  , wenn Benutzer nur beim ersten Umleiten benachrichtigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="11e11-143">**Once per user** if you want to notify users only the first time they are redirected.</span></span>

7. <span data-ttu-id="11e11-144">Klicken Sie auf  **OK**  oder  **Übernehmen** , um diese Richtlinieneinstellung zu speichern.</span><span class="sxs-lookup"><span data-stu-id="11e11-144">Click **OK** or **Apply** to save this policy setting.</span></span>

## <a name="see-also"></a><span data-ttu-id="11e11-145">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="11e11-145">See also</span></span>

- [<span data-ttu-id="11e11-146">Microsoft Edge Enterprise-Angebotsseite</span><span class="sxs-lookup"><span data-stu-id="11e11-146">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="11e11-147">Informationen zum IE-Modus</span><span class="sxs-lookup"><span data-stu-id="11e11-147">About IE mode</span></span>](https://docs.microsoft.com/deployedge/edge-ie-mode)
- [<span data-ttu-id="11e11-148">Weitere Informationen zum Unternehmensmodus</span><span class="sxs-lookup"><span data-stu-id="11e11-148">Additional Enterprise Mode information</span></span>](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
