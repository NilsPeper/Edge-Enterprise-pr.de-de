---
title: Microsoft Edge-Erweiterungen zum Selbsthosten
ms.author: aspoddar
author: AndreaLBarr
manager: balajek
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Erfahren Sie, wie Sie Microsoft Edge-Erweiterungen im Unternehmen verpacken und selbst hosten.
ms.openlocfilehash: aef4438212829006e39572fa938462f13721c580
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "11642871"
---
# <a name="self-host-microsoft-edge-extensions"></a><span data-ttu-id="ef483-103">Microsoft Edge-Erweiterungen zum Selbsthosten</span><span class="sxs-lookup"><span data-stu-id="ef483-103">Self-host Microsoft Edge extensions</span></span>

<span data-ttu-id="ef483-104">Dieser Artikel enthält grundlegende Anleitungen zum Verpacken einer Erweiterung, die in Ihrem eigenen Webstore gehostet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ef483-104">This article provides basic guidance for packaging an extension to host on your own webstore.</span></span> <span data-ttu-id="ef483-105">Ebenso enthält er Anweisungen zum Bereitstellen von Erweiterungen für Geräte und Benutzer in Ihrer Organisation.</span><span class="sxs-lookup"><span data-stu-id="ef483-105">It also includes instructions on how to deploy extensions to devices and users in your organization.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ef483-106">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="ef483-106">Prerequisites</span></span>

<span data-ttu-id="ef483-107">Um Ihre eigenen Erweiterungen selbst zu hosten, müssen Sie Ihre eigenen Webhosting-Dienste für die Erweiterungen und deren Anwendungsmanifestdateien bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="ef483-107">To self-host your own extensions, you will need to provide your own web hosting services for the extensions and their manifest files.</span></span>

 <span data-ttu-id="ef483-108">Bei den folgenden Schritten wird davon ausgegangen, dass Sie Ihre Erweiterung bereits erstellt haben, Erfahrung mit XML-Dateien haben, über praktische Kenntnisse in der Konfiguration von Gruppenrichtlinien verfügen und wissen, wie Sie die Windows-Registrierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="ef483-108">The following steps assume that you’ve already created your extension, have some experience with XML files, have a working knowledge of configuring group policy, and know how to use the Windows registry.</span></span>

## <a name="publish-an-extension"></a><span data-ttu-id="ef483-109">Veröffentlichen einer Erweiterung</span><span class="sxs-lookup"><span data-stu-id="ef483-109">Publish an extension</span></span>

<span data-ttu-id="ef483-110">Bevor Sie eine Erweiterung veröffentlichen, muss sie in eine CRX-Datei (Chrome-Erweiterungsdatei) verpackt werden.</span><span class="sxs-lookup"><span data-stu-id="ef483-110">Before you publish an extension it needs to be packed into a CRX (Chrome extension) file.</span></span> <span data-ttu-id="ef483-111">Führen Sie die folgenden anleitenden Schritte zum Verpacken einer Erweiterung als CRX-Datei aus.</span><span class="sxs-lookup"><span data-stu-id="ef483-111">Use the following steps as a guide to packing an extension as a CRX file.</span></span>

