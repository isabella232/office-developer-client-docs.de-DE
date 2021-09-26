---
title: STnefProblem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.STnefProblem
api_type:
- COM
ms.assetid: 3fe651b7-0ddf-42fd-8277-9224505be1a8
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8e43586edf3e707201d4a05b7b01160f42e89d4f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591059"
---
# <a name="stnefproblem"></a>STnefProblem

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält Informationen zu einem Problem bei der Eigenschaften- oder Attributverarbeitung, das während der Codierung oder Decodierung eines TNEF-Datenstroms (Transport Neutral Encapsulation Format) aufgetreten ist.
  
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

## <a name="members"></a>Members

 **ulComponent**
  
> Die Art der Verarbeitung, während der das Problem aufgetreten ist. Wenn das Problem während der Nachrichtenverarbeitung aufgetreten ist, wird das **ulComponent-Element** auf Null festgelegt. Wenn das Problem während der Anlagenverarbeitung aufgetreten ist, wird **ulComponent** auf den wert des **entsprechenden PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) festgelegt.
    
 **ulAttribute**
  
> Attribut, das der vom **ulPropTag-Element** angegebenen Eigenschaft zugeordnet ist, oder, wenn das TNEF-Verarbeitungsproblem beim Decodieren eines Kapselungsblocks auftritt, einer der folgenden Werte: 
    
 _attMAPIProps_
  
> Nachrichtenebene
    
 _attAttachment_
  
> Anlagenebene
    
 **ulPropTag**
  
> Eigenschaftstag der Eigenschaft, die das TNEF-Verarbeitungsproblem verursacht hat, außer wenn das Problem beim Decodieren eines Kapselungsblocks auftritt, in diesem Fall wird **ulPropTag** auf Null festgelegt. 
    
 **scode**
  
> Fehlerwert, der das Problem angibt, das während der Verarbeitung aufgetreten ist.
    
## <a name="remarks"></a>HinwBemerkungeneise

Wenn während der Verarbeitung eines Attributs oder einer Eigenschaft keine **STnefProblem-Struktur** generiert wird, kann die Anwendung unter der Annahme fortgesetzt werden, dass die Verarbeitung dieses Attributs oder dieser Eigenschaft erfolgreich war. Die einzige Ausnahme tritt auf, wenn das Problem während der Decodierung eines Kapselungsblocks auftritt. In diesem Fall wird die Decodierung der Komponente, die dem Block entspricht, beendet, und die Decodierung wird in einer anderen Komponente fortgesetzt. 
  
## <a name="see-also"></a>Siehe auch



[STnefProblemArray](stnefproblemarray.md)
  
[PidTagAttachNumber (kanonische Eigenschaft)](pidtagattachnumber-canonical-property.md)


[MAPI-Strukturen](mapi-structures.md)

