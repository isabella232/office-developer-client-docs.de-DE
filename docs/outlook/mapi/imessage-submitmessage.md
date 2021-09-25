---
title: IMessageSubmitMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMessage.SubmitMessage
api_type:
- COM
ms.assetid: 9ce93469-c55d-48d1-9abb-a637716ed4f2
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b3c574558f29fbb35d8af257ef0599d45e710703
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551268"
---
# <a name="imessagesubmitmessage"></a>IMessage::SubmitMessage

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Speichert alle Eigenschaften der Nachricht und markiert die Nachricht als bereit zum Senden.
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Bitmaske mit Flags, die zum Steuern der Übermittlung einer Nachricht verwendet werden. Das folgende Kennzeichen kann festgelegt werden:
    
FORCE_SUBMIT 
  
> MAPI sollte die Nachricht sofort übermitteln. Dieses Flag wird derzeit nicht verwendet.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_NO_RECIPIENTS 
  
> Die Empfängertabelle der Nachricht ist leer.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMessage::SubmitMessage-Methode** markiert eine Nachricht als bereit für die Übertragung. MapI übergibt Nachrichten an das zugrunde liegende Messagingsystem in der Reihenfolge, in der sie zum Senden markiert sind. Aufgrund dieser Funktionalität verbleibt eine Nachricht möglicherweise einige Zeit in einem Nachrichtenspeicher, bevor das zugrunde liegende Messagingsystem die Verantwortung dafür übernehmen kann. Die Reihenfolge des Empfangs am Ziel befindet sich im Steuerelement des zugrunde liegenden Messagingsystems und stimmt nicht unbedingt mit der Reihenfolge überein, in der Nachrichten gesendet wurden. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Rufen Sie die [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) der Nachricht auf, um sie zu speichern, und überprüfen Sie dann die **Eigenschaft PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) der Nachricht. Wenn das flag MSGFLAG_RESEND festgelegt ist, rufen Sie [IMAPISupport::P repareSubmit](imapisupport-preparesubmit.md)auf. **PrepareSubmit** aktualisiert den Empfängertyp und **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) -Eigenschaft für alle Empfänger in der erneuten Nachricht.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

When **SubmitMessage** returns, all pointers to the message and its associated subobjects messages, folders, attachments, streams, tables, and so on are no longer valid. Die MAPI lässt keine weiteren Vorgänge für diese Zeiger zu, mit Ausnahme des Aufrufs ihrer **IUnknown::Release-Methoden.** MAPI ist so konzipiert, dass Sie nach dem Aufruf von **SubmitMessage** die Nachricht und alle zugehörigen Unterobjekte freigeben sollten. Wenn **SubmitMessage** jedoch einen Fehlerwert zurückgibt, der auf fehlende oder ungültige Informationen hinweist, bleibt die Nachricht geöffnet, und die Zeiger bleiben gültig. 
  
Um einen Sendevorgang abzubrechen, rufen Sie einen Zeiger auf die **Eigenschaft PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) der Nachricht ab, und speichern Sie diesen, bevor die Nachricht gesendet wird. Da der Eintragsbezeichner einer Nachricht nach dem Senden der Nachricht ungültig wird, muss er vor dem Aufrufen von SubmitMessage gespeichert **werden.** Um das Senden abzubrechen, zeigen Sie den  _parameter lpEntryId_ auf diesen Eintragsbezeichner, und rufen [Sie IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)auf.
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |**CFolderDlg::OnSubmitMessage** <br/> |MFCMAPI verwendet die **IMessage::SubmitMessage-Methode,** um die ausgewählte Nachricht zu senden.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

