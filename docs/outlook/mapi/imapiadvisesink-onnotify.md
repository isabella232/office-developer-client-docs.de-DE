---
title: IMAPIAdviseSinkOnNotify
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIAdviseSink.OnNotify
api_type:
- COM
ms.assetid: 9eec90d3-2369-4340-86ed-0efa58918ed5
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 73eb92b0c1b88e114775231695b91157a3d26a2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792058"
---
# <a name="imapiadvisesinkonnotify"></a>IMAPIAdviseSink::OnNotify

  
  
**Betrifft**: Outlook 
  
Antwortet auf eine Benachrichtigung durch eine oder mehrere Aufgaben ausführen. Die Aufgaben ausgeführt, abhängig von den Typ des Ereignisses und das Objekt, das die Benachrichtigung generiert. 
  
```cpp
ULONG OnNotify(
  ULONG cNotif,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a>Parameter

 _cNotif_
  
> [in] Die Anzahl der [Benachrichtigung](notification.md) Strukturen auf den durch den Parameter _LpNotifications_ verwiesen. 
    
 _lpNotifications_
  
> [in] Ein Zeiger auf eine oder mehrere **Benachrichtigung** -Strukturen, die Informationen zu den Ereignissen bereitstellen, die aufgetreten sind. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Benachrichtigung wurde erfolgreich verarbeitet.
    
## <a name="remarks"></a>Bemerkungen

Der Benachrichtigungsprozess beginnt, wenn ein Client oder MAPI **Advise** -Methode des Dienstanbieters registrieren, um eine Benachrichtigung eines bestimmten Typs für ein bestimmtes Objekt aufruft. Einer der Parameter der **Advise** -Methode ist ein Zeiger auf ein Objekt der Advise-Empfänger, die die [IMAPIAdviseSink](imapiadvisesinkiunknown.md) -Schnittstelle implementiert wird. Bei Auftreten eines Ereignisses auf dem Zielobjekt, das die registrierten Benachrichtigung, den Dienstanbieter entweder direkt oder indirekt über MAPI, entspricht, wird der Advise-Empfänger **OnNotify** -Methode aufgerufen. 
  
Der Aufruf von **OnNotify** kann auftreten, während der MAPI-Aufruf, der das Ereignis verursacht oder zu einem späteren Zeitpunkt. Auf Systemen, die mehreren Threads der Ausführung zu unterstützen, kann die **OnNotify** auf dem gleichen Thread, der für die Registrierung verwendet wurde oder in einem anderen Thread aufgerufen werden. Clients können sicherstellen, dass die **OnNotify** , auf dem gleichen Thread, der zum Aufrufen der **Advise aufgerufen wird** durch Erstellen von der Advise-Empfänger, den sie mit der Funktion [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) an **Advise** übergeben verwendet. 
  
Der Parameter _LpNotifications_ verweist auf ein oder mehrere **Benachrichtigung** Strukturen, die beschreiben, was während des Ereignisses geändert hat. Es ist eine andere Art von **Benachrichtigung** Struktur für jeden Typ von Ereignis. 
  
Die folgende Tabelle enthält die Werte, die zur Darstellung der möglichen Types von Ereignissen und die Verbindung mit jedem Wert Strukturen verwendet werden:
  
|**Benachrichtigungstyp-Ereignis**|**Entsprechende Struktur**|
|:-----|:-----|
|**fnevCriticalError** <br/> |[ERROR_NOTIFICATION](error_notification.md) <br/> |
|**fnevNewMail** <br/> |[NEWMAIL_NOTIFICATION](newmail_notification.md) <br/> |
|**fnevObjectCreated** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectDeleted** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectModified** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectCopied** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevSearchComplete** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevTableModified** <br/> |[TABLE_NOTIFICATION](table_notification.md) <br/> |
|**fnevStatusObjectModified** <br/> |[STATUS_OBJECT_NOTIFICATION](status_object_notification.md) <br/> |
|**fnevExtended** <br/> |[EXTENDED_NOTIFICATION](extended_notification.md) <br/> |
   
Weitere Informationen zum Einrichten und Beenden von Benachrichtigungen finden Sie unter Referenz Einträge für die **Advise** und **Unadvise** Methoden aus einem der folgenden Schnittstellen: [IABLogon](iablogoniunknown.md), [IAddrBook](iaddrbookimapiprop.md), [IMAPIForm](imapiformiunknown.md), [ IMAPISession](imapisessioniunknown.md), [IMAPITable](imapitableiunknown.md), [IMsgStore](imsgstoreimapiprop.md)und [IMSLogon](imslogoniunknown.md). 
  
Allgemeine Informationen zu den Benachrichtigungsprozess finden Sie unter [Event Notification in MAPI](event-notification-in-mapi.md). 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Die Implementierung **OnNotify** wird in der Regel eine oder mehrere Codeblöcke für jede Art von Benachrichtigung bestehen, den Sie erwarten. Führen Sie in diese Codeblöcke alle Aufgaben, die Sie als Antwort auf die Benachrichtigung erforderlichen berücksichtigen. Angenommen Sie, dass Sie registrieren Erhalt von Benachrichtigungen der **FnevObjectModified** für einen Ordner, die in einem Dialogfeld Feld enthalten ist. In den Block mit Code, die Sie in Ihre **OnNotify** -Methode zum Behandeln von Benachrichtigungen **FnevObjectModified** enthalten sind können Sie eine Windows-Nachricht an das Dialogfeld zum Anfordern einer aktualisierten Anzeige senden. 
  
Nicht ändern oder die **Benachrichtigung** Struktur übergeben **OnNotify**frei. Die Daten in der Struktur ist gültig, nur bis **OnNotify** zurückgegeben. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Beim Auftreten von Änderungen auf mehrere Objekte können Sie eine registrierten Advise-Empfänger in einem einzigen Aufruf von **OnNotify** oder mehrere Anrufe je nach Speicherkapazität benachrichtigt wird. Dies gilt unabhängig davon, ob die Änderungen das Ergebnis der Methodenaufruf eine oder mehrere sind. Beispielsweise kann ein Aufruf von [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) mehrere Nachrichten und Ordnern auswirken. Als einen Anbieter für Nachricht anmelden können Sie durch Aufrufen von **OnNotify** für den Zielordner oder viele Anrufe, eine für die einzelnen Nachrichten einen Einfluss darauf zu einem Ereignistyp **FnevObjectModified** machen. Auf ähnliche Weise, wenn ein Client wiederholte Aufrufe [IMAPIFolder::CreateMessage](imapifolder-createmessage.md), diesen anrufen oder werden können kombiniert ein **FnevObjectModified** -Ereignis für den Ordner in einzelne **FnevObjectCreated** Ereignisse für jede neue Nachricht getrennt. 
  
Weitere Informationen dazu, wie und wann Benachrichtigungen generiert finden Sie unter [Benachrichtigung in MAPI](event-notification-in-mapi.md) und [Ereignisbenachrichtigung unterstützen](supporting-event-notification.md). 
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|AdviseSink.h und AdviseSink.cpp  <br/> |CAdviseSink::OnNotifyDesc  <br/> |Zum Behandeln von alle Benachrichtigungen in MFCMAPI (engl.), wird die CAdviseSink-Klasse implementiert.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[HrAllocAdviseSink](hrallocadvisesink.md)
  
[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPISupport::Notify](imapisupport-notify.md)
  
[Benachrichtigung](notification.md)
  
[IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

