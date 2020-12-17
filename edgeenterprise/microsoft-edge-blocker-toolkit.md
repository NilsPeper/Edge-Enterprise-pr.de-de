---
title: Blocker Toolkit zum Deaktivieren der automatischen Übermittlung von Microsoft Edge
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 12/16/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Blocker Toolkit zum Deaktivieren der automatischen Übermittlung von Microsoft Edge
ms.openlocfilehash: 9fb97d2dfec4822f8ce76dc3e37b85118c6572ad
ms.sourcegitcommit: 606282995b466a968bab40c16005a6653323c763
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/16/2020
ms.locfileid: "11229616"
---
# <span data-ttu-id="d7feb-103">Blocker Toolkit zum Deaktivieren der automatischen Bereitstellung von Microsoft Edge (Chromium-basiert)</span><span class="sxs-lookup"><span data-stu-id="d7feb-103">Blocker Toolkit to disable automatic delivery of Microsoft Edge (Chromium-based)</span></span>

<span data-ttu-id="d7feb-104">In diesem Artikel wird das Blocker Toolkit zum Deaktivieren der automatischen Übermittlung und Installation von Microsoft Edge beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d7feb-104">This article describes the Blocker Toolkit for disabling automatic delivery and installation of Microsoft Edge.</span></span>

<span data-ttu-id="d7feb-105">In diesem Artikel wurden die folgenden Aktualisierungen vorgenommen:</span><span class="sxs-lookup"><span data-stu-id="d7feb-105">The following updates have been made to this article:</span></span>

- <span data-ttu-id="d7feb-106">**09.01.2020** Weitere Informationen zu Geräten, für die Sie möglicherweise das Blocker Toolkit verwenden müssen, wurden hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d7feb-106">**01/09/2020** with more information about devices that might require you to use the Blocker Toolkit</span></span>
- <span data-ttu-id="d7feb-107">**28.2.2020** „Von MDM verwaltet“ wurde aus den Kriterien von Geräten entfernt, die von diesem automatischen Update ausgeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d7feb-107">**2/28/2020** to remove "MDM managed" from the criteria of devices to be excluded from this automatic update</span></span>
- <span data-ttu-id="d7feb-108">**30.6.2020** Aktualisierung, um widerzuspiegeln, dass alle verbundenen Windows Update-Geräte in den Geltungsbereich für den Empfang dieses Updates fallen (frühestens ab 30.7.2020 wirksam)</span><span class="sxs-lookup"><span data-stu-id="d7feb-108">**6/30/2020** to reflect that all Windows Update connected devices are in scope to receive this update (effective no sooner than 7/30/2020)</span></span>
- <span data-ttu-id="d7feb-109">**10.12.2020** Aktualisierungen zur Erläuterung von Situationen vor 20H2, in denen die Einstellungen des Blocker Toolkits ignoriert werden</span><span class="sxs-lookup"><span data-stu-id="d7feb-109">**12/10/2020** to explain pre 20H2 situations in which the Blocker Toolkit settings will be ignored</span></span>

> [!NOTE]
> <span data-ttu-id="d7feb-110">Dieser Artikel bezieht sich auf den Microsoft Edge Stable Channel.</span><span class="sxs-lookup"><span data-stu-id="d7feb-110">This applies to Microsoft Edge Stable channel.</span></span>

## <span data-ttu-id="d7feb-111">Übersicht</span><span class="sxs-lookup"><span data-stu-id="d7feb-111">Overview</span></span>

<span data-ttu-id="d7feb-112">Um unseren Kunden zu helfen, sicherer und aktueller zu werden, wird Microsoft den Browser MicrosoftEdge (Chromium-basiert) an alle mit WindowsUpdate verbundenen Geräte unter Windows10 (ab Version1803) verteilen.</span><span class="sxs-lookup"><span data-stu-id="d7feb-112">To help our customers become more secure and up-to-date, Microsoft will distribute Microsoft Edge (Chromium-based) to all Windows Update-connected devices running Windows 10 version 1803 and newer.</span></span> <span data-ttu-id="d7feb-113">Dieser Prozess startet nach dem 15.Januar 2020. An diesem Datum stehen weitere Informationen zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="d7feb-113">This process will start after January 15, 2020 and more information will be available on that date.</span></span>

