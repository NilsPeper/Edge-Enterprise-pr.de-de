---
title: Versionshinweise von Microsoft Edge für Stable Channel
ms.author: aguta
author: AndreaLBarr
manager: srugh
ms.date: 07/09/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Versionshinweise von Microsoft Edge für Stable Channel
ms.openlocfilehash: f82fdbdddb45951fd9e1eca44f90270bc06c32d1
ms.sourcegitcommit: 2a00571483e1d169b2b3b59f4fce43262f460a9a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/12/2021
ms.locfileid: "11643770"
---
# <a name="release-notes-for-microsoft-edge-stable-channel"></a>Versionshinweise für Microsoft Edge Stable Channel

Diese Versionshinweise enthalten Informationen zu neuen Funktionen und nicht sicherheitsrelevanten Updates, die im Microsoft Edge Stable Channel enthalten sind.

- Alle Sicherheitsupdates werden [hier](microsoft-edge-relnotes-security.md) aufgelistet.
- Archivierte Versionshinweise für Microsoft Edge Stable Channel finden Sie [hier.](microsoft-edge-relnote-archive-stable-channel.md)

 Informationen zu Microsoft Edge-Kanälen finden Sie in der [Übersicht über die Microsoft Edge-Kanäle](microsoft-edge-channels.md).

> [!NOTE]
> Für den Stable Channel erfolgt das Rollout von Updates progressiv über einen oder mehrere Tage. Weitere Informationen hierzu finden Sie unter [Progressive Rollouts für Microsoft Edge-Updates](microsoft-edge-update-progressive-rollout.md).
>
> Die Microsoft Edge-Webplattform entwickelt sich ständig weiter, um Benutzerfreundlichkeit, Sicherheit und Datenschutz zu verbessern. Weitere Informationen finden Sie unter [Änderungen mit Auswirkungen auf die Websitekompatibilität, die für Microsoft Edge anstehen](/microsoft-edge/web-platform/site-impacting-changes).

## <a name="version-91086467-july-8"></a>Version 91.0.864.67: 8. Juli

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-91086464-july-2"></a>Version 91.0.864.64: 2. Juli

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-91086459-june-24"></a>Version 91.0.864.59: 24. Juni

