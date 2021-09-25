---
title: IMAPISupportStatusRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.StatusRecips
api_type:
- COM
ms.assetid: 9c34538e-5ba4-47c8-8002-85afa9d6c067
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f892380c1e113d2400d8b5d14e288a9a3fe322af
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592375"
---
# <a name="imapisupportstatusrecips"></a>IMAPISupport::StatusRecips

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Generiert Übermittlungs- und Unzustellbarkeitsberichte.
  
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
  
> [in] Ein Zeiger auf eine [ADRLIST-Struktur,](adrlist.md) die die Empfänger der Nachricht beschreibt, auf die von  _lpMessage_ verwiesen wird.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Bericht wurde erfolgreich generiert.
    
MAPI_W_ERRORS_RETURNED 
  
> Der Anruf war insgesamt erfolgreich, es gibt jedoch keine Empfängeroptionen für diesen Empfängertyp. Wenn diese Warnung zurückgegeben wird, sollte der Aufruf als erfolgreich behandelt werden. Verwenden Sie das Makro **HR_FAILED, um** diese Warnung zu testen. Weitere Informationen finden Sie unter [Verwenden von Makros für die Fehlerbehandlung.](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPISupport::StatusRecips-Methode** wird für Transportanbieter-Supportobjekte implementiert. Transportanbieter rufen **StatusRecips** auf, um anzufordern, dass MAPI einen Übermittlungs- oder Unzustellbarkeitsbericht an einen oder mehrere Empfänger einer Nachricht sendet. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

**StatusRecips** kann während der Verarbeitung einer Nachricht mehrmals aufgerufen werden. Wenn Sie **statusRecips** jedoch für eine geöffnete Nachricht aufrufen, sollten Sie alle Übermittlungs- und Unzustellbarkeitsinformationen für die Nachrichtenempfänger erfassen und **StatusRecips** für diese Empfängerliste aufrufen. Ein einzelner Sammlungspunkt ist wichtig, da mehrere **StatusRecips-Aufrufe** für einen Empfänger dazu führen können, dass mehrere identische Berichte gesendet werden. 
  
Store Eigenschaften, die sich auf die Nachrichtenübermittlung oder die Nichtübermittlung in der **ADRLIST-Struktur** beziehen, die durch den _lpRecipList-Parameter_ angegeben wird. Eine vollständige Liste der erforderlichen und optionalen Eigenschaften für Übermittlungsberichte und Nicht-Nachrichtenberichte finden Sie unter ["Erforderliche Berichtsnachrichteneigenschaften"](required-report-message-properties.md) und ["Optionale Berichtsnachrichteneigenschaften".](optional-report-message-properties.md) 
  
Weisen Sie Speicher für die **ADRLIST-Struktur** in  _lpRecipList_ zu, indem Sie die Funktionen [MAPIAllocateBuffer](mapiallocatebuffer.md) und [MAPIAllocateMore](mapiallocatemore.md) verwenden. MAPI gibt den Speicher frei, indem die [MAPIFreeBuffer-Funktion](mapifreebuffer.md) nur aufgerufen wird, wenn **StatusRecips** erfolgreich ist. 
  
Eine Übersicht über Übermittlungs- und Unzustellbarkeitsberichte finden Sie unter [MAPI-Berichtsnachrichten.](mapi-report-messages.md)
  
## <a name="see-also"></a>Siehe auch



[ADRLIST](adrlist.md)
  
[IMAPISupport::Address](imapisupport-address.md)
  
[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IXPLogon::EndMessage](ixplogon-endmessage.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

