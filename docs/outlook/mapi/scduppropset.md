---
title: ScDupPropset
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.ScDupPropset
api_type:
- COM
ms.assetid: 165ffbd0-54aa-4692-8bd1-09e6ff3762df
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 4da98b19f394e68f801104926b04e52068a1c145
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591234"
---
# <a name="scduppropset"></a>ScDupPropset

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Dupliziert ein Eigenschaftswertarray in einem einzigen MAPI-Speicherblock, der die Vorgänge der [Funktionen ScCopyProps](sccopyprops.md) und [ScCountProps](sccountprops.md) kombiniert. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
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
  
> [in] Anzahl der Eigenschaftswerte im Array, das durch den  _rgprop-Parameter_ angegeben wird. 
    
 _rgprop_
  
> [in] Zeiger auf ein Array von [SPropValue-Strukturen,](spropvalue.md) die die zu duplizierenden Eigenschaftswerte definieren. 
    
 _lpAllocateBuffer_
  
> [in] Zeiger auf die [MAPIAllocateBuffer-Funktion,](mapiallocatebuffer.md) die zum Zuordnen von Speicher für das duplizierte Array verwendet werden soll. 
    
 _prgprop_
  
> [out] Zeiger auf die ursprüngliche Position im Speicher, an der das zurückgegebene duplizierte Array von **SPropValue-Strukturen** gespeichert ist. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    

