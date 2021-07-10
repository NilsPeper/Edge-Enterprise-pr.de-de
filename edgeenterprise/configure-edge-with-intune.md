---
title: Konfigurieren der Microsoft Edge-Richtlinieneinstellungen für Windows mit Microsoft Intune
ms.author: kvice
author: kelleyvice-msft
manager: laurawi
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Konfigurieren Sie die Microsoft Edge-Richtlinieneinstellungen für Windows mit Microsoft Intune.
ms.openlocfilehash: adcd80f68250a9694b9bbaa21fb7941ebcbaf15a
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "11641671"
---
# <a name="configure-microsoft-edge-policy-settings-with-microsoft-intune"></a><span data-ttu-id="fc291-103">Konfigurieren der Microsoft Edge-Richtlinieneinstellungen mit Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="fc291-103">Configure Microsoft Edge policy settings with Microsoft Intune</span></span>

<span data-ttu-id="fc291-104">In diesem Artikel wird erläutert, wie Sie Microsoft Edge Richtlinieneinstellungen für Windows 10 mit Microsoft Intune konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="fc291-104">This article explains how to configure Microsoft Edge policy settings for Windows 10 using Microsoft Intune.</span></span>

> [!NOTE]
> <span data-ttu-id="fc291-105">Dieser Artikel bezieht sich auf Microsoft Edge Version 77 oder höher.</span><span class="sxs-lookup"><span data-stu-id="fc291-105">This article applies to Microsoft Edge version 77 or later.</span></span>

<span data-ttu-id="fc291-106">Sie können Microsoft Edge-Richtlinien und -Einstellungen durch Hinzufügen eines Gerätekonfigurationsprofils in Microsoft Intune konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="fc291-106">You can configure Microsoft Edge policies and settings by adding a device configuration profile to Microsoft Intune.</span></span> <span data-ttu-id="fc291-107">Die Verwendung von Intune zum Verwalten und Erzwingen von Richtlinien entspricht der Verwendung von Active Directory-Gruppenrichtlinien oder der Konfiguration lokaler Gruppenrichtlinienobjekteinstellungen auf Benutzergeräten.</span><span class="sxs-lookup"><span data-stu-id="fc291-107">Using Intune to manage and enforce policies is equivalent to using Active Directory Group Policy or configuring local Group Policy Object (GPO) settings on user devices.</span></span>

<span data-ttu-id="fc291-108">Weitere Informationen zum Verwalten von Microsoft Edge-Richtlinien mit Microsoft Intune finden Sie unter [Verwalten des Webzugriffs mithilfe von Microsoft Edge mit Microsoft Intune](/intune/manage-microsoft-edge). Beachten Sie jedoch, dass der verknüpfte Artikel für Microsoft Edge Version 45 und früher spezifisch ist und daher möglicherweise Informationen und Verweise enthält, die nicht für Microsoft Edge Enterprise Version 77 und höher gelten.</span><span class="sxs-lookup"><span data-stu-id="fc291-108">For more information about managing Microsoft Edge policies with Microsoft Intune, you can read [Manage web access by using Microsoft Edge with Microsoft Intune](/intune/manage-microsoft-edge), but keep in mind that the linked article is specific to Microsoft Edge version 45 and earlier and therefore may contain information and references that don't apply to Microsoft Edge Enterprise version 77 and later.</span></span>

> [!TIP]
> <span data-ttu-id="fc291-109">Informationen zum Konfigurieren von Microsoft Edge auf macOS mithilfe von Microsoft Intune finden Sie unter [Konfigurieren für macOS](configure-microsoft-edge-on-mac.md).</span><span class="sxs-lookup"><span data-stu-id="fc291-109">For information on how to configure Microsoft Edge on macOS using Microsoft Intune, see [Configure for macOS](configure-microsoft-edge-on-mac.md).</span></span>

## <a name="create-a-profile-to-manage-settings-in-microsoft-edge-for-windows-10"></a><span data-ttu-id="fc291-110">Erstellen eines Profils zum Verwalten von Einstellungen in Microsoft Edge für Windows 10</span><span class="sxs-lookup"><span data-stu-id="fc291-110">Create a profile to manage settings in Microsoft Edge for Windows 10</span></span>

