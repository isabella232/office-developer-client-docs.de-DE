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
description: 'Letzte Änderung: Montag, 25. Juni 2012'
ms.openlocfilehash: ff13866139bf422f071eaba2c146aa1140ccd1ab
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565046"
---
# <a name="iattachmentsecurityisattachmentblocked"></a>IAttachmentSecurity::IsAttachmentBlocked

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
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
  
[Überprüfen, ob eine Anlage blockiert ist](how-to-verify-an-attachment-is-blocked.md)

