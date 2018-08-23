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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 4e5f19258fb7716e741928f02a0a87f3939c74e0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575098"
---
# <a name="fbadcolumnset"></a>FBadColumnSet

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
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
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **FBadColumnSet** -Funktion wird vom Typ PT_ERROR als ungültig und Spalten vom Typ PT_NULL als ungültig behandelt. 
  

