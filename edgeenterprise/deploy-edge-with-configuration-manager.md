---
title: Bereitstellen von Microsoft Edge mithilfe vom System Center Konfigurations-Manager
ms.author: kvice
author: kelleyvice-msft
manager: laurawi
ms.date: 06/08/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Erfahren Sie hier, wie Sie Microsoft Edge mithilfe vom System Center Konfigurations-Manager (SCCM) bereitstellen können.
ms.openlocfilehash: b403c8924a0f970aaadff2e1b20ebd05c0641a96
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2021
ms.locfileid: "11617545"
---
# <a name="deploy-microsoft-edge-using-system-center-configuration-manager"></a><span data-ttu-id="2ee89-103">Bereitstellen von Microsoft Edge mithilfe vom System Center Konfigurations-Manager</span><span class="sxs-lookup"><span data-stu-id="2ee89-103">Deploy Microsoft Edge using System Center Configuration Manager</span></span>

<span data-ttu-id="2ee89-104">In diesem Artikel erfahren Sie, wie Sie eine Microsoft Edge-Bereitstellung mithilfe vom System Center Konfigurations-Manager (SCCM) automatisieren.</span><span class="sxs-lookup"><span data-stu-id="2ee89-104">This article shows you how to automate a Microsoft Edge deployment by using System Center Configuration Manager (SCCM).</span></span>

>[!NOTE]
><span data-ttu-id="2ee89-105">Dieser Artikel bezieht sich auf Microsoft Edge Version 77 oder höher.</span><span class="sxs-lookup"><span data-stu-id="2ee89-105">This article applies to Microsoft Edge version 77 or later.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="2ee89-106">Vorbemerkungen</span><span class="sxs-lookup"><span data-stu-id="2ee89-106">Before you begin</span></span>

<span data-ttu-id="2ee89-107">Lesen Sie die Informationen im Artikel [Einführung in die Anwendungsverwaltung im Konfigurations-Manager](/sccm/apps/understand/introduction-to-application-management).</span><span class="sxs-lookup"><span data-stu-id="2ee89-107">Review the information in [Introduction to application management in Configuration Manager](/sccm/apps/understand/introduction-to-application-management).</span></span> <span data-ttu-id="2ee89-108">Dieser Artikel zur Anwendungsverwaltung hilft Ihnen, die in diesem Artikel verwendete Terminologie zu verstehen und ist ein Leitfaden für die Vorbereitung Ihrer Website für die Installation von Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="2ee89-108">This application management article will help you understand the terminology used in this article and is a guide to preparing your site to install applications.</span></span>

<span data-ttu-id="2ee89-109">Laden Sie die Microsoft Edge Enterprise-Installationsdateien (**MicrosoftEdgeDevEnterpriseX64.msi** und/oder **MicrosoftEdgeDevEnterpriseX86.msi**) von der [Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)-Angebotsseite herunter.</span><span class="sxs-lookup"><span data-stu-id="2ee89-109">Download the Microsoft Edge Enterprise installation files (**MicrosoftEdgeDevEnterpriseX64.msi** and/or **MicrosoftEdgeDevEnterpriseX86.msi**) from the [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise).</span></span>

<span data-ttu-id="2ee89-110">Stellen Sie sicher, dass Sie die Microsoft Edge-Installationsdateien an einem zugänglichen Netzwerkspeicherort speichern.</span><span class="sxs-lookup"><span data-stu-id="2ee89-110">Make sure you store the Microsoft Edge installation files in an accessible network location.</span></span>

## <a name="create-the-application"></a><span data-ttu-id="2ee89-111">Erstellen der Anwendung</span><span class="sxs-lookup"><span data-stu-id="2ee89-111">Create the application</span></span>

<span data-ttu-id="2ee89-112">Sie erstellen die Anwendung mithilfe eines Assistenten für Konfigurations-Manager.</span><span class="sxs-lookup"><span data-stu-id="2ee89-112">You'll create the application using a Configuration Manager wizard.</span></span>

### <a name="start-the-create-application-wizard-and-create-the-application"></a><span data-ttu-id="2ee89-113">Starten des Anwendungserstellungs-Assistenten und Erstellen der Anwendung</span><span class="sxs-lookup"><span data-stu-id="2ee89-113">Start the Create Application Wizard and create the application</span></span>  

1. <span data-ttu-id="2ee89-114">Klicken Sie in der Konfigurations-Manager-Konsole auf **Softwarebibliothek** > **Anwendungsverwaltung** > **Anwendungen**.</span><span class="sxs-lookup"><span data-stu-id="2ee89-114">In the Configuration Manager console, click **Software Library** > **Application Management** > **Applications**.</span></span>  

