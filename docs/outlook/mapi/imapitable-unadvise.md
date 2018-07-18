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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: e9d8565cfaa17764e92bddafb29e744d23872515
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792491"
---
# <a name="imapitableunadvise"></a>IMAPITable::Unadvise

  
  
**Betrifft**: Outlook 
  
Bricht ab, das Senden von Benachrichtigungen, die zuvor mit einem Aufruf der Methode [IMAPITable::Advise](imapitable-advise.md) eingerichtet. 
  
```cpp
HRESULT Unadvise(
ULONG_PTR ulConnection
);
```

## <a name="parameters"></a>Parameter

 _ulConnection_
  
> [in] Die Anzahl der Registrierung Verbindung durch einen Aufruf von [IMAPITable::Advise](imapitable-advise.md)zurückgegeben.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf war erfolgreich.
    
## <a name="remarks"></a>Bemerkungen

Verwenden Sie die **IMAPITable::Unadvise** -Methode, um den Zeiger auf den im Parameter _LpAdviseSink_ im vorherigen Aufruf **IMAPITable::Advise**, wodurch Stornieren einer benachrichtigungsregistrierung übergeben Advise-Empfängerobjekt freizugeben. Im Rahmen des Zeigers auf das Empfängerobjekt Advise verwerfen wird das Objekt **IUnknown** -Methode aufgerufen. Im allgemeinen **Release** aufgerufen wird während des Anrufs **Unadvise** , jedoch ist, wenn ein anderer Thread aufruft, die [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) -Methode für die Advise-Empfänger der Anruf **Version** verzögert, bis die **OnNotify** -Methode zurückgegeben. 
  
Weitere Informationen zu den Benachrichtigungsprozess finden Sie unter [Event Notification in MAPI](event-notification-in-mapi.md). Spezifische Informationen zur Tabelle Benachrichtigung finden Sie unter [Zur Tabelle Benachrichtigungen](about-table-notifications.md). Informationen zur Verwendung der Methods **IMAPISupport** zum Benachrichtigung zu unterstützen finden Sie unter [Event Notification unterstützen](supporting-event-notification.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::NotificationOff  <br/> |MFCMAPI (engl.) verwendet die **IMAPITable::Unadvise** -Methode, um Benachrichtigungen für die Tabelle abzubrechen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPITable::Advise](imapitable-advise.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

