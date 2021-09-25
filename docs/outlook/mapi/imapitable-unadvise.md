---
title: IMAPITableUnadvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPITable.Unadvise
api_type:
- COM
ms.assetid: 19f0dad9-9704-4bbe-a689-9531e7198351
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 00d70472e5d93eb6a9caab60f444afda3a75b03d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575722"
---
# <a name="imapitableunadvise"></a>IMAPITable::Unadvise

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bricht das Senden von Benachrichtigungen ab, die zuvor mit einem Aufruf der [IMAPITable::Advise-Methode](imapitable-advise.md) eingerichtet wurden. 
  
```cpp
HRESULT Unadvise(
ULONG_PTR ulConnection
);
```

## <a name="parameters"></a>Parameter

 _ulConnection_
  
> [in] Die Nummer der Registrierungsverbindung, die von einem Aufruf von [IMAPITable::Advise](imapitable-advise.md)zurückgegeben wird.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf war erfolgreich.
    
## <a name="remarks"></a>HinwBemerkungeneise

Verwenden Sie die **IMAPITable::Unadvise-Methode,** um den Zeiger auf das Advise-Senkenobjekt freizugeben, das im  _parameter lpAdviseSink_ im vorherigen Aufruf von **IMAPITable::Advise** übergeben wurde, wodurch eine Benachrichtigungsregistrierung abgebrochen wird. Im Rahmen des Verwerfens des Zeigers auf das Advise-Senkenobjekt wird die **IUnknown::Release-Methode** des Objekts aufgerufen. Im Allgemeinen wird **Release** während des **Unadvise-Aufrufs** aufgerufen, aber wenn ein anderer Thread gerade dabei ist, die [IMAPIAdviseSink::OnNotify-Methode](imapiadvisesink-onnotify.md) für die Empfehlungssenke aufzurufen, wird der **Release-Aufruf** verzögert, bis die **OnNotify-Methode** zurückgegeben wird. 
  
Weitere Informationen zum Benachrichtigungsprozess finden Sie unter [Ereignisbenachrichtigung in MAPI.](event-notification-in-mapi.md) Spezifische Informationen zur Tabellenbenachrichtigung finden Sie unter ["Informationen zu Tabellenbenachrichtigungen".](about-table-notifications.md) Informationen zur Verwendung der **IMAPISupport-Methoden** zur Unterstützung von Benachrichtigungen finden Sie unter ["Unterstützende Ereignisbenachrichtigung".](supporting-event-notification.md)
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::NotificationOff  <br/> |MFCMAPI verwendet die **IMAPITable::Unadvise-Methode,** um Benachrichtigungen für die Tabelle abzubrechen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPITable::Advise](imapitable-advise.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

