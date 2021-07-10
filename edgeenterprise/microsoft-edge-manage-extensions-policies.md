---
title: Verwenden von Gruppenrichtlinien zur Verwaltung von Microsoft Edge Erweiterungen
ms.author: aspoddar
author: AndreaLBarr
manager: balajek
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Verwenden von Gruppenrichtlinien zur Verwaltung von Microsoft Edge Erweiterungen im Unternehmen
ms.openlocfilehash: dad239a448ec1f0ebef60c7072bfaad5c3baed57
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "11641371"
---
# <a name="use-group-policies-to-manage-microsoft-edge-extensions"></a>Verwenden von Gruppenrichtlinien zur Verwaltung von Microsoft Edge Erweiterungen

In diesem Artikel werden die Optionen und Schritte zum Verwalten von Erweiterungen mithilfe von Gruppenrichtlinien beschrieben. Bei diesen Optionen wird davon ausgegangen, dass Sie bereits Microsoft Edge für Ihre Benutzer verwaltet haben. Wenn Sie die Verwaltung von Microsoft Edge für Ihre Benutzer noch nicht eingerichtet haben, folgen Sie dem Link unten, um dies jetzt zu tun.

- [Verwalten von Microsoft Edge-Erweiterungen im Unternehmen](/deployedge/microsoft-edge-manage-extensions)

> [!NOTE]
> Dieser Artikel bezieht sich auf Microsoft Edge Version 77 oder höher.

## <a name="block-extensions-based-on-their-permissions"></a>Blockieren von Erweiterungen basierend auf ihren Berechtigungen

