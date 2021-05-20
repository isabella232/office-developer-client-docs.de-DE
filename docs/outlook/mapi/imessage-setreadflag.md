---
title: IMessageSetReadFlag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.SetReadFlag
api_type:
- COM
ms.assetid: 2d02ebf6-bb8b-42bb-9bd0-870dbae9aeb4
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 874dba4aa18190792a52e29064155f5afa0ef44d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439870"
---
# <a name="imessagesetreadflag"></a>IMessage::SetReadFlag

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Legt das MSGFLAG_READ in der **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) -Eigenschaft der Nachricht fest oder entfernt es und verwaltet das Senden von Leseberichten.
  
```cpp
HRESULT SetReadFlag(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

_ulFlags_
  
> [in] Bitmaske von Flags, die die Einstellung des Lesekennzeichens einer Nachricht steuert, d. h. das MSGFLAG_READ-Flag der Nachricht in ihrer **PR_MESSAGE_FLAGS-Eigenschaft** und die Verarbeitung von Leseberichten. Die folgenden Kennzeichen können festgelegt werden: 
    
  - CLEAR_READ_FLAG: Das MSGFLAG_READ sollte **in** der PR_MESSAGE_FLAGS und kein Lesebericht gesendet werden. 
      
  - CLEAR_NRN_PENDING: Das MSGFLAG_NRN_PENDING-Flag sollte **in** der PR_MESSAGE_FLAGS und ein nicht gelesener Bericht sollte nicht gesendet werden. 
      
  - CLEAR_RN_PENDING: Das MSGFLAG_RN_PENDING-Flag sollte **in** der PR_MESSAGE_FLAGS und kein Lesebericht gesendet werden. 
      
  - GENERATE_RECEIPT_ONLY: Ein Lesebericht sollte gesendet werden, wenn ein Ausstehend ist, aber es sollte keine Änderung im Status des MSGFLAG_READ werden.
      
  - MAPI_DEFERRED_ERRORS: Ermöglicht die erfolgreiche Rückgabe von **SetReadFlag,** möglicherweise vor Abschluss des Vorgangs. 
      
  - SUPPRESS_RECEIPT: Ein ausstehender Lesebericht sollte abgebrochen werden, wenn ein Lesebericht angefordert wurde und dieser Aufruf den Status der Nachricht von ungelesen zu lesen ändert. Wenn dieser Aufruf den Status der Nachricht nicht ändert, kann der Nachrichtenspeicheranbieter dieses Kennzeichen ignorieren.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Leseflag der Nachricht wurde erfolgreich festgelegt oder geräumt.
    
MAPI_E_NO_SUPPRESS 
  
> Der Nachrichtenspeicheranbieter unterstützt die Unterdrückung von Leseberichten nicht.
    
MAPI_E_INVALID_PARAMETER 
  
> Eine der folgenden Kombinationen von Flags wird im  _ulFlags-Parameter_ festgelegt: 
    
   - SUPPRESS_RECEIPT | CLEAR_READ_FLAG 
    
   - SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY
    
   - CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY
    
## <a name="remarks"></a>Hinweise

Die **IMessage::SetReadFlag-Methode** legt das MSGFLAG_READ-Flag der Nachricht in der **PR_MESSAGE_FLAGS-Eigenschaft** fest oder entfernt sie und ruft [IMAPIProp::SaveChanges](imapiprop-savechanges.md) auf, um die Nachricht zu speichern. Das Festlegen MSGFLAG_READ markiert eine Nachricht als gelesen, was nicht unbedingt bedeutet, dass der beabsichtigte Empfänger die Nachricht gelesen hat. 
  
**SetReadFlags** verwaltet auch das Senden von Leseberichten. Ein Lesebericht wird nur gesendet, wenn der Absender einen angefordert hat. 
  
Das Leseflag kann nicht geändert werden für:
  
- Nachrichten, die nicht vorhanden sind.
    
- Nachrichten, die an anderer Stelle verschoben wurden.
    
- Nachrichten, die mit Lese-/Schreibberechtigung geöffnet sind.
    
- Nachrichten, die derzeit übermittelt werden.
    
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn keines der Flags im  _ulFlags-Parameter_ festgelegt ist, gelten die folgenden Regeln: 
  
- Wenn MSGFLAG_READ bereits festgelegt ist, tun Sie nichts.
    
- Wenn MSGFLAG_READ nicht festgelegt ist, legen Sie sie fest, und senden Sie alle ausstehenden Leseberichte, wenn die **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) -Eigenschaft festgelegt ist.
    
Wenn sowohl die SUPPRESS_RECEIPT als auch GENERATE_RECEIPT_ONLY festgelegt sind, sollte das PR_READ_RECEIPT_REQUESTED-Bit, falls festgelegt, geräumt werden, und es sollte kein Lesebericht gesendet werden.
  
Wenn das SUPPRESS_RECEIPT festgelegt ist:
  
- Wenn MSGFLAG_READ bereits festgelegt ist, tun Sie nichts. 
    
- Wenn MSGFLAG_READ nicht festgelegt ist, legen Sie sie fest, und brechen Sie alle ausstehenden Leseberichte ab.
    
Wenn das CLEAR_READ_FLAG festgelegt ist, löschen Sie das MSGFLAG_READ in der  PR_MESSAGE_FLAGS-Eigenschaft jeder Nachricht, und senden Sie keine Leseberichte. 
  
Wenn das GENERATE_RECEIPT_ONLY festgelegt ist, senden Sie alle ausstehenden Leseberichte. Legen Sie keine MSGFLAG_READ.
  
Wenn sowohl SUPPRESS_RECEIPT als auch GENERATE_RECEIPT_ONLY festgelegt sind, legen Sie die PR_READ_RECEIPT_REQUESTED-Eigenschaft auf FALSE, wenn sie festgelegt ist, und senden Sie keinen Lesebericht.
  
Sie können das Berichtsverhalten optimieren, indem Sie die Generierung von Leseberichten unter bestimmten Bedingungen unterdrücken. Wenn Sie jedoch die Unterdrückung von Berichten nicht unterstützen und ein Client **SetReadFlag** mit dem SUPPRESS_RECEIPT aufruft, geben Sie MAPI_E_NO_SUPPRESS. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolderDlg::OnSetReadFlag  <br/> |MFCMAPI verwendet die **IMessage::SetReadFlag-Methode** zum Festlegen von Lesekennzeichen für ausgewählte Nachrichten.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [IMAPIContainer::OpenEntry](imapicontainer-openentry.md)  
- [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md)  
- [IMAPIProp::GetProps](imapiprop-getprops.md)  
- [IMAPIProp::SaveChanges](imapiprop-savechanges.md) 
- [PidTagMessageFlags (kanonische Eigenschaft)](pidtagmessageflags-canonical-property.md) 
- [IMessage: IMAPIProp](imessageimapiprop.md)
- [MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

