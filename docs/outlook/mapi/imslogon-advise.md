---
title: IMSLogonAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMSLogon.Advise
api_type:
- COM
ms.assetid: a3c5d937-642b-463b-b5a0-5d099e651895
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2b09596fda35b85b753180ecf4c4b47c92c491a8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561488"
---
# <a name="imslogonadvise"></a>IMSLogon::Advise

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Registriert ein Objekt bei einem Nachrichtenspeicheranbieter für Benachrichtigungen zu Änderungen im Nachrichtenspeicher. Der Nachrichtenspeicher sendet dann Benachrichtigungen zu Änderungen am registrierten Objekt.
  
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
  
> [in] Die Größe (in Byte) des Eintragsbezeichners, auf den der  _parameter lpEntryID_ verweist. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf den Eintragsbezeichner des Objekts, über das Benachrichtigungen generiert werden sollen. Dieses Objekt kann ein Ordner, eine Nachricht oder ein anderes Objekt im Nachrichtenspeicher sein. Wenn mapi den  _cbEntryID-Parameter_ auf 0 festlegt und **null** für  _lpEntryID_ übergibt, stellt die Empfehlungssenke Benachrichtigungen zu Änderungen am gesamten Nachrichtenspeicher bereit.
    
 _ulEventMask_
  
> [in] Eine Ereignismaske der Typen von Benachrichtigungsereignissen, die für das Objekt auftreten, über das mapi Benachrichtigungen generiert. Die Maske filtert bestimmte Fälle. Jedem Ereignistyp ist eine Struktur zugeordnet, die zusätzliche Informationen zum Ereignis enthält. In der folgenden Tabelle sind die möglichen Ereignistypen zusammen mit den entsprechenden Strukturen aufgeführt.
    
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
  
> [in] Ein Zeiger auf ein Empfehlungssenkenobjekt, das aufgerufen werden soll, wenn ein Ereignis für das Sitzungsobjekt auftritt, zu dem die Benachrichtigung angefordert wurde. Dieses Empfehlungssenkenobjekt muss bereits vorhanden sein.
    
 _lpulConnection_
  
> [out] Ein Zeiger auf eine Variable, die bei einer erfolgreichen Rückgabe die Verbindungsnummer für die Benachrichtigungsregistrierung enthält. Die Verbindungsnummer muss ungleich Null sein.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_NO_SUPPORT 
  
> Der Vorgang wird von der MAPI oder einem oder mehreren Dienstanbietern nicht unterstützt.
    
## <a name="remarks"></a>HinwBemerkungeneise

Nachrichtenspeicheranbieter implementieren die **IMSLogon::Advise-Methode,** um ein Objekt für Benachrichtigungsrückrufe zu registrieren. Bei jeder Änderung des angegebenen Objekts überprüft der Anbieter, welches Ereignismasken-Bit im  _ulEventMask-Parameter_ festgelegt wurde und welcher Änderungstyp aufgetreten ist. Wenn ein Bit festgelegt ist, ruft der Anbieter die [IMAPIAdviseSink::OnNotify-Methode](imapiadvisesink-onnotify.md) für das vom  _lpAdviseSink-Parameter_ angegebene "advise"-Senkenobjekt auf, um das Ereignis zu melden. Daten, die in der Benachrichtigungsstruktur an die **OnNotify-Routine** übergeben werden, beschreiben das Ereignis. 
  
Der Aufruf von **OnNotify** kann während des Aufrufs erfolgen, durch den das Objekt geändert wird, oder zu einem späteren Zeitpunkt. Auf Systemen, die mehrere Ausführungsthreads unterstützen, kann der Aufruf von **OnNotify** in jedem Thread erfolgen. Eine Clientanwendung sollte die [HrThisThreadAdviseSink-Funktion](hrthisthreadadvisesink.md) verwenden, um einen Aufruf von **OnNotify** sicher zu verarbeiten, der zu einem inopportinen Zeitpunkt auftreten kann. 
  
Um Benachrichtigungen bereitzustellen, muss der Nachrichtenspeicheranbieter, der **"Advise"** implementiert, eine Kopie des Zeigers auf das  _lpAdviseSink_ Advise Sink-Objekt beibehalten. Dazu ruft der Anbieter die [IUnknown::AddRef-Methode](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) für die Rate-Senken auf, um den Objektzeiger beizubehalten, bis die Benachrichtigungsregistrierung mit einem Aufruf der [IMSLogon::Unadvise-Methode](imslogon-unadvise.md) abgebrochen wird. Die **Advise-Implementierung** sollte der Benachrichtigungsregistrierung eine Verbindungsnummer zuweisen und **AddRef** für diese Verbindungsnummer aufrufen, bevor sie im  _lpulConnection-Parameter_ zurückgegeben wird. Dienstanbieter können das Empfehlungssenkenobjekt freigeben, bevor die Registrierung abgebrochen wird, aber sie dürfen die Verbindungsnummer erst **freigeben, wenn "Unadvise"** aufgerufen wurde. 
  
Nachdem ein Aufruf von **"Advise"** erfolgreich war und bevor **"Unadvise"** aufgerufen wurde, müssen die Anbieter darauf vorbereitet sein, dass das Empfehlungssenkenobjekt freigegeben wird. Daher sollte ein Anbieter sein Empfehlungssenkenobjekt nach der Rückgabe **von Advise** freigeben, es sei denn, er verwendet es langfristig. 
  
Weitere Informationen zum Benachrichtigungsprozess finden Sie unter [Ereignisbenachrichtigung in MAPI.](event-notification-in-mapi.md) 
  
## <a name="see-also"></a>Siehe auch



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMSLogon::Unadvise](imslogon-unadvise.md)
  
[Benachrichtigung](notification.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

