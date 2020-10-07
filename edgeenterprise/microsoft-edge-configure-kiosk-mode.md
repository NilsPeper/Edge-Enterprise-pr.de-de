---
title: Konfigurieren des Microsoft Edge-Kioskmodus
ms.author: aguta
author: aguta
manager: srugh
ms.date: 10/05/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Konfigurieren des Microsoft Edge-Kioskmodus
ms.openlocfilehash: 799b3dd4b7fc96f0b8e5cb718bca98fd4f38ec15
ms.sourcegitcommit: 78905f66f4a6590a57c8f2bf808af92106b62996
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/05/2020
ms.locfileid: "11094862"
---
# <span data-ttu-id="7279b-103">Konfigurieren des Microsoft Edge-Kioskmodus</span><span class="sxs-lookup"><span data-stu-id="7279b-103">Configure Microsoft Edge kiosk mode</span></span>

<span data-ttu-id="7279b-104">In diesem Artikel wird beschrieben, wie Sie die Optionen für den Microsoft Edge-Kioskmodus Ihren Anforderungen entsprechend konfigurieren können.</span><span class="sxs-lookup"><span data-stu-id="7279b-104">This article describes how to configure Microsoft Edge kiosk mode options that you can pilot.</span></span> <span data-ttu-id="7279b-105">Eine Roadmap zukünftiger Features wird ebenfalls vorgestellt.</span><span class="sxs-lookup"><span data-stu-id="7279b-105">There's also a roadmap of features we are targeting.</span></span>

> [!NOTE]
> <span data-ttu-id="7279b-106">Dieser Artikel bezieht sich auf Microsoft Edge Version 87 oder neuer.</span><span class="sxs-lookup"><span data-stu-id="7279b-106">This article applies to Microsoft Edge version 87 or later.</span></span>

## <span data-ttu-id="7279b-107">Übersicht</span><span class="sxs-lookup"><span data-stu-id="7279b-107">Overview</span></span>

<span data-ttu-id="7279b-108">Im Microsoft Edge-Kiosk-Modus sind zwei gesperrte Browserumgebungen verfügbar, damit Organisationen optimale Umgebungen für ihre Kunden gestalten, verwalten und anbieten können.</span><span class="sxs-lookup"><span data-stu-id="7279b-108">Microsoft Edge kiosk mode offers two lockdown experiences of the browser so organizations can create, manage, and provide the best experience for their customers.</span></span> <span data-ttu-id="7279b-109">Die folgenden gesperrten Umgebungen sind verfügbar:</span><span class="sxs-lookup"><span data-stu-id="7279b-109">The following lockdown experiences are available:</span></span>  

- <span data-ttu-id="7279b-110">Bei der digitalen/interaktiven Beschilderung wird eine bestimmte Website im Vollbildmodus angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7279b-110">The Digital/Interactive signage experience displays a specific site in full-screen mode.</span></span>
- <span data-ttu-id="7279b-111">Bei der Umgebung für öffentliches Surfen wird eine eingeschränkte Version von Microsoft Edge mit mehreren Tabs ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7279b-111">The public-browsing experience runs a limited multi-tab version of Microsoft Edge.</span></span>

<span data-ttu-id="7279b-112">In beiden Fällen wird eine Microsoft Edge-InPrivate-Sitzung ausgeführt, wodurch die Benutzerdaten geschützt sind.</span><span class="sxs-lookup"><span data-stu-id="7279b-112">Both experiences are running a Microsoft Edge InPrivate session, which protects user data.</span></span>

## <span data-ttu-id="7279b-113">Einrichten des Microsoft Edge-Kioskmodus</span><span class="sxs-lookup"><span data-stu-id="7279b-113">Set up Microsoft Edge kiosk mode</span></span>

