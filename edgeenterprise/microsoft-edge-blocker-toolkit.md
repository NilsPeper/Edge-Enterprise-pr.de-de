---
title: Blocker Toolkit zum Deaktivieren der automatischen Übermittlung von Microsoft Edge
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 06/30/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Blocker Toolkit zum Deaktivieren der automatischen Übermittlung von Microsoft Edge
ms.openlocfilehash: 7563d2c94cf91a8434328699e46c75dbcfb77561
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/31/2020
ms.locfileid: "10980055"
---
# <span data-ttu-id="61f0f-103">Blocker Toolkit zum Deaktivieren der automatischen Bereitstellung von Microsoft Edge (Chromium-basiert)</span><span class="sxs-lookup"><span data-stu-id="61f0f-103">Blocker Toolkit to disable automatic delivery of Microsoft Edge (Chromium-based)</span></span>

<span data-ttu-id="61f0f-104">In diesem Artikel wird das Blocker Toolkit zum Deaktivieren der automatischen Übermittlung und Installation von Microsoft Edge beschrieben.</span><span class="sxs-lookup"><span data-stu-id="61f0f-104">This article describes the Blocker Toolkit for disabling automatic delivery and installation of Microsoft Edge.</span></span> <span data-ttu-id="61f0f-105">Dieser Artikel wurde aktualisiert: am **09.01.2020** mit weiteren Informationen zu Geräten, die möglicherweise die Verwendung des Blocker-Toolkits erfordern, am **28.02.2020**, um „MDM-verwaltet“ aus den Kriterien von Geräten zu entfernen, die bei diesem automatischen Update ausgeschlossen werden sollen, und am **30.06.2020**, um darauf hinzuweisen, dass alle mit WindowsUpdate verbundenen Geräte dieses Update erhalten können (wird nicht vor dem 30.07.2020 wirksam).</span><span class="sxs-lookup"><span data-stu-id="61f0f-105">This article was updated on **01/09/2020** with more information about devices that might require you to use the Blocker Toolkit, on **2/28/2020** to remove "MDM managed" from the criteria of devices to be excluded from this automatic update, and on **6/30/2020** to reflect that all Windows Update connected devices are in scope to receive this update (effective no sooner than 7/30/2020).</span></span>

> [!NOTE]
> <span data-ttu-id="61f0f-106">Dieser Artikel bezieht sich auf den stabilen Kanal von Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="61f0f-106">This applies to Microsoft Edge Stable channel.</span></span>

## <span data-ttu-id="61f0f-107">Übersicht</span><span class="sxs-lookup"><span data-stu-id="61f0f-107">Overview</span></span>

<span data-ttu-id="61f0f-108">Um unseren Kunden zu helfen, sicherer und aktueller zu werden, wird Microsoft den Browser MicrosoftEdge (Chromium-basiert) an alle mit WindowsUpdate verbundenen Geräte unter Windows10 (ab Version1803) verteilen.</span><span class="sxs-lookup"><span data-stu-id="61f0f-108">To help our customers become more secure and up-to-date, Microsoft will distribute Microsoft Edge (Chromium-based) to all Windows Update-connected devices running Windows 10 version 1803 and newer.</span></span> <span data-ttu-id="61f0f-109">Dieser Prozess startet nach dem 15.Januar 2020. An diesem Datum stehen weitere Informationen zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="61f0f-109">This process will start after January 15, 2020 and more information will be available on that date.</span></span>

<span data-ttu-id="61f0f-110">Das Blocker Toolkit richtet sich an Organisationen, die die automatische Bereitstellung von MicrosoftEdge (Chromium-basiert) auf mit Windows Update verbundenen Geräten unter Windows10 (ab Version1803) blockieren möchten.</span><span class="sxs-lookup"><span data-stu-id="61f0f-110">The Blocker Toolkit is intended for organizations that would like to block automatic delivery of Microsoft Edge (Chromium-based) to Windows Updated-connected devices running Windows 10 version 1803 and newer.</span></span>
<span data-ttu-id="61f0f-111">Durch Windows Server Update Services (WSUS) oder Windows Update for Business (WUfB) verwaltete Geräte werden bei dieser automatischen Aktualisierung ausgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="61f0f-111">Devices that are Windows Server Update Services (WSUS) or Windows Update for Business (WUfB) managed will be excluded from this automatic update.</span></span>

