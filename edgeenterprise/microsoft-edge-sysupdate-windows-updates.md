---
title: Windows Updates für Microsoft Edge
ms.author: jtkim
author: dan-wesley
manager: srugh
ms.date: 06/28/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Windows Updates für Microsoft Edge.
ms.openlocfilehash: b99d3d7ed048cb829fd2328be9e4e7376334652c
ms.sourcegitcommit: 8968f3107291935ed9adc84bba348d5f187eadae
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/12/2021
ms.locfileid: "11979108"
---
# <a name="windows-updates-to-support-the-next-version-of-microsoft-edge"></a>Windows Updates zur Unterstützung der nächsten Version von Microsoft Edge

In diesem Artikel wird beschrieben, wie Windows aktualisiert wird, um die nächste Version von Microsoft Edge zu unterstützen.

> [!IMPORTANT]
> Lesen Sie den [Blogbeitrag](https://aka.ms/EdgeLegacyEOS) des Microsoft Edge-Produktteams über das Serviceende der Vorgängerversion von Microsoft Edge.

> [!NOTE]
> Dieser Artikel bezieht sich auf den Microsoft Edge Stable-Kanal.

## <a name="microsoft-edge-and-the-windows-release-cycle"></a>Microsoft Edge und der Freigabezyklus der Windows-Versionen

Die nächste Version von Microsoft Edge bietet häufigere und flexiblere Aktualisierungsfunktionen. Da Browserversionen nicht an die Hauptversionen von Windows gebunden sind, werden Änderungen am Betriebssystem vorgenommen, um sicherzustellen, dass die nächste Version von Microsoft Edge nahtlos in Windows passt. Aus diesem Grund werden Featureupdates in einem (etwa) 6-wöchigen Zyklus veröffentlicht. Sicherheits- und Kompatibilitätsupdates werden nach Bedarf ausgeliefert.

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
  > Im Falle einer Installation auf Benutzerebene werden diese Verhaltensweisen nicht ausgelöst.

Zusammen mit den vorherigen Änderungen gibt es Änderungen, die unabhängig davon stattfinden, ob der Stable-Kanal der nächsten Version von Microsoft Edge installiert ist.

- Microsoft Edge hebt die Registrierung für Bücher und XML-Protokolle auf, die von der nächsten Version von Microsoft Edge nicht unterstützt werden. Benutzer, die versuchen, diese Protokolle zu öffnen, werden in einem Dialogfeld aufgefordert, eine Standard-App auszuwählen. Weitere Informationen zu Änderungen an Büchern finden Sie unter [Herunterladen einer ePub-App zum Lesen von E-Books](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fsupport.microsoft.com%2Fhelp%2F4517840&data=02%7C01%7Cv-danwes%40microsoft.com%7Cc9f8571b880549c30fcf08d72be5eaf9%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637026138803983526&sdata=qtb3DvVZQ6H%2FFXnBievkl%2B%2BngAQXwl340PcH8kRc3y4%3D&reserved=0).

## <a name="timeline"></a>Zeitachse

Die Änderungen, die zur Unterstützung der beschriebenen Erfahrung erforderlich sind, werden mit drei Updates für verschiedene Versionen von Windows bereitgestellt.

### <a name="windows-versions-1903-and-1909"></a>Windows-Versionen 1903 und 1909

- Erster Satz von Änderungen im optionalen Update vom Juli 2019, das mit dem Sicherheitsupdate vom August 2019 ausgeliefert wurde.
- Zweiter Satz von Änderungen im optionalen Update vom August 2019, das mit dem Sicherheitsupdate vom September 2019 ausgeliefert wurde.

  > [!NOTE]
  > Dies ist das Update, bei dem Microsoft Edge die Registrierung für das XML-Protokoll aufhebt.

- Dritter Satz von Änderungen im optionalen Update vom September 2019, das mit dem Sicherheitsupdate vom Oktober 2019 ausgeliefert wurde.

  > [!NOTE]
  > Dies ist das Update, ab dem Microsoft Edge keine E-Books mehr unterstützt.

### <a name="windows-versions-1709-1803-and-1809"></a>Windows Versionen 1709, 1803 und 1809

- Erster Satz von Änderungen im optionalen Update vom August 2019, das mit dem Sicherheitsupdate vom September 2019 ausgeliefert wurde.
- Zweiter Satz von Änderungen im optionalen Update vom September 2019, das mit dem Sicherheitsupdate vom Oktober 2019 ausgeliefert wurde.

  > [!NOTE]
  > Dies ist das Update, bei dem Microsoft Edge die Registrierung für das XML-Protokoll aufhebt.

- Dritter Satz von Änderungen im optionalen Update vom Oktober 2019, das mit dem Sicherheitsupdate vom November 2019 ausgeliefert wurde.

  > [!NOTE]
  > Dies ist das Update, ab dem Microsoft Edge keine E-Books mehr unterstützt.

In der folgenden Tabelle sind die Details für bestimmte Aktualisierungen in den einzelnen Änderungssätzen aufgeführt.

| Windows 10 | Weitere Informationen | Erforderlicher Download |
|--|--|--|
| Version 1709 | [KB4525241](https://support.microsoft.com/help/4525241/windows-10-update-kb4525241) | [Kumulatives Update für Windows 10, Version 1709](https://www.catalog.update.microsoft.com/Search.aspx?q=4525241) |
| Version 1803  | [KB4525237](https://support.microsoft.com/help/4525237/windows-10-update-kb4525237) | [Kumulatives Update für Windows 10, Version 1803](https://www.catalog.update.microsoft.com/Search.aspx?q=KB4525237) |
| Version 1809  | [KB4523205](https://support.microsoft.com/help/4523205/windows-10-update-kb4523205) | [Kumulatives Update für Windows 10, Version 1809](https://www.catalog.update.microsoft.com/Search.aspx?q=4523205) |
| Version 1903 und 1909 |[KB4517389](https://support.microsoft.com/help/4517389/windows-10-update-kb4517389)  | [Kumulatives Update für Windows 10, Version 1903 und 1909](https://www.catalog.update.microsoft.com/Search.aspx?q=4517389) |

## <a name="see-also"></a>Weitere Informationen

- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)
- [Dokumentation für Microsoft Edge](./index.yml)