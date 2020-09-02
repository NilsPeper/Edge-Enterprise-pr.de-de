---
title: Übersicht über die Microsoft Edge-Sicherheit
ms.author: srugh
author: srugh
manager: seanlyn
ms.date: 04/29/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Übersicht über die Bereitstellung der Microsoft Edge-Sicherheit
ms.openlocfilehash: f22f2dcbace00cd535d201950c2af488c708525b
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/31/2020
ms.locfileid: "10980076"
---
# <span data-ttu-id="6dcd4-103">Übersicht über die Microsoft Edge-Sicherheit</span><span class="sxs-lookup"><span data-stu-id="6dcd4-103">Overview of Microsoft Edge security</span></span>
  
<span data-ttu-id="6dcd4-104">IT-Administratoren im Unternehmen sind ständig mit einer Vielzahl von vorhandenen und neuen Sicherheitsherausforderungen konfrontiert, während sie das Unternehmensnetzwerk und -Geräte vor böswilligen Angriffen schützen und unbefugten Zugriff und Undichtigkeiten von Unternehmensdaten verhindern.</span><span class="sxs-lookup"><span data-stu-id="6dcd4-104">IT admins in the enterprise are constantly facing a myriad of existing and emerging security challenges while protecting the corporate network and devices from malicious attacks and preventing unauthorized access and leaks of corporate data.</span></span> <span data-ttu-id="6dcd4-105">Microsoft Edge bietet mehrere systemeigene, einzigartige Funktionen, mit denen diese Herausforderungen bewältigt werden können.</span><span class="sxs-lookup"><span data-stu-id="6dcd4-105">Microsoft Edge provides several natively built, unique capabilities that help address these challenges.</span></span>

> [!NOTE]
> <span data-ttu-id="6dcd4-106">Dieser Artikel bezieht sich auf Microsoft Edge Version77 oder höher.</span><span class="sxs-lookup"><span data-stu-id="6dcd4-106">This article applies to Microsoft Edge version 77 or later.</span></span>

## <span data-ttu-id="6dcd4-107">Bedingter Zugriff</span><span class="sxs-lookup"><span data-stu-id="6dcd4-107">Conditional Access</span></span>

<span data-ttu-id="6dcd4-108">Ein wichtiger Aspekt der Cloud-Sicherheit ist die Identität und der Zugriff, wenn es um die Verwaltung von Cloud-Ressourcen geht.</span><span class="sxs-lookup"><span data-stu-id="6dcd4-108">A key aspect of cloud security is identity and access when it comes to managing your cloud resources.</span></span> <span data-ttu-id="6dcd4-109">In einer mobilen Welt, in der die Cloud an erster Stelle steht, können Benutzer mit einer Vielzahl von Geräten und Apps von überall aus auf die Ressourcen Ihres Unternehmens zugreifen.</span><span class="sxs-lookup"><span data-stu-id="6dcd4-109">In a mobile-first, cloud-first world, users can access your organization's resources using a variety of devices and apps from anywhere.</span></span> <span data-ttu-id="6dcd4-110">Folglich reicht es nicht aus, sich nur darauf zu konzentrieren, wer auf eine Ressource zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="6dcd4-110">As a result of this, just focusing on who can access a resource is not sufficient.</span></span> <span data-ttu-id="6dcd4-111">Sie müssen auch berücksichtigen, wie auf eine Ressource zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="6dcd4-111">You also need to factor in how a resource is accessed.</span></span> <span data-ttu-id="6dcd4-112">Mit bedingtem Zugriff auf Azure Active Directory (Azure AD) können Sie das Gleichgewicht zwischen Sicherheit und Produktivität herstellen.</span><span class="sxs-lookup"><span data-stu-id="6dcd4-112">Azure Active Directory (Azure AD) Conditional Access helps you master the balance between security and productivity.</span></span>

### <span data-ttu-id="6dcd4-113">Zugriff auf Ressourcen mit Zugriffsschutz in Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="6dcd4-113">Accessing Conditional Access protected resources in Microsoft Edge</span></span>

<span data-ttu-id="6dcd4-114">Microsoft Edge unterstützt den Azure AD bedingten Zugriff systemeigen.</span><span class="sxs-lookup"><span data-stu-id="6dcd4-114">Microsoft Edge natively supports Azure AD Conditional Access.</span></span> <span data-ttu-id="6dcd4-115">Es ist nicht erforderlich, eine separate Erweiterung zu installieren.</span><span class="sxs-lookup"><span data-stu-id="6dcd4-115">There's no need to install a separate extension.</span></span> <span data-ttu-id="6dcd4-116">Wenn Sie bei einem Microsoft Edge-Profil mit Unternehmens-Azure AD-Anmeldeinformationen angemeldet sind, ermöglicht Microsoft Edge den nahtlosen Zugriff auf Unternehmens-Cloud-Ressourcen, die mit bedingtem Zugriff geschützt sind.</span><span class="sxs-lookup"><span data-stu-id="6dcd4-116">When you're signed into a Microsoft Edge profile with enterprise Azure AD credentials, Microsoft Edge allows seamless access to enterprise cloud resources protected using Conditional Access.</span></span>

