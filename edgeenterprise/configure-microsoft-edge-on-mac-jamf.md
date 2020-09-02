---
title: Konfigurieren von Microsoft Edge unter macOS mit Jamf
ms.author: brianalt
author: dan-wesley
manager: laurawi
ms.date: 02/20/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Konfigurieren der Microsoft Edge-Richtlinieneinstellungen auf Mac-Geräten mit Jamf
ms.openlocfilehash: 336bdfed2c53811615b0183dc5ca7db916cd7428
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979898"
---
# <span data-ttu-id="ef25e-103">Konfigurieren der Microsoft Edge-Richtlinieneinstellungen unter macOS mit Jamf</span><span class="sxs-lookup"><span data-stu-id="ef25e-103">Configure Microsoft Edge policy settings on macOS with Jamf</span></span>

<span data-ttu-id="ef25e-104">In diesem Artikel wird beschrieben, wie Sie Richtlinieneinstellungen unter macOS mithilfe einer Microsoft Edge-Richtlinienmanifestdatei unter Jamf Pro 10.19 konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="ef25e-104">This article describes how to configure policy settings on macOS using a Microsoft Edge policy manifest file on Jamf Pro 10.19.</span></span>

<span data-ttu-id="ef25e-105">Sie können Microsoft Edge-Richtlinieneinstellungen auf macOS auch mithilfe einer Eigenschaftslistendatei (.plist) konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="ef25e-105">You can also configure Microsoft Edge policy settings on macOS by using a property list (.plist) file.</span></span> <span data-ttu-id="ef25e-106">Weitere Informationen finden Sie unter [Konfigurieren für macOS mithilfe einer Eigenschaftsliste (.plist)](configure-microsoft-edge-on-mac.md)</span><span class="sxs-lookup"><span data-stu-id="ef25e-106">For more information, see [Configure for macOS using a .plist](configure-microsoft-edge-on-mac.md)</span></span>


## <span data-ttu-id="ef25e-107">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="ef25e-107">Prerequisites</span></span>

<span data-ttu-id="ef25e-108">Die folgende Software ist erforderlich:</span><span class="sxs-lookup"><span data-stu-id="ef25e-108">The following software is required:</span></span>

- <span data-ttu-id="ef25e-109">Microsoft Edge Stable Kanal 81</span><span class="sxs-lookup"><span data-stu-id="ef25e-109">Microsoft Edge Stable channel 81</span></span>
- <span data-ttu-id="ef25e-110">Richtlinienvorlagendatei, Version 81.0.416.3</span><span class="sxs-lookup"><span data-stu-id="ef25e-110">Policy Templates file, version 81.0.416.3</span></span>
- <span data-ttu-id="ef25e-111">Jamf Pro, Version 10.19</span><span class="sxs-lookup"><span data-stu-id="ef25e-111">Jamf Pro, Version 10.19</span></span>

## <span data-ttu-id="ef25e-112">Informationen zum Jamf Pro-Menü der Anwendungseinstellungen und benutzerdefinierten Einstellungen</span><span class="sxs-lookup"><span data-stu-id="ef25e-112">About the Jamf Pro Application & Custom Settings menu</span></span>

<span data-ttu-id="ef25e-113">Vor Jamf Pro 10.18 musste zur Verwaltung von Office 365 manuell eine Eigenschaftslistendatei (.plist) erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="ef25e-113">Before Jamf Pro 10.18, managing Office 365 involved manually building a .plist file.</span></span> <span data-ttu-id="ef25e-114">Dieser Workflow war zeitaufwändig und erforderte einen starken technischen Hintergrund.</span><span class="sxs-lookup"><span data-stu-id="ef25e-114">This was a time-consuming workflow that required a strong technical background.</span></span> <span data-ttu-id="ef25e-115">Mit Jamf Pro 10.18 wurden diese Barrieren durch Optimierung des Konfigurationsprozesses eliminiert.</span><span class="sxs-lookup"><span data-stu-id="ef25e-115">Jamf Pro 10.18 eliminated those barriers by streamlining the configuration process.</span></span> <span data-ttu-id="ef25e-116">IT-Administratoren konnten diese neue Benutzeroberfläche jedoch nur für bestimmte, von Jamf angegebene Anwendungen und bevorzugten Domänen verwenden.</span><span class="sxs-lookup"><span data-stu-id="ef25e-116">However, IT Admins could only use this new user interface for specific applications and preference domains specified by Jamf.</span></span>

