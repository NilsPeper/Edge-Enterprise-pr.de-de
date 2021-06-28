---
title: Filterformat für Microsoft Edge-URL-Richtlinien
ms.author: brianalt
author: dan-wesley
manager: srugh
ms.date: 05/01/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Hier finden Sie Informationen zum Filterformat, das für Microsoft Edge URLBlocklist- und URLAllowlist-Richtlinien verwendet wird.
ms.openlocfilehash: 94378a9193269c73a7439dd019d6cb2d6ac547df
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2021
ms.locfileid: "11617265"
---
# <a name="filter-format-for-url-list-based-policies"></a>Filterformat für URL-listenbasierte Richtlinien

In diesem Artikel wird das Filterformat beschrieben, das für die Microsoft Edge URL-listenbasierten Richtlinien verwendet wird (zum Beispiel Richtlinien für [URLBlocklist](microsoft-edge-policies.md#urlblocklist), [URLAllowList](microsoft-edge-policies.md#urlallowlist) und [CertificateTransparencyEnforcementDisabledForUrls](microsoft-edge-policies.md#certificatetransparencyenforcementdisabledforurls).

> [!NOTE]
> Dieser Artikel bezieht sich auf Microsoft Edge Version 77 oder höher.

## <a name="the-filter-format"></a>Das Filterformat

Das Filterformat ist:

```
    [scheme://][.]host[:port][/path][@query]
```

Die Felder im Filterformat sind:

| Feld | Beschreibung |
| --- | --- |
| **Schema** (*optional*) | Dabei kann es sich um http://, https://, FTP://, edge:// usw. handeln. |
| **Host** (*erforderlich*) | Es muss sich um einen gültigen Hostnamen handeln und Sie können einen Platzhalter ("\*") verwenden. Um den Unterdomänenabgleich zu deaktivieren, fügen Sie vor dem **Host** einen optionalen Punkt (".") ein. Es kann ein einzelner IP-Adressliteral-Hostname angegeben werden, aber Platzhalter werden für einen IP-Adressliteral-Hostnamen nicht unterstützt. |
| **Port** (*optional*) | Gültige Werte liegen zwischen 1 und 65535. |
| **Pfad** (*optional*) | Sie können eine beliebige Zeichenfolge im Pfad verwenden. |
| **Abfrage** (*optional*) | Bei der **Abfrage** handelt es sich entweder um einen Schlüsselwert oder ein Nur-Schlüssel-Token, die durch ein kaufmännisches Und-Zeichen("&") getrennt sind. Trennen Sie Schlüsselwert-Token mit einem Gleichheitszeichen ("="). Um eine Präfixübereinstimmung anzugeben, können Sie am Ende der **Abfrage** ein Sternchen ("\*") verwenden. |

## <a name="comparing-the-filter-format-to-the-url-format"></a>Vergleichen des Filterformats mit dem URL-Format

Das Filterformat ähnelt dem URL-Format mit Ausnahme der folgenden Unterschiede:

- Wenn Sie "user:pass" angeben, wird es ignoriert. Beispiel: http://user:pass@ftp.contoso.com/pub/example.iso.
- Wenn Sie einen Fragmentbezeichner ("#") einfügen, wird dieser und alles, was auf den Bezeichner folgt, ignoriert.
- Sie können einen Platzhalter ("*") als **Host** verwenden und ihm einen Punkt (".") voranstellen.
- Sie können einen Schrägstrich (/") oder einen Punkt (".") als Suffix für den **Host** verwenden. In diesem Fall wird das Suffix ignoriert.

## <a name="filter-selection-criteria"></a>Kriterien für die Filterauswahl

Der für eine URL ausgewählte Filter ist die spezifischste Übereinstimmung, die nach Verarbeitung der folgenden Filterauswahlregeln gefunden wurde:

1. Filter mit der längsten **Host**-Übereinstimmung werden zuerst ausgewählt.
2. Aus den ausgewählten Filtern werden alle Filter mit einem nicht übereinstimmenden Schema oder Port verworfen.
3. Aus den verbleibenden Filtern wird der Filter mit dem längsten übereinstimmenden **Pfad** ausgewählt.
4. Aus den verbleibenden Filtern wird der Filter mit dem längsten Satz von Abfragetoken ausgewählt. In diesem Schritt hat der Zulassungslistenfilter Vorrang vor dem Sperrlistenfilter, wenn beide Filter die gleiche **Pfadlänge** und Anzahl von **Abfragetoken** aufweisen.
5. Wenn kein gültiger Filter mehr vorhanden ist, wird die Subdomäne ganz links vom **Host** entfernt, und der Auswahlprozess beginnt bei Schritt 1 von vorne. Der **Host** mit dem speziellen Sternchen ("*") ist der zuletzt gesuchte Host, der mit allen Hosts übereinstimmt.
6. Wenn ein Filter verfügbar ist, wird die URL-Anforderung blockiert oder zugelassen.

   >[!NOTE]
   >Das Standardverhalten besteht darin, die URL-Anforderung zuzulassen, wenn keine Übereinstimmung mit einem Filter vorliegt.

## <a name="example-filter-selection-criteria"></a>Beispiel für Kriterien für die Filterauswahl

In diesem Beispiel führt die Filterauswahl bei der Suche nach einer Übereinstimmung mit "https://sub.contoso.com/docs" Folgendes aus:

1. Suchen nach einem Filter für „sub.contoso.com”. Wenn ein Filter gefunden wird, wird die Suche mit Schritt2 fortgesetzt. Wenn ein Filter nicht gefunden wird, wird die Suche erneut mit "contoso.com", "com" und schließlich "" versucht.
2. Aus den ausgewählten Filtern werden alle, die im **Schema** nicht über "http" verfügen, entfernt.
3. Aus den verbleibenden Filtern werden alle, die über eine genaue Portnummer verfügen, die nicht "80" ist, entfernt.
4. Aus den übrigen Filtern werden alle, die nicht „/docs” als Präfix des **Pfads** haben, entfernt.
5. Aus den verbleibenden Filtern wird der Filter mit dem längsten Pfadpräfix ausgewählt und angewendet. Wird kein Filter gefunden, beginnt der Auswahlprozess erneut bei Schritt 1. Der Prozess wird mit der nächsten Unterdomäne wiederholt.

### <a name="additional-filter-information"></a>Zusätzliche Filterinformationen

Wenn ein Filter einen Punkt (".") enthält, der dem **Host** vorangestellt ist, werden nur exakte **Host-Übereinstimmungen** gefiltert. Zum Beispiel:

- "contoso.com" (kein Punkt) stimmt mit "contoso.com", "www.contoso.com" und "sub.www.contoso.com" überein.
- ".www.contoso.com" (mit einem Punkt als Präfix) stimmt nur mit "www.contoso.com" überein.

Sie können entweder ein Standardschema oder ein benutzerdefiniertes **Schema**verwenden. Unterstützte Standardschemata sind:

- _about_, _blob_, _content_, _edge_, _cid_, _data_, _file_, _filesystem_, _ftp_, _gopher_, _http_, _https_, _javascript_, _mailto_, _ws_, und _wss_.

Jedes andere **Schema** wird als benutzerdefiniertes **Schema** behandelt, wobei nur die Muster _Schema:*_ und _schema://*_ zulässig sind. Zum Beispiel:

- "custom:\*" oder "custom://\*" entspricht "custom:app".
- "custom:app" bzw. "custom://app" sind ungültig.

Bei **Schema** und **Host** wird die Groß-/Kleinschreibung nicht beachtet. Zum Beispiel:

- Der Filter "http://contoso.com" stimmt mit "HTTP://contoso.com", "http://contoso.COM" und "http://contoso.com" überein.

Bei **Pfad** und **Abfrage** wird die Groß-/Kleinschreibung beachtet. Zum Beispiel:

- Der Filter "http://contoso.com/path?query=A" stimmt weder mit "http://contoso.com/Path?query=A" noch mit "http://contoso.com/path?Query=A" überein. Er stimmt mit "http://contoso.COM/path?query=A" überein.

## <a name="content-license"></a>Lizenz für Inhalte

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf von Chromium.org erstellten und freigegebenen Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/) beschriebenen Begriffen verwendet werden. Die Originalseite von [Chromium finden Sie hier](https://www.chromium.org/administrators/url-blacklist-filter-format).
  
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />Diese Arbeit unterliegt einer <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)
