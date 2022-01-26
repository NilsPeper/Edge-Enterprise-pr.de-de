---
title: Konfiguration pro Standort nach Richtlinie
ms.author: collw
author: dan-wesley
manager: laurawi
ms.date: 01/04/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Konfiguration pro Standort nach Richtlinie
ms.openlocfilehash: 147f14fdd09f56161bf03ca88b5e6107ba9c88c5
ms.sourcegitcommit: e7f3098d8b7d91cae20b5778a71a87daababc312
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2022
ms.locfileid: "12297867"
---
# <a name="per-site-configuration-by-policy"></a>Konfiguration pro Standort nach Richtlinie

Dieser Artikel beschreibt die Konfigurationen pro Standort nach Richtlinie und wie der Browser Seitenladevorgänge von einer Website verarbeitet.

## <a name="the-browser-as-a-decision-maker"></a>Der Browser als Entscheidungsträger

Im Rahmen jedes Seitenladevorgangs treffen Browser viele Entscheidungen. Einige, aber nicht alle dieser Entscheidungen umfassen: ob eine bestimmte API verfügbar ist, ob eine Ressourcenlast zulässig ist und ob ein Skript ausgeführt werden darf.

In den meisten Fällen werden Browserentscheidungen durch die folgenden Eingaben gesteuert:

- Eine Benutzereinstellung
- Die URL der Seite, für die die Entscheidung getroffen wird

In der Internet Explorer-Webplattform wurde jede dieser Entscheidungen als URLAction bezeichnet. Weitere Informationen finden Sie unter [URL-Aktionsflags.](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537178%28v%3dvs.85%29) UrlAction, Enterprise Gruppenrichtlinie und Benutzereinstellungen in der Internetsystemsteuerung steuerten, wie der Browser die einzelnen Entscheidungen behandeln würde.  

In Microsoft Edge werden die meisten Berechtigungen pro Standort durch Einstellungen und Richtlinien gesteuert, die mithilfe einer einfachen Syntax mit eingeschränkter Platzhalterunterstützung ausgedrückt werden. Windows-Sicherheit Zonen werden weiterhin für einige Konfigurationsentscheidungen verwendet.

## <a name="windows-security-zones"></a>Windows-Sicherheit Zonen

Um die Konfiguration für den Benutzer oder Administrator zu vereinfachen, klassifizierte die Legacyplattform Websites in eine von fünf verschiedenen Sicherheitszonen. Diese Sicherheitszonen sind: lokaler Computer, lokales Intranet, vertrauenswürdig, Internet und eingeschränkte Websites.

Wenn Sie eine Entscheidung zum Laden einer Seite treffen, ordnet der Browser die Website einer Zone zu und sucht dann in der Einstellung für URLAction für diese Zone nach, um zu entscheiden, was sie tun soll. Angemessene Standardwerte wie "Automatische Erfüllung von Authentifizierungsproblemen aus meinem Intranet" bedeuten, dass die meisten Benutzer niemals Standardeinstellungen ändern müssen.

Benutzer können die Internetsystemsteuerung verwenden, um Zonen bestimmte Websites zuzuweisen und die Berechtigungsergebnisse für jede Zone zu konfigurieren. In verwalteten Umgebungen können Administratoren Gruppenrichtlinien verwenden, um Zonen bestimmte Websites zuzuweisen (über die Richtlinie "Site-to-Zone-Zuweisungsliste"), und die Einstellungen für URLActions auf Zonenbasis angeben. Neben der manuellen administrativen oder Benutzerzuweisung von Websites zu Zonen könnten andere Heuristiken [der Zone "Lokales Intranet" Websites zuweisen.](/archive/blogs/ieinternals/the-intranet-zone) Insbesondere wurden der Intranetzone punktlose Hostnamen `http://payroll` (z. B. ) zugewiesen. Wenn ein Proxykonfigurationsskript verwendet wurde, wurden alle Websites, die für die Umgehung des Proxys konfiguriert wurden, der Intranetzone zugeordnet.

Vorgängerversion von Microsoft Edge haben die Zonenarchitektur von ihrem Internet Explorer-Vorgänger mit einigen vereinfachenden Änderungen geerbt:

