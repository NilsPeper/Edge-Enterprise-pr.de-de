---
title: Dokumentation für die Microsoft Edge Update-Richtlinie
ms.author: stmoody
author: dan-wesley
manager: tahills
ms.date: 11/12/2020
audience: ITPro
ms.topic: reference
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
ms.custom: ''
description: Dokumentation für alle vom Microsoft Edge Updater unterstützten Richtlinien
ms.openlocfilehash: 0cdcda984efff8d10a84431e44c49ffbf28ddf07
ms.sourcegitcommit: c2ac4f889b625210b9365a60a447482fb5b4c9d4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/12/2020
ms.locfileid: "11167307"
---
# <span data-ttu-id="bfb45-103">Microsoft Edge – Update-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="bfb45-103">Microsoft Edge - Update policies</span></span>

<span data-ttu-id="bfb45-104">Die neueste Version von Microsoft Edge enthält die folgenden Richtlinien, mit denen Sie steuern können, wie und wann Microsoft Edge aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="bfb45-104">The latest version of Microsoft Edge includes the following policies that you can use to control how and when Microsoft Edge is updated.</span></span>

<span data-ttu-id="bfb45-105">Weitere Informationen zu anderen in Microsoft Edge verfügbaren Richtlinien finden Sie in der [Microsoft Edge Referenz für Browserrichtlinien](microsoft-edge-policies.md)</span><span class="sxs-lookup"><span data-stu-id="bfb45-105">For information about other policies available in Microsoft Edge, check out [Microsoft Edge browser policy reference](microsoft-edge-policies.md)</span></span>
> [!NOTE]
> <span data-ttu-id="bfb45-106">Dieser Artikel bezieht sich auf Microsoft Edge Version 77 oder höher.</span><span class="sxs-lookup"><span data-stu-id="bfb45-106">This article applies to Microsoft Edge version 77 or later.</span></span>
## <span data-ttu-id="bfb45-107">Verfügbare Richtlinien</span><span class="sxs-lookup"><span data-stu-id="bfb45-107">Available policies</span></span>
<span data-ttu-id="bfb45-108">In dieser Tabelle sind sämtliche, in dieser Version von Microsoft Edge verfügbaren Update-bezogenen Gruppenrichtlinien aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="bfb45-108">These tables lists all of the update-related group policies available in this release of Microsoft Edge.</span></span> <span data-ttu-id="bfb45-109">Über die Links in der folgenden Tabelle erhalten Sie weitere Einzelheiten zu bestimmten Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="bfb45-109">Use the links in the table to get more details about specific policies.</span></span>

