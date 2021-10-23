---
title: Abwärtskompatibilität für Enterprise-Seite „Neue Registerkarte”
ms.author: ruchir
author: dan-wesley
manager: vwehren
ms.date: 10/21/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Abwärtskompatibilität für Enterprise-Seite „Neue Registerkarte”
ms.openlocfilehash: eb8e7a69da876e844a576c20f0194d14c92eaeee
ms.sourcegitcommit: f0966278011219cbab4590487a8b34cb76a73232
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/22/2021
ms.locfileid: "12107520"
---
# <a name="backwards-compatibility-for-the-enterprise-new-tab-page"></a>Abwärtskompatibilität für Enterprise-Seite „Neue Registerkarte”

Dieser Artikel beschreibt die Änderung auf der Seite „Neue Registerkarte“ und wie Benutzer mit Microsoft Edge Version 87 und früher abwärtskompatibel sein können.

> [!NOTE]
> Dieser Artikel bezieht sich auf Microsoft Edge Version 87 oder neuer.

## <a name="information-feeds-from-single-endpoint"></a>Informations-Feeds von einem einzigen Endpunkt

Die neue Version der Enterprise-Seite „Neue Registerkarte“ kombiniert konforme Microsoft 365-Inhalte mit branchenrelevanten und konformen Informations-Feeds, die über den MSN.com-Endpunkt bereitgestellt werden.

> [!NOTE]
> Office 365-Inhalte wurden ursprünglich mithilfe der Domäne [Office.com](https://www.office.com) bereitgestellt.

Wenn der Zugriff auf die MSN.com-Domäne für Ihre Organisation eingeschränkt ist, wird dringend empfohlen, Benutzern Zugriff darauf zu [https://ntp.msn.com](https://ntp.msn.com) gewähren.

Wenn Sie mehr Zeit benötigen, um den Zugriff auf die MSN-Domäne zu ermöglichen, empfehlen wir die Verwendung von [NewTabPageSetFeedType](./microsoft-edge-policies.md#newtabpagesetfeedtype), mit dem Sie für die Seite „Neue Registerkarte“ entweder die Microsoft News- oder die Office 365-Feed-Erfahrung wählen können.

### <a name="keep-using-officecom"></a>Verwenden Sie weiterhin Office.com

 Sie können die Richtlinie **NewTabPageSetFeedType** so konfigurieren, dass weiterhin die veraltete Office.com-Domäne verwendet wird.

> [!IMPORTANT]
> Die Richtlinie **NewTabPageSetFeedType** und die Office.com-Domäne, die Office 365-Inhalte bereitstellt, funktionieren nicht mehr, wenn die Microsoft Edge-Version 90 veröffentlicht wird.

Die folgenden Richtlinieneinstellungen erzwingen, dass die Enterprise-Seite „Neue Registerkarte“ den Inhalt von Office-Dokumenten aus der Office.com-Domäne rendert.

- Legen Sie die Richtlinie als **Obligatorisch** fest.
- Legen Sie den Wert für die Richtlinienzuordnung auf **Office (1) = Office 365-Feed-Erfahrung** fest.

Wenn der Umstieg auf Office.com nicht möglich ist, wenden Sie sich an uns und senden Sie uns Ihr Feedback. Eine weitere Möglichkeit besteht darin, die [NewTabPageLocation](./microsoft-edge-policies.md#newtabpagelocation) so zu konfigurieren, dass sie auf eine Endpunkt-URL verweist, die von Ihrer Organisation zulässig ist.

> [!NOTE]
> Die Richtlinie **NewTabPageLocation** hat Vorrang, wenn auch die Richtlinie **NewTabPageSetFeedType** konfiguriert ist.

## <a name="enterprise-users-will-now-get-microsoft-news-content-via-my-feed"></a>Enterprise-Benutzer erhalten jetzt Microsoft-Nachrichteninhalte über „Mein Feed“

Die Enterprise-Seite „Neue Registerkarte“ bietet branchenrelevante Informationen in **Mein Feed** und Office 365-Inhalt in einer einzigen Ansicht für Benutzer, die mit Ihrem Azure Active Directory (Azure AD)-Konto angemeldet sind. Für Benutzer, die mit ihrem Azure Active Directory (Azure AD) angemeldet sind und im Einstellungs-Flyout die Option „Microsoft News“ gewählt haben, wird die neue Registerkartenansicht durch den Inhalt von **Mein Feed** ersetzt. Wenn sie eine neue Registerkarte im Browser öffnen, sieht diese wie das Beispiel im nächsten Screenshot aus.

![Seite „Neue Registerkarte“ mit Inhalten aus „Mein Feed“.](media/microsoft-edge-ntp-backward-compatibility/microsoft-edge-ntp-myfeed-view.png)

> [!NOTE]
> Benutzer, die nicht bei Azure AD angemeldet sind, sehen weiterhin den MSN News-Feed, wenn sie eine neue Registerkarte öffnen.

## <a name="page-layout"></a>Seitenlayout

Mit den Änderungen an der Seite „Neue Registerkarte“ muss das Seitenlayout nicht mehr zwei bestimmte Inhaltstypen (Office 365 und Microsoft News) steuern, so dass der Inhaltsumschalter nicht mehr verfügbar ist. Im nächsten Screenshot wird das Flyout für das Seitenlayout angezeigt.

![Ansicht „Seitenlayout“ für die Seite „Neue Registerkarte“.](media/microsoft-edge-ntp-backward-compatibility/microsoft-edge-ntp-page-layout.png)

Wenn Sie weiterhin auf Microsoft News-Inhalte zugreifen möchten, die nicht an Ihre Organisation gebunden sind, müssen Sie ein anderes Browserprofil verwenden. Wechseln Sie zu *edge://settings/profiles*, und melden Sie sich von Ihrem Azure AD-Profil ab. Mit dieser Aktion wird die standardmäßige Anzeige für die Enterprise-Seite „Neue Registerkarte“ angezeigt. 

## <a name="see-also"></a>Weitere Informationen

- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)
- [Unternehmensmodus für Internet Explorer 11](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)