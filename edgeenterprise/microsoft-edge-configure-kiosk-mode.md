---
title: Konfigurieren des Microsoft Edge-Kioskmodus
ms.author: aguta
author: aguta
manager: srugh
ms.date: 01/21/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Konfigurieren des Microsoft Edge-Kioskmodus
ms.openlocfilehash: be353a0e13e9234de40296a2e8dcc31b1b800f52
ms.sourcegitcommit: 8a88fd38bdb5e132e89bf17dd2b5fb72f5d1b4b9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/22/2021
ms.locfileid: "11297471"
---
# Konfigurieren des Microsoft Edge-Kioskmodus

In diesem Artikel wird beschrieben, wie Sie die Optionen für den Microsoft Edge-Kioskmodus Ihren Anforderungen entsprechend konfigurieren können. Eine Roadmap zukünftiger Features wird ebenfalls vorgestellt.

> [!NOTE]
> Dieser Artikel bezieht sich auf Microsoft Edge Version 87 oder neuer.

## Übersicht

Im Microsoft Edge-Kiosk-Modus sind zwei gesperrte Browserumgebungen verfügbar, damit Organisationen optimale Umgebungen für ihre Kunden gestalten, verwalten und anbieten können. Die folgenden gesperrten Umgebungen sind verfügbar:  

- **Digital/Interactive Signage–** Zeigt eine bestimmte Website im Vollbildmodus an.
- **Öffentliches Browsen** – Führt eine eingeschränkte Version mit mehreren Registerkarten von Microsoft Edge aus.

In beiden Fällen wird eine Microsoft Edge-InPrivate-Sitzung ausgeführt, wodurch die Benutzerdaten geschützt sind.

## Einrichten des Microsoft Edge-Kioskmodus