2. <span data-ttu-id="2ee89-115">Klicken Sie auf der Registerkarte **Start** in der Gruppe **Erstellen** auf **Anwendung erstellen**.</span><span class="sxs-lookup"><span data-stu-id="2ee89-115">On the **Home** tab, in the **Create** group, click **Create Application**.</span></span> <span data-ttu-id="2ee89-116">Alternativ klicken Sie in der Navigationsleiste mit der rechten Maustaste auf **Anwendungen** und anschließend auf **Anwendung erstellen**.</span><span class="sxs-lookup"><span data-stu-id="2ee89-116">Or, right-click on **Applications** in the navigation bar and then click **Create Application**.</span></span>

    ![Erstellen Ihrer ersten Anwendung](./media/edge-ent-deployment-sccm/edge-ent-create-app-1.png)

3. <span data-ttu-id="2ee89-118">Aktivieren Sie auf der Seite **Allgemein** des **Assistenten zum Erstellen von Anwendungen** das Kontrollkästchen **Informationen zu dieser Anwendung automatisch anhand der Installationsdateien erkennen**.</span><span class="sxs-lookup"><span data-stu-id="2ee89-118">On the **General** page of the **Create Application Wizard**, choose **Automatically detect information about this application from installation files**.</span></span> <span data-ttu-id="2ee89-119">Dadurch werden einige der Felder im Assistenten vorab mit Informationen gefüllt, die aus der Datei „install. msi” extrahiert wurden.</span><span class="sxs-lookup"><span data-stu-id="2ee89-119">This pre-populates some of the information in the wizard with information that's extracted from the installation .msi file.</span></span> <span data-ttu-id="2ee89-120">Geben Sie die folgenden Informationen an:</span><span class="sxs-lookup"><span data-stu-id="2ee89-120">Provide the following information:</span></span>  

   - <span data-ttu-id="2ee89-121">**Typ**: Wählen Sie **Windows Installer (\*.MSI-Datei)** aus.</span><span class="sxs-lookup"><span data-stu-id="2ee89-121">**Type**: Choose **Windows Installer (\*.msi file)**.</span></span>  

   - <span data-ttu-id="2ee89-122">**Speicherort**: Geben Sie den Speicherort ein (oder klicken Sie auf **Durchsuchen**), um den Speicherort der Installationsdatei **MicrosoftEdgeDevEnterpriseX64.msi** oder **MicrosoftEdgeDevEnterpriseX86.msi** auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="2ee89-122">**Location**: Type the location (or click **Browse** to select the location) of the installation file **MicrosoftEdgeDevEnterpriseX64.msi** or **MicrosoftEdgeDevEnterpriseX86.msi**.</span></span> <span data-ttu-id="2ee89-123">Beachten Sie, dass der Speicherort im Formular *\\\Server\Share\File* für Konfigurations-Manager angegeben werden muss, um nach der Installationsdateien zu suchen.</span><span class="sxs-lookup"><span data-stu-id="2ee89-123">Note that the location must be specified in the form *\\\Server\Share\File* for Configuration Manager to locate the installation files.</span></span>  

   <span data-ttu-id="2ee89-124">Die Seite **Einstellungen für diese Anwendung angeben** sieht wie im folgenden Beispiel aus:</span><span class="sxs-lookup"><span data-stu-id="2ee89-124">Your **Specify settings for this application** page will look like the following example:</span></span>  

    ![Einstellungen für diese Anwendung angeben](./media/edge-ent-deployment-sccm/edge-ent-create-app-2.png)

4. <span data-ttu-id="2ee89-126">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="2ee89-126">Click **Next**.</span></span> <span data-ttu-id="2ee89-127">Auf der Seite **Importierte Informationen** werden unter **Details** Informationen über die Anwendung und alle zugeordneten Dateien angezeigt, die importiert wurden.</span><span class="sxs-lookup"><span data-stu-id="2ee89-127">Under **Details** on the **Imported Information** page, you'll see information about the application and any associated files that were imported.</span></span> <span data-ttu-id="2ee89-128">Klicken Sie auf **Weiter** , um die Herstellung der drahtgebundenen Verbindung fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="2ee89-128">Click **Next** to continue with the wizard.</span></span>  

    ![Importierte Informationen anzeigen](./media/edge-ent-deployment-sccm/edge-ent-create-app-3.png)

