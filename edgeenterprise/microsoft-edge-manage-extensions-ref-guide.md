---
title: Detaillierter Leitfaden zur ExtensionSettings-Richtlinie
ms.author: aspoddar
author: dan-wesley
manager: balajek
ms.date: 03/31/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Ein detaillierter Referenzleitfaden zum Konfigurieren von Microsoft Edge-Erweiterungen mithilfe der ExtensionSettings-Richtlinie.
ms.openlocfilehash: 89ff329d6e209a4e658907385ec24fd0d2f1d1c2
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2021
ms.locfileid: "11618130"
---
# <a name="detailed-guide-to-the-extensionsettings-policy"></a>Detaillierter Leitfaden zur ExtensionSettings-Richtlinie

Microsoft Edge bietet mehrere Möglichkeiten zum Verwalten von Erweiterungen. Eine gängige Methode ist das Festlegen mehrerer Richtlinien an einem Ort mit einer JSON-Zeichenfolge im Windows Gruppenrichtlinien-Editor oder in der Windows-Registrierung mithilfe der [ExtensionSettings](/deployedge/microsoft-edge-policies#extensionsettings)-Richtlinie.

> [!NOTE]
> Dieser Artikel bezieht sich auf Microsoft Edge Version 77 oder höher.

## <a name="before-you-begin"></a>Bevor Sie beginnen

Sie entscheiden, ob Sie hier alle Erweiterungsverwaltungseinstellungen festlegen oder diese Steuerelemente über andere Richtlinien festlegen möchten.
  
Die ExtensionSettings-Richtlinie kann andere Richtlinien überschreiben, die Sie an anderer Stelle in der Gruppenrichtlinie festgelegt haben, einschließlich der folgenden Richtlinien:

- [ExtensionAllowedTypes](/DeployEdge/microsoft-edge-policies#extensionallowedtypes)
- [ExtensionInstallBlocklist](/DeployEdge/microsoft-edge-policies#extensioninstallblocklist)
- [ExtensionInstallForcelist](/DeployEdge/microsoft-edge-policies#extensioninstallforcelist)
- [ExtensionInstallSources](/DeployEdge/microsoft-edge-policies#extensioninstallsources)
- [ExtensionInstallAllowlist](/DeployEdge/microsoft-edge-policies#extensioninstallsources)

## <a name="extensionsettings-policy-fields"></a>ExtensionSettings-Richtlinienfelder

Diese Richtlinie kann Einstellungen wie die Update-URL steuern, von der die Erweiterung für die Erstinstallation heruntergeladen wird, und blockierte Berechtigungen oder welche Berechtigungen nicht ausgeführt werden dürfen. In der folgenden Tabelle werden die verfügbaren Richtlinienfelder beschrieben.

| &nbsp; | Beschreibung |
|--|--|
| **allowed_types** | Kann nur verwendet werden, um die Standardkonfiguration * zu konfigurieren. Gibt an, welche Arten von App- oder Erweiterungsbenutzern auf Microsoft Edge installiert werden dürfen. Der Wert ist eine Liste von Zeichenfolgen, die jeweils einen der folgenden Typen aufweisen sollten: "extension", "theme", "user_script" und "hosted_app"   |
| **blocked_install_message**| Wenn Sie verhindern, dass Benutzer bestimmte Erweiterungen installieren, können Sie eine benutzerdefinierte Meldung angeben, die im Browser angezeigt werden soll, wenn Benutzer versuchen, sie zu installieren.<br>Fügen Sie Text an die allgemeine Fehlermeldung an, die auf der Microsoft Edge Add-Ons-Website angezeigt wird. Beispielsweise können Sie Benutzern mitteilen, wie sie ihre IT-Abteilung kontaktieren oder warum eine bestimmte Erweiterung nicht verfügbar ist. Die Meldung kann bis zu 1 000 Zeichen lang sein.   |
|**blocked_permissions**  | Verhindert, dass Benutzer Erweiterungen installieren und ausführen, die bestimmte API-Berechtigungen anfordern, die Ihre Organisation nicht zulässt. Sie können z. B. Erweiterungen blockieren, die auf Cookies zugreifen. Wenn eine Erweiterung eine Berechtigung erfordert, die Sie blockiert haben, kann der Benutzer sie nicht installieren. Wenn Benutzer die Erweiterung zuvor installiert haben, wird sie nicht mehr geladen. Wenn eine Erweiterung eine blockierte Berechtigung als optionale Anforderung enthält, wird sie wie gewohnt installiert. Während die Erweiterung ausgeführt wird, werden blockierte Berechtigungen automatisch abgelehnt.<br>Eine Liste der verfügbaren Berechtigungen finden Sie unter [Berechtigungen deklarieren](/microsoft-edge/extensions-chromium/enterprise/declare-permissions).   |
| **installation_mode**| Steuert, ob und wie von Ihnen angegebene Erweiterungen Microsoft Edge hinzugefügt werden. Sie können den Installationsmodus auf eine der folgenden Optionen festlegen:<br>– allowed: Benutzer können die Erweiterung installieren. Wenn kein Installationsmodus definiert ist, ist diese Einstellung die Standardeinstellung.<br>– blocked: Benutzer können die Erweiterung nicht installieren.<br>– force_installed: Automatische Installation der Erweiterung ohne Benutzerinteraktion. Benutzer können sie nicht entfernen. Außerdem müssen Sie den Downloadspeicherort der Erweiterung mithilfe von update_url definieren. **Hinweis**: Sie können diese Einstellung nicht mit * verwenden, da Microsoft Edge nicht weiss, welche Erweiterung automatisch installiert werden soll.<br>– normal_installed: Automatische Installation der Erweiterung ohne Benutzerinteraktion. Benutzer können sie deaktivieren. Außerdem müssen Sie den Downloadspeicherort der Erweiterung mithilfe von update_url definieren. **Hinweis**: Sie können diese Einstellung nicht mit * verwenden, da Microsoft Edge nicht weiss, welche Erweiterung automatisch installiert werden soll.<br>– removed: Benutzer können die Erweiterung nicht installieren. Wenn Benutzer die Erweiterung zuvor installiert haben, entfernt Microsoft Edge sie. |  |
| **install_sources** | Kann nur verwendet werden, um die Standardkonfiguration * zu konfigurieren. Gibt an, welche URLs Erweiterungen installieren dürfen. Sowohl der Speicherort der *CRX-Datei als auch die Seite, von der aus der Download gestartet wird (der Referrer), müssen durch diese Muster zulässig sein. Beispiele für URL-Muster finden Sie unter [Übereinstimmungsmustern](/microsoft-edge/extensions-chromium/enterprise/match-patterns).  |
| **minimum_version_required** |Microsoft Edge deaktiviert Erweiterungen, einschließlich erzwungen installierter Erweiterungen, mit einer Version, die älter als die angegebene Mindestversion ist.<br>Das Format der Versionszeichenfolge entspricht dem Format, das im Erweiterungsmanifest verwendet wird.     |
| **update_url** | Gilt nur für force_installed und normal_installed. Gibt an, von wo aus Microsoft Edge eine Erweiterung herunterladen soll. Wenn die Erweiterung in der Microsoft Edge Add-Ons-Website gehostet wird, verwenden Sie diesen Speicherort: `https://edge.microsoft.com/extensionwebstorebase/v1/crx`.<br>Microsoft Edge verwendet die URL, die Sie für die Erstinstallation der Erweiterung angeben. Für nachfolgende Erweiterungsupdates verwendet Microsoft Edge die URL im Manifest der Erweiterung.   |
| **runtime_allowed_hosts**| Ermöglicht Erweiterungen die Interaktion mit bestimmten Websites, auch wenn sie auch in runtime_blocked_hosts definiert sind. Sie können bis zu 100 Einträge angeben. Zusätzliche Einträge werden verworfen.<br>Das Hostmusterformat ähnelt  [Übereinstimmungsmustern](/microsoft-edge/extensions-chromium/enterprise/match-patterns) , es sei denn, Sie können den Pfad nicht definieren. Beispiel:<br>- *://*.example.com<br>- *://example.* – eTLD-Platzhalter werden unterstützt     |
| **runtime_blocked_hosts**| Verhindern, dass Erweiterungen mit von Ihnen angegebenen Websites interagieren oder diese ändern. Änderungen umfassen das Blockieren der JavaScript-Einfügung, den Cookiezugriff und Webanforderungsänderungen.<br>Sie können bis zu 100 Einträge angeben. Zusätzliche Einträge werden verworfen.<br>Das Hostmusterformat ähnelt Übereinstimmungsmustern, es sei denn, Sie können den Pfad nicht definieren. Beispiel:<br>- *://*.example.com<br>- *://example.* – eTLD-Platzhalter werden unterstützt   |


## <a name="configure-using-a-json-string-in-windows-group-policy-editor"></a>Konfigurieren einer JSON-Zeichenfolge im Gruppenrichtlinien-Editor von Windows

Bei den Schritten zur Verwendung der Erweiterungseinstellungsrichtlinie mithilfe des Gruppenrichtlinienobjekts (GPO) wird davon ausgegangen, dass Sie ADM/ADMX bereits für Microsoft Edge-Richtlinien importiert haben.

1. Öffnen Sie den Gruppenrichtlinien-Editor, und wechseln Sie zu **Microsoft Edge > Erweiterungen > Einstellungsrichtlinie für die Erweiterungsverwaltung konfigurieren**.
2. Aktivieren Sie die Richtlinie, und geben Sie die JSONN-Daten (JavaScript Object Notation) als einzelne Zeile ohne Zeilenumbrüche in das Textfeld ein.
3. Um die Richtlinie zu überprüfen und in einer einzigen Zeile zu komprimieren, verwenden Sie ein JSON-Komprimierungstool.

### <a name="properly-format-json-for-the-extension-settings-policy"></a>Ordnungsgemäßes Formatieren von JSON für die Erweiterungseinstellungsrichtlinie

Sie müssen die beiden Teile dieser Richtlinie verstehen – den Standardbereich und den einzelnen Bereich. Der Standardbereich ist ein Catch-All für Erweiterungen ohne eigenen Bereich. Der einzelne Bereich wird nur auf diese Erweiterung angewendet.  

Der Standardbereich wird durch das Sternchen (*) identifiziert. Im nächsten Beispiel werden ein Standardbereich und ein einzelner Erweiterungsbereich definiert.

```json
{ 
   “*”: {}, 
   “nckgahadagoaajjgafhacjanaoiihapd”: {} 
} 
```

Eine Erweiterung erhält ihre Einstellungen nur aus einem Bereich. Wenn ein einzelner Erweiterungsbereich für diese Erweiterung vorhanden ist, sind dies die Einstellungen, die für diese Erweiterung gelten. Wenn kein einzelner Erweiterungsbereich vorhanden ist, verwendet die Erweiterung den Standardbereich.  

Im nächsten JSON-Beispiel wird verhindert, dass eine Erweiterung auf `.example.com` ausgeführt wird, und alle Erweiterungen blockiert, die die Berechtigung "USB" erfordern.

```json
{ 
  "*": { 
    "runtime_blocked_hosts": ["*://*.example.com"], 
    "blocked_permissions": ["usb"] 
  } 
} 
```

**Compact JSON**

```json
{"*":{"runtime_blocked_hosts":["*://*.example.com"],"blocked_permissions":["usb"]}} 
```

### <a name="a-few-more-json-examples-for-extension-settings"></a>Weitere JSON-Beispiele für Erweiterungseinstellungen

#### <a name="using-installation_mode-property-to-allow-and-block-extensions"></a>Verwendung der installation_mode-Eigenschaft zum Zulassen und Blockieren von Erweiterungen

- Der Benutzer kann alle Erweiterungen installieren – dies ist die Standardeinstellung. 

  `{ "*": {"installation_mode": "allowed" }}`
- Der Benutzer kann keine Erweiterungen installieren.  

  `{ "*": {"installation_mode": "blocked" }}`

- Geben Sie eine benutzerdefinierte Meldung an, die angezeigt werden soll, wenn die Installation blockiert wird.

   `{"*": {"blocked_install_message": ["Call IT(408 - 555 - 1234) for an exception"]}}`

#### <a name="using-installation_mode-property-to-force-install-extensions"></a>Verwendung der installation_mode-Eigenschaft zum Erzwingen der Installation von Erweiterungen

Wenn installation_mode als "force_installed" verwendet wird, wird die Erweiterung automatisch ohne Benutzerinteraktion installiert. Ein Benutzer kann die Erweiterung nicht deaktivieren oder entfernen. Wenn eine Erweiterung "normal" oder "force" installiert ist, muss auch das **update_url**-Feld definiert werden. Dieses Feld verweist auf den Speicherort, von dem aus die Erweiterung installiert werden kann. Verwenden Sie die folgenden Speicherorte für das **update_url**-Feld:

- Wenn die Erweiterung, die Sie herunterladen, im Microsoft Edge Add-Ons-Store gehostet wird, verwenden Sie [https://edge.microsoft.com/extensionwebstorebase/v1/crx](https://edge.microsoft.com/extensionwebstorebase/v1/crx).
- Wenn die Erweiterung, die Sie herunterladen, im Chrome Web Store gehostet wird, verwenden Sie [https://clients2.google.com/service/update2/crx](https://clients2.google.com/service/update2/crx).
- Wenn Sie die Erweiterung auf Ihrem eigenen Server hosten, verwenden Sie die URL, unter der Microsoft Edge die gepackte Erweiterung (CRX-Datei) herunterladen können. JSON-Beispiel:

   `{"nckgahadagoaajjgafhacjanaoiihapd": {"installation_mode": "force_installed","update_url": "https://edge.microsoft.com/extensionwebstorebase/v1/crx"}}`
  
Wenn Sie im obigen Beispiel anstelle von "force_installed" "normal_installed" verwenden, wird die Erweiterung automatisch ohne Benutzerinteraktion installiert, aber sie kann die Erweiterung deaktivieren.  

   > [!TIP]
   > Das richtige Formatieren einer JSON-Zeichenfolge kann schwierig sein. Verwenden Sie vor der Implementierung der Richtlinie eine JSON-Überprüfung. Oder testen Sie die frühe Version des [Generatortools für Erweiterungseinstellungen](https://microsoft.github.io/edge-extension-settings-generator/minimal)

## <a name="configure-using-the-windows-registry"></a>Konfigurieren mithilfe der Windows-Registrierung

Die ExtensionSettings-Richtlinie sollte unter diesem Schlüssel in die Registrierung geschrieben werden:

`HKLM\Software\Policies\Microsoft\Edge\`

> [!NOTE]
> Es ist möglich, HKCU anstelle von HKLM zu verwenden. Der entsprechende Pfad kann mit dem Gruppenrichtlinienobjekt (Group Policy Object, GPO) konfiguriert werden.  

Für Microsoft Edge werden alle Einstellungen unter diesem Schlüssel gestartet:

`HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Edge\`

Der nächste Schlüssel, den Sie erstellen, ist entweder die Erweiterungs-ID für den einzelnen Bereich oder ein Sternchen (*) für den Standardbereich. Beispielsweise verwenden Sie den folgenden Speicherort für Einstellungen, die für Google Hangouts gelten:

`HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Edge\ExtensionSettings\nckgahadagoaajjgafhacjanaoiihapd`

Verwenden Sie für Einstellungen, die für den Standardbereich gelten, folgenden Speicherort:

`HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Edge\ExtensionSettings\*`

Unterschiedliche Einstellungen erfordern unterschiedliche Formate, je nachdem, ob es sich um eine Zeichenfolge oder ein Zeichenfolgenarray handelt. Arraywerte erfordern [＂value＂]. Zeichenfolgenwerte können unverändert eingegeben werden. Die folgende Liste zeigt, welche Einstellungen Arrays oder Zeichenfolgen sind:

- Installation_mode = Zeichenfolge
- update_url = Zeichenfolge
- blocked_permissions = Zeichenfolgenarray
- allowed_permissions = Zeichenfolgenarray
- minimum_version_required = Zeichenfolge
- runtime_blocked_hosts = Zeichenfolgenarray
- runtime_allowed_hosts = Zeichenfolgenarray
- blocked_install_message = Zeichenfolge


## <a name="see-also"></a>Weitere Informationen

- [Verwalten von Microsoft Edge-Erweiterungen im Unternehmen](microsoft-edge-manage-extensions.md)
- [Verwenden von Gruppenrichtlinien zur Verwaltung von Microsoft Edge Erweiterungen](microsoft-edge-manage-extensions-policies.md)
- [Häufig gestellte Fragen (FAQ) zu Microsoft Edge-Erweiterungen](microsoft-edge-manage-extensions-faq.md)
- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)
