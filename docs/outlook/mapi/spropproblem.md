---
title: SPropProblem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropProblem
api_type:
- COM
ms.assetid: 55943197-fd11-442d-bb4b-0bff565b846e
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: b3a0872c94459fc7c24d13e35adf335ef8012182
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357848"
---
# <a name="spropproblem"></a>SPropProblem

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt einen Fehler, der sich auf einen Vorgang mit einer Eigenschaft bezieht.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _SPropProblem
{
  ULONG ulIndex;
  ULONG ulPropTag;
  SCODE scode;
} SPropProblem, FAR *LPSPropProblem;

```

## <a name="members"></a>Elemente

 **ulIndex**
  
> Ein Index in einem Array von Property-Tags.
    
 **ulPropTag**
  
> Property-Tag für die Eigenschaft mit dem Fehler.
    
 **SCODE**
  
> Fehlerwert, der das Problem mit der Eigenschaft beschreibt. Dieser Wert kann ein beliebiger MAPI- [SCODE](scode.md) -Wert sein. 
    
## <a name="remarks"></a>Bemerkungen

Ein Array von **SPropProblem** -Strukturen wird von den folgenden Methoden zurückgegeben: 
  
- [IMAPISupport::DoCopyTo](imapisupport-docopyto.md)
    
- [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md)
    
- [IMAPIProp::DeleteProps](imapiprop-deleteprops.md)
    
- [IMAPIProp::SetProps](imapiprop-setprops.md)
    
- [IMAPIProp::CopyProps](imapiprop-copyprops.md)
    
- [IMAPIProp::CopyTo](imapiprop-copyto.md)
    
- [IPropData::HrAddObjProps](ipropdata-hraddobjprops.md)
    
Eine **SPropProblem** -Struktur enthält einen **SCODE** -Fehlerwert, der aus einem Vorgang resultiert, der versucht, eine MAPI-Eigenschaft zu ändern oder zu löschen. 
  
Weitere Informationen zur Funktionsweise der **SPropProblem** -Struktur mit Fehlern im Zusammenhang mit Eigenschaften finden Sie unter [MAPI Named Properties](mapi-named-properties.md). 
  
## <a name="see-also"></a>Siehe auch



[SCODE](scode.md)
  
[SPropProblemArray](spropproblemarray.md)


[MAPI-Strukturen](mapi-structures.md)

