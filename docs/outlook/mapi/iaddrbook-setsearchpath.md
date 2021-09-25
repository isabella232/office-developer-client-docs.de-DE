---
title: IAddrBookSetSearchPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IAddrBook.SetSearchPath
api_type:
- COM
ms.assetid: fbff82de-77d3-411e-a30c-a37cefdd92fc
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c25bd89d6bc81877a9d5cf9d6b4153081306c2d9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596435"
---
# <a name="iaddrbooksetsearchpath"></a>IAddrBook::SetSearchPath

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Legt einen neuen Suchpfad im Profil fest, der für den Namensauflösungsprozess verwendet wird. 
  
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
  
> [in] Ein Zeiger auf die [SRowSet-Struktur,](srowset.md) die zum Speichern des Suchpfads verwendet wird. Die erste Eigenschaft für jedes **aRow-Element** in **SRowSet** muss **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) sein.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Suchpfad wurde erfolgreich festgelegt.
    
MAPI_E_MISSING_REQUIRED_COLUMN 
  
> Einer der in der **SRowSet-Struktur** beschriebenen Container enthielt nicht die **PR_ENTRYID** Eigenschaft. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Clients und Dienstanbieter rufen die **SetSearchPath-Methode** auf, um Änderungen an der Containersuchreihenfolge zu speichern, die zum Auflösen von Namen mit der [IAddrBook::ResolveName-Methode](iaddrbook-resolvename.md) verwendet wird. Der Suchpfad wird zwischen Instanzen einer Sitzung gespeichert. 
  
Clients und Anbieter müssen die [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) nicht aufrufen, um die Änderungen des Suchpfads dauerhaft zu machen. 
  
## <a name="see-also"></a>Siehe auch



[IAddrBook::GetDefaultDir](iaddrbook-getdefaultdir.md)
  
[IAddrBook::GetPAB](iaddrbook-getpab.md)
  
[IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md)
  
[PidTagContainerFlags (kanonische Eigenschaft)](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

