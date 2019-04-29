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
  
> in Ein Zeiger auf die Nachricht, die vorbereitet werden soll.
    
 _lpulFlags_
  
> [in, out] Bei der Eingabe ist der _lpulFlags_ -Parameter reserviert und muss NULL sein. Bei der Ausgabe muss _LPULFLAGS_ NULL sein. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Nachricht wurde erfolgreich vorbereitet.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISupport::P reparesubmit** -Methode wird für Support Objekte des Nachrichtenspeicher Anbieters implementiert. Nachrichtenspeicher Anbieter rufen **PrepareSubmit** in ihrer Implementierung der [IMessage:: SubmitMessage](imessage-submitmessage.md) -Methode auf, um eine Nachricht für die Übermittlung an den MAPI-Spooler vorzubereiten. 
  
 **PrepareSubmit** wird verwendet, um Nachrichten zu verarbeiten, für die das MSGFLAG_RESEND-Flag in Ihrer **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))-Eigenschaft festgelegt ist. MSGFLAG_RESEND wird für Nachrichten festgelegt, die eine Anforderung zum erneuten Senden einer anfänglichen Übertragung aufweisen. **PrepareSubmit** bestimmt, welche Empfänger in der Empfängerliste die Nachricht erfolgreich empfangen haben und welche nicht. 
  
Um auf die Empfängerliste zuzugreifen, ruft **PrepareSubmit** die [IMessage::](imessage-getrecipienttable.md) getrecipientable-Methode der Nachricht auf. Zum Abrufen der Empfängerdaten ruft **PrepareSubmit** die [IMAPITable:: QueryRows](imapitable-queryrows.md) -Methode der Empfängertabelle auf. Für jede Zeile in der Tabelle prüft **PrepareSubmit** die **PR_RECIPIENT_TYPE** ([pidtagrecipienttype (](pidtagrecipienttype-canonical-property.md))-Eigenschaft und führt eine der folgenden Aktionen aus:
  
- Wenn das MAPI_SUBMITTED-Flag festgelegt ist, löscht **PrepareSubmit** das Flag und legt die **PR_RESPONSIBILITY** ([PIDTAGRESPONSIBILITY (](pidtagresponsibility-canonical-property.md))-Eigenschaft auf false fest.
    
- Wenn das MAPI_SUBMITTED-Flag nicht festgelegt ist, ändert **PrepareSubmit** **PR_RECIPIENT_TYPE** zu MAPI_P1 und legt **PR_RESPONSIBILITY** auf true fest. 
    
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Stellen Sie vor dem Aufrufen von **PrepareSubmit**sicher, dass Sie die [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md) -Methode aufgerufen und das NOTIFY_READYTOSEND-Flag im Parameter _ulFlags_ festgelegt haben. Der **SpoolerNotify** -Aufruf muss einmal pro Sitzung vor dem Aufruf von **PrepareSubmit**durchgeführt werden. **SpoolerNotify** synchronisiert den MAPI-Spooler und stellt sicher, dass alle erforderlichen Transportanbieter angemeldet sind und ihre Adresstypen registriert sind. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md)
  
[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

