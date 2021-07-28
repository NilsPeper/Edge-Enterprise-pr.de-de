---
title: Microsoft Edge-Erweiterungen zum Selbsthosten
ms.author: aspoddar
author: AndreaLBarr
manager: balajek
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Erfahren Sie, wie Sie Microsoft Edge-Erweiterungen im Unternehmen verpacken und selbst hosten.
ms.openlocfilehash: 8b0e9ed346848f7ee9330c51f6a1c9274df89371
ms.sourcegitcommit: 9088e839e82d80c72460586e9af0610c6ca71b83
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/23/2021
ms.locfileid: "11676112"
---
# <a name="self-host-microsoft-edge-extensions"></a>Microsoft Edge-Erweiterungen zum Selbsthosten

Dieser Artikel enthält grundlegende Anleitungen zum Verpacken einer Erweiterung, die in Ihrem eigenen Webstore gehostet werden soll. Ebenso enthält er Anweisungen zum Bereitstellen von Erweiterungen für Geräte und Benutzer in Ihrer Organisation.

## <a name="prerequisites"></a>Voraussetzungen

Um Ihre eigenen Erweiterungen selbst zu hosten, müssen Sie Ihre eigenen Webhosting-Dienste für die Erweiterungen und deren Anwendungsmanifestdateien bereitstellen.

 Bei den folgenden Schritten wird davon ausgegangen, dass Sie Ihre Erweiterung bereits erstellt haben, Erfahrung mit XML-Dateien haben, über praktische Kenntnisse in der Konfiguration von Gruppenrichtlinien verfügen und wissen, wie Sie die Windows-Registrierung verwenden.

## <a name="publish-an-extension"></a>Veröffentlichen einer Erweiterung

Bevor Sie eine Erweiterung veröffentlichen, muss sie in eine CRX-Datei (Chrome-Erweiterungsdatei) verpackt werden. Führen Sie die folgenden anleitenden Schritte zum Verpacken einer Erweiterung als CRX-Datei aus.

1. Wechseln Sie in der Microsoft Edge-Adressleiste zu *edge://extensions* und aktivieren Sie den **Entwicklermodus**, falls er noch nicht aktiviert ist.
2. Klicken Sie unter **Installierte Erweiterungen** auf **Erweiterung verpacken**, um die CRX-Datei zu erstellen.
3. Verwenden Sie das Dialogfeld **Erweiterung verpacken**, um das Verzeichnis zu finden, das die Quelle für die Erweiterung enthält. Wählen Sie das Verzeichnis aus und klicken Sie dann auf **Erweiterung verpacken**.  Dadurch wird Ihre CRX-Datei zusammen mit einer PEM-Datei erstellt. Speichern Sie die PEM-Datei, denn sie wird für Versionsupdates der Erweiterung benötigt. Der nächste Screenshot zeigt das Dialogfeld **Erweiterung verpacken** zum Auffinden des Stammverzeichnisses der Erweiterung.

   :::image type="content" source="media/microsoft-edge-manage-extensions-webstore/manage-extensions-pack-dialog.png" alt-text="Dialogfeld Erweiterung verpacken, zum Auffinden des Quellcodes einer Erweiterung.":::

   > [!IMPORTANT]
   > Speichern Sie die PEM-Datei an einem sicheren Ort, da sie der Schlüssel für die Erweiterung ist und für zukünftige Updates benötigt wird.

4. Bewegen Sie die CRX-Datei in Ihr Erweiterungsfenster und stellen Sie sicher, dass sie geladen wird.
5. Testen Sie die Erweiterung und notieren Sie sich das ID-Feld (das ist die CRX-ID) und die Versionsnummer. Sie benötigen diese Informationen später. Der nächste Screenshot zeigt eine Testerweiterung mit ihrer CRX-ID.

   :::image type="content" source="media/microsoft-edge-manage-extensions-webstore/manage-extensions-test-extension.png" alt-text="Erweiterungsbeispiel mit CRX-ID":::

6. Laden Sie die CRX-Datei auf den Host hoch und notieren Sie sich die URL des Speicherorts, von dem sie heruntergeladen wird. Diese Informationen werden für die XML-Anwendungsmanifestdatei benötigt.
7. Um eine Anwendungsmanifest-XML-Datei mit der App-/Erweiterungs-ID, der Download-URL und der Version zu erstellen, definieren Sie die folgenden Felder:  

   - **appid** – Die Erweiterungs-ID aus Schritt 5
   - **codebase** – Der Downloadspeicherort für die CRX-Datei aus Schritt 6
   - **version** – Die Version der App/Erweiterung, die mit der im Anwendungsmanifest der Erweiterung angegebenen Version übereinstimmen sollte.

   Der nächste Codeausschnitt zeigt ein Beispiel für eine XML-Anwendungsmanifestdatei.

   ```xml
   <?xml version='1.0' encoding='UTF-8'?> 
   <gupdate xmlns='http://www.google.com/update2/response' protocol='2.0'> 
     <app appid='ekilpdeokbpjmminmhfcgkncmmohmfeb'> 
     <updatecheck codebase='https://app.somecompany.com/extensionfolder/helloworld.crx' version='1.0' /> 
     </app> 
   </gupdate> 
   ```

   Weitere Informationen finden Sie unter [AutoUpdate-Erweiterungen in Microsoft Edge – Microsoft Edge Development](/microsoft-edge/extensions-chromium/enterprise/auto-update).

