---
title: Konfigurieren der Microsoft Edge Enterprise-Synchronisierung
ms.author: scottbo
author: dan-wesley
manager: silvanam
ms.date: 03/08/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Administrator- und Benutzeroptionen zum Konfigurieren von Microsoft Edge zum Synchronisieren von Favoriten, Kennwörtern und anderen Browserdaten.
ms.openlocfilehash: bfaa1db297093d0b0655a8d217aefcd59d11ac5e
ms.sourcegitcommit: 86e0de9b27ad4297a6d5a57c866d7ef4fc7bb0cd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "11400139"
---
# <a name="configure-microsoft-edge-enterprise-sync"></a><span data-ttu-id="7d402-103">Konfigurieren der Microsoft Edge Enterprise-Synchronisierung</span><span class="sxs-lookup"><span data-stu-id="7d402-103">Configure Microsoft Edge enterprise sync</span></span>

<span data-ttu-id="7d402-104">In diesem Artikel wird erläutert, wie Administratoren Microsoft Edge konfigurieren können, um Favoriten, Kennwörter und andere Browserdaten von Benutzern über alle angemeldeten Geräte hinweg zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="7d402-104">This article explains how admins can configure Microsoft Edge to sync user favorites, passwords, and other browser data across all signed-in devices.</span></span>

> [!NOTE]
> <span data-ttu-id="7d402-105">Gilt für Microsoft Edge Version 77 oder höher, sofern nicht anderes angegeben.</span><span class="sxs-lookup"><span data-stu-id="7d402-105">Applies to Microsoft Edge version 77 or later unless otherwise noted.</span></span>

## <a name="overview"></a><span data-ttu-id="7d402-106">Übersicht</span><span class="sxs-lookup"><span data-stu-id="7d402-106">Overview</span></span>

<span data-ttu-id="7d402-107">Dank der Microsoft Edge-Synchronisierung können Benutzer auf ihre Browserdaten über alle angemeldeten Geräte hinweg zugreifen.</span><span class="sxs-lookup"><span data-stu-id="7d402-107">Microsoft Edge sync enables users to access their browsing data across all their signed-in devices.</span></span> <span data-ttu-id="7d402-108">Zu den von der Synchronisierung unterstützten Daten gehören:</span><span class="sxs-lookup"><span data-stu-id="7d402-108">The data supported by sync includes:</span></span>

- <span data-ttu-id="7d402-109">Favoriten</span><span class="sxs-lookup"><span data-stu-id="7d402-109">Favorites</span></span>
- <span data-ttu-id="7d402-110">Kennwörter</span><span class="sxs-lookup"><span data-stu-id="7d402-110">Passwords</span></span>
- <span data-ttu-id="7d402-111">Adressen und mehr (Formulareinträge)</span><span class="sxs-lookup"><span data-stu-id="7d402-111">Addresses and more (form-fill)</span></span>
- <span data-ttu-id="7d402-112">Sammlungen</span><span class="sxs-lookup"><span data-stu-id="7d402-112">Collections</span></span>
- <span data-ttu-id="7d402-113">Einstellungen</span><span class="sxs-lookup"><span data-stu-id="7d402-113">Settings</span></span>
- <span data-ttu-id="7d402-114">Erweiterung</span><span class="sxs-lookup"><span data-stu-id="7d402-114">Extension</span></span>
- <span data-ttu-id="7d402-115">Geöffnete Registerkarten (verfügbar in Microsoft Edge, Version 88)</span><span class="sxs-lookup"><span data-stu-id="7d402-115">Open tabs (available in Microsoft Edge version 88)</span></span>
- <span data-ttu-id="7d402-116">Verlauf (verfügbar in Microsoft Edge, Version 88)</span><span class="sxs-lookup"><span data-stu-id="7d402-116">History (available in Microsoft Edge version 88)</span></span>

