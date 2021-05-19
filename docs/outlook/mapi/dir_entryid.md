---
title: DIR_ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9e055269-f3bf-4b64-8384-3cbc372c0b34
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e7abcb2c86ff5cabe0b8f5664ec316244617ac09
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421235"
---
# <a name="dir_entryid"></a>DIR_ENTRYID

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt die Eigenschaften einer Verzeichniseintrags-ID.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |entryid.h  <br/> |
   
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

## <a name="members"></a>Elemente

 **abFlags**
  
> Eine Bitmaske mit Flags, die Informationen zur Beschreibung des Objekts enthält. Weitere Informationen finden Sie in der Beschreibung des **AbFlags-Felds** einer [ENTRYID-Struktur.](entryid.md) 
    
 **muid**
  
> GUID, die den Speicheranbieter identifiziert.
    
 **ulVersion**
  
> Die Versionsnummer der **DIR_ENTRYID** Struktur. Muss auf CONTAB_VERSION. 
    
 **ulType**
  
> Eine ganze Zahl, die den Verzeichniseintrags-ID-Typ darstellt. Dies muss einer der folgenden Werte sein:
    
|**Name**|**Beschreibung**|
|:-----|:-----|
|CONTAB_ROOT  <br/> |Der Stammordner für ein MAPI-Adressbuch.  <br/> |
|CONTAB_SUBROOT  <br/> |Ein im Stammordner des MAPI-Adressbuch-Objekts enthaltener Unterordner.  <br/> |
|CONTAB_CONTAINER  <br/> |Ein Address Book Container-Objekt.  <br/> |
   
 **muidID**
  
> Eine GUID, die das Anmeldeobjekt identifiziert.
    
## <a name="remarks"></a>Hinweise

Die Strukturen **DIR_ENTRYID** [und CONTAB_ENTRYID](contab_entryid.md) sind identisch, mit Ausnahme des **ulType-Mitglieds.** Der Inhalt des **ulType-Mitglieds** bestimmt, welche Struktur für die verbleibenden Felder geeignet ist. 
  
## <a name="see-also"></a>Siehe auch



[CONTAB_ENTRYID](contab_entryid.md)


[MAPI-Strukturen](mapi-structures.md)

