---
title: IMAPISupportCompleteMsg
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.CompleteMsg
api_type:
- COM
ms.assetid: e7932433-abe0-4341-95e0-91b37c848145
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a948c8c25eec9b31735bb34b91e2dec4bca5fcfc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583449"
---
# <a name="imapisupportcompletemsg"></a>IMAPISupport::CompleteMsg

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Führt Nachbearbeitung für eine Nachricht aus. 
  
```cpp
HRESULT CompleteMsg(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
 _cbEntryID_
  
> [in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LpEntryID_ verwiesen. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf die Eintrags-ID der Nachricht zu verarbeiten.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Nachbearbeitung war erfolgreich.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPISupport::CompleteMsg** -Methode wird für Message Store Anbieter Unterstützungsobjekte implementiert und heißt nur Zeichenfolgeneigenschaften Nachricht, die eng mit Anbietern Transport verknüpft sind. Anbieter eng gekoppelten Aufrufen **IMAPISupport::CompleteMsg** um anzuweisen, die MAPI-Warteschlange auf eine Nachricht zu bearbeiten. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Rufen Sie **CompleteMsg** nur, wenn Sie eng mit eines Transportdienstes verknüpft sind, Sie alle Empfänger der Nachricht behandeln können und eine der folgenden Bedingungen zutrifft: 
  
- Die Nachricht wurde vorverarbeitet.
    
- Die Nachricht muss Nachbearbeitung durch die MAPI-Warteschlange.
    
## <a name="see-also"></a>Siehe auch



[IMAPISupport: IUnknown](imapisupportiunknown.md)

