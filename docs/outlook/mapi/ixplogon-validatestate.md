---
title: IXPLogonValidateState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IXPLogon.ValidateState
api_type:
- COM
ms.assetid: c3649daa-cba1-48e3-9ffb-069c1bcf8228
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4da8ae8d05a06c6e377d48a42298e74724674d5e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561306"
---
# <a name="ixplogonvalidatestate"></a>IXPLogon::ValidateState

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Überprüft den externen Status des Transportanbieters. 
  
```cpp
HRESULT ValidateState(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _ulUIParam_
  
> [in] Ein Handle für das übergeordnete Fenster aller Dialogfelder oder Fenster, die von dieser Methode angezeigt werden.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie die Statusüberprüfung durchgeführt wird, und die Ergebnisse der Statusüberprüfung. Die folgenden Flags können festgelegt werden:
    
ABORT_XP_HEADER_OPERATION 
  
> Der Benutzer hat den Vorgang abgebrochen, in der Regel durch Klicken auf die Schaltfläche **Abbrechen** in einem Dialogfeld. Der Transportanbieter hat die Möglichkeit, den Vorgang fortzusetzen, oder er kann den Vorgang abbrechen und MAPI_E_USER_CANCELED zurückgeben. 
    
CONFIG_CHANGED 
  
> Überprüft den Status der aktuell geladenen Transportanbieter, indem der MAPI-Spooler die [IXPLogon::AddressTypes-Methode aufruft.](ixplogon-addresstypes.md) Dieses Flag bietet dem MAPI-Spooler auch die Möglichkeit, kritische Transportanbieterfehler zu beheben, ohne dass Clientanwendungen gezwungen werden, sich abzumelden und sich dann erneut anzumelden. 
    
FORCE_XP_CONNECT 
  
> Der Benutzer hat einen Verbindungsvorgang ausgewählt. Wenn dieses Flag mit dem flag REFRESH_XP_HEADER_CACHE oder PROCESS_XP_HEADER_CACHE verwendet wird, wird die Verbindungsaktion ohne Zwischenspeicherung ausgeführt.
    
FORCE_XP_DISCONNECT 
  
> Der Benutzer hat einen Vorgang zum Trennen ausgewählt. Wenn dieses Flag mit REFRESH_XP_HEADER_CACHE oder PROCESS_XP_HEADER_CACHE verwendet wird, erfolgt die Trennungsaktion ohne Zwischenspeicherung.
    
PROCESS_XP_HEADER_CACHE 
  
> Einträge in der Headercachetabelle sollten verarbeitet werden, alle mit dem MSGSTATUS_REMOTE_DOWNLOAD Flag gekennzeichneten Nachrichten sollten heruntergeladen werden, und alle Nachrichten, die mit dem MSGSTATUS_REMOTE_DELETE Flag gekennzeichnet sind, sollten gelöscht werden. Nachrichten, für die sowohl MSGSTATUS_REMOTE_DOWNLOAD als auch MSGSTATUS_REMOTE_DELETE festgelegt sind, sollten verschoben werden.
    
REFRESH_XP_HEADER_CACHE 
  
> Eine neue Liste der Nachrichtenkopfzeilen sollte heruntergeladen werden, und alle Flags für die Nachrichtenstatuskennzeichnung sollten gelöscht werden.
    
SUPPRESS_UI 
  
> Verhindert, dass der Transportanbieter eine Benutzeroberfläche anzeigt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf war erfolgreich und hat den erwarteten Wert oder die erwarteten Werte zurückgegeben.
    
MAPI_E_BUSY 
  
> Ein weiterer Vorgang wird ausgeführt. Er sollte abgeschlossen werden können, oder er sollte beendet werden, bevor dieser Vorgang versucht wird.
    
MAPI_E_NO_SUPPORT 
  
> Der betroffene Remotetransportanbieter unterstützt keine Benutzeroberfläche, und die Clientanwendung selbst sollte das Dialogfeld anzeigen.
    
MAPI_E_USER_CANCEL 
  
> Der Benutzer hat den Vorgang abgebrochen, in der Regel durch Klicken auf die Schaltfläche **Abbrechen** in einem Dialogfeld. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Der MAPI-Spooler ruft die **IXPLogon::ValidateState-Methode** auf, um Aufrufe der [IMAPIStatus::ValidateState-Methode](imapistatus-validatestate.md) für das Statusobjekt zu unterstützen. Der Transportanbieter sollte auf den **IXPLogon::ValidateState-Aufruf** genau so reagieren, als ob der MAPI-Spooler ein Statusobjekt für die aktuelle Anmeldesitzung geöffnet und dann **IMAPIStatus::ValidateState** für dieses Objekt aufgerufen hätte. 
  
Zur Unterstützung der Implementierung von **IMAPIStatus::ValidateState** ruft der MAPI-Spooler **IXPLogon::ValidateState** für alle Anmeldeobjekte für alle aktiven Transportanbieter auf, die in einer Profilsitzung ausgeführt werden. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIStatus::ValidateState](imapistatus-validatestate.md)
  
[IXPLogon::AddressTypes](ixplogon-addresstypes.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

