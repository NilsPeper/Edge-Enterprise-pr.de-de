---
title: Dokumentation für die Microsoft Edge Update-Richtlinie
ms.author: stmoody
author: brianalt-msft
manager: tahills
ms.date: 06/10/2020
audience: ITPro
ms.topic: reference
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
ms.custom: ''
description: Dokumentation für alle vom Microsoft Edge Updater unterstützten Richtlinien
ms.openlocfilehash: d772d8dd6f60b89e9bd12a77b740e5fad699756a
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/31/2020
ms.locfileid: "10980012"
---
# <span data-ttu-id="20839-103">Microsoft Edge – Update-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="20839-103">Microsoft Edge - Update policies</span></span>
<span data-ttu-id="20839-104">Die neueste Version von Microsoft Edge enthält die folgenden Richtlinien, mit denen Sie steuern können, wie und wann Microsoft Edge aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="20839-104">The latest version of Microsoft Edge includes the following policies that you can use to control how and when Microsoft Edge is updated.</span></span>

           
<span data-ttu-id="20839-105">Weitere Informationen zu anderen in Microsoft Edge verfügbaren Richtlinien finden Sie in der [Microsoft Edge Referenz für Browserrichtlinien](microsoft-edge-policies.md)</span><span class="sxs-lookup"><span data-stu-id="20839-105">For information about other policies available in Microsoft Edge, check out [Microsoft Edge browser policy reference](microsoft-edge-policies.md)</span></span>
> [!NOTE]
> <span data-ttu-id="20839-106">Dieser Artikel bezieht sich auf Microsoft Edge Version 77 oder höher.</span><span class="sxs-lookup"><span data-stu-id="20839-106">This article applies to Microsoft Edge version 77 or later.</span></span>

## <span data-ttu-id="20839-107">Verfügbare Richtlinien</span><span class="sxs-lookup"><span data-stu-id="20839-107">Available policies</span></span>
<span data-ttu-id="20839-108">In dieser Tabelle sind sämtliche, in dieser Version von Microsoft Edge verfügbaren Update-bezogenen Gruppenrichtlinien aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="20839-108">These tables lists all of the update-related group policies available in this release of Microsoft Edge.</span></span> <span data-ttu-id="20839-109">Über die Links in der folgenden Tabelle erhalten Sie weitere Einzelheiten zu bestimmten Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="20839-109">Use the links in the table to get more details about specific policies.</span></span>

