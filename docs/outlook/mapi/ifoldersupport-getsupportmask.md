---
title: IFolderSupportGetSupportMask
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IFolderSupport.GetSupportMask
api_type:
- COM
ms.assetid: 8d8aaeb7-57d7-ba4c-95d1-a5368cfc4afe
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 1c27bdc52ebe725c40cbf318fab0678f41cdc287
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417371"
---
# <a name="ifoldersupportgetsupportmask"></a>IFolderSupport::GetSupportMask

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ruft Informationen zur Unterstützung eines Ordners für die Freigabe ab.
  
```cpp
HRESULT GetSupportMask( 
    DWORD * pdwSupportMask 
); 
```

## <a name="parameters"></a>Parameter

 _pdwSupportMask_
  
> [out] Eine Bitmaske, die angibt, ob der Ordner die Freigabe unterstützt.
    
 **FS_NONE**
  
> Gibt an, dass der Ordner die Freigabe nicht unterstützt.
    
 **FS_SUPPORTS_SHARING**
  
> Gibt an, dass der Ordner die Freigabe unterstützt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf war erfolgreich.
    

