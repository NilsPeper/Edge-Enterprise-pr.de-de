---
title: Konfigurieren von MicrosoftEdge für Windows
ms.author: brianalt
author: kelleyvice-msft
manager: laurawi
ms.date: 10/09/2019
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Konfigurieren der Microsoft Edge-Richtlinieneinstellungen auf Windows-Geräten
ms.openlocfilehash: 99aaf002f868ce29e81aa40024fa1de2e83d76e1
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979893"
---
# Konfigurieren der Microsoft Edge-Richtlinieneinstellungen unter Windows

Verwenden Sie die folgenden Informationen, um die Microsoft Edge-Richtlinieneinstellungen auf Ihren Windows-Geräten zu konfigurieren.

> [!NOTE]
> Dieser Artikel bezieht sich auf Microsoft Edge Version 77 oder höher.

## Konfigurieren von Richtlinieneinstellungen unter Windows

Mithilfe von _Gruppenrichtlinienobjekten (Group Policy Objects GPO)_ können Sie Richtlinieneinstellungen für Microsoft Edge und verwaltete Microsoft Edge-Updates für alle Windows-Versionen konfigurieren. Sie können Richtlinien auch über die Registrierung für Windows-Geräte bereitstellen, die einer Microsoft Active Directory-Domäne angehören, oder für Windows 10 Pro oder Enterprise-Instanzen, die für die Geräteverwaltung in Microsoft Intune registriert sind. Um Microsoft Edge mit Gruppenrichtlinienobjekten zu konfigurieren, installieren Sie _administrative Vorlagen_, die Regeln und Einstellungen für Microsoft Edge zum zentralen Speicher für Gruppenrichtlinien in Ihrer Active Directory-Domäne oder zum Vorlagenordner „Richtliniendefinition” auf einzelnen Computern hinzufügen, und konfigurieren Sie dann die gewünschten Richtlinien, die Sie setzen möchten.

Sie können die Active Directory-Gruppenrichtlinie verwenden, um die Microsoft Edge-Richtlinieneinstellungen zu konfigurieren, wenn Sie es vorziehen, die Richtlinie auf Domänenebene zu verwalten. Auf diese Weise können Sie Richtlinieneinstellungen global verwalten, unterschiedliche Richtlinieneinstellungen auf bestimmte Organisationseinheiten ausrichten oder mithilfe von WMI-Filtern Einstellungen nur auf Benutzer oder Computer anwenden, die von einer bestimmten Abfrage zurückgegeben wurden. Wenn Sie die Richtlinie auf einzelnen Computern konfigurieren möchten, können Sie Richtlinieneinstellungen anwenden, die sich nur auf das lokale Gerät auswirken, indem Sie den Editor für lokale Gruppenrichtlinien auf dem Zielcomputer verwenden.

Microsoft Edge unterstützt sowohl die _obligatorischen_ als auch die _empfohlenen_ Richtlinien. Obligatorische Richtlinien setzen die Benutzerpräferenzen außer Kraft und verhindern, dass der Benutzer sie ändert, während die empfohlene Richtlinie eine Standardeinstellung bietet, die vom Benutzer überschrieben werden kann. Die meisten Richtlinien sind nur obligatorisch. eine Teilmenge ist obligatorisch und wird empfohlen. Wenn beide Versionen einer Richtlinie festgelegt sind, hat die obligatorische Einstellung Vorrang.

>[!TIP]
> Sie können Microsoft Intune zum Konfigurieren der Microsoft Edge-Richtlinieneinstellungen verwenden. Weitere Informationen finden Sie unter [Konfigurieren von Microsoft Edge mit Microsoft Intune](configure-edge-with-intune.md).

Es gibt zwei administrative Vorlagen für Microsoft Edge, die entweder auf Computer- oder auf Active Directory-Domänenebene angewendet werden können:

