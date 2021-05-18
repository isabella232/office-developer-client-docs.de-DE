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
ms.openlocfilehash: 39d8786bf558ade4599d69e0a764f87fe60d99f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408768"
---
# <a name="imapisupportstatusrecips"></a>IMAPISupport::StatusRecips

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Generiert Übermittlungs- und Nicht-Lieferberichte.
  
```cpp
HRESULT StatusRecips(
LPMESSAGE lpMessage,
LPADRLIST lpRecipList
);
```

## <a name="parameters"></a>Parameter

 _lpMessage_
  
> [in] Ein Zeiger auf die Nachricht, für die der Bericht generiert werden soll.
    
 _lpRecipList_
  
> [in] Ein Zeiger auf eine [ADRLIST-Struktur,](adrlist.md) die die Empfänger der Nachricht beschreibt, auf die von _lpMessage verwiesen wird._
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Bericht wurde erfolgreich generiert.
    
MAPI_W_ERRORS_RETURNED 
  
> Der Anruf war insgesamt erfolgreich, es gibt jedoch keine Empfängeroptionen für diesen Empfängertyp. Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden. Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** Makro. Weitere Informationen finden Sie unter [Using Macros for Error Handling](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Hinweise

Die **IMAPISupport::StatusRecips-Methode** wird für Unterstützungsobjekte des Transportanbieters implementiert. Transportanbieter rufen **StatusRecips auf,** um zu fordern, dass MAPI einen Zustellungs- oder Unzustelldienstbericht an einen oder mehrere Empfänger einer Nachricht sendet. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie können **StatusRecips während** der Verarbeitung einer Nachricht mehrmals aufrufen. Wenn Sie **statusRecips** jedoch für eine geöffnete Nachricht aufrufen, tun Sie ihr Bestes, um alle Übermittlungs- und Nichtzustellinformationen für die Nachrichtenempfänger zu sammeln und **StatusRecips** für diese Empfängerliste anzurufen. Ein einzelner Sammlungspunkt ist wichtig, da mehrere **StatusRecips-Aufrufe** für einen Empfänger dazu führen können, dass mehrere identische Berichte gesendet werden. 
  
Store eigenschaften, die sich auf die Nachrichtenzustellung oder Nichtzustellung in der **adrlist-Struktur** beziehen, die durch den _lpRecipList-Parameter angegeben_ wird. Eine vollständige Liste der erforderlichen und optionalen Eigenschaften für Übermittlungsberichte und Nicht-Lieferberichte finden Sie unter [Required Report Message Properties](required-report-message-properties.md) und Optional Report Message [Properties](optional-report-message-properties.md). 
  
Zuordnen von Arbeitsspeicher für die **ADRLIST-Struktur** in _lpRecipList_ mithilfe der [Funktionen MAPIAllocateBuffer](mapiallocatebuffer.md) und [MAPIAllocateMore.](mapiallocatemore.md) MAPI gibt den Speicher frei, indem die [MAPIFreeBuffer-Funktion](mapifreebuffer.md) nur dann aufruft, wenn **StatusRecips erfolgreich** ist. 
  
Eine Übersicht über Zustellungs- und Nicht-Lieferberichte finden Sie unter [MAPI Report Messages](mapi-report-messages.md).
  
## <a name="see-also"></a>Siehe auch



[ADRLIST](adrlist.md)
  
[IMAPISupport::Address](imapisupport-address.md)
  
[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IXPLogon::EndMessage](ixplogon-endmessage.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

