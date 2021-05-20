---
title: IABLogonAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.Advise
api_type:
- COM
ms.assetid: 375d65b1-607d-4e2a-8052-9bcbf08fc2ac
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 4ab0e4b023e6af19f650abf421aed122dcc21879
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428228"
---
# <a name="iablogonadvise"></a>IABLogon::Advise

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Registriert den Anrufer, um Benachrichtigungen über angegebene Ereignisse zu erhalten, die sich auf einen Container, einen Messagingbenutzer oder eine Verteilerliste auswirken.
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a>Parameter

 _cbEntryID_
  
> [in] Die Anzahl der Bytes in der Eintrags-ID, auf die der  _lpEntryID-Parameter_ verweist. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf den Eintragsbezeichner des Objekts, über das Benachrichtigungen generiert werden sollen.
    
 _ulEventMask_
  
> [in] Eine Bitmaske mit Werten, die die Arten von Benachrichtigungsereignissen angibt, die der Anrufer interessiert und in die Registrierung einbezogen werden sollte. Jedem Ereignistyp ist eine entsprechende [NOTIFICATION-Struktur](notification.md) zugeordnet, die Informationen zum Ereignis enthält. In der folgenden Tabelle sind die gültigen Werte für den  _ulEventMask-Parameter_ und die strukturen aufgeführt, die jedem Wert zugeordnet sind. 
    
|**Benachrichtigungsereignistyp**|**Entsprechende **BENACHRICHTIGUNGsstruktur****|
|:-----|:-----|
|**fnevCriticalError** <br/> |[ERROR_NOTIFICATION](error_notification.md) <br/> |
|**fnevObjectCreated** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectDeleted** <br/> |**OBJECT_NOTIFICATION** <br/> |
|**fnevObjectModified** <br/> |**OBJECT_NOTIFICATION** <br/> |
|**fnevObjectCopied** <br/> |**OBJECT_NOTIFICATION** <br/> |
|**fnevObjectMoved** <br/> |**OBJECT_NOTIFICATION** <br/> |
   
 _lpAdviseSink_
  
> [in] Ein Zeiger auf ein Advise Sink-Objekt, um die nachfolgenden Benachrichtigungen zu erhalten.
    
 _lpulConnection_
  
> [out] Ein Zeiger auf einen Wert ungleich Null, der die Benachrichtigungsregistrierung darstellt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Benachrichtigungsregistrierung war erfolgreich.
    
MAPI_E_INVALID_ENTRYID 
  
> Der im  _lpEntryID-Parameter_ übergebene Eintragsbezeichner hat nicht das entsprechende Format. 
    
MAPI_E_NO_SUPPORT 
  
> Der Adressbuchanbieter unterstützt keine Benachrichtigung, möglicherweise, weil er keine Änderungen an seinen Objekten zu lässt.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Der Adressbuchanbieter kann die in  _lpEntryID_ übergebene Eintrags-ID nicht verarbeiten.
    
## <a name="remarks"></a>Hinweise

Adressbuchanbieter implementieren die **IABLogon::Advise-Methode,** um den Anrufer zu registrieren, der benachrichtigt wird, wenn eine Änderung an einem Objekt in einem ihrer Container auftritt. Anrufer können sich für Benachrichtigungen zu Messagingbenutzern, Verteilerlisten oder ganzen Containern registrieren. 
  
Clients rufen in der Regel die [IAddrBook::Advise-Methode auf, um](iaddrbook-advise.md) sich für Adressbuchbenachrichtigungen zu registrieren. MAPI ruft dann die **Advise-Methode** des Adressbuchanbieters auf, der für das Objekt verantwortlich ist, das durch den Eintragsbezeichner in _lpEntryID dargestellt wird._
  
Wenn eine Änderung am angegebenen Objekt des typs auftritt, der in  _ulEventMask_ dargestellt wird, wird ein Aufruf der **OnNotify-Methode** der Ratensenke vorgenommen, auf die  _von lpAdviseSink_ verwiesen wird. Daten, die in der **NOTIFICATION-Struktur** an die **OnNotify-Routine** übergeben werden, beschreiben das Ereignis. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Sie können Benachrichtigungen mit oder ohne Hilfe von MAPI unterstützen. MAPI verfügt über drei Unterstützungsobjektmethoden, mit deren Hilfe Dienstanbieter Benachrichtigungen implementieren können:
  
- [IMAPISupport::Subscribe](imapisupport-subscribe.md)
    
- [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)
    
- [IMAPISupport::Notify](imapisupport-notify.md)
    
Wenn Sie die MAPI-Supportmethoden verwenden möchten, rufen Sie **Subscribe** auf, wenn Ihre **Advise-Methode** aufgerufen wird, und geben Sie den  _lpAdviseSink-Zeiger_ frei. 
  
Wenn Sie die Benachrichtigung selbst unterstützen möchten, rufen Sie die **AddRef-Methode** der Durchwahlsenke auf, die durch den  _lpAdviseSink-Parameter_ dargestellt wird, um eine Kopie dieses Zeigers zu behalten. Bewahren Sie diese Kopie auf, bis Ihre [IABLogon::Unadvise-Methode](iablogon-unadvise.md) aufgerufen wird, um die Registrierung abbricht. 
  
Weisen Sie unabhängig davon, wie Sie die Benachrichtigung unterstützen, der Benachrichtigungsregistrierung eine Verbindungsnummer ungleich Null zu, und geben Sie sie im  _lpulConnection-Parameter_ zurück. Geben Sie diese Verbindungsnummer erst frei, wenn die **Unadvise-Methode** aufgerufen wurde. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Der Hinweissenkenzeiger, den Sie im  _lpAdviseSink-Parameter_ **an Advise** übergeben, kann auf ein Objekt verweisen, das Sie erstellt haben oder das MAPI über die [HrThisThreadAdviseSink-Funktion](hrthisthreadadvisesink.md) erstellt hat. Möglicherweise sollten Sie **HrThisThreadAdviseSink** verwenden, wenn Sie mehrere Ausführungsthreads unterstützen und sicherstellen möchten, dass nachfolgende Aufrufe ihrer **OnNotify-Methode** zu einem geeigneten Zeitpunkt in einem geeigneten Thread erfolgen. 
  
Bereiten Sie sich darauf vor, dass Ihr Advise Sink-Objekt jederzeit nach Ihrem Aufruf von **Advise** und vor Ihrem Anruf bei **Unadvise** freigegeben wird. Daher sollten Sie Ihr Advise Sink-Objekt nach der Rückgabe von **Advise** frei geben, es sei denn, Sie haben eine bestimmte langfristige Verwendung dafür. 
  
Weitere Informationen zum Benachrichtigungsprozess finden Sie unter [Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md). Informationen zur Verwendung der **IMAPISupport-Methoden** zur Unterstützung von Benachrichtigungen finden Sie unter [Supporting Event Notification](supporting-event-notification.md). Weitere Informationen zu Multithreading und MAPI finden Sie unter [Threading in MAPI](threading-in-mapi.md).
  
## <a name="see-also"></a>Siehe auch



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IABLogon::Unadvise](iablogon-unadvise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[Benachrichtigung](notification.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

