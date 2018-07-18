---
title: IOSTXSetSyncResult
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.SetSyncResult
api_type:
- COM
ms.assetid: 7f083ee0-bf36-0059-1589-66e454fe0098
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 74a4e299da6c0637c3da70c329569266d43dbd9a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792709"
---
# <a name="iostxsetsyncresult"></a>IOSTX::SetSyncResult

  
  
**Betrifft**: Outlook 
  
Das Ergebnis der Synchronisierung festgelegt.
  
```cpp
HRESULT SetSyncResult( 
    HRESULT hrSync 
);
```

## <a name="parameters"></a>Parameter

 _hrSync_
  
>  [in] Das Ergebnis der Synchronisierung. 
    
## <a name="remarks"></a>Bemerkungen

Rufen Sie **IOSTX::SetSyncResult** vor **IOSTX::SyncEnd** , um den lokalen Speicher des Ergebnisses der Synchronisierung zu informieren. 
  
## <a name="see-also"></a>Siehe auch



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)


[MAPI-Konstanten](mapi-constants.md)

