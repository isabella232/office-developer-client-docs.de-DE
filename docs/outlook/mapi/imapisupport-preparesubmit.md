---
title: IMAPISupportPrepareSubmit
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.PrepareSubmit
api_type:
- COM
ms.assetid: 467242e3-96c9-4280-9cbc-9ecfe3f279cf
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 738eb346ec5388cbd94b32598236ef2ca05740f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425736"
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
  
> [in] Ein Zeiger auf die zu bereitende Nachricht.
    
 _lpulFlags_
  
> [in, out] Bei der Eingabe ist  _der lpulFlags-Parameter_ reserviert und muss null sein. Bei der Ausgabe  _muss lpulFlags_ NULL sein. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Nachricht wurde erfolgreich vorbereitet.
    
## <a name="remarks"></a>Hinweise

Die **IMAPISupport::P repareSubmit-Methode** wird für Unterstützungsobjekte des Nachrichtenspeicheranbieters implementiert. Nachrichtenspeicheranbieter rufen **PrepareSubmit** in ihrer Implementierung der [IMessage::SubmitMessage-Methode](imessage-submitmessage.md) auf, um eine Nachricht für die Übermittlung an den MAPI-Spooler vorzubereiten. 
  
 **PrepareSubmit wird** verwendet, um Nachrichten zu behandeln, deren MSGFLAG_RESEND -Flag in ihrer **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) festgelegt ist. MSGFLAG_RESEND wird für Nachrichten festgelegt, die eine Anforderung enthalten, die bei einem Fehler bei der ersten Übertragung erneut gesendet werden soll. **PrepareSubmit** bestimmt, welcher der Empfänger in der Empfängerliste die Nachricht erfolgreich empfangen hat und welche nicht. 
  
Um auf die Empfängerliste zu zugreifen, **ruft PrepareSubmit** die [IMessage::GetRecipientTable-Methode der Nachricht](imessage-getrecipienttable.md) auf. Zum Abrufen der Empfängerdaten ruft **PrepareSubmit** die [IMAPITable::QueryRows-Methode](imapitable-queryrows.md) der Empfängertabelle auf. Für jede Zeile in der Tabelle überprüft **PrepareSubmit** die **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) -Eigenschaft und führt eine der folgenden Aktionen aus:
  
- Wenn das MAPI_SUBMITTED festgelegt ist, wird das Flag von **PrepareSubmit** entfernt und die **eigenschaft PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) auf FALSE festgelegt.
    
- Wenn das MAPI_SUBMITTED nicht festgelegt ist, wird  **PrepareSubmit** PR_RECIPIENT_TYPE in MAPI_P1 geändert und **PR_RESPONSIBILITY** TRUE festgelegt. 
    
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Stellen Sie vor dem Aufrufen von **PrepareSubmit** sicher, dass Sie die [IMAPISupport::SpoolerNotify-Methode](imapisupport-spoolernotify.md) aufgerufen haben, und legen Sie das NOTIFY_READYTOSEND im  _ulFlags-Parameter_ fest. Der **SpoolerNotify-Aufruf** muss einmal pro Sitzung vor dem Aufruf von **PrepareSubmit vorgenommen werden.** **SpoolerNotify** synchronisiert den MAPI-Spooler und stellt sicher, dass alle erforderlichen Transportanbieter angemeldet sind und ihre Adresstypen registriert werden. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md)
  
[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

