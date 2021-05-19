---
title: IMAPITableAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.Advise
api_type:
- COM
ms.assetid: e8b5d21e-dc14-4b61-96b3-a51bcfa0d232
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c9401c163c74ab303ec39c147e0432d1979426b8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418813"
---
# <a name="imapitableadvise"></a>IMAPITable::Advise

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Registriert ein Advise Sink-Objekt, um Benachrichtigungen über angegebene Ereignisse zu erhalten, die sich auf die Tabelle ausdingen.
  
```cpp
HRESULT Advise(
ULONG ulEventMask,
LPMAPIADVISESINK lpAdviseSink,
ULONG_PTR FAR * lpulConnection
);
```

## <a name="parameters"></a>Parameter

 _ulEventMask_
  
> [in] Wert, der den Typ des Ereignisses angibt, das die Benachrichtigung generiert. Nur der folgende Wert ist gültig:
    
 `fnevTableModified`
  
 _lpAdviseSink_
  
> [in] Zeiger auf ein Advise Sink-Objekt, um die nachfolgenden Benachrichtigungen zu erhalten. Dieses Ratensenkenobjekt muss bereits zugewiesen worden sein.
    
 _lpulConnection_
  
> [out] Zeiger auf einen Wert ungleich Null, der die erfolgreiche Benachrichtigungsregistrierung darstellt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Benachrichtigungsregistrierung wurde erfolgreich abgeschlossen.
    
MAPI_E_NO_SUPPORT 
  
> Die Tabellenimplementierung unterstützt entweder keine Änderungen an den Zeilen und Spalten oder keine Benachrichtigung.
    
## <a name="remarks"></a>Hinweise

Verwenden Sie die **IMAPITable::Advise-Methode,** um ein im Anbieter implementiertes Tabellenobjekt für Benachrichtigungsrückrufe zu registrieren. Wenn eine Änderung am Tabellenobjekt auftritt, überprüft der Anbieter, welches Ereignismaskenbit im  _ulEventMask-Parameter_ festgelegt wurde und welche Art von Änderung aufgetreten ist. Wenn ein Bit festgelegt ist, ruft der Anbieter die [IMAPIAdviseSink::OnNotify-Methode](imapiadvisesink-onnotify.md) auf, damit das durch den  _lpAdviseSink-Parameter_ angegebene Advise-Sink-Objekt das Ereignis melden kann. Daten, die in der Benachrichtigungsstruktur an die **OnNotify-Routine** übergeben werden, beschreiben das Ereignis. 
  
Der Aufruf von **OnNotify** kann während des Aufrufs erfolgen, der das Objekt ändert, oder zu einem beliebigen nachfolgenden Zeitpunkt. Auf Systemen, die mehrere Ausführungsthreads unterstützen, kann der Aufruf von **OnNotify** in jedem Thread erfolgen. Um einen Aufruf von **OnNotify,** der zu einem unvorstellbaren Zeitpunkt auftreten kann, in einen anruf zu verwandeln, der sicherer zu behandeln ist, sollte ein Anbieter die [HrThisThreadAdviseSink-Funktion](hrthisthreadadvisesink.md) verwenden. 
  
Zum Bereitstellen von Benachrichtigungen muss der Anbieter, der **Advise** implementieren, eine Kopie des Zeigers auf das  _lpAdviseSink-Ratgebersenkenobjekt_ behalten. Dazu ruft sie die **IUnknown::AddRef-Methode** auf, damit die Ratensenke ihren Objektzeiger beibehalten kann, bis die Benachrichtigungsregistrierung mit einem Aufruf der [IMAPITable::Unadvise-Methode](imapitable-unadvise.md) abgebrochen wird. Die **Advise-Implementierung** sollte der Benachrichtigungsregistrierung eine Verbindungsnummer zuweisen und **AddRef** für diese Verbindungsnummer aufrufen, bevor sie im  _lpulConnection-Parameter zurückgesenkt_ wird. Dienstanbieter können das Advise -Sink-Objekt vor dem Abbrechen der Registrierung los, aber sie dürfen die Verbindungsnummer erst los, wenn ** Unadvise ** aufgerufen wurde. 
  
Nachdem ein Aufruf von **Advise** erfolgreich war und bevor ** Unadvise ** aufgerufen wurde, müssen Clients darauf vorbereitet sein, dass das Advise Sink-Objekt freigegeben wird. Ein Client sollte daher sein Advise -Sink-Objekt veröffentlichen, nachdem **Advise** zurückgegeben wird, es sei denn, er hat eine bestimmte langfristige Verwendung dafür. 
  
Aufgrund des asynchronen Verhaltens von Benachrichtigungen können Implementierungen, die Tabellenspalteneinstellungen ändern, Benachrichtigungen mit Informationen empfangen, die in einer vorherigen Spaltenreihenfolge organisiert sind. Beispielsweise kann eine Tabellenzeile für eine Nachricht zurückgegeben werden, die gerade aus dem Container gelöscht wurde. Eine solche Benachrichtigung wird gesendet, wenn die Änderung der Spalteneinstellung vorgenommen wurde und Informationen darüber gesendet wurden, die Benachrichtigungstabelle jedoch noch nicht mit diesen Informationen aktualisiert wurde.
  
Weitere Informationen zum Benachrichtigungsprozess finden Sie unter [Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md). Spezifische Informationen zur Tabellenbenachrichtigung finden Sie unter [Informationen zu Tabellenbenachrichtigungen](about-table-notifications.md). Informationen zur Verwendung der **IMAPISupport-Methoden** zur Unterstützung von Benachrichtigungen finden Sie unter [Supporting Event Notification](supporting-event-notification.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContestTableListCtrl::NotificationOn  <br/> |MFCMAPI verwendet die **IMAPITable::Advise-Methode,** um sich für Benachrichtigungen zu registrieren, damit die Tabellenansicht auf dem aktuellen Stand bleibt.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPITable::Unadvise](imapitable-unadvise.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

