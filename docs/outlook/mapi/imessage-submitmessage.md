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
ms.openlocfilehash: 1d325c67c836e727d8285bd2dceecf88bf68327c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792523"
---
# <a name="imessagesubmitmessage"></a>IMessage::SubmitMessage

  
  
**Betrifft**: Outlook 
  
Speichert alle Eigenschaften der Nachricht und markiert die Nachricht als gesendet werden.
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Bitmaske der Flags, die steuern, wie eine Nachricht gesendet wird. Das folgende Flag kann festgelegt werden:
    
FORCE_SUBMIT 
  
> MAPI sollten die Nachricht sofort zu übermitteln. Dieses Kennzeichen werden derzeit nicht verwendet.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_NO_RECIPIENTS 
  
> Empfänger der Nachricht-Tabelle ist leer.
    
## <a name="remarks"></a>Bemerkungen

Die **IMessage::SubmitMessage** -Methode markiert die Nachricht als übertragen werden bereit. MAPI übergibt Nachrichten an die zugrunde liegenden messaging-System in der Reihenfolge, in der sie zum Senden von markiert sind. Aufgrund dieser Funktionalität möglicherweise eine Meldung in einem Nachrichtenspeicher bleiben Sie für eine Weile, bevor das zugrunde liegende messaging-System Verantwortung für sie entgegennehmen kann. Die Reihenfolge des Eingangs im Zielverzeichnis befindet sich in der zugrunde liegenden messaging-System-Steuerelement und entspricht nicht unbedingt die Reihenfolge, in der Nachrichten gesendet wurden. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Rufen Sie die Nachricht [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode zum Speichern und überprüfen Sie dann die Nachricht **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))-Eigenschaft. Wenn das Flag MSGFLAG_RESEND festgelegt ist, rufen Sie [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md). **PrepareSubmit** aktualisiert die Empfängertyp und **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md))-Eigenschaft für alle Empfänger in der Nachricht erneut senden.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

**SubmitMessage** , gibt alle Zeiger auf die Meldung und die zugehörigen Unterobjekte Nachrichten sind Ordner, Anlagen, Datenströme, Tabellen und So weiter nicht mehr gültig. MAPI erlaubt keine weiteren Vorgänge für diese Zeiger, außer für die **IUnknown** -Methoden aufrufen. MAPI ist darauf ausgelegt, dass nach dem Aufruf von **SubmitMessage** Sie die Nachricht und alle zugehörigen Unterobjekte freigegeben werden sollen. Wenn **SubmitMessage** einen Fehler zurück, der angibt, fehlende oder ungültige Informationen zurückgegeben wird, bleibt geöffnet, die Nachricht und die Zeiger noch gültig. 
  
Um ein Sendevorgang abzubrechen, abrufen und einen Zeiger auf die Nachricht **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft gespeichert werden, bevor die Nachricht gesendet wird. Da er die Eintrags-ID eine Nachricht ungültig ist, nachdem die Nachricht gesendet wurde, ist es erforderlich, vor dem Aufruf von **SubmitMessage**zu speichern. Um das Senden abzubrechen, zeigen Sie den Parameter _LpEntryId_ auf dieses Eintrags-ID, und rufen Sie [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |**CFolderDlg::OnSubmitMessage** <br/> |MFCMAPI (engl.) wird die **IMessage::SubmitMessage** -Methode verwendet, um die ausgewählte Nachricht zu übermitteln.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

