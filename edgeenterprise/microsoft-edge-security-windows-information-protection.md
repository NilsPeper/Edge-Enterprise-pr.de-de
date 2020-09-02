---
title: Microsoft Edge-Unterstützung für Windows Information Protection
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 04/24/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Edge-Unterstützung für Windows Information Protection
ms.openlocfilehash: 4ec48d258deb1cf6d4436716f14aa2561cee2a50
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/31/2020
ms.locfileid: "10980077"
---
# <span data-ttu-id="92667-103">Microsoft Edge-Unterstützung für Windows Information Protection (WIP)</span><span class="sxs-lookup"><span data-stu-id="92667-103">Microsoft Edge support for Windows Information Protection (WIP)</span></span>

<span data-ttu-id="92667-104">In diesem Artikel wird beschrieben, wie Windows Information Protection (WIP) von Microsoft Edge unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="92667-104">This article describes how Microsoft Edge supports Windows Information Protection (WIP).</span></span>

> [!NOTE]
> <span data-ttu-id="92667-105">Dies bezieht sich auf Microsoft Edge Version 81 oder neuer.</span><span class="sxs-lookup"><span data-stu-id="92667-105">This applies to Microsoft Edge version 81 or later.</span></span>

## <span data-ttu-id="92667-106">Übersicht</span><span class="sxs-lookup"><span data-stu-id="92667-106">Overview</span></span>

<span data-ttu-id="92667-107">Windows Information Protection (WIP) ist ein Windows 10-Feature, das Unternehmensdaten vor unbefugtem Zugriff oder versehentlicher Offenlegung schützt.</span><span class="sxs-lookup"><span data-stu-id="92667-107">Windows Information Protection (WIP) is a Windows 10 feature that helps protect enterprise data from unauthorized or accidental disclosure.</span></span> <span data-ttu-id="92667-108">Mit dem Anstieg der Remotearbeit besteht das Risiko, dass Unternehmensdaten außerhalb des Arbeitsplatzes geteilt werden.</span><span class="sxs-lookup"><span data-stu-id="92667-108">With the rise of remote work, there's an increased risk of sharing corporate data outside the workplace.</span></span> <span data-ttu-id="92667-109">Dieses Risiko erhöht sich, wenn persönliche und berufliche Aktivitäten auf Unternehmensgeräten stattfinden.</span><span class="sxs-lookup"><span data-stu-id="92667-109">This risk increases when personal activities and work activities occur on corporate devices.</span></span>

<span data-ttu-id="92667-110">Microsoft Edge unterstützt WIP beim Schutz von Inhalten in einer Webumgebung, in der Benutzer häufig Inhalte freigeben und verteilen.</span><span class="sxs-lookup"><span data-stu-id="92667-110">Microsoft Edge supports WIP to help protect content in a web environment where users often share and distribute content.</span></span>

### <span data-ttu-id="92667-111">Systemanforderungen</span><span class="sxs-lookup"><span data-stu-id="92667-111">System requirements</span></span>

<span data-ttu-id="92667-112">Die folgenden Anforderungen gelten für Geräte, die WIP im Unternehmen verwenden:</span><span class="sxs-lookup"><span data-stu-id="92667-112">The follow requirements apply to devices using WIP in the enterprise:</span></span>

