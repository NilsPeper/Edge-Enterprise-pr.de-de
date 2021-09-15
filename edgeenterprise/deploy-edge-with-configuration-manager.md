---
title: Bereitstellen von Microsoft Edge mithilfe vom System Center Konfigurations-Manager
ms.author: kvice
author: kelleyvice-msft
manager: laurawi
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Erfahren Sie hier, wie Sie Microsoft Edge mithilfe vom System Center Konfigurations-Manager (SCCM) bereitstellen können.
ms.openlocfilehash: b0efa986c7f230f455d052f8e003616e081e324a
ms.sourcegitcommit: 8968f3107291935ed9adc84bba348d5f187eadae
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/12/2021
ms.locfileid: "11979129"
---
# <a name="deploy-microsoft-edge-using-system-center-configuration-manager"></a>Bereitstellen von Microsoft Edge mithilfe vom System Center Konfigurations-Manager

In diesem Artikel erfahren Sie, wie Sie eine Microsoft Edge-Bereitstellung mithilfe vom System Center Konfigurations-Manager (SCCM) automatisieren.

>[!NOTE]
>Dieser Artikel bezieht sich auf Microsoft Edge Version 77 oder höher.

## <a name="before-you-begin"></a>Vorbemerkungen

Lesen Sie die Informationen im Artikel [Einführung in die Anwendungsverwaltung im Konfigurations-Manager](/sccm/apps/understand/introduction-to-application-management). Dieser Artikel zur Anwendungsverwaltung hilft Ihnen, die in diesem Artikel verwendete Terminologie zu verstehen und ist ein Leitfaden für die Vorbereitung Ihrer Website für die Installation von Anwendungen.

Laden Sie die Microsoft Edge Enterprise-Installationsdateien (**MicrosoftEdgeDevEnterpriseX64.msi** und/oder **MicrosoftEdgeDevEnterpriseX86.msi**) von der [Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)-Angebotsseite herunter.

Stellen Sie sicher, dass Sie die Microsoft Edge-Installationsdateien an einem zugänglichen Netzwerkspeicherort speichern.

## <a name="create-the-application"></a>Erstellen der Anwendung

Sie erstellen die Anwendung mithilfe eines Assistenten für Konfigurations-Manager.

### <a name="start-the-create-application-wizard-and-create-the-application"></a>Starten des Anwendungserstellungs-Assistenten und Erstellen der Anwendung  

1. Klicken Sie in der Konfigurations-Manager-Konsole auf **Softwarebibliothek** > **Anwendungsverwaltung** > **Anwendungen**.  

2. Klicken Sie auf der Registerkarte **Start** in der Gruppe **Erstellen** auf **Anwendung erstellen**. Alternativ klicken Sie in der Navigationsleiste mit der rechten Maustaste auf **Anwendungen** und anschließend auf **Anwendung erstellen**.

    ![Erstellen Ihrer ersten Anwendung](./media/edge-ent-deployment-sccm/edge-ent-create-app-1.png)

3. Aktivieren Sie auf der Seite **Allgemein** des **Assistenten zum Erstellen von Anwendungen** das Kontrollkästchen **Informationen zu dieser Anwendung automatisch anhand der Installationsdateien erkennen**. Dadurch werden einige der Felder im Assistenten vorab mit Informationen gefüllt, die aus der Datei „install. msi” extrahiert wurden. Geben Sie die folgenden Informationen an:  

   - **Typ**: Wählen Sie **Windows Installer (\*.MSI-Datei)** aus.  

   - **Speicherort**: Geben Sie den Speicherort ein (oder klicken Sie auf **Durchsuchen**), um den Speicherort der Installationsdatei **MicrosoftEdgeDevEnterpriseX64.msi** oder **MicrosoftEdgeDevEnterpriseX86.msi** auszuwählen. Beachten Sie, dass der Speicherort im Formular *\\\Server\Share\File* für Konfigurations-Manager angegeben werden muss, um nach der Installationsdateien zu suchen.  

   Die Seite **Einstellungen für diese Anwendung angeben** sieht wie im folgenden Beispiel aus:  

    ![Einstellungen für diese Anwendung angeben](./media/edge-ent-deployment-sccm/edge-ent-create-app-2.png)

4. Klicken Sie auf **Weiter**. Auf der Seite **Importierte Informationen** werden unter **Details** Informationen über die Anwendung und alle zugeordneten Dateien angezeigt, die importiert wurden. Klicken Sie auf **Weiter** , um die Herstellung der drahtgebundenen Verbindung fortzusetzen.  

    ![Importierte Informationen anzeigen](./media/edge-ent-deployment-sccm/edge-ent-create-app-3.png)

