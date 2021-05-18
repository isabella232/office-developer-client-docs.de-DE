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
  
Registriert, um Benachrichtigungen über angegebene Ereignisse zu erhalten, die sich auf den Nachrichtenspeicher auswirken.
  
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
  
> [in] Die Byteanzahl im Eintragsbezeichner, auf den der  _lpEntryID-Parameter_ verweist. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf den Eintragsbezeichner des Ordners oder der Nachricht, über den Benachrichtigungen generiert werden sollen, oder **null**. Wenn  _lpEntryID_ auf NULL festgelegt ist, registriert **Advise** Benachrichtigungen im gesamten Nachrichtenspeicher. 
    
 _ulEventMask_
  
> [in] Eine Maske mit Werten, die die Arten von Benachrichtigungsereignissen angibt, die der Anrufer interessiert und in die Registrierung einbezogen werden sollte. Jedem Ereignistyp ist eine entsprechende [NOTIFICATION-Struktur](notification.md) zugeordnet, die Informationen zum Ereignis enthält. Es folgen gültige Werte für den _ulEventMask-Parameter:_ 
    
 _fnevCriticalError_
  
> Registriert für Benachrichtigungen über schwerwiegende Fehler, z. B. unzureichenden Arbeitsspeicher.
    
 _fnevExtended_
  
> Registriert für Benachrichtigungen über Ereignisse, die für den jeweiligen Nachrichtenspeicheranbieter spezifisch sind.
    
 _fnevNewMail_
  
> Registriert für Benachrichtigungen über das Eintreffen neuer Nachrichten. 
    
 _fnevObjectCreated_
  
> Registriert für Benachrichtigungen über die Erstellung eines neuen Ordners oder einer neuen Nachricht.
    
 _fnevObjectCopied_
  
> Registriert für Benachrichtigungen über einen zu kopierenden Ordner oder eine Nachricht.
    
 _fnevObjectDeleted_
  
> Registriert für Benachrichtigungen über einen zu löschenden Ordner oder eine Nachricht.
    
 _fnevObjectModified_
  
> Registriert für Benachrichtigungen über einen zu ändernden Ordner oder eine Nachricht.
    
 _fnevObjectMoved_
  
> Registriert für Benachrichtigungen über einen verschobenen Ordner oder eine Nachricht.
    
 _fnevSearchComplete_
  
> Registriert für Benachrichtigungen über den Abschluss eines Suchvorgangs.
    
 _lpAdviseSink_
  
> [in] Ein Zeiger auf ein Advise Sink-Objekt, um die nachfolgenden Benachrichtigungen zu erhalten. Dieses Ratensenkenobjekt muss bereits zugewiesen worden sein.
    
 _lpulConnection_
  
> [out] Ein Zeiger auf eine Nullnummer, die die Verbindung zwischen dem Ratensenkenobjekt des Anrufers und der Sitzung darstellt. 
    
 _lpAdviseSink_
  
> [in] Ein Zeiger auf ein Advise Sink-Objekt, um die nachfolgenden Benachrichtigungen zu erhalten. Dieses Ratensenkenobjekt muss bereits zugewiesen worden sein. 
    
 _lpulConnection_
  
> [out] Ein Zeiger auf eine Verbindungsnummer ungleich Null, die die Verbindung zwischen dem Ratensenkenobjekt des Anrufers und dem Nachrichtenspeicher darstellt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Registrierung war erfolgreich.
    
MAPI_E_NO_SUPPORT 
  
> Der Nachrichtenspeicheranbieter unterstützt keine Registrierung für Benachrichtigungen über den Nachrichtenspeicher.
    
## <a name="remarks"></a>Hinweise

