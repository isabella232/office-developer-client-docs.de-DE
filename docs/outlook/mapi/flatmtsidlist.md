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
  
Enthält ein Array von [MTSID-Strukturen,](mtsid.md) von denen jede einen X.400 Message Transport System (MTS)-Eintragsbezeichner enthält. 
  
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
  
> Anzahl der **MTSID-Strukturen** im array, das vom **abMTSIDs-Element beschrieben** wird. 
    
 **cbMTSIDs**
  
> Anzahl der Byte im Array, das von **abMTSIDs beschrieben wird.**
    
 **abMTSIDs**
  
> Bytearray, das eine oder mehrere **MTSID-Strukturen** enthält. 
    
## <a name="remarks"></a>Hinweise

Die **Verwendung der FLATMTSIDLIST-Struktur** in X.400-Messaging entspricht der Verwendung der [FLATENTRYLIST-Struktur](flatentrylist.md) in MAPI-Messaging. MAPI verwendet **FLATMTSIDLIST-Strukturen,** um X.400-Eigenschaften während der Nachrichtenverarbeitung zu verwalten. Dienstanbieter verwenden **FLATMTSIDLIST-Strukturen** beim Behandeln eingehender und ausgehender X.400-Nachrichten. 
  
Im **abMTSIDs-Array** wird jede **MTSID-Struktur** an einer natürlich ausgerichteten Grenze ausgerichtet. Zusätzliche Bytes sind als Abstand enthalten, um die natürliche Ausrichtung zwischen zwei **MTSID-Strukturen sicherzustellen.** Die erste **MTSID-Struktur** im Array wird immer richtig ausgerichtet, da der Offset des **abMTSIDs-Mitglieds** 8 ist. Verwenden Sie zum Berechnen des Offsets der nächsten Struktur die Größe des ersten Eintrags, der auf das nächste Vielfache von 4 aufgerundet wurde. Verwenden Sie [das CbNewMTSID-Makro,](cbnewmtsid.md) um die Größe einer **MTSID-Struktur zu** berechnen. 
  
## <a name="see-also"></a>Siehe auch



[CbNewFLATMTSIDLIST](cbnewflatmtsidlist.md)
  
[FLATENTRYLIST](flatentrylist.md)
  
[MTSID](mtsid.md)


[MAPI-Strukturen](mapi-structures.md)

