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
  
Vergleicht zwei Eigenschaftswerte, um zu bestimmen, ob Sie gleich sind. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen und Dienstanbieter  <br/> |
   
```cpp
LONG LPropCompareProp(
  LPSPropValue lpSPropValueA,
  LPSPropValue lpSPropValueB
);
```

## <a name="parameters"></a>Parameter

 _lpSPropValueA_
  
> in Zeiger auf eine [SPropValue](spropvalue.md) -Struktur, die den ersten zu vergleichenden Eigenschaftswert definiert. 
    
 _lpSPropValueB_
  
> in Zeiger auf eine **SPropValue** -Struktur, die den zweiten zu vergleichenden Eigenschaftswert definiert. 
    
## <a name="return-value"></a>Rückgabewert

 **LPropCompareProp** gibt für die meisten Eigenschaftstypen einen der folgenden Werte zurück: 
  
- Kleiner als 0 (null), wenn der vom _lpSPropValueA_ -Parameter angegebene Wert kleiner als der durch den _lpSPropValueB_ -Parameter angegebene ist. 
    
- Größer als 0 (null), wenn der von _lpSPropValueA_ angegebene Wert größer ist als der von _lpSPropValueB_.
    
- NULL, wenn der von _lpSPropValueA_ angegebene Wert dem von _lpSPropValueB_angegebenen Wert entspricht. 
    
Bei Eigenschaftentypen, die keine systeminterne Reihenfolge aufweisen, wie boolesche oder Fehlertypen, gibt die **LPropCompareProp** -Funktion einen nicht definierten Wert zurück, wenn die beiden Eigenschaftswerte ungleich sind. Dieser nicht definierte Wert ist ungleich NULL und konsistent für Aufrufe. 
  
## <a name="remarks"></a>Bemerkungen

Verwenden Sie die **LPropCompareProp** -Funktion nur, wenn die Typen der beiden zu vergleichenden Eigenschaften identisch sind. 
  
Vor dem Aufrufen von **LPropCompareProp**muss eine Clientanwendung oder ein Dienstanbieter zunächst die Eigenschaften für den Vergleich mit einem Aufruf der [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode abrufen. Wenn ein Client oder Anbieter **LPropCompareProp**aufruft, untersucht die Funktion zuerst die Eigenschaftentags, um sicherzustellen, dass der Vergleich der Eigenschaftswerte gültig ist. Die Funktion vergleicht dann die Eigenschaftswerte und gibt einen entsprechenden Wert zurück. 
  
Wenn die Eigenschaftswerte ungleich sind, bestimmt **LPropCompareProp** , welche größer ist. Die Eigenschaften, die von **LPropCompareProp** verglichen werden, müssen nicht zum gleichen Objekt gehören. 
  

