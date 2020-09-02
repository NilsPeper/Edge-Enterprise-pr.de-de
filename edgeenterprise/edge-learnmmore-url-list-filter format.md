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
ms.openlocfilehash: 5a0eff1ca7be17fccd1087716d426b13ea302847
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979985"
---
# <span data-ttu-id="f6dd0-103">Filterformat für URL-listenbasierte Richtlinien</span><span class="sxs-lookup"><span data-stu-id="f6dd0-103">Filter format for URL list-based policies</span></span>

<span data-ttu-id="f6dd0-104">In diesem Artikel wird das Filterformat beschrieben, das für die Microsoft Edge URL-listenbasierten Richtlinien verwendet wird (zum Beispiel Richtlinien für [URLBlocklist](microsoft-edge-policies.md#urlblocklist), [URLAllowList](microsoft-edge-policies.md#urlallowlist) und [CertificateTransparencyEnforcementDisabledForUrls](microsoft-edge-policies.md#certificatetransparencyenforcementdisabledforurls).</span><span class="sxs-lookup"><span data-stu-id="f6dd0-104">This article describes the filter format used for the Microsoft Edge URL list-based policies (For example, [URLBlocklist](microsoft-edge-policies.md#urlblocklist), [URLAllowList](microsoft-edge-policies.md#urlallowlist), and [CertificateTransparencyEnforcementDisabledForUrls](microsoft-edge-policies.md#certificatetransparencyenforcementdisabledforurls) policies.</span></span>

> [!NOTE]
> <span data-ttu-id="f6dd0-105">Dieser Artikel bezieht sich auf Microsoft Edge Version 77 oder höher.</span><span class="sxs-lookup"><span data-stu-id="f6dd0-105">This article applies to Microsoft Edge version 77 or later.</span></span>

## <span data-ttu-id="f6dd0-106">Das Filterformat</span><span class="sxs-lookup"><span data-stu-id="f6dd0-106">The filter format</span></span>

<span data-ttu-id="f6dd0-107">Das Filterformat ist:</span><span class="sxs-lookup"><span data-stu-id="f6dd0-107">The filter format is:</span></span>

```
    [scheme://][.]host[:port][/path][@query]
```

<span data-ttu-id="f6dd0-108">Die Felder im Filterformat sind:</span><span class="sxs-lookup"><span data-stu-id="f6dd0-108">The fields in the filter format are:</span></span>

| <span data-ttu-id="f6dd0-109">Feld</span><span class="sxs-lookup"><span data-stu-id="f6dd0-109">Field</span></span> | <span data-ttu-id="f6dd0-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f6dd0-110">Description</span></span> |
| --- | --- |
| <span data-ttu-id="f6dd0-111">**Schema** (*optional*)</span><span class="sxs-lookup"><span data-stu-id="f6dd0-111">**scheme** (*optional*)</span></span> | <span data-ttu-id="f6dd0-112">Dabei kann es sich um http://, https://, FTP://, edge:// usw. handeln.</span><span class="sxs-lookup"><span data-stu-id="f6dd0-112">It can be http://, https://, ftp://, edge://, etc.</span></span> |
| <span data-ttu-id="f6dd0-113">**Host** (*erforderlich*)</span><span class="sxs-lookup"><span data-stu-id="f6dd0-113">**host** (*required*)</span></span> | <span data-ttu-id="f6dd0-114">Es muss ein gültiger Hostname oder eine gültige IP-Adresse sein, und Sie können einen Platzhalter ("\*") verwenden.</span><span class="sxs-lookup"><span data-stu-id="f6dd0-114">It must be a valid host name or IP address and you can use a wildcard ("\*").</span></span> <span data-ttu-id="f6dd0-115">Um den Unterdomänenabgleich zu deaktivieren, fügen Sie vor dem **Host** einen optionalen Punkt (".") ein.</span><span class="sxs-lookup"><span data-stu-id="f6dd0-115">To disable subdomain matching, include an optional dot (".") before **host**.</span></span> |
| <span data-ttu-id="f6dd0-116">**Port** (*optional*)</span><span class="sxs-lookup"><span data-stu-id="f6dd0-116">**port** (*optional*)</span></span> | <span data-ttu-id="f6dd0-117">Gültige Werte liegen zwischen 1 und 65535.</span><span class="sxs-lookup"><span data-stu-id="f6dd0-117">Valid values range from 1 to 65535.</span></span> |
| <span data-ttu-id="f6dd0-118">**Pfad** (*optional*)</span><span class="sxs-lookup"><span data-stu-id="f6dd0-118">**path** (*optional*)</span></span> | <span data-ttu-id="f6dd0-119">Sie können eine beliebige Zeichenfolge im Pfad verwenden.</span><span class="sxs-lookup"><span data-stu-id="f6dd0-119">You can use any string in the path.</span></span> |
| <span data-ttu-id="f6dd0-120">**Abfrage** (*optional*)</span><span class="sxs-lookup"><span data-stu-id="f6dd0-120">**query** (*optional*)</span></span> | <span data-ttu-id="f6dd0-121">Bei der **Abfrage** handelt es sich entweder um einen Schlüsselwert oder ein Nur-Schlüssel-Token, die durch ein kaufmännisches Und-Zeichen("&") getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="f6dd0-121">The **query** is either key-value or key-only tokens separated by an ampersand ("&").</span></span> <span data-ttu-id="f6dd0-122">Trennen Sie Schlüsselwert-Token mit einem Gleichheitszeichen ("=").</span><span class="sxs-lookup"><span data-stu-id="f6dd0-122">Separate key-value tokens with an equal sign ("=").</span></span> <span data-ttu-id="f6dd0-123">Um eine Präfixübereinstimmung anzugeben, können Sie am Ende der **Abfrage** ein Sternchen ("\*") verwenden.</span><span class="sxs-lookup"><span data-stu-id="f6dd0-123">To indicate a prefix match, you can use an asterisk ("\*") at the end of the **query**.</span></span> |

## <span data-ttu-id="f6dd0-124">Vergleichen des Filterformats mit dem URL-Format</span><span class="sxs-lookup"><span data-stu-id="f6dd0-124">Comparing the filter format to the URL format</span></span>

<span data-ttu-id="f6dd0-125">Das Filterformat ähnelt dem URL-Format mit Ausnahme der folgenden Unterschiede:</span><span class="sxs-lookup"><span data-stu-id="f6dd0-125">The filter format resembles the URL format, except for the following differences:</span></span>

- <span data-ttu-id="f6dd0-126">Wenn Sie "user:pass" angeben, wird es ignoriert.</span><span class="sxs-lookup"><span data-stu-id="f6dd0-126">If you include "user:pass", it will be ignored.</span></span> <span data-ttu-id="f6dd0-127">Beispiel: http://user:pass@ftp.contoso.com/pub/example.iso.</span><span class="sxs-lookup"><span data-stu-id="f6dd0-127">For example, http://user:pass@ftp.contoso.com/pub/example.iso.</span></span>
- <span data-ttu-id="f6dd0-128">Wenn Sie einen Fragmentbezeichner ("#") einfügen, wird dieser und alles, was auf den Bezeichner folgt, ignoriert.</span><span class="sxs-lookup"><span data-stu-id="f6dd0-128">If you include a fragment identifier ("#"), it and everything that follows the identifier is ignored.</span></span>
- <span data-ttu-id="f6dd0-129">Sie können einen Platzhalter ("\*") als **Host** verwenden und ihm einen Punkt (".") voranstellen.</span><span class="sxs-lookup"><span data-stu-id="f6dd0-129">You can use a wildcard ("\*") as the **host** and you can prefix it with a dot (".").</span></span>
- <span data-ttu-id="f6dd0-130">Sie können einen Schrägstrich (/") oder einen Punkt (".") als Suffix für den **Host** verwenden.</span><span class="sxs-lookup"><span data-stu-id="f6dd0-130">You can use a forward slash ("/") or a dot (".") as a suffix for the **host**.</span></span> <span data-ttu-id="f6dd0-131">In diesem Fall wird das Suffix ignoriert.</span><span class="sxs-lookup"><span data-stu-id="f6dd0-131">In this case, the suffix is ignored.</span></span>

## <span data-ttu-id="f6dd0-132">Kriterien für die Filterauswahl</span><span class="sxs-lookup"><span data-stu-id="f6dd0-132">Filter selection criteria</span></span>

<span data-ttu-id="f6dd0-133">Der für eine URL ausgewählte Filter ist die spezifischste Übereinstimmung, die nach Verarbeitung der folgenden Filterauswahlregeln gefunden wurde:</span><span class="sxs-lookup"><span data-stu-id="f6dd0-133">The filter selected for a URL is the most specific match found after processing the following filter selection rules:</span></span>

1. <span data-ttu-id="f6dd0-134">Filter mit der längsten **Host**-Übereinstimmung werden zuerst ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="f6dd0-134">Filters with the longest **host** match are selected first.</span></span>
2. <span data-ttu-id="f6dd0-135">Aus den ausgewählten Filtern werden alle Filter mit einem nicht übereinstimmenden Schema oder Port verworfen.</span><span class="sxs-lookup"><span data-stu-id="f6dd0-135">From the selected filters, any filter with a non-matching scheme or port is discarded.</span></span>
3. <span data-ttu-id="f6dd0-136">Aus den verbleibenden Filtern wird der Filter mit dem längsten übereinstimmenden **Pfad** ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="f6dd0-136">From the remaining filters, the filter with the longest matching **path** is selected.</span></span>
4. <span data-ttu-id="f6dd0-137">Aus den verbleibenden Filtern wird der Filter mit dem längsten Satz von Abfragetoken ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="f6dd0-137">From the remaining filters, the filter with the longest set of query tokens is selected.</span></span> <span data-ttu-id="f6dd0-138">In diesem Schritt hat der Zulassungslistenfilter Vorrang vor dem Sperrlistenfilter, wenn beide Filter die gleiche **Pfadlänge** und Anzahl von **Abfragetoken** aufweisen.</span><span class="sxs-lookup"><span data-stu-id="f6dd0-138">At this step, the allow list filter takes precedence over the block list filter if both filters have the same **path** length and number of **query** tokens.</span></span>
5. <span data-ttu-id="f6dd0-139">Wenn kein gültiger Filter mehr vorhanden ist, wird die Subdomäne ganz links vom **Host** entfernt, und der Auswahlprozess beginnt bei Schritt 1 von vorne.</span><span class="sxs-lookup"><span data-stu-id="f6dd0-139">If there's no valid filter remaining, then the left-most subdomain is removed from **host** and the selection process starts over at step 1.</span></span> <span data-ttu-id="f6dd0-140">Der **Host** mit dem speziellen Sternchen ("\*") ist der zuletzt gesuchte Host, der mit allen Hosts übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="f6dd0-140">The special asterisk ("\*") **host** is the last searched and it matches all hosts.</span></span>
6. <span data-ttu-id="f6dd0-141">Wenn ein Filter verfügbar ist, wird die URL-Anforderung blockiert oder zugelassen.</span><span class="sxs-lookup"><span data-stu-id="f6dd0-141">If a filter's available, it blocks or allows the URL request.</span></span>

   >[!NOTE]
   ><span data-ttu-id="f6dd0-142">Das Standardverhalten besteht darin, die URL-Anforderung zuzulassen, wenn keine Übereinstimmung mit einem Filter vorliegt.</span><span class="sxs-lookup"><span data-stu-id="f6dd0-142">The default behavior is to allow the URL request if no filter is matched.</span></span>

## <span data-ttu-id="f6dd0-143">Beispiel für Kriterien für die Filterauswahl</span><span class="sxs-lookup"><span data-stu-id="f6dd0-143">Example filter selection criteria</span></span>

<span data-ttu-id="f6dd0-144">In diesem Beispiel führt die Filterauswahl bei der Suche nach einer Übereinstimmung mit "https://sub.contoso.com/docs" Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="f6dd0-144">In this example, when searching for a match to "https://sub.contoso.com/docs" the filter selection will:</span></span>

1. <span data-ttu-id="f6dd0-145">Suchen nach einem Filter für „sub.contoso.com”.</span><span class="sxs-lookup"><span data-stu-id="f6dd0-145">Search for a filter for "sub.contoso.com".</span></span> <span data-ttu-id="f6dd0-146">Wenn ein Filter gefunden wird, wird die Suche mit Schritt2 fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="f6dd0-146">If it finds a filter, the search moves to step 2.</span></span> <span data-ttu-id="f6dd0-147">Wenn ein Filter nicht gefunden wird, wird die Suche erneut mit "contoso.com", "com" und schließlich "" versucht.</span><span class="sxs-lookup"><span data-stu-id="f6dd0-147">If a filter isn't found, then it tries again with "contoso.com", "com", and finally "".</span></span>
2. <span data-ttu-id="f6dd0-148">Aus den ausgewählten Filtern werden alle, die im **Schema** nicht über "http" verfügen, entfernt.</span><span class="sxs-lookup"><span data-stu-id="f6dd0-148">From the selected filters, any that don't have "http" in the **scheme** are removed.</span></span>
3. <span data-ttu-id="f6dd0-149">Aus den verbleibenden Filtern werden alle, die über eine genaue Portnummer verfügen, die nicht "80" ist, entfernt.</span><span class="sxs-lookup"><span data-stu-id="f6dd0-149">From the remaining filters, any that have an exact port number that isn't "80" are removed.</span></span>
4. <span data-ttu-id="f6dd0-150">Aus den übrigen Filtern werden alle, die nicht „/docs” als Präfix des **Pfads** haben, entfernt.</span><span class="sxs-lookup"><span data-stu-id="f6dd0-150">From the remaining filters, any that don't have "/docs" as a prefix of the **path** are removed.</span></span>
5. <span data-ttu-id="f6dd0-151">Aus den verbleibenden Filtern wird der Filter mit dem längsten Pfadpräfix ausgewählt und angewendet.</span><span class="sxs-lookup"><span data-stu-id="f6dd0-151">From the remaining filters, the filter with the longest path prefix is selected and applied.</span></span> <span data-ttu-id="f6dd0-152">Wird kein Filter gefunden, beginnt der Auswahlprozess erneut bei Schritt 1.</span><span class="sxs-lookup"><span data-stu-id="f6dd0-152">If a filter isn't found, the selection process starts over again at step 1.</span></span> <span data-ttu-id="f6dd0-153">Der Prozess wird mit der nächsten Unterdomäne wiederholt.</span><span class="sxs-lookup"><span data-stu-id="f6dd0-153">The process is repeated with the next subdomain.</span></span>

### <span data-ttu-id="f6dd0-154">Zusätzliche Filterinformationen</span><span class="sxs-lookup"><span data-stu-id="f6dd0-154">Additional filter information</span></span>

<span data-ttu-id="f6dd0-155">Wenn ein Filter einen Punkt (".") enthält, der dem **Host** vorangestellt ist, werden nur exakte **Host-Übereinstimmungen** gefiltert.</span><span class="sxs-lookup"><span data-stu-id="f6dd0-155">If a filter has a dot (".") prefixing the **host** then only exact **host** matches are filtered.</span></span> <span data-ttu-id="f6dd0-156">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="f6dd0-156">For example:</span></span>

- <span data-ttu-id="f6dd0-157">"contoso.com" (kein Punkt) stimmt mit "contoso.com", "www.contoso.com" und "sub.www.contoso.com" überein.</span><span class="sxs-lookup"><span data-stu-id="f6dd0-157">"contoso.com" (no dot) will match "contoso.com", "www.contoso.com", and "sub.www.contoso.com"</span></span>
- <span data-ttu-id="f6dd0-158">".www.contoso.com" (mit einem Punkt als Präfix) stimmt nur mit "www.contoso.com" überein.</span><span class="sxs-lookup"><span data-stu-id="f6dd0-158">".www.contoso.com" (with a dot prefix) will only match "www.contoso.com"</span></span>

<span data-ttu-id="f6dd0-159">Sie können entweder ein Standard- oder ein benutzerdefiniertes **Schema** verwenden.</span><span class="sxs-lookup"><span data-stu-id="f6dd0-159">You can use either a standard or customer **schema**.</span></span> <span data-ttu-id="f6dd0-160">Unterstützte Standardschemata sind:</span><span class="sxs-lookup"><span data-stu-id="f6dd0-160">Supported standard schemas include:</span></span>

- <span data-ttu-id="f6dd0-161">_about_, _blob_, _content_, _edge_, _cid_, _data_, _file_, _filesystem_, _ftp_, _gopher_, _http_, _https_, _javascript_, _mailto_, _ws_, und _wss_.</span><span class="sxs-lookup"><span data-stu-id="f6dd0-161">_about_, _blob_, _content_, _edge_, _cid_, _data_, _file_, _filesystem_, _ftp_, _gopher_, _http_, _https_, _javascript_, _mailto_, _ws_, and _wss_.</span></span>

<span data-ttu-id="f6dd0-162">Jedes andere **Schema** wird als benutzerdefiniertes **Schema** behandelt, wobei nur die Muster _Schema:\*_ und _schema://\*_ zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="f6dd0-162">Any other **schema** is treated as a custom **schema**, but only the _schema:\*_ and _schema://\*_ patterns are allowed.</span></span> <span data-ttu-id="f6dd0-163">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="f6dd0-163">For example:</span></span>

- <span data-ttu-id="f6dd0-164">"custom:*" bzw. "custom://*" stimmt mit "custom:app" überein.</span><span class="sxs-lookup"><span data-stu-id="f6dd0-164">"custom:*" or "custom://*" will match "custom:app"</span></span>
- <span data-ttu-id="f6dd0-165">"custom:app" bzw. "custom://app" sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="f6dd0-165">"custom:app" or "custom://app" are invalid</span></span>

<span data-ttu-id="f6dd0-166">Bei **Schema** und **Host** wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="f6dd0-166">**schema** and **host** aren't case-sensitive.</span></span> <span data-ttu-id="f6dd0-167">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="f6dd0-167">For example:</span></span>

- <span data-ttu-id="f6dd0-168">Der Filter "http://contoso.com" stimmt mit "HTTP://contoso.com", "http://contoso.COM" und "http://contoso.com" überein.</span><span class="sxs-lookup"><span data-stu-id="f6dd0-168">"http://contoso.com" filter matches "HTTP://contoso.com", "http://contoso.COM", and "http://contoso.com"</span></span>

<span data-ttu-id="f6dd0-169">Bei **Pfad** und **Abfrage** wird die Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="f6dd0-169">**path** and **query** are case-sensitive.</span></span> <span data-ttu-id="f6dd0-170">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="f6dd0-170">For example:</span></span>

- <span data-ttu-id="f6dd0-171">Der Filter "http://contoso.com/path?query=A" stimmt weder mit "http://contoso.com/Path?query=A" noch mit "http://contoso.com/path?Query=A" überein.</span><span class="sxs-lookup"><span data-stu-id="f6dd0-171">"http://contoso.com/path?query=A" filter doesn't match "http://contoso.com/Path?query=A" or "http://contoso.com/path?Query=A".</span></span> <span data-ttu-id="f6dd0-172">Er stimmt mit "http://contoso.COM/path?query=A" überein.</span><span class="sxs-lookup"><span data-stu-id="f6dd0-172">It does match "http://contoso.COM/path?query=A".</span></span>

## <span data-ttu-id="f6dd0-173">Lizenz für Inhalte</span><span class="sxs-lookup"><span data-stu-id="f6dd0-173">Content license</span></span>

> [!NOTE]
> <span data-ttu-id="f6dd0-174">Teile dieser Seite sind Änderungen, die auf von Chromium.org erstellten und freigegebenen Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/) beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f6dd0-174">Portions of this page are modifications based on work created and shared by Chromium.org and used according to terms described in the [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/).</span></span> <span data-ttu-id="f6dd0-175">Die Originalseite von [Chromium finden Sie hier](https://www.chromium.org/administrators/url-blacklist-filter-format).</span><span class="sxs-lookup"><span data-stu-id="f6dd0-175">The original [Chromium page can be found here](https://www.chromium.org/administrators/url-blacklist-filter-format).</span></span>
  
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br /><span data-ttu-id="f6dd0-176">Diese Arbeit unterliegt einer <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.</span><span class="sxs-lookup"><span data-stu-id="f6dd0-176">This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.</span></span>

## <span data-ttu-id="f6dd0-177">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f6dd0-177">See also</span></span>

- [<span data-ttu-id="f6dd0-178">Microsoft Edge Enterprise-Angebotsseite</span><span class="sxs-lookup"><span data-stu-id="f6dd0-178">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
