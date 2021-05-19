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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334699"
---
# <a name="pidtagconversationkey-canonical-property"></a>PidTagConversationKey (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den unterhaltungsschlüssel, der in Microsoft Outlook beim Suchen von **IPM verwendet wird. MessageManager-Nachrichten,** z. B. die Nachricht, die den Downloadverlauf für ein Post Office Protocol (POP3)-Konto enthält. Diese Eigenschaft ist in diesem Microsoft Exchange Server. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_CONVERSATION_KEY  <br/> |
|Kennung:  <br/> |0x000B  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Allgemeines Messaging  <br/> |
   
## <a name="remarks"></a>Hinweise

Verwenden Sie diese Eigenschaft nicht, wenn Sie auf E-Mail-Nachrichten als Unterhaltungen zugreifen und Nachrichteneigenschaften in [TNEF (Transport-Neutral Encapsulation Format)](transport-neutral-encapsulation-format-tnef.md)konvertieren. verwenden Sie stattdessen [die kanonischen Eigenschaften PidTagConversationIndex](pidtagconversationindex-canonical-property.md) und [PidTagConversationTopic.](pidtagconversationtopic-canonical-property.md) 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Microsoft Exchange Server Protokollspezifikationen.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Codiert und decodiert Nachrichten- und Anlagenobjekte in eine effiziente Streamdarstellung.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[IPM-Unterstruktur](ipm-subtree.md)
  
[MAPI-Sonderordner](mapi-special-folders.md)
  
[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