<span data-ttu-id="d7feb-114">Das Blocker Toolkit richtet sich an Organisationen, die die automatische Bereitstellung von MicrosoftEdge (Chromium-basiert) auf mit Windows Update verbundenen Geräten unter Windows10 (ab Version1803) blockieren möchten.</span><span class="sxs-lookup"><span data-stu-id="d7feb-114">The Blocker Toolkit is intended for organizations that would like to block automatic delivery of Microsoft Edge (Chromium-based) to Windows Updated-connected devices running Windows 10 version 1803 and newer.</span></span> <span data-ttu-id="d7feb-115">Von Windows Server Update Services (WSUS) oder Windows Update for Business (WUfB) verwaltete Geräte werden von diesem automatischen Windows-Update ausgeschlossen, können das neue MicrosoftEdge (Chromium-basiert) aber über Ihre Organisation erhalten.</span><span class="sxs-lookup"><span data-stu-id="d7feb-115">Devices that are Windows Server Update Services (WSUS) or Windows Update for Business (WUfB) managed will be excluded from this automatic Windows Update, but may receive the new Microsoft Edge (Chromium-based) through their organization.</span></span>

**<span data-ttu-id="d7feb-116">Beachten Sie unbedingt Folgendes:</span><span class="sxs-lookup"><span data-stu-id="d7feb-116">It's important to note that:</span></span>**