5. <span data-ttu-id="2ee89-130">Auf der Seite **Allgemeine Informationen** können Sie weitere Informationen zur Anwendung hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="2ee89-130">On the **General Information** page, you can add more information about the application.</span></span> <span data-ttu-id="2ee89-131">Zum Beispiel Softwareversion, Administratorkommentare und Herausgeber.</span><span class="sxs-lookup"><span data-stu-id="2ee89-131">For example, Software version, Administrator comments, and Publisher.</span></span> <span data-ttu-id="2ee89-132">Mithilfe dieser Informationen können Sie die Anwendung in der Konfigurations-Manager-Konsole sortieren und suchen.</span><span class="sxs-lookup"><span data-stu-id="2ee89-132">You can use this information to to help you sort and find the application in the Configuration Manager console.</span></span>

   <span data-ttu-id="2ee89-133">Sie können auch das Feld **Installationsprogramm** verwenden, um die vollständige Befehlszeile anzugeben, die zum Installieren der Anwendung auf PCs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2ee89-133">You can also use the **Installation program** field to specify the full command line that will be used to install the application on PCs.</span></span> <span data-ttu-id="2ee89-134">Sie können dies bearbeiten, um eigene Eigenschaften hinzuzufügen (z. B. **/q** für eine unbeaufsichtigte Installation).</span><span class="sxs-lookup"><span data-stu-id="2ee89-134">You can edit this to add your own properties (for example, **/q** for an unattended installation).</span></span>

   <span data-ttu-id="2ee89-135">Der folgende Screenshot zeigt ein Beispiel, in dem die Felder **Informationen über diese Anwendung angeben** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2ee89-135">The following screenshot shows an example where the **Specify information about this application** fields are used.</span></span>

   ![Anwendungsmetadaten angeben](./media/edge-ent-deployment-sccm/edge-ent-create-app-5.png)

6. <span data-ttu-id="2ee89-137">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="2ee89-137">Click **Next**.</span></span>
7. <span data-ttu-id="2ee89-138">Auf der Seite **Zusammenfassung** können Sie die Anwendungseinstellungen unter **Details** bestätigen und anschließend den Assistenten beenden.</span><span class="sxs-lookup"><span data-stu-id="2ee89-138">On the **Summary** page, you can confirm your application settings under **Details** and then finish using the wizard.</span></span> <span data-ttu-id="2ee89-139">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="2ee89-139">Click **Next**.</span></span>  

    ![Details der Anwendungseinstellungen](./media/edge-ent-deployment-sccm/edge-ent-create-app-6.png)

8. <span data-ttu-id="2ee89-141">Klicken Sie auf der Seite **Fertigstellung** auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="2ee89-141">On the **Completion** page, click **Close**.</span></span>

    ![Dialogfeld mit der Erfolgsmeldung](./media/edge-ent-deployment-sccm/edge-ent-create-app-7.png)

<span data-ttu-id="2ee89-143">Sie haben die Anwendung fertig erstellt.</span><span class="sxs-lookup"><span data-stu-id="2ee89-143">You've finished creating the application.</span></span> <span data-ttu-id="2ee89-144">Führen Sie die folgenden Schritteaus, um sie im Konfigurations-Manager anzuzeigen:</span><span class="sxs-lookup"><span data-stu-id="2ee89-144">Use the following steps to see it in Configuration Manager:</span></span>

- <span data-ttu-id="2ee89-145">wählen Sie den Arbeitsbereich **Softwarebibliothek** aus</span><span class="sxs-lookup"><span data-stu-id="2ee89-145">select the **Software Library** workspace</span></span>
- <span data-ttu-id="2ee89-146">erweitern Sie die **Anwendungsverwaltung**</span><span class="sxs-lookup"><span data-stu-id="2ee89-146">expand **Application Management**</span></span>
- <span data-ttu-id="2ee89-147">klicken Sie auf **Anwendungen**.</span><span class="sxs-lookup"><span data-stu-id="2ee89-147">click **Applications**.</span></span>

<span data-ttu-id="2ee89-148">Der folgende Screenshot zeigt das für diesen Artikel verwendete Beispiel.</span><span class="sxs-lookup"><span data-stu-id="2ee89-148">The following screenshot shows the example used for this article.</span></span>  

![Anwendungen](./media/edge-ent-deployment-sccm/edge-ent-create-app-8.png)

## <a name="change-application-properties-and-deployment-settings"></a><span data-ttu-id="2ee89-150">Ändern von Anwendungseigenschaften und Bereitstellungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="2ee89-150">Change application properties and deployment settings</span></span>

<span data-ttu-id="2ee89-151">Nachdem Sie eine Anwendung erstellt haben, können Sie die Anwendungseinstellungen bei Bedarf verfeinern.</span><span class="sxs-lookup"><span data-stu-id="2ee89-151">After you create an application, you can refine the application settings if you need to.</span></span> <span data-ttu-id="2ee89-152">So zeigen Sie die Anwendungseigenschaften an:</span><span class="sxs-lookup"><span data-stu-id="2ee89-152">To look at the application properties:</span></span>

