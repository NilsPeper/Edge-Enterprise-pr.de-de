---
title: Microsoft Edge-Rollback für Unternehmen
ms.author: v-danwes
author: dan-wesley
manager: srugh
ms.date: 11/30/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Zurücksetzen von Microsoft Edge auf eine vorherige Version
ms.openlocfilehash: 69fdfd29572dd6eda9f7eb7cbd4c2500851dcafc
ms.sourcegitcommit: 63a094a5268bb3b4819269438357095acd79abac
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/30/2020
ms.locfileid: "11192425"
---
# Zurücksetzen von Microsoft Edge auf eine vorherige Version

In diesem Artikel wird beschrieben, wie Sie mithilfe des Rollback-Features ein Rollback zu einer früheren Version von Microsoft Edge durchführen können.

>[!NOTE]
>Dieser Artikel bezieht sich auf Microsoft Edge Version 86 oder höher.

## Einführung in die Zurücksetzung

Durch ein Rollback können Sie Ihre Microsoft Edge-Browserversion auf eine frühere Version zurücksetzen. Das Rollback-Feature dient als Sicherheitsnetz für Unternehmen, die Microsoft Edge bereitstellen. Es bietet eine Möglichkeit zur Behandlung von Problemen mit Microsoft Edge. Zu den Vorteilen eines Rollbacks zählt die Möglichkeit, schnell und einfach zu einer vorherigen Browserversion zurückzukehren. Ein Rollback verringert die potenziellen Auswirkungen eines Microsoft Edge-Problems auf Geschäftsvorgänge.

## Vorbemerkungen

Es ist wichtig zu verstehen, wie das Rollback-Feature in einer Microsoft Edge-Umgebung installiert wird. Sie können das Rollback mithilfe von zwei unterschiedlichen Methoden durchführen: manuell mit einer MSI-Datei oder mithilfe von Microsoft Edge Update- und Gruppenrichtlinien. Wir empfehlen außerdem Gruppen-Richtlinien für eine reibungslosere Bereitstellung zu nutzen.

### Empfehlungen

Das Rollback-Feature dient als vorübergehender Fix für Probleme, die eventuell durch ein Microsoft Edge-Browserupdate entstehen. Wir empfehlen Benutzern, die neueste Version des Microsoft Edge-Browsers zu installieren, um die durch die aktuellsten Sicherheitsupdates bereitgestellten Schutzfunktionen nutzen zu können. Ein Rollback zu einer früheren Version birgt Risiken, die mit bekannten Sicherheitsproblemen zu tun haben.

Bevor Sie die Browserversion vorübergehend zurücksetzen, empfehlen wir dringend, die Synchronisierung für alle Benutzer in Ihrer Organisation zu aktivieren. Wenn Sie die Synchronisierung nicht aktivieren, besteht das Risiko eines endgültigen Verlusts von Browserdaten. Weitere Informationen zur Synchronisierung finden Sie unter [Microsoft Edge-Synchronisierung](microsoft-edge-enterprise-sync.md).

> [!CAUTION]
> Führen Sie ein Rollback nur bei tatsächlichem Bedarf durch, da es immer das Risiko von Datenverlusten birgt.

## Manuelles Aktivieren des Rollbacks mit einer MSI-Datei

Führen Sie die folgenden Schritte aus, um die Zurücksetzung mit einer MSI-Datei manuell durchzuführen.

