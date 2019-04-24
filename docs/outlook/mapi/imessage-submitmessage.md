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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 28786f483c4d2031c334d7b9697db7c5e627fe93
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349231"
---
# <a name="imessagesubmitmessage"></a>IMessage::SubmitMessage

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Speichert alle Eigenschaften der Nachricht und markiert die Nachricht als gesendet.
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> in Bitmaske der Flags, die verwendet werden, um zu steuern, wie eine Nachricht übermittelt wird. Das folgende Flag kann festgelegt werden:
    
FORCE_SUBMIT 
  
> MAPI sollte die Nachricht sofort übermitteln. Dieses Flag wird derzeit nicht verwendet.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_NO_RECIPIENTS 
  
> Die Empfängertabelle der Nachricht ist leer.
    
## <a name="remarks"></a>Bemerkungen

Die **IMessage:: SubmitMessage** -Methode kennzeichnet eine Nachricht als bereit zur Übertragung. MAPI übergibt Nachrichten in der Reihenfolge, in der Sie zum Senden markiert sind, an das zugrunde liegende Messagingsystem. Aufgrund dieser Funktionalität kann eine Nachricht eine Weile in einem Nachrichtenspeicher verbleiben, bevor das zugrunde liegende Messagingsystem dafür verantwortlich ist. Die Reihenfolge des Empfangs am Zielort befindet sich im zugrunde liegenden Messagingsystem und entspricht nicht unbedingt der Reihenfolge, in der Nachrichten gesendet wurden. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Rufen Sie die [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode der Nachricht auf, um Sie zu speichern, und überprüfen Sie dann die **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))-Eigenschaft der Nachricht. Wenn das MSGFLAG_RESEND-Flag festgelegt ist, rufen Sie [IMAPISupport::P reparesubmit](imapisupport-preparesubmit.md). **PrepareSubmit** aktualisiert die Empfängertyp-und **PR_RESPONSIBILITY** ([pidtagresponsibility (](pidtagresponsibility-canonical-property.md))-Eigenschaft für alle Empfänger in der Nachricht erneut senden.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn **SubmitMessage** zurückgibt, sind alle Zeiger auf die Nachricht und die dazugehörigen unter Objekte Nachrichten, Ordner, Anlagen, Streams, Tabellen usw. nicht mehr gültig. MAPI ermöglicht keine weiteren Vorgänge für diese Zeiger, mit Ausnahme des Aufrufs Ihrer **IUnknown:: Release** -Methoden. MAPI ist so konzipiert, dass Sie nach dem Aufruf von **SubmitMessage** die Nachricht und alle zugeordneten unter Objekte freigeben sollten. Wenn **SubmitMessage** jedoch einen Fehlerwert zurückgibt, der fehlende oder ungültige Informationen angibt, bleibt die Nachricht geöffnet, und die Zeiger bleiben gültig. 
  
Wenn Sie einen Sendevorgang abbrechen möchten, rufen Sie einen Zeiger auf die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft der Nachricht ab, und speichern Sie ihn, bevor die Nachricht übermittelt wird. Da die Eintrags-ID einer Nachricht nach der Übermittlung der Nachricht ungültig wird, muss Sie vor dem Aufrufen von **SubmitMessage**gespeichert werden. Zeigen Sie zum Abbrechen des Send-Parameters den Parameter _lpEntryId_ auf diese Eintrags-ID, und rufen Sie [IMsgStore:: AbortSubmit](imsgstore-abortsubmit.md)auf.
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|FolderDlg. cpp  <br/> |**CFolderDlg:: OnSubmitMessage** <br/> |MFCMAPI verwendet die **IMessage:: SubmitMessage** -Methode, um die ausgewählte Nachricht zu übermitteln.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

