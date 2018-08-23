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
ms.openlocfilehash: c4e5d2847b53988fb75e23fc6c4dfc386ea678f4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579263"
---
# <a name="getinstance"></a>GetInstance

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Kopiert einen Wert innerhalb einer mehrwertigen Eigenschaft zu einer einwertige Eigenschaft des gleichen Typs. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |MAPIUTIL. H  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
```cpp
VOID GetInstance(
  LPSPropValue pvalMv,
  LPSPropValue pvalSv,
  ULONG uliInst
);
```

## <a name="parameters"></a>Parameter

 _pvalMv_
  
> [in] Zeiger auf eine [SPropValue](spropvalue.md) -Struktur, die eine mehrwertige Eigenschaft definieren. 
    
 _pvalSv_
  
> [in] Zeiger auf eine einwertige Eigenschaft Daten empfangen. 
    
 _uliInst_
  
> [in] Die Instanz an, die ist, das Arrayelement des Werts aus der Struktur, von der _PvalMv_ -Parameter angegebene kopiert werden. 
    
## <a name="return-value"></a>Rückgabewert

None.
  
## <a name="remarks"></a>HinwBemerkungeneise

Wenn der Wert für reservierter Speicher zu groß ist, kopiert die **GetInstance** -Funktion nur Zeiger, anstatt neue Arbeitsspeicher. 
  

