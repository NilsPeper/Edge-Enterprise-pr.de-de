---
title: Automatisieren von Microsoft Edge für die macOS-Bereitstellung mit Jamf
ms.author: kvice
author: dan-wesley
manager: laurawi
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: So automatisieren Sie Microsoft Edge für die macOS-Bereitstellung mit Jamf.
ms.openlocfilehash: 9c8fc0af734d4784ac122602b685bc561aabf340
ms.sourcegitcommit: 8968f3107291935ed9adc84bba348d5f187eadae
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/12/2021
ms.locfileid: "11979160"
---
# <a name="deploy-to-macos-with-jamf"></a>Bereitstellen unter macOS mit JAMF

In diesem Artikel wird beschrieben, wie Microsoft Edge für macOS mithilfe von Jamf bereitgestellt wird.

> [!NOTE]
> Dieser Artikel bezieht sich auf Microsoft Edge Version 77 oder höher.

## <a name="prerequisites"></a>Voraussetzungen

Stellen Sie vor der Bereitstellung von Microsoft Edge sicher, dass die folgenden Voraussetzungen erfüllt sind:

- Die Microsoft Edge-Installationsdatei **MicrosoftEdgeDev-\<version\>.pkg** befindet sich an einem zugänglichen Speicherort in Ihrem Netzwerk. Sie können die Installationsdateien für Microsoft Edge Enterprise von der [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise) herunterladen.
- Sie verfügen über ein JAMF-Cloud-Konto mit der Zugriffsebene und den erforderlichen Berechtigungen zum Erstellen und Bereitstellen von Installationsdateien auf Computern.

## <a name="to-deploy-microsoft-edge-using-jamf"></a>So stellen Sie Microsoft Edge mithilfe von Jamf bereit:

1. Melden Sie sich bei Jamf an und wechseln Sie zu **Alle Einstellungen**.

    ![Alle Einstellungen öffnen](./media/mac-deploy/jamf-dash-main-open-settings.png)

2. Klicken Sie unter **Alle Einstellungen** auf **Computerverwaltung**.

    ![Computerverwaltung auswählen](./media/mac-deploy/jamf-all-settings-computer-mgmt.png)

3. Klicken Sie unter **Computerverwaltung** auf **Pakete**.

    ![Pakete auswählen](./media/mac-deploy/jamf-all-settings-computer-mgmt-pkgs.png)

4. Klicken Sie auf der Seite **Pakete** auf **+ Neu**, um ein neues Paket hinzuzufügen.

    ![„Neu” auswählen, um ein neues Paket hinzufügen](./media/mac-deploy/jamf-all-settings-computer-mgmt-new-pkg.png)

5. Geben Sie auf der Seite **Neues Paket** die Details zum Paket ein und klicken Sie dann auf **Speichern**. (Z. B. ANZEIGENAME, INFO oder NOTIZEN.)

    ![„Speichern” auswählen, um die Paketinformationen zu speichern](./media/mac-deploy/jamf-all-settings-computer-mgmt-save-pkg-info.png)

6. Wählen Sie in der Menüleiste **Computer** aus, und wählen Sie dann in der Navigationsleiste **Richtlinien** aus.

7. Wählen Sie **+ Neu** aus, um den Bereich **Neue Richtlinie** anzuzeigen.

    ![„Neu” auswählen, um eine neue Richtlinie zu erstellen](./media/mac-deploy/jamf-all-settings-computer-new-policy.png)

8. Wählen Sie auf der Registerkarte **Optionen** **Allgemein** aus.

    - Geben Sie unter **ANZEIGENAME** den Anzeigenamen für die Richtlinie ein.
    - Wählen Sie unter **Auslöser** das Ereignis aus, mit dem die Richtlinie ausgelöst wird. (Im Folgenden Beispiel ist das Ereignis das Starten.)

    ![Informationen zur Bereitstellung eingeben](./media/mac-deploy/jamf-all-settings-computer-cfg-policy.png)

9. Klicken Sie auf der Registerkarte **Optionen** auf **Pakete**.

10. Klicken Sie im Popup **Pakete konfigurieren** auf **Konfigurieren**.

    ![Paket konfigurieren](./media/mac-deploy/jamf-all-settings-computer-policy-pkg-configure.png)

11. Das Paket, das Sie hinzugefügt haben, wird im Bereich **Pakete** angezeigt. Klicken Sie auf **Hinzufügen**. In diesem Beispiel lautet der Name des Pakets im folgenden Screenshot „MicrosoftEdgeBeta”.

    ![Paket hinzufügen](./media/mac-deploy/jamf-all-settings-computer-policy-pkg-add-beta.png)

12. Verwenden Sie auf der Seite **Neue Richtlinie** die Dropdown-Listen, um den **VERTEILUNGSPUNKT** und die **AKTION** für die Richtlinie auszuwählen. Klicken Sie auf **Speichern**. Im folgenden Screenshot wird als Beispiel „Der Standardverteilungspunkt für jeden Computer” und „Installieren” verwendet.

    ![Verteilungspunkt und Aktion auswählen](./media/mac-deploy/jamf-all-settings-computer-mgmt-pkg-cfg-distro.png)

13. Wählen Sie auf der Seite **Neue Richtlinie** die Registerkarte **Bereich** aus. Sie können den Umfang der Bereitstellung auf der Grundlage von Computern oder Benutzern verwalten. Wählen Sie in diesem Beispiel **Alle Computer** in der Dropdown-Liste **ZIELCOMPUTER** aus, und klicken Sie dann auf **Speichern**.

    ![Den Bereich der Bereitstellung auswählen](./media/mac-deploy/jamf-all-settings-computer-mgmt-add-target.png)

14. An dieser Stelle können Sie die Microsoft Edge-Bereitstellungsrichtlinie überprüfen. Wenn die Bereitstellungsoptionen Ihren Anforderungen entsprechen, klicken Sie auf **Fertig**.

    ![Klicken Sie auf Fertig.](./media/mac-deploy/jamf-all-settings-computer-mgmt-finish-add-deployment.png)

    > [!NOTE]
    > Sie können jederzeit zu einer Bereitstellungsrichtlinie wechseln, um die Einstellungen zu ändern.

Herzlichen Glückwunsch! Sie haben soeben die Konfiguration von Jamf für die Bereitstellung von Microsoft Edge für macOS abgeschlossen. Wenn die von Ihnen definierte auslösende Bedingung „true” ist, wird das Paket auf den von Ihnen angegebenen Computern bereitgestellt.

## <a name="see-also"></a>Weitere Informationen:

- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)
- [Jamf.com](https://www.jamf.com/)
- [Jamf in Microsoft Intune integrieren](/intune/conditional-access-integrate-jamf)