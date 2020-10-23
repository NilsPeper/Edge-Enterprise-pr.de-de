---
title: Microsoft Edge Enterprise-Synchronisierung
ms.author: scottbo
author: dan-wesley
manager: silvanam
ms.date: 10/21/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Edge Enterprise-Synchronisierung
ms.openlocfilehash: e51346d9bab83228c42a84a7a14ee45dc9b463a7
ms.sourcegitcommit: b32d8d64ae65dc5a46e47b7c34b0211097a0cc65
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/21/2020
ms.locfileid: "11133130"
---
# Microsoft Edge Enterprise-Synchronisierung

In diesem Artikel wird erläutert, wie Sie mit Microsoft Edge Favoriten, Kennwörter und andere Browserdaten auf allen angemeldeten Geräten synchronisieren können.

> [!NOTE]
> Dieser Artikel bezieht sich auf Microsoft Edge Version 77 oder neuer.

## Übersicht

Dank der Microsoft Edge-Synchronisierung können Benutzer auf ihre Browserdaten über alle angemeldeten Geräte hinweg zugreifen. Zu den von der Synchronisierung unterstützten Daten gehören:

- Favoriten
- Kennwörter
- Adressen und mehr (Formulareinträge)
- Sammlungen
- Einstellungen

Die Synchronisierungsfunktion wird nach Zustimmung des Benutzers aktiviert, und dieser kann die Synchronisierung für jeden der oben aufgeführten Datentypen aktivieren oder deaktivieren.

> [!NOTE]
> Zusätzliche Geräteverbindungs- und Konfigurationsdaten (wie Gerätename, Marke und Modell) werden hochgeladen, um die Synchronisationsfunktionalität zu unterstützen.

## Voraussetzungen

Die Synchronisierung von Microsoft Edge für Azure Active Directory (Azure AD)-Konten ist für jedes der folgenden Abonnements verfügbar:

- Azure AD Premium (P1 und P2)
- M365 Business Premium
- Office365 E1 und höher
- Azure Information Protection (AIP) (P1 & P2)
- Alle EDU-Abonnements (Microsoft Apps für Studenten oder Dozenten, Exchange Online für Studenten oder Dozenten, O365 A1 oder höher, M365 A1 oder höher oder Azure Information Protection P1 oder P2 für Studenten oder Dozenten)

## Konfigurieren der Microsoft Edge-Synchronisierung

