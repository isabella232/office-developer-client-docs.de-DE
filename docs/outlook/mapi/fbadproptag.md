---
title: FBadPropTag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadPropTag
api_type:
- HeaderDef
ms.assetid: 143bd3c6-5a55-4122-8522-9c48473aa781
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 9764be2788db8d2649be8708cad4ec67a85af845
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340999"
---
# <a name="fbadproptag"></a>FBadPropTag

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Überprüft ein angegebenes Property-Tag. 
  
|||
|:-----|:-----|
|Headerdatei:  <br/> |Mapival.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Dienstanbieter  <br/> |
   
```cpp
ULONG FBadPropTag(
  ULONG ulPropTag
);
```

## <a name="parameters"></a>Parameter

 _ulPropTag_
  
> in Das zu überprüfende Property-Tag.
    
## <a name="return-value"></a>Rückgabewert

TRUE 
  
> Das angegebene Property-Tag ist kein gültiges MAPI-Eigenschafts. 
    
FALSE 
  
> Das angegebene Property-Tag ist ein gültiges MAPI-Eigenschafts.
    
## <a name="remarks"></a>Bemerkungen

Die **FBadPropTag** -Funktion überprüft das angegebene Property-Tag basierend auf MAPI-Definitionen. Sie stellen sicher, dass der Eigenschaftentyp einer der von MAPI definierten Typen ist und dass der Eigenschaftenbezeichner für diesen Typ definiert ist. 
  
## <a name="see-also"></a>Siehe auch



[FBadProp](fbadprop.md)

