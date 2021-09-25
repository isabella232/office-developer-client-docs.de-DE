---
title: IMAPISupportPrepareSubmit
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.PrepareSubmit
api_type:
- COM
ms.assetid: 467242e3-96c9-4280-9cbc-9ecfe3f279cf
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f2af8c43329b7b6333bc288d420e574276965239
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625413"
---
# <a name="imapisupportpreparesubmit"></a>IMAPISupport::PrepareSubmit

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bereitet eine Nachricht für die Übermittlung an den MAPI-Spooler vor.
  
```cpp
HRESULT PrepareSubmit(
LPMESSAGE lpMessage,
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpMessage_
  
> [in] Ein Zeiger auf die vorzubereitende Nachricht.
    
 _lpulFlags_
  
> [in, out] Bei der Eingabe ist der  _lpulFlags-Parameter_ reserviert und muss null sein. Bei der Ausgabe muss  _lpulFlags_ NULL sein. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Nachricht wurde erfolgreich vorbereitet.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISupport::P repareSubmit-Methode** wird für Supportobjekte des Nachrichtenspeicheranbieters implementiert. Nachrichtenspeicheranbieter rufen **PrepareSubmit** in ihrer Implementierung der [IMessage::SubmitMessage-Methode](imessage-submitmessage.md) auf, um eine Nachricht für die Übermittlung an den MAPI-Spooler vorzubereiten. 
  
 **PrepareSubmit** wird verwendet, um Nachrichten zu behandeln, deren MSGFLAG_RESEND Flag in der **PR_MESSAGE_FLAGS** -[PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) -Eigenschaft festgelegt ist. MSGFLAG_RESEND wird für Nachrichten festgelegt, die eine Anforderung enthalten, die erneut gesendet werden soll, wenn eine anfängliche Übertragung fehlschlägt. **PrepareSubmit** bestimmt, welcher der Empfänger in der Empfängerliste die Nachricht erfolgreich empfangen hat und welche nicht. 
  
Um auf die Empfängerliste zuzugreifen, ruft **PrepareSubmit** die [IMessage::GetRecipientTable-Methode](imessage-getrecipienttable.md) der Nachricht auf. Zum Abrufen der Empfängerdaten ruft **PrepareSubmit** die [IMAPITable::QueryRows-Methode](imapitable-queryrows.md) der Empfängertabelle auf. Für jede Zeile in der Tabelle überprüft **PrepareSubmit** die **Eigenschaft PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) und führt eine der folgenden Aktionen aus:
  
- Wenn das MAPI_SUBMITTED Flag festgelegt ist, löscht **PrepareSubmit** das Flag und legt die **eigenschaft PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) auf FALSE fest.
    
- Wenn das MAPI_SUBMITTED-Kennzeichen nicht festgelegt ist, **ändert PrepareSubmit** **änderungen PR_RECIPIENT_TYPE** auf MAPI_P1 und legt **PR_RESPONSIBILITY** auf TRUE fest. 
    
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Bevor Sie **PrepareSubmit** aufrufen, müssen Sie sicherstellen, dass Sie die [IMAPISupport::SpoolerNotify-Methode](imapisupport-spoolernotify.md) aufgerufen und das NOTIFY_READYTOSEND-Flag im  _ulFlags-Parameter_ festgelegt haben. Der **SpoolerNotify-Aufruf** muss einmal pro Sitzung vor dem Aufruf von **PrepareSubmit** ausgeführt werden. **SpoolerNotify** synchronisiert den MAPI-Spooler und stellt sicher, dass alle erforderlichen Transportanbieter angemeldet sind und ihre Adresstypen registriert sind. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md)
  
[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

