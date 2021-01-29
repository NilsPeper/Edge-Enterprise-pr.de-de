---
title: Automatische Aktivierung des Kennwortmonitors für Benutzer
ms.author: supalsul
author: dan-wesley
manager: tulasim
ms.date: 01/26/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Automatische Aktivierung des Kennwortmonitors für Benutzer
ms.openlocfilehash: 2f796f0cd1bbb437f83d04a8bd59586ef7b6a982
ms.sourcegitcommit: 187203e9eaa9c48c59095b7e7d625d3081a6ba19
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/27/2021
ms.locfileid: "11304535"
---
# Automatische Aktivierung des Kennwortmonitors für Benutzer

In diesem Artikel wird beschrieben, wie der Kennwortmonitor in Microsoft Edge für ausgewählte Benutzer aktiviert wird, und Administratoren erfahren, wie sie die Aktivierung der Überwachung steuern können.

> [!NOTE]
> Dieser Artikel bezieht sich auf Microsoft Edge Version 88 oder höher.

## Einführung, Vorteile und Verfügbarkeit

Der Kennwortmonitor hilft Microsoft Edge-Benutzern, ihre Onlinekonten zu schützen, indem sie informiert werden, ob eines ihrer Kennwörter in einem Onlineleck gefunden wurde. Onlinelecks oder Datenschutzverletzungen geschehen, wenn Angreifer Daten über Apps oder Websites von Drittanbietern stehlen. Weitere Informationen finden Sie im Microsoft Research Blog im Dokument [Kennwortmonitor: Schutz von Kennwörtern in Microsoft Edge](https://www.microsoft.com/research/blog/password-monitor-safeguarding-passwords-in-microsoft-edge/).

### Vorteile

Angesichts der Häufigkeit und des Umfangs dieser Onlineangriffe, ist diese Art von Schutz für jeden erforderlich. Microsoft Edge verfügt über die integrierte Möglichkeit, die gespeicherten Kennwörter eines Benutzers auf sicherem Wege mit Kennwörtern abzugleichen, die als gefährdet bekannt sind, und benachrichtigt den Benutzer, wenn eine Übereinstimmung gefunden wird.  

### Verfügbarkeit

Der Kennwortmonitor ist ab 21. Januar verfügbar im Stabilen Kanal, Version 88. Das Rollout erfolgt schrittweise, und es kann einige Wochen dauern, bis die folgende Meldung und Steuerung auf der Seite **Einstellungen** > **Profil** > **Kennwort** angezeigt wird.

:::image type="content" source="media/microsoft-edge-security-password-monitor/monitor-enable-option.png" alt-text="Option zum Aktivieren des Kennwortmonitors":::

## Konfigurieren von Gruppenrichtlinien für den Kennwortmonitor

Dieses Feature wird über die Gruppenrichtlinie [PasswordMonitorAllowed](https://docs.microsoft.com/deployedge/microsoft-edge-policies#passwordmonitorallowed) gesteuert.

Nach der Aktivierung der Richtlinie müssen Benutzer noch ihre Zustimmung geben, um das Feature zu aktivieren. Die Zustimmung ist erforderlich, da das Feature vertrauliche und personenbezogene Daten (Kennwörter) des Benutzers verwendet. Wenn das Feature mithilfe von Gruppenrichtlinien deaktiviert ist, können Benutzer diese Einstellung nicht außer Kraft setzen.  

## Aktivieren des Kennwortmonitors für Benutzer

Nachdem die Kennwortmonitor-Richtlinie aktiviert wurde, gibt es unterschiedliche Möglichkeiten, dieses Feature Benutzern zur Verfügung zu stellen.

- Automatische Aktivierung. Für Benutzer, die mit ihrem Geschäftskonto (Active Directory oder Azure Active Directory) angemeldet sind und ihre Kennwörter synchronisieren, wird dieses Funktion automatisch aktiviert. Die Benachrichtigung im nächsten Screenshot wird angezeigt, in der sie darüber informiert werden, dass das Feature aktiviert ist.

  :::image type="content" source="media/microsoft-edge-security-password-monitor/monitor-enabled-notice.png" alt-text="Hinweis "Kennwortmonitor aktiviert"":::

-  Einholen der ausdrücklichen Zustimmung. Benutzer, für die die Kennwortsynchronisierung nicht aktiviert ist, werden um die Berechtigung zum Aktivieren des Kennwortmonitors gebeten. Sie werden dazu aufgefordert, wenn die folgenden Aktionen auftreten:
   - Wenn ein Benutzer ein neues Kennwort speichert.
 
     :::image type="content" source="media/microsoft-edge-security-password-monitor/monitor-save-pw-prompt.png" alt-text="Eingabeaufforderung zum Speichern des Kennworts":::

   - Wenn sich ein Benutzer mit einem gespeicherten Kennwort beim Browser angemeldet hat.
  
     :::image type="content" source="media/microsoft-edge-security-password-monitor/monitor-after-signin.png" alt-text="Bestätigungsaufforderung nach der Anmeldung":::
   
- Direkte Aktivierung. Benutzer können das Feature jederzeit unter **Einstellungen** > **Kennwörter** aktivieren oder deaktivieren.

## Benutzerszenarien mit automatische Aktivierung des Kennwortmonitors

In der folgenden Tabelle sind Szenarien aufgeführt, in denen der Kennwortmonitor automatisch aktiviert ist. Zudem wird beschrieben, wie er auf Benutzergeräten funktioniert.

| Szenario | Basisbedingungen | Auswirkungen |
|--|--|--|
| 1 mit aktivierter Synchronisierung | Synchronisierung EIN<br>Zuvor aktiviertes Feature: Nein<br>Antwort auf Zustimmungsbenutzeroberfläche: Keine | Das Feature ist standardmäßig aktiviert, und eine Sprechblase mit einem Hinweis wird 2 Minuten nach dem Start des Browsers angezeigt.<br>– Wird die Synchronisierung danach deaktiviert, ist das Feature deaktiviert.<br>– Wird das Feature vor dem Ändern der Synchronisierung deaktiviert, wirkt sich die Synchronisierung nicht mehr auf das Feature aus.   |
| 2 mit aktivierter Synchronisierung | Synchronisierung EIN<br>Zuvor aktiviertes Feature: Ja<br>Antwort auf Zustimmungsbenutzeroberfläche: Keine | Featureeinstellung entspricht der Benutzerauswahl.  Beachten Sie, dass keine Sprechblase angezeigt wird und dass es keine Auswirkungen auf die Synchronisierungsänderung auf den Featurewert gibt.|
| 3 mit deaktivierter Synchronisierung | Synchronisierung AUS<br>Zuvor aktiviertes Feature: Nein<br>Antwort auf Zustimmungsbenutzeroberfläche: Keine | Die Synchronisierung ist deaktiviert, und das Feature bleibt deaktiviert.<br>– Wenn der Benutzer zu einem beliebigen Zeitpunkt danach die Synchronisierung aktiviert, ohne das Feature zu ändern: Das Feature wird aktiviert, und die Benachrichtigung über die automatische Aktivierung wird 2 Minuten nach Aktivierung der Synchronisierung angezeigt. <br> – Wenn die Synchronisierung wieder deaktiviert wird, wird das Feature deaktiviert. <br>– Wenn das Feature vor dem Aktivieren der Synchronisierung geändert wird, wirkt sich die Synchronisierung nicht mehr auf den Kennwortmonitor aus.  |  
| 4 mit deaktivierter Synchronisierung | Synchronisierung AUS<br>Zuvor aktiviertes Feature: Ja<br>Antwort auf Zustimmungsbenutzeroberfläche: Keine | Featureeinstellung und Benutzerauswahl bleiben identisch. Beachten Sie aber, dass keine Sprechblase angezeigt wird und dass es keine Auswirkungen auf die Synchronisierungsänderung auf den Featurewert gibt.  |

Auch wenn ein Benutzer mit einem Geschäftskonto angemeldet ist, für das eine der folgenden Aktionen über Richtlinien eingeschränkt ist, wird das Feature NICHT automatisch für den Benutzer aktiviert:

- Kennwortmonitor ist deaktiviert  
- Kennwortsynchronisierung ist deaktiviert
- Die Freigabe von Daten für Microsoft-Server ist deaktiviert.

## Häufig gestellte Fragen

### Wie kann der Kennwortmonitor für meine Organisation deaktiviert werden?

Sie können den Kennwortmonitor für Ihre Organisation deaktivieren durch:
- Verwenden der Gruppenrichtlinie "PasswordMonitorAllowed".
- Verhindern, dass Daten synchronisiert und an Microsoft-Server gesendet werden.

  > [!NOTE]
  > Der Kennwortmonitor kann auch dann funktionieren, wenn die Kennwortsynchronisierung deaktiviert ist, solange der Benutzer die explizite Zustimmung zum Aktivieren des Features erteilt oder es über "Einstellungen" selbst aktiviert hat.

### Was geschieht, wenn ein Benutzer, für den das Feature automatisch aktiviert wurde, den Kennwortmonitor über die Einstellungen deaktiviert?

Die Benutzereinstellung wird berücksichtigt, und das Feature bleibt für den Benutzer deaktiviert. Möglicherweise wird ihnen jedoch erneut ein Zustimmungsdialogfeld angezeigt, falls der Benutzer bisher noch nie auf die Zustimmungsaufforderung geantwortet hat.

## Weitere Informationen

- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)