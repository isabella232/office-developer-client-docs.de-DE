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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3b4abef731541e308b2c2ebc6f4aaddf4458e257
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317325"
---
# <a name="imsgstoreadvise"></a>IMsgStore::Advise

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Registriert, um Benachrichtigungen über angegebene Ereignisse zu empfangen, die sich auf den Nachrichtenspeicher auswirken.
  
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
  
> in Ein Zeiger auf die Eintrags-ID des Ordners oder der Nachricht, über die Benachrichtigungen generiert werden sollen, oder **null**. Wenn _lpEntryID_ auf NULL festgelegt ist, **Benachrichtigen** Sie Register für Benachrichtigungen im gesamten Nachrichtenspeicher. 
    
 _ulEventMask_
  
> in Eine Maske mit Werten, die die Typen von Benachrichtigungsereignissen angibt, an denen der Anrufer interessiert ist und in die Registrierung einbezogen werden sollte. Jeder Art von Ereignis [](notification.md) , das Informationen über das Ereignis enthält, ist eine entsprechende Benachrichtigungsstruktur zugeordnet. Im folgenden sind gültige Werte für den _ulEventMask_ -Parameter angegeben: 
    
 _fnevCriticalError_
  
> Registriert für Benachrichtigungen zu schweren Fehlern, beispielsweise unzureichenden Arbeitsspeicher.
    
 _fnevExtended_
  
> Registriert Benachrichtigungen zu Ereignissen, die für den jeweiligen Nachrichtenspeicher Anbieter spezifisch sind.
    
 _uleventmaskfnevnewmail_
  
> Registriert für Benachrichtigungen über das Eintreffen neuer Nachrichten. 
    
 _fnevObjectCreated_
  
> Registriert für Benachrichtigungen über die Erstellung eines neuen Ordners oder einer neuen Nachricht.
    
 _fnevObjectCopied_
  
> Registriert für Benachrichtigungen zu einem Ordner oder einer Nachricht, die kopiert wird.
    
 _fnevObjectDeleted_
  
> Registriert für Benachrichtigungen zu einem Ordner oder einer Nachricht, die gelöscht wird.
    
 _fnevObjectModified_
  
> Registriert für Benachrichtigungen zu einem Ordner oder einer Nachricht, die geändert wird.
    
 _fnevObjectMoved_
  
> Registriert für Benachrichtigungen zu einem Ordner oder einer Nachricht, die verschoben wird.
    
 _fnevSearchComplete_
  
> Registriert für Benachrichtigungen über den Abschluss eines Suchvorgangs.
    
 _lpAdviseSink_
  
> in Ein Zeiger auf ein Advise-Senke-Objekt, um die nachfolgenden Benachrichtigungen zu erhalten. Dieses Advise-Senke-Objekt muss bereits reserviert worden sein.
    
 _lpulConnection_
  
> Timeout Ein Zeiger auf eine Zahl ungleich NULL, die die Verbindung zwischen dem Advise-Senk Objekt des Anrufers und der Sitzung darstellt. 
    
 _lpAdviseSink_
  
> in Ein Zeiger auf ein Advise-Senke-Objekt, um die nachfolgenden Benachrichtigungen zu erhalten. Dieses Advise-Senke-Objekt muss bereits reserviert worden sein. 
    
 _lpulConnection_
  
> Timeout Ein Zeiger auf eine Verbindungsnummer ungleich NULL, die die Verbindung zwischen dem Advise-Senk Objekt des Anrufers und dem Nachrichtenspeicher darstellt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Registrierung war erfolgreich.
    
MAPI_E_NO_SUPPORT 
  
> Der Nachrichtenspeicher Anbieter unterstützt keine Registrierung für die Benachrichtigung über den Nachrichtenspeicher.
    
## <a name="remarks"></a>Hinweise

