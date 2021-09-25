---
title: UFromSz
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.UFromSz
api_type:
- COM
ms.assetid: 4a67faa2-8c2e-49a7-8c92-690a0a65c8f7
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 49f921ddd26fc78cea9b9b1e5ad99e248f4409ac
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609250"
---
# <a name="ufromsz"></a>UFromSz

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Konvertiert eine Zeichenfolge mit null terminierten Dezimalziffern in eine ganze Zahl ohne Vorzeichen. 
  
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
  
> [in] Zeiger auf die Zeichenfolge, die mit NULL beendet wird und konvertiert werden soll. Der  _lpsz-Parameter_ darf 65536 Zeichen nicht überschreiten. 
    
## <a name="return-value"></a>Rückgabewert

 **UFromSz** gibt eine ganze Zahl ohne Vorzeichen zurück. Wenn die Zeichenfolge nicht mit mindestens einer Dezimalzahl beginnt, wird Null zurückgegeben. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Die **UFromSz-Funktion** beendet die Konvertierung, wenn sie das erste Zeichen in der Zeichenfolge erreicht, bei dem es sich nicht um eine Dezimalzahl handelt. Wenn beispielsweise die Zeichenfolge "55" angegeben wird, gibt **UFromSz** den ganzzahligen Wert 55 zurück. Wenn die Zeichenfolge "5a5b" angegeben wird, gibt die Funktion den ganzzahligen Wert 5 zurück. Wenn die Zeichenfolge "a5b5" angegeben wird, gibt **UFromSz** Null zurück. 
  
 **UFromSz** reagiert auf diakritische Unterschiede. Zeichenfolgen im Unicode- und DBCS-Format werden unterstützt. Die Längenbeschränkung für  _lpsz_ ist in Zeichen angegeben, nicht unbedingt in Byte. 
  

