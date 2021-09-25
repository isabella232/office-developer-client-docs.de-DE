---
title: MTSID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.MTSID
api_type:
- COM
ms.assetid: 3d9bc643-332f-4c8e-83e6-ce9b15711945
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 84ffea2a1c5f0cb70cdd49f5aa318921f8a3d044
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59595644"
---
# <a name="mtsid"></a>MTSID

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen X.400 Message Transport System (MTS)-Eintragsbezeichner. 
  
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

## <a name="members"></a>Members

 **cb**
  
> Anzahl der Bytes im Array, das vom **abEntry-Mitglied** beschrieben wird. 
    
 **abEntry**
  
> Bytearray, das die MTS-Eintragsbezeichnerdaten enthält.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **MTSID-Struktur** wird nur für X.400-Zuordnungen von MAPI-Eintragsbezeichnern verwendet. Es entspricht der MAPI [FLATENTRY-Struktur.](flatentry.md) 
  
Ein MTS-Bezeichner hat das gleiche Format wie ein MAPI-Eintragsbezeichner oder ein binärer Eigenschaftswert. MTS-Bezeichner können besonders nützlich sein, um verzögerte Nachrichten abzubrechen. 
  
## <a name="see-also"></a>Siehe auch



[FLATENTRY](flatentry.md)
  
[FLATMTSIDLIST](flatmtsidlist.md)


[MAPI-Strukturen](mapi-structures.md)

