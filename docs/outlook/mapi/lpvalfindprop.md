---
title: LpValFindProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 67461a38-bb60-467b-901b-39c645e764f7
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c4a201411e2232a3e5fdcd97dcbc9460f657b12a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578094"
---
# <a name="lpvalfindprop"></a>LpValFindProp

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
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
  
## <a name="remarks"></a>HinwBemerkungeneise

Die **LpValFindProp** -Funktion ist identisch mit **PpropFindProp**.
  
## <a name="see-also"></a>Siehe auch



[PpropFindProp](ppropfindprop.md)
  
[SPropValue](spropvalue.md)

