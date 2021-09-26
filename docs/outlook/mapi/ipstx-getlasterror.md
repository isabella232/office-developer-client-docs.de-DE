---
title: IPSTXGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IPSTX.GetLastError
api_type:
- COM
ms.assetid: 68dc0ecc-881e-de69-faaa-90acb9857031
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 855d50699a7ada58bd144831709cc72dc65ef322
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620485"
---
# <a name="ipstxgetlasterror"></a>IPSTX::GetLastError

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ruft erweiterte Informationen zum letzten Fehler ab.
  
```cpp
HRESULT GetLastError( 
    HRESULT hResult, 
    ULONG ulFlags, 
    LPMAPIERROR *lppMAPIError 
);
```

## <a name="parameters"></a>Parameter

 _Hresult_
  
>  [in] Fehlercode. 
    
 _ulFlags_
  
>  [in] Flags, die Verhalten ändern. Dies muss 0 sein. 
    
 _lppMAPIError_
  
>  [out] Zeiger auf die **MAPIERROR-Struktur,** die die erweiterten Informationen für den Fehler enthält. Die Typdefinition von **LPMAPIERROR** finden Sie unter mapidefs.h. 
    
## <a name="see-also"></a>Siehe auch



[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)
  
[IPSTX::GetSyncObject](ipstx-getsyncobject.md)

