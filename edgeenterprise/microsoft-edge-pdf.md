---
title: Der PDF-Reader in Microsoft Edge
ms.author: adigan
author: dan-wesley
manager: balajek
ms.date: 03/01/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Erfahren Sie mehr über den PDF-Reader in Microsoft Edge.
ms.openlocfilehash: d84b838556ed10951d7a7a3c6e5085b7e32c286c
ms.sourcegitcommit: f14286edec59ee9183bdf38c15fc890881efd64f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "11385033"
---
# <a name="pdf-reader-in-microsoft-edge"></a>Der PDF-Reader in Microsoft Edge

PDF-Dateien machen einen großen Teil unseres täglichen Lebens aus. Wir erhalten sie in Form von Verträgen und Vereinbarungen, Newslettern, Formularen, Forschungsartikeln, Lebensläufen usw. Diese Dateien verdeutlichen die Notwendigkeit eines zuverlässigen, sicheren und leistungsfähigen PDF-Readers, der in Unternehmen eingesetzt werden kann.

Microsoft Edge bietet einen integrierten PDF-Reader, mit dem Sie lokale PDF-Dateien, Online-PDF-Dateien oder in Webseiten eingebettete PDF-Dateien öffnen können. Sie können diesen Dateien mit Freihand Notizen hinzufügen und sie mit Hervorhebungen versehen. Dieser PDF-Reader stellt eine einzige Anwendung zur Abdeckung aller Anforderungen im Hinblick auf Webseiten und PDF-Dokumente dar. Der Microsoft Edge PDF-Reader ist eine sichere und zuverlässige Anwendung, die auf Windows- und macOS-Desktopplattformen funktioniert.

> [!NOTE]
> Dieser Artikel bezieht sich auf Microsoft Edge Version77 oder höher.

## <a name="prerequisites-support-and-constraints"></a>Voraussetzungen, Support und Einschränkungen

Die folgende Tabelle veranschaulicht, welche Kanäle und Versionen von Microsoft Edge die einzelnen PDF-Features unterstützen.

