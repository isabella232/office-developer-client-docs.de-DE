---
title: PidTagMessageSize (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagMessageSize
api_type:
- HeaderDef
ms.assetid: c67fb54b-8cc7-4fbc-8204-36fcddfa6192
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: edebd29dfc8a6ecbc13c2982a290ece0b02e7fc9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629753"
---
# <a name="pidtagmessagesize-canonical-property"></a>PidTagMessageSize (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die Summe der Größen aller Eigenschaften eines Nachrichtenobjekts in Byte. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_MESSAGE_SIZE  <br/> |
|Kennung:  <br/> |0x0E08  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Allgemeines Messaging  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Es wird empfohlen, diese Eigenschaft durch Nachrichtenobjekte verfügbar zu machen. Die Nachrichtengröße gibt die ungefähre Anzahl von Bytes an, die übertragen werden, wenn die Nachricht von einem Nachrichtenspeicher in einen anderen verschoben wird. Da es sich um die Summe der Größen aller Eigenschaften des Nachrichtenobjekts handelt, ist sie in der Regel erheblich größer als der Nachrichtentext allein. 
  
Die meisten Nachrichtenspeicheranbieter berechnen diese Eigenschaft für Nachrichten, die sie verarbeiten. Einige Nachrichtenspeicheranbieter unterstützen diese Eigenschaft jedoch nicht. In jedem Fall ist diese Eigenschaft erst verfügbar, wenn die [IMAPIProp::SaveChanges-](imapiprop-savechanges.md) oder [IMessage::SubmitMessage-Methode](imessage-submitmessage.md) aufgerufen wurde. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf verwandte Exchange Server Protokollspezifikationen.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Behandelt Nachrichten- und Anlagenobjekte.
    
[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Behandelt Ordnervorgänge.
    
[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)
  
> Gibt zulässige Vorgänge für die zentralen Nachrichtenspeicherobjekte an.
    
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

