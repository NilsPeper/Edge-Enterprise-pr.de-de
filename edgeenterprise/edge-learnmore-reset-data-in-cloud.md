---
title: Zurücksetzen von Microsoft Edge-Daten
ms.author: collw
author: dan-wesley
manager: silvanam
ms.date: 07/09/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Wie werden Microsoft Edge-Daten in der Cloud zurückgesetzt
ms.openlocfilehash: 7b1b54bd3e59190d6ff3bdfeb71b8f97080538c224b7dbddb73b9d11708706ac
ms.sourcegitcommit: d44c0997ffe40d67421312ed96e7766da947eaa0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "11725988"
---
# <a name="reset-microsoft-edge-data-in-the-cloud"></a>Zurücksetzen von Microsoft Edge-Daten in der Cloud

Dieser Artikel beschreibt die Schritte zum Zurücksetzen Ihrer Microsoft Edge-Daten in der Cloud.

> [!NOTE]
> Dieser Artikel bezieht sich auf Microsoft Edge Version 88 oder höher, sofern nichts anderes angegeben ist.

> [!NOTE]
> Wenn sich Ihr Mandant in einer GCC Mod-Umgebung befindet, muss Ihr Mandantenadministrator eine Supportanfrage bei Microsoft zum Zurücksetzen Ihrer Daten einreichen.

## <a name="overview"></a>Übersicht

Es gibt Situationen, in denen Sie Ihre Microsoft Edge-Daten in der Cloud zurücksetzen möchten. Sie möchten beispielsweise Ihre Daten synchronisieren, doch Microsoft Edge meldet, dass die Daten nicht synchronisiert werden können. Oder Sie möchten sicherstellen, dass Ihre Daten aus der Microsoft-Cloud entfernt werden. In beiden Fällen können Sie mit Microsoft Edge eine Clouddaten-Zurücksetzung durchführen.

## <a name="back-up-your-favorites"></a>Sichern Ihrer Favoriten

Bevor Sie eine Zurücksetzung durchführen, empfehlen wir, dass Sie Ihre Favoriten sichern. Führen Sie die folgenden Schritte aus, um Ihre Favoriten zu sichern.

1. Drücken Sie in Microsoft Edge STRG+UMSCHALT+O > wählen Sie die drei Punkte aus > klicken Sie auf **Favoriten exportieren**.
2. Wählen Sie die Datei aus, in der Sie Ihre Favoriten speichern möchten. Sie können Ihren eigenen Dateinamen eingeben oder Sie können „Favoriten_Tag_Monat_Jahr.html“ verwenden, den Microsoft Edge standardmäßig als Dateinamen vorschlägt. Beispiel: „Favoriten_07_05_21.html“. Wenn Sie Ihre Favoriten später wiederherstellen müssen, können Sie dies von dieser Datei tun.
3. Klicken Sie auf **Speichern**.

## <a name="perform-a-reset-to-fix-a-synchronization-problem"></a>Durchführen eines Zurücksetzens, um ein Synchronisierungsproblem zu beheben

Wenn Microsoft Edge meldet, dass Ihre Daten nicht synchronisiert werden können und das Zurücksetzen der Daten vorschlägt, führen Sie eine Zurücksetzung durch, um das Problem zu beheben.

Führen Sie die folgenden Schritte für eine Zurücksetzung durch.

1. Stellen Sie zunächst sicher, dass Sie von Microsoft Edge auf allen ihren Geräten, einschließlich Ihrer mobilen Geräte, abgemeldet sind, mit Ausnahme des Geräts, auf dem Sie die Zurücksetzung durchführen. Wenn Sie sich bei Microsoft Edge abmelden möchten, wählen Sie **Einstellungen > Profile > Abmelden** aus. Wenn Sie sich abmelden, wählen Sie nicht die Option zum Löschen von Favoriten, Einstellungen usw. auf dem lokalen Gerät aus.
2. Nachdem Sie sich bei allen anderen Geräten abgemeldet haben, öffnen Sie Microsoft Edge auf Ihrem Desktop. Wählen Sie **Einstellungen > Profile > Synchronisierung zurücksetzen** aus. Wählen Sie im angezeigten Dialogfeld die Option zum Fortsetzen der Synchronisierung nach dem Zurücksetzen von Daten und dann **Jetzt zurücksetzen** aus.

## <a name="perform-a-reset-to-remove-your-data-from-microsofts-cloud"></a>Zurücksetzung durchführen, um Ihrer Daten aus der Microsoft-Cloud zu entfernen

Wenn Sie Ihre Daten aus der Microsoft-Cloud entfernen möchten, führen Sie die folgenden Schritte aus, um eine Zurücksetzung durchzuführen.

1. Beenden Sie die Synchronisierung auf Geräten mit Ausnahme des Geräts, auf dem Sie die Zurücksetzung durchführen wollen.  Wählen Sie in Microsoft Edge **Einstellungen > Profile > Synchronisierung deaktivieren** aus.  
2. Nachdem Sie die Synchronisierung beendet haben, wählen Sie **Einstellungen > Profile > Synchronisierung zurücksetzen** aus. Wählen Sie im angezeigten Dialogfeld **nicht** die Option zum Fortsetzen der Synchronisierung auf diesem Gerät nach dem Zurücksetzen der Synchronisierung aus. Wählen Sie **Zurücksetzen** aus.

## <a name="what-to-expect-during-and-after-a-data-reset"></a>Was während und nach einer Datenzurücksetzung zu erwarten ist

Eine Datenzurücksetzung kann zwischen wenigen Sekunden und einigen Minuten dauern, je nachdem, wie viele Daten Sie in der Microsoft-Cloud gespeichert haben. In einigen Fällen wird möglicherweise eine Meldung angezeigt, die besagt, dass eine Zurücksetzung nicht abgeschlossen werden konnte, und ein Vorschlag, erneut zurückzusetzen. Warten Sie in diesem Fall einige Stunden, und versuchen Sie dann, die Daten erneut zurückzusetzen. Wenn Sie Ihre Daten weiterhin nicht zurücksetzen können, wenden Sie sich an den Microsoft Edge-Support.

Nachdem eine Datenzurücksetzung erfolgreich abgeschlossen wurde, werden die Daten erneut von Ihrem Gerät synchronisiert, wenn Sie die Option „Fortsetzen der Synchronisierung nach dem Zurücksetzen von Daten“ ausgewählt haben. Sie müssen sich ebenfalls auf Ihren anderen Geräten anmelden, wenn Sie von diesen Geräten synchronisieren möchten. Wenn Sie die Synchronisierung jedoch nicht fortsetzen möchten, werden Ihre Microsoft Edge-Daten aus der Cloud entfernt, und die Daten werden nicht weiter synchronisiert.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft Edge Enterprise-Startseite](https://aka.ms/EdgeEnterprise)
- [Microsoft Edge Enterprise-Synchronisierung](microsoft-edge-enterprise-sync.md)
