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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 950f5513696a9dd9d52db7b7ee912d3f7d12cc48
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433052"
---
# <a name="ulfromszhex"></a>UlFromSzHex

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wandelt eine mit Null beendete Zeichenfolge von Hexadezimalziffern in eine nicht signierte lange ganze Zahl um. 
  
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
  
> [in] Zeiger auf die zu konvertierte Zeichenfolge mit Nullen terminiert. Der  _lpsz-Parameter_ darf 65536 Zeichen nicht überschreiten. 
    
## <a name="return-value"></a>Rückgabewert

 **UlFromSzHex gibt** eine nicht signierte lange ganze Zahl zurück. Wenn die Zeichenfolge nicht mit mindestens einer hexadezimalen Ziffer beginnt, wird Null zurückgegeben. 
  
## <a name="remarks"></a>Hinweise

Die **UlFromSzHex-Funktion** beendet die Konvertierung, wenn sie das erste Zeichen in der Zeichenfolge erreicht, das keine hexadezimale Ziffer ist. Wenn beispielsweise die Zeichenfolge "5a" angegeben wird, gibt **UlFromSzHex** den ganzzahligen Wert 90 zurück. Angesichts der Zeichenfolge "5g5h" gibt die Funktion den ganzzahligen Wert 5 zurück. Angesichts der Zeichenfolge "g5h5" gibt **UlFromSzHex** null zurück. 
  
 **UlFromSzHex** ist für diakritische Unterschiede sensibel, ermöglicht jedoch sowohl "a" über "f" als auch "A" bis "F" für Hexadezimalziffern. Zeichenfolgen in den Formaten Unicode und DBCS werden unterstützt. Der Längengrenzwert für  _lpsz_ beträgt Zeichen, nicht unbedingt Byte. 
  

