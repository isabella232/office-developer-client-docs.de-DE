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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 9947558975098316a547abfaefcdf5e7d4cd2f41
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346536"
---
# <a name="ufromsz"></a>UFromSz

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Konvertiert eine NULL-terminierte Zeichenfolge von Dezimalstellen in eine unsignierte Ganzzahl. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen und Dienstanbieter  <br/> |
   
```cpp
UINT UFromSz(
  LPCSTR lpsz
);
```

## <a name="parameters"></a>Parameter

 _lpsz_
  
> in Zeiger auf die zu konvertierende NULL-terminierte Zeichenfolge. Der _lpsz_ -parameter darf 65536 Zeichen nicht überschreiten. 
    
## <a name="return-value"></a>Rückgabewert

 **UFromSz** gibt eine ganze Zahl ohne Vorzeichen zurück. Wenn die Zeichenfolge nicht mit mindestens einer Dezimalstelle beginnt, wird NULL zurückgegeben. 
  
## <a name="remarks"></a>Bemerkungen

Die **UFromSz** -Funktion wird nicht mehr konvertiert, wenn Sie das erste Zeichen in der Zeichenfolge erreicht, die keine Dezimalziffer ist. Beispiel: bei der Zeichenfolge "55" gibt **UFromSz** den ganzzahligen Wert 55 zurück. Bei der Zeichenfolge "5a5b" gibt die Funktion den ganzzahligen Wert 5 zurück. Bei der Zeichenfolge "a5b5" gibt **UFromSz** NULL zurück. 
  
 **UFromSz** ist anfällig für diakritische Unterschiede. Zeichenfolgen im Unicode-und DBCS-Format werden unterstützt. Die Längenbeschränkung für _lpsz_ ist in Zeichen, nicht unbedingt in Bytes. 
  

