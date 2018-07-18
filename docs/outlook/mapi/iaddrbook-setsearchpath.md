---
title: IAddrBookSetSearchPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.SetSearchPath
api_type:
- COM
ms.assetid: fbff82de-77d3-411e-a30c-a37cefdd92fc
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4f9d2f4d271e467d8fac32b8f17faa8f66cd3f99
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792018"
---
# <a name="iaddrbooksetsearchpath"></a>IAddrBook::SetSearchPath

  
  
**Betrifft**: Outlook 
  
Legt einen neuen Pfad für die Suche in das Profil, das für den Vorgang der Lösung verwendet wird. 
  
```cpp
HRESULT SetSearchPath(
  ULONG ulFlags,
  LPSRowSet lpSearchPath
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
 _lpSearchPath_
  
> [in] Ein Zeiger auf die [SRowSet](srowset.md) -Struktur verwendet, um den Suchpfad aufzunehmen. Die erste Eigenschaft für jedes Mitglied **aRow** in **' srowset '** muss **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Suchpfad wurde erfolgreich festgelegt.
    
MAPI_E_MISSING_REQUIRED_COLUMN 
  
> Eine der in der Struktur **SRowSet** beschriebenen Container haben dessen **PR_ENTRYID** -Eigenschaft nicht eingeschlossen. 
    
## <a name="remarks"></a>Bemerkungen

Rufen die **SetSearchPath** -Methode, um die Änderungen zu speichern, die an die Reihenfolge des Containers Suche vorgenommen wurden, die zum Auflösen von Namen mit der [IAddrBook::ResolveName](iaddrbook-resolvename.md) -Methode verwendet wird, Clients und -Dienstanbieter. Der Suchpfad wird zwischen Instanzen von einer Sitzung gespeichert. 
  
Clients und Anbieter müssen nicht Aufrufen der [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode, um die Suche Pfad Änderungen dauerhaft entfernt wird. 
  
## <a name="see-also"></a>Siehe auch



[IAddrBook::GetDefaultDir](iaddrbook-getdefaultdir.md)
  
[IAddrBook::GetPAB](iaddrbook-getpab.md)
  
[IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md)
  
[PidTagContainerFlags (kanonische Eigenschaft)](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

