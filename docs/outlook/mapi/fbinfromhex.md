---
title: FBinFromHex
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.FBinFromHex
api_type:
- COM
ms.assetid: 47e6c576-bd99-4410-8e41-7dd3159b23b7
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 021336f54d6ca7b00ee6ccb434edc91067075a15
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596463"
---
# <a name="fbinfromhex"></a>FBinFromHex

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Konvertiert eine Zeichenfolgendarstellung einer Hexadezimalzahl in Binärdaten. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
```cpp
BOOL FBinFromHex(
  LPSTR sz,
  LPBYTE pb
);
```

## <a name="parameters"></a>Parameter

 _Sz_
  
> [in] Zeiger auf die ZU konvertierende ASCII-Zeichenfolge mit NULL-Termin. Es handelt sich nicht um eine Unicode-Zeichenfolge. Gültige Zeichen umfassen die Hexadezimalzeichen Null bis neun sowie die Groß- und Kleinbuchstaben A bis F.
    
 _pb_
  
> [out] Zeiger auf die zurückgegebene binäre Zahl.
    
## <a name="return-value"></a>Rückgabewert

TRUE 
  
> Die Zeichenfolge wurde erfolgreich in eine binäre Zahl konvertiert. 
    
FALSE 
  
> Die Eingabezeichenfolge enthält ungültige ASCII-Hexadezimalzeichen.
    
## <a name="see-also"></a>Siehe auch



[ScBinFromHexBounded](scbinfromhexbounded.md)

