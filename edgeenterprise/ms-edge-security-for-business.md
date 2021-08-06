---
title: Sicherheit in Microsoft Edge für Ihr Unternehmen
ms.author: collw
author: seanongit
manager: chuckf
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Sicherheit in Microsoft Edge für Ihr Unternehmen
ms.openlocfilehash: f3ed91c76cb686b0ce67608f749817cce48b412831f29c7734fa0eec06694dd5
ms.sourcegitcommit: d44c0997ffe40d67421312ed96e7766da947eaa0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "11727388"
---
# <a name="microsoft-edge-security-for-your-business"></a>Sicherheit in Microsoft Edge für Ihr Unternehmen

Microsoft Edge basiert auf dem Open Source-Projekt "Chromium", also dem gleichen Projekt, das Google Chrome zugrunde liegt. Das bedeutet, dass er auf der gleichen bewährten und intensiv getesteten Sicherheitsarchitektur und dem gleichen Sicherheitskonzept gründet. Doch die Sicherheit, die Microsoft Edge bietet, geht noch darüber hinaus. Tatsächlich ist **Microsoft Edge unter Windows 10 sicherer als Google Chrome für Ihr Unternehmen**. Er bietet leistungsstarke, integrierte Lösungen zum Schutz vor Phishing und Malware und unterstützt unter Windows 10 nativ die Hardwareisolierung. Es ist keine zusätzliche Software nötig, um diese sichere Grundlage zu schaffen. Zudem bietet Microsoft Edge, mit der nativen Unterstützung von Microsoft 365 Sicherheits- und Compliancediensten gekoppelt, zusätzliche, leistungsstarke Sicherheitsfunktionen und Features, die den Schutz vor Datenverlusten noch weiter verbessern. Weitere Informationen finden Sie im [Video: Sicherheit, Kompatibilität und Verwaltbarkeit von Microsoft Edge](microsoft-edge-video-security-compatibility-manageability.md).

Wir beginnen die Vertiefung mit **externen Bedrohungen**, und gehen dann zu **internen Risiken und Informationsschutz** über.

## <a name="external-threat-protection"></a>Schutz vor externen Bedrohungen

### <a name="highest-rated-protection-against-phishing-and-malware"></a>Hoch bewerteter Schutz vor Phishing und Schadsoftware

