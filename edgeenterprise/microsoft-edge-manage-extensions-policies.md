---
title: Verwenden von Gruppenrichtlinien zur Verwaltung von Microsoft Edge Erweiterungen
ms.author: aspoddar
author: AndreaLBarr
manager: balajek
ms.date: 06/09/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Verwenden von Gruppenrichtlinien zur Verwaltung von Microsoft Edge Erweiterungen im Unternehmen
ms.openlocfilehash: a633b036c1733716dfb257b4711bca57bd6721f0
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2021
ms.locfileid: "11618131"
---
# <a name="use-group-policies-to-manage-microsoft-edge-extensions"></a><span data-ttu-id="0c8b2-103">Verwenden von Gruppenrichtlinien zur Verwaltung von Microsoft Edge Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="0c8b2-103">Use group policies to manage Microsoft Edge extensions</span></span>

<span data-ttu-id="0c8b2-104">In diesem Artikel werden die Optionen und Schritte zum Verwalten von Erweiterungen mithilfe von Gruppenrichtlinien beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0c8b2-104">This article describes the options and steps for managing extensions by using group policies.</span></span> <span data-ttu-id="0c8b2-105">Bei diesen Optionen wird davon ausgegangen, dass Sie bereits Microsoft Edge für Ihre Benutzer verwaltet haben.</span><span class="sxs-lookup"><span data-stu-id="0c8b2-105">These options  assume that you already have Microsoft Edge managed for your users.</span></span> <span data-ttu-id="0c8b2-106">Wenn Sie die Verwaltung von Microsoft Edge für Ihre Benutzer noch nicht eingerichtet haben, folgen Sie dem Link unten, um dies jetzt zu tun.</span><span class="sxs-lookup"><span data-stu-id="0c8b2-106">If you have not already set up Microsoft Edge to be managed for your users please follow the below link to do so now.</span></span>

- [<span data-ttu-id="0c8b2-107">Verwalten von Microsoft Edge-Erweiterungen im Unternehmen</span><span class="sxs-lookup"><span data-stu-id="0c8b2-107">Manage Microsoft Edge extensions in the enterprise</span></span>](/deployedge/microsoft-edge-manage-extensions)

> [!NOTE]
> <span data-ttu-id="0c8b2-108">Dieser Artikel bezieht sich auf Microsoft Edge Version77 oder höher.</span><span class="sxs-lookup"><span data-stu-id="0c8b2-108">This article applies to Microsoft Edge version 77 or later.</span></span>

## <a name="block-extensions-based-on-their-permissions"></a><span data-ttu-id="0c8b2-109">Blockieren von Erweiterungen basierend auf ihren Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="0c8b2-109">Block extensions based on their permissions</span></span>

