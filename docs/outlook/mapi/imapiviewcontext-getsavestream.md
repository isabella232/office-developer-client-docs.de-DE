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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351121"
---
# <a name="imapiviewcontextgetsavestream"></a>IMAPIViewContext::GetSaveStream

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ruft einen Stream ab, der zum Speichern der aktuellen Nachricht verwendet werden soll.
  
```cpp
HRESULT GetSaveStream(
ULONG FAR * pulFlags,
ULONG FAR * pulFormat,
LPSTREAM FAR * ppstm
);
```

## <a name="parameters"></a>Parameter

 _pulFlags_
  
> Out Zeiger auf eine Bitmaske von Flags, die steuert, wie der Nachrichtentext gespeichert werden soll. Das folgende Flag kann festgelegt werden:
    
MAPI_UNICODE 
  
> Der Nachrichtentext wird im Unicode-Format gespeichert. Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, wird der Text im ANSI-Format gespeichert.
    
 _pulFormat_
  
> Out Zeiger auf eine Bitmaske von Flags, die das Format des gespeicherten Texts steuert. Die folgenden Flags können festgelegt werden:
    
SAVE_FORMAT_RICHTEXT 
  
> Der Nachrichtentext soll als formatierter Text im Rich-Text-Format (RTF) gespeichert werden. 
    
SAVE_FORMAT_TEXT 
  
> Der Nachrichtentext soll als nur-Text gespeichert werden. 
    
 _ppstm_
  
> Out Zeiger auf einen Zeiger auf den Stream, der die gespeicherte Nachricht enthält.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Datenstrom wurde erfolgreich abgerufen.
    
## <a name="remarks"></a>Bemerkungen

Formularobjekte rufen die **IMAPIViewContext:: GetSaveStream** -Methode auf, um ein Stream-Objekt abzurufen, das die **IStream** -Schnittstelle implementiert, um die Behandlung des Save as-Verbs im Formular-Viewer zu unterstützen. Die [IMAPIForm::D overb](imapiform-doverb.md) -Methode, die auf dem Formularserver implementiert und vom Formular Betrachter aufgerufen wird, um ein Verb aufzurufen, sollte erst zurückgegeben werden, wenn die Nachricht vollständig in das entsprechende Text Format konvertiert und in den entsprechenden Stream verschoben wurde. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Schreiben Sie nicht in den Stream, auf den von _ppstm_ verwiesen wird, bevor Sie **GetSaveStream**aufrufen. Wenn **GetSaveStream** zurückgegeben wird, setzen Sie die Position des Seek-Zeigers nicht zurück. Dieser Zeiger muss am Ende des gespeicherten Nachrichtentexts bleiben. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)