| Feature | Stable-Kanal-Version |
|---------|------------------------|
| Anzeigen und Drucken von lokalen, Online- und eingebetteten PDF-Dateien | 79.0.309.71                |
| Einfaches Ausfüllen von Formularen<br>(JavaScript-Formulare werden nicht unterstützt) | 79.0.309.71           |
|Inhaltsverzeichnis| 86.0.622.38 |
| Seitenansicht |Derzeit in [Microsoft Edge Insider](https://www.microsoftedgeinsider.com/)-Kanälen verfügbar |
| Browsen im Caretmodus |87.0.664.41 |
| Freihandeingaben  | 80.0.361.48            |
| Freihand-Anpassung | 83.0.478.54  |
| Hervorheben  | 81.0.416.53         |
| Textnotizen | Derzeit in [Microsoft Edge Insider](https://www.microsoftedgeinsider.com/)-Kanälen verfügbar |
| Laut vorlesen | 84.0.522.63  |
| Anzeigen von durch Microsoft Information Protection (MIP) geschützten Dateien | Windows-Unterstützung in 80.0.361.48<br>Mac-Unterstützung in 81.0.416.53 |
|  Anzeigen von durch Information Rights Management (IRM) geschützten Dateien  | 83.0.478.37            |
| Anzeigen und Überprüfen digitaler Signaturen | Verfügbar in Canary- und Dev-Kanälen. Es wird aktiv daran gearbeitet. |

### <a name="constraints"></a>Einschränkungen

Beachten Sie die folgenden Einschränkungen für den aktuellen PDF-Reader:

-  XML Forms Architecture (XFA) ist ein veraltetes Formularformat, das in Microsoft Edge nicht unterstützt wird.
-  Dokumentationen zu Barrierefreiheitsszenarien, die aktuell nicht unterstützt werden, finden Sie im [Microsoft-Konformitätsbericht zur Barrierefreiheit](https://cloudblogs.microsoft.com/industry-blog/government/2018/09/11/accessibility-conformance-reports/)-Blog.

## <a name="features"></a>Features

Der in Microsoft Edge integrierte PDF-Reader verfügt über die grundlegenden Lese- und Navigationsfunktionen, unter anderem Zoom, Drehen, An Seite/Breite passen, zur Seite springen und suchen. Sie können über eine anheftbare Symbolleiste am oberen Rand des PDF-Inhalts darauf zugreifen. Dieser Abschnitt enthält eine Übersicht über einige wichtige Funktionen. Der nächste Screenshot zeigt die Symbolleiste des PDF-Readers.

![Symbolleiste für den PDF-Reader](media/microsoft-edge-pdf/pdf-reader-toolbar.png)

### <a name="table-of-contents"></a>Inhaltsverzeichnis

Mit Inhaltsverzeichnissen können Benutzer ganz einfach durch PDF-Dokumente navigieren, die ein Inhaltsverzeichnis enthalten. Wenn ein Benutzer auf das Inhaltsverzeichnissymbol klickt, wird ein Navigationsbereich mit einer Liste der mit Bezeichnungen versehenen Abschnitte und Unterabschnitte im PDF-Dokument angezeigt. Der Benutzer kann dann auf eine der Bezeichnungen im Bereich klicken, um zu diesem Abschnitt des Dokuments zu navigieren. Der Bereich bleibt so lange wie nötig geöffnet und kann geschlossen werden, wenn der Benutzer zum Lesen des Dokuments zurück möchte. Der nächste Screenshot zeigt den Navigationsbereich für ein geöffnetes Dokument.

![Navigation im PDF-Reader mit Inhaltsverzeichnis](media/microsoft-edge-pdf/pdf-reader-toc.png)

### <a name="page-view"></a>Seitenansicht

Microsoft Edge unterstützt unterschiedliche Ansichten für PDF-Dokumente in unseren Dev- und Canary-Kanälen. Benutzer können das Layout eines Dokuments von einer Einzelseitenansicht in zwei Seiten ändern, die nebeneinander angezeigt werden. Um zu ändern, wie das PDF-Dokument angezeigt wird, können Benutzer auf der PDF-Symbolleiste auf die Schaltfläche „Seitenansicht“ klicken und dann eine der Ansichten auswählen, die sie verwenden möchten. Die Zwei-Seiten-Ansicht wird im nächsten Screenshot angezeigt.

![PDF-Reader, der die Zwei-Seiten-Ansicht eines Dokuments benutzt.](media/microsoft-edge-pdf/pdf-reader-page-view.png)

### <a name="caret-mode-browsing"></a>Browsen im Caretmodus

Das Caretbrowsen ist für in Microsoft Edge geöffnete PDF-Dateien verfügbar, was bedeutet, dass Benutzer über die Tastatur mit PDF-Dateien interagieren können. Wenn ein Benutzer die F7-TASTE an einer beliebigen Stelle im Browser drückt, wird er gefragt, ob das Caretbrowsen aktiviert werden soll. Wenn diese Option aktiviert ist, ist das Caretbrowsen für alle Inhalte verfügbar, die im Browser geöffnet werden, sei es PDF-Dateien oder Webseiten. Wenn ein Benutzer erneut F7 drückt, wird das Caretbrowsen deaktiviert. Wenn das Caretbrowsen aktiv ist und der Fokus auf dem Inhalt liegt, sehen Benutzer einen blinkenden Cursor in der PDF-Datei. Das Caretformat kann auch verwendet werden, um durch die Datei zu navigieren oder Text durch Drücken der UMSCHALTTASTE beim Bewegen des Cursors auszuwählen. Mit dieser Funktion können Benutzer Elemente ganz einfach als Hervorhebungen erstellen oder mit Elementen wie Links, Formularfeldern mit der Tastatur interagieren. Der nächste Screenshot zeigt das Popupmenü zum Aktivieren des Browsens im Caretmodus.

![Menü „PDF-Reader“ für das Browsen im Caretmodus.](media/microsoft-edge-pdf/pdf-reader-caret-mode.png)

### <a name="inking"></a>Freihandeingaben

Freihandeingaben in PDF-Dateien sind praktisch, um sich schnell Notizen zu machen, die auf einfache Weise referenziert werden können, zum Signieren oder um PDF-Formulare auszufüllen. Diese Funktion ist jetzt in Microsoft Edge verfügbar. Neben Freihandeingaben können Sie mithilfe von Farbe und Strichbreite die Aufmerksamkeit auf bestimmte Teile der PDF-Datei lenken. Der nächste Screenshot zeigt, wie ein Benutzer Freihandeingaben auf einer PDF-Seite vornehmen kann.

![Freihandeingaben auf PDF-Seiten](media/microsoft-edge-pdf/pdf-reader-inking.png)

### <a name="highlight"></a>Hervorheben

Der PDF-Reader in Microsoft Edge ermöglicht das Hinzufügen und Bearbeiten von Hervorhebungen. Zum Erstellen eines Hervorhebung muss der Benutzer lediglich den Text markieren, mit der rechten Maustaste darauf klicken, im Menü „Hervorhebungen“ und die gewünschte Farbe auswählen. Highlights können auch mit einem Stift oder einer Tastatur erstellt werden. Der nächste Screenshot zeigt die verfügbaren Hervorhebungsoptionen.

![Verwenden der Option „Hervorheben“ im PDF-Reader](media/microsoft-edge-pdf/pdf-reader-highlight.png)

### <a name="text-notes"></a>Textnotizen

Beim Lesen einer PDF-Datei können Textnotizen zu Text in der Datei hinzugefügt werden, um später einfach nachlesen zu können.

Benutzer können eine Notiz hinzufügen, indem sie den Text markieren, für den sie eine Notiz hinzufügen möchten, und das Kontextmenü mit der rechten Maustaste aufrufen. Wenn Sie im Menü die Option **Kommentar hinzufügen** auswählen, wird ein Textfeld geöffnet, in dem Benutzer ihre Kommentare hinzufügen können. Sie können den Kommentar eingeben und dann auf das Kontrollkästchen klicken, um den Kommentar zu speichern.

Nachdem eine Notiz hinzugefügt wurde, wird der ausgewählte Text hervorgehoben, und es wird ein Kommentarsymbol angezeigt, das den Kommentar angibt. Benutzer können mit der Maus auf dieses Symbol zeigen, um eine Vorschau des Kommentars anzuzeigen, oder darauf klicken, um die Notiz zu öffnen und zu bearbeiten.

Der nächste Screenshot zeigt eine Notiz, die dem hervorgehobenen Text hinzugefügt wird.

![Der PDF-Reader fügt dem Dokument eine Textnotiz hinzu.](media/microsoft-edge-pdf/pdf-reader-text-note.png)

### <a name="read-aloud"></a>Laut vorlesen

Das laute Vorlesen für PDF erhöht den Komfort, dass Benutzer dem Inhalt der PDF zuhören und gleichzeitig andere Aufgaben ausführen können, die ihnen möglicherweise von Bedeutung sind. Außerdem hilft es auditiv Lernenden, sich auf den Inhalt zu konzentrieren, wodurch das Lernen erheblich erleichtert wird. Der nächste Screenshot zeigt ein Beispiel für „Laut vorlesen“. Die Hervorhebung zeigt den Text an, der gerade vorgelesen wird.

![Verwenden der Hervorhebungsoption für „Laut vorlesen“ im PDF-Reader](media/microsoft-edge-pdf/pdf-reader-read-aloud-example.png)

### <a name="protected-pdfs"></a>Geschützte PDF-Dateien

[Microsoft Information Protection (MIP)](https://docs.microsoft.com/microsoft-365/compliance/protect-information?view=o365-worldwide&preserve-view=true) ermöglicht Benutzern die sichere Zusammenarbeit mit anderen Personen und dabei die Compliance-Richtlinien ihrer Organisation einzuhalten. Nachdem eine Datei geschützt wurde, werden die Aktionen, die von Benutzern daran ausgeführt werden können, durch die ihnen zugewiesenen Zugriffsberechtigungen bestimmt.

> [!IMPORTANT]
> Für MIP ist eine Lizenz erforderlich. Weitere Informationen finden Sie in dieser [Microsoft 365-Lizenzierungsanleitung.](https://docs.microsoft.com/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance/microsoft-365-security-compliance-licensing-guidance#information-protection)

Diese Dateien können direkt im Browser geöffnet werden, ohne eine andere Software herunterladen oder ein Add-In installieren zu müssen. Diese Funktion integriert die von MIP bereitgestellte Sicherheit direkt in den Browser, um einen nahtlosen Workflow zu bieten.

![Geschütztes PDF-Dokument.](media/microsoft-edge-pdf/pdf-reader-protected-pdf2.png)

Neben MIP-geschützten Dateien können auch PDF-Dateien in [IRM (Information Rights Management)](https://docs.microsoft.com/microsoft-365/compliance/set-up-irm-in-sp-admin-center?view=o365-worldwide&preserve-view=true)-geschützten SharePoint-Bibliotheken direkt im Browser geöffnet werden.

Mit Microsoft Edge können Benutzer MIP-geschützte Dateien anzeigen, die lokal oder in der Cloud gespeichert sind. Lokal gespeicherte Dateien können direkt im Browser geöffnet werden. Für aus einem Clouddienst wie SharePoint geöffnete Dateien muss der Benutzer möglicherweise die Option "Im Browser öffnen" verwenden.

Wenn das Profil, mit dem der Benutzer bei Microsoft Edge angemeldet ist, mindestens über die Berechtigung zum Anzeigen der Datei verfügt, wird die Datei in Microsoft Edge geöffnet.

![Aufforderung zum Speichern einer SharePoint-PDF-Seite, die durch MIP geschützt ist](media/microsoft-edge-pdf/pdf-reader-sharepoint-irm.png)

### <a name="view-and-validate-certificate-based-digital-signatures"></a>Anzeigen und Überprüfen zertifikatbasierter digitaler Signaturen

In dieser digitalen Welt ist es wichtig, die Authentizität und den Besitz des Inhalts im Dokument nachzuweisen. Zertifikatbasierte digitale Signaturen werden häufig in PDF-Dokumenten verwendet, um sicherzustellen, dass der Inhalt des Dokuments mit dem vom Autor beabsichtigten identisch ist und nicht geändert wurde. Mit Microsoft Edge können Sie digitale Zertifikatsignaturen in PDFs anzeigen und überprüfen.

Wir arbeiten aktiv an der Verbesserung des Supports, um mehr Situationen zu adressieren, und freuen uns auf Feedback dazu.

## <a name="accessibility"></a>Barrierefreiheit

Der PDF-Reader bietet Unterstützung für Barrierefreiheit für Tastaturnavigation, den Modus für hohen Kontrast und die Sprachausgabe für Windows- und macOS-Geräte.

### <a name="keyboard-accessibility"></a>Barrierefreiheit für Tastaturnavigation

Benutzer können mithilfe der Tastatur zu verschiedenen Teilen des Dokuments navigieren, mit denen ein Benutzer interagieren kann, z. B. Formulare und Hervorhebungen. Benutzer können den Caretmodus auch verwenden, um mithilfe der Tastatur in den PDF-Dateien zu navigieren und mit diesen zu interagieren.

### <a name="high-contrast-mode"></a>Modus für hohen Kontrast

Der PDF-Reader verwendet die auf Betriebssystemebene festgelegten Einstellungen, um PDF-Inhalte im Modus „Hoher Kontrast“ darzustellen.

### <a name="screen-reader-support"></a>Unterstützung für Sprachausgabe

Benutzer können mithilfe von Bildschirmsprachausgaben auf Windows- und Mac-Computern in PDF-Dateien navigieren und diese lesen.

## <a name="security-and-reliability"></a>Sicherheit und Zuverlässigkeit

Sicherheit gehört zu den wichtigsten Grundsätzen für jede Organisation. Die Sicherheit des PDF-Readers ist integraler Bestandteil des Microsoft Edge-Sicherheitkonzepts. Zwei der wichtigsten Sicherheitsfeatures Im Hinblick auf den PDF-Reader gibt es zwei wichtige Sicherheitsfeatures: Prozessisolation und Microsoft Defender Application Guard (Application Guard).

- Prozessisolation PDF-Dateien, die von unterschiedlichen Websites geöffnet werden, werden auf Prozessebene vollständig isoliert. Der Browser muss nicht mit Websites oder PDF-Dateien kommunizieren, die aus einer anderen Quelle geöffnet wurden. Das Öffnen von PDF-Dateien ist vor Angriffen geschützt, bei denen kompromittierte PDF-Dateien als Angriffsfläche verwendet werden.

- Application Guard. Über Application Guard können Administratoren eine Liste der Websites festlegen, die von ihrer Organisation als vertrauenswürdig eingestuft werden. Wenn Benutzer andere Websites öffnen, werden diese in einem separaten Application Guard-Fenster geöffnet, das in einem eigenen Container ausgeführt wird. Der Container trägt dazu bei, das Unternehmensnetzwerk und alle Daten, die auf dem Computer des Benutzers vorhanden sind, zu schützen.<br><br>
Dieser Schutz gilt auch für alle angezeigten Online-PDF-Dateien. Darüber hinaus werden alle PDF-Dateien, die aus einem Application Guard-Fenster heruntergeladen wurden, im Container gespeichert und bei Bedarf erneut darin geöffnet. Auf diese Weise bleibt Ihre Umgebung nicht nur dann geschützt, wenn die Datei heruntergeladen wird, sondern während ihres gesamten Lebenszyklus. Weitere Informationen finden Sie unter [Application Guard](https://docs.microsoft.com/DeployEdge/microsoft-edge-security-windows-defender-application-guard).

### <a name="reliability"></a>Zuverlässigkeit

Da Microsoft Edge Chromium-basiert ist, können Benutzer den gleichen Zuverlässigkeitsgrad erwarten, den sie in anderen Chromium-basierten Browsern gewohnt sind.

## <a name="deploy-and-update-pdf-reader"></a>Bereitstellen und Aktualisieren des PDF-Readers

Der PDF-Reader wird mit dem restlichen Microsoft Edge-Browser bereitgestellt und aktualisiert. Wenn Sie mehr über die Bereitstellung von Microsoft Edge wissen möchten, schauen Sie sich das [Bereitstellen von Microsoft Edge für Hunderte oder Tausende von Geräten](microsoft-edge-video-deploy.md) Video an. Weitere Informationen zur Bereitstellung finden Sie auch auf der [Microsoft Edge-Dokumentation](https://docs.microsoft.com/DeployEdge/)-Startseite.

> [!TIP]
> Sie können Microsoft Edge als standardmäßigen PDF-Reader für Ihre Organisation festlegen. Führen Sie dazu [die folgenden Schritte aus](https://docs.microsoft.com/deployedge/edge-default-browser).

## <a name="roadmap-and-feedback"></a>Roadmap und Feedback

Die Roadmap für den PDF-Reader in Microsoft Edge ist [hier](https://techcommunity.microsoft.com/t5/articles/roadmap-for-pdf-reader-in-microsoft-edge/m-p/1467667) verfügbar.

Wir suchen aktive nach Ihrem Feedback zu den Funktionen, die Sie wichtig finden. Senden Sie uns Feedback über das [Microsoft Edge-Insider](https://techcommunity.microsoft.com/t5/microsoft-edge-insider/ct-p/MicrosoftEdgeInsider)-Forum.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft Edge Enterprise Landing Page](https://aka.ms/EdgeEnterprise)
- [Microsoft 365-Roadmap](https://www.microsoft.com/microsoft-365/roadmap)
- [Video: Microsoft Edge PDF-Reader für Unternehmen](microsoft-edge-video-pdf-reader.md)