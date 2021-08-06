---
title: Unterbrechen des Downloads potenziell gefährlicher Dateien
ms.author: kvice
author: AndreaLBarr
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Unterbrechen des Downloads potenziell gefährlicher Dateien
ms.openlocfilehash: 2c2827185cad83b3878139ee82dcbc8407a2a6eebcf73f69a9481430c29f3db9
ms.sourcegitcommit: d44c0997ffe40d67421312ed96e7766da947eaa0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "11727246"
---
# <a name="interrupting-downloads-of-potentially-dangerous-files"></a>Unterbrechen des Downloads potenziell gefährlicher Dateien

Die Komponente „Dateityprichtlinien“ von Microsoft Edge ermöglicht es, Dateien nach ihrer „Gefährlichkeit“ zu klassifizieren, sodass harmlose Dateien (z. B. `.txt`-Dateien) frei heruntergeladen werden können, während potenziell gefährliche Dateien (z. B. `.dll`-Dateien) einem höheren Maß an Überprüfung und sicherheitsorientierter Behandlung in der Benutzerumgebung unterzogen werden.

## <a name="determining-the-danger-level-of-a-file-type"></a>Ermitteln der Gefahrenstufe eines Dateityps

Microsoft Edge erbt die Dateityprichtlinien vom Chromium-Upstreambrowser; Sie können den aktuellen Inhalt der Liste [hier](https://source.chromium.org/chromium/chromium/src/+/main:components/safe_browsing/core/resources/download_file_types.asciipb) anzeigen. In der Liste sehen Sie, dass jeder Typ einen „danger_level“-Wert von `DANGEROUS`, `NOT_DANGEROUS` oder `ALLOW_ON_USER_GESTURE` aufweist.

Die ersten beiden sind einfach: **NOT_DANGEROUS** bedeutet, dass die Datei ohne Sicherheitsrisiko heruntergeladen werden kann, auch wenn der Download versehentlich erfolgt. **DANGEROUS** bedeutet, dass der Browser den Benutzer immer warnen sollte, dass der Download sein Gerät beschädigen kann.

Bei der dritten Einstellung, **ALLOW_ON_USER_GESTURE**, ist es weniger offensichtlich. Solche Dateien sind potenziell gefährlich, aber höchstwahrscheinlich unschädlich, wenn der Benutzer den Download angefordert hat. In Microsoft Edge können solche Downloads automatisch fortgesetzt werden, wenn zwei Bedingungen erfüllt sind:

1. Es gibt eine [Benutzergeste](https://textslashplain.com/2020/05/18/browser-basics-user-gestures/), die mit der Netzwerkanforderung verbunden ist, die den Download initiiert hat (z. B. hat der Benutzer auf einen Link zum Download geklickt).
2. Es existiert ein aufgezeichneter vorheriger Besuch des verweisenden Ursprungs (die Seite, die mit dem Download verknüpft ist) vor letzter Mitternacht (d. h. vom gestrigen Tag oder früher). Dies bedeutet, dass der Benutzer über einen Verlauf des Besuchs der Website verfügt.

Der Download wird auch dann automatisch durchgeführt, wenn der Benutzer ihn explizit über den Befehl **Link speichern unter** im Kontextmenü initiiert hat, wenn er die URL des Downloads direkt in die Adressleiste des Browsers eingegeben hat oder wenn Microsoft Defender SmartScreen anzeigt, dass die Datei sicher ist.

**Update:** Ab Version 91 unterbricht Microsoft Edge Downloads, bei denen die erforderliche Geste fehlt.

## <a name="user-experience-for-downloads-lacking-gestures"></a>Benutzerumgebung für Downloads ohne Gesten

Wenn ein Download eines potenziell gefährlichen Typs ohne die erforderliche Geste gestartet wird, gibt Microsoft Edge an, dass der Download „blockiert“ wurde. Im Menü des Downloadelements sind die Befehle `Keep` und `Delete` verfügbar, ... damit der Benutzer den Download fortsetzen oder abbrechen kann.

:::image type="content" source="media/microsoft-edge-security-Download-interruptions/Dowload-was-blocked.png" alt-text="Download wurde blockiert":::

Auf der `edge://downloads`-Seite werden dem Benutzer die gleichen Optionen angezeigt:

:::image type="content" source="media/microsoft-edge-security-Download-interruptions/msg-keep-delete-option.png" alt-text="MSG Beibehalten Löschen Option":::

## <a name="enterprise-controls"></a>Unternehmenssteuerungen

Es ist zwar unwahrscheinlich, dass Benutzer bei Websites, die sie täglich nutzen, Unterbrechungen beim Herunterladen feststellen, aber bei legitimen Downloads auf Websites, die sie nur selten nutzen, können diese auftreten. Um die Benutzererfahrung für Unternehmen zu optimieren, ist eine Gruppenrichtlinie verfügbar.

Unternehmen können [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](/deployedge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings) verwenden, um die Dateitypen festzulegen, die ohne Unterbrechung von bestimmten Websites heruntergeladen werden dürfen. Mit der folgenden Richtlinie können XML-Dateien beispielsweise ohne Unterbrechung von „contoso.com“ und „woodgrovebank.com“ heruntergeladen werden, und MSG-Dateien können von einer beliebigen Website heruntergeladen werden.

`[{"file_extension":"xml","domains":["contoso.com", "woodgrovebank.com"]},
{"file_extension":"msg", "domains": ["*"]}]`

## <a name="file-types-requiring-a-gesture"></a>Dateitypen, die eine Geste erfordern

Die neuesten [Dateitypenrichtlinien](https://source.chromium.org/chromium/chromium/src/+/main:components/safe_browsing/core/resources/download_file_types.asciipb) werden im Chromium-Quellcode veröffentlicht. Ab Mai 2021 umfassen Dateitypen mit einer `danger_level` von `ALLOW_ON_USER_GESTURE` auf mindestens einer Betriebssystemplattform Folgendes:
`crx, pl, py, pyc, pyo, pyw, rb, efi, oxt, msi, msp, mst, ade, adp, mad, maf, mag, mam, maq, mar, mas, mat, mav, maw, mda, mdb, mde, mdt, mdw, mdz, accdb, accde, accdr, accda, ocx, ops, paf, pcd, pif, plg, prf, prg, pst, cpi, partial, xrm-ms, rels, svg, xml, xsl, xsd, ps1, ps1xml, ps2, ps2xml, psc1, psc2, js, jse, vb, vbe, vbs, vbscript, ws, wsc, wsf, wsh, msh, msh1, msh2, mshxml, msh1xml, msh2xml, ad, app, application, appref-ms, asp, asx, bas, bat, chi, chm, cmd, com, cpl, crt, cer, der, eml, exe, fon, fxp, hlp, htt, inf, ins, inx, isu, isp, job, lnk, mau, mht, mhtml, mmc, msc, msg, reg, rgs, scr, sct, search-ms, settingcontent-ms, shb, shs, slk, u3p, vdx, vsx, vtx, vsdx, vssx, vstx, vsdm, vssm, vstm, vsd, vsmacros, vss, vst, vsw, xnk, cdr, dart, dc42, diskcopy42, dmg, dmgpart, dvdr, dylib, img, imgpart, ndif, service, smi, sparsebundle, sparseimage, toast, udif, action, definition, wflow, caction, as, cpgz, command, mpkg, pax, workflow, xip, mobileconfig, configprofile, internetconnect, networkconnect, pkg, deb, pet, pup, rpm, slp, out, run, bash, csh, ksh, sh, shar, tcsh, desktop, dex,apk`

## <a name="danger-level-may-vary-by-operating-system"></a>Gefahrenstufe kann je nach Betriebssystem variieren

Dateitypeinstellungen variieren manchmal je nach Clientbetriebssystemplattform. Beispielsweise ist `.exe` auf einem Mac nicht gefährlich, während `.applescript` auf Windows unschädlich ist.
