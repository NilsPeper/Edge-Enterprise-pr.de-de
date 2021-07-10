---
title: Edge für Virtualisierungsdesktopinfrastruktur
ms.author: anlake
author: AndreaLBarr
manager: collw
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Microsoft Edge für Virtualized Desktop Infrastructure.
ms.openlocfilehash: 5dc234b0e6fbba4778f8236399a0ff438f704578
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "11641851"
---
# <a name="microsoft-edge-for-virtualized-desktop-infrastructure"></a><span data-ttu-id="fcf05-103">Microsoft Edge für Virtualized Desktop Infrastructure</span><span class="sxs-lookup"><span data-stu-id="fcf05-103">Microsoft Edge for Virtualized Desktop Infrastructure</span></span>

<span data-ttu-id="fcf05-104">In diesem Artikel werden die Anforderungen und Einschränkungen für die Verwendung von Microsoft Edge in einer virtualisierten Umgebung beschrieben.</span><span class="sxs-lookup"><span data-stu-id="fcf05-104">This article describes the requirements and limitations for using Microsoft Edge in a virtualized environment.</span></span>

## <a name="what-is-vdi"></a><span data-ttu-id="fcf05-105">Was ist VDI?</span><span class="sxs-lookup"><span data-stu-id="fcf05-105">What is VDI?</span></span>

<span data-ttu-id="fcf05-106">Virtual Desktop Infrastructure (VDI) ist eine Virtualisierungstechnologie, die ein Desktopbetriebssystem und Anwendungen auf einem zentralen Server in einem Rechenzentrum hostet.</span><span class="sxs-lookup"><span data-stu-id="fcf05-106">Virtual Desktop Infrastructure (VDI) is virtualization technology that hosts a desktop operating system and applications on a centralized server in a data center.</span></span> <span data-ttu-id="fcf05-107">Dies ermöglicht eine vollständig personalisierte Desktopumgebung für Benutzer mit einer vollständig gesicherten und kompatiblen zentralen Quelle.</span><span class="sxs-lookup"><span data-stu-id="fcf05-107">This enables a fully personalized desktop experience for users with a fully secured and compliant centralized source.</span></span>

<span data-ttu-id="fcf05-108">Microsoft Edge kann in einer solchen virtualisierten Umgebung auf die gleiche Weise wie auf dem lokalen Gerät verwendet werden, während sie in einer sicheren und kontrollierten Serverumgebung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="fcf05-108">Microsoft Edge can be used in such a virtualized environment in much the same ways as it can be used on the local device, all the while running from secure and controlled server environment.</span></span> <span data-ttu-id="fcf05-109">Je nach ausgewählter VDI-Lösung kann es auch möglich sein, Ihren Benutzern einen nahtlosen Zugriff auf Intranetanwendungen und -websites zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="fcf05-109">Depending on your chosen VDI solution it may also be possible to give your users seamless access to intranet Applications and Sites.</span></span>

<span data-ttu-id="fcf05-110">Die meisten Features von Edge werden in VDI-Umgebungen ohne spezielle Konfiguration unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fcf05-110">Most features of Edge are supported on VDI environments without any special configuration.</span></span> <span data-ttu-id="fcf05-111">Um jedoch eine optimale Benutzererfahrung sicherzustellen, empfiehlt es sich, die nachstehenden Anleitungen zu befolgen.</span><span class="sxs-lookup"><span data-stu-id="fcf05-111">However, to ensure an optimal experience it’s recommended to follow the guidance below.</span></span>

## <a name="platforms-certified-for-edge"></a><span data-ttu-id="fcf05-112">Für Edge zertifizierte Plattformen</span><span class="sxs-lookup"><span data-stu-id="fcf05-112">Platforms certified for Edge</span></span>

- <span data-ttu-id="fcf05-113">Azure Virtual Desktop</span><span class="sxs-lookup"><span data-stu-id="fcf05-113">Azure Virtual Desktop</span></span>
- <span data-ttu-id="fcf05-114">Citrix Virtual Apps and Desktops (früher bekannt als XenApp und XenDesktop)</span><span class="sxs-lookup"><span data-stu-id="fcf05-114">Citrix Virtual Apps and Desktops (formerly known as XenApp and XenDesktop)</span></span>