<span data-ttu-id="fc291-111">Mithilfe von administrativen Vorlagen in Microsoft Intune können Sie Microsoft Edge-Gruppenrichtlinien auf Ihren Windows 10-Geräten mithilfe der Cloud verwalten.</span><span class="sxs-lookup"><span data-stu-id="fc291-111">Using Administrative Templates in Microsoft Intune, you can manage Microsoft Edge group policies on your Windows 10 devices using the cloud.</span></span> <span data-ttu-id="fc291-112">Dieser Abschnitt unterstützt Sie beim Erstellen einer Vorlage zum Konfigurieren von Microsoft Edge-spezifischen Anwendungseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="fc291-112">This section will help you create a template to configure Microsoft Edge-specific application settings.</span></span> <span data-ttu-id="fc291-113">Wenn Sie die Vorlage erstellen, wird ein Gerätekonfigurationsprofil erstellt.</span><span class="sxs-lookup"><span data-stu-id="fc291-113">When you create the template, it creates a device configuration profile.</span></span> <span data-ttu-id="fc291-114">Sie können dieses Profil dann Windows 10-Geräten in Ihrer Organisation zuweisen oder auf diesen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="fc291-114">You can then assign or deploy this profile to Windows 10 devices in your organization.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="fc291-115">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="fc291-115">Prerequisites</span></span>

