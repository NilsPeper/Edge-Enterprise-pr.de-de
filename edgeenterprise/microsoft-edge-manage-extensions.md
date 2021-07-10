---
title: Verwalten von Microsoft Edge-Erweiterungen im Unternehmen
ms.author: aspoddar
author: AndreaLBarr
manager: balajek
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Verwalten von Microsoft Edge-Erweiterungen im Unternehmen
ms.openlocfilehash: 26134a8c352354c0c447518120f3d79332100c80
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "11642921"
---
# <a name="manage-microsoft-edge-extensions-in-the-enterprise"></a>Verwalten von Microsoft Edge-Erweiterungen im Unternehmen

Dieser Artikel enthält Leitlinien für bewährte Methoden für Administratoren, die Microsoft Edge-Erweiterungen in ihren Organisationen verwalten. Anhand der Informationen in diesem Artikel können Sie eine Strategie für die Verwaltung von Erweiterungen in Ihrer Organisation entwickeln.

> [!NOTE]
> Dieser Artikel bezieht sich auf Microsoft Edge Version 77 oder höher.

## <a name="introduction"></a>Einführung

Organisationen möchten Unternehmens- und Benutzerdaten schützen und Browsererweiterungen auswerten, um sicherzustellen, dass sie sicher und für ihr Unternehmen relevant sind. Administratoren möchten:

- Verhindern, dass ungültige Apps und Erweiterungen installiert werden.
- Erweiterungen beibehalten, die Benutzer für ihre Arbeit benötigen.
- Den Zugriff auf Benutzer- und Unternehmensdaten verwalten.  

Dieser Artikel ist der erste in einer Reihe, die Administratoren bei der Verwaltung von Erweiterungen hilft, um ihren Benutzern eine sichere und produktive Erfahrung zu bieten. Diese Reihe führt Sie durch die verschiedenen Optionen und hilft Ihnen die beste Methode auszuwählen, um Erweiterungen zu verwalten. Die Reihe umfasst die folgenden Artikel:

- [Verwalten von Microsoft Edge Erweiterungen im Unternehmen](microsoft-edge-manage-extensions.md). Erstellen Sie eine Strategie zum Verwalten von Erweiterungen und zum Einrichten administrativer Vorlagen, die für die Verwaltung des Browsers erforderlich sind.
- [Verwenden von Gruppenrichtlinien, um Microsoft Edge-Erweiterungen zu verwalten](microsoft-edge-manage-extensions-policies.md). Optionen, die Gruppenrichtlinien verwenden, um Erweiterungen zu verwalten.
- [Erstellen eines Webspeichers, um Microsoft Edge-Erweiterungen zu hosten](microsoft-edge-manage-extensions-webstore.md). Erstellen und Hosten von Erweiterungen.
- [Häufig gestellte Fragen (FAQ) zu Microsoft Edge-Erweiterungen](microsoft-edge-manage-extensions-faq.md). Häufig gestellte Fragen.

## <a name="things-to-consider-when-managing-extensions"></a>Aspekte, die beim Verwalten von Erweiterungen zu berücksichtigen sind

Ihre Benutzer benötigen Zugriff auf bestimmte Apps, Websites und Erweiterungen, um ihre Aufgaben zu erledigen und gleichzeitig Benutzer- und Unternehmensdaten zu schützen. Eine effektive Sicherheitsstrategie umfasst das Stellen der richtigen Fragen für Ihr Unternehmen und die Frage, wie Erweiterungen den Anforderungen Ihres Unternehmens entsprechen können. Einige der wichtigsten Fragen, die Sie stellen müssen, sind:

- Welche Vorschriften und Compliance-Maßnahmen müssen eingehalten werden?
- Fordern einige Erweiterungen übermäßig umfassende Berechtigungen an, die gegen die Datensicherheitsrichtlinien des Unternehmens verstoßen könnten?
- Wie viele Benutzer- oder Unternehmensdaten werden auf den Benutzergeräten gespeichert?

Während Sie diese Fragen beantworten, können Sie die präzisen Richtlinien verwenden, die Microsoft Edge bereitstellt, um:

- Erweiterungen auf den Computern der Benutzer basierend auf Ihren Datenschutzrichtlinien zu blockieren oder zuzulassen.
- die Installation von Erweiterungen auf den Benutzergeräten zu erzwingen, damit sie über Tools verfügen, die sie benötigen, um produktiv zu sein.
- Zulassungslisten- oder Blocklistenerweiterungen nur die Rechte zu gewähren, die Ihre Benutzer für ihre Arbeit benötigen.

Das herkömmliche Modell für die Verwaltung von Erweiterungen verwendet den Ansatz der „Zulassungsliste“ und „Blockliste“ für bestimmte Erweiterungen. Mit Microsoft Edge können Sie jedoch auch die von Erweiterungen angeforderten Berechtigungen verwalten. Mit diesem Modell können Sie entscheiden, welche Rechte und Berechtigungen für Erweiterungen auf Ihren Computern und Geräten zugelassen werden sollen. Anschließend kann eine globale Richtlinie implementiert werden, die Erweiterungen basierend auf Ihren Anforderungen zulässt oder blockiert.  

