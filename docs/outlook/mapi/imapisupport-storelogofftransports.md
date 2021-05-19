---
title: IMAPISupportStoreLogoffTransports
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.StoreLogoffTransports
api_type:
- COM
ms.assetid: f21fba96-c5ca-4d41-9b93-c7955ab7327f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 30c91ec7a5a28b0c270da5223a2a245fb504d8c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421382"
---
# <a name="imapisupportstorelogofftransports"></a>IMAPISupport::StoreLogoffTransports

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Fordert die geordnete Freigabe eines Nachrichtenspeichers an.
  
```cpp
HRESULT StoreLogoffTransports(
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpulFlags_
  
> [in, out] Eine Bitmaske mit Flags, die steuert, wie der Nachrichtenspeicher abmeldet. Bei der Eingabe schließen sich alle Flags für diesen Parameter gegenseitig aus. Pro Anruf kann nur eines der folgenden Kennzeichen festgelegt werden:
    
LOGOFF_ABORT 
  
> Alle Transportanbieteraktivitäten für diesen Speicher sollten vor dem Abmelden beendet werden. Das Steuerelement wird an den Client zurückgegeben, nachdem die Aktivität beendet wurde und der MAPI-Spooler den Speicher abgemeldet hat. Wenn eine Transportaktivität stattfindet, tritt die Abmeldeung nicht auf, und das Verhalten des MAPI-Spoolers oder des Transportanbieters wird nicht geändert. Wenn derzeit keine Aktivität besteht, gibt der MAPI-Spooler den Speicher frei. 
    
LOGOFF_NO_WAIT 
  
> Der MAPI-Spooler sollte den Speicher freigegeben und die Steuerung sofort an den Client zurückgeben, nachdem alle ausgehenden E-Mails gesendet wurden, die gesendet werden können. Wenn der Nachrichtenspeicher über den Standardeinzug verfügt, wird jede In-Process-Nachricht empfangen, und dann wird der weitere Empfang deaktiviert. 
    
LOGOFF_ORDERLY 
  
> Der MAPI-Spooler sollte den Speicher los lassen und die Steuerung unmittelbar nach Abschluss der Verarbeitung ausstehender Nachrichten an den Client zurückgeben. Es sollten keine neuen Nachrichten verarbeitet werden. 
    
LOGOFF_PURGE 
  
> Funktioniert genauso wie das LOGOFF_NO_WAIT Flag. Das LOGOFF_PURGE gibt das Steuerelement nach Abschluss an den Anrufer zurück. 
    
LOGOFF_QUIET 
  
> Die Abmeldeung sollte nicht auftreten, wenn eine Transportanbieteraktivität stattfindet. Der Typ der Aktivität, die stattfindet, wird als Flag für die Ausgabe zurückgegeben.
    
    On output, MAPI spooler can return one or more of the following flags:
    
LOGOFF_COMPLETE 
  
> Die Abmeldeung kann abgeschlossen werden. Alle dem Speicher zugeordneten Ressourcen wurden freigegeben, und das Objekt wurde ungültig. Der MAPI-Spooler hat alle Anforderungen ausgeführt oder führt diese aus. Nur die **IUnknown::Release-Methode** des Nachrichtenspeichers sollte an diesem Punkt aufgerufen werden. 
    
LOGOFF_INBOUND 
  
> Eine Nachricht wird derzeit von einem oder mehreren Transportanbietern in den Store gesendet. 
    
LOGOFF_OUTBOUND 
  
> Eine Nachricht wird derzeit von einem oder mehreren Transportanbietern aus dem Store gesendet. 
    
LOGOFF_OUTBOUND_QUEUE 
  
> Derzeit befinden sich Nachrichten in der ausgehenden Warteschlange für den Speicher.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Abmeldeprozedur war erfolgreich.
    
## <a name="remarks"></a>Hinweise

Die **IMAPISupport::StoreLogoffTransports-Methode** wird für Unterstützungsobjekte des Nachrichtenspeicheranbieters implementiert. Nachrichtenspeicheranbieter rufen **StoreLogoffTransports** auf, um Clientanwendungen die Kontrolle darüber zu geben, wie MAPI transport provider activity as a message store is closing behandelt. 
  
Wenn ein anderer Prozess den Speicher geöffnet hat, der für dasselbe Profil geöffnet werden soll, ignoriert MAPI einen Aufruf von **StoreLogoffTransports** und gibt das Flag LOGOFF_COMPLETE im  _lpulFlags-Parameter_ zurück. 
  
Das Verhalten des Speicheranbieters nach der Rückgabe von **StoreLogoffTransports** sollte auf dem Wert von  _lpulFlags_ basieren, der den Systemstatus angibt und Clientanweisungen für das Abmeldeverhalten übermittelt. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

 **StoreLogoffTransports** wird in der Regel von der [IMsgStore::StoreLogoff-Methode](imsgstore-storelogoff.md) eines Speicheranbieters aufgerufen. Sie kann jedoch auch von der **IUnknown::Release-Methode des** Nachrichtenspeichers aufgerufen werden. Implementieren Sie **die Release-Methode** Ihres Nachrichtenspeichers, damit Sie überprüfen können, ob ein Aufruf von **StoreLogoffTransports** stattgefunden hat. Wenn kein Anruf erfolgt ist, rufen **Sie StoreLogoffTransports** mit dem LOGOFF_ABORT auf. 
  
Der  _lpulFlags-Parameter_ ist auf ein Flag festgelegt, das angibt, wie der Client das Herunterfahren des Nachrichtenspeichers erfordert. Bestimmen Sie die entsprechende Einstellung für  _ulFlags_ basierend auf der Einstellung des entsprechenden Parameters im Aufruf von **StoreLogoff**. Das heißt, wenn ein Client Ihre **StoreLogoff-Methode** mit  _ulFlags_ auf LOGOFF_ORDERLY festgelegt hat, sollten Sie **StoreLogoffTransports** aufrufen, wenn  _ulFlags_ auf LOGOFF_ORDERLY. 
  
Weitere Informationen zum Abmeldevorgang des Nachrichtenspeichers finden Sie unter [Shutting Down a Message Store Provider](shutting-down-a-message-store-provider.md).
  
## <a name="see-also"></a>Siehe auch



[IMsgStore::StoreLogoff](imsgstore-storelogoff.md)
  
[IXPLogon::FlushQueues](ixplogon-flushqueues.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

