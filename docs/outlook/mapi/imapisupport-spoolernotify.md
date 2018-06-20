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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 21ea5faaccb81e763d6d062b6ff567db509d9d35
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792418"
---
# <a name="imapisupportspoolernotify"></a>IMAPISupport::SpoolerNotify

  
  
**Betrifft**: Outlook 
  
Benachrichtigt die MAPI-Warteschlange von einer Änderung im Status oder eine Anforderung für den Dienst an. 
  
```cpp
HRESULT SpoolerNotify(
ULONG ulFlags,
LPVOID lpvData
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die den Typ der Benachrichtigung angibt. Transportanbieter können alle außer NOTIFY_NEWMAIL_RECEIVED Kennzeichen festgelegt. nur NOTIFY_NEWMAIL_RECEIVED und NOTIFY_READTOSEND sind gültig für eine Nachricht-Anbieter. Die folgenden Kennzeichen sind für den Parameter _UlFlags_ gültig: 
    
NOTIFY_CONFIG_CHANGE 
  
> Eine Anforderung zum Ändern der Konfiguration der Adressbuchhierarchie registriert. 
    
NOTIFY_CRITICAL_ERROR 
  
> Der Transportdienst aufgetretenen Fehler nicht wiederhergestellt. Da NOTIFY_SENTDEFERRED und NOTIFY_CRITICAL_ERROR den Parameter _LpvData_ für Transport Anbieter Anrufe verwenden, sind diese Flags schließen sich gegenseitig aus. 
    
NOTIFY_CRITSEC 
  
> Fordert einen kritischen Abschnitt für den Transportanbieter. Der Parameter _LpvData_ ist nicht definiert und NULL sein. 
    
NOTIFY_NEWMAIL 
  
> Die MAPI-Warteschlange sollten unter der nächsten verfügbaren Zeit neu empfangenen Nachrichten herunterladen. Der Parameter _LpvData_ ist nicht definiert und auf NULL festgelegt werden sollte. 
    
NOTIFY_NEWMAIL_RECEIVED 
  
> Eine neue Nachricht wurde im Nachrichtenspeicher empfangen. Der Parameter _LpvData_ verweist auf eine [NEWMAIL_NOTIFICATION](newmail_notification.md) -Struktur, die die Nachricht beschreibt. Dieses Kennzeichen werden für die Nachricht-Anbieter, die eng mit Anbietern Transport verknüpft sind, und werden ignoriert, wenn der Anbieter mit dem Flag MAPI_NO_MAIL angemeldet ist. 
    
NOTIFY_NONCRIT 
  
> Gibt einen kritischen Abschnitt, der mit einem vorherigen Aufruf von **SpoolerNotify** , mit _UlFlags_ auf NOTIFY_CRITSEC festgelegt abgerufen wurde. Der Parameter _LpvData_ ist nicht definiert und auf NULL festgelegt werden sollte. 
    
NOTIFY_READYTOSEND 
  
> Der Informationsdienst Transport oder einer Nachricht ist bereit zum Senden von Nachrichten. Der Parameter _LpvData_ ist nicht definiert und auf NULL festgelegt werden sollte. 
    
NOTIFY_SENTDEFERRED 
  
> Jetzt sollte eine zuvor zurückgestellte Nachricht gesendet werden, und der Adressbuchhierarchie benachrichtigt werden soll, wenn die Nachricht bereitgestellt werden, mit einem Aufruf der [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) -Methode ist. Die Eintrags-ID der zurückgestellte Nachricht ist in eine [SBinary](sbinary.md) -Struktur, die auf den _LpvData_enthalten. Da NOTIFY_SENTDEFERRED und NOTIFY_CRITICAL_ERROR den _LpvData_ -Parameter verwenden, sind diese Flags schließen sich gegenseitig aus. 
    
 _lpvData_
  
> [in] Ein Zeiger auf die zugehörigen Daten für eine Benachrichtigung gelten. Der _LpvData_ -Parameter verweist auf gültige Daten nur, wenn die folgenden Kennzeichen festgelegt werden (_LpvData_ ist NULL, wenn _UlFlags_ auf anderen Benachrichtigungstypen festgelegt ist): 
    
|**_UlFlags_ -Einstellung**|**_LpvData_ Wert**|
|:-----|:-----|
|NOTIFY_CRITICAL_ERROR  <br/> |Informationen zu dem Fehler.  <br/> |
|NOTIFY_NEWMAIL_RECEIVED  <br/> |Eine **NEWMAIL_NOTIFICATION** -Struktur, die Informationen über die neu gesendete Nachricht enthält.  <br/> |
|NOTIFY_SENTDEFERRED  <br/> |Eine **SBinary** -Struktur, die Eintrags-ID der zurückgestellte Nachricht enthält.  <br/> |
   
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Benachrichtigung war erfolgreich.
    
## <a name="remarks"></a>Hinweise

Die **IMAPISupport::SpoolerNotify** -Methode wird für die Nachricht implementiert speichern und transport-Provider Unterstützungsobjekte. Diese Anbieter rufen Sie **SpoolerNotify** , um die MAPI-Warteschlange von einer Änderung im Status oder eine Anforderung für den Dienst zu benachrichtigen. **SpoolerNotify** wird hauptsächlich von Transportanbieter aufgerufen und können jederzeit während der Sitzung aufgerufen werden. 
  
## <a name="notes-to-transport-providers"></a>Hinweise für Transport-Anbieter

Wenn Sie Ihrer Anbieterkonfiguration Transport geändert haben, rufen Sie **SpoolerNotify** und _UlFlags_ auf NOTIFY_CONFIG_CHANGED festgelegt. Durch Aufrufen der [IXPLogon::AddressTypes](ixplogon-addresstypes.md) -Methode, um die Abfrage für eine Änderung in unterstützte-Adresstypen auf **SpoolerNotify** reagiert. 
  
Wenn Sie einen kritischen Abschnitt um sicherzustellen, dass ununterbrochenen Verarbeitung benötigen, rufen Sie **SpoolerNotify** mit _UlFlags_ auf NOTIFY_CRITSEC festgelegt. Dieses Flag festlegen informiert der MAPI-Warteschlange an, dass die Methoden [IXPLogon::Idle](ixplogon-idle.md) und [IXPLogon::Poll](ixplogon-poll.md) nicht aufgerufen werden soll. Während Sie einen kritischen Abschnitt öffnen haben, MAPI_E_BUSY zurückgeben, wenn die [IMAPIStatus::ValidateState](imapistatus-validatestate.md) -Methode aufgerufen wird. Wenn Sie mit den kritischen Abschnitt fertig sind, stellen Sie einen weiteren Anruf zu **SpoolerNotify** mit _UlFlags_ auf NOTIFY_NONCRIT festgelegt. 
  
Wenn Ihre remote Adressbuchhierarchie wird gerade Nachrichten hochladen, müssen Sie einen Benutzer geben Sie eine Telefonnummer ein, um die remote-Verbindung zu ermöglichen. Bevor Sie das Dialogfeld Feld Verfahren durchlaufen haben, sollten Sie einen kritischen Abschnitt deklarieren. Wenn der Benutzer das Dialogfeld geschlossen wird, sollte, auf dem Sie den kritischen Abschnitt freigeben wird das Dialogfeld Feld Verfahren beendet.
  
Wenn Sie _UlFlags_ auf NOTIFY_CRITICAL_ERROR festlegen, wird die MAPI-Warteschlange keine weiteren Aufrufe an den Anbieter mit Ausnahme von an freigegeben werden soll. Wenn Sie **SpoolerNotify** mit NOTIFY_CRITICAL_ERROR legen Sie die [IXPLogon::StartMessage](ixplogon-startmessage.md) oder [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) -Methoden aufrufen, mit einem entsprechenden Fehlerwert zurückgeben, aus der **StartMessage** oder ** SubmitMessage ** aufrufen unmittelbar nach dem Aufruf **SpoolerNotify** . 
  
Wenn Ihre Adressbuchhierarchie aus einer Bedingung, die zuvor Fehler verursacht hat wiederhergestellt, rufen Sie **SpoolerNotify** mit _UlFlags_ auf NOTIFY_READYTOSEND festgelegt. Dieses Kennzeichen gibt an, dass der Anbieter erneut bereit, um Nachrichten zu verarbeiten. 
  
## <a name="notes-to-message-store-providers"></a>Hinweise für Nachrichtenspeicher-Anbieter

Rufen Sie **SpoolerNotify**, das NOTIFY_READYTOSEND-Flag in _UlFlags_, übergeben, bevor Sie Ihre erste [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md) in **IMessage::SubmitMessage**aufrufen. Dieser Aufruf von **SpoolerNotify** muss nur einmal pro Sitzung vorgenommen werden sollen. 
  
Wenn Ihre Nachrichtenanbieter eng verknüpft ist mit einer Transport-Anbieter und Sie rufen **SpoolerNotify** _UlFlags_ auf NOTIFY_NEWMAIL_RECEIVED festgelegt, die MAPI-Warteschlange wird die neue Nachricht geöffnet, und mit der Verarbeitung der neuen Nachricht Hook-Funktion beginnt. Nach Abschluss der Verarbeitung Ruft die MAPI-Warteschlange die [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) -Methode, um Sie der neuen Nachricht informiert. 
  
Weitere Informationen zum Aufrufen von **SpoolerNotify**finden Sie unter den folgenden Themen:
  
- [Implementieren der FlushQueues-Methode](implementing-the-flushqueues-method.md)
    
- [Interaktion mit der MAPI-Warteschlange](interacting-with-the-mapi-spooler.md)
    
- [Nachricht Empfang Modell](message-reception-model.md)
    
## <a name="see-also"></a>Siehe auch



[IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md)
  
[IXPLogon::StartMessage](ixplogon-startmessage.md)
  
[IXPLogon::SubmitMessage](ixplogon-submitmessage.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

