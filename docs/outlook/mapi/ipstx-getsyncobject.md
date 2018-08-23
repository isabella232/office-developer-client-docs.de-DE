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
ms.openlocfilehash: e0e27d86098ec55849fa96cc150c60934ef2810b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585451"
---
# <a name="ipstxgetsyncobject"></a>IPSTX::GetSyncObject

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Startet eine Sitzung Synchronisierung und ruft die zugehörige **[IOSTX](iostxiunknown.md)** Schnittstelle ab. 
  
```cpp
HRESULT GetSyncObject( 
   IOSTX **ppostx 
);
```

## <a name="parameters"></a>Parameter

 _ppostx_
  
>  [out] Zeiger auf die **IOSTX** -Schnittstelle zu erhalten. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Der Aufrufer muss sicherstellen, dass im gleiche Ordner nicht gleichzeitig auf mehreren Threads synchronisiert ist.
  
## <a name="see-also"></a>Siehe auch



[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)
  
[IPSTX::GetLastError](ipstx-getlasterror.md)

