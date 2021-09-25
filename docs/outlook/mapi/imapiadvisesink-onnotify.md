---
title: IMAPIAdviseSinkOnNotify
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIAdviseSink.OnNotify
api_type:
- COM
ms.assetid: 9eec90d3-2369-4340-86ed-0efa58918ed5
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c05af1aa9ab38ed2501e2d3e65fe48f479128943
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616817"
---
# <a name="imapiadvisesinkonnotify"></a>IMAPIAdviseSink::OnNotify

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Antwortet auf eine Benachrichtigung, indem eine oder mehrere Aufgaben ausgeführt werden. Die ausgeführten Aufgaben hängen vom Ereignistyp und dem Objekt ab, das die Benachrichtigung generiert. 
  
```cpp
ULONG OnNotify(
  ULONG cNotif,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a>Parameter

 _cNotif_
  
> [in] Die Anzahl der [NOTIFICATION-Strukturen,](notification.md) auf die durch den  _LpNotifications-Parameter_ verwiesen wird. 
    
 _LpNotifications_
  
> [in] Ein Zeiger auf eine oder mehrere **NOTIFICATION-Strukturen,** die Informationen zu den aufgetretenen Ereignissen bereitstellen. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Benachrichtigung wurde erfolgreich verarbeitet.
    
## <a name="remarks"></a>Bemerkungen

Der Benachrichtigungsprozess beginnt, wenn ein Client oder eine MAPI die Advise-Methode eines Dienstanbieters **aufruft,** um eine Benachrichtigung eines bestimmten Typs für ein bestimmtes Objekt zu erhalten. Einer der Parameter für die **Advise-Methode** ist ein Zeiger auf ein Advise-Senkenobjekt, das die [IMAPIAdviseSink-Schnittstelle](imapiadvisesinkiunknown.md) implementiert. Wenn ein Ereignis für das Zielobjekt eintritt, das der registrierten Benachrichtigung entspricht, ruft der Dienstanbieter entweder direkt oder indirekt über die MAPI die **OnNotify-Methode** der Empfehlungssenke auf. 
  
Der Aufruf von **OnNotify** kann entweder während des MAPI-Aufrufs erfolgen, der das Ereignis verursacht, oder zu einem späteren Zeitpunkt. Auf Systemen, die mehrere Ausführungsthreads unterstützen, kann **OnNotify** entweder im gleichen Thread aufgerufen werden, der für die Registrierung verwendet wurde, oder in einem anderen Thread. Clients können sicherstellen, dass der **OnNotify-Aufruf** in dem Thread erfolgt, der zum Aufrufen von **"Advise"** verwendet wird, indem sie die Rate-Senken erstellen, die sie mit der [HrThisThreadAdviseSink-Funktion](hrthisthreadadvisesink.md) an **Advise** übergeben. 
  
Der  _lpNotifications-Parameter_ verweist auf eine oder mehrere **NOTIFICATION-Strukturen,** die beschreiben, was sich während des Ereignisses geändert hat. Es gibt einen anderen Typ von **NOTIFICATION-Struktur** für jeden Ereignistyp. 
  
In der folgenden Tabelle sind die Werte aufgeführt, die verwendet werden, um die möglichen Ereignistypen und die den einzelnen Werten zugeordneten Strukturen darzustellen:
  
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
   
Weitere Informationen zum Einrichten und Beenden von Benachrichtigungen finden Sie in den Referenzeinträgen für die Methoden **Advise** und **Unadvise** für eine der folgenden Schnittstellen: [IABLogon](iablogoniunknown.md), [IAddrBook](iaddrbookimapiprop.md), [IMAPIForm](imapiformiunknown.md), [IMAPISession](imapisessioniunknown.md), [IMAPITable](imapitableiunknown.md), [IMsgStore](imsgstoreimapiprop.md)und [IMSLogon](imslogoniunknown.md). 
  
Allgemeine Informationen zum Benachrichtigungsprozess finden Sie unter [Ereignisbenachrichtigung in MAPI.](event-notification-in-mapi.md) 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Ihre **OnNotify-Implementierung** besteht in der Regel aus einem oder mehreren Codeblöcken für jeden Benachrichtigungstyp, den Sie erwarten. Führen Sie in diesen Codeblöcken alle Aufgaben aus, die Sie als Reaktion auf die Benachrichtigung für erforderlich halten. Angenommen, Sie registrieren sich für den Empfang von **fnevObjectModified-Benachrichtigungen** für einen Ordner, der in einem Dialogfeld angezeigt wird. Im Codeblock, den Sie in ihre **OnNotify-Methode** zum Behandeln von **FnevObjectModified-Benachrichtigungen** einschließen, senden Sie möglicherweise eine Windows Nachricht an das Dialogfeld, um eine aktualisierte Anzeige anzufordern. 
  
Ändern oder freigeben Sie die an **OnNotify** übergebene **NOTIFICATION-Struktur** nicht. Die Daten in der Struktur sind nur gültig, bis **OnNotify** zurückgegeben wird. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn Änderungen an mehreren Objekten auftreten, können Sie eine registrierte Empfehlungssenke in einem einzigen Aufruf von **OnNotify** oder in mehreren Aufrufen abhängig von Speichereinschränkungen benachrichtigen. Dies gilt unabhängig davon, ob die Änderungen das Ergebnis eines oder mehrerer Methodenaufrufe sind. Ein Aufruf von [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) kann sich beispielsweise auf mehrere Nachrichten und Ordner auswirken. Als Nachrichtenspeicheranbieter können Sie einen Aufruf an **OnNotify** mit einem **fnevObjectModified-Ereignistyp** für den Zielordner oder viele Aufrufe durchführen, einen für jede Auswirkung auf Nachrichten. Wenn ein Client wiederholt Aufrufe von [IMAPIFolder::CreateMessage](imapifolder-createmessage.md)vornimmt, können diese Aufrufe in einem **fnevObjectModified-Ereignis** für den Ordner kombiniert oder in einzelne **fnevObjectCreated-Ereignisse** für jede neue Nachricht getrennt werden. 
  
Weitere Informationen dazu, wie und wann Benachrichtigungen generiert werden, finden Sie unter ["Ereignisbenachrichtigung" in MAPI](event-notification-in-mapi.md) und ["Unterstützende Ereignisbenachrichtigung".](supporting-event-notification.md) 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|AdviseSink.h und AdviseSink.cpp  <br/> |CAdviseSink::OnNotifyDesc  <br/> |Die CAdviseSink-Klasse wird implementiert, um alle Benachrichtigungen in MFCMAPI zu behandeln.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[HrAllocAdviseSink](hrallocadvisesink.md)
  
[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPISupport::Notify](imapisupport-notify.md)
  
[Benachrichtigung](notification.md)
  
[IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

