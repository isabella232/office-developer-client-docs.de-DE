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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: be11c536804682d1baec8188b6d7487c71d411e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424336"
---
# <a name="imsgstorestorelogoff"></a>IMsgStore::StoreLogoff

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Aktiviert die ordnungsgemäße Abmeldung des Nachrichtenspeichers.
  
```cpp
HRESULT StoreLogoff(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpulFlags_
  
> [in, out] Eine Bitmaske von Flags, die die Abmeldung aus dem Nachrichtenspeicher steuert. Bei der Eingabe schließen sich alle für diesen Parameter festgelegten Flags gegenseitig aus; ein Anrufer muss nur ein Flag pro Anruf angeben. Die folgenden Flags sind bei der Eingabe gültig:
    
LOGOFF_ABORT 
  
> Alle Transportanbieter Aktivitäten für diesen Nachrichtenspeicher sollten vor dem Abmelden angehalten werden. Das Steuerelement wird an den Aufrufer zurückgegeben, nachdem Activity beendet wurde. Wenn eine Transportanbieter Aktivität stattfindet, wird die Abmeldung nicht ausgeführt, und es tritt keine Änderung des Verhaltens der MAPI-Spooler-oder Transportanbieter auf. Wenn sich die Transportanbieter Aktivität im Leerlauf befindet, gibt der MAPI-Spooler den Speicher frei. 
    
LOGOFF_NO_WAIT 
  
> Der Nachrichtenspeicher sollte vor dem Schließen nicht auf Nachrichten von Transportanbietern warten. Ausgehende Nachrichten, die gesendet werden können, werden gesendet. Wenn dieser Speicher den Standard Posteingang enthält, werden alle in-Process-Nachrichten empfangen, und dann wird der weitere Empfang deaktiviert. Wenn alle Aktivitäten abgeschlossen sind, gibt der MAPI-Spooler den Speicher frei, und das Steuerelement wird sofort an den Aufrufer zurückgegeben. 
    
LOGOFF_ORDERLY 
  
> Der Nachrichtenspeicher sollte vor dem Schließen nicht auf Informationen von Transportanbietern warten. Nachrichten, die gerade verarbeitet werden, werden abgeschlossen, es werden jedoch keine neuen Nachrichten verarbeitet. Wenn alle Aktivitäten abgeschlossen sind, gibt der MAPI-Spooler den Speicher frei, und das Steuerelement wird sofort an den Speicheranbieter zurückgegeben. 
    
LOGOFF_PURGE 
  
> Die Abmeldung sollte genauso funktionieren, als ob das LOGOFF_NO_WAIT-Flag festgelegt ist, aber entweder die [IXPLogon:: FlushQueues](ixplogon-flushqueues.md) oder [IMAPIStatus:: FlushQueues](imapistatus-flushqueues.md) -Methode für die entsprechenden Transportanbieter aufgerufen werden soll. Das LOGOFF_PURGE-Flag gibt nach Abschluss die Steuerung an den Aufrufer zurück. 
    
LOGOFF_QUIET 
  
> Wenn eine Transportanbieter Aktivität stattfindet, sollte die Abmeldung nicht erfolgen.
    
    The following flags are valid on output:
    
LOGOFF_INBOUND 
  
> Eingehende Nachrichten werden gerade ankommen.
    
LOGOFF_OUTBOUND 
  
> Ausgehende Nachrichten werden gerade gesendet.
    
LOGOFF_OUTBOUND_QUEUE 
  
> Ausgehende Nachrichten sind ausstehend (das heißt, Sie befinden sich im Postausgang).
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Abmeldung wurde erfolgreich abgeschlossen.
    
## <a name="remarks"></a>Bemerkungen

Die **IMsgStore:: StoreLogoff** -Methode übt während des Abmeldevorgangs die Steuerung der Interaktion zwischen dem Nachrichtenspeicher und den Transportanbietern aus. Das Aufrufen von **StoreLogoff** ist nur für Nachrichtenspeicher zulässig, die nur vom Aufrufer verwendet werden. Wenn beispielsweise zwei Clients denselben Nachrichtenspeicher verwenden und einer von Ihnen **StoreLogoff**aufruft, wird der Nachrichtenspeicher sofort freigegeben, und die Steuerung wird an den aufrufenden Client zurückgegeben.
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Speichern Sie die Flags, die an **StoreLogoff** übergeben werden, und übergeben Sie diese, wenn Sie die [IMAPISupport:: StoreLogoffTransports](imapisupport-storelogofftransports.md) -Methode aufrufen. Rufen Sie **StoreLogoffTransports** erst auf, wenn der Verweiszähler des Nachrichtenspeichers auf Null sinkt. Bei mehreren Aufrufen von **StoreLogoffTransports** werden die gespeicherten Flags einfach überschrieben. 
  
Wenn kein Aufruf an **StoreLogoff** vorgenommen wurde, bevor der Verweiszähler des Nachrichtenspeichers 0 (null) erreicht, legen Sie das LOGOFF_ABORT-Flag im _ulFlags_ -Parameter, den Sie an **StoreLogoffTransports**übergeben.
  
## <a name="see-also"></a>Siehe auch



[IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)
  
[IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md)
  
[IXPLogon::FlushQueues](ixplogon-flushqueues.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)

