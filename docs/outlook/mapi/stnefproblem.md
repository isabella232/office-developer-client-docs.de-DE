---
title: STnefProblem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.STnefProblem
api_type:
- COM
ms.assetid: 3fe651b7-0ddf-42fd-8277-9224505be1a8
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 19d20a3fb06f6a0a0671ba4bfd938da314001778
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336379"
---
# <a name="stnefproblem"></a>STnefProblem

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält Informationen zu einem Problem bei der Eigenschaft oder Attribut Verarbeitung, das bei der Codierung oder Decodierung eines Transport Neutral Encapsulation Format (TNEF)-Streams aufgetreten ist.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |TNEF. h  <br/> |
   
```cpp
typedef struct _STnefProblem
{
  ULONG ulComponent;
  ULONG ulAttribute;
  ULONG ulPropTag;
  SCODE scode;
} STnefProblem;

```

## <a name="members"></a>Elemente

 **ulComponent**
  
> Die Art der Verarbeitung, bei der das Problem aufgetreten ist. Wenn das Problem während der Nachrichtenverarbeitung aufgetreten ist, wird das **ulComponent** -Element auf NULL festgelegt. Wenn das Problem bei der Anlagenverarbeitung aufgetreten ist, wird **ulComponent** auf den Wert **PR_ATTACH_NUM** ([pidtagattachnumber (](pidtagattachnumber-canonical-property.md)) der entsprechenden Anlage festgelegt.
    
 **ulAttribute**
  
> Attribut, das der vom **ulPropTag** -Element angegebenen Eigenschaft zugeordnet ist, oder, wenn beim Decodieren eines Kapselungs Blocks das TNEF-Verarbeitungsproblem auftritt, einer der folgenden Werte: 
    
 _attMAPIProps_
  
> Nachrichtenebene
    
 _attAttachment_
  
> Anlagenebene
    
 **ulPropTag**
  
> Property-Tag der Eigenschaft, die das TNEF-Verarbeitungsproblem verursacht hat, außer wenn das Problem beim Decodieren eines Kapselungs Blocks auftritt, in diesem Fall **ulPropTag** auf NULL festgelegt ist. 
    
 **SCODE**
  
> Fehlerwert, der das während der Verarbeitung auftretende Problem angibt.
    
## <a name="remarks"></a>Bemerkungen

Wenn während der Verarbeitung eines Attributs oder einer Eigenschaft keine **STnefProblem** -Struktur generiert wird, kann die Anwendung weiterhin davon ausgehen, dass die Verarbeitung dieses Attributs oder dieser Eigenschaft erfolgreich war. Die einzige Ausnahme tritt auf, wenn das Problem während der Decodierung eines Kapselungs Blocks auftrat. In diesem Fall wird die Decodierung der Komponente, die dem Block entspricht, angehalten, und die Decodierung wird in einer anderen Komponente fortgesetzt. 
  
## <a name="see-also"></a>Siehe auch



[STnefProblemArray](stnefproblemarray.md)
  
[Kanonische Pidtagattachnumber (-Eigenschaft](pidtagattachnumber-canonical-property.md)


[MAPI-Strukturen](mapi-structures.md)

