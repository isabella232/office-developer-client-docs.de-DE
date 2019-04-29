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
  
Das MSGFLAG_READ-flag in der **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))-Eigenschaft der Nachricht wird festgelegt oder gelöscht, und das Senden von Lese Berichten wird verwaltet.
  
```cpp
HRESULT SetReadFlag(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

_ulFlags_
  
> in Bitmaske von Flags, die die Einstellung des Lese Kennzeichens einer Nachricht steuert, das MSGFLAG_READ-flag der Nachricht in der **PR_MESSAGE_FLAGS** -Eigenschaft und die Verarbeitung von Lese Berichten. Die folgenden Flags können festgelegt werden: 
    
  - CLEAR_READ_FLAG: das MSGFLAG_READ-flag sollte in **PR_MESSAGE_FLAGS** gelöscht werden, und es sollte kein Lesebericht gesendet werden. 
      
  - CLEAR_NRN_PENDING: das MSGFLAG_NRN_PENDING-Flag sollte in **PR_MESSAGE_FLAGS** gelöscht werden, und ein nicht gelesener Bericht sollte nicht gesendet werden. 
      
  - CLEAR_RN_PENDING: das MSGFLAG_RN_PENDING-Flag sollte in **PR_MESSAGE_FLAGS** gelöscht werden, und es sollte kein Lesebericht gesendet werden. 
      
  - GENERATE_RECEIPT_ONLY: ein Lesebericht sollte gesendet werden, wenn ein ausstehender ist, aber es sollte keine Änderung des Status des MSGFLAG_READ-Flags geben.
      
  - MAPI_DEFERRED_ERRORS: ermöglicht es **SetReadFlag** , erfolgreich zurückzugeben, möglicherweise bevor der Vorgang abgeschlossen wurde. 
      
  - SUPPRESS_RECEIPT: ein ausstehender Lesebericht sollte abgebrochen werden, wenn ein Lesebericht angefordert wurde und dieser Aufruf den Status der Nachricht von ungelesen in lesen ändert. Wenn durch diesen Anruf der Status der Nachricht nicht geändert wird, kann der Nachrichtenspeicher Anbieter dieses Flag ignorieren.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Read-Kennzeichnung der Nachricht wurde erfolgreich festgelegt oder gelöscht.
    
MAPI_E_NO_SUPPRESS 
  
> Der Nachrichtenspeicher Anbieter unterstützt die Unterdrückung von Lese Berichten nicht.
    
MAPI_E_INVALID_PARAMETER 
  
> Eine der folgenden Kombinationen von Flags wird im Parameter _ulFlags_ festgelegt: 
    
   - SUPPRESS_RECEIPT | CLEAR_READ_FLAG 
    
   - SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY
    
   - CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY
    
## <a name="remarks"></a>Bemerkungen

Mit der **IMessage:: SetReadFlag** -Methode wird das MSGFLAG_READ-flag der Nachricht in der **PR_MESSAGE_FLAGS** -Eigenschaft festgelegt oder gelöscht, und [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) wird aufgerufen, um die Nachricht zu speichern. Durch Festlegen des MSGFLAG_READ-Flags wird eine Nachricht als gelesen markiert, was nicht unbedingt darauf hinweist, dass der vorgesehene Empfänger die Nachricht tatsächlich gelesen hat. 
  
**SetReadFlags** verwaltet auch das Senden von Lese Berichten. Ein Lesebericht wird nur gesendet, wenn der Absender einen angefordert hat. 
  
Die Read-Kennzeichnung kann nicht geändert werden für:
  
- Nachrichten, die nicht vorhanden sind.
    
- Nachrichten, die an anderer Stelle verschoben wurden.
    
- Mit Lese-/Schreibzugriff geöffnete Nachrichten.
    
- Nachrichten, die derzeit übermittelt werden.
    
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn keines der Flags im Parameter _ulFlags_ festgelegt wird, gelten die folgenden Regeln: 
  
- Wenn MSGFLAG_READ bereits festgelegt ist, tun Sie nichts.
    
- Wenn MSGFLAG_READ nicht festgelegt ist, legen Sie es fest, und senden Sie ausstehende Lese Berichte, wenn die **PR_READ_RECEIPT_REQUESTED** ([pidtagreadreceiptrequested (](pidtagreadreceiptrequested-canonical-property.md))-Eigenschaft festgelegt ist.
    
Wenn sowohl die SUPPRESS_RECEIPT-als auch die GENERATE_RECEIPT_ONLY-Flags festgelegt sind, sollte das PR_READ_RECEIPT_REQUESTED-Bit, falls festgelegt, gelöscht werden, und ein Lesebericht sollte nicht gesendet werden.
  
Wenn das SUPPRESS_RECEIPT-Flag festgelegt ist:
  
- Wenn MSGFLAG_READ bereits festgelegt ist, tun Sie nichts. 
    
- Wenn MSGFLAG_READ nicht festgelegt ist, legen Sie es fest und brechen alle ausstehenden Lese Berichte ab.
    
Wenn das CLEAR_READ_FLAG-Flag festgelegt ist, deaktivieren Sie das MSGFLAG_READ-flag in der **PR_MESSAGE_FLAGS** -Eigenschaft jeder Nachricht, und senden Sie keine Lese Berichte. 
  
Wenn das GENERATE_RECEIPT_ONLY-Flag festgelegt ist, senden Sie ausstehende Lese Berichte. MSGFLAG_READ nicht festlegen oder löschen.
  
Wenn sowohl die SUPPRESS_RECEIPT-als auch die GENERATE_RECEIPT_ONLY-Flags festgelegt sind, legen Sie die PR_READ_RECEIPT_REQUESTED-Eigenschaft auf FALSE fest, wenn Sie festgelegt ist, und senden Sie keinen Lesebericht.
  
Sie können das Verhalten des Berichts optimieren, indem Sie die Generierung von Lese Berichten unter bestimmten Bedingungen verhindern. Wenn Sie jedoch die Unterdrückung von Berichten nicht unterstützen und ein Client **SetReadFlag** mit der SUPPRESS_RECEIPT-flaggruppe aufruft, geben Sie MAPI_E_NO_SUPPRESS zurück. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|FolderDlg. cpp  <br/> |CFolderDlg:: OnSetReadFlag  <br/> |MFCMAPI verwendet die **IMessage:: SetReadFlag** -Methode, um Lese Kennzeichen für ausgewählte Nachrichten festzulegen.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [IMAPIContainer::OpenEntry](imapicontainer-openentry.md)  
- [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md)  
- [IMAPIProp::GetProps](imapiprop-getprops.md)  
- [IMAPIProp::SaveChanges](imapiprop-savechanges.md) 
- [Kanonische PidTagMessageFlags-Eigenschaft](pidtagmessageflags-canonical-property.md) 
- [IMessage: IMAPIProp](imessageimapiprop.md)
- [MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

