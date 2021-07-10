---
title: Lokale Synchronisierung für Active Directory (AD)-Benutzende
ms.author: collw
author: dan-wesley
manager: silvanam
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Lokale Synchronisierung für Active Directory (AD)-Benutzende
ms.openlocfilehash: f595c863193f2b3d383a6215ab7817a53bbf5ca6
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "11642441"
---
# <a name="on-premises-sync-for-active-directory-ad-users"></a>Lokale Synchronisierung für Active Directory (AD)-Benutzende

In diesem Artikel wird erläutert, wie Active Directory (AD)-Benutzende Microsoft Edge-Einstellungen und -Favoriten zwischen Computern übertragen können, ohne eine Verbindung zu Microsoft Cloud Services herzustellen.

> [!NOTE]
> Dieser Artikel bezieht sich auf Microsoft Edge Version 85 oder neuer.

## <a name="introduction"></a>Einführung

Zum Synchronisieren von Benutzerdaten in Microsoft Edge sind in der Regel ein Microsoft-Konto oder ein Azure Active Directory-Konto (Azure AD) sowie eine Verbindung zu Microsoft Cloud Services erforderlich. Bei der lokalen Synchronisierung speichert Microsoft Edge die Favoriten und Einstellungen eines Active Directory-Benutzenden in einer Datei, die zwischen unterschiedlichen Computern verschoben werden kann. Die lokale Synchronisierung wirkt sich nicht auf die Cloud-Synchronisierung für Profile aus, die dies zulassen.

## <a name="how-it-works"></a>Funktionsweise

Mit Microsoft Edge können Profile Active Directory (AD)-Konten zugeordnet werden, die bei der Cloud-Synchronisierung nicht verwendet werden können. Wenn die lokale Synchronisierung aktiviert ist, werden die Daten aus dem AD-Profil in einer Datei mit dem Namen "profile.pb" gespeichert. Diese Datei wird standardmäßig unter *%APPDATA%/Microsoft/Edge* gespeichert. Nachdem diese Datei geschrieben wurde, kann sie zwischen verschiedenen Computern verschoben werden, und die Benutzerdaten werden auf jedem Computer ausgelesen bzw. geschrieben. Microsoft Edge liest und schreibt nur aus dieser Datei. Es liegt in der Verantwortung des Admins, sicherzustellen, dass die Datei bei Bedarf verschoben wird.

## <a name="use-on-premises-sync"></a>Verwenden der lokalen Synchronisierung

Um die lokale Synchronisierung verwenden zu können, müssen Sie sie aktivieren, ein Profil einem AD-Konto zuordnen und optional den Speicherort der Benutzerdaten ändern.

### <a name="enable-on-premises-sync"></a>Aktivieren der lokalen Synchronisierung

