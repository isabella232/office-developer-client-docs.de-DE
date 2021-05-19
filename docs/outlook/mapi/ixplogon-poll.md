---
title: IXPLogonPoll
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.Poll
api_type:
- COM
ms.assetid: 1524eb06-7492-42de-b455-e0982bda7ece
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3e68c564357880b623e02081a228e881c084fa94
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425274"
---
# <a name="ixplogonpoll"></a>IXPLogon::Poll

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt an, ob der Transportanbieter eine oder mehrere eingehende Nachrichten empfangen hat.
  
```cpp
HRESULT Poll(
  ULONG FAR * lpulIncoming
);
```

## <a name="parameters"></a>Parameter

 _lpulIncoming_
  
> [out] Ein Wert, der das Vorhandensein eingehender Nachrichten angibt. Ein Wert ungleich Null gibt an, dass eingehende Nachrichten vorhanden sind.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Hinweise

Der MAPI-Spooler ruft regelmäßig die **IXPLogon::P oll-Methode** auf, wenn der Transportanbieter angibt, dass er nach neuen Nachrichten abfragen muss, was der Anbieter durch Übergeben des LOGON_SP_POLL-Flags an den Aufruf der [IXPProvider::TransportLogon-Methode](ixpprovider-transportlogon.md) am Anfang einer Sitzung tut. Wenn der Transportanbieter als Antwort  auf den Abrufanruf angibt, dass eine oder mehrere eingehende Nachrichten für die Behandlung verfügbar sind, ruft der MAPI-Spooler die [IXPLogon::StartMessage-Methode](ixplogon-startmessage.md) auf, damit der Anbieter die erste eingehende Nachricht verarbeiten kann. Der Transportanbieter gibt eingehende Nachrichten an, indem der Wert im  _lpulIncoming-Parameter_ auf einen Wert ungleich Null festgelegt wird. 
  
## <a name="see-also"></a>Siehe auch



[IXPLogon::StartMessage](ixplogon-startmessage.md)
  
[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

