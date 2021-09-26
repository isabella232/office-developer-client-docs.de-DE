---
title: ScBinFromHexBounded
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.ScBinFromHexBounded
api_type:
- COM
ms.assetid: edac715c-6edb-4b05-82e5-c08c3c7cb6d4
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 4afb140d8c273d274b4d8e7417c39e6dffb97764
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59599039"
---
# <a name="scbinfromhexbounded"></a>ScBinFromHexBounded

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Konvertiert den angegebenen Teil einer Zeichenfolgendarstellung einer Hexadezimalzahl in eine binäre Zahl. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
```cpp
SCODE ScBinFromHexBounded(
  LPSTR sz,
  LPBYTE pb,
  ULONG cb
);
```

## <a name="parameters"></a>Parameter

 _Sz_
  
> [in] Zeiger auf die Zeichenfolge, die mit NULL beendet wird und konvertiert werden soll. Gültige Zeichen umfassen die Hexadezimalzeichen 0 bis 9 und die Groß- und Kleinbuchstaben a bis f.
    
 _pb_
  
> [out] Zeiger auf die zurückgegebene binäre Zahl.
    
 _cb_
  
> [in] Größe des  _PB-Parameters_ in Bytes. 
    
## <a name="return-value"></a>Rückgabewert

S_OK
  
> Die Konvertierung war erfolgreich.
    
MAPI_E_CALL_FAILED
  
> Ungültige Zeichen wurden gefunden.
    
## <a name="see-also"></a>Siehe auch



[FBinFromHex](fbinfromhex.md)

