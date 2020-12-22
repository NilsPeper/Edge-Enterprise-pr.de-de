---
title: Zuordnen von Dateierweiterungen zum Internet Explorer-Modus
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 12/21/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Zuordnen von Dateierweiterungen zum Internet Explorer-Modus
ms.openlocfilehash: 9f39a3319c3e45001090dd9f0cffb3e7ce2648fb
ms.sourcegitcommit: 306582403d4272831bcac390154c7cc7041a9b7e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/21/2020
ms.locfileid: "11238192"
---
# Zuordnen von Dateierweiterungen zum Internet Explorer-Modus

In diesem Artikel wird erläutert, wie Sie Microsoft Edge mit dem Internet Explorer-Modus mit Dateierweiterungen für Desktopanwendungen verknüpfen.

> [!NOTE]
> Dieser Artikel bezieht sich auf Microsoft Edge Version 86 oder höher.

## Leitfaden zur Dateierweiterungszuordnung im Internet Explorer-Modus

Die folgenden Anweisungen zeigen einen Eintrag, der dem Dateityp MHT den Modus Microsoft Edge mit IE zuordnet. Führen Sie die folgenden Schritte aus, um eine Dateizuordnung festzulegen.

> [!NOTE]
> Sie können festlegen, dass bestimmte Dateierweiterungen standardmäßig im Internet Explorer-Modus geöffnet werden, indem Sie die Richtlinie zum **Festlegen einer Konfigurationsdatei für Standardzuordnungen** verwenden. Weitere Informationen finden Sie unter [Policy CSP-ApplicationDefaults](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration).

1. Definieren Sie eine neue ProgID mit dem Microsoft Edge-Kanal, die zum Öffnen im Internet Explorer-Modus verwendet werden soll. Die ProgID enthält den Namen und das Symbol der Anwendung sowie den vollständigen Pfad zu msedge.exe.

```markdown
[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\Application]
"ApplicationCompany"="Microsoft Corporation"
"ApplicationName"="Microsoft Edge with IE Mode"
"ApplicationIcon"="C:\\<edge_installation_dir>\\msedge.exe,4"
"AppUserModelId"=""
```

```markdown
[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\DefaultIcon]
@="C:\\<edge_installation_dir>\\msedge.exe,4"
```

2. Konfigurieren Sie Shell-Updates, um die Befehlszeile zu übergeben, die zum Öffnen mit dem IE-Modus erforderlich ist.

```markdown
[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\shell\open\command]
@="\"C:\\<edge_installation_dir>\\msedge.exe\" -ie-mode-file-url -- \"%1\""
```

3. Ordnen Sie schließlich die MHT-Dateierweiterung einer neuen ProgID zu. Fügen Sie Ihre ProgID als Wertnamen mit dem Werttyp REG_SZ hinzu.

```markdown
[HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\FileExts\.mht\OpenWithProgids]
"MSEdgeIEModeMHT"=hex(0):
```

Nachdem Sie die im vorherigen Beispiel beschriebenen Schlüssel festgelegt haben, wird Ihren Benutzern eine zusätzliche Option im Menü **Öffnen mit** angezeigt, um eine MHT-Datei mit dem Modus Microsoft Edge \<channel\> mit IE zu öffnen.

## Registrierungsbeispiel

Sie können den folgenden Codeausschnitt als Registrierungsdatei speichern und in die Registrierung importieren.

```markdown
Windows Registry Editor Version 5.00

[HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\FileExts\.mht\OpenWithProgids]
"MSEdgeIEModeMHT"=hex(0):

[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT]

[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\Application]
"ApplicationCompany"="Microsoft Corporation"
"ApplicationName"="Microsoft Edge with IE Mode"
"ApplicationIcon"="C:\\<edge_installation_dir>\\msedge.exe,4"
"AppUserModelId"=""

[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\DefaultIcon]
@="C:\\<edge_installation_dir>\\msedge.exe,4"

[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\shell]

[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\shell\open]

[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\shell\open\command]
@="\"C:\\<edge_installation_dir>\\msedge.exe\" -ie-mode-file-url -- \"%1\""

```
## Konfigurieren von Dateitypen zum Öffnen im Internet Explorer-Modus

Ab Microsoft Edge 88 können Sie mit der Richtlinie [Kontextmenü zum Öffnen von Links im Internet Explorer-Modus anzeigen](https://docs.microsoft.com/deployedge/microsoft-edge-policies#show-context-menu-to-open-a-link-in-internet-explorer-mode) bestimmte Links zur Dateitypen so konfigurieren, dass sie im Internet Explorer-Modus geöffnet werden. 

Sie können festlegen, für welche Dateitypen diese Option gelten soll, indem Sie Dateierweiterungen in der Richtlinie [Dateierweiterungs-Zulassungsliste zum Öffnen von lokalen Dateien im Internet Explorer-Modus](https://docs.microsoft.com/deployedge/microsoft-edge-policies#internetexplorerintegrationlocalfileextensionallowlist) angeben. 

## Weitere Informationen

- [Informationen zum IE-Modus](https://docs.microsoft.com/deployedge/edge-ie-mode)
- [Informationen zu konfigurierbaren Websites](https://docs.microsoft.com/deployedge/edge-learnmore-configurable-sites-ie-mode)
- [Weitere Informationen zum Unternehmensmodus](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [Festlegen von Dateitypzuordnungen](https://docs.microsoft.com/windows/win32/shell/fa-file-types)
- [Angebotsseite für Microsoft Edge für Unternehmen](https://aka.ms/EdgeEnterprise)
