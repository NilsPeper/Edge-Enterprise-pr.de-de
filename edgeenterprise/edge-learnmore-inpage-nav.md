---
title: Seiteninterne Navigation im Internet Explorer-Modus beibehalten
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Seiteninterne Navigation im Internet Explorer-Modus beibehalten
ms.openlocfilehash: 20b18d121c3babfaacffd4a08316b25be714d95e
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "11641361"
---
# <a name="keep-in-page-navigation-in-internet-explorer-mode"></a><span data-ttu-id="61473-103">Seiteninterne Navigation im Internet Explorer-Modus beibehalten</span><span class="sxs-lookup"><span data-stu-id="61473-103">Keep in-page navigation in Internet Explorer mode</span></span>

<span data-ttu-id="61473-104">Sie können diese Richtlinie als vorübergehende Lösung verwenden, um zu erzwingen, dass alle seiteninternen Navigationen von Websites im Internet Explorer-Modus (IE-Modus) im IE-Modus verbleiben.</span><span class="sxs-lookup"><span data-stu-id="61473-104">You can use this policy as a temporary solution to force all in-page navigation from Internet Explorer mode (IE mode) sites to stay in IE mode.</span></span>

<span data-ttu-id="61473-105">Eine seiteninterne Navigation wird über einen Link, ein Skript oder ein Formular auf der aktuellen Seite gestartet.</span><span class="sxs-lookup"><span data-stu-id="61473-105">An in-page navigation is started from a link, a script, or a form on the current page.</span></span> <span data-ttu-id="61473-106">Es kann sich auch um eine serverseitige Umleitung eines früheren Versuchs der seiteninternen Navigation handeln.</span><span class="sxs-lookup"><span data-stu-id="61473-106">It can also be a server-side redirect of a previous in-page navigation attempt.</span></span> <span data-ttu-id="61473-107">Umgekehrt kann ein Benutzer eine nicht seiteninterne Navigation, die von der aktuellen Seite unabhängig ist, auf verschiedene Weise mithilfe der Browsersteuerelemente starten.</span><span class="sxs-lookup"><span data-stu-id="61473-107">Conversely, a user can start a navigation that isn't in-page that's independent of the current page in several ways by using the browser controls.</span></span> <span data-ttu-id="61473-108">Zum Beispiel über die Adressleiste, die Zurück-Schaltfläche oder einen Favoritenlink.</span><span class="sxs-lookup"><span data-stu-id="61473-108">For example, using the address bar, the back button, or a favorite link.</span></span>

>[!NOTE]
><span data-ttu-id="61473-109">Dieser Artikel bezieht sich auf Microsoft Edge Version81 oder höher.</span><span class="sxs-lookup"><span data-stu-id="61473-109">This article applies to Microsoft Edge version 81 or later.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="61473-110">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="61473-110">Prerequisites</span></span>

<span data-ttu-id="61473-111">Die folgenden Windows-Updates sind für diese Richtlinie erforderlich:</span><span class="sxs-lookup"><span data-stu-id="61473-111">The following Windows updates are required for this policy:</span></span>

