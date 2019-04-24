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
ms.openlocfilehash: 950f5513696a9dd9d52db7b7ee912d3f7d12cc48
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315365"
---
# <a name="ulfromszhex"></a>UlFromSzHex

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Konvertiert eine NULL-terminierte Zeichenfolge mit Hexadezimalziffern in eine nicht signierte lange ganze Zahl. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen und Dienstanbieter  <br/> |
   
```cpp
ULONG UlFromSzHex(
LPCSTR lpsz
);
```

## <a name="parameters"></a>Parameter

 _lpsz_
  
> in Zeiger auf die zu konvertierende NULL-terminierte Zeichenfolge. Der _lpsz_ -parameter darf 65536 Zeichen nicht überschreiten. 
    
## <a name="return-value"></a>Rückgabewert

 **UlFromSzHex** gibt eine lange ganze Zahl ohne Vorzeichen zurück. Wenn die Zeichenfolge nicht mit mindestens einer Hexadezimalzahl beginnt, wird NULL zurückgegeben. 
  
## <a name="remarks"></a>Bemerkungen

Die **UlFromSzHex** -Funktion wird nicht mehr konvertiert, wenn Sie das erste Zeichen in der Zeichenfolge erreicht, die keine hexadezimale Ziffer ist. Beispiel: bei der Zeichenfolge "5A" gibt **UlFromSzHex** den ganzzahligen Wert 90 zurück. Bei der Zeichenfolge "5g5h" gibt die Funktion den ganzzahligen Wert 5 zurück. Bei der Zeichenfolge "g5h5" gibt **UlFromSzHex** NULL zurück. 
  
 **UlFromSzHex** ist anfällig für diakritische Unterschiede, ermöglicht jedoch sowohl "a" bis "f" als auch "a" bis "f" für Hexadezimalziffern. Zeichenfolgen im Unicode-und DBCS-Format werden unterstützt. Die Längenbeschränkung für _lpsz_ ist in Zeichen, nicht unbedingt in Bytes. 
  

