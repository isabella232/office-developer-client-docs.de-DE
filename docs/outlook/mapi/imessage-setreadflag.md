---
title: IMessageSetReadFlag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMessage.SetReadFlag
api_type:
- COM
ms.assetid: 2d02ebf6-bb8b-42bb-9bd0-870dbae9aeb4
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 98f72229b93c6ae9c5566fc9e277a227469b7e64
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575764"
---
# <a name="imessagesetreadflag"></a>IMessage::SetReadFlag

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Legt fest oder löscht die MSGFLAG_READ Flag in der **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) -Eigenschaft der Nachricht und verwaltet das Senden von Leseberichten.
  
```cpp
HRESULT SetReadFlag(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

_ulFlags_
  
> [in] Bitmaske von Flags, die die Einstellung des Lesekennzeichens einer Nachricht steuert, d. h. die MSGFLAG_READ-Kennzeichnung der Nachricht in der **PR_MESSAGE_FLAGS-Eigenschaft** und die Verarbeitung von Leseberichten. Die folgenden Flags können festgelegt werden: 
    
  - CLEAR_READ_FLAG: Das flag MSGFLAG_READ sollte in **PR_MESSAGE_FLAGS** gelöscht werden, und es sollte kein Lesebericht gesendet werden. 
      
  - CLEAR_NRN_PENDING: Das flag MSGFLAG_NRN_PENDING sollte in **PR_MESSAGE_FLAGS** gelöscht werden, und es sollte kein nicht gelesener Bericht gesendet werden. 
      
  - CLEAR_RN_PENDING: Das flag MSGFLAG_RN_PENDING sollte in **PR_MESSAGE_FLAGS** gelöscht werden, und es sollte kein Lesebericht gesendet werden. 
      
  - GENERATE_RECEIPT_ONLY: Ein Lesebericht sollte gesendet werden, wenn einer aussteht, der Status des MSGFLAG_READ-Flags sollte jedoch nicht geändert werden.
      
  - MAPI_DEFERRED_ERRORS: Ermöglicht **SetReadFlag** die erfolgreiche Rückgabe, möglicherweise bevor der Vorgang abgeschlossen wurde. 
      
  - SUPPRESS_RECEIPT: Ein ausstehender Lesebericht sollte abgebrochen werden, wenn ein Lesebericht angefordert wurde und dieser Aufruf den Status der Nachricht von "Ungelesen" in "Gelesen" ändert. Wenn dieser Aufruf den Status der Nachricht nicht ändert, kann der Nachrichtenspeicheranbieter dieses Kennzeichen ignorieren.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Lesezeichen der Nachricht wurde erfolgreich festgelegt oder gelöscht.
    
MAPI_E_NO_SUPPRESS 
  
> Der Nachrichtenspeicheranbieter unterstützt die Unterdrückung von Leseberichten nicht.
    
MAPI_E_INVALID_PARAMETER 
  
> Eine der folgenden Kombinationen von Flags wird im  _ulFlags-Parameter_ festgelegt: 
    
   - SUPPRESS_RECEIPT | CLEAR_READ_FLAG 
    
   - SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY
    
   - CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMessage::SetReadFlag-Methode** legt das MSGFLAG_READ Flag der Nachricht in der **PR_MESSAGE_FLAGS-Eigenschaft** fest oder löscht sie und ruft [IMAPIProp::SaveChanges](imapiprop-savechanges.md) auf, um die Nachricht zu speichern. Durch Festlegen des MSGFLAG_READ Flags wird eine Nachricht als gelesen gekennzeichnet, was nicht notwendigerweise bedeutet, dass der beabsichtigte Empfänger die Nachricht tatsächlich gelesen hat. 
  
**SetReadFlags** verwaltet auch das Senden von Leseberichten. Ein Lesebericht wird nur gesendet, wenn der Absender einen angefordert hat. 
  
Das Lesezeichen kann für Folgendes nicht geändert werden:
  
- Nachrichten, die nicht vorhanden sind.
    
- Nachrichten, die an eine andere Stelle verschoben wurden.
    
- Nachrichten, die mit Lese-/Schreibberechtigung geöffnet sind.
    
- Nachrichten, die derzeit übermittelt werden.
    
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn keines der Flags im  _ulFlags-Parameter_ festgelegt ist, gelten die folgenden Regeln: 
  
- Wenn MSGFLAG_READ bereits festgelegt ist, führen Sie nichts aus.
    
- Wenn MSGFLAG_READ nicht festgelegt ist, legen Sie es fest, und senden Sie alle ausstehenden Leseberichte, wenn die **eigenschaft PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) festgelegt ist.
    
Wenn die Flags SUPPRESS_RECEIPT und GENERATE_RECEIPT_ONLY festgelegt sind, sollte das PR_READ_RECEIPT_REQUESTED Bit, falls festgelegt, gelöscht und kein Lesebericht gesendet werden.
  
Wenn das flag SUPPRESS_RECEIPT festgelegt ist:
  
- Wenn MSGFLAG_READ bereits festgelegt ist, führen Sie nichts aus. 
    
- Wenn MSGFLAG_READ nicht festgelegt ist, legen Sie es fest, und brechen Sie alle ausstehenden Leseberichte ab.
    
Wenn das flag CLEAR_READ_FLAG festgelegt ist, deaktivieren Sie das MSGFLAG_READ Flag in der **eigenschaft PR_MESSAGE_FLAGS** jeder Nachricht, und senden Sie keine Leseberichte. 
  
Wenn das flag GENERATE_RECEIPT_ONLY festgelegt ist, senden Sie alle ausstehenden Leseberichte. MSGFLAG_READ nicht festlegen oder löschen.
  
Wenn die Flags SUPPRESS_RECEIPT und GENERATE_RECEIPT_ONLY festgelegt sind, legen Sie die PR_READ_RECEIPT_REQUESTED-Eigenschaft auf FALSE fest, wenn sie festgelegt ist, und senden Sie keinen Lesebericht.
  
Sie können das Berichtverhalten optimieren, indem Sie die Generierung von Leseberichten unter bestimmten Bedingungen unterdrücken. Wenn Sie jedoch die Unterdrückung von Berichten nicht unterstützen und ein Client **SetReadFlag** mit dem SUPPRESS_RECEIPT-Flag aufruft, geben Sie MAPI_E_NO_SUPPRESS zurück. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolderDlg::OnSetReadFlag  <br/> |MFCMAPI verwendet die **IMessage::SetReadFlag-Methode,** um Leseflags für ausgewählte Nachrichten festzulegen.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [IMAPIContainer::OpenEntry](imapicontainer-openentry.md)  
- [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md)  
- [IMAPIProp::GetProps](imapiprop-getprops.md)  
- [IMAPIProp::SaveChanges](imapiprop-savechanges.md) 
- [PidTagMessageFlags (kanonische Eigenschaft)](pidtagmessageflags-canonical-property.md) 
- [IMessage: IMAPIProp](imessageimapiprop.md)
- [MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

