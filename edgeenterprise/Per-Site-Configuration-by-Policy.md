---
title: 'Konfiguration pro Website nach Richtlinie '
ms.author: collw
author: AndreaLBarr
manager: laurawi
ms.date: 05/03/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 'Konfiguration pro Website nach Richtlinie '
ms.openlocfilehash: 6bba2c9b1d691c338a3146ef246de9f94e262a03
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2021
ms.locfileid: "11618122"
---
# <a name="persite-configuration-by-policy"></a>Konfiguration pro Website nach Richtlinie

## <a name="introduction-browsers-as-decision-makers"></a>Einführung: Browser als Entscheidungsträger

Im Rahmen jedes Seitenladevorgangs treffen Browser viele Entscheidungen. Sollte eine bestimmte API verfügbar sein? Sollte eine Ressourcenauslastung zulässig sein? Sollte die Ausführung des Skripts zugelassen werden? Die Liste ist lang.

In den meisten Fällen werden Entscheidungen durch zwei Eingaben gesteuert: eine Benutzereinstellung und die URL der Seite, für die die Entscheidung getroffen wird.

In der Legacy-Internet-Explorer-Webplattform wurde jede dieser Entscheidungen als [URLAction](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537178%28v%3dvs.85%29)bezeichnet, und die Enterprise Gruppenrichtlinie und die Benutzereinstellungen in der Internet-Systemsteuerung steuerten, wie der Browser jede Entscheidung behandelte.  

In Microsoft Edge werden die meisten Berechtigungen pro Website durch Einstellungen und Richtlinien gesteuert, die mithilfe einer einfachen Syntax mit eingeschränkter Unterstützung für Platzhalter ausgedrückt werden. Windows-Sicherheitszonen werden weiterhin nur für eine kleine Anzahl von Konfigurationsentscheidungen verwendet.

## <a name="background-windows-security-zones"></a>Hintergrund: Windows-Sicherheitszonen

Um die Konfiguration für den Benutzer oder dessen Administrator zu vereinfachen, hat die Legacyplattform Websites in fünf verschiedene **Sicherheitszonen**klassifiziert: lokaler Computer, lokales Intranet, vertrauenswürdig, Internet und eingeschränkte Websites.

Wenn Sie eine Entscheidung treffen, ordnet der Browser die Website zunächst einer Zone zu und liest dann die Einstellung für diese URLAction für diese Zone, um zu entscheiden, was getan werden soll. Angemessene Standardwerte wie "Automatische Erfüllung von Authentifizierungsproblemen aus meinem Intranet" bedeuteten, dass die meisten Benutzer niemals Einstellungen von abweichend von der Standardeinstellungen ändern mussten.

Benutzer können die Internetsystemsteuerung verwenden, um Zonen bestimmte Websites zuzuweisen und die Berechtigungsergebnisse für jede Zone zu konfigurieren. In verwalteten Umgebungen können Administratoren Gruppenrichtlinien verwenden, um Zonen bestimmte Websites zuzuweisen (über die Richtlinie "Site-to-Zone-Zuweisungsliste"), und die Einstellungen für URLActions auf Zonenbasis angeben. Neben der manuellen administrativen Zuweisung oder der Benutzerzuweisung von Websites zu Zonen können zusätzliche Heuristiken [Websites der lokalen Intranetzone zuweisen](/archive/blogs/ieinternals/the-intranet-zone). Insbesondere wurden der Intranetzone punktlose Hostnamen (z. B. `http://payroll`) zugewiesen. Wenn ein Proxykonfigurationsskript verwendet wurde, wurden alle Websites, die für die Umgehung des Proxys konfiguriert wurden, der Intranetzone zugeordnet.

Vorgängerversion von Microsoft Edge haben die Zonenarchitektur von ihrem Internet Explorer-Vorgänger mit einigen vereinfachenden Änderungen geerbt:

- Die fünf integrierten Windows-Zonen wurden auf drei reduziert: Internet (Internet), vertrauenswürdig (Intranet+ vertrauenswürdig) und lokaler Computer. Die Zone "Eingeschränkte Websites" wurde entfernt.