Mit **der IMsgStore::Advise-Methode** wird eine Verbindung zwischen dem Ratensenkenobjekt des Aufrufers und dem Nachrichtenspeicher oder einem Objekt im Nachrichtenspeicher erstellt. Diese Verbindung wird verwendet, um Benachrichtigungen an die Ratensenke zu senden, wenn ein oder mehrere Ereignisse, wie im  _ulEventMask-Parameter_ angegeben, für das advise-Quellobjekt auftreten. Wenn der  _lpEntryID-Parameter_ auf einen gültigen Eintragsbezeichner verweist, ist die Advise-Quelle das durch diesen Eintragsbezeichner identifizierte Objekt. Wenn  _lpEntryID_ NULL ist, ist die Informationsquelle der Nachrichtenspeicher. 
  
Zum Senden einer Benachrichtigung ruft der Nachrichtenspeicheranbieter oder mapI die [IMAPIAdviseSink::OnNotify-Methode](imapiadvisesink-onnotify.md) der registrierten Hinweissenke auf. Einer der Parameter für **OnNotify**, eine Benachrichtigungsstruktur, enthält Informationen, die das spezifische Ereignis beschreiben.
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Sie können Benachrichtigungen mit oder ohne Hilfe von MAPI unterstützen. MAPI verfügt über drei Unterstützungsobjektmethoden, mit deren Hilfe Dienstanbieter Benachrichtigungen implementieren können: [IMAPISupport::Subscribe](imapisupport-subscribe.md), [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)und [IMAPISupport::Notify](imapisupport-notify.md). Wenn Sie die MAPI-Supportmethoden verwenden möchten, rufen Sie **Subscribe** auf, wenn Ihre **Advise-Methode** aufgerufen wird, und geben Sie den  _lpAdviseSink-Zeiger_ frei. 
  
Wenn Sie die Benachrichtigung selbst unterstützen möchten, rufen Sie die [IUnknown::AddRef-Methode](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) der Durchwahlsenke auf, die durch den  _lpAdviseSink-Parameter_ dargestellt wird, um eine Kopie dieses Zeigers zu behalten. Bewahren Sie diese Kopie auf, bis Ihre [IMsgStore::Unadvise-Methode](imsgstore-unadvise.md) aufgerufen wird, um die Registrierung abbricht. 
  
Weisen Sie unabhängig davon, wie Sie die Benachrichtigung unterstützen, der Benachrichtigungsregistrierung eine Verbindungsnummer ungleich Null zu, und geben Sie sie im  _lpulConnection-Parameter_ zurück. Geben Sie diese Verbindungsnummer erst frei, **wenn Unadvise** aufgerufen und abgeschlossen wurde. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Auf Systemen, die mehrere Ausführungsthreads unterstützen, kann der Aufruf von **OnNotify** jederzeit auch in jedem Thread erfolgen. Wenn Sie sicher sein müssen, dass Benachrichtigungen nur zu einem bestimmten Zeitpunkt in einem bestimmten Thread auftreten, rufen Sie die [HrThisThreadAdviseSink-Funktion](hrthisthreadadvisesink.md) auf, um das an **Advise** übergebene Advise-Sink-Objekt zu generieren. 
  
Nachdem ein Aufruf von **Advise** erfolgreich war und **Unadvise** zum Abbrechen der Registrierung aufgerufen wurde, sollten Sie darauf vorbereitet sein, dass das Objekt "Advise Sink" freigegeben wird. Sie sollten Ihr Advise Sink-Objekt nach **der Rückgabe von Advise** frei geben, es sei denn, Sie haben eine bestimmte langfristige Verwendung dafür. 
  
Weitere Informationen zum Benachrichtigungsprozess finden Sie unter [Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md). 
  
Weitere Informationen zum Behandeln von Benachrichtigungen finden Sie unter [Handling Notifications](handling-notifications.md). 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|BaseDialog.cpp  <br/> |CBaseDialog::OnNotificationsOn  <br/> |MFCMAPI verwendet die **IMsgStore::Advise-Methode,** um sich für Benachrichtigungen im gesamten Nachrichtenspeicher zu registrieren.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMsgStore::Unadvise](imsgstore-unadvise.md)
  
[Benachrichtigung](notification.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

