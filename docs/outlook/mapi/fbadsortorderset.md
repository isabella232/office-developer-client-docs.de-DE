---
title: FBadSortOrderSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadSortOrderSet
api_type:
- COM
ms.assetid: b7f80e0a-8ddd-4b24-ab63-2078a8152058
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 31840923e24cddd0dc3dfa9cc67b610d0dcd7e47
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336974"
---
# <a name="fbadsortorderset"></a>FBadSortOrderSet

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Überprüft eine Sortierreihenfolge, die durch Überprüfen der Speicherbelegung festgelegt wurde. 
  
|||
|:-----|:-----|
|Headerdatei:  <br/> |Mapival.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Dienstanbieter  <br/> |
   
```cpp
ULONG FBadSortOrderSet(
  LPSSortOrderSet lpsos
);
```

## <a name="parameters"></a>Parameter

 _lpsos_
  
> in Zeiger auf eine [SSortOrderSet](ssortorderset.md) -Struktur, die die zu validierende Sortierreihenfolge festgelegt. 
    
## <a name="return-value"></a>Rückgabewert

TRUE 
  
> Die angegebene Sortierreihenfolge ist ungültig. 
    
FALSE 
  
> Der angegebene Sortierreihenfolge-Satz ist gültig.
    
## <a name="remarks"></a>Bemerkungen

Die **FBadSortOrderSet** -Funktion kann verwendet werden, um einen Aufruf einer Sort-Methode wie der [IMAPITable:: sortable](imapitable-sorttable.md) -Methode vorzubereiten. 
  

