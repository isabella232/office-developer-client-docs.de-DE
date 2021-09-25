---
title: FLATMTSIDLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.FLATMTSIDLIST
api_type:
- COM
ms.assetid: b66c2815-72bc-4535-b34c-899bb830f29e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 207978d840272b52ce13422cae9172dd7045cbf7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576275"
---
# <a name="flatmtsidlist"></a>FLATMTSIDLIST

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält ein Array von [MTSID-Strukturen,](mtsid.md) die jeweils einen MTS-Eintragsbezeichner (X.400 Message Transport System) enthalten. 
  
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

## <a name="members"></a>Members

 **cMTSIDs**
  
> Anzahl der **MTSID-Strukturen** im Array, das vom **abMTSIDs-Element** beschrieben wird. 
    
 **cbMTSIDs**
  
> Anzahl der Bytes im durch **abMTSIDs** beschriebenen Array.
    
 **abMTSIDs**
  
> Bytearray, das eine oder mehrere **MTSID-Strukturen** enthält. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Die Verwendung der **FLATMTSIDLIST-Struktur** in X.400-Messaging entspricht der Verwendung der [FLATENTRYLIST-Struktur](flatentrylist.md) in MAPI-Messaging. MAPI verwendet **FLATMTSIDLIST-Strukturen,** um X.400-Eigenschaften während der Nachrichtenverarbeitung beizubehalten. Dienstanbieter verwenden **FLATMTSIDLIST-Strukturen** bei der Verarbeitung von eingehenden und ausgehenden X.400-Nachrichten. 
  
Im **abMTSIDs-Array** wird jede **MTSID-Struktur** an einer natürlich ausgerichteten Grenze ausgerichtet. Zusätzliche Bytes sind als Abstand enthalten, um die natürliche Ausrichtung zwischen zwei **MTSID-Strukturen** sicherzustellen. Die erste **MTSID-Struktur** im Array wird immer korrekt ausgerichtet, da der Offset des **abMTSIDs-Elements** 8 ist. Um den Offset der nächsten Struktur zu berechnen, verwenden Sie die Größe des ersten Eintrags, der auf das nächste Vielfache von 4 aufgerundet wird. Verwenden Sie das [CbNewMTSID-Makro,](cbnewmtsid.md) um die Größe einer **MTSID-Struktur** zu berechnen. 
  
## <a name="see-also"></a>Siehe auch



[CbNewFLATMTSIDLIST](cbnewflatmtsidlist.md)
  
[FLATENTRYLIST](flatentrylist.md)
  
[MTSID](mtsid.md)


[MAPI-Strukturen](mapi-structures.md)

