---
title: Zugreifen auf die alte Version von Microsoft Edge
ms.author: jtkim
author: dan-wesley
manager: srugh
ms.date: 08/17/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Informationen für den Zugriff auf die alte Version von Microsoft Edge
ms.openlocfilehash: e5a97a487dc6b3a45504a721e460a69103b0174e
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/31/2020
ms.locfileid: "10980023"
---
# <span data-ttu-id="6ca22-103">Zugreifen auf Microsoft Edge Legacy nach der Installation der neuen Version von Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="6ca22-103">Access Microsoft Edge Legacy after installing the new version of Microsoft Edge</span></span>

<span data-ttu-id="6ca22-104">Informationen für den Zugriff auf Microsoft Edge Legacy nach der Installation der neuen Version von Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="6ca22-104">Learn how to access Microsoft Edge Legacy after installing the new version of Microsoft Edge.</span></span>

> [!NOTE]
> <span data-ttu-id="6ca22-105">Dieser Artikel bezieht sich auf den Microsoft Edge [Stable-Kanal](microsoft-edge-channels.md).</span><span class="sxs-lookup"><span data-stu-id="6ca22-105">This article applies to the Microsoft Edge [Stable channel](microsoft-edge-channels.md).</span></span>

<span data-ttu-id="6ca22-106">Die meisten Organisationen möchten Microsoft Edge Legacy sicherlich durch die neue Version ersetzen, es gibt aber einige Situationen, in denen Benutzer auf beide Versionen zugreifen müssen.</span><span class="sxs-lookup"><span data-stu-id="6ca22-106">While most organizations will want to replace Microsoft Edge Legacy with the new version, there are some situations where users will need access to both versions.</span></span> <span data-ttu-id="6ca22-107">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="6ca22-107">For example:</span></span>

