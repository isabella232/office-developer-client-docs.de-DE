---
title: PidTagContentUnreadCount (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContentUnreadCount
api_type:
- HeaderDef
ms.assetid: 4fe207e9-a77f-46b9-b51d-d989847a9d02
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9572a053182aaa59020a6816736b8a4b92e778b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331871"
---
# <a name="pidtagcontentunreadcount-canonical-property"></a>PidTagContentUnreadCount (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die Anzahl ungelesener Nachrichten in einem Ordner, wie vom Nachrichtenspeicher berechnet. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_CONTENT_UNREAD  <br/> |
|Kennung:  <br/> |0x3603  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Ordner  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese vom Nachrichtenspeicher berechnete Eigenschaft wird für zwei unterschiedliche, wenngleich verwandte Zwecke verwendet. In einem MAPI-Ordnerobjekt enthält es die Anzahl der Nachrichten in einem Ordner. In einer Überschriftenzeile in kategorisierten MAPI-Tabellen enthält sie die Anzahl nicht gelesener nicht zugeordneter Nachrichten in der Kategorie, die dieser Überschriftenzeile entspricht.
  
Diese Eigenschaft enthält die Anzahl der Nachrichten in der Ordnerinhaltstabelle, für die das flag MSGFLAG_READ in der **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) -Eigenschaft nicht festgelegt ist. Die **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md)) -Eigenschaft enthält die Gesamtanzahl der Nachrichten für den Ordner. Die **PR_CONTENT_COUNT** und diese Eigenschaft sind schreibgeschützt für Clients. 
  
Einige Clientanwendungen zeigen die Überschriftenzeile einer Kategorie abhängig vom Wert dieser Eigenschaft unterschiedlich an. Ein Client kann beispielsweise eine Kategorie anzeigen, die ungelesene Nachrichten fett formatiert enthält. Diese Eigenschaft kann nicht als Kategorie verwendet werden, und ein Versuch dazu führt dazu, dass der MAPI_E_INVALID_PARAMETER von der [IMAPITable::SortTable-Methode zurückgegeben](imapitable-sorttable.md) wird. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Microsoft Exchange Server Protokollspezifikationen.
    
[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Verarbeitet Ordnervorgänge.
    
[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)
  
> Enthält zulässige Vorgänge für die Zentralen Tabellenobjekte.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

