---
title: FBadColumnSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- FBadColumnSet
api_type:
- HeaderDef
ms.assetid: 15be5a8c-4299-4434-b521-c901215b9dda
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 1498705c0459798f1ae8c49586423603500c6e8b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59601002"
---
# <a name="fbadcolumnset"></a>FBadColumnSet

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Überprüft die Gültigkeit eines Tabellenspaltensatzes für die Verwendung durch einen Dienstanbieter in einem nachfolgenden Aufruf der [IMAPITable::SetColumns-Methode.](imapitable-setcolumns.md) 
  
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
  
> [in] Zeiger auf eine [SPropTagArray-Struktur,](sproptagarray.md) die ein Array von Eigenschaftstags enthält, die die zu überprüfenden Tabellenspalten definieren. 
    
## <a name="return-value"></a>Rückgabewert

TRUE 
  
> Der angegebene Spaltensatz ist ungültig. 
    
FALSE 
  
> Der angegebene Spaltensatz ist gültig.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **FBadColumnSet-Funktion** behandelt Spalten vom Typ PT_ERROR als ungültig und Spalten vom Typ PT_NULL als gültig. 
  

