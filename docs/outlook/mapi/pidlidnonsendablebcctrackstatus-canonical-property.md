---
title: PidLidNonSendableBccTrackStatus (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidNonSendableBccTrackStatus
api_type:
- COM
ms.assetid: daad8735-a3da-4a0b-9329-6eb253c281fd
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2533e5cec51e28238e3b43038600261918fae2d2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600582"
---
# <a name="pidlidnonsendablebcctrackstatus-canonical-property"></a>PidLidNonSendableBccTrackStatus (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Wert für jeden Teilnehmer, der in der **Eigenschaft dispidNonSendableBCC** ([PidLidNonSendableBcc](pidlidnonsendablebcc-canonical-property.md)) aufgeführt ist.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidNonSendBccTrackStatus  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Common  <br/> |
|Long ID (LID):  <br/> |0x00008545  <br/> |
|Datentyp:  <br/> |PT_MV_LONG  <br/> |
|Bereich:  <br/> |Allgemeines Messaging  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft ist nur erforderlich, wenn die **dispidNonSendableBCC-Eigenschaft** festgelegt ist. Die Anzahl der Werte in dieser Eigenschaft muss der Anzahl der Werte in der **dispidNonSendableBCC** entsprechen. Jeder Wert in dieser Eigenschaft entspricht dem Teilnehmer in der **dispidNonSendableBCC-Eigenschaft** am selben Index. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftssatzdefinitionen und Verweise auf verwandte Exchange Server Protokollspezifikationen bereit.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungsanfrage- und Antwortnachrichten an.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

