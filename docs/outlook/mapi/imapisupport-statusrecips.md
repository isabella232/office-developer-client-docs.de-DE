---
title: IMAPISupportStatusRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.StatusRecips
api_type:
- COM
ms.assetid: 9c34538e-5ba4-47c8-8002-85afa9d6c067
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: cda629cf78d3f7915b64c130867ed4f8ebbd6f8d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563842"
---
# <a name="imapisupportstatusrecips"></a>IMAPISupport::StatusRecips

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Bereitstellung und Nondelivery Berichte generiert.
  
```cpp
HRESULT StatusRecips(
LPMESSAGE lpMessage,
LPADRLIST lpRecipList
);
```

## <a name="parameters"></a>Parameter

 _lpMessage_
  
> [in] Ein Zeiger auf die Meldung für die der Bericht generiert werden soll.
    
 _lpRecipList_
  
> [in] Ein Zeiger auf eine [ADRLIST](adrlist.md) -Struktur, die Empfänger der Nachricht beschreibt, auf _LpMessage_zeigt.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Bericht wurde erfolgreich generiert.
    
MAPI_W_ERRORS_RETURNED 
  
> Der Aufruf war insgesamt erfolgreich, aber es sind keine Empfänger Optionen für diese Art des Empfängers. Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich verarbeitet. Verwenden Sie das Makro **HR_FAILED** , um für diese Warnung zu testen. Weitere Informationen finden Sie unter [Verwendung von Makros Fehlerbehandlung](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPISupport::StatusRecips** -Methode wird für Transport Anbieter Unterstützungsobjekte implementiert. Transportanbieter Aufrufen **StatusRecips** um anzufordern, MAPI Senden eines Berichts Übermittlung oder Nondelivery einen Satz von mindestens eines der Empfänger einer Nachricht. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie können **StatusRecips** mehrmals während der Verarbeitung einer Nachricht aufrufen. Jedoch, wenn Sie **StatusRecips** für einer geöffneten Nachricht aufrufen, sollten Sie sammeln alle Übermittlung und Nondelivery Informationen für die Empfänger der Nachricht, und rufen Sie **StatusRecips** für diese Empfängerliste. Eine zentrale Stelle Auflistung ist wichtig, da mehrere **StatusRecips** Anrufe für einen Empfänger in mehreren identische Berichten gesendete führen können. 
  
Speichern von Eigenschaften, die auf die Nachrichtenübermittlung oder Nondelivery in der **ADRLIST** -Struktur, die durch den _LpRecipList_ -Parameter angegebenen beziehen. Eine vollständige Liste der erforderlichen und optionalen Eigenschaften für Übermittlungsberichte und Unzustellbarkeitsberichten finden Sie unter [Erforderliche Bericht Nachrichteneigenschaften](required-report-message-properties.md) und [Optional Bericht Nachrichteneigenschaften](optional-report-message-properties.md). 
  
Speicher für die **ADRLIST** -Struktur im _LpRecipList_ mithilfe der Funktionen [MAPIAllocateBuffer](mapiallocatebuffer.md) und [MAPIAllocateMore](mapiallocatemore.md) . MAPI-Freigaben für den Speicher durch Aufrufen der Funktion [MAPIFreeBuffer](mapifreebuffer.md) nur, wenn **StatusRecips** erfolgreich ausgeführt wird. 
  
Eine Übersicht über die Bereitstellung und Nondelivery Berichte finden Sie unter [MAPI-Berichtnachrichten](mapi-report-messages.md).
  
## <a name="see-also"></a>Siehe auch



[ADRLIST](adrlist.md)
  
[IMAPISupport::Address](imapisupport-address.md)
  
[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IXPLogon::EndMessage](ixplogon-endmessage.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