- Die fünf integrierten Windows-Zonen wurden auf drei reduziert: Internet (Internet), vertrauenswürdig (Intranet+ vertrauenswürdig) und lokaler Computer. Die Zone "Eingeschränkte Websites" wurde entfernt.
- Zonen-zu-URLAction-Zuordnungen wurden im Browser hartcodiert, wobei Gruppenrichtlinien und Einstellungen in der Internetsystemsteuerung ignoriert wurden.

## <a name="per-site-permissions-in-microsoft-edge"></a>Berechtigungen pro Website in Microsoft Edge

Microsoft Edge verwendet Windows-Sicherheit Zonen nur eingeschränkt. Stattdessen basieren die meisten Berechtigungen und Features, die Administratoren die Konfiguration pro Website per [Richtlinie](/deployedge/microsoft-edge-policies) bieten, auf Listen von Regeln im [URL-Filterformat.](/DeployEdge/edge-learnmmore-url-list-filter%20format)

Wenn Endbenutzer eine `edge://settings/content/siteDetails?site=https://example.com` Einstellungsseite wie diese öffnen, finden sie eine lange Liste von Konfigurationsoptionen und Listen für verschiedene Berechtigungen. Benutzer verwenden die Einstellungen Seite nur selten direkt, sondern treffen beim Browsen und verwenden verschiedene Widgets und Umschaltflächen in der **Dropdownliste "Seiteninformationen".**   Diese Liste wird angezeigt, wenn Sie das Sperrsymbol in der Adressleiste auswählen. Sie können auch die verschiedenen Eingabeaufforderungen oder Schaltflächen am rechten Rand der Adressleiste verwenden. Der nächste Screenshot zeigt ein Beispiel für Seiteninformationen.

:::image type="content" source="media/per-site-configuration-by-policy/edge-page-info.png" alt-text="Seiteninformationen und Einstellungen für die aktuelle Seite im Browser.":::

