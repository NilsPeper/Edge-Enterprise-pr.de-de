---
title: Microsoft Edge-Lebenszyklus
ms.author: srugh
author: AndreaLBarr
manager: seanlynd
ms.date: 11/26/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Microsoft Edge-Lebenszyklus
ms.openlocfilehash: fd94e92e299ebcb842e6f0a5e65cd5f6c7cd0ca4
ms.sourcegitcommit: e7f3098d8b7d91cae20b5778a71a87daababc312
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2022
ms.locfileid: "12297883"
---
# <a name="microsoft-edge-lifecycle-policy"></a>Microsoft Edge-Lebenszyklusrichtlinie

In diesem Artikel wird die Lebenszyklusrichtlinie beschrieben, die für Microsoft Edge gilt.

> [!NOTE]
> Dieser Artikel bezieht sich auf Microsoft Edge Versionen 77 und höher.

> [!NOTE]
> Beginnend mit der Stable-Channel-Version 94 geht Microsoft Edge zu einem 4-wöchigen Hauptversionszyklus über. Wir wissen jedoch, dass Unternehmenskunden, die komplexe Umgebungen verwalten, mehr Zeit benötigen, um Microsoft Edge-Updates zu planen und zu testen. Um unseren Unternehmenskunden zu helfen, die eine erweiterte Zeitachse zum Verwalten von Updates benötigen, bietet Microsoft Edge eine **erweiterte Stable-Option an, die auf einen längeren, 8-wöchigen Hauptversionszyklus ausgerichtet ist.** Diese Option ist nur für Kunden mit verwalteten Umgebungen verfügbar. [Weitere Informationen finden Sie in unserem Ankündigungsblogbeitrag](https://blogs.windows.com/msedgedev/2021/07/15/opt-in-extended-stable-release-cycle/)

## <a name="overview-of-the-lifecycle-policy-for-microsoft-edge"></a>Übersicht über die Lifecycle-Richtlinie für Microsoft Edge

Microsoft Edge Features häufigere und flexiblere Aktualisierungsfunktionen. Da Browserversionen nicht an die Windows Hauptversionen gebunden sind, ist es erforderlich, dass die richtlinienbasierte Lifecycle-Richtlinie aktualisiert wird, um diese Entkopplung widerzuspiegeln. In Zukunft folgen Microsoft Edge der [Modern-Lifecycle-Richtlinie.](https://support.microsoft.com/help/30881/modern-lifecycle-policy) Sicherheitsupdates und Wartungsupdates sind nur für die neueste Stable-Kanalversion und die neueste Betakanalversion verfügbar. Wenn Sie ältere Versionen von Microsoft Edge verwenden, werden Ihnen wahrscheinlich die neuesten Qualitäts- und Sicherheitsupdates fehlen. Die Verwendung älterer Versionen wird nicht empfohlen. Der unterstützte Support ist wie in den folgenden Abschnitten beschrieben verfügbar.

## <a name="service-and-assisted-support-timeline-for-microsoft-edge-versions-77-93"></a>Zeitachse für Service und unterstützten Support für Microsoft Edge Versionen 77-93

Microsoft Edge verfügt über einen 6-wöchigen Hauptversionszyklus für Stable Channel Version 77 und wird bis Version 93 fortgesetzt.  Wir bieten unterstützungsunterstützten Support für die neuesten drei Stable-Kanalversionen und die neueste Betakanalversion. Die effektive Dauer des persönlichen Supports für eine Stable-Kanalversion beträgt ca. 18 Wochen. Die effektive Supportdauer für eine Betakanalversion beträgt ca. 6 Wochen; Frühere Betakanalversionen werden nicht unterstützt.  In der folgenden Tabelle ist die Dienst- und Supportzeitachse zusammengefasst.

|     Release-Option              |     Hauptversionsversion unterstützt    |     Hauptversionsversion, gewartet    |     Supportabdeckung für alle Versionen    |     Wartungsabdeckung    |
|---------------------------------|----------------------------------------|---------------------------------------|-----------------------------------------|---------------------------|
|     Täglich "Canary"              |     Keiner                               |     Keiner                              |     Keiner                                |     Keiner                  |
|     Wöchentliches "Dev"                |     Keiner                               |     Keiner                              |     Keiner                                |     Keiner                  |
|     `6`-Woche "Beta"               |     Aktuell                            |     Aktuell                           |     `6` Wochen                             |     `6` Wochen               |
|     `6`-Week "Stable"             |     Aktuelle und `2` vorherige             |     Aktuell                           |     `18` Wochen                            |     `6` Wochen               |

## <a name="service-and-assisted-support-timeline-changes-for-microsoft-edge-version-94"></a>Änderungen an der Zeitachse des Diensts und des unterstützten Supports für Microsoft Edge Version 94

Beginnend mit der Stable-Channel-Version 94 geht Microsoft Edge zu einem 4-wöchigen Hauptversionszyklus über. Wir bieten weiterhin supportunterstützten Support für die neuesten drei Stable Channel-Versionen und die neueste Betakanalversion. Die effektive unterstützte Supportdauer für eine Stable-Kanalversion beträgt ca. 12 Wochen.

Wir sind uns bewusst, dass Unternehmenskunden, die komplexe Umgebungen verwalten, mehr Zeit benötigen, um Microsoft Edge Updates zu planen und zu testen. Um unseren Unternehmenskunden zu helfen, die einen erweiterten Zeitplan zum Verwalten von Updates benötigen, bietet Microsoft Edge eine **erweiterte Stable-Option an, die auf einen längeren, 8-wöchigen Hauptversionszyklus ausgerichtet**ist. Der unterstützte Support steht für die letzten beiden Extended Stable-Kanalversionen zur Verfügung. Die effektive unterstützte Supportdauer für eine erweiterte Stable-Kanalversion beträgt ca. 16 Wochen. Weitere Informationen finden Sie in der folgenden Tabelle.

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