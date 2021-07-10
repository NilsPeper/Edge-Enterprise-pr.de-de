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
# <a name="learn-about-microsoft-edge-and-mixed-content-downloads"></a><span data-ttu-id="5dd06-103">Informationen zu Microsoft Edge und Downloads gemischter Inhalte</span><span class="sxs-lookup"><span data-stu-id="5dd06-103">Learn about Microsoft Edge and mixed content downloads</span></span>

<span data-ttu-id="5dd06-104">In diesem Artikel werden Downloads gemischter Inhalte erläutert und wie Microsoft Edge mit diesen umgeht.</span><span class="sxs-lookup"><span data-stu-id="5dd06-104">This article explains mixed content downloads and how Microsoft Edge handles them.</span></span>

>[!NOTE]
><span data-ttu-id="5dd06-105">Dieser Artikel bezieht sich auf Microsoft Edge Version 85 oder neuer.</span><span class="sxs-lookup"><span data-stu-id="5dd06-105">This article applies to Microsoft Edge version 85 or later.</span></span>

## <a name="what-are-mixed-content-downloads"></a><span data-ttu-id="5dd06-106">Was sind Downloads gemischter Inhalte?</span><span class="sxs-lookup"><span data-stu-id="5dd06-106">What are mixed content downloads?</span></span>

<span data-ttu-id="5dd06-107">Zu einem Download gemischter Inhalte kommt es, wenn Sie einen Download von einer HTML-Seite starten, die über eine sichere HTTPS-Verbindung geladen wurde, wobei aber eine der folgenden Bedingungen besteht:</span><span class="sxs-lookup"><span data-stu-id="5dd06-107">A mixed content download happens when you start a download from an HTML page that was loaded over a secure HTTPS connection, but one of the following conditions exists:</span></span>

- <span data-ttu-id="5dd06-108">Mindestens eine der Umleitungen des Downloadspeicherorts wurde über eine unsichere HTTP-Verbindung geladen.</span><span class="sxs-lookup"><span data-stu-id="5dd06-108">One or more of the download location's redirects was loaded over an insecure HTTP connection.</span></span>
- <span data-ttu-id="5dd06-109">Der endgültige Downloadspeicherort wurde über eine unsichere HTTP-Verbindung geladen.</span><span class="sxs-lookup"><span data-stu-id="5dd06-109">The final download location was loaded over an insecure HTTP connection.</span></span>

<span data-ttu-id="5dd06-110">Bei beiden Szenario handelt es sich um gemischten Inhalt, da die Anforderung mit sicherem HTTPS gestellt wurde und sowohl HTTP- als auch HTTPS-Inhalt beim Erreichen des endgültigen Downloadziels beteiligt sind.</span><span class="sxs-lookup"><span data-stu-id="5dd06-110">Either scenario is a mixed content because the request was made using secure HTTPS and both HTTP and HTTPS content are involved in reaching the final download destination.</span></span> <span data-ttu-id="5dd06-111">In modernen Browsern werden Warnungen zu diesem Typ von Inhalt angezeigt, um den Benutzer darauf hinzuweisen, dass dieser Download möglicherweise ungesichert übertragen wird, auch wenn die Seite des ursprünglichen Zugriffs sicher war.</span><span class="sxs-lookup"><span data-stu-id="5dd06-111">Modern browsers display warnings about this type of content to indicate to the user that this download may be transferred insecurely even though the original page accessed was secure.</span></span>

## <a name="download-warnings-and-user-options"></a><span data-ttu-id="5dd06-112">Downloadwarnungen und Benutzeroptionen</span><span class="sxs-lookup"><span data-stu-id="5dd06-112">Download warnings and user options</span></span>

<span data-ttu-id="5dd06-113">Die Downloadwarnung stellt sicher, dass Benutzer wissen, dass die Datei, die sie gerade herunterladen, von bösartigen Angreifern in Ihrem Netzwerk gelesen werden könnte.</span><span class="sxs-lookup"><span data-stu-id="5dd06-113">The download warning ensures that users know that the file they're downloading could be read by malicious attackers on their network.</span></span> <span data-ttu-id="5dd06-114">Durch diese Warnung kann sich ein Benutzer fundiert entscheiden, ob die Datei heruntergeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="5dd06-114">This warning lets a user make an informed decision on whether to download the file.</span></span>

