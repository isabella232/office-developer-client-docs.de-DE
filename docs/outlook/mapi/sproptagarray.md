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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9a5be98298ab1f9333ac1c223a6ef594e60dd86a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430700"
---
# <a name="sproptagarray"></a>SPropTagArray

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält ein Array von Eigenschaftstags. 
  
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

## <a name="members"></a>Elemente

 **cValues**
  
> Anzahl der Eigenschaftstags im Array, das vom **aulPropTag-Element angegeben** wird. 
    
 **aulPropTag**
  
> Array von Eigenschaftstags.
    
## <a name="remarks"></a>Hinweise

Ein Eigenschaftstag ist eine 32-Bit-Ganzzahl ohne Vorzeichen, die aus zwei Teilen besteht: 
  
- Ein Bezeichner in der hohen Reihenfolge von 16 Bit.
    
- Ein Typ in niedriger Reihenfolge von 16 Bit.
    
Der Bezeichner ist ein numerischer Wert in einem bestimmten Bereich. MAPI definiert Bereiche für Bezeichner, um zu beschreiben, wofür die Eigenschaft verwendet wird und wer für die Verwaltung verantwortlich ist. MAPI definiert Einschränkungen für jedes der Eigenschaftentags, die es in der Mapitags.h-Headerdatei unterstützt.
  
Der Typ gibt das Format für den Wert der Eigenschaft an. MAPI definiert Konstanten für jeden der Eigenschaftentypen, die in der Mapidefs.h-Headerdatei unterstützt werden. 
  
Weitere Informationen zu Eigenschaftstags und deren Komponenten finden Sie in einem der folgenden Themen: 
  
[MAPI-Eigenschaftstags](mapi-property-tags.md)
  
[Übersicht über die MAPI-Eigenschafts-ID](mapi-property-identifier-overview.md)
  
[Übersicht über den MAPI-Eigenschaftstyp](mapi-property-type-overview.md)
  
Eine vollständige Liste der einwertigen und mehrwertigen Eigenschaftentypen finden Sie im Anhang, [Property Identifiers und Types](property-identifiers-and-types.md). 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Strukturen](mapi-structures.md)

