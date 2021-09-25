---
title: IMAPISessionAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISession.Advise
api_type:
- COM
ms.assetid: a6a6b6b1-31e2-4899-a5fe-74d5d1c2ccfc
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 617ff6a5486709691bc5b0283cb01825739e14cd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592451"
---
# <a name="imapisessionadvise"></a>IMAPISession::Advise

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Registriert sich, um Benachrichtigungen über angegebene Ereignisse zu erhalten, die sich auf die Sitzung auswirken.
  
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
  
> [in] Ein Zeiger auf den Eintragsbezeichner des Adressbuch- oder Nachrichtenspeicherobjekts, über das Benachrichtigungen generiert werden sollen, oder NULL, der angibt, dass der Client sich registriert, um Benachrichtigungen über Ereignisse zu empfangen, die sich nur auf die Sitzung auswirken. 
    
 _ulEventMask_
  
> [in] Eine Maske mit Werten, die die Typen von Benachrichtigungsereignissen angibt, an denen der Client interessiert ist, und die in die Registrierung einbezogen werden sollten. Wenn  _lpEntryID_ NULL ist, registriert MAPI den Client automatisch für kritische Fehlerereignisse, die sich nur auf die Sitzung auswirken. Wenn  _lpEntryID_ auf einen Eintragsbezeichner zeigt, sind die folgenden Werte für den  _ulEventMask-Parameter_ gültig: 
    
fnevCriticalError 
  
> Registriert Benachrichtigungen zu schwerwiegenden Fehlern, z. B. zu wenig Arbeitsspeicher.
    
fnevExtended 
  
> Registriert Benachrichtigungen zu Ereignissen, die für ein bestimmtes Adressbuch oder einen bestimmten Nachrichtenspeicheranbieter spezifisch sind, und zum Herunterfahren der Sitzung.
    
fnevNewMail 
  
> Registriert sich für Benachrichtigungen über das Eintreffen neuer Nachrichten. 
    
fnevObjectCreated 
  
> Registriert Benachrichtigungen über die Erstellung eines neuen Objekts.
    
fnevObjectCopied
  
> Registriert Benachrichtigungen über ein objekt, das kopiert wird.
    
fnevObjectDeleted
  
> Registriert Benachrichtigungen über ein objekt, das gelöscht wird.
    
fnevObjectModified
  
> Registriert Benachrichtigungen über ein Objekt, das geändert wird.
    
fnevObjectMoved
  
> Registriert Benachrichtigungen über ein Objekt, das verschoben wird.
    
fnevSearchComplete
  
> Registriert Benachrichtigungen über den Abschluss eines Suchvorgangs.
    
 _lpAdviseSink_
  
> [in] Ein Zeiger auf ein Empfehlungs-Senkenobjekt, um die nachfolgenden Benachrichtigungen zu erhalten. Dieses Empfehlungssenkenobjekt muss bereits zugeordnet worden sein.
    
 _lpulConnection_
  
> [out] Ein Zeiger auf eine Zahl ungleich Null, die die Verbindung zwischen dem "Advise Sink"-Objekt des Aufrufers und der Sitzung darstellt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Registrierung war erfolgreich.
    
MAPI_E_INVALID_ENTRYID 
  
> Der Eintragsbezeichner, auf den von  _lpEntryID_ verwiesen wird, stellt keinen gültigen Eintragsbezeichner dar. 
    
MAPI_E_NO_SUPPORT 
  
> Der Dienstanbieter, der für den Eintragsbezeichner verantwortlich ist, auf den  _lpEntryID_ verweist, unterstützt entweder nicht den im  _ulEventMask-Parameter_ angegebenen Ereignistyp oder keine Benachrichtigung. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Der Eintragsbezeichner, auf den  _lpEntryID_ verweist, kann von keinem der Dienstanbieter im Profil verarbeitet werden. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPISession::Advise-Methode** stellt eine Verbindung zwischen dem "advise"-Senkenobjekt des Aufrufers, der Sitzung und optional einem Dienstanbieter her. Diese Verbindung wird verwendet, um Benachrichtigungen an die Empfehlungssenke zu senden, wenn mindestens ein im  _ulEventMask_ -Parameter angegebenes Ereignis auf das Objekt eintritt, auf das von  _lpEntryID_ verwiesen wird. Wenn  _lpEntryID_ NULL ist, ist das Zielobjekt die Sitzung, und Benachrichtigungen werden nur für kritische Fehler und erweiterte Ereignisse gesendet. 
  
Wenn  _lpEntryID_ auf einen gültigen Eintragsbezeichner zeigt, ruft MAPI die **Advise-Methode** des Anmeldeobjekts auf, das zum verantwortlichen Dienstanbieter gehört. Wenn  _lpEntryID_ beispielsweise auf den Eintragsbezeichner einer Verteilerliste zeigt, ruft MAPI die [IABLogon::Advise-Methode](iablogon-advise.md) des entsprechenden Adressbuchanbieters auf. 
  
Zum Senden einer Benachrichtigung ruft der Dienstanbieter oder die MAPI die [IMAPIAdviseSink::OnNotify-Methode](imapiadvisesink-onnotify.md) der registrierten Empfehlungssenke auf. Einer der Parameter für **OnNotify**, eine Benachrichtigungsstruktur, enthält Informationen, die das spezifische Ereignis beschreiben.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Auf Systemen, die mehrere Ausführungsthreads unterstützen, kann der Aufruf von **OnNotify** auch jederzeit in jedem Thread erfolgen. Wenn Sie sicher sein müssen, dass Benachrichtigungen nur zu einem bestimmten Zeitpunkt in einem bestimmten Thread auftreten, rufen Sie die [HrThisThreadAdviseSink-Funktion](hrthisthreadadvisesink.md) auf, um das Advise-Senkenobjekt zu generieren, das Sie an die **Advise-Methode** übergeben. 
  
Um zu ermitteln, wann sich ein Client abgemeldet hat, registrieren Sie sich für Benachrichtigungen in Ihrem Dienstanbieter, indem **Sie "Advise"** aufrufen, wobei  _lpEntryID_ auf NULL und  _cbEntryID_ auf 0 festgelegt ist. Wenn die Abmeldung erfolgt, erhalten Sie eine fnevExtended-Benachrichtigung. 
  
Nachdem ein Aufruf von **"Advise"** erfolgreich war und bevor [IMAPISession::Unadvise](imapisession-unadvise.md) aufgerufen wurde, um die Registrierung abzubrechen, geben Sie Ihr Empfehlungssenkenobjekt frei, es sei denn, Sie haben eine bestimmte langfristige Verwendung dafür. 
  
Eine Übersicht über den Benachrichtigungsprozess finden Sie unter [Ereignisbenachrichtigung in MAPI.](event-notification-in-mapi.md) 
  
Weitere Informationen zum Behandeln von Benachrichtigungen finden Sie unter ["Behandeln von Benachrichtigungen".](handling-notifications.md) 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|BaseDialog.cpp  <br/> |CBaseDialog::OnNotificationsOn  <br/> |MFCMAPI verwendet die **IMAPISession::Advise-Methode,** um sich für Benachrichtigungen für die Sitzung zu registrieren.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IABLogon::Advise](iablogon-advise.md)
  
[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPISession::Unadvise](imapisession-unadvise.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md)

