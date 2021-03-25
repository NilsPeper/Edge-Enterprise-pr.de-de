---
title: Verwenden von Microsoft Edge zum Schutz vor potenziell unerwünschten Anwendungen
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 03/04/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Verwenden von Microsoft Edge zum Schutz vor potenziell unerwünschten Anwendungen
ms.openlocfilehash: 4e9d513c4d1144d4109064d7aa42e4ef31a59b88
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/24/2021
ms.locfileid: "11448029"
---
# <a name="protect-against-potentially-unwanted-applications-puas"></a><span data-ttu-id="c0284-103">Schützen vor potenziell unerwünschten Anwendungen (PUA)</span><span class="sxs-lookup"><span data-stu-id="c0284-103">Protect against potentially unwanted applications (PUAs)</span></span>

<span data-ttu-id="c0284-104">In diesem Artikel wird erläutert, wie Sie sich mit Microsoft Edge oder Windows Defender Antivirus vor potenziell unerwünschten Anwendungen (PUA) schützen können.</span><span class="sxs-lookup"><span data-stu-id="c0284-104">This article explains how you can protect against potentially unwanted applications (PUAs) using Microsoft Edge or by using Windows Defender Antivirus.</span></span>

> [!NOTE]
> <span data-ttu-id="c0284-105">Dieser Artikel bezieht sich auf Microsoft Edge Version80 oder höher.</span><span class="sxs-lookup"><span data-stu-id="c0284-105">This article applies to Microsoft Edge version 80 or later.</span></span>

## <a name="overview"></a><span data-ttu-id="c0284-106">Übersicht</span><span class="sxs-lookup"><span data-stu-id="c0284-106">Overview</span></span>

<span data-ttu-id="c0284-107">Potenziell unerwünschte Anwendungen werden nicht als Viren oder Schadsoftware betrachtet, diese Apps können jedoch Aktionen an Endpunkten ausführen, die sich negativ auf die Endpunktleistung oder -nutzung auswirken.</span><span class="sxs-lookup"><span data-stu-id="c0284-107">Potentially unwanted applications aren't considered to be viruses or malware, but these apps might perform actions on endpoints that adversely affect endpoint performance or use.</span></span> <span data-ttu-id="c0284-108">So versucht *Evasionssoftware* (Software zum Umgehen der Erkennung oder zum Vermeiden anderer Abwehrmaßnahmen) beispielsweise aktiv, die Erkennung durch Sicherheitsprodukte zu umgehen.</span><span class="sxs-lookup"><span data-stu-id="c0284-108">For example, *Evasion software* actively tries to evade detection by security products.</span></span> <span data-ttu-id="c0284-109">Diese Art von Software kann das Risiko erhöhen, dass Ihr Netzwerk mit der eigentlichen Schadsoftware infiziert wird.</span><span class="sxs-lookup"><span data-stu-id="c0284-109">This kind of software can increase the risk of your network being infected with actual malware.</span></span> <span data-ttu-id="c0284-110">PUA kann sich auch auf Anwendungen beziehen, die bekanntermaßen mit Sicherheitsrisiken verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="c0284-110">PUA can also refer to applications that are considered to have poor reputation.</span></span>

