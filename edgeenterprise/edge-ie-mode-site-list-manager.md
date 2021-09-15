---
title: 'Enterprise Site List Manager in Microsoft Edge '
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: 'Aktivieren und Verwenden des Enterprise Site List Managers in Microsoft Edge '
ms.openlocfilehash: add635a17d05cb4be94e710fd99ab480b992a579
ms.sourcegitcommit: 8968f3107291935ed9adc84bba348d5f187eadae
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/12/2021
ms.locfileid: "11979233"
---
# <a name="enterprise-site-list-manager-in-microsoft-edge"></a>Enterprise Site List Manager in Microsoft Edge

>[!Note]
> Die Internet Explorer 11-Desktopanwendung wird eingestellt und wird ab dem 15. Juni 2022 nicht mehr unterstützt (eine Liste der in diesem Bereich enthaltenen Elemente [finden Sie in den FAQ](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549)). Dieselben IE11-Apps und -Websites, die Sie heute verwenden, können in Microsoft Edge im Internet Explorer-Modus geöffnet werden. [Weitere Informationen finden Sie hier](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/).

In diesem Artikel wird erläutert, wie Sie den Zugriff auf und die Verwendung des Enterprise Site List Managers in Microsoft Edge zum Erstellen, Bearbeiten und Exportieren Ihrer Websiteliste für den Unternehmensmodus für Internet Explorer-Modus aktivieren.

> [!NOTE]
> Dieser Artikel bezieht sich auf Microsoft Edge Version 89 oder höher. 

## <a name="overview"></a>Übersicht

