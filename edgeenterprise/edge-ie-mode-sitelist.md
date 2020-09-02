---
title: Konfigurieren von Websites in der Enterprise Mode Site List
ms.author: cjacks
author: cjacks
manager: saudm
ms.date: 05/28/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Konfigurieren der Enterprise Site List
ms.openlocfilehash: 969a4f6001dbe08a51c26ecf35812b101d315a59
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/31/2020
ms.locfileid: "10980039"
---
# Konfigurieren von Websites in der Enterprise Mode Site List

In diesem Artikel werden die Änderungen an der Enterprise Mode Site List beschrieben, die das Konfigurieren des IE-Modus für die Microsoft Edge-Version 77 und höher unterstützen.

Weitere Informationen zum Schema der XML-Datei der Enterprise Mode Site List finden Sie unter [Anleitungen für Enterprise Mode-Schema v.2](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).

> [!NOTE]
> Dieser Artikel bezieht sich auf die Microsoft Edge-Kanäle **Stable**, **Beta** und **Dev**, Version 77 oder höher.

## Aktualisierte Schemaelemente

In der folgenden Tabelle wird das \<open-in app\>-Element beschrieben, das dem Unternehmensmodus-Schema V.2 hinzugefügt wurde:

| **Element** | **Beschreibung** |
| --- | --- |
| \<open-in app="**true**"\> | Ein untergeordnetes Element, das steuert, welcher Browser für Websites verwendet wird. Dieses Element ist für Websites erforderlich, die **in IE11 geöffnet** werden müssen.|

**Beispiel:**

``` xml
<site url="contoso.com">

  <open-in app="true">IE11</open-in>

</site>
```

In der folgenden Tabelle sind die möglichen Werte des \<open-in\>-Elements aufgeführt:

| **Wert** | **Beschreibung** |
| --- | --- |
| **\<open-in\>IE11\</open-in\>** | Öffnet die Website im IE-Modus oder in einem vollständigen IE11-Fenster. Informationen zum Aktivieren des IE-Modus finden Sie unter [Konfigurieren von Richtlinien für den IE-Modus](https://docs.microsoft.com/deployedge/edge-ie-mode-policies)|
| **\<open-in app="**true**"\>IE11\</open-in\>** | Öffnet die Website im IE-Modus oder in einem vollständigen IE11-Fenster |
| **\<open-in\>MSEdge\</open-in\>** | Öffnet die Website in Microsoft Edge |
| **\<open-in\>Keine oder nicht angegeben\</open-in\>** | Öffnet die Website im Standardbrowser oder in dem Browser, in dem der Benutzer zu der Website navigiert. |
|**\<open-in\>Konfigurierbar\</open-in\>** | Ermöglicht der Website die Teilnahme an der Bestimmung der IE-Modus-Engine. Weitere Informationen hierzu finden Sie unter [Informationen zu konfigurierbaren Sites im IE-Modus](edge-learnmore-configurable-sites-ie-mode.md).  |

>[!NOTE]
> Das Attribut app=**„true”** wird nur erkannt, wenn es mit _'open-in' IE11_ verknüpft ist. Durch das Hinzufügen zu den anderen 'open-in'-Elementen wird das Browserverhalten nicht geändert.   

## Konfigurieren von neutralen Websites

Damit der IE-Modus ordnungsgemäß funktioniert, müssen Authentifizierungs- bzw. Single Sign-On-Server explizit als neutrale Websites konfiguriert werden. Andernfalls versuchen die Seiten des IE-Modus, zu Microsoft Edge umzuleiten, und die Authentifizierung wird fehlschlagen.

Eine neutrale Website verwendet den Browser, in dem die Navigation begonnen wurde – entweder Microsoft Edge oder IE-Modus. Außerdem wird durch das Konfigurieren neutraler Websites sichergestellt, dass alle Anwendungen, die diese Authentifizierungsserver verwenden – sowohl moderne als auch ältere – weiterhin funktionsfähig sind.

Sie können neutrale Websites konfigurieren, indem Sie im Enterprise Mode Site List Manager-Tool für *Öffnen mit* in der Dropdownliste "Keine" festlegen, oder indem Sie das Websitelisten-XML direkt aktualisieren:

``` xml
<site url="login.contoso.com">
   
    <open-in>None</open-in>

</site>
```

Wenn Sie Authentifizierungsserver identifizieren möchten, überprüfen Sie den Netzwerkdatenverkehr einer Anwendung mithilfe der IE 11 Developer Tools. Wenn Sie mehr Zeit zum Identifizieren Ihrer Authentifizierungsserver benötigen, können Sie eine Richtlinie konfigurieren, um alle seiteninternen Navigationen im IE-Modus zu halten. Um die Verwendung des IE-Modus zu minimieren, deaktivieren Sie diese Einstellung, sobald Sie Ihre Authentifizierungsserver identifiziert und der Siteliste hinzugefügt haben. Weitere Informationen hierzu finden Sie unter [Konfigurieren Sie die seiteninterne Navigation so, dass sie im IE-Modus bleibt](https://docs.microsoft.com/deployedge/microsoft-edge-policies#internetexplorerintegrationsiteredirect).

>[!NOTE]
   >Das Unternehmensmodusschema V.1 wird für die Integration des IE-Modus nicht unterstützt. Wenn Sie derzeit SchemaV.1 mit Internet Explorer11 verwenden, müssen Sie ein Upgrade auf SchemaV.2 durchführen. Weitere Informationen finden Sie unter [Unternehmensmodusschema V.2-Richtlinien](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).

## Weitere Informationen

- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)
- [Informationen zum IE-Modus](https://docs.microsoft.com/deployedge/edge-ie-mode)
- [Weitere Informationen zum Unternehmensmodus](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)