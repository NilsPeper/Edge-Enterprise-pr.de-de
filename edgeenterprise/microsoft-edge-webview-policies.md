---
title: Dokumentation für die Microsoft Edge WebView2-Richtlinie
ms.author: stmoody
author: dan-wesley
manager: tahills
ms.date: 08/30/2021
audience: ITPro
ms.topic: reference
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
ms.custom: ''
description: Windows- und Mac-Dokumentation für alle vom Microsoft Edge Browser unterstützten Richtlinien
ms.openlocfilehash: b0a7949d71ca037e1adf02b71637f5b1e7351cce
ms.sourcegitcommit: 8968f3107291935ed9adc84bba348d5f187eadae
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/12/2021
ms.locfileid: "11979536"
---
# <a name="microsoft-edge-webview2---policies"></a>Microsoft Edge WebView2 –⁠ Richtlinien

Die neueste Version von Microsoft Edge WebView2 umfasst die folgenden Richtlinien. Sie können diese Richtlinien verwenden, um zu konfigurieren, wie Microsoft Edge WebView2 in Ihrer Organisation ausgeführt wird.

Informationen zu einer zusätzlichen Richtlinie, mit der Sie steuern können, wie und wann Microsoft Edge WebView2 aktualisiert wird, finden Sie unter [Microsoft Edge Updaterichtlinien-Referenz](microsoft-edge-update-policies.md).


> [!NOTE]
> Dieser Artikel bezieht sich auf Microsoft Edge Version 87 oder neuer.

## <a name="available-policies"></a>Verfügbare Richtlinien

In dieser Tabelle sind sämtliche, in dieser Version von Microsoft Edge WebView2 verfügbaren Gruppenrichtlinien aufgeführt. Über die Links in der folgenden Tabelle erhalten Sie weitere Einzelheiten zu bestimmten Richtlinien.

- [Einstellungen für Loader-Außerkraftsetzung](#loader-override-settings)


### [*<a name="loader-override-settings"></a>Einstellungen für Loader-Außerkraftsetzung*](#loader-override-settings-policies)

|Richtlinienname|Beschriftung|
|-|-|
|[BrowserExecutableFolder](#browserexecutablefolder)|Konfigurieren des Speicherorts des ausführbaren Browser-Ordners|
|[ReleaseChannelPreference](#releasechannelpreference)|Einstellen der Präferenz für die Suchreihenfolge der Veröffentlichungskanäle|




  ## <a name="loader-override-settings-policies"></a>Einstellungen für Loader-Außerkraftsetzungsrichtlinien

  [Zurück zum Anfang](#microsoft-edge-webview2---policies)

  ### <a name="browserexecutablefolder"></a>BrowserExecutableFolder

  #### <a name="configure-the-location-of-the-browser-executable-folder"></a>Konfigurieren des Speicherorts des ausführbaren Browser-Ordners

  
  
  #### <a name="supported-versions"></a>Unterstützte Versionen:

  - Unter Windows seit 87 oder später

  #### <a name="description"></a>Beschreibung

  Diese Richtlinie konfiguriert WebView2-Anwendungen, um die WebView2-Laufzeit im angegebenen Pfad zu verwenden. Der Ordner sollte die folgenden Dateien enthalten: msedgewebview2.exe, msedge.dl usw.

Um den Wert für den Ordnerpfad festzulegen, geben Sie einen Wertnamen und ein Wertpaar an. Legen Sie den Wertnamen auf die Anwendungsbenutzer Modell-ID oder den Dateinamen der ausführbaren Datei fest. Sie können den Platzhalter "*" als Wert für alle Anwendungen verwenden.

  #### <a name="supported-features"></a>Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### <a name="data-type"></a>Datentyp:

  - Liste von Zeichenfolgen

  #### <a name="windows-information-and-settings"></a>Windows-Informationen und -Einstellungen

  ##### <a name="group-policy-admx-info"></a>Informationen zur Gruppenrichtlinie (ADMX)

  - Eindeutiger Name der GP: BrowserExecutableFolder
  - Name der GP: Konfigurieren des Speicherorts des ausführbaren Browser-Ordners
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/WebView2/Loader Override Settings
  - GP Pfad (Empfohlen): n.a.
  - Name der GP-ADMX-Datei: MSEdgeWebView2.admx

  ##### <a name="windows-registry-settings"></a>Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge\WebView2\BrowserExecutableFolder
  - Pfad (Empfohlen): n.a.
  - Wertname: REG_SZ-Liste
  - Werttyp: REG_SZ-Liste

  ##### <a name="example-value"></a>Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\WebView2\BrowserExecutableFolder = "Name: *, Value: C:\\Program Files\\Microsoft Edge WebView2 Runtime Redistributable 85.0.541.0 x64"

```

  

  [Zurück zum Anfang](#microsoft-edge-webview2---policies)

  ### <a name="releasechannelpreference"></a>ReleaseChannelPreference

  #### <a name="set-the-release-channel-search-order-preference"></a>Einstellen der Präferenz für die Suchreihenfolge der Veröffentlichungskanäle

  
  
  #### <a name="supported-versions"></a>Unterstützte Versionen:

  - Unter Windows seit 87 oder später

  #### <a name="description"></a>Beschreibung

  Die standardmäßige Kanalsuchreihenfolge ist WebView2 Runtime, Beta, Dev und Canary.

Um die Standardsuchreihenfolge umzukehren, legen Sie diese Richtlinie auf 1 fest.

Um den Wert für den bevorzugten Veröffentlichungskanal festzulegen, geben Sie einen Wertnamen und ein Wertpaar an. Legen Sie den Wertnamen auf die Anwendungsbenutzer Modell-ID oder den Dateinamen der ausführbaren Datei fest. Sie können den Platzhalter "*" als Wert für alle Anwendungen verwenden.

  #### <a name="supported-features"></a>Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### <a name="data-type"></a>Datentyp:

  - Liste von Zeichenfolgen

  #### <a name="windows-information-and-settings"></a>Windows-Informationen und -Einstellungen

  ##### <a name="group-policy-admx-info"></a>Informationen zur Gruppenrichtlinie (ADMX)

  - Eindeutiger Name der GP: ReleaseChannelPreference
  - Name der GP: Einstellen der Präferenz für die Suchreihenfolge der Veröffentlichungskanäle
  - GP-Pfad (verpflichtend): Administrative Templates/Microsoft Edge/WebView2/Loader Override Settings
  - GP Pfad (Empfohlen): n.a.
  - Name der GP-ADMX-Datei: MSEdgeWebView2.admx

  ##### <a name="windows-registry-settings"></a>Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge\WebView2\ReleaseChannelPreference
  - Pfad (Empfohlen): n.a.
  - Wertname: REG_SZ-Liste
  - Werttyp: REG_SZ-Liste

  ##### <a name="example-value"></a>Beispielwert:

```
SOFTWARE\Policies\Microsoft\Edge\WebView2\ReleaseChannelPreference = "Name: *, Value: 1"

```

  

  [Zurück zum Anfang](#microsoft-edge-webview2---policies)


## <a name="see-also"></a>Weitere Informationen

- [Konfigurieren von Microsoft Edge](configure-microsoft-edge.md)
- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)
- [Microsoft Sicherheitsbaselines-Blog](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/bg-p/Microsoft-Security-Baselines)