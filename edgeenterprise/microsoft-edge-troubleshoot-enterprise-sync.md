---
title: Diagnostizieren und Beheben von Microsoft Edge-Synchronisierungsproblemen
ms.author: collw
author: AndreaLBarr
manager: silvanam
ms.date: 07/27/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Anleitungen und Tools für Microsoft Edge-Administratoren zur Problembehandlung und Korrektur häufiger Synchronisierungsprobleme im Unternehmen
ms.openlocfilehash: c46fc716424faf361ea0a3bfab68737b64725473
ms.sourcegitcommit: 8968f3107291935ed9adc84bba348d5f187eadae
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/12/2021
ms.locfileid: "11979506"
---
# <a name="diagnose-and-fix-microsoft-edge-sync-issues"></a>Diagnostizieren und Beheben von Microsoft Edge-Synchronisierungsproblemen

Dieser Artikel enthält eine Anleitung zur Problembehandlung der am häufigsten auftretenden Synchronisierungsprobleme in einer Azure Active Directory (Azure AD)-Umgebung. Er enthält außerdem die empfohlenen Tools zum Sammeln der Protokolle, die für die Problembehandlung eines Synchronisierungsproblems erforderlich sind.

Wenn bei einem Benutzer ein Problem mit dem Synchronisieren von Browserdaten auf seinen Geräten auftritt, kann er die [Synchronisierung zurücksetzen](edge-learnmore-reset-data-in-cloud.md). Wenn dies das Problem nicht behebt, können Administratoren oder Supportmitarbeiter die folgenden Anleitungen verwenden, um ein Synchronisierungsproblem zu beheben.

> [!NOTE]
> Gilt für Microsoft Edge Version 77 oder höher, sofern nicht anderes angegeben.

## <a name="identity-issues-versus-sync-issues"></a>Identitätsprobleme versus Synchronisierungsprobleme

Bevor Sie beginnen, ist es wichtig, den Unterschied zwischen Identitätsproblemen und Synchronisierungsproblemen zu verstehen. Ein beliebter Anwendungsfall für die Aufrechterhaltung der Benutzeridentität im Browser ist die Unterstützung der Synchronisierung. Aus diesem Grund werden Identitätsprobleme häufig mit Synchronisierungsproblemen verwechselt. Verstehen Sie den Unterschied zwischen einem Identitäts- und einem Synchronisierungsproblem, bevor Sie mit der Problembehandlung für die Synchronisierung beginnen.

Bevor Sie ein Problem als Synchronisierungsproblem behandeln, überprüfen Sie, ob der Benutzer mit einem gültigen Konto beim Browser angemeldet ist.

Der nächste Screenshot zeigt ein Beispiel für einen Identitätsfehler. Der Fehler ist "**Last Token Error, EDGE_AUTH_ERROR: 3, 54, 3ea**" und wird in *edge://sync-internals* unter **Anmeldeinformationen** angezeigt:

:::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/sync-identity-issue.png" alt-text="Last Token Error EDGE_AUTH_ERROR: 3,54, 3ea":::

## <a name="common-sync-issues"></a>Häufige Synchronisierungsprobleme

### <a name="issue-cant-access-m365-or-azure-information-protection-subscription"></a>Problem: Zugriff auf M365- oder Azure Information Protection-Abonnement nicht möglich

Haben Sie ein früheres M365- oder Azure Information Protection (AIP)-Abonnement, das abgelaufen ist und dann durch ein neues Abonnement ersetzt wurde? Wenn ja, hat sich die Mandanten-ID geändert, und die Dienstdaten müssen zurückgesetzt werden. Weitere Informationen finden Sie in den Anweisungen zum Zurücksetzen von Daten in der Problembeschreibung **Kryptograph-Fehler aufgetreten**.

### <a name="issue-sync-is-not-available-for-this-account"></a>Problem: „Die Synchronisierung ist für dieses Konto nicht verfügbar.“

Wenn dieser Fehler für ein Azure Active Directory-Konto auftritt oder wenn DISABLED_BY_ADMIN in *edge://sync-internals*angezeigt wird, führen Sie die Schritte im nächsten Verfahren nacheinander aus, bis das Problem behoben ist.

> [!NOTE]
> Da die Ursache dieses Fehlers in der Regel eine Konfigurationsänderung in einem Azure Active Directory-Mandanten erfordert, können diese Schritte zur Problembehandlung nur von einem Mandantenadministrator und nicht von Endbenutzern ausgeführt werden.

