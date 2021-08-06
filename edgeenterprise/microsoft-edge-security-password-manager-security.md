---
title: 'Microsoft Edge Kennwort-Manager-Sicherheit '
ms.author: v-andreabarr
author: AndreaLBarr
manager: collw
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Microsoft Edge Kennwort-Manager-Sicherheit
ms.openlocfilehash: 41f1b269622e0053703af05f344a2d15e8a4b10e72e9507297b877f8047ccccb
ms.sourcegitcommit: d44c0997ffe40d67421312ed96e7766da947eaa0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "11727058"
---
# <a name="microsoft-edge-password-manager-security"></a>Microsoft Edge Kennwort-Manager-Sicherheit 

Die häufig gestellten Fragen in diesem Artikel beschreiben, wie der integrierte Kennwort-Manager von Microsoft Edge Sicherheit für Benutzerkennwörter bietet.

> [!Note]
>Dieser Artikel bezieht sich auf Microsoft Edge Version 77 oder höher.

## <a name="how-are-passwords-stored-in-microsoft-edge-and-how-safe-is-this-approach"></a>Wie werden Kennwörter in Microsoft Edge gespeichert und wie sicher ist dieser Ansatz?

Microsoft Edge speichert Kennwörter, die auf dem Datenträger verschlüsselt sind. Sie werden mit AES256 verschlüsselt, und der Datenverschlüsselungsschlüssel wird in einem Betriebssystemspeicherbereich gespeichert. Diese Technik wird als lokale Datenverschlüsselung bezeichnet. Obwohl nicht alle Browserdaten verschlüsselt sind, werden vertrauliche Daten wie Kennwörter, Kreditkartennummern und Cookies beim Speichern verschlüsselt.

Der Microsoft Edge Kennwort-Manager verschlüsselt Kennwörter, sodass nur auf sie zugegriffen werden kann, wenn ein Benutzer beim Betriebssystem angemeldet ist. Selbst wenn ein Angreifer über Administratorrechte oder Offlinezugriff verfügt und auf die lokal gespeicherten Daten zugreifen kann, ist das System so ausgelegt, dass es verhindert, dass der Angreifer die Klartextkennwörter eines Benutzers erhält, der nicht angemeldet ist.

Die Methode Kennwörter eines anderen Benutzers zu entschlüsseln wäre, wenn dieser Benutzer angemeldet wäre und der Angreifer das Kennwort des Benutzers hätte oder den Domänencontroller kompromittiert hätte.

### <a name="about-the-encryption-method"></a>Informationen zur Verschlüsselungsmethode

Der Verschlüsselungsschlüssel des Profils wird mit OSCrypt von Chromium geschützt und verwendet die folgenden plattformspezifischen Speicherorte für das Betriebssystem:

- Auf Windows ist der Speicherbereich DPAPI.

- Auf dem Mac ist der Speicherbereich der Schlüsselbund.

- Bei Linux lautet der Speicherbereich "Vault Keyring" oder "KWallet".

Alle diese Speicherbereiche verschlüsseln den AES256-Schlüssel mithilfe eines Schlüssels, auf den einige oder alle Prozesse zugreifen können, die als Benutzer ausgeführt werden. Dieser Angriffsvektor wird in Blogs häufig als mögliches "Exploit" oder "Sicherheitsrisiko" bezeichnet. Dies ist ein falsches Verständnis des Bedrohungsmodells und des Sicherheitsstatus des Browsers.

Physisch lokale Angriffe und Schadsoftware befinden sich jedoch außerhalb des Bedrohungsmodells, und unter diesen Bedingungen wären verschlüsselte Daten anfällig. Wenn Ihr Computer mit Schadsoftware infiziert ist, kann ein Angreifer entschlüsselten Zugriff auf die Speicherbereiche des Browsers erhalten. Der Code des Angreifers, der als Ihr Benutzerkonto ausgeführt wird, kann alles tun, was Sie tun können.

## <a name="why-encrypt-data-locally-why-not-store-the-encryption-key-elsewhere-or-make-it-harder-to-obtain"></a>Warum Daten lokal verschlüsseln? Warum speichern Sie den Verschlüsselungsschlüssel nicht an anderer Stelle, oder erschweren Sie den Zugriff?

