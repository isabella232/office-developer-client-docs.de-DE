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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425127"
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
  
> [in] Bitmaske von Flags, die den Typ der zurückgegebenen Zeichenfolgen steuert. Das folgende Flag kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die zurückgegebenen Zeichenfolgen sind im Unicode-Format. Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgen im ANSI-Format.
    
 _lppFormPrintSetup_
  
> [out] Zeiger auf einen Zeiger auf eine Struktur, die die Druckinformationen enthält.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Druckinformationen wurden erfolgreich abgerufen.
    
## <a name="remarks"></a>Hinweise

Formularobjekte rufen die **IMAPIViewContext::GetPrintSetup-Methode** auf, um Informationen zum Druckersetup abzurufen, bevor versucht wird, die aktuelle Nachricht zu drucken. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Weisen Sie **die Mitglieder hDevMode** und **hDevName** der [FORMPRINTSETUP-Struktur](formprintsetup.md) mithilfe der Win32-Funktion **GlobalAlloc zu.**
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn Sie erwarten, dass **die Elemente hDevMode** und **hDevName** der **FORMPRINTSETUP-Struktur,** auf die der  _lppFormPrintSetup-Parameter_ verweist, Unicode-Zeichenfolgen sind, legen Sie  _ulFlags_ auf MAPI_UNICODE. Andernfalls **gibt GetPrintSetup** diese Zeichenfolgen im ANSI-Format zurück. 
  
Geben Sie **die Mitglieder hDevMode** und **hDevName** der **FORMPRINTSETUP-Struktur** frei, indem Sie die Win32-Funktion **GlobalFree aufrufen.** Geben Sie die gesamte **FORMPRINTSETUP-Struktur** frei, indem Sie [MAPIFreeBuffer aufrufen.](mapifreebuffer.md) 
  
## <a name="see-also"></a>Siehe auch



[FORMPRINTSETUP](formprintsetup.md)
  
[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)

