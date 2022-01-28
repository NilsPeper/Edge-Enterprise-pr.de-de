---
title: Häufig gestellte Fragen (FAQ) zu Microsoft Edge im Unternehmen
ms.author: collw
author: dan-wesley
manager: seanlynd
ms.date: 01/11/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Häufig gestellte Fragen (FAQ) zu Microsoft Edge im Unternehmen
ms.openlocfilehash: 86f1fdee4697d8087014e35daf41b600eeb62471
ms.sourcegitcommit: e7f3098d8b7d91cae20b5778a71a87daababc312
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2022
ms.locfileid: "12298317"
---
# <a name="microsoft-edge-frequently-asked-questions"></a>häufig gestellte Fragen Microsoft Edge

Dieser Artikel enthält häufig gestellte Fragen (FAQ) zu Microsoft Edge im Unternehmen.

> [!NOTE]
> Dieser Artikel bezieht sich auf Microsoft Edge Version 77 oder höher.

## <a name="how-do-i-know-which-version-of-microsoft-edge-i-have"></a>Woher weiß ich, welche Version von Microsoft Edge ich habe?

Wählen Sie das Ellipsensymbol (**...**) in der oberen rechten Ecke von Microsoft Edge aus, und wählen Sie dann **Einstellungen**aus. Wählen Sie **Über Microsoft Edge** aus, um Ihre Version von Microsoft Edge anzuzeigen.

## <a name="what-about-internet-explorer-11"></a>Was ist mit Internet Explorer 11?

Die Internet Explorer 11-Desktopanwendung wird eingestellt und wird am 15. Juni 2022 nicht mehr unterstützt. Informationen zum Umfang finden Sie unter [The future of Internet Explorer on Windows 10 is in Microsoft Edge](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/). Dieselben IE11-Apps und -Websites, die Sie heute verwenden, können in Microsoft Edge im Internet Explorer-Modus geöffnet werden. Weitere Informationen finden Sie unter [Internet Explorer 11 desktop app retirement FAQ](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549).

## <a name="does-microsoft-edge-support-activex-controls-or-browser-helper-objects-like-silverlight-or-java"></a>Unterstützt Microsoft Edge ActiveX Steuerelemente oder Browserhilfsobjekte wie Silverlight oder Java?

Nein. Microsoft Edge unterstützt keine ActiveX Steuerelemente oder Browserhilfeobjekte (BROWSER Help Objects, BHOs) wie Silverlight oder Java. Wenn Sie jedoch Web-Apps ausführen, die ActiveX Steuerelemente, BHOs oder ältere Dokumentmodi in Internet Explorer 11 verwenden, können Sie diese so konfigurieren, dass sie im IE-Modus auf Microsoft Edge ausgeführt werden. Weitere Informationen finden Sie unter [Konfigurieren des IE-Modus in Microsoft Edge](./edge-ie-mode.md).

## <a name="will-favorites-be-ported-over-from-the-current-version-of-microsoft-edge-or-will-i-have-to-re-add-them"></a>Werden Favoriten von der aktuellen Version von Microsoft Edge portiert oder muss ich sie erneut hinzufügen?

Microsoft Edge unterstützt den Import aus vorhandenen Installationen von Microsoft Edge, Chrome, Internet Explorer und Firefox (unter Win10). Die folgenden Einstellungen werden für den Import unterstützt: Lesezeichen, Verlauf, Kennwörter und AutoAusfüllen (Zahlungen, Adressen und generische Formulare). Sie können entweder aus der ersten Ausführung oder aus den Browsereinstellungen importieren.

## <a name="whats-the-difference-between-the-stable-beta-dev-and-canary-channelsbuilds"></a>Worin besteht der Unterschied zwischen den Kanälen/Builds Beta, Dev und Canary?

Der Stable-Kanal von Microsoft Edge ist der stabilste Kanal, den wir mit unternehmensorientierten Features anbieten, die Sie für [das Pilotprojekt und die Bewertung](https://aka.ms/EdgeEnterprise) in Ihrer Organisation bereithalten können. Mit dem Beta-Kanal können Sie die nächste Stable-Version mit einer repräsentativen Gruppe von Benutzern überprüfen. Die Stable- und Beta-Kanäle werden ungefähr alle sechs Wochen aktualisiert. Die Dev- und Canary-Kanäle werden weiterhin wöchentlich bzw. täglich aktualisiert. Offline-Installationsprogramme (MSIs und PKG-Dateien) sind nur für Stable-, Beta- und Dev-Kanäle verfügbar. Weitere Informationen finden Sie unter [Übersicht über Microsoft Edge-Kanäle](./microsoft-edge-channels.md).

## <a name="what-kind-of-extension-support-do-i-have-with-microsoft-edge"></a>Welche Art von Erweiterungsunterstützung habe ich mit Microsoft Edge?

Microsoft Edge unterstützt Erweiterungen von [Microsoft Edge Insider-Add-Ins](https://go.microsoft.com/fwlink/?linkid=2081222) und der [Chrome Web Store.](https://go.microsoft.com/fwlink/?linkid=2072338)

## <a name="do-you-support-mobile-device-management-mdm-and-microsoft-intune"></a>Werden die mobile Geräteverwaltung (Mobile Device Management, MDM) und Microsoft Intune unterstützt?

Ja. Das Konfigurieren von Microsoft Edge unter Windows 10 mit Microsoft Intune und der mobilen Geräteverwaltung (Mobile Device Management, MDM) wird jetzt unterstützt. Weitere Informationen finden Sie unter [Konfigurieren von Microsoft Edge mit Microsoft Intune](./configure-edge-with-intune.md) und [Konfigurieren von Microsoft Edge mithilfe der Verwaltung mobiler Geräte](./configure-edge-with-mdm.md).

## <a name="does-windows-server-update-services-wsus-support-the-initial-deployment-of-microsoft-edge"></a>Unterstützt Windows Server Update Services (WSUS) die anfängliche Bereitstellung von Microsoft Edge?

Ja. Es gibt Pakete im [Microsoft Update-Katalog,](https://www.catalog.update.microsoft.com/Search.aspx?q=the%20new%20microsoft%20edge%20for%20windows) die für die anfängliche Bereitstellung von Microsoft Edge über WSUS verwendet werden können. Nach der Erstbereitstellung werden automatische Updates standardmäßig konfiguriert. Weitere Informationen finden Sie unter [Update in WSUS für das neue MicrosoftEdge für Windows10, Version1809, 1903, 1909 und 2004: 29.Oktober2020](https://support.microsoft.com/help/4584642/update-in-wsus-for-the-new-microsoft-edge).

 Manuelle Updates können über ein Konfigurationsverwaltungstool wie [ConfigMgr](/configmgr/apps/deploy-use/deploy-edge?bc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2ftoc.json)erfolgen.

## <a name="are-initial-preferences-supported"></a>Werden die anfänglichen Einstellungen unterstützt?

Ja. Weitere Informationen finden Sie unter [Konfigurieren Microsoft Edge mit den Einstellungen für die anfänglichen Einstellungen für die erste Ausführung](./initial-preferences-support-on-microsoft-edge-browser.md)

## <a name="see-also"></a>Weitere Informationen

- [Angebotsseite der Microsoft Edge-Dokumentation](./index.yml)
- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)
  