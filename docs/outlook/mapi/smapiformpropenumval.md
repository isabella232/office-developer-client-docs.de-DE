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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 353bc574ca5987d71faf4841744de30a3d6c3f19
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309492"
---
# <a name="smapiformpropenumval"></a>SMAPIFormPropEnumVal

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ordnet einen aufgezählten ganzzahligen Wert einem Anzeigenamen für diesen Wert zu. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiform. h  <br/> |
   
```cpp
typedef struct _SMAPIFormPropEnumVal
{
  LPSTR pszDisplayName;
  ULONG nVal;
} SMAPIFormPropEnumVal;

```

## <a name="members"></a>Elemente

 **pszDisplayName**
  
> Zeichenfolge, die den Anzeigenamen für den im **NVAL** -Element angegebenen Wert enthält. 
    
 **nVal**
  
> Ein Enumerationswert für den Anzeigenamen, auf den vom **pszDisplayName** -Element verwiesen wird. 
    
## <a name="remarks"></a>Bemerkungen

Wenn ein Benutzer einen Anzeigenamen aus einem Formular auswählt, wird der entsprechende Enumerationswert des Namens mithilfe der [IMAPIProp](imapipropiunknown.md) -Schnittstellenimplementierung gespeichert, die dem Formular zugeordnet ist. 
  
## <a name="see-also"></a>Siehe auch



[SMAPIFormProp](smapiformprop.md)
  
[SPropValue](spropvalue.md)


[MAPI-Strukturen](mapi-structures.md)

