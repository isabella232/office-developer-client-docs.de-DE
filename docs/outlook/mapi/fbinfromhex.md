---
title: FBinFromHex
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBinFromHex
api_type:
- COM
ms.assetid: 47e6c576-bd99-4410-8e41-7dd3159b23b7
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 55c7deec9d29ae22a07b2f5ccd1c832d56782c03
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341643"
---
# <a name="fbinfromhex"></a>FBinFromHex

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Konvertiert eine Zeichenfolgendarstellung einer hexadezimalen Zahl in Binärdaten. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen und Dienstanbieter  <br/> |
   
```cpp
BOOL FBinFromHex(
  LPSTR sz,
  LPBYTE pb
);
```

## <a name="parameters"></a>Parameter

 _SZ_
  
> in Zeiger auf die zu konvertierende NULL-terminierte ASCII-Zeichenfolge. Es handelt sich nicht um eine Unicode-Zeichenfolge. Gültige Zeichen sind die Hexadezimalzeichen 0 bis 9 und groß-und Kleinbuchstaben A bis F.
    
 _pb_
  
> Out Zeiger auf die zurückgegebene binäre Zahl.
    
## <a name="return-value"></a>Rückgabewert

TRUE 
  
> Die Zeichenfolge wurde erfolgreich in eine binäre Zahl konvertiert. 
    
FALSE 
  
> Die Eingabezeichenfolge enthält ungültige ASCII-Hexadezimalzeichen.
    
## <a name="see-also"></a>Siehe auch



[ScBinFromHexBounded](scbinfromhexbounded.md)

