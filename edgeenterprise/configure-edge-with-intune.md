---
title: Konfigurieren der Microsoft Edge-Richtlinieneinstellungen für Windows mit Microsoft Intune
ms.author: kvice
author: kelleyvice-msft
manager: laurawi
ms.date: 06/18/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Konfigurieren Sie die Microsoft Edge-Richtlinieneinstellungen für Windows mit Microsoft Intune.
ms.openlocfilehash: 0189a3fc2f9dc115563e7cf6dca1df960680bf22
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/24/2021
ms.locfileid: "11447559"
---
# <a name="configure-microsoft-edge-policy-settings-with-microsoft-intune"></a>Konfigurieren der Microsoft Edge-Richtlinieneinstellungen mit Microsoft Intune

In diesem Artikel wird erläutert, wie Sie Microsoft Edge Richtlinieneinstellungen für Windows10 mit Microsoft Intune konfigurieren.

> [!NOTE]
> Dieser Artikel bezieht sich auf Microsoft Edge Version 77 oder höher.

Sie können Microsoft Edge-Richtlinien und -Einstellungen durch Hinzufügen eines Gerätekonfigurationsprofils in Microsoft Intune konfigurieren. Die Verwendung von Intune zum Verwalten und Erzwingen von Richtlinien entspricht der Verwendung von Active Directory-Gruppenrichtlinien oder der Konfiguration lokaler Gruppenrichtlinienobjekteinstellungen auf Benutzergeräten.

Weitere Informationen zum Verwalten von Microsoft Edge-Richtlinien mit Microsoft Intune finden Sie unter [Verwalten des Webzugriffs mithilfe von Microsoft Edge mit Microsoft Intune](/intune/manage-microsoft-edge). Beachten Sie jedoch, dass der verknüpfte Artikel für Microsoft Edge Version 45 und früher spezifisch ist und daher möglicherweise Informationen und Verweise enthält, die nicht für Microsoft Edge Enterprise Version 77 und höher gelten.

> [!TIP]
> Informationen zum Konfigurieren von Microsoft Edge auf macOS mithilfe von Microsoft Intune finden Sie unter [Konfigurieren für macOS](configure-microsoft-edge-on-mac.md).

## <a name="create-a-profile-to-manage-settings-in-microsoft-edge-for-windows-10"></a>Erstellen eines Profils zum Verwalten von Einstellungen in Microsoft Edge für Windows10

Mithilfe von administrativen Vorlagen in Microsoft Intune können Sie Microsoft Edge-Gruppenrichtlinien auf Ihren Windows10-Geräten mithilfe der Cloud verwalten. Dieser Abschnitt unterstützt Sie beim Erstellen einer Vorlage zum Konfigurieren von Microsoft Edge-spezifischen Anwendungseinstellungen. Wenn Sie die Vorlage erstellen, wird ein Gerätekonfigurationsprofil erstellt. Sie können dieses Profil dann Windows10-Geräten in Ihrer Organisation zuweisen oder auf diesen bereitstellen.

### <a name="prerequisites"></a>Voraussetzungen

