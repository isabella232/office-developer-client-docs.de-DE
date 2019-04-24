---
title: Kanonische PidTagConversationIndex-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagConversationIndex
api_type:
- HeaderDef
ms.assetid: c65cdda7-9515-4da9-be75-43ebf45a02df
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: c6fa0d8f1323e8562a78080f50dbf448b8019ec2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334720"
---
# <a name="pidtagconversationindex-canonical-property"></a>Kanonische PidTagConversationIndex-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen Binary-Wert, der die relative Position dieser Nachricht in einem konversationsthread angibt. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_CONVERSATION_INDEX  <br/> |
|Kennung:  <br/> |0x0071  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Allgemeine Nachrichtenübermittlung  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Ein konversationsthread stellt eine Reihe von Nachrichten und Antworten dar. Diese Eigenschaft wird normalerweise mit verketteten Zeitstempelwerten implementiert. Die Verwendung ist optional, auch wenn **PR_CONVERSATION_TOPIC** ([eigenschaftpidtagconversationtopic](pidtagconversationtopic-canonical-property.md)) festgelegt ist. 
  
MAPI stellt die [ScCreateConversationIndex](sccreateconversationindex.md) -Funktion zum Erstellen oder Aktualisieren eines Unterhaltungsindex bereit. Die Funktion verwendet den aktuellen Indexwert als Gezähltes Bytearray und gibt den Indexwert mit einem Zeitstempel zurück, der am Ende verkettet ist. Eine Nachricht, die eine Antwort auf eine andere Nachricht darstellt, sollte **ScCreateConversationIndex** verwenden, um diese Eigenschaft zu aktualisieren. 
  
Ein Nachrichtenspeicher Anbieter kann sicherstellen, dass **PR_CONVERSATION_INDEX** immer für eingehende oder ausgehende Nachrichten festgelegt ist. Dies kann durch Aufrufen von **ScCreateConversationIndex**, entweder mit dem vorhandenen Wert, wenn diese Eigenschaft festgelegt ist, oder mit NULL, wenn dies nicht der Fall ist. Diese Aktion sollte vor dem Aufruf von [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) ausgeführt werden. 
  
Alle Nachrichten, die den gleichen Wert für **PR_CONVERSATION_TOPIC** haben, können nach dieser Eigenschaft sortiert werden, um die hierarchische Beziehung der Nachrichten aufzudecken. 
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für e-Mail-Nachrichtenobjekte zulässig sind.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

