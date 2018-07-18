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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ff748827950c79c3c94e9f70ce8b0bb335884290
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792605"
---
# <a name="imsgserviceadminrenamemsgservice"></a>IMsgServiceAdmin::RenameMsgService

  
  
**Betrifft**: Outlook 
  
Veraltet. Weist einen neuen Namen zu einem Nachrichtendienst. 
  
```cpp
HRESULT RenameMsgService(
  LPMAPIUID lpUID,
  ULONG ulFlags,
  LPSTR lpszDisplayName
);
```

## <a name="parameters"></a>Parameter

 _lpUID_
  
> [in] Ein Zeiger auf die [MAPIUID](mapiuid.md) -Struktur, die den eindeutigen Bezeichner für den Dienst zum Umbenennen enthält. 
    
 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
 _lpszDisplayName_
  
> [in] Ein Zeiger auf den neuen Namen für den Dienst.
    
## <a name="return-value"></a>R�ckgabewert

MAPI_E_NO_SUPPORT 
  
> Dieser Nachrichtendienst umbenennen unterstützt MAPI nicht. Dieser Wert wird immer **RenameMsgService** zurückgegeben. 
    
## <a name="remarks"></a>Bemerkungen

Um eine Message Service einen neuen Namen zuzuweisen, sollten Clients die **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md))-Eigenschaft des Diensts Nachricht verwenden. Die Namen der Dienstanbieter in einem Nachrichtendienst werden in deren Eigenschaften **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) gespeichert. 
  
## <a name="see-also"></a>Siehe auch



[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

