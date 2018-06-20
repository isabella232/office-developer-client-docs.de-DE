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
ms.openlocfilehash: 1767c86cb5390572b95530060f2295034ed35f43
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795595"
---
# <a name="smapiverbarray"></a>SMAPIVerbArray

  
  
**Betrifft**: Outlook 
  
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

## <a name="members"></a>Members

 **cForms**
  
> Anzahl der Verben im Array.
    
 **aFormInfo**
  
> Array von MAPI-Verben.
    
## <a name="remarks"></a>Hinweise

Die Struktur **SMAPIVerbArray** wird als Parameter in der [IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md) -Methode übergeben. 
  
## <a name="see-also"></a>Siehe auch



[SMAPIVerb](smapiverb.md)


[MAPI-Strukturen](mapi-structures.md)

