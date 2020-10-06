---
title: Lokale Synchronisierung für Active Directory (AD)-Benutzende
ms.author: scottbo
author: dan-wesley
manager: silvanam
ms.date: 10/05/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Lokale Synchronisierung für Active Directory (AD)-Benutzende
ms.openlocfilehash: ce7fd912bc8cbd71e12444d58073e43df6b138db
ms.sourcegitcommit: bd68077356a944b99a424d03b444b04aa60272dd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/06/2020
ms.locfileid: "11099744"
---
# <span data-ttu-id="47330-103">Lokale Synchronisierung für Active Directory (AD)-Benutzende</span><span class="sxs-lookup"><span data-stu-id="47330-103">On-premises sync for Active Directory (AD) users</span></span>

<span data-ttu-id="47330-104">In diesem Artikel wird erläutert, wie Active Directory (AD)-Benutzende Microsoft Edge-Einstellungen und -Favoriten zwischen Computern übertragen können, ohne eine Verbindung zu Microsoft Cloud Services herzustellen.</span><span class="sxs-lookup"><span data-stu-id="47330-104">This article explains how Active Directory (AD) users can roam Microsoft Edge favorites and settings between computers without connecting to Microsoft cloud services.</span></span>

> [!NOTE]
> <span data-ttu-id="47330-105">Dieser Artikel bezieht sich auf Microsoft Edge Version 85 oder neuer.</span><span class="sxs-lookup"><span data-stu-id="47330-105">This article applies to Microsoft Edge version 85 or later.</span></span>

## <span data-ttu-id="47330-106">Einführung</span><span class="sxs-lookup"><span data-stu-id="47330-106">Introduction</span></span>

<span data-ttu-id="47330-107">Zum Synchronisieren von Benutzerdaten in Microsoft Edge sind in der Regel ein Microsoft-Konto oder ein Azure Active Directory-Konto (Azure AD) sowie eine Verbindung zu Microsoft Cloud Services erforderlich.</span><span class="sxs-lookup"><span data-stu-id="47330-107">Syncing user data in Microsoft Edge normally requires either a Microsoft Account or an Azure Active Directory (Azure AD) account, and a connection to Microsoft cloud services.</span></span> <span data-ttu-id="47330-108">Bei der lokalen Synchronisierung speichert Microsoft Edge die Favoriten und Einstellungen eines Active Directory-Benutzenden in einer Datei, die zwischen unterschiedlichen Computern verschoben werden kann.</span><span class="sxs-lookup"><span data-stu-id="47330-108">With on-premises sync, Microsoft Edge saves an Active Directory user's favorites and settings to a file that can be moved between different computers.</span></span> <span data-ttu-id="47330-109">Die lokale Synchronisierung wirkt sich nicht auf die Cloud-Synchronisierung für Profile aus, die dies zulassen.</span><span class="sxs-lookup"><span data-stu-id="47330-109">On-premises sync doesn't interfere with cloud syncing for those profiles that allow it.</span></span>

## <span data-ttu-id="47330-110">Funktionsweise</span><span class="sxs-lookup"><span data-stu-id="47330-110">How it works</span></span>

<span data-ttu-id="47330-111">Mit Microsoft Edge können Profile Active Directory (AD)-Konten zugeordnet werden, die bei der Cloud-Synchronisierung nicht verwendet werden können. Wenn die lokale Synchronisierung aktiviert ist, werden die Daten aus dem AD-Profil in einer Datei mit dem Namen "profile.pb" gespeichert.</span><span class="sxs-lookup"><span data-stu-id="47330-111">Microsoft Edge allows profiles to be associated with Active Directory (AD) accounts, which can't be used with cloud sync. When on-premises sync is enabled, the data from the AD profile is saved to a file named profile.pb.</span></span> <span data-ttu-id="47330-112">Diese Datei wird standardmäßig unter *%APPDATA%/Microsoft/Edge* gespeichert.</span><span class="sxs-lookup"><span data-stu-id="47330-112">By default, this file is stored in *%APPDATA%/Microsoft/Edge*.</span></span> <span data-ttu-id="47330-113">Nachdem diese Datei geschrieben wurde, kann sie zwischen verschiedenen Computern verschoben werden, und die Benutzerdaten werden auf jedem Computer ausgelesen bzw. geschrieben.</span><span class="sxs-lookup"><span data-stu-id="47330-113">After this file is written, it can be moved between different computers, and user data will be read and written on each computer.</span></span>

