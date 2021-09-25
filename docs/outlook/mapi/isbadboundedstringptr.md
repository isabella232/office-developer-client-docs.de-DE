---
title: IsBadBoundedStringPtr
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 888c60e3-7376-4d66-8ee2-ce81abafb185
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 00675aada9e2f7a9524552d1e3e0c71ea8d59683
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556273"
---
# <a name="isbadboundedstringptr"></a>IsBadBoundedStringPtr

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Überprüft, ob der aufrufende Prozess Lesezugriff auf den angegebenen Speicherbereich hat.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |mapiwin.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter.  <br/> |
   
```cpp
BOOL IsBadBoundedStringPtr(
  const void FAR* lpsz,
  UINT cchMax
);
```

## <a name="parameters"></a>Parameter

 _lpsz_
  
> [in] Zeiger auf eine MIT NULL beendete ASCII-Zeichenfolge.
    
 _cchMax_
  
> [in] Die maximale Größe der Zeichenfolge in CHARs. Die Funktion überprüft auf Lesezugriff in allen Zeichen bis zum endenden NULL-Zeichen der Zeichenfolge oder bis zur Anzahl der durch diesen Parameter angegebenen Zeichen, je nachdem, welche Zahl kleiner ist. Wenn dieser Parameter Null ist, ist der Rückgabewert Null.
    
## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist Null, wenn der aufrufende Prozess Lesezugriff auf alle Zeichen bis zum endenden NULL-Zeichen der Zeichenfolge hat, oder Lesezugriff bis zur Anzahl der durch  _cchMax_ angegebenen Zeichen hat.
  
Der Rückgabewert ist ungleich Null, wenn der aufrufende Prozess nicht über Lesezugriff auf alle Zeichen bis zum endenden NULL-Zeichen der Zeichenfolge oder Lesezugriff bis zur Anzahl der zeichen verfügt, die durch  _cchMax_ angegeben werden.
  
## <a name="remarks"></a>HinwBemerkungeneise

Die **IsBadBoundedStringPtr** -Funktion entspricht der Verwendung von **IsBadStringPtr**.
  
## <a name="see-also"></a>Siehe auch



[IsBadStringPtr](https://msdn.microsoft.com/library/windows/desktop/aa366714%28v=vs.85%29.aspx)

