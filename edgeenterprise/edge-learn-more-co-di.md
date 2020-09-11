---
title: ClickOnce und DirectInvoke in Microsoft Edge
ms.author: kele
author: dan-wesley
manager: srugh
ms.date: 09/10/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Erfahren Sie mehr über ClickOnce und DirectInvoke in Microsoft Edge.
ms.openlocfilehash: 1d4e08c0ce3ee2afec7968cd892f77ef7bdc3fff
ms.sourcegitcommit: 4c0b84b03e686a7a2989ce2187dbadf35418104a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012795"
---
# Grundlegendes zu den ClickOnce- und DirectInvoke-Features in Microsoft Edge

ClickOnce und DirectInvoke sind Features, die in IE und Microsoft Edge (Version 45 und früher) verfügbar sind und die Verwendung eines Dateihandlers zum Herunterladen von Dateien von einer Website unterstützen. Obwohl sie unterschiedlichen Zwecken dienen, können Websites mit beiden Features angeben, dass eine zum Herunterladen angeforderte Datei an einen Dateihandler auf dem Gerät des Benutzers weitergeleitet wird. ClickOnce-Anforderungen werden vom systemeigenen Dateihandler in Windows verarbeitet. DirectInvoke-Anforderungen werden von einem registrierten Dateihandler verarbeitet, der von der Website angegeben wird, die die Datei hostet.

Weitere Informationen zu Features und Beschränkungen finden Sie in den häufig gestellten Fragen.

