---
title: Edge für Virtualisierungsdesktopinfrastruktur
ms.author: anlake
author: AndreaLBarr
manager: collw
ms.date: 06/08/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Edge für Virtualized Desktop Infrastructure.
ms.openlocfilehash: eaad1b72934b336ce86d14dd8da92a6984d21914
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2021
ms.locfileid: "11618121"
---
# <a name="microsoft-edge-for-virtualized-desktop-infrastructure"></a>Microsoft Edge für Virtualized Desktop Infrastructure

In diesem Artikel werden die Anforderungen und Einschränkungen für die Verwendung von Microsoft Edge in einer virtualisierten Umgebung beschrieben.

## <a name="what-is-vdi"></a>Was ist VDI?

Virtual Desktop Infrastructure (VDI) ist eine Virtualisierungstechnologie, die ein Desktopbetriebssystem und Anwendungen auf einem zentralen Server in einem Rechenzentrum hostet. Dies ermöglicht eine vollständig personalisierte Desktopumgebung für Benutzer mit einer vollständig gesicherten und kompatiblen zentralen Quelle.

Microsoft Edge kann in einer solchen virtualisierten Umgebung auf die gleiche Weise wie auf dem lokalen Gerät verwendet werden, während sie in einer sicheren und kontrollierten Serverumgebung ausgeführt werden. Je nach ausgewählter VDI-Lösung kann es auch möglich sein, Ihren Benutzern einen nahtlosen Zugriff auf Intranetanwendungen und -websites zu ermöglichen.

Die meisten Features von Edge werden in VDI-Umgebungen ohne spezielle Konfiguration unterstützt. Um jedoch eine optimale Benutzererfahrung sicherzustellen, empfiehlt es sich, die nachstehenden Anleitungen zu befolgen.

## <a name="platforms-certified-for-edge"></a>Für Edge zertifizierte Plattformen

- Azure Virtual Desktop
- Citrix Virtual Apps and Desktops (früher bekannt als XenApp und XenDesktop)

Andere VDI-Lösungen wurden zwar noch nicht vom Edge-Team überprüft, es wird jedoch erwartet, dass die häufigsten Workflows in Edge unterstützt werden sollten. Die unten aufgeführten Anleitungen gelten möglicherweise oder nicht für die von Ihnen ausgewählte Lösung.

## <a name="edge-on-vdi-performance-considerations"></a>Überlegungen zur Leistung von Edge auf VDI

Berücksichtigen Sie beim Entwickeln Ihrer VDI-Umgebung sorgfältig die Workflows und Anforderungen Ihrer Benutzer, um eine optimale Leistung zu erzielen, sowie die Grenzen Ihrer Serverkonfiguration.

Edge empfiehlt die folgenden Mindestanforderungen für die Bereitstellung von Edge in VDI-Umgebungen:

- vCPU – 2-4 Kerne pro Benutzer
- RAM – 1GB pro Benutzer

Bitte beachten Sie, dass große komplexe Webanwendungen und Erweiterungen mehr Arbeitsspeicher benötigen und bei der Konfiguration Ihrer Umgebung berücksichtigt werden müssen.

## <a name="edge-on-non-persisted-vdi-environments"></a>Edge in nicht persistenten VDI-Umgebungen

Viele VDI-Lösungen ermöglichen den Zugriff auf persistente Umgebungen, bei denen den Benutzern eine virtuelle Umgebung zugewiesen wird, die zwischen den Sitzungen bestehen bleibt, und auf nicht persistente Umgebungen, bei denen die Benutzer einem von mehreren verfügbaren Rechnern zugewiesen werden, möglicherweise einem anderen Rechner pro Sitzung, wobei die Benutzerdaten zwischen den Sitzungen synchronisiert werden können oder auch nicht.

Wenn man eine nicht persistente Umgebung verwendet, erstellt man normalerweise ein "Golden Image", das für jedes Gerät verwendet wird und die benötigten Apps und Konfigurationen enthält. Im Folgenden finden Sie unsere Empfehlungen für die Vorbereitung von Edge auf ein solches Image.

### <a name="deploy-edge"></a>Bereitstellen von Edge

Wenn Sie Windows 10 Version 1803 und höher verwenden, sollten Sie Microsoft Edge auf Ihrem System installiert haben. Wenn Sie jedoch eine ältere Version von Windows verwenden oder einen anderen Edge-Kanal bereitstellen möchten, werden die folgenden Schritte empfohlen.

