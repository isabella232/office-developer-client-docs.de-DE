---
title: IMAPISessionAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.Advise
api_type:
- COM
ms.assetid: a6a6b6b1-31e2-4899-a5fe-74d5d1c2ccfc
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d5d87d7be9cb3524445107e975a298d4afd5bf98
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419835"
---
# <a name="imapisessionadvise"></a>IMAPISession::Advise

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Registriert die Benachrichtigung über die angegebenen Ereignisse, die sich auf die Sitzung auswirken.
  
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
  
> in Ein Zeiger auf die Eintrags-ID des Adressbuch-oder Nachrichtenspeicher Objekts, über das Benachrichtigungen generiert werden sollen, oder NULL, was darauf hinweist, dass der Client sich für den Empfang von Benachrichtigungen über Ereignisse registriert, die sich nur auf die Sitzung auswirken. 
    
 _ulEventMask_
  
> in Eine Maske mit Werten, die die Typen von Benachrichtigungsereignissen angibt, an denen der Client interessiert ist, und die in die Registrierung aufgenommen werden sollen. Wenn _lpEntryID_ ist, registriert MAPI den Client automatisch auf kritische Fehlerereignisse, die nur die Sitzung betreffen. Wenn _lpEntryID_ auf eine Eintrags-ID zeigt, sind die folgenden Werte für den _ulEventMask_ -Parameter gültig: 
    
fnevCriticalError 
  
> Registriert Benachrichtigungen zu schwerwiegenden Fehlern, beispielsweise unzureichenden Arbeitsspeicher.
    
fnevExtended 
  
> Registriert Benachrichtigungen zu Ereignissen, die für ein bestimmtes Adressbuch oder einen bestimmten Nachrichtenspeicher Anbieter spezifisch sind, sowie für die Sitzungs Sperrung.
    
Uleventmaskfnevnewmail 
  
> Registriert Benachrichtigungen über das Eintreffen neuer Nachrichten. 
    
fnevObjectCreated 
  
> Registriert Benachrichtigungen über die Erstellung eines neuen Objekts.
    
fnevObjectCopied
  
> Registriert Benachrichtigungen zu einem kopierten Objekt.
    
fnevObjectDeleted
  
> Registriert Benachrichtigungen zu einem Objekt, das gelöscht wird.
    
fnevObjectModified
  
> Registriert Benachrichtigungen zu einem Objekt, das geändert wird.
    
fnevObjectMoved
  
> Registriert Benachrichtigungen zu einem Objekt, das verschoben wird.
    
fnevSearchComplete
  
> Registriert Benachrichtigungen über den Abschluss eines Suchvorgangs.
    
 _lpAdviseSink_
  
> in Ein Zeiger auf ein Advise-Senke-Objekt, um die nachfolgenden Benachrichtigungen zu empfangen. Dieses Advise-Senke-Objekt muss bereits zugeordnet worden sein.
    
 _lpulConnection_
  
> Out Ein Zeiger auf eine Zahl ungleich NULL, die die Verbindung zwischen dem Advise-Objekt des Empfängers und der Sitzung darstellt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Registrierung war erfolgreich.
    
MAPI_E_INVALID_ENTRYID 
  
> Die Eintrags-ID, auf die durch _lpEntryID_ verwiesen wird, stellt keine gültige Eintrags-ID dar. 
    
MAPI_E_NO_SUPPORT 
  
> Der Dienstanbieter, der für den Eintragsbezeichner verantwortlich ist, auf den von _lpEntryID_ verwiesen wird, unterstützt entweder nicht die im Parameter _ulEventMask_ angegebene Art von Ereignissen oder unterstützt die Benachrichtigung nicht. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Die Eintrags-ID, auf die durch _lpEntryID_ verwiesen wird, kann von keinem der Dienstanbieter im Profil verarbeitet werden. 
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISession:: Advise** -Methode stellt eine Verbindung zwischen dem Advise-Objekt des Anrufers, der Sitzung und optional einem Dienstanbieter her. Diese Verbindung wird verwendet, um Benachrichtigungen an die Advise-Senke zu senden, wenn ein oder mehrere im _ulEventMask_ -Parameter angegebene Ereignisse für das Objekt auftreten, auf das durch _lpEntryID_verwiesen wird. Wenn _lpEntryID_ ist, ist das Zielobjekt die Sitzung, und Benachrichtigungen werden nur für kritische Fehler und erweiterte Ereignisse gesendet. 
  
Wenn _lpEntryID_ auf eine gültige Eintrags-ID zeigt, ruft MAPI die **Advise** -Methode des LOGON-Objekts auf, das zum Verantwortlichen Dienstanbieter gehört. Wenn _lpEntryID_ beispielsweise auf den Eintragsbezeichner einer Verteilerliste zeigt, ruft MAPI die [IABLogon:: Advise](iablogon-advise.md) -Methode des entsprechenden Adressbuch Anbieters auf. 
  
Zum Senden einer Benachrichtigung ruft der Dienstanbieter oder die MAPI die [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) -Methode der registrierten Advise-Senke auf. Einer der Parameter für **OnNotify**, eine Benachrichtigungsstruktur, enthält Informationen, die das spezifische Ereignis beschreiben.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Auf Systemen, die mehrere Threads der Ausführung unterstützen, kann **** der Aufruf von OnNotify auch jederzeit in jedem Thread auftreten. Wenn Sie sicherstellen möchten, dass Benachrichtigungen nur zu einem bestimmten Zeitpunkt für einen bestimmten Thread auftreten, rufen Sie die [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) -Funktion auf, um das Advise-Senke-Objekt zu generieren, das Sie an die **Advise** -Methode weitergeben. 
  
Um zu bestimmen, wann sich ein Client abgemeldet hat, registrieren Sie sich in Ihrem Dienstanbieter, indem Sie **Advise** aufrufen, wobei _lpEntryID_ auf NULL festgelegt und _cbEntryID_ auf 0 festgelegt ist. Wenn die Abmeldung auftritt, erhalten Sie eine fnevExtended-Benachrichtigung. 
  
Nachdem ein Anruf bei **Advise** erfolgreich abgeschlossen wurde und bevor [IMAPISession:: Unadvise](imapisession-unadvise.md) aufgerufen wurde, um die Registrierung abzubrechen, lassen Sie Ihr Advise-Senke-Objekt Los, es sei denn, Sie haben eine bestimmte langfristige Verwendung dafür. 
  
Eine Übersicht über den Benachrichtigungsprozess finden Sie unter [Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md). 
  
Weitere Informationen zum Behandeln von Benachrichtigungen finden Sie unter [Handling Notifications](handling-notifications.md). 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|BaseDialog. cpp  <br/> |CBaseDialog:: OnNotificationsOn  <br/> |MFCMAPI verwendet die **IMAPISession:: Advise** -Methode, um Benachrichtigungen für die Sitzung zu registrieren.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IABLogon::Advise](iablogon-advise.md)
  
[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPISession::Unadvise](imapisession-unadvise.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md)

