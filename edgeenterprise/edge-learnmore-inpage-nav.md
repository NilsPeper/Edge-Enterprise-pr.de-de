---
title: Seiteninterne Navigation im Internet Explorer-Modus beibehalten
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Seiteninterne Navigation im Internet Explorer-Modus beibehalten
ms.openlocfilehash: 20b18d121c3babfaacffd4a08316b25be714d95e
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "11641361"
---
# <a name="keep-in-page-navigation-in-internet-explorer-mode"></a>Seiteninterne Navigation im Internet Explorer-Modus beibehalten

Sie können diese Richtlinie als vorübergehende Lösung verwenden, um zu erzwingen, dass alle seiteninternen Navigationen von Websites im Internet Explorer-Modus (IE-Modus) im IE-Modus verbleiben.

Eine seiteninterne Navigation wird über einen Link, ein Skript oder ein Formular auf der aktuellen Seite gestartet. Es kann sich auch um eine serverseitige Umleitung eines früheren Versuchs der seiteninternen Navigation handeln. Umgekehrt kann ein Benutzer eine nicht seiteninterne Navigation, die von der aktuellen Seite unabhängig ist, auf verschiedene Weise mithilfe der Browsersteuerelemente starten. Zum Beispiel über die Adressleiste, die Zurück-Schaltfläche oder einen Favoritenlink.

>[!NOTE]
>Dieser Artikel bezieht sich auf Microsoft Edge Version81 oder höher.

## <a name="prerequisites"></a>Voraussetzungen

Die folgenden Windows-Updates sind für diese Richtlinie erforderlich:

- Windows 10 Version 1909 & 1903, Windows Server Version 1909 & 1903 ([KB4532695](https://support.microsoft.com/help/4532695))
- Windows 10 Version 1809, Windows Server Version 1809, Windows Server 2019 ([KB4534321](https://support.microsoft.com/help/4534321))
- Windows 10 Version 1803 ([KB4534308](https://support.microsoft.com/help/4534308))
- Windows 10 Version 1709 ([KB4534318](https://support.microsoft.com/help/4534318))


## <a name="about-this-policy"></a>Informationen zu dieser Richtlinie

Diese Richtlinie gibt Ihnen Zeit, alle Authentifizierungsserver, die von Ihren Websites im IE-Modus verwendet werden, zu identifizieren und zu konfigurieren. Diese Richtlinie kann jedoch zu einer inkonsistenten Browsererfahrung führen, weil einige Websites im IE-Modus und zu anderen Zeiten im Microsoft Edge-Modus gerendert werden. Diese Erfahrung hängt davon ab, ob die Navigation zur Website von einer Seite im IE-Modus aus begann. Jede Website, die nicht ausdrücklich so konfiguriert ist, dass sie in einer bestimmten Rendering-Engine geöffnet wird, unterliegt dieser Inkonsistenz.

Wenn Sie diese Richtlinie aktivieren, empfehlen wir Ihnen, sie zu deaktivieren, nachdem Sie alle Authentifizierungsserver identifiziert und der Websiteliste als neutral hinzugefügt haben. Diese Aktion stellt sicher, dass Ihre modernen Websites niemals versehentlich im IE-Modus gerendert werden.

## <a name="keep-in-page-navigation-in-ie-mode"></a>Beibehaltung der seiteninternen Navigation im IE-Modus

Um automatische oder alle seiteninternen Navigationen im Internet Explorer-Modus beizubehalten, folgen Sie diesen Schritten:

1. Öffnen Sie den lokalen Gruppenrichtlinien-Editor.
2. Klicken Sie auf **Computerkonfiguration** > **Administrative Vorlagen** > **Microsoft Edge**.
3. Doppelklicken Sie unter **Einstellung** auf **Angeben, wie sich "seiteninterne" Navigationen zu nicht konfigurierten Websites verhalten, wenn sie von Seiten im Internet Explorer-Modus gestartet werden**.

   ![Seiteninterne Richtlinieneinstellung](media/edge-learnmore-inpage-nav/learnmore-in-page-nav-settings.png)

4. Wählen Sie **Aktiviert** aus. 

   ![Seiteninterne Richtlinie aktivieren](media/edge-learnmore-inpage-nav/learnmore-in-page-nav-enable.png)

5. Wählen Sie eine der folgenden Optionen aus der Dropdownliste aus:

   - **Standard **: Nur Websites, die zum Öffnen im Internet Explorer-Modus konfiguriert sind, werden in diesem Modus geöffnet. Alle Websites, die nicht zum Öffnen im Internet Explorer-Modus konfiguriert sind, werden zurück zu Microsoft Edge umgeleitet.
   - **Nur automatische Navigationen im Internet Explorer-Modus beibehalten**: Verwenden Sie diese Option, wenn die Standardeinstellung verwendet werden soll, mit der Ausnahme, dass alle automatischen Navigationen (wie z.B. 302-Umleitungen) zu nicht konfigurierten Websites im Internet Explorer-Modus bleiben.
   - **Beibehalten der gesamten seiteninternen Navigation im Internet Explorer-Modus**  * *_(Am wenigsten empfohlen)_*_ – Alle Navigationen von Seiten, die im IE-Modus zu nicht konfigurierten Websites geladen wurden, werden im Internet Explorer-Modus beibehalten.

6. Klicken Sie auf _*OK** oder **übernehmen,** um die Richtlinieneinstellungen zu speichern.

## <a name="see-also"></a>Siehe auch

- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)
