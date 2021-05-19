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
  
Aktiviert die geordnete Abmeldung des Nachrichtenspeichers.
  
```cpp
HRESULT StoreLogoff(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpulFlags_
  
> [in, out] Eine Bitmaske mit Flags, die die Abmeldung aus dem Nachrichtenspeicher steuert. Bei der Eingabe schließen sich alle für diesen Parameter festgelegten Flags gegenseitig aus. Ein Anrufer darf pro Anruf nur ein Flag angeben. Die folgenden Flags sind für die Eingabe gültig:
    
LOGOFF_ABORT 
  
> Alle Transportanbieteraktivitäten für diesen Nachrichtenspeicher sollten vor dem Abmelden beendet werden. Das Steuerelement wird an den Anrufer zurückgegeben, nachdem die Aktivität beendet wurde. Wenn eine Transportanbieteraktivität stattfindet, tritt die Abmeldeung nicht auf, und es tritt keine Änderung des Verhaltens des MAPI-Spoolers oder des Transportanbieters auf. Wenn sich die Aktivität des Transportanbieters im Leerlauf befindet, gibt der MAPI-Spooler den Speicher frei. 
    
LOGOFF_NO_WAIT 
  
> Der Nachrichtenspeicher sollte vor dem Schließen nicht auf Nachrichten von Transportanbietern warten. Ausgehende Nachrichten, die gesendet werden können, werden gesendet. Wenn dieser Speicher den Standardeinzug enthält, werden alle In-Process-Nachrichten empfangen, und dann wird der weitere Empfang deaktiviert. Wenn alle Aktivitäten abgeschlossen sind, gibt der MAPI-Spooler den Speicher frei, und das Steuerelement wird sofort an den Aufrufer zurückgegeben. 
    
LOGOFF_ORDERLY 
  
> Der Nachrichtenspeicher sollte nicht vor dem Schließen auf Informationen von Transportanbietern warten. Nachrichten, die derzeit verarbeitet werden, werden abgeschlossen, es werden jedoch keine neuen Nachrichten verarbeitet. Wenn alle Aktivitäten abgeschlossen sind, gibt der MAPI-Spooler den Speicher frei, und das Steuerelement wird sofort an den Speicheranbieter zurückgegeben. 
    
LOGOFF_PURGE 
  
> Die Abmeldemethode sollte genauso funktionieren, als wäre das LOGOFF_NO_WAIT-Flag festgelegt, aber entweder die [IXPLogon::FlushQueues-](ixplogon-flushqueues.md) oder [IMAPIStatus::FlushQueues-Methode](imapistatus-flushqueues.md) für die entsprechenden Transportanbieter sollte aufgerufen werden. Das LOGOFF_PURGE gibt das Steuerelement nach Abschluss an den Anrufer zurück. 
    
LOGOFF_QUIET 
  
> Wenn eine Transportanbieteraktivität stattfindet, sollte die Abmeldeung nicht erfolgen.
    
    The following flags are valid on output:
    
LOGOFF_INBOUND 
  
> Eingehende Nachrichten werden derzeit empfangen.
    
LOGOFF_OUTBOUND 
  
> Ausgehende Nachrichten werden gerade gesendet.
    
LOGOFF_OUTBOUND_QUEUE 
  
> Ausgehende Nachrichten sind ausstehend (d. h. sie befinden sich im Posteingang).
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Abmeldeung wurde erfolgreich abgeschlossen.
    
## <a name="remarks"></a>Hinweise

Die **IMsgStore::StoreLogoff-Methode** übernimmt während des Abmeldevorgangs die Kontrolle über die Interaktion von Nachrichtenspeicher und Transportanbietern. Das **Aufrufen von StoreLogoff** ist nur für Nachrichtenspeicher gültig, die nur vom Anrufer verwendet werden. Wenn beispielsweise zwei Clients denselben Nachrichtenspeicher verwenden und einer von ihnen **StoreLogoff** aufruft, wird der Nachrichtenspeicher sofort freigegeben und das Steuerelement an den aufrufenden Client zurückgegeben.
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Speichern Sie die Flags, die an **StoreLogoff übergeben** werden, und übergeben Sie sie, wenn Sie die [IMAPISupport::StoreLogoffTransports-Methode](imapisupport-storelogofftransports.md) aufrufen. Rufen Sie **StoreLogoffTransports** erst auf, wenn die Referenzanzahl des Nachrichtenspeichers auf Null sinkt. Mehrere Aufrufe von **StoreLogoffTransports** überschreiben einfach die gespeicherten Flags. 
  
Wenn kein Aufruf von **StoreLogoff** erfolgt ist, bevor die Referenzanzahl des Nachrichtenspeichers null erreicht, legen Sie das LOGOFF_ABORT-Flag im _ulFlags-Parameter_ fest, den Sie an **StoreLogoffTransports übergeben.**
  
## <a name="see-also"></a>Siehe auch



[IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)
  
[IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md)
  
[IXPLogon::FlushQueues](ixplogon-flushqueues.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)

