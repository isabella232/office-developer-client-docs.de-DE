---
title: IPSTXGetSyncObject
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTX.GetSyncObject
api_type:
- COM
ms.assetid: b93dae79-4305-9a3a-7b93-42319f7e26ba
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 31ef1f5c6af498f042ab766ae90fcfbce805700a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407109"
---
# <a name="ipstxgetsyncobject"></a>IPSTX::GetSyncObject

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Startet eine Synchronisierungssitzung und ruft die zugehörige **[IOSTX](iostxiunknown.md)** -Schnittstelle ab. 
  
```cpp
HRESULT GetSyncObject( 
   IOSTX **ppostx 
);
```

## <a name="parameters"></a>Parameter

 _ppostx_
  
>  Out Zeiger auf die **IOSTX** -Schnittstelle abrufen. 
    
## <a name="remarks"></a>Bemerkungen

Der Aufrufer muss sicherstellen, dass derselbe Ordner nicht gleichzeitig für mehrere Threads synchronisiert ist.
  
## <a name="see-also"></a>Siehe auch



[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)
  
[IPSTX::GetLastError](ipstx-getlasterror.md)

