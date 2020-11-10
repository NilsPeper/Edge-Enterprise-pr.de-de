---
title: Cookie-Weitergabe von Microsoft Edge an Internet Explorer
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 11/05/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 'Konfigurieren der Cookie-Weitergabe von Microsoft Edge an Internet Explorer '
ms.openlocfilehash: 5740a4ce31a240573b9106e7a20a5c44688aca0a
ms.sourcegitcommit: 2024629929044e2dcf146674058c1d6312c32e9a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2020
ms.locfileid: "11157541"
---
# Cookie-Weitergabe von Microsoft Edge an Internet Explorer

In diesem Artikel wird erläutert, wie Sie die Weitergabe von Sitzungscookies von einem Microsoft Edge-Prozess an einen Internet Explorer-Prozess konfigurieren können, wenn der Internet Explorer-Modus verwendet wird.

> [!NOTE]
> Dieser Artikel bezieht sich auf Microsoft Edge Version 87 oder neuer.

## Voraussetzungen

- Windows-Updates

  - Windows10, Version2004, Windows Server, Version2004– KB4571744 oder höher
  - Windows10, Version1909, Windows Server, Version1909– KB4566116 oder höher
  - Windows10, Version1903, Windows Server, Version1903– KB4566116 oder höher
  - Windows10, Version1809, Windows Server, Version1809, und Windows Server2019– KB4571748 oder höher
  - Windows10, Version1803– KB4577032 oder höher

- Microsoft Edge, Version87 oder höher
- [IE-Modus](https://aka.ms/iemodeonedge)  konfiguriert mit Enterprise Mode Site List

## Übersicht

Eine in großen Unternehmen häufige Konfiguration besteht darin, eine Anwendung, die in einem modernen Browser funktioniert, mit einer anderen Anwendung zu verknüpfen, welche für das Öffnen im Internet Explorer-Modus mit aktiviertem einmaligem Anmelden (SSO) als Teil des Workflows konfiguriert sein könnte.

Die Microsoft Edge- und Internet Explorer-Prozesse verwenden standardmäßig keine gemeinsamen Sitzungscookies, was in manchen Fällen nachteilig sein kann. Ein Benutzer muss sich beispielsweise im Internet Explorer-Modus erneut authentifizieren, und die Abmeldung von einer Microsoft Edge-Sitzung hat nicht automatisch die Abmeldung von der Sitzung im Internet Explorer-Modus zur Folge. Für solche Szenarien können Sie bestimmte, für SSO festgelegte Cookies so konfigurieren, dass sie von Microsoft Edge an den Internet Explorer gesendet werden, um den Authentifizierungsablauf nahtloser zu gestalten, da auf diese Weise die Notwendigkeit einer erneuten Authentifizierung wegfällt.

> [!NOTE]
> Sitzungscookies können nur von Microsoft Edge an Internet Explorer weitergegeben werden. Die Weitergabe von Sitzungscookies von Internet Explorer an Microsoft Edge ist nicht möglich.

## Funktionsweise der Cookie-Weitergabe

Die Enterprise Mode Site List-XML-Datei wurde erweitert, damit zusätzliche Elemente Cookies angeben können, die von einer Microsoft Edge-Sitzung an Internet Explorer weitergegeben werden müssen.  

Wenn während einer Microsoft Edge-Sitzung zum ersten Mal ein Internet Explorer-Modus-Tab erstellt wird, werden alle übereinstimmenden Cookies an die Internet Explorer-Sitzung weitergegeben. Anschließend wird jedes Mal, wenn ein Cookie, das einer Regel entspricht, hinzugefügt, gelöscht oder geändert wird, dieses als Update an die Internet Explorer-Sitzung weitergegeben. Wenn die Websiteliste aktualisiert wird, werden die weitergegebenen Cookies ebenfalls neu ausgewertet.

### Aktualisierte Schemaelemente

In der folgenden Tabelle wird das \<shared-cookie\>-Element beschrieben, das zur Unterstützung der Cookie-Weitergabe hinzugefügt wurde.

| Element| Beschreibung |
|-|-|
| \<shared-cookie **domain**=".contoso.com" **name**="cookie1"\>\</shared-cookie\><br><br>ODER<br><br>\<shared-cookie **host**="subdomain.contoso.com" **name**="cookie2"\>\</shared-cookie\>   |**(Erforderlich)** Ein \<shared-cookie\>-Element erfordert mindestens ein *domain*-Attribut (für Domänen-Cookies) oder ein *host*-Attribut (für Nur-Host-Cookies) sowie ein *name*-Attribut.<br>Diese müssen jeweils exakt mit der Domäne bzw. mit dem Namen des Cookies übereinstimmen. **Beachten Sie**, dass es bei Unterdomänen keine Übereinstimmung gibt.<br><br>Das *domain*-Attribut wird für Domänen-Cookies verwendet (ein vorangestellter Punkt ist dabei zulässig, aber optional).<br>Das *host*-Attribut wird für Nur-Host-Cookies verwendet (ein vorangestellter Punkt ist dabei ein Fehler). Wenn Sie keine oder beide Optionen angeben, hat dies einen Fehler zur Folge.<br>* Bei einem Cookie handelt es sich um ein Domänen-Cookie, wenn in der Cookie-Zeichenfolge eine Domäne angegeben wurde (über den HTTP-Set-Cookie-Antwortheader oder die "document.cokie JS"-API). Ein Domänen-Cookie gilt für die angegebene Domäne und alle Unterdomänen. Wenn in der Cookie-Zeichenfolge keine Domäne angegeben wurde, handelt es sich bei dem Cookie um ein Nur-Host-Cookie, das nur für den Host gilt, für den es festgelegt wurde. Beachten Sie, dass einige Klassen von URLs wie etwa Einzelwort-Hostnamen (z. B. http://intranetsite) und IP-Adressen (z. B. http://10.0.0.1) ausschließlich Nur-Host-Cookies festlegen können.    |
| \<shared-cookie **host**="subdomain.contoso.com" **name**="cookie2" **path**="/a/b/c"\>\</shared-cookie\>  | **(Optional)** Es kann ein *path*-Attribut angegeben werden. Wenn kein path-Attribut angegeben wird (oder es leer ist), entsprechen alle Cookies, die mit Domain/Host und Name übereinstimmen, der Richtlinie, und das unabhängig vom Pfad (Platzhalterregel).<br><br>Bei Angabe eines Pfads muss es sich um eine exakte Übereinstimmung handeln.<br>Wenn ein Cookie einer Regel mit einem Pfad entspricht, hat dies Vorrang vor einer Regel ohne Pfad. |

#### Weitergabe-Beispiel

```xml
<site-list version="1">
<shared-cookie domain=".contoso.com" name="cookie1"></shared-cookie> 
<shared-cookie host="subdomain.contoso.com" name="cookie2" path="/a/b/c">
</shared-cookie>
</site-list>
```

## Weitere Informationen

- [Informationen zum IE-Modus](https://docs.microsoft.com/deployedge/edge-ie-mode)
- [Informationen zu konfigurierbaren Websites](https://docs.microsoft.com/deployedge/edge-learnmore-configurable-sites-ie-mode)
- [Weitere Informationen zum Unternehmensmodus](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [Angebotsseite für Microsoft Edge für Unternehmen](https://aka.ms/EdgeEnterprise)
