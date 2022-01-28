---
title: Identifizieren und Unterbrechen des Downloads potenziell gefährlicher Dateien
ms.author: kvice
author: AndreaLBarr
manager: srugh
ms.date: 01/10/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Verstehen, wie Microsoft Edge Downloads potenziell gefährlicher Dateien identifiziert und unterbricht
ms.openlocfilehash: 436c85248ef4012d75a9786c36e8f48d53f720d1
ms.sourcegitcommit: e7f3098d8b7d91cae20b5778a71a87daababc312
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2022
ms.locfileid: "12298193"
---
# <a name="identify-and-interrupt-downloads-of-potentially-dangerous-files"></a>Identifizieren und Unterbrechen des Downloads potenziell gefährlicher Dateien

Die Dateityprichtlinienkomponente von Microsoft Edge klassifiziert Dateien nach ihrer "Gefährlichkeit", um Dateidownloads zu verwalten. Eine schädliche Datei (z. B. eine `.txt` Datei) kann frei heruntergeladen werden, während eine potenziell gefährliche Datei wie eine einer `.dll` einer höheren Überprüfung unterzogen wird. Diese Prüfung bietet eine sicherheitsfreundlichere Benutzererfahrung.

## <a name="how-microsoft-edge-determines-the-danger-level-of-a-file-type"></a>Ermitteln der Gefahrenstufe eines Dateityps durch Microsoft Edge

