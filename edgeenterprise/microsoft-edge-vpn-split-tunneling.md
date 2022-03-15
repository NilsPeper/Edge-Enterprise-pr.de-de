---
title: Microsoft Edge- und Split-Tunnel-VPN-Unterstützung für WebRTC
ms.author: juso
author: dan-wesley
manager: harneets
ms.date: 01/24/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Aktivieren der VPN-Unterstützung für Microsoft Edge und geteilten Tunnel für WebRTC (Web Real-Time Communication)
ms.openlocfilehash: 73bd6494ebb95db23d2701cc9dab4023af28eb70
ms.sourcegitcommit: 556aca8dde42dd66364427f095e8e473b86651a0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2022
ms.locfileid: "12445938"
---
# <a name="split-tunnel-vpn-support-for-webrtc-web-real-time-communication"></a>Split-Tunnel-VPN-Unterstützung für WebRTC (Web Real-Time Communication)
  
In diesem Artikel wird Microsoft Edge- und Split-Tunnel-VPN-Unterstützung für WebRTC beschrieben. Mit dieser Unterstützung können Unternehmenskunden den Vorteil eines geteilten VPN-Tunnels für Peer-to-Peer-Datenverkehr auf Microsoft Edge nutzen. Das geteilte VPN-Tunneling verbessert die Peer-to-Peer-Medienstreamingqualität für Benutzer und reduziert die VPN-Serverlast.

> [!NOTE]
> Dieser Artikel bezieht sich auf Microsoft Edge Version 96 oder höher.

## <a name="what-is-vpn-split-tunneling-and-why-should-i-use-it"></a>Was ist geteilter VPN-Tunnel und warum sollte ich ihn verwenden?

Das geteilte VPN-Tunneling ist ein Feature, das es Benutzern ermöglicht, zwei verschiedene Netzwerke für Datenverkehr zu verwenden, anstatt den gesamten Datenverkehr über ein VPN zu leiten. Windows hat dieses Feature für systemeigene Anwendungen unterstützt, und das geteilte VPN-Tunneling wird auch für Microsoft 365 Anwendungen über VPN Split Tunneling auf Windows angeboten. Weitere Informationen finden Sie unter [Übersicht: GETEILTES VPN-Tunneling mit Office 365 – Microsoft 365 Enterprise](/microsoft-365/enterprise/microsoft-365-vpn-split-tunnel?view=o365-worldwide&preserve-view=true). Microsoft Edge hat auch die Konfiguration des geteilten VPN-Tunnels berücksichtigt, aber die Unterstützung für den Peer-to-Peer-Datenverkehr fehlte.

Wir haben von den Kundenanforderungen für das Routing von Peer-to-Peer-Benutzerdatenverkehr über das Unternehmensnetzwerk oder die Cloudinfrastruktur über VPN gehört.Sie waren frustriert über die Qualität der Videokonferenzanrufe ihrer Benutzer in Browsern im Vergleich zu nativen Anwendungen.Wie die systemeigene Erfahrung zeigt, kann das geteilte VPN-Tunneling für Peer-to-Peer-Datenverkehr die Qualität von Benutzervideoanrufen verbessern, indem es über normale Internetverbindungen anstelle von VPN weitergeleitet wird. Es kann auch die gesamte VPN-Serverlast reduzieren, indem der festgelegte Datenverkehr von einem VPN weitergeleitet wird. Microsoft Edge bringt diese Verbesserung des Peer-to-Peer-Datenverkehrs jetzt für Unternehmenskunden.

## <a name="how-to-configure-vpn-split-tunneling-on-microsoft-edge"></a>Konfigurieren des geteilten VPN-Tunnels auf Microsoft Edge

Um das geteilte VPN-Tunneling zu aktivieren und die Netzwerke für Ihre Benutzer zu konfigurieren, empfehlen wir Ihnen, mit der Anleitung zum [Implementieren des geteilten VPN-Tunnels für Office 365 - Microsoft 365 Enterprise](/microsoft-365/enterprise/microsoft-365-vpn-implement-split-tunnel?view=o365-worldwide&preserve-view=true) zu beginnen. Da die richtige Routingtabelle basierend auf den im vorherigen Artikel beschriebenen Informationen konfiguriert ist, müssen Sie lediglich den zusätzlichen Schritt zum Aktivieren der [WebRtcRespectOsRoutingTableEnabled-Richtlinie](/deployedge/microsoft-edge-policies#webrtcrespectosroutingtableenabled) ausführen. Diese Richtlinie ermöglicht die Unterstützung Windows Regeln für die Routingtabelle des Betriebssystems, wenn Peer-to-Peer-Verbindungen über WebRTC hergestellt werden. Jetzt können Sie ein verbessertes Peer-to-Peer-Medienstreaming auf Microsoft Edge bereitstellen!

## <a name="see-also"></a>Weitere Informationen

- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)
