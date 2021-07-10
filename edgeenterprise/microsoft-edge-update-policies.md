---
title: Dokumentation für die Microsoft Edge Update-Richtlinie
ms.author: stmoody
author: dan-wesley
manager: tahills
ms.date: 06/29/2021
audience: ITPro
ms.topic: reference
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
ms.custom: ''
description: Dokumentation für alle vom Microsoft Edge Updater unterstützten Richtlinien
ms.openlocfilehash: a9808981acad544042c6e0ccb59ff755a670c848
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "11642321"
---
# <a name="microsoft-edge---update-policies"></a><span data-ttu-id="d9dee-103">Microsoft Edge – Update-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="d9dee-103">Microsoft Edge - Update policies</span></span>

<span data-ttu-id="d9dee-104">Die neueste Version von Microsoft Edge enthält die folgenden Richtlinien, mit denen Sie steuern können, wie und wann Microsoft Edge aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="d9dee-104">The latest version of Microsoft Edge includes the following policies that you can use to control how and when Microsoft Edge is updated.</span></span>

<span data-ttu-id="d9dee-105">Weitere Informationen zu anderen in Microsoft Edge verfügbaren Richtlinien finden Sie in der [Microsoft Edge Referenz für Browserrichtlinien](microsoft-edge-policies.md)</span><span class="sxs-lookup"><span data-stu-id="d9dee-105">For information about other policies available in Microsoft Edge, check out [Microsoft Edge browser policy reference](microsoft-edge-policies.md)</span></span>
> [!NOTE]
> <span data-ttu-id="d9dee-106">Dieser Artikel bezieht sich auf Microsoft Edge Version 77 oder höher.</span><span class="sxs-lookup"><span data-stu-id="d9dee-106">This article applies to Microsoft Edge version 77 or later.</span></span>
## <a name="available-policies"></a><span data-ttu-id="d9dee-107">Verfügbare Richtlinien</span><span class="sxs-lookup"><span data-stu-id="d9dee-107">Available policies</span></span>
<span data-ttu-id="d9dee-108">In dieser Tabelle sind sämtliche, in dieser Version von Microsoft Edge verfügbaren Update-bezogenen Gruppenrichtlinien aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="d9dee-108">These tables lists all of the update-related group policies available in this release of Microsoft Edge.</span></span> <span data-ttu-id="d9dee-109">Über die Links in der folgenden Tabelle erhalten Sie weitere Einzelheiten zu bestimmten Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="d9dee-109">Use the links in the table to get more details about specific policies.</span></span>

