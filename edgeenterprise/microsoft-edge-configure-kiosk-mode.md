---
title: Konfigurieren des Microsoft Edge-Kioskmodus
ms.author: aguta
author: aguta
manager: srugh
ms.date: 09/22/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Konfigurieren des Microsoft Edge-Kioskmodus
ms.openlocfilehash: d7c9df82079f8343d43ccfd312623e6e01358fa9
ms.sourcegitcommit: 858227653fc89532d1d274735f53280e27b2a8c0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/22/2020
ms.locfileid: "11072678"
---
# <span data-ttu-id="255f6-103">Konfigurieren des Microsoft Edge-Kioskmodus</span><span class="sxs-lookup"><span data-stu-id="255f6-103">Configure Microsoft Edge kiosk mode</span></span>

<span data-ttu-id="255f6-104">In diesem Artikel wird beschrieben, wie Sie die Optionen für den Microsoft Edge-Kioskmodus Ihren Anforderungen entsprechend konfigurieren können.</span><span class="sxs-lookup"><span data-stu-id="255f6-104">This article describes how to configure Microsoft Edge kiosk mode options that you can pilot.</span></span> <span data-ttu-id="255f6-105">Eine Roadmap zukünftiger Features wird ebenfalls vorgestellt.</span><span class="sxs-lookup"><span data-stu-id="255f6-105">There's also a roadmap of features we are targeting.</span></span>

> [!NOTE]
> <span data-ttu-id="255f6-106">Dieser Artikel bezieht sich auf Microsoft Edge Version 87 oder neuer.</span><span class="sxs-lookup"><span data-stu-id="255f6-106">This article applies to Microsoft Edge version 87 or later.</span></span>

