---
title: Microsoft Edge Enterprise-Synchronisierung
ms.author: scottbo
author: dan-wesley
manager: silvanam
ms.date: 10/21/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Edge Enterprise-Synchronisierung
ms.openlocfilehash: e51346d9bab83228c42a84a7a14ee45dc9b463a7
ms.sourcegitcommit: b32d8d64ae65dc5a46e47b7c34b0211097a0cc65
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/21/2020
ms.locfileid: "11133130"
---
# <span data-ttu-id="1430d-103">Microsoft Edge Enterprise-Synchronisierung</span><span class="sxs-lookup"><span data-stu-id="1430d-103">Microsoft Edge Enterprise Sync</span></span>

<span data-ttu-id="1430d-104">In diesem Artikel wird erläutert, wie Sie mit Microsoft Edge Favoriten, Kennwörter und andere Browserdaten auf allen angemeldeten Geräten synchronisieren können.</span><span class="sxs-lookup"><span data-stu-id="1430d-104">This article explains how to use Microsoft Edge to sync your favorites, passwords, and other browser data across all your signed-in devices.</span></span>

> [!NOTE]
> <span data-ttu-id="1430d-105">Dieser Artikel bezieht sich auf Microsoft Edge Version 77 oder neuer.</span><span class="sxs-lookup"><span data-stu-id="1430d-105">This article applies to Microsoft Edge version 77 or later.</span></span>

## <span data-ttu-id="1430d-106">Übersicht</span><span class="sxs-lookup"><span data-stu-id="1430d-106">Overview</span></span>

<span data-ttu-id="1430d-107">Dank der Microsoft Edge-Synchronisierung können Benutzer auf ihre Browserdaten über alle angemeldeten Geräte hinweg zugreifen.</span><span class="sxs-lookup"><span data-stu-id="1430d-107">Microsoft Edge sync enables users to access their browsing data across all their signed-in devices.</span></span> <span data-ttu-id="1430d-108">Zu den von der Synchronisierung unterstützten Daten gehören:</span><span class="sxs-lookup"><span data-stu-id="1430d-108">The data supported by sync includes:</span></span>

- <span data-ttu-id="1430d-109">Favoriten</span><span class="sxs-lookup"><span data-stu-id="1430d-109">Favorites</span></span>
- <span data-ttu-id="1430d-110">Kennwörter</span><span class="sxs-lookup"><span data-stu-id="1430d-110">Passwords</span></span>
- <span data-ttu-id="1430d-111">Adressen und mehr (Formulareinträge)</span><span class="sxs-lookup"><span data-stu-id="1430d-111">Addresses and more (form-fill)</span></span>
- <span data-ttu-id="1430d-112">Sammlungen</span><span class="sxs-lookup"><span data-stu-id="1430d-112">Collections</span></span>
- <span data-ttu-id="1430d-113">Einstellungen</span><span class="sxs-lookup"><span data-stu-id="1430d-113">Settings</span></span>

<span data-ttu-id="1430d-114">Die Synchronisierungsfunktion wird nach Zustimmung des Benutzers aktiviert, und dieser kann die Synchronisierung für jeden der oben aufgeführten Datentypen aktivieren oder deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="1430d-114">Sync functionality is enabled via user consent and users can turn sync on or off for each of the data types listed above.</span></span>

> [!NOTE]
> <span data-ttu-id="1430d-115">Zusätzliche Geräteverbindungs- und Konfigurationsdaten (wie Gerätename, Marke und Modell) werden hochgeladen, um die Synchronisationsfunktionalität zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="1430d-115">Additional device connectivity and configuration data (such as device name, make and model) is uploaded to support sync functionality.</span></span>

## <span data-ttu-id="1430d-116">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="1430d-116">Prerequisites</span></span>

<span data-ttu-id="1430d-117">Die Synchronisierung von Microsoft Edge für Azure Active Directory (Azure AD)-Konten ist für jedes der folgenden Abonnements verfügbar:</span><span class="sxs-lookup"><span data-stu-id="1430d-117">Microsoft Edge sync for Azure Active Directory (Azure AD) accounts is available for any of the following subscriptions:</span></span>

