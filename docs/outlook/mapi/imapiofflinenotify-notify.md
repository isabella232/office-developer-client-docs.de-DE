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
ms.openlocfilehash: 54843339c6843e075ec769da5751ae2fe753f302
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792267"
---
# <a name="imapiofflinenotifynotify"></a>IMAPIOfflineNotify::Notify

  
  
**Betrifft**: Outlook 
  
Sendet Benachrichtigungen an den Client zu den geänderten in Verbindungsstatus.
  
```cpp
void STDMETHODCALLTYPE Notify(  
    const MAPIOFFLINE_NOTIFY * pNotifyInfo 
);
```

## <a name="parameters"></a>Parameter

 _pNotifyInfo_
  
> [in] Benachrichtigung, die Outlook an den Client sendet. Die Benachrichtigung gibt den Teil des Verbindungsstatus, der geändert wurde, den alten Verbindungsstatus und den neuen Verbindungsstatus.
    
## <a name="remarks"></a>Bemerkungen

Outlook verwendet diese Methode, um die Benachrichtigung Rückrufe an einen Client gesendet. Microsoft Outlook 2010 oder Microsoft Outlook 2013 diese Schnittstelle zur Verfügung zu stellen, muss der Client diese Schnittstelle implementieren, und übergeben einen Zeiger als Mitglied in **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** beim Einrichten von Rückrufe mit **[IMAPIOfflineMgr::Advise ](imapiofflinemgr-advise.md)**. 
  
Der Client auch übergibt an **MAPIOFFLINE_ADVISEINFO** ein Clienttoken, Outlook 2010 oder Outlook 2013 verwendet in **IMAPIOfflineNotify::Notify** zum Identifizieren des Clients für den Rückruf Benachrichtigung registriert. 
  
Im Allgemeinen Outlook 2010 und Outlook 2013 können benachrichtigt werden, einem Client online/offline ändert und andere ändern, aber die Offline Zustand-API unterstützt nur Benachrichtigungen für Online-/offline geändert wird. Der Client muss alle anderen Benachrichtigungen ignorieren.
  
## <a name="see-also"></a>Siehe auch



[Informationen zu der Offlinestatus-API](about-the-offline-state-api.md)
  
[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)