- Zonen-zu-URLAction-Zuordnungen wurden im Browser hartcodiert, wobei Gruppenrichtlinien und Einstellungen in der Internetsystemsteuerung ignoriert wurden.

## <a name="per-site-permissions-in-the-microsoft-edge"></a>Per-Site Berechtigungen in Microsoft Edge

Im Gegensatz zu seinen Vorgängern, verwendet das neue Microsoft Edge Windows-Sicherheitszonen nur sehr eingeschränkt. Stattdessen basieren die meisten Berechtigungen und Features, die Administratoren die Konfiguration pro Website per [Richtlinie](/deployedge/microsoft-edge-policies) bieten, auf Listen von Regeln im [URL-Filterformat.](/DeployEdge/edge-learnmmore-url-list-filter%20format)

Wenn Endbenutzer <code>edge://settings/content/siteDetails?site=https://example.com</code>öffnen, finden sie eine lange Liste von Konfigurationsschaltern und Listen für verschiedene Berechtigungen. Benutzer verwenden die Einstellungsseite selten direkt, stattdessen treffen sie beim Browsen mit verschiedenen Widgets und Umschaltflächen in der  **Seiteninformationen** -Dropdownliste (die angezeigt wird, wenn Sie auf das Schlosssymbol in der Adressleiste klicken) oder über verschiedene Eingabeaufforderungen oder Schaltflächen am rechten Rand der Adressleiste Entscheidungen.

