---
title: IABLogonAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IABLogon.Advise
api_type:
- COM
ms.assetid: 375d65b1-607d-4e2a-8052-9bcbf08fc2ac
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6fefb231feced4112da36a2bf20e054c801f8cdc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580048"
---
# <a name="iablogonadvise"></a>IABLogon::Advise

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Registriert den Aufrufer, um Benachrichtigungen über angegebene Ereignisse zu erhalten, die sich auf einen Container, einen Messagingbenutzer oder eine Verteilerliste auswirken.
  
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
  
> [in] Die Anzahl der Bytes im Eintragsbezeichner, auf den der  _lpEntryID-Parameter_ verweist. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf den Eintragsbezeichner des Objekts, über das Benachrichtigungen generiert werden sollen.
    
 _ulEventMask_
  
> [in] Eine Bitmaske mit Werten, die die Typen von Benachrichtigungsereignissen angibt, an denen der Aufrufer interessiert ist, und die in die Registrierung einbezogen werden sollte. Jedem Ereignistyp ist eine entsprechende [NOTIFICATION-Struktur](notification.md) zugeordnet, die Informationen über das Ereignis enthält. In der folgenden Tabelle sind die gültigen Werte für den  _ulEventMask-Parameter_ und die den einzelnen Werten zugeordneten Strukturen aufgeführt. 
    
|**Benachrichtigungsereignistyp**|**Entsprechende **BENACHRICHTIGUNGsstruktur****|
|:-----|:-----|
|**fnevCriticalError** <br/> |[ERROR_NOTIFICATION](error_notification.md) <br/> |
|**fnevObjectCreated** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectDeleted** <br/> |**OBJECT_NOTIFICATION** <br/> |
|**fnevObjectModified** <br/> |**OBJECT_NOTIFICATION** <br/> |
|**fnevObjectCopied** <br/> |**OBJECT_NOTIFICATION** <br/> |
|**fnevObjectMoved** <br/> |**OBJECT_NOTIFICATION** <br/> |
   
 _lpAdviseSink_
  
> [in] Ein Zeiger auf ein Empfehlungs-Senkenobjekt, um die nachfolgenden Benachrichtigungen zu erhalten.
    
 _lpulConnection_
  
> [out] Ein Zeiger auf einen Wert ungleich Null, der die Benachrichtigungsregistrierung darstellt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Benachrichtigungsregistrierung war erfolgreich.
    
MAPI_E_INVALID_ENTRYID 
  
> Der im  _lpEntryID-Parameter_ übergebene Eintragsbezeichner weist nicht das entsprechende Format auf. 
    
MAPI_E_NO_SUPPORT 
  
> Der Adressbuchanbieter unterstützt keine Benachrichtigung, möglicherweise weil er keine Änderungen an seinen Objekten zulässt.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Der Adressbuchanbieter kann den in  _lpEntryID übergebenen_ Eintragsbezeichner nicht verarbeiten.
    
## <a name="remarks"></a>HinwBemerkungeneise

Adressbuchanbieter implementieren die **IABLogon::Advise-Methode,** um den Aufrufer zu registrieren, der benachrichtigt wird, wenn eine Änderung an einem Objekt in einem seiner Container erfolgt. Anrufer können sich für Benachrichtigungen über Messagingbenutzer, Verteilerlisten oder ganze Container registrieren. 
  
Clients rufen in der Regel die [IAddrBook::Advise-Methode](iaddrbook-advise.md) auf, um sich für Adressbuchbenachrichtigungen zu registrieren. MAPI ruft dann die **Advise-Methode** des Adressbuchanbieters auf, der für das Objekt verantwortlich ist, das durch den Eintragsbezeichner in  _lpEntryID_ dargestellt wird.
  
Wenn eine Änderung am angegebenen Objekt des Typs erfolgt, der in  _ulEventMask_ dargestellt wird, wird die **OnNotify-Methode** der Empfehlungssenke aufgerufen, auf die von  _lpAdviseSink_ verwiesen wird. Daten, die in der **NOTIFICATION-Struktur** an die **OnNotify-Routine** übergeben werden, beschreiben das Ereignis. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Sie können Benachrichtigungen mit oder ohne Hilfe von MAPI unterstützen. MAPI verfügt über drei Unterstützungsobjektmethoden, die Dienstanbietern beim Implementieren von Benachrichtigungen helfen:
  
- [IMAPISupport::Subscribe](imapisupport-subscribe.md)
    
- [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)
    
- [IMAPISupport::Notify](imapisupport-notify.md)
    
Wenn Sie die MAPI-Unterstützungsmethoden verwenden möchten, rufen **Sie Subscribe** auf, wenn Ihre **Advise-Methode** aufgerufen wird, und geben Sie den  _lpAdviseSink-Zeiger_ frei. 
  
Wenn Sie sich entscheiden, die Benachrichtigung selbst zu unterstützen, rufen Sie die **AddRef-Methode** der Empfehlungssenke auf, die durch den  _lpAdviseSink-Parameter_ dargestellt wird, um eine Kopie dieses Zeigers beizubehalten. Verwalten Sie diese Kopie, bis Ihre [IABLogon::Unadvise-Methode](iablogon-unadvise.md) aufgerufen wird, um die Registrierung abzubrechen. 
  
Unabhängig davon, wie Sie die Benachrichtigung unterstützen, weisen Sie der Benachrichtigungsregistrierung eine Nonzero-Verbindungsnummer zu und geben Sie sie im  _lpulConnection-Parameter_ zurück. Geben Sie diese Verbindungsnummer erst frei, nachdem die **Unadvise-Methode** aufgerufen wurde. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Der Empfehlungssenkenzeiger, den Sie an den  _Parameter lpAdviseSink_ an **Advise** übergeben, kann auf ein Objekt verweisen, das Sie erstellt haben oder das mapi über die [HrThisThreadAdviseSink-Funktion](hrthisthreadadvisesink.md) erstellt hat. Möglicherweise möchten Sie **HrThisThreadAdviseSink** verwenden, wenn Sie mehrere Ausführungsthreads unterstützen und sicherstellen möchten, dass nachfolgende Aufrufe der **OnNotify-Methode** zu einem geeigneten Zeitpunkt in einem entsprechenden Thread erfolgen. 
  
Bereiten Sie sich darauf vor, dass Ihr Empfehlungssenkenobjekt jederzeit nach Ihrem Aufruf an **"Advise"** und vor dem Aufruf von **"Unadvise"** freigegeben wird. Daher sollten Sie ihr Empfehlungssenkenobjekt freigeben, nachdem **Advise** zurückgegeben wurde, es sei denn, Sie haben eine bestimmte langfristige Verwendung dafür. 
  
Weitere Informationen zum Benachrichtigungsprozess finden Sie unter [Ereignisbenachrichtigung in MAPI.](event-notification-in-mapi.md) Informationen zur Verwendung der **IMAPISupport-Methoden** zur Unterstützung von Benachrichtigungen finden Sie unter ["Unterstützende Ereignisbenachrichtigung".](supporting-event-notification.md) Weitere Informationen zu Multithreading und MAPI finden Sie unter [Threading in MAPI.](threading-in-mapi.md)
  
## <a name="see-also"></a>Siehe auch



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IABLogon::Unadvise](iablogon-unadvise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[Benachrichtigung](notification.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

