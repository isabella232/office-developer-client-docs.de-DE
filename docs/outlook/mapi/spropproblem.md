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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7c19cce33ec351a5627870782ebb4fe509a98be2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573285"
---
# <a name="spropproblem"></a>SPropProblem

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Beschreibt einen Fehler, die einen Vorgang im Zusammenhang mit einer Eigenschaft zuordnen.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
   
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
  
> Ein Index in einem Array von Eigenschaftentags.
    
 **ulPropTag**
  
> Eigenschaftentag für die Eigenschaft, die den Fehler hat.
    
 **SCODE**
  
> Fehlerwert Beschreibung des Problems mit der-Eigenschaft. Dieser Wert kann einen beliebigen MAPI [SCODE](scode.md) -Wert sein. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Ein Array von **SPropProblem** Strukturen wird von folgenden Methoden zurückgegeben: 
  
- [IMAPISupport::DoCopyTo](imapisupport-docopyto.md)
    
- [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md)
    
- [IMAPIProp::DeleteProps](imapiprop-deleteprops.md)
    
- [IMAPIProp::SetProps](imapiprop-setprops.md)
    
- [IMAPIProp::CopyProps](imapiprop-copyprops.md)
    
- [IMAPIProp::CopyTo](imapiprop-copyto.md)
    
- [IPropData::HrAddObjProps](ipropdata-hraddobjprops.md)
    
Eine **SPropProblem** -Struktur enthält einen **SCODE** Fehlerwert, der einen Vorgang versucht, ändern oder Löschen einer MAPI-Eigenschaft ergibt. 
  
Weitere Informationen zur Funktionsweise der **SPropProblem** -Struktur mit Fehlern im Zusammenhang mit Eigenschaften finden Sie unter [MAPI-Eigenschaften mit dem Namen](mapi-named-properties.md). 
  
## <a name="see-also"></a>Siehe auch



[SCODE](scode.md)
  
[SPropProblemArray](spropproblemarray.md)


[MAPI-Strukturen](mapi-structures.md)

