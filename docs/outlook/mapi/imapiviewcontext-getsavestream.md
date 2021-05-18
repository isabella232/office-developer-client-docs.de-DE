---
title: IMAPIViewContextGetSaveStream
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.GetSaveStream
api_type:
- COM
ms.assetid: 8316bfa1-3077-401f-aa1e-e9492aca12a8
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 68eb74f53d6cee4661c98604ec2ea37609e20ab5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408425"
---
# <a name="imapiviewcontextgetsavestream"></a>IMAPIViewContext::GetSaveStream

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ruft einen Datenstrom ab, der zum Speichern der aktuellen Nachricht verwendet werden soll.
  
```cpp
HRESULT GetSaveStream(
ULONG FAR * pulFlags,
ULONG FAR * pulFormat,
LPSTREAM FAR * ppstm
);
```

## <a name="parameters"></a>Parameter

 _pulFlags_
  
> [out] Zeiger auf eine Bitmaske mit Flags, die steuert, wie der Nachrichtentext gespeichert werden soll. Das folgende Flag kann festgelegt werden:
    
MAPI_UNICODE 
  
> Der Nachrichtentext wird im Unicode-Format gespeichert. Wenn das MAPI_UNICODE nicht festgelegt ist, wird der Text im ANSI-Format gespeichert.
    
 _pulFormat_
  
> [out] Zeiger auf eine Bitmaske mit Flags, die das Format des gespeicherten Texts steuert. Die folgenden Kennzeichen können festgelegt werden:
    
SAVE_FORMAT_RICHTEXT 
  
> Der Nachrichtentext soll als formatierter Text im Rich Text Format (RTF) gespeichert werden. 
    
SAVE_FORMAT_TEXT 
  
> Der Nachrichtentext soll als Nur-Text-Text gespeichert werden. 
    
 _ppstm_
  
> [out] Zeiger auf einen Zeiger auf den Datenstrom, der die gespeicherte Nachricht enthält.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Datenstrom wurde erfolgreich abgerufen.
    
## <a name="remarks"></a>Hinweise

Form-Objekte rufen die **IMAPIViewContext::GetSaveStream-Methode** auf, um ein Datenstromobjekt abzurufen, das die **IStream-Schnittstelle** implementiert, um die Behandlung des Verbs Speichern unter in der Formularanzeige zu unterstützen. Die [IMAPIForm::D oVerb-Methode,](imapiform-doverb.md) die im Formularserver implementiert und von der Formularanzeige zum Aufrufen eines Verbs aufgerufen wird, sollte erst zurückkehren, wenn die Nachricht vollständig in das entsprechende Textformat konvertiert und in den entsprechenden Datenstrom platziert wurde. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Schreiben Sie nicht in den Datenstrom, auf den _ppstm verweist,_ bevor **Sie GetSaveStream aufrufen.** Wenn **GetSaveStream zurückgegeben** wird, setzen Sie die Position des Suchzeigers nicht zurück. Dieser Zeiger muss am Ende des gespeicherten Nachrichtentexts verbleiben. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)

