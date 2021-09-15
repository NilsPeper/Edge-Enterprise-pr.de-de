---
title: Deaktivieren von Internet Explorer 11
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 07/09/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Erfahren Sie, wie Sie Internet Explorer 11 deaktivieren und den Internet Explorer-Modus in Microsoft Edge verwenden können.
ms.openlocfilehash: b70da0ff7437d1f5e70cec40e31211046a66205a
ms.sourcegitcommit: 8968f3107291935ed9adc84bba348d5f187eadae
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/12/2021
ms.locfileid: "11979284"
---
# <a name="disable-internet-explorer-11"></a>Deaktivieren von Internet Explorer 11

>[!Note]
> Die Internet Explorer 11-Desktopanwendung wird eingestellt und wird ab dem 15. Juni 2022 nicht mehr unterstützt (eine Liste der in diesem Bereich enthaltenen Elemente [finden Sie in den FAQ](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549)). Dieselben IE11-Apps und -Websites, die Sie heute verwenden, können in Microsoft Edge im Internet Explorer-Modus geöffnet werden. [Weitere Informationen finden Sie hier](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/).

In diesem Artikel wird beschrieben, wie Sie Internet Explorer 11 als eigenständigen Browser in Ihrer Umgebung deaktivieren können.

## <a name="prerequisites"></a>Voraussetzungen

Die folgenden Windows-Updates und Microsoft Edge-Software sind erforderlich:

