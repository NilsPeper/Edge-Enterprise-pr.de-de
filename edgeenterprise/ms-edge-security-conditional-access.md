---
title: Microsoft Edge und bedingter Zugriff
ms.author: srugh
author: srugh
manager: seanlyn
ms.date: 10/02/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Edge und bedingter Zugriff
ms.openlocfilehash: a81d39c15f418dab6565ee7acc45de17f66e3828
ms.sourcegitcommit: 3478cfcf2b03944213a7c7c61f05490bc37aa7c4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/03/2020
ms.locfileid: "11094773"
---
# <span data-ttu-id="6b357-103">Microsoft Edge und bedingter Zugriff</span><span class="sxs-lookup"><span data-stu-id="6b357-103">Microsoft Edge and Conditional Access</span></span>
  
<span data-ttu-id="6b357-104">Dieser Artikel beschreibt, wie Microsoft Edge bedingten Zugriff unterstützt und wie Sie auf Ressourcen zugreifen können, die durch bedingten Zugriff geschützt sind.</span><span class="sxs-lookup"><span data-stu-id="6b357-104">This article describes how Microsoft Edge supports Conditional Access, and how to access resources protected by Conditional Access.</span></span>

> [!NOTE]
> <span data-ttu-id="6b357-105">Dieser Artikel bezieht sich auf Microsoft Edge Version 77 oder neuer.</span><span class="sxs-lookup"><span data-stu-id="6b357-105">This article applies to Microsoft Edge version 77 or later.</span></span>

<span data-ttu-id="6b357-106">Ein wichtiger Aspekt der Cloud-Sicherheit ist die Identität und der Zugriff, wenn es um die Verwaltung von Cloud-Ressourcen geht.</span><span class="sxs-lookup"><span data-stu-id="6b357-106">A key aspect of cloud security is identity and access when it comes to managing your cloud resources.</span></span> <span data-ttu-id="6b357-107">In einer mobilen Welt, in der die Cloud an erster Stelle steht, können Benutzer mit einer Vielzahl von Geräten und Apps von überall aus auf die Ressourcen Ihres Unternehmens zugreifen.</span><span class="sxs-lookup"><span data-stu-id="6b357-107">In a mobile-first, cloud-first world, users can access your organization's resources using a variety of devices and apps from anywhere.</span></span> <span data-ttu-id="6b357-108">Folglich reicht es nicht aus, sich nur darauf zu konzentrieren, wer auf eine Ressource zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="6b357-108">As a result of this, just focusing on who can access a resource is not sufficient.</span></span> <span data-ttu-id="6b357-109">Sie müssen auch berücksichtigen, wie auf eine Ressource zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="6b357-109">You also need to factor in how a resource is accessed.</span></span> <span data-ttu-id="6b357-110">Mit bedingtem Zugriff auf Azure Active Directory (Azure AD) können Sie das Gleichgewicht zwischen Sicherheit und Produktivität herstellen.</span><span class="sxs-lookup"><span data-stu-id="6b357-110">Azure Active Directory (Azure AD) Conditional Access helps you master the balance between security and productivity.</span></span>

## <span data-ttu-id="6b357-111">Zugriff auf Ressourcen mit Zugriffsschutz in Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="6b357-111">Accessing Conditional Access protected resources in Microsoft Edge</span></span>

<span data-ttu-id="6b357-112">Microsoft Edge unterstützt den Azure AD bedingten Zugriff systemeigen.</span><span class="sxs-lookup"><span data-stu-id="6b357-112">Microsoft Edge natively supports Azure AD Conditional Access.</span></span> <span data-ttu-id="6b357-113">Es ist nicht erforderlich, eine separate Erweiterung zu installieren.</span><span class="sxs-lookup"><span data-stu-id="6b357-113">There's no need to install a separate extension.</span></span> <span data-ttu-id="6b357-114">Wenn Sie bei einem Microsoft Edge-Profil mit Unternehmens-Azure AD-Anmeldeinformationen angemeldet sind, ermöglicht Microsoft Edge den nahtlosen Zugriff auf Unternehmens-Cloud-Ressourcen, die mit bedingtem Zugriff geschützt sind.</span><span class="sxs-lookup"><span data-stu-id="6b357-114">When you're signed into a Microsoft Edge profile with enterprise Azure AD credentials, Microsoft Edge allows seamless access to enterprise cloud resources protected using Conditional Access.</span></span>