## <span data-ttu-id="47330-114">Verwenden der lokalen Synchronisierung</span><span class="sxs-lookup"><span data-stu-id="47330-114">Use on-premises sync</span></span>

<span data-ttu-id="47330-115">Um die lokale Synchronisierung verwenden zu können, müssen Sie sie aktivieren, ein Profil einem AD-Konto zuordnen und optional den Speicherort der Benutzerdaten ändern.</span><span class="sxs-lookup"><span data-stu-id="47330-115">To use on-premises sync, you have to enable it, associate a profile with an AD account, and optionally, change the location of the user data.</span></span>

### <span data-ttu-id="47330-116">Aktivieren der lokalen Synchronisierung</span><span class="sxs-lookup"><span data-stu-id="47330-116">Enable on-premises sync</span></span>

<span data-ttu-id="47330-117">Konfigurieren Sie zum Aktivieren der lokalen Synchronisierung in Microsoft Edge die Richtlinie [RoamingProfileSupportEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilesupportenabled).</span><span class="sxs-lookup"><span data-stu-id="47330-117">To enable on-premises sync in Microsoft Edge, configure the [RoamingProfileSupportEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilesupportenabled) policy.</span></span>

### <span data-ttu-id="47330-118">Stellen Sie sicher, dass ein Profil mit einem Active Directory-Konto verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="47330-118">Ensure that a profile is associated with an Active Directory account</span></span>

<span data-ttu-id="47330-119">Die lokale Synchronisierung funktioniert nur mit dem Profil, das mit einem Active Directory (AD)-Konto verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="47330-119">On-premises sync only works with the profile associated with an Active Directory (AD) account.</span></span> <span data-ttu-id="47330-120">Wenn kein solches Profil vorhanden ist, funktioniert die lokale Synchronisierung nicht.</span><span class="sxs-lookup"><span data-stu-id="47330-120">If no such profile exists, on-premises sync will not function.</span></span> <span data-ttu-id="47330-121">Um sicherzustellen, dass sich die Benutzer mit einem AD-Konto anmelden, konfigurieren Sie die Richtlinie [ConfigureOnPremisesAccountAutoSignIn](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configureonpremisesaccountautosignin).</span><span class="sxs-lookup"><span data-stu-id="47330-121">To ensure that users sign on with an AD account, configure the [ConfigureOnPremisesAccountAutoSignIn](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configureonpremisesaccountautosignin) policy.</span></span>

### <span data-ttu-id="47330-122">Ändern des Speicherorts der Benutzerdaten (optional)</span><span class="sxs-lookup"><span data-stu-id="47330-122">Change the location of the user data (optional)</span></span>

<span data-ttu-id="47330-123">Die Benutzerdaten werden standardmäßig in einer Datei namens **profile.pb** unter *%APPDATA%/Microsoft/Edge* gespeichert.</span><span class="sxs-lookup"><span data-stu-id="47330-123">By default, the user data is stored in a filed named **profile.pb** in *%APPDATA%/Microsoft/Edge*.</span></span> <span data-ttu-id="47330-124">Wenn Sie den Speicherort dieser Datei ändern möchten, konfigurieren Sie die Richtlinie [RoamingProfileLocation](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilelocation).</span><span class="sxs-lookup"><span data-stu-id="47330-124">To change the location of this file, configure the [RoamingProfileLocation](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilelocation) policy.</span></span>

## <span data-ttu-id="47330-125">Änderungen in der Benutzerumgebung, wenn die lokale Synchronisierung aktiviert ist</span><span class="sxs-lookup"><span data-stu-id="47330-125">Changes in the user experience when on-premises sync is enabled</span></span>

<span data-ttu-id="47330-126">Wenn die lokale Synchronisierung aktiviert ist, werden die Benutzer nicht aufgefordert, diese zu aktivieren. Darüber hinaus können die Benutzer die Synchronisierung in den Synchronisierungseinstellungen nicht deaktivieren, und sie können keine Synchronisierungstypen aktivieren, die von der lokalen Synchronisierung nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="47330-126">When on-premises sync is enabled, users won't be asked to enable sync. In addition, users can't turn off sync in Sync settings, and they can't turn on sync types that aren't supported by on-premises sync.</span></span>

## <span data-ttu-id="47330-127">Verwendungshinweise zur lokalen Synchronisierung</span><span class="sxs-lookup"><span data-stu-id="47330-127">On-premises sync usage notes</span></span>

