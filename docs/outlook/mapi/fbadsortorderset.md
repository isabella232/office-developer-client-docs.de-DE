---
title: FBadSortOrderSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.FBadSortOrderSet
api_type:
- COM
ms.assetid: b7f80e0a-8ddd-4b24-ab63-2078a8152058
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f051996cf6beb8b9a02889c9917eafa66e15c7d1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567648"
---
# <a name="fbadsortorderset"></a>FBadSortOrderSet

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Überprüft einen Sortierreihenfolgesatz, indem die Speicherzuweisung überprüft wird. 
  
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
  
> [in] Zeiger auf eine [SSortOrderSet-Struktur,](ssortorderset.md) die den zu überprüfenden Sortierreihenfolgesatz identifiziert. 
    
## <a name="return-value"></a>Rückgabewert

TRUE 
  
> Der angegebene Sortierreihenfolgesatz ist ungültig. 
    
FALSE 
  
> Der angegebene Sortierreihenfolgesatz ist gültig.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **FBadSortOrderSet-Funktion** kann verwendet werden, um sich auf einen Aufruf einer Sortiermethode wie der [IMAPITable::SortTable-Methode](imapitable-sorttable.md) vorzubereiten. 
  

