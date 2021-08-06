---
title: Microsoft Edge-Datenschutzeinstellungen für Unternehmen
ms.author: collw
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Konfigurieren von Microsoft Edge-Datenschutzeinstellungen für Unternehmen
ms.openlocfilehash: fe2a6e57d70a6a37297e28854291b913af1fd08e826df845fc3572fecb09f07a
ms.sourcegitcommit: d44c0997ffe40d67421312ed96e7766da947eaa0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "11726188"
---
# <a name="configure-microsoft-edge-policies-to-support-enterprise-privacy"></a>Konfigurieren von Microsoft Edge-Richtlinien zur Unterstützung des Datenschutzes in Unternehmen

Microsoft verpflichtet sich, Unternehmen die Informationen und Steuerelemente bereitzustellen, die für die Auswahl der Datensammlung in Microsoft Edge erforderlich sind.

## <a name="overview"></a>Übersicht

Bei der Bereitstellung von Microsoft Edge unter Windows 10 werden Diagnosedaten standardmäßig basierend auf der [Einstellung für Windows-Diagnosedaten](/windows/privacy/configure-windows-diagnostic-data-in-your-organization) der Benutzer gesendet.

Wenn Microsoft Edge auf Nicht-Windows-Plattformen bereitgestellt wird, werden die Diagnosedaten gemäß den Einstellungen der folgenden Gruppenrichtlinien gesammelt:

- (VERALTET) [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled): Aktivieren der Berichterstellung für Nutzungs- und Absturzdaten. Diese Richtlinie ist in der Microsoft Edge-Version 89 veraltet.
- (VERALTET) [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices): Senden von Siteinformationen, um Microsoft-Dienste zu verbessern. Diese Richtlinie ist in der Microsoft Edge-Version 89 veraltet.