<span data-ttu-id="c0284-111">Eine Beschreibung der Kriterien, anhand derer Software als PUA klassifiziert wird, finden Sie unter [Potenziell unerwünschte Anwendung](/windows/security/threat-protection/intelligence/criteria#potentially-unwanted-application-pua).</span><span class="sxs-lookup"><span data-stu-id="c0284-111">For a description of the criteria used to classify software as a PUA, see [Potentially unwanted application](/windows/security/threat-protection/intelligence/criteria#potentially-unwanted-application-pua).</span></span>

## <a name="protect-against-pua-with-microsoft-edge"></a><span data-ttu-id="c0284-112">Schutz vor PUA mit Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c0284-112">Protect against PUA with Microsoft Edge</span></span>

<span data-ttu-id="c0284-113">Microsoft Edge (Version 80.0.361.50 oder höher) blockiert PUA-Downloads und zugehörige Ressourcen-URLs.</span><span class="sxs-lookup"><span data-stu-id="c0284-113">Microsoft Edge (version 80.0.361.50 or later) blocks PUA downloads and associated resource URLs.</span></span>

<span data-ttu-id="c0284-114">Sie können Schutzmaßnahmen einrichten, indem Sie das Feature **Potenziell unerwünschte Apps blockieren** in Microsoft Edge aktivieren.</span><span class="sxs-lookup"><span data-stu-id="c0284-114">You can set up protection by enabling the **Block potentially unwanted apps** feature in Microsoft Edge.</span></span>

> [!NOTE]
> <span data-ttu-id="c0284-115">Der [Microsoft Edge-Teamblogbeitrag](https://blogs.windows.com/msedgedev/2020/02/27/protecting-users-potentially-unwanted-apps/) beschreibt dieses neue Feature, und erläutert, wie Sie eine falsch beschriftete App behandeln oder eine App als unerwünscht melden.</span><span class="sxs-lookup"><span data-stu-id="c0284-115">The [Microsoft Edge Team blog post](https://blogs.windows.com/msedgedev/2020/02/27/protecting-users-potentially-unwanted-apps/) describes this new feature and explains how to handle a mislabeled app or report an app as unwanted.</span></span>

### <a name="to-enable-pua-protection"></a><span data-ttu-id="c0284-116">So aktivieren Sie den Schutz vor potenziell unerwünschten Anwendungen</span><span class="sxs-lookup"><span data-stu-id="c0284-116">To enable PUA protection:</span></span>

1. <span data-ttu-id="c0284-117">Öffnen Sie **Einstellungen** im Browser.</span><span class="sxs-lookup"><span data-stu-id="c0284-117">Open **Settings** in the browser.</span></span>
2. <span data-ttu-id="c0284-118">Wählen Sie **Datenschutz und Dienste** aus.</span><span class="sxs-lookup"><span data-stu-id="c0284-118">Select **Privacy and services**.</span></span>
3. <span data-ttu-id="c0284-119">Überprüfen Sie im Abschnitt **Dienste**, ob **Microsoft Defender SmartScreen** aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="c0284-119">In the **Services** section, check to see that **Microsoft Defender SmartScreen** is turned on.</span></span> <span data-ttu-id="c0284-120">Wenn nicht, aktivieren Sie Microsoft Defender SmartScreen.</span><span class="sxs-lookup"><span data-stu-id="c0284-120">If not, then turn on Microsoft Defender SmartScreen.</span></span> <span data-ttu-id="c0284-121">Das Beispiel im folgenden Screenshot zeigt, dass der Browser von der Organisation verwaltet wird und dass Microsoft Defender SmartScreen aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="c0284-121">The example in the following screenshot shows the browser is managed by the organization and that Microsoft Defender SmartScreen is turned on.</span></span>

   ![Aktivieren von Microsoft Edge-PUA in den Einstellungen](./media/microsoft-edge-potentially-unwanted-apps/security-pua-setup.png)

4. <span data-ttu-id="c0284-123">Verwenden Sie im Abschnitt **Dienste** den im vorhergehenden Screenshot abgebildeten Umschalter, um **Potenziell unerwünschte Apps blockieren** zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="c0284-123">In the **Services** section, use the toggle shown in the preceding screenshot to turn on **Block potentially unwanted apps**.</span></span>

   > [!TIP]
   > <span data-ttu-id="c0284-124">Sie können das URL-Blockierungsfeature des PUA-Schutzes sicher erkunden, indem Sie es auf einem unserer Windows Defender SmartScreen-[Demoseiten](https://demo.smartscreen.msft.net/) testen.</span><span class="sxs-lookup"><span data-stu-id="c0284-124">You can safely explore the URL-blocking feature of PUA protection by testing it out on one of our Windows Defender SmartScreen [demo pages](https://demo.smartscreen.msft.net/).</span></span>

<span data-ttu-id="c0284-125">Wenn Microsoft Edge eine potenziell unerwünschte Anwendung erkennt, erhalten Sie eine Meldung wie die im nächsten Screenshot gezeigte.</span><span class="sxs-lookup"><span data-stu-id="c0284-125">When Microsoft Edge detects a PUA, you will see a message like the one in the next screenshot.</span></span>

   ![PUA-Warnmeldung in Microsoft Edge](./media/microsoft-edge-potentially-unwanted-apps/security-pua-msg.png)

### <a name="to-block-against-pua-associated-urls"></a><span data-ttu-id="c0284-127">So blockieren Sie URLs, die mit PUA in Zusammenhang stehen</span><span class="sxs-lookup"><span data-stu-id="c0284-127">To block against PUA-associated URLs</span></span>

<span data-ttu-id="c0284-128">Nachdem Sie den PUA-Schutz in Microsoft Edge aktiviert haben, schützt Windows Defender SmartScreen Sie vor URLs, die mit PUA in Zusammenhang stehen.</span><span class="sxs-lookup"><span data-stu-id="c0284-128">After you turn on PUA protection in Microsoft Edge, Windows Defender SmartScreen will protect you from PUA-associated URLs.</span></span>

<span data-ttu-id="c0284-129">Es gibt mehrere Möglichkeiten, wie Administratoren die Zusammenarbeit von Microsoft Edge und Windows Defender SmartScreen konfigurieren können, um Benutzer vor URLs zu schützen, die mit PUA in Zusammenhang stehen.</span><span class="sxs-lookup"><span data-stu-id="c0284-129">There are several ways admins can configure how Microsoft Edge and Windows Defender SmartScreen work together to protect users from PUA-associated URLs.</span></span> <span data-ttu-id="c0284-130">Weitere Informationen finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="c0284-130">For more information, see:</span></span>

- [<span data-ttu-id="c0284-131">Konfigurieren der Microsoft Edge-Richtlinieneinstellungen unter Windows</span><span class="sxs-lookup"><span data-stu-id="c0284-131">Configure Microsoft Edge policy settings on Windows</span></span>](./configure-microsoft-edge.md)
- [<span data-ttu-id="c0284-132">SmartScreen-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="c0284-132">SmartScreen settings</span></span>](./microsoft-edge-policies.md#smartscreen-settings)
- [<span data-ttu-id="c0284-133">SmartScreenPuaEnabled-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="c0284-133">SmartScreenPuaEnabled policy</span></span>](./microsoft-edge-policies.md#smartscreenpuaenabled)
- [<span data-ttu-id="c0284-134">Windows Defender SmartScreen konfigurieren</span><span class="sxs-lookup"><span data-stu-id="c0284-134">Configure Windows Defender SmartScreen</span></span>](/microsoft-edge/deploy/available-policies?source=docs#configure-windows-defender-smartscreen)

<span data-ttu-id="c0284-135">Administratoren können die Microsoft Defender Advanced Threat Protection (Microsoft Defender ATP)-Blockierungsliste auch anpassen.</span><span class="sxs-lookup"><span data-stu-id="c0284-135">Admins can also customize the Microsoft Defender Advanced Threat Protection (Microsoft Defender ATP) block list.</span></span> <span data-ttu-id="c0284-136">Sie können das Microsoft Defender ATP-Portal nutzen, um [Indikatoren für IPs und URLs zu erstellen und zu verwalten](/windows/security/threat-protection/microsoft-defender-atp/manage-indicators#create-indicators-for-ips-and-urlsdomains-preview).</span><span class="sxs-lookup"><span data-stu-id="c0284-136">They can use the Microsoft Defender ATP portal to [create and manage indicators for IPs and URLs](/windows/security/threat-protection/microsoft-defender-atp/manage-indicators#create-indicators-for-ips-and-urlsdomains-preview).</span></span>

## <a name="protect-against-pua-with-windows-defender-antivirus"></a><span data-ttu-id="c0284-137">Schutz vor PUA mit Windows Defender Antivirus</span><span class="sxs-lookup"><span data-stu-id="c0284-137">Protect against PUA with Windows Defender Antivirus</span></span>

<span data-ttu-id="c0284-138">Im Artikel [Erkennen und Blockieren potenziell unerwünschter Anwendungen](/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus#windows-defender-antivirus) wird auch beschrieben, wie Sie Windows Defender Antivirus konfigurieren können, um den PUA-Schutz zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="c0284-138">The [Detect and block potentially unwanted applications](/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus#windows-defender-antivirus) article also describes how you can configure Windows Defender Antivirus to enable PUA protection.</span></span> <span data-ttu-id="c0284-139">Sie können den Schutz mit einer der folgenden Optionen konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="c0284-139">You can configure protection using any of the following options:</span></span>

- [<span data-ttu-id="c0284-140">Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="c0284-140">Microsoft Intune</span></span>](/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus#use-intune-to-configure-pua-protection)
- [<span data-ttu-id="c0284-141">Microsoft Endpoint Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="c0284-141">Microsoft Endpoint Configuration Manager</span></span>](/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus#use-configuration-manager-to-configure-pua-protection)
- [<span data-ttu-id="c0284-142">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="c0284-142">Group Policy</span></span>](/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus#use-group-policy-to-configure-pua-protection)
- [<span data-ttu-id="c0284-143">PowerShell-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="c0284-143">PowerShell cmdlets</span></span>](/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus#use-powershell-cmdlets-to-configure-pua-protection)

<span data-ttu-id="c0284-144">Erkennt Windows Defender eine PUA-Datei auf einem Endpunkt, wird die Datei isoliert, und der Benutzer wird ([sofern die Benachrichtigungen nicht deaktiviert sind](/windows/security/threat-protection/windows-defender-antivirus/configure-notifications-windows-defender-antivirus)) in derselben Form wie bei einer normalen Bedrohungserkennung benachrichtigt (mit dem Präfix "PUA:"). Erkannte Bedrohungen werden auch in der [Quarantäneliste in der Windows-Sicherheits-App](/windows/security/threat-protection/windows-defender-antivirus/windows-defender-security-center-antivirus#detection-history) aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="c0284-144">When Windows Defender detects a PUA file on an endpoint it quarantines the file and notifies the user ([unless notifications are disabled](/windows/security/threat-protection/windows-defender-antivirus/configure-notifications-windows-defender-antivirus)) in the same format as a normal threat detection (prefaced with "PUA:".) Detected threats also appear in the [quarantine list in the Windows Security app](/windows/security/threat-protection/windows-defender-antivirus/windows-defender-security-center-antivirus#detection-history).</span></span>

### <a name="pua-notifications-and-events"></a><span data-ttu-id="c0284-145">PUA-Benachrichtigungen und -Ereignisse</span><span class="sxs-lookup"><span data-stu-id="c0284-145">PUA notifications and events</span></span>

<span data-ttu-id="c0284-146">Es gibt mehrere Möglichkeiten, wie ein Administrator PUA-Ereignisse sehen kann:</span><span class="sxs-lookup"><span data-stu-id="c0284-146">There are several ways an admin can see PUA events:</span></span>

- <span data-ttu-id="c0284-147">In der Windows Ereignisanzeige, aber nicht in Microsoft Endpoint Configuration Manager oder Intune.</span><span class="sxs-lookup"><span data-stu-id="c0284-147">In the Windows Event Viewer, but not in Microsoft Endpoint Configuration Manager or Intune.</span></span>
- <span data-ttu-id="c0284-148">In einer E-Mail, wenn E-Mail-Benachrichtigungen für PUA-Funde aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="c0284-148">In an email if email notifications for PUA detections is turned on.</span></span>
- <span data-ttu-id="c0284-149">In [Windows Defender Antivirus](/windows/security/threat-protection/windows-defender-antivirus/troubleshoot-windows-defender-antivirus)-Ereignisprotokollen, in denen ein PUA-Ereignis unter der Ereignis-ID 1116 mit der folgenden Meldung erfasst wird: "Die Antischadsoftwareplattform hat Schadsoftware oder andere potenziell unerwünschte Software erkannt.</span><span class="sxs-lookup"><span data-stu-id="c0284-149">In [Windows Defender Antivirus](/windows/security/threat-protection/windows-defender-antivirus/troubleshoot-windows-defender-antivirus) event logs, where a PUA event is recorded under event ID 1116 with the message: "The antimalware platform detected malware or other potentially unwanted software."</span></span>

> [!NOTE]
> <span data-ttu-id="c0284-150">Die Benutzer sehen "\*.exe wurde von Microsoft Defender SmartScreen als potenziell unerwünschte Anwendung blockiert".</span><span class="sxs-lookup"><span data-stu-id="c0284-150">Users will see "\*.exe has been blocked as a potentially unwanted app by Microsoft Defender SmartScreen".</span></span>

### <a name="allow-list-an-app"></a><span data-ttu-id="c0284-151">Aufnehmen einer App in die Zulassungsliste</span><span class="sxs-lookup"><span data-stu-id="c0284-151">Allow-list an app</span></span>

<span data-ttu-id="c0284-152">Wie Microsoft Edge bietet auch Windows Defender Antivirus eine Möglichkeit, Dateien zuzulassen, die irrtümlich blockiert wurden oder zur Ausführung einer Aufgabe benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="c0284-152">Like Microsoft Edge, Windows Defender Antivirus provides a way to allow files that are blocked by mistake or needed to complete a task.</span></span> <span data-ttu-id="c0284-153">Wenn dies geschieht, können Sie eine Datei in die Zulassungsliste aufnehmen.</span><span class="sxs-lookup"><span data-stu-id="c0284-153">If this happens you can allow-list a file.</span></span> <span data-ttu-id="c0284-154">Weitere Informationen finden Sie unter [Konfigurieren von Endpoint Protection in Configuration Manager](/previous-versions/system-center/system-center-2012-R2/hh508770(v=technet.10)#to-exclude-specific-files-or-folders), um zu erfahren, wie Sie bestimmte Dateien oder Ordner ausschließen können.</span><span class="sxs-lookup"><span data-stu-id="c0284-154">For more information, see [How to Configure Endpoint Protection in Configuration Manager](/previous-versions/system-center/system-center-2012-R2/hh508770(v=technet.10)#to-exclude-specific-files-or-folders) to learn how to exclude specific files or folders.</span></span>

## <a name="see-also"></a><span data-ttu-id="c0284-155">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c0284-155">See also</span></span>

- [<span data-ttu-id="c0284-156">Microsoft Edge Enterprise-Angebotsseite</span><span class="sxs-lookup"><span data-stu-id="c0284-156">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="c0284-157">Schutz vor Bedrohungen</span><span class="sxs-lookup"><span data-stu-id="c0284-157">Threat protection</span></span>](/windows/security/threat-protection/index)
- [<span data-ttu-id="c0284-158">Konfigurieren von verhaltensbasiertem, heuristischem und Echtzeitschutz</span><span class="sxs-lookup"><span data-stu-id="c0284-158">Configure behavioral, heuristic, and real-time protection</span></span>](/windows/security/threat-protection/windows-defender-antivirus/configure-protection-features-windows-defender-antivirus)
- [<span data-ttu-id="c0284-159">Schutz der nächsten Generation</span><span class="sxs-lookup"><span data-stu-id="c0284-159">Next-generation protection</span></span>](/windows/security/threat-protection/windows-defender-antivirus/windows-defender-antivirus-in-windows-10)
- [<span data-ttu-id="c0284-160">Sicherheitsbaseline für Chromium-basiertes Microsoft Edge, Version 79</span><span class="sxs-lookup"><span data-stu-id="c0284-160">Security baseline for Chromium-based Microsoft Edge, version 79</span></span>](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/security-baseline-final-for-chromium-based-microsoft-edge/ba-p/1111863)