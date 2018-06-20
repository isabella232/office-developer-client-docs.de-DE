---
title: LpValFindProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 67461a38-bb60-467b-901b-39c645e764f7
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: d7601eb50818fa6f39384a6b024215fc4917e83a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792904"
---
# <a name="lpvalfindprop"></a>LpValFindProp

  
  
**Betrifft**: Outlook 
  
Sucht nach einer angegebenen Eigenschaft in einer Eigenschaft festlegen.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter.  <br/> |
   
```cpp
LPSPropValue LpValFindProp(
  ULONG ulPropTag,
  ULONG cValues,
  LPSPropValue lpPropArray
);
```

## <a name="parameters"></a>Parameter

 _ulPropTag_
  
> [in] Tag für die Eigenschaft in den durch den _LpPropArray_ -Parameter angegebenen Eigenschaftensatz suchen. 
    
 _cValues_
  
> [in] Anzahl der Eigenschaften in den Eigenschaftensatz durch den Parameter _LpPropArray_ angegeben. 
    
 _lpPropArray_
  
> [in] Ein Array von **SPropValue** -Strukturen, die die Eigenschaften des zu durchsuchenden definiert. 
    
## <a name="return-value"></a>R�ckgabewert

Die **LpValFindProp** -Funktion gibt eine **SPropValue** -Struktur, die die Eigenschaft, die dem input-Eigenschaftentag übereinstimmt definiert, oder NULL, wenn keine Übereinstimmung vorliegt. 
  
## <a name="remarks"></a>Hinweise

Die **LpValFindProp** -Funktion ist identisch mit **PpropFindProp**.
  
## <a name="see-also"></a>Siehe auch



[PpropFindProp](ppropfindprop.md)
  
[SPropValue](spropvalue.md)