- <span data-ttu-id="6ca22-108">Helpdesk- und Supportmitarbeiter, die mit Benutzern interagieren, die eine oder beide Versionen von Microsoft Edge verwenden.</span><span class="sxs-lookup"><span data-stu-id="6ca22-108">Helpdesk and support staff who interact with users who are using either or both versions of Microsoft Edge.</span></span>
- <span data-ttu-id="6ca22-109">Entwickler, die Support für Kunden bereitstellen, die eine oder beide Versionen von Microsoft Edge verwenden.</span><span class="sxs-lookup"><span data-stu-id="6ca22-109">Developers who support customers who are using either or both versions of Microsoft Edge.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6ca22-110">Die parallele Ausführung von der Vorgängerversion (Microsoft Edge Legacy) sowie der neuen Version von Microsoft Edge wird für den Einsatz in der Produktion nicht empfohlen.</span><span class="sxs-lookup"><span data-stu-id="6ca22-110">Running Microsoft Edge Legacy side-by-side with the new version of Microsoft Edge is not recommended for use in production.</span></span> <span data-ttu-id="6ca22-111">Diese Konfiguration sollte nur in bestimmten Fällen verwendet werden, in denen Tests mit beiden Browserversionen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="6ca22-111">This configuration should only be used in specific cases where testing with both browser versions is required.</span></span>
>
> <span data-ttu-id="6ca22-112">Der Support für die Desktop-App von Microsoft Edge Legacy läuft am 9. März 2021 zugunsten des neuen Microsoft Edge aus.</span><span class="sxs-lookup"><span data-stu-id="6ca22-112">The Microsoft Edge Legacy desktop app will reach end of support on March 9, 2021 in favor of the new Microsoft Edge.</span></span> <span data-ttu-id="6ca22-113">Dies bedeutet, dass Microsoft Edge Legacy nach diesem Datum keine Sicherheitsupdates mehr erhält.</span><span class="sxs-lookup"><span data-stu-id="6ca22-113">This means that Microsoft Edge Legacy will not receive security updates after that date.</span></span> <span data-ttu-id="6ca22-114">Diese Änderung gilt für alle Funktionen der Desktop-App von Microsoft Edge Legacy.</span><span class="sxs-lookup"><span data-stu-id="6ca22-114">This change is applicable to all experiences that run in the Microsoft Edge Legacy desktop app.</span></span> <span data-ttu-id="6ca22-115">[Weitere Informationen](https://techcommunity.microsoft.com/t5/microsoft-365-blog/microsoft-365-apps-say-farewell-to-internet-explorer-11-and/ba-p/1591666).</span><span class="sxs-lookup"><span data-stu-id="6ca22-115">[Learn more](https://techcommunity.microsoft.com/t5/microsoft-365-blog/microsoft-365-apps-say-farewell-to-internet-explorer-11-and/ba-p/1591666).</span></span>

## <span data-ttu-id="6ca22-116">Vorbemerkungen</span><span class="sxs-lookup"><span data-stu-id="6ca22-116">Before you begin</span></span>

<span data-ttu-id="6ca22-117">Die Verfahren in diesem Artikel gelten für Systeme, die mit den neuesten Sicherheitsupdates aktualisiert wurden.</span><span class="sxs-lookup"><span data-stu-id="6ca22-117">The procedures in this article apply to systems that have been updated with the latest security updates.</span></span> <span data-ttu-id="6ca22-118">Wenn die neue Version von Microsoft Edge installiert ist, wird die alte Version (Microsoft Edge Legacy) ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="6ca22-118">When the new version of Microsoft Edge is installed, the old version (Microsoft Edge Legacy) will be hidden.</span></span> <span data-ttu-id="6ca22-119">Bei allen Versuchen, die alte Version von Microsoft Edge zu starten, wird der Benutzer standardmäßig auf die neu installierte Version von Microsoft Edge umgeleitet.</span><span class="sxs-lookup"><span data-stu-id="6ca22-119">By default, all attempts to launch the old version will redirect the user to the newly installed version of Microsoft Edge.</span></span> <span data-ttu-id="6ca22-120">In diesem Artikel wird beschrieben, wie Sie Microsoft Edge Legacy nach der Installation von Microsoft Edge weiterhin verwenden können.</span><span class="sxs-lookup"><span data-stu-id="6ca22-120">This article describes how you can keep using Microsoft Edge Legacy after you install Microsoft Edge.</span></span>

## <span data-ttu-id="6ca22-121">Schnellstart: Parallele Verwendung von Microsoft Edge Beta Channel und Microsoft Edge Legacy</span><span class="sxs-lookup"><span data-stu-id="6ca22-121">Quickstart: Side-by-side experience with Microsoft Edge Beta Channel and Microsoft Edge Legacy</span></span>

<span data-ttu-id="6ca22-122">Bevor Sie die ausführlichen Anweisungen in diesem Artikel verwenden, sollten Sie die folgenden zwei Schritte beachten, damit Ihre Benutzer Microsoft Edge Legacy und Microsoft Edge [Beta Channel](microsoft-edge-channels.md) parallel ausführen können.</span><span class="sxs-lookup"><span data-stu-id="6ca22-122">Before using the detailed instructions in this article, consider the following two steps to let your users run Microsoft Edge Legacy and the Microsoft Edge [Beta channel](microsoft-edge-channels.md) side-by-side.</span></span>

1. <span data-ttu-id="6ca22-123">Verhindern Sie die automatische Installation des Stable-Kanals von Microsoft Edge durch [Windows Update](https://support.microsoft.com/help/12373/windows-update-faq).</span><span class="sxs-lookup"><span data-stu-id="6ca22-123">Prevent the automatic install of the Stable Channel of Microsoft Edge by [Windows Update](https://support.microsoft.com/help/12373/windows-update-faq).</span></span>

   > [!TIP]
   > <span data-ttu-id="6ca22-124">Verwenden Sie das [Blocker-Toolkit](microsoft-edge-blocker-toolkit.md) zum Deaktivieren der automatischen Bereitstellung von Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="6ca22-124">Use the [Blocker Toolkit](microsoft-edge-blocker-toolkit.md) to disable automatic delivery of Microsoft Edge.</span></span>

2. <span data-ttu-id="6ca22-125">Installieren Sie den [Beta-Kanal](https://www.microsoft.com/edge/business/download) der neuen Version von Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="6ca22-125">Install the [Beta channel](https://www.microsoft.com/edge/business/download) of the new version of Microsoft Edge.</span></span>

   > [!NOTE]
   > <span data-ttu-id="6ca22-126">Lesen Sie [Weitere Informationen](#additional-information) zu den Registrierungsschlüsseleinstellungen.</span><span class="sxs-lookup"><span data-stu-id="6ca22-126">Read [Additional information](#additional-information) for information about Registry Key settings.</span></span>

<span data-ttu-id="6ca22-127">Diese parallele Lösung ist weniger komplex und erfordert weniger Verwaltungsaufwand als die in diesem Artikel beschriebene detaillierte Lösung.</span><span class="sxs-lookup"><span data-stu-id="6ca22-127">This side-by-side solution is less complex and requires less management than the detailed solution described in this article.</span></span> <span data-ttu-id="6ca22-128">Diese Lösung bedeutet jedoch, dass Sie den Beta-Kanal anstelle des Stable-Kanals ausführen müssen.</span><span class="sxs-lookup"><span data-stu-id="6ca22-128">However, this solution does mean that you'll be running the Beta Channel rather than the Stable Channel.</span></span>

## <span data-ttu-id="6ca22-129">Parallele Verwendung von Microsoft Edge Stable Channel und Microsoft Edge Legacy</span><span class="sxs-lookup"><span data-stu-id="6ca22-129">Side-by-side experience with Microsoft Edge Stable Channel and Microsoft Edge Legacy</span></span>

<span data-ttu-id="6ca22-130">Wenn Sie den stabilen Kanal der nächsten Version von Microsoft Edge auf Systemebene installieren, wird die aktuelle Version (Microsoft Edge Legacy) ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="6ca22-130">Installing the Stable Channel of the next version of Microsoft Edge at the system-level will cause the current version (Microsoft Edge Legacy) to be hidden.</span></span> <span data-ttu-id="6ca22-131">Wenn Sie Benutzern die parallele Verwendung beider Versionen von Microsoft Edge in Windows ermöglichen möchten, können Sie diese Oberfläche aktivieren, indem Sie die Gruppenrichtlinie **Microsoft Edge-Browser im Parallelbetrieb zulassen** auf **Aktiviert** festlegen.</span><span class="sxs-lookup"><span data-stu-id="6ca22-131">If you want to let your users see both versions of Microsoft Edge side by side in Windows, you can enable this experience by setting the **Allow Microsoft Edge Side by Side browser experience** group policy to **Enabled**.</span></span>

<span data-ttu-id="6ca22-132">Diese Gruppenrichtlinie ist [hier](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#allowsxs) dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="6ca22-132">This group policy is documented [here](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#allowsxs)</span></span>

### <span data-ttu-id="6ca22-133">So richten Sie die Richtlinie für den Parallelbetrieb des Browsers ein:</span><span class="sxs-lookup"><span data-stu-id="6ca22-133">To set up the side-by-side browser experience policy:</span></span>

1. <span data-ttu-id="6ca22-134">Installieren Sie die Richtliniendefinitionen über [Microsoft Edge for Business](https://www.microsoft.com/edge/business/download).</span><span class="sxs-lookup"><span data-stu-id="6ca22-134">Install the Policy Definitions from [Microsoft Edge for Business](https://www.microsoft.com/edge/business/download).</span></span>

   - <span data-ttu-id="6ca22-135">Wählen Sie KANAL/BUILD und PLATTFORM aus, die Sie verwenden möchten, und klicken Sie dann auf RICHTLINIENDATEIEN ABRUFEN.</span><span class="sxs-lookup"><span data-stu-id="6ca22-135">Pick the CHANNEL/BUILD and PLATFORM you want to use, and then click GET POLICY FILES.</span></span>
   - <span data-ttu-id="6ca22-136">Extrahieren Sie die gezippten Dateien.</span><span class="sxs-lookup"><span data-stu-id="6ca22-136">Extract the zipped files.</span></span>
   - <span data-ttu-id="6ca22-137">Kopieren sie msedge.admx und msedgeupdate.admx in das Verzeichnis `C:\Windows\PolicyDefinitions`.</span><span class="sxs-lookup"><span data-stu-id="6ca22-137">Copy msedge.admx and msedgeupdate.admx to the `C:\Windows\PolicyDefinitions` directory.</span></span>
   - <span data-ttu-id="6ca22-138">Kopieren Sie "msedge.adml" und "msedgeupdate.adml" (aus dem entsprechenden Verzeichnis der Sprache bzw. des Gebietsschemas) in das `C:\Windows\PolicyDefinitions\[APPROPRIATE LANGUAGE/LOCALE]`-Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="6ca22-138">Copy msedge.adml and msedgeupdate.adml (from the appropriate language/locale directory) to the `C:\Windows\PolicyDefinitions\[APPROPRIATE LANGUAGE/LOCALE]` directory.</span></span>

2. <span data-ttu-id="6ca22-139">Öffnen Sie den Gruppenrichtlinien-Editor (gpedit.msc).</span><span class="sxs-lookup"><span data-stu-id="6ca22-139">Open the Group Policy Editor (gpedit.msc).</span></span>
3. <span data-ttu-id="6ca22-140">Wechseln Sie unter **Computerkonfiguration** zu *Administrative Vorlagen>Microsoft Edge Update>Anwendungen*.</span><span class="sxs-lookup"><span data-stu-id="6ca22-140">Under **Computer Configuration**, go to *Administrative Templates>Microsoft Edge Update>Applications*.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6ca22-141">Wenn der Ordner *Microsoft Edge Update* nicht angezeigt wird, überprüfen Sie, ob Schritt 1 ordnungsgemäß abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="6ca22-141">If you don't see the *Microsoft Edge Update* folder, verify that step 1 was completed correctly.</span></span>

4. <span data-ttu-id="6ca22-142">Doppelklicken Sie unter **Anwendungen** auf „Microsoft Edge-Browser im Parallelbetrieb zulassen”.</span><span class="sxs-lookup"><span data-stu-id="6ca22-142">Under **Applications**, double-click "Allow Microsoft Edge Side by Side browser experience".</span></span> <span data-ttu-id="6ca22-143">Lesen Sie unsere [Leitlinien für bewährte Methoden](#best-practice-guidance), bevor Sie mit dem nächsten Schrittfortfahren.</span><span class="sxs-lookup"><span data-stu-id="6ca22-143">See our [best practice guidance](#best-practice-guidance) before continuing to the next step.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6ca22-144">Diese Gruppenrichtlinie ist standardmäßig auf „Nicht konfiguriert” festgelegt, was bewirkt, dass Microsoft Edge Legacy nach der Installation der neuen Version von Microsoft Edge ausgeblendet wird.</span><span class="sxs-lookup"><span data-stu-id="6ca22-144">By default, this group policy is set to "Not configured", which results in Microsoft Edge Legacy being hidden when the new version of Microsoft Edge is installed.</span></span>

5. <span data-ttu-id="6ca22-145">Wählen Sie **Aktiviert**, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="6ca22-145">Select **Enabled** and then click **OK**.</span></span>  

<span data-ttu-id="6ca22-146">Durch das Festlegen dieser Richtlinie erhält der folgende Registrierungsschlüssel den Wert "00000001":</span><span class="sxs-lookup"><span data-stu-id="6ca22-146">Setting this policy will set the following Registry Key  to '00000001':</span></span>

- <span data-ttu-id="6ca22-147">Legende:</span><span class="sxs-lookup"><span data-stu-id="6ca22-147">Key:</span></span> `Computer\HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate`
- <span data-ttu-id="6ca22-148">Name des Wertes:</span><span class="sxs-lookup"><span data-stu-id="6ca22-148">Value Name:</span></span> `Allowsxs`
- <span data-ttu-id="6ca22-149">Werttyp:</span><span class="sxs-lookup"><span data-stu-id="6ca22-149">Value Type:</span></span> `'REG_DWORD'`

#### <span data-ttu-id="6ca22-150">Leitlinien für bewährte Methoden</span><span class="sxs-lookup"><span data-stu-id="6ca22-150">Best practice guidance</span></span>

<span data-ttu-id="6ca22-151">Für die bestmögliche Benutzerfreundlichkeit sollte die Option **Microsoft Edge-Browser im Parallelbetrieb zulassen** aktiviert werden, bevor die neue Version von Microsoft Edge auf den Geräten der Benutzer bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="6ca22-151">For the best experience, the **Allow Microsoft Edge Side by Side browser experience** should be enabled before the new version of Microsoft Edge is deployed to your users' devices.</span></span>

<span data-ttu-id="6ca22-152">Wenn die Gruppenrichtlinie aktiviert ist, nachdem Microsoft Edge bereitgestellt wurde, sind die folgenden Nebenwirkungen und erforderliche Aktionen zu beachten:</span><span class="sxs-lookup"><span data-stu-id="6ca22-152">If the group policy is enabled after Microsoft Edge is deployed, there are the following side effects and required actions:</span></span>

1. <span data-ttu-id="6ca22-153">**Microsoft Edge-Browser im Parallelbetrieb zulassen** wird erst wirksam, nachdem das Installationsprogramm für die neue Version von Microsoft Edge erneut ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="6ca22-153">**Allow Microsoft Edge Side by Side browser experience** won't take effect until after the installer for the new version of Microsoft Edge is run again.</span></span>

   > [!NOTE]
   > <span data-ttu-id="6ca22-154">Das Installationsprogramm kann direkt oder automatisch ausgeführt werden, wenn die neue Version von Microsoft Edge aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="6ca22-154">The installer can be run directly or automatically when the new version of Microsoft Edge updates.</span></span>

2. <span data-ttu-id="6ca22-155">Microsoft Edge Legacy muss erneut an "Start" oder die Taskleiste angeheftet werden, da die Anheftung migriert wird, wenn die neue Version von Microsoft Edge bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="6ca22-155">Microsoft Edge Legacy will need to be re-pinned to Start or the Taskbar because the pin is migrated when the new version of Microsoft Edge is deployed.</span></span>
3. <span data-ttu-id="6ca22-156">Sites, die an "Start" oder die Taskleiste für Microsoft Edge Legacy angeheftet waren, werden auf die neue Version von Microsoft Edge migriert.</span><span class="sxs-lookup"><span data-stu-id="6ca22-156">Sites that were pinned to Start or the Taskbar for Microsoft Edge Legacy will be migrated to the new version of Microsoft Edge.</span></span>

## <span data-ttu-id="6ca22-157">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6ca22-157">Additional information</span></span>

<span data-ttu-id="6ca22-158">Nachdem die Systeme vollständig aktualisiert sind und der Stable-Kanal der nächsten Version von Microsoft Edge installiert ist, werden der folgende Registrierungsschlüssel und -wert festgelegt:</span><span class="sxs-lookup"><span data-stu-id="6ca22-158">After the systems are fully updated and the Stable channel of the next version of Microsoft Edge is installed, the following registry key and value is set:</span></span>

- <span data-ttu-id="6ca22-159">Legende:</span><span class="sxs-lookup"><span data-stu-id="6ca22-159">Key:</span></span> `Computer\HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\EdgeUpdate\ClientState\{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}`
- <span data-ttu-id="6ca22-160">Schlüsselwert:</span><span class="sxs-lookup"><span data-stu-id="6ca22-160">Key value:</span></span> `BrowserReplacement`

  > [!IMPORTANT]
  > <span data-ttu-id="6ca22-161">Dieser Schlüssel wird bei jeder Aktualisierung des Microsoft Edge Stable-Kanals überschrieben.</span><span class="sxs-lookup"><span data-stu-id="6ca22-161">This key is over-written every time the Microsoft Edge Stable channel is updated.</span></span> <span data-ttu-id="6ca22-162">Als bewährte Methode wird empfohlen, diesen Schlüssel NICHT zu löschen, damit Benutzer auf beide Versionen von Microsoft Edge zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="6ca22-162">As a best practice, we recommend that you DO NOT delete this key to allow users to access both versions of Microsoft Edge.</span></span>

## <span data-ttu-id="6ca22-163">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6ca22-163">See also</span></span>

- [<span data-ttu-id="6ca22-164">Microsoft Edge Enterprise-Angebotsseite</span><span class="sxs-lookup"><span data-stu-id="6ca22-164">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="6ca22-165">Windows-Updates zur Unterstützung von Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="6ca22-165">Windows updates to support Microsoft Edge</span></span>](microsoft-edge-sysupdate-windows-updates.md)
