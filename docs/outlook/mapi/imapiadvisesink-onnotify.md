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
  
Antwortet auf eine Benachrichtigung, indem mindestens eine Aufgabe ausgeführt wird. Die ausgeführten Aufgaben hängen vom Typ des Ereignisses und dem Objekt ab, das die Benachrichtigung generiert. 
  
```cpp
ULONG OnNotify(
  ULONG cNotif,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a>Parameter

 _cNotif_
  
> [in] Die Anzahl der [NOTIFICATION-Strukturen,](notification.md) auf die der  _lpNotifications-Parameter_ verweist. 
    
 _lpNotifications_
  
> [in] Ein Zeiger auf eine oder mehrere **NOTIFICATION-Strukturen,** die Informationen zu den aufgetretenen Ereignissen bereitstellen. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Benachrichtigung wurde erfolgreich verarbeitet.
    
## <a name="remarks"></a>Hinweise

Der Benachrichtigungsprozess beginnt, wenn ein Client oder eine MAPI die **Advise-Methode** eines Dienstanbieters aufruft, um sich zu registrieren, um eine Benachrichtigung eines bestimmten Typs für ein bestimmtes Objekt zu erhalten. Einer der Parameter für die **Advise-Methode** ist ein Zeiger auf ein Advise Sink-Objekt, das die [IMAPIAdviseSink-Schnittstelle](imapiadvisesinkiunknown.md) implementiert. Wenn ein Ereignis für das Zielobjekt auftritt, das der registrierten Benachrichtigung entspricht, ruft der Dienstanbieter entweder direkt oder indirekt über MAPI die **OnNotify-Methode** der Hinweissenke auf. 
  
Der Aufruf von **OnNotify** kann entweder während des MAPI-Aufrufs erfolgen, der das Ereignis verursacht, oder zu einem späteren Zeitpunkt. Auf Systemen, die mehrere Ausführungsthreads unterstützen, kann **OnNotify** entweder im selben Thread aufgerufen werden, der für die Registrierung verwendet wurde, oder in einem anderen Thread. Clients können sicherstellen, dass der **OnNotify-Aufruf** im selben Thread ausgeführt wird, der zum Aufrufen von **Advise** verwendet wird, indem sie die Ratensenke erstellen, die sie mit der [HrThisThreadAdviseSink-Funktion](hrthisthreadadvisesink.md) an **Advise** übergeben. 
  
Der  _lpNotifications-Parameter_ verweist auf eine oder mehrere **NOTIFICATION-Strukturen,** die beschreiben, was sich während des Ereignisses geändert hat. Es gibt einen anderen Typ von **NOTIFICATION-Struktur** für jeden Ereignistyp. 
  
In der folgenden Tabelle sind die Werte aufgeführt, die zum Darstellen der möglichen Ereignistypen und der strukturen verwendet werden, die den einzelnen Werten zugeordnet sind:
  
|**Benachrichtigungsereignistyp**|**Entsprechende Struktur**|
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
   
Weitere Informationen zum Einrichten und Beenden von Benachrichtigungen finden Sie in den Referenzeinträgen für die **Methoden Advise** und **Unadvise** für eine der folgenden Schnittstellen: [IABLogon](iablogoniunknown.md), [IAddrBook](iaddrbookimapiprop.md), [IMAPIForm](imapiformiunknown.md), [IMAPISession](imapisessioniunknown.md), [IMAPITable](imapitableiunknown.md), [IMsgStore](imsgstoreimapiprop.md)und [IMSLogon](imslogoniunknown.md). 
  
Allgemeine Informationen zum Benachrichtigungsprozess finden Sie unter [Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md). 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Ihre **OnNotify-Implementierung** besteht in der Regel aus einem oder mehreren Codeblöcken für jeden Benachrichtigungstyp, den Sie erwarten. Führen Sie in diesen Codeblöcken alle Aufgaben aus, die Sie als Reaktion auf die Benachrichtigung für erforderlich halten. Angenommen, Sie registrieren sich für den Empfang **von fnevObjectModified-Benachrichtigungen** in einem Ordner, der in einer Dialogfeldanzeige enthalten ist. Im Codeblock, den Sie in Ihre **OnNotify-Methode** zum Behandeln von **fnevObjectModified-Benachrichtigungen** verwenden, senden Sie möglicherweise eine Windows-Nachricht an das Dialogfeld, um eine aktualisierte Anzeige an fordern. 
  
Ändern oder geben Sie die an OnNotify übergebene **NOTIFICATION-Struktur nicht frei.**  Die Daten in der Struktur sind nur gültig, bis **OnNotify zurückgegeben** wird. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn Änderungen an mehreren Objekten vorgenommen werden, können Sie eine registrierte Ratensenke in einem einzigen Aufruf von **OnNotify** oder in mehreren Aufrufen in Abhängigkeit von Speichereinschränkungen benachrichtigen. Dies gilt unabhängig davon, ob die Änderungen das Ergebnis eines oder mehrerer Methodenaufrufe sind. Ein Aufruf von [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) kann sich beispielsweise auf mehrere Nachrichten und Ordner auswirken. Als Nachrichtenspeicheranbieter können Sie einen Aufruf von **OnNotify** mit einem **fnevObjectModified-Ereignistyp** für den Zielordner oder viele Aufrufe, einen für jede Auswirkung auf Nachrichten, erstellen. Wenn ein Client wiederholt [ImAPIFolder::CreateMessage](imapifolder-createmessage.md)aufruft, können diese Aufrufe in einem **fnevObjectModified-Ereignis** für den Ordner kombiniert oder in einzelne **fnevObjectCreated-Ereignisse** für jede neue Nachricht getrennt werden. 
  
Weitere Informationen dazu, wie und wann Benachrichtigungen generiert werden, finden Sie unter [Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md) und [Unterstützende Ereignisbenachrichtigung](supporting-event-notification.md). 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|AdviseSink.h und AdviseSink.cpp  <br/> |CAdviseSink::OnNotifyDesc  <br/> |Die CAdviseSink-Klasse ist implementiert, um alle Benachrichtigungen in MFCMAPI zu behandeln.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[HrAllocAdviseSink](hrallocadvisesink.md)
  
[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPISupport::Notify](imapisupport-notify.md)
  
[Benachrichtigung](notification.md)
  
[IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

