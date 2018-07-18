---
title: FBadProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadProp
api_type:
- HeaderDef
ms.assetid: 929330c8-e6f2-4adf-a36e-fba18fa055d4
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 39e10e9139036cc86ec93ea24a89b98125ea6e83
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791650"
---
# <a name="fbadprop"></a>FBadProp

  
  
**Betrifft**: Outlook 
  
Eine angegebene Eigenschaft überprüft. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapival.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Dienstanbieter  <br/> |
   
```cpp
ULONG FBadProp(
  LPSPropValue lpprop
);
```

## <a name="parameters"></a>Parameter

 _lpprop_
  
> [in] Eine [SPropValue](spropvalue.md) -Struktur definieren die-Eigenschaft überprüft werden soll. 
    
## <a name="return-value"></a>R�ckgabewert

TRUE 
  
> Die angegebene Eigenschaft ist ungültig. 
    
FALSE 
  
> Die angegebene Eigenschaft ist gültig.
    
## <a name="remarks"></a>Bemerkungen

Ein Dienstanbieter kann für verschiedene Gründe, beispielsweise um einen Anruf an die [IMAPIProp::SetProps](imapiprop-setprops.md) -Methode eine Eigenschaft bei der Vorbereitung die **FBadProp** -Funktion aufrufen. **FBadProp** überprüft die angegebene Eigenschaft je nach den Eigenschaftentyp. Angenommen, wenn die Eigenschaft boolescher Wert ist, **FBadProp** , Sures, dass der Wert TRUE ist oder FALSE. Wenn die Eigenschaft binär ist, **FBadProp** überprüft den Zeiger und die Größe und stellt sicher, dass es korrekt zugeordnet wird. 
  
## <a name="see-also"></a>Siehe auch



[FBadPropTag](fbadproptag.md)