Der Enterprise Site List Manager ist eine Browserversion des [eigenständigen Enterprise Mode Site List Manager-Tools](https://www.microsoft.com/download/details.aspx?id=49974), mit dem Sie die Websiteliste Ihres Unternehmens erstellen, bearbeiten und exportieren können.

Zukünftige Verbesserungen am Tool für den Internet Explorer-Modus werden über den Enterprise Site List Manager in Microsoft Edge verfügbar sein. Das eigenständige Tool ist weiterhin im Download-Center verfügbar, es wird jedoch keine weiteren Feature-Updates erhalten.

## <a name="enabling-access-to-enterprise-site-list-manager"></a>Aktivieren des Zugriffs auf den Enterprise Site List Manager

Sie können den Zugriff auf das Tool mithilfe der Gruppenrichtlinie [EnterpriseModeSiteListManagerAllowed](./microsoft-edge-policies.md#enterprisemodesitelistmanagerallowed) konfigurieren.

Wenn diese Option aktiviert ist, werden die Benutzer eine Option mit Namen „Enterprise Site List Manager“ im linken Navigationsbereich in *edge://compat* sehen. Wenn deaktiviert, werden die Benutzer der Einstiegspunkt für den Enterprise Site List Manager im linken Navigationsbereich nicht sehen. Dies ist das standardmäßige Verhalten.

## <a name="using-the-enterprise-site-list-manager"></a>Verwenden des Enterprise Mode Site List Managers

Das Enterprise Site List Manager-Tool verwendet die Version v.2 des Schemas. Wenn Sie ein Schema der Version v.1 in den Enterprise Site List Manager (Schema v.2) importieren, wird der XML-Code in der Version v.2 des Schemas gespeichert. Siehe [Anleitung für das Schema v.2 für den Unternehmensmodus](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).

### <a name="add-single-sites-to-your-site-list"></a>Hinzufügen einzelner Websites zu Ihrer Websiteliste  

Verwenden Sie die folgenden Schritte, um Ihrer Websiteliste einzelne Websites hinzuzufügen.

> [!NOTE]
> Sie können nur bestimmte URLs, jedoch keine Internet- oder Intranetzonen hinzufügen.

1. Klicken Sie im Enterprise Site List Manager auf **Website hinzufügen**.
2. Geben Sie die URL für die Website, die Sie hinzufügen möchten, in das URL-Feld ein, z. B.:  <domain>.com oder <domain>.com/<path> .
3. Wählen Sie eine der folgenden Optionen in der **Öffnen mit** -Liste aus:

   - **IE11**. Öffnet die Website in der IE11-Anwendung.
   - **IE-Modus**. Öffnet die Website im Internet Explorer-Modus auf Microsoft Edge, falls aktiviert, andernfalls in der IE11-App. Siehe [Internet Explorer-Modus auf Microsoft Edge](./edge-ie-mode.md).
   - **MSEdge**. Öffnet die Website in Microsoft Edge.
   - **Konfigurierbar**. Ermöglicht der Website die Teilnahme an der Engine-Bestimmung im IE-Modus. Siehe [Konfigurierbare Websites im IE-Modus](./edge-learnmore-configurable-sites-ie-mode.md)
   - **Keine**. Wird im vom Benutzer ausgewählten Browser geöffnet.  

4. Wählen Sie unter  **Kompatibilitätsmodus**eine der folgenden Optionen aus:

   - **IE8Enterprise**. Lädt die Website im IE8-Unternehmensmodus.
   - **IE7Enterprise**. Lädt die Website im IE7-Unternehmensmodus.
   - **IE[x]**. Dabei ist [x] die Dokumentmodus-Ziffer, und die Website wird im angegebenen Dokumentmodus geladen.
   - **Standardmodus**. Lädt die Website im Standardkompatibilitätsmodus für die Seite.

   Der Pfad innerhalb einer Domäne erfordert unter Umständen einen anderen Kompatibilitätsmodus als die Domäne. Die Domäne wird im IE11-Standardbrowser möglicherweise ordnungsgemäß angezeigt, beim Pfad treten jedoch unter Umständen Probleme auf, und die Verwendung des Unternehmensmodus ist erforderlich. Falls Sie die Domäne bereits hinzugefügt haben, ist Ihre ursprüngliche Kompatibilitätsauswahl immer noch ausgewählt. Wenn die Domäne jedoch neu ist, wird automatisch  **IE8-Unternehmensmodus**  ausgewählt.

   Der Unternehmensmodus hat Vorrang vor den Dokumentmodi. Daher wirkt sich das Update nicht auf Websites aus, die bereits in der Websiteliste für den Unternehmensmodus enthalten sind. Diese Websites werden weiter wie gewohnt im Unternehmensmodus geladen. Ausführlichere Informationen zur Verwendung von Dokumentmodi finden Sie unter  [Beheben von Webkompatibilitätsproblemen mithilfe von Dokumentmodi und der Websiteliste für den Unternehmensmodus](/internet-explorer/ie11-deploy-guide/fix-compat-issues-with-doc-modes-and-enterprise-mode-site-list).

5. Das Kontrollkästchen **Weiterleitung zulassen** gilt für die Behandlung von serverseitigen Weiterleitungen. Wenn Sie dieses Kontrollkästchen aktivieren, werden serverseitige Weiterleitungen in dem durch das „Öffnen mit“-Tag angegebenen Browser geöffnet. Weitere Informationen finden Sie  [hier](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance#updated-schema-attributes).
6. Geben Sie Kommentare zur Website in das Feld **Kommentar** ein. Administratoren können Kommentare nur sehen, während sie sich in diesem Tool befinden, und diese Kommentare werden in der XML-Websiteliste beibehalten.
7. Klicken Sie auf  **Hinzufügen** um die Website Ihrer Websiteliste hinzuzufügen.

### <a name="export-site-list-to-xml"></a>Exportieren einer Websiteliste nach XML

Nachdem Sie Ihre Websiteliste im Enterprise Site List Manager erstellt haben, können Sie den Inhalt in eine Unternehmensmodus- (.EMIE) oder XML-Datei exportieren. 

> [!NOTE]
> Diese Datei enthält alle Ihre URLs sowie die jeweilige Auswahl für den Kompatibilitätsmodus und sollte an einem sicheren Ort gespeichert werden.

Führen Sie die folgenden Schritte aus, um die Websiteliste zu exportieren:

1. Klicken Sie im Enterprise Site List Manager auf **Nach XML exportieren**.
2. Geben Sie eine **Versionsnummer** und einen **Dateinamen** ein.
3. Klicken Sie auf **Exportieren**.

Sie können die Datei lokal oder auf einer Netzwerkfreigabe speichern. Beachten Sie jedoch, dass die Datei an dem Ort bereitgestellt werden muss, den Sie in Ihrem Registrierungsschlüssel angegeben haben. Weitere Informationen finden Sie unter [Aktivieren des Internet Explorer-Modus und Verwenden einer Websiteliste](./edge-ie-mode-policies.md).

### <a name="import-multiple-sites-to-your-site-list"></a>Importieren mehrerer Websites in Ihre Websiteliste

Nachdem Sie Ihre XML-Datei erstellt haben, können Sie mehrere Websites gleichzeitig mithilfe von **Aus XML importieren** zum Editor hinzufügen.

Wenn Sie alle Inhalte im Editor ersetzen möchten, klicken Sie auf die Auslassungspunkte (...) und dann auf **Liste löschen**. Nachdem Sie den Editor geleert haben, verwenden Sie die folgenden Schritte, um die Website zu importieren.

1. Klicken Sie im Enterprise Site List Manager auf **Aus XML importieren**. 
2. Klicken Sie auf **Datei auswählen**, um Ihre Websiteliste auszuwählen, um dem Tool die enthaltenen Websites hinzuzufügen. Wählen Sie die Websiteliste aus, die Sie hinzufügen möchten, und klicken Sie dann auf **Öffnen**. Unterstützte Formate für den Import sind XML, EMIE oder TXT, die das Schema v.2 für die Websiteliste für den Unternehmensmodus enthalten. Siehe [Anleitung für das Schema v.2 für den Unternehmensmodus](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).
3. Klicken Sie auf  **Laden**, um die Websites aus der Datei zum Editor hinzuzufügen.

Sie können die Datei lokal oder auf einer Netzwerkfreigabe speichern. Beachten Sie jedoch, dass die Datei an dem Ort bereitgestellt werden muss, den Sie in Ihrem Registrierungsschlüssel angegeben haben. Weitere Informationen finden Sie unter [Aktivieren des Internet Explorer-Modus und Verwenden einer Websiteliste](./edge-ie-mode-policies.md).

### <a name="edit-sites-in-your-site-list"></a>Bearbeiten von Websites in Ihrer Websiteliste

 Sie können Attribute vorhandener Website-Einträge im Enterprise Site List Manager bearbeiten. Sie können ebenfalls zugehörige Kommentare hinzufügen, entfernen oder löschen.

1. Klicken Sie im Enterprise Site List Manager auf die Auslassungspunkte (...) und wählen Sie **Website bearbeiten** für die URL aus, die Sie bearbeiten möchten.
2. Sie können außer der URL jedes Attribut des Website-Eintrags bearbeiten. Klicken Sie auf **Speichern**, nachdem Sie die Bearbeitung abgeschlossen haben.

   > [!NOTE]
   > Wenn Sie einen Website-Eintrag löschen möchten, wählen Sie in Schritt 1 **Website löschen** aus.

3. Klicken Sie auf **Nach XML exportieren**, und speichern Sie die aktualisierte Datei.

Sie können die Datei lokal oder auf einer Netzwerkfreigabe speichern. Beachten Sie jedoch, dass die Datei an dem Ort bereitgestellt werden muss, den Sie in Ihrem Registrierungsschlüssel angegeben haben. Weitere Informationen finden Sie unter [Aktivieren des Internet Explorer-Modus und Verwenden einer Websiteliste](./edge-ie-mode-policies.md).

### <a name="preview-your-site-list-in-xml-format"></a>Anzeigen der Vorschau Ihrer Websiteliste im XML-Format

Sie können eine Vorschau der Websites im Editor im XML-Format anzeigen, bevor Sie diese exportieren und an Ihrem Speicherort für die Websiteliste speichern. Klicken Sie auf **XML-Vorschau**, um die Datei auf einer neuen Registerkarte zu öffnen.

### <a name="search-in-the-enterprise-site-list-manager"></a>Suchen im Enterprise Site List Manager

Sie können mit einem Suchvorgang überprüfen, ob eine bestimmte Website bereits in Ihrer Websiteliste enthalten ist, damit Sie nicht versuchen, diese erneut hinzufügen.

Geben Sie zum Durchsuchen einen Teil der URL in das Suchfeld  **Websites nach URL filtern** in der oberen rechten Ecke des Editors ein.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)
- [Informationen zum IE-Modus](./edge-ie-mode.md)
- [Anleitungen für das Unternehmensmodusschema V.2](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance)
- [Weitere Informationen zum Unternehmensmodus](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)