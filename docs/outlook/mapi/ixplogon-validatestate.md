---
title: IXPLogonValidateState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.ValidateState
api_type:
- COM
ms.assetid: c3649daa-cba1-48e3-9ffb-069c1bcf8228
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a3469e6baacb52938b870ca87d824bf640a8a88f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351569"
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
  
> in Ein Handle für das übergeordnete Fenster aller von dieser Methode angezeigten Dialogfelder oder Fenster.
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die die Ausführung der Statusüberprüfung und die Ergebnisse der Statusüberprüfung steuert. Die folgenden Flags können festgelegt werden:
    
ABORT_XP_HEADER_OPERATION 
  
> Der Benutzer hat den Vorgang abgebrochen, indem er in einem Dialogfeld auf die Schaltfläche **Abbrechen** geklickt hat. Der Transportanbieter hat die Möglichkeit, weiterhin an dem Vorgang zu arbeiten, oder er kann den Vorgang abbrechen und MAPI_E_USER_CANCELED zurückgeben. 
    
CONFIG_CHANGED 
  
> Überprüft den Status der derzeit geladenen Transportanbieter, indem der MAPI-Spooler die [IXPLogon:: AddressTypes](ixplogon-addresstypes.md) -Methode aufruft. Dieses Flag bietet dem MAPI-Spooler außerdem die Möglichkeit, kritische Transportanbieter Fehler zu korrigieren, ohne dass Clientanwendungen sich abmelden und dann erneut anmelden müssen. 
    
FORCE_XP_CONNECT 
  
> Der Benutzer hat einen Connect-Vorgang ausgewählt. Wenn dieses Flag mit dem REFRESH_XP_HEADER_CACHE-oder PROCESS_XP_HEADER_CACHE-Flag verwendet wird, tritt die Connect-Aktion ohne Zwischenspeicherung auf.
    
FORCE_XP_DISCONNECT 
  
> Der Benutzer hat einen Disconnect-Vorgang ausgewählt. Wenn dieses Flag mit REFRESH_XP_HEADER_CACHE oder PROCESS_XP_HEADER_CACHE verwendet wird, tritt die Disconnect-Aktion ohne Zwischenspeicherung auf.
    
PROCESS_XP_HEADER_CACHE 
  
> Einträge in der Kopfzeile-Cache-Tabelle sollten verarbeitet werden, alle Nachrichten, die mit dem MSGSTATUS_REMOTE_DOWNLOAD-Flag gekennzeichnet sind, sollten heruntergeladen werden, und alle Nachrichten, die mit dem MSGSTATUS_REMOTE_DELETE-Flag gekennzeichnet sind, sollten gelöscht werden. Nachrichten, die sowohl MSGSTATUS_REMOTE_DOWNLOAD als auch MSGSTATUS_REMOTE_DELETE festgelegt haben, sollten verschoben werden.
    
REFRESH_XP_HEADER_CACHE 
  
> Eine neue Liste der Nachrichtenkopfzeilen sollte heruntergeladen werden, und alle Markierungsfahnen für den Nachrichtenstatus sollten deaktiviert werden.
    
SUPPRESS_UI 
  
> Verhindert, dass der Transportanbieter eine Benutzeroberfläche anzeigt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf war erfolgreich, und der erwartete Wert oder die Werte wurden zurückgegeben.
    
MAPI_E_BUSY 
  
> Ein anderer Vorgang wird ausgeführt; Es sollte zugelassen werden, oder es sollte beendet werden, bevor dieser Vorgang versucht wird.
    
MAPI_E_NO_SUPPORT 
  
> Der betroffene Remote Transportanbieter unterstützt keine Benutzeroberfläche, und die Clientanwendung selbst sollte das Dialogfeld anzeigen.
    
MAPI_E_USER_CANCEL 
  
> Der Benutzer hat den Vorgang abgebrochen, indem er in einem Dialogfeld auf die Schaltfläche **Abbrechen** geklickt hat. 
    
## <a name="remarks"></a>Bemerkungen

Die MAPI-Warteschlange ruft die **IXPLogon:: ValidateState** -Methode auf, um Aufrufe der [IMAPIStatus:: ValidateState](imapistatus-validatestate.md) -Methode für das Status-Objekt zu unterstützen. Der Transportanbieter sollte auf den **IXPLogon:: ValidateState** -Aufruf genau so reagieren, als ob der MAPI-Spooler ein Status-Objekt für die aktuelle Anmeldesitzung geöffnet und dann **IMAPIStatus:: ValidateState** für dieses Objekt aufgerufen hätte. 
  
Zur Unterstützung der Implementierung von **IMAPIStatus:: ValidateState**ruft der MAPI-Spooler **IXPLogon:: ValidateState** für alle Anmeldeobjekte für alle aktiven Transportanbieter auf, die in einer Profil Sitzung aktiv sind. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIStatus::ValidateState](imapistatus-validatestate.md)
  
[IXPLogon::AddressTypes](ixplogon-addresstypes.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

