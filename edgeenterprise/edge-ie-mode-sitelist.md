---
title: Konfigurieren von Websites in der Enterprise Mode Site List
ms.author: cjacks
author: cjacks
manager: saudm
ms.date: 05/28/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Konfigurieren der Enterprise Site List
ms.openlocfilehash: 969a4f6001dbe08a51c26ecf35812b101d315a59
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/31/2020
ms.locfileid: "10980039"
---
# <span data-ttu-id="9dac7-103">Konfigurieren von Websites in der Enterprise Mode Site List</span><span class="sxs-lookup"><span data-stu-id="9dac7-103">Configure Sites on the Enterprise Mode Site List</span></span>

<span data-ttu-id="9dac7-104">In diesem Artikel werden die Änderungen an der Enterprise Mode Site List beschrieben, die das Konfigurieren des IE-Modus für die Microsoft Edge-Version 77 und höher unterstützen.</span><span class="sxs-lookup"><span data-stu-id="9dac7-104">This article describes changes to the Enterprise Mode Site List that support configuring IE mode for Microsoft Edge version 77 and later.</span></span>

<span data-ttu-id="9dac7-105">Weitere Informationen zum Schema der XML-Datei der Enterprise Mode Site List finden Sie unter [Anleitungen für Enterprise Mode-Schema v.2](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).</span><span class="sxs-lookup"><span data-stu-id="9dac7-105">For more information on the schema for the Enterprise Mode Site List XML file, see [Enterprise Mode schema v.2 guidance](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).</span></span>

> [!NOTE]
> <span data-ttu-id="9dac7-106">Dieser Artikel bezieht sich auf die Microsoft Edge-Kanäle **Stable**, **Beta** und **Dev**, Version 77 oder höher.</span><span class="sxs-lookup"><span data-stu-id="9dac7-106">This article applies to Microsoft Edge **Stable**, **Beta** and **Dev** Channels, version 77 or later.</span></span>

## <span data-ttu-id="9dac7-107">Aktualisierte Schemaelemente</span><span class="sxs-lookup"><span data-stu-id="9dac7-107">Updated schema elements</span></span>

<span data-ttu-id="9dac7-108">In der folgenden Tabelle wird das \<open-in app\>-Element beschrieben, das dem Unternehmensmodus-Schema V.2 hinzugefügt wurde:</span><span class="sxs-lookup"><span data-stu-id="9dac7-108">The following table describes the \<open-in app\> element added to the v.2 of the Enterprise Mode schema:</span></span>

| **<span data-ttu-id="9dac7-109">Element</span><span class="sxs-lookup"><span data-stu-id="9dac7-109">Element</span></span>** | **<span data-ttu-id="9dac7-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9dac7-110">Description</span></span>** |
| --- | --- |
| \<open-in app="**true**"\> | <span data-ttu-id="9dac7-111">Ein untergeordnetes Element, das steuert, welcher Browser für Websites verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9dac7-111">A child element that controls what browser is used for sites.</span></span> <span data-ttu-id="9dac7-112">Dieses Element ist für Websites erforderlich, die **in IE11 geöffnet** werden müssen.</span><span class="sxs-lookup"><span data-stu-id="9dac7-112">This element is required for sites that need to **open in IE11**.</span></span>|

**<span data-ttu-id="9dac7-113">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="9dac7-113">Example:</span></span>**

``` xml
<site url="contoso.com">

  <open-in app="true">IE11</open-in>

</site>
```

<span data-ttu-id="9dac7-114">In der folgenden Tabelle sind die möglichen Werte des \<open-in\>-Elements aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="9dac7-114">The following table shows the possible values of the \<open-in\> element:</span></span>