### <span data-ttu-id="47330-128">Ausführen von Cloud-Synchronisierung und lokaler Synchronisierung auf demselben Computer</span><span class="sxs-lookup"><span data-stu-id="47330-128">Running cloud sync and on-premises sync on the same computer</span></span>

<span data-ttu-id="47330-129">Die lokale Synchronisierung stört nicht die Cloud-Synchronisierung. Wenn in Microsoft Edge mehrere Microsoft-Konten oder Azure Active Directory-Profile vorhanden sind, die mit der Cloud synchronisiert werden, werden diese Profile weiterhin synchronisiert, während die lokale Synchronisierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="47330-129">On-premises sync doesn't interfere with cloud sync. If Microsoft Edge has multiple Microsoft Account or Azure Active Directory profiles that sync to the cloud, these profiles will continue to sync while on-premises sync is enabled.</span></span>

### <span data-ttu-id="47330-130">Microsoft Edge auf mehreren Computern gleichzeitig auszuführen wird nicht empfohlen.</span><span class="sxs-lookup"><span data-stu-id="47330-130">Running Microsoft Edge on more than one computer at a time isn't recommended</span></span>

<span data-ttu-id="47330-131">Da für die lokale Synchronisierung eine Benutzerdatendatei zwischen Computern verschoben wird, werden bei der lokalen Synchronisierung keine Änderungen zwischen gleichzeitigen Sitzungen synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="47330-131">Because on-premises sync works by moving a user data file between computers, on-premises sync doesn't sync changes between simultaneous sessions.</span></span> <span data-ttu-id="47330-132">Aus diesem Grund funktioniert die lokale Synchronisierung am besten, wenn sie auf nicht mehr als einem Computer gleichzeitig verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="47330-132">For this reason, on-premises sync works best when used on one computer at a time.</span></span> <span data-ttu-id="47330-133">Wenn simultane lokale Sitzungen ausgeführt werden, werden Daten auf einem der Computer u. U. unerwartet von Daten von einem anderen Computer überschrieben, wenn Sie das nächste Mal eine Browsersitzung starten.</span><span class="sxs-lookup"><span data-stu-id="47330-133">If there are simultaneous on-premises sessions running, data on any of the computers may be unexpectedly overwritten by data from another computer the next time you start a browser session.</span></span>

> [!NOTE]
> <span data-ttu-id="47330-134">Microsoft Edge sperrt die **profile.pb**-Datei, wenn die lokale Synchronisierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="47330-134">Microsoft Edge locks the **profile.pb** file when on-premises sync is enabled.</span></span> <span data-ttu-id="47330-135">Wenn die Ordnerumleitung verwendet wird, um eine einzelne **profile.pb**-Datei zwischen verschiedenen Computern freizugeben, kann nur eine der Instanzen von Microsoft Edge gestartet werden, die diese Datei verwendet.</span><span class="sxs-lookup"><span data-stu-id="47330-135">If folder redirection is used to share a single **profile.pb** file between different computers, then only one instance of Microsoft Edge using that file can be started.</span></span>

### <span data-ttu-id="47330-136">Verwenden anderer Synchronisierungsrichtlinien mit der lokalen Synchronisierung</span><span class="sxs-lookup"><span data-stu-id="47330-136">Using other sync policies with on-premises sync</span></span>

<span data-ttu-id="47330-137">Die Richtlinie [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled) kann verwendet werden, um die Synchronisierung der Favoriten oder Einstellungen bei Bedarf selektiv zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="47330-137">The [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled) policy can be used to selectively disable either favorites or settings sync if desired.</span></span> <span data-ttu-id="47330-138">Wenn die Richtlinie [SyncDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#syncdisabled) aktiv ist, wird die lokale Synchronisierung ebenfalls deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="47330-138">If the [SyncDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#syncdisabled) policy is active, then on-premises sync is disabled as well.</span></span>  

## <span data-ttu-id="47330-139">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="47330-139">See also</span></span>

- [<span data-ttu-id="47330-140">Angebotsseite für Microsoft Edge für Unternehmen</span><span class="sxs-lookup"><span data-stu-id="47330-140">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="47330-141">Microsoft Edge und Enterprise State Roaming</span><span class="sxs-lookup"><span data-stu-id="47330-141">Microsoft Edge and Enterprise State Roaming</span></span>](microsoft-edge-enterprise-state-roaming.md)
- [<span data-ttu-id="47330-142">Microsoft Edge Enterprise-Synchronisierung</span><span class="sxs-lookup"><span data-stu-id="47330-142">Microsoft Edge Enterprise Sync</span></span>](microsoft-edge-enterprise-sync.md)
