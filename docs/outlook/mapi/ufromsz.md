---
title: UFromSz
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UFromSz
api_type:
- COM
ms.assetid: 4a67faa2-8c2e-49a7-8c92-690a0a65c8f7
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9947558975098316a547abfaefcdf5e7d4cd2f41
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439009"
---
# <a name="ufromsz"></a>UFromSz

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wandelt eine mit Null beendete Zeichenfolge von Dezimalstellen in eine ganze Zahl ohne Vorzeichen um. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
```cpp
UINT UFromSz(
  LPCSTR lpsz
);
```

## <a name="parameters"></a>Parameter

 _lpsz_
  
> [in] Zeiger auf die zu konvertierte Zeichenfolge mit Nullen terminiert. Der  _lpsz-Parameter_ darf 65536 Zeichen nicht überschreiten. 
    
## <a name="return-value"></a>Rückgabewert

 **UFromSz** gibt eine ganze Zahl ohne Vorzeichen zurück. Wenn die Zeichenfolge nicht mit mindestens einer Dezimalziffer beginnt, wird Null zurückgegeben. 
  
## <a name="remarks"></a>Hinweise

Die **UFromSz-Funktion** beendet die Konvertierung, wenn sie das erste Zeichen in der Zeichenfolge erreicht, das keine Dezimalziffer ist. Bei der Zeichenfolge "55" gibt **UFromSz** beispielsweise den ganzzahligen Wert 55 zurück. Angesichts der Zeichenfolge "5a5b" gibt die Funktion den ganzzahligen Wert 5 zurück. Angesichts der Zeichenfolge "a5b5" gibt **UFromSz** null zurück. 
  
 **UFromSz** ist für diakritische Unterschiede sensibel. Zeichenfolgen in den Formaten Unicode und DBCS werden unterstützt. Der Längengrenzwert für  _lpsz_ beträgt Zeichen, nicht unbedingt Byte. 
  