| **<span data-ttu-id="9dac7-115">Wert</span><span class="sxs-lookup"><span data-stu-id="9dac7-115">Value</span></span>** | **<span data-ttu-id="9dac7-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9dac7-116">Description</span></span>** |
| --- | --- |
| **\<open-in\><span data-ttu-id="9dac7-117">IE11</span><span class="sxs-lookup"><span data-stu-id="9dac7-117">IE11</span></span>\</open-in\>** | <span data-ttu-id="9dac7-118">Öffnet die Website im IE-Modus oder in einem vollständigen IE11-Fenster.</span><span class="sxs-lookup"><span data-stu-id="9dac7-118">Opens the site in IE mode or a full IE11 window.</span></span> <span data-ttu-id="9dac7-119">Informationen zum Aktivieren des IE-Modus finden Sie unter [Konfigurieren von Richtlinien für den IE-Modus](https://docs.microsoft.com/deployedge/edge-ie-mode-policies)</span><span class="sxs-lookup"><span data-stu-id="9dac7-119">To enable IE mode, see [Configure IE mode policies](https://docs.microsoft.com/deployedge/edge-ie-mode-policies)</span></span>|
| **\<open-in app="**true**"\><span data-ttu-id="9dac7-120">IE11</span><span class="sxs-lookup"><span data-stu-id="9dac7-120">IE11</span></span>\</open-in\>** | <span data-ttu-id="9dac7-121">Öffnet die Website im IE-Modus oder in einem vollständigen IE11-Fenster</span><span class="sxs-lookup"><span data-stu-id="9dac7-121">Opens the site in a full IE11 window</span></span> |
| **\<open-in\><span data-ttu-id="9dac7-122">MSEdge</span><span class="sxs-lookup"><span data-stu-id="9dac7-122">MSEdge</span></span>\</open-in\>** | <span data-ttu-id="9dac7-123">Öffnet die Website in Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="9dac7-123">Opens the site in Microsoft Edge</span></span> |
| **\<open-in\><span data-ttu-id="9dac7-124">Keine oder nicht angegeben</span><span class="sxs-lookup"><span data-stu-id="9dac7-124">None or not specified</span></span>\</open-in\>** | <span data-ttu-id="9dac7-125">Öffnet die Website im Standardbrowser oder in dem Browser, in dem der Benutzer zu der Website navigiert.</span><span class="sxs-lookup"><span data-stu-id="9dac7-125">Opens the site in the default browser or in the browser where the user navigated to the site.</span></span> |
|**\<open-in\><span data-ttu-id="9dac7-126">Konfigurierbar</span><span class="sxs-lookup"><span data-stu-id="9dac7-126">Configurable</span></span>\</open-in\>** | <span data-ttu-id="9dac7-127">Ermöglicht der Website die Teilnahme an der Bestimmung der IE-Modus-Engine.</span><span class="sxs-lookup"><span data-stu-id="9dac7-127">Allows the site to participate in IE mode engine determination.</span></span> <span data-ttu-id="9dac7-128">Weitere Informationen hierzu finden Sie unter [Informationen zu konfigurierbaren Sites im IE-Modus](edge-learnmore-configurable-sites-ie-mode.md).</span><span class="sxs-lookup"><span data-stu-id="9dac7-128">To learn more, see [Learn about Configurable sites in IE mode](edge-learnmore-configurable-sites-ie-mode.md).</span></span>  |

>[!NOTE]
> <span data-ttu-id="9dac7-129">Das Attribut app=**„true”** wird nur erkannt, wenn es mit _'open-in' IE11_ verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="9dac7-129">The attribute app=**"true"** is only recognized when associated to _'open-in' IE11_.</span></span> <span data-ttu-id="9dac7-130">Durch das Hinzufügen zu den anderen 'open-in'-Elementen wird das Browserverhalten nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="9dac7-130">Adding it to the other 'open-in' elements won't change browser behavior.</span></span>   

## <span data-ttu-id="9dac7-131">Konfigurieren von neutralen Websites</span><span class="sxs-lookup"><span data-stu-id="9dac7-131">Configure neutral sites</span></span>

<span data-ttu-id="9dac7-132">Damit der IE-Modus ordnungsgemäß funktioniert, müssen Authentifizierungs- bzw. Single Sign-On-Server explizit als neutrale Websites konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="9dac7-132">In order for IE mode to work properly, authentication / Single Sign-On servers will need to be explicitly configured as neutral sites.</span></span> <span data-ttu-id="9dac7-133">Andernfalls versuchen die Seiten des IE-Modus, zu Microsoft Edge umzuleiten, und die Authentifizierung wird fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="9dac7-133">Otherwise, IE mode pages will try to redirect to Microsoft Edge, and authentication will fail.</span></span>

<span data-ttu-id="9dac7-134">Eine neutrale Website verwendet den Browser, in dem die Navigation begonnen wurde – entweder Microsoft Edge oder IE-Modus.</span><span class="sxs-lookup"><span data-stu-id="9dac7-134">A neutral site will use the browser where the navigation started - either Microsoft Edge or IE mode.</span></span> <span data-ttu-id="9dac7-135">Außerdem wird durch das Konfigurieren neutraler Websites sichergestellt, dass alle Anwendungen, die diese Authentifizierungsserver verwenden – sowohl moderne als auch ältere – weiterhin funktionsfähig sind.</span><span class="sxs-lookup"><span data-stu-id="9dac7-135">Configuring neutral sites ensures that all applications using these authentication servers, both modern and legacy, continue to work.</span></span>

<span data-ttu-id="9dac7-136">Sie können neutrale Websites konfigurieren, indem Sie im Enterprise Mode Site List Manager-Tool für *Öffnen mit* in der Dropdownliste "Keine" festlegen, oder indem Sie das Websitelisten-XML direkt aktualisieren:</span><span class="sxs-lookup"><span data-stu-id="9dac7-136">You can configure neutral sites by setting the *Open In* dropdown to 'None' in the Enterprise Mode Site List Manager tool or by directly updating the site list XML:</span></span>

``` xml
<site url="login.contoso.com">
   
    <open-in>None</open-in>

</site>
```

<span data-ttu-id="9dac7-137">Wenn Sie Authentifizierungsserver identifizieren möchten, überprüfen Sie den Netzwerkdatenverkehr einer Anwendung mithilfe der IE 11 Developer Tools.</span><span class="sxs-lookup"><span data-stu-id="9dac7-137">To identify authentication servers, inspect the network traffic from an application using the IE11 Developer Tools.</span></span> <span data-ttu-id="9dac7-138">Wenn Sie mehr Zeit zum Identifizieren Ihrer Authentifizierungsserver benötigen, können Sie eine Richtlinie konfigurieren, um alle seiteninternen Navigationen im IE-Modus zu halten.</span><span class="sxs-lookup"><span data-stu-id="9dac7-138">If you need more time to identify your authentication servers, you can configure a policy to keep all in-page navigation in IE mode.</span></span> <span data-ttu-id="9dac7-139">Um die Verwendung des IE-Modus zu minimieren, deaktivieren Sie diese Einstellung, sobald Sie Ihre Authentifizierungsserver identifiziert und der Siteliste hinzugefügt haben.</span><span class="sxs-lookup"><span data-stu-id="9dac7-139">To minimize the use of IE mode, disable this setting once you've identified and added your authentication servers to the site list.</span></span> <span data-ttu-id="9dac7-140">Weitere Informationen hierzu finden Sie unter [Konfigurieren Sie die seiteninterne Navigation so, dass sie im IE-Modus bleibt](https://docs.microsoft.com/deployedge/microsoft-edge-policies#internetexplorerintegrationsiteredirect).</span><span class="sxs-lookup"><span data-stu-id="9dac7-140">For more information, see [Configure in-page navigation to remain in IE mode](https://docs.microsoft.com/deployedge/microsoft-edge-policies#internetexplorerintegrationsiteredirect).</span></span>

>[!NOTE]
   ><span data-ttu-id="9dac7-141">Das Unternehmensmodusschema V.1 wird für die Integration des IE-Modus nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9dac7-141">Enterprise Mode schema v.1 isn't supported for IE mode integration.</span></span> <span data-ttu-id="9dac7-142">Wenn Sie derzeit SchemaV.1 mit Internet Explorer11 verwenden, müssen Sie ein Upgrade auf SchemaV.2 durchführen.</span><span class="sxs-lookup"><span data-stu-id="9dac7-142">If you are currently using schema v.1 with Internet Explorer 11, you must upgrade to schema v.2.</span></span> <span data-ttu-id="9dac7-143">Weitere Informationen finden Sie unter [Unternehmensmodusschema V.2-Richtlinien](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).</span><span class="sxs-lookup"><span data-stu-id="9dac7-143">For more information, see [Enterprise Mode schema v.2 guidance](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).</span></span>

## <span data-ttu-id="9dac7-144">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9dac7-144">See also</span></span>

- [<span data-ttu-id="9dac7-145">Microsoft Edge Enterprise-Angebotsseite</span><span class="sxs-lookup"><span data-stu-id="9dac7-145">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="9dac7-146">Informationen zum IE-Modus</span><span class="sxs-lookup"><span data-stu-id="9dac7-146">About IE mode</span></span>](https://docs.microsoft.com/deployedge/edge-ie-mode)
- [<span data-ttu-id="9dac7-147">Weitere Informationen zum Unternehmensmodus</span><span class="sxs-lookup"><span data-stu-id="9dac7-147">Additional Enterprise Mode information</span></span>](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)