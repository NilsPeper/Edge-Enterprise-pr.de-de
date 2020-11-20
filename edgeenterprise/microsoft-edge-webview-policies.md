---
title: Dokumentation für die Microsoft Edge WebView2-Richtlinie
ms.author: stmoody
author: dan-wesley
manager: tahills
ms.date: 11/19/2020
audience: ITPro
ms.topic: reference
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
ms.custom: ''
description: Windows- und Mac-Dokumentation für alle vom Microsoft Edge Browser unterstützten Richtlinien
ms.openlocfilehash: a1204b4e334e2545a2570110ab5eaf498ef7c8f7
ms.sourcegitcommit: fc6f86f92f2fecac89028d77524d123bfaf2111d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/19/2020
ms.locfileid: "11181966"
---
# <span data-ttu-id="977ef-103">Microsoft Edge WebView2 –⁠ Richtlinien</span><span class="sxs-lookup"><span data-stu-id="977ef-103">Microsoft Edge WebView2 - Policies</span></span>

<span data-ttu-id="977ef-104">Die neueste Version von Microsoft Edge WebView2 umfasst die folgenden Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="977ef-104">The latest version of Microsoft Edge WebView2 includes the following policies.</span></span> <span data-ttu-id="977ef-105">Sie können diese Richtlinien verwenden, um zu konfigurieren, wie Microsoft Edge WebView2 in Ihrer Organisation ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="977ef-105">You can use these policies to configure how Microsoft Edge WebView2 runs in your organization.</span></span>

<span data-ttu-id="977ef-106">Informationen zu einer zusätzlichen Richtlinie, mit der Sie steuern können, wie und wann Microsoft Edge WebView2 aktualisiert wird, finden Sie unter [Microsoft Edge Updaterichtlinien-Referenz](microsoft-edge-update-policies.md).</span><span class="sxs-lookup"><span data-stu-id="977ef-106">For information about an additional set of policies used to control how and when Microsoft Edge WebView2 is updated, check out [Microsoft Edge update policy reference](microsoft-edge-update-policies.md).</span></span>


> [!NOTE]
> <span data-ttu-id="977ef-107">Dieser Artikel bezieht sich auf Microsoft Edge Version 87 oder neuer.</span><span class="sxs-lookup"><span data-stu-id="977ef-107">This article applies to Microsoft Edge version 87 or later.</span></span>

## <span data-ttu-id="977ef-108">Verfügbare Richtlinien</span><span class="sxs-lookup"><span data-stu-id="977ef-108">Available policies</span></span>

<span data-ttu-id="977ef-109">In dieser Tabelle sind sämtliche, in dieser Version von Microsoft Edge WebView2 verfügbaren Gruppenrichtlinien aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="977ef-109">These tables list all of the group policies available in this release of Microsoft Edge WebView2.</span></span> <span data-ttu-id="977ef-110">Über die Links in der folgenden Tabelle erhalten Sie weitere Einzelheiten zu bestimmten Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="977ef-110">Use the links in the table to get more details about specific policies.</span></span>

