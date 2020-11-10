---
title: Cookie-Weitergabe von Microsoft Edge an Internet Explorer
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 11/05/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 'Konfigurieren der Cookie-Weitergabe von Microsoft Edge an Internet Explorer '
ms.openlocfilehash: 5740a4ce31a240573b9106e7a20a5c44688aca0a
ms.sourcegitcommit: 2024629929044e2dcf146674058c1d6312c32e9a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2020
ms.locfileid: "11157541"
---
# <span data-ttu-id="5a898-103">Cookie-Weitergabe von Microsoft Edge an Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="5a898-103">Cookie sharing from Microsoft Edge to Internet Explorer</span></span>

<span data-ttu-id="5a898-104">In diesem Artikel wird erläutert, wie Sie die Weitergabe von Sitzungscookies von einem Microsoft Edge-Prozess an einen Internet Explorer-Prozess konfigurieren können, wenn der Internet Explorer-Modus verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5a898-104">This article explains explains how to configure session cookie sharing from a Microsoft Edge process to Internet Explorer process, while using Internet Explorer mode.</span></span>

> [!NOTE]
> <span data-ttu-id="5a898-105">Dieser Artikel bezieht sich auf Microsoft Edge Version 87 oder neuer.</span><span class="sxs-lookup"><span data-stu-id="5a898-105">This article applies to Microsoft Edge version 87 or later.</span></span>

## <span data-ttu-id="5a898-106">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="5a898-106">Prerequisites</span></span>

- <span data-ttu-id="5a898-107">Windows-Updates</span><span class="sxs-lookup"><span data-stu-id="5a898-107">Windows updates</span></span>

  - <span data-ttu-id="5a898-108">Windows10, Version2004, Windows Server, Version2004– KB4571744 oder höher</span><span class="sxs-lookup"><span data-stu-id="5a898-108">Windows 10 version 2004, Windows server version 2004 - KB4571744 or higher</span></span>
  - <span data-ttu-id="5a898-109">Windows10, Version1909, Windows Server, Version1909– KB4566116 oder höher</span><span class="sxs-lookup"><span data-stu-id="5a898-109">Windows 10 version 1909, Windows server version 1909 – KB4566116 or higher</span></span>
  - <span data-ttu-id="5a898-110">Windows10, Version1903, Windows Server, Version1903– KB4566116 oder höher</span><span class="sxs-lookup"><span data-stu-id="5a898-110">Windows 10 version 1903, Windows server version 1903 – KB4566116 or higher</span></span>
  - <span data-ttu-id="5a898-111">Windows10, Version1809, Windows Server, Version1809, und Windows Server2019– KB4571748 oder höher</span><span class="sxs-lookup"><span data-stu-id="5a898-111">Windows 10 version 1809, Windows Server version 1809, and Windows Server 2019 - KB4571748 or higher</span></span>
  - <span data-ttu-id="5a898-112">Windows10, Version1803– KB4577032 oder höher</span><span class="sxs-lookup"><span data-stu-id="5a898-112">Windows 10 version 1803 – KB4577032 or higher</span></span>

