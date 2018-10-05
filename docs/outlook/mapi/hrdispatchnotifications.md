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
ms.openlocfilehash: f4af3f2fd094942c48e02849c60f3e46acb1a5f7
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385564"
---
# <a name="hrdispatchnotifications"></a>HrDispatchNotifications

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erzwingt abgesetzt der Benachrichtigungen an alle in der Warteschlange. 
  
|||
|:-----|:-----|
|Headerdatei:  <br/> |Mapiutil.h  <br/> |
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
    
## <a name="return-value"></a>Rückgabewert

S_OK
  
> Alle in der Warteschlange Benachrichtigungen haben verteilt.
    
MAPI_E_USER_CANCEL
  
> WM_QUIT, WM_QUERYENDSESSION oder WM_ENDSESSION wurde empfangen.
    
MAPI_E_NOT_INITIALIZED
  
> MAPI konnte nicht initialisiert werden.
    
## <a name="remarks"></a>Hinweise

Die Funktion **HrDispatchNotifications** bewirkt, dass MAPI zu sendende alle Benachrichtigungen, die derzeit in der MAPI-Benachrichtigung Engine Warteschlange abgelegt werden ohne eine Nachricht Versendung warten. Dies kann eine wirtschaftliche Auswirkung auf die RAM-Auslastung von haben. Weitere Informationen finden Sie unter [erzwingen eine Benachrichtigung](forcing-a-notification.md). 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Einige Anwendungen warten Sie eine Benachrichtigung in einer Timeoutschleife, die mit dem Windows- [PeekMessage](https://msdn.microsoft.com/library/ms644943.aspx) und [DispatchMessage](https://msdn.microsoft.com/library/ms644934.aspx) Funktionen. Klicken Sie auf alle außer den schnellsten Plattformen können solcher Anwendungen schlechten Leistung oder sogar Blockierung der Benachrichtigungen auftreten. Mithilfe von **HrDispatchNotifications** nicht nur verringert Code, sondern wird die Leistung verbessert. 
  

