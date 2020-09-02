---
title: Microsoft Edge Enterprise-Synchronisierung
ms.author: scottbo
author: dan-wesley
manager: silvanam
ms.date: 08/03/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Edge Enterprise-Synchronisierung
ms.openlocfilehash: a6d01356db478871a7c6b386bbb731b32dc4739a
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/31/2020
ms.locfileid: "10980047"
---
# <span data-ttu-id="c595d-103">Microsoft Edge Enterprise-Synchronisierung</span><span class="sxs-lookup"><span data-stu-id="c595d-103">Microsoft Edge Enterprise Sync</span></span>

<span data-ttu-id="c595d-104">In diesem Artikel wird erläutert, wie Sie mit Microsoft Edge Favoriten, Kennwörter und andere Browserdaten auf allen angemeldeten Geräten synchronisieren können.</span><span class="sxs-lookup"><span data-stu-id="c595d-104">This article explains how to use Microsoft Edge to sync your favorites, passwords, and other browser data across all your signed-in devices.</span></span>

> [!NOTE]
> <span data-ttu-id="c595d-105">Dieser Artikel bezieht sich auf Microsoft Edge Version 77 oder neuer.</span><span class="sxs-lookup"><span data-stu-id="c595d-105">This article applies to Microsoft Edge version 77 or later.</span></span>

## <span data-ttu-id="c595d-106">Übersicht</span><span class="sxs-lookup"><span data-stu-id="c595d-106">Overview</span></span>

<span data-ttu-id="c595d-107">Dank der Microsoft Edge-Synchronisierung können Benutzer auf ihre Browserdaten über alle angemeldeten Geräte hinweg zugreifen.</span><span class="sxs-lookup"><span data-stu-id="c595d-107">Microsoft Edge sync enables users to access their browsing data across all their signed-in devices.</span></span> <span data-ttu-id="c595d-108">Zu den von der Synchronisierung unterstützten Daten gehören:</span><span class="sxs-lookup"><span data-stu-id="c595d-108">The data supported by sync includes:</span></span>

- <span data-ttu-id="c595d-109">Favoriten</span><span class="sxs-lookup"><span data-stu-id="c595d-109">Favorites</span></span>
- <span data-ttu-id="c595d-110">Kennwörter</span><span class="sxs-lookup"><span data-stu-id="c595d-110">Passwords</span></span>
- <span data-ttu-id="c595d-111">Adressen und mehr (Formulareinträge)</span><span class="sxs-lookup"><span data-stu-id="c595d-111">Addresses and more (form-fill)</span></span>
- <span data-ttu-id="c595d-112">Sammlungen</span><span class="sxs-lookup"><span data-stu-id="c595d-112">Collections</span></span>
- <span data-ttu-id="c595d-113">Einstellungen</span><span class="sxs-lookup"><span data-stu-id="c595d-113">Settings</span></span>

<span data-ttu-id="c595d-114">Die Synchronisierungsfunktion wird nach Zustimmung des Benutzers aktiviert, und dieser kann die Synchronisierung für jeden der oben aufgeführten Datentypen aktivieren oder deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="c595d-114">Sync functionality is enabled via user consent and users can turn sync on or off for each of the data types listed above.</span></span>

> [!NOTE]
> <span data-ttu-id="c595d-115">Zusätzliche Geräteverbindungs- und Konfigurationsdaten (wie Gerätename, Marke und Modell) werden hochgeladen, um die Synchronisationsfunktionalität zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="c595d-115">Additional device connectivity and configuration data (such as device name, make and model) is uploaded to support sync functionality.</span></span>

## <span data-ttu-id="c595d-116">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="c595d-116">Prerequisites</span></span>

<span data-ttu-id="c595d-117">Derzeit ist die Synchronisierung von Microsoft Edge für Azure Active Directory (Azure AD)-Konten für die folgenden Abonnements verfügbar:</span><span class="sxs-lookup"><span data-stu-id="c595d-117">Currently Microsoft Edge sync for Azure Active Directory (Azure AD) accounts is available for the following subscriptions:</span></span>

