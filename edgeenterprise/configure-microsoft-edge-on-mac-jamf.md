---
title: Konfigurieren von Microsoft Edge unter macOS mit Jamf
ms.author: brianalt
author: dan-wesley
manager: laurawi
ms.date: 11/30/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Konfigurieren der Microsoft Edge-Richtlinieneinstellungen auf Mac-Geräten mit Jamf
ms.openlocfilehash: 1859d9fb1fd3ea8ff6908c41f75df21a8b338769
ms.sourcegitcommit: ed6a5afabf909df87bec48671c4c47bcdfaeb7bc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/02/2020
ms.locfileid: "11194713"
---
# Konfigurieren der Microsoft Edge-Richtlinieneinstellungen unter macOS mit Jamf

In diesem Artikel wird beschrieben, wie Sie Richtlinieneinstellungen unter macOS mithilfe einer Microsoft Edge-Richtlinienmanifestdatei unter Jamf Pro 10.19 konfigurieren.

Sie können Microsoft Edge-Richtlinieneinstellungen auf macOS auch mithilfe einer Eigenschaftslistendatei (.plist) konfigurieren. Weitere Informationen finden Sie unter [Konfigurieren für macOS mithilfe einer Eigenschaftsliste (.plist)](configure-microsoft-edge-on-mac.md)


## Voraussetzungen

Die folgende Software ist erforderlich:

- Microsoft Edge Stable Kanal 81
- Richtlinienvorlagendatei, Version 81.0.416.3
- Jamf Pro, Version 10.19

## Informationen zum Jamf Pro-Menü der Anwendungseinstellungen und benutzerdefinierten Einstellungen

Vor Jamf Pro 10.18 musste zur Verwaltung von Office 365 manuell eine Eigenschaftslistendatei (.plist) erstellt werden. Dieser Workflow war zeitaufwändig und erforderte einen starken technischen Hintergrund. Mit Jamf Pro 10.18 wurden diese Barrieren durch Optimierung des Konfigurationsprozesses eliminiert. IT-Administratoren konnten diese neue Benutzeroberfläche jedoch nur für bestimmte, von Jamf angegebene Anwendungen und bevorzugten Domänen verwenden.

In Jamf Pro 10.19 kann ein Benutzer ein JSON-Manifest als "benutzerdefiniertes Schema" für eine beliebige bevorzugte Domäne hochladen, und die grafische Benutzeroberfläche wird aus diesem Manifest generiert. Das erstellte benutzerdefinierte Schema folgt der JSON-Schemaspezifikation.

