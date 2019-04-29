---
title: IMsgStoreAbortSubmit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.AbortSubmit
api_type:
- COM
ms.assetid: 9be6b88e-2510-4b82-8b35-5f20a0f99fc0
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 1486730dfa2d76bf8e97439213851b195504962f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414382"
---
# <a name="imsgstoreabortsubmit"></a>IMsgStore::AbortSubmit

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Versucht, eine Nachricht aus der ausgehenden Warteschlange zu entfernen.
  
```cpp
AbortSubmit(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _cbEntryID_
  
> in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEntryID_ -Parameter verwiesen wird. 
    
 _lpEntryID_
  
> in Ein Zeiger auf die Eintrags-ID der Nachricht, die aus der ausgehenden Warteschlange entfernt werden soll. 
    
 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Nachricht wurde erfolgreich aus der ausgehenden Warteschlange entfernt.
    
MAPI_E_NOT_IN_QUEUE 
  
> Die von _lpEntryID_ angegebene Nachricht befindet sich nicht mehr in der ausgehenden Warteschlange des Nachrichtenspeichers, in der Regel, weil Sie bereits gesendet wurde. 
    
MAPI_E_UNABLE_TO_ABORT 
  
> Die von _lpEntryID_ angegebene Nachricht wird vom MAPI-Spooler gesperrt, und der Vorgang kann nicht abgebrochen werden. 
    
## <a name="remarks"></a>Bemerkungen

Die **IMsgStore:: AbortSubmit** -Methode versucht, eine übermittelte Nachricht aus der ausgehenden Warteschlange des Nachrichtenspeichers zu entfernen. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Nachdem eine Nachricht übermittelt wurde, wird die Übermittlung durch Aufrufen von **AbortSubmit** abgebrochen und ist die einzige Aktion, die für die Nachricht ausgeführt werden kann. Erwarten Sie nicht, dass **AbortSubmit** immer erfolgreich ist. Je nachdem, wie das zugrunde liegende Messagingsystem implementiert wird, kann das Senden der Nachricht möglicherweise nicht abgebrochen werden. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|FolderDlg. cpp  <br/> |CFolderDlg:: OnAbortSubmit  <br/> |MFCMAPI verwendet die **IMsgStore:: AbortSubmit** -Methode, um die Übermittlung der ausgewählten Nachricht abzubrechen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

