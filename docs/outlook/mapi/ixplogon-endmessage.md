---
title: IXPLogonEndMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IXPLogon.EndMessage
api_type:
- COM
ms.assetid: bb29e6a0-7a92-46eb-bbeb-6f2df6ac6d21
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5ffe1f2ce233227de0e3a483524fc4dcb6fca7d5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584220"
---
# <a name="ixplogonendmessage"></a>IXPLogon::EndMessage

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Informiert den Transportanbieter, dass der MAPI-Spooler die Verarbeitung für eine ausgehende Nachricht abgeschlossen hat.
  
```cpp
HRESULT EndMessage(
  ULONG ulMsgRef,
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parameter

 _ulMsgRef_
  
> [in] Ein nachrichtenspezifischer Verweiswert, der in einem früheren Aufruf der [IXPLogon::SubmitMessage-Methode](ixplogon-submitmessage.md) abgerufen wurde. 
    
 _lpulFlags_
  
> [out] Eine Bitmaske mit Flags, die dem MAPI-Spooler angibt, was er mit der Nachricht tun soll. Wenn keine Flags festgelegt sind, wurde die Nachricht gesendet. Die folgenden Flags können festgelegt werden:
    
END_DONT_RESEND 
  
> Der Transportanbieter verfügt über alle Informationen, die er zu dieser Nachricht vorerst benötigt. Wenn der Transportanbieter weitere Informationen benötigt oder die Nachricht gesendet hat, benachrichtigt er den MAPI-Spooler, indem er die [IMAPISupport::SpoolerNotify-Methode](imapisupport-spoolernotify.md) mit dem NOTIFY_SENTDEFERRED Flag aufruft und den Eintragsbezeichner der Nachricht übergibt. 
    
END_RESEND_LATER 
  
> Der Transportanbieter sendet die Nachricht zum aktuellen Zeitpunkt nicht aus Gründen, die keine Fehlerbedingungen sind. Der Transportanbieter sollte später erneut aufgerufen werden, um die Nachricht zu senden.
    
END_RESEND_NOW 
  
> Der Transportanbieter muss die an ihn übergebene Nachricht in einem [IMessage::SubmitMessage-Methodenaufruf](imessage-submitmessage.md) neu starten. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf war erfolgreich und hat den erwarteten Wert oder die erwarteten Werte zurückgegeben.
    
## <a name="remarks"></a>HinwBemerkungeneise

Der MAPI-Spooler ruft die **IXPLogon::EndMessage-Methode auf,** nachdem sie die Verarbeitung abgeschlossen hat, die für die Bereitstellung erweiterter Übermittlungs- oder Nichtzustellbarkeitsinformationen verwendet wird. 
  
Sobald dieser Aufruf zurückgegeben wird, ist der Wert im  _ulMsgRef-Parameter_ für diese Nachricht nicht mehr gültig. Der Transportanbieter kann denselben Wert in einer zukünftigen Nachricht wiederverwenden. 
  
Alle Objekte, die der Transportanbieter während der Übertragung einer Nachricht öffnet, sollten freigegeben werden, bevor der **EndMessage-Aufruf** zurückgegeben wird, mit Ausnahme des Nachrichtenobjekts, das der MAPI-Spooler an den Transportanbieter übergibt. Das vom MAPI-Spooler übergebene Nachrichtenobjekt ist nach dem **EndMessage-Aufruf** ungültig. 
  
## <a name="see-also"></a>Siehe auch



[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IXPLogon::SubmitMessage](ixplogon-submitmessage.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

