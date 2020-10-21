---
title: Zugreifen auf die alte Version von Microsoft Edge
ms.author: jtkim
author: dan-wesley
manager: srugh
ms.date: 08/17/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Informationen für den Zugriff auf die alte Version von Microsoft Edge
ms.openlocfilehash: e4733d020f3a681ded50e5a087fe086d39362201
ms.sourcegitcommit: f7f7eb69d2298b0f9779a9fd28e3c4e297ef2e05
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125517"
---
# Zugreifen auf Microsoft Edge Legacy nach der Installation der neuen Version von Microsoft Edge

Informationen für den Zugriff auf Microsoft Edge Legacy nach der Installation der neuen Version von Microsoft Edge.

> [!NOTE]
> Dieser Artikel bezieht sich auf den Microsoft Edge [Stable-Kanal](microsoft-edge-channels.md).

Die meisten Organisationen möchten Microsoft Edge Legacy sicherlich durch die neue Version ersetzen, es gibt aber einige Situationen, in denen Benutzer auf beide Versionen zugreifen müssen. Zum Beispiel:

- Helpdesk- und Supportmitarbeiter, die mit Benutzern interagieren, die eine oder beide Versionen von Microsoft Edge verwenden.
- Entwickler, die Support für Kunden bereitstellen, die eine oder beide Versionen von Microsoft Edge verwenden.

