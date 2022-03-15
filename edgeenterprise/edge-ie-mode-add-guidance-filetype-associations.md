---
title: Zuordnen von Dateierweiterungen zum Internet Explorer-Modus
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 02/24/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Zuordnen von Dateierweiterungen zum Internet Explorer-Modus
ms.openlocfilehash: 1d25baa224e4fdcdd76bd599ccedb807c9dd7061
ms.sourcegitcommit: 556aca8dde42dd66364427f095e8e473b86651a0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2022
ms.locfileid: "12445750"
---
# <a name="associate-file-extensions-with-internet-explorer-mode"></a>Zuordnen von Dateierweiterungen zum Internet Explorer-Modus

>[!Note]
> Die Internet Explorer 11-Desktopanwendung wird eingestellt und wird am 15. Juni 2022 nicht mehr unterstützt. Lesen Sie [diese häufig gestellten Fragen](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549), um eine Liste der Bereiche anzuzeigen. Dieselben IE11-Apps und -Websites, die Sie heute verwenden, können in Microsoft Edge im Internet Explorer-Modus geöffnet werden. [Weitere Informationen finden Sie hier](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/).

In diesem Artikel wird erläutert, wie Sie Microsoft Edge mit dem Internet Explorer-Modus mit Dateierweiterungen für Desktopanwendungen verknüpfen.

> [!NOTE]
> Dieser Artikel bezieht sich auf Microsoft Edge Version 86 oder höher.

## <a name="guidance-for-file-extension-association-with-internet-explorer-mode"></a>Leitfaden zur Dateierweiterungszuordnung im Internet Explorer-Modus

Die folgenden Anweisungen zeigen einen Eintrag, der Microsoft Edge dem IE-Modus dem Dateityp \.mht zuweist. Führen Sie die folgenden Schritte aus, um eine Dateizuordnung festzulegen.

> [!NOTE]
> Sie können festlegen, dass bestimmte Dateierweiterungen standardmäßig im Internet Explorer-Modus geöffnet werden, indem Sie die Richtlinie zum **Festlegen einer Konfigurationsdatei für Standardzuordnungen** verwenden. Weitere Informationen finden Sie unter [Policy CSP-ApplicationDefaults](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration).

1. Definieren Sie eine neue ProgID mit dem Microsoft Edge-Kanal, die zum Öffnen im Internet Explorer-Modus verwendet werden soll. Die ProgID enthält den Namen und das Symbol der Anwendung sowie den vollständigen Pfad zu msedge.exe.

```markdown
[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\Application]
"ApplicationCompany"="Microsoft Corporation"
"ApplicationName"="Microsoft Edge with IE Mode"
"ApplicationIcon"="C:\\<edge_installation_dir>\\msedge.exe,0"
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

3. Ordnen Sie schließlich die Dateierweiterung \.mht einer neuen ProgID zu. Fügen Sie Ihre ProgID als Wertnamen mit dem Werttyp REG_SZ hinzu.

```markdown
[HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\FileExts\.mht\OpenWithProgids]
"MSEdgeIEModeMHT"=hex(0):
```

Nachdem Sie die im vorherigen Beispiel beschriebenen Schlüssel festgelegt haben, wird Ihren Benutzern im Menü **"Öffnen mit**" eine weitere Option zum Öffnen einer \.mht-Datei mit Microsoft Edge \<channel\> im IE-Modus angezeigt.

## <a name="registry-example"></a>Registrierungsbeispiel

Sie können den folgenden Codeausschnitt als Registrierungsdatei speichern und in die Registrierung importieren.

```markdown
Windows Registry Editor Version 5.00

[HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\FileExts\.mht\OpenWithProgids]
"MSEdgeIEModeMHT"=hex(0):

[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT]

[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\Application]
"ApplicationCompany"="Microsoft Corporation"
"ApplicationName"="Microsoft Edge with IE Mode"
"ApplicationIcon"="C:\\<edge_installation_dir>\\msedge.exe,0"
"AppUserModelId"=""

[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\DefaultIcon]
@="C:\\<edge_installation_dir>\\msedge.exe,4"

[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\shell]

[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\shell\open]

[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\shell\open\command]
@="\"C:\\<edge_installation_dir>\\msedge.exe\" -ie-mode-file-url -- \"%1\""

```

## <a name="configuring-file-types-to-open-in-internet-explorer-mode"></a>Konfigurieren von Dateitypen zum Öffnen im Internet Explorer-Modus

Ab Microsoft Edge 88 können Sie bestimmte Dateityplinks so konfigurieren, dass sie im Internet Explorer-Modus geöffnet werden. Verwenden Sie dazu das [Kontextmenü "Richtlinie anzeigen", um Links im Internet Explorer-Modus zu öffnen](./microsoft-edge-policies.md#internetexplorerintegrationreloadiniemodeallowed).

Sie können festlegen, für welche Dateitypen diese Option gelten soll, indem Sie Dateierweiterungen in der Richtlinie [Dateierweiterungs-Zulassungsliste zum Öffnen von lokalen Dateien im Internet Explorer-Modus](./microsoft-edge-policies.md#internetexplorerintegrationlocalfileextensionallowlist) angeben. 

## <a name="see-also"></a>Weitere Informationen

- [Informationen zum IE-Modus](./edge-ie-mode.md)
- [Informationen zu konfigurierbaren Websites](./edge-learnmore-configurable-sites-ie-mode.md)
- [Weitere Informationen zum Unternehmensmodus](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [Festlegen von Dateitypzuordnungen](/windows/win32/shell/fa-file-types)
- [Angebotsseite für Microsoft Edge für Unternehmen](https://aka.ms/EdgeEnterprise)