Internetbrowser (einschließlich Microsoft Edge) sind nicht mit Schutzmaßnahmen zum Schutz vor Bedrohungen ausgestattet, bei denen das gesamte Gerät, aufgrund von Schadsoftware, die als Benutzer auf dem Computer ausgeführt wird, kompromittiert wird. Programme wie Microsoft Defender SmartScreen und Schutzmaßnahmen auf Betriebssystemebene wie Windows Defender sollen jedoch sicherstellen, dass das Gerät erst gar nicht kompromittiert wird.

Trotz seiner Unfähigkeit, sich vor voll vertrauenswürdiger Schadsoftware zu schützen, ist die lokale Datenverschlüsselung in bestimmten Szenarien nützlich. Wenn ein Angreifer beispielsweise eine Möglichkeit findet, Dateien vom Datenträger zu stehlen, ohne Code ausführen zu können, oder einen Laptop gestohlen hat, der nicht mit vollständiger Datenträgerverschlüsselung geschützt ist, erschwert die lokale Datenverschlüsselung dem Dieb das Abrufen der gespeicherten Daten.

## <a name="do-you-recommend-storing-passwords-in-microsoft-edge"></a>Empfehlen Sie Kennwörter in Microsoft Edge zu speichern?

Benutzer, die sich auf den integrierten Kennwort-Manager von Microsoft Edge verlassen können, können stärkere und eindeutige Kennwörter öfter verwenden (und tun dies auch), da sie sich nicht alle merken und sie nicht so oft eingeben müssen. Und, da der Kennwort-Manager Kennwörter nur auf den Websites automatisch ausfüllt, zu denen sie gehören, ist die Wahrscheinlichkeit geringer, dass Benutzer Opfer eines Phishing-Angriffs werden.

> [!Note]
>Branchenberichte zeigen, dass 80 % der Onlinevorfälle mit Phishing zusammenhängen und mehr als 37 % der nicht geschulten Benutzer Phishing-Tests nicht bestehen.

Der Kennwort-Manager von Microsoft Edge ist praktisch und einfach verteilt, was zu einer verbesserten Sicherheit beiträgt. In Kombination mit der Synchronisierung können Sie alle Ihre Kennwörter auf allen Ihren Geräten abrufen, und es ist einfach, für jede Website ein anderes Kennwort zu verwenden. Sie können lange und komplexe Kennwörter verwenden, die Sie sich nicht für jede Website merken müssen, und den Aufwand umgehen, jedes Mal eine komplexe Zeichenfolge einzugeben. Die Benutzerfreundlichkeit des Kennwort-Manager bedeutet, dass das Risiko geringer ist, Opfer eines Phishing-Angriffs zu werden.

Die Verwendung eines Kennwort-Managers, der auf die Anmeldesitzung des Betriebssystems des Benutzers festgelegt ist, bedeutet jedoch auch, dass ein Angreifer in dieser Sitzung sofort alle gespeicherten Kennwörter des Benutzers abrufen kann. Ohne einen Kennwort-Manager, von dem gestohlen werden kann, müsste ein Angreifer Tastaturanschläge nachverfolgen oder übermittelte Kennwörter überwachen.

Die Entscheidung, ob ein Kennwort-Manager verwendet werden soll, basiert auf der Bewertung der vielen Vorteile, die wir beschrieben haben, verglichen mit der Möglichkeit, dass das gesamte Gerät kompromittiert werden könnte. Für die meisten Bedrohungsmodelle ist die Verwendung des Microsoft Edge Kennwort-Managers die empfohlene Option.

