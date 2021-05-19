---
title: FBadEntryList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadEntryList
api_type:
- HeaderDef
ms.assetid: 270c47c3-ae68-4995-b304-27f861b350d6
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 21ed5a23b96dabdd594547109ecb1e6c048a4844
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427773"
---
# <a name="fbadentrylist"></a>FBadEntryList

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Überprüft eine Liste der MAPI-Eintragsbezeichner. 
  
|||
|:-----|:-----|
|Headerdatei:  <br/> |Mapival.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Dienstanbieter  <br/> |
   
```cpp
BOOL FBadEntryList(
  LPENTRYLIST lpEntryList
);
```

## <a name="parameters"></a>Parameter

 _lpEntryList_
  
> [in] Zeiger auf eine [ENTRYLIST-Struktur,](entrylist.md) die ein Array von Eintragsbezeichnern enthält, die überprüft werden sollen. 
    
## <a name="return-value"></a>Rückgabewert

TRUE 
  
> Mindestens eine der aufgeführten Eintragsbezeichner ist ungültig. 
    
FALSE 
  
> Alle aufgeführten Eintragsbezeichner sind gültig.
    
## <a name="remarks"></a>Hinweise

Die **FBadEntryList-Funktion** bestimmt, ob die Eintragsbezeichnerliste ordnungsgemäß generiert wurde. Ein Beispiel für einen ungültigen Bezeichner ist ein Bezeichner, für den der Arbeitsspeicher falsch zugewiesen wurde, oder ein Bezeichner mit einer falschen Größe. 
  

