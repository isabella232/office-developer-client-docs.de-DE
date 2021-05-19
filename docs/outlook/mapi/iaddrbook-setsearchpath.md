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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8611249207811446ae47f056486ec498bf1e7eab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426205"
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
  
> [in] Ein Zeiger auf die [SRowSet-Struktur,](srowset.md) die zum Halten des Suchpfads verwendet wird. Die erste Eigenschaft für jedes **aRow-Element** in **SRowSet** muss **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) sein.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Suchpfad wurde erfolgreich festgelegt.
    
MAPI_E_MISSING_REQUIRED_COLUMN 
  
> Einer der in der **SRowSet-Struktur** beschriebenen Container hat seine PR_ENTRYID **enthalten.** 
    
## <a name="remarks"></a>Hinweise

Clients und Dienstanbieter rufen die **SetSearchPath-Methode** auf, um Änderungen an der Containersuchreihenfolge zu speichern, die zum Auflösen von Namen mit der [IAddrBook::ResolveName-Methode](iaddrbook-resolvename.md) verwendet wird. Der Suchpfad wird zwischen Instanzen einer Sitzung gespeichert. 
  
Clients und Anbieter müssen die [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) nicht aufrufen, um die Änderungen des Suchpfads dauerhaft vorzunehmen. 
  
## <a name="see-also"></a>Siehe auch



[IAddrBook::GetDefaultDir](iaddrbook-getdefaultdir.md)
  
[IAddrBook::GetPAB](iaddrbook-getpab.md)
  
[IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md)
  
[PidTagContainerFlags (kanonische Eigenschaft)](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

