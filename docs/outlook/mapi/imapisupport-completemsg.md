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
  
Führt die Nachbearbeitung für eine Nachricht aus. 
  
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
  
> in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEntryID_ -Parameter verwiesen wird. 
    
 _lpEntryID_
  
> in Ein Zeiger auf die Eintrags-ID der zu verarbeitenden Nachricht.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Nachbearbeitung war erfolgreich.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISupport:: CompleteMsg** -Methode wird für Nachrichtenspeicher Anbieter-Support Objekte implementiert und nur von Nachrichtenspeicher Anbietern aufgerufen, die eng mit Transportanbietern verbunden sind. Eng gekoppelte Speicheranbieter rufen **IMAPISupport:: CompleteMsg** auf, um den MAPI-Spooler anzuweisen, eine Nachricht zu senden. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

**CompleteMsg** nur aufrufen, wenn Sie eng mit einem Transportanbieter verbunden sind, können Sie alle Empfänger der Nachricht verarbeiten, und eine der folgenden Bedingungen ist vorhanden: 
  
- Die Nachricht wurde vorverarbeitet.
    
- Die Nachricht erfordert die Nachbearbeitung durch den MAPI-Spooler.
    
## <a name="see-also"></a>Siehe auch



[IMAPISupport: IUnknown](imapisupportiunknown.md)

