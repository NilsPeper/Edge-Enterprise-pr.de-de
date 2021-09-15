---
title: Konfigurieren von Microsoft Edge für macOS mithilfe einer Eigenschaftsliste (.plist)
ms.author: brianalt
author: kelleyvice-msft
manager: laurawi
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Konfigurieren der Microsoft Edge-Richtlinieneinstellungen unter macOS mithilfe einer Eigenschaftsliste (.plist)
ms.openlocfilehash: d2e604e13f0fb7f81b2fb492073eba0751407771
ms.sourcegitcommit: 8968f3107291935ed9adc84bba348d5f187eadae
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/12/2021
ms.locfileid: "11979177"
---
# <a name="configure-microsoft-edge-policy-settings-for-macos-using-a-plist"></a>Konfigurieren der Microsoft Edge-Richtlinieneinstellungen für macOS mithilfe einer Eigenschaftsliste (.plist)

In diesem Artikel wird beschrieben, wie Sie Microsoft Edge auf macOS mithilfe einer Eigenschaftslistendatei (.plist) konfigurieren. Sie erfahren, wie Sie diese Datei erstellen und dann auf Microsoft Intune bereitstellen.

Weitere Informationen finden Sie unter [Informationen zu Eigenschaftslistendateien](https://developer.apple.com/library/archive/documentation/General/Reference/InfoPlistKeyReference/Articles/AboutInformationPropertyListFiles.html) (Apple-Website) und [Benutzerdefinierte Nutzlast-Einstellungen](https://support.apple.com/guide/mdm/custom-mdm9abbdbe7/1/web/1).

> [!NOTE]
> Dieser Artikel bezieht sich auf Microsoft Edge Version 77 oder höher.

## <a name="configure-microsoft-edge-policies-on-macos"></a>Konfigurieren der Microsoft Edge-Richtlinien unter macOS

Der erste Schritt besteht darin, eine *Übermittlung zu erstellen. Sie können die plist-Datei mit einem beliebigen Text-Editor erstellen oder Sie können das [Konfigurationsprofil mithilfe von Terminal erstellen](#create-a-configuration-profile-using-terminal). Es ist jedoch einfacher, eine plist-Datei mit einem Tool zu erstellen und zu bearbeiten, das den XML-Code für Sie formatiert. *Xcode* ist eine ﻿kostenlose integrierte Entwicklungsumgebung, die Sie von einem der folgenden Speicherorte abrufen können:

- [Apple Developer-Website](https://developer.apple.com/xcode/)
- [Mac App Store](https://apps.apple.com/app/xcode/id497799835?mt=12)

Eine liste der unterstützten Richtlinien und ihrer bevorzugten Schlüsselnamen finden Sie in der [Microsoft Edge Referenz für Browserrichtlinien](microsoft-edge-policies.md). In der Richtlinienvorlagendatei, die von der [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise) heruntergeladen werden kann, befindet sich im Ordner **Beispiele** ein Beispiel für plist (*itadminexample.plist*). Die Beispieldatei enthält alle unterstützten Datentypen, die Sie anpassen können, um die Richtlinieneinstellungen zu definieren. 

Der nächste Schritt, nachdem Sie den Inhalt Ihrer plist-Datei erstellt haben, besteht darin, diese unter Verwendung der Microsoft Edge-Einstellungsdomäne *com.microsoft.edge* zu benennen. Der Name unterscheidet zwischen Groß- und Kleinschreibung und sollte nicht den Kanal enthalten, auf den Sie abzielen, da er für alle Microsoft Edge-Kanäle gilt. Der plist-Dateiname muss **_com.microsoft.Edge.plist_** lauten.

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

Stellen Sie nach dem Konvertieren der Datei sicher, dass die Richtliniendaten korrekt sind und die gewünschten Einstellungen für Ihr Konfigurationsprofil enthalten.

> [!NOTE]
> Im Inhalt der plist- oder xml-Datei dürfen nur Schlüssel-Werte-Paare enthalten sein. Entfernen Sie vor dem Hochladen Ihrer Datei in Intune alle \<plist>- und \<dict>-Werte und XML-Header aus der Datei. Die Datei darf nur Schlüssel-Wert Paare enthalten.

## <a name="deploy-your-plist"></a>Bereitstellen Ihrer plist

Erstellen Sie für Microsoft Intune ein neues Gerätekonfigurationsprofil, das auf die macOS-Plattform ausgerichtet ist, und wählen Sie den Profiltyp *Einstellungsdatei* aus. Richten Sie **com.microsoft.Edge** als bevorzugten Domänennamen ein und laden Sie Ihre Eigenschaftsliste hoch. Weitere Informationen finden Sie unter [Hinzufügen einer Eigenschaftslistendatei zu macOS-Geräten mithilfe von Microsoft Intune](/intune/configuration/preference-file-settings-macos).

Laden Sie für Jamf die Eigenschaftslistendatei als Nutzlast für *Benutzerdefinierte Einstellungen* hoch.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)
- [Konfigurieren für macOS mit Jamf](configure-microsoft-edge-on-mac-jamf.md)
- [Konfigurieren für Windows](configure-microsoft-edge.md)
- [Konfigurieren für Windows mit Intune](configure-edge-with-intune.md)