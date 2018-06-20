---
title: IsBadBoundedStringPtr
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 888c60e3-7376-4d66-8ee2-ce81abafb185
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 0e4e5d5910a7ff3551057760f065e79155d65e49
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792825"
---
# <a name="isbadboundedstringptr"></a>IsBadBoundedStringPtr

  
  
**Betrifft**: Outlook 
  
Überprüft, ob der aufrufende Prozess Lesezugriff auf den angegebenen Bereich des Arbeitsspeichers verfügt.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |mapiwin.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter.  <br/> |
   
```cpp
BOOL IsBadBoundedStringPtr(
  const void FAR* lpsz,
  UINT cchMax
);
```

## <a name="parameters"></a>Parameter

 _lpsz_
  
> [in] Zeiger auf eine mit Null endende ASCII-Zeichenfolge.
    
 _cchMax_
  
> [in] Die maximale Größe der Zeichenfolge in Zeichen. Die Funktion für Lesezugriff für alle Zeichen bis zu abschließendes Null-Zeichen der Zeichenfolge überprüft, oder bis zu die Anzahl der Zeichen, die von diesem Parameter angegebene, je nachdem, was kleiner ist. Wenn dieser Parameter auf 0 (null) ist, ist der Rückgabewert 0 (null).
    
## <a name="return-value"></a>R�ckgabewert

Der Rückgabewert ist 0 (null), wenn der aufrufende Prozess Lesezugriff für alle Zeichen bis zu abschließendes Null-Zeichen der Zeichenfolge oder Lesezugriff bis zu der Anzahl von Zeichen durch _CchMax_angegeben hat.
  
Der Rückgabewert ist ungleich NULL, wenn der aufrufende Prozess nicht Lesezugriff für alle Zeichen bis zu abschließendes Null-Zeichen der Zeichenfolge oder Lesezugriff bis zu der Anzahl von Zeichen durch _CchMax_angegeben wird.
  
## <a name="remarks"></a>Hinweise

Die Funktion **IsBadBoundedStringPtr** entspricht **IsBadStringPtr**verwenden.
  
## <a name="see-also"></a>Siehe auch



[IsBadStringPtr](http://msdn.microsoft.com/en-us/library/windows/desktop/aa366714%28v=vs.85%29.aspx)

