---
title: Microsoft Edge in Ihrer Umgebung
ms.author: ryhecht
author: RyanHechtMSFT
manager: tinad
ms.date: 02/05/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Edge in Ihrer Umgebung
ms.openlocfilehash: e1418d21ff9e541d83d5b86baf5ff25c50d2299d
ms.sourcegitcommit: 16a92a51560fdba6f6480e4533453348f026c7ef
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "11313936"
---
# <span data-ttu-id="56016-103">Microsoft Edge in Ihrer Umgebung</span><span class="sxs-lookup"><span data-stu-id="56016-103">Microsoft Edge in your environment</span></span>

<span data-ttu-id="56016-104">In diesem Artikel wird beschrieben, wie Sie die Bereitstellung von Microsoft Edge vorbereiten, wenn die Vorgängerversion von Microsoft Edge das Serviceende erreicht.</span><span class="sxs-lookup"><span data-stu-id="56016-104">This article describes how to prepare to deploy Microsoft Edge when Microsoft Edge Legacy reaches its end of service.</span></span>

<span data-ttu-id="56016-105">Wie im [Blogbeitrag](https://aka.ms/EdgeLegacyEOS) des Microsoft Edge-Produktteams angegeben, endet der Support für die Desktopanwendung der Vorgängerversion von Microsoft Edge am 9.März 2021.</span><span class="sxs-lookup"><span data-stu-id="56016-105">As per the Microsoft Edge Product Team’s [blog post](https://aka.ms/EdgeLegacyEOS), support for the Microsoft Edge Legacy desktop application will end on March 9, 2021.</span></span> <span data-ttu-id="56016-106">Wenn Sie die Version „Update Tuesday“ (oder „B“) im April installieren, wird die Vorgängerversion von Microsoft Edge von Geräten mit Windows 10 RS4 bis 20H1 entfernt und durch Microsoft Edge ersetzt.</span><span class="sxs-lookup"><span data-stu-id="56016-106">When you apply the Update Tuesday (or "B") release in April, it will remove Microsoft Edge Legacy from devices running Windows 10 RS4 through 20H1 and replace it with Microsoft Edge.</span></span>

## <span data-ttu-id="56016-107">Vorbereitungen</span><span class="sxs-lookup"><span data-stu-id="56016-107">How to Prepare</span></span>

<span data-ttu-id="56016-108">Zur Vorbereitung auf die Installation von Microsoft Edge auf Windows 10 RS4- bis 20H1-Geräten mit dem Update Tuesday-Release im April empfehlen wir, den Artikel [Planen der Bereitstellung von Microsoft Edge](deploy-edge-plan-deployment.md) zu lesen.</span><span class="sxs-lookup"><span data-stu-id="56016-108">To prepare for Microsoft Edge being installed on Windows 10 RS4 through 20H1 devices with the Update Tuesday release in April, we recommend reading [Plan your deployment of Microsoft Edge](deploy-edge-plan-deployment.md).</span></span>

<span data-ttu-id="56016-109">Nachdem Sie die Bereitstellung geplant haben, verwenden Sie einen der folgenden Ansätze, um die Bereitstellung von Microsoft Edge vorzubereiten.</span><span class="sxs-lookup"><span data-stu-id="56016-109">After you plan your deployment, use one of the following approaches to prepare to deploy Microsoft Edge.</span></span>

- <span data-ttu-id="56016-110">**Installieren Sie Gruppenrichtlinien, um Ihren Microsoft Edge-Aktualisierungsansatz anzupassen**.</span><span class="sxs-lookup"><span data-stu-id="56016-110">**Install group policies to customize your Microsoft Edge update approach**.</span></span> <span data-ttu-id="56016-111">Weitere Informationen finden Sie unter [Konfigurieren von Microsoft Edge-Richtlinieneinstellungen unter Windows](configure-microsoft-edge.md). Achten Sie dabei besonders auf das [Referenzmaterial zu Updaterichtlinien](microsoft-edge-update-policies.md).</span><span class="sxs-lookup"><span data-stu-id="56016-111">For more information, see [Configure Microsoft Edge policy settings on Windows](configure-microsoft-edge.md), and pay special attention to the [Update Policy reference](microsoft-edge-update-policies.md) material.</span></span> <span data-ttu-id="56016-112">Wenn Sie Gruppenrichtlinien installieren, um Ihre Updates zu verwalten, bevor Sie das Update Tuesday-Release vom April installieren, beginnt Microsoft Edge sofort damit, Ihre Richtlinie anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="56016-112">If you install group policies to manage your updates before installing April’s Update Tuesday release, Microsoft Edge will immediately start respecting your policy.</span></span> <span data-ttu-id="56016-113">Wenn keine Gruppenrichtlinie installiert ist, wird Microsoft Edge automatisch aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="56016-113">If there isn't any installed group policy, Microsoft Edge will automatically update itself.</span></span>

- <span data-ttu-id="56016-114">**Entfernen Sie die Desktopanwendung der Vorgängerversion von Microsoft Edge vor dem Serviceende am 9.März 2021, und stellen Sie Microsoft Edge bereit**.</span><span class="sxs-lookup"><span data-stu-id="56016-114">**Remove the Microsoft Edge Legacy desktop application before its end of service date of March 9, 2021 and deploy Microsoft Edge**.</span></span> <span data-ttu-id="56016-115">Für Windows 10 RS4 bis 20H1 können Sie dies mithilfe von Windows Updates tun.</span><span class="sxs-lookup"><span data-stu-id="56016-115">For Windows 10 RS4 through 20H1, you can do this by using Windows Updates.</span></span> <span data-ttu-id="56016-116">Weitere Informationen finden Sie unter [Bereitstellen von Microsoft Edge mit Windows 10-Updates](deploy-edge-with-windows-10-updates.md).</span><span class="sxs-lookup"><span data-stu-id="56016-116">For more information, see [Deploy Microsoft Edge with Windows 10 updates](deploy-edge-with-windows-10-updates.md).</span></span>

## <span data-ttu-id="56016-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="56016-117">See also</span></span>

- [<span data-ttu-id="56016-118">Microsoft Edge Enterprise-Angebotsseite</span><span class="sxs-lookup"><span data-stu-id="56016-118">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="56016-119">Planen Ihrer Bereitstellung von Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="56016-119">Plan your deployment of Microsoft Edge</span></span>](deploy-edge-plan-deployment.md)