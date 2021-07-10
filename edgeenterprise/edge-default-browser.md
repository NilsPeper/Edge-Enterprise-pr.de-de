---
title: Festlegen von Microsoft Edge als Standardbrowser unter Windows und macOS
ms.author: brianalt
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Erfahren Sie, wie Sie Microsoft Edge als Standardbrowser festlegen
ms.openlocfilehash: 191d7835a0c4aacfc2fde409c57622ff5a351926
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "11641541"
---
# <a name="set-microsoft-edge-as-the-default-browser"></a>Festlegen von Microsoft Edge als Standardbrowser

In diesem Artikel wird erläutert, wie Sie Microsoft Edge als Standardbrowser unter Windows und macOS festlegen können.

> [!NOTE]
> Dieser Artikel bezieht sich auf Microsoft Edge Version 77 oder höher unter Windows 8 und Windows 10. Informationen zu Windows7 und macOS finden Sie in der Richtlinie [Festlegen von Microsoft Edge als Standardbrowser](./microsoft-edge-policies.md#defaultbrowsersettingenabled).

## <a name="introduction"></a>Einführung

Sie können die Gruppenrichtlinie **Konfigurationsdatei für Standardzuordnungen festlegen** bzw. die MDM-Einstellung [DefaultAssociationsConfiguration](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration) für Mobilgeräteverwaltung verwenden, um Microsoft Edge als Standardbrowser für Ihre Organisation festzulegen.

Verwenden Sie das folgende Beispiel für eine Anwendungszuordnungsdatei, um Microsoft Edge Stable als Standardbrowser für HTML-Dateien, http- bzw. https-Links und PDF-Dateien festzulegen:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<DefaultAssociations> 
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier=".html"/>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier=".htm"/>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier="http"/>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier="https"/>  
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgePDF" Identifier=".pdf"/>
</DefaultAssociations>
```

> [!NOTE]
> Wenn Sie Microsoft Edge Beta als Standardbrowser festlegen möchten, legen Sie **ApplicationName** auf „Microsoft Edge Beta” und **ProgId** auf „MSEdgeBHTML” fest. Wenn Sie Microsoft Edge Dev als Standardbrowser festlegen möchten, legen Sie **ApplicationName** auf „Microsoft Edge Dev” und **ProgId** auf „MSEdgeDHTML” fest.


> [!NOTE]
> Die Standarddateizuordnungen werden nicht angewendet, wenn Microsoft Edge nicht auf dem Zielgerät installiert ist. In diesem Szenario werden Benutzer aufgefordert, ihre Standardanwendung auszuwählen, wenn Sie einen Link oder eine HTM/HTML-Datei öffnen.

## <a name="set-microsoft-edge-as-the-default-browser-on-domain-joined-devices"></a>Festlegen von Microsoft Edge als Standardbrowser

Sie können Microsoft Edge auf Geräten mit Domänenbeitritt als Standardbrowser festlegen, indem Sie die Gruppenrichtlinie **Standardzuordnungskonfigurationsdatei festlegen** konfigurieren. Wenn Sie diese Einstellung aktivieren, müssen Sie eine Konfigurationsdatei für Standardzuordnungen erstellen und sie lokal oder auf einer Netzwerkfreigabe speichern. Diese Datei wird lokal oder auf einer Netzwerkfreigabe gespeichert. Weitere Informationen zum Erstellen dieser Datei finden Sie unter [Exportieren und Importieren von Standardanwendungszuordnungen](/windows-hardware/manufacture/desktop/export-or-import-default-application-associations).

### <a name="to-configure-the-group-policy-for-a-default-file-type-and-protocol-associations-configuration-file"></a>So konfigurieren Sie die Gruppenrichtlinie für eine Standardkonfigurationsdatei und eine Konfigurationsdatei für Protokollzuordnungen:

1. Öffnen Sie den Editor für lokale Gruppenrichtlinien und wechseln Sie zu **Computerkonfiguration\Administrative Vorlagen\Windows-Komponenten\Datei-Explorer**.
2. Wählen Sie **Konfigurationsdatei für Standardzuordnungen festlegen** aus.
3. Klicken Sie auf **Richtlinieneinstellung** und dann auf **Aktiviert**.
4. Klicken Sie auf **Aktiviert**, und geben Sie im Bereich Optionen den Speicherort Ihrer Konfigurationsdatei für Standardzuordnungen ein.
5. Klicken Sie auf **OK**, um die Richtlinie zu speichern.

Das Beispiel im nächsten Screenshot zeigt eine Zuordnungsdatei mit dem Namen *appassoc.xml* auf einer Netzwerkfreigabe, auf die vom Zielgerät aus zugegriffen werden kann.

   ![Dateizuordnung in Gruppenrichtlinie aktivieren](./media/edge-learnmore-make-edge-default-browser/edge-learnmore-app-associations.png)

   > [!NOTE]
   > Wenn diese Einstellung aktiviert ist und das Gerät des Benutzers einer Domäne angehört, wird die Konfigurationsdatei für Zuordnungen bei der nächsten Anmeldung des Benutzers verarbeitet.

## <a name="set-microsoft-edge-as-the-default-browser-on-azure-active-directory-joined-devices"></a>Festlegen von Microsoft Edge als Standardbrowser auf verbundenen Azure Active Directory-Geräten

Um Microsoft Edge Beta als Standardbrowser auf verbundenen Azure Active Directory-Geräten festzulegen, führen Sie die Schritte in der Einstellung [DefaultAssociationsConfiguration](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration) für die Mobile Geräteverwaltung anhand des folgenden Beispiels für eine Anwendungszuordnungsdatei aus.

```xml
<?xml version="1.0" encoding="UTF-8"?>
<DefaultAssociations>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier=".html"/>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier=".htm"/>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier="http"/>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier="https"/>  
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgePDF" Identifier=".pdf"/>
</DefaultAssociations>
```

> [!NOTE]
> Wenn Sie Microsoft Edge Beta als Standardbrowser festlegen möchten, legen Sie **ApplicationName** auf „Microsoft Edge Beta” und **ProgId** auf „MSEdgeBHTML” fest. Wenn Sie Microsoft Edge Dev als Standardbrowser festlegen möchten, legen Sie **ApplicationName** auf „Microsoft Edge Dev” und **ProgId** auf „MSEdgeDHTML” fest.

## <a name="set-microsoft-edge-as-the-default-browser-on-macos"></a>Festlegen von Microsoft Edge als Standardbrowser unter macOS

Wenn Sie versuchen, den Standardbrowser programmgesteuert unter macOS festzulegen, wird eine Eingabeaufforderung für den Endbenutzer angezeigt. Diese Eingabeaufforderung ist ein macOS-Sicherheitsfunktion, das nur mithilfe eines AppleScripts automatisiert werden kann.

Aufgrund dieser Einschränkung gibt es zwei Hauptmethoden zum Festlegen von Microsoft Edge als Standardbrowser unter macOS. Die erste Methode besteht darin, das Gerät mit einem Image von macOS zu flashen, auf dem Microsoft Edge bereits als Standardbrowser festgelegt wurde. Die zweite Methode ist die Verwendung der Richtlinie [Microsoft Edge als Standardbrowser festlegen](./microsoft-edge-policies.md#defaultbrowsersettingenabled) , die den Benutzer auffordert, Microsoft Edge als Standardbrowser festzulegen.

Bei Verwendung dieser Methoden können Benutzer den Standardbrowser weiterhin ändern. Dies liegt daran, dass die Standardbrowsereinstellung aus Sicherheitsgründen nicht programmgesteuert gesperrt werden kann. Aus diesem Grund empfiehlt es sich, die Richtlinie **Microsoft Edge als Standardbrowser festlegen** bereitzustellen, auch wenn Sie ein Image mit Microsoft Edge als Standardbrowser erstellen. Wenn die Richtlinie festgelegt ist und ein Benutzer den Standardbrowser von Microsoft Edge ändert, wenn er Microsoft Edge das nächste Mal öffnet, wird er aufgefordert, ihn als Standardbrowser festzulegen.

## <a name="see-also"></a>Weitere Informationen

- [Planen Ihrer Bereitstellung von Microsoft Edge](./deploy-edge-plan-deployment.md)
- [Angebotsseite für Microsoft Edge für Unternehmen](https://aka.ms/EdgeEnterprise)
- [Festlegen von Microsoft Edge als Standardbrowser (Windows 7 und macOS)](./microsoft-edge-policies.md#defaultbrowsersettingenabled)
- [Windows10 – Wie konfiguriert man Dateizuordnungen für IT-Profis?](/archive/blogs/windowsinternals/windows-10-how-to-configure-file-associations-for-it-pros)
- [Exportieren und Importieren von Standardanwendungszuordnungen](/windows-hardware/manufacture/desktop/export-or-import-default-application-associations)
  - [DISM-Übersicht](/windows-hardware/manufacture/desktop/what-is-dism)
  - [Abbildverwaltung für die Bereitstellung (DISM)](/windows-hardware/manufacture/desktop/dism---deployment-image-servicing-and-management-technical-reference-for-windows)