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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6f7aa23606da40c817c9af623b8bade9383ce427
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792059"
---
# <a name="ifoldersupportgetsupportmask"></a>IFolderSupport::GetSupportMask

  
  
**Betrifft**: Outlook 
  
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
    