1. <span data-ttu-id="ef483-112">Wechseln Sie in der Microsoft Edge-Adressleiste zu *edge://extensions* und aktivieren Sie den **Entwicklermodus**, falls er noch nicht aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="ef483-112">In the Microsoft Edge address bar, go to *edge://extensions* and turn on **Developer mode** if it’s not already enabled.</span></span>
2. <span data-ttu-id="ef483-113">Klicken Sie unter **Installierte Erweiterungen** auf **Erweiterung verpacken**, um die CRX-Datei zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ef483-113">Under **Installed extensions**, click **Pack Extension** to create the CRX file.</span></span>
3. <span data-ttu-id="ef483-114">Verwenden Sie das Dialogfeld **Erweiterung verpacken**, um das Verzeichnis zu finden, das die Quelle für die Erweiterung enthält.</span><span class="sxs-lookup"><span data-stu-id="ef483-114">Use the **Pack extension** dialog to find the directory that has the source for the extension.</span></span> <span data-ttu-id="ef483-115">Wählen Sie das Verzeichnis aus und klicken Sie dann auf **Erweiterung verpacken**.</span><span class="sxs-lookup"><span data-stu-id="ef483-115">Select the directory and then click **Pack extension**.</span></span>  <span data-ttu-id="ef483-116">Dadurch wird Ihre CRX-Datei zusammen mit einer PEM-Datei erstellt.</span><span class="sxs-lookup"><span data-stu-id="ef483-116">This will create your CRX file, along with a PEM file.</span></span> <span data-ttu-id="ef483-117">Speichern Sie die PEM-Datei, denn sie wird für Versionsupdates der Erweiterung benötigt.</span><span class="sxs-lookup"><span data-stu-id="ef483-117">Save the PEM file because it’s needed for making version updates to the extension.</span></span> <span data-ttu-id="ef483-118">Der nächste Screenshot zeigt das Dialogfeld **Erweiterung verpacken** zum Auffinden des Stammverzeichnisses der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="ef483-118">The next screenshot shows the **Pack extension** dialog for locating the root directory of the extension.</span></span>

   :::image type="content" source="media/microsoft-edge-manage-extensions-webstore/manage-extensions-pack-dialog.png" alt-text="Dialogfeld Erweiterung verpacken, zum Auffinden des Quellcodes einer Erweiterung.":::

   > [!IMPORTANT]
   > <span data-ttu-id="ef483-120">Speichern Sie die PEM-Datei an einem sicheren Ort, da sie der Schlüssel für die Erweiterung ist und für zukünftige Updates benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="ef483-120">Store the PEM file in a safe location because it’s the key for the extension and it’s needed for future updates.</span></span>

4. <span data-ttu-id="ef483-121">Bewegen Sie die CRX-Datei in Ihr Erweiterungsfenster und stellen Sie sicher, dass sie geladen wird.</span><span class="sxs-lookup"><span data-stu-id="ef483-121">Drag the CRX file into your extensions window and make sure that it loads.</span></span>
5. <span data-ttu-id="ef483-122">Testen Sie die Erweiterung und notieren Sie sich das ID-Feld (das ist die CRX-ID) und die Versionsnummer.</span><span class="sxs-lookup"><span data-stu-id="ef483-122">Test the extension and take note of the ID field (this is the CRX ID) and version number.</span></span> <span data-ttu-id="ef483-123">Sie benötigen diese Informationen später.</span><span class="sxs-lookup"><span data-stu-id="ef483-123">You’ll need this information later.</span></span> <span data-ttu-id="ef483-124">Der nächste Screenshot zeigt eine Testerweiterung mit ihrer CRX-ID.</span><span class="sxs-lookup"><span data-stu-id="ef483-124">The next screenshot shows a test extension with its CRX ID.</span></span>

   :::image type="content" source="media/microsoft-edge-manage-extensions-webstore/manage-extensions-test-extension.png" alt-text="Erweiterungsbeispiel mit CRX-ID":::

