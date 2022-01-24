---
title: Konfigurieren von Microsoft Edge mithilfe von Tools für die mobile Geräteverwaltung
ms.author: kvice
author: dan-wesley
manager: laurawi
ms.date: 11/17/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Konfigurieren Sie Microsoft Edge mithilfe von Tools für die mobile Geräteverwaltung.
ms.openlocfilehash: 96fa6f4d096d8acd5369b92de7e1d979191e13ec
ms.sourcegitcommit: e7f3098d8b7d91cae20b5778a71a87daababc312
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2022
ms.locfileid: "12297733"
---
# <a name="configure-microsoft-edge-using-mobile-device-management"></a>Konfigurieren von Microsoft Edge mithilfe von Tools für die mobile Geräteverwaltung

In diesem Artikel wird erläutert, wie Sie Microsoft Edge auf Windows 10 mithilfe der [mobilen Geräteverwaltung (MOBILE Device Management, MDM)](/windows/client-management/mdm/) mit [ADMX-Aufnahme](/windows/client-management/mdm/win32-and-centennial-app-policy-configuration)konfigurieren. Weitere Inhalte dieses Artikels:

- [Erstellen von Open Mobile Alliance Uniform Resource Identifier (OMA-URI) für Microsoft Edge-Richtlinien](#create-an-oma-uri-for-microsoft-edge-policies).
- [Konfigurieren von Microsoft Edge in Intune mithilfe der ADMX-Aufnahme und benutzerdefinierter OMA-URI](#configure-microsoft-edge-in-intune-using-admx-ingestion).

> [!NOTE]
> Dieser Artikel bezieht sich auf Microsoft Edge Version 77 oder höher.

## <a name="prerequisites"></a>Voraussetzungen

Windows 10, mit den folgenden Mindestvoraussetzungen:

- Windows 10, Version 1903, mit Installation von [KB4512941](https://support.microsoft.com/help/4512941/) und [KB4517211](https://support.microsoft.com/help/4517211/)
- Windows 10, Version 1809, mit Installation von [KB4512534](https://support.microsoft.com/help/4512534/) und [KB4520062](https://support.microsoft.com/help/4520062/)
- Windows 10, Version 1803, mit Installation von [KB4512509](https://support.microsoft.com/help/4512509/) und [KB4519978](https://support.microsoft.com/help/4519978)
- Windows 10, Version 1709, mit Installation von [KB4516071](https://support.microsoft.com/help/4516071/) und [KB4520006](https://support.microsoft.com/help/4520006)

## <a name="overview"></a>Übersicht

Sie können Microsoft Edge auf Windows 10 mithilfe von MDM mit dem bevorzugten Enterprise Mobility Management (EMM)- oder MDM-Anbieter konfigurieren, der die [ADMX-Aufnahme](/windows/client-management/mdm/win32-and-centennial-app-policy-configuration) unterstützt.

Das Konfigurieren von Microsoft Edge mit MDM besteht aus zwei Schritten:

1. Aufnehmen der Microsoft Edge ADMX-Datei in Ihren EMM- oder MDM-Anbieter. Anweisungen zum Aufnehmen einer ADMX-Datei erhalten Sie von Ihrem Anbieter.

   > [!NOTE]
   > Informationen zu Microsoft Intune finden Sie unter [Konfigurieren von Microsoft Edge in Intune mithilfe der ADMX-Aufnahme](#configure-microsoft-edge-in-intune-using-admx-ingestion).

2. [Erstellen eines OMA-URI für eine Microsoft Edge-Richtlinie](#create-an-oma-uri-for-microsoft-edge-policies)

## <a name="create-an-oma-uri-for-microsoft-edge-policies"></a>Erstellen eines OMA-URI für Microsoft Edge-Richtlinien

In den folgenden Abschnitten wird beschrieben, wie Sie den OMA-URI-Pfad erstellen und den Wert im XML-Format für obligatorische und empfohlene Browserrichtlinien suchen und definieren.

Laden Sie vor den ersten Schritten die Datei Microsoft Edge Richtlinienvorlagen (MicrosoftEdgePolicyTemplates.cab) von der [Microsoft Edge Enterprise Zielseite](https://aka.ms/EdgeEnterprise) herunter, und extrahieren Sie den Inhalt.

Es gibt drei Schritte zum Definieren des OMA-URI:

1. [Erstellen des OMA-URI-Pfads](#create-the-oma-uri-path)
2. [Angabe des OMA-URI-Datentyps](#specify-the-data-type)
3. [Festlegen des OMA-URI-Werts](#set-the-value-for-a-browser-policy)

### <a name="create-the-oma-uri-path"></a>Erstellen des OMA-URI-Pfads

Verwenden Sie die folgende Formel als Leitfaden zum Erstellen der OMA-URI-Pfade. <br/><br/>
*`./Device/Vendor/MSFT/Policy/Config/<ADMXIngestName>~Policy~<ADMXNamespace>~<ADMXCategory>/<PolicyName>`* <br/><br/>

| Parameter         | Beschreibung                                                                                   |
|-------------------|-----------------------------------------------------------------------------------------------|
| \<ADMXIngestName> | Verwenden Sie „Edge” oder das, was Sie beim Aufnehmen der administrativen Vorlage definiert haben. Wenn Sie z. B. „./Device/Vendor/MSFT/Policy/ConfigOperations/ADMXInstall/MicrosoftEdge/Policy/EdgeAdmx” verwendet haben, verwenden Sie „MicrosoftEdge”.<br/><br/> Der `<ADMXIngestionName>` muss mit jenem übereinstimmen, den Sie beim Aufnehmen der ADMX-Datei verwendet haben. |
| \<ADMXNamespace>  | Entweder „microsoft_edge” oder „microsoft_edge_recommended”, je nachdem, ob Sie eine obligatorische oder empfohlene Richtlinie festlegen. |
| \<ADMXCategory>   | Die „parentCategory” der Richtlinie wird in der ADMX-Datei definiert. Lassen Sie `<ADMXCategory>` aus, wenn die Richtlinie nicht gruppiert ist (keine „parentCategory” definiert). |
| \<PolicyName>     | Den Richtliniennamen finden Sie im Referenzartikel [](./microsoft-edge-policies.md) zur Browserrichtlinie. |

#### <a name="uri-path-example"></a>URI-Pfadbeispiel:

In diesem Beispiel wird davon ausgegangen, dass der Name des `<ADMXIngestName>`-Knotens „Edge” lautet, und Sie eine obligatorische Richtlinie festlegen. Der URI-Pfad wäre demnach:<br/><br/>
*`./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~<ADMXCategory>/<PolicyName>`*

Wenn sich die Richtlinie nicht in einer Gruppe befindet (z. B. DiskCacheSize), entfernen Sie „`~<ADMXCategory>`”. Ersetzen Sie `<PolicyName>` durch den Namen der Richtlinie, DiskCacheSize. Der URI-Pfad wäre demnach:<br/><br/>
*`./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge/DiskCacheSize`*

Wenn sich die Richtlinie in einer Gruppe befindet, führen Sie die folgenden Schritte aus:

1. Öffnen Sie **msedge.admx** mit einem beliebigen XML-Editor.
2. Suchen Sie nach dem Richtliniennamen, den Sie festlegen möchten. Zum Beispiel „ExtensionInstallForceList”.
3. Verwenden Sie den Wert des *ref*-Attributs aus dem *parentCategory*-Element. Zum Beispiel „Erweiterungen“ aus \<parentCategory ref=" Extensions"/>.
4. Ersetzen Sie `<ADMXCategory>` durch den *ref*-Attributwert, um den URI-Pfad zu erstellen. Der URI-Pfad wäre demnach:<br/><br/>
*`/Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Extensions/ExtensionInstallForcelist`*

### <a name="specify-the-data-type"></a>Angabe des Datentyps

Der OMA-URI-Datentyp lautet immer "String".

### <a name="set-the-value-for-a-browser-policy"></a>Festlegen des Werts für eine Browserrichtlinie

In diesem Abschnitt wird beschrieben, wie Sie den Wert im XML-Format für jeden Datentyp festlegen. Wechseln Sie zur [Browserrichtlinien-Referenz](./microsoft-edge-policies.md), um nach dem Datentyp der Richtlinie zu suchen.

> [!NOTE]
> Bei nicht-booleschen Datentypen beginnt der Wert immer mit `<enabled/>`.

#### <a name="boolean-data-type"></a>Boolescher Datentyp

Verwenden Sie für Richtlinien des booleschen Typs `<enabled/>` oder `<disabled/>`.

#### <a name="integer-data-type"></a>Datentyp „Ganze Zahl”

Der Wert muss immer mit dem `<enabled/>`-Element gefolgt von `<data id="[valueName]" value="[decimal value]"/>` beginnen.

Führen Sie die folgenden Schritte aus, um den Wertnamen und den Dezimalwert für eine neue Registerkartenseite zu finden:

1. Öffnen Sie **msedge.admx** mit einem beliebigen XML-Editor.
2. Suchen Sie nach dem `<policy>`-Element, bei dem das Namensattribut mit dem Richtliniennamen übereinstimmt, den Sie festlegen möchten. Suchen Sie für „RestoreOnStartup” nach `name="RestoreOnStartup"`.
3. Suchen Sie im `<elements>`-Knoten nach dem Wert, den Sie festlegen möchten.
4. Verwenden Sie den Wert im „valueName”-Attribut im `<elements>`-Knoten. Für „RestoreOnStartup” lautet der „valueName” „RestoreOnStartup”.
5. Verwenden Sie den Wert im „value”-Attribut im `<decimal>`-Knoten. Damit „RestoreOnStartup” die neue Registerkartenseite öffnet, lautet der Wert „5”.

So öffnen Sie die neue Registerkartenseite beim Start:<br>
`<enabled/> <data id="RestoreOnStartup" value="5"/>`

#### <a name="list-of-strings-data-type"></a>Liste der Datentypen „Zeichenfolge”

Der Wert muss immer mit dem `<enabled/>`-Element gefolgt von `<data id="[listID]" value="[string 1];[string 2];[string 3]"/>` beginnen.

> [!NOTE]
> Der Attributname „id =” ist nicht der Richtlinienname, obwohl er in den meisten Fällen mit dem Richtliniennamen übereinstimmt. Dies ist der Knoten-ID-Attributwert \<list>, der in der ADMX-Datei enthalten ist.

Gehen Sie folgendermaßen vor, um nach der listID zu suchen und den Wert zum Blockieren einer URL zu definieren:

1. Öffnen Sie **msedge.admx** mit einem beliebigen XML-Editor.
2. Suchen Sie nach dem `<policy>`-Element, bei dem das Namensattribut mit dem Richtliniennamen übereinstimmt, den Sie festlegen möchten. Suchen Sie für „URLBlocklist” nach `name="URLBlocklist"`.
3. Verwenden Sie den Wert im „id”-Attribut von `<list> node for [listID]`.
4. Der "Wert" ist eine durch ein Semikolon (;) getrennte Liste von URLs.

Gehen Sie folgendermaßen vor, um z. B. den Zugriff auf `contoso.com` und `https://ssl.server.com` zu blockieren:<br>
`<enabled/> <data id=" URLBlocklistDesc" value="contoso.com;https://ssl.server.com"/>`

#### <a name="dictionary-or-string-data-type"></a>Datentyp „Dictionary” oder „Zeichenfolge”

Der Wert muss immer mit `<enabled/>` gefolgt von `<data id="[textID]" value="[string]"/>` beginnen.

Gehen Sie folgendermaßen vor, um nach der textID zu suchen und den Wert zum Festlegen des Gebietsschemas zu definieren:

1. Öffnen Sie **msedge.admx** mit einem beliebigen XML-Editor.
2. Suchen Sie nach dem `<policy>`-Element, bei dem das Namensattribut mit dem Richtliniennamen übereinstimmt, den Sie festlegen möchten. Suchen Sie für „ApplicationLocaleValue” nach `name="ApplicationLocaleValue"`.
3. Verwenden Sie den Wert im „id”-Attribut von `<text>`-Knoten für `[textID]`.
4. Setzen Sie den „Wert” auf den Kulturcode.

So legen Sie das Gebietsschema mit der Richtlinie „ApplicationLocaleValue” auf „en-US” fest:<br>
`<enabled/> <data id="ApplicationLocaleValue" value="es-US"/>`

Wörterbuch-Datentypen werden als große Zeichenfolgen behandelt, benötigen jedoch normalerweise zeichenfolgenausweichende Zeichenfolgen, um den Wert in das richtige Formular zu erhalten.

Wenn Sie z. B. die ManagedFavorites-Richtlinie festlegen möchten, lautet der Wert:

```xml
<enabled/> <data id="ManagedFavorites" value="[{&quot;toplevel_name&quot;: &quot;My managed favorites folder&quot;}, {&quot;name&quot;: &quot;Microsoft&quot;, &quot;url&quot;: &quot;microsoft.com&quot;}, {&quot;name&quot;: &quot;Bing&quot;, &quot;url&quot;: &quot;bing.com&quot;}, {&quot;children&quot;: [{&quot;name&quot;: &quot;Microsoft Edge Insiders&quot;, &quot;url&quot;: &quot;www.microsoftedgeinsider.com&quot;}, {&quot;name&quot;: &quot;Microsoft Edge&quot;, &quot;url&quot;: &quot;www.microsoft.com/windows/microsoft-edge&quot;}], &quot;name&quot;: &quot;Microsoft Edge links&quot;}]"/>
```

### <a name="create-the-oma-uri-for-recommended-policies"></a>Erstellen des OMA-URI für empfohlene Richtlinien

Die Definition des URI-Pfads für empfohlene Richtlinien hängt von der zu konfigurierenden Richtlinie ab.

#### <a name="to-define-the-uri-path-for-a-recommended-policy"></a>So definieren Sie den URI-Pfad für eine empfohlene Richtlinie

Verwenden Sie die URI-Pfadformel (*`./Device/Vendor/MSFT/Policy/Config/<ADMXIngestName>~Policy~<ADMXNamespace>~<ADMXCategory>/<PolicyName>`*) und führen Sie die folgenden Schritte aus, um den URI-Pfad zu definieren:
1. Öffnen Sie **msedge.admx** mit einem beliebigen XML-Editor.
2. Wenn die Richtlinie, die Sie konfigurieren möchten, nicht in einer Gruppe ist, fahren Sie mit Schritt 4 fort, und entfernen Sie `~<ADMXCategory>` aus dem Pfad.
3. Wenn die Richtlinie, die Sie konfigurieren möchten, in einer Gruppe ist:

   - Um nach `<ADMXCategory>` zu suchen, suchen Sie nach der Richtlinie, die Sie festlegen möchten. Fügen Sie beim Suchen „_recommended” an den Richtliniennamen an. Eine Suche nach „RegisteredProtocolHandlers_recommended” gibt beispielsweise folgendes Ergebnis zurück:

        ```xml
         <policy class="Both" displayName="$(string.RegisteredProtocolHandlers)" explainText="$(string.RegisteredProtocolHandlers_Explain)" key="Software\Policies\Microsoft\Edge\Recommended" name="RegisteredProtocolHandlers_recommended" presentation="$(presentation.RegisteredProtocolHandlers)">
           <parentCategory ref="ContentSettings_recommended"/>
           <supportedOn ref="SUPPORTED_WIN7_V77"/>
           <elements>
             <text id="RegisteredProtocolHandlers" maxLength="1000000" valueName="RegisteredProtocolHandlers"/>
           </elements>
         </policy>
        ```

   - Kopieren Sie den Wert des *ref*-Attributs aus dem `<parentCategory>`-Element. Kopieren Sie für „ContentSettings” „ContentSettings_recommended” aus `<parentCategory ref=" ContentSettings_recommended"/>`.
   - Ersetzen Sie `<ADMXCategory>` durch den *ref*-Attributwert, um den URI-Pfad in der URI-Pfadformel zu erstellen.

4. `<PolicyName>` ist der Name der Richtlinie, an die „_recommended” angefügt ist.

#### <a name="oma-uri-path-examples-for-recommended-policies"></a>OMA-URI-Pfadbeispiele für empfohlene Richtlinien

In der folgenden Tabelle sind Beispiele für OMA-URI-Pfade für empfohlene Richtlinien aufgeführt.

|      Richtlinie    |   OMA-URI  |
|-----------------------------------|------------------------------------------|
| [RegisteredProtocolHandlers](./microsoft-edge-policies.md#registeredprotocolhandlers)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~ContentSettings_recommended/RegisteredProtocolHandlers_recommended`                        |
| [PasswordManagerEnabled](./microsoft-edge-policies.md#passwordmanagerenabled)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~PasswordManager_recommended/PasswordManagerEnabled_recommended`                        |
| [PrintHeaderFooter](./microsoft-edge-policies.md#printheaderfooter)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~Printing_recommended/PrintHeaderFooter_recommended`                        |
| [SmartScreenEnabled](./microsoft-edge-policies.md#smartscreenenabled)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~SmartScreen_recommended/SmartScreenEnabled_recommended`                        |
| [HomePageLocation](./microsoft-edge-policies.md#homepagelocation)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~Startup_recommended/HomepageLocation_recommended`                        |
| [ShowHomeButton](./microsoft-edge-policies.md#showhomebutton)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~Startup_recommended/ShowHomeButton_recommended`                        |
| [FavoritesBarEnabled](./microsoft-edge-policies.md#favoritesbarenabled)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~/FavoritesBarEnabled_recommended`                        |

### <a name="oma-uri-examples"></a>OMA-URI-Beispiele

OMA-URI-Beispiele mit ihrem URI-Pfad, Typ und einem Beispielwert.

#### <a name="boolean-data-type-examples"></a>Boolescher Datentyp-Beispiele

*[ShowHomeButton](./microsoft-edge-policies.md#showhomebutton):*

| Feld   | Wert                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Name    | Microsoft Edge: ShowHomeButton                                                       |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Startup/ShowHomeButton` |
| Typ    | Zeichenfolge                                                                               |
| Wert   | `<enabled/>`                                                                          |

*[DefaultSearchProviderEnabled](./microsoft-edge-policies.md#defaultsearchproviderenabled):*

| Feld   | Wert                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Name    | Microsoft Edge: DefaultSearchProviderEnabled                                         |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~DefaultSearchProvider/DefaultSearchProviderEnabled`    |
| Typ    | Zeichenfolge                                                                               |
| Wert   | `<disable/>`                                                                          |

### <a name="integer-data-type-examples"></a>Datentyp „Ganze Zahl”-Beispiele

*[AutoImportAtFirstRun](./microsoft-edge-policies.md#autoimportatfirstrun):*

| Feld   | Wert                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Name    | Microsoft Edge: AutoImportAtFirstRun                                                 |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge/AutoImportAtFirstRun`   |
| Typ    | Zeichenfolge                                                                               |
| Wert   | `<enabled/><data id="AutoImportAtFirstRun" value="1"/>`                             |

*[DefaultImagesSetting](./microsoft-edge-policies.md#defaultimagessetting):*

| Feld   | Wert                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Name    | Microsoft Edge: DefaultImagesSetting                                                 |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~ContentSettings/DefaultImagesSetting`    |
| Typ    | Zeichenfolge                                                                               |
| Wert   | `<enabled/><data id="DefaultImagesSetting" value="2"/>`                             |

*[DiskCacheSize](./microsoft-edge-policies.md#diskcachesize):*

| Feld   | Wert                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Name    | Microsoft Edge: DiskCacheSize                                                        |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge/DiskCacheSize`        |
| Typ    | Zeichenfolge                                                                               |
| Wert   | `<enabled/><data id="DiskCacheSize" value="1000000"/>`                               |

#### <a name="list-of-strings-data-type-examples"></a>Liste der Beispiele für den Datentyp „Zeichenfolge”

*[RestoreOnStartupURLS](./microsoft-edge-policies.md#restoreonstartupurls):*

| Feld   | Wert                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Name    | Microsoft Edge: RestoreOnStartupURLS                                                 |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Startup/RestoreOnStartupURLs`    |
| Typ    | Zeichenfolge                                                                               |
| Wert   | `<enabled/><data id="RestoreOnStartupURLsDesc" value="1&#xF000;http://www.bing.com"/>`<br>Für mehrere Listenelemente: `<enabled/><data id="RestoreOnStartupURLsDesc" value="1&#xF000;http://www.bing.com&#xF000;2&#xF000;http://www.microsoft.com"/>`  |

*[ExtensionInstallForcelist](./microsoft-edge-policies.md#extensioninstallforcelist):*

| Feld   | Wert                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Name    | Microsoft Edge: ExtensionInstallForcelist                                            |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Extensions/ExtensionInstallForcelist`    |
| Typ    | Zeichenfolge                                                                               |
| Wert   | `<enabled/><data id="ExtensionInstallForcelistDesc" value="1&#xF000;gbchcmhmhahfdphkhkmpfmihenigjmpp;https://extensionwebstorebase.edgesv.net/v1/crx"/>`                               |

#### <a name="dictionary-and-string-data-type-examples"></a>Beispiele für Wörterbuch- und Zeichenfolgen-Datentypen

*[ProxyMode](./microsoft-edge-policies.md#proxymode):*

| Feld   | Wert      |
|---------|------------|
| Name    | Microsoft Edge: ProxyMode                                                            |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~ProxyMode/ProxyMode`  |
| Typ    | Zeichenfolge                                                                               |
| Wert   | `<enabled/><data id="ProxyMode" value="auto_detect"/>`                               |

*[ManagedFavorites](./microsoft-edge-policies.md#managedfavorites):*

| Feld   | Wert    |
|---------|----------|
| Name    | Microsoft Edge: ManagedFavorites                                                            |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge/ManagedFavorites`  |
| Typ    | Zeichenfolge                                                                               |
| Wert   | `<enabled/> <data id="ManagedFavorites" value="[{&quot;toplevel_name&quot;: &quot;My managed favorites folder&quot;}, {&quot;name&quot;: &quot;Microsoft&quot;, &quot;url&quot;: &quot;microsoft.com&quot;}, {&quot;name&quot;: &quot;Bing&quot;, &quot;url&quot;: &quot;bing.com&quot;}, {&quot;children&quot;: [{&quot;name&quot;: &quot;Microsoft Edge Insiders&quot;, &quot;url&quot;: &quot;www.microsoftedgeinsider.com&quot;}, {&quot;name&quot;: &quot;Microsoft Edge&quot;, &quot;url&quot;: &quot;www.microsoft.com/windows/microsoft-edge&quot;}], &quot;name&quot;: &quot;Microsoft Edge links&quot;}]"/>`                               |

## <a name="configure-microsoft-edge-in-intune-using-admx-ingestion"></a>Konfigurieren von Microsoft Edge in Intune mithilfe der ADMX-Aufnahme

Die empfohlene Methode zum Konfigurieren von Microsoft Edge mit Microsoft Intune ist die Verwendung des Profils "Administrative Vorlagen". Dieses Profil wird unter [Konfigurieren Microsoft Edge Richtlinieneinstellungen mit Microsoft Intune](./configure-edge-with-intune.md)beschrieben. Wenn Sie eine Richtlinie auswerten möchten, die derzeit nicht in den Microsoft Edge Administrative Vorlagen in Intune verfügbar ist, können Sie Microsoft Edge mithilfe [von benutzerdefinierten Einstellungen für Windows 10 Geräte in Intune](/intune/configuration/custom-settings-windows-10)konfigurieren.

In diesem Abschnitt wird das Verwenden von Hintergrundaufgaben beschrieben.

1. [Aufnehmen der Microsoft Edge ADMX-Datei in Intune](#ingest-the-microsoft-edge-admx-file-into-intune)
2. [Festlegen einer Richtlinie mit benutzerdefiniertem OMA-URI in Intune](#set-a-policy-using-custom-oma-uri-in-intune)

> [!IMPORTANT]
> Verwenden Sie als bewährte Methode kein benutzerdefiniertes OMA-URI-Profil und kein administratives Vorlagenprofil, um dieselbe Microsoft Edge-Einstellung in Intune zu konfigurieren. Wenn Sie die gleiche Richtlinie mit einem benutzerdefinierten OMA-URI und einem administrativen Vorlagenprofil, aber mit unterschiedlichen Werten bereitstellen, erhalten Benutzer unvorhersehbare Ergebnisse. Es wird dringend empfohlen, das OMA-URI-Profil zu entfernen, bevor Sie ein administratives Vorlagenprofil verwenden.

### <a name="ingest-the-microsoft-edge-admx-file-into-intune"></a>Aufnehmen der Microsoft Edge ADMX-Datei in Intune

In diesem Abschnitt wird beschrieben, wie die Microsoft Edge administrative Vorlage (**msedge.admx**-Datei) in Intune aufgenommen wird.

> [!WARNING]
> Ändern Sie die ADMX-Datei nicht, bevor Sie sie aufnehmen.

Führen Sie die folgenden Schritte aus, um die ADMX-Datei aufzunehmen:

1. Laden Sie die Microsoft Edge-Richtlinienvorlagendatei (MicrosoftEdgePolicyTemplates.cab) von der [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise) herunter und extrahieren Sie den Inhalt. Die Datei, die Sie aufnehmen möchten, ist **msedge.admx**.
2. Melden Sie sich beim [Microsoft Azure-Portal](https://portal.azure.com)an.
3. Wählen Sie **Intune** aus _Alle Dienste_ aus, oder suchen Sie im Suchfeld des Portals nach Intune.
4. Wählen Sie aus _Microsoft Intune – Übersicht_ **Gerätekonfiguration** | **Profile** aus.
5. Wählen Sie in der oberen Befehlsleiste **+ Profil erstellen** aus.

   ![Erstellen eines Marketingprofils](./media/edge-cfg-with-mdm/configure-edge-mdm-intune-create-profile.png)

6. Geben Sie die folgenden Profilinformationen an:

   - **Name**: Geben Sie einen aussagekräftigen Namen ein. In diesem Beispiel „Microsoft Edge – aufgenommene ADMX-Konfiguration”.
   - **Beschreibung**: Geben Sie eine optionale Beschreibung für das Profil ein.
   - **Plattform**: Wählen Sie „Windows 10 und höher” aus.
   - **Profiltyp**: Wählen Sie „Benutzerdefiniert” aus.

7. Klicken Sie unter **Benutzerdefinierte OMA-URI-Einstellungen** auf **Hinzufügen**, um eine ADMX-Aufnahme hinzuzufügen.

   ![Hinzufügen der Aufnahme für OMA-URI](./media/edge-cfg-with-mdm/configure-edge-mdm-intune-create-profile-add-omauri.png)

8. Geben Sie unter **Zeile hinzufügen** die folgenden Informationen an:

   - **Name**: Geben Sie einen aussagekräftigen Namen ein. In diesem Beispiel verwenden Sie „Microsoft Edge – ADMX-Aufnahme”.
   - **Beschreibung**: Geben Sie eine optionale Beschreibung für die Einstellung ein.
   - **OMA-URI**: Geben Sie „*./Device/Vendor/MSFT/Policy/ConfigOperations/ADMXInstall/Edge/Policy/EdgeAdmx*” ein.
   - **Datentyp**: Wählen Sie „Zeichenfolge” aus.
   - **Wert**: Dieser Eingabebereich wird angezeigt, nachdem Sie den **Datentyp** ausgewählt haben. Öffnen Sie die Datei „msedge.admx” aus der Microsoft Edge-Richtlinienvorlagendatei, die Sie in Schritt 1 extrahiert haben. Kopieren Sie den **GESAMTEN Text** aus der Datei „msedge.admx”, und fügen Sie ihn in den Textbereich **Wert** ein, der im folgenden Screenshot gezeigt wird.

        ![Hinzufügen einer ADMX-Aufnahme](./media/edge-cfg-with-mdm/configure-edge-intune-mdm-omauri-addrow-ingest.png)

   - Klicken Sie auf **OK**.

9. Klicken Sie unter **Benutzerdefinierte OMA-URI-Einstellungen** auf **OK**.
10. Klicken Sie unter **Profil erstellen** auf **Erstellen**. Im nächsten Screenshot werden Informationen zum neu erstellten Profil angezeigt.

    ![Neue Geräteprofilinformationen ](./media/edge-cfg-with-mdm/configure-edge-mdm-intune-create-profile-done.png)

<!--
> [!NOTE]
> You can use the preceding steps to ingest the msedgeupate.admx policy template file.
-->
### <a name="set-a-policy-using-custom-oma-uri-in-intune"></a>Festlegen einer Richtlinie mit benutzerdefiniertem OMA-URI in Intune

> [!NOTE]
> Bevor Sie die Schritte in diesem Abschnitt ausführen, müssen Sie die unter [Aufnehmen der Microsoft Edge ADMX-Datei in Intune](#ingest-the-microsoft-edge-admx-file-into-intune) beschriebenen Schritte ausführen.

1. Melden Sie sich beim [Microsoft Azure-Portal](https://portal.azure.com)an.
2. Wählen Sie **Intune** aus _Alle Dienste_ aus, oder suchen Sie im Suchfeld des Portals nach Intune.
3. Wechseln Sie zu **Intune**>**Gerätekonfiguration**>**Profile**.
4. Wählen sie das Profil „Microsoft Edge – aufgenommene ADMX-Konfiguration” oder den Namen aus, den Sie für das Profil verwendet haben.
5. Um Microsoft Edge-Richtlinieneinstellungen hinzuzufügen, müssen Sie **Benutzerdefinierte OMA-URI-Einstellungen** öffnen. Klicken Sie unter **Verwalten** auf **Eigenschaften** und anschließend auf **Einstellungen**.

    ![Konfigurieren von Profileinstellungen](./media/edge-cfg-with-mdm/configure-edge-mdm-intune-add-policy-settings.png)

6. Klicken Sie unter **OMA-URI-Einstellungen** auf **Hinzufügen**.

    ![Hinzufügen von Zeilen zu den OMA-URI-Einstellungen](./media/edge-cfg-with-mdm/configure-edge-mdm-intune-add-policy-settings-add-row.png)

7. Geben Sie unter **Zeile hinzufügen** die folgenden Informationen an:

   - **Name**: Geben Sie einen aussagekräftigen Namen ein. Es wird empfohlen, den zu konfigurierenden Richtliniennamen zu verwenden. In diesem Beispiel verwenden Sie „ShowHomeButton“.
   - **Beschreibung** (optional): Geben Sie eine Beschreibung für die Einstellung ein.
   - **OMA-URI**: Geben Sie den OMA-URI für die Richtlinie ein. Verwenden Sie für die „ShowHomeButton”-Richtlinie als Beispiel diese Zeichenfolge: „*./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Startup/ShowHomeButton*”
   - **Datentyp**: Wählen Sie den Datentyp „Richtlinieneinstellungen” aus. Verwenden Sie für die „ShowHomeButton”-Richtlinie „Zeichenfolge”.
   - **Wert**: Geben Sie die Einstellung ein, die Sie für die Richtlinie konfigurieren möchten. Geben Sie für das Beispiel „ShowHomeButton” „\<enabled/>” ein. Der folgende Screenshot zeigt die Einstellungen zum Konfigurieren einer Richtlinie.

        ![Hinzufügen von Zeilen, Benutzerdefinierte OMA-URI-Einstellungen](./media/edge-cfg-with-mdm/configure-edge-mdm-custom-omauri-setting.png)

   - Klicken Sie auf **OK**.

8. Klicken Sie unter **Benutzerdefinierte OMA-URI-Einstellungen** auf **OK**.
9. Klicken Sie im Profil „**Microsoft Edge – aufgenommene ADMX-Konfiguration – Eigenschaften**” (oder dem Namen, den Sie verwendet haben) auf **Speichern**.

Nachdem das Profil erstellt und die Eigenschaften festgelegt wurden, müssen Sie [das Profil in Microsoft Intune zuweisen](/intune/configuration/device-profile-assign).

#### <a name="confirm-that-the-policy-was-set"></a>Bestätigen der Festlegung der Richtlinie

Gehen Sie wie folgt vor, um zu bestätigen, dass die Microsoft Edge-Richtlinie das von Ihnen erstellte Profil verwendet. (Geben Sie Microsoft Intune Zeit, die Richtlinie an ein Gerät weiterzugeben, das Sie im Profilbeispiel „Microsoft Edge – aufgenommene ADMX-Konfiguration” zugewiesen haben.)

1. Öffnen Sie Microsoft Edge und wechseln Sie zu *edge://policy*.
2. Überprüfen Sie auf der Seite **Richtlinien**, ob die im Profil festgelegte Richtlinie aufgelistet ist.
3. Wenn Ihre Richtlinie nicht angezeigt wird, finden Sie unter [Diagnostizieren von MDM-Fehlern in Windows 10](/windows/client-management/mdm/diagnose-mdm-failures-in-windows-10) oder [Problembehandlung bei einer Richtlinieneinstellung](#troubleshoot-a-policy-setting) weitere Informationen.

#### <a name="troubleshoot-a-policy-setting"></a>Problembehandlung bei einer Richtlinieneinstellung

Wenn eine Microsoft Edge-Richtlinie nicht wirksam wird, führen Sie die folgenden Schritte aus:

Öffnen Sie die Seite *edge://policy* auf dem Zielgerät (ein Gerät, dem Sie in Microsoft Intune das Profil zugewiesen haben), und suchen Sie nach der Richtlinie. Wenn die Richtlinie nicht auf der Seite *edge://policy* angezeigt wird, versuchen Sie Folgendes:

- Überprüfen Sie, ob sich die Richtlinie in der Registrierung befindet und korrekt ist. Öffnen Sie auf dem Zielgerät den Windows 10-Registrierungs-Editor (**Windows-Taste + r**, geben Sie „*regedit*” ein und drücken Sie dann die **Eingabetaste**). Überprüfen Sie, ob die Richtlinie im Pfad *\Software\Policies\Microsoft \Edge* korrekt definiert ist. Wenn Sie die Richtlinie nicht im erwarteten Pfad finden, wurde die Richtlinie nicht ordnungsgemäß auf das Gerät übertragen.
- Überprüfen Sie, ob der OMA-URI-Pfad korrekt und der Wert eine gültige XML-Zeichenfolge ist. Wenn eines davon fehlerhaft ist, wird die Richtlinie nicht auf das Zielgerät übertragen.

Weitere Tipps zur Problembehebung finden Sie unter [Microsoft Intune einrichten](/intune/fundamentals/setup-steps) und [Geräte synchronisieren](/intune/remote-actions/device-sync).

## <a name="see-also"></a>Weitere Informationen:

- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)
- [Konfigurieren der Microsoft Edge-Richtlinieneinstellungen mit Microsoft Intune](./configure-edge-with-intune.md)
- [Mobile Geräteverwaltung](/windows/client-management/mdm/)
- [Verwenden von benutzerdefinierten Einstellungen für Windows 10-Geräte in Intune](/intune/configuration/custom-settings-windows-10)
- [Richtlinienkonfiguration für Win32- und Desktop-Brücke-Apps](/windows/client-management/mdm/win32-and-centennial-app-policy-configuration)
- [Grundlegende Informationen zu ADMX-gesicherten Richtlinien](/windows/client-management/mdm/understanding-admx-backed-policies)