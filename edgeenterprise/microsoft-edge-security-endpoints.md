---
title: Zulassungsliste für Microsoft Edge-Endpunkte
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 11/02/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Zulassungsliste für Microsoft Edge-Endpunkte
ms.openlocfilehash: 9e6a87290f2f73ba11bc98eecd3aa693c35b5ace
ms.sourcegitcommit: 3e155a4395ae3a2ae478eb4b52c436b1c1f2e5db
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2021
ms.locfileid: "12155210"
---
# <a name="allow-list-for-microsoft-edge-endpoints"></a>Zulassungsliste für Microsoft Edge-Endpunkte

Microsoft Edge erfordert zur Unterstützung der zugehörigen Features eine Internetverbindung. In diesem Artikel werden die Domänen-URLs aufgeführt, die Sie der Zulassungsliste hinzufügen müssen, um die Kommunikation über Firewalls und andere Sicherheitsmechanismen sicherzustellen.

> [!NOTE]
> Dieser Artikel bezieht sich auf Microsoft Edge Version 77 oder neuer.

## <a name="domain-urls-to-allow"></a>Domänen-URLs für Zulassungsliste

Lassen Sie die folgenden Domänen-URLs für Microsoft Edge zu.

### <a name="update-service"></a>Updatedienst

Der Dienst, der Microsoft Edge verwendet, um nach neuen Updates zu suchen.

- `https://msedge.api.cdp.microsoft.com`

### <a name="experimentation-and-configuration-service"></a>Experimentier- und Konfigurationsservice

- `https://config.edge.skype.com`

### <a name="download-locations-for-microsoft-edge"></a>Speicherorte für den Download von Microsoft Edge

Speicherorte, von denen Microsoft Edge während einer Erstinstallation oder bei einem Update heruntergeladen werden kann. Der Downloadort wird vom Update Dienst festgelegt.

#### <a name="http"></a>HTTP

- `http://msedge.f.tlu.dl.delivery.mp.microsoft.com`
- `http://msedge.f.dl.delivery.mp.microsoft.com`
- `http://msedge.b.tlu.dl.delivery.mp.microsoft.com`
- `http://msedge.b.dl.delivery.mp.microsoft.com`

#### <a name="https"></a>HTTPS

- `https://msedge.sf.tlu.dl.delivery.mp.microsoft.com`
- `https://msedge.sf.dl.delivery.mp.microsoft.com`
- `https://msedge.sb.tlu.dl.delivery.mp.microsoft.com`
- `https://msedge.sb.dl.delivery.mp.microsoft.com`

  > [!TIP]
  > Zur Vereinfachung der Zulassungsliste für Downloadorte kann eine Wildcard verwendet werden: `*.dl.delivery.mp.microsoft.com`

### <a name="download-locations-for-microsoft-edge-extensions"></a>Speicherorte für den Download von Erweiterungen für Microsoft Edge

Speicherorte, von denen Microsoft Edge-Erweiterungen während einer Erstinstallation oder bei einem Update heruntergeladen werden können. Der Downloadort wird vom Update Dienst festgelegt.

#### <a name="http"></a>HTTP

- `http://msedgeextensions.f.tlu.dl.delivery.mp.microsoft.com`
- `http://msedgeextensions.f.dl.delivery.mp.microsoft.com`
- `http://msedgeextensions.b.tlu.dl.delivery.mp.microsoft.com`
- `http://msedgeextensions.b.dl.delivery.mp.microsoft.com`

#### <a name="https"></a>HTTPS

- `https://msedgeextensions.sf.tlu.dl.delivery.mp.microsoft.com`
- `https://msedgeextensions.sf.dl.delivery.mp.microsoft.com`
- `https://msedgeextensions.sb.tlu.dl.delivery.mp.microsoft.com`
- `https://msedgeextensions.sb.dl.delivery.mp.microsoft.com`

  > [!TIP]
  > Zur Vereinfachung der Zulassungsliste für Downloadorte kann eine Wildcard verwendet werden: `*.dl.delivery.mp.microsoft.com`

### <a name="optionally-for-download-delivery-optimization"></a>Optional für die Download-Übermittlungsoptimierung

Weitere Informationen zur Übermittlungsoptimierung finden Sie unter [Übermittlungsoptimierung für Windows 10-Updates](/windows/deployment/update/waas-delivery-optimization).

- Kommunikation Client-zu-Dienst: `*.do.dsp.mp.microsoft.com` : (HTTP Port 80, HTTPS Port 443)
- Kommunikation Client-zu-Client: TCP-Port 7680 muss für eingehenden Datenverkehr geöffnet sein

### <a name="sync"></a>Sync

Diese Endpunkte verwalten das Lesen und Schreiben von synchronisierten Daten, die Rechteverwaltung für sichere Daten und die Benachrichtigung des Browsers, wenn neue Synchronisierungsdaten verfügbar sind.

- Endpunkte des Microsoft Edge-Synchronisierungsdiensts:

  - `https://edge-enterprise.activity.windows.com`
  - `https://edge.activity.windows.com`

- Azure Information Protection-Endpunkte:

  - `https://api.aadrm.com` (für die meisten Mandanten)
  - `https://api.aadrm.de` (für Mandanten in Deutschland)
  - `https://api.aadrm.cn` (für Mandanten in China)

- [Windows-Benachrichtigungsdienst-Endpunkte](/windows/uwp/design/shell/tiles-and-notifications/firewall-allowlist-config)

### <a name="cloud-site-list-management"></a>Verwaltung von Cloudwebsitelisten

Der Dienst, der Microsoft Edge zum Herunterladen der in der Cloud gehosteten Websiteliste für den Internet Explorer (IE)-Modus verwendet. Weitere Informationen finden Sie unter [Cloud Site List Management](https://aka.ms/CloudSiteList)

- `https://edge.microsoft.com/`

## <a name="other-browser-support-services"></a>Andere Dienste zur Browserunterstützung

Stellen Sie Metadaten für Browser Features bereit, z. B. Tracking-Schutz, Zertifikatsperrlisten und Updates für Browserkomponenten. Stellen Sie herunterladbare Rechtschreibwörterbücher und Listen zur Blockierung von Werbung bereit. Stellen Sie Dienste bereit, um Browserfeatures wie Sammlungen, AutoFill und Erweiterungsspeicher zu unterstützen.

- `http://edge.microsoft.com/`
- `https://edge.microsoft.com/`

## <a name="see-also"></a>Weitere Informationen

- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)
- [Angebotsseite der Microsoft Edge-Dokumentation](./index.yml)
- [Verwalten von Verbindungsendpunkten für Windows 10 Enterprise, Version 1903](/windows/privacy/manage-windows-1903-endpoints)