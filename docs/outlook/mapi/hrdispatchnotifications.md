---
title: HrDispatchNotifications
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.HrDispatchNotifications
api_type:
- COM
ms.assetid: 42ec4266-67b9-416e-8b9b-163c95011626
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c528826d8a05b6a608c0a9e50d882baf8956e682
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561656"
---
# <a name="hrdispatchnotifications"></a>HrDispatchNotifications

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erzwingt die Verteilung aller Benachrichtigungen in der Warteschlange. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
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
  
> Alle Benachrichtigungen in der Warteschlange wurden gesendet.
    
MAPI_E_USER_CANCEL
  
> WM_QUIT, WM_QUERYENDSESSION oder WM_ENDSESSION empfangen wurde.
    
MAPI_E_NOT_INITIALIZED
  
> MAPI wurde nicht initialisiert.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **HrDispatchNotifications-Funktion** bewirkt, dass die MAPI alle Benachrichtigungen verteilt, die derzeit im MAPI-Benachrichtigungsmodul in die Warteschlange eingereiht sind, ohne auf einen Nachrichtenversand zu warten. Dies kann sich positiv auf die Speicherauslastung auswirken. Weitere Informationen finden Sie unter [Erzwingen einer Benachrichtigung.](forcing-a-notification.md) 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Einige Anwendungen warten mithilfe der Funktionen Windows [PeekMessage](https://msdn.microsoft.com/library/ms644943.aspx) und [DispatchMessage](https://msdn.microsoft.com/library/ms644934.aspx) auf eine Benachrichtigung in einer Timeoutschleife. Auf allen Plattformen außer den schnellsten Plattformen können solche Anwendungen eine schlechte Leistung oder sogar Benachrichtigungen blockieren. Die Verwendung von **HrDispatchNotifications** reduziert nicht nur Code, sondern verbessert auch die Leistung. 
  

