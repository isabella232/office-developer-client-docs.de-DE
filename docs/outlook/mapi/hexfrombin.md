---
title: HexFromBin
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.HexFromBin
api_type:
- COM
ms.assetid: 12b95657-1926-4a24-be63-40305ea6f990
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 338f4336c0d229ccd5d336cdfdbd81f613be8848
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59604950"
---
# <a name="hexfrombin"></a>HexFromBin

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Konvertiert eine binäre Zahl in eine Zeichenfolgendarstellung einer Hexadezimalzahl. 
  
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
  
> [in] Zeiger auf die zu konvertierenden binären Daten. 
    
 _cb_
  
> [in] Größe der binären Daten, auf die durch den  _Pb-Parameter_ verwiesen wird, in Bytes. 
    
 _Sz_
  
> [out] Zeiger auf eine MIT NULL beendete ASCII-Zeichenfolge, die die binären Daten in Hexadezimalziffern darstellt.
    
## <a name="return-value"></a>Return value

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Die **HexFromBin-Funktion** verwendet einen Zeiger auf eine Einheit binärer Daten, deren Größe durch den  _cb-Parameter_ angegeben wird. Es gibt in der  _sz-Zeichenfolge_ innerhalb (2*  _CB_)+1 Byte Speicher eine Darstellung dieser binären Informationen in Hexadezimalzahlen zurück. Wenn der Bytewert z. B. dezimal 10 ist, ist die Hexadezimalzeichenfolge 0A, sodass ein Byte in zwei Bytes in der Zeichenfolge konvertiert wird. 
  

