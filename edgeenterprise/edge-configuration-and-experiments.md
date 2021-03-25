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
# <a name="microsoft-edge-configurations-and-experimentation"></a>Microsoft Edge-Konfigurationen und Experimente

In diesem Artikel wird die Interaktion zwischen Microsoft Edge und dem Experimentier- und Konfigurationsdienst (ECS) beschrieben. Microsoft Edge kommuniziert mit diesem Dienst, um verschiedene Arten von Nutzlasten anzufordern und zu empfangen. Zu diesen Nutzlasten gehören Konfigurationen, Feature-Rollouts und Experimente.

> [!IMPORTANT]
> Stellen Sie sicher, dass Clients auf `https://config.edge.skype.com` zugreifen können, damit Nutzlasten empfangen werden können.

> [!NOTE]
> Dieser Artikel bezieht sich auf Microsoft Edge Version 77 oder höher.

## <a name="configurations"></a>Konfigurationen

Bei Konfigurationen handelt es sich um die Nutzlast, die zur Gewährleistung der Produktintegrität, Sicherheit und Einhaltung der Datenschutzbestimmungen verwendet wird. Sie soll für alle Benutzer (basierend auf Plattformen und Kanälen) den gleichen Wert haben und kann zum Aktivieren eines Feature-Kennzeichens für eine Domänenaktion und zum Deaktivieren eines Feature-Kennzeichens im Falle eines Fehlers verwendet werden.

## <a name="controlled-feature-rollout"></a>Gesteuertes Feature-Rollout

Das gesteuerte Feature-Rollout (Controlled Feature Rollout, CFR) ist ein Verfahren zum langsamen Vergrößern der Benutzergruppe, die eine Funktion erhält. Durch das Verteilen eines neuen Features an eine zufällig ausgewählte Teilmenge der Benutzerpopulation ist es möglich, das Benutzerfeedback mit einer Kontrollgruppe gleicher Größe ohne das Feature zu vergleichen, um die Auswirkung des Features zu messen.

## <a name="experiments"></a>Versuche

Microsoft Edge-Builds verfügen über Features und Funktionen, die sich noch in der Entwicklung befinden oder experimentell sind. Experimente sind wie CFR, aber die Größe der Benutzergruppe zum Testen des neuen Konzepts ist viel kleiner. Diese Features sind standardmäßig ausgeblendet, bis das Feature bereitgestellt oder das Experiment abgeschlossen ist. Experiment-Kennzeichen werden verwendet, um diese Features zu aktivieren und zu deaktivieren.

## <a name="about-the-ecs"></a>Informationen zum ECS

In allen vorhergehenden Szenarien übermittelt der Dienst die Feature-Kennzeichenwerte an den Browserclient, damit sie angewendet werden können. Je nach Update werden Konfigurationen sofort oder beim Neustart des Browsers angewendet.

Die Interaktion von Microsoft Edge mit diesem Dienst wird durch die Einstellungen der [ExperimentationAndConfigurationServiceControl](./microsoft-edge-policies.md#experimentationandconfigurationservicecontrol)-Richtlinie gesteuert. Sie können Richtlinieneinstellungen konfigurieren, um:

- Nur Konfigurationen abzurufen
- Konfigurationen und Experimente abzurufen
- Die Kommunikation mit dem Dienst zu deaktivieren

  > [!CAUTION]
  > Wenn Sie die Kommunikation mit dem Dienst deaktivieren, wirkt sich dies auf die Fähigkeit von Microsoft aus, auf einen schwerwiegenden Fehler rechtzeitig zu reagieren.

## <a name="see-also"></a>Weitere Informationen:

- [Microsoft Edge Enterprise-Angebotsseite](https://www.microsoftedgeinsider.com/enterprise)
- [Angebotsseite der Microsoft Edge-Dokumentation](./index.yml)