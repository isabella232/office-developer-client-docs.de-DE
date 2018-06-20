---
title: DIR_ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9e055269-f3bf-4b64-8384-3cbc372c0b34
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 2af9d529cb92e1040427eba69270908dcf4a5d9f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791557"
---
# <a name="direntryid"></a>DIR_ENTRYID

  
  
**Betrifft**: Outlook 
  
Beschreibt die Eigenschaften einer Directory-Eintrags-ID an.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |EntryID.h  <br/> |
   
```cpp
#pragma pack(4)
typedef struct _dir_entryid
{
    BYTE abFlags[4]; 
    MAPIUID muid; 
    ULONG ulVersion; 
    ULONG ulType; 
    MAPIUID muidID; 
}   DIR_ENTRYID, *LPDIR_ENTRYID; 
#pragma pack()
```

## <a name="members"></a>Members

 **abFlags**
  
> Eine Bitmaske aus Flags, die Informationen für das Objekt bereitstellt. Weitere Informationen finden Sie unter der Beschreibung des Felds **AbFlags** einer [ENTRYID](entryid.md) -Struktur. 
    
 **muid**
  
> GUID, den Speicheranbieter identifiziert.
    
 **ulVersion**
  
> Die Versionsnummer der **DIR_ENTRYID** Struktur. Muss auf CONTAB_VERSION festgelegt sein. 
    
 **ulType**
  
> Eine ganze Zahl, die die Art des Directory-Eintrags-ID darstellt. Es muss eine der folgenden Werte sein:
    
|**Name**|**Beschreibung**|
|:-----|:-----|
|CONTAB_ROOT  <br/> |Der Stammordner für einen MAPI-Adressbuch.  <br/> |
|CONTAB_SUBROOT  <br/> |Ein Unterordner in den Stammordner des MAPI-Address Book-Objekts enthalten sind.  <br/> |
|CONTAB_CONTAINER  <br/> |Ein Address Book Container-Objekt.  <br/> |
   
 **muidID**
  
> Eine GUID, die das Anmeldung-Objekt identifiziert wird.
    
## <a name="remarks"></a>Hinweise

Die Strukturen **DIR_ENTRYID** und [CONTAB_ENTRYID](contab_entryid.md) sind identisch, mit Ausnahme der **UlType** Member. Der Inhalt des Elements **UlType** bestimmt, welche Struktur für die übrigen Felder geeignet ist. 
  
## <a name="see-also"></a>Siehe auch



[CONTAB_ENTRYID](contab_entryid.md)


[MAPI-Strukturen](mapi-structures.md)

