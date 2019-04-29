---
title: Unterstützung für formatierte Text Nachrichtenspeicher zuStändigkeiten
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
# <a name="supporting-formatted-text-message-store-responsibilities"></a>Unterstützung von formatiertem Text: Aufgaben des Nachrichtenspeichers

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Nachrichtenspeicher Anbieter verwenden die **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))-Eigenschaft, um zu veröffentlichen, ob Sie Rich-Text-Format (RTF), HTML-Text und, falls Sie RTF-fähig sind, behandeln können, unabhängig davon, ob Sie den formatierten Text in einem komprimiertes oder nicht komprimiertes Format. Nachrichtenspeicher Anbieter weisen darauf hin, dass Sie RTF-fähig sind, indem Sie das STORE_RTF_OK-Bit festlegen und den formatierten Text in einem unkomprimierten Format speichern, indem Sie das STORE_UNCOMPRESSED_RTF-Bit festlegen. Nachrichtenspeicher Anbieter geben an, dass Sie HTML-fähig sind, indem Sie das STORE_HTML_OK-Bit festlegen.
  
Es ist zwar wichtig, dass ein RTF-fähiger Client überprüft, ob das STORE_RTF_OK-Bit feststellt, dass ein Nachrichtenspeicher RTF unterstützt, aber es ist nicht erforderlich, dass sich ein Client mit dem Format des formatierten Texts in einem RTF-fähigen Speicher befasst. 
  
Alle Nachrichtenspeicher müssen nicht-RTF-fähige Clients unterstützen. Ein nicht-RTF-fähiger Nachrichtenspeicher muss die **PR_RTF_IN_SYNC** ([pidtagrtfinsync (](pidtagrtfinsync-canonical-property.md))-Eigenschaft während eines Aufrufs der [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode der Nachricht löschen, wenn ein Client **PR_BODY** ([pidtagbody (](pidtagbody-canonical-property.md)) ohne Aktualisieren von **PR_RTF_IN_SYNC** oder **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). Durch das Löschen von **PR_RTF_IN_SYNC** wird die **PR_RTF_COMPRESSED** -Eigenschaft aus der **PR_BODY** -Eigenschaft neu berechnet, wenn ein RTF-fähiger Client [RTFSync](rtfsync.md)aufruft. 
  
Die meisten RTF-fähigen Nachrichtenspeicher erhalten den Nachrichtentext nicht von Clients; Sie muss auf Anforderung berechnet werden. Da diese Berechnung zeitaufwändig und kostspielig ist, sollten Clients **PR_RTF_COMPRESSED** nach Möglichkeit verwenden. Zum Berechnen der **PR_BODY** -Eigenschaft muss der Nachrichtenspeicher Anbieter die Komprimierung der Inhalte der **PR_RTF_COMPRESSED** -Eigenschaft aufheben und die Rich-Text-Formatierung entfernen. Clients, die die **PR_RTF_COMPRESSED** -Eigenschaft nicht unterstützen, müssen diese Berechnung für jede Nachricht durchführen. 
  
Beim Kopieren von Nachrichten laufen Nachrichtenspeicher Anbieter, die nicht die **IMAPISupport::D ocopyprops** oder **IMAPISupport::D ocopyto** -Methoden verwenden, Gefahr, eine Nachricht ohne Inhalt zu erstellen, wenn Ihre Implementierung die **PR_BODY** -Eigenschaft und basiert auf **PR_RTF_COMPRESSED**. Die Daten in der **PR_RTF_COMPRESSED** -Eigenschaft können beschädigt werden. Bevor Sie eine dieser Nachrichteninhalts Eigenschaften in den Kopiervorgang ausschließen, überprüfen Sie die folgenden Fehler: 
  
1. Wenn der Wert von **PR_RTF_COMPRESSED** nicht größer als der komprimierte RTF ist, ist die Eigenschaft beschädigt. 
    
2. Wenn der Magic-Wert in der RTF-Kopfzeile nicht _dwMagicCompressedRTF_ oder _dwMagicUncompressedRTF_ist, ist die Eigenschaft beschädigt.
    
Nachrichtenspeicher Anbieter, die die Supportmethoden verwenden, müssen sich nicht um die Implementierung einer Überprüfung auf **PR_RTF_COMPRESSED** -Beschädigung kümmern. MAPI stellt sicher, dass die entsprechenden Eigenschaften vorhanden und gültig sind. 
  
Es gibt drei verschiedene Ebenen der RTF-Unterstützung, die von Nachrichtenspeicher Anbietern implementiert werden können. MAPI empfiehlt, dass RTF-fähige Nachrichtenspeicher Anbieter ihre Unterstützung auf mittlerer oder höchster Ebene implementieren. Alle RTF-fähigen Nachrichtenspeicher Anbieter kümmern sich um das Generieren von **PR_BODY** aus den Daten, die in **PR_RTF_COMPRESSED** bei ausgehenden Nachrichten enthalten sind, und rufen Sie **RTFSync** auf, um Text und Formatierungen für eingehende Nachrichten zu synchronisieren. 
  
Die Unterschiede zwischen diesen drei Ebenen werden in der folgenden Tabelle beschrieben. 
  
|**Unterstützungsumfang**|**Beschreibung**|
|:-----|:-----|
|Niedrig  <br/> |Der Nachrichtenspeicher Anbieter ruft **RTFSync** auf, wenn Änderungen in einer Nachricht gespeichert werden, und extrahiert die Daten für die **PR_BODY** -Eigenschaft aus **PR_RTF_COMPRESSED** , statt sie von Clients zu verlangen. Sowohl **PR_BODY** als auch **PR_RTF_COMPRESSED** werden gespeichert.  <br/> |
|Mittleren  <br/> |Der Nachrichtenspeicher Anbieter speichert nur die **PR_RTF_COMPRESSED** -Eigenschaft, wobei **PR_BODY** bei Bedarf berechnet wird.  <br/> |
|Hoch  <br/> |Der Nachrichtenspeicher Anbieter speichert weder **PR_BODY** noch die zusätzlichen RTF-Eigenschaften. **RTFSync** wird aufgerufen, wenn der Nachrichtentext geändert wurde und die Formatierung unverändert bleibt oder wenn eine neue Nachricht von einem Transportanbieter heruntergeladen wird.  <br/> |
   

