---
title: Der PDF-Reader in Microsoft Edge
ms.author: adigan
author: dan-wesley
manager: balajek
ms.date: 08/05/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Erfahren Sie mehr über den PDF-Reader in Microsoft Edge.
ms.openlocfilehash: c189bc08d4af0c9d5c4d9c573e0b5b7ef32a7fb3
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/31/2020
ms.locfileid: "10980063"
---
# Der PDF-Reader in Microsoft Edge

PDF-Dateien gehören zu unserem Alltag. Wir erhalten sie in Form von Verträgen und Vereinbarungen, Newslettern, Formularen, Forschungsartikeln, Lebensläufen usw. Diese Dateien verdeutlichen die Notwendigkeit eines zuverlässigen, sicheren und leistungsfähigen PDF-Readers, der in Unternehmen eingesetzt werden kann.

Microsoft Edge bietet einen integrierten PDF-Reader, mit dem Sie lokale PDF-Dateien, Online-PDF-Dateien oder in Webseiten eingebettete PDF-Dateien öffnen können. Sie können diesen Dateien mit Freihand Notizen hinzufügen und sie mit Hervorhebungen versehen. Dieser PDF-Reader stellt eine einzige Anwendung zur Abdeckung aller Anforderungen im Hinblick auf Webseiten und PDF-Dokumente dar. Der Microsoft Edge PDF-Reader ist eine sichere und zuverlässige Anwendung, die auf Windows- und macOS-Desktopplattformen funktioniert.

> [!NOTE]
> Dieser Artikel bezieht sich auf Microsoft Edge Version77 oder höher.

## Voraussetzungen, Support und Einschränkungen

Die folgende Tabelle veranschaulicht, welche Kanäle und Versionen von Microsoft Edge die einzelnen PDF-Features unterstützen.

