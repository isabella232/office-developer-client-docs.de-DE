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
ms.openlocfilehash: 55c7deec9d29ae22a07b2f5ccd1c832d56782c03
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414935"
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

 _sz_
  
> [in] Zeiger auf die mit Null beendete ASCII-Zeichenfolge, die konvertiert werden soll. Es handelt sich nicht um eine Unicode-Zeichenfolge. Gültige Zeichen sind die Hexadezimalzeichen Null bis neun sowie die Groß- und Kleinbuchstaben A bis F.
    
 _pb_
  
> [out] Zeiger auf die zurückgegebene Binärnummer.
    
## <a name="return-value"></a>Rückgabewert

TRUE 
  
> Die Zeichenfolge wurde erfolgreich in eine binäre Zahl konvertiert. 
    
FALSE 
  
> Die Eingabezeichenfolge enthält ungültige ASCII-Hexadezimalzeichen.
    
## <a name="see-also"></a>Siehe auch



[ScBinFromHexBounded](scbinfromhexbounded.md)

