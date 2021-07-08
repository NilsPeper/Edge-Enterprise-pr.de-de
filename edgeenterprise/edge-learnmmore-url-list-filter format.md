---
title: Filterformat für Microsoft Edge-URL-Richtlinien
ms.author: brianalt
author: dan-wesley
manager: srugh
ms.date: 05/01/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Hier finden Sie Informationen zum Filterformat, das für Microsoft Edge URLBlocklist- und URLAllowlist-Richtlinien verwendet wird.
ms.openlocfilehash: 94378a9193269c73a7439dd019d6cb2d6ac547df
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2021
ms.locfileid: "11617265"
---
# <a name="filter-format-for-url-list-based-policies"></a><span data-ttu-id="d7236-103">Filterformat für URL-listenbasierte Richtlinien</span><span class="sxs-lookup"><span data-stu-id="d7236-103">Filter format for URL list-based policies</span></span>

<span data-ttu-id="d7236-104">In diesem Artikel wird das Filterformat beschrieben, das für die Microsoft Edge URL-listenbasierten Richtlinien verwendet wird (zum Beispiel Richtlinien für [URLBlocklist](microsoft-edge-policies.md#urlblocklist), [URLAllowList](microsoft-edge-policies.md#urlallowlist) und [CertificateTransparencyEnforcementDisabledForUrls](microsoft-edge-policies.md#certificatetransparencyenforcementdisabledforurls).</span><span class="sxs-lookup"><span data-stu-id="d7236-104">This article describes the filter format used for the Microsoft Edge URL list-based policies (For example, [URLBlocklist](microsoft-edge-policies.md#urlblocklist), [URLAllowList](microsoft-edge-policies.md#urlallowlist), and [CertificateTransparencyEnforcementDisabledForUrls](microsoft-edge-policies.md#certificatetransparencyenforcementdisabledforurls) policies.</span></span>

> [!NOTE]
> <span data-ttu-id="d7236-105">Dieser Artikel bezieht sich auf Microsoft Edge Version 77 oder höher.</span><span class="sxs-lookup"><span data-stu-id="d7236-105">This article applies to Microsoft Edge version 77 or later.</span></span>

## <a name="the-filter-format"></a><span data-ttu-id="d7236-106">Das Filterformat</span><span class="sxs-lookup"><span data-stu-id="d7236-106">The filter format</span></span>

<span data-ttu-id="d7236-107">Das Filterformat ist:</span><span class="sxs-lookup"><span data-stu-id="d7236-107">The filter format is:</span></span>

```
    [scheme://][.]host[:port][/path][@query]
```

<span data-ttu-id="d7236-108">Die Felder im Filterformat sind:</span><span class="sxs-lookup"><span data-stu-id="d7236-108">The fields in the filter format are:</span></span>

| <span data-ttu-id="d7236-109">Feld</span><span class="sxs-lookup"><span data-stu-id="d7236-109">Field</span></span> | <span data-ttu-id="d7236-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d7236-110">Description</span></span> |
| --- | --- |
| <span data-ttu-id="d7236-111">**Schema** (*optional*)</span><span class="sxs-lookup"><span data-stu-id="d7236-111">**scheme** (*optional*)</span></span> | <span data-ttu-id="d7236-112">Dabei kann es sich um http://, https://, FTP://, edge:// usw. handeln.</span><span class="sxs-lookup"><span data-stu-id="d7236-112">It can be http://, https://, ftp://, edge://, etc.</span></span> |
| <span data-ttu-id="d7236-113">**Host** (*erforderlich*)</span><span class="sxs-lookup"><span data-stu-id="d7236-113">**host** (*required*)</span></span> | <span data-ttu-id="d7236-114">Es muss sich um einen gültigen Hostnamen handeln und Sie können einen Platzhalter ("\*") verwenden.</span><span class="sxs-lookup"><span data-stu-id="d7236-114">It must be a valid host name and you can use a wildcard ("\*").</span></span> <span data-ttu-id="d7236-115">Um den Unterdomänenabgleich zu deaktivieren, fügen Sie vor dem **Host** einen optionalen Punkt (".") ein.</span><span class="sxs-lookup"><span data-stu-id="d7236-115">To disable subdomain matching, include an optional dot (".") before **host**.</span></span> <span data-ttu-id="d7236-116">Es kann ein einzelner IP-Adressliteral-Hostname angegeben werden, aber Platzhalter werden für einen IP-Adressliteral-Hostnamen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d7236-116">A single IP Address Literal hostname may be specified, but wildcarding is not supported for an IP Address Literal hostname.</span></span> |
| <span data-ttu-id="d7236-117">**Port** (*optional*)</span><span class="sxs-lookup"><span data-stu-id="d7236-117">**port** (*optional*)</span></span> | <span data-ttu-id="d7236-118">Gültige Werte liegen zwischen 1 und 65535.</span><span class="sxs-lookup"><span data-stu-id="d7236-118">Valid values range from 1 to 65535.</span></span> |
| <span data-ttu-id="d7236-119">**Pfad** (*optional*)</span><span class="sxs-lookup"><span data-stu-id="d7236-119">**path** (*optional*)</span></span> | <span data-ttu-id="d7236-120">Sie können eine beliebige Zeichenfolge im Pfad verwenden.</span><span class="sxs-lookup"><span data-stu-id="d7236-120">You can use any string in the path.</span></span> |
| <span data-ttu-id="d7236-121">**Abfrage** (*optional*)</span><span class="sxs-lookup"><span data-stu-id="d7236-121">**query** (*optional*)</span></span> | <span data-ttu-id="d7236-122">Bei der **Abfrage** handelt es sich entweder um einen Schlüsselwert oder ein Nur-Schlüssel-Token, die durch ein kaufmännisches Und-Zeichen("&") getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="d7236-122">The **query** is either key-value or key-only tokens separated by an ampersand ("&").</span></span> <span data-ttu-id="d7236-123">Trennen Sie Schlüsselwert-Token mit einem Gleichheitszeichen ("=").</span><span class="sxs-lookup"><span data-stu-id="d7236-123">Separate key-value tokens with an equal sign ("=").</span></span> <span data-ttu-id="d7236-124">Um eine Präfixübereinstimmung anzugeben, können Sie am Ende der **Abfrage** ein Sternchen ("\*") verwenden.</span><span class="sxs-lookup"><span data-stu-id="d7236-124">To indicate a prefix match, you can use an asterisk ("\*") at the end of the **query**.</span></span> |

## <a name="comparing-the-filter-format-to-the-url-format"></a><span data-ttu-id="d7236-125">Vergleichen des Filterformats mit dem URL-Format</span><span class="sxs-lookup"><span data-stu-id="d7236-125">Comparing the filter format to the URL format</span></span>

<span data-ttu-id="d7236-126">Das Filterformat ähnelt dem URL-Format mit Ausnahme der folgenden Unterschiede:</span><span class="sxs-lookup"><span data-stu-id="d7236-126">The filter format resembles the URL format, except for the following differences:</span></span>

- <span data-ttu-id="d7236-127">Wenn Sie "user:pass" angeben, wird es ignoriert.</span><span class="sxs-lookup"><span data-stu-id="d7236-127">If you include "user:pass", it will be ignored.</span></span> <span data-ttu-id="d7236-128">Beispiel: http://user:pass@ftp.contoso.com/pub/example.iso.</span><span class="sxs-lookup"><span data-stu-id="d7236-128">For example, http://user:pass@ftp.contoso.com/pub/example.iso.</span></span>
- <span data-ttu-id="d7236-129">Wenn Sie einen Fragmentbezeichner ("#") einfügen, wird dieser und alles, was auf den Bezeichner folgt, ignoriert.</span><span class="sxs-lookup"><span data-stu-id="d7236-129">If you include a fragment identifier ("#"), it and everything that follows the identifier is ignored.</span></span>
- <span data-ttu-id="d7236-130">Sie können einen Platzhalter ("\*") als **Host** verwenden und ihm einen Punkt (".") voranstellen.</span><span class="sxs-lookup"><span data-stu-id="d7236-130">You can use a wildcard ("\*") as the **host** and you can prefix it with a dot (".").</span></span>
- <span data-ttu-id="d7236-131">Sie können einen Schrägstrich (/") oder einen Punkt (".") als Suffix für den **Host** verwenden.</span><span class="sxs-lookup"><span data-stu-id="d7236-131">You can use a forward slash ("/") or a dot (".") as a suffix for the **host**.</span></span> <span data-ttu-id="d7236-132">In diesem Fall wird das Suffix ignoriert.</span><span class="sxs-lookup"><span data-stu-id="d7236-132">In this case, the suffix is ignored.</span></span>

## <a name="filter-selection-criteria"></a><span data-ttu-id="d7236-133">Kriterien für die Filterauswahl</span><span class="sxs-lookup"><span data-stu-id="d7236-133">Filter selection criteria</span></span>

<span data-ttu-id="d7236-134">Der für eine URL ausgewählte Filter ist die spezifischste Übereinstimmung, die nach Verarbeitung der folgenden Filterauswahlregeln gefunden wurde:</span><span class="sxs-lookup"><span data-stu-id="d7236-134">The filter selected for a URL is the most specific match found after processing the following filter selection rules:</span></span>

1. <span data-ttu-id="d7236-135">Filter mit der längsten **Host**-Übereinstimmung werden zuerst ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="d7236-135">Filters with the longest **host** match are selected first.</span></span>
2. <span data-ttu-id="d7236-136">Aus den ausgewählten Filtern werden alle Filter mit einem nicht übereinstimmenden Schema oder Port verworfen.</span><span class="sxs-lookup"><span data-stu-id="d7236-136">From the selected filters, any filter with a non-matching scheme or port is discarded.</span></span>
3. <span data-ttu-id="d7236-137">Aus den verbleibenden Filtern wird der Filter mit dem längsten übereinstimmenden **Pfad** ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="d7236-137">From the remaining filters, the filter with the longest matching **path** is selected.</span></span>
4. <span data-ttu-id="d7236-138">Aus den verbleibenden Filtern wird der Filter mit dem längsten Satz von Abfragetoken ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="d7236-138">From the remaining filters, the filter with the longest set of query tokens is selected.</span></span> <span data-ttu-id="d7236-139">In diesem Schritt hat der Zulassungslistenfilter Vorrang vor dem Sperrlistenfilter, wenn beide Filter die gleiche **Pfadlänge** und Anzahl von **Abfragetoken** aufweisen.</span><span class="sxs-lookup"><span data-stu-id="d7236-139">At this step, the allow list filter takes precedence over the block list filter if both filters have the same **path** length and number of **query** tokens.</span></span>
5. <span data-ttu-id="d7236-140">Wenn kein gültiger Filter mehr vorhanden ist, wird die Subdomäne ganz links vom **Host** entfernt, und der Auswahlprozess beginnt bei Schritt 1 von vorne.</span><span class="sxs-lookup"><span data-stu-id="d7236-140">If there's no valid filter remaining, then the left-most subdomain is removed from **host** and the selection process starts over at step 1.</span></span> <span data-ttu-id="d7236-141">Der **Host** mit dem speziellen Sternchen ("\*") ist der zuletzt gesuchte Host, der mit allen Hosts übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="d7236-141">The special asterisk ("\*") **host** is the last searched and it matches all hosts.</span></span>
6. <span data-ttu-id="d7236-142">Wenn ein Filter verfügbar ist, wird die URL-Anforderung blockiert oder zugelassen.</span><span class="sxs-lookup"><span data-stu-id="d7236-142">If a filter's available, it blocks or allows the URL request.</span></span>

   >[!NOTE]
   ><span data-ttu-id="d7236-143">Das Standardverhalten besteht darin, die URL-Anforderung zuzulassen, wenn keine Übereinstimmung mit einem Filter vorliegt.</span><span class="sxs-lookup"><span data-stu-id="d7236-143">The default behavior is to allow the URL request if no filter is matched.</span></span>

## <a name="example-filter-selection-criteria"></a><span data-ttu-id="d7236-144">Beispiel für Kriterien für die Filterauswahl</span><span class="sxs-lookup"><span data-stu-id="d7236-144">Example filter selection criteria</span></span>

<span data-ttu-id="d7236-145">In diesem Beispiel führt die Filterauswahl bei der Suche nach einer Übereinstimmung mit "https://sub.contoso.com/docs" Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="d7236-145">In this example, when searching for a match to "https://sub.contoso.com/docs" the filter selection will:</span></span>

1. <span data-ttu-id="d7236-146">Suchen nach einem Filter für „sub.contoso.com”.</span><span class="sxs-lookup"><span data-stu-id="d7236-146">Search for a filter for "sub.contoso.com".</span></span> <span data-ttu-id="d7236-147">Wenn ein Filter gefunden wird, wird die Suche mit Schritt 2 fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="d7236-147">If it finds a filter, the search moves to step 2.</span></span> <span data-ttu-id="d7236-148">Wenn ein Filter nicht gefunden wird, wird die Suche erneut mit "contoso.com", "com" und schließlich "" versucht.</span><span class="sxs-lookup"><span data-stu-id="d7236-148">If a filter isn't found, then it tries again with "contoso.com", "com", and finally "".</span></span>
2. <span data-ttu-id="d7236-149">Aus den ausgewählten Filtern werden alle, die im **Schema** nicht über "http" verfügen, entfernt.</span><span class="sxs-lookup"><span data-stu-id="d7236-149">From the selected filters, any that don't have "http" in the **scheme** are removed.</span></span>
3. <span data-ttu-id="d7236-150">Aus den verbleibenden Filtern werden alle, die über eine genaue Portnummer verfügen, die nicht "80" ist, entfernt.</span><span class="sxs-lookup"><span data-stu-id="d7236-150">From the remaining filters, any that have an exact port number that isn't "80" are removed.</span></span>
4. <span data-ttu-id="d7236-151">Aus den übrigen Filtern werden alle, die nicht „/docs” als Präfix des **Pfads** haben, entfernt.</span><span class="sxs-lookup"><span data-stu-id="d7236-151">From the remaining filters, any that don't have "/docs" as a prefix of the **path** are removed.</span></span>
5. <span data-ttu-id="d7236-152">Aus den verbleibenden Filtern wird der Filter mit dem längsten Pfadpräfix ausgewählt und angewendet.</span><span class="sxs-lookup"><span data-stu-id="d7236-152">From the remaining filters, the filter with the longest path prefix is selected and applied.</span></span> <span data-ttu-id="d7236-153">Wird kein Filter gefunden, beginnt der Auswahlprozess erneut bei Schritt 1.</span><span class="sxs-lookup"><span data-stu-id="d7236-153">If a filter isn't found, the selection process starts over again at step 1.</span></span> <span data-ttu-id="d7236-154">Der Prozess wird mit der nächsten Unterdomäne wiederholt.</span><span class="sxs-lookup"><span data-stu-id="d7236-154">The process is repeated with the next subdomain.</span></span>

### <a name="additional-filter-information"></a><span data-ttu-id="d7236-155">Zusätzliche Filterinformationen</span><span class="sxs-lookup"><span data-stu-id="d7236-155">Additional filter information</span></span>

<span data-ttu-id="d7236-156">Wenn ein Filter einen Punkt (".") enthält, der dem **Host** vorangestellt ist, werden nur exakte **Host-Übereinstimmungen** gefiltert.</span><span class="sxs-lookup"><span data-stu-id="d7236-156">If a filter has a dot (".") prefixing the **host** then only exact **host** matches are filtered.</span></span> <span data-ttu-id="d7236-157">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="d7236-157">For example:</span></span>

- <span data-ttu-id="d7236-158">"contoso.com" (kein Punkt) stimmt mit "contoso.com", "www.contoso.com" und "sub.www.contoso.com" überein.</span><span class="sxs-lookup"><span data-stu-id="d7236-158">"contoso.com" (no dot) will match "contoso.com", "www.contoso.com", and "sub.www.contoso.com"</span></span>
- <span data-ttu-id="d7236-159">".www.contoso.com" (mit einem Punkt als Präfix) stimmt nur mit "www.contoso.com" überein.</span><span class="sxs-lookup"><span data-stu-id="d7236-159">".www.contoso.com" (with a dot prefix) will only match "www.contoso.com"</span></span>

<span data-ttu-id="d7236-160">Sie können entweder ein Standardschema oder ein benutzerdefiniertes **Schema**verwenden.</span><span class="sxs-lookup"><span data-stu-id="d7236-160">You can use either a standard or custom **schema**.</span></span> <span data-ttu-id="d7236-161">Unterstützte Standardschemata sind:</span><span class="sxs-lookup"><span data-stu-id="d7236-161">Supported standard schemas include:</span></span>

- <span data-ttu-id="d7236-162">_about_, _blob_, _content_, _edge_, _cid_, _data_, _file_, _filesystem_, _ftp_, _gopher_, _http_, _https_, _javascript_, _mailto_, _ws_, und _wss_.</span><span class="sxs-lookup"><span data-stu-id="d7236-162">_about_, _blob_, _content_, _edge_, _cid_, _data_, _file_, _filesystem_, _ftp_, _gopher_, _http_, _https_, _javascript_, _mailto_, _ws_, and _wss_.</span></span>

<span data-ttu-id="d7236-163">Jedes andere **Schema** wird als benutzerdefiniertes **Schema** behandelt, wobei nur die Muster _Schema:\*_ und _schema://\*_ zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="d7236-163">Any other **schema** is treated as a custom **schema**, but only the _schema:\*_ and _schema://\*_ patterns are allowed.</span></span> <span data-ttu-id="d7236-164">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="d7236-164">For example:</span></span>

- <span data-ttu-id="d7236-165">"custom:\*" oder "custom://\*" entspricht "custom:app".</span><span class="sxs-lookup"><span data-stu-id="d7236-165">"custom:\*" or "custom://\*" will match "custom:app"</span></span>
- <span data-ttu-id="d7236-166">"custom:app" bzw. "custom://app" sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="d7236-166">"custom:app" or "custom://app" are invalid</span></span>

<span data-ttu-id="d7236-167">Bei **Schema** und **Host** wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="d7236-167">**schema** and **host** aren't case-sensitive.</span></span> <span data-ttu-id="d7236-168">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="d7236-168">For example:</span></span>

- <span data-ttu-id="d7236-169">Der Filter "http://contoso.com" stimmt mit "HTTP://contoso.com", "http://contoso.COM" und "http://contoso.com" überein.</span><span class="sxs-lookup"><span data-stu-id="d7236-169">"http://contoso.com" filter matches "HTTP://contoso.com", "http://contoso.COM", and "http://contoso.com"</span></span>

<span data-ttu-id="d7236-170">Bei **Pfad** und **Abfrage** wird die Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="d7236-170">**path** and **query** are case-sensitive.</span></span> <span data-ttu-id="d7236-171">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="d7236-171">For example:</span></span>

- <span data-ttu-id="d7236-172">Der Filter "http://contoso.com/path?query=A" stimmt weder mit "http://contoso.com/Path?query=A" noch mit "http://contoso.com/path?Query=A" überein.</span><span class="sxs-lookup"><span data-stu-id="d7236-172">"http://contoso.com/path?query=A" filter doesn't match "http://contoso.com/Path?query=A" or "http://contoso.com/path?Query=A".</span></span> <span data-ttu-id="d7236-173">Er stimmt mit "http://contoso.COM/path?query=A" überein.</span><span class="sxs-lookup"><span data-stu-id="d7236-173">It does match "http://contoso.COM/path?query=A".</span></span>

## <a name="content-license"></a><span data-ttu-id="d7236-174">Lizenz für Inhalte</span><span class="sxs-lookup"><span data-stu-id="d7236-174">Content license</span></span>

> [!NOTE]
> <span data-ttu-id="d7236-175">Teile dieser Seite sind Änderungen, die auf von Chromium.org erstellten und freigegebenen Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/) beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d7236-175">Portions of this page are modifications based on work created and shared by Chromium.org and used according to terms described in the [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/).</span></span> <span data-ttu-id="d7236-176">Die Originalseite von [Chromium finden Sie hier](https://www.chromium.org/administrators/url-blacklist-filter-format).</span><span class="sxs-lookup"><span data-stu-id="d7236-176">The original [Chromium page can be found here](https://www.chromium.org/administrators/url-blacklist-filter-format).</span></span>
  
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br /><span data-ttu-id="d7236-177">Diese Arbeit unterliegt einer <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.</span><span class="sxs-lookup"><span data-stu-id="d7236-177">This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.</span></span>

## <a name="see-also"></a><span data-ttu-id="d7236-178">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d7236-178">See also</span></span>

- [<span data-ttu-id="d7236-179">Microsoft Edge Enterprise-Angebotsseite</span><span class="sxs-lookup"><span data-stu-id="d7236-179">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
