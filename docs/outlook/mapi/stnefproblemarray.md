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
ms.openlocfilehash: 721b14f101e87299f654507f94d4a957f905cac1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434263"
---
# <a name="stnefproblemarray"></a>STnefProblemArray

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält ein Array von **STnefProblem-Strukturen,** die ein oder mehrere Verarbeitungsprobleme beschreiben, die während der Codierung oder Decodierung eines TNEF-Datenstroms (Transport Neutral Encapsulation Format) aufgetreten sind. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Tnef.h  <br/> |
   
```cpp
typedef struct _STnefProblemArray
{
  ULONG cProblem;
  STnefProblem aProblem[MAPI_DIM];
}STnefProblemArray, FAR * LPSTnefProblemArray

```

## <a name="members"></a>Elemente

 **cProblem**
  
> Anzahl der Elemente im Array, das im **aProblem-Element angegeben** ist. 
    
 **aProblem**
  
> Array von [STnefProblem-Strukturen.](stnefproblem.md) Jede Struktur enthält Informationen zu einem Eigenschafts- oder Attributverarbeitungsproblem. 
    
## <a name="remarks"></a>Hinweise

Wenn während der Attribut- oder Eigenschaftenverarbeitung ein Problem auftritt, erhalten ein Ausgabeparameter in der [ITnef::ExtractProps-Methode](itnef-extractprops.md) und in der [ITnef::Finish-Methode](itnef-finish.md) jeweils einen Zeiger auf eine **STnefProblemArray-Struktur** und **ExtractProps** und **Finish** geben jeweils den Wert MAPI_W_ERRORS_RETURNED. Dieser Fehlerwert gibt an, dass während der Verarbeitung ein Problem aufgetreten ist und eine **STnefProblemArray-Struktur** generiert wurde. 
  
Wenn während der Verarbeitung eines Attributs oder einer Eigenschaft keine **STnefProblem-Struktur** generiert wird, kann die Clientanwendung unter der Annahme fortfahren, dass die Verarbeitung dieses Attributs oder dieser Eigenschaft erfolgreich war. Die einzige Ausnahme tritt auf, wenn das Problem während der Decodierung eines Kapselungsblocks auftstand. Wenn der Fehler während dieser Decodierung aufgetreten ist, MAPI_E_UNABLE_TO_COMPLETE als [SCODE](scode.md) in der Struktur zurückgegeben werden. In diesem Fall wird die Decodierung der Komponente, die dem Block entspricht, beendet, und die Decodierung wird in einer anderen Komponente fortgesetzt. 
  
## <a name="see-also"></a>Siehe auch



[STnefProblem](stnefproblem.md)
  
[SCODE](scode.md)


[MAPI-Strukturen](mapi-structures.md)

