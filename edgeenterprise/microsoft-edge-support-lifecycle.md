---
title: Microsoft Edge-Lebenszyklus
ms.author: srugh
author: dan-wesley
manager: seanlynd
ms.date: 02/02/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Microsoft Edge-Lebenszyklus
ms.openlocfilehash: aced6353ef5b110f27751585ecb202c4825b075d
ms.sourcegitcommit: 556aca8dde42dd66364427f095e8e473b86651a0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2022
ms.locfileid: "12445459"
---
# <a name="microsoft-edge-lifecycle-policy"></a>Microsoft Edge-Lebenszyklusrichtlinie

In diesem Artikel wird die Lebenszyklusrichtlinie beschrieben, die für Microsoft Edge gilt.

> [!NOTE]
> Dieser Artikel bezieht sich auf Microsoft Edge Versionen 77 und höher.

> [!NOTE]
> Ab Stable Channel Version 94 Microsoft Edge in einen 4-wöchigen Hauptversionszyklus verschoben. Wir wissen jedoch, dass Unternehmenskunden, die komplexe Umgebungen verwalten, mehr Zeit benötigen, um Microsoft Edge-Updates zu planen und zu testen. Um unseren Unternehmenskunden zu helfen, die eine erweiterte Zeitachse zum Verwalten von Updates benötigen, bietet Microsoft Edge eine **erweiterte Stable-Option, die auf einen längeren, 8-wöchigen Hauptversionszyklus ausgerichtet ist.** Diese Veröffentlichungsoption ist nur für Kunden mit verwalteten Umgebungen verfügbar. [Weitere Informationen finden Sie in unserem Ankündigungsblogbeitrag](https://blogs.windows.com/msedgedev/2021/07/15/opt-in-extended-stable-release-cycle/)

## <a name="overview-of-the-lifecycle-policy-for-microsoft-edge"></a>Übersicht über die Lifecycle-Richtlinie für Microsoft Edge

Microsoft Edge Features häufigere und flexiblere Aktualisierungsfunktionen. Da Browserversionen nicht an die Windows Hauptversionen gebunden sind, ist es erforderlich, dass die richtlinienbasierte Lifecycle-Richtlinie aktualisiert wird, um diese Entkopplung widerzuspiegeln. In Zukunft folgen Microsoft Edge der [Modern-Lifecycle-Richtlinie](https://support.microsoft.com/help/30881/modern-lifecycle-policy). Sicherheitsupdates und Wartungsupdates sind nur für die neueste Stable-Kanalversion und die neueste Betakanalversion verfügbar. Wenn Sie ältere Versionen von Microsoft Edge verwenden, werden Ihnen wahrscheinlich die neuesten Qualitäts- und Sicherheitsupdates fehlen. Die Verwendung älterer Versionen wird nicht empfohlen. Der unterstützte Support ist wie im folgenden Abschnitt beschrieben verfügbar.

## <a name="service-and-assisted-support-timeline"></a>Zeitachse für Service und unterstützten Support

Ab Stable Channel Version 94 Microsoft Edge in einen 4-wöchigen Hauptversionszyklus verschoben. Wir bieten weiterhin supportunterstützten Support für die neuesten drei Stable-Kanalversionen und die neueste Betakanalversion. Die effektive unterstützte Supportdauer für eine Stable-Kanalversion beträgt ca. 12 Wochen.

Wir sind uns bewusst, dass Unternehmenskunden, die komplexe Umgebungen verwalten, mehr Zeit benötigen, um Microsoft Edge Updates zu planen und zu testen. Um unseren Unternehmenskunden zu helfen, die eine erweiterte Zeitachse zum Verwalten von Updates benötigen, bietet Microsoft Edge eine **erweiterte Stable-Option, die auf einen längeren, 8-wöchigen Hauptversionszyklus ausgerichtet ist**. Der unterstützte Support ist für die letzten beiden Extended Stable-Kanalversionen verfügbar. Die effektive Unterstützte Supportdauer für eine extended Stable-Kanalversion beträgt ca. 16 Wochen. In der folgenden Tabelle sind die Supportoptionen für verschiedene Microsoft Edge Versionen zusammengefasst.

|     Release-Option              |     Hauptversionsversion unterstützt    |     Hauptversionsversion, gewartet    |     Supportabdeckung für alle Versionen    |     Wartungsabdeckung    |
|---------------------------------|----------------------------------------|---------------------------------------|-----------------------------------------|---------------------------|
|     Täglich "Canary"              |     Keiner                               |     Keiner                              |     Keiner                                |     Keiner                  |
|     Wöchentliches "Dev"                |     Keiner                               |     Keiner                              |     Keiner                                |     Keiner                  |
|     `4`-Woche "Beta"               |     Aktuell                            |     Aktuell                           |     `4` Wochen                             |    `4` Wochen               |
|     `4`-Week "Stable"             |     Aktuelle und `2` vorherige             |     Aktuell                           |     `12` Wochen                            |     `4` Wochen               |
|     `8`-Week "Extended Stable"    |     Aktuelle und `1` vorherige             |     Aktuell                           |     `16` Wochen                            |     `8` Wochen               |

## <a name="see-also"></a>Weitere Informationen

- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)
- [Dokumentation für Microsoft Edge](./index.yml)
- [Microsoft Modern Lifecycle-Richtlinie](https://support.microsoft.com/help/30881/modern-lifecycle-policy)
- [Unterstützte Betriebssysteme für Microsoft Edge](./microsoft-edge-supported-operating-systems.md)