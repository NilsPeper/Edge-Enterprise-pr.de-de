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
ms.openlocfilehash: f66da4075c33c1f375dfb593c1a1bd2b4a139833
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979950"
---
# <span data-ttu-id="425f8-103">Microsoft Edge-Konfigurationen und Experimente</span><span class="sxs-lookup"><span data-stu-id="425f8-103">Microsoft Edge configurations and experimentation</span></span>

<span data-ttu-id="425f8-104">In diesem Artikel wird die Interaktion zwischen Microsoft Edge und dem Experimentier- und Konfigurationsdienst (ECS) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="425f8-104">This article describes the interaction between Microsoft Edge and the Experimentation and Configuration Service (ECS).</span></span> <span data-ttu-id="425f8-105">Microsoft Edge kommuniziert mit diesem Dienst, um verschiedene Arten von Nutzlasten anzufordern und zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="425f8-105">Microsoft Edge communicates with this service to request and receive different kinds of payloads.</span></span> <span data-ttu-id="425f8-106">Zu diesen Nutzlasten gehören Konfigurationen, Feature-Rollouts und Experimente.</span><span class="sxs-lookup"><span data-stu-id="425f8-106">These payloads include configurations, feature rollouts, and experiments.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="425f8-107">Stellen Sie sicher, dass Clients auf `https://config.edge.skype.com` zugreifen können, damit Nutzlasten empfangen werden können.</span><span class="sxs-lookup"><span data-stu-id="425f8-107">Make sure clients are able to access `https://config.edge.skype.com` so payloads can be received.</span></span>

> [!NOTE]
> <span data-ttu-id="425f8-108">Dieser Artikel bezieht sich auf Microsoft Edge Version 77 oder höher.</span><span class="sxs-lookup"><span data-stu-id="425f8-108">This applies to Microsoft Edge version 77 or later.</span></span>

## <span data-ttu-id="425f8-109">Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="425f8-109">Configurations</span></span>

<span data-ttu-id="425f8-110">Bei Konfigurationen handelt es sich um die Nutzlast, die zur Gewährleistung der Produktintegrität, Sicherheit und Einhaltung der Datenschutzbestimmungen verwendet wird. Sie soll für alle Benutzer (basierend auf Plattformen und Kanälen) den gleichen Wert haben und kann zum Aktivieren eines Feature-Kennzeichens für eine Domänenaktion und zum Deaktivieren eines Feature-Kennzeichens im Falle eines Fehlers verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="425f8-110">Configurations are the payload meant to ensure product health, security, and privacy compliance, and are intended to have the same value for all the users (based on platforms and channels.) This could be to enable a feature flag for a domain action, and can also be used to disable a feature flag in the event of a bug.</span></span>

## <span data-ttu-id="425f8-111">Gesteuertes Feature-Rollout</span><span class="sxs-lookup"><span data-stu-id="425f8-111">Controlled Feature Rollout</span></span>

<span data-ttu-id="425f8-112">Das gesteuerte Feature-Rollout (Controlled Feature Rollout, CFR) ist ein Verfahren zum langsamen Vergrößern der Benutzergruppe, die eine Funktion erhält.</span><span class="sxs-lookup"><span data-stu-id="425f8-112">Controlled Feature Rollout (CFR) is a procedure for slowly increasing the size of the user group that receives a feature.</span></span> <span data-ttu-id="425f8-113">Durch das Verteilen eines neuen Features an eine zufällig ausgewählte Teilmenge der Benutzerpopulation ist es möglich, das Benutzerfeedback mit einer Kontrollgruppe gleicher Größe ohne das Feature zu vergleichen, um die Auswirkung des Features zu messen.</span><span class="sxs-lookup"><span data-stu-id="425f8-113">By distributing a new feature to a randomly selected subset of the user population, it’s possible to compare user feedback to an equally sized control group without the feature to measure the impact of the feature.</span></span>

## <span data-ttu-id="425f8-114">Versuche</span><span class="sxs-lookup"><span data-stu-id="425f8-114">Experiments</span></span>

<span data-ttu-id="425f8-115">Microsoft Edge-Builds verfügen über Features und Funktionen, die sich noch in der Entwicklung befinden oder experimentell sind.</span><span class="sxs-lookup"><span data-stu-id="425f8-115">Microsoft Edge builds have features and functionality that are still in development or are experimental.</span></span> <span data-ttu-id="425f8-116">Experimente sind wie CFR, aber die Größe der Benutzergruppe zum Testen des neuen Konzepts ist viel kleiner.</span><span class="sxs-lookup"><span data-stu-id="425f8-116">Experiments are like CFR, but the size of the user group is much smaller for testing the new concept.</span></span> <span data-ttu-id="425f8-117">Diese Features sind standardmäßig ausgeblendet, bis das Feature bereitgestellt oder das Experiment abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="425f8-117">These features are hidden by default until the feature's rolled out or the experiment's finished.</span></span> <span data-ttu-id="425f8-118">Experiment-Kennzeichen werden verwendet, um diese Features zu aktivieren und zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="425f8-118">Experiment flags are used to enable and disable these features.</span></span>

## <span data-ttu-id="425f8-119">Informationen zum ECS</span><span class="sxs-lookup"><span data-stu-id="425f8-119">About the ECS</span></span>

<span data-ttu-id="425f8-120">In allen vorhergehenden Szenarien übermittelt der Dienst die Feature-Kennzeichenwerte an den Browserclient, damit sie angewendet werden können.</span><span class="sxs-lookup"><span data-stu-id="425f8-120">In all the preceding scenarios, the service delivers the feature flag values to the browser client so they can be applied.</span></span> <span data-ttu-id="425f8-121">Je nach Update werden Konfigurationen sofort oder beim Neustart des Browsers angewendet.</span><span class="sxs-lookup"><span data-stu-id="425f8-121">Depending on the update, configurations are applied immediately or when the user restarts the browser.</span></span>

<span data-ttu-id="425f8-122">Die Interaktion von Microsoft Edge mit diesem Dienst wird durch die Einstellungen der [ExperimentationAndConfigurationServiceControl](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#experimentationandconfigurationservicecontrol)-Richtlinie gesteuert.</span><span class="sxs-lookup"><span data-stu-id="425f8-122">Microsoft Edge's interaction with this service is controlled by settings in the [ExperimentationAndConfigurationServiceControl](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#experimentationandconfigurationservicecontrol) policy.</span></span> <span data-ttu-id="425f8-123">Sie können Richtlinieneinstellungen konfigurieren, um:</span><span class="sxs-lookup"><span data-stu-id="425f8-123">You can configure policy settings to:</span></span>

- <span data-ttu-id="425f8-124">Nur Konfigurationen abzurufen</span><span class="sxs-lookup"><span data-stu-id="425f8-124">Retrieve configurations only</span></span>
- <span data-ttu-id="425f8-125">Konfigurationen und Experimente abzurufen</span><span class="sxs-lookup"><span data-stu-id="425f8-125">Retrieve configurations and experiments</span></span>
- <span data-ttu-id="425f8-126">Die Kommunikation mit dem Dienst zu deaktivieren</span><span class="sxs-lookup"><span data-stu-id="425f8-126">Disable communication with the service</span></span>

  > [!CAUTION]
  > <span data-ttu-id="425f8-127">Wenn Sie die Kommunikation mit dem Dienst deaktivieren, wirkt sich dies auf die Fähigkeit von Microsoft aus, auf einen schwerwiegenden Fehler rechtzeitig zu reagieren.</span><span class="sxs-lookup"><span data-stu-id="425f8-127">If you disable communications with the service, this will affect Microsoft’s ability to respond to a severe bug in a timely manner.</span></span>

## <span data-ttu-id="425f8-128">Weitere Informationen:</span><span class="sxs-lookup"><span data-stu-id="425f8-128">See also</span></span>

- [<span data-ttu-id="425f8-129">Microsoft Edge Enterprise-Angebotsseite</span><span class="sxs-lookup"><span data-stu-id="425f8-129">Microsoft Edge Enterprise landing page</span></span>](https://www.microsoftedgeinsider.com/enterprise)
- [<span data-ttu-id="425f8-130">Angebotsseite der Microsoft Edge-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="425f8-130">Microsoft Edge documentation landing page</span></span>](https://docs.microsoft.com/DeployEdge/)
