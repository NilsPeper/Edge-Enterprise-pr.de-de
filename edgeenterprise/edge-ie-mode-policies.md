---
title: Konfigurieren von Richtlinien für den IE-Modus
ms.author: cjacks
author: cjacks
manager: saudm
ms.date: 03/25/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Konfigurieren von Richtlinien für den IE-Modus
ms.openlocfilehash: 2d2ded3a3fb338bdf2d815d681b52249007945ac
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979940"
---
# Konfigurieren von Richtlinien für den IE-Modus

In diesem Artikel wird erläutert, wie Sie Richtlinien für den IE-Modus konfiguriert werden.

> [!NOTE]
> Dieser Artikel bezieht sich auf die Microsoft Edge-Kanäle **Stable**, **Beta** und **Dev**, Version 77 oder höher.

Zum Konfigurieren des IE-Modus sind drei Schritte erforderlich:

1. [Konfigurieren der Internet Explorer-Integration](#configure-internet-explorer-integration)
2. [Umleiten von Websites von Microsoft Edge in den IE-Modus](#redirect-sites-from-microsoft-edge-to-ie-mode)
3. (Optional) [Umleiten von Websites von Internet Explorer zu Microsoft Edge](#redirect-sites-from-ie-to-microsoft-edge)

> [!NOTE]
> Richtlinien zum Aktivieren des IE-Modus können über Intune konfiguriert werden. Weitere Informationen finden Sie unter [Microsoft Edge zu Microsoft Intune hinzufügen](https://docs.microsoft.com/intune/apps/apps-windows-edge?toc=https://docs.microsoft.com/DeployEdge/toc.json&bc=https://docs.microsoft.com/DeployEdge/breadcrumb/toc.json) und [Microsoft Edge-Richtlinien mit Microsoft Intune konfigurieren](https://docs.microsoft.com/DeployEdge/configure-edge-with-intune).

## Konfigurieren der Internet Explorer-Integration

Sie können Internet Explorer so konfigurieren, dass er direkt in Microsoft Edge (IE-Modus) geöffnet wird. Sie können Internet Explorer auch so konfigurieren, dass er in einem eigenen Internet Explorer 11-Fenster geöffnet wird. Die meisten Benutzer bevorzugen es, wenn Websites direkt in Microsoft Edge im IE-Modus geöffnet werden.

### Aktivieren der Internet Explorer-Integration mithilfe einer Gruppenrichtlinie

1. Laden Sie die aktuelle [Microsoft Edge-Richtlinienvorlage](https://www.microsoft.com/en-us/edge/business/download) herunter, und verwenden Sie sie.
2. Öffnen Sie den Gruppenrichtlinien-Editor.
3. Klicken Sie auf **Computerkonfiguration** > **Administrative Vorlagen** > **Microsoft Edge**.
4. Doppelklicken Sie auf **Internet Explorer-Integration konfigurieren**.
5. Wählen Sie **Aktiviert** aus.
6. Setzen Sie unter **Optionen**den Dropdown-Wert auf 
   -  **Internet Explorer-Modus**, wenn Sie möchten, dass Websites in Microsoft Edge im IE-Modus geöffnet werden.
   -  **Internet Explorer 11**, wenn Sie möchten, dass Websites in einem eigenständigen Fenster von Internet Explorer 11 geöffnet werden.
   -  **Keines**, falls Sie Benutzer an der Konfiguration des Internet Explorer-Modus über "edge://flags" oder über Befehlszeilenoptionen hindern möchten.

   > [!NOTE]
   > Das Festlegen der Richtlinie auf **Deaktiviert** impliziert, dass der IE-Modus durch die Richtlinie deaktiviert ist, aber über dge://flags oder Befehlszeilenoptionen festgelegt werden kann.
7. Klicken Sie auf **OK** oder **Übernehmen**, um diese Richtlinieneinstellung zu speichern.

## Umleiten von Websites von Microsoft Edge in den IE-Modus

Es gibt zwei Möglichkeiten, um zu bestimmen, welche Websites im IE-Modus geöffnet werden sollen:

- (Empfohlen) [Konfigurieren von Websites in der Enterprise Mode-Siteliste](#configure-sites-on-the-enterprise-site-list)
- [Konfigurieren aller Intranetsites](#configure-all-intranet-sites)

### Konfigurieren von Websites in der Enterprise Mode-Siteliste

Mithilfe der folgenden Gruppenrichtlinien können Sie bestimmte Websites so konfigurieren, dass sie im IE-Modus geöffnet werden:

- Die [Websiteliste für den Unternehmensmodus-IE verwenden](#configure-using-the-use-the-enterprise-mode-ie-website-list-policy) (Internet Explorer)
- [Enterprise Mode Site List konfigurieren](#configure-using-the-configure-the-enterprise-mode-site-list-policy) (Microsoft Edge, Version 78 oder höher)<br/>Mithilfe dieser Richtlinie können Sie eine separate Enterprise Mode Site List für Microsoft Edge erstellen. Durch das Aktivieren dieser Richtlinie werden die Einstellungen in der Richtlinie "Die Websiteliste für den Unternehmensmodus-IE verwenden" außer Kraft gesetzt, wenn die Option "Integrationsrichtlinie für Internet Explorer konfigurieren" aktiviert ist. Das Deaktivieren oder Nichtkonfigurieren dieser Richtlinie wirkt sich nicht auf das Standardverhalten der Richtlinie „Internet Explorer-Integration konfigurieren” aus.
    > [!NOTE]
    > Die Konfiguration der Microsoft Edge-Richtlinie ist nicht zwingend erforderlich. Viele Organisationen verwenden dies als Überschreibung, sodass sie mit der IE-Richtlinie die aktuelle Websiteliste auf alle Benutzer ausrichten können und eine aktualisierte Version leichter auf Pilotverwendungen mit der Microsoft Edge-Richtlinie ausrichten können.

Weitere Informationen zu Enterprise Mode-Siteliste finden Sie unter:

- [Verwenden des Enterprise Mode Site List Manager](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/use-the-enterprise-mode-site-list-manager)
- [Hinzufügen mehrerer Websites zur Websiteliste für den Unternehmensmodus unter Verwendung einer Datei und von Enterprise Mode Site List Manager (Schema V.2)](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/add-multiple-sites-to-enterprise-mode-site-list-using-the-version-2-schema-and-enterprise-mode-tool).

### Konfigurieren mithilfe der Richtlinie "Die Websiteliste für den Unternehmensmodus-IE verwenden":

Der IE-Modus kann die bestehende Richtlinie zur Konfiguration der Enterprise Site List für Internet Explorer verwenden, sodass Sie nur eine einzige Liste erstellen und pflegen müssen.

1. Erstellen oder erneutes Verwenden einer Site List im XML-Format
    1. Alle Websites mit dem Element _\<open-in\>IE11\</open-in\>_ werden jetzt im IE-Modus geöffnet.
2. Öffnen Sie den Gruppenrichtlinien-Editor.
3. Klicken Sie auf **Computerkonfiguration** > **Administrative Vorlagen** > **Windows-Komponenten** > **Internet Explorer**
4. Doppelklicken Sie auf **Die Websiteliste für den Unternehmensmodus-IE verwenden**.
5. Wählen Sie **Aktiviert** aus.
6. Geben Sie unter **Optionen** den Speicherort der Websiteliste ein. Sie können einen der folgenden Speicherorte verwenden:
    - (Empfohlen) HTTPS-Speicherort: **https**:**//iemode/sites.xml**
    - Datei im lokalen Netzwerk: **\\\network\shares\sites.xml**
    - Lokale Datei: **file:///c:/Users/\<user\>/Documents/sites.xml**
7. Klicken Sie auf **OK** oder **Übernehmen**, um die Einstellungen zu speichern.

### Konfiguration mithilfe der Richtlinie "Enterprise Mode Site List konfigurieren":

Sie können den IE-Modus auch mit einer separaten Richtlinie für Microsoft Edge konfigurieren. Diese zusätzliche Richtlinie ermöglicht es Ihnen, die IE-Websiteliste außer Kraft zu setzen. In einigen Organisationen wird die beispielsweise Produktionswebsiteliste auf alle Benutzer ausgerichtet. Sie können die Pilotwebsiteliste dann mithilfe dieser Richtlinie für eine kleine Gruppe von Benutzern bereitstellen.

1. Erstellen oder erneutes Verwenden einer Site List im XML-Format
    1. Alle Websites mit dem Element _\<open-in\>IE11\</open-in\>_ werden jetzt im IE-Modus geöffnet.
2. Öffnen Sie den Gruppenrichtlinien-Editor.
3. Klicken Sie auf **Computerkonfiguration** > **Administrative Vorlagen** > **Microsoft Edge**.
4. Doppelklicken Sie auf **Enterprise Mode-Siteliste konfigurieren**.
5. Wählen Sie **Aktiviert** aus.
6. Geben Sie unter **Optionen** den Speicherort der Websiteliste ein. Sie können einen der folgenden Speicherorte verwenden:
    - (Empfohlen) HTTPS-Speicherort: **https**:**//iemode/sites.xml** <!--Trying to keep this from being an active link in MD -->
    - Datei im lokalen Netzwerk: **\\\network\shares\sites.xml**
    - Lokale Datei: **file:///c:/Users/\<user\>/Documents/sites.xml**
7. Klicken Sie auf **OK** oder **Übernehmen**, um die Einstellungen zu speichern.

### Konfigurieren aller Intranetsites

Der IE-Modus kann so konfiguriert werden, dass er für alle Websites in der lokalen Intranetzone verwendet wird. Mit einer Enterprise Mode Site List können Sie einzelne Websites aus dem IE-Modus entfernen.

>[!NOTE]
>
> Die lokale Intranetzone enthält explizit hinzugefügte Websites, weist dieser Zone aber auch Websites mit Hilfe von Heuristiken zu. Dazu können Hostnamen ohne Punkt gehören (z.B. **https**:**//payroll**) und Websites, die vom Proxykonfigurationsskript konfiguriert werden, um den Proxy zu umgehen. Wenn eine externe Partei den DNS oder Proxy steuert, kann sie potenziell erzwingen, dass Websites den IE-Modus verwenden.

1. Öffnen Sie den lokalen Gruppenrichtlinien-Editor.
2. Klicken Sie auf **Computerkonfiguration** > **Administrative Vorlagen** > **Microsoft Edge**.
3. Doppelklicken Sie auf **Alle Intranetsites an Internet Explorer senden**.
4. Wählen Sie **Aktiviert** aus, und klicken Sie dann auf **OK** oder **Übernehmen**, um die Richtlinieneinstellungen zu speichern.

## Umleiten von Websites von Internet Explorer zu Microsoft Edge

Sie können verhindern, dass Ihre Benutzer Internet Explorer für Websites verwenden, die ihn nicht benötigen. Internet Explorer kann Websites, die sich nicht in Ihrer Websiteliste befinden, automatisch zu Microsoft Edge umleiten.

1. Öffnen Sie den Gruppenrichtlinien-Editor.
2. Klicken Sie auf **Computerkonfiguration** > **Administrative Tools** > **Windows-Komponenten** > **Internet Explorer**.
3. Doppelklicken Sie auf **Senden aller nicht in der Websiteliste für den Unternehmensmodus enthaltenen Websites an Microsoft Edge**.
4. Wählen Sie **Aktiviert** aus.
5. Klicken Sie auf **OK** oder **Übernehmen**, um die Einstellungen zu speichern.
6. Doppelklicken Sie auf **Konfigurieren, welcher Microsoft Edge-Kanal zum Öffnen von umgeleiteten Websites verwendet wird**.
7. Wählen Sie **Aktiviert** aus.
8. Wählen Sie unter **Optionen** die drei wichtigsten Optionen aus, die der Kanal verwenden soll. Internet Explorer führt eine Umleitung auf die am höchsten bewertete Option aus, die der Benutzer auf dem jeweiligen Gerät installiert hat:
   - Microsoft Edge Stable
   - Microsoft Edge Beta, Version 77 oder höher
   - Microsoft Edge Dev, Version 77 oder höher
   - Microsoft Edge Canary, Version 77 oder höher
   - Microsoft Edge, Version 45 oder früher
9. Klicken Sie auf **OK** oder **Übernehmen**, um die Einstellungen zu speichern.

## Weitere Informationen

- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)
- [Informationen zum IE-Modus](https://docs.microsoft.com/deployedge/edge-ie-mode)
- [Weitere Informationen zum Unternehmensmodus](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)