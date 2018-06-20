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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 17470f9ff552eaa4908973c4f033db2b4e754d7c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792878"
---
# <a name="ixplogonpoll"></a>IXPLogon::Poll

  
  
**Betrifft**: Outlook 
  
Gibt an, ob der Adressbuchhierarchie mindestens eine eingehende Nachricht empfangen hat.
  
```cpp
HRESULT Poll(
  ULONG FAR * lpulIncoming
);
```

## <a name="parameters"></a>Parameter

 _lpulIncoming_
  
> [out] Ein Wert, der angibt, das Vorhandensein von eingehenden Nachrichten. Ein Wert ungleich Null gibt an, dass eingehende Nachrichten vorhanden sind.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Hinweise

Die MAPI-Warteschlange in regelmäßigen Abständen um die **IXPLogon::Poll** -Methode aufgerufen, wenn der Adressbuchhierarchie gibt an, dass es für neue Nachrichten abgefragt werden muss, dem der Anbieter, indem Sie die LOGON_SP_POLL übergeben zu den Anruf an die [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) -flag Methode am Anfang einer Sitzung. Wenn der Adressbuchhierarchie gibt als Antwort auf die **Umfrage** Anruf, die eine vorhanden sind oder mehr eingehende Nachrichten an den Prozess, die MAPI-Warteschlange für sie verfügbar Ruft die [IXPLogon::StartMessage](ixplogon-startmessage.md) -Methode, um den Anbieter an den Prozess der ersten ermöglichen, eingehend Nachricht. Der Transportdienst gibt eingehende Nachrichten durch Festlegen des Werts in der _LpulIncoming_ -Parameter auf einen anderen Wert an. 
  
## <a name="see-also"></a>Siehe auch



[IXPLogon::StartMessage](ixplogon-startmessage.md)
  
[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
  
[IXPLogon: IUnknown](ixplogoniunknown.md)

