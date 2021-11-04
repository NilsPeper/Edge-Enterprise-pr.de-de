---
title: Moderner Sicherheitsschutz für anfällige Legacy-Apps
ms.author: gennlu
author: dan-wesley
manager: kawong
ms.date: 10/26/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Erfahren Sie, wie Microsoft Edge mit dem IE-Modus modernen Sicherheitsschutz für anfällige ältere Apps bietet.
ms.openlocfilehash: 9a0a4b896d9077a04f980340e3b12f3ad18e0b1a
ms.sourcegitcommit: 42f01cad0bf15224222b2aeadb48f03d46c35723
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2021
ms.locfileid: "12154506"
---
# <a name="modern-security-protection-for-vulnerable-legacy-apps"></a>Moderner Sicherheitsschutz für anfällige Legacy-Apps

Mit der Entwicklung des Internets in den letzten 20 Jahren haben sich auch die Bedürfnisse und Erwartungen der Benutzer an die von ihnen verwendeten Browser entwickelt. Heutzutage ist das Internet für viele Unternehmen von grundlegender Bedeutung, und ein moderner Browser, der entwickelt wurde, um die Geschäftsanforderungen sicher zu erfüllen, ist von entscheidender Bedeutung. Microsoft Edge ist ein moderner Browser, der für den sicheren Zugriff auf das moderne Web entwickelt wurde. In diesem Artikel wird gezeigt, wie der Internet Explorer -Modus (IE) in Microsoft Edge sicherer als Internet Explorer ist.

## <a name="introduction"></a>Einführung

Die interne Telemetrie von Microsoft zeigt, dass der Browser die Nr.1-Desktop-App ist. Die Zentralität des Browsers als alltägliches Produktivitätswerkzeug bedeutet, dass der Browser eine große Oberfläche darstellt, die Angriffen aus dem Internet ausgesetzt ist. Da das Internet und seine Anwendungen komplexer geworden sind, sind auch die Sicherheitsbedrohungen entsprechend komplexer geworden. Im Laufe der Jahre hat sich die Bedrohungslandschaft weiterentwickelt und anspruchsvolle Bedrohungsakteure angezogen, einschließlich, aber nicht beschränkt auf Nationalstaaten und organisierte kriminelle Gruppen, die durch Phishing, Ransomware usw. profitieren wollen.

Obwohl es sich mit Iterationen bis zu IE11 weiterentwickelt und weiterentwickelt hat, basiert IE immer noch auf einer Technologie, die 25 Jahre alt ist. Es handelt sich um einen älteren Browser, der architektonisch veraltet ist und nicht in der Lage ist, die Sicherheitsherausforderungen des modernen Webs zu bewältigen.

Um die Netzwerke einer Organisation vor den heutigen komplexen Bedrohungen zu schützen, versuchen IT-Administratoren, die Benutzer mithilfe eines modernen Browsers zu schützen. Dadurch wird sichergestellt, dass sie durch moderne Sicherheitsfeatures geschützt sind, meist oder immer während des Browsens.
Die heute übliche Praxis, einen modernen Browser und den IE-Browser zu verwenden, ist eine bequeme Problemumgehung, aber ineffektiv. Benutzer, die den IE-Browser für eine Aktivität verwenden, können IE leicht für alle Aktivitäten verwenden, was den Schutz, den ein moderner Browser bietet, zunichte macht.

Microsoft Edge ist einzigartig positioniert, um aktuelle Sicherheit zu bieten, sodass Benutzer die Vorteile moderner Sicherheitstechnologie so weit wie möglich nutzen können.

## <a name="reduce-threat-surface-area"></a>Reduzierung der möglichen Angriffsfläche für Bedrohungen

Wir sind uns bewusst, dass die Modernisierung Aller Ihrer älteren Websites auf einmal möglicherweise nicht machbar ist. Mit Microsoft Edge und dem IE-Modus können Sie einen sicheren modernen Browser verwenden, um auf Ihre älteren Websites zuzugreifen, bevor Sie sie modernisieren. Microsoft Edge mit dem IE-Modus verwendet ein einzigartiges duales Modulsystem, mit dem Sie Websites mit dem IE-Modul oder mit dem neuen modernen Modul öffnen können. Das Browser-Modul wird von der Website bestimmt, die Sie besuchen. Da das ältere IE-Modul weniger sicher ist, sollten Sie die Verwendung des älteren Moduls auf Websites beschränken, denen Sie vertrauen. Vertrauenswürdige Websites sind Websites, die Sie besitzen, kontrollieren oder von denen Sie wissen, dass sie frei von Sicherheitslücken sind. Als bewährte Methode sollten Sie nur mit dem modernen Browser-Modul auf nicht vertrauenswürdige Websites zugreifen, da dieses sicherer sind.

