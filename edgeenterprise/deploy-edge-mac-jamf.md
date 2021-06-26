---
title: Automatisieren von Microsoft Edge für die macOS-Bereitstellung mit Jamf
ms.author: kvice
author: dan-wesley
manager: laurawi
ms.date: 11/30/2019
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: So automatisieren Sie Microsoft Edge für die macOS-Bereitstellung mit Jamf.
ms.openlocfilehash: e56ed4c2a9c0ebb4a4341830cd09ca040e80a657
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2021
ms.locfileid: "11617525"
---
# <a name="deploy-to-macos-with-jamf"></a><span data-ttu-id="3cf1d-103">Bereitstellen unter macOS mit JAMF</span><span class="sxs-lookup"><span data-stu-id="3cf1d-103">Deploy to macOS with Jamf</span></span>

<span data-ttu-id="3cf1d-104">In diesem Artikel wird beschrieben, wie Microsoft Edge für macOS mithilfe von Jamf bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="3cf1d-104">This article describes how to deploy Microsoft Edge for macOS using Jamf.</span></span>

> [!NOTE]
> <span data-ttu-id="3cf1d-105">Dieser Artikel bezieht sich auf Microsoft Edge Version 77 oder höher.</span><span class="sxs-lookup"><span data-stu-id="3cf1d-105">This article applies to Microsoft Edge version 77 or later.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3cf1d-106">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="3cf1d-106">Prerequisites</span></span>

<span data-ttu-id="3cf1d-107">Stellen Sie vor der Bereitstellung von Microsoft Edge sicher, dass die folgenden Voraussetzungen erfüllt sind:</span><span class="sxs-lookup"><span data-stu-id="3cf1d-107">Before you deploy Microsoft Edge, make sure you meet the following prerequisites:</span></span>

- <span data-ttu-id="3cf1d-108">Die Microsoft Edge-Installationsdatei **MicrosoftEdgeDev-\<version\>.pkg** befindet sich an einem zugänglichen Speicherort in Ihrem Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="3cf1d-108">The Microsoft Edge installation file,  **MicrosoftEdgeDev-\<version\>.pkg** is in an accessible location on your network.</span></span> <span data-ttu-id="3cf1d-109">Sie können die Installationsdateien für Microsoft Edge Enterprise von der [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise) herunterladen.</span><span class="sxs-lookup"><span data-stu-id="3cf1d-109">You can download the Microsoft Edge Enterprise installation files from the [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise).</span></span>
- <span data-ttu-id="3cf1d-110">Sie verfügen über ein JAMF-Cloud-Konto mit der Zugriffsebene und den erforderlichen Berechtigungen zum Erstellen und Bereitstellen von Installationsdateien auf Computern.</span><span class="sxs-lookup"><span data-stu-id="3cf1d-110">You have a Jamf Cloud account with the level of access and privileges needed to create and deploy installation files to computers.</span></span>

## <a name="to-deploy-microsoft-edge-using-jamf"></a><span data-ttu-id="3cf1d-111">So stellen Sie Microsoft Edge mithilfe von Jamf bereit:</span><span class="sxs-lookup"><span data-stu-id="3cf1d-111">To deploy Microsoft Edge using Jamf:</span></span>

1. <span data-ttu-id="3cf1d-112">Melden Sie sich bei Jamf an und wechseln Sie zu **Alle Einstellungen**.</span><span class="sxs-lookup"><span data-stu-id="3cf1d-112">Sign on to Jamf and go to **All Settings**.</span></span>

    ![Alle Einstellungen öffnen](./media/mac-deploy/jamf-dash-main-open-settings.png)

2. <span data-ttu-id="3cf1d-114">Klicken Sie unter **Alle Einstellungen** auf **Computerverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="3cf1d-114">Under **All Settings**, click **Computer Management**.</span></span>

    ![Computerverwaltung auswählen](./media/mac-deploy/jamf-all-settings-computer-mgmt.png)

3. <span data-ttu-id="3cf1d-116">Klicken Sie unter **Computerverwaltung** auf **Pakete**.</span><span class="sxs-lookup"><span data-stu-id="3cf1d-116">Under **Computer Management**, click **Packages**.</span></span>

    ![Pakete auswählen](./media/mac-deploy/jamf-all-settings-computer-mgmt-pkgs.png)