<span data-ttu-id="0c8b2-110">Mithilfe der [ExtensionSettings](/deployedge/microsoft-edge-policies#extensionsettings)-Richtlinie können Sie steuern, welche Erweiterungen Ihre Benutzer basierend auf Berechtigungen installieren können.</span><span class="sxs-lookup"><span data-stu-id="0c8b2-110">You can control what extensions your users can install based on permissions using the [ExtensionSettings](/deployedge/microsoft-edge-policies#extensionsettings) policy.</span></span> <span data-ttu-id="0c8b2-111">Wenn eine installierte Erweiterung eine Berechtigung benötigt, die blockiert ist, wird sie einfach nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0c8b2-111">If an installed extension needs a permission that’s blocked, it just won't run.</span></span> <span data-ttu-id="0c8b2-112">Die Erweiterung wird nicht entfernt, nur deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="0c8b2-112">The extension isn't removed, just disabled.</span></span>

> [!NOTE]
> <span data-ttu-id="0c8b2-113">Die Einstellung für blockierte Berechtigungen kann nur innerhalb der Erweiterungseinstellungsrichtlinie festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="0c8b2-113">The blocked permissions setting can only be set within the extension settings policy.</span></span>  

<span data-ttu-id="0c8b2-114">Nutzen Sie die folgenden Schritte als Anleitung, um eine Erweiterung zu blockieren.</span><span class="sxs-lookup"><span data-stu-id="0c8b2-114">Use the following steps as a guide for blocking an extension.</span></span>

1. <span data-ttu-id="0c8b2-115">Öffnen Sie den Gruppenrichtlinienverwaltungs-Editor, wechseln Sie zu **Administrative Vorlagen > Microsoft Edge > Erweiterungen**, und wählen Sie dann **Erweiterungsverwaltungseinstellungen konfigurieren** aus.</span><span class="sxs-lookup"><span data-stu-id="0c8b2-115">Open the group policy management editor and go to **Administrative Templates > Microsoft Edge > Extensions**  and then select **Configure extension management settings**.</span></span>
2. <span data-ttu-id="0c8b2-116">Aktivieren Sie die Richtlinie, und geben Sie dann die Berechtigungen ein, die sie zulassen oder blockieren möchten, indem Sie eine JSON-Zeichenfolge verwenden, die komprimiert wird.</span><span class="sxs-lookup"><span data-stu-id="0c8b2-116">Enable the policy, then enter the permissions that you want allowed or blocked, by using a JSON string that gets compressed.</span></span> <span data-ttu-id="0c8b2-117">Der nächste Screenshot zeigt, wie Sie eine Erweiterung blockieren, die die Berechtigung „usb“ verwendet.</span><span class="sxs-lookup"><span data-stu-id="0c8b2-117">The next screenshot shows how to block an extension that uses the permission "usb".</span></span>

    :::image type="content" source="media/microsoft-edge-manage-extensions-policies/manage-extensions-gp-block-1.png" alt-text="Konfigurieren Sie die Gruppenrichtlinie, um eine Erweiterung zu blockieren.":::

<span data-ttu-id="0c8b2-119">Das folgende Beispiel zeigt den JSON-Code, um alle Erweiterungen zu blockieren, die die Berechtigung „usb“ und der komprimierten Zeichenfolge verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="0c8b2-119">The following example shows the JSON to block any extension that needs the use of permission "usb" and its compressed string.</span></span>

### <a name="json-example"></a><span data-ttu-id="0c8b2-120">JSON-Beispiel</span><span class="sxs-lookup"><span data-stu-id="0c8b2-120">JSON example</span></span>

   ```json
   { 
        "*": { 
             "blocked_permissions": ["usb"] 
        } 
   } 
   ```

   ```json
   {"*":{"blocked_permissions":["usb"]}} 
   ```

   > [!NOTE]
   > <span data-ttu-id="0c8b2-121">Um alle Erweiterungen zu blockieren, die die Berechtigung verwenden, geben Sie als Erweiterungs-ID ein Sternchen an, wie im vorherigen Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="0c8b2-121">To block all extensions that use the permission, use an asterisk for the extension ID, as shown in the previous example.</span></span> <span data-ttu-id="0c8b2-122">Wenn Sie eine Erweiterungs-ID angeben, gilt die Richtlinie nur für diese Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="0c8b2-122">If you specify one extension ID, the policy will only apply to that extension.</span></span> <span data-ttu-id="0c8b2-123">Sie können mehrere Erweiterungen blockieren, diese müssen aber als separate Einträge angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0c8b2-123">You can block more than one, but they need to be separate entries.</span></span>

## <a name="prevent-extensions-from-altering-web-pages"></a><span data-ttu-id="0c8b2-124">Verhindern, dass Webseiten durch Erweiterungen geändert werden</span><span class="sxs-lookup"><span data-stu-id="0c8b2-124">Prevent extensions from altering web pages</span></span>

<span data-ttu-id="0c8b2-125">Diese Einstellung verhindert, dass Erweiterungen Daten von vertraulichen Websites und Domänen lesen und ändern.</span><span class="sxs-lookup"><span data-stu-id="0c8b2-125">This setting prevents extensions from reading and changing  data from sensitive websites and domains.</span></span> <span data-ttu-id="0c8b2-126">Das Blockieren unerwünschter Aktionen erfolgt durch Blockieren von Aktionen wie Skripteinschleusung in Ihre Websites, Lesen der Cookies oder ausführen von Webanforderungsänderungen.</span><span class="sxs-lookup"><span data-stu-id="0c8b2-126">Blocking unwanted actions is done by blocking actions such as script injection into your websites, reading the cookies, or making web-request modifications.</span></span> <span data-ttu-id="0c8b2-127">Diese Einstellung hindert Ihre Benutzer nicht daran, Erweiterungen zu installieren oder zu entfernen, sie verhindert nur, dass Erweiterungen die angegebenen Websites ändern.</span><span class="sxs-lookup"><span data-stu-id="0c8b2-127">This setting doesn’t prevent your users from installing or removing extensions, it only prevents extensions from altering the specified websites.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="0c8b2-128">Die Einstellung für zulässige/blockierte Hosts kann nur innerhalb der Erweiterungseinstellungsrichtlinie festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="0c8b2-128">The Runtime allowed/blocked hosts setting can only be set within the extension settings policy.</span></span>  

<span data-ttu-id="0c8b2-129">Sie können die folgenden Einstellungen in der ExtensionSettings-Richtlinie konfigurieren, um Änderungen von Websites oder Domänen zu verhindern (oder zuzulassen):</span><span class="sxs-lookup"><span data-stu-id="0c8b2-129">You can configure the following settings in the ExtensionSettings policy to prevent (or allow) alterations of websites or domains:</span></span>

- <span data-ttu-id="0c8b2-130">**Runtime_blocked_hosts**.</span><span class="sxs-lookup"><span data-stu-id="0c8b2-130">**Runtime_blocked_hosts**.</span></span> <span data-ttu-id="0c8b2-131">Mit dieser Einstellung wird verhindert, dass Erweiterungen Änderungen vornehmen oder Daten aus den Websites lesen, die Sie angeben.</span><span class="sxs-lookup"><span data-stu-id="0c8b2-131">This setting blocks extensions from making changes or reading data from the websites you specify.</span></span>
- <span data-ttu-id="0c8b2-132">**Runtime_allowed_hosts**.</span><span class="sxs-lookup"><span data-stu-id="0c8b2-132">**Runtime_allowed_hosts**.</span></span> <span data-ttu-id="0c8b2-133">Mit dieser Einstellung können Erweiterungen Änderungen vornehmen oder Daten aus den Websites lesen, die Sie angeben.</span><span class="sxs-lookup"><span data-stu-id="0c8b2-133">This setting allows extensions to make changes or read data from the websites you specify.</span></span> <span data-ttu-id="0c8b2-134">Das folgende Format wird verwendet, um Ihre Websites in der JSON-Zeichenfolge in der Richtlinie anzugeben:</span><span class="sxs-lookup"><span data-stu-id="0c8b2-134">The following format is used for specifying your site(s) in the JSON string in the policy:</span></span>

  ```json
  [http|https|ftp|*]://[subdomain|*].[hostname|*].[eTLD|*] [http|https|ftp|*],
  ```

  > [!NOTE]
  > `[hostname|*], and [eTLD|*]` <span data-ttu-id="0c8b2-135">Abschnitte sind erforderlich, aber der `[subdomain|*]`-Abschnitt ist optional.</span><span class="sxs-lookup"><span data-stu-id="0c8b2-135">sections are required, but `[subdomain|*]` section is optional.</span></span>

<span data-ttu-id="0c8b2-136">Die folgende Tabelle zeigt Beispiele für gültige Hostmuster und Vergleichsmuster.</span><span class="sxs-lookup"><span data-stu-id="0c8b2-136">The following table shows examples of valid host patterns and matching patterns.</span></span>

|<span data-ttu-id="0c8b2-137">Gültige Hostmuster</span><span class="sxs-lookup"><span data-stu-id="0c8b2-137">Valid host patterns</span></span>|<span data-ttu-id="0c8b2-138">Treffer</span><span class="sxs-lookup"><span data-stu-id="0c8b2-138">Matches</span></span>|<span data-ttu-id="0c8b2-139">Stimmt nicht überein</span><span class="sxs-lookup"><span data-stu-id="0c8b2-139">Doesn't match</span></span>|
|--|--|--|
|  `*://*.example.*` | `http://example.com`<br>`https://test.example.co.uk`   | `https://example.microsoft.com`<br>`http://example.microsoft.co.uk`  |
| `http://example.*` | `http://example.com`<br>`http://example.ly` | `https://example.com`<br>`http://test.example.com`   |
| `http://example.com`   | `http://example.com` | `https://example.com`<br>`http://test.example.co.uk` |
| `*://*`   | <span data-ttu-id="0c8b2-140">Alle URLs</span><span class="sxs-lookup"><span data-stu-id="0c8b2-140">All URLs</span></span>  |   |

<span data-ttu-id="0c8b2-141">Nutzen Sie die folgenden Schritte als Anleitung, um den Zugriff von Erweiterungen auf eine Website oder Domäne zu blockieren oder zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="0c8b2-141">Use the following steps as a guide to block or allow extensions to access a website or domain.</span></span>

1. <span data-ttu-id="0c8b2-142">Öffnen Sie den Gruppenrichtlinienverwaltungs-Editor, wechseln Sie zu **Administrative Vorlagen > Microsoft Edge > Erweiterungen**, und wählen Sie dann **Erweiterungsverwaltungseinstellungen konfigurieren** aus.</span><span class="sxs-lookup"><span data-stu-id="0c8b2-142">Open the group policy management editor and go to **Administrative Templates > Microsoft Edge > Extensions**, and then select **Configure extension management settings**.</span></span>  
2. <span data-ttu-id="0c8b2-143">Aktivieren Sie die Richtlinie, und geben Sie dann die Berechtigungen ein, die sie zulassen oder blockieren möchten, indem die Berechtigungen in eine einzige JSON-Zeichenfolge komprimiert werden.</span><span class="sxs-lookup"><span data-stu-id="0c8b2-143">Enable the policy, then enter the permissions that you want allowed or blocked, compressing the permissions to a single JSON string.</span></span>

<span data-ttu-id="0c8b2-144">In den folgenden Beispielen wird gezeigt, wie Erweiterungen für einen Hostnamen und Erweiterungen in derselben Domäne blockiert werden.</span><span class="sxs-lookup"><span data-stu-id="0c8b2-144">The following examples show how to block extensions on a hostname and how to block extensions on the same domain.</span></span>

### <a name="json-example-to-block-hostname"></a><span data-ttu-id="0c8b2-145">JSON-Beispiel zum Blockieren des Hostnamens</span><span class="sxs-lookup"><span data-stu-id="0c8b2-145">JSON example to block hostname</span></span>

<span data-ttu-id="0c8b2-146">Dieses Beispiel zeigt den JSON-Code und die komprimierte JSON-Zeichenfolge, mit der Sie verhindern, dass eine beliebige Erweiterung auf den `www.microsoft.com`-Hostnamen zugreift.</span><span class="sxs-lookup"><span data-stu-id="0c8b2-146">This example shows the JSON and compressed JSON string to block any extension from accessing the `www.microsoft.com` hostname.</span></span>

```json
{ 
    "*":{ 
            "runtime_blocked_hosts":["www.microsoft.com"] 
    } 
} 
```

```json
{"*":{"runtime_blocked_hosts":["www.microsoft.com"]}} 
```

> [!NOTE]
> <span data-ttu-id="0c8b2-147">Um für alle Erweiterungen den Zugriff auf eine Webseite zu verhindern, geben Sie als Erweiterungs-ID ein Sternchen an, wie im vorherigen Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="0c8b2-147">To block all extensions from accessing a webpage, use an asterisk for the extension ID, as shown in the previous example.</span></span>  <span data-ttu-id="0c8b2-148">Wenn Sie eine Erweiterungs-ID anstelle eines Sternchens angeben, gilt die Richtlinie nur für diese Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="0c8b2-148">If you specify one extension ID instead of an asterisk, the policy will only apply to that extension.</span></span> <span data-ttu-id="0c8b2-149">Sie können mehrere Erweiterungen blockieren, diese müssen aber als separate Einträge angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0c8b2-149">You can block more than one extension, but they need to be separate entries.</span></span>

### <a name="json-example-to-block-extensions-on-same-domain"></a><span data-ttu-id="0c8b2-150">JSON-Beispiel zum Blockieren von Erweiterungen in derselben Domäne</span><span class="sxs-lookup"><span data-stu-id="0c8b2-150">JSON example to block extensions on same domain</span></span>

<span data-ttu-id="0c8b2-151">Dieses Beispiel zeigt den JSON-Code und die komprimierte JSON-Zeichenfolge, mit der Sie verhindern, dass bestimmte Erweiterungen in derselben Domäne „importantwebsite“ ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="0c8b2-151">This example shows the JSON and compressed JSON string to block specific extensions from running on the same domain, "importantwebsite".</span></span>

```json
{ 
    "aapbdbdomjkkjkaonfhkkikfgjllcleb": { 
        "runtime_blocked_hosts": ["*://*.importantwebsite"] 
    }, 
    "bfbmjmiodbnnpllbbbfblcplfjjepjdn": { 
        "runtime_blocked_hosts": ["*://*.importantwebsite"] 
    } 
} 
```

```json
{"aapbdbdomjkkjkaonfhkkikfgjllcleb": {"runtime_blocked_hosts": ["*://,*.importantwebsite"]},"bfbmjmiodbnnpllbbbfblcplfjjepjdn": {"runtime_blocked_hosts": ["*://*.importantwebsite"]}} 
```

## <a name="allow-or-block-extensions-in-group-policy"></a><span data-ttu-id="0c8b2-152">Zulassen oder Blockieren von Erweiterungen in Gruppenrichtlinien</span><span class="sxs-lookup"><span data-stu-id="0c8b2-152">Allow or block extensions in group policy</span></span>

<span data-ttu-id="0c8b2-153">Sie können die [ExtensionInstallBlocklist](/DeployEdge/microsoft-edge-policies#extensioninstallblocklist)- und [ExtensionInstallAllowlist](/DeployEdge/microsoft-edge-policies#extensioninstallallowlist)-Richtlinien verwenden, um zu steuern, welche Erweiterungen blockiert oder zugelassen werden.</span><span class="sxs-lookup"><span data-stu-id="0c8b2-153">You can use the [ExtensionInstallBlocklist](/DeployEdge/microsoft-edge-policies#extensioninstallblocklist) and [ExtensionInstallAllowlist](/DeployEdge/microsoft-edge-policies#extensioninstallallowlist) policies to control which extensions are blocked or allowed.</span></span> <span data-ttu-id="0c8b2-154">Nutzen Sie die folgenden Schritte als Anleitung, um alle Erweiterungen mit Ausnahme der Erweiterungen, die Sie blockieren möchten, zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="0c8b2-154">Use the following steps as a guide to allow all extensions except those you want to block.</span></span>

1. <span data-ttu-id="0c8b2-155">Öffnen Sie den Gruppenrichtlinienverwaltungs-Editor, wechseln Sie zu **Administrative Vorlagen > Microsoft Edge > Erweiterungen**, und wählen Sie dann **Steuern, welche Erweiterungen nicht installiert werden können** aus.</span><span class="sxs-lookup"><span data-stu-id="0c8b2-155">Open the group policy management editor and go to **Administrative Templates > Microsoft Edge > Extensions >** and then select **Control which extensions cannot be installed**.</span></span>
2. <span data-ttu-id="0c8b2-156">Wählen Sie **Aktiviert** aus.</span><span class="sxs-lookup"><span data-stu-id="0c8b2-156">Select **Enabled**.</span></span>
3. <span data-ttu-id="0c8b2-157">Klicken Sie auf **Anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="0c8b2-157">Click **Show**.</span></span>
4. <span data-ttu-id="0c8b2-158">Geben Sie die App-ID der Erweiterungen ein, die Sie blockieren möchten.</span><span class="sxs-lookup"><span data-stu-id="0c8b2-158">Enter the app ID of the extensions that you want to block.</span></span> <span data-ttu-id="0c8b2-159">Verwenden Sie beim Hinzufügen mehrerer App-IDs eine separate Zeile für jede ID.</span><span class="sxs-lookup"><span data-stu-id="0c8b2-159">When adding multiple app ID’s use a separate row for each ID.</span></span>
5. <span data-ttu-id="0c8b2-160">Zum Blockieren aller Erweiterungen geben Sie **\*** in die Richtlinie ein, um zu verhindern, dass Erweiterungen installiert werden.</span><span class="sxs-lookup"><span data-stu-id="0c8b2-160">To block all extensions, type **\*** into the policy to prevent any extensions from being installed.</span></span> <span data-ttu-id="0c8b2-161">Sie können dies in Verbindung mit der Richtlinie „Installation bestimmter Erweiterungen zulassen“ verwenden, um nur die Installation bestimmter Erweiterungen zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="0c8b2-161">You can use this in conjunction with the "Allow specific extensions to be installed" policy to only allow certain extensions to be installed.</span></span> <span data-ttu-id="0c8b2-162">Der nächste Screenshot zeigt eine Erweiterung, die basierend auf der angegebenen App-ID blockiert wird.</span><span class="sxs-lookup"><span data-stu-id="0c8b2-162">The next screenshot shows an extension that will be blocked based on the app ID that's provided.</span></span>

   :::image type="content" source="media/microsoft-edge-manage-extensions-policies/manage-extensions-gp-block-2.png" alt-text="Verwenden Sie die App-ID, um eine Erweiterung zu blockieren.":::

   > [!TIP]
   > <span data-ttu-id="0c8b2-164">Wenn Sie die App-ID einer Erweiterung nicht finden können, sehen Sie sich die Erweiterung auf der Website der Microsoft Edge-Add-Ons an.</span><span class="sxs-lookup"><span data-stu-id="0c8b2-164">If you can’t find the app ID of an extension, look at the extension in the Microsoft Edge Add-ons website.</span></span> <span data-ttu-id="0c8b2-165">Suchen Sie die spezifische Erweiterung, und Sie sehen die App-ID am Ende der URL in der Omnibox.</span><span class="sxs-lookup"><span data-stu-id="0c8b2-165">Find the specific extension and you will see the app ID at the end of the URL in the omnibox.</span></span>

> [!NOTE]
> <span data-ttu-id="0c8b2-166">Sie können eine Erweiterung, die bereits auf dem Computer eines Benutzers installiert ist, zur Blockierungsliste hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="0c8b2-166">You can add an extension to the blocklist that’s already installed on a user’s computer.</span></span> <span data-ttu-id="0c8b2-167">Dadurch wird die Erweiterung deaktiviert und verhindert, dass der Benutzer sie erneut aktiviert.</span><span class="sxs-lookup"><span data-stu-id="0c8b2-167">This will disable the extension and prevent the user from re-enabling it.</span></span> <span data-ttu-id="0c8b2-168">Sie wird nicht deinstalliert, nur deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="0c8b2-168">It won't be uninstalled, just disabled.</span></span>

## <a name="force-install-an-extension"></a><span data-ttu-id="0c8b2-169">Erzwingen der Installation einer Erweiterung</span><span class="sxs-lookup"><span data-stu-id="0c8b2-169">Force-install an extension</span></span>

<span data-ttu-id="0c8b2-170">Verwenden Sie die [ExtensionInstallForcelist](/DeployEdge/microsoft-edge-policies#extensioninstallforcelist)-Richtlinie, um zu steuern, welche Erweiterungen blockiert oder zugelassen werden.</span><span class="sxs-lookup"><span data-stu-id="0c8b2-170">Use the [ExtensionInstallForcelist](/DeployEdge/microsoft-edge-policies#extensioninstallforcelist) policy to control which extensions are blocked or allowed.</span></span> <span data-ttu-id="0c8b2-171">Nutzen Sie die folgenden Schritte als Anleitung, um die Installation einer Erweiterung zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="0c8b2-171">Use the following steps as a guide to force-install an extension.</span></span>

1. <span data-ttu-id="0c8b2-172">Öffnen Sie den Gruppenrichtlinien-Editor, wechseln Sie zu **Administrative Vorlagen > Microsoft Edge > Erweiterungen**, und wählen Sie dann **Steuern, welche Erweiterungen im Hintergrund installiert werden** aus.</span><span class="sxs-lookup"><span data-stu-id="0c8b2-172">In the Group Policy Editor, go to **Administrative Templates> Microsoft Edge >  Extensions >** and then select **Control which extensions are installed silently**.</span></span>
2. <span data-ttu-id="0c8b2-173">Wählen Sie **Aktiviert** aus.</span><span class="sxs-lookup"><span data-stu-id="0c8b2-173">Select **Enabled**.</span></span>  
3. <span data-ttu-id="0c8b2-174">Klicken Sie auf **Anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="0c8b2-174">Click **Show**.</span></span>
4. <span data-ttu-id="0c8b2-175">Geben Sie die App-IDs der Erweiterungen ein, deren Installation Sie erzwingen möchten.</span><span class="sxs-lookup"><span data-stu-id="0c8b2-175">Enter the app ID or IDs of the extension or extensions you want to force-install.</span></span>  

<span data-ttu-id="0c8b2-176">Die Erweiterung wird im Hintergrund und ohne Benutzerinteraktion installiert.</span><span class="sxs-lookup"><span data-stu-id="0c8b2-176">The extension will be installed silently with no need for user interaction.</span></span> <span data-ttu-id="0c8b2-177">Der Benutzer kann die Erweiterung auch nicht deinstallieren oder deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="0c8b2-177">The user also won’t be able to uninstall or disable the extension.</span></span> <span data-ttu-id="0c8b2-178">Diese Einstellung überschreibt alle aktivierten Blockierungslistenrichtlinien.</span><span class="sxs-lookup"><span data-stu-id="0c8b2-178">This setting will overwrite over any blocklist policy that’s enabled.</span></span>

> [!NOTE]
> <span data-ttu-id="0c8b2-179">Verwenden Sie für im Chrome Web Store gehostete Erweiterungen eine Zeichenfolge wie z.B. `pckdojakecnhhplcgfflhndiffaohfah;https://clients2.google.com/service/update2/crx`.</span><span class="sxs-lookup"><span data-stu-id="0c8b2-179">For extensions hosted in the Chrome web store use a string such as: `pckdojakecnhhplcgfflhndiffaohfah;https://clients2.google.com/service/update2/crx`.</span></span>

## <a name="block-extensions-from-a-specific-store-or-update-url"></a><span data-ttu-id="0c8b2-180">Blockieren von Erweiterungen aus einem bestimmten Store oder von einer bestimmten Update-URL</span><span class="sxs-lookup"><span data-stu-id="0c8b2-180">Block extensions from a specific store or update URL</span></span>

<span data-ttu-id="0c8b2-181">Um Erweiterungen aus einem bestimmten Store oder von einer bestimmten URL zu blockieren, müssen Sie nur die *update_url* für den diesen Store mit der Richtlinie [ExtensionSettings](/deployedge/microsoft-edge-policies#extensionsettings) blockieren.</span><span class="sxs-lookup"><span data-stu-id="0c8b2-181">To block extensions from a particular store or URL, you only need to block the *update_url* for that store using the [ExtensionSettings](/deployedge/microsoft-edge-policies#extensionsettings) policy.</span></span>

<span data-ttu-id="0c8b2-182">Nutzen Sie die folgenden Schritte als Anleitung, um Erweiterungen aus einem bestimmten Store oder von einer bestimmten URL zu blockieren.</span><span class="sxs-lookup"><span data-stu-id="0c8b2-182">Use the following steps as a guide to block extensions from an particular store or URL.</span></span>

1. <span data-ttu-id="0c8b2-183">Öffnen Sie den Gruppenrichtlinienverwaltungs-Editor, wechseln Sie zu **Administrative Vorlagen > Microsoft Edge > Erweiterungen**, und wählen Sie dann **Erweiterungsverwaltungseinstellungen konfigurieren** aus.</span><span class="sxs-lookup"><span data-stu-id="0c8b2-183">Open the group policy management editor and go to **Administrative Templates > Microsoft Edge > Extensions >** and then select **Configure extension management settings**.</span></span>  
2. <span data-ttu-id="0c8b2-184">Aktivieren Sie die Richtlinie, und geben Sie dann die Berechtigungen ein, die sie zulassen oder blockieren möchten, indem sie in eine einzige JSON-Zeichenfolge komprimiert werden.</span><span class="sxs-lookup"><span data-stu-id="0c8b2-184">Enable the policy, then enter the permissions that you want allowed or blocked, compressing it to a single JSON string.</span></span>

<span data-ttu-id="0c8b2-185">Das nächste Beispiel zeigt den JSON-Code und die komprimierte JSON-Zeichenfolge, die mithilfe der Update-URL (`https://clients2.google.com/service/update2/crx`) vom Chrome Web Store blockiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0c8b2-185">The next example shows the JSON and compressed JSON string to block from the Chrome Web Store using its update URL (`https://clients2.google.com/service/update2/crx`).</span></span>

### <a name="json-example-for-blocking-on-update-url"></a><span data-ttu-id="0c8b2-186">JSON-Beispiel für das Blockieren der Update-URL</span><span class="sxs-lookup"><span data-stu-id="0c8b2-186">JSON example for blocking on update URL</span></span>

```json
{ 
"update_url:https://clients2.google.com/service/update2/crx":{ 
                                                             " installation_mode":"blocked" 
                                                             } 
} 
```

```json
{"update_url:https://clients2.google.com/service/update2/crx":{"installation_mode":"blocked"}} 
```

> [!NOTE]
> <span data-ttu-id="0c8b2-187">Sie können **ExtensionInstallForceList** und **ExtensionInstallAllowList** weiterhin verwenden, um die Installation bestimmter Erweiterungen zu erzwingen bzw. zu erlauben, auch wenn der Store mit dem JSON im vorherigen Beispiel blockiert wurde.</span><span class="sxs-lookup"><span data-stu-id="0c8b2-187">You can still use **ExtensionInstallForceList** and **ExtensionInstallAllowList** to allow/force install specific extensions even if the store is blocked using the JSON in the previous example.</span></span>

## <a name="see-also"></a><span data-ttu-id="0c8b2-188">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0c8b2-188">See also</span></span>

- [<span data-ttu-id="0c8b2-189">Verwalten von Microsoft Edge-Erweiterungen im Unternehmen</span><span class="sxs-lookup"><span data-stu-id="0c8b2-189">Manage Microsoft Edge extensions in the enterprise</span></span>](microsoft-edge-manage-extensions.md)
- [<span data-ttu-id="0c8b2-190">Erstellen eines Web Stores zum Hosten von Microsoft Edge Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="0c8b2-190">Create a web store to host Microsoft Edge extensions</span></span>](microsoft-edge-manage-extensions-webstore.md)
- [<span data-ttu-id="0c8b2-191">Referenzhandbuch für die „ExtensionSettings“-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="0c8b2-191">Reference guide for the ExtensionSettings policy</span></span>](microsoft-edge-manage-extensions-ref-guide.md)
- [<span data-ttu-id="0c8b2-192">Häufig gestellte Fragen (FAQ) zu Microsoft Edge-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="0c8b2-192">FAQ for Microsoft Edge Extensions</span></span>](microsoft-edge-manage-extensions-faq.md)
- [<span data-ttu-id="0c8b2-193">Microsoft Edge Enterprise-Angebotsseite</span><span class="sxs-lookup"><span data-stu-id="0c8b2-193">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
