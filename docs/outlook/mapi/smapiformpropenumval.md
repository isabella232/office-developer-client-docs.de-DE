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
ms.openlocfilehash: bae750e7e940bc1417b3d225c9c81129e9da77b4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795577"
---
# <a name="smapiformpropenumval"></a>SMAPIFormPropEnumVal

  
  
**Betrifft**: Outlook 
  
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

