---
title: FLATMTSIDLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FLATMTSIDLIST
api_type:
- COM
ms.assetid: b66c2815-72bc-4535-b34c-899bb830f29e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0f1495549df751c59ab84e2b16fffbaf2f4f9fa5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574720"
---
# <a name="flatmtsidlist"></a>FLATMTSIDLIST

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Enthält ein Array von [MTSID](mtsid.md) -Strukturen, von denen jedes einen x. 400-Nachricht Transport System (MTS) Eintrag Bezeichner enthält. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Makros:  <br/> |[CbFLATMTSIDLIST](cbflatmtsidlist.md), [CbNewFLATMTSIDLIST](cbnewflatmtsidlist.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cMTSIDs;
  ULONG cbMTSIDs;
  BYTE abMTSIDs[MAPI_DIM];
} FLATMTSIDLIST, FAR *LPFLATMTSIDLIST;

```

## <a name="members"></a>Elemente

 **cMTSIDs**
  
> Anzahl der **MTSID** Strukturen in das Array von **AbMTSIDs** -Elements beschrieben. 
    
 **cbMTSIDs**
  
> Die Anzahl von Bytes im Array von **AbMTSIDs**beschrieben.
    
 **abMTSIDs**
  
> Bytearray, das eine oder mehrere **MTSID** Strukturen enthält. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **FLATMTSIDLIST** Struktur Verwendung in x. 400-messaging entspricht der [FLATENTRYLIST](flatentrylist.md) -Struktur Verwendung in MAPI messaging. MAPI verwendet **FLATMTSIDLIST** Strukturen zum Verwalten von x. 400-Eigenschaften während der Verarbeitung der Nachricht. Dienstanbieter verwenden **FLATMTSIDLIST** Strukturen beim Verarbeiten von eingehender und ausgehender x. 400-Nachrichten. 
  
Im Array **AbMTSIDs** wird jede **MTSID** Struktur auf einer vertrauten ausgerichtete Grenze ausgerichtet. Zusätzliche Bytes sind als Abstand, stellen Sie sicher, dass natürlichen Ausrichtung alle zweier **MTSID** Strukturen enthalten. Die erste **MTSID** Struktur im Array ist immer ordnungsgemäß ausgerichtet werden, da der Versatz des Elements **AbMTSIDs** 8 ist. Berechnen Sie den Offset der nächsten Struktur, verwenden Sie die Größe des ersten Eintrags aufgerundet auf das nächste Vielfache von 4. Verwenden Sie das Makro [CbNewMTSID](cbnewmtsid.md) , um die Größe einer **MTSID** -Struktur zu berechnen. 
  
## <a name="see-also"></a>Siehe auch



[CbNewFLATMTSIDLIST](cbnewflatmtsidlist.md)
  
[FLATENTRYLIST](flatentrylist.md)
  
[MTSID](mtsid.md)


[MAPI-Strukturen](mapi-structures.md)

