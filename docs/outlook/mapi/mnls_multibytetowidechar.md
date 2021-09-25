---
title: MNLS_MultiByteToWideChar
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 065d78bf-4c9c-48dd-b1f1-b4e59f3f1243
description: 'Last modified: February 21, 2012'
ms.openlocfilehash: a5f0d0d3e209ec1bb1b87b822badcb581a540a35
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583968"
---
# <a name="mnls_multibytetowidechar"></a>MNLS_MultiByteToWideChar

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ähnlich wie **MultiByteToWideChar**, das eine Zeichenzeichenfolge einer UTF-16-Zeichenfolge (Breitzeichen) zuweist. Die Zeichenfolge stammt nicht unbedingt aus einem Mehrbyte-Zeichensatz.
  
```cpp
int MNLS_MultiByteToWideChar(
  UINT uCodePage,
  DWORD dwFlags,
  LPCSTR lpMultiByteStr,
  int cchMultiByte,
  LPWSTR lpWideCharStr,
  int cchWideChar);
```

## <a name="parameters"></a>Parameter

 _uCodePage_
  
> [in] Codepage, die beim Ausführen der Konvertierung verwendet werden soll.
    
 _Dwflags_
  
> [in] Kennzeichen, die den Konvertierungstyp angeben.
    
 _lpMultiByteStr_
  
> [in] Zeiger auf die zu konvertierende Zeichenfolge.
    
 _cchMultiByte_
  
> [in] Größe der durch den Parameter  _lpMultiByteStr_ angegebenen Zeichenfolge in Bytes. 
    
 _lpWideCharStr_
  
> [out] Optional. Zeiger auf einen Puffer, der die konvertierte Zeichenfolge empfängt.
    
 _cchWideChar_
  
> [in] Größe (in Zeichen) des Puffers, der durch  _lpWideCharStr_ angegeben wird.
    
## <a name="return-value"></a>Rückgabewert

Gibt die Anzahl der Zeichen zurück, die in den Puffer geschrieben wurden, der bei erfolgreicher Ausführung durch  _lpWideCharStr_ angegeben wird. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Diese Funktion umschließt die **MultiByteToWideChar-Funktion.** Weitere Informationen finden Sie unter [MultiByteToWideChar](https://msdn.microsoft.com/library/dd319072%28VS.85%29.aspx).
  

