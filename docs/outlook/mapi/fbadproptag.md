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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9764be2788db8d2649be8708cad4ec67a85af845
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433647"
---
# <a name="fbadproptag"></a>FBadPropTag

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Überprüft ein angegebenes Eigenschaftstag. 
  
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
  
> [in] Das zu überprüfende Eigenschaftstag.
    
## <a name="return-value"></a>Rückgabewert

TRUE 
  
> Das angegebene Eigenschaftstag ist kein gültiges MAPI-Eigenschaftstag. 
    
FALSE 
  
> Das angegebene Eigenschaftstag ist ein gültiges MAPI-Eigenschaftstag.
    
## <a name="remarks"></a>Hinweise

Die **FBadPropTag-Funktion** überprüft das angegebene Eigenschaftstag basierend auf MAPI-Definitionen. Es wird sichergestellt, dass der Eigenschaftentyp einer der von MAPI definierten Typen ist und dass der Eigenschaftenbezeichner für diesen Typ definiert ist. 
  
## <a name="see-also"></a>Siehe auch



[FBadProp](fbadprop.md)

