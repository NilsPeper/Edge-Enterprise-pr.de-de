---
title: Zuordnen von Dateierweiterungen zum Internet Explorer-Modus
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 05/19/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Zuordnen von Dateierweiterungen zum Internet Explorer-Modus
ms.openlocfilehash: c027b11e426cd665cb9e6cc25b4c9f66a0c6762a
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2021
ms.locfileid: "11617455"
---
# <a name="associate-file-extensions-with-internet-explorer-mode"></a><span data-ttu-id="3cca8-103">Zuordnen von Dateierweiterungen zum Internet Explorer-Modus</span><span class="sxs-lookup"><span data-stu-id="3cca8-103">Associate file extensions with Internet Explorer mode</span></span>

>[!Note]
> <span data-ttu-id="3cca8-104">Die Internet Explorer 11-Desktopanwendung wird eingestellt und wird ab dem 15. Juni 2022 nicht mehr unterstützt (eine Liste der in diesem Bereich enthaltenen Elemente [finden Sie in den FAQ](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549)).</span><span class="sxs-lookup"><span data-stu-id="3cca8-104">The Internet Explorer 11 desktop application will be retired and go out of support on June 15, 2022 (for a list of what’s in scope, [see the FAQ](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549)).</span></span> <span data-ttu-id="3cca8-105">Dieselben IE11-Apps und -Websites, die Sie heute verwenden, können in Microsoft Edge im Internet Explorer-Modus geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="3cca8-105">The same IE11 apps and sites you use today can open in Microsoft Edge with Internet Explorer mode.</span></span> <span data-ttu-id="3cca8-106">[Weitere Informationen finden Sie hier](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/).</span><span class="sxs-lookup"><span data-stu-id="3cca8-106">[Learn more here](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/).</span></span>

<span data-ttu-id="3cca8-107">In diesem Artikel wird erläutert, wie Sie Microsoft Edge mit dem Internet Explorer-Modus mit Dateierweiterungen für Desktopanwendungen verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="3cca8-107">This article explains how to associate Microsoft Edge with Internet Explorer mode with file extensions for desktop applications.</span></span>

> [!NOTE]
> <span data-ttu-id="3cca8-108">Dieser Artikel bezieht sich auf Microsoft Edge Version 86 oder höher.</span><span class="sxs-lookup"><span data-stu-id="3cca8-108">This article applies to Microsoft Edge version 86 or later.</span></span>

## <a name="guidance-for-file-extension-association-with-internet-explorer-mode"></a><span data-ttu-id="3cca8-109">Leitfaden zur Dateierweiterungszuordnung im Internet Explorer-Modus</span><span class="sxs-lookup"><span data-stu-id="3cca8-109">Guidance for file extension association with Internet Explorer mode</span></span>

<span data-ttu-id="3cca8-110">Die folgenden Anweisungen zeigen einen Eintrag, der dem Dateityp MHT den Modus Microsoft Edge mit IE zuordnet.</span><span class="sxs-lookup"><span data-stu-id="3cca8-110">The following instructions show an entry that associates Microsoft Edge with IE mode with the .mht file type.</span></span> <span data-ttu-id="3cca8-111">Führen Sie die folgenden Schritte aus, um eine Dateizuordnung festzulegen.</span><span class="sxs-lookup"><span data-stu-id="3cca8-111">Use the following steps as a guide for setting a file association.</span></span>

> [!NOTE]
> <span data-ttu-id="3cca8-112">Sie können festlegen, dass bestimmte Dateierweiterungen standardmäßig im Internet Explorer-Modus geöffnet werden, indem Sie die Richtlinie zum **Festlegen einer Konfigurationsdatei für Standardzuordnungen** verwenden.</span><span class="sxs-lookup"><span data-stu-id="3cca8-112">You can set specific file extensions to open in Internet Explorer mode by default using the policy to **Set a default associations configuration file**.</span></span> <span data-ttu-id="3cca8-113">Weitere Informationen finden Sie unter [Policy CSP-ApplicationDefaults](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration).</span><span class="sxs-lookup"><span data-stu-id="3cca8-113">For more information, see [Policy CSP - ApplicationDefaults](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration).</span></span>

1. <span data-ttu-id="3cca8-114">Definieren Sie eine neue ProgID mit dem Microsoft Edge-Kanal, die zum Öffnen im Internet Explorer-Modus verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3cca8-114">Define a new ProgID with the Microsoft Edge channel to use to open with Internet Explorer mode.</span></span> <span data-ttu-id="3cca8-115">Die ProgID enthält den Namen und das Symbol der Anwendung sowie den vollständigen Pfad zu msedge.exe.</span><span class="sxs-lookup"><span data-stu-id="3cca8-115">The ProgID includes the application name and Icon and the full path to msedge.exe.</span></span>

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

2. <span data-ttu-id="3cca8-116">Konfigurieren Sie Shell-Updates, um die Befehlszeile zu übergeben, die zum Öffnen mit dem IE-Modus erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="3cca8-116">Configure shell updates to pass the command line needed to open with IE mode.</span></span>

