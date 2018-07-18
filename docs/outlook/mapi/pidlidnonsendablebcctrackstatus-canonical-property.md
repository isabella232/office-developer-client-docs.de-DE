---
title: PidLidNonSendableBccTrackStatus (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidNonSendableBccTrackStatus
api_type:
- COM
ms.assetid: daad8735-a3da-4a0b-9329-6eb253c281fd
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: da2bd4e87c7076872ccff708983cfbe631b27122
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793671"
---
# <a name="pidlidnonsendablebcctrackstatus-canonical-property"></a>PidLidNonSendableBccTrackStatus (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Enthält den Wert für jeden Teilnehmer, die in der Eigenschaft **DispidNonSendableBCC** ([PidLidNonSendableBcc](pidlidnonsendablebcc-canonical-property.md)) aufgeführt wird.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |dispidNonSendBccTrackStatus  <br/> |
|-Eigenschaft festgelegt:  <br/> |PSETID_Common  <br/> |
|Long-ID (Abdeckung):  <br/> |0x00008545  <br/> |
|Datentyp:  <br/> |PT_MV_LONG  <br/> |
|Bereich:  <br/> |Allgemeine messaging  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ist erforderlich, nur, wenn die **DispidNonSendableBCC** -Eigenschaft festgelegt wird. Die Anzahl von Werten in dieser Eigenschaft muss die Anzahl von Werten in der **DispidNonSendableBCC**entsprechen. Jeder Wert in dieser Eigenschaft entspricht der Teilnehmer in der **DispidNonSendableBCC** -Eigenschaft im selben Index. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

