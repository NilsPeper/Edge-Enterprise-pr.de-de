---
title: Bereitstellen von Favoriten für Microsoft Edge
ms.author: capoon
author: dan-wesley
manager: abutcher
ms.date: 09/29/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Bereitstellen von Favoriten für Microsoft Edge
ms.openlocfilehash: 94bd42573bdbc0fd1b971ded1c82e5fe152acc54
ms.sourcegitcommit: 854dd73eb168960c0eb4b483f81a8efe88806a64
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/29/2020
ms.locfileid: "11088699"
---
# <span data-ttu-id="4006f-103">Bereitstellen von Favoriten für Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="4006f-103">Provision favorites for Microsoft Edge</span></span>

<span data-ttu-id="4006f-104">Angeregt durch Kundenfeedback haben wir Verbesserungen vorgenommen, um die Bereitstellung von Favoriten zu erleichtern.</span><span class="sxs-lookup"><span data-stu-id="4006f-104">Based on customer feedback, we've made improvements to provisioning favorites.</span></span> <span data-ttu-id="4006f-105">Ab Microsoft Edge, Version 85 müssen Administratoren keine Dateien mehr manuell erstellen, um Favoriten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="4006f-105">Starting with Microsoft Edge version 85, Admins no longer have to manually craft a file to provision favorites.</span></span> <span data-ttu-id="4006f-106">Administratoren können zum Hinzufügen von Favoriten und Ordnern die Microsoft Edge-Benutzeroberfläche verwenden, um eine Datei zu generieren, die in eine Gruppenrichtlinie exportiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="4006f-106">Admins can add favorites and folders using the Microsoft Edge UI to generate a file that can be exported to a group policy.</span></span>