5. Auf der Seite **Allgemeine Informationen** können Sie weitere Informationen zur Anwendung hinzufügen. Zum Beispiel Softwareversion, Administratorkommentare und Herausgeber. Mithilfe dieser Informationen können Sie die Anwendung in der Konfigurations-Manager-Konsole sortieren und suchen.

   Sie können auch das Feld **Installationsprogramm** verwenden, um die vollständige Befehlszeile anzugeben, die zum Installieren der Anwendung auf PCs verwendet wird. Sie können dies bearbeiten, um eigene Eigenschaften hinzuzufügen (z. B. **/q** für eine unbeaufsichtigte Installation).

   Der folgende Screenshot zeigt ein Beispiel, in dem die Felder **Informationen über diese Anwendung angeben** verwendet werden.

   ![Anwendungsmetadaten angeben](./media/edge-ent-deployment-sccm/edge-ent-create-app-5.png)

6. Klicken Sie auf **Weiter**.
7. Auf der Seite **Zusammenfassung** können Sie die Anwendungseinstellungen unter **Details** bestätigen und anschließend den Assistenten beenden. Klicken Sie auf **Weiter**.  

    ![Details der Anwendungseinstellungen](./media/edge-ent-deployment-sccm/edge-ent-create-app-6.png)

8. Klicken Sie auf der Seite **Fertigstellung** auf **Schließen**.

    ![Dialogfeld mit der Erfolgsmeldung](./media/edge-ent-deployment-sccm/edge-ent-create-app-7.png)

Sie haben die Anwendung fertig erstellt. Führen Sie die folgenden Schritteaus, um sie im Konfigurations-Manager anzuzeigen:

- wählen Sie den Arbeitsbereich **Softwarebibliothek** aus
- erweitern Sie die **Anwendungsverwaltung**
- klicken Sie auf **Anwendungen**.

Der folgende Screenshot zeigt das für diesen Artikel verwendete Beispiel.  

![Anwendungen](./media/edge-ent-deployment-sccm/edge-ent-create-app-8.png)

## <a name="change-application-properties-and-deployment-settings"></a>Ändern von Anwendungseigenschaften und Bereitstellungseinstellungen

Nachdem Sie eine Anwendung erstellt haben, können Sie die Anwendungseinstellungen bei Bedarf verfeinern. So zeigen Sie die Anwendungseigenschaften an:

- wählen Sie die Anwendung aus
- Klicken Sie unter **Home**>**Eigenschaften** auf **Eigenschaften**.  

   ![Konfigurieren der Anwendungseigenschaften](./media/edge-ent-deployment-sccm/edge-ent-create-app-req-1.png)

 Auf der Dialogseite **<application name\> Anwendungseigenschaften** wird eine Registerkartenansicht der Elemente angezeigt, die Sie konfigurieren können, um das Verhalten der Anwendung zu ändern. Weitere Informationen über die konfigurierbaren Einstellungen finden Sie unter [Anwendungen erstellen](/sccm/apps/deploy-use/create-applications).

In diesem Beispiel ändern Sie einige Eigenschaften des Bereitstellungstyps der Anwendung. So ändern Sie die Bereitstellungseigenschaften:

1. Klicken Sie auf die Registerkarte **Bereitstellungstypen**.
2. Wählen Sie unter **Bereitstellungstypen** den **Namen** der Anwendung aus.
3. Klicken Sie auf **Bearbeiten**.

   ![Bearbeiten Sie den Bereitstellungstyp.](./media/edge-ent-deployment-sccm/edge-ent-create-app-req-2.png)

### <a name="add-a-requirement-to-the-deployment-type"></a>Fügen Sie dem Bereitstellungstyp eine Anforderung hinzu.

 Mit Anforderungen werden Bedingungen angegeben, die erfüllt sein müssen, bevor eine Anwendung auf einem Gerät installiert wird. Sie können aus integrierten Anforderungen auswählen oder Ihre eigene Anforderung erstellen. Sie können beispielsweise eine Anforderung hinzufügen, dass die Anwendung nur auf PCs installiert wird, auf denen Windows10 **x86** oder **x64** ausgeführt wird, abhängig von der Zielprozessorarchitektur der Installationsdatei. In diesem Beispiel geben Sie Windows10 **x86** an.

1. Klicken Sie auf der soeben geöffneten Seite „Eigenschaften des Bereitstellungstyps” auf die Registerkarte **Anforderungen**.

