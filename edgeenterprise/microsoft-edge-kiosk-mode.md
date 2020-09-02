---
title: Microsoft Edge-Kioskmodus
ms.author: brianalt
author: brianalt
manager: seanlynd
ms.date: 01/16/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Edge-Kioskmodus
ms.openlocfilehash: 7a690820752b5361349bf394055a737bd8175215
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/31/2020
ms.locfileid: "10980060"
---
# Microsoft Edge-Kioskmodus

Dieser Artikel enthält eine Übersicht über die Optionen für Microsoft Edge (Version 77 oder höher) im Kioskmodus. Außerdem wird erläutert, was erforderlich ist, um den Kioskmodus von Microsoft Edge Legacy (Version 45 und früher) weiterhin zu verwenden.

Informationen zum Kioskmodus von Microsoft Edge Legacy (Version 45 und früher) finden Sie unter [Bereitstellen des Microsoft Edge-Kioskmodus](https://aka.ms/edgekioskmode).

## Microsoft Edge mit zugewiesenem Zugriff

Microsoft Edge kann unter Windows 10 mit [zugewiesenem Multi-App-Zugriff](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps) ausgeführt werden, was dem Kioskmodustyp „Normales Browsen” von Microsoft Edge Legacy entspricht. Zum Konfigurieren von Microsoft Edge mit zugewiesenem Multi-App-Zugriff folgen Sie den Anweisungen unter [Einrichten eines Multi-App-Kiosks](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps). Die AUMID für den Stable-Kanal von Microsoft Edge ist **MSEdge**.

Bei der Verwendung von Microsoft Edge mit zugewiesenem Multi-App-Zugriff können Sie die [Microsoft Edge-Browserrichtlinien](microsoft-edge-policies.md) verwenden, um das Browsingerlebnis Ihren individuellen Anforderungen entsprechend zu konfigurieren.

Derzeit unterstützt Microsoft Edge nicht die gleichen Microsoft Edge Legacy-Kioskmodustypen für zugewiesenen Einzel-App-Zugriff und den Kioskmodustyp „Öffentliches Browsing” für den zugewiesenen Multi-App-Zugriff. Wenn Sie einen Browser mit zugewiesenem Einzel-App-Zugriff für Ihr Kioskgerät benötigen, empfehlen wir die Verwendung des [Microsoft Edge Legacy-Kioskmodus](https://aka.ms/edgekioskmode) oder der [Microsoft Kiosk Browser-App](https://www.microsoft.com/p/kiosk-browser/9ngb5s5xg2kp?activetab=pivot:overviewtab). 

## Microsoft Edge "--kiosk"-Befehlszeilenparameter

Mit dem Befehlszeilenparameter "`--kiosk`" können Sie Microsoft Edge im Kioskmodus starten. Dadurch wird der Browser im Vollbildmodus geöffnet. Der Tastaturkurzbefehl für den Vollbildmodus (F11) ist dabei deaktiviert. Um dies zu erreichen, erstellen Sie eine Verknüpfung mit folgendem Ziel:<br>
*`"<local path>\msedge.exe" --kiosk http://bing.com`*

> [!NOTE]
> Der "`--kiosk`"-Parameter verhindert weder, dass der Benutzer auf Windows-Tastaturkurzbefehle zugreifen kann, noch dass andere Anwendungen ausgeführt werden. Um diese Art von Kontrolle zu erreichen, können Sie einen [Windows 10-Kiosk mit AppLocker erstellen](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-applocker) und [Tastaturfilter verwenden](https://docs.microsoft.com/windows-hardware/customize/enterprise/keyboardfilter).

Verwenden Sie ALT+F4, um den Kioskmodus zu beenden und den Browser zu schließen.

## Unterstützung für Microsoft Edge Legacy-Kioskmodus

Wenn die neue Stable-Kanal-Version von Microsoft Edge installiert ist, wird Microsoft Edge Legacy ausgeblendet, und alle Versuche, Microsoft Edge Legacy zu starten, werden auf die neue Version umgeleitet. Weitere Informationen

- Anforderungen für Windows-Updates finden Sie unter [Windows-Updates zur Unterstützung der nächsten Version von Microsoft Edge](microsoft-edge-sysupdate-windows-updates.md). 
- Hinwiese für den Zugriff auf Microsoft Edge Legacy nach der Installation von Microsoft Edge finden Sie unter [Zugreifen auf Microsoft Edge Legacy nach der Installation der neuen Version von Microsoft Edge](microsoft-edge-sysupdate-access-old-edge.md)
 
Um den Kioskmodus von Microsoft Edge Legacy auf Ihren Kioskgeräten weiterhin zu verwenden, führen Sie eine der folgenden Aktionen durch: 

- Wenn Sie beabsichtigen, den Microsoft Edge Stable-Kanal zu installieren, seine Installation zulassen möchten oder wenn er bereits auf Ihrem Kioskgerät installiert ist, stellen Sie die Microsoft Edge-Richtlinie [Microsoft Edge-Browser im Parallelbetrieb zulassen](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#allowsxs) bereit.
- Um die Installation von Microsoft Edge Stable-Kanal auf Ihren Kioskgeräten zu verhindern, stellen Sie die Microsoft Edge-Richtlinie [Standardinstallation zulassen](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#allow-installation-default) für den Stable-Kanal bereit oder verwenden das [Blocker-Toolkit zur Deaktivierung der automatischen Bereitstellung von Microsoft Edge](microsoft-edge-blocker-toolkit.md). 

## Weitere Informationen

- [Konfigurieren von Kiosken und digitalen Anmeldungen in Windows-Desktopeditionen](https://docs.microsoft.com/windows/configuration/kiosk-methods)
- [Bereitstellen des Microsoft Edge Legacy-Kioskmodus](https://aka.ms/edgekioskmode) 
- [Planen Ihrer Bereitstellung von Microsoft Edge](deploy-edge-plan-deployment.md)
- [Angebotsseite für Microsoft Edge für Unternehmen](https://aka.ms/EdgeEnterprise)
