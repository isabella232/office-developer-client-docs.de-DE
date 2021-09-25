---
title: IMAPISupportSpoolerNotify
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.SpoolerNotify
api_type:
- COM
ms.assetid: d4f153b2-939f-4153-85fb-dc510193848c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6f775446562dcc004885af1f51f388220129429e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596064"
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
  
> [in] Eine Bitmaske mit Flags, die den Typ der Benachrichtigung angibt. Transportanbieter können alle Flags mit Ausnahme von NOTIFY_NEWMAIL_RECEIVED festlegen. nur NOTIFY_NEWMAIL_RECEIVED und NOTIFY_READTOSEND sind für Nachrichtenspeicheranbieter gültig. Die folgenden Flags sind für den  _ulFlags-Parameter_ gültig: 
    
NOTIFY_CONFIG_CHANGE 
  
> Registriert eine Anforderung zum Ändern der Konfiguration des Transportanbieters. 
    
NOTIFY_CRITICAL_ERROR 
  
> Beim Transportanbieter ist ein nicht behebbarer Fehler aufgetreten. Da sowohl NOTIFY_SENTDEFERRED als auch NOTIFY_CRITICAL_ERROR den  _Parameter "lpvData"_ für Transportanbieteraufrufe verwenden, schließen sich diese Flags gegenseitig aus. 
    
NOTIFY_CRITSEC 
  
> Fordert einen kritischen Abschnitt für den Transportanbieter an. Der  _lpvData-Parameter_ ist nicht definiert und sollte NULL sein. 
    
NOTIFY_NEWMAIL 
  
> Der MAPI-Spooler sollte alle neu empfangenen Nachrichten zum nächsten verfügbaren Zeitpunkt herunterladen. Der  _lpvData-Parameter_ ist nicht definiert und sollte auf NULL festgelegt werden. 
    
NOTIFY_NEWMAIL_RECEIVED 
  
> Eine neue Nachricht wurde im Nachrichtenspeicher empfangen. Der  _lpvData-Parameter_ verweist auf eine [NEWMAIL_NOTIFICATION](newmail_notification.md) Struktur, die die Nachricht beschreibt. Dieses Flag wird für Nachrichtenspeicheranbieter verwendet, die eng mit Transportanbietern gekoppelt sind, und wird ignoriert, wenn der Speicheranbieter mit dem festgelegten MAPI_NO_MAIL Flag angemeldet ist. 
    
NOTIFY_NONCRIT 
  
> Gibt einen kritischen Abschnitt frei, der mit einem vorherigen Aufruf von **SpoolerNotify** mit  _ulFlags_ auf NOTIFY_CRITSEC festgelegt wurde. Der  _lpvData-Parameter_ ist nicht definiert und sollte auf NULL festgelegt werden. 
    
NOTIFY_READYTOSEND 
  
> Der Transport- oder Nachrichtenspeicheranbieter ist bereit, Nachrichten zu senden. Der  _lpvData-Parameter_ ist nicht definiert und sollte auf NULL festgelegt werden. 
    
NOTIFY_SENTDEFERRED 
  
> Eine zuvor verzögerte Nachricht sollte jetzt gesendet werden, und der Transportanbieter sollte benachrichtigt werden, wenn die Nachricht mithilfe eines Aufrufs der [IXPLogon::SubmitMessage-Methode](ixplogon-submitmessage.md) zugestellt werden kann. Der Eintragsbezeichner der verzögerten Nachricht ist in einer [SBinary-Struktur enthalten,](sbinary.md) auf die durch  _lpvData_ verwiesen wird. Da sowohl NOTIFY_SENTDEFERRED als auch NOTIFY_CRITICAL_ERROR den  _Parameter "lpvData"_ verwenden, schließen sich diese Flags gegenseitig aus. 
    
 _lpvData_
  
> [in] Ein Zeiger auf zugeordnete Daten, die für eine Benachrichtigung anwendbar sind. Der  _lpvData-Parameter_ verweist nur auf gültige Daten, wenn die folgenden Flags festgelegt sind (_lpvData_ ist NULL, wenn  _ulFlags_ auf die anderen Benachrichtigungstypen festgelegt ist): 
    
|**_ulFlags-Einstellung_**|**_lpvData-Wert_**|
|:-----|:-----|
|NOTIFY_CRITICAL_ERROR  <br/> |Informationen zu dem Fehler.  <br/> |
|NOTIFY_NEWMAIL_RECEIVED  <br/> |Eine **NEWMAIL_NOTIFICATION** Struktur, die Informationen über die neu zugestellte Nachricht enthält.  <br/> |
|NOTIFY_SENTDEFERRED  <br/> |Eine **SBinary-Struktur,** die den Eintragsbezeichner der verzögerten Nachricht enthält.  <br/> |
   
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Benachrichtigung war erfolgreich.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPISupport::SpoolerNotify-Methode** ist für Nachrichtenspeicher- und Transportanbieter-Supportobjekte implementiert. Diese Anbieter rufen **SpoolerNotify** auf, um den MAPI-Spooler über eine Statusänderung oder eine Dienstanforderung zu benachrichtigen. **SpoolerNotify** wird in erster Linie von Transportanbietern aufgerufen und kann jederzeit während der Sitzung aufgerufen werden. 
  
