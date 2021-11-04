---
title: Problembehandlung im IE-Modus und häufig gestellte Fragen (FAQ)
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 11/03/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Problembehandlung und häufig gestellte Fragen zum Microsoft Edge Internet Explorer-Modus
ms.openlocfilehash: 651fc438e64c21e33787724fb3d5931f0f5b75fa
ms.sourcegitcommit: 4ec03873a85f065d9bfa6203cfe6c3e938f79bc5
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2021
ms.locfileid: "12155145"
---
# <a name="internet-explorer-ie-mode-troubleshooting-and-faq"></a>Internet Explorer (IE)-Modus – Problembehandlung und häufig gestellte Fragen

> [!NOTE]
> Die Internet Explorer 11-Desktopanwendung wird eingestellt und wird am 15. Juni 2022 nicht mehr unterstützt. Eine Liste der Bereiche finden Sie in den häufig gestellten Fragen zur Einstellung von [Internet Explorer 11-Desktop-Apps.](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549) Dieselben IE11-Apps und -Websites, die Sie heute verwenden, können in Microsoft Edge im Internet Explorer-Modus geöffnet werden. Weitere Informationen finden Sie in Microsoft Edge Blogbeitrag zur [Zukunft von Internet Explorer auf Windows 10.](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/)

Dieser Artikel enthält Tipps zur Fehlerbehebung und häufig gestellte Fragen zu Microsoft Edge Version 77 oder höher.

> [!NOTE]
> Dieser Artikel bezieht sich auf Microsoft Edge Version 77 oder höher.

## <a name="troubleshoot-ie-mode"></a>Problembehandlung im IE-Modus

Verwenden Sie die Informationen in diesem Abschnitt, um Probleme mit dem IE-Modus zu diagnostizieren und zu beheben.

### <a name="internet-explorer-mode--general-diagnostic-information"></a>Allgemeine Diagnoseinformationen im Internet Explorer-Modus

Sie können Diagnoseinformationen für den Internet Explorer-Modus auf der Registerkarte zur Microsoft Edge-Kompatibilität abrufen. Wechseln Sie zu *edge://compat/iediagnostic*, um diese Registerkarte zu öffnen. Auf dieser Seite werden möglicherweise Diagnosemeldungen angezeigt. Auf dieser Seite finden Sie auch Konfigurationsinformationen zu den folgenden Kategorien:

- **Überprüfung des Registrierungsschlüssels:** (Wird nur angezeigt, wenn die Überprüfung fehlschlägt.) Überprüft, ob die Internet Explorer-Integration in der Registrierung ordnungsgemäß eingerichtet wurde. Wenn nicht, kann der Benutzer **"Beheben"** auswählen, um das Problem zu beheben.
- **Internet Explorer-Modus:** Zeigt die verwendete API-Version an, die auf der Konfiguration und dem Betriebssystem basiert. Wenn ein Problem vorliegt, wird der Benutzer möglicherweise aufgefordert, ein Windows Update zu installieren.
- **Einstellung für Internet Explorer-Modus:** Zeigt an, ob und wie der Internet Explorer-Modus konfiguriert ist.
- **Befehlszeile:** Zeigt die Befehlszeilenzeichenfolge und Switches an, die zum Starten Microsoft Edge verwendet werden.
- **Gruppenrichtlinieneinstellungen:** Zeigt an, ob der IE-Modus mithilfe von Gruppenrichtlinien und den angewendeten Richtlinien konfiguriert ist.

### <a name="error-message-to-open-this-page-in-internet-explorer-mode-reinstall-microsoft-edge-with-administrator-privileges"></a>Fehlermeldung: "Zum Öffnen dieser Seite im IE-Modus versuchen Sie, Microsoft Edge mit Administratorrechten neu zu installieren."

Dieser Fehler tritt möglicherweise auf, wenn Sie nicht über alle erforderlichen Windows Updates verfügen. Siehe die unter [Info zum IE-Modus](./edge-ie-mode.md) aufgeführten Voraussetzungen für die erforderlichen Versionen von Windows und Microsoft Edge.

