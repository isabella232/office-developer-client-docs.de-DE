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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 0ae35166f01f597c2c3ab399a1b66e5760ab0dc8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792519"
---
# <a name="imessagesetreadflag"></a>IMessage::SetReadFlag

**Betrifft**: Outlook 
  
Festgelegt oder löscht das Flag MSGFLAG_READ in der Eigenschaft **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) der Nachricht und das Senden von lesen Berichte verwaltet.
  
```cpp
HRESULT SetReadFlag(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

_ulFlags_
  
> [in] Bitmaske aus Flags, die die Einstellung der eine Nachricht lesen steuert kennzeichnen d. h., die Nachricht MSGFLAG_READ Flag in seiner **PR_MESSAGE_FLAGS** -Eigenschaft und die Verarbeitung von Berichten lesen. Die folgenden Kennzeichen können festgelegt werden: 
    
  - CLEAR_READ_FLAG: Das Flag MSGFLAG_READ sollte in **PR_MESSAGE_FLAGS** deaktiviert werden und kein Lese Bericht gesendet werden soll. 
      
  - CLEAR_NRN_PENDING: Das Flag MSGFLAG_NRN_PENDING sollte in **PR_MESSAGE_FLAGS** deaktiviert werden und ein Bericht nicht gelesen nicht gesendet werden soll. 
      
  - CLEAR_RN_PENDING: Das Flag MSGFLAG_RN_PENDING sollte in **PR_MESSAGE_FLAGS** deaktiviert werden und kein Lese Bericht gesendet werden soll. 
      
  - GENERATE_RECEIPT_ONLY: Lese-Bericht gesendet werden soll, wenn eine steht noch aus, aber keine Änderung im Zustand des MSGFLAG_READ Flags werden soll.
      
  - MAPI_DEFERRED_ERRORS: Ermöglicht **SetReadFlag** erfolgreich, möglicherweise beendet, bevor der Vorgang abgeschlossen ist. 
      
  - SUPPRESS_RECEIPT: Ein ausstehender lesen Bericht sollte abgebrochen werden, wenn ein Bericht lesen angefordert und dieses Anrufs den Status der Nachricht vom ungelesene zum Lesen von ändert. Wenn dieses Anrufs nicht den Status der Nachricht ändert, kann der Nachricht Speicheranbieter dieses Flag ignorieren.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Lesen Nachrichtenkennzeichnung wurde erfolgreich festgelegt oder gelöscht.
    
MAPI_E_NO_SUPPRESS 
  
> Der Nachricht Speicheranbieter unterstützt nicht die Unterdrückung der Lese-Berichte.
    
MAPI_E_INVALID_PARAMETER 
  
> Eine der folgenden Kombinationen von Flags wird in der _UlFlags_ -Parameter festgelegt: 
    
   - SUPPRESS_RECEIPT | CLEAR_READ_FLAG 
    
   - SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY
    
   - CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY
    
## <a name="remarks"></a>Bemerkungen

Die **IMessage::SetReadFlag** -Methode legt oder löscht die Nachricht MSGFLAG_READ Flag in der **PR_MESSAGE_FLAGS** -Eigenschaft und ruft [IMAPIProp::SaveChanges](imapiprop-savechanges.md) die Nachricht zu speichern. Festlegen des MSGFLAG_READ-Flags markiert eine Nachricht als gelesen, die nicht unbedingt darauf hinweist, dass der Empfänger die Nachricht tatsächlich gelesen hat. 
  
**SetReadFlags** verwaltet auch das Senden von Berichten lesen. Ein Bericht gelesen wird gesendet, nur, wenn der Absender eine angefordert hat. 
  
Das Flag lesen können für nicht geändert werden:
  
- Nachrichten, die nicht vorhanden sind.
    
- Nachrichten, die wurden verschoben eingehen.
    
- Nachrichten, die mit Lese-/Schreibzugriff geöffnet sind.
    
- Nachrichten, die derzeit übermittelt werden.
    
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn keiner der Werte in der _UlFlags_ -Parameter festgelegt ist, gelten die folgenden Regeln: 
  
- Wenn MSGFLAG_READ bereits festgelegt ist, wird keine Aktion durchgeführt.
    
- Wenn MSGFLAG_READ nicht festgelegt ist, legen Sie es, und senden Sie alle ausstehenden lesen Berichte, wenn die Eigenschaft **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) festgelegt ist.
    
Wenn die SUPPRESS_RECEIPT und die GENERATE_RECEIPT_ONLY Flags festgelegt sind, die PR_READ_RECEIPT_REQUESTED bit, wenn festgelegt, gelöscht werden sollen und ein Bericht lesen nicht gesendet werden soll.
  
Wenn das Flag SUPPRESS_RECEIPT festgelegt ist:
  
- Wenn MSGFLAG_READ bereits festgelegt ist, wird keine Aktion durchgeführt. 
    
- Wenn MSGFLAG_READ nicht festgelegt ist, legen Sie es und Abbrechen an alle ausstehenden lesen Berichte.
    
Wenn das Flag CLEAR_READ_FLAG festgelegt ist, deaktivieren Sie die Kennzeichen MSGFLAG_READ in jede Nachricht **PR_MESSAGE_FLAGS** -Eigenschaft und senden Sie keine lesen Berichte. 
  
Wenn das Flag GENERATE_RECEIPT_ONLY festgelegt ist, senden Sie alle ausstehenden Lese-Berichte. Führen Sie MSGFLAG_READ nicht festgelegt oder löschen.
  
Wenn die SUPPRESS_RECEIPT und die GENERATE_RECEIPT_ONLY Flags festgelegt werden, die PR_READ_RECEIPT_REQUESTED-Eigenschaft auf FALSE festgelegt, wenn sie festgelegt ist, und senden Sie einen read Bericht nicht.
  
Sie können Bericht Verhalten optimieren, indem Sie die Generierung von lesen Berichte unter bestimmten Umständen unterdrücken. Jedoch, wenn Sie die Unterdrückung von Berichten nicht unterstützt und **SetReadFlag** von einem Client mit dem Flag SUPPRESS_RECEIPT aufgerufen, MAPI_E_NO_SUPPRESS zurück. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolderDlg::OnSetReadFlag  <br/> |MFCMAPI (engl.) verwendet die **IMessage::SetReadFlag** -Methode, lesen Flags für ausgewählte Nachrichten festzulegen.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [IMAPIContainer::OpenEntry](imapicontainer-openentry.md)  
- [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md)  
- [IMAPIProp::GetProps](imapiprop-getprops.md)  
- [IMAPIProp::SaveChanges](imapiprop-savechanges.md) 
- [PidTagMessageFlags (kanonische Eigenschaft)](pidtagmessageflags-canonical-property.md) 
- [IMessage: IMAPIProp](imessageimapiprop.md)
- [MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

