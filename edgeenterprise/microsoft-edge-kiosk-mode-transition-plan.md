---
title: Planen der Kioskmodusumstellung
ms.author: aguta
author: aguta
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Planen der Kioskmodusumstellung
ms.openlocfilehash: 31a127de166e5bff53ad73951b0fd0f29eed094cae5026bf57995ccebcd5784c
ms.sourcegitcommit: d44c0997ffe40d67421312ed96e7766da947eaa0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "11726748"
---
# <a name="plan-your-kiosk-mode-transition"></a>Planen der Kioskmodusumstellung

Dieser Artikel enthält Anleitungen zur Umstellung Ihres Kiosks der Vorgängerversion von Microsoft Edge auf Microsoft Edge.  

> [!NOTE]
> Dieser Artikel bezieht sich auf die Microsoft Edge-Kanäle Stable, Beta und Dev, Version 87 oder höher.

> [!IMPORTANT]
> Wenn die Unterstützung für die Vorgängerversion von Microsoft Edge am 9. März 2021 endet, wird es entfernt und im Rahmen von Windows Update von April durch Microsoft Edge (Chromium-basiert) ersetzt. Weitere Informationen finden Sie [in diesem Blogbeitrag](https://aka.ms/EdgeLegacyEOS). Damit Sie ihre browserbasierten Kioskszenarien weiterhin verwenden können, müssen Sie Microsoft Edge (Chromium-basiert) installieren und den Kioskmodus vor der Windows Update-Freigabe von April auf Ihrem Gerät einrichten.

## <a name="kiosk-setup-steps"></a>Schritte zum Einrichten des Kiosks

Verwenden Sie die folgenden Schritte als Leitfaden zum Einrichten eines Kiosks in Microsoft Edge.

**Schritt 1: Bewerten Ihrer Anforderungen gegenüber der Funktionalität des veröffentlichten (und bevorstehenden) Kioskmodus.** In der folgenden Tabelle sind die Features aufgeführt, die vom Kioskmodus in Microsoft Edge (Chromium-basiert) und der Vorgängerversion von Microsoft Edge unterstützt werden. Verwenden Sie diese Tabelle als Leitfaden für die Umstellung auf Microsoft Edge, indem Sie vergleichen, wie diese Features in beiden Releases von Microsoft Edge unterstützt werden.

|Feature|Digital\Interactive Signage|Öffentliches Surfen|Verfügbar mit Microsoft Edge, Version (und höher)|Verfügbar mit der Vorgängerversion von Microsoft Edge|
|-|-|-|-|-|
|InPrivate-Navigation|„Y“ zugeordnet ist|„Y“ zugeordnet ist|89|J|
|Zurücksetzen bei Inaktivität|„Y“ zugeordnet ist|„Y“ zugeordnet ist|89|J|
|[Schreibgeschützte Adressleiste](./microsoft-edge-policies.md#kioskaddressbareditingenabled) (Richtlinie) |N|„Y“ zugeordnet ist |89|N|
|[Löschen von Downloads beim Beenden](./microsoft-edge-policies.md#kioskdeletedownloadsonexit) (Richtlinie)  | „Y“ zugeordnet ist|„Y“ zugeordnet ist |89|N|
|F11 blockiert (Vollbildmodus aktivieren/deaktivieren) | „Y“ zugeordnet ist | „Y“ zugeordnet ist | 89 |J|
|F12 blockiert (Entwicklertools starten) | „Y“ zugeordnet ist | „Y“ zugeordnet ist | 89 |J|
| Unterstützung für mehrere Registerkarten | N| „Y“ zugeordnet ist| 89|J|
|[Unterstützung von URLs zulassen](./microsoft-edge-policies.md#urlallowlist) (Richtlinie)|J|„Y“ zugeordnet ist|89|N|
|[Unterstützung von URLs sperren](./microsoft-edge-policies.md#urlblocklist) (Richtlinie)|J|„Y“ zugeordnet ist|89|N|
|[Schaltfläche „Start“ anzeigen](./microsoft-edge-policies.md#showhomebutton) (Richtlinie)|N|„Y“ zugeordnet ist|89|J|
|[Favoriten verwalten](./microsoft-edge-policies.md#managedfavorites) (Richtlinie)|N|„Y“ zugeordnet ist|89|J|
|[Drucker aktivieren](./microsoft-edge-policies.md#printingenabled) (Richtlinie)|J|„Y“ zugeordnet ist|89|J|
|[Konfigurieren der URL der neuen Registerkartenseite](./microsoft-edge-policies.md#newtabpagelocation) (Richtlinie)|N|„Y“ zugeordnet ist|89|J|
|Sitzung beenden | N| „Y“ zugeordnet ist| 89|J|
|Alle internen Microsoft Edge-URLs werden blockiert, mit Ausnahme von *edge://downloads* und *edge://print* |N|„Y“ zugeordnet ist|89|J|
| STRG+N blockiert (neues Fenster öffnen) | „Y“ zugeordnet ist | „Y“ zugeordnet ist | 89 |J|
| STRG+T blockiert (neue Registerkarte öffnen) |J | „Y“ zugeordnet ist | 89 |J|
|Einstellungen und mehr (...) zeigt nur die erforderlichen Optionen an.  |J |„Y“ zugeordnet ist |89 |J|
|Start anderer Anwendungen über den Browser einschränken|J|J|90|J|
|Sperrung der Benutzeroberflächen-Druckeinstellungen|J|J|90|J|
|[Neue Registerkartenseite als Startseite festlegen](./microsoft-edge-policies.md#homepageisnewtabpage) (Richtlinie)|N|J|90|J|

> [!NOTE]
> Informationen zum Veröffentlichungszeitplan für Microsoft Edge finden Sie unter [Microsoft Edge-Veröffentlichungszeitplan](microsoft-edge-release-schedule.md).

**Schritt 2: Testen des neuen Kiosk in Microsoft Edge.** Es wird empfohlen, das Einrichten des Kioskmodus in Microsoft Edge zu testen. Eine schnelle und einfache Möglichkeit zum Testen des Kioskmodus ist das Konfigurieren einer Einzel-App mit zugewiesenen Zugriff mithilfe der Windows-Einstellungen, wie im Folgenden beschrieben.

1. Die Mindestsystemaktualisierungen für die Betriebssysteme, die in der nächsten Tabelle aufgelistet sind.

|Betriebssystem|Version|Updates|
|--|--|--|
|Windows 10 | 2004 oder höher|[KB4601382 oder höher](https://support.microsoft.com/topic/february-24-2021-kb4601382-os-builds-19041-844-and-19042-844-preview-1a7ed2b4-017d-2644-a1e8-dd6bf14cba76) |
|Windows 10| 1909| [KB4601380 oder höher](https://support.microsoft.com/topic/february-16-2021-kb4601380-os-build-18363-1411-preview-2e3c38e1-a947-1033-8006-a30f3806da18)|

2. Um die neuesten Features zu testen, können Sie den neuesten [Microsoft Edge Stable-Kanal](https://www.microsoftedgeinsider.com/download), Version 89 oder höher, herunterladen.

   > [!IMPORTANT]
   > Da eine Installation auf Geräteebene erforderlich ist, wird der Canary-Kanal nicht unterstützt.

3. Öffnen Sie auf dem Kiosk-Computer die Windows-Einstellungen, und geben Sie im Suchfeld „Kiosk“ ein. Wählen Sie  **Einen Kiosk einrichten (zugewiesener Zugriff)** aus, das im nächsten Screenshot dargestellt ist, um das Dialogfeld zum Erstellen des Kiosks zu öffnen.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-1-assigned-access.png" alt-text="Einrichten eines Kiosks mit zugewiesenem Zugriff":::

4. Klicken Sie auf der Seite **Einen Kiosk einrichten**  auf **Erste Schritte**.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-2-get-started.png" alt-text="Seite Kiosk – erste Schritte":::

5. Geben Sie einen Namen ein, um ein neues Kioskkonto zu erstellen, oder wählen Sie ein vorhandenes Konto aus der Dropdownliste aus, und klicken Sie dann auf  **Weiter**.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-3-create-account.png" alt-text="Kioskmodus – Konto erstellen":::

6. Wählen Sie auf der Seite **Kiosk-App auswählen**  die Option **Microsoft Edge** aus, und klicken Sie dann auf  **Weiter**.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-5c-choose-a-kiosk-app.png" alt-text="Auswählen eines Kiosks – digitale Anmeldung im Vollbildmodus":::

7. Wählen Sie eine der folgenden Optionen für die Darstellung von Microsoft Edge aus, wenn es im Kioskmodus ausgeführt wird:

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

**Schritt 3: Entwickeln eines Umstellungsplans.** Basierend auf Ihren Test- und organisatorischen Anforderungen empfehlen wir die Entwicklung eines Umstellungplans und den Wechsel zu Microsoft Edge (Chromium-basiert), bevor der Support für die Vorgängerversion von Microsoft Edge am 9. März 2021 endet.

## <a name="additional-scenarios-that-require-you-to-recreate-an-existing-kiosk-mode"></a>Zusätzliche Szenarien, in denen Sie einen vorhandenen Kioskmodus neu erstellen müssen

Wenn Sie auf Windows 10, Version 20H2, aktualisieren, wird Microsoft Edge (Chromium-basiert) installiert und die Vorgängerversion von Microsoft Edge verborgen. In diesem Fall müssen Sie den Kioskmodus in Microsoft Edge (Chromium-basiert) erneut einrichten.

## <a name="how-to-get-help"></a>So erhalten Sie Hilfe

Der Kioskmodus ist möglicherweise ein wichtiger Bestandteil Ihres täglichen Geschäfts. Daher möchten wir ihnen helfen, diese Umstellung so reibungslos wie möglich zu gestalten und Unterbrechungen zu vermeiden. Wenn Ihr Unternehmen bei der Umstellung auf Microsoft Edge (Chromium-basiert) Hilfe benötigt:

- [Support](https://support.serviceshub.microsoft.com/supportforbusiness/create?sapId=a77ee9b7-b6b6-aa08-d7b9-887ebe228207) steht von Microsoft zur Verfügung. 
- Für Kunden mit 150 oder mehr kostenpflichtigen Plätzen von Windows 10 Enterprise ist zudem [FastTrack-Support](https://www.microsoft.com/fasttrack/microsoft-365/microsoft-edge?rtc=1) kostenlos verfügbar.
- [App Assure](https://www.microsoft.com/en-us/fasttrack/microsoft-365/app-assure) ist verfügbar, wenn Website- oder App-Kompatibilitätsprobleme auftreten.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)
- [Neues Microsoft Edge ersetzt die Vorgängerversion von Microsoft Edge im Rahmen des Windows 10 Update Tuesday Release von April](https://techcommunity.microsoft.com/t5/microsoft-365-blog/new-microsoft-edge-to-replace-microsoft-edge-legacy-with-april-s/ba-p/2114224)