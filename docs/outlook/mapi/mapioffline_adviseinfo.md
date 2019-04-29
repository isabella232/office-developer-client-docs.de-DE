---
title: MAPIOFFLINE_ADVISEINFO
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 20a46c69-d6ae-7d17-f8af-12952867d342
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3cb110fdcbbd88e494c44ba2ed73cc26674638ca
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420024"
---
# <a name="mapiofflineadviseinfo"></a>MAPIOFFLINE_ADVISEINFO
 
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält Informationen zu **[IMAPIOfflineMgr:: Advise](imapiofflinemgr-advise.md)** to Register Callback for an Offline Object. 
  
## <a name="quick-info"></a>QuickInfo

Weitere Informationen finden Sie unter **IMAPIOfflineMgr:: Advise**. 
  
```cpp
typedef struct 
{ 
      ULONG                   ulSize; 
      ULONG                   ulClientToken; 
      MAPIOFFLINE_CALLBACK_TYPE     CallbackType; 
      IUnknown*               pCallback; 
      ULONG                   ulAdviseTypes; 
      ULONG                   ulStateMask; 
} MAPIOFFLINE_ADVISEINFO;
```

## <a name="members"></a>Members

_ulSize_: die Größe von **MAPIOFFLINE_ADVISEINFO**. 
    
_ulClientToken_: ein vom Client definiertes Token zu einem Rückruf. Es ist das *ulClientToken* -Element der **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)** -Struktur, die an **[IMAPIOfflineNotify:: notify](imapiofflinenotify-notify.md)** übergeben wird. 
    
_CallbackType_: Typ des anzulegenden Rückrufs.
    
   -  MAPIOFFLINE_CALLBACK_TYPE_NOTIFY 
    
   - Der Rückruftyp erfolgt per Benachrichtigung. Dies ist der einzige unterstützte Rückruftyp.  *pCallback* muss die Schnittstelle **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**. 
    
_pCallback_: Schnittstelle für Rückruf. Dies ist die Implementierung von **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** durch den Client. 
    
_ulAdviseTypes_: die Art der Beratung, wie durch die Bedingung für die Beratung identifiziert. Der einzige unterstützte Typ ist MAPIOFFLINE_ADVISE_TYPE_STATECHANGE.
    
_ulStateMask_: der einzige unterstützte Status ist MAPIOFFLINE_STATE_ALL.
    
## <a name="see-also"></a>Siehe auch

- [IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)
- [Informationen zur Offlinestatus-API](about-the-offline-state-api.md) 
- [MAPI-Konstanten](mapi-constants.md) 
- [MAPIOFFLINE_CALLBACK_TYPE](mapioffline_callback_type.md)

