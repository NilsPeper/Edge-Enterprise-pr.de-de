---
title: Cookie-Weitergabe von Microsoft Edge an Internet Explorer
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 11/04/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Erfahren Sie, wie Sie Cookies von Microsoft Edge an Internet Explorer freigeben
ms.openlocfilehash: ddd8cb519f2cb22cf238f96d144197a623eb18bc
ms.sourcegitcommit: e7f3098d8b7d91cae20b5778a71a87daababc312
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2022
ms.locfileid: "12298123"
---
# <a name="cookie-sharing-from-microsoft-edge-to-internet-explorer"></a>Cookie-Weitergabe von Microsoft Edge an Internet Explorer

>[!Note]
> Die Internet Explorer (IE) 11-Desktopanwendung wird eingestellt und wird am 15. Juni 2022 nicht mehr unterstützt. Informationen dazu, was beim Zurückziehen von IE 11 im Bereich und außerhalb des Bereichs liegt, finden Sie unter [Internet Explorer 11– Häufig gestellte Fragen](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549)zur Einstellung der Desktop-App. Die gleichen IE 11-Apps und -Websites, die Sie heute verwenden, können im Internet Explorer-Modus in Microsoft Edge geöffnet werden. Weitere Informationen finden Sie unter [Die Zukunft von Internet Explorer auf Windows 10 befindet sich in Microsoft Edge](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/).

In diesem Artikel wird erläutert, wie Sie die Sitzungscookiefreigabe von einem Microsoft Edge-Prozess zu einem Internet Explorer-Prozess konfigurieren, während Sie den Internet Explorer-Modus verwenden.

> [!NOTE]
> Dieser Artikel bezieht sich auf Microsoft Edge Version 87 oder neuer.

## <a name="prerequisites"></a>Voraussetzungen

- Windows-Updates

  - Windows 10, Version 2004, Windows Server, Version 2004 – KB4571744 oder höher
  - Windows 10, Version 1909, Windows Server, Version 1909 – KB4566116 oder höher
  - Windows 10, Version 1903, Windows Server, Version 1903 – KB4566116 oder höher
  - Windows 10, Version 1809, Windows Server, Version 1809, und Windows Server 2019 – KB4571748 oder höher
  - Windows 10, Version 1803 – KB4577032 oder höher
  - Windows 10 Enterprise 2016 LTSC und Windows Server 2016 – KB4580346 oder höher
  - Windows 10 Enterprise 2015 LTSB – KB4580327 oder höher
  - Windows 8.1 und Windows Server 2012 R2 – KB4586768 oder höher
  - Windows 10 Enterprise 2016 LTSC und Windows Server 2016 – KB4580346 oder höher
  - Windows 10 Enterprise 2015 LTSB – KB4580327 oder höher
  - Windows 8.1 und Windows Server 2012 R2 – KB4586768 oder höher

- Microsoft Edge, Version 87 oder höher
- [IE-Modus](./edge-ie-mode.md)  konfiguriert mit Enterprise Mode Site List

## <a name="overview"></a>Übersicht

Eine in großen Unternehmen häufige Konfiguration besteht darin, eine Anwendung, die in einem modernen Browser funktioniert, mit einer anderen Anwendung zu verknüpfen, welche für das Öffnen im Internet Explorer-Modus mit aktiviertem einmaligem Anmelden (SSO) als Teil des Workflows konfiguriert sein könnte.

Standardmäßig geben die Microsoft Edge- und Internet Explorer-Prozesse keine Sitzungscookies frei, und diese fehlende Freigabe kann in einigen Fällen umständlich sein. Wenn sich ein Benutzer beispielsweise im Internet Explorer-Modus erneut authentifizieren muss oder wenn er sich von einer Microsoft Edge Sitzung abmeldet, wird die Internet Explorer-Modussitzung nicht abgemeldet. In diesen Szenarien können Sie bestimmte von SSO festgelegte Cookies so konfigurieren, dass sie von Microsoft Edge an Internet Explorer gesendet werden, damit die Authentifizierungserfahrung verbessert wird, indem keine erneute Authentifizierung erforderlich ist.

> [!NOTE]
> Sitzungscookies können nur von Microsoft Edge an Internet Explorer weitergegeben werden. Die Weitergabe von Sitzungscookies von Internet Explorer an Microsoft Edge ist nicht möglich.

