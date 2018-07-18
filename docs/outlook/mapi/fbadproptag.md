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
ms.openlocfilehash: d1503aaa5bddd23a90035219901e1dc232dbd026
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791662"
---
# <a name="fbadproptag"></a>FBadPropTag

  
  
**Betrifft**: Outlook 
  
Überprüft ein Tag für die angegebene Eigenschaft. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapival.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Dienstanbieter  <br/> |
   
```cpp
ULONG FBadPropTag(
  ULONG ulPropTag
);
```

## <a name="parameters"></a>Parameter

 _ulPropTag_
  
> [in] Die Eigenschaftentag überprüft werden soll.
    
## <a name="return-value"></a>R�ckgabewert

TRUE 
  
> Das Tag für die angegebene Eigenschaft ist kein gültiges Tag der MAPI-Eigenschaft. 
    
FALSE 
  
> Das Tag für die angegebene Eigenschaft ist ein gültiges Tag der MAPI-Eigenschaft.
    
## <a name="remarks"></a>Bemerkungen

Die Funktion **FBadPropTag** überprüft das angegebene Eigenschaftstag basierend auf MAPI-Definitionen. Sures, die von der Eigenschaftstyp ist eine der Typen, die durch MAPI und die Bezeichner der wird definiert, um dieses Typs werden, erleichtern. 
  
## <a name="see-also"></a>Siehe auch



[FBadProp](fbadprop.md)