1. Deaktivieren Sie Microsoft Edge-Updates.

   > [!NOTE]
   > Wir empfehlen, die aktuellsten administrativen Vorlagen zu installieren. Weitere Informationen finden Sie unter [Herunterladen und Installieren der administrativen Vorlage für Microsoft Edge](https://docs.microsoft.com/DeployEdge/configure-microsoft-edge#1-download-and-install-the-microsoft-edge-administrative-template).

   - Öffnen Sie den Editor für lokale Gruppenrichtlinien, und wechseln Sie zu *Computerkonfiguration > Administrative Vorlagen > Microsoft Edge Update > Anwendungen > Microsoft Edge>*.
   - Wählen Sie **Außerkraftsetzung von Updaterichtlinien** aus, und wählen Sie dann **Aktiviert** aus.
   - Wählen Sie unter **Optionen** aus der Richtlinien-Dropdownliste den Eintrag **Update deaktiviert** aus.

2. Laden Sie die MSI-Datei herunter.

   - Laden Sie [hier](https://www.microsoft.com/edge/business/download) die MSI-Datei für die Version herunter, zu der Sie zurückkehren möchten.
   - Speichern Sie die MSI-Datei auf Ihrem Desktop.

3. Führen Sie den Rollback-Befehl aus.

   - Öffnen Sie die Windows-Eingabeaufforderung mit **Als Administrator ausführen**.
   - Geben Sie den folgenden Befehl ein, wobei *C:\Users\username\Desktop\test*  der Pfad zu der heruntergeladenen MSI-Datei ist, und „FileName“ der Name der .msi-Datei:<br>
 `C:\Users\username\Desktop\test>msiexec /I FileName.msi /qn ALLOWDOWNGRADE=1`<br>
     > [!NOTE]
     > Weitere Informationen zu „msiexec“ finden Sie unter [msiexec](https://docs.microsoft.com/windows-server/administration/windows-commands/msiexec).
   - Schließen Sie Microsoft Edge, und öffnen Sie ihn erneut, um zu überprüfen, ob das Rollback erfolgreich war. Wechseln Sie unter **Einstellungen und mehr** (ALT + F) zu **Einstellungen**, und wählen Sie **Über Microsoft Edge** aus.

## Aktivieren des Rollbacks mit Microsoft Edge-Update- und Gruppenrichtlinien

Führen Sie die folgenden Schritte aus, um das Rollback über Microsoft Edge Update- und Gruppenrichtlinien zu aktivieren.

1. Öffnen Sie den Editor für lokale Gruppenrichtlinien, und wechseln Sie zu *Computerkonfiguration > Administrative Vorlagen > Microsoft Edge Update > Anwendungen > Microsoft Edge>*.
2. Wählen Sie **Zurücksetzen auf Zielversion** aus, und wählen Sie dann **Aktiviert**aus.
3. Wählen Sie **Zielversion außer Kraft setzen** und dann die Browserversion aus, auf die Microsoft Edge zurückgesetzt werden soll.
4. Wählen Sie **Außerkraftsetzung von Updaterichtlinien** aus, und wählen Sie dann **Aktiviert** aus. Wählen Sie unter **Optionen** in der Richtlinien-Dropdownliste eine der folgenden Optionen aus (mit Ausnahme von **Update deaktiviert**):

   - Updates immer zulassen
   - Nur automatische unbeaufsichtigte Updates

     > [!NOTE]
     > Um die Aktualisierung einer Gruppenrichtlinie zu erzwingen, geben Sie `gpupdate /force` in der Windows-Eingabeaufforderung mit Administratorrechten ("Als Administrator ausführen") ein.

5. Klicken Sie auf **OK**, um die Richtlinie zu speichern. Das Rollback erfolgt, wenn Microsoft Edge Update das nächste Mal nach einem Update sucht. Wenn Sie die Aktualisierung schneller ausgeführt werden soll, können Sie das Microsoft Edge Update-Abrufintervall ändern oder das Rollback mithilfe einer MSI-Datei aktivieren.

### Häufige Fehler bei der Zurücksetzung

Die folgenden Fehler verhindern ein Rollback:

- Eingabe ist eine nicht unterstützte Zielversion
- Eingabe ist eine nicht vorhandene Zielversion
- Eingabe ist falsch formatiert

### Empfohlene Gruppenrichtlinien

Die folgenden Gruppenrichtlinien und Einstellungen werden für die Durchführung des Rollbacks dringend empfohlen.

#### Gruppenrichtlinien für die Synchronisierung

- ForceSync. Legen Sie ForceSync auf „Aktiviert“ fest. Durch diese Richtlinie wird die Aktivierung der Synchronisierung für alle Azure Active Directory (Azure AD)-Benutzer erzwungen. Diese Richtlinie gilt nur für Microsoft Edge-Versionen 86 und höher.
- Über *Liste der Typen konfigurieren, die von der Synchronisierungsrichtlinie ausgeschlossen werden* können Administratoren steuern, welche Daten von Benutzern synchronisiert werden sollen.

#### Gruppenrichtlinien für Browser-Neustart

Es empfiehlt sich, nach dem Aktivieren des Rollbacks einen Neustart für die Benutzer zu erzwingen.

- Aktivieren Sie *Einen Benutzer informieren, dass für ausstehende Updates ein Browser-Neustart empfohlen oder erforderlich ist*. Wählen Sie unter „Optionen“ **Erforderlich** aus.
- Aktivieren Sie *Zeitraum für Updatebenachrichtigungen festlegen*, und legen Sie dann die gewünschte Zeit in Millisekunden fest.

## Momentaufnahme

Eine Momentaufnahme ist eine mit Versionsstempel versehene Kopie des Benutzerdatenordners. Während eines Versionsupgrades wird eine Momentaufnahme der vorherigen Version erstellt und im Momentaufnahme-Ordner gespeichert. Nach dem Rollback wird eine versionsgleiche Momentaufnahme in den neuen Benutzerdatenordner kopiert und aus dem Momentaufnahme-Ordner gelöscht. Wenn nach dem Downgrade keine versionsgleiche Momentaufnahme verfügbar ist, stützt sich das Rollback auf die Synchronisierung, um die Benutzerdaten in die neue Microsoft Edge-Version einzufügen.

Mit der [UserDataSnapshotRetentionLimit](https://docs.microsoft.com/deployedge/microsoft-edge-policies#userdatasnapshotretentionlimit)-Gruppenrichtlinie können Sie einen Grenzwert für die Anzahl der Snapshots festlegen, die zu einem bestimmten Zeitpunkt aufbewahrt werden können. Standardmäßig werden drei Momentaufnahmen aufbewahrt. Sie können diese Richtlinie so konfigurieren, dass 0-5 Momentaufnahmen aufbewahrt werden.

## Häufig gestellte Fragen

### Manuelles MSI-Rollback

#### Welche allgemeinen MSI-Fehler können auftreten?

1. Wenn die Gruppenrichtlinie zum Installieren von Updates deaktiviert ist, wird das Rollback nicht ausgeführt.

   - Stellen Sie für die Ausführung des Rollbacks sicher, dass die Installationsrichtlinie **aktiviert** ist. Wenn diese Richtlinie deaktiviert ist, wird verhindert, dass Microsoft Edge-Kanäle installiert werden. Weitere Informationen finden Sie unter [Installation](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#install).

2. Wenn keine Enlightenment-Updates vorhanden sind, werden Microsoft Edge-Installationen blockiert, es sei denn, *Microsoft Edge Seite-an-Seite-Browserumgebung zulassen* ist aktiviert.

   - Für Windows-Versionen 1903 und 1909: Wenn Ihre letzte Aktualisierung vor Oktober 2019 war, tritt möglicherweise dieses Problem auf.
   - Für Windows-Versionen 1709, 1803 und 1809: Wenn Ihre letzte Aktualisierung vor November 2019 war, tritt möglicherweise dieses Problem auf.<br>
Weitere Informationen finden Sie unter [Windows-Updates zur Unterstützung der nächsten Version von Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-sysupdate-windows-updates).

#### Die folgende Fehlermeldung wurde angezeigt, nachdem Sie die Eingabeaufforderung verwendet haben und das Rollback nicht ausgeführt wurde. Was ist los?

![Rollback-Statusmeldung](./media/edge-learnmore-rollback/edge-rollback-cmd-flag-error.png)

*ALLOWDOWNGRADE=1* wurde nicht ausgeführt.

### Rollback von Microsoft Edge Update und Gruppenrichtlinien

#### Ich habe *Zurücksetzen auf Zielversion* festgelegt, *Außerkraftsetzung von Updaterichtlinien* aktiviert und die gewünschte Browserversion für *Zielversion außer Kraft setzen* angegeben, aber die Browserversion war nicht die erwartete. Was ist los?

Einige häufige Fehler, durch die das Rollback verhindert wird, sind:

- Wenn die Option zum Zurücksetzen auf Zielversion nicht festgelegt ist, wird das Rollback nicht ausgeführt.
- Bei der Einstellung für die Außerkraftsetzung der Zielversion liegt eines der folgenden Probleme vor:

  - Die Außerkraftsetzung der Zielversion ist auf eine nicht unterstützte Zielversion festgelegt.
  - Die Außerkraftsetzung der Zielversion ist auf eine nicht vorhandene Zielversion festgelegt.
  - Die Eingabe für die Außerkraftsetzung der Zielversion ist falsch formatiert.

- Wenn die Außerkraftsetzung von Updaterichtlinien auf "Updates deaktiviert" festgelegt ist, akzeptiert Microsoft Edge Update keine Updates, und es wird kein Rollback ausgeführt.

### Ich habe alle Gruppenrichtlinien ordnungsgemäß festgelegt, aber das Rollback wird nicht ausgeführt. Was ist passiert?

Microsoft Edge Update hat noch keine Suche nach Updates durchgeführt. Die automatische Updatefunktion sucht standardmäßig alle 10 Stunden nach Updates. Sie können dieses Problem beheben, indem Sie das Abrufintervall für Microsoft Edge Update mithilfe der Gruppenrichtlinie für die Überschreibung des Überprüfungszeitraums für automatische Updates ändern. Weitere Informationen hierzu finden Sie unter [AutoUpdateCheckPeriodMinutes-Richtlinie](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#autoupdatecheckperiodminutes).

### Als IT-Administrator habe ich alle Schritte für eine ordnungsgemäße Zurücksetzung befolgt. Das Rollback wurde nur für einen Teil meiner Benutzergruppe durchgeführt. Warum wurde es nicht auch für die anderen durchgeführt?

Die Gruppenrichtlinieneinstellung wurde noch nicht mit allen Clients synchronisiert. Wenn Administratoren eine Gruppenrichtlinie festlegen, werden die entsprechenden Einstellungen nicht sofort von den Clients empfangen. Sie können [ein Remoteupdate von Gruppenrichtlinien erzwingen](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-server-2012-r2-and-2012/jj134201(v=ws.11)).

## Weitere Informationen

- [Angebotsseite für Microsoft Edge für Unternehmen](https://aka.ms/EdgeEnterprise)
