---
title: IAttachmentSecurityIsAttachmentBlocked
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IAttachmentSecurity.IsAttachmentBlocked
api_type:
- COM
ms.assetid: 6986d27a-9602-e44a-0797-4c47f2184ef7
description: 'Letzte �nderung: Montag, 25. Juni 2012'
ms.openlocfilehash: 80fdb13233b4ad345c3cbef62a733df2f130d527
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580034"
---
# <a name="iattachmentsecurityisattachmentblocked"></a>IAttachmentSecurity::IsAttachmentBlocked

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Überprüft, ob eine angegebene Anlage durch Microsoft Outlook 2010 oder Microsoft Outlook 2013 zum Anzeigen und Indizieren blockiert wird.
  
```cpp
HRESULT IAttachmentSecurity::IsAttachmentBlocked( 
    LPCWSTR pwszFileName,  
    BOOL *pfBlocked 
);
```

## <a name="parameters"></a>Parameter

 _pwszFileName_
  
> [in] Zeiger auf den Dateinamen einer Anlage.
    
 _pfBlocked_
  
> [out] Zeiger auf einen Wert, der **"true"** angibt, wenn die angegebene Anlage blockiert ist; andernfalls **false**.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Konstanten](mapi-constants.md)
  
[Überprüfen, ob eine Anlage blockiert ist](how-to-verify-an-attachment-is-blocked.md)

