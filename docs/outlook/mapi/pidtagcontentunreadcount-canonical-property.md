---
title: PidTagContentUnreadCount (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagContentUnreadCount
api_type:
- HeaderDef
ms.assetid: 4fe207e9-a77f-46b9-b51d-d989847a9d02
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 61958cba1b73b98e161979984d97c47c54f38017
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566829"
---
# <a name="pidtagcontentunreadcount-canonical-property"></a>PidTagContentUnreadCount (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die Anzahl der ungelesenen Nachrichten in einem Ordner, wie vom Nachrichtenspeicher berechnet. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_CONTENT_UNREAD  <br/> |
|Kennung:  <br/> |0x3603  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Ordner  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese vom Nachrichtenspeicher berechnete Eigenschaft wird für zwei verschiedene, jedoch verwandte Zwecke verwendet. In einem MAPI-Ordnerobjekt enthält es die Anzahl der Nachrichten in einem Ordner. In einer Überschriftenzeile in kategorisierten MAPI-Tabellen enthält sie die Anzahl ungelesener nicht zugeordneter Nachrichten in der Kategorie, die dieser Überschriftenzeile entspricht.
  
Diese Eigenschaft enthält die Anzahl der Nachrichten in der Ordnerinhaltstabelle, für die das MSGFLAG_READ Flag nicht in der **eigenschaft PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) festgelegt ist. Die **Eigenschaft PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md)) enthält die Gesamtzahl der Nachrichten für den Ordner. Die **PR_CONTENT_COUNT** und diese Eigenschaft sind für Clients schreibgeschützt. 
  
Einige Clientanwendungen zeigen die Überschriftenzeile einer Kategorie je nach Wert dieser Eigenschaft unterschiedlich an. Beispielsweise kann ein Client eine Kategorie anzeigen, die ungelesene Nachrichten fett formatiert enthält. Diese Eigenschaft kann nicht als Kategorie verwendet werden, und ein Versuch dazu führt dazu, dass der MAPI_E_INVALID_PARAMETER Wert von der [IMAPITable::SortTable-Methode](imapitable-sorttable.md) zurückgegeben wird. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf verwandte Microsoft Exchange Server Protokollspezifikationen.
    
[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Behandelt Ordnervorgänge.
    
[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)
  
> Enthält zulässige Vorgänge für die zentralen Tabellenobjekte.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

