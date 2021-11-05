---
title: Verwaltung von Cloudwebsitelisten für Internet Explorer (IE)-Modus (Öffentliche Vorschau)“
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 11/03/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Erfahren Sie, wie Sie die Verwaltung von Cloudwebsitelisten für den IE-Modus mithilfe des Microsoft 365 Admin Center konfigurieren und verwenden.
ms.openlocfilehash: 29984aa559c0afda5be0457fcbe618dc264a3e68
ms.sourcegitcommit: 4ec03873a85f065d9bfa6203cfe6c3e938f79bc5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2021
ms.locfileid: "12155042"
---
# <a name="cloud-site-list-management-for-ie-mode-public-preview"></a>Verwaltung von Cloudwebsitelisten für den IE-Modus (Öffentliche Vorschau)

In diesem Artikel wird erläutert, wie Sie die Verwaltung von Cloudwebsitelisten für den Internet Explorer (IE)-Modus über das Microsoft 365 Admin Center konfigurieren und verwenden.

## <a name="overview"></a>Übersicht

Während Sie Ihre Workflows und Anwendungen von IE11 in den IE-Modus überführen, können Sie die **Verwaltung von Cloudwebsitelisten** verwenden, um Ihre Websitelisten für den IE-Modus in der Cloud zu verwalten. Sie können mithilfe der **Microsoft Edge-Websitelisten**-Erfahrung im **Microsoft 365 Admin Center** mit Websitelisten arbeiten.