1. Stellen Sie sicher, dass der Unternehmensmandant über ein unterstütztes M365-Abonnement verfügt. Die aktuelle Liste der verfügbaren Abonnementtypen werden [hier bereitgestellt](/azure/information-protection/activate-office365). Wenn der Mandant kein unterstütztes Abonnement hat, kann er Azure Information Protection entweder separat erwerben oder auf eines der unterstützten Abonnements aktualisieren.
2. Wenn ein unterstütztes Abonnement verfügbar ist, stellen Sie sicher, dass für den Mandanten Azure Information Protection (AIP) verfügbar ist. Die Anweisungen zur Überprüfung des AIP-Status und, falls erforderlich, zum Aktivieren von AIP finden Sie [hier](/azure/information-protection/activate-office365).
3. Wenn in Schritt 2 gezeigt wird, dass AIP aktiv ist, die Synchronisierung aber immer noch nicht funktioniert, dann aktivieren Sie Enterprise State Roaming (ESR). Die Anweisungen zum Aktivieren von ESR finden Sie [hier](/azure/active-directory/devices/enterprise-state-roaming-enable). Beachten Sie, dass ESR nicht aktiviert bleiben muss. Sie können ESR deaktivieren, wenn dieser Schritt das Problem behebt.
4. Vergewissern Sie sich, dass Azure Information Protection nicht über eine Onboarding-Richtlinie eingegrenzt ist. Sie können das [PowerShell-Cmdlet "Get-AIPServiceOnboardingControlPolicy"](/powershell/module/aipservice/get-aipserviceonboardingcontrolpolicy?view=azureipps) verwenden, um festzustellen, ob die Bereichsdefinition aktiviert ist. Stellen Sie sicher, dass der aIPService PowerShell-Monitor installiert ist. Sie können es hier abrufen: [Installieren Sie das AIPService PowerShell-Modul für Azure Information Protection.](/azure/information-protection/install-powershell) Die nächsten beiden Beispiele zeigen eine Konfiguration ohne Bereichseingrenzung und eine Konfiguration, die auf eine bestimmte Sicherheitsgruppe eingegrenzt ist.

   ```powershell
    PS C:\Work\scripts\PowerShell> Get-AIPServiceOnboardingControlPolicy
 
    UseRmsUserLicense SecurityGroupObjectId                Scope
    ----------------- ---------------------                -----
                False 
   ```

   ```powershell

    PS C:\Work\scripts\PowerShell> Get-AIPServiceOnboardingControlPolicy
 
    UseRmsUserLicense SecurityGroupObjectId                Scope
    ----------------- ---------------------                -----
                False f1488a05-8196-40a6-9483-524948b90282   All
   ```

   Wenn eine Bereichsdefinition aktiviert ist, sollte der betroffene Benutzer entweder der Sicherheitsgruppe für den Bereich hinzugefügt oder der Bereich entfernt werden. Im folgenden Beispiel hat das Onboarding AIP auf die angegebene Sicherheitsgruppe beschränkt, und die Bereichsdefinition sollte mit dem [PowerShell-Applet "Set-AIPServiceOnboardingControlPolicy"](/powershell/module/aipservice/set-aipserviceonboardingcontrolpolicy?view=azureipps) entfernt werden.

5. Vergewissern Sie sich, dass „IPCv3Service“ im Mandanten aktiviert ist. Das [PowerShell-Cmdlet "Get-AIPServiceConfiguration" ](/powershell/module/aipservice/get-aipserviceconfiguration?view=azureipps)  zeigt den Status des Diensts an.

   :::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/sync-scoped-cfg-example.png" alt-text="Überprüfen Sie, ob „IPCv3Service“ aktiviert ist.":::

6. Wenn das Problem nicht behoben ist, wenden Sie sich an den [Microsoft Edge-Support](https://www.microsoftedgeinsider.com/support).

### <a name="issue-stuck-at-setting-up-sync-or-couldnt-connect-to-the-sync-server-retrying"></a>Problem: Bei „Einrichten der Synchronisierung...“ hängen geblieben oder bei „Es konnte keine Verbindung zum Synchronisierungsserver hergestellt werden. Wiederholen...“

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
   - [Endpunkte des Windows-Benachrichtigungsdiensts](/windows/uwp/design/shell/tiles-and-notifications/firewall-allowlist-config).

5. Wenn das Problem weiterhin besteht, wenden Sie sich an den [Microsoft Edge-Support](https://www.microsoftedgeinsider.com/support).

### <a name="issue-cryptographer-error-encountered"></a>Problem: Kryptograph-Fehler aufgetreten

Dieser Fehler wird unter **Typeninformation** in *edge://sync-internals* angezeigt und kann bedeuten, dass die dienstseitigen Daten des Benutzers zurückgesetzt werden müssen. Das folgende Beispiel zeigt eine Kryptografiefehlermeldung:
<br>"Fehler: GenerateCryptoErrorsForTypes@../../components/sync/driver/data_type_manager_impl.cc:42, Kryptografiefehler wurde erkannt".

1. Starten Sie Microsoft Edge neu, navigieren Sie zu *edge://sync-internals* und überprüfen Sie den Abschnitt „**AAD-Kontoschlüsselstatus**“.
   - "Erfolg“ in „Letztes MIP-Ergebnis“: Der Kryptograph-Fehler bedeutet, dass Serverdaten möglicherweise mit einem verlorenen Schlüssel verschlüsselt sind. Eine Datenzurücksetzung ist erforderlich, um die Synchronisierung fortsetzen zu können.
   - „Keine Berechtigungen“ in „Letztes MIP-Ergebnis“: Dies wird möglicherweise durch eine Azure AD-Änderung oder Mandanten-Abonnementänderung verursacht. Eine Datenzurücksetzung ist erforderlich, um die Synchronisierung fortsetzen zu können.
   - Andere Fehler können auf Probleme mit der Serverkonfiguration hinweisen.
2. Wenn eine Datenzurücksetzung notwendig ist, finden Sie weitere Informationen unter [Zurücksetzen von Microsoft Edge-Daten in der Cloud](edge-learnmore-reset-data-in-cloud.md).

### <a name="issue-sync-has-been-turned-off-by-your-administrator"></a>Problem: „Die Synchronisierung wurde von Ihrem Administrator deaktiviert.“

Stellen Sie sicher, dass die [Richtlinie „SyncDisabled“](./microsoft-edge-policies.md#syncdisabled) nicht festgelegt ist.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft Edge Enterprise-Synchronisierung](microsoft-edge-enterprise-sync.md)
- [Microsoft Edge und Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md)
- [Microsoft Edge Enterprise-Startseite](https://aka.ms/EdgeEnterprise)