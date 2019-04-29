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
  
Enthält eine MTS-Eintrags-ID (X. 400-Nachrichtentransportsystem). 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
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
  
> Die Anzahl der Bytes im vom **abEntry** -Element beschriebenen Array. 
    
 **abEntry**
  
> Bytearray, das die MTS-Eintrags-ID-Daten enthält.
    
## <a name="remarks"></a>Bemerkungen

Die **MTSID** -Struktur wird nur für X. 400-ZUORDNUNGEN von MAPI-Eintrags Bezeichnern verwendet. Es entspricht der MAPI- [FLATENTRY](flatentry.md) -Struktur. 
  
Ein MTS-Bezeichner hat das gleiche Format wie eine MAPI-Eintrags-ID oder einen binären Eigenschaftswert. MTS-IDs können besonders nützlich sein, wenn verzögerte Nachrichten abgebrochen werden. 
  
## <a name="see-also"></a>Siehe auch



[FLATENTRY](flatentry.md)
  
[FLATMTSIDLIST](flatmtsidlist.md)


[MAPI-Strukturen](mapi-structures.md)

