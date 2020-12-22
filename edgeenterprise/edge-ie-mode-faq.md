---
title: FAQ zum IE-Modus
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 12/21/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: FAQ und Problembehandlung für Microsoft Edge mit IE-Modus
ms.openlocfilehash: 62bf8afc5ac908e18d2f503fa9248a19f78fd6f6
ms.sourcegitcommit: 306582403d4272831bcac390154c7cc7041a9b7e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/21/2020
ms.locfileid: "11238172"
---
# FAQ zum IE-Modus

In diesem Artikel finden Sie Tipps zur Problembehandlung und FAQ zu Microsoft Edge (Version 77 oder höher).

> [!NOTE]
> Dieser Artikel bezieht sich auf die Microsoft Edge-Kanäle **Stable**, **Beta** und **Dev**, Version 77 oder höher.

## Problembehandlung für IE-Modus

Verwenden Sie die Informationen in diesem Abschnitt, um Probleme mit dem IE-Modus zu diagnostizieren und zu beheben.

### Diagnoseinformationen zum Internet Explorer-Modus

Sie können Diagnoseinformationen für den Internet Explorer-Modus auf der Registerkarte zur Microsoft Edge-Kompatibilität abrufen. Wechseln Sie zu *edge://compat/iediagnostic*, um diese Registerkarte zu öffnen. Auf dieser Seite werden möglicherweise Diagnosemeldungen angezeigt. Auf dieser Seite finden Sie auch Konfigurationsinformationen zu den folgenden Kategorien:

- **Überprüfung des Registrierungsschlüssels**: (Wird nur angezeigt, wenn die Überprüfung fehlschlägt.) Überprüft, ob die Internet Explorer-Integration in der Registrierung ordnungsgemäß eingerichtet wurde. Wenn nicht, kann der Benutzer auf **Beheben** klicken, um das Problem zu beheben.
- **Internet Explorer-Modus**: Zeigt die verwendete API-Version an, die auf der Konfiguration und dem Betriebssystem basiert. Wenn ein Problem vorliegt, wird der Benutzer möglicherweise aufgefordert, ein **Windows Update** zu installieren.
- **Einstellung für Internet Explorer-Modus**: Zeigt an, ob und wie der Internet Explorer-Modus konfiguriert ist.
- **Befehlszeile**: Zeigt die Befehlszeilenzeichenfolge und die Schalter an, die zum Starten von Microsoft Edge verwendet werden.
- **Gruppenrichtlinieneinstellungen**: Zeigt an, ob der IE-Modus mithilfe von Gruppenrichtlinien und den angewendeten Richtlinien konfiguriert ist.

### Fehlermeldung: "Zum Öffnen dieser Seite im IE-Modus versuchen Sie, Microsoft Edge mit Administratorrechten neu zu installieren."

