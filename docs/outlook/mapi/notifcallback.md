---
title: NOTIFCALLBACK
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.NOTIFCALLBACK
api_type:
- COM
ms.assetid: 416008b4-13aa-4387-8c12-f8f2ca252391
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 17b038fea2dd1614f94f005e32b9e6ba4423dbda
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566264"
---
# <a name="notifcallback"></a>NOTIFCALLBACK

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Definiert eine Rückruffunktion, die MAPI senden eine ereignisbenachrichtigung aufruft. Diese Callback-Funktion kann nur verwendet werden, wenn in einer Advise-Empfängerobjekt erstellt durch Aufrufen der Funktion [HrAllocAdviseSink](hrallocadvisesink.md) eingeschlossen. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Definierte Funktion von implementiert:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
|Definierte Funktion aufgerufen:  <br/> |MAPI  <br/> |
   
```cpp
ULONG (STDAPICALLTYPE NOTIFCALLBACK)(
  LPVOID lpvContext,
  ULONG cNotification,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a>Parameter

 _lpvContext_
  
> [in] Zeiger auf einen beliebigen Wert wird an die Rückruffunktion übergeben, wenn MAPI aufgerufen. Dieser Wert kann eine Bedeutung für die Clientanwendung oder Dienstanbieter-Adresse dar. In der Regel stellt der _LpvContext_ -Parameter für C++-Code einen Zeiger auf ein C++-Objekt. 
    
 _cNotification_
  
> [in] Anzahl der ereignisbenachrichtigungen im Array durch den Parameter _LpNotifications_ angegeben. 
    
 _lpNotifications_
  
> [out] Zeiger auf den Speicherort, in dem diese Funktion ein Array von [Benachrichtigung](notification.md) Strukturen, schreibt, enthält die ereignisbenachrichtigungen. 
    
## <a name="return-value"></a>R�ckgabewert

Der Satz von gültigen Rückgabewerte für die **NOTIFCALLBACK** Funktionsprototyp hängt davon ab, ob die Funktion von einer Clientanwendung oder einem Dienstanbieter implementiert wird. Clients sollte immer S_OK zurück. Anbieter können S_OK oder CALLBACK_DISCONTINUE zurückgeben. 
  
## <a name="remarks"></a>HinwBemerkungeneise

CALLBACK_DISCONTINUE ist ein gültiger Rückgabewert für nur synchrone Rückruffunktionen. fordert, dass MAPI sofort Beenden der Verarbeitung der Rückrufe für diese Benachrichtigung an. Wenn CALLBACK_DISCONTINUE zurückgegeben wird, wird MAPI der _LpUlFlags_ -Parameter auf NOTIFY_CANCELED, wenn es vom [IMAPISupport::Notify](imapisupport-notify.md)zurückgibt. 
  
Im folgenden sind Einschränkungen auf was eine synchrone Callback-Funktion möglich:
  
- Es kann nicht dazu führen, dass eine andere synchrone Benachrichtigung generiert werden soll.
    
- Es kann keine Benutzeroberfläche angezeigt.
    
## <a name="see-also"></a>Siehe auch



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)