Die **IMsgStore:: Advise** -Methode richtet eine Verbindung zwischen dem Advise-Senk Objekt des Anrufers und dem Nachrichtenspeicher oder einem Objekt im Nachrichtenspeicher ein. Diese Verbindung wird zum Senden von Benachrichtigungen an die Advise-Senke verwendet, wenn ein oder mehrere Ereignisse, wie im Parameter _ulEventMask_ angegeben, im Advise-Quellobjekt auftreten. Wenn der Parameter _lpEntryID_ auf eine gültige Eintrags-ID verweist, ist die Advise-Quelle das Objekt, das durch diesen Eintragsbezeichner identifiziert wird. Wenn _lpEntryID_ NULL ist, ist die Advise-Quelle der Nachrichtenspeicher. 
  
Zum Senden einer Benachrichtigung ruft entweder der Nachrichtenspeicher Anbieter oder die MAPI die [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) -Methode der registrierten Advise-Senke auf. Einer der Parameter für **OnNotify**, eine Benachrichtigungsstruktur, enthält Informationen, die das jeweilige Ereignis beschreiben.
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Sie können die Benachrichtigung mit oder ohne Hilfe von MAPI unterstützen. MAPI verfügt über drei Unterstützungsobjekt Methoden, um Dienstanbietern bei der Implementierung der Benachrichtigung zu helfen: [IMAPISupport:: subscribe](imapisupport-subscribe.md), [IMAPISupport:: unsubscribe](imapisupport-unsubscribe.md)und [IMAPISupport:: notify](imapisupport-notify.md). Wenn Sie sich für die Verwendung der MAPI-Unterstützungsmethoden entscheiden, rufen Sie **subscribe** an, wenn Ihre **Advise** -Methode aufgerufen wird, und geben Sie den _lpAdviseSink_ -Zeiger frei. 
  
Wenn Sie die Benachrichtigung selbst unterstützen möchten, rufen Sie die [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) -Methode der Advise-Senke, die durch den _lpAdviseSink_ -Parameter dargestellt wird, auf, um eine Kopie dieses Zeigers beizubehalten. Bewahren Sie diese Kopie auf, bis Ihre [IMsgStore:: Unadvise](imsgstore-unadvise.md) -Methode aufgerufen wird, um die Registrierung abzubrechen. 
  
Unabhängig davon, wie Sie die Benachrichtigung unterstützen, weisen Sie der Benachrichtigungs Registrierung eine ungleich NULL-Verbindungsnummer zu und geben Sie im Parameter _lpulConnection_ zurück. Geben Sie diese Verbindungsnummer nicht frei **** , bis Unadvise aufgerufen wurde und abgeschlossen ist. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Auf Systemen, die mehrere Ausführungs Threads unterstützen, kann der **** Aufruf von OnNotify auch jederzeit auf jedem Thread erfolgen. Wenn Sie sicher sein müssen, dass Benachrichtigungen nur zu einem bestimmten Zeitpunkt für einen bestimmten Thread auftreten, rufen Sie die [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) -Funktion auf, um das Advise-Senke-Objekt zu generieren, das Sie an **Advise**übergeben. 
  
Nachdem ein Aufruf von **Advise** erfolgreich abgeschlossen wurde und bevor **Unadvise** aufgerufen wurde, um die Registrierung abzubrechen, müssen Sie darauf vorbereitet sein, das Advise-Senke-Objekt freizugeben. Sie sollten Ihr Advise-Senke-Objekt nach der Rückgabe von **Advise** freigeben, es sei denn, Sie haben eine bestimmte langfristige Verwendung dafür. 
  
Weitere Informationen zum Benachrichtigungsprozess finden Sie unter [Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md). 
  
Weitere Informationen zum Behandeln von Benachrichtigungen finden Sie unter [Handling Notifications](handling-notifications.md). 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|BaseDialog. cpp  <br/> |CBaseDialog::OnNotificationsOn  <br/> |MfcMapi verwendet die **IMsgStore:: Advise** -Methode, um für Benachrichtigungen im gesamten Nachrichtenspeicher zu registrieren.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMsgStore::Unadvise](imsgstore-unadvise.md)
  
[Benachrichtigung](notification.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

