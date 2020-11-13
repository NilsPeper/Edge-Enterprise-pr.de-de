---
title: Sicherheit in Microsoft Edge für Ihr Unternehmen
ms.author: seanlynd
author: seanongit
manager: chuckf
ms.date: 11/11/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Sicherheit in Microsoft Edge für Ihr Unternehmen
ms.openlocfilehash: e2f45d49d8f4960f3f2263098ff2eb7d0103b6ea
ms.sourcegitcommit: 5efa7f6196804da205c3deff4ba7917a94ffcf4f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/11/2020
ms.locfileid: "11165935"
---
# Sicherheit in Microsoft Edge für Ihr Unternehmen

Microsoft Edge basiert auf dem Open Source-Projekt "Chromium", also dem gleichen Projekt, das Google Chrome zugrunde liegt. Das bedeutet, dass er auf der gleichen bewährten und intensiv getesteten Sicherheitsarchitektur und dem gleichen Sicherheitskonzept gründet. Doch die Sicherheit, die Microsoft Edge bietet, geht noch darüber hinaus. Tatsächlich ist **Microsoft Edge unter Windows 10 sicherer als Google Chrome für Ihr Unternehmen**. Er bietet leistungsstarke, integrierte Lösungen zum Schutz vor Phishing und Malware und unterstützt unter Windows 10 nativ die Hardwareisolierung. Es ist keine zusätzliche Software nötig, um diese sichere Grundlage zu schaffen. Zudem bietet Microsoft Edge, mit der nativen Unterstützung von Microsoft 365 Sicherheits- und Compliancediensten gekoppelt, zusätzliche, leistungsstarke Sicherheitsfunktionen und Features, die den Schutz vor Datenverlusten noch weiter verbessern.

Wir beginnen die Vertiefung mit **externen Bedrohungen**, und gehen dann zu **internen Risiken und Informationsschutz** über.

## Schutz vor externen Bedrohungen

### Hoch bewerteter Schutz vor Phishing und Schadsoftware

