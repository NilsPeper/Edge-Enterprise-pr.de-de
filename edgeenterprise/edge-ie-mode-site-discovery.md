---
title: Schrittweise Anleitung für Enterprise Site Discovery
ms.author: cjacks
author: appcompatguy
manager: saudm
ms.date: 04/07/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Verwenden von Enterprise Site Discovery zur Vorbereitung auf den IE-Modus
ms.openlocfilehash: 2557544a93222b03aaa0961149aa0d3c5d7d8806
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/24/2021
ms.locfileid: "11447719"
---
# <a name="enterprise-site-discovery-step-by-step-guide"></a>Schrittweise Anleitung für Enterprise Site Discovery

Dieser Artikel enthält eine schrittweise Anleitung zur Verwendung von Enterprise Site Discovery mit Microsoft Endpoint Configuration Manager.

Enterprise Site Discovery kann Ihnen beim Konfigurieren Ihrer Enterprise Mode Site List helfen. Enterprise Site Discovery hilft Ihnen bei Folgendem:

- Ermitteln, welche Websites ältere Dokumentmodi verwenden. Falls diese Websites nicht moderne Browser erkennen und unterschiedliche HTML-Adressen bereitstellen, müssen sie wahrscheinlich den IE-Modus verwenden.
- Ermitteln, welche Websites ActiveX-Steuerelemente verwenden. Microsoft Edge unterstützt keine ActiveX-Steuerelemente. Falls diese Websites nicht moderne Browser erkennen und unterschiedliche HTML-Adressen bereitstellen, müssen sie wahrscheinlich den IE-Modus verwenden.

> [!NOTE]
> Dieser Artikel bezieht sich auf die Microsoft Edge-Kanäle **Stable**, **Beta** und **Dev**, Version 77 oder höher.

## <a name="prerequisites"></a>Voraussetzungen

In diesem Leitfaden wird davon ausgegangen, dass Sie mit der Verwendung von Microsoft Endpoint Configuration Manager vertraut sind und die folgenden Dienste und Rollen eingerichtet haben:

1. Microsoft Endpoint Configuration Manager
2. Microsoft SQL Server Reporting Services
3. (Optional) Die Configuration Manager Reporting Services- Punkt-Rolle wurde konfiguriert

## <a name="download-enterprise-site-discovery-tools"></a>Enterprise Site Discovery-Tools herunterladen

Laden Sie die folgenden Tools herunter:

