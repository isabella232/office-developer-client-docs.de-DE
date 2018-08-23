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
ms.openlocfilehash: 0985ed0c5d4482bb22f46bdc9198afc343c61e5f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565536"
---
# <a name="lpropcompareprop"></a>LPropCompareProp

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Vergleicht zwei Eigenschaftswerte, um festzustellen, ob diese gleich sind. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
```cpp
LONG LPropCompareProp(
  LPSPropValue lpSPropValueA,
  LPSPropValue lpSPropValueB
);
```

## <a name="parameters"></a>Parameter

 _lpSPropValueA_
  
> [in] Zeiger auf eine [SPropValue](spropvalue.md) -Struktur definieren den ersten Eigenschaftswert verglichen werden soll. 
    
 _lpSPropValueB_
  
> [in] Zeiger auf eine **SPropValue** -Struktur definieren den zweiten Eigenschaftswert verglichen werden soll. 
    
## <a name="return-value"></a>R�ckgabewert

 **LPropCompareProp** gibt einen der folgenden Werte für die meisten Eigenschaftentypen zurück: 
  
- Kleiner als 0 (null) ist der Parameter _LpSPropValueA_ , wenn der Wert von angegebenen kleiner ist als der durch den Parameter _LpSPropValueB_ angegeben. 
    
- Größer als 0 (null), wenn der Wert von _LpSPropValueA_ angegebene ist größer als der mit _LpSPropValueB_angegeben.
    
- 0 (null), wenn der Wert von _LpSPropValueA_ angegebene gleich den durch _LpSPropValueB_angegebenen Wert ist. 
    
Für Eigenschaftentypen, die keine systeminterne Sortierung, wie etwa boolescher Wert haben oder Fehlertypen, gibt die **LPropCompareProp** -Funktion einen nicht definierten Wert zurück, wenn die zwei Werte nicht gleich sind. Dieser Wert nicht definierte sind ungleich NULL und konsistent Anrufe. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Verwenden Sie die **LPropCompareProp** -Funktion nur, wenn die Typen der beiden Eigenschaften, die verglichen werden identisch sind. 
  
Vor dem Aufruf von **LPropCompareProp**, muss eine Clientanwendung oder Dienstanbieter zunächst die Eigenschaften für den Vergleich mit einem Aufruf der [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode abrufen. Der Vergleich von Eigenschaftswerten ist gültig, wenn ein Client oder Anbieter Anrufe **LPropCompareProp**, die Funktion zuerst die Eigenschaftentags, um sicherzustellen, dass untersucht. Die Funktion vergleicht dann die Eigenschaftswerte, die einen entsprechenden Wert zurückgeben. 
  
Wenn die Werte ungleich sind, bestimmt **LPropCompareProp** an, welche größer ist. Die Eigenschaften, die **LPropCompareProp** vergleicht müssen nicht auf das gleiche Objekt gehören. 
  

