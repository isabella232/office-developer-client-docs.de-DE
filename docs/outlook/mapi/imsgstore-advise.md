---
title: IMsgStoreAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMsgStore.Advise
api_type:
- COM
ms.assetid: 8c57e743-a798-4e39-a61a-46dff8b1ac7c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 4dc842416200ae6a65011e994689e2792642750c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59564106"
---
# <a name="imsgstoreadvise"></a>IMsgStore::Advise

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Registriert sich, um Benachrichtigungen über angegebene Ereignisse zu erhalten, die sich auf den Nachrichtenspeicher auswirken.
  
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
  
> [in] Ein Zeiger auf den Eintragsbezeichner des Ordners oder der Nachricht, über den Benachrichtigungen generiert werden sollen, oder **NULL**. Wenn  _lpEntryID_ auf NULL festgelegt ist, **wird "Advise"** für Benachrichtigungen im gesamten Nachrichtenspeicher registriert. 
    
 _ulEventMask_
  
> [in] Eine Maske mit Werten, die die Typen von Benachrichtigungsereignissen angibt, an denen der Aufrufer interessiert ist, und die in die Registrierung einbezogen werden sollten. Jedem Ereignistyp ist eine entsprechende [NOTIFICATION-Struktur](notification.md) zugeordnet, die Informationen über das Ereignis enthält. Es folgen gültige Werte für den _ulEventMask-Parameter:_ 
    
 _fnevCriticalError_
  
> Registriert Benachrichtigungen zu schwerwiegenden Fehlern, z. B. zu wenig Arbeitsspeicher.
    
 _fnevExtended_
  
> Registriert Benachrichtigungen zu Ereignissen, die für den jeweiligen Nachrichtenspeicheranbieter spezifisch sind.
    
 _fnevNewMail_
  
> Registriert sich für Benachrichtigungen über das Eintreffen neuer Nachrichten. 
    
 _fnevObjectCreated_
  
> Registriert sich für Benachrichtigungen über die Erstellung eines neuen Ordners oder einer neuen Nachricht.
    
 _fnevObjectCopied_
  
> Registriert sich für Benachrichtigungen über einen Ordner oder eine Nachricht, die kopiert wird.
    
 _fnevObjectDeleted_
  
> Registriert sich für Benachrichtigungen über einen Ordner oder eine Nachricht, die gelöscht wird.
    
 _fnevObjectModified_
  
> Registriert Benachrichtigungen über einen Ordner oder eine Nachricht, die geändert wird.
    
 _fnevObjectMoved_
  
> Registriert Benachrichtigungen über einen Ordner oder eine Nachricht, die verschoben wird.
    
 _fnevSearchComplete_
  
> Registriert Benachrichtigungen über den Abschluss eines Suchvorgangs.
    
 _lpAdviseSink_
  
> [in] Ein Zeiger auf ein Empfehlungs-Senkenobjekt, um die nachfolgenden Benachrichtigungen zu erhalten. Dieses Empfehlungssenkenobjekt muss bereits zugeordnet worden sein.
    
 _lpulConnection_
  
> [out] Ein Zeiger auf eine Zahl ungleich Null, die die Verbindung zwischen dem "Advise Sink"-Objekt des Aufrufers und der Sitzung darstellt. 
    
 _lpAdviseSink_
  
> [in] Ein Zeiger auf ein Empfehlungs-Senkenobjekt, um die nachfolgenden Benachrichtigungen zu erhalten. Dieses Empfehlungssenkenobjekt muss bereits zugeordnet worden sein. 
    
 _lpulConnection_
  
> [out] Ein Zeiger auf eine Nicht-Null-Verbindungsnummer, die die Verbindung zwischen dem "Advise Sink"-Objekt des Aufrufers und dem Nachrichtenspeicher darstellt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Registrierung war erfolgreich.
    
MAPI_E_NO_SUPPORT 
  
