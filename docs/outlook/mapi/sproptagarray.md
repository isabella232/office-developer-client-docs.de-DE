---
title: SPropTagArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SPropTagArray
api_type:
- COM
ms.assetid: 4a9e1579-bebe-4a51-8ced-6dba9c3bcb63
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: dd6d8f44b3de487750c28ba5919ab5adda0020b5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566549"
---
# <a name="sproptagarray"></a>SPropTagArray

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
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
  
> Anzahl der Eigenschaftstags im Array, die durch das **aulPropTag-Element** angegeben werden. 
    
 **aulPropTag**
  
> Array von Eigenschaftstags.
    
## <a name="remarks"></a>HinwBemerkungeneise

Ein Eigenschaftstag ist eine 32-Bit-Ganzzahl ohne Vorzeichen, die aus zwei Teilen besteht: 
  
- Ein Bezeichner in der hohen Reihenfolge von 16 Bit.
    
- Ein Typ in der niedrigen Reihenfolge von 16 Bit.
    
Der Bezeichner ist ein numerischer Wert in einem bestimmten Bereich. MAPI definiert Bereiche für Bezeichner, um zu beschreiben, wofür die Eigenschaft verwendet wird und wer für deren Verwaltung zuständig ist. MAPI definiert Einschränkungen für jedes der Eigenschaftstags, die es in der Mapitags.h-Headerdatei unterstützt.
  
Der Typ gibt das Format für den Wert der Eigenschaft an. MAPI definiert Konstanten für jeden der Eigenschaftentypen, die in der Mapidefs.h-Headerdatei unterstützt werden. 
  
Weitere Informationen zu Eigenschaftentags und deren Komponenten finden Sie in einem der folgenden Themen: 
  
[MAPI-Eigenschaftstags](mapi-property-tags.md)
  
[Übersicht über mapi-Eigenschaftsbezeichner](mapi-property-identifier-overview.md)
  
[Übersicht über mapi-Eigenschaftstypen](mapi-property-type-overview.md)
  
Eine vollständige Liste der einwertigen und mehrwertigen Eigenschaftstypen finden Sie im Anhang, [eigenschaftsbezeichner und Typen.](property-identifiers-and-types.md) 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Strukturen](mapi-structures.md)

