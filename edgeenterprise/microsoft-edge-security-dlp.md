---
title: Verhinderung von Datenverlust in Microsoft Edge
ms.author: archandr
author: dan-wesley
manager: seanlynd
ms.date: 03/01/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Verhinderung von Datenverlust (DLP) in Microsoft Edge
ms.openlocfilehash: f25e1fa7a610645f6ca0ca10cbcfc69ae8689b7a
ms.sourcegitcommit: f14286edec59ee9183bdf38c15fc890881efd64f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "11384983"
---
# <a name="data-loss-prevention-dlp-in-microsoft-edge"></a><span data-ttu-id="6b97f-103">Verhinderung von Datenverlust (DLP) in Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="6b97f-103">Data Loss Prevention (DLP) in Microsoft Edge</span></span>

<span data-ttu-id="6b97f-104">Die Verhinderung von Datenverlust (Data Loss Prevention, DLP) ist ein System von Technologien, die vertrauliche Unternehmensdaten erkennen und vor unbefugtem Zugriff schützen.</span><span class="sxs-lookup"><span data-stu-id="6b97f-104">Data loss prevention (DLP) is a system of technologies that identify and safeguard sensitive enterprise data from unauthorized disclosure.</span></span> <span data-ttu-id="6b97f-105">Die Unternehmen müssen vertrauliche Informationen schützen und deren nicht autorisierte Offenlegung verhindern, um den Unternehmensstandards und Branchenvorschriften zu entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b97f-105">To comply with business standards and industry regulations, organizations must protect sensitive information and prevent its unauthorized disclosure.</span></span> <span data-ttu-id="6b97f-106">Zu den vertraulichen Informationen gehören unter anderem Finanzdaten oder personenbezogene Informationen (PII) wie Kreditkartennummern, Sozialversicherungsnummern oder Krankenakten.</span><span class="sxs-lookup"><span data-stu-id="6b97f-106">Sensitive information includes financial data or personally identifiable information (PII) such as credit card numbers, social security numbers, or health records, among many other things.</span></span>

<span data-ttu-id="6b97f-107">Die Fernarbeit hat den Schwerpunkt auf die Verwendung von DLP verstärkt.</span><span class="sxs-lookup"><span data-stu-id="6b97f-107">Remote work has increased the emphasis on using DLP.</span></span> <span data-ttu-id="6b97f-108">Angesichts der zunehmenden Nutzung von persönlichen und geschäftlichen Aktivitäten auf Geräten sehen Unternehmen ein erhöhtes Risiko einer nicht autorisierten Freigabe von Unternehmensdaten außerhalb des Arbeitsplatzes.</span><span class="sxs-lookup"><span data-stu-id="6b97f-108">With the growing use of personal and work activities on devices, enterprises are seeing an increased risk of unauthorized sharing of corporate data outside the workplace.</span></span>

<span data-ttu-id="6b97f-109">Diese Kombination von Benutzeraktivitäten hat sich auch auf Geräte ausgebreitet, bei denen Daten zwischen privaten und unternehmensinternen Geräten über eine Vielzahl von öffentlichen und privaten Netzwerken verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="6b97f-109">This blending of user activities has spread to devices as well, where data is moved between personal and corporate devices over a variety of public and private networks.</span></span> <span data-ttu-id="6b97f-110">Das Ergebnis ist ein erheblich erhöhtes Risiko, vertrauliche Daten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="6b97f-110">The net result is a dramatically increased risk of exposing sensitive data.</span></span>

<span data-ttu-id="6b97f-111">Microsoft Edge unterstützt nativ zwei unterschiedliche DLP-Lösungen, Microsoft Endpoint DLP und Windows Information Protection (WIP).</span><span class="sxs-lookup"><span data-stu-id="6b97f-111">Microsoft Edge natively supports two different DLP solutions, Microsoft Endpoint DLP and Windows Information Protection (WIP).</span></span>

## <a name="microsoft-endpoint-data-loss-prevention-endpoint-dlp"></a><span data-ttu-id="6b97f-112">Microsoft Endpoint-Verhinderung von Datenverlust (Endpunkt-DLP)</span><span class="sxs-lookup"><span data-stu-id="6b97f-112">Microsoft Endpoint data loss prevention (Endpoint DLP)</span></span>