Wenn Sie bereits alle erforderlichen Windows Updates installiert haben, wird möglicherweise dieser Fehler angezeigt, wenn:

- Sie verwenden den Canary Channel, der standardmäßig auf der Benutzerebene installiert wird.
- Sie verwenden den Stable-, Beta- oder Dev-Kanal, aber bei der Aufforderung zur Rechteerweiterung während der Installation wurde die Rechteerweiterung abgebrochen. Wenn Sie die Eingabeaufforderung für erhöhte Rechte abbrechen, wird die Installation auf Benutzerebene fortgesetzt.
- Internet Explorer 11 wurde in Windows-Features deaktiviert.

Mögliche Lösungen sind:

- Führen Sie das Installationsprogramm für einen beliebigen Kanal auf Systemebene aus: `installer.exe --system-level`
- Aktivieren Sie Internet Explorer 11 in Windows-Features.

Um zu überprüfen, ob Microsoft Edge auf Systemebene installiert ist, geben Sie "edge://version" in die Adressleiste von Microsoft Edge ein. Der Pfad für die ausführbare Datei beginnt mit *C:\Programmdateien* und weist auf eine Systeminstallation hin. Wenn der pfad der ausführbaren Datei mit *C:\Users*beginnt, deinstallieren Sie Microsoft Edge mit Administratorrechten, und installieren Sie ihn erneut.

### <a name="error-message-to-open-this-page-in-ie-mode-try-restarting-microsoft-edge"></a>Fehlermeldung "Versuchen Sie, Microsoft Edge neu zu starten, um diese Seite im IE-Modus zu öffnen."

Dieser Fehler wird möglicherweise angezeigt, wenn in Internet Explorer ein unerwarteter Fehler aufgetreten ist. Beim Neustart von Microsoft Edge wird dieser Fehler in der Regel behoben.

### <a name="error-message-turn-off-remote-debugging-to-open-this-site-in-ie-mode-otherwise-it-might-not-work-as-expected"></a>Fehlermeldung: "Deaktivieren Sie das Remotedebuggen, um diese Website im IE-Modus zu öffnen, da es sonst möglicherweise nicht wie erwartet funktioniert."

Dieser Fehler wird möglicherweise angezeigt, wenn Sie remote debuggen und zu einer Webseite navigieren, die für die Ausführung im IE-Modus konfiguriert ist. Sie können den Vorgang fortsetzen, aber die Seite wird mit Microsoft Edge gerendert.

### <a name="error-message-could-not-retrieve-emie-site-list"></a>Fehlermeldung: "EMIE-Websiteliste konnte nicht abgerufen werden."

Möglicherweise wird dieser Fehler auf der *edge://compat/enterprise* Seite angezeigt, der angibt, dass der Download der Websiteliste fehlgeschlagen ist. Ab Microsoft Edge Version 87 ist die HTTP-Authentifizierung ebenfalls nicht zulässig, wenn Cookies mithilfe der [BlockThirdPartyCookies](/deployedge/microsoft-edge-policies#blockthirdpartycookies)-Richtlinie für Anforderungen von Drittanbietern blockiert werden. Sie können Cookies für die bestimmte Domain zulassen, in der sich Ihre Site-Liste im Unternehmensmodus befindet, indem Sie die [CookiesAllowedForURLs](/deployedge/microsoft-edge-policies#cookiesallowedforurls)-Richtlinie verwenden, um sicherzustellen, dass das Herunterladen der Site-Liste erfolgreich ist.

## <a name="frequently-asked-questions"></a>Häufig gestellte Fragen

### <a name="will-ie-mode-replace-internet-explorer-11"></a>Wird der IE-Modus Internet Explorer 11 ersetzen?