- *msedge.admx* zum [Konfigurieren von Microsoft Edge-Einstellungen](microsoft-edge-policies.md)
- *msedgeupdate.admx* zum [Verwalten von Microsoft Edge-Updates](microsoft-edge-update-policies.md).

Laden sie zunächst die Microsoft Edge administrative Vorlage herunter, und installieren Sie sie.

### 1. Herunterladen und Installieren der Microsoft Edge administrativen Vorlage

Wenn Sie Microsoft Edge-Richtlinieneinstellungen in Active Directory konfigurieren möchten, laden Sie die Dateien an einen Netzwerkspeicherort herunter, auf den Sie von einem Domänencontroller oder einer Arbeitsstation mit installierter Remoteserver-Verwaltungstools (RSAT) zugreifen können. Um die Konfiguration auf einem einzelnen Computer auszuführen, laden Sie einfach die Dateien auf diesen Computer herunter.

Wenn Sie die administrativen Vorlagendateien dem entsprechenden Speicherort hinzufügen, sind Microsoft Edge-Richtlinieneinstellungen sofort im Gruppenrichtlinien-Editor verfügbar.

Wechseln Sie zur [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise), um die Microsoft Edge-Richtlinienvorlagendatei (*MicrosoftEdgePolicyTemplates.cab*) herunterzuladen, und extrahieren Sie den Inhalt.

#### Fügen Sie Active Directory die administrative Vorlage hinzu.

