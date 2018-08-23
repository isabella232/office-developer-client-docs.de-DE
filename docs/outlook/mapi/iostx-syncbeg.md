---
title: IOSTXSyncBeg
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.SyncBeg
api_type:
- COM
ms.assetid: 4a935df3-98c4-2742-206e-4e16eda7b9bc
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 37d37d6402b165ea57626fe4791cfb1a4bcf76cc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565116"
---
# <a name="iostxsyncbeg"></a>IOSTX::SyncBeg

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Bereitet den lokalen Speicher für die Synchronisierung in einen bestimmten Status und die erforderliche Informationen zum Replizieren von abgerufen.
  
```cpp
HRESULT SyncBeg( 
    UINT uiSync, 
    LPVOID *ppv 
);
```

## <a name="parameters"></a>Parameter

 _uiSync_
  
>  [in] Der Zustand, den der lokale Speicher eingeben möchten. Es folgt eine Liste mit IDs Status: 
    
LR_SYNC_IDLE
  
> 
    
LR_SYNC
  
> 
    
LR_SYNC_UPLOAD_HIERARCHY
  
> 
    
LR_SYNC_UPLOAD_FOLDER
  
> 
    
LR_SYNC_CONTENTS
  
> 
    
LR_SYNC_UPLOAD_TABLE
  
> 
    
LR_SYNC_UPLOAD_MESSAGE
  
> 
    
LR_SYNC_UPLOAD_MESSAGE_READ
  
> 
    
LR_SYNC_UPLOAD_MESSAGE_DEL
  
> 
    
LR_SYNC_DOWNLOAD_HIERARCHY
  
> 
    
LR_SYNC_DOWNLOAD_TABLE
  
> 
    
 _ppv_
  
>  [in] / [out] Zeiger auf die Datenstruktur, die den Status entspricht eingeben. 
    
[DNHIER](dnhier.md)
  
> 
    
[DNTBL](dntbl.md)
  
> 
    
[DNTBL](dntbl.md)
  
> 
    
[SYNC](sync.md)
  
> 
    
[SYNCCONT](synccont.md)
  
> 
    
[UPDEL](updel.md)
  
> 
    
[UPDELE](updele.md)
  
> 
    
[UPFLD](upfld.md)
  
> 
    
[UPHIER](uphier.md)
  
> 
    
[UPMOV](upmov.md)
  
> 
    
[UPMSG](upmsg.md)
  
> 
    
[UPREAD](upread.md)
  
> 
    
[UPREADE](upreade.md)
  
> 
    
[UPTBL](uptbl.md)
  
> 
    
[UPTBLE](uptble.md)
  
> 
    
## <a name="remarks"></a>HinwBemerkungeneise

Der Client ruft **[IOSTX::SetSyncResult](iostx-setsyncresult.md)** , um das Ergebnis der Synchronisierung festzulegen, und ruft dann **[IOSTX::SyncEnd](iostx-syncend.md)** , um diesen Zustand zu beenden. Der Client muss **[IOSTX::SyncEnd](iostx-syncend.md)** für jeden Anruf, um zu bestimmen, ob der Zustand erfolgreich repliziert wurde, **IOSTX::SyncBeg** aufrufen. Nachdem dies ermittelt wurde, kann Outlook beginnen, bereinigen Sie den internen Zustand. 
  
Die meisten dieser Strukturen enthalten [out] / [in] Informationen, sodass Outlook zum Übergeben von Informationen an den Client und Client zum Übergeben von Informationen an Outlook. Wenn der Client **IOSTX::SyncBeg**aufruft, Outlook weist die Datenstruktur für einen bestimmten Status und mit Informationen für diesen Zustand initialisiert. Dies ist die [Out] Informationen. Klicken Sie in einem Zustand befindet, aktualisiert den Client Datenstruktur des entsprechenden für diesen Zustand. Dies ist die [in] Informationen. 
  
## <a name="see-also"></a>Siehe auch



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[MAPI-Konstanten](mapi-constants.md)

