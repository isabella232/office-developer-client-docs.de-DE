---
title: IMAPITableAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPITable.Advise
api_type:
- COM
ms.assetid: e8b5d21e-dc14-4b61-96b3-a51bcfa0d232
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: aabcb60c16c2c7c5415c997d0f2fdbdf9d2f4dc1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620842"
---
# <a name="imapitableadvise"></a>IMAPITable::Advise

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Registriert ein "advise"-Senkenobjekt, um Benachrichtigungen über angegebene Ereignisse zu erhalten, die sich auf die Tabelle auswirken.
  
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
  
> [in] Zeiger auf ein Empfehlungssenkenobjekt, um die nachfolgenden Benachrichtigungen zu erhalten. Dieses Empfehlungssenkenobjekt muss bereits zugeordnet worden sein.
    
 _lpulConnection_
  
> [out] Zeiger auf einen Wert ungleich Null, der die erfolgreiche Benachrichtigungsregistrierung darstellt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Benachrichtigungsregistrierung wurde erfolgreich abgeschlossen.
    
MAPI_E_NO_SUPPORT 
  
> Die Tabellenimplementierungen unterstützen weder Änderungen an den Zeilen und Spalten noch Benachrichtigungen.
    
## <a name="remarks"></a>Bemerkungen

Verwenden Sie die **IMAPITable::Advise-Methode,** um ein tabellenobjekt zu registrieren, das im Anbieter für Benachrichtigungsrückrufe implementiert ist. Bei jeder Änderung des Tabellenobjekts überprüft der Anbieter, welches Ereignismaskenbit im  _ulEventMask-Parameter_ festgelegt wurde und welche Art von Änderung aufgetreten ist. Wenn ein Bit festgelegt ist, ruft der Anbieter die [IMAPIAdviseSink::OnNotify-Methode](imapiadvisesink-onnotify.md) für das vom  _lpAdviseSink-Parameter_ angegebene "advise"-Senkenobjekt auf, um das Ereignis zu melden. Daten, die in der Benachrichtigungsstruktur an die **OnNotify-Routine** übergeben werden, beschreiben das Ereignis. 
  
Der Aufruf von **OnNotify** kann während des Aufrufs erfolgen, durch den das Objekt geändert wird, oder zu einem beliebigen zeitpunkt. Auf Systemen, die mehrere Ausführungsthreads unterstützen, kann der Aufruf von **OnNotify** in jedem Thread erfolgen. Für eine Möglichkeit, einen Aufruf von **OnNotify,** der zu einem inopportintimen Zeitpunkt erfolgen kann, in einen aufruf zu machen, der sicherer zu verarbeiten ist, sollte ein Anbieter die [HrThisThreadAdviseSink-Funktion](hrthisthreadadvisesink.md) verwenden. 
  
Um Benachrichtigungen bereitzustellen, muss der Anbieter, der **"Advise"** implementiert, eine Kopie des Zeigers auf das  _lpAdviseSink-Empfehlungssenkenobjekt_ beibehalten. Dazu wird die **IUnknown::AddRef-Methode** für die Rate-Senken aufgerufen, um den Objektzeiger beizubehalten, bis die Benachrichtigungsregistrierung mit einem Aufruf der [IMAPITable::Unadvise-Methode](imapitable-unadvise.md) abgebrochen wird. Die **Advise-Implementierung** sollte der Benachrichtigungsregistrierung eine Verbindungsnummer zuweisen und **AddRef** für diese Verbindungsnummer aufrufen, bevor sie im  _lpulConnection-Parameter_ zurückgegeben wird. Dienstanbieter können das Empfehlungssenkenobjekt freigeben, bevor die Registrierung abgebrochen wird, aber sie dürfen die Verbindungsnummer erst freigeben, wenn ** Unadvise ** aufgerufen wurde. 
  
Nachdem ein Aufruf von **Advise** erfolgreich war und bevor ** Unadvise ** aufgerufen wurde, müssen Clients darauf vorbereitet sein, dass das Advise-Senkenobjekt freigegeben wird. Ein Client sollte daher sein Empfehlungssenkenobjekt freigeben, nachdem **Advise** zurückgegeben wurde, es sei denn, er hat eine bestimmte langfristige Verwendung. 
  
Aufgrund des asynchronen Verhaltens von Benachrichtigungen können Implementierungen, die Tabellenspalteneinstellungen ändern, Benachrichtigungen mit Informationen empfangen, die in einer vorherigen Spaltenreihenfolge organisiert sind. Beispielsweise kann eine Tabellenzeile für eine Nachricht zurückgegeben werden, die soeben aus dem Container gelöscht wurde. Eine solche Benachrichtigung wird gesendet, wenn die Spalteneinstellung geändert wurde und Informationen darüber gesendet wurden, die Benachrichtigungstabellenansicht jedoch noch nicht mit diesen Informationen aktualisiert wurde.
  
Weitere Informationen zum Benachrichtigungsprozess finden Sie unter [Ereignisbenachrichtigung in MAPI.](event-notification-in-mapi.md) Spezifische Informationen zur Tabellenbenachrichtigung finden Sie unter ["Informationen zu Tabellenbenachrichtigungen".](about-table-notifications.md) Informationen zur Verwendung der **IMAPISupport-Methoden** zur Unterstützung von Benachrichtigungen finden Sie unter ["Unterstützende Ereignisbenachrichtigung".](supporting-event-notification.md)
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContestTableListCtrl::NotificationOn  <br/> |MFCMAPI verwendet die **IMAPITable::Advise-Methode,** um Benachrichtigungen zu registrieren, damit die Tabellenansicht auf dem neuesten Stand bleibt.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPITable::Unadvise](imapitable-unadvise.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

