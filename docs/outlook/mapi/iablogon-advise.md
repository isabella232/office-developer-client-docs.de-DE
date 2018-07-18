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
ms.openlocfilehash: 926fef0e1b2f905d510102e69afb667414e6cce3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791978"
---
# <a name="iablogonadvise"></a>IABLogon::Advise

  
  
**Betrifft**: Outlook 
  
Den Anrufer, um die Benachrichtigung der angegebenen Ereignisse, die einen Container, messaging-Benutzer oder Verteilerliste betreffen registriert.
  
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
  
> [in] Die Anzahl von Bytes in die Eintrags-ID auf den durch den Parameter _LpEntryID_ verwiesen. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf die Eintrags-ID des Objekts darüber, welche Benachrichtigungen generiert werden soll.
    
 _ulEventMask_
  
> [in] Eine Bitmaske der Werte, die die Typen von Benachrichtigungsereignisse anzugeben, die dem Anrufer ist daran interessiert, und die Registrierung einbezogen werden soll. Es wird eine entsprechende [Benachrichtigung](notification.md) Struktur jede Art von Ereignis, das Informationen über das Ereignis enthält zugeordnet. Die folgende Tabelle enthält die gültigen Werte für den Parameter _UlEventMask_ und die Strukturen jeden Wert zugeordnet. 
    
|**Benachrichtigungstyp-Ereignis**|**Entsprechende **Benachrichtigung** -Struktur**|
|:-----|:-----|
|**fnevCriticalError** <br/> |[ERROR_NOTIFICATION](error_notification.md) <br/> |
|**fnevObjectCreated** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectDeleted** <br/> |**OBJECT_NOTIFICATION** <br/> |
|**fnevObjectModified** <br/> |**OBJECT_NOTIFICATION** <br/> |
|**fnevObjectCopied** <br/> |**OBJECT_NOTIFICATION** <br/> |
|**fnevObjectMoved** <br/> |**OBJECT_NOTIFICATION** <br/> |
   
 _lpAdviseSink_
  
> [in] Ein Zeiger auf eine Advise-Empfängerobjekt nachfolgenden Benachrichtigungen zu empfangen.
    
 _lpulConnection_
  
> [out] Ein Zeiger auf einen Wert ungleich NULL, der die benachrichtigungsregistrierung darstellt.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die benachrichtigungsregistrierung war erfolgreich.
    
MAPI_E_INVALID_ENTRYID 
  
> Die Eintrags-ID in der _LpEntryID_ -Parameter übergeben, ist nicht im entsprechenden Format. 
    
MAPI_E_NO_SUPPORT 
  
> Der Adressbuchanbieter unterstützt Benachrichtigung, möglicherweise nicht, da keine Änderungen auf Objekte getroffen werden können.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Der Adressbuchanbieter kann nicht die Eintrags-ID _LpEntryID_übergebenen behandeln.
    
## <a name="remarks"></a>Bemerkungen

Von adressbuchanbietern implementierte implementieren Sie die **IABLogon::Advise** -Methode zum Registrieren des Aufrufers benachrichtigt werden, wenn ein Objekt in einem der deren Container, geändert. Anrufer können für Benachrichtigungen bezüglich messaging-Benutzern, Verteilerlisten oder gesamte Container registrieren. 
  
Clients aufrufen in der Regel die [IAddrBook::Advise](iaddrbook-advise.md) -Methode für Address Book Benachrichtigungen registriert. MAPI ruft dann die **Advise** -Methode des Adressbuchanbieter an, der für das Objekt, dargestellt durch die Eintrags-ID in _LpEntryID_zuständig ist.
  
Tritt eine Änderung auf das angegebene Objekt vom Typ in _UlEventMask_dargestellt, ist die **OnNotify** -Methode der Advise-Empfänger, die auf den _LpAdviseSink_aufgerufen. Daten, die in der **Benachrichtigung** Struktur der **OnNotify** Routine übergeben wird das Ereignis beschrieben. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Sie können die Benachrichtigung mit oder ohne Hilfe von MAPI unterstützen. MAPI hat drei Support-Objektmethoden zu Dienstanbietern Benachrichtigung zu implementieren:
  
- [IMAPISupport::Subscribe](imapisupport-subscribe.md)
    
- [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)
    
- [IMAPISupport::Notify](imapisupport-notify.md)
    
Wenn Sie sich entscheiden, die MAPI-Support-Methoden verwenden, rufen Sie **Abonnieren** die **Advise** -Methode aufgerufen wird, und heben Sie den Zeiger _LpAdviseSink_ . 
  
Wenn Sie sich entscheiden, die Benachrichtigung zu unterstützen, rufen Sie die **AddRef** -Methode der Advise-Empfänger, die durch den Parameter _LpAdviseSink_ dargestellt, um eine Kopie dieses Zeigers beizubehalten. Verwalten Sie diese Kopie, bis die [IABLogon::Unadvise](iablogon-unadvise.md) -Methode aufgerufen wird, um die Registrierung abzubrechen. 
  
Unabhängig davon, wie Sie Benachrichtigung zu unterstützen weisen Sie eine Zahl ungleich NULL Verbindung die benachrichtigungsregistrierung, und im Parameter _LpulConnection_ zurückzugeben. Freigegeben Sie diese Verbindungsnummer nicht, bis die **Unadvise** -Methode aufgerufen wurde. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Der Advise Empfängerzeiger, den im Parameter _LpAdviseSink_ **Advise** übergebene kann auf ein Objekt verweisen, die Sie erstellt haben oder die MAPI über die Funktion [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) erstellt wurde. Sie möchten möglicherweise **HrThisThreadAdviseSink** zu verwenden, wenn Sie die Unterstützung von mehreren Threads der Ausführung und möchten, um sicherzustellen, dass, die nachfolgende Aufrufe an die **OnNotify** -Methode zu einem geeigneten Zeitpunkt in einem entsprechenden Thread auftreten. 
  
Bereiten Sie für Ihre Advise-Empfängerobjekt jederzeit nach Ihren Anruf von der **Advise** und vor den Anruf auf **Unadvise**freigegeben werden muss. Aus diesem Grund sollten Sie Ihre Advise-Empfängerobjekt freigeben nach **Advise** zurückgegeben wird, es sei denn, Sie eine bestimmte langfristige Verwendung dafür haben. 
  
Weitere Informationen zu den Benachrichtigungsprozess finden Sie unter [Event Notification in MAPI](event-notification-in-mapi.md). Informationen dazu, wie Sie die **IMAPISupport** -Methoden verwenden, um die Benachrichtigung zu unterstützen finden Sie unter [Event Notification unterstützen](supporting-event-notification.md). Weitere Informationen zu multithreading und MAPI, [Threading in MAPI](threading-in-mapi.md)finden Sie unter.
  
## <a name="see-also"></a>Siehe auch



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IABLogon::Unadvise](iablogon-unadvise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[Benachrichtigung](notification.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