|||
|-|-|
|[<span data-ttu-id="bfb45-110">Anwendungen</span><span class="sxs-lookup"><span data-stu-id="bfb45-110">Applications</span></span>](#applications)|[<span data-ttu-id="bfb45-111">Voreinstellungen</span><span class="sxs-lookup"><span data-stu-id="bfb45-111">Preferences</span></span>](#preferences)|
|[<span data-ttu-id="bfb45-112">Proxyserver</span><span class="sxs-lookup"><span data-stu-id="bfb45-112">Proxy Server</span></span>](#proxy-server)|[<span data-ttu-id="bfb45-113">Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="bfb45-113">Microsoft Edge WebView</span></span>](#microsoft-edge-webview)|

### [<span data-ttu-id="bfb45-114">Anwendungen</span><span class="sxs-lookup"><span data-stu-id="bfb45-114">Applications</span></span>](#applications-policies)
|<span data-ttu-id="bfb45-115">Richtlinienname</span><span class="sxs-lookup"><span data-stu-id="bfb45-115">Policy Name</span></span>|<span data-ttu-id="bfb45-116">Beschriftung</span><span class="sxs-lookup"><span data-stu-id="bfb45-116">Caption</span></span>|
|-|-|
|[<span data-ttu-id="bfb45-117">InstallDefault</span><span class="sxs-lookup"><span data-stu-id="bfb45-117">InstallDefault</span></span>](#installdefault)|<span data-ttu-id="bfb45-118">Standardinstallation zulassen</span><span class="sxs-lookup"><span data-stu-id="bfb45-118">Allow installation default</span></span>|
|[<span data-ttu-id="bfb45-119">UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="bfb45-119">UpdateDefault</span></span>](#updatedefault)|<span data-ttu-id="bfb45-120">Die Updaterichtlinie überschreibt die Standardrichtlinie</span><span class="sxs-lookup"><span data-stu-id="bfb45-120">Update policy override default</span></span>|
|[<span data-ttu-id="bfb45-121">Installieren</span><span class="sxs-lookup"><span data-stu-id="bfb45-121">Install</span></span>](#install)|<span data-ttu-id="bfb45-122">Installation zulassen (pro Kanal)</span><span class="sxs-lookup"><span data-stu-id="bfb45-122">Allow installation (per channel)</span></span>|
|[<span data-ttu-id="bfb45-123">Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="bfb45-123">Update</span></span>](#update)|<span data-ttu-id="bfb45-124">Außerkraftsetzung von Updaterichtlinien (pro Kanal)</span><span class="sxs-lookup"><span data-stu-id="bfb45-124">Update policy override (per channel)</span></span>|
|[<span data-ttu-id="bfb45-125">Allowsxs</span><span class="sxs-lookup"><span data-stu-id="bfb45-125">Allowsxs</span></span>](#allowsxs)|<span data-ttu-id="bfb45-126">Microsoft Edge Seite-an-Seite-Browserumgebung zulassen</span><span class="sxs-lookup"><span data-stu-id="bfb45-126">Allow Microsoft Edge Side by Side browser experience</span></span>|
|[<span data-ttu-id="bfb45-127">CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="bfb45-127">CreateDesktopShortcutDefault</span></span>](#createdesktopshortcutdefault)|<span data-ttu-id="bfb45-128">Standardeinstellung für das Verhindern der Erstellung von Desktopverknüpfungen bei der Installation</span><span class="sxs-lookup"><span data-stu-id="bfb45-128">Prevent Desktop Shortcut creation upon install default</span></span>|
|[<span data-ttu-id="bfb45-129">CreateDesktopShortcut</span><span class="sxs-lookup"><span data-stu-id="bfb45-129">CreateDesktopShortcut</span></span>](#createdesktopshortcut)|<span data-ttu-id="bfb45-130">Verhindern der Erstellung von Desktopverknüpfungen bei der Installation (pro Kanal)</span><span class="sxs-lookup"><span data-stu-id="bfb45-130">Prevent Desktop Shortcut creation upon install (per channel)</span></span>|
|[<span data-ttu-id="bfb45-131">RollbackToTargetVersion</span><span class="sxs-lookup"><span data-stu-id="bfb45-131">RollbackToTargetVersion</span></span>](#rollbacktotargetversion)|<span data-ttu-id="bfb45-132">Zurücksetzung auf Zielversion (pro Kanal)</span><span class="sxs-lookup"><span data-stu-id="bfb45-132">Rollback to Target version (per channel)</span></span>|
|[<span data-ttu-id="bfb45-133">TargetVersionPrefix</span><span class="sxs-lookup"><span data-stu-id="bfb45-133">TargetVersionPrefix</span></span>](#targetversionprefix)|<span data-ttu-id="bfb45-134">Außerkraftsetzung der Zielversion (pro Kanal)</span><span class="sxs-lookup"><span data-stu-id="bfb45-134">Target version override (per channel)</span></span>|

### [<span data-ttu-id="bfb45-135">Voreinstellungen</span><span class="sxs-lookup"><span data-stu-id="bfb45-135">Preferences</span></span>](#preferences-policies)
|<span data-ttu-id="bfb45-136">Richtlinienname</span><span class="sxs-lookup"><span data-stu-id="bfb45-136">Policy Name</span></span>|<span data-ttu-id="bfb45-137">Beschriftung</span><span class="sxs-lookup"><span data-stu-id="bfb45-137">Caption</span></span>|
|-|-|
|[<span data-ttu-id="bfb45-138">AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="bfb45-138">AutoUpdateCheckPeriodMinutes</span></span>](#autoupdatecheckperiodminutes)|<span data-ttu-id="bfb45-139">Überschreibung des Überprüfungszeitraums für automatische Updates</span><span class="sxs-lookup"><span data-stu-id="bfb45-139">Auto-update check period override</span></span>|
|[<span data-ttu-id="bfb45-140">UpdatesSuppressed</span><span class="sxs-lookup"><span data-stu-id="bfb45-140">UpdatesSuppressed</span></span>](#updatessuppressed)|<span data-ttu-id="bfb45-141">Zeitraum in jedem Tag zum Unterdrücken der automatischen Überprüfung auf Updates</span><span class="sxs-lookup"><span data-stu-id="bfb45-141">Time period in each day to suppress auto-update check</span></span>|

### [<span data-ttu-id="bfb45-142">Proxyserver</span><span class="sxs-lookup"><span data-stu-id="bfb45-142">Proxy Server</span></span>](#proxy-server-policies)
|<span data-ttu-id="bfb45-143">Richtlinienname</span><span class="sxs-lookup"><span data-stu-id="bfb45-143">Policy Name</span></span>|<span data-ttu-id="bfb45-144">Untertitel für Hörgeschädigte</span><span class="sxs-lookup"><span data-stu-id="bfb45-144">Caption</span></span>|
|-|-|
|[<span data-ttu-id="bfb45-145">ProxyMode</span><span class="sxs-lookup"><span data-stu-id="bfb45-145">ProxyMode</span></span>](#proxymode)|<span data-ttu-id="bfb45-146">Möglichkeit zur Angabe der Proxyservereinstellungen wählen</span><span class="sxs-lookup"><span data-stu-id="bfb45-146">Choose how to specify proxy server settings</span></span>|
|[<span data-ttu-id="bfb45-147">ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="bfb45-147">ProxyPacUrl</span></span>](#proxypacurl)|<span data-ttu-id="bfb45-148">URL zu einer PAC-Proxydatei</span><span class="sxs-lookup"><span data-stu-id="bfb45-148">URL to a proxy .pac file</span></span>|
|[<span data-ttu-id="bfb45-149">ProxyServer</span><span class="sxs-lookup"><span data-stu-id="bfb45-149">ProxyServer</span></span>](#proxyserver)|<span data-ttu-id="bfb45-150">Adresse oder URL des Proxyservers</span><span class="sxs-lookup"><span data-stu-id="bfb45-150">Address or URL of proxy server</span></span>|

### [<span data-ttu-id="bfb45-151">Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="bfb45-151">Microsoft Edge WebView</span></span>](#microsoft-edge-webview-policies)
|<span data-ttu-id="bfb45-152">Richtlinienname</span><span class="sxs-lookup"><span data-stu-id="bfb45-152">Policy Name</span></span>|<span data-ttu-id="bfb45-153">Beschriftung</span><span class="sxs-lookup"><span data-stu-id="bfb45-153">Caption</span></span>|
|-|-|
|[<span data-ttu-id="bfb45-154">Installieren</span><span class="sxs-lookup"><span data-stu-id="bfb45-154">Install</span></span>](#install-webview)|<span data-ttu-id="bfb45-155">Installation zulassen</span><span class="sxs-lookup"><span data-stu-id="bfb45-155">Allow installation</span></span>|
|[<span data-ttu-id="bfb45-156">Update/Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="bfb45-156">Update</span></span>](#update-webview)|<span data-ttu-id="bfb45-157">Außerkraftsetzung von Updaterichtlinien</span><span class="sxs-lookup"><span data-stu-id="bfb45-157">Update policy override</span></span>|

## <span data-ttu-id="bfb45-158">Anwendungsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="bfb45-158">Applications policies</span></span>

[<span data-ttu-id="bfb45-159">Zurück zum Anfang</span><span class="sxs-lookup"><span data-stu-id="bfb45-159">Back to top</span></span>](#microsoft-edge---update-policies)
### <span data-ttu-id="bfb45-160">InstallDefault</span><span class="sxs-lookup"><span data-stu-id="bfb45-160">InstallDefault</span></span>
#### <span data-ttu-id="bfb45-161">Standardinstallation zulassen</span><span class="sxs-lookup"><span data-stu-id="bfb45-161">Allow installation default</span></span>
><span data-ttu-id="bfb45-162">Microsoft Edge Update 1.2.145.5 und höher</span><span class="sxs-lookup"><span data-stu-id="bfb45-162">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="bfb45-163">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bfb45-163">Description</span></span>
<span data-ttu-id="bfb45-164">Sie können das Standardverhalten aller Kanäle festlegen, damit Microsoft Edge für in die Domäne eingebundene Geräte. zugelassen oder blockiert wird.</span><span class="sxs-lookup"><span data-stu-id="bfb45-164">You can specify the default behavior of all channels to allow or block Microsoft Edge on domain-joined devices.</span></span>

<span data-ttu-id="bfb45-165">Sie können diese Richtlinie für einzelne Kanäle außer Kraft setzen, indem Sie die Richtlinie '[Installation zulassen](#install)' für bestimmte Kanäle aktivieren.</span><span class="sxs-lookup"><span data-stu-id="bfb45-165">You can override this policy for individual channels by enabling the '[Allow installation](#install)' policy for specific channels.</span></span>

<span data-ttu-id="bfb45-166">Wenn Sie diese Richtlinie deaktivieren, wird die Installation von Microsoft Edge blockiert.</span><span class="sxs-lookup"><span data-stu-id="bfb45-166">If you disable this policy, the installation of Microsoft Edge is blocked.</span></span> <span data-ttu-id="bfb45-167">Dies wirkt sich nur auf die Installation der Microsoft Edge-Software aus, wenn die Richtlinie "[Installation zulassen](#install)" auf "nicht konfiguriert festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="bfb45-167">This only affects the installation of Microsoft Edge software when the '[Allow installation](#install)' policy is set to Not Configured.</span></span>

<span data-ttu-id="bfb45-168">Diese Richtlinie verhindert nicht, dass Microsoft Edge Update ausgeführt wird, oder dass Benutzer die Microsoft Edge-Software auf andere Weise installieren.</span><span class="sxs-lookup"><span data-stu-id="bfb45-168">This policy doesn't prevent Microsoft Edge Update from running or prevent users from installing Microsoft Edge software using other methods.</span></span>

<span data-ttu-id="bfb45-169">Diese Richtlinie ist nur für Windows-Instanzen verfügbar, die in eine Microsoft® Active Directory®-Domäne eingebunden werden.</span><span class="sxs-lookup"><span data-stu-id="bfb45-169">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <span data-ttu-id="bfb45-170">Windows-Informationen und -Einstellungen</span><span class="sxs-lookup"><span data-stu-id="bfb45-170">Windows information and settings</span></span>
##### <span data-ttu-id="bfb45-171">Informationen zur Gruppenrichtlinie (ADMX)</span><span class="sxs-lookup"><span data-stu-id="bfb45-171">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="bfb45-172">Eindeutiger Name der GP: InstallDefault</span><span class="sxs-lookup"><span data-stu-id="bfb45-172">GP unique name: InstallDefault</span></span>
- <span data-ttu-id="bfb45-173">GP-Name: Standardinstallation zulassen</span><span class="sxs-lookup"><span data-stu-id="bfb45-173">GP name: Allow installation default</span></span>
- <span data-ttu-id="bfb45-174">GP-Pfad: Administrative Vorlagen/Microsoft Edge Update/Anwendungen</span><span class="sxs-lookup"><span data-stu-id="bfb45-174">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="bfb45-175">Name der GP-ADMX-Datei: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="bfb45-175">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="bfb45-176">Windows-Registrierungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="bfb45-176">Windows Registry Settings</span></span>
- <span data-ttu-id="bfb45-177">Pfad: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="bfb45-177">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="bfb45-178">Name des Wertes: InstallDefault</span><span class="sxs-lookup"><span data-stu-id="bfb45-178">Value Name: InstallDefault</span></span>
- <span data-ttu-id="bfb45-179">Werttyp: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="bfb45-179">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="bfb45-180">Beispielwert:</span><span class="sxs-lookup"><span data-stu-id="bfb45-180">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="bfb45-181">Zurück zum Anfang</span><span class="sxs-lookup"><span data-stu-id="bfb45-181">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="bfb45-182">UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="bfb45-182">UpdateDefault</span></span>
#### <span data-ttu-id="bfb45-183">Die Updaterichtlinie überschreibt die Standardrichtlinie</span><span class="sxs-lookup"><span data-stu-id="bfb45-183">Update policy override default</span></span>
><span data-ttu-id="bfb45-184">Microsoft Edge Update 1.2.145.5 und höher</span><span class="sxs-lookup"><span data-stu-id="bfb45-184">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="bfb45-185">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bfb45-185">Description</span></span>
<span data-ttu-id="bfb45-186">Hier können Sie das Standardverhalten für alle Kanäle angeben, wie Microsoft Edge Update verfügbare Updates für Microsoft Edge verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="bfb45-186">Lets you specify the default behavior for all channels concerning the way Microsoft Edge Update handles available updates for Microsoft Edge.</span></span> <span data-ttu-id="bfb45-187">Kann für einzelne Kanäle durch Angabe der Richtlinie '[Außerkraftsetzung von Updaterichtlinien](#update)' für diese bestimmten Kanäle außer Kraft gesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="bfb45-187">Can be overridden for individual channels by specifying the '[Update policy override](#update)' policy for those specific channels.</span></span>

  <span data-ttu-id="bfb45-188">Wenn Sie diese Richtlinie aktivieren, verarbeitet Microsoft Edge Update Microsoft Edge-Updates entsprechend der Konfiguration der folgenden Optionen:</span><span class="sxs-lookup"><span data-stu-id="bfb45-188">If you enable this policy, Microsoft Edge Update handles Microsoft Edge updates according to how you configure the following options:</span></span>
   - <span data-ttu-id="bfb45-189">Updates immer zulassen: Updates werden immer dann angewendet, wenn sie gefunden werden, entweder durch die regelmäßige Updateprüfung oder durch eine manuelle Updateprüfung.</span><span class="sxs-lookup"><span data-stu-id="bfb45-189">Always allow updates: Updates are always applied when found, either by periodic update check or by a manual update check.</span></span>
   - <span data-ttu-id="bfb45-190">Nur automatische unbeaufsichtigte Updates: Updates werden nur angewendet, wenn sie von der regelmäßigen Updateprüfung gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="bfb45-190">Automatic silent updates only: Updates are applied only when they're found by the periodic update check.</span></span>
   - <span data-ttu-id="bfb45-191">Nur manuelle Updates: Updates werden nur angewendet, wenn der Benutzer eine manuelle Updateprüfung ausführt.</span><span class="sxs-lookup"><span data-stu-id="bfb45-191">Manual updates only: Updates are applied only when the user runs a manual update check.</span></span>
   - <span data-ttu-id="bfb45-192">Updates deaktiviert: Updates werden nie angewendet.</span><span class="sxs-lookup"><span data-stu-id="bfb45-192">Updates disabled: Updates are never applied.</span></span>

  <span data-ttu-id="bfb45-193">Wenn Sie „manuelle Updates” auswählen, stellen Sie sicher, dass Sie regelmäßig nach Updates suchen, indem Sie den manuellen Updatemechanismus der App verwenden, sofern verfügbar.</span><span class="sxs-lookup"><span data-stu-id="bfb45-193">If you select manual updates, make sure you periodically check for updates by using the app's manual update mechanism, if available.</span></span> <span data-ttu-id="bfb45-194">Wenn Sie Updates deaktivieren, suchen Sie regelmäßig nach Updates und verteilen Sie diese an die Benutzer.</span><span class="sxs-lookup"><span data-stu-id="bfb45-194">If you disable updates, periodically check for updates, and distribute them to users.</span></span>

  <span data-ttu-id="bfb45-195">Wenn Sie diese Richtlinie nicht aktivieren und konfigurieren, behandelt Microsoft Edge Update die verfügbaren Updates gemäß der Richtlinie '[Außerkraftsetzung von Updaterichtlinien](#update)'.</span><span class="sxs-lookup"><span data-stu-id="bfb45-195">If you don't enable and configure this policy, Microsoft Edge Update handles available updates as specified by the '[Update policy override](#update)' policy.</span></span>

  <span data-ttu-id="bfb45-196">Diese Richtlinie ist nur für Windows-Instanzen verfügbar, die in eine Microsoft® Active Directory®-Domäne eingebunden werden.</span><span class="sxs-lookup"><span data-stu-id="bfb45-196">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <span data-ttu-id="bfb45-197">Windows-Informationen und -Einstellungen</span><span class="sxs-lookup"><span data-stu-id="bfb45-197">Windows information and settings</span></span>
##### <span data-ttu-id="bfb45-198">Informationen zur Gruppenrichtlinie (ADMX)</span><span class="sxs-lookup"><span data-stu-id="bfb45-198">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="bfb45-199">Eindeutiger Name der GP: UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="bfb45-199">GP unique name: UpdateDefault</span></span>
- <span data-ttu-id="bfb45-200">GP-Name: Die Updaterichtlinie überschreibt die Standardrichtlinie</span><span class="sxs-lookup"><span data-stu-id="bfb45-200">GP name: Update policy override default</span></span>
- <span data-ttu-id="bfb45-201">GP-Pfad: Administrative Vorlagen/Microsoft Edge Update/Anwendungen</span><span class="sxs-lookup"><span data-stu-id="bfb45-201">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="bfb45-202">Name der GP-ADMX-Datei: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="bfb45-202">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="bfb45-203">Windows-Registrierungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="bfb45-203">Windows Registry Settings</span></span>
- <span data-ttu-id="bfb45-204">Pfad: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="bfb45-204">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="bfb45-205">Name des Wertes: UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="bfb45-205">Value Name: UpdateDefault</span></span>
- <span data-ttu-id="bfb45-206">Werttyp: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="bfb45-206">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="bfb45-207">Beispielwert:</span><span class="sxs-lookup"><span data-stu-id="bfb45-207">Example value:</span></span>
```
0x00000003
```
[<span data-ttu-id="bfb45-208">Zurück zum Anfang</span><span class="sxs-lookup"><span data-stu-id="bfb45-208">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="bfb45-209">Installieren</span><span class="sxs-lookup"><span data-stu-id="bfb45-209">Install</span></span>
#### <span data-ttu-id="bfb45-210">Installation zulassen</span><span class="sxs-lookup"><span data-stu-id="bfb45-210">Allow installation</span></span>
><span data-ttu-id="bfb45-211">Microsoft Edge Update 1.2.145.5 und höher</span><span class="sxs-lookup"><span data-stu-id="bfb45-211">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="bfb45-212">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bfb45-212">Description</span></span>
<span data-ttu-id="bfb45-213">Gibt an, ob ein Microsoft Edge-Kanal auf in die Domäne eingebundene Geräte installiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="bfb45-213">Specifies whether a Microsoft Edge channel can be installed on domain-joined devices.</span></span>

  <span data-ttu-id="bfb45-214">Wenn Sie diese Richtlinie für einen Kanal aktivieren, wird die Installation von Microsoft Edge nicht blockiert.</span><span class="sxs-lookup"><span data-stu-id="bfb45-214">If you enable this policy for a channel, Microsoft Edge will not be blocked from installation.</span></span>

  <span data-ttu-id="bfb45-215">Wenn Sie diese Richtlinie für einen Kanal deaktivieren, wird die Installation von Microsoft Edge blockiert.</span><span class="sxs-lookup"><span data-stu-id="bfb45-215">If you disable this policy for a channel, Microsoft Edge will be blocked from installation.</span></span>

  <span data-ttu-id="bfb45-216">Wenn Sie diese Richtlinie nicht für einen Kanal konfigurieren, bestimmt die Richtlinienkonfiguration '[Standardinstallation zulassen](#installdefault)', ob Benutzer diesen Kanal von Microsoft Edge installieren können.</span><span class="sxs-lookup"><span data-stu-id="bfb45-216">If you don't configure this policy for a channel, the '[Allow installation default](#installdefault)' policy configuration determines whether users can install that channel of Microsoft Edge.</span></span>

  <span data-ttu-id="bfb45-217">Diese Richtlinie ist nur für Windows-Instanzen verfügbar, die in eine Microsoft® Active Directory®-Domäne eingebunden werden.</span><span class="sxs-lookup"><span data-stu-id="bfb45-217">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <span data-ttu-id="bfb45-218">Windows-Informationen und -Einstellungen</span><span class="sxs-lookup"><span data-stu-id="bfb45-218">Windows information and settings</span></span>
##### <span data-ttu-id="bfb45-219">Informationen zur Gruppenrichtlinie (ADMX)</span><span class="sxs-lookup"><span data-stu-id="bfb45-219">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="bfb45-220">Eindeutiger Name der GP: Install</span><span class="sxs-lookup"><span data-stu-id="bfb45-220">GP unique name: Install</span></span>
- <span data-ttu-id="bfb45-221">GP-Name: Installation zulassen</span><span class="sxs-lookup"><span data-stu-id="bfb45-221">GP name: Allow installation</span></span>
- <span data-ttu-id="bfb45-222">GP-Pfad:</span><span class="sxs-lookup"><span data-stu-id="bfb45-222">GP path:</span></span> 
  - <span data-ttu-id="bfb45-223">Administrative Vorlagen/Microsoft Edge Update/Anwendungen/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="bfb45-223">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="bfb45-224">Administrative Vorlagen/Microsoft Edge Update/Anwendungen/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="bfb45-224">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="bfb45-225">Administrative Vorlagen/Microsoft Edge Update/Anwendungen/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="bfb45-225">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="bfb45-226">Administrative Vorlagen/Microsoft Edge Update/Anwendungen/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="bfb45-226">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="bfb45-227">Name der GP-ADMX-Datei: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="bfb45-227">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="bfb45-228">Windows-Registrierungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="bfb45-228">Windows Registry Settings</span></span>
- <span data-ttu-id="bfb45-229">Pfad: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="bfb45-229">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="bfb45-230">Name des Wertes:</span><span class="sxs-lookup"><span data-stu-id="bfb45-230">Value Name:</span></span> 
  - <span data-ttu-id="bfb45-231">(Stable): Install{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="bfb45-231">(Stable): Install{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="bfb45-232">(Beta): Install{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="bfb45-232">(Beta): Install{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="bfb45-233">(Canary): Install{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="bfb45-233">(Canary): Install{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="bfb45-234">(Dev): Install{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="bfb45-234">(Dev): Install{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="bfb45-235">Werttyp: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="bfb45-235">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="bfb45-236">Beispielwert:</span><span class="sxs-lookup"><span data-stu-id="bfb45-236">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="bfb45-237">Zurück zum Anfang</span><span class="sxs-lookup"><span data-stu-id="bfb45-237">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="bfb45-238">Update</span><span class="sxs-lookup"><span data-stu-id="bfb45-238">Update</span></span>
#### <span data-ttu-id="bfb45-239">Außerkraftsetzung von Updaterichtlinien</span><span class="sxs-lookup"><span data-stu-id="bfb45-239">Update policy override</span></span>
><span data-ttu-id="bfb45-240">Microsoft Edge Update 1.2.145.5 und höher</span><span class="sxs-lookup"><span data-stu-id="bfb45-240">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="bfb45-241">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bfb45-241">Description</span></span>
<span data-ttu-id="bfb45-242">Gibt an, wie Microsoft Edge Update verfügbare Updates von Microsoft Edge behandelt.</span><span class="sxs-lookup"><span data-stu-id="bfb45-242">Specifies how Microsoft Edge Update handles available updates from Microsoft Edge.</span></span>

<span data-ttu-id="bfb45-243">Wenn Sie diese Richtlinie aktivieren, verarbeitet Microsoft Edge Update Microsoft Edge-Updates entsprechend der Konfiguration der folgenden Optionen:</span><span class="sxs-lookup"><span data-stu-id="bfb45-243">If you enable this policy, Microsoft Edge Update handles Microsoft Edge updates according to how you configure the following options:</span></span>
  - <span data-ttu-id="bfb45-244">Updates immer zulassen: Updates werden immer dann angewendet, wenn sie gefunden werden, entweder durch die regelmäßige Updateprüfung oder durch eine manuelle Updateprüfung.</span><span class="sxs-lookup"><span data-stu-id="bfb45-244">Always allow updates: Updates are always applied when found, either by periodic update check or by a manual update check.</span></span>
  - <span data-ttu-id="bfb45-245">Nur automatische unbeaufsichtigte Updates: Updates werden nur angewendet, wenn sie von der regelmäßigen Updateprüfung gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="bfb45-245">Automatic silent updates only: Updates are applied only when they're found by the periodic update check.</span></span>
  - <span data-ttu-id="bfb45-246">Nur manuelle Updates: Updates werden nur angewendet, wenn der Benutzer eine manuelle Updateprüfung ausführt.</span><span class="sxs-lookup"><span data-stu-id="bfb45-246">Manual updates only: Updates are applied only when the user runs a manual update check.</span></span> <span data-ttu-id="bfb45-247">(Nicht alle Apps bieten eine Schnittstelle für diese Option.)</span><span class="sxs-lookup"><span data-stu-id="bfb45-247">(Not all apps provide an interface for this option.)</span></span>
  - <span data-ttu-id="bfb45-248">Updates deaktiviert: Updates werden nie angewendet.</span><span class="sxs-lookup"><span data-stu-id="bfb45-248">Updates disabled: Updates are never applied.</span></span>

<span data-ttu-id="bfb45-249">Wenn Sie „manuelle Updates” auswählen, stellen Sie sicher, dass Sie regelmäßig nach Updates suchen, indem Sie den manuellen Updatemechanismus der App verwenden, sofern verfügbar.</span><span class="sxs-lookup"><span data-stu-id="bfb45-249">If you select manual updates, make sure you periodically check for updates by using the app's manual update mechanism, if available.</span></span> <span data-ttu-id="bfb45-250">Wenn Sie Updates deaktivieren, suchen Sie regelmäßig nach Updates und verteilen Sie diese an die Benutzer.</span><span class="sxs-lookup"><span data-stu-id="bfb45-250">If you disable updates, periodically check for updates, and distribute them to users.</span></span>

<span data-ttu-id="bfb45-251">Wenn Sie diese Richtlinie nicht aktivieren und konfigurieren, behandelt Microsoft Edge Update die verfügbaren Updates gemäß der Richtlinie '[Die Updaterichtlinie überschreibt die Standardrichtlinie](#updatedefault)'.</span><span class="sxs-lookup"><span data-stu-id="bfb45-251">If you don't enable and configure this policy, Microsoft Edge Update handles available updates as specified by the '[Update policy override default](#updatedefault)' policy.</span></span>

<span data-ttu-id="bfb45-252">Weitere Informationen finden Sie unter [https://go.microsoft.com/fwlink/?linkid=2136406](https://go.microsoft.com/fwlink/?linkid=2136406).</span><span class="sxs-lookup"><span data-stu-id="bfb45-252">See [https://go.microsoft.com/fwlink/?linkid=2136406](https://go.microsoft.com/fwlink/?linkid=2136406) for more information.</span></span>

<span data-ttu-id="bfb45-253">Diese Richtlinie ist nur für Windows-Instanzen verfügbar, die in eine Microsoft® Active Directory®-Domäne eingebunden werden.</span><span class="sxs-lookup"><span data-stu-id="bfb45-253">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <span data-ttu-id="bfb45-254">Windows-Informationen und -Einstellungen</span><span class="sxs-lookup"><span data-stu-id="bfb45-254">Windows information and settings</span></span>
##### <span data-ttu-id="bfb45-255">Informationen zur Gruppenrichtlinie (ADMX)</span><span class="sxs-lookup"><span data-stu-id="bfb45-255">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="bfb45-256">Eindeutiger Name der GP: Update</span><span class="sxs-lookup"><span data-stu-id="bfb45-256">GP unique name: Update</span></span>
- <span data-ttu-id="bfb45-257">GP-Name: Außerkraftsetzung von Updaterichtlinien</span><span class="sxs-lookup"><span data-stu-id="bfb45-257">GP name: Update policy override</span></span>
- <span data-ttu-id="bfb45-258">GP-Pfad:</span><span class="sxs-lookup"><span data-stu-id="bfb45-258">GP path:</span></span> 
  - <span data-ttu-id="bfb45-259">Administrative Vorlagen/Microsoft Edge Update/Anwendungen/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="bfb45-259">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="bfb45-260">Administrative Vorlagen/Microsoft Edge Update/Anwendungen/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="bfb45-260">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="bfb45-261">Administrative Vorlagen/Microsoft Edge Update/Anwendungen/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="bfb45-261">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="bfb45-262">Administrative Vorlagen/Microsoft Edge Update/Anwendungen/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="bfb45-262">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="bfb45-263">Name der GP-ADMX-Datei: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="bfb45-263">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="bfb45-264">Windows-Registrierungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="bfb45-264">Windows Registry Settings</span></span>
- <span data-ttu-id="bfb45-265">Pfad: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="bfb45-265">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="bfb45-266">Name des Wertes:</span><span class="sxs-lookup"><span data-stu-id="bfb45-266">Value Name:</span></span> 
  - <span data-ttu-id="bfb45-267">(Stable): Update{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="bfb45-267">(Stable): Update{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="bfb45-268">(Beta): Update{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="bfb45-268">(Beta): Update{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="bfb45-269">(Canary): Update{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="bfb45-269">(Canary): Update{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="bfb45-270">(Dev): Update{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="bfb45-270">(Dev): Update{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="bfb45-271">Werttyp: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="bfb45-271">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="bfb45-272">Beispielwert:</span><span class="sxs-lookup"><span data-stu-id="bfb45-272">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="bfb45-273">Zurück zum Anfang</span><span class="sxs-lookup"><span data-stu-id="bfb45-273">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="bfb45-274">Allowsxs</span><span class="sxs-lookup"><span data-stu-id="bfb45-274">Allowsxs</span></span>
#### <span data-ttu-id="bfb45-275">Microsoft Edge Seite-an-Seite-Browserumgebung zulassen</span><span class="sxs-lookup"><span data-stu-id="bfb45-275">Allow Microsoft Edge Side by Side browser experience</span></span>
><span data-ttu-id="bfb45-276">Microsoft Edge Update 1.2.145.5 und höher</span><span class="sxs-lookup"><span data-stu-id="bfb45-276">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="bfb45-277">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bfb45-277">Description</span></span>
<span data-ttu-id="bfb45-278">Mit dieser Richtlinie können Benutzer Microsoft Edge (Edge-HTML) und Microsoft Edge (Chromium-basiert) nebeneinander ausführen.</span><span class="sxs-lookup"><span data-stu-id="bfb45-278">This policy lets a user run Microsoft Edge (Edge HTML) and Microsoft Edge (Chromium-based) side-by-side.</span></span>

<span data-ttu-id="bfb45-279">Wenn diese Richtlinie auf „Nicht konfiguriert” festgelegt ist, ersetzt Microsoft Edge (Chromium-basiert) Microsoft Edge (Edge-HTML) nach dem stabilen Kanal von Microsoft Edge (Chromium-basierten), und die Sicherheitsupdates vom November2019 werden installiert.</span><span class="sxs-lookup"><span data-stu-id="bfb45-279">If this policy is set to “Not configured”, Microsoft Edge (Chromium-based) will replace Microsoft Edge (Edge HTML) after the Microsoft Edge (Chromium-based) stable channel and the November 2019 security updates are installed.</span></span>  <span data-ttu-id="bfb45-280">Hierbei handelt es sich um das gleiche Verhalten wie bei der Einstellung „Deaktiviert“.</span><span class="sxs-lookup"><span data-stu-id="bfb45-280">This is the same behavior as the “Disabled” setting.</span></span>

<span data-ttu-id="bfb45-281">Die Einstellung „Deaktiviert” blockiert eine Seite-an-Seite-Umgebung, und Microsoft Edge (Chromium-basiert) ersetzt Microsoft Edge (Edge-HTML) nach dem stabilen Kanal von Microsoft Edge (Chromium-basierten). Außerdem werden die Sicherheitsupdates vom November2019 installiert.</span><span class="sxs-lookup"><span data-stu-id="bfb45-281">The “Disabled” setting blocks a side-by-side experience and Microsoft Edge (Chromium-based) will replace Microsoft Edge (Edge HTML) after the Microsoft Edge (Chromium-based) stable channel and the November 2019 security updates are installed.</span></span>  <span data-ttu-id="bfb45-282">Hierbei handelt es sich um das gleiche Verhalten wie bei der Einstellung „Nicht konfiguriert“.</span><span class="sxs-lookup"><span data-stu-id="bfb45-282">This is the same behavior as the “Not Configured” setting.</span></span>

<span data-ttu-id="bfb45-283">Wenn diese Richtlinie aktiviert ist, können Microsoft Edge (Chromium-basiert) und Microsoft Edge (Edge-HTML) nach der Installation von Microsoft Edge (Chromium-basiert) nebeneinander ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="bfb45-283">When this policy is “Enabled”, Microsoft Edge (Chromium-based) and Microsoft Edge (Edge HTML) can run side-by-side after Microsoft Edge (Chromium-based) is installed.</span></span>

<span data-ttu-id="bfb45-284">Damit diese Gruppenrichtlinie wirksam wird, muss sie vor der automatischen Installation von Microsoft Edge (Chromium-basiert) von Windows Update konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="bfb45-284">For this group policy to take affect, it must be configured before the automatic install of Microsoft Edge (Chromium-based) by Windows Update.</span></span> <span data-ttu-id="bfb45-285">Hinweis: Ein Benutzer kann das automatische Update von Microsoft Edge (Chromium-basiert) mit dem Microsoft Edge (Chromium-basiert) Blocker Toolkit blockieren.</span><span class="sxs-lookup"><span data-stu-id="bfb45-285">Note: A user can block the automatic update of Microsoft Edge (Chromium-based) by using the Microsoft Edge (Chromium-based) Blocker Toolkit.</span></span>
#### <span data-ttu-id="bfb45-286">Windows-Informationen und -Einstellungen</span><span class="sxs-lookup"><span data-stu-id="bfb45-286">Windows information and settings</span></span>
##### <span data-ttu-id="bfb45-287">Informationen zur Gruppenrichtlinie (ADMX)</span><span class="sxs-lookup"><span data-stu-id="bfb45-287">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="bfb45-288">Eindeutiger Name der GP: Allowsxs</span><span class="sxs-lookup"><span data-stu-id="bfb45-288">GP unique name: Allowsxs</span></span>
- <span data-ttu-id="bfb45-289">GP-Name: Microsoft Edge Seite-an-Seite-Browserumgebung zulassen</span><span class="sxs-lookup"><span data-stu-id="bfb45-289">GP name: Allow Microsoft Edge Side by Side browser experience</span></span>
- <span data-ttu-id="bfb45-290">GP-Pfad: Administrative Vorlagen/Microsoft Edge Update/Anwendungen</span><span class="sxs-lookup"><span data-stu-id="bfb45-290">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="bfb45-291">Name der GP-ADMX-Datei: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="bfb45-291">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="bfb45-292">Windows-Registrierungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="bfb45-292">Windows Registry Settings</span></span>
- <span data-ttu-id="bfb45-293">Pfad: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="bfb45-293">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="bfb45-294">Name des Wertes: Allowsxs</span><span class="sxs-lookup"><span data-stu-id="bfb45-294">Value Name: Allowsxs</span></span>
- <span data-ttu-id="bfb45-295">Werttyp: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="bfb45-295">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="bfb45-296">Beispielwert:</span><span class="sxs-lookup"><span data-stu-id="bfb45-296">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="bfb45-297">Zurück zum Anfang</span><span class="sxs-lookup"><span data-stu-id="bfb45-297">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="bfb45-298">CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="bfb45-298">CreateDesktopShortcutDefault</span></span>
#### <span data-ttu-id="bfb45-299">Standardeinstellung für das Verhindern der Erstellung von Desktopverknüpfungen bei der Installation</span><span class="sxs-lookup"><span data-stu-id="bfb45-299">Prevent Desktop Shortcut creation upon install default</span></span>
><span data-ttu-id="bfb45-300">Microsoft Edge Update 1.3.128.0 und höher</span><span class="sxs-lookup"><span data-stu-id="bfb45-300">Microsoft Edge Update 1.3.128.0 and later</span></span>

#### <span data-ttu-id="bfb45-301">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bfb45-301">Description</span></span>
<span data-ttu-id="bfb45-302">Ermöglicht es Ihnen, das Standardverhalten aller Kanäle für die Erstellung einer Desktopverknüpfung festzulegen, wenn Microsoft Edge installiert wird.</span><span class="sxs-lookup"><span data-stu-id="bfb45-302">Lets you specify the default behavior for all channels for creating a desktop shortcut when Microsoft Edge is installed.</span></span>

  <span data-ttu-id="bfb45-303">Wenn Sie diese Richtlinie aktivieren, wird beim Installieren von Microsoft Edge eine Desktopverknüpfung erstellt.</span><span class="sxs-lookup"><span data-stu-id="bfb45-303">If you enable this policy a desktop shortcut is created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="bfb45-304">Wenn Sie diese Richtlinie deaktivieren, wird beim Installieren von Microsoft Edge keine Desktopverknüpfung erstellt.</span><span class="sxs-lookup"><span data-stu-id="bfb45-304">If you disable this policy, no desktop shortcut will be created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="bfb45-305">Wenn Sie diese Richtlinie nicht konfigurieren, wird während der Installation eine Desktopverknüpfung zu Microsoft Edge erstellt.</span><span class="sxs-lookup"><span data-stu-id="bfb45-305">If you don’t configure this policy a desktop shortcut to Microsoft Edge will be created during installation.</span></span>
<span data-ttu-id="bfb45-306">Wenn Microsoft Edge bereits installiert ist, hat diese Richtlinie keine Auswirkung.</span><span class="sxs-lookup"><span data-stu-id="bfb45-306">If Microsoft Edge is already installed, this policy will have no effect.</span></span>
#### <span data-ttu-id="bfb45-307">Windows-Informationen und -Einstellungen</span><span class="sxs-lookup"><span data-stu-id="bfb45-307">Windows information and settings</span></span>
##### <span data-ttu-id="bfb45-308">Informationen zur Gruppenrichtlinie (ADMX)</span><span class="sxs-lookup"><span data-stu-id="bfb45-308">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="bfb45-309">Eindeutiger Name der GP: CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="bfb45-309">GP unique name: CreateDesktopShortcutDefault</span></span>
- <span data-ttu-id="bfb45-310">GP-Name: Standardeinstellung "Erstellung von Desktopverknüpfungen bei der Installation verhindern"</span><span class="sxs-lookup"><span data-stu-id="bfb45-310">GP name: Prevent Desktop Shortcut creation upon install default</span></span>
- <span data-ttu-id="bfb45-311">GP-Pfad: Administrative Vorlagen/Microsoft Edge Update/Anwendungen</span><span class="sxs-lookup"><span data-stu-id="bfb45-311">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="bfb45-312">Name der GP-ADMX-Datei: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="bfb45-312">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="bfb45-313">Windows-Registrierungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="bfb45-313">Windows Registry Settings</span></span>
- <span data-ttu-id="bfb45-314">Pfad: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="bfb45-314">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="bfb45-315">Wertname: CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="bfb45-315">Value Name: CreateDesktopShortcutDefault</span></span>
- <span data-ttu-id="bfb45-316">Werttyp: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="bfb45-316">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="bfb45-317">Beispielwert:</span><span class="sxs-lookup"><span data-stu-id="bfb45-317">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="bfb45-318">Zurück zum Anfang</span><span class="sxs-lookup"><span data-stu-id="bfb45-318">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="bfb45-319">CreateDesktopShortcut</span><span class="sxs-lookup"><span data-stu-id="bfb45-319">CreateDesktopShortcut</span></span>
#### <span data-ttu-id="bfb45-320">GP-Name: Erstellen von Desktopverknüpfungen bei Standardinstallation</span><span class="sxs-lookup"><span data-stu-id="bfb45-320">Prevent Desktop Shortcut creation upon install</span></span>
><span data-ttu-id="bfb45-321">Microsoft Edge Update 1.3.128.0 und höher</span><span class="sxs-lookup"><span data-stu-id="bfb45-321">Microsoft Edge Update 1.3.128.0 and later</span></span>

#### <span data-ttu-id="bfb45-322">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bfb45-322">Description</span></span>
<span data-ttu-id="bfb45-323">Wenn Sie diese Richtlinie aktivieren, wird beim Installieren von Microsoft Edge eine Desktopverknüpfung erstellt.</span><span class="sxs-lookup"><span data-stu-id="bfb45-323">If you enable this policy a desktop shortcut is created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="bfb45-324">Wenn Sie diese Richtlinie deaktivieren, wird beim Installieren von Microsoft Edge keine Desktopverknüpfung erstellt.</span><span class="sxs-lookup"><span data-stu-id="bfb45-324">If you disable this policy, no desktop shortcut will be created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="bfb45-325">Wenn Sie diese Richtlinie nicht konfigurieren, wird während der Installation eine Desktopverknüpfung zu Microsoft Edge erstellt.</span><span class="sxs-lookup"><span data-stu-id="bfb45-325">If you don’t configure this policy a desktop shortcut to Microsoft Edge will be created during installation.</span></span>
<span data-ttu-id="bfb45-326">Wenn Microsoft Edge bereits installiert ist, hat diese Richtlinie keine Auswirkung.</span><span class="sxs-lookup"><span data-stu-id="bfb45-326">If Microsoft Edge is already installed, this policy will have no effect.</span></span>

  <span data-ttu-id="bfb45-327">Wenn Sie diese Richtlinie für einen Kanal nicht konfigurieren, bestimmt die Richtlinienkonfiguration "[Standardeinstellung für das Verhindern der Erstellung von Desktopverknüpfungen bei der Installation](#createdesktopshortcutdefault)", ob bei Installation von Microsoft Edge eine Verknüpfung erstellt wird oder nicht.</span><span class="sxs-lookup"><span data-stu-id="bfb45-327">If you don't configure this policy for a channel, the '[Prevent Desktop Shortcut creation upon install default](#createdesktopshortcutdefault)' policy configuration determines shortcut creation when Microsoft Edge is installed.</span></span>
#### <span data-ttu-id="bfb45-328">Windows-Informationen und -Einstellungen</span><span class="sxs-lookup"><span data-stu-id="bfb45-328">Windows information and settings</span></span>
##### <span data-ttu-id="bfb45-329">Informationen zur Gruppenrichtlinie (ADMX)</span><span class="sxs-lookup"><span data-stu-id="bfb45-329">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="bfb45-330">Eindeutiger Name der GP: CreateDesktopShortcut</span><span class="sxs-lookup"><span data-stu-id="bfb45-330">GP unique name: CreateDesktopShortcut</span></span>
- <span data-ttu-id="bfb45-331">GP-Name: Erstellen von Desktopverknüpfungen bei Installation verhindern</span><span class="sxs-lookup"><span data-stu-id="bfb45-331">GP name: Prevent Desktop Shortcut creation upon install</span></span>
- <span data-ttu-id="bfb45-332">GP-Pfad:</span><span class="sxs-lookup"><span data-stu-id="bfb45-332">GP path:</span></span> 
  - <span data-ttu-id="bfb45-333">Administrative Vorlagen/Microsoft Edge Update/Anwendungen/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="bfb45-333">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="bfb45-334">Administrative Vorlagen/Microsoft Edge Update/Anwendungen/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="bfb45-334">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="bfb45-335">Administrative Vorlagen/Microsoft Edge Update/Anwendungen/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="bfb45-335">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="bfb45-336">Administrative Vorlagen/Microsoft Edge Update/Anwendungen/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="bfb45-336">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="bfb45-337">Name der GP-ADMX-Datei: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="bfb45-337">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="bfb45-338">Windows-Registrierungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="bfb45-338">Windows Registry Settings</span></span>
- <span data-ttu-id="bfb45-339">Pfad: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="bfb45-339">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="bfb45-340">Name des Wertes:</span><span class="sxs-lookup"><span data-stu-id="bfb45-340">Value Name:</span></span> 
  - <span data-ttu-id="bfb45-341">(Stable): CreateDesktopShortcut{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="bfb45-341">(Stable): CreateDesktopShortcut{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="bfb45-342">(Beta): CreateDesktopShortcut{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="bfb45-342">(Beta): CreateDesktopShortcut{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="bfb45-343">(Canary): CreateDesktopShortcut{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="bfb45-343">(Canary): CreateDesktopShortcut{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="bfb45-344">(Dev): CreateDesktopShortcut{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="bfb45-344">(Dev): CreateDesktopShortcut{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="bfb45-345">Werttyp: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="bfb45-345">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="bfb45-346">Beispielwert:</span><span class="sxs-lookup"><span data-stu-id="bfb45-346">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="bfb45-347">Zurück zum Anfang</span><span class="sxs-lookup"><span data-stu-id="bfb45-347">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="bfb45-348">RollbackToTargetVersion</span><span class="sxs-lookup"><span data-stu-id="bfb45-348">RollbackToTargetVersion</span></span>
#### <span data-ttu-id="bfb45-349">Zurücksetzung auf Zielversion</span><span class="sxs-lookup"><span data-stu-id="bfb45-349">Rollback to Target version</span></span>
><span data-ttu-id="bfb45-350">Microsoft Edge Update 1.3.133.3 und höher</span><span class="sxs-lookup"><span data-stu-id="bfb45-350">Microsoft Edge Update 1.3.133.3 and later</span></span>

#### <span data-ttu-id="bfb45-351">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bfb45-351">Description</span></span>
<span data-ttu-id="bfb45-352">Gibt an, dass Microsoft Edge Update Installationen von Microsoft Edge auf die in "[Zielversionaußerkraftsetzung](#targetversionprefix)" angegebene Version zurücksetzen soll.</span><span class="sxs-lookup"><span data-stu-id="bfb45-352">Specifies that Microsoft Edge Update should rollback installations of Microsoft Edge to the version indicated in '[Target version override](#targetversionprefix)'.</span></span>

<span data-ttu-id="bfb45-353">Diese Richtlinie hat keine Wirkung, es sei denn, "[Zielversionaußerkraftsetzung](#targetversionprefix)" ist festgelegt und "[Update-Richtlinie außer Kraft setzen](#update)" auf einen der Zustände "ein" festgelegt ist (Updates immer zulassen, Nur automatische unbeaufsichtigte Updates, Nur manuelle Updates).</span><span class="sxs-lookup"><span data-stu-id="bfb45-353">This policy has no effect unless '[Target version override](#targetversionprefix)' is set and '[Update policy override](#update)' is set to one of the ON states (Always allow updates, Automatic silent updates only, Manual updates only).</span></span>

<span data-ttu-id="bfb45-354">Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, bleiben Installationen mit einer höheren Version als die von "[Zielversionaußerkraftsetzung](#targetversionprefix)" unverändert.</span><span class="sxs-lookup"><span data-stu-id="bfb45-354">If you disable this policy or don't configure it, installs that have a version higher than that specified by '[Target version override](#targetversionprefix)' will be left as-is.</span></span>

<span data-ttu-id="bfb45-355">Wenn Sie diese Richtlinie aktivieren, werden Installationen mit einer aktuellen Version, die höher ist als durch "[Zielversionaußerkraftsetzung](#targetversionprefix)" angegeben, auf die Zielversion herabgestuft.</span><span class="sxs-lookup"><span data-stu-id="bfb45-355">If you enable this policy, installs that have a current version higher than specified by the '[Target version override](#targetversionprefix)' will be downgraded to the target version.</span></span>

<span data-ttu-id="bfb45-356">Wir empfehlen Benutzern, die neueste Version des Microsoft Edge-Browsers zu installieren, um den Schutz durch die neuesten Sicherheitsupdates zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="bfb45-356">We recommend that users install the latest version of the Microsoft Edge browser to ensure protection by the latest security updates.</span></span> <span data-ttu-id="bfb45-357">Ein Rollback zu einer früheren Version birgt Risiken, die mit bekannten Sicherheitsproblemen zu tun haben.</span><span class="sxs-lookup"><span data-stu-id="bfb45-357">Rollback to an earlier version risks exposure to known security issues.</span></span> <span data-ttu-id="bfb45-358">Diese Richtlinie ist als vorübergehender Fix zur Behebung von Problemen in einem Microsoft Edge-Browser-Update vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="bfb45-358">This policy is meant to be used as a temporary fix to address issues in a Microsoft Edge browser update.</span></span>

<span data-ttu-id="bfb45-359">Bevor Sie die Browserversion vorübergehend zurücksetzen, empfehlen wir, die Synchronisierung ([https://go.microsoft.com/fwlink/?linkid=2133032](https://go.microsoft.com/fwlink/?linkid=2133032)) für alle Benutzer in Ihrer Organisation zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="bfb45-359">Before temporarily rolling back your browser version, we recommend that you turn on Sync ([https://go.microsoft.com/fwlink/?linkid=2133032](https://go.microsoft.com/fwlink/?linkid=2133032)) for all users in your organization.</span></span> <span data-ttu-id="bfb45-360">Wenn Sie die Synchronisierung nicht aktivieren, besteht das Risiko eines endgültigen Verlusts von Browserdaten.</span><span class="sxs-lookup"><span data-stu-id="bfb45-360">If you don't turn on Sync, there is a risk of permanent browsing data loss.</span></span> <span data-ttu-id="bfb45-361">Verwenden Sie diese Richtlinie auf eigenes Risiko.</span><span class="sxs-lookup"><span data-stu-id="bfb45-361">Use this policy at your own risk.</span></span>

<span data-ttu-id="bfb45-362">Hinweis: alle Versionen, die für einen Rollback verfügbar sind, können Sie hier [https://aka.ms/EdgeEnterprise](https://aka.ms/EdgeEnterprise) anzeigen.</span><span class="sxs-lookup"><span data-stu-id="bfb45-362">Note: All versions available for rollback can be viewed here [https://aka.ms/EdgeEnterprise](https://aka.ms/EdgeEnterprise).</span></span>

<span data-ttu-id="bfb45-363">Diese Richtlinie bezieht sich auf Microsoft Edge Version 86 oder neuer.</span><span class="sxs-lookup"><span data-stu-id="bfb45-363">This policy applies to Microsoft Edge version 86 or later.</span></span>

<span data-ttu-id="bfb45-364">Weitere Informationen finden Sie unter [https://go.microsoft.com/fwlink/?linkid=2133918](https://go.microsoft.com/fwlink/?linkid=2133918).</span><span class="sxs-lookup"><span data-stu-id="bfb45-364">See [https://go.microsoft.com/fwlink/?linkid=2133918](https://go.microsoft.com/fwlink/?linkid=2133918) for more information.</span></span>

<span data-ttu-id="bfb45-365">Diese Richtlinie ist nur für Windows-Instanzen verfügbar, die in eine Microsoft® Active Directory®-Domäne eingebunden werden.</span><span class="sxs-lookup"><span data-stu-id="bfb45-365">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <span data-ttu-id="bfb45-366">Windows-Informationen und -Einstellungen</span><span class="sxs-lookup"><span data-stu-id="bfb45-366">Windows information and settings</span></span>
##### <span data-ttu-id="bfb45-367">Informationen zur Gruppenrichtlinie (ADMX)</span><span class="sxs-lookup"><span data-stu-id="bfb45-367">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="bfb45-368">Eindeutiger Name der GP: RollbackToTargetVersion</span><span class="sxs-lookup"><span data-stu-id="bfb45-368">GP unique name: RollbackToTargetVersion</span></span>
- <span data-ttu-id="bfb45-369">Name der GP: Zurücksetzung auf Zielversion</span><span class="sxs-lookup"><span data-stu-id="bfb45-369">GP name: Rollback to Target version</span></span>
- <span data-ttu-id="bfb45-370">GP-Pfad:</span><span class="sxs-lookup"><span data-stu-id="bfb45-370">GP path:</span></span> 
  - <span data-ttu-id="bfb45-371">Administrative Vorlagen/Microsoft Edge Update/Anwendungen/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="bfb45-371">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="bfb45-372">Administrative Vorlagen/Microsoft Edge Update/Anwendungen/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="bfb45-372">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="bfb45-373">Administrative Vorlagen/Microsoft Edge Update/Anwendungen/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="bfb45-373">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="bfb45-374">Administrative Vorlagen/Microsoft Edge Update/Anwendungen/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="bfb45-374">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="bfb45-375">Name der GP-ADMX-Datei: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="bfb45-375">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="bfb45-376">Windows-Registrierungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="bfb45-376">Windows Registry Settings</span></span>
- <span data-ttu-id="bfb45-377">Pfad: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="bfb45-377">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="bfb45-378">Name des Wertes:</span><span class="sxs-lookup"><span data-stu-id="bfb45-378">Value Name:</span></span> 
  - <span data-ttu-id="bfb45-379">(Stable): RollbackToTargetVersion{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="bfb45-379">(Stable): RollbackToTargetVersion{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="bfb45-380">(Beta): RollbackToTargetVersion{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="bfb45-380">(Beta): RollbackToTargetVersion{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="bfb45-381">(Canary): RollbackToTargetVersion{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="bfb45-381">(Canary): RollbackToTargetVersion{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="bfb45-382">(Dev): RollbackToTargetVersion{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="bfb45-382">(Dev): RollbackToTargetVersion{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="bfb45-383">Werttyp: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="bfb45-383">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="bfb45-384">Beispielwert:</span><span class="sxs-lookup"><span data-stu-id="bfb45-384">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="bfb45-385">Zurück zum Anfang</span><span class="sxs-lookup"><span data-stu-id="bfb45-385">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="bfb45-386">TargetVersionPrefix</span><span class="sxs-lookup"><span data-stu-id="bfb45-386">TargetVersionPrefix</span></span>
#### <span data-ttu-id="bfb45-387">Zielversion außer Kraft setzen</span><span class="sxs-lookup"><span data-stu-id="bfb45-387">Target version override</span></span>
><span data-ttu-id="bfb45-388">Microsoft Edge Update 1.3.119.43 und höher</span><span class="sxs-lookup"><span data-stu-id="bfb45-388">Microsoft Edge Update 1.3.119.43 and later</span></span>

#### <span data-ttu-id="bfb45-389">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bfb45-389">Description</span></span>
<span data-ttu-id="bfb45-390">Wenn diese Richtlinie und die automatische Aktualisierung aktiviert sind, wird Microsoft Edge auf die durch diesen Richtlinienwert angegebene Version aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="bfb45-390">When this policy is enabled, and auto-update is enabled, Microsoft Edge will be updated to the version specified by this policy value.</span></span>

<span data-ttu-id="bfb45-391">Der Richtlinienwert muss eine bestimmte Microsoft Edge-Version sein, z. B. 83.0.499.12.</span><span class="sxs-lookup"><span data-stu-id="bfb45-391">The policy value must be a specific Microsoft Edge version, e.g. 83.0.499.12.</span></span>

<span data-ttu-id="bfb45-392">Wenn ein Gerät über eine neuere Version von Microsoft Edge als der angegebene Wert verfügt, bleibt Microsoft Edge bei der neueren Version und wird nicht auf die angegebene Version herabgestuft.</span><span class="sxs-lookup"><span data-stu-id="bfb45-392">If a device has newer version of Microsoft Edge than the value specified, Microsoft Edge will remain on the newer version and not downgrade to the specified version.</span></span>

<span data-ttu-id="bfb45-393">Wenn die angegebene Version nicht vorhanden oder nicht ordnungsgemäß formatiert ist, bleibt Microsoft Edge bei der aktuellen Version und wird nicht automatisch auf zukünftige Versionen aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="bfb45-393">If the specified version does not exist, or is improperly formatted, then Microsoft Edge will remain on its current version and not update to future versions automatically.</span></span>

<span data-ttu-id="bfb45-394">Weitere Informationen finden Sie unter [https://go.microsoft.com/fwlink/?linkid=2136707](https://go.microsoft.com/fwlink/?linkid=2136707).</span><span class="sxs-lookup"><span data-stu-id="bfb45-394">See [https://go.microsoft.com/fwlink/?linkid=2136707](https://go.microsoft.com/fwlink/?linkid=2136707) for more information.</span></span>

<span data-ttu-id="bfb45-395">Diese Richtlinie ist nur für Windows-Instanzen verfügbar, die in eine Microsoft® Active Directory®-Domäne eingebunden werden.</span><span class="sxs-lookup"><span data-stu-id="bfb45-395">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <span data-ttu-id="bfb45-396">Windows-Informationen und -Einstellungen</span><span class="sxs-lookup"><span data-stu-id="bfb45-396">Windows information and settings</span></span>
##### <span data-ttu-id="bfb45-397">Informationen zur Gruppenrichtlinie (ADMX)</span><span class="sxs-lookup"><span data-stu-id="bfb45-397">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="bfb45-398">Eindeutiger Name der GP: TargetVersionPrefix</span><span class="sxs-lookup"><span data-stu-id="bfb45-398">GP unique name: TargetVersionPrefix</span></span>
- <span data-ttu-id="bfb45-399">GP-Name: Zielversion außer Kraft setzen</span><span class="sxs-lookup"><span data-stu-id="bfb45-399">GP name: Target version override</span></span>
- <span data-ttu-id="bfb45-400">GP-Pfad:</span><span class="sxs-lookup"><span data-stu-id="bfb45-400">GP path:</span></span> 
  - <span data-ttu-id="bfb45-401">Administrative Vorlagen/Microsoft Edge Update/Anwendungen/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="bfb45-401">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="bfb45-402">Administrative Vorlagen/Microsoft Edge Update/Anwendungen/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="bfb45-402">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="bfb45-403">Administrative Vorlagen/Microsoft Edge Update/Anwendungen/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="bfb45-403">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="bfb45-404">Administrative Vorlagen/Microsoft Edge Update/Anwendungen/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="bfb45-404">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="bfb45-405">Name der GP-ADMX-Datei: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="bfb45-405">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="bfb45-406">Windows-Registrierungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="bfb45-406">Windows Registry Settings</span></span>
- <span data-ttu-id="bfb45-407">Pfad: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="bfb45-407">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="bfb45-408">Name des Wertes:</span><span class="sxs-lookup"><span data-stu-id="bfb45-408">Value Name:</span></span> 
  - <span data-ttu-id="bfb45-409">(Stable): TargetVersionPrefix{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="bfb45-409">(Stable): TargetVersionPrefix{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="bfb45-410">(Beta): TargetVersionPrefix{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="bfb45-410">(Beta): TargetVersionPrefix{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="bfb45-411">(Canary): TargetVersionPrefix{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="bfb45-411">(Canary): TargetVersionPrefix{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="bfb45-412">(Dev): TargetVersionPrefix{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="bfb45-412">(Dev): TargetVersionPrefix{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="bfb45-413">Werttyp: REG_SZ</span><span class="sxs-lookup"><span data-stu-id="bfb45-413">Value Type: REG_SZ</span></span>
##### <span data-ttu-id="bfb45-414">Beispielwert:</span><span class="sxs-lookup"><span data-stu-id="bfb45-414">Example value:</span></span>
```
83.0.499.12
```
[<span data-ttu-id="bfb45-415">Zurück zum Anfang</span><span class="sxs-lookup"><span data-stu-id="bfb45-415">Back to top</span></span>](#microsoft-edge---update-policies)


## <span data-ttu-id="bfb45-416">Einstellungsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="bfb45-416">Preferences policies</span></span>

[<span data-ttu-id="bfb45-417">Zurück zum Anfang</span><span class="sxs-lookup"><span data-stu-id="bfb45-417">Back to top</span></span>](#microsoft-edge---update-policies)
### <span data-ttu-id="bfb45-418">AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="bfb45-418">AutoUpdateCheckPeriodMinutes</span></span>
#### <span data-ttu-id="bfb45-419">Überschreibung des Überprüfungszeitraums für automatische Updates</span><span class="sxs-lookup"><span data-stu-id="bfb45-419">Auto-update check period override</span></span>
><span data-ttu-id="bfb45-420">Microsoft Edge Update 1.2.145.5 und höher</span><span class="sxs-lookup"><span data-stu-id="bfb45-420">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="bfb45-421">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bfb45-421">Description</span></span>
<span data-ttu-id="bfb45-422">Wenn diese Richtlinie aktiviert ist, können Sie einen Wert für die Mindestanzahl von Minuten zwischen automatischen Updateprüfungen festlegen.</span><span class="sxs-lookup"><span data-stu-id="bfb45-422">If enabled, this policy lets you set a value for the minimum number of minutes between automatic update checks.</span></span> <span data-ttu-id="bfb45-423">Andernfalls sucht die automatische Updateprüfung standardmäßig alle 10 Stunden nach Updates.</span><span class="sxs-lookup"><span data-stu-id="bfb45-423">Otherwise, by default, auto-update checks for updates every 10 hours.</span></span>

  <span data-ttu-id="bfb45-424">Wenn Sie alle automatischen Updateprüfungen deaktivieren möchten, setzen Sie den Wert auf 0 (nicht empfohlen).</span><span class="sxs-lookup"><span data-stu-id="bfb45-424">If you want to disable all auto-update checks, set the value to 0 (not recommended).</span></span>
#### <span data-ttu-id="bfb45-425">Windows-Informationen und -Einstellungen</span><span class="sxs-lookup"><span data-stu-id="bfb45-425">Windows information and settings</span></span>
##### <span data-ttu-id="bfb45-426">Informationen zur Gruppenrichtlinie (ADMX)</span><span class="sxs-lookup"><span data-stu-id="bfb45-426">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="bfb45-427">Eindeutiger Name der GP: AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="bfb45-427">GP unique name: AutoUpdateCheckPeriodMinutes</span></span>
- <span data-ttu-id="bfb45-428">GP-Name: Überschreibung des Überprüfungszeitraums für automatische Updates</span><span class="sxs-lookup"><span data-stu-id="bfb45-428">GP name: Auto-update check period override</span></span>
- <span data-ttu-id="bfb45-429">GP-Pfad: Administrative Vorlagen/Microsoft Edge Update/Einstellungen</span><span class="sxs-lookup"><span data-stu-id="bfb45-429">GP path: Administrative Templates/Microsoft Edge Update/Preferences</span></span>
- <span data-ttu-id="bfb45-430">Name der GP-ADMX-Datei: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="bfb45-430">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="bfb45-431">Windows-Registrierungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="bfb45-431">Windows Registry Settings</span></span>
- <span data-ttu-id="bfb45-432">Pfad: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="bfb45-432">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="bfb45-433">Name des Wertes: AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="bfb45-433">Value Name: AutoUpdateCheckPeriodMinutes</span></span>
- <span data-ttu-id="bfb45-434">Werttyp: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="bfb45-434">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="bfb45-435">Beispielwert:</span><span class="sxs-lookup"><span data-stu-id="bfb45-435">Example value:</span></span>
```
0x00000578
```
[<span data-ttu-id="bfb45-436">Zurück zum Anfang</span><span class="sxs-lookup"><span data-stu-id="bfb45-436">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="bfb45-437">UpdatesSuppressed</span><span class="sxs-lookup"><span data-stu-id="bfb45-437">UpdatesSuppressed</span></span>
#### <span data-ttu-id="bfb45-438">Zeitraum in jedem Tag zum Unterdrücken der automatischen Überprüfung auf Updates</span><span class="sxs-lookup"><span data-stu-id="bfb45-438">Time period in each day to suppress auto-update check</span></span>
><span data-ttu-id="bfb45-439">Microsoft Edge Update 1.3.33.5 und höher</span><span class="sxs-lookup"><span data-stu-id="bfb45-439">Microsoft Edge Update 1.3.33.5 and later</span></span>

#### <span data-ttu-id="bfb45-440">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bfb45-440">Description</span></span>
<span data-ttu-id="bfb45-441">Wenn Sie diese Richtlinie aktivieren, werden die Updateprüfungen jeden Tag ab Stunde:Minute für einen Zeitraum der Dauer (in Minuten) unterdrückt.</span><span class="sxs-lookup"><span data-stu-id="bfb45-441">If you enable this policy, update checks are suppressed each day starting at Hour:Minute for a period of Duration (in minutes).</span></span> <span data-ttu-id="bfb45-442">Die Dauer ist von der Sommerzeit nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="bfb45-442">Duration isn't affected by daylight saving time.</span></span> <span data-ttu-id="bfb45-443">Wenn die Startzeit z.B. 22:00 lautet und die Dauer 480Minuten beträgt, werden Updates genau 8 Stunden lang unterdrückt, unabhängig davon, ob die Sommerzeit in diesem Zeitraum beginnt oder endet.</span><span class="sxs-lookup"><span data-stu-id="bfb45-443">For example, if the start time is 22:00 and the duration is 480 minutes, updates will be suppressed for exactly 8 hours, regardless of whether daylight saving time starts or ends during this period.</span></span>

  <span data-ttu-id="bfb45-444">Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, werden die Updateprüfungen während eines bestimmten Zeitraums nicht unterdrückt.</span><span class="sxs-lookup"><span data-stu-id="bfb45-444">If you disable or don't configure this policy, update checks aren't suppressed during any specific period.</span></span>
#### <span data-ttu-id="bfb45-445">Windows-Informationen und -Einstellungen</span><span class="sxs-lookup"><span data-stu-id="bfb45-445">Windows information and settings</span></span>
##### <span data-ttu-id="bfb45-446">Informationen zur Gruppenrichtlinie (ADMX)</span><span class="sxs-lookup"><span data-stu-id="bfb45-446">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="bfb45-447">Eindeutiger Name der GP: UpdatesSuppressed</span><span class="sxs-lookup"><span data-stu-id="bfb45-447">GP unique name: UpdatesSuppressed</span></span>
- <span data-ttu-id="bfb45-448">GP-Name: Zeitraum in jedem Tag zum Unterdrücken der automatischen Überprüfung auf Updates</span><span class="sxs-lookup"><span data-stu-id="bfb45-448">GP name: Time period in each day to suppress auto-update check</span></span>
  - <span data-ttu-id="bfb45-449">Optionen {Stunde, Minute, Dauer}</span><span class="sxs-lookup"><span data-stu-id="bfb45-449">Options { Hour, Minute, Duration }</span></span>
- <span data-ttu-id="bfb45-450">GP-Pfad: Administrative Vorlagen/Microsoft Edge Update/Einstellungen</span><span class="sxs-lookup"><span data-stu-id="bfb45-450">GP path: Administrative Templates/Microsoft Edge Update/Preferences</span></span>
- <span data-ttu-id="bfb45-451">Name der GP-ADMX-Datei: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="bfb45-451">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="bfb45-452">Windows-Registrierungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="bfb45-452">Windows Registry Settings</span></span>
- <span data-ttu-id="bfb45-453">Pfad: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="bfb45-453">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="bfb45-454">Name des Wertes:</span><span class="sxs-lookup"><span data-stu-id="bfb45-454">Value Name:</span></span> 
  - <span data-ttu-id="bfb45-455">UpdatesSuppressedDurationMin</span><span class="sxs-lookup"><span data-stu-id="bfb45-455">UpdatesSuppressedDurationMin</span></span>
  - <span data-ttu-id="bfb45-456">UpdatesSuppressedStartHour</span><span class="sxs-lookup"><span data-stu-id="bfb45-456">UpdatesSuppressedStartHour</span></span>
  - <span data-ttu-id="bfb45-457">UpdatesSuppressedStartMin</span><span class="sxs-lookup"><span data-stu-id="bfb45-457">UpdatesSuppressedStartMin</span></span>
- <span data-ttu-id="bfb45-458">Werttyp: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="bfb45-458">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="bfb45-459">Beispielwert:</span><span class="sxs-lookup"><span data-stu-id="bfb45-459">Example value:</span></span>
```
duration   : 0x0000003c
start hour : 0x00000001
start min  : 0x00000002
```
[<span data-ttu-id="bfb45-460">Zurück zum Anfang</span><span class="sxs-lookup"><span data-stu-id="bfb45-460">Back to top</span></span>](#microsoft-edge---update-policies)


## <span data-ttu-id="bfb45-461">Proxyserver-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="bfb45-461">Proxy Server policies</span></span>

[<span data-ttu-id="bfb45-462">Zurück zum Anfang</span><span class="sxs-lookup"><span data-stu-id="bfb45-462">Back to top</span></span>](#microsoft-edge---update-policies)
### <span data-ttu-id="bfb45-463">ProxyMode</span><span class="sxs-lookup"><span data-stu-id="bfb45-463">ProxyMode</span></span>
#### <span data-ttu-id="bfb45-464">Möglichkeit zur Angabe der Proxyservereinstellungen wählen</span><span class="sxs-lookup"><span data-stu-id="bfb45-464">Choose how to specify proxy server settings</span></span>
><span data-ttu-id="bfb45-465">Microsoft Edge Update 1.3.21.81 und höher</span><span class="sxs-lookup"><span data-stu-id="bfb45-465">Microsoft Edge Update 1.3.21.81 and later</span></span>

#### <span data-ttu-id="bfb45-466">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bfb45-466">Description</span></span>
<span data-ttu-id="bfb45-467">Mit dieser Option können Sie die Proxyserver-Einstellungen angeben, die von Microsoft Edge Update verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bfb45-467">Allows you to specify the proxy server settings that are used by Microsoft Edge Update.</span></span>

  <span data-ttu-id="bfb45-468">Wenn Sie diese Richtlinie aktivieren, können Sie zwischen den folgenden Proxyserveroptionen wählen:</span><span class="sxs-lookup"><span data-stu-id="bfb45-468">If you enable this policy, you can choose between the following proxy server options:</span></span>
   - <span data-ttu-id="bfb45-469">Wenn Sie niemals einen Proxyserver verwenden und immer eine direkte Verbindung herstellen, werden alle anderen Optionen ignoriert.</span><span class="sxs-lookup"><span data-stu-id="bfb45-469">If you choose to never use a proxy server and always connect directly, all other options are ignored.</span></span>
   - <span data-ttu-id="bfb45-470">Wenn Sie die System-Proxyeinstellungen verwenden oder den Proxyserver automatisch erkennen möchten, werden alle anderen Optionen ignoriert.</span><span class="sxs-lookup"><span data-stu-id="bfb45-470">If you choose to use system proxy settings or auto-detect the proxy server, all other options are ignored.</span></span>
   - <span data-ttu-id="bfb45-471">Wenn Sie den Proxymodus für feste Server auswählen, können Sie unter '[Adresse oder URL des Proxyservers](#proxyserver)' weitere Optionen angeben.</span><span class="sxs-lookup"><span data-stu-id="bfb45-471">If you choose fixed server proxy mode, you can specify further options in '[Address or URL of proxy server](#proxyserver)' policy.</span></span>
   - <span data-ttu-id="bfb45-472">Wenn Sie ein PAC-Proxyskript verwenden, müssen Sie die URL für das Skript unter '[URL zu einer PAC-Proxydatei](#proxypacurl)' angeben.</span><span class="sxs-lookup"><span data-stu-id="bfb45-472">If you choose to use a .pac proxy script, you must specify the URL for the script in '[URL to a proxy .pac file](#proxypacurl)' policy.</span></span>

  <span data-ttu-id="bfb45-473">Wenn Sie diese Richtlinie aktivieren, können Benutzer in Ihrer Organisation die Proxyeinstellungen in Microsoft Edge Update nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="bfb45-473">If you enable this policy, users in your organization can't change the proxy settings in Microsoft Edge Update.</span></span>

  <span data-ttu-id="bfb45-474">Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, werden keine Proxyservereinstellungen konfiguriert. Benutzer in Ihrer Organisation können jedoch ihre eigenen Proxyeinstellungen für Microsoft Edge Update auswählen.</span><span class="sxs-lookup"><span data-stu-id="bfb45-474">If you disable or don't configure this policy, no proxy server settings are configured, but users in your organization can choose their own proxy settings for Microsoft Edge Update.</span></span>
#### <span data-ttu-id="bfb45-475">Windows-Informationen und -Einstellungen</span><span class="sxs-lookup"><span data-stu-id="bfb45-475">Windows information and settings</span></span>
##### <span data-ttu-id="bfb45-476">Informationen zur Gruppenrichtlinie (ADMX)</span><span class="sxs-lookup"><span data-stu-id="bfb45-476">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="bfb45-477">Eindeutiger Name der GP: ProxyMode</span><span class="sxs-lookup"><span data-stu-id="bfb45-477">GP unique name: ProxyMode</span></span>
- <span data-ttu-id="bfb45-478">GP-Name: Möglichkeit zur Angabe der Proxyservereinstellungen wählen</span><span class="sxs-lookup"><span data-stu-id="bfb45-478">GP name: Choose how to specify proxy server settings</span></span>
- <span data-ttu-id="bfb45-479">GP-Pfad: Administrative Vorlagen/Microsoft Edge Update/Proxyserver</span><span class="sxs-lookup"><span data-stu-id="bfb45-479">GP path: Administrative Templates/Microsoft Edge Update/Proxy Server</span></span>
- <span data-ttu-id="bfb45-480">Name der GP-ADMX-Datei: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="bfb45-480">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="bfb45-481">Windows-Registrierungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="bfb45-481">Windows Registry Settings</span></span>
- <span data-ttu-id="bfb45-482">Pfad: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="bfb45-482">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="bfb45-483">Name des Wertes: ProxyMode</span><span class="sxs-lookup"><span data-stu-id="bfb45-483">Value Name: ProxyMode</span></span>
- <span data-ttu-id="bfb45-484">Werttyp: REG_SZ</span><span class="sxs-lookup"><span data-stu-id="bfb45-484">Value Type: REG_SZ</span></span>
##### <span data-ttu-id="bfb45-485">Beispielwert:</span><span class="sxs-lookup"><span data-stu-id="bfb45-485">Example value:</span></span>
```
fixed_servers
```
[<span data-ttu-id="bfb45-486">Zurück zum Anfang</span><span class="sxs-lookup"><span data-stu-id="bfb45-486">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="bfb45-487">ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="bfb45-487">ProxyPacUrl</span></span>
#### <span data-ttu-id="bfb45-488">URL zu einer PAC-Proxydatei</span><span class="sxs-lookup"><span data-stu-id="bfb45-488">URL to a proxy .pac file</span></span>
><span data-ttu-id="bfb45-489">Microsoft Edge Update 1.3.21.81 und höher</span><span class="sxs-lookup"><span data-stu-id="bfb45-489">Microsoft Edge Update 1.3.21.81 and later</span></span>

#### <span data-ttu-id="bfb45-490">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bfb45-490">Description</span></span>
<span data-ttu-id="bfb45-491">Ermöglicht die Angabe einer URL für eine PAC-Datei (Proxy Auto-Config).</span><span class="sxs-lookup"><span data-stu-id="bfb45-491">Allows you to specify a URL for a proxy auto-config (PAC) file.</span></span>

  <span data-ttu-id="bfb45-492">Wenn Sie diese Richtlinie aktivieren, können Sie eine URL für eine PAC-Datei angeben, um zu automatisieren, wie Microsoft Edge Update den geeigneten Proxyserver zum Abrufen einer bestimmten Website auswählt.</span><span class="sxs-lookup"><span data-stu-id="bfb45-492">If you enable this policy, you can specify a URL for a PAC file to automate how Microsoft Edge Update selects the appropriate proxy server for fetching a particular website.</span></span>

  <span data-ttu-id="bfb45-493">Diese Richtlinie wird nur angewendet, wenn Sie in der Richtlinie '[Möglichkeit zur Angabe der Proxyservereinstellungen wählen](#proxymode)' manuelle Proxyeinstellungen festgelegt haben.</span><span class="sxs-lookup"><span data-stu-id="bfb45-493">This policy is applied only if you have specified manual proxy settings in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>

  <span data-ttu-id="bfb45-494">Konfigurieren Sie diese Richtlinie nicht, wenn Sie eine andere Proxy-Einstellung als manuell in der Richtlinie '[Möglichkeit zur Angabe der Proxyservereinstellungen wählen](#proxymode)' ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="bfb45-494">Don't configure this policy if you have selected a proxy setting other than manual in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>
#### <span data-ttu-id="bfb45-495">Windows-Informationen und -Einstellungen</span><span class="sxs-lookup"><span data-stu-id="bfb45-495">Windows information and settings</span></span>
##### <span data-ttu-id="bfb45-496">Informationen zur Gruppenrichtlinie (ADMX)</span><span class="sxs-lookup"><span data-stu-id="bfb45-496">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="bfb45-497">Eindeutiger Name der GP: ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="bfb45-497">GP unique name: ProxyPacUrl</span></span>
- <span data-ttu-id="bfb45-498">GP-Name: URL zu einer PAC-Proxydatei</span><span class="sxs-lookup"><span data-stu-id="bfb45-498">GP name: URL to a proxy .pac file</span></span>
- <span data-ttu-id="bfb45-499">GP-Pfad: Administrative Vorlagen/Microsoft Edge Update/Proxyserver</span><span class="sxs-lookup"><span data-stu-id="bfb45-499">GP path: Administrative Templates/Microsoft Edge Update/Proxy Server</span></span>
- <span data-ttu-id="bfb45-500">Name der GP-ADMX-Datei: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="bfb45-500">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="bfb45-501">Windows-Registrierungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="bfb45-501">Windows Registry Settings</span></span>
- <span data-ttu-id="bfb45-502">Pfad: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="bfb45-502">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="bfb45-503">Name des Wertes: ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="bfb45-503">Value Name: ProxyPacUrl</span></span>
- <span data-ttu-id="bfb45-504">Werttyp: REG_SZ</span><span class="sxs-lookup"><span data-stu-id="bfb45-504">Value Type: REG_SZ</span></span>
##### <span data-ttu-id="bfb45-505">Beispielwert:</span><span class="sxs-lookup"><span data-stu-id="bfb45-505">Example value:</span></span>
```
https://www.microsoft.com
```
[<span data-ttu-id="bfb45-506">Zurück zum Anfang</span><span class="sxs-lookup"><span data-stu-id="bfb45-506">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="bfb45-507">ProxyServer</span><span class="sxs-lookup"><span data-stu-id="bfb45-507">ProxyServer</span></span>
#### <span data-ttu-id="bfb45-508">Adresse oder URL des Proxyservers</span><span class="sxs-lookup"><span data-stu-id="bfb45-508">Address or URL of proxy server</span></span>
><span data-ttu-id="bfb45-509">Microsoft Edge Update 1.3.21.81 und höher</span><span class="sxs-lookup"><span data-stu-id="bfb45-509">Microsoft Edge Update 1.3.21.81 and later</span></span>

#### <span data-ttu-id="bfb45-510">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bfb45-510">Description</span></span>
<span data-ttu-id="bfb45-511">Hier können Sie die URL des Proxy-Servers angeben, den Microsoft Edge Update verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="bfb45-511">Allows you to specify the URL of the proxy server for Microsoft Edge Update to use.</span></span>

  <span data-ttu-id="bfb45-512">Wenn Sie diese Richtlinie aktivieren, können Sie die Proxyserver-URL festlegen, die von Microsoft Edge Update in Ihrer Organisation verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bfb45-512">If you enable this policy, you can set the proxy server URL used by Microsoft Edge Update in your organization.</span></span>

  <span data-ttu-id="bfb45-513">Diese Richtlinie wird nur angewendet, wenn Sie in der Richtlinie '[Möglichkeit zur Angabe der Proxyservereinstellungen wählen](#proxymode)' manuelle Proxyeinstellungen ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="bfb45-513">This policy is applied only if you have selected manual proxy settings in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>

  <span data-ttu-id="bfb45-514">Konfigurieren Sie diese Richtlinie nicht, wenn Sie eine andere Proxy-Einstellung als manuell in der Richtlinie '[Möglichkeit zur Angabe der Proxyservereinstellungen wählen](#proxymode)' ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="bfb45-514">Don't configure this policy if you have selected a proxy setting other than manual in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>
#### <span data-ttu-id="bfb45-515">Windows-Informationen und -Einstellungen</span><span class="sxs-lookup"><span data-stu-id="bfb45-515">Windows information and settings</span></span>
##### <span data-ttu-id="bfb45-516">Informationen zur Gruppenrichtlinie (ADMX)</span><span class="sxs-lookup"><span data-stu-id="bfb45-516">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="bfb45-517">Eindeutiger Name der GP: ProxyServer</span><span class="sxs-lookup"><span data-stu-id="bfb45-517">GP unique name: ProxyServer</span></span>
- <span data-ttu-id="bfb45-518">GP-Name: Adresse oder URL des Proxyservers</span><span class="sxs-lookup"><span data-stu-id="bfb45-518">GP name: Address or URL of proxy server</span></span>
- <span data-ttu-id="bfb45-519">GP-Pfad: Administrative Vorlagen/Microsoft Edge Update/Proxyserver</span><span class="sxs-lookup"><span data-stu-id="bfb45-519">GP path: Administrative Templates/Microsoft Edge Update/Proxy Server</span></span>
- <span data-ttu-id="bfb45-520">Name der GP-ADMX-Datei: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="bfb45-520">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="bfb45-521">Windows-Registrierungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="bfb45-521">Windows Registry Settings</span></span>
- <span data-ttu-id="bfb45-522">Pfad: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="bfb45-522">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="bfb45-523">Name des Wertes: ProxyServer</span><span class="sxs-lookup"><span data-stu-id="bfb45-523">Value Name: ProxyServer</span></span>
- <span data-ttu-id="bfb45-524">Werttyp: REG_SZ</span><span class="sxs-lookup"><span data-stu-id="bfb45-524">Value Type: REG_SZ</span></span>
##### <span data-ttu-id="bfb45-525">Beispielwert:</span><span class="sxs-lookup"><span data-stu-id="bfb45-525">Example value:</span></span>
```
https://www.microsoft.com
```
[<span data-ttu-id="bfb45-526">Zurück zum Anfang</span><span class="sxs-lookup"><span data-stu-id="bfb45-526">Back to top</span></span>](#microsoft-edge---update-policies)


## <span data-ttu-id="bfb45-527">Microsoft Edge WebView-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="bfb45-527">Microsoft Edge WebView policies</span></span>

[<span data-ttu-id="bfb45-528">Zurück zum Anfang</span><span class="sxs-lookup"><span data-stu-id="bfb45-528">Back to top</span></span>](#microsoft-edge---update-policies)
### <span data-ttu-id="bfb45-529">Installieren (WebView)</span><span class="sxs-lookup"><span data-stu-id="bfb45-529">Install (WebView)</span></span>
#### <span data-ttu-id="bfb45-530">Installation zulassen</span><span class="sxs-lookup"><span data-stu-id="bfb45-530">Allow installation</span></span>
><span data-ttu-id="bfb45-531">Microsoft Edge Update 1.3.127.1 und höher</span><span class="sxs-lookup"><span data-stu-id="bfb45-531">Microsoft Edge Update 1.3.127.1 and later</span></span>

#### <span data-ttu-id="bfb45-532">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bfb45-532">Description</span></span>
<span data-ttu-id="bfb45-533">Hiermit können Sie festlegen, ob Microsoft Edge WebView mithilfe von Microsoft Edge Update installiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="bfb45-533">Lets you specify whether Microsoft Edge WebView can be installed using Microsoft Edge Update.</span></span>

  - <span data-ttu-id="bfb45-534">Wenn Sie diese Richtlinie aktivieren, können Benutzer Microsoft Edge über Microsoft Edge Update installieren.</span><span class="sxs-lookup"><span data-stu-id="bfb45-534">If you enable this policy, users can install Microsoft Edge WebView through Microsoft Edge Update.</span></span>
  - <span data-ttu-id="bfb45-535">Wenn Sie diese Richtlinie deaktivieren, können Benutzer Microsoft Edge nicht über Microsoft Edge Update installieren.</span><span class="sxs-lookup"><span data-stu-id="bfb45-535">If you disable this policy, users cannot install Microsoft Edge WebView through Microsoft Edge Update.</span></span>
  - <span data-ttu-id="bfb45-536">Wenn Sie diese Richtlinie nicht konfigurieren, bestimmt die Richtlinienkonfiguration "[Standardinstallation zulassen](#installdefault)", ob Benutzer Microsoft Edge WebView über Microsoft Edge Update installieren können.</span><span class="sxs-lookup"><span data-stu-id="bfb45-536">If you don't configure this policy, the '[Allow installation default](#installdefault)' policy configuration determines whether users can install Microsoft Edge WebView through Microsoft Edge Update.</span></span>
#### <span data-ttu-id="bfb45-537">Windows-Informationen und -Einstellungen</span><span class="sxs-lookup"><span data-stu-id="bfb45-537">Windows information and settings</span></span>
##### <span data-ttu-id="bfb45-538">Informationen zur Gruppenrichtlinie (ADMX)</span><span class="sxs-lookup"><span data-stu-id="bfb45-538">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="bfb45-539">Eindeutiger Name der GP: Install</span><span class="sxs-lookup"><span data-stu-id="bfb45-539">GP unique name: Install</span></span>
- <span data-ttu-id="bfb45-540">GP-Name: Installation zulassen</span><span class="sxs-lookup"><span data-stu-id="bfb45-540">GP name: Allow installation</span></span>
- <span data-ttu-id="bfb45-541">GP-Pfad: Administrative Vorlagen/Microsoft Edge Update/Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="bfb45-541">GP path: Administrative Templates/Microsoft Edge Update/Microsoft Edge WebView</span></span>
- <span data-ttu-id="bfb45-542">Name der GP-ADMX-Datei: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="bfb45-542">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="bfb45-543">Windows-Registrierungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="bfb45-543">Windows Registry Settings</span></span>
- <span data-ttu-id="bfb45-544">Pfad: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="bfb45-544">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="bfb45-545">Name des Wertes:</span><span class="sxs-lookup"><span data-stu-id="bfb45-545">Value Name:</span></span> 
  - <span data-ttu-id="bfb45-546">Install{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}</span><span class="sxs-lookup"><span data-stu-id="bfb45-546">Install{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}</span></span>
- <span data-ttu-id="bfb45-547">Werttyp: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="bfb45-547">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="bfb45-548">Beispielwert:</span><span class="sxs-lookup"><span data-stu-id="bfb45-548">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="bfb45-549">Zurück zum Anfang</span><span class="sxs-lookup"><span data-stu-id="bfb45-549">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="bfb45-550">Update (WebView)</span><span class="sxs-lookup"><span data-stu-id="bfb45-550">Update (WebView)</span></span>
#### <span data-ttu-id="bfb45-551">Außerkraftsetzung von Updaterichtlinien</span><span class="sxs-lookup"><span data-stu-id="bfb45-551">Update policy override</span></span>
><span data-ttu-id="bfb45-552">Microsoft Edge Update 1.3.127.1 und höher</span><span class="sxs-lookup"><span data-stu-id="bfb45-552">Microsoft Edge Update 1.3.127.1 and later</span></span>

#### <span data-ttu-id="bfb45-553">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bfb45-553">Description</span></span>
<span data-ttu-id="bfb45-554">Sie können angeben, ob automatische Updates für Microsoft Edge WebView aktiviert sind oder nicht.</span><span class="sxs-lookup"><span data-stu-id="bfb45-554">Lets you specify whether or not automatic updates are enabled for Microsoft Edge WebView.</span></span> <span data-ttu-id="bfb45-555">Microsoft Edge WebView ist eine Komponente, die von Anwendungen zum Anzeigen von Webinhalten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bfb45-555">Microsoft Edge WebView is a component used by applications to display web content.</span></span>
<span data-ttu-id="bfb45-556">"Automatische Updates" ist standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="bfb45-556">Automatic updates are enabled by default.</span></span> <span data-ttu-id="bfb45-557">Durch das Deaktivieren von automatischen Updates für Microsoft Edge WebView können Kompatibilitätsprobleme mit Anwendungen verursacht werden, die von dieser Komponente abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="bfb45-557">Disabling automatic updates for Microsoft Edge WebView might cause compatibility issues with applications that depend on this component.</span></span>

  <span data-ttu-id="bfb45-558">Wenn Sie diese Richtlinie aktivieren, verarbeitet Microsoft Edge Update die Microsoft Edge WebView-Updates entsprechend der Konfiguration der folgenden Optionen:</span><span class="sxs-lookup"><span data-stu-id="bfb45-558">If you enable this policy, Microsoft Edge Update handles Microsoft Edge WebView updates according to how you configure the following options:</span></span>
  - <span data-ttu-id="bfb45-559">Updates immer zulassen: Updates werden automatisch heruntergeladen und angewendet</span><span class="sxs-lookup"><span data-stu-id="bfb45-559">Always allow updates: Updates are automatically downloaded and applied</span></span>
  - <span data-ttu-id="bfb45-560">Updates deaktiviert: Updates werden nie heruntergeladen und angewendet</span><span class="sxs-lookup"><span data-stu-id="bfb45-560">Updates disabled: Updates are never downloaded or applied</span></span>

  <span data-ttu-id="bfb45-561">Wenn Sie diese Richtlinie nicht aktivieren, werden Updates automatisch heruntergeladen und angewendet.</span><span class="sxs-lookup"><span data-stu-id="bfb45-561">If you don't enable this policy, updates are automatically downloaded and applied.</span></span>
#### <span data-ttu-id="bfb45-562">Windows-Informationen und -Einstellungen</span><span class="sxs-lookup"><span data-stu-id="bfb45-562">Windows information and settings</span></span>
##### <span data-ttu-id="bfb45-563">Informationen zur Gruppenrichtlinie (ADMX)</span><span class="sxs-lookup"><span data-stu-id="bfb45-563">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="bfb45-564">Eindeutiger Name der GP: Update</span><span class="sxs-lookup"><span data-stu-id="bfb45-564">GP unique name: Update</span></span>
- <span data-ttu-id="bfb45-565">GP-Name: Außerkraftsetzung von Updaterichtlinien</span><span class="sxs-lookup"><span data-stu-id="bfb45-565">GP name: Update policy override</span></span>
- <span data-ttu-id="bfb45-566">GP-Pfad: Administrative Vorlagen/Microsoft Edge Update/Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="bfb45-566">GP path: Administrative Templates/Microsoft Edge Update/Microsoft Edge WebView</span></span>
- <span data-ttu-id="bfb45-567">Name der GP-ADMX-Datei: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="bfb45-567">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="bfb45-568">Windows-Registrierungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="bfb45-568">Windows Registry Settings</span></span>
- <span data-ttu-id="bfb45-569">Pfad: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="bfb45-569">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="bfb45-570">Name des Wertes:</span><span class="sxs-lookup"><span data-stu-id="bfb45-570">Value Name:</span></span> 
  - <span data-ttu-id="bfb45-571">Update{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}</span><span class="sxs-lookup"><span data-stu-id="bfb45-571">Update{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}</span></span>
- <span data-ttu-id="bfb45-572">Werttyp: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="bfb45-572">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="bfb45-573">Beispielwert:</span><span class="sxs-lookup"><span data-stu-id="bfb45-573">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="bfb45-574">Zurück zum Anfang</span><span class="sxs-lookup"><span data-stu-id="bfb45-574">Back to top</span></span>](#microsoft-edge---update-policies)


## <span data-ttu-id="bfb45-575">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="bfb45-575">See also</span></span>
  - [<span data-ttu-id="bfb45-576">Konfigurieren von Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="bfb45-576">Configuring Microsoft Edge</span></span>](configure-microsoft-edge.md)
  - [<span data-ttu-id="bfb45-577">Microsoft Edge Enterprise-Angebotsseite</span><span class="sxs-lookup"><span data-stu-id="bfb45-577">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)