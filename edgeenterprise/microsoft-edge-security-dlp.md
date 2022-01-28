---
title: Grundlegendes zur Verhinderung von Datenverlust in Microsoft Edge
ms.author: archandr
author: dan-wesley
manager: seanlynd
ms.date: 11/22/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Grundlegendes zur Verhinderung von Datenverlust (Data Loss Prevention, DLP) in Microsoft Edge
ms.openlocfilehash: b20a9eb965256adcebd47a5eb1805fb4f0a5992b
ms.sourcegitcommit: e7f3098d8b7d91cae20b5778a71a87daababc312
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2022
ms.locfileid: "12297903"
---
# <a name="understand-data-loss-prevention-dlp-in-microsoft-edge"></a>Grundlegendes zur Verhinderung von Datenverlust (Data Loss Prevention, DLP) in Microsoft Edge

In diesem Artikel wird beschrieben, wie Microsoft Edge die Verhinderung von Datenverlust (Data Loss Prevention, DLP) mit Endpunkt-DLP und Windows Information Protection (WIP) unterstützt.

## <a name="dlp-defined"></a>DLP definiert

Die Verhinderung von Datenverlust (Data Loss Prevention, DLP) ist ein System von Technologien, die vertrauliche Unternehmensdaten erkennen und vor unbefugtem Zugriff schützen. Die Unternehmen müssen vertrauliche Informationen schützen und deren nicht autorisierte Offenlegung verhindern, um den Unternehmensstandards und Branchenvorschriften zu entsprechen. Vertrauliche Informationen umfassen Finanzdaten oder persönliche Informationen. Beispiele für persönliche Informationen sind Kreditkartennummern, Sozialversicherungsnummern und Gesundheitsdatensätze.

Die Fernarbeit hat den Schwerpunkt auf die Verwendung von DLP verstärkt. Angesichts der zunehmenden Nutzung von persönlichen und geschäftlichen Aktivitäten auf Geräten sehen Unternehmen ein erhöhtes Risiko einer nicht autorisierten Freigabe von Unternehmensdaten außerhalb des Arbeitsplatzes.

Diese Vermischung von Benutzeraktivitäten hat sich auch auf Geräte ausgebreitet, bei denen Daten zwischen persönlichen und unternehmenseigenen Geräten über verschiedene öffentliche und private Netzwerke verschoben werden. Das Ergebnis ist ein erheblich erhöhtes Risiko, vertrauliche Daten bereitzustellen.

Microsoft Edge unterstützt nativ zwei unterschiedliche DLP-Lösungen, Microsoft Endpoint DLP und Windows Information Protection (WIP).

## <a name="microsoft-endpoint-data-loss-prevention-endpoint-dlp"></a>Microsoft Endpoint-Verhinderung von Datenverlust (Endpunkt-DLP)

Microsoft Endpoint DLP ist die nächste Generation der Verhinderung von Datenverlust unter Verwendung moderner Konzepte wie des datenzentrischen Schutzes. Es ist in Windows 10 und Microsoft Edge integriert, sodass keine weiteren Agents oder Plug-Ins auf dem Gerät benötigt werden.

> [!NOTE]
> Dieser Artikel bezieht sich auf Microsoft Edge Version 85 oder neuer.

Verwenden Sie die folgenden Ressourcen, um mehr über Endpunkt-DLP zu erfahren:

- [Video: Microsoft Edge und Verhinderung von Datenverlust (DLP)](microsoft-edge-video-security-dlp.md)
- [Informationen zur Verhinderung von Microsoft 365-Endpunkt Datenverlust](/microsoft-365/compliance/endpoint-dlp-learn-about?preserve-view=true&view=o365-worldwide)
- [Erste Schritte mit der Verhinderung von Endpunkt Datenverlust](/microsoft-365/compliance/endpoint-dlp-getting-started?preserve-view=true&view=o365-worldwide)

Microsoft Edge erzwingt vom Administrator konfigurierte Richtlinien für vertrauliche Dateien und zeichnet Überwachungsereignisse für nicht konforme Aktivitäten auf.

Einige der Benutzeraktivitäten, die Sie auf Geräten unter Windows 10 überwachen und verwalten können, umfassen die folgenden Aktivitäten:

- Dateiupload: Schützen Sie den vertraulichen Dateiupload vor nicht autorisierten Cloud-Speicherorten. <!-- The next 3 screenshots show a sequence where a user tries to drop a sensitive data file on to their local storage.-->
- Schutz der Zwischenablage: Verhindern, dass vertrauliche Daten aus der Datei kopiert werden.
- Druckschutz: Schützen vertraulicher Dateien, die gedruckt werden sollen.
- Auf USB/ Im Netzwerk speichern: Schützen vertraulicher Dateien vor dem Speichern in einem USB-Speicher oder nicht autorisierten Netzwerkspeicherorten.

Ausführlichere Informationen zu den Benutzeraktivitäten, die Sie überwachen und verwalten können, finden Sie unter [Endpunktaktivitäten, die Sie überwachen und entsprechende Maßnahmen ergreifen können](/microsoft-365/compliance/endpoint-dlp-learn-about?preserve-view=true&view=o365-worldwide#endpoint-activities-you-can-monitor-and-take-action-on).

## <a name="windows-information-protection"></a>Windows Information Protection

Lesen Sie [Support für Windows Information Protection](./microsoft-edge-security-windows-information-protection.md), in dem beschrieben wird, wie Microsoft Edge Windows Information Protection (WIP) unterstützt. In den folgenden Abschnitten finden Sie Informationen zu den Systemanforderungen, den Vorteilen und den unterstützten Funktionen:

- [Systemanforderungen](./microsoft-edge-security-windows-information-protection.md#system-requirements)
- [Vorteile von Windows Information Protection](./microsoft-edge-security-windows-information-protection.md#windows-information-protection-benefits)
- [In Microsoft Edge unterstützte WIP-Features](./microsoft-edge-security-windows-information-protection.md#wip-features-supported-in-microsoft-edge)

## <a name="see-also"></a>Weitere Informationen

- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)
- [Video: Verhinderung von Datenverlust in Microsoft Edge](https://www.youtube.com/watch?v=dLD04U9eTqg)
- [Übersicht über die Verhinderung von Datenverlust](/microsoft-365/compliance/data-loss-prevention-policies?preserve-view=true&view=o365-worldwide)
- [Schützen von Unternehmensdaten mithilfe von Windows Information Protection](/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip)