---
title: Umleitung von Internet Explorer zu Microsoft Edge zur Kompatibilität mit modernen Websites
ms.author: laannade
author: dan-wesley
manager: ratetali
ms.date: 11/03/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Umleitung von Internet Explorer zu Microsoft Edge zur Kompatibilität mit modernen Websites
ms.openlocfilehash: d822bf4cef76fe4c0298133b47ed80f5d1242b3d
ms.sourcegitcommit: 73fec3998f26d110252ace621be01f1c1142cf57
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2020
ms.locfileid: "11151095"
---
# <span data-ttu-id="f3d66-103">Umleitung von Internet Explorer zu Microsoft Edge zur Kompatibilität mit modernen Websites</span><span class="sxs-lookup"><span data-stu-id="f3d66-103">Redirection from Internet Explorer to Microsoft Edge for compatibility with modern web sites</span></span>

> [!NOTE]
> <span data-ttu-id="f3d66-104">Dieser Artikel bezieht sich auf die stabile Microsoft Edge Version 87 oder neuer.</span><span class="sxs-lookup"><span data-stu-id="f3d66-104">This article applies to Microsoft Edge Stable version 87 or later.</span></span>

## <span data-ttu-id="f3d66-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="f3d66-105">Overview</span></span>

<span data-ttu-id="f3d66-106">Viele moderne Websites haben Designs, die mit Internet Explorer nicht kompatibel sind.</span><span class="sxs-lookup"><span data-stu-id="f3d66-106">Many modern websites have designs that are incompatible with Internet Explorer.</span></span> <span data-ttu-id="f3d66-107">Immer wenn ein Internet Explorer-Benutzer eine inkompatible öffentliche Website besucht, erhält er eine Nachricht, die besagt, dass die Website mit seinem Browser inkompatibel ist, und er muss manuell zu einem anderen Browser wechseln.</span><span class="sxs-lookup"><span data-stu-id="f3d66-107">Whenever an Internet Explorer user visits an incompatible public site, they get a message that tells them the site is incompatible with their browser, and they need to manually switch to a different browser.</span></span>

<span data-ttu-id="f3d66-108">Die Notwendigkeit, manuell zu einem anderen Browser zu wechseln, ändert sich ab der stabilen Microsoft Edge Version 87.</span><span class="sxs-lookup"><span data-stu-id="f3d66-108">The need to  manually switch to a different browser changes starting with Microsoft Edge Stable version 87.</span></span>

<span data-ttu-id="f3d66-109">Wenn ein Benutzer zu einer Website wechselt, die mit Internet Explorer nicht kompatibel ist, wird er automatisch zu Microsoft Edge umgeleitet.</span><span class="sxs-lookup"><span data-stu-id="f3d66-109">When a user goes to a site that is incompatible with Internet Explorer, they will be automatically redirected to Microsoft Edge.</span></span> <span data-ttu-id="f3d66-110">In diesem Artikel werden die Benutzererfahrung für die Umleitung sowie die Gruppenrichtlinien beschrieben, die zum Konfigurieren oder Deaktivieren der automatischen Umleitung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f3d66-110">This article describes the user experience for redirection and the group policies that are used to configure or disable automatic redirection.</span></span>

> [!NOTE]
> <span data-ttu-id="f3d66-111">Microsoft verwaltet eine Liste aller Websites, von denen bekannt ist, dass sie nicht mit Internet Explorer kompatibel sind.</span><span class="sxs-lookup"><span data-stu-id="f3d66-111">Microsoft maintains a list of all sites that are known to be incompatible with Internet Explorer.</span></span>

## <span data-ttu-id="f3d66-112">Umleitungserfahrung</span><span class="sxs-lookup"><span data-stu-id="f3d66-112">Redirection experience</span></span>

<span data-ttu-id="f3d66-113">Bei der Umleitung zu Microsoft Edge wird den Benutzern das einmalige Dialogfeld im nächsten Screenshot angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f3d66-113">On redirection to Microsoft Edge, users are shown the one-time dialog in the next screenshot.</span></span> <span data-ttu-id="f3d66-114">In diesem Dialogfeld wird erklärt, warum sie umgeleitet werden, und fordert sie auf, die Zustimmung zum Kopieren ihrer Browserdaten und -Einstellungen von Internet Explorer zu Microsoft Edge zu erteilen.</span><span class="sxs-lookup"><span data-stu-id="f3d66-114">This dialog explains why they're getting redirected and prompts for consent to copy their browsing data and preferences from Internet Explorer to Microsoft Edge.</span></span> <span data-ttu-id="f3d66-115">Die folgenden Browserdaten werden importiert: Favoriten, Kennwörter, Suchmaschinen, offene Registerkarten, Verlauf, Einstellungen, Cookies und die Startseite.</span><span class="sxs-lookup"><span data-stu-id="f3d66-115">The following browsing data will be imported: Favorites, Passwords, Search engines, open tabs, History, settings, cookies, and the Home Page.</span></span>

