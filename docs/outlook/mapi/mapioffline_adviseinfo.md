---
title: MAPIOFFLINE_ADVISEINFO
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 20a46c69-d6ae-7d17-f8af-12952867d342
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 443644b66ba9c961992e22dbfc260fe8c48fe1b3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793126"
---
# <a name="mapiofflineadviseinfo"></a>MAPIOFFLINE_ADVISEINFO
 
**Betrifft**: Outlook 
  
Enthält Informationen zu **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)** Rückruf für ein offline-Objekt zu registrieren. 
  
## <a name="quick-info"></a>QuickInfo

Finden Sie unter **IMAPIOfflineMgr::Advise**. 
  
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

_UlSize_: die Größe des **MAPIOFFLINE_ADVISEINFO**. 
    
_UlClientToken_: ein Token vom Client über einen Rückruf definiert. Ist die *UlClientToken* Mitglied die **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)** Struktur **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)** übergeben. 
    
_CallbackType_: Typ des Rückrufs vornehmen.
    
   -  MAPIOFFLINE_CALLBACK_TYPE_NOTIFY 
    
   - Der Typ des Rückrufs ist durch Benachrichtigung. Dies ist die einzige unterstützte Art von Rückruf.  *pCallback* muss die Schnittstelle **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** anzugeben. 
    
_pCallback_: Schnittstelle für den Rückruf verwenden. Dies ist die Client-Implementierung von **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**. 
    
_UlAdviseTypes_: die Typen der Advise, wie durch die Bedingung für die mit dem Hinweis identifiziert. Der einzige unterstützte Typ ist MAPIOFFLINE_ADVISE_TYPE_STATECHANGE.
    
_UlStateMask_: der einzige unterstützte Zustand MAPIOFFLINE_STATE_ALL ist.
    
## <a name="see-also"></a>Siehe auch

- [IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)
- [Über die Offline State-API](about-the-offline-state-api.md) 
- [MAPI-Konstanten](mapi-constants.md) 
- [MAPIOFFLINE_CALLBACK_TYPE](mapioffline_callback_type.md)