- [ClickOnce](https://docs.microsoft.com/visualstudio/deployment/clickonce-security-and-deployment?view=vs-2019)
- [DirectInvoke]( https://technet.microsoft.com/learning/jj215788(v=vs.94).aspx)

> [!NOTE]
> Derzeit bietet Chromium keine systemeigene Unterstützung für ClickOnce oder DirectInvoke.

## Übersicht: Voraussetzungen und Prozess

Damit ClickOnce und DirectInvoke wie vorgesehen funktionieren und der Dateihandler erfolgreich angefordert werden kann, muss der Dateihandler im Betriebssystem als unterstützend für ClickOnce oder DirectInvoke registriert sein. Diese Registrierung erfolgt in der Regel, wenn das ursprüngliche Betriebssystem installiert wird oder ein neu installiertes Programm die Verwendung von DirectInvoke für Updates anfordert.

Wenn eine Website eine Downloadanforderung erhält, für die ClickOnce oder DirectInvoke erforderlich ist, werden die folgenden Aktionen ausgeführt:

- Die Website fordert den Browser auf, einen bestimmten Dateihandler zu verwenden.
- Der Browser überprüft die Betriebssystemregistrierung, um festzustellen, ob der Dateihandler für den angeforderten Dateityp registriert ist.
- Wenn der Dateihandler registriert ist, ruft der Browser den Dateihandler auf und übergibt die URL als Argument an den Dateihandler.
- Der Dateihandler verarbeitet die URL und lädt die Datei herunter.

  > [!NOTE]
  > Die URL wird verwendet, um die Quelle der Datei sowie alle Parameter zu bestimmen, die beim Zugriff auf die Datei verwendet werden sollen.  Zum Beispiel: Endpunkte, ein Manifest oder Metadaten.

## Anwendungsfälle

Die folgenden Anwendungsfälle sind repräsentativ.

Sie können ClickOnce verwenden, um Software auf Geräten mit minimaler Benutzerinteraktion einfach bereitzustellen und zu aktualisieren. Benutzer können eine Windows-Anwendung installieren und ausführen, indem sie auf einen Link auf einer Website klicken. Bei ordnungsgemäßer Konfiguration kann die ClickOnce-Anwendung Programme installieren, ohne dass Benutzer Konfigurationen für das Installationsprogramm festlegen müssen. Zum Beispiel Dateispeicherorte, zu installierende Optionen usw.

DirectInvoke-Anwendungsfälle hängen von der Absicht der Website ab, die DirectInvoke anfordert. Zum Beispiel die kollaborative Dateibearbeitungsfunktion von Microsoft Word. Anstatt auf einen Link zu klicken und die gesamte Kopie eines Dokuments herunterzuladen, an dem Sie mit Ihren Kollegen arbeiten, können Sie mit DirectInvoke die Teile des Dokuments herunterladen, die geändert wurden. Dieses Verfahren reduziert die Menge der übertragenen Daten und kann die zum Öffnen des Dokuments benötigte Zeit verkürzen.  

## Aktuelle Unterstützung für ClickOnce und DirectInvoke in Microsoft Edge

Unterstützung für ClickOnce und DirectInvoke:

- ClickOnce und DirectInvoke werden standardmäßig für alle Windows-Benutzer unterstützt.

  > [!NOTE]
  > Benutzer, die ClickOnce-Unterstützung deaktivieren möchten, können zu *edge://flags/#edge-click-once* wechseln und **Deaktiviert** aus der Dropdownliste auswählen. Anschließend müssen Sie den Browser **neu starten**.

- ClickOnce und DirectInvoke werden auf anderen Plattformen als Windows nicht unterstützt.

## Sicherheit beim Umgang mit ClickOnce- und DirectInvoke-Dateien

ClickOnce und DirectInvoke sind durch den URL-Bewertungsdienst von Microsoft Defender SmartScreen geschützt.

Wenn eine ClickOnce- oder DirectInvoke-Anforderung vom URL-Bewertungsdienst von Microsoft Defender SmartScreen als unsicher gekennzeichnet wird, werden Benutzern mit aktiviertem ClickOnce oder DirectInvoke zwei Popups angezeigt.

Das erste Popup fragt den Benutzer, ob er die Datei öffnen möchte. Dieses Popup wird unabhängig davon angezeigt, ob die Datei als sicher oder unsicher gekennzeichnet wurde. Der Benutzer kann die **Datei als unsicher melden**, die Anforderung **abbrechen** oder auf **Öffnen** klicken, um den Vorgang fortzusetzen.

   ![Aufforderung zum Öffnen der Datei](./media/edge-learn-more-co-di/edge-clickonce-modal-1.png)

Wenn der Benutzer versucht, die Datei zu öffnen, und die Datei als unsicher gekennzeichnet wurde, wird ein zweites Popup angezeigt.  Dieses Popup warnt den Benutzer, dass die Datei als unsicher gekennzeichnet wurde, und fragt ihn, ob er sicher ist, dass er die Datei herunterladen möchte.

Das zweite Popup wird nur angezeigt, wenn:

- die Datei eine ClickOnce- oder DirectInvoke-Datei ist
- ClickOnce oder DirectInvoke aktiviert sind
- die Datei als unsicher gekennzeichnet wird

 ![Aufforderung zum Öffnen einer unsicheren Datei](./media/edge-learn-more-co-di/edge-clickonce-modal-2.png)

> [!NOTE]
> Wenn ClickOnce oder DirectInvoke deaktiviert sind, werden angeforderte Dateien als reguläre Downloads behandelt und, wenn sie als unsicher gekennzeichnet sind, als unsicher markiert. Dies entspricht der Behandlung von anderen unsicheren Downloads.

## ClickOnce- und DirectInvoke-Richtlinien

Es gibt zwei Gruppenrichtlinien, mit denen Sie ClickOnce und DirectInvoke für Unternehmensbenutzer aktivieren oder deaktivieren können. Diese beiden Richtlinien sind [ClickOnceEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#clickonceenabled) und [DirectInvokeEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#directinvokeenabled). Diese beiden Richtlinien sind im Gruppenrichtlinien-Editor mit "Zulassen, das Benutzer Dateien mit dem ClickOnce-Protokoll öffnen" und "Zulassen, dass Benutzer Dateien mit dem DirectInvoke-Protokoll öffnen" bezeichnet.

## ClickOnce- und DirectInvoke-Verhalten

Die folgenden Beispiele zeigen die Dateiverarbeitung, wenn ClickOnce und DirectInvoke aktiviert oder deaktiviert sind.

### ClickOnce aktiviert

1. Ein Benutzer öffnet einen Link zu einer Seite, die die ClickOnce-Unterstützung anfordert, und erhält die Aufforderung im nächsten Screenshot.

   ![Aufforderung zum Öffnen einer unsicheren Datei](./media/edge-learn-more-co-di/edge-clickonce-enabled-1.png)

2. Nachdem der Benutzer auf **Öffnen** geklickt hat, versucht ClickOnce, die Anwendung zu starten.

   ![ClickOnce versucht, die Anwendung zu starten](./media/edge-learn-more-co-di/edge-clickonce-enabled-launch-app.png)

3. Nachdem der Benutzer auf **Öffnen**geklickt hat, wird im Browser ein Popup angezeigt, in dem der Benutzer gefragt wird, ob er sicher ist, dass die Anwendung installiert werden soll.

   ![Aufforderung zum Öffnen der Datei](./media/edge-learn-more-co-di/edge-clickonce-enabled-2.png)

   > [!NOTE]
   > Die vom ClickOnce-Dateihandler gezeigte Schnittstelle, Nachrichten und Optionen variieren je nach Typ und Konfiguration der Datei, auf die zugegriffen wird.

### ClickOnce deaktiviert

1. Wenn ein Benutzer einen Link zu einer Seite öffnet, die ClickOnce-Unterstützung anfordert, wird eine Meldung im Download-Tray angezeigt, die jener im nächsten Screenshot ähnelt.

   ![Aufforderung zum Herunterladen der Datei](./media/edge-learn-more-co-di/edge-clickonce-disabled-1.png)

### DirectInvoke deaktiviert

1. Ein Benutzer öffnet einen Link zu einer Seite, die die DirectInvoke-Unterstützung anfordert, und erhält die Aufforderung im nächsten Screenshot.

   ![Aufforderung zum Öffnen der Datei](./media/edge-learn-more-co-di/edge-directinvoke-open-link-1.png)

2. Wenn der Benutzer auf **Öffnen** klickt, wird der angeforderte Dateihandler geöffnet. In diesem Beispiel wird Microsoft Word verwendet, um das im vorherigen Screenshot gezeigte Dokument zu öffnen.

   > [!NOTE]
   > Die vom DirectInvoke-Dateihandler gezeigte Schnittstelle, Nachrichten und Optionen variieren je nach Typ und Konfiguration der Datei, auf die zugegriffen wird.

### DirectInvoke deaktiviert

1. Wenn ein Benutzer einen Link zu einer Seite öffnet, die die DirectInvoke-Unterstützung anfordert, verhält sich DirectInvoke genauso wie ClickOnce deaktiviert. Im Download-Tray wird eine Meldung angezeigt, die jener im nächsten Screenshot ähnelt.

   ![Aufforderung zum Öffnen der Datei](./media/edge-learn-more-co-di/edge-directinvoke-open-link-2.png)

## Weitere Informationen:

- [ClickOnce-Sicherheit und -Bereitstellung](https://go.microsoft.com/fwlink/?linkid=2099880)
- [DirectInvoke im Internet Explorer](https://go.microsoft.com/fwlink/?linkid=2099871)
- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)
