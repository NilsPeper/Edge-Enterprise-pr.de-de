---
title: FAQ zur Microsoft Edge Enterprise-Synchronisierung
ms.author: collw
author: dan-wesley
manager: silvanam
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Häufig gestellte Fragen zur Microsoft Edge Enterprise-Synchronisierung.
ms.openlocfilehash: a13e1f02f6e871004d45f81159d5cf0a3397b6ad
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "11643141"
---
# <a name="microsoft-edge-enterprise-sync-faq"></a>FAQ zur Microsoft Edge Enterprise-Synchronisierung

In diesem Artikel finden Sie Antworten auf häufig gestellte Fragen zur Unternehmenssynchronisierung für Microsoft Edge, Version 77 oder höher.

## <a name="security-and-serverdata-compliance"></a>Sicherheit und Server-/Datenkonformität

### <a name="is-the-synced-data-encrypted"></a>Werden die synchronisierten Daten verschlüsselt?

Die Daten werden beim Transport mithilfe von TLS 1.2 oder höher verschlüsselt. Alle Datentypen werden im Ruhezustand im Microsoft-Dienst zusätzlich mit AES-128 verschlüsselt. Alle Datentypen mit Ausnahme derjenigen, die für die Synchronisierung von geöffneten Registerkarten und Verlaufsdaten verwendet werden, werden mit über die [Azure Information Protection](./microsoft-edge-policies.md#restrictsignintopattern)-Richtlinie verwalteten Schlüsseln zusätzlich verschlüsselt, bevor sie das Gerät des Benutzers verlassen.

### <a name="why-dont-open-tab-and-history-data-have-more-client-side-encryption"></a>Warum haben die Daten von offenen Registerkarten und Verlaufsdaten nicht weitere clientseitige Verschlüsselung?

Um die Ressourcenauslastung auf Endbenutzergeräten zu verringern, werden Verlaufsdaten serverseitig basierend auf den Roaming-Daten der offenen Registerkarten generiert. Dieser Vorgang wäre bei clientseitiger Verschlüsselung dieser Daten nicht möglich. Wenden Sie die Richtlinien [SavingBrowserHistoryDisabled](./microsoft-edge-policies.md#savingbrowserhistorydisabled) oder [SyncTypesListDisabled](./microsoft-edge-policies.md#synctypeslistdisabled) an, um die Synchronisierung von geöffneten Registerkarten und Verlaufsdaten zu deaktivieren.

### <a name="can-tenant-admins-bring-their-own-key"></a>Können Mandantenadministratoren ihren eigenen Schlüssel mitbringen?

Ja, über  [Azure Information Protection](https://azure.microsoft.com/services/information-protection/).

### <a name="where-is-microsoft-edge-sync-data-stored"></a>Wo werden Microsoft Edge-Synchronisierungsdaten für gespeichert?

Synchronisierte Daten für Azure AD-Konten werden auf sicheren Servern entsprechend der Mandanten-ID gespeichert. Beispielsweise werden die Daten eines in den USA registrierten Mandanten auf Servern gespeichert, die sich in dieser geografischen Region befinden, und verwenden die gleiche Speicherlösung wie Office-Anwendungen.

### <a name="does-the-data-ever-leave-microsofts-cloud-aside-from-syncing-to-microsoft-edge"></a>Verlassen die Daten jemals die Cloud von Microsoft, abgesehen von der Synchronisierung mit Microsoft Edge?

Nein.

### <a name="what-terms-of-service-does-enterprise-sync-fall-under"></a>Unter welche Nutzungsbedingungen fällt die Unternehmenssynchronisierung?

Die Nutzungsbedingungen für die Microsoft Edge-Synchronisierung gehören zur Microsoft-Softwarelizenz, die in Microsoft Edge unter  *edge://terms* einsehbar ist. Ihr Abonnement und die Nutzungsbedingungen von Azure AD fallen letztlich unter die [Onlinedienst-Vertragsbedingungen](https://www.microsoft.com/licensing/product-licensing/products) von Microsoft Corporation.

### <a name="does-microsoft-edge-support-government-community-cloud-gcc-high-compliance"></a>Unterstützt Microsoft Edge Government Community Cloud (GCC) High-Compliance?

Derzeit nicht. Für Kunden in der GCC High-Cloud ist die Microsoft Edge-Synchronisierung deaktiviert.

## <a name="applying-sync"></a>Synchronisierung wird angewendet

### <a name="why-isnt-microsoft-edge-sync-supported-in-all-m365-subscriptions"></a>Warum wird die Microsoft Edge-Synchronisierung nicht in allen M365-Abonnements unterstützt?

Die Unternehmenssynchronisierung ist von [Azure Information Protection](https://azure.microsoft.com/services/information-protection/) abhängig, das nicht in allen M365-Abonnements verfügbar ist.

### <a name="is-microsoft-edge-sync-based-on-enterprise-state-roaming"></a>Basiert die Microsoft Edge-Synchronisierung auf Enterprise State Roaming (ESR)?

Nein. ESR kann verwendet werden, um die Synchronisierung zu aktivieren, aber Microsoft Edge-Synchronisierung ist nicht Teil von ESR. Weitere Informationen finden sie unter [Microsoft Edge-Synchronisierung](/DeployEdge/microsoft-edge-enterprise-sync) sowie [Microsoft Edge und Enterprise State Roaming](/DeployEdge/microsoft-edge-enterprise-state-roaming).

### <a name="will-microsoft-edge-ever-support-syncing-between-microsoft-edge-and-ie"></a>Wird Microsoft Edge jemals die Synchronisierung zwischen Microsoft Edge und IE unterstützen?

Es gibt keine Pläne, diese Synchronisierung zu unterstützen. Wenn Sie in Ihrer Umgebung noch IE zur Unterstützung von Legacyanwendungen benötigen, sollten Sie unseren [neuen IE-Modus](./edge-ie-mode.md) in Betracht ziehen.

### <a name="will-microsoft-edge-sync-with-microsoft-edge-legacy"></a>Wird Microsoft Edge mit der Vorgängerversion von Microsoft Edge synchronisiert?

Nein. Wir sind der Meinung, dass die Verbindung dieser beiden Ökosysteme zu Kompromissen bezüglich der Zuverlässigkeit der Synchronisation in Microsoft Edge führen würde. Wir stellen sicher, dass vorhandene Daten zu Microsoft Edge migriert werden. Benutzer werden auch in der Lage sein, Daten aus dem Browser ihrer Wahl zu importieren. Dies bedeutet, dass Microsoft Edge keine Möglichkeit zur Synchronisierung mit IE haben wird.

## <a name="managing-sync"></a>Verwalten der Synchronisierung

### <a name="is-it-possible-to-stop-my-users-from-syncing-with-a-personal-tenant"></a>Kann ich verhindern, dass meine Benutzer mit einem persönlichen Mandanten synchronisiert werden?

Nicht direkt. Sie können jedoch mithilfe der Richtlinie [RestrictSigninToPattern](./microsoft-edge-policies.md#restrictsignintopattern) festlegen, welche Profile sich bei Microsoft Edge anmelden können.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft Edge Enterprise-Synchronisierung](microsoft-edge-enterprise-sync.md)
- [Microsoft Edge und Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md)
- [Microsoft Edge Enterprise-Startseite](https://aka.ms/EdgeEnterprise)