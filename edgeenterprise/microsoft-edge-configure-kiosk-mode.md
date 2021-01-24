---
title: Konfigurieren des Microsoft Edge-Kioskmodus
ms.author: aguta
author: aguta
manager: srugh
ms.date: 01/21/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Konfigurieren des Microsoft Edge-Kioskmodus
ms.openlocfilehash: be353a0e13e9234de40296a2e8dcc31b1b800f52
ms.sourcegitcommit: 8a88fd38bdb5e132e89bf17dd2b5fb72f5d1b4b9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/22/2021
ms.locfileid: "11297471"
---
# <span data-ttu-id="690a3-103">Konfigurieren des Microsoft Edge-Kioskmodus</span><span class="sxs-lookup"><span data-stu-id="690a3-103">Configure Microsoft Edge kiosk mode</span></span>

<span data-ttu-id="690a3-104">In diesem Artikel wird beschrieben, wie Sie die Optionen für den Microsoft Edge-Kioskmodus Ihren Anforderungen entsprechend konfigurieren können.</span><span class="sxs-lookup"><span data-stu-id="690a3-104">This article describes how to configure Microsoft Edge kiosk mode options that you can pilot.</span></span> <span data-ttu-id="690a3-105">Eine Roadmap zukünftiger Features wird ebenfalls vorgestellt.</span><span class="sxs-lookup"><span data-stu-id="690a3-105">There's also a roadmap of features we're targeting.</span></span>

> [!NOTE]
> <span data-ttu-id="690a3-106">Dieser Artikel bezieht sich auf Microsoft Edge Version 87 oder neuer.</span><span class="sxs-lookup"><span data-stu-id="690a3-106">This article applies to Microsoft Edge version 87 or later.</span></span>

## <span data-ttu-id="690a3-107">Übersicht</span><span class="sxs-lookup"><span data-stu-id="690a3-107">Overview</span></span>

<span data-ttu-id="690a3-108">Im Microsoft Edge-Kiosk-Modus sind zwei gesperrte Browserumgebungen verfügbar, damit Organisationen optimale Umgebungen für ihre Kunden gestalten, verwalten und anbieten können.</span><span class="sxs-lookup"><span data-stu-id="690a3-108">Microsoft Edge kiosk mode offers two lockdown experiences of the browser so organizations can create, manage, and provide the best experience for their customers.</span></span> <span data-ttu-id="690a3-109">Die folgenden gesperrten Umgebungen sind verfügbar:</span><span class="sxs-lookup"><span data-stu-id="690a3-109">The following lockdown experiences are available:</span></span>  

- <span data-ttu-id="690a3-110">**Digital/Interactive Signage–** Zeigt eine bestimmte Website im Vollbildmodus an.</span><span class="sxs-lookup"><span data-stu-id="690a3-110">**Digital/Interactive Signage** experience - Displays a specific site in full-screen mode.</span></span>
- <span data-ttu-id="690a3-111">**Öffentliches Browsen** – Führt eine eingeschränkte Version mit mehreren Registerkarten von Microsoft Edge aus.</span><span class="sxs-lookup"><span data-stu-id="690a3-111">**Public-Browsing** experience - Runs a limited multi-tab version of Microsoft Edge.</span></span>

<span data-ttu-id="690a3-112">In beiden Fällen wird eine Microsoft Edge-InPrivate-Sitzung ausgeführt, wodurch die Benutzerdaten geschützt sind.</span><span class="sxs-lookup"><span data-stu-id="690a3-112">Both experiences are running a Microsoft Edge InPrivate session, which protects user data.</span></span>

## <span data-ttu-id="690a3-113">Einrichten des Microsoft Edge-Kioskmodus</span><span class="sxs-lookup"><span data-stu-id="690a3-113">Set up Microsoft Edge kiosk mode</span></span>