Ein anfänglicher Satz von Kioskmodusfeatures steht zum Testen mit Microsoft Edge Stable-Kanal, Version 87, zur Verfügung. Sie können die neueste Version von [Microsoft Edge (offizieller Stable-Kanal) herunterladen.](https://www.microsoft.com/edge)

### Unterstützte Features im Kioskmodus

In der folgenden Tabelle sind die im Kioskmodus unterstützten Features aufgeführt.

|Feature|Digital\Interactive Signage|Öffentliches Surfen|Verfügbar mit Microsoft Edge Version (und höher)|
|-|-|-|-|
|InPrivate-Navigation|„Y“ zugeordnet ist|„Y“ zugeordnet ist|87|
|Zurücksetzen bei Inaktivität|„Y“ zugeordnet ist|„Y“ zugeordnet ist|87|
|[Schreibgeschützte Adressleiste](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskaddressbareditingenabled) (Richtlinie) |N|„Y“ zugeordnet ist |87|
|[Löschen von Downloads beim Beenden](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskdeletedownloadsonexit) (Richtlinie)  | „Y“ zugeordnet ist|„Y“ zugeordnet ist |87|
|F11 blockiert (Vollbild-/Ein-/Austritt) | „Y“ zugeordnet ist | „Y“ zugeordnet ist | 87 |
|F12 blockiert (Entwicklertools starten) | „Y“ zugeordnet ist | „Y“ zugeordnet ist | 87 |
| Unterstützung für mehrere Registerkarten | N| „Y“ zugeordnet ist| 87|
|Sitzung beenden | N| „Y“ zugeordnet ist| 88|
|Alle internen Microsoft Edge-URLs werden blockiert, mit *Ausnahme* von edge://downloads und *edge://print* |N|„Y“ zugeordnet ist|88|
| STRG+N blockiert (neues Fenster öffnen) | „Y“ zugeordnet ist | „Y“ zugeordnet ist | 89 |
| STRG+T blockiert (neue Registerkarte öffnen) | N | „Y“ zugeordnet ist | 89 |
|Einstellungen und vieles mehr (...) zeigt nur die erforderlichen Optionen an.  |N |„Y“ zugeordnet ist |89 |

> [!NOTE]
> Im Laufe der Weiterentwicklung des Kioskmodus werden auch weitere Features verfügbar sein.

## Verwenden der Kioskmodus-Features

Microsoft Edge Kioskmodusfeatures können mit den folgenden Windows 10-Befehlszeilenoptionen aufgerufen werden:

- Kioskmodus "Digitale/interaktive Beschilderung": `msedge.exe --kiosk www.contoso.com --edge-kiosk-type=fullscreen`
- Kioskmodus "Öffentliches Surfen": `msedge.exe --kiosk www.contoso.com --edge-kiosk-type=public-browsing`

### Zusätzliche Befehlszeilenoptionen

- `--no-first-run` : Deaktivieren Sie die erste Ausführung von Microsoft Edge.
- `--kiosk-idle-timeout-minutes` : Ändern Sie den Zeitraum (in Minuten) nach der letzten Benutzeraktivität, nach dem der Microsoft Edge-Kioskmodus die Benutzersitzung zurücksetzt. Die folgenden Werte werden unterstützt:

  - Standardwerte
    - Vollbildmodus – deaktiviert
    - Öffentliches Surfen – 5 Minuten
  - Zulässige Werte
    - 0 – deaktiviert den Timer
    - 1-1440 Minuten für das Zurücksetzen für den Leerlaufzeit-Zeitgeber

## Supportrichtlinien für den Kioskmodus

Verwenden Sie eine der in der folgenden Tabelle aufgeführten Microsoft Edge-Richtlinien, um die Kioskerfahrung für den von Ihnen konfigurierten Microsoft Edge-Kioskmodustyp zu verbessern. Weitere Informationen zu diesen Richtlinien finden Sie unter [Microsoft Edge – Browser policy reference](https://docs.microsoft.com/deployedge/microsoft-edge-policies).

> [!NOTE]
> Die Richtlinienkonfiguration ist nicht auf die in der folgenden Tabelle aufgeführten Richtlinien beschränkt. Es sollten jedoch zusätzliche Richtlinien getestet werden, um sicherzustellen, dass die Funktionalität des Kioskmodus nicht negativ beeinträchtigt wird.

|Gruppenrichtlinie|Digital\Interactive Signage|Einzel-App für öffentliches Browsen|
|--|--|--|
|[Drucken](https://docs.microsoft.com/deployedge/microsoft-edge-policies#printing-policies) | „Y“ zugeordnet ist|„Y“ zugeordnet ist |
|[HomePageLocation](https://docs.microsoft.com/deployedge/microsoft-edge-policies#homepagelocation) |N | „Y“ zugeordnet ist|
|[ShowHomeButton](https://docs.microsoft.com/deployedge/microsoft-edge-policies#showhomebutton) |N | „Y“ zugeordnet ist|
|[NewTabPageLocation](https://docs.microsoft.com/deployedge/microsoft-edge-policies#newtabpagelocation) |N |„Y“ zugeordnet ist |
|[FavoritesBarEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#favoritesbarenabled) |N |„Y“ zugeordnet ist |
|[URLAllowlist](https://docs.microsoft.com/deployedge/microsoft-edge-policies#urlallowlist) |„Y“ zugeordnet ist |„Y“ zugeordnet ist |
|[URLBlocklist](https://docs.microsoft.com/deployedge/microsoft-edge-policies#urlblocklist) |„Y“ zugeordnet ist | „Y“ zugeordnet ist|
|[ManagedSearchEngines](https://docs.microsoft.com/deployedge/microsoft-edge-policies#managedsearchengines) |N | „Y“ zugeordnet ist|
|[UserFeedbackAllowed](https://docs.microsoft.com/deployedge/microsoft-edge-policies#userfeedbackallowed) |N | „Y“ zugeordnet ist|
|[VerticalTabsAllowed](https://docs.microsoft.com/deployedge/microsoft-edge-policies#verticaltabsallowed) | N|„Y“ zugeordnet ist |
|[SmartScreen-Einstellungen](https://docs.microsoft.com/deployedge/microsoft-edge-policies#smartscreen-settings-policies) |„Y“ zugeordnet ist |„Y“ zugeordnet ist |

## Microsoft Edge mit zugewiesenem Zugriff

### Einzel-App-Kiosk

Microsoft Edge unterstützt derzeit eine Teilmenge der gleichen Kioskmodustypen der Vorgängerversion von Microsoft Edge für den zugewiesenen Zugriff mit einer einzelnen App mit den folgenden Sperrmodus-Funktionen: Digitale/interaktive Beschilderung und Öffentliches Browsen.  

Der Kioskmodus mit zugewiesenem Zugriff ist derzeit für Tests mit dem neuesten  [Windows10 Insider Preview-Build](https://insider.windows.com/), Version 20215 oder höher, und mit dem  [Microsoft Edge Dev Channel](https://www.microsoftedgeinsider.com/download), Version 87.0.644.4 oder höher, verfügbar.

**Wie erhalte ich den Windows Insider Preview-Build?**

Wenn Sie einen Windows10 Insider Preview-Build auf einem PC installieren möchten, folgen Sie den Anweisungen unter  [Erste Schritte mit Windows10 Insider Preview-Builds](https://docs.microsoft.com/windows-insider/get-started).

### Multi-App-Kiosk

Microsoft Edge kann unter Windows10 mit [zugewiesenem Multi-App-Zugriff](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps) ausgeführt werden, was dem Kioskmodustyp „Normales Browsen” von Microsoft Edge Legacy entspricht. Befolgen Sie die Anweisungen zum Einrichten eines Multi-App-Kiosks, um Microsoft Edge mit zugewiesenen [Multi-App-Zugriffen zu konfigurieren.](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps) (Die AUMID für den Stable-Kanal von Microsoft Edge ist **MSEdge**.)

Wenn Sie Microsoft Edge mit zugewiesenen Zugriffen mit mehreren Apps verwenden, können Sie den Microsoft Edge Kiosk so konfigurieren, dass er die[Microsoft Edge-Browserrichtlinien](https://review.docs.microsoft.com/DeployEdge/microsoft-edge-policies) verwendet, um die Browsererfahrung so zu konfigurieren, dass Ihre individuellen Anforderungen erfüllt werden.

### Konfigurieren mithilfe der Windows-Einstellungen

Die Windows-Einstellungen sind die einfachste Möglichkeit zum Einrichten von ein oder zwei Einzel-App-Kioskgeräten. Führen Sie die folgenden Schritte aus, um einen Einzel-App-Kioskcomputer einzurichten.

1. Installieren Sie die neueste Windows 10 Insider Preview-Version (20215 oder höher). Folgen Sie den Anweisungen unter [Erste Schritte mit Windows 10 Insider Preview-Builds](https://docs.microsoft.com/windows-insider/get-started).
2. Installieren Sie die neueste Version des [Microsoft Edge Stable-Kanals,](https://www.microsoft.com/edge)Version 87 oder höher.  Um die neuesten Features zu testen, können Sie den neuesten [Microsoft Edge Dev-Kanal,](https://www.microsoftedgeinsider.com/download)Version 89 oder höher, herunterladen.

   > [!IMPORTANT]
   > Da eine Installation auf Geräteebene erforderlich ist, wird nur ein nicht-Canary-Kanal unterstützt.

3. Öffnen Sie auf dem Kiosk-Computer die Windows-Einstellungen, und geben Sie im Suchfeld "Kiosk" ein. Wählen Sie  **Einen Kiosk einrichten (zugewiesener Zugriff)** aus, das im nächsten Screenshot dargestellt ist, um das Dialogfeld zum Erstellen des Kiosks zu öffnen.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-1-assigned-access.png" alt-text="Einrichten eines Kiosks mit zugewiesenem Zugriff":::

4. Klicken Sie auf der Seite **Einen Kiosk einrichten**  auf **Erste Schritte**.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-2-get-started.png" alt-text="Seite "Kiosk" – erste Schritte":::

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

## Funktionale Beschränkungen

Die Veröffentlichung dieser Preview-Version des Kioskmodus erfolgt im Rahmen unserer kontinuierlichen Bemühungen, das Produkt zu verbessern und neue Features hinzuzufügen.

Es wird empfohlen, dies zu deaktivieren:

- [StartupBoostEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#startupboostenabled)
- [InternetExplorerIntegrationLevel](https://docs.microsoft.com/deployedge/microsoft-edge-policies#internetexplorerintegrationlevel)
- [Erweiterungen](https://docs.microsoft.com/deployedge/microsoft-edge-policies#extensions-policies)
- [BackgroundModeEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#backgroundmodeenabled)

## Roadmap

### Anfang 2021

Unterstützung und Funktionen, die hinzukommen werden:

- Allgemeine Verfügbarkeit des Microsoft Edge-Kioskmodus mit zugewiesener Zugriffs-Einzel-App unter Windows 10 1909 und höher.
- Zusätzliche Features für Parität mit Vorgängerversion von Microsoft Edge.
- Integration in Intune zum Konfigurieren von Geräten über die Profil-Benutzerumgebung im Kioskmodus.
- Zusätzliche Tastenkombinationen werden blockiert.
- Schränken Sie den Start anderer Anwendungen über den Browser ein.

## Weitere Informationen

- [Konfigurieren von Kiosken und digitalen Anmeldungen in Windows-Desktopeditionen](https://docs.microsoft.com/windows/configuration/kiosk-methods)
- [Bereitstellen des Microsoft Edge Legacy-Kioskmodus](https://aka.ms/edgekioskmode)
- [Planen Ihrer Bereitstellung von Microsoft Edge](deploy-edge-plan-deployment.md)
- [Angebotsseite für Microsoft Edge für Unternehmen](https://aka.ms/EdgeEnterprise)
