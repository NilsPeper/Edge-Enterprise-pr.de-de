---
title: Umleitung von Internet Explorer zu Microsoft Edge zur Kompatibilität mit modernen Websites
ms.author: laannade
author: dan-wesley
manager: ratetali
ms.date: 11/16/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Umleitung von Internet Explorer zu Microsoft Edge zur Kompatibilität mit modernen Websites
ms.openlocfilehash: 7cd74eda6d8ada7647862ea69f77a982713f0c14
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2021
ms.locfileid: "11617295"
---
# <a name="redirection-from-internet-explorer-to-microsoft-edge-for-compatibility-with-modern-web-sites"></a>Umleitung von Internet Explorer zu Microsoft Edge zur Kompatibilität mit modernen Websites

> [!NOTE]
> Dieser Artikel bezieht sich auf die stabile Microsoft Edge Version 87 oder neuer.

## <a name="overview"></a>Übersicht

>[!Note]
> Die Internet Explorer 11-Desktopanwendung wird eingestellt und wird ab dem 15. Juni 2022 nicht mehr unterstützt (eine Liste der in diesem Bereich enthaltenen Elemente [finden Sie in den FAQ](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549)). Dieselben IE11-Apps und -Websites, die Sie heute verwenden, können in Microsoft Edge im Internet Explorer-Modus geöffnet werden. [Weitere Informationen finden Sie hier](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/).

Viele moderne Websites haben Designs, die mit Internet Explorer nicht kompatibel sind. Immer wenn ein Internet Explorer-Benutzer eine inkompatible öffentliche Website besucht, erhält er eine Nachricht, die besagt, dass die Website mit seinem Browser inkompatibel ist, und er muss manuell zu einem anderen Browser wechseln.

Die Notwendigkeit, manuell zu einem anderen Browser zu wechseln, ändert sich ab der stabilen Microsoft Edge Version 87.

Wenn ein Benutzer zu einer Website wechselt, die mit Internet Explorer nicht kompatibel ist, wird er automatisch zu Microsoft Edge umgeleitet. In diesem Artikel werden die Benutzererfahrung für die Umleitung sowie die Gruppenrichtlinien beschrieben, die zum Konfigurieren oder Deaktivieren der automatischen Umleitung verwendet werden.

