---
title: Microsoft Edge für die virtuelle Desktopinfrastruktur (Virtual Desktop Infrastructure, VDI)
ms.author: anlake
author: dan-wesley
manager: collw
ms.date: 11/12/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Microsoft Edge für virtuelle Desktopinfrastruktur (Virtual Desktop Infrastructure, VDI).
ms.openlocfilehash: fe1c1a7acf0b514812ff0aaf8f7a2b307304657d
ms.sourcegitcommit: e7f3098d8b7d91cae20b5778a71a87daababc312
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2022
ms.locfileid: "12298133"
---
# <a name="microsoft-edge-for-virtual-desktop-infrastructure-vdi"></a>Microsoft Edge für die virtuelle Desktopinfrastruktur (Virtual Desktop Infrastructure, VDI)

In diesem Artikel werden die Anforderungen und Einschränkungen für die Verwendung von Microsoft Edge in einer virtuellen Umgebung beschrieben.

## <a name="what-is-vdi"></a>Was ist VDI?

Virtual Desktop Infrastructure (VDI) ist eine Desktopvirtualisierungstechnologie, die ein Betriebssystem und Anwendungen auf einem zentralen Server in einem Rechenzentrum hostet. Diese Technologie ermöglicht benutzern eine vollständig personalisierte Desktopumgebung auf einer sicheren und kompatiblen zentralen Quelle.

Microsoft Edge können in einer virtuellen Umgebung ähnlich wie auf einem lokalen Gerät verwendet werden. Ein virtueller Desktop nutzt eine sichere und kontrollierte Serverumgebung. Je nach ausgewählter VDI-Lösung kann es auch möglich sein, Ihren Benutzern einen nahtlosen Zugriff auf Intranetanwendungen und -websites zu ermöglichen.

Die meisten Microsoft Edge Features werden in VDI-Umgebungen ohne spezielle Konfiguration unterstützt. Um jedoch eine optimale Benutzererfahrung sicherzustellen, empfehlen wir, die folgenden Anleitungen zu lesen.

## <a name="platforms-certified-for-microsoft-edge"></a>Für Microsoft Edge zertifizierte Plattformen

Die folgenden Plattformen sind für Microsoft Edge zertifiziert:

- Azure Virtual Desktop
- Citrix Virtual Apps and Desktops (früher bekannt als XenApp und XenDesktop)

Obwohl andere VDI-Lösungen noch nicht vom Microsoft Edge Team zertifiziert wurden, wird erwartet, dass die gängigsten Workflows in Microsoft Edge unterstützt werden sollten. Die folgenden Anleitungen gelten möglicherweise oder nicht für die von Ihnen gewählte Lösung.

## <a name="performance-considerations-for-microsoft-edge-on-vdi"></a>Überlegungen zur Leistung bei Microsoft Edge auf VDI

Beim Entwerfen Ihrer VDI-Umgebung sollten Sie die Workflows und Anforderungen Ihrer Benutzer sorgfältig berücksichtigen, um eine optimale Leistung zu erzielen, und die Grenzen Ihrer Serverkonfiguration verstehen.

Für die Bereitstellung von Microsoft Edge in einer VDI-Umgebung werden die folgenden Mindestanforderungen empfohlen:

- vCPU – 2 bis 4 Kerne pro Benutzer
- RAM – 1 GB pro Benutzer

Große und komplexe Webanwendungen und Erweiterungen benötigen mehr Arbeitsspeicher und Verarbeitungsfunktionen, die beim Konfigurieren Ihrer virtuellen Umgebung berücksichtigt werden müssen.

## <a name="microsoft-edge-on-non-persisted-vdi-environments"></a>Microsoft Edge in nicht persistenten VDI-Umgebungen

Viele VDI-Lösungen ermöglichen den Zugriff auf persistente Umgebungen, bei denen den Benutzern eine virtuelle Umgebung zugewiesen wird, die zwischen den Sitzungen bestehen bleibt, und auf nicht persistente Umgebungen, bei denen die Benutzer einem von mehreren verfügbaren Rechnern zugewiesen werden, möglicherweise einem anderen Rechner pro Sitzung, wobei die Benutzerdaten zwischen den Sitzungen synchronisiert werden können oder auch nicht.