> [!IMPORTANT]
> Die parallele Ausführung von der Vorgängerversion (Microsoft Edge Legacy) sowie der neuen Version von Microsoft Edge wird für den Einsatz in der Produktion nicht empfohlen. Diese Konfiguration sollte nur in bestimmten Fällen verwendet werden, in denen Tests mit beiden Browserversionen erforderlich sind.
>
> Der Support für die Desktop-App von Microsoft Edge Legacy läuft am 9. März 2021 zugunsten des neuen Microsoft Edge aus. Dies bedeutet, dass Microsoft Edge Legacy nach diesem Datum keine Sicherheitsupdates mehr erhält. Diese Änderung gilt für alle Funktionen der Desktop-App von Microsoft Edge Legacy. [Weitere Informationen](https://techcommunity.microsoft.com/t5/microsoft-365-blog/microsoft-365-apps-say-farewell-to-internet-explorer-11-and/ba-p/1591666).

## Vorbemerkungen
> [!NOTE]
> Ab Windows 10, Version 20H2, ist Microsoft Edge Legacy nicht mehr enthalten. Ab dieser Version von Windows 10 wird die parallele Verwendung nicht mehr unterstützt.

Die Verfahren in diesem Artikel gelten für Systeme, die mit den neuesten Sicherheitsupdates aktualisiert wurden. Wenn die neue Version von Microsoft Edge installiert ist, wird die alte Version (Microsoft Edge Legacy) ausgeblendet. Bei allen Versuchen, die alte Version von Microsoft Edge zu starten, wird der Benutzer standardmäßig auf die neu installierte Version von Microsoft Edge umgeleitet. In diesem Artikel wird beschrieben, wie Sie Microsoft Edge Legacy nach der Installation von Microsoft Edge weiterhin verwenden können.

## Schnellstart: Parallele Verwendung von Microsoft Edge Beta Channel und Microsoft Edge Legacy

Bevor Sie die ausführlichen Anweisungen in diesem Artikel verwenden, sollten Sie die folgenden zwei Schritte beachten, damit Ihre Benutzer Microsoft Edge Legacy und Microsoft Edge [Beta Channel](microsoft-edge-channels.md) parallel ausführen können.

1. Verhindern Sie die automatische Installation des Stable-Kanals von Microsoft Edge durch [Windows Update](https://support.microsoft.com/help/12373/windows-update-faq).

   > [!TIP]
   > Verwenden Sie das [Blocker-Toolkit](microsoft-edge-blocker-toolkit.md) zum Deaktivieren der automatischen Bereitstellung von Microsoft Edge.

2. Installieren Sie den [Beta-Kanal](https://www.microsoft.com/edge/business/download) der neuen Version von Microsoft Edge.

   > [!NOTE]
   > Lesen Sie [Weitere Informationen](#additional-information) zu den Registrierungsschlüsseleinstellungen.

Diese parallele Lösung ist weniger komplex und erfordert weniger Verwaltungsaufwand als die in diesem Artikel beschriebene detaillierte Lösung. Diese Lösung bedeutet jedoch, dass Sie den Beta-Kanal anstelle des Stable-Kanals ausführen müssen.

## Parallele Verwendung von Microsoft Edge Stable Channel und Microsoft Edge Legacy

Wenn Sie den stabilen Kanal der nächsten Version von Microsoft Edge auf Systemebene installieren, wird die aktuelle Version (Microsoft Edge Legacy) ausgeblendet. Wenn Sie Benutzern die parallele Verwendung beider Versionen von Microsoft Edge in Windows ermöglichen möchten, können Sie diese Oberfläche aktivieren, indem Sie die Gruppenrichtlinie **Microsoft Edge-Browser im Parallelbetrieb zulassen** auf **Aktiviert** festlegen.

Diese Gruppenrichtlinie ist [hier](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#allowsxs) dokumentiert.

### So richten Sie die Richtlinie für den Parallelbetrieb des Browsers ein:

1. Installieren Sie die Richtliniendefinitionen über [Microsoft Edge for Business](https://www.microsoft.com/edge/business/download).

   - Wählen Sie KANAL/BUILD und PLATTFORM aus, die Sie verwenden möchten, und klicken Sie dann auf RICHTLINIENDATEIEN ABRUFEN.
   - Extrahieren Sie die gezippten Dateien.
   - Kopieren sie msedge.admx und msedgeupdate.admx in das Verzeichnis `C:\Windows\PolicyDefinitions`.
   - Kopieren Sie "msedge.adml" und "msedgeupdate.adml" (aus dem entsprechenden Verzeichnis der Sprache bzw. des Gebietsschemas) in das `C:\Windows\PolicyDefinitions\[APPROPRIATE LANGUAGE/LOCALE]`-Verzeichnis.

2. Öffnen Sie den Gruppenrichtlinien-Editor (gpedit.msc).
3. Wechseln Sie unter **Computerkonfiguration** zu *Administrative Vorlagen>Microsoft Edge Update>Anwendungen*.

    > [!NOTE]
    > Wenn der Ordner *Microsoft Edge Update* nicht angezeigt wird, überprüfen Sie, ob Schritt 1 ordnungsgemäß abgeschlossen wurde.

4. Doppelklicken Sie unter **Anwendungen** auf „Microsoft Edge-Browser im Parallelbetrieb zulassen”. Lesen Sie unsere [Leitlinien für bewährte Methoden](#best-practice-guidance), bevor Sie mit dem nächsten Schrittfortfahren.

    > [!NOTE]
    > Diese Gruppenrichtlinie ist standardmäßig auf „Nicht konfiguriert” festgelegt, was bewirkt, dass Microsoft Edge Legacy nach der Installation der neuen Version von Microsoft Edge ausgeblendet wird.

5. Wählen Sie **Aktiviert**, und klicken Sie dann auf **OK**.  

Durch das Festlegen dieser Richtlinie erhält der folgende Registrierungsschlüssel den Wert "00000001":

- Legende: `Computer\HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate`
- Name des Wertes: `Allowsxs`
- Werttyp: `'REG_DWORD'`

#### Leitlinien für bewährte Methoden

Für die bestmögliche Benutzerfreundlichkeit sollte die Option **Microsoft Edge-Browser im Parallelbetrieb zulassen** aktiviert werden, bevor die neue Version von Microsoft Edge auf den Geräten der Benutzer bereitgestellt wird.

Wenn die Gruppenrichtlinie aktiviert ist, nachdem Microsoft Edge bereitgestellt wurde, sind die folgenden Nebenwirkungen und erforderliche Aktionen zu beachten:

1. **Microsoft Edge-Browser im Parallelbetrieb zulassen** wird erst wirksam, nachdem das Installationsprogramm für die neue Version von Microsoft Edge erneut ausgeführt wurde.

   > [!NOTE]
   > Das Installationsprogramm kann direkt oder automatisch ausgeführt werden, wenn die neue Version von Microsoft Edge aktualisiert wird.

2. Microsoft Edge Legacy muss erneut an "Start" oder die Taskleiste angeheftet werden, da die Anheftung migriert wird, wenn die neue Version von Microsoft Edge bereitgestellt wird.
3. Sites, die an "Start" oder die Taskleiste für Microsoft Edge Legacy angeheftet waren, werden auf die neue Version von Microsoft Edge migriert.

## Weitere Informationen

Nachdem die Systeme vollständig aktualisiert sind und der Stable-Kanal der nächsten Version von Microsoft Edge installiert ist, werden der folgende Registrierungsschlüssel und -wert festgelegt:

- Legende: `Computer\HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\EdgeUpdate\ClientState\{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}`
- Schlüsselwert: `BrowserReplacement`

  > [!IMPORTANT]
  > Dieser Schlüssel wird bei jeder Aktualisierung des Microsoft Edge Stable-Kanals überschrieben. Als bewährte Methode wird empfohlen, diesen Schlüssel NICHT zu löschen, damit Benutzer auf beide Versionen von Microsoft Edge zugreifen können.

## Weitere Informationen

- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)
- [Windows-Updates zur Unterstützung von Microsoft Edge](microsoft-edge-sysupdate-windows-updates.md)