Unternehmen können Gruppenrichtlinien verwenden, um Websitelisten für einzelne Richtlinien einzurichten, die das Verhalten des Browsers steuern. Um diese Richtlinien zu finden, öffnen Sie die [Microsoft Edge Gruppenrichtliniendokumentation,](/deployedge/microsoft-edge-policies)   und suchen Sie nach "ForUrls", um die Richtlinien zu finden, die das Verhalten basierend auf der URL der geladenen Website zulassen und blockieren. Die meisten relevanten Einstellungen sind im Abschnitt ["Gruppenrichtlinie für Inhalte Einstellungen"](/deployedge/microsoft-edge-policies#content-settings) aufgeführt.

Es gibt auch viele Richtlinien (deren Namen "Default" enthalten), die das Standardverhalten für eine bestimmte Einstellung steuern.

Viele der Einstellungen sind verdeckt (WebSerial, WebMIDI), und es gibt häufig keinen Grund, eine Einstellung von der Standardeinstellung zu ändern.

## <a name="security-zones-inmicrosoft-edge"></a>Sicherheitszonen in Microsoft Edge

Während Microsoft Edge hauptsächlich auf einzelnen Richtlinien mithilfe des URL-Filterformats basiert, werden die Sicherheitszonen von Windows in einigen Fällen weiterhin standardmäßig verwendet. Dieser Ansatz vereinfacht die Bereitstellung in Unternehmen, die bisher auf der Zonenkonfiguration beruhten.

Die folgenden Verhaltensweisen werden von der Zonenrichtlinie gesteuert:

- Entscheidung, ob Windows Kerberos- oder NTLM-Anmeldeinformationen automatisch freigegeben werden sollen.
- Entscheiden, wie Dateidownloads behandelt werden sollen.
- Für den Internet Explorer-Modus.

## <a name="credential-release"></a>Freigabe von Anmeldeinformationen

Standardmäßig wird Microsoft Edge ausgewertet,  `URLACTION_CREDENTIALS_USE`  um zu entscheiden, ob Windows integrierte Authentifizierung automatisch verwendet wird oder ob dem Benutzer eine aufforderung zur manuellen Authentifizierung angezeigt wird. Durch das Konfigurieren der [AuthServerAllowlist-Websitelistenrichtlinie](/deployedge/microsoft-edge-policies#authserverallowlist) wird verhindert, dass die Zonenrichtlinie abgefragt wird.

## <a name="file-downloads"></a>Dateidownloads

Nachweise über die Ursprünge eines Dateidownloads (auch bekannt als["Mark des Webs"](https://textslashplain.com/2016/04/04/downloads-and-the-mark-of-the-web/)werden für Dateien aufgezeichnet, die aus der Internetzone heruntergeladen wurden. Andere Anwendungen, z. B. die Windows Shell und Microsoft Office können diesen Ursprungsnachweis berücksichtigen, wenn sie entscheiden, wie eine Datei behandelt werden soll.

Wenn die Windows-Sicherheit Zonenrichtlinie so konfiguriert ist, dass die Einstellung zum Starten von Anwendungen und zum Herunterladen unsicherer Dateien deaktiviert wird, blockiert der Download-Manager von Microsoft Edge Dateidownloads von Websites in dieser Zone. Ein Benutzer sieht diesen Hinweis: "Konnte nicht herunterladen – blockiert".  

## <a name="ie-mode"></a>IE-Modus

Der IE-Modus kann so konfiguriert werden, dass  [](/deployedge/edge-ie-mode#configure-all-intranet-sites)alle Intranetsites im IE-Modus öffnen [.](/deployedge/edge-ie-mode#configure-all-intranet-sites) Wenn Sie diese Konfiguration verwenden, wertet Microsoft Edge die Zone einer URL aus, wenn sie entscheidet, ob sie im IE-Modus geöffnet werden soll. Abgesehen von dieser anfänglichen Entscheidung werden Internet Explorer-Registerkarten im IE-Modus wirklich ausgeführt, und daher werten sie Zoneneinstellungen für jede Richtlinienentscheidung genauso aus wie Internet Explorer.

## <a name="summary"></a>Zusammenfassung

In den meisten Fällen können Microsoft Edge-Einstellungen auf ihren Standardwerten belassen werden. Administratoren, die die Standardwerte für alle Websites oder bestimmte Websites ändern möchten, können die entsprechenden Gruppenrichtlinien verwenden, um Websitelisten oder Standardverhalten anzugeben. In einigen wenigen Fällen, z. B. Veröffentlichung von Anmeldeinformationen, Dateidownload und IE-Modus, steuern Administratoren weiterhin das Verhalten, indem sie Windows-Sicherheit Zoneneinstellungen konfigurieren.

## <a name="frequently-asked-questions"></a>Häufig gestellte Fragen

### <a name="can-the-url-filter-format-match-on-a-sites-ip-address"></a>Kann das URL-Filterformat mit der IP-Adresse einer Website übereinstimmen?

Nein, das Format unterstützt nicht die Angabe eines IP-Bereichs für Zulassungs- und Blocklisten. Es unterstützt die Spezifikation einzelner **IP-Literale,** aber solche Regeln werden nur berücksichtigt, wenn der Benutzer mit dem angegebenen Literal zur Website navigiert (z. B. `http://127.0.0.1/` ). Wenn ein Hostname verwendet wird (`http://localhost`), wird die IP-Literalregel nicht berücksichtigt, obwohl die aufgelöste IP-Adresse des Hosts mit der IP-Adresse übereinstimmt, die in der Filterliste aufgeführt ist.

### <a name="can-url-filters-matchdotless-host-names"></a>Können URL-Filter punktlose Hostnamen abgleichen?

Nein. Sie müssen jeden Hostnamen auflisten, z. `https://payroll` `https://stock` B. , `https://who` usw.

Wenn Sie das Intranet so strukturiert haben, dass Ihre Hostnamen das folgende Format aufweisen, haben Sie eine bewährte Methode implementiert.

- `https://payroll.contoso-intranet.com`

- `https://timecard.contoso-intranet.com`

- `https://sharepoint.contoso-intranet.com`

Im vorherigen Szenario können Sie jede Richtlinie mit einem ***CONTOSO-INTRANET.COM**   Eintrag konfigurieren, und Ihr gesamtes Intranet wird aktiviert.

## <a name="see-also"></a>Weitere Informationen:

- [Dokumentation für Microsoft Edge](./index.yml)
- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)