## <a name="notes-to-transport-providers"></a>Hinweise zu Transportanbietern

Wenn Sie ihre Transportanbieterkonfiguration geändert haben, rufen Sie **SpoolerNotify** auf, und legen Sie  _ulFlags_ auf NOTIFY_CONFIG_CHANGED fest. **SpoolerNotify** antwortet, indem die [IXPLogon::AddressTypes-Methode](ixplogon-addresstypes.md) aufgerufen wird, um eine Änderung der unterstützten Adresstypen abfragt. 
  
Wenn Sie einen kritischen Abschnitt benötigen, um eine unterbrechungsfreie Verarbeitung sicherzustellen, rufen Sie **SpoolerNotify** auf, wobei  _ulFlags_ auf NOTIFY_CRITSEC festgelegt ist. Durch Festlegen dieses Kennzeichens wird der MAPI-Spooler darüber informiert, dass die Methoden [IXPLogon::Idle](ixplogon-idle.md) und [IXPLogon::P oll](ixplogon-poll.md) nicht aufgerufen werden sollen. Während Sie einen kritischen Abschnitt geöffnet haben, geben Sie MAPI_E_BUSY zurück, wenn die [IMAPIStatus::ValidateState-Methode](imapistatus-validatestate.md) aufgerufen wird. Wenn Sie mit dem kritischen Abschnitt fertig sind, führen Sie einen weiteren Aufruf von **SpoolerNotify** durch, wobei  _ulFlags_ auf NOTIFY_NONCRIT festgelegt ist. 
  
Wenn z. B. Ihr Remote-Transportanbieter Nachrichten hochlädt, müssen Sie möglicherweise zulassen, dass ein Benutzer eine Telefonnummer eingibt, um die Remoteverbindung herzustellen. Bevor Sie die Dialogfeldprozedur durchlaufen, sollten Sie einen kritischen Abschnitt deklarieren. Wenn der Benutzer das Dialogfeld schließt und die Dialogfeldprozedur beendet, sollten Sie den kritischen Abschnitt freigeben.
  
Wenn Sie  _ulFlags_ auf NOTIFY_CRITICAL_ERROR festlegen, führt der MAPI-Spooler keine weiteren Aufrufe an den Anbieter aus, außer ihn freizugeben. Wenn Sie **SpoolerNotify** mit NOTIFY_CRITICAL_ERROR aufrufen, die über die Methoden [IXPLogon::StartMessage](ixplogon-startmessage.md) oder [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) festgelegt wurden, geben Sie unmittelbar nach dem **SpoolerNotify-Aufruf** einen entsprechenden Fehlerwert aus der **StartMessage** oder ** SubmitMessage ** zurück. 
  
Wenn Ihr Transportanbieter von einer Bedingung wiederhergestellt wurde, die zuvor zu einem Fehler führte, rufen Sie **SpoolerNotify** auf, wobei  _ulFlags_ auf NOTIFY_READYTOSEND festgelegt ist. Dieses Kennzeichen gibt an, dass der Anbieter wieder bereit für die Verarbeitung von Nachrichten ist. 
  
## <a name="notes-to-message-store-providers"></a>Hinweise zu Nachrichtenanbietern Store

Call **SpoolerNotify**, passing the NOTIFY_READYTOSEND flag in  _ulFlags_, before you make your first call to [IMAPISupport::P repareSubmit](imapisupport-preparesubmit.md) in **IMessage::SubmitMessage**. Dieser Aufruf von **SpoolerNotify** muss nur einmal pro Sitzung erfolgen. 
  
Wenn Ihr Nachrichtenspeicheranbieter eng mit einem Transportanbieter gekoppelt ist und Sie **SpoolerNotify** mit  _ulFlags_ aufrufen, die auf NOTIFY_NEWMAIL_RECEIVED festgelegt sind, öffnet der MAPI-Spooler die neue Nachricht und beginnt mit der Verarbeitung der neuen Nachrichtenhookfunktion. Nach Abschluss der Verarbeitung ruft der MAPI-Spooler die [IMsgStore::NotifyNewMail-Methode](imsgstore-notifynewmail.md) auf, um Sie über Ihre eigene neue Nachricht zu informieren. 
  
Weitere Informationen zum Aufrufen von **SpoolerNotify** finden Sie in den folgenden Themen:
  
- [Implementieren der FlushQueues-Methode](implementing-the-flushqueues-method.md)
    
- [Interagieren mit dem MAPI-Spooler](interacting-with-the-mapi-spooler.md)
    
- [Nachrichtenempfangsmodell](message-reception-model.md)
    
## <a name="see-also"></a>Siehe auch



[IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md)
  
[IXPLogon::StartMessage](ixplogon-startmessage.md)
  
[IXPLogon::SubmitMessage](ixplogon-submitmessage.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

