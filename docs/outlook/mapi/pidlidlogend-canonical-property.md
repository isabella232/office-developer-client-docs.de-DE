---
title: PidLidLogEnd (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidLogEnd
api_type:
- COM
ms.assetid: 621459ea-adf5-4420-9f0f-6f31b9b95508
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: ef1c9814aa6d1f81a44883d09ac635a5eed76517
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793658"
---
# <a name="pidlidlogend-canonical-property"></a>PidLidLogEnd (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Stellt das Enddatum und die Uhrzeit für die Journalnachricht.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |dispidLogEnd  <br/> |
|-Eigenschaft festgelegt:  <br/> |PSETID_Log  <br/> |
|Long-ID (Abdeckung):  <br/> |0x00008708  <br/> |
|Datentyp:  <br/> |PT_SYSTIME  <br/> |
|Bereich:  <br/> |Journal  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Der Zeitpunkt, wann die Aktivität in koordinierter Weltzeit The (UTC), beendet der **DispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md))-Eigenschaft gleich und größer als oder gleich **DispidLogStart** ([PidLidLogStart](pidlidlogstart-canonical-property.md))-Eigenschaft sein muss.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Operationen, die für Journale zulässig sind.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

