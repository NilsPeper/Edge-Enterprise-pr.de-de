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
ms.openlocfilehash: 1103c4f5c071b0d04c347a7c7c9fbc5556c4c0fb
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/24/2021
ms.locfileid: "11447669"
---
# <a name="understand-the-clickonce-and-directinvoke-features-in-microsoft-edge"></a><span data-ttu-id="9e990-103">Grundlegendes zu den ClickOnce- und DirectInvoke-Features in Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="9e990-103">Understand the ClickOnce and DirectInvoke features in Microsoft Edge</span></span>

<span data-ttu-id="9e990-104">ClickOnce und DirectInvoke sind Features, die in IE und Microsoft Edge (Version 45 und früher) verfügbar sind und die Verwendung eines Dateihandlers zum Herunterladen von Dateien von einer Website unterstützen.</span><span class="sxs-lookup"><span data-stu-id="9e990-104">ClickOnce and DirectInvoke are features available in IE and Microsoft Edge (version 45 and earlier) that support the use of a file handler to download files from a website.</span></span> <span data-ttu-id="9e990-105">Obwohl sie unterschiedlichen Zwecken dienen, können Websites mit beiden Features angeben, dass eine zum Herunterladen angeforderte Datei an einen Dateihandler auf dem Gerät des Benutzers weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="9e990-105">Although they serve different purposes, both features let websites specify that a file requested for download is passed to a file handler on the user's device.</span></span> <span data-ttu-id="9e990-106">ClickOnce-Anforderungen werden vom systemeigenen Dateihandler in Windows verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="9e990-106">ClickOnce requests are handled by the native file handler in Windows.</span></span> <span data-ttu-id="9e990-107">DirectInvoke-Anforderungen werden von einem registrierten Dateihandler verarbeitet, der von der Website angegeben wird, die die Datei hostet.</span><span class="sxs-lookup"><span data-stu-id="9e990-107">DirectInvoke requests are handled by a registered file handler specified by the website hosting the file.</span></span>

<span data-ttu-id="9e990-108">Weitere Informationen zu Features und Beschränkungen finden Sie in den häufig gestellten Fragen.</span><span class="sxs-lookup"><span data-stu-id="9e990-108">For more information about these features, see:</span></span>

