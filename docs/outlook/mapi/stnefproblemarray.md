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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 721b14f101e87299f654507f94d4a957f905cac1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336498"
---
# <a name="stnefproblemarray"></a>STnefProblemArray

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält ein Array von **STnefProblem** -Strukturen, die ein oder mehrere Verarbeitungsprobleme beschreiben, die während der Codierung oder deCodierung eines Transport Neutral Encapsulation Format (TNEF)-Streams aufgetreten sind. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |TNEF. h  <br/> |
   
```cpp
typedef struct _STnefProblemArray
{
  ULONG cProblem;
  STnefProblem aProblem[MAPI_DIM];
}STnefProblemArray, FAR * LPSTnefProblemArray

```

## <a name="members"></a>Elemente

 **cProblem**
  
> Die Anzahl der Elemente im Array, die im **aProblem** -Element angegeben sind. 
    
 **aProblem**
  
> Array von [STnefProblem](stnefproblem.md) -Strukturen. Jede Struktur enthält Informationen zu einem Problem mit Eigenschaft oder Attribut Verarbeitung. 
    
## <a name="remarks"></a>Bemerkungen

Wenn ein Problem während der Attribut-oder Eigenschaften Verarbeitung auftritt, erhalten ein Output-Parameter in der [ITnef:: ExtractProps](itnef-extractprops.md) -Methode und in der [ITnef:: Finish](itnef-finish.md) -Methode jeweils einen Zeiger auf eine **STnefProblemArray** -Struktur und **ExtractProps **und **Fertig stellen** Sie den Wert MAPI_W_ERRORS_RETURNED. Dieser Fehlerwert gibt an, dass während der Verarbeitung ein Problem auftrat und eine **STnefProblemArray** -Struktur generiert wurde. 
  
Wenn während der Verarbeitung eines Attributs oder einer Eigenschaft keine **STnefProblem** -Struktur generiert wird, kann die Clientanwendung weiterhin davon ausgehen, dass die Verarbeitung dieses Attributs oder dieser Eigenschaft erfolgreich war. Die einzige Ausnahme tritt auf, wenn das Problem während der Decodierung eines Kapselungs Blocks auftrat. Wenn der Fehler während dieser Decodierung aufgetreten ist, kann MAPI_E_UNABLE_TO_COMPLETE als [SCODE](scode.md) in der Struktur zurückgegeben werden. In diesem Fall wird die Decodierung der Komponente, die dem Block entspricht, angehalten, und die Decodierung wird in einer anderen Komponente fortgesetzt. 
  
## <a name="see-also"></a>Siehe auch



[STnefProblem](stnefproblem.md)
  
[SCODE](scode.md)


[MAPI-Strukturen](mapi-structures.md)

