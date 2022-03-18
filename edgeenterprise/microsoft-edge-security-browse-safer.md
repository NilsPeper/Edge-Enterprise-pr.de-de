---
title: Sicherere Navigation mit Microsoft Edge
ms.author: pchiquini
author: dan-wesley
manager: robfranco
ms.date: 02/17/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Erfahren Sie, wie die erhöhte Sicherheit das Browsen mit Microsoft Edge sicherer macht.
ms.openlocfilehash: 43c48cb6210ce194a16759c5adb05a6f67b05249
ms.sourcegitcommit: 556aca8dde42dd66364427f095e8e473b86651a0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2022
ms.locfileid: "12445931"
---
# <a name="browse-more-safely-with-microsoft-edge"></a>Sicherere Navigation mit Microsoft Edge

In diesem Artikel wird beschrieben, wie Microsoft Edge für erhöhte Sicherheit im Web sorgt.

> [!NOTE]
> Dieser Artikel bezieht sich auf die Microsoft Edge-Version 98 oder höher.

## <a name="overview"></a>Übersicht

Microsoft Edge fügt Funktionen für eine erhöhte Sicherheit hinzu, um beim Webbrowsen und beim Besuch unbekannter Websites eine zusätzliche Schutzebene bereitzustellen. Die Webplattform wurde entwickelt, um Ihnen eine umfassende Browsererfahrung mit leistungsstarken Technologien wie JavaScript zu bieten. Andererseits kann diese Leistung zu einer größeren Gefährdung führen, wenn Sie eine schädliche Website besuchen. Mit der erhöhten Sicherheit trägt Microsoft Edge dazu bei, das Risiko eines Angriffs zu verringern, indem automatisch vorsichtigere Sicherheitseinstellungen auf unbekannten Websites angewendet werden und die Einstellungen während des Browsens mit der Zeit angepasst werden.

## <a name="defense-in-depth"></a>Tief greifende Abwehr