Sicherheitsupdates im Stabilen Kanal sind [hier](/deployedge/microsoft-edge-relnotes-security#june-24-2021) aufgeführt.

## <a name="version-91086454-june-18"></a>Version 91.0.864.54: 18. Juni

> [!Important]
> Dieses Update enthält [CVE-2021-30554](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-30554), für das laut Chromium-Team ein Exploit im Umlauf ist. Weitere Informationen finden Sie im [Leitfaden für Sicherheitsupdates](https://msrc.microsoft.com/update-guide/vulnerability/ADV200002).

Sicherheitsupdates im Stabilen Kanal sind [hier](/deployedge/microsoft-edge-relnotes-security#june-18-2021) aufgeführt.

## <a name="version-91086448-june-11"></a>Version 91.0.864.48: 11. Juni

> [!Important]
>Dieses Update enthält [CVE-2021-30551](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-30551), für das laut Chromium-Team ein Exploit im Umlauf ist. Weitere Informationen finden Sie im [Leitfaden für Sicherheitsupdates](https://msrc.microsoft.com/update-guide/vulnerability/ADV200002).

Sicherheitsupdates im Stabilen Kanal sind [hier](/deployedge/microsoft-edge-relnotes-security#june-11-2021) aufgeführt.

## <a name="version-91086441-june-3"></a>Version 91.0.864.41: 3. Juni

Sicherheitsupdates im Stabilen Kanal sind [hier](/deployedge/microsoft-edge-relnotes-security#june-3-2021) aufgeführt.

## <a name="version-91086437-may-27"></a>Version 91.0.864.37: 27. Mai

Sicherheitsupdates im Stabilen Kanal sind [hier](/deployedge/microsoft-edge-relnotes-security#may-27-2021) aufgeführt.

### <a name="feature-updates"></a>Funktionsupdates

- **Identifizieren Sie den Netzwerkdatenverkehr von Microsoft Defender Application Guard-Containern auf Proxyebene**. Ab Microsoft Edge Version 91 gibt es integrierte Unterstützung zum Markieren von Netzwerkdatenverkehr von Application Guard-Containern, sodass Unternehmen diese identifizieren und bestimmte Richtlinien anwenden können.

- **Unterstützungsoption, um die Synchronisierung von Favoriten vom Host mit dem Microsoft Edge Application Guard-Container zuzulassen**. Ab Microsoft Edge Version 91 haben Benutzer die Möglichkeit, Application Guard so zu konfigurieren, dass ihre Favoriten vom Host mit dem Container synchronisiert werden. Dadurch wird sichergestellt, dass auch neue Favoriten im Container angezeigt werden.

- **Ab Microsoft Edge Version 91 wird der Download von Typen, die Ihrem Computer schaden könnten, vom Browser automatisch unterbrochen, wenn diese Downloads ohne Benutzerinteraktion gestartet werden und von der Überprüfung der SmartScreen-Anwendungszuverlässigkeit nicht unterstützt werden.** Benutzer können den Download überschreiben und fortsetzen, indem sie mit der rechten Maustaste auf das Downloadelement klicken und „Beibehalten“ auswählen. Unternehmensadministratoren können dieses Verhalten deaktivieren, indem sie die folgende Richtlinie konfigurieren:
  - [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](/deployedge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings.md): Deaktivieren von auf Dateierweiterungen basierenden Download-Warnungen für bestimmte Dateitypen in Domänen.

    Weitere Informationen finden Sie unter [Unterbrechung von Microsoft Edge-Sicherheitsdownloads](microsoft-edge-security-downloads-interruptions.md).

- **Unterstützung für Spracherkennungs-APIs**. Ab Microsoft Edge Version 91 wird die API-Unterstützung für Spracherkennungsbefehle auf Google.com und ähnlichen Websites hinzugefügt. Diese Funktion ist auf eine zufällig ausgewählte Gruppe von Benutzern beschränkt, die das Experimentieren aktiviert haben. Diese Benutzer geben dem Feature-Team Feedback.

- **Personalisieren Sie Ihren Browser mit neuen Designfarben.**. Personalisieren Sie Ihr Microsoft Edge mit einer der 14 neuen Designfarben auf der Seite „Einstellungen“ > „Darstellung“. Sie können auch benutzerdefinierte Designs von der Microsoft Edge-Add-On-Website installieren. [Weitere Informationen](https://techcommunity.microsoft.com/t5/articles/make-microsoft-edge-your-own-with-themes/m-p/2083165)

### <a name="policy-updates"></a>Richtlinienupdates

#### <a name="new-policies"></a>Neue Richtlinien

Sechs neue Richtlinien wurden hinzugefügt. Laden Sie die aktualisierten administrativen Vorlagen von der [Microsoft Edge Enterprise-Angebotsseite](https://www.microsoft.com/edge/business/download) herunter. Die folgenden neuen Richtlinien wurden hinzugefügt:

- [ApplicationGuardTrafficIdentificationEnabled](/DeployEdge/microsoft-edge-policies#applicationguardtrafficidentificationenabled) – Application Guard-Netzwerkdatenverkehrsidentifikation
- [ExplicitlyAllowedNetworkPorts](/DeployEdge/microsoft-edge-policies#explicitlyallowednetworkports) – Explizit zugelassene Netzwerkports
- [ImportStartupPageSettings](/DeployEdge/microsoft-edge-policies#importstartuppagesettings) – Import von Startseiteneinstellungen zulassen
- [MathSolverEnabled](/DeployEdge/microsoft-edge-policies#mathsolverenabled) – Benutzer können ein mathematisches Problem mit einer schrittweisen Erläuterung in Microsoft Edge lösen
- [NewTabPageContentEnabled](/DeployEdge/microsoft-edge-policies#newtabpagecontentenabled) – Microsoft News-Inhalt auf der neuen Registerkartenseite zulassen
- [NewTabPageQuickLinksEnabled](/DeployEdge/microsoft-edge-policies#newtabpagequicklinksenabled) – Quicklinks auf der neuen Registerkartenseite zulassen

#### <a name="obsoleted-policy"></a>Veraltete Richtlinie

- [ProactiveAuthEnabled](./microsoft-edge-policies.md#proactiveauthenabled) – Proaktive Authentifizierung aktivieren
<!-- end major 91 -->

## <a name="version-90081866-may-20"></a>Version 90.0.818.66: 20. Mai

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-90081862-may-13"></a>Version 90.0.818.62: 13. Mai

Sicherheitsupdates im Stabilen Kanal sind [hier](/deployedge/microsoft-edge-relnotes-security#may-13-2021) aufgeführt.

## <a name="version-90081856-may-6"></a>Version 90.0.818.56: 6. Mai

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-90081851-april-29"></a>Version 90.0.818.51: 29. April

Sicherheitsupdates im Stabilen Kanal sind [hier](/deployedge/microsoft-edge-relnotes-security#april-29-2021) aufgeführt.

## <a name="version-90081849-april-26"></a>Version 90.0.818.49: 26. April

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-90081846-april-22"></a>Version 90.0.818.46: 22. April ##

Sicherheitsupdates im Stabilen Kanal sind [hier](/deployedge/microsoft-edge-relnotes-security#april-22-2021) aufgeführt.

## <a name="version-90081842-april-19"></a>Version 90.0.818.42: 19. April

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-90081841-april-16"></a>Version 90.0.818.41: 16. April ##

> [!Important]
>Dieses Update enthält [CVE-2021-21224](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21224), für das laut Chromium-Team ein Exploit im Umlauf ist. Weitere Informationen finden Sie im [Leitfaden für Sicherheitsupdates](https://msrc.microsoft.com/update-guide).

Sicherheitsupdates im Stabilen Kanal sind [hier](/deployedge/microsoft-edge-relnotes-security#april-16-2021) aufgeführt.

## <a name="version-90081839-april-15"></a>Version 90.0.818.39: 15. April ##

Sicherheitsupdates im Stabilen Kanal sind [hier](/deployedge/microsoft-edge-relnotes-security#april-15-2021) aufgeführt.

## <a name="feature-updates"></a>Funktionsupdates ##

-    **Einmaliges Anmelden (Single Sign On, SSO) ist jetzt für Azure Active Directory (Azure AD)-Konten und Microsoft-Konten (MSA) unter macOS verfügbar.** Ein bei Microsoft Edge unter macOS angemeldeter Benutzer wird nun automatisch bei Websites angemeldet, die so konfiguriert sind, dass eine einmalige Anmeldung mit Arbeits- und Microsoft-Konten möglich ist (z. B. bing.com, office.com, msn.com und outlook.com).

- **Kioskmodus.** Ab Microsoft Edge Version 90 wurden die Druckeinstellungen der Benutzeroberfläche gesperrt, und es werden nur noch die konfigurierten Drucker und „In PDF drucken“-Optionen zugelassen. Wir haben außerdem Verbesserungen am Kioskmodus für den zugewiesenen Zugriff für nur eine App vorgenommen, um das Starten anderer Anwendungen über den Browser einzuschränken. Weitere Informationen zu den Features des Kioskmodus finden Sie [hier](/deployedge/microsoft-edge-configure-kiosk-mode#kiosk-mode-supported-features).

- **Downloads unterbrechen** Ab Microsoft Edge Version 91 wird der Download von Typen, die Ihrem Computer schaden könnten, vom Browser automatisch unterbrochen, wenn diese Downloads ohne Benutzerinteraktion gestartet werden und von der SmartScreen-Anwendungszuverlässigkeitsüberprüfung nicht unterstützt werden. Benutzer können den Download überschreiben und fortsetzen, indem sie mit der rechten Maustaste auf das Downloadelement klicken und „Beibehalten“ auswählen.
Unternehmensadministratoren können dieses Verhalten mit einer der folgenden beiden Richtlinien deaktivieren:
- [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](/deployedge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings): Deaktivieren von auf Dateierweiterungen basierenden Download-Warnungen für bestimmte Dateitypen in Domänen. Weitere Informationen finden Sie unter [Unterbrechung von Microsoft Edge-Sicherheitsdownloads](/deployedge/microsoft-edge-security-downloads-interruptions)

- **Drucken**:

    - **Neuer Druckrasterungsmodus für Nicht-PostScript-Drucker.** Ab Microsoft Edge Version 90 können Administratoren mithilfe einer neuen Richtlinie den Druckrasterungsmodus für ihre Benutzer definieren. Diese Richtlinie steuert, wie Microsoft Edge unter Windows auf Nicht-PostScript-Druckern druckt. Manchmal müssen Druckaufträge bei Nicht-PostScript-Druckern gerastert werden, damit korrekt gedruckt wird. Die Druckoptionen sind „Full" (Vollständig) und „Fast“ (Schnell).
    
  - **Zusätzliche Optionen für die Seitenskalierung beim Drucken.** Benutzer können jetzt die Skalierung anpassen, während sie Webseiten und PDF-Dokumente mit zusätzlichen Optionen drucken. Die Option „An Seite anpassen" stellt sicher, dass die Webseite oder das Dokument in den Bereich passt, der im ausgewählten „Papierformat" zum Drucken verfügbar ist. Die Option "Tatsächliche Größe" stellt sicher, dass sich die Größe des zu druckenden Inhalts unabhängig von der ausgewählten "Papiergröße" nicht ändert.

-   **Produktivität:**

    -   **Vorschläge zum automatischen Ausfüllen werden um den Inhalt von Adressfeldern aus der Zwischenablage erweitert.** Der Inhalt der Zwischenablage wird analysiert, wenn Sie auf ein Profil-/Adressfeld (z. B. Telefon, E-Mail, Postleitzahl, Stadt, Bundesland usw.) klicken, um es als Vorschläge zum automatischen Ausfüllen anzuzeigen.

    -   **Benutzer können nach Vorschlägen zum automatischen Ausfüllen suchen, auch wenn ein Formular oder Feld nicht erkannt wird.** Wenn Sie Ihre Informationen heute in Microsoft Edge gespeichert haben, werden automatisch Vorschläge zum automatischen Ausfüllen angezeigt, mit denen Sie beim Ausfüllen von Formularen Zeit sparen können. In Fällen, in denen beim automatischen Ausfüllen ein Formular fehlt oder wenn Sie Daten in Formularen abrufen möchten, die normalerweise nicht automatisch ausgefüllt sind (z. B. temporäre Formulare), können Sie mithilfe des automatischen Ausfüllens nach Ihren Informationen suchen.

-   **Greifen Sie über ein Flyout in der Menüleiste auf Downloads zu.** Downloads werden in der oberen rechten Ecke mit allen aktiven Downloads an einem Ort angezeigt. Dieses Menü ist leicht zu schließen, sodass Benutzer ununterbrochen weiter surfen und den gesamten Download-Fortschritt direkt über die Symbolleiste überwachen können. [Weitere Informationen](https://techcommunity.microsoft.com/t5/articles/introducing-the-new-downloads-experience/m-p/2111551).

-   **Verbesserungen beim Rendern von Schriftarten.** Ab Microsoft Edge Version 90 haben wir das Rendern von Text verbessert, um die Klarheit zu verbessern und Unschärfe zu reduzieren. Ein Teil der Verbesserungen beim Rendern von Schriftarten wird in der Beta-Version 90 landen, ist jedoch standardmäßig deaktiviert.

- **Kindermodus.** Wir haben die Richtlinie so aktualisiert, dass bei Aktivierung der Richtlinie nicht nur die Familiensicherheit, sondern auch das Feature „Kindermodus“ deaktiviert wird. Weitere Informationen zum Kindermodus finden Sie [hier](https://go.microsoft.com/fwlink/?linkid=2146910)

## <a name="policy-updates"></a>Richtlinienupdates

## <a name="new-policies"></a>Neue Richtlinien

Acht neue Richtlinien wurden hinzugefügt. Laden Sie die aktualisierten administrativen Vorlagen von der [Microsoft Edge Enterprise-Angebotsseite](https://www.microsoft.com/edge/business/download) herunter. Die folgenden neuen Richtlinien wurden hinzugefügt:
-   [ApplicationGuardFavoritesSyncEnabled](/DeployEdge/microsoft-edge-policies#applicationguardfavoritessyncenabled) – Synchronisierung von Application Guard-Favoriten aktiviert
- [ApplicationGuardTrafficIdentificationEnabled](/DeployEdge/microsoft-edge-policies#applicationguardtrafficidentificationenabled) – Application Guard-Netzwerkdatenverkehrsidentifikation
- [ExplicitlyAllowedNetworkPorts](/DeployEdge/microsoft-edge-policies#explicitlyallowednetworkports) – Explizit zugelassene Netzwerkports
- [ImportStartupPageSettings](/DeployEdge/microsoft-edge-policies#importstartuppagesettings) – Import von Startseiteneinstellungen zulassen
- [MathSolverEnabled](/DeployEdge/microsoft-edge-policies#mathsolverenabled) – Benutzer können ein mathematisches Problem mit einer schrittweisen Erläuterung in Microsoft Edge lösen
- [NewTabPageContentEnabled](/DeployEdge/microsoft-edge-policies#newtabpagecontentenabled) – Microsoft News-Inhalt auf der neuen Registerkartenseite zulassen
- [NewTabPageQuickLinksEnabled](/DeployEdge/microsoft-edge-policies#newtabpagequicklinksenabled) – Quicklinks auf der neuen Registerkartenseite zulassen
-   [FetchKeepaliveDurationSecondsOnShutdown](/DeployEdge/microsoft-edge-policies#fetchkeepalivedurationsecondsonshutdown) – Keepalive-Dauer beim Herunterfahren abrufen
-   [ManagedConfigurationPerOrigin](/DeployEdge/microsoft-edge-policies#managedconfigurationperorigin) – Legt verwaltete Konfigurationswerte für Websites auf bestimmte Ursprünge fest
-   [PrintRasterizationMode](/DeployEdge/microsoft-edge-policies#printrasterizationmode) – Druckrasterungsmodus
-   [QuickViewOfficeFilesEnabled](/DeployEdge/microsoft-edge-policies#quickviewofficefilesenabled) : Verwalten der QuickView Office-Dateifunktion in Microsoft Edge
-   [SSLErrorOverrideAllowedForOrigins](/DeployEdge/microsoft-edge-policies#sslerroroverrideallowedfororigins) – Benutzer können von der HTTPS-Warnseite für bestimmte Ursprünge fortfahren
-   [WindowOcclusionEnabled](/DeployEdge/microsoft-edge-policies#windowocclusionenabled) – Fester-Okklusion aktivieren
-   [WindowsHelloForHTTPAuthEnabled](/DeployEdge/microsoft-edge-policies#windowshelloforhttpauthenabled) – Windows Hello für HTTP-Authentifizierung aktiviert

## <a name="deprecated-policies"></a>Veraltete Richtlinien

- [ProactiveAuthEnabled](/DeployEdge/microsoft-edge-policies#proactiveauthenabled) – Proaktive Authentifizierung aktivieren
-   [NativeWindowOcclusionEnabled](/DeployEdge/microsoft-edge-policies#nativewindowocclusionenabled) – Native Fenster-Okklusion aktivieren
-   [SSLVersionMin](/DeployEdge/microsoft-edge-policies#sslversionmin)– Mindestens aktivierte TLS-Version

## <a name="version-89077477-april-14"></a>Version 89.0.774.77: 14. April

> [!Important]
>Dieses Update enthält [CVE-2021-21206](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21206) und [CVE-2021-21220](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21220), für das laut Chromium-Team ein Exploit im Umlauf ist.  Weitere Informationen finden Sie im [Leitfaden für Sicherheitsupdates](https://msrc.microsoft.com/update-guide).

Sicherheitsupdates im Stabilen Kanal sind [hier](/deployedge/microsoft-edge-relnotes-security#april-14-2021) aufgeführt.

## <a name="version-89077476-april-12"></a>Version 89.0.774.76: 12. April

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-89077475-april-8"></a>Version 89.0.774.75: 8. April

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-89077468-april-1"></a>Version 89.0.774.68 vom 1. April

Sicherheitsupdates im Stabilen Kanal sind [hier](./microsoft-edge-relnotes-security.md#april-1-2021) aufgeführt.

## <a name="version-89077463-march-25"></a>Version 89.0.774.63 vom 25. März

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-89077457-march-18"></a>Version 89.0.774.57: 18. März

Verschiedene Bugs und Leistungsprobleme wurden behoben.

## <a name="version-89077454-march-13"></a>Version 89.0.774.54: 13. März

> [!IMPORTANT]
> Dieses Update enthält [CVE-2021-21193,](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21193) für das laut Chromium-Team ein Exploit im Umlauf ist. Weitere Informationen finden Sie im [Leitfaden für Sicherheitsupdates](https://msrc.microsoft.com/update-guide).

Stabile Kanalsicherheitsupdates sind [hier aufgeführt.](./microsoft-edge-relnotes-security.md#march-13-2021)

## <a name="version-89077450-march-10"></a>Version 89.0.774.50: 10. März

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-89077448-march-8"></a>Version 89.0.774.48: 8. März

Verschiedene Fehler und Leistungsprobleme wurden behoben.

<!-- begin major 89 -->
## <a name="version-89077445-march-4"></a>Version 89.0.774.45: 4. März

> [!IMPORTANT]
> Dieses Update enthält [CVE-2021-21166,](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21166) für das laut Chromium-Team ein Exploit im Umlauf ist. Weitere Informationen finden Sie im [Leitfaden für Sicherheitsupdates](https://msrc.microsoft.com/update-guide).

Stabile Kanalsicherheitsupdates sind [hier aufgeführt.](./microsoft-edge-relnotes-security.md#march-4-2021)

### <a name="resolved-issues"></a>Gelöste Probleme

- **Aktualisierungen und Korrekturen von Taskleisten- und Startmenü-Verknüpfungen:**
  - Wenn Sie mit der rechten Maustaste auf die Microsoft Edge-Verknüpfung im Startmenü klicken, wird jetzt die Option zum Entfernen von Microsoft Edge aus der Taskleiste korrekt angezeigt, wenn es angeheftet ist.
  - Startlayouts, die eine [Taskleistenkonfiguration](/windows/configuration/configure-windows-10-taskbar) zum Anheften von Microsoft Edge an die Taskleiste enthalten, führen nicht mehr dazu, dass eine zweite Microsoft Edge-Verknüpfung an die Taskleiste angeheftet wird.
  - Unternehmen, die Windows-Roaming-Profile verwenden, sehen nicht mehr ein leeres weißes Symbol anstelle des Microsoft Edge-Symbols in der Taskleiste, wenn sich ihre Benutzer bei Windows anmelden.

### <a name="feature-updates"></a>Funktionsupdates

- **Der Kiosk-Modus ermöglicht zusätzliche Sperrfunktionen**. Ab Microsoft Edge Version 89 haben wir zusätzliche Sperrfunktionen im Kioskmodus hinzugefügt, damit Kunden ihre Arbeit produktiver und sicherer erledigen können. [Mehr dazu](microsoft-edge-configure-kiosk-mode.md#kiosk-mode-supported-features).

- **Das Site List Manager-Tool im Enterprise-Modus ist im Browser über die Seite *edge://compat* verfügbar**. Mit diesem Tool können Sie XML-Site-Listen für den Internet Explorer-Modus unter Microsoft Edge erstellen, bearbeiten und exportieren. Sie können den Zugriff auf dieses Tool nach Bedarf über Gruppenrichtlinien aktivieren. [Mehr dazu](./edge-ie-mode-site-list-manager.md).

- **Verbessern der Browserleistung mit ruhenden Registerkarten**. Das Ruhen von Registerkarten verbessert die Browserleistung, indem inaktive Registerkarten in den Ruhezustand versetzt werden, um Systemressourcen wie Speicher und CPU freizugeben, sodass aktive Registerkarten oder andere Anwendungen sie verwenden können. Benutzer können verhindern, dass Websites in den Ruhezustand versetzt werden, und die Zeitspanne konfigurieren, in der eine inaktive Registerkarte in den Ruhezustand versetzt wird. Um die Benutzer in ihrem Fluss zu halten, gibt es auch [Heuristiken](https://techcommunity.microsoft.com/t5/articles/sleeping-tabs-faq/m-p/1705434), die verhindern, dass bestimmte Websites in den Ruhezustand versetzt werden, z. B. Intranetsites. Diese Funktion kann mit Gruppenrichtlinien verwaltet werden.

- **Setzen Sie Ihre Microsoft Edge-Synchronisierungsdaten in der Cloud manuell zurück**. Wir bieten eine Möglichkeit, Ihre Microsoft Edge-Synchronisierungsdaten aus dem Produkt heraus zurückzusetzen. Auf diese Weise wird sichergestellt, dass Ihre Daten aus den Microsoft-Diensten gelöscht werden und bestimmte Produktprobleme behoben werden, für die zuvor ein Support-Ticket erforderlich war.

- **Intelligente Aktivierung von einmaligem Anmelden (Single Sign-On, SSO) für alle Windows Azure Active Directory (Azure AD)-Konten für Benutzer mit einem einzigen Microsoft Edge-Profil ohne Azure AD**.  Aktivieren Sie diese Einstellung automatisch für Benutzer, die von diesem Feature am meisten profitieren können. Wenn ein Benutzer nur über ein Microsoft Edge-Profil verfügt (und es sich nicht um Azure AD oder den Modus für Kinder handelt), wird die Einstellung automatisch aktiviert, sobald Microsoft Edge gestartet wird. Dieser automatische Umschalter wird auch automatisch deaktiviert, wenn sich ein Benutzer später mit einem Azure AD-Konto bei einem anderen Microsoft Edge-Profil anmeldet. Benutzer können ihre Einstellungen für dieses Feature unter **Einstellungen > Profile > Profileinstellungen > Einmaliges Anmelden für Geschäfts-, Schul- oder Uniwebsites mithilfe dieses Profils zulassen** manuell aktualisieren.

- **Verbesserungen bei der Textauswahl in PDF-Dokumenten**. Benutzer erhalten eine reibungslosere und konsistentere Textauswahl für PDF-Dokumente, die ab Version 89 in Microsoft Edge geöffnet werden.

- **Das Feld für das Geburtsdatum wird jetzt beim automatischen Ausfüllen unterstützt**. Heute hilft Ihnen Microsoft Edge, Zeit und Mühe beim Ausfüllen von Formularen und beim Erstellen von Online-Konten zu sparen, indem Sie Ihre Daten wie Adressen, Namen, Telefonnummern usw. automatisch ausfüllen. Ab Microsoft Edge Version 89 bieten wir Unterstützung für ein anderes Feld, das Sie gespeichert und automatisch ausgefüllt haben können – das Geburtsdatum. Sie können diese Informationen jederzeit in Ihren Profileinstellungen anzeigen, bearbeiten und löschen.

### <a name="policy-updates"></a>Richtlinienupdates

#### <a name="new-policies"></a>Neue Richtlinien

Es wurden sieben neue Richtlinien hinzugefügt. Laden Sie die aktualisierten administrativen Vorlagen von der [Microsoft Edge Enterprise-Angebotsseite](https://www.microsoft.com/edge/business/download) herunter. Die folgenden neuen Richtlinien wurden hinzugefügt.

- [BrowsingDataLifetime](./microsoft-edge-policies.md#browsingdatalifetime) – Durchsuchen der Einstellungen für die Lebensdauer von Daten
- [MAMEnabled](./microsoft-edge-policies.md#mamenabled) – Mobile App Management aktiviert
- [DefinePreferredLanguages](./microsoft-edge-policies.md#definepreferredlanguages) – Definiert eine geordnete Liste der bevorzugten Sprachen, in denen Websites angezeigt werden sollen, wenn die Website die Sprache unterstützt
- [ShowRecommendationsEnabled](./microsoft-edge-policies.md#showrecommendationsenabled) – Zulassen von Empfehlungen und Werbebenachrichtigungen von Microsoft Edge
- [PrintingAllowedBackgroundGraphicsModes](./microsoft-edge-policies.md#printingallowedbackgroundgraphicsmodes) – Einschränken des Druckmodus für Hintergrundgrafiken
- [PrintingBackgroundGraphicsDefault](./microsoft-edge-policies.md#printingbackgroundgraphicsdefault)– Standard-Druckmodus für Hintergrundgrafiken
- [SmartActionsBlockList](./microsoft-edge-policies.md#smartactionsblocklist)– Blockieren der intelligenten Aktionen für eine Liste von Diensten

#### <a name="obsoleted-policies"></a>Veraltete Richtlinie

Die folgenden Richtlinien sind veraltet.

- [ForceLegacyDefaultReferrerPolicy](./microsoft-edge-policies.md#forcelegacydefaultreferrerpolicy): Verwenden Sie die standardmäßige Verweiserrichtlinie „kein Verweiser beim Downgrade“
- [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) – Aktivieren Sie die Berichterstellung für Nutzung und Absturz
- [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices) – Senden von Site-Informationen, um die Microsoft-Dienste zu verbessern
<!-- end major 89 -->

<!-- Archive from 86.0.622.43: October 15 to beta 88.0.705.81: February 25  ->
<!-- Archive from 86.0.622.38-october-9 to beta 86.0.62.215-september-14  ->
<!-- Archived to version 84.0.522.40: July 16 -->

## <a name="see-also"></a>Weitere Informationen

- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)
