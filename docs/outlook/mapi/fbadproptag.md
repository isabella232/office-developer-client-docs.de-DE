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
ms.openlocfilehash: 943dab0141581adc32c184b0042a063a4ec05c3e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582882"
---
# <a name="fbadproptag"></a>FBadPropTag

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
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