<span data-ttu-id="7d402-117">Die Synchronisierungsfunktion wird nach Zustimmung des Benutzers aktiviert, und Benutzer können die Synchronisierung für die beiden oben aufgeführten Datentypen aktivieren oder deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="7d402-117">Sync functionality is enabled via user consent and users can turn sync on or off for each of the data types listed above.</span></span> <span data-ttu-id="7d402-118">Wenn ein Benutzer ein Synchronisierungsproblem hat, muss er möglicherweise die Synchronisierung unter **Einstellungen** > **Profile** > **Synchronisierung zurücksetzen** zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="7d402-118">If a user is experiencing a sync issue they might need to reset sync in **Settings** > **Profiles** > **Reset sync**.</span></span>

> [!NOTE]
> <span data-ttu-id="7d402-119">Zusätzliche Geräteverbindungs- und Konfigurationsdaten (wie Gerätename, Marke und Modell) werden hochgeladen, um die Synchronisationsfunktionalität zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="7d402-119">Additional device connectivity and configuration data (such as device name, make and model) is uploaded to support sync functionality.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="7d402-120">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="7d402-120">Prerequisites</span></span>

<span data-ttu-id="7d402-121">Die Synchronisierung von Microsoft Edge für Azure Active Directory (Azure AD)-Konten ist für jedes der folgenden Abonnements verfügbar:</span><span class="sxs-lookup"><span data-stu-id="7d402-121">Microsoft Edge sync for Azure Active Directory (Azure AD) accounts is available for any of the following subscriptions:</span></span>

- <span data-ttu-id="7d402-122">Azure AD Premium (P1 oder P2)</span><span class="sxs-lookup"><span data-stu-id="7d402-122">Azure AD Premium (P1 or P2)</span></span>
- <span data-ttu-id="7d402-123">M365 Business Premium</span><span class="sxs-lookup"><span data-stu-id="7d402-123">M365 Business Premium</span></span>
- <span data-ttu-id="7d402-124">Office365E1 und höher</span><span class="sxs-lookup"><span data-stu-id="7d402-124">Office 365 E1 and above</span></span>
- <span data-ttu-id="7d402-125">Azure Information Protection (AIP) (P1 oder P2)</span><span class="sxs-lookup"><span data-stu-id="7d402-125">Azure Information Protection (AIP) (P1 or P2)</span></span>
- <span data-ttu-id="7d402-126">Alle EDU-Abonnements (Microsoft Apps für Studenten oder Dozenten, Exchange Online für Studenten oder Dozenten, O365 A1 oder höher, M365 A1 oder höher oder Azure Information Protection P1 oder P2 für Studenten oder Dozenten)</span><span class="sxs-lookup"><span data-stu-id="7d402-126">All EDU subscriptions (Microsoft Apps for Students or Faculty, Exchange Online for Students or Faculty, O365 A1 or above, M365 A1 or above, or Azure Information Protection P1 or P2 for Students or Faculty)</span></span>

## <a name="sync-group-policies"></a><span data-ttu-id="7d402-127">Synchronisieren von Gruppenrichtlinien</span><span class="sxs-lookup"><span data-stu-id="7d402-127">Sync group policies</span></span>

<span data-ttu-id="7d402-128">Administratoren können die folgenden Gruppenrichtlinien verwenden, um die Microsoft Edge-Synchronisierung zu konfigurieren und zu verwalten:</span><span class="sxs-lookup"><span data-stu-id="7d402-128">Admins can use the following group policies to configure and manage Microsoft Edge sync:</span></span>