6. <span data-ttu-id="ef483-126">Laden Sie die CRX-Datei auf den Host hoch und notieren Sie sich die URL des Speicherorts, von dem sie heruntergeladen wird.</span><span class="sxs-lookup"><span data-stu-id="ef483-126">Upload the the CRX file to the host and note the URL of the location it will be downloaded from.</span></span> <span data-ttu-id="ef483-127">Diese Informationen werden für die XML-Anwendungsmanifestdatei benötigt.</span><span class="sxs-lookup"><span data-stu-id="ef483-127">This information is needed for the XML manifest file.</span></span>
7. <span data-ttu-id="ef483-128">Um eine Anwendungsmanifest-XML-Datei mit der App-/Erweiterungs-ID, der Download-URL und der Version zu erstellen, definieren Sie die folgenden Felder:</span><span class="sxs-lookup"><span data-stu-id="ef483-128">To create a manifest XML file with the app/extension ID, download URL, and version, define the following fields:</span></span>  

   - <span data-ttu-id="ef483-129">**appid** – Die Erweiterungs-ID aus Schritt 5</span><span class="sxs-lookup"><span data-stu-id="ef483-129">**appid** - The extension ID from step 5</span></span>
   - <span data-ttu-id="ef483-130">**codebase** – Der Downloadspeicherort für die CRX-Datei aus Schritt 6</span><span class="sxs-lookup"><span data-stu-id="ef483-130">**codebase** - The download location for the CRX file from step 6</span></span>
   - <span data-ttu-id="ef483-131">**version** – Die Version der App/Erweiterung, die mit der im Anwendungsmanifest der Erweiterung angegebenen Version übereinstimmen sollte.</span><span class="sxs-lookup"><span data-stu-id="ef483-131">**version** - The version of the app/extension, which should match the version specified in the manifest of the extension.</span></span>

   <span data-ttu-id="ef483-132">Der nächste Codeausschnitt zeigt ein Beispiel für eine XML-Anwendungsmanifestdatei.</span><span class="sxs-lookup"><span data-stu-id="ef483-132">The next code snippet shows an example of an XML manifest file.</span></span>

   ```xml
   <?xml version='1.0' encoding='UTF-8'?> 
   <gupdate xmlns='http://www.google.com/update2/response' protocol='2.0'> 
     <app appid='ekilpdeokbpjmminmhfcgkncmmohmfeb'> 
     <updatecheck codebase='https://app.somecompany.com/extensionfolder/helloworld.crx' version='1.0' /> 
     </app> 
   </gupdate> 
   ```

   <span data-ttu-id="ef483-133">Weitere Informationen finden Sie unter [AutoUpdate-Erweiterungen in Microsoft Edge – Microsoft Edge Development](/microsoft-edge/extensions-chromium/enterprise/auto-update).</span><span class="sxs-lookup"><span data-stu-id="ef483-133">For more information, see [Auto-update extensions in Microsoft Edge - Microsoft Edge Development](/microsoft-edge/extensions-chromium/enterprise/auto-update).</span></span>

