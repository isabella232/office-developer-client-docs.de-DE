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
ms.openlocfilehash: c51f4a7266e67be08f31daa5afbf23ce0b256252
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567853"
---
# <a name="ifoldersupportgetsupportmask"></a>IFolderSupport::GetSupportMask

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Ruft Informationen über die Unterstützung für einen Ordner für die Freigabe.
  
```cpp
HRESULT GetSupportMask( 
    DWORD * pdwSupportMask 
); 
```

## <a name="parameters"></a>Parameter

 _pdwSupportMask_
  
> [out] Gibt an, ob der Ordner Freigabe unterstützt eine Bitmaske dar.
    
 **FS_NONE**
  
> Gibt an, dass der Ordner Freigabe nicht unterstützt.
    
 **FS_SUPPORTS_SHARING**
  
> Gibt an, dass der Ordner Freigabe unterstützt.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf war erfolgreich.
    

