---
title: IMAPIOfflineNotifyNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIOfflineNotify.Notify
api_type:
- COM
ms.assetid: 10c7cb9d-2e9d-72eb-6b07-31eed892e646
description: 'Letzte �nderung: Montag, 25. Juni 2012'
ms.openlocfilehash: 42c31247ad9c6445ddbe465539a2f35c6c601ea1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575897"
---
# <a name="imapiofflinenotifynotify"></a>IMAPIOfflineNotify::Notify

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Sendet Benachrichtigungen über Änderungen im Verbindungsstatus an den Client.
  
```cpp
void STDMETHODCALLTYPE Notify(  
    const MAPIOFFLINE_NOTIFY * pNotifyInfo 
);
```

## <a name="parameters"></a>Parameter

 _pNotifyInfo_
  
> [in] Die Benachrichtigung, die Outlook an den Client sendet. Die Benachrichtigung gibt den Teil des Geänderten Verbindungsstatus, den alten Verbindungsstatus und den neuen Verbindungsstatus an.
    
## <a name="remarks"></a>HinwBemerkungeneise

Outlook verwendet diese Methode, um Benachrichtigungsrückrufe an einen Client zu senden. Um diese Schnittstelle Microsoft Outlook 2010 oder Microsoft Outlook 2013 zur Verfügung zu stellen, muss der Client diese Schnittstelle implementieren und einen Zeiger als Mitglied in **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** übergeben, wenn Rückrufe mit **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)** eingerichtet werden. 
  
Der Client übergibt auch an **MAPIOFFLINE_ADVISEINFO** ein Clienttoken, das Outlook 2010 oder Outlook 2013 in **IMAPIOfflineNotify::Notify** verwendet, um den für den Benachrichtigungsrückruf registrierten Client zu identifizieren. 
  
Im Allgemeinen können Outlook 2010 und Outlook 2013 einen Client über Online-/Offlineänderungen und andere Verbindungsstatusänderungen benachrichtigen, aber die Offlinestatus-API unterstützt nur Benachrichtigungen für Online-/Offlineänderungen. Der Client muss alle anderen Benachrichtigungen ignorieren.
  
## <a name="see-also"></a>Siehe auch



[Informationen zur Offlinestatus-API](about-the-offline-state-api.md)
  
[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)

