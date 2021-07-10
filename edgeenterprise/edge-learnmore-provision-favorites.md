---
title: Bereitstellen von Favoriten für Microsoft Edge
ms.author: capoon
author: dan-wesley
manager: abutcher
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Bereitstellen von Favoriten für Microsoft Edge
ms.openlocfilehash: 2d75e9c22a8aa9cc70d8b96c280934137396620a
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "11642181"
---
# <a name="provision-favorites-for-microsoft-edge"></a>Bereitstellen von Favoriten für Microsoft Edge

Angeregt durch Kundenfeedback haben wir Verbesserungen vorgenommen, um die Bereitstellung von Favoriten zu erleichtern. Ab Microsoft Edge, Version 85 müssen Administratoren keine Dateien mehr manuell erstellen, um Favoriten bereitzustellen. Administratoren können zum Hinzufügen von Favoriten und Ordnern die Microsoft Edge-Benutzeroberfläche verwenden, um eine Datei zu generieren, die in eine Gruppenrichtlinie exportiert werden kann.

In diesem Artikel wird beschrieben, wie Sie Favoriten und Ordner für Ihre Organisation bereitstellen. Sie können die Richtlinie zum [Konfigurieren von Favoriten](//DeployEdge/microsoft-edge-policies#configure-favorites) verwenden, um Favoriten und Ordner bereitzustellen.

> [!NOTE]
> Dieser Artikel bezieht sich auf Microsoft Edge Version 85 oder neuer.

## <a name="prerequisites-and-recommendations"></a>Voraussetzungen und Empfehlungen

- Microsoft Edge, Version 85 mit installierter entsprechender administrativer Vorlage für Gruppenrichtlinien.
- Wir empfehlen, zum Bereitstellen dieser Favoriten ein neues Profil in Microsoft Edge zu verwenden. Alle Favoriten, die über dieses Profil gespeichert werden, werden in den Export einbezogen.  

## <a name="provision-favorites-and-folders"></a>Bereitstellen von Favoriten und Ordnern

Führen Sie die folgenden Schritte aus, um Ihren Benutzern Favoriten und Ordner bereitzustellen.

1. Geben Sie in die Microsoft Edge-Adressleiste folgende URL ein: *edge://flags/#edge-favorites-admin-export*.
2. Wählen Sie unter **Export von Favoritenkonfigurationen für Administratoren** aus der Dropdownliste die Option **Aktiviert** aus, und klicken Sie dann auf **Neustart**.

3. Wechseln Sie zur Seite **Favoriten** unter *edge://favorites*, um die gewünschten Favoriten und Ordner hinzuzufügen.

<!--
4. On the **Favorites bar**, click **Add folder**. The folder structure of favorites that are set in the profile you're using will be reflected in the folder you provision for your users. The next screenshot shows "Managed favorites", the folder we'll use to provision favorites.

   ![Add a folder](media/edge-learnmore-provision-favorites/provision-favorites-add-folder.png)

   > [!TIP]
   > Add existing folders that contain favorites you want to provision for your users.

5. Select "Managed favorites" and then click **Add favorite**. The next screenshot shows the favorite we've added.

   ![Add a favorite](media/edge-learnmore-provision-favorites/provision-favorites-add-favorite.png)-->

4. Wenn Sie die Favoriten und Ordner hinzugefügt haben, exportieren Sie sie, damit sie von der Richtlinie zum **Konfigurieren von Favoriten** verwendet werden können. Wechseln Sie über die Adressleiste zu *edge://favorites*, klicken Sie auf die Auslassungspunkte "**...**", und wählen Sie **Favoritenkonfiguration exportieren** aus. Der nächste Screenshot zeigt die Optionen, die Sie beim Bereitstellen von Favoriten haben.

   ![Menüoptionen für die Arbeit mit Favoriten.](media/edge-learnmore-provision-favorites/provision-favorites-menu-options.png)

5. Unter **Favoritenkonfiguration exportieren** ist der Ordner zu benennen, den die Benutzer sehen werden. Geben Sie den Ordnernamen ein, und wählen Sie das gewünschte Plattformformat aus. Klicken Sie auf **In Zwischenablage kopieren**. Im nächsten Screenshot sind "Verwaltete Favoriten" als Ordnernamen und Windows als Plattform zu sehen.

   ![Dialogfeld zum Exportieren von Favoriten in einen Windows-Ordner.](media/edge-learnmore-provision-favorites/provision-favorites-export.png)

6. Öffnen Sie den Gruppenrichtlinien-Editor, navigieren Sie zu *Computerkonfiguration/Administrative Vorlagen/*, und wählen Sie **Favoriten konfigurieren** aus. Aktivieren Sie die Richtlinie "Favoriten konfigurieren". Fügen Sie unter **Optionen:** die exportierten Inhalte in den Textbereich in "Favoriten konfigurieren" ein, und klicken Sie dann auf **Übernehmen**. Der nächste Screenshot zeigt ein Beispiel für den Ordner "Verwaltete Favoriten" aus Schritt 5.

   ![Verwenden Sie "gpedit" zum Aktivieren und Konfigurieren der Richtlinie "Favoriten konfigurieren".](media/edge-learnmore-provision-favorites/provision-favorites-gpedit.png)

7. Klicken Sie auf **OK** oder **Übernehmen**, um die Richtlinieneinstellungen zu speichern.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)