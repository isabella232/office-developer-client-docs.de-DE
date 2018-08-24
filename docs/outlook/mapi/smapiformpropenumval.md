---
title: SMAPIFormPropEnumVal
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIFormPropEnumVal
api_type:
- COM
ms.assetid: 694d40e9-cff2-435e-ad90-446044c306d2
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2c49a17389a9bfc998f892e0becf96dca4cd773f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578717"
---
# <a name="smapiformpropenumval"></a>SMAPIFormPropEnumVal

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ordnet einen enumerierten ganzzahligen Wert einen Anzeigenamen für diesen Wert. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiform.h  <br/> |
   
```cpp
typedef struct _SMAPIFormPropEnumVal
{
  LPSTR pszDisplayName;
  ULONG nVal;
} SMAPIFormPropEnumVal;

```

## <a name="members"></a>Elemente

 **pszDisplayName**
  
> Zeichenfolge, die den Anzeigenamen für die in das **nVal** -Element angegebenen Wert enthält. 
    
 **nVal**
  
> Ein Enumerationswert für den Anzeigenamen auf den Member **PszDisplayName** zeigt. 
    
## <a name="remarks"></a>Bemerkungen

Wenn ein Benutzer einen Anzeigenamen aus einem Formular auswählt, wird den Namen des entsprechenden-Enumerationswert gespeichert, mithilfe der Implementierung der [IMAPIProp](imapipropiunknown.md) -Schnittstelle, die dem Formular zugeordnet ist. 
  
## <a name="see-also"></a>Siehe auch



[SMAPIFormProp](smapiformprop.md)
  
[SPropValue](spropvalue.md)


[MAPI-Strukturen](mapi-structures.md)

