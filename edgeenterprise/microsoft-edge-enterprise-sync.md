---
title: Konfigurieren und Beheben von Problemen mit der Microsoft Edge-Synchronisierung
ms.author: scottbo
author: dan-wesley
manager: silvanam
ms.date: 01/22/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Konfigurieren und Beheben von Problemen mit der Microsoft Edge-Synchronisierung
ms.openlocfilehash: 36912d2fd1c33a227ce1d4b7c912f6ef1dfdcc00
ms.sourcegitcommit: 8a88fd38bdb5e132e89bf17dd2b5fb72f5d1b4b9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/22/2021
ms.locfileid: "11297455"
---
# Konfigurieren und Beheben von Problemen mit der Microsoft Edge-Synchronisierung

In diesem Artikel wird erläutert, wie Sie Microsoft Edge konfigurieren und verwenden, um Ihre Favoriten, Kennwörter und andere Browserdaten über alle Ihre angemeldeten Geräte hinweg zu synchronisieren. Dieser Artikel enthält auch Schritte zur Problembehandlung für die am häufigsten auftretenden Synchronisierungsprobleme. Es enthält außerdem die empfohlenen Tools zum Sammeln der Protokolle, die für die Problembehandlung erforderlich sind.

> [!NOTE]
> Gilt für Microsoft Edge Version 77 oder höher, sofern nicht anderes angegeben.

## Übersicht

Dank der Microsoft Edge-Synchronisierung können Benutzer auf ihre Browserdaten über alle angemeldeten Geräte hinweg zugreifen. Zu den von der Synchronisierung unterstützten Daten gehören:

- Favoriten
- Kennwörter
- Adressen und mehr (Formulareinträge)
- Sammlungen
- Einstellungen
- Erweiterung
- Geöffnete Registerkarten (verfügbar in Microsoft Edge, Version 88)
- Verlauf (verfügbar in Microsoft Edge, Version 88)

Die Synchronisierungsfunktion wird nach Zustimmung des Benutzers aktiviert, und Benutzer können die Synchronisierung für die beiden oben aufgeführten Datentypen aktivieren oder deaktivieren.

> [!NOTE]
> Zusätzliche Geräteverbindungs- und Konfigurationsdaten (wie Gerätename, Marke und Modell) werden hochgeladen, um die Synchronisationsfunktionalität zu unterstützen.

## Voraussetzungen

Die Synchronisierung von Microsoft Edge für Azure Active Directory (Azure AD)-Konten ist für jedes der folgenden Abonnements verfügbar:

- Azure AD Premium (P1 oder P2)
- M365 Business Premium
- Office365E1 und höher
- Azure Information Protection (AIP) (P1 oder P2)
- Alle EDU-Abonnements (Microsoft Apps für Studenten oder Dozenten, Exchange Online für Studenten oder Dozenten, O365 A1 oder höher, M365 A1 oder höher oder Azure Information Protection P1 oder P2 für Studenten oder Dozenten)

## Synchronisierungs-Gruppenrichtlinien

Sie können die folgenden Gruppenrichtlinien verwenden, um die Microsoft Edge-Synchronisierung zu konfigurieren und zu verwalten:

