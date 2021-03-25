---
title: Microsoft Edge-Unterstützung für Windows Information Protection
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 04/24/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Edge-Unterstützung für Windows Information Protection
ms.openlocfilehash: a9981947462627ae4884f18f4df6accf2ee60f12
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/24/2021
ms.locfileid: "11447189"
---
# <a name="microsoft-edge-support-for-windows-information-protection-wip"></a>Microsoft Edge-Unterstützung für Windows Information Protection (WIP)

In diesem Artikel wird beschrieben, wie Windows Information Protection (WIP) von Microsoft Edge unterstützt wird.

> [!NOTE]
> Dies bezieht sich auf Microsoft Edge Version 81 oder neuer.

## <a name="overview"></a>Übersicht

Windows Information Protection (WIP) ist ein Windows 10-Feature, das Unternehmensdaten vor unbefugtem Zugriff oder versehentlicher Offenlegung schützt. Mit dem Anstieg der Remotearbeit besteht das Risiko, dass Unternehmensdaten außerhalb des Arbeitsplatzes geteilt werden. Dieses Risiko erhöht sich, wenn persönliche und berufliche Aktivitäten auf Unternehmensgeräten stattfinden.

Microsoft Edge unterstützt WIP beim Schutz von Inhalten in einer Webumgebung, in der Benutzer häufig Inhalte freigeben und verteilen.

### <a name="system-requirements"></a>Systemanforderungen

Die folgenden Anforderungen gelten für Geräte, die WIP im Unternehmen verwenden:

