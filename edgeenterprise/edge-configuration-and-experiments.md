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
# Microsoft Edge-Konfigurationen und Experimente

In diesem Artikel wird die Interaktion zwischen Microsoft Edge und dem Experimentier- und Konfigurationsdienst (ECS) beschrieben. Microsoft Edge kommuniziert mit diesem Dienst, um verschiedene Arten von Nutzlasten anzufordern und zu empfangen. Zu diesen Nutzlasten gehören Konfigurationen, Feature-Rollouts und Experimente.

> [!IMPORTANT]
> Stellen Sie sicher, dass Clients auf `https://config.edge.skype.com` zugreifen können, damit Nutzlasten empfangen werden können.

> [!NOTE]
> Dieser Artikel bezieht sich auf Microsoft Edge Version 77 oder höher.

## Konfigurationen

Bei Konfigurationen handelt es sich um die Nutzlast, die zur Gewährleistung der Produktintegrität, Sicherheit und Einhaltung der Datenschutzbestimmungen verwendet wird. Sie soll für alle Benutzer (basierend auf Plattformen und Kanälen) den gleichen Wert haben und kann zum Aktivieren eines Feature-Kennzeichens für eine Domänenaktion und zum Deaktivieren eines Feature-Kennzeichens im Falle eines Fehlers verwendet werden.

## Gesteuertes Feature-Rollout

Das gesteuerte Feature-Rollout (Controlled Feature Rollout, CFR) ist ein Verfahren zum langsamen Vergrößern der Benutzergruppe, die eine Funktion erhält. Durch das Verteilen eines neuen Features an eine zufällig ausgewählte Teilmenge der Benutzerpopulation ist es möglich, das Benutzerfeedback mit einer Kontrollgruppe gleicher Größe ohne das Feature zu vergleichen, um die Auswirkung des Features zu messen.

## Versuche

Microsoft Edge-Builds verfügen über Features und Funktionen, die sich noch in der Entwicklung befinden oder experimentell sind. Experimente sind wie CFR, aber die Größe der Benutzergruppe zum Testen des neuen Konzepts ist viel kleiner. Diese Features sind standardmäßig ausgeblendet, bis das Feature bereitgestellt oder das Experiment abgeschlossen ist. Experiment-Kennzeichen werden verwendet, um diese Features zu aktivieren und zu deaktivieren.

## Informationen zum ECS

In allen vorhergehenden Szenarien übermittelt der Dienst die Feature-Kennzeichenwerte an den Browserclient, damit sie angewendet werden können. Je nach Update werden Konfigurationen sofort oder beim Neustart des Browsers angewendet.

Die Interaktion von Microsoft Edge mit diesem Dienst wird durch die Einstellungen der [ExperimentationAndConfigurationServiceControl](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#experimentationandconfigurationservicecontrol)-Richtlinie gesteuert. Sie können Richtlinieneinstellungen konfigurieren, um:

- Nur Konfigurationen abzurufen
- Konfigurationen und Experimente abzurufen
- Die Kommunikation mit dem Dienst zu deaktivieren

  > [!CAUTION]
  > Wenn Sie die Kommunikation mit dem Dienst deaktivieren, wirkt sich dies auf die Fähigkeit von Microsoft aus, auf einen schwerwiegenden Fehler rechtzeitig zu reagieren.

## Weitere Informationen:

- [Microsoft Edge Enterprise-Angebotsseite](https://www.microsoftedgeinsider.com/enterprise)
- [Angebotsseite der Microsoft Edge-Dokumentation](https://docs.microsoft.com/DeployEdge/)
