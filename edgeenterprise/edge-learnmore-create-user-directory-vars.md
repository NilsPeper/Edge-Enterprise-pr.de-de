---
title: Erstellen von Microsoft Edge-Benutzerdatenverzeichnisvariablen
ms.author: brianalt
author: dan-wesley
manager: srugh
ms.date: 05/01/2020
audience: ITPro
ms.topic: procedural
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Erfahren Sie, wie Sie Microsoft Edge-Benutzerdatenverzeichnisvariablen erstellen
ms.openlocfilehash: 284bef9156dc3dff1413f349eebe4e7dac854a98
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/31/2020
ms.locfileid: "10980037"
---
# Erstellen von Microsoft Edge-Benutzerdatenverzeichnisvariablen

In diesem Artikel wird erläutert, wie Sie beim Ändern von Microsoft Edge Datenverzeichnisvariablen anstelle von hartcodierten Pfaden verwenden können.

>[!NOTE]
>Dieser Artikel bezieht sich auf Microsoft Edge Version 77 oder höher.

## Pfadvariablen

Richtlinien zum Ändern von Datenverzeichnispfaden (zum Beispiel das Konfigurieren der Unterstützungsvariablen [UserDataDir](microsoft-edge-policies.md#userdatadir) oder [DownloadDirectory](microsoft-edge-policies.md#downloaddirectory). Beim Konfigurieren dieser Richtlinien können Sie Variablen anstelle hartcodierter Pfade verwenden. Zum Beispiel, um Ihre Profildaten unter Windows unter lokalen Benutzeranwendungsdaten anstelle des Standardverzeichnisses zu speichern. Legen Sie die Richtlinie [UserDataDir](microsoft-edge-policies.md#userdatadir) auf **${local_app_data}\Edge\Profile** fest. Bei den meisten Windows10-Installationen wird dieser Pfad in *C:\Users\\&lt;Current-user&gt;\AppData\Local\Microsoft\Edge\Profile* aufgelöst.

>[!NOTE]
>Wenn nicht festgelegt, verwendet Microsoft Edge Standardverzeichnispfade. Ein Benutzer kann das `--user-data-dir`-Befehlszeilenkennzeichen verwenden, um die Standardeinstellung außer Kraft zu setzen.

Öffnen Sie zum Anzeigen des aktuellen **Profilpfads** die Seite **Informationen zur Version** (geben Sie "edge://version" ein). Der **Profilpfad** folgt dem folgenden Format: *C:\Users\\&lt;Current-user&gt;\AppData\Local\Microsoft\Edge\User Data\Default*.

### Leitfaden für die Verwendung von Pfadvariablen

Lesen Sie die folgenden Hinweise, bevor Sie Variablen für Pfade verwenden.

- Alle Richtlinien, die Pfade beinhalten, in denen Microsoft Edge unterschiedliche Daten speichert, sind plattformabhängig. Einige dieser Richtlinien sind nur auf bestimmten Plattformen verfügbar, andere können jedoch auf allen Plattformen verwendet werden.
- Stellen Sie sicher, dass die Pfade absolut sind, um Fehler zu vermeiden, die durch Anwendungen verursacht werden, die zu verschiedenen Zeitpunkten an verschiedenen Standorten starten.
- Jede Variable kann in einem Pfad nur einmal vorkommen. In den meisten Fällen ist dies die einzige sinnvolle Möglichkeit, Variablen zu verwenden, da sie in absolute Pfade aufgelöst werden.
- In fast allen Richtlinien wird der Pfad erstellt, wenn er nicht vorhanden ist (sofern unter den vorhandenen Umständen möglich).
- Die Verwendung von Netzwerkspeicherorten für einige Richtlinien kann zu unerwarteten Ergebnissen führen, da sich die verschiedenen Versionen bzw. Kanäle von Microsoft Edge in Bezug auf die Behandlung der Ordnerstruktur unterscheiden.

### Unterstützte Pfadvariablen

Microsoft Edge unterstützt die folgenden Pfadvariablen.

#### Alle Plattformen

| Variable | Beschreibung |
| --- | --- |
| **${user_name}** | Der Benutzer, der Microsoft Edge verwendet. Microsoft Edge respektiert SUIDs (Benutzer-ID des Besitzers wird bei Ausführung festgelegt) Beispiel: *audreysmall* |
| **${machine_name}** | Der Computername, möglicherweise einschließlich des Domänennamens. Beispiel: *audreysmall* oder *audrey.ex.contoso.com* |

#### Nur Windows

| Variable | Beschreibung |
| --- | --- |
| **${documents}** | Der Ordner „Eigene Dokumente“ für den aktuellen Benutzer. Beispiel: *C:\Users\Administrator\Documents* |
|**${local_app_data}** | Der Ordner „Anwendungsdaten“ für den aktuellen Benutzer. Beispiel: *C:\Users\Administrator\AppData\Local* |
|**${roaming_app_data}** | Der Ordner für servergespeicherte Anwendungsdaten für den aktuellen Benutzer. Beispiel: *C:\Users\Administrator\AppData\Roaming* |
| **${profile}** | Der Basisordner für den aktuellen Benutzer. Beispiel: *C:\Users\Administrator* |
| **${global_app_data}** | Der systemweite Ordner „Anwendungsdaten”. Beispiel: *C:\AppData* |
| **${program_files}** | Der Ordner „Programme” für den aktuellen Prozess. Dieser Ordner hängt davon ab, ob es sich um einen 32-Bit- oder 64-Bit-Prozess handelt. Beispiel für Auflösung: *C:\Program Files (x86)* |
| **${windows}** | Der Windows-Ordner. Beispiel: *C:\Windows* |
| **${client_name)** | Der Name des Client-PCs, der mit einer RDP- oder Citrix-Sitzung verbunden ist. Diese Variable ist leer, wenn sie aus einer lokalen Sitzung verwendet wird. Wenn sie in einem Pfad verwendet wird, stellen Sie ihr etwas voran, das garantiert nicht leer ist. Beispiel: *C:\edge_profiles\session_${client_name}* wird für Remote-Sitzungen in *C:\edge_profiles\session_&lt;ForlocalSessions&gt;* und *C:\edge_profiles\session_&lt;SomePCname&gt;* aufgelöst. |
| **${session_name}** | Der Name der aktiven Sitzung. Verwenden Sie diesen Namen, um mehrere gleichzeitig verbundene Remote-Sitzungen zu unterscheiden, die ein einziges Benutzerprofil verwenden. Beispiel: *WinSta0 für lokale Desktopsitzungen* |

#### Nur macOS

| Variable | Beschreibung |
| --- | --- |
| **${users}** | Der Ordner, in dem die Benutzerprofile gespeichert werden. Beispiel: */Users* |
| **${documents}** | Der Ordner „Eigene Dokumente“ für den aktuellen Benutzer. Beispiel: */Users/audreysmall/Documents* |

## Lizenz für Inhalte

>[!NOTE]
>Teile dieser Seite sind Änderungen, die auf von Chromium.org erstellten und freigegebenen Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/) beschriebenen Begriffen verwendet werden. Die Originalseite von Chromium finden Sie [hier](https://www.chromium.org/administrators/policy-list-3/user-data-directory-variables).
  
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br/>Diese Arbeit unterliegt einer <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.

## Weitere Informationen

- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)