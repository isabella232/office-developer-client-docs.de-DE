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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6160b8e75bdc9059965c2358b9fe7d296e1f66d2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435936"
---
# <a name="imapisupportnotify"></a>IMAPISupport::Notify

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Sendet eine Benachrichtigung über ein angegebenes Ereignis an eine Hinweisquelle, die ursprünglich über die [IMAPISupport::Subscribe-Methode](imapisupport-subscribe.md) für die Benachrichtigung registriert wurde. 
  
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
  
> [in] Ein Zeiger auf den Benachrichtigungsschlüssel für das advise-Quellobjekt. Der  _lpKey-Parameter_ darf nicht NULL sein. 
    
_cNotification_
  
> [in] Die Anzahl der Benachrichtigungsstrukturen, auf die der  _lpNotifications-Parameter_ verweist. 
    
_lpNotifications_
  
> [in] Ein Zeiger auf ein Array von [NOTIFICATION-Strukturen,](notification.md) die ausstehende Benachrichtigungen beschreiben. 
    
_lpulFlags_
  
> [in, out] Eine Bitmaske mit Flags, die den Benachrichtigungsprozess steuert. Bei der Eingabe kann das folgende Flag festgelegt werden:
    
  - MAPI_UNICODE 
    
    > Die Zeichenfolgen in den Benachrichtigungsstrukturen, auf die  _von lpNotifications_ verwiesen wird, sind im Unicode-Format. Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgen im ANSI-Format. 

    Bei der Ausgabe kann MAPI das folgende Flag festlegen:
        
  - NOTIFY_CANCELED 
    
    > Eine Rückruffunktion hat eine synchrone Benachrichtigung abgebrochen.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Benachrichtigungen wurden erfolgreich generiert.
    
## <a name="remarks"></a>Hinweise

Die **IMAPISupport::Notify-Methode** wird für alle Dienstanbieterunterstützungsobjekte implementiert. Dienstanbieter rufen **Notify auf,** um an zu fordern, dass MAPI eine Benachrichtigung für eine Ratgebersenke generiert, die zuvor über die **IMAPISupport::Subscribe-Methode** für die Benachrichtigung registriert wurde. 
  
**Notify** kopiert die Strukturen, auf die der  _lpNotifications-Parameter_ verweist, in den Arbeitsspeicher und ruft die [IMAPIAdviseSink::OnNotify-Methode](imapiadvisesink-onnotify.md) der entsprechenden Ratensenke auf. Wenn **OnNotify** mit der Benachrichtigung fertig ist, gibt es den betroffenen Arbeitsspeicher frei. Der Aufrufer muss keinen Arbeitsspeicher zuweisen. MAPI führt alle erforderlichen Speicherzuweisungen durch. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Der im  _lpKey-Parameter_ übergebene Benachrichtigungsschlüssel sollte mit dem schlüssel identisch sein, der in  _lpKey_ an die **IMAPISupport::Subscribe-Methode übergeben** wurde. Viele Anbieter verwenden den Eintragsbezeichner der Quelle "Advise" als Schlüssel, aber andere Daten, z. B. ein Dateipfad, können verwendet werden. MAPI verwendet diesen Schlüssel, um alle Registrierungen für Benachrichtigungen in der identifizierten Informationsquelle zu finden. 
  
Stellen Sie sicher, dass Sie das **lpEntryID-Element** der Benachrichtigungsstruktur auf einen langfristigen Eintragsbezeichner festlegen. 
  
Wenn Sie das NOTIFY_SYNC für den  Aufruf abonnieren für eine der ausstehenden Benachrichtigungen festlegen, ruft **Notify** die Rückruffunktionen der **IMAPIAdviseSink::OnNotify-Methode** auf, bevor sie zurückkehrt. Eine Ratensenke kann manuell oder durch Aufrufen von [HrAllocAdviseSink erstellt werden.](hrallocadvisesink.md) Die **HrAllocAdviseSink-Funktion** ermöglicht es dem Aufrufer, eine Rückruffunktion anzugeben, die **Aufrufe** als Teil der Benachrichtigung benachrichtigt. Die Rückruffunktion entspricht dem [NOTIFCALLBACK-Prototyp.](notifcallback.md) Von Clients implementierte Rückruffunktionen geben immer S_OK; Rückruffunktionen, die von Dienstanbietern implementiert werden, können CALLBACK_DISCONTINUE. 
  
Wenn eine Rückruffunktion CALLBACK_DISCONTINUE, beendet MAPI das Senden von Benachrichtigungen und gibt NOTIFY_CANCELED _LpulFlags-Parameter_ der **Notify-Methode** zurück. Sie können davon ausgehen, dass der Prozess inaktiv ist, und die Generierung von Benachrichtigungen für diesen Prozess beenden. Wenn **Notify** 0 in  _lpulFlags_ zurückgibt, ist der Prozess weiterhin aktiv, und Sie sollten weiterhin Benachrichtigungen senden.
  
Wenn Sie synchrone Benachrichtigungen verwenden, achten Sie darauf, Deadlocksituationen zu vermeiden.
  
Weitere Informationen zum Benachrichtigungsprozess finden Sie unter [Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md). 
  
## <a name="see-also"></a>Siehe auch

- [IMAPISupport::Subscribe](imapisupport-subscribe.md)  
- [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)  
- [NOTIFCALLBACK](notifcallback.md) 
- [Benachrichtigung](notification.md)  
- [NOTIFKEY](notifkey.md)  
- [PidTagRecordKey (kanonische Eigenschaft)](pidtagrecordkey-canonical-property.md)  
- [IMAPISupport: IUnknown](imapisupportiunknown.md)

