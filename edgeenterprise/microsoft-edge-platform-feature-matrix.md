---
title: Plattformunterstützung für Microsoft Edge-Features
ms.author: collw
author: dan-wesley
manager: srugh
ms.date: 03/25/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Zusammenfassung der Plattformunterstützung für Microsoft Edge-Features
ms.openlocfilehash: 3ff99e21642aaf1ffe562354ad843f8d56c45726
ms.sourcegitcommit: 93851b83dc11422924646a04a9e0f60ff2554af7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "11470287"
---
# <a name="platform-support-for-microsoft-edge-features"></a>Plattformunterstützung für Microsoft Edge-Features

In diesem Artikel wird die Plattformunterstützung für Microsoft Edge-Features zusammengefasst.

> [!NOTE]
> Dieser Artikel bezieht sich auf Microsoft Edge Version77 oder höher.

## <a name="feature-matrix-for-platforms"></a>Featurematrix für Plattformen

In den folgenden Tabellen wird die Featureunterstützung für die Windows- und macOS-Plattformen zusammengefasst.

> [!NOTE]
> Android und iOS sind in den Supporttabellen derzeit nicht dargestellt. Wir arbeiten jedoch weiterhin an diesen Informationen und werden sie entsprechend aktualisieren.

| Sicherheitsfeatures |Win 10|Win 8.1|Win 7|macOS|URL|
|--------|-------|--------|-----|-------|---|
|Bedingter Azure Active Directory-Zugriff (Azure AD)|Ja|Ja|Ja|Ja|[Bedingter Azure AD-Zugriff](https://docs.microsoft.com/deployedge/ms-edge-security-conditional-access#accessing-conditional-access-protected-resources-in-microsoft-edge)|
|Microsoft Defender Application Guard|Ja (1890+)|Nein|Nein|Nein|[Microsoft Defender Application Guard](https://docs.microsoft.com/deployedge/microsoft-edge-security-windows-defender-application-guard) |
|Microsoft Defender SmartScreen|Ja|Ja|Ja|Ja|[Microsoft Defender SmartScreen](https://docs.microsoft.com/deployedge/microsoft-edge-security-smartscreen) |
|Microsoft Endpoint DLP|Ja|Nein|Nein|Nein|[Microsoft Endpoint DLP](https://docs.microsoft.com/deployedge/microsoft-edge-security-dlp#microsoft-endpoint-data-loss-prevention-endpoint-dlp)|
|Kennwortmonitor|Ja|Ja|Ja|Ja|[Kennwortmonitor](https://blogs.windows.com/msedgedev/2021/01/21/edge-88-privacy/)|
|Kennwortgenerator|Ja|Ja|Ja|Ja |[Kennwortgenerator](https://blogs.windows.com/msedgedev/2021/01/21/edge-88-privacy/)|
|Windows Information Protection (WIP)|Ja (1607+)|Nein|Nein|Nein|[WIP](https://docs.microsoft.com/deployedge/microsoft-edge-security-windows-information-protection#system-requirements)|


|Identitätsfeatures| Win 10 | Win 8.1 | Win 7 | macOS | URL |
|--|--|--|--|--|--|
|Automatische Anmeldung (Hybrid/AAD-J)|Ja|Ja|Ja|Nein|[Hybrid/AAD-J](https://docs.microsoft.com/deployedge/microsoft-edge-security-identity#automatic-sign-in)|
|Automatische Anmeldung (Domäne beigetreten)|Ja|Ja|Ja| Nein|[Domäne beigetreten](https://docs.microsoft.com/deployedge/microsoft-edge-security-identity#automatic-sign-in)|
|Automatische Anmeldung (Standardkonto des Betriebssystems ist MSA)|Ja (1709+)|Nein|Nein|Nein|[MSA](https://docs.microsoft.com/deployedge/microsoft-edge-security-identity#automatic-sign-in)|
|Browser für einmaliges Anmelden (SSO) im Web|Ja|Ja|Ja|Ja|[Browser-Web SSO](https://www.microsoft.com/microsoft-365/roadmap?featureid=66332)|
|Geführter Wechsel/"Automatischer Profilwechsel"|Ja|Ja|Ja|Ja|[Verwenden mehrerer Profile im Unternehmen und Zuhause](https://blogs.windows.com/msedgedev/2020/04/30/automatic-profile-switching/) |
|Mehrere Profile|Ja|Ja|Ja|Ja|[Verwenden mehrerer Profile im Unternehmen und Zuhause](https://blogs.windows.com/msedgedev/2020/04/30/automatic-profile-switching/) |
|Lokale Synchronisierung für Active Directory (AD)|Ja|Ja|Ja|Nein|[Lokale Synchronisierung für Active Directory (AD)-Benutzer](https://docs.microsoft.com/deployedge/microsoft-edge-on-premises-sync) |
|Nahtlose SSO|Ja (1709+)|Ja|Ja|Ja|[Nahtlose SSO](https://docs.microsoft.com/deployedge/microsoft-edge-security-identity#seamless-sso)|
|SSO mit Primärem Aktualisierungstoken (PRT)|Ja (1709+)|Ja|Ja|Nein|[SSO mit PRT](https://docs.microsoft.com/deployedge/microsoft-edge-security-identity#sso-with-primary-refresh-token-prt)|
|Integrierte Windows-Authentifizierung (WIA)|Ja|Ja|Ja|Ja* (Richtlinie erforderlich)|[WIA](https://docs.microsoft.com/deployedge/microsoft-edge-security-identity#windows-integrated-authentication-wia)|

|Weitere Features|Win 10|Win 8.1|Win 7|macOS|URL|
|--------|-------|--------|-----|-------|---|
|Sammlungen|Ja|Ja|Ja|Ja|[Sammlungen](https://blogs.windows.com/msedgedev/2019/12/09/improvements-collections-sync-microsoft-edge/) |
|Neue Registerkartenseite "Unternehmen"|Ja|Ja|Ja|Ja|[Neue Registerkartenseite](https://blogs.windows.com/msedgedev/2020/10/29/enterprise-new-tab-page-my-feed/) |
|IE-Modus|Ja|Ja|Ja|Nein|[IE-Modus](https://docs.microsoft.com/deployedge/edge-ie-mode#prerequisites)|
|Kioskmodus|Ja|Nein|Nein|Nein|[Kioskmodus](https://docs.microsoft.com/deployedge/microsoft-edge-configure-kiosk-mode)|
|Microsoft Search in Bing|Ja|Ja|Ja|Ja|[Intelligente Suche in Bing](https://www.microsoft.com/edge/business/intelligent-search-with-bing) |
|PDF Reader|Ja|Ja|Ja|Ja|[PDF Reader](https://docs.microsoft.com/deployedge/microsoft-edge-pdf) |
|Shopping|Ja|Ja|Ja|Ja|[Shopping](https://techcommunity.microsoft.com/t5/articles/introducing-shopping-with-microsoft-edge/m-p/1870080) |
|Schlummernde Registerkarten|Ja|Ja|Ja|Ja|[Featureübersicht](https://docs.microsoft.com/deployedge/microsoft-edge-relnote-stable-channel)<br>[Neuester Blogbeitrag](https://blogs.windows.com/msedgedev/2021/03/04/edge-89-performance/)<br>[Gruppenrichtlinien](https://docs.microsoft.com/deployedge/microsoft-edge-policies#sleeping-tabs-settings)|
|Synchronisierung|Ja|Ja|Ja|Ja| [Unternehmenssynchronisierung](https://docs.microsoft.com/deployedge/microsoft-edge-enterprise-sync) |
|Versionsrollback|Ja|Ja|Ja|Nein|[Versionsrollback](https://docs.microsoft.com/deployedge/edge-learnmore-rollback) |
|Vertikale Registerkarten|Ja|Ja|Ja|Ja| |

## <a name="see-also"></a>Siehe auch

- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)