---
title: GetInstance
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.GetInstance
api_type:
- COM
ms.assetid: cb432d52-6c96-45d2-bbde-45b0de3f915c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f320ebf3311e2227a2969086606d3b3e592d6e63
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551569"
---
# <a name="getinstance"></a>GetInstance

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Kopiert einen Wert innerhalb einer mehrwertigen Eigenschaft in eine einwertige Eigenschaft desselben Typs. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |MAPIUTIL. H  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
```cpp
VOID GetInstance(
  LPSPropValue pvalMv,
  LPSPropValue pvalSv,
  ULONG uliInst
);
```

## <a name="parameters"></a>Parameter

 _pvalMv_
  
> [in] Zeiger auf eine [SPropValue-Struktur,](spropvalue.md) die eine mehrwertige Eigenschaft definiert. 
    
 _pvalSv_
  
> [in] Zeiger auf eine einwertige Eigenschaft zum Empfangen von Daten. 
    
 _uliInst_
  
> [in] Die Instanznummer, d. h. das Arrayelement, des Werts, der aus der durch den  _pvalMv-Parameter_ angegebenen Struktur kopiert wird. 
    
## <a name="return-value"></a>Return value

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Wenn der kopierte Wert für den zugewiesenen Speicher zu groß ist, kopiert die **GetInstance-Funktion** nur Zeiger, anstatt neuen Speicher zuzuweisen. 
  

