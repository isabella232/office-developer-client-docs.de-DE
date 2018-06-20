---
title: Kanonische PidTagFlagStatus-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFlagStatus
api_type:
- HeaderDef
ms.assetid: b5117360-0939-4535-83fe-3b4a240b5217
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 38df67757082bd12e008e56632ec7e6961ba9d42
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794370"
---
# <a name="pidtagflagstatus-canonical-property"></a>Kanonische PidTagFlagStatus-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Gibt den Status der Kennzeichnung des Message-Objekts.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_FLAG_STATUS  <br/> |
|Bezeichner:  <br/> |0x1090  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Verschiedenes  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft muss auf ein Objekt bezüglich Besprechungen nicht vorhanden, und sollte nicht auf ein Task-Objekt vorhanden sein. Bei Festlegung auf andere Nachrichtenobjekte, muss diese Eigenschaft auf einen der folgenden Werte festgelegt werden:
  
|**Numerischen Wert**|**Name**|**Beschreibung**|
|:-----|:-----|:-----|
|Nicht vorhanden  <br/> |n/v  <br/> |Nicht gekennzeichnet  <br/> |
|0x00000001  <br/> |followupComplete  <br/> |Abgeschlossen gekennzeichnet  <br/> |
|0x00000002  <br/> |followupFlagged  <br/> |Gekennzeichnet  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge im Zusammenhang mit kennzeichnen.
    
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

