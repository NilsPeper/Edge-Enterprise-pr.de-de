---
title: Progressive Rollouts für Microsoft Edge Stable-Kanal-Updates
ms.author: aguta
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Progressive Rollouts für Microsoft Edge Stable-Kanal-Updates
ms.openlocfilehash: d11fd825c7f4de37fe0b6555f503d9a496fb2b427a9645489a165c91490ff5d7
ms.sourcegitcommit: d44c0997ffe40d67421312ed96e7766da947eaa0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "11724858"
---
# <a name="progressive-rollouts-for-microsoft-edge-stable-channel-updates"></a>Progressive Rollouts für Microsoft Edge Stable-Kanal-Updates

Beginnend mit Microsoft Edge, Version 83 werden wir schrittweise Rollouts der wichtigsten Updates für den Microsoft Edge Stable-Kanal über einen Zeitraum von wenigen Tagen durchführen. Dieses progressive Rollout ermöglicht es uns, Upgrades zu überwachen und den Browser organisationsweit sicher zu aktualisieren.

> [!NOTE]
> Dieser Artikel bezieht sich auf den Microsoft Edge Stable-Kanal (Version 83 oder höher).

## <a name="why-do-we-need-progressive-rollout"></a>Warum sind progressive Rollouts erforderlich?

Durch eine genaue Überwachung des Status unserer Updates und das Rollout derselben über einen Zeitraum von mehreren Tagen können wir die Auswirkungen von Problemen begrenzen, die evtl. im Zusammenhang mit einem neuen Update auftreten. Ab Microsoft Edge, Version 83 werden progressive Rollouts für alle Windows 7-, Windows 8- und 8.1- sowie Windows 10-Versionen von Microsoft Edge aktiviert. Sobald verfügbar wird auch Microsoft Edge auf dem Mac unterstützt.

## <a name="how-will-the-updates-work"></a>Wie erfolgen die Updates?

Jeder Installation von Microsoft Edge wird ein Upgradewert zugewiesen. Nachdem mit dem inkrementellen Rollout begonnen wurde, wird das Update angezeigt, wenn der Wert auf Ihrem Gerät innerhalb des Wertebereiches für das Upgrade liegt. Im Laufe des Rollouts (also innerhalb weniger Tage) erhalten alle Benutzer das Update. Das Rollout von Browser-Updates mit kritischen Sicherheitsfixes erfolgt schneller als das von Updates, die keine kritischen Sicherheitsfixes umfassen. Dies geschieht, um sofortigen Schutz vor Sicherheitsrisiken zu gewährleisten.

## <a name="how-does-this-affect-enterprises"></a>Wie wirkt sich dies auf Unternehmen aus?

Microsoft Edge-Produkte werden über verschiedene Mechanismen wie Microsoft Intune, Windows Server Update Service (WSUS) und Configuration Manager an Unternehmen verteilt. Diese Bereitstellungstools verhalten sich im Hinblick auf das progressive Rollout unterschiedlich:

- Unternehmen, die die Verteilung über Microsoft Intune verwalten, sind für automatische Updates registriert. Das progressive Rollout wird verwendet, und innerhalb weniger Tage erfolgt für alle Benutzer eine Aktualisierung.
- Unternehmen, die die Verteilung über WSUS (Windows Server Update Services) oder den Configuration Manager verwalten, sind nicht für automatische Updates registriert. Administratoren verwalten und übernehmen die verfügbaren Updates von Anfang an. Das progressive Rollout wirkt sich nicht auf diesen Vorgang aus.

Wenn Sie irgendwelche Anliegen oder Fragen haben, teilen Sie Ihr wertvolles Feedback mit uns über die Feedback-Schaltfläche (UserVoice) innerhalb der Anwendung, oder unten in den Kommentaren.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)
