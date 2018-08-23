---
title: FPropCompareProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FPropCompareProp
api_type:
- COM
ms.assetid: 17cb53c4-7154-4a4e-b4ec-de720fa055cb
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: adccbaf65adec2c517c4890f722198e8262092cb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564605"
---
# <a name="fpropcompareprop"></a>FPropCompareProp

**Betrifft**: Outlook 2013 | Outlook 2016 
  
Vergleicht zwei Eigenschaftswerte, die mit einem angegebenen relationalen Operator. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
```cpp
BOOL FPropCompareProp(
  LPSPropValue lpSPropValue1,
  ULONG ulRelOp,
  LPSPropValue lpSPropValue2
);
```

## <a name="parameters"></a>Parameter

_lpSPropValue1_
  
> [in] Zeiger auf eine [SPropValue](spropvalue.md) -Struktur für den Vergleich den ersten Eigenschaftswert definieren. 
    
_ulRelOp_
  
> [in] Der relationale Operator, im Vergleich zu verwenden. Zulässige Werte finden Sie unter der Struktur [SComparePropsRestriction](scomparepropsrestriction.md) . 
    
_lpSPropValue2_
  
> [in] Zeiger auf eine **SPropValue** -Struktur für den Vergleich den zweiten Eigenschaftswert definieren. 
    
## <a name="return-value"></a>R�ckgabewert

TRUE 
  
> Die Eigenschaftswerte erfüllen die angegebene Relation-Objekt. 
    
FALSE 
  
> Die Eigenschaftswerte werden nicht die angegebene Relation-Objekt erfüllen.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die Vergleichsmethode hängt die Eigenschaftentypen in die Definitionen der [SPropValue](spropvalue.md) -Eigenschaft angegeben. Die Funktionen **FPropCompareProp** und [FPropContainsProp](fpropcontainsprop.md) können verwendet werden, um Einschränkungen zum Generieren einer Tabelle vorzubereiten. 
  
Die Reihenfolge des Vergleichs ist _lpSPropValue1_, _ UlRelOp _, _ lpSPropValue2 _. Die **FPropCompareProp** -Funktion gibt FALSE zurück, wenn die Eigenschaftentypen der Eigenschaftswerte, die verglichen werden nicht übereinstimmen. 
  

