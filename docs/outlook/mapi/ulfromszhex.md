---
title: UlFromSzHex
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlFromSzHex
api_type:
- COM
ms.assetid: e2d6b6bf-f96d-460c-859a-21961ac9237c
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: d5ba7e7bc52ba041e9fe6c9a01b35dc91d3b947b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795786"
---
# <a name="ulfromszhex"></a>UlFromSzHex

  
  
**Betrifft**: Outlook 
  
Konvertiert eine mit Null endende Zeichenfolge von Hexadezimalzahlen in eine lange Ganzzahl ohne Vorzeichen. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
```cpp
ULONG UlFromSzHex(
LPCSTR lpsz
);
```

## <a name="parameters"></a>Parameter

 _lpsz_
  
> [in] Zeiger auf die Null-Zeichenfolge konvertiert werden soll. Der Parameter _Lpsz_ muss 65536 Zeichen nicht überschreiten. 
    
## <a name="return-value"></a>R�ckgabewert

 **UlFromSzHex** gibt eine lange Ganzzahl ohne Vorzeichen zurück. Wenn die Zeichenfolge nicht mit mindestens eine hexadezimale Ziffer beginnt, wird 0 (null) zurückgegeben. 
  
## <a name="remarks"></a>Hinweise

Die Funktion **UlFromSzHex** beendet konvertieren, wenn das erste Zeichen in der Zeichenfolge, die keine hexadezimale Ziffer ist erreicht. Beispielsweise gibt **UlFromSzHex** die Zeichenfolge "5a" wird angegeben, den Ganzzahlwert 90. Die Zeichenfolge "5g5h" angegeben, gibt die Funktion den ganzzahligen Wert 5 zurück. Wenn die Zeichenfolge "g5h5", gibt **UlFromSzHex** 0 (null) zurück. 
  
 **UlFromSzHex** wird entsprechend diakritischen Unterschiede ermöglicht aber auch "a" bis "f" und "A" bis "F" für Hexadezimalzahlen. In den Formaten Unicode und DBCS Zeichenfolgen werden unterstützt. Die maximale Länge _Lpsz_ ist in Zeichen, was nicht notwendigerweise Bytes. 
  

