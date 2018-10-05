---
title: PidTagConversationKey (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 52c97d6c-7f4b-4522-aeac-0c1ed8475952
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 00c65dae9bc29fe9cdb310b819ba99d6d46ebfe3
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389764"
---
# <a name="pidtagconversationkey-canonical-property"></a>PidTagConversationKey (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Unterhaltung Schlüssel in Microsoft Outlook verwendet nur, wenn **IPM suchen. Nachrichten-Managers** Nachrichten wie die Nachricht, Downloadverlauf für ein Konto Post Office Protocol (POP3) enthält. Diese Eigenschaft ist in Microsoft Exchange Server veraltet. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_CONVERSATION_KEY  <br/> |
|Kennung:  <br/> |0x000b  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Allgemeine messaging  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn Sie e-Mail-Nachrichten als Unterhaltungen und Konvertieren von Nachrichteneigenschaften in [Transport-Neutral Encapsulation Format (TNEF)](transport-neutral-encapsulation-format-tnef.md)zugreifen möchten, verwenden Sie diese Eigenschaft nicht. Verwenden Sie stattdessen die kanonischen Eigenschaften [PidTagConversationIndex](pidtagconversationindex-canonical-property.md) und [Eigenschaftpidtagconversationtopic](pidtagconversationtopic-canonical-property.md) . 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Spezifikationen von Microsoft Exchange Server-Protokoll.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Operationen, die für Objekte, die e-Mail-Nachricht zulässig sind.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Codiert und decodiert Nachrichten- und Objekte, die auf eine effiziente Streamdarstellung.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[IPM-Teilstruktur](ipm-subtree.md)
  
[MAPI-Spezialordner](mapi-special-folders.md)
  
[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

