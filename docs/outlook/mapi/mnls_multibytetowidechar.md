---
title: MNLS_MultiByteToWideChar
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 065d78bf-4c9c-48dd-b1f1-b4e59f3f1243
description: 'Zuletzt geändert: 21 Februar 2012'
ms.openlocfilehash: ab082c8ac70bf851097080fb41033f76bccc3044
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793276"
---
# <a name="mnlsmultibytetowidechar"></a>MNLS_MultiByteToWideChar

  
  
**Betrifft**: Outlook 
  
Vergleichbar mit der **MultiByteToWideChar**, der eine Zeichenfolge in einen String UTF-16 (Breitzeichen) zugeordnet ist. Die Zeichenfolge ist nicht unbedingt aus einem multibyte-Zeichen festgelegt.
  
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
  
> [in] Codepage verwendet wird, in die Konvertierung ausgeführt.
    
 _dwFlags_
  
> [in] Flags, die den Typ für die Konvertierung angibt.
    
 _lpMultiByteStr_
  
> [in] Zeiger auf die Zeichenfolge zu konvertieren.
    
 _cchMultiByte_
  
> [in] Größe in Bytes, der von der _LpMultiByteStr_ -Parameter angegebene Zeichenfolge. 
    
 _lpWideCharStr_
  
> [out] Optional. Zeiger auf einen Puffer, der die konvertierte Zeichenfolge empfängt.
    
 _cchWideChar_
  
> [in] Größe des Puffers durch _LpWideCharStr_in Zeichen.
    
## <a name="return-value"></a>R�ckgabewert

Gibt die Anzahl der Zeichen in den Puffer angegeben durch _LpWideCharStr_ bei erfolgreicher geschriebenen zurück. 
  
## <a name="remarks"></a>Bemerkungen

Diese Funktion wird die Funktion **MultiByteToWideChar** umbrochen. Weitere Informationen finden Sie unter [MultiByteToWideChar](http://msdn.microsoft.com/en-us/library/dd319072%28VS.85%29.aspx).
  

