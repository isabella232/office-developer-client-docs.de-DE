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
  
Generiert Unzustellbarkeitsberichte.
  
```cpp
HRESULT StatusRecips(
LPMESSAGE lpMessage,
LPADRLIST lpRecipList
);
```

## <a name="parameters"></a>Parameter

 _lpMessage_
  
> in Ein Zeiger auf die Nachricht, für die der Bericht generiert werden soll.
    
 _lpRecipList_
  
> in Ein Zeiger auf eine [ADRLIST](adrlist.md) -Struktur, die die Empfänger der Nachricht beschreibt, auf die von _lpMessage_verwiesen wird.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Bericht wurde erfolgreich generiert.
    
MAPI_W_ERRORS_RETURNED 
  
> Der Anruf war insgesamt erfolgreich, aber es gibt keine Empfängeroptionen für diesen Empfängertyp. Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden. Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** -Makro. Weitere Informationen finden Sie unter [Verwenden von Makros zur Fehlerbehandlung](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISupport:: StatusRecips** -Methode wird für Support Objekte des Transportanbieters implementiert. Transport Anbieter rufen **StatusRecips** auf, um anzufordern, dass MAPI einen Zustellungs-oder Unzustellbarkeitsbericht an eine Gruppe von einem oder mehreren Empfängern einer Nachricht sendet. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie können **StatusRecips** während der Verarbeitung einer Nachricht mehrmals aufrufen. Wenn Sie jedoch **StatusRecips** für eine offene Nachricht aufrufen, sollten Sie alle zugestellten und nicht zugestellten Informationen für die Nachrichtenempfänger erfassen und **StatusRecips** für diese Empfängerliste aufrufen. Ein einzelner Sammlungspunkt ist wichtig, da mehrere **StatusRecips** -Aufrufe für einen Empfänger dazu führen können, dass mehrere identische Berichte gesendet werden. 
  
Speichern von Eigenschaften, die sich auf die Nachrichtenübermittlung oder Nichtübermittlung beziehen, in der **ADRLIST** -Struktur, die durch den _lpRecipList_ -Parameter angegeben wird. Eine vollständige Liste der erforderlichen und optionalen Eigenschaften für Zustellungsberichte und Unzustellbarkeitsberichte finden Sie unter erforderliche Eigenschaften für [Berichtsnachrichten](required-report-message-properties.md) und [optionale Berichtnachrichten Eigenschaften](optional-report-message-properties.md). 
  
Zuweisen von Arbeitsspeicher für die **ADRLIST** -Struktur in _LpRecipList_ mithilfe der [MAPIAllocateBuffer](mapiallocatebuffer.md) -und [MAPIAllocateMore](mapiallocatemore.md) -Funktionen. MAPI gibt den Arbeitsspeicher frei, indem die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion nur aufgerufen wird, wenn **StatusRecips** erfolgreich ausgeführt wird. 
  
Eine Übersicht über Zusteller-und Unzustellbarkeitsberichte finden Sie unter [MAPI Report Messages](mapi-report-messages.md).
  
## <a name="see-also"></a>Siehe auch



[ADRLIST](adrlist.md)
  
[IMAPISupport::Address](imapisupport-address.md)
  
[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IXPLogon::EndMessage](ixplogon-endmessage.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

