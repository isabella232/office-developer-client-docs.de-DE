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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 135db8d690d4d4bd610bd15893c358fedddb4605
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589280"
---
# <a name="scbinfromhexbounded"></a>ScBinFromHexBounded

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
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