<span data-ttu-id="6b97f-113">Microsoft Endpoint DLP ist die nächste Generation der Verhinderung von Datenverlust unter Verwendung moderner Konzepte wie des datenzentrischen Schutzes.</span><span class="sxs-lookup"><span data-stu-id="6b97f-113">Microsoft Endpoint DLP is the next generation of data loss prevention using modern concepts such as data-centric protection.</span></span> <span data-ttu-id="6b97f-114">Sie ist in Windows 10 und Microsoft Edge integriert, sodass keine zusätzlichen Agents oder Plugins auf dem Gerät benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="6b97f-114">It's built-in to Windows 10 and Microsoft Edge so it doesn't need additional agents or plugins on the device.</span></span>

> [!NOTE]
> <span data-ttu-id="6b97f-115">Dieser Artikel bezieht sich auf Microsoft Edge Version 85 oder neuer.</span><span class="sxs-lookup"><span data-stu-id="6b97f-115">This applies to Microsoft Edge version 85 or later.</span></span>

<span data-ttu-id="6b97f-116">Verwenden Sie die folgenden Ressourcen, um mehr über Endpunkt-DLP zu erfahren:</span><span class="sxs-lookup"><span data-stu-id="6b97f-116">To learn more about Endpoint DLP, use the following resources:</span></span>

