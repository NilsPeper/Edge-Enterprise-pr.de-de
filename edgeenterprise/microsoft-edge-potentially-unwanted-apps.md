---
title: Verwenden von Microsoft Edge zum Schutz vor potenziell unerwünschten Anwendungen
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 03/04/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Verwenden von Microsoft Edge zum Schutz vor potenziell unerwünschten Anwendungen
ms.openlocfilehash: 4e9d513c4d1144d4109064d7aa42e4ef31a59b88
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/24/2021
ms.locfileid: "11448029"
---
# <a name="protect-against-potentially-unwanted-applications-puas"></a>Schützen vor potenziell unerwünschten Anwendungen (PUA)

In diesem Artikel wird erläutert, wie Sie sich mit Microsoft Edge oder Windows Defender Antivirus vor potenziell unerwünschten Anwendungen (PUA) schützen können.

> [!NOTE]
> Dieser Artikel bezieht sich auf Microsoft Edge Version80 oder höher.

## <a name="overview"></a>Übersicht

Potenziell unerwünschte Anwendungen werden nicht als Viren oder Schadsoftware betrachtet, diese Apps können jedoch Aktionen an Endpunkten ausführen, die sich negativ auf die Endpunktleistung oder -nutzung auswirken. So versucht *Evasionssoftware* (Software zum Umgehen der Erkennung oder zum Vermeiden anderer Abwehrmaßnahmen) beispielsweise aktiv, die Erkennung durch Sicherheitsprodukte zu umgehen. Diese Art von Software kann das Risiko erhöhen, dass Ihr Netzwerk mit der eigentlichen Schadsoftware infiziert wird. PUA kann sich auch auf Anwendungen beziehen, die bekanntermaßen mit Sicherheitsrisiken verbunden sind.

