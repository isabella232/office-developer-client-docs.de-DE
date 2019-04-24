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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351611"
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
  
> Out Ein Wert, der angibt, ob eingehende Nachrichten vorhanden sind. Ein Wert ungleich NULL gibt an, dass eingehende Nachrichten vorhanden sind.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Bemerkungen

Der MAPI-Spooler ruft in regelmäßigen Abständen die **IXPLogon::P oll** -Methode auf, wenn der Transportanbieter angibt, dass er für neue Nachrichten abgefragt werden muss, die der Anbieter ausführt, indem er das LOGON_SP_POLL-Flag an den Aufruf an das [IXPProvider übergibt:: TransportLogon](ixpprovider-transportlogon.md) -Methode am Anfang einer Sitzung. Wenn der Transportanbieter als Reaktion auf den **Umfrage** Aufruf angibt, dass eine oder mehrere eingehende Nachrichten zur Verarbeitung zur Verfügung stehen, ruft der MAPI-Spooler die [IXPLogon:: StartMessage](ixplogon-startmessage.md) -Methode auf, damit der Anbieter die erste eingehende Nachricht verarbeiten kann. Nachricht. Der Transportanbieter gibt eingehende Nachrichten an, indem der Wert im _lpulIncoming_ -Parameter auf einen Wert ungleich NULL festgelegt wird. 
  
## <a name="see-also"></a>Siehe auch



[IXPLogon::StartMessage](ixplogon-startmessage.md)
  
[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

