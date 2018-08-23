---
title: MAPIOFFLINE_NOTIFY_TYPE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a111d7b7-6e87-4958-8f9b-0f2adbeb8b63
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e7120b843eae8df70cb2c4f9cbf581dcf0e09c11
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566887"
---
# <a name="mapiofflinenotifytype"></a>MAPIOFFLINE_NOTIFY_TYPE

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Die MAPIOFFLINE_NOTIFY_TYPE einer Benachrichtigung gibt an, ob eine Änderung in den Verbindungsstatus ist stattfinden soll, erfolgt oder abgeschlossen ist. 
  
## <a name="quick-info"></a>QuickInfo

Finden Sie unter **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**. 
  
```cpp
typedef enum { 
    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START = 1,  
    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE = 2,  
    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE = 3  
} MAPIOFFLINE_NOTIFY_TYPE;
```

## <a name="see-also"></a>Siehe auch



[Informationen zu der Offlinestatus-API](about-the-offline-state-api.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)

