---
title: IPSTXGetSyncObject
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IPSTX.GetSyncObject
api_type:
- COM
ms.assetid: b93dae79-4305-9a3a-7b93-42319f7e26ba
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: afb2d133259f5eb8645e67ad1def88097b5ed60b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59587832"
---
# <a name="ipstxgetsyncobject"></a>IPSTX::GetSyncObject

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Startet eine Synchronisierungssitzung und ruft die zugeordnete **[IOSTX-Schnittstelle](iostxiunknown.md)** ab. 
  
```cpp
HRESULT GetSyncObject( 
   IOSTX **ppostx 
);
```

## <a name="parameters"></a>Parameter

 _ppostx_
  
>  [out] Zeiger auf die **abzurufende IOSTX-Schnittstelle.** 
    
## <a name="remarks"></a>HinwBemerkungeneise

Der Aufrufer muss sicherstellen, dass derselbe Ordner nicht gleichzeitig in mehreren Threads synchronisiert wird.
  
## <a name="see-also"></a>Siehe auch



[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)
  
[IPSTX::GetLastError](ipstx-getlasterror.md)

