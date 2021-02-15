---
title: Lokale Synchronisierung für Active Directory (AD)-Benutzende
ms.author: scottbo
author: dan-wesley
manager: silvanam
ms.date: 02/12/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Lokale Synchronisierung für Active Directory (AD)-Benutzende
ms.openlocfilehash: adf0adc8370aa1e18d07d0d2e91727d1ac607bf1
ms.sourcegitcommit: 90b8eab62edbed0e0a84780abd7d3854bf95c130
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "11328047"
---
# Lokale Synchronisierung für Active Directory (AD)-Benutzende

In diesem Artikel wird erläutert, wie Active Directory (AD)-Benutzende Microsoft Edge-Einstellungen und -Favoriten zwischen Computern übertragen können, ohne eine Verbindung zu Microsoft Cloud Services herzustellen.

> [!NOTE]
> Dieser Artikel bezieht sich auf Microsoft Edge Version 85 oder neuer.

## Einführung

Zum Synchronisieren von Benutzerdaten in Microsoft Edge sind in der Regel ein Microsoft-Konto oder ein Azure Active Directory-Konto (Azure AD) sowie eine Verbindung zu Microsoft Cloud Services erforderlich. Bei der lokalen Synchronisierung speichert Microsoft Edge die Favoriten und Einstellungen eines Active Directory-Benutzenden in einer Datei, die zwischen unterschiedlichen Computern verschoben werden kann. Die lokale Synchronisierung wirkt sich nicht auf die Cloud-Synchronisierung für Profile aus, die dies zulassen.

## Funktionsweise

Mit Microsoft Edge können Profile Active Directory (AD)-Konten zugeordnet werden, die bei der Cloud-Synchronisierung nicht verwendet werden können. Wenn die lokale Synchronisierung aktiviert ist, werden die Daten aus dem AD-Profil in einer Datei mit dem Namen "profile.pb" gespeichert. Diese Datei wird standardmäßig unter *%APPDATA%/Microsoft/Edge* gespeichert. Nachdem diese Datei geschrieben wurde, kann sie zwischen verschiedenen Computern verschoben werden, und die Benutzerdaten werden auf jedem Computer ausgelesen bzw. geschrieben. Microsoft Edge liest und schreibt nur aus dieser Datei. Es liegt in der Verantwortung des Admins, sicherzustellen, dass die Datei bei Bedarf verschoben wird.

## Verwenden der lokalen Synchronisierung

Um die lokale Synchronisierung verwenden zu können, müssen Sie sie aktivieren, ein Profil einem AD-Konto zuordnen und optional den Speicherort der Benutzerdaten ändern.

### Aktivieren der lokalen Synchronisierung

Konfigurieren Sie zum Aktivieren der lokalen Synchronisierung in Microsoft Edge die Richtlinie [RoamingProfileSupportEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilesupportenabled).

### Stellen Sie sicher, dass ein Profil mit einem Active Directory-Konto verknüpft ist.

Die lokale Synchronisierung funktioniert nur mit dem Profil, das mit einem Active Directory (AD)-Konto verknüpft ist. Wenn kein solches Profil vorhanden ist, funktioniert die lokale Synchronisierung nicht. Um sicherzustellen, dass sich die Benutzer mit einem AD-Konto anmelden, konfigurieren Sie die Richtlinie [ConfigureOnPremisesAccountAutoSignIn](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configureonpremisesaccountautosignin). Für die lokale Synchronisierung verwendet Microsoft Edge nur AD, um eine Identität für die Benutzerdaten zu erstellen, und es besteht keine direkte Beziehung zwischen der Art und Weise, wie Microsoft Edge lokale Daten liest und schreibt, und der Art und Weise, wie der Administrator das Roaming für einen AD-Benutzer konfiguriert hat.

### Ändern des Speicherorts der Benutzerdaten (optional)

Die Benutzerdaten werden standardmäßig in einer Datei namens **profile.pb** unter *%APPDATA%/Microsoft/Edge* gespeichert. Wenn Sie den Speicherort dieser Datei ändern möchten, konfigurieren Sie die Richtlinie [RoamingProfileLocation](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilelocation).

## Änderungen in der Benutzerumgebung, wenn die lokale Synchronisierung aktiviert ist

Wenn die lokale Synchronisierung aktiviert ist, werden die Benutzer nicht aufgefordert, diese zu aktivieren. Darüber hinaus können die Benutzer die Synchronisierung in den Synchronisierungseinstellungen nicht deaktivieren, und sie können keine Synchronisierungstypen aktivieren, die von der lokalen Synchronisierung nicht unterstützt werden.

## Verwendungshinweise zur lokalen Synchronisierung

### Ausführen von Cloud-Synchronisierung und lokaler Synchronisierung auf demselben Computer

Die lokale Synchronisierung stört nicht die Cloud-Synchronisierung. Wenn in Microsoft Edge mehrere Microsoft-Konten oder Azure Active Directory-Profile vorhanden sind, die mit der Cloud synchronisiert werden, werden diese Profile weiterhin synchronisiert, während die lokale Synchronisierung aktiviert ist.

### Microsoft Edge auf mehreren Computern gleichzeitig auszuführen wird nicht empfohlen.

Da für die lokale Synchronisierung eine Benutzerdatendatei zwischen Computern verschoben wird, werden bei der lokalen Synchronisierung keine Änderungen zwischen gleichzeitigen Sitzungen synchronisiert. Aus diesem Grund funktioniert die lokale Synchronisierung am besten, wenn sie auf nicht mehr als einem Computer gleichzeitig verwendet wird. Wenn simultane lokale Sitzungen ausgeführt werden, werden Daten auf einem der Computer u. U. unerwartet von Daten von einem anderen Computer überschrieben, wenn Sie das nächste Mal eine Browsersitzung starten.

> [!NOTE]
> Microsoft Edge sperrt die **profile.pb**-Datei, wenn die lokale Synchronisierung aktiviert ist. Wenn die Ordnerumleitung verwendet wird, um eine einzelne **profile.pb**-Datei zwischen verschiedenen Computern freizugeben, kann nur eine der Instanzen von Microsoft Edge gestartet werden, die diese Datei verwendet.

### Verwenden anderer Synchronisierungsrichtlinien mit der lokalen Synchronisierung

Die Richtlinie [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled) kann verwendet werden, um die Synchronisierung der Favoriten oder Einstellungen bei Bedarf selektiv zu deaktivieren. Die Richtline [SyncDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#syncdisabled) hat keine Auswirkungen auf die lokale Synchronisierung.

## Weitere Informationen

- [Angebotsseite für Microsoft Edge für Unternehmen](https://aka.ms/EdgeEnterprise)
- [Microsoft Edge und Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md)
- [Microsoft Edge Enterprise-Synchronisierung](microsoft-edge-enterprise-sync.md)
