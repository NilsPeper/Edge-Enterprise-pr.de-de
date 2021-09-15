---
title: Planen Ihrer Bereitstellung von Microsoft Edge
ms.author: collw
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Planen Ihrer Bereitstellung von Microsoft Edge
ms.openlocfilehash: be85aa5182bbee51f90fe42e80cdee0b9c793b4e
ms.sourcegitcommit: 8968f3107291935ed9adc84bba348d5f187eadae
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/12/2021
ms.locfileid: "11979135"
---
# <a name="plan-your-deployment-of-microsoft-edge"></a>Planen Ihrer Bereitstellung von Microsoft Edge

In diesem Artikel werden die empfohlenen Vorgehensweisen für die Bereitstellung von Microsoft Edge in einer Unternehmensumgebung beschrieben.

>[!NOTE]
>Dieser Artikel bezieht sich auf Microsoft Edge Version 77 oder höher.

Die folgenden Abschnitte enthalten spezifische Anleitungen für die Planung Ihrer Microsoft Edge-Bereitstellung.

- [Auswerten der Browserumgebung und -anforderungen](#evaluate-your-existing-browser-environment-and-browser-needs)
- [Sicherstellen, dass Windows 10-Geräte bereit sind](#make-sure-your-windows-10-devices-are-ready)
- [Auswählen der Bereitstellungsmethode](#determine-your-deployment-methodology)
- [Site-Discovery](#do-site-discovery)
- [Auswählen der Kanalstrategie](#determine-your-channel-strategy)
- [Definieren und Konfigurieren von Richtlinien](#define-and-configure-policies)
- [Testen der App-Kompatibilität](#do-app-compatibility-testing)
- [Microsoft Edge-Pilotprojekt](#deploy-microsoft-edge-to-a-pilot-group)
- [Auswerten des Pilotprojekts](#validate-your-deployment)
- [Bereitstellen von Microsoft Edge im gesamten Unternehmen](#broad-deployment-of-microsoft-edge)

## <a name="evaluate-your-existing-browser-environment-and-browser-needs"></a>Bewerten der vorhandenen Browserumgebung und der Browseranforderungen

Nehmen Sie sich Zeit, um den aktuellen Browserstatus und das Ziel Ihres Projekts zu verstehen und sicherzustellen, dass alle Projektbeteiligten auf dem gleichen Stand sind und auf dasselbe Ergebnis hinarbeiten.

Definieren Sie zunächst den aktuellen Status:

- Welche Browser werden derzeit in Ihrer Umgebung bereitgestellt?
- Welcher Browser ist als Standardbrowser festgelegt?
- Müssen Sie Internet Explorer für einige Ihrer Anwendungen nutzen?
- Verwenden Sie derzeit eine Enterprise Mode-Siteliste zum Konfigurieren von Internet Explorer?
- Welche Betriebssystemplattformen werden in Ihrer Umgebung unterstützt? (Windows 10, macOS, Windows 7, Windows Server usw.)
- Welche Verwaltungstools verwenden Sie für die Browserverwaltung?
- Wer ist für die Browserkonfiguration und -verwaltung zuständig?
- Wie sieht Ihr Prozess zur Überprüfung der Browserkompatibilität aus?

Nachdem Sie den aktuellen Zustand erfasst haben, können Sie die gewünschten Ziele für Ihre Browserbereitstellung ermitteln. Berücksichtigen Sie dabei folgende Punkte:

- Möchten Sie [Microsoft Edge als Ihren Standardbrowser einrichten](./edge-default-browser.md)?
- Wie werden Sie [Microsoft Edge konfigurieren](./configure-microsoft-edge.md)?
- Welche Features sind wichtig und sollten im Rahmen der Erstbereitstellung konfiguriert werden?
- Wie sieht der Prozess für die Behandlung von erkannten Kompatibilitäts- oder Konfigurationsproblemen aus?

Sie sollten auch die **Voraussetzungen** für die Features kennen, die Sie interessieren, z. B.:

- [Windows Defender Application Guard](/windows/security/threat-protection/windows-defender-application-guard/reqs-wd-app-guard)
- [Internet Explorer-Modus](./edge-ie-mode.md)
- [Authentifizierung und Synchronisierung](./microsoft-edge-security-identity.md)

Wenn Sie diese Fragen beantwortet haben, sind Sie bereit, Ihre Microsoft Edge-Bereitstellung zu planen.
<!--bookmark -->

## <a name="make-sure-your-windows-10-devices-are-ready"></a>Stellen Sie sicher, dass Ihre Windows 10-Geräte bereit sind

Für den Edge Stable-Kanal ist das neueste kumulative Update (Latest Cumulative Update, LCU) von Oktober 2019 (oder höher) erforderlich. Wenn Sie versuchen, die Installation auf einem Windows 10-Gerät mit einem älteren LCU durchzuführen, schlägt die Installation fehl. Weitere Details zum minimalen LCU, die vor der Bereitstellung von Edge angewendet werden müssen, finden Sie unter [Windows-Updates zur Unterstützung der nächsten Version von Microsoft Edge](./microsoft-edge-sysupdate-windows-updates.md).

## <a name="determine-your-deployment-methodology"></a>Ermitteln der Bereitstellungsmethode

Wenn Sie den gewünschten Endzustand kennen, können Sie mit der Planung beginnen. Die zwei wesentlichen Möglichkeiten für die Bereitstellung von Microsoft Edge sind die Bereitstellung nach Rolle und die Bereitstellung nach Site.

### <a name="deploy-to-end-users-by-role"></a>Bereitstellung für Endbenutzer nach Rolle

Wenn für Sie die Anwendungskompatibilität am wichtigsten ist, und Sie nicht genau wissen, welche Anwendungen getestet werden sollten, erwägen Sie die Bereitstellung für Endbenutzer nach Rolle. So stehen in jedem Abschnitt einer phasenweisen Bereitstellung Feedback und Einblicke zu Anwendungen zur Verfügung, deren Konfiguration möglicherweise geändert werden muss, um Kompatibilitätsprobleme zu beheben.

### <a name="deploy-to-end-users-by-site"></a>Bereitstellung für Endbenutzer nach Site

Wenn die Bandbreite Ihr Hauptanliegen darstellt, sollten Sie Anwendungskompatibilitätstests im Voraus durchführen. Nachdem Sie die Tests abgeschlossen haben, stellen Sie die Anwendungen für Endbenutzer nach Site bereit, damit Sie andere Optimierungen der Softwarebereitstellung puffern können.

## <a name="do-site-discovery"></a>Site-Discovery

Wenn Sie von älteren Webanwendungen abhängig sind und vorhaben, den Internet Explorer-Modus zu verwenden (was die meisten Kunden tun), müssen Sie wahrscheinlich eine zusätzliche Site-Discovery durchführen.

### <a name="if-youve-already-deployed-and-configured-the-legacy-version-of-microsoft-edge"></a>Wenn Sie die Vorgängerversion von Microsoft Edge bereits bereitgestellt und konfiguriert haben

Wenn Sie die Enterprise-Siteliste bereits so konfiguriert haben, dass sie für die Vorgängerversion von Microsoft Edge funktioniert, sind Sie fast schon fertig! Das einzige, was Sie hinzufügen müssen, sind neutrale Sites.

Neutrale Sites sind in der Regel Sites, die einmaliges Anmelden (Single Sign-On, SSO) bereitstellen. Wenn Sie von Microsoft Edge zu einer neutralen Site navigieren, möchten Sie vielleicht in Microsoft Edge bleiben, um sich zu authentifizieren. Wenn Sie im Internet Explorer-Modus zu einer neutralen Site navigieren, möchten Sie ggf. im Internet Explorer-Modus bleiben, um sich zu authentifizieren.

Identifizieren Sie alle SSO-Sites (oder andere neutrale Sites), die Sie verwenden, und fügen Sie diese Ihrer Enterprise-Siteliste hinzu.

### <a name="if-youve-configured-internet-explorer-as-your-default-browser"></a>Wenn Sie Internet Explorer als Standardbrowser konfiguriert haben

Wenn Sie aktuell nur Internet Explorer verwenden, wissen Sie möglicherweise nicht, welche Sites auf moderne Webstandards aktualisiert wurden und für welche weiterhin Internet Explorer erforderlich ist. Sie können diese Sites suchen und sie der Enterprise-Siteliste hinzufügen. So können Sie den Internet Explorer-Modus nur auf Sites verwenden, die ihn benötigen.

> [!TIP]
> Verwenden Sie die Tools von [Enterprise Site Discovery](/internet-explorer/ie11-deploy-guide/collect-data-using-enterprise-site-discovery), um die Sites zu ermitteln, die möglicherweise den Internet Explorer-Modus benötigen. Sie können Daten auf Computern, auf denen Windows Internet Explorer 8 bis 11 ausgeführt wird, unter Windows 10, Windows 8.1 oder Windows 7 sammeln.

### <a name="analyze-site-discovery-data"></a>Analysieren der durch Site-Discovery ermittelten Daten

Nachdem Sie die Sitedaten gesammelt haben, empfehlen wir den folgenden vierstufigen Prozess zum Analysieren der Daten:

1. Sortieren Sie die Daten nach Domäne und anschließend nach URL.
2. Definieren Sie die „Grenzen“ einer Anwendung zur Konfiguration für den Internet Explorer-Modus. Sie möchten alle Sites und Websteuerelemente einbeziehen, die die Anwendung definieren. Sie möchten aber keine zusätzlichen Sites und Steuerelemente einbeziehen, wenn Sie die Anwendung zu weitgefasst definieren. Einige Sites sind möglicherweise so einfach wie „http://contoso.com/app1“, während andere die Definition mehrerer Sites und Seiten erfordern.
3. Testen Sie die Anwendung, um sicherzustellen, dass Sie nicht nativ funktioniert. Viele Sites bieten moderne Inhalte, wenn sie einen modernen Browser erkennen, und nur ältere Inhalte, wenn sie Internet Explorer erkennen.
4. Fügen Sie die Anwendung Ihrer Enterprise-Siteliste hinzu, wenn sie die Tests nicht besteht.

   > [!NOTE]
   > Als bewährte Methode sollten Sie alle Sites gruppieren, aus denen eine Anwendung besteht. Wenn alle Sites zur Ausführung einer Aufgabe verwendet werden müssen und in der Regel zusammen aktualisiert werden, ist dies ein guter Hinweis darauf, dass sie gruppiert werden sollten. So ist es beim Upgrade einer Anwendung einfacher, die gesamte Site aus dem Internet Explorer-Modus zu entfernen und einen modernen Browser für diese Anwendung zu verwenden.

## <a name="determine-your-channel-strategy"></a>Festlegen Ihrer Kanalstrategie

Microsoft Edge wird in [mehreren Kanälen](./microsoft-edge-channels.md) veröffentlicht.

> [!NOTE]
> Sie können mehr als einen Kanal auf einem Gerät installieren.

Sie möchten auf den meisten Geräten den stabilen Kanal bereitstellen. Sie sollten sich jedoch eine Bereitstellungsstrategie überlegen, die mehrere Geräte und mehrere Kanäle umfasst.

### <a name="multiple-devices-and-channels"></a>Mehrere Geräte und Kanäle

Es wird empfohlen, eine repräsentative Teilmenge von Geräten für die Verwendung des Beta-Kanals zu konfigurieren. So können Sie bevorstehende Änderungen am Browser in einer Vorschau anzeigen. Sie können sehen, ob sich diese Änderungen auf Ihre Endbenutzer oder Anwendungen auswirken.

Möglicherweise möchten Sie auch den Dev-Kanal (oder sogar den Canary-Kanal) für einige Rollen, z. B. für Webentwickler, zur Verfügung stellen. Überlegen Sie, ob einige Geräte mit flüssigeren und sich schnell ändernden Kanälen anvisiert werden sollen, oder ob diese Kanäle für die Benutzer einfach zur Verfügung gestellt werden sollten, damit diese entscheiden können, sie zu installieren.

Da es möglich ist, auf einem Gerät mehrere Kanäle zu installieren, können Sie das Risiko von Tests für Benutzer reduzieren, die sich für die Installation eines Kanals in einer Vorabversion entschieden haben. Wenn Sie beispielsweise einen Benutzer haben, der den Beta-Kanal verwendet, und dann ein Problem auftritt, kann dieser zum stabilen Kanal wechseln und weiterarbeiten. Dadurch werden Blockierungen aufgehoben, bis das Problem behoben werden kann.

> [!NOTE]
> Wenn der Benutzer die Synchronisierung aktiviert hat, wird seine Konfiguration über mehrere Kanäle synchronisiert, was den Wechsel zwischen Kanälen noch einfacher macht.

## <a name="define-and-configure-policies"></a>Definieren und Konfigurieren von Richtlinien

Nach der Erstellung der Enterprise-Siteliste wird empfohlen, die Richtlinien zu ermitteln und zu konfigurieren, die Sie mit Microsoft Edge bereitstellen möchten. So wird sichergestellt, dass diese Richtlinien beim Ausführen der Tests angewendet werden.

Überlegen Sie zunächst, welche Erfahrung die Benutzer bei der ersten Ausführung haben sollen. Wenn Einstellungen automatisch aus dem aktuellen Browser importiert werden sollen, konfigurieren Sie die Richtlinie für [AutoImportAtFirstRun](./microsoft-edge-policies.md#autoimportatfirstrun).

Für Sicherheitsrichtlinien empfiehlt es sich, mit der Microsoft Edge-Sicherheitsbaseline zu beginnen. Die Sicherheitsbaseline kann mithilfe der [empfohlenen Sicherheitskonfigurationsbaseline-Einstellungen](https://techcommunity.microsoft.com/t5/Microsoft-Security-Baselines/Security-baseline-DRAFT-for-Chromium-based-Microsoft-Edge/ba-p/949991) oder mithilfe von [Microsoft Intune](/intune/protect/security-baseline-settings-edge) angewendet werden.

Für andere Richtlinien sollten Sie sich die Richtlinienkonfigurationen für [Microsoft Edge](./microsoft-edge-policies.md) und [Microsoft Edge Updates](./microsoft-edge-update-policies.md) anschauen.

### <a name="define-your-update-strategy-and-policies"></a>Definieren der Updatestrategie und -richtlinien

Sie können außerdem festlegen, wie Updates nach der Bereitstellung von Microsoft Edge ausgeführt werden sollen:

- **Microsoft Edge erlauben, sich selbst zu aktualisieren** (Standard). Wenn Sie automatische Updates von Microsoft Edge zulassen, wird Microsoft Edge automatisch in dem Tempo aktualisiert, das von den von Ihnen bereitgestellten Kanälen vorgegeben wird.
- **Microsoft Edge in eigenem Tempo aktualisieren**. Wenn Sie explizit steuern möchten, wann Updates bereitgestellt werden, können Sie automatische Updates deaktivieren und selbst bereitstellen (siehe [Referenz für Updaterichtlinien](./microsoft-edge-update-policies.md)). Wenn Sie automatische Updates deaktiviert haben, können Sie Updates für jeden Kanal mithilfe eines der folgenden Tools bereitstellen:

- [Intune](/intune/apps/apps-windows-edge?bc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2ftoc.json)
- [Konfigurations-Manager](./deploy-edge-with-configuration-manager.md)
- Bereitstellungstool Ihrer Wahl.

Unabhängig von Ihrer Updatestrategie wird empfohlen, eine mit Ringen versehene Bereitstellungsstrategie zu nutzen. Bei automatischen Updates erhalten Sie so eine repräsentative Stichprobe von Benutzern, die den Beta-Kanal ausführen, um Probleme damit zu identifizieren, was zum stabilen Kanal wird. Bei manuellen Updates kann dies auch eine zusätzliche Überprüfung einer Pilotgruppe beinhalten, nachdem ein neuer Build des stabilen Kanals herausgegeben wurde. Danach folgt die allgemeine Bereitstellung.

>[!NOTE]
>Microsoft Edge-Support ist nur für die neueste Version von Microsoft Edge in jedem Kanal verfügbar.

## <a name="do-app-compatibility-testing"></a>Testen der Anwendungskompatibilität

Die Anwendungskompatibilität für Microsoft Edge ist extrem hoch – so hoch, dass Microsoft die folgenden Kompatibilitätszusagen macht:

1. Wenn es in Microsoft Edge *Version 45 und früher* funktioniert, funktioniert es in Microsoft Edge *Version 77 und höher*.
2. Wenn es in Internet Explorer funktioniert, funktioniert es in Microsoft Edge im Internet Explorer-Modus.
3. Wenn es in Google Chrome funktioniert, funktioniert es in Microsoft Edge.

Wenn Sie eine Anwendung haben, bei der wir unsere Kompatibilitätszusage nicht erfüllen, stehen wir hinter dem Versprechen, es mit [Microsoft App Assure](https://www.microsoft.com/fasttrack/microsoft-365/desktop-app-assure) zu beheben.

### <a name="internal-line-of-business-app-testing"></a>Interne Branchen-App-Tests

Ungeachtet unserer Kompatibilitätszusage wissen wir, dass viele Organisationen Anwendungen aus Gründen der Konformität oder des Risikomanagements überprüfen müssen. Auch wenn wir davon ausgehen, dass das Verfahren sehr unkompliziert ist, ist es wichtig, dass Sie Anwendungstests auf organisierte Weise und strikt durchführen.

Es gibt zwei Möglichkeiten zum Testen der Anwendungskompatibilität:

1. Labtests: Anwendungen werden in einer streng kontrollierten Umgebung mit bestimmten Konfigurationen getestet.
2. Pilottests: Anwendungen werden von einer begrenzten Anzahl von Benutzern in ihrer täglichen Arbeitsumgebung mithilfe ihrer eigenen Geräte getestet.

Wählen Sie die Methode aus, die für jede Anwendung am besten geeignet ist. So können Sie die Risiken minimieren, ohne zu viel in Kompatibilitätstests zu investieren.

### <a name="third-party-app-support"></a>Unterstützung von Drittanbieter-Apps

Zusätzlich zu den eigenen Branchen-Apps verwenden viele Organisationen Apps, die von externen Quellen bereitgestellt werden. Der Artikel [Bereit für Microsoft Edge](deploy-edge-ready-for-edge.md) enthält eine Liste der Webanwendungen, die möglicherweise in Ihrer Organisation verwendet werden. Diese Liste enthält Links zu Unterstützungserklärungen der Anbieter für ihre Produkte bei Verwendung mit Microsoft Edge.

## <a name="deploy-microsoft-edge-to-a-pilot-group"></a>Bereitstellen von Microsoft Edge für eine Pilotgruppe

Nachdem Sie Ihre Richtlinien definiert und die ersten Anwendungskompatibilitätstests abgeschlossen haben, können Sie die Bereitstellung für Ihre Pilotgruppe durchführen. Stellen Sie Ihre Pilotgruppe mithilfe eines der folgenden Tools bereit:

- [Microsoft Intune für Windows](/intune/apps/apps-windows-edge?bc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2ftoc.json) oder [Microsoft Intune für macOS](/intune/apps/apps-edge-macos?bc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2ftoc.json)
- [Konfigurations-Manager](./deploy-edge-with-configuration-manager.md).
- Weiteres Verwaltungstool: Laden Sie die [MSI-Datei für Microsoft Edge](https://www.microsoftedgeinsider.com/enterprise) herunter, und stellen Sie sie bereit.

## <a name="validate-your-deployment"></a>Überprüfen Ihrer Bereitstellung

Nachdem Sie das Pilotprojekt bereitgestellt haben, können Sie das gesamte Feedback Ihrer Benutzer erfassen.

- Erfassen Sie Feedback zur Kompatibilität. Ermitteln Sie die Sites, die zur Enterprise-Siteliste gehören und während der Site-Discovery nicht identifiziert wurden.
- Erfassen Sie Feedback zur Richtlinienkonfiguration. Stellen Sie sicher, dass Benutzer wichtige Features verwenden und ihre Arbeit erledigen können, während die Sicherheitsrichtlinien befolgt werden.
- Erfassen Sie Feedback zur Benutzerfreundlichkeit und zu neuen Features. Identifizieren Sie alle Bereiche, in denen Schulungen basierend auf Benutzerfragen entwickelt und bereitgestellt werden sollten.

## <a name="broad-deployment-of-microsoft-edge"></a>Allgemeine Bereitstellung von Microsoft Edge

Nachdem Sie das Pilotprojekt abgeschlossen und den Bereitstellungsplan mit den Erkenntnissen aus dem Pilotprojekt aktualisiert haben, können Sie Microsoft Edge allen Benutzern vollständig bereitstellen.  Herzlichen Glückwunsch!

## <a name="see-also"></a>Weitere Informationen:

- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)
- [Video – Bereitstellen von Microsoft Edge](microsoft-edge-video-deploy.md)