---
title: Konfigurieren sie Microsoft Edge für macOS mithilfe einer Eigenschaftenliste.
ms.author: brianalt
author: kelleyvice-msft
manager: laurawi
ms.date: 12/14/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Erfahren Sie, wie Sie Microsoft Edge Richtlinieneinstellungen unter macOS mithilfe einer Eigenschaftenliste konfigurieren, die Sie auf Microsoft Intune bereitstellen können.
ms.openlocfilehash: 4cb3d635c8fc108a3b81ec17175ce0e3d8fa287a
ms.sourcegitcommit: e7f3098d8b7d91cae20b5778a71a87daababc312
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2022
ms.locfileid: "12297701"
---
# <a name="configure-microsoft-edge-policy-settings-for-macos-using-a-property-list"></a>Konfigurieren Microsoft Edge Richtlinieneinstellungen für macOS mithilfe einer Eigenschaftenliste

In diesem Artikel wird beschrieben, wie Sie Microsoft Edge unter macOS mithilfe einer Eigenschaftenlistendatei (\.plist) konfigurieren. Sie erfahren, wie Sie diese Datei erstellen und dann auf Microsoft Intune bereitstellen.

Weitere Informationen finden Sie unter [Informationen zu Eigenschaftslistendateien](https://developer.apple.com/library/archive/documentation/General/Reference/InfoPlistKeyReference/Articles/AboutInformationPropertyListFiles.html) (Apple-Website) und [Benutzerdefinierte Nutzlast-Einstellungen](https://support.apple.com/guide/mdm/custom-mdm9abbdbe7/1/web/1).

> [!NOTE]
> Dieser Artikel bezieht sich auf Microsoft Edge Version 77 oder höher.

## <a name="configure-microsoft-edge-policies-on-macos"></a>Konfigurieren der Microsoft Edge-Richtlinien unter macOS

Der erste Schritt besteht darin, eine *Übermittlung zu erstellen. Sie können die plist-Datei mit einem beliebigen Text-Editor erstellen. Eine weitere Option besteht darin, [Terminal zum Erstellen des Konfigurationsprofils zu](#create-a-configuration-profile-using-terminal)verwenden. Es ist jedoch einfacher, eine plist-Datei mit einem Tool zu erstellen und zu bearbeiten, das den XML-Code für Sie formatiert. *Xcode* ist eine kostenlose integrierte Entwicklungsumgebung, die an den folgenden Speicherorten verfügbar ist:

- [Apple Developer-Website](https://developer.apple.com/xcode/)
- [Mac App Store](https://apps.apple.com/app/xcode/id497799835?mt=12)

Eine liste der unterstützten Richtlinien und ihrer bevorzugten Schlüsselnamen finden Sie in der [Microsoft Edge Referenz für Browserrichtlinien](./microsoft-edge-policies.md). In der Richtlinienvorlagendatei, die von der [Microsoft Edge Enterprise Zielseite](https://aka.ms/EdgeEnterprise)heruntergeladen werden kann, befindet sich ein plist-Beispiel (*itadminexample.plist*) im **Beispielordner.** Diese Datei enthält alle unterstützten Datentypen, die Sie anpassen können, um Ihre Richtlinieneinstellungen zu definieren.

Nachdem Sie den Inhalt Ihrer plist erstellt haben, benennen Sie die plist mithilfe der Microsoft Edge Einstellungsdomäne, die *"com.microsoft.Edge"* lautet. Bei diesem Namen wird die Groß-/Kleinschreibung beachtet und sollte nicht den Kanal enthalten, auf den Sie abzielen, da er für alle Microsoft Edge Kanäle gilt. Der plist-Dateiname muss **_com.microsoft.Edge.plist_** lauten.

> [!IMPORTANT]
> Ab dem Build 78.0.249.2 werden alle Microsoft Edge-Kanäle auf macOS aus der Einstellungsdomäne **com.microsoft.Edge** eingelesen. Alle früheren Versionen wurden aus einer kanalspezifischen Domäne eingelesen, z. B. **com.microsoft.Edge.Dev** für den Dev Channel.

Der letzte Schritt besteht darin, Ihre Eigenschaftsliste auf den Mac-Geräten Ihrer Benutzer mit Ihrem bevorzugten MDM-Anbieter bereitzustellen, z. B. Microsoft Intune. Anweisungen finden Sie unter [Bereitstellen Ihrer plist](#deploy-your-plist)..

### <a name="create-a-configuration-profile-using-terminal"></a>Erstellen eines Konfigurationsprofils mithilfe von Terminal

1. Verwenden Sie in Terminal den folgenden Befehl, um eine plist für Microsoft Edge auf Ihrem Desktop mit den bevorzugten Einstellungen zu erstellen:

   ```cmd
   /usr/bin/defaults write ~/Desktop/com.microsoft.Edge.plist RestoreOnStartup -int 1
   ```

2. Konvertieren Sie die plist aus dem Binärformat in das Nur-Text-Format:

   ```cmd
   /usr/bin/plutil -convert xml1 ~/Desktop/com.microsoft.Edge.plist
   ```

Überprüfen Sie nach dem Konvertieren der Datei, ob Ihre Richtliniendaten korrekt sind und die Einstellungen enthalten, für Ihr Konfigurationsprofil.

> [!NOTE]
> Im Inhalt der plist- oder xml-Datei dürfen nur Schlüssel-Werte-Paare enthalten sein. Entfernen Sie vor dem Hochladen Ihrer Datei in Intune alle \<plist>- und \<dict>-Werte und XML-Header aus der Datei. Die Datei darf nur Schlüssel-Wert Paare enthalten.

## <a name="deploy-your-plist"></a>Bereitstellen Ihrer plist

Erstellen Sie mit Microsoft Intune ein neues Gerätekonfigurationsprofil für die macOS-Plattform, und wählen Sie den *Einstellungsdateiprofiltyp* aus. Richten Sie **com.microsoft.Edge** als bevorzugten Domänennamen ein und laden Sie Ihre Eigenschaftsliste hoch. Weitere Informationen finden Sie unter [Hinzufügen einer Eigenschaftenlistendatei zu macOS-Geräten mit Microsoft Intune](/intune/configuration/preference-file-settings-macos).

Laden Sie für Jamf die Datei "\.plist" als nutzlast des *benutzerdefinierten Einstellungen* hoch.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)
- [Konfigurieren für macOS mit Jamf](configure-microsoft-edge-on-mac-jamf.md)
- [Konfigurieren für Windows](configure-microsoft-edge.md)
- [Konfigurieren für Windows mit Intune](configure-edge-with-intune.md)