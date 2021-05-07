---
title: Konfigurieren des Microsoft Edge-Kioskmodus
ms.author: aguta
author: aguta
manager: srugh
ms.date: 03/16/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Erfahren Sie mehr über Kioskmodus-Features und wie Sie Microsoft Edge-Kioskmodusoptionen konfigurieren können.
ms.openlocfilehash: 9d76bfcaebeaf56e627a401cc4f0375bce9d17a3
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/24/2021
ms.locfileid: "11448129"
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
|InPrivate-Navigation|„Y“ zugeordnet ist|„Y“ zugeordnet ist|89|„Y“ zugeordnet ist|
|Zurücksetzen bei Inaktivität|„Y“ zugeordnet ist|„Y“ zugeordnet ist|89|J|
|[Schreibgeschützte Adressleiste](./microsoft-edge-policies.md#kioskaddressbareditingenabled) (Richtlinie) |N|„Y“ zugeordnet ist |89|N|
|[Löschen von Downloads beim Beenden](./microsoft-edge-policies.md#kioskdeletedownloadsonexit) (Richtlinie)  | „Y“ zugeordnet ist|„Y“ zugeordnet ist |89|N|
|F11 blockiert (Vollbildmodus aktivieren/deaktivieren) | „Y“ zugeordnet ist | „Y“ zugeordnet ist | 89 |„Y“ zugeordnet ist|
|F12 blockiert (Entwicklertools starten) | „Y“ zugeordnet ist | „Y“ zugeordnet ist | 89 |J|
| Unterstützung für mehrere Registerkarten | N| „Y“ zugeordnet ist| 89|J|
|[Unterstützung von URLs zulassen](./microsoft-edge-policies.md#urlallowlist) (Richtlinie)|„Y“ zugeordnet ist|„Y“ zugeordnet ist|89|N|
|[Unterstützung von URLs sperren](./microsoft-edge-policies.md#urlblocklist) (Richtlinie)|J|„Y“ zugeordnet ist|89|N|
|[Schaltfläche „Start“ anzeigen](./microsoft-edge-policies.md#showhomebutton) (Richtlinie)|N|„Y“ zugeordnet ist|89|J|
|[Favoriten verwalten](./microsoft-edge-policies.md#managedfavorites) (Richtlinie)|N|„Y“ zugeordnet ist|89|J|
|[Drucker aktivieren](./microsoft-edge-policies.md#printingenabled) (Richtlinie)|J|„Y“ zugeordnet ist|89|J|
|[Konfigurieren der URL der neuen Registerkartenseite](./microsoft-edge-policies.md#newtabpagelocation) (Richtlinie)|N|„Y“ zugeordnet ist||Y|
|Schaltfläche „Sitzung beenden" * | N| „Y“ zugeordnet ist| 89|J|
|Alle internen Microsoft Edge-URLs werden blockiert, mit Ausnahme von *edge://downloads* und *edge://print* |N|„Y“ zugeordnet ist|89|Y|
| STRG+N gesperrt (öffnen Sie ein neues Fenster) * | Y | „Y“ zugeordnet ist | 89 |J|
| STRG+T blockiert (neue Registerkarte öffnen) |Y | N | 89 |J|
|Einstellungen und mehr (...) zeigt nur die erforderlichen Optionen an.  |„Y“ zugeordnet ist |„Y“ zugeordnet ist |89 |„Y“ zugeordnet ist|
|Start anderer Anwendungen über den Browser einschränken|J|„Y“ zugeordnet ist|90/91|J|
|Sperrung der Benutzeroberflächen-Druckeinstellungen|J|„Y“ zugeordnet ist|90/91|J|
|[Neue Registerkartenseite als Startseite festlegen](./microsoft-edge-policies.md#homepageisnewtabpage) (Richtlinie)|-|-|TBD|Y|

> [!NOTE]
> Features gefolgt von "*" werden nur in einem zugewiesenen Zugriffsszenario für einzelne Apps aktiviert.

## <a name="use-kiosk-mode-features"></a>Verwenden der Kioskmodus-Features

Features des Microsoft Edge-Kioskmodus können mit den folgenden Windows 10-Befehlszeilenoptionen für digitale/interaktive Beschilderung und öffentliches Browsen aufgerufen werden.

### <a name="kiosk-mode-digitalinteractive-signage"></a>Kioskmodus: digitale/interaktive Beschilderung
 
```
msedge.exe --kiosk www.contoso.com --edge-kiosk-type=fullscreen
```

### <a name="kiosk-mode-public-browsing"></a>Kioskmodus: öffentliches Browsen

```
msedge.exe --kiosk www.contoso.com --edge-kiosk-type=public-browsing
```

### <a name="additional-command-line-options"></a>Zusätzliche Befehlszeilenoptionen

- **--no-first-run**: Deaktivieren der Umgebung der ersten Microsoft Edge-Ausführung.

   ```
  msedge.exe --kiosk www.contoso.com --edge-kiosk-type=fullscreen --no-first-run
  ```

  ```
  msedge.exe --kiosk www.contoso.com --edge-kiosk-type=public-browsing --no-first-run
  ```

- **--kiosk-idle-timeout-minutes=**: Ändern der Zeit (in Minuten) zwischen der letzten Benutzeraktivität und der Zurücksetzung der Sitzung des Benutzers durch den Microsoft Edge-Kioskmodus. Ersetzen Sie „value“ im nächsten Beispiel durch die Anzahl der Minuten.

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

Microsoft Edge unterstützt derzeit eine Teilmenge der gleichen Kioskmodustypen der Vorgängerversion von Microsoft Edge für den zugewiesenen Zugriff mit einer einzelnen App mit den folgenden Sperrmodus-Funktionen: Digitale/interaktive Beschilderung und Öffentliches Browsen.  

Der Microsoft Edge-Kioskmodus mit einer Einzel-App mit zugewiesenen Zugriff ist derzeit für Tests mit dem neuesten  [Windows 10 Insider Preview-Build](https://insider.windows.com/), Version 20215 oder höher, und mit dem  [Microsoft Edge Beta Channel](https://www.microsoftedgeinsider.com/download), Version 89 oder höher, verfügbar.

**Wie erhalte ich den Windows Insider Preview-Build?**

Wenn Sie einen Windows10 Insider Preview-Build auf einem PC installieren möchten, folgen Sie den Anweisungen unter  [Erste Schritte mit Windows10 Insider Preview-Builds](/windows-insider/get-started).

### <a name="multi-app-kiosk"></a>Multi-App-Kiosk

Microsoft Edge kann unter Windows10 mit [zugewiesenem Multi-App-Zugriff](/windows/configuration/lock-down-windows-10-to-specific-apps) ausgeführt werden, was dem Kioskmodustyp „Normales Browsen” von Microsoft Edge Legacy entspricht. Befolgen Sie die Anweisungen zum Einrichten eines Multi-App-Kiosks, um Microsoft Edge mit zugewiesenen [Multi-App-Zugriffen zu konfigurieren.](/windows/configuration/lock-down-windows-10-to-specific-apps) (Die AUMID für den Stable-Kanal von Microsoft Edge ist **MSEdge**.)

Wenn Sie Microsoft Edge mit zugewiesenen Zugriffen mit mehreren Apps verwenden, können Sie den Microsoft Edge Kiosk so konfigurieren, dass er die[Microsoft Edge-Browserrichtlinien](https://review.docs.microsoft.com/DeployEdge/microsoft-edge-policies) verwendet, um die Browsererfahrung so zu konfigurieren, dass Ihre individuellen Anforderungen erfüllt werden.

### <a name="configure-using-windows-settings"></a>Konfigurieren mithilfe der Windows-Einstellungen

Die Windows-Einstellungen sind die einfachste Möglichkeit zum Einrichten von ein oder zwei Einzel-App-Kioskgeräten. Führen Sie die folgenden Schritte aus, um einen Einzel-App-Kioskcomputer einzurichten.

1. Installieren Sie die neueste Windows 10 Insider Preview-Version (20215 oder höher). Folgen Sie den Anweisungen unter [Erste Schritte mit Windows 10 Insider Preview-Builds](/windows-insider/get-started).
2. Um die neuesten Features zu testen, können Sie den neuesten [Microsoft Edge Beta Channel](https://www.microsoftedgeinsider.com/download), Version 89 oder höher, herunterladen.
3. Öffnen Sie auf dem Kiosk-Computer die Windows-Einstellungen, und geben Sie im Suchfeld „Kiosk“ ein. Wählen Sie  **Einen Kiosk einrichten (zugewiesener Zugriff)** aus, das im nächsten Screenshot dargestellt ist, um das Dialogfeld zum Erstellen des Kiosks zu öffnen.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-1-assigned-access.png" alt-text="Einrichten eines Kiosks mit zugewiesenem Zugriff":::

4. Klicken Sie auf der Seite **Einen Kiosk einrichten**  auf **Erste Schritte**.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-2-get-started.png" alt-text="Seite Kiosk – erste Schritte":::

5. Geben Sie einen Namen ein, um ein neues Kioskkonto zu erstellen, oder wählen Sie ein vorhandenes Konto aus der Dropdownliste aus, und klicken Sie dann auf  **Weiter**.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-3-create-account.png" alt-text="Kioskmodus – Konto erstellen":::

6. Wählen Sie auf der Seite **Kiosk-App auswählen**  die Option **Microsoft Edge** aus, und klicken Sie dann auf  **Weiter**.

   > [!NOTE]
   > Dies gilt nur für Microsoft Edge Dev, Beta und Stable-Kanäle.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-4-pick-app.png" alt-text="Kioskmodus – App auswählen":::

7. Wählen Sie eine der folgenden Optionen für die Darstellung von Microsoft Edge aus, wenn er im Kioskmodus ausgeführt wird:

   - Digitale/interaktive Beschilderung: Zeigt eine bestimmte Website im Vollbildmodus an, dabei wird Microsoft Edge ausgeführt.
   - Öffentliches Surfen: Führt eine eingeschränkte Version von Microsoft Edge mit mehreren Tabs aus.

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-5a-digital-sign.png" alt-text="Kioskmodus – digitale Beschilderung im Vollbildmodus":::

8. Wählen Sie ** Weiter** aus.
9. Geben Sie die URL ein, die beim Start des Kiosks geladen werden soll.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-6-enter-url.png" alt-text="Kioskmodus – URL eingeben":::

10. Übernehmen Sie den Standardwert von 5 Minuten für die Leerlaufzeit, oder geben Sie einen eigenen Wert ein.

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-7-enter-idle-time.png" alt-text="Kioskmodus – Leerlaufzeit eingeben":::

11. Klicken Sie auf  **Weiter**.
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

## <a name="roadmap"></a>Roadmap

### <a name="in-early-2021"></a>Anfang 2021

Unterstützung und Funktionen, die hinzukommen werden:

- Allgemeine Verfügbarkeit des Microsoft Edge-Kioskmodus mit zugewiesener Zugriffs-Einzel-App unter Windows 10 1909 und höher.
- Zusätzliche Features für Parität mit Vorgängerversion von Microsoft Edge.
- Integration in Intune zum Konfigurieren von Geräten über die Profil-Benutzerumgebung im Kioskmodus.
- Schränken Sie den Start anderer Anwendungen über den Browser ein.
- Sperrung der Benutzeroberflächen-Druckeinstellungen.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)
- [Planen Ihrer Bereitstellung von Microsoft Edge](deploy-edge-plan-deployment.md)
- [Konfigurieren von Kiosken und digitalen Anmeldungen in Windows-Desktopeditionen](/windows/configuration/kiosk-methods)
- [Planen der Kioskmodusumstellung](microsoft-edge-kiosk-mode-transition-plan.md)