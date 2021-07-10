---
title: Abwärtskompatibilität für Enterprise-Seite „Neue Registerkarte”
ms.author: ruchir
author: dan-wesley
manager: vwehren
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Abwärtskompatibilität für Enterprise-Seite „Neue Registerkarte”
ms.openlocfilehash: e2534f9df82aa81843d7cd292ada99a4c7574a3c
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "11642081"
---
# <a name="backwards-compatibility-for-the-enterprise-new-tab-page"></a><span data-ttu-id="e8f48-103">Abwärtskompatibilität für Enterprise-Seite „Neue Registerkarte”</span><span class="sxs-lookup"><span data-stu-id="e8f48-103">Backwards compatibility for the Enterprise New tab page</span></span>

<span data-ttu-id="e8f48-104">Dieser Artikel beschreibt die Änderung auf der Seite „Neue Registerkarte“ und wie Benutzer mit Microsoft Edge Version 87 und früher abwärtskompatibel sein können.</span><span class="sxs-lookup"><span data-stu-id="e8f48-104">This article describes the change to the New tab page and how users can be backwards compatible with Microsoft Edge version 87 and earlier.</span></span>

> [!NOTE]
> <span data-ttu-id="e8f48-105">Dieser Artikel bezieht sich auf Microsoft Edge Version 87 oder neuer.</span><span class="sxs-lookup"><span data-stu-id="e8f48-105">This article applies to Microsoft Edge version 87 or later.</span></span>

## <a name="information-feeds-from-single-endpoint"></a><span data-ttu-id="e8f48-106">Informations-Feeds von einem einzigen Endpunkt</span><span class="sxs-lookup"><span data-stu-id="e8f48-106">Information feeds from single endpoint</span></span>

<span data-ttu-id="e8f48-107">Die neue Version der Enterprise-Seite „Neue Registerkarte“ kombiniert konforme Microsoft 365-Inhalte mit branchenrelevanten und konformen Informations-Feeds, die über den MSN.com-Endpunkt bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="e8f48-107">The new version of the Enterprise New tab page combines compliant Microsoft 365 content with industry relevant and compliant information feeds that are served via the MSN.com endpoint.</span></span>

