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
ms.openlocfilehash: 8f68de5e18d84c728241c188b932f99456f5be8c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584835"
---
# <a name="hexfrombin"></a>HexFromBin

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
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
  
## <a name="remarks"></a>HinwBemerkungeneise

Die **HexFromBin** -Funktion verwendet einen Zeiger auf einer Einheit von binären Daten, deren Größe von der _Cb_ -Parameter angegeben ist. Es gibt in der Zeichenfolge _su_ innerhalb (2 * _Cb_) + 1 Byte an Arbeitsspeicher, eine Darstellung dieses Binärdaten in Hexadezimalzahlen. Wenn der Bytewert Dezimalzahl 10 ist, beispielsweise werden die hexadezimale Zeichenfolge 0A, dies der Fall ist ein Byte in die beiden Bytes in der Zeichenfolge konvertiert. 
  

