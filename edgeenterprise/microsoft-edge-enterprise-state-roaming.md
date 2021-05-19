---
title: Microsoft Edge und Enterprise State Roaming
ms.author: kvice
author: dan-wesley
manager: laurawi
ms.date: 02/14/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Edge und Enterprise State Roaming
ms.openlocfilehash: 6090ecfda2f792d49e452771943bc6348066a3d8
ms.sourcegitcommit: 90b8eab62edbed0e0a84780abd7d3854bf95c130
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "11328057"
---
# <span data-ttu-id="88c4c-103">Microsoft Edge und Enterprise State Roaming</span><span class="sxs-lookup"><span data-stu-id="88c4c-103">Microsoft Edge and Enterprise State Roaming</span></span>

<span data-ttu-id="88c4c-104">Dieser Artikel erklärt, wie sich die Teilnahme von Microsoft Edge am Enterprise State Roaming (ESR)-Angebot ändert, um eine bessere Synchronisierung zwischen Plattformen und Geräten zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="88c4c-104">This article explains how Microsoft Edge participation in the Enterprise State Roaming (ESR) offering is changing to better support sync across platforms and devices.</span></span>

> [!NOTE]
> <span data-ttu-id="88c4c-105">Dieser Artikel bezieht sich auf Microsoft Edge Version 77 oder neuer.</span><span class="sxs-lookup"><span data-stu-id="88c4c-105">This article applies to Microsoft Edge version 77 or later.</span></span>

## <span data-ttu-id="88c4c-106">Einführung</span><span class="sxs-lookup"><span data-stu-id="88c4c-106">Introduction</span></span>

