---
title: FBadColumnSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadColumnSet
api_type:
- HeaderDef
ms.assetid: 15be5a8c-4299-4434-b521-c901215b9dda
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 5d1654908c50c348a27e1281168756100b7a88a2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791666"
---
# <a name="fbadcolumnset"></a>FBadColumnSet

  
  
**Betrifft**: Outlook 
  
Legen Sie die Gültigkeit einer Tabellenspalte für Tests verwenden, indem Sie einem Dienstanbieter in einem nachfolgenden Aufruf der [IMAPITable::SetColumns](imapitable-setcolumns.md) -Methode. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapival.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Dienstanbieter  <br/> |
   
```cpp
ULONG FBadColumnSet(
  LPSPropTagArray lpptaCols
);
```

## <a name="parameters"></a>Parameter

 _lpptaCols_
  
> [in] Zeiger auf eine [SPropTagArray](sproptagarray.md) -Struktur, die ein Array von Eigenschaftentags definieren die Tabellenspalten überprüfen enthält. 
    
## <a name="return-value"></a>R�ckgabewert

TRUE 
  
> Der angegebene Spalte ist ungültig. 
    
FALSE 
  
> Der angegebene Spalte ist ungültig.
    
## <a name="remarks"></a>Hinweise

Die **FBadColumnSet** -Funktion wird vom Typ PT_ERROR als ungültig und Spalten vom Typ PT_NULL als ungültig behandelt. 
  

