---
title: MAPIOFFLINE_ADVISEINFO
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 20a46c69-d6ae-7d17-f8af-12952867d342
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f501784a8939de6afd892a92ace122c44af070be
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575477"
---
# <a name="mapioffline_adviseinfo"></a>MAPIOFFLINE_ADVISEINFO
 
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Stellt Informationen für **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)** zum Registrieren des Rückrufs für ein Offlineobjekt bereit. 
  
## <a name="quick-info"></a>QuickInfo

Siehe **IMAPIOfflineMgr::Advise**. 
  
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

_ulSize_: Die Größe von **MAPIOFFLINE_ADVISEINFO**. 
    
_ulClientToken:_ Ein token, das vom Client für einen Rückruf definiert wird. Es ist das *ulClientToken-Mitglied* der **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)** Struktur, die an **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)** übergeben wird. 
    
_CallbackType:_ Typ des zu tätigenden Rückrufs.
    
   -  MAPIOFFLINE_CALLBACK_TYPE_NOTIFY 
    
   - Der Rückruftyp erfolgt über eine Benachrichtigung. Dies ist der einzige unterstützte Rückruftyp.  *pCallback*  muss die Schnittstelle **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** angeben. 
    
_pCallback:_ Schnittstelle, die für den Rückruf verwendet werden soll. Dies ist die Implementierung von **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** durch den Client. 
    
_ulAdviseTypes:_ Die Arten von Ratschlägen, wie durch die Bedingung für die Empfehlung identifiziert. Der einzige unterstützte Typ ist MAPIOFFLINE_ADVISE_TYPE_STATECHANGE.
    
_ulStateMask:_ Der einzige unterstützte Status ist MAPIOFFLINE_STATE_ALL.
    
## <a name="see-also"></a>Siehe auch

- [IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)
- [Informationen zur Offlinestatus-API](about-the-offline-state-api.md) 
- [MAPI-Konstanten](mapi-constants.md) 
- [MAPIOFFLINE_CALLBACK_TYPE](mapioffline_callback_type.md)

