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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f6902b45cde3e5349d69b6f35c3f8980deb031b4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792424"
---
# <a name="imapisupportpreparesubmit"></a>IMAPISupport::PrepareSubmit

  
  
**Betrifft**: Outlook 
  
Bereitet eine Nachricht für die Übermittlung an die MAPI-Warteschlange.
  
```cpp
HRESULT PrepareSubmit(
LPMESSAGE lpMessage,
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpMessage_
  
> [in] Ein Zeiger auf die Nachricht zum Vorbereiten.
    
 _lpulFlags_
  
> [in, out] Bei der Eingabe der Parameter _LpulFlags_ ist reserviert und muss NULL sein. _LpulFlags_ muss NULL sein, bei der Ausgabe. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Nachricht wurde erfolgreich vorbereitet.
    
## <a name="remarks"></a>Hinweise

Die **IMAPISupport::PrepareSubmit** -Methode wird für Message Store Anbieter Unterstützungsobjekte implementiert. Nachricht-Anbieter anrufen **PrepareSubmit** in ihrer Implementierung der [IMessage::SubmitMessage](imessage-submitmessage.md) -Methode, um eine Nachricht für die Übermittlung an die Warteschlange MAPI vorbereiten. 
  
 **PrepareSubmit** wird verwendet, um die Verarbeitung von Nachrichten, die die in ihrer **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))-Eigenschaft MSGFLAG_RESEND gekennzeichnet sind. MSGFLAG_RESEND wird für Nachrichten festgelegt, die eine Anforderung erneut gesendet werden, wenn eine anfängliche Übertragung fehlschlägt enthalten. **PrepareSubmit** bestimmt, dem der Empfänger in der Liste der Empfänger die Nachricht erfolgreich empfangen und die nicht der Fall. 
  
**PrepareSubmit** die Nachricht [IMessage::GetRecipientTable](imessage-getrecipienttable.md) Methode aufgerufen, um Zugriff auf die Empfängerliste. Zum Abrufen der Empfängerdaten ruft **PrepareSubmit** [QueryRows der Empfänger Tabelle](imapitable-queryrows.md) . Für jede Zeile in der Tabelle **PrepareSubmit** die **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))-Eigenschaft überprüft und akzeptiert einen der folgenden Aktionen:
  
- Wenn das Flag MAPI_SUBMITTED festgelegt ist, löscht das Flag **PrepareSubmit** , und die **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md))-Eigenschaft auf FALSE festgelegt.
    
- Wenn das Flag MAPI_SUBMITTED nicht festgelegt ist, wird **PrepareSubmit** **PR_RECIPIENT_TYPE** in MAPI_P1 geändert und **PR_RESPONSIBILITY** auf TRUE festgelegt. 
    
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Bevor Sie **PrepareSubmit**aufrufen, müssen Sie unbedingt, haben die [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) -Methode aufgerufen und legen Sie die Kennzeichen NOTIFY_READYTOSEND im _UlFlags_ -Parameter. Die **SpoolerNotify** muss einmal pro Sitzung vor dem Aufruf von **PrepareSubmit**aufgerufen werden. **SpoolerNotify** synchronisiert die MAPI-Warteschlange und wird sichergestellt, dass alle erforderlichen Transportanbieter angemeldet sind und ihre Adresstypen registriert sind. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md)
  
[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

