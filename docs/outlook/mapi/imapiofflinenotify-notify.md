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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270084"
---
# <a name="imapiofflinenotifynotify"></a>IMAPIOfflineNotify::Notify

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Sendet Benachrichtigungen an den Client über Änderungen im Verbindungsstatus.
  
```cpp
void STDMETHODCALLTYPE Notify(  
    const MAPIOFFLINE_NOTIFY * pNotifyInfo 
);
```

## <a name="parameters"></a>Parameter

 _pNotifyInfo_
  
> in Die Benachrichtigung, die Outlook an den Client sendet. Die Benachrichtigung gibt den Teil des Verbindungsstatus an, der geändert wurde, den alten Verbindungsstatus und den neuen Verbindungsstatus.
    
## <a name="remarks"></a>Bemerkungen

Outlook verwendet diese Methode zum Senden von Benachrichtigungs Rückrufen an einen Client. Um diese Schnittstelle für Microsoft Outlook 2010 oder Microsoft Outlook 2013 zur Verfügung zu stellen, muss der Client diese Schnittstelle implementieren und einen Zeiger als Member in **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** beim Einrichten von Rückrufen mithilfe von **[IMAPIOfflineMgr übergeben:: Advise ](imapiofflinemgr-advise.md)**. 
  
Der Client übergibt auch an **MAPIOFFLINE_ADVISEINFO** ein Clienttoken, das Outlook 2010 oder Outlook 2013 in **IMAPIOfflineNotify:: notify** verwendet, um den für den Benachrichtigungsrückruf registrierten Client zu identifizieren. 
  
Im Allgemeinen können Outlook 2010 und Outlook 2013 einen Client über Online/Offline-Änderungen und andere Verbindungsstatusänderungen informieren, die Offlinestatus-API unterstützt jedoch nur Benachrichtigungen für Online/Offline-Änderungen. Der Client muss alle anderen Benachrichtigungen ignorieren.
  
## <a name="see-also"></a>Siehe auch



[Informationen zur Offlinestatus-API](about-the-offline-state-api.md)
  
[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)