<span data-ttu-id="7279b-114">Jetzt können Sie mit Microsoft Edge Canary, Version 87, eine erste Sammlung von Kioskmodus-Features testen.</span><span class="sxs-lookup"><span data-stu-id="7279b-114">An initial set of kiosk mode features are now available to test with Microsoft Edge Canary Channel, version 87.</span></span> <span data-ttu-id="7279b-115">Sie können Microsoft Edge Canary über die Seite [Microsoft Edge Insider Channels](https://www.microsoftedgeinsider.com/download) herunterladen.</span><span class="sxs-lookup"><span data-stu-id="7279b-115">You can download Microsoft Edge Canary from the [Microsoft Edge Insider Channels](https://www.microsoftedgeinsider.com/download) page.</span></span>

### <span data-ttu-id="7279b-116">Kioskmodus-Features</span><span class="sxs-lookup"><span data-stu-id="7279b-116">Kiosk mode features</span></span>

<span data-ttu-id="7279b-117">Die folgenden Features sind verfügbar:</span><span class="sxs-lookup"><span data-stu-id="7279b-117">The following features are available:</span></span>

- <span data-ttu-id="7279b-118">Die InPrivate-Navigation schützt Benutzerdaten durch das Löschen von Browserdaten und Downloads, wenn die Sitzung beendet wird.</span><span class="sxs-lookup"><span data-stu-id="7279b-118">InPrivate navigation protects user data by deleting browser data and downloads when the session ends.</span></span>
- <span data-ttu-id="7279b-119">Eine Richtlinie zum Konfigurieren des Löschens von Downloads beim Beenden.</span><span class="sxs-lookup"><span data-stu-id="7279b-119">A policy to configure Delete downloads on exit.</span></span>
- <span data-ttu-id="7279b-120">Die Option zum Zurücksetzen der Benutzersitzung nach einer bestimmten Zeit der Inaktivität.</span><span class="sxs-lookup"><span data-stu-id="7279b-120">The option to reset a user session after a certain period of inactivity.</span></span>
- <span data-ttu-id="7279b-121">Eine erste Reihe verfügbarer Sperrfunktionen.</span><span class="sxs-lookup"><span data-stu-id="7279b-121">An initial set of lockdown functionality.</span></span> <span data-ttu-id="7279b-122">Die folgenden Funktionen sind verfügbar:</span><span class="sxs-lookup"><span data-stu-id="7279b-122">The following functions are available:</span></span>

  - <span data-ttu-id="7279b-123">Maus-Kontextmenü</span><span class="sxs-lookup"><span data-stu-id="7279b-123">Mouse context menu</span></span>
  - <span data-ttu-id="7279b-124">F12 Entwicklertools</span><span class="sxs-lookup"><span data-stu-id="7279b-124">F12 Developer Tools</span></span>
  - <span data-ttu-id="7279b-125">F11 Beenden des Vollbildmodus (im Vollbildmodus)</span><span class="sxs-lookup"><span data-stu-id="7279b-125">F11 Exit full screen (while in full screen mode)</span></span>
  - <span data-ttu-id="7279b-126">Blockieren der ersten Reihe von *Edge://*-Seiten</span><span class="sxs-lookup"><span data-stu-id="7279b-126">Blocking of the initial set of *Edge://* pages</span></span>

> [!NOTE]
> <span data-ttu-id="7279b-127">Im Laufe der Weiterentwicklung des Kioskmodus werden auch weitere Features verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="7279b-127">As kiosk mode evolves, more features will be available.</span></span>

## <span data-ttu-id="7279b-128">Verwenden der Kioskmodus-Features</span><span class="sxs-lookup"><span data-stu-id="7279b-128">Use kiosk mode features</span></span>

<span data-ttu-id="7279b-129">Die Microsoft Edge-Kioskmodus-Features können mit den folgenden Windows 10-Befehlszeilenoptionen aufgerufen werden:</span><span class="sxs-lookup"><span data-stu-id="7279b-129">You can invoke Microsoft Edge kiosk mode features can be invoked with the following Windows 10 command line options:</span></span>

- <span data-ttu-id="7279b-130">Kioskmodus "Digitale/interaktive Beschilderung":</span><span class="sxs-lookup"><span data-stu-id="7279b-130">Kiosk mode Digital/Interactive signage:</span></span> `msedge.exe --kiosk www.contoso.com --edge-kiosk-type=fullscreen`
- <span data-ttu-id="7279b-131">Kioskmodus "Öffentliches Surfen":</span><span class="sxs-lookup"><span data-stu-id="7279b-131">Kiosk mode public browsing:</span></span> `msedge.exe --kiosk www.contoso.com --edge-kiosk-type=public-browsing`

### <span data-ttu-id="7279b-132">Zusätzliche Befehlszeilenoptionen</span><span class="sxs-lookup"><span data-stu-id="7279b-132">Additional command line options</span></span>

- `--no-first-run` <span data-ttu-id="7279b-133">: Deaktivieren Sie die erste Ausführung von Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7279b-133">: Disable the first Microsoft Edge run experience.</span></span>
- `--kiosk-idle-timeout-minutes` <span data-ttu-id="7279b-134">: Ändern Sie den Zeitraum (in Minuten) nach der letzten Benutzeraktivität, nach dem der Microsoft Edge-Kioskmodus die Benutzersitzung zurücksetzt.</span><span class="sxs-lookup"><span data-stu-id="7279b-134">: Change the time (in minutes) from the last user activity before Microsoft Edge kiosk mode resets the user's session.</span></span> <span data-ttu-id="7279b-135">Die folgenden Werte werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="7279b-135">The following values are supported:</span></span>

  - <span data-ttu-id="7279b-136">Standardwerte</span><span class="sxs-lookup"><span data-stu-id="7279b-136">Default values</span></span>
    - <span data-ttu-id="7279b-137">Vollbildmodus – deaktiviert</span><span class="sxs-lookup"><span data-stu-id="7279b-137">Full screen - turned off</span></span>
    - <span data-ttu-id="7279b-138">Öffentliches Surfen – 5 Minuten</span><span class="sxs-lookup"><span data-stu-id="7279b-138">Public browsing - 5 minutes</span></span>
  - <span data-ttu-id="7279b-139">Zulässige Werte</span><span class="sxs-lookup"><span data-stu-id="7279b-139">Allowed values</span></span>
    - <span data-ttu-id="7279b-140">0 – deaktiviert den Timer</span><span class="sxs-lookup"><span data-stu-id="7279b-140">0 - turns off the timer</span></span>
    - <span data-ttu-id="7279b-141">1-1440 Minuten für das Zurücksetzen für den Leerlaufzeit-Zeitgeber</span><span class="sxs-lookup"><span data-stu-id="7279b-141">1-1440 minutes for reset on idle timer</span></span>

## <span data-ttu-id="7279b-142">Microsoft Edge mit zugewiesenem Zugriff</span><span class="sxs-lookup"><span data-stu-id="7279b-142">Microsoft Edge with assigned access</span></span>

### <span data-ttu-id="7279b-143">Einzel-App-Kiosk</span><span class="sxs-lookup"><span data-stu-id="7279b-143">Single app kiosk</span></span>

<span data-ttu-id="7279b-144">Microsoft Edge unterstützt derzeit eine Teilmenge der gleichen Vorgängerversionen der Microsoft Edge-Kioskmodustypen für den zugewiesenen Zugriff mit einer App mit den folgenden Sperrmoduserfahrungen, digitaler/interaktiver Beschilderung und Public-Browsing.</span><span class="sxs-lookup"><span data-stu-id="7279b-144">Microsoft Edge currently supports a subset of the same Microsoft Edge Legacy kiosk mode types for single-app assigned access with the following lockdown experiences, Digital/Interactive signage and Public-browsing.</span></span>  

<span data-ttu-id="7279b-145">Der Kioskmodus mit zugewiesenem Zugriff ist derzeit für Tests mit dem neuesten  [Windows10 Insider Preview-Build](https://insider.windows.com/), Version 20215 oder höher, und mit dem  [Microsoft Edge Dev Channel](https://www.microsoftedgeinsider.com/download), Version 87.0.644.4 oder höher, verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7279b-145">Kiosk mode with assigned access is currently available for testing with the latest [Windows 10 Insider Preview Build](https://insider.windows.com/), version 20215 or higher, and with the [Microsoft Edge Dev Channel](https://www.microsoftedgeinsider.com/download), version 87.0.644.4 or higher.</span></span>

**<span data-ttu-id="7279b-146">Wie erhalte ich den Windows Insider Preview-Build?</span><span class="sxs-lookup"><span data-stu-id="7279b-146">How do I get the Windows Insiders preview?</span></span>**

<span data-ttu-id="7279b-147">Wenn Sie einen Windows10 Insider Preview-Build auf einem PC installieren möchten, folgen Sie den Anweisungen unter  [Erste Schritte mit Windows10 Insider Preview-Builds](https://docs.microsoft.com/windows-insider/get-started).</span><span class="sxs-lookup"><span data-stu-id="7279b-147">To install a Windows 10 Insider Preview Build on a PC, follow the instructions in [Getting started with Windows 10 Insider Preview Builds](https://docs.microsoft.com/windows-insider/get-started).</span></span>

### <span data-ttu-id="7279b-148">Multi-App-Kiosk</span><span class="sxs-lookup"><span data-stu-id="7279b-148">Multi-app kiosk</span></span>

<span data-ttu-id="7279b-149">Microsoft Edge kann unter Windows10 mit [zugewiesenem Multi-App-Zugriff](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps) ausgeführt werden, was dem Kioskmodustyp „Normales Browsen” von Microsoft Edge Legacy entspricht.</span><span class="sxs-lookup"><span data-stu-id="7279b-149">Microsoft Edge can be run with [multi-app assigned access](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps) on Windows 10, which is the equivalent of Microsoft Edge Legacy "Normal browsing" kiosk mode type.</span></span> <span data-ttu-id="7279b-150">Zum Konfigurieren von Microsoft Edge mit zugewiesenem Multi-App-Zugriff folgen Sie den Anweisungen unter [Einrichten eines Multi-App-Kiosks](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps).</span><span class="sxs-lookup"><span data-stu-id="7279b-150">To configure Microsoft Edge with multi-app assigned access follow the instructions on how to [Set up a multi-app kiosk](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps).</span></span> <span data-ttu-id="7279b-151">(Die AUMID für den Stable-Kanal von Microsoft Edge ist **MSEdge**.)</span><span class="sxs-lookup"><span data-stu-id="7279b-151">(The AUMID for the Microsoft Edge Stable channel is **MSEdge**).</span></span>

<span data-ttu-id="7279b-152">Für das Konfigurieren von Microsoft Edge mit zugewiesenem Multi-App-Zugriff können Sie die [Microsoft Edge-Browserrichtlinien](https://review.docs.microsoft.com/en-us/DeployEdge/microsoft-edge-policies) verwenden, um das Browsingerlebnis Ihren individuellen Anforderungen entsprechend zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="7279b-152">Configure Microsoft Edge kiosk mode When using Microsoft Edge with multi-app assigned access you can use the [Microsoft Edge browser policies](https://review.docs.microsoft.com/en-us/DeployEdge/microsoft-edge-policies) to configure the browsing experience to meet your unique requirements.</span></span>

### <span data-ttu-id="7279b-153">Konfigurieren mithilfe der Windows-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="7279b-153">Configure using Windows Settings</span></span>

<span data-ttu-id="7279b-154">Die Windows-Einstellungen sind die einfachste Möglichkeit zum Einrichten von ein oder zwei Einzel-App-Kioskgeräten.</span><span class="sxs-lookup"><span data-stu-id="7279b-154">Windows Settings is the simplest way to set up one or two single-app kiosk devices.</span></span> <span data-ttu-id="7279b-155">Führen Sie die folgenden Schritte aus, um einen Einzel-App-Kioskcomputer einzurichten.</span><span class="sxs-lookup"><span data-stu-id="7279b-155">Use the following steps to set up a single-app kiosk computer.</span></span>

1. <span data-ttu-id="7279b-156">Installieren Sie die neueste Windows 10 Insider Preview-Version (20215 oder höher).</span><span class="sxs-lookup"><span data-stu-id="7279b-156">Install the latest Windows 10 Insider Preview, version 20215 or higher.</span></span> <span data-ttu-id="7279b-157">Folgen Sie den Anweisungen unter [Erste Schritte mit Windows 10 Insider Preview-Builds](https://docs.microsoft.com/windows-insider/get-started).</span><span class="sxs-lookup"><span data-stu-id="7279b-157">Follow the instructions in [Getting started with Windows 10 Insider Preview Builds](https://docs.microsoft.com/windows-insider/get-started).</span></span>
2. <span data-ttu-id="7279b-158">Installieren Sie die neueste Version von [Microsoft Edge Dev Channel](https://www.microsoftedgeinsider.com/download), Version 87.0.644.4 oder höher.</span><span class="sxs-lookup"><span data-stu-id="7279b-158">Install the latest version of [Microsoft Edge Dev channel](https://www.microsoftedgeinsider.com/download), 87.0.644.4 or higher.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="7279b-159">Da eine Installation auf Geräteebene erforderlich ist, wird nur ein nicht-Canary-Kanal unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7279b-159">Because a device level installation is required, only a non-Canary channel is supported.</span></span>

3. <span data-ttu-id="7279b-160">Öffnen Sie auf dem Kiosk-Computer die Windows-Einstellungen, und geben Sie im Suchfeld "Kiosk" ein.</span><span class="sxs-lookup"><span data-stu-id="7279b-160">On the kiosk computer, open Windows Settings, and type "kiosk" in the search field.</span></span> <span data-ttu-id="7279b-161">Wählen Sie  **Einen Kiosk einrichten (zugewiesener Zugriff)** aus, das im nächsten Screenshot dargestellt ist, um das Dialogfeld zum Erstellen des Kiosks zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="7279b-161">Select  **Set up a kiosk (assigned access)**, shown in the next screenshot to open the dialog for creating the kiosk.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-1-assigned-access.png" alt-text="Einrichten eines Kiosks mit zugewiesenem Zugriff":::

4. <span data-ttu-id="7279b-163">Klicken Sie auf der Seite **Einen Kiosk einrichten**  auf **Erste Schritte**.</span><span class="sxs-lookup"><span data-stu-id="7279b-163">On the **Set up a kiosk** page, click **Get started**.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-2-get-started.png" alt-text="Einrichten eines Kiosks mit zugewiesenem Zugriff":::

5. <span data-ttu-id="7279b-165">Geben Sie einen Namen ein, um ein neues Kioskkonto zu erstellen, oder wählen Sie ein vorhandenes Konto aus der Dropdownliste aus, und klicken Sie dann auf  **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="7279b-165">Type a name to create a new kiosk account or choose an existing account from the populated dropdown list and then click **Next**.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-3-create-account.png" alt-text="Einrichten eines Kiosks mit zugewiesenem Zugriff":::

6. <span data-ttu-id="7279b-167">Wählen Sie auf der Seite **Kiosk-App auswählen**  die Option **Microsoft Edge** aus, und klicken Sie dann auf  **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="7279b-167">On the **Choose a kiosk app** page, select **Microsoft Edge** and then click **Next**.</span></span>

   > [!NOTE]
   > <span data-ttu-id="7279b-168">Dies gilt nur für Microsoft Edge Dev, Beta und Stable-Kanäle.</span><span class="sxs-lookup"><span data-stu-id="7279b-168">This only applies to Microsoft Edge Dev, Beta, and Stable channels.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-4-pick-app.png" alt-text="Einrichten eines Kiosks mit zugewiesenem Zugriff":::

7. <span data-ttu-id="7279b-170">Wählen Sie eine der folgenden Optionen für die Darstellung von Microsoft Edge aus, wenn er im Kioskmodus ausgeführt wird:</span><span class="sxs-lookup"><span data-stu-id="7279b-170">Pick one of the following options for how Microsoft Edge displays when running in kiosk mode:</span></span>

   - <span data-ttu-id="7279b-171">Digitale/interaktive Beschilderung: Zeigt eine bestimmte Website im Vollbildmodus an, dabei wird Microsoft Edge ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7279b-171">Digital/Interactive signage - Displays a specific site in full-screen mode, running Microsoft Edge.</span></span>
   - <span data-ttu-id="7279b-172">Öffentliches Surfen: Führt eine eingeschränkte Version von Microsoft Edge mit mehreren Tabs aus.</span><span class="sxs-lookup"><span data-stu-id="7279b-172">Public browser - Runs a limited multi-tab version of Microsoft Edge.</span></span>

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-5a-digital-sign.png" alt-text="Einrichten eines Kiosks mit zugewiesenem Zugriff":::

8. <span data-ttu-id="7279b-174">Wählen Sie \*\* Weiter\*\* aus.</span><span class="sxs-lookup"><span data-stu-id="7279b-174">Select **Next**.</span></span>
9. <span data-ttu-id="7279b-175">Geben Sie die URL ein, die beim Start des Kiosks geladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="7279b-175">Type the URL to load when the kiosk launches.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-6-enter-url.png" alt-text="Einrichten eines Kiosks mit zugewiesenem Zugriff":::

10. <span data-ttu-id="7279b-177">Übernehmen Sie den Standardwert von 5 Minuten für die Leerlaufzeit, oder geben Sie einen eigenen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="7279b-177">Accept the default value of 5 minutes for the idle time or provide a value of your own.</span></span>

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-7-enter-idle-time.png" alt-text="Einrichten eines Kiosks mit zugewiesenem Zugriff":::

11. <span data-ttu-id="7279b-179">Klicken Sie auf  **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="7279b-179">Click **Next**.</span></span>
12. <span data-ttu-id="7279b-180">Schließen Sie das Fenster  **Einstellungen** , um Ihre Auswahl zu speichern und anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="7279b-180">Close the **Settings** window to save and apply your choices.</span></span>

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode--8-done.png" alt-text="Einrichten eines Kiosks mit zugewiesenem Zugriff":::

13. <span data-ttu-id="7279b-182">Melden Sie sich vom Kioskgerät ab, und melden Sie sich mit dem lokalen Kioskkonto an, um die Konfiguration zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="7279b-182">Sign off from the kiosk device and sign in with the local kiosk account to validate the configuration.</span></span>

## <span data-ttu-id="7279b-183">Funktionale Beschränkungen</span><span class="sxs-lookup"><span data-stu-id="7279b-183">Functional limitations</span></span>

<span data-ttu-id="7279b-184">Die Veröffentlichung dieser Preview-Version des Kioskmodus erfolgt im Rahmen unserer kontinuierlichen Bemühungen, das Produkt zu verbessern und neue Features hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="7279b-184">With the release of this preview version of kiosk mode we're continuing work on improving the product and adding new features.</span></span>

<span data-ttu-id="7279b-185">Die folgenden Funktionen werden im Kioskmodus zurzeit zwar nicht unterstützt, wir arbeiten aber daran:</span><span class="sxs-lookup"><span data-stu-id="7279b-185">Although kiosk mode doesn't currently support the following functionality, work is underway on the following features:</span></span>

- <span data-ttu-id="7279b-186">Sammlungen</span><span class="sxs-lookup"><span data-stu-id="7279b-186">Collections</span></span>
- <span data-ttu-id="7279b-187">Extensions</span><span class="sxs-lookup"><span data-stu-id="7279b-187">Extensions</span></span>
- <span data-ttu-id="7279b-188">Internet Explorer-Modus</span><span class="sxs-lookup"><span data-stu-id="7279b-188">Internet Explorer mode</span></span>
- <span data-ttu-id="7279b-189">Windows Defender Application Guard (WDAG)</span><span class="sxs-lookup"><span data-stu-id="7279b-189">Windows Defender Application Guard (WDAG)</span></span>

## <span data-ttu-id="7279b-190">Roadmap</span><span class="sxs-lookup"><span data-stu-id="7279b-190">Roadmap</span></span>

### <span data-ttu-id="7279b-191">Später in diesem Jahr (2020)</span><span class="sxs-lookup"><span data-stu-id="7279b-191">Later this year (2020)</span></span>

<span data-ttu-id="7279b-192">Die folgenden Features werden hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="7279b-192">We'll add the following features:</span></span>

- <span data-ttu-id="7279b-193">Sitzung beenden</span><span class="sxs-lookup"><span data-stu-id="7279b-193">End session button</span></span>
- <span data-ttu-id="7279b-194">Schreibgeschützte Adressleiste</span><span class="sxs-lookup"><span data-stu-id="7279b-194">Read only address bar</span></span>  
  - <span data-ttu-id="7279b-195">Konfigurierbar mit Gruppenrichtlinien</span><span class="sxs-lookup"><span data-stu-id="7279b-195">Configurable with group policy</span></span>
  - <span data-ttu-id="7279b-196">Wenn diese Option aktiviert ist, werden die Benutzer daran gehindert, die Adressleiste zu ändern, um zu einer anderen Seite zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="7279b-196">When enabled, users will be prevented from editing the address bar and navigating to another page.</span></span>

- <span data-ttu-id="7279b-197">Weitere Sperrfunktionen:</span><span class="sxs-lookup"><span data-stu-id="7279b-197">More lockdown functions:</span></span>

  - <span data-ttu-id="7279b-198">Weitere Tastenkombinationen werden blockiert (beispielsweise STRG + N).</span><span class="sxs-lookup"><span data-stu-id="7279b-198">Additional accelerators will be blocked (for example, CTRL+N)</span></span>
  - <span data-ttu-id="7279b-199">Im "..."-Menü werden nur erforderliche Optionen aktiviert sein (z. B. "Drucken", "Hilfe", "Feedback" und "Laut vorlesen").</span><span class="sxs-lookup"><span data-stu-id="7279b-199">The "…" settings menu will enable only required options (for example, Print, Help,  Feedback, and Read aloud)</span></span>
  - <span data-ttu-id="7279b-200">Sperrung weiterer *edge://*-Seiten (z. B. *Edge://Settings*)</span><span class="sxs-lookup"><span data-stu-id="7279b-200">Additional *edge://* pages lockdown (for example, *edge://settings*)</span></span>
  - <span data-ttu-id="7279b-201">Konfigurieren der Druckoptionen-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="7279b-201">Configure print options UI</span></span>
  - <span data-ttu-id="7279b-202">Einschränken des Datei-Explorers auf den Downloadordner</span><span class="sxs-lookup"><span data-stu-id="7279b-202">Limiting file explorer to the download folder only.</span></span>

### <span data-ttu-id="7279b-203">Anfang 2021</span><span class="sxs-lookup"><span data-stu-id="7279b-203">In early 2021</span></span>

<span data-ttu-id="7279b-204">Unterstützung und Funktionen, die hinzukommen werden:</span><span class="sxs-lookup"><span data-stu-id="7279b-204">We'll add the following support and features:</span></span>

- <span data-ttu-id="7279b-205">Allgemeine Verfügbarkeit des Microsoft Edge-Kioskmodus mit zugewiesenem Zugriff (Einzel-App) für Windows.</span><span class="sxs-lookup"><span data-stu-id="7279b-205">General availability of Microsoft Edge kiosk mode with assigned access single app on Windows.</span></span>
- <span data-ttu-id="7279b-206">Zusätzliche Features für Parität mit Vorgängerversion von Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="7279b-206">Additional features for parity with Microsoft Edge Legacy.</span></span>
- <span data-ttu-id="7279b-207">Integration in Intune zum Konfigurieren von Geräten über die Profil-Benutzerumgebung im Kioskmodus</span><span class="sxs-lookup"><span data-stu-id="7279b-207">Integration with Intune to configure devices using kiosk mode profile UX.</span></span>

## <span data-ttu-id="7279b-208">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7279b-208">See also</span></span>

- [<span data-ttu-id="7279b-209">Konfigurieren von Kiosken und digitalen Anmeldungen in Windows-Desktopeditionen</span><span class="sxs-lookup"><span data-stu-id="7279b-209">Configure kiosks and digital signs on Windows desktop editions</span></span>](https://docs.microsoft.com/windows/configuration/kiosk-methods)
- [<span data-ttu-id="7279b-210">Bereitstellen des Microsoft Edge Legacy-Kioskmodus</span><span class="sxs-lookup"><span data-stu-id="7279b-210">Deploy Microsoft Edge Legacy kiosk mode</span></span>](https://aka.ms/edgekioskmode)
- [<span data-ttu-id="7279b-211">Planen Ihrer Bereitstellung von Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="7279b-211">Plan your deployment of Microsoft Edge</span></span>](deploy-edge-plan-deployment.md)
- [<span data-ttu-id="7279b-212">Angebotsseite für Microsoft Edge für Unternehmen</span><span class="sxs-lookup"><span data-stu-id="7279b-212">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
