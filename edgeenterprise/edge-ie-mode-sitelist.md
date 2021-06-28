---
title: Konfigurationsstrategie für Unternehmensstandorte
ms.author: shisub
author: shisub
manager: srugh
ms.date: 05/19/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Eine schrittweise Anleitung zum Konfigurieren der Enterprise Mode Site List für den Internet Explorer-Modus.
ms.openlocfilehash: 7369e4e14f33fc37c6ded0ebc7df57d64a34df50
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2021
ms.locfileid: "11617395"
---
# <a name="enterprise-site-configuration-strategy"></a><span data-ttu-id="24dfc-103">Konfigurationsstrategie für Unternehmensstandorte</span><span class="sxs-lookup"><span data-stu-id="24dfc-103">Enterprise site configuration strategy</span></span>

>[!Note]
> <span data-ttu-id="24dfc-104">Die Internet Explorer 11-Desktopanwendung wird eingestellt und wird ab dem 15. Juni 2022 nicht mehr unterstützt (eine Liste der in diesem Bereich enthaltenen Elemente [finden Sie in den FAQ](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549)).</span><span class="sxs-lookup"><span data-stu-id="24dfc-104">The Internet Explorer 11 desktop application will be retired and go out of support on June 15, 2022 (for a list of what’s in scope, [see the FAQ](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549)).</span></span> <span data-ttu-id="24dfc-105">Dieselben IE11-Apps und -Websites, die Sie heute verwenden, können in Microsoft Edge im Internet Explorer-Modus geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="24dfc-105">The same IE11 apps and sites you use today can open in Microsoft Edge with Internet Explorer mode.</span></span> <span data-ttu-id="24dfc-106">[Weitere Informationen finden Sie hier](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/).</span><span class="sxs-lookup"><span data-stu-id="24dfc-106">[Learn more here](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/).</span></span>

<span data-ttu-id="24dfc-107">In diesem Artikel werden Änderungen an der Enterprise Mode Site List beschrieben, um den Internet Explorer-Modus für Microsoft Edge Version77 und höher zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="24dfc-107">This article describes changes to the Enterprise Mode Site List to support Internet Explorer mode for Microsoft Edge version 77 and later.</span></span>

<span data-ttu-id="24dfc-108">Weitere Informationen zum Schema der XML-Datei der Enterprise Mode Site List finden Sie unter [Anleitungen für Enterprise Mode-Schema Version 2](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).</span><span class="sxs-lookup"><span data-stu-id="24dfc-108">For more information on the schema for the Enterprise Mode Site List XML file, see [Enterprise Mode schema v.2 guidance](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).</span></span>

> [!NOTE]
> <span data-ttu-id="24dfc-109">Dieser Artikel bezieht sich auf Microsoft Edge Version77 oder höher.</span><span class="sxs-lookup"><span data-stu-id="24dfc-109">This article applies to Microsoft Edge version 77 or later.</span></span>
<!--
## Updated schema elements

The following table describes the \<open-in app\> element added to the v.2 of the Enterprise Mode schema:

| **Element** | **Description** |
| --- | --- |
| \<open-in app="**true**"\> | A child element that controls what browser is used for sites. This element is required for sites that need to **open in IE11**.|

**Example:**

``` xml
<site url="contoso.com">

  <open-in app="true">IE11</open-in>

</site>
```

The following table shows the possible values of the \<open-in\> element:

| **Value** | **Description** |
| --- | --- |
| **\<open-in\>IE11\</open-in\>** | Opens the site in IE mode or a full IE11 window. To enable IE mode, see [Configure IE mode policies](./edge-ie-mode-policies.md)|
| **\<open-in app="**true**"\>IE11\</open-in\>** | Opens the site in a full IE11 window |
| **\<open-in\>MSEdge\</open-in\>** | Opens the site in Microsoft Edge |
| **\<open-in\>None or not specified\</open-in\>** | Opens the site in the default browser or in the browser where the user navigated to the site. |
|**\<open-in\>Configurable\</open-in\>** | Allows the site to participate in IE mode engine determination. To learn more, see [Learn about Configurable sites in IE mode](edge-learnmore-configurable-sites-ie-mode.md).  |

>[!NOTE]
> The attribute app=**"true"** is only recognized when associated to _'open-in' IE11_. Adding it to the other 'open-in' elements won't change browser behavior.   -->

## <a name="configuration-strategy"></a><span data-ttu-id="24dfc-110">Konfigurationsstrategie</span><span class="sxs-lookup"><span data-stu-id="24dfc-110">Configuration strategy</span></span>

