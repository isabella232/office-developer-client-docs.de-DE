---
title: FBadProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- FBadProp
api_type:
- HeaderDef
ms.assetid: 929330c8-e6f2-4adf-a36e-fba18fa055d4
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2274fa324425bfc3e04ec5a6a45ff1270cbfbca8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621150"
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

