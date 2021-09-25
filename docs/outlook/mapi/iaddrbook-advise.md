---
title: IAddrBookAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IAddrBook.Advise
api_type:
- COM
ms.assetid: 2def89ed-e4ce-446a-8b80-132d11ae8f8b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 83eeb0069e6f75f117a0abcfcbd841d1c1cd8e77
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576149"
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
  
> [in] Ein Zeiger auf den Eintragsbezeichner des Adressbuchcontainers, des Messagingbenutzers oder der Verteilerliste, der eine Benachrichtigung generiert, wenn eine Änderung des typs oder der Typen erfolgt, die im  _ulEventMask-Parameter_ beschrieben sind. 
    
 _ulEventMask_
  
> [in] Ein oder mehrere Benachrichtigungsereignisse, die der Aufrufer für den Empfang registriert. Jedes Ereignis ist einer bestimmten Benachrichtigungsstruktur zugeordnet, die Informationen über die aufgetretene Änderung enthält. In der folgenden Tabelle sind die gültigen Werte für  _ulEventMask_ und die entsprechenden Strukturen aufgeführt. 
    
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
  
> [in] Ein Zeiger auf das Rate-Senkenobjekt, das aufgerufen werden soll, wenn das Ereignis eintritt, für das eine Benachrichtigung angefordert wurde.
    
 _lpulConnection_
  
> [out] Ein Zeiger auf eine Nicht-Null-Verbindungsnummer, die die Benachrichtigungsregistrierung darstellt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Benachrichtigungsregistrierung war erfolgreich.
    
MAPI_E_INVALID_ENTRYID 
  
> Der Adressbuchanbieter, der für den in  _lpEntryID übergebenen_ Eintragsbezeichner verantwortlich ist, konnte keine Benachrichtigung für den entsprechenden Eintrag registrieren. 
    
MAPI_E_NO_SUPPORT 
  
> Die Benachrichtigung wird von dem Adressbuchanbieter nicht unterstützt, der für das Objekt verantwortlich ist, das durch den Im  _lpEntryID-Parameter übergebenen_ Eintragsbezeichner identifiziert wird. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Der in  _lpEntryID_ übergebene Eintragsbezeichner kann von keinem der Adressbuchanbieter im Profil verarbeitet werden. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Clients und Dienstanbieter rufen die **Advise-Methode** auf, um sich für einen bestimmten Benachrichtigungstyp oder eine bestimmte Art von Benachrichtigung für einen Adressbucheintrag zu registrieren. Die Arten von Benachrichtigungen werden durch die Ereignismaske angegeben, die mit dem  _ulEventMask-Parameter_ übergeben wird. 
  
MAPI leitet diesen **Advise-Aufruf** an den Adressbuchanbieter weiter, der für den Eintrag verantwortlich ist, wie durch den Eintragsbezeichner im  _lpEntryID-Parameter_ angegeben. Der Adressbuchanbieter verarbeitet entweder die Registrierung selbst oder ruft die Supportmethode [IMAPISupport::Subscribe](imapisupport-subscribe.md)auf, um die MAPI aufzufordern, den Aufrufer zu registrieren. Eine Nicht-Null-Verbindungsnummer wird zurückgegeben, um die erfolgreiche Registrierung darzustellen.
  
Wenn eine Änderung am Eintrag des Typs erfolgt, der durch die Benachrichtigungsregistrierung angegeben wird, ruft der Adressbuchanbieter die [IMAPIAdviseSink::OnNotify-Methode](imapiadvisesink-onnotify.md) für das im  _lpAdviseSink-Parameter_ angegebene Empfehlungssenkenobjekt auf. Die **OnNotify-Methode** enthält eine [NOTIFICATION-Struktur](notification.md) als Eingabeparameter, der Daten zur Beschreibung des Ereignisses enthält. 
  
Je nach Adressbuchanbieter kann der Aufruf von **OnNotify** unmittelbar nach der Änderung des registrierten Objekts oder zu einem späteren Zeitpunkt erfolgen. Auf Systemen, die mehrere Ausführungsthreads unterstützen, kann der Aufruf von **OnNotify** in jedem Thread erfolgen. Clients können anfordern, dass diese Benachrichtigungen in einem bestimmten Thread auftreten, indem sie die [HrThisThreadAdviseSink-Funktion](hrthisthreadadvisesink.md) aufrufen, um das Advise-Senkenobjekt zu erstellen, das an **Advise** übergeben wird. 
  
Da ein Adressbuchanbieter das von Clients übergebene Empfehlungssenkenobjekt jederzeit nach erfolgreichem Abschluss des **Advise-Aufrufs** und vor einem [IAddrBook::Unadvise-Aufruf](iaddrbook-unadvise.md) freigeben kann, um die Benachrichtigung abzubrechen, sollten Clients ihre Advise-Senkenobjekte freigeben, wenn **Advise** zurückgegeben wird. 
  
Weitere Informationen zum Benachrichtigungsprozess finden Sie unter [Ereignisbenachrichtigung in MAPI.](event-notification-in-mapi.md)
  
## <a name="see-also"></a>Siehe auch



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IAddrBook::Unadvise](iaddrbook-unadvise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[Benachrichtigung](notification.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

