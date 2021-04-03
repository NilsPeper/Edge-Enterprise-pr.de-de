---
title: Versionshinweise von Microsoft Edge für Stable Channel
ms.author: aguta
author: dan-wesley
manager: srugh
ms.date: 03/25/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Versionshinweise von Microsoft Edge für Stable Channel
ms.openlocfilehash: 36f6e5fe462fcb4c43862754603bef7902fcf670
ms.sourcegitcommit: 93851b83dc11422924646a04a9e0f60ff2554af7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "11470273"
---
# <a name="release-notes-for-microsoft-edge-stable-channel"></a>Versionshinweise für Microsoft Edge Stable Channel

Diese Versionshinweise enthalten Informationen zu neuen Funktionen und nicht sicherheitsrelevanten Updates, die im Microsoft Edge Stable Channel enthalten sind.

- Alle Sicherheitsupdates werden [hier](microsoft-edge-relnotes-security.md) aufgelistet.
- Archivierte Versionshinweise für Microsoft Edge Stable Channel finden Sie [hier.](microsoft-edge-relnote-archive-stable-channel.md)

 Informationen zu Microsoft Edge-Kanälen finden Sie in der [Übersicht über die Microsoft Edge-Kanäle](microsoft-edge-channels.md).

> [!NOTE]
> Für den Stable Channel erfolgt das Rollout von Updates progressiv über einen oder mehrere Tage. Weitere Informationen hierzu finden Sie unter [Progressive Rollouts für Microsoft Edge-Updates](microsoft-edge-update-progressive-rollout.md).

## <a name="version-89077463-march-25"></a>Version 89.0.774.63: 25. März

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