Weitere Informationen finden Sie im Video [Verwaltung von Cloudwebsitelisten für Internet Explorer (IE)-Modus](https://www.youtube.com/watch?v=9-GovDcryXQ).

> [!NOTE]
> Diese Erfahrung befindet sich jetzt in der öffentlichen Vorschau.

In der Vorschauerfahrung können Sie die Websiteliste Ihrer Organisation an einem konformen Cloudspeicherort speichern, anstatt eine lokale Infrastruktur zum Hosten Ihrer Websiteliste zu benötigen. Sie können Websitelisten erstellen, importieren, exportieren und Änderungen an Websitelisteneinträgen über das Microsoft 365 Admin Center überwachen. Sie können mehrere Websitelisten in der Cloud veröffentlichen und Gruppenrichtlinien verwenden, um verschiedenen Gruppen von Geräten die Verwendung unterschiedlicher Listen zuzuweisen.

## <a name="prerequisites"></a>Voraussetzungen

Die folgenden Voraussetzungen gelten für diese öffentliche Vorschau.

1. Kunden müssen über einen Azure AD-Mandanten verfügen.
2. Administratoren müssen Microsoft Edge Version 93 oder höher und die neueste Version der [Richtliniendateien](https://aka.ms/edgeenterprise) installiert haben.
3. Administratoren müssen ein [Microsoft Edge-Administrator](/azure/active-directory/roles/permissions-reference#edge-administrator) oder ein [Globaler Administrator](/azure/active-directory/roles/permissions-reference#global-administrator) für den Mandanten sein, um auf die Microsoft Edge-Websitelistenerfahrung zugreifen zu können.
   - Um die öffentliche Vorschau zu abonnieren, muss ein globaler Administrator den Mandanten für den „gezielten Release“ registrieren. Weitere Informationen finden Sie unter [Abonnieren der öffentlichen Vorschau](#opt-in-to-public-preview).

## <a name="the-preview-experience"></a>Die Vorschauerfahrung

Die Vorschauerfahrung umfasst drei Aspekte.

### <a name="publish-enterprise-site-list-to-the-cloud"></a>Veröffentlichen der Unternehmenswebsiteliste in der Cloud

Administratoren können eine oder mehrere Websitelisten für einen authentifizierten Endpunkt veröffentlichen, welche Microsoft Edge-Clients in ihrem Mandanten für die IE-Modus-Erfahrung herunterladen können. Administratoren können die vorhandene XML-Datei der Unternehmenswebsiteliste in die Microsoft Edge-Websitelisten im Microsoft 365 Admin Center importieren und dann am Cloudspeicherort veröffentlichen. 

### <a name="associate-the-cloud-hosted-site-list-with-microsoft-edge"></a>Zuordnen der in der Cloud gehosteten Websiteliste zu Microsoft Edge

Mit Microsoft Edge Version 93 können Administratoren die Einstellung [InternetExplorerIntegrationCloudSiteList](/docs.microsoft.com/deployedge/microsoft-edge-policies#internetexplorerintegrationcloudsitelist) verwenden, um eine der in der Cloud gehosteten Websitelisten zu konfigurieren, die Microsoft Edge für den IE-Modus nutzen kann. Benutzer müssen bei Microsoft Edge angemeldet sein, damit der Client die Websiteliste aus der Cloud nutzen kann.

> [!IMPORTANT]
> Wenn diese Richtlinie konfiguriert ist, überschreibt sie die ursprüngliche Richtlinie [InternetExplorerIntegrationSiteList](/docs.microsoft.com/deployedge/microsoft-edge-policies#internetexplorerintegrationsitelist).

### <a name="manage-site-list-contents-on-the-microsoft-365-admin-center"></a>Websitelisteninhalte im Microsoft 365 Admin Center verwalten

Administratoren können eine neue Liste erstellen oder eine vorhandene Websiteliste in die Microsoft Edge-Websitelistenerfahrung importieren. Sie können Websitelisteninhalte hinzufügen, bearbeiten, löschen und den Kommentarverlauf anzeigen, um Änderungen an einzelnen Einträgen nachzuverfolgen. Im nächsten Abschnitt wird erläutert, wie Sie die öffentliche Vorschau abonnieren und auf die Microsoft Edge-Websitelistenerfahrung im Microsoft 365 Admin Center zugreifen.

## <a name="opt-in-to-public-preview"></a>Öffentliche Vorschau abonnieren

In der öffentlichen Vorschau müssen Sie die Anzeige der Vorschauerfahrung im Microsoft 365 Admin Center abonnieren. Sie müssen ein globaler Administrator in Microsoft 365 sein, um dies abonnieren zu können.

Verwenden Sie die folgenden Schritte, um zu ändern, wie Ihre Organisation Microsoft 365-Updates erhält.

> [!NOTE]
> Es kann bis zu 24 Stunden dauern, bis die folgenden Konfigurationsänderungen in Microsoft 365 wirksam werden. Wenn Sie das Abonnement für ein gezieltes Release nach der Aktivierung kündigen, verlieren Ihre Benutzer möglicherweise den Zugriff auf Features, die den geplante Release noch nicht erreicht haben.

1. Melden Sie sich beim [Microsoft 365 Admin Center](https://admin.microsoft.com) an, und wechseln Sie dann zu  **Einstellungen > Organisationseinstellung**. Wählen Sie unter der Registerkarte  **Organisationsprofil** die Option **Release-Voreinstellungen** aus.
2. Um das gezielte Release zu deaktivieren, wählen Sie  **Standardrelease** und dann  **Änderungen speichern** aus.
3. Um das gezielte Release für alle Benutzer in Ihrer Organisation zu aktivieren, wählen Sie **Gezieltes Release für alle Benutzer** aus, und wählen Sie dann **Änderungen speichern** aus.
4. Um das gezielte Release für einige Personen in Ihrer Organisation zu aktivieren, wählen Sie **Gezieltes Release für ausgewählte Benutzer** und dann  **Änderungen speichern** aus.
5. Wählen Sie **Benutzer auswählen** aus, um Benutzer einzeln hinzufügen, oder  **Benutzer hochladen** , um sie in großen Mengen hinzuzufügen.
6. Wenn Sie mit dem Hinzufügen von Benutzern fertig sind, wählen Sie  **Änderungen speichern** aus.

Weitere Informationen finden Sie unter [Einrichten der Standard- oder gezielten Releaseoptionen – Microsoft 365 Admin](/microsoft-365/admin/manage/release-options-in-office-365)

## <a name="publish-enterprise-site-list-to-the-cloud"></a>Veröffentlichen der Unternehmenswebsiteliste in der Cloud

Verwenden Sie die folgenden Schritte als Leitlinie, um eine Websiteliste zu erstellen, eine Websiteliste zu importieren und die Websiteliste zu veröffentlichen. Bevor Sie diese Schritte durchführen können, melden Sie sich beim Microsoft 365 Admin Center an.

1. Melden Sie sich beim [Microsoft 365 Admin Center](https://admin.microsoft.com) mit Ihren Administratoranmeldeinformationen an.
2. Wählen Sie im linken Navigationsbereich **Einstellungen > Organisationseinstellungen**.
3. Sie werden die Option **Microsoft Edge-Websitelisten (Vorschau)** sehen.

### <a name="steps-to-create-a-site-list"></a>Schritte zum Erstellen einer Websiteliste

1. Wählen Sie auf der Seite „Organisationseinstellungen“ die Option **Microsoft Edge-Websitelisten (Vorschau)** aus.
2. Wählen Sie auf der resultierenden Seite die Option **Erstellen einer neuen Liste** aus.
3. Geben Sie einen **Websitelistennamen** und eine **Beschreibung** ein, und wählen Sie dann **Erstellen** aus.
4. Nachdem Sie die Bestätigung erhalten haben, wählen Sie **Bereich schließen** aus. 

### <a name="steps-to-import-a-site-list"></a>Schritte zum Importieren einer Websiteliste

1. Wählen Sie die Websiteliste aus, die Sie auffüllen möchten.
2. Wählen Sie auf der resultierenden Seite **Liste importieren** aus.
3. Wählen Sie im rechten Bereich **Browsen** aus.
4. Wählen Sie die Datei aus, die Sie importieren möchten, und wählen Sie dann unten im Bereich **Hochladen** aus.
5. Sie können die URLs in der hochgeladenen Datei überfliegen. Wenn Sie eine andere Datei auswählen möchten, können Sie oben im Bereich **Hochladen einer anderen Datei** auswählen. Wenn alles richtig aussieht, wählen Sie **Hinzufügen** am unteren Rand des Bereichs aus.
6. Nachdem Ihre Liste importiert wurde, wählen Sie **Bereich schließen** aus. 

### <a name="steps-to-publish-a-site-list"></a>Schritte zum Veröffentlichen einer Websiteliste

1. Um eine Websiteliste zu veröffentlichen, wechseln Sie zurück zur Seite „Microsoft Edge-Websitelisten“. Wählen Sie den Breadcrumb über dem Namen der Websiteliste aus, um eine Ebene nach oben zu wechseln.
2. Wählen Sie auf der Seite „Microsoft Edge-Websitelisten“ die Websiteliste aus, die Sie in der Cloud veröffentlichen möchten, und wählen Sie dann **Websiteliste veröffentlichen** aus.
3. Aktualisieren Sie im rechten Bereich die **Versionsnummer**, und wählen Sie unten im Bereich **Veröffentlichen** aus.
4. Wählen Sie nach der Bestätigung **Bereich schließen** aus. 
5. Die Spalten **Status der Veröffentlichung**, **Zuletzt veröffentlicht** und **Zuletzt veröffentlicht durch** werden alle aktualisiert.

## <a name="associate-the-cloud-hosted-site-list-with-microsoft-edge"></a>Zuordnen der in der Cloud gehosteten Websiteliste zu Microsoft Edge

Verwenden Sie die folgenden Schritte, um die in der Cloud gehostete Websiteliste an Microsoft Edge zuzuordnen.

1. Um Geräte für die Verwendung einer veröffentlichten Websiteliste zu konfigurieren, klicken Sie auf die Websiteliste, die Sie Geräten zuweisen möchten.
2. Kopieren Sie auf der resultierenden Seite die **Websitelisten-ID**.
3. Wählen Sie für die von Ihnen ausgewählte Gerätegruppe **Aktiviert** aus, und geben Sie die **Websitelisten-ID** in die Richtlinie [Konfiguration der Unternehmensmodus-Cloudwebsiteliste](/deployedge/microsoft-edge-policies#internetexplorerintegrationcloudsitelist) ein.
4. Sie können **gpupdate/force** über die Eingabeaufforderung ausführen, um das Gerät mit der Richtlinie zu aktualisieren, oder warten, bis die Gruppenrichtlinie wirksam wird. Nachdem die Richtlinie aktualisiert wurde, können Sie überprüfen, ob Microsoft Edge die Cloudwebsiteliste liest, indem Sie zu [edge://compat/enterprise](edge://compat/enterprise) wechseln. Sie müssen bei Microsoft Edge angemeldet sein.

> [!NOTE]
> Nachdem Sie eine Websiteliste zum ersten Mal veröffentlicht und die Gruppenrichtlinie aktualisiert haben, müssen Sie Microsoft Edge neu starten. Warten Sie 60 Sekunden, oder wählen Sie unter [edge://compat/enterprise](edge://compat/enterprise) die Schaltfläche „Aktualisierung erzwingen“ aus. Beim Veröffentlichen von Aktualisierungen für eine bereits zugeordnete Websiteliste befindet sich möglicherweise eine ältere Version der Websiteliste im Cache. Dieser Eintrag wird nach 60 Sekunden aktualisiert. Weitere Informationen finden Sie unter [Was geschieht, wenn sich Benutzer bei Microsoft Edge abmelden?](#what-happens-if-users-log-out-of-microsoft-edge)

## <a name="manage-site-list-contents-on-the-microsoft-365-admin-center"></a>Websitelisteninhalte im Microsoft 365 Admin Center verwalten

Sie können einzelne Websiteeinträge hinzufügen, Websiteeinträge löschen und den Änderungsverlauf für Kommentare anzeigen.
Wenn Sie hybride Szenarien haben, die erfordern, dass Ihre Websiteliste lokal gehostet werden muss, können Sie Ihre Websiteliste aus dem Microsoft 365 Admin Center exportieren. Verwenden Sie die folgenden Schritte als Leitlinie zum Verwalten von Websitelisteninhalten aus.

### <a name="add-individual-sites-to-the-site-list"></a>Hinzufügen einzelner Websites zur Websiteliste

Sie können jeder Websiteliste einzelne Websites hinzufügen. Nach dem Hinzufügen von Websites zur Liste können Sie die vordefinierten Filter mithilfe der Schaltfläche **Filter** (neben dem Eingabebereich der Suche) verwenden, um Aktualisierungen der Liste anzuzeigen.

1. Wechseln Sie zur Websiteliste, in der Sie eine Website hinzufügen möchten.
2. Wählen Sie **Website hinzufügen** aus.
3. Geben Sie die Websiteadresse ein, und wählen Sie das Modul aus, das zum Öffnen der Website verwendet werden soll. Fügen Sie bei Bedarf Kommentare hinzu, und wählen Sie **Speichern** aus.

   > [!NOTE]
   > In der Spalte **Status** für alle Einträge, die einer Liste veröffentlichter Websites hinzugefügt werden, wird **Hinzufügen ausstehend** angezeigt. Wenn Sie zur Liste der Websitelisten navigieren, indem Sie oben auf dem Bildschirm **Microsoft Edge-Websitelisten** auswählen, sehen Sie, dass in der Spalte **Status der Veröffentlichung** der Wert **Änderungen warten auf die Veröffentlichung** angezeigt wird, um darauf hinzuweisen, dass die neuesten Aktualisierungen der Websiteliste veröffentlicht werden müssen, damit Benutzer Sie erhalten können. Sie können die Schaltfläche **Filter** _(neben dem Suchfeld)_ verwenden, um „Hinzufügen ausstehend“ auszuwählen, um alle hinzugefügten Einträge anzuzeigen, für die eine Veröffentlichung ausstehen.

### <a name="view-the-change-history-for-site-entries"></a>Anzeigen des Änderungsverlaufs für Websiteeinträge

1. Wählen Sie den Websiteeintrag aus, für den Sie den Änderungsverlauf anzeigen möchten, und wählen Sie dann **Kommentare anzeigen** aus.

### <a name="delete-a-site-from-the-site-list"></a>Löschen einer Website aus der Websiteliste

Verwenden Sie die folgenden Schritte, um einen Websiteeintrag zu löschen.

1. Wählen Sie den Eintrag für die Websiteliste aus, aus der Sie eine Website löschen möchten. Wählen Sie **Website löschen** aus.
2. Wählen Sie unten im Bereich **Löschen** aus.
3. Nachdem Sie die Bestätigung erhalten haben, dass ein Websiteeintrag gelöscht wurde, bleibt er in der Liste, bis die Websiteliste am Cloudspeicherort veröffentlicht wird. Sie können die Liste der gelöschten Websites vor der Veröffentlichung anzeigen, indem Sie die Schaltfläche „Filter“ auswählen und nach Websites mit Status **Löschen ausstehend** filtern.

   > [!NOTE]
   > In der Spalte **Status** für alle Einträge, die aus einer Liste veröffentlichter Websites gelöscht wurden, wird **Löschen ausstehend** angezeigt. Wenn Sie zur Liste der Websitelisten navigieren, indem Sie oben auf dem Bildschirm **Microsoft Edge-Websitelisten** auswählen, sehen Sie, dass in der Spalte **Status der Veröffentlichung** der Wert **Änderungen warten auf die Veröffentlichung** angezeigt wird, um darauf hinzuweisen, dass die neuesten Aktualisierungen der Websiteliste veröffentlicht werden müssen, damit Benutzer Sie erhalten können. Sie können die Schaltfläche **Filter** _(neben dem Suchfeld)_ verwenden, um „Löschen ausstehend“ auszuwählen, um alle gelöschten Einträge anzuzeigen, deren Veröffentlichung aussteht.

### <a name="export-a-site-list"></a>Exportieren einer Websiteliste

Es gibt Szenarien, in denen Sie eine Websiteliste exportieren möchten. Beispielsweise, wenn Sie Ihre Websiteliste nicht sofort in die Cloud verschieben können oder wenn Sie eine Hybridumgebung mit Websitelisten in der Cloud und lokal verwalten müssen. Sie können die Verwaltungserfahrung für Cloudwebsitelisten verwenden, um Aktualisierungen für eine Websiteliste an einem zentralen Ort zu verwalten und die Websiteliste auf den lokalen Host zu exportieren.

1. Wählen Sie auf der Seite „Microsoft Edge-Websitelisten“ die Websiteliste aus, die Sie exportieren möchten.
2. Auf der resultierenden Seite werden die Websitelisteneinträge und die Option **Liste exportieren** angezeigt.
3. Wählen Sie **Liste exportieren** aus, um die XML-Datei der Websiteliste herunterzuladen.

## <a name="faq"></a>FAQ

### <a name="when-i-select-microsoft-edge-site-lists-and-try-to-create-a-new-list-i-get-this-error---request-failed-with-status-code-500-why-is-that"></a>Wenn ich „Microsoft Edge-Websitelisten“ auswähle und versuche, eine neue Liste zu erstellen, erhalte ich diesen Fehler: „Anforderung mit Statuscode 500 fehlgeschlagen“. Weshalb?

„Microsoft Edge-Websitelisten“ speichert ihre Daten und Konfiguration in einer Dienstinfrastruktur, die mit Unternehmensclouddiensten wie Exchange Online, SharePoint Online, Teams und Azure Active Directory gemeinsam genutzt wird. In seltenen Fällen kann die Bereitstellung einige Zeit in Anspruch nehmen, wenn Microsoft Edge-Websitelisten das erste Feature ist, das diese Infrastruktur verwendet. In diesen Fällen schlägt die anfängliche Anforderung aus dem Microsoft 365 Admin Center fehl. Wenn die Anforderung fehlschlägt, wird eine Warnung an das Bereitstellungssystem gesendet, um das Problem zu beheben. Die Bereitstellung wird in der Regel in drei Tagen abgeschlossen. Wenn dieser Fehler angezeigt wird, versuchen Sie es in einigen Tagen erneut, und erstellen Sie eine neue Liste. Wenn Sie immer noch keine neue Liste erstellen können oder dringende Unterstützung benötigen, wenden Sie sich an den Microsoft-Support.

### <a name="can-users-who-havent-signed-in-to-microsoft-edge-download-the-site-list"></a>Können Benutzer, die nicht bei Microsoft Edge angemeldet sind, die Websiteliste herunterladen?

Nein, Benutzer müssen sich beim Browser anmelden, um die Liste der in der Cloud gehosteten Websites herunterzuladen. Sie können eine Richtlinie so konfigurieren, dass die implizite Anmeldung zugelassen wird, um eine Unterbrechung der Benutzererfahrung zu verhindern. Weitere Informationen finden Sie unter [ImplicitSignInEnabled](/docs.microsoft.com/DeployEdge/microsoft-edge-policies#implicitsigninenabled).

### <a name="what-is-the-default-refresh-interval-after-updates-are-made-to-site-list-contents"></a>Was ist das Standardaktualisierungsintervall, nachdem Aktualisierungen an Websitelisteninhalten vorgenommen wurden?

Die Websiteliste wird alle zwei Stunden in Microsoft Edge aktualisiert. Sie können dieses Intervall über die Richtlinie [NavigationDelayForInitialSiteListDownloadTimeout](/docs.microsoft.com/deployedge/microsoft-edge-policies#navigationdelayforinitialsitelistdownloadtimeout) ändern. Das minimale Aktualisierungsintervall beträgt 30 Minuten.

### <a name="what-happens-if-users-log-out-of-microsoft-edge"></a>Was geschieht, wenn sich Benutzer bei Microsoft Edge abmelden?

Für den Zugriff auf die Websiteliste ist eine explizite Browseranmeldung für den ersten Download erforderlich. In einem Szenario, in dem sich der Benutzer nach der Anmeldung wieder abmeldet, wird die Websiteliste in Microsoft Edge zwischengespeichert. Die Liste bleibt auch dann zwischengespeichert, wenn sich der Benutzer von Microsoft Edge aus dem Azure Active Directory (Azure AD)-Konto abmeldet. Microsoft Edge wird nicht versuchen, auf den Nicht-Cloud-Downloadspeicherort zurückzugreifen, solange die Richtlinie für die Cloudwebsiteliste konfiguriert ist. Microsoft Edge versucht, die zwischengespeicherte Websiteliste zu den folgenden Zeiten zu aktualisieren (beachten Sie, dass alle Versuche fehlschlagen, wenn der Benutzer nicht bei Microsoft Edge angemeldet ist):

- 60 Sekunden nach dem Neustart des Browsers. Wenn die Startverzögerung von 60 Sekunden kürzer sein muss, können Sie die Richtlinie [NavigationDelayForInitialSiteListDownloadTimeout](/deployedge/microsoft-edge-policies#navigationdelayforinitialsitelistdownloadtimeout) verwenden, um die Verzögerung zu ändern.
- Alle zwei Stunden, wenn Microsoft Edge ausgeführt wird.

## <a name="support-and-feedback"></a>Support und Feedback

Während der öffentlichen Vorschau wird die Verwaltungserfahrung für Cloudwebsitelisten durch Ihren vorhandenen [Microsoft Premier-Support](https://www.microsoft.com/en-us/unifiedsupport/premier)-Vertrag abgedeckt. Sie können sich an den Microsoft-Support wenden, um Probleme oder Feedback zu melden. Feedback können Sie auch in unserem [TechCommunity-Forum](https://techcommunity.microsoft.com/t5/enterprise/bd-p/EdgeInsiderEnterprise) hinterlassen.

## <a name="see-also"></a>Weitere Informationen

- [Informationen zum IE-Modus](./edge-ie-mode.md)
- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)
  
