---
title: Microsoft Edge-Proxyeinstellungen
ms.author: brianalt
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: 'Verwenden von Befehlszeilenoptionen zum Konfigurieren von Proxyeinstellungen '
ms.openlocfilehash: 99a5f0776ea42f1e26050e0d30adb48a63907b8c
ms.sourcegitcommit: 8968f3107291935ed9adc84bba348d5f187eadae
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/12/2021
ms.locfileid: "11979276"
---
# <a name="how-to-use-microsoft-edge-command-line-options-to-configure-proxy-settings"></a>So verwenden Sie Microsoft Edge-Befehlszeilenoptionen zum Konfigurieren von Proxyeinstellungen

In diesem Artikel wird beschrieben, wie Sie mithilfe von Befehlszeilenoptionen die Standardnetzwerkeinstellungen des Systems überschreiben können.

>[!NOTE]
>Dieser Artikel bezieht sich auf Microsoft Edge Version 77 oder höher.

## <a name="system-network-settings"></a>Netzwerkeinstellungen des Systems

Der Microsoft Edge-Netzwerkstapel verwendet standardmäßig die Netzwerkeinstellungen des Systems. Zu diesen Einstellungen gehören *Proxyeinstellungen* sowie *Zertifikat- und private Schlüsselspeicher*.

Es gibt Szenarien, in denen Benutzer eine Alternative zur Verwendung der Standardproxyeinstellungen des Systems anfordern. Zur Unterstützung dieser Szenarien unterstützt Microsoft Edge Befehlszeilenoptionen, mit denen Sie benutzerdefinierte Proxyeinstellungen konfigurieren können.

Diese Befehlszeilenoptionen entsprechen den folgenden Richtlinien in der **Proxyserver**-Gruppe:

- [ProxyBypassList](./microsoft-edge-policies.md#proxybypasslist)
- [ProxyMode](./microsoft-edge-policies.md#proxymode)
- [ProxyPacUrl](./microsoft-edge-policies.md#proxypacurl)
- [ProxyServer](./microsoft-edge-policies.md#proxyserver)
- [ProxySettings](./microsoft-edge-policies.md#proxysettings)

## <a name="command-line-options-for-proxy-settings"></a>Befehlszeilenoptionen für Proxyeinstellungen

Microsoft Edge unterstützt die folgenden proxybezogenen Befehlszeilenoptionen.

 **`--no-proxy-server`**
 
Weist Microsoft Edge an, keinen Proxy zu verwenden, auch wenn das System anderweitig für die Verwendung eines Proxys konfiguriert ist. Es werden alle anderen bereitgestellten Proxyeinstellungen außer Kraft gesetzt.

**`--proxy-auto-detect`**

Weist Microsoft Edge an, Ihre Proxykonfiguration zu testen und automatisch zu erkennen. Dieses Argument wird ignoriert, wenn `--proxy-server` konfiguriert ist.

**`--proxy-server=<scheme>=<uri>[:<port>][;...] | <uri>[:<port>] | "direct://"`**

Weist Microsoft Edge an, eine benutzerdefinierte Proxykonfiguration zu verwenden. Sie können eine benutzerdefinierte Proxykonfiguration auf drei Arten angeben.

1. Stellen Sie eine durch Semikola getrennte Zuordnung des Listenschemas zu URL/Port-Paaren bereit. Beispielsweise weist `--proxy-server="http=proxy1:8080;ftp=ftpproxy"` Microsoft Edge an, den HTTP-Proxy „proxy1: 8080” für http-URLs und den HTTP-Proxy „ftpproxy: 80” für ftp-URLs zu verwenden.
2. Indem ein einzelner URI mit optionalem Port für alle URLs bereitgestellt wird. Beispielsweise verwendet `--proxy-server="proxy2:8080"` den Proxy unter „proxy2: 8080” für den gesamten Datenverkehr.
3. Mit dem speziellen Wert „direct://”. Beispielsweise stellt `--proxy-server="direct://"` sicher, dass keine der Verbindungen einen Proxy verwendet. 

>[!NOTE]
>Sie können Microsoft Edge so konfigurieren, dass versucht wird, einen Proxy zu verwenden, und dass ein Fallback ausgeführt wird, wenn der Proxy nicht verfügbar ist. Beispiel: `--proxy-server="http://proxy2:8080,direct://`.

**`--proxy-bypass-list=(<trailing_domain>|<ip-address>)[:<port>][;...]`**

Weist Microsoft Edge an, alle angegebenen Proxys für die angegebene durch Semikola getrennte Liste der Hosts zu umgehen. Dieses Kennzeichen muss mit `--proxy-server` verwendet werden.

>[!NOTE]
>Für den Abgleich von nachgestellten Domänen sind keine „.”-Trennzeichen erforderlich. Die Trennzeichen „\*microsoft.com” stimmen mit „imicrosoft.com” überein. Beispielsweise verwendet `--proxy-server="proxy2:8080" --proxy-bypass-list="*.microsoft.com;*example.com;127.0.0.1:8080"` den Proxyserver „proxy2” auf Port 8080 für alle Hosts, mit Ausnahme der Anforderungen für \*.microsoft.com, example.com und 127.0.0.1 auf Port 8080. Im vorherigen Beispiel werden imicrosoft.com-Anforderungen weiterhin mit Proxys übertragen. Allerdings werden iexample.com-Anforderungen den Proxy umgehen, da \*example.com anstelle von \*.example.com angegeben wurde.

**`--proxy-pac-url=<pac-file-url>`**

Weist Microsoft Edge an, die PAC-datei unter der angegebenen URL zu verwenden. Beispielsweise weist `--proxy-pac-url="https://wpad/proxy.pac"` Microsoft Edge an, Proxyinformationen für URL-Anforderungen mithilfe der **proxy.pac**-Datei aufzulösen.

## <a name="content-license"></a>Lizenz für Inhalte

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf von Chromium.org erstellten und freigegebenen Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/) beschriebenen Begriffen verwendet werden. Die Originalseite von Chromium finden Sie [hier](https://www.chromium.org/developers/design-documents/network-settings#TOC-Command-line-options-for-proxy-sett).
  
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />Diese Arbeit unterliegt einer <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.

## <a name="see-also"></a>Weitere Informationen

- Informationen zu erweiterten Konfigurationseinstellungen und zusätzlichen Optionen finden Sie in der [Proxy-Dokumentation](https://chromium.googlesource.com/chromium/src/+/HEAD/net/docs/proxy.md) des Chromium Open Source-Projekts.
- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)