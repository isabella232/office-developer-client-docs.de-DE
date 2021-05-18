---
title: IsBadBoundedStringPtr
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 888c60e3-7376-4d66-8ee2-ce81abafb185
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9d5ebb0e16138c3cc65ff6fd7c635e5498c9c1ba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278834"
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
  
> [in] Zeiger auf eine mit Null beendete ASCII-Zeichenfolge.
    
 _cchMax_
  
> [in] Die maximale Größe der Zeichenfolge in CHARs. Die Funktion überprüft den Lesezugriff in allen Zeichen bis zum beendenden Nullzeichen der Zeichenfolge oder bis zur durch diesen Parameter angegebenen Anzahl von Zeichen, je nach kleinerer Zahl. Wenn dieser Parameter null ist, ist der Rückgabewert null.
    
## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist Null, wenn der aufrufende Prozess Lesezugriff auf alle Zeichen bis zum beendenden Nullzeichen der Zeichenfolge hat, oder lesezugriff bis zur anzahl der von  _cchMax_ angegebenen Zeichen.
  
Der Rückgabewert ist nicht null, wenn der aufrufende Prozess nicht über Lesezugriff auf alle Zeichen bis zum beendenden Nullzeichen der Zeichenfolge verfügt, oder lesezugriff bis zur anzahl der von  _cchMax_ angegebenen Zeichen.
  
## <a name="remarks"></a>Hinweise

Die **IsBadBoundedStringPtr-Funktion** entspricht der Verwendung von **IsBadStringPtr**.
  
## <a name="see-also"></a>Siehe auch



[IsBadStringPtr](https://msdn.microsoft.com/library/windows/desktop/aa366714%28v=vs.85%29.aspx)

