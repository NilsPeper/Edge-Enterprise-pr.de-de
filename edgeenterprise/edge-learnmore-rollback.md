---
title: Microsoft Edge-Rollback für Unternehmen
ms.author: v-danwes
author: dan-wesley
manager: srugh
ms.date: 07/21/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: So setzen Sie Microsoft Edge auf eine vorherige Version zurück
ms.openlocfilehash: 9af0881a079dd3059e567eaadb912b3d929924c4
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979977"
---
# <span data-ttu-id="105c1-103">Zurücksetzen von Microsoft Edge auf eine vorherige Version</span><span class="sxs-lookup"><span data-stu-id="105c1-103">How to roll back Microsoft Edge to a previous version</span></span>

<span data-ttu-id="105c1-104">In diesem Artikel wird beschrieben, wie Sie mithilfe des Rollback-Features ein Rollback zu einer früheren Version von Microsoft Edge durchführen können.</span><span class="sxs-lookup"><span data-stu-id="105c1-104">This article describes how to roll back to a previous version of Microsoft Edge using the rollback feature.</span></span>

>[!NOTE]
><span data-ttu-id="105c1-105">Dieser Artikel bezieht sich auf Microsoft Edge Version 86 oder höher.</span><span class="sxs-lookup"><span data-stu-id="105c1-105">This article applies to Microsoft Edge version 86 or later.</span></span>

## <span data-ttu-id="105c1-106">Einführung in die Zurücksetzung</span><span class="sxs-lookup"><span data-stu-id="105c1-106">Introduction to rollback</span></span>

<span data-ttu-id="105c1-107">Durch ein Rollback können Sie Ihre Microsoft Edge-Browserversion auf eine frühere Version zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="105c1-107">Rollback lets you replace your Microsoft Edge browser version with an earlier version.</span></span> <span data-ttu-id="105c1-108">Das Rollback-Feature dient als Sicherheitsnetz für Unternehmen, die Microsoft Edge bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="105c1-108">This feature is designed to be a safety net for enterprises deploying Microsoft Edge.</span></span> <span data-ttu-id="105c1-109">Es bietet eine Möglichkeit zur Behandlung von Problemen mit Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="105c1-109">It provides a way to troubleshoot issues with Microsoft Edge.</span></span> <span data-ttu-id="105c1-110">Zu den Vorteilen eines Rollbacks zählt die Möglichkeit, schnell und einfach zu einer vorherigen Browserversion zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="105c1-110">The benefits of rollback are the ability to revert to previous browser version easily and quickly.</span></span> <span data-ttu-id="105c1-111">Ein Rollback verringert die potenziellen Auswirkungen eines Microsoft Edge-Problems auf Geschäftsvorgänge.</span><span class="sxs-lookup"><span data-stu-id="105c1-111">Rollback reduces the potential impact that a Microsoft Edge issue has on business operations.</span></span>

## <span data-ttu-id="105c1-112">Vorbemerkungen</span><span class="sxs-lookup"><span data-stu-id="105c1-112">Before you begin</span></span>

<span data-ttu-id="105c1-113">Es ist wichtig zu verstehen, wie das Rollback-Feature in einer Microsoft Edge-Umgebung installiert wird.</span><span class="sxs-lookup"><span data-stu-id="105c1-113">It's important to understand how the rollback feature is installed in a Microsoft Edge environment.</span></span> <span data-ttu-id="105c1-114">Sie können das Rollback mithilfe von zwei unterschiedlichen Methoden durchführen: manuell mit einer MSI-Datei oder mithilfe von Microsoft Edge Update- und Gruppenrichtlinien.</span><span class="sxs-lookup"><span data-stu-id="105c1-114">You can deploy rollback using two different methods: manually with an MSI or by using Microsoft Edge update and Group Policy.</span></span> <span data-ttu-id="105c1-115">Außerdem empfehlen wir die Verwendung einer Auswahl von Gruppenrichtlinien für eine reibungslosere Durchführung.</span><span class="sxs-lookup"><span data-stu-id="105c1-115">We also  encourage using a selection of Group Policies for a smoother deployment.</span></span>

### <span data-ttu-id="105c1-116">Empfehlungen</span><span class="sxs-lookup"><span data-stu-id="105c1-116">Recommendations</span></span>

