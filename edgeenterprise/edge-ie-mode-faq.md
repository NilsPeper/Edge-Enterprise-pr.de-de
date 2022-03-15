---
title: Internet Explorer (IE)-Modus – Problembehandlung und häufig gestellte Fragen
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 01/18/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Anleitung zur Problembehandlung und häufig gestellte Fragen für Microsoft Edge Internet Explorer-Modus
ms.openlocfilehash: 064174744dbdc8d16912e4c196a8974c243de732
ms.sourcegitcommit: 556aca8dde42dd66364427f095e8e473b86651a0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2022
ms.locfileid: "12445679"
---
# <a name="internet-explorer-ie-mode-troubleshooting-and-faq"></a>Internet Explorer (IE)-Modus – Problembehandlung und häufig gestellte Fragen

> [!NOTE]
> Die Internet Explorer 11-Desktopanwendung wird eingestellt und wird am 15. Juni 2022 nicht mehr unterstützt. Informationen zur Liste der Bereiche finden Sie in den [häufig gestellten Fragen zur Einstellung von Internet Explorer 11-Desktop-Apps](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549). Dieselben IE11-Apps und -Websites, die Sie heute verwenden, können in Microsoft Edge im Internet Explorer-Modus geöffnet werden. Weitere Informationen zur [Zukunft von Internet Explorer auf Windows 10 finden Sie in Microsoft Edge](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/) Blogbeitrag.

Dieser Artikel enthält Tipps und häufig gestellte Fragen zur Problembehandlung für Microsoft Edge Version 77 oder höher.

> [!NOTE]
> Dieser Artikel bezieht sich auf Microsoft Edge Version 77 oder neuer.

## <a name="what-if-i-need-help-with-setting-up-microsoft-edge-or-internet-explorer-mode"></a>Was geschieht, wenn ich Hilfe beim Einrichten des Microsoft Edge- oder Internet Explorer-Modus benötiere?