Konfigurationsoptionen für die Microsoft Edge-Synchronisierung stehen über den Azure Information Protection (AIP)-Dienst zur Verfügung. Wenn AIP für einen Mandanten aktiviert ist, können alle Benutzer Microsoft Edge-Daten unabhängig von der Lizenzierung synchronisieren. Anweisungen zum Aktivieren von AIP finden Sie [hier](https://docs.microsoft.com/azure/information-protection/activate-office365).

Um die Synchronisierung auf eine bestimmte Benutzergruppe zu beschränken, können Sie die [AIP-Richtlinie zur Onboarding-Steuerung](https://docs.microsoft.com/powershell/module/aipservice/set-aipserviceonboardingcontrolpolicy?view=azureipps) für diese Benutzer aktivieren. Wenn die Synchronisierung immer noch nicht verfügbar ist, nachdem Sie sich vergewissert haben, dass das Onboarding für alle erforderlichen Benutzer erfolgt ist, stellen Sie mithilfe des PowerShell-Cmdlets [Get-AIPServiceIPCv3](https://docs.microsoft.com/powershell/module/aipservice/get-aipserviceipcv3?view=azureipps)  sicher, dass IPCv3Service aktiviert ist.

> [!CAUTION]
> Die Aktivierung von Azure Information Protection erlaubt auch anderen Anwendungen, wie z.B. Microsoft Word oder Microsoft Outlook, Inhalte mit AIP zu schützen. Darüber hinaus wird jede Onboarding-Kontrollrichtlinie, die zur Einschränkung der Edge-Synchronisierung verwendet wird, auch andere Anwendungen daran hindern, Inhalte mithilfe von AIP zu schützen.

## Microsoft Edge und Enterprise State Roaming

Der neue Microsoft Edge ist eine plattformübergreifende Anwendung mit erweiterten Möglichkeiten zur Synchronisierung von Benutzerdaten auf allen Geräten und nicht mehr Teil von Azure AD Enterprise State Roaming. Das neue Microsoft Edge erfüllt jedoch die ESR-Datenschutzoptionen wie z.B. die Möglichkeit, einen eigenen Schlüssel zu verwenden. Weitere Informationen finden sie unter [Microsoft Edge und Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).

## Synchronisierungs-Gruppenrichtlinien

Die folgenden Gruppenrichtlinien wirken sich auf die Microsoft Edge-Synchronisierung aus:

- [SyncDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled): Deaktiviert die Synchronisierung vollständig.
- [SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled): Deaktiviert das Speichern des Browserverlaufs und die Synchronisierung. Die Synchronisierung geöffneter Registerkarten wird durch diese Richtlinie ebenfalls deaktiviert.
- [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled): Konfigurieren Sie die Liste der Typen, die von der Synchronisierung ausgeschlossen werden.
- [RoamingProfileSupportEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilesupportenabled): Zulassen, dass Active Directory (AD)-Profile lokalen Speicher verwenden. Weitere Informationen finden Sie unter [Lokale Synchronisierung für Active Directory (AD)-Benutzende](https://docs.microsoft.com/DeployEdge/microsoft-edge-on-premises-sync).
- [ForceSync]( https://docs.microsoft.com/deployedge/microsoft-edge-policies#forcesync): Aktivieren Sie die Synchronisierung standardmäßig, und fordern Sie keine Benutzerzustimmung zur Synchronisierung an.  

## Häufig gestellte Fragen

### SICHERHEIT und von SERVER-/DATENKONFORMITÄT

#### Werden die synchronisierten Daten verschlüsselt? 

Die Daten werden beim Transport mithilfe von TLS 1.2 oder höher verschlüsselt. Die meisten Datentypen werden im Ruhezustand im Microsoft-Dienst zusätzlich mit AES256 verschlüsselt. 

#### Wo werden Microsoft Edge-Synchronisierungsdaten für gespeichert?

Synchronisierte Daten für Azure AD-Konten werden auf sicheren Servern entsprechend der Mandanten-ID gespeichert. Beispielsweise werden die Daten eines in den USA registrierten Mandanten auf Servern gespeichert, die sich in dieser geografischen Region befinden, und verwenden die gleiche Speicherlösung wie Office-Anwendungen.

#### Verlassen die Daten jemals die Cloud von Microsoft, abgesehen von der Synchronisierung mit Microsoft Edge?

Nein.

#### Können Mandantenadministratoren ihren eigenen Schlüssel mitbringen?

Ja, über [Azure Information Protection](https://azure.microsoft.com/services/information-protection/).

#### Unter welche Nutzungsbedingungen fällt die Unternehmenssynchronisierung?

Die Nutzungsbedingungen sind die gleichen wie bei Ihrem Azure AD-Abonnement. Alle Nutzungsbedingungen von Azure AD fallen letztlich unter die [Onlinedienst-Vertragsbedingungen](https://www.microsoft.com/licensing/product-licensing/products) von Microsoft.

#### Unterstützt Microsoft Edge Government Community Cloud (GCC) High-Compliance?

Derzeit nicht. GCC High ist Tarifstufe D, während Microsoft Edge nur bis zur Tarifstufe C Unterstützung bietet.

### ANWENDEN DER SYNCHRONISIERUNG

#### Was gilt für Kunden aus Unternehmen und dem Bildungsbereich, die sich für Microsoft Edge Legacy entscheiden?

Die aktuelle Version des Microsoft Edge-Browsers ist weiterhin im ESR-Angebot verfügbar.

#### Warum brauche ich ein Premium-Abonnement für Azure AD für die Synchronisierung?

Die Unternehmenssynchronisierung ist von Azure Information Protection abhängig, das nicht in allen Azure AD-Tarifstufen verfügbar ist.

#### Basiert die Microsoft Edge-Synchronisierung auf Enterprise State Roaming (ESR)?

Nein. ESR kann verwendet werden, um die Synchronisierung zu aktivieren, aber Microsoft Edge-Synchronisierung ist nicht Teil von ESR. Weitere Informationen finden sie unter [Microsoft Edge-Synchronisierung](microsoft-edge-enterprise-sync.md) sowie [Microsoft Edge und Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).

#### Wird Microsoft Edge jemals die Synchronisierung zwischen Microsoft Edge und IE unterstützen?

Es gibt keine Pläne, diese Synchronisierung zu unterstützen. Wenn Sie in Ihrer Umgebung noch IE zur Unterstützung von Legacyanwendungen benötigen, sollten Sie unseren [neuen IE-Modus](https://docs.microsoft.com/deployedge/edge-ie-mode) in Betracht ziehen.

#### Wird der neue Microsoft Edge-Browser mit der Vorgängerversion von Microsoft Edge synchronisiert?

Nein. Wir sind der Meinung, dass die Verbindung dieser beiden Ökosysteme zu Kompromissen bezüglich der Zuverlässigkeit der Synchronisation im neuen Microsoft Edge führen würde. Wir stellen sicher, dass vorhandene Daten zum neuen Microsoft Edge migriert werden. Benutzer können zudem Daten aus dem Browser Ihrer Wahl importieren. Dies bedeutet auch, dass der neue Microsoft Edge-Browser keine Möglichkeit für eine Synchronisierung mit dem IE bietet.

### VERWALTEN DER SYNCHRONISIERUNG

#### Kann ich verhindern, dass meine Benutzer mit einem persönlichen Mandanten synchronisiert werden?

Nicht direkt. Sie können jedoch mithilfe der Richtlinie [RestrictSigninToPattern](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern) festlegen, welche Profile sich bei Microsoft Edge anmelden können.

## Weitere Informationen

- [Angebotsseite für Microsoft Edge für Unternehmen](https://aka.ms/EdgeEnterprise)
- [Microsoft Edge und Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md)
