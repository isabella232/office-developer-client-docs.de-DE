---
title: IMsgStoreStoreLogoff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMsgStore.StoreLogoff
api_type:
- COM
ms.assetid: 3773c98e-531e-4bdc-a39a-2c3bb7378cd3
ms.openlocfilehash: d5a5b25dd41238cf27bf4a7224bb4d5d1eeb1469
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59604838"
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
  
> [in, out] Eine Bitmaske mit Flags, die die Abmeldung vom Nachrichtenspeicher steuert. Bei der Eingabe schließen sich alle für diesen Parameter festgelegten Flags gegenseitig aus. Ein Anrufer darf nur ein Flag pro Anruf angeben. Die folgenden Flags sind für Eingaben gültig:
    
LOGOFF_ABORT 
  
> Alle Transportanbieteraktivitäten für diesen Nachrichtenspeicher sollten vor der Abmeldung beendet werden. Das Steuerelement wird an den Aufrufer zurückgegeben, nachdem die Aktivität beendet wurde. Wenn eine Transportanbieteraktivität stattfindet, tritt die Abmeldung nicht auf, und das Verhalten des MAPI-Spoolers oder Transportanbieters ändert sich nicht. Wenn die Aktivität des Transportanbieters im Leerlauf ist, gibt der MAPI-Spooler den Speicher frei. 
    
LOGOFF_NO_WAIT 
  
> Der Nachrichtenspeicher sollte nicht auf Nachrichten von Transportanbietern warten, bevor er geschlossen wird. Ausgehende Nachrichten, die bereit zum Senden sind, werden gesendet. Wenn dieser Informationsspeicher den Standard-Posteingang enthält, werden alle in-Process-Nachrichten empfangen, und der weitere Empfang wird deaktiviert. Wenn alle Aktivitäten abgeschlossen sind, gibt der MAPI-Spooler den Speicher frei, und das Steuerelement wird sofort an den Aufrufer zurückgegeben. 
    
LOGOFF_ORDERLY 
  
> Der Nachrichtenspeicher sollte nicht auf Informationen von Transportanbietern warten, bevor er geschlossen wird. Nachrichten, die derzeit verarbeitet werden, werden abgeschlossen, es werden jedoch keine neuen Nachrichten verarbeitet. Wenn alle Aktivitäten abgeschlossen sind, gibt der MAPI-Spooler den Speicher frei, und das Steuerelement wird sofort an den Store-Anbieter zurückgegeben. 
    
LOGOFF_PURGE 
  
> Die Abmeldung sollte genauso funktionieren, als ob das LOGOFF_NO_WAIT-Flag festgelegt ist, aber entweder die [IXPLogon::FlushQueues-](ixplogon-flushqueues.md) oder [IMAPIStatus::FlushQueues-Methode](imapistatus-flushqueues.md) für die entsprechenden Transportanbieter sollte aufgerufen werden. Das flag LOGOFF_PURGE gibt die Steuerung an den Aufrufer nach Abschluss zurück. 
    
LOGOFF_QUIET 
  
> Wenn eine Transportanbieteraktivität stattfindet, sollte die Abmeldung nicht erfolgen.
    
Die folgenden Flags sind für die Ausgabe gültig.
    
LOGOFF_INBOUND 
  
> Eingehende Nachrichten werden derzeit eintreffen.
    
LOGOFF_OUTBOUND 
  
> Ausgehende Nachrichten werden gerade gesendet.
    
LOGOFF_OUTBOUND_QUEUE 
  
> Ausgehende Nachrichten sind ausstehend (d. h. sie befinden sich im Posteingang).
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Abmeldung wurde erfolgreich abgeschlossen.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMsgStore::StoreLogoff-Methode** steuert die Interaktion des Nachrichtenspeichers und der Transportanbieter während des Abmeldevorgangs. Das Aufrufen von **StoreLogoff** gilt nur für Nachrichtenspeicher, die nur vom Aufrufer verwendet werden. Wenn beispielsweise zwei Clients denselben Nachrichtenspeicher verwenden und einer von ihnen **StoreLogoff** aufruft, wird der Nachrichtenspeicher sofort freigegeben, und die Steuerung wird an den aufrufenden Client zurückgegeben.
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Speichern Sie die Flags, die an **StoreLogoff** übergeben werden, und übergeben Sie sie, wenn Sie die [IMAPISupport::StoreLogoffTransports-Methode](imapisupport-storelogofftransports.md) aufrufen. Rufen Sie **StoreLogoffTransports** erst auf, wenn die Referenzanzahl des Nachrichtenspeichers auf Null fällt. Mehrere Aufrufe von **StoreLogoffTransports** überschreiben einfach die gespeicherten Flags. 
  
Wenn **storeLogoff** noch nicht aufgerufen wurde, bevor die Referenzanzahl des Nachrichtenspeichers Null erreicht, legen Sie das flag LOGOFF_ABORT im  _ulFlags-Parameter_ fest, den Sie an **StoreLogoffTransports** übergeben.
  
## <a name="see-also"></a>Siehe auch



[IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)
  
[IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md)
  
[IXPLogon::FlushQueues](ixplogon-flushqueues.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)

