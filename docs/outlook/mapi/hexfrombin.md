---
title: HexFromBin
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HexFromBin
api_type:
- COM
ms.assetid: 12b95657-1926-4a24-be63-40305ea6f990
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a1bf02de914865e27c8c018aba8695c858888ae2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412576"
---
# <a name="hexfrombin"></a>HexFromBin

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wandelt eine binäre Zahl in eine Zeichenfolgendarstellung einer hexadezimalen Zahl um. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
```cpp
void HexFromBin(
  LPBYTE pb,
  int cb,
  LPSTR sz
);
```

## <a name="parameters"></a>Parameter

 _pb_
  
> [in] Zeiger auf die zu konvertierten Binärdaten. 
    
 _cb_
  
> [in] Größe der binären Daten, auf die  der pb-Parameter verweist, in Bytes. 
    
 _sz_
  
> [out] Zeiger auf eine mit Null beendete ASCII-Zeichenfolge, die die Binärdaten in hexadezimalen Ziffern darstellt.
    
## <a name="return-value"></a>Return value

Keine.
  
## <a name="remarks"></a>Hinweise

Die **HexFromBin-Funktion** verwendet einen Zeiger auf eine Binärdateneinheit, deren Größe durch den  _cb-Parameter angegeben_ wird. Es gibt in der  _sz-Zeichenfolge_ innerhalb (2*  _cb_)+1 Byte Arbeitsspeicher eine Darstellung dieser binären Informationen in hexadezimalen Zahlen zurück. Wenn der Bytewert z. B. dezimal 10 ist, ist die hexadezimale Zeichenfolge 0A, sodass ein Byte in zwei Bytes in der Zeichenfolge konvertiert wird. 
  

