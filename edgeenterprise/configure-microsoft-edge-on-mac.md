---
title: Konfigurieren von MicrosoftEdge für macOS mithilfe einer Eigenschaftsliste (.plist)
ms.author: brianalt
author: kelleyvice-msft
manager: laurawi
ms.date: 11/30/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Konfigurieren der Microsoft Edge-Richtlinieneinstellungen unter macOS mithilfe einer Eigenschaftsliste (.plist)
ms.openlocfilehash: abe110ab3589cc9276f28590273ece2d372be3b8
ms.sourcegitcommit: ed6a5afabf909df87bec48671c4c47bcdfaeb7bc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/02/2020
ms.locfileid: "11194686"
---
# <span data-ttu-id="c14b2-103">Konfigurieren der Microsoft Edge-Richtlinieneinstellungen für macOS mithilfe einer Eigenschaftsliste (.plist)</span><span class="sxs-lookup"><span data-stu-id="c14b2-103">Configure Microsoft Edge policy settings for macOS using a .plist</span></span>

<span data-ttu-id="c14b2-104">In diesem Artikel wird beschrieben, wie Sie Microsoft Edge auf macOS mithilfe einer Eigenschaftslistendatei (.plist) konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="c14b2-104">This article describes how to configure Microsoft Edge on macOS using a property list (.plist) file.</span></span> <span data-ttu-id="c14b2-105">Sie erfahren, wie Sie diese Datei erstellen und dann auf Microsoft Intune bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="c14b2-105">You'll learn how to create this file and then deploy it to Microsoft Intune.</span></span>

