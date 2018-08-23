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
ms.openlocfilehash: 59e9cf23aed2a389384318468c3853cd41c9ec1e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585682"
---
# <a name="mtsid"></a>MTSID

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
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

## <a name="members"></a>Elemente

 **cb**
  
> Anzahl der Bytes im Array vom **AbEntry** Member beschrieben. 
    
 **abEntry**
  
> Byte-Array, das MTS Eintrags-ID-Daten enthält.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die Struktur **MTSID** wird nur für x. 400-Zuordnungen der MAPI-Eintragsbezeichner verwendet. Es entspricht der MAPI- [FLATENTRY](flatentry.md) -Struktur. 
  
Ein Bezeichner MTS hat das gleiche Format wie ein MAPI-Eintrags-ID oder eine binäre Eigenschaft-Wert. MTS-IDs können für das Abbrechen Zurückgestellte Nachrichten besonders nützlich sein. 
  
## <a name="see-also"></a>Siehe auch



[FLATENTRY](flatentry.md)
  
[FLATMTSIDLIST](flatmtsidlist.md)


[MAPI-Strukturen](mapi-structures.md)