> Der Nachrichtenspeicheranbieter unterstützt keine Registrierung für Benachrichtigungen über den Nachrichtenspeicher.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMsgStore::Advise-Methode** stellt eine Verbindung zwischen dem "advise"-Senkenobjekt des Aufrufers und dem Nachrichtenspeicher oder einem Objekt im Nachrichtenspeicher her. Diese Verbindung wird verwendet, um Benachrichtigungen an die Empfehlungssenke zu senden, wenn ein oder mehrere Ereignisse, wie im  _ulEventMask-Parameter_ angegeben, für das Empfehlungsquellobjekt auftreten. Wenn der  _lpEntryID-Parameter_ auf einen gültigen Eintragsbezeichner zeigt, ist die Empfehlungsquelle das durch diesen Eintragsbezeichner identifizierte Objekt. Wenn  _lpEntryID_ NULL ist, ist die Empfehlungsquelle der Nachrichtenspeicher. 
  
Um eine Benachrichtigung zu senden, ruft entweder der Nachrichtenspeicheranbieter oder die MAPI die [IMAPIAdviseSink::OnNotify-Methode](imapiadvisesink-onnotify.md) der registrierten Empfehlungssenke auf. Einer der Parameter für **OnNotify**, eine Benachrichtigungsstruktur, enthält Informationen, die das spezifische Ereignis beschreiben.
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Sie können Benachrichtigungen mit oder ohne Hilfe von MAPI unterstützen. DIE MAPI verfügt über drei Unterstützungsobjektmethoden, die Dienstanbietern beim Implementieren von Benachrichtigungen helfen: [IMAPISupport::Subscribe](imapisupport-subscribe.md), [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)und [IMAPISupport::Notify](imapisupport-notify.md). Wenn Sie die MAPI-Unterstützungsmethoden verwenden möchten, rufen **Sie Subscribe** auf, wenn Ihre **Advise-Methode** aufgerufen wird, und geben Sie den  _lpAdviseSink-Zeiger_ frei. 
  
Wenn Sie sich entscheiden, die Benachrichtigung selbst zu unterstützen, rufen Sie die [IUnknown::AddRef-Methode](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) der Rate-Senken auf, die durch den  _lpAdviseSink-Parameter_ dargestellt wird, um eine Kopie dieses Zeigers beizubehalten. Verwalten Sie diese Kopie, bis Ihre [IMsgStore::Unadvise-Methode](imsgstore-unadvise.md) aufgerufen wird, um die Registrierung abzubrechen. 
  
Unabhängig davon, wie Sie die Benachrichtigung unterstützen, weisen Sie der Benachrichtigungsregistrierung eine Nonzero-Verbindungsnummer zu und geben Sie sie im  _lpulConnection-Parameter_ zurück. Geben Sie diese Verbindungsnummer erst frei, **nachdem "Unadvise"** aufgerufen und abgeschlossen wurde. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Auf Systemen, die mehrere Ausführungsthreads unterstützen, kann der Aufruf von **OnNotify** auch jederzeit in jedem Thread erfolgen. Wenn Sie sicher sein müssen, dass Benachrichtigungen nur zu einem bestimmten Zeitpunkt in einem bestimmten Thread auftreten, rufen Sie die [HrThisThreadAdviseSink-Funktion](hrthisthreadadvisesink.md) auf, um das Anraten-Senkenobjekt zu generieren, das Sie an **Advise** übergeben. 
  
Nachdem ein Aufruf von **"Advise"** erfolgreich war und bevor **"Unadvise"** aufgerufen wurde, um die Registrierung abzubrechen, sollten Sie darauf vorbereitet sein, dass das Advise-Senkenobjekt freigegeben wird. Sie sollten Ihr Advise-Senkenobjekt freigeben, nachdem **Advise** zurückgegeben wurde, es sei denn, Sie haben eine bestimmte langfristige Verwendung dafür. 
  
Weitere Informationen zum Benachrichtigungsprozess finden Sie unter [Ereignisbenachrichtigung in MAPI.](event-notification-in-mapi.md) 
  
Weitere Informationen zum Behandeln von Benachrichtigungen finden Sie unter ["Behandeln von Benachrichtigungen".](handling-notifications.md) 
  
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