2. Klicken Sie auf **Hinzufügen**, um das Dialogfeld **Anforderung erstellen** zu öffnen.

    ![Anforderung erstellen](./media/edge-ent-deployment-sccm/edge-ent-create-app-req-3.png)

3. Geben Sie im Dialogfeld **Anforderung erstellen** die folgenden Informationen ein:

    - **Kategorie**: **Gerät**  

    - **Bedingung**: **Betriebssystem**  

    - **Regeltyp**: **Wert**  

    - **Operator**: **Einer von**  

    - Wählen Sie in der Liste der Betriebssysteme **Windows10** > **Alle Windows10 (32-Bit)-Systeme** aus.  

    Wenn Sie fertig sind, sieht das Dialogfeld folgendermaßen aus:

    ![Anforderung hinzufügen](./media/edge-ent-deployment-sccm/edge-ent-create-app-req-4.png)

4. Klicken Sie auf **OK**, um die einzelnen geöffneten Eigenschaftenseiten zu schließen und zur Liste **Anwendungen** in der Konfigurations-Manager-Konsole zurückzukehren.  

## <a name="add-the-application-content-to-a-distribution-point"></a>Hinzufügen des Anwendungsinhalts zu einem Verteilungspunkt  

Um die aktualisierte Anwendung auf PCs bereitzustellen, müssen Sie sicherstellen, dass der Anwendungsinhalt auf einen Verteilungspunkt kopiert wird. PCs greifen auf den Verteilungspunkt zu, um die Anwendung zu installieren.  

>[!TIP]
>Weitere Informationen zu Verteilungspunkten und zur Inhaltsverwaltung im Konfigurations-Manager finden Sie unter [Bereitstellen und Verwalten von Inhalten für System Center Konfigurations-Manager](/sccm/core/servers/deploy/configure/deploy-and-manage-content).  

1. Klicken Sie in der Konfigurations-Manager-Konsole auf **Softwarebibliothek**.  

2. Erweitern Sie im Arbeitsbereich **Softwarebibliothek** den Eintrag **Anwendungen**. Wählen Sie in der Liste der Anwendungen die von Ihnen erstellte Anwendung aus.

3. Klicken Sie in der **Bereitstellungsgruppe** auf der Registerkarte **Start** auf **Inhalt verteilen**.  

4. Überprüfen Sie auf der Seite **Allgemein** des **Assistenten für die Verteilung von Inhalt**, ob der Anwendungsname korrekt ist, und klicken Sie dann auf **Weiter**.  

5. Überprüfen Sie auf der Seite **Inhalt** die Informationen, die in den Verteilungspunkt kopiert werden, und klicken Sie dann auf **Weiter**.  

6. Klicken Sie auf der Seite **Inhaltsziel** auf **Hinzufügen**, um eine oder mehrere Sammlungen, Verteilungspunkte oder die Verteilungspunktgruppe auszuwählen, auf denen der Anwendungsinhalt installiert werden soll.

7. Führen Sie den Assistenten bis zum Ende aus.

Sie können im Arbeitsbereich **Überwachung** unter **Verteilungsstatus** > **Inhaltsstatus** überprüfen, ob der Anwendungsinhalt erfolgreich auf den Verteilungspunkt kopiert wurde.  

## <a name="deploy-the-application"></a>Bereitstellen der Anwendung  

Stellen Sie als Nächstes die Anwendung für eine Gerätesammlung in Ihrer Hierarchie bereit. In diesem Beispiel stellen Sie die Anwendung für die Gerätesammlung **Alle Systeme“** bereit.  

>[!TIP]
>Beachten Sie, dass die Anwendung nur von Windows 10-Computern mit der angegebenen Prozessorarchitektur aufgrund der zuvor ausgewählten Anforderungen installiert wird.  

1. Klicken Sie in der Konfigurations-Manager-Konsole auf **Softwarebibliothek** > **Anwendungsverwaltung** > **Anwendungen**.

2. Wählen Sie aus der Liste der Anwendungen die Anwendung aus, die Sie zuvor erstellt haben. Klicken Sie dann auf der Registerkarte **Start** in der Gruppe **Bereitstellung** auf **Bereitstellen**, oder klicken Sie mit der rechten Maustaste auf die Anwendung und wählen Sie **Bereitstellen** aus.

    ![Bereitstellen der Anwendung](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-1.png)

3. Klicken Sie im **Assistenten zum Bereitstellen von Software** auf der Seite **Allgemein** auf **Durchsuchen**, um die Gerätesammlung auszuwählen, für die Sie die Anwendung bereitstellen möchten.

    ![Navigieren zur Installationsdatei](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-2.png)

