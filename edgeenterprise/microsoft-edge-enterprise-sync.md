---
title: Konfigurieren der Microsoft Edge Enterprise-Synchronisierung
ms.author: scottbo
author: dan-wesley
manager: silvanam
ms.date: 03/08/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Administrator- und Benutzeroptionen zum Konfigurieren von Microsoft Edge zum Synchronisieren von Favoriten, Kennwörtern und anderen Browserdaten.
ms.openlocfilehash: 93af96bd864f08bb17bb1d6f0669f602a56fd8ca
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/24/2021
ms.locfileid: "11448119"
---
# <a name="configure-microsoft-edge-enterprise-sync"></a>Konfigurieren der Microsoft Edge Enterprise-Synchronisierung

In diesem Artikel wird erläutert, wie Administratoren Microsoft Edge konfigurieren können, um Favoriten, Kennwörter und andere Browserdaten von Benutzern über alle angemeldeten Geräte hinweg zu synchronisieren.

> [!NOTE]
> Gilt für Microsoft Edge Version 77 oder höher, sofern nicht anderes angegeben.

## <a name="overview"></a>Übersicht

Dank der Microsoft Edge-Synchronisierung können Benutzer auf ihre Browserdaten über alle angemeldeten Geräte hinweg zugreifen. Zu den von der Synchronisierung unterstützten Daten gehören:

- Favoriten
- Kennwörter
- Adressen und mehr (Formulareinträge)
- Sammlungen
- Einstellungen
- Erweiterung
- Geöffnete Registerkarten (verfügbar in Microsoft Edge, Version 88)
- Verlauf (verfügbar in Microsoft Edge, Version 88)

Die Synchronisierungsfunktion wird nach Zustimmung des Benutzers aktiviert, und Benutzer können die Synchronisierung für die beiden oben aufgeführten Datentypen aktivieren oder deaktivieren. Wenn ein Benutzer ein Synchronisierungsproblem hat, muss er möglicherweise die Synchronisierung unter **Einstellungen** > **Profile** > **Synchronisierung zurücksetzen** zurücksetzen.

> [!NOTE]
> Zusätzliche Geräteverbindungs- und Konfigurationsdaten (wie Gerätename, Marke und Modell) werden hochgeladen, um die Synchronisationsfunktionalität zu unterstützen.

## <a name="prerequisites"></a>Voraussetzungen

Die Synchronisierung von Microsoft Edge für Azure Active Directory (Azure AD)-Konten ist für jedes der folgenden Abonnements verfügbar:

- Azure AD Premium (P1 oder P2)
- M365 Business Premium
- Office365E1 und höher
- Azure Information Protection (AIP) (P1 oder P2)
- Alle EDU-Abonnements (Microsoft Apps für Studenten oder Dozenten, Exchange Online für Studenten oder Dozenten, O365 A1 oder höher, M365 A1 oder höher oder Azure Information Protection P1 oder P2 für Studenten oder Dozenten)

## <a name="sync-group-policies"></a>Synchronisieren von Gruppenrichtlinien

Administratoren können die folgenden Gruppenrichtlinien verwenden, um die Microsoft Edge-Synchronisierung zu konfigurieren und zu verwalten:

- [SyncDisabled](./microsoft-edge-policies.md#syncdisabled): Deaktiviert die Synchronisierung vollständig.
- [SavingBrowserHistoryDisabled](./microsoft-edge-policies.md#savingbrowserhistorydisabled): Deaktiviert das Speichern des Browserverlaufs und die Synchronisierung. Die Synchronisierung geöffneter Registerkarten wird durch diese Richtlinie ebenfalls deaktiviert.
- [AllowDeletingBrowserHistory](./microsoft-edge-policies.md#allowdeletingbrowserhistory): Wenn diese Richtlinie deaktiviert ist, wird auch die Verlaufsdatensynchronisierung deaktiviert.
- [SyncTypesListDisabled](./microsoft-edge-policies.md#synctypeslistdisabled): Konfigurieren Sie die Liste der Typen, die von der Synchronisierung ausgeschlossen werden.
- [RoamingProfileSupportEnabled](./microsoft-edge-policies.md#roamingprofilesupportenabled): Zulassen, dass Active Directory (AD)-Profile lokalen Speicher verwenden. Weitere Informationen finden Sie unter [Lokale Synchronisierung für Active Directory (AD)-Benutzer](./microsoft-edge-on-premises-sync.md).
- [ForceSync]( https://docs.microsoft.com/deployedge/microsoft-edge-policies#forcesync): Aktivieren Sie die Synchronisierung standardmäßig, und fordern Sie keine Benutzerzustimmung zur Synchronisierung an.  

## <a name="configure-microsoft-edge-sync"></a>Konfigurieren der Microsoft Edge-Synchronisierung

Konfigurationsoptionen für die Microsoft Edge-Synchronisierung stehen über den Azure Information Protection (AIP)-Dienst zur Verfügung. Wenn AIP für einen Mandanten aktiviert ist, können alle Benutzer Microsoft Edge-Daten unabhängig von der Lizenzierung synchronisieren. Anweisungen zum Aktivieren von AIP finden Sie [hier](/azure/information-protection/activate-office365).

Um die Synchronisierung auf eine bestimmte Benutzergruppe zu beschränken, können Sie die [AIP-Richtlinie zur Onboarding-Steuerung](/powershell/module/aipservice/set-aipserviceonboardingcontrolpolicy?preserve-view=true&view=azureipps) für diese Benutzer aktivieren. Wenn die Synchronisierung immer noch nicht verfügbar ist, nachdem Sie sich vergewissert haben, dass das Onboarding für alle erforderlichen Benutzer erfolgt ist, stellen Sie mithilfe des PowerShell-Cmdlets [Get-AIPServiceIPCv3](/powershell/module/aipservice/get-aipserviceipcv3?preserve-view=true&view=azureipps)  sicher, dass IPCv3Service aktiviert ist.

> [!CAUTION]
> Die Aktivierung von Azure Information Protection erlaubt auch anderen Anwendungen, wie z.B. Microsoft Word oder Microsoft Outlook, Inhalte mit AIP zu schützen. Darüber hinaus wird jede Onboarding-Kontrollrichtlinie, die zur Einschränkung der Microsoft Edge-Synchronisierung verwendet wird, auch andere Anwendungen daran hindern, Inhalte mithilfe von AIP zu schützen.

## <a name="microsoft-edge-and-enterprise-state-roaming-esr"></a>Microsoft Edge und Enterprise State Roaming (ESR)

Microsoft Edge ist eine plattformübergreifende Anwendung mit erweiterten Möglichkeiten zur Synchronisierung von Benutzerdaten auf allen Geräten und ist nicht mehr Teil von Azure AD Enterprise State Roaming. Microsoft Edge erfüllt jedoch die Datenschutzversprechen von ESR, wie z. B. die Möglichkeit, einen eigenen Schlüssel zu verwenden. Weitere Informationen finden sie unter [Microsoft Edge und Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).

## <a name="see-also"></a>Weitere Informationen

- [Microsoft Edge Enterprise-Synchronisierung](microsoft-edge-enterprise-sync.md)
- [Diagnostizieren und Beheben von Microsoft Edge-Synchronisierungsproblemen](microsoft-edge-troubleshoot-enterprise-sync.md)
- [Microsoft Edge und Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md)
- [Microsoft Edge Enterprise-Startseite](https://aka.ms/EdgeEnterprise)