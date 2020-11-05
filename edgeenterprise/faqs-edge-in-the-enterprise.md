---
title: Häufig gestellte Fragen zu Edge im Unternehmen
ms.author: jwhit
author: jwhit-MSFT
manager: laurawi
ms.date: 11/04/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Häufig gestellte Fragen zur Bereitstellung von Microsoft Edge im Unternehmen
ms.openlocfilehash: e689967cbad950e2969535bad0dd63d5d7081798
ms.sourcegitcommit: 12827458f6217f443128e826c1d18d36d401d03b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "11154320"
---
# Häufig gestellte Fragen zu Microsoft Edge im Unternehmen

> [!NOTE]
> Dieser Artikel bezieht sich auf Microsoft Edge Version77 oder höher.

## Woher weiß ich, welche Version von Microsoft Edge ich habe?

Klicken Sie in der rechten oberen Ecke von Microsoft Edge auf die Auslassungspunkte (**…**) und dann auf **Einstellungen**. Wählen Sie **Über Microsoft Edge** aus, um Ihre Version von Microsoft Edge anzuzeigen.

## Wird es für Internet Explorer 11 auch weiterhin Updates geben?

Wir bemühen uns, Internet Explorer als unterstützten, zuverlässigen und sicheren Browser zu erhalten. Internet Explorer ist weiterhin eine Komponente des Windows-Betriebssystems, und verfügt daher über denselben Supportlebenszyklus wie das Betriebssystem, auf dem er installiert ist. Weitere Informationen finden Sie unter [Häufig gestellte Fragen zum Lebenszyklus – Internet Explorer](https://support.microsoft.com/help/17454/). Zwar unterstützen und aktualisieren wir Internet Explorer weiterhin, sind die neuesten Funktionen und Plattformaktualisierungen nur in Microsoft Edge verfügbar.

## Kann ich die aktuelle Version von Microsoft Edge (Microsoft Edge Legacy) parallel ausführen, wenn ich die neue Version teste?

Ja, können Sie. Nach dem 15. Januar 2020 wird die neue Version von Microsoft Edge (Chromium-basiert) an Geräte mit der Home- und Pro-Edition von Windows 10 (Version 1803 oder neuer) verteilt. Geräte, die einer Domäne angehören, sind von diesem Update ausgeschlossen. Weitere Informationen finden Sie unter [Übersicht über Microsoft Edge-Updates](https://docs.microsoft.com/deployedge/microsoft-edge-blocker-toolkit#overview). Sie können Microsoft Edge Legacy zusätzlich installieren, wenn Sie die nächste Version von Microsoft Edge evaluieren. Weitere Informationen finden Sie unter [Zugreifen auf die alte Version von Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-sysupdate-access-old-edge). Zudem wird jeder der neuen Microsoft Edge-Kanäle auch Parallelinstallationen unterstützen. Weitere Informationen finden Sie unter [Übersicht über Microsoft Edge-Kanäle](https://docs.microsoft.com/deployedge/microsoft-edge-channels).

## Unterstützt Microsoft Edge (Chromium-basiert) ActiveX-Steuerelemente oder BHOs wie Silverlight oder Java?

Nein. Microsoft Edge unterstützt keine ActiveX-Steuerelemente oder BHOs wie Silverlight oder Java. Wenn Sie jedoch Web-Apps ausführen, die ActiveX-Steuerelemente, BHOs oder veraltete Dokumentmodi in Internet Explorer 11 verwenden, können Sie diese so konfigurieren, dass Sie im neuen Microsoft Edge im IE-Modus ausgeführt werden. Weitere Informationen finden Sie unter [Konfigurieren des IE-Modus in Microsoft Edge](https://docs.microsoft.com/DeployEdge/edge-ie-mode).

## Werden Favoriten aus der aktuellen Version von Microsoft Edge portiert oder muss ich sie erneut hinzufügen?

Derzeit unterstützt Microsoft Edge den Import aus vorhandenen Installationen von Microsoft Edge, Chrome, Internet Explorer und Firefox (auf Win10). Die folgenden Einstellungen werden für den Import unterstützt: Lesezeichen, Verlauf, Kennwörter und AutoAusfüllen (Zahlungen, Adressen und generische Formulare). Sie können entweder aus der ersten Ausführung oder aus den Browsereinstellungen importieren.  

## Worin besteht der Unterschied zwischen den Kanälen/Builds Beta, Dev und Canary?

Die Stable-Kanal der nächsten Version von Microsoft Edge ist der stabilste Kanal, den wir anbieten, und verfügt über unternehmensspezifische Funktionen, die Sie unternehmensübergreifend [testen und bewerten](https://aka.ms/EdgeEnterprise) können. Mit dem Beta-Kanal können Sie die nächste Stable-Version mit einer repräsentativen Gruppe von Benutzern überprüfen. Die Stable- und Beta-Kanäle werden etwa alle sechs Wochen aktualisiert. Die Kanäle „Dev” und „Canary” werden weiterhin wöchentlich und täglich aktualisiert. Offline-Installationsprogramme (MSIS und PKG-Dateien) stehen nur für Stable-, Beta-und Dev-Kanäle zur Verfügung. Weitere Informationen finden Sie unter [Übersicht über Microsoft Edge-Kanäle](https://docs.microsoft.com/deployedge/microsoft-edge-channels).

## Welche Art von Erweiterungsunterstützung habe ich mit der neuen Version von Microsoft Edge?

Microsoft Edge unterstützt Erweiterungen von [Microsoft Edge Insider-Addons](https://go.microsoft.com/fwlink/?linkid=2081222) und dem [Chrome Web Store](https://go.microsoft.com/fwlink/?linkid=2072338).

## Werden die mobile Geräteverwaltung (Mobile Device Management, MDM) und Microsoft Intune unterstützt?

Ja. Das Konfigurieren von Microsoft Edge unter Windows10 mit Microsoft Intune und der mobilen Geräteverwaltung (Mobile Device Management, MDM) wird jetzt unterstützt. Weitere Informationen finden Sie unter [Konfigurieren von Microsoft Edge mit Microsoft Intune](configure-edge-with-intune.md) und [Konfigurieren von Microsoft Edge mithilfe der Verwaltung mobiler Geräte](configure-edge-with-mdm.md).

## Unterstützt WSUS die Erstbereitstellung des neuen Microsoft Edge?

Ja. Es gibt Pakete im [Microsoft Update-Katalog](https://www.catalog.update.microsoft.com/Search.aspx?q=the%20new%20microsoft%20edge%20for%20windows), die für die Erstbereitstellung des neuen MicrosoftEdge über WSUS verwendet werden können. Nach der Erstbereitstellung werden automatische Updates standardmäßig konfiguriert. Weitere Informationen finden Sie unter [Update in WSUS für das neue MicrosoftEdge für Windows10, Version1809, 1903, 1909 und 2004: 29.Oktober2020](https://support.microsoft.com/help/4584642/update-in-wsus-for-the-new-microsoft-edge).

Manuelle Updates können mithilfe eines Konfigurationsverwaltungstools, z.B. [ConfigMgr](https://docs.microsoft.com/configmgr/apps/deploy-use/deploy-edge?toc=https://docs.microsoft.com/DeployEdge/toc.json&bc=https://docs.microsoft.com/DeployEdge/breadcrumb/toc.json), durchgeführt werden.

## Weitere Informationen

- [Angebotsseite der Microsoft Edge-Dokumentation](https://docs.microsoft.com/DeployEdge/)
- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)
