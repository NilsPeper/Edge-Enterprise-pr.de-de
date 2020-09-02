---
title: Übersicht über die Microsoft Edge-Sicherheit
ms.author: srugh
author: srugh
manager: seanlyn
ms.date: 04/29/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Übersicht über die Bereitstellung der Microsoft Edge-Sicherheit
ms.openlocfilehash: f22f2dcbace00cd535d201950c2af488c708525b
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/31/2020
ms.locfileid: "10980076"
---
# Übersicht über die Microsoft Edge-Sicherheit
  
IT-Administratoren im Unternehmen sind ständig mit einer Vielzahl von vorhandenen und neuen Sicherheitsherausforderungen konfrontiert, während sie das Unternehmensnetzwerk und -Geräte vor böswilligen Angriffen schützen und unbefugten Zugriff und Undichtigkeiten von Unternehmensdaten verhindern. Microsoft Edge bietet mehrere systemeigene, einzigartige Funktionen, mit denen diese Herausforderungen bewältigt werden können.

> [!NOTE]
> Dieser Artikel bezieht sich auf Microsoft Edge Version77 oder höher.

## Bedingter Zugriff

Ein wichtiger Aspekt der Cloud-Sicherheit ist die Identität und der Zugriff, wenn es um die Verwaltung von Cloud-Ressourcen geht. In einer mobilen Welt, in der die Cloud an erster Stelle steht, können Benutzer mit einer Vielzahl von Geräten und Apps von überall aus auf die Ressourcen Ihres Unternehmens zugreifen. Folglich reicht es nicht aus, sich nur darauf zu konzentrieren, wer auf eine Ressource zugreifen kann. Sie müssen auch berücksichtigen, wie auf eine Ressource zugegriffen wird. Mit bedingtem Zugriff auf Azure Active Directory (Azure AD) können Sie das Gleichgewicht zwischen Sicherheit und Produktivität herstellen.

### Zugriff auf Ressourcen mit Zugriffsschutz in Microsoft Edge

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
