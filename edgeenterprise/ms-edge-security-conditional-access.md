---
title: Microsoft Edge und bedingter Zugriff
ms.author: srugh
author: srugh
manager: seanlyn
ms.date: 10/02/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Edge und bedingter Zugriff
ms.openlocfilehash: a81d39c15f418dab6565ee7acc45de17f66e3828
ms.sourcegitcommit: 3478cfcf2b03944213a7c7c61f05490bc37aa7c4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/03/2020
ms.locfileid: "11094773"
---
# Microsoft Edge und bedingter Zugriff
  
Dieser Artikel beschreibt, wie Microsoft Edge bedingten Zugriff unterstützt und wie Sie auf Ressourcen zugreifen können, die durch bedingten Zugriff geschützt sind.

> [!NOTE]
> Dieser Artikel bezieht sich auf Microsoft Edge Version 77 oder neuer.

Ein wichtiger Aspekt der Cloud-Sicherheit ist die Identität und der Zugriff, wenn es um die Verwaltung von Cloud-Ressourcen geht. In einer mobilen Welt, in der die Cloud an erster Stelle steht, können Benutzer mit einer Vielzahl von Geräten und Apps von überall aus auf die Ressourcen Ihres Unternehmens zugreifen. Folglich reicht es nicht aus, sich nur darauf zu konzentrieren, wer auf eine Ressource zugreifen kann. Sie müssen auch berücksichtigen, wie auf eine Ressource zugegriffen wird. Mit bedingtem Zugriff auf Azure Active Directory (Azure AD) können Sie das Gleichgewicht zwischen Sicherheit und Produktivität herstellen.

## Zugriff auf Ressourcen mit Zugriffsschutz in Microsoft Edge

Microsoft Edge unterstützt den Azure AD bedingten Zugriff systemeigen. Es ist nicht erforderlich, eine separate Erweiterung zu installieren. Wenn Sie bei einem Microsoft Edge-Profil mit Unternehmens-Azure AD-Anmeldeinformationen angemeldet sind, ermöglicht Microsoft Edge den nahtlosen Zugriff auf Unternehmens-Cloud-Ressourcen, die mit bedingtem Zugriff geschützt sind.

Auf einem kompatiblen Gerät sollte die Identität, die auf die Ressource zugreift, mit der Identität im Profil übereinstimmen.  Wenn dies nicht der Fall ist, wird eine Meldung wie die im nächsten Screenshot angezeigt. Im Screenshot-Beispiel ist „testadmin@evostsoneboxtest.com” das Anmeldekonto, das für den Zugriff auf die Ressource erforderlich ist.

![Nachricht über bedingten Zugriff im Browser](./media/edge-security/microsoft-edge-security-conditional-access.png)

Um fortzufahren, müssen Sie zu dem erforderlichen Profil (falls vorhanden) wechseln oder ein Profil mit einer entsprechenden Identität erstellen.

Klicken Sie in der oberen rechten Ecke des Browsers auf das Profilbild, um sich anzumelden und mit Ihrem Profil zu arbeiten. Sie können das Menü Manage Alert für folgende Aufgaben verwenden:

- Wählen Sie ein anderes Profil aus. Klicken Sie auf den Profilnamen.
- Erstellen eines Marketingprofils Klicken Sie auf **Feature hinzufügen**.
- Verwalten Sie Ihre Profile. Klicken Sie auf **Profileinstellungen verwalten**.

Diese Unterstützung ist auf allen Plattformen verfügbar, einschließlich aller unterstützten Versionen von Windows und macOS.

### So stellen Sie den bedingten Zugriff in Azure Active Directory bereit

[Bereitstellen des bedingten Zugriffs](https://docs.microsoft.com/azure/active-directory/conditional-access/plan-conditional-access) enthält eine ausführliche Anleitung zur Bereitstellung des bedingten Zugriffs in Azure Active Directory.

## Weitere Informationen

- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)
- [Video: Sicherheit, Kompatibilität und Verwaltbarkeit](/microsoft-edge-video-security-compatibility-manageability.md)