<span data-ttu-id="105c1-117">Das Rollback-Feature dient als vorübergehender Fix für Probleme, die eventuell durch ein Microsoft Edge-Browserupdate entstehen.</span><span class="sxs-lookup"><span data-stu-id="105c1-117">The rollback feature is meant to be a temporary fix for issues you might find in a Microsoft Edge browser update.</span></span> <span data-ttu-id="105c1-118">Wir empfehlen Benutzern, die neueste Version des Microsoft Edge-Browsers zu installieren, um die durch die aktuellsten Sicherheitsupdates bereitgestellten Schutzfunktionen nutzen zu können.</span><span class="sxs-lookup"><span data-stu-id="105c1-118">We recommend that users install the latest version of the Microsoft Edge browser to use the protection provided by the latest security updates.</span></span> <span data-ttu-id="105c1-119">Ein Rollback zu einer früheren Version birgt Risiken, die mit bekannten Sicherheitsproblemen zu tun haben.</span><span class="sxs-lookup"><span data-stu-id="105c1-119">Rollback to an earlier version risks exposure to known security issues.</span></span>

<span data-ttu-id="105c1-120">Bevor Sie die Browserversion vorübergehend zurücksetzen, empfehlen wir dringend, die Synchronisierung für alle Benutzer in Ihrer Organisation zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="105c1-120">Before temporarily rolling back your browser version, we also highly recommend that you enable Sync for all the users in your organization.</span></span> <span data-ttu-id="105c1-121">Wenn Sie die Synchronisierung nicht aktivieren, besteht das Risiko eines endgültigen Verlusts von Browserdaten.</span><span class="sxs-lookup"><span data-stu-id="105c1-121">If you don't turn on Sync, there's a risk of permanent browsing data loss.</span></span> <span data-ttu-id="105c1-122">Weitere Informationen zur Synchronisierung finden Sie unter [Microsoft Edge-Synchronisierung](microsoft-edge-enterprise-sync.md).</span><span class="sxs-lookup"><span data-stu-id="105c1-122">For more information about Sync, see [Microsoft Edge Sync](microsoft-edge-enterprise-sync.md).</span></span>

> [!CAUTION]
> <span data-ttu-id="105c1-123">Führen Sie ein Rollback nur bei tatsächlichem Bedarf durch, da es immer das Risiko von Datenverlusten birgt.</span><span class="sxs-lookup"><span data-stu-id="105c1-123">Only use rollback when necessary, there's always the risk of data loss.</span></span>

## <span data-ttu-id="105c1-124">Manuelles Aktivieren des Rollbacks mit einer MSI-Datei</span><span class="sxs-lookup"><span data-stu-id="105c1-124">Enable rollback manually with an MSI</span></span>

<span data-ttu-id="105c1-125">Führen Sie die folgenden Schritte aus, um die Zurücksetzung mit einer MSI-Datei manuell durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="105c1-125">Use the following steps to roll back manually with an MSI.</span></span>

