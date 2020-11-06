---
title: Umleitung von Internet Explorer zu Microsoft Edge zur Kompatibilität mit modernen Websites
ms.author: laannade
author: dan-wesley
manager: ratetali
ms.date: 11/03/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Umleitung von Internet Explorer zu Microsoft Edge zur Kompatibilität mit modernen Websites
ms.openlocfilehash: d822bf4cef76fe4c0298133b47ed80f5d1242b3d
ms.sourcegitcommit: 73fec3998f26d110252ace621be01f1c1142cf57
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2020
ms.locfileid: "11151095"
---
# Umleitung von Internet Explorer zu Microsoft Edge zur Kompatibilität mit modernen Websites

> [!NOTE]
> Dieser Artikel bezieht sich auf die stabile Microsoft Edge Version 87 oder neuer.

## Übersicht

Viele moderne Websites haben Designs, die mit Internet Explorer nicht kompatibel sind. Immer wenn ein Internet Explorer-Benutzer eine inkompatible öffentliche Website besucht, erhält er eine Nachricht, die besagt, dass die Website mit seinem Browser inkompatibel ist, und er muss manuell zu einem anderen Browser wechseln.

Die Notwendigkeit, manuell zu einem anderen Browser zu wechseln, ändert sich ab der stabilen Microsoft Edge Version 87.

Wenn ein Benutzer zu einer Website wechselt, die mit Internet Explorer nicht kompatibel ist, wird er automatisch zu Microsoft Edge umgeleitet. In diesem Artikel werden die Benutzererfahrung für die Umleitung sowie die Gruppenrichtlinien beschrieben, die zum Konfigurieren oder Deaktivieren der automatischen Umleitung verwendet werden.

> [!NOTE]
> Microsoft verwaltet eine Liste aller Websites, von denen bekannt ist, dass sie nicht mit Internet Explorer kompatibel sind.

## Umleitungserfahrung

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

## Richtlinien zum Konfigurieren der Umleitung zu Microsoft Edge

> [!NOTE]
> Diese Richtlinien werden bis zum 26. Oktober 2020 als ADMX-Datei-Updates, und bis zum 9. November 2020 in Intune verfügbar sein.

Drei Gruppenrichtlinien müssen konfiguriert sein, um die automatische Umleitung zu Microsoft Edge zu aktivieren. Diese Richtlinien lauten:

- RedirectSitesFromInternetExplorerPreventBHOInstall
- RedirectSitesFromInternetExplorerRedirectMode
- HideInternetExplorerRedirectUXForIncompatibleSitesEnabled

### Richtlinie: RedirectSitesFromInternetExplorerPreventBHOInstall

Die Umleitung von Internet Explorer zu Microsoft Edge erfordert ein Internet Explorer-Browserhilfsobjekt (BHO) mit dem Namen „IEtoEdge BHO“. Die Richtlinie **RedirectSitesFromInternetExplorerPreventBHOInstall** steuert, ob dieses BHO installiert ist oder nicht.  

- Wenn Sie diese Richtlinie aktivieren, wird das für die Umleitung erforderliche BHO nicht installiert, und Ihre Benutzer sehen weiterhin Inkompatibilitätsmeldungen für bestimmte Websites in Internet Explorer. Wenn das BHO bereits installiert ist, wird es beim nächsten Update des stabilen Microsoft Edge-Kanals deinstalliert.
- Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, wird das BHO installiert. Hierbei handelt es sich um das standardmäßige Verhalten.

Zusätzlich zur Notwendigkeit des BHO gibt es eine Abhängigkeit bei **RedirectSitesFromInternetExplorerRedirectMode**, was auf „Websites basierend auf der Websiteliste inkompatibler Websites umleiten“ oder „Nicht konfiguriert“ festgelegt sein muss.