| Feature | Stable-Kanal-Version |
|---------|------------------------|
| Anzeigen und Drucken von lokalen, Online- und eingebetteten PDF-Dateien | 79.0.309.71                |
| Einfaches Ausfüllen von Formularen<br>(JavaScript-Formulare werden nicht unterstützt) | 79.0.309.71           |
| Freihandeingaben  | 80.0.361.48            |
| Freihand-Anpassung | 83.0.478.54  |
| Hervorheben  | 81.0.416.53         |
| Laut vorlesen | Derzeit in [Microsoft Edge Insider](https://www.microsoftedgeinsider.com/)-Kanälen verfügbar |
| Anzeigen von MIP-geschützten Dateien | Windows-Unterstützung in 80.0.361.48<br>Mac-Unterstützung in 81.0.416.53 |
|  Anzeigen von IRM-geschützten Dateien  | 83.0.478.37            |

### Einschränkungen

Beachten Sie die folgenden Einschränkungen für den aktuellen PDF-Reader:

-  XML Forms Architecture (XFA) ist ein veraltetes Formularformat, das in Microsoft Edge nicht unterstützt wird.
-  Dokumentationen zu Barrierefreiheitsszenarien, die aktuell nicht unterstützt werden, finden Sie im [Microsoft-Konformitätsbericht zur Barrierefreiheit](https://cloudblogs.microsoft.com/industry-blog/government/2018/09/11/accessibility-conformance-reports/)-Blog.

## Features

### Freihandeingaben

Freihandeingaben in PDF-Dateien sind praktisch, um sich schnell Notizen zu machen, die auf einfache Weise referenziert werden können, zum Signieren oder um PDF-Formulare auszufüllen. Diese Funktion ist jetzt in Microsoft Edge verfügbar. Neben Freihandeingaben können Sie mithilfe von Farbe und Strichbreite die Aufmerksamkeit auf bestimmte Teile der PDF-Datei lenken. Der nächste Screenshot zeigt, wie ein Benutzer Freihandeingaben auf einer PDF-Seite vornehmen kann.

<!-- SCREENSHOT -->
![Freihandeingaben auf PDF-Seiten](media/microsoft-edge-pdf/pdf-reader-inking.png)

### Hervorheben

Der PDF-Reader in Microsoft Edge ermöglicht das Hinzufügen und Bearbeiten von Hervorhebungen. Zum Erstellen eines Hervorhebung muss der Benutzer lediglich den Text markieren, mit der rechten Maustaste darauf klicken, im Menü „Hervorhebungen“ und die gewünschte Farbe auswählen. Der nächste Screenshot zeigt die verfügbaren Hervorhebungsoptionen.

![Verwenden der Option „Hervorheben“ im PDF-Reader](media/microsoft-edge-pdf/pdf-reader-highlight.png)

### Laut vorlesen

„Laut vorlesen“ für PDF ermöglicht Benutzern das bequeme Anhören von PDF-Inhalten, während sie andere wichtige Aufgaben ausführen. Außerdem hilft es auditiv Lernenden, sich auf den Inhalt zu konzentrieren, wodurch das Lernen erheblich erleichtert wird. Der nächste Screenshot zeigt ein Beispiel für die „Laut vorlesen“-Funktion. Die Hervorhebung zeigt den Text an, der gerade vorgelesen wird.

![Verwenden der Option „Hervorheben“ im PDF-Reader](media/microsoft-edge-pdf/pdf-reader-read-aloud-example.png)

### Geschützte PDF-Dateien

[Microsoft Information Protection (MIP)](https://docs.microsoft.com/microsoft-365/compliance/protect-information?view=o365-worldwide) ermöglicht Benutzern die sichere Zusammenarbeit mit anderen Personen und dabei die Compliance-Richtlinien ihrer Organisation einzuhalten. Nachdem eine Datei geschützt wurde, werden die Aktionen, die von Benutzern daran ausgeführt werden können, durch die ihnen zugewiesenen Zugriffsberechtigungen bestimmt.

Diese Dateien können direkt im Browser geöffnet werden, ohne eine andere Software herunterladen oder ein Add-In installieren zu müssen. Damit wird die von MIP gebotene Sicherheit direkt in den Browser integriert und so ein nahtloser Workflow ermöglicht.

<!-- SCREENSHOT -->
![Geschütztes PDF-Dokument.](media/microsoft-edge-pdf/pdf-reader-protected-pdf2.png)

Neben MIP-geschützten Dateien können auch PDF-Dateien in [IRM (Information Rights Management)](https://docs.microsoft.com/microsoft-365/compliance/set-up-irm-in-sp-admin-center?view=o365-worldwide)-geschützten SharePoint-Bibliotheken direkt im Browser geöffnet werden.

Mit Microsoft Edge können Benutzer MIP-geschützte Dateien anzeigen, die lokal oder in der Cloud gespeichert sind. Lokal gespeicherte Dateien können direkt im Browser geöffnet werden. Für aus einem Clouddienst wie SharePoint geöffnete Dateien muss der Benutzer möglicherweise die Option "Im Browser öffnen" verwenden.

Wenn das Profil, mit dem der Benutzer bei Microsoft Edge angemeldet ist, mindestens über die Berechtigung zum Anzeigen der Datei verfügt, wird die Datei in Microsoft Edge geöffnet.

<!-- SCREENSHOT -->
![Aufforderung zum Speichern einer SharePoint-PDF-Seite, die durch MIP geschützt ist](media/microsoft-edge-pdf/pdf-reader-sharepoint-irm.png)

## Bedienungshilfen

Der PDF-Reader bietet Unterstützung für Barrierefreiheit für Tastaturnavigation, den Modus für hohen Kontrast und die Sprachausgabe für Windows- und macOS-Geräte.

### Barrierefreiheit für Tastaturnavigation

Benutzer können mithilfe der Tastatur zu verschiedenen Teilen des Dokuments navigieren, mit denen ein Benutzer interagieren kann, z. B. Formulare und Hervorhebungen.

<!-- SCREENSHOT -->

### Modus für hohen Kontrast

Der PDF-Reader verwendet die auf Betriebssystemebene festgelegten Einstellungen, um PDF-Inhalte im Modus „Hoher Kontrast“ darzustellen.

<!-- SCREENSHOT -->
<!--![High contrast mode for pdf file](media/microsoft-edge-pdf/pdf-reader-high-contrast.png)-->

### Unterstützung für Sprachausgabe

Benutzer können mithilfe von Bildschirmsprachausgaben auf Windows- und Mac-Computern in PDF-Dateien navigieren und diese lesen. <!--The next screenshot shows the toolbar that users can use for audio settings when they're using the Read Aloud option in PDF reader. -->

<!-- SCREENSHOT -->
<!--
![Screen reader toolbar](media/microsoft-edge-pdf/pdf-reader-read-aloud.png) -->

## Sicherheit und Zuverlässigkeit

Sicherheit gehört zu den wichtigsten Grundsätzen für jede Organisation. Die Sicherheit des PDF-Readers ist integraler Bestandteil des Microsoft Edge-Sicherheitkonzepts. Zwei der wichtigsten Sicherheitsfeatures Im Hinblick auf den PDF-Reader gibt es zwei wichtige Sicherheitsfeatures: Prozessisolation und Microsoft Defender Application Guard (Application Guard).

- Prozessisolation PDF-Dateien, die von unterschiedlichen Websites geöffnet werden, werden auf Prozessebene vollständig isoliert. Der Browser muss nicht mit Websites oder PDF-Dateien kommunizieren, die aus einer anderen Quelle geöffnet wurden. Das Öffnen von PDF-Dateien ist vor Angriffen geschützt, bei denen kompromittierte PDF-Dateien als Angriffsfläche verwendet werden.

- Application Guard. Über Application Guard können Administratoren eine Liste der Websites festlegen, die von ihrer Organisation als vertrauenswürdig eingestuft werden. Wenn Benutzer andere Websites öffnen, werden diese in einem separaten Application Guard-Fenster geöffnet, das in einem eigenen Container ausgeführt wird. Der Container trägt dazu bei, das Unternehmensnetzwerk und alle Daten, die auf dem Computer des Benutzers vorhanden sind, zu schützen.<br><br>
Dieser Schutz gilt auch für alle angezeigten Online-PDF-Dateien. Darüber hinaus werden alle PDF-Dateien, die aus einem Application Guard-Fenster heruntergeladen wurden, im Container gespeichert und bei Bedarf erneut darin geöffnet. Auf diese Weise bleibt Ihre Umgebung nicht nur dann geschützt, wenn die Datei heruntergeladen wird, sondern während ihres gesamten Lebenszyklus. Weitere Informationen finden Sie unter [Application Guard](https://docs.microsoft.com/DeployEdge/microsoft-edge-security-windows-defender-application-guard).

### Zuverlässigkeit

Da Microsoft Edge auf Chromium basiert, können die Benutzer mit dem gleichen Maß an Zuverlässigkeit rechnen, den sie von Google Chrome gewohnt.

## Bereitstellen und Aktualisieren des PDF-Readers

Der PDF-Reader wird mit dem restlichen Microsoft Edge-Browser bereitgestellt und aktualisiert. Wenn Sie mehr über die Bereitstellung von Microsoft Edge wissen möchten, schauen Sie sich das [Bereitstellen von Microsoft Edge für Hunderte oder Tausende von Geräten](microsoft-edge-video-deploy.md) Video an. Weitere Informationen zur Bereitstellung finden Sie auch auf der [Microsoft Edge-Dokumentation](https://docs.microsoft.com/DeployEdge/)-Startseite.

> [!TIP]
> Sie können Microsoft Edge als standardmäßigen PDF-Reader für Ihre Organisation festlegen. Führen Sie dazu [die folgenden Schritte aus](https://docs.microsoft.com/deployedge/edge-default-browser).

## Roadmap und Feedback

Die Roadmap für den PDF-Reader in Microsoft Edge finden Sie [hier](https://techcommunity.microsoft.com/t5/articles/roadmap-for-pdf-reader-in-microsoft-edge/m-p/1467667).

Wir freuen uns auf Ihr Feedback zu den Funktionen, die Ihnen besonders wichtig sind. Senden Sie uns Ihr Feedback über [Microsoft Edge UserVoice](https://microsoftedge.uservoice.com/) und über das [Microsoft Edge Insider](https://techcommunity.microsoft.com/t5/microsoft-edge-insider/ct-p/MicrosoftEdgeInsider)-Forum.

## Weitere Informationen

- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)