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
ms.openlocfilehash: 87be00bce55fabda6271b472a9e5c446aaf8054a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792656"
---
# <a name="imslogonadvise"></a>IMSLogon::Advise

  
  
**Betrifft**: Outlook 
  
Registriert ein Objekt mit einem Anbieter für Benachrichtigungen zu Änderungen im Nachrichtenspeicher Nachricht. Nachrichtenspeicher sendet dann Benachrichtigungen zu Änderungen an das registrierte Objekt.
  
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
  
> [in] Die Größe des Eintrags-ID, die auf das durch den Parameter _LpEntryID_ in Bytes. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf die Eintrags-ID des Objekts darüber, welche Benachrichtigungen generiert werden soll. Dieses Objekt kann es sich um einen Ordner, eine Nachricht oder ein anderes Objekt in der Nachrichtenspeicher sein. Alternativ MAPI der _CbEntryID_ -Parameter auf 0 festgelegt, und übergibt **null** für _LpEntryID_, werden der Advise-Empfänger Benachrichtigungen zu Änderungen an den Speicher für die gesamte Nachricht bereitgestellt.
    
 _ulEventMask_
  
> [in] Ein Ereignismaske der Typen der Benachrichtigungsereignisse für das Objekt zu dem MAPI-Benachrichtigungen generiert wird. Die Maske Filter Sonderfälle. Jeder Ereignistyp hat eine Struktur zugeordnet, die zusätzliche Informationen über das Ereignis enthält. Die folgende Tabelle enthält die möglichen Ereignistypen zusammen mit ihren entsprechenden Strukturen.
    
|**Benachrichtigungstyp-Ereignis**|**Entsprechende Struktur**|
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
  
> [in] Ein Zeiger auf eine Advise-Empfängerobjekt aufgerufen werden, wenn ein Ereignis für das Sitzungsobjekt auftritt darüber, welche Benachrichtigung angefordert wurde. Diese Advise-Empfängerobjekt muss bereits vorhanden sein.
    
 _lpulConnection_
  
> [out] Ein Zeiger auf eine Variable, die bei einer erfolgreichen Rückgabe die Anzahl der Verbindung für die benachrichtigungsregistrierung enthält. Die Nummer muss ungleich NULL sein.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_NO_SUPPORT 
  
> Der Vorgang wird durch MAPI oder durch eine oder mehrere Dienstanbieter nicht unterstützt.
    
## <a name="remarks"></a>Bemerkungen

Nachricht-Anbieter implementiert die **IMSLogon::Advise** -Methode, um ein Objekt für Benachrichtigung Rückrufe registrieren. Wenn eine Änderung für das angegebene Objekt auftritt, überprüft der Anbieter finden Sie unter welche Ereignis Maskenbit im Parameter _UlEventMask_ gesetzt wurde und somit die Art der Änderung. Wenn ein bit festgelegt ist, ruft der Anbieter die [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) -Methode für die Advise-Empfängerobjekt durch den Parameter _LpAdviseSink_ Sie das Ereignis melden angegeben. Daten, die in der Benachrichtigungsstruktur der **OnNotify** Routine übergeben wird das Ereignis beschrieben. 
  
Der Aufruf von **OnNotify** kann auftreten, während des Anrufs, der das Objekt geändert wird, oder zu einem späteren Zeitpunkt. Auf Systemen, die mehreren Threads der Ausführung zu unterstützen, kann der Aufruf von **OnNotify** auf einem beliebigen Thread auftreten. Um einen Anruf an **OnNotify** sicher zu behandeln, die zu einem ungünstigen Zeitpunkt auftreten, sollte eine Clientanwendung die [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) -Funktion verwenden. 
  
Um Benachrichtigungen zu ermöglichen, der Nachricht Speicher-Anbieter, der **Advise** muss eine Kopie des Zeigers auf das _LpAdviseSink_ implementiert advise-Empfängerobjekt; Hierzu ruft der Anbieter die [IUnknown:: AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) -Methode für die Advise-Empfänger, dessen Objektzeiger verwalten, bis benachrichtigungsregistrierung mit einem Aufruf der Methode [IMSLogon::Unadvise](imslogon-unadvise.md) abgebrochen wird. Die **Advise** -Implementierung sollte weisen eine Verbindungsnummer zu der benachrichtigungsregistrierung und rufen **AddRef** für diese Verbindungsnummer vor der Rückgabe im _LpulConnection_ -Parameter. Dienstanbieter können das Empfängerobjekt Advise freigeben, müssen sie die Nummer nicht freigeben, bis **Unadvise** aufgerufen wurde, bevor die Registrierung wird abgebrochen. 
  
Nachdem ein Aufruf von **Advise** erfolgreich abgeschlossen wurde und bevor **Unadvise** aufgerufen wurde, müssen für das Empfängerobjekt Advise freigegeben werden muss Anbieter vorbereitet werden. Daher sollte ein Anbieter seine Advise-Empfängerobjekt freigeben, nachdem **Advise** zurückgegeben wird, sofern eine bestimmte langfristige Verwendung dafür ist. 
  
Weitere Informationen zu den Benachrichtigungsprozess finden Sie unter [Event Notification in MAPI](event-notification-in-mapi.md). 
  
## <a name="see-also"></a>Siehe auch



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMSLogon::Unadvise](imslogon-unadvise.md)
  
[Benachrichtigung](notification.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