<span data-ttu-id="fcf05-115">Andere VDI-Lösungen wurden zwar noch nicht vom Edge-Team überprüft, es wird jedoch erwartet, dass die häufigsten Workflows in Edge unterstützt werden sollten.</span><span class="sxs-lookup"><span data-stu-id="fcf05-115">While other VDI solutions have not yet been verified by the Edge team, it is expected that the most common workflows in Edge should be supported.</span></span> <span data-ttu-id="fcf05-116">Die unten aufgeführten Anleitungen gelten möglicherweise oder nicht für die von Ihnen ausgewählte Lösung.</span><span class="sxs-lookup"><span data-stu-id="fcf05-116">Guidance provided below may or may not be applicable to your chosen solution.</span></span>

## <a name="edge-on-vdi-performance-considerations"></a><span data-ttu-id="fcf05-117">Überlegungen zur Leistung von Edge auf VDI</span><span class="sxs-lookup"><span data-stu-id="fcf05-117">Edge on VDI performance considerations</span></span>

<span data-ttu-id="fcf05-118">Berücksichtigen Sie beim Entwickeln Ihrer VDI-Umgebung sorgfältig die Workflows und Anforderungen Ihrer Benutzer, um eine optimale Leistung zu erzielen, sowie die Grenzen Ihrer Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="fcf05-118">When designing your VDI environment you should carefully consider the workflows and needs of your users to achieve optimal performance, as well as the limits of your server configuration.</span></span>

<span data-ttu-id="fcf05-119">Edge empfiehlt die folgenden Mindestanforderungen für die Bereitstellung von Edge in VDI-Umgebungen:</span><span class="sxs-lookup"><span data-stu-id="fcf05-119">Edge recommends the following minimal requirements for deploying Edge to VDI environments:</span></span>

- <span data-ttu-id="fcf05-120">vCPU – 2-4 Kerne pro Benutzer</span><span class="sxs-lookup"><span data-stu-id="fcf05-120">vCPU – 2-4 Cores per User</span></span>
- <span data-ttu-id="fcf05-121">RAM – 1 GB pro Benutzer</span><span class="sxs-lookup"><span data-stu-id="fcf05-121">RAM – 1 GB per User</span></span>

<span data-ttu-id="fcf05-122">Bitte beachten Sie, dass große komplexe Webanwendungen und Erweiterungen mehr Arbeitsspeicher benötigen und bei der Konfiguration Ihrer Umgebung berücksichtigt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="fcf05-122">Please note that large complex web applications and extensions will require more memory and will have to be accounted for when configuring your environment.</span></span>

## <a name="edge-on-non-persisted-vdi-environments"></a><span data-ttu-id="fcf05-123">Edge in nicht persistenten VDI-Umgebungen</span><span class="sxs-lookup"><span data-stu-id="fcf05-123">Edge on non-persisted VDI environments</span></span>

<span data-ttu-id="fcf05-124">Viele VDI-Lösungen ermöglichen den Zugriff auf persistente Umgebungen, bei denen den Benutzern eine virtuelle Umgebung zugewiesen wird, die zwischen den Sitzungen bestehen bleibt, und auf nicht persistente Umgebungen, bei denen die Benutzer einem von mehreren verfügbaren Rechnern zugewiesen werden, möglicherweise einem anderen Rechner pro Sitzung, wobei die Benutzerdaten zwischen den Sitzungen synchronisiert werden können oder auch nicht.</span><span class="sxs-lookup"><span data-stu-id="fcf05-124">Many VDI solutions allow access to persisted environments, where users are assigned a virtual environment that persists between sessions, and non-persisted environments, where users are assigned to one of several available machines, possibly a different machine each session, user data may or may not sync between sessions.</span></span>

<span data-ttu-id="fcf05-125">Wenn man eine nicht persistente Umgebung verwendet, erstellt man normalerweise ein "Golden Image", das für jedes Gerät verwendet wird und die benötigten Apps und Konfigurationen enthält.</span><span class="sxs-lookup"><span data-stu-id="fcf05-125">When using a non-persisted environment, one usually creates a “golden image” which is used for each device that includes the needed apps and configurations.</span></span> <span data-ttu-id="fcf05-126">Im Folgenden finden Sie unsere Empfehlungen für die Vorbereitung von Edge auf ein solches Image.</span><span class="sxs-lookup"><span data-stu-id="fcf05-126">Below are our recommendations for preparing Edge for such an image.</span></span>