- Windows10, Version 1607 oder höher
- Nur Windows-Client-SKUs
- Eine der unter [WIP-Voraussetzungen](/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip#prerequisites) beschriebenen Verwaltungslösungen

### <a name="windows-information-protection-benefits"></a>Vorteile von Windows Information Protection

WIP bietet die folgenden Vorteile:

- Eindeutige Trennung zwischen persönlichen Daten und Unternehmensdaten, ohne dass Mitarbeiter zwischen Umgebungen oder Apps wechseln müssen
- Zusätzlicher Schutz von Daten für vorhandene Branchen-Apps, ohne dass die Apps aktualisiert werden müssen
- Die Möglichkeit, aus der Ferne Unternehmensdaten von den für das Intune Mobile Device Management (MDM) registrierten Geräten zu löschen, ohne dass persönliche Daten hiervon betroffen sind. 
- Überwachungsberichte zum Nachverfolgen von Problemen und für Abhilfemaßnahmen, z. B. Benutzerschulungen zum Thema Compliance.
- Integration in Ihr bestehendes Verwaltungssystem zum Konfigurieren, Bereitstellen und Verwalten von WIP. Einige Beispiele sind Microsoft Intune, Microsoft Endpoint Configuration Manager oder Ihr aktuelles System für die mobile Geräteverwaltung (Mobile Device Management, MDM).

## <a name="wip-policy-and-protection-modes"></a>WIP-Richtlinie und-Schutzmodi

Mithilfe von Richtlinien können Sie die vier in der folgenden Tabelle beschriebenen Schutzmodi konfigurieren. Weitere Informationen finden Sie unter [WIP-Schutzmodi](/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip#wip-protection-modes).

| Modus | Beschreibung |
|------|-------------|
| Blockieren | WIP sucht nach unerwünschten Datenfreigaben und hindert Mitarbeiter daran, den Schritt auszuführen. Diese Suche kann die gemeinsame Nutzung von Unternehmensdaten in nicht vom Unternehmen geschützten Apps sowie außerdem die gemeinsame Nutzung von Unternehmensdaten zwischen Apps oder Freigabeversuche außerhalb des Netzwerk Ihrer Organisation umfassen. |
| Allow Overrides | WIP ermittelt ungeeignete Datenfreigaben und warnt Mitarbeiter davor, eine potenziell unsichere Aktion auszuführen. Bei diesem Verwaltungsmodus können Mitarbeiter die Richtlinie jedoch außer Kraft setzen und die Daten freigeben, wobei die Aktion jedoch in ihrem Überwachungsprotokoll protokolliert wird. |
| Unbeaufsichtigt | WIP wird im Hintergrund ausgeführt, wobei unangemessene Datenfreigaben protokolliert werden, ohne irgendetwas anzuhalten, das für die Interaktion des Mitarbeiters im Modus „Außerkraftsetzung“ erforderlich gewesen wäre. Unerlaubte Aktionen, z.B. wenn Apps unzulässigerweise versuchen, auf eine Netzwerkressource oder auf WIP-geschützte Daten zuzugreifen, werden weiterhin verhindert. |
| Deaktiviert | WIP ist deaktiviert, und Ihre Daten werden weder geschützt noch überwacht. Nachdem WIP deaktiviert wurde, wird versucht, alle durch WIP gekennzeichneten Dateien auf den lokal angeschlossenen Laufwerken zu entschlüsseln. Ihre vorherigen Entschlüsselungs- und Richtlinieninformationen werden nicht automatisch erneut angewendet, wenn Sie den WIP-Schutz wieder aktivieren.
 |

## <a name="wip-features-supported-in-microsoft-edge"></a>In Microsoft Edge unterstützte WIP-Features

Ab Version 81 von Microsoft Edge werden die folgenden Features unterstützt:

- Arbeitsbezogene Websites werden durch ein Aktenkoffer-Symbol in der Adressleiste angezeigt.  
- Dateien, die von einem arbeitsbezogenen Speicherort heruntergeladen wurden, werden automatisch verschlüsselt.
- Durchsetzung der Ebenen Silent/Block/Override für das Hochladen von arbeitsbezogenen Dateien an nicht arbeitsbezogene Speicherorte.  
- Durchsetzung der Ebenen Silent/Block/Override für Drag & Drop-Aktionen.
- Durchsetzung der Ebenen Silent/Block/Override für Zwischenablage-Aktionen.
- Beim Navigieren zu arbeitsbezogenen Speicherorten von nicht arbeitsbezogenen Profilen aus erfolgt eine automatische Umleitung an das (der Azure AD-Identität zugeordnete) Arbeitsprofil.
- Der IE-Modus unterstützt die vollständige WIP-Funktionalität.

## <a name="working-with-wip-in-microsoft-edge"></a>Arbeiten mit WIP in Microsoft Edge

Nach der Aktivierung der WIP-Unterstützung für Microsoft Edge wird es Benutzern angezeigt, wenn sie auf arbeitsbezogene Informationen zugreifen. Der nächste Screenshot zeigt das Symbol „Aktenkoffer“ in der Adressleiste, das anzeigt, dass über den Browser auf arbeitsbezogene Informationen zugegriffen wird.

 ![Adressleistenanzeige für arbeitsbezogene Websites](./media/microsoft-edge-security-windows-information-protection/microsoft-edge-wip-notify.png)

In Microsoft Edge können Benutzer geschützte Inhalte auf nicht genehmigten Websites freizugeben. Der nächste Screenshot zeigt die Microsoft Edge-Eingabeaufforderung, die es einem Benutzer gestattet, geschützte Inhalte auf einer nicht genehmigten Website zu verwenden.

 ![Aufforderung für die Außerkraftsetzung des Inhaltsschutzes](./media/microsoft-edge-security-windows-information-protection/microsoft-edge-wip-override.png)

## <a name="configure-policies-to-support-wip"></a>Konfigurieren von Richtlinien zur Unterstützung von WIP

Um WIP mit Microsoft Edge verwenden zu können, müssen Sie über ein Arbeitsprofil verfügen.

### <a name="ensure-the-presence-of-a-work-profile"></a>Sicherstellen des Vorhandenseins eines Arbeitsprofils

Bei hybrid verbundenen Computern wird Microsoft Edge automatisch mit dem Azure Active Directory-Konto (Azure AD) angemeldet. Um sicherzustellen, dass Benutzer dieses Profil, das für WIP benötigt wird, nicht entfernen, konfigurieren Sie die folgende Richtlinie:

- [NonRemovableProfileEnabled](./microsoft-edge-policies.md#nonremovableprofileenabled)

> [!NOTE]
> Wenn Ihre Umgebung nicht hybrid verbunden ist, können Sie mit diesen Anweisungen eine Hybridverbindung herstellen: [Planen Ihrer Implementierung einer hybriden Einbindung in Azure Active Directory](/azure/active-directory/devices/hybrid-azuread-join-plan).

Wenn eine Hybridverbindung keine Option ist, können Sie lokale Active Directory-Konten verwenden, um Microsoft Edge zu ermöglichen, automatisch spezielle Arbeitsprofile mit den Domänenkonten der Benutzer zu erstellen. Bitte beachten Sie, dass für lokale Konten möglicherweise nicht alle Features von Azure AD vorhanden sind, wie z.B. Cloudsynchronisierung, Office NTP usw.)

#### <a name="active-directory-ad-accounts"></a>Active Directory (AD)-Konten

Für AD-Konten müssen Sie die folgende Richtlinie konfigurieren, damit Microsoft Edge automatisch ein spezielles Arbeitsprofil erstellt.

- [ConfigureOnPremisesAccountAutoSignIn](./microsoft-edge-policies.md#configureonpremisesaccountautosignin)

### <a name="windows-policies-for-wip"></a>Windows-Richtlinien für WIP

Sie können WIP mithilfe von Windows-Richtlinien konfigurieren. Weitere Informationen finden Sie unter [Erstellen und Bereitstellen von WIP-Richtlinien mithilfe von Microsoft Intune](/windows/security/information-protection/windows-information-protection/overview-create-wip-policy)

## <a name="frequently-asked-questions"></a>Häufig gestellte Fragen

### <a name="how-do-i-resolve-error-code--2147024540"></a>Wie behebe ich den Fehler mit dem Code -2147024540?

Dieser Fehlercode entspricht dem folgenden Windows Information Protection-Fehler: *ERROR_EDP_POLICY_DENIES_OPERATION: der angeforderte Vorgang wurde durch die Windows Information Protection-Richtlinie blockiert. Wenn Sie weitere Informationen benötigen, wenden Sie sich an den System Administrator.*

Microsoft Edge zeigt diesen Fehler an, wenn die Organisation Windows Information Protection (WIP) aktiviert hat, um Benutzern mit genehmigten Anwendungen nur den Zugriff auf Unternehmensressourcen zu gestatten. Da Microsoft Edge sich in diesem Fall nicht in der Liste genehmigter Anwendungen befindet, muss der Administrator die WIP-Richtlinien aktualisieren, um Zugriff auf Microsoft Edge zu gewähren.

Der folgende Screenshot zeigt, wie Microsoft Intune verwendet wird, um Microsoft Edge als zulässige App für WIP hinzuzufügen.

 ![Intune-Dialogfeld zum Hinzufügen von Microsoft Edge als App für WIP](./media/microsoft-edge-security-windows-information-protection/microsoft-edge-wip-exemption.png)

Wenn Sie Microsoft Intune nicht verwenden, laden Sie das Richtlinienupdate in der Datei [WIP-Richtlinie für Enterprise AppLocker](https://download.microsoft.com/download/8/9/9/8995d820-065c-4ab1-aa2a-9d6dc0cd7ffa/MsEdge%20-%20WIP%20Enterprise%20AppLocker%20Policy%20Files.zip) herunter, und wenden Sie diese an.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise) 
- [Schützen von Unternehmensdaten mithilfe von Windows Information Protection](/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip)