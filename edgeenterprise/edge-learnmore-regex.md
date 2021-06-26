---
title: Regulärer Ausdruck 2 Syntax
ms.author: comanea
author: dan-wesley
manager: seanlyn
ms.date: 06/09/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Regulärer Ausdruck 2 Syntax
ms.openlocfilehash: 5d7026a034300e098497c63911f7516f72877c5d
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2021
ms.locfileid: "11617315"
---
# <a name="regular-expression-2-re2h-syntax"></a>Regulärer Ausdruck 2 (re2.h), Syntax

Reguläre Ausdrücke sind eine Notation zur Beschreibung von Gruppen von Zeichenfolgen. Wenn sich eine Zeichenfolge in der durch einen regulären Ausdruck beschriebenen Gruppe befindet, wird häufig davon gesprochen, dass der reguläre Ausdruck der Zeichenfolge entspricht.

Der einfachste reguläre Ausdruck ist ein einzelnes Literalzeichen. Außer bei Metazeichen wie *\ * +? ()|* entsprechen die Zeichen einander. Um einem Metazeichen zu entsprechen, können Sie es mit einem umgekehrten Schrägstrich ausgleichen: \+ entspricht einem Literal-Pluszeichen.

Zwei reguläre Ausdrücke können geändert oder verkettet werden, um einen neuen regulären Ausdruck zu erstellen: Wenn e1 mit s und e2 mit t übereinstimmt, stimmt e1e2 mit s oder t überein und *e<sub>1</sub>* *e<sub>2</sub>* mit _st_.

Die Metazeichen _\*_ , _+_ und _?_ sind Wiederholungsoperatoren: *e<sub>1</sub>* _\*_ stimmt mit einer Sequenz von null oder mehreren (möglicherweise unterschiedlichen) Zeichenfolgen überein, die jeweils mit *e<sub>1</sub>* übereinstimmen; *e<sub>1</sub>* _+_ stimmen mit einer oder mehreren überein; *e<sub>1</sub>* _?_ stimmt mit null oder einer überein.

Die Rangfolge des Operators von der schwächsten zur stärksten Bindung, lautet zuerst Alternierung, dann Verkettung und schließlich Wiederholungsoperatoren. Explizite Klammern können, genau wie in arithmetischen Ausdrücken, verwendet werden, um unterschiedliche Bedeutungen zu erzwingen. Einige Beispiele: ab|cd entspricht (ab)|(cd); _ab\*_ entspricht _a(b\*)_ .

Die bisher beschriebene Syntax entspricht zum größten Teil der herkömmlichen _egrep_-Syntax regulärer Ausdrücke in UNIX. Diese Teilmenge reicht aus, um alle regulären Sprachen zu beschreiben: vereinfacht gesagt ist eine reguläre Sprache eine Reihe von Zeichenfolgen, die in einem einzigen Durchlaufen des Texts mit nur einer festen Menge an Speicher abgeglichen werden können. Neuere Einrichtungen für reguläre Ausdrücke (insbesondere Perl und solche, die diese kopiert haben) haben viele neue Operatoren und Escapesequenzen hinzugefügt, wodurch die regulären Ausdrücke präziser und manchmal kryptischer, aber in der Regel nicht mächtiger werden.

Auf dieser Seite wird die Syntax regulärer Ausdrücke aufgelistet, die von RE2 akzeptiert wird.

Außerdem finden Sie Syntax, die von PCRE, PERL und VIM akzeptiert wird.

## <a name="syntax-tables"></a>Syntaxtabellen