- <span data-ttu-id="5a898-113">Microsoft Edge, Version87 oder höher</span><span class="sxs-lookup"><span data-stu-id="5a898-113">Microsoft Edge version 87 or later</span></span>
- <span data-ttu-id="5a898-114">[IE-Modus](https://aka.ms/iemodeonedge)  konfiguriert mit Enterprise Mode Site List</span><span class="sxs-lookup"><span data-stu-id="5a898-114">[IE mode](https://aka.ms/iemodeonedge) configured with Enterprise Mode Site List</span></span>

## <span data-ttu-id="5a898-115">Übersicht</span><span class="sxs-lookup"><span data-stu-id="5a898-115">Overview</span></span>

<span data-ttu-id="5a898-116">Eine in großen Unternehmen häufige Konfiguration besteht darin, eine Anwendung, die in einem modernen Browser funktioniert, mit einer anderen Anwendung zu verknüpfen, welche für das Öffnen im Internet Explorer-Modus mit aktiviertem einmaligem Anmelden (SSO) als Teil des Workflows konfiguriert sein könnte.</span><span class="sxs-lookup"><span data-stu-id="5a898-116">A common configuration in large organizations is to have an application that works on a modern browser link to another application, which might be configured to open in Internet Explorer mode with Single Sign On (SSO) enabled as part of the workflow.</span></span>

<span data-ttu-id="5a898-117">Die Microsoft Edge- und Internet Explorer-Prozesse verwenden standardmäßig keine gemeinsamen Sitzungscookies, was in manchen Fällen nachteilig sein kann.</span><span class="sxs-lookup"><span data-stu-id="5a898-117">By default, the Microsoft Edge and Internet Explorer processes don't share session cookies, and this can be inconvenient in some cases.</span></span> <span data-ttu-id="5a898-118">Ein Benutzer muss sich beispielsweise im Internet Explorer-Modus erneut authentifizieren, und die Abmeldung von einer Microsoft Edge-Sitzung hat nicht automatisch die Abmeldung von der Sitzung im Internet Explorer-Modus zur Folge.</span><span class="sxs-lookup"><span data-stu-id="5a898-118">For example, when a user has to re-authenticate in Internet Explorer mode or when signing out of an Microsoft Edge session doesn’t sign out of the Internet Explorer mode session.</span></span> <span data-ttu-id="5a898-119">Für solche Szenarien können Sie bestimmte, für SSO festgelegte Cookies so konfigurieren, dass sie von Microsoft Edge an den Internet Explorer gesendet werden, um den Authentifizierungsablauf nahtloser zu gestalten, da auf diese Weise die Notwendigkeit einer erneuten Authentifizierung wegfällt.</span><span class="sxs-lookup"><span data-stu-id="5a898-119">In these scenarios, you can configure specific cookies set by SSO to be sent from Microsoft Edge to Internet Explorer so the authentication experience becomes more seamless by eliminating the need to re-authenticate.</span></span>

> [!NOTE]
> <span data-ttu-id="5a898-120">Sitzungscookies können nur von Microsoft Edge an Internet Explorer weitergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5a898-120">Session cookies can only be shared from Microsoft Edge to Internet Explorer.</span></span> <span data-ttu-id="5a898-121">Die Weitergabe von Sitzungscookies von Internet Explorer an Microsoft Edge ist nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="5a898-121">Sharing session cookies in reverse (from Internet Explorer to Microsoft Edge) isn't possible.</span></span>

## <span data-ttu-id="5a898-122">Funktionsweise der Cookie-Weitergabe</span><span class="sxs-lookup"><span data-stu-id="5a898-122">How cookie sharing works</span></span>

<span data-ttu-id="5a898-123">Die Enterprise Mode Site List-XML-Datei wurde erweitert, damit zusätzliche Elemente Cookies angeben können, die von einer Microsoft Edge-Sitzung an Internet Explorer weitergegeben werden müssen.</span><span class="sxs-lookup"><span data-stu-id="5a898-123">The Enterprise Mode site list XML has been extended to allow additional elements to specify cookies that need to be shared from a Microsoft Edge session with Internet Explorer.</span></span>  

<span data-ttu-id="5a898-124">Wenn während einer Microsoft Edge-Sitzung zum ersten Mal ein Internet Explorer-Modus-Tab erstellt wird, werden alle übereinstimmenden Cookies an die Internet Explorer-Sitzung weitergegeben.</span><span class="sxs-lookup"><span data-stu-id="5a898-124">The first time an Internet Explorer mode tab is created in a Microsoft Edge session, all matching cookies are shared to the Internet Explorer session.</span></span> <span data-ttu-id="5a898-125">Anschließend wird jedes Mal, wenn ein Cookie, das einer Regel entspricht, hinzugefügt, gelöscht oder geändert wird, dieses als Update an die Internet Explorer-Sitzung weitergegeben.</span><span class="sxs-lookup"><span data-stu-id="5a898-125">Subsequently, any time a cookie that matches a rule is added, deleted, or modified it is sent as an update to the Internet Explorer session.</span></span> <span data-ttu-id="5a898-126">Wenn die Websiteliste aktualisiert wird, werden die weitergegebenen Cookies ebenfalls neu ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="5a898-126">The set of shared cookies is also re-evaluated when the site list is updated.</span></span>

### <span data-ttu-id="5a898-127">Aktualisierte Schemaelemente</span><span class="sxs-lookup"><span data-stu-id="5a898-127">Updated schema elements</span></span>

<span data-ttu-id="5a898-128">In der folgenden Tabelle wird das \<shared-cookie\>-Element beschrieben, das zur Unterstützung der Cookie-Weitergabe hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="5a898-128">The following table describes the \<shared-cookie\> element added to support the cookie sharing feature.</span></span>

| <span data-ttu-id="5a898-129">Element</span><span class="sxs-lookup"><span data-stu-id="5a898-129">Element</span></span>| <span data-ttu-id="5a898-130">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5a898-130">Description</span></span> |
|-|-|
| \<shared-cookie **domain**=".contoso.com" **name**="cookie1"\>\</shared-cookie\><br><br><span data-ttu-id="5a898-131">ODER</span><span class="sxs-lookup"><span data-stu-id="5a898-131">OR</span></span><br><br>\<shared-cookie **host**="subdomain.contoso.com" **name**="cookie2"\>\</shared-cookie\>   |<span data-ttu-id="5a898-132">**(Erforderlich)** Ein \<shared-cookie\>-Element erfordert mindestens ein *domain*-Attribut (für Domänen-Cookies) oder ein *host*-Attribut (für Nur-Host-Cookies) sowie ein *name*-Attribut.</span><span class="sxs-lookup"><span data-stu-id="5a898-132">**(Required)** A \<shared-cookie\> element requires, at minimum, a *domain* (for domain cookies) or a *host* (for host-only cookies) attribute and a *name* attribute.</span></span><br><span data-ttu-id="5a898-133">Diese müssen jeweils exakt mit der Domäne bzw. mit dem Namen des Cookies übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="5a898-133">These must be exact matches to the cookie's domain and name respectively.</span></span> <span data-ttu-id="5a898-134">**Beachten Sie**, dass es bei Unterdomänen keine Übereinstimmung gibt.</span><span class="sxs-lookup"><span data-stu-id="5a898-134">**Note** that subdomains do not match.</span></span><br><br><span data-ttu-id="5a898-135">Das *domain*-Attribut wird für Domänen-Cookies verwendet (ein vorangestellter Punkt ist dabei zulässig, aber optional).</span><span class="sxs-lookup"><span data-stu-id="5a898-135">The *domain* attribute is used for domain cookies (and a leading dot is allowed but optional).</span></span><br><span data-ttu-id="5a898-136">Das *host*-Attribut wird für Nur-Host-Cookies verwendet (ein vorangestellter Punkt ist dabei ein Fehler).</span><span class="sxs-lookup"><span data-stu-id="5a898-136">The *host* attribute is used for host-only cookies (and a leading dot is an error).</span></span> <span data-ttu-id="5a898-137">Wenn Sie keine oder beide Optionen angeben, hat dies einen Fehler zur Folge.</span><span class="sxs-lookup"><span data-stu-id="5a898-137">Specifying neither or both will result in an error.</span></span><br><span data-ttu-id="5a898-138">\* Bei einem Cookie handelt es sich um ein Domänen-Cookie, wenn in der Cookie-Zeichenfolge eine Domäne angegeben wurde (über den HTTP-Set-Cookie-Antwortheader oder die "document.cokie JS"-API).</span><span class="sxs-lookup"><span data-stu-id="5a898-138">\* A cookie is a domain cookie if a domain was specified in the cookie string (via HTTP Set-Cookie response header or document.cookie JS API).</span></span> <span data-ttu-id="5a898-139">Ein Domänen-Cookie gilt für die angegebene Domäne und alle Unterdomänen.</span><span class="sxs-lookup"><span data-stu-id="5a898-139">A domain cookie applies to the specified domain and all subdomains.</span></span> <span data-ttu-id="5a898-140">Wenn in der Cookie-Zeichenfolge keine Domäne angegeben wurde, handelt es sich bei dem Cookie um ein Nur-Host-Cookie, das nur für den Host gilt, für den es festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="5a898-140">If a domain was not specified in the cookie string, the cookie is a host-only cookie and only applies to the specific host that it was set for.</span></span> <span data-ttu-id="5a898-141">Beachten Sie, dass einige Klassen von URLs wie etwa Einzelwort-Hostnamen (z. B. http://intranetsite) und IP-Adressen (z. B. http://10.0.0.1) ausschließlich Nur-Host-Cookies festlegen können.</span><span class="sxs-lookup"><span data-stu-id="5a898-141">Note that some classes of URLs such as single-word hostnames (e.g. http://intranetsite) and IP addresses (e.g. http://10.0.0.1) can only set host-only cookies.</span></span>    |
| \<shared-cookie **host**="subdomain.contoso.com" **name**="cookie2" **path**="/a/b/c"\>\</shared-cookie\>  | <span data-ttu-id="5a898-142">**(Optional)** Es kann ein *path*-Attribut angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5a898-142">**(Optional)** A *path* attribute may be specified.</span></span> <span data-ttu-id="5a898-143">Wenn kein path-Attribut angegeben wird (oder es leer ist), entsprechen alle Cookies, die mit Domain/Host und Name übereinstimmen, der Richtlinie, und das unabhängig vom Pfad (Platzhalterregel).</span><span class="sxs-lookup"><span data-stu-id="5a898-143">If no path attribute is specified (or if the path attribute is empty), any cookies matching domain/host and name match the policy, regardless of path (wildcard rule).</span></span><br><br><span data-ttu-id="5a898-144">Bei Angabe eines Pfads muss es sich um eine exakte Übereinstimmung handeln.</span><span class="sxs-lookup"><span data-stu-id="5a898-144">If a path is specified, it must be an exact match.</span></span><br><span data-ttu-id="5a898-145">Wenn ein Cookie einer Regel mit einem Pfad entspricht, hat dies Vorrang vor einer Regel ohne Pfad.</span><span class="sxs-lookup"><span data-stu-id="5a898-145">If a cookie matches a rule with a path, that takes precedence over a rule without a path.</span></span> |

#### <span data-ttu-id="5a898-146">Weitergabe-Beispiel</span><span class="sxs-lookup"><span data-stu-id="5a898-146">Sharing example</span></span>

```xml
<site-list version="1">
<shared-cookie domain=".contoso.com" name="cookie1"></shared-cookie> 
<shared-cookie host="subdomain.contoso.com" name="cookie2" path="/a/b/c">
</shared-cookie>
</site-list>
```

## <span data-ttu-id="5a898-147">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5a898-147">See also</span></span>

- [<span data-ttu-id="5a898-148">Informationen zum IE-Modus</span><span class="sxs-lookup"><span data-stu-id="5a898-148">About IE mode</span></span>](https://docs.microsoft.com/deployedge/edge-ie-mode)
- [<span data-ttu-id="5a898-149">Informationen zu konfigurierbaren Websites</span><span class="sxs-lookup"><span data-stu-id="5a898-149">Configurable sites information</span></span>](https://docs.microsoft.com/deployedge/edge-learnmore-configurable-sites-ie-mode)
- [<span data-ttu-id="5a898-150">Weitere Informationen zum Unternehmensmodus</span><span class="sxs-lookup"><span data-stu-id="5a898-150">Additional Enterprise Mode information</span></span>](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [<span data-ttu-id="5a898-151">Angebotsseite für Microsoft Edge für Unternehmen</span><span class="sxs-lookup"><span data-stu-id="5a898-151">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
