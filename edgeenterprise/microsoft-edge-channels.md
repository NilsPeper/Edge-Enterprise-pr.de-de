---
title: Microsoft Edge – Kanalübersicht
ms.author: srugh
author: RyanHechtMSFT
manager: seanlynd
ms.date: 09/23/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Microsoft Edge – Kanalübersicht
ms.openlocfilehash: dd65d932950be90d3d9278fa41ae843335b2074d
ms.sourcegitcommit: 8e5294e82cf62abc916cfd24692f55925330d42b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/23/2021
ms.locfileid: "12037188"
---
# <a name="overview-of-the-microsoft-edge-channels"></a>Übersicht über die Microsoft Edge-Kanäle

Einer der Vorteile der nächsten Microsoft Edge-Version besteht darin, dass Microsoft in regelmäßigen Abständen neue Features bereitstellen kann. Als der Administrator, der Microsoft Edge für die Benutzer in Ihrem Unternehmen bereitstellt, möchten Sie jedoch möglicherweise mehr Kontrolle darüber haben, wie oft Ihre Benutzer diese neuen Features erhalten. Microsoft bietet ihnen vier Optionen, sog. Kanäle, um zu steuern, wie oft Microsoft Edge mit neuen Features aktualisiert wird. Hier eine Übersicht über die vier Optionen.

Weitere Informationen zur Unterstützung für jeden Kanal finden Sie unter:[ Microsoft Edge Lifecycle](/deployedge/microsoft-edge-support-lifecycle)
  
> [!NOTE]
> Dieser Artikel bezieht sich auf Microsoft Edge Version 77 oder höher.

## <a name="channel-overview"></a>Kanalübersicht