### <a name="deploy-edge"></a><span data-ttu-id="fcf05-127">Bereitstellen von Edge</span><span class="sxs-lookup"><span data-stu-id="fcf05-127">Deploy Edge</span></span>

<span data-ttu-id="fcf05-128">Wenn Sie Windows 10 Version 1803 und höher verwenden, sollten Sie Microsoft Edge auf Ihrem System installiert haben.</span><span class="sxs-lookup"><span data-stu-id="fcf05-128">If you are on Windows 10, version 1803 and above, you should have Microsoft Edge installed on your system.</span></span> <span data-ttu-id="fcf05-129">Wenn Sie jedoch eine ältere Version von Windows verwenden oder einen anderen Edge-Kanal bereitstellen möchten, werden die folgenden Schritte empfohlen.</span><span class="sxs-lookup"><span data-stu-id="fcf05-129">However, if you are on an older version of Windows or wish to deploy a different channel of Edge, the following steps are recommended.</span></span>

1. <span data-ttu-id="fcf05-130">Laden Sie das Edge-MSI-Paket herunter, das ihrem VDI-VM-Betriebssystem entspricht:</span><span class="sxs-lookup"><span data-stu-id="fcf05-130">Download the Edge MSI package matching your VDI VM operating system from:</span></span>

    - [<span data-ttu-id="fcf05-131">Herunterladen von Microsoft Edge for Business – Microsoft</span><span class="sxs-lookup"><span data-stu-id="fcf05-131">Download Microsoft Edge for Business - Microsoft</span></span>](https://www.microsoft.com/edge/business/download)

2. <span data-ttu-id="fcf05-132">Installieren Sie die MSI-Datei auf dem virtuellen VDI-Computer, indem Sie den folgenden Befehl ausführen:</span><span class="sxs-lookup"><span data-stu-id="fcf05-132">Install the MSI to the VDI VM by running the following command:</span></span>

    - `msiexec /i <path_to_msi> /qn /norestart /l*v <install_logfile_name>`

### <a name="disable-automatic-updates"></a><span data-ttu-id="fcf05-133">Deaktivieren von automatischen Updates</span><span class="sxs-lookup"><span data-stu-id="fcf05-133">Disable automatic updates</span></span>

<span data-ttu-id="fcf05-134">Für nicht persistente Computer empfiehlt es sich, automatische Updates zu deaktivieren und stattdessen Edge zu aktualisieren, indem Sie das "Golden Image" aktualisieren, um sicherzustellen, dass keine Versionskonflikte zwischen dem Computerpool bestehen.</span><span class="sxs-lookup"><span data-stu-id="fcf05-134">For non-persisted machines it is best practice to disable automatic updates and instead update Edge by updating the “golden image” to ensure that there are no version mismatches among the pool of machines.</span></span>

<span data-ttu-id="fcf05-135">Lesen Sie die folgenden Richtlinien zum Deaktivieren von automatischen Updates:</span><span class="sxs-lookup"><span data-stu-id="fcf05-135">See the following policies for disabling automatic updates:</span></span>

- [<span data-ttu-id="fcf05-136">Die Updaterichtlinie überschreibt die Standardrichtlinie</span><span class="sxs-lookup"><span data-stu-id="fcf05-136">Update policy override default</span></span>](/deployedge/microsoft-edge-update-policies#updatedefault)

- [<span data-ttu-id="fcf05-137">Außerkraftsetzung von Updaterichtlinien</span><span class="sxs-lookup"><span data-stu-id="fcf05-137">Update policy override</span></span>](/deployedge/microsoft-edge-update-policies#update)

### <a name="profile-management"></a><span data-ttu-id="fcf05-138">Profilverwaltung</span><span class="sxs-lookup"><span data-stu-id="fcf05-138">Profile management</span></span>

<span data-ttu-id="fcf05-139">Bei nicht persistenten Umgebungen ist es wichtig zu berücksichtigen, dass virtuelle Computer möglicherweise nicht den Benutzerstatus zwischen Sitzungen beibehalten oder Benutzern eine VM zugewiesen wird, die sie noch nie verwendet haben und daher keine Benutzerdaten aufweisen.</span><span class="sxs-lookup"><span data-stu-id="fcf05-139">On non-persisted setups it is important to consider that VMs may not maintain user state between sessions or users may be assigned a VM they have never used before and as such has none of their user data.</span></span>

<span data-ttu-id="fcf05-140">Edge unterstützt mehrere Methoden zum Synchronisieren von Benutzerdaten, sodass sie verfügbar sind, unabhängig davon, wie sie auf Edge zugreifen.</span><span class="sxs-lookup"><span data-stu-id="fcf05-140">Edge supports several methods for syncing user data such that it is available regardless of how they are accessing Edge.</span></span>

### <a name="azure-ad-sync"></a><span data-ttu-id="fcf05-141">Microsoft Azure Active Directory-Synchronisierungsdienste</span><span class="sxs-lookup"><span data-stu-id="fcf05-141">Azure AD Sync</span></span>

<span data-ttu-id="fcf05-142">Wenn Ihr Azure AD-Plan dies unterstützt, ist Enterprise-Synchronisierung die schnellste und einfachste Methode, um sicherzustellen, dass Edge-Benutzerdaten mit allen Benutzergeräten synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="fcf05-142">If your Azure AD plan supports it, Enterprise sync is the fastest and easiest method to ensure that Edge user data is synced to all user devices.</span></span>  

<span data-ttu-id="fcf05-143">Weitere Informationen zu Anforderungen und Konfiguration finden Sie im Folgenden.</span><span class="sxs-lookup"><span data-stu-id="fcf05-143">See the following for more information on requirements and configuration.</span></span>  

- [<span data-ttu-id="fcf05-144">Konfigurieren von Microsoft Edge Enterprise-Synchronisierung | Microsoft-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="fcf05-144">Configure Microsoft Edge enterprise sync | Microsoft Docs</span></span>](/deployedge/microsoft-edge-enterprise-sync)

### <a name="on-premise-sync-for-active-directory-users"></a><span data-ttu-id="fcf05-145">Lokale Synchronisierung für Active Directory-Benutzer</span><span class="sxs-lookup"><span data-stu-id="fcf05-145">On-premise Sync for Active Directory Users</span></span>

<span data-ttu-id="fcf05-146">Bei der lokalen Synchronisierung speichert Microsoft Edge die Favoriten und Einstellungen eines Active Directory-Benutzers in einer Datei, die problemlos zwischen verschiedenen Computern verschoben werden kann.</span><span class="sxs-lookup"><span data-stu-id="fcf05-146">With on-premises sync, Microsoft Edge saves an Active Directory user's favorites and settings to a file that can easily be moved between different computers.</span></span>  

<span data-ttu-id="fcf05-147">Weitere Informationen zu Anforderungen und Konfiguration finden Sie im Folgenden.</span><span class="sxs-lookup"><span data-stu-id="fcf05-147">See the following for more information on requirements and configuration.</span></span>  

- [<span data-ttu-id="fcf05-148">Lokale Synchronisierung für Active Directory (AD)-Benutzer | Microsoft-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="fcf05-148">On-premises sync for Active Directory (AD) users | Microsoft Docs</span></span>](/deployedge/microsoft-edge-on-premises-sync)

### <a name="user-profile-redirection"></a><span data-ttu-id="fcf05-149">Benutzerprofilumleitung</span><span class="sxs-lookup"><span data-stu-id="fcf05-149">User Profile Redirection</span></span>  

<span data-ttu-id="fcf05-150">Es gibt mehrere Lösungen zum Migrieren und Umleiten des gesamten Benutzerordners, um sicherzustellen, dass der Benutzerkontext in solchen nicht persistenten Umgebungen beibehalten wird.</span><span class="sxs-lookup"><span data-stu-id="fcf05-150">There are several solutions for migrating and redirecting the entire user folder to ensure that user context is maintained in such non-persisted environments.</span></span> <span data-ttu-id="fcf05-151">Wenden Sie sich an Ihren VDI-Anbieter, um die empfohlene Lösung zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="fcf05-151">Check with your VDI provider to determine the recommended solution.</span></span>

<span data-ttu-id="fcf05-152">Einige beliebte Lösungen sind:</span><span class="sxs-lookup"><span data-stu-id="fcf05-152">Some popular solutions include:</span></span>

- [<span data-ttu-id="fcf05-153">FSLogix-Übersicht – FSLogix | Microsoft-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="fcf05-153">FSLogix Overview - FSLogix | Microsoft Docs</span></span>](/fslogix/overview)
- [<span data-ttu-id="fcf05-154">Konfigurieren der Citrix-Profilverwaltung</span><span class="sxs-lookup"><span data-stu-id="fcf05-154">How to Configure Citrix Profile Management</span></span>](https://support.citrix.com/article/CTX222893)

<span data-ttu-id="fcf05-155">Es kann auch empfohlen werden, bei Verwendung dieser Methode unnötige Ordner aus dem gesicherten Benutzerordner auszuschließen, um die anfänglichen Ladezeiten zu reduzieren, wenn sich Benutzer bei einem Computer anmelden und das Profil migriert wird.</span><span class="sxs-lookup"><span data-stu-id="fcf05-155">It is also may be recommended that when using this method unnecessary folders be excluded from the backed-up user folder to reduce initial loading times when users are logging on to a machine and the profile is being migrated.</span></span> <span data-ttu-id="fcf05-156">Wenn ja, empfehlen wir, die folgenden Ordner aus der Sicherung auszuschließen, um die Größe zu verringern.</span><span class="sxs-lookup"><span data-stu-id="fcf05-156">If so, we recommend the following folders be excluded from your backup to reduce size.</span></span>

- <span data-ttu-id="fcf05-157">%LocalAppData%\Microsoft\Edge\User Data\Default\Cache</span><span class="sxs-lookup"><span data-stu-id="fcf05-157">%LocalAppData%\Microsoft\Edge\User Data\Default\Cache</span></span>
- <span data-ttu-id="fcf05-158">%LocalAppData%\Microsoft\Edge\User Data\Default\Code Cache</span><span class="sxs-lookup"><span data-stu-id="fcf05-158">%LocalAppData%\Microsoft\Edge\User Data\Default\Code Cache</span></span>
- <span data-ttu-id="fcf05-159">%LocalAppData%\Microsoft\Edge\User Data\Default\JumpListIconsTopSites</span><span class="sxs-lookup"><span data-stu-id="fcf05-159">%LocalAppData%\Microsoft\Edge\User Data\Default\JumpListIconsTopSites</span></span>
- <span data-ttu-id="fcf05-160">%LocalAppData%\Microsoft\Edge\User Data\Default\JumpListIconsRecentClosed</span><span class="sxs-lookup"><span data-stu-id="fcf05-160">%LocalAppData%\Microsoft\Edge\User Data\Default\JumpListIconsRecentClosed</span></span>

## <a name="known-issues"></a><span data-ttu-id="fcf05-161">Bekannte Probleme</span><span class="sxs-lookup"><span data-stu-id="fcf05-161">Known issues</span></span>

### <a name="microsoft-edge-crashes-in-older-versions-of-xenapp-and-xendesktop"></a><span data-ttu-id="fcf05-162">Abstürzen von Microsoft Edge in älteren Versionen von XenApp und XenDesktop</span><span class="sxs-lookup"><span data-stu-id="fcf05-162">Microsoft Edge crashes in older versions of XenApp and XenDesktop</span></span>

<span data-ttu-id="fcf05-163">Dieses Problem sollte in neueren Versionen behoben werden. Wenn dieses Problem jedoch in Ihrer Umgebung auftritt, können Sie das Problem umgehen, indem Sie Citrix API Hooks für Edge deaktivieren. Weitere Informationen finden Sie unter [Deaktivieren von Citrix API Hooks auf Anwendungsbasis.](https://support.citrix.com/article/CTX107825)</span><span class="sxs-lookup"><span data-stu-id="fcf05-163">This issue should be mitigated in newer versions however if you are encountering this issue in your environment, you can work around the issue by disabling Citrix API Hooks for Edge, see [How to Disable Citrix API Hooks on a Per-application Basis.](https://support.citrix.com/article/CTX107825)</span></span>

### <a name="degraded-performance-when-rendering-pages-with-exceptionally-large-html-tables"></a><span data-ttu-id="fcf05-164">Beeinträchtigte Leistung beim Rendering von Seiten mit ungewöhnlich großen HTML-Tabellen</span><span class="sxs-lookup"><span data-stu-id="fcf05-164">Degraded performance when rendering pages with exceptionally large HTML tables</span></span>

<span data-ttu-id="fcf05-165">Die folgenden Citrix-Richtlinien sind dafür bekannt, dass HTML-Seiten mit sehr großen Tabellen (mehr als 30 000 Zeilen) langsam gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="fcf05-165">The following Citrix policies are known to slow rendering of html pages with very large (30,000+ row) tables.</span></span>

- <span data-ttu-id="fcf05-166">Automatische Tastaturanzeige</span><span class="sxs-lookup"><span data-stu-id="fcf05-166">Automatic keyboard display</span></span>
- <span data-ttu-id="fcf05-167">Remotezugriff auf das Kombinationsfeld</span><span class="sxs-lookup"><span data-stu-id="fcf05-167">Remote the combo box</span></span>

<span data-ttu-id="fcf05-168">Weitere Informationen finden Sie unter [Richtlinieneinstellungen für die mobile Benutzeroberfläche (citrix.com)](https://docs.citrix.com/citrix-virtual-apps-desktops/policies/reference/ica-policy-settings/mobile-experience-policy-settings.html).</span><span class="sxs-lookup"><span data-stu-id="fcf05-168">See [Mobile experience policy settings (citrix.com)](https://docs.citrix.com/citrix-virtual-apps-desktops/policies/reference/ica-policy-settings/mobile-experience-policy-settings.html) for more information.</span></span> <span data-ttu-id="fcf05-169">Durch das Deaktivieren dieser Richtlinien sollte das Problem behoben werden.</span><span class="sxs-lookup"><span data-stu-id="fcf05-169">Disabling these policies should mitigate the issue.</span></span>

### <a name="windows-account-manager-authorization-scenarios-ie--azure-sync-fail-in-edge-when-run-as-a-citrix-seamless-application"></a><span data-ttu-id="fcf05-170">Windows-Kontomnager-Autorisierungsszenarien (d. h.  Azure-Synchronisierung) schlägt in Edge fehl, wenn es als nahtlose Citrix-Anwendung ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="fcf05-170">Windows Account Manager authorization scenarios (i.e.  Azure sync) fail in Edge when run as a Citrix seamless application</span></span>

<span data-ttu-id="fcf05-171">Dies ist ein bekanntes Problem in Edge und anderen Anwendungen, die WAM (d. h. Office) verwenden, da Windows-Komponenten, die für solche Szenarien erforderlich sind, nicht initialisiert werden, wenn sie im "nahtlosen" Modus ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="fcf05-171">This is a known issue in Edge and other applications that use WAM (i.e. Office) due to Windows components necessary for such scenarios not being initialized when running in the “seamless” mode.</span></span> <span data-ttu-id="fcf05-172">Problemumgehung:</span><span class="sxs-lookup"><span data-stu-id="fcf05-172">To work around this issue:</span></span>

- <span data-ttu-id="fcf05-173">Verwenden Sie Edge über einen Remotedesktop zum Citrix-Host anstatt als nahtlose Remoteanwendung.</span><span class="sxs-lookup"><span data-stu-id="fcf05-173">Use Edge via a Remote Desktop to the Citrix Host instead of as a seamless remote application.</span></span>
- <span data-ttu-id="fcf05-174">Verwenden Sie stattdessen Azure Virtual Desktop-Remote-Apps, die über Abhilfemaßnahmen für dieses Problem verfügen.</span><span class="sxs-lookup"><span data-stu-id="fcf05-174">Use Azure Virtual Desktop remote apps instead, which has mitigation's for this issue.</span></span>
