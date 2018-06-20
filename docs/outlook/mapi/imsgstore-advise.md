---
title: IMsgStoreAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.Advise
api_type:
- COM
ms.assetid: 8c57e743-a798-4e39-a61a-46dff8b1ac7c
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 6a315cef8263f7e241a815a0f054dc3174d88fa7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792612"
---
# <a name="imsgstoreadvise"></a>IMsgStore::Advise

  
  
**Betrifft**: Outlook 
  
Um die Benachrichtigung der angegebenen Ereignisse, die Einfluss auf die Nachrichtenspeicher registriert.
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG_PTR lpulConnection
);
```

## <a name="parameters"></a>Parameter

 _cbEntryID_
  
> [in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LpEntryID_ verwiesen. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf die Eintrags-ID des Ordners oder Meldung über welche Benachrichtigungen generiert werden soll, oder **null**. Wenn _LpEntryID_ auf NULL festgelegt ist, wird für Benachrichtigungen auf dem gesamten Nachrichtenspeicher **Advise** registriert. 
    
 _ulEventMask_
  
> [in] Eine Maske von Werten, mit die die Typen von Benachrichtigungsereignisse anzugeben, die dem Anrufer ist daran interessiert, und die Registrierung einbezogen werden soll. Es wird eine entsprechende [Benachrichtigung](notification.md) Struktur jede Art von Ereignis, das Informationen über das Ereignis enthält zugeordnet. Folgende sind gültige Werte für den Parameter _UlEventMask_ : 
    
 _fnevCriticalError_
  
> Register für Benachrichtigungen zu schwerwiegenden Fehlern, beispielsweise nicht genügend Arbeitsspeicher.
    
 _fnevExtended_
  
> Register für Benachrichtigungen über Ereignisse, die speziell für bestimmte Nachricht Speicheranbieter.
    
 _fnevNewMail_
  
> Register für die Benachrichtigung über den Empfang von neuen Nachrichten. 
    
 _fnevObjectCreated_
  
> Register für die Benachrichtigung über die Erstellung einer neuen Ordner oder einer Nachricht.
    
 _fnevObjectCopied_
  
> Register für Benachrichtigungen bezüglich eines Ordners oder die Nachricht kopiert wird.
    
 _fnevObjectDeleted_
  
> Register für Benachrichtigungen bezüglich eines Ordners oder die Nachricht wird gelöscht.
    
 _fnevObjectModified_
  
> Register für Benachrichtigungen bezüglich eines Ordners oder einer Nachricht geändert wird.
    
 _fnevObjectMoved_
  
> Register für Benachrichtigungen bezüglich eines Ordners oder die Nachricht verschoben wird.
    
 _fnevSearchComplete_
  
> Register für die Benachrichtigung über den Abschluss der Suchvorgang.
    
 _lpAdviseSink_
  
> [in] Ein Zeiger auf eine Advise-Empfängerobjekt nachfolgenden Benachrichtigungen zu empfangen. Diese Advise-Empfängerobjekt muss bereits zugewiesen wurden.
    
 _lpulConnection_
  
> [out] Ein Zeiger auf eine Zahl ungleich NULL für die Verbindung zwischen des Anrufers advise-Empfängerobjekt und der Sitzung. 
    
 _lpAdviseSink_
  
> [in] Ein Zeiger auf eine Advise-Empfängerobjekt nachfolgenden Benachrichtigungen zu empfangen. Diese Advise-Empfängerobjekt muss bereits zugewiesen wurden. 
    
 _lpulConnection_
  
> [out] Ein Zeiger auf eine ungleich NULL Verbindung Zahl, die die Verbindung zwischen des Anrufers stellt advise-Empfängerobjekt und des Nachrichtenspeichers.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Registrierung erfolgreich war.
    
MAPI_E_NO_SUPPORT 
  
> Die Nachrichtenanbieter unterstützt keine Registrierung für die Benachrichtigung über den Nachrichtenspeicher.
    
## <a name="remarks"></a>Hinweise

Die **IMsgStore::Advise** -Methode richtet eine Verbindung zwischen dem Anrufer der advise-Empfängerobjekt und der Nachrichtenspeicher oder ein Objekt im Nachrichtenspeicher. Diese Verbindung wird verwendet, um das Senden von Benachrichtigungen an der Advise-Empfänger, wenn sich ein oder mehr Ereignisse, wie in den _UlEventMask_ -Parameter angegeben an das Quellobjekt Advise auftreten. Wenn der _LpEntryID_ -Parameter verweist auf eine gültige Eingabe Bezeichner, hat die Advise-Quelle das Objekt durch dieses Eintrags-ID identifiziert. Wenn _LpEntryID_ NULL ist, ist die Advise-Quelle des Nachrichtenspeichers. 
  
Um eine Benachrichtigung zu senden, die Nachricht Speicheranbieter oder MAPI der registrierten Advise-Empfänger [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) -Methode aufgerufen. Einer der Parameter zu **OnNotify**, eine Benachrichtigungsstruktur enthält Informationen des jeweiligen Ereignisses.
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Sie können die Benachrichtigung mit oder ohne Hilfe von MAPI unterstützen. MAPI hat drei Methoden von Support-Objekt zur Verfügung stehen-Dienstanbieter Benachrichtigung implementieren: [IMAPISupport::Subscribe](imapisupport-subscribe.md), [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)und [IMAPISupport::Notify](imapisupport-notify.md). Wenn Sie sich entscheiden, die MAPI-Support-Methoden verwenden, rufen Sie **Abonnieren** die **Advise** -Methode aufgerufen wird, und heben Sie den Zeiger _LpAdviseSink_ . 
  
Wenn Sie sich entscheiden, die Benachrichtigung zu unterstützen, rufen Sie die [IUnknown:: AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) -Methode der Advise-Empfänger, die durch den Parameter _LpAdviseSink_ dargestellt, um eine Kopie dieses Zeigers beizubehalten. Verwalten Sie diese Kopie, bis die [IMsgStore::Unadvise](imsgstore-unadvise.md) -Methode aufgerufen wird, um die Registrierung abzubrechen. 
  
Unabhängig davon, wie Sie Benachrichtigung zu unterstützen weisen Sie eine Zahl ungleich NULL Verbindung die benachrichtigungsregistrierung, und im Parameter _LpulConnection_ zurückzugeben. Freigegeben Sie diese Verbindungsnummer nicht, bis **Unadvise** aufgerufen wurde und dass die Benutzerreplikation abgeschlossen ist. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Auf Systemen, die mehreren Threads der Ausführung zu unterstützen, kann der Aufruf von **OnNotify** auch jederzeit auf einem beliebigen Thread auftreten. Wenn Sie müssen, die Benachrichtigungen nur zu einem bestimmten Zeitpunkt in einem bestimmten Thread auftreten sicher sein, rufen Sie die [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) -Funktion, um das Empfängerobjekt Advise generieren, das an **Advise**übergeben. 
  
Nach einem Aufruf von **Advise** erfolgreich war, und bereiten Sie vor dem **Unadvise** aufgerufen wurde, um die Registrierung abzubrechen, für das Empfängerobjekt Advise freigegeben werden muss. Sie sollten Ihre Advise-Empfängerobjekt freigeben, nachdem **Advise** zurückgegeben, es sei denn, Sie eine bestimmte langfristige Verwendung dafür haben. 
  
Weitere Informationen zu den Benachrichtigungsprozess finden Sie unter [Event Notification in MAPI](event-notification-in-mapi.md). 
  
Weitere Informationen zum Behandeln von Benachrichtigungen finden Sie unter [Behandeln von Benachrichtigungen](handling-notifications.md). 
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|BaseDialog.cpp  <br/> |CBaseDialog::OnNotificationsOn  <br/> |MFCMAPI (engl.) verwendet die **IMsgStore::Advise** -Methode, um für Benachrichtigungen auf dem gesamten Nachrichtenspeicher registrieren.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMsgStore::Unadvise](imsgstore-unadvise.md)
  
[Benachrichtigung](notification.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

