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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 21ed5a23b96dabdd594547109ecb1e6c048a4844
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341069"
---
# <a name="fbadentrylist"></a>FBadEntryList

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Überprüft eine Liste von MAPI-Eintrags-IDs. 
  
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
  
> in Zeiger auf eine [entrylist](entrylist.md) -Struktur, die ein Array von Eintrags-IDs enthält, die validiert werden sollen. 
    
## <a name="return-value"></a>Rückgabewert

TRUE 
  
> Mindestens einer der aufgeführten Eintragsbezeichner ist ungültig. 
    
FALSE 
  
> Alle aufgeführten Eintragsbezeichner sind gültig.
    
## <a name="remarks"></a>Bemerkungen

Die **FBadEntryList** -Funktion bestimmt, ob die Eintrags-ID-Liste ordnungsgemäß generiert wurde. Ein Beispiel für einen ungültigen Bezeichner ist einer, für den der Arbeitsspeicher falsch zugeordnet wurde, oder ein Bezeichner mit einer falschen Größe. 
  