1. Laden Sie das Edge-MSI-Paket herunter, das ihrem VDI-VM-Betriebssystem entspricht:

    - [Herunterladen von Microsoft Edge for Business – Microsoft](https://www.microsoft.com/edge/business/download)

2. Installieren Sie die MSI-Datei auf dem virtuellen VDI-Computer, indem Sie den folgenden Befehl ausführen:

    - `msiexec /i <path_to_msi> /qn /norestart /l*v <install_logfile_name>`

### <a name="disable-automatic-updates"></a>Deaktivieren von automatischen Updates

Für nicht persistente Computer empfiehlt es sich, automatische Updates zu deaktivieren und stattdessen Edge zu aktualisieren, indem Sie das "Golden Image" aktualisieren, um sicherzustellen, dass keine Versionskonflikte zwischen dem Computerpool bestehen.

Lesen Sie die folgenden Richtlinien zum Deaktivieren von automatischen Updates:

- [Die Updaterichtlinie überschreibt die Standardrichtlinie](/deployedge/microsoft-edge-update-policies#updatedefault)

- [Außerkraftsetzung von Updaterichtlinien](/deployedge/microsoft-edge-update-policies#update)

### <a name="profile-management"></a>Profilverwaltung

Bei nicht persistenten Umgebungen ist es wichtig zu berücksichtigen, dass virtuelle Computer möglicherweise nicht den Benutzerstatus zwischen Sitzungen beibehalten oder Benutzern eine VM zugewiesen wird, die sie noch nie verwendet haben und daher keine Benutzerdaten aufweisen.

Edge unterstützt mehrere Methoden zum Synchronisieren von Benutzerdaten, sodass sie verfügbar sind, unabhängig davon, wie sie auf Edge zugreifen.

### <a name="azure-ad-sync"></a>Microsoft Azure Active Directory-Synchronisierungsdienste

Wenn Ihr Azure AD-Plan dies unterstützt, ist Enterprise-Synchronisierung die schnellste und einfachste Methode, um sicherzustellen, dass Edge-Benutzerdaten mit allen Benutzergeräten synchronisiert werden.  

Weitere Informationen zu Anforderungen und Konfiguration finden Sie im Folgenden.  

- [Konfigurieren von Microsoft Edge Enterprise-Synchronisierung | Microsoft-Dokumentation](/deployedge/microsoft-edge-enterprise-sync)

### <a name="on-premise-sync-for-active-directory-users"></a>Lokale Synchronisierung für Active Directory-Benutzer

Bei der lokalen Synchronisierung speichert Microsoft Edge die Favoriten und Einstellungen eines Active Directory-Benutzers in einer Datei, die problemlos zwischen verschiedenen Computern verschoben werden kann.  

Weitere Informationen zu Anforderungen und Konfiguration finden Sie im Folgenden.  

- [Lokale Synchronisierung für Active Directory (AD)-Benutzer | Microsoft-Dokumentation](/deployedge/microsoft-edge-on-premises-sync)

### <a name="user-profile-redirection"></a>Benutzerprofilumleitung  

Es gibt mehrere Lösungen zum Migrieren und Umleiten des gesamten Benutzerordners, um sicherzustellen, dass der Benutzerkontext in solchen nicht persistenten Umgebungen beibehalten wird. Wenden Sie sich an Ihren VDI-Anbieter, um die empfohlene Lösung zu ermitteln.

Einige beliebte Lösungen sind:

- [FSLogix-Übersicht – FSLogix | Microsoft-Dokumentation](/fslogix/overview)
- [Konfigurieren der Citrix-Profilverwaltung](https://support.citrix.com/article/CTX222893)

Es kann auch empfohlen werden, bei Verwendung dieser Methode unnötige Ordner aus dem gesicherten Benutzerordner auszuschließen, um die anfänglichen Ladezeiten zu reduzieren, wenn sich Benutzer bei einem Computer anmelden und das Profil migriert wird. Wenn ja, empfehlen wir, die folgenden Ordner aus der Sicherung auszuschließen, um die Größe zu verringern.

- %LocalAppData%\Microsoft\Edge\User Data\Default\Cache
- %LocalAppData%\Microsoft\Edge\User Data\Default\Code Cache
- %LocalAppData%\Microsoft\Edge\User Data\Default\JumpListIconsTopSites
- %LocalAppData%\Microsoft\Edge\User Data\Default\JumpListIconsRecentClosed

## <a name="known-issues"></a>Bekannte Probleme

### <a name="microsoft-edge-crashes-in-older-versions-of-xenapp-and-xendesktop"></a>Abstürzen von Microsoft Edge in älteren Versionen von XenApp und XenDesktop

Dieses Problem sollte in neueren Versionen behoben werden. Wenn dieses Problem jedoch in Ihrer Umgebung auftritt, können Sie das Problem umgehen, indem Sie Citrix API Hooks für Edge deaktivieren. Weitere Informationen finden Sie unter [Deaktivieren von Citrix API Hooks auf Anwendungsbasis.](https://support.citrix.com/article/CTX107825)

### <a name="degraded-performance-when-rendering-pages-with-exceptionally-large-html-tables"></a>Beeinträchtigte Leistung beim Rendering von Seiten mit ungewöhnlich großen HTML-Tabellen

Die folgenden Citrix-Richtlinien sind dafür bekannt, dass HTML-Seiten mit sehr großen Tabellen (mehr als 30000 Zeilen) langsam gerendert werden.

- Automatische Tastaturanzeige
- Remotezugriff auf das Kombinationsfeld

Weitere Informationen finden Sie unter [Richtlinieneinstellungen für die mobile Benutzeroberfläche (citrix.com)](https://docs.citrix.com/citrix-virtual-apps-desktops/policies/reference/ica-policy-settings/mobile-experience-policy-settings.html). Durch das Deaktivieren dieser Richtlinien sollte das Problem behoben werden.

### <a name="windows-account-manager-authorization-scenarios-ie--azure-sync-fail-in-edge-when-run-as-a-citrix-seamless-application"></a>Windows-Kontomnager-Autorisierungsszenarien (d.h.  Azure-Synchronisierung) schlägt in Edge fehl, wenn es als nahtlose Citrix-Anwendung ausgeführt wird

Dies ist ein bekanntes Problem in Edge und anderen Anwendungen, die WAM (d.h. Office) verwenden, da Windows-Komponenten, die für solche Szenarien erforderlich sind, nicht initialisiert werden, wenn sie im "nahtlosen" Modus ausgeführt werden. Problemumgehung:

- Verwenden Sie Edge über einen Remotedesktop zum Citrix-Host anstatt als nahtlose Remoteanwendung.
- Verwenden Sie stattdessen Azure Virtual Desktop-Remote-Apps, die über Abhilfemaßnahmen für dieses Problem verfügen.
