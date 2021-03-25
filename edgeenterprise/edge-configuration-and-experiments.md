---
title: Microsoft Edge-Konfigurationen und Experimente
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 02/20/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Edge-Konfigurationen und Experimente
ms.openlocfilehash: aef19fd9c119926a934a1ab00009a89ce2fe31fc
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/24/2021
ms.locfileid: "11447769"
---
# <a name="microsoft-edge-configurations-and-experimentation"></a><span data-ttu-id="366e6-103">Microsoft Edge-Konfigurationen und Experimente</span><span class="sxs-lookup"><span data-stu-id="366e6-103">Microsoft Edge configurations and experimentation</span></span>

<span data-ttu-id="366e6-104">In diesem Artikel wird die Interaktion zwischen Microsoft Edge und dem Experimentier- und Konfigurationsdienst (ECS) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="366e6-104">This article describes the interaction between Microsoft Edge and the Experimentation and Configuration Service (ECS).</span></span> <span data-ttu-id="366e6-105">Microsoft Edge kommuniziert mit diesem Dienst, um verschiedene Arten von Nutzlasten anzufordern und zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="366e6-105">Microsoft Edge communicates with this service to request and receive different kinds of payloads.</span></span> <span data-ttu-id="366e6-106">Zu diesen Nutzlasten gehören Konfigurationen, Feature-Rollouts und Experimente.</span><span class="sxs-lookup"><span data-stu-id="366e6-106">These payloads include configurations, feature rollouts, and experiments.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="366e6-107">Stellen Sie sicher, dass Clients auf `https://config.edge.skype.com` zugreifen können, damit Nutzlasten empfangen werden können.</span><span class="sxs-lookup"><span data-stu-id="366e6-107">Make sure clients are able to access `https://config.edge.skype.com` so payloads can be received.</span></span>

> [!NOTE]
> <span data-ttu-id="366e6-108">Dieser Artikel bezieht sich auf Microsoft Edge Version 77 oder höher.</span><span class="sxs-lookup"><span data-stu-id="366e6-108">This applies to Microsoft Edge version 77 or later.</span></span>

## <a name="configurations"></a><span data-ttu-id="366e6-109">Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="366e6-109">Configurations</span></span>

<span data-ttu-id="366e6-110">Bei Konfigurationen handelt es sich um die Nutzlast, die zur Gewährleistung der Produktintegrität, Sicherheit und Einhaltung der Datenschutzbestimmungen verwendet wird. Sie soll für alle Benutzer (basierend auf Plattformen und Kanälen) den gleichen Wert haben und kann zum Aktivieren eines Feature-Kennzeichens für eine Domänenaktion und zum Deaktivieren eines Feature-Kennzeichens im Falle eines Fehlers verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="366e6-110">Configurations are the payload meant to ensure product health, security, and privacy compliance, and are intended to have the same value for all the users (based on platforms and channels.) This could be to enable a feature flag for a domain action, and can also be used to disable a feature flag in the event of a bug.</span></span>

## <a name="controlled-feature-rollout"></a><span data-ttu-id="366e6-111">Gesteuertes Feature-Rollout</span><span class="sxs-lookup"><span data-stu-id="366e6-111">Controlled Feature Rollout</span></span>

<span data-ttu-id="366e6-112">Das gesteuerte Feature-Rollout (Controlled Feature Rollout, CFR) ist ein Verfahren zum langsamen Vergrößern der Benutzergruppe, die eine Funktion erhält.</span><span class="sxs-lookup"><span data-stu-id="366e6-112">Controlled Feature Rollout (CFR) is a procedure for slowly increasing the size of the user group that receives a feature.</span></span> <span data-ttu-id="366e6-113">Durch das Verteilen eines neuen Features an eine zufällig ausgewählte Teilmenge der Benutzerpopulation ist es möglich, das Benutzerfeedback mit einer Kontrollgruppe gleicher Größe ohne das Feature zu vergleichen, um die Auswirkung des Features zu messen.</span><span class="sxs-lookup"><span data-stu-id="366e6-113">By distributing a new feature to a randomly selected subset of the user population, it’s possible to compare user feedback to an equally sized control group without the feature to measure the impact of the feature.</span></span>

## <a name="experiments"></a><span data-ttu-id="366e6-114">Versuche</span><span class="sxs-lookup"><span data-stu-id="366e6-114">Experiments</span></span>

