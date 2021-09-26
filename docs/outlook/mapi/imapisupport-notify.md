---
title: IMAPISupportNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.Notify
api_type:
- COM
ms.assetid: c16c668e-2c8b-4759-bbca-d0c5662b62e9
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 67d60bf7e2da26f51eafcc0192d864b447aa3b9f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620877"
---
# <a name="imapisupportnotify"></a>IMAPISupport::Notify

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Sendet eine Benachrichtigung über ein angegebenes Ereignis an eine Empfehlungsquelle, die ursprünglich über die [IMAPISupport::Subscribe-Methode](imapisupport-subscribe.md) für die Benachrichtigung registriert wurde. 
  
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
  
> [in] Ein Zeiger auf den Benachrichtigungsschlüssel für das Empfehlungsquellobjekt. Der  _lpKey-Parameter_ darf nicht NULL sein. 
    
_cNotification_
  
> [in] Die Anzahl der Benachrichtigungsstrukturen, auf die der  _lpNotifications-Parameter_ verweist. 
    
_LpNotifications_
  
> [in] Ein Zeiger auf ein Array von [NOTIFICATION-Strukturen,](notification.md) die ausstehende Benachrichtigungen beschreiben. 
    
_lpulFlags_
  
> [in, out] Eine Bitmaske mit Flags, die den Benachrichtigungsprozess steuert. Bei der Eingabe kann das folgende Kennzeichen festgelegt werden:
    
  - MAPI_UNICODE 
    
    > Die Zeichenfolgen in den Benachrichtigungsstrukturen, auf die von  _lpNotifications_ verwiesen wird, haben das Unicode-Format. Wenn das flag MAPI_UNICODE nicht festgelegt ist, haben die Zeichenfolgen das ANSI-Format. 

    Bei der Ausgabe kann die MAPI das folgende Flag festlegen:
        
  - NOTIFY_CANCELED 
    
    > Eine Rückruffunktion hat eine synchrone Benachrichtigung abgebrochen.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Benachrichtigungen wurden erfolgreich generiert.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISupport::Notify-Methode** wird für alle Supportobjekte des Dienstanbieters implementiert. Dienstanbieter rufen **"Benachrichtigen"** auf, um anzufordern, dass die MAPI eine Benachrichtigung für eine Empfehlungssenke generiert, die zuvor über die **IMAPISupport::Subscribe-Methode** für die Benachrichtigung registriert wurde. 
  
**Benachrichtigen Sie,** dass die Strukturen, auf die der  _lpNotifications-Parameter_ verweist, in den Arbeitsspeicher kopiert werden, und ruft die [IMAPIAdviseSink::OnNotify-Methode](imapiadvisesink-onnotify.md) der entsprechenden Empfehlungssenke auf. Wenn **OnNotify** mit der Benachrichtigung fertig ist, gibt es den benötigten Speicher frei. Der Aufrufer muss keinen Speicher zuordnen. MAPI führt alle erforderlichen Speicherzuweisungen durch. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Der im parameter  _lpKey_ übergebene Benachrichtigungsschlüssel sollte mit dem Schlüssel identisch sein, der in  _lpKey_ an die **IMAPISupport::Subscribe-Methode** übergeben wurde. Viele Anbieter verwenden den Eintragsbezeichner der Empfehlungsquelle als Schlüssel, aber andere Daten, z. B. ein Dateipfad, können verwendet werden. MAPI verwendet diesen Schlüssel, um alle Registrierungen für Benachrichtigungen in der identifizierten Empfehlungsquelle zu finden. 
  
Stellen Sie sicher, dass Sie das **lpEntryID-Element** der Benachrichtigungsstruktur auf einen langfristigen Eintragsbezeichner festlegen. 
  
Wenn Sie das flag NOTIFY_SYNC für den **Subscribe-Aufruf** für eine der ausstehenden Benachrichtigungen festlegen, **rufen Sie** die **IMAPIAdviseSink::OnNotify-Methodenrückruffunktionen** vor der Rückgabe auf. Eine Empfehlungssenke kann manuell oder durch Aufrufen von [HrAllocAdviseSink](hrallocadvisesink.md)erstellt werden. Mit **der HrAllocAdviseSink-Funktion** kann der Aufrufer eine Rückruffunktion angeben, die Aufrufe als Teil der Benachrichtigung **benachrichtigt.** Die Rückruffunktion entspricht dem [NOTIFCALLBACK-Prototyp.](notifcallback.md) Von Clients implementierte Rückruffunktionen geben immer S_OK zurück. von Dienstanbietern implementierte Rückruffunktionen können CALLBACK_DISCONTINUE zurückgeben. 
  
Wenn eine Rückruffunktion CALLBACK_DISCONTINUE zurückgibt, beendet MAPI das Senden von Benachrichtigungen und gibt NOTIFY_CANCELED im _LpulFlags-Parameter_ der **Notify-Methode** zurück. Sie können davon ausgehen, dass der Prozess inaktiv ist und das Generieren von Benachrichtigungen für diesen Prozess beenden. Wenn **Notify** 0 in  _lpulFlags_ zurückgibt, ist der Prozess weiterhin aktiv, und Sie sollten weiterhin Benachrichtigungen senden, sofern zutreffend.
  
Wenn Sie synchrone Benachrichtigungen verwenden, vermeiden Sie Deadlock-Situationen.
  
Weitere Informationen zum Benachrichtigungsprozess finden Sie unter [Ereignisbenachrichtigung in MAPI.](event-notification-in-mapi.md) 
  
## <a name="see-also"></a>Siehe auch

- [IMAPISupport::Subscribe](imapisupport-subscribe.md)  
- [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)  
- [NOTIFCALLBACK](notifcallback.md) 
- [Benachrichtigung](notification.md)  
- [NOTIFKEY](notifkey.md)  
- [Kanonische PidTagRecordKey-Eigenschaft](pidtagrecordkey-canonical-property.md)  
- [IMAPISupport: IUnknown](imapisupportiunknown.md)

