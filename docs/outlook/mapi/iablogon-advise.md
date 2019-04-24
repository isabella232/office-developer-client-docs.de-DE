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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 4ab0e4b023e6af19f650abf421aed122dcc21879
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338577"
---
# <a name="iablogonadvise"></a>IABLogon::Advise

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Registriert den Anrufer so, dass er Benachrichtigungen über angegebene Ereignisse erhält, die sich auf einen Container, einen Messagingbenutzer oder eine Verteilerliste auswirken.
  
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
  
> in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEntryID_ -Parameter verwiesen wird. 
    
 _lpEntryID_
  
> in Ein Zeiger auf die Eintrags-ID des Objekts, über das Benachrichtigungen generiert werden sollen.
    
 _ulEventMask_
  
> in Eine Bitmaske von Werten, die die Typen von Benachrichtigungsereignissen angibt, an denen der Anrufer interessiert ist, und die in die Registrierung aufgenommen werden sollen. Jeder Art von Ereignis [](notification.md) , das Informationen über das Ereignis enthält, ist eine entsprechende Benachrichtigungsstruktur zugeordnet. In der folgenden Tabelle sind die gültigen Werte für den _ulEventMask_ -Parameter und die jedem Wert zugeordneten Strukturen aufgeführt. 
    
|**Benachrichtigungs Ereignistyp**|**Entsprechende **Benachrichtigungs** Struktur**|
|:-----|:-----|
|**fnevCriticalError** <br/> |[ERROR_NOTIFICATION](error_notification.md) <br/> |
|**fnevObjectCreated** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectDeleted** <br/> |**OBJECT_NOTIFICATION** <br/> |
|**fnevObjectModified** <br/> |**OBJECT_NOTIFICATION** <br/> |
|**fnevObjectCopied** <br/> |**OBJECT_NOTIFICATION** <br/> |
|**fnevObjectMoved** <br/> |**OBJECT_NOTIFICATION** <br/> |
   
 _lpAdviseSink_
  
> in Ein Zeiger auf ein Advise-Senke-Objekt, um die nachfolgenden Benachrichtigungen zu empfangen.
    
 _lpulConnection_
  
> Out Ein Zeiger auf einen Wert ungleich NULL, der die Benachrichtigungs Registrierung darstellt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Benachrichtigungs Registrierung war erfolgreich.
    
MAPI_E_INVALID_ENTRYID 
  
> Die im _lpEntryID_ -Parameter übergebene Eintrags-ID weist nicht das entsprechende Format auf. 
    
MAPI_E_NO_SUPPORT 
  
> Der Adressbuchanbieter unterstützt keine Benachrichtigung, da möglicherweise keine Änderungen an den Objekten vorgenommen werden können.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Der Adressbuchanbieter kann den in _lpEntryID_übergebenen Eintragsbezeichner nicht verarbeiten.
    
## <a name="remarks"></a>Bemerkungen

Adressbuchanbieter implementieren die **IABLogon:: Advise** -Methode, um den Anrufer zu registrieren, der benachrichtigt werden soll, wenn eine Änderung an einem Objekt in einem ihrer Container erfolgt. Anrufer können sich für Benachrichtigungen zu Messaging Benutzern, Verteilerlisten oder ganzen Containern registrieren. 
  
Clients rufen in der Regel die [IAddrBook:: Advise](iaddrbook-advise.md) -Methode auf, um Adressbuch Benachrichtigungen zu registrieren. Anschließend ruft MAPI die **Advise** -Methode des Adressbuch Anbieters auf, der für das durch den Eintragsbezeichner in _lpEntryID_dargestellte Objekt zuständig ist.
  
Wenn eine Änderung an dem angegebenen Objekt des in _ulEventMask_dargestellten Typs erfolgt, wird ein Aufruf an die OnNotify-Methode der Advise-Senke durch _lpAdviseSink_verwiesen. **** Die Daten, die **** in der Benachrichtigungsstruktur an die OnNotify-Routine übergeben werden, beschreiben das Ereignis. **** 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Sie können Benachrichtigungen mit oder ohne Hilfe von MAPI unterstützen. MAPI verfügt über drei Support Objektmethoden, mit denen Dienstanbieter Benachrichtigungen implementieren können:
  
- [IMAPISupport::Subscribe](imapisupport-subscribe.md)
    
- [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)
    
- [IMAPISupport::Notify](imapisupport-notify.md)
    
Wenn Sie die MAPI-Supportmethoden verwenden möchten, rufen Sie **subscribe** auf, wenn Ihre **Advise** -Methode aufgerufen wird, und geben Sie den _lpAdviseSink_ -Zeiger frei. 
  
Wenn Sie sich für die Unterstützung der Benachrichtigung entscheiden, rufen Sie die **AddRef** -Methode der durch den _lpAdviseSink_ -Parameter dargestellten Advise-Senke auf, um eine Kopie dieses Zeigers aufzubewahren. Bewahren Sie diese Kopie auf, bis die [IABLogon:: Unadvise](iablogon-unadvise.md) -Methode aufgerufen wird, um die Registrierung abzubrechen. 
  
Unabhängig davon, wie Sie die Benachrichtigung unterstützen, weisen Sie der Benachrichtigungs Registrierung eine unGleich NULL-Verbindung zu und geben Sie im _lpulConnection_ -Parameter zurück. Geben Sie diese Verbindungsnummer erst frei, **** wenn die Unadvise-Methode aufgerufen wurde. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Der Advise-Senke-Zeiger, den Sie im _lpAdviseSink_ -Parameter an **Advise** übergeben, kann auf ein Objekt verweisen, das Sie erstellt haben oder die MAPI über die [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) -Funktion erstellt hat. Möglicherweise möchten Sie **HrThisThreadAdviseSink** verwenden, wenn Sie mehrere Threads der Ausführung unterstützen und sicher sein möchten, dass nachfolgende **** Aufrufe an Ihre OnNotify-Methode zu einem geeigneten Zeitpunkt in einem entsprechenden Thread stattfinden. 
  
Bereiten Sie sich darauf vor, dass Ihr Advise-Senke-Objekt jederzeit nach dem Anruf zur **Beratung** und vor dem Aufruf von Unadvise freigegeben werden kann. **** Daher sollten Sie Ihr Advise-Senke-Objekt nach der Rückgabe von **Advise** freigeben, es sei denn, Sie haben eine bestimmte langfristige Verwendung dafür. 
  
Weitere Informationen zum Benachrichtigungsprozess finden Sie unter [Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md). Informationen zur Verwendung der **IMAPISupport** -Methoden zur Unterstützung von Benachrichtigungen finden Sie unter [unterstützende Ereignisbenachrichtigung](supporting-event-notification.md). Weitere Informationen zu Multithreading und MAPI finden Sie unter [Threading in MAPI](threading-in-mapi.md).
  
## <a name="see-also"></a>Siehe auch



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IABLogon::Unadvise](iablogon-unadvise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[Benachrichtigung](notification.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

