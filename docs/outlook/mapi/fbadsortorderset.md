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
ms.openlocfilehash: 0e200ea20c55cfd5729ce4c1f590de2d61ca73bc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791664"
---
# <a name="fbadsortorderset"></a>FBadSortOrderSet

  
  
**Betrifft**: Outlook 
  
Überprüft eine Sortierreihenfolge festlegen, indem Sie die Zuweisung von virtuellem Speicher überprüfen. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapival.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Dienstanbieter  <br/> |
   
```cpp
ULONG FBadSortOrderSet(
  LPSSortOrderSet lpsos
);
```

## <a name="parameters"></a>Parameter

 _lpsos_
  
> [in] Zeiger auf eine [SSortOrderSet](ssortorderset.md) -Struktur, die die Sortierreihenfolge festlegen zu überprüfenden identifiziert. 
    
## <a name="return-value"></a>R�ckgabewert

TRUE 
  
> Die angegebene sortieren Reihenfolge Gruppe ist ungültig. 
    
FALSE 
  
> Der angegebene sortieren Reihenfolge ist ungültig.
    
## <a name="remarks"></a>Bemerkungen

Die **FBadSortOrderSet** -Funktion kann zur Vorbereitung eines Anrufs an eine Sortiermethode wie der [SortTable](imapitable-sorttable.md) -Methode verwendet werden. 
  