- <span data-ttu-id="1430d-118">Azure AD Premium (P1 und P2)</span><span class="sxs-lookup"><span data-stu-id="1430d-118">Azure AD Premium (P1 and P2)</span></span>
- <span data-ttu-id="1430d-119">M365 Business Premium</span><span class="sxs-lookup"><span data-stu-id="1430d-119">M365 Business Premium</span></span>
- <span data-ttu-id="1430d-120">Office365 E1 und höher</span><span class="sxs-lookup"><span data-stu-id="1430d-120">Office 365 E1 and above</span></span>
- <span data-ttu-id="1430d-121">Azure Information Protection (AIP) (P1 & P2)</span><span class="sxs-lookup"><span data-stu-id="1430d-121">Azure Information Protection (AIP) (P1& P2)</span></span>
- <span data-ttu-id="1430d-122">Alle EDU-Abonnements (Microsoft Apps für Studenten oder Dozenten, Exchange Online für Studenten oder Dozenten, O365 A1 oder höher, M365 A1 oder höher oder Azure Information Protection P1 oder P2 für Studenten oder Dozenten)</span><span class="sxs-lookup"><span data-stu-id="1430d-122">All EDU subscriptions (Microsoft Apps for Students or Faculty, Exchange Online for Students or Faculty, O365 A1 or above, M365 A1 or above, or Azure Information Protection P1 or P2 for Students or Faculty)</span></span>

## <span data-ttu-id="1430d-123">Konfigurieren der Microsoft Edge-Synchronisierung</span><span class="sxs-lookup"><span data-stu-id="1430d-123">Configuring Microsoft Edge sync</span></span>

