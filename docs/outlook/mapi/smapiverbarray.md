---
title: SMAPIVerbArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SMAPIVerbArray
api_type:
- COM
ms.assetid: 8736f75c-3e95-42dd-9bc1-2f0bd23c4a02
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: fe3bcec6e8e0c3148314bf97a8597e784c45aefe
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609454"
---
# <a name="smapiverbarray"></a>SMAPIVerbArray

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält ein Array von [SMAPIVerb-Strukturen,](smapiverb.md) die MAPI-Verben beschreiben. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiform.h  <br/> |
|Verwandtes Makro:  <br/> |[CbMAPIVerbArray](cbmapiverbarray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cMAPIVerb;
  SMAPIVerb aMAPIVerb[MAPI_DIM];
} SMAPIVerbArray, FAR * LPMAPIVERBARRAY;

```

## <a name="members"></a>Members

 **Cforms**
  
> Anzahl der Verben im Array.
    
 **aFormInfo**
  
> Array von MAPI-Verben.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **SMAPIVerbArray-Struktur** wird als Parameter in der [IMAPIFormInfo::CalcVerbSet-Methode](imapiforminfo-calcverbset.md) übergeben. 
  
## <a name="see-also"></a>Siehe auch



[SMAPIVerb](smapiverb.md)


[MAPI-Strukturen](mapi-structures.md)

