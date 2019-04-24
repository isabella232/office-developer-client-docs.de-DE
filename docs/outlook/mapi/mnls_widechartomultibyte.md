---
title: MNLS_WideCharToMultiByte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f64cde12-7ed1-444f-8ca4-51cb3ea514cf
description: 'Zuletzt geändert: 21, 2012'
ms.openlocfilehash: ad41f9b6060e5cfbabecfd9bb29a47815929d6b5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338731"
---
# <a name="mnlswidechartomultibyte"></a>MNLS_WideCharToMultiByte

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Diese Funktion ähnelt **WideCharToMultiByte**, wodurch eine Zeichenfolge vom Typ UTF-16 (Breitzeichen) einer neuen Zeichenfolge zugeordnet wird. Die neue Zeichenfolge ist nicht unbedingt aus einem Mehrbyte-Zeichensatz.
  
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
  
> in Codepage, die beim Ausführen der Konvertierung verwendet werden soll.
    
 _dwFlags_
  
> in Flags, die den Konvertierungs angeben.
    
 _lpWideCharStr_
  
> in Zeiger auf die zu konvertierende Unicode-Zeichenfolge.
    
 _cchWideChar_
  
> in Flags, die den Konvertierungs angeben.
    
 _lpMultiByteStr_
  
> [out] Optional. Zeiger auf einen Puffer, der die konvertierte Zeichenfolge empfängt.
    
 _cchMultiByte_
  
> in Die Größe des von _lpMultiByteStr_angegebenen Puffers in Byte.
    
 _lpDefaultChar_
  
> [in] Optional. Zeiger auf das Zeichen, das verwendet werden soll, wenn ein Zeichen nicht auf der angegebenen Codepage dargestellt werden kann.
    
 _lpfUsedDefaultChar_
  
> [out] Optional. Zeiger auf ein Flag, das angibt, ob die Funktion in der Konvertierung ein Standardzeichen verwendet hat.
    
## <a name="return-value"></a>Rückgabewert

Gibt die Anzahl der in den Puffer geschriebenen Bytes zurück, auf die durch _lpMultiByteStr_ , wenn erfolgreich, verwiesen wird. 
  
## <a name="remarks"></a>Bemerkungen

Diese Funktion umschließt die **WideCharToMultiByte** -Funktion. Weitere Informationen finden Sie unter [WideCharToMultiByte](https://msdn.microsoft.com/library/dd374130%28VS.85%29.aspx).
  
## <a name="see-also"></a>Siehe auch



[WideCharToMultiByte](https://msdn.microsoft.com/library/dd374130%28VS.85%29.aspx)

