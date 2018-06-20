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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 7f81a0c3c9a9ad0a9bcef5c5685aa5b343237f19
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792868"
---
# <a name="ixplogonendmessage"></a>IXPLogon::EndMessage

  
  
**Betrifft**: Outlook 
  
Der Transportdienst informiert werden, dass die MAPI-Warteschlange die Verarbeitung für eine ausgehende Nachricht abgeschlossen.
  
```cpp
HRESULT EndMessage(
  ULONG ulMsgRef,
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parameter

 _ulMsgRef_
  
> [in] Ein Message-spezifische-Verweiswert, der in einem früheren Aufruf der [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) -Methode abgerufen wurde. 
    
 _lpulFlags_
  
> [out] Eine Bitmaske aus Flags, die an die Warteschlange MAPI gibt an, was mit der Nachricht Verfahren werden soll. Wenn keine Flags festgelegt sind, hat die Nachricht gesendet wurde. Die folgenden Kennzeichen können festgelegt werden:
    
END_DONT_RESEND 
  
> Der Transportdienst verfügt über alle Informationen, die über diese Meldung für jetzt benötigt. Wenn der Adressbuchhierarchie Weitere Informationen erforderlich sind, oder wenn sie die Nachricht gesendet hat, benachrichtigt die MAPI-Warteschlange, die [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) -Methode mit dem NOTIFY_SENTDEFERRED-Flag und durch Übergeben der Eintrags-ID der Nachricht. 
    
END_RESEND_LATER 
  
> Der Transportdienst sendet die Nachricht nicht an der aktuellen Zeit Gründen, die nicht fehlerbedingungen sind. Der Transportdienst sollte erneut zum Senden der Nachricht höher aufgerufen werden.
    
END_RESEND_NOW 
  
> Der Transportdienst muss neu gestartet werden die Nachricht in einem Aufruf der [IMessage::SubmitMessage](imessage-submitmessage.md) -Methode übergeben. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgeführt und der erwartete Wert oder Werte zurückgegeben.
    
## <a name="remarks"></a>Hinweise

Die MAPI-Warteschlange Ruft die **IXPLogon::EndMessage** -Methode nach dem Abschluss der Verarbeitung von erweiterten Übermittlung oder Nondelivery Informationen bereitstellen. 
  
Nachdem dieser Aufruf zurückgegeben wird, ist der Wert in der _UlMsgRef_ -Parameter nicht mehr gültig für diese Nachricht. Der Transportdienst kann den gleichen Wert auf eine zukünftige Nachricht wiederverwenden. 
  
Alle Objekte, die der Adressbuchhierarchie während der Übertragung einer Nachricht öffnet sollten vor der **EndMessage** Rückgabe, mit Ausnahme von Message-Objekts freigegeben werden, die die MAPI-Warteschlange an der Adressbuchhierarchie übergibt. Die MAPI-Warteschlange übergebener Message-Objekts ist nach dem Aufruf der **EndMessage** ungültig. 
  
## <a name="see-also"></a>Siehe auch



[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IXPLogon::SubmitMessage](ixplogon-submitmessage.md)
  
[IXPLogon: IUnknown](ixplogoniunknown.md)

