---
title: ScDupPropset
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScDupPropset
api_type:
- COM
ms.assetid: 165ffbd0-54aa-4692-8bd1-09e6ff3762df
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 77a376bba8d65737be84e2af62e65e0419d20957
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406017"
---
# <a name="scduppropset"></a>ScDupPropset

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Dupliziert ein Eigenschafts Wertarray in einem einzelnen MAPI-Blockspeicher, der die Vorgänge der [ScCopyProps](sccopyprops.md) -und [ScCountProps](sccountprops.md) -Funktionen kombiniert. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen und Dienstanbieter  <br/> |
   
```cpp
SCODE ScDupPropset(
  int cprop,
  LPSPropValue rgprop,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPSPropValue FAR * prgprop
);
```

## <a name="parameters"></a>Parameter

 _cprop_
  
> in Die Anzahl der Eigenschaftswerte im durch den _rgprop_ -Parameter angegebenen Array. 
    
 _rgprop_
  
> in Zeiger auf ein Array von [SPropValue](spropvalue.md) -Strukturen, die die Eigenschaftswerte definieren, die dupliziert werden sollen. 
    
 _lpAllocateBuffer_
  
> in Zeiger auf die [MAPIAllocateBuffer](mapiallocatebuffer.md) -Funktion, die zum Zuweisen von Arbeitsspeicher für das duplizierte Array verwendet werden soll. 
    
 _prgprop_
  
> Out Zeiger auf die Anfangsposition im Arbeitsspeicher, in der das zurückgegebene duplizierte Array von **SPropValue** -Strukturen gespeichert wird. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    

