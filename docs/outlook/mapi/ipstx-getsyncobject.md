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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 44261e5ac296004fd113d4c9123b99c482bcb732
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792819"
---
# <a name="ipstxgetsyncobject"></a>IPSTX::GetSyncObject

  
  
**Betrifft**: Outlook 
  
Startet eine Sitzung Synchronisierung und ruft die zugehörige **[IOSTX](iostxiunknown.md)** Schnittstelle ab. 
  
```cpp
HRESULT GetSyncObject( 
   IOSTX **ppostx 
);
```

## <a name="parameters"></a>Parameter

 _ppostx_
  
>  [out] Zeiger auf die **IOSTX** -Schnittstelle zu erhalten. 
    
## <a name="remarks"></a>Bemerkungen

Der Aufrufer muss sicherstellen, dass im gleiche Ordner nicht gleichzeitig auf mehreren Threads synchronisiert ist.
  
## <a name="see-also"></a>Siehe auch



[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)
  
[IPSTX::GetLastError](ipstx-getlasterror.md)

