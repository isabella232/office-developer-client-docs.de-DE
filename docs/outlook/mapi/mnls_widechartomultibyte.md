---
title: MNLS_WideCharToMultiByte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: f64cde12-7ed1-444f-8ca4-51cb3ea514cf
description: 'Last modified: February 21, 2012'
ms.openlocfilehash: 13824c686c92901db5fa7849247b3be176aba961
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571394"
---
# <a name="mnls_widechartomultibyte"></a>MNLS_WideCharToMultiByte

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Diese Funktion ist ähnlich wie **WideCharToMultiByte**, das eine UTF-16-Zeichenfolge (Breitzeichen) einer neuen Zeichenzeichenfolge zuweist. Die neue Zeichenfolge stammt nicht unbedingt aus einem Mehrbyte-Zeichensatz.
  
```cpp
int MNLS_WideCharToMultiByte(
  UINT uCodePage,
  DWORD dwFlags,
  LPCWSTR lpWideCharStr,
  int cchWideChar,
  LPSTR lpMultiByteStr,
  int cchMultiByte,
  LPCSTR lpDefaultChar,
  BOOL FAR *lpfUsedDefaultChar);
```

## <a name="parameters"></a>Parameter

 _uCodePage_
  
> [in] Codepage, die beim Ausführen der Konvertierung verwendet werden soll.
    
 _Dwflags_
  
> [in] Kennzeichen, die den Konvertierungstyp angeben.
    
 _lpWideCharStr_
  
> [in] Zeiger auf die zu konvertierende Unicode-Zeichenfolge.
    
 _cchWideChar_
  
> [in] Kennzeichen, die den Konvertierungstyp angeben.
    
 _lpMultiByteStr_
  
> [out] Optional. Zeiger auf einen Puffer, der die konvertierte Zeichenfolge empfängt.
    
 _cchMultiByte_
  
> [in] Größe des Puffers in Byte, angegeben durch  _lpMultiByteStr_.
    
 _lpDefaultChar_
  
> [in] Optional. Zeiger auf das zu verwendende Zeichen, wenn ein Zeichen nicht auf der angegebenen Codepage dargestellt werden kann.
    
 _lpfUsedDefaultChar_
  
> [out] Optional. Zeiger auf ein Flag, das angibt, ob die Funktion ein Standardzeichen in der Konvertierung verwendet hat.
    
## <a name="return-value"></a>Rückgabewert

Gibt die Anzahl der Bytes zurück, die in den Puffer geschrieben wurden, auf den von  _lpMultiByteStr_ verwiesen wird, wenn dies erfolgreich war. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Diese Funktion umschließt die **WideCharToMultiByte-Funktion.** Weitere Informationen finden Sie unter [WideCharToMultiByte](https://msdn.microsoft.com/library/dd374130%28VS.85%29.aspx).
  
## <a name="see-also"></a>Siehe auch



[WideCharToMultiByte](https://msdn.microsoft.com/library/dd374130%28VS.85%29.aspx)

