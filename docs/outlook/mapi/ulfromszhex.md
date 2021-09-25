---
title: UlFromSzHex
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.UlFromSzHex
api_type:
- COM
ms.assetid: e2d6b6bf-f96d-460c-859a-21961ac9237c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7d545e93d9ebd746d50c1e5d4db55f2114551ca1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623992"
---
# <a name="ulfromszhex"></a>UlFromSzHex

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Konvertiert eine Zeichenfolge mit Null-Endung von Hexadezimalziffern in eine lange ganze Zahl ohne Vorzeichen. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
```cpp
ULONG UlFromSzHex(
LPCSTR lpsz
);
```

## <a name="parameters"></a>Parameter

 _lpsz_
  
> [in] Zeiger auf die Zeichenfolge, die mit NULL beendet wird und konvertiert werden soll. Der  _lpsz-Parameter_ darf 65536 Zeichen nicht überschreiten. 
    
## <a name="return-value"></a>Rückgabewert

 **UlFromSzHex** gibt eine ganze Zahl ohne Vorzeichen zurück. Wenn die Zeichenfolge nicht mit mindestens einer Hexadezimalziffer beginnt, wird Null zurückgegeben. 
  
## <a name="remarks"></a>Bemerkungen

Die **UlFromSzHex-Funktion** beendet die Konvertierung, wenn sie das erste Zeichen in der Zeichenfolge erreicht, bei dem es sich nicht um eine Hexadezimalzahl handelt. Wenn beispielsweise die Zeichenfolge "5a" angegeben wird, gibt **UlFromSzHex** den ganzzahligen Wert 90 zurück. Wenn die Zeichenfolge "5g5h" angegeben wird, gibt die Funktion den ganzzahligen Wert 5 zurück. Wenn die Zeichenfolge "g5h5" angegeben wird, gibt **UlFromSzHex** Null zurück. 
  
 **UlFromSzHex** reagiert auf diakritische Unterschiede, lässt jedoch sowohl "a" bis "f" als auch "A" bis "F" für Hexadezimalziffern zu. Zeichenfolgen im Unicode- und DBCS-Format werden unterstützt. Die Längenbeschränkung für  _lpsz_ ist in Zeichen angegeben, nicht unbedingt in Byte. 
  

