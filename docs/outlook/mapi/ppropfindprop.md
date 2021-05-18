---
title: PpropFindProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PpropFindProp
api_type:
- HeaderDef
ms.assetid: f23dd6f4-915b-4fe8-ab3f-6d625c7d6061
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 97021128f92af0486af1ba3125c7843eaa357648
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406339"
---
# <a name="ppropfindprop"></a>PpropFindProp

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Sucht nach einer angegebenen Eigenschaft in einem Eigenschaftensatz.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
```cpp
LPSPropValue PpropFindProp(
  LPSPropValue rgprop,
  ULONG cprop,
  ULONG ulPropTag
);
```

## <a name="parameters"></a>Parameter

 _rgprop_
  
> [in] Array von [SPropValue-Strukturen,](spropvalue.md) die die zu durchsuchenden Eigenschaften definieren. 
    
 _cprop_
  
> [in] Anzahl der Eigenschaften im Eigenschaftensatz, der durch den  _rgprop-Parameter angegeben_ wird. 
    
 _ulPropTag_
  
> [in] Eigenschaftstag für die Eigenschaft, nach der im Eigenschaftensatz gesucht werden soll, der durch den  _rgprop-Parameter angegeben_ wird. 
    
## <a name="return-value"></a>Rückgabewert

 **PpropFindProp gibt** eine [SPropValue-Struktur](spropvalue.md) zurück, die die Eigenschaft definiert, die dem Eingabeeigenschaftstag entspricht, oder NULL, wenn keine Übereinstimmung vorkommt. 
  
## <a name="remarks"></a>Hinweise

Wenn das angegebene Eigenschaftstag eine Eigenschaft vom Typ PT_UNSPECIFIED, findet die **PpropFindProp-Funktion** eine Übereinstimmung nur für den Eigenschaftenbezeichner im Tag. Andernfalls findet sie eine Übereinstimmung für das gesamte Eigenschaftstag, einschließlich des Eigenschaftentyps, und gibt die identifizierte Eigenschaft zurück. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::BuildDataItem  <br/> |MFCMAPI verwendet die **PpropFindProp-Methode,** um Eigenschaften in einem Eigenschaftensatz zu finden, der der Liste hinzugefügt wird.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

