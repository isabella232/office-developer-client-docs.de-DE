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
ms.openlocfilehash: 3b4abef731541e308b2c2ebc6f4aaddf4458e257
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317325"
---
# <a name="imsgstoreadvise"></a>IMsgStore::Advise

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Registriert die Benachrichtigung über angegebene Ereignisse, die sich auf den Nachrichtenspeicher auswirken.
  
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
  
> in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEntryID_ -Parameter verwiesen wird. 
    
 _lpEntryID_
  
> in Ein Zeiger auf die Eintrags-ID des Ordners oder der Nachricht, über die Benachrichtigungen generiert werden sollen, oder **null**. Wenn _lpEntryID_ auf NULL festgelegt ist, **Raten** Sie Register für Benachrichtigungen im gesamten Nachrichtenspeicher. 
    
 _ulEventMask_
  
> in Eine Maske mit Werten, die die Typen von Benachrichtigungsereignissen angibt, an denen der Anrufer interessiert ist, und die in die Registrierung aufgenommen werden sollen. Jeder Art von Ereignis [](notification.md) , das Informationen über das Ereignis enthält, ist eine entsprechende Benachrichtigungsstruktur zugeordnet. Im folgenden finden Sie gültige Werte für den Parameter _ulEventMask_ : 
    
 _fnevCriticalError_
  
> Registriert Benachrichtigungen zu schwerwiegenden Fehlern, beispielsweise unzureichenden Arbeitsspeicher.
    
 _fnevExtended_
  
> Registriert Benachrichtigungen zu Ereignissen, die spezifisch für den jeweiligen Nachrichtenspeicher Anbieter sind.
    
 _Uleventmaskfnevnewmail_
  
> Registriert Benachrichtigungen über das Eintreffen neuer Nachrichten. 
    
 _fnevObjectCreated_
  
> Registriert Benachrichtigungen über das Erstellen eines neuen Ordners oder einer Nachricht.
    
 _fnevObjectCopied_
  
> Registriert Benachrichtigungen zu einem Ordner oder einer Nachricht, die kopiert wird.
    
 _fnevObjectDeleted_
  
> Registriert Benachrichtigungen zu einem Ordner oder einer Nachricht, die gelöscht wird.
    
 _fnevObjectModified_
  
> Registriert Benachrichtigungen zu einem Ordner oder einer Nachricht, die geändert wird.
    
 _fnevObjectMoved_
  
> Registriert Benachrichtigungen zu einem Ordner oder einer Nachricht, die verschoben wird.
    
 _fnevSearchComplete_
  
> Registriert Benachrichtigungen über den Abschluss eines Suchvorgangs.
    
 _lpAdviseSink_
  
> in Ein Zeiger auf ein Advise-Senke-Objekt, um die nachfolgenden Benachrichtigungen zu empfangen. Dieses Advise-Senke-Objekt muss bereits zugeordnet worden sein.
    
 _lpulConnection_
  
> Out Ein Zeiger auf eine Zahl ungleich NULL, die die Verbindung zwischen dem Advise-Objekt des Empfängers und der Sitzung darstellt. 
    
 _lpAdviseSink_
  
> in Ein Zeiger auf ein Advise-Senke-Objekt, um die nachfolgenden Benachrichtigungen zu empfangen. Dieses Advise-Senke-Objekt muss bereits zugeordnet worden sein. 
    
 _lpulConnection_
  
> Out Ein Zeiger auf eine Verbindungsnummer ungleich NULL, die die Verbindung zwischen dem Advise-Objekt des Empfängers und dem Nachrichtenspeicher darstellt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Registrierung war erfolgreich.
    
MAPI_E_NO_SUPPORT 
  
> Der Nachrichtenspeicher Anbieter unterstützt keine Registrierung für Benachrichtigungen über den Nachrichtenspeicher.
    
## <a name="remarks"></a>Bemerkungen

