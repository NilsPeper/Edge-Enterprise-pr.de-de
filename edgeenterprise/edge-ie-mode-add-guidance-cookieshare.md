---
title: Cookie-Austausch zwischen Microsoft Edge und Internet Explorer
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 03/08/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Informationen zum Freigeben von Cookies zwischen Microsoft Edge und Internet Explorer
ms.openlocfilehash: 403404c96b91cde62e714324864b87ff2e57f8db
ms.sourcegitcommit: dd8cdbd35726c795ddce917e549ddf17ee7f5290
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/11/2022
ms.locfileid: "12473417"
---
# <a name="cookie-sharing-between-microsoft-edge-and-internet-explorer"></a>Cookie-Austausch zwischen Microsoft Edge und Internet Explorer

>[!Note]
> Die Internet Explorer (IE) 11-Desktopanwendung wird eingestellt und wird am 15. Juni 2022 nicht mehr unterstützt. Informationen dazu, was sich im Bereich und außerhalb des Gültigkeitsbereichs befindet, wenn IE 11 eingestellt wird, finden Sie in den häufig gestellten [Fragen zur Einstellung von Desktop-Apps in Internet Explorer 11](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549). Die gleichen IE 11-Apps und -Websites, die Sie heute verwenden, können in Microsoft Edge im Internet Explorer-Modus geöffnet werden. Weitere Informationen finden Sie unter [Die Zukunft von Internet Explorer auf Windows 10 befindet sich in Microsoft Edge](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/).

In diesem Artikel wird erläutert, wie Sie die Sitzungscookiefreigabe zwischen einem Microsoft Edge-Prozess und einem Internet Explorer-Prozess konfigurieren, während Sie den Internet Explorer-Modus verwenden.

> [!NOTE]
> Dieser Artikel bezieht sich auf Microsoft Edge Version 87 oder neuer.

## <a name="prerequisites"></a>Voraussetzungen

So geben Sie Sitzungscookies von Microsoft Edge an Internet Explorer frei:

- Windows-Updates

  - Windows 11
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

So geben Sie Sitzungscookies zwischen Microsoft Edge und Internet Explorer frei:

- Windows-Updates
  
  - Windows 11 – KB5010414 oder höher
  - Windows Server 2022 – KB5010421 oder höher
  - Windows 10 Version 20H2 – KB5010415 oder höher
  - Windows 10 Version 21H1 – KB5010415 oder höher
  - Windows 10 Version 21H2- KB5010415 oder höher
- Microsoft Edge Version 99 oder höher
- [IE-Modus](./edge-ie-mode.md)  konfiguriert mit Enterprise Mode Site List

## <a name="overview"></a>Übersicht

Eine in großen Unternehmen häufige Konfiguration besteht darin, eine Anwendung, die in einem modernen Browser funktioniert, mit einer anderen Anwendung zu verknüpfen, welche für das Öffnen im Internet Explorer-Modus mit aktiviertem einmaligem Anmelden (SSO) als Teil des Workflows konfiguriert sein könnte.

Standardmäßig geben die Microsoft Edge- und Internet Explorer-Prozesse keine Sitzungscookies frei, und dieser Mangel an Freigabe kann in einigen Fällen unbequem sein. Wenn ein Benutzer z. B. im Internet Explorer-Modus erneut authentifizieren muss oder sich von einer Microsoft Edge-Sitzung abmeldet, melde er sich nicht von der Sitzung im Internet Explorer-Modus ab. In diesen Szenarien können Sie bestimmte von SSO festgelegte Cookies so konfigurieren, dass sie von Microsoft Edge an Internet Explorer gesendet werden, damit die Authentifizierungserfahrung verbessert wird, indem keine erneute Authentifizierung erforderlich ist.

> [!NOTE]
> Vor Microsoft Edge Version 99 können Sitzungscookies nur von Microsoft Edge an Internet Explorer freigegeben werden. Ab Microsoft Edge Version 99 ist das Freigeben von Sitzungscookies umgekehrt (von Internet Explorer bis Microsoft Edge) möglich.

## <a name="how-cookie-sharing-works"></a>Funktionsweise der Cookie-Weitergabe

Die Websitelisten-XML für den Unternehmensmodus wird erweitert, damit mehr Elemente Sitzungscookies angeben können, die zwischen Microsoft Edge und Internet Explorer freigegeben werden müssen.

Wenn während einer Microsoft Edge-Sitzung zum ersten Mal ein Internet Explorer-Modus-Tab erstellt wird, werden alle übereinstimmenden Cookies an die Internet Explorer-Sitzung weitergegeben. Danach wird jedes Mal, wenn ein Cookie, das einer Regel entspricht, hinzugefügt, gelöscht oder geändert, als Update an die Internet Explorer-Sitzung gesendet. Die Gruppe der freigegebenen Cookies wird auch erneut ausgewertet, wenn die Websiteliste aktualisiert wird.

