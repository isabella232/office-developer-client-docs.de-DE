---
title: SMAPIVerbArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIVerbArray
api_type:
- COM
ms.assetid: 8736f75c-3e95-42dd-9bc1-2f0bd23c4a02
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7a2911779e5f9edb8c0bba7c3476a74ce410477c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569463"
---
# <a name="smapiverbarray"></a>SMAPIVerbArray

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Enthält ein Array von [SMAPIVerb](smapiverb.md) -Strukturen, die MAPI-Verben beschreiben. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiform.h  <br/> |
|Verwandte Makro:  <br/> |[CbMAPIVerbArray](cbmapiverbarray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cMAPIVerb;
  SMAPIVerb aMAPIVerb[MAPI_DIM];
} SMAPIVerbArray, FAR * LPMAPIVERBARRAY;

```

## <a name="members"></a>Elemente

 **cForms**
  
> Anzahl der Verben im Array.
    
 **aFormInfo**
  
> Array von MAPI-Verben.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die Struktur **SMAPIVerbArray** wird als Parameter in der [IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md) -Methode übergeben. 
  
## <a name="see-also"></a>Siehe auch



[SMAPIVerb](smapiverb.md)


[MAPI-Strukturen](mapi-structures.md)

