---
title: IMAPIViewContextGetPrintSetup
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.GetPrintSetup
api_type:
- COM
ms.assetid: eaf3bafb-975d-42c8-99ea-7f9ef9c934ba
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a58e723113f70c10b5c8468f5bdd0d8d9014bd2c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351125"
---
# <a name="imapiviewcontextgetprintsetup"></a>IMAPIViewContext::GetPrintSetup

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ruft aktuelle Druckinformationen ab.
  
```cpp
HRESULT GetPrintSetup(
ULONG ulFlags,
LPFORMPRINTSETUP FAR * lppFormPrintSetup
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> in Bitmaske von Flags, die den Typ der zurückgegebenen Zeichenfolgen steuert. Das folgende Flag kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die zurückgegebenen Zeichenfolgen sind im Unicode-Format. Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, werden die Zeichenfolgen im ANSI-Format.
    
 _lppFormPrintSetup_
  
> Out Zeiger auf einen Zeiger auf eine Struktur, die die Druckinformationen enthält.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Druckinformationen wurden erfolgreich abgerufen.
    
## <a name="remarks"></a>Bemerkungen

Formularobjekte rufen die **IMAPIViewContext:: GetPrintSetup** -Methode auf, um Informationen über die Druckereinrichtung abzurufen, bevor Sie versuchen, die aktuelle Nachricht zu drucken. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Weisen Sie die **hDevMode** -und **hDevName** -Member der [FORMPRINTSETUP](formprintsetup.md) -Struktur mithilfe der Win32-Funktion **GlobalAlloc**zu.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn Sie davon ausgehen, dass die **hDevMode** -und **hDevName** -Elemente der **FORMPRINTSETUP** -Struktur, auf die durch den _lppFormPrintSetup_ -Parameter verwiesen wird, Unicode-Zeichenfolgen sein sollen, legen Sie _ulFlags_ auf MAPI_UNICODE fest. Andernfalls gibt **GetPrintSetup** diese Zeichenfolgen im ANSI-Format zurück. 
  
Geben Sie die **hDevMode** -und **hDevName** -Member der **FORMPRINTSETUP** -Struktur frei, indem Sie die Win32-Funktion **GlobalFree**aufrufen. Freigeben der gesamten **FORMPRINTSETUP** -Struktur durch Aufrufen von [mapifreebufferfreigegeben](mapifreebuffer.md). 
  
## <a name="see-also"></a>Siehe auch



[FORMPRINTSETUP](formprintsetup.md)
  
[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)

