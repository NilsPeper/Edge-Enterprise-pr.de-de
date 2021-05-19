---
title: Konfigurieren von Microsoft Edge mithilfe von Tools für die mobile Geräteverwaltung
ms.author: kvice
author: dan-wesley
manager: laurawi
ms.date: 10/25/2019
audience: ITPro
ms.topic: technical
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Konfigurieren Sie Microsoft Edge mithilfe von Tools für die mobile Geräteverwaltung.
ms.openlocfilehash: dda35199f653b3dfb8f20b33b068c59621222b36
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979917"
---
# <span data-ttu-id="f7852-103">Konfigurieren von Microsoft Edge mithilfe von Tools für die mobile Geräteverwaltung</span><span class="sxs-lookup"><span data-stu-id="f7852-103">Configure Microsoft Edge using Mobile Device Management</span></span>

<span data-ttu-id="f7852-104">In diesem Artikel wird erläutert, wie Sie Microsoft Edge auf Windows 10 mithilfe der [Geräteverwaltung für Mobilgeräte (MDM)](https://docs.microsoft.com/windows/client-management/mdm/) mit [ADMX-Aufnahme](https://docs.microsoft.com/windows/client-management/mdm/win32-and-centennial-app-policy-configuration) konfigurieren können.</span><span class="sxs-lookup"><span data-stu-id="f7852-104">This article explains how to configure Microsoft Edge on Windows 10 using [Mobile Device Management (MDM)](https://docs.microsoft.com/windows/client-management/mdm/) by means of [ADMX Ingestion](https://docs.microsoft.com/windows/client-management/mdm/win32-and-centennial-app-policy-configuration).</span></span> <span data-ttu-id="f7852-105">Weitere Inhalte dieses Artikels:</span><span class="sxs-lookup"><span data-stu-id="f7852-105">This article also describes:</span></span>

- <span data-ttu-id="f7852-106">[Erstellen von Open Mobile Alliance Uniform Resource Identifier (OMA-URI) für Microsoft Edge-Richtlinien](#create-an-oma-uri-for-microsoft-edge-policies).</span><span class="sxs-lookup"><span data-stu-id="f7852-106">How to [create Open Mobile Alliance Uniform Resource Identifier (OMA-URI) for Microsoft Edge policies](#create-an-oma-uri-for-microsoft-edge-policies).</span></span>
- <span data-ttu-id="f7852-107">[Konfigurieren von Microsoft Edge in Intune mithilfe der ADMX-Aufnahme und benutzerdefinierter OMA-URI](#configure-microsoft-edge-in-intune-using-admx-ingestion).</span><span class="sxs-lookup"><span data-stu-id="f7852-107">How to [configure Microsoft Edge in Intune using ADMX ingestion and custom OMA-URI](#configure-microsoft-edge-in-intune-using-admx-ingestion).</span></span>

> [!NOTE]
> <span data-ttu-id="f7852-108">Dieser Artikel bezieht sich auf Microsoft Edge Version 77 oder höher.</span><span class="sxs-lookup"><span data-stu-id="f7852-108">This article applies to Microsoft Edge version 77 or later.</span></span>

## <span data-ttu-id="f7852-109">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="f7852-109">Prerequisites</span></span>

<span data-ttu-id="f7852-110">Windows 10, mit den folgenden Mindestvoraussetzungen:</span><span class="sxs-lookup"><span data-stu-id="f7852-110">Windows 10, with the following minimum system requirements:</span></span>

- <span data-ttu-id="f7852-111">Windows 10, Version 1903, mit Installation von [KB4512941](https://support.microsoft.com/help/4512941/) und [KB4517211](https://support.microsoft.com/help/4517211/)</span><span class="sxs-lookup"><span data-stu-id="f7852-111">Windows 10, version 1903 with [KB4512941](https://support.microsoft.com/help/4512941/) and [KB4517211](https://support.microsoft.com/help/4517211/) installed</span></span>
- <span data-ttu-id="f7852-112">Windows 10, Version 1809, mit Installation von [KB4512534](https://support.microsoft.com/help/4512534/) und [KB4520062](https://support.microsoft.com/help/4520062/)</span><span class="sxs-lookup"><span data-stu-id="f7852-112">Windows 10, version 1809 with [KB4512534](https://support.microsoft.com/help/4512534/) and [KB4520062](https://support.microsoft.com/help/4520062/) installed</span></span>
- <span data-ttu-id="f7852-113">Windows 10, Version 1803, mit Installation von [KB4512509](https://support.microsoft.com/help/4512509/) und [KB4519978](https://support.microsoft.com/help/4519978)</span><span class="sxs-lookup"><span data-stu-id="f7852-113">Windows 10, version 1803 with [KB4512509](https://support.microsoft.com/help/4512509/) and [KB4519978](https://support.microsoft.com/help/4519978) installed</span></span>
- <span data-ttu-id="f7852-114">Windows 10, Version 1709, mit Installation von [KB4516071](https://support.microsoft.com/help/4516071/) und [KB4520006](https://support.microsoft.com/help/4520006)</span><span class="sxs-lookup"><span data-stu-id="f7852-114">Windows 10, version 1709 with [KB4516071](https://support.microsoft.com/help/4516071/) and [KB4520006](https://support.microsoft.com/help/4520006) installed</span></span>

## <span data-ttu-id="f7852-115">Übersicht</span><span class="sxs-lookup"><span data-stu-id="f7852-115">Overview</span></span>

<span data-ttu-id="f7852-116">Sie können Microsoft Edge auf Windows 10 mithilfe von MDM mit dem bevorzugten Enterprise Mobility Management (EMM)- oder MDM-Anbieter konfigurieren, der die [ADMX-Aufnahme](https://docs.microsoft.com/windows/client-management/mdm/win32-and-centennial-app-policy-configuration) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f7852-116">You can configure Microsoft Edge on Windows 10 using MDM with your preferred Enterprise Mobility Management (EMM) or MDM provider that supports [ADMX Ingestion](https://docs.microsoft.com/windows/client-management/mdm/win32-and-centennial-app-policy-configuration).</span></span>

<span data-ttu-id="f7852-117">Das Konfigurieren von Microsoft Edge mit MDM besteht aus zwei Schritten:</span><span class="sxs-lookup"><span data-stu-id="f7852-117">Configuring Microsoft Edge with MDM is a two part process:</span></span>

1. <span data-ttu-id="f7852-118">Aufnehmen der Microsoft Edge ADMX-Datei in Ihren EMM- oder MDM-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="f7852-118">Ingesting the Microsoft Edge ADMX file into your EMM or MDM provider.</span></span> <span data-ttu-id="f7852-119">Anweisungen zum Aufnehmen einer ADMX-Datei erhalten Sie von Ihrem Anbieter.</span><span class="sxs-lookup"><span data-stu-id="f7852-119">See your provider for instructions on how to ingest an ADMX file.</span></span>

   > [!NOTE]
   > <span data-ttu-id="f7852-120">Informationen zu Microsoft Intune finden Sie unter [Konfigurieren von Microsoft Edge in Intune mithilfe der ADMX-Aufnahme](#configure-microsoft-edge-in-intune-using-admx-ingestion).</span><span class="sxs-lookup"><span data-stu-id="f7852-120">For Microsoft Intune, see [Configure Microsoft Edge in Intune using ADMX ingestion](#configure-microsoft-edge-in-intune-using-admx-ingestion).</span></span>

2. <span data-ttu-id="f7852-121">[Erstellen eines OMA-URI für eine Microsoft Edge-Richtlinie](#create-an-oma-uri-for-microsoft-edge-policies)</span><span class="sxs-lookup"><span data-stu-id="f7852-121">[Creating an OMA-URI for a Microsoft Edge policy](#create-an-oma-uri-for-microsoft-edge-policies).</span></span>

## <span data-ttu-id="f7852-122">Erstellen eines OMA-URI für Microsoft Edge-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="f7852-122">Create an OMA-URI for Microsoft Edge policies</span></span>

<span data-ttu-id="f7852-123">In den folgenden Abschnitten wird beschrieben, wie Sie den OMA-URI-Pfad erstellen und den Wert im XML-Format für obligatorische und empfohlene Browserrichtlinien suchen und definieren.</span><span class="sxs-lookup"><span data-stu-id="f7852-123">The following sections describe how to create the OMA-URI path and look up and define the value in XML format for mandatory and recommended browser polices.</span></span>

<span data-ttu-id="f7852-124">Laden Sie zunächst die Microsoft Edge-Richtlinienvorlagendatei (MicrosoftEdgePolicyTemplates.cab) von der [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise) herunter und extrahieren Sie den Inhalt.</span><span class="sxs-lookup"><span data-stu-id="f7852-124">Before you get started download the Microsoft Edge policy templates file (MicrosoftEdgePolicyTemplates.cab) from the [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise) and extract the contents.</span></span>

<span data-ttu-id="f7852-125">Es gibt drei Schritte zum Definieren des OMA-URI:</span><span class="sxs-lookup"><span data-stu-id="f7852-125">There are three steps for defining the OMA-URI:</span></span>

1. [<span data-ttu-id="f7852-126">Erstellen des OMA-URI-Pfads</span><span class="sxs-lookup"><span data-stu-id="f7852-126">Create the OMA-URI path</span></span>](#create-the-oma-uri-path)
2. [<span data-ttu-id="f7852-127">Angabe des OMA-URI-Datentyps</span><span class="sxs-lookup"><span data-stu-id="f7852-127">Specify the OMA-URI data type</span></span>](#specify-the-data-type)
3. [<span data-ttu-id="f7852-128">Festlegen des OMA-URI-Werts</span><span class="sxs-lookup"><span data-stu-id="f7852-128">Set the OMA-URI value</span></span>](#set-the-value-for-a-browser-policy)

### <span data-ttu-id="f7852-129">Erstellen des OMA-URI-Pfads</span><span class="sxs-lookup"><span data-stu-id="f7852-129">Create the OMA-URI path</span></span>

<span data-ttu-id="f7852-130">Verwenden Sie die folgende Formel als Leitfaden zum Erstellen der OMA-URI-Pfade.</span><span class="sxs-lookup"><span data-stu-id="f7852-130">Use the following formula as a guide for creating the OMA-URI paths.</span></span> <br/><br/>
*`./Device/Vendor/MSFT/Policy/Config/<ADMXIngestName>~Policy~<ADMXNamespace>~<ADMXCategory>/<PolicyName>`* <br/><br/>

| <span data-ttu-id="f7852-131">Parameter</span><span class="sxs-lookup"><span data-stu-id="f7852-131">Parameter</span></span>         | <span data-ttu-id="f7852-132">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f7852-132">Description</span></span>                                                                                   |
|-------------------|-----------------------------------------------------------------------------------------------|
| \<ADMXIngestName> | <span data-ttu-id="f7852-133">Verwenden Sie „Edge” oder das, was Sie beim Aufnehmen der administrativen Vorlage definiert haben.</span><span class="sxs-lookup"><span data-stu-id="f7852-133">Use "Edge" or what you defined when ingesting the administrative template.</span></span> <span data-ttu-id="f7852-134">Wenn Sie z. B. „./Device/Vendor/MSFT/Policy/ConfigOperations/ADMXInstall/MicrosoftEdge/Policy/EdgeAdmx” verwendet haben, verwenden Sie „MicrosoftEdge”.</span><span class="sxs-lookup"><span data-stu-id="f7852-134">For example, if you used "./Device/Vendor/MSFT/Policy/ConfigOperations/ADMXInstall/MicrosoftEdge/Policy/EdgeAdmx", then use "MicrosoftEdge".</span></span><br/><br/> <span data-ttu-id="f7852-135">Der `<ADMXIngestionName>` muss mit jenem übereinstimmen, den Sie beim Aufnehmen der ADMX-Datei verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="f7852-135">The `<ADMXIngestionName>` must match what was used when you ingested the ADMX file.</span></span> |
| \<ADMXNamespace>  | <span data-ttu-id="f7852-136">Entweder „microsoft_edge” oder „microsoft_edge_recommended”, je nachdem, ob Sie eine obligatorische oder empfohlene Richtlinie festlegen.</span><span class="sxs-lookup"><span data-stu-id="f7852-136">Either "microsoft_edge" or "microsoft_edge_recommended" depending on whether you're setting a mandatory or recommended policy.</span></span> |
| \<ADMXCategory>   | <span data-ttu-id="f7852-137">Die „parentCategory” der Richtlinie wird in der ADMX-Datei definiert.</span><span class="sxs-lookup"><span data-stu-id="f7852-137">The "parentCategory" of the policy is defined in the ADMX file.</span></span> <span data-ttu-id="f7852-138">Lassen Sie `<ADMXCategory>` aus, wenn die Richtlinie nicht gruppiert ist (keine „parentCategory” definiert).</span><span class="sxs-lookup"><span data-stu-id="f7852-138">Omit the `<ADMXCategory>` if the policy isn't grouped (No "parentCategory" defined).</span></span> |
| \<PolicyName>     | <span data-ttu-id="f7852-139">Den Richtliniennamen finden Sie im Referenzartikel [](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies) zur Browserrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="f7852-139">The policy name can be found in the [Browser policy reference](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies) article.</span></span> |

#### <span data-ttu-id="f7852-140">URI-Pfadbeispiel:</span><span class="sxs-lookup"><span data-stu-id="f7852-140">URI path example:</span></span>

<span data-ttu-id="f7852-141">In diesem Beispiel wird davon ausgegangen, dass der Name des `<ADMXIngestName>`-Knotens „Edge” lautet, und Sie eine obligatorische Richtlinie festlegen.</span><span class="sxs-lookup"><span data-stu-id="f7852-141">For this example, assume the `<ADMXIngestName>` node was named “Edge" and you're setting a mandatory policy.</span></span> <span data-ttu-id="f7852-142">Der URI-Pfad wäre demnach:</span><span class="sxs-lookup"><span data-stu-id="f7852-142">The URI path would be:</span></span><br/><br/>
*`./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~<ADMXCategory>/<PolicyName>`*

<span data-ttu-id="f7852-143">Wenn sich die Richtlinie nicht in einer Gruppe befindet (z. B. DiskCacheSize), entfernen Sie „`~<ADMXCategory>`”.</span><span class="sxs-lookup"><span data-stu-id="f7852-143">If the policy isn't in a group (for example, DiskCacheSize) remove "`~<ADMXCategory>`".</span></span> <span data-ttu-id="f7852-144">Ersetzen Sie `<PolicyName>` durch den Namen der Richtlinie, DiskCacheSize.</span><span class="sxs-lookup"><span data-stu-id="f7852-144">Replace `<PolicyName>` with the name of the policy, DiskCacheSize.</span></span> <span data-ttu-id="f7852-145">Der URI-Pfad wäre demnach:</span><span class="sxs-lookup"><span data-stu-id="f7852-145">The URI path would be:</span></span><br/><br/>
*`./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge/DiskCacheSize`*

<span data-ttu-id="f7852-146">Wenn sich die Richtlinie in einer Gruppe befindet, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="f7852-146">If the policy is in a group, follow these steps:</span></span>

1. <span data-ttu-id="f7852-147">Öffnen Sie **msedge.admx** mit einem beliebigen XML-Editor.</span><span class="sxs-lookup"><span data-stu-id="f7852-147">Open **msedge.admx** with any xml editor.</span></span>
2. <span data-ttu-id="f7852-148">Suchen Sie nach dem Richtliniennamen, den Sie festlegen möchten.</span><span class="sxs-lookup"><span data-stu-id="f7852-148">Search for the policy name you want to set.</span></span> <span data-ttu-id="f7852-149">Zum Beispiel „ExtensionInstallForceList”.</span><span class="sxs-lookup"><span data-stu-id="f7852-149">For example, "ExtensionInstallForceList".</span></span>
3. <span data-ttu-id="f7852-150">Verwenden Sie den Wert des *ref*-Attributs aus dem *parentCategory*-Element.</span><span class="sxs-lookup"><span data-stu-id="f7852-150">Use the value of the *ref* attribute from the *parentCategory* element.</span></span> <span data-ttu-id="f7852-151">Zum Beispiel „Erweiterungen“ aus \<parentCategory ref=" Extensions"/>.</span><span class="sxs-lookup"><span data-stu-id="f7852-151">For example, "Extensions" from \<parentCategory ref=" Extensions"/>.</span></span>
4. <span data-ttu-id="f7852-152">Ersetzen Sie `<ADMXCategory>` durch den *ref*-Attributwert, um den URI-Pfad zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f7852-152">Replace `<ADMXCategory>` with the *ref* attribute value to construct the URI path.</span></span> <span data-ttu-id="f7852-153">Der URI-Pfad wäre demnach:</span><span class="sxs-lookup"><span data-stu-id="f7852-153">The URI path would be:</span></span><br/><br/>
*`/Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Extensions/ExtensionInstallForcelist`*

### <span data-ttu-id="f7852-154">Angabe des Datentyps</span><span class="sxs-lookup"><span data-stu-id="f7852-154">Specify the data type</span></span>

<span data-ttu-id="f7852-155">Der OMA-URI-Datentyp ist immer „Zeichenfolge””.</span><span class="sxs-lookup"><span data-stu-id="f7852-155">The OMA-URI data type is always “String”.</span></span>

### <span data-ttu-id="f7852-156">Festlegen des Werts für eine Browserrichtlinie</span><span class="sxs-lookup"><span data-stu-id="f7852-156">Set the value for a browser policy</span></span>

<span data-ttu-id="f7852-157">In diesem Abschnitt wird beschrieben, wie Sie den Wert im XML-Format für jeden Datentyp festlegen.</span><span class="sxs-lookup"><span data-stu-id="f7852-157">This section describes how to set the value, in XML format, for each data type.</span></span> <span data-ttu-id="f7852-158">Wechseln Sie zur [Browserrichtlinien-Referenz](https://docs.microsoft.com/deployedge/microsoft-edge-policies), um nach dem Datentyp der Richtlinie zu suchen.</span><span class="sxs-lookup"><span data-stu-id="f7852-158">Go to [Browser policy reference](https://docs.microsoft.com/deployedge/microsoft-edge-policies) to look up the data type of the policy.</span></span>

> [!NOTE]
> <span data-ttu-id="f7852-159">Bei nicht-booleschen Datentypen beginnt der Wert immer mit `<enabled/>`.</span><span class="sxs-lookup"><span data-stu-id="f7852-159">For non-Boolean data types, the value always starts with `<enabled/>`.</span></span>

#### <span data-ttu-id="f7852-160">Boolescher Datentyp</span><span class="sxs-lookup"><span data-stu-id="f7852-160">Boolean data type</span></span>

<span data-ttu-id="f7852-161">Verwenden Sie für Richtlinien des booleschen Typs `<enabled/>` oder `<disabled/>`.</span><span class="sxs-lookup"><span data-stu-id="f7852-161">For policies that are Boolean types use `<enabled/>` or `<disabled/>`.</span></span>

#### <span data-ttu-id="f7852-162">Datentyp „Ganze Zahl”</span><span class="sxs-lookup"><span data-stu-id="f7852-162">Integer data type</span></span>

<span data-ttu-id="f7852-163">Der Wert muss immer mit dem `<enabled/>`-Element gefolgt von `<data id="[valueName]" value="[decimal value]"/>` beginnen.</span><span class="sxs-lookup"><span data-stu-id="f7852-163">The value always needs to start with the `<enabled/>` element followed by `<data id="[valueName]" value="[decimal value]"/>`.</span></span>

<span data-ttu-id="f7852-164">Führen Sie die folgenden Schritte aus, um den Wertnamen und den Dezimalwert für eine neue Registerkartenseite zu finden:</span><span class="sxs-lookup"><span data-stu-id="f7852-164">To find the value name and decimal value for a new tab page, use the following steps:</span></span>

1. <span data-ttu-id="f7852-165">Öffnen Sie **msedge.admx** mit einem beliebigen XML-Editor.</span><span class="sxs-lookup"><span data-stu-id="f7852-165">Open **msedge.admx** with any xml editor.</span></span>
2. <span data-ttu-id="f7852-166">Suchen Sie nach dem `<policy>`-Element, bei dem das Namensattribut mit dem Richtliniennamen übereinstimmt, den Sie festlegen möchten.</span><span class="sxs-lookup"><span data-stu-id="f7852-166">Search for the `<policy>` element where the name attribute matches the policy name you want to set.</span></span> <span data-ttu-id="f7852-167">Suchen Sie für „RestoreOnStartup” nach `name="RestoreOnStartup"`.</span><span class="sxs-lookup"><span data-stu-id="f7852-167">For "RestoreOnStartup", search for `name="RestoreOnStartup"`.</span></span>
3. <span data-ttu-id="f7852-168">Suchen Sie im `<elements>`-Knoten nach dem Wert, den Sie festlegen möchten.</span><span class="sxs-lookup"><span data-stu-id="f7852-168">In the `<elements>` node, find the value you want to set.</span></span>
4. <span data-ttu-id="f7852-169">Verwenden Sie den Wert im „valueName”-Attribut im `<elements>`-Knoten.</span><span class="sxs-lookup"><span data-stu-id="f7852-169">Use the value in the "valueName" attribute in the `<elements>` node.</span></span> <span data-ttu-id="f7852-170">Für „RestoreOnStartup” lautet der „valueName” „RestoreOnStartup”.</span><span class="sxs-lookup"><span data-stu-id="f7852-170">For "RestoreOnStartup" the "valueName" is "RestoreOnStartup".</span></span>
5. <span data-ttu-id="f7852-171">Verwenden Sie den Wert im „value”-Attribut im `<decimal>`-Knoten.</span><span class="sxs-lookup"><span data-stu-id="f7852-171">Use the value in the "value" attribute in the `<decimal>` node.</span></span> <span data-ttu-id="f7852-172">Damit „RestoreOnStartup” die neue Registerkartenseite öffnet, lautet der Wert „5”.</span><span class="sxs-lookup"><span data-stu-id="f7852-172">For "RestoreOnStartup" to open the new tab page the value is "5".</span></span>

<span data-ttu-id="f7852-173">So öffnen Sie die neue Registerkartenseite beim Start:</span><span class="sxs-lookup"><span data-stu-id="f7852-173">To open the new tab page on startup use:</span></span><br>
`<enabled/> <data id="RestoreOnStartup" value="5"/>`

#### <span data-ttu-id="f7852-174">Liste der Datentypen „Zeichenfolge”</span><span class="sxs-lookup"><span data-stu-id="f7852-174">List of strings data type</span></span>

<span data-ttu-id="f7852-175">Der Wert muss immer mit dem `<enabled/>`-Element gefolgt von `<data id="[listID]" value="[string 1];[string 2];[string 3]"/>` beginnen.</span><span class="sxs-lookup"><span data-stu-id="f7852-175">The value always needs to start with the `<enabled/>` element followed by `<data id="[listID]" value="[string 1];[string 2];[string 3]"/>`.</span></span>

> [!NOTE]
> <span data-ttu-id="f7852-176">Der Attributname „id =” ist nicht der Richtlinienname, obwohl er in den meisten Fällen mit dem Richtliniennamen übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="f7852-176">The "id=" attribute name isn't the policy name, even though in most cases it matches the policy name.</span></span> <span data-ttu-id="f7852-177">Dies ist der Knoten-ID-Attributwert \<list>, der in der ADMX-Datei enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="f7852-177">It's the \<list> node id attribute value, which is found in the ADMX file.</span></span>

<span data-ttu-id="f7852-178">Gehen Sie folgendermaßen vor, um nach der listID zu suchen und den Wert zum Blockieren einer URL zu definieren:</span><span class="sxs-lookup"><span data-stu-id="f7852-178">To find the listID and define the value to block a URL, follow these steps:</span></span>

1. <span data-ttu-id="f7852-179">Öffnen Sie **msedge.admx** mit einem beliebigen XML-Editor.</span><span class="sxs-lookup"><span data-stu-id="f7852-179">Open **msedge.admx** with any xml editor.</span></span>
2. <span data-ttu-id="f7852-180">Suchen Sie nach dem `<policy>`-Element, bei dem das Namensattribut mit dem Richtliniennamen übereinstimmt, den Sie festlegen möchten.</span><span class="sxs-lookup"><span data-stu-id="f7852-180">Search for the `<policy>` element where the name attribute matches the policy name you want to set.</span></span> <span data-ttu-id="f7852-181">Suchen Sie für „URLBlocklist” nach `name="URLBlocklist"`.</span><span class="sxs-lookup"><span data-stu-id="f7852-181">For "URLBlocklist", search for `name="URLBlocklist"`.</span></span>
3. <span data-ttu-id="f7852-182">Verwenden Sie den Wert im „id”-Attribut von `<list> node for [listID]`.</span><span class="sxs-lookup"><span data-stu-id="f7852-182">Use the value in the "id" attribute of the `<list> node for [listID]`.</span></span>
4. <span data-ttu-id="f7852-183">Der "Wert" ist eine durch ein Semikolon (;) getrennte Liste von URLs.</span><span class="sxs-lookup"><span data-stu-id="f7852-183">The "value" is a list of URLs separated by a semicolon (;)</span></span>

<span data-ttu-id="f7852-184">Gehen Sie folgendermaßen vor, um z. B. den Zugriff auf `contoso.com` und `https://ssl.server.com` zu blockieren:</span><span class="sxs-lookup"><span data-stu-id="f7852-184">For example, to block access to `contoso.com` and `https://ssl.server.com`:</span></span><br>
`<enabled/> <data id=" URLBlocklistDesc" value="contoso.com;https://ssl.server.com"/>`

#### <span data-ttu-id="f7852-185">Datentyp „Dictionary” oder „Zeichenfolge”</span><span class="sxs-lookup"><span data-stu-id="f7852-185">Dictionary or String data type</span></span>

<span data-ttu-id="f7852-186">Der Wert muss immer mit `<enabled/>` gefolgt von `<data id="[textID]" value="[string]"/>` beginnen.</span><span class="sxs-lookup"><span data-stu-id="f7852-186">The value always needs to start with the `<enabled/>` followed by `<data id="[textID]" value="[string]"/>` .</span></span>

<span data-ttu-id="f7852-187">Gehen Sie folgendermaßen vor, um nach der textID zu suchen und den Wert zum Festlegen des Gebietsschemas zu definieren:</span><span class="sxs-lookup"><span data-stu-id="f7852-187">To find the textID and define the value set the locale, follow these steps:</span></span>

1. <span data-ttu-id="f7852-188">Öffnen Sie **msedge.admx** mit einem beliebigen XML-Editor.</span><span class="sxs-lookup"><span data-stu-id="f7852-188">Open **msedge.admx** with any xml editor.</span></span>
2. <span data-ttu-id="f7852-189">Suchen Sie nach dem `<policy>`-Element, bei dem das Namensattribut mit dem Richtliniennamen übereinstimmt, den Sie festlegen möchten.</span><span class="sxs-lookup"><span data-stu-id="f7852-189">Search for the `<policy>` element where the name attribute matches the policy name you want to set.</span></span> <span data-ttu-id="f7852-190">Suchen Sie für „ApplicationLocaleValue” nach `name="ApplicationLocaleValue"`.</span><span class="sxs-lookup"><span data-stu-id="f7852-190">For "ApplicationLocaleValue", search for `name="ApplicationLocaleValue"`.</span></span>
3. <span data-ttu-id="f7852-191">Verwenden Sie den Wert im „id”-Attribut von `<text>`-Knoten für `[textID]`.</span><span class="sxs-lookup"><span data-stu-id="f7852-191">Use the value in the "id" attribute of the `<text>` node for `[textID]`.</span></span>
4. <span data-ttu-id="f7852-192">Setzen Sie den „Wert” auf den Kulturcode.</span><span class="sxs-lookup"><span data-stu-id="f7852-192">Set the "value" to the culture code.</span></span>

<span data-ttu-id="f7852-193">So legen Sie das Gebietsschema mit der Richtlinie „ApplicationLocaleValue” auf „en-US” fest:</span><span class="sxs-lookup"><span data-stu-id="f7852-193">To set the locale to "es-US" with the "ApplicationLocaleValue" policy:</span></span><br>
`<enabled/> <data id="ApplicationLocaleValue" value="es-US"/>`

### <span data-ttu-id="f7852-194">Erstellen des OMA-URI für eine empfohlene Richtlinie</span><span class="sxs-lookup"><span data-stu-id="f7852-194">Create the OMA-URI for a recommended policies</span></span>

<span data-ttu-id="f7852-195">Die Definition des URI-Pfads für empfohlene Richtlinien hängt von der zu konfigurierenden Richtlinie ab.</span><span class="sxs-lookup"><span data-stu-id="f7852-195">Defining the URI path for recommended policies depends on the policy you want to configure.</span></span>

#### <span data-ttu-id="f7852-196">So definieren Sie den URI-Pfad für eine empfohlene Richtlinie</span><span class="sxs-lookup"><span data-stu-id="f7852-196">To define the URI path for a recommended policy</span></span>

<span data-ttu-id="f7852-197">Verwenden Sie die URI-Pfadformel (*`./Device/Vendor/MSFT/Policy/Config/<ADMXIngestName>~Policy~<ADMXNamespace>~<ADMXCategory>/<PolicyName>`*) und führen Sie die folgenden Schritte aus, um den URI-Pfad zu definieren:</span><span class="sxs-lookup"><span data-stu-id="f7852-197">Use the URI path formula (*`./Device/Vendor/MSFT/Policy/Config/<ADMXIngestName>~Policy~<ADMXNamespace>~<ADMXCategory>/<PolicyName>`*) and the following steps to define the URI path:</span></span>

1. <span data-ttu-id="f7852-198">Öffnen Sie **msedge.admx** mit einem beliebigen XML-Editor.</span><span class="sxs-lookup"><span data-stu-id="f7852-198">Open **msedge.admx** with any xml editor.</span></span>
2. <span data-ttu-id="f7852-199">Wenn die Richtlinie, die Sie konfigurieren möchten, nicht in einer Gruppe ist, fahren Sie mit Schritt 4 fort, und entfernen Sie `~<ADMXCategory>` aus dem Pfad.</span><span class="sxs-lookup"><span data-stu-id="f7852-199">If the policy you want to configure isn't in a group, skip to step 4 and remove `~<ADMXCategory>` from the path.</span></span>
3. <span data-ttu-id="f7852-200">Wenn die Richtlinie, die Sie konfigurieren möchten, in einer Gruppe ist:</span><span class="sxs-lookup"><span data-stu-id="f7852-200">If the policy you want to configure is in a group:</span></span>

   - <span data-ttu-id="f7852-201">Um nach `<ADMXCategory>` zu suchen, suchen Sie nach der Richtlinie, die Sie festlegen möchten.</span><span class="sxs-lookup"><span data-stu-id="f7852-201">To look up the `<ADMXCategory>`, search for the policy you want to set.</span></span> <span data-ttu-id="f7852-202">Fügen Sie beim Suchen „_recommended” an den Richtliniennamen an.</span><span class="sxs-lookup"><span data-stu-id="f7852-202">When searching append "_recommended" to the policy name.</span></span> <span data-ttu-id="f7852-203">Eine Suche nach „RegisteredProtocolHandlers_recommended” gibt beispielsweise folgendes Ergebnis zurück:</span><span class="sxs-lookup"><span data-stu-id="f7852-203">For example, a search for "RegisteredProtocolHandlers_recommended” has the following result:</span></span>

        ```xml
         <policy class="Both" displayName="$(string.RegisteredProtocolHandlers)" explainText="$(string.RegisteredProtocolHandlers_Explain)" key="Software\Policies\Microsoft\Edge\Recommended" name="RegisteredProtocolHandlers_recommended" presentation="$(presentation.RegisteredProtocolHandlers)">
           <parentCategory ref="ContentSettings_recommended"/>
           <supportedOn ref="SUPPORTED_WIN7_V77"/>
           <elements>
             <text id="RegisteredProtocolHandlers" maxLength="1000000" valueName="RegisteredProtocolHandlers"/>
           </elements>
         </policy>
        ```

   - <span data-ttu-id="f7852-204">Kopieren Sie den Wert des *ref*-Attributs aus dem `<parentCategory>`-Element.</span><span class="sxs-lookup"><span data-stu-id="f7852-204">Copy the value of the *ref* attribute from the `<parentCategory>` element.</span></span> <span data-ttu-id="f7852-205">Kopieren Sie für „ContentSettings” „ContentSettings_recommended” aus `<parentCategory ref=" ContentSettings_recommended"/>`.</span><span class="sxs-lookup"><span data-stu-id="f7852-205">For "ContentSettings", copy "ContentSettings_recommended" from `<parentCategory ref=" ContentSettings_recommended"/>`.</span></span>
   - <span data-ttu-id="f7852-206">Ersetzen Sie `<ADMXCategory>` durch den *ref*-Attributwert, um den URI-Pfad in der URI-Pfadformel zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f7852-206">Replace `<ADMXCategory>` with the *ref* attribute value to construct the URI path in the URI path formula.</span></span>

4. <span data-ttu-id="f7852-207">`<PolicyName>` ist der Name der Richtlinie, an die „_recommended” angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="f7852-207">The `<PolicyName>` is the name of the policy with "_recommended" appended to it.</span></span>

#### <span data-ttu-id="f7852-208">OMA-URI-Pfadbeispiele für empfohlene Richtlinien</span><span class="sxs-lookup"><span data-stu-id="f7852-208">OMA-URI path examples for recommended policies</span></span>

<span data-ttu-id="f7852-209">In der folgenden Tabelle sind Beispiele für OMA-URI-Pfade für empfohlene Richtlinien aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="f7852-209">The following table shows examples of OMA-URI paths for recommended policies.</span></span>

|              <span data-ttu-id="f7852-210">Richtlinie</span><span class="sxs-lookup"><span data-stu-id="f7852-210">Policy</span></span>               |             <span data-ttu-id="f7852-211">OMA-URI</span><span class="sxs-lookup"><span data-stu-id="f7852-211">OMA-URI</span></span>                      |
|-----------------------------------|------------------------------------------|
| [<span data-ttu-id="f7852-212">RegisteredProtocolHandlers</span><span class="sxs-lookup"><span data-stu-id="f7852-212">RegisteredProtocolHandlers</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#registeredprotocolhandlers)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~ContentSettings_recommended/RegisteredProtocolHandlers_recommended`                        |
| [<span data-ttu-id="f7852-213">PasswordManagerEnabled</span><span class="sxs-lookup"><span data-stu-id="f7852-213">PasswordManagerEnabled</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#passwordmanagerenabled)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~PasswordManager_recommended/PasswordManagerEnabled_recommended`                        |
| [<span data-ttu-id="f7852-214">PrintHeaderFooter</span><span class="sxs-lookup"><span data-stu-id="f7852-214">PrintHeaderFooter</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#printheaderfooter)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~Printing_recommended/PrintHeaderFooter_recommended`                        |
| [<span data-ttu-id="f7852-215">SmartScreenEnabled</span><span class="sxs-lookup"><span data-stu-id="f7852-215">SmartScreenEnabled</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#smartscreenenabled)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~SmartScreen_recommended/SmartScreenEnabled_recommended`                        |
| [<span data-ttu-id="f7852-216">HomePageLocation</span><span class="sxs-lookup"><span data-stu-id="f7852-216">HomePageLocation</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#homepagelocation)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~Startup_recommended/HomepageLocation_recommended`                        |
| [<span data-ttu-id="f7852-217">ShowHomeButton</span><span class="sxs-lookup"><span data-stu-id="f7852-217">ShowHomeButton</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#showhomebutton)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~Startup_recommended/ShowHomeButton_recommended`                        |
| [<span data-ttu-id="f7852-218">FavoritesBarEnabled</span><span class="sxs-lookup"><span data-stu-id="f7852-218">FavoritesBarEnabled</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#favoritesbarenabled)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~/FavoritesBarEnabled_recommended`                        |

### <span data-ttu-id="f7852-219">OMA-URI-Beispiele</span><span class="sxs-lookup"><span data-stu-id="f7852-219">OMA-URI examples</span></span>

<span data-ttu-id="f7852-220">OMA-URI-Beispiele mit ihrem URI-Pfad, Typ und einem Beispielwert.</span><span class="sxs-lookup"><span data-stu-id="f7852-220">OMA-URI examples with their URI path, type, and an example value.</span></span>

#### <span data-ttu-id="f7852-221">Boolescher Datentyp-Beispiele</span><span class="sxs-lookup"><span data-stu-id="f7852-221">Boolean data type examples</span></span>

*<span data-ttu-id="f7852-222">[ShowHomeButton](https://docs.microsoft.com/deployedge/microsoft-edge-policies#ShowHomeButton):</span><span class="sxs-lookup"><span data-stu-id="f7852-222">[ShowHomeButton](https://docs.microsoft.com/deployedge/microsoft-edge-policies#ShowHomeButton):</span></span>*

| <span data-ttu-id="f7852-223">Feld</span><span class="sxs-lookup"><span data-stu-id="f7852-223">Field</span></span>   | <span data-ttu-id="f7852-224">Wert</span><span class="sxs-lookup"><span data-stu-id="f7852-224">Value</span></span>                                                                                |
|---------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f7852-225">Name</span><span class="sxs-lookup"><span data-stu-id="f7852-225">Name</span></span>    | <span data-ttu-id="f7852-226">Microsoft Edge: ShowHomeButton</span><span class="sxs-lookup"><span data-stu-id="f7852-226">Microsoft Edge: ShowHomeButton</span></span>                                                       |
| <span data-ttu-id="f7852-227">OMA-URI</span><span class="sxs-lookup"><span data-stu-id="f7852-227">OMA-URI</span></span> | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Startup/ShowHomeButton` |
| <span data-ttu-id="f7852-228">Typ</span><span class="sxs-lookup"><span data-stu-id="f7852-228">type</span></span>    | <span data-ttu-id="f7852-229">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f7852-229">String</span></span>                                                                               |
| <span data-ttu-id="f7852-230">Wert</span><span class="sxs-lookup"><span data-stu-id="f7852-230">Value</span></span>   | `<enabled/>`                                                                          |

*<span data-ttu-id="f7852-231">[DefaultSearchProviderEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#DefaultSearchProviderEnabled):</span><span class="sxs-lookup"><span data-stu-id="f7852-231">[DefaultSearchProviderEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#DefaultSearchProviderEnabled):</span></span>*

| <span data-ttu-id="f7852-232">Feld</span><span class="sxs-lookup"><span data-stu-id="f7852-232">Field</span></span>   | <span data-ttu-id="f7852-233">Wert</span><span class="sxs-lookup"><span data-stu-id="f7852-233">Value</span></span>                                                                                |
|---------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f7852-234">Name</span><span class="sxs-lookup"><span data-stu-id="f7852-234">Name</span></span>    | <span data-ttu-id="f7852-235">Microsoft Edge: DefaultSearchProviderEnabled</span><span class="sxs-lookup"><span data-stu-id="f7852-235">Microsoft Edge: DefaultSearchProviderEnabled</span></span>                                         |
| <span data-ttu-id="f7852-236">OMA-URI</span><span class="sxs-lookup"><span data-stu-id="f7852-236">OMA-URI</span></span> | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~DefaultSearchProvider/DefaultSearchProviderEnabled`    |
| <span data-ttu-id="f7852-237">Typ</span><span class="sxs-lookup"><span data-stu-id="f7852-237">type</span></span>    | <span data-ttu-id="f7852-238">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f7852-238">String</span></span>                                                                               |
| <span data-ttu-id="f7852-239">Wert</span><span class="sxs-lookup"><span data-stu-id="f7852-239">Value</span></span>   | `<disable/>`                                                                          |

### <span data-ttu-id="f7852-240">Datentyp „Ganze Zahl”-Beispiele</span><span class="sxs-lookup"><span data-stu-id="f7852-240">Integer data type examples</span></span>

*<span data-ttu-id="f7852-241">[AutoImportAtFirstRun](https://docs.microsoft.com/deployedge/microsoft-edge-policies#AutoImportAtFirstRun):</span><span class="sxs-lookup"><span data-stu-id="f7852-241">[AutoImportAtFirstRun](https://docs.microsoft.com/deployedge/microsoft-edge-policies#AutoImportAtFirstRun):</span></span>*

| <span data-ttu-id="f7852-242">Feld</span><span class="sxs-lookup"><span data-stu-id="f7852-242">Field</span></span>   | <span data-ttu-id="f7852-243">Wert</span><span class="sxs-lookup"><span data-stu-id="f7852-243">Value</span></span>                                                                                |
|---------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f7852-244">Name</span><span class="sxs-lookup"><span data-stu-id="f7852-244">Name</span></span>    | <span data-ttu-id="f7852-245">Microsoft Edge: AutoImportAtFirstRun</span><span class="sxs-lookup"><span data-stu-id="f7852-245">Microsoft Edge: AutoImportAtFirstRun</span></span>                                                 |
| <span data-ttu-id="f7852-246">OMA-URI</span><span class="sxs-lookup"><span data-stu-id="f7852-246">OMA-URI</span></span> | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge/AutoImportAtFirstRun`   |
| <span data-ttu-id="f7852-247">Typ</span><span class="sxs-lookup"><span data-stu-id="f7852-247">type</span></span>    | <span data-ttu-id="f7852-248">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f7852-248">String</span></span>                                                                               |
| <span data-ttu-id="f7852-249">Wert</span><span class="sxs-lookup"><span data-stu-id="f7852-249">Value</span></span>   | `<enabled/><data id="AutoImportAtFirstRun" value="1"/>`                             |

*<span data-ttu-id="f7852-250">[DefaultImagesSetting](https://docs.microsoft.com/deployedge/microsoft-edge-policies#DefaultImagesSetting):</span><span class="sxs-lookup"><span data-stu-id="f7852-250">[DefaultImagesSetting](https://docs.microsoft.com/deployedge/microsoft-edge-policies#DefaultImagesSetting):</span></span>*

| <span data-ttu-id="f7852-251">Feld</span><span class="sxs-lookup"><span data-stu-id="f7852-251">Field</span></span>   | <span data-ttu-id="f7852-252">Wert</span><span class="sxs-lookup"><span data-stu-id="f7852-252">Value</span></span>                                                                                |
|---------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f7852-253">Name</span><span class="sxs-lookup"><span data-stu-id="f7852-253">Name</span></span>    | <span data-ttu-id="f7852-254">Microsoft Edge: DefaultImagesSetting</span><span class="sxs-lookup"><span data-stu-id="f7852-254">Microsoft Edge: DefaultImagesSetting</span></span>                                                 |
| <span data-ttu-id="f7852-255">OMA-URI</span><span class="sxs-lookup"><span data-stu-id="f7852-255">OMA-URI</span></span> | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~ContentSettings/DefaultImagesSetting`    |
| <span data-ttu-id="f7852-256">Typ</span><span class="sxs-lookup"><span data-stu-id="f7852-256">type</span></span>    | <span data-ttu-id="f7852-257">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f7852-257">String</span></span>                                                                               |
| <span data-ttu-id="f7852-258">Wert</span><span class="sxs-lookup"><span data-stu-id="f7852-258">Value</span></span>   | `<enabled/><data id="DefaultImagesSetting" value="2"/>`                             |

*<span data-ttu-id="f7852-259">[DiskCacheSize](https://docs.microsoft.com/deployedge/microsoft-edge-policies#DiskCacheSize):</span><span class="sxs-lookup"><span data-stu-id="f7852-259">[DiskCacheSize](https://docs.microsoft.com/deployedge/microsoft-edge-policies#DiskCacheSize):</span></span>*

| <span data-ttu-id="f7852-260">Feld</span><span class="sxs-lookup"><span data-stu-id="f7852-260">Field</span></span>   | <span data-ttu-id="f7852-261">Wert</span><span class="sxs-lookup"><span data-stu-id="f7852-261">Value</span></span>                                                                                |
|---------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f7852-262">Name</span><span class="sxs-lookup"><span data-stu-id="f7852-262">Name</span></span>    | <span data-ttu-id="f7852-263">Microsoft Edge: DiskCacheSize</span><span class="sxs-lookup"><span data-stu-id="f7852-263">Microsoft Edge: DiskCacheSize</span></span>                                                        |
| <span data-ttu-id="f7852-264">OMA-URI</span><span class="sxs-lookup"><span data-stu-id="f7852-264">OMA-URI</span></span> | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge/DiskCacheSize`        |
| <span data-ttu-id="f7852-265">Typ</span><span class="sxs-lookup"><span data-stu-id="f7852-265">type</span></span>    | <span data-ttu-id="f7852-266">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f7852-266">String</span></span>                                                                               |
| <span data-ttu-id="f7852-267">Wert</span><span class="sxs-lookup"><span data-stu-id="f7852-267">Value</span></span>   | `<enabled/><data id="DiskCacheSize" value="1000000"/>`                               |

#### <span data-ttu-id="f7852-268">Liste der Beispiele für den Datentyp „Zeichenfolge”</span><span class="sxs-lookup"><span data-stu-id="f7852-268">List of strings data type examples</span></span>
<!--
*[NotificationsAllowedForUrls](https://docs.microsoft.com/deployedge/microsoft-edge-policies#NotificationsAllowedForUrls):*

| Field   | Value                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Name    | Microsoft Edge: NotificationsAllowedForUrls                                          |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~ContentSettings/NotificationsAllowedForUrls`    |
| Type    | String                                                                               |
| Value   | `<enabled/><data id="NotificationsAllowedForUrlsDesc" value="https://www.contoso.com"/>`<br>For multiple list items: `<data id="NotificationsAllowedForUrlsDesc" value="https://www.contoso.com;[*.]contoso.edu"/>`                               |
-->
*<span data-ttu-id="f7852-269">[RestoreOnStartupURLS](https://docs.microsoft.com/deployedge/microsoft-edge-policies#RestoreOnStartupURLS):</span><span class="sxs-lookup"><span data-stu-id="f7852-269">[RestoreOnStartupURLS](https://docs.microsoft.com/deployedge/microsoft-edge-policies#RestoreOnStartupURLS):</span></span>*

| <span data-ttu-id="f7852-270">Feld</span><span class="sxs-lookup"><span data-stu-id="f7852-270">Field</span></span>   | <span data-ttu-id="f7852-271">Wert</span><span class="sxs-lookup"><span data-stu-id="f7852-271">Value</span></span>                                                                                |
|---------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f7852-272">Name</span><span class="sxs-lookup"><span data-stu-id="f7852-272">Name</span></span>    | <span data-ttu-id="f7852-273">Microsoft Edge: RestoreOnStartupURLS</span><span class="sxs-lookup"><span data-stu-id="f7852-273">Microsoft Edge: RestoreOnStartupURLS</span></span>                                                 |
| <span data-ttu-id="f7852-274">OMA-URI</span><span class="sxs-lookup"><span data-stu-id="f7852-274">OMA-URI</span></span> | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Startup/RestoreOnStartupURLs`    |
| <span data-ttu-id="f7852-275">Typ</span><span class="sxs-lookup"><span data-stu-id="f7852-275">Type</span></span>    | <span data-ttu-id="f7852-276">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f7852-276">String</span></span>                                                                               |
| <span data-ttu-id="f7852-277">Wert</span><span class="sxs-lookup"><span data-stu-id="f7852-277">Value</span></span>   | `<enabled/><data id="RestoreOnStartupURLsDesc" value="1&#xF000;http://www.bing.com"/>`<br><span data-ttu-id="f7852-278">Für mehrere Listenelemente:</span><span class="sxs-lookup"><span data-stu-id="f7852-278">For multiple list items:</span></span> `<enabled/><data id="RestoreOnStartupURLsDesc" value="1&#xF000;http://www.bing.com&#xF000;2&#xF000;http://www.microsoft.com"/>`  |

*<span data-ttu-id="f7852-279">[ExtensionInstallForcelist](https://docs.microsoft.com/deployedge/microsoft-edge-policies#ExtensionInstallForcelist):</span><span class="sxs-lookup"><span data-stu-id="f7852-279">[ExtensionInstallForcelist](https://docs.microsoft.com/deployedge/microsoft-edge-policies#ExtensionInstallForcelist):</span></span>*

| <span data-ttu-id="f7852-280">Feld</span><span class="sxs-lookup"><span data-stu-id="f7852-280">Field</span></span>   | <span data-ttu-id="f7852-281">Wert</span><span class="sxs-lookup"><span data-stu-id="f7852-281">Value</span></span>                                                                                |
|---------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f7852-282">Name</span><span class="sxs-lookup"><span data-stu-id="f7852-282">Name</span></span>    | <span data-ttu-id="f7852-283">Microsoft Edge: ExtensionInstallForcelist</span><span class="sxs-lookup"><span data-stu-id="f7852-283">Microsoft Edge: ExtensionInstallForcelist</span></span>                                            |
| <span data-ttu-id="f7852-284">OMA-URI</span><span class="sxs-lookup"><span data-stu-id="f7852-284">OMA-URI</span></span> | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Extensions/ExtensionInstallForcelist`    |
| <span data-ttu-id="f7852-285">Typ</span><span class="sxs-lookup"><span data-stu-id="f7852-285">Type</span></span>    | <span data-ttu-id="f7852-286">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f7852-286">String</span></span>                                                                               |
| <span data-ttu-id="f7852-287">Wert</span><span class="sxs-lookup"><span data-stu-id="f7852-287">Value</span></span>   | `<enabled/><data id="ExtensionInstallForcelistDesc" value="1&#xF000;gbchcmhmhahfdphkhkmpfmihenigjmpp;https://extensionwebstorebase.edgesv.net/v1/crx"/>`                               |

#### <span data-ttu-id="f7852-288">Beispiel für Wörterbuch- und Zeichenfolgen-Datentyp</span><span class="sxs-lookup"><span data-stu-id="f7852-288">Dictionary and String data type example</span></span>

*<span data-ttu-id="f7852-289">[ProxyMode](https://docs.microsoft.com/deployedge/microsoft-edge-policies#ProxyMode):</span><span class="sxs-lookup"><span data-stu-id="f7852-289">[ProxyMode](https://docs.microsoft.com/deployedge/microsoft-edge-policies#ProxyMode):</span></span>*

| <span data-ttu-id="f7852-290">Feld</span><span class="sxs-lookup"><span data-stu-id="f7852-290">Field</span></span>   | <span data-ttu-id="f7852-291">Wert</span><span class="sxs-lookup"><span data-stu-id="f7852-291">Value</span></span>                                                                                |
|---------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f7852-292">Name</span><span class="sxs-lookup"><span data-stu-id="f7852-292">Name</span></span>    | <span data-ttu-id="f7852-293">Microsoft Edge: ProxyMode</span><span class="sxs-lookup"><span data-stu-id="f7852-293">Microsoft Edge: ProxyMode</span></span>                                                            |
| <span data-ttu-id="f7852-294">OMA-URI</span><span class="sxs-lookup"><span data-stu-id="f7852-294">OMA-URI</span></span> | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~ProxyMode/ProxyMode`  |
| <span data-ttu-id="f7852-295">Typ</span><span class="sxs-lookup"><span data-stu-id="f7852-295">Type</span></span>    | <span data-ttu-id="f7852-296">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f7852-296">String</span></span>                                                                               |
| <span data-ttu-id="f7852-297">Wert</span><span class="sxs-lookup"><span data-stu-id="f7852-297">Value</span></span>   | `<enabled/><data id="ProxyMode" value="auto_detect"/>`                               |

## <span data-ttu-id="f7852-298">Konfigurieren von Microsoft Edge in Intune mithilfe der ADMX-Aufnahme</span><span class="sxs-lookup"><span data-stu-id="f7852-298">Configure Microsoft Edge in Intune using ADMX ingestion</span></span>

<span data-ttu-id="f7852-299">Die empfohlene Methode zum Konfigurieren von Microsoft Edge mit Microsoft Intune ist die Verwendung des Profils „Administrative Vorlagen”, wie unter [Konfigurieren der Microsoft Edge-Richtlinieneinstellungen mit Microsoft Intune](https://docs.microsoft.com/deployedge/configure-edge-with-intune) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f7852-299">The recommended way to configure Microsoft Edge with Microsoft Intune is to use the Administrative Templates profile as described in [Configure Microsoft Edge policy settings with Microsoft Intune](https://docs.microsoft.com/deployedge/configure-edge-with-intune).</span></span> <span data-ttu-id="f7852-300">Wenn Sie eine Richtlinie auswerten möchten, die derzeit nicht im Microsoft Edge Administrative Vorlagen in Intune verfügbar ist, können Sie Microsoft Edge mithilfe [benutzerdefinierter Einstellungen für Windows 10-Geräte in Intune konfigurieren](https://docs.microsoft.com/intune/configuration/custom-settings-windows-10).</span><span class="sxs-lookup"><span data-stu-id="f7852-300">If you want to evaluate a policy that is currently not available in the Microsoft Edge Administrative Templates in Intune you can configure Microsoft Edge using  [custom settings for Windows 10 devices in Intune](https://docs.microsoft.com/intune/configuration/custom-settings-windows-10).</span></span>

<span data-ttu-id="f7852-301">In diesem Abschnitt wird das Verwenden von Hintergrundaufgaben beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f7852-301">This section describes how to:</span></span>

1. [<span data-ttu-id="f7852-302">Aufnehmen der Microsoft Edge ADMX-Datei in Intune</span><span class="sxs-lookup"><span data-stu-id="f7852-302">Ingest the Microsoft Edge ADMX file into Intune</span></span>](#ingest-the-microsoft-edge-admx-file-into-intune)
2. [<span data-ttu-id="f7852-303">Festlegen einer Richtlinie mit benutzerdefiniertem OMA-URI in Intune</span><span class="sxs-lookup"><span data-stu-id="f7852-303">Set a policy using custom OMA-URI in Intune</span></span>](#set-a-policy-using-custom-oma-uri-in-intune)

> [!IMPORTANT]
> <span data-ttu-id="f7852-304">Verwenden Sie als bewährte Methode kein benutzerdefiniertes OMA-URI-Profil und kein administratives Vorlagenprofil, um dieselbe Microsoft Edge-Einstellung in Intune zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="f7852-304">As a best practice, don’t use a custom OMA-URI profile and an Administration templates profile to configure the same Microsoft Edge setting in Intune.</span></span> <span data-ttu-id="f7852-305">Wenn Sie die gleiche Richtlinie mit einem benutzerdefinierten OMA-URI und einem administrativen Vorlagenprofil, aber mit unterschiedlichen Werten bereitstellen, erhalten Benutzer unvorhersehbare Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="f7852-305">If you deploy the same policy using both a custom OMA-URI  and an Administrative template profile, but with different values, users will get unpredictable results.</span></span> <span data-ttu-id="f7852-306">Es wird dringend empfohlen, das OMA-URI-Profil zu entfernen, bevor Sie ein administratives Vorlagenprofil verwenden.</span><span class="sxs-lookup"><span data-stu-id="f7852-306">We strongly recommend removing your OMA-URI profile before using an Administration templates profile.</span></span>

### <span data-ttu-id="f7852-307">Aufnehmen der Microsoft Edge ADMX-Datei in Intune</span><span class="sxs-lookup"><span data-stu-id="f7852-307">Ingest the Microsoft Edge ADMX file into Intune</span></span>

<span data-ttu-id="f7852-308">In diesem Abschnitt wird beschrieben, wie die Microsoft Edge administrative Vorlage (**msedge.admx**-Datei) in Intune aufgenommen wird.</span><span class="sxs-lookup"><span data-stu-id="f7852-308">This section describes how to ingest the Microsoft Edge administrative template (**msedge.admx** file) into Intune.</span></span>

> [!WARNING]
> <span data-ttu-id="f7852-309">Ändern Sie die ADMX-Datei nicht, bevor Sie sie aufnehmen.</span><span class="sxs-lookup"><span data-stu-id="f7852-309">Don't modify the ADMX file before ingesting the file.</span></span>

<span data-ttu-id="f7852-310">Führen Sie die folgenden Schritte aus, um die ADMX-Datei aufzunehmen:</span><span class="sxs-lookup"><span data-stu-id="f7852-310">To ingest the ADMX file, follow these steps:</span></span>

1. <span data-ttu-id="f7852-311">Laden Sie die Microsoft Edge-Richtlinienvorlagendatei (MicrosoftEdgePolicyTemplates.cab) von der [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise) herunter und extrahieren Sie den Inhalt.</span><span class="sxs-lookup"><span data-stu-id="f7852-311">Download the Microsoft Edge policy templates file (MicrosoftEdgePolicyTemplates.cab) from the [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise) and extract the contents.</span></span> <span data-ttu-id="f7852-312">Die Datei, die Sie aufnehmen möchten, ist **msedge.admx**.</span><span class="sxs-lookup"><span data-stu-id="f7852-312">The file that you want to ingest is **msedge.admx**.</span></span>
2. <span data-ttu-id="f7852-313">Melden Sie sich beim [Microsoft Azure-Portal](https://portal.azure.com)an.</span><span class="sxs-lookup"><span data-stu-id="f7852-313">Sign in to the [Microsoft Azure portal](https://portal.azure.com).</span></span>
3. <span data-ttu-id="f7852-314">Wählen Sie **Intune** aus _Alle Dienste_ aus, oder suchen Sie im Suchfeld des Portals nach Intune.</span><span class="sxs-lookup"><span data-stu-id="f7852-314">Select **Intune** from _All Services_, or search for Intune in the portal search box.</span></span>
4. <span data-ttu-id="f7852-315">Wählen Sie aus _Microsoft Intune – Übersicht_ **Gerätekonfiguration** | **Profile** aus.</span><span class="sxs-lookup"><span data-stu-id="f7852-315">From _Microsoft Intune - Overview_, select **Device configuration** | **Profiles**.</span></span>
5. <span data-ttu-id="f7852-316">Wählen Sie in der oberen Befehlsleiste **+ Profil erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="f7852-316">On the top command bar, select **+ Create profile**.</span></span>

   ![Erstellen eines Marketingprofils](./media/edge-cfg-with-mdm/configure-edge-mdm-intune-create-profile.png)

6. <span data-ttu-id="f7852-318">Geben Sie die folgenden Profilinformationen an:</span><span class="sxs-lookup"><span data-stu-id="f7852-318">Provide the following profile information:</span></span>

   - <span data-ttu-id="f7852-319">**Name**: Geben Sie einen aussagekräftigen Namen ein.</span><span class="sxs-lookup"><span data-stu-id="f7852-319">**Name**: Enter a descriptive name.</span></span> <span data-ttu-id="f7852-320">In diesem Beispiel „Microsoft Edge – aufgenommene ADMX-Konfiguration”.</span><span class="sxs-lookup"><span data-stu-id="f7852-320">For this example, "Microsoft Edge ADMX ingested configuration".</span></span>
   - <span data-ttu-id="f7852-321">**Beschreibung**: Geben Sie eine optionale Beschreibung für das Profil ein.</span><span class="sxs-lookup"><span data-stu-id="f7852-321">**Description**: Enter an optional description for the profile.</span></span>
   - <span data-ttu-id="f7852-322">**Plattform**: Wählen Sie „Windows 10 und höher” aus.</span><span class="sxs-lookup"><span data-stu-id="f7852-322">**Platform**: Select "Windows 10 and later"</span></span>
   - <span data-ttu-id="f7852-323">**Profiltyp**: Wählen Sie „Benutzerdefiniert” aus.</span><span class="sxs-lookup"><span data-stu-id="f7852-323">**Profile type**: Select "Custom"</span></span>

7. <span data-ttu-id="f7852-324">Klicken Sie unter **Benutzerdefinierte OMA-URI-Einstellungen** auf **Hinzufügen**, um eine ADMX-Aufnahme hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="f7852-324">On **Custom OMA-URI Settings**, click **Add** to add an ADMX ingestion.</span></span>

   ![Hinzufügen der Aufnahme für OMA-URI](./media/edge-cfg-with-mdm/configure-edge-mdm-intune-create-profile-add-omauri.png)

8. <span data-ttu-id="f7852-326">Geben Sie unter **Zeile hinzufügen** die folgenden Informationen an:</span><span class="sxs-lookup"><span data-stu-id="f7852-326">On **Add Row**, provide the following information:</span></span>

   - <span data-ttu-id="f7852-327">**Name**: Geben Sie einen aussagekräftigen Namen ein.</span><span class="sxs-lookup"><span data-stu-id="f7852-327">**Name**: Enter a descriptive name.</span></span> <span data-ttu-id="f7852-328">In diesem Beispiel verwenden Sie „Microsoft Edge – ADMX-Aufnahme”.</span><span class="sxs-lookup"><span data-stu-id="f7852-328">For this example, use "Microsoft Edge ADMX ingestion".</span></span>
   - <span data-ttu-id="f7852-329">**Beschreibung**: Geben Sie eine optionale Beschreibung für die Einstellung ein.</span><span class="sxs-lookup"><span data-stu-id="f7852-329">**Description**: Enter an optional description for the setting.</span></span>
   - <span data-ttu-id="f7852-330">**OMA-URI**: Geben Sie „*./Device/Vendor/MSFT/Policy/ConfigOperations/ADMXInstall/Edge/Policy/EdgeAdmx*” ein.</span><span class="sxs-lookup"><span data-stu-id="f7852-330">**OMA-URI**: Enter "*./Device/Vendor/MSFT/Policy/ConfigOperations/ADMXInstall/Edge/Policy/EdgeAdmx*"</span></span>
   - <span data-ttu-id="f7852-331">**Datentyp**: Wählen Sie „Zeichenfolge” aus.</span><span class="sxs-lookup"><span data-stu-id="f7852-331">**Data type**: Select "String"</span></span>
   - <span data-ttu-id="f7852-332">**Wert**: Dieser Eingabebereich wird angezeigt, nachdem Sie den **Datentyp** ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="f7852-332">**Value**: This input area appears after you select the **Data type**.</span></span> <span data-ttu-id="f7852-333">Öffnen Sie die Datei „msedge.admx” aus der Microsoft Edge-Richtlinienvorlagendatei, die Sie in Schritt 1 extrahiert haben.</span><span class="sxs-lookup"><span data-stu-id="f7852-333">Open the msedge.admx file from the Microsoft Edge policy templates file you extracted in step 1.</span></span> <span data-ttu-id="f7852-334">Kopieren Sie den **GESAMTEN Text** aus der Datei „msedge.admx”, und fügen Sie ihn in den Textbereich **Wert** ein, der im folgenden Screenshot gezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="f7852-334">Copy **ALL the text** from the msedge.admx file and paste it in the **Value** text area shown in the following screenshot.</span></span>

        ![Hinzufügen einer ADMX-Aufnahme](./media/edge-cfg-with-mdm/configure-edge-intune-mdm-omauri-addrow-ingest.png)

   - <span data-ttu-id="f7852-336">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="f7852-336">Click **OK**.</span></span>

9. <span data-ttu-id="f7852-337">Klicken Sie unter **Benutzerdefinierte OMA-URI-Einstellungen** auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="f7852-337">On **Custom OMA-URI Settings**, click **OK**.</span></span>
10. <span data-ttu-id="f7852-338">Klicken Sie unter **Profil erstellen** auf **Erstellen**.</span><span class="sxs-lookup"><span data-stu-id="f7852-338">On **Create profile**, click **Create**.</span></span> <span data-ttu-id="f7852-339">Im nächsten Screenshot werden Informationen zum neu erstellten Profil angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f7852-339">The next screenshot shows information about the newly created profile.</span></span>

    ![<span data-ttu-id="f7852-340">Neue Geräteprofilinformationen</span><span class="sxs-lookup"><span data-stu-id="f7852-340">New device profile information</span></span> ](./media/edge-cfg-with-mdm/configure-edge-mdm-intune-create-profile-done.png)

<!--
> [!NOTE]
> You can use the preceding steps to ingest the msedgeupate.admx policy template file.
-->
### <span data-ttu-id="f7852-341">Festlegen einer Richtlinie mit benutzerdefiniertem OMA-URI in Intune</span><span class="sxs-lookup"><span data-stu-id="f7852-341">Set a policy using custom OMA-URI in Intune</span></span>

> [!NOTE]
> <span data-ttu-id="f7852-342">Bevor Sie die Schritte in diesem Abschnitt ausführen, müssen Sie die unter [Aufnehmen der Microsoft Edge ADMX-Datei in Intune](#ingest-the-microsoft-edge-admx-file-into-intune) beschriebenen Schritte ausführen.</span><span class="sxs-lookup"><span data-stu-id="f7852-342">Before using the steps in this section you must complete the steps described in [Ingest the Microsoft Edge ADMX file into Intune](#ingest-the-microsoft-edge-admx-file-into-intune).</span></span>

1. <span data-ttu-id="f7852-343">Melden Sie sich beim [Microsoft Azure-Portal](https://portal.azure.com)an.</span><span class="sxs-lookup"><span data-stu-id="f7852-343">Sign in to the [Microsoft Azure portal](https://portal.azure.com).</span></span>
2. <span data-ttu-id="f7852-344">Wählen Sie **Intune** aus _Alle Dienste_ aus, oder suchen Sie im Suchfeld des Portals nach Intune.</span><span class="sxs-lookup"><span data-stu-id="f7852-344">Select **Intune** from _All Services_, or search for Intune in the portal search box.</span></span>
3. <span data-ttu-id="f7852-345">Wechseln Sie zu **Intune**>**Gerätekonfiguration**>**Profile**.</span><span class="sxs-lookup"><span data-stu-id="f7852-345">Go to **Intune**>**Device configuration**>**Profiles**.</span></span>
4. <span data-ttu-id="f7852-346">Wählen sie das Profil „Microsoft Edge – aufgenommene ADMX-Konfiguration” oder den Namen aus, den Sie für das Profil verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="f7852-346">Select the "Microsoft Edge ADMX ingested configuration" profile or the name you used for the profile.</span></span>
5. <span data-ttu-id="f7852-347">Um Microsoft Edge-Richtlinieneinstellungen hinzuzufügen, müssen Sie **Benutzerdefinierte OMA-URI-Einstellungen** öffnen.</span><span class="sxs-lookup"><span data-stu-id="f7852-347">To add Microsoft Edge policy settings, you have to open **Custom OMA-URI Settings**.</span></span> <span data-ttu-id="f7852-348">Klicken Sie unter **Verwalten** auf **Eigenschaften** und anschließend auf **Einstellungen**.</span><span class="sxs-lookup"><span data-stu-id="f7852-348">Under **Manage**, click **Properties**, and then click **Settings**.</span></span>

    ![Konfigurieren von Profileinstellungen](./media/edge-cfg-with-mdm/configure-edge-mdm-intune-add-policy-settings.png)

6. <span data-ttu-id="f7852-350">Klicken Sie unter **OMA-URI-Einstellungen** auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="f7852-350">On **Custom OMA-URI Settings**, click **Add**.</span></span>

    ![Hinzufügen von Zeilen zu den OMA-URI-Einstellungen](./media/edge-cfg-with-mdm/configure-edge-mdm-intune-add-policy-settings-add-row.png)

7. <span data-ttu-id="f7852-352">Geben Sie unter **Zeile hinzufügen** die folgenden Informationen an:</span><span class="sxs-lookup"><span data-stu-id="f7852-352">On **Add Row**, provide the following information:</span></span>

   - <span data-ttu-id="f7852-353">**Name**: Geben Sie einen aussagekräftigen Namen ein.</span><span class="sxs-lookup"><span data-stu-id="f7852-353">**Name**: Enter a descriptive name.</span></span> <span data-ttu-id="f7852-354">Es wird empfohlen, den zu konfigurierenden Richtliniennamen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="f7852-354">We suggest using the policy name you want to configure.</span></span> <span data-ttu-id="f7852-355">In diesem Beispiel verwenden Sie „ShowHomeButton“.</span><span class="sxs-lookup"><span data-stu-id="f7852-355">For this example, use "ShowHomeButton".</span></span>
   - <span data-ttu-id="f7852-356">**Beschreibung** (optional): Geben Sie eine Beschreibung für die Einstellung ein.</span><span class="sxs-lookup"><span data-stu-id="f7852-356">**Description** (Optional): Enter a description for the setting.</span></span>
   - <span data-ttu-id="f7852-357">**OMA-URI**: Geben Sie den OMA-URI für die Richtlinie ein.</span><span class="sxs-lookup"><span data-stu-id="f7852-357">**OMA-URI**: Enter the OMA-URI for the policy.</span></span> <span data-ttu-id="f7852-358">Verwenden Sie für die „ShowHomeButton”-Richtlinie als Beispiel diese Zeichenfolge: „*./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Startup/ShowHomeButton*”</span><span class="sxs-lookup"><span data-stu-id="f7852-358">Using the for "ShowHomeButton" policy as an example, use this string: "*./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Startup/ShowHomeButton*"</span></span>
   - <span data-ttu-id="f7852-359">**Datentyp**: Wählen Sie den Datentyp „Richtlinieneinstellungen” aus.</span><span class="sxs-lookup"><span data-stu-id="f7852-359">**Data type**: Select the policy settings data type.</span></span> <span data-ttu-id="f7852-360">Verwenden Sie für die „ShowHomeButton”-Richtlinie „Zeichenfolge”.</span><span class="sxs-lookup"><span data-stu-id="f7852-360">For the "ShowHomeButton" policy, use "String"</span></span>
   - <span data-ttu-id="f7852-361">**Wert**: Geben Sie die Einstellung ein, die Sie für die Richtlinie konfigurieren möchten.</span><span class="sxs-lookup"><span data-stu-id="f7852-361">**Value**: Enter the setting that you want to configure for the policy.</span></span> <span data-ttu-id="f7852-362">Geben Sie für das Beispiel „ShowHomeButton” „\<enabled/>” ein.</span><span class="sxs-lookup"><span data-stu-id="f7852-362">For "ShowHomeButton" example, enter "\<enabled/>".</span></span> <span data-ttu-id="f7852-363">Der folgende Screenshot zeigt die Einstellungen zum Konfigurieren einer Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="f7852-363">The following screenshot shows the settings for configuring a policy.</span></span>

        ![Hinzufügen von Zeilen, Benutzerdefinierte OMA-URI-Einstellungen](./media/edge-cfg-with-mdm/configure-edge-mdm-custom-omauri-setting.png)

   - <span data-ttu-id="f7852-365">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="f7852-365">Click **OK**.</span></span>

8. <span data-ttu-id="f7852-366">Klicken Sie unter **Benutzerdefinierte OMA-URI-Einstellungen** auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="f7852-366">On **Custom OMA-URI Settings**, click **OK**.</span></span>
9. <span data-ttu-id="f7852-367">Klicken Sie im Profil „**Microsoft Edge – aufgenommene ADMX-Konfiguration – Eigenschaften**” (oder dem Namen, den Sie verwendet haben) auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="f7852-367">On the "**Microsoft Edge ADMX ingested configuration - Properties**" profile (or the name you used), click **Save**.</span></span>

<span data-ttu-id="f7852-368">Nachdem das Profil erstellt und die Eigenschaften festgelegt wurden, müssen Sie [das Profil in Microsoft Intune zuweisen](https://docs.microsoft.com/intune/configuration/device-profile-assign).</span><span class="sxs-lookup"><span data-stu-id="f7852-368">After the profile is created and the properties set, you have to [assign the profile in Microsoft Intune](https://docs.microsoft.com/intune/configuration/device-profile-assign).</span></span>

#### <span data-ttu-id="f7852-369">Bestätigen der Festlegung der Richtlinie</span><span class="sxs-lookup"><span data-stu-id="f7852-369">Confirm that the policy was set</span></span>

<span data-ttu-id="f7852-370">Gehen Sie wie folgt vor, um zu bestätigen, dass die Microsoft Edge-Richtlinie das von Ihnen erstellte Profil verwendet.</span><span class="sxs-lookup"><span data-stu-id="f7852-370">Use the following steps to confirm that the Microsoft Edge policy is using the profile you created.</span></span> <span data-ttu-id="f7852-371">(Geben Sie Microsoft Intune Zeit, die Richtlinie an ein Gerät weiterzugeben, das Sie im Profilbeispiel „Microsoft Edge – aufgenommene ADMX-Konfiguration” zugewiesen haben.)</span><span class="sxs-lookup"><span data-stu-id="f7852-371">(Give Microsoft Intune time to propagate the policy to a device you assigned in the "Microsoft Edge ADMX ingested configuration" profile example.)</span></span>

1. <span data-ttu-id="f7852-372">Öffnen Sie Microsoft Edge und wechseln Sie zu *edge://policy*.</span><span class="sxs-lookup"><span data-stu-id="f7852-372">Open Microsoft Edge and go to *edge://policy*.</span></span>
2. <span data-ttu-id="f7852-373">Überprüfen Sie auf der Seite **Richtlinien**, ob die im Profil festgelegte Richtlinie aufgelistet ist.</span><span class="sxs-lookup"><span data-stu-id="f7852-373">On the **Policies** page, see if the policy you set in the profile is listed.</span></span>
3. <span data-ttu-id="f7852-374">Wenn Ihre Richtlinie nicht angezeigt wird, finden Sie unter [Diagnostizieren von MDM-Fehlern in Windows 10](https://docs.microsoft.com/windows/client-management/mdm/diagnose-mdm-failures-in-windows-10) oder [Problembehandlung bei einer Richtlinieneinstellung](#troubleshoot-a-policy-setting) weitere Informationen.</span><span class="sxs-lookup"><span data-stu-id="f7852-374">If your policy isn't shown, see [Diagnose MDM failures in Windows 10](https://docs.microsoft.com/windows/client-management/mdm/diagnose-mdm-failures-in-windows-10) or [Troubleshoot a policy setting](#troubleshoot-a-policy-setting).</span></span>

#### <span data-ttu-id="f7852-375">Problembehandlung bei einer Richtlinieneinstellung</span><span class="sxs-lookup"><span data-stu-id="f7852-375">Troubleshoot a policy setting</span></span>

<span data-ttu-id="f7852-376">Wenn eine Microsoft Edge-Richtlinie nicht wirksam wird, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="f7852-376">If a Microsoft Edge policy isn’t taking effect, try the following steps:</span></span>

<span data-ttu-id="f7852-377">Öffnen Sie die Seite *edge://policy* auf dem Zielgerät (ein Gerät, dem Sie in Microsoft Intune das Profil zugewiesen haben), und suchen Sie nach der Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="f7852-377">Open the *edge://policy* page on the target device (a device you assigned the profile to in Microsoft Intune) and search for the policy.</span></span> <span data-ttu-id="f7852-378">Wenn die Richtlinie nicht auf der Seite *edge://policy* angezeigt wird, versuchen Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="f7852-378">If the policy isn’t on the *edge://policy* page, try the following:</span></span>

- <span data-ttu-id="f7852-379">Überprüfen Sie, ob sich die Richtlinie in der Registrierung befindet und korrekt ist.</span><span class="sxs-lookup"><span data-stu-id="f7852-379">Check that the policy is in the registry and is correct.</span></span> <span data-ttu-id="f7852-380">Öffnen Sie auf dem Zielgerät den Windows 10-Registrierungs-Editor (**Windows-Taste + r**, geben Sie „*regedit*” ein und drücken Sie dann die **Eingabetaste**). Überprüfen Sie, ob die Richtlinie im Pfad *\Software\Policies\Microsoft \Edge* korrekt definiert ist.</span><span class="sxs-lookup"><span data-stu-id="f7852-380">On the target device open the Windows 10 Registry Editor (**Windows key + r**, enter “*regedit*” and then press **Enter**.) Check that the policy is correctly defined in the *\Software\Policies\ Microsoft\Edge* path.</span></span> <span data-ttu-id="f7852-381">Wenn Sie die Richtlinie nicht im erwarteten Pfad finden, wurde die Richtlinie nicht ordnungsgemäß auf das Gerät übertragen.</span><span class="sxs-lookup"><span data-stu-id="f7852-381">If you don’t find the policy in the expected path, then the policy wasn’t pushed to the device correctly.</span></span>
- <span data-ttu-id="f7852-382">Überprüfen Sie, ob der OMA-URI-Pfad korrekt und der Wert eine gültige XML-Zeichenfolge ist.</span><span class="sxs-lookup"><span data-stu-id="f7852-382">Check that the OMA-URI path is correct, and the value is a valid XML string.</span></span> <span data-ttu-id="f7852-383">Wenn eines davon fehlerhaft ist, wird die Richtlinie nicht auf das Zielgerät übertragen.</span><span class="sxs-lookup"><span data-stu-id="f7852-383">If either of these are incorrect the policy won’t be pushed to the target device.</span></span>

<span data-ttu-id="f7852-384">Weitere Tipps zur Problembehebung finden Sie unter [Microsoft Intune einrichten](https://docs.microsoft.com/intune/fundamentals/setup-steps) und [Geräte synchronisieren](https://docs.microsoft.com/intune/remote-actions/device-sync).</span><span class="sxs-lookup"><span data-stu-id="f7852-384">For more trouble shooting tips, see [Set up Microsoft Intune](https://docs.microsoft.com/intune/fundamentals/setup-steps) and [Sync devices](https://docs.microsoft.com/intune/remote-actions/device-sync).</span></span>

## <span data-ttu-id="f7852-385">Weitere Informationen:</span><span class="sxs-lookup"><span data-stu-id="f7852-385">See also</span></span>

- [<span data-ttu-id="f7852-386">Microsoft Edge Enterprise-Angebotsseite</span><span class="sxs-lookup"><span data-stu-id="f7852-386">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="f7852-387">Konfigurieren der Microsoft Edge-Richtlinieneinstellungen mit Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="f7852-387">Configure Microsoft Edge policy settings with Microsoft Intune</span></span>](configure-edge-with-intune.md)
- [<span data-ttu-id="f7852-388">Mobile Geräteverwaltung</span><span class="sxs-lookup"><span data-stu-id="f7852-388">Mobile device management</span></span>](https://docs.microsoft.com/windows/client-management/mdm/)
- [<span data-ttu-id="f7852-389">Verwenden von benutzerdefinierten Einstellungen für Windows 10-Geräte in Intune</span><span class="sxs-lookup"><span data-stu-id="f7852-389">Use custom settings for Windows 10 devices in Intune</span></span>](https://docs.microsoft.com/intune/configuration/custom-settings-windows-10)
- [<span data-ttu-id="f7852-390">Richtlinienkonfiguration für Win32- und Desktop-Brücke-Apps</span><span class="sxs-lookup"><span data-stu-id="f7852-390">Win32 and Desktop Bridge app policy configuration</span></span>](https://docs.microsoft.com/windows/client-management/mdm/win32-and-centennial-app-policy-configuration)
- [<span data-ttu-id="f7852-391">Grundlegende Informationen zu ADMX-gesicherten Richtlinien</span><span class="sxs-lookup"><span data-stu-id="f7852-391">Understanding ADMX-backed policies</span></span>](https://docs.microsoft.com/windows/client-management/mdm/understanding-admx-backed-policies)
