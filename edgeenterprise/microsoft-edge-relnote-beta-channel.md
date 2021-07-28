---
title: Anmerkungen zu dieser Version von Microsoft Edge für Beta-Kanal
ms.author: aguta
author: AndreaLBarr
manager: srugh
ms.date: 07/21/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Anmerkungen zu dieser Version von Microsoft Edge für Beta-Kanal
ms.openlocfilehash: 4bedc609fd150b77b72590f0e16c97f6fb74ed7e
ms.sourcegitcommit: 9088e839e82d80c72460586e9af0610c6ca71b83
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/23/2021
ms.locfileid: "11675952"
---
# <a name="release-notes-for-microsoft-edge-beta-channel"></a>Versionshinweise für Microsoft Edge Beta-Kanal

Diese Versionshinweise enthalten Informationen zu neuen Funktionen und nicht sicherheitsrelevanten Updates, die im Microsoft Edge Beta-Kanal enthalten sind. Archivierte Versionen dieser Versionshinweise sind [hier](microsoft-edge-relnote-archive-beta-channel.md) verfügbar.

> [!NOTE]
> Die Microsoft Edge-Webplattform entwickelt sich ständig weiter, um Benutzerfreundlichkeit, Sicherheit und Datenschutz zu verbessern. Weitere Informationen finden Sie unter [Änderungen mit Auswirkungen auf die Websitekompatibilität, die für Microsoft Edge anstehen](/microsoft-edge/web-platform/site-impacting-changes).

## <a name="version-92090255-july-21"></a>Version 92.0.902.55: 21. Juli

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-92090245-july-12"></a>Version 92.0.902.45: 12. Juli

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-92090240-july-6"></a>Version 92.0.902.40: 6. Juli

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-92090222-june-21"></a>Version 92.0.902.22: 21. Juni

### <a name="feature-updates"></a>Funktionsupdates

- **Suche in natürlicher Sprache nach Browserverlauf in der Adressleiste.** Die Suche nach dem gesuchten Artikel/der Website ist jetzt dank der Suche in natürlicher Sprache direkt über die Adressleiste einfacher. Sie finden Suchergebnisse basierend auf Seiteninhalt/Beschreibung/Timing (z. B. "Rezept aus der letzten Woche") zusätzlich zu Titeln/URL-Schlüsselwortübereinstimmungen allein.
Bitte beachten Sie: Dies ist ein kontrolliertes Featurerollout. Wenn dieses Feature nicht angezeigt wird, schauen Sie bitte in Kürze wieder vorbei, da wir mit dem Rollout fortfahren.

