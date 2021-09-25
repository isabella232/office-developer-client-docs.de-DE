---
title: FBadEntryList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- FBadEntryList
api_type:
- HeaderDef
ms.assetid: 270c47c3-ae68-4995-b304-27f861b350d6
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 333cbf047ebefd13c6da39f4d05ab349318d6ccf
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576296"
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
  
> Mindestens einer der aufgeführten Eintragsbezeichner ist ungültig. 
    
FALSE 
  
> Alle aufgeführten Eintragsbezeichner sind gültig.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **FBadEntryList-Funktion** bestimmt, ob die Eintragsbezeichnerliste ordnungsgemäß generiert wurde. Ein Beispiel für einen ungültigen Bezeichner ist ein Bezeichner, für den der Speicher falsch zugewiesen wurde, oder ein Bezeichner mit einer falschen Größe. 
  

