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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 936a20c4236ab76e5acdb178737c3044d3f53bfe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299545"
---
# <a name="getinstance"></a>GetInstance

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Kopiert einen Wert in einer mehrwertigen Eigenschaft in eine einwertige Eigenschaft desselben Typs. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |MAPIUTIL. H  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen und Dienstanbieter  <br/> |
   
```cpp
VOID GetInstance(
  LPSPropValue pvalMv,
  LPSPropValue pvalSv,
  ULONG uliInst
);
```

## <a name="parameters"></a>Parameter

 _pvalMv_
  
> in Zeiger auf eine [SPropValue](spropvalue.md) -Struktur, die eine mehrwertige Eigenschaft definiert. 
    
 _pvalSv_
  
> in Zeiger auf eine einwertige Eigenschaft zum Empfangen von Daten. 
    
 _uliInst_
  
> in Die Instanznummer, also das Arrayelement, des Werts, der aus der vom _pvalMv_ -Parameter angegebenen Struktur kopiert wird. 
    
## <a name="return-value"></a>Return value

Keine.
  
## <a name="remarks"></a>Bemerkungen

Wenn der kopierte Wert für den zugewiesenen Speicher zu umfangreich **** ist, kopiert die GetInstance-Funktion nur Zeiger, anstatt neuen Speicher zuzuweisen. 
  

