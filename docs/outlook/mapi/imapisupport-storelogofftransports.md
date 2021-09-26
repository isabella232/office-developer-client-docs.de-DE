---
title: IMAPISupportStoreLogoffTransports
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.StoreLogoffTransports
api_type:
- COM
ms.assetid: f21fba96-c5ca-4d41-9b93-c7955ab7327f
ms.openlocfilehash: 7b5f3c6d791fc543e892289964fb7ffdab5357e1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620856"
---
# <a name="imapisupportstorelogofftransports"></a>IMAPISupport::StoreLogoffTransports
 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Fordert die geordnete Veröffentlichung eines Nachrichtenspeichers an.
  
```cpp
HRESULT StoreLogoffTransports(
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpulFlags_
  
> [in, out] Eine Bitmaske mit Flags, die steuert, wie die Abmeldung des Nachrichtenspeichers erfolgt. Bei der Eingabe schließen sich alle Flags für diesen Parameter gegenseitig aus. Pro Anruf kann nur eines der folgenden Flags festgelegt werden:
    
LOGOFF_ABORT 
  
> Alle Transportanbieteraktivitäten für diesen Speicher sollten vor der Abmeldung beendet werden. Die Steuerung wird an den Client zurückgegeben, nachdem die Aktivität beendet wurde und der MAPI-Spooler sich vom Speicher abgemeldet hat. Wenn eine Transportaktivität stattfindet, tritt die Abmeldung nicht auf, und das Verhalten des MAPI-Spoolers oder Transportanbieters ändert sich nicht. Wenn derzeit keine Aktivität vorhanden ist, gibt der MAPI-Spooler den Store frei. 
    
LOGOFF_NO_WAIT 
  
> Der MAPI-Spooler sollte den Speicher freigeben und die Steuerung an den Client zurückgeben, unmittelbar nachdem alle ausgehenden E-Mails gesendet wurden, die zum Senden bereit sind. Wenn der Nachrichtenspeicher den Standard-Posteingang aufweist, wird jede in-Process-Nachricht empfangen, und der weitere Empfang wird deaktiviert. 
    
LOGOFF_ORDERLY 
  
> Der MAPI-Spooler sollte den Speicher freigeben und die Steuerung an den Client zurückgeben, unmittelbar nachdem alle ausstehenden Nachrichten verarbeitet wurden. Es sollten keine neuen Nachrichten verarbeitet werden. 
    
LOGOFF_PURGE 
  
> Funktioniert genauso wie das LOGOFF_NO_WAIT Flag. Das flag LOGOFF_PURGE gibt die Steuerung nach Abschluss an den Aufrufer zurück. 
    
LOGOFF_QUIET 
  
> Die Abmeldung sollte nicht erfolgen, wenn eine Transportanbieteraktivität stattfindet. Der Typ der ausgeführten Aktivität wird als Kennzeichen für die Ausgabe zurückgegeben.

Bei der Ausgabe kann der MAPI-Spooler eines oder mehrere der folgenden Flags zurückgeben:
    
LOGOFF_COMPLETE 
  
> Die Abmeldung kann abgeschlossen werden. Alle dem Speicher zugeordneten Ressourcen wurden freigegeben, und das Objekt wurde ungültig. Der MAPI-Spooler hat alle Anforderungen ausgeführt oder führt diese aus. Nur die **IUnknown::Release-Methode** des Nachrichtenspeichers sollte an diesem Punkt aufgerufen werden. 
    
LOGOFF_INBOUND 
  
> Eine Nachricht wird derzeit von einem oder mehreren Transportanbietern in den Speicher eingespart. 
    
LOGOFF_OUTBOUND 
  
> Eine Nachricht wird derzeit von einem oder mehreren Transportanbietern aus dem Store gesendet. 
    
LOGOFF_OUTBOUND_QUEUE 
  
> Derzeit befinden sich Nachrichten in der ausgehenden Warteschlange für den Speicher.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Abmeldeprozedur war erfolgreich.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISupport::StoreLogoffTransports-Methode** ist für Supportobjekte des Nachrichtenspeicheranbieters implementiert. Nachrichtenspeicheranbieter rufen **StoreLogoffTransports** auf, um Clientanwendungen eine gewisse Kontrolle darüber zu geben, wie MAPI Transportanbieteraktivitäten verarbeitet, während ein Nachrichtenspeicher geschlossen wird. 
  
Wenn ein anderer Prozess den Speicher, der für dasselbe Profil abgemeldet werden soll, geöffnet hat, ignoriert MAPI einen Aufruf von **StoreLogoffTransports** und gibt das Flag LOGOFF_COMPLETE im  _Parameter "lpulFlags"_ zurück. 
  
Das Verhalten des Store-Anbieters nach der Rückgabe von **StoreLogoffTransports** sollte auf dem Wert von  _lpulFlags_ basieren, der den Systemstatus angibt und Clientanweisungen für das Abmeldungsverhalten enthält. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

 **StoreLogoffTransports** wird in der Regel von der [IMsgStore::StoreLogoff-Methode](imsgstore-storelogoff.md) eines Store-Anbieters aufgerufen. Sie kann jedoch auch von der **IUnknown::Release-Methode** des Nachrichtenspeichers aufgerufen werden. Implementieren Sie die **Release-Methode** Ihres Nachrichtenspeichers, damit Sie überprüfen können, ob ein Aufruf von **StoreLogoffTransports** stattgefunden hat. Wenn kein Anruf erfolgt ist, rufen **Sie StoreLogoffTransports** auf, wobei das LOGOFF_ABORT-Kennzeichen festgelegt ist. 
  
Der  _lpulFlags-Parameter_ wird auf ein Flag festgelegt, das angibt, wie der Client den Nachrichtenspeicher herunterfahren muss. Bestimmen Sie die entsprechende Einstellung für  _ulFlags_ basierend auf der Einstellung des entsprechenden Parameters im Aufruf von **StoreLogoff**. Das heißt, wenn ein Client Ihre **StoreLogoff-Methode** mit  _ulFlags_ auf LOGOFF_ORDERLY festgelegt hat, sollten Sie **StoreLogoffTransports** aufrufen, wobei  _ulFlags_ auf LOGOFF_ORDERLY festgelegt ist. 
  
Weitere Informationen zum Abmeldevorgang des Nachrichtenspeichers finden Sie unter [Herunterfahren eines Nachrichtenanbieters Store](shutting-down-a-message-store-provider.md).
  
## <a name="see-also"></a>Siehe auch



[IMsgStore::StoreLogoff](imsgstore-storelogoff.md)
  
[IXPLogon::FlushQueues](ixplogon-flushqueues.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