<span data-ttu-id="24dfc-111">Die folgenden Schritte sind Teil einer Websitekonfigurationsstrategie für den IE-Modus:</span><span class="sxs-lookup"><span data-stu-id="24dfc-111">The following steps are part of a site configuration strategy for IE mode:</span></span>
1. <span data-ttu-id="24dfc-112">Vorbereiten der Websiteliste</span><span class="sxs-lookup"><span data-stu-id="24dfc-112">Prepare your site list</span></span>
2. <span data-ttu-id="24dfc-113">Konfigurieren von neutralen Websites</span><span class="sxs-lookup"><span data-stu-id="24dfc-113">Configure neutral sites</span></span>
3. <span data-ttu-id="24dfc-114">(Optional) Verwenden der Cookiefreigabe bei Bedarf</span><span class="sxs-lookup"><span data-stu-id="24dfc-114">(Optional) Use cookie sharing if necessary</span></span>

<!--
Step 1.  – if you don’t have one use Site Discovery Step-by-Step
Step 2 – Neutral sites + sticky mode
        Use more examples and explain sticky mode better
Step 3 – If that doesn’t cover your needs, then use Cookie sharing -->

## <a name="prepare-your-site-list"></a><span data-ttu-id="24dfc-115">Vorbereiten der Websiteliste</span><span class="sxs-lookup"><span data-stu-id="24dfc-115">Prepare your site list</span></span>

<span data-ttu-id="24dfc-116">Wenn Sie bereits über eine Enterprise Mode Site List für IE11 oder die Vorgängerversion von Microsoft Edge verfügen, können Sie sie wiederverwenden, um den IE-Modus zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="24dfc-116">If you already have an Enterprise Mode site list for IE11 or Microsoft Edge Legacy, you can reuse it to configure IE mode.</span></span>

<span data-ttu-id="24dfc-117">Wenn Sie jedoch keine Websiteliste haben, können Sie das [Enterprise Site Discovery-Tool](/deployedge/edge-ie-mode-site-discovery) verwenden, um Ihre Websiteliste aufzufüllen.</span><span class="sxs-lookup"><span data-stu-id="24dfc-117">However, if you don't have a site list, you can use the [Enterprise Site Discovery tool](/deployedge/edge-ie-mode-site-discovery) to populate your site list.</span></span>

## <a name="configure-neutral-sites"></a><span data-ttu-id="24dfc-118">Konfigurieren von neutralen Websites</span><span class="sxs-lookup"><span data-stu-id="24dfc-118">Configure neutral sites</span></span>

<span data-ttu-id="24dfc-119">Damit der IE-Modus ordnungsgemäß funktioniert, müssen Authentifizierungs-/Einmaliges Anmelden (Single Sign-On, SSO)-Server explizit als neutrale Standorte konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="24dfc-119">In order for IE mode to work properly, authentication / Single Sign-On (SSO) servers will need to be explicitly configured as neutral sites.</span></span> <span data-ttu-id="24dfc-120">Andernfalls versuchen die Seiten des IE-Modus, zu Microsoft Edge umzuleiten, und die Authentifizierung wird fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="24dfc-120">Otherwise, IE mode pages will try to redirect to Microsoft Edge, and authentication will fail.</span></span>

<span data-ttu-id="24dfc-121">Eine neutrale Website verwendet den Browser, in dem die Navigation begonnen wurde – entweder Microsoft Edge oder IE-Modus.</span><span class="sxs-lookup"><span data-stu-id="24dfc-121">A neutral site will use the browser where the navigation started - either Microsoft Edge or IE mode.</span></span> <span data-ttu-id="24dfc-122">Außerdem wird durch das Konfigurieren neutraler Websites sichergestellt, dass alle Anwendungen, die diese Authentifizierungsserver verwenden – sowohl moderne als auch ältere – weiterhin funktionsfähig sind.</span><span class="sxs-lookup"><span data-stu-id="24dfc-122">Configuring neutral sites ensures that all applications using these authentication servers, both modern and legacy, continue to work.</span></span>

<span data-ttu-id="24dfc-123">Sie können neutrale Websites konfigurieren, indem Sie im Enterprise Mode Site List Manager-Tool für *Öffnen mit* in der Dropdownliste "Keine" festlegen, oder indem Sie das Websitelisten-XML direkt aktualisieren:</span><span class="sxs-lookup"><span data-stu-id="24dfc-123">You can configure neutral sites by setting the *Open In* dropdown to 'None' in the Enterprise Mode Site List Manager tool or by directly updating the site list XML:</span></span>

``` xml
<site url="login.contoso.com">
   
    <open-in>None</open-in>

</site>
```

