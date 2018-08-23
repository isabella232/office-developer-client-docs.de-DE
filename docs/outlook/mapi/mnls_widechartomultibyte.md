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
ms.openlocfilehash: 6957888f6727175d73d277cf4f5b84dc234d22ea
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570037"
---
# <a name="mnlswidechartomultibyte"></a>MNLS_WideCharToMultiByte

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
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
  
## <a name="remarks"></a>HinwBemerkungeneise

Diese Funktion wird die Funktion **WideCharToMultiByte** umbrochen. Weitere Informationen finden Sie unter [WideCharToMultiByte](http://msdn.microsoft.com/en-us/library/dd374130%28VS.85%29.aspx).
  
## <a name="see-also"></a>Siehe auch



[WideCharToMultiByte](http://msdn.microsoft.com/en-us/library/dd374130%28VS.85%29.aspx)

