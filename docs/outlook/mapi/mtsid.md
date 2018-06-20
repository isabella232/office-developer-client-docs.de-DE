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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: e42bbf23ea8cf4e6196017a962329366e168420d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793288"
---
# <a name="mtsid"></a>MTSID

  
  
**Betrifft**: Outlook 
  
Enthält einen Eintrag Bezeichner für x. 400-Nachricht Transport System (MTS). 
  
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
  
> Anzahl der Bytes im Array vom **AbEntry** Member beschrieben. 
    
 **abEntry**
  
> Byte-Array, das MTS Eintrags-ID-Daten enthält.
    
## <a name="remarks"></a>Hinweise

Die Struktur **MTSID** wird nur für x. 400-Zuordnungen der MAPI-Eintragsbezeichner verwendet. Es entspricht der MAPI- [FLATENTRY](flatentry.md) -Struktur. 
  
Ein Bezeichner MTS hat das gleiche Format wie ein MAPI-Eintrags-ID oder eine binäre Eigenschaft-Wert. MTS-IDs können für das Abbrechen Zurückgestellte Nachrichten besonders nützlich sein. 
  
## <a name="see-also"></a>Siehe auch



[FLATENTRY](flatentry.md)
  
[FLATMTSIDLIST](flatmtsidlist.md)


[MAPI-Strukturen](mapi-structures.md)

