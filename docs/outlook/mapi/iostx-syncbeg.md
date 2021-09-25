---
title: IOSTXSyncBeg
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IOSTX.SyncBeg
api_type:
- COM
ms.assetid: 4a935df3-98c4-2742-206e-4e16eda7b9bc
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b35d5a55a61620cbc829da2640c3a3f588584b84
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59613898"
---
# <a name="iostxsyncbeg"></a>IOSTX::SyncBeg

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bereitet den lokalen Speicher für die Synchronisierung in einem bestimmten Zustand vor und ruft die erforderlichen Informationen zum Replizieren ab.
  
```cpp
HRESULT SyncBeg( 
    UINT uiSync, 
    LPVOID *ppv 
);
```

## <a name="parameters"></a>Parameter

 _uiSync_
  
>  [in] Der Zustand, den der lokale Speicher eingibt. Es folgt eine Liste der Statusidentifer: 
    
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
    
 _Ppv_
  
>  [in]/[out] Zeiger auf die Datenstruktur, die dem einzugebenden Zustand entspricht. 
    
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
    
## <a name="remarks"></a>Bemerkungen

Der Client ruft **[IOSTX::SetSyncResult](iostx-setsyncresult.md)** auf, um das Ergebnis der Synchronisierung festzulegen, und ruft dann **[IOSTX::SyncEnd](iostx-syncend.md)** auf, um diesen Zustand zu beenden. Der Client muss **[IOSTX::SyncEnd](iostx-syncend.md)** für jeden Aufruf von **IOSTX::SyncBeg** aufrufen, um festzustellen, ob der Status erfolgreich repliziert wurde. Sobald dies ermittelt wurde, können Outlook mit der Bereinigung des internen Zustands beginnen. 
  
Die meisten dieser Strukturen enthalten [out]/[in]-Informationen, sodass Outlook Informationen an den Client übergeben können, und der Client informationen an Outlook übergeben kann. Wenn der Client **IOSTX::SyncBeg aufruft,** ordnet Outlook die Datenstruktur für einen bestimmten Zustand zu und initialisiert sie mit Informationen für diesen Zustand. Dies sind die [out]-Informationen. In einem Zustand aktualisiert der Client die entsprechende Datenstruktur für diesen Zustand. Dies sind die [in]-Informationen. 
  
## <a name="see-also"></a>Siehe auch



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[MAPI-Konstanten](mapi-constants.md)

