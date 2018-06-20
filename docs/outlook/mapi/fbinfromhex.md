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
ms.openlocfilehash: 64d205ee7f51c0ce6a6eb1e982659c6cda675f8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791680"
---
# <a name="fbinfromhex"></a>FBinFromHex

  
  
**Betrifft**: Outlook 
  
Zeichenfolgendarstellung einer eine hexadezimale Zahl konvertiert um Binärdaten. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
```cpp
BOOL FBinFromHex(
  LPSTR sz,
  LPBYTE pb
);
```

## <a name="parameters"></a>Parameter

 _su_
  
> [in] Zeiger auf Null endende ASCII-Zeichenfolge konvertiert werden soll. Es ist keine Unicode-Zeichenfolge. Gültige Zeichen umfassen die Hexadezimalzeichen 0 (null) bis neun und sowohl Groß- und Kleinbuchstaben Zeichen A bis F.
    
 _pb_
  
> [out] Zeiger auf das zurückgegebene binäre Zahl.
    
## <a name="return-value"></a>R�ckgabewert

TRUE 
  
> Die Zeichenfolge wurde erfolgreich in eine binäre Zahl konvertiert. 
    
FALSE 
  
> Die eingegebene Zeichenfolge enthält ungültige hexadezimale ASCII-Zeichen.
    
## <a name="see-also"></a>Siehe auch



[ScBinFromHexBounded](scbinfromhexbounded.md)

