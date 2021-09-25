---
title: FPropCompareProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.FPropCompareProp
api_type:
- COM
ms.assetid: 17cb53c4-7154-4a4e-b4ec-de720fa055cb
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5357bd8a2adc470322b772ceabbeaef8596290f5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621045"
---
# <a name="fpropcompareprop"></a>FPropCompareProp

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Vergleicht zwei Eigenschaftswerte mithilfe eines angegebenen relationalen Operators. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
```cpp
BOOL FPropCompareProp(
  LPSPropValue lpSPropValue1,
  ULONG ulRelOp,
  LPSPropValue lpSPropValue2
);
```

## <a name="parameters"></a>Parameter

_lpSPropValue1_
  
> [in] Zeiger auf eine [SPropValue-Struktur,](spropvalue.md) die den ersten Eigenschaftswert für den Vergleich definiert. 
    
_ulRelOp_
  
> [in] Der relationale Operator, der im Vergleich verwendet werden soll. Zulässige Werte finden Sie in der [Struktur "SComparePropsRestriction".](scomparepropsrestriction.md) 
    
_lpSPropValue2_
  
> [in] Zeiger auf eine **SPropValue-Struktur,** die den zweiten Eigenschaftswert für den Vergleich definiert. 
    
## <a name="return-value"></a>Rückgabewert

TRUE 
  
> Die Eigenschaftswerte erfüllen die angegebene Beziehung. 
    
FALSE 
  
> Die Eigenschaftswerte erfüllen nicht die angegebene Beziehung.
    
## <a name="remarks"></a>Bemerkungen

Die Vergleichsmethode hängt von den in den [SPropValue-Eigenschaftsdefinitionen](spropvalue.md) angegebenen Eigenschaftstypen ab. Die Funktionen **FPropCompareProp** und [FPropContainsProp](fpropcontainsprop.md) können verwendet werden, um Einschränkungen für das Generieren einer Tabelle vorzubereiten. 
  
Die Reihenfolge des Vergleichs ist  _lpSPropValue1_, _ ulRelOp _, _ lpSPropValue2 _. Wenn die Eigenschaftstypen der zu vergleichenden Eigenschaftswerte nicht übereinstimmen, gibt die **FPropCompareProp-Funktion** FALSE zurück. 
  