Eine Beschreibung der Kriterien, anhand derer Software als PUA klassifiziert wird, finden Sie unter [Potenziell unerwünschte Anwendung](/windows/security/threat-protection/intelligence/criteria#potentially-unwanted-application-pua).

## <a name="protect-against-pua-with-microsoft-edge"></a>Schutz vor PUA mit Microsoft Edge

Microsoft Edge (Version 80.0.361.50 oder höher) blockiert PUA-Downloads und zugehörige Ressourcen-URLs.

Sie können Schutzmaßnahmen einrichten, indem Sie das Feature **Potenziell unerwünschte Apps blockieren** in Microsoft Edge aktivieren.

> [!NOTE]
> Der [Microsoft Edge-Teamblogbeitrag](https://blogs.windows.com/msedgedev/2020/02/27/protecting-users-potentially-unwanted-apps/) beschreibt dieses neue Feature, und erläutert, wie Sie eine falsch beschriftete App behandeln oder eine App als unerwünscht melden.

### <a name="to-enable-pua-protection"></a>So aktivieren Sie den Schutz vor potenziell unerwünschten Anwendungen

1. Öffnen Sie **Einstellungen** im Browser.
2. Wählen Sie **Datenschutz und Dienste** aus.
3. Überprüfen Sie im Abschnitt **Dienste**, ob **Microsoft Defender SmartScreen** aktiviert ist. Wenn nicht, aktivieren Sie Microsoft Defender SmartScreen. Das Beispiel im folgenden Screenshot zeigt, dass der Browser von der Organisation verwaltet wird und dass Microsoft Defender SmartScreen aktiviert ist.

   ![Aktivieren von Microsoft Edge-PUA in den Einstellungen](./media/microsoft-edge-potentially-unwanted-apps/security-pua-setup.png)

4. Verwenden Sie im Abschnitt **Dienste** den im vorhergehenden Screenshot abgebildeten Umschalter, um **Potenziell unerwünschte Apps blockieren** zu aktivieren.

   > [!TIP]
   > Sie können das URL-Blockierungsfeature des PUA-Schutzes sicher erkunden, indem Sie es auf einem unserer Windows Defender SmartScreen-[Demoseiten](https://demo.smartscreen.msft.net/) testen.

Wenn Microsoft Edge eine potenziell unerwünschte Anwendung erkennt, erhalten Sie eine Meldung wie die im nächsten Screenshot gezeigte.

   ![PUA-Warnmeldung in Microsoft Edge](./media/microsoft-edge-potentially-unwanted-apps/security-pua-msg.png)

### <a name="to-block-against-pua-associated-urls"></a>So blockieren Sie URLs, die mit PUA in Zusammenhang stehen

Nachdem Sie den PUA-Schutz in Microsoft Edge aktiviert haben, schützt Windows Defender SmartScreen Sie vor URLs, die mit PUA in Zusammenhang stehen.

Es gibt mehrere Möglichkeiten, wie Administratoren die Zusammenarbeit von Microsoft Edge und Windows Defender SmartScreen konfigurieren können, um Benutzer vor URLs zu schützen, die mit PUA in Zusammenhang stehen. Weitere Informationen finden Sie unter:

- [Konfigurieren der Microsoft Edge-Richtlinieneinstellungen unter Windows](./configure-microsoft-edge.md)
- [SmartScreen-Einstellungen](./microsoft-edge-policies.md#smartscreen-settings)
- [SmartScreenPuaEnabled-Richtlinie](./microsoft-edge-policies.md#smartscreenpuaenabled)
- [Windows Defender SmartScreen konfigurieren](/microsoft-edge/deploy/available-policies?source=docs#configure-windows-defender-smartscreen)

Administratoren können die Microsoft Defender Advanced Threat Protection (Microsoft Defender ATP)-Blockierungsliste auch anpassen. Sie können das Microsoft Defender ATP-Portal nutzen, um [Indikatoren für IPs und URLs zu erstellen und zu verwalten](/windows/security/threat-protection/microsoft-defender-atp/manage-indicators#create-indicators-for-ips-and-urlsdomains-preview).

## <a name="protect-against-pua-with-windows-defender-antivirus"></a>Schutz vor PUA mit Windows Defender Antivirus

Im Artikel [Erkennen und Blockieren potenziell unerwünschter Anwendungen](/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus#windows-defender-antivirus) wird auch beschrieben, wie Sie Windows Defender Antivirus konfigurieren können, um den PUA-Schutz zu aktivieren. Sie können den Schutz mit einer der folgenden Optionen konfigurieren:

- [Microsoft Intune](/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus#use-intune-to-configure-pua-protection)
- [Microsoft Endpoint Configuration Manager](/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus#use-configuration-manager-to-configure-pua-protection)
- [Gruppenrichtlinie](/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus#use-group-policy-to-configure-pua-protection)
- [PowerShell-Cmdlets](/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus#use-powershell-cmdlets-to-configure-pua-protection)

Erkennt Windows Defender eine PUA-Datei auf einem Endpunkt, wird die Datei isoliert, und der Benutzer wird ([sofern die Benachrichtigungen nicht deaktiviert sind](/windows/security/threat-protection/windows-defender-antivirus/configure-notifications-windows-defender-antivirus)) in derselben Form wie bei einer normalen Bedrohungserkennung benachrichtigt (mit dem Präfix "PUA:"). Erkannte Bedrohungen werden auch in der [Quarantäneliste in der Windows-Sicherheits-App](/windows/security/threat-protection/windows-defender-antivirus/windows-defender-security-center-antivirus#detection-history) aufgeführt.

### <a name="pua-notifications-and-events"></a>PUA-Benachrichtigungen und -Ereignisse

Es gibt mehrere Möglichkeiten, wie ein Administrator PUA-Ereignisse sehen kann:

- In der Windows Ereignisanzeige, aber nicht in Microsoft Endpoint Configuration Manager oder Intune.
- In einer E-Mail, wenn E-Mail-Benachrichtigungen für PUA-Funde aktiviert sind.
- In [Windows Defender Antivirus](/windows/security/threat-protection/windows-defender-antivirus/troubleshoot-windows-defender-antivirus)-Ereignisprotokollen, in denen ein PUA-Ereignis unter der Ereignis-ID 1116 mit der folgenden Meldung erfasst wird: "Die Antischadsoftwareplattform hat Schadsoftware oder andere potenziell unerwünschte Software erkannt.

> [!NOTE]
> Die Benutzer sehen "*.exe wurde von Microsoft Defender SmartScreen als potenziell unerwünschte Anwendung blockiert".

### <a name="allow-list-an-app"></a>Aufnehmen einer App in die Zulassungsliste

Wie Microsoft Edge bietet auch Windows Defender Antivirus eine Möglichkeit, Dateien zuzulassen, die irrtümlich blockiert wurden oder zur Ausführung einer Aufgabe benötigt werden. Wenn dies geschieht, können Sie eine Datei in die Zulassungsliste aufnehmen. Weitere Informationen finden Sie unter [Konfigurieren von Endpoint Protection in Configuration Manager](/previous-versions/system-center/system-center-2012-R2/hh508770(v=technet.10)#to-exclude-specific-files-or-folders), um zu erfahren, wie Sie bestimmte Dateien oder Ordner ausschließen können.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)
- [Schutz vor Bedrohungen](/windows/security/threat-protection/index)
- [Konfigurieren von verhaltensbasiertem, heuristischem und Echtzeitschutz](/windows/security/threat-protection/windows-defender-antivirus/configure-protection-features-windows-defender-antivirus)
- [Schutz der nächsten Generation](/windows/security/threat-protection/windows-defender-antivirus/windows-defender-antivirus-in-windows-10)
- [Sicherheitsbaseline für Chromium-basiertes Microsoft Edge, Version 79](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/security-baseline-final-for-chromium-based-microsoft-edge/ba-p/1111863)