---
title: Microsoft Edge in Ihrer Umgebung
ms.author: ryhecht
author: RyanHechtMSFT
manager: tinad
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Microsoft Edge in Ihrer Umgebung
ms.openlocfilehash: 2381380cb399f6a1fbb5efa9378ffeba20fa774f
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "11641601"
---
# <a name="microsoft-edge-in-your-environment"></a>Microsoft Edge in Ihrer Umgebung

In diesem Artikel wird beschrieben, wie Sie die Bereitstellung von Microsoft Edge vorbereiten, wenn die Vorgängerversion von Microsoft Edge das Serviceende erreicht.

Wie im [Blogbeitrag](https://aka.ms/EdgeLegacyEOS) des Microsoft Edge-Produktteams angegeben, endet der Support für die Desktopanwendung der Vorgängerversion von Microsoft Edge am 9. März 2021. Wenn Sie die Version „Update Tuesday“ (oder „B“) im April installieren, wird die Vorgängerversion von Microsoft Edge von Geräten mit Windows 10 RS4 bis 20H1 entfernt und durch Microsoft Edge ersetzt.

## <a name="how-to-prepare"></a>Vorbereitungen

Zur Vorbereitung auf die Installation von Microsoft Edge auf Windows 10 RS4- bis 20H1-Geräten mit dem Update Tuesday-Release im April empfehlen wir, den Artikel [Planen der Bereitstellung von Microsoft Edge](deploy-edge-plan-deployment.md) zu lesen.

Nachdem Sie die Bereitstellung geplant haben, verwenden Sie einen der folgenden Ansätze, um die Bereitstellung von Microsoft Edge vorzubereiten.

- **Installieren Sie Gruppenrichtlinien, um Ihren Microsoft Edge-Aktualisierungsansatz anzupassen**. Weitere Informationen finden Sie unter [Konfigurieren von Microsoft Edge-Richtlinieneinstellungen unter Windows](configure-microsoft-edge.md). Achten Sie dabei besonders auf das [Referenzmaterial zu Updaterichtlinien](microsoft-edge-update-policies.md). Wenn Sie Gruppenrichtlinien installieren, um Ihre Updates zu verwalten, bevor Sie das Update Tuesday-Release vom April installieren, beginnt Microsoft Edge sofort damit, Ihre Richtlinie anzuwenden. Wenn keine Gruppenrichtlinie installiert ist, wird Microsoft Edge automatisch aktualisiert.

- **Entfernen Sie die Desktopanwendung der Vorgängerversion von Microsoft Edge vor dem Serviceende am 9. März 2021, und stellen Sie Microsoft Edge bereit**. Für Windows 10 RS4 bis 20H1 können Sie dies mithilfe von Windows Updates tun. Weitere Informationen finden Sie unter [Bereitstellen von Microsoft Edge mit Windows 10-Updates](deploy-edge-with-windows-10-updates.md).

## <a name="see-also"></a>Weitere Informationen

- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)
- [Planen Ihrer Bereitstellung von Microsoft Edge](deploy-edge-plan-deployment.md)