- <span data-ttu-id="7d402-129">[SyncDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled): Deaktiviert die Synchronisierung vollständig.</span><span class="sxs-lookup"><span data-stu-id="7d402-129">[SyncDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled): Disables sync completely.</span></span>
- <span data-ttu-id="7d402-130">[SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled): Deaktiviert das Speichern des Browserverlaufs und die Synchronisierung. Die Synchronisierung geöffneter Registerkarten wird durch diese Richtlinie ebenfalls deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="7d402-130">[SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled): Disables saving browsing history and sync. This policy also disables open-tabs sync.</span></span>
- <span data-ttu-id="7d402-131">[AllowDeletingBrowserHistory](https://docs.microsoft.com/deployedge/microsoft-edge-policies#allowdeletingbrowserhistory): Wenn diese Richtlinie deaktiviert ist, wird auch die Verlaufsdatensynchronisierung deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="7d402-131">[AllowDeletingBrowserHistory](https://docs.microsoft.com/deployedge/microsoft-edge-policies#allowdeletingbrowserhistory): When this policy is set to disabled, history sync will also be disabled.</span></span>
- <span data-ttu-id="7d402-132">[SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled): Konfigurieren Sie die Liste der Typen, die von der Synchronisierung ausgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="7d402-132">[SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled): Configure the list of types that are excluded from synchronization.</span></span>
- <span data-ttu-id="7d402-133">[RoamingProfileSupportEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilesupportenabled): Zulassen, dass Active Directory (AD)-Profile lokalen Speicher verwenden.</span><span class="sxs-lookup"><span data-stu-id="7d402-133">[RoamingProfileSupportEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilesupportenabled): Allow Active Directory (AD) profiles to use on-premises storage.</span></span> <span data-ttu-id="7d402-134">Weitere Informationen finden Sie unter [Lokale Synchronisierung für Active Directory (AD)-Benutzer](https://docs.microsoft.com/DeployEdge/microsoft-edge-on-premises-sync).</span><span class="sxs-lookup"><span data-stu-id="7d402-134">For more information, see [On-premises sync for Active Directory (AD) users](https://docs.microsoft.com/DeployEdge/microsoft-edge-on-premises-sync).</span></span>
- <span data-ttu-id="7d402-135">[ForceSync]( https://docs.microsoft.com/deployedge/microsoft-edge-policies#forcesync): Aktivieren Sie die Synchronisierung standardmäßig, und fordern Sie keine Benutzerzustimmung zur Synchronisierung an.</span><span class="sxs-lookup"><span data-stu-id="7d402-135">[ForceSync]( https://docs.microsoft.com/deployedge/microsoft-edge-policies#forcesync): Turn on sync by default and do not require user consent to sync.</span></span>  

## <a name="configure-microsoft-edge-sync"></a><span data-ttu-id="7d402-136">Konfigurieren der Microsoft Edge-Synchronisierung</span><span class="sxs-lookup"><span data-stu-id="7d402-136">Configure Microsoft Edge sync</span></span>

<span data-ttu-id="7d402-137">Konfigurationsoptionen für die Microsoft Edge-Synchronisierung stehen über den Azure Information Protection (AIP)-Dienst zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="7d402-137">Configuration options for Microsoft Edge sync are available through the Azure Information Protection (AIP) service.</span></span> <span data-ttu-id="7d402-138">Wenn AIP für einen Mandanten aktiviert ist, können alle Benutzer Microsoft Edge-Daten unabhängig von der Lizenzierung synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="7d402-138">When AIP is enabled for a tenant, all users can sync Microsoft Edge data, regardless of licensing.</span></span> <span data-ttu-id="7d402-139">Anweisungen zum Aktivieren von AIP finden Sie [hier](https://docs.microsoft.com/azure/information-protection/activate-office365).</span><span class="sxs-lookup"><span data-stu-id="7d402-139">Instructions on how to enable AIP can be found [here](https://docs.microsoft.com/azure/information-protection/activate-office365).</span></span>

<span data-ttu-id="7d402-140">Um die Synchronisierung auf eine bestimmte Benutzergruppe zu beschränken, können Sie die [AIP-Richtlinie zur Onboarding-Steuerung](https://docs.microsoft.com/powershell/module/aipservice/set-aipserviceonboardingcontrolpolicy?view=azureipps&preserve-view=true) für diese Benutzer aktivieren.</span><span class="sxs-lookup"><span data-stu-id="7d402-140">To restrict sync to certain set of users, you can enable the [AIP onboarding control policy](https://docs.microsoft.com/powershell/module/aipservice/set-aipserviceonboardingcontrolpolicy?view=azureipps&preserve-view=true) for those users.</span></span> <span data-ttu-id="7d402-141">Wenn die Synchronisierung immer noch nicht verfügbar ist, nachdem Sie sich vergewissert haben, dass das Onboarding für alle erforderlichen Benutzer erfolgt ist, stellen Sie mithilfe des PowerShell-Cmdlets [Get-AIPServiceIPCv3](https://docs.microsoft.com/powershell/module/aipservice/get-aipserviceipcv3?view=azureipps&preserve-view=true)  sicher, dass IPCv3Service aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="7d402-141">If sync is still not available after ensuring that all necessary users are onboarded, ensure that the IPCv3Service is enabled using the [Get-AIPServiceIPCv3](https://docs.microsoft.com/powershell/module/aipservice/get-aipserviceipcv3?view=azureipps&preserve-view=true)  PowerShell cmdlet.</span></span>

> [!CAUTION]
> <span data-ttu-id="7d402-142">Die Aktivierung von Azure Information Protection erlaubt auch anderen Anwendungen, wie z.B. Microsoft Word oder Microsoft Outlook, Inhalte mit AIP zu schützen.</span><span class="sxs-lookup"><span data-stu-id="7d402-142">Activating Azure Information Protection will also allow other applications, such as Microsoft Word or Microsoft Outlook, to protect content with AIP.</span></span> <span data-ttu-id="7d402-143">Darüber hinaus wird jede Onboarding-Kontrollrichtlinie, die zur Einschränkung der Microsoft Edge-Synchronisierung verwendet wird, auch andere Anwendungen daran hindern, Inhalte mithilfe von AIP zu schützen.</span><span class="sxs-lookup"><span data-stu-id="7d402-143">In addition, any onboarding control policy used to restrict Edge sync will also restrict other applications from protecting content using AIP.</span></span>

## <a name="microsoft-edge-and-enterprise-state-roaming-esr"></a><span data-ttu-id="7d402-144">Microsoft Edge und Enterprise State Roaming (ESR)</span><span class="sxs-lookup"><span data-stu-id="7d402-144">Microsoft Edge and Enterprise State Roaming (ESR)</span></span>

<span data-ttu-id="7d402-145">Microsoft Edge ist eine plattformübergreifende Anwendung mit erweiterten Möglichkeiten zur Synchronisierung von Benutzerdaten auf allen Geräten und ist nicht mehr Teil von Azure AD Enterprise State Roaming.</span><span class="sxs-lookup"><span data-stu-id="7d402-145">Microsoft Edge is a cross-platform application with an expanded scope for syncing user data across all their devices and is no longer a part of Azure AD Enterprise State Roaming.</span></span> <span data-ttu-id="7d402-146">Microsoft Edge erfüllt jedoch die Datenschutzversprechen von ESR, wie z. B. die Möglichkeit, einen eigenen Schlüssel zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="7d402-146">However, the Microsoft Edge will fulfill the data protection promises of ESR, such as the ability to bring your own key.</span></span> <span data-ttu-id="7d402-147">Weitere Informationen finden sie unter [Microsoft Edge und Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span><span class="sxs-lookup"><span data-stu-id="7d402-147">For more information, see [Microsoft Edge and Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="7d402-148">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7d402-148">See also</span></span>

- [<span data-ttu-id="7d402-149">Microsoft Edge Enterprise-Synchronisierung</span><span class="sxs-lookup"><span data-stu-id="7d402-149">Microsoft Edge Enterprise Sync</span></span>](microsoft-edge-enterprise-sync.md)
- [<span data-ttu-id="7d402-150">Diagnostizieren und Beheben von Microsoft Edge-Synchronisierungsproblemen</span><span class="sxs-lookup"><span data-stu-id="7d402-150">Diagnose and fix Microsoft Edge sync issues</span></span>](microsoft-edge-troubleshoot-enterprise-sync.md)
- [<span data-ttu-id="7d402-151">Microsoft Edge und Enterprise State Roaming</span><span class="sxs-lookup"><span data-stu-id="7d402-151">Microsoft Edge and Enterprise State Roaming</span></span>](microsoft-edge-enterprise-state-roaming.md)
- [<span data-ttu-id="7d402-152">Microsoft Edge Enterprise-Startseite</span><span class="sxs-lookup"><span data-stu-id="7d402-152">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
