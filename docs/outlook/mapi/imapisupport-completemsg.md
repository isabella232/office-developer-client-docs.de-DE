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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: db28d9684f1bb679ce36f99346f4ecc67a1a93e6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/21/2018
ms.locfileid: "19792352"
---
# <a name="imapisupportcompletemsg"></a>IMAPISupport::CompleteMsg

  
  
**Betrifft**: Outlook 
  
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
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISupport::CompleteMsg** -Methode wird für Message Store Anbieter Unterstützungsobjekte implementiert und heißt nur Zeichenfolgeneigenschaften Nachricht, die eng mit Anbietern Transport verknüpft sind. Anbieter eng gekoppelten Aufrufen **IMAPISupport::CompleteMsg** um anzuweisen, die MAPI-Warteschlange auf eine Nachricht zu bearbeiten. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Rufen Sie **CompleteMsg** nur, wenn Sie eng mit eines Transportdienstes verknüpft sind, Sie alle Empfänger der Nachricht behandeln können und eine der folgenden Bedingungen zutrifft: 
  
- Die Nachricht wurde vorverarbeitet.
    
- Die Nachricht muss Nachbearbeitung durch die MAPI-Warteschlange.
    
## <a name="see-also"></a>Siehe auch



[IMAPISupport: IUnknown](imapisupportiunknown.md)

