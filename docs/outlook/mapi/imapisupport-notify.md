---
title: IMAPISupportNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.Notify
api_type:
- COM
ms.assetid: c16c668e-2c8b-4759-bbca-d0c5662b62e9
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: db23d1801bf32fd947a77dfd887c56f75ded5681
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792388"
---
# <a name="imapisupportnotify"></a>IMAPISupport::Notify

**Betrifft**: Outlook 
  
Sendet eine Benachrichtigung über ein bestimmtes Ereignis mit einer Advise-Datenquelle, die ursprünglich für die Benachrichtigung über die [IMAPISupport::Subscribe](imapisupport-subscribe.md) -Methode registriert. 
  
```cpp
HRESULT Notify(
LPNOTIFKEY lpKey,
ULONG cNotification,
LPNOTIFICATION lpNotifications,
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parameter

_lpKey_
  
> [in] Ein Zeiger auf die Benachrichtigung Schlüssel für das Quellobjekt Advise. Der Parameter _LpKey_ darf nicht NULL sein. 
    
_cNotification_
  
> [in] Die Anzahl der Benachrichtigung Strukturen auf den durch den Parameter _LpNotifications_ verwiesen. 
    
_lpNotifications_
  
> [in] Ein Zeiger auf ein Array von [Benachrichtigung](notification.md) Strukturen, die ausstehende Benachrichtigungen zu beschreiben. 
    
_lpulFlags_
  
> [in, out] Eine Bitmaske aus Flags, die den Benachrichtigungsprozess steuert. Bei der Eingabe kann das folgende Flag festgelegt werden:
    
  - PARAMETER MAPI_UNICODE 
    
    > Die Zeichenfolgen in der Benachrichtigung Strukturen auf den _LpNotifications_ sind im Unicode-Format. Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format. 

    Bei der Ausgabe kann MAPI das folgende Flag festlegen:
        
  - NOTIFY_CANCELED 
    
    > Eine Rückruffunktion abgebrochen eine synchrone Benachrichtigung.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Benachrichtigungen wurden erfolgreich generiert.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISupport::Notify** -Methode wird für alle dienstanbieterobjekten Unterstützung implementiert. Dienstanbieter anrufen **Benachrichtigen** , um anzufordern, dass MAPI generieren eine Benachrichtigung für eine Advise-Empfänger, die für die Benachrichtigung über die **IMAPISupport::Subscribe** -Methode zuvor registriert hat. 
  
**Benachrichtigen** Kopien die Strukturen durch den Parameter _LpNotifications_ auf das in den Speicher und die entsprechenden Advise-Empfänger [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) -Methode aufgerufen. Wenn mit der Benachrichtigung **OnNotify** abgeschlossen ist, wird den Beteiligten Speicher freigegeben. Der Aufrufer muss nicht Speicher zugewiesen werden. MAPI führt alle erforderlichen arbeitsspeicherreservierung. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Die Benachrichtigung-Taste im _LpKey_ -Parameter übergeben müssen Sie zum Schlüssel _LpKey_ an die **IMAPISupport::Subscribe** -Methode übergebenen identisch sein. Viele Anbieter für die Eintrags-ID der Advise-Quelle als Schlüssel verwenden, aber andere Daten enthält, wie ein Dateipfad verwendet werden können. MAPI verwendet diesen Schlüssel, um alle Registrierungen für Benachrichtigungen für die identifizierten Advise-Quelle zu suchen. 
  
Stellen Sie sicher, dass Sie das **LpEntryID** Mitglied der Benachrichtigungsstruktur auf langfristige Eintrags-ID festgelegt. 
  
Wenn Sie festlegen, rufen Sie das NOTIFY_SYNC-Flag auf die **Subscribe** für eines der ausstehenden Benachrichtigungen, **Benachrichtigen** Anrufe Rückruffunktionen **IMAPIAdviseSink::OnNotify** -Methode vor der Rückgabe. Advise-Empfänger kann manuell oder durch Aufrufen von [HrAllocAdviseSink](hrallocadvisesink.md)erstellt werden. Die Funktion **HrAllocAdviseSink** ermöglicht dessen Aufrufer einer Callback-Funktion als Teil der Benachrichtigung, **Notify** -Aufrufe angeben. Die Callback-Funktion entspricht der [NOTIFCALLBACK](notifcallback.md) Prototyp. Rückruffunktionen immer durch Clients implementiert geben S_OK zurück. Implementierung von Dienstanbietern Rückruffunktionen können CALLBACK_DISCONTINUE zurück. 
  
Wenn eine Rückruffunktion CALLBACK_DISCONTINUE zurückgibt, MAPI beendet Senden von Benachrichtigungen und NOTIFY_CANCELED in _LpulFlags_ -Parameter die **Notify** -Methode zurückgegeben. Sie können davon ausgehen, dass der Prozess inaktiv und Generieren von Benachrichtigungen für diesen Prozess beenden ist. Wenn **Benachrichtigen** in _LpulFlags_gibt 0 zurück, der Prozess noch aktiv ist, und Sie sollten weiterhin zum Senden von Benachrichtigungen, nach Bedarf.
  
Wenn Sie synchrone Benachrichtigungen verwenden, sollten Sie darauf achten Sie, Deadlocks zu vermeiden.
  
Weitere Informationen zu den Benachrichtigungsprozess finden Sie unter [Event Notification in MAPI](event-notification-in-mapi.md). 
  
## <a name="see-also"></a>Siehe auch

- [IMAPISupport::Subscribe](imapisupport-subscribe.md)  
- [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)  
- [NOTIFCALLBACK](notifcallback.md) 
- [Benachrichtigung](notification.md)  
- [NOTIFKEY](notifkey.md)  
- [PidTagRecordKey (kanonische Eigenschaft)](pidtagrecordkey-canonical-property.md)  
- [IMAPISupport: IUnknown](imapisupportiunknown.md)