Weitere Informationen finden Sie im Jamf Pro-Administratorhandbuch unter [Computer Configuration Profiles](https://jamf.it/computer-configuration-profiles) (Computerkonfigurationsprofile).

## Abrufen des Richtlinienmanifests für eine bestimmte Version von Microsoft Edge

So rufen Sie das Richtlinienmanifest ab

- Navigieren Sie zur [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise).
- Wählen Sie in der Dropdownliste „Kanal/Version“ **einen beliebigen Kanal mit Version 81 oder höher aus.**_.
- Wählen Sie in der Dropdownliste „Build“ einen beliebigen _*81 Build oder höher**_ aus.
- Klicken Sie auf GET POLICY FILES (Richtliniendateien abrufen), um Ihr Richtlinienvorlagenpaket herunterzuladen.

  > [!NOTE]
  > Derzeit ist das Richtlinienvorlagenpaket als CAB-Datei signiert. Sie müssen ein Drittanbietertool verwenden, z.B. The Unarchiver, um die Datei unter macOS zu öffnen.

Nachdem Sie die CAB-Datei entpackt haben, entpacken Sie die ZIP-Datei, und navigieren Sie zum Verzeichnis "Mac" auf der obersten Ebene. Das Manifest namens "policy_manifest.json" befindet sich in diesem Verzeichnis.

Dieses Manifest wird ab Build 81.0.416.3 in jedem Richtlinienpaket veröffentlicht. Wenn Sie Richtlinien im Dev Channel testen möchten, können Sie das den einzelnen Entwicklerreleases zugeordnete Manifest verwenden und in Jamf Pro testen.  

## Verwenden des Richtlinienmanifests in Jamf Pro

Führen Sie die folgenden Schritte aus, um das Richtlinienmanifest in Jamf Pro hochzuladen, und erstellen Sie dann ein Richtlinienprofil für macOS.

1. Melden Sie sich bei Jamf an.
2. Wählen Sie die Registerkarte _*Computer** aus.
3. Wählen Sie unter **Content Management** (Inhaltsverwaltung) **Configuration Profiles** (Konfigurationsprofile) aus.
4. Klicken Sie auf der Seite **Configuration Profiles** (Konfigurationsprofile) auf **+ New** (Neu).

   ![Hinzufügen eines neuen Profils in Jamf](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-configuration-profiles.png)

5. Wählen Sie unter **New macOS Configuration Profile** (Neues macOS-Konfigurationsprofil) >**Options** (Optionen) **Application & Custom Settings** (Anwendungs- und benutzerdefinierte Einstellungen) aus.
6. Klicken Sie im Popupfenster **Application & Custom Settings** (Anwendungs- und benutzerdefinierte Einstellungen) auf **Configure** (Konfigurieren).

   ![Konfigurieren von Anwendungseinstellungen und benutzerdefinierten Einstellungen](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-app-and-custom.png)

7. Legen Sie im Abschnitt **Application & Custom Settings** (Anwendungs- und benutzerdefinierte Einstellungen) die im folgenden Screenshot dargestellten Werte fest.

   ![Profilquelle und benutzerdefiniertes Schema](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-app-and-custom-schema.png)

   - Wählen Sie für **Creation Method** (Erstellungsmethode) die Option **Configure settings** (Einstellungen konfigurieren) aus.
   - Wählen Sie für **Source** (Quelle) die Option **Custom Schema** (Benutzerdefiniertes Schema) aus.
   - Geben Sie für **Preference Domain** (Bevorzugte Domäne) den Namen Ihrer Domäne an. In diesem Beispiel wird *com.microsoft.Edge* als Domäne verwendet.
   - Fügen Sie für **Custom Schema** (Benutzerdefiniertes Schema) den Inhalt der Manifestdatei "policy_manifest.json" ein.
   - Klicken Sie auf **Speichern**.

8. Nachdem Sie das Profil gespeichert haben, zeigt Jamf den Abschnitt **General** (Allgemein) an, wie im nächsten Screenshot dargestellt.

   ![Abschnitt "Configure General" (Konfigurieren, Allgemein)](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-app-and-custom-general-setting.png)

   - Geben Sie einen **Anzeigenamen** und eine **Beschreibung** für das Profil ein.
   - Behalten Sie die Standardeinstellung **None** (Keine) für **Category** (Kategorie) bei.
   - Für **Distribution Method** (Verteilungsmethode) lauten die Optionen **Install Automatically** (Automatisch installieren) oder **Make Available in Self Service** (Im Self-Service bereitstellen).
   - Für **Level** (Ebene) lauten die Optionen **User Level** (Benutzerebene) oder **Computer Level** (Computerebene).
   - Klicken Sie auf **Speichern**.

9. Nachdem Sie den Abschnitt "General" (Allgemein) gespeichert haben, zeigt Jamf das Microsoft Edge Beta Channel-Konfigurationsprofil an, das in unserem Beispiel eingerichtet wurde. Beachten Sie im nächsten Screenshot, dass Sie das Profil weiter bearbeiten können, indem Sie auf **Edit** (Bearbeiten) klicken. Wenn Sie fertig sind, klicken Sie auf **Done** (Fertig).

   ![Neues Konfigurationsprofil mit Optionen](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-configuration-profiles-beta-channel.png)

   > [!NOTE]
   > Sie können dieses Profil, nachdem es gespeichert wurde, oder auch in einer anderen Jamf-Sitzung bearbeiten. So könnten Sie beispielsweise die Verteilungsmethode so ändern, dass sie im Self-Service bereitgestellt wird.

   Wenn Sie im Microsoft Edge Stable-Kanal eine Nachbearbeitung durchführen oder es löschen möchten, wählen Sie den Profilnamen aus, der im folgenden Screenshot der Konfigurationsprofile dargestellt wird.

   ![Liste der Konfigurationsprofile](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-configuration-profiles-beta-channel-done.png)

Nachdem Sie das neue Konfigurationsprofil erstellt haben, müssen Sie noch den **Scope** (Geltungsbereich) für das Profil konfigurieren.

### So konfigurieren Sie den Geltungsbereich

1. Stellen Sie für **Targets** (Ziele) die folgenden Minimaleinstellungen bereit:

   - ZIELCOMPUTER. Die Optionen sind "Bestimmte Computer" oder "Alle Computer".
   - ZIELBENUTZER. Die Optionen sind "Bestimmte Benutzer" oder "Alle Benutzer".
   - Klicken Sie auf **Speichern**.
2. Behalten Sie für **Limitations** (Beschränkungen) die Standardeinstellung bei: "None" (Keine). Klicken Sie auf **Abbrechen**.
3. Behalten Sie für **Exclusions** (Ausschlüsse) die Standardeinstellung bei: "None" (Keine). Klicken Sie auf **Abbrechen**.

## Weitere Informationen

- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)
- [Konfigurieren für macOS mit Intune](configure-microsoft-edge-on-mac.md)
- [Konfigurieren für Windows](configure-microsoft-edge.md)
- [Konfigurieren für Windows mit Intune](configure-edge-with-intune.md)