1. Navigieren Sie auf einem Domänencontroller oder einer Arbeitsstation mit RSAT zum Ordner **PolicyDefinition** (auch als _zentraler Speicher_ bezeichnet) auf einem beliebigen Domänencontroller für Ihre Domäne. Bei älteren Versionen von Windows Server müssen Sie möglicherweise den Ordner „PolicyDefinition” erstellen. Weitere Informationen finden Sie unter [Erstellen und Verwalten des zentralen Speichers für Administrative Vorlagen für Gruppenrichtlinien in Windows](https://support.microsoft.com/help/3087759/how-to-create-and-manage-the-central-store-for-group-policy-administra).
1. Öffnen Sie *MicrosoftEdgePolicyTemplates*, und wechseln Sie zu **windows** > **admx**.
1. Kopieren Sie die Datei *msedge.admx* in den Ordner „PolicyDefinition”. (Beispiel: %systemroot%\sysvol\domain\policies\PolicyDefinitions)
1. Öffnen Sie im Ordner *admx* den entsprechenden Sprachordner. Wenn Sie sich beispielsweise in den Vereinigten Staaten befinden, öffnen Sie den Ordner **en-US**.
1. Kopieren Sie die Datei *msedge.adml* in den entsprechenden Sprachordner im Ordner „PolicyDefinition”. Erstellen Sie den Ordner, falls er noch nicht vorhanden ist. (Beispiel: %systemroot%\sysvol\domain\policies\PolicyDefinitions\EN-US)
1. Wenn Ihre Domäne über mehr als einen Domänencontroller verfügt, werden die neuen ADMX-Dateien beim nächsten Domänen-Replikationsintervall auf diese repliziert.
1. Um zu bestätigen, dass die Dateien richtig geladen wurden, öffnen Sie den **Gruppenrichtlinienverwaltungs-Editor** über die Windows-Verwaltungsprogramme und erweitern Sie **Computerkonfiguration** > **Richtlinien** > **Administrative Vorlagen** > **Microsoft Edge**. Es sollte mindestens ein Microsoft Edge-Knoten angezeigt werden, wie unten dargestellt.

    ![Microsoft Edge-Richtlinien](./media/configure-microsoft-edge/edge-gpo-policies.png)

#### Hinzufügen der administrativen Vorlage zu einem einzelnen Computer

1. Öffnen Sie auf dem Zielcomputer *MicrosoftEdgePolicyTemplates* und wechseln Sie zu **windows** > **admx**.
2. Kopieren Sie die Datei *msedge.admx* in den Vorlagenordner „Richtliniendefinition”. (Beispiel: C:\Windows\PolicyDefinitions)
3. Öffnen Sie im Ordner *admx* den entsprechenden Sprachordner. Wenn Sie sich beispielsweise in den Vereinigten Staaten befinden, öffnen Sie den Ordner **en-US**.
4. Kopieren Sie die Datei *msedge.adml* in den entsprechenden Sprachordner im Vorlagenordner „Richtliniendefinition”. (Beispiel: C:\Windows\PolicyDefinitions\en-US)
5. Öffnen Sie zum Bestätigen der korrekten Dateien entweder den Editor für lokale Gruppenrichtlinien direkt (Windows-Taste + R) und geben Sie „gpedit.msc” ein oder öffnen Sie MMC, und laden Sie das Snap-In „Editor für lokale Gruppenrichtlinien”. Wenn ein Fehler auftritt, liegt dies normalerweise daran, dass sich die Dateien an einem falschen Speicherort befinden.

<!--
To add the administrative template to manage Microsoft Edge updates:

1. Open the *MicrosoftEdgePolicyTemplates* file and go to **windows** > **admx**.
2. Copy the *msedgeupdate.admx* file to your Policy Definition template folder. (Example: C:\Windows\PolicyDefinitions)
3. In the *updatepolicies* folder, open the appropriate language folder. For example, if you’re in Germany, open the **de-DE** folder.
4. Copy the *msedgeupdate.adml* file to the matching language folder in your Policy Definition folder. (Example: C:\Windows\PolicyDefinitions\de-DE)
5. Open MMC and load the Local Group Policy Editor snap-in to confirm the files loaded correctly. If an error occurs, it’s usually because the files are in an incorrect location.

> [!NOTE]
> Currently the Microsoft Edge update policies are only localized in en-US. Additional language support will be added in a future release.
-->

### 2. Festlegen von obligatorischen oder empfohlenen Richtlinien

Sie können obligatorische oder empfohlene Richtlinien festlegen, um Microsoft Edge mit dem Gruppenrichtlinien-Editor für Active Directory und einzelne Computer zu konfigurieren. Sie können Richtlinieneinstellungen entweder auf die **Computerkonfiguration** oder die **Benutzerkonfiguration** festlegen, indem Sie den entsprechenden Knoten wie unten beschrieben auswählen.

- Öffnen Sie zum Konfigurieren einer obligatorischen Richtlinie den Gruppenrichtlinien-Editor und wechseln Sie zu (**Computerkonfiguration** oder **Benutzerkonfiguration**) > **Richtlinien** > **Administrative Vorlagen** > **Microsoft Edge**.
- Öffnen Sie zum Konfigurieren einer empfohlenen Richtlinie den Gruppenrichtlinien-Editor und wechseln Sie zu (**Computerkonfiguration** oder **Benutzerkonfiguration**) > **Richtlinien** > **Administrative Vorlagen** > **Microsoft Edge – Standardeinstellungen (kann von Benutzern übergangen werden)**.

  ![Öffnen Sie den Gruppenrichtlinien-Editor.](./media/configure-microsoft-edge/edge-ad-policy.png)

### 3. Testen Ihrer Richtlinien

Öffnen Sie auf einem Zielclientgerät Microsoft Edge und navigieren Sie zu **edge://policy**, um alle angewendeten Richtlinien anzuzeigen. Wenn Sie Richtlinieneinstellungen auf dem lokalen Computer angewendet haben, sollten Richtlinien sofort angezeigt werden. Möglicherweise müssen Sie Microsoft Edge schließen und erneut öffnen, wenn es während der Konfiguration der Richtlinieneinstellungen geöffnet war.

![Anzeigen der konfigurierten Richtlinien im Browser](./media/configure-microsoft-edge/edge-gpEdit.png)

Für Active Directory-Gruppenrichtlinieneinstellungen werden Richtlinieneinstellungen in regelmäßigen Abständen, die vom Domänenadministrator definiert werden, an Domänencomputer übermittelt, und Zielcomputer erhalten möglicherweise nicht sofort Richtlinienaktualisierungen. Um Active Directory-Gruppenrichtlinieneinstellungen auf einem Zielcomputer manuell zu aktualisieren, führen Sie den folgenden Befehl in einer Eingabeaufforderung oder PowerShell-Sitzung auf dem Zielcomputer aus:

``` powershell
gpupdate /force
```

Möglicherweise müssen Sie Microsoft Edge schließen und erneut öffnen, bevor die neuen Richtlinien angezeigt werden.

Sie können auch REGEDIT.exe auf einem Zielcomputer verwenden, um die Registrierungseinstellungen anzuzeigen, in denen Gruppenrichtlinieneinstellungen gespeichert werden. Diese Einstellungen befinden sich im Registrierungspfad **HKLM\SOFTWARE\Policies\Microsoft\Edge.**

## Häufig gestellte Fragen

### Kann Microsoft Edge für die Verwendung von Master-Einstellungen konfiguriert werden?

Ja, Sie können Microsoft Edge so konfigurieren, dass es eine Mastervoreinstellungsdatei verwendet.

 Mit einer Mastervoreinstellungsdatei können Sie Standardeinstellungen konfigurieren, wenn Microsoft Edge bereitgestellt wird. Sie können auch eine Mastervoreinstellungsdatei verwenden, um Einstellungen auf Computern anzuwenden, die nicht von einem Geräteverwaltungssystem verwaltet werden. Diese Einstellungen werden auf das Profil des Benutzers angewendet, wenn der Benutzer zum ersten Mal den Browser ausführt. Nachdem der Benutzer den Browser ausgeführt hat, werden Änderungen an der Mastervoreinstellungsdatei nicht angewendet. Benutzer können Einstellungen aus den Mastervoreinstellungen im Browser ändern. Wenn Sie eine Einstellung zwingend vornehmen oder eine Einstellung nach der ersten Ausführung des Browsers ändern möchten, müssen Sie eine Richtlinie verwenden.

Mit einer Mastervoreinstellungsdatei können Sie viele verschiedene Einstellungen und Voreinstellungen für den Browser anpassen, einschließlich der für andere Chromium-basierte Browser und Microsoft Edge-spezifische Einstellungen.  Richtlinienbezogene Voreinstellungen können mithilfe der Mastervoreinstellungsdatei konfiguriert werden. In Fällen, in denen eine Richtlinie festgelegt ist und ein entsprechender Master-Voreinstellungssatz vorhanden ist, hat die Richtlinieneinstellung Vorrang.

> [!IMPORTANT]
> Möglicherweise sind nicht alle verfügbaren Einstellungen mit der Microsoft Edge-Terminologie und den Namenskonventionen konsistent.  Es besteht keine Garantie dafür, dass diese Voreinstellungen in zukünftigen Versionen weiterhin wie erwartet funktionieren. Voreinstellungen werden in späteren Versionen möglicherweise geändert oder ignoriert.

Eine Master-Voreinstellungsdatei ist eine Textdatei, die mit JSON-Markup formatiert wurde. Diese Datei muss demselben Verzeichnis wie die ausführbare msedge.exe-Datei hinzugefügt werden. Für systemweite Unternehmensbereitstellungen unter Windows ist dies in der Regel: *Windows: C:\Program Files\Microsoft\Edge\Application\ master_preferences*.

## Weitere Informationen:

- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)
- [Konfigurieren für Windows mit Intune](configure-edge-with-intune.md)
- [Konfigurieren für macOS](configure-microsoft-edge-on-mac.md)
- [Microsoft Edge-Unternehmensrichtlinien durchsuchen](microsoft-edge-policies.md)


