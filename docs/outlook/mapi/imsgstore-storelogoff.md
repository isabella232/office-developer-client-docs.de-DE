---
title: IMsgStoreStoreLogoff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.StoreLogoff
api_type:
- COM
ms.assetid: 3773c98e-531e-4bdc-a39a-2c3bb7378cd3
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2ac8fb6f4e56b6f086e6061c227120cd49fc621a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792638"
---
# <a name="imsgstorestorelogoff"></a>IMsgStore::StoreLogoff

  
  
**Betrifft**: Outlook 
  
Ermöglicht das ordnungsgemäße Abmelden des Nachrichtenspeichers.
  
```cpp
HRESULT StoreLogoff(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpulFlags_
  
> [in, out] Eine Bitmaske aus Flags, die aus dem Nachrichtenspeicher Abmeldung steuert. Bei der Eingabe sind alle Flags für diesen Parameter festlegen schließen sich gegenseitig aus. ein Anrufer muss nur ein Flag pro Aufruf angeben. Die folgenden Kennzeichen sind bei der Eingabe gültig:
    
LOGOFF_ABORT 
  
> Alle Anbieter transportaktivität für diesen Nachrichtenspeicher sollten vor der Abmeldung beendet werden. Steuerelement wird mit dem Anrufer zurückgegeben, nachdem Aktivität beendet wurde. Wenn alle Anbieter transportaktivität stattfindet, die Abmeldung tritt nicht auf, und keine Änderung des Verhaltens der MAPI-Warteschlange oder Transport Anbieter tritt auf. Wenn der Anbieter transportaktivität im Leerlauf befindet, gibt die MAPI-Warteschlange den Speicher frei. 
    
LOGOFF_NO_WAIT 
  
> Der Nachrichtenspeicher sollte nicht für Nachrichten von Anbietern vor dem Schließen Transport warten. Ausgehende Nachrichten, die gesendet werden können, werden gesendet. Wenn dieser Speicher der standardmäßige Posteingang enthält, werden alle Nachrichten in-Process empfangen, und klicken Sie dann weitere Empfang deaktiviert. Wenn alle Aktivitäten abgeschlossen ist, die MAPI-Warteschlange gibt den Speicher und Steuerelement wird mit dem Anrufer sofort zurückgegeben. 
    
LOGOFF_ORDERLY 
  
> Der Nachrichtenspeicher sollten Informationen von Transport Anbietern vor dem Schließen nicht warten. Nachrichten, die aktuell verarbeitet werden abgeschlossen sind, jedoch keine neuen Nachrichten verarbeitet werden. Wenn alle Aktivitäten abgeschlossen ist, die MAPI-Warteschlange gibt den Speicher und Steuerung sofort auf den Anbieter zurückgegeben wird. 
    
LOGOFF_PURGE 
  
> Das Abmelden sollte dieselbe funktionieren das Flag LOGOFF_NO_WAIT festgelegt ist, wobei jedoch die [IXPLogon::FlushQueues](ixplogon-flushqueues.md) oder [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) -Methode für die entsprechenden Transportanbieter sollte aufgerufen werden. Das Flag LOGOFF_PURGE gibt das Steuerelement mit dem Anrufer nach Abschluss zurück. 
    
LOGOFF_QUIET 
  
> Wenn alle Anbieter transportaktivität stattfindet, sollte das Abmelden nicht erfolgen.
    
    The following flags are valid on output:
    
LOGOFF_INBOUND 
  
> Eingehende Nachrichten werden derzeit erhältlich.
    
LOGOFF_OUTBOUND 
  
> Ausgehende Nachrichten werden gerade gesendet werden.
    
LOGOFF_OUTBOUND_QUEUE 
  
> Ausgehende Nachrichten werden ausstehende (d. h., sie sind in den Postausgang).
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Abmeldung wurde erfolgreich abgeschlossen.
    
## <a name="remarks"></a>Hinweise

Die **IMsgStore::StoreLogoff** -Methode beim Ausrichten ausübt Steuerelement über die Interaktion der Nachricht speichern und transport-Anbieter während des Abmeldevorgangs. Aufrufen von **StoreLogoff** gilt nur für Nachrichtenspeicher, die nur vom Anrufer verwendet werden. Beispielsweise wenn zwei Clients den gleichen Nachrichtenspeicher verwenden und einer von ihnen **StoreLogoff**aufruft, der Nachrichtenspeicher wird sofort freigegeben und wird die Steuerung an den aufrufenden Client zurückgegeben.
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Speichern Sie die Kennzeichen, die an **StoreLogoff** übergeben werden, und übergeben Sie diese Option, wenn Sie die [IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md) -Methode aufrufen. Rufen Sie nicht **StoreLogoffTransports** , bis der Nachrichtenspeicher Referenzzähler auf Null fällt. Mehrere Aufrufe von **StoreLogoffTransports** überschreiben einfach die gespeicherten Kennzeichen. 
  
Wenn kein Aufruf an **StoreLogoff** vorgenommen wurde vor der Meldung des Informationsspeichers Referenzzähler 0 (null) erreicht, legen Sie das Flag LOGOFF_ABORT im _UlFlags_ -Parameter, den an **StoreLogoffTransports**übergeben.
  
## <a name="see-also"></a>Siehe auch



[IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)
  
[IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md)
  
[IXPLogon::FlushQueues](ixplogon-flushqueues.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)

