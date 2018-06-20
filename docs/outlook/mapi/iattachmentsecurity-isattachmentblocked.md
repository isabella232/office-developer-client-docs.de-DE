---
title: IAttachmentSecurityIsAttachmentBlocked
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAttachmentSecurity.IsAttachmentBlocked
api_type:
- COM
ms.assetid: 6986d27a-9602-e44a-0797-4c47f2184ef7
description: 'Letzte �nderung: Montag, 25. Juni 2012'
ms.openlocfilehash: 45e4362fc025c1784e9432c5d641e865a044bd00
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792034"
---
# <a name="iattachmentsecurityisattachmentblocked"></a>IAttachmentSecurity::IsAttachmentBlocked

  
  
**Betrifft**: Outlook 
  
Überprüft, ob eine angegebene Anlage zum Anzeigen und Indizieren von Microsoft Outlook 2010 oder Microsoft Outlook 2013 ausgeschlossen wird.
  
```cpp
HRESULT IAttachmentSecurity::IsAttachmentBlocked( 
    LPCWSTR pwszFileName,  
    BOOL *pfBlocked 
);
```

## <a name="parameters"></a>Parameter

 _pwszFileName_
  
> [in] Zeiger auf den Dateinamen der Anlage.
    
 _pfBlocked_
  
> [out] Zeiger auf einen Wert angibt, **true,** Wenn die angegebene Anlage blockiert wird; anderenfalls **false**.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Konstanten](mapi-constants.md)
  
[Stellen Sie sicher, dass eine Anlage gesperrt ist](how-to-verify-an-attachment-is-blocked.md)