<span data-ttu-id="6dcd4-117">Auf einem kompatiblen Gerät sollte die Identität, die auf die Ressource zugreift, mit der Identität im Profil übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="6dcd4-117">On a compliant device, the identity accessing the resource should match the identity on the profile.</span></span>  <span data-ttu-id="6dcd4-118">Wenn dies nicht der Fall ist, wird eine Meldung wie die im nächsten Screenshot angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6dcd4-118">If it doesn't, you'll see a message like the one in the next screenshot.</span></span> <span data-ttu-id="6dcd4-119">Im Screenshot-Beispiel ist „testadmin@evostsoneboxtest.com” das Anmeldekonto, das für den Zugriff auf die Ressource erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="6dcd4-119">In the screenshot example, "testadmin@evostsoneboxtest.com" is the sign-in account needed to access the resource.</span></span>

![Nachricht über bedingten Zugriff im Browser](./media/edge-security/microsoft-edge-security-conditional-access.png)

<span data-ttu-id="6dcd4-121">Um fortzufahren, müssen Sie zu dem erforderlichen Profil (falls vorhanden) wechseln oder ein Profil mit einer entsprechenden Identität erstellen.</span><span class="sxs-lookup"><span data-stu-id="6dcd4-121">To continue, you have to switch to the required profile (if you have one) or create a profile with matching identity.</span></span>

<span data-ttu-id="6dcd4-122">Klicken Sie in der oberen rechten Ecke des Browsers auf das Profilbild, um sich anzumelden und mit Ihrem Profil zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="6dcd4-122">To sign in and work with your profile, click the account picture in the top right corner of the browser.</span></span> <span data-ttu-id="6dcd4-123">Sie können das Menü Manage Alert für folgende Aufgaben verwenden:</span><span class="sxs-lookup"><span data-stu-id="6dcd4-123">You can use the dropdown menu to:</span></span>

- <span data-ttu-id="6dcd4-124">Wählen Sie ein anderes Profil aus.</span><span class="sxs-lookup"><span data-stu-id="6dcd4-124">Select another profile.</span></span> <span data-ttu-id="6dcd4-125">Klicken Sie auf den Profilnamen.</span><span class="sxs-lookup"><span data-stu-id="6dcd4-125">Click the profile name.</span></span>
- <span data-ttu-id="6dcd4-126">Erstellen eines Marketingprofils</span><span class="sxs-lookup"><span data-stu-id="6dcd4-126">Create a profile.</span></span> <span data-ttu-id="6dcd4-127">Klicken Sie auf **Feature hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="6dcd4-127">Click **Add a profile**.</span></span>
- <span data-ttu-id="6dcd4-128">Verwalten Sie Ihre Profile.</span><span class="sxs-lookup"><span data-stu-id="6dcd4-128">Manage your profiles.</span></span> <span data-ttu-id="6dcd4-129">Klicken Sie auf **Profileinstellungen verwalten**.</span><span class="sxs-lookup"><span data-stu-id="6dcd4-129">Click **Manage profile settings**.</span></span>

<span data-ttu-id="6dcd4-130">Diese Unterstützung ist auf allen Plattformen verfügbar, einschließlich aller unterstützten Versionen von Windows und macOS.</span><span class="sxs-lookup"><span data-stu-id="6dcd4-130">This support is available across all platforms, including all supported versions of Windows and macOS.</span></span>

### <span data-ttu-id="6dcd4-131">So stellen Sie den bedingten Zugriff in Azure Active Directory bereit</span><span class="sxs-lookup"><span data-stu-id="6dcd4-131">How to deploy Conditional Access in Azure Active Directory</span></span>

<span data-ttu-id="6dcd4-132">[Bereitstellen des bedingten Zugriffs](https://docs.microsoft.com/azure/active-directory/conditional-access/plan-conditional-access) enthält eine ausführliche Anleitung zur Bereitstellung des bedingten Zugriffs in Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6dcd4-132">[Deploy Conditional Access](https://docs.microsoft.com/azure/active-directory/conditional-access/plan-conditional-access) provides a detailed guide to help deploy Conditional Access in Azure Active Directory.</span></span>

## <span data-ttu-id="6dcd4-133">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6dcd4-133">See also</span></span>

- [<span data-ttu-id="6dcd4-134">Microsoft Edge Enterprise-Angebotsseite</span><span class="sxs-lookup"><span data-stu-id="6dcd4-134">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="6dcd4-135">Video: Sicherheit, Kompatibilität und Verwaltbarkeit</span><span class="sxs-lookup"><span data-stu-id="6dcd4-135">Video: Security, compatibility, and manageability</span></span>](/microsoft-edge-video-security-compatibility-manageability.md)
