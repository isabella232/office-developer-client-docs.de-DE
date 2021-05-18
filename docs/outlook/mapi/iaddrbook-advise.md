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
  
Registriert einen Client oder Dienstanbieter, um Benachrichtigungen über Änderungen an einem oder mehreren Einträgen im Adressbuch zu erhalten.
  
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
  
> [in] Die Byteanzahl im Eintragsbezeichner, auf den der  _lpEntryID-Parameter_ verweist. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf die Eintrags-ID des Adressbuchcontainers, des Messagingbenutzers oder der Verteilerliste, der eine Benachrichtigung generiert, wenn eine Änderung des im  _ulEventMask-Parameter_ beschriebenen Typs oder Typs erfolgt. 
    
 _ulEventMask_
  
> [in] Mindestens ein Benachrichtigungsereignisse, das der Anrufer für den Empfang registriert. Jedes Ereignis ist einer bestimmten Benachrichtigungsstruktur zugeordnet, die Informationen zur aufgetretenen Änderung enthält. In der folgenden Tabelle sind die gültigen Werte für  _ulEventMask und_ deren entsprechende Strukturen aufgeführt. 
    
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
  
> [in] Ein Zeiger auf das objekt advise sink, das aufgerufen werden soll, wenn das Ereignis auftritt, für das eine Benachrichtigung angefordert wurde.
    
 _lpulConnection_
  
> [out] Ein Zeiger auf eine Verbindungsnummer ungleich Null, die die Benachrichtigungsregistrierung darstellt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Benachrichtigungsregistrierung war erfolgreich.
    
MAPI_E_INVALID_ENTRYID 
  
> Der Adressbuchanbieter, der für die in  _lpEntryID_ übergebene Eintrags-ID verantwortlich ist, konnte keine Benachrichtigung für den entsprechenden Eintrag registrieren. 
    
MAPI_E_NO_SUPPORT 
  
> Die Benachrichtigung wird vom Adressbuchanbieter nicht unterstützt, der für das objekt verantwortlich ist, das durch den eintragsbezeichner identifiziert wird, der im  _lpEntryID-Parameter übergeben_ wird. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Der in  _lpEntryID_ übergebene Eintragsbezeichner kann nicht von einem der Adressbuchanbieter im Profil verarbeitet werden. 
    
## <a name="remarks"></a>Hinweise

Clients und Dienstanbieter rufen die **Advise-Methode** auf, um sich für einen bestimmten Typ oder Benachrichtigungstyp für einen Adressbucheintrag zu registrieren. Die Benachrichtigungstypen werden durch die Ereignismaske angegeben, die mit dem  _ulEventMask-Parameter übergeben_ wird. 
  
MAPI gibt diesen **Advise-Aufruf** an den Adressbuchanbieter weiter, der für den Eintrag verantwortlich ist, wie durch den Eintragsbezeichner im  _lpEntryID-Parameter_ angegeben. Der Adressbuchanbieter übernimmt entweder die Registrierung selbst oder ruft die Supportmethode [IMAPISupport::Subscribe](imapisupport-subscribe.md)auf, um MAPI zur Registrierung des Anrufers auffordern. Eine Verbindungsnummer ungleich Null wird zurückgegeben, um die erfolgreiche Registrierung zu repräsentieren.
  
Wenn eine Änderung am Eintrag des durch die Benachrichtigungsregistrierung angegebenen Typs auftritt, ruft der Adressbuchanbieter die [IMAPIAdviseSink::OnNotify-Methode](imapiadvisesink-onnotify.md) für das im  _lpAdviseSink-Parameter_ angegebene Advise-Sink-Objekt auf. Die **OnNotify-Methode** enthält eine [NOTIFICATION-Struktur](notification.md) als Eingabeparameter, der Daten zur Beschreibung des Ereignisses enthält. 
  
Je nach Adressbuchanbieter kann der Aufruf von **OnNotify** unmittelbar nach der Änderung am registrierten Objekt oder zu einem späteren Zeitpunkt erfolgen. Auf Systemen, die mehrere Ausführungsthreads unterstützen, kann der Aufruf von **OnNotify** in jedem Thread erfolgen. Clients können anfordern, dass diese Benachrichtigungen in einem bestimmten Thread auftreten, indem sie die [HrThisThreadAdviseSink-Funktion](hrthisthreadadvisesink.md) aufrufen, um das an Advise übergebene Advise-Sink-Objekt **zu erstellen.** 
  
Da ein Adressbuchanbieter das von Clients übergebene Advise-Sink-Objekt jederzeit nach erfolgreichem Abschluss des **Aufrufs "Advise"** und vor einem [IAddrBook::Unadvise-Aufruf](iaddrbook-unadvise.md) zum Abbrechen der Benachrichtigung lossagen kann, sollten Clients ihre Ratgebersenkenobjekte los, wenn **Advise** zurückgibt. 
  
Weitere Informationen zum Benachrichtigungsprozess finden Sie unter [Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md).
  
## <a name="see-also"></a>Siehe auch



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IAddrBook::Unadvise](iaddrbook-unadvise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[Benachrichtigung](notification.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

