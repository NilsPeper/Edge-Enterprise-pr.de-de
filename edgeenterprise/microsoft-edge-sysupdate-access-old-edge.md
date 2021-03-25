---
title: Zugreifen auf die alte Version von Microsoft Edge
ms.author: jtkim
author: dan-wesley
manager: srugh
ms.date: 02/05/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Informationen für den Zugriff auf die alte Version von Microsoft Edge
ms.openlocfilehash: b521ab9ea093b62db7268e6bf2f4d656b3dc8d4b
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/24/2021
ms.locfileid: "11447089"
---
# <a name="access-microsoft-edge-legacy-after-installing-the-new-version-of-microsoft-edge"></a><span data-ttu-id="e9587-103">Zugreifen auf Microsoft Edge Legacy nach der Installation der neuen Version von Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="e9587-103">Access Microsoft Edge Legacy after installing the new version of Microsoft Edge</span></span>

<span data-ttu-id="e9587-104">Die Vorgängerversion von Microsoft Edge erhält ab dem 9.März2021 keine Sicherheitsupdates mehr.</span><span class="sxs-lookup"><span data-stu-id="e9587-104">Microsoft Edge Legacy will stop receiving security updates on March 9, 2021.</span></span> <span data-ttu-id="e9587-105">Sie können bis zum 13.April auf die Vorgängerversion von Microsoft Edge zugreifen.</span><span class="sxs-lookup"><span data-stu-id="e9587-105">You can access Microsoft Edge Legacy until April 13.</span></span> <span data-ttu-id="e9587-106">Weitere Informationen finden Sie im [Blogbeitrag](https://aka.ms/EdgeLegacyEOS) des Microsoft Edge-Produktteams.</span><span class="sxs-lookup"><span data-stu-id="e9587-106">For more information, see Microsoft Edge Product Team’s [blog post](https://aka.ms/EdgeLegacyEOS).</span></span>

> [!NOTE]
> <span data-ttu-id="e9587-107">Dieser Artikel bezieht sich auf den Microsoft Edge [Stable-Kanal](microsoft-edge-channels.md).</span><span class="sxs-lookup"><span data-stu-id="e9587-107">This article applies to the Microsoft Edge [Stable channel](microsoft-edge-channels.md).</span></span>

<span data-ttu-id="e9587-108">Die meisten Organisationen möchten Microsoft Edge Legacy sicherlich durch die neue Version ersetzen, es gibt aber einige Situationen, in denen Benutzer auf beide Versionen zugreifen müssen.</span><span class="sxs-lookup"><span data-stu-id="e9587-108">While most organizations will want to replace Microsoft Edge Legacy with the new version, there are some situations where users will need access to both versions.</span></span> <span data-ttu-id="e9587-109">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="e9587-109">For example:</span></span>

- <span data-ttu-id="e9587-110">Helpdesk- und Supportmitarbeiter, die mit Benutzern interagieren, die eine oder beide Versionen von Microsoft Edge verwenden.</span><span class="sxs-lookup"><span data-stu-id="e9587-110">Helpdesk and support staff who interact with users who are using either or both versions of Microsoft Edge.</span></span>
- <span data-ttu-id="e9587-111">Entwickler, die Support für Kunden bereitstellen, die eine oder beide Versionen von Microsoft Edge verwenden.</span><span class="sxs-lookup"><span data-stu-id="e9587-111">Developers who support customers who are using either or both versions of Microsoft Edge.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e9587-112">Die parallele Ausführung von der Vorgängerversion (Microsoft Edge Legacy) sowie der neuen Version von Microsoft Edge wird für den Einsatz in der Produktion nicht empfohlen.</span><span class="sxs-lookup"><span data-stu-id="e9587-112">Running Microsoft Edge Legacy side-by-side with the new version of Microsoft Edge is not recommended for use in production.</span></span> <span data-ttu-id="e9587-113">Diese Konfiguration sollte nur in bestimmten Fällen verwendet werden, in denen Tests mit beiden Browserversionen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="e9587-113">This configuration should only be used in specific cases where testing with both browser versions is required.</span></span>
>
> <span data-ttu-id="e9587-114">Der Support für die Desktop-App von Microsoft Edge Legacy läuft am 9. März 2021 zugunsten des neuen Microsoft Edge aus.</span><span class="sxs-lookup"><span data-stu-id="e9587-114">The Microsoft Edge Legacy desktop app will reach end of support on March 9, 2021 in favor of the new Microsoft Edge.</span></span> <span data-ttu-id="e9587-115">Dies bedeutet, dass Microsoft Edge Legacy nach diesem Datum keine Sicherheitsupdates mehr erhält.</span><span class="sxs-lookup"><span data-stu-id="e9587-115">This means that Microsoft Edge Legacy will not receive security updates after that date.</span></span> <span data-ttu-id="e9587-116">Diese Änderung gilt für alle Funktionen der Desktop-App von Microsoft Edge Legacy.</span><span class="sxs-lookup"><span data-stu-id="e9587-116">This change is applicable to all experiences that run in the Microsoft Edge Legacy desktop app.</span></span> <span data-ttu-id="e9587-117">[Weitere Informationen](https://techcommunity.microsoft.com/t5/microsoft-365-blog/microsoft-365-apps-say-farewell-to-internet-explorer-11-and/ba-p/1591666).</span><span class="sxs-lookup"><span data-stu-id="e9587-117">[Learn more](https://techcommunity.microsoft.com/t5/microsoft-365-blog/microsoft-365-apps-say-farewell-to-internet-explorer-11-and/ba-p/1591666).</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="e9587-118">Vorbemerkungen</span><span class="sxs-lookup"><span data-stu-id="e9587-118">Before you begin</span></span>
> [!NOTE]
> <span data-ttu-id="e9587-119">Ab Windows 10, Version 20H2, ist Microsoft Edge Legacy nicht mehr enthalten.</span><span class="sxs-lookup"><span data-stu-id="e9587-119">Starting with Windows 10 version 20H2 Microsoft Edge Legacy is no longer included.</span></span> <span data-ttu-id="e9587-120">Ab dieser Version von Windows 10 wird die parallele Verwendung nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e9587-120">Starting with this version of Windows 10 the side-by-side experience is not supported.</span></span>

<span data-ttu-id="e9587-121">Die Verfahren in diesem Artikel gelten für Systeme, die mit den neuesten Sicherheitsupdates aktualisiert wurden.</span><span class="sxs-lookup"><span data-stu-id="e9587-121">The procedures in this article apply to systems that have been updated with the latest security updates.</span></span> <span data-ttu-id="e9587-122">Wenn die neue Version von Microsoft Edge installiert ist, wird die alte Version (Microsoft Edge Legacy) ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="e9587-122">When the new version of Microsoft Edge is installed, the old version (Microsoft Edge Legacy) will be hidden.</span></span> <span data-ttu-id="e9587-123">Bei allen Versuchen, die alte Version von Microsoft Edge zu starten, wird der Benutzer standardmäßig auf die neu installierte Version von Microsoft Edge umgeleitet.</span><span class="sxs-lookup"><span data-stu-id="e9587-123">By default, all attempts to launch the old version will redirect the user to the newly installed version of Microsoft Edge.</span></span> <span data-ttu-id="e9587-124">In diesem Artikel wird beschrieben, wie Sie Microsoft Edge Legacy nach der Installation von Microsoft Edge weiterhin verwenden können.</span><span class="sxs-lookup"><span data-stu-id="e9587-124">This article describes how you can keep using Microsoft Edge Legacy after you install Microsoft Edge.</span></span>

## <a name="quickstart-side-by-side-experience-with-microsoft-edge-beta-channel-and-microsoft-edge-legacy"></a><span data-ttu-id="e9587-125">Schnellstart: Parallele Verwendung von Microsoft Edge Beta Channel und Microsoft Edge Legacy</span><span class="sxs-lookup"><span data-stu-id="e9587-125">Quickstart: Side-by-side experience with Microsoft Edge Beta Channel and Microsoft Edge Legacy</span></span>

<span data-ttu-id="e9587-126">Bevor Sie die ausführlichen Anweisungen in diesem Artikel verwenden, sollten Sie die folgenden zwei Schritte beachten, damit Ihre Benutzer Microsoft Edge Legacy und Microsoft Edge [Beta Channel](microsoft-edge-channels.md) parallel ausführen können.</span><span class="sxs-lookup"><span data-stu-id="e9587-126">Before using the detailed instructions in this article, consider the following two steps to let your users run Microsoft Edge Legacy and the Microsoft Edge [Beta channel](microsoft-edge-channels.md) side-by-side.</span></span>

1. <span data-ttu-id="e9587-127">Verhindern Sie die automatische Installation des Stable-Kanals von Microsoft Edge durch [Windows Update](https://support.microsoft.com/help/12373/windows-update-faq).</span><span class="sxs-lookup"><span data-stu-id="e9587-127">Prevent the automatic install of the Stable Channel of Microsoft Edge by [Windows Update](https://support.microsoft.com/help/12373/windows-update-faq).</span></span>
2. <span data-ttu-id="e9587-128">Installieren Sie den [Beta-Kanal](https://www.microsoft.com/edge/business/download) der neuen Version von Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="e9587-128">Install the [Beta channel](https://www.microsoft.com/edge/business/download) of the new version of Microsoft Edge.</span></span>

   > [!NOTE]
   > <span data-ttu-id="e9587-129">Lesen Sie [Weitere Informationen](#additional-information) zu den Registrierungsschlüsseleinstellungen.</span><span class="sxs-lookup"><span data-stu-id="e9587-129">Read [Additional information](#additional-information) for information about Registry Key settings.</span></span>

<span data-ttu-id="e9587-130">Diese parallele Lösung ist weniger komplex und erfordert weniger Verwaltungsaufwand als die in diesem Artikel beschriebene detaillierte Lösung.</span><span class="sxs-lookup"><span data-stu-id="e9587-130">This side-by-side solution is less complex and requires less management than the detailed solution described in this article.</span></span> <span data-ttu-id="e9587-131">Diese Lösung bedeutet jedoch, dass Sie den Beta-Kanal anstelle des Stable-Kanals ausführen müssen.</span><span class="sxs-lookup"><span data-stu-id="e9587-131">However, this solution does mean that you'll be running the Beta Channel rather than the Stable Channel.</span></span>

## <a name="side-by-side-experience-with-microsoft-edge-stable-channel-and-microsoft-edge-legacy"></a><span data-ttu-id="e9587-132">Parallele Verwendung von Microsoft Edge Stable Channel und Microsoft Edge Legacy</span><span class="sxs-lookup"><span data-stu-id="e9587-132">Side-by-side experience with Microsoft Edge Stable Channel and Microsoft Edge Legacy</span></span>

<span data-ttu-id="e9587-133">Wenn Sie den stabilen Kanal der nächsten Version von Microsoft Edge auf Systemebene installieren, wird die aktuelle Version (Microsoft Edge Legacy) ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="e9587-133">Installing the Stable Channel of the next version of Microsoft Edge at the system-level will cause the current version (Microsoft Edge Legacy) to be hidden.</span></span> <span data-ttu-id="e9587-134">Wenn Sie Benutzern die parallele Verwendung beider Versionen von Microsoft Edge in Windows ermöglichen möchten, können Sie diese Oberfläche aktivieren, indem Sie die Gruppenrichtlinie **Microsoft Edge-Browser im Parallelbetrieb zulassen** auf **Aktiviert** festlegen.</span><span class="sxs-lookup"><span data-stu-id="e9587-134">If you want to let your users see both versions of Microsoft Edge side by side in Windows, you can enable this experience by setting the **Allow Microsoft Edge Side by Side browser experience** group policy to **Enabled**.</span></span>

<span data-ttu-id="e9587-135">Diese Gruppenrichtlinie ist [hier](./microsoft-edge-update-policies.md#allowsxs) dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="e9587-135">This group policy is documented [here](./microsoft-edge-update-policies.md#allowsxs)</span></span>

### <a name="to-set-up-the-side-by-side-browser-experience-policy"></a><span data-ttu-id="e9587-136">So richten Sie die Richtlinie für den Parallelbetrieb des Browsers ein:</span><span class="sxs-lookup"><span data-stu-id="e9587-136">To set up the side-by-side browser experience policy:</span></span>

1. <span data-ttu-id="e9587-137">Installieren Sie die Richtliniendefinitionen über [Microsoft Edge for Business](https://www.microsoft.com/edge/business/download).</span><span class="sxs-lookup"><span data-stu-id="e9587-137">Install the Policy Definitions from [Microsoft Edge for Business](https://www.microsoft.com/edge/business/download).</span></span>

   - <span data-ttu-id="e9587-138">Wählen Sie KANAL/BUILD und PLATTFORM aus, die Sie verwenden möchten, und klicken Sie dann auf RICHTLINIENDATEIEN ABRUFEN.</span><span class="sxs-lookup"><span data-stu-id="e9587-138">Pick the CHANNEL/BUILD and PLATFORM you want to use, and then click GET POLICY FILES.</span></span>
   - <span data-ttu-id="e9587-139">Extrahieren Sie die gezippten Dateien.</span><span class="sxs-lookup"><span data-stu-id="e9587-139">Extract the zipped files.</span></span>
   - <span data-ttu-id="e9587-140">Kopieren sie msedge.admx und msedgeupdate.admx in das Verzeichnis `C:\Windows\PolicyDefinitions`.</span><span class="sxs-lookup"><span data-stu-id="e9587-140">Copy msedge.admx and msedgeupdate.admx to the `C:\Windows\PolicyDefinitions` directory.</span></span>
   - <span data-ttu-id="e9587-141">Kopieren Sie "msedge.adml" und "msedgeupdate.adml" (aus dem entsprechenden Verzeichnis der Sprache bzw. des Gebietsschemas) in das `C:\Windows\PolicyDefinitions\[APPROPRIATE LANGUAGE/LOCALE]`-Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="e9587-141">Copy msedge.adml and msedgeupdate.adml (from the appropriate language/locale directory) to the `C:\Windows\PolicyDefinitions\[APPROPRIATE LANGUAGE/LOCALE]` directory.</span></span>

2. <span data-ttu-id="e9587-142">Öffnen Sie den Gruppenrichtlinien-Editor (gpedit.msc).</span><span class="sxs-lookup"><span data-stu-id="e9587-142">Open the Group Policy Editor (gpedit.msc).</span></span>
3. <span data-ttu-id="e9587-143">Wechseln Sie unter **Computerkonfiguration** zu *Administrative Vorlagen>Microsoft Edge Update>Anwendungen*.</span><span class="sxs-lookup"><span data-stu-id="e9587-143">Under **Computer Configuration**, go to *Administrative Templates>Microsoft Edge Update>Applications*.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e9587-144">Wenn der Ordner *Microsoft Edge Update* nicht angezeigt wird, überprüfen Sie, ob Schritt 1 ordnungsgemäß abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="e9587-144">If you don't see the *Microsoft Edge Update* folder, verify that step 1 was completed correctly.</span></span>

4. <span data-ttu-id="e9587-145">Doppelklicken Sie unter **Anwendungen** auf „Microsoft Edge-Browser im Parallelbetrieb zulassen”.</span><span class="sxs-lookup"><span data-stu-id="e9587-145">Under **Applications**, double-click "Allow Microsoft Edge Side by Side browser experience".</span></span> <span data-ttu-id="e9587-146">Lesen Sie unsere [Leitlinien für bewährte Methoden](#best-practice-guidance), bevor Sie mit dem nächsten Schrittfortfahren.</span><span class="sxs-lookup"><span data-stu-id="e9587-146">See our [best practice guidance](#best-practice-guidance) before continuing to the next step.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e9587-147">Diese Gruppenrichtlinie ist standardmäßig auf „Nicht konfiguriert” festgelegt, was bewirkt, dass Microsoft Edge Legacy nach der Installation der neuen Version von Microsoft Edge ausgeblendet wird.</span><span class="sxs-lookup"><span data-stu-id="e9587-147">By default, this group policy is set to "Not configured", which results in Microsoft Edge Legacy being hidden when the new version of Microsoft Edge is installed.</span></span>

5. <span data-ttu-id="e9587-148">Wählen Sie **Aktiviert**, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="e9587-148">Select **Enabled** and then click **OK**.</span></span>  

<span data-ttu-id="e9587-149">Durch das Festlegen dieser Richtlinie erhält der folgende Registrierungsschlüssel den Wert "00000001":</span><span class="sxs-lookup"><span data-stu-id="e9587-149">Setting this policy will set the following Registry Key  to '00000001':</span></span>

- <span data-ttu-id="e9587-150">Legende:</span><span class="sxs-lookup"><span data-stu-id="e9587-150">Key:</span></span> `Computer\HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate`
- <span data-ttu-id="e9587-151">Name des Wertes:</span><span class="sxs-lookup"><span data-stu-id="e9587-151">Value Name:</span></span> `Allowsxs`
- <span data-ttu-id="e9587-152">Werttyp:</span><span class="sxs-lookup"><span data-stu-id="e9587-152">Value Type:</span></span> `'REG_DWORD'`

#### <a name="best-practice-guidance"></a><span data-ttu-id="e9587-153">Leitlinien für bewährte Methoden</span><span class="sxs-lookup"><span data-stu-id="e9587-153">Best practice guidance</span></span>

<span data-ttu-id="e9587-154">Für die bestmögliche Benutzerfreundlichkeit sollte die Option **Microsoft Edge-Browser im Parallelbetrieb zulassen** aktiviert werden, bevor die neue Version von Microsoft Edge auf den Geräten der Benutzer bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="e9587-154">For the best experience, the **Allow Microsoft Edge Side by Side browser experience** should be enabled before the new version of Microsoft Edge is deployed to your users' devices.</span></span>

<span data-ttu-id="e9587-155">Wenn die Gruppenrichtlinie aktiviert ist, nachdem Microsoft Edge bereitgestellt wurde, sind die folgenden Nebenwirkungen und erforderliche Aktionen zu beachten:</span><span class="sxs-lookup"><span data-stu-id="e9587-155">If the group policy is enabled after Microsoft Edge is deployed, there are the following side effects and required actions:</span></span>

1. <span data-ttu-id="e9587-156">**Microsoft Edge-Browser im Parallelbetrieb zulassen** wird erst wirksam, nachdem das Installationsprogramm für die neue Version von Microsoft Edge erneut ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="e9587-156">**Allow Microsoft Edge Side by Side browser experience** won't take effect until after the installer for the new version of Microsoft Edge is run again.</span></span>

   > [!NOTE]
   > <span data-ttu-id="e9587-157">Das Installationsprogramm kann direkt oder automatisch ausgeführt werden, wenn die neue Version von Microsoft Edge aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="e9587-157">The installer can be run directly or automatically when the new version of Microsoft Edge updates.</span></span>

2. <span data-ttu-id="e9587-158">Microsoft Edge Legacy muss erneut an "Start" oder die Taskleiste angeheftet werden, da die Anheftung migriert wird, wenn die neue Version von Microsoft Edge bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="e9587-158">Microsoft Edge Legacy will need to be re-pinned to Start or the Taskbar because the pin is migrated when the new version of Microsoft Edge is deployed.</span></span>
3. <span data-ttu-id="e9587-159">Sites, die an "Start" oder die Taskleiste für Microsoft Edge Legacy angeheftet waren, werden auf die neue Version von Microsoft Edge migriert.</span><span class="sxs-lookup"><span data-stu-id="e9587-159">Sites that were pinned to Start or the Taskbar for Microsoft Edge Legacy will be migrated to the new version of Microsoft Edge.</span></span>

## <a name="additional-information"></a><span data-ttu-id="e9587-160">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e9587-160">Additional information</span></span>

<span data-ttu-id="e9587-161">Nachdem die Systeme vollständig aktualisiert sind und der Stable-Kanal der nächsten Version von Microsoft Edge installiert ist, werden der folgende Registrierungsschlüssel und -wert festgelegt:</span><span class="sxs-lookup"><span data-stu-id="e9587-161">After the systems are fully updated and the Stable channel of the next version of Microsoft Edge is installed, the following registry key and value is set:</span></span>

- <span data-ttu-id="e9587-162">Legende:</span><span class="sxs-lookup"><span data-stu-id="e9587-162">Key:</span></span> `Computer\HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\EdgeUpdate\ClientState\{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}`
- <span data-ttu-id="e9587-163">Schlüsselwert:</span><span class="sxs-lookup"><span data-stu-id="e9587-163">Key value:</span></span> `BrowserReplacement`

  > [!IMPORTANT]
  > <span data-ttu-id="e9587-164">Dieser Schlüssel wird bei jeder Aktualisierung des Microsoft Edge Stable-Kanals überschrieben.</span><span class="sxs-lookup"><span data-stu-id="e9587-164">This key is over-written every time the Microsoft Edge Stable channel is updated.</span></span> <span data-ttu-id="e9587-165">Als bewährte Methode wird empfohlen, diesen Schlüssel NICHT zu löschen, damit Benutzer auf beide Versionen von Microsoft Edge zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="e9587-165">As a best practice, we recommend that you DO NOT delete this key to allow users to access both versions of Microsoft Edge.</span></span>

## <a name="see-also"></a><span data-ttu-id="e9587-166">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e9587-166">See also</span></span>

- [<span data-ttu-id="e9587-167">Microsoft Edge Enterprise-Angebotsseite</span><span class="sxs-lookup"><span data-stu-id="e9587-167">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="e9587-168">Windows-Updates zur Unterstützung von Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="e9587-168">Windows updates to support Microsoft Edge</span></span>](microsoft-edge-sysupdate-windows-updates.md)