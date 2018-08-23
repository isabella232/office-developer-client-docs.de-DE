---
title: IPSTXGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTX.GetLastError
api_type:
- COM
ms.assetid: 68dc0ecc-881e-de69-faaa-90acb9857031
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f45b070464fe1b3c177088ff6aa3295f961d45f6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592591"
---
# <a name="ipstxgetlasterror"></a>IPSTX::GetLastError

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Ruft Informationen über den letzten Fehler erweitert.
  
```cpp
HRESULT GetLastError( 
    HRESULT hResult, 
    ULONG ulFlags, 
    LPMAPIERROR *lppMAPIError 
);
```

## <a name="parameters"></a>Parameter

 _hResult_
  
>  [in] Fehlercode. 
    
 _ulFlags_
  
>  [in] Flags, die Verhalten ändern. Dies muss 0 sein. 
    
 _lppMAPIError_
  
>  [out] Zeiger auf die **MAPIERROR** -Struktur, die erweiterte Informationen für den Fehler enthält. Finden Sie unter mapidefs.h für die Definition des **LPMAPIERROR**Typs. 
    
## <a name="see-also"></a>Siehe auch



[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)
  
[IPSTX::GetSyncObject](ipstx-getsyncobject.md)

