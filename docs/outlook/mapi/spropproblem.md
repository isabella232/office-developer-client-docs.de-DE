---
title: SPropProblem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SPropProblem
api_type:
- COM
ms.assetid: 55943197-fd11-442d-bb4b-0bff565b846e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f8fc822d4b3d11b2b310e511d43da612ffcc32c2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566563"
---
# <a name="spropproblem"></a>SPropProblem

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt einen Fehler, der sich auf einen Vorgang bezieht, der eine Eigenschaft betrifft.
  
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

## <a name="members"></a>Members

 **ulIndex**
  
> Ein Index in einem Array von Eigenschaftentags.
    
 **ulPropTag**
  
> Eigenschaftstag für die Eigenschaft, die den Fehler aufweist.
    
 **scode**
  
> Fehlerwert, der das Problem mit der Eigenschaft beschreibt. Dieser Wert kann ein beliebiger [MAPI-SCODE-Wert](scode.md) sein. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Ein Array von **SPropProblem-Strukturen** wird von den folgenden Methoden zurückgegeben: 
  
- [IMAPISupport::DoCopyTo](imapisupport-docopyto.md)
    
- [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md)
    
- [IMAPIProp::DeleteProps](imapiprop-deleteprops.md)
    
- [IMAPIProp::SetProps](imapiprop-setprops.md)
    
- [IMAPIProp::CopyProps](imapiprop-copyprops.md)
    
- [IMAPIProp::CopyTo](imapiprop-copyto.md)
    
- [IPropData::HrAddObjProps](ipropdata-hraddobjprops.md)
    
Eine **SPropProblem-Struktur** enthält einen **SCODE-Fehlerwert,** der aus einem Vorgang resultiert, der versucht, eine MAPI-Eigenschaft zu ändern oder zu löschen. 
  
Weitere Informationen zur Funktionsweise der **SPropProblem-Struktur** mit Fehlern im Zusammenhang mit Eigenschaften finden Sie unter [MAPI Named Properties](mapi-named-properties.md). 
  
## <a name="see-also"></a>Siehe auch



[SCODE](scode.md)
  
[SPropProblemArray](spropproblemarray.md)


[MAPI-Strukturen](mapi-structures.md)

