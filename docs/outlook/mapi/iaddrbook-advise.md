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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 8214390af883432d72f608452b8b944417884fd2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791997"
---
# <a name="iaddrbookadvise"></a>IAddrBook::Advise

  
  
**Betrifft**: Outlook 
  
Registriert einen Client oder Dienstanbieter Erhalt von Benachrichtigungen zu Änderungen an einen oder mehrere Einträge im Adressbuch an.
  
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
  
> [in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LpEntryID_ verwiesen. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf die Eintrags-ID der Adressbuchcontainer messaging-Benutzer oder eine Verteilerliste, die eine Benachrichtigung generiert wird, bei einer Änderung des Typs oder Typen, die im Parameter _UlEventMask_ beschrieben wird. 
    
 _ulEventMask_
  
> [in] Eine oder mehrere Benachrichtigungsereignisse, die der Anrufer Empfang registriert wird. Jedes Ereignis ist eine bestimmte Benachrichtigung-Struktur, die Informationen zum Ändern der aufgetretenen enthält zugeordnet. Die folgende Tabelle enthält die gültigen Werte für _UlEventMask_ und ihre entsprechenden Strukturen. 
    
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
  
> [in] Ein Zeiger auf das Empfängerobjekt Advise aufgerufen werden, tritt das Ereignis für das Benachrichtigung angefordert wurde.
    
 _lpulConnection_
  
> [out] Ein Zeiger auf eine Verbindung ungleich NULL-Zahl, die benachrichtigungsregistrierung darstellt.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die benachrichtigungsregistrierung war erfolgreich.
    
MAPI_E_INVALID_ENTRYID 
  
> Verantwortlich für die Eintrags-ID _LpEntryID_ übergebenen Adressbuchanbieter konnte eine Benachrichtigung für den entsprechenden Eintrag nicht registriert werden. 
    
MAPI_E_NO_SUPPORT 
  
> Benachrichtigung wird von Adressbuchanbieter verantwortlich für das durch die Eintrags-ID in der _LpEntryID_ -Parameter übergebene Objekt nicht unterstützt. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Die Eintrags-ID _LpEntryID_ übergebenen kann von jedem der adressbuchanbietern implementierte im Profil behandelt werden. 
    
## <a name="remarks"></a>Bemerkungen

Clients und Dienstanbieter Aufrufen die **Advise** -Methode für einen bestimmten Typ oder Typen der Benachrichtigung auf ein Adressbuch Adresseintrag registriert. Die Typen der Benachrichtigung werden durch die mit der _UlEventMask_ -Parameter übergebene Ereignismaske angezeigt. 
  
MAPI leitet diese **Advise** -Anruf an die Adressbuchanbieter, die verantwortlich für den Eintrag wie die Eintrags-ID in der _LpEntryID_ -Parameter angegeben ist. Der Adressbuchanbieter behandelt die Registrierung selbst, oder ruft die Support-Methode, [IMAPISupport::Subscribe](imapisupport-subscribe.md), MAPI, um den Anrufer registrieren aufgefordert. Eine Zahl ungleich NULL Verbindung wird zurückgegeben, um die erfolgreiche Registrierung darzustellen.
  
Wenn eine Änderung an den Eintrag vom Typ angegeben durch die benachrichtigungsregistrierung auftritt, ruft der Adressbuchanbieter die [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) -Methode für der Advise-Empfängerobjekt im _LpAdviseSink_ -Parameter angegebene. Die **OnNotify** -Methode enthält eine [Benachrichtigung](notification.md) Struktur als Eingabeparameter, der Daten zur Beschreibung des Ereignisses enthält. 
  
Je nach der Adressbuchanbieter kann der Anruf an **OnNotify** unmittelbar nach der Änderung an das registrierte Objekt oder zu einem späteren Zeitpunkt auftreten. Auf Systemen, die mehreren Threads der Ausführung zu unterstützen, kann der Aufruf von **OnNotify** auf einem beliebigen Thread auftreten. Clients können anfordern, dass diese Benachrichtigungen erfolgen für einen bestimmten Thread durch Aufrufen der [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) -Funktion, um das Empfängerobjekt Advise erstellen, das an **Advise**übergeben wird. 
  
Da ein Adressbuchanbieter der Advise-Empfängerobjekt kann jederzeit nach der erfolgreiche Abschluss der **Advise** aufrufen und aufrufen, bevor eine [IAddrBook::Unadvise](iaddrbook-unadvise.md) die Benachrichtigung Abbrechen von Clients übergebenen freigeben kann, sollte Clients freigeben. Ihre Advise Empfängerobjekten, wenn **Advise** zurückgegeben. 
  
Weitere Informationen zu den Benachrichtigungsprozess finden Sie unter [Event Notification in MAPI](event-notification-in-mapi.md).
  
## <a name="see-also"></a>Siehe auch



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IAddrBook::Unadvise](iaddrbook-unadvise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[Benachrichtigung](notification.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