<span data-ttu-id="1430d-124">Konfigurationsoptionen für die Microsoft Edge-Synchronisierung stehen über den Azure Information Protection (AIP)-Dienst zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="1430d-124">Configuration options for Microsoft Edge sync are available through the Azure Information Protection (AIP) service.</span></span> <span data-ttu-id="1430d-125">Wenn AIP für einen Mandanten aktiviert ist, können alle Benutzer Microsoft Edge-Daten unabhängig von der Lizenzierung synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="1430d-125">When AIP is enabled for a tenant, all users can sync Microsoft Edge data, regardless of licensing.</span></span> <span data-ttu-id="1430d-126">Anweisungen zum Aktivieren von AIP finden Sie [hier](https://docs.microsoft.com/azure/information-protection/activate-office365).</span><span class="sxs-lookup"><span data-stu-id="1430d-126">Instructions on how to enable AIP can be found [here](https://docs.microsoft.com/azure/information-protection/activate-office365).</span></span>

<span data-ttu-id="1430d-127">Um die Synchronisierung auf eine bestimmte Benutzergruppe zu beschränken, können Sie die [AIP-Richtlinie zur Onboarding-Steuerung](https://docs.microsoft.com/powershell/module/aipservice/set-aipserviceonboardingcontrolpolicy?view=azureipps) für diese Benutzer aktivieren.</span><span class="sxs-lookup"><span data-stu-id="1430d-127">To restrict sync to certain set of users, you can enable the [AIP onboarding control policy](https://docs.microsoft.com/powershell/module/aipservice/set-aipserviceonboardingcontrolpolicy?view=azureipps) for those users.</span></span> <span data-ttu-id="1430d-128">Wenn die Synchronisierung immer noch nicht verfügbar ist, nachdem Sie sich vergewissert haben, dass das Onboarding für alle erforderlichen Benutzer erfolgt ist, stellen Sie mithilfe des PowerShell-Cmdlets [Get-AIPServiceIPCv3](https://docs.microsoft.com/powershell/module/aipservice/get-aipserviceipcv3?view=azureipps)  sicher, dass IPCv3Service aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="1430d-128">If sync is still not available after ensuring that all necessary users are onboarded, ensure that the IPCv3Service is enabled using the [Get-AIPServiceIPCv3](https://docs.microsoft.com/powershell/module/aipservice/get-aipserviceipcv3?view=azureipps)  PowerShell cmdlet.</span></span>

> [!CAUTION]
> <span data-ttu-id="1430d-129">Die Aktivierung von Azure Information Protection erlaubt auch anderen Anwendungen, wie z.B. Microsoft Word oder Microsoft Outlook, Inhalte mit AIP zu schützen.</span><span class="sxs-lookup"><span data-stu-id="1430d-129">Activating Azure Information Protection will also allow other applications, such as Microsoft Word or Microsoft Outlook, to protect content with AIP.</span></span> <span data-ttu-id="1430d-130">Darüber hinaus wird jede Onboarding-Kontrollrichtlinie, die zur Einschränkung der Edge-Synchronisierung verwendet wird, auch andere Anwendungen daran hindern, Inhalte mithilfe von AIP zu schützen.</span><span class="sxs-lookup"><span data-stu-id="1430d-130">In addition, any onboarding control policy used to restrict Edge sync will also restrict other applications from protecting content using AIP.</span></span>

## <span data-ttu-id="1430d-131">Microsoft Edge und Enterprise State Roaming</span><span class="sxs-lookup"><span data-stu-id="1430d-131">Microsoft Edge and Enterprise State Roaming</span></span>

<span data-ttu-id="1430d-132">Der neue Microsoft Edge ist eine plattformübergreifende Anwendung mit erweiterten Möglichkeiten zur Synchronisierung von Benutzerdaten auf allen Geräten und nicht mehr Teil von Azure AD Enterprise State Roaming.</span><span class="sxs-lookup"><span data-stu-id="1430d-132">The new Microsoft Edge is a cross-platform application with an expanded scope for syncing user data across all their devices and is no longer a part of Azure AD Enterprise State Roaming.</span></span> <span data-ttu-id="1430d-133">Das neue Microsoft Edge erfüllt jedoch die ESR-Datenschutzoptionen wie z.B. die Möglichkeit, einen eigenen Schlüssel zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="1430d-133">However, the new Microsoft Edge will fulfill the data protection promises of ESR, such as the ability to bring your own key.</span></span> <span data-ttu-id="1430d-134">Weitere Informationen finden sie unter [Microsoft Edge und Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span><span class="sxs-lookup"><span data-stu-id="1430d-134">For more information, see [Microsoft Edge and Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span></span>

## <span data-ttu-id="1430d-135">Synchronisierungs-Gruppenrichtlinien</span><span class="sxs-lookup"><span data-stu-id="1430d-135">Sync group policies</span></span>

<span data-ttu-id="1430d-136">Die folgenden Gruppenrichtlinien wirken sich auf die Microsoft Edge-Synchronisierung aus:</span><span class="sxs-lookup"><span data-stu-id="1430d-136">The following group policies impact Microsoft Edge sync:</span></span>

- <span data-ttu-id="1430d-137">[SyncDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled): Deaktiviert die Synchronisierung vollständig.</span><span class="sxs-lookup"><span data-stu-id="1430d-137">[SyncDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled): Disables sync completely.</span></span>
- <span data-ttu-id="1430d-138">[SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled): Deaktiviert das Speichern des Browserverlaufs und die Synchronisierung. Die Synchronisierung geöffneter Registerkarten wird durch diese Richtlinie ebenfalls deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="1430d-138">[SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled): Disables saving browsing history and sync. This policy also disables open-tabs sync.</span></span>
- <span data-ttu-id="1430d-139">[SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled): Konfigurieren Sie die Liste der Typen, die von der Synchronisierung ausgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="1430d-139">[SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled): Configure the list of types that are excluded from synchronization.</span></span>
- <span data-ttu-id="1430d-140">[RoamingProfileSupportEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilesupportenabled): Zulassen, dass Active Directory (AD)-Profile lokalen Speicher verwenden.</span><span class="sxs-lookup"><span data-stu-id="1430d-140">[RoamingProfileSupportEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilesupportenabled): Allow Active Directory (AD) profiles to use on-premises storage.</span></span> <span data-ttu-id="1430d-141">Weitere Informationen finden Sie unter [Lokale Synchronisierung für Active Directory (AD)-Benutzende](https://docs.microsoft.com/DeployEdge/microsoft-edge-on-premises-sync).</span><span class="sxs-lookup"><span data-stu-id="1430d-141">For more information, see [On-premises sync for Active Directory (AD) users](https://docs.microsoft.com/DeployEdge/microsoft-edge-on-premises-sync).</span></span>
- <span data-ttu-id="1430d-142">[ForceSync]( https://docs.microsoft.com/deployedge/microsoft-edge-policies#forcesync): Aktivieren Sie die Synchronisierung standardmäßig, und fordern Sie keine Benutzerzustimmung zur Synchronisierung an.</span><span class="sxs-lookup"><span data-stu-id="1430d-142">[ForceSync]( https://docs.microsoft.com/deployedge/microsoft-edge-policies#forcesync): Turn sync on by default and do not require user consent to sync.</span></span>  

## <span data-ttu-id="1430d-143">Häufig gestellte Fragen</span><span class="sxs-lookup"><span data-stu-id="1430d-143">Frequently Asked Questions</span></span>

### <span data-ttu-id="1430d-144">SICHERHEIT und von SERVER-/DATENKONFORMITÄT</span><span class="sxs-lookup"><span data-stu-id="1430d-144">SECURITY and SERVER/DATA COMPLIANCE</span></span>

#### <span data-ttu-id="1430d-145">Werden die synchronisierten Daten verschlüsselt?</span><span class="sxs-lookup"><span data-stu-id="1430d-145">Is the synced data encrypted?</span></span> 

<span data-ttu-id="1430d-146">Die Daten werden beim Transport mithilfe von TLS 1.2 oder höher verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="1430d-146">The data is encrypted in transport using TLS 1.2 or greater.</span></span> <span data-ttu-id="1430d-147">Die meisten Datentypen werden im Ruhezustand im Microsoft-Dienst zusätzlich mit AES256 verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="1430d-147">Most data types are additionally encrypted at rest in Microsoft's service using AES256.</span></span> 

#### <span data-ttu-id="1430d-148">Wo werden Microsoft Edge-Synchronisierungsdaten für gespeichert?</span><span class="sxs-lookup"><span data-stu-id="1430d-148">Where is Microsoft Edge sync data stored?</span></span>

<span data-ttu-id="1430d-149">Synchronisierte Daten für Azure AD-Konten werden auf sicheren Servern entsprechend der Mandanten-ID gespeichert.</span><span class="sxs-lookup"><span data-stu-id="1430d-149">Synced data for Azure AD accounts is stored in secure servers according to the tenant ID.</span></span> <span data-ttu-id="1430d-150">Beispielsweise werden die Daten eines in den USA registrierten Mandanten auf Servern gespeichert, die sich in dieser geografischen Region befinden, und verwenden die gleiche Speicherlösung wie Office-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="1430d-150">For example, the data for a tenant that is registered in the United States is stored in servers geo-located for that region and uses the same storage solution as Office applications.</span></span>

#### <span data-ttu-id="1430d-151">Verlassen die Daten jemals die Cloud von Microsoft, abgesehen von der Synchronisierung mit Microsoft Edge?</span><span class="sxs-lookup"><span data-stu-id="1430d-151">Does the data ever leave Microsoft's cloud, aside from syncing to Microsoft Edge?</span></span>

<span data-ttu-id="1430d-152">Nein.</span><span class="sxs-lookup"><span data-stu-id="1430d-152">No.</span></span>

#### <span data-ttu-id="1430d-153">Können Mandantenadministratoren ihren eigenen Schlüssel mitbringen?</span><span class="sxs-lookup"><span data-stu-id="1430d-153">Can tenant admins bring their own key?</span></span>

<span data-ttu-id="1430d-154">Ja, über [Azure Information Protection](https://azure.microsoft.com/services/information-protection/).</span><span class="sxs-lookup"><span data-stu-id="1430d-154">Yes, through [Azure Information Protection](https://azure.microsoft.com/services/information-protection/).</span></span>

#### <span data-ttu-id="1430d-155">Unter welche Nutzungsbedingungen fällt die Unternehmenssynchronisierung?</span><span class="sxs-lookup"><span data-stu-id="1430d-155">What terms of service does enterprise sync fall under?</span></span>

<span data-ttu-id="1430d-156">Die Nutzungsbedingungen sind die gleichen wie bei Ihrem Azure AD-Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1430d-156">The terms of service are the same terms as your Azure AD subscription.</span></span> <span data-ttu-id="1430d-157">Alle Nutzungsbedingungen von Azure AD fallen letztlich unter die [Onlinedienst-Vertragsbedingungen](https://www.microsoft.com/licensing/product-licensing/products) von Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1430d-157">All the Azure AD terms of service ultimately fall under Microsoft's [Online Service Terms](https://www.microsoft.com/licensing/product-licensing/products).</span></span>

#### <span data-ttu-id="1430d-158">Unterstützt Microsoft Edge Government Community Cloud (GCC) High-Compliance?</span><span class="sxs-lookup"><span data-stu-id="1430d-158">Does Microsoft Edge support Government Community Cloud (GCC) High compliance?</span></span>

<span data-ttu-id="1430d-159">Derzeit nicht.</span><span class="sxs-lookup"><span data-stu-id="1430d-159">Not today.</span></span> <span data-ttu-id="1430d-160">GCC High ist Tarifstufe D, während Microsoft Edge nur bis zur Tarifstufe C Unterstützung bietet.</span><span class="sxs-lookup"><span data-stu-id="1430d-160">GCC High is Tier D, while Microsoft Edge supports up to Tier C.</span></span>

### <span data-ttu-id="1430d-161">ANWENDEN DER SYNCHRONISIERUNG</span><span class="sxs-lookup"><span data-stu-id="1430d-161">APPLYING SYNC</span></span>

#### <span data-ttu-id="1430d-162">Was gilt für Kunden aus Unternehmen und dem Bildungsbereich, die sich für Microsoft Edge Legacy entscheiden?</span><span class="sxs-lookup"><span data-stu-id="1430d-162">What happens with enterprise and educational customers who decide to stay with Microsoft Edge Legacy?</span></span>

<span data-ttu-id="1430d-163">Die aktuelle Version des Microsoft Edge-Browsers ist weiterhin im ESR-Angebot verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1430d-163">The current version of Microsoft Edge browser will continue to participate in the ESR offering.</span></span>

#### <span data-ttu-id="1430d-164">Warum brauche ich ein Premium-Abonnement für Azure AD für die Synchronisierung?</span><span class="sxs-lookup"><span data-stu-id="1430d-164">Why do I need a premium Azure AD subscription to sync?</span></span>

<span data-ttu-id="1430d-165">Die Unternehmenssynchronisierung ist von Azure Information Protection abhängig, das nicht in allen Azure AD-Tarifstufen verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="1430d-165">Enterprise sync depends on Azure Information Protection, which is not available in all Azure AD tiers.</span></span>

#### <span data-ttu-id="1430d-166">Basiert die Microsoft Edge-Synchronisierung auf Enterprise State Roaming (ESR)?</span><span class="sxs-lookup"><span data-stu-id="1430d-166">Is Microsoft Edge sync based on Enterprise State Roaming?</span></span>

<span data-ttu-id="1430d-167">Nein.</span><span class="sxs-lookup"><span data-stu-id="1430d-167">No.</span></span> <span data-ttu-id="1430d-168">ESR kann verwendet werden, um die Synchronisierung zu aktivieren, aber Microsoft Edge-Synchronisierung ist nicht Teil von ESR.</span><span class="sxs-lookup"><span data-stu-id="1430d-168">ESR can be used to enable sync, but Microsoft Edge sync is not a part of ESR.</span></span> <span data-ttu-id="1430d-169">Weitere Informationen finden sie unter [Microsoft Edge-Synchronisierung](microsoft-edge-enterprise-sync.md) sowie [Microsoft Edge und Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span><span class="sxs-lookup"><span data-stu-id="1430d-169">For more information, see [Microsoft Edge Sync](microsoft-edge-enterprise-sync.md) and [Microsoft Edge and Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span></span>

#### <span data-ttu-id="1430d-170">Wird Microsoft Edge jemals die Synchronisierung zwischen Microsoft Edge und IE unterstützen?</span><span class="sxs-lookup"><span data-stu-id="1430d-170">Will Microsoft Edge ever support syncing between Microsoft Edge and IE?</span></span>

<span data-ttu-id="1430d-171">Es gibt keine Pläne, diese Synchronisierung zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="1430d-171">There are no plans to support this syncing.</span></span> <span data-ttu-id="1430d-172">Wenn Sie in Ihrer Umgebung noch IE zur Unterstützung von Legacyanwendungen benötigen, sollten Sie unseren [neuen IE-Modus](https://docs.microsoft.com/deployedge/edge-ie-mode) in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="1430d-172">If you still need IE in your environment to support legacy apps, consider our [new IE mode](https://docs.microsoft.com/deployedge/edge-ie-mode).</span></span>

#### <span data-ttu-id="1430d-173">Wird der neue Microsoft Edge-Browser mit der Vorgängerversion von Microsoft Edge synchronisiert?</span><span class="sxs-lookup"><span data-stu-id="1430d-173">Will the new Microsoft Edge browser sync with Microsoft Edge Legacy?</span></span>

<span data-ttu-id="1430d-174">Nein.</span><span class="sxs-lookup"><span data-stu-id="1430d-174">No, it won't.</span></span> <span data-ttu-id="1430d-175">Wir sind der Meinung, dass die Verbindung dieser beiden Ökosysteme zu Kompromissen bezüglich der Zuverlässigkeit der Synchronisation im neuen Microsoft Edge führen würde.</span><span class="sxs-lookup"><span data-stu-id="1430d-175">We believe connecting these two ecosystems will lead to compromises in the reliability of sync in the new Microsoft Edge.</span></span> <span data-ttu-id="1430d-176">Wir stellen sicher, dass vorhandene Daten zum neuen Microsoft Edge migriert werden.</span><span class="sxs-lookup"><span data-stu-id="1430d-176">We will ensure that existing data is migrated to the new Microsoft Edge.</span></span> <span data-ttu-id="1430d-177">Benutzer können zudem Daten aus dem Browser Ihrer Wahl importieren.</span><span class="sxs-lookup"><span data-stu-id="1430d-177">Users will also be able to import data from browser of their choice.</span></span> <span data-ttu-id="1430d-178">Dies bedeutet auch, dass der neue Microsoft Edge-Browser keine Möglichkeit für eine Synchronisierung mit dem IE bietet.</span><span class="sxs-lookup"><span data-stu-id="1430d-178">This also means that new Microsoft Edge browser won't have a way to sync with IE.</span></span>

### <span data-ttu-id="1430d-179">VERWALTEN DER SYNCHRONISIERUNG</span><span class="sxs-lookup"><span data-stu-id="1430d-179">MANAGING SYNC</span></span>

#### <span data-ttu-id="1430d-180">Kann ich verhindern, dass meine Benutzer mit einem persönlichen Mandanten synchronisiert werden?</span><span class="sxs-lookup"><span data-stu-id="1430d-180">Is it possible to stop my users from syncing with a personal tenant?</span></span>

<span data-ttu-id="1430d-181">Nicht direkt. Sie können jedoch mithilfe der Richtlinie [RestrictSigninToPattern](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern) festlegen, welche Profile sich bei Microsoft Edge anmelden können.</span><span class="sxs-lookup"><span data-stu-id="1430d-181">Not directly, but you can determine which profiles can sign on to Microsoft Edge using the [RestrictSigninToPattern](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern) policy.</span></span>

## <span data-ttu-id="1430d-182">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1430d-182">See also</span></span>

- [<span data-ttu-id="1430d-183">Angebotsseite für Microsoft Edge für Unternehmen</span><span class="sxs-lookup"><span data-stu-id="1430d-183">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="1430d-184">Microsoft Edge und Enterprise State Roaming</span><span class="sxs-lookup"><span data-stu-id="1430d-184">Microsoft Edge and Enterprise State Roaming</span></span>](microsoft-edge-enterprise-state-roaming.md)