Die vorhergehenden veralteten Richtlinien werden ersetzt durch [Telemetrie zulassen](/windows/privacy/configure-windows-diagnostic-data-in-your-organization) unter Windows 10 sowie die [DiagnosticData](./microsoft-edge-policies.md#diagnosticdata)-Richtlinie für alle anderen Plattformen.  

## <a name="configure-policy-settings"></a>Konfigurieren von Richtlinieneinstellungen

Laden Sie zunächst die aktuelle Microsoft Edge-Richtlinienvorlage herunter, und verwenden Sie diese (weitere Informationen finden Sie unter [Konfigurieren von Microsoft Edge](configure-microsoft-edge.md)).

### <a name="send-required-and-optional-diagnostic-data-about-browser-usage"></a>Senden erforderlicher und optionaler Diagnosedaten zur Browsernutzung

Wenn die [DiagnosticData](./microsoft-edge-policies.md#diagnosticdata)-Richtlinie konfiguriert ist, hat Sie Vorrang vor [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) und [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices).

#### <a name="required-and-optional-diagnostic-data"></a>Erforderliche und optionale Diagnosedaten senden

Erforderliche Diagnosedaten werden gesammelt, um Microsoft Edge sicher und aktuell zu halten und die erwartete Leistung zu gewährleisten.

Optionale Diagnosedaten umfassen Daten zu Ihrer Verwendung des Browsers, Ihren besuchten Websites und Absturzberichte, um Microsoft Edge sicher und aktuell zu halten und die erwartete Leistung zu erzielen. Sie werden verwendet, um Microsoft Edge und andere Microsoft-Produkte und -Dienste für alle Benutzer zu verbessern.

> [!NOTE]
> Diese Richtlinie wird auf Windows 10-Geräten nicht unterstützt. Um die Datenerfassung unter Windows 10 zu steuern, müssen IT-Administratoren die Windows-Diagnosedaten-Gruppenrichtlinie verwenden. Diese Richtlinie handelt es sich je nach Windows-Version entweder um **Telemetrie zulassen** oder um **Diagnosedaten zulassen**. Weitere Informationen zur [Windows 10-Diagnosedatenerfassung](/windows/privacy/configure-windows-diagnostic-data-in-your-organization).

Verwenden Sie eine der folgenden Einstellungen, um **DiagnosticData** zu konfigurieren:

- Aus (nicht empfohlen) (0) deaktiviert die erforderliche und optionale Diagnosedatenerfassung. 
- RequiredData (1) sendet die erforderlichen Diagnosedaten, deaktiviert jedoch die optionale Diagnosedatenerfassung. Microsoft Edge sendet die erforderlichen Diagnosedaten, die notwendig sind, um Microsoft Edge sicher, aktuell und erwartungsgemäß zu halten. 
- Optional data (2) sendet optionale Diagnosedaten die Daten zur Browsernutzung, besuchten Websites und an Microsoft gesendete Absturzberichte umfassen, um Microsoft Edge sicher und aktuell zu halten und die erwartete Leistung zu erzielen. Sie werden verwendet, um Microsoft Edge und andere Microsoft-Produkte und -Dienste für alle Benutzer zu verbessern.

Unter Windows 7, Windows 8/8.1 und macOS steuert diese Richtlinie das Senden der erforderlichen und optionalen Daten an Microsoft.

Wenn Sie diese Richtlinie nicht konfigurieren oder deaktivieren, verwendet Microsoft Edge standardmäßig die Einstellungen des Benutzers.

### <a name="deprecated-enable-usage-and-crash-related-data-reporting"></a>(VERALTET) Aktivieren der Berichterstellung für Nutzung und Absturz.

Die Richtlinie **MetricsReportingEnabled** ermöglicht die Erstellung von Berichten zu Nutzungs- und Absturzdaten über Microsoft Edge an Microsoft.

Microsoft Edge erfasst eine Reihe erforderlicher Daten, die benötigt werden, um das Produkt sicher, auf dem neuesten Stand und erwartungsgemäß leistungsfähig zu halten. Diese Daten umfassen grundlegende Informationen zur Gerätekonnektivität und -konfiguration von Microsoft Edge über die aktuelle Zustimmung zur Datenerfassung, die App-Version und den Installationsstatus bezüglich Ihrer Installation von Microsoft Edge. Diese Datenerfassung kann durch Deaktivieren der Richtlinie deaktiviert werden.

Aktivieren Sie diese Richtlinie, um Berichte zu Nutzungs- und Absturzdaten an Microsoft zu senden. Deaktivieren Sie diese Richtlinie, wenn Sie die Daten nicht an Microsoft senden möchten. In beiden Fällen können Benutzer die Einstellung weder ändern noch außer Kraft setzen.

Wenn Microsoft Edge unter Windows 10 ausgeführt wird:

- Wenn diese Richtlinie nicht konfiguriert ist, wird für Microsoft Edge standardmäßig die Einstellung für Windows-Diagnosedaten verwendet.
- Wenn diese Richtlinie aktiviert ist, sendet Microsoft Edge nur dann Nutzungsdaten, wenn die Einstellung für Windows-Diagnosedaten auf **Erweitert** oder **Vollständig** festgelegt ist.
  - Wenn diese Richtlinie aktiviert ist, sendet Microsoft Edge nur Verwendungsdaten, wenn [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices) ebenfalls aktiviert ist.
- Wenn diese Richtlinie deaktiviert ist, werden von Microsoft Edge keine Nutzungsdaten gesendet. Absturzdaten werden basierend auf der Einstellung für Windows-Diagnosedaten gesendet. [Weitere Informationen zu den Einstellungen für Windows-Diagnosedaten](/windows/privacy/configure-windows-diagnostic-data-in-your-organization).

Wenn Microsoft Edge unter Windows 7, 8 und macOS ausgeführt wird:

- Wenn diese Richtlinie nicht konfiguriert ist, wird für Microsoft Edge standardmäßig die Benutzereinstellung verwendet.
-  Wenn diese Richtlinie aktiviert ist, sendet Microsoft Edge nur Verwendungsdaten, wenn [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices) ebenfalls aktiviert ist.

### <a name="deprecated-send-site-information-to-improve-microsoft-services"></a>(VERALTET) Senden von Websiteinformationen, um die Microsoft-Dienste zu verbessern.

Die Richtlinie **SendSiteInformationToImproveServices** ermöglicht das Senden von Informationen über besuchte Websites in Microsoft Edge an Microsoft, um Produkte und Dienste von Microsoft wie z. B. die Suche zu verbessern.

Aktivieren Sie diese Richtlinie, um Informationen zu den Websites, die in Microsoft Edge besucht wurden, an Microsoft zu senden. Deaktivieren Sie diese Richtlinie, um keine Informationen zu den Websites, die in Microsoft Edge besucht wurden, an Microsoft zu senden. In beiden Fällen können Benutzer die Einstellung weder ändern noch außer Kraft setzen.

Wenn Microsoft Edge unter Windows 10 ausgeführt wird:

- Wenn diese Richtlinie nicht konfiguriert ist, wird für Microsoft Edge standardmäßig die Einstellung für Windows-Diagnosedaten verwendet.
- Wenn diese Richtlinie aktiviert ist, sendet Microsoft Edge nur dann Informationen zu besuchten Websites, wenn die Einstellung für Windows-Diagnosedaten auf **Vollständig** festgelegt ist.
  - Wenn diese Richtlinie aktiviert ist, sendet Microsoft Edge nur Verwendungsdaten, wenn [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) ebenfalls aktiviert ist. 
- Wenn diese Richtlinie deaktiviert ist, werden von Microsoft Edge keine Informationen zu besuchten Websites gesendet. [Weitere Informationen zu den Einstellungen für Windows-Diagnosedaten](/windows/privacy/configure-windows-diagnostic-data-in-your-organization)

Wenn Microsoft Edge unter Windows 7, 8 und macOS ausgeführt wird:

- Wenn diese Richtlinie aktiviert ist, sendet Microsoft Edge nur Verwendungsdaten, wenn [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) ebenfalls aktiviert ist.
- Wenn diese Richtlinie nicht konfiguriert ist, wird für Microsoft Edge standardmäßig die Benutzereinstellung verwendet.

## <a name="implementation-details"></a>Einzelheiten zur Implementierung

Für Nicht-Windows 10-Geräte: 
- Wenn die Richtlinie [DiagnosticData](./microsoft-edge-policies.md#diagnosticdata) konfiguriert ist, hat Sie Vorrang vor [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) und [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices). 
- Wenn die Richtlinie [DiagnosticData](./microsoft-edge-policies.md#diagnosticdata) nicht konfiguriert ist, hört Microsoft Edge auf [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) und [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices).  

Damit Windows 10 unsere Implementierung mit der Abhängigkeit von der Einstellung der Windows-Diagnosedaten verstehen kann, gibt die folgende Tabelle an, ob  **Erforderliche** und **Optionale** Diagnosedaten an Microsoft gesendet werden.

| Einstellung für Windows-Diagnosedaten | Erforderliche Diagnosedaten  | Optionale Diagnosedaten |
|---------------------------------|-----------------------------------------------|-----------------------------------------------------|
| Sicherheit                        | Nicht gesendet                                      | Nicht gesendet                                            |
| Einfach                           | Gesendet                                      | Nicht gesendet                                            |
| Erweitert                        | Gesendet                                          | Nicht gesendet                                            |
| Vollständig                            | Gesendet                                          | Gesendet                                                |

> [!IMPORTANT]
> Microsoft Edge unterstützt **MetricsReportingEnabled** und **SendSiteInfoToImproveServices** für Microsoft Edge-Versionen 86 bis inklusive 88. In der Microsoft Edge-Version 89 werden **MetricsReportingEnabled** und **SendSiteInfoToImproveServices** nicht mehr unterstützt, und auf Nicht-Windows 10-Plattformen standardmäßig auf **DiagnosticData** oder die Richtlinie **Telemetrie zulassen** für Windows 10 gesetzt.

## <a name="additional-privacy-policy-options"></a>Zusätzliche Datenschutzrichtlinien-Optionen

Möglicherweise möchten Sie die folgenden Gruppenrichtlinien im Zusammenhang mit dem Datenschutz berücksichtigen:

- Blockieren von Cookies auf bestimmten Websites
- Blockieren der Cookies von Drittanbietern
- DNT konfigurieren
- Deaktivieren des InPrivate-Modus

## <a name="see-also"></a>Weitere Informationen:

- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)
- [Microsoft Edge-Richtlinien](microsoft-edge-policies.md)
- [Whitepaper zum Microsoft Edge-Datenschutz](/microsoft-edge/privacy-whitepaper)