## <a name="understand-extension-permissions"></a>Grundlegendes zu Erweiterungsberechtigungen

Erweiterungen können Rechte anfordern, um Änderungen auf Geräten oder Webseiten vorzunehmen, damit diese ordnungsgemäß ausgeführt werden können. Diese Rechte werden Berechtigungen genannt. Entwickler müssen auflisten, welche Rechte und Zugriffe ihre Erweiterungen benötigen. Es gibt zwei Hauptkategorien für Berechtigungen, und viele Erweiterungen benötigen beide der folgenden Berechtigungen:

- Hostberechtigungen erfordern, dass die Erweiterung Webseiten auflistet, die sie anzeigen oder ändern kann.
- Geräteberechtigungen sind die Rechte, die von einer Erweiterung auf dem Gerät benötigt werden, auf dem sie ausgeführt wird.

Beispiele für diese Berechtigungen sind: Zugriff auf einen USB-Anschluss, auf den Speicher oder den Anzeigebildschirm sowie Kommunikation mit nativen Programmen.  

## <a name="get-ready-to-manage-extensions"></a>Lernen Sie, wie Erweiterungen verwaltet werden

## <a name="before-you-begin"></a>Bevor Sie beginnen

Bei den Erweiterungsoptionen wird davon ausgegangen, dass Sie Microsoft Edge bereits für Ihre Benutzer verwaltet haben. Weitere Informationen darüber, wie administrative Vorlagen für Microsoft Edge-Richtlinien eingerichtet werden, finden Sie unter:

-   [Microsoft Edge-Richtlinieneinstellungen unter Windows konfigurieren](/DeployEdge/configure-microsoft-edge)
-   [Konfigurieren für Windows mit Intune](/mem/intune/configuration/administrative-templates-configure-edge?bc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2ftoc.json)
-   [Konfigurieren für Windows mit mobiler Geräteverwaltung](/deployedge/configure-edge-with-mdm)
-   [Konfigurieren für macOS mithilfe einer .plist](/deployedge/configure-microsoft-edge-on-mac)
-   [Konfigurieren für macOS mit Jamf](/deployedge/configure-microsoft-edge-on-mac-jamf)

Die Konfigurationsschritte in diesem Artikel gelten für Windows. Informationen für die entsprechende Implementierung unter MAC/Linux finden Sie in der Microsoft Edge-Browserrichtlinienreferenz.

## <a name="decide-which-extensions-to-allow"></a>Entscheiden, welche Erweiterungen zugelassen werden sollen

Die meisten Organisationen sollten Erweiterungen anhand ihrer Berechtigungen und der Websites, auf die sie Zugriff haben, verwalten. Diese Methode ist sicherer, einfacher zu verwalten und für große Organisationen skalierbar.  

- Blockierte/zulässige Berechtigungen – Ermöglichen Ihnen, Erweiterungen anhand der benötigten Berechtigungen zu steuern.
- Laufzeitblockhosts – Ermöglichen Ihnen zu steuern, auf welche Websites diese Erweiterungen zugreifen können.

Diese Vorgehensweise spart Zeit, da Sie diese nur einmal festlegen müssen. Und mit der Laufzeithostrichtlinie werden Ihre wichtigsten Websites geschützt. Es gibt auch andere Optionen, z. B.:

-   Installation von Erweiterungen erzwingen – Ermöglicht die automatische Installation von Erweiterungen.
-   Zulassungsliste/Blockliste (falls erforderlich) – Entscheiden Sie, welche Erweiterungen installiert werden dürfen.

Verwenden Sie die folgenden Schritte als Leitfaden, um zu entscheiden, welche Erweiterungen in Ihrer Organisation zugelassen werden können.

1. Erstellen Sie eine Liste der Erweiterungen, die Mitarbeiter auf ihren Computern benötigen. Testen Sie die Erweiterungen in einer Testumgebung, um Kompatibilitätsprobleme mit internen Apps zu diagnostizieren.
2. Wählen Sie aus, welche Websites sicherer sein müssen.

   - Erfahren Sie, welchen vertraulichen internen Websites oder Domänen Sie benötigen, um Erweiterungen daran zu hindern, Änderungen an Daten vorzunehmen oder Daten zu lesen.  
   - Verhindern Sie den Zugriff auf diese Websites, indem Sie die API-Aufrufe blockieren, wenn die Erweiterung ausgeführt wird. Dazu gehören das Blockieren von Webanforderungen, das Lesen von Cookies, JavaScript-Einfügung, XHR usw.