4. Überprüfen Sie auf der Seite **Inhalt**, ob der Verteilungspunkt ausgewählt ist, von dem aus PCs die Anwendung installieren sollen.

    ![Angeben des Verteilungspunktes](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-6.png)

5. Stellen Sie auf der Seite **Bereitstellungseinstellungen** sicher, dass die Bereitstellungsaktion auf **Installieren** und der Bereitstellungszweck auf **Erforderlich** festgelegt ist.

    ![Konfigurieren der Bereitstellungseinstellungen](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-8.png)

    >[!TIP]
    >Indem Sie den Bereitstellungszweck auf **Erforderlich** festlegen, stellen Sie sicher, dass die Anwendung auf PCs installiert wird, die die von Ihnen festgelegten Anforderungen erfüllen. Wenn Sie diesen Wert auf **"Verfügbar**" festlegen, können Benutzer die Anwendung bei Bedarf über das Software Center installieren.  

6. Auf der Seite **Planen** können Sie konfigurieren, wann die Anwendung installiert wird. Wählen Sie in diesem Beispiel **So bald wie möglich nach dem Zeitpunkt der Verfügbarkeit** aus.

    ![Planen der Bereitstellung](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-9.png)

7. Wählen Sie auf der Seite **Installationsoptionen** die gewünschten Werte aus und klicken Sie auf **Weiter**.

    ![Angeben von Installationsoptionen](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-10.png)

8. Geben Sie die gewünschten Benachrichtigungsoptionen an und klicken Sie auf **Weiter**.

    ![Angeben von Benachrichtigungseinstellungen](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-11.png)

9. Führen Sie den Assistenten bis zum Ende aus.

Verwenden Sie die Informationen im folgenden Abschnitt **Überwachen der Anwendung**, um den Status der Anwendungsbereitstellung anzuzeigen.  

## <a name="monitor-the-application"></a>Die Anwendung überwachen

 In diesem Abschnittsehen Sie sich den Bereitstellungsstatus der soeben bereitgestellten Anwendung an.  

### <a name="to-review-the-deployment-status"></a>So überprüfen Sie den Bereitstellungsstatus  

1. Klicken Sie in der Konfigurations-Manager-Konsole auf **Überwachung** > **Bereitstellungen**.  

2. Wählen Sie die Anwendung aus der Liste der Bereitstellungen aus.

    ![Überwachen der Bereitstellung](./media/edge-ent-deployment-sccm/edge-ent-monitor-deployment.png)

3. Klicken Sie auf der Registerkarte **Start** in der Gruppe **Bereitstellung** auf **Status anzeigen**.  

4. Wählen Sie eine der folgenden Registerkarten aus, um weitere Statusaktualisierungen zur Anwendungsbereitstellung anzuzeigen:  

    - **Erfolg**: Die Anwendung wurde auf den angegebenen PCs erfolgreich installiert.  

    - **In Bearbeitung**: Die Anwendung ist noch nicht fertig installiert.  

    - **Fehler**: Bei der Installation der Anwendung auf den angegebenen PCs ist ein Fehler aufgetreten. Weitere Informationen zum Fehler werden ebenfalls angezeigt.  

    - **Anforderungen nicht erfüllt**: Auf den angegebenen Geräten wurde kein Installationsversuch durchgeführt, da sie nicht den von Ihnen konfigurierten Anforderungen entsprachen (in diesem Beispiel, weil sie nicht unter Windows 10 ausgeführt werden).

    - **Unbekannt**: Der Konfigurations-Manager konnte den Status der Bereitstellung nicht melden. Bitte versuchen Sie es später noch einmal.  

    >[!TIP]
    >Es gibt verschiedene Möglichkeiten, Anwendungsbereitstellungen zu überwachen. Weitere Informationen finden Sie unter [Überwachen von Anwendungen in der System Center Konfigurations-Manager-Konsole](/sccm/apps/deploy-use/monitor-applications-from-the-console).  

## <a name="end-user-experience"></a>Installationsoptionen für Endbenutzer  

Benutzer mit PCs, die von Konfigurations-Manager verwaltet werden und Windows10 der angegebenen Prozessorarchitektur ausführen, werden in einer Meldung darüber informiert, dass sie die Microsoft Edge Dev-Anwendung installieren müssen. Wenn sie diese Installationsoption akzeptieren, wird die Anwendung installiert.  

## <a name="see-also"></a>Weitere Informationen:

- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)
- [Weitere Informationen zum Bereitstellen von MSI-Paketen finden Sie unter Erstellen und Bereitstellen einer Anwendung mit System Center Konfigurations-Manager.](/sccm/apps/get-started/create-and-deploy-an-application)