```markdown
[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\shell\open\command]
@="\"C:\\<edge_installation_dir>\\msedge.exe\" -ie-mode-file-url -- \"%1\""
```

3. <span data-ttu-id="3cca8-117">Ordnen Sie schließlich die MHT-Dateierweiterung einer neuen ProgID zu.</span><span class="sxs-lookup"><span data-stu-id="3cca8-117">Finally, associate the .mht file extension with a new ProgID.</span></span> <span data-ttu-id="3cca8-118">Fügen Sie Ihre ProgID als Wertnamen mit dem Werttyp REG_SZ hinzu.</span><span class="sxs-lookup"><span data-stu-id="3cca8-118">Add your ProgID as a value name, with the value type of REG_SZ.</span></span>

```markdown
[HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\FileExts\.mht\OpenWithProgids]
"MSEdgeIEModeMHT"=hex(0):
```

<span data-ttu-id="3cca8-119">Nachdem Sie die im vorherigen Beispiel beschriebenen Schlüssel festgelegt haben, wird Ihren Benutzern eine zusätzliche Option im Menü **Öffnen mit** angezeigt, um eine MHT-Datei mit dem Modus Microsoft Edge \<channel\> mit IE zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="3cca8-119">After you set the keys described in the previous example, your users will see an additional option on the **Open with** menu to open an .mht file using Microsoft Edge \<channel\> with IE mode.</span></span>

## <a name="registry-example"></a><span data-ttu-id="3cca8-120">Registrierungsbeispiel</span><span class="sxs-lookup"><span data-stu-id="3cca8-120">Registry Example</span></span>

<span data-ttu-id="3cca8-121">Sie können den folgenden Codeausschnitt als Registrierungsdatei speichern und in die Registrierung importieren.</span><span class="sxs-lookup"><span data-stu-id="3cca8-121">You can save the following code snippet as a .reg file and import it into the registry.</span></span>

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

## <a name="configuring-file-types-to-open-in-internet-explorer-mode"></a><span data-ttu-id="3cca8-122">Konfigurieren von Dateitypen zum Öffnen im Internet Explorer-Modus</span><span class="sxs-lookup"><span data-stu-id="3cca8-122">Configuring file types to open in Internet Explorer mode</span></span>

<span data-ttu-id="3cca8-123">Ab Microsoft Edge 88 können Sie mit der Richtlinie [Kontextmenü zum Öffnen von Links im Internet Explorer-Modus anzeigen](./microsoft-edge-policies.md#internetexplorerintegrationreloadiniemodeallowed) bestimmte Links zur Dateitypen so konfigurieren, dass sie im Internet Explorer-Modus geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="3cca8-123">Starting Edge 88, you can configure specific file type links to open in Internet Explorer mode using the policy [Show context menu to open links in Internet Explorer mode](./microsoft-edge-policies.md#internetexplorerintegrationreloadiniemodeallowed).</span></span>

<span data-ttu-id="3cca8-124">Sie können festlegen, für welche Dateitypen diese Option gelten soll, indem Sie Dateierweiterungen in der Richtlinie [Dateierweiterungs-Zulassungsliste zum Öffnen von lokalen Dateien im Internet Explorer-Modus](./microsoft-edge-policies.md#internetexplorerintegrationlocalfileextensionallowlist) angeben.</span><span class="sxs-lookup"><span data-stu-id="3cca8-124">You can define file types this option should apply to, by specifying file extensions in this policy [Open local files in Internet Explorer mode file extension allow list](./microsoft-edge-policies.md#internetexplorerintegrationlocalfileextensionallowlist).</span></span> 

## <a name="see-also"></a><span data-ttu-id="3cca8-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3cca8-125">See also</span></span>

- [<span data-ttu-id="3cca8-126">Informationen zum IE-Modus</span><span class="sxs-lookup"><span data-stu-id="3cca8-126">About IE mode</span></span>](./edge-ie-mode.md)
- [<span data-ttu-id="3cca8-127">Informationen zu konfigurierbaren Websites</span><span class="sxs-lookup"><span data-stu-id="3cca8-127">Configurable sites information</span></span>](./edge-learnmore-configurable-sites-ie-mode.md)
- [<span data-ttu-id="3cca8-128">Weitere Informationen zum Unternehmensmodus</span><span class="sxs-lookup"><span data-stu-id="3cca8-128">Additional Enterprise Mode information</span></span>](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [<span data-ttu-id="3cca8-129">Festlegen von Dateitypzuordnungen</span><span class="sxs-lookup"><span data-stu-id="3cca8-129">Setting file type associations</span></span>](/windows/win32/shell/fa-file-types)
- [<span data-ttu-id="3cca8-130">Angebotsseite für Microsoft Edge für Unternehmen</span><span class="sxs-lookup"><span data-stu-id="3cca8-130">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)