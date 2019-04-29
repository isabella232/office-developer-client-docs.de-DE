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
  
Enthält ein Array von Property-Tags. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
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
  
> Die Anzahl der Eigenschaftstags im vom **aulPropTag** -Element angegebenen Array. 
    
 **aulPropTag**
  
> Array von Property-Tags.
    
## <a name="remarks"></a>Bemerkungen

Ein Property-Tag ist eine 32-Bit-Ganzzahl ohne Vorzeichen, die aus zwei Teilen besteht: 
  
- Ein Bezeichner in den hochwertigen 16 Bits.
    
- Ein Typ in den niederwertigen 16 Bits.
    
Der Bezeichner ist ein numerischer Wert in einem bestimmten Zeitraum. MAPI definiert Bereiche für Bezeichner, um zu beschreiben, wofür die Eigenschaft verwendet wird und wer für deren Verwaltung zuständig ist. MAPI definiert Einschränkungen für die einzelnen Eigenschaftentags, die in der Headerdatei Mapitags. h unterstützt werden.
  
Der Typ gibt das Format für den Wert der Eigenschaft an. MAPI definiert Konstanten für alle Eigenschaftentypen, die in der Headerdatei Mapidefs. h unterstützt werden. 
  
Weitere Informationen zu Eigenschaftstags und ihren Komponenten finden Sie in einem der folgenden Themen: 
  
[MAPI-Eigenschafts Tags](mapi-property-tags.md)
  
[Übersicht über die MAPI-EigenschaftsKennung](mapi-property-identifier-overview.md)
  
[Übersicht über die MAPI-EigenschaftsTypen](mapi-property-type-overview.md)
  
Eine vollständige Liste der einwertigen und mehrwertigen Eigenschaftentypen finden Sie im Anhang, [Eigenschaftenbezeichner und-Typen](property-identifiers-and-types.md). 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Strukturen](mapi-structures.md)

