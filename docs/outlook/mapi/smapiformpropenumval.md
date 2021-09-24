---
title: SMAPIFormPropEnumVal
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SMAPIFormPropEnumVal
api_type:
- COM
ms.assetid: 694d40e9-cff2-435e-ad90-446044c306d2
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9ea204f2f1cf324b4276563005c2cd90ac53e0c0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59549910"
---
# <a name="smapiformpropenumval"></a>SMAPIFormPropEnumVal

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Karten einen aufgezählten ganzzahligen Wert zu einem Anzeigenamen für diesen Wert. 
  
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

## <a name="members"></a>Members

 **pszDisplayName**
  
> Zeichenfolge, die den Anzeigenamen für den im **nVal-Element** angegebenen Wert enthält. 
    
 **nVal**
  
> Ein Enumerationswert für den Anzeigenamen, auf den der **PszDisplayName-Member** verweist. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Wenn ein Benutzer einen Anzeigenamen aus einem Formular auswählt, wird der entsprechende Enumerationswert des Namens mithilfe der [IMAPIProp-Schnittstellenimplementierungen](imapipropiunknown.md) gespeichert, die dem Formular zugeordnet sind. 
  
## <a name="see-also"></a>Siehe auch



[SMAPIFormProp](smapiformprop.md)
  
[SPropValue](spropvalue.md)


[MAPI-Strukturen](mapi-structures.md)

