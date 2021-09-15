---
title: Konfigurationsstrategie für Unternehmensstandorte
ms.author: shisub
author: shisub
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Eine schrittweise Anleitung zum Konfigurieren der Enterprise Mode Site List für den Internet Explorer-Modus.
ms.openlocfilehash: 72de393a5da0b4b0e2950951ae527f6ef870e110
ms.sourcegitcommit: 8968f3107291935ed9adc84bba348d5f187eadae
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/12/2021
ms.locfileid: "11979225"
---
# <a name="enterprise-site-configuration-strategy"></a>Konfigurationsstrategie für Unternehmensstandorte

>[!Note]
> Die Internet Explorer 11-Desktopanwendung wird eingestellt und wird ab dem 15. Juni 2022 nicht mehr unterstützt (eine Liste der in diesem Bereich enthaltenen Elemente [finden Sie in den FAQ](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549)). Dieselben IE11-Apps und -Websites, die Sie heute verwenden, können in Microsoft Edge im Internet Explorer-Modus geöffnet werden. [Weitere Informationen finden Sie hier](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/).

In diesem Artikel werden Änderungen an der Enterprise Mode Site List beschrieben, um den Internet Explorer-Modus für Microsoft Edge Version 77 und höher zu unterstützen.

Weitere Informationen zum Schema der XML-Datei der Enterprise Mode Site List finden Sie unter [Anleitungen für Enterprise Mode-Schema Version 2](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).

> [!NOTE]
> Dieser Artikel bezieht sich auf Microsoft Edge Version 77 oder höher.
<!--
## Updated schema elements

The following table describes the \<open-in app\> element added to the v.2 of the Enterprise Mode schema:

| **Element** | **Description** |
| --- | --- |
| \<open-in app="**true**"\> | A child element that controls what browser is used for sites. This element is required for sites that need to **open in IE11**.|

**Example:**

``` xml
<site url="contoso.com">

  <open-in app="true">IE11</open-in>

</site>
```

The following table shows the possible values of the \<open-in\> element:

| **Value** | **Description** |
| --- | --- |
| **\<open-in\>IE11\</open-in\>** | Opens the site in IE mode or a full IE11 window. To enable IE mode, see [Configure IE mode policies](./edge-ie-mode-policies.md)|
| **\<open-in app="**true**"\>IE11\</open-in\>** | Opens the site in a full IE11 window |
| **\<open-in\>MSEdge\</open-in\>** | Opens the site in Microsoft Edge |
| **\<open-in\>None or not specified\</open-in\>** | Opens the site in the default browser or in the browser where the user navigated to the site. |
|**\<open-in\>Configurable\</open-in\>** | Allows the site to participate in IE mode engine determination. To learn more, see [Learn about Configurable sites in IE mode](edge-learnmore-configurable-sites-ie-mode.md).  |

>[!NOTE]
> The attribute app=**"true"** is only recognized when associated to _'open-in' IE11_. Adding it to the other 'open-in' elements won't change browser behavior.   -->

## <a name="configuration-strategy"></a>Konfigurationsstrategie

Die folgenden Schritte sind Teil einer Websitekonfigurationsstrategie für den IE-Modus:
1. Vorbereiten der Websiteliste
2. Konfigurieren von neutralen Websites
3. (Optional) Verwenden der Cookiefreigabe bei Bedarf

<!--
Step 1.  – if you don’t have one use Site Discovery Step-by-Step
Step 2 – Neutral sites + sticky mode
        Use more examples and explain sticky mode better
Step 3 – If that doesn’t cover your needs, then use Cookie sharing -->

## <a name="prepare-your-site-list"></a>Vorbereiten der Websiteliste

Wenn Sie bereits über eine Enterprise Mode Site List für IE11 oder die Vorgängerversion von Microsoft Edge verfügen, können Sie sie wiederverwenden, um den IE-Modus zu konfigurieren.

