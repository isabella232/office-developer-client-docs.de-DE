---
title: IMessageSubmitMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.SubmitMessage
api_type:
- COM
ms.assetid: 9ce93469-c55d-48d1-9abb-a637716ed4f2
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 28786f483c4d2031c334d7b9697db7c5e627fe93
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437364"
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
  
> [in] Bitmaske von Flags, die verwendet werden, um zu steuern, wie eine Nachricht übermittelt wird. Das folgende Flag kann festgelegt werden:
    
FORCE_SUBMIT 
  
> MAPI sollte die Nachricht sofort übermitteln. Dieses Flag wird derzeit nicht verwendet.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_NO_RECIPIENTS 
  
> Die Empfängertabelle der Nachricht ist leer.
    
## <a name="remarks"></a>Hinweise

Die **IMessage::SubmitMessage-Methode** markiert eine Nachricht als bereit für die Übertragung. MAPI übergibt Nachrichten an das zugrunde liegende Messagingsystem in der Reihenfolge, in der sie für das Senden markiert sind. Aufgrund dieser Funktionalität bleibt eine Nachricht möglicherweise einige Zeit in einem Nachrichtenspeicher, bevor das zugrunde liegende Messagingsystem die Verantwortung dafür übernehmen kann. Die Reihenfolge des Empfangs am Ziel befindet sich im Steuerelement des zugrunde liegenden Messagingsystems und nicht unbedingt mit der Reihenfolge, in der Nachrichten gesendet wurden. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Rufen Sie die [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) der Nachricht auf, um sie zu speichern, und überprüfen Sie dann die **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))-Eigenschaft der Nachricht. Wenn das MSGFLAG_RESEND festgelegt ist, rufen [Sie IMAPISupport::P repareSubmit auf.](imapisupport-preparesubmit.md) **PrepareSubmit** aktualisiert den Empfängertyp **und PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md))-Eigenschaft für alle Empfänger in der erneut gesendeten Nachricht.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn **SubmitMessage** zurückgegeben wird, sind alle Zeiger auf die Nachricht und die zugehörigen Unterobjekte Nachrichten, Ordner, Anlagen, Datenströme, Tabellen und so weiter nicht mehr gültig. MAPI lässt keine weiteren Vorgänge für diese Zeiger zu, mit Ausnahme des Aufrufens ihrer **IUnknown::Release-Methoden.** MAPI ist so konzipiert, dass Sie nach dem Aufgerufen von **SubmitMessage** die Nachricht und alle zugehörigen Unterobjekte los lassen sollten. Wenn **SubmitMessage** jedoch einen Fehlerwert zurückgibt, der fehlende oder ungültige Informationen angibt, bleibt die Nachricht geöffnet, und die Zeiger bleiben gültig. 
  
Um einen Sendevorgang abbricht, erhalten und speichern Sie einen Zeiger auf die **PR_ENTRYID** -[PidTagEntryId](pidtagentryid-canonical-property.md)-Eigenschaft der Nachricht, bevor die Nachricht übermittelt wird. Da der Eintragsbezeichner einer Nachricht ungültig ist, nachdem die Nachricht übermittelt wurde, muss sie gespeichert werden, bevor **Sie SubmitMessage aufrufen.** Wenn Sie das Senden abbrechen möchten, zeigen Sie den _lpEntryId-Parameter_ auf diesen Eintragsbezeichner, und rufen Sie [IMsgStore::AbortSubmit auf.](imsgstore-abortsubmit.md)
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |**CFolderDlg::OnSubmitMessage** <br/> |MFCMAPI verwendet die **IMessage::SubmitMessage-Methode,** um die ausgewählte Nachricht zu übermitteln.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