- <span data-ttu-id="92667-113">Windows10, Version 1607 oder höher</span><span class="sxs-lookup"><span data-stu-id="92667-113">Windows 10, version 1607 or later</span></span>
- <span data-ttu-id="92667-114">Nur Windows-Client-SKUs</span><span class="sxs-lookup"><span data-stu-id="92667-114">Only Windows client SKUs</span></span>
- <span data-ttu-id="92667-115">Eine der unter [WIP-Voraussetzungen](https://docs.microsoft.com/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip#prerequisites) beschriebenen Verwaltungslösungen</span><span class="sxs-lookup"><span data-stu-id="92667-115">One of the management solutions described in [WIP prerequisites](https://docs.microsoft.com/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip#prerequisites)</span></span>

### <span data-ttu-id="92667-116">Vorteile von Windows Information Protection</span><span class="sxs-lookup"><span data-stu-id="92667-116">Windows Information Protection benefits</span></span>

<span data-ttu-id="92667-117">WIP bietet die folgenden Vorteile:</span><span class="sxs-lookup"><span data-stu-id="92667-117">WIP provides the following benefits:</span></span>

- <span data-ttu-id="92667-118">Eindeutige Trennung zwischen persönlichen Daten und Unternehmensdaten, ohne dass Mitarbeiter zwischen Umgebungen oder Apps wechseln müssen</span><span class="sxs-lookup"><span data-stu-id="92667-118">Obvious separation between personal and corporate data, without requiring employees to switch environments or apps.</span></span>
- <span data-ttu-id="92667-119">Zusätzlicher Schutz von Daten für vorhandene Branchen-Apps, ohne dass die Apps aktualisiert werden müssen</span><span class="sxs-lookup"><span data-stu-id="92667-119">Additional data protection for existing line-of-business apps without a need to update the apps.</span></span>
- <span data-ttu-id="92667-120">Die Möglichkeit, aus der Ferne Unternehmensdaten von den für das Intune Mobile Device Management (MDM) registrierten Geräten zu löschen, ohne dass persönliche Daten hiervon betroffen sind.</span><span class="sxs-lookup"><span data-stu-id="92667-120">The ability to remote wipes corporate data from Intune Mobile Device Management (MDM) enrolled devices while leaving personal data unaffected.</span></span> 
- <span data-ttu-id="92667-121">Überwachungsberichte zum Nachverfolgen von Problemen und für Abhilfemaßnahmen, z. B. Benutzerschulungen zum Thema Compliance.</span><span class="sxs-lookup"><span data-stu-id="92667-121">Audit reports for tracking issues and for remedial actions such as compliance training for users.</span></span>
- <span data-ttu-id="92667-122">Integration in Ihr bestehendes Verwaltungssystem zum Konfigurieren, Bereitstellen und Verwalten von WIP.</span><span class="sxs-lookup"><span data-stu-id="92667-122">Integration with your existing management system to configure, deploy, and manage WIP.</span></span> <span data-ttu-id="92667-123">Einige Beispiele sind Microsoft Intune, Microsoft Endpoint Configuration Manager oder Ihr aktuelles System für die mobile Geräteverwaltung (Mobile Device Management, MDM).</span><span class="sxs-lookup"><span data-stu-id="92667-123">Some examples are Microsoft Intune, Microsoft Endpoint Configuration Manager, or your current mobile device management (MDM) system.</span></span>

## <span data-ttu-id="92667-124">WIP-Richtlinie und-Schutzmodi</span><span class="sxs-lookup"><span data-stu-id="92667-124">WIP policy and protection modes</span></span>

<span data-ttu-id="92667-125">Mithilfe von Richtlinien können Sie die vier in der folgenden Tabelle beschriebenen Schutzmodi konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="92667-125">Using policies, you can configure the four protection modes described in the following table.</span></span> <span data-ttu-id="92667-126">Weitere Informationen finden Sie unter [WIP-Schutzmodi](https://docs.microsoft.com/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip#wip-protection-modes).</span><span class="sxs-lookup"><span data-stu-id="92667-126">For more information, see [WIP-protection modes](https://docs.microsoft.com/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip#wip-protection-modes).</span></span>

| <span data-ttu-id="92667-127">Modus</span><span class="sxs-lookup"><span data-stu-id="92667-127">Mode</span></span> | <span data-ttu-id="92667-128">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="92667-128">Description</span></span> |
|------|-------------|
| <span data-ttu-id="92667-129">Blockieren</span><span class="sxs-lookup"><span data-stu-id="92667-129">Block</span></span> | <span data-ttu-id="92667-130">WIP sucht nach unerwünschten Datenfreigaben und hindert Mitarbeiter daran, den Schritt auszuführen.</span><span class="sxs-lookup"><span data-stu-id="92667-130">WIP looks for inappropriate data sharing practices and stops the employee from completing the action.</span></span> <span data-ttu-id="92667-131">Diese Suche kann die gemeinsame Nutzung von Unternehmensdaten in nicht vom Unternehmen geschützten Apps sowie außerdem die gemeinsame Nutzung von Unternehmensdaten zwischen Apps oder Freigabeversuche außerhalb des Netzwerk Ihrer Organisation umfassen.</span><span class="sxs-lookup"><span data-stu-id="92667-131">This search can include sharing enterprise data to non-enterprise-protected apps in addition to sharing enterprise data between apps or attempting to share outside of your organization's network.</span></span> |
| <span data-ttu-id="92667-132">Allow Overrides</span><span class="sxs-lookup"><span data-stu-id="92667-132">Allow Overrides</span></span> | <span data-ttu-id="92667-133">WIP ermittelt ungeeignete Datenfreigaben und warnt Mitarbeiter davor, eine potenziell unsichere Aktion auszuführen.</span><span class="sxs-lookup"><span data-stu-id="92667-133">WIP looks for inappropriate data sharing, warning employees if they do something deemed potentially unsafe.</span></span> <span data-ttu-id="92667-134">Bei diesem Verwaltungsmodus können Mitarbeiter die Richtlinie jedoch außer Kraft setzen und die Daten freigeben, wobei die Aktion jedoch in ihrem Überwachungsprotokoll protokolliert wird.</span><span class="sxs-lookup"><span data-stu-id="92667-134">However, this management mode lets the employee override the policy and share the data, logging the action to your audit log.</span></span> |
| <span data-ttu-id="92667-135">Unbeaufsichtigt</span><span class="sxs-lookup"><span data-stu-id="92667-135">Silent</span></span> | <span data-ttu-id="92667-136">WIP wird im Hintergrund ausgeführt, wobei unangemessene Datenfreigaben protokolliert werden, ohne irgendetwas anzuhalten, das für die Interaktion des Mitarbeiters im Modus „Außerkraftsetzung“ erforderlich gewesen wäre.</span><span class="sxs-lookup"><span data-stu-id="92667-136">WIP runs silently, logging inappropriate data sharing, without stopping anything that would have been prompted for employee interaction while in Allow Overrides mode.</span></span> <span data-ttu-id="92667-137">Unerlaubte Aktionen, z.B. wenn Apps unzulässigerweise versuchen, auf eine Netzwerkressource oder auf WIP-geschützte Daten zuzugreifen, werden weiterhin verhindert.</span><span class="sxs-lookup"><span data-stu-id="92667-137">Unallowed actions, like apps inappropriately trying to access a network resource or WIP-protected data, are still stopped.</span></span> |
| <span data-ttu-id="92667-138">Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="92667-138">Off</span></span> | <span data-ttu-id="92667-139">WIP ist deaktiviert, und Ihre Daten werden weder geschützt noch überwacht.</span><span class="sxs-lookup"><span data-stu-id="92667-139">WIP is turned off and doesn't help to protect or audit your data.</span></span> <span data-ttu-id="92667-140">Nachdem WIP deaktiviert wurde, wird versucht, alle durch WIP gekennzeichneten Dateien auf den lokal angeschlossenen Laufwerken zu entschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="92667-140">After you turn off WIP, an attempt is made to decrypt any WIP-tagged files on the locally attached drives.</span></span> <span data-ttu-id="92667-141">Ihre vorherigen Entschlüsselungs- und Richtlinieninformationen werden nicht automatisch erneut angewendet, wenn Sie den WIP-Schutz wieder aktivieren.</span><span class="sxs-lookup"><span data-stu-id="92667-141">Your previous decryption and policy info isn't automatically reapplied if you turn WIP protection back on.</span></span>
 |

## <span data-ttu-id="92667-142">In Microsoft Edge unterstützte WIP-Features</span><span class="sxs-lookup"><span data-stu-id="92667-142">WIP features supported in Microsoft Edge</span></span>

<span data-ttu-id="92667-143">Ab Version 81 von Microsoft Edge werden die folgenden Features unterstützt:</span><span class="sxs-lookup"><span data-stu-id="92667-143">Starting with Microsoft Edge version 81, the following features are supported:</span></span>

- <span data-ttu-id="92667-144">Arbeitsbezogene Websites werden durch ein Aktenkoffer-Symbol in der Adressleiste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="92667-144">Work sites will be indicated by a briefcase icon on the address bar.</span></span>  
- <span data-ttu-id="92667-145">Dateien, die von einem arbeitsbezogenen Speicherort heruntergeladen wurden, werden automatisch verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="92667-145">Files downloaded from a work location are automatically encrypted.</span></span>
- <span data-ttu-id="92667-146">Durchsetzung der Ebenen Silent/Block/Override für das Hochladen von arbeitsbezogenen Dateien an nicht arbeitsbezogene Speicherorte.</span><span class="sxs-lookup"><span data-stu-id="92667-146">Silent/Block/Override enforcement for work file uploads to non-work locations.</span></span>  
- <span data-ttu-id="92667-147">Durchsetzung der Ebenen Silent/Block/Override für Drag & Drop-Aktionen.</span><span class="sxs-lookup"><span data-stu-id="92667-147">Silent/Block/Override enforcement for file Drag & Drop actions.</span></span>
- <span data-ttu-id="92667-148">Durchsetzung der Ebenen Silent/Block/Override für Zwischenablage-Aktionen.</span><span class="sxs-lookup"><span data-stu-id="92667-148">Silent/Block/Override enforcement for Clipboard actions.</span></span>
- <span data-ttu-id="92667-149">Beim Navigieren zu arbeitsbezogenen Speicherorten von nicht arbeitsbezogenen Profilen aus erfolgt eine automatische Umleitung an das (der Azure AD-Identität zugeordnete) Arbeitsprofil.</span><span class="sxs-lookup"><span data-stu-id="92667-149">Browsing to work locations from non-work profiles automatically redirects to the Work Profile (associated with the Azure AD Identity.)</span></span>
- <span data-ttu-id="92667-150">Der IE-Modus unterstützt die vollständige WIP-Funktionalität.</span><span class="sxs-lookup"><span data-stu-id="92667-150">IE Mode supports full WIP functionality.</span></span>

## <span data-ttu-id="92667-151">Arbeiten mit WIP in Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="92667-151">Working with WIP in Microsoft Edge</span></span>

<span data-ttu-id="92667-152">Nach der Aktivierung der WIP-Unterstützung für Microsoft Edge wird es Benutzern angezeigt, wenn sie auf arbeitsbezogene Informationen zugreifen.</span><span class="sxs-lookup"><span data-stu-id="92667-152">After WIP support is enabled for Microsoft Edge, users will see when work-related information is accessed.</span></span> <span data-ttu-id="92667-153">Der nächste Screenshot zeigt das Symbol „Aktenkoffer“ in der Adressleiste, das anzeigt, dass über den Browser auf arbeitsbezogene Informationen zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="92667-153">The next screenshot shows the briefcase icon in the address bar, indicating that work-related information is accessed via the browser.</span></span>

 ![Adressleistenanzeige für arbeitsbezogene Websites](./media/microsoft-edge-security-windows-information-protection/microsoft-edge-wip-notify.png)

<span data-ttu-id="92667-155">In Microsoft Edge können Benutzer geschützte Inhalte auf nicht genehmigten Websites freizugeben.</span><span class="sxs-lookup"><span data-stu-id="92667-155">Microsoft Edge gives users the ability to share protected content in an unapproved website.</span></span> <span data-ttu-id="92667-156">Der nächste Screenshot zeigt die Microsoft Edge-Eingabeaufforderung, die es einem Benutzer gestattet, geschützte Inhalte auf einer nicht genehmigten Website zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="92667-156">The next screenshot shows the Microsoft Edge prompt that allows a user to use protected content in an unapproved website.</span></span>

 ![Aufforderung für die Außerkraftsetzung des Inhaltsschutzes](./media/microsoft-edge-security-windows-information-protection/microsoft-edge-wip-override.png)

## <span data-ttu-id="92667-158">Konfigurieren von Richtlinien zur Unterstützung von WIP</span><span class="sxs-lookup"><span data-stu-id="92667-158">Configure policies to support WIP</span></span>

<span data-ttu-id="92667-159">Um WIP mit Microsoft Edge verwenden zu können, müssen Sie über ein Arbeitsprofil verfügen.</span><span class="sxs-lookup"><span data-stu-id="92667-159">Using WIP with Microsoft Edge requires the presence of a work profile.</span></span>

### <span data-ttu-id="92667-160">Sicherstellen des Vorhandenseins eines Arbeitsprofils</span><span class="sxs-lookup"><span data-stu-id="92667-160">Ensure the presence of a work profile</span></span>

<span data-ttu-id="92667-161">Bei hybrid verbundenen Computern wird Microsoft Edge automatisch mit dem Azure Active Directory-Konto (Azure AD) angemeldet.</span><span class="sxs-lookup"><span data-stu-id="92667-161">On hybrid joined machines, Microsoft Edge is automatically signed in with the Azure Active Directory (Azure AD) account.</span></span> <span data-ttu-id="92667-162">Um sicherzustellen, dass Benutzer dieses Profil, das für WIP benötigt wird, nicht entfernen, konfigurieren Sie die folgende Richtlinie:</span><span class="sxs-lookup"><span data-stu-id="92667-162">To make sure that users don't remove this profile, which is needed for WIP, configure the following policy:</span></span>

- [<span data-ttu-id="92667-163">NonRemovableProfileEnabled</span><span class="sxs-lookup"><span data-stu-id="92667-163">NonRemovableProfileEnabled</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#nonremovableprofileenabled)

> [!NOTE]
> <span data-ttu-id="92667-164">Wenn Ihre Umgebung nicht hybrid verbunden ist, können Sie mit diesen Anweisungen eine Hybridverbindung herstellen: [Planen Ihrer Implementierung einer hybriden Einbindung in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/devices/hybrid-azuread-join-plan).</span><span class="sxs-lookup"><span data-stu-id="92667-164">If your environment isn't hybrid joined, you can hybrid join using these instructions: [Plan your hybrid Azure Active Directory join implementation](https://docs.microsoft.com/azure/active-directory/devices/hybrid-azuread-join-plan).</span></span>

<span data-ttu-id="92667-165">Wenn eine Hybridverbindung keine Option ist, können Sie lokale Active Directory-Konten verwenden, um Microsoft Edge zu ermöglichen, automatisch spezielle Arbeitsprofile mit den Domänenkonten der Benutzer zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="92667-165">If hybrid joining isn't an option, you can use on-prem Active Directory accounts to allow Microsoft Edge to auto create a special work profile with the users' domain accounts.</span></span> <span data-ttu-id="92667-166">Bitte beachten Sie, dass für lokale Konten möglicherweise nicht alle Features von Azure AD vorhanden sind, wie z.B. Cloudsynchronisierung, Office NTP usw.)</span><span class="sxs-lookup"><span data-stu-id="92667-166">Note that on-premises accounts may not receive all of Azure AD's features, such as cloud sync, Office NTP, and so on.)</span></span>

#### <span data-ttu-id="92667-167">Active Directory (AD)-Konten</span><span class="sxs-lookup"><span data-stu-id="92667-167">Active Directory (AD) accounts</span></span>

<span data-ttu-id="92667-168">Für AD-Konten müssen Sie die folgende Richtlinie konfigurieren, damit Microsoft Edge automatisch ein spezielles Arbeitsprofil erstellt.</span><span class="sxs-lookup"><span data-stu-id="92667-168">For AD accounts, you must configure the following policy to have the Microsoft Edge auto create a special work profile.</span></span>

- [<span data-ttu-id="92667-169">ConfigureOnPremisesAccountAutoSignIn</span><span class="sxs-lookup"><span data-stu-id="92667-169">ConfigureOnPremisesAccountAutoSignIn</span></span>](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configureonpremisesaccountautosignin)

### <span data-ttu-id="92667-170">Windows-Richtlinien für WIP</span><span class="sxs-lookup"><span data-stu-id="92667-170">Windows policies for WIP</span></span>

<span data-ttu-id="92667-171">Sie können WIP mithilfe von Windows-Richtlinien konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="92667-171">You can configure WIP using Windows policies.</span></span> <span data-ttu-id="92667-172">Weitere Informationen finden Sie unter [Erstellen und Bereitstellen von WIP-Richtlinien mithilfe von Microsoft Intune](https://docs.microsoft.com/windows/security/information-protection/windows-information-protection/overview-create-wip-policy)</span><span class="sxs-lookup"><span data-stu-id="92667-172">For more information, see [Create and deploy WIP policies using Microsoft Intune](https://docs.microsoft.com/windows/security/information-protection/windows-information-protection/overview-create-wip-policy)</span></span>

## <span data-ttu-id="92667-173">Häufig gestellte Fragen</span><span class="sxs-lookup"><span data-stu-id="92667-173">Frequently Asked Questions</span></span>

### <span data-ttu-id="92667-174">Wie behebe ich den Fehler mit dem Code -2147024540?</span><span class="sxs-lookup"><span data-stu-id="92667-174">How do I resolve Error Code -2147024540?</span></span>

<span data-ttu-id="92667-175">Dieser Fehlercode entspricht dem folgenden Windows Information Protection-Fehler: *ERROR_EDP_POLICY_DENIES_OPERATION: der angeforderte Vorgang wurde durch die Windows Information Protection-Richtlinie blockiert. Wenn Sie weitere Informationen benötigen, wenden Sie sich an den System Administrator.*</span><span class="sxs-lookup"><span data-stu-id="92667-175">This error code corresponds to the following Windows Information Protection error: *ERROR_EDP_POLICY_DENIES_OPERATION: The requested operation was blocked by Windows Information Protection policy. For more information, contact your system administrator.*</span></span>

<span data-ttu-id="92667-176">Microsoft Edge zeigt diesen Fehler an, wenn die Organisation Windows Information Protection (WIP) aktiviert hat, um Benutzern mit genehmigten Anwendungen nur den Zugriff auf Unternehmensressourcen zu gestatten.</span><span class="sxs-lookup"><span data-stu-id="92667-176">Microsoft Edge shows this error when the organization has enabled Windows Information Protection (WIP) to only allow users with approved applications to access corporate resources.</span></span> <span data-ttu-id="92667-177">Da Microsoft Edge sich in diesem Fall nicht in der Liste genehmigter Anwendungen befindet, muss der Administrator die WIP-Richtlinien aktualisieren, um Zugriff auf Microsoft Edge zu gewähren.</span><span class="sxs-lookup"><span data-stu-id="92667-177">In this case because Microsoft Edge isn't on the approved applications list, the admin will have to update the WIP policies to grant access to Microsoft Edge.</span></span>

<span data-ttu-id="92667-178">Der folgende Screenshot zeigt, wie Microsoft Intune verwendet wird, um Microsoft Edge als zulässige App für WIP hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="92667-178">The following screenshot shows how the Microsoft Intune is used to add Microsoft Edge as an allowed app for WIP.</span></span>

 ![Intune-Dialogfeld zum Hinzufügen von Microsoft Edge als App für WIP](./media/microsoft-edge-security-windows-information-protection/microsoft-edge-wip-exemption.png)

<span data-ttu-id="92667-180">Wenn Sie Microsoft Intune nicht verwenden, laden Sie das Richtlinienupdate in der Datei [WIP-Richtlinie für Enterprise AppLocker](https://download.microsoft.com/download/8/9/9/8995d820-065c-4ab1-aa2a-9d6dc0cd7ffa/MsEdge%20-%20WIP%20Enterprise%20AppLocker%20Policy%20Files.zip) herunter, und wenden Sie diese an.</span><span class="sxs-lookup"><span data-stu-id="92667-180">If you're not using Microsoft Intune, download and apply the policy update in the [WIP Enterprise AppLocker Policy](https://download.microsoft.com/download/8/9/9/8995d820-065c-4ab1-aa2a-9d6dc0cd7ffa/MsEdge%20-%20WIP%20Enterprise%20AppLocker%20Policy%20Files.zip) file.</span></span>

## <span data-ttu-id="92667-181">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="92667-181">See also</span></span>

- [<span data-ttu-id="92667-182">Microsoft Edge Enterprise-Angebotsseite</span><span class="sxs-lookup"><span data-stu-id="92667-182">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise) 
- [<span data-ttu-id="92667-183">Schützen von Unternehmensdaten mithilfe von Windows Information Protection</span><span class="sxs-lookup"><span data-stu-id="92667-183">Protect enterprise data using Windows Information Protection</span></span>](https://docs.microsoft.com/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip)