<span data-ttu-id="d9dee-110">|&nbsp;|&nbsp;| |**-**|-| |**[Anwendungen](#applications)**|[Einstellungen](#preferences)| |**[Proxyserver](#proxy-server)**|[Microsoft Edge WebView](#microsoft-edge-webview)|</span><span class="sxs-lookup"><span data-stu-id="d9dee-110">|&nbsp;|&nbsp;| |**-**|-| |**[Applications](#applications)**|[Preferences](#preferences)| |**[Proxy Server](#proxy-server)**|[Microsoft Edge WebView](#microsoft-edge-webview)|</span></span>
### [<a name="applications"></a><span data-ttu-id="d9dee-111">Anwendungen</span><span class="sxs-lookup"><span data-stu-id="d9dee-111">Applications</span></span>](#applications-policies)
|<span data-ttu-id="d9dee-112">Richtlinienname</span><span class="sxs-lookup"><span data-stu-id="d9dee-112">Policy Name</span></span>|<span data-ttu-id="d9dee-113">Beschriftung</span><span class="sxs-lookup"><span data-stu-id="d9dee-113">Caption</span></span>|
|-|-|
|[<span data-ttu-id="d9dee-114">InstallDefault</span><span class="sxs-lookup"><span data-stu-id="d9dee-114">InstallDefault</span></span>](#installdefault)|<span data-ttu-id="d9dee-115">Standardinstallation zulassen</span><span class="sxs-lookup"><span data-stu-id="d9dee-115">Allow installation default</span></span>|
|[<span data-ttu-id="d9dee-116">UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="d9dee-116">UpdateDefault</span></span>](#updatedefault)|<span data-ttu-id="d9dee-117">Die Updaterichtlinie überschreibt die Standardrichtlinie</span><span class="sxs-lookup"><span data-stu-id="d9dee-117">Update policy override default</span></span>|
|[<span data-ttu-id="d9dee-118">Installieren</span><span class="sxs-lookup"><span data-stu-id="d9dee-118">Install</span></span>](#install)|<span data-ttu-id="d9dee-119">Installation zulassen (pro Kanal)</span><span class="sxs-lookup"><span data-stu-id="d9dee-119">Allow installation (per channel)</span></span>|
|[<span data-ttu-id="d9dee-120">Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="d9dee-120">Update</span></span>](#update)|<span data-ttu-id="d9dee-121">Außerkraftsetzung von Updaterichtlinien (pro Kanal)</span><span class="sxs-lookup"><span data-stu-id="d9dee-121">Update policy override (per channel)</span></span>|
|[<span data-ttu-id="d9dee-122">Allowsxs</span><span class="sxs-lookup"><span data-stu-id="d9dee-122">Allowsxs</span></span>](#allowsxs)|<span data-ttu-id="d9dee-123">Microsoft Edge Seite-an-Seite-Browserumgebung zulassen</span><span class="sxs-lookup"><span data-stu-id="d9dee-123">Allow Microsoft Edge Side by Side browser experience</span></span>|
|[<span data-ttu-id="d9dee-124">CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="d9dee-124">CreateDesktopShortcutDefault</span></span>](#createdesktopshortcutdefault)|<span data-ttu-id="d9dee-125">Standardeinstellung für das Verhindern der Erstellung von Desktopverknüpfungen bei der Installation</span><span class="sxs-lookup"><span data-stu-id="d9dee-125">Prevent Desktop Shortcut creation upon install default</span></span>|
|[<span data-ttu-id="d9dee-126">CreateDesktopShortcut</span><span class="sxs-lookup"><span data-stu-id="d9dee-126">CreateDesktopShortcut</span></span>](#createdesktopshortcut)|<span data-ttu-id="d9dee-127">Verhindern der Erstellung von Desktopverknüpfungen bei der Installation (pro Kanal)</span><span class="sxs-lookup"><span data-stu-id="d9dee-127">Prevent Desktop Shortcut creation upon install (per channel)</span></span>|
|[<span data-ttu-id="d9dee-128">RollbackToTargetVersion</span><span class="sxs-lookup"><span data-stu-id="d9dee-128">RollbackToTargetVersion</span></span>](#rollbacktotargetversion)|<span data-ttu-id="d9dee-129">Zurücksetzung auf Zielversion (pro Kanal)</span><span class="sxs-lookup"><span data-stu-id="d9dee-129">Rollback to Target version (per channel)</span></span>|
|[<span data-ttu-id="d9dee-130">TargetVersionPrefix</span><span class="sxs-lookup"><span data-stu-id="d9dee-130">TargetVersionPrefix</span></span>](#targetversionprefix)|<span data-ttu-id="d9dee-131">Außerkraftsetzung der Zielversion (pro Kanal)</span><span class="sxs-lookup"><span data-stu-id="d9dee-131">Target version override (per channel)</span></span>|

### [<a name="preferences"></a><span data-ttu-id="d9dee-132">Voreinstellungen</span><span class="sxs-lookup"><span data-stu-id="d9dee-132">Preferences</span></span>](#preferences-policies)
|<span data-ttu-id="d9dee-133">Richtlinienname</span><span class="sxs-lookup"><span data-stu-id="d9dee-133">Policy Name</span></span>|<span data-ttu-id="d9dee-134">Beschriftung</span><span class="sxs-lookup"><span data-stu-id="d9dee-134">Caption</span></span>|
|-|-|
|[<span data-ttu-id="d9dee-135">AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="d9dee-135">AutoUpdateCheckPeriodMinutes</span></span>](#autoupdatecheckperiodminutes)|<span data-ttu-id="d9dee-136">Überschreibung des Überprüfungszeitraums für automatische Updates</span><span class="sxs-lookup"><span data-stu-id="d9dee-136">Auto-update check period override</span></span>|
|[<span data-ttu-id="d9dee-137">UpdatesSuppressed</span><span class="sxs-lookup"><span data-stu-id="d9dee-137">UpdatesSuppressed</span></span>](#updatessuppressed)|<span data-ttu-id="d9dee-138">Zeitraum in jedem Tag zum Unterdrücken der automatischen Überprüfung auf Updates</span><span class="sxs-lookup"><span data-stu-id="d9dee-138">Time period in each day to suppress auto-update check</span></span>|

### [<a name="proxy-server"></a><span data-ttu-id="d9dee-139">Proxyserver</span><span class="sxs-lookup"><span data-stu-id="d9dee-139">Proxy Server</span></span>](#proxy-server-policies)
|<span data-ttu-id="d9dee-140">Richtlinienname</span><span class="sxs-lookup"><span data-stu-id="d9dee-140">Policy Name</span></span>|<span data-ttu-id="d9dee-141">Untertitel für Hörgeschädigte</span><span class="sxs-lookup"><span data-stu-id="d9dee-141">Caption</span></span>|
|-|-|
|[<span data-ttu-id="d9dee-142">ProxyMode</span><span class="sxs-lookup"><span data-stu-id="d9dee-142">ProxyMode</span></span>](#proxymode)|<span data-ttu-id="d9dee-143">Möglichkeit zur Angabe der Proxyservereinstellungen wählen</span><span class="sxs-lookup"><span data-stu-id="d9dee-143">Choose how to specify proxy server settings</span></span>|
|[<span data-ttu-id="d9dee-144">ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="d9dee-144">ProxyPacUrl</span></span>](#proxypacurl)|<span data-ttu-id="d9dee-145">URL zu einer PAC-Proxydatei</span><span class="sxs-lookup"><span data-stu-id="d9dee-145">URL to a proxy .pac file</span></span>|
|[<span data-ttu-id="d9dee-146">ProxyServer</span><span class="sxs-lookup"><span data-stu-id="d9dee-146">ProxyServer</span></span>](#proxyserver)|<span data-ttu-id="d9dee-147">Adresse oder URL des Proxyservers</span><span class="sxs-lookup"><span data-stu-id="d9dee-147">Address or URL of proxy server</span></span>|

### [<a name="microsoft-edge-webview"></a><span data-ttu-id="d9dee-148">Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="d9dee-148">Microsoft Edge WebView</span></span>](#microsoft-edge-webview-policies)
|<span data-ttu-id="d9dee-149">Richtlinienname</span><span class="sxs-lookup"><span data-stu-id="d9dee-149">Policy Name</span></span>|<span data-ttu-id="d9dee-150">Beschriftung</span><span class="sxs-lookup"><span data-stu-id="d9dee-150">Caption</span></span>|
|-|-|
|[<span data-ttu-id="d9dee-151">Installieren</span><span class="sxs-lookup"><span data-stu-id="d9dee-151">Install</span></span>](#install-webview)|<span data-ttu-id="d9dee-152">Installation zulassen</span><span class="sxs-lookup"><span data-stu-id="d9dee-152">Allow installation</span></span>|
|[<span data-ttu-id="d9dee-153">Update/Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="d9dee-153">Update</span></span>](#update-webview)|<span data-ttu-id="d9dee-154">Außerkraftsetzung von Updaterichtlinien</span><span class="sxs-lookup"><span data-stu-id="d9dee-154">Update policy override</span></span>|

## <a name="applications-policies"></a><span data-ttu-id="d9dee-155">Anwendungsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="d9dee-155">Applications policies</span></span>

[<span data-ttu-id="d9dee-156">Zurück zum Anfang</span><span class="sxs-lookup"><span data-stu-id="d9dee-156">Back to top</span></span>](#microsoft-edge---update-policies)
### <a name="installdefault"></a><span data-ttu-id="d9dee-157">InstallDefault</span><span class="sxs-lookup"><span data-stu-id="d9dee-157">InstallDefault</span></span>
#### <a name="allow-installation-default"></a><span data-ttu-id="d9dee-158">Standardinstallation zulassen</span><span class="sxs-lookup"><span data-stu-id="d9dee-158">Allow installation default</span></span>
><span data-ttu-id="d9dee-159">Microsoft Edge Update 1.2.145.5 und höher</span><span class="sxs-lookup"><span data-stu-id="d9dee-159">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <a name="description"></a><span data-ttu-id="d9dee-160">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d9dee-160">Description</span></span>
<span data-ttu-id="d9dee-161">Sie können das Standardverhalten aller Kanäle festlegen, damit Microsoft Edge für in die Domäne eingebundene Geräte. zugelassen oder blockiert wird.</span><span class="sxs-lookup"><span data-stu-id="d9dee-161">You can specify the default behavior of all channels to allow or block Microsoft Edge on domain-joined devices.</span></span>

<span data-ttu-id="d9dee-162">Sie können diese Richtlinie für einzelne Kanäle außer Kraft setzen, indem Sie die Richtlinie '[Installation zulassen](#install)' für bestimmte Kanäle aktivieren.</span><span class="sxs-lookup"><span data-stu-id="d9dee-162">You can override this policy for individual channels by enabling the '[Allow installation](#install)' policy for specific channels.</span></span>

<span data-ttu-id="d9dee-163">Wenn Sie diese Richtlinie deaktivieren, wird die Installation von Microsoft Edge blockiert.</span><span class="sxs-lookup"><span data-stu-id="d9dee-163">If you disable this policy, the installation of Microsoft Edge is blocked.</span></span> <span data-ttu-id="d9dee-164">Dies wirkt sich nur auf die Installation der Microsoft Edge-Software aus, wenn die Richtlinie "[Installation zulassen](#install)" auf "nicht konfiguriert festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d9dee-164">This only affects the installation of Microsoft Edge software when the '[Allow installation](#install)' policy is set to Not Configured.</span></span>

<span data-ttu-id="d9dee-165">Diese Richtlinie verhindert nicht, dass Microsoft Edge Update ausgeführt wird, oder dass Benutzer die Microsoft Edge-Software auf andere Weise installieren.</span><span class="sxs-lookup"><span data-stu-id="d9dee-165">This policy doesn't prevent Microsoft Edge Update from running or prevent users from installing Microsoft Edge software using other methods.</span></span>

<span data-ttu-id="d9dee-166">Diese Richtlinie ist nur für Windows-Instanzen verfügbar, die in eine Microsoft® Active Directory®-Domäne eingebunden werden.</span><span class="sxs-lookup"><span data-stu-id="d9dee-166">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="d9dee-167">Windows-Informationen und -Einstellungen</span><span class="sxs-lookup"><span data-stu-id="d9dee-167">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="d9dee-168">Informationen zur Gruppenrichtlinie (ADMX)</span><span class="sxs-lookup"><span data-stu-id="d9dee-168">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="d9dee-169">Eindeutiger Name der GP: InstallDefault</span><span class="sxs-lookup"><span data-stu-id="d9dee-169">GP unique name: InstallDefault</span></span>
- <span data-ttu-id="d9dee-170">GP-Name: Standardinstallation zulassen</span><span class="sxs-lookup"><span data-stu-id="d9dee-170">GP name: Allow installation default</span></span>
- <span data-ttu-id="d9dee-171">GP-Pfad: Administrative Vorlagen/Microsoft Edge Update/Anwendungen</span><span class="sxs-lookup"><span data-stu-id="d9dee-171">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="d9dee-172">Name der GP-ADMX-Datei: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="d9dee-172">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="d9dee-173">Windows-Registrierungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="d9dee-173">Windows Registry Settings</span></span>
- <span data-ttu-id="d9dee-174">Pfad: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="d9dee-174">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="d9dee-175">Name des Wertes: InstallDefault</span><span class="sxs-lookup"><span data-stu-id="d9dee-175">Value Name: InstallDefault</span></span>
- <span data-ttu-id="d9dee-176">Werttyp: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="d9dee-176">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="d9dee-177">Beispielwert:</span><span class="sxs-lookup"><span data-stu-id="d9dee-177">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="d9dee-178">Zurück zum Anfang</span><span class="sxs-lookup"><span data-stu-id="d9dee-178">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="updatedefault"></a><span data-ttu-id="d9dee-179">UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="d9dee-179">UpdateDefault</span></span>
#### <a name="update-policy-override-default"></a><span data-ttu-id="d9dee-180">Die Updaterichtlinie überschreibt die Standardrichtlinie</span><span class="sxs-lookup"><span data-stu-id="d9dee-180">Update policy override default</span></span>
><span data-ttu-id="d9dee-181">Microsoft Edge Update 1.2.145.5 und höher</span><span class="sxs-lookup"><span data-stu-id="d9dee-181">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <a name="description"></a><span data-ttu-id="d9dee-182">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d9dee-182">Description</span></span>
<span data-ttu-id="d9dee-183">Hier können Sie das Standardverhalten für alle Kanäle angeben, wie Microsoft Edge Update verfügbare Updates für Microsoft Edge verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="d9dee-183">Lets you specify the default behavior for all channels concerning the way Microsoft Edge Update handles available updates for Microsoft Edge.</span></span> <span data-ttu-id="d9dee-184">Kann für einzelne Kanäle durch Angabe der Richtlinie '[Außerkraftsetzung von Updaterichtlinien](#update)' für diese bestimmten Kanäle außer Kraft gesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="d9dee-184">Can be overridden for individual channels by specifying the '[Update policy override](#update)' policy for those specific channels.</span></span>

  <span data-ttu-id="d9dee-185">Wenn Sie diese Richtlinie aktivieren, verarbeitet Microsoft Edge Update Microsoft Edge-Updates entsprechend der Konfiguration der folgenden Optionen:</span><span class="sxs-lookup"><span data-stu-id="d9dee-185">If you enable this policy, Microsoft Edge Update handles Microsoft Edge updates according to how you configure the following options:</span></span>
   - <span data-ttu-id="d9dee-186">Updates immer zulassen: Updates werden immer dann angewendet, wenn sie gefunden werden, entweder durch die regelmäßige Updateprüfung oder durch eine manuelle Updateprüfung.</span><span class="sxs-lookup"><span data-stu-id="d9dee-186">Always allow updates: Updates are always applied when found, either by periodic update check or by a manual update check.</span></span>
   - <span data-ttu-id="d9dee-187">Nur automatische unbeaufsichtigte Updates: Updates werden nur angewendet, wenn sie von der regelmäßigen Updateprüfung gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="d9dee-187">Automatic silent updates only: Updates are applied only when they're found by the periodic update check.</span></span>
   - <span data-ttu-id="d9dee-188">Nur manuelle Updates: Updates werden nur angewendet, wenn der Benutzer eine manuelle Updateprüfung ausführt.</span><span class="sxs-lookup"><span data-stu-id="d9dee-188">Manual updates only: Updates are applied only when the user runs a manual update check.</span></span>
   - <span data-ttu-id="d9dee-189">Updates deaktiviert: Updates werden nie angewendet.</span><span class="sxs-lookup"><span data-stu-id="d9dee-189">Updates disabled: Updates are never applied.</span></span>

  <span data-ttu-id="d9dee-190">Wenn Sie „manuelle Updates” auswählen, stellen Sie sicher, dass Sie regelmäßig nach Updates suchen, indem Sie den manuellen Updatemechanismus der App verwenden, sofern verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d9dee-190">If you select manual updates, make sure you periodically check for updates by using the app's manual update mechanism, if available.</span></span> <span data-ttu-id="d9dee-191">Wenn Sie Updates deaktivieren, suchen Sie regelmäßig nach Updates und verteilen Sie diese an die Benutzer.</span><span class="sxs-lookup"><span data-stu-id="d9dee-191">If you disable updates, periodically check for updates, and distribute them to users.</span></span>

  <span data-ttu-id="d9dee-192">Wenn Sie diese Richtlinie nicht aktivieren und konfigurieren, behandelt Microsoft Edge Update die verfügbaren Updates gemäß der Richtlinie '[Außerkraftsetzung von Updaterichtlinien](#update)'.</span><span class="sxs-lookup"><span data-stu-id="d9dee-192">If you don't enable and configure this policy, Microsoft Edge Update handles available updates as specified by the '[Update policy override](#update)' policy.</span></span>

  <span data-ttu-id="d9dee-193">Diese Richtlinie ist nur für Windows-Instanzen verfügbar, die in eine Microsoft® Active Directory®-Domäne eingebunden werden.</span><span class="sxs-lookup"><span data-stu-id="d9dee-193">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="d9dee-194">Windows-Informationen und -Einstellungen</span><span class="sxs-lookup"><span data-stu-id="d9dee-194">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="d9dee-195">Informationen zur Gruppenrichtlinie (ADMX)</span><span class="sxs-lookup"><span data-stu-id="d9dee-195">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="d9dee-196">Eindeutiger Name der GP: UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="d9dee-196">GP unique name: UpdateDefault</span></span>
- <span data-ttu-id="d9dee-197">GP-Name: Die Updaterichtlinie überschreibt die Standardrichtlinie</span><span class="sxs-lookup"><span data-stu-id="d9dee-197">GP name: Update policy override default</span></span>
- <span data-ttu-id="d9dee-198">GP-Pfad: Administrative Vorlagen/Microsoft Edge Update/Anwendungen</span><span class="sxs-lookup"><span data-stu-id="d9dee-198">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="d9dee-199">Name der GP-ADMX-Datei: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="d9dee-199">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="d9dee-200">Windows-Registrierungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="d9dee-200">Windows Registry Settings</span></span>
- <span data-ttu-id="d9dee-201">Pfad: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="d9dee-201">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="d9dee-202">Name des Wertes: UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="d9dee-202">Value Name: UpdateDefault</span></span>
- <span data-ttu-id="d9dee-203">Werttyp: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="d9dee-203">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="d9dee-204">Beispielwert:</span><span class="sxs-lookup"><span data-stu-id="d9dee-204">Example value:</span></span>
```
0x00000003
```
[<span data-ttu-id="d9dee-205">Zurück zum Anfang</span><span class="sxs-lookup"><span data-stu-id="d9dee-205">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="install"></a><span data-ttu-id="d9dee-206">Installieren</span><span class="sxs-lookup"><span data-stu-id="d9dee-206">Install</span></span>
#### <a name="allow-installation"></a><span data-ttu-id="d9dee-207">Installation zulassen</span><span class="sxs-lookup"><span data-stu-id="d9dee-207">Allow installation</span></span>
><span data-ttu-id="d9dee-208">Microsoft Edge Update 1.2.145.5 und höher</span><span class="sxs-lookup"><span data-stu-id="d9dee-208">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <a name="description"></a><span data-ttu-id="d9dee-209">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d9dee-209">Description</span></span>
<span data-ttu-id="d9dee-210">Gibt an, ob ein Microsoft Edge-Kanal auf in die Domäne eingebundene Geräte installiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="d9dee-210">Specifies whether a Microsoft Edge channel can be installed on domain-joined devices.</span></span>

  <span data-ttu-id="d9dee-211">Wenn Sie diese Richtlinie für einen Kanal aktivieren, wird die Installation von Microsoft Edge nicht blockiert.</span><span class="sxs-lookup"><span data-stu-id="d9dee-211">If you enable this policy for a channel, Microsoft Edge will not be blocked from installation.</span></span>

  <span data-ttu-id="d9dee-212">Wenn Sie diese Richtlinie für einen Kanal deaktivieren, wird die Installation von Microsoft Edge blockiert.</span><span class="sxs-lookup"><span data-stu-id="d9dee-212">If you disable this policy for a channel, Microsoft Edge will be blocked from installation.</span></span>

  <span data-ttu-id="d9dee-213">Wenn Sie diese Richtlinie nicht für einen Kanal konfigurieren, bestimmt die Richtlinienkonfiguration '[Standardinstallation zulassen](#installdefault)', ob Benutzer diesen Kanal von Microsoft Edge installieren können.</span><span class="sxs-lookup"><span data-stu-id="d9dee-213">If you don't configure this policy for a channel, the '[Allow installation default](#installdefault)' policy configuration determines whether users can install that channel of Microsoft Edge.</span></span>

  <span data-ttu-id="d9dee-214">Diese Richtlinie ist nur für Windows-Instanzen verfügbar, die in eine Microsoft® Active Directory®-Domäne eingebunden werden.</span><span class="sxs-lookup"><span data-stu-id="d9dee-214">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="d9dee-215">Windows-Informationen und -Einstellungen</span><span class="sxs-lookup"><span data-stu-id="d9dee-215">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="d9dee-216">Informationen zur Gruppenrichtlinie (ADMX)</span><span class="sxs-lookup"><span data-stu-id="d9dee-216">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="d9dee-217">Eindeutiger Name der GP: Install</span><span class="sxs-lookup"><span data-stu-id="d9dee-217">GP unique name: Install</span></span>
- <span data-ttu-id="d9dee-218">GP-Name: Installation zulassen</span><span class="sxs-lookup"><span data-stu-id="d9dee-218">GP name: Allow installation</span></span>
- <span data-ttu-id="d9dee-219">GP-Pfad:</span><span class="sxs-lookup"><span data-stu-id="d9dee-219">GP path:</span></span> 
  - <span data-ttu-id="d9dee-220">Administrative Vorlagen/Microsoft Edge Update/Anwendungen/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="d9dee-220">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="d9dee-221">Administrative Vorlagen/Microsoft Edge Update/Anwendungen/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="d9dee-221">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="d9dee-222">Administrative Vorlagen/Microsoft Edge Update/Anwendungen/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="d9dee-222">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="d9dee-223">Administrative Vorlagen/Microsoft Edge Update/Anwendungen/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="d9dee-223">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="d9dee-224">Name der GP-ADMX-Datei: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="d9dee-224">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="d9dee-225">Windows-Registrierungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="d9dee-225">Windows Registry Settings</span></span>
- <span data-ttu-id="d9dee-226">Pfad: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="d9dee-226">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="d9dee-227">Name des Wertes:</span><span class="sxs-lookup"><span data-stu-id="d9dee-227">Value Name:</span></span> 
  - <span data-ttu-id="d9dee-228">(Stable): Install{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="d9dee-228">(Stable): Install{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="d9dee-229">(Beta): Install{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="d9dee-229">(Beta): Install{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="d9dee-230">(Canary): Install{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="d9dee-230">(Canary): Install{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="d9dee-231">(Dev): Install{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="d9dee-231">(Dev): Install{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="d9dee-232">Werttyp: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="d9dee-232">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="d9dee-233">Beispielwert:</span><span class="sxs-lookup"><span data-stu-id="d9dee-233">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="d9dee-234">Zurück zum Anfang</span><span class="sxs-lookup"><span data-stu-id="d9dee-234">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="update"></a><span data-ttu-id="d9dee-235">Update</span><span class="sxs-lookup"><span data-stu-id="d9dee-235">Update</span></span>
#### <a name="update-policy-override"></a><span data-ttu-id="d9dee-236">Außerkraftsetzung von Updaterichtlinien</span><span class="sxs-lookup"><span data-stu-id="d9dee-236">Update policy override</span></span>
><span data-ttu-id="d9dee-237">Microsoft Edge Update 1.2.145.5 und höher</span><span class="sxs-lookup"><span data-stu-id="d9dee-237">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <a name="description"></a><span data-ttu-id="d9dee-238">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d9dee-238">Description</span></span>
<span data-ttu-id="d9dee-239">Gibt an, wie Microsoft Edge Update verfügbare Updates von Microsoft Edge behandelt.</span><span class="sxs-lookup"><span data-stu-id="d9dee-239">Specifies how Microsoft Edge Update handles available updates from Microsoft Edge.</span></span>

<span data-ttu-id="d9dee-240">Wenn Sie diese Richtlinie aktivieren, verarbeitet Microsoft Edge Update Microsoft Edge-Updates entsprechend der Konfiguration der folgenden Optionen:</span><span class="sxs-lookup"><span data-stu-id="d9dee-240">If you enable this policy, Microsoft Edge Update handles Microsoft Edge updates according to how you configure the following options:</span></span>
  - <span data-ttu-id="d9dee-241">Updates immer zulassen: Updates werden immer dann angewendet, wenn sie gefunden werden, entweder durch die regelmäßige Updateprüfung oder durch eine manuelle Updateprüfung.</span><span class="sxs-lookup"><span data-stu-id="d9dee-241">Always allow updates: Updates are always applied when found, either by periodic update check or by a manual update check.</span></span>
  - <span data-ttu-id="d9dee-242">Nur automatische unbeaufsichtigte Updates: Updates werden nur angewendet, wenn sie von der regelmäßigen Updateprüfung gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="d9dee-242">Automatic silent updates only: Updates are applied only when they're found by the periodic update check.</span></span>
  - <span data-ttu-id="d9dee-243">Nur manuelle Updates: Updates werden nur angewendet, wenn der Benutzer eine manuelle Updateprüfung ausführt.</span><span class="sxs-lookup"><span data-stu-id="d9dee-243">Manual updates only: Updates are applied only when the user runs a manual update check.</span></span> <span data-ttu-id="d9dee-244">(Nicht alle Apps bieten eine Schnittstelle für diese Option.)</span><span class="sxs-lookup"><span data-stu-id="d9dee-244">(Not all apps provide an interface for this option.)</span></span>
  - <span data-ttu-id="d9dee-245">Updates deaktiviert: Updates werden nie angewendet.</span><span class="sxs-lookup"><span data-stu-id="d9dee-245">Updates disabled: Updates are never applied.</span></span>

<span data-ttu-id="d9dee-246">Wenn Sie „manuelle Updates” auswählen, stellen Sie sicher, dass Sie regelmäßig nach Updates suchen, indem Sie den manuellen Updatemechanismus der App verwenden, sofern verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d9dee-246">If you select manual updates, make sure you periodically check for updates by using the app's manual update mechanism, if available.</span></span> <span data-ttu-id="d9dee-247">Wenn Sie Updates deaktivieren, suchen Sie regelmäßig nach Updates und verteilen Sie diese an die Benutzer.</span><span class="sxs-lookup"><span data-stu-id="d9dee-247">If you disable updates, periodically check for updates, and distribute them to users.</span></span>

<span data-ttu-id="d9dee-248">Wenn Sie diese Richtlinie nicht aktivieren und konfigurieren, behandelt Microsoft Edge Update die verfügbaren Updates gemäß der Richtlinie '[Die Updaterichtlinie überschreibt die Standardrichtlinie](#updatedefault)'.</span><span class="sxs-lookup"><span data-stu-id="d9dee-248">If you don't enable and configure this policy, Microsoft Edge Update handles available updates as specified by the '[Update policy override default](#updatedefault)' policy.</span></span>

<span data-ttu-id="d9dee-249">Weitere Informationen finden Sie unter [https://go.microsoft.com/fwlink/?linkid=2136406](https://go.microsoft.com/fwlink/?linkid=2136406).</span><span class="sxs-lookup"><span data-stu-id="d9dee-249">See [https://go.microsoft.com/fwlink/?linkid=2136406](https://go.microsoft.com/fwlink/?linkid=2136406) for more information.</span></span>

<span data-ttu-id="d9dee-250">Diese Richtlinie ist nur für Windows-Instanzen verfügbar, die in eine Microsoft® Active Directory®-Domäne eingebunden werden.</span><span class="sxs-lookup"><span data-stu-id="d9dee-250">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="d9dee-251">Windows-Informationen und -Einstellungen</span><span class="sxs-lookup"><span data-stu-id="d9dee-251">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="d9dee-252">Informationen zur Gruppenrichtlinie (ADMX)</span><span class="sxs-lookup"><span data-stu-id="d9dee-252">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="d9dee-253">Eindeutiger Name der GP: Update</span><span class="sxs-lookup"><span data-stu-id="d9dee-253">GP unique name: Update</span></span>
- <span data-ttu-id="d9dee-254">GP-Name: Außerkraftsetzung von Updaterichtlinien</span><span class="sxs-lookup"><span data-stu-id="d9dee-254">GP name: Update policy override</span></span>
- <span data-ttu-id="d9dee-255">GP-Pfad:</span><span class="sxs-lookup"><span data-stu-id="d9dee-255">GP path:</span></span> 
  - <span data-ttu-id="d9dee-256">Administrative Vorlagen/Microsoft Edge Update/Anwendungen/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="d9dee-256">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="d9dee-257">Administrative Vorlagen/Microsoft Edge Update/Anwendungen/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="d9dee-257">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="d9dee-258">Administrative Vorlagen/Microsoft Edge Update/Anwendungen/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="d9dee-258">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="d9dee-259">Administrative Vorlagen/Microsoft Edge Update/Anwendungen/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="d9dee-259">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="d9dee-260">Name der GP-ADMX-Datei: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="d9dee-260">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="d9dee-261">Windows-Registrierungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="d9dee-261">Windows Registry Settings</span></span>
- <span data-ttu-id="d9dee-262">Pfad: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="d9dee-262">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="d9dee-263">Name des Wertes:</span><span class="sxs-lookup"><span data-stu-id="d9dee-263">Value Name:</span></span> 
  - <span data-ttu-id="d9dee-264">(Stable): Update{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="d9dee-264">(Stable): Update{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="d9dee-265">(Beta): Update{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="d9dee-265">(Beta): Update{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="d9dee-266">(Canary): Update{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="d9dee-266">(Canary): Update{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="d9dee-267">(Dev): Update{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="d9dee-267">(Dev): Update{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="d9dee-268">Werttyp: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="d9dee-268">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="d9dee-269">Beispielwert:</span><span class="sxs-lookup"><span data-stu-id="d9dee-269">Example value:</span></span>
```
always allow updates 0x00000001
Automatic silent updates only 0x00000003
manual updates only 0x00000002
updates disabled 0x00000000
```
[<span data-ttu-id="d9dee-270">Zurück zum Anfang</span><span class="sxs-lookup"><span data-stu-id="d9dee-270">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="allowsxs"></a><span data-ttu-id="d9dee-271">Allowsxs</span><span class="sxs-lookup"><span data-stu-id="d9dee-271">Allowsxs</span></span>
#### <a name="allow-microsoft-edge-side-by-side-browser-experience"></a><span data-ttu-id="d9dee-272">Microsoft Edge Seite-an-Seite-Browserumgebung zulassen</span><span class="sxs-lookup"><span data-stu-id="d9dee-272">Allow Microsoft Edge Side by Side browser experience</span></span>
><span data-ttu-id="d9dee-273">Microsoft Edge Update 1.2.145.5 und höher</span><span class="sxs-lookup"><span data-stu-id="d9dee-273">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <a name="description"></a><span data-ttu-id="d9dee-274">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d9dee-274">Description</span></span>
<span data-ttu-id="d9dee-275">Mit dieser Richtlinie können Benutzer Microsoft Edge (Edge-HTML) und Microsoft Edge (Chromium-basiert) nebeneinander ausführen.</span><span class="sxs-lookup"><span data-stu-id="d9dee-275">This policy lets a user run Microsoft Edge (Edge HTML) and Microsoft Edge (Chromium-based) side-by-side.</span></span>

<span data-ttu-id="d9dee-276">Wenn diese Richtlinie auf „Nicht konfiguriert” festgelegt ist, ersetzt Microsoft Edge (Chromium-basiert) Microsoft Edge (Edge-HTML) nach dem stabilen Kanal von Microsoft Edge (Chromium-basierten), und die Sicherheitsupdates vom November 2019 werden installiert.</span><span class="sxs-lookup"><span data-stu-id="d9dee-276">If this policy is set to “Not configured”, Microsoft Edge (Chromium-based) will replace Microsoft Edge (Edge HTML) after the Microsoft Edge (Chromium-based) stable channel and the November 2019 security updates are installed.</span></span>  <span data-ttu-id="d9dee-277">Hierbei handelt es sich um das gleiche Verhalten wie bei der Einstellung „Deaktiviert“.</span><span class="sxs-lookup"><span data-stu-id="d9dee-277">This is the same behavior as the “Disabled” setting.</span></span>

<span data-ttu-id="d9dee-278">Die Einstellung „Deaktiviert” blockiert eine Seite-an-Seite-Umgebung, und Microsoft Edge (Chromium-basiert) ersetzt Microsoft Edge (Edge-HTML) nach dem stabilen Kanal von Microsoft Edge (Chromium-basierten). Außerdem werden die Sicherheitsupdates vom November 2019 installiert.</span><span class="sxs-lookup"><span data-stu-id="d9dee-278">The “Disabled” setting blocks a side-by-side experience and Microsoft Edge (Chromium-based) will replace Microsoft Edge (Edge HTML) after the Microsoft Edge (Chromium-based) stable channel and the November 2019 security updates are installed.</span></span>  <span data-ttu-id="d9dee-279">Hierbei handelt es sich um das gleiche Verhalten wie bei der Einstellung „Nicht konfiguriert“.</span><span class="sxs-lookup"><span data-stu-id="d9dee-279">This is the same behavior as the “Not Configured” setting.</span></span>

<span data-ttu-id="d9dee-280">Wenn diese Richtlinie aktiviert ist, können Microsoft Edge (Chromium-basiert) und Microsoft Edge (Edge-HTML) nach der Installation von Microsoft Edge (Chromium-basiert) nebeneinander ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d9dee-280">When this policy is “Enabled”, Microsoft Edge (Chromium-based) and Microsoft Edge (Edge HTML) can run side-by-side after Microsoft Edge (Chromium-based) is installed.</span></span>

<span data-ttu-id="d9dee-281">Damit diese Gruppenrichtlinie wirksam wird, muss sie vor der automatischen Installation von Microsoft Edge (Chromium-basiert) von Windows Update konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="d9dee-281">For this group policy to take affect, it must be configured before the automatic install of Microsoft Edge (Chromium-based) by Windows Update.</span></span> <span data-ttu-id="d9dee-282">Hinweis: Ein Benutzer kann das automatische Update von Microsoft Edge (Chromium-basiert) mit dem Microsoft Edge (Chromium-basiert) Blocker Toolkit blockieren.</span><span class="sxs-lookup"><span data-stu-id="d9dee-282">Note: A user can block the automatic update of Microsoft Edge (Chromium-based) by using the Microsoft Edge (Chromium-based) Blocker Toolkit.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="d9dee-283">Windows-Informationen und -Einstellungen</span><span class="sxs-lookup"><span data-stu-id="d9dee-283">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="d9dee-284">Informationen zur Gruppenrichtlinie (ADMX)</span><span class="sxs-lookup"><span data-stu-id="d9dee-284">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="d9dee-285">Eindeutiger Name der GP: Allowsxs</span><span class="sxs-lookup"><span data-stu-id="d9dee-285">GP unique name: Allowsxs</span></span>
- <span data-ttu-id="d9dee-286">GP-Name: Microsoft Edge Seite-an-Seite-Browserumgebung zulassen</span><span class="sxs-lookup"><span data-stu-id="d9dee-286">GP name: Allow Microsoft Edge Side by Side browser experience</span></span>
- <span data-ttu-id="d9dee-287">GP-Pfad: Administrative Vorlagen/Microsoft Edge Update/Anwendungen</span><span class="sxs-lookup"><span data-stu-id="d9dee-287">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="d9dee-288">Name der GP-ADMX-Datei: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="d9dee-288">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="d9dee-289">Windows-Registrierungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="d9dee-289">Windows Registry Settings</span></span>
- <span data-ttu-id="d9dee-290">Pfad: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="d9dee-290">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="d9dee-291">Name des Wertes: Allowsxs</span><span class="sxs-lookup"><span data-stu-id="d9dee-291">Value Name: Allowsxs</span></span>
- <span data-ttu-id="d9dee-292">Werttyp: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="d9dee-292">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="d9dee-293">Beispielwert:</span><span class="sxs-lookup"><span data-stu-id="d9dee-293">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="d9dee-294">Zurück zum Anfang</span><span class="sxs-lookup"><span data-stu-id="d9dee-294">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="createdesktopshortcutdefault"></a><span data-ttu-id="d9dee-295">CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="d9dee-295">CreateDesktopShortcutDefault</span></span>
#### <a name="prevent-desktop-shortcut-creation-upon-install-default"></a><span data-ttu-id="d9dee-296">Standardeinstellung für das Verhindern der Erstellung von Desktopverknüpfungen bei der Installation</span><span class="sxs-lookup"><span data-stu-id="d9dee-296">Prevent Desktop Shortcut creation upon install default</span></span>
><span data-ttu-id="d9dee-297">Microsoft Edge Update 1.3.128.0 und höher</span><span class="sxs-lookup"><span data-stu-id="d9dee-297">Microsoft Edge Update 1.3.128.0 and later</span></span>

#### <a name="description"></a><span data-ttu-id="d9dee-298">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d9dee-298">Description</span></span>
<span data-ttu-id="d9dee-299">Ermöglicht es Ihnen, das Standardverhalten aller Kanäle für die Erstellung einer Desktopverknüpfung festzulegen, wenn Microsoft Edge installiert wird.</span><span class="sxs-lookup"><span data-stu-id="d9dee-299">Lets you specify the default behavior for all channels for creating a desktop shortcut when Microsoft Edge is installed.</span></span>

  <span data-ttu-id="d9dee-300">Wenn Sie diese Richtlinie aktivieren, wird beim Installieren von Microsoft Edge eine Desktopverknüpfung erstellt.</span><span class="sxs-lookup"><span data-stu-id="d9dee-300">If you enable this policy a desktop shortcut is created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="d9dee-301">Wenn Sie diese Richtlinie deaktivieren, wird beim Installieren von Microsoft Edge keine Desktopverknüpfung erstellt.</span><span class="sxs-lookup"><span data-stu-id="d9dee-301">If you disable this policy, no desktop shortcut will be created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="d9dee-302">Wenn Sie diese Richtlinie nicht konfigurieren, wird während der Installation eine Desktopverknüpfung zu Microsoft Edge erstellt.</span><span class="sxs-lookup"><span data-stu-id="d9dee-302">If you don’t configure this policy a desktop shortcut to Microsoft Edge will be created during installation.</span></span>
<span data-ttu-id="d9dee-303">Wenn Microsoft Edge bereits installiert ist, hat diese Richtlinie keine Auswirkung.</span><span class="sxs-lookup"><span data-stu-id="d9dee-303">If Microsoft Edge is already installed, this policy will have no effect.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="d9dee-304">Windows-Informationen und -Einstellungen</span><span class="sxs-lookup"><span data-stu-id="d9dee-304">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="d9dee-305">Informationen zur Gruppenrichtlinie (ADMX)</span><span class="sxs-lookup"><span data-stu-id="d9dee-305">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="d9dee-306">Eindeutiger Name der GP: CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="d9dee-306">GP unique name: CreateDesktopShortcutDefault</span></span>
- <span data-ttu-id="d9dee-307">GP-Name: Standardeinstellung "Erstellung von Desktopverknüpfungen bei der Installation verhindern"</span><span class="sxs-lookup"><span data-stu-id="d9dee-307">GP name: Prevent Desktop Shortcut creation upon install default</span></span>
- <span data-ttu-id="d9dee-308">GP-Pfad: Administrative Vorlagen/Microsoft Edge Update/Anwendungen</span><span class="sxs-lookup"><span data-stu-id="d9dee-308">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="d9dee-309">Name der GP-ADMX-Datei: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="d9dee-309">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="d9dee-310">Windows-Registrierungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="d9dee-310">Windows Registry Settings</span></span>
- <span data-ttu-id="d9dee-311">Pfad: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="d9dee-311">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="d9dee-312">Wertname: CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="d9dee-312">Value Name: CreateDesktopShortcutDefault</span></span>
- <span data-ttu-id="d9dee-313">Werttyp: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="d9dee-313">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="d9dee-314">Beispielwert:</span><span class="sxs-lookup"><span data-stu-id="d9dee-314">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="d9dee-315">Zurück zum Anfang</span><span class="sxs-lookup"><span data-stu-id="d9dee-315">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="createdesktopshortcut"></a><span data-ttu-id="d9dee-316">CreateDesktopShortcut</span><span class="sxs-lookup"><span data-stu-id="d9dee-316">CreateDesktopShortcut</span></span>
#### <a name="prevent-desktop-shortcut-creation-upon-install"></a><span data-ttu-id="d9dee-317">GP-Name: Erstellen von Desktopverknüpfungen bei Standardinstallation</span><span class="sxs-lookup"><span data-stu-id="d9dee-317">Prevent Desktop Shortcut creation upon install</span></span>
><span data-ttu-id="d9dee-318">Microsoft Edge Update 1.3.128.0 und höher</span><span class="sxs-lookup"><span data-stu-id="d9dee-318">Microsoft Edge Update 1.3.128.0 and later</span></span>

#### <a name="description"></a><span data-ttu-id="d9dee-319">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d9dee-319">Description</span></span>
<span data-ttu-id="d9dee-320">Wenn Sie diese Richtlinie aktivieren, wird beim Installieren von Microsoft Edge eine Desktopverknüpfung erstellt.</span><span class="sxs-lookup"><span data-stu-id="d9dee-320">If you enable this policy a desktop shortcut is created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="d9dee-321">Wenn Sie diese Richtlinie deaktivieren, wird beim Installieren von Microsoft Edge keine Desktopverknüpfung erstellt.</span><span class="sxs-lookup"><span data-stu-id="d9dee-321">If you disable this policy, no desktop shortcut will be created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="d9dee-322">Wenn Sie diese Richtlinie nicht konfigurieren, wird während der Installation eine Desktopverknüpfung zu Microsoft Edge erstellt.</span><span class="sxs-lookup"><span data-stu-id="d9dee-322">If you don’t configure this policy a desktop shortcut to Microsoft Edge will be created during installation.</span></span>
<span data-ttu-id="d9dee-323">Wenn Microsoft Edge bereits installiert ist, hat diese Richtlinie keine Auswirkung.</span><span class="sxs-lookup"><span data-stu-id="d9dee-323">If Microsoft Edge is already installed, this policy will have no effect.</span></span>

  <span data-ttu-id="d9dee-324">Wenn Sie diese Richtlinie für einen Kanal nicht konfigurieren, bestimmt die Richtlinienkonfiguration "[Standardeinstellung für das Verhindern der Erstellung von Desktopverknüpfungen bei der Installation](#createdesktopshortcutdefault)", ob bei Installation von Microsoft Edge eine Verknüpfung erstellt wird oder nicht.</span><span class="sxs-lookup"><span data-stu-id="d9dee-324">If you don't configure this policy for a channel, the '[Prevent Desktop Shortcut creation upon install default](#createdesktopshortcutdefault)' policy configuration determines shortcut creation when Microsoft Edge is installed.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="d9dee-325">Windows-Informationen und -Einstellungen</span><span class="sxs-lookup"><span data-stu-id="d9dee-325">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="d9dee-326">Informationen zur Gruppenrichtlinie (ADMX)</span><span class="sxs-lookup"><span data-stu-id="d9dee-326">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="d9dee-327">Eindeutiger Name der GP: CreateDesktopShortcut</span><span class="sxs-lookup"><span data-stu-id="d9dee-327">GP unique name: CreateDesktopShortcut</span></span>
- <span data-ttu-id="d9dee-328">GP-Name: Erstellen von Desktopverknüpfungen bei Installation verhindern</span><span class="sxs-lookup"><span data-stu-id="d9dee-328">GP name: Prevent Desktop Shortcut creation upon install</span></span>
- <span data-ttu-id="d9dee-329">GP-Pfad:</span><span class="sxs-lookup"><span data-stu-id="d9dee-329">GP path:</span></span> 
  - <span data-ttu-id="d9dee-330">Administrative Vorlagen/Microsoft Edge Update/Anwendungen/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="d9dee-330">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="d9dee-331">Administrative Vorlagen/Microsoft Edge Update/Anwendungen/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="d9dee-331">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="d9dee-332">Administrative Vorlagen/Microsoft Edge Update/Anwendungen/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="d9dee-332">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="d9dee-333">Administrative Vorlagen/Microsoft Edge Update/Anwendungen/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="d9dee-333">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="d9dee-334">Name der GP-ADMX-Datei: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="d9dee-334">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="d9dee-335">Windows-Registrierungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="d9dee-335">Windows Registry Settings</span></span>
- <span data-ttu-id="d9dee-336">Pfad: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="d9dee-336">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="d9dee-337">Name des Wertes:</span><span class="sxs-lookup"><span data-stu-id="d9dee-337">Value Name:</span></span> 
  - <span data-ttu-id="d9dee-338">(Stable): CreateDesktopShortcut{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="d9dee-338">(Stable): CreateDesktopShortcut{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="d9dee-339">(Beta): CreateDesktopShortcut{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="d9dee-339">(Beta): CreateDesktopShortcut{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="d9dee-340">(Canary): CreateDesktopShortcut{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="d9dee-340">(Canary): CreateDesktopShortcut{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="d9dee-341">(Dev): CreateDesktopShortcut{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="d9dee-341">(Dev): CreateDesktopShortcut{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="d9dee-342">Werttyp: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="d9dee-342">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="d9dee-343">Beispielwert:</span><span class="sxs-lookup"><span data-stu-id="d9dee-343">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="d9dee-344">Zurück zum Anfang</span><span class="sxs-lookup"><span data-stu-id="d9dee-344">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="rollbacktotargetversion"></a><span data-ttu-id="d9dee-345">RollbackToTargetVersion</span><span class="sxs-lookup"><span data-stu-id="d9dee-345">RollbackToTargetVersion</span></span>
#### <a name="rollback-to-target-version"></a><span data-ttu-id="d9dee-346">Zurücksetzung auf Zielversion</span><span class="sxs-lookup"><span data-stu-id="d9dee-346">Rollback to Target version</span></span>
><span data-ttu-id="d9dee-347">Microsoft Edge Update 1.3.133.3 und höher</span><span class="sxs-lookup"><span data-stu-id="d9dee-347">Microsoft Edge Update 1.3.133.3 and later</span></span>

#### <a name="description"></a><span data-ttu-id="d9dee-348">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d9dee-348">Description</span></span>
<span data-ttu-id="d9dee-349">Gibt an, dass Microsoft Edge Update Installationen von Microsoft Edge auf die in "[Zielversionaußerkraftsetzung](#targetversionprefix)" angegebene Version zurücksetzen soll.</span><span class="sxs-lookup"><span data-stu-id="d9dee-349">Specifies that Microsoft Edge Update should rollback installations of Microsoft Edge to the version indicated in '[Target version override](#targetversionprefix)'.</span></span>

<span data-ttu-id="d9dee-350">Diese Richtlinie hat keine Wirkung, es sei denn, "[Zielversionaußerkraftsetzung](#targetversionprefix)" ist festgelegt und "[Update-Richtlinie außer Kraft setzen](#update)" auf einen der Zustände "ein" festgelegt ist (Updates immer zulassen, Nur automatische unbeaufsichtigte Updates, Nur manuelle Updates).</span><span class="sxs-lookup"><span data-stu-id="d9dee-350">This policy has no effect unless '[Target version override](#targetversionprefix)' is set and '[Update policy override](#update)' is set to one of the ON states (Always allow updates, Automatic silent updates only, Manual updates only).</span></span>

<span data-ttu-id="d9dee-351">Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, bleiben Installationen mit einer höheren Version als die von "[Zielversionaußerkraftsetzung](#targetversionprefix)" unverändert.</span><span class="sxs-lookup"><span data-stu-id="d9dee-351">If you disable this policy or don't configure it, installs that have a version higher than that specified by '[Target version override](#targetversionprefix)' will be left as-is.</span></span>

<span data-ttu-id="d9dee-352">Wenn Sie diese Richtlinie aktivieren, werden Installationen mit einer aktuellen Version, die höher ist als durch "[Zielversionaußerkraftsetzung](#targetversionprefix)" angegeben, auf die Zielversion herabgestuft.</span><span class="sxs-lookup"><span data-stu-id="d9dee-352">If you enable this policy, installs that have a current version higher than specified by the '[Target version override](#targetversionprefix)' will be downgraded to the target version.</span></span>

<span data-ttu-id="d9dee-353">Wir empfehlen Benutzern, die neueste Version des Microsoft Edge-Browsers zu installieren, um den Schutz durch die neuesten Sicherheitsupdates zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="d9dee-353">We recommend that users install the latest version of the Microsoft Edge browser to ensure protection by the latest security updates.</span></span> <span data-ttu-id="d9dee-354">Ein Rollback zu einer früheren Version birgt Risiken, die mit bekannten Sicherheitsproblemen zu tun haben.</span><span class="sxs-lookup"><span data-stu-id="d9dee-354">Rollback to an earlier version risks exposure to known security issues.</span></span> <span data-ttu-id="d9dee-355">Diese Richtlinie ist als vorübergehender Fix zur Behebung von Problemen in einem Microsoft Edge-Browser-Update vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="d9dee-355">This policy is meant to be used as a temporary fix to address issues in a Microsoft Edge browser update.</span></span>

<span data-ttu-id="d9dee-356">Bevor Sie die Browserversion vorübergehend zurücksetzen, empfehlen wir, die Synchronisierung ([https://go.microsoft.com/fwlink/?linkid=2133032](https://go.microsoft.com/fwlink/?linkid=2133032)) für alle Benutzer in Ihrer Organisation zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="d9dee-356">Before temporarily rolling back your browser version, we recommend that you turn on Sync ([https://go.microsoft.com/fwlink/?linkid=2133032](https://go.microsoft.com/fwlink/?linkid=2133032)) for all users in your organization.</span></span> <span data-ttu-id="d9dee-357">Wenn Sie die Synchronisierung nicht aktivieren, besteht das Risiko eines endgültigen Verlusts von Browserdaten.</span><span class="sxs-lookup"><span data-stu-id="d9dee-357">If you don't turn on Sync, there is a risk of permanent browsing data loss.</span></span> <span data-ttu-id="d9dee-358">Verwenden Sie diese Richtlinie auf eigenes Risiko.</span><span class="sxs-lookup"><span data-stu-id="d9dee-358">Use this policy at your own risk.</span></span>

<span data-ttu-id="d9dee-359">Hinweis: alle Versionen, die für einen Rollback verfügbar sind, können Sie hier [https://aka.ms/EdgeEnterprise](https://aka.ms/EdgeEnterprise) anzeigen.</span><span class="sxs-lookup"><span data-stu-id="d9dee-359">Note: All versions available for rollback can be viewed here [https://aka.ms/EdgeEnterprise](https://aka.ms/EdgeEnterprise).</span></span>

<span data-ttu-id="d9dee-360">Diese Richtlinie bezieht sich auf Microsoft Edge Version 86 oder neuer.</span><span class="sxs-lookup"><span data-stu-id="d9dee-360">This policy applies to Microsoft Edge version 86 or later.</span></span>

<span data-ttu-id="d9dee-361">Weitere Informationen finden Sie unter [https://go.microsoft.com/fwlink/?linkid=2133918](https://go.microsoft.com/fwlink/?linkid=2133918).</span><span class="sxs-lookup"><span data-stu-id="d9dee-361">See [https://go.microsoft.com/fwlink/?linkid=2133918](https://go.microsoft.com/fwlink/?linkid=2133918) for more information.</span></span>

<span data-ttu-id="d9dee-362">Diese Richtlinie ist nur für Windows-Instanzen verfügbar, die in eine Microsoft® Active Directory®-Domäne eingebunden werden.</span><span class="sxs-lookup"><span data-stu-id="d9dee-362">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="d9dee-363">Windows-Informationen und -Einstellungen</span><span class="sxs-lookup"><span data-stu-id="d9dee-363">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="d9dee-364">Informationen zur Gruppenrichtlinie (ADMX)</span><span class="sxs-lookup"><span data-stu-id="d9dee-364">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="d9dee-365">Eindeutiger Name der GP: RollbackToTargetVersion</span><span class="sxs-lookup"><span data-stu-id="d9dee-365">GP unique name: RollbackToTargetVersion</span></span>
- <span data-ttu-id="d9dee-366">Name der GP: Zurücksetzung auf Zielversion</span><span class="sxs-lookup"><span data-stu-id="d9dee-366">GP name: Rollback to Target version</span></span>
- <span data-ttu-id="d9dee-367">GP-Pfad:</span><span class="sxs-lookup"><span data-stu-id="d9dee-367">GP path:</span></span> 
  - <span data-ttu-id="d9dee-368">Administrative Vorlagen/Microsoft Edge Update/Anwendungen/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="d9dee-368">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="d9dee-369">Administrative Vorlagen/Microsoft Edge Update/Anwendungen/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="d9dee-369">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="d9dee-370">Administrative Vorlagen/Microsoft Edge Update/Anwendungen/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="d9dee-370">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="d9dee-371">Administrative Vorlagen/Microsoft Edge Update/Anwendungen/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="d9dee-371">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="d9dee-372">Name der GP-ADMX-Datei: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="d9dee-372">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="d9dee-373">Windows-Registrierungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="d9dee-373">Windows Registry Settings</span></span>
- <span data-ttu-id="d9dee-374">Pfad: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="d9dee-374">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="d9dee-375">Name des Wertes:</span><span class="sxs-lookup"><span data-stu-id="d9dee-375">Value Name:</span></span> 
  - <span data-ttu-id="d9dee-376">(Stable): RollbackToTargetVersion{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="d9dee-376">(Stable): RollbackToTargetVersion{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="d9dee-377">(Beta): RollbackToTargetVersion{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="d9dee-377">(Beta): RollbackToTargetVersion{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="d9dee-378">(Canary): RollbackToTargetVersion{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="d9dee-378">(Canary): RollbackToTargetVersion{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="d9dee-379">(Dev): RollbackToTargetVersion{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="d9dee-379">(Dev): RollbackToTargetVersion{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="d9dee-380">Werttyp: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="d9dee-380">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="d9dee-381">Beispielwert:</span><span class="sxs-lookup"><span data-stu-id="d9dee-381">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="d9dee-382">Zurück zum Anfang</span><span class="sxs-lookup"><span data-stu-id="d9dee-382">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="targetversionprefix"></a><span data-ttu-id="d9dee-383">TargetVersionPrefix</span><span class="sxs-lookup"><span data-stu-id="d9dee-383">TargetVersionPrefix</span></span>
#### <a name="target-version-override"></a><span data-ttu-id="d9dee-384">Zielversion außer Kraft setzen</span><span class="sxs-lookup"><span data-stu-id="d9dee-384">Target version override</span></span>
><span data-ttu-id="d9dee-385">Microsoft Edge Update 1.3.119.43 und höher</span><span class="sxs-lookup"><span data-stu-id="d9dee-385">Microsoft Edge Update 1.3.119.43 and later</span></span>

#### <a name="description"></a><span data-ttu-id="d9dee-386">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d9dee-386">Description</span></span>
<span data-ttu-id="d9dee-387">Wenn diese Richtlinie und die automatische Aktualisierung aktiviert sind, wird Microsoft Edge auf die durch diesen Richtlinienwert angegebene Version aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="d9dee-387">When this policy is enabled, and auto-update is enabled, Microsoft Edge will be updated to the version specified by this policy value.</span></span>

<span data-ttu-id="d9dee-388">Der Richtlinienwert muss eine bestimmte Microsoft Edge-Version sein, z. B. 83.0.499.12.</span><span class="sxs-lookup"><span data-stu-id="d9dee-388">The policy value must be a specific Microsoft Edge version, e.g. 83.0.499.12.</span></span>

<span data-ttu-id="d9dee-389">Wenn ein Gerät über eine neuere Version von Microsoft Edge als der angegebene Wert verfügt, bleibt Microsoft Edge bei der neueren Version und wird nicht auf die angegebene Version herabgestuft.</span><span class="sxs-lookup"><span data-stu-id="d9dee-389">If a device has newer version of Microsoft Edge than the value specified, Microsoft Edge will remain on the newer version and not downgrade to the specified version.</span></span>

<span data-ttu-id="d9dee-390">Wenn die angegebene Version nicht vorhanden oder nicht ordnungsgemäß formatiert ist, bleibt Microsoft Edge bei der aktuellen Version und wird nicht automatisch auf zukünftige Versionen aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="d9dee-390">If the specified version does not exist, or is improperly formatted, then Microsoft Edge will remain on its current version and not update to future versions automatically.</span></span>

<span data-ttu-id="d9dee-391">Weitere Informationen finden Sie unter [https://go.microsoft.com/fwlink/?linkid=2136707](https://go.microsoft.com/fwlink/?linkid=2136707).</span><span class="sxs-lookup"><span data-stu-id="d9dee-391">See [https://go.microsoft.com/fwlink/?linkid=2136707](https://go.microsoft.com/fwlink/?linkid=2136707) for more information.</span></span>

<span data-ttu-id="d9dee-392">Diese Richtlinie ist nur für Windows-Instanzen verfügbar, die in eine Microsoft® Active Directory®-Domäne eingebunden werden.</span><span class="sxs-lookup"><span data-stu-id="d9dee-392">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="d9dee-393">Windows-Informationen und -Einstellungen</span><span class="sxs-lookup"><span data-stu-id="d9dee-393">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="d9dee-394">Informationen zur Gruppenrichtlinie (ADMX)</span><span class="sxs-lookup"><span data-stu-id="d9dee-394">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="d9dee-395">Eindeutiger Name der GP: TargetVersionPrefix</span><span class="sxs-lookup"><span data-stu-id="d9dee-395">GP unique name: TargetVersionPrefix</span></span>
- <span data-ttu-id="d9dee-396">GP-Name: Zielversion außer Kraft setzen</span><span class="sxs-lookup"><span data-stu-id="d9dee-396">GP name: Target version override</span></span>
- <span data-ttu-id="d9dee-397">GP-Pfad:</span><span class="sxs-lookup"><span data-stu-id="d9dee-397">GP path:</span></span> 
  - <span data-ttu-id="d9dee-398">Administrative Vorlagen/Microsoft Edge Update/Anwendungen/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="d9dee-398">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="d9dee-399">Administrative Vorlagen/Microsoft Edge Update/Anwendungen/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="d9dee-399">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="d9dee-400">Administrative Vorlagen/Microsoft Edge Update/Anwendungen/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="d9dee-400">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="d9dee-401">Administrative Vorlagen/Microsoft Edge Update/Anwendungen/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="d9dee-401">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="d9dee-402">Name der GP-ADMX-Datei: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="d9dee-402">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="d9dee-403">Windows-Registrierungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="d9dee-403">Windows Registry Settings</span></span>
- <span data-ttu-id="d9dee-404">Pfad: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="d9dee-404">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="d9dee-405">Name des Wertes:</span><span class="sxs-lookup"><span data-stu-id="d9dee-405">Value Name:</span></span> 
  - <span data-ttu-id="d9dee-406">(Stable): TargetVersionPrefix{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="d9dee-406">(Stable): TargetVersionPrefix{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="d9dee-407">(Beta): TargetVersionPrefix{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="d9dee-407">(Beta): TargetVersionPrefix{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="d9dee-408">(Canary): TargetVersionPrefix{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="d9dee-408">(Canary): TargetVersionPrefix{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="d9dee-409">(Dev): TargetVersionPrefix{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="d9dee-409">(Dev): TargetVersionPrefix{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="d9dee-410">Werttyp: REG_SZ</span><span class="sxs-lookup"><span data-stu-id="d9dee-410">Value Type: REG_SZ</span></span>
##### <a name="example-value"></a><span data-ttu-id="d9dee-411">Beispielwert:</span><span class="sxs-lookup"><span data-stu-id="d9dee-411">Example value:</span></span>
```
83.0.499.12
```
[<span data-ttu-id="d9dee-412">Zurück zum Anfang</span><span class="sxs-lookup"><span data-stu-id="d9dee-412">Back to top</span></span>](#microsoft-edge---update-policies)


## <a name="preferences-policies"></a><span data-ttu-id="d9dee-413">Einstellungsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="d9dee-413">Preferences policies</span></span>

[<span data-ttu-id="d9dee-414">Zurück zum Anfang</span><span class="sxs-lookup"><span data-stu-id="d9dee-414">Back to top</span></span>](#microsoft-edge---update-policies)
### <a name="autoupdatecheckperiodminutes"></a><span data-ttu-id="d9dee-415">AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="d9dee-415">AutoUpdateCheckPeriodMinutes</span></span>
#### <a name="auto-update-check-period-override"></a><span data-ttu-id="d9dee-416">Überschreibung des Überprüfungszeitraums für automatische Updates</span><span class="sxs-lookup"><span data-stu-id="d9dee-416">Auto-update check period override</span></span>
><span data-ttu-id="d9dee-417">Microsoft Edge Update 1.2.145.5 und höher</span><span class="sxs-lookup"><span data-stu-id="d9dee-417">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <a name="description"></a><span data-ttu-id="d9dee-418">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d9dee-418">Description</span></span>
<span data-ttu-id="d9dee-419">Wenn diese Richtlinie aktiviert ist, können Sie einen Wert für die Mindestanzahl von Minuten zwischen automatischen Updateprüfungen festlegen.</span><span class="sxs-lookup"><span data-stu-id="d9dee-419">If enabled, this policy lets you set a value for the minimum number of minutes between automatic update checks.</span></span> <span data-ttu-id="d9dee-420">Andernfalls sucht die automatische Updateprüfung standardmäßig alle 10 Stunden nach Updates.</span><span class="sxs-lookup"><span data-stu-id="d9dee-420">Otherwise, by default, auto-update checks for updates every 10 hours.</span></span>

  <span data-ttu-id="d9dee-421">Wenn Sie alle automatischen Updateprüfungen deaktivieren möchten, setzen Sie den Wert auf 0 (nicht empfohlen).</span><span class="sxs-lookup"><span data-stu-id="d9dee-421">If you want to disable all auto-update checks, set the value to 0 (not recommended).</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="d9dee-422">Windows-Informationen und -Einstellungen</span><span class="sxs-lookup"><span data-stu-id="d9dee-422">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="d9dee-423">Informationen zur Gruppenrichtlinie (ADMX)</span><span class="sxs-lookup"><span data-stu-id="d9dee-423">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="d9dee-424">Eindeutiger Name der GP: AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="d9dee-424">GP unique name: AutoUpdateCheckPeriodMinutes</span></span>
- <span data-ttu-id="d9dee-425">GP-Name: Überschreibung des Überprüfungszeitraums für automatische Updates</span><span class="sxs-lookup"><span data-stu-id="d9dee-425">GP name: Auto-update check period override</span></span>
- <span data-ttu-id="d9dee-426">GP-Pfad: Administrative Vorlagen/Microsoft Edge Update/Einstellungen</span><span class="sxs-lookup"><span data-stu-id="d9dee-426">GP path: Administrative Templates/Microsoft Edge Update/Preferences</span></span>
- <span data-ttu-id="d9dee-427">Name der GP-ADMX-Datei: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="d9dee-427">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="d9dee-428">Windows-Registrierungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="d9dee-428">Windows Registry Settings</span></span>
- <span data-ttu-id="d9dee-429">Pfad: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="d9dee-429">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="d9dee-430">Name des Wertes: AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="d9dee-430">Value Name: AutoUpdateCheckPeriodMinutes</span></span>
- <span data-ttu-id="d9dee-431">Werttyp: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="d9dee-431">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="d9dee-432">Beispielwert:</span><span class="sxs-lookup"><span data-stu-id="d9dee-432">Example value:</span></span>
```
0x00000578
```
[<span data-ttu-id="d9dee-433">Zurück zum Anfang</span><span class="sxs-lookup"><span data-stu-id="d9dee-433">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="updatessuppressed"></a><span data-ttu-id="d9dee-434">UpdatesSuppressed</span><span class="sxs-lookup"><span data-stu-id="d9dee-434">UpdatesSuppressed</span></span>
#### <a name="time-period-in-each-day-to-suppress-auto-update-check"></a><span data-ttu-id="d9dee-435">Zeitraum in jedem Tag zum Unterdrücken der automatischen Überprüfung auf Updates</span><span class="sxs-lookup"><span data-stu-id="d9dee-435">Time period in each day to suppress auto-update check</span></span>
><span data-ttu-id="d9dee-436">Microsoft Edge Update 1.3.33.5 und höher</span><span class="sxs-lookup"><span data-stu-id="d9dee-436">Microsoft Edge Update 1.3.33.5 and later</span></span>

#### <a name="description"></a><span data-ttu-id="d9dee-437">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d9dee-437">Description</span></span>
<span data-ttu-id="d9dee-438">Wenn Sie diese Richtlinie aktivieren, werden die Updateprüfungen jeden Tag ab Stunde:Minute für einen Zeitraum der Dauer (in Minuten) unterdrückt.</span><span class="sxs-lookup"><span data-stu-id="d9dee-438">If you enable this policy, update checks are suppressed each day starting at Hour:Minute for a period of Duration (in minutes).</span></span> <span data-ttu-id="d9dee-439">Die Dauer ist von der Sommerzeit nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="d9dee-439">Duration isn't affected by daylight saving time.</span></span> <span data-ttu-id="d9dee-440">Wenn die Startzeit z. B. 22:00 lautet und die Dauer 480 Minuten beträgt, werden Updates genau 8 Stunden lang unterdrückt, unabhängig davon, ob die Sommerzeit in diesem Zeitraum beginnt oder endet.</span><span class="sxs-lookup"><span data-stu-id="d9dee-440">For example, if the start time is 22:00 and the duration is 480 minutes, updates will be suppressed for exactly 8 hours, regardless of whether daylight saving time starts or ends during this period.</span></span>

  <span data-ttu-id="d9dee-441">Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, werden die Updateprüfungen während eines bestimmten Zeitraums nicht unterdrückt.</span><span class="sxs-lookup"><span data-stu-id="d9dee-441">If you disable or don't configure this policy, update checks aren't suppressed during any specific period.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="d9dee-442">Windows-Informationen und -Einstellungen</span><span class="sxs-lookup"><span data-stu-id="d9dee-442">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="d9dee-443">Informationen zur Gruppenrichtlinie (ADMX)</span><span class="sxs-lookup"><span data-stu-id="d9dee-443">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="d9dee-444">Eindeutiger Name der GP: UpdatesSuppressed</span><span class="sxs-lookup"><span data-stu-id="d9dee-444">GP unique name: UpdatesSuppressed</span></span>
- <span data-ttu-id="d9dee-445">GP-Name: Zeitraum in jedem Tag zum Unterdrücken der automatischen Überprüfung auf Updates</span><span class="sxs-lookup"><span data-stu-id="d9dee-445">GP name: Time period in each day to suppress auto-update check</span></span>
  - <span data-ttu-id="d9dee-446">Optionen {Stunde, Minute, Dauer}</span><span class="sxs-lookup"><span data-stu-id="d9dee-446">Options { Hour, Minute, Duration }</span></span>
- <span data-ttu-id="d9dee-447">GP-Pfad: Administrative Vorlagen/Microsoft Edge Update/Einstellungen</span><span class="sxs-lookup"><span data-stu-id="d9dee-447">GP path: Administrative Templates/Microsoft Edge Update/Preferences</span></span>
- <span data-ttu-id="d9dee-448">Name der GP-ADMX-Datei: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="d9dee-448">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="d9dee-449">Windows-Registrierungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="d9dee-449">Windows Registry Settings</span></span>
- <span data-ttu-id="d9dee-450">Pfad: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="d9dee-450">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="d9dee-451">Name des Wertes:</span><span class="sxs-lookup"><span data-stu-id="d9dee-451">Value Name:</span></span> 
  - <span data-ttu-id="d9dee-452">UpdatesSuppressedDurationMin</span><span class="sxs-lookup"><span data-stu-id="d9dee-452">UpdatesSuppressedDurationMin</span></span>
  - <span data-ttu-id="d9dee-453">UpdatesSuppressedStartHour</span><span class="sxs-lookup"><span data-stu-id="d9dee-453">UpdatesSuppressedStartHour</span></span>
  - <span data-ttu-id="d9dee-454">UpdatesSuppressedStartMin</span><span class="sxs-lookup"><span data-stu-id="d9dee-454">UpdatesSuppressedStartMin</span></span>
- <span data-ttu-id="d9dee-455">Werttyp: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="d9dee-455">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="d9dee-456">Beispielwert:</span><span class="sxs-lookup"><span data-stu-id="d9dee-456">Example value:</span></span>
```
duration   : 0x0000003c
start hour : 0x00000001
start min  : 0x00000002
```
[<span data-ttu-id="d9dee-457">Zurück zum Anfang</span><span class="sxs-lookup"><span data-stu-id="d9dee-457">Back to top</span></span>](#microsoft-edge---update-policies)


## <a name="proxy-server-policies"></a><span data-ttu-id="d9dee-458">Proxyserver-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="d9dee-458">Proxy Server policies</span></span>

[<span data-ttu-id="d9dee-459">Zurück zum Anfang</span><span class="sxs-lookup"><span data-stu-id="d9dee-459">Back to top</span></span>](#microsoft-edge---update-policies)
### <a name="proxymode"></a><span data-ttu-id="d9dee-460">ProxyMode</span><span class="sxs-lookup"><span data-stu-id="d9dee-460">ProxyMode</span></span>
#### <a name="choose-how-to-specify-proxy-server-settings"></a><span data-ttu-id="d9dee-461">Möglichkeit zur Angabe der Proxyservereinstellungen wählen</span><span class="sxs-lookup"><span data-stu-id="d9dee-461">Choose how to specify proxy server settings</span></span>
><span data-ttu-id="d9dee-462">Microsoft Edge Update 1.3.21.81 und höher</span><span class="sxs-lookup"><span data-stu-id="d9dee-462">Microsoft Edge Update 1.3.21.81 and later</span></span>

#### <a name="description"></a><span data-ttu-id="d9dee-463">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d9dee-463">Description</span></span>
<span data-ttu-id="d9dee-464">Mit dieser Option können Sie die Proxyserver-Einstellungen angeben, die von Microsoft Edge Update verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d9dee-464">Allows you to specify the proxy server settings that are used by Microsoft Edge Update.</span></span>

  <span data-ttu-id="d9dee-465">Wenn Sie diese Richtlinie aktivieren, können Sie zwischen den folgenden Proxyserveroptionen wählen:</span><span class="sxs-lookup"><span data-stu-id="d9dee-465">If you enable this policy, you can choose between the following proxy server options:</span></span>
   - <span data-ttu-id="d9dee-466">Wenn Sie niemals einen Proxyserver verwenden und immer eine direkte Verbindung herstellen, werden alle anderen Optionen ignoriert.</span><span class="sxs-lookup"><span data-stu-id="d9dee-466">If you choose to never use a proxy server and always connect directly, all other options are ignored.</span></span>
   - <span data-ttu-id="d9dee-467">Wenn Sie die System-Proxyeinstellungen verwenden oder den Proxyserver automatisch erkennen möchten, werden alle anderen Optionen ignoriert.</span><span class="sxs-lookup"><span data-stu-id="d9dee-467">If you choose to use system proxy settings or auto-detect the proxy server, all other options are ignored.</span></span>
   - <span data-ttu-id="d9dee-468">Wenn Sie den Proxymodus für feste Server auswählen, können Sie unter '[Adresse oder URL des Proxyservers](#proxyserver)' weitere Optionen angeben.</span><span class="sxs-lookup"><span data-stu-id="d9dee-468">If you choose fixed server proxy mode, you can specify further options in '[Address or URL of proxy server](#proxyserver)' policy.</span></span>
   - <span data-ttu-id="d9dee-469">Wenn Sie ein PAC-Proxyskript verwenden, müssen Sie die URL für das Skript unter '[URL zu einer PAC-Proxydatei](#proxypacurl)' angeben.</span><span class="sxs-lookup"><span data-stu-id="d9dee-469">If you choose to use a .pac proxy script, you must specify the URL for the script in '[URL to a proxy .pac file](#proxypacurl)' policy.</span></span>

  <span data-ttu-id="d9dee-470">Wenn Sie diese Richtlinie aktivieren, können Benutzer in Ihrer Organisation die Proxyeinstellungen in Microsoft Edge Update nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="d9dee-470">If you enable this policy, users in your organization can't change the proxy settings in Microsoft Edge Update.</span></span>

  <span data-ttu-id="d9dee-471">Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, werden keine Proxyservereinstellungen konfiguriert. Benutzer in Ihrer Organisation können jedoch ihre eigenen Proxyeinstellungen für Microsoft Edge Update auswählen.</span><span class="sxs-lookup"><span data-stu-id="d9dee-471">If you disable or don't configure this policy, no proxy server settings are configured, but users in your organization can choose their own proxy settings for Microsoft Edge Update.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="d9dee-472">Windows-Informationen und -Einstellungen</span><span class="sxs-lookup"><span data-stu-id="d9dee-472">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="d9dee-473">Informationen zur Gruppenrichtlinie (ADMX)</span><span class="sxs-lookup"><span data-stu-id="d9dee-473">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="d9dee-474">Eindeutiger Name der GP: ProxyMode</span><span class="sxs-lookup"><span data-stu-id="d9dee-474">GP unique name: ProxyMode</span></span>
- <span data-ttu-id="d9dee-475">GP-Name: Möglichkeit zur Angabe der Proxyservereinstellungen wählen</span><span class="sxs-lookup"><span data-stu-id="d9dee-475">GP name: Choose how to specify proxy server settings</span></span>
- <span data-ttu-id="d9dee-476">GP-Pfad: Administrative Vorlagen/Microsoft Edge Update/Proxyserver</span><span class="sxs-lookup"><span data-stu-id="d9dee-476">GP path: Administrative Templates/Microsoft Edge Update/Proxy Server</span></span>
- <span data-ttu-id="d9dee-477">Name der GP-ADMX-Datei: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="d9dee-477">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="d9dee-478">Windows-Registrierungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="d9dee-478">Windows Registry Settings</span></span>
- <span data-ttu-id="d9dee-479">Pfad: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="d9dee-479">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="d9dee-480">Name des Wertes: ProxyMode</span><span class="sxs-lookup"><span data-stu-id="d9dee-480">Value Name: ProxyMode</span></span>
- <span data-ttu-id="d9dee-481">Werttyp: REG_SZ</span><span class="sxs-lookup"><span data-stu-id="d9dee-481">Value Type: REG_SZ</span></span>
##### <a name="example-value"></a><span data-ttu-id="d9dee-482">Beispielwert:</span><span class="sxs-lookup"><span data-stu-id="d9dee-482">Example value:</span></span>
```
fixed_servers
```
[<span data-ttu-id="d9dee-483">Zurück zum Anfang</span><span class="sxs-lookup"><span data-stu-id="d9dee-483">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="proxypacurl"></a><span data-ttu-id="d9dee-484">ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="d9dee-484">ProxyPacUrl</span></span>
#### <a name="url-to-a-proxy-pac-file"></a><span data-ttu-id="d9dee-485">URL zu einer PAC-Proxydatei</span><span class="sxs-lookup"><span data-stu-id="d9dee-485">URL to a proxy .pac file</span></span>
><span data-ttu-id="d9dee-486">Microsoft Edge Update 1.3.21.81 und höher</span><span class="sxs-lookup"><span data-stu-id="d9dee-486">Microsoft Edge Update 1.3.21.81 and later</span></span>

#### <a name="description"></a><span data-ttu-id="d9dee-487">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d9dee-487">Description</span></span>
<span data-ttu-id="d9dee-488">Ermöglicht die Angabe einer URL für eine PAC-Datei (Proxy Auto-Config).</span><span class="sxs-lookup"><span data-stu-id="d9dee-488">Allows you to specify a URL for a proxy auto-config (PAC) file.</span></span>

  <span data-ttu-id="d9dee-489">Wenn Sie diese Richtlinie aktivieren, können Sie eine URL für eine PAC-Datei angeben, um zu automatisieren, wie Microsoft Edge Update den geeigneten Proxyserver zum Abrufen einer bestimmten Website auswählt.</span><span class="sxs-lookup"><span data-stu-id="d9dee-489">If you enable this policy, you can specify a URL for a PAC file to automate how Microsoft Edge Update selects the appropriate proxy server for fetching a particular website.</span></span>

  <span data-ttu-id="d9dee-490">Diese Richtlinie wird nur angewendet, wenn Sie in der Richtlinie '[Möglichkeit zur Angabe der Proxyservereinstellungen wählen](#proxymode)' manuelle Proxyeinstellungen festgelegt haben.</span><span class="sxs-lookup"><span data-stu-id="d9dee-490">This policy is applied only if you have specified manual proxy settings in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>

  <span data-ttu-id="d9dee-491">Konfigurieren Sie diese Richtlinie nicht, wenn Sie eine andere Proxy-Einstellung als manuell in der Richtlinie '[Möglichkeit zur Angabe der Proxyservereinstellungen wählen](#proxymode)' ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="d9dee-491">Don't configure this policy if you have selected a proxy setting other than manual in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="d9dee-492">Windows-Informationen und -Einstellungen</span><span class="sxs-lookup"><span data-stu-id="d9dee-492">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="d9dee-493">Informationen zur Gruppenrichtlinie (ADMX)</span><span class="sxs-lookup"><span data-stu-id="d9dee-493">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="d9dee-494">Eindeutiger Name der GP: ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="d9dee-494">GP unique name: ProxyPacUrl</span></span>
- <span data-ttu-id="d9dee-495">GP-Name: URL zu einer PAC-Proxydatei</span><span class="sxs-lookup"><span data-stu-id="d9dee-495">GP name: URL to a proxy .pac file</span></span>
- <span data-ttu-id="d9dee-496">GP-Pfad: Administrative Vorlagen/Microsoft Edge Update/Proxyserver</span><span class="sxs-lookup"><span data-stu-id="d9dee-496">GP path: Administrative Templates/Microsoft Edge Update/Proxy Server</span></span>
- <span data-ttu-id="d9dee-497">Name der GP-ADMX-Datei: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="d9dee-497">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="d9dee-498">Windows-Registrierungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="d9dee-498">Windows Registry Settings</span></span>
- <span data-ttu-id="d9dee-499">Pfad: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="d9dee-499">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="d9dee-500">Name des Wertes: ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="d9dee-500">Value Name: ProxyPacUrl</span></span>
- <span data-ttu-id="d9dee-501">Werttyp: REG_SZ</span><span class="sxs-lookup"><span data-stu-id="d9dee-501">Value Type: REG_SZ</span></span>
##### <a name="example-value"></a><span data-ttu-id="d9dee-502">Beispielwert:</span><span class="sxs-lookup"><span data-stu-id="d9dee-502">Example value:</span></span>
```
https://www.microsoft.com
```
[<span data-ttu-id="d9dee-503">Zurück zum Anfang</span><span class="sxs-lookup"><span data-stu-id="d9dee-503">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="proxyserver"></a><span data-ttu-id="d9dee-504">ProxyServer</span><span class="sxs-lookup"><span data-stu-id="d9dee-504">ProxyServer</span></span>
#### <a name="address-or-url-of-proxy-server"></a><span data-ttu-id="d9dee-505">Adresse oder URL des Proxyservers</span><span class="sxs-lookup"><span data-stu-id="d9dee-505">Address or URL of proxy server</span></span>
><span data-ttu-id="d9dee-506">Microsoft Edge Update 1.3.21.81 und höher</span><span class="sxs-lookup"><span data-stu-id="d9dee-506">Microsoft Edge Update 1.3.21.81 and later</span></span>

#### <a name="description"></a><span data-ttu-id="d9dee-507">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d9dee-507">Description</span></span>
<span data-ttu-id="d9dee-508">Hier können Sie die URL des Proxy-Servers angeben, den Microsoft Edge Update verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="d9dee-508">Allows you to specify the URL of the proxy server for Microsoft Edge Update to use.</span></span>

  <span data-ttu-id="d9dee-509">Wenn Sie diese Richtlinie aktivieren, können Sie die Proxyserver-URL festlegen, die von Microsoft Edge Update in Ihrer Organisation verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d9dee-509">If you enable this policy, you can set the proxy server URL used by Microsoft Edge Update in your organization.</span></span>

  <span data-ttu-id="d9dee-510">Diese Richtlinie wird nur angewendet, wenn Sie in der Richtlinie '[Möglichkeit zur Angabe der Proxyservereinstellungen wählen](#proxymode)' manuelle Proxyeinstellungen ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="d9dee-510">This policy is applied only if you have selected manual proxy settings in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>

  <span data-ttu-id="d9dee-511">Konfigurieren Sie diese Richtlinie nicht, wenn Sie eine andere Proxy-Einstellung als manuell in der Richtlinie '[Möglichkeit zur Angabe der Proxyservereinstellungen wählen](#proxymode)' ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="d9dee-511">Don't configure this policy if you have selected a proxy setting other than manual in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="d9dee-512">Windows-Informationen und -Einstellungen</span><span class="sxs-lookup"><span data-stu-id="d9dee-512">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="d9dee-513">Informationen zur Gruppenrichtlinie (ADMX)</span><span class="sxs-lookup"><span data-stu-id="d9dee-513">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="d9dee-514">Eindeutiger Name der GP: ProxyServer</span><span class="sxs-lookup"><span data-stu-id="d9dee-514">GP unique name: ProxyServer</span></span>
- <span data-ttu-id="d9dee-515">GP-Name: Adresse oder URL des Proxyservers</span><span class="sxs-lookup"><span data-stu-id="d9dee-515">GP name: Address or URL of proxy server</span></span>
- <span data-ttu-id="d9dee-516">GP-Pfad: Administrative Vorlagen/Microsoft Edge Update/Proxyserver</span><span class="sxs-lookup"><span data-stu-id="d9dee-516">GP path: Administrative Templates/Microsoft Edge Update/Proxy Server</span></span>
- <span data-ttu-id="d9dee-517">Name der GP-ADMX-Datei: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="d9dee-517">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="d9dee-518">Windows-Registrierungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="d9dee-518">Windows Registry Settings</span></span>
- <span data-ttu-id="d9dee-519">Pfad: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="d9dee-519">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="d9dee-520">Name des Wertes: ProxyServer</span><span class="sxs-lookup"><span data-stu-id="d9dee-520">Value Name: ProxyServer</span></span>
- <span data-ttu-id="d9dee-521">Werttyp: REG_SZ</span><span class="sxs-lookup"><span data-stu-id="d9dee-521">Value Type: REG_SZ</span></span>
##### <a name="example-value"></a><span data-ttu-id="d9dee-522">Beispielwert:</span><span class="sxs-lookup"><span data-stu-id="d9dee-522">Example value:</span></span>
```
https://www.microsoft.com
```
[<span data-ttu-id="d9dee-523">Zurück zum Anfang</span><span class="sxs-lookup"><span data-stu-id="d9dee-523">Back to top</span></span>](#microsoft-edge---update-policies)


## <a name="microsoft-edge-webview-policies"></a><span data-ttu-id="d9dee-524">Microsoft Edge WebView-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="d9dee-524">Microsoft Edge WebView policies</span></span>

[<span data-ttu-id="d9dee-525">Zurück zum Anfang</span><span class="sxs-lookup"><span data-stu-id="d9dee-525">Back to top</span></span>](#microsoft-edge---update-policies)
### <a name="install-webview"></a><span data-ttu-id="d9dee-526">Installieren (WebView)</span><span class="sxs-lookup"><span data-stu-id="d9dee-526">Install (WebView)</span></span>
#### <a name="allow-installation"></a><span data-ttu-id="d9dee-527">Installation zulassen</span><span class="sxs-lookup"><span data-stu-id="d9dee-527">Allow installation</span></span>
><span data-ttu-id="d9dee-528">Microsoft Edge Update 1.3.127.1 und höher</span><span class="sxs-lookup"><span data-stu-id="d9dee-528">Microsoft Edge Update 1.3.127.1 and later</span></span>

#### <a name="description"></a><span data-ttu-id="d9dee-529">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d9dee-529">Description</span></span>
<span data-ttu-id="d9dee-530">Hiermit können Sie festlegen, ob Microsoft Edge WebView mithilfe von Microsoft Edge Update installiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="d9dee-530">Lets you specify whether Microsoft Edge WebView can be installed using Microsoft Edge Update.</span></span>

  - <span data-ttu-id="d9dee-531">Wenn Sie diese Richtlinie aktivieren, können Benutzer Microsoft Edge über Microsoft Edge Update installieren.</span><span class="sxs-lookup"><span data-stu-id="d9dee-531">If you enable this policy, users can install Microsoft Edge WebView through Microsoft Edge Update.</span></span>
  - <span data-ttu-id="d9dee-532">Wenn Sie diese Richtlinie deaktivieren, können Benutzer Microsoft Edge nicht über Microsoft Edge Update installieren.</span><span class="sxs-lookup"><span data-stu-id="d9dee-532">If you disable this policy, users cannot install Microsoft Edge WebView through Microsoft Edge Update.</span></span>
  - <span data-ttu-id="d9dee-533">Wenn Sie diese Richtlinie nicht konfigurieren, bestimmt die Richtlinienkonfiguration "[Standardinstallation zulassen](#installdefault)", ob Benutzer Microsoft Edge WebView über Microsoft Edge Update installieren können.</span><span class="sxs-lookup"><span data-stu-id="d9dee-533">If you don't configure this policy, the '[Allow installation default](#installdefault)' policy configuration determines whether users can install Microsoft Edge WebView through Microsoft Edge Update.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="d9dee-534">Windows-Informationen und -Einstellungen</span><span class="sxs-lookup"><span data-stu-id="d9dee-534">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="d9dee-535">Informationen zur Gruppenrichtlinie (ADMX)</span><span class="sxs-lookup"><span data-stu-id="d9dee-535">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="d9dee-536">Eindeutiger Name der GP: Install</span><span class="sxs-lookup"><span data-stu-id="d9dee-536">GP unique name: Install</span></span>
- <span data-ttu-id="d9dee-537">GP-Name: Installation zulassen</span><span class="sxs-lookup"><span data-stu-id="d9dee-537">GP name: Allow installation</span></span>
- <span data-ttu-id="d9dee-538">GP-Pfad: Administrative Vorlagen/Microsoft Edge Update/Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="d9dee-538">GP path: Administrative Templates/Microsoft Edge Update/Microsoft Edge WebView</span></span>
- <span data-ttu-id="d9dee-539">Name der GP-ADMX-Datei: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="d9dee-539">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="d9dee-540">Windows-Registrierungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="d9dee-540">Windows Registry Settings</span></span>
- <span data-ttu-id="d9dee-541">Pfad: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="d9dee-541">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="d9dee-542">Name des Wertes:</span><span class="sxs-lookup"><span data-stu-id="d9dee-542">Value Name:</span></span> 
  - <span data-ttu-id="d9dee-543">Install{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}</span><span class="sxs-lookup"><span data-stu-id="d9dee-543">Install{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}</span></span>
- <span data-ttu-id="d9dee-544">Werttyp: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="d9dee-544">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="d9dee-545">Beispielwert:</span><span class="sxs-lookup"><span data-stu-id="d9dee-545">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="d9dee-546">Zurück zum Anfang</span><span class="sxs-lookup"><span data-stu-id="d9dee-546">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="update-webview"></a><span data-ttu-id="d9dee-547">Update (WebView)</span><span class="sxs-lookup"><span data-stu-id="d9dee-547">Update (WebView)</span></span>
#### <a name="update-policy-override"></a><span data-ttu-id="d9dee-548">Außerkraftsetzung von Updaterichtlinien</span><span class="sxs-lookup"><span data-stu-id="d9dee-548">Update policy override</span></span>
><span data-ttu-id="d9dee-549">Microsoft Edge Update 1.3.127.1 und höher</span><span class="sxs-lookup"><span data-stu-id="d9dee-549">Microsoft Edge Update 1.3.127.1 and later</span></span>

#### <a name="description"></a><span data-ttu-id="d9dee-550">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d9dee-550">Description</span></span>
<span data-ttu-id="d9dee-551">Sie können angeben, ob automatische Updates für Microsoft Edge WebView aktiviert sind oder nicht.</span><span class="sxs-lookup"><span data-stu-id="d9dee-551">Lets you specify whether or not automatic updates are enabled for Microsoft Edge WebView.</span></span> <span data-ttu-id="d9dee-552">Microsoft Edge WebView ist eine Komponente, die von Anwendungen zum Anzeigen von Webinhalten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d9dee-552">Microsoft Edge WebView is a component used by applications to display web content.</span></span>
<span data-ttu-id="d9dee-553">"Automatische Updates" ist standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="d9dee-553">Automatic updates are enabled by default.</span></span> <span data-ttu-id="d9dee-554">Durch das Deaktivieren von automatischen Updates für Microsoft Edge WebView können Kompatibilitätsprobleme mit Anwendungen verursacht werden, die von dieser Komponente abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="d9dee-554">Disabling automatic updates for Microsoft Edge WebView might cause compatibility issues with applications that depend on this component.</span></span>

  <span data-ttu-id="d9dee-555">Wenn Sie diese Richtlinie aktivieren, verarbeitet Microsoft Edge Update die Microsoft Edge WebView-Updates entsprechend der Konfiguration der folgenden Optionen:</span><span class="sxs-lookup"><span data-stu-id="d9dee-555">If you enable this policy, Microsoft Edge Update handles Microsoft Edge WebView updates according to how you configure the following options:</span></span>
  - <span data-ttu-id="d9dee-556">Updates immer zulassen: Updates werden automatisch heruntergeladen und angewendet</span><span class="sxs-lookup"><span data-stu-id="d9dee-556">Always allow updates: Updates are automatically downloaded and applied</span></span>
  - <span data-ttu-id="d9dee-557">Updates deaktiviert: Updates werden nie heruntergeladen und angewendet</span><span class="sxs-lookup"><span data-stu-id="d9dee-557">Updates disabled: Updates are never downloaded or applied</span></span>

  <span data-ttu-id="d9dee-558">Wenn Sie diese Richtlinie nicht aktivieren, werden Updates automatisch heruntergeladen und angewendet.</span><span class="sxs-lookup"><span data-stu-id="d9dee-558">If you don't enable this policy, updates are automatically downloaded and applied.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="d9dee-559">Windows-Informationen und -Einstellungen</span><span class="sxs-lookup"><span data-stu-id="d9dee-559">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="d9dee-560">Informationen zur Gruppenrichtlinie (ADMX)</span><span class="sxs-lookup"><span data-stu-id="d9dee-560">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="d9dee-561">Eindeutiger Name der GP: Update</span><span class="sxs-lookup"><span data-stu-id="d9dee-561">GP unique name: Update</span></span>
- <span data-ttu-id="d9dee-562">GP-Name: Außerkraftsetzung von Updaterichtlinien</span><span class="sxs-lookup"><span data-stu-id="d9dee-562">GP name: Update policy override</span></span>
- <span data-ttu-id="d9dee-563">GP-Pfad: Administrative Vorlagen/Microsoft Edge Update/Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="d9dee-563">GP path: Administrative Templates/Microsoft Edge Update/Microsoft Edge WebView</span></span>
- <span data-ttu-id="d9dee-564">Name der GP-ADMX-Datei: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="d9dee-564">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="d9dee-565">Windows-Registrierungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="d9dee-565">Windows Registry Settings</span></span>
- <span data-ttu-id="d9dee-566">Pfad: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="d9dee-566">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="d9dee-567">Name des Wertes:</span><span class="sxs-lookup"><span data-stu-id="d9dee-567">Value Name:</span></span> 
  - <span data-ttu-id="d9dee-568">Update{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}</span><span class="sxs-lookup"><span data-stu-id="d9dee-568">Update{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}</span></span>
- <span data-ttu-id="d9dee-569">Werttyp: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="d9dee-569">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="d9dee-570">Beispielwert:</span><span class="sxs-lookup"><span data-stu-id="d9dee-570">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="d9dee-571">Zurück zum Anfang</span><span class="sxs-lookup"><span data-stu-id="d9dee-571">Back to top</span></span>](#microsoft-edge---update-policies)


## <a name="see-also"></a><span data-ttu-id="d9dee-572">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d9dee-572">See also</span></span>
  - [<span data-ttu-id="d9dee-573">Konfigurieren von Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="d9dee-573">Configuring Microsoft Edge</span></span>](configure-microsoft-edge.md)
  - [<span data-ttu-id="d9dee-574">Microsoft Edge Enterprise-Angebotsseite</span><span class="sxs-lookup"><span data-stu-id="d9dee-574">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
