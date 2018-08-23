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
ms.openlocfilehash: 113628ef5487bc66a07d1367c938ed178a8e32ec
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582910"
---
# <a name="fbadentrylist"></a>FBadEntryList

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
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
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **FBadEntryList** -Funktion bestimmt, ob die Liste den Eintrag Bezeichner ordnungsgemäß generiert wurde. Ein Beispiel für einen ungültigen Bezeichner ist eine für welche Speicher falsch zugewiesen wurde oder einen Bezeichner, der eine falsche Größe. 
  

