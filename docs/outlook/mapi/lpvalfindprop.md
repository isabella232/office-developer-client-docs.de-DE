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
ms.openlocfilehash: fa1588d4a58824b57c132fc8e66a0abd6e9acd0a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357428"
---
# <a name="lpvalfindprop"></a>LpValFindProp

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Sucht nach einer angegebenen Eigenschaft in einem Eigenschaftensatz.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |mapiutil. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen und Dienstanbieter.  <br/> |
   
```cpp
LPSPropValue LpValFindProp(
  ULONG ulPropTag,
  ULONG cValues,
  LPSPropValue lpPropArray
);
```

## <a name="parameters"></a>Parameter

 _ulPropTag_
  
> in -Tag für die Eigenschaft, nach der im Eigenschaftensatz gesucht werden soll, angegeben durch den _lpPropArray_ -Parameter. 
    
 _cValues_
  
> in Die Anzahl der Eigenschaften im Eigenschaftensatz, angegeben durch den _lpPropArray_ -Parameter. 
    
 _lpPropArray_
  
> in Array von **SPropValue** -Strukturen, die die zu durchsuchenden Eigenschaften definieren. 
    
## <a name="return-value"></a>Rückgabewert

Die **LpValFindProp** -Funktion gibt eine **SPropValue** -Struktur zurück, die die Eigenschaft definiert, die mit dem Eingabe Eigenschafts übereinstimmt, oder NULL, wenn keine Übereinstimmung vorliegt. 
  
## <a name="remarks"></a>Bemerkungen

Die **LpValFindProp** -Funktion ist identisch mit **PpropFindProp**.
  
## <a name="see-also"></a>Siehe auch



[PpropFindProp](ppropfindprop.md)
  
[SPropValue](spropvalue.md)