Der IE-Modus wurde entwickelt, um den Zugriff auf nicht vertrauenswürdige Websites zu verwalten. Der IE-Modus verwendet eine „Zulassungsliste“, in der Sie die vertrauenswürdigen Websites identifizieren, die das ältere Modul verwenden können. Jede Website, die nicht in der Liste enthalten ist, wird automatisch mithilfe des modernen Moduls für die sicherste Browsererfahrung geöffnet. Nicht vertrauenswürdige Inhalte aus nicht vertrauenswürdigen Quellen werden immer vom modernen Modul verarbeitet. Im IE-Modus steuern Sie, welche Websites mithilfe des älteren Moduls gerendert werden. Wenn Sie zu einer anderen Website navigieren, wechselt Microsoft Edge automatisch zurück zum modernen Modul. Infolgedessen muss sich eine Organisation nicht auf das Benutzerverhalten und die Praktiken verlassen, um sich selbst zu regulieren und zu entscheiden, welchen Browser verwendet werden soll. Aus Sicht der Benutzer ist es eine flüssige Erfahrung. Sie müssen nicht überlegen, welchen „richtigen“ Browser sie verwenden sollen, da Microsoft Edge die Website, auf die sie zugreifen möchten, nahtlos öffnet, unabhängig davon, ob es sich um eine ältere Website oder eine moderne Website handelt.

Der IE-Modus ist sicherer als der IE, da Symbolleisten nicht unterstützt werden, wodurch die Angriffsfläche reduziert wird. Symbolleisten sind bewährte Vektoren für Schadsoftware und Phishing-Angriffe. Darüber hinaus wird die IE-Desktop-App nach der Einstellung deaktiviert, wodurch die Benutzer keine Zeit mehr mit einem veralteten Browser haben. Benutzer können auf vertrauenswürdige ältere Apps und Websites zugreifen, die in einer Zulassungsliste für den IE-Modus in Microsoft Edge identifiziert sind.

Der Benutzer befindet sich in einer modernen Umgebung, ohne sein Verhalten anpassen zu müssen, aber auch ohne den Zugriff auf unternehmenskritische ältere Apps und Websites zu verlieren. Microsoft Edge ist der einzige Browser, mit dem Benutzer mit einem einzigen Browser auf ältere und moderne Websites zugreifen können.  

Im nächsten Abschnitt wird erläutert, warum es wichtig ist, die Zeit zu minimieren, die Benutzer mit dem älteren Browser-Modul verbringen.

## <a name="minimize-legacy-browser-use"></a>Minimieren der Nutzung des älteren Browsers

In den folgenden Abschnitten werden die Gründe erläutert, warum es wichtig ist, die Verwendung älterer Browser-Module zu minimieren.

### <a name="architectural-deficiency"></a>Architekturdefizite

Architekturdefizite im IE rühren daher, dass seine ursprüngliche Architektur nicht die Komplexität des modernen Webs oder der modernen Bedrohungslandschaft berücksichtigte. IE entwickelte sich aus einer einzigen Prozessarchitektur, die zu unzureichendem Sandboxing und einer vergleichsweise breiten Angriffsfläche führte. Moderne Browser wie Microsoft Edge basieren auf einem Bedrohungsmodell, das auf der aktuellen Bedrohungslandschaft basiert. Diese Browser enthalten Sicherheitsfortschritte wie Standortisolation und hardwarebasierte Sicherheitsfeatures. Zum Beispiel: Intels Control Flow Enforcement Technology (CET), die viele moderne Sicherheitsbedrohungen bewältigt. Diese Sicherheitsminderungen sind in IE NICHT verfügbar, was ihn zu einem einfachen Ziel selbst für einfache Angriffe macht.

### <a name="ease-of-exploitation"></a>Erleichterte Ausnutzung