<span data-ttu-id="5dd06-115">In Microsoft Edge werden Downloads gemischter Inhalte blockiert, aber Benutzer können dies bei Bedarf außer Kraft setzen und die Datei herunterladen.</span><span class="sxs-lookup"><span data-stu-id="5dd06-115">In Microsoft Edge, mixed content downloads will be blocked but users can override and download the file if they want to.</span></span> <span data-ttu-id="5dd06-116">Microsoft Edge plant, das Blockieren von Downloads gemischter Inhalte mit ausführbaren Dateien ab Microsoft Edge, Version85, einzuführen, und unterschiedliche Dateitypen werden in zukünftigen Releases ebenfalls blockiert.</span><span class="sxs-lookup"><span data-stu-id="5dd06-116">Microsoft Edge plans on starting to block mixed content executable file downloads starting with Microsoft Edge version 85 and will block different filetypes in future releases.</span></span>

> [!NOTE]
> <span data-ttu-id="5dd06-117">Die Bereitstellung dieser Funktion kann sich in Abhängigkeit vom Veröffentlichungszeitplan und dem Benutzerfeedback ändern.</span><span class="sxs-lookup"><span data-stu-id="5dd06-117">Deployment of this feature is subject to change based on release schedule and user feedback.</span></span>

<!-- The schedule of the block for different filetypes is to be determined and may be impacted by usage data and user feedback. -->

<span data-ttu-id="5dd06-118">Im Downloadbereich sieht die Blockier-Warnmeldung wie im nächsten Screenshot aus.</span><span class="sxs-lookup"><span data-stu-id="5dd06-118">In the download shelf, the block warning message looks like the example in the next screenshot.</span></span>

 ![Warnung wegen gemischter Inhalte im Downloadbereich](./media/edge-learnmore-mixed-content-downloads/edge-mixed-content-download-tray-warning.png)

<span data-ttu-id="5dd06-120">Auf der Downloadseite sieht die Blockier-Warnung wie das folgende Screenshotbeispiel aus:</span><span class="sxs-lookup"><span data-stu-id="5dd06-120">On the download page, the block warning looks like the following screenshot example:</span></span>

 ![Aufforderung zum Außerkraftsetzen gemischter Inhalte](./media/edge-learnmore-mixed-content-downloads/edge-mixed-content-download-page-warning.png)

<span data-ttu-id="5dd06-122">Wenn sich ein Benutzer entschließt, den Download zu behalten, wird er zum Bestätigen seiner Aktion aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="5dd06-122">If a user decides to keep the download, they are prompted to confirm their action.</span></span> <span data-ttu-id="5dd06-123">Der nächste Screenshot zeigt ein Beispiel für diese Bestätigungsaufforderung.</span><span class="sxs-lookup"><span data-stu-id="5dd06-123">The next screenshot shows an example of this confirmation prompt.</span></span>

 ![Internet Explorer-Modus](./media/edge-learnmore-mixed-content-downloads/edge-mixed-content-download-override.png)

## <a name="supporting-policies"></a><span data-ttu-id="5dd06-125">Unterstützende Richtlinien</span><span class="sxs-lookup"><span data-stu-id="5dd06-125">Supporting policies</span></span>

<span data-ttu-id="5dd06-126">Unternehmen, die das Blockieren gemischter Inhalte von bestimmten Websites ausschließen möchten, können hierfür die Richtlinie [InsecureContentAllowedForUrls](./microsoft-edge-policies.md#insecurecontentallowedforurls) verwenden.</span><span class="sxs-lookup"><span data-stu-id="5dd06-126">Enterprises that want to exclude mixed content blocking from specific websites can use the [InsecureContentAllowedForUrls](./microsoft-edge-policies.md#insecurecontentallowedforurls) policy to do so.</span></span>

## <a name="content-license"></a><span data-ttu-id="5dd06-127">Lizenz für Inhalte</span><span class="sxs-lookup"><span data-stu-id="5dd06-127">Content license</span></span>

> [!NOTE]
> <span data-ttu-id="5dd06-128">Teile dieser Seite sind Änderungen, die auf von Chromium.org erstellten und freigegebenen Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/) beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5dd06-128">Portions of this page are modifications based on work created and shared by Chromium.org and used according to terms described in the [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/).</span></span> <span data-ttu-id="5dd06-129">Die Originalseite von Chromium finden Sie [hier](https://developers.google.com/web/fundamentals/security/prevent-mixed-content/what-is-mixed-content).</span><span class="sxs-lookup"><span data-stu-id="5dd06-129">The original page can be found [here](https://developers.google.com/web/fundamentals/security/prevent-mixed-content/what-is-mixed-content).</span></span>
  
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br /><span data-ttu-id="5dd06-130">Diese Arbeit unterliegt einer <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.</span><span class="sxs-lookup"><span data-stu-id="5dd06-130">This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.</span></span>

## <a name="see-also"></a><span data-ttu-id="5dd06-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5dd06-131">See also</span></span>

- [<span data-ttu-id="5dd06-132">Microsoft Edge Enterprise-Angebotsseite</span><span class="sxs-lookup"><span data-stu-id="5dd06-132">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)