Ja, die Internet Explorer 11-Desktopanwendung wird eingestellt und wird am 15. Juni 2022 nicht mehr unterstützt. Informationen zum Umfang finden Sie unter ["Häufig gestellte Fragen zum Lebenszyklus" – Internet Explorer.](/lifecycle/faq/internet-explorer-microsoft-edge) Dieselben IE11-Apps und -Websites, die Sie heute verwenden, können in Microsoft Edge im Internet Explorer-Modus geöffnet werden. Weitere Informationen finden Sie [unter "Die Zukunft von Internet Explorer auf Windows 10 befindet sich in Microsoft Edge.](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/)

### <a name="how-can-i-debug-my-legacy-application-while-using-ie-mode-on-microsoft-edge"></a>Wie kann ich meine Legacyanwendung debuggen, während ich den IE-Modus auf Microsoft Edge verwende?

Sie können IEChooser verwenden, um die Internet Explorer DevTools zu starten, um den Inhalt Ihrer IE-Modus-Registerkarten zu debuggen. Gehen Sie folgendermaßen vor, um IEChooser zu verwenden:

1. Öffnen Sie IEChooser.
   - Öffnen des Dialogfelds Ausführen Drücken Sie z. B. die `Windows logo key`  +  `R` .
   - Geben Sie `%systemroot%\system32\f12\IEChooser.exe` ein, und wählen Sie dann **OK**aus.
2. Wählen Sie in IEChooser den Eintrag für die Registerkarte "IE-Modus" aus.

### <a name="can-i-test-a-site-in-microsoft-edge-while-it-is-configured-to-open-ie-mode-in-the-enterprise-mode-site-list"></a>Kann ich eine Website in Microsoft Edge testen, während sie so konfiguriert ist, dass der IE-Modus in der Websiteliste für den Enterprise modus geöffnet wird?

Ja, während Sie Ihre älteren Websites modernisieren, können Sie im IE-Modus konfigurierte Anwendungen auf Microsoft Edge testen. Dazu können Sie Microsoft Edge mit dem `--ie-mode-test` Befehlszeilen-Flag ausführen. Stellen Sie sicher, dass keine anderen Microsoft Edge Instanzen ausgeführt werden. Anschließend können Sie **Einstellungen und mehr** auswählen (das Ellipsensymbol ...) **> Weitere Tools > Öffnen von Websites im Edgemodus.**

### <a name="can-i-use-view-in-file-explorer-in-sharepoint-online-on-microsoft-edge"></a>Kann ich "Im Datei-Explorer anzeigen" in SharePoint Online auf Microsoft Edge verwenden?

Ab Microsoft Edge Version 95 können Sie die Funktion **"Im Datei-Explorer anzeigen"** für SharePoint modernen Onlinedokumentbibliotheken aktivieren. Damit diese Erfahrung für Ihre Benutzer sichtbar und funktionsfähig ist, müssen Sie die richtlinie [Microsoft Edge "Konfigurieren der Ansicht im Datei-Explorer-Feature für SharePoint Seiten in Microsoft Edge"](/deployedge/microsoft-edge-policies#configureviewinfileexplorer) aktivieren und Ihre SharePoint Onlinemandantenkonfiguration aktualisieren. Weitere Informationen: [Anzeigen SharePoint Dateien mit dem Datei-Explorer in Microsoft Edge – SharePoint in Microsoft 365 | Microsoft Docs](/SharePoint/sharepoint-view-in-edge).

Anstatt jedoch die Option "Im Datei-Explorer anzeigen" zu verwenden, empfiehlt es sich, Dateien und Ordner außerhalb von SharePoint zu verwalten, die [Synchronisierung SharePoint und das Teams von Dateien mit Ihrem Computer](https://support.microsoft.com/office/sync-sharepoint-and-teams-files-with-your-computer-6de9ede8-5b6e-4503-80b2-6190f3354a88?ui=en-us&rs=en-us&ad=us) oder das Verschieben oder Kopieren von Dateien in [SharePoint.](https://support.microsoft.com/office/move-or-copy-files-in-sharepoint-00e2f483-4df3-46be-a861-1f5f0c1a87bc?ui=en-us&rs=en-us&ad=us)

### <a name="does-ie-mode-on-microsoft-edge-support-the-no-merge-option-that-was-supported-in-internet-explorer-11"></a>Unterstützt der IE-Modus auf Microsoft Edge die Option "Nicht zusammenführen", die in Internet Explorer 11 unterstützt wurde?

Die empfohlenen Alternativen für die No-Merge-Funktionalität in Microsoft Edge sind eine der folgenden Aktionen:

1. Verwenden Von Profilen in Microsoft Edge : Jedes Profil ist einer anderen IE-Sitzung für IE-Modusseiten zugeordnet, sodass es sich identisch mit der Option zum Zusammenführen verhält.
2. Verwenden Sie die Befehlszeile `--user-data-dir=<path>`, aber für jede Sitzung mit einem anderen Pfad. Bei Bedarf können Sie ein Hilfsprogramm für den Benutzer erstellen, mit dem Microsoft Edge gestartet und der Pfad für die Sitzung geändert wird.

Wenn keine der vorherigen Optionen für Ihr Szenario funktioniert, unterstützt der IE-Modus ab Microsoft Edge Version 93 für Microsoft Edge keine Zusammenführung. Wenn ein neues Browserfenster von einer IE-Modusanwendung gestartet wird, befindet sich ein Endbenutzer in einer separaten Sitzung, wie z. B. das No-Merge-Verhalten in IE11.

Bei jedem Microsoft Edge Fenster wird beim ersten Aufrufen einer IE-Modus-Registerkarte in diesem Fenster, wenn es sich um eine bestimmte "No-Merge"-Website handelt, dieses Fenster in einer anderen IE-Sitzung ohne Zusammenführung gesperrt.  Dieses Fenster bleibt von allen anderen Microsoft Edge Fenstern gesperrt, bis die letzte Registerkarte für den IE-Modus im gesperrten Fenster geschlossen wird. Dies folgt dem vorherigen Verhalten, bei dem Benutzer IE ohne Zusammenführung starten und Microsoft Edge ohne Zusammenführung mit anderen Mechanismen starten konnten. Alle Websites, die in einem neuen Fenster (über window.open) geöffnet werden, berücksichtigen die Zusammenführungsart des übergeordneten Prozesses.

> [!NOTE]
> Das Wechseln der Sitzung wird nicht unterstützt. Navigationen auf derselben Registerkarte im IE-Modus verwenden dieselbe Sitzung.

Sie können das No-Merge-Verhalten in Microsoft Edge Version 93 oder höher überprüfen, indem Sie die folgenden Schritte ausführen:

1. Stellen Sie sicher, dass der IE-Modus in Microsoft Edge Version 93 oder höher aktiviert ist.
2. Sie können Websites konfigurieren, die die Sitzungsfreigabe in der Enterprise Mode Site List verhindern müssen, indem Sie den Wert des Seriendruck-Attributs auf "no-merge" festlegen. Dieses Attribut gilt nicht nur, wenn das Open-In-Element auf Microsoft Edge festgelegt ist. Standardmäßig weisen alle Websites einen Seriendrucktypwert auf. (**Hinweis:** Das integrierte Websitelisten-Manager-Tool, das unter *edge://compat/sitelistmanager* verfügbar ist, enthält beim Hinzufügen oder Bearbeiten einer Website das Kontrollkästchen **"Kein Zusammenführen".)**

   ```
   <site url="contoso.com">
   <open-in merge-type="no-merge">IE11</open-in>
   </site>
   ```

3. Navigieren Sie zu einer beliebigen Website, die als Seriendruck konfiguriert ist. Die Website sollte sich in einer eigenen nicht zusammengeführten IE-Sitzung befinden. Wenn Sie eine andere Microsoft Edge Instanz oder ein anderes Fenster öffnen und zur gleichen Website navigieren, sollte sich diese in einer eigenen IE-Sitzung befinden. Beachten Sie, dass es sich um mehrere iexplore.exe Prozesse im Task-Manager handelt.

Wenn Sie Feedback haben, wenden Sie sich über einen unserer Feedbackkanäle: Microsoft-Support oder das [TechCommunity-Forum.](https://techcommunity.microsoft.com/t5/enterprise/bd-p/EdgeInsiderEnterprise)

### <a name="can-i-save-links-as-webpages-in-internet-explorer-mode"></a>Kann ich Links im Internet Explorer-Modus als Webseiten speichern?

Ja, Sie können die Option „Ziel speichern unter“ im Kontextmenü für den Internet Explorer-Modus in Microsoft Edge aktivieren. Konfigurieren Sie dazu die Gruppenrichtlinie *"Ziel speichern im Internet Explorer-Modus zulassen"* unter *Computerkonfiguration > Administrative Vorlagen > Windows Komponenten > Internet Explorer.* Der Speichermechanismus funktioniert gleich wie in Internet Explorer, und wenn das Ziel als HTML-Datei gespeichert wird, rendert die Datei beim erneuten Öffnen die Seite in Microsoft Edge.

Die Möglichkeit, Links als Webseiten zu speichern, erfordert die folgenden Mindestaktualisierungen des Betriebssystems:

- Windows 10, Version 2004, Windows Server, Version 2004, Windows 10, Version 20H2: [KB4580364](https://support.microsoft.com/help/4580364/windows-10-update-kb4580364)
- Windows 10 Version 1903, Windows 10, Version 1909, Windows Server, Version 1903 ([KB4580386](https://support.microsoft.com/help/4580386/windows-10-update-kb4580386))
- Windows 10 Version 1809, Windows Server Version 1809, Windows Server 2019 ([KB4580390](https://support.microsoft.com/help/4580390/windows-10-update-kb4580390))
- Windows 10, Version 1803: [KB4586785](https://support.microsoft.com/help/4586785/windows-10-update-kb4586785)
- Windows 10, Version 1607: [KB4586830](https://support.microsoft.com/help/4586830/windows-10-update-kb4586830)
- Windows 10, Version 1507: [KB4586787](https://support.microsoft.com/help/4586787/windows-10-update-kb4586787)

### <a name="can-i-test-a-site-in-microsoft-edge-while-it-is-configured-to-open-ie-mode-in-the-enterprise-mode-site-list"></a>Kann ich eine Website in Microsoft Edge testen, während sie so konfiguriert ist, dass der IE-Modus in der Websiteliste für den Enterprise modus geöffnet wird?

Ja, während Sie Ihre älteren Websites modernisieren, können Sie Websites im IE-Modus auf Microsoft Edge testen. Dazu können Sie Microsoft Edge mit der `--ie-mode-test` Befehlszeilenkennzeichnung ausführen. Stellen Sie sicher, dass keine anderen Microsoft Edge Instanzen ausgeführt werden. Wählen Sie dann **Einstellungen und mehr** aus (das Ellipsensymbol) ... **> Weitere Tools > Öffnen von Websites im Edgemodus.**

### <a name="my-application-requires-transferring-post-data-between-ie-mode-and-microsoft-edge-is-this-supported"></a>Meine Anwendung erfordert die Übertragung von POST-Daten zwischen dem IE-Modus und Microsoft Edge. Wird dies unterstützt?

Ab Microsoft Edge Beta Channel Version 96 enthalten Navigationen, die zwischen Internet Explorer-Modus und Microsoft Edge wechseln, Formulardaten und zusätzliche HTTP-Header. Wenn Formulardaten jedoch Dateianlagen enthalten, werden sie nicht zwischen Modulen übertragen. Mithilfe der [Gruppenrichtlinie "InternetExplorerIntegrationComplexNavDataTypes"](/deployedge/microsoft-edge-policies#internetexplorerintegrationcomplexnavdatatypes) können Sie auswählen, welche Datentypen in solche Navigationen eingeschlossen werden sollen.

Zusätzlich zu Microsoft Edge Version 96 müssen Für diese Erfahrung die folgenden Windows Updates installiert sein:

- Windows 10 Version 2004; Windows Serverversion 2004; Windows 10 Version; Windows Serverversion 20H2 und Windows 10 Version 21H1 – KB5006738 oder höher

  > [!NOTE]
  > Updates für Windows 10 Version 19H2, Windows Server 2022 und Windows 11 werden in Kürze verfügbar sein.

## <a name="see-also"></a>Weitere Informationen
  
- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)
- [Informationen zum IE-Modus](./edge-ie-mode.md)
- [Weitere Informationen zum Unternehmensmodus](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
