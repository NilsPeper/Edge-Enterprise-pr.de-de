---
title: Microsoft Edge und Enterprise State Roaming
ms.author: kvice
author: dan-wesley
manager: laurawi
ms.date: 02/14/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Edge und Enterprise State Roaming
ms.openlocfilehash: 6090ecfda2f792d49e452771943bc6348066a3d8
ms.sourcegitcommit: 90b8eab62edbed0e0a84780abd7d3854bf95c130
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "11328057"
---
# Microsoft Edge und Enterprise State Roaming

Dieser Artikel erklärt, wie sich die Teilnahme von Microsoft Edge am Enterprise State Roaming (ESR)-Angebot ändert, um eine bessere Synchronisierung zwischen Plattformen und Geräten zu ermöglichen.

> [!NOTE]
> Dieser Artikel bezieht sich auf Microsoft Edge Version 77 oder neuer.

##  <a name="introduction"></a>Einführung

Mit Windows 10 [Azure Active Directory (Azure AD)](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-whatis) haben Benutzer die Möglichkeit, ihre Benutzereinstellungen und Einstellungen der Anwendungsdaten in der Cloud sicher zu synchronisieren. [Enterprise State Roaming (ESR)](https://docs.microsoft.com/azure/active-directory/devices/enterprise-state-roaming-overview) ermöglicht Benutzern eine einheitliche Erfahrung auf allen Windows-Geräten und verringert die benötigte Zeit für die Konfiguration eines neuen Geräts.

Durch die Übernahme der Chromium-Plattform ist die Synchronisierungslösung von Microsoft Edge nun vom Windows-Synchronisierungssystem getrennt. Dies wirkt sich auf die Beziehung zwischen Microsoft Edge und dem ESR-Angebot aus.

> [!IMPORTANT]
> Die neue Microsoft Edge nimmt nicht am ESR-Angebot teil.

##  <a name="what’s-changing-with-microsoft-edge"></a>Was ändert sich mit Microsoft Edge?

Mit dem neuen Microsoft Edge ist die Synchronisierungslösung nicht an das Synchronisierungs-Ökosystem von Windows gebunden. Dadurch können wir Microsoft Edge auf allen Plattformen anbieten, z. B. auf Windows 7, Windows 8 1, iOS, Android und macOS. Zudem können wir Synchronisierung auch für nicht primäre Konten unter Windows anbieten. Darüber hinaus können wir Microsoft Edge mit einer häufigeren und flexibleren Freigabekadenz als Windows ausliefern. Weitere Informationen finden Sie unter [Windows-Updates zur Unterstützung der nächsten Version von Microsoft Edge](microsoft-edge-sysupdate-windows-updates.md). Alle diese Faktoren führten zu der Notwendigkeit, die Teilnahme von Microsoft Edge am ESR-Angebot neu zu bewerten.

ESR ist als Windows-Produktangebot für den Umgang mit Daten von Windows-Geräten konzipiert. Die Synchronisierung mit Microsoft Edge geht über Windows-Geräte hinaus. Und da die Daten sich über diese Geräte verteilen, ist es schwierig, das Microsoft Edge-Synchronisierungsangebot im Rahmen von ESR zu definieren. Um Funktionsweise und Verwaltung der Synchronisierung zu vereinfachen und die hervorgehobenen Änderungen zu berücksichtigen, wurde beschlossen, Microsoft Edge aus dem ESR-Angebot herauszunehmen.

##  <a name="does-this-mean-enterprises-will-lose-the-abilities-they-had-as-part-of-esr"></a>Bedeutet dies, dass Unternehmen die Möglichkeiten verlieren, die Sie im Rahmen von ESR hatten?

Nein. Microsoft Edge wird weiterhin die meisten der im ESR-Angebot bereitgestellten Funktionen unterstützen.

###  <a name="unified-experience-across-devices-and-new-device-configuration-time"></a>Einheitliche geräteübergreifende Erfahrung und Zeit für die Konfiguration neuer Geräte

Wenn ein Benutzer mit einem Azure Active Directory (Azure AD-Konto) auf seinem Windows-Gerät angemeldet ist, erbt Microsoft Edge diese Identität beim ersten Start des neuen Browsers.

Nachdem ein Benutzer ausdrücklich zugestimmt hat, die Synchronisierung im neuen Microsoft Edge einzuschalten, synchronisiert der Browser alle Browserdaten wie Favoriten, Passwörter und Verlauf. Dies gewährleistet eine einheitliche Benutzererfahrung auf allen Geräten und reduziert den Zeitaufwand für die Personalisierung des Browsers.

###  <a name="separation-of-corporate-and-consumer-data"></a>Trennung von Unternehmens- und Kundendaten

Unternehmen haben die Kontrolle über ihre Daten, und es gibt keine Vermischung mit Unternehmensdaten in einem Kunden-Cloudkonto oder mit Kundendaten in einem Unternehmens-Cloudkonto.

###  <a name="enhanced-security"></a>Erhöhte Sicherheit

Daten werden automatisch über Azure Information Protection verschlüsselt, bevor sie das Windows 10-Gerät des Benutzers verlassen, und bleiben im Ruhezustand in der Cloud verschlüsselt. Alle Inhalte bleiben in der Cloud im Ruhezustand verschlüsselt, mit Ausnahme der Namespaces, wie z. B. Einstellungsnamen.

###  <a name="monitoring"></a>Überwachung

Durch die Integration in das Azure AD-Portal bieten wir Kontrolle und Transparenz darüber, wer die Einstellungen in Ihrem Unternehmen synchronisiert und auf welchen Geräten dies erfolgt. Diese Funktion wird in einer zukünftigen Version aktiviert.

###  <a name="management"></a>Verwaltung

Administratoren können festlegen, welche Mitglieder in Ihrer Organisation die Synchronisierung aktivieren können. Weitere Informationen finden sie unter [Konfigurieren von Microsoft Edge-Synchronisierung](microsoft-edge-enterprise-sync.md#configure-microsoft-edge-sync) und [Synchronisierungs-Gruppenrichtlinien](microsoft-edge-enterprise-sync.md#sync-group-policies). Zudem können Benutzer die Synchronisierung für jedes Ihrer Geräte aktivieren/deaktivieren und jedes Datenattribut einzeln für die Synchronisierung umschalten.

###  <a name="key-management"></a>Schlüsselverwaltung

Das Synchronisierungsfeature nutzt Azure Information Protection (AIP), um die synchronisierten Daten nur für den Benutzer und die Unternehmensadministratoren zu schützen. AIP unterstützt sowohl die Schlüsselverwaltung durch Microsoft (Standard) als auch die Verwendung Ihrer eigenen Schlüssel für die Cloud-Schlüsselverwaltung. Die von Ihrem Unternehmen verwendete Strategie zur Cloud-Schlüsselverwaltung ist für Microsoft Edge transparent und hat keinen Einfluss auf die Synchronisierungsfunktion.

> [!IMPORTANT]
> [Hold your own key (HYOK)](https://docs.microsoft.com/azure/information-protection/configure-adrms-restrictions) und der Active Directory Rights Management Service werden nicht unterstützt.

##  <a name="summary-of-sync-attributes"></a>Zusammenfassung der Synchronisierungsattribute

Die folgenden Datenattribute werden in der neuen Version von Microsoft Edge beim ersten Start synchronisiert:

- Favoriten
- Kennwörter
- Formularinhalte
- Verlauf
- Geöffnete Registerkarten (Sitzungen)
- Einstellungen (Voreinstellungen)
- Erweiterungen

Die Attribute aus der obige Liste unterscheiden sich von denen, die in Microsoft Edge Legacy synchronisiert werden können. (weitere Informationen zu Einstellungen für Microsoft Edge Legacy finden Sie unter [Roaming-Einstellungen für Windows 10](https://docs.microsoft.com/azure/active-directory/devices/enterprise-state-roaming-windows-settings-reference).) Benutzer können diese Attribute in den Microsoft Edge-Einstellungen einzeln aktivieren bzw. deaktivieren. Aufgrund der unterschiedlichen Attribute in den beiden Versionen (z. B. Verlauf) werden Benutzer möglicherweise aufgefordert, die Zustimmung zur Synchronisierung erneut zu erteilen.

> [!NOTE]
> Im Gegensatz zu Microsoft Edge Legacy verwendet das neue Microsoft Edge nicht die Windows-Anmeldeinformationsverwaltung für Kennwörter und synchronisiert diese daher nicht mit dem Internet Explorer oder anderen Anwendungen, die mit der Windows-Anmeldeinformationsverwaltung arbeiten.

##  <a name="terms-of-service"></a>Vertragsbedingungen

Die Nutzungsbedingungen für die Microsoft Edge-Synchronisierung gehören zur Microsoft-Softwarelizenz, die in Microsoft Edge unter *edge://terms* einsehbar ist.

##  <a name="additional-information"></a>Weitere Informationen

- [Angebotsseite für Microsoft Edge für Unternehmen](https://aka.ms/EdgeEnterprise)
- [Microsoft Edge-Synchronisierung](microsoft-edge-enterprise-sync.md)