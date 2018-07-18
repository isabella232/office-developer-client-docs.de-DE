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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: b7755f2ec067003e47d358a9736c6d7d96ede267
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795319"
---
# <a name="ppropfindprop"></a>PpropFindProp

  
  
**Betrifft**: Outlook 
  
Sucht nach einer angegebenen Eigenschaft in einer Eigenschaft festlegen.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
```cpp
LPSPropValue PpropFindProp(
  LPSPropValue rgprop,
  ULONG cprop,
  ULONG ulPropTag
);
```

## <a name="parameters"></a>Parameter

 _rgprop_
  
> [in] Array von [SPropValue](spropvalue.md) -Strukturen, die definieren die Eigenschaften, die durchsucht werden soll. 
    
 _cprop_
  
> [in] Anzahl der Eigenschaften in den Eigenschaftensatz, der durch den Parameter _Rgprop_ angegeben. 
    
 _ulPropTag_
  
> [in] Eigenschaftentag für die Eigenschaft in dem durch den _Rgprop_ -Parameter angegebenen Eigenschaftensatz suchen. 
    
## <a name="return-value"></a>R�ckgabewert

 **PpropFindProp** gibt eine [SPropValue](spropvalue.md) -Struktur definieren die Eigenschaft, die dem input-Eigenschaftentag übereinstimmt, oder NULL, wenn keine Übereinstimmung vorliegt. 
  
## <a name="remarks"></a>Bemerkungen

Wenn der angegebene Eigenschaftstag eine Eigenschaft vom Typ PT_UNSPECIFIED gibt an, sucht die **PpropFindProp** -Funktion nur eine Übereinstimmung mit der Bezeichner für die in das Tag an. Andernfalls findet eine Übereinstimmung für das gesamte Eigenschafts-Tag, einschließlich den Eigenschaftentyp und gibt die angegebene Eigenschaft zurück. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::BuildDataItem  <br/> |MFCMAPI (engl.) verwendet die **PpropFindProp** -Methode, um zu finden, dass Eigenschaften in einer Eigenschaft festgelegt, die der Liste hinzugefügt wird.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

