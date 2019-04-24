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
ms.openlocfilehash: 99377d63b4b5cf8731809446b70770f0c24231ed
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326285"
---
# <a name="imapisupportspoolernotify"></a>IMAPISupport::SpoolerNotify

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Benachrichtigt den MAPI-Spooler über eine Änderung des Status oder eine Anforderung für Dienst. 
  
```cpp
HRESULT SpoolerNotify(
ULONG ulFlags,
LPVOID lpvData
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> in Eine Bitmaske von Flags, die den Benachrichtigungstyp angibt. Transport Anbieter können alle Flags festlegen, mit Ausnahme von NOTIFY_NEWMAIL_RECEIVED; nur NOTIFY_NEWMAIL_RECEIVED und NOTIFY_READTOSEND sind für Nachrichtenspeicher Anbieter gültig. Die folgenden Flags sind für den _ulFlags_ -Parameter gültig: 
    
NOTIFY_CONFIG_CHANGE 
  
> Registriert eine Anforderung zum Ändern der Konfiguration des Transportanbieters. 
    
NOTIFY_CRITICAL_ERROR 
  
> Ein nicht behebbarer Fehler ist beim Transportanbieter aufgetreten. Da sowohl NOTIFY_SENTDEFERRED als auch NOTIFY_CRITICAL_ERROR den _lpvData_ -Parameter für Transportanbieter Aufrufe verwenden, schließen sich diese Flags gegenseitig aus. 
    
NOTIFY_CRITSEC 
  
> Fordert einen kritischen Abschnitt für den Transportanbieter an. Der _lpvData_ -Parameter ist nicht definiert und sollte NULL sein. 
    
NOTIFY_NEWMAIL 
  
> Der MAPI-Spooler sollte alle neu empfangenen Nachrichten zum nächsten verfügbaren Zeitpunkt herunterladen. Der Parameter _lpvData_ ist nicht definiert und sollte auf NULL festgelegt werden. 
    
NOTIFY_NEWMAIL_RECEIVED 
  
> Im Nachrichtenspeicher wurde eine neue Nachricht empfangen. Der _lpvData_ -Parameter verweist auf eine [NEWMAIL_NOTIFICATION](newmail_notification.md) -Struktur, die die Nachricht beschreibt. Dieses Flag wird für Nachrichtenspeicher Anbieter verwendet, die eng mit Transportanbietern gekoppelt sind, und wird ignoriert, wenn der Informationsspeicher Anbieter mit dem MAPI_NO_MAIL-Kennzeichen Satz angemeldet ist. 
    
NOTIFY_NONCRIT 
  
> Gibt einen kritischen Abschnitt zurück, der mit einem vorherigen Aufruf von **SpoolerNotify** abgerufen wurde, wobei _ulFlags_ auf NOTIFY_CRITSEC festgelegt ist. Der Parameter _lpvData_ ist nicht definiert und sollte auf NULL festgelegt werden. 
    
NOTIFY_READYTOSEND 
  
> Der Transport-oder Nachrichtenspeicher Anbieter ist bereit, Nachrichten zu senden. Der Parameter _lpvData_ ist nicht definiert und sollte auf NULL festgelegt werden. 
    
NOTIFY_SENTDEFERRED 
  
> Eine zuvor verzögerte Nachricht sollte jetzt gesendet werden, und der Transportanbieter sollte benachrichtigt werden, wenn die Nachricht mithilfe eines Aufrufs der [IXPLogon:: SubmitMessage](ixplogon-submitmessage.md) -Methode bereitgestellt werden kann. Der Eintragsbezeichner der verzögerten Nachricht ist in einer [SBinary](sbinary.md) -Struktur enthalten, auf die durch _lpvData_verwiesen wird. Da sowohl NOTIFY_SENTDEFERRED als auch NOTIFY_CRITICAL_ERROR den _lpvData_ -Parameter verwenden, schließen sich diese Flags gegenseitig aus. 
    
 _lpvData_
  
> in Ein Zeiger auf zugeordnete Daten, die für eine Benachrichtigung gelten. Der Parameter _lpvData_ zeigt nur dann auf gültige Daten, wenn die folgenden Flags festgelegt sind (_lpvData_ ist NULL, wenn _ulFlags_ auf andere Benachrichtigungstypen festgelegt ist): 
    
|**_ulFlags_ -Einstellung**|**_lpvData_ -Wert**|
|:-----|:-----|
|NOTIFY_CRITICAL_ERROR  <br/> |Informationen zu dem Fehler.  <br/> |
|NOTIFY_NEWMAIL_RECEIVED  <br/> |Eine **NEWMAIL_NOTIFICATION** -Struktur, die Informationen über die neu zugestellte Nachricht enthält.  <br/> |
|NOTIFY_SENTDEFERRED  <br/> |Eine **SBinary** -Struktur, die den Eintragsbezeichner der verzögerten Nachricht enthält.  <br/> |
   
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Benachrichtigung wurde erfolgreich ausgeführt.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISupport:: SpoolerNotify** -Methode wird für Nachrichtenspeicher-und Transportanbieter-Support Objekte implementiert. Diese Anbieter rufen **SpoolerNotify** auf, um den MAPI-Spooler über eine Änderung des Status oder eine Anforderung für Dienst zu informieren. **SpoolerNotify** wird in erster Linie von Transportanbietern aufgerufen und kann jederzeit während der Sitzung aufgerufen werden. 
  
## <a name="notes-to-transport-providers"></a>Hinweise für Transport Anbieter

Wenn Sie Ihre Transportanbieter Konfiguration geändert haben, rufen Sie **SpoolerNotify** auf, und legen Sie _ulFlags_ auf NOTIFY_CONFIG_CHANGED. **SpoolerNotify** antwortet durch Aufrufen der [IXPLogon:: AddressTypes](ixplogon-addresstypes.md) -Methode, um eine Änderung der unterstützten Adresstypen abzufragen. 
  
Wenn Sie einen kritischen Abschnitt benötigen, um eine ununterbrochene Verarbeitung sicherzustellen, rufen Sie **SpoolerNotify** mit _ulFlags_ auf NOTIFY_CRITSEC festgelegt. Wenn Sie dieses Flag festlegen, wird der MAPI-Spooler darüber informiert, dass die [IXPLogon:: idle](ixplogon-idle.md) -und [IXPLogon::P-oll](ixplogon-poll.md) -Methoden nicht aufgerufen werden sollen. Wenn ein kritischer Abschnitt geöffnet ist, geben Sie MAPI_E_BUSY immer dann zurück, wenn die [IMAPIStatus:: ValidateState](imapistatus-validatestate.md) -Methode aufgerufen wird. Wenn Sie den kritischen Abschnitt beendet haben, führen Sie einen weiteren Aufruf von **SpoolerNotify** aus, wobei _ulFlags_ auf NOTIFY_NONCRIT festgelegt ist. 
  
Wenn beispielsweise der Remote Transport-Anbieter Nachrichten hochgeladen hat, müssen Sie möglicherweise einem Benutzer die Eingabe einer Telefonnummer gestatten, um die Remoteverbindung herzustellen. Bevor Sie die Dialogfeldprozedur durchlaufen, sollten Sie einen kritischen Abschnitt deklarieren. Wenn der Benutzer das Dialogfeld schließt und die Dialogfeldprozedur beendet, sollten Sie den kritischen Abschnitt freigeben.
  
Wenn Sie _ulFlags_ auf NOTIFY_CRITICAL_ERROR festlegen, führt der MAPI-Spooler keine weiteren Aufrufe an den Anbieter aus, außer dass dieser freigegeben wird. Wenn Sie **SpoolerNotify** mit NOTIFY_CRITICAL_ERROR-Set aus der [IXPLogon:: StartMessage](ixplogon-startmessage.md) -oder [IXPLogon:: SubmitMessage](ixplogon-submitmessage.md) -Methode aufrufen, geben Sie mit einem entsprechenden Fehlerwert aus dem **StartMessage** oder * * SubmitMessage * * Call zurück. unmittelbar nach dem **SpoolerNotify** -Aufruf. 
  
Wenn der Transportanbieter von einer Bedingung wiederhergestellt wurde, die zuvor einen Fehler verursacht hat, rufen Sie **SpoolerNotify** mit _ulFlags_ auf NOTIFY_READYTOSEND festgelegt. Dieses Flag gibt an, dass der Anbieter wieder für die Verarbeitung von Nachrichten bereit ist. 
  
## <a name="notes-to-message-store-providers"></a>Hinweise für Nachrichtenspeicher Anbieter

Rufen Sie **SpoolerNotify**auf, und übergeben Sie das NOTIFY_READYTOSEND-Flag in _ulFlags_, bevor Sie den ersten aufruf an [IMAPISupport::P Reparesubmit](imapisupport-preparesubmit.md) in **IMessage:: SubmitMessage**durchführen. Dieser Aufruf von **SpoolerNotify** muss nur einmal pro Sitzung erfolgen. 
  
Wenn der Nachrichtenspeicher Anbieter eng mit einem Transportanbieter gekoppelt ist und Sie **SpoolerNotify** aufrufen, wobei _ulFlags_ auf NOTIFY_NEWMAIL_RECEIVED festgelegt ist, wird die neue Nachricht vom MAPI-Spooler geöffnet und mit der Verarbeitung der neuen Nachrichten Hookfunktion begonnen. Nach Abschluss der Verarbeitung ruft der MAPI-Spooler die [IMsgStore:: NotifyNewMail](imsgstore-notifynewmail.md) -Methode auf, um Sie über Ihre eigene neue Nachricht zu informieren. 
  
Weitere Informationen zum Aufrufen von **SpoolerNotify**finden Sie in den folgenden Themen:
  
- [Implementieren der FlushQueues-Methode](implementing-the-flushqueues-method.md)
    
- [Interaktion mit dem MAPI-Spooler](interacting-with-the-mapi-spooler.md)
    
- [Nachrichtenempfangs Modell](message-reception-model.md)
    
## <a name="see-also"></a>Siehe auch



[IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md)
  
[IXPLogon::StartMessage](ixplogon-startmessage.md)
  
[IXPLogon::SubmitMessage](ixplogon-submitmessage.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