- [Setup- und Konfigurationspaket für Enterprise Site Discovery](https://go.microsoft.com/fwlink/p/?LinkId=517719)
- [Microsoft Berichts-Generator](https://www.microsoft.com/download/details.aspx?id=53613)

## <a name="enable-enterprise-site-discovery"></a>Enterprise Site Discovery aktivieren

Bevor Sie eine Verbindung mit der Windows-Verwaltungsinstrumentation (WMI) herstellen können, um Website-Ermittlungsdaten abzurufen, müssen Sie zuerst den WMI-Klassenanbieter auf dem Gerät bereitstellen.

Extrahieren Sie die Inhalte aus dem **Setup- und Konfigurationspaket für Enterprise Site Discovery** in einen Ordner in der endgültigen Softwarebibliotheksfreigabe. Beispiel: **\\\\DSL\\EnterpriseSiteDiscovery**.

Erstellen Sie als Nächstes ein Paket in Microsoft Endpoint Configuration Manager, wie in der [Dokumentation](/configmgr/apps/deploy-use/packages-and-programs)beschrieben, und wählen Sie die folgenden Optionen aus:

- Wählen Sie auf der **Paket**-Seite **Name** aus, und geben Sie den Namen **Site-Discovery aktivieren** an.
- Aktivieren Sie auf der **Paket**-Seite die Option **Dieses Paket enthält Quelldateien**.
- Geben Sie auf der **Paket**-Seite den Quellordner an, in den Sie die Dateien extrahiert haben (z. B. **\\\\DSL\\EnterpriseSiteDiscovery**)
- Wählen Sie auf der Seite **Programmtyp** die Option **Standardprogramm**.
- Klicken Sie auf der Seite **Standardprogramm** in die Befehlszeile, um die Site-Discovery auf dem Gerät wie folgt zu konfigurieren:
  ```dos
  powershell.exe -ExecutionPolicy Bypass .\IETelemetrySetUp-Win8.ps1
  ```
  > [!NOTE]
  > Das Skript unterstützt die Verwendung von Befehlszeilenoptionen für `-ZoneAllowList` und `-SiteAllowList`. In dieser schrittweisen Anleitung konfigurieren Sie diese Optionen über eine Gruppenrichtlinie (siehe weiter unten).
- Wählen Sie auf der Seite **Standardprogramm** die Option zum Ausführen **im Hintergrund** aus.
- Wählen Sie auf der Seite **Standardprogramm** unter **Programm kann ausgeführt werden** die Option **Unabhängig von Benutzeranmeldung** aus.

Nachdem Sie das Paket erstellt haben, doppelklicken Sie auf den Paketnamen **Site-Discovery aktivieren**, um dessen Eigenschaften anzuzeigen. Wählen Sie in der Eigenschaft **Nach dem Ausführen** die Option **Configuration Manager startet Computer neu** aus. Die WMI-Datenerfassung beginnt nach dem Neustart des Geräts.

> [!NOTE]
> Sie können die Zeitdauer konfigurieren, die ein Benutzer zum Neustarten des Geräts hat, wie in der [Dokumentation zu Clienteinstellungen](/configmgr/core/clients/deploy/about-client-settings#computer-restart) beschrieben.

## <a name="configure-enterprise-site-discovery-via-group-policy"></a>Konfigurieren von Enterprise Site Discovery über eine Gruppenrichtlinie

Wenn Enterprise Site Discovery aktiviert ist, können Sie konfigurieren, welche Daten erfasst werden sollen. Berücksichtigen Sie die lokalen Gesetze und behördlichen Bestimmungen gemäß der Beschreibung [auf dieser Seite](/internet-explorer/ie11-deploy-guide/collect-data-using-enterprise-site-discovery#what-data-is-collected).

1. Öffnen Sie den Gruppenrichtlinien-Editor.
2. Klicken Sie auf **Computerkonfiguration** > **Administrative Vorlagen** > **Windows-Komponenten** > **Internet Explorer**. 
3. Doppelklicken Sie auf **WMI-Ausgabe für Site-Discovery aktivieren**.
4. Wählen Sie **Aktiviert** aus.
5. Klicken Sie auf **OK** oder **Übernehmen**, um diese Richtlinieneinstellung zu speichern.

Sie können die Zonen einschränken, in denen Websitedaten erfasst werden:

1. Doppelklicken Sie auf **Site-Discovery-Ausgabe nach Zone beschränken**.
2. Wählen Sie **Aktiviert** aus.
3. Geben Sie eine Bitmaske an, die angibt, für welche Zonen die Site-Discovery aktiviert werden soll:
    1. Zone eingeschränkter Sites
    2. Zone „Internet“
    3. Zone der vertrauenswürdigen Sites
    4. Zone „Lokales Intranet“
    5. Zone des lokalen Computers
    
    Beispiel 1: **00010** erfasst nur Daten für die lokale Intranetzone.

    Beispiel 2: **10111** erfasst Daten für alle Zonen außer der Internet-Zone.
4. Klicken Sie auf **OK** oder **Übernehmen**, um diese Richtlinieneinstellung zu speichern.

Sie können die Domänen einschränken, zu denen Websitedaten erfasst werden:

1. Doppelklicken Sie auf **Site-Discovery-Ausgabe nach Domäne beschränken**.
2. Wählen Sie **Aktiviert** aus.
3. Geben Sie die Domänen ein, zu denen Daten erfasst werden sollen (eine Domäne pro Zeile).
4. Klicken Sie auf **OK** oder **Übernehmen**, um diese Richtlinieneinstellung zu speichern.

## <a name="collect-site-discovery-data-using-configuration-manager"></a>Erfassen von Site-Discovery-Daten mithilfe von Configuration Manager

Nachdem Ihre Geräte begonnen haben, Daten zu generieren, ist es an der Zeit, diese Daten in Configuration Manager zu erfassen.

1. Wählen Sie in der Configuration Manager-Konsole **Verwaltung** > **Clienteinstellungen** > **Clientstandardeinstellungen** aus.
2. Wählen Sie auf der Registerkarte **Startseite** in der Gruppe **Eigenschaften** die Option **Eigenschaften** aus.
3. Klicken Sie im Dialogfeld **Clientstandardeinstellungen** auf **Hardwareinventur**.
4. Wählen Sie in der Liste **Geräteeinstellungen** die Option **Klassen festlegen** aus.
5. Wählen Sie im Dialogfeld **Hardwareinventurklassen** die Option **Hinzufügen** aus.
6. Klicken Sie im Dialogfeld **Hardwareinventurklasse hinzufügen** auf **Verbinden**.
7. Geben Sie im Dialogfeld **WMI-Verbindung herstellen** den Namen eines Computers ein, auf dem Enterprise Site Discovery konfiguriert ist. Wenn Sie eine Verbindung mit einem anderen Computer herstellen möchten, benötigen Sie Anmeldeinformationen mit der Berechtigung für den Zugriff auf WMI.
8. Geben Sie in das Textfeld **WMI-Namespace** Folgendes ein: **root\cimv2\IETelemetry**.
9. Wählen Sie **Verbinden** aus.
10. Wählen Sie im Dialogfeld **Hardwareinventurklasse hinzufügen** in der Liste **Inventurklassen** die WMI-Klassen **IESystemINfo**, **IEUrlInfo** und **IECountInfo* aus.
11. Klicken Sie auf **OK**, um das Dialogfeld **Klassenkennzeichner** und die anderen geöffneten Dialogfelder zu schließen.

Nachdem der Client die Einstellungen über den Verwaltungspunkt aktualisiert hat, werden Datenberichte beim Ausführen der nächsten Hardwareinventur (standardmäßig alle sieben Tage) erstellt.

## <a name="import-site-discovery-reports"></a>Importieren von Site-Discovery-Berichten

Das Enterprise Site Discovery-Paket enthält zwei Beispielberichte. Ein Bericht umfasst Websites, die ActiveX-Steuerelemente verwenden, und der andere Websites, die ältere Dokumentmodi verwenden.

### <a name="configure-the-site-discovery-sample-report"></a>Konfigurieren des Site-Discovery-Beispielberichts

Führen Sie die folgenden Schritte aus, um einen Beispielbericht zu erstellen, der drei Datenquellen verwendet: die von Benutzern besuchten Websites, Informationen zu ihrem System und die von den Websites verwendeten Dokumentmodi. Anhand dieses Berichts können Sie Websites identifizieren, die von älteren Dokumentmodi abhängig sein könnten.

1. Kopieren Sie den Bericht **SCCM_Report-Site_Discovery.rdl** auf den Configuration Manager-Server.
2. Installieren Sie den [Microsoft Berichts-Generator](/sql/reporting-services/install-windows/install-report-builder?view=sql-server-ver15).
3. Doppelklicken Sie auf **SCCM_Report-Site_Discovery.rdl**, um den Bericht im Berichts-Generator zu öffnen.
4. Wenn Sie den Bericht zum ersten Mal öffnen, versucht er, den Server zu kontaktieren, auf dem er erstellt wurde. Wenn Sie aufgefordert werden, eine **Verbindung mit dem Berichtsserver herzustellen**, klicken Sie auf **Nein**.
5. Erweitern Sie nach dem Öffnen des Berichts **Datenquellen**, und doppelklicken Sie auf **DataSource1**.
6. Wählen Sie im Fenster **Datenquelleneigenschaften** die Option **In meinem Bericht eingebettete Verbindung verwenden** aus, und klicken Sie dann auf die Schaltfläche **Erstellen...** aus.
7. Wählen Sie im Fenster **Verbindungseigenschaften** die Option **Servername** aus, und geben Sie den Namen des Configuration Manager-Servers ein. Wählen Sie dann unter **Datenbanknamen auswählen oder eingeben** den Namen der Configuration Manager-Datenbank aus der Dropdownliste aus.
8. Klicken Sie auf **OK**, um das **Verbindungseigenschaften**-Fenster zu schließen.
9. Klicken Sie auf **Verbindung testen**, um die Verbindung zu testen. Wenn die Verbindung erfolgreich hergestellt werden konnte, klicken Sie auf **OK**, um das Dialogfeld **Datenquelleneigenschaften** zu schließen.
10. Wiederholen Sie die Schritte 5 bis 9 für **Data Source 2**.
11. Erweitern Sie **Datasets**, und doppelklicken Sie auf **DataSet1**.
12. Klicken Sie im Fenster **Dataseteigenschaften** in das Textfeld **Abfrage:**, und ersetzen Sie **USE CM_A1B** mit dem in Schritt 7 ausgewählten Datenbanknamen.
13. Wiederholen Sie die Schritte 11 bis 12 für **DataSet2**, **DataSet3** und **DataSet4**.
14. Klicken Sie auf Registerkarte **Startseite** des Menübands auf die Schaltfläche **Ausführen**, um den Bericht zu testen.
15. Speichern Sie den Bericht.
16. Schließen Sie den Microsoft Berichts-Generator.
17. Benennen Sie die Datei in **Site Discovery.rdl** um.

### <a name="configure-the-activex-sample-report"></a>Konfigurieren des ActiveX-Beispielberichts

Führen Sie die folgenden Schritte aus, um einen Beispielbericht mit einer einzigen Datenquelle zu erstellen, nämlich den Websites, die ActiveX-Steuerelemente verwenden. Da der Internet Explorer der einzige Browser ist, der ActiveX-Steuerelemente unterstützt, ist für diese Websites möglicherweise der IE-Modus erforderlich.

1. Kopieren Sie den Bericht **SCCM Report Sample - ActiveX.rdl** auf den Configuration Manager-Server.
2. Installieren Sie den [Microsoft Berichts-Generator](/sql/reporting-services/install-windows/install-report-builder?view=sql-server-ver15).
3. Doppelklicken Sie auf **SCCM Report Sample - ActiveX.rdl**, um den Bericht im Berichts-Generator zu öffnen.
4. Wenn Sie den Bericht zum ersten Mal öffnen, versucht er, den Server zu kontaktieren, auf dem er erstellt wurde. Wenn Sie aufgefordert werden, eine **Verbindung mit dem Berichtsserver herzustellen**, klicken Sie auf **Nein**.
5. Erweitern Sie nach dem Öffnen des Berichts **Datenquellen**, und doppelklicken Sie auf **AutoGen__5C6358F2_4BB6_4a1b_A16E_8D96795D8602_**.
6. Wählen Sie im Fenster **Datenquelleneigenschaften** die Option **In meinem Bericht eingebettete Verbindung verwenden** aus, und klicken Sie dann auf die Schaltfläche **Erstellen...** aus.
7. Wählen Sie im Fenster **Verbindungseigenschaften** die Option **Servername** aus, und geben Sie den Namen des Configuration Manager-Servers ein. Wählen Sie dann unter **Datenbanknamen auswählen oder eingeben** den Namen der Configuration Manager-Datenbank aus der Dropdownliste aus.
8. Klicken Sie auf **OK**, um das **Verbindungseigenschaften**-Fenster zu schließen.
9. Klicken Sie auf **Verbindung testen**, um die Verbindung zu testen. Wenn die Verbindung erfolgreich hergestellt werden konnte, klicken Sie auf **OK**, um das Dialogfeld **Datenquelleneigenschaften** zu schließen.
10. Erweitern Sie **Datasets**, und doppelklicken Sie auf **DataSet1**.
11. Klicken Sie im Fenster **Dataseteigenschaften** in das Textfeld **Abfrage:**, und ersetzen Sie **USE CM_A1B** mit dem in Schritt 7 ausgewählten Datenbanknamen.
12. Klicken Sie auf Registerkarte **Startseite** des Menübands auf die Schaltfläche **Ausführen**, um den Bericht zu testen.
13. Speichern Sie den Bericht.
14. Schließen Sie den Microsoft Berichts-Generator.
15. Benennen Sie die Datei in **ActiveX** um.

### <a name="upload-configured-reports-to-microsoft-sql-server-reporting-services"></a>Hochladen konfigurierter Berichte in Microsoft SQL Server Reporting Services

Nachdem Sie die Berichte für Ihre Umgebung konfiguriert haben, laden Sie sie auf den Berichtsserver hoch.

1. Starten Sie die Anwendung **Reporting Services Configuration Manager**.
2. Klicken Sie im Fenster **Berichtsserver-Verbindung** auf **Verbinden**, und klicken Sie dann auf die URL, die unter **Web Portal Site Identification** aufgeführt ist.
3. In dem daraufhin angezeigten Browserfenster sollten Sie sich auf der Seite **SQL Server Reporting Services** befinden; klicken Sie auf den Ordner **ConfigMgr_SCCMSiteCode** für Ihren SCCM-Site-Code.
4. Zeigen Sie im Menüband auf **+Neu**, und klicken Sie auf das **Ordner**-Menüelement.
5. Geben Sie einen Ordnernamen ein, z. B. **Enterprise Site Discovery**, und klicken Sie dann auf die Schaltfläche **Erstellen**.
6. Klicken Sie auf den Ordner **Enterprise Site Discovery**.
7. Klicken Sie im Menüband auf die Schaltfläche **Hochladen**.
8. Wählen Sie den Bericht **Site-Discovery** aus, und klicken Sie auf **OK**.
9. Wiederholen Sie die Schritte 7 und 8 für den **ActiveX**-Bericht.

### <a name="view-reports-in-configuration-manager"></a>Anzeigen von Berichten im Configuration Manager

Nachdem Sie die Berichte angepasst und hochgeladen haben, können Sie sie im Configuration Manager anzeigen.

1. Wählen Sie in der Configuration Manager-Konsole **Überwachung** > **Berichterstellung** > **Berichte** > **Enterprise Site Discovery** aus.
2. Doppelklicken Sie auf einen Bericht, um ihn anzuzeigen.

## <a name="disable-enterprise-site-discovery"></a>Enterprise Site Discovery deaktivieren

Wenn Sie die Datenerfassung abgeschlossen haben, sollten Sie Enterprise Site Discovery deaktivieren. Erstellen Sie ein zweites Paket, um Enterprise Site Discovery in Microsoft Endpoint Configuration Manager zu deaktivieren, wie in der [Dokumentation](/configmgr/apps/deploy-use/packages-and-programs)beschrieben, und wählen Sie die folgenden Optionen aus:

- Wählen Sie auf der Seite **Paket** die Option **Name** aus, und geben Sie den Namen **Site-Discovery deaktivieren** an.
- Aktivieren Sie auf der **Paket**-Seite die Option **Dieses Paket enthält Quelldateien**.
- Geben Sie auf der **Paket**-Seite den Quellordner an, in den Sie die Dateien extrahiert haben (z. B. **\\\\DSL\\EnterpriseSiteDiscovery**)
- Wählen Sie auf der Seite **Programmtyp** die Option **Standardprogramm**.
- Geben Sie auf der Seite **Standardprogramm** die folgende Befehlszeile ein, durch die die Site-Discovery auf dem Gerät deaktiviert wird:
  ```dos
  powershell.exe -ExecutionPolicy Bypass .\IETelemetrySetUp-Win8.ps1 -IEFeatureOff
  ```
- Wählen Sie auf der Seite **Standardprogramm** die Option zum Ausführen **im Hintergrund** aus.
- Wählen Sie auf der Seite **Standardprogramm** unter **Programm kann ausgeführt werden** die Option **Unabhängig von Benutzeranmeldung** aus.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)
- [Informationen zum IE-Modus](./edge-ie-mode.md)
- [Weitere Informationen zum Unternehmensmodus](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [Zusätzliche Informationen zu Enterprise Site Discovery](/internet-explorer/ie11-deploy-guide/collect-data-using-enterprise-site-discovery)