Die erhöhte Sicherheit in Microsoft Edge verringert speicherbezogene Sicherheitsrisiken durch Deaktivieren der Just-in-Time (JIT)-JavaScript-Kompilierung und Aktivieren zusätzlicher Betriebssystemschutzmechanismen für den Browser. Zu diesen Schutzmechanismen gehören der [hardwaregestützte Stapelschutz](https://techcommunity.microsoft.com/t5/windows-kernel-internals-blog/developer-guidance-for-hardware-enforced-stack-protection/ba-p/2163340) und der [Arbitrary Code Guard (ACG)](/microsoft-365/security/defender-endpoint/exploit-protection-reference?view=o365-worldwide#arbitrary-code-guard).

In Kombination tragen diese Änderungen zu einer „'tief greifenden Abwehr“ bei, da sie es einer bösartigen Website schwerer als je zuvor machen, eine ungepatchte Sicherheitslücke auszunutzen, um in den ausführbaren Speicher zu schreiben und einen Endbenutzer anzugreifen. Weitere Informationen zu den Experimentergebnissen finden Sie im [Blogbeitrag](https://microsoftedge.github.io/edgevr/posts/Super-Duper-Secure-Mode) des Microsoft Edge Security-Teams und unter [Einführung der erhöhten Sicherheit für Microsoft Edge](https://microsoftedge.github.io/edgevr/posts/Introducing-Enhanced-Security-for-Microsoft-Edge/).

Möglicherweise sind Sie auch daran interessiert, mehr über die grundlegenden [Sicherheitsmechanismen in Microsoft Edge](/deployedge/ms-edge-security-for-business) zu erfahren. Vielleicht möchten Sie mehr darüber erfahren, wie [Microsoft Edge SmartScreen](/deployedge/microsoft-edge-security-smartscreen) Benutzer vor Phishing-Betrug und Malware-Downloads schützt.

> [!NOTE]
> Websites, die WebAssembly (WASM) verwenden, werden in diesem Modus derzeit nicht unterstützt. Wenn Sie Zugriff auf eine Website benötigen, die WASM benötigt, können Sie sie wie nachfolgend beschrieben ihrer Ausnahmeliste hinzufügen.

## <a name="whats-new-in-microsoft-edge-security-settings"></a>Neuigkeiten in den Microsoft Edge-Sicherheitseinstellungen

Mit **Sicherheit im Web erhöhen** bietet Ihnen Microsoft Edge eine zusätzliche Schutzebene beim Webbrowsen.

Führen Sie die folgenden Schritte aus, um eine erhöhte Sicherheit zu konfigurieren.

1. Gehen Sie in Microsoft Edge zu **Einstellungen und mehr** > **Einstellungen** > **Datenschutz, Suche und Dienste**.
2. Überprüfen Sie unter **Sicherheit**, ob die Option **Sicherheit im Web erhöhen** aktiviert ist.
3. Wählen Sie die Option aus, die für Ihr Webbrowsen am besten geeignet ist.

Die folgenden Ein-/Aus-Einstellungen sind verfügbar:

- Ausschalten (Standard): Funktion ist deaktiviert
- Einschalten – ausgewoben (empfohlen): Microsoft Edge wendet zusätzliche Sicherheitsmechanismen an, wenn Benutzer unbekannte Websites besuchen, umgeht diese Schutzmechanismen jedoch bei häufig besuchten Websites. Diese Kombination bietet ein praktisches Maß an Schutz vor Angreifern, während die Benutzererfahrung für die üblichen Aufgaben eines Benutzers im Web erhalten bleibt.
- Einschalten – strikt: Microsoft Edge wendet zusätzliche Sicherheitsmechanismen auf alle Websites an, die ein Benutzer besucht. Die Benutzer können über einige Schwierigkeiten bei der Erledigung ihrer üblichen Aufgaben berichten.

Der folgende Screenshot zeigt die Konfigurationsseite „Sicherheit im Web erhöhen“ mit aktivierter erhöhter Sicherheit, wobei der Modus für eine ausgewogene Sicherheit festgelegt wurde.

:::image type="content" source="media/microsoft-edge-security-browse-safer/browse-safer-enhance-security-dialog.png" alt-text="Dialogfeld zum Konfigurieren der ausgewogenen Sicherheit im Web.":::

### <a name="how-balanced-mode-works"></a>Funktionsweise des Modus „Ausgewogen“

Der Modus „Ausgewogen“" ist ein adaptiver Modus, der auf dem Verhalten des Benutzers auf einem bestimmten Gerät und Microsofts Kenntnissen über die Risiken im Web basiert, um Websites, die von den Benutzern am wahrscheinlichsten genutzt werden und denen sie vertrauen, Vollzugriff auf die Webplattform zu gewähren, während die Möglichkeiten neuer und unbekannter Websites eingeschränkt werden.

### <a name="how-strict-mode-works"></a>Funktionsweise des Modus „Strikt“

Wie der Name schon sagt, wendet der Modus „Strikt“ diese Sicherheitsmechanismen standardmäßig auf alle Websites an. Sie können der Ausnahmewebsiteliste jedoch weiterhin manuell Websites hinzufügen, und die Konfiguration des Unternehmensadministrators gilt weiterhin, sofern vorhanden. Der Modus „Strikt“ ist für die meisten Endbenutzer nicht geeignet, da er ein gewisses Maß an Konfiguration erfordert, damit der Benutzer seine normalen Aufgaben erledigen kann.

### <a name="exception-site-list"></a>Ausnahmewebsiteliste

Im Modus „Ausgewogen“ und „im Modus „Strikt“ können Sie auch Ausnahmen für bestimmte vertraute Websites erstellen, denen Sie vertrauen. Führen Sie die folgenden Schritte aus, um Ihrer Ausnahmeliste eine Website hinzuzufügen.

1. Wählen Sie in Microsoft Edge **Einstellungen und mehr** > **Einstellungen** > **Datenschutz, Suche und Dienste** aus.
2. Vergewissern Sie sich, dass die Option **Sicherheit im Web erhöhen** aktiviert ist.
3. Wählen Sie unter **Sicherheit im Web erhöhen** die Option **Ausnahmen** aus.
4. Wählen Sie **Website hinzufügen** aus, geben Sie die vollständige URL ein, und wählen Sie dann **Hinzufügen** aus.

> [!NOTE]
> Sie können die Schritte (1 bis 3) verwenden, um Websites unter **Ausnahmen der erhöhten Sicherheit** anzuzeigen. Sie können eine Website **bearbeiten** oder **entfernen** sowie über die Option **Alle entfernen** alle Ausnahmen entfernen.

Der nächste Screenshot zeigt die Seite „Einstellungen“ für Sicherheitsausnahmen.

:::image type="content" source="media/microsoft-edge-security-browse-safer/browse-safer-enhanced-exceptions.png" alt-text="Seite „Einstellungen“ zum Konfigurieren von Sicherheitsausnahmen":::

### <a name="enterprise-controls"></a>Unternehmenssteuerungen

Unternehmensadministratoren können diese Sicherheitsfunktion mithilfe von Gruppenrichtlinieneinstellungen konfigurieren, einschließlich der Erstellung von „Zulassen“- und „Verweigern“-Listen, um die Sicherheit für ihre Benutzer beim Besuch bestimmter Websites explizit zu erhöhen oder den Modus für andere zu deaktivieren. Eine vollständige Liste der Richtlinien finden Sie in der [Dokumentation zur Microsoft Edge-Browserrichtlinie](/deployedge/microsoft-edge-policies).

## <a name="user-experience-with-enhanced-security"></a>Benutzererfahrung mit erhöhter Sicherheit

Nachdem ein Benutzer die erhöhte Sicherheit aktiviert hat, wird ein Banner mit den den Worten „Erhöhte Sicherheit“ in der URL-Navigationsleiste angezeigt, wenn Microsoft Edge die erhöhte Sicherheit auf eine bestimmte Website anwendet.

:::image type="content" source="media/microsoft-edge-security-browse-safer/browse-safer-added-security-banner.png" alt-text="Banner, das zeigt, dass die erhöhte Sicherheit aktiviert ist.":::

Wenn Sie das Banner auswählen, wird das folgende Flyout angezeigt. Sie können die Option „Sicherheit für diese Website erhöhen“ ein- oder ausschalten, um die erhöhte Sicherheit für eine bestimmte Website manuell zu aktivieren oder zu deaktivieren. Wenn Sie die Option „Sicherheit für diese Website erhöhen“ ändern, fügt Microsoft Edge diese Website der Ausnahmewebsiteliste hinzu. Im nächsten Screenshot ist die Funktion für die Website ausgeschaltet.  

:::image type="content" source="media/microsoft-edge-security-browse-safer/browse-safer-enhanced-security-off.png" alt-text="Dialogfeld mit deaktivierter Option „Erhöhte Sicherheit“.":::

> [!NOTE]
> Die Option „Sicherheit für diese Website erhöhen“ wird nur angezeigt, wenn die erweiterte Sicherheit auf der Seite „Einstellungen“ aktiviert ist.

## <a name="send-us-feedback"></a>Senden Sie uns Feedback

Wir würden gern Ihr Feedback zu unserer nächsten Iteration zur Verbesserung der Option „Sicherheit im Web erhöhen“ erhalten. Wenn etwas nicht so funktioniert, wie Sie es erwarten, oder wenn Sie uns Ihr Feedback zu diesen Änderungen mitteilen möchten, freuen wir uns auf Ihre Rückmeldung. Sie können sich an den Microsoft-Support wenden, um Probleme oder Feedback zu melden. Feedback können Sie auch in unserem [TechCommunity-Forum](https://techcommunity.microsoft.com/t5/enterprise/bd-p/EdgeInsiderEnterprise) hinterlassen.

## <a name="see-also"></a>Weitere Informationen

- [Video: Sicheres Browsen in Microsoft Edge](microsoft-edge-video-security-smartscreen.md)
- [Super Duper Secure Mode](https://microsoftedge.github.io/edgevr/posts/Super-Duper-Secure-Mode/)
- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)
