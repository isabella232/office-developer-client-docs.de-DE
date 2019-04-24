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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326369"
---
# <a name="imapisupportnotify"></a>IMAPISupport::Notify

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Sendet eine Benachrichtigung über ein angegebenes Ereignis an eine Advise-Quelle, die ursprünglich für die Benachrichtigung über die [IMAPISupport:: subscribe](imapisupport-subscribe.md) -Methode registriert wurde. 
  
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
  
> in Ein Zeiger auf den Benachrichtigungs Schlüssel für das Advise-Quellobjekt. Der _lpKey_ -Parameter darf nicht NULL sein. 
    
_cNotification_
  
> in Die Anzahl der Benachrichtigungs Strukturen, auf die durch den _lpNotifications_ -Parameter verwiesen wird. 
    
_lpNotifications_
  
> in Ein Zeiger auf ein Array von [Benachrichtigungs](notification.md) Strukturen, die ausstehende Benachrichtigungen beschreiben. 
    
_lpulFlags_
  
> [in, out] Eine Bitmaske von Flags, die den Benachrichtigungsprozess steuert. Bei Eingabe kann das folgende Flag festgelegt werden:
    
  - MAPI_UNICODE 
    
    > Die Zeichenfolgen in den Benachrichtigungs Strukturen, auf die von _lpNotifications_ verwiesen wird, liegen im Unicode-Format vor. Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, werden die Zeichenfolgen im ANSI-Format. 

    Bei der Ausgabe kann MAPI das folgende Flag festlegen:
        
  - NOTIFY_CANCELED 
    
    > Eine Rückruffunktion hat eine synchrone Benachrichtigung abgebrochen.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Benachrichtigungen wurden erfolgreich generiert.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISupport:: notify** -Methode wird für alle Support Objekte des Dienstanbieters implementiert. Dienstanbieter rufen **Notify** auf, um zu fordern, dass MAPI eine Benachrichtigung für eine Advise-Senke generiert, die zuvor für die Benachrichtigung über die **IMAPISupport:: subscribe** -Methode registriert wurde. 
  
**Notify** kopiert die Strukturen, auf die durch den _lpNotifications_ -Parameter verwiesen wird, in den Arbeitsspeicher und ruft die [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) -Methode der entsprechenden Advise-Senke auf. Wenn **OnNotify** mit der Benachrichtigung beendet wird, gibt Sie den betreffenden Arbeitsspeicher frei. Der Aufrufer muss keinen Arbeitsspeicher reservieren; MAPI führt alle erforderlichen Speicherzuordnungen aus. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Der im _lpKey_ -Parameter übergebene Benachrichtigungs Schlüssel sollte mit dem Schlüssel identisch sein, der in _LpKey_ an die **IMAPISupport:: subscribe** -Methode übergeben wird. Viele Anbieter verwenden den Eintragsbezeichner der Advise-Quelle als Schlüssel, aber andere Daten, wie beispielsweise ein Dateipfad, können verwendet werden. MAPI verwendet diesen Schlüssel, um alle Registrierungen für Benachrichtigungen in der angegebenen Advise-Quelle zu finden. 
  
Stellen Sie sicher, dass Sie das **lpEntryID** -Element der Benachrichtigungsstruktur auf eine langfristige Eintrags-ID festlegen. 
  
Wenn Sie das NOTIFY_SYNC-Flag für den **subscribe** -Aufruf für eine der ausstehenden Benachrichtigungen festlegen, ruft **Notify** die **IMAPIAdviseSink:: OnNotify** -Methoden-Rückruffunktionen vor dem zurückgeben auf. Eine Advise-Senke kann manuell oder durch Aufrufen von [HrAllocAdviseSink](hrallocadvisesink.md)erstellt werden. Mit der **HrAllocAdviseSink** -Funktion kann der Aufrufer eine Rückruffunktion angeben, die Anrufe im Rahmen der Benachrichtigung **benachrichtigt** . Die Rückruffunktion entspricht dem Prototyp [NOTIFCALLBACK](notifcallback.md) . Von Clients implementierte Rückruffunktionen geben immer S_OK zurück; von Dienstanbietern implementierte Rückruffunktionen können CALLBACK_DISCONTINUE zurückgeben. 
  
Wenn eine Rückruffunktion CALLBACK_DISCONTINUE zurückgibt, beendet MAPI das Senden von Benachrichtigungen und gibt NOTIFY_CANCELED im _lpulFlags_ -Parameter der **Notify** -Methode zurück. Sie können davon ausgehen, dass der Prozess inaktiv ist und die Generierung von Benachrichtigungen für diesen Prozess beenden. Wenn **Notify** 0 in _lpulFlags_zurückgibt, ist der Prozess weiterhin aktiv, und Sie sollten weiterhin nach Bedarf Benachrichtigungen senden.
  
Wenn Sie synchrone Benachrichtigungen verwenden, achten Sie darauf, Deadlock-Situationen zu vermeiden.
  
Weitere Informationen zum Benachrichtigungsprozess finden Sie unter [Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md). 
  
## <a name="see-also"></a>Siehe auch

- [IMAPISupport::Subscribe](imapisupport-subscribe.md)  
- [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)  
- [NOTIFCALLBACK](notifcallback.md) 
- [Benachrichtigung](notification.md)  
- [NOTIFKEY](notifkey.md)  
- [Kanonische Pidtagrecordkey (-Eigenschaft](pidtagrecordkey-canonical-property.md)  
- [IMAPISupport: IUnknown](imapisupportiunknown.md)

