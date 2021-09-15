---
title: Anfängliche Einstellungsunterstützung für Microsoft Edge Browser
ms.author: collw
author: AndreaLBarr
manager: srugh
ms.date: 07/27/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Anfängliche Einstellungsunterstützung für Microsoft Edge Browser.
ms.openlocfilehash: 7a497fd2f3305b0c027a396936ef86bacbcb5b20
ms.sourcegitcommit: 8968f3107291935ed9adc84bba348d5f187eadae
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/12/2021
ms.locfileid: "11979196"
---
# <a name="configure-microsoft-edge-using-initial-preferences-settings-for-the-first-run"></a>Konfigurieren von Microsoft Edge mithilfe der anfänglichen Einstellungen für die Erstausführung

Verwenden Sie die folgenden Informationen, um Microsoft Edge Einstellungen für die anfänglichen Einstellungen auf Ihren Windows Geräten zu konfigurieren.

> [!Note]
> Dieser Artikel bezieht sich auf Microsoft Edge Version 93 oder höher.

## <a name="configure-policy-settings-on-windows"></a>Konfigurieren von Richtlinieneinstellungen unter Windows

Ab Microsoft Edge version 93 unterstützt Microsoft ab Version 93 eine begrenzte Anzahl von Anfänglichen Einstellungen, die früher als "Mastereinstellungen" bezeichnet wurden, um Administratoren bei der Konfiguration von Browsern für die erste Ausführung zu unterstützen. sehen Sie sich die Liste der unterstützten Einstellungen unten an.  

Bei der Bereitstellung dienen die anfänglichen Einstellungen als Standardbrowsereinstellungen auf verwalteten Geräten. Dies sind die Einstellungen, die von Administratoren bevorzugt werden, um als Standard verwendet zu werden, aber von Benutzern geändert werden können oder für einige Geräte nicht verfügbar sind, da sie keiner Active Directory®domäne angehören.

Einige Beispiele für Intialeinstellungen sind die anfängliche Konfiguration einer Standardstartseite oder Registerkarten mit bestimmten URLs.

Einstellungen werden nur einmal aus initial_preferences Datei kopiert, und alle Änderungen, die nach der Konfiguration an dieser Datei vorgenommen wurden, werden nicht berücksichtigt. Wenn eine Einstellung von einer [Microsoft Edge-Richtlinie](/deployedge/microsoft-edge-policies) verwaltet und in der initial_preferences-Datei konfiguriert ist, hat die Richtlinie immer Vorrang.

Nachfolgend finden Sie eine Liste der Einstellungseinstellungen, die derzeit von Microsoft Edge unterstützt werden:

| Einstellungskategorie | Einstellung |
| - | - |
| Bookmark_bar | show_apps_shortcut<br>show_managed_bookmarks<br>show_on_all_tabs |
| Bookmarks | editing_enabled |
| Browser/clear_data | browsing_history<br>browsing_history_basic"<br>Cache<br>cache_basic<br>Cookies<br>download_history<br>form_data<br>Kennwörter |
| Verlauf | browsing_history<br>Cache<br>Cookies<br>download_history<br>form_data<br>hosted_apps_data<br>Kennwörter<br>site_settings |
| Browser | first_run_tabs<br>dark_theme<br>show_toolbar_bookmarks_button<br>show_toolbar_collections_butto<br>show_toolbar_downloads_button<br>show_home_button<br>show_prompt_before_closing_tabs<br>show_toolbar_history_button |
| default_search_provider | [default_search_provider] aktiviert |
| Vollbild | Zugelassen |
| Homepage | Homepage_url |
| homepage_is_newtabpage | homepage_is_newtabpage |
| Sitzung | restore_on_startup<br>startup_urls |
| Erweiterungen | Erweiterungen: Einstellungen |

## <a name="1-download-an-example-initial_preferences-file"></a>1: Herunterladen einer Beispieldatei initial_preferences

To get started, download the "Policy" file from the [Microsoft Edge Enterprise landing page](https://www.microsoft.com/edge/business/download). Extrahieren Sie die Dateien, und öffnen Sie die `initial_preferences` Datei innerhalb des `examples` Ordners.

## <a name="2-customize-and-validate-the-initial_preferences-file"></a>2: Anpassen und Überprüfen der initial_preferences Datei

Passen Sie die Einstellungseinstellungen in der heruntergeladenen *initial_preferences-Datei* an, und überprüfen Sie die Änderungen, um sicherzustellen, dass im JSON-Code keine Fehler vorhanden sind. Wenn Sie Fehler finden, überprüfen Sie die Syntax und Struktur der *initial_preferences* Datei, nehmen Sie Korrekturen vor und überprüfen Sie sie erneut. Einige Beispieltools zum Überprüfen von JSON, Online [JSON Tools](https://jsonformatter.org/) oder [JSON-Bearbeitung in Visual Studio Code](https://code.visualstudio.com/docs/languages/json).

## <a name="3-deploy-preferences-to-users-computer"></a>3: Bereitstellen von Einstellungen auf dem Computer der Benutzer

Stellen Sie die *initial_preferences* Datei auf den Geräten der Benutzer zur gleichen Zeit bereit, wie Microsoft Edge Browser bereitgestellt wird, und platzieren Sie die Datei am folgenden Speicherort auf dem Gerät.

### <a name="windows-amd64-and-arm64"></a>Windows (AMD64 und ARM64)

| Kanal | Ort |
| - | - |
| Stable | `"C:\Program Files (x86)\Microsoft\Edge\Application"` |
| Beta | `"C:\Program Files (x86)\Microsoft\Edge Beta\Application"` |
|Canary | `"%LOCALAPPDATA%\Microsoft\Edge SxS\Application"` |
| Dev | `"C:\Program Files (x86)\Microsoft\Edge Dev\Application"` |

**Hinweis:** Die *initial_preferences* Datei muss im selben Ordner wie die msedge.exe-Datei auf den Computern der Benutzer Windows bereitgestellt werden.  

### <a name="macos"></a>macOS

| Kanal | Ort |
| - | - |
| Stable | `"~/Library/Application Support/Microsoft Edge/Microsoft Edge Initial Preferences"` |
| Beta | `“~/Library/Application Support/Microsoft Edge Beta/Microsoft Edge Initial Preferences"` |
| Canary | `“~/Library/Application Support/Microsoft Edge Canary/Microsoft Edge Initial Preferences"` |
| Dev | `"~/Library/Application Support/Microsoft Edge Dev/Microsoft Edge Initial Preferences"` |

## <a name="important-notes-msi--pkg-deployment-and-initial_preferences-interaction"></a>Wichtige Hinweise: MSI-/Pkg-Bereitstellung und *initial_preferences* Interaktion

Die anfänglichen Einstellungen werden nur wirksam, wenn die initial_preferences-Datei bereitgestellt wird, bevor der Browser von den Endbenutzern zum ersten Mal ausgeführt wird.  

## <a name="see-also"></a>Weitere Informationen

- [Die *initial_prefrences* Beispielvorlagendatei](https://www.microsoft.com/edge/business/download)