- <span data-ttu-id="c595d-118">Azure AD Premium (P1 und P2)</span><span class="sxs-lookup"><span data-stu-id="c595d-118">Azure AD Premium (P1 and P2)</span></span>
- <span data-ttu-id="c595d-119">M365 Business Premium</span><span class="sxs-lookup"><span data-stu-id="c595d-119">M365 Business Premium</span></span>
- <span data-ttu-id="c595d-120">Office 365 E3 und höher</span><span class="sxs-lookup"><span data-stu-id="c595d-120">Office 365 E3 and above</span></span>
- <span data-ttu-id="c595d-121">Azure Information Protection (AIP) (P1 & P2)</span><span class="sxs-lookup"><span data-stu-id="c595d-121">Azure Information Protection (AIP) (P1& P2)</span></span>
- <span data-ttu-id="c595d-122">Alle EDU-Abonnements (O365 A1 oder höher, M365 A1 oder höher oder Azure Information Protection P1 oder P2 für Studenten oder Dozenten)</span><span class="sxs-lookup"><span data-stu-id="c595d-122">All EDU subscriptions (O365 A1 or above, M365 A1 or above, or Azure Information Protection P1 or P2 for Students or Faculty)</span></span>

> [!NOTE]
> <span data-ttu-id="c595d-123">Die Synchronisierung ist abhängig von dem Schutzdienst, der von Azure Information Protection (AIP) zum Schutz der Synchronisationsdaten angeboten wird.</span><span class="sxs-lookup"><span data-stu-id="c595d-123">Sync has a dependency on the protection service offered by Azure Information Protection (AIP) to protect sync data.</span></span> <span data-ttu-id="c595d-124">Dieser Dienst ist derzeit für die zuvor genannten Abonnements verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c595d-124">This service is currently available to the preceding subscriptions.</span></span> <span data-ttu-id="c595d-125">Eine vollständige Liste der AIP-SKUs finden Sie unter [Preis für den Informationsschutz](https://azure.microsoft.com/pricing/details/information-protection/).</span><span class="sxs-lookup"><span data-stu-id="c595d-125">To see the full list of SKUs with AIP, see [Information Protection Pricing](https://azure.microsoft.com/pricing/details/information-protection/).</span></span>

## <span data-ttu-id="c595d-126">Konfigurationsoptionen für die Microsoft Edge-Synchronisierung</span><span class="sxs-lookup"><span data-stu-id="c595d-126">Configuration options for Microsoft Edge sync</span></span>

<span data-ttu-id="c595d-127">Die folgenden Konfigurationsoptionen stehen zur Aktivierung der Microsoft Edge-Synchronisierung zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="c595d-127">The following configuration options are available for enabling Microsoft Edge sync:</span></span>

- <span data-ttu-id="c595d-128">Azure Information Protection (AIP)</span><span class="sxs-lookup"><span data-stu-id="c595d-128">Azure Information Protection (AIP)</span></span>
- <span data-ttu-id="c595d-129">Azure AD Enterprise State Roaming (ESR)</span><span class="sxs-lookup"><span data-stu-id="c595d-129">Azure AD Enterprise State Roaming (ESR)</span></span>

<span data-ttu-id="c595d-130">Wenn sowohl AIP als auch ESR deaktiviert sind, wird Benutzern eine Fehlermeldung angezeigt, die besagt, dass die Synchronisierung für Ihr Konto nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="c595d-130">If both AIP and ESR are disabled, users will see an error message indicating that sync is not available for their account.</span></span>

### <span data-ttu-id="c595d-131">Azure Information Protection (AIP)</span><span class="sxs-lookup"><span data-stu-id="c595d-131">Azure Information Protection (AIP)</span></span>

