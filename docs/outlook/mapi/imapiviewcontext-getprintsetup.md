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
ms.openlocfilehash: 63e3eca4e91e560a28d57f05250264d7e0592142
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587257"
---
# <a name="imapiviewcontextgetprintsetup"></a>IMAPIViewContext::GetPrintSetup

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Ruft die aktuellen Drucken von Informationen.
  
```cpp
HRESULT GetPrintSetup(
ULONG ulFlags,
LPFORMPRINTSETUP FAR * lppFormPrintSetup
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Bitmaske aus Flags, die den Typ des zurückgegebenen Zeichenfolgen steuert. Das folgende Flag kann festgelegt werden:
    
PARAMETER MAPI_UNICODE 
  
> Die zurückgegebenen Zeichenfolgen sind im Unicode-Format. Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.
    
 _lppFormPrintSetup_
  
> [out] Zeiger auf einen Zeiger auf eine Struktur, die die Drucken von Informationen enthält.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Drucken von Informationen wurde erfolgreich abgerufen.
    
## <a name="remarks"></a>HinwBemerkungeneise

Formularobjekte Aufrufen die **IMAPIViewContext::GetPrintSetup** -Methode zum Abrufen von Informationen zur Einrichtung Druckers bevor Sie versuchen, die aktuelle Nachricht zu drucken. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Ordnen Sie die **hDevMode-Feld** und **hDevName** Member der Struktur [FORMPRINTSETUP](formprintsetup.md) mithilfe der Win32-Funktion **GlobalAlloc**.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn Sie erwarten, die **hDevMode-Feld dass** und **hDevName** Member der Struktur **FORMPRINTSETUP** auf das durch den Parameter _LppFormPrintSetup_ Unicode-Zeichenfolgen werden, legen Sie _UlFlags_ auf Parameter MAPI_UNICODE. Andernfalls wird **GetPrintSetup** diese Zeichenfolgen in ANSI-Format zurückgegeben. 
  
Freigegeben Sie die **hDevMode-Feld** und **hDevName** Member der Struktur **FORMPRINTSETUP** durch Aufrufen der Win32-Funktion **GlobalFree**werden. Freigegeben Sie die gesamte Struktur **FORMPRINTSETUP** durch Aufrufen von [MAPIFreeBuffer](mapifreebuffer.md)werden. 
  
## <a name="see-also"></a>Siehe auch



[FORMPRINTSETUP](formprintsetup.md)
  
[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)

