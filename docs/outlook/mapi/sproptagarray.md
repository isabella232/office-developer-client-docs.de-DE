---
title: SPropTagArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropTagArray
api_type:
- COM
ms.assetid: 4a9e1579-bebe-4a51-8ced-6dba9c3bcb63
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 5cfad1c75aaab9afae47de5798f9e6b7ea530940
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795609"
---
# <a name="sproptagarray"></a>SPropTagArray

  
  
**Betrifft**: Outlook 
  
Enthält ein Array von Eigenschaftentags. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Makros:  <br/> |[CbNewSPropTagArray](cbnewsproptagarray.md), [CbSPropTagArray](cbsproptagarray.md), [SizedSPropTagArray](sizedsproptagarray.md) <br/> |
   
```cpp
typedef struct _SPropTagArray
{
  ULONG cValues;
  ULONG aulPropTag[MAPI_DIM];
} SPropTagArray, FAR *LPSPropTagArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Anzahl der Eigenschaftentags im Array vom **AulPropTag** Member angegeben. 
    
 **aulPropTag**
  
> Array von Eigenschaftentags.
    
## <a name="remarks"></a>Hinweise

Ein Eigenschaftentag ist eine 32-Bit-Ganzzahl ohne Vorzeichen, die besteht aus zwei Teilen: 
  
- Ein Bezeichner in der hohen 16 Bits.
    
- Ein Typ in den niederwertige 16 Bit.
    
Der Bezeichner ist einen numerischen Wert in einem bestimmten Bereich. MAPI definiert Bereiche für Bezeichner zum Beschreiben der für die-Eigenschaft verwendet wird und die, die für die Verwaltung zuständig ist. MAPI definiert Einschränkungen für jede Eigenschaft Tags, die sie in der Headerdatei Mapitags.h unterstützt.
  
Der Typ gibt das Format für den Wert der Eigenschaft. MAPI definiert Konstanten für jede Eigenschaftentypen, die in der Headerdatei Mapidefs.h unterstützt. 
  
Weitere Informationen zu Eigenschaftentags und deren Komponenten finden Sie in den folgenden Themen: 
  
[MAPI-Eigenschaftentags](mapi-property-tags.md)
  
[Übersicht über die Bezeichner des MAPI-Eigenschaft](mapi-property-identifier-overview.md)
  
[Übersicht über Typ von MAPI-Eigenschaft](mapi-property-type-overview.md)
  
Eine vollständige Liste der Eigenschaftentypen einwertige und mehrwertige finden Sie im Anhang, [Eigenschaftenbezeichner und Typen](property-identifiers-and-types.md). 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Strukturen](mapi-structures.md)