Konfigurieren Sie zum Aktivieren der lokalen Synchronisierung in Microsoft Edge die Richtlinie [RoamingProfileSupportEnabled](./microsoft-edge-policies.md#roamingprofilesupportenabled).

### <a name="ensure-that-a-profile-is-associated-with-an-active-directory-account"></a>Stellen Sie sicher, dass ein Profil mit einem Active Directory-Konto verknüpft ist.

Die lokale Synchronisierung funktioniert nur mit dem Profil, das mit einem Active Directory (AD)-Konto verknüpft ist. Wenn kein solches Profil vorhanden ist, funktioniert die lokale Synchronisierung nicht. Um sicherzustellen, dass sich die Benutzer mit einem AD-Konto anmelden, konfigurieren Sie die Richtlinie [ConfigureOnPremisesAccountAutoSignIn](./microsoft-edge-policies.md#configureonpremisesaccountautosignin). Für die lokale Synchronisierung verwendet Microsoft Edge nur AD, um eine Identität für die Benutzerdaten zu erstellen, und es besteht keine direkte Beziehung zwischen der Art und Weise, wie Microsoft Edge lokale Daten liest und schreibt, und der Art und Weise, wie der Administrator das Roaming für einen AD-Benutzer konfiguriert hat.

### <a name="change-the-location-of-the-user-data-optional"></a>Ändern des Speicherorts der Benutzerdaten (optional)

Die Benutzerdaten werden standardmäßig in einer Datei namens **profile.pb** unter *%APPDATA%/Microsoft/Edge* gespeichert. Wenn Sie den Speicherort dieser Datei ändern möchten, konfigurieren Sie die Richtlinie [RoamingProfileLocation](./microsoft-edge-policies.md#roamingprofilelocation).

## <a name="changes-in-the-user-experience-when-on-premises-sync-is-enabled"></a>Änderungen in der Benutzerumgebung, wenn die lokale Synchronisierung aktiviert ist

Wenn die lokale Synchronisierung aktiviert ist, werden die Benutzer nicht aufgefordert, diese zu aktivieren. Darüber hinaus können die Benutzer die Synchronisierung in den Synchronisierungseinstellungen nicht deaktivieren, und sie können keine Synchronisierungstypen aktivieren, die von der lokalen Synchronisierung nicht unterstützt werden.

## <a name="on-premises-sync-usage-notes"></a>Verwendungshinweise zur lokalen Synchronisierung

### <a name="running-cloud-sync-and-on-premises-sync-on-the-same-computer"></a>Ausführen von Cloud-Synchronisierung und lokaler Synchronisierung auf demselben Computer

Die lokale Synchronisierung stört nicht die Cloud-Synchronisierung. Wenn in Microsoft Edge mehrere Microsoft-Konten oder Azure Active Directory-Profile vorhanden sind, die mit der Cloud synchronisiert werden, werden diese Profile weiterhin synchronisiert, während die lokale Synchronisierung aktiviert ist.

### <a name="running-microsoft-edge-on-more-than-one-computer-at-a-time-isnt-recommended"></a>Microsoft Edge auf mehreren Computern gleichzeitig auszuführen wird nicht empfohlen.

Da für die lokale Synchronisierung eine Benutzerdatendatei zwischen Computern verschoben wird, werden bei der lokalen Synchronisierung keine Änderungen zwischen gleichzeitigen Sitzungen synchronisiert. Aus diesem Grund funktioniert die lokale Synchronisierung am besten, wenn sie auf nicht mehr als einem Computer gleichzeitig verwendet wird. Wenn simultane lokale Sitzungen ausgeführt werden, werden Daten auf einem der Computer u. U. unerwartet von Daten von einem anderen Computer überschrieben, wenn Sie das nächste Mal eine Browsersitzung starten.

> [!NOTE]
> Microsoft Edge sperrt die **profile.pb**-Datei, wenn die lokale Synchronisierung aktiviert ist. Wenn die Ordnerumleitung verwendet wird, um eine einzelne **profile.pb**-Datei zwischen verschiedenen Computern freizugeben, kann nur eine der Instanzen von Microsoft Edge gestartet werden, die diese Datei verwendet.

### <a name="using-other-sync-policies-with-on-premises-sync"></a>Verwenden anderer Synchronisierungsrichtlinien mit der lokalen Synchronisierung

Die Richtlinie [SyncTypesListDisabled](./microsoft-edge-policies.md#synctypeslistdisabled) kann verwendet werden, um die Synchronisierung der Favoriten oder Einstellungen bei Bedarf selektiv zu deaktivieren. Die Richtline [SyncDisabled](./microsoft-edge-policies.md#syncdisabled) hat keine Auswirkungen auf die lokale Synchronisierung.

## <a name="see-also"></a>Weitere Informationen

- [Angebotsseite für Microsoft Edge für Unternehmen](https://aka.ms/EdgeEnterprise)
- [Microsoft Edge und Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md)
- [Microsoft Edge Enterprise-Synchronisierung](microsoft-edge-enterprise-sync.md)