Microsoft Edge erbt die Dateityprichtlinien vom upstream Chromium Browser. Sie können diese Dateitypen und ihre Klassifizierung in der [Datei download_file_types.asciipb](https://source.chromium.org/chromium/chromium/src/+/main:components/safe_browsing/core/resources/download_file_types.asciipb;drc=af17ad3f07c1d8a24381eb7669bec0c2ffb86521) anzeigen. In dieser Datei sehen Sie, dass jeder Typ über einen **danger_level**verfügt, der einen von drei Werten aufweist: `DANGEROUS` oder `NOT_DANGEROUS` `ALLOW_ON_USER_GESTURE` .

Die folgenden beiden Klassifizierungen sind einfach:

- **NOT_DANGEROUS** bedeutet, dass die Datei sicher heruntergeladen werden kann, auch wenn die Downloadanforderung versehentlich war.
- **DANGEROUS** bedeutet, dass der Browser den Benutzer immer warnen sollte, dass der Download sein Gerät beschädigen kann.

Die dritte Einstellung, **ALLOW_ON_USER_GESTURE** ist subtiler. Diese Dateien sind potenziell gefährlich, aber höchstwahrscheinlich unschädlich, wenn der Benutzer den Download anfordert. Microsoft Edge ermöglicht, dass diese Downloads automatisch fortgesetzt werden, wenn eine der folgenden Bedingungen erfüllt ist:

- Es ist eine [Benutzergeste](https://textslashplain.com/2020/05/18/browser-basics-user-gestures/) mit der Netzwerkanforderung verknüpft, die den Download gestartet hat. Beispielsweise hat der Benutzer auf einen Link zum Download geklickt.
- Es gibt einen aufgezeichneten vorherigen Besuch des verweisenden Ursprungs (die Seite, die mit dem Download verknüpft ist) vor der letzten Mitternacht (d. b. gestrigen oder früheren). Dieser aufgezeichnete Besuch impliziert, dass der Benutzer über einen Verlauf des Besuchs der Website verfügt.

Der Download wird auch automatisch fortgesetzt, wenn der Benutzer ihn explizit mithilfe des Befehls **"Link als** Kontextmenü speichern" startet, die URL des Downloads direkt in die Adressleiste des Browsers eingibt oder wenn Microsoft Defender SmartScreen angibt, dass die Datei sicher ist.

> [!NOTE]
> Ab Version 91 unterbricht Microsoft Edge Downloads ohne die erforderliche Geste.

## <a name="user-experience-for-downloads-that-lack-a-gesture"></a>Benutzerfreundlichkeit für Downloads ohne Geste

Wenn ein Download für einen potenziell gefährlichen Typ ohne die erforderliche Geste gestartet wird, gibt Microsoft Edge an, dass der Download "blockiert" wurde. Befehle benannt `Keep` und sind in der `Delete` **...** (Auslassungszeichen) für das Downloadelement, damit der Benutzer den Download fortsetzen oder abbrechen kann.

:::image type="content" source="media/microsoft-edge-security-Download-interruptions/Dowload-was-blocked.png" alt-text="Der Download wird blockiert, der Benutzer kann den Download beibehalten oder löschen.":::

Auf der `edge://downloads` Seite werden dem Benutzer die gleichen Optionen angezeigt. Der nächste Screenshot zeigt ein Beispiel für diese Optionen.

:::image type="content" source="media/microsoft-edge-security-Download-interruptions/msg-keep-delete-option.png" alt-text="Der Download wird blockiert, aber der Benutzer kann den Download beibehalten oder löschen.":::

## <a name="enterprise-controls-for-downloads"></a>Enterprise-Steuerelemente für Downloads

Es ist zwar unwahrscheinlich, dass Benutzer bei Websites, die sie täglich nutzen, Unterbrechungen beim Herunterladen feststellen, aber bei legitimen Downloads auf Websites, die sie nur selten nutzen, können diese auftreten. Um die Benutzererfahrung für Unternehmen zu optimieren, ist eine Gruppenrichtlinie verfügbar.

Unternehmen können [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](/deployedge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings) verwenden, um die Dateitypen festzulegen, die ohne Unterbrechung von bestimmten Websites heruntergeladen werden dürfen. Mit der folgenden Richtlinie können XML-Dateien beispielsweise von contoso.com und woodgrovebank.com ohne Unterbrechung heruntergeladen werden, und MSG-Dateien können von einer beliebigen Website heruntergeladen werden.

`[{"file_extension":"xml","domains":["contoso.com", "woodgrovebank.com"]},
{"file_extension":"msg", "domains": ["*"]}]`

## <a name="file-types-requiring-a-gesture"></a>Dateitypen, die eine Geste erfordern

Die neuesten [Dateitypenrichtlinien](https://source.chromium.org/chromium/chromium/src/+/main:components/safe_browsing/core/resources/download_file_types.asciipb;drc=af17ad3f07c1d8a24381eb7669bec0c2ffb86521) werden im Chromium-Quellcode veröffentlicht. Ab Mai 2021 umfassen Dateitypen mit einer `danger_level` von `ALLOW_ON_USER_GESTURE` auf mindestens einer Betriebssystemplattform Folgendes:
`crx, pl, py, pyc, pyo, pyw, rb, efi, oxt, msi, msp, mst, ade, adp, mad, maf, mag, mam, maq, mar, mas, mat, mav, maw, mda, mdb, mde, mdt, mdw, mdz, accdb, accde, accdr, accda, ocx, ops, paf, pcd, pif, plg, prf, prg, pst, cpi, partial, xrm-ms, rels, svg, xml, xsl, xsd, ps1, ps1xml, ps2, ps2xml, psc1, psc2, js, jse, vb, vbe, vbs, vbscript, ws, wsc, wsf, wsh, msh, msh1, msh2, mshxml, msh1xml, msh2xml, ad, app, application, appref-ms, asp, asx, bas, bat, chi, chm, cmd, com, cpl, crt, cer, der, eml, exe, fon, fxp, hlp, htt, inf, ins, inx, isu, isp, job, lnk, mau, mht, mhtml, mmc, msc, msg, reg, rgs, scr, sct, search-ms, settingcontent-ms, shb, shs, slk, u3p, vdx, vsx, vtx, vsdx, vssx, vstx, vsdm, vssm, vstm, vsd, vsmacros, vss, vst, vsw, xnk, cdr, dart, dc42, diskcopy42, dmg, dmgpart, dvdr, dylib, img, imgpart, ndif, service, smi, sparsebundle, sparseimage, toast, udif, action, definition, wflow, caction, as, cpgz, command, mpkg, pax, workflow, xip, mobileconfig, configprofile, internetconnect, networkconnect, pkg, deb, pet, pup, rpm, slp, out, run, bash, csh, ksh, sh, shar, tcsh, desktop, dex,apk`

## <a name="the-file-type-danger-level-may-vary-by-operating-system"></a>Die Bedrohungsstufe des Dateityps kann je nach Betriebssystem variieren.

Dateitypeinstellungen variieren manchmal je nach Clientbetriebssystemplattform. Beispielsweise ist eine `.exe` Datei auf einem Mac nicht gefährlich, während eine Datei auf Windows `.applescript` unschädlich ist.
