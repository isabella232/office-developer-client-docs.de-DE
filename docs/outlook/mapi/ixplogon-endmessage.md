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
  
Informiert den Transportanbieter darüber, dass der MAPI-Spooler seine Verarbeitung für eine ausgehende Nachricht abgeschlossen hat.
  
```cpp
HRESULT EndMessage(
  ULONG ulMsgRef,
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parameter

 _ulMsgRef_
  
> in Ein Nachrichten spezifischer Verweiswert, der in einem früheren Aufruf der [IXPLogon:: SubmitMessage](ixplogon-submitmessage.md) -Methode abgerufen wurde. 
    
 _lpulFlags_
  
> Out Eine Bitmaske von Flags, die dem MAPI-Spooler mitteilen, was er mit der Nachricht tun soll. Wenn keine Flags festgelegt sind, wurde die Nachricht gesendet. Die folgenden Flags können festgelegt werden:
    
END_DONT_RESEND 
  
> Der Transportanbieter verfügt jetzt über alle erforderlichen Informationen zu dieser Nachricht. Wenn der Transportanbieter Weitere Informationen benötigt oder wenn er die Nachricht gesendet hat, benachrichtigt er den MAPI-Spooler durch Aufrufen der [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md) -Methode mit dem NOTIFY_SENTDEFERRED-Flag und durch übergeben der Eintrags-ID der Nachricht. 
    
END_RESEND_LATER 
  
> Der Transportanbieter sendet die Nachricht nicht zum aktuellen Zeitpunkt aus Gründen, die keine Fehlerbedingungen sind. Der Transportanbieter sollte später erneut aufgerufen werden, um die Nachricht zu senden.
    
END_RESEND_NOW 
  
> Der Transportanbieter muss die an ihn übergebene Nachricht in einem [IMessage:: SubmitMessage](imessage-submitmessage.md) -Methodenaufruf neu starten. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf war erfolgreich, und der erwartete Wert oder die Werte wurden zurückgegeben.
    
## <a name="remarks"></a>Bemerkungen

Die MAPI-Warteschlange ruft die **IXPLogon:: EndMessage** -Methode auf, nachdem Sie die Verarbeitung abgeschlossen hat, die für die Bereitstellung erweiterter Zustellungs-oder Unzustellbarkeits Informationen erforderlich ist. 
  
Sobald dieser Aufruf zurückgegeben wird, ist der Wert im _ulMsgRef_ -Parameter für diese Nachricht nicht mehr gültig. Der Transportanbieter kann denselben Wert für eine zukünftige Nachricht wieder verwenden. 
  
Alle Objekte, die der Transportanbieter während der Übertragung einer Nachricht öffnet, sollten freigegeben werden, bevor der **EndMessage** -Aufruf zurückgegeben wird, mit Ausnahme des Message-Objekts, das vom MAPI-Spooler an den Transportanbieter übergeben wird. Das vom MAPI-Spooler übergebene Nachrichtenobjekt ist nach dem **EndMessage** -Aufruf ungültig. 
  
## <a name="see-also"></a>Siehe auch



[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IXPLogon::SubmitMessage](ixplogon-submitmessage.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

