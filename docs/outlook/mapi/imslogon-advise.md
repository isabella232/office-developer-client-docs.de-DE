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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: abe4867b965f05e781f931d2e72920474d007d78
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317311"
---
# <a name="imslogonadvise"></a>IMSLogon::Advise

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Registriert ein Objekt bei einem Nachrichtenspeicheranbieter für Benachrichtigungen über Änderungen im Nachrichtenspeicher. Der Nachrichtenspeicher sendet dann Benachrichtigungen über Änderungen am registrierten Objekt.
  
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
  
> [in] Die Größe des Eintragsbezeichners in Bytes, auf den der  _lpEntryID-Parameter_ verweist. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf den Eintragsbezeichner des Objekts, über das Benachrichtigungen generiert werden sollen. Dieses Objekt kann ein Ordner, eine Nachricht oder ein beliebiges anderes Objekt im Nachrichtenspeicher sein. Wenn MAPI den  _cbEntryID-Parameter_ auf 0 legt und **null** für  _lpEntryID_ übergibt, stellt die Hinweisesenke Benachrichtigungen zu Änderungen am gesamten Nachrichtenspeicher zur Hand.
    
 _ulEventMask_
  
> [in] Eine Ereignismaske der Arten von Benachrichtigungsereignissen, die für das Objekt auftreten, über das MAPI Benachrichtigungen generiert. Die Maske filtert bestimmte Fälle. Jedem Ereignistyp ist eine Struktur zugeordnet, die zusätzliche Informationen zum Ereignis enthält. In der folgenden Tabelle sind die möglichen Ereignistypen zusammen mit den entsprechenden Strukturen aufgeführt.
    
|**Benachrichtigungsereignistyp**|**Entsprechende Struktur**|
|:-----|:-----|
|fnevCriticalError  <br/> |[ERROR_NOTIFICATION](error_notification.md) <br/> |
|fnevNewMail  <br/> |[NEWMAIL_NOTIFICATION](newmail_notification.md) <br/> |
|fnevObjectCreated  <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|fnevObjectDeleted  <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|fnevObjectModified  <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|fnevObjectCopied  <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|fnevObjectMoved  <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|fnevSearchComplete  <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|fnevStatusObjectModified  <br/> |[STATUS_OBJECT_NOTIFICATION](status_object_notification.md) <br/> |
   
 _lpAdviseSink_
  
> [in] Ein Zeiger auf ein Advise Sink-Objekt, das aufgerufen werden soll, wenn ein Ereignis für das Sitzungsobjekt auftritt, über das eine Benachrichtigung angefordert wurde. Dieses ratende Sink-Objekt muss bereits vorhanden sein.
    
 _lpulConnection_
  
> [out] Ein Zeiger auf eine Variable, die bei erfolgreicher Rückgabe die Verbindungsnummer für die Benachrichtigungsregistrierung enthält. Die Verbindungsnummer muss ungleich Null sein.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_NO_SUPPORT 
  
> Der Vorgang wird weder von MAPI noch von einem oder mehreren Dienstanbietern unterstützt.
    
## <a name="remarks"></a>Hinweise

Nachrichtenspeicheranbieter implementieren die **IMSLogon::Advise-Methode,** um ein Objekt für Benachrichtigungsrückrufe zu registrieren. Wenn eine Änderung am angegebenen Objekt auftritt, überprüft der Anbieter, welches Ereignismaskenbit im  _ulEventMask-Parameter_ festgelegt wurde und welche Art von Änderung aufgetreten ist. Wenn ein Bit festgelegt ist, ruft der Anbieter die [IMAPIAdviseSink::OnNotify-Methode](imapiadvisesink-onnotify.md) auf, damit das vom  _lpAdviseSink-Parameter_ angegebene Advise Sink-Objekt das Ereignis melden kann. Daten, die in der Benachrichtigungsstruktur an die **OnNotify-Routine** übergeben werden, beschreiben das Ereignis. 
  
Der Aufruf von **OnNotify** kann während des Aufrufs erfolgen, der das Objekt ändert, oder zu einem späteren Zeitpunkt. Auf Systemen, die mehrere Ausführungsthreads unterstützen, kann der Aufruf von **OnNotify** in jedem Thread erfolgen. Zum sicheren Behandeln eines Aufrufs von **OnNotify,** der zu einem unvorstellbarem Zeitpunkt ausgeführt werden kann, sollte eine Clientanwendung die [HrThisThreadAdviseSink-Funktion](hrthisthreadadvisesink.md) verwenden. 
  
Um Benachrichtigungen bereitstellen zu können, muss der Nachrichtenspeicheranbieter, der **Advise** implementiert, eine Kopie des Zeigers auf das  _lpAdviseSink-Ratgeber-Sink-Objekt_ behalten. Dazu ruft der Anbieter die [IUnknown::AddRef-Methode](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) auf, um den Objektzeiger zu verwalten, bis die Benachrichtigungsregistrierung mit einem Aufruf der [IMSLogon::Unadvise-Methode](imslogon-unadvise.md) abgebrochen wird. Die **Advise-Implementierung** sollte der Benachrichtigungsregistrierung eine Verbindungsnummer zuweisen und **AddRef** für diese Verbindungsnummer aufrufen, bevor sie im  _lpulConnection-Parameter zurückgesenkt_ wird. Dienstanbieter können das Advise -Sink-Objekt vor dem Abbrechen der Registrierung los, aber sie dürfen die Verbindungsnummer erst los, wenn **Unadvise** aufgerufen wurde. 
  
Nachdem ein Aufruf von **Advise** erfolgreich war und **unadvise** aufgerufen wurde, müssen Anbieter darauf vorbereitet sein, dass das Advise Sink-Objekt freigegeben wird. Daher sollte ein Anbieter sein Advise -Sink-Objekt nach **der Rückgabe** von Advise veröffentlichen, es sei denn, er hat eine bestimmte langfristige Verwendung dafür. 
  
Weitere Informationen zum Benachrichtigungsprozess finden Sie unter [Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md). 
  
## <a name="see-also"></a>Siehe auch



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMSLogon::Unadvise](imslogon-unadvise.md)
  
[Benachrichtigung](notification.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