- <span data-ttu-id="2ee89-153">wählen Sie die Anwendung aus</span><span class="sxs-lookup"><span data-stu-id="2ee89-153">select the application</span></span>
- <span data-ttu-id="2ee89-154">Klicken Sie unter **Home**>**Eigenschaften** auf **Eigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="2ee89-154">in **Home**>**Properties**, click **Properties**.</span></span>  

   ![Konfigurieren der Anwendungseigenschaften](./media/edge-ent-deployment-sccm/edge-ent-create-app-req-1.png)

 <span data-ttu-id="2ee89-156">Auf der Dialogseite **<application name\> Anwendungseigenschaften** wird eine Registerkartenansicht der Elemente angezeigt, die Sie konfigurieren können, um das Verhalten der Anwendung zu ändern.</span><span class="sxs-lookup"><span data-stu-id="2ee89-156">In the **<application name\> Application Properties** dialog page, you'll see a tabbed view of the items that you can configure to change the behavior of the application.</span></span> <span data-ttu-id="2ee89-157">Weitere Informationen über die konfigurierbaren Einstellungen finden Sie unter [Anwendungen erstellen](/sccm/apps/deploy-use/create-applications).</span><span class="sxs-lookup"><span data-stu-id="2ee89-157">For more information about the settings you can configure, see [Create applications](/sccm/apps/deploy-use/create-applications).</span></span>

<span data-ttu-id="2ee89-158">In diesem Beispiel ändern Sie einige Eigenschaften des Bereitstellungstyps der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="2ee89-158">For this example, you'll change some properties of the application's deployment type.</span></span> <span data-ttu-id="2ee89-159">So ändern Sie die Bereitstellungseigenschaften:</span><span class="sxs-lookup"><span data-stu-id="2ee89-159">To change the deployment properties:</span></span>

1. <span data-ttu-id="2ee89-160">Klicken Sie auf die Registerkarte **Bereitstellungstypen**.</span><span class="sxs-lookup"><span data-stu-id="2ee89-160">Click the **Deployment Types** tab.</span></span>
2. <span data-ttu-id="2ee89-161">Wählen Sie unter **Bereitstellungstypen** den **Namen** der Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="2ee89-161">Under **Deployment types:**, select the application **Name**</span></span>
3. <span data-ttu-id="2ee89-162">Klicken Sie auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="2ee89-162">Click **Edit**.</span></span>

   ![Bearbeiten Sie den Bereitstellungstyp.](./media/edge-ent-deployment-sccm/edge-ent-create-app-req-2.png)

### <a name="add-a-requirement-to-the-deployment-type"></a><span data-ttu-id="2ee89-164">Fügen Sie dem Bereitstellungstyp eine Anforderung hinzu.</span><span class="sxs-lookup"><span data-stu-id="2ee89-164">Add a requirement to the deployment type</span></span>

 <span data-ttu-id="2ee89-165">Mit Anforderungen werden Bedingungen angegeben, die erfüllt sein müssen, bevor eine Anwendung auf einem Gerät installiert wird.</span><span class="sxs-lookup"><span data-stu-id="2ee89-165">Requirements specify conditions that must be met before an application is installed on a device.</span></span> <span data-ttu-id="2ee89-166">Sie können aus integrierten Anforderungen auswählen oder Ihre eigene Anforderung erstellen.</span><span class="sxs-lookup"><span data-stu-id="2ee89-166">You can choose from built-in requirements or you can create your own.</span></span> <span data-ttu-id="2ee89-167">Sie können beispielsweise eine Anforderung hinzufügen, dass die Anwendung nur auf PCs installiert wird, auf denen Windows10 **x86** oder **x64** ausgeführt wird, abhängig von der Zielprozessorarchitektur der Installationsdatei.</span><span class="sxs-lookup"><span data-stu-id="2ee89-167">For example, you can add a requirement that the application will only be installed on PCs that are running Windows 10 **x86** or **x64**, depending on the installation file's target processor architecture.</span></span> <span data-ttu-id="2ee89-168">In diesem Beispiel geben Sie Windows10 **x86** an.</span><span class="sxs-lookup"><span data-stu-id="2ee89-168">In this example, you'll specify Windows 10 **x86**.</span></span>

1. <span data-ttu-id="2ee89-169">Klicken Sie auf der soeben geöffneten Seite „Eigenschaften des Bereitstellungstyps” auf die Registerkarte **Anforderungen**.</span><span class="sxs-lookup"><span data-stu-id="2ee89-169">From the deployment type properties page you just opened, click the **Requirements** tab.</span></span>

2. <span data-ttu-id="2ee89-170">Klicken Sie auf **Hinzufügen**, um das Dialogfeld **Anforderung erstellen** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="2ee89-170">Click **Add** to open the **Create Requirement** dialog.</span></span>

    ![Anforderung erstellen](./media/edge-ent-deployment-sccm/edge-ent-create-app-req-3.png)