In Microsoft Edge integriert, blockiert SmartScreen laut einer unabhängigen Studie von NSS Labs mehr [Phishing](https://edgeconsumerproduction.blob.core.windows.net/hostingdocs/NSS_Labs_Browser_Phishing_Report_Q2_2020.pdf)- und [Malware](https://edgeconsumerproduction.blob.core.windows.net/hostingdocs/NSS_Labs_Browser_Malware_Report_Q2_2020.pdf)-Versuche als das sichere Browsen von Google Chrome. SmartScreen überprüft die Zuverlässigkeit von Websites und Downloads in Echtzeit, wenn Benutzer online arbeiten, und ist Teil von [Microsoft Intelligent Security Graph](https://www.microsoft.com/microsoft-365/windows/intelligent-security), das Signale und Erkenntnisse aufzeichnet, die von Microsofts großem Netzwerk aus globalen Ressourcen, Forschern und Partnern generiert werden. Durch die Überprüfung anhand dynamischer, Cloud-basierter Listen gefährlicher Websites und Downloads hilft Ihnen Microsoft Edge beim Erkennen und Blockieren von selbst kurzlebigen Bedrohungen, die schnell wieder verschwinden.  

[Microsoft Edge mit SmartScreen](https://docs.microsoft.com//DeployEdge/microsoft-edge-security-smartscreen) blockierte [während des NSS Labs-Tests](https://www.nsslabs.com/tested-technologies/web-browser-security-wbs/) 95,5 % der Phishing-Versuche und 98, 5% aller Angriffsversuche durch Schadsoftware, während die Raten der Safe Browsing-Funktion von Chrome bei 86,9 % bzw. 86,0 % lagen.

### Der einzige Browser unter Windows 10, der die Hardwareisolierung nativ unterstützt

Microsoft Edge ist der einzige Browser unter Windows 10, der Funktionen für die Hardwareisolierung nativ unterstützt. Als Bestandteil von Windows 10 Pro oder Enterprise führt Microsoft Defender Application Guard (Application Guard) nicht vertrauenswürdige Websites in einem Kernel aus, der vom lokalen Gerät und internen Netzwerken isoliert ist. Die nicht vertrauenswürdigen Websites werden in einem "Container" ausgeführt, der bei einem Angriff in eine Sandbox verlegt und somit vom restlichen Unternehmensnetzwerk isoliert wird. Weitere Informationen finden Sie unter [Microsoft Edge-Unterstützung für Application Guard](https://docs.microsoft.com/DeployEdge/microsoft-edge-security-windows-defender-application-guard).

Für Chrome ist eine Erweiterung für die Nutzung der Hardwareisolierung unter Windows 10 verfügbar: die MDAG-Erweiterung. Diese Erweiterung führt Microsoft Edge aus, um die Isolierung auf Kernelebene von Application Guard zu nutzen. Um eine ähnliche Isolierung auf Kernelebene für eine reine Chrome-Lösung zu erreichen, ist Isolierungssoftware von Drittanbietern erforderlich.

> [!NOTE]
> Application Guard ist unter Windows 10, 1809 und höher verfügbar. Application Guard ist in Windows 10 Home-Editionen nicht verfügbar.

## Interne Risiken und Informationsschutz

### Native Unterstützung von Microsoft 365 Security ohne zusätzliche Software

Neben dem Schutz vor externen Bedrohungen müssen IT-Administratoren auch für den Schutz vor internen Risiken sorgen. Der zuverlässige und anpassbare Schutz vertraulicher Unternehmensdaten hat für IT-Administratoren hohe Priorität, insbesondere, wenn die Mitarbeiter dezentral arbeiten. Microsoft Edge ist der einzige Browser mit systemeigener Unterstützung für das Azure AD-Feature für bedingten Zugriff, Windows Information Protection und das neue Microsoft-Feature zur Verhinderung von Datenverlust am Endpunkt (Data Loss Prevention, DLP), ohne dass zusätzliche Software erforderlich ist.

**Microsoft Edge ist der einzige Browser, der den bedingten Zugriff nativ unterstützt**. [Die Unterstützung des bedingten Zugriffs durch Microsoft Edge](ms-edge-security-conditional-access.md) erleichtert es Organisationen, Identitätssignale im Rahmen ihrer Maßnahmen zur Zugriffssteuerung zu nutzen. [Der bedingte Zugriff](https://docs.microsoft.com/azure/active-directory/conditional-access/overview) ist das von Azure Active Directory genutzte Tool, um Signale zusammenzuführen, Entscheidungen zu treffen und Organisationsrichtlinien durchzusetzen. Der bedingte Zugriff ist das Herzstück der neuen identitätsorientierten Steuerungsebene. Damit der bedingte Zugriff in Chrome unterstützt wird, ist ein zusätzliches Plug-In erforderlich.

> [!NOTE]
> Für das Azure AD-Feature für bedingten Zugriff ist ein Microsoft 365 E3-Abonnement oder höher erforderlich.

**Microsoft Edge ist der einzige Browser, der Windows Information Protection (WIP) nativ unterstützt**. Dies trägt zum Schutz von Unternehmensdaten und zur Verhinderung von Datenlecks durch Benutzer auf Windows 10-Geräten bei. [Die Unterstützung von WIP durch Microsoft Edge](https://docs.microsoft.com/DeployEdge/microsoft-edge-security-windows-information-protection) kann so konfiguriert werden, dass der Zugriff auf Unternehmensdaten nur von der IT-Abteilung festgelegten Apps gestattet ist. Hinzu kommen Kontrollfunktionen zur Verhinderung von Datenlecks wie der Schutz der Zwischenablage, das Verschlüsseln von Dateien beim Download und das Verhindern von Dateiuploads in nicht autorisierte Netzwerkfreigaben oder Cloud-Speicherorte, und das alles in einer nahtlosen Benutzerumgebung. WIP funktioniert auf der Grundlage einer perimeterbasierten Konfiguration: Die IT-Administratoren definieren die Grenze des Unternehmen, und alle Daten innerhalb dieser Grenze werden als dem Unternehmen zugehörig betrachtet. Chrome ist nicht für WIP mit Kontrollfunktionen zur Verhinderung von Datenlecks optimiert.

> [!NOTE]
> Die Konfiguration von Windows Information Protection (WIP) erfordert entweder die Lizenzierung von Microsoft Intune oder Microsoft Endpoint Configuration Manager, oder die Verwendung einer MDM-Lösung (Mobile Device Management) von Drittanbietern, für die möglicherweise zusätzliche Lizenzen erforderlich sind.

**Microsoft-Endpunkt-DLP wird in Microsoft Edge nur nativ unterstützt**. Microsoft Endpunkt-DLP (Data Loss Prevention, Verhinderung von Datenverlust am Endpunkt) ist in das Microsoft Security Center integriert und erweitert den Informationsschutz auf Microsoft Edge, damit Benutzer auf nicht kompatible Aktivitäten aufmerksam gemacht werden und um den Verlust von Daten zu verhindern, wenn Benutzer online arbeiten. Es erkennt und kennzeichnet vertrauliche Daten innerhalb des Unternehmens, die vom Administrator festgelegten Kriterien entsprechen, z. B. Dateien mit Kreditkartennummern oder behördlichen IDs (beispielsweise Sozialversicherungsnummern), Finanzinformationen usw. Microsoft Information Protection-Richtlinien können ohne zusätzliche Neukonfiguration für Microsoft Endpunkt-DLP genutzt werden, einschließlich Bezeichner für vertrauliche Inhalte und von den IT-Administratoren bereits angepasster Richtlinien. Dies bedeutet die nahtlose Bereitstellung von Informationsschutz für IT-Administratoren.

> [!NOTE]
> Für Microsoft Endpunkt-DLP ist ein Microsoft 365 E5- oder Microsoft 365 E5-Compliance-Abonnement erforderlich.

## Weitere Informationen

- [Angebotsseite für Microsoft Edge für Unternehmen](https://aka.ms/EdgeEnterprise)
