---
title: Microsoft Edge und Downloads gemischter Inhalte
ms.author: collw
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Microsoft Edge und Downloads gemischter Inhalte
ms.openlocfilehash: 4871b23145d365e814c5cf1cac7699044f3da35e
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "11642141"
---
# <a name="learn-about-microsoft-edge-and-mixed-content-downloads"></a>Informationen zu Microsoft Edge und Downloads gemischter Inhalte

In diesem Artikel werden Downloads gemischter Inhalte erläutert und wie Microsoft Edge mit diesen umgeht.

>[!NOTE]
>Dieser Artikel bezieht sich auf Microsoft Edge Version 85 oder neuer.

## <a name="what-are-mixed-content-downloads"></a>Was sind Downloads gemischter Inhalte?

Zu einem Download gemischter Inhalte kommt es, wenn Sie einen Download von einer HTML-Seite starten, die über eine sichere HTTPS-Verbindung geladen wurde, wobei aber eine der folgenden Bedingungen besteht:

- Mindestens eine der Umleitungen des Downloadspeicherorts wurde über eine unsichere HTTP-Verbindung geladen.
- Der endgültige Downloadspeicherort wurde über eine unsichere HTTP-Verbindung geladen.

Bei beiden Szenario handelt es sich um gemischten Inhalt, da die Anforderung mit sicherem HTTPS gestellt wurde und sowohl HTTP- als auch HTTPS-Inhalt beim Erreichen des endgültigen Downloadziels beteiligt sind. In modernen Browsern werden Warnungen zu diesem Typ von Inhalt angezeigt, um den Benutzer darauf hinzuweisen, dass dieser Download möglicherweise ungesichert übertragen wird, auch wenn die Seite des ursprünglichen Zugriffs sicher war.

## <a name="download-warnings-and-user-options"></a>Downloadwarnungen und Benutzeroptionen

Die Downloadwarnung stellt sicher, dass Benutzer wissen, dass die Datei, die sie gerade herunterladen, von bösartigen Angreifern in Ihrem Netzwerk gelesen werden könnte. Durch diese Warnung kann sich ein Benutzer fundiert entscheiden, ob die Datei heruntergeladen werden soll.

In Microsoft Edge werden Downloads gemischter Inhalte blockiert, aber Benutzer können dies bei Bedarf außer Kraft setzen und die Datei herunterladen. Microsoft Edge plant, das Blockieren von Downloads gemischter Inhalte mit ausführbaren Dateien ab Microsoft Edge, Version85, einzuführen, und unterschiedliche Dateitypen werden in zukünftigen Releases ebenfalls blockiert.

> [!NOTE]
> Die Bereitstellung dieser Funktion kann sich in Abhängigkeit vom Veröffentlichungszeitplan und dem Benutzerfeedback ändern.

<!-- The schedule of the block for different filetypes is to be determined and may be impacted by usage data and user feedback. -->

Im Downloadbereich sieht die Blockier-Warnmeldung wie im nächsten Screenshot aus.

 ![Warnung wegen gemischter Inhalte im Downloadbereich](./media/edge-learnmore-mixed-content-downloads/edge-mixed-content-download-tray-warning.png)

Auf der Downloadseite sieht die Blockier-Warnung wie das folgende Screenshotbeispiel aus:

 ![Aufforderung zum Außerkraftsetzen gemischter Inhalte](./media/edge-learnmore-mixed-content-downloads/edge-mixed-content-download-page-warning.png)

Wenn sich ein Benutzer entschließt, den Download zu behalten, wird er zum Bestätigen seiner Aktion aufgefordert. Der nächste Screenshot zeigt ein Beispiel für diese Bestätigungsaufforderung.

 ![Internet Explorer-Modus](./media/edge-learnmore-mixed-content-downloads/edge-mixed-content-download-override.png)

## <a name="supporting-policies"></a>Unterstützende Richtlinien

Unternehmen, die das Blockieren gemischter Inhalte von bestimmten Websites ausschließen möchten, können hierfür die Richtlinie [InsecureContentAllowedForUrls](./microsoft-edge-policies.md#insecurecontentallowedforurls) verwenden.

## <a name="content-license"></a>Lizenz für Inhalte

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf von Chromium.org erstellten und freigegebenen Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/) beschriebenen Begriffen verwendet werden. Die Originalseite von Chromium finden Sie [hier](https://developers.google.com/web/fundamentals/security/prevent-mixed-content/what-is-mixed-content).
  
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />Diese Arbeit unterliegt einer <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)