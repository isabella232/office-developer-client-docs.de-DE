---
title: IMsgServiceAdminRenameMsgService
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMsgServiceAdmin.RenameMsgService
api_type:
- COM
ms.assetid: eba0e7f2-03c1-4713-aa36-3d0b398cd197
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 0018833c991a62ac11b50682b49a55a3dc97e70b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551247"
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
  
> [in] Ein Zeiger auf die [MAPIUID-Struktur,](mapiuid.md) die den eindeutigen Bezeichner enthält, den der Nachrichtendienst umbenennen soll. 
    
 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
 _lpszDisplayName_
  
> [in] Ein Zeiger auf den neuen Namen für den Nachrichtendienst.
    
## <a name="return-value"></a>Rückgabewert

MAPI_E_NO_SUPPORT 
  
> MapI unterstützt das Umbenennen dieses Nachrichtendiensts nicht. **RenameMsgService** gibt immer diesen Wert zurück. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Um einem Nachrichtendienst einen neuen Namen zuzuweisen, sollten Clients die **eigenschaft PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) des Nachrichtendiensts verwenden. Die Namen von Dienstanbietern in einem Nachrichtendienst werden in ihren **PR_DISPLAY_NAME** -[PidTagDisplayName](pidtagdisplayname-canonical-property.md)) -Eigenschaften gespeichert. 
  
## <a name="see-also"></a>Siehe auch



[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