IE ist aufgrund seiner Architektur und fehlender Unterstützung für moderne Sicherheitsfeatures leichter auszunutzen als Microsoft Edge. Es ist einfacher, eine einzelne Schwachstelle in IE zu finden, die zu einer Remotecodeausführung (Remote Code Execution, RCE) führen könnte, als eine ähnliche Schwachstelle in Microsoft Edge zu finden, bei der mehrere Sicherheitsanfälligkeiten miteinander verkettet werden müssen, um ein ähnliches Ergebnis zu erzielen. Darüber hinaus sind ActiveX- und Browser-Hilfsobjekte zu Schwachstellen geworden, und die Unterstützung von IE für sie macht es noch einfacher, den Browser auszunutzen.  

### <a name="speed-of-security-patching"></a>Geschwindigkeit des Sicherheitspatches

Browser sind eine der am häufigsten verwendeten Anwendungen auf dem Desktop, die zum routinemäßigen Herunterladen und Verarbeiten nicht vertrauenswürdiger Inhalte aus nicht vertrauenswürdigen Quellen verwendet wird. Um Sicherheitsbedrohungen immer einen Schritt voraus zu sein, können moderne Browser sicherheitsrelevante Updates schnell bereitstellen. Da IE an das Windows Betriebssystem gebunden ist, sind die Geschwindigkeiten von Sicherheitsupdates begrenzt und führen dazu, dass IE für längere Zeit anfällig bleibt. Im Gegensatz zu IE verfügt Microsoft Edge über einen integrierten Updater mit einer wesentlich schnelleren Updatefrequenz, wodurch die Reaktionszeit auf Tage und nicht auf Wochen oder Monate reduziert wird.

### <a name="security-researcher-ecosystem"></a>Ökosystem für Sicherheitsforscher

Die Verbesserung der realen Browsersicherheit hängt stark von einem breiten Ökosystem externer Sicherheitsforscher ab, die durch Bounty-Programme angeregt werden, neue Schwachstellen und Exploits zu finden. Internet Explorer unterstützt kein Bounty-Programm, was den Umfang seiner Sicherheitsverbesserungen einschränkt. Im Vergleich dazu verfügt Microsoft Edge über ein vollwertiges Bounty-Programm und ein internes Schwachstellenforschungsteam, um die moderne Browsersicherheit zu fördern. Da Microsoft Edge auf Chromium Open Source basiert, profitiert es auch vom Browser-Sicherheitsökosystem von Chromium.

### <a name="phishing-protection-using-smartscreen"></a>Phishing-Schutz mit SmartScreen

SmartScreen, die Phishing-Schutztechnologie von Microsoft, blockiert laut einer unabhängigen Studie von [CyberRatings.org](https://www.cyberratings.org/) mehr Phishing-Versuche <sup>1</sup> und Schadsoftware <sup> 2 </sup> als Google Chrome‘s Safe Browsing.

> [!NOTE]
> <sup>1 </sup> Webbrowser im Vergleich zu. Phishing, Vergleichstestbericht (Juli 2021), CyberRatings.org<br>
> <sup>2 </sup> Webbrowser im Vergleich zu Schadsoftware, Vergleichstestbericht (Juli 2021), CyberRatings.org

Microsoft Edge bietet vollständige systemeigene Unterstützung für SmartScreen, IE wird jedoch aufgrund seiner veralteten Architektur nur teilweise unterstützt.

Zusätzlich zur Bereitstellung von Sicherheitsfortschritten, die modernen Sicherheitspraktiken entsprechen, ist Microsoft Edge für Unternehmen unter Windows 10 sicherer als Chrome. Microsoft Edge wurde auch entwickelt, um die Sicherheitsfeatures, Funktionen und Tools zu nutzen, die in der Microsoft 365-Suite und Windows 10 verfügbar sind. Dieses Produktökosystem reduziert die Komplexität von Sicherheit und Datenschutz für das IT-Team. Beispielsweise können Investitionen und Entscheidungen, die in Microsoft 365 für die Identität getroffen werden, problemlos auf Microsoft Edge angewendet werden.

Der IE-Modus auf Microsoft Edge ist eine einzigartige Lösung, die sicherstellt, dass Benutzer auf geschäftskritische ältere IE-Websites zugreifen können und gleichzeitig vor modernen Bedrohungen geschützt bleiben.

## <a name="see-also"></a>Weitere Informationen

- [Informationen zum IE-Modus](./edge-ie-mode.md)
- [Weitere Informationen zum Unternehmensmodus](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [Sicherheit für Ihr Unternehmen](./ms-edge-security-for-business.md)
- [Microsoft Edge Enterprise-Startseite](https://aka.ms/EdgeEnterprise)