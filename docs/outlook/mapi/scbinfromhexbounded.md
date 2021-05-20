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
ms.openlocfilehash: 813fab28e3e865c9f04f85c854b292ce7229dad5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439758"
---
# <a name="scbinfromhexbounded"></a>ScBinFromHexBounded

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wandelt den angegebenen Teil einer Zeichenfolgendarstellung einer Hexadezimalzahl in eine binäre Zahl um. 
  
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

 _sz_
  
> [in] Zeiger auf die zu konvertierte Zeichenfolge mit Nullen terminiert. Gültige Zeichen sind die Hexadezimalzeichen 0 bis 9 sowie Groß- und Kleinbuchstaben a bis f.
    
 _pb_
  
> [out] Zeiger auf die zurückgegebene Binärnummer.
    
 _cb_
  
> [in] Größe des pb-Parameters  in Bytes. 
    
## <a name="return-value"></a>Rückgabewert

S_OK
  
> Die Konvertierung war erfolgreich.
    
MAPI_E_CALL_FAILED
  
> Es wurden ungültige Zeichen gefunden.
    
## <a name="see-also"></a>Siehe auch



[FBinFromHex](fbinfromhex.md)