<span data-ttu-id="c595d-132">Wenn der Azure Information Protection (AIP)-Dienst für einen Mandanten aktiviert ist, können alle Benutzer Microsoft Edge-Daten unabhängig von der Lizenzierung synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="c595d-132">If the Azure Information Protection (AIP) service is enabled for a tenant, all users can sync Microsoft Edge data, regardless of licensing.</span></span> <span data-ttu-id="c595d-133">Anweisungen zum Aktivieren von AIP finden Sie [hier](https://docs.microsoft.com/azure/information-protection/activate-office365).</span><span class="sxs-lookup"><span data-stu-id="c595d-133">Instructions on how to enable AIP can be found [here](https://docs.microsoft.com/azure/information-protection/activate-office365).</span></span>

<span data-ttu-id="c595d-134">Um die Synchronisierung auf eine bestimmte Benutzergruppe zu beschränken, können Sie die [AADRM-Richtlinie zur Onboarding-Steuerung](https://docs.microsoft.com/powershell/module/aadrm/set-aadrmonboardingcontrolpolicy?view=azureipps) für diese Benutzer aktivieren.</span><span class="sxs-lookup"><span data-stu-id="c595d-134">To restrict sync to certain set of users, you can enable the [AADRM onboarding control policy](https://docs.microsoft.com/powershell/module/aadrm/set-aadrmonboardingcontrolpolicy?view=azureipps) for those users.</span></span> <span data-ttu-id="c595d-135">Wenn die Synchronisierung immer noch nicht verfügbar ist, nachdem Sie sich vergewissert haben, dass das Onboarding für alle erforderlichen Benutzer erfolgt ist, Stellen Sie mithilfe des PowerShell-Cmdlets [Get-AIPServiceIPCv3](https://docs.microsoft.com/powershell/module/aipservice/Get-AipServiceIPCv3?view=azureipps) sicher, dass IPCv3Service aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="c595d-135">If sync is still not available after ensuring that all necessary users are onboarded, ensure that the IPCv3Service is enabled using the [Get-AIPServiceIPCv3](https://docs.microsoft.com/powershell/module/aipservice/Get-AipServiceIPCv3?view=azureipps) PowerShell cmdlet.</span></span>

> [!CAUTION]
> <span data-ttu-id="c595d-136">Die Aktivierung von Azure Information Protection schränkt auch den Zugriff für andere Anwendungen mit AIP ein, wie z.B. Microsoft Word oder Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="c595d-136">Activating Azure Information Protection will also restrict access for other applications using AIP, such as Microsoft Word or Microsoft Outlook.</span></span>

### <span data-ttu-id="c595d-137">Azure AD Enterprise State Roaming (ESR)</span><span class="sxs-lookup"><span data-stu-id="c595d-137">Azure AD Enterprise State Roaming (ESR)</span></span>

<span data-ttu-id="c595d-138">Wenn das Feature Azure Active Directory [Enterprise State Roaming](https://docs.microsoft.com/azure/active-directory/devices/enterprise-state-roaming-overview) (ESR) für jeden Benutzer oder Mandanten aktiviert ist, können diese die Microsoft Edge-Synchronisierungsfunktion unabhängig von der Einstellung der Onboarding-Steuerrichtlinie verwenden.</span><span class="sxs-lookup"><span data-stu-id="c595d-138">If the Azure Active Directory [Enterprise State Roaming](https://docs.microsoft.com/azure/active-directory/devices/enterprise-state-roaming-overview) (ESR) feature is enabled for any user or tenant, they can use the Microsoft Edge sync feature regardless of the onboarding control policy setting.</span></span>

## <span data-ttu-id="c595d-139">Microsoft Edge und Enterprise State Roaming</span><span class="sxs-lookup"><span data-stu-id="c595d-139">Microsoft Edge and Enterprise State Roaming</span></span>

<span data-ttu-id="c595d-140">Der neue Microsoft Edge ist eine plattformübergreifende Anwendung mit erweiterten Möglichkeiten zur Synchronisierung von Benutzerdaten auf allen Geräten und nicht mehr Teil von Azure AD Enterprise State Roaming.</span><span class="sxs-lookup"><span data-stu-id="c595d-140">The new Microsoft Edge is a cross-platform application with an expanded scope for syncing user data across all their devices and is no longer a part of Azure AD Enterprise State Roaming.</span></span> <span data-ttu-id="c595d-141">Das neue Microsoft Edge erfüllt jedoch die ESR-Datenschutzoptionen wie z.B. die Möglichkeit, einen eigenen Schlüssel zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="c595d-141">However, the new Microsoft Edge will fulfill the data protection promises of ESR, such as the ability to bring your own key.</span></span> <span data-ttu-id="c595d-142">Weitere Informationen finden sie unter [Microsoft Edge und Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span><span class="sxs-lookup"><span data-stu-id="c595d-142">For more information, see [Microsoft Edge and Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span></span>

## <span data-ttu-id="c595d-143">Synchronisierungs-Gruppenrichtlinien</span><span class="sxs-lookup"><span data-stu-id="c595d-143">Sync group policies</span></span>

<span data-ttu-id="c595d-144">Die folgenden Gruppenrichtlinien wirken sich auf die Microsoft Edge-Synchronisierung aus:</span><span class="sxs-lookup"><span data-stu-id="c595d-144">The following group policies impact Microsoft Edge sync:</span></span>

- <span data-ttu-id="c595d-145">[SyncDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled): Deaktiviert die Synchronisierung vollständig.</span><span class="sxs-lookup"><span data-stu-id="c595d-145">[SyncDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled): Disables sync completely.</span></span>
- <span data-ttu-id="c595d-146">[SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled): Deaktiviert das Speichern des Browserverlaufs und die Synchronisierung. Die Synchronisierung geöffneter Registerkarten wird durch diese Richtlinie ebenfalls deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="c595d-146">[SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled): Disables saving browsing history and sync. This policy also disables open-tabs sync.</span></span>
- <span data-ttu-id="c595d-147">[SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled): Konfigurieren Sie die Liste der Typen, die von der Synchronisierung ausgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="c595d-147">[SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled): Configure the list of types that are excluded from synchronization.</span></span>

## <span data-ttu-id="c595d-148">Häufig gestellte Fragen</span><span class="sxs-lookup"><span data-stu-id="c595d-148">Frequently Asked Questions</span></span>

### <span data-ttu-id="c595d-149">SICHERHEIT und von SERVER-/DATENKONFORMITÄT</span><span class="sxs-lookup"><span data-stu-id="c595d-149">SECURITY and SERVER/DATA COMPLIANCE</span></span>

#### <span data-ttu-id="c595d-150">Werden die synchronisierten Daten verschlüsselt?</span><span class="sxs-lookup"><span data-stu-id="c595d-150">Is the synced data encrypted?</span></span> 

<span data-ttu-id="c595d-151">Die Daten werden beim Transport mithilfe von TLS 1.2 oder höher verschlüsselt und zusätzlich im Ruhezustand im Microsoft-Dienst mithilfe von AES256.</span><span class="sxs-lookup"><span data-stu-id="c595d-151">The data is encrypted in transport using TLS 1.2 or greater, and additionally at rest in Microsoft's service using AES256.</span></span>

#### <span data-ttu-id="c595d-152">Wo werden Microsoft Edge-Synchronisierungsdaten für gespeichert?</span><span class="sxs-lookup"><span data-stu-id="c595d-152">Where is Microsoft Edge sync data stored?</span></span>

<span data-ttu-id="c595d-153">Synchronisierte Daten für Azure AD-Konten werden auf sicheren Servern entsprechend der Mandanten-ID gespeichert.</span><span class="sxs-lookup"><span data-stu-id="c595d-153">Synced data for Azure AD accounts is stored in secure servers according to the tenant ID.</span></span> <span data-ttu-id="c595d-154">Beispielsweise werden die Daten eines in den USA registrierten Mandanten auf Servern gespeichert, die sich in dieser geografischen Region befinden, und verwenden die gleiche Speicherlösung wie Office-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="c595d-154">For example, the data for a tenant that is registered in the United States is stored in servers geo-located for that region and uses the same storage solution as Office applications.</span></span>

#### <span data-ttu-id="c595d-155">Verlassen die Daten jemals die Cloud von Microsoft, abgesehen von der Synchronisierung mit Microsoft Edge?</span><span class="sxs-lookup"><span data-stu-id="c595d-155">Does the data ever leave Microsoft's cloud, aside from syncing to Microsoft Edge?</span></span>

<span data-ttu-id="c595d-156">Nein.</span><span class="sxs-lookup"><span data-stu-id="c595d-156">No.</span></span>

#### <span data-ttu-id="c595d-157">Können Mandantenadministratoren ihren eigenen Schlüssel mitbringen?</span><span class="sxs-lookup"><span data-stu-id="c595d-157">Can tenant admins bring their own key?</span></span>

<span data-ttu-id="c595d-158">Ja, über [Azure Information Protection](https://azure.microsoft.com/services/information-protection/).</span><span class="sxs-lookup"><span data-stu-id="c595d-158">Yes, through [Azure Information Protection](https://azure.microsoft.com/services/information-protection/).</span></span>

#### <span data-ttu-id="c595d-159">Unter welche Nutzungsbedingungen fällt die Unternehmenssynchronisierung?</span><span class="sxs-lookup"><span data-stu-id="c595d-159">What terms of service does enterprise sync fall under?</span></span>

<span data-ttu-id="c595d-160">Die Nutzungsbedingungen sind die gleichen wie bei Ihrem Azure AD-Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c595d-160">The terms of service are the same terms as your Azure AD subscription.</span></span> <span data-ttu-id="c595d-161">Alle Nutzungsbedingungen von Azure AD fallen letztlich unter die [Onlinedienst-Vertragsbedingungen](https://www.microsoft.com/licensing/product-licensing/products) von Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c595d-161">All the Azure AD terms of service ultimately fall under Microsoft's [Online Service Terms](https://www.microsoft.com/licensing/product-licensing/products).</span></span>

#### <span data-ttu-id="c595d-162">Unterstützt Microsoft Edge Government Community Cloud (GCC) High-Compliance?</span><span class="sxs-lookup"><span data-stu-id="c595d-162">Does Microsoft Edge support Government Community Cloud (GCC) High compliance?</span></span>

<span data-ttu-id="c595d-163">Derzeit nicht.</span><span class="sxs-lookup"><span data-stu-id="c595d-163">Not today.</span></span> <span data-ttu-id="c595d-164">GCC High ist Tarifstufe D, während Microsoft Edge nur bis zur Tarifstufe C Unterstützung bietet.</span><span class="sxs-lookup"><span data-stu-id="c595d-164">GCC High is Tier D, while Microsoft Edge supports up to Tier C.</span></span>

### <span data-ttu-id="c595d-165">ANWENDEN DER SYNCHRONISIERUNG</span><span class="sxs-lookup"><span data-stu-id="c595d-165">APPLYING SYNC</span></span>

#### <span data-ttu-id="c595d-166">Was gilt für Kunden aus Unternehmen und dem Bildungsbereich, die sich für Microsoft Edge Legacy entscheiden?</span><span class="sxs-lookup"><span data-stu-id="c595d-166">What happens with enterprise and educational customers who decide to stay with Microsoft Edge Legacy?</span></span>

<span data-ttu-id="c595d-167">Die aktuelle Version des Microsoft Edge-Browsers ist weiterhin im ESR-Angebot verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c595d-167">The current version of Microsoft Edge browser will continue to participate in the ESR offering.</span></span>

#### <span data-ttu-id="c595d-168">Warum brauche ich ein Premium-Abonnement für Azure AD für die Synchronisierung?</span><span class="sxs-lookup"><span data-stu-id="c595d-168">Why do I need a premium Azure AD subscription to sync?</span></span>

<span data-ttu-id="c595d-169">Die Unternehmenssynchronisierung ist von Azure Information Protection abhängig, das nicht in allen Azure AD-Tarifstufen verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="c595d-169">Enterprise sync depends on Azure Information Protection, which is not available in all Azure AD tiers.</span></span>

#### <span data-ttu-id="c595d-170">Basiert die Microsoft Edge-Synchronisierung auf Enterprise State Roaming (ESR)?</span><span class="sxs-lookup"><span data-stu-id="c595d-170">Is Microsoft Edge sync based on Enterprise State Roaming?</span></span>

<span data-ttu-id="c595d-171">Nein.</span><span class="sxs-lookup"><span data-stu-id="c595d-171">No.</span></span> <span data-ttu-id="c595d-172">ESR kann verwendet werden, um die Synchronisierung zu aktivieren, aber Microsoft Edge-Synchronisierung ist nicht Teil von ESR.</span><span class="sxs-lookup"><span data-stu-id="c595d-172">ESR can be used to enable sync, but Microsoft Edge sync is not a part of ESR.</span></span> <span data-ttu-id="c595d-173">Weitere Informationen finden sie unter [Microsoft Edge-Synchronisierung](microsoft-edge-enterprise-sync.md) sowie [Microsoft Edge und Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span><span class="sxs-lookup"><span data-stu-id="c595d-173">For more information, see [Microsoft Edge Sync](microsoft-edge-enterprise-sync.md) and [Microsoft Edge and Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span></span>

#### <span data-ttu-id="c595d-174">Wird Microsoft Edge jemals die Synchronisierung zwischen Microsoft Edge und IE unterstützen?</span><span class="sxs-lookup"><span data-stu-id="c595d-174">Will Microsoft Edge ever support syncing between Microsoft Edge and IE?</span></span>

<span data-ttu-id="c595d-175">Es gibt keine Pläne, diese Synchronisierung zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="c595d-175">There are no plans to support this syncing.</span></span> <span data-ttu-id="c595d-176">Wenn Sie in Ihrer Umgebung noch IE zur Unterstützung von Legacyanwendungen benötigen, sollten Sie unseren [neuen IE-Modus](https://docs.microsoft.com/deployedge/edge-ie-mode) in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="c595d-176">If you still need IE in your environment to support legacy apps, consider our [new IE mode](https://docs.microsoft.com/deployedge/edge-ie-mode).</span></span>

#### <span data-ttu-id="c595d-177">Wird der neue Microsoft Edge-Browser mit der Vorgängerversion von Microsoft Edge synchronisiert?</span><span class="sxs-lookup"><span data-stu-id="c595d-177">Will the new Microsoft Edge browser sync with Microsoft Edge Legacy?</span></span>

<span data-ttu-id="c595d-178">Nein.</span><span class="sxs-lookup"><span data-stu-id="c595d-178">No, it won't.</span></span> <span data-ttu-id="c595d-179">Wir sind der Meinung, dass die Verbindung dieser beiden Ökosysteme zu Kompromissen bezüglich der Zuverlässigkeit der Synchronisation im neuen Microsoft Edge führen würde.</span><span class="sxs-lookup"><span data-stu-id="c595d-179">We believe connecting these two ecosystems will lead to compromises in the reliability of sync in the new Microsoft Edge.</span></span> <span data-ttu-id="c595d-180">Wir stellen sicher, dass vorhandene Daten zum neuen Microsoft Edge migriert werden.</span><span class="sxs-lookup"><span data-stu-id="c595d-180">We will ensure that existing data is migrated to the new Microsoft Edge.</span></span> <span data-ttu-id="c595d-181">Benutzer können zudem Daten aus dem Browser Ihrer Wahl importieren.</span><span class="sxs-lookup"><span data-stu-id="c595d-181">Users will also be able to import data from browser of their choice.</span></span> <span data-ttu-id="c595d-182">Dies bedeutet auch, dass der neue Microsoft Edge-Browser keine Möglichkeit für eine Synchronisierung mit dem IE bietet.</span><span class="sxs-lookup"><span data-stu-id="c595d-182">This also means that new Microsoft Edge browser won't have a way to sync with IE.</span></span>

### <span data-ttu-id="c595d-183">VERWALTEN DER SYNCHRONISIERUNG</span><span class="sxs-lookup"><span data-stu-id="c595d-183">MANAGING SYNC</span></span>

#### <span data-ttu-id="c595d-184">Kann ich verhindern, dass meine Benutzer mit einem persönlichen Mandanten synchronisiert werden?</span><span class="sxs-lookup"><span data-stu-id="c595d-184">Is it possible to stop my users from syncing with a personal tenant?</span></span>

<span data-ttu-id="c595d-185">Nicht direkt. Sie können jedoch mithilfe der Richtlinie [RestrictSigninToPattern](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern) festlegen, welche Profile sich bei Microsoft Edge anmelden können.</span><span class="sxs-lookup"><span data-stu-id="c595d-185">Not directly, but you can determine which profiles can sign on to Microsoft Edge using the [RestrictSigninToPattern](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern) policy.</span></span>

## <span data-ttu-id="c595d-186">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c595d-186">See also</span></span>

- [<span data-ttu-id="c595d-187">Angebotsseite für Microsoft Edge für Unternehmen</span><span class="sxs-lookup"><span data-stu-id="c595d-187">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="c595d-188">Microsoft Edge und Enterprise State Roaming</span><span class="sxs-lookup"><span data-stu-id="c595d-188">Microsoft Edge and Enterprise State Roaming</span></span>](microsoft-edge-enterprise-state-roaming.md)
