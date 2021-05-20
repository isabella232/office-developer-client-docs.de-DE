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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439485"
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
  
> [in] Ein Handle zum übergeordneten Fenster aller Dialogfelder oder Fenster, die von dieser Methode angezeigt werden.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie die Statusüberprüfung durchgeführt wird, und die Ergebnisse der Statusüberprüfung. Die folgenden Kennzeichen können festgelegt werden:
    
ABORT_XP_HEADER_OPERATION 
  
> Der Benutzer hat den Vorgang abgebrochen, in der Regel durch Klicken auf die **Schaltfläche** Abbrechen in einem Dialogfeld. Der Transportanbieter kann weiterhin an dem Vorgang arbeiten, oder er kann den Vorgang abbrechen und MAPI_E_USER_CANCELED. 
    
CONFIG_CHANGED 
  
> Überprüft den Status der derzeit geladenen Transportanbieter, indem der MAPI-Spooler seine [IXPLogon::AddressTypes-Methode aufruft.](ixplogon-addresstypes.md) Dieses Flag bietet dem MAPI-Spooler auch die Möglichkeit, kritische Fehler des Transportanbieters zu beheben, ohne clientanwendungen zum Abmelden und anschließenden erneuten Anmelden zu zwingen. 
    
FORCE_XP_CONNECT 
  
> Der Benutzer hat einen Verbindungsvorgang ausgewählt. Wenn dieses Flag mit dem REFRESH_XP_HEADER_CACHE- oder PROCESS_XP_HEADER_CACHE verwendet wird, erfolgt die Verbindungsaktion ohne Zwischenspeicherung.
    
FORCE_XP_DISCONNECT 
  
> Der Benutzer hat einen Verbindungstrennungsvorgang ausgewählt. Wenn dieses Flag mit REFRESH_XP_HEADER_CACHE oder PROCESS_XP_HEADER_CACHE verwendet wird, erfolgt die Verbindungstrennungsaktion ohne Zwischenspeicherung.
    
PROCESS_XP_HEADER_CACHE 
  
> Einträge in der Kopfzeilencachetabelle sollten verarbeitet werden, alle nachrichten, die mit dem flag MSGSTATUS_REMOTE_DOWNLOAD gekennzeichnet sind, heruntergeladen werden, und alle Nachrichten, die mit dem MSGSTATUS_REMOTE_DELETE gekennzeichnet sind, sollten gelöscht werden. Nachrichten, die sowohl MSGSTATUS_REMOTE_DOWNLOAD als auch MSGSTATUS_REMOTE_DELETE festgelegt sind, sollten verschoben werden.
    
REFRESH_XP_HEADER_CACHE 
  
> Eine neue Liste von Nachrichtenkopfzeilen sollte heruntergeladen werden, und alle Kennzeichnungskennzeichen für nachrichtenstatus sollten entfernt werden.
    
SUPPRESS_UI 
  
> Verhindert, dass vom Transportanbieter eine Benutzeroberfläche angezeigt wird.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf war erfolgreich und hat den erwarteten Wert oder die erwarteten Werte zurückgegeben.
    
MAPI_E_BUSY 
  
> Ein weiterer Vorgang wird ausgeführt. Sie sollte abgeschlossen sein oder beendet werden, bevor dieser Vorgang versucht wird.
    
MAPI_E_NO_SUPPORT 
  
> Der beteiligte Remotetransportanbieter unterstützt keine Benutzeroberfläche, und die Clientanwendung selbst sollte das Dialogfeld anzeigen.
    
MAPI_E_USER_CANCEL 
  
> Der Benutzer hat den Vorgang abgebrochen, in der Regel durch Klicken auf die **Schaltfläche** Abbrechen in einem Dialogfeld. 
    
## <a name="remarks"></a>Hinweise

Der MAPI-Spooler ruft die **IXPLogon::ValidateState-Methode** auf, um Aufrufe der [IMAPIStatus::ValidateState-Methode](imapistatus-validatestate.md) für das Statusobjekt zu unterstützen. Der Transportanbieter sollte auf den **IXPLogon::ValidateState-Aufruf** genauso reagieren, als ob der MAPI-Spooler ein Statusobjekt für die aktuelle Anmeldesitzung geöffnet und dann **IMAPIStatus::ValidateState für** dieses Objekt aufgerufen hätte. 
  
Zur Unterstützung der Implementierung von **IMAPIStatus::ValidateState** ruft der MAPI-Spooler **IXPLogon::ValidateState** für alle Anmeldeobjekte für alle aktiven Transportanbieter auf, die in einer Profilsitzung ausgeführt werden. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIStatus::ValidateState](imapistatus-validatestate.md)
  
[IXPLogon::AddressTypes](ixplogon-addresstypes.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

