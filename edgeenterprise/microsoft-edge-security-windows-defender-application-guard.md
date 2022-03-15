---
title: Microsoft Edge und Microsoft Defender Application Guard
ms.author: srugh
author: AndreaLBarr
manager: seanlyn
ms.date: 03/07/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Microsoft Edge-Unterstützung für Microsoft Defender Application Guard
ms.openlocfilehash: fd5293dae19be2aa0939e3a14eeb118907ad375a
ms.sourcegitcommit: 556aca8dde42dd66364427f095e8e473b86651a0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2022
ms.locfileid: "12445489"
---
# <a name="microsoft-edge-support-for-microsoft-defender-application-guard"></a>Microsoft Edge-Unterstützung für Microsoft Defender Application Guard

In diesem Artikel wird beschrieben, wie Microsoft Edge den Microsoft Defender Application Guard (Application Guard) unterstützt.

> [!NOTE]
> Dieser Artikel bezieht sich auf Microsoft Edge Version 77 oder höher.

## <a name="overview"></a>Übersicht

Sicherheitsarchitekten im Unternehmen müssen sich mit dem Spannungsverhältnis zwischen Produktivität und Sicherheit auseinandersetzen. Es ist relativ einfach, einen Browser zu sperren und nur das Laden einer Handvoll vertrauenswürdiger Websites zu erlauben. Dieser Ansatz verbessert die allgemeine Sicherheitslage, ist aber wohl weniger produktiv. Wenn Sie die Einschränkungen lockern um die Produktivität zu steigern, erhöhen Sie dadurch das Risikoprofil. Es ist schwierig, eine Balance zu finden!

In dieser sich ständig verändernden Bedrohungslandschaft ist es noch schwieriger, mit neu aufkommenden Bedrohungen Schritt zu halten. Browser bleiben die Hauptangriffsfläche auf Clientgeräten, da es ihre grundlegende Aufgabe ist, Benutzern zu ermöglichen, auf nicht vertrauenswürdige Inhalte von nicht vertrauenswürdigen Quellen zuzugreifen, diese herunterzuladen und auszuführen. Böswillige Akteure arbeiten ständig daran, neue Formen von Angriffen auf den Browser zu entwickeln. Die Verhinderung von Sicherheitsvorfällen oder Strategien zur Erkennung bzw. Reaktion können keine 100 %-ige Sicherheit garantieren.

