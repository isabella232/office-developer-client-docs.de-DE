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
ms.openlocfilehash: a00a9b2200f76dfd600f72bf387467b5792599c6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795430"
---
# <a name="scbinfromhexbounded"></a>ScBinFromHexBounded

  
  
**Betrifft**: Outlook 
  
Konvertiert den angegebenen Teil einer Zeichenfolgendarstellung eine hexadezimale Zahl in eine binäre Zahl. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
```cpp
SCODE ScBinFromHexBounded(
  LPSTR sz,
  LPBYTE pb,
  ULONG cb
);
```

## <a name="parameters"></a>Parameter

 _su_
  
> [in] Zeiger auf die Null-Zeichenfolge konvertiert werden soll. Gültige Zeichen umfassen den Hexadezimalzeichen 0 bis 9 und beide Zeichen von Groß- und Kleinbuchstaben a bis f.
    
 _pb_
  
> [out] Zeiger auf das zurückgegebene binäre Zahl.
    
 _cb_
  
> [in] Größe des Parameters _pb_ in Bytes. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK
  
> Konvertierung erfolgreich war.
    
MAPI_E_CALL_FAILED
  
> Ungültige Zeichen sind aufgetreten.
    
## <a name="see-also"></a>Siehe auch



[FBinFromHex](fbinfromhex.md)