Mithilfe der [ExtensionSettings](/deployedge/microsoft-edge-policies#extensionsettings)-Richtlinie können Sie steuern, welche Erweiterungen Ihre Benutzer basierend auf Berechtigungen installieren können. Wenn eine installierte Erweiterung eine Berechtigung benötigt, die blockiert ist, wird sie einfach nicht ausgeführt. Die Erweiterung wird nicht entfernt, nur deaktiviert.

> [!NOTE]
> Die Einstellung für blockierte Berechtigungen kann nur innerhalb der Erweiterungseinstellungsrichtlinie festgelegt werden.  

Nutzen Sie die folgenden Schritte als Anleitung, um eine Erweiterung zu blockieren.

1. Öffnen Sie den Gruppenrichtlinienverwaltungs-Editor, wechseln Sie zu **Administrative Vorlagen > Microsoft Edge > Erweiterungen**, und wählen Sie dann **Erweiterungsverwaltungseinstellungen konfigurieren** aus.
2. Aktivieren Sie die Richtlinie, und geben Sie dann die Berechtigungen ein, die sie zulassen oder blockieren möchten, indem Sie eine JSON-Zeichenfolge verwenden, die komprimiert wird. Der nächste Screenshot zeigt, wie Sie eine Erweiterung blockieren, die die Berechtigung „usb“ verwendet.

    :::image type="content" source="media/microsoft-edge-manage-extensions-policies/manage-extensions-gp-block-1.png" alt-text="Konfigurieren Sie die Gruppenrichtlinie, um eine Erweiterung zu blockieren.":::

Das folgende Beispiel zeigt den JSON-Code, um alle Erweiterungen zu blockieren, die die Berechtigung „usb“ und der komprimierten Zeichenfolge verwenden müssen.

### <a name="json-example"></a>JSON-Beispiel

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
   > Um alle Erweiterungen zu blockieren, die die Berechtigung verwenden, geben Sie als Erweiterungs-ID ein Sternchen an, wie im vorherigen Beispiel gezeigt. Wenn Sie eine Erweiterungs-ID angeben, gilt die Richtlinie nur für diese Erweiterung. Sie können mehrere Erweiterungen blockieren, diese müssen aber als separate Einträge angegeben werden.

## <a name="prevent-extensions-from-altering-web-pages"></a>Verhindern, dass Webseiten durch Erweiterungen geändert werden

Diese Einstellung verhindert, dass Erweiterungen Daten von vertraulichen Websites und Domänen lesen und ändern. Das Blockieren unerwünschter Aktionen erfolgt durch Blockieren von Aktionen wie Skripteinschleusung in Ihre Websites, Lesen der Cookies oder ausführen von Webanforderungsänderungen. Diese Einstellung hindert Ihre Benutzer nicht daran, Erweiterungen zu installieren oder zu entfernen, sie verhindert nur, dass Erweiterungen die angegebenen Websites ändern. 
  
> [!NOTE]
> Die Einstellung für zulässige/blockierte Hosts kann nur innerhalb der Erweiterungseinstellungsrichtlinie festgelegt werden.  

Sie können die folgenden Einstellungen in der ExtensionSettings-Richtlinie konfigurieren, um Änderungen von Websites oder Domänen zu verhindern (oder zuzulassen):

- **Runtime_blocked_hosts**. Mit dieser Einstellung wird verhindert, dass Erweiterungen Änderungen vornehmen oder Daten aus den Websites lesen, die Sie angeben.
- **Runtime_allowed_hosts**. Mit dieser Einstellung können Erweiterungen Änderungen vornehmen oder Daten aus den Websites lesen, die Sie angeben. Das folgende Format wird verwendet, um Ihre Websites in der JSON-Zeichenfolge in der Richtlinie anzugeben:

  ```json
  [http|https|ftp|*]://[subdomain|*].[hostname|*].[eTLD|*] [http|https|ftp|*],
  ```

  > [!NOTE]
  > `[hostname|*], and [eTLD|*]` Abschnitte sind erforderlich, aber der `[subdomain|*]`-Abschnitt ist optional.

Die folgende Tabelle zeigt Beispiele für gültige Hostmuster und Vergleichsmuster.

|Gültige Hostmuster|Treffer|Stimmt nicht überein|
|--|--|--|
|  `*://*.example.*` | `http://example.com`<br>`https://test.example.co.uk`   | `https://example.microsoft.com`<br>`http://example.microsoft.co.uk`  |
| `http://example.*` | `http://example.com`<br>`http://example.ly` | `https://example.com`<br>`http://test.example.com`   |
| `http://example.com`   | `http://example.com` | `https://example.com`<br>`http://test.example.co.uk` |
| `*://*`   | Alle URLs  |   |

Nutzen Sie die folgenden Schritte als Anleitung, um den Zugriff von Erweiterungen auf eine Website oder Domäne zu blockieren oder zuzulassen.

1. Öffnen Sie den Gruppenrichtlinienverwaltungs-Editor, wechseln Sie zu **Administrative Vorlagen > Microsoft Edge > Erweiterungen**, und wählen Sie dann **Erweiterungsverwaltungseinstellungen konfigurieren** aus.  
2. Aktivieren Sie die Richtlinie, und geben Sie dann die Berechtigungen ein, die sie zulassen oder blockieren möchten, indem die Berechtigungen in eine einzige JSON-Zeichenfolge komprimiert werden.

In den folgenden Beispielen wird gezeigt, wie Erweiterungen für einen Hostnamen und Erweiterungen in derselben Domäne blockiert werden.

### <a name="json-example-to-block-hostname"></a>JSON-Beispiel zum Blockieren des Hostnamens

Dieses Beispiel zeigt den JSON-Code und die komprimierte JSON-Zeichenfolge, mit der Sie verhindern, dass eine beliebige Erweiterung auf den `www.microsoft.com`-Hostnamen zugreift.

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
> Um für alle Erweiterungen den Zugriff auf eine Webseite zu verhindern, geben Sie als Erweiterungs-ID ein Sternchen an, wie im vorherigen Beispiel gezeigt.  Wenn Sie eine Erweiterungs-ID anstelle eines Sternchens angeben, gilt die Richtlinie nur für diese Erweiterung. Sie können mehrere Erweiterungen blockieren, diese müssen aber als separate Einträge angegeben werden.

### <a name="json-example-to-block-extensions-on-same-domain"></a>JSON-Beispiel zum Blockieren von Erweiterungen in derselben Domäne

Dieses Beispiel zeigt den JSON-Code und die komprimierte JSON-Zeichenfolge, mit der Sie verhindern, dass bestimmte Erweiterungen in derselben Domäne „importantwebsite“ ausgeführt werden.

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

## <a name="allow-or-block-extensions-in-group-policy"></a>Zulassen oder Blockieren von Erweiterungen in Gruppenrichtlinien

Sie können die [ExtensionInstallBlocklist](/DeployEdge/microsoft-edge-policies#extensioninstallblocklist)- und [ExtensionInstallAllowlist](/DeployEdge/microsoft-edge-policies#extensioninstallallowlist)-Richtlinien verwenden, um zu steuern, welche Erweiterungen blockiert oder zugelassen werden. Nutzen Sie die folgenden Schritte als Anleitung, um alle Erweiterungen mit Ausnahme der Erweiterungen, die Sie blockieren möchten, zuzulassen.

1. Öffnen Sie den Gruppenrichtlinienverwaltungs-Editor, wechseln Sie zu **Administrative Vorlagen > Microsoft Edge > Erweiterungen**, und wählen Sie dann **Steuern, welche Erweiterungen nicht installiert werden können** aus.
2. Wählen Sie **Aktiviert** aus.
3. Klicken Sie auf **Anzeigen**.
4. Geben Sie die App-ID der Erweiterungen ein, die Sie blockieren möchten. Verwenden Sie beim Hinzufügen mehrerer App-IDs eine separate Zeile für jede ID.
5. Um alle Erweiterungen zu blockieren, geben Sie * *\** _ in die Richtlinie ein, um zu verhindern, dass Erweiterungen installiert werden. Sie können dies in Verbindung mit der Richtlinie „Installation bestimmter Erweiterungen zulassen“ verwenden, um nur die Installation bestimmter Erweiterungen zuzulassen. Der nächste Screenshot zeigt eine Erweiterung, die basierend auf der angegebenen App-ID blockiert wird.

   :::image type="content" source="media/microsoft-edge-manage-extensions-policies/manage-extensions-gp-block-2.png" alt-text="Verwenden Sie die App-ID, um eine Erweiterung zu blockieren.":::

   > [!TIP]
   > Wenn Sie die App-ID einer Erweiterung nicht finden können, sehen Sie sich die Erweiterung auf der Website der Microsoft Edge-Add-Ons an. Suchen Sie die spezifische Erweiterung, und Sie sehen die App-ID am Ende der URL in der Omnibox.

> [!NOTE]
> Sie können eine Erweiterung, die bereits auf dem Computer eines Benutzers installiert ist, zur Blockierungsliste hinzufügen. Dadurch wird die Erweiterung deaktiviert und verhindert, dass der Benutzer sie erneut aktiviert. Sie wird nicht deinstalliert, nur deaktiviert.

## <a name="force-install-an-extension"></a>Erzwingen der Installation einer Erweiterung

Verwenden Sie die [ExtensionInstallForcelist](/DeployEdge/microsoft-edge-policies#extensioninstallforcelist)-Richtlinie, um zu steuern, welche Erweiterungen blockiert oder zugelassen werden. Nutzen Sie die folgenden Schritte als Anleitung, um die Installation einer Erweiterung zu erzwingen.

1. Wechseln Sie im Gruppenrichtlinien-Editor zu _*Administrative Vorlagen> Microsoft Edge > Erweiterungen >** und wählen Sie dann **steuern, welche Erweiterungen im Hintergrund installiert werden.**
2. Wählen Sie **Aktiviert** aus.  
3. Klicken Sie auf **Anzeigen**.
4. Geben Sie die App-IDs der Erweiterungen ein, deren Installation Sie erzwingen möchten.  

Die Erweiterung wird im Hintergrund und ohne Benutzerinteraktion installiert. Der Benutzer kann die Erweiterung auch nicht deinstallieren oder deaktivieren. Diese Einstellung überschreibt alle aktivierten Blockierungslistenrichtlinien.

> [!NOTE]
> Verwenden Sie für im Chrome Web Store gehostete Erweiterungen eine Zeichenfolge wie z. B. `pckdojakecnhhplcgfflhndiffaohfah;https://clients2.google.com/service/update2/crx`.

## <a name="block-extensions-from-a-specific-store-or-update-url"></a>Blockieren von Erweiterungen aus einem bestimmten Store oder von einer bestimmten Update-URL

Um Erweiterungen aus einem bestimmten Store oder von einer bestimmten URL zu blockieren, müssen Sie nur die *update_url* für den diesen Store mit der Richtlinie [ExtensionSettings](/deployedge/microsoft-edge-policies#extensionsettings) blockieren.

Nutzen Sie die folgenden Schritte als Anleitung, um Erweiterungen aus einem bestimmten Store oder von einer bestimmten URL zu blockieren.

1. Öffnen Sie den Gruppenrichtlinienverwaltungs-Editor, wechseln Sie zu **Administrative Vorlagen > Microsoft Edge > Erweiterungen**, und wählen Sie dann **Erweiterungsverwaltungseinstellungen konfigurieren** aus.  
2. Aktivieren Sie die Richtlinie, und geben Sie dann die Berechtigungen ein, die sie zulassen oder blockieren möchten, indem sie in eine einzige JSON-Zeichenfolge komprimiert werden.

Das nächste Beispiel zeigt den JSON-Code und die komprimierte JSON-Zeichenfolge, die mithilfe der Update-URL (`https://clients2.google.com/service/update2/crx`) vom Chrome Web Store blockiert werden sollen.

### <a name="json-example-for-blocking-on-update-url"></a>JSON-Beispiel für das Blockieren der Update-URL

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
> Sie können **ExtensionInstallForceList** und **ExtensionInstallAllowList** weiterhin verwenden, um die Installation bestimmter Erweiterungen zu erzwingen bzw. zu erlauben, auch wenn der Store mit dem JSON im vorherigen Beispiel blockiert wurde.

## <a name="see-also"></a>Weitere Informationen

- [Verwalten von Microsoft Edge-Erweiterungen im Unternehmen](microsoft-edge-manage-extensions.md)
- [Erstellen eines Web Stores zum Hosten von Microsoft Edge Erweiterungen](microsoft-edge-manage-extensions-webstore.md)
- [Referenzhandbuch für die „ExtensionSettings“-Richtlinie](microsoft-edge-manage-extensions-ref-guide.md)
- [Häufig gestellte Fragen (FAQ) zu Microsoft Edge-Erweiterungen](microsoft-edge-manage-extensions-faq.md)
- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)