|Kanal|Hauptzweck|Wie oft mit neuen Features aktualisiert|Unterstützt?|
|:---:|---|:---:|:---:|
|[Stable](#stable-channel)|Breite Bereitstellung|~4 Wochen|Ja|
|[Extended Stable](#extended-stable-channel)|Eine Enterprise-Veröffentlichungsoption für Stable, die auf einen längeren Veröffentlichungszyklus ausgerichtet ist |~8 Wochen|Ja|
|[Beta](#beta-channel)|Repräsentative Überprüfung in der Organisation|~4 Wochen|Ja|
|[Dev](#dev-channel)|Planung und Entwicklung|Wöchentlich|Nein|
|[Canary](#canary-channel)|Neuster Inhalt|Täglich|Nein|

Welcher Updatekanal Sie für Ihre Benutzer bereitstellen möchten, hängt von mehreren Faktoren ab, z. B. davon, wie viele Branchenanwendungen der Benutzer nutzt und dass Sie jedes Mal testen müssen, wenn er über eine aktualisierte Version von Microsoft Edge verfügt. Um Ihnen diese Entscheidung zu erleichtern, hier einige Informationen über die vier Updatekanäle, die für Microsoft Edge verfügbar sind.

### <a name="stable-channel"></a>Stable-Kanal

Der Stable-Kanal ist für den breiten Einsatz in Ihrem Unternehmen gedacht. Diesen Kanal sollten die meisten Benutzer verwenden. Es ist der stabilste Kanal und das Ergebnis der Stabilität des Featuresatzes, der in der vorherigen Betakanalversion verfügbar ist. Neue Features werden etwa alle 4 Wochen ausgeliefert. Sicherheits- und Qualitätsupdates werden nach Bedarf ausgeliefert. Eine Freigabe aus dem Stabilen Kanal wird bedient, bis die nächste Freigabe aus dem Kanal verfügbar ist.

### <a name="beta-channel"></a>Beta-Kanal

Der Beta-Kanal ist für den Produktionseinsatz in Ihrem Unternehmen für eine repräsentative Auswahl von Benutzern vorgesehen. Es handelt sich um eine unterstützte Freigabe und jede Betaversion wird bedient, bis die nächste Freigabe dieses Kanals verfügbar ist. Dies ist eine gute Gelegenheit, um zu überprüfen, ob alles in Ihrer Umgebung wie erwartet funktioniert. Wenn ein Problem auftritt, kann es vor der Veröffentlichung im Stable-Kanal behoben werden. Neue Features werden etwa alle 4 Wochen ausgeliefert. Sicherheits- und Qualitätsupdates werden nach Bedarf ausgeliefert.

### <a name="dev-channel"></a>Dev-Kanal

Der Dev-Kanal soll Sie bei der Planung und Entwicklung mit den neuesten Funktionen von Microsoft Edge unterstützen, jedoch mit einer höheren Qualität als im Canary-Kanal. Dies ist Ihre Gelegenheit, sich einen ersten Überblick über die nächsten Schritte zu verschaffen und sich auf die nächste Beta-Version vorzubereiten.

### <a name="canary-channel"></a>Canary-Kanal

Der Canary-Kanal wird täglich ausgeliefert und ist der aktuellste aller Kanäle. Wenn Sie Zugriff auf die neuesten Investitionen benötigen, werden sie hier zuerst angezeigt. Aufgrund der Art dieser Häufigkeit treten Überstunden probleme auf, daher möchten Sie möglicherweise, dass ein anderer Kanal nebeneinander installiert wird, wenn Sie die Canary-Versionen nutzen.

### <a name="extended-stable-channel"></a>Erweiterter stable-Kanal

Im Gegensatz zu unseren Vorschaukanälen (Canary, Dev und Beta) ist der extended Stable Channel nicht als separate Browseranwendung verfügbar. Stattdessen handelt es sich um eine Enterprise-Veröffentlichungsoption für die Microsoft Edge Stable-Anwendung, die an einen längeren, 8-wöchigen Hauptversionszyklus ausgerichtet ist (im Gegensatz zum 4-wöchigen Hauptversionszyklus in Stable). Während wir empfehlen, Stable automatisch auf den 4-wöchigen Veröffentlichungszyklus zu aktualisieren, ist extended Stable vorhanden, um Organisationen effektiver zu dienen, die möglicherweise eine längere Zeitachse benötigen, um neue Browserversionen zu testen und zu überprüfen.

Die 8-wöchige Option für den Veröffentlichungszyklus "Extended Stable" für Microsoft Edge Stable bietet kumulative Featureupdates, die an versionen mit _gerader Nummerierung_ ausgerichtet sind, beginnend mit Microsoft Edge 94; Alle Funktionsupdates von Versionen mit ungerader Nummer werden gepackt und als Teil der nachfolgenden geraden Version bereitgestellt. Wenn eine Organisation beispielsweise den 8-wöchigen Veröffentlichungszyklus "Extended Stable" mit Microsoft Edge 94 auswählt, erhalten sie nachfolgende Funktionsupdates mit Microsoft Edge 96, Microsoft Edge 98 usw. Während Featureupdates basierend auf dem ausgewählten Veröffentlichungszyklus gepackt und mit neuen Versionsversionen bereitgestellt werden, werden wichtige Sicherheitspatches und Fixes nach Bedarf unabhängig von der ausgewählten Releaseoption bereitgestellt, um die Browsersicherheit zu gewährleisten. Kunden können sich jederzeit für die Extended Stable-Veröffentlichungsoption entscheiden, die mit der nächsten extended Stable-Version wirksam wird.

![Beispiel für einen Vergleich Microsoft Edge Optionen für den stabilen und den erweiterten Stabil-Releasezyklus.](./media/microsoft-edge-channels/extended-stable-explainer.png)

#### <a name="opting-in-to-the-extended-stable-release-cadence"></a>Opt-In für den erweiterten Stable Release Cadence

##### <a name="opting-in-to-extended-stable-on-windows-with-automatic-updates-recommended"></a>Aktivieren von Extended Stable auf Windows mit automatischen Updates (empfohlen)

Wenn Sie Microsoft Edge automatisch aktualisieren, können Sie gruppenrichtlinienobjekte verwenden, um sich für den Erweiterten Stable-Versionsrhythmus zu entscheiden. [Folgen Sie diesem Leitfaden,](/DeployEdge/configure-microsoft-edge#1-download-and-install-the-microsoft-edge-administrative-template) um weitere Informationen zum Herunterladen und Installieren der neuesten administrativen Vorlagen für Microsoft Edge Gruppenrichtlinien zu erfahren.

1. Öffnen Sie den Editor für lokale Gruppenrichtlinien, und wechseln Sie zu _Computerkonfiguration > Administrative Vorlagen > Microsoft Edge Update > Anwendungen > Microsoft Edge>_.
2. Wählen Sie **"Zielkanalüberschreibung"** und dann **"Aktiviert"** aus.
3. Wählen Sie unter **"Optionen"** in der Dropdownliste "Richtlinie" die Option **"Extended Stable"** aus.

Wenn das nächste Update für den erweiterten Stable-Kanal veröffentlicht wird, dessen Versionsnummer größer ist als das, was Ihr Gerät derzeit installiert hat, wird Microsoft Edge automatisch auf den erweiterten Stable-Kanal aktualisiert. Die Versionszeichenfolge `edge://settings/help` zeigt an, dass Sie einen anderen Kanal ausführen.

> [!NOTE]
> Die Zustimmung zu Extended Stable wird wirksam, wenn ein neues Update auf dem erweiterten Stable-Kanal mit einer größeren Versionsnummer (Hauptversion oder Nebenversion) als der aktuell auf Ihrem Gerät installiert ist. Wenn Sie die neueste Version von Microsoft Edge Stable ausführen und sich für extended Stable anmelden, wird sie mit dem nächsten Patch oder Update von Microsoft Edge wirksam.
>
> Standardmäßig wird Microsoft Edge sich selbst nicht herabstufen. Wenn Sie derzeit eine ungerade Version von Microsoft Edge Stable ausführen, bedeutet die Anmeldung bei Extended Stable, dass Sie keine Updates bis zur nächsten geraden Microsoft Edge version erhalten.
>
> Wenn Sie sicherstellen möchten, dass alle Ihre Geräte mit einer bestimmten Version von Extended Stable beginnen, können Sie diese bestimmte Version von Edge Stable als MSI mit aktivierter Rollbackversion bereitstellen. Wenn Sie beispielsweise mit Extended Stable 94 beginnen möchten, einige Geräte jedoch bereits auf Stable 95 aktualisiert haben, können Sie eine MSI-Datei von Edge 94 mit aktivierter Rollbackbereitstellung bereitstellen. Weitere Informationen zum Bereitstellen von Edge-MSIs mit aktivierten Rollbacks finden Sie in unserem [Rollbackhandbuch.](/DeployEdge/edge-learnmore-rollback)

##### <a name="opting-in-to-extended-stable-on-windows-via-intune"></a>Opt-In für extended Stable auf Windows über Intune

Microsoft Edge Administrative Vorlagen können ähnlich wie lokale Gruppenrichtlinienobjekte aus dem Microsoft Endpoint Manager Admin Center verwaltet werden. Folgen Sie unserem [Leitfaden zum Konfigurieren von Microsoft Edge mit Intune.](/mem/intune/configuration/administrative-templates-configure-edge) 

Die Einstellung "**Zielkanalüberschreibung**" finden Sie unter den Unterordnern "_Microsoft Edge Update >Anwendungen>Microsoft Edge_". Sie sollte auf **"Extended Stable"** festgelegt werden. 

Wenn das nächste Update für den erweiterten Stable-Kanal veröffentlicht wird, dessen Versionsnummer größer ist als das, was Ihr Gerät derzeit installiert hat, wird Microsoft Edge automatisch auf den erweiterten Stable-Kanal aktualisiert. Die Versionszeichenfolge `edge://settings/help` zeigt an, dass Sie einen anderen Kanal ausführen.

##### <a name="opting-in-to-extended-stable-on-windows-via-configuration-manager"></a>Opt-In für extended Stable auf Windows über Configuration Manager

Weitere Informationen zum Synchronisieren und Genehmigen Microsoft Edge Updates in Configuration Manager finden Sie in unserem Leitfaden zum Aktualisieren von [Microsoft Edge mit Configuration](/mem/configmgr/apps/deploy-use/deploy-edge#update-microsoft-edge) Manager.

Erweiterte stabile Updates werden in der Softwarebibliothek unter der Produktkategorie "Microsoft Edge" verteilt, ähnlich wie vorhandene Updates für die Stable-, Beta- und Dev-Kanäle. Im Gegensatz zu Beta und Dev, die für ihre eigenen Browseranwendungen gelten, gelten die extended Stable-Updates jedoch für Microsoft Edge Stable-Anwendung. Damit Ihr Windows Updateclient ermittelt, ob stabile oder erweiterte Stable-Updates angewendet werden sollen, überprüft er daher den Status der Gruppenrichtlinie "Zielkanal außer Kraft setzen". Wenn die Richtlinie nicht konfiguriert oder auf "Stabil" festgelegt ist, gelten stabile Updates. Wenn sie auf "Extended Stable" festgelegt ist, gelten erweiterte Stable-Updates. Folgen Sie den obigen Anweisungen für die Anmeldung bei Extended Stable mit automatischen Updates, um Anweisungen zum ordnungsgemäßen Festlegen der Gruppenrichtlinie zu erhalten. 

## <a name="flighting-pre-release-channels-in-your-organization"></a>Test-Flighting-Vorabversionskanäle in Ihrer Organisation

Die Gruppenrichtlinie "Zielkanal außer Kraft setzen" kann auch verwendet werden, um Kanäle von Microsoft Edge in Ihrer Organisation nahtlos zu starten, ohne dass Ihre Benutzer eine zweite Webbrowseranwendung verwenden müssen. Sie können beispielsweise die Richtlinie "Zielkanalüberschreibung" für eine repräsentative Beispielgruppe von Benutzern in Ihrer Organisation auf "Beta" festlegen. Wenn diese Benutzer Microsoft Edge öffnen, führen sie die Betakanalversion anstelle von Stable aus (wahrscheinlich ohne dass sie es überhaupt merken!). Auf diese Weise erhalten Sie einen frühen Einblick in die Leistung der nächsten Version von Microsoft Edge in Ihrem Unternehmen und können überprüfen, ob alles in Ihrer Umgebung erwartungsgemäß funktioniert. Sie erhalten frühe Signale von Ihren Benutzern, die auf Probleme stoßen, und können sicherstellen, dass sie vor der Veröffentlichung im Stable Channel behoben sind. Im Rahmen der Problembehandlung eines Benutzers informiert Sie die Versionszeichenfolge at darüber, `edge://settings/help` ob sich der Kanal des Benutzers vom Standardmäßigen Stable-Kanal unterscheidet.

> [!NOTE]
> Da build on the "Beta" and "Dev" channels of Microsoft Edge have major version numbers larger than that of "Stable", if you take an update to the "Beta" or "Dev" channel and wish to revert to Stable, [Microsoft Edge's rollback feature](/DeployEdge/edge-learnmore-rollback) will be required. Wenn Sie einfach "Zielkanalüberschreibung" wieder auf Stable festlegen, erhalten Sie keine Updates, bis die neueste Stable-Version eine höhere Versionsnummer hat als die Version von Microsoft Edge Sie derzeit auf Ihrem Gerät ausgeführt werden.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)
- [Kanal-Downloads](https://aka.ms/EdgeEnterprise)
