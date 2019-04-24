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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7cba5dce60ce15ddb12776d619143849298aac9f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357477"
---
# <a name="smapiverbarray"></a>SMAPIVerbArray

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält ein Array von [SMAPIVerb](smapiverb.md) -Strukturen, die MAPI-Verben beschreiben. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiform. h  <br/> |
|Zugehöriges Makro:  <br/> |[CbMAPIVerbArray](cbmapiverbarray.md) <br/> |
   
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
    
## <a name="remarks"></a>Bemerkungen

Die **SMAPIVerbArray** -Struktur wird als Parameter in der [IMAPIFormInfo:: CalcVerbSet](imapiforminfo-calcverbset.md) -Methode übergeben. 
  
## <a name="see-also"></a>Siehe auch



[SMAPIVerb](smapiverb.md)


[MAPI-Strukturen](mapi-structures.md)

