---
title: PidTagContentCount (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagContentCount
api_type:
- HeaderDef
ms.assetid: 27c75031-a968-4636-98a6-4a5b7422f57c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 69c5ab6da80ae4f1e32dfe215338d0eb0872a499
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616537"
---
# <a name="pidtagcontentcount-canonical-property"></a>PidTagContentCount (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die Anzahl der Nachrichten in einem Ordner, wie vom Nachrichtenspeicher berechnet.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_CONTENT_COUNT  <br/> |
|Kennung:  <br/> |0x3602  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Ordner  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese vom Nachrichtenspeicher berechnete Eigenschaft wird für zwei verschiedene, jedoch verwandte Zwecke verwendet. In einem MapiFolder-Objekt enthält es die Anzahl der Nachrichten in einem Ordner. In einer Überschriftenzeile in kategorisierten MAPI-Tabellen enthält sie die Anzahl nicht zugeordneter Nachrichten in der Kategorie, die dieser Überschriftenzeile entspricht.
  
Die in dieser Eigenschaft enthaltene Zahl enthält keine zugeordneten Einträge im Ordner. **PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md)) enthält die Anzahl der ungelesenen Nachrichten für den Ordner. Eine Clientanwendung kann diese Eigenschaft lesen, aber nicht ändern und **PR_CONTENT_UNREAD**. 
  
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