> [!NOTE]
> <span data-ttu-id="e8f48-108">Office 365-Inhalte wurden ursprünglich mithilfe der Domäne [Office.com](https://www.office.com) bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="e8f48-108">Office 365 content was originally served using the [Office.com](https://www.office.com) domain.</span></span>

<span data-ttu-id="e8f48-109">Wenn der Zugriff auf die MSN.com-Domäne für Ihre Organisation eingeschränkt ist, empfehlen wir dringend, den Benutzern den Zugriff auf diese [URL](https://ntp.msn.com).</span><span class="sxs-lookup"><span data-stu-id="e8f48-109">If access to the MSN.com domain is restricted for your organization, we strongly recommend giving users access to this [url](https://ntp.msn.com).</span></span>

<span data-ttu-id="e8f48-110">Wenn Sie mehr Zeit benötigen, um den Zugriff auf die MSN-Domäne zu ermöglichen, empfehlen wir die Verwendung von [NewTabPageSetFeedType](./microsoft-edge-policies.md#newtabpagesetfeedtype), mit dem Sie für die Seite „Neue Registerkarte“ entweder die Microsoft News- oder die Office 365-Feed-Erfahrung wählen können.</span><span class="sxs-lookup"><span data-stu-id="e8f48-110">If you need more time to enable access to the MSN domain, we recommend using the [NewTabPageSetFeedType](./microsoft-edge-policies.md#newtabpagesetfeedtype), that lets you choose either the Microsoft News or Office 365 feed experience for the new tab page.</span></span>

### <a name="keep-using-officecom"></a><span data-ttu-id="e8f48-111">Verwenden Sie weiterhin Office.com</span><span class="sxs-lookup"><span data-stu-id="e8f48-111">Keep using Office.com</span></span>

 <span data-ttu-id="e8f48-112">Sie können die Richtlinie **NewTabPageSetFeedType** so konfigurieren, dass weiterhin die veraltete Office.com-Domäne verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e8f48-112">You can configure the **NewTabPageSetFeedType** policy to keep using the deprecated Office.com domain.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e8f48-113">Die Richtlinie **NewTabPageSetFeedType** und die Office.com-Domäne, die Office 365-Inhalte bereitstellt, funktionieren nicht mehr, wenn die Microsoft Edge-Version 90 veröffentlicht wird.</span><span class="sxs-lookup"><span data-stu-id="e8f48-113">The **NewTabPageSetFeedType** policy and the Office.com domain that serves Office 365 content will quit working when Microsoft Edge version 90 is released.</span></span>

<span data-ttu-id="e8f48-114">Die folgenden Richtlinieneinstellungen erzwingen, dass die Enterprise-Seite „Neue Registerkarte“ den Inhalt von Office-Dokumenten aus der Office.com-Domäne rendert.</span><span class="sxs-lookup"><span data-stu-id="e8f48-114">The following policy settings will force the Enterprise New tab page to render Office document content from the Office.com domain.</span></span>

- <span data-ttu-id="e8f48-115">Legen Sie die Richtlinie als **Obligatorisch** fest.</span><span class="sxs-lookup"><span data-stu-id="e8f48-115">Set the policy as **Mandatory**.</span></span>
- <span data-ttu-id="e8f48-116">Legen Sie den Wert für die Richtlinienzuordnung auf **Office (1) = Office 365-Feed-Erfahrung** fest.</span><span class="sxs-lookup"><span data-stu-id="e8f48-116">Set the value of the policy mapping to **Office (1) = Office 365 feed experience**.</span></span>

<span data-ttu-id="e8f48-117">Wenn der Umstieg auf Office.com nicht möglich ist, wenden Sie sich an uns und senden Sie uns Ihr Feedback.</span><span class="sxs-lookup"><span data-stu-id="e8f48-117">If the switch to the Office.com isn't possible, reach out and send us feedback.</span></span> <span data-ttu-id="e8f48-118">Eine weitere Möglichkeit besteht darin, die [NewTabPageLocation](./microsoft-edge-policies.md#newtabpagelocation) so zu konfigurieren, dass sie auf eine Endpunkt-URL verweist, die von Ihrer Organisation zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="e8f48-118">Another option is to configure the [NewTabPageLocation](./microsoft-edge-policies.md#newtabpagelocation) so it points to an endpoint URL that's allowed by your organization.</span></span>

> [!NOTE]
> <span data-ttu-id="e8f48-119">Die Richtlinie **NewTabPageLocation** hat Vorrang, wenn auch die Richtlinie **NewTabPageSetFeedType** konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="e8f48-119">The **NewTabPageLocation** policy has precedence if the **NewTabPageSetFeedType** policy is also configured.</span></span>

## <a name="enterprise-users-will-now-get-microsoft-news-content-via-my-feed"></a><span data-ttu-id="e8f48-120">Enterprise-Benutzer erhalten jetzt Microsoft-Nachrichteninhalte über „Mein Feed“</span><span class="sxs-lookup"><span data-stu-id="e8f48-120">Enterprise users will now get Microsoft news content via My Feed</span></span>

<span data-ttu-id="e8f48-121">Die Enterprise-Seite „Neue Registerkarte“ bietet branchenrelevante Informationen in **Mein Feed** und Office 365-Inhalt in einer einzigen Ansicht für Benutzer, die mit Ihrem Azure Active Directory (Azure AD)-Konto angemeldet sind.</span><span class="sxs-lookup"><span data-stu-id="e8f48-121">The Enterprise New tab page will offer industry relevant information in **My Feed** and Office 365 content in a single view for users signed in with their Azure Active Directory (Azure AD) account.</span></span> <span data-ttu-id="e8f48-122">Für Benutzer, die mit ihrem Azure Active Directory (Azure AD) angemeldet sind und im Einstellungs-Flyout die Option „Microsoft News“ gewählt haben, wird die neue Registerkartenansicht durch den Inhalt von **Mein Feed** ersetzt.</span><span class="sxs-lookup"><span data-stu-id="e8f48-122">For users signed in with their Azure Active Directory (Azure AD) who selected the Microsoft News option in the settings flyout, their new tab page view will be replaced with **My Feed** content.</span></span> <span data-ttu-id="e8f48-123">Wenn sie eine neue Registerkarte im Browser öffnen, sieht diese wie das Beispiel im nächsten Screenshot aus.</span><span class="sxs-lookup"><span data-stu-id="e8f48-123">When they open a new tab page in the browser it will look like the example in the next screenshot.</span></span>

![Seite „Neue Registerkarte“ mit Inhalten aus „Mein Feed“.](media/microsoft-edge-ntp-backward-compatibility/microsoft-edge-ntp-myfeed-view.png)

> [!NOTE]
> <span data-ttu-id="e8f48-125">Benutzer, die nicht bei Azure AD angemeldet sind, sehen weiterhin den MSN News-Feed, wenn sie eine neue Registerkarte öffnen.</span><span class="sxs-lookup"><span data-stu-id="e8f48-125">Users who aren't signed in with Azure AD will continue to see the MSN News feed when they open a new tab.</span></span>

## <a name="page-layout"></a><span data-ttu-id="e8f48-126">Seitenlayout</span><span class="sxs-lookup"><span data-stu-id="e8f48-126">Page layout</span></span>

<span data-ttu-id="e8f48-127">Mit den Änderungen an der Seite „Neue Registerkarte“ muss das Seitenlayout nicht mehr zwei bestimmte Inhaltstypen (Office 365 und Microsoft News) steuern, so dass der Inhaltsumschalter nicht mehr verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="e8f48-127">With the changes to the New tab page, the Page layout no longer has to control two specific content types (Office 365 and Microsoft News), so the content toggle isn't available.</span></span> <span data-ttu-id="e8f48-128">Im nächsten Screenshot wird das Flyout für das Seitenlayout angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e8f48-128">The next screenshot shows the flyout for the Page layout.</span></span>

![Ansicht „Seitenlayout“ für die Seite „Neue Registerkarte“.](media/microsoft-edge-ntp-backward-compatibility/microsoft-edge-ntp-page-layout.png)

<span data-ttu-id="e8f48-130">Wenn Sie weiterhin auf Microsoft News-Inhalte zugreifen möchten, die nicht an Ihre Organisation gebunden sind, müssen Sie ein anderes Browserprofil verwenden.</span><span class="sxs-lookup"><span data-stu-id="e8f48-130">If you want to keep accessing Microsoft News content that isn't tied to your organization, you must use a different browser profile.</span></span> <span data-ttu-id="e8f48-131">Wechseln Sie zu *edge://settings/profiles*, und melden Sie sich von Ihrem Azure AD-Profil ab.</span><span class="sxs-lookup"><span data-stu-id="e8f48-131">Go to  *edge://settings/profiles* and sign out of your Azure AD profile.</span></span> <span data-ttu-id="e8f48-132">Mit dieser Aktion wird die standardmäßige Anzeige für die Enterprise-Seite „Neue Registerkarte“ angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e8f48-132">This action will bring up the  standard view for the Enterprise new tab page.</span></span> 

## <a name="see-also"></a><span data-ttu-id="e8f48-133">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e8f48-133">See also</span></span>

- [<span data-ttu-id="e8f48-134">Microsoft Edge Enterprise-Angebotsseite</span><span class="sxs-lookup"><span data-stu-id="e8f48-134">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="e8f48-135">Unternehmensmodus für Internet Explorer 11</span><span class="sxs-lookup"><span data-stu-id="e8f48-135">Enterprise Mode for Internet Explorer 11</span></span>](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)