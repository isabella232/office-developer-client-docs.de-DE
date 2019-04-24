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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d899c8af541da231b015f6178eb7bc8f0ffd86e0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341041"
---
# <a name="fbadprop"></a>FBadProp

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Überprüft eine angegebene Eigenschaft. 
  
|||
|:-----|:-----|
|Headerdatei:  <br/> |Mapival.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Dienstanbieter  <br/> |
   
```cpp
ULONG FBadProp(
  LPSPropValue lpprop
);
```

## <a name="parameters"></a>Parameter

 _lpprop_
  
> [in] Eine [SPropValue](spropvalue.md)-Struktur definiert die zu überprüfende Eigenschaft. 
    
## <a name="return-value"></a>Rückgabewert

TRUE 
  
> Die angegebene Eigenschaft ist ungültig. 
    
FALSE 
  
> Die angegebene Eigenschaft ist gültig.
    
## <a name="remarks"></a>Hinweise

Ein Dienstanbieter kann die **FBadProp**-Funktion aus mehreren Gründen aufrufen, z. B. zur Vorbereitung auf einen Aufruf der [IMAPIProp::SetProps](imapiprop-setprops.md)-Methode, die eine Eigenschaft festlegt. **FBadProp** überprüft die angegebene Eigenschaft in Abhängigkeit vom Eigenschaftentyp. Wenn die Eigenschaft beispielsweise „Boolean“ ist, wird durch **FBadProp** sichergestellt, dass der Wert entweder TRUE oder FALSE ist. Wenn die Eigenschaft „binary“ ist, überprüft **FBadProp** Zeiger und Größe und stellt sicher, dass sie korrekt zugeordnet wird. 
  
## <a name="see-also"></a>Siehe auch



[FBadPropTag](fbadproptag.md)