- [SyncDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled): Deaktiviert die Synchronisierung vollständig.
- [SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled): Deaktiviert das Speichern des Browserverlaufs und die Synchronisierung. Die Synchronisierung geöffneter Registerkarten wird durch diese Richtlinie ebenfalls deaktiviert.
- [AllowDeletingBrowserHistory](https://docs.microsoft.com/deployedge/microsoft-edge-policies#allowdeletingbrowserhistory): Wenn diese Richtlinie deaktiviert ist, wird auch die Verlaufsdatensynchronisierung deaktiviert.
- [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled): Konfigurieren Sie die Liste der Typen, die von der Synchronisierung ausgeschlossen werden.
- [RoamingProfileSupportEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilesupportenabled): Zulassen, dass Active Directory (AD)-Profile lokalen Speicher verwenden. Weitere Informationen finden Sie unter [Lokale Synchronisierung für Active Directory (AD)-Benutzer](https://docs.microsoft.com/DeployEdge/microsoft-edge-on-premises-sync).
- [ForceSync]( https://docs.microsoft.com/deployedge/microsoft-edge-policies#forcesync): Aktivieren Sie die Synchronisierung standardmäßig, und fordern Sie keine Benutzerzustimmung zur Synchronisierung an.  

## Konfigurieren der Microsoft Edge-Synchronisierung

Konfigurationsoptionen für die Microsoft Edge-Synchronisierung stehen über den Azure Information Protection (AIP)-Dienst zur Verfügung. Wenn AIP für einen Mandanten aktiviert ist, können alle Benutzer Microsoft Edge-Daten unabhängig von der Lizenzierung synchronisieren. Anweisungen zum Aktivieren von AIP finden Sie [hier](https://docs.microsoft.com/azure/information-protection/activate-office365).

Um die Synchronisierung auf eine bestimmte Benutzergruppe zu beschränken, können Sie die [AIP-Richtlinie zur Onboarding-Steuerung](https://docs.microsoft.com/powershell/module/aipservice/set-aipserviceonboardingcontrolpolicy?view=azureipps&preserve-view=true) für diese Benutzer aktivieren. Wenn die Synchronisierung immer noch nicht verfügbar ist, nachdem Sie sich vergewissert haben, dass das Onboarding für alle erforderlichen Benutzer erfolgt ist, stellen Sie mithilfe des PowerShell-Cmdlets [Get-AIPServiceIPCv3](https://docs.microsoft.com/powershell/module/aipservice/get-aipserviceipcv3?view=azureipps&preserve-view=true)  sicher, dass IPCv3Service aktiviert ist.

> [!CAUTION]
> Die Aktivierung von Azure Information Protection erlaubt auch anderen Anwendungen, wie z.B. Microsoft Word oder Microsoft Outlook, Inhalte mit AIP zu schützen. Darüber hinaus wird jede Onboarding-Kontrollrichtlinie, die zur Einschränkung der Microsoft Edge-Synchronisierung verwendet wird, auch andere Anwendungen daran hindern, Inhalte mithilfe von AIP zu schützen.

## Microsoft Edge und Enterprise State Roaming (ESR)

Microsoft Edge ist eine plattformübergreifende Anwendung mit erweiterten Möglichkeiten zur Synchronisierung von Benutzerdaten auf allen Geräten und ist nicht mehr Teil von Azure AD Enterprise State Roaming. Microsoft Edge erfüllt jedoch die Datenschutzversprechen von ESR, wie z. B. die Möglichkeit, einen eigenen Schlüssel zu verwenden. Weitere Informationen finden sie unter [Microsoft Edge und Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).

## Beheben von Synchronisierungsproblemen

Dieser Abschnitt enthält Schritte zur Problembehandlung der am häufigsten auftretenden Synchronisierungsprobleme. Es enthält außerdem die empfohlenen Tools zum Sammeln der Protokolle, die für die Problembehandlung erforderlich sind.

### Identitätsprobleme versus Synchronisierungsprobleme

Ein beliebter Anwendungsfall für die Aufrechterhaltung der Benutzeridentität im Browser ist die Unterstützung der Synchronisierung. Aus diesem Grund werden Identitätsprobleme häufig mit Synchronisierungsproblemen verwechselt. Verstehen Sie den Unterschied zwischen einem Identitäts- und einem Synchronisierungsproblem, bevor Sie mit der Problembehandlung für die Synchronisierung beginnen.

Bevor Sie ein Problem als Synchronisierungsproblem behandeln, überprüfen Sie, ob der Benutzer mit einem gültigen Konto beim Browser angemeldet ist.

Der nächste Screenshot zeigt ein Beispiel für einen Identitätsfehler. Der Fehler ist "**Last Token Error, EDGE_AUTH_ERROR: 3, 54, 3ea**" und wird in *edge://sync-internals* unter **Anmeldeinformationen** angezeigt:

:::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/sync-identity-issue.png" alt-text="Last Token Error EDGE_AUTH_ERROR: 3,54, 3ea":::

### Häufige Synchronisierungsprobleme

#### Problem: Zugriff auf M365- oder Azure Information Protection-Abonnement nicht möglich

Haben Sie ein früheres M365- oder Azure Information Protection (AIP)-Abonnement, das abgelaufen ist und dann durch ein neues Abonnement ersetzt wurde? Wenn ja, hat sich die Mandanten-ID geändert, und die Dienstdaten müssen zurückgesetzt werden. Weitere Informationen finden Sie in den Anweisungen zum Zurücksetzen von Daten in der Problembeschreibung **Kryptograph-Fehler aufgetreten**.

#### Problem: „Die Synchronisierung ist für dieses Konto nicht verfügbar.“

Wenn dieser Fehler für ein Azure Active Directory-Konto auftritt oder wenn DISABLED_BY_ADMIN in *edge://sync-internals*angezeigt wird, führen Sie die Schritte im nächsten Verfahren nacheinander aus, bis das Problem behoben ist.

> [!NOTE]
> Da die Ursache dieses Fehlers in der Regel eine Konfigurationsänderung in einem Azure Active Directory-Mandanten erfordert, können diese Schritte zur Problembehandlung nur von einem Mandantenadministrator und nicht von Endbenutzern ausgeführt werden.

1. Stellen Sie sicher, dass der Unternehmensmandant über ein unterstütztes M365-Abonnement verfügt. Die aktuelle Liste der verfügbaren Abonnementtypen werden [hier bereitgestellt](https://docs.microsoft.com/azure/information-protection/activate-office365). Wenn der Mandant kein unterstütztes Abonnement hat, kann er Azure Information Protection entweder separat erwerben oder auf eines der unterstützten Abonnements aktualisieren.
2. Wenn ein unterstütztes Abonnement verfügbar ist, stellen Sie sicher, dass für den Mandanten Azure Information Protection (AIP) verfügbar ist. Die Anweisungen zur Überprüfung des AIP-Status und, falls erforderlich, zum Aktivieren von AIP finden Sie [hier](https://docs.microsoft.com/azure/information-protection/activate-office365).
3. Wenn in Schritt 2 gezeigt wird, dass AIP aktiv ist, die Synchronisierung aber immer noch nicht funktioniert, dann aktivieren Sie Enterprise State Roaming (ESR). Die Anweisungen zum Aktivieren von ESR finden Sie [hier](https://docs.microsoft.com/azure/active-directory/devices/enterprise-state-roaming-enable). Beachten Sie, dass ESR nicht aktiviert bleiben muss. Sie können ESR deaktivieren, wenn dieser Schritt das Problem behebt.
4. Vergewissern Sie sich, dass Azure Information Protection nicht über eine Onboarding-Richtlinie eingegrenzt ist. Sie können das PowerShell-Applet [Get-AadrmOnboardingControlPolicy](https://docs.microsoft.com/powershell/module/aadrm/get-aadrmonboardingcontrolpolicy?view=azureipps)  verwenden, um zu sehen, ob eine Bereichsdefinition aktiviert ist. Die nächsten beiden Beispiele zeigen eine Konfiguration ohne Bereichseingrenzung und eine Konfiguration, die auf eine bestimmte Sicherheitsgruppe eingegrenzt ist.

   ```powershell
    PS C:\Work\scripts\PowerShell> Get-AadrmOnboardingControlPolicy
 
    UseRmsUserLicense SecurityGroupObjectId                Scope
    ----------------- ---------------------                -----
                False 
   ```

   ```powershell

    PS C:\Work\scripts\PowerShell> Get-AadrmOnboardingControlPolicy
 
    UseRmsUserLicense SecurityGroupObjectId                Scope
    ----------------- ---------------------                -----
                False f1488a05-8196-40a6-9483-524948b90282   All
   ```


   Wenn eine Bereichsdefinition aktiviert ist, sollte der betroffene Benutzer entweder der Sicherheitsgruppe für den Bereich hinzugefügt oder der Bereich entfernt werden. Im folgenden Beispiel hat Onboarding den AIP für die angegebene Sicherheitsgruppe eingegrenzt, und die Bereichsdefinition sollte mit dem PowerShell-Applet [Set-AadrmOnboardingControlPolicy](https://docs.microsoft.com/powershell/module/aadrm/set-aadrmonboardingcontrolpolicy?view=azureipps) entfernt werden.

5. Vergewissern Sie sich, dass „IPCv3Service“ im Mandanten aktiviert ist. Das PowerShell-Applet [Get-AadrmConfiguration](https://docs.microsoft.com/powershell/module/aadrm/get-aadrmconfiguration?view=azureipps)  zeigt den Status des Diensts an.

   :::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/sync-scoped-cfg-example.png" alt-text="Überprüfen Sie, ob „IPCv3Service“ aktiviert ist.":::

6. Wenn das Problem nicht behoben ist, wenden Sie sich an den [Microsoft Edge-Support](https://www.microsoftedgeinsider.com/support).

#### Problem: Bei „Einrichten der Synchronisierung...“ hängen geblieben oder bei „Es konnte keine Verbindung zum Synchronisierungsserver hergestellt werden. Wiederholen...“

1. Versuchen Sie sich abzumelden und dann anzumelden.
2. Gehen Sie zu *edge://sync-internals*. Wenn im Abschnitt „**Typeninformation**“ der folgende Fehler vorhanden ist, dann fahren Sie mit der folgenden Problembeschreibung weiter: **Kryptograph-Fehler aufgetreten**.

   `"Error:GenerateCryptoErrorsForTypes@../../components/sync/driver/data_type_manager_impl.cc:42, cryptographer error was encountered"`

3. Versuchen Sie, den Serverendpunkt zu pingen. Der Serverendpunkt für einen Client ist verfügbar in *edge://sync-internals*. Der nächste Screenshot zeigt Endpunktinformationen unter **Umgebungsinformationen**.

   :::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/sync-endpoint-info.png" alt-text="Endpunktinformationen":::

4. Wenn der Serverendpunkt leer ist oder der Server nicht gepingt werden kann und in der Umgebung eine Firewall vorhanden ist, dann stellen Sie sicher, dass die erforderlichen Dienstendpunkte für den Clientcomputer verfügbar sind.

   - Endpunkte des Microsoft Edge-Synchronisierungsdiensts:
     - [https://edge-enterprise.activity.windows.com](https://edge-enterprise.activity.windows.com)
     - [https://edge.activity.windows.com](https://edge.activity.windows.com)
    - Azure Information Protection-Endpunkte:
      - [https://api.aadrm.com](https://api.aadrm.com) (für die meisten Mandanten)
      - [https://api.aadrm.de](https://api.aadrm.de) (für Mandanten in Deutschland)
      - [https://api.aadrm.cn](https://api.aadrm.cn) (für Mandanten in China)
   - [Endpunkte des Windows-Benachrichtigungsdiensts](https://docs.microsoft.com/windows/uwp/design/shell/tiles-and-notifications/firewall-allowlist-config).

5. Wenn das Problem weiterhin besteht, wenden Sie sich an den [Microsoft Edge-Support](https://www.microsoftedgeinsider.com/support).

### Problem: Kryptograph-Fehler aufgetreten

Dieser Fehler wird unter **Typeninformation** in *edge://sync-internals* angezeigt und kann bedeuten, dass die dienstseitigen Daten des Benutzers zurückgesetzt werden müssen. Das folgende Beispiel zeigt eine Kryptografiefehlermeldung:
<br>"Fehler:GenerateCryptoErrorsForTypes@../../components/sync/driver/data_type_manager_impl.cc:42, Kryptografiefehler wurde erkannt".

1. Starten Sie Microsoft Edge neu, navigieren Sie zu *edge://sync-internals* und überprüfen Sie den Abschnitt „**AAD-Kontoschlüsselstatus**“.
   - "Erfolg“ in „Letztes MIP-Ergebnis“: Der Kryptograph-Fehler bedeutet, dass Serverdaten möglicherweise mit einem verlorenen Schlüssel verschlüsselt sind. Eine Datenzurücksetzung ist erforderlich, um die Synchronisierung fortsetzen zu können.
   - „Keine Berechtigungen“ in „Letztes MIP-Ergebnis“: Dies wird möglicherweise durch eine Azure AD-Änderung oder Mandanten-Abonnementänderung verursacht. Eine Datenzurücksetzung ist erforderlich, um die Synchronisierung fortsetzen zu können.
   - Andere Fehler können auf Probleme mit der Serverkonfiguration hinweisen.
2. Wenn eine Datenzurücksetzung notwendig ist, finden Sie weitere Informationen unter [Zurücksetzen von Microsoft Edge-Daten in der Cloud](edge-learnmore-reset-data-in-cloud.md).

#### Problem: „Die Synchronisierung wurde von Ihrem Administrator deaktiviert.“

Stellen Sie sicher, dass die [Richtlinie „SyncDisabled“](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled) nicht festgelegt ist.

## Häufig gestellte Fragen

### SICHERHEIT und von SERVER-/DATENKONFORMITÄT

#### Werden die synchronisierten Daten verschlüsselt?

Die Daten werden beim Transport mithilfe von TLS 1.2 oder höher verschlüsselt. Alle Datentypen werden im Ruhezustand im Microsoft-Dienst zusätzlich mit AES-128 verschlüsselt. Alle Datentypen mit Ausnahme derjenigen, die für die Synchronisierung von geöffneten Registerkarten und Verlaufsdaten verwendet werden, werden mit über die [Azure Information Protection](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern)-Richtlinie verwalteten Schlüsseln zusätzlich verschlüsselt, bevor sie das Gerät des Benutzers verlassen.

#### Warum haben die Daten von offenen Registerkarten und Verlaufsdaten nicht weitere clientseitige Verschlüsselung?

Um die Ressourcenauslastung auf Endbenutzergeräten zu verringern, werden Verlaufsdaten serverseitig basierend auf den Roaming-Daten der offenen Registerkarten generiert. Dieser Vorgang wäre bei clientseitiger Verschlüsselung dieser Daten nicht möglich. Wenden Sie die Richtlinien [SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled) oder [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled) an, um die Synchronisierung von geöffneten Registerkarten und Verlaufsdaten zu deaktivieren.

#### Können Mandantenadministratoren ihren eigenen Schlüssel mitbringen?

Ja, über  [Azure Information Protection](https://azure.microsoft.com/services/information-protection/).

#### Wo werden Microsoft Edge-Synchronisierungsdaten für gespeichert?

Synchronisierte Daten für Azure AD-Konten werden auf sicheren Servern entsprechend der Mandanten-ID gespeichert. Beispielsweise werden die Daten eines in den USA registrierten Mandanten auf Servern gespeichert, die sich in dieser geografischen Region befinden, und verwenden die gleiche Speicherlösung wie Office-Anwendungen.

#### Verlassen die Daten jemals die Cloud von Microsoft, abgesehen von der Synchronisierung mit Microsoft Edge?

Nein.

#### Unter welche Nutzungsbedingungen fällt die Unternehmenssynchronisierung?

Die Nutzungsbedingungen für die Microsoft Edge-Synchronisierung gehören zur Microsoft-Softwarelizenz, die in Microsoft Edge unter  *edge://terms* einsehbar ist. Ihr Abonnement und die Nutzungsbedingungen von Azure AD fallen letztlich unter die [Onlinedienst-Vertragsbedingungen](https://www.microsoft.com/licensing/product-licensing/products) von Microsoft Corporation.

#### Unterstützt Microsoft Edge Government Community Cloud (GCC) High-Compliance?

Derzeit nicht. Für Kunden in der GCC High-Cloud ist die Microsoft Edge-Synchronisierung deaktiviert.

### ANWENDEN DER SYNCHRONISIERUNG

#### Warum wird die Microsoft Edge-Synchronisierung nicht in allen M365-Abonnements unterstützt?

Die Unternehmenssynchronisierung ist von [Azure Information Protection](https://azure.microsoft.com/services/information-protection/) abhängig, das nicht in allen M365-Abonnements verfügbar ist.

#### Basiert die Microsoft Edge-Synchronisierung auf Enterprise State Roaming (ESR)?

Nein. ESR kann verwendet werden, um die Synchronisierung zu aktivieren, aber Microsoft Edge-Synchronisierung ist nicht Teil von ESR. Weitere Informationen finden sie unter [Microsoft Edge-Synchronisierung](https://review.docs.microsoft.com/DeployEdge/microsoft-edge-enterprise-sync) sowie [Microsoft Edge und Enterprise State Roaming](https://review.docs.microsoft.com/DeployEdge/microsoft-edge-enterprise-state-roaming).

#### Wird Microsoft Edge jemals die Synchronisierung zwischen Microsoft Edge und IE unterstützen?

Es gibt keine Pläne, diese Synchronisierung zu unterstützen. Wenn Sie in Ihrer Umgebung noch IE zur Unterstützung von Legacyanwendungen benötigen, sollten Sie unseren [neuen IE-Modus](https://docs.microsoft.com/deployedge/edge-ie-mode) in Betracht ziehen.

#### Wird Microsoft Edge mit der Vorgängerversion von Microsoft Edge synchronisiert?

Nein. Wir sind der Meinung, dass die Verbindung dieser beiden Ökosysteme zu Kompromissen bezüglich der Zuverlässigkeit der Synchronisation in Microsoft Edge führen würde. Wir stellen sicher, dass vorhandene Daten zu Microsoft Edge migriert werden. Benutzer werden auch in der Lage sein, Daten aus dem Browser ihrer Wahl zu importieren. Dies bedeutet, dass Microsoft Edge keine Möglichkeit zur Synchronisierung mit IE haben wird.

### VERWALTEN DER SYNCHRONISIERUNG

#### Kann ich verhindern, dass meine Benutzer mit einem persönlichen Mandanten synchronisiert werden?

Nicht direkt. Sie können jedoch mithilfe der Richtlinie [RestrictSigninToPattern](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern) festlegen, welche Profile sich bei Microsoft Edge anmelden können.

## Weitere Informationen

- [Microsoft Edge Enterprise-Synchronisierung](microsoft-edge-enterprise-sync.md)
- [Microsoft Edge und Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md)
- [Microsoft Edge Enterprise-Startseite](https://aka.ms/EdgeEnterprise)
