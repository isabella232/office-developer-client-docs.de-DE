---
title: LPropCompareProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.LPropCompareProp
api_type:
- COM
ms.assetid: f14ad568-fe45-4875-957d-415d39dc6f28
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b08be76fa214570dcc336431fe227a8629762de6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584185"
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
  
> [in] Zeiger auf eine [SPropValue-Struktur,](spropvalue.md) die den ersten Eigenschaftswert definiert, der verglichen werden soll. 
    
 _lpSPropValueB_
  
> [in] Zeiger auf eine **SPropValue-Struktur,** die den zweiten eigenschaftswert definiert, der verglichen werden soll. 
    
## <a name="return-value"></a>Rückgabewert

 **LPropCompareProp** gibt einen der folgenden Werte für die meisten Eigenschaftstypen zurück: 
  
- Kleiner als Null, wenn der vom  _lpSPropValueA-Parameter_ angegebene Wert kleiner als der vom  _lpSPropValueB-Parameter_ angegebene Wert ist. 
    
- Größer als Null, wenn der durch  _lpSPropValueA_ angegebene Wert größer als der durch  _lpSPropValueB_ angegebene Wert ist.
    
- Null, wenn der durch  _lpSPropValueA_ angegebene Wert dem durch  _lpSPropValueB_ angegebenen Wert entspricht. 
    
Bei Eigenschaftstypen, die keine systeminterne Sortierung haben, z. B. Boolescher Wert oder Fehlertyp, gibt die **LPropCompareProp-Funktion** einen nicht definierten Wert zurück, wenn die beiden Eigenschaftswerte ungleich sind. Dieser nicht definierte Wert ist für alle Aufrufe ungleich Null und konsistent. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Verwenden Sie die **LPropCompareProp-Funktion** nur, wenn die Typen der beiden zu vergleichenden Eigenschaften identisch sind. 
  
Vor dem Aufrufen von **LPropCompareProp** muss eine Clientanwendung oder ein Dienstanbieter zuerst die Eigenschaften zum Vergleich mit einem Aufruf der [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) abrufen. Wenn ein Client oder Anbieter **LPropCompareProp** aufruft, überprüft die Funktion zuerst die Eigenschaftstags, um sicherzustellen, dass der Vergleich der Eigenschaftswerte gültig ist. Die Funktion vergleicht dann die Eigenschaftswerte und gibt einen entsprechenden Wert zurück. 
  
Wenn die Eigenschaftswerte unerreicht sind, bestimmt **LPropCompareProp,** welcher größer ist. Die Eigenschaften, die **LPropCompareProp** vergleicht, müssen nicht zum gleichen Objekt gehören. 
  

