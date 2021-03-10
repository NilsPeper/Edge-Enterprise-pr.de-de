---
title: FAQ zur Microsoft Edge Enterprise-Synchronisierung
ms.author: scottbo
author: dan-wesley
manager: silvanam
ms.date: 03/08/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Häufig gestellte Fragen zur Microsoft Edge Enterprise-Synchronisierung.
ms.openlocfilehash: 51f6dfc4cd8f308815ee111c30d5501ec0e44f59
ms.sourcegitcommit: 86e0de9b27ad4297a6d5a57c866d7ef4fc7bb0cd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "11400192"
---
# <a name="microsoft-edge-enterprise-sync-faq"></a><span data-ttu-id="a05f1-103">FAQ zur Microsoft Edge Enterprise-Synchronisierung</span><span class="sxs-lookup"><span data-stu-id="a05f1-103">Microsoft Edge enterprise sync FAQ</span></span>

<span data-ttu-id="a05f1-104">In diesem Artikel finden Sie Antworten auf häufig gestellte Fragen zur Unternehmenssynchronisierung für Microsoft Edge, Version 77 oder höher.</span><span class="sxs-lookup"><span data-stu-id="a05f1-104">This article answers frequently asked questions about enterprise sync for Microsoft Edge version 77 or later.</span></span>

## <a name="security-and-serverdata-compliance"></a><span data-ttu-id="a05f1-105">Sicherheit und Server-/Datenkonformität</span><span class="sxs-lookup"><span data-stu-id="a05f1-105">Security and Server/Data Compliance</span></span>

### <a name="is-the-synced-data-encrypted"></a><span data-ttu-id="a05f1-106">Werden die synchronisierten Daten verschlüsselt?</span><span class="sxs-lookup"><span data-stu-id="a05f1-106">Is the synced data encrypted?</span></span>

<span data-ttu-id="a05f1-107">Die Daten werden beim Transport mithilfe von TLS 1.2 oder höher verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="a05f1-107">The data is encrypted in transport using TLS 1.2 or greater.</span></span> <span data-ttu-id="a05f1-108">Alle Datentypen werden im Ruhezustand im Microsoft-Dienst zusätzlich mit AES-128 verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="a05f1-108">All data types are additionally encrypted at rest in Microsoft's service using AES128.</span></span> <span data-ttu-id="a05f1-109">Alle Datentypen mit Ausnahme derjenigen, die für die Synchronisierung von geöffneten Registerkarten und Verlaufsdaten verwendet werden, werden mit über die [Azure Information Protection](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern)-Richtlinie verwalteten Schlüsseln zusätzlich verschlüsselt, bevor sie das Gerät des Benutzers verlassen.</span><span class="sxs-lookup"><span data-stu-id="a05f1-109">All data types except those used for open tab and history sync are additionally encrypted before leaving the user’s device with keys managed via the [Azure Information Protection](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern) policy.</span></span>

### <a name="why-dont-open-tab-and-history-data-have-more-client-side-encryption"></a><span data-ttu-id="a05f1-110">Warum haben die Daten von offenen Registerkarten und Verlaufsdaten nicht weitere clientseitige Verschlüsselung?</span><span class="sxs-lookup"><span data-stu-id="a05f1-110">Why don’t open tab and history data have more client-side encryption?</span></span>

<span data-ttu-id="a05f1-111">Um die Ressourcenauslastung auf Endbenutzergeräten zu verringern, werden Verlaufsdaten serverseitig basierend auf den Roaming-Daten der offenen Registerkarten generiert.</span><span class="sxs-lookup"><span data-stu-id="a05f1-111">To reduce resource utilization on end-user devices, history data is generated server-side based on open tab roaming data.</span></span> <span data-ttu-id="a05f1-112">Dieser Vorgang wäre bei clientseitiger Verschlüsselung dieser Daten nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="a05f1-112">This process would not be possible with client-side encryption of this data.</span></span> <span data-ttu-id="a05f1-113">Wenden Sie die Richtlinien [SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled) oder [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled) an, um die Synchronisierung von geöffneten Registerkarten und Verlaufsdaten zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="a05f1-113">To disable open tab and history sync, apply the [SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled) or [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled) policies.</span></span>

