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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5983ed3229f6b0053f15a614116cf5680e942587
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407361"
---
# <a name="imapiadvisesinkonnotify"></a>IMAPIAdviseSink::OnNotify

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Reagiert auf eine Benachrichtigung, indem eine oder mehrere Aufgaben ausgeführt werden. Die ausgeführten Aufgaben hängen vom Ereignistyp und dem Objekt ab, das die Benachrichtigung generiert. 
  
```cpp
ULONG OnNotify(
  ULONG cNotif,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a>Parameter

 _cNotif_
  
> in Die Anzahl der [Benachrichtigungs](notification.md) Strukturen, auf die durch den _lpNotifications_ -Parameter verwiesen wird. 
    
 _lpNotifications_
  
> in Ein Zeiger auf eine oder mehrere **Benachrichtigungs** Strukturen, die Informationen zu den aufgetretenen Ereignissen bereitstellen. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Benachrichtigung wurde erfolgreich verarbeitet.
    
## <a name="remarks"></a>Bemerkungen

Der Benachrichtigungsprozess wird gestartet, wenn ein Client oder eine MAPI einen Anruf an die **Advise** -Methode eines Dienstanbieters durchführt, um sich für ein bestimmtes Objekt für eine Benachrichtigung eines bestimmten Typs zu registrieren. Einer der Parameter für die **Advise** -Methode ist ein Zeiger auf ein Advise-Objekt, das die [IMAPIAdviseSink](imapiadvisesinkiunknown.md) -Schnittstelle implementiert. Wenn ein Ereignis für das Zielobjekt auftritt, das der registrierten Benachrichtigung entspricht, ruft der Dienstanbieter, entweder direkt oder indirekt über MAPI, die onNotify- **** Methode der Advise-Senke auf. 
  
Der Aufruf von **OnNotify** kann entweder während des MAPI-Aufrufs auftreten, der das Ereignis verursacht, oder zu einem späteren Zeitpunkt. Auf Systemen, die mehrere Threads der Ausführung unter **** stützen, kann OnNotify entweder im gleichen Thread aufgerufen werden, der für die Registrierung oder in einem anderen Thread verwendet wurde. Clients können sicherstellen, dass **** der OnNotify-Aufruf über den gleichen Thread erfolgt, der zum Aufrufen von **Advise** verwendet wird, indem die Advise-Senke erstellt wird, die Sie an **Advise** mit der [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) -Funktion weiterleiten. 
  
Der _lpNotifications_ -Parameter verweist auf eine oder **** mehrere Benachrichtigungs Strukturen, die beschreiben, was während des Ereignisses geändert wurde. Es gibt eine andere Art von **Benachrichtigungs** Struktur für jede Art von Ereignis. 
  
In der folgenden Tabelle sind die Werte aufgeführt, die verwendet werden, um die möglichen Ereignistypen und die jedem Wert zugeordneten Strukturen darzustellen:
  
|**Benachrichtigungs Ereignistyp**|**Entsprechende Struktur**|
|:-----|:-----|
|**fnevCriticalError** <br/> |[ERROR_NOTIFICATION](error_notification.md) <br/> |
|**Uleventmaskfnevnewmail** <br/> |[NEWMAIL_NOTIFICATION](newmail_notification.md) <br/> |
|**fnevObjectCreated** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectDeleted** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectModified** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectCopied** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevSearchComplete** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevTableModified** <br/> |[TABLE_NOTIFICATION](table_notification.md) <br/> |
|**fnevStatusObjectModified** <br/> |[STATUS_OBJECT_NOTIFICATION](status_object_notification.md) <br/> |
|**fnevExtended** <br/> |[EXTENDED_NOTIFICATION](extended_notification.md) <br/> |
   
Weitere Informationen zum Einrichten und Beenden von Benachrichtigungen finden Sie in den Referenz Einträgen für die Methoden **Advise** und **Unadvise** für die folgenden Schnittstellen: [IABLogon](iablogoniunknown.md), [IAddrBook](iaddrbookimapiprop.md), [IMAPIForm](imapiformiunknown.md), [ IMAPISession](imapisessioniunknown.md), [IMAPITable](imapitableiunknown.md), [IMsgStore](imsgstoreimapiprop.md)und [IMSLogon](imslogoniunknown.md). 
  
Allgemeine Informationen zum Benachrichtigungsprozess finden Sie unter [Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md). 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Ihre **OnNotify** -Implementierung besteht in der Regel aus einem oder mehreren Codeblöcken für jeden Benachrichtigungstyp, den Sie erwarten. Führen Sie innerhalb dieser Codeblöcke alle Aufgaben aus, die Sie als Antwort auf die Benachrichtigung als erforderlich betrachten. Angenommen, Sie registrieren, um **fnevObjectModified** -Benachrichtigungen für einen Ordner zu erhalten, der in einer Dialogfeldanzeige enthalten ist. In dem Codeblock, den Sie in Ihre **OnNotify** -Methode aufnehmen, um **fnevObjectModified** -Benachrichtigungen zu behandeln, können Sie eine Windows-Meldung an das Dialogfeld senden, um eine aktualisierte Anzeige anzufordern. 
  
Ändern oder freigeben Sie die **Benachrichtigungs** Struktur, die an OnNotify übergeben wurde, nicht. **** Die Daten in der Struktur sind nur gültig, **** wenn OnNotify zurückgegeben wird. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn Änderungen an mehreren Objekten auftreten, können Sie eine registrierte Advise-Senke in einem einzelnen Aufruf **** von OnNotify oder in mehreren anrufen abhängig von Arbeitsspeichereinschränkungen benachrichtigen. Dies gilt unabhängig davon, ob die Änderungen das Ergebnis eines Methodenaufrufs oder mehrere sind. Beispielsweise kann ein Aufruf von [IMAPIFolder:: CopyMessages](imapifolder-copymessages.md) mehrere Nachrichten und Ordner betreffen. Als Nachrichtenspeicher Anbieter können Sie einen Aufruf von onNotify mit **** einem **fnevObjectModified** -Ereignistyp für den Zielordner oder zahlreiche Aufrufe durchführen, und zwar einen für jeden Nachrichten Affekt. Wenn ein Client wiederholt [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md)aufruft, können diese Aufrufe in einem **fnevObjectModified** -Ereignis für den Ordner kombiniert oder für jede neue Nachricht in einzelne **fnevObjectCreated** -Ereignisse aufgeteilt werden. 
  
Weitere Informationen dazu, wie und wann Benachrichtigungen generiert werden, finden Sie unter [Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md) und [unterstützende Ereignisbenachrichtigung](supporting-event-notification.md). 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|AdviseSink. h und AdviseSink. cpp  <br/> |CAdviseSink:: OnNotifyDesc  <br/> |Die CAdviseSink-Klasse wird implementiert, um alle Benachrichtigungen in MFCMAPI zu behandeln.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[HrAllocAdviseSink](hrallocadvisesink.md)
  
[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPISupport::Notify](imapisupport-notify.md)
  
[Benachrichtigung](notification.md)
  
[IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