> [!NOTE]
> Microsoft verwaltet eine Liste aller Websites, von denen bekannt ist, dass sie nicht mit Internet Explorer kompatibel sind. Weitere Informationen finden Sie unter [Anfordern von Updates für die Liste inkompatibler Websites](/microsoft-edge/web-platform/ie-to-microsoft-edge-redirection#request-an-update-to-the-ie-compatibility-list)

## <a name="prerequisites"></a>Voraussetzungen
- Microsoft Edge Stabile Version 87 oder höher
- Windows Versionen
    - Windows10 Version 1709 oder höher
    - Windows8.1
    - Windows7



## <a name="redirection-experience"></a>Umleitungserfahrung

Bei der Umleitung zu Microsoft Edge wird den Benutzern das einmalige Dialogfeld im nächsten Screenshot angezeigt. In diesem Dialogfeld wird erklärt, warum sie umgeleitet werden, und fordert sie auf, die Zustimmung zum Kopieren ihrer Browserdaten und -Einstellungen von Internet Explorer zu Microsoft Edge zu erteilen. Die folgenden Browserdaten werden importiert: Favoriten, Kennwörter, Suchmaschinen, offene Registerkarten, Verlauf, Einstellungen, Cookies und die Startseite.

![Suchbenachrichtigung und Aufforderung zum Import von Daten und Einstellungen.](media/edge-learnmore-neededge/neededge-dialog1.png)

Selbst wenn sie keine Zustimmung durch das Ankreuzen von „Meine Browserdaten und -Einstellungen von Internet Explorer immer übermitteln", können sie auf **Weiter surfen** klicken, um ihre Sitzung fortzusetzen.

Schließlich wird für jede Umleitung unterhalb der Adressleiste ein Banner zur Websiteinkompatibilität angezeigt, das im nächsten Screenshot dargestellt wird.

![Benachrichtigung über moderne Websites und Aufforderung, Microsoft Edge als Standardbrowser festzulegen oder Microsoft Edge zu erkunden.](media/edge-learnmore-neededge/neededge-banner.png)

Das Banner zur Websiteinkompatibilität:

- Ermutigt den Benutzer, zu Microsoft Edge zu wechseln.
- Bietet an, Microsoft Edge als Standardbrowser festzulegen.
- Bietet dem Benutzer die Möglichkeit, Microsoft Edge zu erkunden.

Wenn eine Website von Internet Explorer zu Microsoft Edge umgeleitet wird, wird die Internet Explorer-Registerkarte, mit der die Website geladen wurde, geschlossen, wenn Sie keine vorherigen Inhalte aufweist. Andernfalls wechselt die aktive Registerkartendarstellung zu einer Microsoft [Support](https://support.microsoft.com/office/the-website-you-were-trying-to-reach-doesn-t-work-with-internet-explorer-8f5fc675-cd47-414c-9535-12821ddfc554?ui=en-US&rs=en-US&ad=US) -Seite, die erklärt, warum die Website zu Microsoft Edge umgeleitet wurde.

> [!NOTE]
> Nach einer Umleitung können Benutzer zu Internet Explorer zurückkehren, um Websites zu nutzen, die nicht in der Internet Explorer-Inkompatibilitätsliste enthalten sind.  

## <a name="policies-to-configure-redirection-to-microsoft-edge"></a>Richtlinien zum Konfigurieren der Umleitung zu Microsoft Edge

> [!NOTE]
> Diese Richtlinien werden bis zum 26. Oktober 2020 als ADMX-Datei-Updates, und bis zum 9. November 2020 in Intune verfügbar sein.

Drei Gruppenrichtlinien müssen konfiguriert sein, um die automatische Umleitung zu Microsoft Edge zu aktivieren. Diese Richtlinien lauten:

- RedirectSitesFromInternetExplorerPreventBHOInstall
- RedirectSitesFromInternetExplorerRedirectMode
- HideInternetExplorerRedirectUXForIncompatibleSitesEnabled

### <a name="policy-redirectsitesfrominternetexplorerpreventbhoinstall"></a>Richtlinie: RedirectSitesFromInternetExplorerPreventBHOInstall

Die Umleitung von Internet Explorer zu Microsoft Edge erfordert ein Internet Explorer-Browserhilfsobjekt (BHO) mit dem Namen „IEtoEdge BHO“. Die Richtlinie **RedirectSitesFromInternetExplorerPreventBHOInstall** steuert, ob dieses BHO installiert ist oder nicht.  

- Wenn Sie diese Richtlinie aktivieren, wird das für die Umleitung erforderliche BHO nicht installiert, und Ihre Benutzer sehen weiterhin Inkompatibilitätsmeldungen für bestimmte Websites in Internet Explorer. Wenn das BHO bereits installiert ist, wird es beim nächsten Update des stabilen Microsoft Edge-Kanals deinstalliert.
- Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, wird das BHO installiert. Hierbei handelt es sich um das standardmäßige Verhalten.

Zusätzlich zur Notwendigkeit des BHO gibt es eine Abhängigkeit bei **RedirectSitesFromInternetExplorerRedirectMode**, was auf „Websites basierend auf der Websiteliste inkompatibler Websites umleiten“ oder „Nicht konfiguriert“ festgelegt sein muss.

### <a name="policy-redirectsitesfrominternetexplorerredirectmode"></a>Richtlinie: RedirectSitesFromInternetExplorerRedirectMode

 Diese Richtlinie entspricht der Microsoft Edge-**Standardbrowser**-Einstellung „Internet Explorer kann Websites in Microsoft Edge öffnen". Sie können auf diese Einstellung zugreifen, indem Sie zur URL *edge://settings/defaultbrowser* wechseln.  

- Wenn Sie diese Richtlinie nicht konfigurieren oder auf „Websiteliste“ festlegen, leitet Internet Explorer inkompatible Websites zu Microsoft Edge um. Hierbei handelt es sich um das standardmäßige Verhalten.
- Wenn Sie diese Richtlinie deaktivieren möchten, wählen Sie **Aktiviert** UND dann in der Dropdownliste unter “Optionen: Inkompatible Websites von Internet Explorer zu Microsoft Edge umleiten” **Deaktivieren** aus. In diesem Zustand werden inkompatible Websites nicht zu Microsoft Edge umgeleitet.

> [!NOTE]
> Wenn Sie ein persönliches Gerät verwenden, das nicht von Ihrem Unternehmen verwaltet wird, wird unter **Internet Explorer-Kompatibilität** die Einstellung „Zulassen, dass Websites im Internet Explorer-Modus geladen werden“ angezeigt.
>
>Wenn Sie ein in die Domäne eingebundenes Gerät oder ein beim Mobile Device Management (MDM) registriertes Gerät verwenden, wird diese Option nicht angezeigt.
>
> Wenn Sie Ihren Benutzern stattdessen das Laden von Websites im Internet Explorer-Modus gestatten möchten, können Sie dies tun, indem Sie die Richtlinie [Internet Explorer-Modustest](./microsoft-edge-policies.md#intranetredirectbehavior) konfigurieren.

### <a name="policy-hideinternetexplorerredirectuxforincompatiblesitesenabled"></a>Richtlinie: HideInternetExplorerRedirectUXForIncompatibleSitesEnabled

Diese Richtlinie konfiguriert die Benutzererfahrung bei der Umleitung bei inkompatiblen Websites zu Microsoft Edge.  

- Wenn Sie diese Richtlinie aktivieren, wird den Benutzern nie das einmalige Umleitungsdialogfeld und das Umleitungsbanner angezeigt. Es werden keine Browserdaten oder Benutzereinstellungen importiert.
- Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, wird das Umleitungsdialogfeld bei der ersten Umleitung angezeigt, und das beständige Umleitungsbanner wird für Sitzungen angezeigt, die mit einer Umleitung beginnen.

  > [!NOTE]
  > Benutzer-Browserdaten werden jedes Mal importiert, wenn ein Benutzer neu umgeleitet wird. Dies geschieht jedoch nur, wenn der Benutzer dem Import im einmaligen Umleitungsdialogfeld zugestimmt hat.

## <a name="disable-redirection-to-microsoft-edge"></a>Deaktivieren der Umleitung zu Microsoft Edge

Wenn Sie die Umleitung VOR dem Update auf die stabile Microsoft Edge-Version 87 deaktivieren möchten, führen Sie die folgenden Schritte aus:

1. Legen Sie die Richtlinie **RedirectSitesFromInternetExplorerPreventBHOInstall** auf **Aktiviert** fest.

Wenn Sie die Umleitung NACH dem Update auf die stabile Microsoft Edge-Version 87 deaktivieren möchten, führen Sie die folgenden Schritte aus:

1. Legen Sie die Richtlinie **RedirectSitesFromInternetExplorerRedirectMode** auf **Aktiviert** fest, und wählen Sie dann in der Dropdownliste unter “Optionen: Inkompatible Websites von Internet Explorer zu Microsoft Edge umleiten” **Deaktivieren** aus. Diese Einstellung beendet die Umleitung, sobald die Richtlinie wirksam wird.
2. Legen Sie die Richtlinie **RedirectSitesFromInternetExplorerPreventBHOInstall** auf **Aktiviert** fest. Damit wird das BHO nach dem nächsten Microsoft Edge-Update deinstalliert.

## <a name="see-also"></a>Siehe auch

- [Anfordern von Updates für die Liste inkompatibler Websites](/microsoft-edge/web-platform/ie-to-microsoft-edge-redirection#request-an-update-to-the-ie-compatibility-list)
- [Angebotsseite für Microsoft Edge für Unternehmen](https://aka.ms/EdgeEnterprise)
- [Microsoft Edge-Richtlinien](./microsoft-edge-policies.md)