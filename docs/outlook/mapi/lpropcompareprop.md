---
title: LPropCompareProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.LPropCompareProp
api_type:
- COM
ms.assetid: f14ad568-fe45-4875-957d-415d39dc6f28
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7417ddeb814cafb954d5ab80a6dae771fd0f7a79
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414613"
---
# <a name="lpropcompareprop"></a>LPropCompareProp

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Vergleicht zwei Eigenschaftswerte, um zu bestimmen, ob sie gleich sind. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
```cpp
LONG LPropCompareProp(
  LPSPropValue lpSPropValueA,
  LPSPropValue lpSPropValueB
);
```

## <a name="parameters"></a>Parameter

 _lpSPropValueA_
  
> [in] Zeiger auf eine [SPropValue-Struktur,](spropvalue.md) die den ersten zu vergleichenden Eigenschaftswert definiert. 
    
 _lpSPropValueB_
  
> [in] Zeiger auf eine **SPropValue-Struktur,** die den zweiten zu vergleichenden Eigenschaftswert definiert. 
    
## <a name="return-value"></a>Rückgabewert

 **LPropCompareProp** gibt einen der folgenden Werte für die meisten Eigenschaftstypen zurück: 
  
- Kleiner als Null, wenn der vom  _lpSPropValueA-Parameter_ angegebene Wert kleiner als der wert ist, der durch den  _lpSPropValueB-Parameter angegeben_ wird. 
    
- Größer als Null, wenn der von  _lpSPropValueA_ angegebene Wert größer als der von  _lpSPropValueB_ angegebene Wert ist.
    
- Null, wenn der von _lpSPropValueA_ angegebene Wert dem von _lpSPropValueB angegebenen Wert entspricht._ 
    
Bei Eigenschaftstypen ohne systeminterne Sortierung, z. B. Boolean- oder Fehlertypen, gibt die **LPropCompareProp-Funktion** einen nicht definierten Wert zurück, wenn die beiden Eigenschaftswerte nicht gleich sind. Dieser undefined-Wert ist ungleich Null und für alle Aufrufe konsistent. 
  
## <a name="remarks"></a>Hinweise

Verwenden Sie **die LPropCompareProp-Funktion** nur, wenn die Typen der beiden zu vergleichenden Eigenschaften identisch sind. 
  
Vor dem Aufrufen **von LPropCompareProp** muss eine Clientanwendung oder ein Dienstanbieter zuerst die Eigenschaften für den Vergleich mit einem Aufruf der [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) abrufen. Wenn ein Client oder Anbieter **LPropCompareProp** aufruft, untersucht die Funktion zunächst die Eigenschaftstags, um sicherzustellen, dass der Vergleich der Eigenschaftswerte gültig ist. Die Funktion vergleicht dann die Eigenschaftswerte und gibt einen entsprechenden Wert zurück. 
  
Wenn die Eigenschaftswerte ungleichmäßig sind, **bestimmt LPropCompareProp,** welcher der größere ist. Die Eigenschaften, **die LPropCompareProp** vergleicht, müssen nicht zum gleichen Objekt gehören. 
  