Wir bieten verschiedene Supportoptionen. Wenn Sie Microsoft Unified Support haben, können Sie sich an diesen Supportdienst wenden, um Hilfe beim Übergang zu erhalten. Es gibt auch  [FastTrack](https://www.microsoft.com/en-us/fasttrack/microsoft-365/microsoft-edge?rtc=1), die für Kunden mit mindestens 150 kostenpflichtigen Windows 10 kostenlos zur Verfügung stehen.

Wir empfehlen auch unsere Microsoft Edge + Erste [Schritte](https://query.prod.cms.rt.microsoft.com/cms/api/am/binary/RWEHMs) im Internet Explorer-Modus und unsere [Blogreihe für den IE-Modus](https://techcommunity.microsoft.com/t5/windows-10/internet-explorer-to-microsoft-edge-with-ie-mode-blog-series/m-p/2617124).

## <a name="common-ie-mode-issues"></a>Häufige Probleme im IE-Modus

Verwenden Sie diesen Abschnitt als Leitfaden, um die beiden häufigsten Probleme beim Wechseln zu Microsoft Edge im IE-Modus zu beheben und zu beheben. Diese Probleme sind:

- Falsche Dokumentmoduskonfigurationen
- Unvollständige neutrale Websitekonfigurationen

### <a name="incorrect-document-mode-configurations"></a>Falsche Dokumentmoduskonfigurationen

In diesem Abschnitt werden die Symptome beschrieben und Schritte zum Diagnostizieren und Beheben dieses Problems beschrieben.

#### <a name="symptoms"></a>Symptome

Bei Benutzern treten die folgenden Symptome auf:
  
- Größe und Positionierung von Seitenelementen sind möglicherweise deaktiviert oder fehlen 
- Einige Funktionen gehen möglicherweise verloren oder funktionieren nicht wie erwartet. Schaltflächen, die mit Internet Explorer funktioniert haben, führen beispielsweise keine Aktion aus oder geben einen Fehler zurück.

#### <a name="how-to-troubleshoot-and-fix"></a>Problembehandlung und Problembehandlung

Die allgemeine Strategie besteht darin, die gleichen Einstellungen zu duplizieren, die mit Internet Explorer 11 für eine bestimmte Website in unserer Websiteliste für den IE-Modus funktioniert haben. Verwenden Sie die Registerkarte "Emulation" der F12-Entwicklersymbolleiste in IE 11, die im nächsten Screenshot angezeigt wird, um das Szenario zu untersuchen, das Sie beheben möchten. Drücken Sie zum Öffnen der Entwicklersymbolleiste die F12-Taste, und wählen Sie dann **"DevTools öffnen" aus**.

![Registerkarte "Emulation" in der DevTools-Ansicht](./media/edge-ie-mode-faq/edge-ie-mode-emulation-tab.png)

Auf der Registerkarte "Emulation" werden zwei Informationen angezeigt, auf die sie sich konzentrieren müssen: der Dokumentmodus (1) und der Text unterhalb der Dropdownliste (2). Anhand dieser Informationen kann erläutert werden, warum wir uns im 11-Modus (Standard) für die Seite oder Website befinden, die wir uns ansehen.

Es gibt verschiedene Nachrichten, die für den Dokumentmodus angezeigt werden können, und in unserem Beispiel sind dies:
  
- Über X-UA-kompatibles Metatag
- Über X-UA-kompatiblen HTTP-Header

Die beiden X-UA-kompatiblen Optionen deuten darauf hin, dass auf der Webseite oder auf dem Webserver, auf dem die Website gehostet wird, der Dokumentmodus angezeigt wird, der vom Browser verwendet werden soll.  

Wir möchten den Dokumentmodus in fast allen Fällen berücksichtigen. Dazu müssen wir einen der folgenden Modi im Websitelisteneintrag für den IE-Modus für die Website auswählen:

- Standard
- IE8-Enterprise
- IE7-Enterprise

Diese Optionen berücksichtigen die Webseiten- oder Webserverdirektiven. Denken Sie daran, dass wir eine Option auswählen müssen, die den angegebenen Dokumentmodus enthält. Im Screenshot-Beispiel wird "Standard" ausgewählt, da der angegebene Dokumentmodus 11 ist, da IE8 Enterprise und IE7 Enterprise den IE 11-Dokumentmodus nicht unterstützen.  

Wenn der Dokumentmodus angibt, dass eine der folgenden Kompatibilitätsansichten für den Standort erforderlich ist, ist die Konfigurationseinstellung einfach.

- Über lokale Kompatibilitätsansichtseinstellungen
- Über die Kompatibilitätsansichtsliste
- Über Intranetkompatibilitätseinstellungen

Da alle Einstellungen der Kompatibilitätsansicht das Verhalten "IE7 Enterprise" zur Folge haben, wählen Sie diese Einstellung im Abschnitt "Compat Mode" des IE-Modus-Websitelisteneintrags aus.

Weitere Informationen zur Logik, die Internet Explorer oder der IE-Modus verwendet, um in einem Dokumentmodus über einen anderen zu landen, finden Sie im Artikel zu [veralteten Dokumentmodi und Internet Explorer 11](/internet-explorer/ie11-deploy-guide/deprecated-document-modes) .

Die allgemeine Regel besteht darin, den aktuellen logikbasierten Modus zu verwenden, der es einer bestimmten Website ermöglicht, wie erwartet zu funktionieren. Wir beginnen mit dem Standardmodus, wechseln in den IE8-Enterprise modus und bei Bedarf zum IE7-Enterprise Modus. Diese Auswahl bietet untergeordneten Seiten die Flexibilität, bei Bedarf unterschiedliche Dokumentmodi über die integrierte Logik für ihre spezifischen Anforderungen zu verwenden. Daher sind nicht alle Websiteseiten in einem bestimmten Dokumentmodus gesperrt.  

In der folgenden Tabelle sind die verfügbaren Dokumentmodi für diese Einstellungen aufgeführt.

| Logikbasierter Modus | Standard | IE8-Enterprise | IE7-Enterprise |
|--|--|--|--|
| Verfügbare Dokumentmodi | IE11-Dokumentmodus<br> IE10-Dokumentmodus<br>IE9-Dokumentmodus<br> IE8-Dokumentmodus<br>IE7-Dokumentmodus<br>IE5-Quirksmodus | IE8-Dokumentmodus<br>IE7-Dokumentmodus<br>IE5-Quirksmodus   | IE7-Dokumentmodus<br>IE5-Quirksmodus  |

> [!NOTE]
> In einigen Fällen erfordert eine bestimmte Website oder Seite einen bestimmten Dokumentmodus, um wie vorgesehen zu funktionieren. Es wird empfohlen, explizite Dokumentmodusoptionen nur zu verwenden, wenn die logikbasierten Optionen nicht wirksam sind.

### <a name="incomplete-neutral-site-configurations"></a>Unvollständige neutrale Websitekonfigurationen

In diesem Abschnitt werden die Symptome beschrieben und Schritte zum Diagnostizieren und Beheben dieses Problems beschrieben.

#### <a name="symptoms"></a>Symptome
  
Eine Seite verwendet SSO für die Authentifizierung, aber Benutzer werden mehrmals zur Eingabe von Anmeldeinformationen aufgefordert, erfahren ein Schleifenumleitungsverhalten, fehlgeschlagene Authentifizierungsfehler oder eine Kombination dieser Symptome.
  
#### <a name="how-to-troubleshoot-and-fix"></a>Problembehandlung und Problembehandlung
  
Bevor wir mit der Analyse eines fehlerhaften Workflows in Microsoft Edge beginnen, sehen Sie sich die Adressleiste für das IE-Modus-Logo "e" an, das im nächsten Screenshot angezeigt wird.

![IE-Logo auf Microsoft Edge Menüleiste.](./media/edge-ie-mode-faq/edge--ie-mode-logo.png)

Wenn während des SSO-Authentifizierungsprozesses das "e" angezeigt wird, aber nach einer Umleitung nicht mehr angezeigt wird, zeigt dieses Verhalten auf eine fehlende neutrale Website. Nachdem Microsoft Edge in den IE-Modus wechselt, müssen wir dort bleiben, um Sitzungs- und Cookieinformationen zu verwalten. Wenn die URL lange genug in der Adressleiste angezeigt wird, um sie zu identifizieren, fügen Sie sie der Websiteliste für den IE-Modus als neutrale Website hinzu, indem Sie die unter [Konfigurieren neutraler Websites](/deployedge/edge-ie-mode-sitelist#configure-neutral-sites) beschriebenen Schritte ausführen.

Häufig erfolgt der Umleitungszyklus so schnell, dass es schwierig ist, die fehlenden neutralen Websites zu identifizieren. Zur Unterstützung dieser Analyse verwenden wir ein Tool, das in das Chromium-Modul integriert ist: **Den Nettoexport**.

> [!TIP]
> Netzwerkablaufverfolgungen sind grundsätzlich laut. Um das Rauschen zu minimieren, schließen Sie alle anderen Browserinstanzen und Registerkarten, die für den spezifischen Workflow, den Sie untersuchen, nicht benötigt werden.

In den folgenden Schritten wird die Problembehandlung bei einer neutralen Standortkonfiguration beschrieben.
  
1. Öffnen Sie eine neue Registerkarte in Microsoft Edge, und wechseln Sie zu *edge://net-export*.
2. Wählen Sie **"Protokollierung auf Datenträger starten"** aus, und wählen Sie dann einen Speicherort aus, an dem Sie das resultierende JSON-Protokoll speichern möchten. Dieses Protokoll kann sicher gelöscht werden, nachdem Sie die Problembehandlung abgeschlossen haben.
3. Öffnen Sie eine weitere Registerkarte (lassen Sie die Registerkarte "NetExport" geöffnet), und wiederholen Sie den fehlerhaften Workflow.
4. Kehren Sie nach Abschluss des Vorgangs zur Registerkarte "Nettoexport" zurück, und wählen Sie **"Protokollierung beenden" aus**.
5. Wählen Sie den Link "netlog viewer" aus.
6. Wählen Sie auf der resultierenden Seite **"Datei auswählen"** aus, und wählen Sie dann die JSON-Datei aus, die Sie in Schritt 2 erstellt haben.
7. Nachdem die Protokolldatei geladen wurde, wählen Sie **Ereignisse** aus dem linken Menü aus.
8. Scrollen Sie durch das Netzwerkprotokoll, und identifizieren Sie die Start-URL. (Sie können auch die Suchfunktion verwenden, um Ihren Ausgangspunkt zu finden.)
9. Scrollen Sie vom Ausgangspunkt aus nach unten, und suchen Sie im Workflow nach URLs, die keinen Eintrag in der Websiteliste für den IE-Modus haben. Achten Sie besonders auf URLs mit Indikatoren für SSO, AUTH, LOGIN usw.
10. Nachdem Sie eine Kandidaten-URL identifiziert haben, fügen Sie sie der Websiteliste für den IE-Modus als neutrale Website hinzu, indem Sie in der Dropdownliste "Öffnen" **"Keine** " auswählen. Testen Sie den Workflow erneut.

In einigen Fällen sind je nach vorhandener Websitearchitektur mehrere neutrale Websiteeinträge erforderlich. Wenn der Workflow nach dem Hinzufügen einer neuen neutralen Website weiterhin fehlschlägt, wiederholen Sie den Vorgang, um ein neues Netexportprotokoll zu erfassen, und führen Sie einen weiteren Durchlauf aus.

In einigen seltenen Fällen kann es erforderlich sein, bestimmte freigegebene Cookies zu konfigurieren, um sicherzustellen, dass die erforderlichen Informationen auf Ihre Websites im IE-Modus übertragen werden. Wenn Sie ein bestimmtes Cookie kennen, das benötigt wird, können Sie die Cookiefreigabe mithilfe der unter Cookiefreigabe beschriebenen Schritte [von Microsoft Edge zu Internet Explorer](/deployedge/edge-ie-mode-add-guidance-cookieshare) konfigurieren.

### <a name="what-if-these-steps-dont-fix-the-issue"></a>Was geschieht, wenn das Problem durch diese Schritte nicht behoben wird?

Dieser Artikel soll ihnen helfen, die häufigsten Probleme bei der Konfiguration des IE-Modus zu beheben, aber möglicherweise wird nicht jedes mögliche Szenario behandelt. Wenn ein Problem auftritt, das Sie nicht beheben können und Hilfe benötigen, wenden Sie sich an App Assure, [https://aka.ms/AppAssure](https://aka.ms/AppAssure) und wir helfen Ihnen bei Ihrem Problem.

## <a name="get-general-diagnostic-and-configuration-information"></a>Abrufen allgemeiner Diagnose- und Konfigurationsinformationen

Sie können Diagnoseinformationen für den Internet Explorer-Modus auf der Registerkarte zur Microsoft Edge-Kompatibilität abrufen. Wechseln Sie zu *edge://compat/iediagnostic*, um diese Registerkarte zu öffnen. Auf der Seite "Diagnoseinformationen im Internet Explorer-Modus" werden möglicherweise Diagnosemeldungen angezeigt, und Sie können Diagnosedaten in eine XML-Datei exportieren. Diese Diagnoseinformationsseite enthält auch Konfigurationsinformationen für die folgenden Kategorien:

- **Überprüfung des Registrierungsschlüssels:** (Wird nur angezeigt, wenn die Überprüfung fehlschlägt.) Überprüft, ob die Internet Explorer-Integration in der Registrierung ordnungsgemäß eingerichtet wurde. Wenn nicht, kann der Benutzer **"Beheben"** auswählen, um das Problem zu beheben.
- **Internet Explorer-Modus:** Zeigt die verwendete API-Version an, die auf der Konfiguration und dem Betriebssystem basiert. Wenn ein Problem vorliegt, wird der Benutzer möglicherweise aufgefordert, ein Windows Update zu installieren.
- **Einstellung für Internet Explorer-Modus:** Zeigt an, ob und wie der Internet Explorer-Modus konfiguriert ist.
- **Befehlszeile:** Zeigt die Befehlszeilenzeichenfolge und Switches an, die zum Starten Microsoft Edge verwendet werden.
- **Gruppenrichtlinieneinstellungen:** Zeigt an, ob der IE-Modus mithilfe von Gruppenrichtlinien und den angewendeten Richtlinien konfiguriert ist.

### <a name="error-message-to-open-this-page-in-internet-explorer-mode-reinstall-microsoft-edge-with-administrator-privileges"></a>Fehlermeldung: "Zum Öffnen dieser Seite im IE-Modus versuchen Sie, Microsoft Edge mit Administratorrechten neu zu installieren."

Dieser Fehler wird möglicherweise angezeigt, wenn Nicht alle erforderlichen Windows Updates vorhanden sind. Siehe die unter [Info zum IE-Modus](./edge-ie-mode.md) aufgeführten Voraussetzungen für die erforderlichen Versionen von Windows und Microsoft Edge.

If you've already installed all required Windows Updates, you might see this error if:

- Sie verwenden den Canary Channel, der standardmäßig auf der Benutzerebene installiert wird.
- Sie verwenden den Stable-, Beta- oder Dev-Kanal, aber bei der Aufforderung zur Rechteerweiterung während der Installation wurde die Rechteerweiterung abgebrochen. Wenn Sie die Eingabeaufforderung für erhöhte Rechte abbrechen, wird die Installation auf Benutzerebene fortgesetzt.
- Internet Explorer 11 wurde in Windows-Features deaktiviert.

Mögliche Lösungen sind:

- Führen Sie das Installationsprogramm für einen beliebigen Kanal auf Systemebene aus: `installer.exe --system-level`
- Aktivieren Sie Internet Explorer 11 in Windows-Features.

Um zu überprüfen, ob Microsoft Edge auf Systemebene installiert ist, geben Sie "edge://version" in die Adressleiste von Microsoft Edge ein. Der Pfad für die ausführbare Datei beginnt mit *C:\Programmdateien* und weist auf eine Systeminstallation hin. Wenn der pfad der ausführbaren Datei mit *C:\Users* beginnt, deinstallieren Sie Microsoft Edge mit Administratorrechten, und installieren Sie ihn neu.

### <a name="error-message-to-open-this-page-in-ie-mode-try-restarting-microsoft-edge"></a>Fehlermeldung "Versuchen Sie, Microsoft Edge neu zu starten, um diese Seite im IE-Modus zu öffnen."

Dieser Fehler wird möglicherweise angezeigt, wenn in Internet Explorer ein unerwarteter Fehler aufgetreten ist. Beim Neustart von Microsoft Edge wird dieser Fehler in der Regel behoben.

### <a name="error-message-turn-off-remote-debugging-to-open-this-site-in-ie-mode-otherwise-it-might-not-work-as-expected"></a>Fehlermeldung: "Deaktivieren Sie das Remotedebuggen, um diese Website im IE-Modus zu öffnen, da es sonst möglicherweise nicht wie erwartet funktioniert."

Dieser Fehler wird möglicherweise angezeigt, wenn Sie remote debuggen und zu einer Webseite navigieren, die für die Ausführung im IE-Modus konfiguriert ist. Sie können den Vorgang fortsetzen, aber die Seite wird mit Microsoft Edge gerendert.

### <a name="error-message-could-not-retrieve-emie-site-list"></a>Fehlermeldung: "EMIE-Websiteliste konnte nicht abgerufen werden."

Möglicherweise wird dieser Fehler auf der *edge://compat/enterprise* Seite angezeigt, der angibt, dass der Download der Websiteliste fehlgeschlagen ist. Ab Microsoft Edge Version 87 ist die HTTP-Authentifizierung auch nicht zulässig, wenn Cookies für Anforderungen von Drittanbietern mithilfe der [BlockThirdPartyCookies-Richtlinie](/deployedge/microsoft-edge-policies#blockthirdpartycookies) blockiert werden. Sie können Cookies für die bestimmte Domain zulassen, in der sich Ihre Site-Liste im Unternehmensmodus befindet, indem Sie die [CookiesAllowedForURLs](/deployedge/microsoft-edge-policies#cookiesallowedforurls)-Richtlinie verwenden, um sicherzustellen, dass das Herunterladen der Site-Liste erfolgreich ist.

### <a name="error-message-the-connection-for-this-site-is-not-secure"></a>Fehlermeldung: "Die Verbindung für diese Website ist nicht sicher"

Dieser Fehler kann auftreten, wenn Sie versuchen, eine ältere Website im IE-Modus zu öffnen und die Website für die Ausführung in TLS 1.0 oder TLS 1.1 konfiguriert ist. Diese Protokolle sind in Microsoft Edge standardmäßig deaktiviert. Weitere Informationen finden Sie unter [Plan for change: TLS 1.0 and TLS 1.1 soon to be disabled by default](https://blogs.windows.com/msedgedev/2020/03/31/tls-1-0-tls-1-1-schedule-update-edge-ie11/)

### <a name="error-message-this-form-cannot-be-opened-in-a-web-browser-to-open-this-form-use-microsoft-infopath"></a>Fehlermeldung: "Dieses Formular kann nicht in einem Webbrowser geöffnet werden. Verwenden Sie zum Öffnen dieses Formulars Microsoft InfoPath.

Für bestimmte Anwendungen müssen Sie die Webseite möglicherweise im IE-Modus laden. Sie können das IE-Modusfeature in Microsoft Edge verwenden.

Möglicherweise müssen Sie auch das Attribut in Enterprise `compat-mode` Mode Site List auf **"Default**" festlegen. Weitere Informationen finden Sie unter [Enterprise Modus und der Enterprise Mode Site List](/internet-explorer/ie11-deploy-guide/what-is-enterprise-mode#enterprise-mode-and-the-enterprise-mode-site-list-1).

> [!TIP]
> Ihre Benutzer können diese Websiteliste und den Kompatibilitätsmodus ganz einfach anzeigen, indem Sie **"about:compat**" in Microsoft Edge eingeben.

## <a name="frequently-asked-questions"></a>Häufig gestellte Fragen

### <a name="will-ie-mode-replace-internet-explorer-11"></a>Wird der IE-Modus Internet Explorer 11 ersetzen?

Ja, die Internet Explorer 11-Desktopanwendung wird eingestellt und wird am 15. Juni 2022 nicht mehr unterstützt. Informationen zum Umfang finden Sie unter ["Häufig gestellte Fragen zum Lebenszyklus" – Internet Explorer](/lifecycle/faq/internet-explorer-microsoft-edge). Dieselben IE11-Apps und -Websites, die Sie heute verwenden, können in Microsoft Edge im Internet Explorer-Modus geöffnet werden. Weitere Informationen finden Sie [unter "The future of Internet Explorer on Windows 10 is in Microsoft Edge](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/)".

### <a name="can-i-use-view-in-file-explorer-in-sharepoint-online-on-microsoft-edge"></a>Kann ich "Im Datei-Explorer anzeigen" in SharePoint Online auf Microsoft Edge verwenden?

Ab Microsoft Edge Version 95 können Sie die Funktion "**Im Datei-Explorer anzeigen**" für SharePoint moderne Onlinedokumentbibliotheken aktivieren. Damit diese Erfahrung für Ihre Benutzer sichtbar und funktionsfähig ist, müssen Sie die Richtlinie [Microsoft Edge "Konfigurieren des Features "Ansicht im Datei-Explorer für SharePoint Seiten in Microsoft Edge"](/deployedge/microsoft-edge-policies#configureviewinfileexplorer) aktivieren und Ihre SharePoint Onlinemandantenkonfiguration aktualisieren. Weitere Informationen: [Anzeigen SharePoint Dateien mit dem Datei-Explorer in Microsoft Edge – SharePoint in Microsoft 365 | Microsoft Docs](/SharePoint/sharepoint-view-in-edge).

Anstatt jedoch die Option "Im Datei-Explorer anzeigen" zu verwenden, empfiehlt es sich, Dateien und Ordner außerhalb von SharePoint zu verwalten, das [Synchronisieren SharePoint und Teams von Dateien mit Ihrem Computer](https://support.microsoft.com/office/sync-sharepoint-and-teams-files-with-your-computer-6de9ede8-5b6e-4503-80b2-6190f3354a88?ui=en-us&rs=en-us&ad=us) oder [das Verschieben oder Kopieren von Dateien in SharePoint](https://support.microsoft.com/office/move-or-copy-files-in-sharepoint-00e2f483-4df3-46be-a861-1f5f0c1a87bc?ui=en-us&rs=en-us&ad=us).

### <a name="does-ie-mode-on-microsoft-edge-support-the-no-merge-option-that-was-supported-in-internet-explorer-11"></a>Unterstützt der IE-Modus auf Microsoft Edge die Option "Kein Zusammenführen", die in Internet Explorer 11 unterstützt wurde?

Die empfohlenen Alternativen für die No-Merge-Funktionalität in Microsoft Edge sind eine der folgenden Aktionen:

1. Verwenden von Profilen in Microsoft Edge – Jedes Profil ist einer anderen IE-Sitzung für IE-Modusseiten zugeordnet, sodass es sich identisch mit der Option zum Zusammenführen verhält.
2. Verwenden Sie die Befehlszeile `--user-data-dir=<path>`, aber für jede Sitzung mit einem anderen Pfad. Bei Bedarf können Sie ein Hilfsprogramm für den Benutzer erstellen, das Microsoft Edge startet und den Pfad für die Sitzung ändert.

Wenn keine der vorherigen Optionen für Ihr Szenario funktioniert, unterstützt der IE-Modus für Microsoft Edge ab Microsoft Edge Version 93 keine Zusammenführung. Wenn ein neues Browserfenster von einer IE-Modusanwendung gestartet wird, befindet sich ein Endbenutzer in einer separaten Sitzung, wie z. B. das No-Merge-Verhalten in IE11.

Bei jedem Microsoft Edge Fenster wird beim ersten Aufrufen einer IE-Modus-Registerkarte in diesem Fenster, wenn es sich um eine bestimmte "No-Merge"-Website handelt, dieses Fenster in einer anderen IE-Sitzung ohne Zusammenführung gesperrt.  Dieses Fenster bleibt von allen anderen Microsoft Edge Fenstern gesperrt, bis die letzte IE-Modus-Registerkarte im gesperrten Fenster geschlossen wird. Dies folgt dem vorherigen Verhalten, bei dem Benutzer IE ohne Zusammenführung starten und Microsoft Edge ohne Zusammenführung mit anderen Mechanismen starten konnten. Alle Websites, die in einem neuen Fenster (über window.open) geöffnet werden, berücksichtigen die Zusammenführungsart des übergeordneten Prozesses.

> [!NOTE]
> Das Wechseln der Sitzung wird nicht unterstützt. Navigationen auf derselben Registerkarte im IE-Modus verwenden dieselbe Sitzung.

Sie können das No-Merge-Verhalten in Microsoft Edge Version 93 oder höher überprüfen, indem Sie die folgenden Schritte ausführen:

1. Stellen Sie sicher, dass der IE-Modus in Microsoft Edge Version 93 oder höher aktiviert ist.
2. Sie können Websites konfigurieren, die die Sitzungsfreigabe in der Enterprise Mode Site List verhindern müssen, indem Sie den Wert des Seriendruck-Attributs auf "no-merge" festlegen. Dieses Attribut gilt nicht nur, wenn das Open-In-Element auf Microsoft Edge festgelegt ist. Standardmäßig weisen alle Websites einen Seriendrucktypwert auf. (**Hinweis:** Das integrierte Websitelisten-Manager-Tool, das unter *edge://compat/sitelistmanager* verfügbar ist, enthält beim Hinzufügen oder Bearbeiten einer Website das Kontrollkästchen **"Keine Zusammenführung** ".)

   ```
   <site url="contoso.com">
   <open-in merge-type="no-merge">IE11</open-in>
   </site>
   ```

3. Navigieren Sie zu einer beliebigen Website, die als Seriendruck konfiguriert ist. Die Website sollte sich in einer eigenen nicht zusammengeführten IE-Sitzung befinden. Wenn Sie eine andere Microsoft Edge Instanz oder ein anderes Fenster öffnen und zu derselben Website navigieren, sollte sich diese in einer eigenen IE-Sitzung befinden. Beachten Sie, dass es mehrere iexplore.exe Prozesse im Task-Manager gibt.

Wenn Sie Feedback haben, wenden Sie sich über einen unserer Feedbackkanäle: Microsoft-Support oder das [TechCommunity-Forum](https://techcommunity.microsoft.com/t5/enterprise/bd-p/EdgeInsiderEnterprise) .

### <a name="can-i-save-links-as-webpages-in-internet-explorer-mode"></a>Kann ich Links im Internet Explorer-Modus als Webseiten speichern?

Ja, Sie können die Option „Ziel speichern unter“ im Kontextmenü für den Internet Explorer-Modus in Microsoft Edge aktivieren. Konfigurieren Sie dazu die Gruppenrichtlinie "Speichern des *Ziels im Internet Explorer-Modus zulassen*" unter *Computerkonfiguration > Administrative Vorlagen > Windows Komponenten > Internet Explorer*. Der Speichermechanismus funktioniert wie in Internet Explorer, und wenn das Ziel als HTML-Datei gespeichert wird, wird die Seite beim erneuten Öffnen der Datei in Microsoft Edge gerendert.

Die Möglichkeit, Links als Webseiten zu speichern, erfordert die folgenden Mindestaktualisierungen des Betriebssystems:

- Windows 10, Version 2004, Windows Server, Version 2004, Windows 10, Version 20H2: [KB4580364](https://support.microsoft.com/help/4580364/windows-10-update-kb4580364)
- Windows 10 Version 1903, Windows 10, Version 1909, Windows Server, Version 1903 ([KB4580386](https://support.microsoft.com/help/4580386/windows-10-update-kb4580386))
- Windows 10 Version 1809, Windows Server Version 1809, Windows Server 2019 ([KB4580390](https://support.microsoft.com/help/4580390/windows-10-update-kb4580390))
- Windows 10, Version 1803: [KB4586785](https://support.microsoft.com/help/4586785/windows-10-update-kb4586785)
- Windows 10, Version 1607: [KB4586830](https://support.microsoft.com/help/4586830/windows-10-update-kb4586830)
- Windows 10, Version 1507: [KB4586787](https://support.microsoft.com/help/4586787/windows-10-update-kb4586787)

### <a name="can-i-test-a-site-in-microsoft-edge-while-it-is-configured-to-open-ie-mode-in-the-enterprise-mode-site-list"></a>Kann ich eine Website in Microsoft Edge testen, während sie so konfiguriert ist, dass der IE-Modus in der Websiteliste für den Enterprise modus geöffnet wird?

Ja, während Sie Ihre älteren Websites modernisieren, können Sie im IE-Modus konfigurierte Anwendungen auf Microsoft Edge testen. Zum Testen dieser Apps können Sie die [InternetExplorerModeTabInEdgeModeAllowed-Richtlinie](/deployedge/microsoft-edge-policies#internetexplorermodetabinedgemodeallowed) konfigurieren. Wenn Sie diese Richtlinie aktivieren, können Ihre Benutzer Websites im IE-Modus in Microsoft Edge öffnen, indem **sie Einstellungen und mehr** (das Ellipsensymbol ...) > **Weitere** **ToolsOpen-Websites** >  im Edgemodus auswählen.

### <a name="how-can-i-debug-my-legacy-application-while-using-ie-mode-on-microsoft-edge"></a>Wie kann ich meine Legacyanwendung debuggen, während ich den IE-Modus auf Microsoft Edge verwende?

Sie können IEChooser verwenden, um die Internet Explorer DevTools zu starten, um den Inhalt Ihrer IE-Modus-Registerkarten zu debuggen. Gehen Sie folgendermaßen vor, um IEChooser zu verwenden:

1. Öffnen Sie IEChooser.
   - Öffnen des Dialogfelds Ausführen Drücken Sie z. B. die `Windows logo key` + `R`.
   - Geben Sie ein `%systemroot%\system32\f12\IEChooser.exe`, und wählen Sie dann **OK** aus.
2. Wählen Sie in IEChooser den Eintrag für die Registerkarte "IE-Modus" aus.

### <a name="my-application-requires-transferring-post-data-between-ie-mode-and-microsoft-edge-is-this-supported"></a>Meine Anwendung erfordert die Übertragung von POST-Daten zwischen dem IE-Modus und Microsoft Edge. Wird dies unterstützt?

Ab Microsoft Edge Beta Channel Version 96 enthalten Navigationen, die zwischen Internet Explorer-Modus und Microsoft Edge wechseln, Formulardaten und zusätzliche HTTP-Header. Wenn Formulardaten jedoch Dateianlagen enthalten, werden sie nicht zwischen Modulen übertragen. Mithilfe der [Gruppenrichtlinie "InternetExplorerIntegrationComplexNavDataTypes](/deployedge/microsoft-edge-policies#internetexplorerintegrationcomplexnavdatatypes) " können Sie auswählen, welche Datentypen in solche Navigationen eingeschlossen werden sollen.

Zusätzlich zu Microsoft Edge Version 96 müssen Für diese Erfahrung die folgenden Windows Updates installiert sein:

- Windows 11 [KB5007262](https://support.microsoft.com/topic/november-22-2021-kb5007262-os-build-22000-348-preview-7f3e18d7-4189-4882-b0e9-afc920253aee) oder höher
- Windows Server 2022 [KB5007254](
https://support.microsoft.com/topic/november-22-2021-kb5007254-os-build-20348-380-preview-9a960291-d62e-486a-adcc-6babe5ae6fc1) oder höher
- Windows 10 Version 2004; Windows Server Version 2004; Windows 10 Version; Windows Server Version 20H2 und Windows 10 Version 21H1 – [KB5006738](https://support.microsoft.com/topic/october-26-2021-kb5006738-os-builds-19041-1320-19042-1320-and-19043-1320-preview-ccbce6bf-ae00-4e66-9789-ce8e7ea35541) oder höher
- Windows 10 Version 1909 [KB5007189](
https://support.microsoft.com/topic/november-9-2021-kb5007189-os-build-18362-1916-91b4647c-9979-4d84-8e64-efc8674e8c1f) oder höher

### <a name="where-can-i-find-the-reload-in-internet-explorer-mode-option"></a>Wo finde ich die Option "Im Internet Explorer-Modus neu laden"?

Dieses Feature ist in Microsoft Edge Version 92 oder höher verfügbar. Um diese Option zu aktivieren, konfigurieren Sie "Zulassen, dass Websites in den Einstellungen des Internet Explorer-Modus neu geladen werden" in Microsoft Edge auf "Zulassen".  Weitere Informationen finden Sie unter [Aktivieren der lokalen Websitelistenoberfläche](/deployedge/edge-ie-mode-local-site-list#enable-the-local-site-list-experience).

### <a name="where-is-the-file--new-session-option-in-microsoft-edge"></a>Wo befindet sich die Option "Datei > Neue Sitzung" in Microsoft Edge?

Eine moderne Browserlösung ist mithilfe mehrerer Profile in Microsoft Edge verfügbar. Mit diesem Feature können Sie eine neue Sitzung mit einem anderen Konto erstellen. Die folgenden Ressourcen enthalten Informationen zu den Vorteilen mehrerer Profile und deren Verwendung.

- [Video: Microsoft Edge und Identität](/deployedge/microsoft-edge-video-identity)
- [Die Verwendung mehrerer Profile bei der Arbeit und zu Hause ist jetzt mit Microsoft Edge](https://blogs.windows.com/msedgedev/2020/04/30/automatic-profile-switching/)

### <a name="why-am-i-getting-multiple-authentication-prompts-when-running-a-page-in-ie-mode-on-microsoft-edge"></a>Warum erhalte ich beim Ausführen einer Seite im IE-Modus auf Microsoft Edge mehrere Authentifizierungsaufforderungen?

Das Clientzertifikat kann zweimal im IE-Modus angefordert werden. Beim ersten Mal wird das Dialogfeld für die Zertifikatauswahl im IE-Modus angezeigt, und beim zweiten Mal wird das Dialogfeld in Microsoft Edge angezeigt. Sowohl der Frameprozess als auch der Fensterprozess müssen eine Authentifizierung anfordern.

Nachdem der Favicon-Cache erstellt wurde, werden Sie nicht erneut nach einem Clientzertifikat gefragt, es sei denn, Sie löschen den Cache. Alternativ können Sie eine Regel in der Serverkonfiguration festlegen, z. B. IIS, um kein Clientzertifikat für das Favicon zu benötigen.

### <a name="why-are-there-rendering-issues-like-text-wrapping-and-content-truncation-when-child-windows-are-running-in-ie-mode-in-microsoft-edge"></a>Warum gibt es Renderingprobleme wie Textumbruch und Inhaltskürzung, wenn untergeordnete Fenster im IE-Modus in Microsoft Edge ausgeführt werden?

Der Inhaltsbereich eines untergeordneten Fensters, das im IE-Modus in Microsoft Edge gerendert wird, unterscheidet sich geringfügig von dem in Internet Explorer 11. Wenn eine Webseite mit pixelbasierter Ausrichtung oder Positionierung entworfen wurde, tritt möglicherweise ein falsches Rendering, Textumbruch usw. auf.

Microsoft Edge Version 95 wurden zwei Richtlinieneinstellungen hinzugefügt, mit denen Sie benutzerdefinierte Anpassungen der Höhe und Breite von Popupfenstern festlegen können, die über die Methode von Websites im `window.open` IE-Modus generiert werden. Sie können die folgenden Richtlinien verwenden, um die Fenstergröße anzupassen:

- [InternetExplorerIntegrationWindowOpenHeightAdjustment](/deployedge/microsoft-edge-policies#internetexplorerintegrationwindowopenheightadjustment) : Mit dieser Einstellung können Sie eine benutzerdefinierte Anpassung an die Höhe der Popupfenster festlegen, die von der Internet Explorer-Moduswebsite generiert werden.
- [InternetExplorerIntegrationWindowOpenWidthAdjustment](/deployedge/microsoft-edge-policies#internetexplorerintegrationwindowopenwidthadjustment) – Mit dieser Einstellung können Sie eine benutzerdefinierte Anpassung an die Breite der Popupfenster festlegen, die von der Internet Explorer-Moduswebsite generiert werden.

### <a name="why-arent-pop-ups-or-redirected-websites-loading-in-ie-mode-or-in-internet-explorer-11"></a>Warum werden Popups oder umgeleitete Websites nicht im IE-Modus oder in Internet Explorer 11 geladen?

Nach dem Konfigurieren des IE-Modus werden bestimmte Websites, insbesondere websites, die ein neues Fenster erstellen oder eine Website, die umgeleitet wird, möglicherweise nicht im IE-Modus gerendert oder in Internet Explorer 11 geöffnet.

Für diese Art von umgeleiteter Website können Sie die `allow-redirect="true"` In der Websitelistenkonfiguration verwenden. Weitere Informationen finden Sie unter [Aktualisierte Schemaelemente](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance#updated-schema-elements).

### <a name="why-arent-websites-loading-in-ie-mode-when-i-launch-microsoft-edge-for-the-first-time"></a>Warum werden Websites nicht im IE-Modus geladen, wenn ich Microsoft Edge zum ersten Mal starte?

Microsoft Edge muss die Websiteliste für den IE-Modus herunterladen, bevor sie IE-Moduseinstellungen anwenden kann. Dieser Vorgang wird möglicherweise nicht abgeschlossen, wenn der Browser gestartet wird. Es ist eine Richtlinie verfügbar, die das Laden der Websiteliste erzwingen kann, bevor eine Website geladen wird. Weitere Informationen hierzu finden Sie in der [DelayNavigationsForInitialSiteListDownload](/deployedge/microsoft-edge-policies#delaynavigationsforinitialsitelistdownload)-Richtlinie.

### <a name="why-cant-i-open-files-or-pages-that-are-found-by-using-file-urls-in-microsoft-edge"></a>Warum kann ich keine Dateien oder Seiten öffnen, die mithilfe file:// URLs in Microsoft Edge gefunden werden?

Aufgrund einer Chromium Sicherheitseinschränkung muss der IE-Modus verwendet werden. Sie können das IE-Modusfeature Microsoft Edge verwenden, um Webseiten zu laden, die im **file://**-Protokoll innerhalb einer Intranetzone gehostet werden. Sie können die [IntranetFileLinksEnabled-Gruppenrichtlinie](/deployedge/microsoft-edge-policies#intranetfilelinksenabled) verwenden, um diese Funktionalität zu aktivieren.

## <a name="see-also"></a>Weitere Informationen
  
- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)
- [Informationen zum IE-Modus](./edge-ie-mode.md)
- [Weitere Informationen zum Unternehmensmodus](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
