---
title: Hinzufügen des Internet Explorer-Modus zum Kontextmenü „Öffnen mit“
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 11/13/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Hinzufügen des Internet Explorer-Modus zum Kontextmenü „Öffnen mit“
ms.openlocfilehash: 6453cd2587e3bec10404d2491914debb999fcf3f
ms.sourcegitcommit: e3c80274a9b8ef15761c968214b3cba593476132
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/13/2020
ms.locfileid: "11168485"
---
# <span data-ttu-id="2250e-103">Hinzufügen des Internet Explorer-Modus zum Kontextmenü „Öffnen mit“</span><span class="sxs-lookup"><span data-stu-id="2250e-103">Add Internet Explorer mode to the "Open with" context menu</span></span>

<span data-ttu-id="2250e-104">In diesem Artikel wird erläutert, wie Sie Microsoft Edge mit dem Internet Explorer-Modus mit Dateierweiterungen für Desktopanwendungen verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="2250e-104">This article explains how to associate Microsoft Edge with Internet Explorer mode with file extensions for desktop applications.</span></span>

> [!NOTE]
> <span data-ttu-id="2250e-105">Dieser Artikel bezieht sich auf Microsoft Edge Version 86 oder höher.</span><span class="sxs-lookup"><span data-stu-id="2250e-105">This article applies to Microsoft Edge version 86 or later.</span></span>

## <span data-ttu-id="2250e-106">Leitfaden zur Dateierweiterungszuordnung im Internet Explorer-Modus</span><span class="sxs-lookup"><span data-stu-id="2250e-106">Guidance for file extension association with Internet Explorer mode</span></span>

<span data-ttu-id="2250e-107">Die folgenden Anweisungen zeigen einen Eintrag, der dem Dateityp MHT den Modus Microsoft Edge mit IE zuordnet.</span><span class="sxs-lookup"><span data-stu-id="2250e-107">The following instructions show an entry that associates Microsoft Edge with IE mode with the .mht file type.</span></span> <span data-ttu-id="2250e-108">Führen Sie die folgenden Schritte aus, um eine Dateizuordnung festzulegen.</span><span class="sxs-lookup"><span data-stu-id="2250e-108">Use the following steps as a guide for setting a file association.</span></span>

> [!NOTE]
> <span data-ttu-id="2250e-109">Sie können festlegen, dass bestimmte Dateierweiterungen standardmäßig im Internet Explorer-Modus geöffnet werden, indem Sie die Richtlinie zum **Festlegen einer Konfigurationsdatei für Standardzuordnungen** verwenden.</span><span class="sxs-lookup"><span data-stu-id="2250e-109">You can set specific file extensions to open in Internet Explorer mode by default using the policy to **Set a default associations configuration file**.</span></span> <span data-ttu-id="2250e-110">Weitere Informationen finden Sie unter [Policy CSP-ApplicationDefaults](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration).</span><span class="sxs-lookup"><span data-stu-id="2250e-110">For more information, see [Policy CSP - ApplicationDefaults](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration).</span></span>

1. <span data-ttu-id="2250e-111">Definieren Sie eine neue ProgID mit dem Microsoft Edge-Kanal, die zum Öffnen im Internet Explorer-Modus verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2250e-111">Define a new ProgID with the Microsoft Edge channel to use to open with Internet Explorer mode.</span></span> <span data-ttu-id="2250e-112">Die ProgID enthält den Namen und das Symbol der Anwendung sowie den vollständigen Pfad zu msedge.exe.</span><span class="sxs-lookup"><span data-stu-id="2250e-112">The ProgID includes the application name and Icon and the full path to msedge.exe.</span></span>

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

2. <span data-ttu-id="2250e-113">Konfigurieren Sie Shell-Updates, um die Befehlszeile zu übergeben, die zum Öffnen mit dem IE-Modus erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="2250e-113">Configure shell updates to pass the command line needed to open with IE mode.</span></span>

```markdown
[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\shell\open\command]
@="\"C:\\<edge_installation_dir>\\msedge.exe\" -ie-mode-file-url -- \"%1\""
```

3. <span data-ttu-id="2250e-114">Ordnen Sie schließlich die MHT-Dateierweiterung einer neuen ProgID zu.</span><span class="sxs-lookup"><span data-stu-id="2250e-114">Finally, associate the .mht file extension with a new ProgID.</span></span> <span data-ttu-id="2250e-115">Fügen Sie Ihre ProgID als Wertnamen mit dem Werttyp REG_SZ hinzu.</span><span class="sxs-lookup"><span data-stu-id="2250e-115">Add your ProgID as a value name, with the value type of REG_SZ.</span></span>

```markdown
[HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\FileExts\.mht\OpenWithProgids]
"MSEdgeIEModeMHT"=hex(0):
```

<span data-ttu-id="2250e-116">Nachdem Sie die im vorherigen Beispiel beschriebenen Schlüssel festgelegt haben, wird Ihren Benutzern eine zusätzliche Option im Menü **Öffnen mit** angezeigt, um eine MHT-Datei mit dem Modus Microsoft Edge \<channel\> mit IE zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="2250e-116">After you set the keys described in the previous example, your users will see an additional option on the **Open with** menu to open an .mht file using Microsoft Edge \<channel\> with IE mode.</span></span>

## <span data-ttu-id="2250e-117">Registrierungsbeispiel</span><span class="sxs-lookup"><span data-stu-id="2250e-117">Registry Example</span></span>

<span data-ttu-id="2250e-118">Sie können den folgenden Codeausschnitt als Registrierungsdatei speichern und in die Registrierung importieren.</span><span class="sxs-lookup"><span data-stu-id="2250e-118">You can save the following code snippet as a .reg file and import it into the registry.</span></span>

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

## <span data-ttu-id="2250e-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2250e-119">See also</span></span>

- [<span data-ttu-id="2250e-120">Informationen zum IE-Modus</span><span class="sxs-lookup"><span data-stu-id="2250e-120">About IE mode</span></span>](https://docs.microsoft.com/deployedge/edge-ie-mode)
- [<span data-ttu-id="2250e-121">Informationen zu konfigurierbaren Websites</span><span class="sxs-lookup"><span data-stu-id="2250e-121">Configurable sites information</span></span>](https://docs.microsoft.com/deployedge/edge-learnmore-configurable-sites-ie-mode)
- [<span data-ttu-id="2250e-122">Weitere Informationen zum Unternehmensmodus</span><span class="sxs-lookup"><span data-stu-id="2250e-122">Additional Enterprise Mode information</span></span>](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [<span data-ttu-id="2250e-123">Festlegen von Dateitypzuordnungen</span><span class="sxs-lookup"><span data-stu-id="2250e-123">Setting file type associations</span></span>](https://docs.microsoft.com/windows/win32/shell/fa-file-types)
- [<span data-ttu-id="2250e-124">Angebotsseite für Microsoft Edge für Unternehmen</span><span class="sxs-lookup"><span data-stu-id="2250e-124">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
