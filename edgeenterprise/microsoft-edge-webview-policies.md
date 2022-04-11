---
title: Dokumentation für die Microsoft Edge WebView2-Richtlinie
ms.author: stmoody
author: dan-wesley
manager: tahills
ms.date: 04/08/2022
audience: ITPro
ms.topic: reference
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
ms.custom: ''
description: Windows- und Mac-Dokumentation für alle vom Microsoft Edge Browser unterstützten Richtlinien
ms.openlocfilehash: d785ab4a06a6972dcc8d85b560bbae5049c9d314
ms.sourcegitcommit: dd8cdbd35726c795ddce917e549ddf17ee7f5290
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/11/2022
ms.locfileid: "12473601"
---
# <a name="microsoft-edge-webview2---policies"></a>Microsoft Edge WebView2 –⁠ Richtlinien

Die neueste Version von Microsoft Edge WebView2 umfasst die folgenden Richtlinien. Sie können diese Richtlinien verwenden, um zu konfigurieren, wie Microsoft Edge WebView2 in Ihrer Organisation ausgeführt wird.

Informationen zu einer zusätzlichen Richtlinie, mit der Sie steuern können, wie und wann Microsoft Edge WebView2 aktualisiert wird, finden Sie unter [Microsoft Edge Updaterichtlinien-Referenz](microsoft-edge-update-policies.md).


> [!NOTE]
> Dieser Artikel bezieht sich auf Microsoft Edge Version 87 oder neuer.

## <a name="available-policies"></a>Verfügbare Richtlinien

In dieser Tabelle sind sämtliche, in dieser Version von Microsoft Edge WebView2 verfügbaren Gruppenrichtlinien aufgeführt. Über die Links in der folgenden Tabelle erhalten Sie weitere Einzelheiten zu bestimmten Richtlinien.

- [Einstellungen für Loader-Außerkraftsetzung](#loader-override-settings)
- [Sonstiges](#additional)


### [*<a name="loader-override-settings"></a>Einstellungen für Loader-Außerkraftsetzung*](#loader-override-settings-policies)

|Richtlinienname|Beschriftung|
|-|-|
|[BrowserExecutableFolder](#browserexecutablefolder)|Konfigurieren des Speicherorts des ausführbaren Browser-Ordners|
|[ReleaseChannelPreference](#releasechannelpreference)|Einstellen der Präferenz für die Suchreihenfolge der Veröffentlichungskanäle|
### [*<a name="additional"></a>Sonstiges*](#additional-policies)

|Richtlinienname|Beschriftung|
|-|-|
|[ExperimentationAndConfigurationServiceControl](#experimentationandconfigurationservicecontrol)|Steuern der Kommunikation mit dem Experimentier- und Konfigurationsservice|




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

  ## <a name="additional-policies"></a>Weitere Richtlinien

  [Zurück zum Anfang](#microsoft-edge-webview2---policies)

  ### <a name="experimentationandconfigurationservicecontrol"></a>ExperimentationAndConfigurationServiceControl

  #### <a name="control-communication-with-the-experimentation-and-configuration-service"></a>Steuern der Kommunikation mit dem Experimentier- und Konfigurationsservice

  
  
  #### <a name="supported-versions"></a>Unterstützte Versionen:

  - Unter Windows ab 97 oder höher

  #### <a name="description"></a>Beschreibung

  Der Experimentier- und Konfigurationsservice wird verwendet, um Experimentier- und Konfigurationsnutzlasten für den Client bereitzustellen.

Die Experimentier-Nutzlast besteht aus einer Liste von Funktionen in Frühstadien der Entwicklung, die Microsoft zu Test- und Feedbackzwecken aktiviert.

Die Konfigurationsnutzlast besteht aus einer Liste von empfohlenen Einstellungen, die Microsoft bereitstellen möchte, um die Benutzererfahrung zu optimieren.

Die Konfigurationsnutzlast kann auch eine Liste der Aktionen enthalten, die aus Kompatibilitätsgründen für bestimmte Domänen ausgeführt werden sollen. Beispielsweise kann der Browser die Zeichenfolge des Benutzer-Agenten auf einer Website überschreiben, wenn diese Website beschädigt ist. Jede dieser Aktionen soll temporär sein, während Microsoft versucht, das Problem mit dem Websitebesitzer zu beheben.

Wenn Sie diese Richtlinie auf „FullMode“ setzen, wird die vollständige Nutzlast aus dem Experimentier- und Konfigurationsservice heruntergeladen. Dies umfasst sowohl die Test- als auch die Konfigurationsnutzlast.

Wenn Sie diese Richtlinie auf „ConfigurationsOnlyMode“ setzen, wird nur die Konfigurationsnutzlast heruntergeladen.

Wenn Sie diese Richtlinie auf „RestrictedMode“ setzen, wird die Kommunikation mit dem Experimentier- und Konfigurationsservice vollständig gestoppt. Microsoft empfiehlt diese Einstellung nicht.

Wenn Sie diese Richtlinie auf einem verwalteten Gerät nicht konfigurieren, ist das Verhalten auf Beta- und Stable-Kanälen identisch mit dem „ConfigurationsOnlyMode“. In Canary- und Dev-Kanälen ist das Verhalten identisch mit dem „FullMode“.

Wenn Sie diese Richtlinie auf einem nicht verwalten Gerät nicht konfigurieren, ist das Verhalten identisch mit dem „FullMode“.

Zuordnung von Richtlinienoptionen:

* FullMode (2) = Abrufen von Konfigurationen und Experimenten

* ConfigurationsOnlyMode (1) = Nur Konfigurationen abrufen

* RestrictedMode (0) = Kommunikation mit dem Experimentier- und Konfigurationsservice deaktivieren

Verwenden Sie die vorstehenden Informationen, wenn Sie diese Richtlinie konfigurieren.

  #### <a name="supported-features"></a>Unterstützte Funktionen:

  - Kann zwingend erforderlich sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### <a name="data-type"></a>Datentyp:

  - Ganze Zahl

  #### <a name="windows-information-and-settings"></a>Windows-Informationen und -Einstellungen

  ##### <a name="group-policy-admx-info"></a>Informationen zur Gruppenrichtlinie (ADMX)

  - GP eindeutiger Name: ExperimentationAndConfigurationServiceControl
  - GP-Name: Steuern der Kommunikation mit dem Experimentier- und Konfigurationsservice
  - GP-Pfad (verpflichtend): Administrative Vorlagen/Microsoft Edge WebView2/
  - GP Pfad (Empfohlen): n.a.
  - Name der GP-ADMX-Datei: MSEdgeWebView2.admx

  ##### <a name="windows-registry-settings"></a>Windows-Registrierungseinstellungen

  - Pfad (verpflichtend): SOFTWARE\Policies\Microsoft\Edge\WebView2
  - Pfad (Empfohlen): n.a.
  - Wertname: ExperimentationAndConfigurationServiceControl
  - Werttyp: REG_DWORD

  ##### <a name="example-value"></a>Beispielwert:

```
0x00000002
```

  

  [Zurück zum Anfang](#microsoft-edge-webview2---policies)


## <a name="see-also"></a>Weitere Informationen

- [Konfigurieren von Microsoft Edge](configure-microsoft-edge.md)
- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)
- [Microsoft Sicherheitsbaselines-Blog](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/bg-p/Microsoft-Security-Baselines)