<span data-ttu-id="366e6-115">Microsoft Edge-Builds verfügen über Features und Funktionen, die sich noch in der Entwicklung befinden oder experimentell sind.</span><span class="sxs-lookup"><span data-stu-id="366e6-115">Microsoft Edge builds have features and functionality that are still in development or are experimental.</span></span> <span data-ttu-id="366e6-116">Experimente sind wie CFR, aber die Größe der Benutzergruppe zum Testen des neuen Konzepts ist viel kleiner.</span><span class="sxs-lookup"><span data-stu-id="366e6-116">Experiments are like CFR, but the size of the user group is much smaller for testing the new concept.</span></span> <span data-ttu-id="366e6-117">Diese Features sind standardmäßig ausgeblendet, bis das Feature bereitgestellt oder das Experiment abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="366e6-117">These features are hidden by default until the feature's rolled out or the experiment's finished.</span></span> <span data-ttu-id="366e6-118">Experiment-Kennzeichen werden verwendet, um diese Features zu aktivieren und zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="366e6-118">Experiment flags are used to enable and disable these features.</span></span>

## <a name="about-the-ecs"></a><span data-ttu-id="366e6-119">Informationen zum ECS</span><span class="sxs-lookup"><span data-stu-id="366e6-119">About the ECS</span></span>

<span data-ttu-id="366e6-120">In allen vorhergehenden Szenarien übermittelt der Dienst die Feature-Kennzeichenwerte an den Browserclient, damit sie angewendet werden können.</span><span class="sxs-lookup"><span data-stu-id="366e6-120">In all the preceding scenarios, the service delivers the feature flag values to the browser client so they can be applied.</span></span> <span data-ttu-id="366e6-121">Je nach Update werden Konfigurationen sofort oder beim Neustart des Browsers angewendet.</span><span class="sxs-lookup"><span data-stu-id="366e6-121">Depending on the update, configurations are applied immediately or when the user restarts the browser.</span></span>

<span data-ttu-id="366e6-122">Die Interaktion von Microsoft Edge mit diesem Dienst wird durch die Einstellungen der [ExperimentationAndConfigurationServiceControl](./microsoft-edge-policies.md#experimentationandconfigurationservicecontrol)-Richtlinie gesteuert.</span><span class="sxs-lookup"><span data-stu-id="366e6-122">Microsoft Edge's interaction with this service is controlled by settings in the [ExperimentationAndConfigurationServiceControl](./microsoft-edge-policies.md#experimentationandconfigurationservicecontrol) policy.</span></span> <span data-ttu-id="366e6-123">Sie können Richtlinieneinstellungen konfigurieren, um:</span><span class="sxs-lookup"><span data-stu-id="366e6-123">You can configure policy settings to:</span></span>

- <span data-ttu-id="366e6-124">Nur Konfigurationen abzurufen</span><span class="sxs-lookup"><span data-stu-id="366e6-124">Retrieve configurations only</span></span>
- <span data-ttu-id="366e6-125">Konfigurationen und Experimente abzurufen</span><span class="sxs-lookup"><span data-stu-id="366e6-125">Retrieve configurations and experiments</span></span>
- <span data-ttu-id="366e6-126">Die Kommunikation mit dem Dienst zu deaktivieren</span><span class="sxs-lookup"><span data-stu-id="366e6-126">Disable communication with the service</span></span>

  > [!CAUTION]
  > <span data-ttu-id="366e6-127">Wenn Sie die Kommunikation mit dem Dienst deaktivieren, wirkt sich dies auf die Fähigkeit von Microsoft aus, auf einen schwerwiegenden Fehler rechtzeitig zu reagieren.</span><span class="sxs-lookup"><span data-stu-id="366e6-127">If you disable communications with the service, this will affect Microsoft’s ability to respond to a severe bug in a timely manner.</span></span>

## <a name="see-also"></a><span data-ttu-id="366e6-128">Weitere Informationen:</span><span class="sxs-lookup"><span data-stu-id="366e6-128">See also</span></span>

- [<span data-ttu-id="366e6-129">Microsoft Edge Enterprise-Angebotsseite</span><span class="sxs-lookup"><span data-stu-id="366e6-129">Microsoft Edge Enterprise landing page</span></span>](https://www.microsoftedgeinsider.com/enterprise)
- [<span data-ttu-id="366e6-130">Angebotsseite der Microsoft Edge-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="366e6-130">Microsoft Edge documentation landing page</span></span>](./index.yml)