### <a name="can-tenant-admins-bring-their-own-key"></a><span data-ttu-id="a05f1-114">Können Mandantenadministratoren ihren eigenen Schlüssel mitbringen?</span><span class="sxs-lookup"><span data-stu-id="a05f1-114">Can tenant admins bring their own key?</span></span>

<span data-ttu-id="a05f1-115">Ja, über  [Azure Information Protection](https://azure.microsoft.com/services/information-protection/).</span><span class="sxs-lookup"><span data-stu-id="a05f1-115">Yes, through [Azure Information Protection](https://azure.microsoft.com/services/information-protection/).</span></span>

### <a name="where-is-microsoft-edge-sync-data-stored"></a><span data-ttu-id="a05f1-116">Wo werden Microsoft Edge-Synchronisierungsdaten für gespeichert?</span><span class="sxs-lookup"><span data-stu-id="a05f1-116">Where is Microsoft Edge sync data stored?</span></span>

<span data-ttu-id="a05f1-117">Synchronisierte Daten für Azure AD-Konten werden auf sicheren Servern entsprechend der Mandanten-ID gespeichert.</span><span class="sxs-lookup"><span data-stu-id="a05f1-117">Synced data for Azure AD accounts is stored in secure servers according to the tenant ID.</span></span> <span data-ttu-id="a05f1-118">Beispielsweise werden die Daten eines in den USA registrierten Mandanten auf Servern gespeichert, die sich in dieser geografischen Region befinden, und verwenden die gleiche Speicherlösung wie Office-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="a05f1-118">For example, the data for a tenant that is registered in the United States is stored in servers geo-located for that region and uses the same storage solution as Office applications.</span></span>

### <a name="does-the-data-ever-leave-microsofts-cloud-aside-from-syncing-to-microsoft-edge"></a><span data-ttu-id="a05f1-119">Verlassen die Daten jemals die Cloud von Microsoft, abgesehen von der Synchronisierung mit Microsoft Edge?</span><span class="sxs-lookup"><span data-stu-id="a05f1-119">Does the data ever leave Microsoft's cloud, aside from syncing to Microsoft Edge?</span></span>

<span data-ttu-id="a05f1-120">Nein.</span><span class="sxs-lookup"><span data-stu-id="a05f1-120">No.</span></span>

### <a name="what-terms-of-service-does-enterprise-sync-fall-under"></a><span data-ttu-id="a05f1-121">Unter welche Nutzungsbedingungen fällt die Unternehmenssynchronisierung?</span><span class="sxs-lookup"><span data-stu-id="a05f1-121">What terms of service does enterprise sync fall under?</span></span>

<span data-ttu-id="a05f1-122">Die Nutzungsbedingungen für die Microsoft Edge-Synchronisierung gehören zur Microsoft-Softwarelizenz, die in Microsoft Edge unter  *edge://terms* einsehbar ist.</span><span class="sxs-lookup"><span data-stu-id="a05f1-122">Terms of service for Microsoft Edge sync falls under the Microsoft software license viewable in Microsoft Edge at *edge://terms*.</span></span> <span data-ttu-id="a05f1-123">Ihr Abonnement und die Nutzungsbedingungen von Azure AD fallen letztlich unter die [Onlinedienst-Vertragsbedingungen](https://www.microsoft.com/licensing/product-licensing/products) von Microsoft Corporation.</span><span class="sxs-lookup"><span data-stu-id="a05f1-123">Your Azure AD subscription and terms of service ultimately fall under Microsoft's [Online Service Terms](https://www.microsoft.com/licensing/product-licensing/products).</span></span>

### <a name="does-microsoft-edge-support-government-community-cloud-gcc-high-compliance"></a><span data-ttu-id="a05f1-124">Unterstützt Microsoft Edge Government Community Cloud (GCC) High-Compliance?</span><span class="sxs-lookup"><span data-stu-id="a05f1-124">Does Microsoft Edge support Government Community Cloud (GCC) High compliance?</span></span>

<span data-ttu-id="a05f1-125">Derzeit nicht.</span><span class="sxs-lookup"><span data-stu-id="a05f1-125">Not today.</span></span> <span data-ttu-id="a05f1-126">Für Kunden in der GCC High-Cloud ist die Microsoft Edge-Synchronisierung deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="a05f1-126">For customers in the GCC High cloud, Microsoft Edge sync is disabled.</span></span>

## <a name="applying-sync"></a><span data-ttu-id="a05f1-127">Synchronisierung wird angewendet</span><span class="sxs-lookup"><span data-stu-id="a05f1-127">Applying Sync</span></span>

### <a name="why-isnt-microsoft-edge-sync-supported-in-all-m365-subscriptions"></a><span data-ttu-id="a05f1-128">Warum wird die Microsoft Edge-Synchronisierung nicht in allen M365-Abonnements unterstützt?</span><span class="sxs-lookup"><span data-stu-id="a05f1-128">Why isn’t Microsoft Edge sync supported in all M365 subscriptions?</span></span>

<span data-ttu-id="a05f1-129">Die Unternehmenssynchronisierung ist von [Azure Information Protection](https://azure.microsoft.com/services/information-protection/) abhängig, das nicht in allen M365-Abonnements verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="a05f1-129">Enterprise sync depends on [Azure Information Protection](https://azure.microsoft.com/services/information-protection/), which is not available in all M365 subscriptions.</span></span>

### <a name="is-microsoft-edge-sync-based-on-enterprise-state-roaming"></a><span data-ttu-id="a05f1-130">Basiert die Microsoft Edge-Synchronisierung auf Enterprise State Roaming (ESR)?</span><span class="sxs-lookup"><span data-stu-id="a05f1-130">Is Microsoft Edge sync based on Enterprise State Roaming?</span></span>

<span data-ttu-id="a05f1-131">Nein.</span><span class="sxs-lookup"><span data-stu-id="a05f1-131">No.</span></span> <span data-ttu-id="a05f1-132">ESR kann verwendet werden, um die Synchronisierung zu aktivieren, aber Microsoft Edge-Synchronisierung ist nicht Teil von ESR.</span><span class="sxs-lookup"><span data-stu-id="a05f1-132">ESR can be used to enable sync, but Microsoft Edge sync is not a part of ESR.</span></span> <span data-ttu-id="a05f1-133">Weitere Informationen finden sie unter [Microsoft Edge-Synchronisierung](https://review.docs.microsoft.com/DeployEdge/microsoft-edge-enterprise-sync) sowie [Microsoft Edge und Enterprise State Roaming](https://review.docs.microsoft.com/DeployEdge/microsoft-edge-enterprise-state-roaming).</span><span class="sxs-lookup"><span data-stu-id="a05f1-133">For more information, see [Microsoft Edge Sync](https://review.docs.microsoft.com/DeployEdge/microsoft-edge-enterprise-sync) and [Microsoft Edge and Enterprise State Roaming](https://review.docs.microsoft.com/DeployEdge/microsoft-edge-enterprise-state-roaming).</span></span>

### <a name="will-microsoft-edge-ever-support-syncing-between-microsoft-edge-and-ie"></a><span data-ttu-id="a05f1-134">Wird Microsoft Edge jemals die Synchronisierung zwischen Microsoft Edge und IE unterstützen?</span><span class="sxs-lookup"><span data-stu-id="a05f1-134">Will Microsoft Edge ever support syncing between Microsoft Edge and IE?</span></span>

<span data-ttu-id="a05f1-135">Es gibt keine Pläne, diese Synchronisierung zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="a05f1-135">There are no plans to support this syncing.</span></span> <span data-ttu-id="a05f1-136">Wenn Sie in Ihrer Umgebung noch IE zur Unterstützung von Legacyanwendungen benötigen, sollten Sie unseren [neuen IE-Modus](https://docs.microsoft.com/deployedge/edge-ie-mode) in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="a05f1-136">If you still need IE in your environment to support legacy apps, consider our [new IE mode](https://docs.microsoft.com/deployedge/edge-ie-mode).</span></span>

### <a name="will-microsoft-edge-sync-with-microsoft-edge-legacy"></a><span data-ttu-id="a05f1-137">Wird Microsoft Edge mit der Vorgängerversion von Microsoft Edge synchronisiert?</span><span class="sxs-lookup"><span data-stu-id="a05f1-137">Will Microsoft Edge sync with Microsoft Edge Legacy?</span></span>

<span data-ttu-id="a05f1-138">Nein.</span><span class="sxs-lookup"><span data-stu-id="a05f1-138">No, it won't.</span></span> <span data-ttu-id="a05f1-139">Wir sind der Meinung, dass die Verbindung dieser beiden Ökosysteme zu Kompromissen bezüglich der Zuverlässigkeit der Synchronisation in Microsoft Edge führen würde.</span><span class="sxs-lookup"><span data-stu-id="a05f1-139">We believe connecting these two ecosystems will lead to compromises in the reliability of sync in the Microsoft Edge.</span></span> <span data-ttu-id="a05f1-140">Wir stellen sicher, dass vorhandene Daten zu Microsoft Edge migriert werden.</span><span class="sxs-lookup"><span data-stu-id="a05f1-140">We will ensure that existing data is migrated to the Microsoft Edge.</span></span> <span data-ttu-id="a05f1-141">Benutzer werden auch in der Lage sein, Daten aus dem Browser ihrer Wahl zu importieren. Dies bedeutet, dass Microsoft Edge keine Möglichkeit zur Synchronisierung mit IE haben wird.</span><span class="sxs-lookup"><span data-stu-id="a05f1-141">Users will also be able to import data from browser of their choice, which also means that Microsoft Edge won't have a way to sync with IE.</span></span>

## <a name="managing-sync"></a><span data-ttu-id="a05f1-142">Verwalten der Synchronisierung</span><span class="sxs-lookup"><span data-stu-id="a05f1-142">Managing Sync</span></span>

### <a name="is-it-possible-to-stop-my-users-from-syncing-with-a-personal-tenant"></a><span data-ttu-id="a05f1-143">Kann ich verhindern, dass meine Benutzer mit einem persönlichen Mandanten synchronisiert werden?</span><span class="sxs-lookup"><span data-stu-id="a05f1-143">Is it possible to stop my users from syncing with a personal tenant?</span></span>

<span data-ttu-id="a05f1-144">Nicht direkt. Sie können jedoch mithilfe der Richtlinie [RestrictSigninToPattern](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern) festlegen, welche Profile sich bei Microsoft Edge anmelden können.</span><span class="sxs-lookup"><span data-stu-id="a05f1-144">Not directly, but you can determine which profiles can sign on to Microsoft Edge using the [RestrictSigninToPattern](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern) policy.</span></span>

## <a name="see-also"></a><span data-ttu-id="a05f1-145">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a05f1-145">See also</span></span>

- [<span data-ttu-id="a05f1-146">Microsoft Edge Enterprise-Synchronisierung</span><span class="sxs-lookup"><span data-stu-id="a05f1-146">Microsoft Edge Enterprise Sync</span></span>](microsoft-edge-enterprise-sync.md)
- [<span data-ttu-id="a05f1-147">Microsoft Edge und Enterprise State Roaming</span><span class="sxs-lookup"><span data-stu-id="a05f1-147">Microsoft Edge and Enterprise State Roaming</span></span>](microsoft-edge-enterprise-state-roaming.md)
- [<span data-ttu-id="a05f1-148">Microsoft Edge Enterprise-Startseite</span><span class="sxs-lookup"><span data-stu-id="a05f1-148">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
