---
title: MNLS_WideCharToMultiByte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f64cde12-7ed1-444f-8ca4-51cb3ea514cf
description: 'Zuletzt geändert: 21 Februar 2012'
ms.openlocfilehash: f5cb63ca3d421073b00a448f762ecf0137494f2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793286"
---
# <a name="mnlswidechartomultibyte"></a>MNLS_WideCharToMultiByte

  
  
**Betrifft**: Outlook 
  
Diese Funktion ähnelt **WideCharToMultiByte**, der eine Zeichenfolge mit UTF-16 (Breitzeichen) in eine neue Zeichenfolge zugeordnet ist. Die neue Zeichenfolge ist nicht unbedingt aus einem multibyte-Zeichen festgelegt.
  
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
  
> [in] Codepage verwendet wird, in die Konvertierung ausgeführt.
    
 _dwFlags_
  
> [in] Flags, die den Typ für die Konvertierung angibt.
    
 _lpWideCharStr_
  
> [in] Zeiger auf die Unicode-Zeichenfolge konvertiert.
    
 _cchWideChar_
  
> [in] Flags, die den Typ für die Konvertierung angibt.
    
 _lpMultiByteStr_
  
> [out] Optional. Zeiger auf einen Puffer, der die konvertierte Zeichenfolge empfängt.
    
 _cchMultiByte_
  
> [in] Größe des Puffers durch _LpMultiByteStr_in Bytes.
    
 _lpDefaultChar_
  
> [in] Optional. Zeiger auf das Zeichen verwenden, wenn ein Zeichen in der angegebenen Codepage dargestellt werden kann.
    
 _lpfUsedDefaultChar_
  
> [out] Optional. Zeiger auf ein Flag, das angibt, ob die Funktion einer Standardwerte für die Zeichen in der Konvertierung verwendet hat.
    
## <a name="return-value"></a>R�ckgabewert

Gibt die Anzahl der in den Puffer auf den _LpMultiByteStr_ bei erfolgreicher geschriebenen Bytes zurück. 
  
## <a name="remarks"></a>Bemerkungen

Diese Funktion wird die Funktion **WideCharToMultiByte** umbrochen. Weitere Informationen finden Sie unter [WideCharToMultiByte](http://msdn.microsoft.com/en-us/library/dd374130%28VS.85%29.aspx).
  
## <a name="see-also"></a>Siehe auch



[WideCharToMultiByte](http://msdn.microsoft.com/en-us/library/dd374130%28VS.85%29.aspx)