![Suchbenachrichtigung und Aufforderung zum Import von Daten und Einstellungen.](media/edge-learnmore-neededge/neededge-dialog1.png)

<span data-ttu-id="f3d66-117">Selbst wenn sie keine Zustimmung durch das Ankreuzen von „Meine Browserdaten und -Einstellungen von Internet Explorer immer übermitteln", können sie auf **Weiter surfen** klicken, um ihre Sitzung fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="f3d66-117">Even if they don't give their consent by checking "Always bring over my browsing data and preferences from Internet Explorer", they can click **Continue browsing** to continue their session.</span></span>

<span data-ttu-id="f3d66-118">Schließlich wird für jede Umleitung unterhalb der Adressleiste ein Banner zur Websiteinkompatibilität angezeigt, das im nächsten Screenshot dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="f3d66-118">Finally, a website incompatibility banner, shown in the next screenshot, appears below the address bar for every redirection.</span></span>

![Benachrichtigung über moderne Websites und Aufforderung, Microsoft Edge als Standardbrowser festzulegen oder Microsoft Edge zu erkunden.](media/edge-learnmore-neededge/neededge-banner.png)

<span data-ttu-id="f3d66-120">Das Banner zur Websiteinkompatibilität:</span><span class="sxs-lookup"><span data-stu-id="f3d66-120">The website incompatibility banner:</span></span>

- <span data-ttu-id="f3d66-121">Ermutigt den Benutzer, zu Microsoft Edge zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="f3d66-121">encourages the user to switch to Microsoft Edge</span></span>
- <span data-ttu-id="f3d66-122">Bietet an, Microsoft Edge als Standardbrowser festzulegen.</span><span class="sxs-lookup"><span data-stu-id="f3d66-122">offers to make Microsoft Edge as the default browser</span></span>
- <span data-ttu-id="f3d66-123">Bietet dem Benutzer die Möglichkeit, Microsoft Edge zu erkunden.</span><span class="sxs-lookup"><span data-stu-id="f3d66-123">gives the user the option to explore Microsoft Edge</span></span>