> [!Note]
>Wenn ein Unternehmen beunruhigt ist, dass ein bestimmtes Kennwort oder eine Website aufgrund eines gestohlenen Kennworts kompromittiert wird, sollten zusätzliche Vorsichtsmaßnahmen ergriffen werden. Einige effektive Lösungen, die dazu beitragen, diese Art von Vorfällen zu mindern, sind Einmaliges Anmelden (Single Sign On, SSO) über Active Directory, Azure Active Directory oder einen Drittanbieter. Andere Lösungen umfassen 2FA (z. B. [MS Authenticator](/azure/active-directory/user-help/user-help-auth-app-download-install)) oder [WebAuthN](https://webauthn.guide/).

## <a name="should-a-password-manager-be-enabled-by-an-organization"></a>Sollte ein Kennwort-Manager von einer Organisation aktiviert werden?

Die einfache und einfache Antwort lautet: Ja, verwenden Sie den Kennwort-Manager des Browsers.

Eine umfassendere Reaktion bedeutet, dass Sie über detaillierte Kenntnisse über Ihr Bedrohungsmodell verfügen, da die Sicherheitsoptionen und -Möglichkeiten je nach verschiedenen Bedrohungsmodellen variieren. Einige relevante Fragen, die Sie berücksichtigen sollten, wenn Sie überlegen, ob Sie den Kennwort-Manager für Ihre Organisation aktivieren sollten, sind:

- Welche Art von Angreifern befürchten Sie?

- Bei welcher Art von Websites melden sich Ihre Benutzer an?

- Wählen Ihre Benutzer sichere, eindeutige Kennwörter aus?

- Sind die Konten Ihrer Benutzer durch 2FA geschützt?

- Welche Art von Angriffen ist am wahrscheinlichsten?

- Wie schützen Sie Ihre Unternehmensgeräte vor Schadsoftware?

- Wie viel Unannehmlichkeiten tolerieren Ihrer Benutzer?

- Berücksichtigen Sie die Auswirkungen der Datensynchronisierung.

Es ist wichtig, die Sicherheit von Benutzerdaten zu berücksichtigen, wenn sie mit verschiedenen Benutzergeräten synchronisiert werden, und wie viel Kontrolle die Organisation bei der Datensynchronisierung mit automatischem Ausfüllen hat.

Datensynchronisierung und Microsoft Edge:

- Die Datensynchronisierung kann organisationsweit nach Bedarf aktiviert oder deaktiviert werden.

- Datensicherheit während der Übertragung und im Ruhezustand in der Cloud: Alle synchronisierten Daten werden bei der Übertragung über HTTPS verschlüsselt, wenn sie zwischen dem Browser und Microsoft-Servern übertragen werden. Die synchronisierten Daten werden auch in einem verschlüsselten Zustand auf Microsoft-Servern gespeichert. Vertrauliche Datentypen wie Adressen und Kennwörter werden vor der Synchronisierung auf dem Gerät weiter verschlüsselt. Wenn Sie ein Geschäfts-, Schul- oder Unikonto verwenden, werden alle Datentypen vor der Synchronisierung mit Microsoft Information Protection weiter verschlüsselt.

## <a name="why-do-microsoft-security-baselines-recommend-disabling-the-password-manager"></a>Warum empfehlen Microsoft-Sicherheitsbaselines, den Kennwort-Manager zu deaktivieren?

Das Microsoft-Sicherheitsteam hat aktuell die Auswirkungen eines Computerwurms, der ein Netzwerk von Enterprise-PCS gefährdet (was zu einem Verlust aller Anmeldeinformationen in den Kennwort-Managern aller Geräte führt) als schwerwiegender bewertet, als das (wahrscheinlichere, aber geringere) Risiko von gezielten Phishing-Angriffen, die eine einzelne vom Benutzer eingegebene Anmeldeinformation gefährden.

Diese Bewertung wird derzeit erörtert und kann sich durch das Hinzufügen neuer Features zur Verbesserung der Sicherheit in Microsoft Edge ändern.

## <a name="can-malicious-extensions-gain-access-to-passwords"></a>Können bösartige Erweiterungen Zugriff auf Kennwörter erhalten?

Eine Erweiterung mit der Berechtigung zur Interaktion mit einer Seite kann grundsätzlich auf alle Elemente von dieser Seite zugreifen, einschließlich eines automatisch ausgefüllten Kennworts. Ebenso kann eine bösartige Erweiterung den Inhalt von Formularfeldern und Netzwerkanforderungen/-antworten ändern, um die Autorität des aktuellen Benutzeranmeldekontexts zu missbrauchen.

Microsoft Edge bietet jedoch eine umfangreiche Bandbreite von Richtlinien, die eine genaue Kontrolle über installierte Erweiterungen ermöglichen. Die Verwendung der Richtlinien in der folgenden Tabelle ist zum Schutz von Unternehmensdaten erforderlich.

| Richtlinie | Beschriftung |
|-|-|
|[BlockExternalExtensions](/deployedge/microsoft-edge-policies#blockexternalextensions)|Blockiert die Installation externer Erweiterungen|
|[ExtensionAllowedTypes](/deployedge/microsoft-edge-policies#extensionallowedtypes)|Konfigurieren von zulässigen Erweiterungstypen|
|[ExtensionInstallAllowlist](/deployedge/microsoft-edge-policies#extensioninstallallowlist)|Zulassen, dass bestimmte Erweiterungen installiert werden|
|[ExtensionInstallBlocklist](/deployedge/microsoft-edge-policies#extensioninstallblocklist)|Steuern, welche Erweiterungen nicht installiert werden können|
|[ExtensionInstallForcelist](/deployedge/microsoft-edge-policies#extensioninstallforcelist)|Steuern, welche Erweiterungen im Hintergrund installiert werden|
|[ExtensionInstallSources](/deployedge/microsoft-edge-policies#extensioninstallsources)|Konfigurieren von Erweiterungen und Installationsquellen für Benutzerskripts|
| [ExtensionSettings](/deployedge/microsoft-edge-policies#extensionsettings) |Konfigurieren der Erweiterungsverwaltungseinstellungen |

## <a name="how-does-the-microsoft-edge-password-manager-compare-with-a-third-party-product"></a>Wie schneidet der Microsoft Edge Kennwort-Manager im Vergeich mit einem Drittanbieterprodukt ab?

Die folgende Tabelle zeigt, wie der Microsoft Edge Kennwort-Manager im Vergleich mit Kennwort-Managern von Drittanbietern abschneidet.

| Kennwort-Manager eines Drittanbieters | Microsoft Edge Kennwort-Manager|
|-|-|
| *Serversynchronisierung*. Einige Produkte speichern Kennwörter in der Cloud, um alle Ihre Geräte zu synchronisieren. Dieses Feature ist hilfreich, aber es besteht ein Risiko, wenn der Clouddienst kompromittiert wird und Ihre Daten verfügbar gemacht werden. **Hinweise:** Das Risiko wird verringert, indem Kennwörter in der Cloud verschlüsselt werden und der Verschlüsselungsschlüssel auf Ihren Geräten gespeichert wird, damit Angreifer nicht auf den Schlüssel und Ihre Kennwörter zugreifen können.| Es besteht ein Cloud-Expositionsrisiko, da Kennwörter auf Windows-Geräten synchronisiert werden, auf denen Microsoft Edge installiert sind. **Hinweise:** Dieses Risiko wird durch die Datensicherheitsschritte, die in diesem Artikel behandelt werden, verringert.|
| *Vertrauensstellung*. Es ist notwendig zu vertrauen, dass der Drittanbieter keine schädlichen Aktionen ausführt, z. B. das Senden Ihrer Kennwörter an eine andere Partei. **Hinweise:** Dieses Risiko kann durch Überprüfen des Quellcodes (bei Open-Source-Produkten) verringert werden oder durch das Vertrauen, dass dem Anbieter seine Reputation und der Umsatz wichtig sind. | **Hinweise:** Microsoft ist ein bekannter und vertrauenswürdiger Anbieter mit einer jahrzehntelangen Geschichte bei der Bereitstellung von Sicherheit und Produktivität auf Unternehmensniveau mit Ressourcen, die zum weltweiten Schutz Ihrer Kennwörter entwickelt wurden. |
| *Lieferkettensicherheit*. Es ist schwierig zu überprüfen, ob der Anbieter über sichere Lieferketten-/Build-/Releaseprozesse für den Quellcode verfügt. |**Hinweise:** Microsoft verfügt über robuste interne Prozesse, um ein minimales Risiko für den Quellcode sicherzustellen. |
| *kompromittierter/s Client oder Konto*. Wenn ein Clientgerät oder Benutzerkonto kompromittiert wird, kann ein Angreifer die Kennwörter abrufen. **Hinweise:**   Dieses Risiko wird für einige Kennwortmanager verringert, bei denen der Benutzer ein Masterkennwort eingeben muss, das nicht lokal gespeichert ist, um die Kennwörter zu entschlüsseln. Ein Masterkennwort ist nur teilweise mindernd, da ein Angreifer Tastatureingaben lesen und das Masterkennwort abrufen kann, während es eingegeben wird, oder Kennwörter aus dem Prozessspeicher lesen kann, wenn er ein Formularfeld ausfüllt. | **Hinweise:** Microsoft bietet Schutzmaßnahmen auf Betriebssystemebene wie Windows Defender, um sicherzustellen, dass das Gerät erst gar nicht kompromittiert wird. Wenn jedoch ein Clientgerät kompromittiert wird, kann ein Angreifer die Kennwörter möglicherweise entschlüsseln. |

> [!Note]
> Produkte von Drittanbietern bieten möglicherweise Schutz vor zusätzlichen Bedrohungsmodellen, aber dies geht auf Kosten der Komplexität oder der Benutzerfreundlichkeit. Der Microsoft Edge Kennwort-Manager ist für eine komfortable und benutzerfreundliche Kennwortverwaltung konzipiert, die von IT-Administratoren mithilfe von Gruppenrichtlinien vollständig gesteuert werden kann und kein Vertrauen in einen Drittanbieters erfordert.

## <a name="why-doesnt-microsoft-offer-a-master-password-to-protect-the-data"></a>Warum bietet Microsoft kein Masterkennwort zum Schutz der Daten an?

Wenn Browser-Kennwörter auf dem Datenträger verschlüsselt werden, ist der Verschlüsselungsschlüssel für jeden Prozess auf Ihrem Gerät verfügbar, der lokal ausgeführte Schadsoftware einschließt. Selbst wenn Kennwörter in einem "Tresor" mit einem Hauptschlüssel verschlüsselt werden, werden sie entschlüsselt, wenn sie im Arbeitsspeicher des Browsers geladen werden und können nach dem Entsperren des Tresors abgerufen werden.

Ein "Masterkennwort"-Feature (das den Benutzer authentifiziert, bevor seine Daten automatisch ausgefüllt werden) bietet einen Kompromiss zwischen Benutzerfreundlichkeit und einer umfassenden Bedrohungsminderung. Insbesondere trägt es dazu bei, das Zeitfenster der Datenexposition gegen latente Schadsoftware oder physisch lokale Angreifer zu reduzieren. Ein Masterkennwort ist jedoch keine Patentlösung, und lokale Angreifer und dedizierte Schadsoftware haben verschiedene Strategien, um den Schutz eines Master-Kennworts zu umgehen.

> [!Note]
> Microsoft ist sich bewusst, wie wertvoll die Authentifizierung von Benutzern vor dem automatischen Ausfüllen ist, und diese Funktionalität wird in einer zukünftigen Version von Microsoft Edge hinzugefügt.

## <a name="can-using-a-password-manager-impact-my-privacy"></a>Kann sich die Verwendung eines Kennwort-Managers auf meinen Datenschutz auswirken?

Nein, nicht, wenn Schritte zum Schutz des Zugriffs auf Ihre gespeicherten Kennwörter ausgeführt werden.

Es gibt einen bekannten Exploit, den einige Werbekunden verwenden, der gespeicherte Kennwörter verwendet, um Benutzer eindeutig zu identifizieren und nachzuverfolgen. Weitere Informationen finden Sie unter [Ad-Targeters rufen Daten aus dem Kennwort-Manager Ihres Browsers ab](https://www.theverge.com/2017/12/30/16829804/browser-password-manager-adthink-princeton-research). Browser haben Maßnahmen ergriffen, um dieses [Datenschutzproblem](https://bugs.chromium.org/p/chromium/issues/detail?id=798492)zu beheben.Mit der PasswordValueGatekeeper-Klasse kann der Zugriff auf die Kennwortfelddaten eingeschränkt werden, auch wenn der Browser für das automatische Ausfüllen beim Laden konfiguriert ist.

Diese Bedrohung durch das Sammeln von Benutzerinformationen kann leicht entschärft werden, indem das optionale "edge://flags/#fill-on-account-select"-Feature aktiviert wird. Dieses Feature ermöglicht nur das Hinzufügen von Kennwörtern zu einem Formularfeld, nachdem der Benutzer explizit eine Anmeldeinformation ausgewählt hat, wodurch sichergestellt wird, dass Benutzer wissen, wer ihre Kennwörter empfängt.

## <a name="see-also"></a>Weitere Informationen

[Microsoft Edge Enterprise-Startseite](https://www.microsoft.com/edge/business/download)

[Warum Microsoft Edge auf Windows 10 sicherer als Chrome for Business ist](/DeployEdge/ms-edge-security-for-business)
