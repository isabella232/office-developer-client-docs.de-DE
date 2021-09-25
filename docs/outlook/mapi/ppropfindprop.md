---
title: PpropFindProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PpropFindProp
api_type:
- HeaderDef
ms.assetid: f23dd6f4-915b-4fe8-ab3f-6d625c7d6061
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 29a06ebfec45acecbc938611c50c4939e3a52286
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578893"
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
  
> [in] Anzahl der Eigenschaften im Eigenschaftensatz, die durch den  _rgprop-Parameter_ angegeben werden. 
    
 _ulPropTag_
  
> [in] Eigenschaftstag für die Eigenschaft, nach der gesucht werden soll, in dem durch den  _rgprop-Parameter_ angegebenen Eigenschaftensatz. 
    
## <a name="return-value"></a>Rückgabewert

 **PpropFindProp** gibt eine [SPropValue-Struktur](spropvalue.md) zurück, die die Eigenschaft definiert, die dem Eingabeeigenschaftstag entspricht, oder NULL, wenn keine Übereinstimmung vorhanden ist. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Wenn das angegebene Eigenschaftstag eine Eigenschaft vom Typ PT_UNSPECIFIED angibt, findet die **PpropFindProp-Funktion** eine Übereinstimmung nur für den Eigenschaftsbezeichner im Tag. Andernfalls wird eine Übereinstimmung für das gesamte Eigenschaftentag einschließlich des Eigenschaftstyps gefunden und die identifizierte Eigenschaft zurückgegeben. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::BuildDataItem  <br/> |MFCMAPI verwendet die **PpropFindProp-Methode,** um Eigenschaften in einem Eigenschaftensatz zu suchen, der der Liste hinzugefügt wird.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

