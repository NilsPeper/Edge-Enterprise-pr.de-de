---
title: Plattformunterstützung für Microsoft Edge-Features
ms.author: collw
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Zusammenfassung der Plattformunterstützung für Microsoft Edge-Features
ms.openlocfilehash: c34249e126a1fb27c84a2f025c826654bb9df358
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "11643121"
---
# <a name="platform-support-for-microsoft-edge-features"></a>Plattformunterstützung für Microsoft Edge-Features

In diesem Artikel wird die Plattformunterstützung für Microsoft Edge-Features zusammengefasst.

> [!NOTE]
> Dieser Artikel bezieht sich auf Microsoft Edge Version 77 oder höher.

## <a name="feature-matrix-for-platforms"></a>Featurematrix für Plattformen

In den folgenden Tabellen wird die Featureunterstützung für die Windows- und macOS-Plattformen zusammengefasst.

> [!NOTE]
> Android und iOS sind in den Supporttabellen derzeit nicht dargestellt. Wir arbeiten jedoch weiterhin an diesen Informationen und werden sie entsprechend aktualisieren.

| Sicherheitsfeatures |Win 10|Win 8.1|Win 7|macOS|URL|
|--------|-------|--------|-----|-------|---|
|Bedingter Azure Active Directory-Zugriff (Azure AD)|Ja|Ja|Ja|Ja|[Bedingter Azure AD-Zugriff](/deployedge/ms-edge-security-conditional-access#accessing-conditional-access-protected-resources-in-microsoft-edge)|
|Microsoft Defender Application Guard|Ja (1890+)|Nein|Nein|Nein|[Microsoft Defender Application Guard](/deployedge/microsoft-edge-security-windows-defender-application-guard) |
|Microsoft Defender SmartScreen|Ja|Ja|Ja|Ja|[Microsoft Defender SmartScreen](/deployedge/microsoft-edge-security-smartscreen) |
|Microsoft Endpoint DLP|Ja|Nein|Nein|Nein|[Microsoft Endpoint DLP](/deployedge/microsoft-edge-security-dlp#microsoft-endpoint-data-loss-prevention-endpoint-dlp)|
|Kennwortmonitor|Ja|Ja|Ja|Ja|[Kennwortmonitor](https://blogs.windows.com/msedgedev/2021/01/21/edge-88-privacy/)|
|Kennwortgenerator|Ja|Ja|Ja|Ja|[Kennwortgenerator](https://blogs.windows.com/msedgedev/2021/01/21/edge-88-privacy/)|
|Windows Information Protection (WIP)|Ja (1607+)|Nein|Nein|Nein|[WIP](/deployedge/microsoft-edge-security-windows-information-protection#system-requirements)|

|Identitätsfeatures| Win 10 | Win 8.1 | Win 7 | macOS | URL |
|--|--|--|--|--|--|
|Automatische Anmeldung (Hybrid/AAD-J)|Ja|Ja|Ja|Nein|[Hybrid/AAD-J](/deployedge/microsoft-edge-security-identity#automatic-sign-in)|
|Automatische Anmeldung (Domäne beigetreten)|Ja|Ja|Ja|Nein|[Domäne beigetreten](/deployedge/microsoft-edge-security-identity#automatic-sign-in)|
|Automatische Anmeldung (Standardkonto des Betriebssystems ist MSA)|Ja (1709+)|Nein|Nein|Nein|[MSA](/deployedge/microsoft-edge-security-identity#automatic-sign-in)|
|Browser für einmaliges Anmelden (SSO) im Web|Ja|Ja|Ja|Ja|[Browser-Web SSO](https://www.microsoft.com/microsoft-365/roadmap?featureid=66332)|
|Geführter Wechsel/"Automatischer Profilwechsel"|Ja|Ja|Ja|Ja|[Verwenden mehrerer Profile im Unternehmen und Zuhause](https://blogs.windows.com/msedgedev/2020/04/30/automatic-profile-switching/) |
|Mehrere Profile|Ja|Ja|Ja|Ja|[Verwenden mehrerer Profile im Unternehmen und Zuhause](https://blogs.windows.com/msedgedev/2020/04/30/automatic-profile-switching/) |
|Lokale Synchronisierung für Active Directory (AD)|Ja|Ja|Ja|Nein|[Lokale Synchronisierung für Active Directory (AD)-Benutzer](/deployedge/microsoft-edge-on-premises-sync) |
|Nahtlose SSO|Ja (1709+)|Ja|Ja|Ja|[Nahtlose SSO](/deployedge/microsoft-edge-security-identity#seamless-sso)|
|SSO mit Primärem Aktualisierungstoken (PRT)|Ja (1709+)|Ja|Ja|Nein|[SSO mit PRT](/deployedge/microsoft-edge-security-identity#sso-with-primary-refresh-token-prt)|
|Integrierte Windows-Authentifizierung (WIA)|Ja|Ja|Ja|Ja* (Richtlinie erforderlich)|[WIA](/deployedge/microsoft-edge-security-identity#windows-integrated-authentication-wia)|

|Weitere Features|Win 10|Win 8.1|Win 7|macOS|URL|
|--------|-------|--------|-----|-------|---|
|Sammlungen|Ja|Ja|Ja|Ja|[Sammlungen](https://blogs.windows.com/msedgedev/2019/12/09/improvements-collections-sync-microsoft-edge/) |
|Neue Registerkartenseite "Unternehmen"|Ja|Ja|Ja|Ja|[Neue Registerkartenseite](https://blogs.windows.com/msedgedev/2020/10/29/enterprise-new-tab-page-my-feed/) |
|IE-Modus|Ja|Ja|Ja|Nein|[IE-Modus](/deployedge/edge-ie-mode#prerequisites)|
|Kioskmodus|Ja|Nein|Nein|Nein|[Kioskmodus](/deployedge/microsoft-edge-configure-kiosk-mode)|
|Microsoft Search in Bing|Ja|Ja|Ja|Ja|[Intelligente Suche in Bing](https://www.microsoft.com/edge/business/intelligent-search-with-bing) |
|PDF Reader|Ja|Ja|Ja|Ja|[PDF Reader](/deployedge/microsoft-edge-pdf) |
|Shopping|Ja|Ja|Ja|Ja|[Shopping](https://techcommunity.microsoft.com/t5/articles/introducing-shopping-with-microsoft-edge/m-p/1870080) |
|Schlummernde Registerkarten|Ja|Ja|Ja|Ja|[Featureübersicht](/deployedge/microsoft-edge-relnote-stable-channel)<br>[Neuester Blogbeitrag](https://blogs.windows.com/msedgedev/2021/03/04/edge-89-performance/)<br>[Gruppenrichtlinien](/deployedge/microsoft-edge-policies#sleeping-tabs-settings)|
|Synchronisierung|Ja|Ja|Ja|Ja| [Unternehmenssynchronisierung](/deployedge/microsoft-edge-enterprise-sync) |
|Versionsrollback|Ja|Ja|Ja|Nein|[Versionsrollback](/deployedge/edge-learnmore-rollback) |
|Vertikale Registerkarten|Ja|Ja|Ja|Ja| |

## <a name="see-also"></a>Siehe auch

- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)