Unternehmen können Gruppenrichtlinie verwenden, um Websitelisten für einzelne Richtlinien bereitzustellen, die das Verhalten des Browsers steuern. Um diese Richtlinien zu finden, öffnen Sie einfach die [Microsoft Edge Gruppenrichtlinie Dokumentation](/deployedge/microsoft-edge-policies) , und suchen Sie nach **ForUrls** , um die Richtlinien zu finden, die das Verhalten basierend auf der URL der geladenen Website zulassen und blockieren. Die meisten relevanten Einstellungen sind im Abschnitt [Gruppenrichtlinie für Inhaltseinstellungen](/deployedge/microsoft-edge-policies#content-settings) aufgeführt.

Es gibt auch eine Reihe von Richtlinien (deren Namen **Standard**enthalten), die das Standardverhalten für eine bestimmte Einstellung steuern.

Viele der Einstellungen sind sehr verdeckt (WebSerial, WebMIDI), und es gibt sehr oft keinen Grund, eine Einstellung abweichend von der Standardeinstellung (Bilder) zu ändern.

## <a name="common-questions"></a>Allgemeine Fragen

## <a name="q-can-the-url-filter-format-match-on-a-sites-ip-address"></a>F: Kann das URL-Filterformat für die IP-Adresse einer Website übereinstimmen?

Nein, das Format unterstützt nicht die Spezifikation eines IP-Bereichs für Zulassungs- und Sperrlisten. Es unterstützt die Spezifikation einzelner IP- **Literale**. Diese Regeln werden jedoch nur berücksichtigt, wenn der Benutzer mit dem angegebenen Literal zur Website navigiert (z. B. <http://127.0.0.1/>). Wenn ein Hostname verwendet wird (<http://localhost>), wird die IP-Literalregel nicht berücksichtigt, obwohl die aufgelöste IP-Adresse des Hosts mit der IP-Adresse übereinstimmt, die in der Filterliste aufgeführt ist.

## <a name="q-can-url-filters-matchjustdotless-host-names"></a>F: Können URL-Filter nur punktlosen Hostnamen entsprechen?

Nein. Sie müssen jeden gewünschten Hostnamen einzeln auflisten, z. B. ( `https://payroll`, `https://stock`, `https://who` usw.).

Wenn Sie soweit voraus gedacht haben und Ihr Intranet so zu strukturiert haben, dass Ihre Hostnamen folgendes Format haben:

- <div style="display: inline">`https://payroll.contoso-intranet.com`</div>

- <div style="display: inline">`https://timecard.contoso-intranet.com`</div>

- <div style="display: inline">`https://sharepoint.contoso-intranet.com`</div>

Herzlichen Glückwunsch, Sie haben eine bewährte Methode implementiert. Sie können jede gewünschte Richtlinie mit einem ***.contoso-intranet.com** Eintrag konfigurieren, und Ihr gesamtes Intranet wird registriert.

## <a name="use-of-security-zones-inthe-microsoft-edge"></a>Verwendung von Sicherheitszonen in Microsoft Edge

Während Microsoft Edge hauptsächlich auf einzelnen Richtlinien mit dem URL-Filterformat basiert, werden die Windows-Sicherheitszonen an wenigen Stellen weiterhin standardmäßig verwendet, um die Bereitstellung in Unternehmen zu vereinfachen, die in der Vergangenheit auf die Zonenkonfiguration angewiesen waren. Die folgenden Verhaltensweisen werden von der Zonenrichtlinie gesteuert:

1. Bei der Entscheidung, ob Windows Kerberos/NTLM-Anmeldeinformationen automatisch freigegeben werden sollen

2. Bei der Entscheidung, wie Dateidownloads behandelt werden sollen

3. Für den Internet Explorer-Modus

## <a name="credential-release"></a>Freigabe von Anmeldeinformationen

Microsoft Edge wertet URLACTION_CREDENTIALS_USE standardmäßig aus, um zu entscheiden, ob die integrierte Windows-Authentifizierung automatisch verwendet wird, oder ob der Benutzer stattdessen eine manuelle Authentifizierungsaufforderung sehen sollte. Durch das Konfigurieren einer [AuthServerAllowlist-Websitelistenrichtlinie](/deployedge/microsoft-edge-policies#authserverallowlist) wird verhindert, dass die Zonenrichtlinie abgefragt wird.

## <a name="file-downloads"></a>Dateidownloads

Ursprungsnachweise eines Dateidownloads (die so genannte "[Mark of the Web](https://textslashplain.com/2016/04/04/downloads-and-the-mark-of-the-web/)") werden für Dateien aufgezeichnet, die aus der Internetzone heruntergeladen wurden. Andere Anwendungen (z. B. Windows Shell, Microsoft Office usw.) können diesen Ursprungsnachweis berücksichtigen, wenn sie entscheiden, wie eine Datei behandelt werden soll.

Wenn die Windows-Sicherheitszonenrichtlinie so konfiguriert ist, dass die "Einstellung zum Starten von Anwendungen und unsicheren Dateien deaktiviert wird", blockiert der Microsoft Edge Download-Manager Dateidownloads von Websites in dieser Zone mit dem Hinweis: "Konnte nicht herunterladen – blockiert".  

## <a name="ie-mode"></a>IE-Modus

Der IE-Modus kann so konfiguriert werden, dass  [](/deployedge/edge-ie-mode#configure-all-intranet-sites)alle Intranetsites im IE-Modus öffnen [.](/deployedge/edge-ie-mode#configure-all-intranet-sites) Bei dieser Konfiguration wertet Edge die Zone einer URL aus, wenn entschieden wird, ob sie im IE-Modus geöffnet werden soll. Über diese anfängliche Entscheidung hinaus, führen tatsächlich Registerkarten im IE-Modus den Internet Explorer aus, und werten folglich Zoneneinstellungen für jede Richtlinienentscheidung so aus, wie es der Internet Explorer selbst getan hat.

## <a name="summary"></a>Zusammenfassung

In den meisten Fällen können Microsoft Edge-Einstellungen auf ihren Standardwerten belassen werden. Administratoren, die die Standardwerte für alle Websites oder bestimmte Websites ändern möchten, können die entsprechenden Gruppenrichtlinien verwenden, um Websitelisten oder Standardverhalten anzugeben. In einigen wenigen Fällen (Freigabe von Anmeldeinformationen, Dateidownload und IE-Modus) steuern weiterhin Administratoren das Verhalten, indem sie Windows-Sicherheitszoneneinstellungen konfigurieren.
