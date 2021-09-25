---
title: IMAPIViewContextGetSaveStream
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIViewContext.GetSaveStream
api_type:
- COM
ms.assetid: 8316bfa1-3077-401f-aa1e-e9492aca12a8
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ae363eafc089d5af3f9f45a575d220c63ca2e4ff
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600848"
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
  
> [out] Zeiger auf eine Bitmaske mit Flags, die steuert, wie der Nachrichtentext gespeichert werden soll. Das folgende Kennzeichen kann festgelegt werden:
    
MAPI_UNICODE 
  
> Der Nachrichtentext wird im Unicode-Format gespeichert. Wenn das flag MAPI_UNICODE nicht festgelegt ist, wird der Text im ANSI-Format gespeichert.
    
 _pulFormat_
  
> [out] Zeiger auf eine Bitmaske mit Flags, die das Format des gespeicherten Texts steuert. Die folgenden Flags können festgelegt werden:
    
SAVE_FORMAT_RICHTEXT 
  
> Der Nachrichtentext soll als formatierter Text im RTF -Format (Rich Text Format) gespeichert werden. 
    
SAVE_FORMAT_TEXT 
  
> Der Nachrichtentext soll als Nur-Text gespeichert werden. 
    
 _ppstm_
  
> [out] Zeiger auf einen Zeiger auf den Datenstrom, der die gespeicherte Nachricht enthält.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Datenstrom wurde erfolgreich abgerufen.
    
## <a name="remarks"></a>HinwBemerkungeneise

Formularobjekte rufen die **IMAPIViewContext::GetSaveStream-Methode** auf, um einen Datenstrom abzurufen, der die **IStream-Schnittstelle** implementiert, um die Verarbeitung des Verbs "Speichern unter" im Formularviewer zu unterstützen. Die [IMAPIForm::D oVerb-Methode,](imapiform-doverb.md) die im Formularserver implementiert und vom Formularviewer aufgerufen wird, um ein Verb aufzurufen, sollte erst zurückgegeben werden, wenn die Nachricht vollständig in das entsprechende Textformat konvertiert und in den entsprechenden Datenstrom eingefügt wird. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Schreiben Sie nicht in den Datenstrom, auf den  _ppstm verweist,_ bevor **Sie GetSaveStream** aufrufen. Wenn **GetSaveStream** zurückgegeben wird, setzen Sie die Position des Suchzeigers nicht zurück. Dieser Zeiger muss am Ende des gespeicherten Nachrichtentexts verbleiben. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)

