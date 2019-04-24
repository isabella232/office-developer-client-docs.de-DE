---
title: ScBinFromHexBounded
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScBinFromHexBounded
api_type:
- COM
ms.assetid: edac715c-6edb-4b05-82e5-c08c3c7cb6d4
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 813fab28e3e865c9f04f85c854b292ce7229dad5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357498"
---
# <a name="scbinfromhexbounded"></a>ScBinFromHexBounded

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Konvertiert den angegebenen Teil einer Zeichenfolgendarstellung einer hexadezimalen Zahl in eine binäre Zahl. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen und Dienstanbieter  <br/> |
   
```cpp
SCODE ScBinFromHexBounded(
  LPSTR sz,
  LPBYTE pb,
  ULONG cb
);
```

## <a name="parameters"></a>Parameter

 _SZ_
  
> in Zeiger auf die zu konvertierende NULL-terminierte Zeichenfolge. Gültige Zeichen sind die Hexadezimalzeichen 0 bis 9 und groß-und Kleinbuchstaben a bis f.
    
 _pb_
  
> Out Zeiger auf die zurückgegebene binäre Zahl.
    
 _cb_
  
> in Die Größe des _PB_ -Parameters in Byte. 
    
## <a name="return-value"></a>Rückgabewert

S_OK
  
> Die Konvertierung war erfolgreich.
    
MAPI_E_CALL_FAILED
  
> Ungültige Zeichen wurden gefunden.
    
## <a name="see-also"></a>Siehe auch



[FBinFromHex](fbinfromhex.md)