3. <span data-ttu-id="2ee89-172">Geben Sie im Dialogfeld **Anforderung erstellen** die folgenden Informationen ein:</span><span class="sxs-lookup"><span data-stu-id="2ee89-172">In the **Create Requirement** dialog box, specify the following information:</span></span>

    - <span data-ttu-id="2ee89-173">**Kategorie**: **Gerät**</span><span class="sxs-lookup"><span data-stu-id="2ee89-173">**Category**: **Device**</span></span>  

    - <span data-ttu-id="2ee89-174">**Bedingung**: **Betriebssystem**</span><span class="sxs-lookup"><span data-stu-id="2ee89-174">**Condition**: **Operating system**</span></span>  

    - <span data-ttu-id="2ee89-175">**Regeltyp**: **Wert**</span><span class="sxs-lookup"><span data-stu-id="2ee89-175">**Rule type**: **Value**</span></span>  

    - <span data-ttu-id="2ee89-176">**Operator**: **Einer von**</span><span class="sxs-lookup"><span data-stu-id="2ee89-176">**Operator**: **One of**</span></span>  

    - <span data-ttu-id="2ee89-177">Wählen Sie in der Liste der Betriebssysteme **Windows10** > **Alle Windows10 (32-Bit)-Systeme** aus.</span><span class="sxs-lookup"><span data-stu-id="2ee89-177">From the operating systems list, select **Windows 10** > **All Windows 10 (32-bit)**.</span></span>  

    <span data-ttu-id="2ee89-178">Wenn Sie fertig sind, sieht das Dialogfeld folgendermaßen aus:</span><span class="sxs-lookup"><span data-stu-id="2ee89-178">When you're finished, the dialog will look like the following screenshot example:</span></span>

    ![Anforderung hinzufügen](./media/edge-ent-deployment-sccm/edge-ent-create-app-req-4.png)

4. <span data-ttu-id="2ee89-180">Klicken Sie auf **OK**, um die einzelnen geöffneten Eigenschaftenseiten zu schließen und zur Liste **Anwendungen** in der Konfigurations-Manager-Konsole zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="2ee89-180">Click **OK** to close each open property page and return to the **Applications** list in the Configuration Manager console.</span></span>  

## <a name="add-the-application-content-to-a-distribution-point"></a><span data-ttu-id="2ee89-181">Hinzufügen des Anwendungsinhalts zu einem Verteilungspunkt</span><span class="sxs-lookup"><span data-stu-id="2ee89-181">Add the application content to a distribution point</span></span>  

<span data-ttu-id="2ee89-182">Um die aktualisierte Anwendung auf PCs bereitzustellen, müssen Sie sicherstellen, dass der Anwendungsinhalt auf einen Verteilungspunkt kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="2ee89-182">To deploy the updated application to PCs, make sure that the application content is copied to a distribution point.</span></span> <span data-ttu-id="2ee89-183">PCs greifen auf den Verteilungspunkt zu, um die Anwendung zu installieren.</span><span class="sxs-lookup"><span data-stu-id="2ee89-183">PCs access the distribution point to install the application.</span></span>  

>[!TIP]
><span data-ttu-id="2ee89-184">Weitere Informationen zu Verteilungspunkten und zur Inhaltsverwaltung im Konfigurations-Manager finden Sie unter [Bereitstellen und Verwalten von Inhalten für System Center Konfigurations-Manager](/sccm/core/servers/deploy/configure/deploy-and-manage-content).</span><span class="sxs-lookup"><span data-stu-id="2ee89-184">To find out more about distribution points and content management in Configuration Manager, see [Deploy and manage content for System Center Configuration Manager](/sccm/core/servers/deploy/configure/deploy-and-manage-content).</span></span>  

1. <span data-ttu-id="2ee89-185">Klicken Sie in der Konfigurations-Manager-Konsole auf **Softwarebibliothek**.</span><span class="sxs-lookup"><span data-stu-id="2ee89-185">In the Configuration Manager console, click **Software Library**.</span></span>  

2. <span data-ttu-id="2ee89-186">Erweitern Sie im Arbeitsbereich **Softwarebibliothek** den Eintrag **Anwendungen**.</span><span class="sxs-lookup"><span data-stu-id="2ee89-186">In the **Software Library** workspace, expand **Applications**.</span></span> <span data-ttu-id="2ee89-187">Wählen Sie in der Liste der Anwendungen die von Ihnen erstellte Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="2ee89-187">Select the application you created in the list of applications.</span></span>

3. <span data-ttu-id="2ee89-188">Klicken Sie in der **Bereitstellungsgruppe** auf der Registerkarte **Start** auf **Inhalt verteilen**.</span><span class="sxs-lookup"><span data-stu-id="2ee89-188">On the **Home** tab in the **Deployment** group, click **Distribute Content**.</span></span>  