8. Laden Sie die fertige XML-Datei an einen Speicherort hoch, von dem sie heruntergeladen werden kann, und notieren Sie sich die URL. Diese URL wird benötigt, wenn Sie die Erweiterung mithilfe einer Gruppenrichtlinie installieren. Informationen unter [Verteilen einer privat gehosteten Erweiterung](#distribute-a-privately-hosted-extension).

   > [!IMPORTANT]
   > Der Hosting-Standort für die Erweiterung erfordert keine Authentifizierung. Er muss für Benutzergeräte zugänglich sein, wo immer diese verwendet werden.

## <a name="publish-updates-to-an-extension"></a>Veröffentlichen von Updates für eine Erweiterung

Nachdem Sie die aktualisierte Erweiterung geändert und getestet haben, können Sie diese veröffentlichen. Führen Sie die folgenden anleitenden Schritte für die Veröffentlichung eines Updates aus.

1. Ändern Sie die Versionsnummer in Ihrer Erweiterungsdatei manifest.JSON mit der folgenden Syntax in eine höhere Nummer: `"version":"versionString"`. Wenn es sich um "version":"1.0" handelt, können Sie auf "version":"1.1" oder eine beliebige Zahl höher als "1.0" aktualisieren.
2. Aktualisieren Sie die "Version" von `<updatecheck>` in der XML-Datei, damit sie mit der Nummer übereinstimmt, die Sie im vorherigen Schritt in die Anwendungsmanifestdatei eingegeben haben. Beispiel:<br>`<updatecheck codebase='https://app.somecompany.com/extensionfolder/helloworld.crx' version='1.1' />`
3. Erstellen Sie eine CRX-Datei, welche die neuen Änderungen enthält. Wechseln Sie zu *edge://extensions,* und aktivieren Sie **den Entwicklermodus**.
4. Klicken Sie auf **Erweiterung verpacken** und wechseln Sie für die Erweiterungsquelle zum Verzeichnis.

   > [!IMPORTANT]
   > Verwenden Sie dieselbe PEM-Datei, die beim ersten Erstellen der CRX-Datei generiert und gespeichert wurde. Wenn Sie nicht dieselbe PEM-Datei verwenden, ändert sich die App-ID der Erweiterung und das Update wird als neue Erweiterung behandelt.

5. Bewegen Sie die CRX-Datei in das Erweiterungsfenster und legen Sie diese dort ab, und stellen Sie sicher, dass sie geladen wird. Die Erweiterung wird nach diesem Vorgang deaktiviert. Zum Aktivieren fügen Sie die CRX-ID der Erweiterung der ExtensionInstallAllowList-Richtlinie hinzu. 
6. Testen Sie die aktualisierte Erweiterung.
7. Ersetzen Sie für die aktualisierte Erweiterung die alten CRX-und XML-Dateien durch die neuen Dateien.

Die Änderungen der Erweiterung werden während des nächsten Richtliniensynchronisierungszyklus übernommen. Weitere Informationen zum Aktualisieren von Erweiterungen finden Sie unter: [URL aktualisieren](/microsoft-edge/extensions-chromium/enterprise/auto-update#update-url) und [Anwendungsmanifest aktualisieren](/microsoft-edge/extensions-chromium/enterprise/auto-update#updated-manifest).

## <a name="distribute-a-privately-hosted-extension"></a>Verteilen einer privat gehosteten Erweiterung

Sie können den Link des Speicherortes teilen, an dem die CRX-Datei gehostet wird, und sobald Benutzer die URL in ihren Browser eingeben, wird die Erweiterung heruntergeladen und installiert. Benutzer können die Erweiterung über die Seite edge://extensions aktivieren. Damit Benutzer selbst gehostete Erweiterungen installieren können, müssen Sie die CRX-IDs der [ExtensionInstallAllowList-Richtlinie](/deployedge/microsoft-edge-policies#extensioninstallallowlist) hinzufügen und die URL des Speicherorts, an dem die CRX-Datei gehostet wird, der [ExtensionInstallSources-Richtlinie](/deployedge/microsoft-edge-policies#extensioninstallsources) hinzufügen.

Alternativ können Sie die Gruppenrichtlinie [ExtensionInstallForceList](/deployedge/microsoft-edge-manage-extensions-policies#force-install-an-extension) verwenden, um die Installation einer Erweiterung auf den Geräten Ihrer Benutzer zu erzwingen.

Sie können diese Richtlinien auf Ihre ausgewählten Benutzer, Geräte oder auf beides anwenden. Beachten Sie jedoch, dass Richtlinienaktualisierungen nicht sofort erfolgen und es einige Zeit dauern kann, bis die Richtlinieneinstellungen wirksam werden.

## <a name="see-also"></a>Weitere Informationen

- [Verwalten von Microsoft Edge-Erweiterungen im Unternehmen](microsoft-edge-manage-extensions.md)
- [Verwenden von Gruppenrichtlinien zum Verwalten von Microsoft Edge-Erweiterungen](microsoft-edge-manage-extensions-policies.md)
- [Detaillierter Leitfaden zur ExtensionSettings-Richtlinie](microsoft-edge-manage-extensions-ref-guide.md)
- [Häufig gestellte Fragen (FAQ) zu Microsoft Edge-Erweiterungen](microsoft-edge-manage-extensions-faq.md)
- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)
