---
title: IAddrBookAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.Advise
api_type:
- COM
ms.assetid: 2def89ed-e4ce-446a-8b80-132d11ae8f8b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7abafafd3d4bd9618d85a7dac34e4556545167bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406276"
---
# <a name="iaddrbookadvise"></a>IAddrBook::Advise

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Registriert einen Client oder Dienstanbieter für den Empfang von Benachrichtigungen zu Änderungen an einem oder mehreren Einträgen im Adressbuch.
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG_PTR lpulConnection
);
```

## <a name="parameters"></a>Parameter

 _cbEntryID_
  
> in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEntryID_ -Parameter verwiesen wird. 
    
 _lpEntryID_
  
> in Ein Zeiger auf die Eintrags-ID des Adressbuch Containers, des Messaging Benutzers oder der Verteilerliste, der eine Benachrichtigung generiert, wenn eine Änderung der im _ulEventMask_ -Parameter beschriebenen Typen auftritt. 
    
 _ulEventMask_
  
> in Ein oder mehrere Benachrichtigungsereignisse, die der Anrufer für den Empfang registriert. Jedes Ereignis ist einer bestimmten Benachrichtigungsstruktur zugeordnet, die Informationen zu der eingetretenen Änderung enthält. In der folgenden Tabelle sind die gültigen Werte für _ulEventMask_ und die entsprechenden Strukturen aufgeführt. 
    
|**Benachrichtigungsereignis**|**Entsprechende Struktur**|
|:-----|:-----|
|**fnevCriticalError** <br/> |[ERROR_NOTIFICATION](error_notification.md) <br/> |
|**fnevObjectCreated** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectDeleted** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectModified** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectCopied** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectMoved** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevTableModified** <br/> |[TABLE_NOTIFICATION](table_notification.md) <br/> |
   
 _lpAdviseSink_
  
> in Ein Zeiger auf das Advise-Senke-Objekt, das aufgerufen werden soll, wenn das Ereignis, für das die Benachrichtigung angefordert wurde, auftritt.
    
 _lpulConnection_
  
> Out Ein Zeiger auf eine Verbindungsnummer ungleich NULL, die die Benachrichtigungs Registrierung darstellt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Benachrichtigungs Registrierung war erfolgreich.
    
MAPI_E_INVALID_ENTRYID 
  
> Der Adressbuchanbieter, der für die in _lpEntryID_ übergebene Eintrags-ID zuständig ist, konnte keine Benachrichtigung für den entsprechenden Eintrag registrieren. 
    
MAPI_E_NO_SUPPORT 
  
> Die Benachrichtigung wird nicht vom Adressbuchanbieter unterstützt, der für das durch den _lpEntryID_ -Parameter übergebene Eintragsbezeichner verantwortlich ist. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Die in _lpEntryID_ übergebene Eintrags-ID kann von keinem der Adressbuchanbieter im Profil verarbeitet werden. 
    
## <a name="remarks"></a>Bemerkungen

Clients und Dienstanbieter rufen die **Advise** -Methode auf, um für einen bestimmten Typ oder eine Art von Benachrichtigung für einen Adressbucheintrag zu registrieren. Die Benachrichtigungstypen werden durch die Ereignismaske angezeigt, die mit dem _ulEventMask_ -Parameter übergeben wird. 
  
MAPI leitet diesen **Advise** -Aufruf an den Adressbuchanbieter weiter, der für den Eintrag verantwortlich ist, wie durch die Eintrags-ID im _lpEntryID_ -Parameter angegeben. Der Adressbuchanbieter behandelt die Registrierung selbst oder ruft die Support Methode [IMAPISupport:: subscribe](imapisupport-subscribe.md)auf, um MAPI zur Registrierung des Anrufers aufzufordern. Eine Verbindungsnummer, die ungleich NULL ist, wird zurückgegeben, um die erfolgreiche Registrierung darzustellen.
  
Bei jeder Änderung des Eintrags des Typs, der durch die Benachrichtigungs Registrierung angegeben wird, ruft der Adressbuchanbieter die [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) -Methode für das Advise-Senke-Objekt auf, das im _lpAdviseSink_ -Parameter angegeben ist. Die **OnNotify** -Methode enthält [](notification.md) eine Benachrichtigungsstruktur als Eingabeparameter, der Daten zum Beschreiben des Ereignisses enthält. 
  
Je nach Adressbuchanbieter kann der Aufruf von onNotify **** unmittelbar nach der Änderung des registrierten Objekts oder zu einem späteren Zeitpunkt erfolgen. Auf Systemen, die mehrere Threads der Ausführung unterstützen, kann **** der Aufruf von OnNotify in jedem Thread auftreten. Clients können diese Benachrichtigungen für einen bestimmten Thread anfordern, indem Sie die [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) -Funktion zum Erstellen des Advise-Senke-Objekts aufrufen, das an **Advise**übergeben wird. 
  
Da ein Adressbuchanbieter das Advise-Senke-Objekt, das von Clients übergeben wird, jederzeit freigeben kann, nachdem der **Advise** -Aufruf erfolgreich abgeschlossen wurde, und bevor ein [IAddrBook:: Unadvise](iaddrbook-unadvise.md) -Aufruf zum Abbrechen der Benachrichtigung ausgeführt wird, sollten Clients die Freigabe Ihre Advise-Senke-Objekte, wenn **Advise** zurückgegeben wird. 
  
Weitere Informationen zum Benachrichtigungsprozess finden Sie unter [Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md).
  
## <a name="see-also"></a>Siehe auch



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IAddrBook::Unadvise](iaddrbook-unadvise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[Benachrichtigung](notification.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

