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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: c9401c163c74ab303ec39c147e0432d1979426b8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329018"
---
# <a name="imapitableadvise"></a>IMAPITable::Advise

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Registriert ein Advise-Senke-Objekt, um Benachrichtigungen über angegebene Ereignisse zu erhalten, die sich auf die Tabelle auswirken.
  
```cpp
HRESULT Advise(
ULONG ulEventMask,
LPMAPIADVISESINK lpAdviseSink,
ULONG_PTR FAR * lpulConnection
);
```

## <a name="parameters"></a>Parameter

 _ulEventMask_
  
> in Wert, der den Typ des Ereignisses angibt, das die Benachrichtigung generiert. Nur der folgende Wert ist gültig:
    
 `fnevTableModified`
  
 _lpAdviseSink_
  
> in Zeiger auf ein Advise-Senke-Objekt, um die nachfolgenden Benachrichtigungen zu erhalten. Dieses Advise-Senke-Objekt muss bereits zugeordnet worden sein.
    
 _lpulConnection_
  
> Out Zeiger auf einen Wert ungleich NULL, der die erfolgreiche Benachrichtigungs Registrierung darstellt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Benachrichtigungs Registrierung wurde erfolgreich abgeschlossen.
    
MAPI_E_NO_SUPPORT 
  
> Die Tabellen Implementierung unterstützt keine Änderungen an den Zeilen und Spalten oder unterstützt keine Benachrichtigung.
    
## <a name="remarks"></a>Bemerkungen

Verwenden Sie die **IMAPITable:: Advise** -Methode, um ein Table-Objekt zu registrieren, das im Anbieter für Benachrichtigungsrückrufe implementiert ist. Wenn eine Änderung für das Table-Objekt auftritt, überprüft der Anbieter, welches Ereignis Masken Bit im Parameter _ulEventMask_ festgelegt wurde und welche Art von Änderung aufgetreten ist. Wenn ein Bit festgelegt ist, ruft der Anbieter die [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) -Methode für das vom _lpAdviseSink_ -Parameter angegebene Advise-Senke-Objekt auf, um das Ereignis zu melden. Die Daten, die in der Benachrichtigungs **** Struktur an die OnNotify-Routine übergeben werden, beschreiben das Ereignis. 
  
Der Aufruf von **OnNotify** kann während des Anrufs auftreten, der das Objekt ändert oder zu einem beliebigen Zeitpunkt. Auf Systemen, die mehrere Threads der Ausführung unterstützen, kann **** der Aufruf von OnNotify in jedem Thread auftreten. Damit ein Anruf an onNotify, der **** möglicherweise zu einem ungünstigen Zeitpunkt stattfindet, zu einem sicherer wird, der zu handhaben ist, sollte ein Anbieter die [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) -Funktion verwenden. 
  
Um Benachrichtigungen bereitzustellen, muss der Anbieter, der **Advise** implementiert, eine Kopie des Zeigers auf das _lpAdviseSink_ -Advise-Objekt beibehalten; Hierzu wird die **IUnknown:: AddRef** -Methode für die Advise-Senke aufgerufen, um den Objektzeiger zu warten, bis die Benachrichtigungs Registrierung mit einem Aufruf der [IMAPITable:: Unadvise](imapitable-unadvise.md) -Methode abgebrochen wird. Die **Advise** -Implementierung sollte der Benachrichtigungs Registrierung eine Verbindungsnummer zuweisen und **AddRef** für diese Verbindungsnummer aufrufen, bevor Sie im _lpulConnection_ -Parameter zurückgegeben wird. Dienstanbieter können das Advise-Senke-Objekt freigeben, bevor die Registrierung abgebrochen wird, aber Sie dürfen die Verbindungsnummer erst freigeben, wenn * * Unadvise * * aufgerufen wurde. 
  
Nachdem ein Anruf bei **Advise** erfolgreich war und bevor * * Unadvise * * aufgerufen wurde, müssen Clients für das Advise-Senke-Objekt freigegeben werden. Ein Client sollte daher sein Advise-Senke-Objekt freigeben, nachdem **Advise** zurückgegeben wird, es sei denn, er hat eine bestimmte langfristige Verwendung dafür. 
  
Aufgrund des asynchronen Verhaltens der Benachrichtigung können Implementierungen, die Tabellenspalten Einstellungen ändern, Benachrichtigungen mit Informationen erhalten, die in einer vorherigen Spaltenreihenfolge organisiert sind. Beispielsweise kann eine Tabellenzeile für eine Nachricht zurückgegeben werden, die soeben aus dem Container gelöscht wurde. Eine solche Benachrichtigung wird gesendet, wenn die Spalten Einstellung geändert wurde und Informationen über Sie gesendet wurden, aber die Benachrichtigungstabellen Ansicht noch nicht mit diesen Informationen aktualisiert wurde.
  
Weitere Informationen zum Benachrichtigungsprozess finden Sie unter [Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md). Spezifische Informationen zur Tabellenbenachrichtigung finden Sie unter [Informationen zu Tabellen Benachrichtigungen](about-table-notifications.md). Informationen zur Verwendung der **IMAPISupport** -Methoden zur Unterstützung von Benachrichtigungen finden Sie unter [unterstützende Ereignisbenachrichtigung](supporting-event-notification.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|ContentsTableListCtrl. cpp  <br/> |CContestTableListCtrl:: NotificationOn  <br/> |MFCMAPI verwendet die **IMAPITable:: Advise** -Methode, um Benachrichtigungen zu registrieren, damit die Tabellenansicht aktuell bleibt.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPITable::Unadvise](imapitable-unadvise.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

