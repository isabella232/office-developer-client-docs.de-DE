---
title: IMAPITableUnadvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.Unadvise
api_type:
- COM
ms.assetid: 19f0dad9-9704-4bbe-a689-9531e7198351
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: da11f15dfe9d269b79f465f01f713de401584962
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430231"
---
# <a name="imapitableunadvise"></a>IMAPITable::Unadvise

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bricht das Senden von Benachrichtigungen ab, die zuvor mit einem Aufruf der [IMAPITable::Advise-Methode eingerichtet](imapitable-advise.md) wurden. 
  
```cpp
HRESULT Unadvise(
ULONG_PTR ulConnection
);
```

## <a name="parameters"></a>Parameter

 _ulConnection_
  
> [in] Die Nummer der Registrierungsverbindung, die von einem Aufruf von [IMAPITable::Advise zurückgegeben wird.](imapitable-advise.md)
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf war erfolgreich.
    
## <a name="remarks"></a>Hinweise

Verwenden Sie die **IMAPITable::Unadvise-Methode,** um den Zeiger auf das im  _lpAdviseSink-Parameter im_ vorherigen Aufruf von **IMAPITable::Advise** übergebene Advise-Sink-Objekt frei zu geben, wodurch eine Benachrichtigungsregistrierung abgebrochen wird. Im Rahmen des Verwerfens des Zeigers auf das advise-Sink-Objekt wird die **IUnknown::Release-Methode des** Objekts aufgerufen. Im Allgemeinen wird **Release** während des **Unadvise-Aufrufs** aufgerufen, aber wenn ein anderer Thread die [IMAPIAdviseSink::OnNotify-Methode](imapiadvisesink-onnotify.md) für die Ratensenke aufruft, wird der Release-Aufruf verzögert, bis die **OnNotify-Methode** zurückgegeben wird.  
  
Weitere Informationen zum Benachrichtigungsprozess finden Sie unter [Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md). Spezifische Informationen zur Tabellenbenachrichtigung finden Sie unter [Informationen zu Tabellenbenachrichtigungen](about-table-notifications.md). Informationen zur Verwendung der **IMAPISupport-Methoden** zur Unterstützung von Benachrichtigungen finden Sie unter [Supporting Event Notification](supporting-event-notification.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::NotificationOff  <br/> |MFCMAPI verwendet die **IMAPITable::Unadvise-Methode,** um Benachrichtigungen für die Tabelle abbricht.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPITable::Advise](imapitable-advise.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

