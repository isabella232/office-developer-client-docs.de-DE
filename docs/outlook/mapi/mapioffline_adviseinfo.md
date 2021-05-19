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
# <a name="mapioffline_adviseinfo"></a>MAPIOFFLINE_ADVISEINFO
 
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Stellt Informationen für **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)** zum Registrieren des Rückrufs für ein Offlineobjekt zur Verfügung. 
  
## <a name="quick-info"></a>QuickInfo

Weitere Informationen finden Sie unter **IMAPIOfflineMgr::Advise**. 
  
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

## <a name="members"></a>Elemente

_ulSize_: Die Größe **MAPIOFFLINE_ADVISEINFO**. 
    
_ulClientToken_: Ein vom Client definiertes Token über einen Rückruf. Es ist das *ulClientToken-Element* der **[MAPIOFFLINE_NOTIFY,](mapioffline_notify.md)** die **[an IMAPIOfflineNotify::Notify übergeben wird.](imapiofflinenotify-notify.md)** 
    
_CallbackType_: Typ des zu erstellende Rückrufs.
    
   -  MAPIOFFLINE_CALLBACK_TYPE_NOTIFY 
    
   - Der Typ des Rückrufs ist per Benachrichtigung. Dies ist der einzige unterstützte Rückruftyp.  *pCallback* muss die Schnittstelle **[IMAPIOfflineNotify angeben.](imapiofflinenotifyiunknown.md)** 
    
_pCallback_: Schnittstelle, die für Rückrufe verwendet werden soll. Dies ist die Clientimplementierung von **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**. 
    
_ulAdviseTypes_: Die Arten von Rat, die durch die Bedingung für die Beratung identifiziert werden. Der einzige unterstützte Typ ist MAPIOFFLINE_ADVISE_TYPE_STATECHANGE.
    
_ulStateMask_: Der einzige unterstützte Status ist MAPIOFFLINE_STATE_ALL.
    
## <a name="see-also"></a>Siehe auch

- [IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)
- [Informationen zur Offlinestatus-API](about-the-offline-state-api.md) 
- [MAPI-Konstanten](mapi-constants.md) 
- [MAPIOFFLINE_CALLBACK_TYPE](mapioffline_callback_type.md)