4. <span data-ttu-id="2ee89-189">Überprüfen Sie auf der Seite **Allgemein** des **Assistenten für die Verteilung von Inhalt**, ob der Anwendungsname korrekt ist, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="2ee89-189">On the **General** page of the **Distribute Content Wizard**, check that the application name is correct, and then click **Next**.</span></span>  

5. <span data-ttu-id="2ee89-190">Überprüfen Sie auf der Seite **Inhalt** die Informationen, die in den Verteilungspunkt kopiert werden, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="2ee89-190">On the **Content** page, review the information that will be copied to the distribution point, and then click **Next**.</span></span>  

6. <span data-ttu-id="2ee89-191">Klicken Sie auf der Seite **Inhaltsziel** auf **Hinzufügen**, um eine oder mehrere Sammlungen, Verteilungspunkte oder die Verteilungspunktgruppe auszuwählen, auf denen der Anwendungsinhalt installiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="2ee89-191">On the **Content Destination** page, click **Add** to select one or more collections, distribution points, or distribution point groups on which to install the application content.</span></span>

7. <span data-ttu-id="2ee89-192">Führen Sie den Assistenten bis zum Ende aus.</span><span class="sxs-lookup"><span data-stu-id="2ee89-192">Complete the wizard.</span></span>

<span data-ttu-id="2ee89-193">Sie können im Arbeitsbereich **Überwachung** unter **Verteilungsstatus** > **Inhaltsstatus** überprüfen, ob der Anwendungsinhalt erfolgreich auf den Verteilungspunkt kopiert wurde.</span><span class="sxs-lookup"><span data-stu-id="2ee89-193">You can check that the application content was copied successfully to the distribution point from the **Monitoring** workspace, under **Distribution Status** > **Content Status**.</span></span>  

## <a name="deploy-the-application"></a><span data-ttu-id="2ee89-194">Bereitstellen der Anwendung</span><span class="sxs-lookup"><span data-stu-id="2ee89-194">Deploy the application</span></span>  

<span data-ttu-id="2ee89-195">Stellen Sie als Nächstes die Anwendung für eine Gerätesammlung in Ihrer Hierarchie bereit.</span><span class="sxs-lookup"><span data-stu-id="2ee89-195">Next, deploy the application to a device collection in your hierarchy.</span></span> <span data-ttu-id="2ee89-196">In diesem Beispiel stellen Sie die Anwendung für die Gerätesammlung **Alle Systeme“** bereit.</span><span class="sxs-lookup"><span data-stu-id="2ee89-196">In this example, you deploy the application to the **All Systems** device collection.</span></span>  

>[!TIP]
><span data-ttu-id="2ee89-197">Beachten Sie, dass die Anwendung nur von Windows 10-Computern mit der angegebenen Prozessorarchitektur aufgrund der zuvor ausgewählten Anforderungen installiert wird.</span><span class="sxs-lookup"><span data-stu-id="2ee89-197">Remember that only Windows 10 computers of the specified processor architecture will install the application because of the requirements that you selected earlier.</span></span>  

1. <span data-ttu-id="2ee89-198">Klicken Sie in der Konfigurations-Manager-Konsole auf **Softwarebibliothek** > **Anwendungsverwaltung** > **Anwendungen**.</span><span class="sxs-lookup"><span data-stu-id="2ee89-198">In the Configuration Manager console, click **Software Library** > **Application Management** > **Applications**.</span></span>

2. <span data-ttu-id="2ee89-199">Wählen Sie aus der Liste der Anwendungen die Anwendung aus, die Sie zuvor erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="2ee89-199">From the list of applications, select the application that you created earlier.</span></span> <span data-ttu-id="2ee89-200">Klicken Sie dann auf der Registerkarte **Start** in der Gruppe **Bereitstellung** auf **Bereitstellen**, oder klicken Sie mit der rechten Maustaste auf die Anwendung und wählen Sie **Bereitstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="2ee89-200">Then, on the **Home** tab in the **Deployment** group, click **Deploy**, or right-click the application and select **Deploy**.</span></span>

    ![Bereitstellen der Anwendung](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-1.png)

3. <span data-ttu-id="2ee89-202">Klicken Sie im **Assistenten zum Bereitstellen von Software** auf der Seite **Allgemein** auf **Durchsuchen**, um die Gerätesammlung auszuwählen, für die Sie die Anwendung bereitstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="2ee89-202">On the **General** page of the **Deploy Software Wizard**, click **Browse** to select the device collection to which you want to deploy the application.</span></span>

    ![Navigieren zur Installationsdatei](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-2.png)

4. <span data-ttu-id="2ee89-204">Überprüfen Sie auf der Seite **Inhalt**, ob der Verteilungspunkt ausgewählt ist, von dem aus PCs die Anwendung installieren sollen.</span><span class="sxs-lookup"><span data-stu-id="2ee89-204">On the **Content** page, check that the distribution point from which you want PCs to install the application is selected.</span></span>

    ![Angeben des Verteilungspunktes](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-6.png)

