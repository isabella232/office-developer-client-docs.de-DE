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
ms.openlocfilehash: e8c52d71ee47966be09c6c0806eceafae0c5ff5b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411190"
---
# <a name="imapisupportcompletemsg"></a>IMAPISupport::CompleteMsg

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Führt die Nachverarbeitung für eine Nachricht durch. 
  
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
  
> [in] Die Byteanzahl im Eintragsbezeichner, auf den der  _lpEntryID-Parameter_ verweist. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf die Eintrags-ID der zu verarbeitende Nachricht.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Nachverarbeitung war erfolgreich.
    
## <a name="remarks"></a>Hinweise

Die **IMAPISupport::CompleteMsg-Methode** wird für Unterstützungsobjekte des Nachrichtenspeicheranbieters implementiert und nur von Nachrichtenspeicheranbietern aufgerufen, die eng mit Transportanbietern gekoppelt sind. Eng gekoppelte Speicheranbieter rufen **IMAPISupport::CompleteMsg** auf, um den MAPI-Spooler anweisen, eine Nachricht nachverarbeitet zu haben. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Rufen **Sie CompleteMsg** nur auf, wenn Sie eng mit einem Transportanbieter gekoppelt sind, Sie alle Empfänger der Nachricht behandeln können, und eine der folgenden Bedingungen ist vorhanden: 
  
- Die Nachricht wurde vorverarbeitet.
    
- Die Nachricht erfordert die Nachverarbeitung durch den MAPI-Spooler.
    
## <a name="see-also"></a>Siehe auch



[IMAPISupport: IUnknown](imapisupportiunknown.md)

