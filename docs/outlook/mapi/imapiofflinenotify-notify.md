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
description: 'Letzte Änderung: Montag, 25. Juni 2012'
ms.openlocfilehash: a84114a3363f9cbcd9455bce12d3171843bd18a4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571115"
---
# <a name="imapiofflinenotifynotify"></a>IMAPIOfflineNotify::Notify

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Sendet Benachrichtigungen an den Client zu den geänderten in Verbindungsstatus.
  
```cpp
void STDMETHODCALLTYPE Notify(  
    const MAPIOFFLINE_NOTIFY * pNotifyInfo 
);
```

## <a name="parameters"></a>Parameter

 _pNotifyInfo_
  
> [in] Benachrichtigung, die Outlook an den Client sendet. Die Benachrichtigung gibt den Teil des Verbindungsstatus, der geändert wurde, den alten Verbindungsstatus und den neuen Verbindungsstatus.
    
## <a name="remarks"></a>HinwBemerkungeneise

Outlook verwendet diese Methode, um die Benachrichtigung Rückrufe an einen Client gesendet. Microsoft Outlook 2010 oder Microsoft Outlook 2013 diese Schnittstelle zur Verfügung zu stellen, muss der Client diese Schnittstelle implementieren, und übergeben einen Zeiger als Mitglied in **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** beim Einrichten von Rückrufe mit **[IMAPIOfflineMgr::Advise ](imapiofflinemgr-advise.md)**. 
  
Der Client auch übergibt an **MAPIOFFLINE_ADVISEINFO** ein Clienttoken, Outlook 2010 oder Outlook 2013 verwendet in **IMAPIOfflineNotify::Notify** zum Identifizieren des Clients für den Rückruf Benachrichtigung registriert. 
  
Im Allgemeinen Outlook 2010 und Outlook 2013 können benachrichtigt werden, einem Client online/offline ändert und andere ändern, aber die Offline Zustand-API unterstützt nur Benachrichtigungen für Online-/offline geändert wird. Der Client muss alle anderen Benachrichtigungen ignorieren.
  
## <a name="see-also"></a>Siehe auch



[Informationen zu der Offlinestatus-API](about-the-offline-state-api.md)
  
[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)

