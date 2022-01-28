---
title: Konfigurieren des Microsoft Edge-Kioskmodus
ms.author: aguta
author: aguta
manager: srugh
ms.date: 11/30/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Erfahren Sie mehr über Kioskmodus-Features und wie Sie Microsoft Edge-Kioskmodusoptionen konfigurieren können.
ms.openlocfilehash: fa53f52dd9115d85da6fec6a75aefb972c9f6ece
ms.sourcegitcommit: e7f3098d8b7d91cae20b5778a71a87daababc312
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2022
ms.locfileid: "12298303"
---
# <a name="configure-microsoft-edge-kiosk-mode"></a>Konfigurieren des Microsoft Edge-Kioskmodus

In diesem Artikel wird beschrieben, wie Sie die Optionen für den Microsoft Edge-Kioskmodus Ihren Anforderungen entsprechend konfigurieren können. Eine Roadmap zukünftiger Features wird ebenfalls vorgestellt.

> [!NOTE]
> Dieser Artikel bezieht sich auf Microsoft Edge Version 87 oder höher.

> [!IMPORTANT]
> Aufrufen der Microsoft Edge-Kioskmodusfeatures in Windows 10 mithilfe der Befehlszeilenargumente, die unter [Verwenden von Kioskmodusfeatures](#use-kiosk-mode-features) angegeben sind.

## <a name="overview"></a>Übersicht

Im Microsoft Edge-Kiosk-Modus sind zwei gesperrte Browserumgebungen verfügbar, damit Organisationen optimale Umgebungen für ihre Kunden gestalten, verwalten und anbieten können. Die folgenden gesperrten Umgebungen sind verfügbar:  

- **Digital/Interactive Signage–** Zeigt eine bestimmte Website im Vollbildmodus an.
- **Öffentliches Browsen** – Führt eine eingeschränkte Version mit mehreren Registerkarten von Microsoft Edge aus.

In beiden Fällen wird eine Microsoft Edge-InPrivate-Sitzung ausgeführt, wodurch die Benutzerdaten geschützt sind.

## <a name="set-up-microsoft-edge-kiosk-mode"></a>Einrichten des Microsoft Edge-Kioskmodus

Ein anfänglicher Satz von Kioskmodusfeatures steht zum Testen mit Microsoft Edge Stable-Kanal, Version 87, zur Verfügung. Sie können die neueste Version von [Microsoft Edge (offizieller Stable-Kanal) herunterladen.](https://www.microsoft.com/edge)

### <a name="kiosk-mode-supported-features"></a>Unterstützte Features im Kioskmodus

In der folgenden Tabelle sind die Features aufgeführt, die vom Kioskmodus in Microsoft Edge und der Vorgängerversion von Microsoft Edge unterstützt werden. Verwenden Sie diese Tabelle als Leitfaden für die Umstellung auf Microsoft Edge, indem Sie vergleichen, wie diese Features in beiden Versionen von Microsoft Edge unterstützt werden.

|Feature|Digital\Interactive Signage|Öffentliches Surfen|Verfügbar mit Microsoft Edge, Version (und höher)|Verfügbar mit der Vorgängerversion von Microsoft Edge|
|-|-|-|-|-|
|InPrivate-Navigation|„Y“ zugeordnet ist|„Y“ zugeordnet ist|89|J|
|Zurücksetzen bei Inaktivität|„Y“ zugeordnet ist|„Y“ zugeordnet ist|89|J|
|[Schreibgeschützte Adressleiste](./microsoft-edge-policies.md#kioskaddressbareditingenabled) (Richtlinie) |N|„Y“ zugeordnet ist |89|N|
|[Löschen von Downloads beim Beenden](./microsoft-edge-policies.md#kioskdeletedownloadsonexit) (Richtlinie)  | „Y“ zugeordnet ist|„Y“ zugeordnet ist |89|N|
|F11 blockiert (Vollbildmodus aktivieren/deaktivieren) | „Y“ zugeordnet ist | „Y“ zugeordnet ist |89|J|
|F12 blockiert (Entwicklertools starten) | „Y“ zugeordnet ist | „Y“ zugeordnet ist |89|J|
| Unterstützung für mehrere Registerkarten | N| „Y“ zugeordnet ist|89|J|
|[Unterstützung von URLs zulassen](./microsoft-edge-policies.md#urlallowlist) (Richtlinie)|J|„Y“ zugeordnet ist|89|N|
|[Unterstützung von URLs sperren](./microsoft-edge-policies.md#urlblocklist) (Richtlinie)|J|„Y“ zugeordnet ist|89|N|
|[Schaltfläche „Start“ anzeigen](./microsoft-edge-policies.md#showhomebutton) (Richtlinie)|N|„Y“ zugeordnet ist|89|J|
|[Favoriten verwalten](./microsoft-edge-policies.md#managedfavorites) (Richtlinie)|N|„Y“ zugeordnet ist|89|J|
|[Drucker aktivieren](./microsoft-edge-policies.md#printingenabled) (Richtlinie)|J|„Y“ zugeordnet ist|89|J|
|[Konfigurieren der URL der neuen Registerkartenseite](./microsoft-edge-policies.md#newtabpagelocation) (Richtlinie)|N|„Y“ zugeordnet ist|89|Y|
|Schaltfläche „Sitzung beenden" * | N| „Y“ zugeordnet ist|89|J|
|Alle internen Microsoft Edge-URLs werden blockiert, mit Ausnahme von *edge://downloads* und *edge://print* |N|„Y“ zugeordnet ist|89|Y|
| STRG+N gesperrt (öffnen Sie ein neues Fenster) * | Y | „Y“ zugeordnet ist |89|J|
| STRG+T blockiert (neue Registerkarte öffnen) |Y | N |89|J|
|Einstellungen und mehr (...) zeigt nur die erforderlichen Optionen an.  |J |„Y“ zugeordnet ist |89|J|
|Start anderer Anwendungen über den Browser einschränken|J|J|90|J|
|Sperrung der Benutzeroberflächen-Druckeinstellungen|J|J|90|J|
|[Neue Registerkartenseite als Startseite festlegen](./microsoft-edge-policies.md#homepageisnewtabpage) (Richtlinie)|N|J|90|Y|

> [!NOTE]
> Features gefolgt von "*" werden nur in einem zugewiesenen Zugriffsszenario für einzelne Apps aktiviert.

## <a name="use-kiosk-mode-features"></a>Verwenden der Kioskmodus-Features

Microsoft Edge Kioskmodusfeatures können mit den folgenden Windows 10 Befehlszeilenoptionen für digitale/interaktive Beschilderung und öffentliches Browsen aufgerufen werden.

### <a name="kiosk-mode-digitalinteractive-signage"></a>Kioskmodus: digitale/interaktive Beschilderung
 
```
msedge.exe --kiosk www.contoso.com --edge-kiosk-type=fullscreen
```

### <a name="kiosk-mode-public-browsing"></a>Kioskmodus: öffentliches Browsen

```
msedge.exe --kiosk www.contoso.com --edge-kiosk-type=public-browsing
```

### <a name="kiosk-mode-download-files-on-exit"></a>Kioskmodus Dateien beim Beenden herunterladen

Um Microsoft Edge einzurichten, um heruntergeladene Dateien zu entfernen, wenn eine Kioskinstanz geschlossen wird, müssen die folgenden beiden Gruppenrichtlinien konfiguriert werden:
- [Downloads beim Beenden löschen](./microsoft-edge-policies.md#kioskdeletedownloadsonexit) = aktiviert
- [Downloadverzeichnis festlegen](./microsoft-edge-policies.md#downloaddirectory) = ${local_app_data}\Microsoft\Edge\KioskDownloads 


### <a name="additional-command-line-options"></a>Zusätzliche Befehlszeilenoptionen

- **--no-first-run**: Deaktivieren der Umgebung der ersten Microsoft Edge-Ausführung.

   ```
  msedge.exe --kiosk www.contoso.com --edge-kiosk-type=fullscreen --no-first-run
  ```

  ```
  msedge.exe --kiosk www.contoso.com --edge-kiosk-type=public-browsing --no-first-run
  ```

- **--kiosk-idle-timeout-minutes=**: Ändern Sie die Zeit (in Minuten) von der letzten Benutzeraktivität, bevor Microsoft Edge Kioskmodus die Sitzung des Benutzers zurücksetzt, indem Sie den Browser schließen. Hinweis: Dieses Flag wird Microsoft Edge nach dem Schließen nicht neu gestartet. Eine separate Technologie, z. B. zugewiesener Zugriff oder Shell-Start, ist erforderlich, um Edge nach dem Leerlauftimeout automatisch neu zu starten. Ersetzen Sie „value“ im nächsten Beispiel durch die Anzahl der Minuten.

   ```
   --kiosk-idle-timeout-minutes=value
   ``` 
   Die folgenden Werte werden unterstützt:

     - Standardwerte (in Minuten)
       - Vollbild – 0 (deaktiviert)
       - Öffentliches Surfen – 5 Minuten
    - Zulässige Werte
      - 0 – deaktiviert den Timer
      - 1-1440 Minuten für das Zurücksetzen für den Leerlaufzeit-Zeitgeber


    ```
    msedge.exe --kiosk www.contoso.com --edge-kiosk-type=fullscreen --kiosk-idle-timeout-minutes=1
   ```

   ```
   msedge.exe --kiosk www.contoso.com --edge-kiosk-type=public-browsing --kiosk-idle-timeout-minutes=1
   ```

## <a name="support-policies-for-kiosk-mode"></a>Supportrichtlinien für den Kioskmodus

Verwenden Sie eine der in der folgenden Tabelle aufgeführten Microsoft Edge-Richtlinien, um die Kioskerfahrung für den von Ihnen konfigurierten Microsoft Edge-Kioskmodustyp zu verbessern. Weitere Informationen zu diesen Richtlinien finden Sie unter [Microsoft Edge – Browser policy reference](./microsoft-edge-policies.md).

> [!NOTE]
> Die Richtlinienkonfiguration ist nicht auf die in der folgenden Tabelle aufgeführten Richtlinien beschränkt. Es sollten jedoch zusätzliche Richtlinien getestet werden, um sicherzustellen, dass die Funktionalität des Kioskmodus nicht negativ beeinträchtigt wird.

|Gruppenrichtlinie|Digital\Interactive Signage|Einzel-App für öffentliches Browsen|
|--|--|--|
|[Drucken](./microsoft-edge-policies.md#printing-policies) | „Y“ zugeordnet ist|„Y“ zugeordnet ist |
|[HomePageLocation](./microsoft-edge-policies.md#homepagelocation) |N | „Y“ zugeordnet ist|
|[ShowHomeButton](./microsoft-edge-policies.md#showhomebutton) |N | „Y“ zugeordnet ist|
|[NewTabPageLocation](./microsoft-edge-policies.md#newtabpagelocation) |N |„Y“ zugeordnet ist |
|[FavoritesBarEnabled](./microsoft-edge-policies.md#favoritesbarenabled) |N |„Y“ zugeordnet ist |
|[URLAllowlist](./microsoft-edge-policies.md#urlallowlist) |„Y“ zugeordnet ist |„Y“ zugeordnet ist |
|[URLBlocklist](./microsoft-edge-policies.md#urlblocklist) |„Y“ zugeordnet ist | „Y“ zugeordnet ist|
|[ManagedSearchEngines](./microsoft-edge-policies.md#managedsearchengines) |N | „Y“ zugeordnet ist|
|[UserFeedbackAllowed](./microsoft-edge-policies.md#userfeedbackallowed) |N | „Y“ zugeordnet ist|
|[VerticalTabsAllowed](./microsoft-edge-policies.md#verticaltabsallowed) | N|„Y“ zugeordnet ist |
|[SmartScreen-Einstellungen](./microsoft-edge-policies.md#smartscreen-settings-policies) |„Y“ zugeordnet ist |J |
|[EdgeCollectionsEnabled](./microsoft-edge-policies.md#edgecollectionsenabled)|J|„Y“ zugeordnet ist|

## <a name="microsoft-edge-with-assigned-access"></a>Microsoft Edge mit zugewiesenem Zugriff

### <a name="single-app-kiosk"></a>Einzel-App-Kiosk

Der Kioskmodus von Microsoft Edge Version 90 bietet eine umfangreiche Liste von Features. Weitere Informationen finden Sie im Abschnitt „Unterstützte Features im Kioskmodus“.
Mit den folgenden Windows Updates können Sie Microsoft Edge über eine einzelne App mit zugewiesenem Zugriff konfigurieren.

|Betriebssystem|Version|Updates|
|--|--|--|
|Windows 10 | 2004 oder höher|[KB4601382 oder höher](https://support.microsoft.com/topic/february-24-2021-kb4601382-os-builds-19041-844-and-19042-844-preview-1a7ed2b4-017d-2644-a1e8-dd6bf14cba76) |
|Windows 10| 1909| [KB4601380 oder höher](https://support.microsoft.com/topic/february-16-2021-kb4601380-os-build-18363-1411-preview-2e3c38e1-a947-1033-8006-a30f3806da18)|

Sie können den zugewiesenen Zugriff einzelner Apps im Kioskmodus von Microsoft Edge über [Windows-Einstellungen](/deployedge/microsoft-edge-configure-kiosk-mode#configure-using-windows-settings) und Intune verwalten.

### <a name="multi-app-kiosk"></a>Multi-App-Kiosk

Microsoft Edge kann unter Windows 10 mit [zugewiesenem Multi-App-Zugriff](/windows/configuration/lock-down-windows-10-to-specific-apps) ausgeführt werden, was dem Kioskmodustyp „Normales Browsen” von Microsoft Edge Legacy entspricht. Befolgen Sie die Anweisungen zum Einrichten eines Multi-App-Kiosks, um Microsoft Edge mit zugewiesenen [Multi-App-Zugriffen zu konfigurieren.](/windows/configuration/lock-down-windows-10-to-specific-apps) (Die AUMID für den Microsoft Edge Stable-Kanal ist **Microsoft.MicrosoftEdge.Stable_8wekyb3d8bbwe! MSEDGE**).

Wenn Sie Microsoft Edge mit zugewiesenem Zugriff mit mehreren Apps verwenden, können Sie Microsoft Edge Kiosk so konfigurieren, dass die [Browserrichtlinien Microsoft Edge](./microsoft-edge-policies.md) verwendet werden, um die Browserumgebung so zu konfigurieren, dass Ihre individuellen Anforderungen erfüllt werden.

### <a name="configure-using-windows-settings"></a>Konfigurieren mithilfe der Windows-Einstellungen

Die Windows-Einstellungen sind die einfachste Möglichkeit zum Einrichten von ein oder zwei Einzel-App-Kioskgeräten. Führen Sie die folgenden Schritte aus, um einen Einzel-App-Kioskcomputer einzurichten.

1. Die Mindestsystemaktualisierungen für die Betriebssysteme, die in der nächsten Tabelle aufgelistet sind.

|Betriebssystem|Version|Updates|
|--|--|--|
|Windows 10 | 2004 oder höher|[KB4601382 oder höher](https://support.microsoft.com/topic/february-24-2021-kb4601382-os-builds-19041-844-and-19042-844-preview-1a7ed2b4-017d-2644-a1e8-dd6bf14cba76) |
|Windows 10| 1909| [KB4601380 oder höher](https://support.microsoft.com/topic/february-16-2021-kb4601380-os-build-18363-1411-preview-2e3c38e1-a947-1033-8006-a30f3806da18)|

2. Um die neuesten Features zu testen, können Sie den neuesten [Microsoft Edge Stable Channel](https://www.microsoft.com/edge/business/download), Version 89 oder höher, herunterladen.

3. Öffnen Sie auf dem Kioskcomputer die Windows-Einstellungen, und geben Sie im Suchfeld „Kiosk“ ein. Wählen Sie  **Einen Kiosk einrichten (zugewiesener Zugriff)** aus, das im nächsten Screenshot dargestellt ist, um das Dialogfeld zum Erstellen des Kiosks zu öffnen.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-1-assigned-access.png" alt-text="Einrichten eines Kiosks mit zugewiesenem Zugriff":::

4. Wählen Sie auf der Seite **"Kiosk einrichten"**   die Option **"Erste Schritte" aus.**

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-2-get-started.png" alt-text="Seite Kiosk – erste Schritte":::

5. Geben Sie einen Namen ein, um ein neues Kioskkonto zu erstellen, oder wählen Sie ein vorhandenes Konto aus der ausgefüllten Dropdownliste aus, und wählen Sie dann **"Weiter"** aus.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-3-create-account.png" alt-text="Kioskmodus – Konto erstellen":::

6. Wählen Sie auf der Seite **"Kiosk-App**   **auswählen" Microsoft Edge**und dann **"Weiter"** aus.

   > [!NOTE]
   > Dies gilt nur für Microsoft Edge Dev, Beta und Stable Channels.

     :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-5c-choose-a-kiosk-app.png" alt-text="Kioskmodusanzeige: digitale Beschilderung im Vollbildmodus":::

7. Wählen Sie eine der folgenden Optionen für die Darstellung von Microsoft Edge aus, wenn es im Kioskmodus ausgeführt wird:

   - Digitale/interaktive Beschilderung: Zeigt eine bestimmte Website im Vollbildmodus an, dabei wird Microsoft Edge ausgeführt.
   - Öffentliches Surfen: Führt eine eingeschränkte Version von Microsoft Edge mit mehreren Tabs aus.

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-5a-digital-sign.png" alt-text="Verwendung des Kiosks: digitale Beschilderung im Vollbildmodus":::

8. Wählen Sie  **Weiter** aus.
9. Geben Sie die URL ein, die beim Start des Kiosks geladen werden soll.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-6-enter-url.png" alt-text="Kioskmodus – URL eingeben":::

10. Übernehmen Sie den Standardwert von 5 Minuten für die Leerlaufzeit, oder geben Sie einen eigenen Wert ein.

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-7-enter-idle-time.png" alt-text="Kioskmodus – Leerlaufzeit eingeben":::

11. Wählen Sie ** Weiter** aus.
12. Schließen Sie das Fenster  **Einstellungen** , um Ihre Auswahl zu speichern und anzuwenden.

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode--8-done.png" alt-text="Kioskmodus – Einrichten abschließen":::

13. Melden Sie sich vom Kioskgerät ab, und melden Sie sich mit dem lokalen Kioskkonto an, um die Konfiguration zu überprüfen.

## <a name="functional-limitations"></a>Funktionale Beschränkungen

Die Veröffentlichung dieser Preview-Version des Kioskmodus erfolgt im Rahmen unserer kontinuierlichen Bemühungen, das Produkt zu verbessern und neue Features hinzuzufügen.

Wir unterstützen derzeit die folgenden Features nicht und empfehlen, diese zu deaktivieren:

- [InPrivateModeAvailability](./microsoft-edge-policies.md#inprivatemodeavailability)
- [IsolateOrigins](./microsoft-edge-policies.md#isolateorigins)
- [ManagedFavorites](./microsoft-edge-policies.md#managedfavorites)
- [EdgeShoppingAssistantEnabled](./microsoft-edge-policies.md#edgeshoppingassistantenabled)
- [EdgeCollectionsEnabled](./microsoft-edge-policies.md#edgecollectionsenabled)
- [UserFeedbackAllowed](./microsoft-edge-policies.md#userfeedbackallowed)
- [DefaultPopupsSetting](./microsoft-edge-policies.md#defaultpopupssetting)
- [StartupBoostEnabled](./microsoft-edge-policies.md#startupboostenabled)
- [InternetExplorerIntegrationLevel](./microsoft-edge-policies.md#internetexplorerintegrationlevel)
- [Erweiterungen](./microsoft-edge-policies.md#extensions-policies)
- [BackgroundModeEnabled](./microsoft-edge-policies.md#backgroundmodeenabled)
- [UserFeedbackAllowed](./microsoft-edge-policies.md#userfeedbackallowed)

## <a name="see-also"></a>Weitere Informationen

- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)
- [Planen Ihrer Bereitstellung von Microsoft Edge](deploy-edge-plan-deployment.md)
- [Konfigurieren von Kiosken und digitalen Anmeldungen in Windows-Desktopeditionen](/windows/configuration/kiosk-methods)
- [Planen der Kioskmodusumstellung](microsoft-edge-kiosk-mode-transition-plan.md)
