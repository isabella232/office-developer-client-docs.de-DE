---
title: IXPLogonPoll
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IXPLogon.Poll
api_type:
- COM
ms.assetid: 1524eb06-7492-42de-b455-e0982bda7ece
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f0981c87ccf51b98296d7658d5695b6c58d37948
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584206"
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
  
> [out] Ein Wert, der angibt, dass eingehende Nachrichten vorhanden sind. Ein Wert ungleich Null gibt an, dass eingehende Nachrichten vorhanden sind.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>HinwBemerkungeneise

Der MAPI-Spooler ruft in regelmäßigen Abständen die **IXPLogon::P oll-Methode** auf, wenn der Transportanbieter angibt, dass er für neue Nachrichten abgefragt werden muss, was der Anbieter durch Übergeben des LOGON_SP_POLL Flags an den Aufruf der [IXPProvider::TransportLogon-Methode](ixpprovider-transportlogon.md) zu Beginn einer Sitzung durchführt. Wenn der Transportanbieter als Reaktion auf den **Poll-Aufruf** angibt, dass eine oder mehrere eingehende Nachrichten für die Verarbeitung verfügbar sind, ruft der MAPI-Spooler die [IXPLogon::StartMessage-Methode](ixplogon-startmessage.md) auf, damit der Anbieter die erste eingehende Nachricht verarbeiten kann. Der Transportanbieter gibt eingehende Nachrichten an, indem der Wert im  _lpulIncoming-Parameter_ auf einen Wert ungleich Null festgelegt wird. 
  
## <a name="see-also"></a>Siehe auch



[IXPLogon::StartMessage](ixplogon-startmessage.md)
  
[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