<span data-ttu-id="24dfc-124">Wenn Sie Authentifizierungsserver identifizieren möchten, überprüfen Sie den Netzwerkdatenverkehr einer Anwendung mithilfe der IE 11-Entwicklungstools.</span><span class="sxs-lookup"><span data-stu-id="24dfc-124">To identify authentication servers, inspect the network traffic from an application using the IE11 Developer Tools.</span></span> <span data-ttu-id="24dfc-125">Wenn Sie mehr Zeit benötigen, um Ihre Authentifizierungsserver zu identifizieren, können Sie eine Richtlinie so konfigurieren, dass alle Seitennavigationen im IE-Modus bleiben, damit Ihre Benutzer ihre Workflows ohne Unterbrechungen fortsetzen können.</span><span class="sxs-lookup"><span data-stu-id="24dfc-125">If you need more time to identify your authentication servers, you can configure a policy to keep all in-page navigations in IE mode to allow your users to continue their workflows uninterrupted.</span></span> <span data-ttu-id="24dfc-126">Deaktivieren Sie diese Einstellung, sobald Sie ihre Authentifizierungsserver identifiziert und der Websiteliste hinzugefügt haben, um die Verwendung des IE-Modus zu minimieren.</span><span class="sxs-lookup"><span data-stu-id="24dfc-126">To minimize the use of IE mode when unnecessary, disable this setting once you've identified and added your authentication servers to the site list.</span></span> <span data-ttu-id="24dfc-127">Weitere Informationen finden Sie unter [Keep in-page navigation in IE mode](/deployedge/edge-learnmore-inpage-nav).</span><span class="sxs-lookup"><span data-stu-id="24dfc-127">For more information, see [Keep in-page navigation in IE mode](/deployedge/edge-learnmore-inpage-nav).</span></span>

>[!NOTE]
   ><span data-ttu-id="24dfc-128">Das Enterprise Mode-Schema Version 1 wird für die Integration des IE-Modus nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="24dfc-128">Enterprise Mode schema v.1 isn't supported for IE mode integration.</span></span> <span data-ttu-id="24dfc-129">Wenn Sie derzeit Schema V.1 mit Internet Explorer 11 verwenden, müssen Sie ein Upgrade auf Schema V.2 durchführen.</span><span class="sxs-lookup"><span data-stu-id="24dfc-129">If you are currently using schema v.1 with Internet Explorer 11, you must upgrade to schema v.2.</span></span> <span data-ttu-id="24dfc-130">Weitere Informationen finden Sie unter [Enterprise Mode-Schema Version 2-Richtlinien](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).</span><span class="sxs-lookup"><span data-stu-id="24dfc-130">For more information, see [Enterprise Mode schema v.2 guidance](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).</span></span>

## <a name="optional-use-cookie-sharing-if-necessary"></a><span data-ttu-id="24dfc-131">(Optional) Verwenden der Cookiefreigabe bei Bedarf</span><span class="sxs-lookup"><span data-stu-id="24dfc-131">(Optional) Use cookie sharing if necessary</span></span>

<span data-ttu-id="24dfc-132">Standardmäßig teilen die Microsoft Edge- und Internet Explorer-Prozesse keine Sitzungscookies, und diese mangelnde Freigabe kann während des IE-Modus in einigen Fällen unpraktisch sein.</span><span class="sxs-lookup"><span data-stu-id="24dfc-132">By default, the Microsoft Edge and Internet Explorer processes don't share session cookies, and this lack of sharing can be inconvenient in some cases while using IE mode.</span></span> <span data-ttu-id="24dfc-133">Wenn sich ein Benutzer z. B. im IE-Modus erneut authentifizieren muss, wenn er dies gewohnt ist oder wenn er sich von einer Microsoft Edge-Sitzung abmeldet, wird die Internet Explorer-Modussitzung für kritische Transaktionen nicht abgemeldet.</span><span class="sxs-lookup"><span data-stu-id="24dfc-133">For example, when a user has to reauthenticate in IE mode when previously they are accustomed to doing so or when signing out of a Microsoft Edge session doesn’t sign out of the Internet Explorer mode session for critical transactions.</span></span> <span data-ttu-id="24dfc-134">In diesen Szenarien können Sie bestimmte von SSO festgelegte Cookies so konfigurieren, dass sie von Microsoft Edge an Internet Explorer gesendet werden, damit die Authentifizierungserfahrung verbessert wird, indem keine erneute Authentifizierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="24dfc-134">In these scenarios, you can configure specific cookies set by SSO to be sent from Microsoft Edge to Internet Explorer so the authentication experience becomes more seamless by eliminating the need to reauthenticate.</span></span> <span data-ttu-id="24dfc-135">Weitere Informationen finden Sie unter [Cookie sharing from Microsoft Edge to Internet Explorer](/deployedge/edge-ie-mode-add-guidance-cookieshare).</span><span class="sxs-lookup"><span data-stu-id="24dfc-135">For more information, see [Cookie sharing from Microsoft Edge to Internet Explorer](/deployedge/edge-ie-mode-add-guidance-cookieshare).</span></span>

## <a name="see-also"></a><span data-ttu-id="24dfc-136">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="24dfc-136">See also</span></span>

- [<span data-ttu-id="24dfc-137">Microsoft Edge Enterprise-Angebotsseite</span><span class="sxs-lookup"><span data-stu-id="24dfc-137">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="24dfc-138">Informationen zum IE-Modus</span><span class="sxs-lookup"><span data-stu-id="24dfc-138">About IE mode</span></span>](./edge-ie-mode.md)
- [<span data-ttu-id="24dfc-139">Weitere Informationen zum Unternehmensmodus</span><span class="sxs-lookup"><span data-stu-id="24dfc-139">Additional Enterprise Mode information</span></span>](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
