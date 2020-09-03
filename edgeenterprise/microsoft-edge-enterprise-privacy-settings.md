---
title: Microsoft Edge-Datenschutzeinstellungen für Unternehmen
ms.author: likravit
author: dan-wesley
manager: srugh
ms.date: 05/26/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Konfigurieren von Microsoft Edge-Datenschutzeinstellungen für Unternehmen
ms.openlocfilehash: 2b7a33087ae5110c53d18b3192486d4ae62fa540
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/31/2020
ms.locfileid: "10980048"
---
# Konfigurieren von Microsoft Edge-Richtlinien zur Unterstützung des Datenschutzes in Unternehmen

Microsoft verpflichtet sich, Unternehmen die Informationen und Steuerelemente bereitzustellen, die für die Auswahl der Datensammlung in Microsoft Edge erforderlich sind.

## Übersicht

Ist Microsoft Edge auf Windows-Plattformen installiert, werden standardmäßig keine Diagnosedaten oder Siteinformationen an Microsoft gesendet. Bei der Bereitstellung von Microsoft Edge unter Windows 10 werden Diagnosedaten standardmäßig basierend auf der [Einstellung für Windows-Diagnosedaten](https://go.microsoft.com/fwlink/?linkid=2099569) der Benutzer gesendet.

Sie können darüber hinaus mit den folgenden Gruppenrichtlinien konfigurieren, wie Microsoft Edge die Datenerfassung für Ihre Organisation behandelt:

- [MetricsReportingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#metricsreportingenabled): Aktivieren der Berichterstellung für Nutzungs- und Absturzdaten.
- [SendSiteInfoToImproveServices](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices): Senden von Siteinformationen, um Microsoft-Dienste zu verbessern.

## Konfigurieren von Richtlinieneinstellungen

Laden Sie zunächst die aktuelle Microsoft Edge-Richtlinienvorlage herunter, und verwenden Sie diese (weitere Informationen finden Sie unter [Konfigurieren von Microsoft Edge](configure-microsoft-edge.md)).

### Aktivieren der Berichterstellung für Nutzungs- und Absturzdaten

Diese Richtlinie ermöglicht die Erstellung von Berichten zu Nutzungs- und Absturzdaten über Microsoft Edge an Microsoft.

Microsoft Edge erfasst eine Reihe erforderlicher Daten, die benötigt werden, um das Produkt sicher, auf dem neuesten Stand und leistungsfähig zu halten. Diese Daten umfassen grundlegende Informationen zur Gerätekonnektivität und -konfiguration von Microsoft Edge über die aktuelle Zustimmung zur Datenerfassung, die App-Version und den Installationsstatus bezüglich Ihrer Installation von Microsoft Edge. Diese Datenerfassung kann durch Deaktivieren der Richtlinie deaktiviert werden.

Aktivieren Sie diese Richtlinie, um Berichte zu Nutzungs- und Absturzdaten an Microsoft zu senden. Deaktivieren Sie diese Richtlinie, wenn Sie die Daten nicht an Microsoft senden möchten. In beiden Fällen können Benutzer die Einstellung weder ändern noch außer Kraft setzen.

Wenn Microsoft Edge unter Windows 10 ausgeführt wird:

- Wenn diese Richtlinie nicht konfiguriert ist, wird für Microsoft Edge standardmäßig die Einstellung für Windows-Diagnosedaten verwendet.
- Wenn diese Richtlinie aktiviert ist, sendet Microsoft Edge nur dann Nutzungsdaten, wenn die Einstellung für Windows-Diagnosedaten auf **Erweitert** oder **Vollständig** festgelegt ist.
- Wenn diese Richtlinie deaktiviert ist, werden von Microsoft Edge keine Nutzungsdaten gesendet. Absturzdaten werden basierend auf der Einstellung für Windows-Diagnosedaten gesendet. [Weitere Informationen zu den Einstellungen für Windows-Diagnosedaten](https://go.microsoft.com/fwlink/?linkid=2099569).

Wenn Microsoft Edge unter Windows 7, 8 und macOS ausgeführt wird:

- Wenn diese Richtlinie nicht konfiguriert ist, wird für Microsoft Edge standardmäßig die Benutzereinstellung verwendet.

### Senden von Siteinformationen, um Microsoft-Dienste zu verbessern

Diese Richtlinie ermöglicht das Senden von Informationen über besuchte Websites in Microsoft Edge an Microsoft, um Produkte und Dienste von Microsoft wie z.B. die Suche zu verbessern.

Aktivieren Sie diese Richtlinie, um Informationen zu den Websites, die in Microsoft Edge besucht wurden, an Microsoft zu senden. Deaktivieren Sie diese Richtlinie, um keine Informationen zu den Websites, die in Microsoft Edge besucht wurden, an Microsoft zu senden. In beiden Fällen können Benutzer die Einstellung weder ändern noch außer Kraft setzen.

Wenn Microsoft Edge unter Windows 10 ausgeführt wird:

- Wenn diese Richtlinie nicht konfiguriert ist, wird für Microsoft Edge standardmäßig die Einstellung für Windows-Diagnosedaten verwendet.
- Wenn diese Richtlinie aktiviert ist, sendet Microsoft Edge nur dann Informationen zu besuchten Websites, wenn die Einstellung für Windows-Diagnosedaten auf **Vollständig** festgelegt ist.
- Wenn diese Richtlinie deaktiviert ist, werden von Microsoft Edge keine Informationen zu besuchten Websites gesendet. [Weitere Informationen zu den Einstellungen für Windows-Diagnosedaten](https://go.microsoft.com/fwlink/?linkid=2099569)

Wenn Microsoft Edge unter Windows 7, 8 und macOS ausgeführt wird:

- Wenn diese Richtlinie nicht konfiguriert ist, wird für Microsoft Edge standardmäßig die Benutzereinstellung verwendet.

## Einzelheiten zur Implementierung

Für Windows10: Um unsere Implementierung bezüglich der Abhängigkeit von der Einstellung für Windows-Diagnosedaten verständlich zu machen, wird in der folgenden Tabelle die Konfiguration beschrieben, wenn die Optionen **Aktivieren der Berichterstellung für Nutzungs- und Absturzdaten** und **Senden von Siteinformationen, um Microsoft-Dienste zu verbessern** nicht konfiguriert wurden.

| Einstellung für Windows-Diagnosedaten | Aktivieren der Berichterstellung für Nutzungs- und Absturzdaten | Senden von Siteinformationen, um Microsoft-Dienste zu verbessern |
|---------------------------------|-----------------------------------------------|-----------------------------------------------------|
| Sicherheit                        | Nicht gesendet                                      | Nicht gesendet                                            |
| Einfach                           | Nicht gesendet                                      | Nicht gesendet                                            |
| Erweitert                        | Gesendet                                          | Nicht gesendet                                            |
| Vollständig                            | Gesendet                                          | Gesendet                                                |

Wenn Ihre Konfigurationen für Windows10 nicht in Übereinstimmung mit der vorstehenden Tabelle konfiguriert sind, wird auf die Einstellung für die geringere Datenerfassung zurückgegriffen.

Zum Beispiel:

- Sie haben die Richtlinie "Aktivieren der Berichterstellung für Nutzungs- und Absturzdaten" auf **Aktiviert** festgelegt, die Einstellung für die Windows-Diagnosedaten ist jedoch auf **Einfach** festgelegt. Es werden keine Nutzungs- und Absturzdaten gesendet.
- Sie haben die Richtlinie "Senden von Siteinformationen, um Microsoft-Dienste zu verbessern" auf **Deaktiviert** festgelegt, die Einstellung für Windows-Diagnosedaten jedoch auf **Vollständig** festgelegt. Es werden keine Informationen zu den Websites, die besucht wurden, gesendet.

Die richtige Implementierung der voranstehenden Einstellungen besteht darin, die Richtlinie "Aktivieren der Berichterstellung für Nutzungs- und Absturzdaten" auf **Aktiviert** und die Einstellung für Windows- Diagnosedaten auf **Erweitert** oder **Vollständig** festzulegen.

## Zusätzliche Datenschutzrichtlinien-Optionen

Möglicherweise möchten Sie die folgenden Gruppenrichtlinien im Zusammenhang mit dem Datenschutz berücksichtigen:

- Blockieren von Cookies auf bestimmten Websites
- Blockieren der Cookies von Drittanbietern
- DNT konfigurieren
- Deaktivieren des InPrivate-Modus

## Weitere Informationen:

- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)
- [Microsoft Edge-Richtlinien](microsoft-edge-policies.md)
- [Whitepaper zum Microsoft Edge-Datenschutz](https://docs.microsoft.com/microsoft-edge/privacy-whitepaper)