- **Benutzer können auf Internet Explorer-Modus auf Microsoft Edge problemlos wechseln**. Ab Microsoft Edge Version 92 können Benutzer eine Website im Internet Explorer-Modus auf Microsoft Edge neu laden, anstatt sich auf die eigenständige IE 11-Anwendung zu verlassen, während sie auf die Konfiguration einer Website in der Websiteliste für den Enterprise-Modus warten. Benutzer werden aufgefordert, die Website ihrer lokalen Websiteliste hinzuzufügen, sodass die Navigation zu derselben Seite in Microsoft Edge für die nächsten 30 Tage automatisch im IE-Modus gerendert wird. Mit der *[InternetExplorerIntegrationReloadInIEModeAllowed](/deployedge/microsoft-edge-policies#internetexplorerintegrationreloadiniemodeallowed)*-Richtlinie können Sie diese Umgebung konfigurieren und den Zugriff auf die Einstiegspunkte des IE-Modus sowie die Möglichkeit zum Hinzufügen von Websites zur lokalen Websiteliste zulassen. Mit der *[InternetExplorerIntegrationLocalSiteListExpirationDays](/deployedge/microsoft-edge-policies#internetexplorerintegrationlocalsitelistexpirationdays)*-Richtlinie können Sie die Anzahl der Tage anpassen, um Websites in der lokalen Websiteliste zu speichern.
Beachten Sie, dass KB5003698 oder höher für Windows 10, Version 1909, erforderlich ist; oder KB5003690 oder höher für Windows 10, Version 2004, Windows 10, Version 20H2 oder Windows 10, Version 21H1, für die End-to-End-Erfahrung erforderlich ist.

- **MHTML-Dateien werden standardmäßig im Internet Explorer-Modus geöffnet**. Ab Microsoft Edge Version 92 Stable werden MHTML-Dateitypen automatisch im Internet Explorer-Modus auf Microsoft Edge anstelle der Internet Explorer-Anwendung (IE11) geöffnet. Dies wird am häufigsten beim Versuch beobachtet, Outlook-E-Mails in einem Browser anzuzeigen. Diese Änderung tritt nur auf, wenn IE11 der Standardhandler für diesen Dateityp ist. Wenn Sie dies lieber ändern möchten, können Sie dies vor der Installation des Stable Version 92-Updates mithilfe [dieser Anleitung](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration) tun.

- **Zahlungsinstrumente werden jetzt geräteübergreifend synchronisiert**. Ab Microsoft Edge Version 92 haben Sie die Möglichkeit, Ihre Zahlungsinformationen auf ihren angemeldeten Geräten zu synchronisieren.
Bitte beachten Sie: Dies ist ein kontrolliertes Featurerollout. Wenn dieses Feature nicht angezeigt wird, schauen Sie bitte in Kürze wieder vorbei, da wir mit dem Rollout fortfahren.

- **Die Warnung "Entwicklermoduserweiterungen deaktivieren" kann dauerhaft verworfen werden**. Ab Microsoft Edge, Version 92, können Sie die Warnung "Entwicklermoduserweiterungen deaktivieren" deaktivieren, indem Sie auf die Option "Diese Option nicht erneut anzeigen" klicken.
Bitte beachten Sie: Dies ist ein kontrolliertes Featurerollout. Wenn dieses Feature nicht angezeigt wird, schauen Sie bitte in Kürze wieder vorbei, da wir mit dem Rollout fortfahren.

- **Verwalten Sie Ihre Erweiterungen direkt über die Symbolleiste**. Mit dem Menü "Ganz neue Erweiterungen" auf der Symbolleiste können Sie Erweiterungen einfach ausblenden/anheften. Die Quicklinks zum Verwalten von Erweiterungen und zum Suchen neuer Erweiterungen erleichtern Ihnen das Auffinden neuer Erweiterungen und das Verwalten Ihrer vorhandenen Erweiterungen.
Bitte beachten Sie: Dies ist ein kontrolliertes Featurerollout. Wenn dieses Feature nicht angezeigt wird, schauen Sie bitte in Kürze wieder vorbei, da wir mit dem Rollout fortfahren.

- **Automatisches HTTPS**. Benutzer haben die Möglichkeit, die Navigation von HTTP auf HTTPS in Domänen zu aktualisieren, die wahrscheinlich dieses sicherere Protokoll unterstützen. Diese Unterstützung kann auch so konfiguriert werden, dass die Übermittlung über HTTPS für alle Domänen versucht wird.
Bitte beachten Sie: Wir experimentieren mit diesem Feature, und dieses Verhalten wird nicht angezeigt, wenn Sie sich von Experimenten abgemeldet haben.

- **Verbesserungen beim Rendern von Schriftarten**. Das Rendering von Text wurde verbessert, um die Übersichtlichkeit zu verbessern und die Unschärfe zu verringern.
Bitte beachten Sie: Dies ist ein kontrolliertes Featurerollout. Wenn dieses Feature nicht angezeigt wird, schauen Sie bitte in Kürze wieder vorbei, da wir mit dem Rollout fortfahren.

### <a name="policy-updates"></a>Richtlinienupdates

#### <a name="new-policies"></a>Neue Richtlinien

Acht neue Richtlinien wurden hinzugefügt. Laden Sie die aktualisierten administrativen Vorlagen von der [Microsoft Edge Enterprise-Angebotsseite](https://www.microsoft.com/edge/business/download) herunter. Die folgenden neuen Richtlinien wurden hinzugefügt:

- [AADWebSiteSSOUsingThisProfileEnabled](/DeployEdge/microsoft-edge-policies#aadwebsitessousingthisprofileenabled): Einmaliges Anmelden für geschäftliche oder Schulwebsites, auf denen dieses Profil aktiviert ist.
- [AutomaticHttpsDefault](/DeployEdge/microsoft-edge-policies#automatichttpsdefault): Automatisches HTTPS konfigurieren
- [HeadlessModeEnabled](/DeployEdge/microsoft-edge-policies#headlessmodeenabled): Steuern der Verwendung des Headless-Modus
- [InsecurePrivateNetworkRequestsAllowed](/DeployEdge/microsoft-edge-policies#insecureprivatenetworkrequestsallowed): Gibt an, ob unsichere Websites Anforderungen an privatere Netzwerkendpunkte stellen dürfen
- [InsecurePrivateNetworkRequestsAllowedForUrls](/DeployEdge/microsoft-edge-policies#insecureprivatenetworkrequestsallowedforurls): Zulassen, dass die aufgeführten Websites Anforderungen an privatere Netzwerkendpunkte aus unsicheren Kontexten stellen
- [InternetExplorerIntegrationLocalSiteListExpirationDays](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationlocalsitelistexpirationdays): Angeben der Anzahl der Tage, die eine Website in der lokalen Websiteliste für den IE-Modus verbleibt
- [InternetExplorerIntegrationReloadInIEModeAllowed](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationreloadiniemodeallowed): Zulassen, dass nicht konfigurierte Websites im Internet Explorer-Modus neu geladen werden
- [SharedArrayBufferUnrestrictedAccessAllowed](/DeployEdge/microsoft-edge-policies#sharedarraybufferunrestrictedaccessallowed): Gibt an, ob SharedArrayBuffers in einem nicht ursprungsübergreifenden isolierten Kontext verwendet werden können

#### <a name="obsoleted-policy"></a>Veraltete Richtlinie

- [EnableSha1ForLocalAnchors](/DeployEdge/microsoft-edge-policies#enablesha1forlocalanchors): Zulassen von Zertifikaten, die mit SHA-1 signiert wurden, wenn sie von lokalen Vertrauensankern ausgegeben wurden.

## <a name="version-9209029-june-8"></a>Version 92.0.902.9: 8. Juni

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-91086441-june-3"></a>Version 91.0.864.41: 3. Juni

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-91086437-may-27"></a>Version 91.0.864.37: 27. Mai

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-91086436-may-26"></a>Version 91.0.864.36: 26. Mai

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-91086433-may-21"></a>Version 91.0.864.33: 21. Mai

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-91086427-may-14"></a>Version 91.0.864.27: 14. Mai

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-91086419-may-7"></a>Version 91.0.864.19: 7. Mai

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-91086415-may-3"></a>Version 91.0.864.15: 3. Mai

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-91086411-april-30"></a>Version 91.0.864.11: 30. April

### <a name="feature-updates"></a>Funktionsupdates

- **Identifizieren Sie den Netzwerkdatenverkehr von Microsoft Defender Application Guard-Containern auf Proxyebene**. Ab Microsoft Edge Version 91 gibt es integrierte Unterstützung zum Markieren von Netzwerkdatenverkehr von Application Guard-Containern, sodass Unternehmen diese identifizieren und bestimmte Richtlinien anwenden können.

- **Unterstützungsoption, um die Synchronisierung von Favoriten vom Host mit dem Microsoft Edge Application Guard-Container zuzulassen**. Ab Microsoft Edge Version 91 haben Benutzer die Möglichkeit, Application Guard so zu konfigurieren, dass ihre Favoriten vom Host mit dem Container synchronisiert werden. Dadurch wird sichergestellt, dass auch neue Favoriten im Container angezeigt werden.

- **Unterstützung für Spracherkennungs-APIs**. Ab Microsoft Edge Version 91 wird die API-Unterstützung für Spracherkennungsbefehle auf Google.com und ähnlichen Websites hinzugefügt. Diese Funktion ist auf eine zufällig ausgewählte Gruppe von Benutzern beschränkt, die das Experimentieren aktiviert haben. Diese Benutzer geben dem Feature-Team Feedback.

- **Personalisieren Sie Ihren Browser mit neuen Designfarben.**. Personalisieren Sie Ihr Microsoft Edge mit einer der 14 neuen Designfarben auf der Seite „Einstellungen“ > „Darstellung“. Sie können auch benutzerdefinierte Designs von der Microsoft Edge-Add-On-Website installieren. [Weitere Informationen](https://techcommunity.microsoft.com/t5/articles/make-microsoft-edge-your-own-with-themes/m-p/2083165)

- **Downloads unterbrechen** Ab Microsoft Edge Version 91 wird der Download von Typen, die Ihrem Computer schaden könnten, vom Browser automatisch unterbrochen, wenn diese Downloads ohne Benutzerinteraktion gestartet werden und von der SmartScreen-Anwendungszuverlässigkeitsüberprüfung nicht unterstützt werden. Benutzer können den Download überschreiben und fortsetzen, indem sie mit der rechten Maustaste auf das Downloadelement klicken und „Beibehalten“ auswählen.
Unternehmensadministratoren können dieses Verhalten mit einer der folgenden beiden Richtlinien deaktivieren:
    - [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](/deployedge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings): Deaktivieren von auf Dateierweiterungen basierenden Download-Warnungen für bestimmte Dateitypen in Domänen. Weitere Informationen finden Sie unter [Unterbrechung von Microsoft Edge-Sicherheitsdownloads](/deployedge/microsoft-edge-security-downloads-interruptions)

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

## <a name="version-90081846-april-22"></a>Version 90.0.818.46: 22. April

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-90081842-april-20"></a>Version 90.0.818.42: 20. April

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-90081841-april-16"></a>Version 90.0.818.41: 16. April

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-90081838-april-14"></a>Version 90.0.818.38: 14. April

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-90081836-april-12"></a>Version 90.0.818.36: 12. April

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-90081827-april-2"></a>Version 90.0.818.27 vom 2. April

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-90081822-march-29"></a>Version 90.0.818.22 vom 29. März

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-90081814-march-22"></a>Version 90.0.818.14: 22. März

Verschiedene Fehler und Leistungsprobleme wurden behoben.
<!-- begin major 90 -->
## <a name="version-9008188-march-16"></a>Version 90.0.818.8: 16. März

### <a name="feature-updates"></a>Funktionsupdates

- **Einmaliges Anmelden (Single Sign On, SSO) ist jetzt für Azure Active Directory (Azure AD)-Konten und Microsoft-Konten (MSA) unter macOS verfügbar.** Ein bei Microsoft Edge unter macOS angemeldeter Benutzer wird nun automatisch bei Websites angemeldet, die so konfiguriert sind, dass eine einmalige Anmeldung mit Arbeits- und Microsoft-Konten möglich ist (z. B. bing.com, office.com, msn.com und outlook.com).

- **Kioskmodus.** Ab Microsoft Edge Version 90 wurden die Druckeinstellungen der Benutzeroberfläche gesperrt, und es werden nur noch die konfigurierten Drucker und „In PDF drucken“-Optionen zugelassen. Wir haben außerdem Verbesserungen am Kioskmodus für den zugewiesenen Zugriff für nur eine App vorgenommen, um das Starten anderer Anwendungen über den Browser einzuschränken. Weitere Informationen zu den Features des Kioskmodus finden Sie [hier](/deployedge/microsoft-edge-configure-kiosk-mode#kiosk-mode-supported-features).

- **Drucken:**

  - **Neuer Druckrasterungsmodus für Nicht-PostScript-Drucker**. Ab Microsoft Edge Version 90 können Administratoren mithilfe einer neuen Richtlinie den Druckrasterungsmodus für ihre Benutzer definieren. Diese Richtlinie steuert, wie Microsoft Edge unter Windows auf Nicht-PostScript-Druckern druckt.  Manchmal müssen Druckaufträge bei Nicht-PostScript-Druckern gerastert werden, damit korrekt gedruckt wird. Die Druckoptionen sind „Full" (Vollständig) und „Fast“ (Schnell).

  - **Zusätzliche Optionen für die Seitenskalierung beim Drucken**. Benutzer können jetzt die Skalierung anpassen, während sie Webseiten und PDF-Dokumente mit zusätzlichen Optionen drucken. Die Option „An Seite anpassen" stellt sicher, dass die Webseite oder das Dokument in den Bereich passt, der im ausgewählten „Papierformat" zum Drucken verfügbar ist. Die Option "Tatsächliche Größe" stellt sicher, dass sich die Größe des zu druckenden Inhalts unabhängig von der ausgewählten "Papiergröße" nicht ändert.

- **Produktivität:**

  - **Vorschläge zum automatischen Ausfüllen werden um den Inhalt von Adressfeldern aus der Zwischenablage erweitert.** Der Inhalt der Zwischenablage wird analysiert, wenn Sie auf ein Profil-/Adressfeld (z. B. Telefon, E-Mail, Postleitzahl, Stadt, Bundesland usw.) klicken, um es als Vorschläge zum automatischen Ausfüllen anzuzeigen.

  - **Benutzer können nach Vorschlägen zum automatischen Ausfüllen suchen, auch wenn ein Formular oder Feld nicht erkannt wird**. Wenn Sie Ihre Informationen heute in Microsoft Edge gespeichert haben, werden automatisch Vorschläge zum automatischen Ausfüllen angezeigt, mit denen Sie beim Ausfüllen von Formularen Zeit sparen können. In Fällen, in denen beim automatischen Ausfüllen ein Formular fehlt oder wenn Sie Daten in Formularen abrufen möchten, die normalerweise nicht automatisch ausgefüllt sind (z. B. temporäre Formulare), können Sie mithilfe des automatischen Ausfüllens nach Ihren Informationen suchen.

- **Greifen Sie über ein Flyout in der Menüleiste auf Downloads zu**. Downloads werden in der oberen rechten Ecke mit allen aktiven Downloads an einem Ort angezeigt. Dieses Menü ist leicht zu schließen, sodass Benutzer ununterbrochen weiter surfen und den gesamten Download-Fortschritt direkt über die Symbolleiste überwachen können. [Weitere Informationen](https://techcommunity.microsoft.com/t5/articles/introducing-the-new-downloads-experience/m-p/2111551).


### <a name="policy-updates"></a>Richtlinienupdates

#### <a name="new-policies"></a>Neue Richtlinien

Es wurden sieben neue Richtlinien hinzugefügt. Laden Sie die aktualisierten administrativen Vorlagen von der [Microsoft Edge Enterprise-Angebotsseite](https://www.microsoft.com/edge/business/download) herunter. Die folgenden neuen Richtlinien wurden hinzugefügt:

- [ApplicationGuardFavoritesSyncEnabled](./microsoft-edge-policies.md#applicationguardfavoritessyncenabled) – Synchronisierung von Application Guard-Favoriten aktiviert
- [ManagedConfigurationPerOrigin](./microsoft-edge-policies.md#managedconfigurationperorigin) – Legt verwaltete Konfigurationswerte für Websites auf bestimmte Ursprünge fest
- [PrintRasterizationMode](./microsoft-edge-policies.md#printrasterizationmode) – Druckrasterungsmodus
- [QuickViewOfficeFilesEnabled](./microsoft-edge-policies.md#quickviewofficefilesenabled) : Verwalten der QuickView Office-Dateifunktion in Microsoft Edge
- [SSLErrorOverrideAllowedForOrigins](./microsoft-edge-policies.md#sslerroroverrideallowedfororigins) – Benutzer können von der HTTPS-Warnseite für bestimmte Ursprünge fortfahren
- [WindowOcclusionEnabled](./microsoft-edge-policies.md#windowocclusionenabled) – Fester-Okklusion aktivieren
- [WindowsHelloForHTTPAuthEnabled](./microsoft-edge-policies.md#windowshelloforhttpauthenabled) – Windows Hello für HTTP-Authentifizierung aktiviert

#### <a name="deprecated-policies"></a>Veraltete Richtlinien

- [NativeWindowOcclusionEnabled](./microsoft-edge-policies.md#nativewindowocclusionenabled) – Native Fenster-Okklusion aktivieren
- [SSLVersionMin](./microsoft-edge-policies.md#sslversionmin)– Mindestens aktivierte TLS-Version
<!-- end major 90 -->

## <a name="version-89077454-march-13"></a>Version 89.0.774.54: 13. März

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-89077450-march-10"></a>Version 89.0.774.50: 10. März

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-89077448-march-8"></a>Version 89.0.774.48: 8. März

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-89077445-march-3"></a>Version 89.0.774.45: 3. März

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-89077439-february-26"></a>Version 89.0.774.39: 26. Februar

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-89077434-february-22"></a>Version 89.0.774.34: 22. Februar

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-89077427-february-12"></a>Version 89.0.774.27: 12. Februar

Verschiedene Fehler und Leistungsprobleme wurden behoben.

## <a name="version-89077423-february-8"></a>Version 89.0.774.23: 8. Februar

Verschiedene Fehler und Leistungsprobleme wurden behoben.

<!-- begin major 89 -->

<!--- Archived from Version 87.0.664.18: October 26 to to version 89.0.774.18: February 3 ---->
<!--- Archived from Version 87.0.664.12: October 20 to to version 86.0.622.15: September 14 ---->
<!--- Archived to version 86.0.622.11: September 9 ---->
<!--- Archived to version 85.0.564.18: July 28 ---->

## <a name="see-also"></a>Weitere Informationen

- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)