3. Bestimmen Sie, welche Berechtigungen erforderlich sind, um diese Erweiterungen auszuführen. Ermitteln Sie, welche Berechtigungen potenzielle Risiken für Ihre Benutzer darstellen.

   - Überwachen Sie die Erweiterungen, die Ihre Benutzer installiert haben, und sehen Sie, welche Berechtigungen diese benötigen. Sie können sich die JSON-Datei des Web-App-Manifests im Code der Erweiterung ansehen. Führen Sie die folgenden Schritte aus, um zu sehen, welche Rechte die Erweiterung benötigt:

     - Installieren Sie die Erweiterung von der [Microsoft Edge Add-ons-Website](https://microsoftedge.microsoft.com/addons/) oder aus dem [Chrome Web Store.](https://chrome.google.com/webstore)
     - Testen Sie die Erweiterung, und verstehen Sie, wie sie in Ihrer Organisation funktioniert.
     - Überprüfen Sie die Berechtigungen, die die Erweiterung benötigt, indem Sie zu *edge://extensions*navigieren. Die im nächsten Screenshot gezeigte Microsoft Office-Erweiterung fordert beispielsweise die Berechtigungen „Browserverlauf lesen“ und „Benachrichtigungen anzeigen“ an. Wägen Sie die Nützlichkeit dieser Erweiterung gegen die angeforderte Berechtigungsstufe ab. Nachdem Sie eine Erweiterung für Ihre Organisation genehmigt haben, verwalten Sie diese mit den folgenden Tools.
   :::image type="content" source="media/microsoft-edge-manage-extensions/manage-extesions-office-extension.png" alt-text="Microsoft Office-Erweiterung mit Berechtigungen.":::

   - Sie können auch Erweiterungen, die von Benutzern in Ihrer Organisation angefordert werden, überprüfen, bevor Sie diese in der Organisation genehmigen. Einige der Berechtigungen, die Erweiterungen verwenden, können vage sein. Bei unternehmenskritischen Apps können Sie sich direkt an den App-Entwickler oder -Anbieter wenden, um weitere Informationen über die Erweiterung zu erhalten oder sich den Quellcode anzusehen. Sie sollten in der Lage sein, die Änderungen, die die Erweiterung auf Geräten und Websites vornehmen kann, detailliert anzugeben.
   - Überprüfen Sie die Liste „Berechtigungen deklarieren“, die alle Berechtigungen auflistet, die eine Erweiterung verwenden kann. Mit dieser Liste können Sie entscheiden, welche Berechtigungen Sie in Ihrer Organisation zulassen möchten.

4. Erstellen Sie eine Masterliste anhand der von Ihnen gesammelten Daten. Diese Liste enthält die folgenden Informationen:

   - **Erforderliche Erweiterungen**. Diese Liste kann nach Abteilung, Bürostandort oder anderen relevanten Informationen organisiert werden.
   - **Zulassungsliste der Erweiterungen**. Erforderliche Erweiterungen mit Berechtigungen, die möglicherweise blockiert sind, aber ausgeführt werden dürfen. Diese Erweiterungen werden von Ihren Benutzern benötigt oder wurden durch Unterhaltungen mit dem Anbieter als risikolos eingestuft.
   - **Blockliste der Erweiterung**. Erweiterungen, die für die Installation blockiert sind. Die Erweiterungen in dieser Liste verfügen über Berechtigungen, die nicht ausgeführt werden dürfen. Führen Sie auch die zentralen Websites und Domänen auf, die sicher bleiben sollen und auf keine Erweiterungen zugreifen dürfen. Sie können diese Blockliste später mit anderen vergleichen, die Sie bereits erstellt haben. Möglicherweise stellen Sie fest, dass Sie Ihre aktuellen Blocklistenrichtlinien lockern können.

5. Präsentieren Sie Ihre Liste den Projektbeteiligten und dem IT-Team, um deren Zustimmung zu erhalten.
6. Testen Sie die neue Richtlinie in Ihrem Labor oder mit einem kleinen Pilotversuch in Ihrer Organisation.
7. Führen Sie diese neuen Richtliniensätze für Mitarbeiter phasenweise ein. Weitere Informationen finden Sie unter [Verwenden von Gruppenrichtlinien zum Verwalten von Microsoft Edge-Erweiterungen.](microsoft-edge-manage-extensions-policies.md)
8. Überprüfen Sie das Feedback Ihrer Benutzer.
9. Wiederholen und optimieren Sie den Prozess monatlich, vierteljährlich oder jährlich.

Wenn Sie die Grundlienie der zulässigen Berechtigungen durchsetzen und vertrauliche Unternehmenswebsites schützen, können Sie Ihrem Unternehmen mehr Sicherheit und ihren Benutzer gleichzeitig mehr Benutzerfreundlichkeit bieten. Mitarbeiter installieren möglicherweise Erweiterungen, die sie zuvor nicht installieren konnten, führen sie jedoch nicht auf vertraulichen Businesswebsites aus.  

## <a name="see-also"></a>Siehe auch

- [Verwenden von Gruppenrichtlinien zum Verwalten von Microsoft Edge-Erweiterungen](microsoft-edge-manage-extensions-policies.md)
- [Erstellen eines Webspeichers zum Hosten von Microsoft Edge-Erweiterungen](microsoft-edge-manage-extensions-webstore.md)
- [Referenzhandbuch für die „ExtensionSettings“-Richtlinie](microsoft-edge-manage-extensions-ref-guide.md)
- [Häufig gestellte Fragen (FAQ) zu Microsoft Edge-Erweiterungen](microsoft-edge-manage-extensions-faq.md)
- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)