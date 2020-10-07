---
title: Konfigurieren des Microsoft Edge-Kioskmodus
ms.author: aguta
author: aguta
manager: srugh
ms.date: 10/05/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Konfigurieren des Microsoft Edge-Kioskmodus
ms.openlocfilehash: 799b3dd4b7fc96f0b8e5cb718bca98fd4f38ec15
ms.sourcegitcommit: 78905f66f4a6590a57c8f2bf808af92106b62996
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/05/2020
ms.locfileid: "11094862"
---
# Konfigurieren des Microsoft Edge-Kioskmodus

In diesem Artikel wird beschrieben, wie Sie die Optionen für den Microsoft Edge-Kioskmodus Ihren Anforderungen entsprechend konfigurieren können. Eine Roadmap zukünftiger Features wird ebenfalls vorgestellt.

> [!NOTE]
> Dieser Artikel bezieht sich auf Microsoft Edge Version 87 oder neuer.

## Übersicht

Im Microsoft Edge-Kiosk-Modus sind zwei gesperrte Browserumgebungen verfügbar, damit Organisationen optimale Umgebungen für ihre Kunden gestalten, verwalten und anbieten können. Die folgenden gesperrten Umgebungen sind verfügbar:  

- Bei der digitalen/interaktiven Beschilderung wird eine bestimmte Website im Vollbildmodus angezeigt.
- Bei der Umgebung für öffentliches Surfen wird eine eingeschränkte Version von Microsoft Edge mit mehreren Tabs ausgeführt.

In beiden Fällen wird eine Microsoft Edge-InPrivate-Sitzung ausgeführt, wodurch die Benutzerdaten geschützt sind.

## Einrichten des Microsoft Edge-Kioskmodus