<span data-ttu-id="6b357-115">Auf einem kompatiblen Gerät sollte die Identität, die auf die Ressource zugreift, mit der Identität im Profil übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="6b357-115">On a compliant device, the identity accessing the resource should match the identity on the profile.</span></span>  <span data-ttu-id="6b357-116">Wenn dies nicht der Fall ist, wird eine Meldung wie die im nächsten Screenshot angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6b357-116">If it doesn't, you'll see a message like the one in the next screenshot.</span></span> <span data-ttu-id="6b357-117">Im Screenshot-Beispiel ist „testadmin@evostsoneboxtest.com” das Anmeldekonto, das für den Zugriff auf die Ressource erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="6b357-117">In the screenshot example, "testadmin@evostsoneboxtest.com" is the sign-in account needed to access the resource.</span></span>

![Nachricht über bedingten Zugriff im Browser](./media/edge-security/microsoft-edge-security-conditional-access.png)

<span data-ttu-id="6b357-119">Um fortzufahren, müssen Sie zu dem erforderlichen Profil (falls vorhanden) wechseln oder ein Profil mit einer entsprechenden Identität erstellen.</span><span class="sxs-lookup"><span data-stu-id="6b357-119">To continue, you have to switch to the required profile (if you have one) or create a profile with matching identity.</span></span>

<span data-ttu-id="6b357-120">Klicken Sie in der oberen rechten Ecke des Browsers auf das Profilbild, um sich anzumelden und mit Ihrem Profil zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="6b357-120">To sign in and work with your profile, click the account picture in the top right corner of the browser.</span></span> <span data-ttu-id="6b357-121">Sie können das Menü Manage Alert für folgende Aufgaben verwenden:</span><span class="sxs-lookup"><span data-stu-id="6b357-121">You can use the dropdown menu to:</span></span>

- <span data-ttu-id="6b357-122">Wählen Sie ein anderes Profil aus.</span><span class="sxs-lookup"><span data-stu-id="6b357-122">Select another profile.</span></span> <span data-ttu-id="6b357-123">Klicken Sie auf den Profilnamen.</span><span class="sxs-lookup"><span data-stu-id="6b357-123">Click the profile name.</span></span>
- <span data-ttu-id="6b357-124">Erstellen eines Marketingprofils</span><span class="sxs-lookup"><span data-stu-id="6b357-124">Create a profile.</span></span> <span data-ttu-id="6b357-125">Klicken Sie auf **Feature hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="6b357-125">Click **Add a profile**.</span></span>
- <span data-ttu-id="6b357-126">Verwalten Sie Ihre Profile.</span><span class="sxs-lookup"><span data-stu-id="6b357-126">Manage your profiles.</span></span> <span data-ttu-id="6b357-127">Klicken Sie auf **Profileinstellungen verwalten**.</span><span class="sxs-lookup"><span data-stu-id="6b357-127">Click **Manage profile settings**.</span></span>

<span data-ttu-id="6b357-128">Diese Unterstützung ist auf allen Plattformen verfügbar, einschließlich aller unterstützten Versionen von Windows und macOS.</span><span class="sxs-lookup"><span data-stu-id="6b357-128">This support is available across all platforms, including all supported versions of Windows and macOS.</span></span>

### <span data-ttu-id="6b357-129">So stellen Sie den bedingten Zugriff in Azure Active Directory bereit</span><span class="sxs-lookup"><span data-stu-id="6b357-129">How to deploy Conditional Access in Azure Active Directory</span></span>

<span data-ttu-id="6b357-130">[Bereitstellen des bedingten Zugriffs](https://docs.microsoft.com/azure/active-directory/conditional-access/plan-conditional-access) enthält eine ausführliche Anleitung zur Bereitstellung des bedingten Zugriffs in Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6b357-130">[Deploy Conditional Access](https://docs.microsoft.com/azure/active-directory/conditional-access/plan-conditional-access) provides a detailed guide to help deploy Conditional Access in Azure Active Directory.</span></span>

## <span data-ttu-id="6b357-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6b357-131">See also</span></span>

- [<span data-ttu-id="6b357-132">Microsoft Edge Enterprise-Angebotsseite</span><span class="sxs-lookup"><span data-stu-id="6b357-132">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="6b357-133">Video: Sicherheit, Kompatibilität und Verwaltbarkeit</span><span class="sxs-lookup"><span data-stu-id="6b357-133">Video: Security, compatibility, and manageability</span></span>](/microsoft-edge-video-security-compatibility-manageability.md)
