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
ms.openlocfilehash: bd9bfe4d1411b84a7811235aa68728afaefe64ab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439219"
---
# <a name="flatmtsidlist"></a>FLATMTSIDLIST

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält ein Array von [MTSID](mtsid.md) -Strukturen, die jeweils eine MTS-Eintrags-ID (X. 400-Nachrichtentransportsystem) enthalten. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
|Verwandte Makros:  <br/> |[CbFLATMTSIDLIST](cbflatmtsidlist.md), [CbNewFLATMTSIDLIST](cbnewflatmtsidlist.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cMTSIDs;
  ULONG cbMTSIDs;
  BYTE abMTSIDs[MAPI_DIM];
} FLATMTSIDLIST, FAR *LPFLATMTSIDLIST;

```

## <a name="members"></a>Members

 **cMTSIDs**
  
> Die Anzahl der **MTSID** -Strukturen in dem vom **abMTSIDs** -Element beschriebenen Array. 
    
 **cbMTSIDs**
  
> Die Anzahl der Bytes im von **abMTSIDs**beschriebenen Array.
    
 **abMTSIDs**
  
> Bytearray, das eine oder mehrere **MTSID** -Strukturen enthält. 
    
## <a name="remarks"></a>Bemerkungen

Die Verwendung der **FLATMTSIDLIST** -Struktur in X. 400-Messaging entspricht der Verwendung der [FLATENTRYLIST](flatentrylist.md) -Struktur in MAPI-Messaging. MAPI verwendet **FLATMTSIDLIST** -Strukturen, um X. 400-Eigenschaften während der Nachrichtenverarbeitung zu verwalten. Dienstanbieter verwenden **FLATMTSIDLIST** -Strukturen, wenn Sie eingehende und ausgehende X. 400-Nachrichten verarbeiten. 
  
Im **abMTSIDs** -Array wird jede **MTSID** -Struktur an einer natürlich ausgerichteten Grenze ausgerichtet. Zusätzliche Bytes sind als Padding enthalten, um eine natürliche Ausrichtung zwischen zwei **MTSID** -Strukturen sicherzustellen. Die erste **MTSID** -Struktur im Array wird immer korrekt ausgerichtet, da der Offset des **abMTSIDs** -Elements 8 ist. Um den Offset der nächsten Struktur zu berechnen, verwenden Sie die Größe des ersten Eintrags, aufgerundet auf das nächste Vielfache von 4. Verwenden Sie das [CbNewMTSID](cbnewmtsid.md) -Makro, um die Größe einer **MTSID** -Struktur zu berechnen. 
  
## <a name="see-also"></a>Siehe auch



[CbNewFLATMTSIDLIST](cbnewflatmtsidlist.md)
  
[FLATENTRYLIST](flatentrylist.md)
  
[MTSID](mtsid.md)


[MAPI-Strukturen](mapi-structures.md)