|||
|-|-|
|[<span data-ttu-id="977ef-111">Einstellungen für Loader-Außerkraftsetzung</span><span class="sxs-lookup"><span data-stu-id="977ef-111">Loader Override Settings</span></span>](#loader-override-settings)|

### [*<span data-ttu-id="977ef-112">Einstellungen für Loader-Außerkraftsetzung</span><span class="sxs-lookup"><span data-stu-id="977ef-112">Loader Override Settings</span></span>*](#loader-override-settings-policies)

|<span data-ttu-id="977ef-113">Richtlinienname</span><span class="sxs-lookup"><span data-stu-id="977ef-113">Policy Name</span></span>|<span data-ttu-id="977ef-114">Beschriftung</span><span class="sxs-lookup"><span data-stu-id="977ef-114">Caption</span></span>|
|-|-|
|[<span data-ttu-id="977ef-115">BrowserExecutableFolder</span><span class="sxs-lookup"><span data-stu-id="977ef-115">BrowserExecutableFolder</span></span>](#browserexecutablefolder)|<span data-ttu-id="977ef-116">Konfigurieren des Speicherorts des ausführbaren Browser-Ordners</span><span class="sxs-lookup"><span data-stu-id="977ef-116">Configure the location of the browser executable folder</span></span>|
|[<span data-ttu-id="977ef-117">ReleaseChannelPreference</span><span class="sxs-lookup"><span data-stu-id="977ef-117">ReleaseChannelPreference</span></span>](#releasechannelpreference)|<span data-ttu-id="977ef-118">Einstellen der Präferenz für die Suchreihenfolge der Veröffentlichungskanäle</span><span class="sxs-lookup"><span data-stu-id="977ef-118">Set the release channel search order preference</span></span>|




  ## <span data-ttu-id="977ef-119">Einstellungen für Loader-Außerkraftsetzungsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="977ef-119">Loader Override Settings policies</span></span>

  [<span data-ttu-id="977ef-120">Zurück zum Anfang</span><span class="sxs-lookup"><span data-stu-id="977ef-120">Back to top</span></span>](#microsoft-edge-webview2---policies)

  ### <span data-ttu-id="977ef-121">BrowserExecutableFolder</span><span class="sxs-lookup"><span data-stu-id="977ef-121">BrowserExecutableFolder</span></span>

  #### <span data-ttu-id="977ef-122">Konfigurieren des Speicherorts des ausführbaren Browser-Ordners</span><span class="sxs-lookup"><span data-stu-id="977ef-122">Configure the location of the browser executable folder</span></span>

  
  
  #### <span data-ttu-id="977ef-123">Unterstützte Versionen:</span><span class="sxs-lookup"><span data-stu-id="977ef-123">Supported versions:</span></span>

  - <span data-ttu-id="977ef-124">Unter Windows seit 87 oder später</span><span class="sxs-lookup"><span data-stu-id="977ef-124">On Windows since 87 or later</span></span>

  #### <span data-ttu-id="977ef-125">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="977ef-125">Description</span></span>

  <span data-ttu-id="977ef-126">Diese Richtlinie konfiguriert WebView2-Anwendungen, um die WebView2-Laufzeit im angegebenen Pfad zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="977ef-126">This policy configures WebView2 applications to use the WebView2 Runtime in the specified path.</span></span> <span data-ttu-id="977ef-127">Der Ordner sollte die folgenden Dateien enthalten: msedgewebview2.exe, msedge.dl usw.</span><span class="sxs-lookup"><span data-stu-id="977ef-127">The folder should contain the following files: msedgewebview2.exe, msedge.dll, and so on.</span></span>

<span data-ttu-id="977ef-128">Um den Wert für den Ordnerpfad festzulegen, geben Sie einen Wertnamen und ein Wertpaar an.</span><span class="sxs-lookup"><span data-stu-id="977ef-128">To set the value for the folder path, provide a Value name and Value pair.</span></span> <span data-ttu-id="977ef-129">Legen Sie den Wertnamen auf die Anwendungsbenutzer Modell-ID oder den Dateinamen der ausführbaren Datei fest.</span><span class="sxs-lookup"><span data-stu-id="977ef-129">Set value name to the Application User Model ID or the executable file name.</span></span> <span data-ttu-id="977ef-130">Sie können den Platzhalter "\*" als Wert für alle Anwendungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="977ef-130">You can use the "\*" wildcard as value name to apply to all applications.</span></span>

  #### <span data-ttu-id="977ef-131">Unterstützte Funktionen:</span><span class="sxs-lookup"><span data-stu-id="977ef-131">Supported features:</span></span>

  - <span data-ttu-id="977ef-132">Kann zwingend erforderlich sein: Ja</span><span class="sxs-lookup"><span data-stu-id="977ef-132">Can be mandatory: Yes</span></span>
  - <span data-ttu-id="977ef-133">Kann empfohlen werden: Nein</span><span class="sxs-lookup"><span data-stu-id="977ef-133">Can be recommended: No</span></span>
  - <span data-ttu-id="977ef-134">Dynamische Richtlinienaktualisierung: Ja</span><span class="sxs-lookup"><span data-stu-id="977ef-134">Dynamic Policy Refresh: Yes</span></span>

  #### <span data-ttu-id="977ef-135">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="977ef-135">Data Type:</span></span>

  - <span data-ttu-id="977ef-136">Liste von Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="977ef-136">List of strings</span></span>

  #### <span data-ttu-id="977ef-137">Windows-Informationen und -Einstellungen</span><span class="sxs-lookup"><span data-stu-id="977ef-137">Windows information and settings</span></span>

  ##### <span data-ttu-id="977ef-138">Informationen zur Gruppenrichtlinie (ADMX)</span><span class="sxs-lookup"><span data-stu-id="977ef-138">Group Policy (ADMX) info</span></span>

  - <span data-ttu-id="977ef-139">Eindeutiger Name der GP: BrowserExecutableFolder</span><span class="sxs-lookup"><span data-stu-id="977ef-139">GP unique name: BrowserExecutableFolder</span></span>
  - <span data-ttu-id="977ef-140">Name der GP: Konfigurieren des Speicherorts des ausführbaren Browser-Ordners</span><span class="sxs-lookup"><span data-stu-id="977ef-140">GP name: Configure the location of the browser executable folder</span></span>
  - <span data-ttu-id="977ef-141">GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/WebView2/Loader Override Settings</span><span class="sxs-lookup"><span data-stu-id="977ef-141">GP path (Mandatory): Administrative Templates/Microsoft Edge WebView2/Loader Override Settings</span></span>
  - <span data-ttu-id="977ef-142">GP Pfad (Empfohlen): n.a.</span><span class="sxs-lookup"><span data-stu-id="977ef-142">GP path (Recommended): N/A</span></span>
  - <span data-ttu-id="977ef-143">Name der GP-ADMX-Datei: MSEdgeWebView2.admx</span><span class="sxs-lookup"><span data-stu-id="977ef-143">GP ADMX file name: MSEdgeWebView2.admx</span></span>

  ##### <span data-ttu-id="977ef-144">Windows-Registrierungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="977ef-144">Windows Registry Settings</span></span>

  - <span data-ttu-id="977ef-145">Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge\WebView2\BrowserExecutableFolder</span><span class="sxs-lookup"><span data-stu-id="977ef-145">Path (Mandatory): SOFTWARE\Policies\Microsoft\Edge\WebView2\BrowserExecutableFolder</span></span>
  - <span data-ttu-id="977ef-146">Pfad (Empfohlen): n.a.</span><span class="sxs-lookup"><span data-stu-id="977ef-146">Path (Recommended): N/A</span></span>
  - <span data-ttu-id="977ef-147">Wertname: REG_SZ-Liste</span><span class="sxs-lookup"><span data-stu-id="977ef-147">Value Name: list of REG_SZ</span></span>
  - <span data-ttu-id="977ef-148">Werttyp: REG_SZ-Liste</span><span class="sxs-lookup"><span data-stu-id="977ef-148">Value Type: list of REG_SZ</span></span>

  ##### <span data-ttu-id="977ef-149">Beispielwert:</span><span class="sxs-lookup"><span data-stu-id="977ef-149">Example value:</span></span>

```
SOFTWARE\Policies\Microsoft\Edge\WebView2\BrowserExecutableFolder = "Name: *, Value: C:\\Program Files\\Microsoft Edge WebView2 Runtime Redistributable 85.0.541.0 x64"

```

  

  [<span data-ttu-id="977ef-150">Zurück zum Anfang</span><span class="sxs-lookup"><span data-stu-id="977ef-150">Back to top</span></span>](#microsoft-edge-webview2---policies)

  ### <span data-ttu-id="977ef-151">ReleaseChannelPreference</span><span class="sxs-lookup"><span data-stu-id="977ef-151">ReleaseChannelPreference</span></span>

  #### <span data-ttu-id="977ef-152">Einstellen der Präferenz für die Suchreihenfolge der Veröffentlichungskanäle</span><span class="sxs-lookup"><span data-stu-id="977ef-152">Set the release channel search order preference</span></span>

  
  
  #### <span data-ttu-id="977ef-153">Unterstützte Versionen:</span><span class="sxs-lookup"><span data-stu-id="977ef-153">Supported versions:</span></span>

  - <span data-ttu-id="977ef-154">Unter Windows seit 87 oder später</span><span class="sxs-lookup"><span data-stu-id="977ef-154">On Windows since 87 or later</span></span>

  #### <span data-ttu-id="977ef-155">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="977ef-155">Description</span></span>

  <span data-ttu-id="977ef-156">Die standardmäßige Kanalsuchreihenfolge ist WebView2 Runtime, Beta, Dev und Canary.</span><span class="sxs-lookup"><span data-stu-id="977ef-156">The default channel search order is WebView2 Runtime, Beta, Dev, and Canary.</span></span>

<span data-ttu-id="977ef-157">Um die Standardsuchreihenfolge umzukehren, legen Sie diese Richtlinie auf 1 fest.</span><span class="sxs-lookup"><span data-stu-id="977ef-157">To reverse the default search order, set this policy to 1.</span></span>

<span data-ttu-id="977ef-158">Um den Wert für den bevorzugten Veröffentlichungskanal festzulegen, geben Sie einen Wertnamen und ein Wertpaar an.</span><span class="sxs-lookup"><span data-stu-id="977ef-158">To set the value for the release channel preference, provide a Value name and Value pair.</span></span> <span data-ttu-id="977ef-159">Legen Sie den Wertnamen auf die Anwendungsbenutzer Modell-ID oder den Dateinamen der ausführbaren Datei fest.</span><span class="sxs-lookup"><span data-stu-id="977ef-159">Set value name to the Application User Model ID or the executable file name.</span></span> <span data-ttu-id="977ef-160">Sie können den Platzhalter "\*" als Wert für alle Anwendungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="977ef-160">You can use the "\*" wildcard as value name to apply to all applications.</span></span>

  #### <span data-ttu-id="977ef-161">Unterstützte Funktionen:</span><span class="sxs-lookup"><span data-stu-id="977ef-161">Supported features:</span></span>

  - <span data-ttu-id="977ef-162">Kann zwingend erforderlich sein: Ja</span><span class="sxs-lookup"><span data-stu-id="977ef-162">Can be mandatory: Yes</span></span>
  - <span data-ttu-id="977ef-163">Kann empfohlen werden: Nein</span><span class="sxs-lookup"><span data-stu-id="977ef-163">Can be recommended: No</span></span>
  - <span data-ttu-id="977ef-164">Dynamische Richtlinienaktualisierung: Ja</span><span class="sxs-lookup"><span data-stu-id="977ef-164">Dynamic Policy Refresh: Yes</span></span>

  #### <span data-ttu-id="977ef-165">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="977ef-165">Data Type:</span></span>

  - <span data-ttu-id="977ef-166">Liste von Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="977ef-166">List of strings</span></span>

  #### <span data-ttu-id="977ef-167">Windows-Informationen und -Einstellungen</span><span class="sxs-lookup"><span data-stu-id="977ef-167">Windows information and settings</span></span>

  ##### <span data-ttu-id="977ef-168">Informationen zur Gruppenrichtlinie (ADMX)</span><span class="sxs-lookup"><span data-stu-id="977ef-168">Group Policy (ADMX) info</span></span>

  - <span data-ttu-id="977ef-169">Eindeutiger Name der GP: ReleaseChannelPreference</span><span class="sxs-lookup"><span data-stu-id="977ef-169">GP unique name: ReleaseChannelPreference</span></span>
  - <span data-ttu-id="977ef-170">Name der GP: Einstellen der Präferenz für die Suchreihenfolge der Veröffentlichungskanäle</span><span class="sxs-lookup"><span data-stu-id="977ef-170">GP name: Set the release channel search order preference</span></span>
  - <span data-ttu-id="977ef-171">GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/WebView2/Loader Override Settings</span><span class="sxs-lookup"><span data-stu-id="977ef-171">GP path (Mandatory): Administrative Templates/Microsoft Edge WebView2/Loader Override Settings</span></span>
  - <span data-ttu-id="977ef-172">GP Pfad (Empfohlen): n.a.</span><span class="sxs-lookup"><span data-stu-id="977ef-172">GP path (Recommended): N/A</span></span>
  - <span data-ttu-id="977ef-173">Name der GP-ADMX-Datei: MSEdgeWebView2.admx</span><span class="sxs-lookup"><span data-stu-id="977ef-173">GP ADMX file name: MSEdgeWebView2.admx</span></span>

  ##### <span data-ttu-id="977ef-174">Windows-Registrierungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="977ef-174">Windows Registry Settings</span></span>

  - <span data-ttu-id="977ef-175">Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge\WebView2\ReleaseChannelPreference</span><span class="sxs-lookup"><span data-stu-id="977ef-175">Path (Mandatory): SOFTWARE\Policies\Microsoft\Edge\WebView2\ReleaseChannelPreference</span></span>
  - <span data-ttu-id="977ef-176">Pfad (Empfohlen): n.a.</span><span class="sxs-lookup"><span data-stu-id="977ef-176">Path (Recommended): N/A</span></span>
  - <span data-ttu-id="977ef-177">Wertname: REG_SZ-Liste</span><span class="sxs-lookup"><span data-stu-id="977ef-177">Value Name: list of REG_SZ</span></span>
  - <span data-ttu-id="977ef-178">Werttyp: REG_SZ-Liste</span><span class="sxs-lookup"><span data-stu-id="977ef-178">Value Type: list of REG_SZ</span></span>

  ##### <span data-ttu-id="977ef-179">Beispielwert:</span><span class="sxs-lookup"><span data-stu-id="977ef-179">Example value:</span></span>

```
SOFTWARE\Policies\Microsoft\Edge\WebView2\ReleaseChannelPreference = "Name: *, Value: 1"

```

  

  [<span data-ttu-id="977ef-180">Zurück zum Anfang</span><span class="sxs-lookup"><span data-stu-id="977ef-180">Back to top</span></span>](#microsoft-edge-webview2---policies)


## <span data-ttu-id="977ef-181">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="977ef-181">See also</span></span>

- [<span data-ttu-id="977ef-182">Konfigurieren von Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="977ef-182">Configuring Microsoft Edge</span></span>](configure-microsoft-edge.md)
- [<span data-ttu-id="977ef-183">Microsoft Edge Enterprise-Angebotsseite</span><span class="sxs-lookup"><span data-stu-id="977ef-183">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="977ef-184">Microsoft Sicherheitsbaselines-Blog</span><span class="sxs-lookup"><span data-stu-id="977ef-184">Microsoft Security Baselines Blog</span></span>](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/bg-p/Microsoft-Security-Baselines)