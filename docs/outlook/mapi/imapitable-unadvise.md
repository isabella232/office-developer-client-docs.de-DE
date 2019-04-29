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
  
Bricht das Senden von Benachrichtigungen ab, die zuvor mit einem Aufruf der [IMAPITable:: Advise](imapitable-advise.md) -Methode eingerichtet wurden. 
  
```cpp
HRESULT Unadvise(
ULONG_PTR ulConnection
);
```

## <a name="parameters"></a>Parameter

 _ulConnection_
  
> in Die Nummer der Registrierungs Verbindung, die von einem Aufruf von [IMAPITable:: Advise](imapitable-advise.md)zurückgegeben wird.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf war erfolgreich.
    
## <a name="remarks"></a>Bemerkungen

Verwenden Sie die **IMAPITable:: Unadvise** -Methode, um den Zeiger auf das Advise-Senke-Objekt, das im _lpAdviseSink_ -Parameter im vorherigen Aufruf von **IMAPITable:: Advise**übergeben wird, aufzuheben, wodurch eine Benachrichtigungs Registrierung abgebrochen wird. Als Teil des Verwerfens des Zeigers auf das Advise-Senke-Objekt wird die **IUnknown:: Release** -Methode des Objekts aufgerufen. Im Allgemeinen wird **Release** während des Unadvise-Aufrufs aufgerufen, aber wenn ein anderer Thread gerade **** die [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) -Methode für die Advise-Senke aufruft, wird der **Freigabe** Aufruf verzögert, bis die OnNotify **** Methode gibt zurück. 
  
Weitere Informationen zum Benachrichtigungsprozess finden Sie unter [Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md). Spezifische Informationen zur Tabellenbenachrichtigung finden Sie unter [Informationen zu Tabellen Benachrichtigungen](about-table-notifications.md). Informationen zur Verwendung der **IMAPISupport** -Methoden zur Unterstützung von Benachrichtigungen finden Sie unter [unterstützende Ereignisbenachrichtigung](supporting-event-notification.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|ContentsTableListCtrl. cpp  <br/> |CContentsTableListCtrl:: NotificationOff  <br/> |MFCMAPI verwendet die **IMAPITable:: Unadvise** -Methode, um Benachrichtigungen für die Tabelle abzubrechen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPITable::Advise](imapitable-advise.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

