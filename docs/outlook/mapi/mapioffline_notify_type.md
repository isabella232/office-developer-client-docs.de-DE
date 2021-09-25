---
title: MAPIOFFLINE_NOTIFY_TYPE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: a111d7b7-6e87-4958-8f9b-0f2adbeb8b63
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d97c88ee27fbe0b68c7495657c77fa2ca4734e81
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59604761"
---
# <a name="mapioffline_notify_type"></a>MAPIOFFLINE_NOTIFY_TYPE

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die MAPIOFFLINE_NOTIFY_TYPE einer Benachrichtigung gibt an, ob eine Änderung des Verbindungsstatus stattfindet, stattfindet oder abgeschlossen wurde. 
  
## <a name="quick-info"></a>QuickInfo

Siehe **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**. 
  
```cpp
typedef enum { 
    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START = 1,  
    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE = 2,  
    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE = 3  
} MAPIOFFLINE_NOTIFY_TYPE;
```

## <a name="see-also"></a>Siehe auch



[Informationen zur Offlinestatus-API](about-the-offline-state-api.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)

