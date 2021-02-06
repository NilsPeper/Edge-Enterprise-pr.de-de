---
title: Microsoft Edge-Support für Microsoft Defender SmartScreen
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 02/05/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Edge-Support für Microsoft Defender SmartScreen
ms.openlocfilehash: 2de93b4ebe26b4a90592f7ee9143f6f775b682ce
ms.sourcegitcommit: c290b0b0fa6b7d7f94dcdfdda91302da733326ec
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2021
ms.locfileid: "11314688"
---
# Microsoft Edge-Support für Microsoft Defender SmartScreen

In diesem Artikel werden die Vorteile der Verwendung von Microsoft Defender SmartScreen beschrieben, dessen Funktionsweise erläutert und das Konfigurieren dieses Microsoft Edge-Features beschrieben.

> [!NOTE]
> Dieser Artikel bezieht sich auf Microsoft Edge Version77 oder höher.

Microsoft Defender SmartScreen ist ein Dienst, mit dem Microsoft Edge Sie beim Surfen im Internet schützt. Microsoft Defender SmartScreen stellt ein Frühwarnsystem bereit, um Benutzer bei Websites zu informieren, die an Phishingangriffen oder an der Verteilung von Schadsoftware über einen gezielten Angriff beteiligt sein könnten. Weitere Informationen finden Sie im [Video: Sicheres Browsen auf Microsoft Edge](microsoft-edge-video-security-smartscreen.md).

> [!NOTE]
> Vor Windows10, Version1703, wurde dieses Feature bei Verwendung innerhalb des Browsers SmartScreen-Filter und bei Verwendung außerhalb des Browsers Microsoft SmartScreen genannt.

## Die Vorteile von Microsoft Defender SmartScreen

