---
title: Progressive Rollouts für Microsoft Edge Stable-Kanal-Updates
ms.author: aguta
author: dan-wesley
manager: srugh
ms.date: 05/21/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Progressive Rollouts für Microsoft Edge Stable-Kanal-Updates
ms.openlocfilehash: 5b0d2f58318b10538d0470b644d346b5b9b9489b
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/31/2020
ms.locfileid: "10980010"
---
# Progressive Rollouts für Microsoft Edge Stable-Kanal-Updates

Beginnend mit Microsoft Edge, Version 83 werden wir schrittweise Rollouts der wichtigsten Updates für den Microsoft Edge Stable-Kanal über einen Zeitraum von wenigen Tagen durchführen. Dieses progressive Rollout ermöglicht es uns, Upgrades zu überwachen und den Browser organisationsweit sicher zu aktualisieren.

> [!NOTE]
> Dieser Artikel bezieht sich auf den Microsoft Edge Stable-Kanal (Version 83 oder höher).

## Warum sind progressive Rollouts erforderlich?

Durch eine genaue Überwachung des Status unserer Updates und das Rollout derselben über einen Zeitraum von mehreren Tagen können wir die Auswirkungen von Problemen begrenzen, die evtl. im Zusammenhang mit einem neuen Update auftreten. Ab Microsoft Edge, Version 83 werden progressive Rollouts für alle Windows 7-, Windows 8- und 8.1- sowie Windows 10-Versionen von Microsoft Edge aktiviert. Sobald verfügbar wird auch Microsoft Edge auf dem Mac unterstützt.

## Wie erfolgen die Updates?

Jeder Installation von Microsoft Edge wird ein Upgradewert zugewiesen. Nachdem mit dem inkrementellen Rollout begonnen wurde, wird das Update angezeigt, wenn der Wert auf Ihrem Gerät innerhalb des Wertebereiches für das Upgrade liegt. Im Laufe des Rollouts (also innerhalb weniger Tage) erhalten alle Benutzer das Update. Das Rollout von Browser-Updates mit kritischen Sicherheitsfixes erfolgt schneller als das von Updates, die keine kritischen Sicherheitsfixes umfassen. Dies geschieht, um sofortigen Schutz vor Sicherheitsrisiken zu gewährleisten.

## Wie wirkt sich dies auf Unternehmen aus?

Microsoft Edge-Produkte werden über verschiedene Mechanismen wie Microsoft Intune, Windows Server Update Service (WSUS) und Configuration Manager an Unternehmen verteilt. Diese Bereitstellungstools verhalten sich im Hinblick auf das progressive Rollout unterschiedlich:

- Unternehmen, die die Verteilung über Microsoft Intune verwalten, sind für automatische Updates registriert. Das progressive Rollout wird verwendet, und innerhalb weniger Tage erfolgt für alle Benutzer eine Aktualisierung.
- Unternehmen, die die Verteilung über WSUS (Windows Server Update Services) oder den Configuration Manager verwalten, sind nicht für automatische Updates registriert. Administratoren verwalten und übernehmen die verfügbaren Updates von Anfang an. Das progressive Rollout wirkt sich nicht auf diesen Vorgang aus.

Wenn Sie irgendwelche Anliegen oder Fragen haben, teilen Sie Ihr wertvolles Feedback mit uns über die Feedback-Schaltfläche (UserVoice) innerhalb der Anwendung, oder unten in den Kommentaren.

## Weitere Informationen

- [Angebotsseite für Microsoft Edge für Unternehmen](https://aka.ms/EdgeEnterprise)
