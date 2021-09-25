---
title: IOSTXSetSyncResult
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IOSTX.SetSyncResult
api_type:
- COM
ms.assetid: 7f083ee0-bf36-0059-1589-66e454fe0098
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 664c8f3c1fdbfbdf830c16834f62220fbfe0949b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571577"
---
# <a name="iostxsetsyncresult"></a>IOSTX::SetSyncResult

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Legt das Ergebnis der Synchronisierung fest.
  
```cpp
HRESULT SetSyncResult( 
    HRESULT hrSync 
);
```

## <a name="parameters"></a>Parameter

 _hrSync_
  
>  [in] Das Ergebnis der Synchronisierung. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Rufen Sie **IOSTX::SetSyncResult** vor dem Aufrufen von **IOSTX::SyncEnd** auf, um den lokalen Speicher über das Ergebnis der Synchronisierung zu informieren. 
  
## <a name="see-also"></a>Siehe auch



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)


[MAPI-Konstanten](mapi-constants.md)