<span data-ttu-id="f3d66-124">Wenn eine Website von Internet Explorer zu Microsoft Edge umgeleitet wird, wird die Internet Explorer-Registerkarte, mit der die Website geladen wurde, geschlossen, wenn Sie keine vorherigen Inhalte aufweist.</span><span class="sxs-lookup"><span data-stu-id="f3d66-124">When a site is redirected from Internet Explorer to Microsoft Edge, the Internet Explorer tab that started loading the site is closed if it had no prior content.</span></span> <span data-ttu-id="f3d66-125">Andernfalls wechselt die aktive Registerkartendarstellung zu einer Microsoft [Support](https://support.microsoft.com/office/the-website-you-were-trying-to-reach-doesn-t-work-with-internet-explorer-8f5fc675-cd47-414c-9535-12821ddfc554?ui=en-US&rs=en-US&ad=US) -Seite, die erklärt, warum die Website zu Microsoft Edge umgeleitet wurde.</span><span class="sxs-lookup"><span data-stu-id="f3d66-125">Otherwise, the active tab view goes to a  Microsoft [support](https://support.microsoft.com/office/the-website-you-were-trying-to-reach-doesn-t-work-with-internet-explorer-8f5fc675-cd47-414c-9535-12821ddfc554?ui=en-US&rs=en-US&ad=US) page that explains why the site was redirected to Microsoft Edge.</span></span>

> [!NOTE]
> <span data-ttu-id="f3d66-126">Nach einer Umleitung können Benutzer zu Internet Explorer zurückkehren, um Websites zu nutzen, die nicht in der Internet Explorer-Inkompatibilitätsliste enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="f3d66-126">After a redirection users can go back to using Internet Explorer for sites that are not on the Internet Explorer incompatibility list.</span></span>  

## <span data-ttu-id="f3d66-127">Richtlinien zum Konfigurieren der Umleitung zu Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f3d66-127">Policies to configure redirection to Microsoft Edge</span></span>

> [!NOTE]
> <span data-ttu-id="f3d66-128">Diese Richtlinien werden bis zum 26. Oktober 2020 als ADMX-Datei-Updates, und bis zum 9. November 2020 in Intune verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="f3d66-128">These policies will be available as ADMX file updates by October 26, 2020 and will be available in Intune by November 9, 2020.</span></span>

<span data-ttu-id="f3d66-129">Drei Gruppenrichtlinien müssen konfiguriert sein, um die automatische Umleitung zu Microsoft Edge zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="f3d66-129">Three group policies must be configured to enable automatic redirection to Microsoft Edge.</span></span> <span data-ttu-id="f3d66-130">Diese Richtlinien lauten:</span><span class="sxs-lookup"><span data-stu-id="f3d66-130">These policies are:</span></span>

- <span data-ttu-id="f3d66-131">RedirectSitesFromInternetExplorerPreventBHOInstall</span><span class="sxs-lookup"><span data-stu-id="f3d66-131">RedirectSitesFromInternetExplorerPreventBHOInstall</span></span>
- <span data-ttu-id="f3d66-132">RedirectSitesFromInternetExplorerRedirectMode</span><span class="sxs-lookup"><span data-stu-id="f3d66-132">RedirectSitesFromInternetExplorerRedirectMode</span></span>
- <span data-ttu-id="f3d66-133">HideInternetExplorerRedirectUXForIncompatibleSitesEnabled</span><span class="sxs-lookup"><span data-stu-id="f3d66-133">HideInternetExplorerRedirectUXForIncompatibleSitesEnabled</span></span>

### <span data-ttu-id="f3d66-134">Richtlinie: RedirectSitesFromInternetExplorerPreventBHOInstall</span><span class="sxs-lookup"><span data-stu-id="f3d66-134">Policy: RedirectSitesFromInternetExplorerPreventBHOInstall</span></span>

<span data-ttu-id="f3d66-135">Die Umleitung von Internet Explorer zu Microsoft Edge erfordert ein Internet Explorer-Browserhilfsobjekt (BHO) mit dem Namen „IEtoEdge BHO“.</span><span class="sxs-lookup"><span data-stu-id="f3d66-135">Redirection from Internet Explorer to Microsoft Edge requires an Internet Explorer Browser Helper Object (BHO) named "IEtoEdge BHO".</span></span> <span data-ttu-id="f3d66-136">Die Richtlinie **RedirectSitesFromInternetExplorerPreventBHOInstall** steuert, ob dieses BHO installiert ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="f3d66-136">The **RedirectSitesFromInternetExplorerPreventBHOInstall** policy controls whether or not this BHO is installed.</span></span>  

- <span data-ttu-id="f3d66-137">Wenn Sie diese Richtlinie aktivieren, wird das für die Umleitung erforderliche BHO nicht installiert, und Ihre Benutzer sehen weiterhin Inkompatibilitätsmeldungen für bestimmte Websites in Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="f3d66-137">If you enable this policy, the BHO required for redirection will not be installed and your users will continue to see incompatibility messages for certain websites on Internet Explorer.</span></span> <span data-ttu-id="f3d66-138">Wenn das BHO bereits installiert ist, wird es beim nächsten Update des stabilen Microsoft Edge-Kanals deinstalliert.</span><span class="sxs-lookup"><span data-stu-id="f3d66-138">If the BHO is already installed, it will be uninstalled the next time the Microsoft Edge Stable channel is updated.</span></span>
- <span data-ttu-id="f3d66-139">Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, wird das BHO installiert.</span><span class="sxs-lookup"><span data-stu-id="f3d66-139">If you disable or don't configure this policy, the BHO will be installed.</span></span> <span data-ttu-id="f3d66-140">Hierbei handelt es sich um das standardmäßige Verhalten.</span><span class="sxs-lookup"><span data-stu-id="f3d66-140">This is the default behavior.</span></span>

<span data-ttu-id="f3d66-141">Zusätzlich zur Notwendigkeit des BHO gibt es eine Abhängigkeit bei **RedirectSitesFromInternetExplorerRedirectMode**, was auf „Websites basierend auf der Websiteliste inkompatibler Websites umleiten“ oder „Nicht konfiguriert“ festgelegt sein muss.</span><span class="sxs-lookup"><span data-stu-id="f3d66-141">In addition to needing the BHO, there is a dependency on the **RedirectSitesFromInternetExplorerRedirectMode**, which needs to be set to "Redirect sites based on the incompatible sites sitelist" or "Not Configured".</span></span>

### <span data-ttu-id="f3d66-142">Richtlinie: RedirectSitesFromInternetExplorerRedirectMode</span><span class="sxs-lookup"><span data-stu-id="f3d66-142">Policy: RedirectSitesFromInternetExplorerRedirectMode</span></span>

 <span data-ttu-id="f3d66-143">Diese Richtlinie entspricht der Microsoft Edge-**Standardbrowser**-Einstellung „Internet Explorer kann Websites in Microsoft Edge öffnen".</span><span class="sxs-lookup"><span data-stu-id="f3d66-143">This policy corresponds to the Microsoft Edge **Default browser** setting "Let Internet Explorer open sites in Microsoft Edge".</span></span> <span data-ttu-id="f3d66-144">Sie können auf diese Einstellung zugreifen, indem Sie zur URL *edge://settings/defaultbrowser* wechseln.</span><span class="sxs-lookup"><span data-stu-id="f3d66-144">You can access this setting by going to the *edge://settings/defaultbrowser* URL.</span></span>  

- <span data-ttu-id="f3d66-145">Wenn Sie diese Richtlinie nicht konfigurieren oder auf „Websiteliste“ festlegen, leitet Internet Explorer inkompatible Websites zu Microsoft Edge um.</span><span class="sxs-lookup"><span data-stu-id="f3d66-145">If you don't configure this policy or set it to "Sitelist", Internet Explorer will redirect incompatible sites to Microsoft Edge.</span></span> <span data-ttu-id="f3d66-146">Hierbei handelt es sich um das standardmäßige Verhalten.</span><span class="sxs-lookup"><span data-stu-id="f3d66-146">This is the default behavior.</span></span>
- <span data-ttu-id="f3d66-147">Wenn Sie diese Richtlinie deaktivieren möchten, wählen Sie **Aktiviert** UND dann in der Dropdownliste unter “Optionen: Inkompatible Websites von Internet Explorer zu Microsoft Edge umleiten” **Deaktivieren** aus.</span><span class="sxs-lookup"><span data-stu-id="f3d66-147">To disable this policy, select **Enabled** AND then in the dropdown under Options: Redirect incompatible sites from Internet Explorer to Microsoft Edge, select **Disable**.</span></span> <span data-ttu-id="f3d66-148">In diesem Zustand werden inkompatible Websites nicht zu Microsoft Edge umgeleitet.</span><span class="sxs-lookup"><span data-stu-id="f3d66-148">In this state, incompatible sites aren't redirected to Microsoft Edge.</span></span>

> [!NOTE]
> <span data-ttu-id="f3d66-149">Wenn Sie ein persönliches Gerät verwenden, das nicht von Ihrem Unternehmen verwaltet wird, wird unter **Internet Explorer-Kompatibilität** die Einstellung „Zulassen, dass Websites im Internet Explorer-Modus geladen werden“ angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f3d66-149">If you're on a personal device that isn't  managed by your organization, you'll see another setting named "Allow sites to be loaded in Internet Explorer mode" under **Internet Explorer compatibility**.</span></span>
>
><span data-ttu-id="f3d66-150">Wenn Sie ein in die Domäne eingebundenes Gerät oder ein beim Mobile Device Management (MDM) registriertes Gerät verwenden, wird diese Option nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f3d66-150">If you're on a domain joined or Mobile Device Management (MDM) enrolled device, you won't see this option.</span></span>
>
> <span data-ttu-id="f3d66-151">Wenn Sie Ihren Benutzern stattdessen das Laden von Websites im Internet Explorer-Modus gestatten möchten, können Sie dies tun, indem Sie die Richtlinie [Internet Explorer-Modustest](https://docs.microsoft.com/deployedge/microsoft-edge-policies#allow-internet-explorer-mode-testing) konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="f3d66-151">Instead, if you want to let your users load sites in Internet Explorer mode, you can do so by configuring the policy [Allow Internet Explorer mode testing](https://docs.microsoft.com/deployedge/microsoft-edge-policies#allow-internet-explorer-mode-testing).</span></span>

### <span data-ttu-id="f3d66-152">Richtlinie: HideInternetExplorerRedirectUXForIncompatibleSitesEnabled</span><span class="sxs-lookup"><span data-stu-id="f3d66-152">Policy: HideInternetExplorerRedirectUXForIncompatibleSitesEnabled</span></span>

<span data-ttu-id="f3d66-153">Diese Richtlinie konfiguriert die Benutzererfahrung bei der Umleitung bei inkompatiblen Websites zu Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="f3d66-153">This policy configures the user experience for incompatible site redirection to Microsoft Edge.</span></span>  

- <span data-ttu-id="f3d66-154">Wenn Sie diese Richtlinie aktivieren, wird den Benutzern nie das einmalige Umleitungsdialogfeld und das Umleitungsbanner angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f3d66-154">If you enable this policy, users never see the one-time redirection dialog and the redirection banner.</span></span> <span data-ttu-id="f3d66-155">Es werden keine Browserdaten oder Benutzereinstellungen importiert.</span><span class="sxs-lookup"><span data-stu-id="f3d66-155">No browser data or user preferences are imported.</span></span>
- <span data-ttu-id="f3d66-156">Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, wird das Umleitungsdialogfeld bei der ersten Umleitung angezeigt, und das beständige Umleitungsbanner wird für Sitzungen angezeigt, die mit einer Umleitung beginnen.</span><span class="sxs-lookup"><span data-stu-id="f3d66-156">If you disable or don't configure this policy, the redirection dialog will be shown on the first redirection and the persistent redirection banner will be shown for sessions that start with a redirection.</span></span>

  > [!NOTE]
  > <span data-ttu-id="f3d66-157">Benutzer-Browserdaten werden jedes Mal importiert, wenn ein Benutzer neu umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="f3d66-157">User browsing data will be imported every time a user encounters a new redirection.</span></span> <span data-ttu-id="f3d66-158">Dies geschieht jedoch nur, wenn der Benutzer dem Import im einmaligen Umleitungsdialogfeld zugestimmt hat.</span><span class="sxs-lookup"><span data-stu-id="f3d66-158">However, this only happens if the user consented to the import on the one-time redirection dialog.</span></span>

## <span data-ttu-id="f3d66-159">Deaktivieren der Umleitung zu Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f3d66-159">Disable redirection to Microsoft Edge</span></span>

<span data-ttu-id="f3d66-160">Wenn Sie die Umleitung VOR dem Update auf die stabile Microsoft Edge-Version 87 deaktivieren möchten, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="f3d66-160">If you want to disable redirection BEFORE updating to Microsoft Edge Stable version 87, use the following step:</span></span>

1. <span data-ttu-id="f3d66-161">Legen Sie die Richtlinie **RedirectSitesFromInternetExplorerPreventBHOInstall** auf **Aktiviert** fest.</span><span class="sxs-lookup"><span data-stu-id="f3d66-161">Set the **RedirectSitesFromInternetExplorerPreventBHOInstall** policy to **Enabled**.</span></span>

<span data-ttu-id="f3d66-162">Wenn Sie die Umleitung NACH dem Update auf die stabile Microsoft Edge-Version 87 deaktivieren möchten, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="f3d66-162">If you want to disable redirection AFTER updating to Microsoft Edge Stable version 87, use the following steps:</span></span>

1. <span data-ttu-id="f3d66-163">Legen Sie die Richtlinie **RedirectSitesFromInternetExplorerRedirectMode** auf **Aktiviert** fest, und wählen Sie dann in der Dropdownliste unter “Optionen: Inkompatible Websites von Internet Explorer zu Microsoft Edge umleiten” **Deaktivieren** aus.</span><span class="sxs-lookup"><span data-stu-id="f3d66-163">Set the **RedirectSitesFromInternetExplorerRedirectMode** policy to **Enabled** AND then in the dropdown under Options: Redirect incompatible sites from Internet Explorer to Microsoft Edge, select **Disable**.</span></span> <span data-ttu-id="f3d66-164">Diese Einstellung beendet die Umleitung, sobald die Richtlinie wirksam wird.</span><span class="sxs-lookup"><span data-stu-id="f3d66-164">This setting will stop redirecting as soon as the policy takes effect.</span></span>
2. <span data-ttu-id="f3d66-165">Legen Sie die Richtlinie **RedirectSitesFromInternetExplorerPreventBHOInstall** auf **Aktiviert** fest.</span><span class="sxs-lookup"><span data-stu-id="f3d66-165">Set the **RedirectSitesFromInternetExplorerPreventBHOInstall** policy to **Enabled**.</span></span> <span data-ttu-id="f3d66-166">Damit wird das BHO nach dem nächsten Microsoft Edge-Update deinstalliert.</span><span class="sxs-lookup"><span data-stu-id="f3d66-166">This will uninstall the BHO after the next Microsoft Edge update.</span></span>

## <span data-ttu-id="f3d66-167">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f3d66-167">See also</span></span>

- [<span data-ttu-id="f3d66-168">Microsoft Edge Enterprise-Angebotsseite</span><span class="sxs-lookup"><span data-stu-id="f3d66-168">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="f3d66-169">Microsoft Edge-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="f3d66-169">Microsoft Edge Policies</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies)
