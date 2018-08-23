---
title: HrDispatchNotifications
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrDispatchNotifications
api_type:
- COM
ms.assetid: 42ec4266-67b9-416e-8b9b-163c95011626
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 60c5d7e980d1dc4d4263a2be2267008dbee1fd4d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594698"
---
# <a name="hrdispatchnotifications"></a>HrDispatchNotifications

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Erzwingt abgesetzt der Benachrichtigungen an alle in der Warteschlange. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
```cpp
HRESULT HrDispatchNotifications(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Reserviert. NULL muss sein. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK
  
> Alle in der Warteschlange Benachrichtigungen haben verteilt.
    
MAPI_E_USER_CANCEL
  
> WM_QUIT, WM_QUERYENDSESSION oder WM_ENDSESSION wurde empfangen.
    
MAPI_E_NOT_INITIALIZED
  
> MAPI konnte nicht initialisiert werden.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die Funktion **HrDispatchNotifications** bewirkt, dass MAPI zu sendende alle Benachrichtigungen, die derzeit in der MAPI-Benachrichtigung Engine Warteschlange abgelegt werden ohne eine Nachricht Versendung warten. Dies kann eine wirtschaftliche Auswirkung auf die RAM-Auslastung von haben. Weitere Informationen finden Sie unter [erzwingen eine Benachrichtigung](forcing-a-notification.md). 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Einige Anwendungen warten Sie eine Benachrichtigung in einer Timeoutschleife, die mit dem Windows- [PeekMessage](http://msdn.microsoft.com/en-us/library/ms644943.aspx) und [DispatchMessage](http://msdn.microsoft.com/en-us/library/ms644934.aspx) Funktionen. Klicken Sie auf alle außer den schnellsten Plattformen können solcher Anwendungen schlechten Leistung oder sogar Blockierung der Benachrichtigungen auftreten. Mithilfe von **HrDispatchNotifications** nicht nur verringert Code, sondern wird die Leistung verbessert. 
  

