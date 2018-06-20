---
title: HRESULT
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HRESULT
api_type:
- COM
ms.assetid: b248ed11-3d8a-4d4c-9b84-fa5bee7979c7
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5bacf3c73ba7f9a7720586c77ee520d289c40e11
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791905"
---
# <a name="hresult"></a>HRESULT

  
  
**Betrifft**: Outlook 
  
Ein 32-Bit-Wert, der verwendet wird, um einen Fehler oder eine Warnung zu beschreiben.
  
```cpp
typedef LONG HRESULT;
```

## <a name="remarks"></a>Hinweise

Der **HRESULT** -Datentyp ist identisch mit der [SCODE](scode.md) -Datentyp. 
  
Ein **HRESULT** -Wert besteht aus den folgenden Feldern: 
  
- Einen Schweregrad 1-Bit-Code, darstellt wobei 0 (null) Erfolg und 1 steht Fehler.
    
- Ein reserviertes 4-Bit-Wert.
    
- Ein 11-Bit-Code, der angibt, die Verantwortung für die Fehlermeldung oder einer Warnung, auch bekannt als einen Facility Code.
    
- Ein 16-Bit-Code Beschreibung des Fehlers oder eine Warnung ein.
    
Die meisten MAPI-Schnittstellenmethoden und Funktionen zurückgeben **HRESULT** -Werte, um ausführliche Ursache Bildung bereitzustellen. **HRESULT** -Werte werden auch in OLE-Schnittstellenmethoden großem Maß genutzt. OLE bietet mehrere Makros für die Konvertierung zwischen **HRESULT** -Werte und **SCODE** -Werte von einer anderen gemeinsamen Datentyp für die Fehlerbehandlung. 
  
> [!NOTE]
> In 64-Bit-MAPI ist **HRESULT** noch ein 32-Bit-Wert. 
  
Informationen über die Verwendung von OLE **HRESULT** -Werte finden Sie unter der *OLE Programmer's Reference* . Weitere Informationen zur Verwendung der folgenden Werte in MAPI finden Sie unter [Fehlerbehandlung](error-handling-in-mapi.md) und eine der folgenden Schnittstellenmethoden: 
  
[IABLogon::GetLastError](iablogon-getlasterror.md)
  
[IMAPISupport::GetLastError](imapisupport-getlasterror.md)
  
[IMAPIControl::GetLastError](imapicontrol-getlasterror.md)
  
[IMAPITable::GetLastError](imapitable-getlasterror.md)
  
[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPIViewAdviseSink::OnPrint](imapiviewadvisesink-onprint.md)
  
## <a name="see-also"></a>Siehe auch



[SCODE](scode.md)


[MAPI-Datentypen](mapi-data-types.md)