- [<span data-ttu-id="6b97f-117">Video: Microsoft Edge und Verhinderung von Datenverlust (DLP)</span><span class="sxs-lookup"><span data-stu-id="6b97f-117">Video: Microsoft Edge and Data loss prevention (DLP)</span></span>](microsoft-edge-video-security-dlp.md)
- [<span data-ttu-id="6b97f-118">Informationen zur Verhinderung von Microsoft 365-Endpunkt Datenverlust</span><span class="sxs-lookup"><span data-stu-id="6b97f-118">Learn about Microsoft 365 Endpoint data loss prevention</span></span>](https://docs.microsoft.com/microsoft-365/compliance/endpoint-dlp-learn-about?view=o365-worldwide&preserve-view=true)
- [<span data-ttu-id="6b97f-119">Erste Schritte mit der Verhinderung von Endpunkt Datenverlust</span><span class="sxs-lookup"><span data-stu-id="6b97f-119">Get started with Endpoint data loss prevention</span></span>](https://docs.microsoft.com/microsoft-365/compliance/endpoint-dlp-getting-started?view=o365-worldwide&preserve-view=true)

<span data-ttu-id="6b97f-120">Microsoft Edge erzwingt administratorenkonfigurierte Richtlinien für vertrauliche Dateien und zeichnet Überwachungsereignisse für nicht kompatible Aktivitäten auf.</span><span class="sxs-lookup"><span data-stu-id="6b97f-120">Microsoft Edge enforces admin configured policies for sensitive files and records audit events for non-compliant activities.</span></span>

<span data-ttu-id="6b97f-121">Einige der Benutzeraktivitäten, die Sie auf Geräten unter Windows 10 überwachen und verwalten können, umfassen die folgenden Aktivitäten:</span><span class="sxs-lookup"><span data-stu-id="6b97f-121">Some of the user activities that you can audit and manage on devices running Windows 10 include the following activities:</span></span>

- <span data-ttu-id="6b97f-122">Dateiupload: Schützen Sie den vertraulichen Dateiupload vor nicht autorisierten Cloud-Speicherorten.</span><span class="sxs-lookup"><span data-stu-id="6b97f-122">File Upload: Protect sensitive file upload to unauthorized cloud locations.</span></span> <!-- The next 3 screenshots show a sequence where a user tries to drop a sensitive data file on to their local storage.-->
- <span data-ttu-id="6b97f-123">Schutz der Zwischenablage: Verhindern, dass vertrauliche Daten aus der Datei kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="6b97f-123">Clipboard Protection: Protect sensitive data from being copied out of the file.</span></span>
- <span data-ttu-id="6b97f-124">Druckschutz: Schützen vertraulicher Dateien, die gedruckt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6b97f-124">Print Protection: Protect sensitive file from being printed.</span></span>
- <span data-ttu-id="6b97f-125">Auf USB/ Im Netzwerk speichern: Schützen vertraulicher Dateien vor dem Speichern in einem USB-Speicher oder nicht autorisierten Netzwerkspeicherorten.</span><span class="sxs-lookup"><span data-stu-id="6b97f-125">Save to USB/Network: Protect sensitive file from being saved to removable USB storage or unauthorized network locations.</span></span>

<span data-ttu-id="6b97f-126">Ausführlichere Informationen zu den Benutzeraktivitäten, die Sie überwachen und verwalten können, finden Sie unter [Endpunktaktivitäten, die Sie überwachen und entsprechende Maßnahmen ergreifen können](https://docs.microsoft.com/microsoft-365/compliance/endpoint-dlp-learn-about?view=o365-worldwide#endpoint-activities-you-can-monitor-and-take-action-on&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="6b97f-126">For more detailed information about user activities you can audit and manage, see [Endpoint activities you can monitor and take action on](https://docs.microsoft.com/microsoft-365/compliance/endpoint-dlp-learn-about?view=o365-worldwide#endpoint-activities-you-can-monitor-and-take-action-on&preserve-view=true).</span></span>

## <a name="windows-information-protection"></a><span data-ttu-id="6b97f-127">Windows Information Protection</span><span class="sxs-lookup"><span data-stu-id="6b97f-127">Windows Information Protection</span></span>

<span data-ttu-id="6b97f-128">Lesen Sie [Support für Windows Information Protection](https://docs.microsoft.com/deployedge/microsoft-edge-security-windows-information-protection), in dem beschrieben wird, wie Microsoft Edge Windows Information Protection (WIP) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6b97f-128">Check out [Support for Windows Information Protection](https://docs.microsoft.com/deployedge/microsoft-edge-security-windows-information-protection), which describes how Microsoft Edge supports Windows Information Protection (WIP).</span></span> <span data-ttu-id="6b97f-129">In den folgenden Abschnitten finden Sie Informationen zu den Systemanforderungen, den Vorteilen und den unterstützten Funktionen:</span><span class="sxs-lookup"><span data-stu-id="6b97f-129">You can learn moe about system requirements, benefits, and supported features in the following sections:</span></span>

- [<span data-ttu-id="6b97f-130">Systemanforderungen</span><span class="sxs-lookup"><span data-stu-id="6b97f-130">System Requirements</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-security-windows-information-protection#system-requirements)
- [<span data-ttu-id="6b97f-131">Vorteile von Windows Information Protection</span><span class="sxs-lookup"><span data-stu-id="6b97f-131">Windows Information Protection Benefits</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-security-windows-information-protection#windows-information-protection-benefits)
- [<span data-ttu-id="6b97f-132">In Microsoft Edge unterstützte WIP-Features</span><span class="sxs-lookup"><span data-stu-id="6b97f-132">WIP features supported in Microsoft Edge</span></span>](https://docs.microsoft.com/DeployEdge/microsoft-edge-security-windows-information-protection#wip-features-supported-in-microsoft-edge)

## <a name="see-also"></a><span data-ttu-id="6b97f-133">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6b97f-133">See also</span></span>

- [<span data-ttu-id="6b97f-134">Microsoft Edge Enterprise-Angebotsseite</span><span class="sxs-lookup"><span data-stu-id="6b97f-134">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="6b97f-135">Video: Verhinderung von Datenverlust in Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="6b97f-135">Video: Data loss prevention - Microsoft Edge</span></span>](https://www.youtube.com/watch?v=dLD04U9eTqg)
- [<span data-ttu-id="6b97f-136">Übersicht über die Verhinderung von Datenverlust</span><span class="sxs-lookup"><span data-stu-id="6b97f-136">Overview of data loss prevention</span></span>](https://docs.microsoft.com/microsoft-365/compliance/data-loss-prevention-policies?view=o365-worldwide&preserve-view=true)
- [<span data-ttu-id="6b97f-137">Schützen von Unternehmensdaten mithilfe von Windows Information Protection</span><span class="sxs-lookup"><span data-stu-id="6b97f-137">Protect your enterprise data using Windows Information Protection</span></span>](https://docs.microsoft.com/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip)
