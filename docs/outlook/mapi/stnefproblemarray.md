---
title: STnefProblemArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.STnefProblemArray
api_type:
- COM
ms.assetid: 115d845b-4168-4d49-b880-219ee28baa9a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 924ddbc7c2ad1ed84ce6927ae089b6eb223bfb92
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563506"
---
# <a name="stnefproblemarray"></a>STnefProblemArray

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Enthält ein Array von **STnefProblem** -Strukturen, die eine oder mehrere Verarbeitung von Problemen, die bei der Codierung aufgetreten oder Decodierung eines Streams Transport Neutral Encapsulation Format (TNEF) beschreiben. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |TNEF.h  <br/> |
   
```cpp
typedef struct _STnefProblemArray
{
  ULONG cProblem;
  STnefProblem aProblem[MAPI_DIM];
}STnefProblemArray, FAR * LPSTnefProblemArray

```

## <a name="members"></a>Elemente

 **cProblem**
  
> Anzahl der Elemente im Array im **aProblem** -Member angegeben. 
    
 **aProblem**
  
> Array von Strukturen [STnefProblem](stnefproblem.md) . Jede Struktur enthält Informationen zu einer Eigenschaft oder ein Problem bei der Verarbeitung. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Wenn Attribut oder Eigenschaft Verarbeitung ein Problem auftritt, wird ein Output-Parameter in der [ITnef::ExtractProps](itnef-extractprops.md) -Methode und in der [ITnef::Finish](itnef-finish.md) -Methode jedes einen Zeiger auf eine **STnefProblemArray** Struktur und **ExtractProps **und der Wert MAPI_W_ERRORS_RETURNED **Ende** jeder zurückgegeben. Dieser Fehlerwert gibt an, dass ein Problem aufgetreten, während der Verarbeitung ist und eine **STnefProblemArray** -Struktur generiert wurde. 
  
Wenn eine Struktur **STnefProblem** während der Verarbeitung eines Attribut oder Eigenschaft nicht generiert wird, kann die Client-Anwendung unter der Annahme weiterhin, die die Verarbeitung dieses Attribut oder Eigenschaft erfolgreich waren. Die einzige Ausnahme tritt auf, wenn das Problem aufgetreten ist, während der Decodierung eines Blocks Kapselung. Wenn der Fehler aufgetreten ist, während diese Decodierung, kann als die [SCODE](scode.md) in der Struktur MAPI_E_UNABLE_TO_COMPLETE zurückgegeben werden. In diesem Fall die Decodierung der die entsprechende Komponente für den Block wird angehalten und der Decodierung in einer anderen Komponente fortgesetzt wird. 
  
## <a name="see-also"></a>Siehe auch



[STnefProblem](stnefproblem.md)
  
[SCODE](scode.md)


[MAPI-Strukturen](mapi-structures.md)