4. <span data-ttu-id="3cf1d-118">Klicken Sie auf der Seite **Pakete** auf **+ Neu**, um ein neues Paket hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="3cf1d-118">On the **Packages** page, click **+ New** to add a new package.</span></span>

    ![„Neu” auswählen, um ein neues Paket hinzufügen](./media/mac-deploy/jamf-all-settings-computer-mgmt-new-pkg.png)

5. <span data-ttu-id="3cf1d-120">Geben Sie auf der Seite **Neues Paket** die Details zum Paket ein und klicken Sie dann auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="3cf1d-120">On the **New Package** page, enter the details about the package and then click **Save**.</span></span> <span data-ttu-id="3cf1d-121">(Z. B. ANZEIGENAME, INFO oder NOTIZEN.)</span><span class="sxs-lookup"><span data-stu-id="3cf1d-121">(For example, DISPLAY NAME, INFO, or NOTES.)</span></span>

    ![„Speichern” auswählen, um die Paketinformationen zu speichern](./media/mac-deploy/jamf-all-settings-computer-mgmt-save-pkg-info.png)

6. <span data-ttu-id="3cf1d-123">Wählen Sie in der Menüleiste **Computer** aus, und wählen Sie dann in der Navigationsleiste **Richtlinien** aus.</span><span class="sxs-lookup"><span data-stu-id="3cf1d-123">Select **Computers** on the menu bar, and then select **Policies** in the navigation bar.</span></span>

7. <span data-ttu-id="3cf1d-124">Wählen Sie **+ Neu** aus, um den Bereich **Neue Richtlinie** anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="3cf1d-124">Select **+ New** to display the **New Policy** pane.</span></span>

    ![„Neu” auswählen, um eine neue Richtlinie zu erstellen](./media/mac-deploy/jamf-all-settings-computer-new-policy.png)

8. <span data-ttu-id="3cf1d-126">Wählen Sie auf der Registerkarte **Optionen** **Allgemein** aus.</span><span class="sxs-lookup"><span data-stu-id="3cf1d-126">On the **Options** tab, select **General**.</span></span>

    - <span data-ttu-id="3cf1d-127">Geben Sie unter **ANZEIGENAME** den Anzeigenamen für die Richtlinie ein.</span><span class="sxs-lookup"><span data-stu-id="3cf1d-127">Under **DISPLAY NAME**, enter the display name for the policy.</span></span>
    - <span data-ttu-id="3cf1d-128">Wählen Sie unter **Auslöser** das Ereignis aus, mit dem die Richtlinie ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="3cf1d-128">Under **Trigger**, select the event that will trigger the policy.</span></span> <span data-ttu-id="3cf1d-129">(Im Folgenden Beispiel ist das Ereignis das Starten.)</span><span class="sxs-lookup"><span data-stu-id="3cf1d-129">(In the following example, the event is Startup.)</span></span>

    ![Informationen zur Bereitstellung eingeben](./media/mac-deploy/jamf-all-settings-computer-cfg-policy.png)

9. <span data-ttu-id="3cf1d-131">Klicken Sie auf der Registerkarte **Optionen** auf **Pakete**.</span><span class="sxs-lookup"><span data-stu-id="3cf1d-131">On the **Options** tab, click **Packages**.</span></span>

10. <span data-ttu-id="3cf1d-132">Klicken Sie im Popup **Pakete konfigurieren** auf **Konfigurieren**.</span><span class="sxs-lookup"><span data-stu-id="3cf1d-132">On the **Configure Packages** popup, click **Configure**.</span></span>

    ![Paket konfigurieren](./media/mac-deploy/jamf-all-settings-computer-policy-pkg-configure.png)

11. <span data-ttu-id="3cf1d-134">Das Paket, das Sie hinzugefügt haben, wird im Bereich **Pakete** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3cf1d-134">The package that you added shows on the **Packages** pane.</span></span> <span data-ttu-id="3cf1d-135">Klicken Sie auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="3cf1d-135">Click **Add**.</span></span> <span data-ttu-id="3cf1d-136">In diesem Beispiel lautet der Name des Pakets im folgenden Screenshot „MicrosoftEdgeBeta”.</span><span class="sxs-lookup"><span data-stu-id="3cf1d-136">For this example, the package is "MicrosoftEdgeBeta" in the following screenshot.</span></span>

    ![Paket hinzufügen](./media/mac-deploy/jamf-all-settings-computer-policy-pkg-add-beta.png)