| Arten von Ausdrücken, die aus einem einzelnen Zeichen bestehen | Beispiele |
| --- | --- |
| ein beliebiges Zeichen, das möglicherweise ein Zeilenumbruch einschließt (s = wahr) | . |
| Zeichenklasse | [xyz] |
| negierte Zeichenklasse | [^xyz] |
| Perl-Zeichenklasse ([link](#user-content-perl)) | \d |
| negierte Perl-Zeichenklasse | \D |
| ASCII-Zeichenklasse ([link](#user-content-ascii)) | [[:alpha:]] |
| negierte ASCII-Zeichenklasse | [[:^alpha:]] |
| Unicode-Zeichenklasse (einbuchstabiger Name) | \pN |
| Unicode-Zeichenklasse | \p{Greek} |
| negierte Unicode-Zeichenklasse (einbuchstabiger Name) | \PN |
| negierte Unicode-Zeichenklasse | \P{Greek} |

|&nbsp;| Composites |
| --- | --- |
| xy | x, gefolgt von y |
| x\|y | x oder y (x bevorzugen) |

|&nbsp;| Wiederholungen |
| --- | --- |
| x\* | null oder mehr x (mehr bevorzugen) |
| x+ | ein oder mehrere x, mehrere bevorzugen |
| x? | null oder ein x, ein x bevorzugen |
| x{n,m} | n oder n+1 oder … m x, mehrere bevorzugen |
| x{n,} | n oder mehrere x, mehrere bevorzugen |
| x{n} | genau n x |
| x\*? | null oder mehr x, (weniger bevorzugen) |
| x+? | ein oder mehr x, weniger bevorzugen |
| x?? | null oder ein x, null bevorzugen |
| x{n,m}? | n oder n+1 oder … m x, weniger bevorzugen |
| x{n,}? | no der mehr x, weniger bevorzugen |
| x{n}? | genau n x |
| x{} | (≡ x\*) (NICHT UNTERSTÜTZT) VIM |
| x{-} | (≡ x\*?) (NOT UNTERSTÜTZT) VIM |
| x{-n} | (≡ x{n}?) (NICHT UNTERSTÜTZT) VIM |
| x= | (≡ x?) (NICHT UNTERSTÜTZT) VIM |

Implementierungseinschränkung: die Zählformen x{n,m}, x{n,} und x{n} weisen Formen zurück, die eine minimale oder maximale Wiederholungszahl über 1.000 erzeugen. Unbegrenzte Wiederholungen unterliegen dieser Einschränkung nicht.

|&nbsp;| Possessive Wiederholungen |
| --- | --- |
| x\*+ | null oder mehre x, possessiv (NICHT UNTERSTÜTZT) |
| x++ | ein oder mehre x, possessiv (NICHT UNTERSTÜTZT) |
| x?+ | null oder ein x, possessiv (NICHT UNTERSTÜTZT) |
| x {n, m} + | n oder … oder m x, possessiv (NICHT UNTERSTÜTZT) |
| x {n,} + | n oder mehre x, possessiv (NICHT UNTERSTÜTZT) |
| x{n}+ | genau n x, possessiv (NICHT UNTERSTÜTZT) |

|&nbsp;| Gruppierung |
| --- | --- |
| (re) | nummerierte Erfassungsgruppe (Teilübereinstimmung) |
| (? P&lt;name&gt;re) | benannte &amp; nummerierte Erfassungsgruppe (Teilübereinstimmung) |
| (?&lt;name&gt;re) | benannte &amp; nummerierte Erfassungsgruppe (Teilübereinstimmung) (NICHT UNTERSTÜTZT) |
| (?&#39;name&#39;re) | benannte &amp; nummerierte Erfassungsgruppe (Teilübereinstimmung) (NICHT UNTERSTÜTZT) |
| (?:re) | nicht erfassende Gruppe |
| (?flags) | Flags innerhalb der aktuellen Gruppe setzen; nicht erfassend |
| (?flags:re) | Flags während re setzen; nicht erfassend |
| (?#text) | Kommentar (NICHT UNTERSTÜTZT) |
| (?\|x\|y\|z) | Zurücksetzen von Zweignummerierungen (NICHT UNTERSTÜTZT) |
| (?&gt;re) | possessive Übereinstimmung von re (NICHT UNTERSTÜTZT) |
| re@&gt; | possessive Übereinstimmung von re (NICHT UNTERSTÜTZT) VIM |
| %(re) | nicht erfassende Gruppe (NICHT UNTERSTÜTZT) VIM |

|&nbsp;| Flags |
| --- | --- |
| i | Groß-/Kleinschreibung wird nicht beachtet (Standard: falsch) |
| m | Mehrzeilenmodus: ^ und $ stimmen zusätzlich zum Anfang- und Endtext mit der Anfangs- und Endzeile überein (Standard: falsch) |
| s | lassen. \n zuordnen (Standard falsch) |
| U | nicht gierig: Swap-Bedeutung von x\* und x\*?, x+ und x+?, usw. (Standard: falsch) |

Die Flag-Syntax lautet xyz (festlegen) oder-xyz (löschen) oder xy-z (xy festlegen, z löschen).

|&nbsp;| Leere Zeichenfolgen |
| --- | --- |
| ^ | am Text- oder Zeilenanfang (m = wahr) |
| $ | am Textende (z. B. \z nicht \Z) oder Zeilenende (m = wahr) |
| \A | am Textanfang |
| \b | bei ASCII-Wortgrenze (\w auf einer Seite und \W, \A oder \Z auf der anderen) |
| \B | nicht bei ASCII-Wortgrenze |
| \g. | am Anfang des gerade durchsuchten Subtexts (NICHT UNTERSTÜTZT) PCRE |
| \G | am Ende der letzten Übereinstimmung (NICHT UNTERSTÜTZT) PERL |
| \Z | am Textende oder vor dem Zeilenumbruch am Ende des Texts (NICHT UNTERSTÜTZT) |
| \z | am Textende |
| (?=re) | vor dem mit re übereinstimmenden Text (NICHT UNTERSTÜTZT) |
| (?!re) | vor dem nicht mit re übereinstimmenden Text (NICHT UNTERSTÜTZT) |
| (?&lt;=re) | nach dem mit re übereinstimmenden Text (NICHT UNTERSTÜTZT) |
| (?&lt;!re) | nach dem nicht mit re übereinstimmenden Text (NICHT UNTERSTÜTZT) |
| &amp;re | vor dem mit re übereinstimmenden Text (NICHT UNTERSTÜTZT) VIM |
| re@= | vor dem mit re übereinstimmenden Text (NICHT UNTERSTÜTZT) VIM |
| re@! | vor dem nicht mit re übereinstimmenden Text (NICHT UNTERSTÜTZT) VIM |
| re@&lt;= | nach dem mit re übereinstimmenden Text (NICHT UNTERSTÜTZT) VIM |
| re@&lt;! | nach dem nicht mit re übereinstimmenden Text (NICHT UNTERSTÜTZT) VIM |
| \zs | legt den Anfang der Übereinstimmung fest (= \K) (NICHT UNTERSTÜTZT) VIM |
| \ze | legt Ende der Übereinstimmung fest (NICHT UNTERSTÜTZT) VIM |
| \%^ | Anfang der Datei (NICHT UNTERSTÜTZT) VIM |
| \%$ | Ende der Datei (NICHT UNTERSTÜTZT) VIM |
| \%V | auf dem Bildschirm (NICHT UNTERSTÜTZT) VIM |
| \%# | Cursorposition (NICHT UNTERSTÜTZT) VIM |
| \%&#39;m | Position der m-Markierung (NICHT UNTERSTÜTZT) VIM |
| \%23l | in Zeile 23 (NICHT UNTERSTÜTZT) VIM |
| \%23c | in Spalte 23 (NICHT UNTERSTÜTZT) VIM |
| \%23v | in virtueller Spalte 23 (NICHT UNTERSTÜTZT) VIM |

|&nbsp;| Escapesequenzen |
| --- | --- |
| \a | Bell (≡ \007) |
| \f | Seitenvorschub (≡ \014) |
| \t | Horizontal-Tabulator (≡ \011) |
| \n | Zeilenumbruch (≡ \012) |
| \r | Wagenrücklauf (≡ \015) |
| \v | vertikales Tabstoppzeichen (≡ \013) |
| \* | literal \* für jedes Interpunktionszeichen \* |
| \123 | oktaler Zeichencode (bis zu drei Ziffern) |
| \x7F | hexadezimaler Zeichencode (genau zwei Ziffern) |
| \x{10FFFF} | hexadezimaler Zeichencode |
| \C | Übereinstimmung mit einem einzelnen Byte sogar im UTF-8-Modus |
| \Q...\E | Literaltext …selbst wenn …hat Interpunktion |
| \1 | Rückverweis (NICHT UNTERSTÜTZT) |
| \b | Rücktaste (NICHT UNTERSTÜTZT) (\010 verwenden) |
| \cK | Steuerelement char^ K (NICHT UNTERSTÜTZT) (\001 usw. verwenden) |
| \e | Escape (NICHT UNTERSTÜTZT) (\033 verwenden) |
| \g1 | Rückverweis (NICHT UNTERSTÜTZT) |
| \g{1} | Rückverweis (NICHT UNTERSTÜTZT) |
| \g{+1} | Rückverweis (NICHT UNTERSTÜTZT) |
| \g{-1} | Rückverweis (NICHT UNTERSTÜTZT) |
| \g{name} | benannter Rückverweis (NICHT UNTERSTÜTZT) |
| \g&lt;name&gt; | Unterroutinenaufruf (NICHT UNTERSTÜTZT) |
| \g&#39;name&#39; | Unterroutinenaufruf (NICHT UNTERSTÜTZT) |
| \k&lt;name&gt; | benannter Rückverweis (NICHT UNTERSTÜTZT) |
| \k&#39;name&#39; | benannter Rückverweis (NICHT UNTERSTÜTZT) |
| \lX | X als Kleinbuchstabe (NICHT UNTERSTÜTZT) |
| \ux | X als Großbuchstabe (NICHT UNTERSTÜTZT) |
| \L...\E | Text in Kleinbuchstaben (NICHT UNTERSTÜTZT) |
| \K | Zurücksetzen des Anfangs von $0 (NICHT UNTERSTÜTZT) |
| \N{name} | benanntes Unicode-Zeichen (NICHT UNTERSTÜTZT) |
| \R | Zeilenumbruch (NICHT UNTERSTÜTZT) |
| \U...\E | Text in Großbuchstaben (NICHT UNTERSTÜTZT) |
| \X | erweiterte Unicode-Sequenz (NICHT UNTERSTÜTZT) |
| \%d123 | Dezimalzeichen 123 (NICHT UNTERSTÜTZT) VIM |
| \%xFF | Hexadezimalzeichen FF (NICHT UNTERSTÜTZT) VIM |
| \%o123 | Oktales Zeichen 123 (NICHT UNTERSTÜTZT) VIM |
| \%u1234 | Unicode-Zeichen 0x1234 (NICHT UNTERSTÜTZT) VIM |
| \%U12345678 | Unicode-Zeichen 0x12345678 (NICHT UNTERSTÜTZT) VIM |

|&nbsp;| Zeichenklassenelemente |
| --- | --- |
| x | einzelnes Zeichen |
| A-Z | Zeichenbereich (einschließlich) |
| \d | Perl-Zeichenklasse |
| [:foo:] | ASCII-Zeichenklasse foo |
| \p{Foo} | Unicode-Zeichenklasse Foo |
| \pF | Unicode-Zeichenklasse F (einbuchstabiger Name) |

|&nbsp;| Benannte Zeichenklassen als Zeichenklassenelemente |
| --- | --- |
| [\d] | Ziffern (≡ \d) |
| [^\d] | keine Ziffern (≡ \D) |
| [\D] | keine Ziffern (≡ \D) |
| [^\D] | nur Ziffern (doppelt verneint) (≡ \d) |
| [[:name:]] | benannte ASCII-Klasse innerhalb der Zeichenklasse (≡ [:name:]) |
| [^[:name:]] | benannte ASCII-Klasse innerhalb negierter Zeichenklasse (≡ [:^name:]) |
| [\p{Name}] | benannte Unicode-Eigenschaft innerhalb der Zeichenklasse (≡ \p{Name}) |
| [^\p{Name}] | benannte Unicode-Eigenschaft innerhalb der negierten Zeichenklasse (≡ \P{Name}) |

| <a name="user-content-perl"></a> | Perl-Zeichenklassen (alle nur in ASCII-Format) |
| --- | --- |
| \d | Ziffern (≡ [0-9]) |
| \D | keine Ziffern (≡ [0-9]) |
| \s | Leerraumzeichen (≡ [\t\n\f\r]) |
| \S | kein Leerzeichen (≡ [^\t\n\f\r]) |
| \w | Wortzeichen (≡ [0-9A-Za-z\_]) |
| \W | keine Wortzeichen (≡ [0-9A-Za-z\_]) |
| \h | horizontaler Abstand (NICHT UNTERSTÜTZT) |
| \H | kein horizontaler Abstand (NICHT UNTERSTÜTZT) |
| \v | vertikaler Abstand (NICHT UNTERSTÜTZT) |
| \V | kein vertikaler Abstand (NICHT UNTERSTÜTZT) |

|<a name="user-content-ascii"></a>  | ASCII-Zeichenklassen |
| --- | --- |
| [[:alnum:]] | alphanumerisch (≡ [0-9A-Za-z]) |
| [[:alpha:]] | alphabetisch (≡ [A-Za-z]) |
| [[:ascii:]] | ASCII (≡ [\x00-\x7F]) |
| [[:blank:]] | blank (≡ [\t]) |
| [[:cntrl:]] | Steuerelement (≡ [\x00-\x1F\x7F]) |
| [[:digit:]] | Ziffern (≡ [0-9]) |
| [[:graph:]] | grafisch (≡ `[!-~]` ≡ `[A-Za-z0-9!&quot;#$%&amp;&#39;()\*+,\-./:;&lt;=&gt;?@[\\\]^_`\` `{\|}~]`) |
| [[:lower:]] | Kleinbuchstaben (≡ [a-z]) |
| [[:print:]] | druckbar (≡ [-~] ≡ [[:graph:]]) |
| [[:punct:]] | Zeichensetzung (≡ [!-/:-@[-`{-~]) |
| [[:space:]] | Leerraumzeichen (≡ [\t\n\v\f\r]) |
| [[:upper:]] | Großbuchstaben (≡ [A-Z]) |
| [[:word:]] | Wortzeichen (≡ [0-9A-Za-z\_]) |
| [[:xdigit:]] | Hexadezimalziffer (≡ [0-9A-Fa-f]) |

|&nbsp;| Unicode-Zeichenklassennamen – allgemeine Kategorie |
| --- | --- |
| C | andere |
| Cc | control |
| Cf | format |
| Cn | nicht zugewiesene Codepunkte (NICHT UNTERSTÜTZT) |
| Co | private Nutzung |
| Cs | Ersatz |
| L | Buchstabe |
| LC | Großbuchstabe (nicht unterstützt) |
| L&amp; | Großbuchstabe (nicht unterstützt) |
| Ll | Kleinbuchstabe |
| Lm | Modifiziererbuchstabe |
| Lo | anderer Buchstabe |
| Lt | Titelschriftbuchstabe |
| Lu | Großbuchstabe |
| M | Markierung |
| Mc | Zeichenabstandsmarkierung |
| Me | Einschlusszeichen |
| Mn | Zeichen ohne Zwischenraum |
| N | number |
| Nd | Dezimalzahl |
| Nl | Buchstabe Zahl |
| Nein | andere Zahl |
| P | Zeichensetzung |
| Pc | Verbinder-Interpunktionszeichen |
| Pd | Gedankenstrich-Interpunktionszeichen |
| Pe | Schließendes Interpunktionszeichen |
| Pf | Abschließendes Interpunktionszeichen |
| Pi | Beginnendes Interpunktionszeichen |
| Po | andere Zeichensetzung |
| Ps | offene Zeichensetzung |
| E | symbol |
| Sc | Währungssymbol |
| Sk | Modifizierersymbol |
| Sm | Mathematisches Symbol |
| So | anderes Symbol |
| Z | Trennzeichen |
| Zl | Zeilentrennzeichen |
| Zp | Absatztrennzeichen |
| Zs | Leerzeichentrennzeichen |

| Unicode-Zeichenklassennamen – Skripte |
| --- |
| Adlam |
| Ahom |
| Anatolisch\_Hieroglyphen |
| Arabisch |
| Armenisch |
| Avestan |
| Balinesisch |
| Bamum |
| Bassa\_Vah |
| Batak |
| Bengali |
| Bhaiksuki |
| Bopomofo |
| Brahmi |
| Braille |
| Buginese |
| Buhid |
| Kanadisch\_Ureinwohner |
| Karisch |
| Kaukasisch\_Albanisch |
| Chakma |
| Cham |
| Cherokee |
| Chorasmian |
| Allgemein |
| Koptisch |
| Cuneiform |
| Zyprisch |
| Kyrillisch |
| Deseret |
| Devanagari |
| Dives\_Akuru |
| Dogra |
| Duployé-Kurzschrift |
| Ägyptisch\_Hieroglyphen |
| Elbasan |
| Elymaisch |
| Äthiopisch |
| Georgisch |
| Glagolitisch |
| Gothic |
| Grantha |
| Griechisch |
| Gujarati |
| Gunjala\_Gondi |
| Gurmukhi |
| Han |
| Hangul |
| Hanifi\_Rohingya |
| Hanunoo |
| Hatran |
| Hebräisch |
| Hiragana |
| Reichsaramäisch |
| Geerbt |
| Inschriften-Pahlavi |
| Inschriften-Parthisch |
| Javanisch |
| Kaithi |
| Kannada |
| Katakana |
| Kayah\_Li |
| Kharoshthi |
| Khitan\_Small\_Script |
| Khmer |
| Khojki |
| Khudawadi |
| Laotisch |
| Lateinisch |
| Lepcha |
| Limbu |
| Linear\_A |
| Linear\_B |
| Lisu |
| Lykisch |
| Lydisch |
| Mahajani |
| Makasar |
| Malayalam |
| Mandäisch |
| Manichäisch |
| Marchen |
| Masaram\_Gondi |
| Medefaidrin |
| Meetei\_Mayek |
| Mende\_Kikakui |
| Meroitische\_Kursiv |
| Meroitisch\_Hieroglyphen |
| Miao |
| Modi |
| Mongolisch |
| Mro |
| Multani |
| Myanmar |
| Nabatäisch |
| Nandinagari |
| Neu-Tai-Lue |
| Newa |
| Nko |
| Nushu |
| Nyiakeng\_Puachue\_Hmong |
| Ogham |
| Ol\_Chiki |
| Altungarisch |
| Altitalienisch |
| Altnordarabisch |
| Altpermisch |
| Altpersisch |
| Altsogdisch |
| Altsüdarabisch |
| Alttürkisch |
| Odia |
| Osage |
| Osmanisch |
| Pahawh\_Hmong |
| Palmyrenisch |
| Pau\_Cin\_Hau |
| Phags\_Pa |
| Phönizisch |
| Psalter\_Pahlavi |
| Rejang |
| Runisch |
| Samaritanisch |
| Saurashtra |
| Sharada |
| Shaw-Alphabet |
| Siddham |
| Gebärdensprache |
| Sinhala |
| Sogdisch |
| Sora\_Sompeng |
| Soyombo |
| Sundanesisch |
| Syloti\_Nagri |
| Syrisch |
| Tagalog |
| Tagbanwa |
| Tai\_Le |
| Tai\_Tham |
| Tai\_Viet |
| Takri |
| Tamil |
| Tangutisch |
| Telugu |
| Thaana |
| Thailändisch |
| Tibetisch |
| Tifinagh |
| Tirhuta |
| Ugaritisch |
| Vai |
| Wancho |
| Warang\_Citi |
| Jesidisch |
| Yi |
| Zanabazar\_Square |

|&nbsp;| VIM-Zeichenklasse |
| --- | --- |
| \i | Kennungszeichen (NICHT UNTERSTÜTZT) VIM |
| \I | \i mit Ausnahme von Ziffern (NICHT UNTERSTÜTZT) VIM |
| \k | Schlüsselwortzeichen (NICHT UNTERSTÜTZT) VIM |
| \K | \k mit Ausnahme von Ziffern (NICHT UNTERSTÜTZT) VIM |
| \f | Dateinamenzeichen (NICHT UNTERSTÜTZT) VIM |
| \F | \f mit Ausnahme von Ziffern (NICHT UNTERSTÜTZT) VIM |
| \p | druckbares Zeichen (NICHT UNTERSTÜTZT) VIM |
| \P | \p mit Ausnahme von Ziffern (NICHT UNTERSTÜTZT) VIM |
| \s | Leerraumzeichen (≡ [\t]) (NICHT UNTERSTÜTZT) VIM |
| \S | kein Leerraumzeichen (≡ [^ \t]) (NICHT UNTERSTÜTZT) VIM |
| \d | Ziffern (≡ [0-9]) VIM |
| \D | nicht \d VIM |
| \x | Hexadezimalziffern (≡ [0-9a-FA-f]) (NICHT UNTERSTÜTZT) VIM |
| \X | nicht \x (NICHT UNTERSTÜTZT) VIM |
| \o. | oktale Ziffern (≡ [0-7]) (NICHT UNTERSTÜTZT) VIM |
| \O | nicht \o (NICHT UNTERSTÜTZT) VIM |
| \w | Wortzeichen VIM |
| \W | nicht \w VIM |
| \h | Kopf eines Wortzeichens (NICHT UNTERSTÜTZT) VIM |
| \H | nicht \h (NICHT UNTERSTÜTZT) VIM |
| \a | alphabetisch (NICHT UNTERSTÜTZT) VIM |
| \A | nicht \a (NICHT UNTERSTÜTZT) VIM |
| \l | Kleinbuchstaben (NICHT UNTERSTÜTZT) VIM |
| \L | keine Kleinbuchstaben (NICHT UNTERSTÜTZT) VIM |
| \u | Großschreibung (NICHT UNTERSTÜTZT) VIM |
| \U | keine Großschreibung (NICHT UNTERSTÜTZT) VIM |
| _x | \x und Zeilenumbruch für jedes x (NICHT UNTERSTÜTZT) VIM |
| \c | Groß-/Kleinschreibung ignorieren (NICHT UNTERSTÜTZT) VIM |
| \C | Groß-/Kleinschreibung anpassen(NICHT UNTERSTÜTZT) VIM |
| \m | magic (NICHT UNTERSTÜTZT) VIM |
| \M | nomagic (NICHT UNTERSTÜTZT) VIM |
| \v | verymagic (NICHT UNTERSTÜTZT) VIM |
| \V | verynomagic (NICHT UNTERSTÜTZT) VIM |
| \Z | Unterschiede bei Unicode-Zeichenkombinationen ignorieren (NICHT UNTERSTÜTZT) VIM |

| &nbsp; | Magic |
| --- | --- |
| (?{code}) | beliebiger Perl-Code (NICHT UNTERSTÜTZT) PERL |
| (??{code}) | zurückgestellter, beliebiger Perl-Code (NICHT UNTERSTÜTZT) PERL |
| (?n) | rekursive Aufruf von regexp-Erfassungsgruppe n (NICHT UNTERSTÜTZT) |
| (?+n) | rekursive Aufruf von relativer Gruppe +n (NICHT UNTERSTÜTZT) |
| (?-n) | rekursive Aufruf von relativer Gruppe -n (NICHT UNTERSTÜTZT) |
| (?C) | PCRE-Callout (NICHT UNTERSTÜTZT) PCRE |
| (?R) | rekursive Aufruf von gesamter regexp (≡ (?0)) (NICHT UNTERSTÜTZT) |
| (?&amp;name) | rekursive Aufruf von benannter Gruppe (NICHT UNTERSTÜTZT) |
| (?P=name) | benannter Rückverweis (NICHT UNTERSTÜTZT) |
| (?P&gt;name) | rekursive Aufruf von benannter Gruppe (NICHT UNTERSTÜTZT) |
| (?(cond)true|false) | bedingte Verzweigung (NICHT UNTERSTÜTZT) |
| (?(cond)true) | bedingte Verzweigung (NICHT UNTERSTÜTZT) |
| (\*ACCEPT) | regexps eher wie Prolog machen (NICHT UNTERSTÜTZT) |
| (\*COMMIT) | (NICHT UNTERSTÜTZT) |
| (\*F) | (NICHT UNTERSTÜTZT) |
| (\*FAIL) | (NICHT UNTERSTÜTZT) |
| (\*MARK) | (NICHT UNTERSTÜTZT) |
| (\*PRUNE) | (NICHT UNTERSTÜTZT) |
| (\*SKIP) | (NICHT UNTERSTÜTZT) |
| (\*THEN) | (NICHT UNTERSTÜTZT) |
| (\*ANY) | Festlegen der Konvention für Zeilenumbruch (nicht unterstützt) |
| (\*ANYCRLF) | (NICHT UNTERSTÜTZT) |
| (\*CR) | (NICHT UNTERSTÜTZT) |
| (\*CRLF) | (NICHT UNTERSTÜTZT) |
| (\*LF) | (NICHT UNTERSTÜTZT) |
| (\*BSR\_ANYCRLF) | Festlegen der \R-Konvention (nicht unterstützt) PCRE |
| (\*BSR\_UNICODE) | (NICHT UNTERSTÜTZT) PCRE |

## <a name="content-license"></a>Lizenz für Inhalte

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf von Chromium.org erstellten und freigegebenen Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/) beschriebenen Begriffen verwendet werden. Die Originalseite von Chromium finden Sie [hier](https://github.com/google/re2/wiki/Syntax).
  
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />Diese Arbeit unterliegt einer <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)