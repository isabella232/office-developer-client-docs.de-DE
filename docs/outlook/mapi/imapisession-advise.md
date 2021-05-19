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
  
Registriert, um Benachrichtigungen über angegebene Ereignisse zu erhalten, die sich auf die Sitzung auswirken.
  
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
  
> [in] Ein Zeiger auf die Eintrags-ID des Adressbuch- oder Nachrichtenspeicherobjekts, über das Benachrichtigungen generiert werden sollen, oder NULL, der angibt, dass der Client sich für den Empfang von Benachrichtigungen über Ereignisse registriert, die sich nur auf die Sitzung auswirken. 
    
 _ulEventMask_
  
> [in] Eine Maske mit Werten, die die Arten von Benachrichtigungsereignissen angibt, für die der Client interessiert ist und in die Registrierung einbezogen werden sollte. Wenn  _lpEntryID_ NULL ist, registriert MAPI den Client automatisch für kritische Fehlerereignisse, die sich nur auf die Sitzung auswirken. Wenn  _lpEntryID_ auf einen Eintragsbezeichner verweist, sind die folgenden Werte für den  _ulEventMask-Parameter_ gültig: 
    
fnevCriticalError 
  
> Registriert für Benachrichtigungen über schwerwiegende Fehler, z. B. unzureichenden Arbeitsspeicher.
    
fnevExtended 
  
> Registriert für Benachrichtigungen über Ereignisse, die für ein bestimmtes Adressbuch oder einen bestimmten Nachrichtenspeicheranbieter spezifisch sind, und für das Herunterfahren der Sitzung.
    
fnevNewMail 
  
> Registriert für Benachrichtigungen über das Eintreffen neuer Nachrichten. 
    
fnevObjectCreated 
  
> Registriert für Benachrichtigungen über die Erstellung eines neuen Objekts.
    
fnevObjectCopied
  
> Registriert für Benachrichtigungen über ein objekt, das kopiert wird.
    
fnevObjectDeleted
  
> Registriert für Benachrichtigungen über ein zu löschendes Objekt.
    
fnevObjectModified
  
> Registriert für Benachrichtigungen über ein zu änderndes Objekt.
    
fnevObjectMoved
  
> Registriert für Benachrichtigungen über ein verschobenes Objekt.
    
fnevSearchComplete
  
> Registriert für Benachrichtigungen über den Abschluss eines Suchvorgangs.
    
 _lpAdviseSink_
  
> [in] Ein Zeiger auf ein Advise Sink-Objekt, um die nachfolgenden Benachrichtigungen zu erhalten. Dieses Ratensenkenobjekt muss bereits zugewiesen worden sein.
    
 _lpulConnection_
  
> [out] Ein Zeiger auf eine Nullnummer, die die Verbindung zwischen dem Ratensenkenobjekt des Anrufers und der Sitzung darstellt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Registrierung war erfolgreich.
    
MAPI_E_INVALID_ENTRYID 
  
> Der Eintragsbezeichner, auf den  _lpEntryID verweist,_ stellt keinen gültigen Eintragsbezeichner dar. 
    
MAPI_E_NO_SUPPORT 
  
> Der Dienstanbieter, der für den Eintragsbezeichner verantwortlich ist, auf den  _lpEntryID_ verweist, unterstützt entweder den im  _ulEventMask-Parameter_ angegebenen Ereignistyp nicht oder unterstützt keine Benachrichtigung. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Der Eintragsbezeichner, auf den  _lpEntryID verweist,_ kann nicht von einem der Dienstanbieter im Profil verarbeitet werden. 
    
## <a name="remarks"></a>Hinweise

Die **IMAPISession::Advise-Methode** stellt eine Verbindung zwischen dem Ratgebersenkenobjekt des Anrufers, der Sitzung und optional einem Dienstanbieter fest. Diese Verbindung wird verwendet, um Benachrichtigungen an die Ratensenke zu senden, wenn mindestens ein im _ulEventMask-Parameter_ angegebenes Ereignis auf das Objekt auftritt, auf das _von lpEntryID verwiesen wird._ Wenn  _lpEntryID_ NULL ist, ist das Zielobjekt die Sitzung, und Benachrichtigungen werden nur für kritische Fehler und erweiterte Ereignisse gesendet. 
  
Wenn  _lpEntryID_ auf einen gültigen Eintragsbezeichner verweist, ruft MAPI die **Advise-Methode** des Anmeldeobjekts auf, das zum zuständigen Dienstanbieter gehört. Wenn beispielsweise  _lpEntryID_ auf den Eintragsbezeichner einer Verteilerliste verweist, ruft MAPI die [IABLogon::Advise-Methode](iablogon-advise.md) des entsprechenden Adressbuchanbieters auf. 
  
Zum Senden einer Benachrichtigung ruft der Dienstanbieter oder die MAPI die [IMAPIAdviseSink::OnNotify-Methode](imapiadvisesink-onnotify.md) der registrierten Hinweissenke auf. Einer der Parameter für **OnNotify**, eine Benachrichtigungsstruktur, enthält Informationen, die das spezifische Ereignis beschreiben.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Auf Systemen, die mehrere Ausführungsthreads unterstützen, kann der Aufruf von **OnNotify** jederzeit auch in jedem Thread erfolgen. Wenn Sie sicher sein müssen, dass Benachrichtigungen nur zu einem bestimmten Zeitpunkt in einem bestimmten Thread auftreten, rufen Sie die [HrThisThreadAdviseSink-Funktion](hrthisthreadadvisesink.md) auf, um das Advise Sink-Objekt zu generieren, das Sie an die **Advise-Methode** übergeben. 
  
Um zu bestimmen, wann sich ein Client abgemeldet hat, registrieren Sie sich für Benachrichtigungen in Ihrem Dienstanbieter, indem Sie **Advise** aufrufen,  _wenn lpEntryID_ auf NULL und  _cbEntryID_ auf 0 festgelegt ist. Wenn die Abmeldung auftritt, erhalten Sie eine fnevExtended-Benachrichtigung. 
  
Nachdem ein Aufruf von **Advise** erfolgreich war und [bevor IMAPISession::Unadvise](imapisession-unadvise.md) zum Abbrechen der Registrierung aufgerufen wurde, geben Sie Ihr Advise Sink-Objekt frei, es sei denn, Sie haben eine bestimmte langfristige Verwendung dafür. 
  
Eine Übersicht über den Benachrichtigungsprozess finden Sie unter [Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md). 
  
Weitere Informationen zum Behandeln von Benachrichtigungen finden Sie unter [Handling Notifications](handling-notifications.md). 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|BaseDialog.cpp  <br/> |CBaseDialog::OnNotificationsOn  <br/> |MFCMAPI verwendet die **IMAPISession::Advise-Methode, um** sich für Benachrichtigungen für die Sitzung zu registrieren.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IABLogon::Advise](iablogon-advise.md)
  
[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPISession::Unadvise](imapisession-unadvise.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md)

