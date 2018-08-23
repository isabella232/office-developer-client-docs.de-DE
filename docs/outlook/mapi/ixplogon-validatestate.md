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
ms.openlocfilehash: 4fd0dd02c5cf6f6a49b782d06c02e373dcfc3327
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577485"
---
# <a name="ixplogonvalidatestate"></a>IXPLogon::ValidateState

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Externe Status der Adressbuchhierarchie überprüft. 
  
```cpp
HRESULT ValidateState(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _ulUIParam_
  
> [in] Ein Handle für das übergeordnete Fenster für alle Dialogfelder oder Windows, die diese Methode anzeigt.
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die steuert, wie die statusüberprüfung ausgeführt wird und die Ergebnisse über den Status überprüfen. Die folgenden Kennzeichen können festgelegt werden:
    
ABORT_XP_HEADER_OPERATION 
  
> Der Benutzer hat den Vorgang in der Regel durch Klicken auf die Schaltfläche " **Abbrechen** " in einem Dialogfeld abgebrochen. Der Transportdienst hat die Möglichkeit, den Vorgang fortsetzen, oder den Vorgang abzubrechen und MAPI_E_USER_CANCELED zurückgeben kann. 
    
CONFIG_CHANGED 
  
> Überprüft den Status der aktuell geladenen Transportanbieter durch verursacht die MAPI-Warteschlange ihrer [IXPLogon::AddressTypes](ixplogon-addresstypes.md) -Methode aufrufen. Dieses Kennzeichen ermöglicht auch der MAPI-Warteschlange an den richtigen kritische Adressbuchhierarchie Fehler ohne dass Clientanwendungen abmelden und dann erneut anmelden. 
    
FORCE_XP_CONNECT 
  
> Vom Benutzer ausgewählte einen Verbindungsvorgang. Wenn dieses Flag mit dem REFRESH_XP_HEADER_CACHE oder PROCESS_XP_HEADER_CACHE-Flag verwendet wird, erfolgt die Connect-Aktion ohne Zwischenspeichern.
    
FORCE_XP_DISCONNECT 
  
> Vom Benutzer ausgewählte einen Trennvorgang. Wenn dieses Flag mit REFRESH_XP_HEADER_CACHE oder PROCESS_XP_HEADER_CACHE verwendet wird, erfolgt die Disconnect-Aktion ohne Zwischenspeichern.
    
PROCESS_XP_HEADER_CACHE 
  
> Einträge in der Kopfzeile Cachetabelle verarbeitet werden soll, sollten alle Nachrichten mit dem MSGSTATUS_REMOTE_DOWNLOAD-Flag heruntergeladen werden und alle Nachrichten mit dem MSGSTATUS_REMOTE_DELETE-Flag gekennzeichnet gelöscht werden sollen. Nachrichten, die MSGSTATUS_REMOTE_DOWNLOAD und MSGSTATUS_REMOTE_DELETE festgelegt haben, sollten verschoben werden.
    
REFRESH_XP_HEADER_CACHE 
  
> Sollte eine neue Liste der Kopfzeilen heruntergeladen werden, und alle Flags Markierung Nachrichtenstatus sollte deaktiviert werden.
    
SUPPRESS_UI 
  
> Verhindert, dass der Adressbuchhierarchie eine Benutzeroberfläche angezeigt.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgeführt und der erwartete Wert oder Werte zurückgegeben.
    
MAPI_E_BUSY 
  
> Ein anderer Vorgang ist in Bearbeitung. Sie dürfen die Durchführung oder sollte beendet werden, bevor der Vorgang ausgeführt wird.
    
MAPI_E_NO_SUPPORT 
  
> Der beteiligten remote Adressbuchhierarchie eine Benutzeroberfläche nicht unterstützt, und die Clientanwendung selbst sollte das Dialogfeld angezeigt.
    
MAPI_E_USER_CANCEL 
  
> Der Benutzer hat den Vorgang in der Regel durch Klicken auf die Schaltfläche " **Abbrechen** " in einem Dialogfeld abgebrochen. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Die MAPI-Warteschlange Ruft die **IXPLogon::ValidateState** -Methode zur Unterstützung der Aufrufe der [IMAPIStatus::ValidateState](imapistatus-validatestate.md) -Methode für das Statusobjekt. Der Transportdienst sollte für den Aufruf der **IXPLogon::ValidateState** reagieren, als ob die MAPI-Warteschlange ein Statusobjekt für die aktuelle Sitzung geöffnet und anschließend **IMAPIStatus::ValidateState** für dieses Objekt aufgerufen wurde. 
  
Zur Unterstützung der Implementierung der **IMAPIStatus::ValidateState**Ruft die MAPI-Warteschlange **IXPLogon::ValidateState** für alle Objekte, die Anmeldung für alle aktiven Transport-Anbieter, die in einer Sitzung Profil ausgeführt werden. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIStatus::ValidateState](imapistatus-validatestate.md)
  
[IXPLogon::AddressTypes](ixplogon-addresstypes.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

