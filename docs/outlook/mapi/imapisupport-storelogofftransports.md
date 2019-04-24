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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326495"
---
# <a name="imapisupportstorelogofftransports"></a>IMAPISupport::StoreLogoffTransports

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Fordert die ordnungsgemäße Freigabe eines Nachrichtenspeichers an.
  
```cpp
HRESULT StoreLogoffTransports(
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpulFlags_
  
> [in, out] Eine Bitmaske von Flags, die die Anzeige des Nachrichtenspeichers steuert. Bei der Eingabe schließen sich alle Flags für diesen Parameter gegenseitig aus; nur eines der folgenden Flags kann pro Aufruf festgelegt werden:
    
LOGOFF_ABORT 
  
> Jede Transportanbieter Aktivität für diesen Speicher sollte vor dem Abmelden angehalten werden. Das Steuerelement wird an den Client zurückgegeben, nachdem die Aktivität beendet wurde und der MAPI-Spooler sich vom Speicher abgemeldet hat. Wenn eine Transportaktivität stattfindet, wird die Abmeldung nicht ausgeführt, und es tritt keine Änderung des MAPI-Spoolers oder des Transportanbieter Verhaltens auf. Wenn derzeit keine Aktivität vorhanden ist, gibt der MAPI-Spooler den Speicher frei. 
    
LOGOFF_NO_WAIT 
  
> Der MAPI-Spooler sollte den Store freigeben und sofort die Steuerung an den Client zurückgeben, nachdem alle zu sendenden ausgehenden e-Mails gesendet wurden. Wenn der Nachrichtenspeicher den Standard Posteingang hat, werden alle in-Process-Nachrichten empfangen, und dann wird der weitere Empfang deaktiviert. 
    
LOGOFF_ORDERLY 
  
> Der MAPI-Spooler sollte den Speicher freigeben und sofort die Steuerung an den Client zurückgeben, nachdem alle ausstehenden Nachrichten verarbeitet wurden. Es sollten keine neuen Nachrichten verarbeitet werden. 
    
LOGOFF_PURGE 
  
> Funktioniert wie das LOGOFF_NO_WAIT-Flag. Das LOGOFF_PURGE-Flag gibt nach Abschluss die Steuerung an den Aufrufer zurück. 
    
LOGOFF_QUIET 
  
> Die Abmeldung sollte nicht auftreten, wenn eine Transportanbieter Aktivität stattfindet. Die Art der Aktivität, die stattfindet, wird als Flag für die Ausgabe zurückgegeben.
    
    On output, MAPI spooler can return one or more of the following flags:
    
LOGOFF_COMPLETE 
  
> Die Abmeldung kann abgeschlossen werden. Alle dem Speicher zugeordneten Ressourcen wurden freigegeben, und das Objekt wurde für ungültig erklärt. Der MAPI-Spooler hat alle Anforderungen ausgeführt oder führt Sie aus. Nur die **IUnknown:: Release** -Methode des Nachrichtenspeichers sollte an dieser Stelle aufgerufen werden. 
    
LOGOFF_INBOUND 
  
> Eine Nachricht kommt derzeit von einem oder mehreren Transportanbietern in den Store. 
    
LOGOFF_OUTBOUND 
  
> Eine Nachricht wird derzeit von einem oder mehreren Transportanbietern aus dem Store gesendet. 
    
LOGOFF_OUTBOUND_QUEUE 
  
> Es befinden sich derzeit Nachrichten in der ausgehenden Warteschlange für den Speicher.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Abmelde Prozedur war erfolgreich.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISupport:: StoreLogoffTransports** -Methode wird für Support Objekte des Nachrichtenspeicher Anbieters implementiert. Nachrichtenspeicher Anbieter rufen **StoreLogoffTransports** auf, um Clientanwendungen zu steuern, wie MAPI die Transportanbieter Aktivität verarbeitet, wenn der Nachrichtenspeicher geschlossen wird. 
  
Wenn ein anderer Prozess den zu speichernden Speicher für dasselbe Profil geöffnet hat, ignoriert MAPI einen Aufruf von **StoreLogoffTransports** und gibt das Flag LOGOFF_COMPLETE im _lpulFlags_ -Parameter zurück. 
  
Das Verhalten des Speicheranbieters nach der Rückgabe von **StoreLogoffTransports** sollte auf dem Wert von _lpulFlags_basieren, der den Systemstatus angibt und Client Anweisungen für das Verhalten der Abmeldung vermittelt. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

 **StoreLogoffTransports** wird in der Regel von der [IMsgStore:: StoreLogoff](imsgstore-storelogoff.md) -Methode eines Speicheranbieters aufgerufen. Sie kann jedoch auch über die **IUnknown:: Release** -Methode des Nachrichtenspeichers aufgerufen werden. Implementieren Sie die **Release** -Methode des Nachrichtenspeichers, damit Sie überprüfen können, ob ein Aufruf von **StoreLogoffTransports** aufgetreten ist. Wenn kein Anruf aufgetreten ist, rufen Sie **StoreLogoffTransports** mit dem LOGOFF_ABORT-Kennzeichen Satz auf. 
  
Der Parameter _lpulFlags_ wird auf ein Flag festgelegt, das angibt, wie der Nachrichtenspeicher heruntergefahren werden muss. Bestimmen Sie die entsprechende Einstellung für _ulFlags_ basierend auf der Einstellung des entsprechenden Parameters im Aufruf von **StoreLogoff**. Das heißt, wenn ein Client Ihre **StoreLogoff** -Methode mit _ulFlags_ auf LOGOFF_ORDERLY festgelegt aufgerufen, sollten Sie **StoreLogoffTransports** mit _ulFlags_ auf LOGOFF_ORDERLY festgelegt aufrufen. 
  
Weitere Informationen zum ABMELDEPROZESS für den Nachrichtenspeicher finden Sie unter [Herunterfahren eines Nachrichtenspeicher Anbieters](shutting-down-a-message-store-provider.md).
  
## <a name="see-also"></a>Siehe auch



[IMsgStore::StoreLogoff](imsgstore-storelogoff.md)
  
[IXPLogon::FlushQueues](ixplogon-flushqueues.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

