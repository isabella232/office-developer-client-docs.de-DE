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
  
Konvertiert eine binäre Zahl in eine Zeichenfolgendarstellung einer Hexadezimalzahl. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen und Dienstanbieter  <br/> |
   
```cpp
void HexFromBin(
  LPBYTE pb,
  int cb,
  LPSTR sz
);
```

## <a name="parameters"></a>Parameter

 _pb_
  
> in Zeiger auf die zu konvertierenden Binärdaten. 
    
 _cb_
  
> in Die Größe der Binärdaten, auf die durch den _PB_ -Parameter verwiesen wird, in Byte. 
    
 _SZ_
  
> Out Zeiger auf eine mit NULL endende ASCII-Zeichenfolge, die die Binärdaten in Hexadezimalziffern darstellt.
    
## <a name="return-value"></a>Return value

Keine.
  
## <a name="remarks"></a>Bemerkungen

Die **HexFromBin** -Funktion verwendet einen Zeiger auf eine Einheit von Binärdaten, deren Größe durch den _CB_ -Parameter angegeben wird. In der _SZ_ -Zeichenfolge wird innerhalb von (2 * _CB_) + 1 Byte des Arbeitsspeichers eine Darstellung dieser Binärinformationen in Hexadezimalzahlen zurückgegeben. Wenn der Byte-Wert dezimal 10 ist, wird beispielsweise die hexadezimale Zeichenfolge 0A, sodass ein Byte in zwei Bytes in der Zeichenfolge konvertiert. 
  

