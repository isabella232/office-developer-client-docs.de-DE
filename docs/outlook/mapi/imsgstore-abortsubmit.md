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
ms.openlocfilehash: a176b51577c7d4616d988a0b28f2afcfb554e9f7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564983"
---
# <a name="imsgstoreabortsubmit"></a>IMsgStore::AbortSubmit

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
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
  
> [in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LpEntryID_ verwiesen. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf die Eintrags-ID der Nachricht aus der ausgehenden Warteschlange zu entfernen. 
    
 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Nachricht wurde aus der ausgehenden Warteschlange erfolgreich entfernt.
    
MAPI_E_NOT_IN_QUEUE 
  
> Die Nachricht vom _LpEntryID_ ist nicht mehr in der Nachrichtenspeicher ausgehenden Warteschlange, in der Regel, da es bereits gesendet wurde. 
    
MAPI_E_UNABLE_TO_ABORT 
  
> Die Nachricht vom _LpEntryID_ gesperrt ist, durch die MAPI-Warteschlange, und der Vorgang kann nicht abgebrochen werden. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMsgStore::AbortSubmit** -Methode versucht, eine gesendete Nachricht aus dem Nachrichtenspeicher ausgehende Warteschlange zu entfernen. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Nachdem eine Nachricht gesendet wird, ist das Abbrechen der Übermittlung durch Aufrufen von **AbortSubmit** die einzige Aktion, die für die Nachricht ausgeführt werden kann. Davon ausgehen, dass **AbortSubmit** immer erfolgreich ausgeführt werden kann. Je nachdem, wie das zugrunde liegende messaging-System implementiert wird möglicherweise es nicht möglich, das Senden der Nachricht abzubrechen. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolderDlg::OnAbortSubmit  <br/> |MFCMAPI (engl.) verwendet die **IMsgStore::AbortSubmit** -Methode, um der Übermittlung der ausgewählten Nachricht abzubrechen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