## <a name="how-cookie-sharing-works"></a>Funktionsweise der Cookie-Weitergabe

Der XML-Code Enterprise Mode-Websiteliste wurde erweitert, damit mehr Elemente Cookies angeben können, die aus einer Microsoft Edge Sitzung mit Internet Explorer freigegeben werden müssen.  

Wenn während einer Microsoft Edge-Sitzung zum ersten Mal ein Internet Explorer-Modus-Tab erstellt wird, werden alle übereinstimmenden Cookies an die Internet Explorer-Sitzung weitergegeben. Danach wird jedes Mal, wenn ein Cookie hinzugefügt, gelöscht oder geändert wird, das einer Regel entspricht, als Update an die Internet Explorer-Sitzung gesendet. Die Gruppe der freigegebenen Cookies wird auch erneut ausgewertet, wenn die Websiteliste aktualisiert wird.

### <a name="updated-schema-elements"></a>Aktualisierte Schemaelemente

In der folgenden Tabelle wird das \<shared-cookie\>-Element beschrieben, das zur Unterstützung der Cookie-Weitergabe hinzugefügt wurde.

| Element| Beschreibung |
|-|-|
| \<shared-cookie **domain**=".contoso.com" **name**="cookie1"\>\</shared-cookie\><br><br>ODER<br><br>\<shared-cookie **host**="subdomain.contoso.com" **name**="cookie2"\>\</shared-cookie\>   |**(Erforderlich)** Ein \<shared-cookie\>-Element erfordert mindestens ein *domain*-Attribut (für Domänen-Cookies) oder ein *host*-Attribut (für Nur-Host-Cookies) sowie ein *name*-Attribut.<br>Diese Attribute müssen exakt mit der Domäne und dem Namen des Cookies übereinstimmen. **Beachten Sie**, dass es bei Unterdomänen keine Übereinstimmung gibt.<br><br>Das *domain*-Attribut wird für Domänen-Cookies verwendet (ein vorangestellter Punkt ist dabei zulässig, aber optional).<br>Das *host*-Attribut wird für Nur-Host-Cookies verwendet (ein vorangestellter Punkt ist dabei ein Fehler). Wenn Sie keine oder beide Optionen angeben, hat dies einen Fehler zur Folge.<br>* Bei einem Cookie handelt es sich um ein Domänen-Cookie, wenn in der Cookie-Zeichenfolge eine Domäne angegeben wurde (über den HTTP-Set-Cookie-Antwortheader oder die "document.cokie JS"-API). Ein Domänen-Cookie gilt für die angegebene Domäne und alle Unterdomänen. Wenn eine Domäne nicht in der Cookiezeichenfolge angegeben wurde, ist das Cookie ein Nur-Host-Cookie und gilt nur für den bestimmten Host, für den es festgelegt wurde. Einige Klassen von URLs, z. B. Single-Word-Hostnamen (z. B. http://intranetsite) und IP-Adressen), http://10.0.0.1) können nur Nur-Host-Cookies festlegen.    |
| \<shared-cookie **host**="subdomain.contoso.com" **name**="cookie2" **path**="/a/b/c"\>\</shared-cookie\>  | **(Optional)** Es kann ein *path*-Attribut angegeben werden. Wenn kein path-Attribut angegeben wird (oder es leer ist), entsprechen alle Cookies, die mit Domain/Host und Name übereinstimmen, der Richtlinie, und das unabhängig vom Pfad (Platzhalterregel).<br><br>Bei Angabe eines Pfads muss es sich um eine exakte Übereinstimmung handeln.<br>Wenn ein Cookie einer Regel mit einem Pfad entspricht, hat dies Vorrang vor einer Regel ohne Pfad. |

#### <a name="sharing-example"></a>Weitergabe-Beispiel

```xml
<site-list version="1">
<shared-cookie domain=".contoso.com" name="cookie1"></shared-cookie> 
<shared-cookie host="subdomain.contoso.com" name="cookie2" path="/a/b/c">
</shared-cookie>
</site-list>
```

## <a name="see-also"></a>Weitere Informationen

- [Informationen zum IE-Modus](./edge-ie-mode.md)
- [Informationen zu konfigurierbaren Websites](./edge-learnmore-configurable-sites-ie-mode.md)
- [Weitere Informationen zum Unternehmensmodus](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [Angebotsseite für Microsoft Edge für Unternehmen](https://aka.ms/EdgeEnterprise)
