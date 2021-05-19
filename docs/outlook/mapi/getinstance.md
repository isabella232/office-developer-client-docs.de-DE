---
title: GetInstance
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.GetInstance
api_type:
- COM
ms.assetid: cb432d52-6c96-45d2-bbde-45b0de3f915c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 936a20c4236ab76e5acdb178737c3044d3f53bfe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418722"
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
  
> [in] Zeiger auf eine einwertiger Eigenschaft zum Empfangen von Daten. 
    
 _uliInst_
  
> [in] Die Instanznummer, d. h. das Arrayelement, des Werts, der aus der durch den  _pvalMv-Parameter_ angegebenen Struktur kopiert wird. 
    
## <a name="return-value"></a>Return value

Keine.
  
## <a name="remarks"></a>Hinweise

Wenn der kopierte Wert für den zugewiesenen Arbeitsspeicher zu groß ist, kopiert die **GetInstance-Funktion** nur Zeiger, anstatt neuen Arbeitsspeicher zuzuordnen. 
  

