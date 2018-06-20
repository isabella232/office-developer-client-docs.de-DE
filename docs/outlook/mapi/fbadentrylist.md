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
ms.openlocfilehash: aae2e97b987414fc5e46b410465d3232b61f1ffe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791652"
---
# <a name="fbadentrylist"></a>FBadEntryList

  
  
**Betrifft**: Outlook 
  
Eine Liste der MAPI-Eintragsbezeichner überprüft. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapival.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Dienstanbieter  <br/> |
   
```cpp
BOOL FBadEntryList(
  LPENTRYLIST lpEntryList
);
```

## <a name="parameters"></a>Parameter

 _lpEntryList_
  
> [in] Zeiger auf eine [ENTRYLIST](entrylist.md) -Struktur, die ein Array von Eintragsbezeichner überprüft werden soll. 
    
## <a name="return-value"></a>R�ckgabewert

TRUE 
  
> Mindestens eines der aufgelisteten-Eintragsbezeichner sind ungültig. 
    
FALSE 
  
> Alle der aufgelisteten-Eintragsbezeichner sind ungültig.
    
## <a name="remarks"></a>Hinweise

Die **FBadEntryList** -Funktion bestimmt, ob die Liste den Eintrag Bezeichner ordnungsgemäß generiert wurde. Ein Beispiel für einen ungültigen Bezeichner ist eine für welche Speicher falsch zugewiesen wurde oder einen Bezeichner, der eine falsche Größe. 
  

