---
title: Unterstützen von Formatierten Textnachrichten Store Verantwortlichkeiten
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a97993c2-52e4-4b71-ac03-2c02d82447d8
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 502ba82279664638c8e7e4ae68f74df74758918d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435516"
---
# <a name="supporting-formatted-text-message-store-responsibilities"></a>Unterstützen von formatierten Text: Nachrichten Store Verantwortlichkeiten

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Nachrichtenspeicheranbieter verwenden die **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))-Eigenschaft, um zu veröffentlichen, ob sie Rich Text Format (RTF), #A0 verarbeiten können und ob sie den formatierten Text in einem komprimierten oder nicht komprimierten Format speichern, wenn sie RTF-lich sind. Nachrichtenspeicheranbieter geben an, dass sie RTF-bewusst sind, indem sie das STORE_RTF_OK-Bit festlegen und den formatierten Text in einem nicht komprimierten Formular speichern, indem sie das STORE_UNCOMPRESSED_RTF festlegen. Nachrichtenspeicheranbieter geben an, dass sie HTML-bewusst sind, indem sie STORE_HTML_OK festlegen.
  
Es ist zwar wichtig, dass ein RTF-bewusster Client auf das STORE_RTF_OK-Bit überprüft, um festzustellen, ob ein Nachrichtenspeicher RTF unterstützt, es ist jedoch nicht erforderlich, dass sich ein Client mit dem Format des formatierten Texts eines RTF-benachrichtigungsspeichers gedankent. 
  
Alle Nachrichtenspeicher müssen Nicht-RTF-bewusste Clients unterstützen. Ein Nicht-RTF-benachrichtigungsspeicher muss die **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md))-Eigenschaft während eines Aufrufs der [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) der Nachricht löschen, wenn ein Client **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) geändert hat, ohne entweder **PR_RTF_IN_SYNC** oder **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) zu aktualisieren. Das **PR_RTF_IN_SYNC** bewirkt, **dass die PR_RTF_COMPRESSED-Eigenschaft** beim nächsten Aufruf von RTFSync von der **PR_BODY-Eigenschaft** neu komputiert [wird.](rtfsync.md) 
  
Die meisten #A0 erhalten keinen Nachrichtentext von Clients. sie muss auf Anforderung berechnet werden. Da diese Berechnung zeitaufwändig und kostspielig ist, sollten Clients nach Möglichkeit **PR_RTF_COMPRESSED** verwenden. Um die **PR_BODY** zu berechnen, muss der Nachrichtenspeicheranbieter die Komprimierung des Inhalts der PR_RTF_COMPRESSED-Eigenschaft und die **Rich-Text-Formatierung** entfernen. Für Clients, die die PR_RTF_COMPRESSED **nicht** unterstützen, muss diese Berechnung für jede Nachricht stattfinden. 
  
Beim Kopieren von Nachrichten laufen Nachrichtenspeicheranbieter, die die **Methoden IMAPISupport::D oCopyProps** oder **IMAPISupport::D oCopyTo** nicht verwenden, das Risiko, eine Nachricht ohne Inhalt zu erstellen, wenn ihre Implementierung die **PR_BODY-Eigenschaft** ausschließt und auf **PR_RTF_COMPRESSED PR_RTF_COMPRESSED**. Es ist möglich, dass die Daten in **der PR_RTF_COMPRESSED** beschädigt sind. Überprüfen Sie vor dem Ausschließen einer dieser Nachrichteninhaltseigenschaften im Kopiervorgang wie folgt auf Beschädigungen: 
  
1. Wenn der Wert der **PR_RTF_COMPRESSED** nicht größer als der komprimierte RTF ist, ist die Eigenschaft beschädigt. 
    
2. Wenn der magische Wert im RTF-Header nicht  _dwMagicCompressedRTF_ oder  _dwMagicUncompressedRTF_ ist, ist die Eigenschaft beschädigt.
    
Nachrichtenspeicheranbieter, die die Supportmethoden verwenden, müssen sich nicht mit der Implementierung einer Überprüfung auf **PR_RTF_COMPRESSED** sorgen. MAPI stellt sicher, dass die entsprechenden Eigenschaften vorhanden sind und gültig sind. 
  
Es gibt drei verschiedene Stufen der #A0 für Nachrichtenspeicheranbieter, die sie implementieren können. MAPI empfiehlt, dass RTF-bewusste Nachrichtenspeicheranbieter ihre Unterstützung auf mittlerer oder höchster Ebene implementieren. Alle RTF-benachrichtigungsspeicheranbieter sorgen  dafür, PR_BODY aus den in **PR_RTF_COMPRESSED** enthaltenen Daten für ausgehende Nachrichten zu generieren und einen Aufruf an **RTFSync** zu senden, um Text und Formatierungen für eingehende Nachrichten zu synchronisieren. 
  
Die Unterschiede zwischen diesen drei Ebenen werden in der folgenden Tabelle beschrieben. 
  
|**Unterstützungsumfang**|**Beschreibung**|
|:-----|:-----|
|Niedrig  <br/> |Der Nachrichtenspeicheranbieter ruft **RTFSync** auf, wenn Änderungen an einer Nachricht gespeichert werden, und extrahiert die Daten für die **PR_BODY-Eigenschaft** aus **PR_RTF_COMPRESSED** anstatt dass Clients sie festlegen müssen. Sowohl **PR_BODY** als **auch PR_RTF_COMPRESSED** werden gespeichert.  <br/> |
|Middle  <br/> |Der Nachrichtenspeicheranbieter speichert nur **die PR_RTF_COMPRESSED-** und **Computereigenschaft,** PR_BODY falls erforderlich.  <br/> |
|Hoch  <br/> |Nachrichtenspeicheranbieter speichert weder **PR_BODY** noch die zusätzlichen RTF-Eigenschaften. **RTFSync wird** aufgerufen, wenn sich der Nachrichtentext geändert hat und die Formatierung unverändert bleibt oder wenn eine neue Nachricht von einem Transportanbieter heruntergeladen wird.  <br/> |
   