- <span data-ttu-id="fc291-116">Windows 10, mit den folgenden Mindestvoraussetzungen:</span><span class="sxs-lookup"><span data-stu-id="fc291-116">Windows 10 with the following minimum system requirements:</span></span>
  - <span data-ttu-id="fc291-117">Windows 10, Version 1909</span><span class="sxs-lookup"><span data-stu-id="fc291-117">Windows 10, version 1909</span></span>
  - <span data-ttu-id="fc291-118">Windows 10, Version 1903, mit Installation von [KB4512941](https://support.microsoft.com/kb/4512941)</span><span class="sxs-lookup"><span data-stu-id="fc291-118">Windows 10, version 1903 with [KB4512941](https://support.microsoft.com/kb/4512941) installed</span></span>
  - <span data-ttu-id="fc291-119">Windows 10, Version 1809, mit Installation von [KB4512534](https://support.microsoft.com/kb/4512534)</span><span class="sxs-lookup"><span data-stu-id="fc291-119">Windows 10, version 1809 with [KB4512534](https://support.microsoft.com/kb/4512534) installed</span></span>
  - <span data-ttu-id="fc291-120">Windows 10, Version 1803, mit Installation von [KB4512509](https://support.microsoft.com/kb/4512509)</span><span class="sxs-lookup"><span data-stu-id="fc291-120">Windows 10, version 1803 with [KB4512509](https://support.microsoft.com/kb/4512509) installed</span></span>
  - <span data-ttu-id="fc291-121">Windows 10, Version 1709, mit Installation von [KB4516071](https://support.microsoft.com/kb/4516071)</span><span class="sxs-lookup"><span data-stu-id="fc291-121">Windows 10, version 1709 with [KB4516071](https://support.microsoft.com/kb/4516071) installed</span></span>

### <a name="use-administrative-templates-to-create-a-policy-for-microsoft-edge"></a><span data-ttu-id="fc291-122">Verwenden von Administrativen Vorlagen zur Erstellung einer Richtlinie für Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="fc291-122">Use Administrative Templates to create a policy for Microsoft Edge</span></span>

<span data-ttu-id="fc291-123">Dieses Verfahren nutzt administrative Vorlagen (die Sie möglicherweise aus der Gruppenrichtlinie kennen), die in Intune integriert sind.</span><span class="sxs-lookup"><span data-stu-id="fc291-123">This procedure leverages Administrative templates (which you might be familiar with from Group Policy) that are built into Intune.</span></span> <span data-ttu-id="fc291-124">Sie können diese Vorlagen zur Erstellung einer Richtlinie für Microsoft Edge verwenden, indem Sie Einstellungen aus einer vorkonfigurierten Liste auswählen.</span><span class="sxs-lookup"><span data-stu-id="fc291-124">You can use these templates to create a policy for Microsoft Edge by selecting settings from a pre-configured list.</span></span>

1. <span data-ttu-id="fc291-125">Melden Sie sich beim [Microsoft Endpoint Manager](https://endpoint.microsoft.com/)-Portal an.</span><span class="sxs-lookup"><span data-stu-id="fc291-125">Sign in to the [Microsoft Endpoint Manager](https://endpoint.microsoft.com/) portal.</span></span>
2. <span data-ttu-id="fc291-126">Wählen Sie im linken Navigationsbereich **Geräte** aus.</span><span class="sxs-lookup"><span data-stu-id="fc291-126">Select **Devices** in the left-hand navigation pane.</span></span>
3. <span data-ttu-id="fc291-127">Wählen Sie nach**Geräte** | **Übersicht** aus, und gehen Sie dann auf **Konfigurationsprofile** (unter der Überschrift Richtlinien) aus.</span><span class="sxs-lookup"><span data-stu-id="fc291-127">From **Devices** | **Overview**, select **Configuration Profiles** (under Policy heading).</span></span>
4. <span data-ttu-id="fc291-128">Wählen Sie in der oberen Befehlsleiste **Profil erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="fc291-128">On the top command bar, select **Create profile**.</span></span>
5. <span data-ttu-id="fc291-129">Wählen Sie in der Dropdownliste unterhalb **Plattform\*\*\*\*Windows 10 und höher**aus.</span><span class="sxs-lookup"><span data-stu-id="fc291-129">In the drop-down list below **Platform**, select **Windows 10 and later**.</span></span>
6. <span data-ttu-id="fc291-130">Wählen Sie in der Dropdownliste unterhalb **Profil\*\*\*\*Administrative Vorlagen** aus, und klicken Sie dann auf die Schaltfläche **Erstellen**.</span><span class="sxs-lookup"><span data-stu-id="fc291-130">In the drop-down list below **Profile**, select **Administrative Templates** and then click the **Create** button.</span></span> <span data-ttu-id="fc291-131">Der nächste Screenshot zeigt die Dropdownlisten, in denen Plattform und Art des Profil ausgewählt werden können.</span><span class="sxs-lookup"><span data-stu-id="fc291-131">The next screenshot shows the drop-down lists to select the platform and type of profile.</span></span>

    ![Wählen Sie die Plattform und Art des Profils aus](./media/configure-edge-with-intune/create-profile-platform.png)

7. <span data-ttu-id="fc291-133">Geben Sie auf der Registerkarte **Grundlagen** einen**Namen** zur Beschreibung ein, z. b. die Microsoft-Edge-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="fc291-133">On the **Basics** tab, enter a descriptive **Name**, such as Microsoft Edge Policy.</span></span> <span data-ttu-id="fc291-134">Ooptional können Sie eine  **Beschreibung** der Richtlinie eingeben.</span><span class="sxs-lookup"><span data-stu-id="fc291-134">Optionally, enter a  **Description** for the policy.</span></span>
<span data-ttu-id="fc291-135">Der nächste Screenshot zeigt das Format für die Registerkarte **Grundlagen** an. Die Menüleiste zeigt die nächsten Schritte (als abgeblendete Registerkarten) zur Erstellung des Profils an.</span><span class="sxs-lookup"><span data-stu-id="fc291-135">The next screenshot shows the form for the **Basics** tab and the menu bar shows the next steps (as grayed out tabs) to create the profile.</span></span>

   ![Geben Sie einen Namen und eine Beschreibung ein](./media/configure-edge-with-intune/create-profile-basics-tab.png)

8. <span data-ttu-id="fc291-137">Wählen Sie **Weiter** aus.</span><span class="sxs-lookup"><span data-stu-id="fc291-137">Select **Next**.</span></span>
9. <span data-ttu-id="fc291-138">Wählen Sie auf der Registerkarte **Konfigurationseinstellungen** den Ordner Microsoft Edge an einen der folgenden Speicherorte aus:</span><span class="sxs-lookup"><span data-stu-id="fc291-138">On the **Configuration settings** tab, select the Microsoft Edge folder in one of the following locations:</span></span>

   - <span data-ttu-id="fc291-139">unter dem Ordner Computerkonfiguration</span><span class="sxs-lookup"><span data-stu-id="fc291-139">below the Computer Configuration folder</span></span>
   - <span data-ttu-id="fc291-140">unter dem Ordner Benutzerkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="fc291-140">below the User Configuration folder.</span></span>

   <span data-ttu-id="fc291-141">Die verfügbaren Einstellungen für Microsoft Edge werden im rechten Bereich angezeigt.</span><span class="sxs-lookup"><span data-stu-id="fc291-141">The available settings for Microsoft Edge will be shown on the right pane.</span></span> <span data-ttu-id="fc291-142">Beispielsweise *Computerkonfiguration/Microsoft Edge/Downloadbeschränkungen zulassen*, welche im folgenden Screenshot gezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="fc291-142">For example, *Computer Configuration/Microsoft Edge/Allow download restrictions* shown in the following screenshot.</span></span>

   ![Registerkarte Konfigurationseinstellungen](./media/configure-edge-with-intune/create-profile-configuration-settings-tab.png)

   > [!NOTE]
   > <span data-ttu-id="fc291-144">Die vollständigste und aktuellste Liste aller verfügbaren Einstellungen für Microsoft Edge finden Sie unter [Microsoft Edge – Richtlinien](./microsoft-edge-policies.md) und [Microsoft Edge – Updaterichtlinien](./microsoft-edge-update-policies.md).</span><span class="sxs-lookup"><span data-stu-id="fc291-144">See [Microsoft Edge – Policies](./microsoft-edge-policies.md) and [Microsoft Edge – Update policies](./microsoft-edge-update-policies.md) for the most complete and up to date list of all the available settings for Microsoft Edge.</span></span>

10. <span data-ttu-id="fc291-145">Verwenden Sie das Suchfeld („Filtern von Elementen...“), um eine bestimmte Einstellung zu finden, die Sie konfigurieren möchten.</span><span class="sxs-lookup"><span data-stu-id="fc291-145">Use the search field ("Search to filter items ...") to find a specific setting you want to configure.</span></span> <span data-ttu-id="fc291-146">In diesem Beispiel lautet der Suchtext „Homepage“.</span><span class="sxs-lookup"><span data-stu-id="fc291-146">In this example, the search string is "home page".</span></span> <span data-ttu-id="fc291-147">Der nächste Screenshot zeigt die Suchergebnisse an.</span><span class="sxs-lookup"><span data-stu-id="fc291-147">The next screenshot shows the search results.</span></span>

    ![Suchergebnisse](./media/configure-edge-with-intune/create-profile-configuration-settings-tab-search.png)

11. <span data-ttu-id="fc291-149">Nachdem Sie die Einstellung gefunden haben, die Sie konfigurieren möchten, wählen Sie diese aus, und lassen Sie sich so die konfigurierbaren Werte anzeigen.</span><span class="sxs-lookup"><span data-stu-id="fc291-149">After you find the setting you intend to configure, select it to expose the values you can set.</span></span> <span data-ttu-id="fc291-150">Im nächsten Screenshot wird als Beispiel „Startseiten-URL konfigurieren“ ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="fc291-150">In the next screenshot, we selected "Configure the home page URL" as an example.</span></span>

    ![Konfigurieren der Richtlinie zur Startseiten-URL](./media/configure-edge-with-intune/create-profile-configuration-settings-tab-edit-pol.png)

12. <span data-ttu-id="fc291-152">Aktivieren Sie die Richtlinie, und geben Sie einen Wert für die Startseiten-URL ein, wie im vorherigen Screenshot gezeigt.</span><span class="sxs-lookup"><span data-stu-id="fc291-152">Enable the policy and enter a value for the Home page URL, as shown in the previous screenshot.</span></span>

13. <span data-ttu-id="fc291-153">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="fc291-153">Click **OK**.</span></span> <span data-ttu-id="fc291-154">Die Spalte „Status“ muss in den Einstellungen als „Aktiviert“ angezeigt werden, wie im folgenden Screenshot dargestellt.</span><span class="sxs-lookup"><span data-stu-id="fc291-154">The settings "State" column should appear as "Enabled", as shown in the following screenshot example.</span></span>

    ![Die Einstellung „Status“ ist aktiviert](./media/configure-edge-with-intune/create-profile-configuration-settings-tab-set-enabled.png)

14. <span data-ttu-id="fc291-156">Klicken Sie auf die Schaltfläche **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="fc291-156">Click the **Next** button.</span></span>

15. <span data-ttu-id="fc291-157">Fügen Sie auf der Registerkarte **Bereichsmarkierung** falls gewünscht eine Bereichsmarkierung hinzu. Andernfalls klicken Sie auf die Schaltfläche **Nächste**.</span><span class="sxs-lookup"><span data-stu-id="fc291-157">On the **Scope tags** tab, add a Scope tag if wanted, otherwise click the **Next** button.</span></span>

16. <span data-ttu-id="fc291-158">Klicken Sie auf der Registerkarte **Zuweisungen** auf **+ wählen Sie Gruppen aus, die einbezogen werden sollen**, um diese Richtlinie der Azure Active Directory-Gruppe (Azure Active Directory) zuzuweisen, welche die Geräte oder die Benutzer enthält, für die Sie diese Richtlinieneinstellung erhalten möchten.</span><span class="sxs-lookup"><span data-stu-id="fc291-158">On the **Assignments** tab, click **+ Select groups to include** to assign this policy to the Azure Active Directory (Azure AD) group that contains the devices or the users that you want to receive this policy setting.</span></span> <span data-ttu-id="fc291-159">Unter [Zuweisen von Benutzer- und Geräteprofilen in Microsoft Intune](/intune/device-profile-assign) finden Sie Informationen dazu, wie Sie das Profil Ihren Benutzer- oder Gerätegruppen in Azure AD zuweisen.</span><span class="sxs-lookup"><span data-stu-id="fc291-159">See [Assign user and device profiles in Microsoft Intune](/intune/device-profile-assign) for information about how to assign the profile to your Azure AD user or device groups.</span></span>

    ![Wählen Sie die Gruppen, die einbezogen werden sollen](./media/configure-edge-with-intune/create-profile-assignments-tab.png)

17. <span data-ttu-id="fc291-161">Klicken Sie auf die Schaltfläche **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="fc291-161">Click the **Next** button.</span></span>

18. <span data-ttu-id="fc291-162">Überprüfen Sie auf der Registerkarte **Überprüfen + erstellen** die Zusammenfassung Ihrer Änderungen, um sicherzustellen, dass sie korrekt sind, und klicken Sie dann auf die Schaltfläche **Erstellen**.</span><span class="sxs-lookup"><span data-stu-id="fc291-162">On the **Review + create** tab, review the summary of your changes to ensure it's correct and then click the **Create** button.</span></span>

19. <span data-ttu-id="fc291-163">Die neu erstellte Richtlinie (Microsoft Edge-Richtlinie) wird im folgenden Screenshot gezeigt.</span><span class="sxs-lookup"><span data-stu-id="fc291-163">The newly created policy (Microsoft Edge Policy) is shown in the following screenshot.</span></span>

    ![Wählen Sie die Gruppen, die einbezogen werden sollen](./media/configure-edge-with-intune/create-profile-new-policy-finished.png)

<span data-ttu-id="fc291-165">Weitere Informationen zu Windows 10-Profilen finden Sie unter [Verwenden von Windows 10-Vorlagen zum Konfigurieren von Gruppenrichtlinieneinstellungen in Microsoft Intune](/intune/administrative-templates-windows).</span><span class="sxs-lookup"><span data-stu-id="fc291-165">For more information about Windows 10 profiles, see [Use Windows 10 templates to configure group policy settings in Microsoft Intune](/intune/administrative-templates-windows).</span></span>

## <a name="see-also"></a><span data-ttu-id="fc291-166">Weitere Informationen:</span><span class="sxs-lookup"><span data-stu-id="fc291-166">See also</span></span>

- [<span data-ttu-id="fc291-167">Microsoft Edge Enterprise-Angebotsseite</span><span class="sxs-lookup"><span data-stu-id="fc291-167">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="fc291-168">Verwalten von Webzugriffen mithilfe von Microsoft Edge mit Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="fc291-168">Manage web access by using Microsoft Edge with Microsoft Intune</span></span>](/intune/manage-microsoft-edge)
- [<span data-ttu-id="fc291-169">Verwenden Sie Windows 10-Vorlagen zum Konfigurieren von Gruppenrichtlinieneinstellungen in Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="fc291-169">Use Windows 10 templates to configure group policy settings in Microsoft Intune</span></span>](/intune/administrative-templates-windows)
- [<span data-ttu-id="fc291-170">Bereitstellen von Microsoft Edge mit Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="fc291-170">Deploy Microsoft Edge using Microsoft Intune</span></span>](/intune/apps/apps-windows-edge/?bc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2ftoc.json)