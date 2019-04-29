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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 31840923e24cddd0dc3dfa9cc67b610d0dcd7e47
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428459"
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
  