**<span data-ttu-id="61f0f-112">Beachten Sie unbedingt Folgendes:</span><span class="sxs-lookup"><span data-stu-id="61f0f-112">It's important to note that:</span></span>**

- <span data-ttu-id="61f0f-113">Das Blocker Toolkit kann nicht verhindern, dass Benutzer Microsoft Edge (Chromium-basiert) manuell aus dem Internet oder von externen Medien herunterladen und installieren.</span><span class="sxs-lookup"><span data-stu-id="61f0f-113">The Blocker Toolkit will not prevent users from manually installing Microsoft Edge (Chromium-based) from Internet download, or from external media.</span></span>
- <span data-ttu-id="61f0f-114">Organisationen mit Updates, die über Windows Update for Business (WUfB) verwaltet werden, erhalten dieses Update nicht automatisch und müssen das Blocker Toolkit nicht bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="61f0f-114">Organizations with updates managed through Windows Update for Business (WUfB) will not automatically receive this update and do not need to deploy the blocker toolkit.</span></span>
- <span data-ttu-id="61f0f-115">Organisationen mit Umgebungen, die mit einer Update-Verwaltungslösung wie Windows Server Update Services (WSUS) oder System Center Konfigurations-Manager (SCCM) verwaltet werden, müssen das Blocker Toolkit nicht bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="61f0f-115">Organizations with environments managed with an update management solution such as Windows Server Update Services (WSUS) or System Center Configuration Manager (SCCM) do not have to deploy the Blocker Toolkit.</span></span> <span data-ttu-id="61f0f-116">Sie können diese Produkte verwenden, um die Bereitstellung von Updates, die über Windows Update und Microsoft Update veröffentlicht wurden, einschließlich Microsoft Edge (Chromium-basiert), in ihrer Umgebung vollständig zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="61f0f-116">They can use those products to fully manage deployment of updates released through Windows Update and Microsoft Update, including Microsoft Edge (Chromium-based), within their environment.</span></span>
- <span data-ttu-id="61f0f-117">Dieses Update ist ein eigenständiges Update (also nicht Teil des monatlichen kumulativen Updates), damit die Unternehmenskunden Flexibilität und maximale Kontrolle über die Bereitstellung dieses Updates haben.</span><span class="sxs-lookup"><span data-stu-id="61f0f-117">This update is a stand-alone update (not part of the monthly cumulative update) to give Enterprise customers flexibility and maximum control over deploying this update.</span></span>
- <span data-ttu-id="61f0f-118">Das neue MicrosoftEdge (Chromium-basiert) wird im Rahmen des Windows10-Funktionsupdates, Version20H2, in der zweiten Hälfte von 2020 einbezogen.</span><span class="sxs-lookup"><span data-stu-id="61f0f-118">The new Microsoft Edge (Chromium-based) will be included as part of the Windows 10, version 20H2 feature update in the second half of 2020.</span></span> <span data-ttu-id="61f0f-119">Das Blocker-Toolkit wirkt sich nicht auf das Verhalten oder die Bereitstellung von 20H2 aus.</span><span class="sxs-lookup"><span data-stu-id="61f0f-119">The Blocker toolkit does not impact 20H2 behaviors or deployment.</span></span> <span data-ttu-id="61f0f-120">Weitere Informationen zu Windows10, Version20H2, finden Sie [hier](https://blogs.windows.com/windowsexperience/2020/06/16/whats-next-for-windows-10-updates/).</span><span class="sxs-lookup"><span data-stu-id="61f0f-120">See more information about Windows 10, version 20H2 [here](https://blogs.windows.com/windowsexperience/2020/06/16/whats-next-for-windows-10-updates/).</span></span>

<span data-ttu-id="61f0f-121">Sie können die ausführbare Datei des Blocker Toolkit unter [https://msedgeblockertoolkit.blob.core.windows.net/blockertoolkit/MicrosoftEdgeChromiumBlockerToolkit.exe](https://msedgeblockertoolkit.blob.core.windows.net/blockertoolkit/MicrosoftEdgeChromiumBlockerToolkit.exe) herunterladen.</span><span class="sxs-lookup"><span data-stu-id="61f0f-121">You can download the Blocker Toolkit executable file from [https://msedgeblockertoolkit.blob.core.windows.net/blockertoolkit/MicrosoftEdgeChromiumBlockerToolkit.exe](https://msedgeblockertoolkit.blob.core.windows.net/blockertoolkit/MicrosoftEdgeChromiumBlockerToolkit.exe).</span></span>

### <span data-ttu-id="61f0f-122">Toolkit-Komponenten</span><span class="sxs-lookup"><span data-stu-id="61f0f-122">Toolkit components</span></span>

<span data-ttu-id="61f0f-123">Diese Toolkit enthält die folgenden Komponenten:</span><span class="sxs-lookup"><span data-stu-id="61f0f-123">This toolkit contains the following components:</span></span>

- <span data-ttu-id="61f0f-124">Ausführbares Blocker-Skript (.CMD)</span><span class="sxs-lookup"><span data-stu-id="61f0f-124">Executable blocker script (.CMD)</span></span>
- <span data-ttu-id="61f0f-125">Administrative Vorlage für Gruppenrichtlinien (.ADMX und .ADML)</span><span class="sxs-lookup"><span data-stu-id="61f0f-125">Group Policy Administrative Template (.ADMX and .ADML)</span></span>

### <span data-ttu-id="61f0f-126">Unterstützte Betriebssysteme</span><span class="sxs-lookup"><span data-stu-id="61f0f-126">Supported Operating Systems</span></span>

<span data-ttu-id="61f0f-127">Windows 10 ab Version 1803</span><span class="sxs-lookup"><span data-stu-id="61f0f-127">Windows 10 version 1803 and newer.</span></span>

## <span data-ttu-id="61f0f-128">Blocker-Skript</span><span class="sxs-lookup"><span data-stu-id="61f0f-128">Blocker script</span></span>

<span data-ttu-id="61f0f-129">Das Skript erstellt einen Registrierungsschlüssel und setzt den zugehörigen Wert so, dass er die automatische Bereitstellung von Microsoft Edge (Chromium-basiert) auf dem lokalen Computer oder einem entfernten Zielcomputer blockiert oder entsperrt (abhängig von der verwendeten Befehlszeilenoption).</span><span class="sxs-lookup"><span data-stu-id="61f0f-129">The script creates a registry key and sets the associated value to block or unblock (depending on the command-line option used) automatic delivery of Microsoft Edge (Chromium-based) on either the local machine or a remote target machine.</span></span>

**<span data-ttu-id="61f0f-130">Registrierungsschlüssel:</span><span class="sxs-lookup"><span data-stu-id="61f0f-130">Registry key:</span></span>** `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\EdgeUpdate`<br>
**<span data-ttu-id="61f0f-131">Schlüsselwertname:</span><span class="sxs-lookup"><span data-stu-id="61f0f-131">Key value name:</span></span>** `DoNotUpdateToEdgeWithChromium`

| <span data-ttu-id="61f0f-132">Wert</span><span class="sxs-lookup"><span data-stu-id="61f0f-132">Value</span></span>                | <span data-ttu-id="61f0f-133">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="61f0f-133">Result</span></span>                         |
|----------------------|--------------------------------|
| *<span data-ttu-id="61f0f-134">Schlüssel ist nicht definiert</span><span class="sxs-lookup"><span data-stu-id="61f0f-134">Key is not defined</span></span>* | <span data-ttu-id="61f0f-135">Verteilung ist *nicht* blockiert.</span><span class="sxs-lookup"><span data-stu-id="61f0f-135">Distribution is *not* blocked.</span></span> |
| <span data-ttu-id="61f0f-136">0</span><span class="sxs-lookup"><span data-stu-id="61f0f-136">0</span></span>                    | <span data-ttu-id="61f0f-137">Verteilung ist *nicht* blockiert.</span><span class="sxs-lookup"><span data-stu-id="61f0f-137">Distribution is *not* blocked.</span></span> |
| <span data-ttu-id="61f0f-138">1</span><span class="sxs-lookup"><span data-stu-id="61f0f-138">1</span></span>                    | <span data-ttu-id="61f0f-139">Verteilung ist blockiert.</span><span class="sxs-lookup"><span data-stu-id="61f0f-139">Distribution is blocked.</span></span>       |

<span data-ttu-id="61f0f-140">Das Skript hat folgende Befehlszeilensyntax:</span><span class="sxs-lookup"><span data-stu-id="61f0f-140">The script has the following command-line syntax:</span></span><br>
`EdgeChromium_Blocker.cmd [<machine name>] [/B] [/U] [/H]`

### <span data-ttu-id="61f0f-141">Computername</span><span class="sxs-lookup"><span data-stu-id="61f0f-141">Machine name</span></span>

<span data-ttu-id="61f0f-142">Der Parameter `<machine name>` ist optional.</span><span class="sxs-lookup"><span data-stu-id="61f0f-142">The `<machine name>` parameter is optional.</span></span> <span data-ttu-id="61f0f-143">Wenn er fehlt, wird die Aktion auf dem lokalen Computer ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="61f0f-143">If not specified, the action is performed on the local machine.</span></span> <span data-ttu-id="61f0f-144">Andernfalls erfolgt der Zugriff auf den Remotecomputer über die Remote-Registrierungsfunktionen des Befehls `REG`.</span><span class="sxs-lookup"><span data-stu-id="61f0f-144">Otherwise, the remote machine is accessed through the remote registry capabilities of the `REG` command.</span></span> <span data-ttu-id="61f0f-145">Wenn auf die Remoteregistrierung aufgrund von Sicherheitsberechtigungen nicht zugegriffen werden kann oder wenn der Remotecomputer nicht gefunden werden kann, wird vom Befehl `REG` eine Fehlermeldung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="61f0f-145">If the remote registry can't be accessed due to security permissions or the remote machine can't be found, an error message is returned from the `REG` command.</span></span>

### <span data-ttu-id="61f0f-146">Schalter</span><span class="sxs-lookup"><span data-stu-id="61f0f-146">Switches</span></span>

<span data-ttu-id="61f0f-147">Die vom Skript verwendeten Schalter schließen sich gegenseitig aus, und nur der erste gültige Schalter eines bestimmten Befehls wird aktiviert.</span><span class="sxs-lookup"><span data-stu-id="61f0f-147">Switches used by the script are mutually exclusive and only the first valid switch from a given command is acted on.</span></span> <span data-ttu-id="61f0f-148">Das Skript kann mehrmals auf demselben Computer ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="61f0f-148">The script can be run multiple times on the same machine.</span></span>

| <span data-ttu-id="61f0f-149">Schalter</span><span class="sxs-lookup"><span data-stu-id="61f0f-149">Switch</span></span>       | <span data-ttu-id="61f0f-150">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="61f0f-150">Description</span></span>                              |
|--------------|------------------------------------------|
| `/B`         | <span data-ttu-id="61f0f-151">Verteilung wird blockiert</span><span class="sxs-lookup"><span data-stu-id="61f0f-151">Blocks distribution</span></span>                      |
| `/U`         | <span data-ttu-id="61f0f-152">Blockierung der Verteilung wird aufgehoben</span><span class="sxs-lookup"><span data-stu-id="61f0f-152">Unblocks distribution</span></span>                    |
| `/H` <span data-ttu-id="61f0f-153">oder</span><span class="sxs-lookup"><span data-stu-id="61f0f-153">or</span></span> `/?` | <span data-ttu-id="61f0f-154">Zeigt die folgende Zusammenfassung für Hilfe an:</span><span class="sxs-lookup"><span data-stu-id="61f0f-154">Displays the following summary help:</span></span><br>`This tool can be used to remotely block or unblock the delivery of Microsoft Edge (Chromium-based) through Automatic Updates.`<br> `Usage:`<br>`EdgeChromium_Blocker.cmd [<machine name>] [/B][/U][/H]`<br>`B = Block Microsoft Edge (Chromium-based) deployment`<br>`U = Allow Microsoft Edge (Chromium-based) deployment`<br>`H = Help`<br>`Examples:`<br>`EdgeChromium_Blocker.cmd mymachine /B (blocks delivery on machine "mymachine")`<br>`EdgeChromium_Blocker.cmd /U (unblocks delivery on the local machine)`<br> |

## <span data-ttu-id="61f0f-155">Administrative Vorlage für Gruppenrichtlinien (.ADMX- und .ADML-Dateien)</span><span class="sxs-lookup"><span data-stu-id="61f0f-155">Group Policy Administrative Template (.ADMX and .ADML files)</span></span>

<span data-ttu-id="61f0f-156">Die Verwaltungsvorlage für Gruppenrichtlinien (.ADMX- und .ADML-Dateien) ermöglicht es Administratoren, die neuen Gruppenrichtlinieneinstellungen zu importieren, um die automatische Bereitstellung von Microsoft Edge (Chromium-basiert) in ihrer Gruppenrichtlinienumgebung zu blockieren oder freizugeben. Administratoren können mit der Gruppenrichtlinie die Aktion in ihrer Umgebung systemübergreifend zentral ausführen.</span><span class="sxs-lookup"><span data-stu-id="61f0f-156">The Group Policy Administrative Template (.ADMX  and .ADML files) allows administrators to import the new Group Policy settings to block or unblock automatic delivery of Microsoft Edge (Chromium-based) into their Group Policy environment, and use Group Policy to centrally execute the action across systems in their environment.</span></span>

<span data-ttu-id="61f0f-157">Benutzer, die Windows 10 RS3 Enterprise/EDU und RS4 und neuer verwenden, finden die Richtlinie unter dem folgenden Pfad:</span><span class="sxs-lookup"><span data-stu-id="61f0f-157">Users running Windows 10 RS3 Enterprise/EDU and RS4 and newer, will see the policy under the following path:</span></span>

```
/Computer Configuration  
  /Administrative Templates
    /Classic Administrative Templates
      /Windows Components
        /Windows Update  
          /Microsoft Edge (Chromium-based) Blockers  
```

<span data-ttu-id="61f0f-158">Diese Einstellung ist nicht pro Benutzer, sondern nur als Computereinstellung verfügbar.</span><span class="sxs-lookup"><span data-stu-id="61f0f-158">This setting is available only as a Computer setting; there is no Per-User setting.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="61f0f-159">Diese Registrierungseinstellung wird nicht in einem Richtlinienschlüssel gespeichert und gilt als *Präferenz*.</span><span class="sxs-lookup"><span data-stu-id="61f0f-159">This registry setting isn't stored in a policies key and is considered a *preference*.</span></span> <span data-ttu-id="61f0f-160">Somit bleibt die Einstellung erhalten, wenn das Gruppenrichtlinienobjekt, das die Einstellung implementiert, entfernt oder die Richtlinie auf **nicht konfiguriert**festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="61f0f-160">Therefore, if the Group Policy Object that implements the setting is ever removed or the policy is set to **Not Configured**, the setting will remain.</span></span> <span data-ttu-id="61f0f-161">Um die Verteilung von Microsoft Edge (Chromium-basiert) über die Gruppenrichtlinie freizugeben, legen Sie die Richtlinie auf **Deaktiviert** fest.</span><span class="sxs-lookup"><span data-stu-id="61f0f-161">To unblock distribution of Microsoft Edge (Chromium-based) by using Group Policy, set the policy to **Disabled**.</span></span>

## <span data-ttu-id="61f0f-162">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="61f0f-162">See also</span></span>

- [<span data-ttu-id="61f0f-163">Microsoft Edge Enterprise-Angebotsseite</span><span class="sxs-lookup"><span data-stu-id="61f0f-163">Microsoft Edge Enterprise landing page</span></span>](https://www.microsoftedgeinsider.com/enterprise)
- [<span data-ttu-id="61f0f-164">Windows-Updates zur Unterstützung von Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="61f0f-164">Windows updates to support Microsoft Edge</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-sysupdate-windows-updates)
- [<span data-ttu-id="61f0f-165">Zugreifen auf die alte Version von Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="61f0f-165">How to access the old version of Microsoft Edge</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-sysupdate-access-old-edge)