- [<span data-ttu-id="9e990-109">ClickOnce</span><span class="sxs-lookup"><span data-stu-id="9e990-109">ClickOnce</span></span>](/visualstudio/deployment/clickonce-security-and-deployment?view=vs-2019)
- [<span data-ttu-id="9e990-110">DirectInvoke</span><span class="sxs-lookup"><span data-stu-id="9e990-110">DirectInvoke</span></span>]( https://technet.microsoft.com/learning/jj215788(v=vs.94).aspx)

> [!NOTE]
> <span data-ttu-id="9e990-111">Derzeit bietet Chromium keine systemeigene Unterstützung für ClickOnce oder DirectInvoke.</span><span class="sxs-lookup"><span data-stu-id="9e990-111">Currently, Chromium doesn't provide native support for ClickOnce or DirectInvoke.</span></span>

## <a name="overview-prerequisites-and-process"></a><span data-ttu-id="9e990-112">Übersicht: Voraussetzungen und Prozess</span><span class="sxs-lookup"><span data-stu-id="9e990-112">Overview: prerequisites and process</span></span>

<span data-ttu-id="9e990-113">Damit ClickOnce und DirectInvoke wie vorgesehen funktionieren und der Dateihandler erfolgreich angefordert werden kann, muss der Dateihandler im Betriebssystem als unterstützend für ClickOnce oder DirectInvoke registriert sein.</span><span class="sxs-lookup"><span data-stu-id="9e990-113">For ClickOnce and DirectInvoke to work as designed and for the file handler to be successfully requested, the file handler must be registered to the operating system as supporting ClickOnce or DirectInvoke.</span></span> <span data-ttu-id="9e990-114">Diese Registrierung erfolgt in der Regel, wenn das ursprüngliche Betriebssystem installiert wird oder ein neu installiertes Programm die Verwendung von DirectInvoke für Updates anfordert.</span><span class="sxs-lookup"><span data-stu-id="9e990-114">This registration typically happens when the original operating system is installed or when a new program that's installed requests the ability to use DirectInvoke for updates.</span></span>

<span data-ttu-id="9e990-115">Wenn eine Website eine Downloadanforderung erhält, für die ClickOnce oder DirectInvoke erforderlich ist, werden die folgenden Aktionen ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="9e990-115">When a website receives a download request that requires ClickOnce or DirectInvoke, the following actions happen:</span></span>

- <span data-ttu-id="9e990-116">Die Website fordert den Browser auf, einen bestimmten Dateihandler zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="9e990-116">The website requests that the browser use a specified file handler.</span></span>
- <span data-ttu-id="9e990-117">Der Browser überprüft die Betriebssystemregistrierung, um festzustellen, ob der Dateihandler für den angeforderten Dateityp registriert ist.</span><span class="sxs-lookup"><span data-stu-id="9e990-117">The browser checks the operating system registry to see if the file handler is registered for the requested file type.</span></span>
- <span data-ttu-id="9e990-118">Wenn der Dateihandler registriert ist, ruft der Browser den Dateihandler auf und übergibt die URL als Argument an den Dateihandler.</span><span class="sxs-lookup"><span data-stu-id="9e990-118">If the file handler is registered, the browser calls the file handler and passes the URL as an argument to the file handler.</span></span>
- <span data-ttu-id="9e990-119">Der Dateihandler verarbeitet die URL und lädt die Datei herunter.</span><span class="sxs-lookup"><span data-stu-id="9e990-119">The file handler processes the URL and downloads the file.</span></span>

  > [!NOTE]
  > <span data-ttu-id="9e990-120">Die URL wird verwendet, um die Quelle der Datei sowie alle Parameter zu bestimmen, die beim Zugriff auf die Datei verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9e990-120">The URL is used to determine the source of the file, as well as any parameters to use when accessing the file.</span></span>  <span data-ttu-id="9e990-121">Zum Beispiel: Endpunkte, ein Manifest oder Metadaten.</span><span class="sxs-lookup"><span data-stu-id="9e990-121">For example: endpoints, a manifest, or metadata.</span></span>

## <a name="use-cases"></a><span data-ttu-id="9e990-122">Anwendungsfälle</span><span class="sxs-lookup"><span data-stu-id="9e990-122">Use cases</span></span>

<span data-ttu-id="9e990-123">Die folgenden Anwendungsfälle sind repräsentativ.</span><span class="sxs-lookup"><span data-stu-id="9e990-123">The following use cases are representative.</span></span>

<span data-ttu-id="9e990-124">Sie können ClickOnce verwenden, um Software auf Geräten mit minimaler Benutzerinteraktion einfach bereitzustellen und zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="9e990-124">You can use ClickOnce to easily deploy and update software on devices with minimal user interaction.</span></span> <span data-ttu-id="9e990-125">Benutzer können eine Windows-Anwendung installieren und ausführen, indem sie auf einen Link auf einer Website klicken.</span><span class="sxs-lookup"><span data-stu-id="9e990-125">Users can install and run a Windows application by clicking a link in a web page.</span></span> <span data-ttu-id="9e990-126">Bei ordnungsgemäßer Konfiguration kann die ClickOnce-Anwendung Programme installieren, ohne dass Benutzer Konfigurationen für das Installationsprogramm festlegen müssen.</span><span class="sxs-lookup"><span data-stu-id="9e990-126">If configured correctly, the ClickOnce application can install programs without having users set configurations for the installer.</span></span> <span data-ttu-id="9e990-127">Zum Beispiel Dateispeicherorte, zu installierende Optionen usw.</span><span class="sxs-lookup"><span data-stu-id="9e990-127">For example, file locations, what options to install, and so on.</span></span>

<span data-ttu-id="9e990-128">DirectInvoke-Anwendungsfälle hängen von der Absicht der Website ab, die DirectInvoke anfordert.</span><span class="sxs-lookup"><span data-stu-id="9e990-128">DirectInvoke use cases depend on the intent of the website requesting DirectInvoke.</span></span> <span data-ttu-id="9e990-129">Zum Beispiel die kollaborative Dateibearbeitungsfunktion von Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="9e990-129">For example, the collaborative file-editing feature of Microsoft Word.</span></span> <span data-ttu-id="9e990-130">Anstatt auf einen Link zu klicken und die gesamte Kopie eines Dokuments herunterzuladen, an dem Sie mit Ihren Kollegen arbeiten, können Sie mit DirectInvoke die Teile des Dokuments herunterladen, die geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="9e990-130">Instead of clicking a link and downloading the entire copy of a document you're working on with your colleagues, DirectInvoke lets you download the parts of the document that have been changed.</span></span> <span data-ttu-id="9e990-131">Dieses Verfahren reduziert die Menge der übertragenen Daten und kann die zum Öffnen des Dokuments benötigte Zeit verkürzen.</span><span class="sxs-lookup"><span data-stu-id="9e990-131">This strategy reduces the amount of data transferred and can reduce the time needed to open the document.</span></span>  

## <a name="current-support-for-clickonce-and-directinvoke-in-microsoft-edge"></a><span data-ttu-id="9e990-132">Aktuelle Unterstützung für ClickOnce und DirectInvoke in Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="9e990-132">Current support for ClickOnce and DirectInvoke in Microsoft Edge</span></span>

<span data-ttu-id="9e990-133">Unterstützung für ClickOnce und DirectInvoke:</span><span class="sxs-lookup"><span data-stu-id="9e990-133">Support for ClickOnce and DirectInvoke:</span></span>

- <span data-ttu-id="9e990-134">ClickOnce und DirectInvoke werden standardmäßig für alle Windows-Benutzer unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9e990-134">ClickOnce and DirectInvoke are supported out of the box for all Windows users.</span></span>

  > [!NOTE]
  > <span data-ttu-id="9e990-135">Benutzer, die ClickOnce-Unterstützung deaktivieren möchten, können zu *edge://flags/#edge-click-once* wechseln und **Deaktiviert** aus der Dropdownliste auswählen.</span><span class="sxs-lookup"><span data-stu-id="9e990-135">Users that want to disable ClickOnce support can go to *edge://flags/#edge-click-once* and select **Disabled** from the dropdown list.</span></span> <span data-ttu-id="9e990-136">Anschließend müssen Sie den Browser **neu starten**.</span><span class="sxs-lookup"><span data-stu-id="9e990-136">You'll have to **Restart** the browser.</span></span>

- <span data-ttu-id="9e990-137">ClickOnce und DirectInvoke werden auf anderen Plattformen als Windows nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9e990-137">ClickOnce and DirectInvoke aren't supported on any platforms other than Windows.</span></span>

## <a name="clickonce-and-directinvoke-file-handling-security"></a><span data-ttu-id="9e990-138">Sicherheit beim Umgang mit ClickOnce- und DirectInvoke-Dateien</span><span class="sxs-lookup"><span data-stu-id="9e990-138">ClickOnce and DirectInvoke file handling security</span></span>

<span data-ttu-id="9e990-139">ClickOnce und DirectInvoke sind durch den URL-Bewertungsdienst von Microsoft Defender SmartScreen geschützt.</span><span class="sxs-lookup"><span data-stu-id="9e990-139">ClickOnce and DirectInvoke are protected by Microsoft Defender SmartScreen's URL reputation scanning service.</span></span>

<span data-ttu-id="9e990-140">Wenn eine ClickOnce- oder DirectInvoke-Anforderung vom URL-Bewertungsdienst von Microsoft Defender SmartScreen als unsicher gekennzeichnet wird, werden Benutzern mit aktiviertem ClickOnce oder DirectInvoke zwei Popups angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9e990-140">If a ClickOnce or a DirectInvoke request is flagged by the Microsoft Defender SmartScreen URL reputation service as unsafe, users with ClickOnce or DirectInvoke enabled will see two popups.</span></span>

<span data-ttu-id="9e990-141">Das erste Popup fragt den Benutzer, ob er die Datei öffnen möchte.</span><span class="sxs-lookup"><span data-stu-id="9e990-141">The first popup asks the user if they want to open the file.</span></span> <span data-ttu-id="9e990-142">Dieses Popup wird unabhängig davon angezeigt, ob die Datei als sicher oder unsicher gekennzeichnet wurde.</span><span class="sxs-lookup"><span data-stu-id="9e990-142">This popup is displayed regardless of whether the file was flagged as safe or unsafe.</span></span> <span data-ttu-id="9e990-143">Der Benutzer kann die **Datei als unsicher melden**, die Anforderung **abbrechen** oder auf **Öffnen** klicken, um den Vorgang fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="9e990-143">The user can **Report the file as unsafe**, **Cancel** the request, or click **Open** to continue.</span></span>

   ![Aufforderung zum Öffnen der Datei](./media/edge-learn-more-co-di/edge-clickonce-modal-1.png)

<span data-ttu-id="9e990-145">Wenn der Benutzer versucht, die Datei zu öffnen, und die Datei als unsicher gekennzeichnet wurde, wird ein zweites Popup angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9e990-145">If the user tries to open the file, and the file was flagged as unsafe, a second popup is displayed.</span></span>  <span data-ttu-id="9e990-146">Dieses Popup warnt den Benutzer, dass die Datei als unsicher gekennzeichnet wurde, und fragt ihn, ob er sicher ist, dass er die Datei herunterladen möchte.</span><span class="sxs-lookup"><span data-stu-id="9e990-146">This popup warns the user that the file was flagged as unsafe, and asks them if they're sure they want to download the file.</span></span>

<span data-ttu-id="9e990-147">Das zweite Popup wird nur angezeigt, wenn:</span><span class="sxs-lookup"><span data-stu-id="9e990-147">The second popup only shows up if:</span></span>

- <span data-ttu-id="9e990-148">die Datei eine ClickOnce- oder DirectInvoke-Datei ist</span><span class="sxs-lookup"><span data-stu-id="9e990-148">the file is a ClickOnce or DirectInvoke file</span></span>
- <span data-ttu-id="9e990-149">ClickOnce oder DirectInvoke aktiviert sind</span><span class="sxs-lookup"><span data-stu-id="9e990-149">ClickOnce or DirectInvoke are enabled</span></span>
- <span data-ttu-id="9e990-150">die Datei als unsicher gekennzeichnet wird</span><span class="sxs-lookup"><span data-stu-id="9e990-150">the file is flagged as unsafe</span></span>

 ![Aufforderung zum Öffnen einer unsicheren Datei](./media/edge-learn-more-co-di/edge-clickonce-modal-2.png)

> [!NOTE]
> <span data-ttu-id="9e990-152">Wenn ClickOnce oder DirectInvoke deaktiviert sind, werden angeforderte Dateien als reguläre Downloads behandelt und, wenn sie als unsicher gekennzeichnet sind, als unsicher markiert.</span><span class="sxs-lookup"><span data-stu-id="9e990-152">If ClickOnce or DirectInvoke are disabled, requested files are treated as regular downloads and if flagged as unsafe, will be marked as unsafe.</span></span> <span data-ttu-id="9e990-153">Dies entspricht der Behandlung von anderen unsicheren Downloads.</span><span class="sxs-lookup"><span data-stu-id="9e990-153">This is consistent with the treatment of other unsafe downloads.</span></span>

## <a name="clickonce-and-directinvoke-policies"></a><span data-ttu-id="9e990-154">ClickOnce- und DirectInvoke-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="9e990-154">ClickOnce and DirectInvoke policies</span></span>

<span data-ttu-id="9e990-155">Es gibt zwei Gruppenrichtlinien, mit denen Sie ClickOnce und DirectInvoke für Unternehmensbenutzer aktivieren oder deaktivieren können.</span><span class="sxs-lookup"><span data-stu-id="9e990-155">There are two group policies that you can use to enable or disable ClickOnce and DirectInvoke for enterprise users.</span></span> <span data-ttu-id="9e990-156">Diese beiden Richtlinien sind [ClickOnceEnabled](./microsoft-edge-policies.md#clickonceenabled) und [DirectInvokeEnabled](./microsoft-edge-policies.md#directinvokeenabled).</span><span class="sxs-lookup"><span data-stu-id="9e990-156">These two policies are [ClickOnceEnabled](./microsoft-edge-policies.md#clickonceenabled) and [DirectInvokeEnabled](./microsoft-edge-policies.md#directinvokeenabled).</span></span> <span data-ttu-id="9e990-157">Diese beiden Richtlinien sind im Gruppenrichtlinien-Editor mit "Zulassen, das Benutzer Dateien mit dem ClickOnce-Protokoll öffnen" und "Zulassen, dass Benutzer Dateien mit dem DirectInvoke-Protokoll öffnen" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="9e990-157">These two policies are labeled in the Group Policy Editor as "Allow users to open files using the ClickOnce protocol" and "Allow users to open files using the DirectInvoke protocol" respectively.</span></span>

## <a name="clickonce-and-directinvoke-behavior"></a><span data-ttu-id="9e990-158">ClickOnce- und DirectInvoke-Verhalten</span><span class="sxs-lookup"><span data-stu-id="9e990-158">ClickOnce and DirectInvoke behavior</span></span>

<span data-ttu-id="9e990-159">Die folgenden Beispiele zeigen die Dateiverarbeitung, wenn ClickOnce und DirectInvoke aktiviert oder deaktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="9e990-159">The following examples show file handling when ClickOnce and DirectInvoke are enabled or disabled.</span></span>

### <a name="clickonce-enabled"></a><span data-ttu-id="9e990-160">ClickOnce aktiviert</span><span class="sxs-lookup"><span data-stu-id="9e990-160">ClickOnce enabled</span></span>

1. <span data-ttu-id="9e990-161">Ein Benutzer öffnet einen Link zu einer Seite, die die ClickOnce-Unterstützung anfordert, und erhält die Aufforderung im nächsten Screenshot.</span><span class="sxs-lookup"><span data-stu-id="9e990-161">A user opens a link to a page that requests ClickOnce support and gets the prompt in the next screenshot.</span></span>

   ![Aufforderung zum Öffnen einer unsicheren Datei](./media/edge-learn-more-co-di/edge-clickonce-enabled-1.png)

2. <span data-ttu-id="9e990-163">Nachdem der Benutzer auf **Öffnen** geklickt hat, versucht ClickOnce, die Anwendung zu starten.</span><span class="sxs-lookup"><span data-stu-id="9e990-163">After the user clicks **Open**, ClickOnce attempts to launch the application.</span></span>

   ![ClickOnce versucht, die Anwendung zu starten](./media/edge-learn-more-co-di/edge-clickonce-enabled-launch-app.png)

3. <span data-ttu-id="9e990-165">Nachdem der Benutzer auf **Öffnen**geklickt hat, wird im Browser ein Popup angezeigt, in dem der Benutzer gefragt wird, ob er sicher ist, dass die Anwendung installiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="9e990-165">After the user clicks **Open**, the browser shows a popup that asks the user if they're sure they want to install the application.</span></span>

   ![Aufforderung zum Öffnen der Datei](./media/edge-learn-more-co-di/edge-clickonce-enabled-2.png)

   > [!NOTE]
   > <span data-ttu-id="9e990-167">Die vom ClickOnce-Dateihandler gezeigte Schnittstelle, Nachrichten und Optionen variieren je nach Typ und Konfiguration der Datei, auf die zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="9e990-167">The interface, messaging, and options shown by the ClickOnce file handler will vary depending on the type and configuration of the file that's accessed.</span></span>

### <a name="clickonce-disabled"></a><span data-ttu-id="9e990-168">ClickOnce deaktiviert</span><span class="sxs-lookup"><span data-stu-id="9e990-168">ClickOnce disabled</span></span>

1. <span data-ttu-id="9e990-169">Wenn ein Benutzer einen Link zu einer Seite öffnet, die ClickOnce-Unterstützung anfordert, wird eine Meldung im Download-Tray angezeigt, die jener im nächsten Screenshot ähnelt.</span><span class="sxs-lookup"><span data-stu-id="9e990-169">When a user opens a link to a page that requests ClickOnce support, they will see a message in the download tray that is similar to the one in the next screenshot.</span></span>

   ![Aufforderung zum Herunterladen der Datei](./media/edge-learn-more-co-di/edge-clickonce-disabled-1.png)

### <a name="directinvoke-enabled"></a><span data-ttu-id="9e990-171">DirectInvoke deaktiviert</span><span class="sxs-lookup"><span data-stu-id="9e990-171">DirectInvoke enabled</span></span>

1. <span data-ttu-id="9e990-172">Ein Benutzer öffnet einen Link zu einer Seite, die die DirectInvoke-Unterstützung anfordert, und erhält die Aufforderung im nächsten Screenshot.</span><span class="sxs-lookup"><span data-stu-id="9e990-172">A user opens a link to a page that requests DirectInvoke support and gets the prompt in the next screenshot.</span></span>

   ![Aufforderung zum Öffnen der Datei](./media/edge-learn-more-co-di/edge-directinvoke-open-link-1.png)

2. <span data-ttu-id="9e990-174">Wenn der Benutzer auf **Öffnen** klickt, wird der angeforderte Dateihandler geöffnet.</span><span class="sxs-lookup"><span data-stu-id="9e990-174">When the user clicks **Open**, the requested file handler is opened.</span></span> <span data-ttu-id="9e990-175">In diesem Beispiel wird Microsoft Word verwendet, um das im vorherigen Screenshot gezeigte Dokument zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="9e990-175">In this example, Microsoft Word is used to open the document that's shown in the previous screenshot.</span></span>

   > [!NOTE]
   > <span data-ttu-id="9e990-176">Die vom DirectInvoke-Dateihandler gezeigte Schnittstelle, Nachrichten und Optionen variieren je nach Typ und Konfiguration der Datei, auf die zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="9e990-176">The interface, messaging, and options shown by the DirectInvoke file handler will vary depending on the type and configuration of the file that's accessed.</span></span>

### <a name="directinvoke-disabled"></a><span data-ttu-id="9e990-177">DirectInvoke deaktiviert</span><span class="sxs-lookup"><span data-stu-id="9e990-177">DirectInvoke disabled</span></span>

1. <span data-ttu-id="9e990-178">Wenn ein Benutzer einen Link zu einer Seite öffnet, die die DirectInvoke-Unterstützung anfordert, verhält sich DirectInvoke genauso wie ClickOnce deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="9e990-178">When a user opens a link to a page that requests DirectInvoke support, DirectInvoke behaves the same as when ClickOnce is disabled.</span></span> <span data-ttu-id="9e990-179">Im Download-Tray wird eine Meldung angezeigt, die jener im nächsten Screenshot ähnelt.</span><span class="sxs-lookup"><span data-stu-id="9e990-179">They will see a message in the download tray that's similar to the one in the next screenshot.</span></span>

   ![Aufforderung zum Öffnen der Datei](./media/edge-learn-more-co-di/edge-directinvoke-open-link-2.png)

## <a name="see-also"></a><span data-ttu-id="9e990-181">Weitere Informationen:</span><span class="sxs-lookup"><span data-stu-id="9e990-181">See also</span></span>

- [<span data-ttu-id="9e990-182">ClickOnce-Sicherheit und -Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="9e990-182">ClickOnce security and deployment</span></span>](/visualstudio/deployment/clickonce-security-and-deployment)
- [<span data-ttu-id="9e990-183">DirectInvoke im Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="9e990-183">DirectInvoke in Internet Explorer</span></span>](/previous-versions/windows/internet-explorer/ie-developer/dev-guides/jj215788(v=vs.85))
- [<span data-ttu-id="9e990-184">Microsoft Edge Enterprise-Angebotsseite</span><span class="sxs-lookup"><span data-stu-id="9e990-184">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)