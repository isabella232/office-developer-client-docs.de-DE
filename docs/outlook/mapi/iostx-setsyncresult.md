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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f8982bafc0678378ae46dc31a9417cc11bb695a7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563072"
---
# <a name="iostxsetsyncresult"></a>IOSTX::SetSyncResult

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Das Ergebnis der Synchronisierung festgelegt.
  
```cpp
HRESULT SetSyncResult( 
    HRESULT hrSync 
);
```

## <a name="parameters"></a>Parameter

 _hrSync_
  
>  [in] Das Ergebnis der Synchronisierung. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Rufen Sie **IOSTX::SetSyncResult** vor **IOSTX::SyncEnd** , um den lokalen Speicher des Ergebnisses der Synchronisierung zu informieren. 
  
## <a name="see-also"></a>Siehe auch



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)


[MAPI-Konstanten](mapi-constants.md)

