---
title: PidTagConversationKey (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 52c97d6c-7f4b-4522-aeac-0c1ed8475952
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c6e6825c0e899693d47457dff8d922db67f3adbb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59555454"
---
# <a name="pidtagconversationkey-canonical-property"></a>PidTagConversationKey (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Unterhaltungsschlüssel, der in Microsoft Outlook nur bei der Suche nach IPM verwendet **wird. MessageManager-Nachrichten,** z. B. die Nachricht, die den Downloadverlauf für ein POP3-Konto (Post Office Protocol) enthält. Diese Eigenschaft ist in Microsoft Exchange Server veraltet. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_CONVERSATION_KEY  <br/> |
|Kennung:  <br/> |0x000B  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Allgemeines Messaging  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Verwenden Sie diese Eigenschaft nicht, wenn Sie als Unterhaltungen auf E-Mail-Nachrichten zugreifen und Nachrichteneigenschaften in [das transportneutrale Kapselungsformat (Transport-Neutral Encapsulation Format, TNEF)](transport-neutral-encapsulation-format-tnef.md)konvertieren. Verwenden Sie stattdessen die kanonischen Eigenschaften [PidTagConversationIndex](pidtagconversationindex-canonical-property.md) und [PidTagConversationTopic.](pidtagconversationtopic-canonical-property.md) 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf verwandte Microsoft Exchange Server Protokollspezifikationen.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Codiert und decodiert Nachrichten- und Anlagenobjekte in einer effizienten Datenstromdarstellung.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[IPM-Unterstruktur](ipm-subtree.md)
  
[MAPI-Spezialordner](mapi-special-folders.md)
  
[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

