---
title: FBadPropTag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- FBadPropTag
api_type:
- HeaderDef
ms.assetid: 143bd3c6-5a55-4122-8522-9c48473aa781
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d1e5bac98f69080a3b534bfa8f96bbe3f5a3e4f8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596470"
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
  
> [in] Das zu überprüfende Eigenschaftentag.
    
## <a name="return-value"></a>Rückgabewert

TRUE 
  
> Das angegebene Eigenschaftstag ist kein gültiges MAPI-Eigenschaftstag. 
    
FALSE 
  
> Das angegebene Eigenschaftstag ist ein gültiges MAPI-Eigenschaftstag.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **FBadPropTag-Funktion** überprüft das angegebene Eigenschaftstag basierend auf MAPI-Definitionen. Es wird sichergestellt, dass der Eigenschaftstyp einer der von mapi definierten Typen ist und dass der Eigenschaftsbezeichner so definiert ist, dass er diesen Typ aufweist. 
  
## <a name="see-also"></a>Siehe auch



[FBadProp](fbadprop.md)