Diese Fehlermeldung wird möglicherweise angezeigt, wenn nicht alle erforderlichen Windows-Updates vorhanden sind. Siehe die unter [Info zum IE-Modus](https://docs.microsoft.com/deployedge/edge-ie-mode) aufgeführten Voraussetzungen für die erforderlichen Versionen von Windows und Microsoft Edge.

Diese Fehlermeldung wird möglicherweise angezeigt, wenn alle erforderlichen Windows-Updates installiert sind:

- Sie verwenden den Canary Channel, der standardmäßig auf der Benutzerebene installiert wird.
- Sie verwenden den Stable-, Beta- oder Dev-Kanal, aber bei der Aufforderung zur Rechteerweiterung während der Installation wurde die Rechteerweiterung abgebrochen. Wenn Sie die Eingabeaufforderung für erhöhte Rechte abbrechen, wird die Installation auf Benutzerebene fortgesetzt.
- Internet Explorer11 wurde in Windows-Features deaktiviert.

Mögliche Lösungen:

- Führen Sie das Installationsprogramm für einen beliebigen Kanal auf Systemebene aus: `installer.exe --system-level`
- Aktivieren Sie Internet Explorer11 in Windows-Features.

Um zu überprüfen, ob Microsoft Edge auf Systemebene installiert ist, geben Sie "edge://version" in die Adressleiste von Microsoft Edge ein. Der Pfad für die ausführbare Datei beginnt mit *C:\Programmdateien* und weist auf eine Systeminstallation hin. Wenn der Pfad der ausführbaren Datei mit *C:\Users\*, beginnt, deinstallieren Sie Microsoft Edge, und installieren Sie ihn mit Administratorrechten neu.

### Fehlermeldung: "Zum Öffnen dieser Seite im IE-Modus versuchen Sie, Microsoft Edge neu zu starten."

Dieser Fehler wird möglicherweise angezeigt, wenn in Internet Explorer ein unerwarteter Fehler aufgetreten ist. Beim Neustart von Microsoft Edge wird dieser Fehler in der Regel behoben.

### Fehlermeldung: "Deaktivieren Sie das Remotedebuggen, um diese Website im IE-Modus zu öffnen, da es sonst möglicherweise nicht wie erwartet funktioniert."

Diese Fehlermeldung wird möglicherweise angezeigt, wenn Sie Remotedebuggen durchführen und zu einer Webseite navigieren, die für die Ausführung im IE-Modus konfiguriert ist. Sie können den Vorgang fortsetzen, aber die Seite wird mit Microsoft Edge gerendert.

## Häufig gestellte Fragen

### Wird der IE-Modus Internet Explorer11 ersetzen?

Wir bemühen uns, Internet Explorer als unterstützten, zuverlässigen und sicheren Browser zu erhalten. Internet Explorer ist weiterhin eine Komponente des Windows-Betriebssystems, und verfügt daher über denselben Supportlebenszyklus wie das Betriebssystem, auf dem er installiert ist. Weitere Details finden Sie unter [Häufig gestellte Fragen zum Lebenszyklus – Internet Explorer](https://support.microsoft.com/help/17454/). Zwar unterstützt und aktualisiert Microsoft Internet Explorer weiterhin, die neuesten Features und Plattformupdates sind jedoch nur in Microsoft Edge verfügbar.

### Kann ich "Mit Explorer öffnen" oder "Im Datei-Explorer anzeigen" in SharePoint mit dem IE-Modus verwenden?

Ja, wenn dies im eigenständigen Internet Explorer 11 funktioniert, funktioniert es auch im IE-Modus. Anstatt aber die Option „Öffnen mit Explorer“ zu verwenden, besteht der empfohlene Ansatz zum Verwalten von Dateien und Ordnern außerhalb von SharePoint darin, [Ihre SharePoint-Dateien zu synchronisieren](https://support.office.com/en-us/article/sync-sharepoint-files-with-the-onedrive-sync-app-6de9ede8-5b6e-4503-80b2-6190f3354a88) oder [Dateien in SharePoint zu verschieben oder zu kopieren](https://support.office.com/en-us/article/move-or-copy-files-in-sharepoint-00e2f483-4df3-46be-a861-1f5f0c1a87bc).

### Unterstützt der IE-Modus in Microsoft Edge die von Internet Explorer 11 unterstützte Option *nomerge*?

In Microsoft Edge gibt es keine explizite Befehlszeile, die der Option *nomerge* entspricht, aber es gibt eine Reihe von Alternativen, die wir empfehlen, um diese Funktionalität bereitzustellen.

1. Verwenden Sie Profile in Microsoft Edge: Jedes Profil wird einer anderen IE-Sitzung für IE-Modus-Seiten zugeordnet. Dieses Verhalten ist also identisch mit der Option *nomerge*.
2. Verwenden Sie die Befehlszeile `--user-data-dir=<path>`, aber für jede Sitzung mit einem anderen Pfad. Bei Bedarf können Sie ein Hilfsprogramm für den Benutzer erstellen, mit dem Microsoft Edge gestartet und der Pfad für die Sitzung geändert wird.

Wenn keine der vorstehenden Optionen für Ihr Szenario geeignet ist, setzen Sie sich über einen unserer Feedbackkanäle mit uns in Verbindung: Microsoft-Support, [TechCommunity-Forum](https://techcommunity.microsoft.com/t5/enterprise/bd-p/EdgeInsiderEnterprise) oder [Microsoft Edge UserVoice](https://microsoftedge.uservoice.com/forums/928825-enterprise).

### Kann ich Links im Internet Explorer-Modus als Webseiten speichern?
 
Ja, Sie können die Option „Ziel speichern unter“ im Kontextmenü für den Internet Explorer-Modus in Microsoft Edge aktivieren. Konfigurieren Sie dazu die Gruppenrichtlinie *„‘Ziel speichern als‘ im Internet Explorer-Modus zulassen“* unter *Computer-Konfiguration > Administrative Vorlagen > Windows-Komponenten > Internet Explorer*.
Der Speichermechanismus funktioniert gleich wie in Internet Explorer, und wenn das Ziel als HTML-Datei gespeichert wird, rendert die Datei beim erneuten Öffnen die Seite in Microsoft Edge.
 
Beachten Sie, dass für diese Funktion die folgenden minimalen Updates für das Betriebssystem erforderlich sind:
- Windows 10, Version 2004, Windows Server, Version 2004, Windows 10, Version 20H2: [KB4580364](https://support.microsoft.com/help/4580364/windows-10-update-kb4580364)
- Windows 10 Version 1903, Windows 10, Version 1909, Windows Server, Version 1903 ([KB4580386](https://support.microsoft.com/help/4580386/windows-10-update-kb4580386))
- Windows 10 Version 1809, Windows Server Version 1809, Windows Server 2019 ([KB4580390](https://support.microsoft.com/help/4580390/windows-10-update-kb4580390))
- Windows 10, Version 1803: [KB4586785](https://support.microsoft.com/help/4586785/windows-10-update-kb4586785)
- Windows 10, Version 1607: [KB4586830](https://support.microsoft.com/help/4586830/windows-10-update-kb4586830)
- Windows 10, Version 1507: [KB4586787](https://support.microsoft.com/help/4586787/windows-10-update-kb4586787)


## Weitere Informationen

- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)
- [Informationen zum IE-Modus](https://docs.microsoft.com/deployedge/edge-ie-mode)
- [Weitere Informationen zum Unternehmensmodus](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
