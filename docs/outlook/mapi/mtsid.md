---
title: MTSID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MTSID
api_type:
- COM
ms.assetid: 3d9bc643-332f-4c8e-83e6-ce9b15711945
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 96da91acec741322e6c07c64555171d35f0f7e00
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435173"
---
# <a name="mtsid"></a>MTSID

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine X.400 Message Transport System (MTS)-Eintrags-ID. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Makros:  <br/> |[CbMTSID](cbmtsid.md), [CbNewMTSID](cbnewmtsid.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE abEntry[MAPI_DIM];
} MTSID, FAR *LPMTSID;

```

## <a name="members"></a>Elemente

 **cb**
  
> Anzahl der Bytes im array, das vom **abEntry-Element beschrieben** wird. 
    
 **abEntry**
  
> Bytearray, das die MTS-Eintrags-ID-Daten enthält.
    
## <a name="remarks"></a>Hinweise

Die **MTSID-Struktur** wird nur für X.400-Zuordnungen von MAPI-Eintragsbezeichnern verwendet. Sie entspricht der MAPI [FLATENTRY-Struktur.](flatentry.md) 
  
Ein MTS-Bezeichner hat das gleiche Format wie ein MAPI-Eintragsbezeichner oder ein binärer Eigenschaftswert. MTS-Bezeichner können besonders nützlich sein, um verzögerte Nachrichten abgesagt zu haben. 
  
## <a name="see-also"></a>Siehe auch



[FLATENTRY](flatentry.md)
  
[FLATMTSIDLIST](flatmtsidlist.md)


[MAPI-Strukturen](mapi-structures.md)

