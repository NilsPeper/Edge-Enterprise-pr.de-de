---
title: Blocker Toolkit zum Deaktivieren der automatischen Übermittlung von Microsoft Edge
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 06/30/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Blocker Toolkit zum Deaktivieren der automatischen Übermittlung von Microsoft Edge
ms.openlocfilehash: 7563d2c94cf91a8434328699e46c75dbcfb77561
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/31/2020
ms.locfileid: "10980055"
---
# Blocker Toolkit zum Deaktivieren der automatischen Bereitstellung von Microsoft Edge (Chromium-basiert)

In diesem Artikel wird das Blocker Toolkit zum Deaktivieren der automatischen Übermittlung und Installation von Microsoft Edge beschrieben. Dieser Artikel wurde aktualisiert: am **09.01.2020** mit weiteren Informationen zu Geräten, die möglicherweise die Verwendung des Blocker-Toolkits erfordern, am **28.02.2020**, um „MDM-verwaltet“ aus den Kriterien von Geräten zu entfernen, die bei diesem automatischen Update ausgeschlossen werden sollen, und am **30.06.2020**, um darauf hinzuweisen, dass alle mit WindowsUpdate verbundenen Geräte dieses Update erhalten können (wird nicht vor dem 30.07.2020 wirksam).

> [!NOTE]
> Dieser Artikel bezieht sich auf den stabilen Kanal von Microsoft Edge.

## Übersicht

Um unseren Kunden zu helfen, sicherer und aktueller zu werden, wird Microsoft den Browser MicrosoftEdge (Chromium-basiert) an alle mit WindowsUpdate verbundenen Geräte unter Windows10 (ab Version1803) verteilen. Dieser Prozess startet nach dem 15.Januar 2020. An diesem Datum stehen weitere Informationen zur Verfügung.

Das Blocker Toolkit richtet sich an Organisationen, die die automatische Bereitstellung von MicrosoftEdge (Chromium-basiert) auf mit Windows Update verbundenen Geräten unter Windows10 (ab Version1803) blockieren möchten.
Durch Windows Server Update Services (WSUS) oder Windows Update for Business (WUfB) verwaltete Geräte werden bei dieser automatischen Aktualisierung ausgeschlossen.

**Beachten Sie unbedingt Folgendes:**