In Microsoft Edge integriert, blockiert SmartScreen laut einer unabhängigen Studie von NSS Labs mehr [Phishing](https://query.prod.cms.rt.microsoft.com/cms/api/am/binary/RWASN1)- und [Malware](https://query.prod.cms.rt.microsoft.com/cms/api/am/binary/RWANMW)-Versuche als das sichere Browsen von Google Chrome. SmartScreen überprüft die Zuverlässigkeit von Websites und Downloads in Echtzeit, wenn Benutzer online arbeiten, und ist Teil von [Microsoft Intelligent Security Graph](https://www.microsoft.com/microsoft-365/windows/intelligent-security), das Signale und Erkenntnisse aufzeichnet, die von Microsofts großem Netzwerk aus globalen Ressourcen, Forschern und Partnern generiert werden. Durch die Überprüfung anhand dynamischer, Cloud-basierter Listen gefährlicher Websites und Downloads hilft Ihnen Microsoft Edge beim Erkennen und Blockieren von selbst kurzlebigen Bedrohungen, die schnell wieder verschwinden.  

[Microsoft Edge SmartScreen](//DeployEdge/microsoft-edge-security-smartscreen) hat 95,5 % der Phishing-Versuche während des [NSS Labs-Phishing-Schutztests](https://query.prod.cms.rt.microsoft.com/cms/api/am/binary/RWASN1) und 98,5 % der Schadsoftwareversuche während dem [NSS Labs-Tests zum Schutz vor Schadsoftware](https://query.prod.cms.rt.microsoft.com/cms/api/am/binary/RWANMW)blockiert, im Vergleich zu den „Sicheres Browsen“-Zahlen von Chrome von 86,9 % bzw. 86,0 %.

### <a name="the-only-browser-on-windows-10-that-natively-supports-hardware-isolation"></a>Der einzige Browser unter Windows 10, der die Hardwareisolierung nativ unterstützt

Microsoft Edge ist der einzige Browser unter Windows 10, der Funktionen für die Hardwareisolierung nativ unterstützt. Als Bestandteil von Windows 10 Pro oder Enterprise führt Microsoft Defender Application Guard (Application Guard) nicht vertrauenswürdige Websites in einem Kernel aus, der vom lokalen Gerät und internen Netzwerken isoliert ist. Die nicht vertrauenswürdigen Websites werden in einem "Container" ausgeführt, der bei einem Angriff in eine Sandbox verlegt und somit vom restlichen Unternehmensnetzwerk isoliert wird. Weitere Informationen finden Sie unter [Microsoft Edge-Unterstützung für Application Guard](./microsoft-edge-security-windows-defender-application-guard.md).

Für Chrome ist eine Erweiterung für die Nutzung der Hardwareisolierung unter Windows 10 verfügbar: die MDAG-Erweiterung. Diese Erweiterung führt Microsoft Edge aus, um die Isolierung auf Kernelebene von Application Guard zu nutzen. Um eine ähnliche Isolierung auf Kernelebene für eine reine Chrome-Lösung zu erreichen, ist Isolierungssoftware von Drittanbietern erforderlich.

> [!NOTE]
> Application Guard ist unter Windows 10, 1809 und höher verfügbar. Application Guard ist in Windows 10 Home-Editionen nicht verfügbar.

## <a name="internal-risks-and-information-protection"></a>Interne Risiken und Informationsschutz

### <a name="native-support-for-microsoft-365-security-without-additional-software"></a>Native Unterstützung von Microsoft 365 Security ohne zusätzliche Software

Neben dem Schutz vor externen Bedrohungen müssen IT-Administratoren auch für den Schutz vor internen Risiken sorgen. Der zuverlässige und anpassbare Schutz vertraulicher Unternehmensdaten hat für IT-Administratoren hohe Priorität, insbesondere, wenn die Mitarbeiter dezentral arbeiten. Microsoft Edge ist der einzige Browser mit systemeigener Unterstützung für das Azure AD-Feature für bedingten Zugriff, Windows Information Protection und das neue Microsoft-Feature zur Verhinderung von Datenverlust am Endpunkt (Data Loss Prevention, DLP), ohne dass zusätzliche Software erforderlich ist.

**Microsoft Edge ist der einzige Browser, der den bedingten Zugriff nativ unterstützt**. [Die Unterstützung des bedingten Zugriffs durch Microsoft Edge](ms-edge-security-conditional-access.md) erleichtert es Organisationen, Identitätssignale im Rahmen ihrer Maßnahmen zur Zugriffssteuerung zu nutzen. [Der bedingte Zugriff](/azure/active-directory/conditional-access/overview) ist das von Azure Active Directory genutzte Tool, um Signale zusammenzuführen, Entscheidungen zu treffen und Organisationsrichtlinien durchzusetzen. Der bedingte Zugriff ist das Herzstück der neuen identitätsorientierten Steuerungsebene. Damit der bedingte Zugriff in Chrome unterstützt wird, ist ein zusätzliches Plug-In erforderlich.

> [!NOTE]
> Für das Azure AD-Feature für bedingten Zugriff ist ein Microsoft 365 E3-Abonnement oder höher erforderlich.

**Microsoft Edge ist der einzige Browser, der Windows Information Protection (WIP) nativ unterstützt**. Dies trägt zum Schutz von Unternehmensdaten und zur Verhinderung von Datenlecks durch Benutzer auf Windows 10-Geräten bei. [Die Unterstützung von WIP durch Microsoft Edge](./microsoft-edge-security-windows-information-protection.md) kann so konfiguriert werden, dass der Zugriff auf Unternehmensdaten nur von der IT-Abteilung festgelegten Apps gestattet ist. Hinzu kommen Kontrollfunktionen zur Verhinderung von Datenlecks wie der Schutz der Zwischenablage, das Verschlüsseln von Dateien beim Download und das Verhindern von Dateiuploads in nicht autorisierte Netzwerkfreigaben oder Cloud-Speicherorte, und das alles in einer nahtlosen Benutzerumgebung. WIP funktioniert auf der Grundlage einer perimeterbasierten Konfiguration: Die IT-Administratoren definieren die Grenze des Unternehmen, und alle Daten innerhalb dieser Grenze werden als dem Unternehmen zugehörig betrachtet. Chrome ist nicht für WIP mit Kontrollfunktionen zur Verhinderung von Datenlecks optimiert.

> [!NOTE]
> Die Konfiguration von Windows Information Protection (WIP) erfordert entweder die Lizenzierung von Microsoft Intune oder Microsoft Endpoint Configuration Manager, oder die Verwendung einer MDM-Lösung (Mobile Device Management) von Drittanbietern, für die möglicherweise zusätzliche Lizenzen erforderlich sind.

**Microsoft Endpoint-Verhinderung von Datenverlust (Endpunkt-DLP) wird nur nativ in Microsoft Edge unterstützt**. Endpunkt-DLP wird in das Microsoft-Sicherheitscenter integriert und erweitert den Informationsschutz auf Microsoft Edge, um Benutzer auf nicht konforme Aktivitäten aufmerksam zu unterstützen und Datenverluste zu verhindern, wenn Benutzer online arbeiten. Es erkennt und kennzeichnet vertrauliche Daten innerhalb des Unternehmens, die vom Administrator festgelegten Kriterien entsprechen, z. B. Dateien mit Kreditkartennummern oder behördlichen IDs (beispielsweise Sozialversicherungsnummern), Finanzinformationen usw. Microsoft Information Protection-Richtlinien können ohne zusätzliche Neukonfiguration für Microsoft Endpunkt-DLP genutzt werden, einschließlich Bezeichner für vertrauliche Inhalte und von den IT-Administratoren bereits angepasster Richtlinien. Dies bedeutet die nahtlose Bereitstellung von Informationsschutz für IT-Administratoren.

Weitere Informationen zu den Voraussetzungen für Endpunkt-DLP und deren Einrichtung finden Sie unter [Erste Schritte mit Endpunkt-Datenverlust Verhinderung](/microsoft-365/compliance/endpoint-dlp-getting-started?preserve-view=true&view=o365-worldwide).

> [!NOTE]
> Microsoft 365 E5-oder Microsoft 365 E5-Konformitätsabonnement erforderlich für Microsoft Endpoint-Datenverlust Verhinderung.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft Edge Enterprise-Angebotsseite](https://aka.ms/EdgeEnterprise)
- [Video: Microsoft Edge: Sicherheit, Kompatibilität und Verwaltbarkeit](microsoft-edge-video-security-compatibility-manageability.md)