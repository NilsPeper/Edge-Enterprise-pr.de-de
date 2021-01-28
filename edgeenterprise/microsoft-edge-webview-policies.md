---
title: Dokumentation für die Microsoft Edge WebView2-Richtlinie
ms.author: stmoody
author: dan-wesley
manager: tahills
ms.date: 01/27/2021
audience: ITPro
ms.topic: reference
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
ms.custom: ''
description: Windows- und Mac-Dokumentation für alle vom Microsoft Edge Browser unterstützten Richtlinien
ms.openlocfilehash: 52c426e3c08764fbbfdce207127ca083d38a93c4
ms.sourcegitcommit: e9433045503c2614386ee4948cda0a9c9701bac5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/28/2021
ms.locfileid: "11304718"
---
# Microsoft Edge WebView2 –⁠ Richtlinien

Die neueste Version von Microsoft Edge WebView2 umfasst die folgenden Richtlinien. Sie können diese Richtlinien verwenden, um zu konfigurieren, wie Microsoft Edge WebView2 in Ihrer Organisation ausgeführt wird.

Informationen zu einer zusätzlichen Richtlinie, mit der Sie steuern können, wie und wann Microsoft Edge WebView2 aktualisiert wird, finden Sie unter [Microsoft Edge Updaterichtlinien-Referenz](microsoft-edge-update-policies.md).

> [!NOTE]
> Dieser Artikel bezieht sich auf Microsoft Edge Version 87 oder neuer.

## Verfügbare Richtlinien

In dieser Tabelle sind sämtliche, in dieser Version von Microsoft Edge WebView2 verfügbaren Gruppenrichtlinien aufgeführt. Über die Links in der folgenden Tabelle erhalten Sie weitere Einzelheiten zu bestimmten Richtlinien.

|||
|-|-|
|[Einstellungen für Loader-Außerkraftsetzung](#loader-override-settings)|

### [*Einstellungen für Loader-Außerkraftsetzung*](#loader-override-settings-policies)

|Richtlinienname|Beschriftung|
|-|-|
|[BrowserExecutableFolder](#browserexecutablefolder)|Konfigurieren des Speicherorts des ausführbaren Browser-Ordners|
|[ReleaseChannelPreference](#releasechannelpreference)|Einstellen der Präferenz für die Suchreihenfolge der Veröffentlichungskanäle|




  ## Einstellungen für Loader-Außerkraftsetzungsrichtlinien

  [Zurück zum Anfang](#microsoft-edge-webview2---policies)

  ### BrowserExecutableFolder

  #### Konfigurieren des Speicherorts des ausführbaren Browser-Ordners

  
  
  #### Unterstützte Versionen:

  - Unter Windows seit 87 oder später

  #### Beschreibung

  Diese Richtlinie konfiguriert WebView2-Anwendungen, um die WebView2-Laufzeit im angegebenen Pfad zu verwenden. Der Ordner sollte die folgenden Dateien enthalten: msedgewebview2.exe, msedge.dl usw.

Um den Wert für den Ordnerpfad festzulegen, geben Sie einen Wertnamen und ein Wertpaar an. Legen Sie den Wertnamen auf die Anwendungsbenutzer Modell-ID oder den Dateinamen der ausführbaren Datei fest. Sie können den Platzhalter "*" als Wert für alle Anwendungen verwenden.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Liste von Zeichenfolgen

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - Eindeutiger Name der GP: BrowserExecutableFolder
  - Name der GP: Konfigurieren des Speicherorts des ausführbaren Browser-Ordners
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/WebView2/Loader Override Settings
  - GP Pfad (Empfohlen): n.a.
  - Name der GP-ADMX-Datei: MSEdgeWebView2.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge\WebView2\BrowserExecutableFolder
  - Pfad (Empfohlen): n.a.
  - Wertname: REG_SZ-Liste
  - Werttyp: REG_SZ-Liste

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\WebView2\BrowserExecutableFolder = "Name: *, Value: C:\\Program Files\\Microsoft Edge WebView2 Runtime Redistributable 85.0.541.0 x64"

```

  

  [Zurück zum Anfang](#microsoft-edge-webview2---policies)

  ### ReleaseChannelPreference

  #### Einstellen der Präferenz für die Suchreihenfolge der Veröffentlichungskanäle

  
  
  #### Unterstützte Versionen:

  - Unter Windows seit 87 oder später

  #### Beschreibung

  Die standardmäßige Kanalsuchreihenfolge ist WebView2 Runtime, Beta, Dev und Canary.

Um die Standardsuchreihenfolge umzukehren, legen Sie diese Richtlinie auf 1 fest.

Um den Wert für den bevorzugten Veröffentlichungskanal festzulegen, geben Sie einen Wertnamen und ein Wertpaar an. Legen Sie den Wertnamen auf die Anwendungsbenutzer Modell-ID oder den Dateinamen der ausführbaren Datei fest. Sie können den Platzhalter "*" als Wert für alle Anwendungen verwenden.

  #### Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:

  - Liste von Zeichenfolgen

  #### Windows-Informationen und -Einstellungen

  ##### Informationen zur Gruppenrichtlinie (ADMX)

  - Eindeutiger Name der GP: ReleaseChannelPreference
  - Name der GP: Einstellen der Präferenz für die Suchreihenfolge der Veröffentlichungskanäle
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/WebView2/Loader Override Settings
  - GP Pfad (Empfohlen): n.a.
  - Name der GP-ADMX-Datei: MSEdgeWebView2.admx

  ##### Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge\WebView2\ReleaseChannelPreference
  - Pfad (Empfohlen): n.a.
  - Wertname: REG_SZ-Liste
  - Werttyp: REG_SZ-Liste

  ##### Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\WebView2\ReleaseChannelPreference = "Name: *, Value: 1"

```

  

  [Zurück zum Anfang](#microsoft-edge-webview2---policies)


## Weitere Informationen

- [Konfigurieren von Microsoft Edge](configure-microsoft-edge.md)
- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)
- [Microsoft Sicherheitsbaselines-Blog](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/bg-p/Microsoft-Security-Baselines)