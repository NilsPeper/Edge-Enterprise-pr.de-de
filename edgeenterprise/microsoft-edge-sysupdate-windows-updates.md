---
title: Windows-Updates zur Unterstützung von Microsoft Edge
ms.author: jtkim
author: dan-wesley
manager: srugh
ms.date: 11/17/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Windows-Updates zur Unterstützung von Microsoft Edge.
ms.openlocfilehash: 85f60b3ee09154c702debcfb222567996be9462f
ms.sourcegitcommit: e7f3098d8b7d91cae20b5778a71a87daababc312
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2022
ms.locfileid: "12298163"
---
# <a name="windows-updates-to-support-the-next-version-of-microsoft-edge"></a>Windows Updates zur Unterstützung der nächsten Version von Microsoft Edge

Dieser Artikel beschreibt, wie Windows aktualisiert wird, um die nächste Version von Microsoft Edge zu unterstützen

> [!IMPORTANT]
> Lesen Sie den [Blogbeitrag](https://aka.ms/EdgeLegacyEOS) des Microsoft Edge-Produktteams über das Serviceende der Vorgängerversion von Microsoft Edge.

> [!NOTE]
> Dieser Artikel bezieht sich auf den Microsoft Edge Stable-Kanal.

## <a name="microsoft-edge-and-the-windows-release-cycle"></a>Microsoft Edge und der Freigabezyklus der Windows-Versionen

Die nächste Version von Microsoft Edge bietet häufigere und flexiblere Aktualisierungsfunktionen. Da Browserversionen nicht an die Hauptversionen von Windows gebunden sind, werden Änderungen am Betriebssystem vorgenommen, um sicherzustellen, dass die nächste Version von Microsoft Edge nahtlos in Windows passt. Daher werden Featureupdates in einem 4-Wochen-Zyklus (ungefähr) veröffentlicht. Sicherheits- und Kompatibilitätsupdates werden nach Bedarf ausgeliefert.

## <a name="updates-and-the-user-experience"></a>Updates und die Benutzererfahrung

Updates ändern die Benutzererfahrung erst, wenn der Stable-Kanal der nächsten Version von Microsoft Edge installiert ist. Die Installation von Microsoft Edge Beta, Dev oder Canary löst keine Änderungen in Windows aus. Diese Browserversionen werden zusammen mit vorhandenen Browsern installiert.

Wenn alle Updates angewendet wurden UND der Stable-Kanal der nächsten Version von Microsoft Edge auf Systemebene installiert ist, werden die folgenden Änderungen auf dem System wirksam:

- Alle Startmenü-Pins, Kacheln und Verknüpfungen für die aktuelle Version von Microsoft Edge werden auf die nächste Version von Microsoft Edge migriert.
- Alle Taskleisten-Pins und Verknüpfungen für die aktuelle Version von Microsoft Edge werden auf die nächste Version von Microsoft Edge migriert.
- Die nächste Version von Microsoft Edge wird an die Taskleiste angeheftet. Wenn die aktuelle Version von Microsoft Edge bereits angeheftet ist, wird sie ersetzt.
- Die nächste Version von Microsoft Edge fügt eine Verknüpfung auf dem Desktop hinzu. Wenn für die aktuelle Version von Microsoft Edge bereits eine Verknüpfung vorhanden ist, wird sie ersetzt.
- Die meisten Protokolle, die standardmäßig von Microsoft Edge behandelt werden, werden auf die nächste Version von Microsoft Edge migriert.
- Die aktuelle Version von Microsoft Edge wird auf allen UX-Oberflächen im Betriebssystem ausgeblendet, einschließlich der Einstellungen, aller Apps und aller Dialogfelder zur Unterstützung von Dateien oder Protokollen.
- Bei allen Versuchen, die aktuelle Version von Microsoft Edge zu starten, wird auf die nächste Version von Microsoft Edge umgeleitet.

  > [!NOTE]
  > Installationen auf Benutzerebene lösen die oben genannten Verhaltensweisen nicht aus.

Zusammen mit den vorherigen Änderungen gibt es Änderungen, die unabhängig davon stattfinden, ob der Stable-Kanal der nächsten Version von Microsoft Edge installiert ist.

- Microsoft Edge hebt die Registrierung für Bücher und XML-Protokolle auf, die von der nächsten Version von Microsoft Edge nicht unterstützt werden. Benutzer, die versuchen, diese Protokolle zu öffnen, werden in einem Dialogfeld aufgefordert, eine Standard-App auszuwählen. Besuchen Sie den Microsoft Store, um unsere Empfehlungen für E-Book-Leser zu sehen.
  
## <a name="older-versions-of-windows"></a>Ältere Versionen von Windows

Um Microsoft Edge auf einem Gerät bereitzustellen, auf dem eine ältere Windows-Version als Windows 10 RS4 ausgeführt wird, verwenden Sie den [Konfigurations-Manager](https://docs.microsoft.com/mem/configmgr/apps/deploy-use/deploy-edge?bc=https%3A%2F%2Fdocs.microsoft.com%2FDeployEdge%2Fbreadcrumb%2Ftoc.json&toc=https%3A%2F%2Fdocs.microsoft.com%2FDeployEdge%2Ftoc.json) oder [Microsoft Intune](https://docs.microsoft.com/mem/intune/apps/apps-windows-edge?bc=https%3A%2F%2Fdocs.microsoft.com%2FDeployEdge%2Fbreadcrumb%2Ftoc.json&toc=https%3A%2F%2Fdocs.microsoft.com%2FDeployEdge%2Ftoc.json), oder führen Sie ein Upgrade auf eine unterstützte Version von Windows 10 durch. Im folgenden Artikel werden die derzeit unterstützten Versionen von Windows 10 und Windows 11 aufgeführt.

- [Unterstützte Versionen des Windows-Clients](/windows/release-health/supported-versions-windows-client)

> [!NOTE]
> Stellen Sie für Windows 10 RS4-20H1 eine Windows-LCU von Mai 2021 oder höher bereit, um Microsoft Edge abzurufen. Weitere Informationen finden Sie unter [Windows 10 Updateverlauf](https://support.microsoft.com/topic/windows-10-update-history-1b6aac92-bf01-42b5-b158-f80c6d93eb11)

> [!IMPORTANT]
> Wenn Sie Updates benötigen, die hier nicht aufgeführt sind, führen Sie bitte Windows Update aus, oder wenden Sie sich an Ihren Administrator.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)
- [Dokumentation für Microsoft Edge](./index.yml)