<span data-ttu-id="255f6-107">Informationen zum Kioskmodus von Microsoft Edge Legacy (Version 45 und früher) finden Sie unter [Bereitstellen des Microsoft Edge-Kioskmodus](https://aka.ms/edgekioskmode).</span><span class="sxs-lookup"><span data-stu-id="255f6-107">For information about Microsoft Edge Legacy kiosk mode (version 45 and earlier) see [Deploy Microsoft Edge kiosk mode](https://aka.ms/edgekioskmode).</span></span>

## <span data-ttu-id="255f6-108">Übersicht</span><span class="sxs-lookup"><span data-stu-id="255f6-108">Overview</span></span>

<span data-ttu-id="255f6-109">Im Microsoft Edge-Kiosk-Modus sind zwei gesperrte Browserumgebungen verfügbar, damit Organisationen optimale Umgebungen für ihre Kunden gestalten, verwalten und anbieten können.</span><span class="sxs-lookup"><span data-stu-id="255f6-109">Microsoft Edge kiosk mode offers two lockdown experiences of the browser so organizations can create, manage, and provide the best experience for their customers.</span></span> <span data-ttu-id="255f6-110">Die folgenden gesperrten Umgebungen sind verfügbar:</span><span class="sxs-lookup"><span data-stu-id="255f6-110">The following lockdown experiences are available:</span></span>  

- <span data-ttu-id="255f6-111">Bei der digitalen/interaktiven Beschilderung wird eine bestimmte Website im Vollbildmodus angezeigt.</span><span class="sxs-lookup"><span data-stu-id="255f6-111">The Digital/Interactive signage experience displays a specific site in full-screen mode.</span></span>
- <span data-ttu-id="255f6-112">Bei der Umgebung für öffentliches Surfen wird eine eingeschränkte Version von Microsoft Edge mit mehreren Tabs ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="255f6-112">The public-browsing experience runs a limited multi-tab version of Microsoft Edge.</span></span>

<span data-ttu-id="255f6-113">In beiden Fällen wird eine Microsoft Edge-InPrivate-Sitzung ausgeführt, wodurch die Benutzerdaten geschützt sind.</span><span class="sxs-lookup"><span data-stu-id="255f6-113">Both experiences are running a Microsoft Edge InPrivate session, which protects user data.</span></span>

## <span data-ttu-id="255f6-114">Einrichten des Microsoft Edge-Kioskmodus</span><span class="sxs-lookup"><span data-stu-id="255f6-114">Set up Microsoft Edge kiosk mode</span></span>  

<span data-ttu-id="255f6-115">Jetzt können Sie mit Microsoft Edge Canary, Version 87, eine erste Sammlung von Kioskmodus-Features testen.</span><span class="sxs-lookup"><span data-stu-id="255f6-115">An initial set of kiosk mode features are now available to test with Microsoft Edge Canary Channel, version 87.</span></span> <span data-ttu-id="255f6-116">Sie können Microsoft Edge Canary über die Seite [Microsoft Edge Insider Channels](https://www.microsoftedgeinsider.com/download) herunterladen.</span><span class="sxs-lookup"><span data-stu-id="255f6-116">You can download Microsoft Edge Canary from the [Microsoft Edge Insider Channels](https://www.microsoftedgeinsider.com/download) page.</span></span>

### <span data-ttu-id="255f6-117">Kioskmodus-Features</span><span class="sxs-lookup"><span data-stu-id="255f6-117">Kiosk mode features</span></span>

<span data-ttu-id="255f6-118">Die folgenden Features sind verfügbar:</span><span class="sxs-lookup"><span data-stu-id="255f6-118">The following features are available:</span></span>

- <span data-ttu-id="255f6-119">InPrivate-Navigation.</span><span class="sxs-lookup"><span data-stu-id="255f6-119">InPrivate navigation.</span></span> <span data-ttu-id="255f6-120">Schützt Benutzerdaten durch das Löschen von Browserdaten und Downloads, wenn die Sitzung beendet wird.</span><span class="sxs-lookup"><span data-stu-id="255f6-120">Protects user data by deleting browser data and downloads when the session ends.</span></span>
- <span data-ttu-id="255f6-121">Richtlinie zum Konfigurieren des Löschens von Downloads beim Beenden.</span><span class="sxs-lookup"><span data-stu-id="255f6-121">Policy to configure Delete downloads on exit.</span></span>
- <span data-ttu-id="255f6-122">Zurücksetzen der Benutzersitzung nach einer bestimmten Zeit der Inaktivität.</span><span class="sxs-lookup"><span data-stu-id="255f6-122">Reset user session after a certain period of inactivity.</span></span>
- <span data-ttu-id="255f6-123">Erste verfügbare Sperrfunktionen.</span><span class="sxs-lookup"><span data-stu-id="255f6-123">Initial set of lockdown functionality.</span></span> <span data-ttu-id="255f6-124">Die folgenden Funktionen sind verfügbar:</span><span class="sxs-lookup"><span data-stu-id="255f6-124">The following functions are available:</span></span>

  - <span data-ttu-id="255f6-125">Maus-Kontextmenü</span><span class="sxs-lookup"><span data-stu-id="255f6-125">Mouse context menu</span></span>
  - <span data-ttu-id="255f6-126">F12 Entwicklertools</span><span class="sxs-lookup"><span data-stu-id="255f6-126">F12 Developer Tools</span></span>
  - <span data-ttu-id="255f6-127">F11 Beenden des Vollbildmodus (im Vollbildmodus)</span><span class="sxs-lookup"><span data-stu-id="255f6-127">F11 Exit full screen (while in full screen mode)</span></span>
  - <span data-ttu-id="255f6-128">Blockieren der ersten Reihe von *Edge://*-Seiten</span><span class="sxs-lookup"><span data-stu-id="255f6-128">Blocking of the initial set of *Edge://* pages</span></span>

> [!NOTE]
> <span data-ttu-id="255f6-129">Im Laufe der Weiterentwicklung des Kioskmodus werden auch weitere Features verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="255f6-129">As kiosk mode evolves, more features will be available.</span></span>

### <span data-ttu-id="255f6-130">Verwenden der Kioskmodus-Features</span><span class="sxs-lookup"><span data-stu-id="255f6-130">Use kiosk mode features</span></span>

<span data-ttu-id="255f6-131">Die Microsoft Edge-Kioskmodus-Features können mit den folgenden Windows 10-Befehlszeilenoptionen aufgerufen werden:</span><span class="sxs-lookup"><span data-stu-id="255f6-131">You can invoke Microsoft Edge kiosk mode features can be invoked with the following Windows 10 command line options:</span></span>

- <span data-ttu-id="255f6-132">Kioskmodus "Digitale/interaktive Beschilderung":</span><span class="sxs-lookup"><span data-stu-id="255f6-132">Kiosk mode Digital/Interactive signage:</span></span> `msedge.exe --kiosk www.contoso.com --edge-kiosk-type=fullscreen`
- <span data-ttu-id="255f6-133">Kioskmodus "Öffentliches Surfen":</span><span class="sxs-lookup"><span data-stu-id="255f6-133">Kiosk mode public browsing:</span></span> `msedge.exe --kiosk www.contoso.com --edge-kiosk-type=public-browsing`

#### <span data-ttu-id="255f6-134">Zusätzliche Befehlszeilenoptionen</span><span class="sxs-lookup"><span data-stu-id="255f6-134">Additional command line options</span></span>

- `--no-first-run` <span data-ttu-id="255f6-135">: Deaktivieren Sie die erste Ausführung von Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="255f6-135">: Disable the first Microsoft Edge run experience.</span></span>
- `--kiosk-idle-timeout-minutes` <span data-ttu-id="255f6-136">: Ändern Sie den Zeitraum (in Minuten) nach der letzten Benutzeraktivität, nach dem der Microsoft Edge-Kioskmodus die Benutzersitzung zurücksetzt.</span><span class="sxs-lookup"><span data-stu-id="255f6-136">: Change the time (in minutes) from the last user activity before Microsoft Edge kiosk mode resets the user's session.</span></span> <span data-ttu-id="255f6-137">Die folgenden Werte werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="255f6-137">The following values are supported:</span></span>

  - <span data-ttu-id="255f6-138">Standardwerte</span><span class="sxs-lookup"><span data-stu-id="255f6-138">Default values</span></span>
    - <span data-ttu-id="255f6-139">Vollbildmodus – deaktiviert</span><span class="sxs-lookup"><span data-stu-id="255f6-139">Full screen - turned off</span></span>
    - <span data-ttu-id="255f6-140">Öffentliches Surfen – 5 Minuten</span><span class="sxs-lookup"><span data-stu-id="255f6-140">Public browsing - 5 minutes</span></span>
  - <span data-ttu-id="255f6-141">Zulässige Werte</span><span class="sxs-lookup"><span data-stu-id="255f6-141">Allowed values</span></span>
    - <span data-ttu-id="255f6-142">0 – deaktiviert den Timer</span><span class="sxs-lookup"><span data-stu-id="255f6-142">0 - turns off the timer</span></span>
    - <span data-ttu-id="255f6-143">1-1440 Minuten für das Zurücksetzen für den Leerlaufzeit-Zeitgeber</span><span class="sxs-lookup"><span data-stu-id="255f6-143">1-1440 minutes for reset on idle timer</span></span>

## <span data-ttu-id="255f6-144">Einrichten des Kioskmodus mit zugewiesenem Zugriff</span><span class="sxs-lookup"><span data-stu-id="255f6-144">Set up kiosk mode with assigned access</span></span>

<span data-ttu-id="255f6-145">Der Microsoft Edge-Kioskmodus mit zugewiesenem Zugriff ist derzeit für Tests mit dem neuesten [Windows 10 Insider Preview-Build](https://insider.windows.com/), Version 20215 oder höher, und mit dem [Microsoft Edge Dev Channel](https://www.microsoftedgeinsider.com/download), Version 87.0.644 oder höher, verfügbar.</span><span class="sxs-lookup"><span data-stu-id="255f6-145">Microsoft Edge kiosk mode with assigned access is currently available for testing with the latest [Windows 10 Insider Preview Build](https://insider.windows.com/), version 20215 or higher, and with the [Microsoft Edge Dev Channel](https://www.microsoftedgeinsider.com/download), version 87.0.644 or higher.</span></span>

**<span data-ttu-id="255f6-146">Wie erhalte ich den Windows Insider Preview-Build?</span><span class="sxs-lookup"><span data-stu-id="255f6-146">How do I get the Windows Insiders preview?</span></span>**

<span data-ttu-id="255f6-147">Wenn Sie einen Windows 10 Insider Preview-Build auf einem PC installieren möchten, folgen Sie den Anweisungen unter [Erste Schritte mit Windows 10 Insider Preview-Builds](https://docs.microsoft.com/windows-insider/get-started).</span><span class="sxs-lookup"><span data-stu-id="255f6-147">To install a Windows 10 Insider Preview Build on a PC, follow the instructions in [Getting started with Windows 10 Insider Preview Builds](https://docs.microsoft.com/windows-insider/get-started).</span></span>

### <span data-ttu-id="255f6-148">Konfigurieren mithilfe der Windows-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="255f6-148">Configure using Windows Settings</span></span>

<span data-ttu-id="255f6-149">Die Windows-Einstellungen sind die einfachste Möglichkeit zum Einrichten von ein oder zwei Einzel-App-Kioskgeräten.</span><span class="sxs-lookup"><span data-stu-id="255f6-149">Windows Settings is the simplest way to set up one or two single-app kiosk devices.</span></span> <span data-ttu-id="255f6-150">Führen Sie die folgenden Schritte aus, um einen Einzel-App-Kioskcomputer einzurichten.</span><span class="sxs-lookup"><span data-stu-id="255f6-150">Use the following steps to set up a single-app kiosk computer.</span></span>

1. <span data-ttu-id="255f6-151">Installieren Sie die neueste Windows 10 Insider Preview-Version (20215 oder höher).</span><span class="sxs-lookup"><span data-stu-id="255f6-151">Install the latest Windows 10 Insider Preview, version 20215 or higher.</span></span> <span data-ttu-id="255f6-152">Folgen Sie den Anweisungen unter [Erste Schritte mit Windows 10 Insider Preview-Builds](https://docs.microsoft.com/windows-insider/get-started).</span><span class="sxs-lookup"><span data-stu-id="255f6-152">Follow the instructions in [Getting started with Windows 10 Insider Preview Builds](https://docs.microsoft.com/windows-insider/get-started).</span></span>
2. <span data-ttu-id="255f6-153">Installieren Sie die neueste Version von [Microsoft Edge Dev Channel](https://www.microsoftedgeinsider.com/download) (87.0.644 oder höher).</span><span class="sxs-lookup"><span data-stu-id="255f6-153">Install the latest version of [Microsoft Edge Dev channel](https://www.microsoftedgeinsider.com/download), 87.0.644 or higher.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="255f6-154">Da eine Installation auf Geräteebene erforderlich ist, wird nur ein nicht-Canary-Kanal unterstützt.</span><span class="sxs-lookup"><span data-stu-id="255f6-154">Because a device level installation is required, only a non-Canary channel is supported.</span></span>

3. <span data-ttu-id="255f6-155">Öffnen Sie auf dem Kiosk-Computer die Windows-Einstellungen, und geben Sie im Suchfeld "Kiosk" ein.</span><span class="sxs-lookup"><span data-stu-id="255f6-155">On the kiosk computer, open Windows Settings, and type "kiosk" in the search field.</span></span> <span data-ttu-id="255f6-156">Wählen Sie  **Einen Kiosk einrichten (zugewiesener Zugriff)** aus, das im nächsten Screenshot dargestellt ist, um das Dialogfeld zum Erstellen des Kiosks zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="255f6-156">Select  **Set up a kiosk (assigned access)**, shown in the next screenshot to open the dialog for creating the kiosk.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-1-assigned-access.png" alt-text="Einrichten eines Kiosks mit zugewiesenem Zugriff":::

4. <span data-ttu-id="255f6-158">Klicken Sie auf der Seite **Einen Kiosk einrichten**  auf **Erste Schritte**.</span><span class="sxs-lookup"><span data-stu-id="255f6-158">On the **Set up a kiosk** page, click **Get started**.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-2-get-started.png" alt-text="Seite "Kiosk" – erste Schritte":::

5. <span data-ttu-id="255f6-160">Geben Sie einen Namen ein, um ein neues Kioskkonto zu erstellen, oder wählen Sie ein vorhandenes Konto aus der Dropdownliste aus, und klicken Sie dann auf  **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="255f6-160">Type a name to create a new kiosk account or choose an existing account from the populated dropdown list and then click **Next**.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-3-create-account.png" alt-text="Kioskmodus – Konto erstellen":::

6. <span data-ttu-id="255f6-162">Wählen Sie auf der Seite **Kiosk-App auswählen**  die Option **Microsoft Edge** aus, und klicken Sie dann auf  **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="255f6-162">On the **Choose a kiosk app** page, select **Microsoft Edge** and then click **Next**.</span></span>

   > [!NOTE]
   > <span data-ttu-id="255f6-163">Dies gilt nur für Microsoft Edge Dev, Beta und Stable-Kanäle.</span><span class="sxs-lookup"><span data-stu-id="255f6-163">This only applies to Microsoft Edge Dev, Beta, and Stable channels.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-4-pick-app.png" alt-text="Kioskmodus – App auswählen":::

7. <span data-ttu-id="255f6-165">Wählen Sie eine der folgenden Optionen für die Darstellung von Microsoft Edge aus, wenn er im Kioskmodus ausgeführt wird:</span><span class="sxs-lookup"><span data-stu-id="255f6-165">Pick one of the following options for how Microsoft Edge displays when running in kiosk mode:</span></span>

   - <span data-ttu-id="255f6-166">Digitale/interaktive Beschilderung: Zeigt eine bestimmte Website im Vollbildmodus an, dabei wird Microsoft Edge ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="255f6-166">Digital/Interactive signage - Displays a specific site in full-screen mode, running Microsoft Edge.</span></span>
   - <span data-ttu-id="255f6-167">Öffentliches Surfen: Führt eine eingeschränkte Version von Microsoft Edge mit mehreren Tabs aus.</span><span class="sxs-lookup"><span data-stu-id="255f6-167">Public browser - Runs a limited multi-tab version of Microsoft Edge.</span></span>

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-5a-digital-sign.png" alt-text="Kioskmodus – digitale Beschilderung im Vollbildmodus":::

8. <span data-ttu-id="255f6-169">Wählen Sie \*\* Weiter\*\* aus.</span><span class="sxs-lookup"><span data-stu-id="255f6-169">Select **Next**.</span></span>
9. <span data-ttu-id="255f6-170">Geben Sie die URL ein, die beim Start des Kiosks geladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="255f6-170">Type the URL to load when the kiosk launches.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-6-enter-url.png" alt-text="Kioskmodus – URL eingeben":::

10. <span data-ttu-id="255f6-172">Übernehmen Sie den Standardwert von 5 Minuten für die Leerlaufzeit, oder geben Sie einen eigenen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="255f6-172">Accept the default value of 5 minutes for the idle time or provide a value of your own.</span></span>

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-7-enter-idle-time.png" alt-text="Kioskmodus – Leerlaufzeit eingeben":::

11. <span data-ttu-id="255f6-174">Klicken Sie auf  **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="255f6-174">Click **Next**.</span></span>
12. <span data-ttu-id="255f6-175">Schließen Sie das Fenster  **Einstellungen** , um Ihre Auswahl zu speichern und anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="255f6-175">Close the **Settings** window to save and apply your choices.</span></span>

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode--8-done.png" alt-text="Kioskmodus – Einrichten abschließen":::

13. <span data-ttu-id="255f6-177">Melden Sie sich vom Kioskgerät ab, und melden Sie sich mit dem lokalen Kioskkonto an, um die Konfiguration zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="255f6-177">Sign off from the kiosk device and sign in with the local kiosk account to validate the configuration.</span></span>

## <span data-ttu-id="255f6-178">Funktionale Beschränkungen</span><span class="sxs-lookup"><span data-stu-id="255f6-178">Functional limitations</span></span>

<span data-ttu-id="255f6-179">Die Veröffentlichung dieser Preview-Version des Kioskmodus erfolgt im Rahmen unserer kontinuierlichen Bemühungen, das Produkt zu verbessern und neue Features hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="255f6-179">With the release of this preview version of kiosk mode we're continuing work on improving the product and adding new features.</span></span>

<span data-ttu-id="255f6-180">Die folgenden Funktionen werden im Kioskmodus zurzeit zwar nicht unterstützt, wir arbeiten aber daran:</span><span class="sxs-lookup"><span data-stu-id="255f6-180">Although kiosk mode doesn't currently support the following functionality, work is underway on the following features:</span></span>

- <span data-ttu-id="255f6-181">Sammlungen</span><span class="sxs-lookup"><span data-stu-id="255f6-181">Collections</span></span>
- <span data-ttu-id="255f6-182">Extensions</span><span class="sxs-lookup"><span data-stu-id="255f6-182">Extensions</span></span>
- <span data-ttu-id="255f6-183">Internet Explorer-Modus</span><span class="sxs-lookup"><span data-stu-id="255f6-183">Internet Explorer mode</span></span>
- <span data-ttu-id="255f6-184">Windows Defender Application Guard (WDAG)</span><span class="sxs-lookup"><span data-stu-id="255f6-184">Windows Defender Application Guard (WDAG)</span></span>

## <span data-ttu-id="255f6-185">Roadmap</span><span class="sxs-lookup"><span data-stu-id="255f6-185">Roadmap</span></span>

### <span data-ttu-id="255f6-186">Später in diesem Jahr (2020)</span><span class="sxs-lookup"><span data-stu-id="255f6-186">Later this year (2020)</span></span>

<span data-ttu-id="255f6-187">Die folgenden Features werden hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="255f6-187">We'll add the following features:</span></span>

- <span data-ttu-id="255f6-188">Sitzung beenden</span><span class="sxs-lookup"><span data-stu-id="255f6-188">End session button</span></span>
- <span data-ttu-id="255f6-189">Schreibgeschützte URL-Adressleiste</span><span class="sxs-lookup"><span data-stu-id="255f6-189">Read only URL address bar</span></span>  
  - <span data-ttu-id="255f6-190">Konfigurierbar mit Gruppenrichtlinien</span><span class="sxs-lookup"><span data-stu-id="255f6-190">Configurable with group policy</span></span>
  - <span data-ttu-id="255f6-191">Wenn diese Option aktiviert ist, werden die Benutzer daran gehindert, die Adressleisten-URL zu ändern, um zu einer anderen Seite zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="255f6-191">When enabled, users will be prevented from editing the address bar URL to try navigating away to another page.</span></span>

- <span data-ttu-id="255f6-192">Weitere Sperrfunktionen:</span><span class="sxs-lookup"><span data-stu-id="255f6-192">More lockdown functions:</span></span>

  - <span data-ttu-id="255f6-193">Weitere Tastenkombinationen werden blockiert (beispielsweise STRG + N).</span><span class="sxs-lookup"><span data-stu-id="255f6-193">Additional accelerators will be blocked (for example, CTRL+N)</span></span>
  - <span data-ttu-id="255f6-194">Im "..."-Menü werden nur erforderliche Optionen aktiviert sein (z. B. "Drucken", "Hilfe", "Feedback" und "Laut vorlesen").</span><span class="sxs-lookup"><span data-stu-id="255f6-194">The "…" settings menu will enable only required options (for example, Print, Help,  Feedback, and Read aloud)</span></span>
  - <span data-ttu-id="255f6-195">Sperrung weiterer *edge://*-Seiten (z. B. *Edge://Settings*)</span><span class="sxs-lookup"><span data-stu-id="255f6-195">Additional *edge://* pages lockdown (for example, *edge://settings*)</span></span>
  - <span data-ttu-id="255f6-196">Konfigurieren der Druckoptionen-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="255f6-196">Configure print options UI</span></span>
  - <span data-ttu-id="255f6-197">Einschränken des Datei-Explorers auf den Downloadordner</span><span class="sxs-lookup"><span data-stu-id="255f6-197">Limiting file explorer to the download folder only.</span></span>

### <span data-ttu-id="255f6-198">Anfang 2021</span><span class="sxs-lookup"><span data-stu-id="255f6-198">In early 2021</span></span>

<span data-ttu-id="255f6-199">Unterstützung und Funktionen, die hinzukommen werden:</span><span class="sxs-lookup"><span data-stu-id="255f6-199">We'll add the following support and features:</span></span>

- <span data-ttu-id="255f6-200">Allgemeine Verfügbarkeit des Microsoft Edge-Kioskmodus mit zugewiesenem Zugriff (Einzel-App) für Windows.</span><span class="sxs-lookup"><span data-stu-id="255f6-200">General availability of Microsoft Edge kiosk mode with assigned access single app on Windows.</span></span>
- <span data-ttu-id="255f6-201">Zusätzliche Features für Parität mit Vorgängerversion von Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="255f6-201">Additional features for parity with Microsoft Edge Legacy.</span></span>
- <span data-ttu-id="255f6-202">Integration in Intune zum Konfigurieren von Geräten über die Profil-Benutzerumgebung im Kioskmodus</span><span class="sxs-lookup"><span data-stu-id="255f6-202">Integration with Intune to configure devices using kiosk mode profile UX.</span></span>

## <span data-ttu-id="255f6-203">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="255f6-203">See also</span></span>

- [<span data-ttu-id="255f6-204">Konfigurieren von Kiosken und digitalen Anmeldungen in Windows-Desktopeditionen</span><span class="sxs-lookup"><span data-stu-id="255f6-204">Configure kiosks and digital signs on Windows desktop editions</span></span>](https://docs.microsoft.com/windows/configuration/kiosk-methods)
- [<span data-ttu-id="255f6-205">Bereitstellen des Microsoft Edge Legacy-Kioskmodus</span><span class="sxs-lookup"><span data-stu-id="255f6-205">Deploy Microsoft Edge Legacy kiosk mode</span></span>](https://aka.ms/edgekioskmode) 
- [<span data-ttu-id="255f6-206">Planen Ihrer Bereitstellung von Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="255f6-206">Plan your deployment of Microsoft Edge</span></span>](deploy-edge-plan-deployment.md)
- [<span data-ttu-id="255f6-207">Angebotsseite für Microsoft Edge für Unternehmen</span><span class="sxs-lookup"><span data-stu-id="255f6-207">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)