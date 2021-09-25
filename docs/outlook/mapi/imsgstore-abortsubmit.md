---
title: IMsgStoreAbortSubmit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMsgStore.AbortSubmit
api_type:
- COM
ms.assetid: 9be6b88e-2510-4b82-8b35-5f20a0f99fc0
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 28275f50db2775e4183a9386ecaea1d3ff450a2f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551205"
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
  
> [in] Die Byteanzahl im Eintragsbezeichner, auf den der  _lpEntryID-Parameter_ verweist. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf den Eintragsbezeichner der Nachricht, die aus der ausgehenden Warteschlange entfernt werden soll. 
    
 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Nachricht wurde erfolgreich aus der ausgehenden Warteschlange entfernt.
    
MAPI_E_NOT_IN_QUEUE 
  
> Die von  _lpEntryID_ identifizierte Nachricht befindet sich nicht mehr in der ausgehenden Warteschlange des Nachrichtenspeichers, in der Regel, weil sie bereits gesendet wurde. 
    
MAPI_E_UNABLE_TO_ABORT 
  
> Die von  _lpEntryID_ identifizierte Nachricht ist durch den MAPI-Spooler gesperrt, und der Vorgang kann nicht abgebrochen werden. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMsgStore::AbortSubmit-Methode** versucht, eine gesendete Nachricht aus der ausgehenden Warteschlange des Nachrichtenspeichers zu entfernen. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Nachdem eine Nachricht gesendet wurde, ist das Abbrechen der Übermittlung durch Aufrufen von **"AbortSubmit"** die einzige Aktion, die für die Nachricht ausgeführt werden kann. Erwarten Sie nicht, dass **AbortSubmit** immer erfolgreich ist. Je nachdem, wie das zugrunde liegende Messagingsystem implementiert wird, ist es möglicherweise nicht möglich, das Senden der Nachricht abzubrechen. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolderDlg::OnAbortSubmit  <br/> |MFCMAPI verwendet die **IMsgStore::AbortSubmit-Methode,** um die Übermittlung der ausgewählten Nachricht abzubricht.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