Jetzt können Sie mit Microsoft Edge Canary, Version 87, eine erste Sammlung von Kioskmodus-Features testen. Sie können Microsoft Edge Canary über die Seite [Microsoft Edge Insider Channels](https://www.microsoftedgeinsider.com/download) herunterladen.

### Kioskmodus-Features

Die folgenden Features sind verfügbar:

- Die InPrivate-Navigation schützt Benutzerdaten durch das Löschen von Browserdaten und Downloads, wenn die Sitzung beendet wird.
- Eine Richtlinie zum Konfigurieren des Löschens von Downloads beim Beenden.
- Die Option zum Zurücksetzen der Benutzersitzung nach einer bestimmten Zeit der Inaktivität.
- Eine erste Reihe verfügbarer Sperrfunktionen. Die folgenden Funktionen sind verfügbar:

  - Maus-Kontextmenü
  - F12 Entwicklertools
  - F11 Beenden des Vollbildmodus (im Vollbildmodus)
  - Blockieren der ersten Reihe von *Edge://*-Seiten

> [!NOTE]
> Im Laufe der Weiterentwicklung des Kioskmodus werden auch weitere Features verfügbar sein.

## Verwenden der Kioskmodus-Features

Die Microsoft Edge-Kioskmodus-Features können mit den folgenden Windows 10-Befehlszeilenoptionen aufgerufen werden:

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

## Microsoft Edge mit zugewiesenem Zugriff

### Einzel-App-Kiosk

Microsoft Edge unterstützt derzeit eine Teilmenge der gleichen Vorgängerversionen der Microsoft Edge-Kioskmodustypen für den zugewiesenen Zugriff mit einer App mit den folgenden Sperrmoduserfahrungen, digitaler/interaktiver Beschilderung und Public-Browsing.  

Der Kioskmodus mit zugewiesenem Zugriff ist derzeit für Tests mit dem neuesten  [Windows10 Insider Preview-Build](https://insider.windows.com/), Version 20215 oder höher, und mit dem  [Microsoft Edge Dev Channel](https://www.microsoftedgeinsider.com/download), Version 87.0.644.4 oder höher, verfügbar.

**Wie erhalte ich den Windows Insider Preview-Build?**

Wenn Sie einen Windows10 Insider Preview-Build auf einem PC installieren möchten, folgen Sie den Anweisungen unter  [Erste Schritte mit Windows10 Insider Preview-Builds](https://docs.microsoft.com/windows-insider/get-started).

### Multi-App-Kiosk

Microsoft Edge kann unter Windows10 mit [zugewiesenem Multi-App-Zugriff](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps) ausgeführt werden, was dem Kioskmodustyp „Normales Browsen” von Microsoft Edge Legacy entspricht. Zum Konfigurieren von Microsoft Edge mit zugewiesenem Multi-App-Zugriff folgen Sie den Anweisungen unter [Einrichten eines Multi-App-Kiosks](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps). (Die AUMID für den Stable-Kanal von Microsoft Edge ist **MSEdge**.)

Für das Konfigurieren von Microsoft Edge mit zugewiesenem Multi-App-Zugriff können Sie die [Microsoft Edge-Browserrichtlinien](https://review.docs.microsoft.com/en-us/DeployEdge/microsoft-edge-policies) verwenden, um das Browsingerlebnis Ihren individuellen Anforderungen entsprechend zu konfigurieren.

### Konfigurieren mithilfe der Windows-Einstellungen

Die Windows-Einstellungen sind die einfachste Möglichkeit zum Einrichten von ein oder zwei Einzel-App-Kioskgeräten. Führen Sie die folgenden Schritte aus, um einen Einzel-App-Kioskcomputer einzurichten.

1. Installieren Sie die neueste Windows 10 Insider Preview-Version (20215 oder höher). Folgen Sie den Anweisungen unter [Erste Schritte mit Windows 10 Insider Preview-Builds](https://docs.microsoft.com/windows-insider/get-started).
2. Installieren Sie die neueste Version von [Microsoft Edge Dev Channel](https://www.microsoftedgeinsider.com/download), Version 87.0.644.4 oder höher.

   > [!IMPORTANT]
   > Da eine Installation auf Geräteebene erforderlich ist, wird nur ein nicht-Canary-Kanal unterstützt.

3. Öffnen Sie auf dem Kiosk-Computer die Windows-Einstellungen, und geben Sie im Suchfeld "Kiosk" ein. Wählen Sie  **Einen Kiosk einrichten (zugewiesener Zugriff)** aus, das im nächsten Screenshot dargestellt ist, um das Dialogfeld zum Erstellen des Kiosks zu öffnen.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-1-assigned-access.png" alt-text="Einrichten eines Kiosks mit zugewiesenem Zugriff":::

4. Klicken Sie auf der Seite **Einen Kiosk einrichten**  auf **Erste Schritte**.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-2-get-started.png" alt-text="Einrichten eines Kiosks mit zugewiesenem Zugriff":::

5. Geben Sie einen Namen ein, um ein neues Kioskkonto zu erstellen, oder wählen Sie ein vorhandenes Konto aus der Dropdownliste aus, und klicken Sie dann auf  **Weiter**.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-3-create-account.png" alt-text="Einrichten eines Kiosks mit zugewiesenem Zugriff":::

6. Wählen Sie auf der Seite **Kiosk-App auswählen**  die Option **Microsoft Edge** aus, und klicken Sie dann auf  **Weiter**.

   > [!NOTE]
   > Dies gilt nur für Microsoft Edge Dev, Beta und Stable-Kanäle.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-4-pick-app.png" alt-text="Einrichten eines Kiosks mit zugewiesenem Zugriff":::

7. Wählen Sie eine der folgenden Optionen für die Darstellung von Microsoft Edge aus, wenn er im Kioskmodus ausgeführt wird:

   - Digitale/interaktive Beschilderung: Zeigt eine bestimmte Website im Vollbildmodus an, dabei wird Microsoft Edge ausgeführt.
   - Öffentliches Surfen: Führt eine eingeschränkte Version von Microsoft Edge mit mehreren Tabs aus.

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-5a-digital-sign.png" alt-text="Einrichten eines Kiosks mit zugewiesenem Zugriff":::

8. Wählen Sie ** Weiter** aus.
9. Geben Sie die URL ein, die beim Start des Kiosks geladen werden soll.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-6-enter-url.png" alt-text="Einrichten eines Kiosks mit zugewiesenem Zugriff":::

10. Übernehmen Sie den Standardwert von 5 Minuten für die Leerlaufzeit, oder geben Sie einen eigenen Wert ein.

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-7-enter-idle-time.png" alt-text="Einrichten eines Kiosks mit zugewiesenem Zugriff":::

11. Klicken Sie auf  **Weiter**.
12. Schließen Sie das Fenster  **Einstellungen** , um Ihre Auswahl zu speichern und anzuwenden.

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode--8-done.png" alt-text="Einrichten eines Kiosks mit zugewiesenem Zugriff" und "Laut vorlesen").
  - Sperrung weiterer *edge://*-Seiten (z. B. *Edge://Settings*)
  - Konfigurieren der Druckoptionen-Benutzeroberfläche
  - Einschränken des Datei-Explorers auf den Downloadordner

### Anfang 2021

Unterstützung und Funktionen, die hinzukommen werden:

- Allgemeine Verfügbarkeit des Microsoft Edge-Kioskmodus mit zugewiesenem Zugriff (Einzel-App) für Windows.
- Zusätzliche Features für Parität mit Vorgängerversion von Microsoft Edge
- Integration in Intune zum Konfigurieren von Geräten über die Profil-Benutzerumgebung im Kioskmodus

## Weitere Informationen

- [Konfigurieren von Kiosken und digitalen Anmeldungen in Windows-Desktopeditionen](https://docs.microsoft.com/windows/configuration/kiosk-methods)
- [Bereitstellen des Microsoft Edge Legacy-Kioskmodus](https://aka.ms/edgekioskmode)
- [Planen Ihrer Bereitstellung von Microsoft Edge](deploy-edge-plan-deployment.md)
- [Angebotsseite für Microsoft Edge für Unternehmen](https://aka.ms/EdgeEnterprise)
