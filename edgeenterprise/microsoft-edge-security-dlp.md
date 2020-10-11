---
title: Verhinderung von Datenverlust in Microsoft Edge
ms.author: archandr
author: dan-wesley
manager: seanlynd
ms.date: 10/08/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Verhinderung von Datenverlust (DLP) in Microsoft Edge
ms.openlocfilehash: 59c1b68c0526a49a2ee30283893707852514828d
ms.sourcegitcommit: 2af303fc97e8493024e2359fa2e8be162ab95a59
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/08/2020
ms.locfileid: "11104612"
---
# <span data-ttu-id="15ecb-103">Verhinderung von Datenverlust (DLP) in Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="15ecb-103">Data Loss Prevention (DLP) in Microsoft Edge</span></span>

<span data-ttu-id="15ecb-104">Die Verhinderung von Datenverlust (Data Loss Prevention, DLP) ist ein System von Technologien, die vertrauliche Unternehmensdaten erkennen und vor unbefugtem Zugriff schützen.</span><span class="sxs-lookup"><span data-stu-id="15ecb-104">Data loss prevention (DLP) is a system of technologies that identify and safeguard sensitive enterprise data from unauthorized disclosure.</span></span> <span data-ttu-id="15ecb-105">Die Unternehmen müssen vertrauliche Informationen schützen und deren nicht autorisierte Offenlegung verhindern, um den Unternehmensstandards und Branchenvorschriften zu entsprechen.</span><span class="sxs-lookup"><span data-stu-id="15ecb-105">To comply with business standards and industry regulations, organizations must protect sensitive information and prevent its unauthorized disclosure.</span></span> <span data-ttu-id="15ecb-106">Zu den vertraulichen Informationen gehören unter anderem Finanzdaten oder personenbezogene Informationen (PII) wie Kreditkartennummern, Sozialversicherungsnummern oder Krankenakten.</span><span class="sxs-lookup"><span data-stu-id="15ecb-106">Sensitive information includes financial data or personally identifiable information (PII) such as credit card numbers, social security numbers, or health records, among many other things.</span></span>

<span data-ttu-id="15ecb-107">Die Fernarbeit hat den Schwerpunkt auf die Verwendung von DLP verstärkt.</span><span class="sxs-lookup"><span data-stu-id="15ecb-107">Remote work has increased the emphasis on using DLP.</span></span> <span data-ttu-id="15ecb-108">Angesichts der zunehmenden Nutzung von persönlichen und geschäftlichen Aktivitäten auf Geräten sehen Unternehmen ein erhöhtes Risiko einer nicht autorisierten Freigabe von Unternehmensdaten außerhalb des Arbeitsplatzes.</span><span class="sxs-lookup"><span data-stu-id="15ecb-108">With the growing use of personal and work activities on devices, enterprises are seeing an increased risk of unauthorized sharing of corporate data outside the workplace.</span></span>

<span data-ttu-id="15ecb-109">Diese Kombination von Benutzeraktivitäten hat sich auch auf Geräte ausgebreitet, bei denen Daten zwischen privaten und unternehmensinternen Geräten über eine Vielzahl von öffentlichen und privaten Netzwerken verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="15ecb-109">This blending of user activities has spread to devices as well, where data is moved between personal and corporate devices over a variety of public and private networks.</span></span> <span data-ttu-id="15ecb-110">Das Ergebnis ist ein erheblich erhöhtes Risiko, vertrauliche Daten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="15ecb-110">The net result is a dramatically increased risk of exposing sensitive data.</span></span>

<span data-ttu-id="15ecb-111">Microsoft Edge unterstützt nativ zwei unterschiedliche DLP-Lösungen, Microsoft Endpoint DLP und Windows Information Protection (WIP).</span><span class="sxs-lookup"><span data-stu-id="15ecb-111">Microsoft Edge natively supports two different DLP solutions, Microsoft Endpoint DLP and Windows Information Protection (WIP).</span></span>

