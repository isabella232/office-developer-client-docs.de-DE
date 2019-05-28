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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348097"
---
# <a name="hrdispatchnotifications"></a>HrDispatchNotifications

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erzwingt die Versendung aller Benachrichtigungen in der Warteschlange. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen und Dienstanbieter  <br/> |
   
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
  
> WM_QUIT, WM_QUERYENDSESSION oder WM_ENDSESSION wurde empfangen.
    
MAPI_E_NOT_INITIALIZED
  
> MAPI wurde nicht initialisiert.
    
## <a name="remarks"></a>Hinweise

Die **HrDispatchNotifications** -Funktion bewirkt, dass MAPI alle Benachrichtigungen versendet, die derzeit in der MAPI-Benachrichtigungsmodul in der Warteschlange liegen, ohne auf den Nachrichtenversand zu warten. Dies kann sich vorteilhaft auf die Speicherauslastung auswirken. Weitere Informationen finden Sie unter [Erzwingen einer Benachrichtigung](forcing-a-notification.md). 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Einige Anwendungen warten auf eine Benachrichtigungsmeldung in einer Timeout Schleife mit den Funktionen Windows [PeekMessage](https://msdn.microsoft.com/library/ms644943.aspx) und [DispatchMessage](https://msdn.microsoft.com/library/ms644934.aspx) . Auf allen, aber auf den schnellsten Plattformen können solche Anwendungen schlechte Leistung oder sogar Blockierung von Benachrichtigungen haben. Durch die Verwendung von **HrDispatchNotifications** wird nicht nur der Code reduziert, sondern auch die Leistung verbessert. 
  

