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
ms.openlocfilehash: 7726811467324242037ec11a69ae0b1b123d7f21
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427157"
---
# <a name="fpropcompareprop"></a>FPropCompareProp

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Vergleicht zwei Eigenschaftswerte mit einem angegebenen relationalen Operator. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen und Dienstanbieter  <br/> |
   
```cpp
BOOL FPropCompareProp(
  LPSPropValue lpSPropValue1,
  ULONG ulRelOp,
  LPSPropValue lpSPropValue2
);
```

## <a name="parameters"></a>Parameter

_lpSPropValue1_
  
> in Zeiger auf eine [SPropValue](spropvalue.md) -Struktur, die den ersten Eigenschaftswert für den Vergleich definiert. 
    
_ulRelOp_
  
> in Der relationale Operator, der im Vergleich verwendet werden soll. Informationen zu zulässigen Werten finden Sie in der [SComparePropsRestriction](scomparepropsrestriction.md) -Struktur. 
    
_lpSPropValue2_
  
> in Zeiger auf eine **SPropValue** -Struktur, die den zweiten Eigenschaftswert für den Vergleich definiert. 
    
## <a name="return-value"></a>Rückgabewert

TRUE 
  
> Die Eigenschaftswerte erfüllen die angegebene Beziehung. 
    
FALSE 
  
> Die Eigenschaftswerte erfüllen nicht die angegebene Beziehung.
    
## <a name="remarks"></a>Bemerkungen

Die Vergleichsmethode hängt von den Eigenschaftentypen ab, die in den [SPropValue](spropvalue.md) -Eigenschaftsdefinitionen angegeben sind. Die **FPropCompareProp** -und [FPropContainsProp](fpropcontainsprop.md) -Funktionen können verwendet werden, um Einschränkungen für das Generieren einer Tabelle vorzubereiten. 
  
Die Reihenfolge des Vergleichs ist _lpSPropValue1_, _ ulRelOp _, _ lpSPropValue2 _. Wenn die Eigenschaftentypen der zu vergleichenden Eigenschaftswerte nicht übereinstimmen, gibt die **FPropCompareProp** -Funktion false zurück. 
  