### Richtlinie: RedirectSitesFromInternetExplorerRedirectMode

 Diese Richtlinie entspricht der Microsoft Edge-**Standardbrowser**-Einstellung „Internet Explorer kann Websites in Microsoft Edge öffnen". Sie können auf diese Einstellung zugreifen, indem Sie zur URL *edge://settings/defaultbrowser* wechseln.  

- Wenn Sie diese Richtlinie nicht konfigurieren oder auf „Websiteliste“ festlegen, leitet Internet Explorer inkompatible Websites zu Microsoft Edge um. Hierbei handelt es sich um das standardmäßige Verhalten.
- Wenn Sie diese Richtlinie deaktivieren möchten, wählen Sie **Aktiviert** UND dann in der Dropdownliste unter “Optionen: Inkompatible Websites von Internet Explorer zu Microsoft Edge umleiten” **Deaktivieren** aus. In diesem Zustand werden inkompatible Websites nicht zu Microsoft Edge umgeleitet.

> [!NOTE]
> Wenn Sie ein persönliches Gerät verwenden, das nicht von Ihrem Unternehmen verwaltet wird, wird unter **Internet Explorer-Kompatibilität** die Einstellung „Zulassen, dass Websites im Internet Explorer-Modus geladen werden“ angezeigt.
>
>Wenn Sie ein in die Domäne eingebundenes Gerät oder ein beim Mobile Device Management (MDM) registriertes Gerät verwenden, wird diese Option nicht angezeigt.
>
> Wenn Sie Ihren Benutzern stattdessen das Laden von Websites im Internet Explorer-Modus gestatten möchten, können Sie dies tun, indem Sie die Richtlinie [Internet Explorer-Modustest](https://docs.microsoft.com/deployedge/microsoft-edge-policies#allow-internet-explorer-mode-testing) konfigurieren.

### Richtlinie: HideInternetExplorerRedirectUXForIncompatibleSitesEnabled

Diese Richtlinie konfiguriert die Benutzererfahrung bei der Umleitung bei inkompatiblen Websites zu Microsoft Edge.  

- Wenn Sie diese Richtlinie aktivieren, wird den Benutzern nie das einmalige Umleitungsdialogfeld und das Umleitungsbanner angezeigt. Es werden keine Browserdaten oder Benutzereinstellungen importiert.
- Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, wird das Umleitungsdialogfeld bei der ersten Umleitung angezeigt, und das beständige Umleitungsbanner wird für Sitzungen angezeigt, die mit einer Umleitung beginnen.

  > [!NOTE]
  > Benutzer-Browserdaten werden jedes Mal importiert, wenn ein Benutzer neu umgeleitet wird. Dies geschieht jedoch nur, wenn der Benutzer dem Import im einmaligen Umleitungsdialogfeld zugestimmt hat.

## Deaktivieren der Umleitung zu Microsoft Edge

Wenn Sie die Umleitung VOR dem Update auf die stabile Microsoft Edge-Version 87 deaktivieren möchten, führen Sie die folgenden Schritte aus:

1. Legen Sie die Richtlinie **RedirectSitesFromInternetExplorerPreventBHOInstall** auf **Aktiviert** fest.

Wenn Sie die Umleitung NACH dem Update auf die stabile Microsoft Edge-Version 87 deaktivieren möchten, führen Sie die folgenden Schritte aus:

1. Legen Sie die Richtlinie **RedirectSitesFromInternetExplorerRedirectMode** auf **Aktiviert** fest, und wählen Sie dann in der Dropdownliste unter “Optionen: Inkompatible Websites von Internet Explorer zu Microsoft Edge umleiten” **Deaktivieren** aus. Diese Einstellung beendet die Umleitung, sobald die Richtlinie wirksam wird.
2. Legen Sie die Richtlinie **RedirectSitesFromInternetExplorerPreventBHOInstall** auf **Aktiviert** fest. Damit wird das BHO nach dem nächsten Microsoft Edge-Update deinstalliert.

## Weitere Informationen

- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)
- [Microsoft Edge-Richtlinien](https://docs.microsoft.com/deployedge/microsoft-edge-policies)
