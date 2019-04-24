---
title: IMSLogonAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.Advise
api_type:
- COM
ms.assetid: a3c5d937-642b-463b-b5a0-5d099e651895
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: abe4867b965f05e781f931d2e72920474d007d78
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317311"
---
# <a name="imslogonadvise"></a>IMSLogon::Advise

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Registriert ein Objekt bei einem Nachrichtenspeicher Anbieter für Benachrichtigungen zu Änderungen im Nachrichtenspeicher. Der Nachrichtenspeicher sendet dann Benachrichtigungen zu Änderungen am registrierten Objekt.
  
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
  
> in Die Größe der Eintrags-ID, auf die durch den _lpEntryID_ -Parameter verwiesen wird, in Bytes. 
    
 _lpEntryID_
  
> in Ein Zeiger auf die Eintrags-ID des Objekts, über das Benachrichtigungen generiert werden sollen. Bei diesem Objekt kann es sich um einen Ordner, eine Nachricht oder ein beliebiges anderes Objekt im Nachrichtenspeicher handeln. Wenn MAPI den Parameter _cbEntryID_ auf 0 festlegt und für _lpEntryID_den Wert **null** übergibt, stellt die Advise-Senke Benachrichtigungen zu Änderungen am gesamten Nachrichtenspeicher bereit.
    
 _ulEventMask_
  
> in Eine Ereignismaske der Typen von Benachrichtigungsereignissen, die für das Objekt auftreten, über das MAPI Benachrichtigungen generiert. Die Maske filtert bestimmte Fälle. Jedem Ereignistyp ist eine Struktur zugeordnet, die zusätzliche Informationen über das Ereignis enthält. In der folgenden Tabelle sind die möglichen Ereignistypen zusammen mit den entsprechenden Strukturen aufgeführt.
    
|**Benachrichtigungs Ereignistyp**|**Entsprechende Struktur**|
|:-----|:-----|
|fnevCriticalError  <br/> |[ERROR_NOTIFICATION](error_notification.md) <br/> |
|Uleventmaskfnevnewmail  <br/> |[NEWMAIL_NOTIFICATION](newmail_notification.md) <br/> |
|fnevObjectCreated  <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|fnevObjectDeleted  <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|fnevObjectModified  <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|fnevObjectCopied  <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|fnevObjectMoved  <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|fnevSearchComplete  <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|fnevStatusObjectModified  <br/> |[STATUS_OBJECT_NOTIFICATION](status_object_notification.md) <br/> |
   
 _lpAdviseSink_
  
> in Ein Zeiger auf ein Advise-Senke-Objekt, das aufgerufen werden soll, wenn ein Ereignis für das Session-Objekt auftritt, über das die Benachrichtigung angefordert wurde. Dieses Advise-Senke-Objekt muss bereits vorhanden sein.
    
 _lpulConnection_
  
> Out Ein Zeiger auf eine Variable, die bei erfolgreicher Rückgabe die Verbindungsnummer für die Benachrichtigungs Registrierung enthält. Die Verbindungsnummer muss ungleich NULL sein.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_NO_SUPPORT 
  
> Der Vorgang wird nicht von MAPI oder von einem oder mehreren Dienstanbietern unterstützt.
    
## <a name="remarks"></a>Bemerkungen

Nachrichtenspeicher Anbieter implementieren die **IMSLogon:: Advise** -Methode, um ein Objekt für Benachrichtigungsrückrufe zu registrieren. Wenn eine Änderung für das angegebene Objekt auftritt, überprüft der Anbieter, um zu sehen, welches Ereignis Masken Bit im _ulEventMask_ -Parameter festgelegt wurde, und daher, welche Art von Änderung aufgetreten ist. Wenn ein Bit festgelegt ist, ruft der Anbieter die [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) -Methode für das vom _lpAdviseSink_ -Parameter angegebene Advise-Senke-Objekt auf, um das Ereignis zu melden. Die Daten, die in der Benachrichtigungs **** Struktur an die OnNotify-Routine übergeben werden, beschreiben das Ereignis. 
  
Der Aufruf von **OnNotify** kann während des Anrufs auftreten, der das Objekt oder zu einem späteren Zeitpunkt ändert. Auf Systemen, die mehrere Threads der Ausführung unterstützen, kann **** der Aufruf von OnNotify in jedem Thread auftreten. Um einen Anruf von onNotify **** sicher zu behandeln, der zu einem ungünstigen Zeitpunkt geschehen kann, sollte eine Clientanwendung die [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) -Funktion verwenden. 
  
Um Benachrichtigungen bereitzustellen, muss der Nachrichtenspeicher Anbieter, der **Advise** implementiert, eine Kopie des Zeigers auf das _lpAdviseSink_ -Advise-Senke-Objekt aufbewahren; Hierzu ruft der Anbieter die [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) -Methode für die Advise-Senke auf, um den Objektzeiger zu warten, bis die Benachrichtigungs Registrierung mit einem Aufruf der [IMSLogon:: Unadvise](imslogon-unadvise.md) -Methode abgebrochen wird. Die **Advise** -Implementierung sollte der Benachrichtigungs Registrierung eine Verbindungsnummer zuweisen und **AddRef** für diese Verbindungsnummer aufrufen, bevor Sie im _lpulConnection_ -Parameter zurückgegeben wird. Dienstanbieter können das Advise-Senke-Objekt freigeben, bevor die Registrierung abgebrochen wird, aber Sie dürfen **** die Verbindungsnummer erst freigeben, wenn Unadvise aufgerufen wurde. 
  
Nachdem ein Aufruf von **Advise** erfolgreich war und bevor **Unadvise** aufgerufen wurde, müssen Anbieter für das Advise-Senke-Objekt freigegeben werden vorbereitet werden. Daher sollte ein Anbieter seine Advise-Senke-Objekt nach der Rückgabe von **Advise** freigeben, es sei denn, es hat eine bestimmte langfristige Verwendung für Sie. 
  
Weitere Informationen zum Benachrichtigungsprozess finden Sie unter [Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md). 
  
## <a name="see-also"></a>Siehe auch



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMSLogon::Unadvise](imslogon-unadvise.md)
  
[Benachrichtigung](notification.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