<span data-ttu-id="c14b2-106">Weitere Informationen finden Sie unter [Informationen zu Eigenschaftslistendateien](https://developer.apple.com/library/archive/documentation/General/Reference/InfoPlistKeyReference/Articles/AboutInformationPropertyListFiles.html) (Apple-Website) und [Benutzerdefinierte Nutzlast-Einstellungen](https://support.apple.com/guide/mdm/custom-mdm9abbdbe7/1/web/1).</span><span class="sxs-lookup"><span data-stu-id="c14b2-106">For more information, see [About Information Property List Files](https://developer.apple.com/library/archive/documentation/General/Reference/InfoPlistKeyReference/Articles/AboutInformationPropertyListFiles.html) (Apple's website) and [Custom payload settings](https://support.apple.com/guide/mdm/custom-mdm9abbdbe7/1/web/1).</span></span>

> [!NOTE]
> <span data-ttu-id="c14b2-107">Dieser Artikel bezieht sich auf Microsoft Edge Version 77 oder höher.</span><span class="sxs-lookup"><span data-stu-id="c14b2-107">This article applies to Microsoft Edge version 77 or later.</span></span>

## <span data-ttu-id="c14b2-108">Konfigurieren der Microsoft Edge-Richtlinien unter macOS</span><span class="sxs-lookup"><span data-stu-id="c14b2-108">Configure Microsoft Edge policies on macOS</span></span>

<span data-ttu-id="c14b2-109">Der erste Schritt besteht darin, eine \*Übermittlung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c14b2-109">The first step is to create your plist.</span></span> <span data-ttu-id="c14b2-110">Sie können die plist-Datei mit einem beliebigen Text-Editor erstellen oder Sie können das [Konfigurationsprofil mithilfe von Terminal erstellen](#create-a-configuration-profile-using-terminal).</span><span class="sxs-lookup"><span data-stu-id="c14b2-110">You can create the plist file with any text editor or you can use [Terminal to create the configuration profile](#create-a-configuration-profile-using-terminal).</span></span> <span data-ttu-id="c14b2-111">Es ist jedoch einfacher, eine plist-Datei mit einem Tool zu erstellen und zu bearbeiten, das den XML-Code für Sie formatiert.</span><span class="sxs-lookup"><span data-stu-id="c14b2-111">However, it's easier to create and edit a plist file using a tool that formats the XML code for you.</span></span> <span data-ttu-id="c14b2-112">*Xcode* ist eine ﻿kostenlose integrierte Entwicklungsumgebung, die Sie von einem der folgenden Speicherorte abrufen können:</span><span class="sxs-lookup"><span data-stu-id="c14b2-112">*Xcode* is a free integrated development environment that you can get from one of the following locations:</span></span>

- [<span data-ttu-id="c14b2-113">Apple Developer-Website</span><span class="sxs-lookup"><span data-stu-id="c14b2-113">Apple developer website</span></span>](https://developer.apple.com/xcode/)
- [<span data-ttu-id="c14b2-114">Mac App Store</span><span class="sxs-lookup"><span data-stu-id="c14b2-114">Mac App Store</span></span>](https://apps.apple.com/app/xcode/id497799835?mt=12)

<span data-ttu-id="c14b2-115">Eine liste der unterstützten Richtlinien und ihrer bevorzugten Schlüsselnamen finden Sie in der [Microsoft Edge Referenz für Browserrichtlinien](microsoft-edge-policies.md).</span><span class="sxs-lookup"><span data-stu-id="c14b2-115">For a list of supported policies and their preference key names, see [Microsoft Edge browser policies reference](microsoft-edge-policies.md).</span></span> <span data-ttu-id="c14b2-116">In der Richtlinienvorlagendatei, die von der [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise) heruntergeladen werden kann, befindet sich im Ordner **Beispiele** ein Beispiel für plist (*itadminexample.plist*).</span><span class="sxs-lookup"><span data-stu-id="c14b2-116">In the policy templates file, which can be downloaded from the [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise), there's an example plist (*itadminexample.plist*) in the **examples** folder.</span></span> <span data-ttu-id="c14b2-117">Die Beispieldatei enthält alle unterstützten Datentypen, die Sie anpassen können, um die Richtlinieneinstellungen zu definieren.</span><span class="sxs-lookup"><span data-stu-id="c14b2-117">The example file contains all supported data types that you can customize to define your policy settings.</span></span> 

<span data-ttu-id="c14b2-118">Der nächste Schritt, nachdem Sie den Inhalt Ihrer plist-Datei erstellt haben, besteht darin, diese unter Verwendung der Microsoft Edge-Einstellungsdomäne *com.microsoft.edge* zu benennen.</span><span class="sxs-lookup"><span data-stu-id="c14b2-118">The next step after you create the contents of your plist, is to name it using the Microsoft Edge preference domain, *com.microsoft.Edge*.</span></span> <span data-ttu-id="c14b2-119">Der Name unterscheidet zwischen Groß- und Kleinschreibung und sollte nicht den Kanal enthalten, auf den Sie abzielen, da er für alle Microsoft Edge-Kanäle gilt.</span><span class="sxs-lookup"><span data-stu-id="c14b2-119">The name is case sensitive and should not include the channel you are targeting because it applies to all Microsoft Edge channels.</span></span> <span data-ttu-id="c14b2-120">Der plist-Dateiname muss **_com.microsoft.Edge.plist_** lauten.</span><span class="sxs-lookup"><span data-stu-id="c14b2-120">The plist file name must be **_com.microsoft.Edge.plist_**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c14b2-121">Ab dem Build 78.0.249.2 werden alle Microsoft Edge-Kanäle auf macOS aus der Einstellungsdomäne **com.microsoft.Edge** eingelesen.</span><span class="sxs-lookup"><span data-stu-id="c14b2-121">Starting with build 78.0.249.2, all Microsoft Edge channels on macOS read from the **com.microsoft.Edge** preference domain.</span></span> <span data-ttu-id="c14b2-122">Alle früheren Versionen wurden aus einer kanalspezifischen Domäne eingelesen, z. B. **com.microsoft.Edge.Dev** für den Dev Channel.</span><span class="sxs-lookup"><span data-stu-id="c14b2-122">All prior releases read from a channel specific domain, such as **com.microsoft.Edge.Dev** for Dev channel.</span></span>

<span data-ttu-id="c14b2-123">Der letzte Schritt besteht darin, Ihre Eigenschaftsliste auf den Mac-Geräten Ihrer Benutzer mit Ihrem bevorzugten MDM-Anbieter bereitzustellen, z.B. Microsoft Intune.</span><span class="sxs-lookup"><span data-stu-id="c14b2-123">The last step is to deploy your plist to your users' Mac devices using your preferred MDM provider, such as Microsoft Intune.</span></span> <span data-ttu-id="c14b2-124">Anweisungen finden Sie unter [Bereitstellen Ihrer plist](#deploy-your-plist)..</span><span class="sxs-lookup"><span data-stu-id="c14b2-124">For instructions see [Deploy your plist](#deploy-your-plist).</span></span>

### <span data-ttu-id="c14b2-125">Erstellen eines Konfigurationsprofils mithilfe von Terminal</span><span class="sxs-lookup"><span data-stu-id="c14b2-125">Create a configuration profile using Terminal</span></span>

1. <span data-ttu-id="c14b2-126">Verwenden Sie in Terminal den folgenden Befehl, um eine plist für Microsoft Edge auf Ihrem Desktop mit den bevorzugten Einstellungen zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="c14b2-126">In Terminal, use the following command to create a plist for Microsoft Edge on your desktop with your preferred settings:</span></span>

   ```cmd
   /usr/bin/defaults write ~/Desktop/com.microsoft.Edge.plist RestoreOnStartup -int 1
   ```

2. <span data-ttu-id="c14b2-127">Konvertieren Sie die plist aus dem Binärformat in das Nur-Text-Format:</span><span class="sxs-lookup"><span data-stu-id="c14b2-127">Convert the plist from binary to plain text format:</span></span>

   ```cmd
   /usr/bin/plutil -convert xml1 ~/Desktop/com.microsoft.Edge.plist
   ```

<span data-ttu-id="c14b2-128">Stellen Sie nach dem Konvertieren der Datei sicher, dass die Richtliniendaten korrekt sind und die gewünschten Einstellungen für Ihr Konfigurationsprofil enthalten.</span><span class="sxs-lookup"><span data-stu-id="c14b2-128">After converting the file verify that your policy data is correct and contains the settings you want for your configuration profile.</span></span>

> [!NOTE]
> <span data-ttu-id="c14b2-129">Im Inhalt der plist- oder xml-Datei dürfen nur Schlüssel-Werte-Paare enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="c14b2-129">Only key value pairs should be in the contents of the plist or xml file.</span></span> <span data-ttu-id="c14b2-130">Entfernen Sie vor dem Hochladen Ihrer Datei in Intune alle \<plist>- und \<dict>-Werte und XML-Header aus der Datei.</span><span class="sxs-lookup"><span data-stu-id="c14b2-130">Prior to uploading your file into Intune remove all the \<plist> and \<dict> values, and xml headers from your file.</span></span> <span data-ttu-id="c14b2-131">Die Datei darf nur Schlüssel-Wert Paare enthalten.</span><span class="sxs-lookup"><span data-stu-id="c14b2-131">The file should only contain key value pairs.</span></span>

## <span data-ttu-id="c14b2-132">Bereitstellen Ihrer plist</span><span class="sxs-lookup"><span data-stu-id="c14b2-132">Deploy your plist</span></span>

<span data-ttu-id="c14b2-133">Erstellen Sie für Microsoft Intune ein neues Gerätekonfigurationsprofil, das auf die macOS-Plattform ausgerichtet ist, und wählen Sie den Profiltyp *Einstellungsdatei* aus.</span><span class="sxs-lookup"><span data-stu-id="c14b2-133">For Microsoft Intune create a new device configuration profile targeting the macOS platform and select the *Preference file* profile type.</span></span> <span data-ttu-id="c14b2-134">Richten Sie **com.microsoft.Edge** als bevorzugten Domänennamen ein und laden Sie Ihre Eigenschaftsliste hoch.</span><span class="sxs-lookup"><span data-stu-id="c14b2-134">Target **com.microsoft.Edge** as the preference domain name and upload your plist.</span></span> <span data-ttu-id="c14b2-135">Weitere Informationen finden Sie unter [Hinzufügen einer Eigenschaftslistendatei zu macOS-Geräten mithilfe von Microsoft Intune](https://docs.microsoft.com/intune/configuration/preference-file-settings-macos).</span><span class="sxs-lookup"><span data-stu-id="c14b2-135">For more information see [Add a property list file to macOS devices using Microsoft Intune](https://docs.microsoft.com/intune/configuration/preference-file-settings-macos).</span></span>

<span data-ttu-id="c14b2-136">Laden Sie für Jamf die Eigenschaftslistendatei als Nutzlast für *Benutzerdefinierte Einstellungen* hoch.</span><span class="sxs-lookup"><span data-stu-id="c14b2-136">For Jamf upload the .plist file as a *Custom Settings* payload.</span></span>

## <span data-ttu-id="c14b2-137">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c14b2-137">See also</span></span>

- [<span data-ttu-id="c14b2-138">Microsoft Edge Enterprise-Angebotsseite</span><span class="sxs-lookup"><span data-stu-id="c14b2-138">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="c14b2-139">Konfigurieren für macOS mit Jamf</span><span class="sxs-lookup"><span data-stu-id="c14b2-139">Configure for macOS with Jamf</span></span>](configure-microsoft-edge-on-mac-jamf.md)
- [<span data-ttu-id="c14b2-140">Konfigurieren für Windows</span><span class="sxs-lookup"><span data-stu-id="c14b2-140">Configure for Windows</span></span>](configure-microsoft-edge.md)
- [<span data-ttu-id="c14b2-141">Konfigurieren für Windows mit Intune</span><span class="sxs-lookup"><span data-stu-id="c14b2-141">Configure for Windows with Intune</span></span>](configure-edge-with-intune.md)