<span data-ttu-id="4006f-107">In diesem Artikel wird beschrieben, wie Sie Favoriten und Ordner für Ihre Organisation bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="4006f-107">This article describes how to provision a set of favorites and folders for your organization.</span></span> <span data-ttu-id="4006f-108">Sie können die Richtlinie zum [Konfigurieren von Favoriten](https://docs.microsoft.com//DeployEdge/microsoft-edge-policies#configure-favorites) verwenden, um Favoriten und Ordner bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="4006f-108">You can use the [Configure favorites](https://docs.microsoft.com//DeployEdge/microsoft-edge-policies#configure-favorites) policy to provision favorites and folders.</span></span>

> [!NOTE]
> <span data-ttu-id="4006f-109">Dieser Artikel bezieht sich auf Microsoft Edge Version 85 oder neuer.</span><span class="sxs-lookup"><span data-stu-id="4006f-109">This article applies to Microsoft Edge version 85 or later.</span></span>

## <span data-ttu-id="4006f-110">Voraussetzungen und Empfehlungen</span><span class="sxs-lookup"><span data-stu-id="4006f-110">Prerequisites and recommendations</span></span>

- <span data-ttu-id="4006f-111">Microsoft Edge, Version 85 mit installierter entsprechender administrativer Vorlage für Gruppenrichtlinien.</span><span class="sxs-lookup"><span data-stu-id="4006f-111">Microsoft Edge version 85 with the appropriate administrative template installed for group policies.</span></span>
- <span data-ttu-id="4006f-112">Wir empfehlen, zum Bereitstellen dieser Favoriten ein neues Profil in Microsoft Edge zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="4006f-112">We recommend that you use a new profile in Microsoft Edge to provision these favorites.</span></span> <span data-ttu-id="4006f-113">Alle Favoriten, die über dieses Profil gespeichert werden, werden in den Export einbezogen.</span><span class="sxs-lookup"><span data-stu-id="4006f-113">All favorites that are saved with the profile will be included in the export.</span></span>  

## <span data-ttu-id="4006f-114">Bereitstellen von Favoriten und Ordnern</span><span class="sxs-lookup"><span data-stu-id="4006f-114">Provision favorites and folders</span></span>

<span data-ttu-id="4006f-115">Führen Sie die folgenden Schritte aus, um Ihren Benutzern Favoriten und Ordner bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="4006f-115">Use the following steps to provision favorites and folders for your users.</span></span>

1. <span data-ttu-id="4006f-116">Geben Sie in die Microsoft Edge-Adressleiste folgende URL ein: *edge://flags/#edge-favorites-admin-export*.</span><span class="sxs-lookup"><span data-stu-id="4006f-116">Go to the Microsoft Edge address bar and type this URL: *edge://flags/#edge-favorites-admin-export*.</span></span>
2. <span data-ttu-id="4006f-117">Wählen Sie unter **Export von Favoritenkonfigurationen für Administratoren** aus der Dropdownliste die Option **Aktiviert** aus, und klicken Sie dann auf **Neustart**.</span><span class="sxs-lookup"><span data-stu-id="4006f-117">Under **Favorites configuration export for administrators**, pick **Enabled** from the dropdown list and then click **Restart**.</span></span>

3. <span data-ttu-id="4006f-118">Wechseln Sie zur Seite **Favoriten** unter *edge://favorites*, um die gewünschten Favoriten und Ordner hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="4006f-118">Go to the **Favorites** page at *edge://favorites* so you can add the favorites and folders that you want to provision.</span></span>

<!--
4. On the **Favorites bar**, click **Add folder**. The folder structure of favorites that are set in the profile you're using will be reflected in the folder you provision for your users. The next screenshot shows "Managed favorites", the folder we'll use to provision favorites.

   ![Add a folder](media/edge-learnmore-provision-favorites/provision-favorites-add-folder.png)

   > [!TIP]
   > Add existing folders that contain favorites you want to provision for your users.

5. Select "Managed favorites" and then click **Add favorite**. The next screenshot shows the favorite we've added.

   ![Add a favorite](media/edge-learnmore-provision-favorites/provision-favorites-add-favorite.png)-->

4. <span data-ttu-id="4006f-119">Wenn Sie die Favoriten und Ordner hinzugefügt haben, exportieren Sie sie, damit sie von der Richtlinie zum **Konfigurieren von Favoriten** verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="4006f-119">When you finish adding favorites and folders you'll export them so they can be used by the **Configure favorites** policy.</span></span> <span data-ttu-id="4006f-120">Wechseln Sie über die Adressleiste zu *edge://favorites*, klicken Sie auf die Auslassungspunkte "**...**", und wählen Sie **Favoritenkonfiguration exportieren** aus.</span><span class="sxs-lookup"><span data-stu-id="4006f-120">Go to the address bar and navigate to *edge://favorites*, click the ellipsis "**…**" and choose **Export favorites configuration**.</span></span> <span data-ttu-id="4006f-121">Der nächste Screenshot zeigt die Optionen, die Sie beim Bereitstellen von Favoriten haben.</span><span class="sxs-lookup"><span data-stu-id="4006f-121">The next screenshot shows the options you have when provisioning favorites.</span></span>

   ![Menüoptionen für die Arbeit mit Favoriten.](media/edge-learnmore-provision-favorites/provision-favorites-menu-options.png)

5. <span data-ttu-id="4006f-123">Unter **Favoritenkonfiguration exportieren** ist der Ordner zu benennen, den die Benutzer sehen werden.</span><span class="sxs-lookup"><span data-stu-id="4006f-123">Under **Export your favorites configuration** you provide a name for the folder that your users will see.</span></span> <span data-ttu-id="4006f-124">Geben Sie den Ordnernamen ein, und wählen Sie das gewünschte Plattformformat aus.</span><span class="sxs-lookup"><span data-stu-id="4006f-124">Type the Folder name and pick the Platform format you want to use.</span></span> <span data-ttu-id="4006f-125">Klicken Sie auf **In Zwischenablage kopieren**.</span><span class="sxs-lookup"><span data-stu-id="4006f-125">Click **Copy to clipboard**.</span></span> <span data-ttu-id="4006f-126">Im nächsten Screenshot sind "Verwaltete Favoriten" als Ordnernamen und Windows als Plattform zu sehen.</span><span class="sxs-lookup"><span data-stu-id="4006f-126">The next screenshot shows "Managed favorites" for the folder name and the platform is Windows.</span></span>

   ![Dialogfeld zum Exportieren von Favoriten in einen Windows-Ordner.](media/edge-learnmore-provision-favorites/provision-favorites-export.png)

6. <span data-ttu-id="4006f-128">Öffnen Sie den Gruppenrichtlinien-Editor, navigieren Sie zu *Computerkonfiguration/Administrative Vorlagen/*, und wählen Sie **Favoriten konfigurieren** aus.</span><span class="sxs-lookup"><span data-stu-id="4006f-128">Open the Group Policy Editor, navigate to *Computer Configuration/Administrative Templates/* and pick **Configure Favorites**.</span></span> <span data-ttu-id="4006f-129">Aktivieren Sie die Richtlinie "Favoriten konfigurieren".</span><span class="sxs-lookup"><span data-stu-id="4006f-129">Enable the "Configure Favorites" policy.</span></span> <span data-ttu-id="4006f-130">Fügen Sie unter **Optionen:** die exportierten Inhalte in den Textbereich in "Favoriten konfigurieren" ein, und klicken Sie dann auf **Übernehmen**.</span><span class="sxs-lookup"><span data-stu-id="4006f-130">Under **Options:**, paste the exported contents in the Configure favorites text area then click **Apply**.</span></span> <span data-ttu-id="4006f-131">Der nächste Screenshot zeigt ein Beispiel für den Ordner "Verwaltete Favoriten" aus Schritt 5.</span><span class="sxs-lookup"><span data-stu-id="4006f-131">The next screenshot shows an example of the "Managed favorites" folder from step 5.</span></span>

   ![Verwenden Sie "gpedit" zum Aktivieren und Konfigurieren der Richtlinie "Favoriten konfigurieren".](media/edge-learnmore-provision-favorites/provision-favorites-gpedit.png)

7. <span data-ttu-id="4006f-133">Klicken Sie auf **OK** oder **Übernehmen**, um die Richtlinieneinstellungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="4006f-133">Click **OK** or **Apply** to safe the policy settings.</span></span>

## <span data-ttu-id="4006f-134">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4006f-134">See also</span></span>

- [<span data-ttu-id="4006f-135">Microsoft Edge Enterprise-Angebotsseite</span><span class="sxs-lookup"><span data-stu-id="4006f-135">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)