---
title: Zulassungsliste für Microsoft Edge-Endpunkte
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 06/09/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Zulassungsliste für Microsoft Edge-Endpunkte
ms.openlocfilehash: 76186524a708861432199d5da7eec7573ebecb96
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/31/2020
ms.locfileid: "10980083"
---
# Zulassungsliste für Microsoft Edge-Endpunkte

Microsoft Edge erfordert zur Unterstützung der zugehörigen Features eine Internetverbindung. In diesem Artikel werden die Domänen-URLs aufgeführt, die Sie der Zulassungsliste hinzufügen müssen, um die Kommunikation über Firewalls und andere Sicherheitsmechanismen sicherzustellen.

> [!NOTE]
> Dieser Artikel bezieht sich auf Microsoft Edge Version 77 oder neuer.

## Domänen-URLs für Zulassungsliste

Lassen Sie die folgenden Domänen-URLs für Microsoft Edge zu.

### Updatedienst

Der Dienst, der Microsoft Edge verwendet, um nach neuen Updates zu suchen.

- `https://msedge.api.cdp.microsoft.com`

### Experimentier- und Konfigurationsservice

- `https://config.ecs.skype.com`

### Speicherorte für den Download von Microsoft Edge

Speicherorte, von denen Microsoft Edge während einer Erstinstallation oder bei einem Update heruntergeladen werden kann. Der Downloadort wird vom Update Dienst festgelegt.

#### HTTP

- `http://msedge.f.tlu.dl.delivery.mp.microsoft.com`
- `http://msedge.f.dl.delivery.mp.microsoft.com`
- `http://msedge.b.tlu.dl.delivery.mp.microsoft.com`
- `http://msedge.b.dl.delivery.mp.microsoft.com`

#### HTTPS

- `https://msedge.sf.tlu.dl.delivery.mp.microsoft.com`
- `https://msedge.sf.dl.delivery.mp.microsoft.com`
- `https://msedge.sb.tlu.dl.delivery.mp.microsoft.com`
- `https://msedge.sb.dl.delivery.mp.microsoft.com`

  > [!TIP]
  > Zur Vereinfachung der Zulassungsliste für Downloadorte kann eine Wildcard verwendet werden: `*.dl.delivery.mp.microsoft.com`

### Speicherorte für den Download von Erweiterungen für Microsoft Edge

Speicherorte, von denen Microsoft Edge-Erweiterungen während einer Erstinstallation oder bei einem Update heruntergeladen werden können. Der Downloadort wird vom Update Dienst festgelegt.

#### HTTP

- `http://msedgeextensions.f.tlu.dl.delivery.mp.microsoft.com`
- `http://msedgeextensions.f.dl.delivery.mp.microsoft.com`
- `http://msedgeextensions.b.tlu.dl.delivery.mp.microsoft.com`
- `http://msedgeextensions.b.dl.delivery.mp.microsoft.com`

#### HTTPS

- `https://msedgeextensions.sf.tlu.dl.delivery.mp.microsoft.com`
- `https://msedgeextensions.sf.dl.delivery.mp.microsoft.com`
- `https://msedgeextensions.sb.tlu.dl.delivery.mp.microsoft.com`
- `https://msedgeextensions.sb.dl.delivery.mp.microsoft.com`

  > [!TIP]
  > Zur Vereinfachung der Zulassungsliste für Downloadorte kann eine Wildcard verwendet werden: `*.dl.delivery.mp.microsoft.com`

### Optional für die Download-Übermittlungsoptimierung

Weitere Informationen zur Übermittlungsoptimierung finden Sie unter [Übermittlungsoptimierung für Windows 10-Updates](https://aka.ms/waas-do).

- Kommunikation Client-zu-Dienst: `*.do.dsp.mp.microsoft.com` : (HTTP Port 80, HTTPS Port 443)
- Kommunikation Client-zu-Client: TCP-Port 7680 muss für eingehenden Datenverkehr geöffnet sein

### Sync

Diese Endpunkte verwalten das Lesen und Schreiben von synchronisierten Daten, die Rechteverwaltung für sichere Daten und die Benachrichtigung des Browsers, wenn neue Synchronisierungsdaten verfügbar sind.

- Edge-Synchronisierungsdienst-Endpunkte:

  - `https://enterprise.edge.activity.windows.com`
  - `https://edge.activity.windows.com`

- Azure Information Protection-Endpunkte:

  - `https://api.aadrm.com` (für die meisten Mandanten)
  - `https://api.aadrm.de` (für Mandanten in Deutschland)
  - `https://api.aadrm.cn` (für Mandanten in China)

- [Windows-Benachrichtigungsdienst-Endpunkte](https://docs.microsoft.com/windows/uwp/design/shell/tiles-and-notifications/firewall-allowlist-config)

## Andere Dienste zur Browserunterstützung

Stellen Sie Metadaten für Browser Features bereit, z.B. Tracking-Schutz, Zertifikatsperrlisten und Updates für Browserkomponenten. Stellen Sie herunterladbare Rechtschreibwörterbücher und Listen zur Blockierung von Werbung bereit. Stellen Sie Dienste bereit, um Browserfeatures wie Sammlungen, AutoFill und Erweiterungsspeicher zu unterstützen.

- `http://edge.microsoft.com/`
- `https://edge.microsoft.com/`

## Weitere Informationen

- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)
- [Angebotsseite der Microsoft Edge-Dokumentation](https://docs.microsoft.com/DeployEdge/)
- [Verwalten von Verbindungsendpunkten für Windows 10 Enterprise, Version 1903](https://docs.microsoft.com/windows/privacy/manage-windows-1903-endpoints)
