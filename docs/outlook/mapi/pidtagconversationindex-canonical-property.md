---
title: PidTagConversationIndex (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 77fee834108a603c1cd10e8e47776cc34fd75a2b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584167"
---
# <a name="pidtagconversationindex-canonical-property"></a>PidTagConversationIndex (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Enthält einen binären Wert, der die relative Position dieser Nachricht innerhalb einer Unterhaltungsthreads angibt. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_CONVERSATION_INDEX  <br/> |
|Kennung:  <br/> |0x0071  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Allgemeine messaging  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Eine Unterhaltungsthreads stellt eine Reihe von Nachrichten und Antworten. Diese Eigenschaft wird normalerweise mithilfe von verketteten Zeitstempelwerten implementiert. Die Verwendung ist optional, selbst wenn **PR_CONVERSATION_TOPIC** ([Eigenschaftpidtagconversationtopic](pidtagconversationtopic-canonical-property.md)) festgelegt ist. 
  
MAPI bietet die [ScCreateConversationIndex](sccreateconversationindex.md) -Funktion zum Erstellen oder Aktualisieren eines Unterhaltung Indexes. Die Funktion nimmt den aktuellen Indexwert als Bytearray gezählte und gibt den Indexwert mit einem Zeitstempel verkettet, auf die Seite zurück. Eine Nachricht, die eine Antwort auf eine andere Nachricht darstellen soll **ScCreateConversationIndex** verwenden, um diese Eigenschaft zu aktualisieren. 
  
Eine Nachricht Speicheranbieter hat die Möglichkeit der Sicherstellung, die **PR_CONVERSATION_INDEX** immer für eingehende und ausgehende Nachrichten festgelegt ist. Hierzu können sie **ScCreateConversationIndex**, entweder mit den vorhandenen Wert, wenn diese Eigenschaft festgelegt ist oder mit NULL, falls noch nicht aufrufen. Diese Aktion sollte berücksichtigt werden, bevor [IMAPIProp::SaveChanges](imapiprop-savechanges.md) aufgerufen wird. 
  
Alle Nachrichten, die den gleichen Wert für **PR_CONVERSATION_TOPIC** aufweisen können auf diese Eigenschaft, um die hierarchische Beziehung der Nachrichten anzuzeigen sortiert werden. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Operationen, die für Objekte, die e-Mail-Nachricht zulässig sind.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

