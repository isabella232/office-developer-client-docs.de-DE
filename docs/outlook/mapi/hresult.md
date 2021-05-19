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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 64fcbebbd71bc3f478f36c711e49db9a3518ef9a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435019"
---
# <a name="hresult"></a>HRESULT

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein 32-Bit-Wert, der zum Beschreiben eines Fehlers oder einer Warnung verwendet wird.
  
```cpp
typedef LONG HRESULT;
```

## <a name="remarks"></a>Hinweise

Der **HRESULT-Datentyp** ist mit dem [SCODE-Datentyp](scode.md) identisch. 
  
Ein **HRESULT-Wert** besteht aus den folgenden Feldern: 
  
- Ein 1-Bit-Code, der den Schweregrad angibt, wobei Null den Erfolg und 1 den Fehler darstellt.
    
- Ein reservierter 4-Bit-Wert.
    
- Ein 11-Bit-Code, der die Verantwortung für den Fehler oder die Warnung angibt, auch als Einrichtungscode bezeichnet.
    
- Ein 16-Bit-Code, der den Fehler oder die Warnung beschreibt.
    
Die meisten METHODEN und Funktionen der MAPI-Schnittstelle geben **HRESULT-Werte zurück,** um eine detaillierte Ursachenbildung zu ermöglichen. **HRESULT-Werte** werden auch häufig in OLE-Schnittstellenmethoden verwendet. OLE stellt mehrere Makros für die Konvertierung zwischen **HRESULT-** und **SCODE-Werten** zur Auswahl, ein weiterer gängiger Datentyp für die Fehlerbehandlung. 
  
> [!NOTE]
> In 64-Bit-MAPI ist **HRESULT** immer noch ein 32-Bit-Wert. 
  
Informationen zur OLE-Verwendung von **HRESULT-Werten** finden Sie unter  *OLE Programmer's Reference*  . Weitere Informationen zur Verwendung dieser Werte in MAPI finden Sie unter [Fehlerbehandlung](error-handling-in-mapi.md) und eine der folgenden Schnittstellenmethoden: 
  
[IABLogon::GetLastError](iablogon-getlasterror.md)
  
[IMAPISupport::GetLastError](imapisupport-getlasterror.md)
  
[IMAPIControl::GetLastError](imapicontrol-getlasterror.md)
  
[IMAPITable::GetLastError](imapitable-getlasterror.md)
  
[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPIViewAdviseSink::OnPrint](imapiviewadvisesink-onprint.md)
  
## <a name="see-also"></a>Siehe auch



[SCODE](scode.md)


[MAPI-Datentypen](mapi-data-types.md)

