---
title: IXPLogonEndMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.EndMessage
api_type:
- COM
ms.assetid: bb29e6a0-7a92-46eb-bbeb-6f2df6ac6d21
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 03eccfe27c6f93e42ee01a34fbf5df766c145cf1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414158"
---
# <a name="ixplogonendmessage"></a>IXPLogon::EndMessage

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Informiert den Transportanbieter, dass der MAPI-Spooler seine Verarbeitung für eine ausgehende Nachricht abgeschlossen hat.
  
```cpp
HRESULT EndMessage(
  ULONG ulMsgRef,
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parameter

 _ulMsgRef_
  
> [in] Ein nachrichtenspezifischer Referenzwert, der bei einem früheren Aufruf der [IXPLogon::SubmitMessage-Methode erhalten](ixplogon-submitmessage.md) wurde. 
    
 _lpulFlags_
  
> [out] Eine Bitmaske mit Flags, die dem MAPI-Spooler angibt, was mit der Nachricht zu tun ist. Wenn keine Kennzeichen festgelegt sind, wurde die Nachricht gesendet. Die folgenden Kennzeichen können festgelegt werden:
    
END_DONT_RESEND 
  
> Der Transportanbieter verfügt derzeit über alle Informationen, die er zu dieser Nachricht benötigt. Wenn der Transportanbieter weitere Informationen benötigt oder die Nachricht gesendet hat, benachrichtigt er den MAPI-Spooler, indem er die [IMAPISupport::SpoolerNotify-Methode](imapisupport-spoolernotify.md) mit dem flag NOTIFY_SENTDEFERRED aufruft und den Eintragsbezeichner der Nachricht übergeben. 
    
END_RESEND_LATER 
  
> Der Transportanbieter sendet die Nachricht zum aktuellen Zeitpunkt nicht aus Gründen, die keine Fehlerbedingungen sind. Der Transportanbieter sollte später erneut aufgerufen werden, um die Nachricht zu senden.
    
END_RESEND_NOW 
  
> Der Transportanbieter muss die An ihn übergebene Nachricht in einem [IMessage::SubmitMessage-Methodenaufruf](imessage-submitmessage.md) neu starten. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf war erfolgreich und hat den erwarteten Wert oder die erwarteten Werte zurückgegeben.
    
## <a name="remarks"></a>Hinweise

Der MAPI-Spooler ruft die **IXPLogon::EndMessage-Methode** auf, nachdem er die Verarbeitung abgeschlossen hat, die an der Bereitstellung von erweiterten Übermittlungs- oder nicht-unausgeblichen Informationen beteiligt ist. 
  
Sobald dieser Aufruf zurückgegeben wird, ist der Wert im  _ulMsgRef-Parameter_ für diese Nachricht nicht mehr gültig. Der Transportanbieter kann denselben Wert für eine zukünftige Nachricht wiederverwenden. 
  
Alle Objekte, die der Transportanbieter während der Übertragung einer Nachricht öffnet, sollten vor der Rückgabe des **EndMessage-Aufrufs** freigegeben werden, mit Ausnahme des Nachrichtenobjekts, das der MAPI-Spooler an den Transportanbieter übergibt. Das vom MAPI-Spooler übergebene Message-Objekt ist nach dem **EndMessage-Aufruf** ungültig. 
  
## <a name="see-also"></a>Siehe auch



[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IXPLogon::SubmitMessage](ixplogon-submitmessage.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