8. <span data-ttu-id="ef483-134">Laden Sie die fertige XML-Datei an einen Speicherort hoch, von dem sie heruntergeladen werden kann, und notieren Sie sich die URL.</span><span class="sxs-lookup"><span data-stu-id="ef483-134">Upload the completed XML file to a location where it can be downloaded from, noting the URL.</span></span> <span data-ttu-id="ef483-135">Diese URL wird benötigt, wenn Sie die Erweiterung mithilfe einer Gruppenrichtlinie installieren.</span><span class="sxs-lookup"><span data-stu-id="ef483-135">This URL will be needed when you install the extension using a group policy.</span></span> <span data-ttu-id="ef483-136">Informationen unter [Verteilen einer privat gehosteten Erweiterung](#distribute-a-privately-hosted-extension).</span><span class="sxs-lookup"><span data-stu-id="ef483-136">See [Distribute a privately hosted extension](#distribute-a-privately-hosted-extension).</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="ef483-137">Der Hosting-Standort für die Erweiterung erfordert keine Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="ef483-137">The hosting location for the extension doesn’t need authentication.</span></span> <span data-ttu-id="ef483-138">Er muss für Benutzergeräte zugänglich sein, wo immer diese verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ef483-138">It needs to be accessible by user devices wherever they might be used.</span></span>

## <a name="publish-updates-to-an-extension"></a><span data-ttu-id="ef483-139">Veröffentlichen von Updates für eine Erweiterung</span><span class="sxs-lookup"><span data-stu-id="ef483-139">Publish updates to an extension</span></span>

<span data-ttu-id="ef483-140">Nachdem Sie die aktualisierte Erweiterung geändert und getestet haben, können Sie diese veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="ef483-140">After you change and test the updated extension you can publish it.</span></span> <span data-ttu-id="ef483-141">Führen Sie die folgenden anleitenden Schritte für die Veröffentlichung eines Updates aus.</span><span class="sxs-lookup"><span data-stu-id="ef483-141">Use the following steps as a guide for publishing an update.</span></span>

1. <span data-ttu-id="ef483-142">Ändern Sie die Versionsnummer in Ihrer Erweiterungsdatei manifest.JSON mit der folgenden Syntax in eine höhere Nummer: `"version":"versionString"`.</span><span class="sxs-lookup"><span data-stu-id="ef483-142">Change the version number in your extension's manifest.JSON file to a higher number using the following syntax: `"version":"versionString"`.</span></span> <span data-ttu-id="ef483-143">Wenn es sich um "version":"1.0" handelt, können Sie auf "version":"1.1" oder eine beliebige Zahl höher als "1.0" aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="ef483-143">If the "version":"1.0", then you can update to "version":"1.1" or any number higher than "1.0".</span></span>
2. <span data-ttu-id="ef483-144">Aktualisieren Sie die "Version" von `<updatecheck>` in der XML-Datei, damit sie mit der Nummer übereinstimmt, die Sie im vorherigen Schritt in die Anwendungsmanifestdatei eingegeben haben.</span><span class="sxs-lookup"><span data-stu-id="ef483-144">Update the "version" of `<updatecheck>` in the XML file to match the number that you put in the manifest file in the previous step.</span></span> <span data-ttu-id="ef483-145">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="ef483-145">For example:</span></span><br>`<updatecheck codebase='https://app.somecompany.com/extensionfolder/helloworld.crx' version='1.1' />`
3. <span data-ttu-id="ef483-146">Erstellen Sie eine CRX-Datei, welche die neuen Änderungen enthält.</span><span class="sxs-lookup"><span data-stu-id="ef483-146">Create a CRX file that includes the new changes.</span></span> <span data-ttu-id="ef483-147">Wechseln Sie zu *edge://extensions,* und aktivieren Sie **den Entwicklermodus**.</span><span class="sxs-lookup"><span data-stu-id="ef483-147">Go to *edge://extensions* and enable **Developer mode**.</span></span>
4. <span data-ttu-id="ef483-148">Klicken Sie auf **Erweiterung verpacken** und wechseln Sie für die Erweiterungsquelle zum Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="ef483-148">Click **Pack extension** and go to the directory for the extension source.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="ef483-149">Verwenden Sie dieselbe PEM-Datei, die beim ersten Erstellen der CRX-Datei generiert und gespeichert wurde.</span><span class="sxs-lookup"><span data-stu-id="ef483-149">Use the same PEM file that was generated and saved the first time the CRX file was created.</span></span> <span data-ttu-id="ef483-150">Wenn Sie nicht dieselbe PEM-Datei verwenden, ändert sich die App-ID der Erweiterung und das Update wird als neue Erweiterung behandelt.</span><span class="sxs-lookup"><span data-stu-id="ef483-150">If you don't use the same PEM file the app ID of the extension will change and the update will be treated as a new extension.</span></span>

5. <span data-ttu-id="ef483-151">Bewegen Sie die CRX-Datei in das Erweiterungsfenster und legen Sie diese dort ab, und stellen Sie sicher, dass sie geladen wird.</span><span class="sxs-lookup"><span data-stu-id="ef483-151">Drag and drop the CRX file into the extensions window and verify that it loads.</span></span>
6. <span data-ttu-id="ef483-152">Testen Sie die aktualisierte Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="ef483-152">Test the updated extension.</span></span>
7. <span data-ttu-id="ef483-153">Ersetzen Sie für die aktualisierte Erweiterung die alten CRX-und XML-Dateien durch die neuen Dateien.</span><span class="sxs-lookup"><span data-stu-id="ef483-153">Replace the old CRX file and XML file with the new files for the updated extension.</span></span>

<span data-ttu-id="ef483-154">Die Änderungen der Erweiterung werden während des nächsten Richtliniensynchronisierungszyklus übernommen.</span><span class="sxs-lookup"><span data-stu-id="ef483-154">The extension's changes will be picked up during the next policy sync cycle.</span></span> <span data-ttu-id="ef483-155">Weitere Informationen zum Aktualisieren von Erweiterungen finden Sie unter: [URL aktualisieren](/microsoft-edge/extensions-chromium/enterprise/auto-update#update-url) und [Anwendungsmanifest aktualisieren](/microsoft-edge/extensions-chromium/enterprise/auto-update#updated-manifest).</span><span class="sxs-lookup"><span data-stu-id="ef483-155">For more information about updating extensions, see: [Update URL](/microsoft-edge/extensions-chromium/enterprise/auto-update#update-url) and [Update manifest](/microsoft-edge/extensions-chromium/enterprise/auto-update#updated-manifest).</span></span>

## <a name="distribute-a-privately-hosted-extension"></a><span data-ttu-id="ef483-156">Verteilen einer privat gehosteten Erweiterung</span><span class="sxs-lookup"><span data-stu-id="ef483-156">Distribute a privately hosted extension</span></span>

<span data-ttu-id="ef483-157">Sie können den Link des Speicherortes teilen, an dem die CRX-Datei gehostet wird, und sobald Benutzer die URL in ihren Browser eingeben, wird die Erweiterung heruntergeladen und installiert.</span><span class="sxs-lookup"><span data-stu-id="ef483-157">You can share the link of the location where the CRX file is hosted, and as soon as users enter the URL in their browser the extension will be downloaded and installed.</span></span> <span data-ttu-id="ef483-158">Benutzer können die Erweiterung über die Seite edge://extensions aktivieren.</span><span class="sxs-lookup"><span data-stu-id="ef483-158">Users can enable the extension from the edge://extensions page.</span></span> <span data-ttu-id="ef483-159">Damit Benutzer selbst gehostete Erweiterungen installieren können, müssen Sie die CRX-IDs der Erweiterungen zur [ExtensionInstallAllowList](/deployedge/microsoft-edge-policies#extensioninstallallowlist)-Richtlinie hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="ef483-159">To allow users to install self-hosted extensions, you need to add the extension CRX IDs to the [ExtensionInstallAllowList](/deployedge/microsoft-edge-policies#extensioninstallallowlist) policy.</span></span>

<span data-ttu-id="ef483-160">Alternativ können Sie die Gruppenrichtlinie [ExtensionInstallForceList](/deployedge/microsoft-edge-manage-extensions-policies#force-install-an-extension) verwenden, um die Installation einer Erweiterung auf den Geräten Ihrer Benutzer zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="ef483-160">Alternatively, you can use group policy [ExtensionInstallForceList](/deployedge/microsoft-edge-manage-extensions-policies#force-install-an-extension) to Force-install an extension on your users’ devices.</span></span>

<span data-ttu-id="ef483-161">Sie können diese Richtlinien auf Ihre ausgewählten Benutzer, Geräte oder auf beides anwenden.</span><span class="sxs-lookup"><span data-stu-id="ef483-161">You can apply these policies to your selected users, devices, or both.</span></span> <span data-ttu-id="ef483-162">Beachten Sie jedoch, dass Richtlinienaktualisierungen nicht sofort erfolgen und es einige Zeit dauern kann, bis die Richtlinieneinstellungen wirksam werden.</span><span class="sxs-lookup"><span data-stu-id="ef483-162">Remember though that policy updates are not instantaneous, and it will take time for the policy settings to take effect.</span></span>

## <a name="see-also"></a><span data-ttu-id="ef483-163">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ef483-163">See also</span></span>

- [<span data-ttu-id="ef483-164">Verwalten von Microsoft Edge-Erweiterungen im Unternehmen</span><span class="sxs-lookup"><span data-stu-id="ef483-164">Manage Microsoft Edge extensions in the enterprise</span></span>](microsoft-edge-manage-extensions.md)
- [<span data-ttu-id="ef483-165">Verwenden von Gruppenrichtlinien zum Verwalten von Microsoft Edge-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="ef483-165">Use group policies to manage Microsoft Edge extensions</span></span>](microsoft-edge-manage-extensions-policies.md)
- [<span data-ttu-id="ef483-166">Detaillierter Leitfaden zur ExtensionSettings-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="ef483-166">Detailed guide to the ExtensionSettings policy</span></span>](microsoft-edge-manage-extensions-ref-guide.md)
- [<span data-ttu-id="ef483-167">Häufig gestellte Fragen (FAQ) zu Microsoft Edge-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="ef483-167">FAQ for Microsoft Edge Extensions</span></span>](microsoft-edge-manage-extensions-faq.md)
- [<span data-ttu-id="ef483-168">Microsoft Edge Enterprise-Angebotsseite</span><span class="sxs-lookup"><span data-stu-id="ef483-168">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