Die **IMsgStore:: Advise** -Methode stellt eine Verbindung zwischen dem Advise-Objekt des Anrufers und dem Nachrichtenspeicher oder einem Objekt im Nachrichtenspeicher her. Diese Verbindung wird verwendet, um Benachrichtigungen an die Advise-Senke zu senden, wenn mindestens ein Ereignis, wie im _ulEventMask_ -Parameter angegeben, für das Advise-Quellobjekt auftritt. Wenn der _lpEntryID_ -Parameter auf eine gültige Eintrags-ID zeigt, ist die Advise-Quelle das Objekt, das durch diese Eintrags-ID identifiziert wird. Wenn _lpEntryID_ ist, ist die Advise-Quelle der Nachrichtenspeicher. 
  
Zum Senden einer Benachrichtigung ruft der Nachrichtenspeicher Anbieter oder die MAPI die [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) -Methode der registrierten Advise-Senke auf. Einer der Parameter für **OnNotify**, eine Benachrichtigungsstruktur, enthält Informationen, die das spezifische Ereignis beschreiben.
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Sie können Benachrichtigungen mit oder ohne Hilfe von MAPI unterstützen. MAPI verfügt über drei Support Objektmethoden, mit denen Dienstanbieter die Benachrichtigung implementieren können: [IMAPISupport:: subscribe](imapisupport-subscribe.md), [IMAPISupport:: unsubscribe](imapisupport-unsubscribe.md)und [IMAPISupport:: notify](imapisupport-notify.md). Wenn Sie die MAPI-Supportmethoden verwenden möchten, rufen Sie **subscribe** auf, wenn Ihre **Advise** -Methode aufgerufen wird, und geben Sie den _lpAdviseSink_ -Zeiger frei. 
  
Wenn Sie sich für die Unterstützung der Benachrichtigung entscheiden, rufen Sie die [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) -Methode der Advise-Senke auf, die durch den _lpAdviseSink_ -Parameter dargestellt wird, um eine Kopie dieses Zeigers aufzubewahren. Bewahren Sie diese Kopie auf, bis die [IMsgStore:: Unadvise](imsgstore-unadvise.md) -Methode aufgerufen wird, um die Registrierung abzubrechen. 
  
Unabhängig davon, wie Sie die Benachrichtigung unterstützen, weisen Sie der Benachrichtigungs Registrierung eine unGleich NULL-Verbindung zu und geben Sie im _lpulConnection_ -Parameter zurück. Geben Sie diese Verbindungsnummer nicht frei **** , bis Unadvise aufgerufen und abgeschlossen wurde. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Auf Systemen, die mehrere Threads der Ausführung unterstützen, kann **** der Aufruf von OnNotify auch jederzeit in jedem Thread auftreten. Wenn Sie sicher sein müssen, dass Benachrichtigungen nur zu einem bestimmten Zeitpunkt für einen bestimmten Thread auftreten, rufen Sie die [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) -Funktion auf, um das Advise-Objekt, das Sie an **Advise**weitergeben, zu generieren. 
  
Nachdem ein Anruf bei **Advise** erfolgreich war und bevor **Unadvise** aufgerufen wurde, um die Registrierung abzubrechen, müssen Sie darauf vorbereitet sein, dass das Advise-Senke-Objekt freigegeben werden soll. Sie sollten Ihr Advise-Senke-Objekt freigeben, nachdem **Advise** zurückgegeben wird, es sei denn, Sie haben eine bestimmte langfristige Verwendung dafür. 
  
Weitere Informationen zum Benachrichtigungsprozess finden Sie unter [Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md). 
  
Weitere Informationen zum Behandeln von Benachrichtigungen finden Sie unter [Handling Notifications](handling-notifications.md). 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|BaseDialog. cpp  <br/> |CBaseDialog:: OnNotificationsOn  <br/> |MFCMAPI verwendet die **IMsgStore:: Advise** -Methode, um Benachrichtigungen für den gesamten Nachrichtenspeicher zu registrieren.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMsgStore::Unadvise](imsgstore-unadvise.md)
  
[Benachrichtigung](notification.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