Wenn Sie jedoch keine Websiteliste haben, können Sie das [Enterprise Site Discovery-Tool](/deployedge/edge-ie-mode-site-discovery) verwenden, um Ihre Websiteliste aufzufüllen.

## <a name="configure-neutral-sites"></a>Konfigurieren von neutralen Websites

Damit der IE-Modus ordnungsgemäß funktioniert, müssen Authentifizierungs-/Einmaliges Anmelden (Single Sign-On, SSO)-Server explizit als neutrale Standorte konfiguriert werden. Andernfalls versuchen die Seiten des IE-Modus, zu Microsoft Edge umzuleiten, und die Authentifizierung wird fehlschlagen.

Eine neutrale Website verwendet den Browser, in dem die Navigation begonnen wurde – entweder Microsoft Edge oder IE-Modus. Außerdem wird durch das Konfigurieren neutraler Websites sichergestellt, dass alle Anwendungen, die diese Authentifizierungsserver verwenden – sowohl moderne als auch ältere – weiterhin funktionsfähig sind.

Sie können neutrale Websites konfigurieren, indem Sie im Enterprise Mode Site List Manager-Tool für *Öffnen mit* in der Dropdownliste "Keine" festlegen, oder indem Sie das Websitelisten-XML direkt aktualisieren:

``` xml
<site url="login.contoso.com">
   
    <open-in>None</open-in>

</site>
```

Wenn Sie Authentifizierungsserver identifizieren möchten, überprüfen Sie den Netzwerkdatenverkehr einer Anwendung mithilfe der IE 11-Entwicklungstools. Wenn Sie mehr Zeit benötigen, um Ihre Authentifizierungsserver zu identifizieren, können Sie eine Richtlinie so konfigurieren, dass alle Seitennavigationen im IE-Modus bleiben, damit Ihre Benutzer ihre Workflows ohne Unterbrechungen fortsetzen können. Deaktivieren Sie diese Einstellung, sobald Sie ihre Authentifizierungsserver identifiziert und der Websiteliste hinzugefügt haben, um die Verwendung des IE-Modus zu minimieren. Weitere Informationen finden Sie unter [Keep in-page navigation in IE mode](/deployedge/edge-learnmore-inpage-nav).

>[!NOTE]
   >Das Enterprise Mode-Schema Version 1 wird für die Integration des IE-Modus nicht unterstützt. Wenn Sie derzeit Schema V.1 mit Internet Explorer 11 verwenden, müssen Sie ein Upgrade auf Schema V.2 durchführen. Weitere Informationen finden Sie unter [Enterprise Mode-Schema Version 2-Richtlinien](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).

## <a name="optional-use-cookie-sharing-if-necessary"></a>(Optional) Verwenden der Cookiefreigabe bei Bedarf

Standardmäßig teilen die Microsoft Edge- und Internet Explorer-Prozesse keine Sitzungscookies, und diese mangelnde Freigabe kann während des IE-Modus in einigen Fällen unpraktisch sein. Wenn sich ein Benutzer z. B. im IE-Modus erneut authentifizieren muss, wenn er dies gewohnt ist oder wenn er sich von einer Microsoft Edge-Sitzung abmeldet, wird die Internet Explorer-Modussitzung für kritische Transaktionen nicht abgemeldet. In diesen Szenarien können Sie bestimmte von SSO festgelegte Cookies so konfigurieren, dass sie von Microsoft Edge an Internet Explorer gesendet werden, damit die Authentifizierungserfahrung verbessert wird, indem keine erneute Authentifizierung erforderlich ist. Weitere Informationen finden Sie unter [Cookie sharing from Microsoft Edge to Internet Explorer](/deployedge/edge-ie-mode-add-guidance-cookieshare).

## <a name="see-also"></a>Weitere Informationen

- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)
- [Informationen zum IE-Modus](./edge-ie-mode.md)
- [Weitere Informationen zum Unternehmensmodus](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
