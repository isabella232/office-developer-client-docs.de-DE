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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 0e2a1a582894e082722d73422fc8bafe34c4230c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334475"
---
# <a name="notifcallback"></a>NOTIFCALLBACK

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Definiert eine Rückruffunktion, die von MAPI aufgerufen wird, um eine Ereignisbenachrichtigung zu senden. Diese Rückruffunktion kann nur verwendet werden, wenn Sie in ein Advise-Senke-Objekt eingeschlossen wird, das durch Aufrufen der [HrAllocAdviseSink](hrallocadvisesink.md) -Funktion erstellt wurde. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
|Definierte Funktion, implementiert von:  <br/> |Client Anwendungen und Dienstanbieter  <br/> |
|Definierte Funktion, aufgerufen von:  <br/> |MAPI  <br/> |
   
```cpp
ULONG (STDAPICALLTYPE NOTIFCALLBACK)(
  LPVOID lpvContext,
  ULONG cNotification,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a>Parameter

 _lpvContext_
  
> in Zeiger auf einen beliebigen Wert, der beim Aufrufen von MAPI an die Rückruffunktion übergeben wird. Dieser Wert kann eine Adresse darstellen, die für die Clientanwendung oder den Dienstanbieter von Bedeutung ist. Für C++-Code stellt der Parameter _LpvContext_ in der Regel einen Zeiger auf ein c++-Objekt dar. 
    
 _cNotification_
  
> in Die Anzahl der Ereignisbenachrichtigungen im durch den _lpNotifications_ -Parameter angegebenen Array. 
    
 _lpNotifications_
  
> Out Zeiger auf den Speicherort, an dem diese Funktion ein Array [](notification.md) von Benachrichtigungs Strukturen mit den Ereignisbenachrichtigungen schreibt. 
    
## <a name="return-value"></a>Rückgabewert

Die Menge gültiger Rückgabewerte für den Prototyp der **NOTIFCALLBACK** -Funktion hängt davon ab, ob die Funktion von einer Clientanwendung oder einem Dienstanbieter implementiert wird. Clients sollten immer S_OK zurückgeben. Anbieter können S_OK oder CALLBACK_DISCONTINUE zurückgeben. 
  
## <a name="remarks"></a>Bemerkungen

CALLBACK_DISCONTINUE ist ein gültiger Rückgabewert für synchrone Rückruffunktionen; Sie fordert, dass MAPI die Verarbeitung der Rückrufe für diese Benachrichtigung sofort beendet. Wenn CALLBACK_DISCONTINUE zurückgegeben wird, wird der Parameter _lpUlFlags_ auf NOTIFY_CANCELED festgelegt, wenn er von [IMAPISupport:: notify](imapisupport-notify.md)zurückgegeben wird. 
  
Die folgenden Einschränkungen gelten für eine synchrone Rückruffunktion:
  
- Es kann keine weitere synchrone Benachrichtigung generiert werden.
    
- Eine Benutzeroberfläche kann nicht angezeigt werden.
    
## <a name="see-also"></a>Siehe auch



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)

