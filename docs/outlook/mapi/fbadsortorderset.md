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
ms.openlocfilehash: 3b3f88495cafbd6ea764ca8901ac67c23749aebe
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578577"
---
# <a name="fbadsortorderset"></a>FBadSortOrderSet

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
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
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **FBadSortOrderSet** -Funktion kann zur Vorbereitung eines Anrufs an eine Sortiermethode wie der [SortTable](imapitable-sorttable.md) -Methode verwendet werden. 
  

