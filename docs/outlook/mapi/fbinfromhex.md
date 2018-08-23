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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 87a470c1c682225eb1deefba9ccc8c12fbdc49c9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569827"
---
# <a name="fbinfromhex"></a>FBinFromHex

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
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