1. <span data-ttu-id="105c1-126">Deaktivieren Sie Microsoft Edge-Updates.</span><span class="sxs-lookup"><span data-stu-id="105c1-126">Disable Microsoft Edge Updates.</span></span>

   > [!NOTE]
   > <span data-ttu-id="105c1-127">Wir empfehlen, die aktuellsten administrativen Vorlagen zu installieren.</span><span class="sxs-lookup"><span data-stu-id="105c1-127">We recommend that you install the most current Administrative templates.</span></span> <span data-ttu-id="105c1-128">Weitere Informationen finden Sie unter [Herunterladen und Installieren der administrativen Vorlage für Microsoft Edge](https://docs.microsoft.com/DeployEdge/configure-microsoft-edge#1-download-and-install-the-microsoft-edge-administrative-template).</span><span class="sxs-lookup"><span data-stu-id="105c1-128">For more information, see [Download and install the Microsoft Edge administrative template](https://docs.microsoft.com/DeployEdge/configure-microsoft-edge#1-download-and-install-the-microsoft-edge-administrative-template).</span></span>

   - <span data-ttu-id="105c1-129">Öffnen Sie den Editor für lokale Gruppenrichtlinien, und wechseln Sie zu *Computerkonfiguration > Administrative Vorlagen > Microsoft Edge Update > Anwendungen > Microsoft Edge>*.</span><span class="sxs-lookup"><span data-stu-id="105c1-129">Open the local Group Policy Editor and go to *Computer Configuration>Administrative Templates>Microsoft Edge Update>Applications>Microsoft Edge>*.</span></span>
   - <span data-ttu-id="105c1-130">Wählen Sie **Außerkraftsetzung von Updaterichtlinien** aus, und wählen Sie dann **Aktiviert** aus.</span><span class="sxs-lookup"><span data-stu-id="105c1-130">Select **Update policy override** and then select **Enabled**.</span></span>
   - <span data-ttu-id="105c1-131">Wählen Sie unter **Optionen** aus der Richtlinien-Dropdownliste den Eintrag **Update deaktiviert** aus.</span><span class="sxs-lookup"><span data-stu-id="105c1-131">Under **Options**, pick **Update disabled** from the Policy dropdown list.</span></span>

2. <span data-ttu-id="105c1-132">Laden Sie die MSI-Datei herunter.</span><span class="sxs-lookup"><span data-stu-id="105c1-132">Get the MSI.</span></span>

   - <span data-ttu-id="105c1-133">Laden Sie [hier](https://www.microsoft.com/edge/business/download) die MSI-Datei für die Version herunter, zu der Sie zurückkehren möchten.</span><span class="sxs-lookup"><span data-stu-id="105c1-133">Download the MSI for the version you want to roll back to [from here](https://www.microsoft.com/edge/business/download).</span></span>
   - <span data-ttu-id="105c1-134">Speichern Sie die MSI-Datei auf Ihrem Desktop.</span><span class="sxs-lookup"><span data-stu-id="105c1-134">Save the MSI to your desktop.</span></span>

3. <span data-ttu-id="105c1-135">Führen Sie den Rollback-Befehl aus.</span><span class="sxs-lookup"><span data-stu-id="105c1-135">Run the rollback command.</span></span>

   - <span data-ttu-id="105c1-136">Öffnen Sie die Windows-Eingabeaufforderung mit **Als Administrator ausführen**.</span><span class="sxs-lookup"><span data-stu-id="105c1-136">Open the Windows command prompt with **Run as administrator**.</span></span>
   - <span data-ttu-id="105c1-137">Geben Sie den folgenden Befehl ein, wobei *C:\Users\username\Desktop\test*  der Pfad zu der heruntergeladenen MSI-Datei ist, und „FileName“ der Name der .msi-Datei:</span><span class="sxs-lookup"><span data-stu-id="105c1-137">Type the following command, where: *C:\Users\username\Desktop\test* is the path to the MSI you downloaded, and FileName is the name of the .msi file:</span></span><br>
 `C:\Users\username\Desktop\test>msiexec /I FileName.msi /qn ALLOWDOWNGRADE=1`<br>
     > [!NOTE]
     > <span data-ttu-id="105c1-138">Weitere Informationen zu „msiexec“ finden Sie unter [msiexec](https://docs.microsoft.com/windows-server/administration/windows-commands/msiexec).</span><span class="sxs-lookup"><span data-stu-id="105c1-138">For more information about msiexec, see [msiexec](https://docs.microsoft.com/windows-server/administration/windows-commands/msiexec).</span></span>
   - <span data-ttu-id="105c1-139">Schließen Sie Microsoft Edge, und öffnen Sie ihn erneut, um zu überprüfen, ob das Rollback erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="105c1-139">Close and reopen Microsoft Edge to verify that the rollback worked.</span></span> <span data-ttu-id="105c1-140">Wechseln Sie unter **Einstellungen und mehr** (ALT + F) zu **Einstellungen**, und wählen Sie **Über Microsoft Edge** aus.</span><span class="sxs-lookup"><span data-stu-id="105c1-140">Under **Settings and more** (ALT + F), go to **Settings** and select **About Microsoft Edge**.</span></span>

## <span data-ttu-id="105c1-141">Aktivieren des Rollbacks mit Microsoft Edge-Update- und Gruppenrichtlinien</span><span class="sxs-lookup"><span data-stu-id="105c1-141">Enable rollback with Microsoft Edge update and Group Policy</span></span>

<span data-ttu-id="105c1-142">Führen Sie die folgenden Schritte aus, um das Rollback über Microsoft Edge Update- und Gruppenrichtlinien zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="105c1-142">Use the following steps to enable rollback with Microsoft Edge update and Group Policy.</span></span>

1. <span data-ttu-id="105c1-143">Öffnen Sie den Editor für lokale Gruppenrichtlinien, und wechseln Sie zu *Computerkonfiguration > Administrative Vorlagen > Microsoft Edge Update > Anwendungen > Microsoft Edge>*.</span><span class="sxs-lookup"><span data-stu-id="105c1-143">Open the local Group Policy Editor and go to *Computer Configuration>Administrative Templates>Microsoft Edge Update>Applications>Microsoft Edge>*.</span></span>
2. <span data-ttu-id="105c1-144">Wählen Sie **Zurücksetzen auf Zielversion** aus, und wählen Sie dann **Aktiviert**aus.</span><span class="sxs-lookup"><span data-stu-id="105c1-144">Select **Rollback to target version** and then select **Enabled**.</span></span>
3. <span data-ttu-id="105c1-145">Wählen Sie **Zielversion außer Kraft setzen** und dann die Browserversion aus, auf die Microsoft Edge zurückgesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="105c1-145">Select **Target version override** and pick the browser version you want to roll back to.</span></span>
4. <span data-ttu-id="105c1-146">Wählen Sie **Außerkraftsetzung von Updaterichtlinien** aus, und wählen Sie dann **Aktiviert** aus.</span><span class="sxs-lookup"><span data-stu-id="105c1-146">Select **Update policy override** and then select **Enabled**.</span></span> <span data-ttu-id="105c1-147">Wählen Sie unter **Optionen** in der Richtlinien-Dropdownliste eine der folgenden Optionen aus (mit Ausnahme von **Update deaktiviert**):</span><span class="sxs-lookup"><span data-stu-id="105c1-147">Under **Options**, pick one of the following options from the Policy dropdown list (except for **Update disabled**):</span></span>

   - <span data-ttu-id="105c1-148">Updates immer zulassen</span><span class="sxs-lookup"><span data-stu-id="105c1-148">Always allow updates</span></span>
   - <span data-ttu-id="105c1-149">Nur automatische unbeaufsichtigte Updates</span><span class="sxs-lookup"><span data-stu-id="105c1-149">Automatic silent updates only</span></span>
   - <span data-ttu-id="105c1-150">Nur manuelle Updates</span><span class="sxs-lookup"><span data-stu-id="105c1-150">Manual updates only</span></span>  

5. <span data-ttu-id="105c1-151">Das Rollback erfolgt, wenn Microsoft Edge Update das nächste Mal nach einem Update sucht.</span><span class="sxs-lookup"><span data-stu-id="105c1-151">Rollback will happen the next time Microsoft Edge Update checks for an update.</span></span>

   > [!NOTE]
   > <span data-ttu-id="105c1-152">Wenn Sie das Rollback sofort ausführen möchten, müssen Sie das Microsoft Edge Update-Abrufintervall ändern oder das Rollback mithilfe einer MSI-Datei aktivieren.</span><span class="sxs-lookup"><span data-stu-id="105c1-152">If you want rollback to happen right away you have to change the Microsoft Edge Update polling interval or enable rollback using an MSI.</span></span>

### <span data-ttu-id="105c1-153">Häufige Fehler bei der Zurücksetzung</span><span class="sxs-lookup"><span data-stu-id="105c1-153">Common rollback errors</span></span>

<span data-ttu-id="105c1-154">Die folgenden Fehler verhindern ein Rollback:</span><span class="sxs-lookup"><span data-stu-id="105c1-154">The following errors will prevent rollback:</span></span>

- <span data-ttu-id="105c1-155">Eingabe ist eine nicht unterstützte Zielversion</span><span class="sxs-lookup"><span data-stu-id="105c1-155">Input is an unsupported target version</span></span>
- <span data-ttu-id="105c1-156">Eingabe ist eine nicht vorhandene Zielversion</span><span class="sxs-lookup"><span data-stu-id="105c1-156">Input is a non-existent target version</span></span>
- <span data-ttu-id="105c1-157">Eingabe ist falsch formatiert</span><span class="sxs-lookup"><span data-stu-id="105c1-157">Input is incorrectly formatted</span></span>

### <span data-ttu-id="105c1-158">Empfohlene Gruppenrichtlinien</span><span class="sxs-lookup"><span data-stu-id="105c1-158">Recommended Group Policies</span></span>

<span data-ttu-id="105c1-159">Die folgenden Gruppenrichtlinien und Einstellungen werden für die Durchführung des Rollbacks dringend empfohlen.</span><span class="sxs-lookup"><span data-stu-id="105c1-159">The following group policies and settings are highly recommended for using rollback.</span></span>

#### <span data-ttu-id="105c1-160">Gruppenrichtlinien für die Synchronisierung</span><span class="sxs-lookup"><span data-stu-id="105c1-160">Sync Group Policies</span></span>

- <span data-ttu-id="105c1-161">ForceSync.</span><span class="sxs-lookup"><span data-stu-id="105c1-161">ForceSync.</span></span> <span data-ttu-id="105c1-162">Legen Sie ForceSync auf „Aktiviert“ fest.</span><span class="sxs-lookup"><span data-stu-id="105c1-162">Set ForceSync to enabled.</span></span> <span data-ttu-id="105c1-163">Durch diese Richtlinie wird die Aktivierung der Synchronisierung für alle Azure Active Directory (Azure AD)-Benutzer erzwungen.</span><span class="sxs-lookup"><span data-stu-id="105c1-163">This policy will force enable Sync on all Azure Active Directory (Azure AD) users.</span></span> <span data-ttu-id="105c1-164">Diese Richtlinie gilt nur für Microsoft Edge-Versionen 86 und höher.</span><span class="sxs-lookup"><span data-stu-id="105c1-164">This policy is only effective for Microsoft Edge versions 86 and later.</span></span>
- <span data-ttu-id="105c1-165">Über *Liste der Typen konfigurieren, die von der Synchronisierungsrichtlinie ausgeschlossen werden* können Administratoren steuern, welche Daten von Benutzern synchronisiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="105c1-165">The *Configure the list of the types that are excluded from synchronization policy* allows admins to control what data can be synced by users.</span></span>

#### <span data-ttu-id="105c1-166">Gruppenrichtlinien für Browser-Neustart</span><span class="sxs-lookup"><span data-stu-id="105c1-166">Browser restart Group Policies</span></span>

<span data-ttu-id="105c1-167">Es empfiehlt sich, nach dem Aktivieren des Rollbacks einen Neustart für die Benutzer zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="105c1-167">We recommend forcing a restart on users after rollback is enabled.</span></span>

- <span data-ttu-id="105c1-168">Aktivieren Sie *Einen Benutzer informieren, dass für ausstehende Updates ein Browser-Neustart empfohlen oder erforderlich ist*.</span><span class="sxs-lookup"><span data-stu-id="105c1-168">Enable *Notify a user that a browser restart is recommended or required for pending updates*.</span></span> <span data-ttu-id="105c1-169">Wählen Sie unter „Optionen“ **Erforderlich** aus.</span><span class="sxs-lookup"><span data-stu-id="105c1-169">Under Options, select **Required**.</span></span>
- <span data-ttu-id="105c1-170">Aktivieren Sie *Zeitraum für Updatebenachrichtigungen festlegen*, und legen Sie dann die gewünschte Zeit in Millisekunden fest.</span><span class="sxs-lookup"><span data-stu-id="105c1-170">Enable *Set the time period for update notifications* and then set the desired time in milliseconds.</span></span>

## <span data-ttu-id="105c1-171">Häufig gestellte Fragen</span><span class="sxs-lookup"><span data-stu-id="105c1-171">Frequently asked questions</span></span>

### <span data-ttu-id="105c1-172">Manuelles MSI-Rollback</span><span class="sxs-lookup"><span data-stu-id="105c1-172">Manual MSI rollback</span></span>

#### <span data-ttu-id="105c1-173">Welche allgemeinen MSI-Fehler können auftreten?</span><span class="sxs-lookup"><span data-stu-id="105c1-173">What generic MSI failures that can happen?</span></span>

1. <span data-ttu-id="105c1-174">Wenn die Gruppenrichtlinie zum Installieren von Updates deaktiviert ist, wird das Rollback nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="105c1-174">If the Install update group policy is disabled, rollback won't occur.</span></span>

   - <span data-ttu-id="105c1-175">Stellen Sie für die Ausführung des Rollbacks sicher, dass die Installationsrichtlinie **aktiviert** ist.</span><span class="sxs-lookup"><span data-stu-id="105c1-175">To use rollback, make sure Install is set to **Enabled**.</span></span> <span data-ttu-id="105c1-176">Wenn diese Richtlinie deaktiviert ist, wird verhindert, dass Microsoft Edge-Kanäle installiert werden.</span><span class="sxs-lookup"><span data-stu-id="105c1-176">When this policy is disabled, it prevents Microsoft Edge channels from being installed.</span></span> <span data-ttu-id="105c1-177">Weitere Informationen finden Sie unter [Installation](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#install).</span><span class="sxs-lookup"><span data-stu-id="105c1-177">For more information, see [Install](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#install).</span></span>

2. <span data-ttu-id="105c1-178">Wenn keine Enlightenment-Updates vorhanden sind, werden Microsoft Edge-Installationen blockiert, es sei denn, *Microsoft Edge Seite-an-Seite-Browserumgebung zulassen* ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="105c1-178">If Enlightenment Updates aren't present, Microsoft Edge installations will be blocked unless *Allow Microsoft Edge Side by Side browser experience* is enabled.</span></span>

   - <span data-ttu-id="105c1-179">Für Windows-Versionen 1903 und 1909: Wenn Ihre letzte Aktualisierung vor Oktober 2019 war, tritt möglicherweise dieses Problem auf.</span><span class="sxs-lookup"><span data-stu-id="105c1-179">For Windows versions 1903 and 1909: If your last update was before October 2019, you may have this issue.</span></span>
   - <span data-ttu-id="105c1-180">Für Windows-Versionen 1709, 1803 und 1809: Wenn Ihre letzte Aktualisierung vor November 2019 war, tritt möglicherweise dieses Problem auf.</span><span class="sxs-lookup"><span data-stu-id="105c1-180">For Windows versions 1709, 1803, and 1809: If your last update was before November 2019, you may have this issue.</span></span><br>
<span data-ttu-id="105c1-181">Weitere Informationen finden Sie unter [Windows-Updates zur Unterstützung der nächsten Version von Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-sysupdate-windows-updates).</span><span class="sxs-lookup"><span data-stu-id="105c1-181">For more information, see [Windows updates to support the next version of Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-sysupdate-windows-updates)</span></span>

#### <span data-ttu-id="105c1-182">Die folgende Fehlermeldung wurde angezeigt, nachdem Sie die Eingabeaufforderung verwendet haben und das Rollback nicht ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="105c1-182">The following error message was shown after using the Command Prompt and rollback didn't occur.</span></span> <span data-ttu-id="105c1-183">Was ist los?</span><span class="sxs-lookup"><span data-stu-id="105c1-183">What's wrong?</span></span>

![Rollback-Statusmeldung](./media/edge-learnmore-rollback/edge-rollback-cmd-flag-error.png)

<span data-ttu-id="105c1-185">*ALLOWDOWNGRADE=1* wurde nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="105c1-185">*ALLOWDOWNGRADE=1* was not executed.</span></span>

### <span data-ttu-id="105c1-186">Rollback von Microsoft Edge Update und Gruppenrichtlinien</span><span class="sxs-lookup"><span data-stu-id="105c1-186">Microsoft Edge Update and Group Policy rollback</span></span>

#### <span data-ttu-id="105c1-187">Ich habe *Zurücksetzen auf Zielversion* festgelegt, *Außerkraftsetzung von Updaterichtlinien* aktiviert und die gewünschte Browserversion für *Zielversion außer Kraft setzen* angegeben, aber die Browserversion war nicht die erwartete.</span><span class="sxs-lookup"><span data-stu-id="105c1-187">I set *Rollback to target version*, enabled *Update policy override*, input my desired browser version for *Target version override*, but the browser version wasn't what I expected.</span></span> <span data-ttu-id="105c1-188">Was ist los?</span><span class="sxs-lookup"><span data-stu-id="105c1-188">What's wrong?</span></span>

<span data-ttu-id="105c1-189">Einige häufige Fehler, durch die das Rollback verhindert wird, sind:</span><span class="sxs-lookup"><span data-stu-id="105c1-189">Some common errors that prevent rollback are:</span></span>

- <span data-ttu-id="105c1-190">Wenn die Option zum Zurücksetzen auf Zielversion nicht festgelegt ist, wird das Rollback nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="105c1-190">If Rollback to target version isn't set, rollback will not be executed.</span></span>
- <span data-ttu-id="105c1-191">Bei der Einstellung für die Außerkraftsetzung der Zielversion liegt eines der folgenden Probleme vor:</span><span class="sxs-lookup"><span data-stu-id="105c1-191">There are one of the following issues with the target version override setting:</span></span>

  - <span data-ttu-id="105c1-192">Die Außerkraftsetzung der Zielversion ist auf eine nicht unterstützte Zielversion festgelegt.</span><span class="sxs-lookup"><span data-stu-id="105c1-192">Target version override is set to an unsupported target version.</span></span>
  - <span data-ttu-id="105c1-193">Die Außerkraftsetzung der Zielversion ist auf eine nicht vorhandene Zielversion festgelegt.</span><span class="sxs-lookup"><span data-stu-id="105c1-193">Target version override is set to a non-existent target version.</span></span>
  - <span data-ttu-id="105c1-194">Die Eingabe für die Außerkraftsetzung der Zielversion ist falsch formatiert.</span><span class="sxs-lookup"><span data-stu-id="105c1-194">Target version override input is incorrectly formatted.</span></span>

- <span data-ttu-id="105c1-195">Wenn die Außerkraftsetzung von Updaterichtlinien auf "Updates deaktiviert" festgelegt ist, akzeptiert Microsoft Edge Update keine Updates.</span><span class="sxs-lookup"><span data-stu-id="105c1-195">If Update policy override is set to "Updates disabled", Microsoft Edge Update won't accept any updates.</span></span> <span data-ttu-id="105c1-196">Dies führt dazu, dass das Rollback nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="105c1-196">This results in rollback not getting executed.</span></span>

### <span data-ttu-id="105c1-197">Ich habe alle Gruppenrichtlinien ordnungsgemäß festgelegt, aber das Rollback wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="105c1-197">I set all the group policies correctly, but rollback didn't execute.</span></span> <span data-ttu-id="105c1-198">Was ist passiert?</span><span class="sxs-lookup"><span data-stu-id="105c1-198">What happened?</span></span>

<span data-ttu-id="105c1-199">Microsoft Edge Update hat noch keine Suche nach Updates durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="105c1-199">Microsoft Edge Update hasn't run a check for updates yet.</span></span> <span data-ttu-id="105c1-200">Die automatische Updatefunktion sucht standardmäßig alle 10 Stunden nach Updates.</span><span class="sxs-lookup"><span data-stu-id="105c1-200">By default, auto-update checks for updates every 10 hours.</span></span> <span data-ttu-id="105c1-201">Sie können dieses Problem beheben, indem Sie das Abrufintervall für Microsoft Edge Update mithilfe der Gruppenrichtlinie für die Überschreibung des Überprüfungszeitraums für automatische Updates ändern.</span><span class="sxs-lookup"><span data-stu-id="105c1-201">You can fix this by changing Microsoft Edge Update's polling interval with the Auto-update check period override group policy.</span></span> <span data-ttu-id="105c1-202">Weitere Informationen hierzu finden Sie unter [AutoUpdateCheckPeriodMinutes-Richtlinie](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#autoupdatecheckperiodminutes).</span><span class="sxs-lookup"><span data-stu-id="105c1-202">For more information, see the [AutoUpdateCheckPeriodMinutes](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#autoupdatecheckperiodminutes) policy.</span></span>

### <span data-ttu-id="105c1-203">Als IT-Administrator habe ich alle Schritte für eine ordnungsgemäße Zurücksetzung befolgt.</span><span class="sxs-lookup"><span data-stu-id="105c1-203">As an IT admin, I followed all the steps for rollback correctly.</span></span> <span data-ttu-id="105c1-204">Das Rollback wurde nur für einen Teil meiner Benutzergruppe durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="105c1-204">Only a portion of my user group was rolled back.</span></span> <span data-ttu-id="105c1-205">Warum wurde es nicht auch für die anderen durchgeführt?</span><span class="sxs-lookup"><span data-stu-id="105c1-205">Why haven't the other users been rolled back yet?</span></span>

<span data-ttu-id="105c1-206">Die Gruppenrichtlinieneinstellung wurde noch nicht mit allen Clients synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="105c1-206">The group policy setting hasn't synced to all the clients yet.</span></span> <span data-ttu-id="105c1-207">Wenn Administratoren eine Gruppenrichtlinie festlegen, werden die entsprechenden Einstellungen nicht sofort von den Clients empfangen.</span><span class="sxs-lookup"><span data-stu-id="105c1-207">When admins set a group policy, clients don't receive these settings instantaneously.</span></span>

<!--
You can update all users' group policy with the  

When admins set all users don't get this setting instantaneously 

GP Update force group policy – link to this 

-->





## <span data-ttu-id="105c1-208">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="105c1-208">See also</span></span>

- [<span data-ttu-id="105c1-209">Microsoft Edge Enterprise-Angebotsseite</span><span class="sxs-lookup"><span data-stu-id="105c1-209">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