Bei Verwendung einer nicht dauerhaften Umgebung erstellt man in der Regel ein "goldenen Image", das die erforderlichen Apps und Konfigurationen enthält, die auf jedem Gerät bereitgestellt werden. Verwenden Sie die folgenden Empfehlungen als Leitfaden für die Vorbereitung eines goldenen Bilds.

### <a name="deploy-microsoft-edge"></a>Bereitstellen von Microsoft Edge

Wenn Sie Windows 10, Version 1803 und höher, verwenden, sollten Sie bereits Microsoft Edge auf Ihrem System installiert haben. Wenn Sie jedoch eine ältere Version von Windows verwenden oder einen anderen Microsoft Edge Kanal bereitstellen möchten, führen Sie die folgenden Schritte aus:

1. Laden Sie das Microsoft Edge MSI-Paket herunter, das ihrem VDI-VM-Betriebssystem entspricht:

    - [Herunterladen von Microsoft Edge for Business – Microsoft](https://www.microsoft.com/edge/business/download)

2. Führen Sie den folgenden Befehl aus, um die MSI-Datei auf dem virtuellen VDI-Computer (VM) zu installieren:

    - `msiexec /i <path_to_msi> /qn /norestart /l*v <install_logfile_name>`

### <a name="disable-automatic-updates"></a>Deaktivieren von automatischen Updates

Bei nicht persistenten Computern empfiehlt es sich, automatische Updates zu deaktivieren und Microsoft Edge durch Aktualisieren des goldenen Images zu aktualisieren, um sicherzustellen, dass keine Versionskonflikte zwischen dem Pool virtueller Computer bestehen.

Weitere Informationen zum Deaktivieren automatischer Updates finden Sie in den folgenden Richtlinien:

- [Die Updaterichtlinie überschreibt die Standardrichtlinie](/deployedge/microsoft-edge-update-policies#updatedefault)

- [Außerkraftsetzung von Updaterichtlinien](/deployedge/microsoft-edge-update-policies#update)

### <a name="profile-management"></a>Profilverwaltung

Bei nicht beibehaltenen Setups ist es wichtig zu berücksichtigen, dass virtuelle Computer möglicherweise nicht den Benutzerstatus zwischen Sitzungen beibehalten oder Benutzern eine VM zugewiesen wird, die sie noch nie verwendet haben. In diesem Szenario verfügt der virtuelle Computer nicht über die Daten des Benutzers.

Microsoft Edge unterstützt mehrere Methoden zum Synchronisieren von Benutzerdaten, sodass sie verfügbar sind, unabhängig davon, wie sie auf Microsoft Edge zugreifen. Zwei Methoden sind Azure Active Directory (Azure AD) Synchronisierung und lokale Synchronisierung für AD-Benutzer.

### <a name="azure-ad-sync"></a>Microsoft Azure Active Directory-Synchronisierungsdienste

Wenn Ihr Azure AD Plan dies unterstützt, ist Enterprise Synchronisierung die schnellste und einfachste Methode, um sicherzustellen, dass Microsoft Edge Benutzerdaten mit allen Benutzergeräten synchronisiert werden. Weitere Informationen finden Sie unter [Konfigurieren Microsoft Edge Unternehmenssynchronisierung](/deployedge/microsoft-edge-enterprise-sync)

### <a name="on-premise-sync-for-active-directory-users"></a>Lokale Synchronisierung für Active Directory-Benutzer

Bei der lokalen Synchronisierung speichert Microsoft Edge die Favoriten und Einstellungen eines Active Directory-Benutzers in einer Datei, die problemlos zwischen verschiedenen Computern verschoben werden kann.  

Weitere Informationen zu Anforderungen und Konfiguration finden Sie unter ["Lokale Synchronisierung für Active Directory (AD)-Benutzer"](/deployedge/microsoft-edge-on-premises-sync)

### <a name="user-profile-redirection"></a>Benutzerprofilumleitung  

Es gibt mehrere Lösungen zum Migrieren und Umleiten des gesamten Benutzerordners, um sicherzustellen, dass der Benutzerkontext in einer nicht dauerhaften Umgebung beibehalten wird. Wenden Sie sich an Ihren VDI-Anbieter, um die empfohlene Lösung für Ihre Umgebung zu ermitteln.

Einige beliebte Lösungen umfassen die folgenden Optionen:

- [FSLogix-Übersicht – FSLogix](/fslogix/overview)
- [Konfigurieren der Citrix-Profilverwaltung](https://support.citrix.com/article/CTX222893)

In einigen Fällen sollten unnötige Ordner aus dem gesicherten Benutzerordner ausgeschlossen werden, um die anfänglichen Ladezeiten zu reduzieren, wenn sich ein Benutzer bei einem Computer anmeldet und sein Profil migriert wird. Wenn ja, empfehlen wir, die folgenden Ordner aus der Sicherung auszuschließen, um die Größe zu verringern.

- %LocalAppData%\Microsoft\Edge\User Data\Default\Cache
- %LocalAppData%\Microsoft\Edge\User Data\Default\Code Cache
- %LocalAppData%\Microsoft\Edge\User Data\Default\JumpListIconsTopSites
- %LocalAppData%\Microsoft\Edge\User Data\Default\JumpListIconsRecentClosed

## <a name="known-issues"></a>Bekannte Probleme

### <a name="microsoft-edge-crashes-in-older-versions-of-xenapp-and-xendesktop"></a>Abstürzen von Microsoft Edge in älteren Versionen von XenApp und XenDesktop

Dieses Problem sollte in neueren Versionen dieser Produkte behoben werden. Wenn dieses Problem jedoch in Ihrer Umgebung auftritt, können Sie das Problem umgehen, indem Sie Citrix API Hooks für Microsoft Edge deaktivieren. Weitere Informationen finden Sie unter ["Deaktivieren von Citrix API Hooks pro Anwendung".](https://support.citrix.com/article/CTX107825)

### <a name="degraded-performance-when-rendering-pages-with-exceptionally-large-html-tables"></a>Beeinträchtigte Leistung beim Rendering von Seiten mit ungewöhnlich großen HTML-Tabellen

Die folgenden Citrix-Richtlinien sind dafür bekannt, dass html-Seiten mit großen Tabellen (mehr als 30.000 Zeilen) langsam gerendert werden.

- Automatische Tastaturanzeige
- Remotezugriff auf das Kombinationsfeld

Weitere Informationen finden Sie unter [Richtlinieneinstellungen für mobile Umgebungen (citrix.com).](https://docs.citrix.com/citrix-virtual-apps-desktops/policies/reference/ica-policy-settings/mobile-experience-policy-settings.html) Durch das Deaktivieren dieser Richtlinien sollte das Problem behoben werden.

### <a name="windows-account-manager-authorization-scenarios-that-is-azure-sync-fail-in-microsoft-edge-when-run-as-a-citrix-seamless-application"></a>Windows Konto-Manager-Autorisierungsszenarien (d. b. Azure-Synchronisierung) schlagen in Microsoft Edge fehl, wenn sie als nahtlose Citrix-Anwendung ausgeführt werden

Dies ist ein bekanntes Problem in Microsoft Edge und anderen Anwendungen, die WAM (d. h. Office) verwenden, da erforderliche Windows Komponenten nicht initialisiert werden, wenn sie im "nahtlosen" Modus ausgeführt werden. Versuchen Sie eine der folgenden Optionen, um dieses Problem zu umgehen:

- Verwenden Sie Microsoft Edge über einen Remotedesktop zum Citrix Host anstelle einer nahtlosen Remoteanwendung.
- Verwenden Sie stattdessen Azure Virtual Desktop-Remote-Apps, die Gegenmaßnahmen für dieses Problem haben.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)
- [Azure Virtual Desktop](https://azure.microsoft.com/services/virtual-desktop/)