|||
|-|-|
|[<span data-ttu-id="20839-110">Anwendungen</span><span class="sxs-lookup"><span data-stu-id="20839-110">Applications</span></span>](#applications)|[<span data-ttu-id="20839-111">Voreinstellungen</span><span class="sxs-lookup"><span data-stu-id="20839-111">Preferences</span></span>](#preferences)|
|[<span data-ttu-id="20839-112">Proxyserver</span><span class="sxs-lookup"><span data-stu-id="20839-112">Proxy Server</span></span>](#proxy-server)||

### [<span data-ttu-id="20839-113">Anwendungen</span><span class="sxs-lookup"><span data-stu-id="20839-113">Applications</span></span>](#applications-policies)
|<span data-ttu-id="20839-114">Richtlinienname</span><span class="sxs-lookup"><span data-stu-id="20839-114">Policy Name</span></span>|<span data-ttu-id="20839-115">Beschriftung</span><span class="sxs-lookup"><span data-stu-id="20839-115">Caption</span></span>|
|-|-|
|[<span data-ttu-id="20839-116">InstallDefault</span><span class="sxs-lookup"><span data-stu-id="20839-116">InstallDefault</span></span>](#installdefault)|<span data-ttu-id="20839-117">Standardinstallation zulassen</span><span class="sxs-lookup"><span data-stu-id="20839-117">Allow installation default</span></span>|
|[<span data-ttu-id="20839-118">UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="20839-118">UpdateDefault</span></span>](#updatedefault)|<span data-ttu-id="20839-119">Die Updaterichtlinie überschreibt die Standardrichtlinie</span><span class="sxs-lookup"><span data-stu-id="20839-119">Update policy override default</span></span>|
|[<span data-ttu-id="20839-120">Installieren</span><span class="sxs-lookup"><span data-stu-id="20839-120">Install</span></span>](#install)|<span data-ttu-id="20839-121">Installation zulassen (pro Kanal)</span><span class="sxs-lookup"><span data-stu-id="20839-121">Allow installation (per channel)</span></span>|
|[<span data-ttu-id="20839-122">Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="20839-122">Update</span></span>](#update)|<span data-ttu-id="20839-123">Außerkraftsetzung von Updaterichtlinien (pro Kanal)</span><span class="sxs-lookup"><span data-stu-id="20839-123">Update policy override (per channel)</span></span>|
|[<span data-ttu-id="20839-124">Allowsxs</span><span class="sxs-lookup"><span data-stu-id="20839-124">Allowsxs</span></span>](#allowsxs)|<span data-ttu-id="20839-125">Microsoft Edge Seite-an-Seite-Browserumgebung zulassen</span><span class="sxs-lookup"><span data-stu-id="20839-125">Allow Microsoft Edge Side by Side browser experience</span></span>|
|[<span data-ttu-id="20839-126">CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="20839-126">CreateDesktopShortcutDefault</span></span>](#createdesktopshortcutdefault)|<span data-ttu-id="20839-127">Standardeinstellung für das Verhindern der Erstellung von Desktopverknüpfungen bei der Installation</span><span class="sxs-lookup"><span data-stu-id="20839-127">Prevent Desktop Shortcut creation upon install default</span></span>|
|[<span data-ttu-id="20839-128">CreateDesktopShortcut</span><span class="sxs-lookup"><span data-stu-id="20839-128">CreateDesktopShortcut</span></span>](#createdesktopshortcut)|<span data-ttu-id="20839-129">Verhindern der Erstellung von Desktopverknüpfungen bei der Installation (pro Kanal)</span><span class="sxs-lookup"><span data-stu-id="20839-129">Prevent Desktop Shortcut creation upon install (per channel)</span></span>|
|[<span data-ttu-id="20839-130">TargetVersionPrefix</span><span class="sxs-lookup"><span data-stu-id="20839-130">TargetVersionPrefix</span></span>](#targetversionprefix)|<span data-ttu-id="20839-131">Außerkraftsetzung der Zielversion (pro Kanal)</span><span class="sxs-lookup"><span data-stu-id="20839-131">Target version override (per channel)</span></span>|

### [<span data-ttu-id="20839-132">Voreinstellungen</span><span class="sxs-lookup"><span data-stu-id="20839-132">Preferences</span></span>](#preferences-policies)
|<span data-ttu-id="20839-133">Richtlinienname</span><span class="sxs-lookup"><span data-stu-id="20839-133">Policy Name</span></span>|<span data-ttu-id="20839-134">Beschriftung</span><span class="sxs-lookup"><span data-stu-id="20839-134">Caption</span></span>|
|-|-|
|[<span data-ttu-id="20839-135">AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="20839-135">AutoUpdateCheckPeriodMinutes</span></span>](#autoupdatecheckperiodminutes)|<span data-ttu-id="20839-136">Überschreibung des Überprüfungszeitraums für automatische Updates</span><span class="sxs-lookup"><span data-stu-id="20839-136">Auto-update check period override</span></span>|
|[<span data-ttu-id="20839-137">UpdatesSuppressed</span><span class="sxs-lookup"><span data-stu-id="20839-137">UpdatesSuppressed</span></span>](#updatessuppressed)|<span data-ttu-id="20839-138">Zeitraum in jedem Tag zum Unterdrücken der automatischen Überprüfung auf Updates</span><span class="sxs-lookup"><span data-stu-id="20839-138">Time period in each day to suppress auto-update check</span></span>|

### [<span data-ttu-id="20839-139">Proxyserver</span><span class="sxs-lookup"><span data-stu-id="20839-139">Proxy Server</span></span>](#proxy-server-policies)
|<span data-ttu-id="20839-140">Richtlinienname</span><span class="sxs-lookup"><span data-stu-id="20839-140">Policy Name</span></span>|<span data-ttu-id="20839-141">Untertitel für Hörgeschädigte</span><span class="sxs-lookup"><span data-stu-id="20839-141">Caption</span></span>|
|-|-|
|[<span data-ttu-id="20839-142">ProxyMode</span><span class="sxs-lookup"><span data-stu-id="20839-142">ProxyMode</span></span>](#proxymode)|<span data-ttu-id="20839-143">Möglichkeit zur Angabe der Proxyservereinstellungen wählen</span><span class="sxs-lookup"><span data-stu-id="20839-143">Choose how to specify proxy server settings</span></span>|
|[<span data-ttu-id="20839-144">ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="20839-144">ProxyPacUrl</span></span>](#proxypacurl)|<span data-ttu-id="20839-145">URL zu einer PAC-Proxydatei</span><span class="sxs-lookup"><span data-stu-id="20839-145">URL to a proxy .pac file</span></span>|
|[<span data-ttu-id="20839-146">ProxyServer</span><span class="sxs-lookup"><span data-stu-id="20839-146">ProxyServer</span></span>](#proxyserver)|<span data-ttu-id="20839-147">Adresse oder URL des Proxyservers</span><span class="sxs-lookup"><span data-stu-id="20839-147">Address or URL of proxy server</span></span>|

                 
      
  
             
            
                  

## <span data-ttu-id="20839-148">Anwendungsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="20839-148">Applications policies</span></span>

[<span data-ttu-id="20839-149">Zurück zum Anfang</span><span class="sxs-lookup"><span data-stu-id="20839-149">Back to top</span></span>](#microsoft-edge---update-policies)
### <span data-ttu-id="20839-150">InstallDefault</span><span class="sxs-lookup"><span data-stu-id="20839-150">InstallDefault</span></span>
#### <span data-ttu-id="20839-151">Standardinstallation zulassen</span><span class="sxs-lookup"><span data-stu-id="20839-151">Allow installation default</span></span>
><span data-ttu-id="20839-152">Microsoft Edge Update 1.2.145.5 und höher</span><span class="sxs-lookup"><span data-stu-id="20839-152">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="20839-153">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="20839-153">Description</span></span>
<span data-ttu-id="20839-154">Sie können das Standardverhalten aller Kanäle festlegen, damit Microsoft Edge-Updates bei Verwendung von Microsoft Edge Update zugelassen oder blockiert werden.</span><span class="sxs-lookup"><span data-stu-id="20839-154">You can specify the default behavior of all channels to allow or block Microsoft Edge updates when Microsoft Edge Update is used.</span></span>

<span data-ttu-id="20839-155">Sie können diese Richtlinie für einzelne Kanäle außer Kraft setzen, indem Sie die Richtlinie '[Installation zulassen](#install)' für bestimmte Kanäle aktivieren.</span><span class="sxs-lookup"><span data-stu-id="20839-155">You can override this policy for individual channels by enabling the '[Allow installation](#install)' policy for specific channels.</span></span>

<span data-ttu-id="20839-156">Wenn Sie diese Richtlinie deaktivieren, wird die Installation von Microsoft Edge über Microsoft Edge Update blockiert.</span><span class="sxs-lookup"><span data-stu-id="20839-156">If you disable this policy, the installation of Microsoft Edge through Microsoft Edge Update is blocked.</span></span> <span data-ttu-id="20839-157">Dies wirkt sich nur auf die Installation von Microsoft Edge-Software aus und nur dann, wenn Benutzer Microsoft Edge Update ausführen und die Richtlinie '[Installation zulassen](#install)' nicht konfiguriert haben.</span><span class="sxs-lookup"><span data-stu-id="20839-157">This only affects the installation of Microsoft Edge software only when users are running Microsoft Edge Update and when they haven't configured the '[Allow installation](#install)' policy.</span></span>

<span data-ttu-id="20839-158">Diese Richtlinie verhindert nicht, dass Microsoft Edge Update ausgeführt wird, oder dass Benutzer die Microsoft Edge-Software auf andere Weise installieren.</span><span class="sxs-lookup"><span data-stu-id="20839-158">This policy doesn't prevent Microsoft Edge Update from running or prevent users from installing Microsoft Edge software using other methods.</span></span>
#### <span data-ttu-id="20839-159">Windows-Informationen und -Einstellungen</span><span class="sxs-lookup"><span data-stu-id="20839-159">Windows information and settings</span></span>
##### <span data-ttu-id="20839-160">Informationen zur Gruppenrichtlinie (ADMX)</span><span class="sxs-lookup"><span data-stu-id="20839-160">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="20839-161">Eindeutiger Name der GP: InstallDefault</span><span class="sxs-lookup"><span data-stu-id="20839-161">GP unique name: InstallDefault</span></span>
- <span data-ttu-id="20839-162">GP-Name: Standardinstallation zulassen</span><span class="sxs-lookup"><span data-stu-id="20839-162">GP name: Allow installation default</span></span>
- <span data-ttu-id="20839-163">GP-Pfad: Administrative Vorlagen/Microsoft Edge Update/Anwendungen</span><span class="sxs-lookup"><span data-stu-id="20839-163">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="20839-164">Name der GP-ADMX-Datei: edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="20839-164">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="20839-165">Windows-Registrierungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="20839-165">Windows Registry Settings</span></span>
- <span data-ttu-id="20839-166">Pfad: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="20839-166">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="20839-167">Name des Wertes: InstallDefault</span><span class="sxs-lookup"><span data-stu-id="20839-167">Value Name: InstallDefault</span></span>
- <span data-ttu-id="20839-168">Werttyp: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="20839-168">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="20839-169">Beispielwert:</span><span class="sxs-lookup"><span data-stu-id="20839-169">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="20839-170">Zurück zum Anfang</span><span class="sxs-lookup"><span data-stu-id="20839-170">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="20839-171">UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="20839-171">UpdateDefault</span></span>
#### <span data-ttu-id="20839-172">Die Updaterichtlinie überschreibt die Standardrichtlinie</span><span class="sxs-lookup"><span data-stu-id="20839-172">Update policy override default</span></span>
><span data-ttu-id="20839-173">Microsoft Edge Update 1.2.145.5 und höher</span><span class="sxs-lookup"><span data-stu-id="20839-173">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="20839-174">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="20839-174">Description</span></span>
<span data-ttu-id="20839-175">Hier können Sie das Standardverhalten für alle Kanäle angeben, wie Microsoft Edge Update verfügbare Updates für Microsoft Edge verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="20839-175">Lets you specify the default behavior for all channels concerning the way Microsoft Edge Update handles available updates for Microsoft Edge.</span></span> <span data-ttu-id="20839-176">Kann für einzelne Kanäle durch Angabe der Richtlinie '[Außerkraftsetzung von Updaterichtlinien](#update)' für diese bestimmten Kanäle außer Kraft gesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="20839-176">Can be overridden for individual channels by specifying the '[Update policy override](#update)' policy for those specific channels.</span></span>

  <span data-ttu-id="20839-177">Wenn Sie diese Richtlinie aktivieren, verarbeitet Microsoft Edge Update Microsoft Edge-Updates entsprechend der Konfiguration der folgenden Optionen:</span><span class="sxs-lookup"><span data-stu-id="20839-177">If you enable this policy, Microsoft Edge Update handles Microsoft Edge updates according to how you configure the following options:</span></span>
   - <span data-ttu-id="20839-178">Updates immer zulassen: Updates werden immer dann angewendet, wenn sie gefunden werden, entweder durch die regelmäßige Updateprüfung oder durch eine manuelle Updateprüfung.</span><span class="sxs-lookup"><span data-stu-id="20839-178">Always allow updates: Updates are always applied when found, either by periodic update check or by a manual update check.</span></span>
   - <span data-ttu-id="20839-179">Nur automatische unbeaufsichtigte Updates: Updates werden nur angewendet, wenn sie von der regelmäßigen Updateprüfung gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="20839-179">Automatic silent updates only: Updates are applied only when they're found by the periodic update check.</span></span>
   - <span data-ttu-id="20839-180">Nur manuelle Updates: Updates werden nur angewendet, wenn der Benutzer eine manuelle Updateprüfung ausführt.</span><span class="sxs-lookup"><span data-stu-id="20839-180">Manual updates only: Updates are applied only when the user runs a manual update check.</span></span>
   - <span data-ttu-id="20839-181">Updates deaktiviert: Updates werden nie angewendet.</span><span class="sxs-lookup"><span data-stu-id="20839-181">Updates disabled: Updates are never applied.</span></span>

  <span data-ttu-id="20839-182">Wenn Sie „manuelle Updates” auswählen, stellen Sie sicher, dass Sie regelmäßig nach Updates suchen, indem Sie den manuellen Updatemechanismus der App verwenden, sofern verfügbar.</span><span class="sxs-lookup"><span data-stu-id="20839-182">If you select manual updates, make sure you periodically check for updates by using the app's manual update mechanism, if available.</span></span> <span data-ttu-id="20839-183">Wenn Sie Updates deaktivieren, suchen Sie regelmäßig nach Updates und verteilen Sie diese an die Benutzer.</span><span class="sxs-lookup"><span data-stu-id="20839-183">If you disable updates, periodically check for updates, and distribute them to users.</span></span>

  <span data-ttu-id="20839-184">Wenn Sie diese Richtlinie nicht aktivieren und konfigurieren, behandelt Microsoft Edge Update die verfügbaren Updates gemäß der Richtlinie '[Außerkraftsetzung von Updaterichtlinien](#update)'.</span><span class="sxs-lookup"><span data-stu-id="20839-184">If you don't enable and configure this policy, Microsoft Edge Update handles available updates as specified by the '[Update policy override](#update)' policy.</span></span>
#### <span data-ttu-id="20839-185">Windows-Informationen und -Einstellungen</span><span class="sxs-lookup"><span data-stu-id="20839-185">Windows information and settings</span></span>
##### <span data-ttu-id="20839-186">Informationen zur Gruppenrichtlinie (ADMX)</span><span class="sxs-lookup"><span data-stu-id="20839-186">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="20839-187">Eindeutiger Name der GP: UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="20839-187">GP unique name: UpdateDefault</span></span>
- <span data-ttu-id="20839-188">GP-Name: Die Updaterichtlinie überschreibt die Standardrichtlinie</span><span class="sxs-lookup"><span data-stu-id="20839-188">GP name: Update policy override default</span></span>
- <span data-ttu-id="20839-189">GP-Pfad: Administrative Vorlagen/Microsoft Edge Update/Anwendungen</span><span class="sxs-lookup"><span data-stu-id="20839-189">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="20839-190">Name der GP-ADMX-Datei: edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="20839-190">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="20839-191">Windows-Registrierungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="20839-191">Windows Registry Settings</span></span>
- <span data-ttu-id="20839-192">Pfad: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="20839-192">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="20839-193">Name des Wertes: UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="20839-193">Value Name: UpdateDefault</span></span>
- <span data-ttu-id="20839-194">Werttyp: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="20839-194">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="20839-195">Beispielwert:</span><span class="sxs-lookup"><span data-stu-id="20839-195">Example value:</span></span>
```
0x00000003
```
[<span data-ttu-id="20839-196">Zurück zum Anfang</span><span class="sxs-lookup"><span data-stu-id="20839-196">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="20839-197">Installieren</span><span class="sxs-lookup"><span data-stu-id="20839-197">Install</span></span>
#### <span data-ttu-id="20839-198">Installation zulassen</span><span class="sxs-lookup"><span data-stu-id="20839-198">Allow installation</span></span>
><span data-ttu-id="20839-199">Microsoft Edge Update 1.2.145.5 und höher</span><span class="sxs-lookup"><span data-stu-id="20839-199">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="20839-200">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="20839-200">Description</span></span>
<span data-ttu-id="20839-201">Gibt an, ob ein Microsoft Edge-Kanal mithilfe von Microsoft Edge Update installiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="20839-201">Specifies whether a Microsoft Edge channel can be installed using Microsoft Edge Update.</span></span>

  <span data-ttu-id="20839-202">Wenn Sie diese Richtlinie für einen Kanal aktivieren, können Benutzer diesen Kanal von Microsoft Edge über Microsoft Edge Update installieren.</span><span class="sxs-lookup"><span data-stu-id="20839-202">If you enable this policy for a channel, users can install that channel of Microsoft Edge through Microsoft Edge Update.</span></span>

  <span data-ttu-id="20839-203">Wenn Sie diese Richtlinie für einen Kanal deaktivieren, können Sie diesen Kanal von Microsoft Edge nicht über Microsoft Edge Update installieren.</span><span class="sxs-lookup"><span data-stu-id="20839-203">If you disable this policy for a channel, users cannot install that channel of Microsoft Edge through Microsoft Edge Update.</span></span>

  <span data-ttu-id="20839-204">Wenn Sie diese Richtlinie nicht für einen Kanal konfigurieren, bestimmt die Richtlinienkonfiguration '[Standardinstallation zulassen](#installdefault)', ob Benutzer diesen Kanal von Microsoft Edge über Microsoft Edge Update installieren können.</span><span class="sxs-lookup"><span data-stu-id="20839-204">If you don't configure this policy for a channel, the '[Allow installation default](#installdefault)' policy configuration determines whether users can install that channel of Microsoft Edge through Microsoft Edge Update.</span></span>
#### <span data-ttu-id="20839-205">Windows-Informationen und -Einstellungen</span><span class="sxs-lookup"><span data-stu-id="20839-205">Windows information and settings</span></span>
##### <span data-ttu-id="20839-206">Informationen zur Gruppenrichtlinie (ADMX)</span><span class="sxs-lookup"><span data-stu-id="20839-206">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="20839-207">Eindeutiger Name der GP: Install</span><span class="sxs-lookup"><span data-stu-id="20839-207">GP unique name: Install</span></span>
- <span data-ttu-id="20839-208">GP-Name: Installation zulassen</span><span class="sxs-lookup"><span data-stu-id="20839-208">GP name: Allow installation</span></span>
- <span data-ttu-id="20839-209">GP-Pfad:</span><span class="sxs-lookup"><span data-stu-id="20839-209">GP path:</span></span> 
  - <span data-ttu-id="20839-210">Administrative Vorlagen/Microsoft Edge Update/Anwendungen/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="20839-210">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="20839-211">Administrative Vorlagen/Microsoft Edge Update/Anwendungen/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="20839-211">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="20839-212">Administrative Vorlagen/Microsoft Edge Update/Anwendungen/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="20839-212">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="20839-213">Administrative Vorlagen/Microsoft Edge Update/Anwendungen/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="20839-213">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="20839-214">Name der GP-ADMX-Datei: edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="20839-214">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="20839-215">Windows-Registrierungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="20839-215">Windows Registry Settings</span></span>
- <span data-ttu-id="20839-216">Pfad: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="20839-216">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="20839-217">Name des Wertes:</span><span class="sxs-lookup"><span data-stu-id="20839-217">Value Name:</span></span> 
  - <span data-ttu-id="20839-218">(Stable): Install{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="20839-218">(Stable): Install{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="20839-219">(Beta): Install{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="20839-219">(Beta): Install{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="20839-220">(Canary): Install{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="20839-220">(Canary): Install{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="20839-221">(Dev): Install{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="20839-221">(Dev): Install{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="20839-222">Werttyp: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="20839-222">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="20839-223">Beispielwert:</span><span class="sxs-lookup"><span data-stu-id="20839-223">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="20839-224">Zurück zum Anfang</span><span class="sxs-lookup"><span data-stu-id="20839-224">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="20839-225">Update</span><span class="sxs-lookup"><span data-stu-id="20839-225">Update</span></span>
#### <span data-ttu-id="20839-226">Außerkraftsetzung von Updaterichtlinien</span><span class="sxs-lookup"><span data-stu-id="20839-226">Update policy override</span></span>
><span data-ttu-id="20839-227">Microsoft Edge Update 1.2.145.5 und höher</span><span class="sxs-lookup"><span data-stu-id="20839-227">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="20839-228">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="20839-228">Description</span></span>
<span data-ttu-id="20839-229">Gibt an, wie Microsoft Edge Update verfügbare Updates von Microsoft Edge behandelt.</span><span class="sxs-lookup"><span data-stu-id="20839-229">Specifies how Microsoft Edge Update handles available updates from Microsoft Edge.</span></span>

  <span data-ttu-id="20839-230">Wenn Sie diese Richtlinie aktivieren, verarbeitet Microsoft Edge Update Microsoft Edge-Updates entsprechend der Konfiguration der folgenden Optionen:</span><span class="sxs-lookup"><span data-stu-id="20839-230">If you enable this policy, Microsoft Edge Update handles Microsoft Edge updates according to how you configure the following options:</span></span>
   - <span data-ttu-id="20839-231">Updates immer zulassen: Updates werden immer dann angewendet, wenn sie gefunden werden, entweder durch die regelmäßige Updateprüfung oder durch eine manuelle Updateprüfung.</span><span class="sxs-lookup"><span data-stu-id="20839-231">Always allow updates: Updates are always applied when found, either by periodic update check or by a manual update check.</span></span>
   - <span data-ttu-id="20839-232">Nur automatische unbeaufsichtigte Updates: Updates werden nur angewendet, wenn sie von der regelmäßigen Updateprüfung gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="20839-232">Automatic silent updates only: Updates are applied only when they're found by the periodic update check.</span></span>
   - <span data-ttu-id="20839-233">Nur manuelle Updates: Updates werden nur angewendet, wenn der Benutzer eine manuelle Updateprüfung ausführt.</span><span class="sxs-lookup"><span data-stu-id="20839-233">Manual updates only: Updates are applied only when the user runs a manual update check.</span></span> <span data-ttu-id="20839-234">(Nicht alle Apps bieten eine Schnittstelle für diese Option.)</span><span class="sxs-lookup"><span data-stu-id="20839-234">(Not all apps provide an interface for this option.)</span></span>
   - <span data-ttu-id="20839-235">Updates deaktiviert: Updates werden nie angewendet.</span><span class="sxs-lookup"><span data-stu-id="20839-235">Updates disabled: Updates are never applied.</span></span>

  <span data-ttu-id="20839-236">Wenn Sie „manuelle Updates” auswählen, stellen Sie sicher, dass Sie regelmäßig nach Updates suchen, indem Sie den manuellen Updatemechanismus der App verwenden, sofern verfügbar.</span><span class="sxs-lookup"><span data-stu-id="20839-236">If you select manual updates, make sure you periodically check for updates by using the app's manual update mechanism, if available.</span></span> <span data-ttu-id="20839-237">Wenn Sie Updates deaktivieren, suchen Sie regelmäßig nach Updates und verteilen Sie diese an die Benutzer.</span><span class="sxs-lookup"><span data-stu-id="20839-237">If you disable updates, periodically check for updates, and distribute them to users.</span></span>

  <span data-ttu-id="20839-238">Wenn Sie diese Richtlinie nicht aktivieren und konfigurieren, behandelt Microsoft Edge Update die verfügbaren Updates gemäß der Richtlinie '[Die Updaterichtlinie überschreibt die Standardrichtlinie](#updatedefault)'.</span><span class="sxs-lookup"><span data-stu-id="20839-238">If you don't enable and configure this policy, Microsoft Edge Update handles available updates as specified by the '[Update policy override default](#updatedefault)' policy.</span></span>
#### <span data-ttu-id="20839-239">Windows-Informationen und -Einstellungen</span><span class="sxs-lookup"><span data-stu-id="20839-239">Windows information and settings</span></span>
##### <span data-ttu-id="20839-240">Informationen zur Gruppenrichtlinie (ADMX)</span><span class="sxs-lookup"><span data-stu-id="20839-240">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="20839-241">Eindeutiger Name der GP: Update</span><span class="sxs-lookup"><span data-stu-id="20839-241">GP unique name: Update</span></span>
- <span data-ttu-id="20839-242">GP-Name: Außerkraftsetzung von Updaterichtlinien</span><span class="sxs-lookup"><span data-stu-id="20839-242">GP name: Update policy override</span></span>
- <span data-ttu-id="20839-243">GP-Pfad:</span><span class="sxs-lookup"><span data-stu-id="20839-243">GP path:</span></span> 
  - <span data-ttu-id="20839-244">Administrative Vorlagen/Microsoft Edge Update/Anwendungen/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="20839-244">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="20839-245">Administrative Vorlagen/Microsoft Edge Update/Anwendungen/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="20839-245">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="20839-246">Administrative Vorlagen/Microsoft Edge Update/Anwendungen/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="20839-246">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="20839-247">Administrative Vorlagen/Microsoft Edge Update/Anwendungen/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="20839-247">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="20839-248">Name der GP-ADMX-Datei: edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="20839-248">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="20839-249">Windows-Registrierungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="20839-249">Windows Registry Settings</span></span>
- <span data-ttu-id="20839-250">Pfad: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="20839-250">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="20839-251">Name des Wertes:</span><span class="sxs-lookup"><span data-stu-id="20839-251">Value Name:</span></span> 
  - <span data-ttu-id="20839-252">(Stable): Update{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="20839-252">(Stable): Update{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="20839-253">(Beta): Update{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="20839-253">(Beta): Update{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="20839-254">(Canary): Update{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="20839-254">(Canary): Update{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="20839-255">(Dev): Update{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="20839-255">(Dev): Update{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="20839-256">Werttyp: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="20839-256">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="20839-257">Beispielwert:</span><span class="sxs-lookup"><span data-stu-id="20839-257">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="20839-258">Zurück zum Anfang</span><span class="sxs-lookup"><span data-stu-id="20839-258">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="20839-259">Allowsxs</span><span class="sxs-lookup"><span data-stu-id="20839-259">Allowsxs</span></span>
#### <span data-ttu-id="20839-260">Microsoft Edge Seite-an-Seite-Browserumgebung zulassen</span><span class="sxs-lookup"><span data-stu-id="20839-260">Allow Microsoft Edge Side by Side browser experience</span></span>
><span data-ttu-id="20839-261">Microsoft Edge Update 1.2.145.5 und höher</span><span class="sxs-lookup"><span data-stu-id="20839-261">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="20839-262">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="20839-262">Description</span></span>
<span data-ttu-id="20839-263">Mit dieser Richtlinie können Benutzer Microsoft Edge (Edge-HTML) und Microsoft Edge (Chromium-basiert) nebeneinander ausführen.</span><span class="sxs-lookup"><span data-stu-id="20839-263">This policy lets a user run Microsoft Edge (Edge HTML) and Microsoft Edge (Chromium-based) side-by-side.</span></span>

<span data-ttu-id="20839-264">Wenn diese Richtlinie auf „Nicht konfiguriert” festgelegt ist, ersetzt Microsoft Edge (Chromium-basiert) Microsoft Edge (Edge-HTML) nach dem stabilen Kanal von Microsoft Edge (Chromium-basierten), und die Sicherheitsupdates vom November2019 werden installiert.</span><span class="sxs-lookup"><span data-stu-id="20839-264">If this policy is set to “Not configured”, Microsoft Edge (Chromium-based) will replace Microsoft Edge (Edge HTML) after the Microsoft Edge (Chromium-based) stable channel and the November 2019 security updates are installed.</span></span>  <span data-ttu-id="20839-265">Hierbei handelt es sich um das gleiche Verhalten wie bei der Einstellung „Deaktiviert“.</span><span class="sxs-lookup"><span data-stu-id="20839-265">This is the same behavior as the “Disabled” setting.</span></span>

<span data-ttu-id="20839-266">Die Einstellung „Deaktiviert” blockiert eine Seite-an-Seite-Umgebung, und Microsoft Edge (Chromium-basiert) ersetzt Microsoft Edge (Edge-HTML) nach dem stabilen Kanal von Microsoft Edge (Chromium-basierten). Außerdem werden die Sicherheitsupdates vom November2019 installiert.</span><span class="sxs-lookup"><span data-stu-id="20839-266">The “Disabled” setting blocks a side-by-side experience and Microsoft Edge (Chromium-based) will replace Microsoft Edge (Edge HTML) after the Microsoft Edge (Chromium-based) stable channel and the November 2019 security updates are installed.</span></span>  <span data-ttu-id="20839-267">Hierbei handelt es sich um das gleiche Verhalten wie bei der Einstellung „Nicht konfiguriert“.</span><span class="sxs-lookup"><span data-stu-id="20839-267">This is the same behavior as the “Not Configured” setting.</span></span>

<span data-ttu-id="20839-268">Wenn diese Richtlinie aktiviert ist, können Microsoft Edge (Chromium-basiert) und Microsoft Edge (Edge-HTML) nach der Installation von Microsoft Edge (Chromium-basiert) nebeneinander ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="20839-268">When this policy is “Enabled”, Microsoft Edge (Chromium-based) and Microsoft Edge (Edge HTML) can run side-by-side after Microsoft Edge (Chromium-based) is installed.</span></span>

<span data-ttu-id="20839-269">Damit diese Gruppenrichtlinie wirksam wird, muss sie vor der automatischen Installation von Microsoft Edge (Chromium-basiert) von Windows Update konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="20839-269">For this group policy to take affect, it must be configured before the automatic install of Microsoft Edge (Chromium-based) by Windows Update.</span></span> <span data-ttu-id="20839-270">Hinweis: Ein Benutzer kann das automatische Update von Microsoft Edge (Chromium-basiert) mit dem Microsoft Edge (Chromium-basiert) Blocker Toolkit blockieren.</span><span class="sxs-lookup"><span data-stu-id="20839-270">Note: A user can block the automatic update of Microsoft Edge (Chromium-based) by using the Microsoft Edge (Chromium-based) Blocker Toolkit.</span></span>
#### <span data-ttu-id="20839-271">Windows-Informationen und -Einstellungen</span><span class="sxs-lookup"><span data-stu-id="20839-271">Windows information and settings</span></span>
##### <span data-ttu-id="20839-272">Informationen zur Gruppenrichtlinie (ADMX)</span><span class="sxs-lookup"><span data-stu-id="20839-272">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="20839-273">Eindeutiger Name der GP: Allowsxs</span><span class="sxs-lookup"><span data-stu-id="20839-273">GP unique name: Allowsxs</span></span>
- <span data-ttu-id="20839-274">GP-Name: Microsoft Edge Seite-an-Seite-Browserumgebung zulassen</span><span class="sxs-lookup"><span data-stu-id="20839-274">GP name: Allow Microsoft Edge Side by Side browser experience</span></span>
- <span data-ttu-id="20839-275">GP-Pfad: Administrative Vorlagen/Microsoft Edge Update/Anwendungen</span><span class="sxs-lookup"><span data-stu-id="20839-275">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="20839-276">Name der GP-ADMX-Datei: edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="20839-276">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="20839-277">Windows-Registrierungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="20839-277">Windows Registry Settings</span></span>
- <span data-ttu-id="20839-278">Pfad: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="20839-278">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="20839-279">Name des Wertes: Allowsxs</span><span class="sxs-lookup"><span data-stu-id="20839-279">Value Name: Allowsxs</span></span>
- <span data-ttu-id="20839-280">Werttyp: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="20839-280">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="20839-281">Beispielwert:</span><span class="sxs-lookup"><span data-stu-id="20839-281">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="20839-282">Zurück zum Anfang</span><span class="sxs-lookup"><span data-stu-id="20839-282">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="20839-283">CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="20839-283">CreateDesktopShortcutDefault</span></span>
#### <span data-ttu-id="20839-284">Standardeinstellung für das Verhindern der Erstellung von Desktopverknüpfungen bei der Installation</span><span class="sxs-lookup"><span data-stu-id="20839-284">Prevent Desktop Shortcut creation upon install default</span></span>
><span data-ttu-id="20839-285">Microsoft Edge Update 1.3.128.0 und höher</span><span class="sxs-lookup"><span data-stu-id="20839-285">Microsoft Edge Update 1.3.128.0 and later</span></span>

#### <span data-ttu-id="20839-286">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="20839-286">Description</span></span>
<span data-ttu-id="20839-287">Ermöglicht es Ihnen, das Standardverhalten aller Kanäle für die Erstellung einer Desktopverknüpfung festzulegen, wenn Microsoft Edge installiert wird.</span><span class="sxs-lookup"><span data-stu-id="20839-287">Lets you specify the default behavior for all channels for creating a desktop shortcut when Microsoft Edge is installed.</span></span>

  <span data-ttu-id="20839-288">Wenn Sie diese Richtlinie aktivieren, wird beim Installieren von Microsoft Edge eine Desktopverknüpfung erstellt.</span><span class="sxs-lookup"><span data-stu-id="20839-288">If you enable this policy a desktop shortcut is created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="20839-289">Wenn Sie diese Richtlinie deaktivieren, wird beim Installieren von Microsoft Edge keine Desktopverknüpfung erstellt.</span><span class="sxs-lookup"><span data-stu-id="20839-289">If you disable this policy, no desktop shortcut will be created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="20839-290">Wenn Sie diese Richtlinie nicht konfigurieren, wird während der Installation eine Desktopverknüpfung zu Microsoft Edge erstellt.</span><span class="sxs-lookup"><span data-stu-id="20839-290">If you don’t configure this policy a desktop shortcut to Microsoft Edge will be created during installation.</span></span>
<span data-ttu-id="20839-291">Wenn Microsoft Edge bereits installiert ist, hat diese Richtlinie keine Auswirkung.</span><span class="sxs-lookup"><span data-stu-id="20839-291">If Microsoft Edge is already installed, this policy will have no effect.</span></span>
#### <span data-ttu-id="20839-292">Windows-Informationen und -Einstellungen</span><span class="sxs-lookup"><span data-stu-id="20839-292">Windows information and settings</span></span>
##### <span data-ttu-id="20839-293">Informationen zur Gruppenrichtlinie (ADMX)</span><span class="sxs-lookup"><span data-stu-id="20839-293">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="20839-294">Eindeutiger Name der GP: CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="20839-294">GP unique name: CreateDesktopShortcutDefault</span></span>
- <span data-ttu-id="20839-295">GP-Name: Standardeinstellung "Erstellung von Desktopverknüpfungen bei der Installation verhindern"</span><span class="sxs-lookup"><span data-stu-id="20839-295">GP name: Prevent Desktop Shortcut creation upon install default</span></span>
- <span data-ttu-id="20839-296">GP-Pfad: Administrative Vorlagen/Microsoft Edge Update/Anwendungen</span><span class="sxs-lookup"><span data-stu-id="20839-296">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="20839-297">Name der GP-ADMX-Datei: edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="20839-297">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="20839-298">Windows-Registrierungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="20839-298">Windows Registry Settings</span></span>
- <span data-ttu-id="20839-299">Pfad: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="20839-299">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="20839-300">Wertname: CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="20839-300">Value Name: CreateDesktopShortcutDefault</span></span>
- <span data-ttu-id="20839-301">Werttyp: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="20839-301">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="20839-302">Beispielwert:</span><span class="sxs-lookup"><span data-stu-id="20839-302">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="20839-303">Zurück zum Anfang</span><span class="sxs-lookup"><span data-stu-id="20839-303">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="20839-304">CreateDesktopShortcut</span><span class="sxs-lookup"><span data-stu-id="20839-304">CreateDesktopShortcut</span></span>
#### <span data-ttu-id="20839-305">GP-Name: Erstellen von Desktopverknüpfungen bei Standardinstallation</span><span class="sxs-lookup"><span data-stu-id="20839-305">Prevent Desktop Shortcut creation upon install</span></span>
><span data-ttu-id="20839-306">Microsoft Edge Update 1.3.128.0 und höher</span><span class="sxs-lookup"><span data-stu-id="20839-306">Microsoft Edge Update 1.3.128.0 and later</span></span>

#### <span data-ttu-id="20839-307">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="20839-307">Description</span></span>
<span data-ttu-id="20839-308">Wenn Sie diese Richtlinie aktivieren, wird beim Installieren von Microsoft Edge eine Desktopverknüpfung erstellt.</span><span class="sxs-lookup"><span data-stu-id="20839-308">If you enable this policy a desktop shortcut is created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="20839-309">Wenn Sie diese Richtlinie deaktivieren, wird beim Installieren von Microsoft Edge keine Desktopverknüpfung erstellt.</span><span class="sxs-lookup"><span data-stu-id="20839-309">If you disable this policy, no desktop shortcut will be created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="20839-310">Wenn Sie diese Richtlinie nicht konfigurieren, wird während der Installation eine Desktopverknüpfung zu Microsoft Edge erstellt.</span><span class="sxs-lookup"><span data-stu-id="20839-310">If you don’t configure this policy a desktop shortcut to Microsoft Edge will be created during installation.</span></span>
<span data-ttu-id="20839-311">Wenn Microsoft Edge bereits installiert ist, hat diese Richtlinie keine Auswirkung.</span><span class="sxs-lookup"><span data-stu-id="20839-311">If Microsoft Edge is already installed, this policy will have no effect.</span></span>

  <span data-ttu-id="20839-312">Wenn Sie diese Richtlinie für einen Kanal nicht konfigurieren, bestimmt die Richtlinienkonfiguration "[Standardeinstellung für das Verhindern der Erstellung von Desktopverknüpfungen bei der Installation](#createdesktopshortcutdefault)", ob bei Installation von Microsoft Edge eine Verknüpfung erstellt wird oder nicht.</span><span class="sxs-lookup"><span data-stu-id="20839-312">If you don't configure this policy for a channel, the '[Prevent Desktop Shortcut creation upon install default](#createdesktopshortcutdefault)' policy configuration determines shortcut creation when Microsoft Edge is installed.</span></span>
#### <span data-ttu-id="20839-313">Windows-Informationen und -Einstellungen</span><span class="sxs-lookup"><span data-stu-id="20839-313">Windows information and settings</span></span>
##### <span data-ttu-id="20839-314">Informationen zur Gruppenrichtlinie (ADMX)</span><span class="sxs-lookup"><span data-stu-id="20839-314">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="20839-315">Eindeutiger Name der GP: CreateDesktopShortcut</span><span class="sxs-lookup"><span data-stu-id="20839-315">GP unique name: CreateDesktopShortcut</span></span>
- <span data-ttu-id="20839-316">GP-Name: Erstellen von Desktopverknüpfungen bei Installation verhindern</span><span class="sxs-lookup"><span data-stu-id="20839-316">GP name: Prevent Desktop Shortcut creation upon install</span></span>
- <span data-ttu-id="20839-317">GP-Pfad:</span><span class="sxs-lookup"><span data-stu-id="20839-317">GP path:</span></span> 
  - <span data-ttu-id="20839-318">Administrative Vorlagen/Microsoft Edge Update/Anwendungen/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="20839-318">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="20839-319">Administrative Vorlagen/Microsoft Edge Update/Anwendungen/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="20839-319">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="20839-320">Administrative Vorlagen/Microsoft Edge Update/Anwendungen/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="20839-320">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="20839-321">Administrative Vorlagen/Microsoft Edge Update/Anwendungen/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="20839-321">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="20839-322">Name der GP-ADMX-Datei: edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="20839-322">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="20839-323">Windows-Registrierungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="20839-323">Windows Registry Settings</span></span>
- <span data-ttu-id="20839-324">Pfad: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="20839-324">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="20839-325">Name des Wertes:</span><span class="sxs-lookup"><span data-stu-id="20839-325">Value Name:</span></span> 
  - <span data-ttu-id="20839-326">(Stable): CreateDesktopShortcut{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="20839-326">(Stable): CreateDesktopShortcut{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="20839-327">(Beta): CreateDesktopShortcut{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="20839-327">(Beta): CreateDesktopShortcut{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="20839-328">(Canary): CreateDesktopShortcut{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="20839-328">(Canary): CreateDesktopShortcut{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="20839-329">(Dev): CreateDesktopShortcut{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="20839-329">(Dev): CreateDesktopShortcut{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="20839-330">Werttyp: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="20839-330">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="20839-331">Beispielwert:</span><span class="sxs-lookup"><span data-stu-id="20839-331">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="20839-332">Zurück zum Anfang</span><span class="sxs-lookup"><span data-stu-id="20839-332">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="20839-333">TargetVersionPrefix</span><span class="sxs-lookup"><span data-stu-id="20839-333">TargetVersionPrefix</span></span>
#### <span data-ttu-id="20839-334">Zielversion außer Kraft setzen</span><span class="sxs-lookup"><span data-stu-id="20839-334">Target version override</span></span>
><span data-ttu-id="20839-335">Microsoft Edge Update 1.3.119.43 und höher</span><span class="sxs-lookup"><span data-stu-id="20839-335">Microsoft Edge Update 1.3.119.43 and later</span></span>

#### <span data-ttu-id="20839-336">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="20839-336">Description</span></span>
<span data-ttu-id="20839-337">Wenn diese Richtlinie und die automatische Aktualisierung aktiviert sind, wird Microsoft Edge auf die durch diesen Richtlinienwert angegebene Version aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="20839-337">When this policy is enabled, and auto-update is enabled, Microsoft Edge will be updated to the version specified by this policy value.</span></span>

<span data-ttu-id="20839-338">Der Richtlinienwert muss eine bestimmte Microsoft Edge-Version sein, z. B. 83.0.499.12.</span><span class="sxs-lookup"><span data-stu-id="20839-338">The policy value must be a specific Microsoft Edge version, e.g. 83.0.499.12.</span></span>

<span data-ttu-id="20839-339">Wenn ein Gerät über eine neuere Version von Microsoft Edge als der angegebene Wert verfügt, bleibt Microsoft Edge bei der neueren Version und wird nicht auf die angegebene Version herabgestuft.</span><span class="sxs-lookup"><span data-stu-id="20839-339">If a device has newer version of Microsoft Edge than the value specified, Microsoft Edge will remain on the newer version and not downgrade to the specified version.</span></span>

<span data-ttu-id="20839-340">Wenn die angegebene Version nicht vorhanden oder nicht ordnungsgemäß formatiert ist, bleibt Microsoft Edge bei der aktuellen Version und wird nicht automatisch auf zukünftige Versionen aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="20839-340">If the specified version does not exist, or is improperly formatted, then Microsoft Edge will remain on its current version and not update to future versions automatically.</span></span>
#### <span data-ttu-id="20839-341">Windows-Informationen und -Einstellungen</span><span class="sxs-lookup"><span data-stu-id="20839-341">Windows information and settings</span></span>
##### <span data-ttu-id="20839-342">Informationen zur Gruppenrichtlinie (ADMX)</span><span class="sxs-lookup"><span data-stu-id="20839-342">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="20839-343">Eindeutiger Name der GP: TargetVersionPrefix</span><span class="sxs-lookup"><span data-stu-id="20839-343">GP unique name: TargetVersionPrefix</span></span>
- <span data-ttu-id="20839-344">GP-Name: Zielversion außer Kraft setzen</span><span class="sxs-lookup"><span data-stu-id="20839-344">GP name: Target version override</span></span>
- <span data-ttu-id="20839-345">GP-Pfad:</span><span class="sxs-lookup"><span data-stu-id="20839-345">GP path:</span></span> 
  - <span data-ttu-id="20839-346">Administrative Vorlagen/Microsoft Edge Update/Anwendungen/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="20839-346">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="20839-347">Administrative Vorlagen/Microsoft Edge Update/Anwendungen/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="20839-347">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="20839-348">Administrative Vorlagen/Microsoft Edge Update/Anwendungen/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="20839-348">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="20839-349">Administrative Vorlagen/Microsoft Edge Update/Anwendungen/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="20839-349">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="20839-350">Name der GP-ADMX-Datei: edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="20839-350">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="20839-351">Windows-Registrierungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="20839-351">Windows Registry Settings</span></span>
- <span data-ttu-id="20839-352">Pfad: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="20839-352">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="20839-353">Name des Wertes:</span><span class="sxs-lookup"><span data-stu-id="20839-353">Value Name:</span></span> 
  - <span data-ttu-id="20839-354">(Stable): TargetVersionPrefix{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="20839-354">(Stable): TargetVersionPrefix{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="20839-355">(Beta): TargetVersionPrefix{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="20839-355">(Beta): TargetVersionPrefix{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="20839-356">(Canary): TargetVersionPrefix{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="20839-356">(Canary): TargetVersionPrefix{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="20839-357">(Dev): TargetVersionPrefix{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="20839-357">(Dev): TargetVersionPrefix{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="20839-358">Werttyp: REG_SZ</span><span class="sxs-lookup"><span data-stu-id="20839-358">Value Type: REG_SZ</span></span>
##### <span data-ttu-id="20839-359">Beispielwert:</span><span class="sxs-lookup"><span data-stu-id="20839-359">Example value:</span></span>
```
83.0.499.12
```
[<span data-ttu-id="20839-360">Zurück zum Anfang</span><span class="sxs-lookup"><span data-stu-id="20839-360">Back to top</span></span>](#microsoft-edge---update-policies)


## <span data-ttu-id="20839-361">Einstellungsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="20839-361">Preferences policies</span></span>

[<span data-ttu-id="20839-362">Zurück zum Anfang</span><span class="sxs-lookup"><span data-stu-id="20839-362">Back to top</span></span>](#microsoft-edge---update-policies)
### <span data-ttu-id="20839-363">AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="20839-363">AutoUpdateCheckPeriodMinutes</span></span>
#### <span data-ttu-id="20839-364">Überschreibung des Überprüfungszeitraums für automatische Updates</span><span class="sxs-lookup"><span data-stu-id="20839-364">Auto-update check period override</span></span>
><span data-ttu-id="20839-365">Microsoft Edge Update 1.2.145.5 und höher</span><span class="sxs-lookup"><span data-stu-id="20839-365">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="20839-366">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="20839-366">Description</span></span>
<span data-ttu-id="20839-367">Wenn diese Richtlinie aktiviert ist, können Sie einen Wert für die Mindestanzahl von Minuten zwischen automatischen Updateprüfungen festlegen.</span><span class="sxs-lookup"><span data-stu-id="20839-367">If enabled, this policy lets you set a value for the minimum number of minutes between automatic update checks.</span></span> <span data-ttu-id="20839-368">Andernfalls sucht die automatische Updateprüfung standardmäßig alle 10 Stunden nach Updates.</span><span class="sxs-lookup"><span data-stu-id="20839-368">Otherwise, by default, auto-update checks for updates every 10 hours.</span></span>

  <span data-ttu-id="20839-369">Wenn Sie alle automatischen Updateprüfungen deaktivieren möchten, setzen Sie den Wert auf 0 (nicht empfohlen).</span><span class="sxs-lookup"><span data-stu-id="20839-369">If you want to disable all auto-update checks, set the value to 0 (not recommended).</span></span>
#### <span data-ttu-id="20839-370">Windows-Informationen und -Einstellungen</span><span class="sxs-lookup"><span data-stu-id="20839-370">Windows information and settings</span></span>
##### <span data-ttu-id="20839-371">Informationen zur Gruppenrichtlinie (ADMX)</span><span class="sxs-lookup"><span data-stu-id="20839-371">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="20839-372">Eindeutiger Name der GP: AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="20839-372">GP unique name: AutoUpdateCheckPeriodMinutes</span></span>
- <span data-ttu-id="20839-373">GP-Name: Überschreibung des Überprüfungszeitraums für automatische Updates</span><span class="sxs-lookup"><span data-stu-id="20839-373">GP name: Auto-update check period override</span></span>
- <span data-ttu-id="20839-374">GP-Pfad: Administrative Vorlagen/Microsoft Edge Update/Einstellungen</span><span class="sxs-lookup"><span data-stu-id="20839-374">GP path: Administrative Templates/Microsoft Edge Update/Preferences</span></span>
- <span data-ttu-id="20839-375">Name der GP-ADMX-Datei: edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="20839-375">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="20839-376">Windows-Registrierungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="20839-376">Windows Registry Settings</span></span>
- <span data-ttu-id="20839-377">Pfad: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="20839-377">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="20839-378">Name des Wertes: AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="20839-378">Value Name: AutoUpdateCheckPeriodMinutes</span></span>
- <span data-ttu-id="20839-379">Werttyp: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="20839-379">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="20839-380">Beispielwert:</span><span class="sxs-lookup"><span data-stu-id="20839-380">Example value:</span></span>
```
0x00000578
```
[<span data-ttu-id="20839-381">Zurück zum Anfang</span><span class="sxs-lookup"><span data-stu-id="20839-381">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="20839-382">UpdatesSuppressed</span><span class="sxs-lookup"><span data-stu-id="20839-382">UpdatesSuppressed</span></span>
#### <span data-ttu-id="20839-383">Zeitraum in jedem Tag zum Unterdrücken der automatischen Überprüfung auf Updates</span><span class="sxs-lookup"><span data-stu-id="20839-383">Time period in each day to suppress auto-update check</span></span>
><span data-ttu-id="20839-384">Microsoft Edge Update 1.3.33.5 und höher</span><span class="sxs-lookup"><span data-stu-id="20839-384">Microsoft Edge Update 1.3.33.5 and later</span></span>

#### <span data-ttu-id="20839-385">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="20839-385">Description</span></span>
<span data-ttu-id="20839-386">Wenn Sie diese Richtlinie aktivieren, werden die Updateprüfungen jeden Tag ab Stunde:Minute für einen Zeitraum der Dauer (in Minuten) unterdrückt.</span><span class="sxs-lookup"><span data-stu-id="20839-386">If you enable this policy, update checks are suppressed each day starting at Hour:Minute for a period of Duration (in minutes).</span></span> <span data-ttu-id="20839-387">Die Dauer ist von der Sommerzeit nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="20839-387">Duration isn't affected by daylight saving time.</span></span> <span data-ttu-id="20839-388">Wenn die Startzeit z.B. 22:00 lautet und die Dauer 480Minuten beträgt, werden Updates genau 8 Stunden lang unterdrückt, unabhängig davon, ob die Sommerzeit in diesem Zeitraum beginnt oder endet.</span><span class="sxs-lookup"><span data-stu-id="20839-388">For example, if the start time is 22:00 and the duration is 480 minutes, updates will be suppressed for exactly 8 hours, regardless of whether daylight saving time starts or ends during this period.</span></span>

  <span data-ttu-id="20839-389">Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, werden die Updateprüfungen während eines bestimmten Zeitraums nicht unterdrückt.</span><span class="sxs-lookup"><span data-stu-id="20839-389">If you disable or don't configure this policy, update checks aren't suppressed during any specific period.</span></span>
#### <span data-ttu-id="20839-390">Windows-Informationen und -Einstellungen</span><span class="sxs-lookup"><span data-stu-id="20839-390">Windows information and settings</span></span>
##### <span data-ttu-id="20839-391">Informationen zur Gruppenrichtlinie (ADMX)</span><span class="sxs-lookup"><span data-stu-id="20839-391">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="20839-392">Eindeutiger Name der GP: UpdatesSuppressed</span><span class="sxs-lookup"><span data-stu-id="20839-392">GP unique name: UpdatesSuppressed</span></span>
- <span data-ttu-id="20839-393">GP-Name: Zeitraum in jedem Tag zum Unterdrücken der automatischen Überprüfung auf Updates</span><span class="sxs-lookup"><span data-stu-id="20839-393">GP name: Time period in each day to suppress auto-update check</span></span>
  - <span data-ttu-id="20839-394">Optionen {Stunde, Minute, Dauer}</span><span class="sxs-lookup"><span data-stu-id="20839-394">Options { Hour, Minute, Duration }</span></span>
- <span data-ttu-id="20839-395">GP-Pfad: Administrative Vorlagen/Microsoft Edge Update/Einstellungen</span><span class="sxs-lookup"><span data-stu-id="20839-395">GP path: Administrative Templates/Microsoft Edge Update/Preferences</span></span>
- <span data-ttu-id="20839-396">Name der GP-ADMX-Datei: edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="20839-396">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="20839-397">Windows-Registrierungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="20839-397">Windows Registry Settings</span></span>
- <span data-ttu-id="20839-398">Pfad: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="20839-398">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="20839-399">Name des Wertes:</span><span class="sxs-lookup"><span data-stu-id="20839-399">Value Name:</span></span> 
  - <span data-ttu-id="20839-400">UpdatesSuppressedDurationMin</span><span class="sxs-lookup"><span data-stu-id="20839-400">UpdatesSuppressedDurationMin</span></span>
  - <span data-ttu-id="20839-401">UpdatesSuppressedStartHour</span><span class="sxs-lookup"><span data-stu-id="20839-401">UpdatesSuppressedStartHour</span></span>
  - <span data-ttu-id="20839-402">UpdatesSuppressedStartMin</span><span class="sxs-lookup"><span data-stu-id="20839-402">UpdatesSuppressedStartMin</span></span>
- <span data-ttu-id="20839-403">Werttyp: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="20839-403">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="20839-404">Beispielwert:</span><span class="sxs-lookup"><span data-stu-id="20839-404">Example value:</span></span>
```
duration   : 0x0000003c
start hour : 0x00000001
start min  : 0x00000002
```
[<span data-ttu-id="20839-405">Zurück zum Anfang</span><span class="sxs-lookup"><span data-stu-id="20839-405">Back to top</span></span>](#microsoft-edge---update-policies)


## <span data-ttu-id="20839-406">Proxyserver-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="20839-406">Proxy Server policies</span></span>
  
  

[<span data-ttu-id="20839-407">Zurück zum Anfang</span><span class="sxs-lookup"><span data-stu-id="20839-407">Back to top</span></span>](#microsoft-edge---update-policies)
### <span data-ttu-id="20839-408">ProxyMode</span><span class="sxs-lookup"><span data-stu-id="20839-408">ProxyMode</span></span>
#### <span data-ttu-id="20839-409">Möglichkeit zur Angabe der Proxyservereinstellungen wählen</span><span class="sxs-lookup"><span data-stu-id="20839-409">Choose how to specify proxy server settings</span></span>
><span data-ttu-id="20839-410">Microsoft Edge Update 1.3.21.81 und höher</span><span class="sxs-lookup"><span data-stu-id="20839-410">Microsoft Edge Update 1.3.21.81 and later</span></span>

#### <span data-ttu-id="20839-411">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="20839-411">Description</span></span>
<span data-ttu-id="20839-412">Mit dieser Option können Sie die Proxyserver-Einstellungen angeben, die von Microsoft Edge Update verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="20839-412">Allows you to specify the proxy server settings that are used by Microsoft Edge Update.</span></span>

  <span data-ttu-id="20839-413">Wenn Sie diese Richtlinie aktivieren, können Sie zwischen den folgenden Proxyserveroptionen wählen:</span><span class="sxs-lookup"><span data-stu-id="20839-413">If you enable this policy, you can choose between the following proxy server options:</span></span>
   - <span data-ttu-id="20839-414">Wenn Sie niemals einen Proxyserver verwenden und immer eine direkte Verbindung herstellen, werden alle anderen Optionen ignoriert.</span><span class="sxs-lookup"><span data-stu-id="20839-414">If you choose to never use a proxy server and always connect directly, all other options are ignored.</span></span>
   - <span data-ttu-id="20839-415">Wenn Sie die System-Proxyeinstellungen verwenden oder den Proxyserver automatisch erkennen möchten, werden alle anderen Optionen ignoriert.</span><span class="sxs-lookup"><span data-stu-id="20839-415">If you choose to use system proxy settings or auto-detect the proxy server, all other options are ignored.</span></span>
   - <span data-ttu-id="20839-416">Wenn Sie den Proxymodus für feste Server auswählen, können Sie unter '[Adresse oder URL des Proxyservers](#proxyserver)' weitere Optionen angeben.</span><span class="sxs-lookup"><span data-stu-id="20839-416">If you choose fixed server proxy mode, you can specify further options in '[Address or URL of proxy server](#proxyserver)' policy.</span></span>
   - <span data-ttu-id="20839-417">Wenn Sie ein PAC-Proxyskript verwenden, müssen Sie die URL für das Skript unter '[URL zu einer PAC-Proxydatei](#proxypacurl)' angeben.</span><span class="sxs-lookup"><span data-stu-id="20839-417">If you choose to use a .pac proxy script, you must specify the URL for the script in '[URL to a proxy .pac file](#proxypacurl)' policy.</span></span>

  <span data-ttu-id="20839-418">Wenn Sie diese Richtlinie aktivieren, können Benutzer in Ihrer Organisation die Proxyeinstellungen in Microsoft Edge Update nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="20839-418">If you enable this policy, users in your organization can't change the proxy settings in Microsoft Edge Update.</span></span>

  <span data-ttu-id="20839-419">Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, werden keine Proxyservereinstellungen konfiguriert. Benutzer in Ihrer Organisation können jedoch ihre eigenen Proxyeinstellungen für Microsoft Edge Update auswählen.</span><span class="sxs-lookup"><span data-stu-id="20839-419">If you disable or don't configure this policy, no proxy server settings are configured, but users in your organization can choose their own proxy settings for Microsoft Edge Update.</span></span>
#### <span data-ttu-id="20839-420">Windows-Informationen und -Einstellungen</span><span class="sxs-lookup"><span data-stu-id="20839-420">Windows information and settings</span></span>
##### <span data-ttu-id="20839-421">Informationen zur Gruppenrichtlinie (ADMX)</span><span class="sxs-lookup"><span data-stu-id="20839-421">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="20839-422">Eindeutiger Name der GP: ProxyMode</span><span class="sxs-lookup"><span data-stu-id="20839-422">GP unique name: ProxyMode</span></span>
- <span data-ttu-id="20839-423">GP-Name: Möglichkeit zur Angabe der Proxyservereinstellungen wählen</span><span class="sxs-lookup"><span data-stu-id="20839-423">GP name: Choose how to specify proxy server settings</span></span>
- <span data-ttu-id="20839-424">GP-Pfad: Administrative Vorlagen/Microsoft Edge Update/Proxyserver</span><span class="sxs-lookup"><span data-stu-id="20839-424">GP path: Administrative Templates/Microsoft Edge Update/Proxy Server</span></span>
- <span data-ttu-id="20839-425">Name der GP-ADMX-Datei: edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="20839-425">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="20839-426">Windows-Registrierungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="20839-426">Windows Registry Settings</span></span>
- <span data-ttu-id="20839-427">Pfad: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="20839-427">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="20839-428">Name des Wertes: ProxyMode</span><span class="sxs-lookup"><span data-stu-id="20839-428">Value Name: ProxyMode</span></span>
- <span data-ttu-id="20839-429">Werttyp: REG_SZ</span><span class="sxs-lookup"><span data-stu-id="20839-429">Value Type: REG_SZ</span></span>
##### <span data-ttu-id="20839-430">Beispielwert:</span><span class="sxs-lookup"><span data-stu-id="20839-430">Example value:</span></span>
```
fixed_servers
```
[<span data-ttu-id="20839-431">Zurück zum Anfang</span><span class="sxs-lookup"><span data-stu-id="20839-431">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="20839-432">ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="20839-432">ProxyPacUrl</span></span>
#### <span data-ttu-id="20839-433">URL zu einer PAC-Proxydatei</span><span class="sxs-lookup"><span data-stu-id="20839-433">URL to a proxy .pac file</span></span>
><span data-ttu-id="20839-434">Microsoft Edge Update 1.3.21.81 und höher</span><span class="sxs-lookup"><span data-stu-id="20839-434">Microsoft Edge Update 1.3.21.81 and later</span></span>

#### <span data-ttu-id="20839-435">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="20839-435">Description</span></span>
<span data-ttu-id="20839-436">Ermöglicht die Angabe einer URL für eine PAC-Datei (Proxy Auto-Config).</span><span class="sxs-lookup"><span data-stu-id="20839-436">Allows you to specify a URL for a proxy auto-config (PAC) file.</span></span>

  <span data-ttu-id="20839-437">Wenn Sie diese Richtlinie aktivieren, können Sie eine URL für eine PAC-Datei angeben, um zu automatisieren, wie Microsoft Edge Update den geeigneten Proxyserver zum Abrufen einer bestimmten Website auswählt.</span><span class="sxs-lookup"><span data-stu-id="20839-437">If you enable this policy, you can specify a URL for a PAC file to automate how Microsoft Edge Update selects the appropriate proxy server for fetching a particular website.</span></span>

  <span data-ttu-id="20839-438">Diese Richtlinie wird nur angewendet, wenn Sie in der Richtlinie '[Möglichkeit zur Angabe der Proxyservereinstellungen wählen](#proxymode)' manuelle Proxyeinstellungen festgelegt haben.</span><span class="sxs-lookup"><span data-stu-id="20839-438">This policy is applied only if you have specified manual proxy settings in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>

  <span data-ttu-id="20839-439">Konfigurieren Sie diese Richtlinie nicht, wenn Sie eine andere Proxy-Einstellung als manuell in der Richtlinie '[Möglichkeit zur Angabe der Proxyservereinstellungen wählen](#proxymode)' ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="20839-439">Don't configure this policy if you have selected a proxy setting other than manual in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>
#### <span data-ttu-id="20839-440">Windows-Informationen und -Einstellungen</span><span class="sxs-lookup"><span data-stu-id="20839-440">Windows information and settings</span></span>
##### <span data-ttu-id="20839-441">Informationen zur Gruppenrichtlinie (ADMX)</span><span class="sxs-lookup"><span data-stu-id="20839-441">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="20839-442">Eindeutiger Name der GP: ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="20839-442">GP unique name: ProxyPacUrl</span></span>
- <span data-ttu-id="20839-443">GP-Name: URL zu einer PAC-Proxydatei</span><span class="sxs-lookup"><span data-stu-id="20839-443">GP name: URL to a proxy .pac file</span></span>
- <span data-ttu-id="20839-444">GP-Pfad: Administrative Vorlagen/Microsoft Edge Update/Proxyserver</span><span class="sxs-lookup"><span data-stu-id="20839-444">GP path: Administrative Templates/Microsoft Edge Update/Proxy Server</span></span>
- <span data-ttu-id="20839-445">Name der GP-ADMX-Datei: edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="20839-445">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="20839-446">Windows-Registrierungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="20839-446">Windows Registry Settings</span></span>
- <span data-ttu-id="20839-447">Pfad: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="20839-447">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="20839-448">Name des Wertes: ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="20839-448">Value Name: ProxyPacUrl</span></span>
- <span data-ttu-id="20839-449">Werttyp: REG_SZ</span><span class="sxs-lookup"><span data-stu-id="20839-449">Value Type: REG_SZ</span></span>
##### <span data-ttu-id="20839-450">Beispielwert:</span><span class="sxs-lookup"><span data-stu-id="20839-450">Example value:</span></span>
```
https://www.microsoft.com
```
[<span data-ttu-id="20839-451">Zurück zum Anfang</span><span class="sxs-lookup"><span data-stu-id="20839-451">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="20839-452">ProxyServer</span><span class="sxs-lookup"><span data-stu-id="20839-452">ProxyServer</span></span>
#### <span data-ttu-id="20839-453">Adresse oder URL des Proxyservers</span><span class="sxs-lookup"><span data-stu-id="20839-453">Address or URL of proxy server</span></span>
><span data-ttu-id="20839-454">Microsoft Edge Update 1.3.21.81 und höher</span><span class="sxs-lookup"><span data-stu-id="20839-454">Microsoft Edge Update 1.3.21.81 and later</span></span>

#### <span data-ttu-id="20839-455">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="20839-455">Description</span></span>
<span data-ttu-id="20839-456">Hier können Sie die URL des Proxy-Servers angeben, den Microsoft Edge Update verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="20839-456">Allows you to specify the URL of the proxy server for Microsoft Edge Update to use.</span></span>

  <span data-ttu-id="20839-457">Wenn Sie diese Richtlinie aktivieren, können Sie die Proxyserver-URL festlegen, die von Microsoft Edge Update in Ihrer Organisation verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="20839-457">If you enable this policy, you can set the proxy server URL used by Microsoft Edge Update in your organization.</span></span>

  <span data-ttu-id="20839-458">Diese Richtlinie wird nur angewendet, wenn Sie in der Richtlinie '[Möglichkeit zur Angabe der Proxyservereinstellungen wählen](#proxymode)' manuelle Proxyeinstellungen ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="20839-458">This policy is applied only if you have selected manual proxy settings in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>

  <span data-ttu-id="20839-459">Konfigurieren Sie diese Richtlinie nicht, wenn Sie eine andere Proxy-Einstellung als manuell in der Richtlinie '[Möglichkeit zur Angabe der Proxyservereinstellungen wählen](#proxymode)' ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="20839-459">Don't configure this policy if you have selected a proxy setting other than manual in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>
#### <span data-ttu-id="20839-460">Windows-Informationen und -Einstellungen</span><span class="sxs-lookup"><span data-stu-id="20839-460">Windows information and settings</span></span>
##### <span data-ttu-id="20839-461">Informationen zur Gruppenrichtlinie (ADMX)</span><span class="sxs-lookup"><span data-stu-id="20839-461">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="20839-462">Eindeutiger Name der GP: ProxyServer</span><span class="sxs-lookup"><span data-stu-id="20839-462">GP unique name: ProxyServer</span></span>
- <span data-ttu-id="20839-463">GP-Name: Adresse oder URL des Proxyservers</span><span class="sxs-lookup"><span data-stu-id="20839-463">GP name: Address or URL of proxy server</span></span>
- <span data-ttu-id="20839-464">GP-Pfad: Administrative Vorlagen/Microsoft Edge Update/Proxyserver</span><span class="sxs-lookup"><span data-stu-id="20839-464">GP path: Administrative Templates/Microsoft Edge Update/Proxy Server</span></span>
- <span data-ttu-id="20839-465">Name der GP-ADMX-Datei: edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="20839-465">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="20839-466">Windows-Registrierungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="20839-466">Windows Registry Settings</span></span>
- <span data-ttu-id="20839-467">Pfad: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="20839-467">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="20839-468">Name des Wertes: ProxyServer</span><span class="sxs-lookup"><span data-stu-id="20839-468">Value Name: ProxyServer</span></span>
- <span data-ttu-id="20839-469">Werttyp: REG_SZ</span><span class="sxs-lookup"><span data-stu-id="20839-469">Value Type: REG_SZ</span></span>
##### <span data-ttu-id="20839-470">Beispielwert:</span><span class="sxs-lookup"><span data-stu-id="20839-470">Example value:</span></span>
```
https://www.microsoft.com
```
[<span data-ttu-id="20839-471">Zurück zum Anfang</span><span class="sxs-lookup"><span data-stu-id="20839-471">Back to top</span></span>](#microsoft-edge---update-policies)


## <span data-ttu-id="20839-472">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="20839-472">See also</span></span>
  - [<span data-ttu-id="20839-473">Konfigurieren von Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="20839-473">Configuring Microsoft Edge</span></span>](configure-microsoft-edge.md)
  - [<span data-ttu-id="20839-474">Microsoft Edge Enterprise-Angebotsseite</span><span class="sxs-lookup"><span data-stu-id="20839-474">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