<span data-ttu-id="ef25e-117">In Jamf Pro 10.19 kann ein Benutzer ein JSON-Manifest als "benutzerdefiniertes Schema" für eine beliebige bevorzugte Domäne hochladen, und die grafische Benutzeroberfläche wird aus diesem Manifest generiert.</span><span class="sxs-lookup"><span data-stu-id="ef25e-117">In Jamf Pro 10.19, a user can upload a JSON manifest as a "custom schema" to target any preference domain, and the graphical user interface will be generated from this manifest.</span></span> <span data-ttu-id="ef25e-118">Das erstellte benutzerdefinierte Schema folgt der JSON-Schemaspezifikation.</span><span class="sxs-lookup"><span data-stu-id="ef25e-118">The custom schema that's created follows the JSON Schema specification.</span></span>

<span data-ttu-id="ef25e-119">Weitere Informationen finden Sie im Jamf Pro-Administratorhandbuch unter [Computer Configuration Profiles](https://jamf.it/computer-configuration-profiles) (Computerkonfigurationsprofile).</span><span class="sxs-lookup"><span data-stu-id="ef25e-119">For more information, see [Computer Configuration Profiles](https://jamf.it/computer-configuration-profiles) in the Jamf Pro Administrator's Guide.</span></span>

## <span data-ttu-id="ef25e-120">Abrufen des Richtlinienmanifests für eine bestimmte Version von Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ef25e-120">Get the policy manifest for a specific version of Microsoft Edge</span></span>

<span data-ttu-id="ef25e-121">So rufen Sie das Richtlinienmanifest ab</span><span class="sxs-lookup"><span data-stu-id="ef25e-121">To get the policy manifest:</span></span>

- <span data-ttu-id="ef25e-122">Navigieren Sie zur [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise).</span><span class="sxs-lookup"><span data-stu-id="ef25e-122">Go to the [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise).</span></span>
- <span data-ttu-id="ef25e-123">Wählen Sie in der Dropdownliste „Kanal/Version“ \*\*einen beliebigen Kanal mit der Version 81 oder höher aus.\*\*\*.</span><span class="sxs-lookup"><span data-stu-id="ef25e-123">On the Channel/Version dropdown list, select \*\*any channel with version 81 or later.\*\*\*.</span></span>
- <span data-ttu-id="ef25e-124">Wählen Sie in der Dropdownliste „Build“ den Eintrag jeder \*\* 81 Build oder höher\*\* aus.\*\*\*.</span><span class="sxs-lookup"><span data-stu-id="ef25e-124">On the Build dropdown list, select any \*\*81 build or later.\*\*\*.</span></span>
- <span data-ttu-id="ef25e-125">Klicken Sie auf GET POLICY FILES (Richtliniendateien abrufen), um Ihr Richtlinienvorlagenpaket herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="ef25e-125">Click GET POLICY FILES to download our policy templates bundle.</span></span>

  > [!NOTE]
  > <span data-ttu-id="ef25e-126">Derzeit ist das Richtlinienvorlagenpaket als CAB-Datei signiert.</span><span class="sxs-lookup"><span data-stu-id="ef25e-126">Currently, the policy templates bundle is signed as a CAB file.</span></span> <span data-ttu-id="ef25e-127">Sie müssen ein Drittanbietertool verwenden, z.B. The Unarchiver, um die Datei unter macOS zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ef25e-127">You'll need to use a 3rd party tool, such as The Unarchiver to open the file on macOS.</span></span>

<span data-ttu-id="ef25e-128">Nachdem Sie die CAB-Datei entpackt haben, entpacken Sie die ZIP-Datei, und navigieren Sie zum Verzeichnis "Mac" auf der obersten Ebene.</span><span class="sxs-lookup"><span data-stu-id="ef25e-128">After you unpack the CAB file, unpack the ZIP file and navigate to the "mac" top level directory.</span></span> <span data-ttu-id="ef25e-129">Das Manifest namens "policy_manifest.json" befindet sich in diesem Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="ef25e-129">The manifest, which is named "policy_manifest.json", is in this directory.</span></span>

<span data-ttu-id="ef25e-130">Dieses Manifest wird ab Build 81.0.416.3 in jedem Richtlinienpaket veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="ef25e-130">This manifest will be published in every policy bundle starting with build 81.0.416.3.</span></span> <span data-ttu-id="ef25e-131">Wenn Sie Richtlinien im Dev Channel testen möchten, können Sie das den einzelnen Entwicklerreleases zugeordnete Manifest verwenden und in Jamf Pro testen.</span><span class="sxs-lookup"><span data-stu-id="ef25e-131">If you want to test policies in the Dev channel, you can take the manifest associated with each Dev release and test it in Jamf Pro.</span></span>  

## <span data-ttu-id="ef25e-132">Verwenden des Richtlinienmanifests in Jamf Pro</span><span class="sxs-lookup"><span data-stu-id="ef25e-132">Use the policy manifest in Jamf Pro</span></span>

<span data-ttu-id="ef25e-133">Führen Sie die folgenden Schritte aus, um das Richtlinienmanifest in Jamf Pro hochzuladen, und erstellen Sie dann ein Richtlinienprofil für macOS.</span><span class="sxs-lookup"><span data-stu-id="ef25e-133">Use the following steps to upload the policy manifest to Jamf Pro and then create a policy profile for macOS.</span></span>

1. <span data-ttu-id="ef25e-134">Melden Sie sich bei Jamf an.</span><span class="sxs-lookup"><span data-stu-id="ef25e-134">Sign in to Jamf.</span></span>
2. <span data-ttu-id="ef25e-135">Wählen Sie die Registerkarte **Computer** aus.</span><span class="sxs-lookup"><span data-stu-id="ef25e-135">Select the **Computer** tab.</span></span>
3. <span data-ttu-id="ef25e-136">Wählen Sie unter **Content Management** (Inhaltsverwaltung) **Configuration Profiles** (Konfigurationsprofile) aus.</span><span class="sxs-lookup"><span data-stu-id="ef25e-136">Under **Content Management**, select **Configuration Profiles**.</span></span>
4. <span data-ttu-id="ef25e-137">Klicken Sie auf der Seite **Configuration Profiles** (Konfigurationsprofile) auf **+ New** (Neu).</span><span class="sxs-lookup"><span data-stu-id="ef25e-137">On the **Configuration Profiles** page, click **+ New**.</span></span>

   ![Hinzufügen eines neuen Profils in Jamf](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-configuration-profiles.png)

5. <span data-ttu-id="ef25e-139">Wählen Sie unter **New macOS Configuration Profile** (Neues macOS-Konfigurationsprofil) >**Options** (Optionen) **Application & Custom Settings** (Anwendungs- und benutzerdefinierte Einstellungen) aus.</span><span class="sxs-lookup"><span data-stu-id="ef25e-139">On **New macOS Configuration Profile**>**Options**, select **Application & Custom Settings**.</span></span>
6. <span data-ttu-id="ef25e-140">Klicken Sie im Popupfenster **Application & Custom Settings** (Anwendungs- und benutzerdefinierte Einstellungen) auf **Configure** (Konfigurieren).</span><span class="sxs-lookup"><span data-stu-id="ef25e-140">On the **Application & Custom Settings** popup window, click **Configure**.</span></span>

   ![Konfigurieren von Anwendungseinstellungen und benutzerdefinierten Einstellungen](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-app-and-custom.png)

7. <span data-ttu-id="ef25e-142">Legen Sie im Abschnitt **Application & Custom Settings** (Anwendungs- und benutzerdefinierte Einstellungen) die im folgenden Screenshot dargestellten Werte fest.</span><span class="sxs-lookup"><span data-stu-id="ef25e-142">In the **Application & Custom Settings** section, set the values shown in the following screen shot.</span></span>

   ![Profilquelle und benutzerdefiniertes Schema](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-app-and-custom-schema.png)

   - <span data-ttu-id="ef25e-144">Wählen Sie für **Creation Method** (Erstellungsmethode) die Option **Configure settings** (Einstellungen konfigurieren) aus.</span><span class="sxs-lookup"><span data-stu-id="ef25e-144">For **Creation Method**, pick **Configure settings**.</span></span>
   - <span data-ttu-id="ef25e-145">Wählen Sie für **Source** (Quelle) die Option **Custom Schema** (Benutzerdefiniertes Schema) aus.</span><span class="sxs-lookup"><span data-stu-id="ef25e-145">For **Source**, pick **Custom Schema**.</span></span>
   - <span data-ttu-id="ef25e-146">Geben Sie für **Preference Domain** (Bevorzugte Domäne) den Namen Ihrer Domäne an.</span><span class="sxs-lookup"><span data-stu-id="ef25e-146">For **Preference Domain**, provide the name of your domain.</span></span> <span data-ttu-id="ef25e-147">In diesem Beispiel wird *com.microsoft.Edge* als Domäne verwendet.</span><span class="sxs-lookup"><span data-stu-id="ef25e-147">This example uses *com.microsoft.Edge* as the domain.</span></span>
   - <span data-ttu-id="ef25e-148">Fügen Sie für **Custom Schema** (Benutzerdefiniertes Schema) den Inhalt der Manifestdatei "policy_manifest.json" ein.</span><span class="sxs-lookup"><span data-stu-id="ef25e-148">For **Custom Schema**, paste the contents of the "policy_manifest.json" manifest file.</span></span>
   - <span data-ttu-id="ef25e-149">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="ef25e-149">Click **Save**.</span></span>

8. <span data-ttu-id="ef25e-150">Nachdem Sie das Profil gespeichert haben, zeigt Jamf den Abschnitt **General** (Allgemein) an, wie im nächsten Screenshot dargestellt.</span><span class="sxs-lookup"><span data-stu-id="ef25e-150">After you save the profile, Jamf displays the **General** section shown in the next screen shot.</span></span>

   ![Abschnitt "Configure General" (Konfigurieren, Allgemein)](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-app-and-custom-general-setting.png)

   - <span data-ttu-id="ef25e-152">Geben Sie einen **Anzeigenamen** und eine **Beschreibung** für das Profil ein.</span><span class="sxs-lookup"><span data-stu-id="ef25e-152">Provide a display **Name** for the profile and a **Description**.</span></span>
   - <span data-ttu-id="ef25e-153">Behalten Sie die Standardeinstellung **None** (Keine) für **Category** (Kategorie) bei.</span><span class="sxs-lookup"><span data-stu-id="ef25e-153">Keep the default setting for **Category**, which is **None**.</span></span>
   - <span data-ttu-id="ef25e-154">Für **Distribution Method** (Verteilungsmethode) lauten die Optionen **Install Automatically** (Automatisch installieren) oder **Make Available in Self Service** (Im Self-Service bereitstellen).</span><span class="sxs-lookup"><span data-stu-id="ef25e-154">For **Distribution Method**, the options are **Install Automatically** or **Make Available in Self Service**.</span></span>
   - <span data-ttu-id="ef25e-155">Für **Level** (Ebene) lauten die Optionen **User Level** (Benutzerebene) oder **Computer Level** (Computerebene).</span><span class="sxs-lookup"><span data-stu-id="ef25e-155">For **Level**, the options are **User Level** or **Computer Level**.</span></span>
   - <span data-ttu-id="ef25e-156">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="ef25e-156">Click **Save**.</span></span>

9. <span data-ttu-id="ef25e-157">Nachdem Sie den Abschnitt "General" (Allgemein) gespeichert haben, zeigt Jamf das Microsoft Edge Beta Channel-Konfigurationsprofil an, das in unserem Beispiel eingerichtet wurde.</span><span class="sxs-lookup"><span data-stu-id="ef25e-157">After you save the General section, Jamf shows the "Microsoft Edge Beta Channel" configuration profile set up for our example.</span></span> <span data-ttu-id="ef25e-158">Beachten Sie im nächsten Screenshot, dass Sie das Profil weiter bearbeiten können, indem Sie auf **Edit** (Bearbeiten) klicken. Wenn Sie fertig sind, klicken Sie auf **Done** (Fertig).</span><span class="sxs-lookup"><span data-stu-id="ef25e-158">In the next screen shot, note that you can keep working the profile by clicking **Edit** or if you're finished, click **Done**.</span></span>

   ![Neues Konfigurationsprofil mit Optionen](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-configuration-profiles-beta-channel.png)

   > [!NOTE]
   > <span data-ttu-id="ef25e-160">Sie können dieses Profil, nachdem es gespeichert wurde, oder auch in einer anderen Jamf-Sitzung bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="ef25e-160">You can edit this profile after it's been saved and in another Jamf session.</span></span> <span data-ttu-id="ef25e-161">So könnten Sie beispielsweise die Verteilungsmethode so ändern, dass sie im Self-Service bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="ef25e-161">For example, you might decide to change the Distribution Method to Make Available in Self Service.</span></span>

   <span data-ttu-id="ef25e-162">Wenn Sie im Microsoft Edge Stable-Kanal eine Nachbearbeitung durchführen oder es löschen möchten, wählen Sie den Profilnamen aus, der im folgenden Screenshot der Konfigurationsprofile dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="ef25e-162">To do a follow up edit on the Microsoft Edge Stable Channel, or delete it, select the profile name, shown in the following Configuration Profiles screen shot.</span></span>

   ![Liste der Konfigurationsprofile](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-configuration-profiles-beta-channel-done.png)

<span data-ttu-id="ef25e-164">Nachdem Sie das neue Konfigurationsprofil erstellt haben, müssen Sie noch den **Scope** (Geltungsbereich) für das Profil konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="ef25e-164">After you create the new configuration profile you still have to configure the **Scope** for the profile.</span></span>

### <span data-ttu-id="ef25e-165">So konfigurieren Sie den Geltungsbereich</span><span class="sxs-lookup"><span data-stu-id="ef25e-165">To configure the scope</span></span>

1. <span data-ttu-id="ef25e-166">Stellen Sie für **Targets** (Ziele) die folgenden Minimaleinstellungen bereit:</span><span class="sxs-lookup"><span data-stu-id="ef25e-166">For **Targets**, provide the following minimum settings:</span></span>

   - <span data-ttu-id="ef25e-167">ZIELCOMPUTER.</span><span class="sxs-lookup"><span data-stu-id="ef25e-167">TARGET COMPUTERS.</span></span> <span data-ttu-id="ef25e-168">Die Optionen sind "Bestimmte Computer" oder "Alle Computer".</span><span class="sxs-lookup"><span data-stu-id="ef25e-168">The options are Specific Computers or All Computers.</span></span>
   - <span data-ttu-id="ef25e-169">ZIELBENUTZER.</span><span class="sxs-lookup"><span data-stu-id="ef25e-169">TARGET USERS.</span></span> <span data-ttu-id="ef25e-170">Die Optionen sind "Bestimmte Benutzer" oder "Alle Benutzer".</span><span class="sxs-lookup"><span data-stu-id="ef25e-170">The options are Specific Users or All Users.</span></span>
   - <span data-ttu-id="ef25e-171">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="ef25e-171">Click **Save**.</span></span>
2. <span data-ttu-id="ef25e-172">Behalten Sie für **Limitations** (Beschränkungen) die Standardeinstellung bei: "None" (Keine).</span><span class="sxs-lookup"><span data-stu-id="ef25e-172">For **Limitations**, keep the default setting: None.</span></span> <span data-ttu-id="ef25e-173">Klicken Sie auf **Abbrechen**.</span><span class="sxs-lookup"><span data-stu-id="ef25e-173">Click **Cancel**.</span></span>
3. <span data-ttu-id="ef25e-174">Behalten Sie für **Exclusions** (Ausschlüsse) die Standardeinstellung bei: "None" (Keine).</span><span class="sxs-lookup"><span data-stu-id="ef25e-174">For **Exclusions**, keep the default setting: None.</span></span> <span data-ttu-id="ef25e-175">Klicken Sie auf **Abbrechen**.</span><span class="sxs-lookup"><span data-stu-id="ef25e-175">Click **Cancel**.</span></span>

## <span data-ttu-id="ef25e-176">Häufig gestellte Fragen</span><span class="sxs-lookup"><span data-stu-id="ef25e-176">Frequently Asked Questions</span></span>

### <span data-ttu-id="ef25e-177">Kann Microsoft Edge für die Verwendung von Master-Einstellungen konfiguriert werden?</span><span class="sxs-lookup"><span data-stu-id="ef25e-177">Can Microsoft Edge be configured to use master preferences?</span></span>

<span data-ttu-id="ef25e-178">Ja, Sie können Microsoft Edge so konfigurieren, dass es eine Mastervoreinstellungsdatei verwendet.</span><span class="sxs-lookup"><span data-stu-id="ef25e-178">Yes, you can configure Microsoft Edge to use a master preferences file.</span></span>

<span data-ttu-id="ef25e-179">Mit einer Mastervoreinstellungsdatei können Sie Standardeinstellungen für ein Browser-Benutzerprofil konfigurieren, wenn Microsoft Edge bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="ef25e-179">A master preferences file lets you configure default settings for a browser user profile when Microsoft Edge is deployed.</span></span> <span data-ttu-id="ef25e-180">Sie können auch eine Mastervoreinstellungsdatei verwenden, um Einstellungen auf Computern anzuwenden, die nicht von einem Geräteverwaltungssystem verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="ef25e-180">You can also use a master preferences file to apply settings on computers that aren't managed by a device management system.</span></span> <span data-ttu-id="ef25e-181">Diese Einstellungen werden auf das Profil des Benutzers angewendet, wenn der Benutzer zum ersten Mal den Browser ausführt.</span><span class="sxs-lookup"><span data-stu-id="ef25e-181">These settings are applied to the user’s profile the first time the user runs the browser.</span></span> <span data-ttu-id="ef25e-182">Nachdem der Benutzer den Browser ausgeführt hat, werden Änderungen an der Mastervoreinstellungsdatei nicht angewendet.</span><span class="sxs-lookup"><span data-stu-id="ef25e-182">After the user runs the browser, changes to the master preferences file aren’t applied.</span></span> <span data-ttu-id="ef25e-183">Benutzer können Einstellungen aus den Mastervoreinstellungen im Browser ändern.</span><span class="sxs-lookup"><span data-stu-id="ef25e-183">A user can change settings from the master preferences in the browser.</span></span> <span data-ttu-id="ef25e-184">Wenn Sie eine Einstellung zwingend vornehmen oder eine Einstellung nach der ersten Ausführung des Browsers ändern möchten, müssen Sie eine Richtlinie verwenden.</span><span class="sxs-lookup"><span data-stu-id="ef25e-184">If you want to make a setting mandatory or change a setting after the first run of the browser, you must use a policy.</span></span>

<span data-ttu-id="ef25e-185">Mit einer Mastervoreinstellungsdatei können Sie viele verschiedene Einstellungen und Voreinstellungen für den Browser anpassen, einschließlich der für andere Chromium-basierte Browser und Microsoft Edge-spezifische Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="ef25e-185">A master preferences file lets you to customize many different settings and preferences for the browser, including those shared with other Chromium based browsers and specific to Microsoft Edge.</span></span>  <span data-ttu-id="ef25e-186">Richtlinienbezogene Voreinstellungen können mithilfe der Mastervoreinstellungsdatei konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="ef25e-186">Policy related preferences can be configured using the master preferences file.</span></span> <span data-ttu-id="ef25e-187">In Fällen, in denen eine Richtlinie festgelegt ist und ein entsprechender Master-Voreinstellungssatz vorhanden ist, hat die Richtlinieneinstellung Vorrang.</span><span class="sxs-lookup"><span data-stu-id="ef25e-187">In cases where a policy is set and there’s a corresponding master preference set, the policy setting takes precedence.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ef25e-188">Möglicherweise sind nicht alle verfügbaren Einstellungen mit der Microsoft Edge-Terminologie und den Namenskonventionen konsistent.</span><span class="sxs-lookup"><span data-stu-id="ef25e-188">All the available preferences might not be consistent with Microsoft Edge terminology and naming conventions.</span></span>  <span data-ttu-id="ef25e-189">Es besteht keine Garantie dafür, dass diese Voreinstellungen in zukünftigen Versionen weiterhin wie erwartet funktionieren.</span><span class="sxs-lookup"><span data-stu-id="ef25e-189">There’s no guarantee that these preferences will continue to work as expected in future releases.</span></span> <span data-ttu-id="ef25e-190">Voreinstellungen werden in späteren Versionen möglicherweise geändert oder ignoriert.</span><span class="sxs-lookup"><span data-stu-id="ef25e-190">Preferences might be changed or ignored in later versions.</span></span>

<span data-ttu-id="ef25e-191">Eine Master-Voreinstellungsdatei ist eine Textdatei, die mit JSON-Markup formatiert wurde.</span><span class="sxs-lookup"><span data-stu-id="ef25e-191">A master preferences file is a text file that’s formatted using JSON markup.</span></span> <span data-ttu-id="ef25e-192">Diese Datei muss demselben Verzeichnis wie die ausführbare msedge.exe-Datei hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="ef25e-192">This file needs to be added to the same directory as the msedge.exe executable.</span></span> <span data-ttu-id="ef25e-193">Für systemweite Enterprise-Bereitstellungen auf macOS ist die sin der Regel: „*~/Library/Application Support/Microsoft/Microsoft Edge Master Preferences*” oder „*/Library/Microsoft/Microsoft Edge Master Preferences*”.</span><span class="sxs-lookup"><span data-stu-id="ef25e-193">For system wide enterprise deployments on macOS this is typically: “*~/Library/Application Support/Microsoft/Microsoft Edge Master Preferences*" or "*/Library/Microsoft/Microsoft Edge Master Preferences*”.</span></span>

## <span data-ttu-id="ef25e-194">Weitere Informationen:</span><span class="sxs-lookup"><span data-stu-id="ef25e-194">See also</span></span>

- [<span data-ttu-id="ef25e-195">Microsoft Edge Enterprise-Angebotsseite</span><span class="sxs-lookup"><span data-stu-id="ef25e-195">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="ef25e-196">Konfigurieren für macOS mit Intune</span><span class="sxs-lookup"><span data-stu-id="ef25e-196">Configure for macOS with Intune</span></span>](configure-microsoft-edge-on-mac.md)
- [<span data-ttu-id="ef25e-197">Konfigurieren für Windows</span><span class="sxs-lookup"><span data-stu-id="ef25e-197">Configure for Windows</span></span>](configure-microsoft-edge.md)
- [<span data-ttu-id="ef25e-198">Konfigurieren für Windows mit Intune</span><span class="sxs-lookup"><span data-stu-id="ef25e-198">Configure for Windows with Intune</span></span>](configure-edge-with-intune.md)