Eine wichtige Sicherheitsstrategie, die es zu berücksichtigen gilt, ist die [Assume Breach-Methode](/office365/Enterprise/office-365-monitoring-and-testing#assume-breach-methodology), d. h. es wird akzeptiert, dass ein Angriff mindestens einmal erfolgreich sein wird, unabhängig von den Bemühungen, dies zu verhindern. Diese Denkweise erfordert es, Verteidigungmechanismen zu erstellen, um den Schaden einzudämmen, wodurch sichergestellt wird, dass das Unternehmensnetzwerk und andere Ressourcen in diesem Szenario geschützt bleiben.  Die Bereitstellung von Application Guard für Microsoft Edge passt genau in diese Strategie.

## <a name="about-application-guard"></a>Informationen zu Application Guard

Application Guard wurde für Windows 10 und Microsoft Edge entwickelt und verwendet einen Ansatz der Hardwareisolierung. Dieser Ansatz ermöglicht den Start einer nicht vertrauenswürdigen Websitenavigation innerhalb eines Containers. Die Hardwareisolierung hilft Unternehmen, ihr Unternehmensnetzwerk und ihre Daten zu schützen, falls Benutzer eine kompromittierte oder böswillige Website besuchen.

Der Unternehmensadministrator definiert, was zu vertrauenswürdigen Websites, Cloudressourcen und internen Netzwerken gehört. Alles, was nicht in der Liste der vertrauenswürdigen Sites enthalten ist, wird als nicht vertrauenswürdig angesehen. Diese Websites werden vom Unternehmensnetzwerk und den Daten auf dem Gerät des Benutzers isoliert.

Weitere Informationen finden Sie unter:

- Sehen Sie sich unser Video zur [Microsoft Edge-Browserisolation mit Application Guard](microsoft-edge-video-security-application-guard.md) an.
- Lesen Sie, [was Application Guard ist und wie es funktioniert.](/windows/security/threat-protection/microsoft-defender-application-guard/md-app-guard-overview#what-is-application-guard-and-how-does-it-work)

Der nächste Screenshot zeigt ein Beispiel einer Meldung von Application Guard, die zeigt, dass sich der Benutzer in einem sicheren Bereich befindet.

![Application Guard-Meldung über sicheres Surfen](media/microsoft-edge-security-windows-defender-application-guard/wd-application-guard-1.png)

## <a name="whats-new"></a>Neuigkeiten

Die Unterstützung von Application Guard im neuen Microsoft Edge-Browser ist funktional gleichwertig mit der Vorgängerversion von Microsoft Edge und umfasst mehrere Verbesserungen.

### <a name="enable-application-guard-in-passive-mode-and-browse-edge-normally"></a>Aktivieren von Application Guard im passiven Modus und normales Durchsuchen von Edge

Ab Microsoft Edge 94 haben Benutzer jetzt die Möglichkeit, den passiven Modus zu konfigurieren, was bedeutet, dass Application Guard die Konfiguration der Websitelisten ignoriert und Benutzer Edge normal durchsuchen können. Diese Unterstützung kann über Richtlinien gesteuert werden. Sie können die Edgerichtlinie [ApplicationGuardPassiveModeEnabled](/deployedge/microsoft-edge-policies#applicationguardpassivemodeenabled) aktualisieren, um den passiven Modus zu aktivieren oder zu deaktivieren.

> [!Note]
> Diese Richtlinie wirkt sich NUR auf Edge aus, sodass Navigationen von anderen Browsern möglicherweise an den Application Guard-Container umgeleitet werden, wenn die entsprechenden Erweiterungen aktiviert sind.

### <a name="favorites-synchronizing-from-the-host-to-the-container"></a>Favoriten, die vom Host mit dem Container synchronisiert werden

Einige unserer Kunden haben nach der Synchronisierung von Favoriten zwischen dem Hostbrowser und dem Container in Application Guard gefragt. Ab Microsoft Edge 91 haben Benutzer jetzt die Möglichkeit, Application Guard so zu konfigurieren, dass ihre Favoriten vom Host mit dem Container synchronisiert werden. Dadurch wird sichergestellt, dass auch neue Favoriten im Container angezeigt werden.

Diese Unterstützung kann über eine Richtlinie gesteuert werden. Sie können die Edgerichtlinie [ApplicationGuardFavoritesSyncEnabled](/deployedge/microsoft-edge-policies#applicationguardfavoritessyncenabled) aktualisieren, um die Favoritensynchronisierung zu aktivieren oder zu deaktivieren.

> [!Note]
> Aus Sicherheitsgründen ist die Favoritensynchronisierung nur vom Host zum Container möglich und nicht umgekehrt. Um eine einheitliche Liste von Favoriten für den Host und den Container sicherzustellen, haben wir die Favoritenverwaltung innerhalb des Containers deaktiviert.

### <a name="identify-network-traffic-originating-from-the-container"></a>Identifizieren von Netzwerkdatenverkehr, der vom Container stammt

Mehrere Kunden verwenden WDAG in einer bestimmten Konfiguration, in der sie Netzwerkdatenverkehr identifizieren möchten, der aus dem Container stammt. Einige solcher Szenarien sind:

- Zugriff beschränken auf eine Reihe nicht vertrauenswürdiger Websites
- Internetzugriff nur über den Container erlauben

Ab Microsoft Edge Version 91 gibt es integrierte Unterstützung zum Markieren von Netzwerkdatenverkehr von Application Guard-Containern, sodass Unternehmen Proxy verwenden können, um Datenverkehr herauszufiltern und bestimmte Richtlinien anzuwenden. Sie können den Header verwenden, um mithilfe von [ApplicationGuardTrafficIdentificationEnabled](/deployedge/microsoft-edge-policies#applicationguardtrafficidentificationenabled) zu ermitteln, welcher Datenverkehr durch den Container oder den Host geleitet wird.

### <a name="extension-support-inside-the-container"></a>Unterstützung von Erweiterungen im Container

Die Unterstützung von Erweiterungen im Container war eines der wichtigsten Anliegen der Kunden. Die Wunschszenarien reichten vom Ausführen von Werbeblockern innerhalb des Containers über die Steigerung der Browserleistung bis hin zur Möglichkeit, benutzerdefinierte, selbst entwickelte Erweiterungen innerhalb des Containers auszuführen.

Die Installation von Erweiterungen im Container wird nun ab Microsoft Edge Version 81 unterstützt. Diese Unterstützung kann über Richtlinien gesteuert werden. Die `updateURL`, die in der Richtlinie [ExtensionInstallForcelist](./microsoft-edge-policies.md#extensioninstallforcelist) verwendet wird, sollte als neutrale Ressourcen in die von Application Guard verwendeten Richtlinien zur Netzwerkisolierung aufgenommen werden.

Die folgenden Szenarien sind einige Beispiele für die Containerunterstützung:

- Erzwingen der Installation einer Erweiterung auf dem Host
- Entfernen einer Erweiterung vom Host
- Auf dem Host blockierte Erweiterungen

> [!NOTE]
> Es ist auch möglich, einzelne Erweiterungen innerhalb des Containers manuell aus dem Erweiterungsspeicher zu installieren. Manuell installierte Erweiterungen bleiben nur dann im Container erhalten, wenn die Richtlinie [Persistenz erlauben](/windows/security/threat-protection/microsoft-defender-application-guard/configure-md-app-guard#application-specific-settings) aktiviert ist.

### <a name="identifying-application-guard-traffic-via-dual-proxy"></a>Identifizieren des Datenverkehrs in Application Guard über den dualen Proxy

Einige Enterprise-Kunden stellen Application Guard mit einem bestimmten Verwendungsfall bereit, in dem sie den Webdatenverkehr ermitteln müssen, der aus einem Microsoft Defender Application Guard-Container auf der Proxyebene stammt. Beginnend mit der Stable-Kanalversion 84 unterstützt Microsoft Edge den dualen Proxy, um diese Anforderung zu erfüllen. Sie können diese Funktion mithilfe der [ApplicationGuardContainerProxy](./microsoft-edge-policies.md#applicationguardcontainerproxy)-Richtlinie konfigurieren.

Die folgende Abbildung zeigt die Architektur des dualen Proxys für Microsoft Edge.

![Duale Proxy-Architektur für Application Guard](media/microsoft-edge-security-windows-defender-application-guard/wd-application-guard-dual-proxy.png)

### <a name="diagnostic-page-for-troubleshooting"></a>Diagnoseseite zur Problembehandlung

Ein weiterer Problempunkt für den Benutzer ist die Behandlung von Problemen beim Konfigurieren von Application Guard auf einem Gerät, wenn ein Problem gemeldet wird. Microsoft Edge verfügt über eine Diagnoseseite (`edge://application-guard-internals`) zur Behebung von Benutzerproblemen. Eine dieser Diagnosen ist die Möglichkeit, die URL-Vertrauenswürdigkeit auf der Grundlage der Konfiguration auf dem Gerät des Benutzers zu überprüfen.

Der nächste Screenshot zeigt eine Diagnoseseite mit mehreren Registerkarten, die bei der Diagnose von Problemen auf dem Gerät hilft, die vom Benutzer gemeldet werden.

![Application Guard-Diagnoseseite](media/microsoft-edge-security-windows-defender-application-guard/wd-application-guard-2.png)

### <a name="microsoft-edge-updates-in-the-container"></a>Microsoft Edge-Updates im Container

Microsoft Edge Legacy-Updates im Container sind Teil des Windows OS-Updatezyklus. Da die neue Version von Microsoft Edge unabhängig vom Windows-Betriebssystem aktualisiert wird, gibt es keine Abhängigkeit mehr von Containerupdates. Kanal und Version des Microsoft Edge-Hosts werden innerhalb des Containers repliziert.

## <a name="prerequisites"></a>Voraussetzungen

Die folgenden Anforderungen gelten für Geräte, die Application Guard mit Microsoft Edge verwenden:

- Windows 10 1809 (RS5) und höher.
- Nur Windows-Client-SKUs

  > [!NOTE]
  > Application Guard wird nur unter Windows 10 Pro und Windows 10 Enterprise SKUs unterstützt.

- Eine der unter [Softwareanforderungen](/windows/security/threat-protection/microsoft-defender-application-guard/reqs-md-app-guard#software-requirements) beschriebenen Verwaltungslösungen

## <a name="how-to-install-application-guard"></a>Installieren von Application Guard

Die folgenden Artikel enthalten die Informationen, die Sie zum Installieren, Konfigurieren und Testen von Application Guard mit Microsoft Edge benötigen.

- [Systemanforderungen](/windows/security/threat-protection/microsoft-defender-application-guard/reqs-md-app-guard)
- [Microsoft Defender Application Guard installieren](/windows/security/threat-protection/microsoft-defender-application-guard/install-md-app-guard)
- [Konfigurieren von Application Guard-Gruppenrichtlinieneinstellungen](/windows/security/threat-protection/microsoft-defender-application-guard/configure-md-app-guard)
- [Testen von Application Guard](/windows/security/threat-protection/microsoft-defender-application-guard/test-scenarios-md-app-guard)

## <a name="frequently-asked-questions"></a>Häufig gestellte Fragen

### <a name="does-application-guard-work-in-ie-mode"></a>Funktioniert Application Guard im IE-Modus?

Der IE-Modus unterstützt Application Guard-Funktionalität, aber wir gehen davon aus, dass dieses Feature im IE-Modus nicht viel genutzt wird. Es wird empfohlen, den IE-Modus für eine Liste vertrauenswürdiger interner Websites bereitzustellen, und Application Guard gilt nur für nicht vertrauenswürdige Websites. Stellen Sie sicher, dass alle Websites oder IP-Adressen im IE-Modus auch der Richtlinie zur Netzwerkisolierung hinzugefügt werden, um von Application Guard als vertrauenswürdige Ressourcen betrachtet zu werden.

### <a name="do-i-need-to-install-the-application-guard-chrome-extension"></a>Muss ich die Application Guard Chrome-Erweiterung installieren?

Nein, das Application Guard-Feature wird in Microsoft Edge nativ unterstützt. Tatsächlich ist die Application Guard Chrome-Erweiterung keine unterstützte Konfiguration in Microsoft Edge.

### <a name="can-employees-download-documents-from-the-application-guard-edge-session-onto-host-devices"></a>Können Mitarbeiter Dokumente aus der Application Guard Edge-Sitzung auf Hostgeräte herunterladen?

In Windows 10 Enterprise Edition, Version 1803, können Benutzer Dokumente aus dem isolierten Application Guard-Container auf den Host-PC herunterladen. Diese Funktion wird durch eine Richtlinie verwaltet.

In Windows 10 Enterprise Edition, Version 1709, oder Windows 10 Professional Edition, Version 1803, ist es nicht möglich, Dateien aus dem isolierten Application Guard-Container auf den Hostcomputer herunterzuladen. Mitarbeiter können jedoch die Option Als PDF drucken oder Als XPS drucken verwenden und die jeweiligen Dateien auf dem Hostgerät speichern.

### <a name="can-employees-copy-and-paste-between-the-host-device-and-the-application-guard-edge-session"></a>Können Mitarbeiter Kopieren-und-Einfügen-Vorgänge zwischen dem Hostgerät und der Application Guard Edge-Sitzung vornehmen?

Abhängig von den Einstellungen Ihrer Organisation können Mitarbeiter Bilder (.bmp) und Text in und aus dem isolierten Container kopieren und einfügen.

### <a name="why-dont-employees-see-their-favorites-in-the-application-guard-edge-session"></a>Warum sehen Mitarbeiter ihre Favoriten nicht in der Application Guard Edge-Sitzung?

Abhängig von den Einstellungen Ihrer Organisation kann es sein, dass die Favoritensynchronisierung deaktiviert ist. Informationen zum Verwalten der Richtlinie finden Sie unter: Microsoft Edge und Microsoft Defender Application Guard | Microsoft Docs.

### <a name="why-arent-employees-able-to-see-their-extensions-in-the-application-guard-edge-session"></a>Warum können Mitarbeiter ihre Erweiterungen in der Application Guard Edge-Sitzung nicht sehen?

Stellen Sie sicher, dass Sie die Erweiterungsrichtlinie für Ihre Application Guard-Konfiguration aktivieren.

### <a name="my-extension-doesnt-seem-to-work-in-edge-application-guard"></a>Meine Erweiterung funktioniert in Edge Application Guard scheinbar nicht?

Wenn die Erweiterungsrichtlinie für MDAG in der Konfiguration aktiviert ist, überprüfen Sie, ob Ihre Erweiterung systemeigene Nachrichtenbehandlungskomponenten erfordert. Diese Erweiterungen werden im Application Guard-Container nicht unterstützt.

### <a name="im-trying-to-watch-playback-video-with-hdr-why-is-the-hdr-option-missing"></a>Ich versuche, die Videowiedergabe mit HDR anzusehen, warum fehlt die HDR-Option?

Damit die HDR-Videowiedergabe im Container funktioniert, muss die vGPU-Hardwarebeschleunigung in Application Guard aktiviert werden.

### <a name="are-there-any-other-platform-related-faqs"></a>Gibt es weitere plattformbezogene FAQs?

Ja. [Häufig gestellte Fragen – Microsoft Defender Application Guard](/windows/security/threat-protection/microsoft-defender-application-guard/faq-md-app-guard) 

## <a name="see-also"></a>Weitere Informationen

- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)
- [Microsoft Defender Advanced Threat Protection](/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection)
- [Video: Microsoft Edge-Browserisolation mit Application Guard](https://www.youtube.com/watch?v=zQjaRqNXMqw&t=3s)