5. <span data-ttu-id="2ee89-206">Stellen Sie auf der Seite **Bereitstellungseinstellungen** sicher, dass die Bereitstellungsaktion auf **Installieren** und der Bereitstellungszweck auf **Erforderlich** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="2ee89-206">On the **Deployment Settings** page, make sure that the deployment action is set to **Install**, and the deployment purpose is set to **Required**.</span></span>

    ![Konfigurieren der Bereitstellungseinstellungen](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-8.png)

    >[!TIP]
    ><span data-ttu-id="2ee89-208">Indem Sie den Bereitstellungszweck auf **Erforderlich** festlegen, stellen Sie sicher, dass die Anwendung auf PCs installiert wird, die die von Ihnen festgelegten Anforderungen erfüllen.</span><span class="sxs-lookup"><span data-stu-id="2ee89-208">By setting the deployment purpose to **Required**, you make sure that the application is installed on PCs that meet the requirements that you set.</span></span> <span data-ttu-id="2ee89-209">Wenn Sie diesen Wert auf **"Verfügbar**" festlegen, können Benutzer die Anwendung bei Bedarf über das Software Center installieren.</span><span class="sxs-lookup"><span data-stu-id="2ee89-209">If you set this value to **Available**, then users can install the application on demand from Software Center.</span></span>  

6. <span data-ttu-id="2ee89-210">Auf der Seite **Planen** können Sie konfigurieren, wann die Anwendung installiert wird.</span><span class="sxs-lookup"><span data-stu-id="2ee89-210">On the **Scheduling** page, you can configure when the application will be installed.</span></span> <span data-ttu-id="2ee89-211">Wählen Sie in diesem Beispiel **So bald wie möglich nach dem Zeitpunkt der Verfügbarkeit** aus.</span><span class="sxs-lookup"><span data-stu-id="2ee89-211">For this example, select **As soon as possible after the available time**.</span></span>

    ![Planen der Bereitstellung](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-9.png)

7. <span data-ttu-id="2ee89-213">Wählen Sie auf der Seite **Installationsoptionen** die gewünschten Werte aus und klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="2ee89-213">On the **User Experience** page, select your desired values and click **Next**.</span></span>

    ![Angeben von Installationsoptionen](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-10.png)

8. <span data-ttu-id="2ee89-215">Geben Sie die gewünschten Benachrichtigungsoptionen an und klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="2ee89-215">Specify your desired alert options and click **Next**.</span></span>

    ![Angeben von Benachrichtigungseinstellungen](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-11.png)

9. <span data-ttu-id="2ee89-217">Führen Sie den Assistenten bis zum Ende aus.</span><span class="sxs-lookup"><span data-stu-id="2ee89-217">Complete the wizard.</span></span>

<span data-ttu-id="2ee89-218">Verwenden Sie die Informationen im folgenden Abschnitt **Überwachen der Anwendung**, um den Status der Anwendungsbereitstellung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="2ee89-218">Use the information in the following **Monitor the application** section to see the status of your application deployment.</span></span>  

## <a name="monitor-the-application"></a><span data-ttu-id="2ee89-219">Die Anwendung überwachen</span><span class="sxs-lookup"><span data-stu-id="2ee89-219">Monitor the application</span></span>

 <span data-ttu-id="2ee89-220">In diesem Abschnittsehen Sie sich den Bereitstellungsstatus der soeben bereitgestellten Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="2ee89-220">In this section, you'll take a quick look at the deployment status of the application that you just deployed.</span></span>  

### <a name="to-review-the-deployment-status"></a><span data-ttu-id="2ee89-221">So überprüfen Sie den Bereitstellungsstatus</span><span class="sxs-lookup"><span data-stu-id="2ee89-221">To review the deployment status</span></span>  

1. <span data-ttu-id="2ee89-222">Klicken Sie in der Konfigurations-Manager-Konsole auf **Überwachung** > **Bereitstellungen**.</span><span class="sxs-lookup"><span data-stu-id="2ee89-222">In the Configuration Manager console, click **Monitoring** > **Deployments**.</span></span>  

2. <span data-ttu-id="2ee89-223">Wählen Sie die Anwendung aus der Liste der Bereitstellungen aus.</span><span class="sxs-lookup"><span data-stu-id="2ee89-223">From the list of deployments, select the application.</span></span>

    ![Überwachen der Bereitstellung](./media/edge-ent-deployment-sccm/edge-ent-monitor-deployment.png)

3. <span data-ttu-id="2ee89-225">Klicken Sie auf der Registerkarte **Start** in der Gruppe **Bereitstellung** auf **Status anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="2ee89-225">On the **Home** tab in the **Deployment** group, click **View Status**.</span></span>  

