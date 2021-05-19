---
title: IMAPISupportSpoolerNotify
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.SpoolerNotify
api_type:
- COM
ms.assetid: d4f153b2-939f-4153-85fb-dc510193848c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 99377d63b4b5cf8731809446b70770f0c24231ed
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423769"
---
# <a name="imapisupportspoolernotify"></a>IMAPISupport::SpoolerNotify

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Benachrichtigt den MAPI-Spooler über eine Statusänderung oder eine Dienstanforderung. 
  
```cpp
HRESULT SpoolerNotify(
ULONG ulFlags,
LPVOID lpvData
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die den Typ der Benachrichtigung angibt. Transportanbieter können alle Flags mit Ausnahme von NOTIFY_NEWMAIL_RECEIVED. Nur NOTIFY_NEWMAIL_RECEIVED und NOTIFY_READTOSEND sind für Nachrichtenspeicheranbieter gültig. Die folgenden Kennzeichen sind für den  _ulFlags-Parameter_ gültig: 
    
NOTIFY_CONFIG_CHANGE 
  
> Registriert eine Anforderung zum Ändern der Konfiguration des Transportanbieters. 
    
NOTIFY_CRITICAL_ERROR 
  
> Beim Transportanbieter ist ein nicht behebbarer Fehler aufgetreten. Da sowohl NOTIFY_SENTDEFERRED als auch NOTIFY_CRITICAL_ERROR  _den Parameter lpvData_ für Transportanbieteraufrufe verwenden, schließen sich diese Flags gegenseitig aus. 
    
NOTIFY_CRITSEC 
  
> Fordert einen kritischen Abschnitt für den Transportanbieter an. Der  _lpvData-Parameter_ ist nicht definiert und sollte NULL sein. 
    
NOTIFY_NEWMAIL 
  
> Der MAPI-Spooler sollte alle neu empfangenen Nachrichten zum nächsten verfügbaren Zeitpunkt herunterladen. Der  _lpvData-Parameter_ ist nicht definiert und sollte auf NULL festgelegt werden. 
    
NOTIFY_NEWMAIL_RECEIVED 
  
> Im Nachrichtenspeicher wurde eine neue Nachricht empfangen. Der  _lpvData-Parameter_ zeigt auf [eine NEWMAIL_NOTIFICATION,](newmail_notification.md) die die Nachricht beschreibt. Dieses Flag wird für Nachrichtenspeicheranbieter verwendet, die eng mit Transportanbietern gekoppelt sind und ignoriert werden, wenn der Speicheranbieter mit dem MAPI_NO_MAIL angemeldet ist. 
    
NOTIFY_NONCRIT 
  
> Gibt einen kritischen Abschnitt frei, der mit einem vorherigen Aufruf von **SpoolerNotify** mit  _ulFlags_ auf NOTIFY_CRITSEC. Der  _lpvData-Parameter_ ist nicht definiert und sollte auf NULL festgelegt werden. 
    
NOTIFY_READYTOSEND 
  
> Der Transport- oder Nachrichtenspeicheranbieter kann Nachrichten senden. Der  _lpvData-Parameter_ ist nicht definiert und sollte auf NULL festgelegt werden. 
    
NOTIFY_SENTDEFERRED 
  
> Nun sollte eine zuvor verzögerte Nachricht gesendet werden, und der Transportanbieter sollte benachrichtigt werden, wenn die Nachricht mithilfe eines Aufrufs der [IXPLogon::SubmitMessage-Methode](ixplogon-submitmessage.md) zugestellt werden kann. Der Eintragsbezeichner der verzögerten Nachricht ist in einer [SBinary-Struktur](sbinary.md) enthalten, auf die von _lpvData verwiesen wird._ Da sowohl NOTIFY_SENTDEFERRED als auch NOTIFY_CRITICAL_ERROR  _lpvData-Parameter_ verwenden, schließen sich diese Flags gegenseitig aus. 
    
 _lpvData_
  
> [in] Ein Zeiger auf zugeordnete Daten, die auf eine Benachrichtigung anwendbar sind. Der  _lpvData-Parameter_ verweist nur dann auf gültige Daten, wenn die folgenden Flags festgelegt sind (_lpvData_ ist NULL, wenn  _ulFlags_ auf die anderen Benachrichtigungstypen festgelegt ist): 
    
|**_ulFlags-Einstellung_**|**_lpvData-Wert_**|
|:-----|:-----|
|NOTIFY_CRITICAL_ERROR  <br/> |Informationen zum Fehler.  <br/> |
|NOTIFY_NEWMAIL_RECEIVED  <br/> |Eine **NEWMAIL_NOTIFICATION,** die Informationen zur neu zugestellten Nachricht enthält.  <br/> |
|NOTIFY_SENTDEFERRED  <br/> |Eine **SBinary-Struktur,** die den Eintragsbezeichner der verzögerten Nachricht enthält.  <br/> |
   
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Benachrichtigung war erfolgreich.
    
## <a name="remarks"></a>Hinweise

Die **IMAPISupport::SpoolerNotify-Methode** wird für Nachrichtenspeicher- und Transportanbieterunterstützungsobjekte implementiert. Diese Anbieter rufen **SpoolerNotify auf,** um den MAPI-Spooler über eine Statusänderung oder eine Dienstanforderung zu informieren. **SpoolerNotify** wird hauptsächlich von Transportanbietern aufgerufen und kann jederzeit während der Sitzung aufgerufen werden. 
  
## <a name="notes-to-transport-providers"></a>Hinweise zu Transportanbietern

Wenn Sie ihre Konfiguration des Transportanbieters geändert haben, rufen **Sie SpoolerNotify** auf, und legen Sie  _ulFlags auf_ NOTIFY_CONFIG_CHANGED. **SpoolerNotify** antwortet, indem die [IXPLogon::AddressTypes-Methode](ixplogon-addresstypes.md) zum Abfragen einer Änderung der unterstützten Adresstypen aufruft. 
  
Wenn Sie einen kritischen Abschnitt benötigen, um eine unterbrechungsfreie Verarbeitung sicherzustellen, rufen **Sie SpoolerNotify** auf, wenn  _ulFlags_ auf NOTIFY_CRITSEC. Durch Festlegen dieses Kennzeichens wird der MAPI-Spooler darüber informiert, dass er die [Methoden IXPLogon::Idle](ixplogon-idle.md) und [IXPLogon::P oll](ixplogon-poll.md) nicht aufrufen sollte. Wenn Sie einen kritischen Abschnitt geöffnet haben, geben MAPI_E_BUSY zurück, wenn die [IMAPIStatus::ValidateState-Methode](imapistatus-validatestate.md) aufgerufen wird. Wenn Sie den kritischen Abschnitt abgeschlossen haben, rufen Sie **SpoolerNotify** erneut auf, und  _ulFlags_ ist auf NOTIFY_NONCRIT. 
  
Wenn Ihr Remotetransportanbieter beispielsweise Nachrichten hochladet, müssen Sie möglicherweise zulassen, dass ein Benutzer eine Telefonnummer eingeben kann, um die Remoteverbindung herzustellen. Bevor Sie die Dialogfeldprozedur durchschleifen, sollten Sie einen kritischen Abschnitt deklarieren. Wenn der Benutzer das Dialogfeld schließt und die Dialogfeldprozedur beendet, sollten Sie den kritischen Abschnitt los.
  
Wenn Sie  _ulFlags_ auf NOTIFY_CRITICAL_ERROR festlegen, ruft der MAPI-Spooler keine weiteren Aufrufe an den Anbieter ab, es sei denn, er wird freigegeben. Wenn Sie **SpoolerNotify** mit NOTIFY_CRITICAL_ERROR von der [IXPLogon::StartMessage-](ixplogon-startmessage.md) oder [IXPLogon::SubmitMessage-Methode](ixplogon-submitmessage.md) aufrufen, geben Sie mit einem entsprechenden Fehlerwert aus dem **StartMessage-** oder ** SubmitMessage **-Aufruf unmittelbar nach dem **SpoolerNotify-Aufruf** zurück. 
  
Wenn Ihr Transportanbieter von einer Bedingung wiederhergestellt wurde, die zuvor zu einem Fehler führte, rufen Sie **SpoolerNotify** auf, wenn  _ulFlags_ auf NOTIFY_READYTOSEND. Dieses Flag gibt an, dass der Anbieter wieder für die Verarbeitung von Nachrichten bereit ist. 
  
## <a name="notes-to-message-store-providers"></a>Hinweise zu Nachrichtenanbietern Store

Rufen **Sie SpoolerNotify** auf, übergeben Sie das NOTIFY_READYTOSEND-Flag in _ulFlags,_ bevor Sie den ersten Aufruf von [IMAPISupport::P repareSubmit](imapisupport-preparesubmit.md) in **IMessage::SubmitMessage machen.** Dieser Aufruf **von SpoolerNotify** muss nur einmal pro Sitzung vorgenommen werden. 
  
Wenn Ihr Nachrichtenspeicheranbieter eng mit einem Transportanbieter gekoppelt ist und **Sie SpoolerNotify** mit  _ulFlags_ aufrufen, die auf NOTIFY_NEWMAIL_RECEIVED festgelegt sind, öffnet der MAPI-Spooler die neue Nachricht und beginnt mit der Verarbeitung der neuen Message Hook-Funktion. Nach Abschluss der Verarbeitung ruft der MAPI-Spooler die [IMsgStore::NotifyNewMail-Methode](imsgstore-notifynewmail.md) auf, um Sie über Ihre eigene neue Nachricht zu informieren. 
  
Weitere Informationen zum Aufrufen von **SpoolerNotify** finden Sie in den folgenden Themen:
  
- [Implementieren der FlushQueues-Methode](implementing-the-flushqueues-method.md)
    
- [Interagieren mit dem MAPI-Spooler](interacting-with-the-mapi-spooler.md)
    
- [Nachrichtenempfangsmodell](message-reception-model.md)
    
## <a name="see-also"></a>Siehe auch



[IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md)
  
[IXPLogon::StartMessage](ixplogon-startmessage.md)
  
[IXPLogon::SubmitMessage](ixplogon-submitmessage.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

