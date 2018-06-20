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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6624c4abf05dc7df9fc79df43f1d0fe76251d052
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792439"
---
# <a name="imapisupportstorelogofftransports"></a>IMAPISupport::StoreLogoffTransports

  
  
**Betrifft**: Outlook 
  
Fordert die ordnungsgemäße Version von eines Nachrichtenspeichers.
  
```cpp
HRESULT StoreLogoffTransports(
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpulFlags_
  
> [in, out] Eine Bitmaske aus Flags, die steuert, wie die Nachricht Store Abmeldung erfolgt. Bei der Eingabe sind alle Flags für diesen Parameter schließen sich gegenseitig aus. pro Aufruf kann nur eine der folgenden Werte festgelegt werden:
    
LOGOFF_ABORT 
  
> Alle Anbieter transportaktivität für diesen Informationsspeicher sollten vor der Abmeldung beendet werden. Steuerelement wird an den Client zurückgegeben, nachdem die Aktivität beendet wurde und die MAPI-Warteschlange hat den Speicher abgemeldet. Wenn keine transportaktivität stattfindet, die Abmeldung tritt nicht auf, und keine Änderung in das MAPI-Warteschlange oder Transport Anbieter Verhalten tritt auf. Wenn derzeit keine Aktivität vorhanden ist, gibt die MAPI-Warteschlange den Speicher frei. 
    
LOGOFF_NO_WAIT 
  
> Die MAPI-Warteschlange sollte lassen Sie den Speicher und sofort gesendet erst, nachdem alle ausgehender Nachrichten, der gesendet werden kann, wird die Steuerung an den Client zurück. Weist der Nachrichtenspeicher der standardmäßige Posteingang, alle in-Process-Nachricht empfangen, und klicken Sie dann weitere Empfang ist deaktiviert. 
    
LOGOFF_ORDERLY 
  
> Die MAPI-Warteschlange sollte Version den Speicher und die Steuerung an den Client zurückgegeben, unmittelbar nachdem alle ausstehenden Nachrichten abgeschlossen sind verarbeiten. Keine neuen Nachrichten verarbeitet werden soll. 
    
LOGOFF_PURGE 
  
> Funktioniert das Flag LOGOFF_NO_WAIT identisch. Das Flag LOGOFF_PURGE gibt das Steuerelement mit dem Anrufer nach Abschluss zurück. 
    
LOGOFF_QUIET 
  
> Das Abmelden sollte nicht auftreten, wenn alle Anbieter transportaktivität stattfindet. Der Typ der Aktivität stattfinden wird als Flag auf Ausgabe zurückgegeben.
    
    On output, MAPI spooler can return one or more of the following flags:
    
LOGOFF_COMPLETE 
  
> Führen Sie das Abmelden kann. Das Objekt wurde für ungültig erklärt wurde, und alle mit dem Speicher zugeordnete Ressourcen veröffentlicht wurden. Die MAPI-Warteschlange durchgeführten oder führt alle Anfragen. Nur die Nachrichtenspeicher **IUnknown** -Methode sollte zu diesem Zeitpunkt aufgerufen werden. 
    
LOGOFF_INBOUND 
  
> Eine Nachricht stammt aktuell in den Speicher mindestens einen Transportanbieter. 
    
LOGOFF_OUTBOUND 
  
> Eine Nachricht wird derzeit aus dem Speicher von Anbietern für eine oder mehrere Transport gesendet. 
    
LOGOFF_OUTBOUND_QUEUE 
  
> Meldungen sind in die Warteschlange für den Speicher für ausgehende derzeit verfügbar.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Das Abmelden Verfahren erfolgreich war.
    
## <a name="remarks"></a>Hinweise

Die **IMAPISupport::StoreLogoffTransports** -Methode wird für Message Store Anbieter Unterstützungsobjekte implementiert. Nachricht-Anbieter anrufen **StoreLogoffTransports** um-Clientanwendungen können einige Steuern wie MAPI-Handles Transport Anbieter Aktivität als Nachrichtenspeicher geschlossen wird. 
  
Weist einem anderen Prozess auf den Speicher zu öffnen, für das gleiche Profil abgemeldet werden, MAPI einen Anruf an **StoreLogoffTransports** ignoriert und das Flag LOGOFF_COMPLETE in der _LpulFlags_ -Parameter zurückgegeben. 
  
Das Verhalten des Anbieters zur Rückgabe von **StoreLogoffTransports** folgen sollte auf den Wert der _LpulFlags_, basieren die anzeigt, Systemstatus und Client-Anweisungen für die Abmeldung Verhalten übermittelt. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

 **StoreLogoffTransports** wird normalerweise aus einem Speicheranbieter [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) -Methode aufgerufen. Es kann jedoch auch von der **IUnknown** -Methode des Nachrichtenspeichers aufgerufen werden. Implementieren Sie die **Release** -Methode des Nachrichtenspeichers, damit Sie überprüfen können, unabhängig davon, ob ein Aufruf von **StoreLogoffTransports** stattgefunden hat. Wenn Sie ein Anruf nicht aufgetreten ist, rufen Sie **StoreLogoffTransports** mit der LOGOFF_ABORT-Flag. 
  
Der Parameter _LpulFlags_ ist auf ein Flag festgelegt, der angibt, wie der Client den Nachrichtenspeicher heruntergefahren werden, erfordert. Bestimmen Sie die entsprechende Einstellung für _UlFlags_ basierend auf der Einstellung des entsprechenden Parameters im Aufruf **StoreLogoff**. D. h., wenn ein Client mit _UlFlags_ auf LOGOFF_ORDERLY festgelegt Ihrer **StoreLogoff** -Methode aufgerufen, sollten Sie **StoreLogoffTransports** mit _UlFlags_ legen auf LOGOFF_ORDERLY aufrufen. 
  
Weitere Informationen zu der Nachricht Speichervorgang Abmeldung wird finden Sie unter [Herunterfahren nach unten einer Nachricht speichern-Anbieter](shutting-down-a-message-store-provider.md).
  
## <a name="see-also"></a>Siehe auch



[IMsgStore::StoreLogoff](imsgstore-storelogoff.md)
  
[IXPLogon::FlushQueues](ixplogon-flushqueues.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