- <span data-ttu-id="61473-112">Windows 10 Version 1909 & 1903, Windows Server Version 1909 & 1903 ([KB4532695](https://support.microsoft.com/help/4532695))</span><span class="sxs-lookup"><span data-stu-id="61473-112">Windows 10 version 1909 & 1903, Windows Server version 1909 & 1903  ([KB4532695](https://support.microsoft.com/help/4532695))</span></span>
- <span data-ttu-id="61473-113">Windows 10 Version 1809, Windows Server Version 1809, Windows Server 2019 ([KB4534321](https://support.microsoft.com/help/4534321))</span><span class="sxs-lookup"><span data-stu-id="61473-113">Windows 10 version 1809, Windows Server version 1809, Windows Server 2019 ([KB4534321](https://support.microsoft.com/help/4534321))</span></span>
- <span data-ttu-id="61473-114">Windows 10 Version 1803 ([KB4534308](https://support.microsoft.com/help/4534308))</span><span class="sxs-lookup"><span data-stu-id="61473-114">Windows 10 version 1803 ([KB4534308](https://support.microsoft.com/help/4534308))</span></span>
- <span data-ttu-id="61473-115">Windows 10 Version 1709 ([KB4534318](https://support.microsoft.com/help/4534318))</span><span class="sxs-lookup"><span data-stu-id="61473-115">Windows 10 version 1709 ([KB4534318](https://support.microsoft.com/help/4534318))</span></span>


## <a name="about-this-policy"></a><span data-ttu-id="61473-116">Informationen zu dieser Richtlinie</span><span class="sxs-lookup"><span data-stu-id="61473-116">About this policy</span></span>

<span data-ttu-id="61473-117">Diese Richtlinie gibt Ihnen Zeit, alle Authentifizierungsserver, die von Ihren Websites im IE-Modus verwendet werden, zu identifizieren und zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="61473-117">This policy gives you time to identify and configure all of the authentication servers used by your IE mode sites.</span></span> <span data-ttu-id="61473-118">Diese Richtlinie kann jedoch zu einer inkonsistenten Browsererfahrung führen, weil einige Websites im IE-Modus und zu anderen Zeiten im Microsoft Edge-Modus gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="61473-118">However, this policy can result in an inconsistent browsing experience, where some sites are rendered in IE mode and at other times rendered in Microsoft Edge mode.</span></span> <span data-ttu-id="61473-119">Diese Erfahrung hängt davon ab, ob die Navigation zur Website von einer Seite im IE-Modus aus begann.</span><span class="sxs-lookup"><span data-stu-id="61473-119">This experience depends on whether the navigation to the site began from an IE mode page.</span></span> <span data-ttu-id="61473-120">Jede Website, die nicht ausdrücklich so konfiguriert ist, dass sie in einer bestimmten Rendering-Engine geöffnet wird, unterliegt dieser Inkonsistenz.</span><span class="sxs-lookup"><span data-stu-id="61473-120">Any site that isn't explicitly configured to open in a specific rendering engine will be subject to this inconsistency.</span></span>

<span data-ttu-id="61473-121">Wenn Sie diese Richtlinie aktivieren, empfehlen wir Ihnen, sie zu deaktivieren, nachdem Sie alle Authentifizierungsserver identifiziert und der Websiteliste als neutral hinzugefügt haben.</span><span class="sxs-lookup"><span data-stu-id="61473-121">If you enable this policy, we recommend that you disable it after you've identified all the authentication servers and added them to the site list as neutral.</span></span> <span data-ttu-id="61473-122">Diese Aktion stellt sicher, dass Ihre modernen Websites niemals versehentlich im IE-Modus gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="61473-122">This action ensures that your modern sites never inadvertently render in IE mode.</span></span>

## <a name="keep-in-page-navigation-in-ie-mode"></a><span data-ttu-id="61473-123">Beibehaltung der seiteninternen Navigation im IE-Modus</span><span class="sxs-lookup"><span data-stu-id="61473-123">Keep in-page navigation in IE mode</span></span>

<span data-ttu-id="61473-124">Um automatische oder alle seiteninternen Navigationen im Internet Explorer-Modus beizubehalten, folgen Sie diesen Schritten:</span><span class="sxs-lookup"><span data-stu-id="61473-124">To keep automatic or all in-page navigation in Internet Explorer mode, follow these steps:</span></span>

1. <span data-ttu-id="61473-125">Öffnen Sie den lokalen Gruppenrichtlinien-Editor.</span><span class="sxs-lookup"><span data-stu-id="61473-125">Open Local Group Policy Editor.</span></span>
2. <span data-ttu-id="61473-126">Klicken Sie auf **Computerkonfiguration** > **Administrative Vorlagen** > **Microsoft Edge**.</span><span class="sxs-lookup"><span data-stu-id="61473-126">Click **Computer Configuration** > **Administrative Templates** > **Microsoft Edge**.</span></span>
3. <span data-ttu-id="61473-127">Doppelklicken Sie unter **Einstellung** auf **Angeben, wie sich "seiteninterne" Navigationen zu nicht konfigurierten Websites verhalten, wenn sie von Seiten im Internet Explorer-Modus gestartet werden**.</span><span class="sxs-lookup"><span data-stu-id="61473-127">Under **Setting**, double-click **Specify how "in-page" navigations to unconfigured sites behave when started from Internet Explorer mode pages**.</span></span>

   ![Seiteninterne Richtlinieneinstellung](media/edge-learnmore-inpage-nav/learnmore-in-page-nav-settings.png)

4. <span data-ttu-id="61473-129">Wählen Sie **Aktiviert** aus.</span><span class="sxs-lookup"><span data-stu-id="61473-129">Select **Enabled**</span></span> 

   ![Seiteninterne Richtlinie aktivieren](media/edge-learnmore-inpage-nav/learnmore-in-page-nav-enable.png)

5. <span data-ttu-id="61473-131">Wählen Sie eine der folgenden Optionen aus der Dropdownliste aus:</span><span class="sxs-lookup"><span data-stu-id="61473-131">Choose one of the following options from the dropdown list:</span></span>

   - <span data-ttu-id="61473-132">\*\*Standard \*\*: Nur Websites, die zum Öffnen im Internet Explorer-Modus konfiguriert sind, werden in diesem Modus geöffnet.</span><span class="sxs-lookup"><span data-stu-id="61473-132">**Default** - Only sites configured to open in Internet Explorer mode will open in that mode.</span></span> <span data-ttu-id="61473-133">Alle Websites, die nicht zum Öffnen im Internet Explorer-Modus konfiguriert sind, werden zurück zu Microsoft Edge umgeleitet.</span><span class="sxs-lookup"><span data-stu-id="61473-133">Any site not configured to open in Internet Explorer mode will be redirected back to Microsoft Edge.</span></span>
   - <span data-ttu-id="61473-134">**Nur automatische Navigationen im Internet Explorer-Modus beibehalten**: Verwenden Sie diese Option, wenn die Standardeinstellung verwendet werden soll, mit der Ausnahme, dass alle automatischen Navigationen (wie z.B. 302-Umleitungen) zu nicht konfigurierten Websites im Internet Explorer-Modus bleiben.</span><span class="sxs-lookup"><span data-stu-id="61473-134">**Keep only automatic navigations in Internet Explorer mode** - Use this option if you want the default experience except that all automatic navigations (such as 302 redirects) to unconfigured sites will be kept in Internet Explorer mode.</span></span>
   - <span data-ttu-id="61473-135">**Beibehalten der gesamten seiteninternen Navigation im Internet Explorer-Modus**  \* *_(Am wenigsten empfohlen)_*_ – Alle Navigationen von Seiten, die im IE-Modus zu nicht konfigurierten Websites geladen wurden, werden im Internet Explorer-Modus beibehalten.</span><span class="sxs-lookup"><span data-stu-id="61473-135">**Keep all in-page navigation in Internet Explorer mode** \**_(Least Recommended)_*_ - All navigations from pages loaded in IE mode to unconfigured sites are kept in Internet Explorer mode.</span></span>

6. <span data-ttu-id="61473-136">Klicken Sie auf _*OK*\* oder **übernehmen,** um die Richtlinieneinstellungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="61473-136">Click _*OK*\* or **Apply** to save the policy settings.</span></span>

## <a name="see-also"></a><span data-ttu-id="61473-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="61473-137">See also</span></span>

- [<span data-ttu-id="61473-138">Microsoft Edge Enterprise-Angebotsseite</span><span class="sxs-lookup"><span data-stu-id="61473-138">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