- Das Blocker Toolkit kann nicht verhindern, dass Benutzer Microsoft Edge (Chromium-basiert) manuell aus dem Internet oder von externen Medien herunterladen und installieren.
- Organisationen mit Updates, die über Windows Update for Business (WUfB) verwaltet werden, erhalten dieses Update nicht automatisch und müssen das Blocker Toolkit nicht bereitstellen.
- Organisationen mit Umgebungen, die mit einer Update-Verwaltungslösung wie Windows Server Update Services (WSUS) oder System Center Konfigurations-Manager (SCCM) verwaltet werden, müssen das Blocker Toolkit nicht bereitstellen. Sie können diese Produkte verwenden, um die Bereitstellung von Updates, die über Windows Update und Microsoft Update veröffentlicht wurden, einschließlich Microsoft Edge (Chromium-basiert), in ihrer Umgebung vollständig zu verwalten.
- Dieses Update ist ein eigenständiges Update (also nicht Teil des monatlichen kumulativen Updates), damit die Unternehmenskunden Flexibilität und maximale Kontrolle über die Bereitstellung dieses Updates haben.
- Das neue MicrosoftEdge (Chromium-basiert) wird im Rahmen des Windows10-Funktionsupdates, Version20H2, in der zweiten Hälfte von 2020 einbezogen. Das Blocker-Toolkit wirkt sich nicht auf das Verhalten oder die Bereitstellung von 20H2 aus. Weitere Informationen zu Windows10, Version20H2, finden Sie [hier](https://blogs.windows.com/windowsexperience/2020/06/16/whats-next-for-windows-10-updates/).

Sie können die ausführbare Datei des Blocker Toolkit unter [https://msedgeblockertoolkit.blob.core.windows.net/blockertoolkit/MicrosoftEdgeChromiumBlockerToolkit.exe](https://msedgeblockertoolkit.blob.core.windows.net/blockertoolkit/MicrosoftEdgeChromiumBlockerToolkit.exe) herunterladen.

### Toolkit-Komponenten

Diese Toolkit enthält die folgenden Komponenten:

- Ausführbares Blocker-Skript (.CMD)
- Administrative Vorlage für Gruppenrichtlinien (.ADMX und .ADML)

### Unterstützte Betriebssysteme

Windows 10 ab Version 1803

## Blocker-Skript

Das Skript erstellt einen Registrierungsschlüssel und setzt den zugehörigen Wert so, dass er die automatische Bereitstellung von Microsoft Edge (Chromium-basiert) auf dem lokalen Computer oder einem entfernten Zielcomputer blockiert oder entsperrt (abhängig von der verwendeten Befehlszeilenoption).

**Registrierungsschlüssel:** `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\EdgeUpdate`<br>
**Schlüsselwertname:** `DoNotUpdateToEdgeWithChromium`

| Wert                | Ergebnis                         |
|----------------------|--------------------------------|
| *Schlüssel ist nicht definiert* | Verteilung ist *nicht* blockiert. |
| 0                    | Verteilung ist *nicht* blockiert. |
| 1                    | Verteilung ist blockiert.       |

Das Skript hat folgende Befehlszeilensyntax:<br>
`EdgeChromium_Blocker.cmd [<machine name>] [/B] [/U] [/H]`

### Computername

Der Parameter `<machine name>` ist optional. Wenn er fehlt, wird die Aktion auf dem lokalen Computer ausgeführt. Andernfalls erfolgt der Zugriff auf den Remotecomputer über die Remote-Registrierungsfunktionen des Befehls `REG`. Wenn auf die Remoteregistrierung aufgrund von Sicherheitsberechtigungen nicht zugegriffen werden kann oder wenn der Remotecomputer nicht gefunden werden kann, wird vom Befehl `REG` eine Fehlermeldung zurückgegeben.

### Schalter

Die vom Skript verwendeten Schalter schließen sich gegenseitig aus, und nur der erste gültige Schalter eines bestimmten Befehls wird aktiviert. Das Skript kann mehrmals auf demselben Computer ausgeführt werden.

| Schalter       | Beschreibung                              |
|--------------|------------------------------------------|
| `/B`         | Verteilung wird blockiert                      |
| `/U`         | Blockierung der Verteilung wird aufgehoben                    |
| `/H` oder `/?` | Zeigt die folgende Zusammenfassung für Hilfe an:<br>`This tool can be used to remotely block or unblock the delivery of Microsoft Edge (Chromium-based) through Automatic Updates.`<br> `Usage:`<br>`EdgeChromium_Blocker.cmd [<machine name>] [/B][/U][/H]`<br>`B = Block Microsoft Edge (Chromium-based) deployment`<br>`U = Allow Microsoft Edge (Chromium-based) deployment`<br>`H = Help`<br>`Examples:`<br>`EdgeChromium_Blocker.cmd mymachine /B (blocks delivery on machine "mymachine")`<br>`EdgeChromium_Blocker.cmd /U (unblocks delivery on the local machine)`<br> |

## Administrative Vorlage für Gruppenrichtlinien (.ADMX- und .ADML-Dateien)

Die Verwaltungsvorlage für Gruppenrichtlinien (.ADMX- und .ADML-Dateien) ermöglicht es Administratoren, die neuen Gruppenrichtlinieneinstellungen zu importieren, um die automatische Bereitstellung von Microsoft Edge (Chromium-basiert) in ihrer Gruppenrichtlinienumgebung zu blockieren oder freizugeben. Administratoren können mit der Gruppenrichtlinie die Aktion in ihrer Umgebung systemübergreifend zentral ausführen.

Benutzer, die Windows 10 RS3 Enterprise/EDU und RS4 und neuer verwenden, finden die Richtlinie unter dem folgenden Pfad:

```
/Computer Configuration  
  /Administrative Templates
    /Classic Administrative Templates
      /Windows Components
        /Windows Update  
          /Microsoft Edge (Chromium-based) Blockers  
```

Diese Einstellung ist nicht pro Benutzer, sondern nur als Computereinstellung verfügbar.

> [!IMPORTANT]
> Diese Registrierungseinstellung wird nicht in einem Richtlinienschlüssel gespeichert und gilt als *Präferenz*. Somit bleibt die Einstellung erhalten, wenn das Gruppenrichtlinienobjekt, das die Einstellung implementiert, entfernt oder die Richtlinie auf **nicht konfiguriert**festgelegt wird. Um die Verteilung von Microsoft Edge (Chromium-basiert) über die Gruppenrichtlinie freizugeben, legen Sie die Richtlinie auf **Deaktiviert** fest.

## Weitere Informationen

- [Microsoft Edge Enterprise-Angebotsseite](https://www.microsoftedgeinsider.com/enterprise)
- [Windows-Updates zur Unterstützung von Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-sysupdate-windows-updates)
- [Zugreifen auf die alte Version von Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-sysupdate-access-old-edge)