<span data-ttu-id="88c4c-107">Mit Windows 10 [Azure Active Directory (Azure AD)](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-whatis) haben Benutzer die Möglichkeit, ihre Benutzereinstellungen und Einstellungen der Anwendungsdaten in der Cloud sicher zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="88c4c-107">With Windows 10, [Azure Active Directory (Azure AD)](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-whatis) users gained the ability to securely synchronize their user settings and application settings data to the cloud.</span></span> <span data-ttu-id="88c4c-108">[Enterprise State Roaming (ESR)](https://docs.microsoft.com/azure/active-directory/devices/enterprise-state-roaming-overview) ermöglicht Benutzern eine einheitliche Erfahrung auf allen Windows-Geräten und verringert die benötigte Zeit für die Konfiguration eines neuen Geräts.</span><span class="sxs-lookup"><span data-stu-id="88c4c-108">[Enterprise State Roaming (ESR)](https://docs.microsoft.com/azure/active-directory/devices/enterprise-state-roaming-overview) provides users with a unified experience across their Windows devices and reduces the time needed for configuring a new device.</span></span>

<span data-ttu-id="88c4c-109">Durch die Übernahme der Chromium-Plattform ist die Synchronisierungslösung von Microsoft Edge nun vom Windows-Synchronisierungssystem getrennt.</span><span class="sxs-lookup"><span data-stu-id="88c4c-109">As part of Microsoft Edge adopting the Chromium platform, its sync solution is now disconnected from Windows sync framework.</span></span> <span data-ttu-id="88c4c-110">Dies wirkt sich auf die Beziehung zwischen Microsoft Edge und dem ESR-Angebot aus.</span><span class="sxs-lookup"><span data-stu-id="88c4c-110">This affects the relationship of Microsoft Edge to the ESR offering.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="88c4c-111">Die neue Microsoft Edge nimmt nicht am ESR-Angebot teil.</span><span class="sxs-lookup"><span data-stu-id="88c4c-111">The new Microsoft Edge does not participate in the ESR offering.</span></span>

## <span data-ttu-id="88c4c-112">Was ändert sich mit Microsoft Edge?</span><span class="sxs-lookup"><span data-stu-id="88c4c-112">What’s changing with Microsoft Edge?</span></span>

<span data-ttu-id="88c4c-113">Mit dem neuen Microsoft Edge ist die Synchronisierungslösung nicht an das Synchronisierungs-Ökosystem von Windows gebunden.</span><span class="sxs-lookup"><span data-stu-id="88c4c-113">With the new Microsoft Edge, the sync solution isn’t tied to Windows sync ecosystem.</span></span> <span data-ttu-id="88c4c-114">Dadurch können wir Microsoft Edge auf allen Plattformen anbieten, z. B. auf Windows 7, Windows 8 1, iOS, Android und macOS.</span><span class="sxs-lookup"><span data-stu-id="88c4c-114">This enables us to offer Microsoft Edge across all the platforms, such as Windows 7, Windows 8.1, iOS, Android and macOS.</span></span> <span data-ttu-id="88c4c-115">Zudem können wir Synchronisierung auch für nicht primäre Konten unter Windows anbieten.</span><span class="sxs-lookup"><span data-stu-id="88c4c-115">This also enables us to offer sync for non-primary accounts on Windows.</span></span> <span data-ttu-id="88c4c-116">Darüber hinaus können wir Microsoft Edge mit einer häufigeren und flexibleren Freigabekadenz als Windows ausliefern.</span><span class="sxs-lookup"><span data-stu-id="88c4c-116">In addition, we can ship Microsoft Edge at a more frequent and flexible release cadence than Windows.</span></span> <span data-ttu-id="88c4c-117">Weitere Informationen finden Sie unter [Windows-Updates zur Unterstützung der nächsten Version von Microsoft Edge](microsoft-edge-sysupdate-windows-updates.md).</span><span class="sxs-lookup"><span data-stu-id="88c4c-117">(For more information, see [Windows updates to support the next version of Microsoft Edge](microsoft-edge-sysupdate-windows-updates.md).</span></span> <span data-ttu-id="88c4c-118">Alle diese Faktoren führten zu der Notwendigkeit, die Teilnahme von Microsoft Edge am ESR-Angebot neu zu bewerten.</span><span class="sxs-lookup"><span data-stu-id="88c4c-118">All these factors highlighted the need to re-assess Microsoft Edge participation in the ESR offering.</span></span>

<span data-ttu-id="88c4c-119">ESR ist als Windows-Produktangebot für den Umgang mit Daten von Windows-Geräten konzipiert. Die Synchronisierung mit Microsoft Edge geht über Windows-Geräte hinaus.</span><span class="sxs-lookup"><span data-stu-id="88c4c-119">ESR is framed as a Windows product offering with promises about how data from Windows devices is handled, but Microsoft Edge sync will extend beyond Windows devices.</span></span> <span data-ttu-id="88c4c-120">Und da die Daten sich über diese Geräte verteilen, ist es schwierig, das Microsoft Edge-Synchronisierungsangebot im Rahmen von ESR zu definieren.</span><span class="sxs-lookup"><span data-stu-id="88c4c-120">And, as the data roams across these devices, it makes it difficult to define the Microsoft Edge sync offering in the context of ESR.</span></span> <span data-ttu-id="88c4c-121">Um Funktionsweise und Verwaltung der Synchronisierung zu vereinfachen und die hervorgehobenen Änderungen zu berücksichtigen, wurde beschlossen, Microsoft Edge aus dem ESR-Angebot herauszunehmen.</span><span class="sxs-lookup"><span data-stu-id="88c4c-121">To simplify how sync works and is managed, and to accommodate the changes that are highlighted, a decision was made to pull Microsoft Edge out of the ESR offering.</span></span>

## <span data-ttu-id="88c4c-122">Bedeutet dies, dass Unternehmen die Möglichkeiten verlieren, die Sie im Rahmen von ESR hatten?</span><span class="sxs-lookup"><span data-stu-id="88c4c-122">Does this mean Enterprises will lose the abilities they had as part of ESR?</span></span>

<span data-ttu-id="88c4c-123">Nein.</span><span class="sxs-lookup"><span data-stu-id="88c4c-123">No.</span></span> <span data-ttu-id="88c4c-124">Microsoft Edge wird weiterhin die meisten der im ESR-Angebot bereitgestellten Funktionen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="88c4c-124">Microsoft Edge will continue to support most of the abilities provided in the ESR offering.</span></span>

### <span data-ttu-id="88c4c-125">Einheitliche geräteübergreifende Erfahrung und Zeit für die Konfiguration neuer Geräte</span><span class="sxs-lookup"><span data-stu-id="88c4c-125">Unified experience across devices and new device configuration time</span></span>

<span data-ttu-id="88c4c-126">Wenn ein Benutzer mit einem Azure Active Directory (Azure AD-Konto) auf seinem Windows-Gerät angemeldet ist, erbt Microsoft Edge diese Identität beim ersten Start des neuen Browsers.</span><span class="sxs-lookup"><span data-stu-id="88c4c-126">When a user is signed into their windows device with an Azure Active Directory (Azure AD account), Microsoft Edge will implicitly inherit that Identity on first launch of the new browser.</span></span>

<span data-ttu-id="88c4c-127">Nachdem ein Benutzer ausdrücklich zugestimmt hat, die Synchronisierung im neuen Microsoft Edge einzuschalten, synchronisiert der Browser alle Browserdaten wie Favoriten, Passwörter und Verlauf.</span><span class="sxs-lookup"><span data-stu-id="88c4c-127">After a user has explicitly consented to turning on sync in the new Microsoft Edge, the browser will sync all the browser data, such as favorites, passwords, and history.</span></span> <span data-ttu-id="88c4c-128">Dies gewährleistet eine einheitliche Benutzererfahrung auf allen Geräten und reduziert den Zeitaufwand für die Personalisierung des Browsers.</span><span class="sxs-lookup"><span data-stu-id="88c4c-128">This ensures a unified experience across devices and reduces the time needed to personalize the browser.</span></span>

### <span data-ttu-id="88c4c-129">Trennung von Unternehmens- und Kundendaten</span><span class="sxs-lookup"><span data-stu-id="88c4c-129">Separation of corporate and consumer data</span></span>

<span data-ttu-id="88c4c-130">Unternehmen haben die Kontrolle über ihre Daten, und es gibt keine Vermischung mit Unternehmensdaten in einem Kunden-Cloudkonto oder mit Kundendaten in einem Unternehmens-Cloudkonto.</span><span class="sxs-lookup"><span data-stu-id="88c4c-130">Organizations are in control of their data, and there is no mixing of corporate data in a consumer cloud account or consumer data in an enterprise cloud account.</span></span>

### <span data-ttu-id="88c4c-131">Erhöhte Sicherheit</span><span class="sxs-lookup"><span data-stu-id="88c4c-131">Enhanced security</span></span>

<span data-ttu-id="88c4c-132">Daten werden automatisch über Azure Information Protection verschlüsselt, bevor sie das Windows 10-Gerät des Benutzers verlassen, und bleiben im Ruhezustand in der Cloud verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="88c4c-132">Data is automatically encrypted before leaving the user’s Windows 10 device by using Azure Information Protection, and data stays encrypted at rest in the cloud.</span></span> <span data-ttu-id="88c4c-133">Alle Inhalte bleiben in der Cloud im Ruhezustand verschlüsselt, mit Ausnahme der Namespaces, wie z. B. Einstellungsnamen.</span><span class="sxs-lookup"><span data-stu-id="88c4c-133">All content stays encrypted at rest in the cloud, except for the namespaces, like settings names.</span></span>

### <span data-ttu-id="88c4c-134">Überwachung</span><span class="sxs-lookup"><span data-stu-id="88c4c-134">Monitoring</span></span>

<span data-ttu-id="88c4c-135">Durch die Integration in das Azure AD-Portal bieten wir Kontrolle und Transparenz darüber, wer die Einstellungen in Ihrem Unternehmen synchronisiert und auf welchen Geräten dies erfolgt.</span><span class="sxs-lookup"><span data-stu-id="88c4c-135">We will provide control and visibility over who syncs settings in your organization and on which devices through integration with the Azure AD portal.</span></span> <span data-ttu-id="88c4c-136">Diese Funktion wird in einer zukünftigen Version aktiviert.</span><span class="sxs-lookup"><span data-stu-id="88c4c-136">This capability will be enabled in a future release.</span></span>

### <span data-ttu-id="88c4c-137">Verwaltung</span><span class="sxs-lookup"><span data-stu-id="88c4c-137">Management</span></span>

<span data-ttu-id="88c4c-138">Administratoren können festlegen, welche Mitglieder in Ihrer Organisation die Synchronisierung aktivieren können. Weitere Informationen finden sie unter [Konfigurieren von Microsoft Edge-Synchronisierung](microsoft-edge-enterprise-sync.md#configure-microsoft-edge-sync) und [Synchronisierungs-Gruppenrichtlinien](microsoft-edge-enterprise-sync.md#sync-group-policies).</span><span class="sxs-lookup"><span data-stu-id="88c4c-138">Admins will be able to control which members in your organization can enable sync. See [Configure Microsoft Edge sync](microsoft-edge-enterprise-sync.md#configure-microsoft-edge-sync) and [Sync group policies](microsoft-edge-enterprise-sync.md#sync-group-policies).</span></span> <span data-ttu-id="88c4c-139">Zudem können Benutzer die Synchronisierung für jedes Ihrer Geräte aktivieren/deaktivieren und jedes Datenattribut einzeln für die Synchronisierung umschalten.</span><span class="sxs-lookup"><span data-stu-id="88c4c-139">Additionally, users can turn sync on/off for each of their devices as well as toggle each data attribute individually for sync.</span></span>

### <span data-ttu-id="88c4c-140">Schlüsselverwaltung</span><span class="sxs-lookup"><span data-stu-id="88c4c-140">Key management</span></span>

<span data-ttu-id="88c4c-141">Das Synchronisierungsfeature nutzt Azure Information Protection (AIP), um die synchronisierten Daten nur für den Benutzer und die Unternehmensadministratoren zu schützen.</span><span class="sxs-lookup"><span data-stu-id="88c4c-141">The synchronization feature leverages Azure Information Protection (AIP) to protect the synchronized data for only the user and the enterprise admins.</span></span> <span data-ttu-id="88c4c-142">AIP unterstützt sowohl die Schlüsselverwaltung durch Microsoft (Standard) als auch die Verwendung Ihrer eigenen Schlüssel für die Cloud-Schlüsselverwaltung.</span><span class="sxs-lookup"><span data-stu-id="88c4c-142">AIP supports both Microsoft managed (default) and bring your own key for cloud-key management.</span></span> <span data-ttu-id="88c4c-143">Die von Ihrem Unternehmen verwendete Strategie zur Cloud-Schlüsselverwaltung ist für Microsoft Edge transparent und hat keinen Einfluss auf die Synchronisierungsfunktion.</span><span class="sxs-lookup"><span data-stu-id="88c4c-143">The cloud-key management strategy your organization uses is transparent to Microsoft Edge and has no impact on the synchronization feature.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="88c4c-144">[Hold your own key (HYOK)](https://docs.microsoft.com/azure/information-protection/configure-adrms-restrictions) und der Active Directory Rights Management Service werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="88c4c-144">[Hold your own key (HYOK)](https://docs.microsoft.com/azure/information-protection/configure-adrms-restrictions) and the Active Directory Rights Management Service aren't supported.</span></span>

## <span data-ttu-id="88c4c-145">Zusammenfassung der Synchronisierungsattribute</span><span class="sxs-lookup"><span data-stu-id="88c4c-145">Summary of sync attributes</span></span>

<span data-ttu-id="88c4c-146">Die folgenden Datenattribute werden in der neuen Version von Microsoft Edge beim ersten Start synchronisiert:</span><span class="sxs-lookup"><span data-stu-id="88c4c-146">The following data attributes will sync in the new version of Microsoft Edge at first launch:</span></span>

- <span data-ttu-id="88c4c-147">Favoriten</span><span class="sxs-lookup"><span data-stu-id="88c4c-147">Favorites</span></span>
- <span data-ttu-id="88c4c-148">Kennwörter</span><span class="sxs-lookup"><span data-stu-id="88c4c-148">Passwords</span></span>
- <span data-ttu-id="88c4c-149">Formularinhalte</span><span class="sxs-lookup"><span data-stu-id="88c4c-149">Form-fill</span></span>
- <span data-ttu-id="88c4c-150">Verlauf</span><span class="sxs-lookup"><span data-stu-id="88c4c-150">History</span></span>
- <span data-ttu-id="88c4c-151">Geöffnete Registerkarten (Sitzungen)</span><span class="sxs-lookup"><span data-stu-id="88c4c-151">Open tabs (sessions)</span></span>
- <span data-ttu-id="88c4c-152">Einstellungen (Voreinstellungen)</span><span class="sxs-lookup"><span data-stu-id="88c4c-152">Settings (preferences)</span></span>
- <span data-ttu-id="88c4c-153">Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="88c4c-153">Extensions</span></span>

<span data-ttu-id="88c4c-154">Die Attribute aus der obige Liste unterscheiden sich von denen, die in Microsoft Edge Legacy synchronisiert werden können.</span><span class="sxs-lookup"><span data-stu-id="88c4c-154">The preceding list of attributes is different than the attributes that could be synced in Microsoft Edge Legacy.</span></span> <span data-ttu-id="88c4c-155">(weitere Informationen zu Einstellungen für Microsoft Edge Legacy finden Sie unter [Roaming-Einstellungen für Windows 10](https://docs.microsoft.com/azure/active-directory/devices/enterprise-state-roaming-windows-settings-reference).) Benutzer können diese Attribute in den Microsoft Edge-Einstellungen einzeln aktivieren bzw. deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="88c4c-155">(For details about Microsoft Edge Legacy settings, see [Windows 10 roaming settings](https://docs.microsoft.com/azure/active-directory/devices/enterprise-state-roaming-windows-settings-reference).) Users can selectively enable/disable these attributes using Microsoft Edge settings.</span></span> <span data-ttu-id="88c4c-156">Aufgrund der unterschiedlichen Attribute in den beiden Versionen (z. B. Verlauf) werden Benutzer möglicherweise aufgefordert, die Zustimmung zur Synchronisierung erneut zu erteilen.</span><span class="sxs-lookup"><span data-stu-id="88c4c-156">Given the difference in attributes between the two versions (for example, history), users might be asked to give sync consent again.</span></span>

> [!NOTE]
> <span data-ttu-id="88c4c-157">Im Gegensatz zu Microsoft Edge Legacy verwendet das neue Microsoft Edge nicht die Windows-Anmeldeinformationsverwaltung für Kennwörter und synchronisiert diese daher nicht mit dem Internet Explorer oder anderen Anwendungen, die mit der Windows-Anmeldeinformationsverwaltung arbeiten.</span><span class="sxs-lookup"><span data-stu-id="88c4c-157">Unlike Microsoft Edge Legacy, the new Microsoft Edge doesn't use Windows credential Manager for passwords and as a result, won't sync passwords with Internet Explorer or other apps that use Windows Credential manager.</span></span>

## <span data-ttu-id="88c4c-158">Vertragsbedingungen</span><span class="sxs-lookup"><span data-stu-id="88c4c-158">Terms of service</span></span>

<span data-ttu-id="88c4c-159">Die Nutzungsbedingungen für die Microsoft Edge-Synchronisierung gehören zur Microsoft-Softwarelizenz, die in Microsoft Edge unter *edge://terms* einsehbar ist.</span><span class="sxs-lookup"><span data-stu-id="88c4c-159">Terms of service for Microsoft Edge sync falls under the Microsoft software license viewable in Microsoft Edge at *edge://terms*.</span></span>

## <span data-ttu-id="88c4c-160">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="88c4c-160">See also</span></span>

- [<span data-ttu-id="88c4c-161">Angebotsseite für Microsoft Edge für Unternehmen</span><span class="sxs-lookup"><span data-stu-id="88c4c-161">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="88c4c-162">Microsoft Edge-Synchronisierung</span><span class="sxs-lookup"><span data-stu-id="88c4c-162">Microsoft Edge Sync</span></span>](microsoft-edge-enterprise-sync.md)