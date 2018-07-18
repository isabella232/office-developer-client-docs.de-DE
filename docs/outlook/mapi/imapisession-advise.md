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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 45033ab924dcf443e9d231b3a7b4348119758935
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792315"
---
# <a name="imapisessionadvise"></a>IMAPISession::Advise

  
  
**Betrifft**: Outlook 
  
Um die Benachrichtigung der angegebenen Ereignisse, die Einfluss auf die Sitzung registriert.
  
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
  
> [in] Ein Zeiger auf die Eintrags-ID des Adressbuch oder Message Store-Objekts darüber, welche Benachrichtigungen generiert werden soll, oder NULL-Wert gibt an, dass der Client Erhalt von Benachrichtigungen zu Ereignissen, die nur die Sitzung betreffen registriert wird. 
    
 _ulEventMask_
  
> [in] Eine Maske von Werten, mit die die Typen von Benachrichtigungsereignisse anzugeben, die der Client ist daran interessiert, und in der Registrierung eingeschlossen sein soll. Wenn _LpEntryID_ NULL ist, registriert MAPI automatisch den Client für kritische Fehlerereignisse, die nur die Sitzung zu beeinflussen. Wenn _LpEntryID_ auf einen Eintrag Bezeichner verweist, sind die folgenden Werte für den Parameter _UlEventMask_ gültig: 
    
fnevCriticalError 
  
> Register für Benachrichtigungen zu schwerwiegenden Fehlern, beispielsweise nicht genügend Arbeitsspeicher.
    
fnevExtended 
  
> Register für Benachrichtigungen über Ereignisse, die speziell für ein bestimmtes Adressbuch oder einer Nachricht Speicheranbieter und zur Sitzung beendet.
    
fnevNewMail 
  
> Register für die Benachrichtigung über den Empfang von neuen Nachrichten. 
    
fnevObjectCreated 
  
> Register für die Benachrichtigung über die Erstellung eines neuen Objekts.
    
fnevObjectCopied
  
> Register für Benachrichtigungen zu einem Objekt kopiert wird.
    
fnevObjectDeleted
  
> Register für Benachrichtigungen zu einem Objekt, das gelöscht wird.
    
fnevObjectModified
  
> Register für Benachrichtigungen zu einem Objekt geändert wird.
    
fnevObjectMoved
  
> Register für Benachrichtigungen zu einem Objekt verschoben wird.
    
fnevSearchComplete
  
> Register für die Benachrichtigung über den Abschluss der Suchvorgang.
    
 _lpAdviseSink_
  
> [in] Ein Zeiger auf eine Advise-Empfängerobjekt nachfolgenden Benachrichtigungen zu empfangen. Diese Advise-Empfängerobjekt muss bereits zugewiesen wurden.
    
 _lpulConnection_
  
> [out] Ein Zeiger auf eine Zahl ungleich NULL für die Verbindung zwischen des Anrufers advise-Empfängerobjekt und der Sitzung.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Registrierung erfolgreich war.
    
MAPI_E_INVALID_ENTRYID 
  
> Die Eintrags-ID auf den _LpEntryID_ stellt keinen gültige Eingabe Bezeichner dar. 
    
MAPI_E_NO_SUPPORT 
  
> Der Dienstanbieter verantwortlich für die Eintrags-ID auf den _LpEntryID_ unterstützt nicht die Art der Ereignisse in der _UlEventMask_ -Parameter angegeben, oder unterstützt keine Benachrichtigung. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Die Eintrags-ID auf den _LpEntryID_ kann von jedem-Dienstanbieter im Profil behandelt werden. 
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISession::Advise** -Methode richtet eine Verbindung zwischen dem Anrufer der advise-Empfängerobjekt, die Sitzung und optional einem Dienstanbieter. Diese Verbindung wird verwendet, um das Senden von Benachrichtigungen an der Advise-Empfänger, wenn sich ein oder mehr Ereignisse in der _UlEventMask_ -Parameter angegebene auf das Objekt, auf das _LpEntryID_auftreten. Wenn _LpEntryID_ NULL ist, das Zielobjekt ist die Sitzung und Benachrichtigungen werden nur für schwerwiegende Fehler und erweiterte Ereignisse gesendet. 
  
Wenn _LpEntryID_ auf einen gültigen Eintrag Bezeichner verweist, ruft MAPI die **Advise** -Methode des Anmeldung-Objekts, das an den zuständigen Dienstanbieter gehört. Beispielsweise ruft _LpEntryID_ auf die Eintrags-ID einer Verteilerliste verweist, MAPI die entsprechenden-Adressbuchanbieter [IABLogon::Advise](iablogon-advise.md) -Methode. 
  
Um eine Benachrichtigung zu senden, Dienstanbieter oder MAPI der registrierten Advise-Empfänger [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) -Methode aufgerufen. Einer der Parameter zu **OnNotify**, eine Benachrichtigungsstruktur enthält Informationen des jeweiligen Ereignisses.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Auf Systemen, die mehreren Threads der Ausführung zu unterstützen, kann der Aufruf von **OnNotify** auch jederzeit auf einem beliebigen Thread auftreten. Wenn Sie Benachrichtigungen nur zu einem bestimmten Zeitpunkt in einem bestimmten Thread treten Assurance benötigen, rufen Sie die [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) -Funktion, um das Empfängerobjekt Advise generieren, das Sie an der **Advise** -Methode übergeben. 
  
Um zu bestimmen, wann ein Client abgemeldet, registrieren Sie sich für Benachrichtigungen in Ihren Dienstanbieter durch Aufrufen von **Advise** mit _LpEntryID_ festlegen auf NULL und _CbEntryID_ auf 0 festgelegt. Wenn die Abmeldung auftritt, erhalten Sie eine Benachrichtigung FnevExtended. 
  
Freigeben Sie nach ein Aufruf von **Advise** erfolgreich abgeschlossen wurde und bevor [IMAPISession::Unadvise](imapisession-unadvise.md) aufgerufen wurde, um die Registrierung abzubrechen, Ihrer Advise-Empfängerobjekt, es sei denn, Sie eine bestimmte langfristige Verwendung dafür haben. 
  
Eine Übersicht über den Benachrichtigungsprozess finden Sie unter [Event Notification in MAPI](event-notification-in-mapi.md). 
  
Weitere Informationen zum Behandeln von Benachrichtigungen finden Sie unter [Behandeln von Benachrichtigungen](handling-notifications.md). 
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|BaseDialog.cpp  <br/> |CBaseDialog::OnNotificationsOn  <br/> |MFCMAPI (engl.) verwendet die **IMAPISession::Advise** -Methode, um für Benachrichtigungen vor der Sitzung zu registrieren.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IABLogon::Advise](iablogon-advise.md)
  
[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPISession::Unadvise](imapisession-unadvise.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md)

