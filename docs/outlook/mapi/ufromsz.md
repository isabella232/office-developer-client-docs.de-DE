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
ms.openlocfilehash: 7513e361f4c1c1bcc93cc420f3a1987e0d817c54
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580502"
---
# <a name="ufromsz"></a>UFromSz

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Konvertiert eine mit Null endende Zeichenfolge der Nachkommastellen in ganze Zahl ohne Vorzeichen. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
```cpp
UINT UFromSz(
  LPCSTR lpsz
);
```

## <a name="parameters"></a>Parameter

 _lpsz_
  
> [in] Zeiger auf die Null-Zeichenfolge konvertiert werden soll. Der Parameter _Lpsz_ muss 65536 Zeichen nicht überschreiten. 
    
## <a name="return-value"></a>R�ckgabewert

 **UFromSz** gibt eine Ganzzahl ohne Vorzeichen zurück. Wenn die Zeichenfolge nicht mit mindestens eine Dezimalzahl beginnt, wird 0 (null) zurückgegeben. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Die Funktion **UFromSz** beendet konvertieren, wenn das erste Zeichen in der Zeichenfolge, die kein Dezimalzahl ist erreicht. Beispielsweise gibt **UFromSz** die Zeichenfolge "55" angegeben, den Ganzzahlwert 55. Die Zeichenfolge "5a5b" angegeben, gibt die Funktion den ganzzahligen Wert 5 zurück. Wenn die Zeichenfolge "a5b5", gibt **UFromSz** 0 (null) zurück. 
  
 **UFromSz** wird Kleinschreibung mit diakritischen Zeichen unterschieden. In den Formaten Unicode und DBCS Zeichenfolgen werden unterstützt. Die maximale Länge _Lpsz_ ist in Zeichen, was nicht notwendigerweise Bytes. 
  

