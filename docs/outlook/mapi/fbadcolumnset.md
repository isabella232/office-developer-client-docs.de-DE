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
ms.openlocfilehash: b0260ffe5dc4806cb627fd71c78866bf96796455
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341006"
---
# <a name="fbadcolumnset"></a>FBadColumnSet

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Testet die Gültigkeit eines Tabellenspalten Satzes, der von einem Dienstanbieter bei einem nachfolgenden Aufruf der [IMAPITable::](imapitable-setcolumns.md) SetColumns-Methode verwendet wird. 
  
|||
|:-----|:-----|
|Headerdatei:  <br/> |Mapival.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Dienstanbieter  <br/> |
   
```cpp
ULONG FBadColumnSet(
  LPSPropTagArray lpptaCols
);
```

## <a name="parameters"></a>Parameter

 _lpptaCols_
  
> in Zeiger auf eine [SPropTagArray](sproptagarray.md) -Struktur, die ein Array von Property-Tags enthält, die die zu überprüfenden Tabellenspalten definieren. 
    
## <a name="return-value"></a>Rückgabewert

TRUE 
  
> Der angegebene Spaltensatz ist ungültig. 
    
FALSE 
  
> Der angegebene Spaltensatz ist gültig.
    
## <a name="remarks"></a>Bemerkungen

Die **FBadColumnSet** -Funktion behandelt Spalten vom Typ PT_ERROR als ungültig und Spalten vom Typ PT_NULL als gültig. 
  