4. <span data-ttu-id="2ee89-226">Wählen Sie eine der folgenden Registerkarten aus, um weitere Statusaktualisierungen zur Anwendungsbereitstellung anzuzeigen:</span><span class="sxs-lookup"><span data-stu-id="2ee89-226">Select one of the following tabs to see more status updates about the application deployment:</span></span>  

    - <span data-ttu-id="2ee89-227">**Erfolg**: Die Anwendung wurde auf den angegebenen PCs erfolgreich installiert.</span><span class="sxs-lookup"><span data-stu-id="2ee89-227">**Success**: The application installed successfully on the indicated PCs.</span></span>  

    - <span data-ttu-id="2ee89-228">**In Bearbeitung**: Die Anwendung ist noch nicht fertig installiert.</span><span class="sxs-lookup"><span data-stu-id="2ee89-228">**In Progress**: The application has not yet finished installing.</span></span>  

    - <span data-ttu-id="2ee89-229">**Fehler**: Bei der Installation der Anwendung auf den angegebenen PCs ist ein Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="2ee89-229">**Error**: An error occurred installing the application on the indicated PCs.</span></span> <span data-ttu-id="2ee89-230">Weitere Informationen zum Fehler werden ebenfalls angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2ee89-230">Further information about the error is also displayed.</span></span>  

    - <span data-ttu-id="2ee89-231">**Anforderungen nicht erfüllt**: Auf den angegebenen Geräten wurde kein Installationsversuch durchgeführt, da sie nicht den von Ihnen konfigurierten Anforderungen entsprachen (in diesem Beispiel, weil sie nicht unter Windows 10 ausgeführt werden).</span><span class="sxs-lookup"><span data-stu-id="2ee89-231">**Requirements Not Met**: No installation attempt was made on the indicated devices because they did not meet the requirements you configured (in this example, because they do not run on Windows 10.)</span></span>

    - <span data-ttu-id="2ee89-232">**Unbekannt**: Der Konfigurations-Manager konnte den Status der Bereitstellung nicht melden.</span><span class="sxs-lookup"><span data-stu-id="2ee89-232">**Unknown**: Configuration Manager was unable to report the status of the deployment.</span></span> <span data-ttu-id="2ee89-233">Bitte versuchen Sie es später noch einmal.</span><span class="sxs-lookup"><span data-stu-id="2ee89-233">Check back again later.</span></span>  

    >[!TIP]
    ><span data-ttu-id="2ee89-234">Es gibt verschiedene Möglichkeiten, Anwendungsbereitstellungen zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="2ee89-234">There are several ways you can monitor application deployments.</span></span> <span data-ttu-id="2ee89-235">Weitere Informationen finden Sie unter [Überwachen von Anwendungen in der System Center Konfigurations-Manager-Konsole](/sccm/apps/deploy-use/monitor-applications-from-the-console).</span><span class="sxs-lookup"><span data-stu-id="2ee89-235">For more information, see [Monitor applications from the System Center Configuration Manager console](/sccm/apps/deploy-use/monitor-applications-from-the-console).</span></span>  

## <a name="end-user-experience"></a><span data-ttu-id="2ee89-236">Installationsoptionen für Endbenutzer</span><span class="sxs-lookup"><span data-stu-id="2ee89-236">End-user experience</span></span>  

<span data-ttu-id="2ee89-237">Benutzer mit PCs, die von Konfigurations-Manager verwaltet werden und Windows10 der angegebenen Prozessorarchitektur ausführen, werden in einer Meldung darüber informiert, dass sie die Microsoft Edge Dev-Anwendung installieren müssen.</span><span class="sxs-lookup"><span data-stu-id="2ee89-237">Users who have PCs that are managed by Configuration Manager and are running Windows 10 of the specified processor architecture, will see a message telling them that they must install the Microsoft Edge Dev application.</span></span> <span data-ttu-id="2ee89-238">Wenn sie diese Installationsoption akzeptieren, wird die Anwendung installiert.</span><span class="sxs-lookup"><span data-stu-id="2ee89-238">When they accept this installation option, the application is installed.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2ee89-239">Weitere Informationen:</span><span class="sxs-lookup"><span data-stu-id="2ee89-239">See also</span></span>

- [<span data-ttu-id="2ee89-240">Microsoft Edge Enterprise-Angebotsseite</span><span class="sxs-lookup"><span data-stu-id="2ee89-240">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="2ee89-241">Weitere Informationen zum Bereitstellen von MSI-Paketen finden Sie unter Erstellen und Bereitstellen einer Anwendung mit System Center Konfigurations-Manager.</span><span class="sxs-lookup"><span data-stu-id="2ee89-241">Create and deploy an application with System Center Configuration Manager</span></span>](/sccm/apps/get-started/create-and-deploy-an-application)