<span data-ttu-id="690a3-114">Ein anfänglicher Satz von Kioskmodusfeatures steht zum Testen mit Microsoft Edge Stable-Kanal, Version 87, zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="690a3-114">An initial set of kiosk mode features is available to test with Microsoft Edge Stable Channel, version 87.</span></span> <span data-ttu-id="690a3-115">Sie können die neueste Version von [Microsoft Edge (offizieller Stable-Kanal) herunterladen.](https://www.microsoft.com/edge)</span><span class="sxs-lookup"><span data-stu-id="690a3-115">You can download the latest version from [Microsoft Edge (Official Stable Channel)](https://www.microsoft.com/edge).</span></span>

### <span data-ttu-id="690a3-116">Unterstützte Features im Kioskmodus</span><span class="sxs-lookup"><span data-stu-id="690a3-116">Kiosk mode supported features</span></span>

<span data-ttu-id="690a3-117">In der folgenden Tabelle sind die im Kioskmodus unterstützten Features aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="690a3-117">The following table lists the features supported by kiosk mode.</span></span>

|<span data-ttu-id="690a3-118">Feature</span><span class="sxs-lookup"><span data-stu-id="690a3-118">Feature</span></span>|<span data-ttu-id="690a3-119">Digital\Interactive Signage</span><span class="sxs-lookup"><span data-stu-id="690a3-119">Digital\Interactive Signage</span></span>|<span data-ttu-id="690a3-120">Öffentliches Surfen</span><span class="sxs-lookup"><span data-stu-id="690a3-120">Public browsing</span></span>|<span data-ttu-id="690a3-121">Verfügbar mit Microsoft Edge Version (und höher)</span><span class="sxs-lookup"><span data-stu-id="690a3-121">Available with Microsoft Edge version (and higher)</span></span>|
|-|-|-|-|
|<span data-ttu-id="690a3-122">InPrivate-Navigation</span><span class="sxs-lookup"><span data-stu-id="690a3-122">InPrivate Navigation</span></span>|<span data-ttu-id="690a3-123">„Y“ zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="690a3-123">Y</span></span>|<span data-ttu-id="690a3-124">„Y“ zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="690a3-124">Y</span></span>|<span data-ttu-id="690a3-125">87</span><span class="sxs-lookup"><span data-stu-id="690a3-125">87</span></span>|
|<span data-ttu-id="690a3-126">Zurücksetzen bei Inaktivität</span><span class="sxs-lookup"><span data-stu-id="690a3-126">Reset on inactivity</span></span>|<span data-ttu-id="690a3-127">„Y“ zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="690a3-127">Y</span></span>|<span data-ttu-id="690a3-128">„Y“ zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="690a3-128">Y</span></span>|<span data-ttu-id="690a3-129">87</span><span class="sxs-lookup"><span data-stu-id="690a3-129">87</span></span>|
|<span data-ttu-id="690a3-130">[Schreibgeschützte Adressleiste](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskaddressbareditingenabled) (Richtlinie)</span><span class="sxs-lookup"><span data-stu-id="690a3-130">[Read only address bar](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskaddressbareditingenabled) (policy)</span></span> |<span data-ttu-id="690a3-131">N</span><span class="sxs-lookup"><span data-stu-id="690a3-131">N</span></span>|<span data-ttu-id="690a3-132">„Y“ zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="690a3-132">Y</span></span> |<span data-ttu-id="690a3-133">87</span><span class="sxs-lookup"><span data-stu-id="690a3-133">87</span></span>|
|<span data-ttu-id="690a3-134">[Löschen von Downloads beim Beenden](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskdeletedownloadsonexit) (Richtlinie)</span><span class="sxs-lookup"><span data-stu-id="690a3-134">[Delete downloads on exit](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskdeletedownloadsonexit) (policy)</span></span>  | <span data-ttu-id="690a3-135">„Y“ zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="690a3-135">Y</span></span>|<span data-ttu-id="690a3-136">„Y“ zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="690a3-136">Y</span></span> |<span data-ttu-id="690a3-137">87</span><span class="sxs-lookup"><span data-stu-id="690a3-137">87</span></span>|
|<span data-ttu-id="690a3-138">F11 blockiert (Vollbild-/Ein-/Austritt)</span><span class="sxs-lookup"><span data-stu-id="690a3-138">F11 blocked (enter/exit full-screen)</span></span> | <span data-ttu-id="690a3-139">„Y“ zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="690a3-139">Y</span></span> | <span data-ttu-id="690a3-140">„Y“ zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="690a3-140">Y</span></span> | <span data-ttu-id="690a3-141">87</span><span class="sxs-lookup"><span data-stu-id="690a3-141">87</span></span> |
|<span data-ttu-id="690a3-142">F12 blockiert (Entwicklertools starten)</span><span class="sxs-lookup"><span data-stu-id="690a3-142">F12 blocked (launch Developer Tools)</span></span> | <span data-ttu-id="690a3-143">„Y“ zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="690a3-143">Y</span></span> | <span data-ttu-id="690a3-144">„Y“ zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="690a3-144">Y</span></span> | <span data-ttu-id="690a3-145">87</span><span class="sxs-lookup"><span data-stu-id="690a3-145">87</span></span> |
| <span data-ttu-id="690a3-146">Unterstützung für mehrere Registerkarten</span><span class="sxs-lookup"><span data-stu-id="690a3-146">Multi tab support</span></span> | <span data-ttu-id="690a3-147">N</span><span class="sxs-lookup"><span data-stu-id="690a3-147">N</span></span>| <span data-ttu-id="690a3-148">„Y“ zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="690a3-148">Y</span></span>| <span data-ttu-id="690a3-149">87</span><span class="sxs-lookup"><span data-stu-id="690a3-149">87</span></span>|
|<span data-ttu-id="690a3-150">Sitzung beenden</span><span class="sxs-lookup"><span data-stu-id="690a3-150">End session button</span></span> | <span data-ttu-id="690a3-151">N</span><span class="sxs-lookup"><span data-stu-id="690a3-151">N</span></span>| <span data-ttu-id="690a3-152">„Y“ zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="690a3-152">Y</span></span>| <span data-ttu-id="690a3-153">88</span><span class="sxs-lookup"><span data-stu-id="690a3-153">88</span></span>|
|<span data-ttu-id="690a3-154">Alle internen Microsoft Edge-URLs werden blockiert, mit *Ausnahme* von edge://downloads und *edge://print*</span><span class="sxs-lookup"><span data-stu-id="690a3-154">All internal Microsoft Edge URLs are blocked, except for *edge://downloads* and *edge://print*</span></span> |<span data-ttu-id="690a3-155">N</span><span class="sxs-lookup"><span data-stu-id="690a3-155">N</span></span>|<span data-ttu-id="690a3-156">„Y“ zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="690a3-156">Y</span></span>|<span data-ttu-id="690a3-157">88</span><span class="sxs-lookup"><span data-stu-id="690a3-157">88</span></span>|
| <span data-ttu-id="690a3-158">STRG+N blockiert (neues Fenster öffnen)</span><span class="sxs-lookup"><span data-stu-id="690a3-158">CTRL+N blocked (open a new window)</span></span> | <span data-ttu-id="690a3-159">„Y“ zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="690a3-159">Y</span></span> | <span data-ttu-id="690a3-160">„Y“ zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="690a3-160">Y</span></span> | <span data-ttu-id="690a3-161">89</span><span class="sxs-lookup"><span data-stu-id="690a3-161">89</span></span> |
| <span data-ttu-id="690a3-162">STRG+T blockiert (neue Registerkarte öffnen)</span><span class="sxs-lookup"><span data-stu-id="690a3-162">CTRL+T blocked (open new tab)</span></span> | <span data-ttu-id="690a3-163">N</span><span class="sxs-lookup"><span data-stu-id="690a3-163">N</span></span> | <span data-ttu-id="690a3-164">„Y“ zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="690a3-164">Y</span></span> | <span data-ttu-id="690a3-165">89</span><span class="sxs-lookup"><span data-stu-id="690a3-165">89</span></span> |
|<span data-ttu-id="690a3-166">Einstellungen und vieles mehr (...) zeigt nur die erforderlichen Optionen an.</span><span class="sxs-lookup"><span data-stu-id="690a3-166">Settings and more (...) will display only the required options</span></span>  |<span data-ttu-id="690a3-167">N</span><span class="sxs-lookup"><span data-stu-id="690a3-167">N</span></span> |<span data-ttu-id="690a3-168">„Y“ zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="690a3-168">Y</span></span> |<span data-ttu-id="690a3-169">89</span><span class="sxs-lookup"><span data-stu-id="690a3-169">89</span></span> |

> [!NOTE]
> <span data-ttu-id="690a3-170">Im Laufe der Weiterentwicklung des Kioskmodus werden auch weitere Features verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="690a3-170">As kiosk mode evolves, more features will be available.</span></span>

## <span data-ttu-id="690a3-171">Verwenden der Kioskmodus-Features</span><span class="sxs-lookup"><span data-stu-id="690a3-171">Use kiosk mode features</span></span>

<span data-ttu-id="690a3-172">Microsoft Edge Kioskmodusfeatures können mit den folgenden Windows 10-Befehlszeilenoptionen aufgerufen werden:</span><span class="sxs-lookup"><span data-stu-id="690a3-172">Microsoft Edge kiosk mode features can be invoked with the following Windows 10 command line options:</span></span>

- <span data-ttu-id="690a3-173">Kioskmodus "Digitale/interaktive Beschilderung":</span><span class="sxs-lookup"><span data-stu-id="690a3-173">Kiosk mode Digital/Interactive signage:</span></span> `msedge.exe --kiosk www.contoso.com --edge-kiosk-type=fullscreen`
- <span data-ttu-id="690a3-174">Kioskmodus "Öffentliches Surfen":</span><span class="sxs-lookup"><span data-stu-id="690a3-174">Kiosk mode public browsing:</span></span> `msedge.exe --kiosk www.contoso.com --edge-kiosk-type=public-browsing`

### <span data-ttu-id="690a3-175">Zusätzliche Befehlszeilenoptionen</span><span class="sxs-lookup"><span data-stu-id="690a3-175">Additional command line options</span></span>

- `--no-first-run` <span data-ttu-id="690a3-176">: Deaktivieren Sie die erste Ausführung von Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="690a3-176">: Disable the first Microsoft Edge run experience.</span></span>
- `--kiosk-idle-timeout-minutes` <span data-ttu-id="690a3-177">: Ändern Sie den Zeitraum (in Minuten) nach der letzten Benutzeraktivität, nach dem der Microsoft Edge-Kioskmodus die Benutzersitzung zurücksetzt.</span><span class="sxs-lookup"><span data-stu-id="690a3-177">: Change the time (in minutes) from the last user activity before Microsoft Edge kiosk mode resets the user's session.</span></span> <span data-ttu-id="690a3-178">Die folgenden Werte werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="690a3-178">The following values are supported:</span></span>

  - <span data-ttu-id="690a3-179">Standardwerte</span><span class="sxs-lookup"><span data-stu-id="690a3-179">Default values</span></span>
    - <span data-ttu-id="690a3-180">Vollbildmodus – deaktiviert</span><span class="sxs-lookup"><span data-stu-id="690a3-180">Full screen - turned off</span></span>
    - <span data-ttu-id="690a3-181">Öffentliches Surfen – 5 Minuten</span><span class="sxs-lookup"><span data-stu-id="690a3-181">Public browsing - 5 minutes</span></span>
  - <span data-ttu-id="690a3-182">Zulässige Werte</span><span class="sxs-lookup"><span data-stu-id="690a3-182">Allowed values</span></span>
    - <span data-ttu-id="690a3-183">0 – deaktiviert den Timer</span><span class="sxs-lookup"><span data-stu-id="690a3-183">0 - turns off the timer</span></span>
    - <span data-ttu-id="690a3-184">1-1440 Minuten für das Zurücksetzen für den Leerlaufzeit-Zeitgeber</span><span class="sxs-lookup"><span data-stu-id="690a3-184">1-1440 minutes for reset on idle timer</span></span>

## <span data-ttu-id="690a3-185">Supportrichtlinien für den Kioskmodus</span><span class="sxs-lookup"><span data-stu-id="690a3-185">Support policies for kiosk mode</span></span>

<span data-ttu-id="690a3-186">Verwenden Sie eine der in der folgenden Tabelle aufgeführten Microsoft Edge-Richtlinien, um die Kioskerfahrung für den von Ihnen konfigurierten Microsoft Edge-Kioskmodustyp zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="690a3-186">Use any of the Microsoft Edge policies listed in the following table to enhance the kiosk experience for the Microsoft Edge kiosk mode type you configure.</span></span> <span data-ttu-id="690a3-187">Weitere Informationen zu diesen Richtlinien finden Sie unter [Microsoft Edge – Browser policy reference](https://docs.microsoft.com/deployedge/microsoft-edge-policies).</span><span class="sxs-lookup"><span data-stu-id="690a3-187">To learn more about these policies, see [Microsoft Edge – Browser policy reference](https://docs.microsoft.com/deployedge/microsoft-edge-policies).</span></span>

> [!NOTE]
> <span data-ttu-id="690a3-188">Die Richtlinienkonfiguration ist nicht auf die in der folgenden Tabelle aufgeführten Richtlinien beschränkt. Es sollten jedoch zusätzliche Richtlinien getestet werden, um sicherzustellen, dass die Funktionalität des Kioskmodus nicht negativ beeinträchtigt wird.</span><span class="sxs-lookup"><span data-stu-id="690a3-188">Policy configuration isn't limited to the policies listed in the following table, however additional policies should be tested to ensure that kiosk mode functionality isn't negatively affected.</span></span>

|<span data-ttu-id="690a3-189">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="690a3-189">Group policy</span></span>|<span data-ttu-id="690a3-190">Digital\Interactive Signage</span><span class="sxs-lookup"><span data-stu-id="690a3-190">Digital\Interactive signage</span></span>|<span data-ttu-id="690a3-191">Einzel-App für öffentliches Browsen</span><span class="sxs-lookup"><span data-stu-id="690a3-191">Public browsing single-app</span></span>|
|--|--|--|
|[<span data-ttu-id="690a3-192">Drucken</span><span class="sxs-lookup"><span data-stu-id="690a3-192">Printing</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#printing-policies) | <span data-ttu-id="690a3-193">„Y“ zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="690a3-193">Y</span></span>|<span data-ttu-id="690a3-194">„Y“ zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="690a3-194">Y</span></span> |
|[<span data-ttu-id="690a3-195">HomePageLocation</span><span class="sxs-lookup"><span data-stu-id="690a3-195">HomePageLocation</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#homepagelocation) |<span data-ttu-id="690a3-196">N</span><span class="sxs-lookup"><span data-stu-id="690a3-196">N</span></span> | <span data-ttu-id="690a3-197">„Y“ zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="690a3-197">Y</span></span>|
|[<span data-ttu-id="690a3-198">ShowHomeButton</span><span class="sxs-lookup"><span data-stu-id="690a3-198">ShowHomeButton</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#showhomebutton) |<span data-ttu-id="690a3-199">N</span><span class="sxs-lookup"><span data-stu-id="690a3-199">N</span></span> | <span data-ttu-id="690a3-200">„Y“ zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="690a3-200">Y</span></span>|
|[<span data-ttu-id="690a3-201">NewTabPageLocation</span><span class="sxs-lookup"><span data-stu-id="690a3-201">NewTabPageLocation</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#newtabpagelocation) |<span data-ttu-id="690a3-202">N</span><span class="sxs-lookup"><span data-stu-id="690a3-202">N</span></span> |<span data-ttu-id="690a3-203">„Y“ zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="690a3-203">Y</span></span> |
|[<span data-ttu-id="690a3-204">FavoritesBarEnabled</span><span class="sxs-lookup"><span data-stu-id="690a3-204">FavoritesBarEnabled</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#favoritesbarenabled) |<span data-ttu-id="690a3-205">N</span><span class="sxs-lookup"><span data-stu-id="690a3-205">N</span></span> |<span data-ttu-id="690a3-206">„Y“ zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="690a3-206">Y</span></span> |
|[<span data-ttu-id="690a3-207">URLAllowlist</span><span class="sxs-lookup"><span data-stu-id="690a3-207">URLAllowlist</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#urlallowlist) |<span data-ttu-id="690a3-208">„Y“ zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="690a3-208">Y</span></span> |<span data-ttu-id="690a3-209">„Y“ zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="690a3-209">Y</span></span> |
|[<span data-ttu-id="690a3-210">URLBlocklist</span><span class="sxs-lookup"><span data-stu-id="690a3-210">URLBlocklist</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#urlblocklist) |<span data-ttu-id="690a3-211">„Y“ zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="690a3-211">Y</span></span> | <span data-ttu-id="690a3-212">„Y“ zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="690a3-212">Y</span></span>|
|[<span data-ttu-id="690a3-213">ManagedSearchEngines</span><span class="sxs-lookup"><span data-stu-id="690a3-213">ManagedSearchEngines</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#managedsearchengines) |<span data-ttu-id="690a3-214">N</span><span class="sxs-lookup"><span data-stu-id="690a3-214">N</span></span> | <span data-ttu-id="690a3-215">„Y“ zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="690a3-215">Y</span></span>|
|[<span data-ttu-id="690a3-216">UserFeedbackAllowed</span><span class="sxs-lookup"><span data-stu-id="690a3-216">UserFeedbackAllowed</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#userfeedbackallowed) |<span data-ttu-id="690a3-217">N</span><span class="sxs-lookup"><span data-stu-id="690a3-217">N</span></span> | <span data-ttu-id="690a3-218">„Y“ zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="690a3-218">Y</span></span>|
|[<span data-ttu-id="690a3-219">VerticalTabsAllowed</span><span class="sxs-lookup"><span data-stu-id="690a3-219">VerticalTabsAllowed</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#verticaltabsallowed) | <span data-ttu-id="690a3-220">N</span><span class="sxs-lookup"><span data-stu-id="690a3-220">N</span></span>|<span data-ttu-id="690a3-221">„Y“ zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="690a3-221">Y</span></span> |
|[<span data-ttu-id="690a3-222">SmartScreen-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="690a3-222">SmartScreen settings</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#smartscreen-settings-policies) |<span data-ttu-id="690a3-223">„Y“ zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="690a3-223">Y</span></span> |<span data-ttu-id="690a3-224">„Y“ zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="690a3-224">Y</span></span> |

## <span data-ttu-id="690a3-225">Microsoft Edge mit zugewiesenem Zugriff</span><span class="sxs-lookup"><span data-stu-id="690a3-225">Microsoft Edge with assigned access</span></span>

### <span data-ttu-id="690a3-226">Einzel-App-Kiosk</span><span class="sxs-lookup"><span data-stu-id="690a3-226">Single app kiosk</span></span>

<span data-ttu-id="690a3-227">Microsoft Edge unterstützt derzeit eine Teilmenge der gleichen Kioskmodustypen der Vorgängerversion von Microsoft Edge für den zugewiesenen Zugriff mit einer einzelnen App mit den folgenden Sperrmodus-Funktionen: Digitale/interaktive Beschilderung und Öffentliches Browsen.</span><span class="sxs-lookup"><span data-stu-id="690a3-227">Microsoft Edge currently supports a subset of the same Microsoft Edge Legacy kiosk mode types for single-app assigned access with the following lockdown experiences: Digital/Interactive signage, and Public-browsing.</span></span>  

<span data-ttu-id="690a3-228">Der Kioskmodus mit zugewiesenem Zugriff ist derzeit für Tests mit dem neuesten  [Windows10 Insider Preview-Build](https://insider.windows.com/), Version 20215 oder höher, und mit dem  [Microsoft Edge Dev Channel](https://www.microsoftedgeinsider.com/download), Version 87.0.644.4 oder höher, verfügbar.</span><span class="sxs-lookup"><span data-stu-id="690a3-228">Kiosk mode with assigned access is currently available for testing with the latest [Windows 10 Insider Preview Build](https://insider.windows.com/), version 20215 or higher, and with the [Microsoft Edge Dev Channel](https://www.microsoftedgeinsider.com/download), version 87.0.644.4 or higher.</span></span>

**<span data-ttu-id="690a3-229">Wie erhalte ich den Windows Insider Preview-Build?</span><span class="sxs-lookup"><span data-stu-id="690a3-229">How do I get the Windows Insiders preview?</span></span>**

<span data-ttu-id="690a3-230">Wenn Sie einen Windows10 Insider Preview-Build auf einem PC installieren möchten, folgen Sie den Anweisungen unter  [Erste Schritte mit Windows10 Insider Preview-Builds](https://docs.microsoft.com/windows-insider/get-started).</span><span class="sxs-lookup"><span data-stu-id="690a3-230">To install a Windows 10 Insider Preview Build on a PC, follow the instructions in [Getting started with Windows 10 Insider Preview Builds](https://docs.microsoft.com/windows-insider/get-started).</span></span>

### <span data-ttu-id="690a3-231">Multi-App-Kiosk</span><span class="sxs-lookup"><span data-stu-id="690a3-231">Multi-app kiosk</span></span>

<span data-ttu-id="690a3-232">Microsoft Edge kann unter Windows10 mit [zugewiesenem Multi-App-Zugriff](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps) ausgeführt werden, was dem Kioskmodustyp „Normales Browsen” von Microsoft Edge Legacy entspricht.</span><span class="sxs-lookup"><span data-stu-id="690a3-232">Microsoft Edge can be run with [multi-app assigned access](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps) on Windows 10, which is the equivalent of Microsoft Edge Legacy "Normal browsing" kiosk mode type.</span></span> <span data-ttu-id="690a3-233">Befolgen Sie die Anweisungen zum Einrichten eines Multi-App-Kiosks, um Microsoft Edge mit zugewiesenen [Multi-App-Zugriffen zu konfigurieren.](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps)</span><span class="sxs-lookup"><span data-stu-id="690a3-233">To configure Microsoft Edge with multi-app assigned access, follow the instructions on how to [Set up a multi-app kiosk](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps).</span></span> <span data-ttu-id="690a3-234">(Die AUMID für den Stable-Kanal von Microsoft Edge ist **MSEdge**.)</span><span class="sxs-lookup"><span data-stu-id="690a3-234">(The AUMID for the Microsoft Edge Stable channel is **MSEdge**).</span></span>

<span data-ttu-id="690a3-235">Wenn Sie Microsoft Edge mit zugewiesenen Zugriffen mit mehreren Apps verwenden, können Sie den Microsoft Edge Kiosk so konfigurieren, dass er die[Microsoft Edge-Browserrichtlinien](https://review.docs.microsoft.com/DeployEdge/microsoft-edge-policies) verwendet, um die Browsererfahrung so zu konfigurieren, dass Ihre individuellen Anforderungen erfüllt werden.</span><span class="sxs-lookup"><span data-stu-id="690a3-235">When using Microsoft Edge with multi-app assigned access, you can configure Microsoft Edge kiosk to use the[Microsoft Edge browser policies](https://review.docs.microsoft.com/DeployEdge/microsoft-edge-policies) to configure the browsing experience to meet your unique requirements.</span></span>

### <span data-ttu-id="690a3-236">Konfigurieren mithilfe der Windows-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="690a3-236">Configure using Windows Settings</span></span>

<span data-ttu-id="690a3-237">Die Windows-Einstellungen sind die einfachste Möglichkeit zum Einrichten von ein oder zwei Einzel-App-Kioskgeräten.</span><span class="sxs-lookup"><span data-stu-id="690a3-237">Windows Settings is the simplest way to set up one or two single-app kiosk devices.</span></span> <span data-ttu-id="690a3-238">Führen Sie die folgenden Schritte aus, um einen Einzel-App-Kioskcomputer einzurichten.</span><span class="sxs-lookup"><span data-stu-id="690a3-238">Use the following steps to set up a single-app kiosk computer.</span></span>

1. <span data-ttu-id="690a3-239">Installieren Sie die neueste Windows 10 Insider Preview-Version (20215 oder höher).</span><span class="sxs-lookup"><span data-stu-id="690a3-239">Install the latest Windows 10 Insider Preview, version 20215 or higher.</span></span> <span data-ttu-id="690a3-240">Folgen Sie den Anweisungen unter [Erste Schritte mit Windows 10 Insider Preview-Builds](https://docs.microsoft.com/windows-insider/get-started).</span><span class="sxs-lookup"><span data-stu-id="690a3-240">Follow the instructions in [Getting started with Windows 10 Insider Preview Builds](https://docs.microsoft.com/windows-insider/get-started).</span></span>
2. <span data-ttu-id="690a3-241">Installieren Sie die neueste Version des [Microsoft Edge Stable-Kanals,](https://www.microsoft.com/edge)Version 87 oder höher.</span><span class="sxs-lookup"><span data-stu-id="690a3-241">Install the latest version of [Microsoft Edge Stable channel](https://www.microsoft.com/edge), version 87 or higher.</span></span>  <span data-ttu-id="690a3-242">Um die neuesten Features zu testen, können Sie den neuesten [Microsoft Edge Dev-Kanal,](https://www.microsoftedgeinsider.com/download)Version 89 oder höher, herunterladen.</span><span class="sxs-lookup"><span data-stu-id="690a3-242">To test the latest features, you can download the latest [Microsoft Edge Dev channel](https://www.microsoftedgeinsider.com/download), version 89 or higher.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="690a3-243">Da eine Installation auf Geräteebene erforderlich ist, wird nur ein nicht-Canary-Kanal unterstützt.</span><span class="sxs-lookup"><span data-stu-id="690a3-243">Because a device level installation is required, only a non-Canary channel is supported.</span></span>

3. <span data-ttu-id="690a3-244">Öffnen Sie auf dem Kiosk-Computer die Windows-Einstellungen, und geben Sie im Suchfeld "Kiosk" ein.</span><span class="sxs-lookup"><span data-stu-id="690a3-244">On the kiosk computer, open Windows Settings, and type "kiosk" in the search field.</span></span> <span data-ttu-id="690a3-245">Wählen Sie  **Einen Kiosk einrichten (zugewiesener Zugriff)** aus, das im nächsten Screenshot dargestellt ist, um das Dialogfeld zum Erstellen des Kiosks zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="690a3-245">Select  **Set up a kiosk (assigned access)**, shown in the next screenshot to open the dialog for creating the kiosk.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-1-assigned-access.png" alt-text="Einrichten eines Kiosks mit zugewiesenem Zugriff":::

4. <span data-ttu-id="690a3-247">Klicken Sie auf der Seite **Einen Kiosk einrichten**  auf **Erste Schritte**.</span><span class="sxs-lookup"><span data-stu-id="690a3-247">On the **Set up a kiosk** page, click **Get started**.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-2-get-started.png" alt-text="Seite "Kiosk" – erste Schritte":::

5. <span data-ttu-id="690a3-249">Geben Sie einen Namen ein, um ein neues Kioskkonto zu erstellen, oder wählen Sie ein vorhandenes Konto aus der Dropdownliste aus, und klicken Sie dann auf  **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="690a3-249">Type a name to create a new kiosk account or choose an existing account from the populated dropdown list and then click **Next**.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-3-create-account.png" alt-text="Kioskmodus – Konto erstellen":::

6. <span data-ttu-id="690a3-251">Wählen Sie auf der Seite **Kiosk-App auswählen**  die Option **Microsoft Edge** aus, und klicken Sie dann auf  **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="690a3-251">On the **Choose a kiosk app** page, select **Microsoft Edge** and then click **Next**.</span></span>

   > [!NOTE]
   > <span data-ttu-id="690a3-252">Dies gilt nur für Microsoft Edge Dev, Beta und Stable-Kanäle.</span><span class="sxs-lookup"><span data-stu-id="690a3-252">This only applies to Microsoft Edge Dev, Beta, and Stable channels.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-4-pick-app.png" alt-text="Kioskmodus – App auswählen":::

7. <span data-ttu-id="690a3-254">Wählen Sie eine der folgenden Optionen für die Darstellung von Microsoft Edge aus, wenn er im Kioskmodus ausgeführt wird:</span><span class="sxs-lookup"><span data-stu-id="690a3-254">Pick one of the following options for how Microsoft Edge displays when running in kiosk mode:</span></span>

   - <span data-ttu-id="690a3-255">Digitale/interaktive Beschilderung: Zeigt eine bestimmte Website im Vollbildmodus an, dabei wird Microsoft Edge ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="690a3-255">Digital/Interactive signage - Displays a specific site in full-screen mode, running Microsoft Edge.</span></span>
   - <span data-ttu-id="690a3-256">Öffentliches Surfen: Führt eine eingeschränkte Version von Microsoft Edge mit mehreren Tabs aus.</span><span class="sxs-lookup"><span data-stu-id="690a3-256">Public browser - Runs a limited multi-tab version of Microsoft Edge.</span></span>

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-5a-digital-sign.png" alt-text="Kioskmodus – digitale Beschilderung im Vollbildmodus":::

8. <span data-ttu-id="690a3-258">Wählen Sie \*\* Weiter\*\* aus.</span><span class="sxs-lookup"><span data-stu-id="690a3-258">Select **Next**.</span></span>
9. <span data-ttu-id="690a3-259">Geben Sie die URL ein, die beim Start des Kiosks geladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="690a3-259">Type the URL to load when the kiosk launches.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-6-enter-url.png" alt-text="Kioskmodus – URL eingeben":::

10. <span data-ttu-id="690a3-261">Übernehmen Sie den Standardwert von 5 Minuten für die Leerlaufzeit, oder geben Sie einen eigenen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="690a3-261">Accept the default value of 5 minutes for the idle time or provide a value of your own.</span></span>

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-7-enter-idle-time.png" alt-text="Kioskmodus – Leerlaufzeit eingeben":::

11. <span data-ttu-id="690a3-263">Klicken Sie auf  **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="690a3-263">Click **Next**.</span></span>
12. <span data-ttu-id="690a3-264">Schließen Sie das Fenster  **Einstellungen** , um Ihre Auswahl zu speichern und anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="690a3-264">Close the **Settings** window to save and apply your choices.</span></span>

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode--8-done.png" alt-text="Kioskmodus – Einrichten abschließen":::

13. <span data-ttu-id="690a3-266">Melden Sie sich vom Kioskgerät ab, und melden Sie sich mit dem lokalen Kioskkonto an, um die Konfiguration zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="690a3-266">Sign out from the kiosk device and sign in with the local kiosk account to validate the configuration.</span></span>

## <span data-ttu-id="690a3-267">Funktionale Beschränkungen</span><span class="sxs-lookup"><span data-stu-id="690a3-267">Functional limitations</span></span>

<span data-ttu-id="690a3-268">Die Veröffentlichung dieser Preview-Version des Kioskmodus erfolgt im Rahmen unserer kontinuierlichen Bemühungen, das Produkt zu verbessern und neue Features hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="690a3-268">With the release of this preview version of kiosk mode we're continuing work on improving the product and adding new features.</span></span>

<span data-ttu-id="690a3-269">Es wird empfohlen, dies zu deaktivieren:</span><span class="sxs-lookup"><span data-stu-id="690a3-269">We recommend that you turn off:</span></span>

- [<span data-ttu-id="690a3-270">StartupBoostEnabled</span><span class="sxs-lookup"><span data-stu-id="690a3-270">StartupBoostEnabled</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#startupboostenabled)
- [<span data-ttu-id="690a3-271">InternetExplorerIntegrationLevel</span><span class="sxs-lookup"><span data-stu-id="690a3-271">InternetExplorerIntegrationLevel</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#internetexplorerintegrationlevel)
- [<span data-ttu-id="690a3-272">Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="690a3-272">Extensions</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#extensions-policies)
- [<span data-ttu-id="690a3-273">BackgroundModeEnabled</span><span class="sxs-lookup"><span data-stu-id="690a3-273">BackgroundModeEnabled</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#backgroundmodeenabled)

## <span data-ttu-id="690a3-274">Roadmap</span><span class="sxs-lookup"><span data-stu-id="690a3-274">Roadmap</span></span>

### <span data-ttu-id="690a3-275">Anfang 2021</span><span class="sxs-lookup"><span data-stu-id="690a3-275">In early 2021</span></span>

<span data-ttu-id="690a3-276">Unterstützung und Funktionen, die hinzukommen werden:</span><span class="sxs-lookup"><span data-stu-id="690a3-276">We'll add the following support and features:</span></span>

- <span data-ttu-id="690a3-277">Allgemeine Verfügbarkeit des Microsoft Edge-Kioskmodus mit zugewiesener Zugriffs-Einzel-App unter Windows 10 1909 und höher.</span><span class="sxs-lookup"><span data-stu-id="690a3-277">General availability of Microsoft Edge kiosk mode with assigned access single app on Windows 10 1909 and higher.</span></span>
- <span data-ttu-id="690a3-278">Zusätzliche Features für Parität mit Vorgängerversion von Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="690a3-278">Additional features for parity with Microsoft Edge Legacy.</span></span>
- <span data-ttu-id="690a3-279">Integration in Intune zum Konfigurieren von Geräten über die Profil-Benutzerumgebung im Kioskmodus.</span><span class="sxs-lookup"><span data-stu-id="690a3-279">Integration with Intune to configure devices using kiosk mode profile UX.</span></span>
- <span data-ttu-id="690a3-280">Zusätzliche Tastenkombinationen werden blockiert.</span><span class="sxs-lookup"><span data-stu-id="690a3-280">Additional keyboard shortcuts will be blocked.</span></span>
- <span data-ttu-id="690a3-281">Schränken Sie den Start anderer Anwendungen über den Browser ein.</span><span class="sxs-lookup"><span data-stu-id="690a3-281">Restrict the launch of other applications from the browser.</span></span>

## <span data-ttu-id="690a3-282">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="690a3-282">See also</span></span>

- [<span data-ttu-id="690a3-283">Konfigurieren von Kiosken und digitalen Anmeldungen in Windows-Desktopeditionen</span><span class="sxs-lookup"><span data-stu-id="690a3-283">Configure kiosks and digital signs on Windows desktop editions</span></span>](https://docs.microsoft.com/windows/configuration/kiosk-methods)
- [<span data-ttu-id="690a3-284">Bereitstellen des Microsoft Edge Legacy-Kioskmodus</span><span class="sxs-lookup"><span data-stu-id="690a3-284">Deploy Microsoft Edge Legacy kiosk mode</span></span>](https://aka.ms/edgekioskmode)
- [<span data-ttu-id="690a3-285">Planen Ihrer Bereitstellung von Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="690a3-285">Plan your deployment of Microsoft Edge</span></span>](deploy-edge-plan-deployment.md)
- [<span data-ttu-id="690a3-286">Angebotsseite für Microsoft Edge für Unternehmen</span><span class="sxs-lookup"><span data-stu-id="690a3-286">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
