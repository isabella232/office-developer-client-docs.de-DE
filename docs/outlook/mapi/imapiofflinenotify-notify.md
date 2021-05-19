---
title: IMAPIOfflineNotifyNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOfflineNotify.Notify
api_type:
- COM
ms.assetid: 10c7cb9d-2e9d-72eb-6b07-31eed892e646
description: 'Letzte �nderung: Montag, 25. Juni 2012'
ms.openlocfilehash: 4440df4b8e4a46e13748cf47d599e16599aaf858
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410693"
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
  
> [in] Die Benachrichtigung, Outlook an den Client gesendet wird. Die Benachrichtigung gibt den Teil des geänderten Verbindungsstatus, den alten Verbindungsstatus und den neuen Verbindungsstatus an.
    
## <a name="remarks"></a>Hinweise

Outlook verwendet diese Methode, um Benachrichtigungsrückrufe an einen Client zu senden. Um diese Schnittstelle für Microsoft Outlook 2010 oder Microsoft Outlook 2013 zur Verfügung zu stellen, muss der Client diese Schnittstelle implementieren und einen Zeiger als Mitglied in **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** übergeben, wenn Rückrufe mit **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)** eingerichtet werden. 
  
Der Client übergibt  außerdem MAPIOFFLINE_ADVISEINFO ein Clienttoken, das Outlook 2010 oder Outlook 2013 in **IMAPIOfflineNotify::Notify** verwendet wird, um den für den Benachrichtigungsrückruf registrierten Client zu identifizieren. 
  
Im Allgemeinen können Outlook 2010 und Outlook 2013 einen Client über Online-/Offlineänderungen und andere Verbindungsstatusänderungen benachrichtigen, die Offlinestatus-API unterstützt jedoch nur Benachrichtigungen für Online-/Offlineänderungen. Der Client muss alle anderen Benachrichtigungen ignorieren.
  
## <a name="see-also"></a>Siehe auch



[Informationen zur Offlinestatus-API](about-the-offline-state-api.md)
  
[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)