## <span data-ttu-id="15ecb-112">Microsoft Endpoint DLP</span><span class="sxs-lookup"><span data-stu-id="15ecb-112">Microsoft Endpoint DLP</span></span>

<span data-ttu-id="15ecb-113">Microsoft Endpoint DLP ist die nächste Generation von DLP, die moderne Konzepte wie datenbasierten Schutz verwendet.</span><span class="sxs-lookup"><span data-stu-id="15ecb-113">Microsoft Endpoint DLP is the next generation of DLP using modern concepts such as data-centric protection.</span></span> <span data-ttu-id="15ecb-114">Er ist in Windows 10 und Microsoft Edge integriert, sodass keine weiteren Agents oder Plugins auf dem Gerät erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="15ecb-114">It's  built-in to Windows 10 and Microsoft Edge so it doesn't need additional agents or plugins on the device.</span></span> <span data-ttu-id="15ecb-115">Weitere Informationen zu Endpunkt-DLP finden Sie unter [Informationen zum Microsoft 365-Endpunkt zur Verhinderung von Datenverlust](https://docs.microsoft.com/microsoft-365/compliance/endpoint-dlp-learn-about?view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="15ecb-115">To learn more about endpoint DLP, read [Learn about Microsoft 365 Endpoint data loss prevention](https://docs.microsoft.com/microsoft-365/compliance/endpoint-dlp-learn-about?view=o365-worldwide).</span></span>

> [!NOTE]
> <span data-ttu-id="15ecb-116">Dieser Artikel bezieht sich auf Microsoft Edge Version 85 oder neuer.</span><span class="sxs-lookup"><span data-stu-id="15ecb-116">This applies to Microsoft Edge version 85 or later.</span></span>

<span data-ttu-id="15ecb-117">Microsoft Edge erzwingt administratorenkonfigurierte Richtlinien für vertrauliche Dateien und zeichnet Überwachungsereignisse für nicht kompatible Aktivitäten auf.</span><span class="sxs-lookup"><span data-stu-id="15ecb-117">Microsoft Edge enforces admin configured policies for sensitive files and records audit events for non-compliant activities.</span></span>

<span data-ttu-id="15ecb-118">Einige der Benutzeraktivitäten, die Sie auf Geräten unter Windows 10 überwachen und verwalten können, umfassen die folgenden Aktivitäten:</span><span class="sxs-lookup"><span data-stu-id="15ecb-118">Some of the user activities that you can audit and manage on devices running Windows 10 include the following activities:</span></span>

- <span data-ttu-id="15ecb-119">Dateiupload: Schützen Sie den vertraulichen Dateiupload vor nicht autorisierten Cloud-Speicherorten.</span><span class="sxs-lookup"><span data-stu-id="15ecb-119">File Upload: Protect sensitive file upload to unauthorized cloud locations.</span></span> <span data-ttu-id="15ecb-120">Die nächsten drei Screenshots zeigen eine Reihenfolge, in der ein Benutzer versucht, eine vertrauliche Datendatei in den lokalen Speicher zu setzen.</span><span class="sxs-lookup"><span data-stu-id="15ecb-120">The next 3 screenshots show a sequence where a user tries to drop a sensitive data file on to their local storage.</span></span>
- <span data-ttu-id="15ecb-121">Schutz der Zwischenablage: Verhindern, dass vertrauliche Daten aus der Datei kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="15ecb-121">Clipboard Protection: Protect sensitive data from being copied out of the file.</span></span>
- <span data-ttu-id="15ecb-122">Druckschutz: Schützen vertraulicher Dateien, die gedruckt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="15ecb-122">Print Protection: Protect sensitive file from being printed.</span></span>
- <span data-ttu-id="15ecb-123">Auf USB/ Im Netzwerk speichern: Schützen vertraulicher Dateien vor dem Speichern in einem USB-Speicher oder nicht autorisierten Netzwerkspeicherorten.</span><span class="sxs-lookup"><span data-stu-id="15ecb-123">Save to USB/Network: Protect sensitive file from being saved to removable USB storage or unauthorized network locations.</span></span>

<span data-ttu-id="15ecb-124">Ausführlichere Informationen zu den Benutzeraktivitäten, die Sie überwachen und verwalten können, finden Sie unter [Endpunktaktivitäten, die Sie überwachen und entsprechende Maßnahmen ergreifen können](https://docs.microsoft.com/microsoft-365/compliance/endpoint-dlp-learn-about?view=o365-worldwide#endpoint-activities-you-can-monitor-and-take-action-on).</span><span class="sxs-lookup"><span data-stu-id="15ecb-124">For more detailed information about user activities you can audit and manage, see [Endpoint activities you can monitor and take action on](https://docs.microsoft.com/microsoft-365/compliance/endpoint-dlp-learn-about?view=o365-worldwide#endpoint-activities-you-can-monitor-and-take-action-on).</span></span>

## <span data-ttu-id="15ecb-125">Windows Information Protection</span><span class="sxs-lookup"><span data-stu-id="15ecb-125">Windows Information Protection</span></span>

<span data-ttu-id="15ecb-126">Lesen Sie [Support für Windows Information Protection](https://docs.microsoft.com/deployedge/microsoft-edge-security-windows-information-protection), in dem beschrieben wird, wie Microsoft Edge Windows Information Protection (WIP) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="15ecb-126">Check out [Support for Windows Information Protection](https://docs.microsoft.com/deployedge/microsoft-edge-security-windows-information-protection), which describes how Microsoft Edge supports Windows Information Protection (WIP).</span></span> <span data-ttu-id="15ecb-127">In den folgenden Abschnitten finden Sie Informationen zu den Systemanforderungen, den Vorteilen und den unterstützten Funktionen:</span><span class="sxs-lookup"><span data-stu-id="15ecb-127">You can learn moe about system requirements, benefits, and supported features in the following sections:</span></span>

- [<span data-ttu-id="15ecb-128">Systemanforderungen</span><span class="sxs-lookup"><span data-stu-id="15ecb-128">System Requirements</span></span>](https://docs.microsoft.com/deployedge/:microsoft-edge-security-windows-information-protection#system-requirements)
- [<span data-ttu-id="15ecb-129">Vorteile von Windows Information Protection</span><span class="sxs-lookup"><span data-stu-id="15ecb-129">Windows Information Protection Benefits</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-security-windows-information-protection#windows-information-protection-benefits)
- [<span data-ttu-id="15ecb-130">In Microsoft Edge unterstützte WIP-Features</span><span class="sxs-lookup"><span data-stu-id="15ecb-130">WIP features supported in Microsoft Edge</span></span>](https://docs.microsoft.com/DeployEdge/microsoft-edge-security-windows-information-protection#wip-features-supported-in-microsoft-edge)

## <span data-ttu-id="15ecb-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="15ecb-131">See also</span></span>

- [<span data-ttu-id="15ecb-132">Microsoft Edge Enterprise-Angebotsseite</span><span class="sxs-lookup"><span data-stu-id="15ecb-132">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="15ecb-133">Video: Verhinderung von Datenverlust in Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="15ecb-133">Video: Data loss prevention - Microsoft Edge</span></span>](https://www.youtube.com/watch?v=dLD04U9eTqg)
- [<span data-ttu-id="15ecb-134">Übersicht über die Verhinderung von Datenverlust</span><span class="sxs-lookup"><span data-stu-id="15ecb-134">Overview of data loss prevention</span></span>](https://docs.microsoft.com/microsoft-365/compliance/data-loss-prevention-policies?view=o365-worldwide)
- [<span data-ttu-id="15ecb-135">Schützen von Unternehmensdaten mithilfe von Windows Information Protection</span><span class="sxs-lookup"><span data-stu-id="15ecb-135">Protect your enterprise data using Windows Information Protection</span></span>](https://docs.microsoft.com/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip)
