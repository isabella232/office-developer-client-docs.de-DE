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
ms.openlocfilehash: 8bbe8aa00ce446d228c23e1d474fa5140ae7b40a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581979"
---
# <a name="scduppropset"></a>ScDupPropset

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Array-Eigenschaft ein Wert in einem Block MAPI-Speicher die Vorgänge der Funktionen [ScCopyProps](sccopyprops.md) und [ScCountProps](sccountprops.md) kombinieren dupliziert. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
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
  
> [in] Anzahl der-Eigenschaftswerte im Array durch den Parameter _Rgprop_ angegeben. 
    
 _rgprop_
  
> [in] Zeiger auf ein Array von [SPropValue](spropvalue.md) Strukturen definieren die Eigenschaftswerte dupliziert werden. 
    
 _lpAllocateBuffer_
  
> [in] Zeiger auf die Funktion [MAPIAllocateBuffer](mapiallocatebuffer.md) , Speicher für das duplizierte Array verwendet werden soll. 
    
 _prgprop_
  
> [out] Zeiger auf die Ausgangsposition im Arbeitsspeicher, in dem das duplizierte zurückgegebene Array von **SPropValue** -Strukturen gespeichert ist. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    

