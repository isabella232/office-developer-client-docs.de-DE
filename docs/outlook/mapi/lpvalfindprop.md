---
title: LpValFindProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 67461a38-bb60-467b-901b-39c645e764f7
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 05b8620469b289969bdcc2bb4f15f940d9c767e1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592186"
---
# <a name="lpvalfindprop"></a>LpValFindProp

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Sucht nach einer angegebenen Eigenschaft in einem Eigenschaftensatz.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter.  <br/> |
   
```cpp
LPSPropValue LpValFindProp(
  ULONG ulPropTag,
  ULONG cValues,
  LPSPropValue lpPropArray
);
```

## <a name="parameters"></a>Parameter

 _ulPropTag_
  
> [in] Tag für die Eigenschaft, nach der im Eigenschaftensatz gesucht werden soll, angegeben durch den _LpPropArray-Parameter._ 
    
 _cValues_
  
> [in] Anzahl der Eigenschaften im Eigenschaftensatz, angegeben durch den _LpPropArray-Parameter._ 
    
 _lpPropArray_
  
> [in] Array von **SPropValue-Strukturen,** die die zu durchsuchenden Eigenschaften definieren. 
    
## <a name="return-value"></a>Rückgabewert

Die **LpValFindProp-Funktion** gibt eine **SPropValue-Struktur** zurück, die die Eigenschaft definiert, die dem Eingabeeigenschaftstag entspricht, oder NULL, wenn keine Übereinstimmung vorhanden ist. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Die **LpValFindProp-Funktion** ist identisch mit **PpropFindProp.**
  
## <a name="see-also"></a>Siehe auch



[PpropFindProp](ppropfindprop.md)
  
[SPropValue](spropvalue.md)

