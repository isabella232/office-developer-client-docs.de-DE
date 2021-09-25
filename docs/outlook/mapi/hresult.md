---
title: HRESULT
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.HRESULT
api_type:
- COM
ms.assetid: b248ed11-3d8a-4d4c-9b84-fa5bee7979c7
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ee2ef6d3f8b61c5cf140f29fb97342033b4777a2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571934"
---
# <a name="hresult"></a>HRESULT

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein 32-Bit-Wert, der verwendet wird, um einen Fehler oder eine Warnung zu beschreiben.
  
```cpp
typedef LONG HRESULT;
```

## <a name="remarks"></a>HinwBemerkungeneise

Der **HRESULT-Datentyp** ist identisch mit dem [SCODE-Datentyp.](scode.md) 
  
Ein **HRESULT-Wert** besteht aus den folgenden Feldern: 
  
- Ein 1-Bit-Code, der den Schweregrad angibt, wobei Null den Erfolg und 1 den Fehler darstellt.
    
- Ein reservierter 4-Bit-Wert.
    
- Ein 11-Bit-Code, der die Verantwortung für den Fehler oder die Warnung angibt, auch als Einrichtungscode bezeichnet.
    
- Ein 16-Bit-Code, der den Fehler oder die Warnung beschreibt.
    
Die meisten MAPI-Schnittstellenmethoden und -Funktionen geben **HRESULT-Werte** zurück, um eine detaillierte Ursache bereitzustellen. **HRESULT-Werte** werden auch häufig in OLE-Schnittstellenmethoden verwendet. OLE stellt mehrere Makros für die Konvertierung zwischen **HRESULT-Werten** und **SCODE-Werten** bereit, ein weiterer allgemeiner Datentyp für die Fehlerbehandlung. 
  
> [!NOTE]
> In der 64-Bit-MAPI ist **HRESULT** immer noch ein 32-Bit-Wert. 
  
Informationen zur OLE-Verwendung von **HRESULT-Werten** finden Sie in der *OLE-Programmierreferenz.* Weitere Informationen zur Verwendung dieser Werte in der MAPI finden Sie unter ["Fehlerbehandlung"](error-handling-in-mapi.md) und einer der folgenden Schnittstellenmethoden: 
  
[IABLogon::GetLastError](iablogon-getlasterror.md)
  
[IMAPISupport::GetLastError](imapisupport-getlasterror.md)
  
[IMAPIControl::GetLastError](imapicontrol-getlasterror.md)
  
[IMAPITable::GetLastError](imapitable-getlasterror.md)
  
[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPIViewAdviseSink::OnPrint](imapiviewadvisesink-onprint.md)
  
## <a name="see-also"></a>Siehe auch



[SCODE](scode.md)


[MAPI-Datentypen](mapi-data-types.md)