Microsoft Defender SmartScreen bietet mehrere Vorteile, die in der folgenden Liste zusammengefasst sind. Diese Vorteile sind in der [Microsoft Defender SmartScreen-Dokumentation](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview#benefits-of-windows-defender-smartscreen) detailliert beschrieben. Ihre Vorteile:

- Schutz gegen Phishing- und Schadsoftware
- Zuverlässigkeitsbasierter URL- und App-Schutz
- Integration in das Betriebssystem
- Verbesserte Heuristik und Diagnosedaten
- Verwaltung durch Gruppenrichtlinien und Microsoft Intune
- Blockieren von URLs, die potenziell unerwünschten Anwendungen zugeordnet sind

## Grundlegendes zur Funktionsweise von Microsoft Defender SmartScreen

Eine Reihe von Eingaben tragen zu den Microsoft Defender SmartScreen-Warnungen bei. Daten werden aus mehreren Quellen empfangen, einschließlich Benutzerfeedback, Datenanbietern und Intelligence-Modellen. Diese Daten werden verwendet, um potenziell schädliche Inhalte zu erkennen. Microsoft Defender SmartScreen untersucht außerdem heruntergeladene Apps oder App-Installationsprogramme auf ihre Bösartigkeit. In beiden Szenarien warnt Microsoft Defender SmartScreen die Benutzer entsprechend zu verdächtigen Inhalten.

### Websiteanalyse

Microsoft Defender SmartScreen ermittelt folgendermaßen, ob eine Website potenziell schädlich ist:

- Analyse der besuchten Websites nach Hinweisen auf verdächtiges Verhalten.
- Überprüfung der besuchten Websites anhand eines dynamischen Datensatzes von gemeldeten Phishing-Websites.

Wenn Microsoft Defender SmartScreen feststellt, dass eine Seite bösartig ist, wird eine Warnseite angezeigt, um den Benutzer zu benachrichtigen, dass diese Website als unsicher gemeldet wurde. Der nächste Screenshot zeigt ein Beispiel für eine Microsoft Defender SmartScreen-Warnung, die angezeigt wird, wenn ein Benutzer versucht, eine bösartige Website zu öffnen.

![Blockierungsseite von Microsoft Defender SmartScreen für einen Link zu einer externen Website](media/microsoft-edge-security-smartscreen/microsoft-edge-smartscreen-warning.png)

Innerhalb der Warnmeldung können Benutzer eine Website als sicher oder unsicher melden. Weitere Informationen finden Sie unter [Eine Seite melden](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-set-individual-device#how-users-can-report-websites-as-safe-or-unsafe).

### Dateianalyse

Microsoft Defender SmartScreen ermittelt anhand vieler Kriterien, ob heruntergeladene Apps oder App-Installationsprogramme potenziell bösartig ist. Dazu zählen Download-Datenverkehr, Downloadverlauf, frühere Ergebnisse von Antivirenprogrammen und URL-Zuverlässigkeit.

- Als sicher bekannte Dateien werden ohne Benachrichtigung heruntergeladen.  
- Bei als bösartig eingestuften Dateien wird eine Warnung angezeigt, um den Benutzer darauf hinzuweisen, dass die Datei nicht sicher ist und als bösartig gemeldet wurde. Der nächste Screenshot zeigt ein Beispiel für eine Warnung für eine bösartige Datei.

  ![Microsoft Defender SmartScreen-Blockierbenachrichtigung für als bösartig eingestufte Datei](media/microsoft-edge-security-smartscreen/ms-edge-smartscreen-known-malicious.png)

- Bei unbekannten Dateien wird eine Warnung angezeigt, um den Benutzer darauf hinzuweisen, dass für der Download kein bekannter Fußabdruck vorliegt und somit Vorsicht geboten ist. Der nächste Screenshot zeigt ein Beispiel für eine Warnung vor einer unbekannten Datei.

  ![Microsoft Defender SmartScreen-Blockbenachrichtigung für Datei mit unbekannter Bewertung](media/microsoft-edge-security-smartscreen/ms-edge-smartscreen-unknown-malicious.png)

Nicht alle unbekannten Programme sind bösartig, und die Warnung zu unbekannten Objekten dient dazu, den Benutzern, die sie benötigen, Kontext und Hilfe bereitzustellen, insbesondere, wenn die Warnung unerwartet ist.

  ![Als bösartig eingestufte Datei behalten](media/microsoft-edge-security-smartscreen/ms-edge-smartscreen-unknown-malicious-keep.png)

Benutzer können die Anwendung aber trotzdem herunterladen und ausführen, indem sie auf **... | Behalten | Mehr anzeigen | Trotzdem behalten**.

> [!TIP]
> **Informationen für Enterprise-Kunden.** Standardmäßig erlaubt es Microsoft Defender SmartScreen Benutzern, Warnungen zu umgehen. Da diese Benutzerinteraktion potenziell riskant ist, sollten Sie sich diese [empfohlenen Gruppenrichtlinieneinstellungen](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-available-settings#recommended-group-policy-and-mdm-settings-for-your-organization) ansehen.

Verwenden Sie unsere [Demo-Website](https://demo.smartscreen.msft.net/) um zu sehen, wie Microsoft Defender SmartScreen auf verschiedene Szenarios reagiert.

## Microsoft Defender SmartScreen und Schutz der Privatsphäre

Microsoft Defender SmartScreen schützt Benutzer während des Surfens im Internet durch ein System zur Überprüfung der Zuverlässigkeit. Microsoft Edge übergibt relevante Informationen über eine URL oder Datei an den Microsoft Defender SmartScreen-Dienst, um die Zuverlässigkeitsprüfung zu starten. Bei der Überprüfung wird die Website oder Datei anhand dynamischer Listen von als gefährlich bekannten Websites und Dateien verglichen. Alle Anforderungen des Microsoft Defender SmartScreen-Diensts werden mit TLS-Verschlüsselung ausgeführt. Der Dienst gibt die Ergebnisse der Zuverlässigkeitsprüfung zurück, woraufhin Microsoft Edge u. U. eine Warnung für die Website oder Datei anzeigt. Diese Ergebnisse werden lokal auf dem Gerät gespeichert.

Der Microsoft Defender SmartScreen-Dienst speichert Daten zu Zuverlässigkeitsüberprüfungen. Wenn eine neue Website identifiziert wird, fügt der Dienst sie einer dynamischer Datenbank mit bekannten bösartigen URLs und Dateien hinzu. Diese Daten werden auf sicheren Microsoft-Servern gespeichert und nur für Microsoft Security-Dienste verwendet. Diese Daten werden nicht verwendet, um Benutzer in irgendeiner Weise zu identifizieren oder anzusprechen. Durch das Löschen des Browser-Caches werden alle lokal gespeicherten Microsoft Defender SmartScreen-URL-Daten gelöscht. Wenn der Downloadverlauf gelöscht wird, werden alle lokal gespeicherten SmartScreen-Daten zu Dateidownloads entfernt.

Weitere Informationen zu Microsoft Defender SmartScreen und Datenschutz in Microsoft Edge finden Sie im [Whitepaper zum Microsoft Edge-Datenschutz](https://docs.microsoft.com/microsoft-edge/privacy-whitepaper#smartscreen).

## Microsoft Defender SmartScreen-Setup für Administratoren

Administratoren können Microsoft Defender SmartScreen mithilfe von Gruppenrichtlinien, Microsoft Intune oder MDM-Einstellungen (Mobile Device Management) konfigurieren. Je nachdem, wie Sie Microsoft Defender SmartScreen einrichten, können Sie eine Warnseite für Mitarbeiter anzeigen und sie die entsprechende Website aufrufen lassen, oder die Website vollständig blockieren.

### Microsoft Defender SmartScreen-Setup mithilfe von Gruppenrichtlinien

Eine umfassende Liste von SmartScreen-Richtlinien finden Sie unter [Microsoft Defender SmartScreen-Einstellungen](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#smartscreen-settings).

### Microsoft Defender SmartScreen-Setup mithilfe von MDM

Weitere Informationen finden Sie unter:

- [Windows Intune-Einstellungen für Microsoft Defender SmartScreen](https://docs.microsoft.com/mem/intune/protect/endpoint-protection-windows-10#windows-defender-smartscreen-settings)
- [MDM-Richtlinieneinstellungen](https://docs.microsoft.com/mem/intune/protect/endpoint-protection-windows-10#windows-defender-smartscreen-settings)

## Microsoft Defender SmartScreen-Setup für Benutzer

Microsoft Defender SmartScreen ist standardmäßig für Microsoft Edge aktiviert. Zum Deaktivieren von Microsoft Defender SmartScreen wechseln Sie zu *edge://settings/privacy > Dienste > Microsoft Defender SmartScreen*. Diese Einstellung ist für alle Profile identisch, die mit der Installation von Microsoft Edge auf einem Gerät verbunden sind. Diese Einstellung wird nicht geräteübergreifend synchronisiert. Die Einstellung gilt für InPrivate-Browsing und den Gastmodus. Wenn ein Gerät über Gruppenrichtlinien verwaltet wird, die von einer Organisation festgelegt wurden, wird diese Konfiguration in *edge://settings/privacy* übernommen.

> [!NOTE]
> Benutzer können Microsoft Defender SmartScreen für ein einzelnes Gerät einrichten, es sei denn, Gruppenrichtlinien oder MDM sind so konfiguriert, dass dies verhindert wird. Weitere Informationen finden Sie unter [Einrichten und Verwenden von Microsoft Defender SmartScreen auf einzelnen Geräten](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-set-individual-device).

## Häufig gestellte Fragen

### Wie funktioniert das System zum Überprüfen der Zuverlässigkeit?

Während Sie im Internet surfen, kategorisiert Microsoft Defender SmartScreen Websites und Downloads als "häufigster Datenverkehr", "gefährlich" oder "unbekannt". Der "häufigste Datenverkehr" umfasst Websites, die von Microsoft Defender SmartScreen als vertrauenswürdig eingestuft wurden. Wenn Sie zu einer Website wechseln, die als gefährlich gekennzeichnet ist, blockiert Microsoft Defender SmartScreen sofort den Zugriff darauf. Wenn Sie zu einer unbekannten Website wechseln, überprüft Microsoft DefenderSmartScreen ihren Zuverlässigkeitsgrad, um zu bestimmen, ob der Zugriff darauf zugelassen werden soll.

## Weitere Informationen

- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)
- [Video: Sicheres Browsen in Microsoft Edge](microsoft-edge-video-security-smartscreen.md)
- [Übersicht über Microsoft Defender SmartScreen](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview)
- [Schutz vor Bedrohungen](https://docs.microsoft.com/windows/security/threat-protection/index)
- [Schutz vor potenziell unerwünschten Anwendungen](https://docs.microsoft.com/DeployEdge/microsoft-edge-potentially-unwanted-apps)