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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: c1d333c7c019c30c3f6c6b3567453f2f022d4b5d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791859"
---
# <a name="hexfrombin"></a>HexFromBin

  
  
**Betrifft**: Outlook 
  
Konvertiert eine binäre Zahl in eine String-Darstellung eine hexadezimale Zahl. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
```cpp
void HexFromBin(
  LPBYTE pb,
  int cb,
  LPSTR sz
);
```

## <a name="parameters"></a>Parameter

 _pb_
  
> [in] Zeiger auf die binären Daten konvertiert werden soll. 
    
 _cb_
  
> [in] Größe in Bytes, die binären Daten, die durch den Parameter _pb_ auf. 
    
 _su_
  
> [out] Zeiger auf eine Null endende ASCII-Zeichenfolge, die binären Daten in Hexadezimalzahlen darstellt.
    
## <a name="return-value"></a>Rückgabewert

None.
  
## <a name="remarks"></a>Hinweise

Die **HexFromBin** -Funktion verwendet einen Zeiger auf einer Einheit von binären Daten, deren Größe von der _Cb_ -Parameter angegeben ist. Es gibt in der Zeichenfolge _su_ innerhalb (2 * _Cb_) + 1 Byte an Arbeitsspeicher, eine Darstellung dieses Binärdaten in Hexadezimalzahlen. Wenn der Bytewert Dezimalzahl 10 ist, beispielsweise werden die hexadezimale Zeichenfolge 0A, dies der Fall ist ein Byte in die beiden Bytes in der Zeichenfolge konvertiert. 
  

