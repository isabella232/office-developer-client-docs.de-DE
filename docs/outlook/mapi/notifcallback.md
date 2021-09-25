---
title: NOTIFCALLBACK
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.NOTIFCALLBACK
api_type:
- COM
ms.assetid: 416008b4-13aa-4387-8c12-f8f2ca252391
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9eca18be8d9b6cc1db17d503edff8f121175f27a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591997"
---
# <a name="notifcallback"></a>NOTIFCALLBACK

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Definiert eine Rückruffunktion, die MAPI aufruft, um eine Ereignisbenachrichtigung zu senden. Diese Rückruffunktion kann nur verwendet werden, wenn sie in ein Empfehlungs-Senkenobjekt eingeschlossen wird, das durch Aufrufen der [HrAllocAdviseSink-Funktion](hrallocadvisesink.md) erstellt wurde. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Definierte Funktion implementiert von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
|Definierte Funktion aufgerufen von:  <br/> |MAPI  <br/> |
   
```cpp
ULONG (STDAPICALLTYPE NOTIFCALLBACK)(
  LPVOID lpvContext,
  ULONG cNotification,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a>Parameter

 _lpvContext_
  
> [in] Zeiger auf einen beliebigen Wert, der an die Rückruffunktion übergeben wird, wenn die MAPI sie aufruft. Dieser Wert kann eine Adresse darstellen, die für die Clientanwendung oder den Dienstanbieter von Bedeutung ist. In der Regel stellt der  _lpvContext-Parameter_ für C++-Code einen Zeiger auf ein C++-Objekt dar. 
    
 _cNotification_
  
> [in] Anzahl der Ereignisbenachrichtigungen im Array, das durch den  _LpNotifications-Parameter_ angegeben wird. 
    
 _LpNotifications_
  
> [out] Zeiger auf den Speicherort, an dem diese Funktion ein Array von [NOTIFICATION-Strukturen](notification.md) schreibt, die die Ereignisbenachrichtigungen enthalten. 
    
## <a name="return-value"></a>Rückgabewert

Der Satz gültiger Rückgabewerte für den **NOTIFCALLBACK-Funktionsprototyp** hängt davon ab, ob die Funktion von einer Clientanwendung oder einem Dienstanbieter implementiert wird. Clients sollten immer S_OK zurückgeben. Anbieter können entweder S_OK oder CALLBACK_DISCONTINUE zurückgeben. 
  
## <a name="remarks"></a>HinwBemerkungeneise

CALLBACK_DISCONTINUE ist nur für synchrone Rückruffunktionen ein gültiger Rückgabewert. sie fordert an, dass die MAPI die Verarbeitung der Rückrufe für diese Benachrichtigung sofort beendet. Wenn CALLBACK_DISCONTINUE zurückgegeben wird, legt MAPI den  _lpUlFlags-Parameter_ auf NOTIFY_CANCELED fest, wenn er von [IMAPISupport::Notify](imapisupport-notify.md)zurückgegeben wird. 
  
Es folgen Einschränkungen hinsichtlich der Möglichkeiten einer synchronen Rückruffunktion:
  
- Es kann nicht dazu führen, dass eine weitere synchrone Benachrichtigung generiert wird.
    
- Es kann keine Benutzeroberfläche angezeigt werden.
    
## <a name="see-also"></a>Siehe auch



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)

