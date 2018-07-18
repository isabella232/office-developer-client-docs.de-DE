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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 28afa338b37e747ed441a8767981b7e63808e741
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791918"
---
# <a name="hrdispatchnotifications"></a>HrDispatchNotifications

  
  
**Betrifft**: Outlook 
  
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
    
## <a name="remarks"></a>Bemerkungen

Die Funktion **HrDispatchNotifications** bewirkt, dass MAPI zu sendende alle Benachrichtigungen, die derzeit in der MAPI-Benachrichtigung Engine Warteschlange abgelegt werden ohne eine Nachricht Versendung warten. Dies kann eine wirtschaftliche Auswirkung auf die RAM-Auslastung von haben. Weitere Informationen finden Sie unter [erzwingen eine Benachrichtigung](forcing-a-notification.md). 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Einige Anwendungen warten Sie eine Benachrichtigung in einer Timeoutschleife, die mit dem Windows- [PeekMessage](http://msdn.microsoft.com/en-us/library/ms644943.aspx) und [DispatchMessage](http://msdn.microsoft.com/en-us/library/ms644934.aspx) Funktionen. Klicken Sie auf alle außer den schnellsten Plattformen können solcher Anwendungen schlechten Leistung oder sogar Blockierung der Benachrichtigungen auftreten. Mithilfe von **HrDispatchNotifications** nicht nur verringert Code, sondern wird die Leistung verbessert. 
  