- Windows 10, mit den folgenden Mindestvoraussetzungen:
  - Windows10, Version 1909
  - Windows10, Version 1903, mit Installation von [KB4512941](https://support.microsoft.com/kb/4512941)
  - Windows10, Version 1809, mit Installation von [KB4512534](https://support.microsoft.com/kb/4512534)
  - Windows10, Version 1803, mit Installation von [KB4512509](https://support.microsoft.com/kb/4512509)
  - Windows10, Version 1709, mit Installation von [KB4516071](https://support.microsoft.com/kb/4516071)

### <a name="use-administrative-templates-to-create-a-policy-for-microsoft-edge"></a>Verwenden von Administrativen Vorlagen zur Erstellung einer Richtlinie für Microsoft Edge

Dieses Verfahren nutzt administrative Vorlagen (die Sie möglicherweise aus der Gruppenrichtlinie kennen), die in Intune integriert sind. Sie können diese Vorlagen zur Erstellung einer Richtlinie für Microsoft Edge verwenden, indem Sie Einstellungen aus einer vorkonfigurierten Liste auswählen.

1. Melden Sie sich beim [Microsoft Endpoint Manager](https://endpoint.microsoft.com/)-Portal an.
2. Wählen Sie im linken Navigationsbereich **Geräte** aus.
3. Wählen Sie nach**Geräte** | **Übersicht** aus, und gehen Sie dann auf **Konfigurationsprofile** (unter der Überschrift Richtlinien) aus.
4. Wählen Sie in der oberen Befehlsleiste **Profil erstellen** aus.
5. Wählen Sie in der Dropdownliste unterhalb **Plattform****Windows 10 und höher**aus.
6. Wählen Sie in der Dropdownliste unterhalb **Profil****Administrative Vorlagen** aus, und klicken Sie dann auf die Schaltfläche **Erstellen**. Der nächste Screenshot zeigt die Dropdownlisten, in denen Plattform und Art des Profil ausgewählt werden können.

    ![Wählen Sie die Plattform und Art des Profils aus](./media/configure-edge-with-intune/create-profile-platform.png)

7. Geben Sie auf der Registerkarte **Grundlagen** einen**Namen** zur Beschreibung ein, z. b. die Microsoft-Edge-Richtlinie. Ooptional können Sie eine  **Beschreibung** der Richtlinie eingeben.
Der nächste Screenshot zeigt das Format für die Registerkarte **Grundlagen** an. Die Menüleiste zeigt die nächsten Schritte (als abgeblendete Registerkarten) zur Erstellung des Profils an.

   ![Geben Sie einen Namen und eine Beschreibung ein](./media/configure-edge-with-intune/create-profile-basics-tab.png)

8. Wählen Sie **Weiter** aus.
9. Wählen Sie auf der Registerkarte **Konfigurationseinstellungen** den Ordner Microsoft Edge an einen der folgenden Speicherorte aus:

   - unter dem Ordner Computerkonfiguration
   - unter dem Ordner Benutzerkonfiguration.

   Die verfügbaren Einstellungen für Microsoft Edge werden im rechten Bereich angezeigt. Beispielsweise *Computerkonfiguration/Microsoft Edge/Downloadbeschränkungen zulassen*, welche im folgenden Screenshot gezeigt werden.

   ![Registerkarte Konfigurationseinstellungen](./media/configure-edge-with-intune/create-profile-configuration-settings-tab.png)

   > [!NOTE]
   > Die vollständigste und aktuellste Liste aller verfügbaren Einstellungen für Microsoft Edge finden Sie unter [Microsoft Edge – Richtlinien](./microsoft-edge-policies.md) und [Microsoft Edge – Updaterichtlinien](./microsoft-edge-update-policies.md).

10. Verwenden Sie das Suchfeld („Filtern von Elementen...“), um eine bestimmte Einstellung zu finden, die Sie konfigurieren möchten. In diesem Beispiel lautet der Suchtext „Homepage“. Der nächste Screenshot zeigt die Suchergebnisse an.

    ![Suchergebnisse](./media/configure-edge-with-intune/create-profile-configuration-settings-tab-search.png)

11. Nachdem Sie die Einstellung gefunden haben, die Sie konfigurieren möchten, wählen Sie diese aus, und lassen Sie sich so die konfigurierbaren Werte anzeigen. Im nächsten Screenshot wird als Beispiel „Startseiten-URL konfigurieren“ ausgewählt.

    ![Konfigurieren der Richtlinie zur Startseiten-URL](./media/configure-edge-with-intune/create-profile-configuration-settings-tab-edit-pol.png)

12. Aktivieren Sie die Richtlinie, und geben Sie einen Wert für die Startseiten-URL ein, wie im vorherigen Screenshot gezeigt.

13. Klicken Sie auf **OK**. Die Spalte „Status“ muss in den Einstellungen als „Aktiviert“ angezeigt werden, wie im folgenden Screenshot dargestellt.

    ![Die Einstellung „Status“ ist aktiviert](./media/configure-edge-with-intune/create-profile-configuration-settings-tab-set-enabled.png)

14. Klicken Sie auf die Schaltfläche **Weiter**.

15. Fügen Sie auf der Registerkarte **Bereichsmarkierung** falls gewünscht eine Bereichsmarkierung hinzu. Andernfalls klicken Sie auf die Schaltfläche **Nächste**.

16. Klicken Sie auf der Registerkarte **Zuweisungen** auf **+ wählen Sie Gruppen aus, die einbezogen werden sollen**, um diese Richtlinie der Azure Active Directory-Gruppe (Azure Active Directory) zuzuweisen, welche die Geräte oder die Benutzer enthält, für die Sie diese Richtlinieneinstellung erhalten möchten. Unter [Zuweisen von Benutzer- und Geräteprofilen in Microsoft Intune](/intune/device-profile-assign) finden Sie Informationen dazu, wie Sie das Profil Ihren Benutzer- oder Gerätegruppen in Azure AD zuweisen.

    ![Wählen Sie die Gruppen, die einbezogen werden sollen](./media/configure-edge-with-intune/create-profile-assignments-tab.png)

17. Klicken Sie auf die Schaltfläche **Weiter**.

18. Überprüfen Sie auf der Registerkarte **Überprüfen + erstellen** die Zusammenfassung Ihrer Änderungen, um sicherzustellen, dass sie korrekt sind, und klicken Sie dann auf die Schaltfläche **Erstellen**.

19. Die neu erstellte Richtlinie (Microsoft Edge-Richtlinie) wird im folgenden Screenshot gezeigt.

    ![Wählen Sie die Gruppen, die einbezogen werden sollen](./media/configure-edge-with-intune/create-profile-new-policy-finished.png)

Weitere Informationen zu Windows10-Profilen finden Sie unter [Verwenden von Windows10-Vorlagen zum Konfigurieren von Gruppenrichtlinieneinstellungen in Microsoft Intune](/intune/administrative-templates-windows).

## <a name="see-also"></a>Weitere Informationen:

- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)
- [Verwalten von Webzugriffen mithilfe von Microsoft Edge mit Microsoft Intune](/intune/manage-microsoft-edge)
- [Verwenden Sie Windows10-Vorlagen zum Konfigurieren von Gruppenrichtlinieneinstellungen in Microsoft Intune](/intune/administrative-templates-windows)
- [Bereitstellen von Microsoft Edge mit Microsoft Intune](/intune/apps/apps-windows-edge/?bc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2ftoc.json)