- **Verbessern der Browserleistung mit ruhenden Registerkarten**. Das Ruhen von Registerkarten verbessert die Browserleistung, indem inaktive Registerkarten in den Ruhezustand versetzt werden, um Systemressourcen wie Speicher und CPU freizugeben, sodass aktive Registerkarten oder andere Anwendungen sie verwenden können. Benutzer können verhindern, dass Websites in den Ruhezustand versetzt werden, und die Zeitspanne konfigurieren, in der eine inaktive Registerkarte in den Ruhezustand versetzt wird. Um die Benutzer in ihrem Fluss zu halten, gibt es auch [Heuristiken](https://techcommunity.microsoft.com/t5/articles/sleeping-tabs-faq/m-p/1705434), die verhindern, dass bestimmte Websites in den Ruhezustand versetzt werden, z.B. Intranetsites. Diese Funktion kann mit Gruppenrichtlinien verwaltet werden.

- **Setzen Sie Ihre Microsoft Edge-Synchronisierungsdaten in der Cloud manuell zurück**. Wir bieten eine Möglichkeit, Ihre Microsoft Edge-Synchronisierungsdaten aus dem Produkt heraus zurückzusetzen. Auf diese Weise wird sichergestellt, dass Ihre Daten aus den Microsoft-Diensten gelöscht werden und bestimmte Produktprobleme behoben werden, für die zuvor ein Support-Ticket erforderlich war.

- **Intelligente Aktivierung von einmaligem Anmelden (Single Sign-On, SSO) für alle Windows Azure Active Directory (Azure AD)-Konten für Benutzer mit einem einzigen Microsoft Edge-Profil ohne Azure AD**.  Aktivieren Sie diese Einstellung automatisch für Benutzer, die von diesem Feature am meisten profitieren können. Wenn ein Benutzer nur über ein Microsoft Edge-Profil verfügt (und es sich nicht um Azure AD oder den Modus für Kinder handelt), wird die Einstellung automatisch aktiviert, sobald Microsoft Edge gestartet wird. Dieser automatische Umschalter wird auch automatisch deaktiviert, wenn sich ein Benutzer später mit einem Azure AD-Konto bei einem anderen Microsoft Edge-Profil anmeldet. Benutzer können ihre Einstellungen für dieses Feature unter **Einstellungen > Profile > Profileinstellungen > Einmaliges Anmelden für Geschäfts-, Schul- oder Uniwebsites mithilfe dieses Profils zulassen** manuell aktualisieren.

- **Verbesserungen bei der Textauswahl in PDF-Dokumenten**. Benutzer erhalten eine reibungslosere und konsistentere Textauswahl für PDF-Dokumente, die ab Version 89 in Microsoft Edge geöffnet werden.

- **Das Feld für das Geburtsdatum wird jetzt beim automatischen Ausfüllen unterstützt**. Heute hilft Ihnen Microsoft Edge, Zeit und Mühe beim Ausfüllen von Formularen und beim Erstellen von Online-Konten zu sparen, indem Sie Ihre Daten wie Adressen, Namen, Telefonnummern usw. automatisch ausfüllen. Ab Microsoft Edge Version 89 bieten wir Unterstützung für ein anderes Feld, das Sie gespeichert und automatisch ausgefüllt haben können – das Geburtsdatum. Sie können diese Informationen jederzeit in Ihren Profileinstellungen anzeigen, bearbeiten und löschen.

### <a name="policy-updates"></a>Richtlinienupdates

#### <a name="new-policies"></a>Neue Richtlinien

Es wurden sieben neue Richtlinien hinzugefügt. Laden Sie die aktualisierten administrativen Vorlagen von der [Microsoft Edge Enterprise Angebotsseite](https://www.microsoft.com/edge/business/download) herunter. Die folgenden neuen Richtlinien wurden hinzugefügt.

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
## <a name="version-88070581-february-25"></a>Version 88.0.705.81: 25. Februar

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-88070574-february-17"></a>Version 88.0.705.74: 17. Februar

Stabile Kanalsicherheitsupdates sind [hier aufgeführt.](./microsoft-edge-relnotes-security.md#february-17-2021)

## <a name="version-88070568-february-11"></a>Version 88.0.705.68: 11. Februar

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-88070563-february-5"></a>Version 88.0.705.63: 5. Februar

> [!IMPORTANT]
> Dieses Update enthält [CVE-2021-21148,](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21148) für das laut Chromium-Team ein Exploit im Umlauf ist.

Stabile Kanalsicherheitsupdates sind [hier aufgeführt.](./microsoft-edge-relnotes-security.md#february-5-2021)

## <a name="version-88070562-february-4"></a>Version 88.0.705.62: 4. Februar

Stabile Kanalsicherheitsupdates sind [hier aufgeführt.](./microsoft-edge-relnotes-security.md#february-4-2021)

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-88070556-january-28"></a>Version 88.0.705.56: 28. Januar

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-88070553-january-26"></a>Version 88.0.705.53: 26. Januar

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-88070550-january-21"></a>Version 88.0.705.50: 21. Januar

Stabile Kanalsicherheitsupdates sind [hier aufgeführt.](./microsoft-edge-relnotes-security.md#january-21-2021)

<!--- begin major 88  --->
### <a name="feature-updates"></a>Funktionsupdates

- **Abschreibungen:**

  - Veraltete Unterstützung für das FTP-Protokoll. Die Unterstützung für das ältere FTP-Protokoll wurde von Microsoft Edge entfernt. Der Versuch, zu einer FTP-Verbindung zu navigieren, führt dazu, dass der Browser das Betriebssystem anweist, eine externe Anwendung zu öffnen, um die FTP-Verbindung zu verarbeiten. Alternativ können IT-Administratoren Microsoft Edge so konfigurieren, dass der IE-Modus für Sites verwendet wird, die auf dem FTP-Protokoll basieren.
  - Die Adobe Flash-Unterstützung wird entfernt. Ab Microsoft Edge Beta Version 88 werden die Adobe Flash-Funktionen und die Unterstützung entfernt. Weitere Informationen: [Update auf Adobe Flash Player Ende der Unterstützung – Microsoft Edge-Blog (windows.com)](https://blogs.windows.com/msedgedev/2020/09/04/update-adobe-flash-end-support/)

- **Authentifizierung:**

  - Einmaliges Anmelden (SSO, Single Sign On) ist jetzt für Azure Active Directory-Konten (Azure AD) und Microsoft-Konto (MSA) unter Windows auf niedrigerer Ebene verfügbar. Ein Benutzer, der bei Microsoft Edge unter Microsoft Windows auf niedrigerer Ebene (7, 8.1) angemeldet ist, wird jetzt automatisch bei Websites angemeldet, die so konfiguriert sind, dass sie eine einmalige Anmeldung mit Geschäfts- und Microsoft-Konten ermöglichen (z. B. bing.com, office.com, msn.com, outlook.com).<br>Hinweis: Ein Benutzer muss sich möglicherweise abmelden und dann erneut anmelden, wenn er sich in einer Version vor Microsoft Edge 88 bei Microsoft Edge angemeldet hat, um diese Funktion nutzen zu können.
  
  - Single Sign-On (SSO) auf Geschäftswebsites mit beliebigen Windows Azure Active Directory (Azure AD)-Konten auf dem System in Nicht-Azure AD-Microsoft Edge-Profilen. Dieses Feature kann für jedes Profil aktiviert werden, das nicht mit einem Geschäfts-/Schulkonto angemeldet ist und nicht Gast oder Privat ist und die Verwendung eines beliebigen angemeldeten Geschäfts-/Schulkontos auf dem Betriebssystem mit diesem Profil zulässt. Dieses Feature kann in **Einstellungen** > **Profile** > **Profileinstellungen** > **Single Sign-on für Geschäfts- und Schulwebsites mit diesem Profil erlauben** konfiguriert werden.
  
    > [!NOTE]
    > „Single Sign-On (SSO) für alle Windows-Konten, die das Microsoft Edge-Profil verwenden" ist eine Aktualisierung für die Versionshinweise vom 21. Januar.

- **Kioskmodus-Option zum Beenden der Sitzung**. Die Schaltfläche „Sitzung beenden“ ist jetzt im öffentlichen Browsing im Kioskmodus verfügbar. Diese Funktion stellt sicher, dass Browserdaten und -einstellungen gelöscht werden, wenn Microsoft Edge geschlossen wird. Weitere Informationen zu den Funktionen und der Roadmap des Kioskmodus finden Sie unter [Konfigurieren des Microsoft Edge-Kioskmodus](./microsoft-edge-configure-kiosk-mode.md).

- **Sicherheit und Datenschutz:**

  - Benachrichtigungen werden generiert, wenn das Kennwort eines Benutzers in einem Onlineleck gefunden wird. Benutzerkennwörter werden gegen ein Verzeichnis bekannter Anmeldeinformationen überprüft und geben dem Benutzer eine Warnung zurück, wenn eine Übereinstimmung gefunden wird. Um die Sicherheit und den Datenschutz zu gewährleisten, werden Benutzerkennwörter gehashed und verschlüsselt, wenn Sie mit der Datenbank der durchgesickerten Anmeldeinformationen abgeglichen werden.
  - Aktualisieren Sie gemischte Inhalte automatisch. Über HTTPS gelieferte sichere Seiten können Referenzbilder enthalten, die über nicht sicheres HTTP bereitgestellt werden. Um den Datenschutz und die Sicherheit in Microsoft Edge 88 zu verbessern, werden diese Bilder stattdessen über HTTPS abgerufen. Wenn das Bild nicht über HTTPS verfügbar ist, wird es nicht geladen.
  - Anzeigen von Site-Berechtigungen nach Site und nach letzten Aktivitäten. Ab Microsoft Edge 88 können Benutzer Site-Berechtigungen einfacher verwalten. Sie können Berechtigungen nach Website und nicht nur nach Berechtigungstyp anzeigen. Darüber hinaus haben wir einen Abschnitt mit den letzten Aktivitäten hinzugefügt, in dem ein Benutzer alle letzten Änderungen an seinen Websiteberechtigungen anzeigt.
  - Verbesserte Steuerelemente für Browser-Cookies. Ab Microsoft Edge 88 können Benutzer Cookies von Drittanbietern löschen, ohne dass dies Auswirkungen auf Cookies von Drittanbietern hat. Benutzer können ihre Cookies auch nach Erst- oder Drittanbietern filtern und nach Name, Anzahl der Cookies und der Menge der gespeicherten und zuletzt geänderten Daten sortieren.

- **Kennwörter:**

  - Kennwortgenerator. Microsoft Edge bietet einen integrierten Generator für starke Kennwörter an, den Sie beim Erstellen eines neuen Kontos oder beim Ändern eines vorhandenen Kennworts verwenden können. Suchen Sie einfach nach dem vom Browser vorgeschlagenen Kennwort-Dropdown im Kennwortfeld. Wenn diese Option ausgewählt ist, wird sie Kennwörter automatisch im Browser speichern und geräteübergreifend synchronisieren, damit Sie diese in Zukunft einfach verwenden können.
  - Kennwortüberwachung. Wenn eines Ihrer im Browser gespeicherten Kennwörter mit denen in der Liste der kompromittierten Anmeldeinformationen übereinstimmt, benachrichtigt Microsoft Edge Sie und fordert Sie auf, Ihr Kennwort zu aktualisieren. Die Kennwortüberwachung prüft in Ihrem Auftrag auf Übereinstimmungen und ist standardmäßig aktiviert.
  - Kennwort bearbeiten. Sie können ihre gespeicherten Kennwörter jetzt direkt in den Microsoft Edge-Einstellungen bearbeiten. Jedes Mal, wenn ein Kennwort außerhalb von Microsoft Edge aktualisiert wurde, können Sie das gespeicherte ältere Kennwort ganz einfach durch das neue ersetzen, indem Sie den gespeicherten Eintrag in den Einstellungen bearbeiten. 

- **Verbessern der Startgeschwindigkeit von Microsoft Edge mit der Startbeschleunigung**. Um die Startgeschwindigkeit von Microsoft Edge zu verbessern, haben wir eine Funktion namens Startup Boost entwickelt. Durch den Startschub wird der Start von Microsoft Edge beschleunigt, da Microsoft Edge im Hintergrund ausgeführt werden kann. Hinweis: Diese Funktion ist auf eine zufällig ausgewählte Gruppe von Benutzern beschränkt, die das Experimentieren aktiviert haben. Diese Benutzer geben dem Feature-Team Feedback.

- **Produktivität:**

  - Verbessern Sie die Produktivität und das Multitasking mit vertikalen Registerkarten. Wenn die Anzahl der horizontalen Registerkarten zunimmt, werden die Site-Titel abgeschnitten und die Steuerelemente der Registerkarten gehen verloren, wenn die einzelnen Registerkarten verkleinert werden. Dies unterbricht den Benutzerworkflow, da sie mehr Zeit damit verbringen, ihre Registerkarten zu finden, zu wechseln und zu verwalten, und weniger Zeit für die jeweilige Aufgabe. Mit vertikalen Registerkarten können Benutzer ihre Registerkarten zur Seite verschieben. Vertikal ausgerichtete Symbole und längere Site-Titel erleichtern das schnelle Scannen, Identifizieren und Wechseln zu der Registerkarte, die sie öffnen möchten.
  - Das Feld für das Geburtsdatum wird automatisch ausgefüllt. Microsoft Edge spart bereits Zeit und Mühe beim Ausfüllen von Formularen und beim Erstellen von Online-Konten, indem Benutzerdaten wie Adressen, Namen, Telefonnummern usw. automatisch ausgefüllt werden. Microsoft Edge unterstützt jetzt das Feld für das Geburtsdatum, das Benutzer speichern und automatisch ausfüllen können. Ein Benutzer kann diese Informationen jederzeit in seinen Profileinstellungen anzeigen, bearbeiten und löschen.
  - Verbesserungen an Vor kurzem im Verlauf geschlossen. „Vor kurzem geschlossen“ behält jetzt die letzten 25 Registerkarten und Fenster aus früheren Browsersitzungen und nicht nur aus der vorherigen Sitzung bei. Benutzer können in der neuen Verlaufserfahrung die Option „Zuletzt geschlossen“ auswählen, um alle geöffneten Registerkarten anzuzeigen.
  - Das Feature "Ihr Tag auf einen Blick" ist standardmäßig aktiviert. Beginnend mit Microsoft Edge Version 88 können Informationsdienste von intelligenten Produktivitätsfunktionen auf ihrer „Neue Registerkartenseite (NTP)“ profitieren. Microsoft Edge 87-Benutzern werden diese Erfahrungen innerhalb von zwei Wochen nach der Veröffentlichung von Microsoft Edge 88 auch erhalten. Wir bieten Benutzern, die mit Ihrem Geschäfts- oder Schulkonto angemeldet sind, personalisierte und relevante Inhalte an, die von ihrem M365 Graph unterstützt werden. Benutzer können Ihre "Ihr Tag auf einen Blick"-Module schnell durchsuchen, um Ihre Besprechungen und die aktuelle Arbeit zu überwachen sowie die Anwendungen, die Sie verwenden möchten, schnell zu starten.

- **Verlaufs- und geöffnete Registerkarten-Synchronisierung**. Die Verlaufssynchronisierung und Synchronisierung von geöffneten Registerkarten ist jetzt für Benutzer verfügbar. Das Aktivieren dieses Features hilft Benutzern dort weiterzumachen, wo Sie aufgehört haben, indem Sie ihren Browserverlauf und die geöffneten Registerkarten auf allen ihren Synchronisierungsgeräten zur Verfügung stellen. Wir haben die Synchronisierungs- und Browserverlaufsrichtlinien aktualisiert, sodass die Benutzer jetzt über Microsoft Edge geräteübergreifend verbunden und produktiv sind. [Mehr dazu](https://blogs.windows.com/windowsexperience/2021/01/21/this-year-lets-resolve-to-make-the-most-of-our-time-online-and-better-protect-ourselves-from-online-threats/).

- **PDF:**

  - PDF-Dokumentanzeige in der Buchansicht (zwei Seiten). Ab Microsoft Edge Version 88 können Benutzer PDF-Dokumente auf einer einzelnen Seite oder in der zweiseitigen Buchansicht anzeigen. Um die Ansicht zu ändern, klicken Sie in der Symbolleiste auf die Schaltfläche **Seitenansicht**.
  - Unterstützung für verankerte Textnotizen für PDF-Dateien. Ab Microsoft Edge Version 87 können Benutzer zu jedem Text in PDF-Dateien getippte Textnotizen hinzufügen.

- **Schriftarten:**

  - Browsersymbole werden auf das Fluent-Designsystem aktualisiert. Im Rahmen unserer fortgesetzten Arbeit an Fluent Design im Browser haben wir Änderungen vorgenommen, um die Symbole näher am neuen Microsoft-Symbolsystem auszurichten. Diese Änderungen wirken sich auf viele unserer High-Touch-Benutzeroberflächen aus, einschließlich Registerkarten, Adressleiste sowie Navigations- und Wegfindungssymbole in unseren verschiedenen Menüs.
  - Verbesserte Schriftwiedergabe. Die Textwiedergabe wurde verbessert, um die Übersichtlichkeit zu verbessern und Unschärfe zu verringern.

### <a name="policy-updates"></a>Richtlinienupdates

#### <a name="new-policies"></a>Neue Richtlinien

Achtzehn neue Richtlinien wurden hinzugefügt. Laden Sie die aktualisierten administrativen Vorlagen von der [Microsoft Edge Enterprise-Angebotsseite](https://www.microsoft.com/edge/business/download) herunter. Die folgenden neuen Richtlinien wurden hinzugefügt.

- [BasicAuthOverHttpEnabled](./microsoft-edge-policies.md#basicauthoverhttpenabled) – Lassen Sie die Standardauthentifizierung für HTTP zu.
- [BlockExternalExtensions](./microsoft-edge-policies.md#blockexternalextensions) – Blockieren Sie die Installation externer Erweiterungen.
- [InternetExplorerIntegrationLocalFileAllowed](./microsoft-edge-policies.md#internetexplorerintegrationlocalfileallowed) – Ermöglichen Sie das Starten lokaler Dateien im Internet Explorer-Modus.
- [InternetExplorerIntegrationLocalFileExtensionAllowList](./microsoft-edge-policies.md#internetexplorerintegrationlocalfileextensionallowlist) – Öffnen Sie lokale Dateien im Internet Explorer-Modus.
- [InternetExplorerIntegrationLocalFileShowContextMenu](./microsoft-edge-policies.md#internetexplorerintegrationlocalfileshowcontextmenu) – Leiten Sie das Kontextmenü an, einen Link im Internet Explorer-Modus zu öffnen.
- [IntranetRedirectBehavior](./microsoft-edge-policies.md#intranetredirectbehavior) – Intranet-Umleitungsverhalten.
- [PrinterTypeDenyList](./microsoft-edge-policies.md#printertypedenylist) – Deaktivieren Sie die Druckertypen in der Verweigerungsliste.
- [ShowMicrosoftRewards](./microsoft-edge-policies.md#showmicrosoftrewards) – Zeigen Sie Microsoft Rewards-Erfahrungen an.
- [SleepingTabsEnabled](./microsoft-edge-policies.md#sleepingtabsenabled) – Konfigurieren Sie Sleeping Tabs.
- [SleepingTabsTimeout](./microsoft-edge-policies.md#sleepingtabstimeout) – Legen Sie das Zeitlimit für die Inaktivität der Hintergrundregisterkarte für Sleeping Tabs fest.
- [SleepingTabsBlockedForUrls](./microsoft-edge-policies.md#sleepingtabsblockedforurls) – Blockieren Sie Sleeping Tabs auf bestimmten Websites.
- [StartupBoostEnabled](./microsoft-edge-policies.md#startupboostenabled) – Aktivieren Sie die Startbeschleunigung.
- [TargetBlankImpliesNoOpener](./microsoft-edge-policies.md#targetblankimpliesnoopener) – Legen Sie "window.opener" nicht für Links fest, die auf _blank abzielen.
- [UpdatePolicyOverride](./microsoft-edge-policies.md#updatepolicyoverride) – Gibt an, wie Microsoft Edge Update verfügbare Updates von Microsoft Edge verarbeitet. 
- [VerticalTabsAllowed](./microsoft-edge-policies.md#verticaltabsallowed) – Konfiguriert die Verfügbarkeit eines vertikalen Layouts für Registerkarten an der Seite des Browsers.
- [WebRtcAllowLegacyTLSProtocols](./microsoft-edge-policies.md#webrtcallowlegacytlsprotocols) – Ermöglichen Sie ein älteres TLS/DTLS-Downgrade in WebRTC.
- [WebWidgetAllowed](./microsoft-edge-policies.md#webwidgetallowed) – Aktivieren Sie das Web-Widget.
- [WebWidgetIsEnabledOnStartup](./microsoft-edge-policies.md#webwidgetisenabledonstartup) – Lassen Sie das Web-Widget beim Start von Windows zu.

#### <a name="deprecated-policies"></a>Veraltete Richtlinien

- [ProactiveAuthEnabled](./microsoft-edge-policies.md#proactiveauthenabled) – Aktivieren Sie die proaktive Authentifizierung.
- [ProxyBypassList](./microsoft-edge-policies.md#proxybypasslist) – Konfigurieren Sie die Proxy-Umgehungsregeln.
- [ProxyMode](./microsoft-edge-policies.md#proxymode) – Konfigurieren Sie die Proxy-Server-Einstellungen.
- [ProxyPacUrl](./microsoft-edge-policies.md#proxypacurl) – Legen Sie die URL der Proxy .pac-Datei fest.
- [Proxyserver](./microsoft-edge-policies.md#proxyserver) – Konfigurieren Sie die Adresse oder URL des Proxyservers.
- [WebDriverOverridesIncompatiblePolicies](./microsoft-edge-policies.md#webdriveroverridesincompatiblepolicies) – Erlauben Sie WebDriver, inkompatible Richtlinien zu überschreiben.

### <a name="obsoleted-policies"></a>Abgeschaffte Richtlinien

- [AllowPopupsDuringPageUnload](./microsoft-edge-policies.md#allowpopupsduringpageunload) – Ermöglicht einer Seite das Anzeigen von Popups während der Entladung.
- [DefaultPluginsSetting](./microsoft-edge-policies.md#defaultpluginssetting) – Standardeinstellung für Adobe Flash.
- [PluginsAllowedForUrls](./microsoft-edge-policies.md#pluginsallowedforurls) – Lassen Sie das Adobe Flash-Plug-In auf bestimmten Websites zu.
- [PluginsBlockedForUrls](./microsoft-edge-policies.md#pluginsblockedforurls) – Blockieren Sie das Adobe Flash-Plug-in auf bestimmten Websites.
- [RunAllFlashInAllowMode](./microsoft-edge-policies.md#runallflashinallowmode) – Erweitern der Adobe Flash-Inhaltseinstellung auf alle Inhalte.
<!--- end major 88  --->
## <a name="version-87066475-january-7"></a>Version 87.0.664.75: 7. Januar

Stabile Kanalsicherheitsupdates sind [hier aufgeführt.](./microsoft-edge-relnotes-security.md#january-7-2021)

## <a name="version-87066466-december-17"></a>Version 87.0.664.66: 17. Dezember

Verschiedene Bugs und Leistungsprobleme wurden behoben.

## <a name="version-87066460-december-10"></a>Version 87.0.664.60: 10. Dezember

Verschiedene Bugs und Leistungsprobleme wurden behoben.

## <a name="version-87066457-december-7"></a>Version 87.0.664.57: 7. Dezember

Verschiedene Fehler und Leistungsprobleme wurden behoben. Stabile Kanalsicherheitsupdates sind [hier aufgeführt.](./microsoft-edge-relnotes-security.md#december-7-2020)

## <a name="version-87066455-december-3"></a>Version 87.0.664.55: 3. Dezember

Verschiedene Bugs und Leistungsprobleme wurden behoben. Das folgende Feature wurde mit diesem Release aktualisiert.

- **Shopping ist standardmäßig aktiviert**. Ab Microsoft Edge, Version87, können Unternehmensbenutzer von Shopping-Features in Microsoft Edge profitieren. Mit den Shopping-Features hilft Microsoft Edge Benutzern, beim Onlineshopping Gutscheine und bessere Preise zu finden. (Die Coupon-Erfahrung wurde mit Stable Version 87.0.664.41 veröffentlicht). Die Preisvergleich-Erfahrung ist jetzt mit diesem Update verfügbar. Dieses Feature kann mithilfe der [EdgeShoppingAssistantEnabled](./microsoft-edge-policies.md#edgeshoppingassistantenabled)-Richtlinie konfiguriert werden. Schauen Sie sich unseren [Blog](https://blogs.windows.com/windowsexperience/2020/11/19/finish-up-that-holiday-shopping-with-new-features-from-microsoft-edge-and-bing/) an, und [erfahren Sie mehr](/microsoft-edge/privacy-whitepaper#shopping) über Microsoft Shopping.

## <a name="version-87066452-november-30"></a>Version 87.0.664.52: 30. November

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-87066447-november-23"></a>Version 87.0.664.47: vom 23. November

Verschiedene Fehler und Leistungsprobleme wurden behoben.

<!-- begin major 87 --->
## <a name="version-87066441-november-19"></a>Version 87.0.664.41: 19. November

Stabile Kanalsicherheitsupdates sind [hier aufgeführt.](./microsoft-edge-relnotes-security.md#november-19-2020)

### <a name="feature-updates"></a>Funktionsupdates

- **Automatisches Umleiten von inkompatiblen Websites aus Internet Explorer zu MicrosoftEdge**. Ab dem Microsoft Edge 87 Stable-Update werden öffentliche Websites, die eine Inkompatibilitätsmeldung in Internet Explorer anzeigen, automatisch an Microsoft Edge umgeleitet. Weitere Informationen hierzu und zum Konfigurieren dieser Umgebung finden Sie unter [Umleiten von nicht kompatiblen Websites](./edge-learnmore-neededge.md).

- **Datenschutzfeatures des Kioskmodus aktiviert**. Ab MicrosoftEdge, Version87, werden Kioskmodus-Features aktiviert, die Unternehmen im Zusammenhang mit dem Datenschutz für Benutzerdaten helfen. Diese Features ermöglichen es beispielsweise, dass die Benutzerdaten beim Beenden gelöscht werden, dass heruntergeladene Dateien gelöscht werden und dass die konfigurierte Startumgebung nach einer festgelegten Leerlaufzeitspanne zurückgesetzt wird. Informieren Sie sich genauer zum [Konfigurieren des MicrosoftEdge-Kioskmodus](./microsoft-edge-configure-kiosk-mode.md).

- **Shopping-Features standardmäßig aktiviert**. Ab Microsoft Edge, Version87, können Unternehmensbenutzer auch von Shopping-Features in Microsoft Edge profitieren. Mit den Shopping-Features hilft Microsoft Edge Benutzern, beim Onlineshopping Gutscheine und bessere Preise zu finden. Die Couponumgebung ist mit diesem Update verfügbar, und der Preisvergleich wird in den bevorstehenden Updates für Microsoft Edge 87 veröffentlicht. Dieses Feature kann über die [EdgeShoppingAssistantEnabled](./microsoft-edge-policies.md#edgeshoppingassistantenabled)-Richtlinie konfiguriert werden. Schauen Sie sich unseren [Blog](https://blogs.windows.com/windowsexperience/2020/11/19/finish-up-that-holiday-shopping-with-new-features-from-microsoft-edge-and-bing/) an, und [erfahren Sie mehr](/microsoft-edge/privacy-whitepaper#shopping) über Microsoft Shopping.

- **ClickOnce-Bereitstellung standardmäßig aktiviert**. ClickOnce ist in MicrosoftEdge87 standardmäßig aktiviert, wodurch die Hindernisse für Unternehmen reduziert werden, die Software bereitstellen und mit dem Browserverhalten der Vorgängerversion von MicrosoftEdge besser übereinstimmen möchten. Ab MicrosoftEdge87 gibt der Status „Nicht konfiguriert“ der Richtlinie „ClickOnceEnabled“ den neuen standardmäßigen ClickOnce-Status „Aktiviert“ (im Vergleich zum vorherigen Standardstatus „Deaktiviert“) wieder.

- **Auf der Enterprise-Seite „Neue Registerkarte” (New Tab Page, NTP) wird Produktivität in anpassbare, arbeitsrelevante Feedinhalte integriert**. Im Enterprise-NTP-Bereich werden die Office365-Produktivitätsseite, die wir den mit ihrem Geschäfts-, Schul-oder Unikonto angemeldeten Benutzern bieten, mit personalisierten, arbeitsrelevanten Unternehmens- und Branchenfeeds zusammengeführt, die auf einer einzigen Seite organisiert sind. Benutzer können die vertrauten Office365-Inhalte und MicrosoftSearch for Business erkennen, das von Bing unterstützt wird. Darüber hinaus können sie "Mein Feed" leicht anpassen, indem sie aus den verfügbaren Inhalten und Modulen für ihre Organisation die für sie relevantesten auswählen. IT-Administratoren können die Einstellungen für Newsfeeds für Ihre Organisation, einschließlich der ausgewählten Branche für die Microsoft Edge-Seite "Neue Registerkarte", über das Microsoft 365 Admin Center steuern. [Weitere Informationen](https://blogs.windows.com/msedgedev/2020/10/29/enterprise-new-tab-page-my-feed/)

- **Datenschutz und Sicherheit:**

  - Unterstützung von TLS-Tokenbindung für mit Richtlinien konfigurierte Websites. Die TLS-Tokenbindung hilft bei der Verhinderung von Angriffen zum Diebstahl von Token, um sicherzustellen, dass Cookies nur auf dem Gerät wiederverwendet werden können, auf dem sie ursprünglich festgelegt wurden. Die Verwendung der TLS-Tokenbindung erfordert es, dass die Richtlinie [AllowTokenBindingForUrls](./microsoft-edge-policies.md#allowtokenbindingforurls) festgelegt wurde und dass die aufgeführten Websites dieses Feature unterstützen.

- **Tastaturunterstützung für Textmarker in PDF-Dateien**. Benutzer können jeden beliebigen Text in einer PDF-Datei mithilfe ihrer Tastatur hervorheben.

- **Drucken:**

  - Wählen Sie die Seite aus, die beim beidseitigen Drucken gedreht werden soll. Benutzer können auswählen, ob ein Blatt beim beidseitigen Drucken auf die lange Seite (Querformat) oder die kurze Seite (Hochformat) gedreht werden soll.
  - Wählen Sie den Druckmodus „Rasterung“ für das Unternehmen aus. Steuern Sie, wie MicrosoftEdge auf einem Nicht-PostScript-Drucker unter Windows druckt. Manchmal müssen Druckaufträge bei Nicht-PostScript-Druckern gerastert werden, damit korrekt gedruckt wird. Die Druckoptionen sind „Full" (Vollständig) und „Fast“ (Schnell).

### <a name="policy-updates"></a>Richtlinienupdates

#### <a name="new-policies"></a>Neue Richtlinien

Es wurden zehn neue Richtlinien hinzugefügt. Laden Sie die aktualisierten administrativen Vorlagen von der [Microsoft Edge Enterprise Angebotsseite](https://www.microsoft.com/edge/business/download) herunter. Die folgenden neuen Richtlinien wurden hinzugefügt.

- [ConfigureFriendlyURLFormat](./microsoft-edge-policies.md#configurefriendlyurlformat) – Zum Konfigurieren des Standardformats für das Einfügen von URLs, die aus MicrosoftEdge kopiert wurden, und zum Ermitteln, ob Benutzern weitere Formate zur Verfügung stehen.
- [EdgeShoppingAssistantEnabled](./microsoft-edge-policies.md#edgeshoppingassistantenabled) – Shopping in MicrosoftEdge aktiviert.
- [HideInternetExplorerRedirectUXForIncompatibleSitesEnabled](./microsoft-edge-policies.md#hideinternetexplorerredirectuxforincompatiblesitesenabled) – Zum Ausblenden des Dialogfelds für einmalige Umleitung und des Banners in MicrosoftEdge.
- [KioskAddressBarEditingEnabled](./microsoft-edge-policies.md#kioskaddressbareditingenabled) – Zum Konfigurieren der Adressleistenbearbeitung für Benutzerfreundlichkeit beim öffentlichen Surfen im Kioskmodus.
- [KioskDeleteDownloadsOnExit](./microsoft-edge-policies.md#kioskdeletedownloadsonexit) – Zum Löschen von während einer Kiosksitzung heruntergeladenen Dateien, wenn MicrosoftEdge geschlossen wird.
- [PasswordRevealEnabled](./microsoft-edge-policies.md#passwordrevealenabled) – Zum Aktivieren der Schaltfläche für Kennwortanzeige.
- [RedirectSitesFromInternetExplorerPreventBHOInstall](./microsoft-edge-policies.md#redirectsitesfrominternetexplorerpreventbhoinstall) – Zum Verhindern, dass das Browserhilfsobjekt (BHO) installiert wird, um inkompatible Websites von Internet Explorer zu MicrosoftEdge umzuleiten.
- [RedirectSitesFromInternetExplorerRedirectMode](./microsoft-edge-policies.md#redirectsitesfrominternetexplorerredirectmode) – Zum Umleiten inkompatibler Websites von Internet Explorer zu MicrosoftEdge.
- [SpeechRecognitionEnabled](./microsoft-edge-policies.md#speechrecognitionenabled) – Zum Konfigurieren der Spracherkennung.
- [WebCaptureEnabled](./microsoft-edge-policies.md#webcaptureenabled) – Zum Aktivieren des Features "Weberfassung" in MicrosoftEdge.

#### <a name="deprecated-policy"></a>Veraltete Richtlinie

[NewTabPageSetFeedType](./microsoft-edge-policies.md#newtabpagesetfeedtype) – Zum Konfigurieren der MicrosoftEdge-Oberfläche für neue Registerkartenseiten.

#### <a name="obsoleted-policy"></a>Veraltete Richtlinie

[EnableDeprecatedWebPlatformFeatures](./microsoft-edge-policies.md#enabledeprecatedwebplatformfeatures) – Zum Reaktivieren veralteter Features für Webplattformen für einen begrenzten Zeitraum.

<!-- end major 87 -->

## <a name="version-86062269-november-13"></a>Version 86.0.622.69: 13. November

> [!IMPORTANT]
> Dieses Update enthält [CVE-2020-16013](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-16013) und [CVE-2020-16017](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-16017), wovon laut Chromium-Team ein Exploit im Umlauf ist.

Stabile Kanalsicherheitsupdates sind [hier aufgeführt.](./microsoft-edge-relnotes-security.md#november-13-2020)

## <a name="version-86062268-november-11"></a>Version 86.0.622.68: 11.November

Sicherheitsupdates für stabile Kanäle sind hier [aufgeführt.](./microsoft-edge-relnotes-security.md#november-11-2020)

## <a name="version-86062263-november-4"></a>Version 86.0.622.63: 4.November

> [!IMPORTANT]
> Dieses Update enthält [CVE-2020-16009](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-16009), wovon laut Chromium-Team ein Exploit im Umlauf ist.

Stabile Kanalsicherheitsupdates sind [hier aufgeführt.](./microsoft-edge-relnotes-security.md#november-4-2020)

## <a name="version-86062261-november-2"></a>Version 86.0.622.61: 2. November

Verschiedene Bugs und Leistungsprobleme wurden behoben.

## <a name="version-86062258-october-29"></a>Version 86.0.622.58: 29.Oktober

Verschiedene Bugs und Leistungsprobleme wurden behoben.

## <a name="version-86062256-october-27"></a>Version 86.0.622.56: 27.Oktober

Verschiedene Bugs und Leistungsprobleme wurden behoben.

## <a name="version-86062251-october-22"></a>Version 86.0.622.51: 22.Oktober

Sicherheitsupdates für stabile Kanäle sind hier [aufgeführt.](./microsoft-edge-relnotes-security.md#october-22-2020)

## <a name="version-86062248-october-20"></a>Version 86.0.622.48: 20. Oktober

Verschiedene Bugs und Leistungsprobleme wurden behoben.

## <a name="version-86062243-october-15"></a>Version 86.0.622.43: 15. Oktober

Verschiedene Bugs und Leistungsprobleme wurden behoben.

<!-- Archive from 86.0.622.38-october-9 to beta 86.0.62.215-september-14  ->
<!-- Archived to version 84.0.522.40: July 16 -->

## <a name="see-also"></a>Weitere Informationen

- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)