- Windows-Updates

  - Windows 10, Version 21H1 oder höher
  - Windows 10, Version 2004; Windows Serverversion 2004; Windows 10, Version 20H2; Windows Serverversion 20H2: [KB4598291](https://support.microsoft.com/topic/february-2-2021-kb4598291-os-builds-19041-789-and-19042-789-preview-6a766199-a4f1-616e-1f5c-58bdc3ca5e3b) oder höher
  - Windows 10 Version 1909: [KB4598298](https://support.microsoft.com/topic/january-21-2021-kb4598298-os-build-18363-1350-preview-02dfd9ba-91a2-1b82-dede-42f288c02511) oder höher
  - Windows Server 2019; Windows 10 Enterprise 2019 LTSC: [KB4598296](https://support.microsoft.com/topic/january-21-2021-kb4598296-os-build-17763-1728-preview-4c0931ff-45b7-ff59-5e00-c03b5afb363d) oder höher
  - Windows Server 2016; Windows 10 Enterprise 2016 LTSB: [KB4601318](https://support.microsoft.com/topic/february-9-2021-kb4601318-os-build-14393-4225-c5e3de6c-e3e6-ffb5-6197-48b9ce16446e) oder höher
  - Windows 10 Enterprise 2015 LTSB: [KB4601331](https://support.microsoft.com/office/february-9-2021%e2%80%94kb4601331-os-build-10240-18842-6227d078-fef3-8d67-27e0-1882e6cb79ff?ui=en-US&rs=en-US&ad=US) oder höher
  - Windows 8.1; Windows Server 2012 R2: [KB4601384](https://support.microsoft.com/topic/february-9-2021-kb4601384-monthly-rollup-16bdbb75-dd4b-2910-abc5-7891c9756b96) oder höher
  - Windows Server 2012: [KB4601348](https://support.microsoft.com/topic/february-9-2021-kb4601348-monthly-rollup-2c338c0c-73d6-fb80-cc91-f1a86e80db0c) oder höher
  
- Microsoft Edge Stable Channel


## <a name="overview"></a>Übersicht

Organisationen, die Internet Explorer 11 (IE11) für Abwärtskompatibilität benötigen, bietet der Internet Explorer-Modus (IE-Modus) in Microsoft Edge eine nahtlose, für sich stehende Browserumgebung. Benutzer können von Microsoft Edge aus auf ältere Anwendungen zugreifen, ohne zu IE11 zurückkehren zu müssen.

Nachdem Sie den IE-Modus konfiguriert haben, können Sie mithilfe von Gruppenrichtlinien IE11 als eigenständigen Browser in Ihrer Organisation deaktivieren, **ohne die Funktionalität des IE-Modus zu beeinträchtigen**.

> [!NOTE]
> Wenn Sie die eigenständige IE11-App für bestimmte Websites benötigen und der übrige Browsertraffic an Microsoft Edge weitergeleitet werden soll, können Sie die Richtlinie [Alle Websites, die nicht in der Websiteliste enthalten sind, an Microsoft Edge weiterleiten](./edge-ie-mode-policies.md#redirect-sites-from-ie-to-microsoft-edge) so konfigurieren, dass Websites von IE zu Microsoft Edge umgeleitet werden.

## <a name="user-experience-after-redirecting-traffic-to-microsoft-edge"></a>Benutzererfahrung nach dem Umleiten von Traffic zu Microsoft Edge

Wenn Sie die Richtlinie **Internet Explorer 11 als eigenständigen Browser deaktivieren** aktivieren, werden alle IE11-Aktivitäten zu Microsoft Edge umgeleitet, und die Benutzererfahrung sieht folgendermaßen aus:

- Das IE11-Symbol wird aus dem Startmenü entfernt, bleibt auf der Taskleiste jedoch erhalten.
- Wenn Benutzer versuchen, Verknüpfungen oder Dateizuordnungen zu starten, die IE11 verwenden, werden sie umgeleitet, um dieselbe Datei/URL in Microsoft Edge zu öffnen.
- Wenn Benutzer versuchen, IE11 zu starten, indem sie die iexplore.exe-Binärdatei direkt aufrufen, wird stattdessen Microsoft Edge gestartet.

Während des Festlegens der Richtlinie für diese Benutzererfahrung können Sie optional eine Umleitungsnachricht für jeden Benutzer anzeigen lassen, der versucht, IE11 zu öffnen. Für diese Meldung können Sie auswählen, ob sie "Immer" oder "Einmal pro Benutzer" angezeigt wird. Die im nächsten Screenshot dargestellte Umleitungsnachricht wird standardmäßig nie angezeigt.

:::image type="content" source="media/edge-ie-disable-ie11/disable-ie-redirect-msg.png" alt-text="Warnung beim Versuch, IE zu öffnen, wenn die Umleitung zu Microsoft Edge aktiv ist.":::

Wenn Ihre Websiteliste für den Unternehmensmodus Anwendungen enthält, die für das Öffnen in der IE11-App konfiguriert sind und Sie IE11 mit dieser Richtlinie deaktivieren, werden die Anwendungen in Microsoft Edge im IE-Modus geöffnet.
> [!NOTE]
> Es gab ein bekanntes Problem mit dem Benutzerablauf, das auftritt, wenn eine Website für das Öffnen in der IE11-Anwendung konfiguriert ist und die Richtlinie zum Deaktivieren von IE11 aktiv ist. Das Problem wurde in Microsoft Edge, Version 91.0.840.0 oder höher, behoben.

## <a name="disable-internet-explorer-11-as-a-standalone-browser"></a>Deaktivieren von Internet Explorer 11 als eigenständiger Browser

Führen Sie die folgenden Schritte aus, um Internet Explorer 11 mithilfe von Gruppenrichtlinien zu deaktivieren:

1. Stellen Sie sicher, dass Sie über die erforderlichen Betriebssystemupdates verfügen. In diesem Schritt werden die ADMX-Dateien auf Ihrem Computer direkt aktualisiert (insbesondere „inetres.adml“ und „inetres.admx“). Bitte beachten Sie, dass Sie, wenn Sie Ihren Central Store aktualisieren möchten, die ADML- und ADMX-Dateien von einem Computer kopieren müssen, der über die erforderlichen Updates verfügt. Weitere Informationen finden Sie unter [Erstellen und Verwalten des Central Store](/troubleshoot/windows-client/group-policy/create-and-manage-central-store)
2. Öffnen Sie den Gruppenrichtlinien-Editor.
3. Wechseln Sie zu ***Computerkonfiguration/Administrative Vorlagen/Windows-Komponenten/Internet Explorer***. 
4. Doppelklicken Sie auf  ** Internet Explorer 11 als eigenständigen Browser deaktivieren**.
5. Wählen Sie  **Aktiviert** aus.
6. Wählen Sie unter  **Optionen** einen der folgenden Einträge aus:

   - **Nie** , wenn Benutzer nicht darüber benachrichtigt werden sollen, dass IE11 deaktiviert ist.
   - **Immer** , wenn Benutzer jedes Mal benachrichtigt werden sollen, wenn sie von IE11 umgeleitet werden.
   - **Einmal pro Benutzer**  , wenn Benutzer nur beim ersten Umleiten benachrichtigt werden sollen.

7. Klicken Sie auf  **OK**  oder  **Übernehmen** , um diese Richtlinieneinstellung zu speichern.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)
- [Informationen zum IE-Modus](./edge-ie-mode.md)
- [Weitere Informationen zum Unternehmensmodus](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
