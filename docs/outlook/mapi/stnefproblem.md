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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 19d20a3fb06f6a0a0671ba4bfd938da314001778
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435180"
---
# <a name="stnefproblem"></a>STnefProblem

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält Informationen zu einem Eigenschafts- oder Attributverarbeitungsproblem, das während der Codierung oder Decodierung eines Transport Neutral Encapsulation Format (TNEF)-Datenstroms aufgetreten ist.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Tnef.h  <br/> |
   
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
  
> Die Art der Verarbeitung, während der das Problem aufgetreten ist. Wenn das Problem während der Nachrichtenverarbeitung aufgetreten ist, wird **das ulComponent-Element** auf Null festgelegt. Wenn das Problem während der Anlagenverarbeitung aufgetreten ist, wird **ulComponent** auf den wert **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) der entsprechenden Anlage festgelegt.
    
 **ulAttribute**
  
> Attribut, das der eigenschaft zugeordnet ist, die durch das **ulPropTag-Element** angegeben wird, oder, wenn das TNEF-Verarbeitungsproblem beim Decodieren eines Kapselungsblocks auftritt, einen der folgenden Werte: 
    
 _attMAPIProps_
  
> Nachrichtenebene
    
 _attAttachment_
  
> Anlagenebene
    
 **ulPropTag**
  
> Eigenschaftstag der Eigenschaft, die das TNEF-Verarbeitungsproblem verursacht hat, außer wenn das Problem beim Decodieren eines Kapselungsblocks auftritt, in diesem Fall **ist ulPropTag** auf Null festgelegt. 
    
 **scode**
  
> Fehlerwert, der das Während der Verarbeitung aufgetretene Problem angibt.
    
## <a name="remarks"></a>Hinweise

Wenn während der Verarbeitung eines Attributs oder einer Eigenschaft keine **STnefProblem-Struktur** generiert wird, kann die Anwendung unter der Annahme fortfahren, dass die Verarbeitung dieses Attributs oder dieser Eigenschaft erfolgreich war. Die einzige Ausnahme tritt auf, wenn das Problem während der Decodierung eines Kapselungsblocks auftstand. In diesem Fall wird die Decodierung der Komponente, die dem Block entspricht, beendet, und die Decodierung wird in einer anderen Komponente fortgesetzt. 
  
## <a name="see-also"></a>Siehe auch



[STnefProblemArray](stnefproblemarray.md)
  
[PidTagAttachNumber (kanonische Eigenschaft)](pidtagattachnumber-canonical-property.md)


[MAPI-Strukturen](mapi-structures.md)