- <span data-ttu-id="d7feb-117">Das Blocker Toolkit kann nicht verhindern, dass Benutzer Microsoft Edge (Chromium-basiert) manuell aus dem Internet oder von externen Medien herunterladen und installieren.</span><span class="sxs-lookup"><span data-stu-id="d7feb-117">The Blocker Toolkit will not prevent users from manually installing Microsoft Edge (Chromium-based) from Internet download, or from external media.</span></span>
- <span data-ttu-id="d7feb-118">Organisationen mit Updates, die über Windows Update for Business (WUfB) verwaltet werden, erhalten dieses Update nicht automatisch und müssen das Blocker Toolkit nicht bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="d7feb-118">Organizations with updates managed through Windows Update for Business (WUfB) will not automatically receive this update and do not need to deploy the blocker toolkit.</span></span>
- <span data-ttu-id="d7feb-119">Organisationen mit Umgebungen, die mit einer Update-Verwaltungslösung wie Windows Server Update Services (WSUS) oder System Center Konfigurations-Manager (SCCM) verwaltet werden, müssen das Blocker Toolkit nicht bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="d7feb-119">Organizations with environments managed with an update management solution such as Windows Server Update Services (WSUS) or System Center Configuration Manager (SCCM) do not have to deploy the Blocker Toolkit.</span></span> <span data-ttu-id="d7feb-120">Sie können diese Produkte verwenden, um die Bereitstellung von Updates, die über Windows Update und Microsoft Update veröffentlicht wurden, einschließlich [Update in WSUS für das neue Microsoft Edge](https://support.microsoft.com/help/4584642/update-in-wsus-for-the-new-microsoft-edge), in ihrer Umgebung vollständig zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="d7feb-120">They can use those products to fully manage deployment of updates released through Windows Update and Microsoft Update, including the [Update in WSUS for the new Microsoft Edge](https://support.microsoft.com/help/4584642/update-in-wsus-for-the-new-microsoft-edge), within their environment.</span></span>
- <span data-ttu-id="d7feb-121">Dieses Update ist ein eigenständiges Update (also nicht Teil des monatlichen kumulativen Updates), damit die Unternehmenskunden Flexibilität und maximale Kontrolle über die Bereitstellung dieses Updates haben.</span><span class="sxs-lookup"><span data-stu-id="d7feb-121">This update is a stand-alone update (not part of the monthly cumulative update) to give Enterprise customers flexibility and maximum control over deploying this update.</span></span>
- <span data-ttu-id="d7feb-122">Das neue MicrosoftEdge (Chromium-basiert) wird im Rahmen des Windows10-Featureupdates, Version20H2, in der zweiten Hälfte von 2020 einbezogen.</span><span class="sxs-lookup"><span data-stu-id="d7feb-122">The new Microsoft Edge (Chromium-based) is included as part of the Windows 10, version 20H2 feature update in the second half of 2020.</span></span> <span data-ttu-id="d7feb-123">Das Blocker Toolkit wirkt sich nicht auf das Verhalten oder die Bereitstellung von 20H2 aus.</span><span class="sxs-lookup"><span data-stu-id="d7feb-123">The Blocker toolkit does not impact 20H2 behaviors or deployment.</span></span> <span data-ttu-id="d7feb-124">Weitere Informationen zu Windows10, Version20H2, finden Sie [hier](https://blogs.windows.com/windowsexperience/2020/06/16/whats-next-for-windows-10-updates/).</span><span class="sxs-lookup"><span data-stu-id="d7feb-124">See more information about Windows 10, version 20H2 [here](https://blogs.windows.com/windowsexperience/2020/06/16/whats-next-for-windows-10-updates/).</span></span>

<span data-ttu-id="d7feb-125">Sie können die ausführbare Datei des Blocker Toolkit unter [https://msedgeblockertoolkit.blob.core.windows.net/blockertoolkit/MicrosoftEdgeChromiumBlockerToolkit.exe](https://msedgeblockertoolkit.blob.core.windows.net/blockertoolkit/MicrosoftEdgeChromiumBlockerToolkit.exe) herunterladen.</span><span class="sxs-lookup"><span data-stu-id="d7feb-125">You can download the Blocker Toolkit executable file from [https://msedgeblockertoolkit.blob.core.windows.net/blockertoolkit/MicrosoftEdgeChromiumBlockerToolkit.exe](https://msedgeblockertoolkit.blob.core.windows.net/blockertoolkit/MicrosoftEdgeChromiumBlockerToolkit.exe).</span></span>

### <span data-ttu-id="d7feb-126">Toolkit-Komponenten</span><span class="sxs-lookup"><span data-stu-id="d7feb-126">Toolkit components</span></span>

<span data-ttu-id="d7feb-127">Diese Toolkit enthält die folgenden Komponenten:</span><span class="sxs-lookup"><span data-stu-id="d7feb-127">This toolkit contains the following components:</span></span>

- <span data-ttu-id="d7feb-128">Ausführbares Blocker-Skript (.CMD)</span><span class="sxs-lookup"><span data-stu-id="d7feb-128">Executable blocker script (.CMD)</span></span>
- <span data-ttu-id="d7feb-129">Administrative Vorlage für Gruppenrichtlinien (.ADMX und .ADML)</span><span class="sxs-lookup"><span data-stu-id="d7feb-129">Group Policy Administrative Template (.ADMX and .ADML)</span></span>

### <span data-ttu-id="d7feb-130">Unterstützte Betriebssysteme</span><span class="sxs-lookup"><span data-stu-id="d7feb-130">Supported Operating Systems</span></span>

<span data-ttu-id="d7feb-131">Windows 10 ab Version 1803</span><span class="sxs-lookup"><span data-stu-id="d7feb-131">Windows 10 version 1803 and newer.</span></span>

## <span data-ttu-id="d7feb-132">Blocker-Skript</span><span class="sxs-lookup"><span data-stu-id="d7feb-132">Blocker script</span></span>

<span data-ttu-id="d7feb-133">Das Skript erstellt einen Registrierungsschlüssel und setzt den zugehörigen Wert so, dass er die automatische Bereitstellung von Microsoft Edge (Chromium-basiert) auf dem lokalen Computer oder einem entfernten Zielcomputer blockiert oder entsperrt (abhängig von der verwendeten Befehlszeilenoption).</span><span class="sxs-lookup"><span data-stu-id="d7feb-133">The script creates a registry key and sets the associated value to block or unblock (depending on the command-line option used) automatic delivery of Microsoft Edge (Chromium-based) on either the local machine or a remote target machine.</span></span>

**<span data-ttu-id="d7feb-134">Registrierungsschlüssel:</span><span class="sxs-lookup"><span data-stu-id="d7feb-134">Registry key:</span></span>** `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\EdgeUpdate`<br>
**<span data-ttu-id="d7feb-135">Schlüsselwertname:</span><span class="sxs-lookup"><span data-stu-id="d7feb-135">Key value name:</span></span>** `DoNotUpdateToEdgeWithChromium`

| <span data-ttu-id="d7feb-136">Wert</span><span class="sxs-lookup"><span data-stu-id="d7feb-136">Value</span></span>                | <span data-ttu-id="d7feb-137">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="d7feb-137">Result</span></span>                         |
|----------------------|--------------------------------|
| *<span data-ttu-id="d7feb-138">Schlüssel ist nicht definiert</span><span class="sxs-lookup"><span data-stu-id="d7feb-138">Key is not defined</span></span>* | <span data-ttu-id="d7feb-139">Verteilung ist *nicht* blockiert.</span><span class="sxs-lookup"><span data-stu-id="d7feb-139">Distribution is *not* blocked.</span></span> |
| <span data-ttu-id="d7feb-140">0</span><span class="sxs-lookup"><span data-stu-id="d7feb-140">0</span></span>                    | <span data-ttu-id="d7feb-141">Verteilung ist *nicht* blockiert.</span><span class="sxs-lookup"><span data-stu-id="d7feb-141">Distribution is *not* blocked.</span></span> |
| <span data-ttu-id="d7feb-142">1</span><span class="sxs-lookup"><span data-stu-id="d7feb-142">1</span></span>                    | <span data-ttu-id="d7feb-143">Verteilung ist blockiert.</span><span class="sxs-lookup"><span data-stu-id="d7feb-143">Distribution is blocked.</span></span>       |

<span data-ttu-id="d7feb-144">Das Skript hat folgende Befehlszeilensyntax:</span><span class="sxs-lookup"><span data-stu-id="d7feb-144">The script has the following command-line syntax:</span></span><br>
`EdgeChromium_Blocker.cmd [<machine name>] [/B] [/U] [/H]`

### <span data-ttu-id="d7feb-145">Computername</span><span class="sxs-lookup"><span data-stu-id="d7feb-145">Machine name</span></span>

<span data-ttu-id="d7feb-146">Der Parameter `<machine name>` ist optional.</span><span class="sxs-lookup"><span data-stu-id="d7feb-146">The `<machine name>` parameter is optional.</span></span> <span data-ttu-id="d7feb-147">Wenn er fehlt, wird die Aktion auf dem lokalen Computer ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d7feb-147">If not specified, the action is performed on the local machine.</span></span> <span data-ttu-id="d7feb-148">Andernfalls erfolgt der Zugriff auf den Remotecomputer über die Remote-Registrierungsfunktionen des Befehls `REG`.</span><span class="sxs-lookup"><span data-stu-id="d7feb-148">Otherwise, the remote machine is accessed through the remote registry capabilities of the `REG` command.</span></span> <span data-ttu-id="d7feb-149">Wenn auf die Remoteregistrierung aufgrund von Sicherheitsberechtigungen nicht zugegriffen werden kann oder wenn der Remotecomputer nicht gefunden werden kann, wird vom Befehl `REG` eine Fehlermeldung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d7feb-149">If the remote registry can't be accessed due to security permissions or the remote machine can't be found, an error message is returned from the `REG` command.</span></span>

### <span data-ttu-id="d7feb-150">Schalter</span><span class="sxs-lookup"><span data-stu-id="d7feb-150">Switches</span></span>

<span data-ttu-id="d7feb-151">Die vom Skript verwendeten Schalter schließen sich gegenseitig aus, und nur der erste gültige Schalter eines bestimmten Befehls wird aktiviert.</span><span class="sxs-lookup"><span data-stu-id="d7feb-151">Switches used by the script are mutually exclusive and only the first valid switch from a given command is acted on.</span></span> <span data-ttu-id="d7feb-152">Das Skript kann mehrmals auf demselben Computer ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d7feb-152">The script can be run multiple times on the same machine.</span></span>

| <span data-ttu-id="d7feb-153">Schalter</span><span class="sxs-lookup"><span data-stu-id="d7feb-153">Switch</span></span>       | <span data-ttu-id="d7feb-154">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d7feb-154">Description</span></span>                              |
|--------------|------------------------------------------|
| `/B`         | <span data-ttu-id="d7feb-155">Verteilung wird blockiert</span><span class="sxs-lookup"><span data-stu-id="d7feb-155">Blocks distribution</span></span>                      |
| `/U`         | <span data-ttu-id="d7feb-156">Blockierung der Verteilung wird aufgehoben</span><span class="sxs-lookup"><span data-stu-id="d7feb-156">Unblocks distribution</span></span>                    |
| `/H` <span data-ttu-id="d7feb-157">oder</span><span class="sxs-lookup"><span data-stu-id="d7feb-157">or</span></span> `/?` | <span data-ttu-id="d7feb-158">Zeigt die folgende Zusammenfassung für Hilfe an:</span><span class="sxs-lookup"><span data-stu-id="d7feb-158">Displays the following summary help:</span></span><br>`This tool can be used to remotely block or unblock the delivery of Microsoft Edge (Chromium-based) through Automatic Updates.`<br> `Usage:`<br>`EdgeChromium_Blocker.cmd [<machine name>] [/B][/U][/H]`<br>`B = Block Microsoft Edge (Chromium-based) deployment`<br>`U = Allow Microsoft Edge (Chromium-based) deployment`<br>`H = Help`<br>`Examples:`<br>`EdgeChromium_Blocker.cmd mymachine /B (blocks delivery on machine "mymachine")`<br>`EdgeChromium_Blocker.cmd /U (unblocks delivery on the local machine)`<br> |

## <span data-ttu-id="d7feb-159">Administrative Vorlage für Gruppenrichtlinien (.ADMX- und .ADML-Dateien)</span><span class="sxs-lookup"><span data-stu-id="d7feb-159">Group Policy Administrative Template (.ADMX and .ADML files)</span></span>

<span data-ttu-id="d7feb-160">Die Verwaltungsvorlage für Gruppenrichtlinien (.ADMX- und .ADML-Dateien) ermöglicht es Administratoren, die neuen Gruppenrichtlinieneinstellungen zu importieren, um die automatische Bereitstellung von Microsoft Edge (Chromium-basiert) in ihrer Gruppenrichtlinienumgebung zu blockieren oder freizugeben. Administratoren können mit der Gruppenrichtlinie die Aktion in ihrer Umgebung systemübergreifend zentral ausführen.</span><span class="sxs-lookup"><span data-stu-id="d7feb-160">The Group Policy Administrative Template (.ADMX  and .ADML files) allows administrators to import the new Group Policy settings to block or unblock automatic delivery of Microsoft Edge (Chromium-based) into their Group Policy environment, and use Group Policy to centrally execute the action across systems in their environment.</span></span>

<span data-ttu-id="d7feb-161">Benutzer, die Windows 10 RS3 Enterprise/EDU und RS4 und neuer verwenden, finden die Richtlinie unter dem folgenden Pfad:</span><span class="sxs-lookup"><span data-stu-id="d7feb-161">Users running Windows 10 RS3 Enterprise/EDU and RS4 and newer, will see the policy under the following path:</span></span>

```
/Computer Configuration  
  /Administrative Templates
    /Classic Administrative Templates
      /Windows Components
        /Windows Update  
          /Microsoft Edge (Chromium-based) Blockers  
```

<span data-ttu-id="d7feb-162">Diese Einstellung ist nicht pro Benutzer, sondern nur als Computereinstellung verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d7feb-162">This setting is available only as a Computer setting; there is no Per-User setting.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d7feb-163">Diese Registrierungseinstellung wird nicht in einem Richtlinienschlüssel gespeichert und gilt als *Präferenz*.</span><span class="sxs-lookup"><span data-stu-id="d7feb-163">This registry setting isn't stored in a policies key and is considered a *preference*.</span></span> <span data-ttu-id="d7feb-164">Somit bleibt die Einstellung erhalten, wenn das Gruppenrichtlinienobjekt, das die Einstellung implementiert, entfernt oder die Richtlinie auf **nicht konfiguriert**festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="d7feb-164">Therefore, if the Group Policy Object that implements the setting is ever removed or the policy is set to **Not Configured**, the setting will remain.</span></span> <span data-ttu-id="d7feb-165">Um die Verteilung von Microsoft Edge (Chromium-basiert) über die Gruppenrichtlinie freizugeben, legen Sie die Richtlinie auf **Deaktiviert** fest.</span><span class="sxs-lookup"><span data-stu-id="d7feb-165">To unblock distribution of Microsoft Edge (Chromium-based) by using Group Policy, set the policy to **Disabled**.</span></span>

## <span data-ttu-id="d7feb-166">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d7feb-166">See also</span></span>

- [<span data-ttu-id="d7feb-167">Microsoft Edge Enterprise-Angebotsseite</span><span class="sxs-lookup"><span data-stu-id="d7feb-167">Microsoft Edge Enterprise landing page</span></span>](https://www.microsoftedgeinsider.com/enterprise)
- [<span data-ttu-id="d7feb-168">Windows-Updates zur Unterstützung von Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="d7feb-168">Windows updates to support Microsoft Edge</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-sysupdate-windows-updates)
- [<span data-ttu-id="d7feb-169">Zugreifen auf die alte Version von Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="d7feb-169">How to access the old version of Microsoft Edge</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-sysupdate-access-old-edge)
