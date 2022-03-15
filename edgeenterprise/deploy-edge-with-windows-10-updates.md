---
title: Bereitstellen von Microsoft Edge mit Windows 10-Updates
ms.author: ryhecht
author: RyanHechtMSFT
manager: tinad
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Bereitstellen von Microsoft Edge mit Windows 10-Updates
ms.openlocfilehash: 1f3a99259cb28c46e4f6f30de05fade6ac158336
ms.sourcegitcommit: 556aca8dde42dd66364427f095e8e473b86651a0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2022
ms.locfileid: "12445829"
---
# <a name="deploy-microsoft-edge-with-windows-10-updates"></a>Bereitstellen von Microsoft Edge mit Windows 10-Updates

Der Artikel enthält Informationen für Benutzer, die Microsoft Edge mithilfe von Windows 10-Updates bereitstellen.

## <a name="for-windows-10-release-20h2"></a>Für Windows 10, Release 20H2

Windows 10 20H2 und höher enthalten Microsoft Edge als Standardbrowser vorinstalliert. Version 84 von Edge, die mit Windows 10 20H2 ausgeliefert wurde, und Version 92 von Edge, die mit Windows 10 21H2 ausgeliefert wurde, sind jetzt veraltet. Während Microsoft Edge sich automatisch auf eine neuere Version aktualisieren, nachdem sich ein Benutzer angemeldet hat, da der Zeitpunkt des Updates von verschiedenen Faktoren abhängt, kann dies etwas unaufdränglich sein. Für Organisationen, die mehr Kontrolle wünschen und sicherstellen möchten, dass Edge (Stable Channel) vor der Benutzeranmeldung auf die neueste Version aktualisiert wird, kann der folgende PowerShell-Befehl verwendet werden, um ein Edgeupdate während Windows Windows-Willkommensseite zu erzwingen.

`Start-Process -FilePath "C:\Program Files (x86)\Microsoft\EdgeUpdate\MicrosoftEdgeUpdate.exe" -argumentlist "/silent /install appguid={56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}&appname=Microsoft%20Edge&needsadmin=True"`

Wenn Sie Windows Autopilot verwenden, ist es möglich, dieses Skript mithilfe des [Microsoft Win32-Inhaltsvorbereitungstools](/mem/intune/apps/apps-win32-prepare) als INTUNEWIN-Datei einzuschließen. Sie kann dann bei Bedarf als erforderliche App für die Registrierungsstatusseite (Esp) festgelegt werden.

> [!NOTE]
> Wenn Sie derzeit Richtlinien wie [die Außerkraftsetzung des Zielkanals](/deployedge/microsoft-edge-update-policies#target-channel-override) oder die [Außerkraftsetzung der Zielversion](/deployedge/microsoft-edge-update-policies#targetversionprefix) nutzen, um auf einer älteren Version von Edge zu verbleiben, beachten Sie, dass das obige Skript keine Richtlinien berücksichtigt und einfach auf die neueste Version aktualisiert wird. Standardmäßig stuft Edge sich selbst nicht herunter, einschließlich, sobald diese Richtlinien später empfangen werden.

## <a name="for-windows-10-releases-rs4-through-20h1"></a>Für Windows 10, Release RS4 bis 20H1

Windows Server Update Services (WSUS) verfügt über Updates für jede Version von Windows 10 von RS4 bis 20H1, die die Desktop-App der Vorgängerversion von Microsoft Edge entfernt und durch Microsoft Edge ersetzt. Weitere Informationen finden Sie in [diesem Supportartikel](https://support.microsoft.com/topic/update-in-wsus-for-the-new-microsoft-edge-for-windows-10-version-1809-1903-1909-and-2004-october-29-2020-b4980418-4ec4-dee7-3b17-1c6499bd127c). Hier erfahren Sie, welches WSUS-Update für Ihre Windows-Version geeignet ist.

## <a name="for-windows-10-releases-prior-to-rs4-and-windows-7-81-and-earlier"></a>Für Windows 10-Releases vor RS4 (sowie Windows 7, 8.1 und früher)

Windows-Updates zur Installation von Microsoft Edge sind für diese Versionen nicht verfügbar. Ziehen Sie andere Optionen für die Bereitstellung von Microsoft Edge auf diesen Geräten in Betracht, z. B. den [Konfigurations-Manager](/configmgr/apps/deploy-use/deploy-edge?bc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2ftoc.json) oder [Intune](/intune/apps/apps-windows-edge/?bc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2ftoc.json).

## <a name="see-also"></a>Weitere Informationen

- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)
- [Planen Ihrer Bereitstellung von Microsoft Edge](deploy-edge-plan-deployment.md)