12. <span data-ttu-id="3cf1d-138">Verwenden Sie auf der Seite **Neue Richtlinie** die Dropdown-Listen, um den **VERTEILUNGSPUNKT** und die **AKTION** für die Richtlinie auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="3cf1d-138">On the **New Policy** page, uUse the drop-down lists to select the **DISTRIBUTION POINT** and **ACTION** to take for the policy.</span></span> <span data-ttu-id="3cf1d-139">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="3cf1d-139">Click **Save**.</span></span> <span data-ttu-id="3cf1d-140">Im folgenden Screenshot wird als Beispiel „Der Standardverteilungspunkt für jeden Computer” und „Installieren” verwendet.</span><span class="sxs-lookup"><span data-stu-id="3cf1d-140">The following screenshot uses "Each computer's default distribution point" and "Install" as an example.</span></span>

    ![Verteilungspunkt und Aktion auswählen](./media/mac-deploy/jamf-all-settings-computer-mgmt-pkg-cfg-distro.png)

13. <span data-ttu-id="3cf1d-142">Wählen Sie auf der Seite **Neue Richtlinie** die Registerkarte **Bereich** aus. Sie können den Umfang der Bereitstellung auf der Grundlage von Computern oder Benutzern verwalten.</span><span class="sxs-lookup"><span data-stu-id="3cf1d-142">On the **New Policy** page, select the **Scope** tab. You can manage the scope of the deployment based on computers or users.</span></span> <span data-ttu-id="3cf1d-143">Wählen Sie in diesem Beispiel **Alle Computer** in der Dropdown-Liste **ZIELCOMPUTER** aus, und klicken Sie dann auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="3cf1d-143">For this example, select **All Computers** from the **TARGET COMPUTERS** drop-down list and then click **Save**.</span></span>

    ![Den Bereich der Bereitstellung auswählen](./media/mac-deploy/jamf-all-settings-computer-mgmt-add-target.png)

14. <span data-ttu-id="3cf1d-145">An dieser Stelle können Sie die Microsoft Edge-Bereitstellungsrichtlinie überprüfen.</span><span class="sxs-lookup"><span data-stu-id="3cf1d-145">At this point you can review the Microsoft Edge deployment policy.</span></span> <span data-ttu-id="3cf1d-146">Wenn die Bereitstellungsoptionen Ihren Anforderungen entsprechen, klicken Sie auf **Fertig**.</span><span class="sxs-lookup"><span data-stu-id="3cf1d-146">If the deployment options meet your requirements, click **Done**.</span></span>

    ![Klicken Sie auf Fertig.](./media/mac-deploy/jamf-all-settings-computer-mgmt-finish-add-deployment.png)

    > [!NOTE]
    > <span data-ttu-id="3cf1d-148">Sie können jederzeit zu einer Bereitstellungsrichtlinie wechseln, um die Einstellungen zu ändern.</span><span class="sxs-lookup"><span data-stu-id="3cf1d-148">You can return to a deployment policy at any time to change settings.</span></span>

<span data-ttu-id="3cf1d-149">Herzlichen Glückwunsch!</span><span class="sxs-lookup"><span data-stu-id="3cf1d-149">Congratulations!</span></span> <span data-ttu-id="3cf1d-150">Sie haben soeben die Konfiguration von Jamf für die Bereitstellung von Microsoft Edge für macOS abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="3cf1d-150">You’ve just finished configuring Jamf to deploy Microsoft Edge for macOS.</span></span> <span data-ttu-id="3cf1d-151">Wenn die von Ihnen definierte auslösende Bedingung „true” ist, wird das Paket auf den von Ihnen angegebenen Computern bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="3cf1d-151">When the trigger condition you defined is true, the package will get deployed to the computers you specified.</span></span>

## <a name="see-also"></a><span data-ttu-id="3cf1d-152">Weitere Informationen:</span><span class="sxs-lookup"><span data-stu-id="3cf1d-152">See also</span></span>

- [<span data-ttu-id="3cf1d-153">Microsoft Edge Enterprise-Angebotsseite</span><span class="sxs-lookup"><span data-stu-id="3cf1d-153">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="3cf1d-154">Jamf.com</span><span class="sxs-lookup"><span data-stu-id="3cf1d-154">Jamf.com</span></span>](https://www.jamf.com/)
- [<span data-ttu-id="3cf1d-155">Jamf in Microsoft Intune integrieren</span><span class="sxs-lookup"><span data-stu-id="3cf1d-155">Integrate Jamf with Microsoft Intune</span></span>](/intune/conditional-access-integrate-jamf)