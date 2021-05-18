---
title: IMsgServiceAdminRenameMsgService
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.RenameMsgService
api_type:
- COM
ms.assetid: eba0e7f2-03c1-4713-aa36-3d0b398cd197
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2f0f1fb94ea36512bbc40df8a4877e89d2613a25
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422103"
---
# <a name="imsgserviceadminrenamemsgservice"></a>IMsgServiceAdmin::RenameMsgService

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Veraltet. Weist einem Nachrichtendienst einen neuen Namen zu. 
  
```cpp
HRESULT RenameMsgService(
  LPMAPIUID lpUID,
  ULONG ulFlags,
  LPSTR lpszDisplayName
);
```

## <a name="parameters"></a>Parameter

 _lpUID_
  
> [in] Ein Zeiger auf die [MAPIUID-Struktur,](mapiuid.md) die den eindeutigen Bezeichner für den umzubenennenden Nachrichtendienst enthält. 
    
 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
 _lpszDisplayName_
  
> [in] Ein Zeiger auf den neuen Namen für den Nachrichtendienst.
    
## <a name="return-value"></a>Rückgabewert

MAPI_E_NO_SUPPORT 
  
> MapI unterstützt die Umbenennung dieses Nachrichtendiensts nicht. **RenameMsgService** gibt diesen Wert immer zurück. 
    
## <a name="remarks"></a>Hinweise

Um einem Nachrichtendienst einen neuen Namen zuzuordnen, sollten Clients die **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) -Eigenschaft des Nachrichtendiensts verwenden. Die Namen von Dienstanbietern in einem Nachrichtendienst werden in ihren eigenschaften **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) gespeichert. 
  
## <a name="see-also"></a>Siehe auch



[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

