---
title: IMAPIViewContextGetPrintSetup
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIViewContext.GetPrintSetup
api_type:
- COM
ms.assetid: eaf3bafb-975d-42c8-99ea-7f9ef9c934ba
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 58eccafa4faec96de0acacd4338798dba9f110d2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556462"
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
  
> [in] Bitmaske von Flags, die den Typ der zurückgegebenen Zeichenfolgen steuert. Das folgende Kennzeichen kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die zurückgegebenen Zeichenfolgen haben das Unicode-Format. Wenn das flag MAPI_UNICODE nicht festgelegt ist, haben die Zeichenfolgen das ANSI-Format.
    
 _lppFormPrintSetup_
  
> [out] Zeiger auf einen Zeiger auf eine Struktur, die die Druckinformationen enthält.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Druckinformationen wurden erfolgreich abgerufen.
    
## <a name="remarks"></a>HinwBemerkungeneise

Formularobjekte rufen die **IMAPIViewContext::GetPrintSetup-Methode** auf, um Informationen zum Druckersetup abzurufen, bevor versucht wird, die aktuelle Nachricht zu drucken. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Weisen Sie die **Elemente hDevMode** und **hDevName** der [FORMPRINTSETUP-Struktur](formprintsetup.md) mithilfe der Win32-Funktion **GlobalAlloc** zu.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn Sie erwarten, dass die **Elemente hDevMode** und **hDevName** der **FORMPRINTSETUP-Struktur,** auf die durch den  _Parameter lppFormPrintSetup_ verwiesen wird, Unicode-Zeichenfolgen sind, legen Sie  _ulFlags_ auf MAPI_UNICODE fest. Andernfalls gibt **GetPrintSetup** diese Zeichenfolgen im ANSI-Format zurück. 
  
Geben Sie die **Elemente hDevMode** und **hDevName** der **FORMPRINTSETUP-Struktur** frei, indem Sie die Win32-Funktion **GlobalFree** aufrufen. Geben Sie die gesamte **FORMPRINTSETUP-Struktur** frei, indem [Sie MAPIFreeBuffer](mapifreebuffer.md)aufrufen. 
  
## <a name="see-also"></a>Siehe auch



[FORMPRINTSETUP](formprintsetup.md)
  
[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)

