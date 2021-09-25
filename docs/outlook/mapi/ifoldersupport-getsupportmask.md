---
title: IFolderSupportGetSupportMask
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IFolderSupport.GetSupportMask
api_type:
- COM
ms.assetid: 8d8aaeb7-57d7-ba4c-95d1-a5368cfc4afe
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f337f93393766d6a456d5659b8f1cee13d23a299
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600960"
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
  
> Der Anruf war erfolgreich.
    

