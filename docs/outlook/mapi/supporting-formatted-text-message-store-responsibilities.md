---
title: Unterstützen formatierter Store Zuständigkeiten für Textnachrichten
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: a97993c2-52e4-4b71-ac03-2c02d82447d8
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 698a21901030ded8063753638df3501e5dc5cf78
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590996"
---
# <a name="supporting-formatted-text-message-store-responsibilities"></a>Unterstützen von formatiertem Text: Zuständigkeiten für Nachrichten Store

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Nachrichtenspeicheranbieter verwenden die **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) -Eigenschaft, um zu veröffentlichen, ob sie RtF (Rich Text Format), HTML-Text und, wenn sie RTF-fähig sind, ob sie den formatierten Text in einem komprimierten oder unkomprimierten Format speichern können. Nachrichtenspeicheranbieter geben an, dass sie RTF-fähig sind, indem sie das STORE_RTF_OK Bit festlegen und den formatierten Text in einem nicht komprimierten Format speichern, indem sie das STORE_UNCOMPRESSED_RTF Bit festlegen. Nachrichtenspeicheranbieter geben an, dass sie HTML-fähig sind, indem sie das STORE_HTML_OK Bit festlegen.
  
Es ist zwar wichtig, dass ein RTF-fähiger Client nach dem STORE_RTF_OK Bit sucht, um festzustellen, ob ein Nachrichtenspeicher RTF unterstützt, es ist jedoch nicht erforderlich, dass sich ein Client mit dem Format des formatierten Texts eines RTF-fähigen Speichers befasst. 
  
Alle Nachrichtenspeicher müssen Nicht-RTF-fähige Clients unterstützen. Ein nicht RTF-fähiger Nachrichtenspeicher muss die **eigenschaft PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) während eines Aufrufs der [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) der Nachricht löschen, wenn ein Client **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) geändert hat, ohne **PR_RTF_IN_SYNC** oder **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) zu aktualisieren. Das Löschen **PR_RTF_IN_SYNC** bewirkt, dass die **PR_RTF_COMPRESSED-Eigenschaft** beim nächsten Aufruf von [RTFSync](rtfsync.md)von einem RTF-fähigen Client aus der **PR_BODY** Eigenschaft neu kompiliert wird. 
  
Die meisten RTF-fähigen Nachrichtenspeicher erhalten den Nachrichtentext nicht von Clients; sie muss auf Anforderung berechnet werden. Da diese Berechnung zeitaufwändig und kostspielig ist, sollten Clients nach Möglichkeit **PR_RTF_COMPRESSED** verwenden. Um die **PR_BODY** Eigenschaft zu berechnen, muss der Nachrichtenspeicheranbieter die Komprimierung des Inhalts der **PR_RTF_COMPRESSED Eigenschaft** aufheben und die Rich-Text-Formatierung entfernen. Clients, die die **PR_RTF_COMPRESSED-Eigenschaft** nicht unterstützen, erfordern diese Berechnung für jede Nachricht. 
  
Beim Kopieren von Nachrichten laufen Nachrichtenspeicheranbieter, die nicht die Methoden **IMAPISupport::D oCopyProps** oder **IMAPISupport::D oCopyTo** verwenden, das Risiko, dass eine Nachricht ohne Inhalt erstellt wird, wenn ihre Implementierung die **PR_BODY-Eigenschaft** ausschließt und **auf PR_RTF_COMPRESSED** basiert. Es ist möglich, dass die Daten in der **PR_RTF_COMPRESSED-Eigenschaft** beschädigt sind. Bevor Sie eine dieser Nachrichteninhaltseigenschaften im Kopiervorgang ausschließen, überprüfen Sie wie folgt auf Beschädigung: 
  
1. Wenn der Wert von **PR_RTF_COMPRESSED** nicht größer als der komprimierte RTF ist, ist die Eigenschaft beschädigt. 
    
2. Wenn der Größenwert im RTF-Header nicht  _"mvMagicCompressedRTF"_ oder  _"wetterMagicUncompressedRTF"_ lautet, ist die Eigenschaft beschädigt.
    
Nachrichtenspeicheranbieter, die die Supportmethoden verwenden, müssen sich nicht darum kümmern, eine Überprüfung **auf PR_RTF_COMPRESSED** Beschädigung zu implementieren. MAPI stellt sicher, dass die entsprechenden Eigenschaften vorhanden und gültig sind. 
  
Es gibt drei verschiedene Ebenen der RTF-Unterstützung, die Nachrichtenspeicheranbieter implementieren können. MAPI empfiehlt, dass RTF-fähige Nachrichtenspeicheranbieter ihre Unterstützung auf der mittleren oder höchsten Ebene implementieren. Alle RTF-fähigen Nachrichtenspeicheranbieter generieren **PR_BODY** aus den Daten, die in **PR_RTF_COMPRESSED** für ausgehende Nachrichten enthalten sind, und rufen **RTFSync** auf, um Text und Formatierung für eingehende Nachrichten zu synchronisieren. 
  
Die Unterschiede zwischen diesen drei Ebenen werden in der folgenden Tabelle beschrieben. 
  
|**Unterstützungsumfang**|**Beschreibung**|
|:-----|:-----|
|Niedrig  <br/> |Der Nachrichtenspeicheranbieter ruft **RTFSync** immer dann auf, wenn Änderungen an einer Nachricht gespeichert werden, und extrahiert die Daten für die **PR_BODY-Eigenschaft** aus **PR_RTF_COMPRESSED,** anstatt sie von Clients festzulegen. **Sowohl PR_BODY** als **auch PR_RTF_COMPRESSED** werden gespeichert.  <br/> |
|Mitte  <br/> |Der Nachrichtenspeicheranbieter speichert nur die **PR_RTF_COMPRESSED** Eigenschaft, wobei bei Bedarf **PR_BODY** werden.  <br/> |
|Hoch  <br/> |Der Nachrichtenspeicheranbieter speichert weder **PR_BODY** noch die zusätzlichen RTF-Eigenschaften. **RTFSync** wird aufgerufen, wenn sich der Nachrichtentext geändert hat und die Formatierung unverändert bleibt oder wenn eine neue Nachricht von einem Transportanbieter heruntergeladen wird.  <br/> |
   