### <a name="updated-schema-elements"></a>Aktualisierte Schemaelemente

In der folgenden Tabelle wird das \<shared-cookie\>-Element beschrieben, das zur Unterstützung der Cookie-Weitergabe hinzugefügt wurde.

| Element| Beschreibung |
|-|-|
| \<shared-cookie **domain**=".contoso.com" **name**="cookie1"\>\</shared-cookie\><br><br>ODER<br><br>\<shared-cookie **host**="subdomain.contoso.com" **name**="cookie2"\>\</shared-cookie\>   |**(Erforderlich)** Ein \<shared-cookie\>-Element erfordert mindestens ein *domain*-Attribut (für Domänen-Cookies) oder ein *host*-Attribut (für Nur-Host-Cookies) sowie ein *name*-Attribut.<br>Diese Attribute müssen exakt mit der Domäne bzw. dem Namen des Cookies übereinstimmen. **Beachten Sie**, dass es bei Unterdomänen keine Übereinstimmung gibt.<br><br>Das *domain*-Attribut wird für Domänen-Cookies verwendet (ein vorangestellter Punkt ist dabei zulässig, aber optional).<br>Das *host*-Attribut wird für Nur-Host-Cookies verwendet (ein vorangestellter Punkt ist dabei ein Fehler). Wenn Sie keine oder beide Optionen angeben, hat dies einen Fehler zur Folge.<br>* Bei einem Cookie handelt es sich um ein Domänen-Cookie, wenn in der Cookie-Zeichenfolge eine Domäne angegeben wurde (über den HTTP-Set-Cookie-Antwortheader oder die "document.cokie JS"-API). Ein Domänen-Cookie gilt für die angegebene Domäne und alle Unterdomänen. Wenn eine Domäne in der Cookiezeichenfolge nicht angegeben wurde, ist das Cookie nur ein Hostcookie und gilt nur für den bestimmten Host, für den es festgelegt wurde. Einige Klassen von URLs, z. B. Hostnamen mit einem Wort (z. B http://intranetsite) . und IP-Adressen) (z http://10.0.0.1) . B. können nur Hostcookies festgelegt werden.    |
| \<shared-cookie **host**="subdomain.contoso.com" **name**="cookie2" **path**="/a/b/c"\>\</shared-cookie\>  | **(Optional)** Es kann ein *path*-Attribut angegeben werden. Wenn kein path-Attribut angegeben wird (oder es leer ist), entsprechen alle Cookies, die mit Domain/Host und Name übereinstimmen, der Richtlinie, und das unabhängig vom Pfad (Platzhalterregel).<br><br>Bei Angabe eines Pfads muss es sich um eine exakte Übereinstimmung handeln.<br>Wenn ein Cookie einer Regel mit einem Pfad entspricht, hat dies Vorrang vor einer Regel ohne Pfad. |
| \<shared-cookie **domain**=".contoso.com" **name**="cookie1" **source-engine**="MSEdge"\>\</shared-cookie\><br><br>ODER<br><br>\<shared-cookie **domain**=".contoso.com" **name**="cookie1" **source-engine**="IE11"\>\</shared-cookie\><br><br>ODER<br><br>\<shared-cookie **domain**=".contoso.com" **name**="cookie1" **source-engine**="Both"\>\</shared-cookie\> | **(Optional)** Das Quellmodulattribut gibt an, wie die Sitzungscookies zwischen Microsoft Edge und Internet Explorer freigegeben werden. Es gilt Folgendes:<br><br>- **MSEdge**. Freigeben von Sitzungscookies von Microsoft Edge an Internet Explorer.<br>- **IE11**.  Freigeben von Sitzungscookies aus Internet Explorer an Microsoft Edge.<br>- **Beides**. Geben Sie Sitzungscookies für Microsoft Edge und Internet Explorer frei.<br>- **Standard oder nicht angegeben**. Sitzungscookies werden von Microsoft Edge an Internet Explorer weitergegeben. |

#### <a name="sharing-example"></a>Weitergabe-Beispiel

```xml
<site-list version="1"> 
<shared-cookie domain=".contoso.com" name="cookie1"></shared-cookie>  
<shared-cookie host="subdomain.contoso.com" name="cookie2" path="/a/b/c"> 
</shared-cookie> 
<shared-cookie host="subdomain.contoso.com" name="cookie3" source-engine="MSEdge"></shared-cookie> 
</site-list> 
```

## <a name="see-also"></a>Weitere Informationen

- [Informationen zum IE-Modus](./edge-ie-mode.md)
- [Informationen zu konfigurierbaren Websites](./edge-learnmore-configurable-sites-ie-mode.md)
- [Weitere Informationen zum Unternehmensmodus](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [Angebotsseite für Microsoft Edge für Unternehmen](https://aka.ms/EdgeEnterprise)
