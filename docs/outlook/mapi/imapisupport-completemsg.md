---
title: IMAPISupportCompleteMsg
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.CompleteMsg
api_type:
- COM
ms.assetid: e7932433-abe0-4341-95e0-91b37c848145
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 87640445c1243f6725c42fbc0a20f77f54e45dde
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625441"
---
# <a name="imapisupportcompletemsg"></a>IMAPISupport::CompleteMsg

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Führt eine Nachverarbeitung für eine Nachricht aus. 
  
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
  
> [in] Ein Zeiger auf den Eintragsbezeichner der zu verarbeitenden Nachricht.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Nachbearbeitung war erfolgreich.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISupport::CompleteMsg-Methode** ist für Supportobjekte des Nachrichtenspeicheranbieters implementiert und wird nur von Nachrichtenspeicheranbietern aufgerufen, die eng mit Transportanbietern gekoppelt sind. Eng gekoppelte Speicheranbieter rufen **IMAPISupport::CompleteMsg** auf, um den MAPI-Spooler anzuweisen, eine Nachricht nachzuverarbeiten. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Rufen Sie **CompleteMsg** nur auf, wenn Sie eng mit einem Transportanbieter verbunden sind, können Sie alle Empfänger der Nachricht behandeln, und eine der folgenden Bedingungen ist vorhanden: 
  
- Die Nachricht wurde vorverarbeitet.
    
- Die Nachricht erfordert eine Nachverarbeitung durch den MAPI-Spooler.
    
## <a name="see-also"></a>Siehe auch



[IMAPISupport: IUnknown](imapisupportiunknown.md)

